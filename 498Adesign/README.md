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

---

## 11. v2.1 · Componentes e iteraciones del playground (2026-05-17)

Lo que sigue son los componentes y decisiones que emergieron del stress-test en `playground.html` y que ya forman parte del sistema canónico. El playground es la **fuente de verdad** visual; este documento es el índice navegable.

### 11.1 Nav · raíl flotante transparente

Estructura: dos clusters opacos sobre fondo transparente. El contenido scrollea por debajo.

```html
<nav class="nav">
  <a class="nav__brand-box" href="#">498 <em>A</em>DVANCE</a>
  <div class="nav__links">
    <a class="nav__link-box"><span class="num">01</span>Vision</a>
    ...
  </div>
  <div class="nav__spacer" aria-hidden="true"></div>
  <a class="nav__cta-box" href="#contact">Hablemos →</a>
</nav>
```

- **Brand-box**: caja negra contigua a los links · texto `498 ADVANCE` en mono UPPER · la "A" de ADVANCE en verde primario.
- **Link boxes**: blancas, bordes 1 px compartidos (border-left:0 en consecutivos), hover verde-50 + verde-deep.
- **Spacer transparente**: flex:1 sin bordes, solo empuja el CTA a la derecha.
- **CTA box**: caja negra aislada · `width: var(--498-rail-width)` (148 px) · cierra el raíl derecho.

**Token nuevo**: `--498-rail-width: 148px` · compartido con el lang grid del hero.

### 11.2 Language selector · matriz 2×3

Sustituye al corner-tag del hero. Misma `--498-rail-width` que el CTA para alinear vertical en el raíl derecho.

```html
<nav class="lang-grid" aria-label="Idioma">
  <a class="lang-grid__cell" hreflang="ca">CAT</a>
  <a class="lang-grid__cell is-active" hreflang="es" aria-current="true">ES</a>
  <a class="lang-grid__cell" hreflang="en">EN</a>
  <a class="lang-grid__cell" hreflang="fr">FR</a>
  <a class="lang-grid__cell" hreflang="de">DE</a>
  <a class="lang-grid__cell lang-cjk" hreflang="zh" aria-label="中文">中</a>
</nav>
```

- Posicionado absoluto en hero, top: 96 px, right: var(--498-page-pad).
- Bordes 1 px compartidos (último de cada fila/columna sin border).
- `.is-active`: fondo verde-deep + texto blanco.
- `.lang-cjk`: regla especial para el glifo `中` (tamaño +3 px, sin uppercase ni tracking, para compensar óptica del CJK frente al mono latino).

Códigos elegidos: **CAT · ES · EN / FR · DE · 中** (ISO 639-1 estándar para latinos, carácter chino para señalar "otra cosa").

### 11.3 Patrón backpropagation · SVG + animaciones

`assets/patterns/grid-backprop.svg` (120×120 tile, fondo transparente):

- 36 puntos `#B0B0B0` en grid 6×6 imaginario.
- 5 números diagonales activos en verde primario (`0.34`, `-0.12`, `1.05`, `-0.45`, `0.92`).
- 4 números dormidos en gris medio (`0.78`, `-0.83`, `1.21`, `-0.66`).
- 5 cells de la diagonal con verde fill opacity escalado 7→13%.

**Dos aplicaciones en CSS** con distinta intensidad:

