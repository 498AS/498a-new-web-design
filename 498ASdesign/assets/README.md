# 498ASdesign — Assets descargados desde 498as.com

Acceso al servidor de producción vía la **REST API pública de WordPress** (`/wp-json/wp/v2/media`) — no se requirió autenticación.

**Fecha del sweep:** 2026-05-15
**Total assets descubiertos:** 327 entradas en la mediateca (174 URLs únicas tras deduplicación)
**Páginas API:** 4 (`per_page=100`)

---

## Hallazgo de seguridad menor

La mediateca expone URLs en **dos hostnames** simultáneos:

1. `https://498as.com/wp-content/uploads/…` — CDN/producción
2. `http://161.22.44.59/~a49579wx/wp-content/uploads/…` — **IP origen del servidor compartido (cPanel)**

El segundo hostname **revela la IP del hosting compartido y el username del cPanel** (`a49579wx`). Es información que normalmente se oculta detrás del CDN/proxy. No es crítico, pero conviene:

- Forzar todas las URLs canónicas a `https://498as.com/…` (regenerar con un *URL replace* en la BD de WordPress).
- Bloquear acceso directo por IP en el servidor (`Deny from all` salvo CDN).

> Marca esto en el backlog técnico — no afecta a este entregable, pero es la clase de cosa que tu propio sistema (GEORadar/DOC) flaggearía en una auditoría AX.

---

## Inventario descargado

### `/logos/` — Identidad de marca

| Archivo | Origen | Notas |
|---------|--------|-------|
| `498_LOGO_BLANCO.svg` | `/2025/498_LOGO_BLANCO.svg` (9.9 KB) | **Logo principal vectorial**, fill `#fff`, viewBox 841.89 × 595.28. Export Adobe Illustrator 28.6. Pensado para fondos oscuros. |
| `logo-498-footer.png` | `/logo-498-footer.png` (19 KB) | Versión PNG usada en footer. |
| `favi-498as.png` | `/favi-498as.png` (12 KB) | Favicon principal. |
| `favi.png` | `/favi.png` (12 KB) | Favicon alternativo (legacy). |
| `logo-digitalizadores-NextGenEU.webp` | `/logo-digitalizadores-mw.webp` (16 KB) | Sello "Financiado por la Unión Europea — Next Generation EU" (Kit Digital). |

> ⚠️ **No se encontró logo en versión negra** ni isotipo aislado en la mediateca. Si existen, no están publicados. Habría que pedírselos a marca/diseño internos o vectorizar el footer PNG.

### `/team/` — Fotografía corporativa

| Archivo | Origen | Notas |
|---------|--------|-------|
| `carlos-ortet-fundador.webp` | `/carlos-ortet_fundador-498as.webp` (44 KB) | Retrato Carlos Ortet — *CEO & Cofundador*. |
| `carlos-ortet-ceo.webp` | `/equipo-498as_calos-ortet.webp` (50 KB) | Variante "CEO 498AS". |
| `equipo-personal.webp` | `/equipo-498as_personal.webp` (3.9 KB) | Personal de oficina (imagen pequeña). |
| `equipo-innovacion.webp` | `/innovacion-tecnologica_equipo.webp` (76 KB) | Foto de grupo del equipo. |
| `equipo-innovador-barcelona.webp` | `/equipo-innovador.webp` (484 KB) | **Foto principal** del equipo en Barcelona. |

### `/hero/` — Imágenes hero y OG

| Archivo | Origen | Notas |
|---------|--------|-------|
| `hero-498-innovacion.webp` | `/2025/498-innovacion.webp` (188 KB) | **Hero principal** del home actual (background del primer fold). |
| `og-consultoria-innovacion.webp` | `/2025/consultoria-innovacion-tecnologica.webp` (50 KB) | Open Graph image (551 × 328). |
| `2_Home_Online_Training-Hero.jpg` | `/2025/04/2_Home_Online_Training-Hero.jpg` (244 KB) | Hero alternativo, posible variante anterior. |
| `fast-startup.webp` | `/2025/fast-startup.webp` (9.4 KB) | Asset secundario. |

