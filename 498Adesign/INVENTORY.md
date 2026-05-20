# Inventario · 498Adesign system

> Inventario completo del design system 498A v2.1 a fecha **2026-05-20**.
> Fuente de verdad sobre qué hay, qué se usa, y qué queda disponible.

---

## 1 · Archivos core del sistema

| Archivo | Líneas | Tamaño | Propósito |
|---------|--------|--------|-----------|
| `tokens.css` | 412 | 16 KB | Variables CSS canónicas · paleta · tipografía · escala · radius · motion |
| `playground.html` | 3.523 | 136 KB | **Stress design page** · todos los componentes con Lorem Ipsum · fuente de verdad visual |
| `index.html` | 2.855 | 112 KB | **Home v4** · producción · copy real de `498A-homepage-REVIEW.md` |
| `showcase.html` | 377 | 24 KB | Showcase legacy v1 (pre-v2.1) · queda como referencia histórica |
| `README.md` | 603 | 27 KB | Documentación canónica del sistema (incluye §11 v2.1) |
| `INVENTORY.md` | este | — | Este inventario |

**Total core**: 5 archivos · ~315 KB

---

## 2 · Assets · resumen por carpeta

| Carpeta | Archivos | Tamaño | Usados en playground | Sin usar |
|---------|----------|--------|----------------------|----------|
| `logos/` | 6 | 56 KB | 1 | 5 |
| `patterns/` | 5 | 28 KB | 1 | 4 |
| `icons/` | 5 | 20 KB | 1 | 4 (PNG legacy) |
| `team/` | 14 | 1.6 MB | 14 | 0 ✓ todos usados |
| `visuals/` | 26 | 3.3 MB | 11 | 15 (disponibles para sub-páginas) |
| `video/` | 11 | 36 MB | 4 | 7 (5 enlazados en index.html, 2 reserva) |
| **TOTAL** | **67** | **41 MB** | **32** | **35** |

---

## 3 · Logos · `assets/logos/`

| Archivo | Tamaño | Usado en | Disponible para |
|---------|--------|----------|------------------|
| `498A_ADVANCED_black.svg` | 6 KB | playground · index | Producción · uso general fondo claro |
| `498A_ADVANCED_green.svg` | 6 KB | — | Variantes verde brand |
| `498A_ADVANCED_white.svg` | 6 KB | — | Fondos oscuros · video hero · footer dark |
| `georadar_isotype_black.svg` | 4 KB | — | Producto GEORadar · footer · sub-brand |
| `georadar_wordmark_white.svg` | 6 KB | — | GEORadar · footer dark · partner pages |
| `sello-NextGenEU.webp` | 28 KB | — | Footer institucional · financiación |

---

## 4 · Patrones · `assets/patterns/`

| Archivo | Uso | Estado |
|---------|-----|--------|
| `grid-backprop.svg` | Pattern band oscura entre secciones · animada con `patternFlow + gradientDrift + shimmer` | ✓ Activo en playground/index |
| `grid.svg` | Grid puro hairlines | Reserva |
| `hexagrams-iching.svg` | Hexagramas I Ching · concept original 498AS | Reserva · puede no encajar en v2.1 |
| `pixel-generative.svg` | Pixel art generativo | Reserva |
| `pixel-mosaic.svg` | Mosaico pixel | Reserva |

---

## 5 · Iconos · `assets/icons/`

| Archivo | Uso | Estado |
|---------|-----|--------|
| `icon-linkedin.png` | Footer social link | ✓ Activo |
| `icon-countries.png` | — | **Legacy 498AS** · candidato a borrar (sustituido por marcas geométricas SVG inline) |
| `icon-experience.png` | — | **Legacy 498AS** · candidato a borrar |
| `icon-projects.png` | — | **Legacy 498AS** · candidato a borrar |
| `plus-circle.png` | — | **Legacy 498AS** · candidato a borrar |

---

## 6 · Team · `assets/team/`

