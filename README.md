# Curso Práctico de Git

## Programa de Estudios

+ **Flujo de Trabajo Básico de Git.** Introducción a Git y sus características principales.
+ **Operaciones Importantes de Git.** Aprende diferentes maneras de deshacer los cambios realizados en un proyecto y cuándo utilizarlas.
+ **Operaciones Git Prácticas.** Aprende cómo utilizar los comandos esenciales de Git que facilitan las tareas diarias.

## Flujo de Trabajo Básico de Git

## *¿Qué es Git?*

Git es un software de línea de comandos que permite realizar un **seguimiento** de los cambios realizados en un proyecto a lo largo del tiempo. Su funcionamiento se basa en registrar los cambios que se realizan en un proyecto y permitir que un programador los consulte cuando sea necesario.

> Diseñado por Linus Torvalds, pensando en la eficiencia, la confiabilidad y compatibilidad del mantenimiento de versiones de aplicaciones informáticas cuando estas tienen un gran número de archivos de código fuente.

### Flujo de Trabajo de Git

Un proyecto Git se puede concebir como compuesto por tres partes:

+ **Directorio de Trabajo (Working Directory).** Donde se realiza todo el trabajo: crear, editar, eliminar y organizar archivos.
+ **Área de Preparación (Staging Area).** Donde se listan los cambios realizados en el directorio de trabajo.
+ **Repositorio (Repository).** Donde se almacenan permanentemente esos cambios como diferentes versiones del proyecto.

El siguiente diagrama ilustra las tres partes del flujo de trabajo de Git.

![Flujo de Trabajo de Git](https://dungeonofbits.com/images/tranajarcongit1.jpg)

El flujo de trabajo en Git consiste en modificar archivos dentro del directorio de trabajo, añadirlos al área de preparación y luego registrar los cambios en un repositorio. En este sistema, los cambios se almacenan mediante confirmaciones, que actúan como instantáneas de una rama específica dentro del repositorio. Estas confirmaciones permiten mantener un registro del desarrollo de todas las ramas, creando un historial detallado de la evolución del proyecto en Git.