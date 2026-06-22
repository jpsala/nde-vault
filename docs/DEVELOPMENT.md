# Development

## Stack actual

- Markdown + YAML frontmatter.
- Obsidian como interfaz de exploración/curaduría.
- Scripts locales en `scripts/` cuando el flujo lo justifique.
- Groq/Whisper para transcripción cuando corresponda.
- Bun disponible para scripts AOS de contexto.

## Persistencia

- Fuente canónica de conocimiento: `vault/`.
- Documentación operativa: `docs/`.
- Secretos locales: `.env` o variables de entorno; nunca versionar valores reales.
- Temporales/audio/intermedios: `.tmp/` o `tmp/`, no tratarlos como fuente durable.

## Comandos de contexto

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```

## Guardrails técnicos

- No tocar producto/datos/deploy/runtime externo sin confirmación.
- No leer ni imprimir `.env`.
- No sobrescribir raw transcripts ni metadata fuente.
- No editar `vault/.obsidian/plugins/` salvo pedido explícito.
- Antes de reemplazar reglas o docs existentes, crear backup en `.agentic-os-backups/`.
