# NDE Vault Project

Proyecto para construir un vault Markdown/Obsidian vivo sobre experiencias cercanas a la muerte (NDEs/ECM), con transcripciones, casos, conceptos dinámicos, patrones, rutas de exploración y futuro chat con referencias al corpus.

Repositorio público: <https://github.com/jpsala/nde-vault>

## Decisiones iniciales

- El vault Markdown será la fuente canónica.
- Obsidian será la primera interfaz de exploración y curación.
- Cada video se convertirá en un caso trazable.
- Cada concepto del nuevo paradigma vivirá en una nota propia.
- Las notas de concepto acumularán evidencia de múltiples casos con citas y timestamps.
- Las secciones generadas automáticamente estarán delimitadas con bloques `AUTO`.
- El futuro chat deberá responder desde el corpus con referencias.

## Estructura

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
scripts/
docs/
```

Ver `docs/project-os.md`, `docs/workflow-url-a-caso.md`, `docs/transcription-policy.md`, `docs/canonical-transcript-design.md`, `docs/concept-lifecycle.md`, `docs/DECISIONS.md`, `docs/operating-modes.md` y `AGENTS.md` para las reglas operativas.

## Cómo empezar ahora

Por ahora trabajamos sin interfaz propia. El usuario puede pasar una URL de YouTube por chat:

```txt
Procesá esta NDE: https://www.youtube.com/watch?v=...
```

El agente debe seguir el workflow documentado, crear/actualizar Markdown en el vault y devolver un resumen con conceptos, citas y decisiones pendientes.

## Credenciales

Crear un archivo `.env` local con:

```bash
GROQ_API_KEY=...
```

No commitear claves reales.
