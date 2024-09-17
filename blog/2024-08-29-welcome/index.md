---
slug: welcome
title: Como colaborar
authors: [enry6tz]
tags: [ docusaurus, markdown]
---

# Bienvenido a Docusaurus

Docusaurus es una herramienta moderna para la creación de sitios web estáticos, ideal para documentación, blogs, y mucho más. En esta guía, aprenderás cómo agregar un blog y cómo estructurar documentos dentro de tu proyecto Docusaurus.

<!-- truncate -->
![Docusaurus Plushie](./docusaurus-plushie-banner.jpeg)

## Comenzando

Para empezar, **clona el repositorio desde mi GitHub** y asegúrate de tener [Node.js](https://nodejs.org/en/download/) versión 18.0 o superior instalado en tu sistema. 

- **Node.js**: Se recomienda seleccionar todas las casillas relacionadas con dependencias al instalar Node.js.

## Clonar el repositorio

Clona el repositorio utilizando el siguiente comando:

```bash
git clone <URL_DE_TU_REPOSITORIO>
```

Reemplaza `<URL_DE_TU_REPOSITORIO>` con la URL del repositorio en tu GitHub.

Luego, navega al directorio del proyecto:

```bash
cd nombre-del-repositorio
```

Instala las dependencias necesarias con:

```bash
npm install
```

## Iniciar tu sitio

Corre el servidor de desarrollo con:

```bash
npm run start
```

Este comando construye tu sitio web localmente y lo sirve a través de un servidor de desarrollo, listo para que lo visualices en http://localhost:3000/.

Abre `docs/intro.md` (esta página) y edita algunas líneas: el sitio **se recargará automáticamente** y mostrará tus cambios.


## Agregar un Blog
Para empezar a usar el blog de Docusaurus, simplemente añade archivos Markdown (o carpetas) al directorio blog en tu proyecto. Cada archivo representa una entrada de blog. Aquí hay algunos ejemplos de cómo deberían verse los nombres de los archivos:
<br></br>
- 2019-05-30-hola.md
- 2019-05-29-hello-world/index.md
<br></br>


Los nombres de los archivos determinan la fecha del post, así que es importante seguir este formato. Si prefieres organizar tus imágenes junto con tus posts, puedes crear una carpeta para cada post, como se ve en este blog.


### Encabezados

Docusaurus utiliza **Front Matter**, estos metadatos generan automáticamente las páginas y organizarlas según tus configuraciones en el sitio.
```
---
slug: introduccion-docusaurus
title: Introducción a Docusaurus
authors: enry6tz
tags: [docusaurus, guía]
---
```

#### Desglose del Front Matter
- slug: ruta-del-archivo
El slug es la parte final de la URL que representa la página. Por ejemplo, si defines slug: ruta-del-archivo, la URL de la página será https://tusitio.com/ruta-del-archivo. Este parámetro permite controlar la ruta de acceso a la página.

- title: Titulo
Este campo define el título de la página o publicación. El título aparecerá en la parte superior de la página y también se utilizará en los metadatos para SEO (optimización de motores de búsqueda) y en el encabezado del navegador.

- authors: enry6tz
Este campo identifica al autor o autores del contenido. En este caso, "enry6tz" es el nombre del autor. Si tienes un archivo authors.yml, puedes definir autores recurrentes y referenciarlos aquí para gestionar fácilmente la atribución.

- tags: [docusaurus]
Las etiquetas o tags permiten categorizar el contenido. En este ejemplo, la etiqueta "docusaurus" ayuda a agrupar todas las publicaciones relacionadas con Docusaurus. Las etiquetas facilitan la navegación y búsqueda de contenido relacionado en tu sitio.

Uso del Front Matter
El front matter debe ir al principio del archivo Markdown, encerrado entre tres guiones --- al inicio y al final. 


>Puedes añadir autores recurrentes al archivo authors.yml, lo que te permite gestionar fácilmente quién escribe en tu blog.

>Soporte de Etiquetas
>El blog también soporta etiquetas, lo que te permite categorizar tus entradas y facilitar la navegación a los usuarios.



## Agregar Documentos
Docusaurus facilita la creación de documentación técnica a través de archivos Markdown que puedes organizar en el directorio docs. En tu plantilla de proyecto, los documentos se encuentran en:

```markdown
my-website
└── docs
    ├── doc1.md
    ├── doc2.md
    ├── doc3.md
    └── mdx.md
```
Estos archivos pueden estructurarse mediante un archivo sidebars.js, que define cómo se mostrarán los documentos en la barra lateral de navegación.



>   [Docusaurus blogging features](https://docusaurus.io/docs/blog) are powered by the [blog plugin](https://docusaurus.io/docs/api/plugins/@docusaurus/plugin-content-blog).
