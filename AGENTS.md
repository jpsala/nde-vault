# AGENTS.md

Este repo es un vault Markdown/Obsidian vivo para construir conocimiento trazable sobre el paso del paradigma de miedo/desconfianza/soledad hacia un paradigma de creatividad, confianza, paz, cuidado y universo/Dios confiable.

Las Near Death Experiences (NDEs/ECM) siguen siendo una fuente privilegiada porque muchas personas relatan haber recordado el “hogar” o una realidad más amplia, pero **ya no son el límite del corpus**. También pueden incorporarse videos, documentos, entrevistas, libros, charlas o fuentes no-ECM si aportan evidencia útil al norte vivencial del proyecto.

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

## Principios

1. **Markdown como fuente canónica**: el vault Markdown es la base primaria del conocimiento. Obsidian, sitio web, buscador y chat deben derivar de esa misma fuente.
2. **Trazabilidad obligatoria**: toda idea/concepto/síntesis debe poder volver a casos concretos, citas y timestamps del video original.
3. **Separar fuente de interpretación**: distinguir siempre entre lo que la fuente/persona dijo, el tipo de fuente, el fenómeno o enseñanza reportada, el patrón acumulado y la lectura paradigmática.
4. **IA propone, humano valida**: las secciones automáticas pueden actualizar evidencia y síntesis, pero los conceptos nuevos requieren aprobación explícita del usuario antes de crear una nota conceptual definitiva.
5. **No dogmatismo**: formular conclusiones como patrones emergentes desde el corpus, no como afirmaciones absolutas.
6. **Preservar originales**: transcripciones originales, metadata y fuentes no deben sobrescribirse. Mantener separadas la transcripción raw de YouTube, la raw de Groq y la versión visible/canónica mejorada.
7. **Citas primero**: el chat y las síntesis deben responder con referencias cuando sea posible.
8. **Vault habitable**: proveer índices, mapas, rutas guiadas, metadata y búsqueda semántica para que el usuario no tenga que conocer todo el vault.

## Convenciones del vault

Estructura inicial esperada:

```txt
vault/
  00-inbox/
  01-casos/
  02-conceptos/
  03-patrones/
  04-paradigma/
  05-preguntas/
  06-fuentes/
  07-rutas/
  99-templates/
```

Usar frontmatter YAML en notas estructuradas. Preferir slugs estables en minúsculas y sin espacios para IDs internos.

## Reglas de edición

- No tocar producto, datos privados, credenciales, deploy ni runtime externo sin confirmación explícita.
- No modificar `.env`, `.tmp/`, audios, raw transcripts, ni `vault/.obsidian/plugins/` salvo pedido específico.
- No sobrescribir transcripciones originales ni metadata fuente; crear nuevas capas derivadas cuando haga falta.
- No modificar fuera de bloques `AUTO` salvo que la tarea lo requiera explícitamente.
- Si se necesita cambiar una sección manual o crear un concepto definitivo, pedir aprobación si la decisión conceptual es fuerte.
- Para nuevas fuentes no-ECM, registrar explícitamente `tipo_fuente`, `relacion_norte` y si es testimonio, enseñanza, entrevista, documento o síntesis; no forzarla como “experiencia cercana a la muerte”.
- Mantener docs livianos: decisiones durables van en `docs/DECISIONS.md`, estado vivo en `docs/WORKING_MEMORY.md`, temas recuperables en `docs/topics/`.
- Para `aos-realinear-os` o auditoría/reparación de contexto, usar `docs/topics/agentic-os-operations.md` y limitarse a la capa agentica salvo confirmación.
- En Pi, usar los slash locales `/aos-*` para continuidad, sync, status, guardado de sesión, nueva sesión, gol y orquestación; si no aparecen, ejecutar `/reload` y luego `/aos-sync`.
- Archivos de contexto, notas o drafts preexistentes deben quedar integrados, indexados, archivados con estado claro o consultados antes de borrar.

## Secciones automáticas

Cuando una nota tenga contenido generado o actualizado por scripts/agentes, delimitarlo así:

```md
<!-- AUTO:EVIDENCE:START -->
...
<!-- AUTO:EVIDENCE:END -->
```

## Groq / credenciales

La API key de Groq debe manejarse exclusivamente como secreto local mediante variable de entorno `GROQ_API_KEY` o archivo `.env` ignorado por git.

Nunca escribir claves reales en archivos versionables, documentación, logs, tests o respuestas finales.

## Idioma

El idioma principal del proyecto y del vault será español, salvo fuentes o citas originales en otros idiomas.
