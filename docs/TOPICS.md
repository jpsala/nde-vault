# Topics del proyecto

Router liviano de conocimiento. Si un documento no está enlazado acá o desde `docs/README.md`, queda colgado.

## Topics de entrada

| Si el usuario pide o menciona | Abrir primero | Para qué sirve |
| --- | --- | --- |
| NDE, ECM, vault, casos, conceptos, paradigma, Obsidian | `topics/nde-vault.md` | Norte del proyecto, reglas del vault y referencias clave. |
| concepto nuevo, aprobación, fusionar/dividir conceptos | `topics/concept-governance.md` | Gobernanza liviana para conceptos y revisión humana. |
| URL de YouTube, procesar fuente, crear caso | `workflow-url-a-caso.md` | Flujo operativo para transformar una fuente en caso trazable. |
| transcripción, Groq, raw, readable, timestamps | `transcription-policy.md`, `canonical-transcript-design.md` | Política y diseño de transcripciones. |
| modo de trabajo, interfaz futura, automatización | `operating-modes.md` | Cómo trabajar ahora y cuándo automatizar. |
| comandos/frases útiles | `commands-for-user.md` | Cómo pedir trabajo al agente. |
| docs, memoria, índice, audit, AOS local | `topics/agentic-os-local.md` | Mantener la capa agentica local sin pisar memoria del proyecto. |
| Pi, slash commands, `/aos-sync`, `/aos-guardar-sesion`, `/aos-nueva-sesion`, `/aos-gol` | `topics/pi-agentic-os.md`, `OS_PLAYBOOK.md` | Usar el adapter Pi local para aprovechar AOS en conversaciones. |
| realinear os, adopt/update os, reparar contexto | `topics/agentic-os-operations.md` | Operaciones AOS locales preservando reglas NDE/ECM. |

## Documentos raíz

| Documento | Rol |
| --- | --- |
| `../AGENTS.md` | Reglas críticas para agentes. |
| `README.md` | Mapa de documentación. |
| `PROJECT.md` | Propósito y estado del proyecto. |
| `WORKING_MEMORY.md` | Estado vivo y próximos pasos. |
| `DEVELOPMENT.md` | Stack, comandos y persistencia. |
| `DECISIONS.md` | Decisiones durables. |
| `OPEN_QUESTIONS.md` | Preguntas abiertas. |
| `project-os.md` | Diseño operativo original del sistema NDE. |

## Reglas

- Leer poco y abrir referencias profundas solo bajo demanda.
- Mantener `WORKING_MEMORY.md` corto.
- Promover decisiones durables a `DECISIONS.md` o topics.
- No dejar notas de contexto sueltas: integrar, indexar, archivar o preguntar antes de borrar.
