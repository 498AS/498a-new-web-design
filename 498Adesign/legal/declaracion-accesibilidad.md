---
title: Declaración de Accesibilidad · 498 Advance
slug: declaracion-accesibilidad
languages:
  - es
  - ca
  - en
# CA y EN traducidas desde ES · borrador pendiente revisión legal
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

# Declaració d'Accessibilitat · 498 Advance

> **Esborrany**: traducció al català realitzada des de la versió castellana. Pendent de revisió i validació per l'equip legal de 498 Advance.

498 Advanced Solutions SL (d'ara endavant, **498 Advance** o **498A**) es compromet a fer accessible el seu lloc web `www.498a.com` de conformitat amb el Reial Decret 1112/2018 de 7 de setembre, sobre accessibilitat dels llocs web i aplicacions per a dispositius mòbils del sector públic (transposició de la Directiva (UE) 2016/2102 a l'ordenament jurídic espanyol) i la **Directiva (UE) 2019/882 — European Accessibility Act**, aplicable a productes i serveis privats des del 28 de juny de 2025.

La present Declaració d'Accessibilitat s'aplica al lloc `www.498a.com`.

---

## Situació de compliment

Aquest lloc web és **parcialment conforme** amb la norma **UNE-EN 301 549:2022**, que recull els requisits d'accessibilitat WCAG 2.1 nivell AA, a causa de les excepcions i de la manca de conformitat dels aspectes que s'indiquen a continuació.

---

## Contingut no accessible

El contingut que es recull a continuació no és accessible pels motius següents:

### 1. Manca de conformitat pendent d'auditoria externa professional

A data de **18 de maig de 2026**, aquesta declaració es basa en una **revisió manual interna** de l'equip de 498A. Està pendent de:

- **Auditoria professional externa** per entitat certificada en accessibilitat (Funka, accessibility.es o una altra acreditada).
- **Tests automatitzats** amb axe DevTools i Lighthouse en pre-producció.
- **Tests d'usabilitat amb persones usuàries de tecnologies de suport** (lectors de pantalla, navegació per teclat, alt contrast).

Fins que aquests tests no es completin, es publiquen com a "no auditats" els mòduls següents:

- Hero amb vídeo autoplay (vídeo sense subtítols ni descripció detallada en pista alternativa).
- Animacions decoratives: pattern band animada, persiana scaleY en caixes, typewriter reveal en eyebrows d'alta jerarquia.
- Components interactius del playground stress-test (gestor de cookies, selector d'idioma, navegació principal).

### 2. Contingut pendent

- **Subtítols del vídeo hero**: el vídeo del hero es reprodueix en bucle, sense àudio significatiu (és atmosfèric) però sense pista de text descriptiva. S'inclourà descripció en `<track kind="descriptions">` quan se substitueixi per contingut productiu.
- **Versions en català i anglès** d'alguns textos legals (Avís Legal, Política de Privacitat, Política de Cookies).
- **Auditoria de contrast exhaustiva** en components derivats del design system v2.1 quan es desplegui en producció.

### 3. Càrrega desproporcionada

No s'invoquen exempcions per càrrega desproporcionada en aquesta versió.

---

## Millores d'accessibilitat ja implementades

Com a part del redisseny v2.1 del lloc (maig 2026), s'han incorporat les mesures següents:

### Estructura semàntica
- HTML semàntic amb landmarks `<nav>`, `<main>`, `<header>`, `<footer>`, `<section>`, `<article>`, `<aside>`.
- **Enllaç de salt** "Saltar al contingut principal" visible en rebre el focus de teclat (WCAG 2.4.1).
- Jerarquia de capçaleres consistent (`h1` → `h2` → `h3` sense salts directes).

### Navegació per teclat
- **Focus visible global** amb outline verd de 2 px i offset 2 px en tots els elements interactius (WCAG 2.4.7).
- **Tab order lògic** a la navegació principal, selector d'idioma i formularis.
- **Tecla Escape** tanca el modal de cookies (WCAG 2.1.2).
- **Focus trap** dins del modal de cookies amb retorn del focus a l'element que el va invocar (WCAG 2.4.3).

### Color i contrast
- Verd marca primari (`#2DD60F`, ràtio 2.83:1 sobre blanc) reservat a fons foscos i elements no textuals.
- Verd profund (`#0E7A1F`, ràtio 6.1:1 sobre blanc) utilitzat en text i enllaços sobre fons clar · compleix AA.
- Color de text secundari pujat a `#717171` (ràtio 4.6:1) · compleix AA per a body text.
- Color de text principal `#1A1A1A` (ràtio 16.9:1) · compleix AAA.

### Lectors de pantalla
- **Atributs ARIA**: `aria-label`, `aria-current`, `aria-modal`, `aria-labelledby`, `aria-hidden`, `role="dialog"` aplicats on correspon.
- **Elements decoratius** (marques SVG, frame-cross corners, separadors) marcats com `aria-hidden="true"`.
- **Atribut `lang`** declarat en cada bloc d'idioma als documents legals.
- **Text alternatiu `sr-only`** per al typewriter reveal de l'eyebrow "Founder Voice" (els lectors de pantalla reben el text complet, mentre l'animació visual es manté per a usuaris sense tecnologies de suport).

