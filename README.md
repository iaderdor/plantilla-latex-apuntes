# plantilla-latex-apuntes

plantilla-latex-apuntes es una recopilación de documentos de LaTeX pensados para facilitar la realización de apuntes. Para ello, hace uso de varios paquetes propios de LaTeX con la intención de evitar el típico archivo de Algebra.tex de 15000 líneas.

## ¿Cómo funciona?

El paradigma en el que se basa principalmente esta plantilla es en el divide y vencerás. Para facilitar la gestión, escritura y depuración de errores, se ha dividido el documento en varias carpetas y archivos.

Para gestionar los paquetes, comandos definidos por el usuario y la portada, se han generado varios paquetes, concretamente los siguientes:

 * `paquetes.sty` Contiene todos los paquetes que se desean cargar.
 * `comandos.sty` Contiene todos los comandos definidos por el usuario.
 * `titulo.sty`   Contiene todos los datos necesarios para generar la portada de los apuntes.

Del mismo modo, se han generado dos carpetas. `img/` tiene como propósito servir para juntar todas las imágenes. Dentro de `tex/` se encuentran todos los archivos que generarán el documento. Para ello se hace uso del paquete `subfiles`.

El archivo `apuntes.tex` aglutina todo, generando el documento final que deseamos.


## Uso

Para descargar la plantilla, recomiendo clonar directamente el respositorio desde github:

```
    git clone 
```

Sin embargo, sino tienes git o no te sientes a gusto con ello, también puedes descargarte las plantillas en ZIP.

    [plantillas-apuntes-latex.zip](https://github.com/iaderdor/plantilla-latex-apuntes/archive/master.zip)

Te recomiendo eliminar los siguientes archivos y carpetas:

    * `.gitignore`
    * `git/`

### Creando el proyecto

Llegados a este punto, hay que darle un nombre al proyecto. Esto lo conseguirás haciendo lo siguiente:

    1. Cambia el nombre de la carpeta `plantillas-latex-apuntes` por uno que se corresponda con el uso que le vas a dar.
    2. Abre el archivo `sty/titulo.sty` y cambia los parámetros por los que desees que aparezcan en la portada.
    3. Del mismo modo, dentro de la carpeta `tex/`, es muy probable que quieras modificar los siguientes archivos:
     * `intro.tex`
     * `licencia.tex`
     * `prefacio.tex`

### Creando un nuevo capítulo

Para crear un nuevo capítulo, sigue los siguientes pasos:

    1. Copia `tex/modelo.tex` en `tex/capituloN.tex`.
    2. Añade a `apuntes.tex` después de `\mainmatter` lo siguiente:

    ```
        \subfile{tex/capituloN}
    ```
    3. Ya puedes editar `tex/capituloN.tex` como necesites.

### Compilando un documento

Para compilar un documento necesitarás usar XeLaTeX. Este es un compilador para el lenguaje de LaTeX pero creado en el siglo XXI (LaTeX vio la patita en 1984, allá por la prehistoria de la informática).

Usar XeLaTeX no es ningún problema. Suele instalarse junto con MiKTeX, texlive y demás distribuciones de LaTeX. Si usas un IDE, probablemente tengas una pestaña en la que puedas elegir el compilador que quieras usar en la barra de herramientas. Si eres más aficionado a la línea de comandos, el comando que buscas es `xelatex`.


###Licencias

Este proyecto se distribuye mediante la licencia MIT. Puedes ver dicha licencia en el archivo `LICENCIAS.md`. Por otro lado, la plantilla del título `tex/titulo.tex` se distribuye mediante la licencia de [CC BY-NC-SA 3.0](http://creativecommons.org/licenses/by-nc-sa/3.0/) y fue originalmente creado por Peter Wilson <herries.press@earthlink.net>.

###Archivos

A continuación se encuentra una lista que describe lo que hace (o debería de hacer) cada archivo y carpeta.

####`apuntes.tex`

Es el archivo principal del documento. Es el que hay que compilar en caso de que se desee sacar el documento entero.

####`INSTRUCCIONES.md`

Es el presente documento.

####`LICENCIAS.md`

Este archivo contiene la totalidad de las licencias que afectan al código.

####`img/`

Dentro de estas carpetas deberían de ir las distintas imágenes que estén dentro del documento.

####`sty/comandos.sty`

En este archivo se hallan definidos algunos comandos de `LaTeX`. Debería modificarse según la necesidad de el trabajo a realizar.

**IMPORTANTE**: Todas las definiciones de comandos, teoremas, ambientes y demás debería de realizarse en este archivo para que si en algún momento sedecidiese cambiar algo afectase al documento entero y no únicamente a partes.

###`sty/paquetes.sty`

Este archivo carga todos los paquetes necesarios para que compile el documento, así como algunas opciones de los propios paquetes. Declarándolos aquí en vez de en `apuntes.tex` conseguimos mayor limpieza y modularidad en el documento.

###`sty/titulo.sty`

En este archivo se encuentran las variables que modifican el título, descripción, autor y editor que posteriormente se aplicarán a la portada del documento.

####`tex/`

Dentro de esta carpeta deberían de ir la totalidad de los archivos `.tex`, a excepción de `apuntes.tex`, que es el documento padre.

Cada tema o capítulo debería de tener un archivo `.tex` a parte.

####`tex/titulo.tex`

Este documento es el que genera la portada de los apuntes.

####`tex/intro.tex`

En este archivo se incluye la introducción de los apuntes. Aquí se deberían de anotar algunas cosas de imporancia de la asignatura tales como:

* Contacto con profesores
* Tutorías
* Evaluación
* Recursos de la asignatura
* Algún dato interesante

####`tex/modelo.tex`

Este archivo es un modelo para generar los distintos capítulos de los que estén conformados los apuntes.

## TODO

En esta sección se pueden encontrar las características que se desean implementar en un futuro. Entre las consideradas importantes se encuentran las siguientes:

 * Reorganizar la carpeta `tex/` para mejorar la colocación de los distintos capítulos.
 * Sustituir el texto de los distintos 
 * Realizar una versión en inglés de los apuntes.

A largo plazo, pretendo implementar las siguientes funcionalidades:

 * Script para borrar los archivos de registro de latex.
 * Hacer una herramienta para crear nuevos proyectos, crear capítulos y gestionar el proyecto.


## Autor

El autor de este proyecto es Ismael Aderdor Domingo <aderdor@gmail.com>.
