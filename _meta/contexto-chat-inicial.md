---
type: context-handoff
created: 2026-05-06
purpose: "Contexto completo del chat que originó este repo. Para que cualquier agente Claude que arranque en /vida tenga el background sin re-derivar."
---

# Contexto chat inicial — bootstrap del repo `vida/`

Este archivo es el handoff completo del chat de creación. Léelo si arrancas una nueva sesión Claude en este repo y necesitas saber **por qué** existe lo que existe.

---

## 1. Quién es el usuario

- Estudiante CC (Ciencia de la Computación) entre 3ro y 4to año, Perú.
- Founder de Cofoundy (`/home/lepaccio/Escritorio/cofoundy/` y plugin/repos asociados).
- Cofounder de Alertrace (`/home/lepaccio/Escritorio/proyectos/alertrace estrategia/`).
- Email: info@cofoundy.dev.
- Idioma de operación: español. Trabaja con Claude Code (Opus 4.7).
- Modo de comunicación preferido: caveman (respuestas comprimidas). Está activo por sessionStart hook.

## 2. Por qué existe este repo

El usuario tenía repo de Alertrace con estructura PARA + ADRs + frontmatter validado. Pidió replicar el patrón para "toda su vida" — incluyendo aprendizaje de errores en distintas áreas.

Hipótesis original del usuario: PARA + `lessons/` + `journal/` + `retros/`.

Antes de construir, se hizo investigación profunda que validó/ajustó la hipótesis. La investigación está sintetizada en este archivo (sección 4) y el sistema final refleja sus conclusiones.

## 3. Estado actual del usuario al momento de bootstrap (mayo 2026)

### Universidad — ALERTA ROJA

- **Cálculo Avanzado (3ro)**: 3ra matrícula → **TRIKA**. Si jala = suspensión 1 año en su U.
- **Base de Datos (4to)**: 2da matrícula → BIKA.
- Semana 8 del ciclo (~16 semanas total). Quedan ~8 sem + parciales/finales.
- Modalidad: presencial.
- Horarios cálculo: Martes 8-10, Jueves 8-10, Sábado 8-10 teoría, Sábado 14-16 práctica.
- Commute: 3h cada ida (presumido round-trip; aclarar con usuario si dudas).
- Tiempo estudio disponible declarado: **8h/semana** fuera de clases.
- **Sin tutor / sin asesoría / sin grupo de estudio** (gap táctico crítico identificado).
- Pre-requisito formal: ninguno reportado, pero algoritmos sí pega para BD.

### Causa raíz autoreportada de las 2 jaladas previas en cálculo

Marcó honestamente:
- (a) No estudié suficiente / procrastinación
- (f) Cofoundy/alertrace consumieron tiempo
- (h) No asistí a clases
- (i) Mix

**Governing belief refutado** (Argyris double-loop): "puedo cargar cofoundy + alertrace + estudios a full intensidad simultáneamente". Refutado 2 veces. Trika = costo de seguir creyéndolo.

### Estado emocional

Entró al chat "cagado por la u". Reformulación operativa: trika = emergencia justificada, no ansiedad genérica. Stakes reales.

## 4. Investigación que sustenta el sistema

(Síntesis ultra-comprimida. Sources listados al final del archivo.)

### Sistemas PKM revisados
- PARA (Forte) — base. Falla: areas crece sin límite, P↔A confusión.
- Zettelkasten (Luhmann/Ahrens) — para aprendizaje profundo. Over-engineered para vida.
- Johnny.Decimal — límite duro útil, pero rígido.
- LYT/MOCs (Milo) — anti-olvido vía índices vivos.
- BuJo — monthly migration ritual.
- GTD (Allen) — weekly review = "critical success factor".

**Conclusión**: ningún sistema solo cubre. Composición: PARA esqueleto + Zettelkasten en `3-resources/aprendizaje/` + GTD weekly review + LYT MOCs en `_INDEX.md` + BuJo monthly poda areas.

