# isomorphicdesign

Design system extraído de [isomorphiclabs.com](https://www.isomorphiclabs.com/) — la web de Isomorphic Labs (spin-off de DeepMind dedicada a *AI-first drug design*). El sistema tiene una identidad **científica, sobria y silenciosa**: monocromo apoyado en una paleta de acentos espectral, una tipografía suiza ligera (Söhne) y composiciones de generosísimo aire blanco.

Tokens reconstruidos a partir del CSS de producción del 2026-05-15 (`iso-ax3b7-q2f8-z4l5-kc0r.webflow.shared.a961a4f59.css`, 212 KB).

---

## 1. Principios

| Principio | Traducción visual |
|-----------|-------------------|
| **Rigor científico** | Tipografía mono para metadatos, tracking quirúrgico en displays (-2 px). |
| **Silencio editorial** | 90 % blanco/negro/gris; el color solo aparece como etiqueta o ilustración. |
| **Profundidad ligera** | Pesos 200–300 en displays grandes, nunca bold. |
| **Datos como narrativa** | Tag mono `UPPERCASE` para categorizar (`RESEARCH`, `INTERVIEW`, `PODCAST`). |
| **Mesura editorial** | Indents narrativos (caption 300 px, párrafo 108 px en desktop). |

---

## 2. Tipografía

### 2.1 Familias

| Token | Familia | Peso | Uso |
|-------|---------|------|-----|
| `--family-200-200-300` | **Söhne Extraleicht** → **Söhne Leicht** (desktop) | 200 / 300 | Displays |
| `--family-300` | **Söhne Leicht** | 300 | Headlines, párrafos |
| `--family-400` | **Söhne Buch** | 400 | Paragraph XS / labels |
| `--family-mono-400` | **Söhne Mono** | 400 | Tags, metadatos, código |

Fallback global: `Arial, sans-serif`.
Söhne y Söhne Mono son tipografías comerciales de Klim Type Foundry — sustituye por **Inter** (light/regular) y **JetBrains Mono** si no tienes licencia.

### 2.2 Escala (mobile / tablet / desktop)

| Token | Mobile | Tablet | Desktop | Line-height (desktop) | Tracking (desktop) | Peso |
|-------|--------|--------|---------|------------------------|---------------------|------|
| **Display 1** | 28 | 48 | **70** | 77 | -2 px | 300 |
| **Display 2** | 28 | 42 | **56** | 61.6 | -1.7 px | 300 |
| **Display 3** | 28 | 36 | **48** | 57.6 | -1 px | 300 |
| **Headline 1** | 26 | 28 | **36** | 43.2 | -.7 px | 300 |
| **Headline 2** | 24 | 26 | **28** | 36.4 | -.3 px | 300 |
| **Headline 3** | 22 | 22 | **24** | 31.2 | -.2 px | 300 |
| **Quote L** | 22 | 28 | **48** | 57.6 | -1 px | 300 italic |
| **Paragraph XL** | 16 | 22 | **24** | 32.4 | 0 | 300 |
| **Paragraph L** | 16 | 18 | **20** | 28 | 0 | 300 |
| **Paragraph M** | 14 | 14 | **16** | 22.4 | 0 | 300 |
| **Paragraph Longform** | 16 | — | **20** | 28 | +.2 px | 300 |
| **Paragraph S** | 12 | 12 | **14** | 19.6 | 0 | 300 |
| **Paragraph XS** | 10 | 10 | **12** | 16.8 | +.3 px | 400 |
| **Tag L** | 12 | 12 | **14** | 19.6 | +1.1 px | 400 mono UPPER |
| **Tag S** | 10 | 10 | **12** | 16.8 | +1 px | 400 mono UPPER |

Regla: en pantallas grandes, los **displays** usan tracking negativo agresivo (-1 a -2 px) y line-height ≈ 1.1; el **párrafo longform** abre el tracking a +.2 px para respirar.

---

## 3. Color

### 3.1 Núcleo monocromo (UI)

| Rol | Hex | Notas |
|-----|-----|-------|
| Black | `#000000` | Fondos hero, footer |
| Ink (text primary) | `#1e1e1e` | Texto principal sobre claro |
| Charcoal | `#3a3a3a` | Sub-texto |
| Graphite | `#585858` · `#626262` | Captions, líneas |
| Steel | `#758696` | **Color funcional más usado del sistema** — bordes, iconografía, tag de categoría neutra |
| Steel-light | `#aaadb0` · `#c3c3c3` · `#c8c8c8` | Estados disabled |
| Hairline | `#d8d8d8` · `#e2e2e2` · `#e8e8e8` | Separadores |
| Paper | `#fafafa` · `#f7f7f7` · `#f5f8f9` | Fondos suaves |
| White | `#ffffff` | Lienzo principal |
| Label scrim | `#62626280` (40 % alpha) | Fondo de etiquetas sobre imagen |

### 3.2 Paleta editorial (etiquetas + ilustración)

Cada acento viene **en pareja** (`tint suave` + `acento profundo`) y se asigna por tema/categoría de contenido. Nunca aparecen más de 2-3 acentos en una misma vista.

| Familia | Tint claro | Acento | Profundo |
|---------|------------|--------|----------|
| Azul ciencia | `#e6f7ff` / `#ccecfe` / `#9cdcff` | `#2895f7` · `#0082f3` · `#1378d1` | `#2d62ff` · `#1e00ff` |
| Acero brand | `#cddbe3` | `#67aacf` · `#6e848f` · `#5d6c7b` | `#304a57` · `#367496` |
| Lila/molecular | `#f8ebff` · `#ffecfc` | `#d38df4` · `#8744a7` · `#cc508b` | `#652085` · `#a12661` · `#130535` |
| Verde clínico | `#e9ffe9` · `#cbfedc` · `#94f1cf` | `#57be98` | `#258360` |
| Lima/datos | `#e8fac3` · `#dff0ad` · `#e6fa5e` | `#b3c828` | `#768702` |
| Tierra/protein | `#ffe4cc` · `#ffdede` · `#ffbedd` | `#bf7027` · `#8e4605` | `#3b0b0b` |
| Alerta | — | `#ea384c` | — |

> **Uso**: el monocromo es la regla. Los acentos viven en **tags** (`PERSPECTIVES`, `INTERVIEW`…), en **ilustraciones moleculares** y en **un único elemento por sección** (un dot, un underline, un highlight). Nunca en superficies grandes.

---

## 4. Layout

| Token | Mobile | Tablet | Desktop |
|-------|--------|--------|---------|
| Breakpoint nominal | 360 | 768 | 1440 |
| Max screen-width | — | — | **1440 px** |
| Page side padding | 20 px | 24 px | **8 vw** |
| Hero height | 440 px | 500 px | **660 px** |
| Navigation height | 72 px | 72 px | 72 px |
| Navigation padding | 20 px | 20 px | 20 px |

### Indents narrativos (página de noticia/post)
Estos son **el truco editorial** del site: párrafos, captions e interviews se indentan distinto.

| Tipo | Mobile | Tablet | Desktop |
|------|--------|--------|---------|
| Paragraph indent | 0 | 100 px | 108 px |
| Interview indent | 48 | 100 | 108 |
| Caption indent | 48 | 108 | **300 px** |

---

## 5. Forma — radios

| Token | Mobile | Tablet | Desktop | Uso |
|-------|--------|--------|---------|-----|
| `--radius-1` | 2.8 px | 3.1 px | 3.3 px | Tags |
| `--radius-2` | 3.6 | 3.9 | 4.5 | Inputs |
| `--radius-3` | 4.2 | 4.8 | 5.6 | Botones |
| `--radius-4` | 5 | 5.9 | 7 | Chips grandes |
| `--radius-5` | 10 | 10 | 10 | — |
| `--radius-container` | **12 px** | **16 px** | **20 px** | Tarjetas, hero, imágenes |

Notar la escalada **fraccionaria** (2.8, 3.1, 3.3…): el radio crece con el viewport, no es un valor fijo. Esto produce esa sensación de cards "respirando" en desktop sin perder definición en mobile.

---

## 6. Iconografía & componentes

### 6.1 Tamaños de icono

| Token | Mobile | Tablet | Desktop |
|-------|--------|--------|---------|
| Functional XL | 14 | 20 | 24 |
| Functional L | 12 | 16 | 20 |
| Functional M | 12 | 16 | 16 |
| Functional S | 10 | 12 | 12 |
| **Expressive** (hero, sección) | 26 | 32 | **40** |

### 6.2 Card padding

28 px (mobile) → 36 px (tablet) → **50 px** (desktop). Combinado con `radius-container: 20 px` define el look de las cards de prensa/news.

### 6.3 Botón "Work with us" (CTA primario)

- Fondo: `#1e1e1e` (Ink) o transparente con borde 1 px Ink
- Texto: Söhne Buch 14 / 1.1, tracking 0
- Padding: ~14 px / 22 px
- Radius: `--radius-3` (≈ 5.6 px desktop)
- Hover: ligero shift de fondo a `#3a3a3a`

### 6.4 Tag de categoría

- Söhne Mono 12 px UPPERCASE, tracking +1 px
- Color texto = acento de familia (ver §3.2)
- Sin fondo, o fondo `#62626280` cuando va sobre imagen
- Precedido a veces de un punto `•` del mismo color

---

## 7. Mood / dirección de arte

- **Imagery**: macro de superficies científicas (cristales, mallas moleculares, retratos en luz natural). Tratamiento alto contraste, grano fino, paleta fría.
- **Movimiento**: transiciones suaves (200–300 ms ease-out), reveal por opacidad, parallax sutil en hero. Nada decorativo.
- **Voz**: declarativa y ambiciosa ("Solve all disease"). Frases cortas en Display 1, soporte largo en Paragraph Longform.
- **Densidad**: 1 idea grande por sección. Whitespace > densidad informativa.

---

## 8. Ficheros del kit

| Fichero | Contenido |
|---------|-----------|
| `README.md` | Este documento (spec). |
| `tokens.css` | Variables CSS listas para `:root` con la escala completa por breakpoint. |
| `showcase.html` | Visualización de la escala tipográfica, paleta y componentes. |

---

*Extraído de producción el 2026-05-15. Fuente: CSS público de isomorphiclabs.com. Söhne © Klim Type Foundry — no se redistribuye la tipografía.*
