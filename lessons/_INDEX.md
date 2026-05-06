# Lessons — índice

Errores procesados. Numerados `LSN-YYYY-NNN`. Append-only post-commit (excepto sección `## Reviews`).

## Cómo funciona

- Lesson nace cuando un error o aprendizaje merece **regla de comportamiento futuro**.
- Sin `governing-belief` y `trigger` no se commitea — no es lesson, es queja.
- Review forzado en `review-after` (típicamente 2-3 meses).
- Si 3+ lessons comparten `pattern` → escalan a `patterns/PAT-...md`.

## Status enum

- `active` — vigente, regla aplica.
- `invalidated` — la creencia regla fue refutada o reemplazada.
- `superseded` — reemplazada por lesson más nueva (referencia en frontmatter).

## Lessons activas

| ID | Fecha | Título | Pattern | Trigger | Review |
|---|---|---|---|---|---|
| LSN-2026-001 | 2026-05-06 | Causa raíz jaladas cálculo: "puedo con todo a la vez" | tiempo-founder-vs-estudiante | Planificación semanal / aceptar nueva responsabilidad | 2026-07-06 |

## Patterns emergentes (3+ lessons)

(Aún ninguno. Cuando aparezca, crear archivo en `patterns/`.)

- `tiempo-founder-vs-estudiante` — 1 lesson hasta hoy. Si emergen 2 más → promover a pattern.

## Dataview (cuando uses Obsidian)

```dataview
TABLE date, title, pattern, status, review-after
FROM "lessons"
WHERE type = "lesson" AND status = "active"
SORT review-after ASC
```
