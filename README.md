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
