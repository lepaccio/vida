# CLAUDE.md — contexto vida/

Este repo es el sistema personal de organización + aprendizaje del usuario. NO es un proyecto profesional. NO es código.

> **Si es tu primera vez en este repo: lee primero `_meta/contexto-chat-inicial.md`** — handoff completo del chat que originó el sistema, incluye estado actual del usuario (foco trika cálculo), causa raíz de errores previos, investigación que sustenta el diseño, y acciones pendientes.

## Quién es el usuario

- Estudiante CC entre 3ro y 4to año (Perú).
- Founder de Cofoundy + cofounder de Alertrace.
- Email: info@cofoundy.dev.
- Idioma de operación: español.

## Qué hay aquí

PKM + decision journal + lesson tracker + retros. Modelo: PARA (Forte) + Zettelkasten para aprendizaje + GTD weekly review + lessons-de-errores estilo AAR/Argyris/Black-Box.

## Reglas de operación

Las 10 reglas viven en `_meta/README.md`. Léelas siempre antes de modificar contenido del repo.

Resumen no-exhaustivo:
1. Captura → `_inbox/`. Promoción solo en weekly review.
2. Lesson sin `governing-belief` y `trigger` no se commitea — no es lesson, es queja.
3. Areas se podan mensualmente (>90 días sin actividad → archive).
4. Decisions son append-only post-commit.
5. Frontmatter validado.

## Cómo asistir al usuario

- Default español. Caveman OK si está activo.
- Para decisiones grandes: empuja al usuario a crear archivo en `decisions/` con pre-mortem ANTES de actuar.
- Para errores recientes: empuja a procesar a `lessons/` con governing-belief + trigger explícitos.
- Si emerge patrón (3+ lessons con misma raíz): proponer crear `patterns/PAT-...md`.
- Weekly review domingo: ayuda a procesar `_inbox/`, promover dailies, revisar decisions abiertas.

## Foco actual

`1-projects/2026-cerrar-u/` es prioridad #1 absoluta hasta fin de ciclo (~julio 2026). Cálculo Avanzado en TRIKA. Si jala = suspensión 1 año. No negociar.

## Qué NO hacer

- No crear archivos en areas/ sin razón clara.
- No expandir frontmatter "por si acaso".
- No introducir plugins/scripts nuevos sin que usuario lo pida.
- No reescribir lessons/decisions ya commiteadas (append-only).
- No mezclar contenido operativo de cofoundy o alertrace aquí (esos tienen sus propios repos).

## Schemas

Ver `_meta/schemas/` (cuando existan) o `_meta/templates/` para forma canónica de cada tipo (daily, weekly, lesson, decision).

## Privacy

Repo privado. Si hay contenido sensible (nombres, finanzas, conflictos) ir a `journal/raw/` (futuro git-crypt).
