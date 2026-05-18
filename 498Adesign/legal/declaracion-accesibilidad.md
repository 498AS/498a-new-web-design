---
title: Declaración de Accesibilidad · 498 Advance
slug: declaracion-accesibilidad
languages:
  - es
  - ca  # pendiente
  - en  # pendiente
entity: 498 Advanced Solutions SL
cif: B64519622
domain_target: www.498a.com
last_updated: 2026-05-18
conformance_level: parcialmente conforme
standard: WCAG 2.1 nivel AA
framework_legal:
  - UNE-EN 301 549:2022
  - RD 1112/2018 (transposición Directiva UE 2016/2102)
  - European Accessibility Act (Directiva UE 2019/882 · aplicable desde junio 2025)
audit_method: revisión manual + axe DevTools + Lighthouse pendiente
audit_date: 2026-05-18 (revisión manual interna)
status: borrador · pendiente audit externo profesional antes de publicación
---

# Declaración de Accesibilidad · 498 Advance

498 Advanced Solutions SL (en adelante, **498 Advance** o **498A**) se compromete a hacer accesible su sitio web `www.498a.com` de conformidad con el Real Decreto 1112/2018 de 7 de septiembre, sobre accesibilidad de los sitios web y aplicaciones para dispositivos móviles del sector público (transposición de la Directiva (UE) 2016/2102 al ordenamiento jurídico español) y la **Directiva (UE) 2019/882 — European Accessibility Act**, aplicable a productos y servicios privados desde el 28 de junio de 2025.

La presente Declaración de Accesibilidad se aplica al sitio `www.498a.com`.

---

## Situación de cumplimiento

Este sitio web es **parcialmente conforme** con la norma **UNE-EN 301 549:2022**, que recoge los requisitos de accesibilidad WCAG 2.1 nivel AA, debido a las excepciones y a la falta de conformidad de los aspectos que se indican a continuación.

---

## Contenido no accesible

El contenido que se recoge a continuación no es accesible por los siguientes motivos:

### 1. Falta de conformidad pendiente de auditoría externa profesional

A fecha de **18 de mayo de 2026**, esta declaración se basa en una **revisión manual interna** del equipo de 498A. Está pendiente de:

- **Auditoría profesional externa** por entidad certificada en accesibilidad (Funka, accessibility.es u otra acreditada).
- **Tests automatizados** con axe DevTools y Lighthouse en pre-producción.
- **Tests de usabilidad con personas usuarias de tecnologías de apoyo** (lectores de pantalla, navegación por teclado, alto contraste).

Hasta que estos tests se completen, se publican como "no auditados" los siguientes módulos:

- Hero con vídeo autoplay (vídeo sin subtítulos ni descripción detallada en pista alternativa).
- Animaciones decorativas: pattern band animada, persiana scaleY en cajas, typewriter reveal en eyebrows de alta jerarquía.
- Componentes interactivos del playground stress-test (gestor de cookies, selector de idioma, navegación principal).

### 2. Contenido pendiente

- **Subtítulos del vídeo hero**: el vídeo del hero se reproduce en bucle, sin audio significativo (es atmosférico) pero sin pista de texto descriptiva. Se incluirá descripción en `<track kind="descriptions">` cuando se reemplace por contenido productivo.
- **Versiones en catalán e inglés** de algunos textos legales (Aviso Legal, Política de Privacidad, Política de Cookies).
- **Auditoría de contraste exhaustiva** en componentes derivados del design system v2.1 cuando se desplieguen en producción.

### 3. Carga desproporcionada

No se invocan exenciones por carga desproporcionada en esta versión.

---

## Mejoras de accesibilidad ya implementadas

Como parte del rediseño v2.1 del sitio (mayo 2026), se han incorporado las siguientes medidas:

### Estructura semántica
- HTML semántico con landmarks `<nav>`, `<main>`, `<header>`, `<footer>`, `<section>`, `<article>`, `<aside>`.
- **Skip link** "Saltar al contenido principal" visible al recibir focus de teclado (WCAG 2.4.1).
- Jerarquía de encabezados consistente (`h1` → `h2` → `h3` sin saltos directos).

### Navegación por teclado
- **Focus visible global** con outline verde de 2 px y offset 2 px en todos los elementos interactivos (WCAG 2.4.7).
- **Tab order lógico** en navegación principal, selector de idioma y formularios.
- **Tecla Escape** cierra el modal de cookies (WCAG 2.1.2).
- **Focus trap** dentro del modal de cookies con devolución del focus al elemento que lo invocó (WCAG 2.4.3).

### Color y contraste
- Verde marca primario (`#2DD60F`, ratio 2.83:1 sobre blanco) reservado a fondos oscuros y elementos no textuales.
- Verde profundo (`#0E7A1F`, ratio 6.1:1 sobre blanco) utilizado en texto y enlaces sobre fondo claro · cumple AA.
- Color de texto secundario subido a `#717171` (ratio 4.6:1) · cumple AA para body text.
- Color de texto principal `#1A1A1A` (ratio 16.9:1) · cumple AAA.

