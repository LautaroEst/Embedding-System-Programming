# Prueba 2

Vamos a tratar de hacer un ejemplo un poco más trabajado. Estamos practicando con el ejmplo v3 del demo m2.

Quiero compilar los archivos `.c` con el compilador `arm-none-eabi-gcc` porque estoy trabajando con una arquitectura ARM y no tengo un sistema operativo. Además, dado que tengo para elegir entre las placas KL25Z y MSP432, voy a crear una librería para cada una de ellas. Cada una de estas librerías consiste en un único archivo que contiene una única función:


```
Líbrería para KL25Z:
	|
	|----> inc
	|		|
	|		|----> kl25.h
	|
	|----> src
	|		|
	|		|----> kl25.c


Líbrería para MSP432:
	|
	|----> inc
	|		|
	|		|----> msp.h
	|
	|----> src
	|		|
	|		|----> msp.c
```

En los archivos `.c` de las librerías puedo incluír funciones de otra librería.

