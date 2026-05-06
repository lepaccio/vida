# _meta — reglas, templates, schemas

Este folder es el **sistema operativo** del repo. Si algo aquí cambia, todo el repo debe alinearse.

## 10 reglas no-negociables

1. **Captura va a `_inbox/` por default.** Promoción ocurre en weekly review, no en captura.
2. **Lesson sin `governing-belief` no es lesson, es queja.** Required field. Sin esto repites el patrón con táctica nueva (Argyris double-loop).
3. **Lesson sin `trigger` no se va a surfacear nunca.** Required field. El trigger es la condición en la que la lesson debe aparecer en tu memoria operativa (ej: "antes de firmar contrato").
4. **Pattern aparece cuando hay 3+ lessons con el mismo `pattern` tag.** Antes son lessons sueltas. Forzar pattern prematuro = ruido.
5. **Si una lesson no se invalida ni se cumple su `review-after` 2 veces seguidas, sube a pattern o se archiva.** No mantener zombies.
6. **Areas se auditan mensual.** >90 días sin actividad → pasa a `4-archive/areas/`. Re-activable cuando tenga sentido.
7. **Decisions son immutable post-commit.** Solo `status` y notas de review pueden añadirse (append-only en body, sección `## Reviews`).
8. **Frontmatter es validado.** Si introducimos hook, build rojo = no commit. Mientras tanto: revisar manual antes de commitear.
9. **`journal/raw/` es solo para ti, no se procesa.** Lo que importa se promueve a daily procesado o a lesson.
10. **Un cambio de sistema por mes max.** Anti productivity-theater. Si el sistema te frustra: anota en `_inbox/` propuesta, espera próximo monthly review.

## Cuándo crear cada tipo de archivo

| Tipo | Cuándo |
|---|---|
| `_inbox/X.md` | Captura inmediata. No procesado. |
| `journal/daily/YYYY-MM-DD.md` | Cada noche. |
| `lessons/LSN-...md` | Cuando un error/aprendizaje merezca regla futura. Solo si tienes governing-belief + trigger. |
| `decisions/DEC-...md` | Antes de cualquier compromiso > 6 meses o > S/ X significativo. Pre-mortem incluido. |
| `patterns/PAT-...md` | Cuando 3+ lessons comparten raíz. Lo crea el usuario en weekly/monthly review, no en captura. |
| `retros/.../...md` | Según cadencia. Domingo PM (weekly), último domingo mes, etc. |
| `1-projects/<slug>/` | Objetivo + deadline. README.md obligatorio. |
| `2-areas/<area>/` | Solo las 9 listadas. No agregar sin justificación. |
| `3-resources/<topic>.md` | Tema de interés permanente. Notas procesadas (no copy-paste). |

## Areas activas

Las 9 areas viven en `2-areas/`. No agregar más sin pasar por una decision file:

1. `cofoundy/` — rol founder. NO operación cofoundy (esa va en repo cofoundy).
2. `universidad/` — admin/trámites U. Operación curso = `1-projects/2026-cerrar-u/`.
3. `familia/`
4. `amigos-pareja/`
5. `salud-fisica/`
6. `salud-mental/`
7. `finanzas/` — personales. NO finanzas cofoundy/alertrace.
8. `aprendizaje/` — libros, cursos, podcasts procesados.
9. `proposito-valores/` — anchor para annual review (Bloom 7Q).

## Idioma

Español.

## Frontmatter mínimo por tipo

Ver `_meta/templates/`. No expandir frontmatter sin justificación operacional.
