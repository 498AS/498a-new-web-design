# Blog · 498A

Estructura preparada, sin contenido todavía. Nada de esta carpeta está publicado
hasta que se cree `blog/index.html`.

## Convención de URL

```
/blog/                              índice (pendiente de crear)
/blog/slug-del-articulo.html        artículo
```

El slug va en minúsculas, sin acentos ni eñes, separado por guiones, y no cambia
nunca una vez publicado. Si hay que corregirlo, se añade una redirección 301 en
el `.htaccess` de la raíz.

## Publicar un artículo

1. Copiar `_plantilla-post.html` y renombrarlo con el slug.
2. Rellenar los marcadores `{{...}}` del `<head>`: título, descripción, slug,
   fecha ISO, tiempo de lectura e imagen social.
3. Escribir el cuerpo dentro de `<article class="post__body">`.
4. Generar la imagen social a 1200×630 en `/assets/og/slug.jpg`.
   Se puede reutilizar el método de `og-image.jpg`: HTML + Chrome headless.
5. Añadir la URL a `/sitemap.xml`.
6. Añadir un `<item>` a `/feed.xml` con título, enlace, descripción, `pubDate`
   en formato RFC-822 y `guid`.
7. Descomentar el bloque del blog en `/sitemap.xml` cuando exista el índice.

## Pendiente antes de lanzar el blog

- `blog/index.html` con el listado
- Enlace al blog en la navegación principal y en el footer de `index.html`
- Decidir si "Perspectivas" de la home pasa a ser el índice del blog o convive
  con él como sección de publicaciones externas

## Coherencia GEO

Cada artículo debe llevar JSON-LD de tipo `Article` con `author`, `datePublished`
e `isPartOf` apuntando al sitio, canonical propio y OG completo. Es la misma
regla que aplicamos a los clientes en las auditorías de GEO_DOCTOR.