### Animacions i moviment
- Suport complet de **`prefers-reduced-motion`** en totes les animacions de la web (pattern band, persiana, typewriter, gradient drift, shimmer).
- Vídeo hero sense so (`muted`) per defecte. Loops curts sense transicions agressives.

### Formularis i controls
- Toggles del gestor de cookies amb `<label>` envoltant `<input>` (associació nativa).
- Focus visible explícit en estat `:focus-visible`.
- Mides de touch target ≥ 44 × 44 px en pantalles tàctils per al selector d'idioma (WCAG 2.5.5).

---

## Preparació de la present declaració

La present declaració va ser preparada el **18 de maig de 2026**.

El mètode emprat per preparar la declaració ha estat una **autoavaluació** duta a terme pel propi equip de 498A, sobre la versió v2.1 del nou lloc web (encara en pre-producció).

Última revisió de la declaració: **18 de maig de 2026**.

---

## Observacions i dades de contacte

Pots realitzar comunicacions sobre requisits d'accessibilitat (Article 10.2.a del RD 1112/2018) com per exemple:

- Informar sobre qualsevol possible incompliment per part d'aquest lloc web.
- Transmetre altres dificultats d'accés al contingut.
- Formular qualsevol altra consulta o suggeriment de millora relativa a l'accessibilitat del lloc web.

A través del correu electrònic: **accesibilidad@498a.com**

Les comunicacions seran rebudes i tractades per 498 Advanced Solutions SL.

---

## Procediment d'aplicació

En el cas que, un cop realitzada una sol·licitud d'informació accessible o queixa, aquesta hagi estat desestimada, no s'estigui d'acord amb la decisió adoptada, o la resposta no compleixi els requisits previstos a l'article 12.5 del RD 1112/2018, la persona interessada podrà iniciar una reclamació per conèixer i oposar-se als motius de la desestimació, instar l'adopció de les mesures oportunes en cas de no estar d'acord amb la decisió adoptada, o exposar les raons per les quals es considera que la resposta no compleix els requisits exigits.

La reclamació es pot presentar a través del correu: **accesibilidad@498a.com**

---

## Contingut opcional

### Disseny tècnic

