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
| Declaración de accesibilidad | ⏳ pendiente · auditoría primero | ⏳ pendiente | — | Fix gaps WCAG identificados en playground · audit con axe/Lighthouse · entonces redactar |

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

## Próximos pasos

1. **Recibir versiones CA y EN** de Privacidad y Cookies del equipo legal.
2. **Recibir versión ES** del Aviso legal.
3. **Auditoría de accesibilidad** del playground (axe DevTools + Lighthouse + WAVE). Cerrar gaps WCAG 2.1 AA antes de redactar la Declaración de Accesibilidad (no copiar la legacy; declarar el estado real auditado).
4. **Confirmar dominio target** y propagar a todos los textos.
5. **Reescribir inventario de cookies** cuando el nuevo stack esté en pre-producción.
6. **Validar conformidad** GDPR / LOPDGDD / LSSI-CE / EAA (Accessibility Act) con asesoría legal antes de publicar.

---

*Última actualización: 2026-05-18.*
