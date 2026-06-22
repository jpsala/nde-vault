# Working Memory

Estado vivo corto del proyecto. Mantener liviano.

Última actualización manual: 2026-06-22.

## Lectura rápida

| Área | Estado | Abrir primero | Siguiente acción |
| --- | --- | --- | --- |
| Proyecto NDE/ECM Vault | active | `docs/topics/nde-vault.md` | Procesar fuentes con trazabilidad y curaduría humana. |
| Workflow URL a caso | active | `docs/workflow-url-a-caso.md` | Usar para nuevas URLs de YouTube/NDE. |
| Transcripciones | active | `docs/transcription-policy.md` | Preservar raw y crear readable auditable. |
| Conceptos Caso 0001 | active | `docs/tracks/conceptos-caso-0001-mary-helen-hensley.md` | Seguir con `revision-de-vida-sin-juicio-externo`. |
| AOS local | active | `docs/topics/agentic-os-local.md` | Mantener docs livianos, índice y audit. |

## Estado actual

- El proyecto es un vault Markdown/Obsidian para NDE/ECM.
- `vault/` es la fuente canónica de casos, conceptos, patrones, preguntas, fuentes y rutas.
- Se trabaja por ahora sin interfaz propia: chat + archivos Markdown + revisión en Obsidian.
- Conceptos definitivos requieren aprobación humana; el agente los trabaja conversacionalmente en `docs/tracks/` y solo crea notas definitivas tras aprobación.
- Conceptos aprobados: `identidad-mas-alla-del-cuerpo`, `muerte-como-transicion` y `percepcion-extracorporal-de-la-realidad-fisica`.
- `cuerpo-como-vehiculo`, `ausencia-de-miedo-a-la-muerte` y `elementos-verificables` quedan como subconceptos/aliases por ahora, no como notas separadas.
- Transcripciones raw y metadata fuente no deben sobrescribirse.
- AOS fue adoptado localmente el 2026-06-22 como capa mínima/adaptada: core docs, topics/tracks, skills mínimas y scripts de contexto.
- Repositorio Git público: `https://github.com/jpsala/nde-vault`; se evitó reutilizar `jpsala/nde` porque existía como repo privado con contenido viejo.
- Adapter Pi `.pi/` agregado por defecto para aprovechar AOS conversacional en repos de JP: `/aos-guardar-sesion`, `/aos-nueva-sesion`, `/aos-sync`, `/aos-gol`, `/aos-orquestar` y `/aos-fanout`.

## Riesgos

- No exponer ni leer `.env` salvo necesidad explícita; `GROQ_API_KEY` es secreto local.
- No tocar `.tmp/`, audios, raw transcripts ni `vault/.obsidian/plugins/` salvo pedido concreto.
- No convertir interpretaciones en afirmaciones absolutas; mantener trazabilidad a citas/timestamps.
- No crear conceptos definitivos sin aprobación humana.

## Próximo paso probable

1. Seguir la conversación conceptual del Caso 0001 con `revision-de-vida-sin-juicio-externo`.
2. Procesar próximas URL NDE siguiendo `docs/workflow-url-a-caso.md`.
3. Cuando el flujo se repita, automatizar partes con scripts preservando raw/canónica y tracks conceptuales.

## Comandos de contexto

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```
