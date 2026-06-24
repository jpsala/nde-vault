---
id: docs-knowledge-system
status: active
kind: how-to
triggers:
  - docs knowledge system
  - guardar sesion
  - documentar sesion
  - working memory
  - decisions
  - tracks
  - context index
primary_refs:
  - docs/WORKING_MEMORY.md
  - docs/DECISIONS.md
  - docs/topics/
  - docs/tracks/
  - docs/.generated/context-index.md
  - scripts/context-index.ts
  - scripts/agent-context-audit.ts
---

# Sistema documental de conocimiento

## Propósito

Mantener el conocimiento durable del proyecto en Markdown versionable, liviano y retomable, sin convertir cada sesión en transcript.

## Rutas de memoria

- `docs/WORKING_MEMORY.md`: estado vivo corto, riesgos, comandos útiles y próximo paso probable.
- `docs/DECISIONS.md`: decisiones durables aprobadas por el usuario o confirmadas conversacionalmente.
- `docs/topics/`: reglas, preferencias, políticas y mapas de contexto reutilizables.
- `docs/tracks/`: trabajos retomables por caso, auditoría o línea de trabajo activa.
- `vault/05-preguntas/`: propuestas conceptuales o preguntas estructuradas antes/después de aprobación.
- `vault/02-conceptos/`: conceptos aprobados con evidencia trazable.

## Guardar Sesion

Cuando el usuario pida guardar sesión, documentar sesión, `aos-checkpoint` o equivalente:

1. Extraer solo valor durable: decisiones, estado vivo, riesgos, archivos relevantes, checks/comandos útiles y próximo paso.
2. Rutear cada memoria al destino correcto:
   - decisiones aprobadas → `docs/DECISIONS.md`;
   - estado vivo y próximos pasos → `docs/WORKING_MEMORY.md`;
   - reglas/preferencias estables → topic en `docs/topics/`;
   - avance de un caso/línea de trabajo → track en `docs/tracks/`;
   - propuestas conceptuales → `vault/05-preguntas/`;
   - conceptos aprobados → `vault/02-conceptos/`.
3. Mantener docs livianos: no transcript, no logs largos, no duplicar toda la conversación.
4. No abrir thread nuevo, no preparar handoff, no pedir `aos-gol` y no compactar salvo pedido explícito.
5. Regenerar `docs/.generated/context-index.md` si cambian topics, tracks, specs, skills, aliases o prompts documentados.
6. Correr `bun scripts/agent-context-audit.ts` si se tocó capa agentica o hay riesgo de drift.
7. Responder con síntesis compacta de qué quedó persistido y cómo seguir.

## Checks

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```
