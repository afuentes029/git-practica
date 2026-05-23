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

![Flujo de Trabajo de Git](https://media.licdn.com/dms/image/v2/D4E22AQF5D6cmPxZBTQ/feedshare-shrink_800/feedshare-shrink_800/0/1708835401420?e=2147483647&v=beta&t=BvgzqaH8bM4ETA6xbh1Jta3Dnc-lLtZ0jLKnL5USGm4 | height="300")

El flujo de trabajo de Git consiste en modificar archivos en el directorio de trabajo, agregarlos al área de preparación y luego guardar los cambios en un repositorio Git. En este sistema, los cambios se almacenan mediante confirmaciones (commits), que actúan como instantáneas de una rama específica en un repositorio.

En conjunto, las confirmaciones representan el historial de crecimiento de las ramas en un repositorio Git. La confirmación más reciente se considera directamente relacionada con el puntero de la rama actual.

### *Cómo Comprobar el Estado de un Repositorio Git*

El comando git status se utiliza en un repositorio Git para obtener su estado actual, incluyendo la confirmación actual, los archivos modificados y los archivos nuevos que no esté siendo rastreado por Git.

La salida del comando puede variar considerablemente y a menudo incluye mensajes útiles para guiar al usuario en la gestión de su repositorio. Por ejemplo, mostrará al usuario los archivos que confirmaría ejecutando git commit y los que podría confirmar ejecutando git add antes de ejecutar git commit.

Para verificar el estado de los cambios realizados, ejecute el siguiente comando:

	git status

Podrás ver el estado del directorio de trabajo y el área de preparación. Indica qué archivos no están bajo seguimiento (mostrados en rojo) y cuáles están bajo seguimiento y preparados para su confirmación (mostrados en verde). Los archivos en verde se encuentran en el área de preparación y serán incluidos en el próximo commit.

### *Agregar Cambios al Área de Preparación*

El comando git add se utiliza para agregar los cambios del directorio de trabajo al área de preparación. Una vez que los cambios se hayan preparado, puedes usar el comando git commit para guardarlos de forma permanente en el repositorio.

Para agregar un archivo al área de preparación, ejecute el siguiente comando:

	git add filename

La palabra filename se refiere al nombre del archivo que está editando, como por ejemplo scene-1.txt.

Este comando ofrece a los desarrolladores la posibilidad de elegir qué cambios desean registrar, proporcionando un control preciso sobre el historial de versiones y permitiendo realizar confirmaciones más organizadas y coherentes en cualquier flujo de trabajo de Git.

### *Visualización de Diferencias con Git Diff*

El comando git diff mostrará las diferencias entre el directorio de trabajo y el área de preparación en un archivo específico. Úselo antes de agregar contenido nuevo para asegurarse de que está realizando los cambios esperados.

Para verificar las diferencias entre el directorio de trabajo y el área de preparación, ejecute el siguiente comando:

	git diff filename

Aquí, filename es el nombre del archivo. Si el nombre del archivo fuera changes.txt, el comando sería:

	git diff changes.txt

### *Confirmando tu Código*

El comando git commit crea una nueva confirmación que contiene:

+ El contenido actual del área de preparación.
+ Un mensaje de registro que describe los cambios en el repositorio.

Un commit es el último paso en nuestro flujo de trabajo de Git. Este proceso almacena permanentemente los cambios que se encuentran en el área de preparación dentro del repositorio. Por lo general, se utiliza en combinación con el comando git add, ya que este último se usa para agregar archivos al área de preparación antes de ser confirmados.

Para realizar la confirmación, ejecute el siguiente comando:

	git commit -m "mensaje de confirmación"

Convenciones estándar para los mensajes de confirmación:

+ Debe ir entre comillas doble.
+ Escrito en tiempo presente.
+ Debe ser breve (50 caracteres o menos) cuando se utilice la opción -m.

La opción -m permite ingresar el mensaje de confirmación directamente en la línea de comandos, evitando así la necesidad de abrir el editor de texto para escribirlo.

Las confirmaciones se registran de forma cronológica en el repositorio y se pueden consultar ejecutando el comando git log.

### *Mostrando los Registros de Confirmación de Git*

El comando git log muestra el historial de confirmaciones de una rama. Para cada confirmación se muestra lo siguiente:

- Un código de 40 caracteres, llamado SHA, que identifica de forma única la confirmación.
- El autor de la confirmación.
- La fecha y hora de la confirmación.
- El mensaje de confirmación.

Para ver los registros de confirmación, ejecute el siguiente comando:

	git log

Este comando es útil cuando se necesita volver a una versión anterior de un proyecto. El código SHA único permite identificar un punto en el historial del proyecto al que se desea regresar.

## Operaciones Importantes de Git

### *Introducción al Retroceso*

Al trabajar en un proyecto Git, a veces hacemos cambios que queremos deshacer. Para ello, Git ofrece algunas funciones que nos permiten corregir errores durante la creación del proyecto. En esta sección, aprenderemos algunas de estas funciones.

### *Mostrando el Registro de Confirmación más Reciente*

En Git, la confirmación en el que te encuentras actualmente se conoce como la HEAD commit. HEAD es una referencia simbólica (un puntero) a la confirmación actual o a la última instantánea del directorio de trabajo.

Para ver la confirmación más reciente, ejecute el siguiente comando:

	git show HEAD

La salida de este comando mostrará toda la información que muestra el comando git log para la HEAD commit, además de todos los cambios realizados en los archivos que se confirmaron.
