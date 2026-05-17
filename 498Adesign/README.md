# 498Adesign · v2

Design system de la nueva web de 498A. Reemplaza a `498ASdesign/` (v1, legacy) post-rebrand 498AS → 498A.

**Fecha**: 2026-05-16
**Estado**: canonical
**Predecesor**: `../498ASdesign/` (queda como referencia histórica)
**Referencia conceptual**: la escala tipográfica y los degradados se inspiran en [isomorphiclabs.com](https://www.isomorphiclabs.com/), traducidos a la paleta y las fuentes de 498A.

---

## Resumen del cambio v1 → v2

| Eje | v1 | v2 |
|-----|----|----|
| Paleta | verde fluor + negro + greys sueltos | **verde-gris-negro** con tier explícito de 10 greys + 2 verdes |
| Verde brand | `#37E813` (fluorescente, estridente) | **`#2DD60F`** (un punto menos saturado, sigue siendo eléctrico pero menos radioactivo) |
| Segundo verde | — | **`#0E7A1F`** (verde profundo, para gradientes y profundidad) |
| Tipografía | Bebas Neue gigante (80–100 px), Hepta Slab 26/33 | Misma familia pero **escala Isomorphic** (Display 70 / H1 36 / Body 16) — restraint editorial |
| Esquinas | angular, 0–6 px | **igual · esquinas cuadradas confirmadas · máximo 4 px** |
| Degradados | inexistente / negro plano | **6 degradados** estilo Isomorphic adaptados a la paleta 498A |
| Hipervínculos | sin estilo definido | underline sutil verde, hover en verde primario, variante externa con `↗` |
| Citas técnicas | sin sistema | **número clickable tipo paper académico** + lista de referencias con anclas verdes al pie |
| Naming | `--as-*` | `--498-*` |

---

## 1. Color · verde-gris-negro con dos tonos de verde

### Brand

| Token | Hex | Uso |
|-------|-----|-----|
| `--498-green` | `#2DD60F` | **Primary** · CTAs, highlights, links, eyebrows, números destacados. Un punto menos estridente que el viejo `#37E813`. |
| `--498-green-deep` | `#0E7A1F` | **Deep** · ancla de gradientes, hover backgrounds, capa de profundidad. Forest/moss complementario. |
| `--498-green-hover` | `#26B30D` | Hover de botones primarios (slight darker) |
| `--498-green-soft` | `rgba(45,214,15,.12)` | Glow, fondos suaves, hover de ghost buttons |
| `--498-green-line` | `rgba(45,214,15,.35)` | Underlines de links, borders de citas |

### Grey scale (10 niveles)

`--498-grey-50` `#F7F7F7` paper · `--498-grey-100` `#ECECEC` background · `--498-grey-200` `#D9D9D9` text on dark · `--498-grey-300` `#BFBFBF` · `--498-grey-400` `#999999` text soft · `--498-grey-500` `#7A7A7A` text muted · `--498-grey-600` `#5C5C5C` · `--498-grey-700` `#404040` surface 2 · `--498-grey-800` `#2D2D2D` surface 1 · `--498-grey-900` `#1A1A1A` deep surface.

### Anclas

`--498-black` `#000000` · `--498-white` `#FFFFFF` · `--498-alert` `#E84B3C` (también un punto menos estridente que antes).

### Regla de uso del verde

El verde primario **nunca cubre superficies grandes**. Aparece como:
- Subrayado de verbos clave en displays
- Color de números (counters, citas, tags)
- Underline de links
- Background de CTAs (combinado con degradado a verde profundo)
- Borders de elementos interactivos

El verde profundo aparece como:
- Ancla de gradientes (radiales bottom-left, degradados de CTA)
- Hover oscuro sobre elementos verdes
- Cuando el verde primario competiría con otro elemento, el deep le cede el papel.

---

## 2. Tipografía · escala Isomorphic, fuentes 498A

Bebas Neue para displays UPPER. Hepta Slab para headlines y body. Roboto Mono para tags/citas. Roboto para UI. Dela Gothic One reservado para acentos chunky puntuales.

### Escala desktop (idéntica a Isomorphic, traducida a fuentes 498A)

| Token | Tamaño | Line-height | Tracking | Familia | Peso |
|-------|--------|-------------|----------|---------|------|
| Display 1 | 70 px | 77 | -2 px | Bebas Neue | 600 UPPER |
| Display 2 | 56 px | 61.6 | -1.7 px | Bebas Neue | 600 UPPER |
| Display 3 | 48 px | 57.6 | -1 px | Bebas Neue | 600 UPPER |
| Headline 1 | 36 px | 43.2 | -.7 px | Hepta Slab | 300 |
| Headline 2 | 28 px | 36.4 | -.3 px | Hepta Slab | 300 |
| Headline 3 | 24 px | 31.2 | -.2 px | Hepta Slab | 300 |
| Quote L (italic) | 48 px | 57.6 | -1 px | Hepta Slab italic | 300 |
| Paragraph XL | 24 px | 32.4 | 0 | Hepta Slab | 300 |
| Paragraph L | 20 px | 28 | 0 | Hepta Slab | 300 |
| Paragraph M | 16 px | 22.4 | 0 | Hepta Slab | 300 |
| Paragraph S | 14 px | 19.6 | 0 | Hepta Slab | 300 |
| Paragraph XS | 12 px | 16.8 | +.3 px | Hepta Slab | 400 |
| Tag L (UPPER) | 14 px | 19.6 | +1.1 px | Roboto Mono | 500 |
| Tag S (UPPER) | 12 px | 16.8 | +1 px | Roboto Mono | 500 |

### Cambio respecto a v1

- v1: Display gigante (100 px counters · 80 px mega · 55 px h1) — energía gritada
- v2: Display contenido (70 px display 1 · 48 px display 3) — energía contenida

La intención es la misma que en Isomorphic: la fuerza no viene de tamaño grande, viene del *whitespace generoso* alrededor del display.

### Responsive

Breakpoints a 1024 px (tablet) y 600 px (mobile). Display 1 baja a 48 px en tablet y 32 px en mobile, manteniendo proporciones.

---

## 3. Degradados · 6 anclas adaptadas de Isomorphic

| Token | Composición | Uso |
|-------|-------------|-----|
| `--498-gradient-hero` | radial verde 12% + radial verde profundo 25% + negro | Background del hero |
| `--498-gradient-section` | linear 180° negro → grey-900 | Background sutil de sección |
| `--498-gradient-section-light` | linear 180° grey-50 → grey-100 | Sección clara (rompe la monocromía) |
| `--498-gradient-cta` | linear 135° green → green-deep | Fondo de botones primarios |
| `--498-gradient-card-highlight` | radial verde 8% top-left | Highlight sutil en esquina superior izquierda de cards |
| `--498-gradient-soft-glow` | radial verde 15% bottom-center | Glow para elementos centrales (counters, citas) |

### Cómo se diferencia de Isomorphic

Isomorphic usa radiales pastel azul/morado/cyan en hero. 498A los reemplaza por radiales verde primario + verde profundo. Misma sintaxis, misma sutileza (alphas bajos, fade a transparent), distinta paleta. Esto preserva el look científico-sereno sin imitar.

---

## 4. Esquinas cuadradas · sin redondeos suaves

- `--498-radius-0` = 0
- `--498-radius-1` = 2 px
- `--498-radius-2` = 4 px **(máximo permitido)**

Confirmado explícitamente: no se usan los radios 12 / 16 / 20 px del sistema Isomorphic. 498A es angular. Cards, botones, badges y avatars mantienen el carácter brutalista-tecnológico de la marca.

---

## 5. Hipervínculos

```html
<a class="link" href="...">texto del link</a>
<a class="link link-ext" href="..." target="_blank">link externo</a>
```

- Color: verde primario
- Underline: 1 px verde a 35% opacidad
- Hover: underline a 100% opacidad
- Externo: añade `↗` automáticamente vía pseudo-elemento

---

## 6. Citas técnicas · sistema de referencias

Inspirado en papers académicos. Cada cita es un número clickable que ancla a una referencia al pie del artículo. Da peso técnico al texto y permite navegación rápida.

### Marca inline (cita en el texto)

```html
GEORadar audita el espacio semántico con 3.000 a 30.000 prompts<span class="cite"><a href="#ref-1">[1]</a></span>.
```

Renderiza como: superíndice `[1]` en Roboto Mono, con border cuadrado verde a 35% opacidad. Hover invierte: fondo verde, texto negro.

### Lista de referencias al pie

```html
<ol class="references">
  <li id="ref-1">Autor. <em>Título</em>. Publicación, año. <a href="...">URL</a></li>
  <li id="ref-2">...</li>
</ol>
```

Renderiza con `[1] [2] [3]` en mono verde como marcadores numerados, items en Hepta Slab 14 sobre grey-400. El `id="ref-N"` permite el ancla desde la cita. Border superior gris para separar la lista del cuerpo del artículo.

### Por qué importa este sistema

- Comunica **rigor técnico** sin necesidad de adjetivos.
- Permite citar fuentes externas (papers, repos, blogs) sin romper el flow del párrafo.
- Da **profundidad navegable**: el lector que quiere ir más allá tiene siempre un anchor a un click.
- Encaja con el frame *"frontera investigación↔aplicación"* que pide la home: si decimos *investigación*, mejor verlo en el HTML.

---

## 7. Reglas de estilo activas (style rules en memoria)

Tres reglas viven en `~/.claude/projects/-Users-cop-Documents-claudecode-proj-contentfactory/memory/` y aplican a cualquier copy producido para 498A:

1. **No usar guiones em ni en entre cláusulas** (`feedback_no_guiones.md`). Sustituir por punto, punto y coma o coma. El em-dash delata autoría LLM.
2. **Titulares en afirmativo, nunca negar** (`feedback_writing_no_negations.md`). H1 / H2 / Eyebrows afirman. La carga emocional de una afirmación llega antes al cerebro que la lógica que invierte una negación.
3. **Smart Brevity por defecto** (`feedback_writing_smart_brevity.md`). Lead con el punchline, frases cortas, verbos activos, números > adjetivos, bold en lo importante, sin copy aspiracional.

---

## 8. Migración desde v1 (498ASdesign)

| v1 token | v2 token |
|----------|----------|
| `--as-green` `#37E813` | `--498-green` `#2DD60F` |
| `--as-green-hover` `#00B147` | `--498-green-hover` `#26B30D` |
| `--as-text-on-dark` `#DBDBDB` | `--498-grey-200` `#D9D9D9` |
| `--as-text-muted` `#CCCCCC` | `--498-grey-300` `#BFBFBF` |
| `--as-surface-1` `#303030` | `--498-grey-800` `#2D2D2D` |
| `--as-surface-2` `#343434` | `--498-grey-700` `#404040` |
| `--as-hairline-dark` `#343434` | `--498-line` (alias de grey-700) |
| `--as-h1-size` 55 px | `--498-display-1-size` 70 px / `--498-h1-size` 36 px |
| `--as-counter-size` 100 px | `--498-display-1-size` 70 px |
| Sin gradientes | 6 tokens `--498-gradient-*` |
| Sin estilo de link | `.link`, `.link-ext` |
| Sin sistema de citas | `.cite`, `.references` |

Para migrar un HTML construido con v1: cambiar el import a `498Adesign/tokens.css`, sustituir clases `as-*` por `t-*` (tipografía) y `--as-*` por `--498-*` (color). El layout no requiere cambios — esquinas, spacings y comportamiento responsive permanecen.

---

## 9. Ficheros del kit

| Fichero | Contenido |
|---------|-----------|
| `tokens.css` | Variables, media queries responsive, utility classes (`t-display-1`, `t-h1`, `t-p-l`, `t-tag-l`...), componentes (`btn`, `card`, `link`, `cite`, `references`, `hero-498`). |
| `showcase.html` | Demo navegable de todos los tokens en acción: paleta, gradientes, escala tipográfica completa, botones, cards, ejemplo editorial con hipervínculos y 4 citas reales. |
| `README.md` | Este documento. |

---

## 10. Próximos pasos sugeridos

1. **Maquetar la home v3** ([498A-homepage-REVIEW.md](../498A-homepage-REVIEW.md)) con estos tokens. La estructura editorial de Isomorphic showcase + tokens de 498Adesign + copy de v3 = home navegable lista para Webflow/WP.
2. **Producir el logo SVG outline final** combinando el wordmark 498A nuevo con la paleta v2.
3. **Renombrar carpeta `498ASdesign/` → `_legacy/`** cuando todos los consumidores migren a v2. Mientras tanto, conviven.
4. **Validar contraste WCAG** del verde nuevo sobre fondos negro y blanco — el `#2DD60F` sobre negro pasa AA; sobre blanco está más justo, conviene usarlo solo como acento, no como texto largo.

---

*Generado: 2026-05-16. Inspiración escala tipográfica + degradados: isomorphiclabs.com. Fuentes: Bebas Neue, Hepta Slab, Roboto, Roboto Mono, Poppins, Dela Gothic One (todas Google Fonts).*
