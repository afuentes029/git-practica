# Curso Práctico de Git y GitHub

## ¿Qué es Git?

Git es un software de línea de comandos que permite realizar un **seguimiento** de los cambios realizados en un proyecto a lo largo del tiempo. Su funcionamiento se basa en registrar los cambios que se realizan en un proyecto y permitir que un programador los consulte cuando sea necesario.

### Flujo de Trabajo de Git

Un proyecto Git se puede concebir como compuesto por tres partes:

+ **Directorio de Trabajo (Working Directory).** Donde se realiza todo el trabajo: crear, editar, eliminar y organizar archivos.
+ **Área de Preparación (Staging Area).** Donde se listan los cambios realizados en el directorio de trabajo.
+ **Repositorio (Repository).** Donde se almacenan permanentemente esos cambios como diferentes versiones del proyecto.

El siguiente diagrama ilustra las tres partes del flujo de trabajo de Git.

![alt Flujo de Trabajo de Git](https://dungeonofbits.com/images/tranajarcongit1.jpg)

El flujo de trabajo en Git consiste en modificar archivos dentro del directorio de trabajo, añadirlos al área de preparación y luego registrar los cambios en un repositorio. En este sistema, los cambios se almacenan mediante confirmaciones, que actúan como instantáneas de una rama específica dentro del repositorio. Estas confirmaciones permiten mantener un registro del desarrollo de todas las ramas, creando un historial detallado de la evolución del proyecto en Git.

## ¿Qué es GitHub?

GitHub es un sitio web como un **servicio** que facilita el desarrollo de software al permitirte almacenar tu código en contenedores, llamados repositorios , y al realizar un seguimiento de los cambios realizados en tu código. Además, ofrece un servicio de alojamiento y herramientas para compilar, probar e implementar código.