# Instrucciones del proyecto


## Qué es este repositorio

Este es el sitio estático **luisfuentes.me**, publicado en GitHub Pages. El repo contiene el **output generado** por Hexo (generador de sitios estáticos), no el source de Hexo. No hay proceso de build local: los archivos HTML ya están compilados.

## Estructura

Cada post es un directorio con su propio `index.html`:
```
/hola-mundo/index.html
/guia-npm/index.html
...
```

El CSS en producción es `css/apollo.css`. El source SCSS está en `scss/apollo.scss` como referencia, pero **no hay pipeline de compilación en este repo** — si se modifica el SCSS, hay que compilarlo manualmente y reemplazar `css/apollo.css`.

## Publicar cambios

El sitio se actualiza haciendo push a `master`:

```bash
git add .
git commit -m "Site updated"
git push origin master
```

GitHub Pages sirve directamente desde la rama `master`.

## Agregar un post

1. Crear directorio con el slug del post: `/nombre-del-post/`
2. Crear `index.html` dentro siguiendo la estructura de posts existentes (ver `hola-mundo/index.html`)
3. Actualizar `index.html` raíz para incluir el post en el listado
4. Actualizar `archives/index.html` y `atom.xml` con el nuevo post
5. Agregar imágenes relevantes en `/images/`

## Convenciones HTML

- Todos los `index.html` son archivos minificados de una sola línea
- El tema es Apollo con la fuente `Source Sans Pro` de Google Fonts
- Comentarios Disqus con `disqus_shortname = 'luisfuentes'`
- Google Analytics con `UA-64770465-1`
- Idioma: español (`lang="es"`)