### Frameworks aprendizaje-de-errores
- AAR (US Army) — 4 preguntas: qué se suponía / qué pasó / por qué / qué cambio.
- Pre-mortem (Klein) — imaginar que decisión falló, escribir por qué.
- Double-loop learning (Argyris) — cuestionar governing variables, no solo táctica.
- Black Box Thinking (Syed) — error como dato, no fallo moral.
- Failure CV (Haushofer) — registro anual de fracasos.
- Decision Journal (Kahneman/Parrish) — 8 campos canónicos, especificidad probabilística.

**Conclusión**: lesson sin `governing-belief` y `trigger` no es lesson, es queja. Decisions con pre-mortem obligatorio. Pattern emerge cuando 3+ lessons comparten raíz — pieza ausente del enfoque naive.

### Anti-patterns documentados que el sistema mitiga
- Collector's fallacy → resources requiere procesamiento.
- Areas crece infinito → poda mensual >90 días.
- Lessons nunca relidas → Dataview `_INDEX.md` + `review-after`.
- Frontmatter pesado → schemas mínimos.
- Productivity theater → 1 cambio sistema/mes max.

### Cadencia
- Diario PM: AAR-light en `journal/daily/`.
- Semanal: GTD weekly review domingo (no negociable).
- Mensual: BuJo migration + auditoría areas.
- Trimestral: Schlafman start/stop/continue.
- Anual: Ferriss past-year + Bloom 7 preguntas + failure-cv.

### Plugins Obsidian load-bearing (4)
Templater, Periodic Notes, Dataview, Tasks. Resto = ruido inicial.

### Privacy
Plain por default. `journal/raw/` con git-crypt si emerge contenido sensible. No encriptación prematura.

## 5. Decisiones de diseño tomadas en el chat

Tres ajustes a la hipótesis original del usuario:
1. **`decisions/` afuera de PARA** — régimen de revisión propio, no se pierde en areas.
2. **`_meta/` añadido** — schemas, templates, taxonomy, reglas. Sin esto el sistema deriva.
3. **`patterns/` añadido** — agregador de lessons recurrentes. Sin esto repites el patrón con táctica nueva.

Áreas decididas (9):
- cofoundy, universidad, familia, amigos-pareja, salud-fisica, salud-mental, finanzas, aprendizaje, proposito-valores.

Áreas que faltaban en la lista del usuario (que solo nombró 5 — cofoundy/u/familia/estado-fisico/alertrace):
- Faltaron: finanzas, salud-mental separada de física, aprendizaje, amigos-pareja, propósito-valores.
- Alertrace NO es área porque tiene repo propio. Aquí solo `3-resources/alertrace-link.md` con regla de no-duplicar.

## 6. Lo que se construyó (state del repo al commit inicial)

```
vida/  (git main, commit 7e292b1)
├── README.md
├── CLAUDE.md  ← reglas para agentes
├── .gitignore
├── _meta/
│   ├── README.md  ← 10 reglas no-negociables
│   ├── tags.md
│   ├── templates/{daily, weekly-review, lesson, decision}.md
│   └── schemas/  (vacío, futuro)
├── _inbox/
├── 1-projects/2026-cerrar-u/  ← POBLADO
│   ├── README.md         (plan macro 8 sem)
│   ├── calculo-avanzado.md  (plan táctico trika)
│   └── base-datos.md     (plan bika)
├── 2-areas/  (9 carpetas con .gitkeep, sin contenido aún)
├── 3-resources/alertrace-link.md
├── 4-archive/
├── decisions/
│   ├── _INDEX.md
│   └── DEC-2026-001-priorizar-trika-vs-cofoundy.md  ← FIRMADA
├── lessons/
│   ├── _INDEX.md
│   └── LSN-2026-001-causa-raiz-jaladas-calculo.md  ← FIRMADA
├── patterns/
├── retros/{weekly, monthly, quarterly, annual}/
├── journal/{daily, raw}/
└── failure-cv/
```

## 7. Acciones pendientes (orden importa)

