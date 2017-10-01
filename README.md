# Instrucciones

El presente documento pretende recopilar las instrucciones de uso de las plantillas de apuntes de `LaTeX` hechas por Ismael Aderdor <aderdor@gmail.com>.

### Objetivo

Este documento pretende ser una ayuda para tomar apuntes a LaTeX directamente en clase. Se encuentra organizado de tal manera que añadir distintas cosas clase tras clase sea sencillo.

### Licencias

Si está interesado acerca de las licencias que cubren estos archivos, puede echar un vistazo al archivo `LICENCIAS.md`.

### Archivos

A continuación se encuentra una lista que describe lo que hace (o debería de hacer) cada archivo y carpeta.

#### `apuntes.tex`

Es el archivo principal del documento. Es el que hay que compilar en caso de que se desee sacar el documento entero.

#### `INSTRUCCIONES.md`

Es el presente documento.

#### `LICENCIAS.md`

Este archivo contiene la totalidad de las licencias que afectan al código.

#### `img/`

Dentro de estas carpetas deberían de ir las distintas imágenes que estén dentro del documento.

#### `sty/comandos.sty`

En este archivo se hallan definidos algunos comandos de `LaTeX`. Debería modificarse según la necesidad de el trabajo a realizar.

**IMPORTANTE**: Todas las definiciones de comandos, teoremas, ambientes y demás debería de realizarse en este archivo para que si en algún momento sedecidiese cambiar algo afectase al documento entero y no únicamente a partes.

### `sty/paquetes.sty`

Este archivo carga todos los paquetes necesarios para que compile el documento, así como algunas opciones de los propios paquetes. Declarándolos aquí en vez de en `apuntes.tex` conseguimos mayor limpieza y modularidad en el documento.

### `sty/titulo.sty`

En este archivo se encuentran las variables que modifican el título, descripción, autor y editor que posteriormente se aplicarán a la portada del documento.

#### `tex/`

Dentro de esta carpeta deberían de ir la totalidad de los archivos `.tex`, a excepción de `apuntes.tex`, que es el documento padre.

Cada tema o capítulo debería de tener un archivo `.tex` a parte.

#### `tex/titulo.tex`

Este documento es el que genera la portada de los apuntes.

#### `tex/intro.tex`

En este archivo se incluye la introducción de los apuntes. Aquí se deberían de anotar algunas cosas de imporancia de la asignatura tales como:

* Contacto con profesores
* Tutorías
* Evaluación
* Recursos de la asignatura
* Algún dato interesante

#### `tex/modelo.tex`

Este archivo es un modelo para generar los distintos capítulos de los que estén conformados los apuntes.

## Funcionamiento

#### Compilar

Para compilar los archivos generados es necesario usar `XeTeX` o `XeLaTeX`. Personalmente, uso el IDE `TeXmaker` para trabajar con este tipo de proyectos. Sin embargo, puede usarse directamente el comando `xelatex` con las opciones necesarias.

## TODO

Las siguientes características serán (o no) implementadas en un futuro:

* Inicialización de la plantilla de apuntes
* Script de borrado de archivos de registro de LaTeX
