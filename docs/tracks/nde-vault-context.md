---
status: active
started: 2026-06-22
updated: 2026-06-22
priority: high
related:
  - docs/topics/nde-vault.md
  - docs/topics/agentic-os-local.md
  - docs/workflow-url-a-caso.md
  - docs/transcription-policy.md
---

# NDE Vault Context

## Objetivo

Mantener el proyecto NDE/ECM retomable para agentes: reglas claras, memoria viva corta, docs indexados y checks de contexto.

## Estado actual

- AOS local adoptado como capa mínima/adaptada el 2026-06-22.
- Se preservaron reglas locales de `AGENTS.md`, `README.md` y docs existentes.
- No se tocó `vault/`, `.env`, `.tmp/`, producto, datos ni deploy.
- Backups de adopción/alineación en `.agentic-os-backups/2026-06-22-align-os/`.

## Próximo paso

Procesar próximas fuentes NDE usando `docs/workflow-url-a-caso.md` y actualizar conceptos solo con aprobación humana cuando sean definitivos.

## Evidencia / Source Refs

- `bun scripts/context-index.ts`
- `bun scripts/agent-context-audit.ts`
