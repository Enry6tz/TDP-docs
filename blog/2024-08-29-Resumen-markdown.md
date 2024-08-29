---
slug: guide-markdown
title: Guia resumen Markdown
authors: enry6tz
tags: [ docusaurus]
---

Markdown es un lenguaje de marcado ligero que permite formatear texto de manera simple y eficiente. Es ampliamente utilizado en proyectos de documentación, blogs y sitios web. Esta guía te proporcionará un resumen básico de Markdown para que puedas comenzar a contribuir de inmediato.

<!-- truncate -->

## ¿Qué es Markdown?

Markdown es un lenguaje de marcado que convierte texto plano en HTML estructurado. Su sintaxis es fácil de aprender y leer, lo que lo hace ideal para escribir documentos, blogs y comentarios. Markdown se utiliza comúnmente en GitHub, foros, y otras plataformas de desarrollo.

## Sintaxis Básica de Markdown

### Encabezados

Los encabezados se crean utilizando el símbolo `#`. El número de `#` indica el nivel del encabezado.

```markdown
# Encabezado 1
## Encabezado 2
### Encabezado 3
```

Esto se verá así:

# Encabezado 1
## Encabezado 2
### Encabezado 3

### Énfasis

Puedes aplicar **negrita** y *cursiva* al texto.

- **Negrita**: Usa doble asterisco `**` o doble guion bajo `__`.
- *Cursiva*: Usa un solo asterisco `*` o un solo guion bajo `_`.

```markdown
**Este texto es negrita**
*Este texto es cursiva*
```

### Listas

Markdown soporta listas ordenadas y no ordenadas.

- **Listas no ordenadas**: Usa asteriscos `*`, signos más `+`, o guiones `-`.
- **Listas ordenadas**: Usa números seguidos de un punto.

```markdown
- Elemento 1
- Elemento 2
  - Subelemento

1. Elemento 1
2. Elemento 2
```

### Enlaces

Para crear un enlace, usa corchetes `[Texto]` seguido de paréntesis `(URL)`.

```markdown
[Visita Docusaurus](https://docusaurus.io/)
```

Esto se verá como: [Visita Docusaurus](https://docusaurus.io/)

### Imágenes

Para insertar una imagen, usa el mismo formato que los enlaces, pero precedido por un signo de exclamación `!`.

```markdown
![Texto alternativo](ruta/de/la/imagen.jpg)
```

### Citas

Puedes citar texto usando el símbolo `>`.

```markdown
> Esta es una cita.
```

### Código

Para insertar fragmentos de código en línea, usa comillas invertidas `` ` ``. Para bloques de código, usa tres comillas invertidas ```` ``` ````.

```markdown
`código en línea`

```
bloque de código
```
```

### Tablas

Puedes crear tablas usando `|` para separar columnas y guiones `-` para definir la cabecera.

```markdown
| Columna 1 | Columna 2 |
|-----------|-----------|
| Dato 1    | Dato 2    |
| Dato 3    | Dato 4    |
```

Esto se verá así:

| Columna 1 | Columna 2 |
|-----------|-----------|
| Dato 1    | Dato 2    |
| Dato 3    | Dato 4    |

## Tarjetas


Docusaurus tiene una sintaxis especial para crear Tarjetas:

```md
:::tip My tip

Use this awesome feature option

:::

:::danger Take care

This action is dangerous

:::
```

:::tip My tip

Use this awesome feature option

:::

:::danger Take care

This action is dangerous

:::


Markdown es un lenguaje simple pero poderoso que te permitirá contribuir fácilmente a proyectos de documentación y contenido web.