14 fotos del equipo Barcelona + grupo. **Todas en uso** en el módulo de team de playground/index (Nivel 1 grupo, Nivel 2 senior grid de 5, Nivel 3 talent pool de 7).

| Persona | Rol | Archivo |
|---------|-----|---------|
| Carlos Ortet (founder · color) | Founder · 498A | `carlos-ortet.webp` |
| Carles Ortet | Director / CEO Zoopa | `carles-ortet.png` |
| Daniel Ebo | Dirección de arte | `dani-ebo.jpeg` |
| Mer Canet | Producción | `mer-canet.jpeg` |
| Charly Fernández | Realizador | `charly-fernandez.jpeg` |
| Roger de Gràcia | Talent / presentador | `roger-de-gracia.jpg` |
| Irene Laprof | Talent jove / digital | `irene-laprof.png` |
| Carla Calvo | Talent pool | `carla-calvo.jpeg` |
| Mia Ortet | Talent pool | `mia-ortet.jpeg` |
| Esther Rodríguez | Talent pool | `esther-rodriguez.jpeg` |
| Matteo Remuzzi | Talent pool | `matteo-remuzzi.jpeg` |
| Roger Adam | Talent pool | `roger-adam.jpeg` |
| Juanjo Sánchez | Técnico / digitallab | `juanjo-sanchez.jpeg` |
| Equipo Barcelona (foto grupo) | — | `equipo-barcelona.webp` |

---

## 7 · Visuales · `assets/visuals/`

### En uso en playground (11)

| Archivo | Slot |
|---------|------|
| `vision-organism.jpg` | Vision hero card |
| `science-stacks.jpg` | Science · Layers |
| `science-network.jpg` | Science · Ecosystem |
| `sc-geo-visibility.jpg` | Sectio 02B card · GEO |
| `sc-multiagent-flow.jpg` | Sectio 02B card · Multiagent |
| `sc-simulation-cube.jpg` | Sectio 02B card · Simulation |
| `sc-datasets-layers.jpg` | Sectio 02B card · Datasets |
| `news-llm.jpg` | News card #3 |
| `manifesto-hands.jpg` | Manifesto gradient card |
| `blog-hero.jpg` | Blog post hero |
| `blog-figure.jpg` | Blog post inline figure |

### Disponibles sin usar en playground (15)

| Archivo | Concepto · candidato para… |
|---------|------------------------------|
| `biomorph-shell.webp` | Forma biomorfa · sistemas multiagente |
| `crystal-cluster.svg` | Cubos isométricos placeholder · vision |
| `data-network.webp` | Red de datos clásica |
| `data-network-alt.webp` | Red de datos · variante |
| `green-architecture.webp` | Arquitectura modular verde · usado en index.html Tesis v3 |
| `isometric-cubes.svg` | Cubos isométricos · multi-agent |
| `library-garden.jpg` | Jardín experimental · library cards |
| `library-grid.jpg` | Coral con grid verde · datos curados |
| `method-panels.jpg` | Paneles verticales con luz · IA privada |
| `news-growth.jpg` | Cristal flotante + vegetación · growth news |
| `news-rd.jpg` | Cerebro orgánico con musgo · I+D news |
| `stacked-layers.webp` | Capas translúcidas · architecture |
| `tesis-frontier.svg` | Diagrama estructural · descartado por usuario |
| `visual-ecosystem.webp` | Ecosistema visual · concept |
| `visual-layers.webp` | Capas |

---

## 8 · Vídeos · `assets/video/`