### Operativo trika — ESTA SEMANA (W8)
1. Confirmar regla exacta de TRIKA en su U (leer reglamento).
2. Conseguir tutor cálculo — deadline viernes 9 mayo.
3. Llenar lista temas perdidos en `calculo-avanzado.md` con sílabo del curso.
4. Comunicar a equipos cofoundy + alertrace: 8 semanas modo mantenimiento.
5. Bloquear horarios estudio en calendario (inmovibles).

### Sistema vida
6. Primera entrada `journal/daily/2026-05-06.md` esta noche (PM).
7. Primer weekly review domingo 2026-05-10 → `retros/weekly/2026/W19.md`.

### Pendiente confirmación del usuario (al cierre del chat)
8. **GitHub privado**: el usuario quiere repo + git. Git local listo. Falta crear remote y push:
   ```
   cd ~/Escritorio/vida && gh repo create vida --private --source=. --push
   ```
   Pidió que se creara — confirmar al inicio si aún aplica.
9. **Obsidian config**: vault + plugins (Templater, Periodic Notes, Dataview, Tasks). Pendiente.

## 8. Restricciones operativas claves para asistir

- Cálculo > BD > todo lo demás durante 8 semanas. No relaxar bajo ninguna excusa estándar.
- Cofoundy/alertrace en mantenimiento. Si usuario plantea expandir scope ahí: recordar DEC-2026-001 antes de avanzar.
- Cualquier nueva responsabilidad cofoundy/alertrace/voluntariado debe pasar por LSN-2026-001 trigger ("no aceptar nuevas responsabilidades sin horas de estudio honradas las últimas 2 semanas").
- Lessons/decisions = append-only post-commit. Solo `## Reviews` admite nuevas entradas con fecha.
- Frontmatter no expande sin justificación operacional.
- Un cambio de sistema por mes max.

## 9. Tono y modo de asistir

- Idioma: español.
- Caveman OK si el hook está activo. Ver `~/.claude/plugins/cache/caveman/`.
- Para decisiones grandes: empujar al usuario a crear `decisions/DEC-...md` con pre-mortem ANTES de actuar.
- Para errores recientes: empujar a procesar a `lessons/LSN-...md` con governing-belief + trigger.
- Si emerge patrón (3+ lessons con misma raíz): proponer `patterns/PAT-...md`.
- Weekly review domingo: ayuda a procesar `_inbox/`, promover dailies, revisar decisions abiertas.
- No mezclar contenido operativo cofoundy/alertrace aquí. Esos tienen sus repos.

## 10. Repos relacionados del ecosistema usuario

- `/home/lepaccio/Escritorio/Percy/` — workspace base
- `/home/lepaccio/Escritorio/cofoundy/` — Cofoundy
- `/home/lepaccio/Escritorio/cofoundy-toolkit/` — toolkit/skills
- `/home/lepaccio/Escritorio/proyectos/alertrace estrategia/` — Alertrace (modelo PARA/ADR del que se replicó este sistema)

---

## Sources de la investigación (referencia rápida)

- Forte Labs — PARA original + Hot or Cold method
- Sönke Ahrens — How to Take Smart Notes (con críticas Zettelkasten Forum)
- Andy Matuschak — notas evergreen
- Cody Burleson — Patterns for PKM: Johnny Decimal
- Nick Milo — Linking Your Thinking
- FM 7-0 Appendix K — After Action Reviews (US Army)
- Wharton Executive Education — AAR usage
- Gary Klein — Premortem (HBR 2007)
- Argyris & Schön — Theories of Action / Double-Loop Learning
- Matthew Syed — Black Box Thinking
- Johannes Haushofer — CV of Failures
- Farnam Street (Shane Parrish) — Decision Journal
- David Allen — GTD Weekly Review Checklist
- Ness Labs / Stubblebine — Interstitial Journaling
- Tim Ferriss — Past Year Review
- Sahil Bloom — Personal Annual Review (7 preguntas)
- Steve Schlafman — Quarterly Review
- Obsidian docs — YAML frontmatter
- AGWA — git-crypt
- Tiago Forte — Building a Second Brain (CODE: Capture/Organize/Distill/Express)

(Si necesitas profundizar en alguna, pídelo y se vuelve a buscar.)
