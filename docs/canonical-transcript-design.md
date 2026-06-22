# Diseño de transcripción canónica híbrida

## Objetivo

Crear una transcripción visible para el usuario que sea:

- legible;
- fiel al testimonio;
- navegable por timestamps;
- citable desde casos y conceptos;
- auditable contra las fuentes raw.

La versión canónica debe combinar:

```txt
Texto base: Groq/Whisper
Timestamps: Groq + YouTube, priorizando precisión y navegación
Fuente final de verdad: video original
```

## Capas

### 1. YouTube raw

Archivo:

```txt
transcript_youtube_raw.md/json
```

Uso:

- preservar subtítulos automáticos originales;
- tener timestamps finos;
- auditar diferencias;
- rescatar timing granular cuando Groq agrupe demasiado.

No se muestra como lectura principal al usuario.

### 2. Groq raw

Archivo:

```txt
transcript_groq_raw.md/json
```

Uso:

- preservar transcripción propia;
- obtener texto más limpio;
- mejorar puntuación y continuidad;
- comparar contra YouTube.

No se edita manualmente.

### 3. Transcripción canónica / readable

Archivo:

```txt
transcript_readable.md
```

Uso:

- lectura humana;
- análisis conceptual;
- citas en casos;
- links desde notas de conceptos;
- base del futuro buscador/chat.

Debe ser la versión que ve el usuario por defecto.

## Regla de construcción

La canónica debe seguir esta prioridad:

1. **Texto de Groq** como base principal, porque suele tener mejor puntuación y frases más legibles.
2. **Timestamps de Groq** cuando coinciden bien con el contenido.
3. **Timestamps de YouTube** para refinar granularidad cuando Groq agrupa demasiado.
4. **Ajuste manual** para fragmentos conceptualmente importantes.
5. **Video original** como árbitro final si hay conflicto.

## Formato recomendado

```md
[00:07:10](https://youtube.com/watch?v=VIDEO_ID&t=430) When you come up and out of the body, the last thing you're thinking about is that physical form. It's just a vehicle... ^t000710
```

Cada bloque debe tener:

- timestamp visible;
- link a YouTube;
- texto legible;
- block ref de Obsidian (`^tHHMMSS`).

## Timestamps y granularidad

Idealmente, cada bloque debe representar una unidad semántica corta:

- una oración;
- una idea completa;
- o un párrafo breve.

No conviene que los bloques sean demasiado largos, porque los conceptos necesitan enlazar a momentos específicos.

Si Groq genera segmentos largos, se puede:

- dividir el texto por oraciones;
- estimar timestamps intermedios proporcionalmente;
- alinear con timestamps cercanos de YouTube;
- marcar segmentos dudosos para revisión.

## Auditoría

Toda cita importante debe poder rastrearse así:

```txt
Concepto → Caso → transcript_readable.md → timestamp YouTube → video original
                                     ↘ transcript_youtube_raw / transcript_groq_raw
```

Si una frase es central para un concepto, debe verificarse contra:

- `transcript_readable.md`;
- `transcript_groq_raw.md`;
- `transcript_youtube_raw.md` si hay dudas;
- el audio/video original si la formulación es delicada.

## Regla editorial

La canónica puede corregir:

- puntuación;
- mayúsculas;
- cortes raros;
- palabras obviamente mal transcritas;
- nombres propios cuando estén claros;
- segmentación.

La canónica no puede:

- inventar contenido;
- suavizar ideas incómodas;
- traducir sin marcarlo;
- reemplazar una afirmación ambigua por una más fuerte;
- borrar dudas sin dejar rastro.

Si hay duda, usar una marca como:

```md
[inaudible]
[?]
```

O agregar una nota editorial breve.

## Naming definitivo

Para cada video:

```txt
metadata.json
transcript_youtube_raw.json
transcript_youtube_raw.md
transcript_youtube_indexed.md      # opcional, raw + block refs
transcript_groq_raw.json
transcript_groq_raw.md
transcript_readable.md             # canónica visible
transcript_alignment.json          # futuro: mapa YouTube ↔ Groq ↔ readable
```

## Estado de madurez

`transcript_readable.md` debe tener un estado:

```yaml
transcript_readable_status: provisional | alineada | revisada | verificada
```

Significados:

- `provisional`: generada automáticamente desde Groq con timestamps básicos.
- `alineada`: combinó Groq + YouTube para mejorar timestamps.
- `revisada`: un humano revisó fragmentos importantes.
- `verificada`: citas centrales fueron cotejadas contra video/audio.

## Recomendación operativa

Para el MVP:

1. Descargar YouTube raw si existe.
2. Transcribir con Groq.
3. Generar `transcript_readable.md` desde Groq.
4. Conservar timestamps clickeables.
5. En documentos de revisión conceptual, enlazar siempre a `transcript_readable.md`.
6. Para citas importantes, ajustar el timestamp manualmente si hace falta.

Más adelante:

7. Crear script de alineación Groq/YouTube.
8. Generar `transcript_alignment.json`.
9. Dividir la canónica en unidades semánticas más finas.
