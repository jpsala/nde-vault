---
id: nde-vault
status: active
kind: how-to
triggers:
  - nde
  - ecm
  - vault
  - caso
  - casos
  - conceptos
  - paradigma
  - obsidian
primary_refs:
  - AGENTS.md
  - docs/project-os.md
  - docs/workflow-url-a-caso.md
  - docs/transcription-policy.md
  - docs/canonical-transcript-design.md
  - docs/operating-modes.md
  - vault/
---

# NDE/ECM Vault

## Uso

Usar este topic para trabajos sobre el corpus NDE/ECM, casos, conceptos, patrones, rutas, Obsidian y trazabilidad.

## Principios operativos

- `vault/` es la fuente canónica.
- Toda síntesis importante debe poder volver a casos, citas y timestamps.
- Separar testimonio literal, fenómeno reportado, patrón, interpretación paradigmática y preguntas abiertas.
- No crear conceptos definitivos sin aprobación humana.
- Preservar raw transcripts y metadata fuente; crear capas derivadas para legibilidad/análisis.

## Ruta según pedido

| Pedido | Abrir |
| --- | --- |
| Procesar URL/fuente | `docs/workflow-url-a-caso.md` |
| Transcripción/raw/readable | `docs/transcription-policy.md`, `docs/canonical-transcript-design.md` |
| Modo de trabajo o automatización | `docs/operating-modes.md` |
| Frases útiles del usuario | `docs/commands-for-user.md` |
| Estado vivo | `docs/WORKING_MEMORY.md` |

## Guardrails

- No leer `.env` ni exponer secretos.
- No tocar `.tmp/`, audios, raw transcripts ni `vault/.obsidian/plugins/` salvo pedido explícito.
- No dogmatizar: reportar patrones emergentes, evidencia y tensiones.
