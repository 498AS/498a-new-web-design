# Logos 498A & georadar — v2 (fuente buena)

Versión final basada en los **SVGs vectoriales originales aportados por marca** (2026-05-16), ya con el rebrand 498A aplicado y el descriptor `ADVANCED` correcto.

---

## Fuentes originales

| Archivo fuente | Contenido | viewBox |
|----------------|-----------|---------|
| `assets/498_A_ADVANCED_SINBOCADILLOogo.svg` | Wordmark "498A" + descriptor "ADVANCED" sin bocadillo. **Fuente buena recomendada.** | 0 0 194.96 170.27 |
| `assets/498_A_ADVANCED_ogo.svg` | Mismo lockup dentro del pin/bocadillo geográfico. | 0 0 194.96 273.11 |

Los dos originales ya están limpios:
- ✅ Solo "498A" (sin la S del antiguo "498AS")
- ✅ Descriptor `ADVANCED` con grafía correcta (8 letras: A-D-V-A-N-C-E-D, sin la T extra del typo "ADVATCED")
- ✅ Paths vectoriales bien estructurados (export Adobe Illustrator 30.2.1)

---

## Variantes generadas

### Wordmark sin bocadillo · **uso principal**

| Archivo | Fill | Uso |
|---------|------|-----|
| **`498A_ADVANCED_white.svg`** | `#ffffff` | Sobre fondo oscuro — marca principal en `498Adesign` (dark mode) |
| **`498A_ADVANCED_black.svg`** | `#000000` | Sobre fondo claro — documentos, print |
| **`498A_ADVANCED_green.svg`** | `#37E813` | Brand green — acento, header en oscuro |

### Pin con bocadillo · sticker / sello

| Archivo | Fill | Uso |
|---------|------|-----|
| `498A_ADVANCED_pin_green.svg` | `#37E813` | **Iconic** sobre fondo blanco — los huecos del wordmark muestran el bg |
| `498A_ADVANCED_pin_white.svg` | `#ffffff` | Sobre fondo oscuro |
| `498A_ADVANCED_pin_black.svg` | `#000000` | Sobre fondo claro · print neutro |

> ⚠️ Las versiones pin son **path único con cutouts** — el wordmark son huecos en el bocadillo. Funcionan colocándose sobre un fondo de color contrastado. Si necesitas la versión "pin verde + wordmark blanco self-contained", hay que componerlo en Illustrator o pídeme una versión con `clipPath`.

### georadar

| Archivo | Uso |
|---------|-----|
| **`georadar_wordmark_white.svg`** | Wordmark `georadar` sobre fondos oscuros |
| **`georadar_isotype_black.svg`** | Isotipo vectorial (la "g" + eco satélite) — favicon, marca de app, sello pequeño |

---

## Cambios respecto a la v1

La v1 (eliminada) la generé yo desde el SVG viejo del servidor (`498_LOGO_BLANCO.svg`) haciendo cirugía sobre paths — eliminé quirúrgicamente la "S" y reconstruí el descriptor con Anton porque tenía el typo "ADVATCED".

La **v2 que entrega esta carpeta** se basa en los archivos correctos de marca, así que:
- ✅ La tipografía del descriptor es la **original real** (no Anton sustituta).
- ✅ El kerning y proporción son los oficiales.
- ✅ El lockup con bocadillo es el diseño de marca correcto (no mi reconstrucción aproximada).

---

## Propagación al design system

Los 6 SVGs de 498A + 2 SVGs de georadar se han copiado a:
`498ASdesign/assets/logos/`

El antiguo `498_LOGO_BLANCO.svg` (del servidor, con typo + "498AS") queda como `.deprecated.svg` para trazabilidad.

---

## Próximos pasos

1. **Subir estos SVG a la mediateca de WordPress** (`https://498as.com/wp-admin`) y actualizar referencias del tema. El logo blanco del servidor debería pasar a `498A_ADVANCED_white.svg`.
2. **Renombrar la carpeta del design system** `498ASdesign/` → `498Adesign/` cuando confirmes que no rompe nada externo.
3. **Pin self-contained**: si lo necesitas como asset auto-suficiente (no dependiente del bg), pídemelo y te genero la versión con `clipPath` + `rect` blanco detrás.
4. **Renombrar los archivos fuente originales** — los nombres tienen un typo: `498_A_ADVANCED_ogo.svg` y `498_A_ADVANCED_SINBOCADILLOogo.svg` deberían ser `..._logo.svg`. No los he renombrado por respeto al archivo del usuario.

---

*Generado: 2026-05-16. Fuente: SVG originales aportados por marca.*
