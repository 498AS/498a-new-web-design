# 498A — Homepage copy v1

Copy de la nueva home de [498a.com](https://498a.com), redactado bajo el **esquema editorial de Isomorphic Labs** (un concepto por sección, aire blanco, voz declarativa) aplicado al posicionamiento corregido de 498A:

> **Consultora de IA aplicada. Cuatro capacidades en producción hoy (sistemas multiagente, visibilidad GEO en LLMs, IA privada y datasets a medida). Un programa de investigación a medio plazo orientado a la simulación de personas, grupos y sociedades.**

El copy se entrega como sistema de bloques (un bloque = una sección). Cada bloque incluye el copy final y una nota corta de implementación que mapea a los tokens de `isomorphicdesign` / `498ASdesign`.

---

## 00 · NAV

```
498A         capacidades   investigación   equipo   perspectivas   [ Hablemos → ]
```

**Implementación**: nav sticky 72 px, fondo negro con blur, separador 1 px charcoal, links en Roboto 14 / 500 / UPPER. CTA Roboto 14 con fondo verde `#37E813` sobre negro.

---

## 01 · HERO — *la frase grande*

> *(eyebrow)*
> **PROGRAMA DE INVESTIGACIÓN APLICADA · BARCELONA**
>
> *(display)*
> **Anticipar el comportamiento.<br>Construirlo antes de que llegue.**
>
> *(lead)*
> 498 segundos es el tiempo que tarda la luz del Sol en llegar a la Tierra. Lo que ya está pasando en el Sol todavía no lo vemos. Nuestro trabajo es construir los sistemas que permiten ver el comportamiento antes de que llegue al negocio, a la institución o a la sociedad.
>
> *(sub editorial)*
> 498A es una consultora de inteligencia artificial aplicada con un programa de investigación a medio plazo orientado a la simulación de personas, grupos y sociedades.
>
> *(CTA)*
> [ Hablemos → ]   ·   [ Ver capacidades ]

**Implementación** *(equivalente Isomorphic display 1 + paragraph longform)*:
- Hero 100 vh, fondo negro absoluto, foto opcional con overlay `#000 / .45`
- Display: Bebas Neue 100/1 sobre dos líneas, blanco; "Construirlo antes de que llegue" en verde `#37E813` para subrayar el verbo
- Eyebrow: Roboto Mono 12 / UPPER / `#37E813` / tracking +1.5 px
- Lead: Hepta Slab 24 / 1.4 / 300 / blanco / max-width 720 px
- CTA primary verde, secundaria ghost

---

## 02 · TESIS — *por qué existimos*

> *(eyebrow)*
> **TESIS · 01**
>
> *(headline)*
> **Entre la investigación y el negocio hay una distancia que casi nadie atraviesa.**
>
> *(body)*
> Los laboratorios producen modelos. Las consultoras los despliegan. Pocas casas viven a la vez en los dos lados. 498A trabaja en esa frontera — investigación rigurosa que produce código en producción, código en producción que genera preguntas de investigación. Es una elección deliberada. Es la única que permite anticipar.

**Implementación**: sección full-bleed con padding generoso (≥ 120 px vertical). Headline Hepta Slab 38 / 300, body Hepta Slab 22 / 300 / muted grey. Una sola columna, ancho 760 px. **Cero elementos decorativos.** El bloque transmite densidad solo por la rotundidad de la frase.

---

## 03 · MÉTODO — *cómo trabajamos*

> *(eyebrow)*
> **MÉTODO · 02**
>
> *(headline)*
> **Empezamos por el dato. Acabamos en la decisión.**
>
> *(body)*
> No hay inteligencia artificial útil sin datos propios. No hay despliegue serio sin control sobre el modelo. No hay valor sin medición sostenida en el tiempo. Cada proyecto que sale por la puerta de 498A pasa por las cuatro etapas — dataset, modelo, despliegue, medición — porque ninguna de ellas se entiende sin las otras tres.

**Implementación**: misma estructura que TESIS pero con un pequeño diagrama editorial debajo del body (cuatro pasos en mono UPPER en una sola línea horizontal, separados por puntos): `DATASET · MODELO · DESPLIEGUE · MEDICIÓN`. Roboto Mono 14 / UPPER / `#37E813` / tracking +2 px.

---

## 04 · CAPACIDADES — *lo que hacemos hoy*

> *(eyebrow)*
> **CAPACIDADES · LO QUE ENTREGAMOS EN PRODUCCIÓN**
>
> *(section title)*
> **Cuatro líneas de trabajo. Cada una autosuficiente. Las cuatro conectadas.**

> Cada capacidad debajo se presenta en una sección propia, no agrupadas en cards. Cada una ocupa una pantalla, con número grande Bebas Neue y body en Hepta Slab.

---

### 04 · A — SISTEMAS MULTIAGENTE

> *(eyebrow)*
> **CAPACIDAD 01 · SISTEMAS MULTIAGENTE**
>
> *(display number)*
> **01**
>
> *(headline)*
> **Equipos digitales que deciden, colaboran y aprenden.**
>
> *(body)*
> Los desplegamos en operaciones reales — atención al cliente, análisis de mercado, vigilancia regulatoria, generación de contenido — conectados a las herramientas que tu equipo ya usa. No son chatbots ni copilotos pasivos. Son agentes que orquestan tareas complejas, toman decisiones autónomas dentro de límites definidos y mejoran su comportamiento con cada interacción.
>
> *(proof)*
> **+100.000 horas manuales liberadas** para clientes en producción.

**Implementación**: número `01` en Bebas Neue 200 px verde `#37E813`, headline Hepta Slab 38 / 300 blanco, body Hepta Slab 20 / 300 muted, proof line en Roboto Mono 14 UPPER blanco con la cifra en verde brand. Layout asimétrico (número grande a la izquierda, copy a la derecha) — eco directo del estilo Isomorphic news cards pero adaptado al peso visual de 498A.

---

### 04 · B — VISIBILIDAD EN MOTORES GENERATIVOS (GEO)

> *(eyebrow)*
> **CAPACIDAD 02 · GEO · VISIBILIDAD EN MOTORES GENERATIVOS**
>
> *(display number)*
> **02**
>
> *(headline)*
> **La decisión de tu cliente se toma en ChatGPT, Claude, Gemini, Perplexity, Copilot y Google AI Overviews.**
>
> *(body)*
> Mientras tu competencia optimiza para Google clásico, los modelos generativos y los bloques AIO ya están filtrando, comparando y recomendando marcas en el momento exacto de la decisión. **GEORadar** —nuestra plataforma propia— audita ese espacio semántico con 3.000 a 30.000 prompts personalizados por estudio, ejecutados contra los seis motores. No es un dashboard genérico: es un sistema de seis módulos *(GEOAtlas · multi-LLM · GEOdesk · DOC · SAM · LEO)* que entrega visibilidad, preferencia, percepción, benchmark competitivo y trazabilidad de fuentes. Cierre con plan de acción de 90 días, no con un informe.
>
> *(verticals editorial — un párrafo extra)*
> Nueve verticales con KPIs propietarios cerrados: Travel, Finance, Health, Education, Corporate, Consumer, Energy, Mobility y Civic. Cada uno con su composite KPI. Cada uno probado con caso ancla en producción.
>
> *(proof)*
> **Primera consultora europea especializada en GEO.**
> **1.000.000+ prompts personalizados simulados.**
> **9.000.000+ menciones de marca analizadas.**
> **16+ marcas líderes en producción**: Banco Sabadell · Coca-Cola · Ford · Iberostar · Veolia · NAOS · Adeslas · Danone · La Caixa · Imagin · AstraZeneca · AXA · Nestlé · Dexeus Mujer · PortAventura · Generalitat de Catalunya · UE/INTPA · 3Cat · UAB · UVic *(entre otros)*.

---

### 04 · C — IA PRIVADA Y LOCAL

> *(eyebrow)*
> **CAPACIDAD 03 · IA PRIVADA**
>
> *(display number)*
> **03**
>
> *(headline)*
> **Modelos en tu infraestructura. Tu dato no sale de tu casa.**
>
> *(body)*
> Para empresas e instituciones que no pueden permitirse que sus datos atraviesen un API externo. Desplegamos modelos open-source ajustados a tu dominio, en tu infraestructura, bajo tu control. Cumplimiento del EU AI Act, soberanía del dato, latencia baja, coste predecible. La misma potencia que un modelo comercial sin el chantaje del vendor lock-in.
>
> *(proof)*
> **Marcos de gobernanza alineados con EU AI Act y UNESCO AI Working Group.**

---

### 04 · D — DATASETS A MEDIDA

> *(eyebrow)*
> **CAPACIDAD 04 · DATASETS**
>
> *(display number)*
> **04**
>
> *(headline)*
> **El cuello de botella de cualquier IA seria es el dato.**
>
> *(body)*
> Construimos corpus específicos para el problema concreto — anotación experta, validación cruzada con la Universitat Autònoma de Barcelona y el CSIC, trazabilidad metodológica que tus auditores aceptarán. Son los datos sobre los que se entrenarán los modelos que después decidirán dentro de tu organización. Su calidad es el techo de todo lo demás.
>
> *(proof)*
> **Co-fundadores académicos: UAB y CSIC. Colaboración activa desde 2023.**

---

## 05 · INVESTIGACIÓN — *hacia dónde vamos · Gerard*

> *(eyebrow)*
> **PROGRAMA DE I+D · GERARD · HORIZONTE 2026–2028**
>
> *(display)*
> **Generative Research<br>And Rapid Development.**
>
> *(sub display)*
> **Construyendo Gerard: investigación sintética asistida por IA.**
>
> *(body)*
> Las cuatro capacidades anteriores no son un catálogo cerrado. Son la infraestructura sobre la que estamos construyendo **Gerard** — *The Generative R&D Platform* — un sistema que simula el comportamiento de personas, grupos y poblaciones como entornos seguros donde una empresa puede ensayar un producto, una institución puede probar una política y un equipo puede observar el efecto cascada de una decisión antes de aplicarla.
>
> Es un horizonte de medio plazo. El piloto privado arranca en 2026 con tres clientes actuales del grupo. No se vende todavía. Es la razón por la que cada agente que entregamos, cada dataset que construimos y cada modelo privado que desplegamos hoy está pensado para escalar mañana hacia algo más grande: ensayar el futuro antes de que ocurra.
>
> *(connector visual — 4 líneas mono UPPER con flechas verdes)*
> SISTEMAS MULTIAGENTE → AGENT-BASED RESEARCH
> DATASETS A MEDIDA → POBLACIONES SINTÉTICAS VALIDADAS
> VISIBILIDAD GEO → PERSONAS SINTÉTICAS PARA TEST DE MARCA
> IA PRIVADA → SANDBOX SOBERANO DE SIMULACIÓN
>
> *(meta line)*
> Gerard se construye sobre el stack de **GEORadar** (GEOAtlas, GEOdesk, SAM, LEO, DOC) integrado con un Research Agent Orchestrator multiagente, un Participant Simulator de personas sintéticas y un Insight Synthesizer con RAG sobre datos propietarios. Stack europeo, GDPR by design, infraestructura AWS Frankfurt.

**Implementación**: sección con fondo `#0a0a0a` (más oscuro que el resto), display Bebas Neue 90 / 1 blanco a doble línea — el verbo *"AND"* del wordmark Generative Research **AND** Rapid Development en verde brand para subrayar el "rapid" como diferenciador del producto. Sub-display Hepta Slab 38 / 300 / muted. Prosa en Hepta Slab 22 / 300. El connector visual: cuatro líneas Roboto Mono 14 / UPPER con flechas `→` en verde brand y un punto al inicio. Meta line en Roboto 14 / muted al pie de la sección, casi como nota técnica.

---

## 06 · PRUEBA — *validación + escala + clientes*

> *(eyebrow)*
> **EVIDENCIA**
>
> *(headline)*
> **Investigación a la izquierda. Producción a la derecha. Escala en el medio.**

Tres columnas, una idea por columna. Sin más decoración.

| Investigación | Producción · Cartera GEORadar | Escala |
|---------------|------------------------------|--------|
| UAB · Universitat Autònoma de Barcelona *(co-fundadora, 2023)* | **Banca/Seguros**: Banco Sabadell · La Caixa · Imagin · Adeslas · AXA | **40+ proyectos** desde 2023 |
| CSIC *(colaborador fundacional)* | **Gran consumo**: Coca-Cola · Danone · NAOS · Selena | **6 sectores**: farmacia · salud · banca · instituciones · gran consumo · medios |
| UNESCO AI Governance Working Group | **Mobility**: Ford | **9 verticales** GEORadar con KPIs propietarios cerrados |
| EU AI Act alignment | **Travel**: Iberostar · PortAventura | 1.000.000+ prompts simulados acumulados |
| Repositorios públicos en GitHub: `498AS/docs-geo`, `498AS/ai-overviews-research` | **Health/Pharma**: AstraZeneca · Dexeus Mujer | 9.000.000+ menciones de marca analizadas |
| Papers, no decks | **Energy**: Veolia | 5 LLMs + Google AIO cubiertos: ChatGPT · Claude · Gemini · Perplexity · Copilot · AIO |
| | **Corporate**: Nestlé | |
| | **Media/Institucional**: 3Cat (CCMA) · Generalitat de Catalunya · UE/INTPA · Mataró | |
| | **Educación**: UAB · UVic | |

**Implementación**: títulos de columna Roboto Mono 14 / UPPER / `#37E813`. Items en Hepta Slab 18 / 300 blanco, line-height 1.8. Separadores 1 px charcoal entre columnas. Una sola sección, máxima respiración.

---

## 07 · EQUIPO — *quiénes somos*

> *(eyebrow)*
> **EQUIPO · BARCELONA · DESDE 2023**
>
> *(headline)*
> **Una casa pequeña que trabaja con casas grandes.**
>
> *(body)*
> 498A se fundó en 2023 junto a la Universitat Autònoma de Barcelona y en colaboración con el CSIC. Es la división de I+D en inteligencia artificial del grupo Zoopa, dirigida por Carlos Ortet — Senior Innovation Engineer y uno de los primeros consultores GEO operando en Europa. El equipo es deliberadamente compacto: cada proyecto que entra en 498A lleva un socio del equipo dirigiéndolo de principio a fin. Es la garantía. Es también el límite de cuántos proyectos podemos llevar a la vez.

**Implementación**: foto del equipo (`equipo-innovador-barcelona.webp`, 484 KB ya en assets) en ancho completo, copy a la derecha. Layout 60/40 imagen/texto. Headline Hepta Slab 38 / 300.

---

## 08 · VOCES — *lo que dicen quienes han trabajado con 498A*

Tres testimonios reales, no plantillas. Tratamiento editorial estilo Isomorphic: cada uno ocupa su propia sección, una sola cita por scroll, con la atribución contenida. El tercero queda en inglés deliberadamente — Specialisterne es multinacional y el frame en su idioma original suena auténtico.

### 08 · A — Specialisterne *(cita principal, ancla la tesis)*

> *(eyebrow)*
> **CLIENT VOICE · SPECIALISTERNE · INTERNATIONAL**
>
> *(quote large, italic, en inglés)*
> *"As a multinational specialised in cognitively diverse profiles, we needed frontier solutions that were truly personalised. We don't know of any other consultancy that knows how to work in that thin line between research and applied solutions."*
>
> *(attribution)*
> **DANIEL REYES**
> Specialisterne

> **Por qué esta cita va primera**: literalmente valida la tesis del posicionamiento ("that thin line between research and applied solutions"). El cliente dice en sus palabras lo que la home reclama en las suyas.

### 08 · B — imagin bank *(cita técnica)*

> *(eyebrow)*
> **CLIENT VOICE · IMAGIN BANK · BANCA DIGITAL**
>
> *(quote, italic)*
> *"498A ideó un sistema basado en intención que no creíamos posible y que impulsó nuestra reputación en las app stores durante cuatro años."*
>
> *(attribution)*
> **CHRISTIAN M.**
> imagin bank

### 08 · C — NAOS *(cita estratégica)*

> *(eyebrow)*
> **CLIENT VOICE · NAOS · GRAN CONSUMO**
>
> *(quote, italic)*
> *"498A nos ha abierto las puertas a un escenario de innovación basado en IA realmente aplicado a nuestro negocio."*
>
> *(attribution)*
> **HÉCTOR MENÉNDEZ**
> CEO · NAOS

**Implementación**: cada cita en su propia sección, fondo negro, Hepta Slab italic 48 / 300 / blanco, máx 900 px de ancho. Eyebrow en Roboto Mono UPPER verde brand. Atribución: nombre en Bebas Neue 28 UPPER blanco, empresa+cargo en Roboto 14 muted. **Separación generosa entre las tres** — al menos 120 px verticales — para que cada una respire como un statement independiente.

---

## 09 · CITA DEL FUNDADOR — *la voz interna*

> *(quote large, italic)*
> *"Una organización próspera es la que sabe anticiparse, construir desde la incertidumbre y alinear su progreso con el del mundo que la rodea."*
>
> *(attribution)*
> **CARLOS ORTET**
> Fundador · 498A

**Implementación**: sección dedicada, fondo negro, cita en Hepta Slab italic 48 / 1.2 / 300, ancho máx 900 px, alineada a la izquierda con sangrado editorial (mismo gesto que las Quote L de Isomorphic). Atribución en Bebas Neue 28 UPPER blanco + Roboto 14 muted.

---

## 10 · INVITACIÓN — *CTA final*

> *(eyebrow)*
> **CONTACTO**
>
> *(headline)*
> **Si tu organización tiene una decisión que depende de IA, hablemos.**
>
> *(body)*
> Trabajamos con un número limitado de proyectos cada trimestre para garantizar profundidad. La primera conversación es una llamada de 30 minutos sin compromiso. Si encajamos, lo sabremos al final de esa llamada.
>
> *(CTA primary)*
> [ Hablemos → ]
>
> *(CTA secondary)*
> [ Suscribirme a las perspectivas ]

**Implementación**: bloque hero invertido — fondo negro, copy alineado a la izquierda, CTA grande Roboto 18 / 500 sobre verde brand. Después de este bloque solo queda footer + perspectivas opcional.

---

## 11 · PERSPECTIVAS *(opcional, below the fold)*

> *(eyebrow)*
> **PERSPECTIVAS**
>
> *(section title)*
> **Lo que estamos pensando.**

Grid de 3 cards estilo Isomorphic news block: `PAPER`, `BLOG`, `PODCAST` como tags en verde mono UPPER, título Hepta Slab 28 / 300, meta de fecha + tiempo de lectura en Roboto Mono 12 muted.

**Implementación**: misma estructura que el news grid de isomorphiclabs.com — 3 columnas en desktop, 1 en mobile. Imágenes en aspect ratio 4:3. Border radius 4 px (sistema angular 498A, no los 20 px suaves de Isomorphic — esto distingue las dos marcas a pesar de la estructura común).

---

## 12 · FOOTER

```
498A
Una compañía del grupo Zoopa · Barcelona, España
Co-fundada en 2023 con la UAB y el CSIC
hola@498a.com · +34 ...

CAPACIDADES                  PRODUCTOS                  INVESTIGACIÓN              COMPAÑÍA
Sistemas multiagente         GEORadar                   Gerard (en roadmap)        Sobre 498A
GEO en motores generativos   S.A.M.                     Papers                     Equipo
IA privada                   LEO                        UAB · CSIC                 Contacto
Datasets a medida            DOC                        Perspectivas               Trabaja con nosotros

498 segundos · La distancia entre lo que pasa y lo que vemos.

© 2026 498A. Todos los derechos reservados.
Aviso legal · Política de privacidad · Política de cookies
```

**Implementación**: footer con fondo `#0a0a0a`, 4 columnas en desktop. Logo del grupo Zoopa al lado del logo 498A. **Crítico**: actualizar todo `498AS` → `498A` (la web actual sigue con la marca antigua en footer y en la atribución de Carlos).

---

## Cambios respecto a la web actual

| Hoy en 498a.com | Propuesta |
|------------------|-----------|
| 6 servicios (Estratégica, Agentes, Automatización, Data Science, Governance, GEO) | 4 capacidades (Multiagente, GEO, IA Privada, Datasets) — los otros 3 se reabsorben |
| Tagline inglés "Building Tomorrow's Intelligence" | Tagline castellano *"Anticipar el comportamiento. Construirlo antes de que llegue."* |
| Counters en 0 (bug) | Cifras reales hardcodeadas: **40+ proyectos · 6 sectores · desde 2023** |
| Testimonios con empresas ficticias (QuantumPath, Synapse Labs, Nébula Studio) | **Testimonios reales**: Daniel Reyes (Specialisterne) · Christian M. (imagin bank) · Héctor Menéndez (NAOS) |
| Validación académica genérica ("UB y CSIC") | **Fundación documentada**: 498A creada en 2023 junto a la UAB y en colaboración con el CSIC |
| "© 498AS – BARCELONA" en footer | "© 2026 498A. Una compañía del grupo Zoopa · Barcelona" |
| Carlos Ortet atribuido como *"CEO y founder de 498AS"* | *"CARLOS ORTET · Fundador · 498A"* |
| Sin sección de I+D / dirección estratégica | Sección **05 · INVESTIGACIÓN** dedicada a la simulación social (el bet diferencial) |
| Slogan del 498 enterrado en footer | Slogan del 498 promovido al hero como tesis de la casa |
| Hero indeterminado sobre qué hacéis | Hero específico: AI aplicada + dirección hacia simulación |

---

## Decisiones de voz

**Lo que el copy hace deliberadamente:**

1. **Voz declarativa, no comercial.** Frases cortas, en presente, sin adjetivos vacíos ("innovador", "líder", "disruptivo"). Cuando un servicio promete algo, viene una cifra detrás.
2. **Castellano principal, mono UPPER para metadata.** Los eyebrows en inglés-estilo-LATAM-tech (`CAPABILITY · 01`) se traducen a `CAPACIDAD · 01`. No se mezclan idiomas en el cuerpo del copy.
3. **Cero "innovación".** La palabra está agotada. Se sustituye por verbos concretos: *desplegar, simular, anticipar, construir, decidir*.
4. **Una idea por sección, una sección por scroll.** No hay bloques con tres tarjetas dentro. Cada sección monopoliza la atención por 8–12 segundos.
5. **Slab serif para body, condensada UPPER para headlines.** Es la herencia del design system actual de 498A (Hepta Slab + Bebas Neue). El editorial style de Isomorphic encaja porque comparten la idea de cuerpo en peso 300 y display fuerte para contraste.
6. **Verde brand como subrayado, no como fondo.** En todo el copy, `#37E813` aparece para destacar un verbo, una cifra o un eyebrow. Nunca como bloque grande. Es la regla de oro del color en el sistema.

---

## Próximos pasos

1. ~~**Validación con marca**: confirmar el frame "consultora de IA aplicada con I+D hacia simulación social".~~ ✓ Validado (2026-05-16).
2. ~~**Reescribir testimonios** con clientes reales.~~ ✓ Tres testimonios reales incorporados (Specialisterne, imagin bank, NAOS).
3. **Permiso de uso de los testimonios**: confirmar con Daniel Reyes, Christian M. y Héctor Menéndez que aceptan publicación de sus citas en la home. Es buena práctica aunque sean clientes conocidos.
4. **Logos de clientes**: producir una banda de logos *trusted by* con CaixaBank, Sabadell, Danone, Ford, Inter Miami, LIDL para reforzar la columna "Producción" del bloque PRUEBA. Necesita las marcas en SVG con permiso de uso.
5. **Imágenes adicionales**: el equipo ya tiene `equipo-innovador-barcelona.webp`. Faltan 1-2 imágenes hero documentales (un agente IA visualizado, una simulación, un dataset anotado) — pueden generarse con Imagen 4 si no hay disponibles.
6. **Implementación**: maquetar con los tokens de `498ASdesign/tokens.css` aplicando la estructura editorial de `isomorphicdesign/showcase.html`. El sistema visual existente lo sostiene tal cual.

---

*Borrador: 2026-05-16. Estructura editorial inspirada en isomorphiclabs.com, traducida al tono y sistema visual de 498A. Listo para iteración con el equipo de marca antes de maquetar.*
