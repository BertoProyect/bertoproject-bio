# bertoproject-bio

Landing de enlaces para la bio de BertoProject. Es HTML y CSS puro, sin compilación, publicado en Cloudflare Workers como archivos estáticos.

## Cómo se cambia

Cada push a `main` se publica solo en Cloudflare en aproximadamente un minuto.

| Quiero… | Archivo |
|---|---|
| Cambiar a dónde lleva `/ig`, `/tiktok`, `/yt`, `/orbita` o crear una ruta nueva | `public/_redirects` |
| Cambiar textos, orden de botones o añadir uno | `public/index.html` |
| Destacar otro botón en azul | Mover la clase `featured` a otro `<a class="link">` (solo uno) |
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

Se basa en el sistema de diseño de Linear (colección awesome-design-md): fondo `#010102`, superficies con borde fino y un único acento, el azul BertoProject `#00A3FF`. Ese azul se usa solo en el botón destacado.

## Probar en local (opcional)

```
npx wrangler dev
```