| Componente | Fondo | Animaciones | Cuándo usar |
|------------|-------|-------------|-------------|
| `.pattern-band` | `--498-surface-lab` (#0F1410) | `patternFlow 60s` + `gradientDrift 22s` + `shimmer 14s` | Pausa atmosférica entre secciones light · solo decoración, sin texto encima |
| `.box-pattern` | white | `patternFlow 90s` + `gradientDrift 28s` (multiply blend) | Cards con contenido legible dentro · animación mucho más sutil |

Ambos respetan `prefers-reduced-motion` y usan `> * { z-index: 1 }` para garantizar que el contenido queda por encima de las capas animadas.

**Label de banda**: `<span class="pattern-band__label">Grid · backpropagation · gradient flow</span>` · caja blanca con border negro y shadow 16 px que pincha contra el fondo dark.

### 11.3b Periodic grid · módulo arquitectónico tipo tabla periódica

Módulo añadido en v2.1 para inventarios estructurados (capacidades del lab, motores LLM cubiertos, verticales, KPIs). Inspirado en la tabla periódica de elementos: celdas contiguas con estructura interna fija que se repite, formando una **tabla legible como dataset** más que como colección de cards.

**Anatomía de cada celda**:

```
┌─────────────────┐
│ 01         Lab  │  ← número (mono · grey faint) + tag categoría (mono · verde-deep)
│                 │
│      GEO        │  ← símbolo grande (Bebas Neue 56 px · 2-3 letras)
│                 │
│ ────────────────│  ← divider horizontal 1 px black (eco 498as.com)
│ ■ Capability    │  ← cuadradito verde (10×10 px · verde primary) + texto
└─────────────────┘
```

**Reglas del sistema**:
- Cells **contiguas** con shared 1 px black borders (sin gap).
- Encuadre exterior 1 px black sólido → la matriz lee como "tabla cerrada".
- Cada celda con `display: grid` interno fijo: `auto 1fr 1px auto`.
- Aspect ratio 4:5 (cells casi cuadradas).
- Hover: fondo verde-50 + símbolo pasa a verde-deep.
- **Celdas vacías** (`.box--periodic-empty`) con diagonal sutil → placeholder de expansión.
- Responsive: 4 cols desktop → 3 cols tablet → 2 cols mobile (con re-cálculo de borders).

**Diferencias clave vs `.box-collection--frame-cross`**:

| | frame-cross | periodic |
|---|-------------|----------|
| Espaciado entre cards | Gap 20 px | Contiguas |
| Corner marks "+" | Custom SVG `::before` | Naturales (intersección de borders + divider) |
| Estructura interna | Libre (la que tenga la card) | Fija (meta + symbol + divider + desc) |
| Encuadre exterior | No | 1 px black sólido |
| Sensación | Cards independientes con craft marks | Tabla / chart / catálogo |

**Uso recomendado**:
- Mapa de capacidades del lab (Sectio 02b "Capabilities matrix" en playground)
- Inventario de motores IA cubiertos (ChatGPT · Gemini · Claude · Perplexity · Copilot · AIO)
- Verticales de industria que cubre 498A
- Stack técnico del producto (módulos GEORadar: GEOAtlas · S.A.M. · DOC · LEO · GEOdesk)
- KPIs del Core (SOV · BIS · Sentiment · Position · Attribute · Co-branding)

**Estructura HTML**:

```html
<div class="box-collection box-collection--4 box-collection--periodic">
  <article class="box">
    <div class="periodic__meta">
      <span class="periodic__num">01</span>
      <span class="periodic__tag">Lab</span>
    </div>
    <div class="periodic__symbol">GEO</div>
    <div class="periodic__divider" aria-hidden="true"></div>
    <p class="periodic__desc">GEO · Generative Engine Optimization</p>
  </article>
  <!-- más celdas... -->
  <article class="box box--periodic-empty" aria-hidden="true"></article>
</div>
```

**Convenciones de naming sugeridas para el símbolo**:
- Capacidades del lab: 3 letras UPPER (GEO, MAS, SIM, NLU)
- Productos: 3 letras (RAD, SAM, LEO, ATL)
- Tags de categoría: Lab · R+D · Prod · Service

### 11.3c Service cards · grid arquitectónico tipo 498as.com

Módulo añadido en v2.1 para secciones de servicios o capacidades donde la imagen tiene peso visual. Replica fielmente el patrón del legacy 498as.com con cards grandes contiguas.

**Anatomía de cada card**:

```
┌────────────────────────────┐
│                            │
│        IMAGE               │  ← full-width · aspect-ratio 16:10 · border-bottom 1px
│                            │
├────────────────────────────┤
│                            │
│  TITLE (mono UPPER · 11px) │  ← centrado · padding 24/32/12
│                            │
│  ■ Description text        │  ← cuadradito verde 11×11 + texto Hepta Slab 13
│  con múltiples líneas      │
│                            │
└────────────────────────────┘
```

**Reglas del sistema**:
- Cells contiguas (técnica gap+background) con 1 px black borders.
- Imagen full-width con `aspect-ratio: 16 / 10`.
- Divider horizontal 1 px black entre imagen y texto (es el `border-bottom` de la imagen).
- Título: mono UPPER 11 px, letter-spacing 2 px, centrado, padding 24 px arriba / 12 px abajo.
- Descripción: Hepta Slab 13 px, color black, con cuadradito verde 11×11 px como bullet a la izquierda (`flex` con `gap: 10px`).
- Hover: fondo verde-50.
- Las "+" en las esquinas salen gratis del cruce natural de gaps.

**Cuándo usar este módulo vs los otros**:

| Variante | Caso de uso |
|----------|-------------|
| `--periodic` | Inventarios de **celdas atómicas pequeñas** (símbolo + 2-3 líneas) · tabla periódica · catálogos densos |
| `--service-cards` | Servicios o capacidades **con imagen protagonista** · cards más grandes (2×2, 3×N) · landing-style |
| `--frame-cross` | Cards independientes con craft decorativo (marcas de registro tipo print) en las esquinas |

**Estructura HTML**:

```html
<div class="box-collection box-collection--2 box-collection--service-cards">
  <article class="box">
    <div class="service-card__image">
      <img src="..." alt="...">
    </div>
    <h3 class="service-card__title">GEO &amp; Visibilidad en IA</h3>
    <p class="service-card__desc">Descripción del servicio...</p>
  </article>
  <!-- más cards... -->
</div>
```

**Layouts soportados**:
- `box-collection--2` → 2 cols (recomendado para 2×2 con 4 cards)
- `box-collection--3` → 3 cols
- `box-collection--4` → 4 cols (cards estrechas, mejor con descripciones cortas)

Responsive: en `≤ 900 px` y `≤ 600 px` colapsa a layout single-column manteniendo proporciones.

**Showcase**: Sectio · 02b · Matrix del playground · 4 cards 2×2 mostrando GEO & Visibilidad / Simulación social Gerard / Sistemas multiagente / Datasets a medida.

### 11.4 Marcas geométricas para box collections

Sustituyen a los iconos PNG corporativos (que delataban registro "deck de consultora"). 1 px stroke verde-deep, 28×28 px, totalmente abstractas — vocabulary del sistema: cuadrados angulares, puntos, diagonales, frame-cross.

```html
<span class="box__mark" aria-hidden="true">
  <svg viewBox="0 0 28 28" fill="none" stroke="currentColor" stroke-width="1">
    <rect x="1.5" y="1.5" width="25" height="25"/>
    ...
  </svg>
</span>
```

Las 4 marcas canónicas de Pillars:
1. **Cuadrados concéntricos** · profundidad / escala
2. **3 diagonales paralelas** · gradient flow (eco del patrón backprop)
3. **Grid 3×3 puntos con nodo central conectado** · red / atribución
4. **Cuadrado con frame-cross inscrito** · marca del sistema

Hover: color → verde primario + rotate 45° en 400 ms.

### 11.5 Botones · esquinas a 0 + nueva variante sólida

**Decisión v2.1**: todos los botones a `border-radius: 0`. El radius-2 (4 px) leía suave contra el resto del sistema angular.

| Clase | Fondo | Texto | Cuándo |
|-------|-------|-------|--------|
| `.btn-on-video` | white sólido | black | Hero video |
| `.btn-ghost-on-video` | transparent | white | Hero video, secundario |
| `.btn-light` | black | white | Sección clara, primario |
| `.btn-ghost-light` | transparent | text | Sección clara, secundario |
| `.btn-solid-dark` | black | white | **Nueva**. Pincha sobre fondos con textura (pattern, video) cuando ghost no se lee |
| `.btn-split` | white + black caja flecha | text | Estilo Isomorphic, en gradient cards |

Hover universal: verde-deep + verde-deep border.

### 11.6 Tarjeta gradient reutilizable (`.vision-hero-card`)

Componente extraído del hero "Our Goal" y reutilizado como "Cómo trabajamos / Manifiesto" antes del contacto.

```html
<article class="vision-hero-card">
  <div class="vision-hero-card__content">
    <span class="eyebrow-square">Cómo trabajamos</span>
    <h2 class="vision-hero-card__claim">Cada proyecto<br>como un <em>experimento</em>.</h2>
    <p class="ed-body">Texto explicativo breve · Smart Brevity.</p>
    <a class="btn-split" href="#">
      <span class="btn-split__label">Ver metodología</span>
      <span class="btn-split__arrow">→</span>
    </a>
  </div>
  <div class="vision-hero-card__visual">
    <img src="..." alt="...">
  </div>
</article>
```

Uso pensado:
- **Opener** de una sección (lo que la inspiró: "Our Goal" en Vision).
- **Closer** de la home, antes del contacto (bookend conceptual).
- **Cualquier punto de la página donde haya que explicar algo con peso**.

Grid 2 columnas, gradient 135° verde-200 → verde-100 → verde-50 → white, padding 56 px, esquinas a 0.

### 11.7 Cursor blink utilities

Dos variantes, distintos casos de uso.

**A · `.has-cursor`** · cursor estático parpadeante al final de un elemento.

```html
<h2 class="has-cursor">Texto importante</h2>
```

Cuadradito verde primario, ratio 900 ms on / 900 ms off (`steps(1)`). Para títulos secundarios de alta jerarquía cuando se quiere "live thinking" sin reveal.

**B · `.typewriter`** · reveal char-by-char con cursor avanzando · el cursor desaparece al terminar.

```html
<span class="typewriter" style="--chars: 13;">Founder Voice</span>
```

Solo se dispara cuando el elemento entra en viewport (JS IntersectionObserver, threshold 0.6). Cadena de 3 animaciones:
1. `typewriterReveal` · `width: 0 → calc(--chars × --char-w)` con `steps(--chars, end)` · reveal discreto, no interpolado.
2. `typewriterCursorShow` · enciende el cursor instantáneamente al empezar.
3. `typewriterCursorHide` · desactiva el cursor 150 ms después de terminar el reveal · transición seca, sin parpadeo.

**Cursor**: línea vertical fina (`border-right: 2px solid currentColor`) que hereda el color del texto (no verde brand). Una vez el texto está completo, el cursor desaparece y queda solo el título estático.

**Regla de escasez**: máximo 2-3 typewriters en toda la home. Reservados para eyebrows de nivel "Founder Voice" — nunca en body, nunca en h1 normales. Si todo parpadea, nada parpadea.

Variables custom para parametrizar:
- `--chars`: número de caracteres (incluye espacios)
- `--char-w`: ancho aprox por char (default `0.78em` · funciona para mono UPPER 11 px + tracking 1.8 px; sobrescribir si la fuente cambia)

Ambas utilidades respetan `prefers-reduced-motion`.

### 11.8 Eyebrow-square (cuadradito + texto mono)

Eyebrow con cuadradito negro `::before` (8×8 px) seguido de texto mono UPPER.

```html
<span class="eyebrow-square">Our Goal</span>
```

Variante con typewriter:

```html
<span class="eyebrow-square">
  <span class="typewriter" style="--chars: 11;">Founder Voice</span>
</span>
```

El cuadradito queda quieto a la izquierda, el texto se escribe al lado.

### 11.9 Citas ChatGPT inline · 3 variantes

Cuadradito 16×16 con número blanco clickable. Reemplaza al sistema `[1]` académico cuando se quiere estética "respuesta de LLM" en vez de "paper".

```html
texto<a class="cite-chat" href="#ref-1">1</a>.
texto<a class="cite-chat cite-chat--grey" href="#ref-2">2</a>.
texto<a class="cite-chat cite-chat--green" href="#ref-3">3</a>.
```

- **Default** (negro): cita principal, máxima atención.
- **Grey**: cita secundaria, menos peso visual.
- **Green**: cita conectada con el thread principal de argumentación (acento brand).

### 11.10 Frame-cross corner marks

Marcas de registro tipo print/editorial. Las hairlines del borde se extienden ligeramente más allá de las esquinas, creando un "+" sutil en cada vértice. Heritage de impresión técnica.

```html
<div class="frame-cross">contenido</div>
```

Aplicable a cualquier contenedor que necesite signal de "elemento de sistema". Usar con moderación — el efecto pierde fuerza si está en todos los bordes.

### 11.11 Filosofía de imagen actualizada (post-feedback simulación)

**El brief visual no es "AI consultancy" sino "lab de simulación"**. 498A simula agentes, personas, sociedades, entornos. La imaginería de mundos sintéticos generados es on-thesis, no biotech imitation.

Filtro para cualquier imagen nueva:

> **¿Esta imagen lee como un mundo, sistema o agente generado, con reglas visibles?**

Si sí → suma. Si solo es 3D decorativo bonito → resta.

**Registros que funcionan**:
- Mundos isométricos sintéticos (ciudades, ecosistemas, infraestructuras)
- Multi-agent crowds (cientos de figuras pequeñas con rutas)
- Paisajes procedurales con parámetros visibles (curvas, contornos, heatmaps)
- Geometría cellular / Voronoi / autómata
- Cartografía especulativa
- Cristales / biomorfos SI van con cifras flotantes que digan "esto es output de simulación"

**Drift a evitar**:
- Renders puros de moléculas/proteínas aisladas → biotech
- Stock 3D "AI brain" / "neural network globe" → categoría equivocada
- Microscopía / scanner médico → biotech

### 11.12 Tokens nuevos en `tokens.css`

```css
--498-rail-width:    148px;   /* CTA nav + lang grid · raíl derecho compartido */
--498-surface-lab:   #0F1410; /* pattern band oscura · lab notebook */
```

### 11.13 Próximos pasos del sistema

1. **Validar el sistema en mobile** — el playground se diseñó desktop-first, hay que probar la densidad en 600 px.
2. **Extraer componentes a archivos separados** si se decide maquetar en Webflow/WP con componentes reutilizables (`nav.html`, `pattern-band.html`, `gradient-card.html`, etc.). Mientras la home siga viviendo en `playground.html`, no hace falta.
3. **Decisión sobre cursor en Vision claim** — el "Our Goal" podría llevar typewriter también. Pendiente de validar si rompe la escasez o la refuerza.
4. **Imagen IA real** de cubos isométricos para reemplazar `crystal-cluster.svg` (placeholder).
5. **Sustituir Lorem Ipsum** por copy real de `498A-homepage-REVIEW.md` al maquetar.

---

*Actualizado v2.1: 2026-05-17. Iteraciones del playground integradas al sistema canónico.*
