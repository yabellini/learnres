# Contribuir a learnres

Este documento es una guía para proponer un cambio en learnres. 
Para obtener información más detallada sobre cómo contribuir a este, y otros paquetes ordenados, por favor revisa la 
[**guía de contribución al desarrollo**](https://rstd.io/tidy-contrib). 

Como este es un paquete que solo contiene plantilla para tutoriales no encontrarás archivos `.R` o `.Rd` para editar.

## Arreglar los errores en el texto

Puedes corregir errores de escritura, ortografía o gramaticales en la documentación directamente usando la interfaz web de GitHub, siempre y cuando los cambios se hagan en el archivo _source_. 

Esto generalmente significa que necesitarás editar el archivo skeleton.Rmd.  Para entender mejor como funcionan las plantillas de rmkardown por favor revisa [esta guía](https://usethis.r-lib.org/reference/use_rmarkdown_template.html) y chequea el sitio de [learnr](https://rstudio.github.io/learnr/) para entender como funcionan los tutoriales basados en `learnr`.

## Cambios más grandes

Si quieres hacer un cambio mayor, es una buena idea presentar primero un problema y asegurarse de que alguien del equipo esté de acuerdo en que es necesario. 
Si encontraste un error, por favor, crea un issue que ilustre el error con un ejemplo mínimo ([reprex](https://www.tidyverse.org/help/#reprex), esto también te ayudará a escribir un unit test, si es necesario).

### Proceso de Pull requests

* Crea un fork del paquete y clonalo en tu computadora. Si nunca hicistes esto, te recomendamos que uses `usethis::create_from_github("yabellini/learnres", fork = TRUE)`.

* Instala todas las dependencias de desarrollo con `devtools::install_dev_deps()`, y luego asegúrate de que el paquete pase el chequeo R CMD ejecutando `devtools::check()`. 
    Si el chequeo R CMD no pasa completamente, es una buena idea pedir ayuda antes de continuar. 
* Crea una nueva rama Git para tu pull request (PR). Recomendamos usar `usethis::pr_init("breve descripción del cambio")`.

* Haz tus cambios, crea un commit con git, y luego crea un PR ejecutando `usethis::pr_push()`, y siguiendo las indicaciones de tu navegador.
    El título de tu PR debería describir brevemente el cambio.
    El cuerpo de tu PR debe contener "Arreglo #número-de-issue".

Traducción realizada con la versión gratuita del traductor www.DeepL.com/Translator

### Estilo de código

* El nuevo código debe seguir la [guía de estilo] tidyverse (https://style.tidyverse.org). 
    Puedes usar el paquete [styler](https://CRAN.R-project.org/package=styler) para aplicar estos estilos, pero por favor no cambies el estilo de código que no tiene nada que ver con tu PR.  

* Usamos [roxygen2](https://cran.r-project.org/package=roxygen2), con [sintaxis Markdown](https://cran.r-project.org/web/packages/roxygen2/vignettes/rd-formatting.html), para la documentación.  

* Usamos [testthat](https://cran.r-project.org/package=testthat) para hacer unit tests. 
   Las contribuciones con tests incluidos son más fáciles de aceptar.

## Código de Conducta

Este proyecto incluye un [Código de Conducta](https://github.com/yabellini/learnres/blob/main/CONDUCT.md). Al contribuir en este paquete, aceptás complir con este código.
