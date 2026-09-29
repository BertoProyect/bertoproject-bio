# bertoproject-bio

Landing de enlaces para la bio de BertoProject. Es HTML y CSS puro, sin compilación, publicado en Cloudflare Workers como archivos estáticos.

## Cómo se cambia

Cada push a `main` se publica solo en Cloudflare en aproximadamente un minuto.

| Quiero… | Archivo |
|---|---|
| Cambiar a dónde lleva `/ig`, `/tiktok`, `/yt`, `/orbita` o crear una ruta nueva | `public/_redirects` |
| Cambiar textos, orden de botones o añadir uno | `public/index.html` |
| Cambiar la foto | Reemplazar `public/avatar.webp` (cuadrada, 320×320) y `public/og.jpg` |

## Rutas cortas

| Ruta | Destino |
|---|---|
| `/tiktok`, `/tk` | tiktok.com/@berto.project |
| `/ig` | instagram.com/berto.project |
| `/yt` | youtube.com/@BertoProjectt |
| `/orbita` | orbitawebs.com |

Los botones apuntan a estas rutas, no directamente a las redes. Así, cuando se añada el conteo de clics, no habrá que tocar los enlaces.

## Diseño

Sigue el sistema de diseño de Apple (colección awesome-design-md): fondo parchment `#f5f5f7`, tarjetas blancas con radio de 18px y borde fino, texto a 17px y un único azul, `#00A3FF`. Solo existe en modo claro: el modo oscuro está bloqueado.

## Probar en local (opcional)

```
npx wrangler dev
```