### Lectores de pantalla
- **Atributos ARIA**: `aria-label`, `aria-current`, `aria-modal`, `aria-labelledby`, `aria-hidden`, `role="dialog"` aplicados donde procede.
- **Elementos decorativos** (marcas SVG, frame-cross corners, separadores) marcados como `aria-hidden="true"`.
- **Atributo `lang`** declarado en cada bloque de idioma en los documentos legales.
- **Texto alternativo `sr-only`** para el typewriter reveal del eyebrow "Founder Voice" (los lectores de pantalla reciben el texto completo, mientras la animación visual permanece para usuarios sin tecnologías de apoyo).

### Animaciones y movimiento
- Soporte completo de **`prefers-reduced-motion`** en todas las animaciones de la web (pattern band, persiana, typewriter, gradient drift, shimmer).
- Vídeo hero sin sonido (`muted`) por defecto. Loops cortos sin transiciones agresivas.

### Formularios y controles
- Toggles del gestor de cookies con `<label>` envolviendo `<input>` (asociación nativa).
- Focus visible explícito en estado `:focus-visible`.
- Tamaños de touch target ≥ 44 × 44 px en pantallas táctiles para el selector de idioma (WCAG 2.5.5).

---

## Preparación de la presente declaración

La presente declaración fue preparada el **18 de mayo de 2026**.

El método empleado para preparar la declaración ha sido una **autoevaluación** llevada a cabo por el propio equipo de 498A, sobre la versión v2.1 del nuevo sitio web (todavía en pre-producción).

Última revisión de la declaración: **18 de mayo de 2026**.

---

## Observaciones y datos de contacto

Puedes realizar comunicaciones sobre requisitos de accesibilidad (Artículo 10.2.a del RD 1112/2018) como por ejemplo:

- Informar sobre cualquier posible incumplimiento por parte de este sitio web.
- Transmitir otras dificultades de acceso al contenido.
- Formular cualquier otra consulta o sugerencia de mejora relativa a la accesibilidad del sitio web.

A través del correo electrónico: **accesibilidad@498a.com**

Las comunicaciones serán recibidas y tratadas por 498 Advanced Solutions SL.

---

## Procedimiento de aplicación

En el caso de que, una vez realizada una solicitud de información accesible o queja, ésta hubiera sido desestimada, no se estuviera de acuerdo con la decisión adoptada, o la respuesta no cumpliera los requisitos contemplados en el artículo 12.5 del RD 1112/2018, la persona interesada podrá iniciar una reclamación para conocer y oponerse a los motivos de la desestimación, instar la adopción de las medidas oportunas en el caso de no estar de acuerdo con la decisión adoptada, o exponer las razones por las que se considera que la respuesta no cumple con los requisitos exigidos.

La reclamación puede presentarse a través del correo: **accesibilidad@498a.com**

---

## Contenido opcional

### Diseño técnico

Este sitio web ha sido desarrollado sobre un design system propio (`498Adesign v2.1`) basado en HTML5 semántico, CSS3 y JavaScript vanilla mínimo (un único `IntersectionObserver` para animaciones de entrada en viewport y un módulo de gestión de consent de cookies).

No utiliza frameworks reactivos pesados (React, Vue, Angular) que generen árboles de accesibilidad opacos.

### Compatibilidad con navegadores y tecnologías de apoyo

El sitio web es compatible con las versiones más recientes de los siguientes navegadores y combinaciones de tecnologías de apoyo (pendiente de tests formales):

- **Chrome, Edge, Firefox, Safari** (últimas 2 versiones) en escritorio.
- **Chrome y Safari** en dispositivos móviles iOS y Android.
- Lectores de pantalla **NVDA + Firefox** y **VoiceOver + Safari** (pendiente test formal).

### Tecnologías utilizadas

HTML5 · CSS3 · JavaScript (ES5 vanilla · `IntersectionObserver` · `localStorage` API).

---

## Próximos pasos para alcanzar conformidad plena

1. **Auditoría profesional externa** con entidad certificada antes del go-live.
2. **Tests automatizados continuos** con axe DevTools / Lighthouse / WAVE integrados en CI.
3. **Tests de usabilidad** con personas usuarias de tecnologías de apoyo.
4. **Subtítulos y descripciones** para vídeo del hero cuando se sustituya por contenido productivo.
5. **Versiones CA y EN** de todos los textos legales.
6. **Revisión semestral** de la declaración una vez en producción.

---

## Versión EN · Accessibility Statement

> Pending translation. The Spanish version is the canonical source until the English version is reviewed by the legal team.

## Versión CA · Declaració d'Accessibilitat

> Pendent de traducció. La versió en castellà és la font canònica fins que la versió en català sigui revisada per l'equip legal.

---

*Última actualización: 2026-05-18. Documento mantenido por 498 Advance · 498 Advanced Solutions SL · CIF B64519622.*
