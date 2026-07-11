---
id: agentic-os-local
status: active
kind: how-to
triggers:
  - aos
  - agentic os
  - memoria
  - working memory
  - topics
  - audit
  - context index
  - guardar sesion
  - alinear os
primary_refs:
  - AGENTS.md
  - docs/WORKING_MEMORY.md
  - docs/TOPICS.md
  - docs/.generated/context-index.md
  - docs/topics/docs-knowledge-system.md
  - scripts/context-index.ts
  - scripts/agent-context-audit.ts
---

# Agentic OS local

## Propósito

Mantener una capa agentica mínima y local para este proyecto sin convertirlo en el upstream manager de AOS.

## Reglas

- Preservar reglas y memoria local del proyecto NDE/ECM.
- No copiar registry global, decisiones históricas del kit AOS ni tracks manager-only.
- Mantener ruta caliente liviana: `AGENTS.md`, `docs/.generated/context-index.md`, `docs/WORKING_MEMORY.md`, `docs/TOPICS.md`.
- Usar `docs/topics/docs-knowledge-system.md` como fuente canónica para ruteo documental y guardado de sesión.
- Usar `docs/topics/minimal-implementation.md` para revisiones de implementación mínima/Ponytail solo como modo opcional subordinado a AOS.
- Promover decisiones durables a `docs/DECISIONS.md` y estado vivo a `docs/WORKING_MEMORY.md`.
- No dejar archivos de contexto sueltos: integrar, indexar, archivar o preguntar antes de borrar.
- Crear backups antes de reemplazar archivos existentes.

## Checks

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```

## Capas locales

- Core docs: `docs/README.md`, `PROJECT.md`, `WORKING_MEMORY.md`, `TOPICS.md`, `DEVELOPMENT.md`, `DECISIONS.md`, `OPEN_QUESTIONS.md`.
- Topics locales en `docs/topics/`.
- Tracks en `docs/tracks/` para trabajos retomables.
- La skill específica `aos-gol-lite` en `docs/skills/` si el harness la usa; las skills AOS portables se resuelven desde `C:/dev/os/docs/skills/`.
- Scripts de contexto en `scripts/`.
