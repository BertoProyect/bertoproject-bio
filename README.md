# bertoproject-bio

Landing de enlaces para la bio de BertoProject. Es HTML y CSS puro, sin compilación, publicado en Cloudflare Workers como archivos estáticos.

## Cómo se cambia

Cada push a `main` se publica solo en Cloudflare en aproximadamente un minuto.

| Quiero… | Archivo |
|---|---|
| Cambiar a dónde lleva `/ig`, `/tiktok`, `/yt`, `/orbita` o crear una ruta nueva | `public/_redirects` |
| Cambiar textos, orden de botones o añadir uno | `public/index.html` |
| Cambiar la foto | Reemplazar `public/avatar.webp` (cuadrada, 320×320) y `public/og.jpg` |
| Cambiar el icono (pestaña, Google, iPhone, Android) | `favicon.ico`, `icon-*.png`, `apple-touch-icon.png` en `public/` |
| Añadir una página nueva para que Google la indexe | `public/sitemap.xml` (una `<url>` por página) |
| Abrir una red social nueva y vincularla en Google | `sameAs` en el bloque `application/ld+json` de `public/index.html` |

## Google

- `public/robots.txt` permite rastrear todo y apunta al sitemap.
- `public/sitemap.xml` lista las páginas que se deben indexar (ahora solo la portada).
- `index.html` lleva canonical a `https://bertoproject.com/` y datos estructurados (WebSite, ProfilePage y Person con `sameAs` a TikTok, Instagram y YouTube).
- La propiedad se gestiona en Google Search Console (propiedad de tipo dominio, verificada por DNS en Cloudflare).

## Rutas cortas

| Ruta | Destino |
|---|---|
| `/tiktok`, `/tk` | tiktok.com/@berto.project |
| `/ig` | instagram.com/berto.project |
| `/yt` | youtube.com/@bertoprojectt |
| `/orbita` | orbitawebs.com |

Los botones apuntan a estas rutas, no directamente a las redes. Así, cuando se añada el conteo de clics, no habrá que tocar los enlaces.

## Diseño

Sigue el sistema de diseño de Apple (colección awesome-design-md): fondo parchment `#f5f5f7`, tarjetas blancas con radio de 18px y borde fino, texto a 17px y un único azul, `#00A3FF`. Solo existe en modo claro: el modo oscuro está bloqueado.

## Probar en local (opcional)

```
npx wrangler dev
```
