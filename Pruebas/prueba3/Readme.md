# Prueba 3: Primer intento de tutorial

## Introducción

¿Qué hace una computadora? Una computadora es un pequeño gran circuito que tiene una memoria llamada "memoria de programa" en donde se guardan las instrucciones que realiza cada vez que se resetea. Con esas instrucciones y un montón de circuitos lógicos más, la computadora va ejecutando tareas y comunicándose con el resto de sus periféricos. No hay mucho más. El resto, es relleno técnico. 

Sin embargo, hay muchas formas de realizar una tarea a partir de un código escrito en la memoria de programa. Por ejemplo, en un micro con un sistema operativo instalado, uno escribe un programa que luego será ejecutado por éste, pero nunca se escribe en la memoria de programa. 

## Programando un microcontrolador

Lo primero que hay que hacer para programar un microcontrolador es definir si se va a usar un sistema operativo o simplemente se va a escribir el código en la memoria del programa. Un sistema operativo es un conjunto de códigos que están escritos en la memoria del programa y que administran los tiempos del procesador, la memoria y otros recursos para simular tareas en paralelo. Más adelante se van a estudiar con más detalle los sistemas operativos, pero por el momento hay que saber que se puede escribir un programa en C para ser ejecutado en un sistema operativo determinado. 

Por ejemplo, cuando compilamos con `gcc` el siguiente código:

```C
#include <stdio.h>

int main(void){

	printf("Hola, mundo!\n");
	
	return 0;
}
```

estamos generando un archivo que va a poder ser ejecutado por el sistema operativo que estemos usando (Linux, Windows, etc.), el cual, a su vez, está escrito en memoria y sabe cómo hacer para ejecutar estos archivos. 

Otra cosa muy distinta es escribir un programa que va a ser escrito en la Flash y se va a ejecutar cada vez que el micro se resetee. Este tipo de aplicaciones se conocen como *Bare-Metal* y se usa este nombre en contraposición con la programación en un Sistema Operativo.

## Escribiendo un programa en C *Bare-Metal*

Gracias a los compiladores (y a mucha gente más, en realidad) es posible escribir un programa en lenguaje de alto nivel y traducirlo a código de máquina. El objetivo de esta parte va a consistir en estudiar un poco cómo se usa y qué hace el compilador. Esto nos va a permitir hacer programas en lenguaje de alto nivel, entender los programas que ya están hechos y optimizar los recursos de los microcontroladores (lo cual siempre es bueno, dado que son escasos).





## IDE vs Make

Tanto el Make como la IDE pueden verse como cajas negras que reciben los archivos donde están escritos los programas y la dirección donde está instalado el compilador, y devuelven los archivos necesarios para la ejecución o la escritura en la flash. Este proceso requiere muchas configuraciones y puede variar mucho internamente, por lo cual hay que saber exactamente lo que se está haciendo. La diferencia entre ellos es que en la IDE se configuran haciendo click las opciones y se generan automáticamente los archivos make (o incluso, a veces se generan otros archivos), mientras que en el Make, se definen los archivos a mano.


## TO DO: 

En labo de micros se aprende con suficiente profundidad la arquitectura de los micros y cómo programar en assembly. Entonces, como los alumnos ya saben lo más difícil, la secuencia de cosas que habría que explicar sería:

1. Repaso de arquitectura de computadoras, y conceptos básicos. Repaso de assembly.

2. Programación Bare Metal en C. Proceso de compilación (tiene que quedar claro que no es lo mismo programar con gcc que con arm-gcc). Uso de Makefiles (antes de usar la IDE, hay que saber qué es lo que hace).

3. Introducción a debuggeo de micros y comienzo de la segunda parte...



