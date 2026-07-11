# AGENTS.md

Vault Markdown/Obsidian vivo para construir conocimiento trazable sobre el paso del paradigma de miedo/desconfianza/soledad hacia creatividad, confianza, paz, cuidado y universo/Dios confiable.

Las NDEs/ECM son fuente privilegiada, pero **no el límite del corpus**: también entran videos, documentos, entrevistas, libros, charlas o fuentes no-ECM si aportan evidencia útil al norte vivencial.

## Lectura Inicial

Antes de trabajar en este proyecto, usar ruta liviana:

1. `docs/.generated/context-index.md` si existe.
2. `docs/WORKING_MEMORY.md`.
3. `docs/README.md` solo si hace falta mapa documental.
4. `docs/TOPICS.md` o busqueda por triggers para elegir tema.
5. Topic/doc/vault puntual segun el pedido.

No abrir transcripciones largas, vault completo, `.env`, `.tmp`, `.obsidian/plugins/` ni referencias profundas salvo que el pedido lo requiera.

## Norte del proyecto

Construir un vault Markdown/Obsidian vivo para ayudar a **vivir más en creatividad y confianza**, integrando evidencia trazable sobre manifestación, creencias, miedo, salud, creación, cuidado, Dios/Universo confiable y no-soledad.

El objetivo no es acumular videos ni limitarse a NDEs: es transformar fuentes trazables —ECM/NDE y no-ECM— en conceptos, patrones, rutas y mapas navegables del nuevo paradigma.

## Web, Internet E Instalaciones

- Usar web por defecto cuando evite adivinar (docs oficiales, releases, issues, APIs, errores); no enviar secretos, `.env`, código privado sensible, datos personales ni credenciales.
- Si evidencia online contradice repo/docs/runtime observado, consultar a JP con fuentes e impacto.
- Antes de instalar dependencias, CLIs, paquetes de sistema, herramientas o binarios/scripts remotos, pedir autorización con comando, alcance, razón, riesgos, alternativa, cambios esperados y rollback. `curl | sh` es alto riesgo.

## Principios

1. **Markdown canónico**: Obsidian, sitio, buscador y chat derivan del vault.
2. **Trazabilidad obligatoria**: ideas/síntesis vuelven a casos, citas y timestamps.
3. **Separar fuente de interpretación**: diferenciar dicho textual, tipo de fuente, fenómeno/enseñanza, patrón y lectura paradigmática.
4. **IA propone, humano valida**: conceptos definitivos requieren aprobación explícita.
5. **No dogmatismo**: conclusiones como patrones emergentes, no absolutos.
6. **Preservar originales**: no sobrescribir transcripciones, metadata ni fuentes; separar raw YouTube/Groq/readable.
7. **Citas primero**: responder con referencias cuando sea posible.
8. **Vault habitable**: índices, mapas, rutas, metadata y búsqueda semántica.

## Convenciones del vault

Estructura esperada: `vault/00-inbox`, `01-casos`, `02-conceptos`, `03-patrones`, `04-paradigma`, `05-preguntas`, `06-fuentes`, `07-rutas`, `99-templates`.

Usar frontmatter YAML en notas estructuradas. Preferir slugs estables en minúsculas y sin espacios.

## Pi Vault Mind En NDE

`pi-vault-mind` es ayuda local de recuperación semántica/FTS/grafo sobre `C:/dev/nde/vault`; no reemplaza Markdown versionado ni validación humana. Detalle: `docs/topics/pi-vault-mind.md`. Antes de abrir muchas notas usar `vm_search`/`vm_fts_search`/`vm_query`; watcher/agentes pasivos apagados salvo pedido explícito.

## Reglas de edición

- No tocar producto, datos privados, credenciales, deploy ni runtime externo sin confirmación explícita.
- No modificar `.env`, `.tmp/`, audios, raw transcripts, ni `vault/.obsidian/plugins/` salvo pedido específico.
- No sobrescribir transcripciones originales ni metadata fuente; crear nuevas capas derivadas cuando haga falta.
- No modificar fuera de bloques `AUTO` salvo que la tarea lo requiera explícitamente.
- Si se necesita cambiar una sección manual o crear un concepto definitivo, pedir aprobación si la decisión conceptual es fuerte.
- Para nuevas fuentes no-ECM, registrar explícitamente `tipo_fuente`, `relacion_norte` y si es testimonio, enseñanza, entrevista, documento o síntesis; no forzarla como “experiencia cercana a la muerte”.
- Mantener docs livianos: decisiones durables van en `docs/DECISIONS.md`, estado vivo en `docs/WORKING_MEMORY.md`, temas recuperables en `docs/topics/`.
- Usar `docs/topics/minimal-implementation.md` como política liviana para implementación mínima/Ponytail: opcional, subordinada a AOS y sin instalar dependencias salvo pedido explícito.
- Para `aos-realinear-os` o auditoría/reparación de contexto, usar `docs/topics/agentic-os-operations.md` y limitarse a la capa agentica salvo confirmación.
- Para `aos-cerrar-sesion`, guardar el valor durable en los docs vivos antes de cerrar.
- En Pi, usar los slash locales `/aos-*` para continuidad, sync, status, guardado de sesión, nueva sesión, gol y orquestación; si no aparecen, ejecutar `/reload` y luego `/aos-sync`.
- Archivos de contexto, notas o drafts preexistentes deben quedar integrados, indexados, archivados con estado claro o consultados antes de borrar.

## Secciones automáticas y credenciales

Contenido generado en notas: delimitar con `<!-- AUTO:EVIDENCE:START -->` / `<!-- AUTO:EVIDENCE:END -->`. Groq: usar solo `GROQ_API_KEY` o `.env` ignorado; nunca escribir claves reales en archivos versionables, docs, logs, tests ni respuestas.

## Idioma

El idioma principal del proyecto y del vault será español, salvo fuentes o citas originales en otros idiomas.


## Continuidad Pi

- JP guarda valor durable con `/aos-guardar-sesion`; despues `/aos-continuar [objetivo]` abre una sesion nueva con prompt de continuidad desde docs vivos. Usar `--preview` para revisar antes de enviar.
