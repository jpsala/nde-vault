---
id: agentic-os-operations
status: active
kind: how-to
triggers:
  - aos
  - adopt os
  - update os
  - realinear os
  - auditar sistema agentico
  - reparar contexto
primary_refs:
  - AGENTS.md
  - docs/topics/agentic-os-local.md
  - docs/WORKING_MEMORY.md
  - scripts/context-index.ts
  - scripts/agent-context-audit.ts
---

# Operaciones AOS locales

Este proyecto es un downstream AOS local. No es el upstream manager.

## Uso

- `aos-realinear-os`: auditar y reparar drift de la capa agentica local.
- `aos-adopt-os` / `aos-update-os`: solo si se necesita fusionar mejoras AOS preservando reglas NDE/ECM.
- `aos-perfect-os`: compactar ruta caliente, indexar docs y correr audit.

## Guardrails

- No tocar `vault/`, `.env`, `.tmp/`, raw transcripts, producto, datos ni deploy sin confirmación.
- Crear backups antes de reemplazar archivos existentes.
- Fusionar reglas locales; no pisar `AGENTS.md`, `WORKING_MEMORY.md`, `DECISIONS.md`, tracks o topics sin integrar.
- No copiar piezas manager-only de AOS como registry global o decisiones del kit.
- Propagar mejoras upstream solo si aportan como política local liviana; `minimal-implementation`/Ponytail es opcional y no instala paquetes ni dependencias.
- La política de computer use vive en `docs/topics/pi-agentic-os.md`: documentar superficie/fixture/evidencia/ask-before antes de automatizar UI real.

## Checks

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```
