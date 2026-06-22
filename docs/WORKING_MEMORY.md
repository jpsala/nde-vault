# Working Memory

Estado vivo corto del proyecto. Mantener liviano.

Última actualización manual: 2026-06-22.

## Lectura rápida

| Área | Estado | Abrir primero | Siguiente acción |
| --- | --- | --- | --- |
| Proyecto NDE/ECM Vault | active | `docs/topics/nde-vault.md` | Procesar fuentes con trazabilidad y curaduría humana. |
| Workflow URL a caso | active | `docs/workflow-url-a-caso.md` | Usar para nuevas URLs de YouTube/NDE. |
| Transcripciones | active | `docs/transcription-policy.md` | Preservar raw y crear readable auditable. |
| AOS local | active | `docs/topics/agentic-os-local.md` | Mantener docs livianos, índice y audit. |

## Estado actual

- El proyecto es un vault Markdown/Obsidian para NDE/ECM.
- `vault/` es la fuente canónica de casos, conceptos, patrones, preguntas, fuentes y rutas.
- Se trabaja por ahora sin interfaz propia: chat + archivos Markdown + revisión en Obsidian.
- Conceptos definitivos requieren aprobación humana; el agente puede proponerlos en `vault/05-preguntas/`.
- Transcripciones raw y metadata fuente no deben sobrescribirse.
- AOS fue adoptado localmente el 2026-06-22 como capa mínima/adaptada: core docs, topics/tracks, skills mínimas y scripts de contexto.
- Repositorio Git público: `https://github.com/jpsala/nde-vault`; se evitó reutilizar `jpsala/nde` porque existía como repo privado con contenido viejo.

## Riesgos

- No exponer ni leer `.env` salvo necesidad explícita; `GROQ_API_KEY` es secreto local.
- No tocar `.tmp/`, audios, raw transcripts ni `vault/.obsidian/plugins/` salvo pedido concreto.
- No convertir interpretaciones en afirmaciones absolutas; mantener trazabilidad a citas/timestamps.
- No crear conceptos definitivos sin aprobación humana.

## Próximo paso probable

1. Procesar la próxima URL NDE siguiendo `docs/workflow-url-a-caso.md`.
2. Revisar en Obsidian propuestas de conceptos en `vault/05-preguntas/`.
3. Cuando el flujo se repita, automatizar partes con scripts preservando raw/canónica.

## Comandos de contexto

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```
