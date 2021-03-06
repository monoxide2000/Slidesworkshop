---
title       : Reportes dinámicos con R y RStudio
subtitle    : Introducción a los paquetes knitr y rmarkdown
author      : Julio César Ramírez Pacheco
job         : Universidad del Caribe
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax,quiz, bootstrap, interactive] # {mathjax, quiz, bootstrap}
ext_widgets : {rCharts: [libraries/nvd3, libraries/leaflet, libraries/dygraphs]}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
logo        : unicaribelogo.jpeg
biglogo     : unicaribelogo.jpeg
assets      : {assets: ../../assets}
---

<style type="text/css">
body {background:grey transparent;
}
</style>



## Reportes dinámicos
> - La forma tradicional de escribir reportes es producir los gráficos en un software como `R` y guardarlos en formato `PDF` o `PNG`. Posteriormente se incluye en un editor (o de composición) de textos estos gráficos en conjunto con la descripción de sus resultados.
.
> - Un reporte realizado de esta manera puede causar problemas ya que si los análisis se realizan con un conjunto más pequeño de los datos, el reporte tiene que rehacerse siguiendo los mismos pasos.
> - Un documento, por lo tanto, es dinámico si contiene código y la narrativa de las figuras, tablas, etc. Si los datos cambian, simplemente ejecutamos de nuevo el programa para obtener un nuevo documento.

> - Los reportes dinámicos permiten de igual forma obtener reportes reproducibles si se comparte de igual forma los códigos y los datos utilizados. 


--- .class #id 

## Reportes dinámicos en `R`.

> - R permite generar reportes dinámicos utilizando los paquetes `markdown`, `rmarkdown` y `knitr`.
> - Los reportes generados en `rmarkdown` pueden ser de tipo `PDF`, `Word`, `html`, `markdown`, etc.
> - Para generar estos reportes es necesario ejecutar en la consola de `R`, el comando 

> - ```{r, eval=FALSE} 
ìnstall.packages(c("rmarkdown", "knitr"), dependencies = TRUE)
``` 
> - Usualmente, `RStudio` instala por defecto los paquetes `rmarkdown` y `knit`. Si este es el caso, entonces simplemente cargamos los paquetes usando `library(c(rmarkdown, knitr))`

--- .segue bg:grey

## R Markdown

---


## R Markdown (mecánica de generación)
- Flujo de trabajo:

<img src="./assets/img/flujo.jpg" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" width="100%" />

- `RStudio` contiene un sólo botón que realiza todas estas tareas y produce un documento como resultado.

--- .class #id 

## R Markdown (Empezando con `RStudio`)
- Flujo de trabajo:

<img src="./assets/img/rstudioOpen.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" width="80%" style="display: block; margin: auto;" />

--- .class #id 

## R Markdown (sintaxis)

<img src="./assets/img/markdown1.png" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" width="80%" style="display: block; margin: auto;" />

--- .class #id

## R Markdown (sintaxis), cont.

<img src="./assets/img/markdown2.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" width="90%" style="display: block; margin: auto;" />

--- .class #id 

## R Markdown (definición del encabezado YAML)

<img src="./assets/img/yaml.jpg" title="plot of chunk unnamed-chunk-5" alt="plot of chunk unnamed-chunk-5" width="75%" style="display: block; margin: auto;" />

--- .class #id 


## R Markdown (inserción de código)

<img src="./assets/img/chunk.png" title="plot of chunk unnamed-chunk-6" alt="plot of chunk unnamed-chunk-6" width="75%" style="display: block; margin: auto;" />

--- .class #id 


## R Markdown (opciones de código)

<img src="./assets/img/options.png" title="plot of chunk unnamed-chunk-7" alt="plot of chunk unnamed-chunk-7" width="75%" style="display: block; margin: auto;" />

--- .class #id 


## R Markdown (finalmente genera el documento)

<img src="./assets/img/generate.png" title="plot of chunk unnamed-chunk-8" alt="plot of chunk unnamed-chunk-8" width="90%" style="display: block; margin: auto;" />

--- .segue bg:grey

## Elementos interactivos

---

## Paquetes que mejoran la estética del documento

- Paquetes como `highcharter`, `tutorial`, `rCharts`, `dygraphs`, `iquiz`, `prettydoc` mejoran significativamente la estética del documento final, siempre y cuando el documento generado sea en formato `HTML`.

- Para el caso de los documentos `PDF`, éstos se pueden incluir, sin embargo, se pierde la interacción con el reporte.

- Ahora iniciemos creando un documento en `R Markdown`.


--- .class #id



