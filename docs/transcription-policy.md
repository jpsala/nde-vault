# Política de transcripciones

## Decisión

Para cada video vamos a separar tres capas:

```txt
1. Original original / raw de YouTube
2. Transcripción Groq raw sin editar
3. Transcripción visible/canónica híbrida
```

La idea central es:

> Preservar siempre los originales, pero mostrar al usuario una versión legible y mejorada que combine el mejor texto posible con timestamps clickeables.

## 1. Original original / raw

Es la transcripción tal como viene de YouTube u otra fuente, sin correcciones editoriales.

Debe preservarse para trazabilidad y auditoría.

Archivos sugeridos:

```txt
vault/06-fuentes/youtube/<video_id>/transcript_youtube_raw.json
vault/06-fuentes/youtube/<video_id>/transcript_youtube_raw.md
```

Reglas:

- no corregir palabras;
- no mejorar puntuación;
- no reordenar;
- no borrar silencios o errores;
- si agregamos block refs de Obsidian, hacerlo en una copia indexada, no en el raw.

## 2. Transcripción Groq sin editar

Es la transcripción hecha por nosotros desde el audio usando Groq/Whisper.

Debe guardarse sin edición manual para poder comparar contra YouTube.

Archivos sugeridos:

```txt
vault/06-fuentes/youtube/<video_id>/transcript_groq_raw.json
vault/06-fuentes/youtube/<video_id>/transcript_groq_raw.md
```

Reglas:

- no mezclar con YouTube;
- preservar salida cruda;
- mantener timestamps si están disponibles;
- registrar modelo y fecha.

## 3. Transcripción visible/canónica híbrida

Es la versión que debe ver el usuario y que debe usar el análisis conceptual por defecto.

Se construye usando Groq como base textual principal y los timestamps de Groq/YouTube como soporte de navegación. La meta es conservar lo mejor de ambos mundos:

- texto limpio y legible;
- timestamps clickeables y suficientemente precisos;
- trazabilidad hacia los raw y el video original.

Archivo sugerido:

```txt
vault/06-fuentes/youtube/<video_id>/transcript_readable.md
```

Reglas:

- debe ser legible;
- puede corregir puntuación, cortes, palabras mal transcritas y nombres;
- debe mantener timestamps y links al video;
- debe poder enlazar cada fragmento importante desde Obsidian;
- debe usar Groq como texto base salvo que YouTube sea claramente mejor en un tramo;
- debe usar YouTube para granularidad fina cuando ayude;
- no debe inventar contenido;
- si hay duda, conservar nota o marcar `(? )` en lugar de afirmar.

## Uso por defecto

- Para auditoría: usar `transcript_youtube_raw.*` y `transcript_groq_raw.*`.
- Para lectura humana: usar `transcript_readable.md`.
- Para extracción de conceptos: usar `transcript_readable.md`, con posibilidad de volver a los raw si una cita es importante.
- Para citas finales: verificar contra raw y/o video cuando la frase sea central.

## Naming recomendado

```txt
metadata.json
transcript_youtube_raw.json
transcript_youtube_raw.md
transcript_youtube_indexed.md        # opcional: YouTube raw con block refs de Obsidian
transcript_groq_raw.json
transcript_groq_raw.md
transcript_readable.md               # versión visible/canónica
transcript_segments.json             # segmentos normalizados para scripts
```

## Regla editorial

La versión visible no reemplaza a los originales. Los originales se preservan; la visible es una edición trazable para lectura, análisis y navegación.