### `/video/` — Videos hero (heredados del IP origen)

| Archivo | Origen | Tamaño | Notas |
|---------|--------|--------|-------|
| `1_HOME.mp4` | `~a49579wx/1_HOME.mp4` | 15 MB | **Video hero del home** (posible loop de fondo). |
| `4_PRODUCTOS.mp4` | `~a49579wx/4_PRODUCTOS.mp4` | 1.9 MB | Hero sección productos. |
| `5_SERVICIOS-DESARROLLO-PRODUCTO.mp4` | `~a49579wx/5_SERVICIOS-…mp4` | 3.1 MB | Hero sección servicios. |

> Hay más videos en el servidor (`2_QUIENES-SOMOS_01.mp4` 20 MB, `3_SERVICIOS.mp4` 21 MB, `6_BLOG.mp4` 16 MB). No los descargué para no inflar la carpeta — están listados en `INVENTORY.csv`.

### `/icons/` — Iconografía y elementos UI

| Archivo | Origen | Notas |
|---------|--------|-------|
| `circulo-cruz.png` | `/circulo-cruz.png` (1.2 KB) | Icono "+ producto" / cross-in-circle. |
| `proyectos-tecnologicos.png` | `/proyectos-tecnologicos.png` (2.1 KB) | Icono "proyectos". |
| `paises-tecnologia.png` | `/paises-tecnologia.png` (4 KB) | Icono "países". |
| `experiencia-tecnologia.png` | `/experiencia-tecnoclogia.png` (2.7 KB) | Icono "experiencia" (sic — typo en URL original). |
| `linkedin.png` | `/linked.png` (3.4 KB) | Icono social LinkedIn. |

---

## Familias tipográficas en servidor

La mediateca tiene **18 ficheros TTF Poppins** subidos directamente como uploads (no como webfonts servidos por Google). Familia completa:

```
Poppins-Thin / ThinItalic / ExtraLight / ExtraLightItalic / Light / LightItalic /
Regular / Italic / Medium / MediumItalic / SemiBold / SemiBoldItalic /
Bold / BoldItalic / ExtraBold / ExtraBoldItalic / Black / BlackItalic
```

URLs base: `https://498as.com/wp-content/uploads/Poppins-{weight}.ttf`

> No bajé los TTF porque Poppins está en Google Fonts (ya importado en `tokens.css`). Si quieres self-host completo, son ~3 MB en total.

**No están en servidor**: Bebas Neue, Dela Gothic One, Hepta Slab, Roboto — esas se cargan desde Google Fonts.

---

## Contenido temático presente (no descargado)

El resto de los 174 assets son ilustraciones SEO-friendly del blog WordPress, con nombres descriptivos en castellano:

- `consultoria-innovacion-tecnologia_*` (~25 archivos): hero/banners de páginas servicio.
- `empresa-innovacion-tecnologica_*` (~30 archivos): hero/banners de páginas corporativas.
- `productos-tecnologicos_*` (~12 archivos): hero/banners de fichas de producto (GEORadar, S.A.M., Stardesk, etc.).
- `blog-innovacion-tecnologica_*` (~20 archivos): featured images del blog.
- `img-h-blog-*`, `img-intro-blog-*`, `img-bottom-blog-*` (~30 archivos): imágenes interiores de posts.

Todas en formato **WebP**, comprimidas para web.

---

## Cómo regenerar el inventario

```bash
for p in 1 2 3 4; do
  curl -sL "https://498as.com/wp-json/wp/v2/media?per_page=100&page=$p" \
    -o "/tmp/498-media-$p.json"
done
```

Inventario completo deduplicado en [`INVENTORY.csv`](INVENTORY.csv) (174 filas).

---

*Sweep ejecutado: 2026-05-15. Acceso público sin autenticación. Todos los assets son contenido propio de 498 Advance (Zoopa).*
