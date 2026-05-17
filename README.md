# 498A · new web design

Rediseño completo de la web pública de **498A** (laboratorio de IA aplicada con I+D hacia simulación social, del grupo Zoopa). Incluye:

- **Design system v2.1** (post-rebrand 498AS → 498A · iteraciones del playground integradas)
- Tokens CSS, showcase visual y playground de stress-test navegable
- Copy completo de la home en castellano (versión review iterada)
- Logos vectoriales corregidos (sin "S" final, sin typo "ADVATCED")
- Assets brand (video hero, fotos equipo, visuales 3D, iconos)
- Patrones SVG propios (grid-backprop animado, pixel-mosaic, hexagramas I Ching)
- Componentes editoriales: nav raíl flotante, lang grid 2×3, pattern band oscura animada, gradient cards reutilizables, marcas geométricas SVG, typewriter reveal, citas ChatGPT inline, frame-cross marks
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

**Posicionamiento aprobado**: laboratorio de IA aplicada con I+D hacia simulación de agentes, personas, sociedades y entornos (Gerard).

**Paleta**:
- Brand: `#2DD60F` verde primario · `#0E7A1F` verde profundo (un punto menos estridente que el fluor original `#37E813`)
- Greys: tier de 10 niveles `#F7F7F7` → `#1A1A1A`
- Surface lab: `#0F1410` (pattern band oscura · casi-negro con deriva verde)
- **Esquinas: angular, 0 px en botones/cards/eyebrow-square** (radius-2 = 4 px reservado solo a forms/badges)

**Tipografía**: Hepta Slab Light 200/300 italic para displays. Roboto Mono UPPER para tags y metadata. Bebas Neue reservado para nav brand y números grandes. Todo desde Google Fonts.

**Dominante visual**: light total. Black moments controlados: (1) video hero full-bleed, (2) pattern band entre secciones, (3) cuadradito de citas ChatGPT inline. Ritmo editorial: light → black hero → light → dark band → light.

**Sistema editorial**: cajas en contacto con bordes compartidos · animación persiana al entrar al viewport · nav transparente con clusters opacos flotando (brand+links + CTA) · pattern band oscura animada (`patternFlow 60s` + `gradientDrift 22s` + `shimmer 14s`) · gradient cards reutilizables (`vision-hero-card`) · marcas geométricas SVG (no iconos PNG) · typewriter reveal en eyebrows de máxima jerarquía · citas ChatGPT inline en 3 variantes.

**Filosofía de imagen**: 498A es lab de simulación, no biotech. Filtro para cada imagen: *¿lee como un mundo, sistema o agente generado, con reglas visibles?* Si sí, suma. Si solo es 3D decorativo, resta.

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

- ✅ **Design system v2.1** completo (tokens + showcase + playground + 12 componentes nuevos documentados en `498Adesign/README.md` §11)
- ✅ Copy de la home v3 cerrada (8 puntos del grill resueltos)
- ✅ Logos 498A corregidos (rebrand 498AS → 498A · typo ADVATCED → ADVANCED)
- ✅ Identidad visual extendida (paleta · grid · patrones · trama backprop animada)
- ✅ Filosofía de imagen alineada con lab framing (simulación de agentes/sociedades)
- ⏳ Validar el sistema en mobile (playground es desktop-first)
- ⏳ Actualizar `showcase.html` con los componentes v2.1 (opcional · el playground ya es source of truth)
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

*Actualizado v2.1 · 2026-05-17 · Barcelona · 498A · Una compañía del grupo Zoopa*
