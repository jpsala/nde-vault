# Working Memory

Estado vivo corto del proyecto. Mantener liviano; detalles retomables viven en tracks y topics.

Última actualización manual: 2026-07-01.

## Lectura rápida

| Área | Estado | Abrir primero | Siguiente acción |
| --- | --- | --- | --- |
| Proyecto confianza/creatividad | active | `docs/topics/paradigma-confianza-creatividad.md`, `docs/topics/nde-vault.md`, `docs/tracks/nde-vault-context.md` | Procesar fuentes ECM y no-ECM con trazabilidad hacia el norte vivencial. |
| Workflow URL a caso | active | `docs/workflow-url-a-caso.md` | Usar para nuevas URLs de YouTube/NDE o fuentes no-ECM. |
| Transcripciones | active | `docs/transcription-policy.md` | Preservar raw y crear readable auditable. |
| Prioridades conceptuales | active | `docs/topics/concept-priorities.md`, `docs/topics/paradigma-confianza-creatividad.md` | Integrar manifestación/creencias/confianza/salud/miedo como eje central. |
| Propuestas en observación | active | `docs/tracks/rechequeo-propuestas-observacion-2026-06-29.md` | Rechequear backlog antes de crear conceptos nuevos. |
| AOS local | active | `docs/topics/agentic-os-local.md`, `docs/topics/docs-knowledge-system.md` | Mantener docs livianos, índice y audit. |
| Pi Vault Mind | active/experimental | `AGENTS.md`, `pi-vault-mind.config.json`, `vault/Agent/` | Usar `vm_*` para recuperacion semantica/FTS/grafo sin reemplazar Markdown canonico ni validacion humana. |

## Estado actual

- Vault Markdown/Obsidian público para construir un paradigma de creatividad/confianza/paz/cuidado y universo-Dios confiable. NDE/ECM es fuente privilegiada, pero no exclusiva.
- `vault/` es fuente canónica; toda síntesis debe volver a casos/unidades, citas, timestamps o ubicaciones equivalentes.
- Conceptos definitivos requieren aprobación humana explícita. Trabajo previo/propuestas vive en `docs/tracks/` y `vault/05-preguntas/`.
- Regla operativa desde 2026-06-29: en cada video nuevo, enlazar automáticamente conceptos aprobados cuando el encaje sea seguro; proponer al usuario solo conceptos nuevos, dudosos o cambios fuertes. Listar propuestas nuevas numeradas.
- Casos/unidades procesadas hasta ahora: 0001-0008, unidad 0009 Daniel Shai, casos 0010-0015. Resumen retomable: `docs/tracks/nde-vault-context.md`; tracks puntuales en `docs/tracks/conceptos-*`.
- Conceptos aprobados recientes incluyen `dios-como-presencia-cercana-y-no-punitiva`, `aceptacion-como-no-resistencia`, y conceptos surgidos en 0010-0011 como amor/oración/Jesús/ancla, perdón, llamado y Dios enviando personas/palabras.
- Norte/prioridades: `manifestacion`, `creencias`, `confianza`, `salud`, `miedo`, `creacion`, `dios-como-padre-cercano`, `jesus-como-hermano`, `estamos-siendo-cuidados`. `salud` es eje central ligado a manifestación/confianza/creencias, miedo, cuerpo, coherencia interior, recuperación y cuidado.
- Subconceptos/aliases delicados, incluido `cuerpo-como-senal-de-desalineacion`, quedan en observación; no crear notas separadas ni afirmaciones médicas/culpabilizantes sin conversación.
- Para fuentes textuales usar `source-notes.md`; en videos separar thumbnail, foto del experienciador y avatar del canal.
- Nota técnica durable: si `fetch_content` falla con YouTube por login/Gemini, usar `python -m yt_dlp --remote-components ejs:github`; preferir `python -m yt_dlp` porque el binario `yt-dlp` directo puede fallar por DLL faltante.
- AOS/Pi local activo; repo público: `https://github.com/jpsala/nde-vault`.
- `pi-vault-mind` instalado project-local y configurado para `C:/dev/nde/vault`; colecciones JSONL en `vault/Agent/Collections/`, salidas revisables en `vault/Agent/Inbox/`, índice derivado `.lancedb/` ignorado por git.

## Riesgos

- No exponer ni leer `.env` salvo necesidad explícita; `GROQ_API_KEY` es secreto local.
- No tocar `.tmp/`, audios, raw transcripts ni `vault/.obsidian/plugins/` salvo pedido concreto.
- No convertir interpretaciones en afirmaciones absolutas; mantener trazabilidad a citas/timestamps.
- No crear conceptos definitivos sin aprobación humana.
- Resultados de `pi-vault-mind`/embeddings no son fuente canonica: citar notas/timestamps y reindexar si hay duda de freshness.

## Próximo paso probable

Al procesar nuevos videos/fuentes, usar `docs/workflow-url-a-caso.md`, integrar evidencia segura en conceptos aprobados, y rechequear `docs/tracks/rechequeo-propuestas-observacion-2026-06-29.md` antes de proponer/crear conceptos nuevos. Para exploracion amplia, probar primero `vm_search`/`vm_fts_search` contra el vault y verificar evidencia en Markdown. Posible renombre en observación: `amor-encarnado-como-proposito`.

## Comandos de contexto

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```
- Continuidad Pi 2026-07-04: JP guarda primero con `/aos-guardar-sesion`; luego `/aos-continuar [objetivo]` es el unico comando para abrir sesion nueva con prompt de continuidad desde docs vivos. `--preview` permite revisar antes de enviar.
