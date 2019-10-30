# Embedding-System-Programming

Repositorio con información, apuntes, links útiles y otras cosas sobre programación para sistemas embedbidos.

## Entorno de trabajo de los Sistemas Embebidos

Un sistema embebido es un sistema digital que cumple una aplicación específica. Estos sitemas están basados, generalmente, en un circuito con un microcontrolador, por lo que es necesario escribir un programa y bajarlo al circuito y verificar que cumpla bien todo lo que tenga que hacer. Este proceso muchas veces es muy complejo, por lo que se requiere de muchas herramientas para obtener un sistema embebido funcional. Este conjunto de herramientas se conoce como "enviroment", e incluye todos los programas capaces de escribir el programa, bajarlo al micro y testear todo el sistema.

El tema con el desarrollo de un sistema embebido es que, una vez desarrollada la aplicación, en algún momento voy a tener que hacer algo parecido, entonces yo quiero transportar lo que hice de alguna manera o compartirlo con un equipo, y para eso necesito hacer las cosas más o menos estandarizadas. También tengo que seguir un guideline de cómo escribir el código. Esto puede variar entre equipos, empresas, etc, pero me suena que deben ser todos más o menos parecidos.

El enviroment se compone de:

* Editor de texto
* Un programa que compile el código (Build stage, que se hace con el GNU toolchain)
* Installing (bajar el programa al micro)
* Debugging (gdb)

La IDE junta todas esas herramientas en un solo programa.


Platform components:

* Host Machine
* Development Enviroments
* Compiler Toolchain
* Development Kids
* Version Control


# 30-10-2019

Hoy empecé a ver el curso de Miro Samek con más detalle y me di cuenta de algunas cosas que paso a describir...

Para programar sistemas embebidos se trabaja primero en una placa placa de desarrollo como la EDU-CIAA o el Arduino UNO o lo que fuera. Ahí se desarrolla el código, los periféricos, se hacen pruebas, etc. hasta tener el sistema más o menos andando. Después, se hace un diseño más en serio hasta tener un prototipo comercial (o con los requerimientos que fueran). Básicamente, lo que se hace en sistemas embebidos es hacer el código del sistema digital fabricado (es decir, se programa el micro). Este proceso, en la práctica, consiste de varias instancias:
* Escribir el código en un lenguaje de alto nivel, usando un editor de texto.
* Compilar el código con algún compilador + organizador de instrucciones (GNU Make)
* Simular y/o debuggear el código compilado. Esto implica revisar instrucción por instrucción el código de bajo nivel y ver que ande todo como yo quiero.
La forma moderna de aprender a crear código para sistemas embebidos consiste en repetir este ciclo con programas cada vez más complejos. 

Estaría bueno seguir los ejemplos del curso de Samek, pero él usa el IAR. Por eso, primero voy a seguir haciendo el curso de Coursera (particularmente, el módulo 2 en el que practicás usar Make y las herramientas en las que no necesitás usar el IDE). 
