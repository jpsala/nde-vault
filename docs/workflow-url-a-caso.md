# Workflow inicial — de URL/fuente a caso o unidad del vault

Este es el flujo manual/asistido inicial. Antes de crear una interfaz, vamos a procesar URLs por conversación para descubrir el mejor modelo de datos, los prompts, las categorías y las decisiones editoriales.

## Principio

El usuario puede pasar una URL de YouTube, documento, entrevista, artículo, libro o fuente textual en el chat y pedir que sea procesada.

El agente debe convertir esa fuente en conocimiento trazable dentro del vault:

```txt
URL / documento / fuente
  ↓
metadata + original/transcripción/notas preservadas
  ↓
ficha de caso o unidad de análisis
  ↓
fragmentos relevantes con timestamps o ubicaciones
  ↓
conceptos detectados, especialmente los ligados al norte vivencial
  ↓
actualización/propuesta de notas de concepto
```

NDE/ECM sigue siendo una fuente privilegiada, pero ya no es requisito. Para fuentes no-ECM, registrar explícitamente que `es_ecm: false` y explicar `relacion_norte`.

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
- tipo de fuente (`youtube`, `web`, `pdf`, `libro`, `entrevista`, etc.);
- si es ECM/NDE (`es_ecm: true/false`);
- relación con el norte vivencial (`relacion_norte`: manifestación, creencias, confianza, miedo, salud, cuidado, etc.);
- video id si aplica;
- título si está disponible;
- canal/autor del video si está disponible;
- link al canal/autor del video;
- nombre y link de la persona que da el testimonio / experienciador(a) / autor(a) / docente / entrevistado(a), si está disponible;
- foto del experienciador(a), idealmente preservada localmente;
- avatar del canal solo como dato secundario, nunca como foto del experienciador;
- thumbnail del video, idealmente preservado localmente;
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
vault/06-fuentes/youtube/<video_id>/source-card.md
vault/06-fuentes/youtube/<video_id>/media/video-thumbnail.jpg
vault/06-fuentes/youtube/<video_id>/media/experiencer-photo.jpg
vault/06-fuentes/youtube/<video_id>/media/channel-avatar.jpg   # opcional/secundario
vault/06-fuentes/youtube/<video_id>/transcript_youtube_raw.json
vault/06-fuentes/youtube/<video_id>/transcript_youtube_raw.md
vault/06-fuentes/youtube/<video_id>/transcript_groq_raw.json
vault/06-fuentes/youtube/<video_id>/transcript_groq_raw.md
vault/06-fuentes/youtube/<video_id>/transcript_readable.md
```

Ver `docs/transcription-policy.md`.

### 3. Crear caso Markdown o unidad de análisis

Crear, cuando corresponda:

```txt
vault/01-casos/<case_id>-<slug>.md
```

Para una fuente no testimonial o no-ECM, también se puede usar el mismo formato como “unidad de análisis” si aporta evidencia conceptual. Debe contener:

- metadata;
- link a la fuente de video y a la tarjeta visual de fuente (`source-card.md`) cuando exista;
- resumen;
- conceptos detectados;
- fragmentos relevantes;
- links a timestamps;
- link a transcripción/fuente original;
- estado de revisión;
- `tipo_fuente`, `es_ecm` y `relacion_norte` en frontmatter cuando aplique.

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
- sugiere crear un concepto nuevo;
- aporta al norte vivencial del proyecto: manifestación, creencias, confianza, creatividad, miedo, salud, cuidado, Dios/Universo confiable, no-soledad.

Si aparece un concepto nuevo importante, **no crear la nota conceptual definitiva sin aprobación explícita del usuario**. En su lugar, registrar una propuesta en el caso y/o en `vault/05-preguntas/` con evidencia y motivo.

### 6. Crear o actualizar track conceptual conversacional

Antes de crear conceptos definitivos, crear o actualizar un track retomable en `docs/tracks/`.

El track no es transcript ni formulario. Debe guardar estado durable y conversacional:

- caso/fuente activa;
- qué transcripciones y archivos ya existen;
- conceptos existentes/semilla que el caso podría iluminar;
- conceptos nuevos propuestos;
- evidencia clave con timestamps y links a `transcript_readable.md`;
- preguntas conceptuales abiertas;
- decisiones ya tomadas en conversación;
- próximos pasos para retomar en otra sesión.

La discusión conceptual ocurre por chat. El agente va actualizando el track cuando aparecen decisiones, dudas importantes o cambios de dirección.

Los documentos con checkboxes en `vault/05-preguntas/` pueden existir como artefactos experimentales o auxiliares, pero el flujo principal es conversacional y se retoma desde `docs/tracks/`.

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
