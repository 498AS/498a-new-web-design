# 498ASdesign

Design system extraído de [498as.com](https://498as.com/) — consultora de innovación tecnológica del grupo Zoopa (división 498 Advance, ex *498AS Innovation Lab*). El sistema es **brutalista-tecnológico**: negro absoluto + verde fluor #37E813, displays masivos en Bebas Neue, body en Hepta Slab (slab serif ligero), y un segundo display ultra-pesado en Dela Gothic One para acentos rotundos.

Tokens reconstruidos a partir del CSS de producción del 2026-05-15 (Elementor + tema Hello Elementor child).

---

## 1. Principios

| Principio | Traducción visual |
|-----------|-------------------|
| **Energía tecno-deportiva** | Negro absoluto + verde fluor #37E813 (radioactivo, alta saturación). |
| **Voz mayúscula** | Bebas Neue condensada en UPPERCASE para headlines. |
| **Contraste de pesos** | Display 600 condensado vs body 300 slab — choque deliberado. |
| **Densidad informativa** | Tipografías de ancho variado (condensada + chunky + slab + sans). |
| **Hero inmersivo** | 100 vh, fotografía documental con overlay negro 45 %, copy blanco. |

---

## 2. Tipografía

### 2.1 Familias (cuatro, con rol claro)

| Token | Familia | Peso | Rol |
|-------|---------|------|-----|
| `--type-primary` | **Bebas Neue** | 600 | Display condensado UPPERCASE — h1, counters, números grandes |
| `--type-secondary` | **Dela Gothic One** | 500 | Display ultra-pesado — acentos puntuales, labels rotundos |
| `--type-text` | **Hepta Slab** | 300 | Body slab serif — párrafos, lead, hero copy |
| `--type-accent` | **Roboto** | 500 | UI funcional — botones, nav, formularios |
| `--type-alt` | **Poppins** | 300 | Hero secundario, citas (uso editorial) |

> Las cinco son **Google Fonts gratis**. Cualquier replica del sistema se monta sin licencias.

### 2.2 Escala

| Token | Tamaño | Line-height | Peso | Familia |
|-------|--------|-------------|------|---------|
| Counter / mega | 80–100 px | 1.0 | 600 | Bebas Neue |
| Display 1 (h1) | **55 px** | 50 px | 600 | Bebas Neue |
| Display 2 (h2) | 38 px | 1.1 | 300 | Hepta Slab |
| Display chunky | 33 px | — | 500 | Dela Gothic One |
| Hero sub | 30 px | 37 px | 300 UPPER | Poppins |
| Lead | 28 px | 1.3 | 300 | Poppins |
| Body XL | **26 px** | **33 px** | 300 | Hepta Slab |
| Body L | 24 px | 1.4 | 300 | Hepta Slab |
| Body M | 22 px | 1.4 | 300 | Hepta Slab |
| Body S | 20 px | 1.5 | 300 | Hepta Slab |
| Caption | 18 px | 1.5 | 300 | Poppins |
| Meta | 14 px | 1.5 | 500 | Roboto |
| Micro | 11 px | 1.5 | 500 UPPER | Roboto |

Tamaños presentes en el CSS de producción: 11, 14, 16, 18, 19, 20, 22, 23, 24, 26, 28, 30, 34, 38, 55, 80, 100 px.

### 2.3 Reglas

- **Headlines siempre UPPERCASE** cuando van en Bebas Neue o Poppins display.
- **Body en Hepta Slab 300** — nunca regular ni bold. La voz ligera del slab serif equilibra el peso de Bebas Neue.
- **Text-shadow oscuro permitido** en hero sobre foto: `2px 2px 5px rgba(0,0,0,.75)`.

---

## 3. Color

### 3.1 Núcleo (alto contraste)

| Rol | Hex | Notas |
|-----|-----|-------|
| **Black** | `#000000` | Fondo dominante — usado 45× en CSS |
| **White** | `#FFFFFF` | Texto primario (`--e-global-color-primary`) |
| **Brand green** | `#37E813` | Verde radioactivo — el color de marca, 24× en CSS |
| **Brand green hover** | `#00B147` | Estado hover/active más oscuro |
| Text grey | `#DBDBDB` | Body sobre negro |
| Secondary grey | `#CCCCCC` | Subtexto / muted |
| Light hairline | `#E5E5E5` | Separadores claros |
| Mid grey | `#B9B9B9` | Overlay fondos (`#B9B9B9FC` con alpha) |
| Charcoal 1 | `#676767` | Caption grey |
| Charcoal 2 | `#474747` | UI surfaces |
| Charcoal 3 | `#343434` | Borders dark |
| Charcoal 4 | `#303030` | Card dark fondo |

### 3.2 Reglas de aplicación

- **Tema oscuro por defecto**: negro de fondo, blanco para títulos, gris claro `#DBDBDB` para body.
- **Verde #37E813**: reservado para CTAs primarios, hover de enlaces, números destacados (counters) y subrayados. **Nunca como fondo de superficies grandes** — quemaría.
- **Overlay hero**: imagen + capa negra a 45 % opacidad (`#000 / opacity .45`) — patrón canónico.
- **Sombra de texto** sobre foto: `2 2 5 rgba(0,0,0,.75)` cuando el copy va encima de una imagen sin overlay suficiente.

---

## 4. Layout & componentes

### 4.1 Layout

| Token | Valor |
|-------|-------|
| Max content width | 1100 px (cards) / 1640 px (full bleed) |
| Hero height | **100 vh desktop · 95 vh mobile** |
| Page side padding | 5 % izquierda · 4 % derecha (asimétrico) |
| Section vertical padding | ≥ 65 px |
| Grid breakpoint | 1024 px (tablet) · 767 px (mobile) |

### 4.2 Hero canónico

1. `min-height: 100vh`
2. Background photo `50% 50%`, `background-size: cover`
3. Overlay `#000` + `opacity: 0.45`
4. Copy alineado a derecha (`text-align: right`), márgenes superiores ≥ 100 px
5. Display copy: Hepta Slab 38 px 300 + Poppins 28–30 px 300 UPPERCASE
6. CTA: borde + verde brand en hover

### 4.3 Botones

| Estado | Estilo |
|--------|--------|
| Primary | Fondo `#37E813`, texto `#000`, Roboto 500, padding 14/22, radius 4 px |
| Primary hover | Fondo `#00B147`, texto `#fff` |
| Ghost (sobre oscuro) | Borde 1 px `#37E813`, texto `#37E813`, fondo transparente |
| Ghost hover | Fondo `#37E813`, texto `#000` |

### 4.4 Counters (sección de cifras)

- Número: Bebas Neue 80–100 px, color `#37E813`
- Label: Dela Gothic One 33 px, color `#fff`
- Centrado, separación generosa

### 4.5 Cards

- Fondo `#303030` o `#fff` (según contexto)
- Borde 1 px `#343434` o `#E5E5E5`
- Radio: 0–4 px (sistema **angular**, no redondea)
- Padding 30–40 px

### 4.6 Testimonios / carrusel

- Texto: Hepta Slab 26 px 300
- Nombre: Bebas Neue 55 px UPPER (autoría dramática)
- Cargo: Dela Gothic One 33 px

---

## 5. Mood / dirección de arte

- **Imagery**: fotografía documental (oficinas, equipo, tecnología), tratada con overlay negro. Tono frío, contraste alto.
- **Iconografía**: line icons FontAwesome (heredado del stack WordPress/Elementor). Acompañan body, nunca son protagonistas.
- **Voz**: directa, en español, mayúsculas constantes para slogans ("INNOVACIÓN", "CONSULTORÍA TECNOLÓGICA"). Tono asertivo, comercial-técnico.
- **Movimiento**: `fadeIn` clásico de Elementor, scroll-reveals suaves. Counter animado para cifras. Sticky header.
- **Densidad**: media-alta. El sitio prioriza informar sobre dejar respirar — opuesto a Isomorphic Labs.

---

## 6. Comparativa rápida con `isomorphicdesign`

| Eje | 498ASdesign | isomorphicdesign |
|-----|-------------|------------------|
| Voz | Tecno-comercial, asertiva, ES | Científica, contenida, EN |
| Color base | Negro + verde fluor | Blanco + steel grey |
| Display | Bebas Neue 600 UPPER | Söhne Extraleicht 200 |
| Body | Hepta Slab 300 (slab) | Söhne Leicht 300 (sans) |
| Densidad | Alta, información-first | Aire blanco, idea-first |
| Acento | 1 verde radioactivo | 7 familias editoriales |
| Hero | 100 vh + foto con overlay | 660 px + claim grande |
| Radios | 0–4 px (angular) | 12–20 px (suaves) |

Son **opuestos deliberados** — coherente con la posición de cada marca: 498 vende ejecución y energía; Isomorphic vende rigor científico.

---

## 7. Ficheros del kit

| Fichero | Contenido |
|---------|-----------|
| `README.md` | Este documento. |
| `tokens.css` | Variables CSS + import de Google Fonts + clases utilitarias. |
| `showcase.html` | Visualización tipográfica, paleta, hero, counters, botones, cards. |

---

*Extraído de producción el 2026-05-15. Fuente: CSS público de 498as.com (Elementor + Hello Elementor child theme). Fuentes vía Google Fonts.*
