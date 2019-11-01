# Prueba 1

Vamos a tratar de hacer un projecto desde cero.

Primero, vamos a definir que el sistema embebido que vamos a diseñar trabaja tiene una arquitectura ARM y no tiene sistema operativo (bare-metal). En base a eso, decidimos que el compilador `arm-none-eabi-gcc`. 

## Ejemplo 1

Escribimos el siguiente código en C:

```C
/******************************************************************************
 * Copyright (C) 2017 by Alex Fosdick - University of Colorado
 *
 * Redistribution, modification or use of this software in source or binary
 * forms is permitted as long as the files maintain this copyright. Users are 
 * permitted to modify this and use it to learn about the field of embedded
 * software. Alex Fosdick and the University of Colorado are not liable for any
 * misuse of this material. 
 *
 *****************************************************************************/

#include <stdio.h>

/* A pretty boring main file */
int main(void){

  printf("Hello World!\n");  /* Std-Library function call! */

  return 0;
}
```

y ejecutamos

```
arm-none-eabi-gcc -std=c99 -mcpu=cortex-m0plus -mthumb -Wall -S main.c -o main.s
```

para convertirlo en instrucciones de assembly, y obtenemos el siguiente resultado:

```
	.cpu cortex-m0plus
	.fpu softvfp
	.eabi_attribute 20, 1
	.eabi_attribute 21, 1
	.eabi_attribute 23, 3
	.eabi_attribute 24, 1
	.eabi_attribute 25, 1
	.eabi_attribute 26, 1
	.eabi_attribute 30, 6
	.eabi_attribute 34, 0
	.eabi_attribute 18, 4
	.code	16
	.file	"main.c"
	.section	.rodata
	.align	2
.LC0:
	.ascii	"Hello World!\000"
	.text
	.align	2
	.global	main
	.code	16
	.thumb_func
	.type	main, %function
main:
	push	{r7, lr}
	add	r7, sp, #0
	ldr	r3, .L3
	mov	r0, r3
	bl	puts
	mov	r3, #0
	mov	r0, r3
	mov	sp, r7
	@ sp needed
	pop	{r7, pc}
.L4:
	.align	2
.L3:
	.word	.LC0
	.size	main, .-main
	.ident	"GCC: (15:4.9.3+svn231177-1) 4.9.3 20150529 (prerelease)"
```


## Ejemplo 2

Puede ser que yo tenga una aplicación que use una librería `KL25z_UART.h` o una `MSP432_UART.h` dependiendo de la placa de desarrollo que esté usando. En ese caso, lo más correcto es tener en el código una instancia de validación por directivas del preprocesador:

```C
#if defined(KL25Z) && ! defined(MSP)
#include "kl25z.h"
#elif defined(MSP) && ! defined(KL25Z)
#include "msp.h"
#else
#error "Please specify only a single platform, -DKL25Z or -DMSP"
#endif

int main(void){

	...

}
```

y que en el momento de compilar, se le pase el macro `KL25Z` o el `MSP432` mediante la instrucción `-D<MACRO-NAME>`:

```
arm-none-eabi-gcc -DKL25Z -std=c99 ...
```

para que sepa qué placa usa.


## Ejemplo 3

En los sistemas embebidos los recursos son limitados. Está bueno usar librerías pre-hechas, pero es probable que esas librerías no estén optimizadas para el componente que nosotros estamos usando. Por eso, muchas veces hay que implementar sí o sí cosas desde cero.

Dentro de las librerías pre-compiladas, están las *static libraries* y las *shared libraries*. Tengo que revisar cuál es la diferencia entre cada una de ellas, pero las dos tienen el mismo tipo de header file.









