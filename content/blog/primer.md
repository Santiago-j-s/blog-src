+++
date = "2017-04-25T23:14:03-03:00"
description = "Desc"
meta_img = "/images/image.jpg"
tags = []
title = "Como crear un blog con Hugo"

+++

[Hugo](http://gohugo.io) es un generador de páginas web estáticas muy sencillo de usar. ¿Qué es una página web estática? Simple, una página en la que el único trabajo que tiene que hacer el servidor HTTP es servir los archivos HTML, JS y CSS previamente generados, a diferencia de los sitios dinámicos en que el contenido HTML es generado por el servidor desde el código de algún lenguaje de programación (PHP por ejemplo) al momento de recibir una petición.

Los sitios estáticos tienen algunas ventajas tales como facilidad de mantenimiento y el poder alojar el sitio en casi cualquier lado.

### Pasos necesarios para crear el blog
Para empezar necesitamos instalar Hugo, si tienen el entorno del lenguaje de programación Go instalado todo lo que tienen que hacer es ejecutar los siguientes comandos en una terminal:
```bash
go get github.com/kardianos/govendor
govendor get github.com/spf13/hugo
go install github.com/spf13/hugo
```

También se puede instalar Hugo desde los binarios (Windows, Linux, OS X, FreeBSD) que se pueden encontrar [aquí](https://github.com/spf13/hugo/releases).

Una vez instalado sobre el directorio que va a alojar el blog ejecutamos:
```bash
hugo new site "blog"
```

que creará la siguiente estructura de directorios:
```bash
- blog
   - archetypes
   - config.toml
   - content
   - data
   - layouts
   - static
   - themes
```

Ya casi esta listo el sitio para empezar a escribir el contenido, pero todavía falta elegir un tema para nuestro blog antes de poder empezar a usarlo, en http://themes.gohugo.io/ tienen una amplia lista de temas disponibles para ver. En este caso instalaré el tema _cocoa-eh_, lo que tienen que hacer es descargar el tema de [aquí](https://github.com/fuegowolf/cocoa-eh-hugo-theme/releases), descomprimirlo dentro dentro de la carpeta _themes_, luego sobreescriban los archivos del directorio blog con los que se encuentran en _exampleSite_ dentro de la carpeta del tema.

Con esto la configuración esta lista, pueden probar el sitio usando el comando 
```bash
hugo serve -D 
```

Podrán entrar al sitio desde http://localhost:1313.