| Archivo | Resolución | Tamaño | Usado en playground | Usado en index.html |
|---------|------------|--------|---------------------|---------------------|
| `hero-loop.mp4` | 1920×1080 | 3.4 MB | ✓ Hero video | ✓ Hero rotation pool |
| `hero-loop-mobile.mp4` | 720×1280 | 1.9 MB | ✓ Hero mobile | ✓ Hero mobile |
| `loop-productos.mp4` | — | 1.9 MB | ✓ News card 1 | — |
| `loop-servicios.mp4` | — | 3.1 MB | ✓ News card 2 | — |
| `section-home.mp4` | 1920×1080 | 4.1 MB | — | ✓ Hero rotation pool |
| `section-services.mp4` | 1920×1080 | 2.5 MB | — | ✓ Hero rotation pool |
| `section-vision-01.mp4` | 1920×1080 | 3.3 MB | — | ✓ Hero rotation pool |
| `section-vision-02.mp4` | 1920×1080 | 4.8 MB | — | ✓ Hero rotation pool |
| `section-news.mp4` | 1080×1920 | 4.5 MB | — | — (vertical · reserva) |
| `section-products.mp4` | — | 1.9 MB | — | — (reserva) |
| `section-product-dev.mp4` | — | 3.1 MB | — | — (reserva) |

**Optimización aplicada**: re-encode H.264 CRF 26, sin audio, faststart. 108 MB → 36 MB (-67 %).

---

## 9 · Legal · `legal/`

4 documentos completos en CA + ES + EN (algunos idiomas como borrador pendiente validación legal).

| Documento | Markdown | HTML | Idiomas |
|-----------|----------|------|---------|
| Aviso legal | ✓ `aviso-legal.md` | ✓ `aviso-legal.html` | CA + EN + ES (borrador) |
| Política de privacidad | ✓ `politica-privacidad.md` | ✓ `politica-privacidad.html` | ES + CA + EN (borrador) |
| Política de cookies | ✓ `politica-cookies.md` | ✓ `politica-cookies.html` | ES + CA + EN (borrador) |
| Declaración de accesibilidad | ✓ `declaracion-accesibilidad.md` | ✓ `declaracion-accesibilidad.html` | ES + CA + EN (borrador) |
| Índice | — | — | `legal/README.md` |

---

## 10 · Cobertura de uso por superficie

```
                Playground (stress)    Index (home v4)
Logos                  17 %                 33 % (estimado)
Patterns               20 %                 20 %
Icons                  20 % (1 de 5)        20 %
Team                  100 % ✓              ~90 %
Visuals                42 %                 ~55 %
Videos                 36 %                 73 % (8 de 11)

TOTAL aprox cobertura  ~50 %                ~60 %
```

El **stress page** demuestra los componentes con un subset de assets.
La **home v4** activa más assets reales pero todavía no usa el 100 %.

---

## 11 · Acciones pendientes recomendadas

1. **Limpiar PNG legacy** · borrar 4 iconos PNG sin usar (`icon-countries.png`, `icon-experience.png`, `icon-projects.png`, `plus-circle.png`) · liberan 17 KB y eliminan confusión.
2. **Decidir patrones reserva** · si `grid.svg`, `hexagrams-iching.svg`, `pixel-generative.svg`, `pixel-mosaic.svg` no entran en el plan editorial, borrarlos.
3. **Auditar visuales sin usar** · 15 archivos disponibles. Algunos son backups (`data-network.webp` + `data-network-alt.webp` redundantes). Decidir qué se reserva para sub-páginas (productos, blog, casos) y qué se descarta.
4. **Documentar en README §11** qué visuales están reservados para qué tipo de sección · evita confusión futura al maquetar nuevas páginas.
5. **Crear sub-páginas de producto** (GEORadar · S.A.M. · Stardesk · ROBIN) reutilizando los visuales libres + patrones reserva.
6. **Borrar `showcase.html` legacy** o moverlo a `_legacy/` cuando todos los consumidores migren a `playground.html` como source of truth.

---

## 12 · Git y deploy

- **Repo**: [github.com/carlosortet/498a-new-web-design](https://github.com/carlosortet/498a-new-web-design) (privado)
- **Última actualización**: 2026-05-20
- **Estado git**: clean · pushed
- **Dominio target**: `www.498a.com` (pendiente confirmación post-rebrand)

---

*Inventario generado: 2026-05-20 · 498A · v2.1 · Diseño desarrollado con [Claude Code](https://claude.com/claude-code).*