Aquest lloc web ha estat desenvolupat sobre un design system propi (`498Adesign v2.1`) basat en HTML5 semàntic, CSS3 i JavaScript vanilla mínim (un únic `IntersectionObserver` per a animacions d'entrada en viewport i un mòdul de gestió de consent de cookies).

No utilitza frameworks reactius pesants (React, Vue, Angular) que generin arbres d'accessibilitat opacs.

### Compatibilitat amb navegadors i tecnologies de suport

El lloc web és compatible amb les versions més recents dels navegadors i combinacions de tecnologies de suport següents (pendent de tests formals):

- **Chrome, Edge, Firefox, Safari** (últimes 2 versions) a escriptori.
- **Chrome i Safari** en dispositius mòbils iOS i Android.
- Lectors de pantalla **NVDA + Firefox** i **VoiceOver + Safari** (pendent test formal).

### Tecnologies utilitzades

HTML5 · CSS3 · JavaScript (ES5 vanilla · `IntersectionObserver` · `localStorage` API).

---

## Propers passos per assolir conformitat plena

1. **Auditoria professional externa** amb entitat certificada abans del go-live.
2. **Tests automatitzats continus** amb axe DevTools / Lighthouse / WAVE integrats a CI.
3. **Tests d'usabilitat** amb persones usuàries de tecnologies de suport.
4. **Subtítols i descripcions** per al vídeo del hero quan se substitueixi per contingut productiu.
5. **Versions CA i EN** de tots els textos legals.
6. **Revisió semestral** de la declaració un cop en producció.

---

# Accessibility Statement · 498 Advance

> **Draft**: English translation from the Spanish version. Pending review and validation by 498 Advance's legal team.

498 Advanced Solutions SL (hereinafter, **498 Advance** or **498A**) is committed to making its website `www.498a.com` accessible in accordance with Royal Decree 1112/2018 of 7 September, on the accessibility of public sector websites and mobile applications (transposition of Directive (EU) 2016/2102 into the Spanish legal system) and **Directive (EU) 2019/882 — European Accessibility Act**, applicable to private products and services since 28 June 2025.

This Accessibility Statement applies to the website `www.498a.com`.

---

## Conformance status

This website is **partially conformant** with **UNE-EN 301 549:2022**, which sets out the WCAG 2.1 Level AA accessibility requirements, due to the exceptions and non-conformance of the aspects listed below.

---

## Non-accessible content

The content listed below is not accessible for the following reasons:

### 1. Non-conformance pending external professional audit

As of **18 May 2026**, this statement is based on an **internal manual review** by the 498A team. Pending:

- **External professional audit** by an entity certified in accessibility (Funka, accessibility.es or another accredited body).
- **Automated tests** with axe DevTools and Lighthouse in pre-production.
- **Usability tests with users of assistive technologies** (screen readers, keyboard navigation, high contrast).

Until these tests are completed, the following modules are published as "non-audited":

- Hero with autoplay video (video without subtitles or detailed description in an alternative track).
- Decorative animations: animated pattern band, scaleY shutter on boxes, typewriter reveal on high-hierarchy eyebrows.
- Interactive components of the stress-test playground (cookie manager, language selector, main navigation).

### 2. Pending content

- **Hero video subtitles**: the hero video plays in a loop, without significant audio (it is atmospheric) but without a descriptive text track. A description will be included in `<track kind="descriptions">` when it is replaced by production content.
- **Catalan and English versions** of some legal texts (Legal Notice, Privacy Policy, Cookie Policy).
- **Exhaustive contrast audit** of components derived from design system v2.1 once deployed to production.

### 3. Disproportionate burden

No disproportionate burden exemptions are invoked in this version.

---

## Accessibility improvements already implemented

As part of the v2.1 redesign of the site (May 2026), the following measures have been incorporated:

### Semantic structure
- Semantic HTML with `<nav>`, `<main>`, `<header>`, `<footer>`, `<section>`, `<article>`, `<aside>` landmarks.
- **Skip link** "Skip to main content" visible when receiving keyboard focus (WCAG 2.4.1).
- Consistent heading hierarchy (`h1` → `h2` → `h3` without direct jumps).

### Keyboard navigation
- **Global focus visible** with 2 px green outline and 2 px offset on all interactive elements (WCAG 2.4.7).
- **Logical tab order** in main navigation, language selector and forms.
- **Escape key** closes the cookie modal (WCAG 2.1.2).
- **Focus trap** inside the cookie modal with focus return to the element that invoked it (WCAG 2.4.3).

### Color and contrast
- Primary brand green (`#2DD60F`, 2.83:1 ratio on white) reserved for dark backgrounds and non-textual elements.
- Deep green (`#0E7A1F`, 6.1:1 ratio on white) used for text and links on light background · meets AA.
- Secondary text color raised to `#717171` (4.6:1 ratio) · meets AA for body text.
- Main text color `#1A1A1A` (16.9:1 ratio) · meets AAA.

### Screen readers
- **ARIA attributes**: `aria-label`, `aria-current`, `aria-modal`, `aria-labelledby`, `aria-hidden`, `role="dialog"` applied where appropriate.
- **Decorative elements** (SVG marks, frame-cross corners, separators) marked as `aria-hidden="true"`.
- **`lang` attribute** declared on each language block in legal documents.
- **`sr-only` alternative text** for the typewriter reveal of the "Founder Voice" eyebrow (screen readers receive the full text, while the visual animation remains for users without assistive technologies).

### Animations and motion
- Full support for **`prefers-reduced-motion`** across all animations on the site (pattern band, shutter, typewriter, gradient drift, shimmer).
- Hero video without sound (`muted`) by default. Short loops without aggressive transitions.

### Forms and controls
- Cookie manager toggles with `<label>` wrapping `<input>` (native association).
- Explicit focus visible on `:focus-visible` state.
- Touch target sizes ≥ 44 × 44 px on touch screens for the language selector (WCAG 2.5.5).

---

## Preparation of this statement

This statement was prepared on **18 May 2026**.

The method used to prepare the statement was a **self-assessment** carried out by the 498A team itself, on version v2.1 of the new website (still in pre-production).

Last review of the statement: **18 May 2026**.

---

## Observations and contact details

You may submit communications regarding accessibility requirements (Article 10.2.a of Royal Decree 1112/2018) such as:

- Reporting any possible non-compliance by this website.
- Conveying other difficulties in accessing the content.
- Submitting any other query or suggestion for improvement regarding the accessibility of the website.

Through email: **accesibilidad@498a.com**

Communications will be received and processed by 498 Advanced Solutions SL.

---

## Enforcement procedure

If, once a request for accessible information or a complaint has been made, it has been rejected, you do not agree with the decision adopted, or the response does not meet the requirements set out in Article 12.5 of Royal Decree 1112/2018, the interested party may initiate a claim to ascertain and contest the reasons for the rejection, request the adoption of appropriate measures if not in agreement with the decision adopted, or set out the reasons why the response is deemed not to meet the required standards.

The claim may be submitted through email: **accesibilidad@498a.com**

---

## Optional content

### Technical design

This website has been developed on a proprietary design system (`498Adesign v2.1`) based on semantic HTML5, CSS3 and minimal vanilla JavaScript (a single `IntersectionObserver` for viewport entry animations and a cookie consent management module).

It does not use heavy reactive frameworks (React, Vue, Angular) that generate opaque accessibility trees.

### Compatibility with browsers and assistive technologies

The website is compatible with the most recent versions of the following browsers and combinations of assistive technologies (pending formal testing):

- **Chrome, Edge, Firefox, Safari** (latest 2 versions) on desktop.
- **Chrome and Safari** on iOS and Android mobile devices.
- Screen readers **NVDA + Firefox** and **VoiceOver + Safari** (pending formal testing).

### Technologies used

HTML5 · CSS3 · JavaScript (ES5 vanilla · `IntersectionObserver` · `localStorage` API).

---

## Next steps to achieve full conformance

1. **External professional audit** by a certified entity before go-live.
2. **Continuous automated tests** with axe DevTools / Lighthouse / WAVE integrated in CI.
3. **Usability tests** with users of assistive technologies.
4. **Subtitles and descriptions** for the hero video when replaced by production content.
5. **CA and EN versions** of all legal texts.
6. **Biannual review** of the statement once in production.

---

*Última actualización: 2026-05-18. Documento mantenido por 498 Advance · 498 Advanced Solutions SL · CIF B64519622.*
