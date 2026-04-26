# Aprende Git. Introducción

## Programa de Estudios

+ **Flujo de Trabajo Básico de Git.** Introducción a Git y sus características principales.
+ **Operaciones Importantes de Git.** Aprende diferentes maneras de deshacer los cambios realizados en un proyecto y cuándo utilizarlas.
+ **Operaciones Git Prácticas.** Aprende cómo utilizar los comandos esenciales de Git que facilitan las tareas diarias.

## Flujo de Trabajo Básico de Git

### *¿Qué es Git?*

Git es un software de línea de comandos que permite realizar un **seguimiento** de los cambios realizados en un proyecto a lo largo del tiempo. Su funcionamiento se basa en registrar los cambios que se realizan en un proyecto y permitir que un programador los consulte cuando sea necesario.

> Diseñado por Linus Torvalds, pensando en la eficiencia, la confiabilidad y compatibilidad del mantenimiento de versiones de aplicaciones informáticas cuando estas tienen un gran número de archivos de código fuente.

### *Inicializando un Repositorio Git*

El comando git init inicializa un repositorio Git vacío. Crea un directorio .git con todas las herramientas y datos necesarios para gestionar las versiones del proyecto. Este comando solo debe usarse una vez por proyecto para completar la configuración inicial.

Para configurar la carpeta de un proyecto como un nuevo repositorio Git, ejecute el siguiente comando:

	git init

La palabra init significa inicializar. Al comenzar un nuevo proyecto, este es el primer paso para realizar un seguimiento de los cambios en los archivos y carpetas del proyecto.

### *Flujo de Trabajo de Git*

Un proyecto Git se puede concebir como compuesto por tres partes:

+ **Directorio de Trabajo (Working Directory).** Donde se realiza todo el trabajo: crear, editar, eliminar y organizar archivos.
+ **Área de Preparación (Staging Area).** Donde se listan los cambios realizados en el directorio de trabajo.
+ **Repositorio (Repository).** Donde se almacenan permanentemente los cambios como diferentes versiones del proyecto.

El siguiente diagrama ilustra las tres partes del flujo de trabajo de Git.

![Flujo de Trabajo de Git](https://media.licdn.com/dms/image/v2/D4D22AQHe0747v5fyCg/feedshare-shrink_2048_1536/feedshare-shrink_2048_1536/0/1719818487506?e=2147483647&v=beta&t=u6BghJ8p6TWBe5JSxkEa6dpkccvgpHyXAjCI2-OrzJA)

El flujo de trabajo de Git consiste en modificar archivos en el directorio de trabajo, agregarlos al área de preparación y luego guardar los cambios en un repositorio Git. En este sistema, los cambios se almacenan mediante confirmaciones (commits), que actúan como instantáneas de una rama específica en un repositorio.

En conjunto, las confirmaciones representan el historial de crecimiento de las ramas en un repositorio Git. La confirmación más reciente se considera directamente relacionada con el puntero de la rama actual.

### Cómo Comprobar el Estado de un Repositorio Git

El comando git status se utiliza en un repositorio Git para obtener su estado actual, incluyendo la confirmación actual, los archivos modificados y los archivos nuevos que no esté siendo rastreado por Git.

La salida del comando puede variar considerablemente y a menudo incluye mensajes útiles para guiar al usuario en la gestión de su repositorio. Por ejemplo, mostrará al usuario los archivos que confirmaría ejecutando git commit y los que podría confirmar ejecutando git add antes de ejecutar git commit.

Para verificar el estado de los cambios realizados, ejecute el siguiente comando:

	git status

Podrás ver el estado del directorio de trabajo y el área de preparación. Indica qué archivos no están bajo seguimiento (mostrados en rojo) y cuáles están bajo seguimiento y preparados para su confirmación (mostrados en verde). Los archivos en verde se encuentran en el área de preparación y serán incluidos en el próximo commit.
