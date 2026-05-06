# Decisions — índice

ADRs personales. Numerados `DEC-YYYY-NNN`. Append-only post-commit.

## Cómo funciona

- Decisión grande (>6 meses impacto, >S/X, irreversible o costosa de revertir) → archivo nuevo.
- Pre-mortem incluido (Klein).
- Review programado en `review-date`. Append en sección `## Reviews`.
- Si genera lesson tras outcome → linkear `related-lessons:` y crear `LSN-...md`.

## Status enum

- `open` — todavía no se manifiesta el outcome.
- `resolved-as-expected` — outcome ≈ probabilidad esperada.
- `resolved-better` — mejor de lo esperado.
- `resolved-worse` — peor. Generar lesson casi seguro.
- `superseded` — reemplazada por decisión posterior.

## Decisions activas

| ID | Fecha | Título | Status | Review |
|---|---|---|---|---|
| DEC-2026-001 | 2026-05-06 | Priorizar trika cálculo sobre cofoundy + alertrace 8 sem | open | 2026-08-06 |

## Cuando uses Obsidian + Dataview

Reemplazar la tabla manual con:

```dataview
TABLE date, title, status, review-date
FROM "decisions"
WHERE type = "decision" AND status = "open"
SORT review-date ASC
```
