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

# Corpus trazable — confianza y creatividad

## Uso

Usar este topic para trabajos sobre el corpus del proyecto: fuentes NDE/ECM y no-ECM, casos/unidades de análisis, conceptos, patrones, rutas, Obsidian y trazabilidad.

NDE/ECM sigue siendo un tipo de fuente privilegiada, pero el norte actual del proyecto es más amplio: vivir en creatividad/confianza y salir del paradigma de miedo/desconfianza/soledad.

## Principios operativos

- `vault/` es la fuente canónica.
- Toda síntesis importante debe poder volver a fuentes, casos/unidades, citas y timestamps o ubicaciones equivalentes.
- Separar testimonio literal, fenómeno reportado, patrón, interpretación paradigmática y preguntas abiertas.
- No crear conceptos definitivos sin aprobación humana.
- Preservar raw transcripts y metadata fuente; crear capas derivadas para legibilidad/análisis.
- También se pueden incorporar casos desde fuentes textuales reconocidas (NDERF u otros repositorios conocidos), marcándolas como fuente textual/web y usando `source-notes.md` en lugar de transcript cuando no hay audio/video.
- Se pueden incorporar fuentes no-ECM si aportan al norte vivencial; marcarlas con `tipo_fuente`, `es_ecm: false` y `relacion_norte` para no confundirlas con testimonios NDE.
- En fuentes de video, separar thumbnail del video, foto del experienciador/a y avatar del canal; no usar el avatar del canal como si fuera foto del testimoniante.

## Ruta según pedido

| Pedido | Abrir |
| --- | --- |
| Procesar URL/fuente | `docs/workflow-url-a-caso.md`; si es fuente textual, registrar en `vault/06-fuentes/web/`; si no es ECM, justificar `relacion_norte` |
| Tarjetas visuales de fuente | `docs/workflow-url-a-caso.md`, `vault/06-fuentes/youtube/<video_id>/source-card.md` |
| Transcripción/raw/readable | `docs/transcription-policy.md`, `docs/canonical-transcript-design.md` |
| Modo de trabajo o automatización | `docs/operating-modes.md` |
| Frases útiles del usuario | `docs/commands-for-user.md` |
| Estado vivo | `docs/WORKING_MEMORY.md` |

## Guardrails

- No leer `.env` ni exponer secretos.
- No tocar `.tmp/`, audios, raw transcripts ni `vault/.obsidian/plugins/` salvo pedido explícito.
- No dogmatizar: reportar patrones emergentes, evidencia y tensiones.
