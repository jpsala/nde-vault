# Project OS — NDE/ECM Vault

## Propósito

Crear un sistema de investigación, navegación y conversación sobre experiencias cercanas a la muerte, construido desde testimonios acumulados y trazables.

El sistema debe ayudar a explorar un nuevo paradigma sobre conciencia, muerte, existencia, realidad material, identidad, amor, propósito y transformación.

## Decisiones tomadas

### 1. Vault Markdown como base

El proyecto será primero un vault Markdown compatible con Obsidian.

El vault no será solo una visualización: será la fuente canónica del conocimiento.

### 2. Obsidian como primera interfaz

Obsidian se usará para:

- explorar notas;
- navegar backlinks;
- visualizar grafos;
- curar conceptos;
- usar mapas de contenido;
- eventualmente usar Dataview/Bases para vistas dinámicas.

### 3. Casos derivados de videos

Cada URL de YouTube procesada debe generar un caso con:

- metadata;
- transcripción original preservada;
- transcripción Groq preservada cuando se use;
- transcripción visible/canónica mejorada para lectura y análisis;
- resumen;
- conceptos detectados;
- citas con timestamps;
- vínculos a notas de conceptos.

Ver `docs/transcription-policy.md` y `docs/canonical-transcript-design.md`.

### 4. Conceptos vivos

Cada concepto del nuevo paradigma tendrá una nota propia.

Ejemplos:

- `[[El universo material como constructo]]`
- `[[Conciencia no local]]`
- `[[Muerte como transición]]`
- `[[Amor como estructura de la realidad]]`
- `[[La realidad más real que esta realidad]]`

Cada concepto debe crecer acumulando evidencia de múltiples casos.

### 5. Partes humanas y partes automáticas

Las notas deben separar:

- texto curado/manual;
- evidencia agregada automáticamente;
- síntesis acumulada generada/propuesta por IA.

Formato:

```md
<!-- AUTO:EVIDENCE:START -->
...
<!-- AUTO:EVIDENCE:END -->
```

### 6. Referencias a timestamps

Toda cita relevante debe enlazar al momento del video cuando sea posible:

```md
[00:14:32](https://youtube.com/watch?v=VIDEO_ID&t=872)
```

### 7. Capas de análisis

Separar siempre:

1. testimonio literal;
2. fenómeno reportado;
3. patrón entre casos;
4. implicación paradigmática;
5. preguntas abiertas;
6. explicaciones alternativas o tensiones cuando correspondan.

### 8. Navegación para vault grande

Como el vault crecerá mucho, necesitaremos:

- mapas de contenido;
- rutas guiadas;
- dashboards;
- metadata YAML;
- ontología de relaciones;
- búsqueda textual;
- búsqueda semántica;
- chat RAG con citas;
- sitio web en una etapa posterior.

### 9. Chat futuro

El chat debe actuar como bibliotecario e investigador del corpus.

Debe:

- responder desde el vault;
- citar casos y timestamps;
- sugerir conceptos relacionados;
- guiar al usuario por rutas;
- distinguir corpus, patrón e interpretación.

### 10. Manejo de credenciales

La clave de Groq debe vivir en `.env` o variable de entorno `GROQ_API_KEY`.

No debe aparecer en archivos versionables.

## Arquitectura conceptual

```txt
YouTube URLs
  ↓
Transcripción con Groq/Whisper
  ↓
Transcripción original preservada
  ↓
Caso Markdown
  ↓
Extracción de citas/conceptos
  ↓
Notas de conceptos actualizadas
  ↓
Índices, mapas y rutas
  ↓
Búsqueda semántica + chat
  ↓
Sitio web futuro
```

## Stack inicial recomendado

- Markdown + YAML frontmatter
- Obsidian
- Scripts locales
- Groq para transcripción
- `.env` para secretos
- Futuro: embeddings + búsqueda semántica + RAG

## Criterio de calidad

Una afirmación importante del paradigma solo es útil si puede responder:

> ¿De qué casos, citas y timestamps sale esto?
