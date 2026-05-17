# 498A · new web design

Rediseño completo de la web pública de **498A** (consultora de IA aplicada del grupo Zoopa). Incluye:

- Design system v2 (post-rebrand 498AS → 498A)
- Tokens CSS, showcase visual y playground de stress-test
- Copy completo de la home en castellano (versión review iterada)
- Logos vectoriales corregidos (sin "S" final, sin typo "ADVATCED")
- Assets brand (video hero, fotos equipo, visuales 3D, iconos)
- Patrones SVG propios (trama de píxeles, cuadrícula backpropagation, hexagramas I Ching)
- Referencia del análisis del estilo de [isomorphiclabs.com](https://www.isomorphiclabs.com/) que sirve como espejo

---

## Estructura

```
498a-new-web-design/
├── 498Adesign/              ← canonical · v2 · post-rebrand
│   ├── tokens.css           ← variables CSS, escala tipográfica, gradientes
│   ├── showcase.html        ← visualización del sistema completo
│   ├── playground.html      ← stress-test navegable con Lorem Ipsum
│   ├── README.md            ← documentación del sistema
│   └── assets/
│       ├── logos/           ← 498A wordmark · georadar isotype + wordmark
│       ├── team/            ← Carlos Ortet · equipo Barcelona
│       ├── video/           ← hero loop + loops productos/servicios
│       ├── icons/           ← proyectos · países · experiencia · LinkedIn
│       ├── visuals/         ← cubos isométricos · capas 3D · ecosistema
│       └── patterns/        ← grid-backprop · pixel-mosaic · hexagrams · etc.
│
├── 498ASdesign/             ← legacy · v1 · referencia histórica
│   └── assets/              ← assets originales descargados de 498as.com
│
├── isomorphicdesign/        ← análisis del referente
│   ├── tokens.css           ← tokens extraídos de isomorphiclabs.com
│   ├── showcase.html        ← demo del sistema Isomorphic
│   └── README.md            ← extracción canónica
│
├── assets/                  ← logos brand originales (incl. PNG legacy)
│   └── fixed/               ← logos vectoriales corregidos (post-rebrand)
│
├── 498A-homepage-REVIEW.md  ← copy limpio para revisión
├── 498A-homepage-copy.md    ← master doc con notas de implementación
└── README.md                ← este documento
```

---

## Decisiones de sistema

**Posicionamiento aprobado**: consultora de IA aplicada con I+D hacia simulación social (Gerard).

**Paleta**:
- Brand: `#2DD60F` verde primario · `#0E7A1F` verde profundo (un punto menos estridente que el fluor original `#37E813`)
- Greys: tier de 10 niveles `#F7F7F7` → `#1A1A1A`
- Esquinas: angular, máximo `4 px` (sin redondeos suaves de Isomorphic)

**Tipografía**: Hepta Slab Light 200/300 italic para displays. Roboto Mono UPPER para tags y metadata. Bebas Neue reservado para nav brand y números grandes. Todo desde Google Fonts.

**Dominante visual**: light total. Negro reservado para video hero full-bleed y citas tipo ChatGPT (cuadradito negro 16×16 + número blanco).

**Sistema editorial**: cajas en contacto con bordes compartidos · animación persiana al entrar al viewport · trama de cuadrícula backpropagation (puntos grises + diagonal verde con gradients) en bands decorativos · hipervínculos verde profundo con underline sutil.

---

## Cómo abrirlo

```bash
# Stress-test playground (todos los componentes en Lorem Ipsum)
open 498Adesign/playground.html

# Showcase del sistema (todos los tokens documentados)
open 498Adesign/showcase.html

# Referente Isomorphic (análisis del estilo de referencia)
open isomorphicdesign/showcase.html
```

---

## Stack de implementación

Pensado para maquetar en **Webflow** o WordPress (Elementor + tema custom). Los tokens son CSS puro sin dependencias. Las animaciones son CSS + un único `IntersectionObserver` mínimo (10 líneas de JS).

---

## Estado actual y próximos pasos

- ✅ Design system v2 completo (tokens + showcase + playground)
- ✅ Copy de la home v3 cerrada (8 puntos del grill resueltos)
- ✅ Logos 498A corregidos (rebrand 498AS → 498A · typo ADVATCED → ADVANCED)
- ✅ Identidad visual extendida (paleta · grid · patrones · trama backprop)
- ⏳ Maquetación final en plataforma (Webflow / WP)
- ⏳ Imagen IA real de cubos isométricos para Vision card (placeholder SVG actual)
- ⏳ Permisos de publicación de los 3 testimonios reales (Specialisterne · imagin · NAOS)
- ⏳ Reemplazar texto Lorem Ipsum del playground por copy real al maquetar

---

## Créditos

- **Carlos Ortet** · founder 498A · dirección creativa, copy, validación
- Diseño desarrollado con [Claude Code](https://claude.com/claude-code)
- Estilo visual inspirado en [isomorphiclabs.com](https://www.isomorphiclabs.com/)

---

*2026-05-17 · Barcelona · 498A · Una compañía del grupo Zoopa*
