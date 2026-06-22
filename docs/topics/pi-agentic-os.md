---
id: pi-agentic-os
status: active
kind: how-to
triggers:
  - pi
  - pi os
  - slash commands
  - /aos-sync
  - /aos-guardar-sesion
  - /aos-nueva-sesion
  - /aos-gol
  - /aos-orquestar
  - /aos-fanout
  - continuar sesion
primary_refs:
  - .pi/prompts/
  - .pi/extensions/aos-tools.ts
  - .pi/extensions/aos-checkpoint-nudge.ts
  - docs/OS_PLAYBOOK.md
  - scripts/context-index.ts
  - scripts/agent-context-audit.ts
---

# Pi Agentic OS local

Este proyecto incluye el adapter Pi porque JP opera sus repos desde Pi y los comandos conversacionales/slash son parte del valor practico de AOS.

## Regla local

- `.pi/` viaja por defecto en repos de JP salvo razon explicita para omitirlo.
- No contiene secretos; es un shim fino sobre docs/scripts locales.
- `docs/skills/` no aparece como slash por si solo cuando el discovery global esta apagado; los `/aos-*` visibles vienen de `.pi/prompts/` y `.pi/extensions/`.
- Si se agregan o cambian prompts/extensiones, correr `/reload` en Pi y luego `/aos-sync`.

## Comandos clave

| Comando | Uso |
| --- | --- |
| `/aos-help` | Ver comandos AOS locales. |
| `/aos-guardar-sesion` | Persistir valor durable en docs sin transcript. |
| `/aos-nueva-sesion` | Guardar y abrir una sesion limpia con handoff. |
| `/aos-nueva-sesion-con-gol` | Guardar, abrir sesion limpia y arrancar con lote chico. |
| `/aos-sync` | Regenerar index/audit y revisar skills link. |
| `/aos-status audit` | Ver estado operativo y audit. |
| `/aos-gol` | Preparar un `/until-done` acotado cuando se quiera loop revisable. |
| `/aos-orquestar` / `/aos-fanout` | Usar subagentes/threads cuando aporte valor real. |

## Checks

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```
