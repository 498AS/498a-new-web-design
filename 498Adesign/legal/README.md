# Legal · 498 Advance

Carpeta canónica de los textos legales de la nueva web 498A. Cada documento existe en 2 formatos:

- `*.md` — markdown source con frontmatter YAML (canonical · fuente de verdad)
- `*.html` — página renderizada usando los tokens del design system v2.1

Las dos versiones contienen el mismo texto; la HTML añade selector de idioma sticky, navegación, footer y estilos editoriales.

---

## Estado

| Documento | Markdown | HTML | Idiomas | Pendiente |
|-----------|----------|------|---------|-----------|
| Aviso legal | ✅ `aviso-legal.md` | ✅ `aviso-legal.html` | CA · EN · ES (pendiente) | Versión ES · revisión post-rebrand |
| Política de privacidad | ✅ `politica-privacidad.md` | ✅ `politica-privacidad.html` | ES · CA, EN (pendientes) | Gaps RGPD · versiones CA y EN |
| Política de cookies | ✅ `politica-cookies.md` | ✅ `politica-cookies.html` | ES · CA, EN (pendientes) | Inventario cookies del nuevo stack · versiones CA y EN |
| Declaración de accesibilidad | ✅ `declaracion-accesibilidad.md` | ✅ `declaracion-accesibilidad.html` | ES · CA, EN (pendientes) | Audit externo profesional · axe/Lighthouse en CI · subtítulos vídeo · tests con usuarios de tecnologías de apoyo |

---

## Datos canónicos de la entidad legal

| Campo | Valor |
|-------|-------|
| Razón social | 498 Advanced Solutions SL |
| CIF | B64519622 |
| Domicilio | Calle Doctor Trueta, 158 · 08005 Barcelona · España |
| Email contacto | info@498a.com |
| Email DPO (cookies + RGPD) | protecciondedatos@498a.com |
| Dominio target post-rebrand | www.498a.com (pendiente confirmación final) |

> **Nota de transición aplicada**: el texto recibido del equipo legal usaba la nomenclatura legacy `498AS` y `www.498as.com`. Se ha sustituido por `498A` (nombre comercial post-rebrand) y `www.498a.com` (dominio target). La razón social legal (498 Advanced Solutions SL) y CIF (B64519622) no cambian. Validar con legal: (1) actualización de nombre comercial, (2) dominio final, (3) versiones castellana e inglesa de privacidad/cookies, (4) cierre de gaps RGPD identificados.

---

## Gaps detectados en los textos legacy

### Política de privacidad
El texto legacy es **mínimo** y le faltan elementos que las buenas prácticas RGPD recomiendan:
- Canal específico para ejercer derechos ARSOPL (no está en el doc de privacidad; sí aparece en cookies: `protecciondedatos@498a.com`)
- Referencia explícita a Delegado de Protección de Datos (DPO) si existe
- Referencia a la AEPD como autoridad de control para reclamaciones
- Información sobre transferencias internacionales
- Plazos concretos de conservación por tipo de dato

### Política de cookies
- El inventario de cookies refleja el stack legacy WordPress + Elementor + Complianz + WooCommerce + Stripe. La nueva web **no usará este stack**. Cuando se confirme el stack final (Webflow / WordPress diferente / framework custom), hay que **reescribir entera** la sección "Cookies específicas utilizadas" auditando las cookies reales en producción.
- El consent manager de la nueva web ya está implementado en `playground.html` (banner + modal + `localStorage` con clave `498a.cookie-consent.v1`).

---

## Cómo se enlaza desde el resto del sistema

- `playground.html` footer · 4 links legales:
  - `Aviso legal` → `legal/aviso-legal.html` (anclas `#ca`, `#es`, `#en`)
  - `Política de privacidad` → `legal/politica-privacidad.html`
  - `Política de cookies` → abre el modal de consent (también `legal/politica-cookies.html` para texto largo)
  - `Declaración de accesibilidad` → pendiente
- Cada página legal tiene `legal-nav` con back a `playground.html` y selector de idioma `CA / ES / EN`.

---

## Mejoras de accesibilidad implementadas en el playground v2.1

Como parte del cierre de la Declaración de Accesibilidad, se han aplicado las siguientes mejoras WCAG 2.1 AA:

- **Skip link** "Saltar al contenido principal" (WCAG 2.4.1)
- **`<main>` landmark** envolviendo el contenido principal (WCAG 1.3.1, 2.4.1)
- **`<a>`/`<button>`/`<input>` focus-visible** global con outline verde 2 px + offset 2 px (WCAG 2.4.7)
- **Focus trap** del modal de cookies con devolución de focus al trigger (WCAG 2.4.3)
- **Contraste de texto**: `--pg-text-faint` subido de `#999` a `#717171` (ratio 4.6:1, pasa AA). `.eyebrow` en tokens.css cambiado a verde-deep (`#0E7A1F`, ratio 6.1:1) en lugar de verde primary (`#2DD60F`, fallaba)
- **Typewriter sr-only**: el reveal char-by-char tiene un `<span class="sr-only">` con el texto completo para lectores de pantalla, mientras la animación visual usa `aria-hidden="true"`
- **Touch targets**: `lang-grid` ≥ 44 × 44 px en pantallas táctiles (WCAG 2.5.5)
- **`aria-label`** en el vídeo hero describiendo el contenido visual (WCAG 1.2.5)
- **`prefers-reduced-motion`** respetado en todas las animaciones (WCAG 2.3.3)

## Próximos pasos

1. **Auditoría profesional externa** con entidad certificada (Funka u otra) antes del go-live.
2. **Tests automatizados** con axe DevTools / Lighthouse / WAVE integrados en CI.
3. **Tests con usuarios** de tecnologías de apoyo (NVDA + Firefox, VoiceOver + Safari).
4. **Recibir versiones CA y EN** de Privacidad, Cookies y Accesibilidad del equipo legal.
5. **Recibir versión ES** del Aviso legal.
6. **Confirmar dominio target** (`www.498a.com` provisional) y propagar a todos los textos.
7. **Reescribir inventario de cookies** cuando el nuevo stack esté en pre-producción.
8. **Subtítulos del vídeo hero** cuando se sustituya por contenido productivo.
9. **Validar conformidad** GDPR / LOPDGDD / LSSI-CE / EAA con asesoría legal antes de publicar.
10. **Revisión semestral** de la Declaración de Accesibilidad una vez en producción.

---

*Última actualización: 2026-05-18.*
