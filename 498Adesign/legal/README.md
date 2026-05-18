# Legal · 498 Advance

Carpeta canónica de los textos legales de la nueva web 498A. Cada documento existe en 2 formatos:

- `*.md` — markdown source con frontmatter YAML (canonical · fuente de verdad)
- `*.html` — página renderizada usando los tokens del design system v2.1

Las dos versiones contienen el mismo texto; la HTML añade selector de idioma sticky, navegación, footer y estilos editoriales.

---

## Estado

| Documento | Markdown | HTML | Idiomas |
|-----------|----------|------|---------|
| Aviso legal | ✅ `aviso-legal.md` | ✅ `aviso-legal.html` | CA · EN · ES (pendiente) |
| Política de privacidad | ⏳ pendiente | ⏳ pendiente | — |
| Política de cookies | ⏳ pendiente · gestor UI ya implementado en playground | ⏳ pendiente | — |
| Declaración de accesibilidad | ⏳ pendiente | ⏳ pendiente | — |

---

## Datos canónicos de la entidad legal

| Campo | Valor |
|-------|-------|
| Razón social | 498 Advanced Solutions SL |
| CIF | B64519622 |
| Domicilio | Calle Doctor Trueta, 158 · 08005 Barcelona · España |
| Email contacto | info@498as.com |
| Dominio legacy | www.498as.com |
| Dominio target post-rebrand | pendiente confirmación |

> **Nota de transición**: el texto recibido del equipo legal referencia `498AS` y `www.498as.com` (legacy). El rebrand 498AS → 498A está en curso. La razón social y CIF no cambian. El dominio público y el branding visual pasan a 498 Advance · 498a tras el cierre del rebrand. Antes de publicar en producción, validar con legal que se actualicen referencias de URL y branding en el texto.

---

## Cómo se enlaza desde el resto del sistema

- `playground.html` footer · 4 links legales (`Aviso legal`, `Política de privacidad`, `Política de cookies`, `Declaración de accesibilidad`).
- `Aviso legal` apunta a `legal/aviso-legal.html` con anclas por idioma (`#ca`, `#es`, `#en`).
- `Política de cookies` abre el modal de gestión de consent (no es página legal todavía; el documento de policy en sí está pendiente).

---

## Próximos pasos

1. **Recibir versión castellana** del Aviso legal del equipo legal.
2. **Recibir** Política de privacidad, Política de cookies (texto completo), Declaración de accesibilidad.
3. **Revisar** referencias `498AS` / `498as.com` en el texto cuando el rebrand cierre.
4. **Validar conformidad** GDPR / LOPDGDD / LSSI-CE / EAA (Accessibility Act) con asesoría legal.

---

*Última actualización: 2026-05-18.*
