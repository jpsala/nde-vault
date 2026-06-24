# Paradigma de confianza y creatividad — Vault

Proyecto para construir un vault Markdown/Obsidian vivo sobre el paso del paradigma de miedo/desconfianza/soledad hacia un paradigma de creatividad, confianza, paz, cuidado y universo/Dios confiable.

Las experiencias cercanas a la muerte (NDEs/ECM) son una fuente privilegiada del corpus, pero ya no son el límite: también pueden incorporarse videos, documentos, entrevistas, libros o charlas no-ECM si aportan evidencia trazable al norte vivencial.

Repositorio público: <https://github.com/jpsala/nde-vault>

## Decisiones iniciales

- El vault Markdown será la fuente canónica.
- Obsidian será la primera interfaz de exploración y curación.
- Cada fuente relevante —ECM o no-ECM— se registrará de forma trazable.
- Cada concepto del nuevo paradigma vivirá en una nota propia con prioridad según su relación con el norte vivencial.
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

Por ahora trabajamos sin interfaz propia. El usuario puede pasar una URL o documento por chat:

```txt
Procesá esta fuente: https://...
```

El agente debe seguir el workflow documentado, crear/actualizar Markdown en el vault y devolver un resumen con conceptos, citas y decisiones pendientes. Si la fuente no es NDE/ECM, debe marcarse explícitamente como tal y justificar su relación con creatividad/confianza/manifestación/creencias/miedo/cuidado.

## Credenciales

Crear un archivo `.env` local con:

```bash
GROQ_API_KEY=...
```

No commitear claves reales.
