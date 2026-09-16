# Despliegue · 498advance.com

Web estática. No hay build, ni dependencias, ni backend. Se sube por FTP/SFTP y ya.

- **Origen**: Dinahosting (Apache · `hl1082.dinaserver.com`)
- **CDN**: Cloudflare por delante
- **Dominio canónico**: `498advance.com`
- **Repo**: https://github.com/498AS/498a-new-web-design

---

## 1 · Qué subir

Sube **el contenido de la carpeta `498Adesign/`**, no la carpeta.

En la raíz del hosting (`/public_html/` o equivalente) deben quedar así:

```
index.html          404.html          tokens.css
robots.txt          llms.txt          sitemap.xml
feed.xml            .htaccess
favicon.ico         apple-touch-icon.png    og-image.jpg
assets/             legal/
```

> Si subes la carpeta `498Adesign` entera, la web queda en
> `498advance.com/498Adesign/` y se rompe todo. Comprueba que `index.html`
> está en la raíz.

**El `.htaccess` empieza por punto**, así que muchos clientes FTP lo ocultan.
Activa "mostrar archivos ocultos" antes de subir y verifica que llegó.

## 2 · Qué NO subir

Estos archivos están en el repo para trabajar, no para publicarse:

```
playground.html      showcase.html      design-system.html
INVENTORY.md         README.md          legal/*.md         blog/
```

`playground.html` y `design-system.html` exponen el design system completo y el
mosaico con las fotos y nombres del equipo. `blog/` solo contiene la plantilla y
su documentación: no se sube hasta que haya artículos.

El `.htaccess` ya bloquea los `.md` por si alguno se cuela, pero es mejor no subirlos.

## 3 · Cloudflare · dos cambios obligatorios

**a) Invertir la redirección.** Hoy Cloudflare redirige `498advance.com → 498as.com`
con un 301. El `.htaccess` hace lo contrario. **Si no se quita esa regla antes de
subir, se produce un bucle de redirecciones y la web no carga.**

Panel de Cloudflare → dominio `498advance.com` → Rules → borrar o invertir la
regla de redirección.

**b) Activar el proxy en `498as.com`.** Hoy su registro A apunta directo a la IP de
Dinahosting con la nube gris: Cloudflare solo hace DNS, no cachea nada. Para que
actúe de CDN hay que ponerlo en naranja. Hazlo **después** de subir la web.

Los dos dominios deben apuntar al mismo origen. El `.htaccess` se encarga de
canonicalizar hacia `498advance.com`.

**c) Revisa el Bot Fight Mode.** Si está activo, puede bloquear a GPTBot,
ClaudeBot y PerplexityBot, que es justo lo contrario de lo que declara nuestro
`robots.txt`.

## 4 · Comprobaciones después de subir

```bash
curl -sI https://498advance.com/            # 200
curl -sI https://498as.com/                 # 301 hacia 498advance.com
curl -sI https://www.498advance.com/        # 301 hacia 498advance.com
curl -s  https://498advance.com/robots.txt  # debe listar el sitemap
curl -s  https://498advance.com/llms.txt | head -5
curl -sI https://498advance.com/sitemap.xml # 200, application/xml
curl -sI https://498advance.com/pagina-que-no-existe   # 404 servido por 404.html
curl -sI https://498advance.com/README.md   # 403, bloqueado por .htaccess
```

En el navegador:

- La home carga con el vídeo del hero y sin errores en consola
- Los cuatro enlaces legales del footer funcionan, y el "volver a la home" de cada
  página legal devuelve a la home (no al playground)
- Pegar `https://498advance.com` en LinkedIn o Slack muestra la imagen social
- Revisar en móvil real, no solo en el emulador

## 5 · Después de publicar

- Dar de alta el sitio en Google Search Console y Bing Webmaster Tools
- Enviar `https://498advance.com/sitemap.xml`
- Si `498as.com` estaba indexado, dejar el 301 permanente, nunca borrarlo
