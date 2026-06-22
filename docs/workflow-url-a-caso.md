# Workflow inicial — de URL de YouTube a caso del vault

Este es el flujo manual/asistido inicial. Antes de crear una interfaz, vamos a procesar URLs por conversación para descubrir el mejor modelo de datos, los prompts, las categorías y las decisiones editoriales.

## Principio

El usuario puede pasar una URL de YouTube en el chat y pedir que sea procesada.

El agente debe convertir esa URL en conocimiento trazable dentro del vault:

```txt
URL de YouTube
  ↓
metadata + transcripción original
  ↓
ficha de caso
  ↓
fragmentos relevantes con timestamps
  ↓
conceptos detectados
  ↓
actualización/propuesta de notas de concepto
```

## Modo de trabajo actual

Por ahora trabajaremos **sin interfaz propia**.

Usaremos:

- el chat como interfaz de operación;
- archivos Markdown como salida canónica;
- Obsidian para visualizar y curar;
- scripts solo cuando el proceso manual se repita lo suficiente;
- Groq para transcripción cuando corresponda.

## Qué debe hacer el agente cuando recibe una URL

### 1. Registrar la fuente

Crear o actualizar un registro de fuente/caso con:

- URL;
- video id;
- título si está disponible;
- canal si está disponible;
- idioma estimado;
- fecha de ingreso;
- estado inicial.

### 2. Obtener transcripción

Prioridad:

1. Si existe transcript/subtítulo confiable, preservarlo.
2. Si no, descargar/extractar audio y transcribir con Groq/Whisper.
3. Guardar siempre una copia original sin edición.

Archivos sugeridos:

```txt
vault/06-fuentes/youtube/<video_id>/metadata.json
vault/06-fuentes/youtube/<video_id>/transcript_youtube_raw.json
vault/06-fuentes/youtube/<video_id>/transcript_youtube_raw.md
vault/06-fuentes/youtube/<video_id>/transcript_groq_raw.json
vault/06-fuentes/youtube/<video_id>/transcript_groq_raw.md
vault/06-fuentes/youtube/<video_id>/transcript_readable.md
```

Ver `docs/transcription-policy.md`.

### 3. Crear caso Markdown

Crear:

```txt
vault/01-casos/<case_id>-<slug>.md
```

Debe contener:

- metadata;
- resumen;
- conceptos detectados;
- fragmentos relevantes;
- links a timestamps;
- link a transcripción/fuente original;
- estado de revisión.

### 4. Extraer fragmentos relevantes

Cada fragmento debe tener:

- cita textual;
- timestamp inicial y, si se puede, final;
- link al video en ese momento;
- concepto/s asociado/s;
- breve nota de por qué importa.

Formato sugerido:

```md
### [[El universo material como constructo]]

> "..."

Fuente: [00:14:32](https://youtube.com/watch?v=VIDEO_ID&t=872)  
Importancia: describe la realidad física como una construcción/escenario/sueño.
```

### 5. Detectar conceptos existentes o nuevos

El agente debe revisar `vault/02-conceptos/` y decidir si cada fragmento:

- apoya un concepto existente;
- matiza un concepto existente;
- contradice o tensiona un concepto existente;
- sugiere crear un concepto nuevo.

Si aparece un concepto nuevo importante, **no crear la nota conceptual definitiva sin aprobación explícita del usuario**. En su lugar, registrar una propuesta en el caso y/o en `vault/05-preguntas/` con evidencia y motivo.

### 6. Crear documento de revisión de conceptos

Antes de crear conceptos definitivos, generar un documento en `vault/05-preguntas/` con:

- conceptos existentes/semilla a los que el caso podría referenciar;
- conceptos nuevos propuestos;
- por qué surge cada concepto;
- evidencia con timestamps de YouTube;
- links internos a la transcripción en el punto relevante;
- checkboxes de decisión;
- espacio para comentarios del usuario.

El usuario debe poder revisar ese documento en Obsidian y decidir qué conceptos aprobar, fusionar, observar o descartar.

### 7. Actualizar notas de concepto

Solo después de aprobación del usuario, crear o actualizar notas de concepto.

Actualizar solo bloques automáticos cuando sea posible:

```md
<!-- AUTO:EVIDENCE:START -->
...
<!-- AUTO:EVIDENCE:END -->
```

Si se necesita modificar una sección manual, hacerlo como propuesta o pedir confirmación si el cambio es conceptual fuerte.

### 8. Devolver resumen al usuario

Al terminar, responder con:

- caso creado;
- cantidad de fragmentos extraídos;
- conceptos vinculados;
- conceptos nuevos propuestos/creados;
- dudas o decisiones editoriales pendientes.

## Estados posibles

Para casos:

- `pendiente`
- `transcrito`
- `analizado`
- `revisado`
- `publicable`

Para conceptos:

- `borrador`
- `en-desarrollo`
- `maduro`
- `requiere-revision`

## Regla editorial clave

No confundir:

1. lo que la persona dijo;
2. la etiqueta fenomenológica;
3. el patrón entre casos;
4. la interpretación desde el paradigma NDE/ECM;
5. una conclusión fuerte.

Toda conclusión debe sostenerse en citas y casos.
