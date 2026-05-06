# vida

Sistema personal de organización + aprendizaje-de-errores.

PARA + decisions/lessons/patterns + journal/retros. Markdown + git + Obsidian.

## Estructura

```
vida/
├── _inbox/              Captura cruda. Vacía en weekly review.
├── _meta/               Reglas, templates, schemas, taxonomía.
├── 1-projects/          Objetivo + deadline. Acaba.
├── 2-areas/             Responsabilidad continua. No acaba.
├── 3-resources/         Referencia. Tema de interés.
├── 4-archive/           Inactivo. Re-activable.
├── decisions/           ADRs personales. DEC-YYYY-NNN.
├── lessons/             Errores procesados. LSN-YYYY-NNN.
├── patterns/            Agregadores de lessons recurrentes.
├── retros/              weekly / monthly / quarterly / annual.
├── journal/daily/       Daily notes procesadas.
├── journal/raw/         Stream of consciousness. git-crypt si aplica.
└── failure-cv/          Lista anual cruda de fracasos.
```

## Reglas operativas

Ver `_meta/README.md`. 10 reglas no negociables.

## Cadencia

| Cuándo | Qué | Duración |
|---|---|---|
| Diario PM 21:00 | AAR-light en daily | 5-10 min |
| Domingo 18:00 | Weekly review (GTD) | 30-45 min |
| Último domingo del mes | Monthly review + auditoría areas | 90 min |
| Último domingo del trimestre | Quarterly review (Schlafman) | 3 hrs |
| 28-31 diciembre | Annual review (Ferriss + Bloom) + failure CV | medio día |
| Pre-decisión grande | Decision file + pre-mortem | 15 min |

## Foco actual (mayo 2026)

`1-projects/2026-cerrar-u/` — trika cálculo avanzado + bika base de datos. 8 semanas hasta fin de ciclo. Prioridad #1 absoluta.

## Privacy

Repo privado git. Plain por default. Solo `journal/raw/` con git-crypt si contenido lo requiere.

## Stack

- Markdown plano
- Git + GitHub privado
- Obsidian (opcional, para UI + Dataview)
- Plugins load-bearing: Templater, Periodic Notes, Dataview, Tasks
