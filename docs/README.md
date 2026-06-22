# Documentación del proyecto

Mapa liviano para agentes y humanos. No reemplaza a `AGENTS.md` ni al vault.

## Regla de lectura liviana

1. `docs/.generated/context-index.md` si existe.
2. `docs/WORKING_MEMORY.md`.
3. `docs/TOPICS.md` para elegir topic/doc.
4. Abrir solo el documento puntual necesario.

Evitar leer transcripciones largas, `.obsidian/plugins/`, `.tmp/`, secretos o vault completo salvo pedido explícito.

## Documentos principales

| Documento | Rol |
| --- | --- |
| `../AGENTS.md` | Reglas críticas para agentes. |
| `PROJECT.md` | Propósito y alcance del proyecto. |
| `WORKING_MEMORY.md` | Estado vivo corto y próximos pasos. |
| `TOPICS.md` | Router de conocimiento. |
| `DEVELOPMENT.md` | Stack, comandos y persistencia. |
| `DECISIONS.md` | Decisiones durables. |
| `OPEN_QUESTIONS.md` | Preguntas abiertas. |
| `project-os.md` | Diseño operativo original del vault NDE. |
| `workflow-url-a-caso.md` | Flujo para transformar URL en caso. |
| `transcription-policy.md` | Política de transcripciones raw/canónica. |
| `canonical-transcript-design.md` | Diseño de transcripción legible y auditable. |
| `operating-modes.md` | Modo actual y futuras interfaces. |
| `commands-for-user.md` | Frases útiles para pedir trabajo. |

## Carpetas

- `docs/topics/`: entradas recuperables por tema.
- `docs/tracks/`: trabajos vivos retomables.
- `docs/skills/`: skills locales portables, si se habilitan en un harness compatible.
- `vault/`: fuente canónica de conocimiento NDE/ECM.
- `scripts/`: automatizaciones locales.
