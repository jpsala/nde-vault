# Decisiones del proyecto

Registro de decisiones durables del vault NDE/ECM.

## 2026-06-29 — Mantener backlog de propuestas y rechequearlo con nuevos videos

Decisión: las propuestas en observación no deben forzarse a concepto nuevo de inmediato. Pueden quedar guardadas como backlog conceptual y se rechequearán al procesar nuevos videos/fuentes para decidir si se absorben en conceptos existentes, se acumula evidencia o pasan a propuesta de concepto aprobado.

Motivo: el usuario prefiere conservar las sugerencias útiles y dejar que el corpus nuevo determine si merecen nota propia o integración en conceptos existentes.

Afecta: `docs/tracks/rechequeo-propuestas-observacion-2026-06-29.md`, tracks conceptuales por caso, respuestas al usuario tras nuevos videos y revisión periódica de ontología.

Guardrail: no crear conceptos definitivos desde el backlog sin aprobación explícita. Al presentar propuestas al usuario, mantener listas numeradas para facilitar referencia por número.

## 2026-06-29 — Numerar propuestas nuevas en observación al responder

Decisión: cuando el agente devuelva al usuario conceptos nuevos en observación/propuestas, debe presentarlos siempre como lista numerada estable (`1.`, `2.`, `3.`...).

Motivo: el usuario quiere poder aprobar, rechazar o comentar propuestas usando solo los números.

Afecta: respuestas finales tras procesar videos/fuentes, `docs/workflow-url-a-caso.md`, `docs/concept-lifecycle.md` y tracks conceptuales cuando se preparen listas conversacionales.

Guardrail: conservar los mismos números mientras se siga conversando sobre esa misma lista; si se crea una lista nueva o se reagrupan propuestas, dejar claro que la numeración fue regenerada.

## 2026-06-29 — Nuevos conceptos aprobados desde Caso 0011 John Paul Martinez

Decisión: crear como conceptos aprobados `estado-intermedio-de-oscuridad-o-experiencia-infernal`, `perdon-como-liberacion-y-sanacion`, `llamado-como-reorientacion-de-vida` y `dios-envia-personas-y-palabras`.

Motivo: tras procesar el Caso 0011, el usuario aprobó implementar las sugerencias conceptuales del agente. Estos conceptos capturan cuatro patrones importantes: oscuridad/advertencia con guardrails contra dogmatismo de miedo; perdón como sanación del corazón/mente; llamado como reorientación de vida hacia servicio; y cuidado divino/universal mediado por personas, palabras, lugares y situaciones oportunas.

Afecta: `vault/02-conceptos/estado-intermedio-de-oscuridad-o-experiencia-infernal.md`, `vault/02-conceptos/perdon-como-liberacion-y-sanacion.md`, `vault/02-conceptos/llamado-como-reorientacion-de-vida.md`, `vault/02-conceptos/dios-envia-personas-y-palabras.md`, `vault/01-casos/caso-0011-john-paul-martinez.md`, `docs/tracks/conceptos-caso-0011-john-paul-martinez.md`, además de índices/rutas/prioridades.

Casos/evidencia: Caso 0011 John Paul Martinez — “outer darkness” y gritos 08:43–10:02; oración/perdón/sanación 24:26–27:55; “but still I called you” 25:39; “God will send something our way” 33:27. Evidencia comparativa: Landon Dennis para estado intermedio/oraciones como luz; Tricia Barker para culpa infantil lavada por amor; Peter Anthony para universo que provee personas/lugares/situaciones; Billy Garaffa para misión y personas oportunas en emergencia.

Guardrail: no dogmatizar experiencias infernales ni usar religión/oración/perdón como sustituto de ayuda médica, psicológica, comunitaria, legal o reparación. Mantener lenguaje testimonial y diferenciar fenómeno, interpretación y doctrina.

## 2026-06-29 — Nuevos conceptos aprobados desde Caso 0010 Billy Garaffa

Decisión: crear como conceptos aprobados `amor-como-nucleo-simple-de-la-vida`, `oracion-como-linea-de-cuidado`, `jesus-como-ancla`, `teologia-subordinada-al-amor` y `olor-sabor-y-sentidos-espirituales`.

Motivo: tras procesar el Caso 0010, el usuario aprobó implementar las propuestas surgidas del análisis. Los primeros cuatro conceptos son directamente relevantes para el norte confianza/creatividad: amor como centro, oración como cuidado, Jesús cercano/ancla y creencias religiosas subordinadas al amor. `olor-sabor-y-sentidos-espirituales` se aprueba como concepto fenomenológico de soporte, con menor prioridad.

Afecta: `vault/02-conceptos/amor-como-nucleo-simple-de-la-vida.md`, `vault/02-conceptos/oracion-como-linea-de-cuidado.md`, `vault/02-conceptos/jesus-como-ancla.md`, `vault/02-conceptos/teologia-subordinada-al-amor.md`, `vault/02-conceptos/olor-sabor-y-sentidos-espirituales.md`, `vault/01-casos/caso-0010-billy-garaffa.md`, `docs/tracks/conceptos-caso-0010-billy-garaffa.md`, `vault/04-paradigma/indice-del-paradigma.md`, `vault/07-rutas/vivir-en-confianza-y-creatividad.md`, `docs/topics/concept-priorities.md`.

Casos/evidencia: Caso 0010 Billy Garaffa — amor a Dios/prójimo bajo el cual cae todo 06:31 y 22:32; Jesús siempre presente/guiando 14:35–15:54; oración/invocación de Jesús 13:23 y 23:54; sentidos espirituales de oler/saborear a Dios y olor de muerte 07:46 y 29:13. Caso 0008 Landon Dennis — oración como línea directa 14:54, oraciones como luz 21:01, “My anchor is Jesus Christ” 44:10, Dios no limitado al nombre usado 14:21.

Guardrail: no convertir estos conceptos en dogma religioso universal ni en sustituto de acción médica/psicológica/comunitaria. Mantener lenguaje testimonial y distinguir casos cristianos de la amplitud del corpus. `jesus-como-hermano` queda como posible subtipo/renombre futuro; `olor-sabor-y-sentidos-espirituales` queda como soporte fenomenológico inicial.

## 2026-06-29 — Referenciar automáticamente conceptos existentes cuando el encaje es seguro

Decisión: para cada video/fuente nueva, el agente debe revisar los conceptos ya aprobados y, cuando tenga seguridad alta de que el caso/fragmento se ajusta, crear o actualizar la referencia entre el video/caso y esos conceptos sin pedir aprobación previa.

Motivo: el usuario propuso un flujo más eficiente: los conceptos existentes se alimentan automáticamente con evidencia clara; la conversación humana se reserva para conceptos nuevos o conceptos donde el agente no esté seguro.

Afecta: `docs/workflow-url-a-caso.md`, `docs/concept-lifecycle.md`, tracks por caso y bloques `AUTO` de `vault/02-conceptos/`.

Guardrail: no crear conceptos definitivos nuevos, cambiar definiciones manuales, renombrar, fusionar o dividir conceptos sin aprobación explícita. Si el encaje es parcial, ambiguo, sensible o requiere reinterpretar el concepto, dejarlo en observación/propuesta con evidencia y preguntar por conversación.

## 2026-06-26 — Aceptación como no-resistencia aprobada

Decisión: crear `aceptacion-como-no-resistencia` como concepto aprobado del paradigma.

Motivo: el usuario pidió trabajar este eje y aprobó convertirlo en concepto definitivo. La fuente no-ECM de Daniel Shai aporta el lenguaje más explícito —aceptación/no-lucha, “freedom within”, no escapar de la experiencia— y Jane Thompson aporta el ancla ECM más directa: “Fear is resistance and fear is glue and there is no flow there.” El concepto funciona como puente práctico entre confianza, miedo, manifestación, salud y creencias.

Afecta: `vault/02-conceptos/aceptacion-como-no-resistencia.md`, `vault/05-preguntas/cambio-conceptual-20260626-aceptacion-como-no-resistencia.md`, `docs/tracks/conceptos-unidad-0009-daniel-shai-liberacion.md`, notas relacionadas de confianza, miedo, manifestación, salud y creencias.

Casos/evidencia: Unidad 0009 Daniel Shai — “Acceptance makes nothing into a problem” 17:04; “freedom within” 35:46. Caso 0006 Jane Thompson — “Fear is resistance and fear is glue...” 35:38; gratitud/flujo 37:55. Caso 0003 Anita Moorjani — rendición a Fuente/Dios sin entregar poder personal 01:15:04. Caso 0005 Peter Anthony — “show up in faith not in fear” 27:42 y confiar en que el universo provee personas/lugares/situaciones 31:47.

Guardrail: no confundir aceptación con resignación, pasividad, sometimiento, bypass espiritual, fatalismo ni abandono de límites, ayuda médica/psicológica o acción responsable. Separar evidencia ECM de enseñanza no-ECM.

## 2026-06-24 — Dios como presencia cercana y no punitiva aprobado

Decisión: crear `dios-como-presencia-cercana-y-no-punitiva` como concepto aprobado del paradigma.

Motivo: el Caso 0007 — Tricia Barker aporta evidencia fuerte de Dios/Luz como presencia cercana, amorosa, sanadora y no punitiva: “child of God”, “loved completely”, “that wasn't your fault” y seguridad/cuidado cerca de Dios. El usuario confirmó interés y expectativa de recurrencia: “me interesa, la vamos a encontrar seguido”.

Afecta: `vault/02-conceptos/dios-como-presencia-cercana-y-no-punitiva.md`, `vault/05-preguntas/cambio-conceptual-20260624-dios-presencia-cercana-no-punitiva.md`, `docs/topics/concept-priorities.md`, `vault/07-rutas/vivir-en-confianza-y-creatividad.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Casos/evidencia: Caso 0007 — “like the light of God” 00:08:47; “that wasn't your fault” 00:11:48; “you're a child of God; you are loved completely” 00:11:52; “I was loved deeply by God” 00:12:04; “I'm safe. I'm taken care of” 00:12:52. Caso 0006 — luz blanca que cuida amorosamente 08:14; “all is well” / “we're all taken care of” 09:42.

Guardrail: no convertir lenguaje teísta/cristiano en requisito para todas las fuentes; mantener Dios/Luz/Fuente según el testimonio. No negar sufrimiento ni convertir “Dios cercano” en bypass espiritual. `dios-como-padre-cercano` queda como subconcepto/posible nota futura; `jesus-como-hermano` sigue como búsqueda prioritaria separada.

## 2026-06-24 — Paquete conceptual del norte confianza/creatividad aprobado

Decisión: crear como conceptos aprobados del paradigma `manifestacion-como-alineamiento-y-entrega`, `confianza-en-el-universo`, `creencias-que-crean-experiencia`, `salud-y-conciencia`, `miedo-como-contraccion-o-separacion` y `estamos-siendo-cuidados`.

Motivo: el usuario confirmó que estos ejes son centrales para el norte vivencial, remarcó especialmente `salud` como concepto central ligado a manifestación/confianza/creencias, y aprobó avanzar con “go” tras la auditoría de transcripciones desde el norte.

Afecta: `vault/02-conceptos/`, `vault/07-rutas/vivir-en-confianza-y-creatividad.md`, `vault/04-paradigma/indice-del-paradigma.md`, `docs/topics/concept-priorities.md`.

Guardrail: mantener trazabilidad a citas/casos, evitar dogmatismo y proteger especialmente el eje salud/creencias de lecturas culpabilizantes o recomendaciones médicas. `estamos-siendo-cuidados` queda como nota propia, no solo alias de `acompanamiento-no-fisico`, porque expresa el norte existencial de cuidado/soporte activo.

## 2026-06-24 — Fuentes textuales reconocidas pueden usarse como casos del corpus

Decisión: Además de videos/transcripciones, el vault puede incorporar casos desde fuentes textuales reconocidas como NDERF y otros repositorios/lugares conocidos, siempre que se registren como fuente textual y no se presenten como si tuvieran video/transcripción audiovisual.

Motivo: Al revisar James E, no apareció video ni transcripción audiovisual, pero el usuario confirmó que estos casos pueden servir y que se pueden usar casos de NDERF y otros lugares conocidos.

Afecta: `vault/01-casos/`, `vault/06-fuentes/web/`, `docs/tracks/`, notas conceptuales que acumulen evidencia de casos textuales.

Guardrail: Marcar claramente el tipo de fuente (`web`, `textual`, `NDERF`, etc.), conservar citas/extractos y URL, y distinguir nivel de documentación: fuente textual única, fuente audiovisual, múltiples fuentes, o documentación clínica/externa. No crear “transcript” cuando no hay audio/video; usar `source-notes.md` o equivalente.

## 2026-06-23 — Tarjetas visuales de fuente separan experienciador, video y canal

Decisión: Cada fuente de video debe tener una tarjeta visual (`source-card.md`) que separe explícitamente: thumbnail del video (`media/video-thumbnail.jpg`), foto de la persona que da testimonio (`media/experiencer-photo.jpg`) y, solo como dato secundario, avatar/link del canal (`media/channel-avatar.jpg`).

Motivo: El usuario aclaró que no quiere la foto del dueño del canal como “autor” visual del caso, sino la foto del experienciador/testimoniante. El canal sigue siendo fuente/publicador, pero no reemplaza a la persona del testimonio.

Afecta: `docs/workflow-url-a-caso.md`, `docs/WORKING_MEMORY.md`, `vault/06-fuentes/youtube/*/source-card.md`, `metadata.json` de fuentes YouTube.

Guardrail: Si no hay retrato independiente verificado, usar un fallback explícitamente marcado como provisional (por ejemplo, thumbnail del video) y no hacerlo pasar por foto verificada del experienciador.

## 2026-06-23 — Curación extrema post-ECM aprobada desde Caso 0003

Decisión: Crear `curacion-extrema-post-ecm` como concepto propio para recuperaciones corporales rápidas, profundas y difíciles de explicar desde las expectativas médicas ordinarias disponibles en el relato. `sanacion-post-ecm`, `curacion-inexplicable-post-ecm` y formulaciones similares quedan como aliases.

Motivo: El usuario pidió aprovechar las fuentes de Anita Moorjani para hacer fuerte este concepto. El Caso 0003 aporta un ancla densa: coma terminal, órganos apagándose, pronóstico de 36 horas, tumores tamaño limón, reducción tumoral 60–70% en cuatro días, no detección de cáncer en semanas, debate sobre quimioterapia, médicos desconcertados y lesiones abiertas sanando sin cirugía.

Afecta: `vault/02-conceptos/curacion-extrema-post-ecm.md`, `vault/01-casos/caso-0003-anita-moorjani.md`, `docs/tracks/conceptos-caso-0003-anita-moorjani.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Guardrail: No usar como consejo médico, promesa terapéutica ni causalidad general sobre cáncer/emociones. Separar estado médico relatado, cambio físico relatado, interpretación de la experienciadora y tensiones médicas/documentales.

## 2026-06-23 — Reentrada al cuerpo aprobada desde Caso 0002

Decisión: Crear `reentrada-al-cuerpo` como concepto propio para el momento experiencial de volver a la percepción corporal tras una ECM/NDE o experiencia extracorporal. `retorno-al-cuerpo`, `volver-al-cuerpo` y formulaciones equivalentes quedan como aliases.

Motivo: El Caso 0002 muestra una reentrada brusca tras “Not yet”, y el usuario señaló que hay muchos casos que hablan de la reentrada al cuerpo; por tanto no debe quedar como observación menor.

Afecta: `vault/02-conceptos/reentrada-al-cuerpo.md`, `vault/01-casos/caso-0002-kevin-mohatt.md`, `docs/tracks/conceptos-caso-0002-kevin-mohatt.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Guardrail: Separar `reentrada-al-cuerpo` de `muerte-como-transicion` y de `no-es-tu-momento`; no toda reentrada será traumática ni tendrá el mismo mecanismo.

## 2026-06-23 — No es tu momento aprobado desde Caso 0002

Decisión: Crear `no-es-tu-momento` como concepto propio para el mensaje o límite de retorno expresado como “not yet”, “todavía no”, “no es tu momento”, “tienes que volver” o variantes.

Motivo: En el Caso 0002, Kevin Mohatt recibe “Not yet. Not yet.” como comunicación interior; el usuario indicó que este patrón aparece en una gran cantidad de experiencias. Se separa el contenido del mensaje (`no-es-tu-momento`) del modo comunicativo (`conocimiento-directo-no-verbal`).

Afecta: `vault/02-conceptos/no-es-tu-momento.md`, `vault/02-conceptos/conocimiento-directo-no-verbal.md`, `vault/01-casos/caso-0002-kevin-mohatt.md`, `docs/tracks/conceptos-caso-0002-kevin-mohatt.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Guardrail: No asumir siempre autoridad externa ni misión doctrinal; puede aparecer como voz, presencia, comprensión interior, elección o límite del entorno.

## 2026-06-23 — Criterio de confianza testimonial del corpus seleccionado

Decisión: Trabajar los testimonios elegidos por el usuario como relatos de buena fe; no analizarlos por defecto desde la sospecha de mentira.

Motivo: El usuario aclaró que elige videos que le generan seguridad de que la persona no está mintiendo. Esto no excluye que haya visiones dependientes del experienciador o elementos subjetivos.

Afecta: `docs/topics/concept-governance.md`, notas conceptuales con matices sobre corroboración y el método general de análisis.

Guardrail: “Sin corroboración externa independiente registrada” significa matiz de trazabilidad documental dentro del vault, no acusación de mentira. Seguir separando relato, percepción subjetiva, elemento físico potencialmente verificable, patrón acumulado e interpretación paradigmática.

## 2026-06-23 — Continuidad de vínculos con fallecidos aprobada como idea con nombre provisional para Caso 0001

Decisión: Crear `continuidad-de-vinculos-con-fallecidos` como concepto para la persistencia de vínculos afectivos o relacionales con personas fallecidas. El nombre queda explícitamente provisional y ajustable a medida que se analicen otros videos.

Motivo: El usuario aprobó la idea, pero indicó que no está seguro del nombre; se prioriza conservar el núcleo conceptual sin fijar definitivamente la formulación.

Afecta: `vault/02-conceptos/`, `vault/01-casos/caso-0001-mary-helen-hensley.md`, `docs/tracks/conceptos-caso-0001-mary-helen-hensley.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Casos/evidencia: Caso 0001 — el abuelo fallecido “Judge” aparece como mejor amigo/compañero 00:00:27–00:00:46; Mary Helen habla con él y relata cosas que no podría saber 00:00:55–00:01:10; habla con personas fallecidas vinculadas a la congregación de su padre 00:01:40; primeras experiencias fuera del cuerpo con su abuelo fallecido 00:02:32–00:02:45.

Guardrail: No formular como prueba absoluta ni como práctica mediúmnica general; registrar continuidad vincular testimonial con trazabilidad. Revisar nombre cuando haya más casos y variantes.

## 2026-06-23 — Ausencia de condena final aprobada para Caso 0001

Decisión: Crear `ausencia-de-condena-final` como concepto propio para la no exclusión definitiva o no condena eterna tras la muerte. `todos-son-bienvenidos`, `no-condena-final`, `acogida-universal` y `no-exclusion-final` quedan como aliases/formulaciones.

Motivo: El usuario aprobó el nombre neutral `ausencia-de-condena-final` para distinguir este núcleo de `ausencia-de-juicio-externo`. El foco no es solo si hay juez durante una revisión de vida, sino si existe una exclusión/condena final tipo cielo/infierno.

Afecta: `vault/02-conceptos/`, `vault/01-casos/caso-0001-mary-helen-hensley.md`, `docs/tracks/conceptos-caso-0001-mary-helen-hensley.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Casos/evidencia: Caso 0001 — el padre teme por el destino de su propio padre 00:34:33–00:34:58; al morir lo ve en el espacio no físico 00:35:06; “I've had it wrong all along” 00:35:17; “Everybody's welcome here” y “You can't mess this thing up” 00:35:23–00:35:25; crítica a la separación cielo/infierno 00:35:42–00:35:50; disponible para cada uno 00:36:09.

Guardrail: No confundir ausencia de condena final con ausencia de responsabilidad, revisión, aprendizaje o consecuencias experienciales. En el Caso 0001 la evidencia central es testimonio indirecto de la experiencia del padre relatada por Mary Helen.

## 2026-06-23 — Conocimiento directo no verbal aprobado para Caso 0001

Decisión: Crear `conocimiento-directo-no-verbal` como concepto propio para comunicación/conocimiento sin palabras, como comprensión directa o compartida. `comunicacion-telepatica-o-conocimiento-directo` queda supersedido como formulación provisional; `telepatia` y `comunicacion-telepatica` quedan como aliases.

Motivo: El usuario eligió el nombre fenomenológico `conocimiento-directo-no-verbal` para evitar cargar el concepto con supuestos previos de “telepatía” y para no reducirlo a `acompanamiento-no-fisico`.

Afecta: `vault/02-conceptos/`, `vault/01-casos/caso-0001-mary-helen-hensley.md`, `docs/tracks/conceptos-caso-0001-mary-helen-hensley.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Casos/evidencia: Caso 0001 — comunicación con guías sin movimiento de boca 00:20:35; “we are just knowing each other” 00:20:40; “telepathic... just a knowing” y “no words had to be spoken” 00:20:44–00:20:50.

Guardrail: Registrar el fenómeno como comunicación/conocimiento no verbal reportado, sin cerrar todavía un mecanismo ontológico; en este caso aparece con guías, pero puede aparecer en futuros casos con fallecidos, seres, revisiones de vida o descargas de información.

## 2026-06-23 — Realidad material como constructo experiencial aprobada para Caso 0001

Decisión: Crear `realidad-material-como-constructo-experiencial` como concepto raíz/paraguas para realidad física como escenario, juego, interfaz, plano o constructo inmersivo con reglas, cuerpos, tiempo, roles y contraste. `realidad-como-juego-o-constructo-experiencial` queda supersedido como formulación provisional.

Motivo: El usuario señaló que realidad como juego, realidad como constructo y plano físico como escenario son variantes de un patrón muy importante y recurrente en muchos experienciadores, por lo que no debe quedar como metáfora menor ni simple subconcepto.

Afecta: `vault/02-conceptos/`, `vault/01-casos/caso-0001-mary-helen-hensley.md`, `docs/tracks/conceptos-caso-0001-mary-helen-hensley.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Casos/evidencia: Caso 0001 — implosión de tiempo/espacio/realidad 00:18:44; tiempo como constructo/plantilla 00:20:18–00:20:23; analogía del Monopoly 00:43:45–00:44:19; playground/schoolhouse 00:47:43.

Guardrail: “Juego” no significa trivialidad ni ausencia de sufrimiento; usarlo como entorno inmersivo con reglas, roles, riesgo emocional y aprendizaje. El aporte acumulado del usuario guía la jerarquía conceptual, pero las notas deben sostenerse con casos trazables.

## 2026-06-23 — Encarnación como experiencia de aprendizaje aprobada para Caso 0001

Decisión: Crear `encarnacion-como-experiencia-de-aprendizaje` como concepto raíz para la vida encarnada como experiencia inmersiva de contraste, aprendizaje, crecimiento y evolución. Dejar `tierra-como-escuela` y `experiencia-inmersiva` como aliases/formulaciones, no como notas separadas todavía.

Motivo: El usuario aprobó aplicar esta arquitectura para el núcleo `tierra-como-escuela` / experiencia inmersiva. También pidió estar atento a `cuerpo-como-senal-de-desalineacion`, que queda registrado como observación emergente delicada.

Afecta: `vault/02-conceptos/`, `vault/01-casos/caso-0001-mary-helen-hensley.md`, `docs/tracks/conceptos-caso-0001-mary-helen-hensley.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Casos/evidencia: Caso 0001 — Tierra como dicotomía de oscuridad/luz 00:16:39; “schoolhouse” 00:17:06; aprender/crecer/evolucionar 00:17:13; experiencia inmersiva del alma 00:20:04; analogía del Monopoly 00:43:45–00:44:19; cuerpo como posible señal/desalineación 00:45:14–00:46:05; playground/schoolhouse 00:47:43.

Guardrail: `cuerpo-como-senal-de-desalineacion` no debe formularse como afirmación médica, causal general ni culpabilizante; requiere más corpus y revisión humana antes de convertirse en concepto independiente.

## 2026-06-23 — Acompañamiento no físico aprobado para Caso 0001

Decisión: Crear `acompanamiento-no-fisico` como concepto raíz neutral y amplio para presencias no físicas que acompañan, reciben, guían o sostienen. Dejar `guias-espirituales` y `nunca-estamos-solos` como aliases/formulaciones, no como notas separadas todavía.

Motivo: El usuario aprobó la arquitectura propuesta para evitar fijar demasiado pronto una ontología cerrada y permitir que futuros casos incluyan guías, presencias, seres, familiares fallecidos u otras formas de acompañamiento.

Afecta: `vault/02-conceptos/`, `vault/01-casos/caso-0001-mary-helen-hensley.md`, `docs/tracks/conceptos-caso-0001-mary-helen-hensley.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Casos/evidencia: Caso 0001 — reconocimiento de guías 00:15:35; acompañamiento desde el inicio de la existencia 00:15:42; “nunca estás solo” 00:15:54; conocen la historia profunda y acompañan 00:15:58–00:16:22.

## 2026-06-23 — Tiempo y temporalidad aprobados para Caso 0001

Decisión: Crear `tiempo-y-temporalidad` como concepto paraguas y `tiempo-no-lineal` como concepto aprobado bajo ese paraguas. Dejar `multiples-lineas-temporales` como subconcepto/observación emergente, no como nota independiente todavía.

Motivo: El usuario aprobó `tiempo-no-lineal` y señaló que conviene ubicarlo bajo un concepto mayor sobre el tiempo porque muchos NDEs/ECMs hablan de temporalidad y múltiples líneas temporales.

Afecta: `vault/02-conceptos/`, `vault/01-casos/caso-0001-mary-helen-hensley.md`, `docs/tracks/conceptos-caso-0001-mary-helen-hensley.md`, `vault/04-paradigma/indice-del-paradigma.md`.

Casos/evidencia: Caso 0001 — revisión de vida no lineal 00:18:04; tiempo como constructo 00:20:18–00:20:23; múltiples líneas temporales 00:25:16.

## 2026-06-23 — Conceptos de revisión, juicio y unidad aprobados para Caso 0001

Decisión: Crear notas definitivas para `revision-de-vida`, `ausencia-de-juicio-externo`, el compuesto `revision-de-vida-sin-juicio-externo` y `unidad-e-interconexion-de-los-seres`.

Motivo: El usuario dio OK conversacional a estos conceptos y pidió aplicar la distinción entre conceptos base, compuesto y aliases/formulaciones.

Afecta: `vault/02-conceptos/`, `vault/01-casos/caso-0001-mary-helen-hensley.md`, `docs/tracks/conceptos-caso-0001-mary-helen-hensley.md`.

Casos/evidencia: Caso 0001 — revisión de vida 00:17:53–00:17:59; ausencia de juicio externo/autoevaluación amorosa 00:21:22–00:21:58; unidad/interconexión 00:26:21–00:26:38.

## 2026-06-22 — Vault Markdown como fuente canónica

Decisión: El vault Markdown será la fuente primaria del conocimiento. Obsidian, sitio web, buscador y chat derivarán de esa fuente.

Motivo: mantener portabilidad, trazabilidad y control humano.

Afecta: estructura del proyecto, templates, workflow de casos y conceptos.

## 2026-06-22 — Conceptos nuevos requieren aprobación humana

Decisión: La IA puede proponer conceptos, pero no crear conceptos definitivos del paradigma sin aprobación explícita del usuario.

Motivo: evitar inflación conceptual y preservar criterio humano sobre el nuevo paradigma.

Afecta: `vault/02-conceptos/`, documentos de revisión en `vault/05-preguntas/`.

## 2026-06-22 — Transcripción canónica híbrida

Decisión: Para cada video se preservan YouTube raw y Groq raw, pero el usuario ve una transcripción canónica/readable que combina texto mejorado con timestamps clickeables.

Motivo: preservar trazabilidad sin obligar al usuario a leer transcripciones crudas de baja calidad.

Afecta: `docs/transcription-policy.md`, `docs/canonical-transcript-design.md`, fuentes en `vault/06-fuentes/`.

## 2026-06-22 — Revisión conceptual conversacional con tracks

Decisión: Reemplazar el flujo principal de revisión conceptual con checkboxes por una conversación guiada respaldada por tracks activos en `docs/tracks/`.

Motivo: Los conceptos del paradigma son hipótesis vivas; conversarlos permite ajustar nombres, jerarquías y matices mejor que un formulario rígido.

Afecta: `docs/workflow-url-a-caso.md`, `docs/concept-lifecycle.md`, `docs/topics/concept-governance.md`, `docs/tracks/`.

## 2026-06-24 — Prioridades conceptuales del usuario

Decisión: registrar como temas de máxima atención del usuario `manifestacion`, `confianza`, `salud`, `miedo`, `creacion`, `dios-como-padre-cercano`, `jesus-como-hermano` y `estamos-siendo-cuidados`.

Motivo: el usuario indicó explícitamente que estos conceptos le interesan más que otros y que los conceptos relacionados deben considerarse 10/10 en importancia.

Afecta: `docs/topics/concept-priorities.md`, `docs/concept-lifecycle.md`, `docs/topics/concept-governance.md`, `vault/99-templates/concepto.md` y las notas existentes en `vault/02-conceptos/` mediante las propiedades YAML `importancia_usuario` y `temas_prioritarios_usuario`.

Guardrail: el puntaje mide prioridad/interés del usuario, no nivel de verdad, evidencia ni madurez conceptual. Los temas prioritarios que todavía no sean conceptos aprobados deben tratarse como observaciones/propuestas hasta aprobación explícita.

## 2026-06-24 — Norte vivencial: creatividad y confianza

Decisión: integrar como norte vivencial del proyecto el paso de un paradigma de miedo/desconfianza/soledad a un paradigma de creatividad, confianza, paz, cuidado y universo/Dios confiable.

Motivo: el usuario explicitó que el objetivo principal es vivir en creatividad y confianza, usando testimonios ECM/NDE como recuerdos del hogar/origen y como evidencia trazable para desarmar el paradigma de miedo aprendido.

Afecta: `docs/topics/paradigma-confianza-creatividad.md`, `docs/topics/concept-priorities.md`, `docs/WORKING_MEMORY.md`, YAML de conceptos relacionados en `vault/02-conceptos/`.

Regla operativa: todo lo relacionado con manifestación, creencias y confianza aumenta de prioridad; cuanto más relacionado esté un concepto con ese eje, más importante es para el usuario.

Guardrail: mantener trazabilidad a testimonios/citas, evitar dogmatismo y no convertir salud/creencias en culpa médica o consejo clínico.

## 2026-06-24 — El norte supera el recorte NDE

Decisión: el norte principal del proyecto pasa a ser el paradigma de creatividad/confianza —manifestación, creencias, confianza, miedo, salud, creación, cuidado y universo/Dios confiable— por encima del recorte NDE/ECM en sí mismo.

Motivo: el usuario explicitó que, a partir de ahora, ese norte es más importante que NDE como categoría. Las NDEs/ECM siguen siendo una fuente privilegiada porque muestran recuerdos del hogar/origen, pero el corpus puede incorporar videos, documentos, entrevistas, libros o charlas no-ECM si aportan al norte vivencial.

Afecta: `AGENTS.md`, `README.md`, `docs/PROJECT.md`, `docs/project-os.md`, `docs/topics/nde-vault.md`, `docs/topics/paradigma-confianza-creatividad.md`, `docs/workflow-url-a-caso.md`, `vault/99-templates/caso.md`.

Regla operativa: para fuentes no-ECM registrar `tipo_fuente`, `es_ecm: false` y `relacion_norte`; no forzarlas como testimonios NDE. Mantener trazabilidad, citas/timestamps/ubicaciones y separación entre fuente, patrón e interpretación.

### 2026-07-04 - Usar internet libremente y pedir permiso antes de instalar

Estado: accepted

Decision: los agentes deben usar web/internet libremente por defecto cuando conocimiento externo o cambiante evite adivinar, priorizando fuentes oficiales y sin enviar secretos, `.env`, codigo privado sensible, datos personales ni credenciales. Si evidencia online contradice el repo local, docs del proyecto o comportamiento observado, deben consultar a JP antes de decidir y presentar ambas evidencias con fuentes e impacto. Para instalar dependencias, CLIs, paquetes de sistema, herramientas auxiliares o binarios/scripts remotos, deben pedir autorizacion explicita con comando exacto, alcance, motivo, riesgos, alternativas, cambios esperados y rollback.

Motivo: JP quiere recuperar poder agente usando conocimiento disponible en internet en vez de inferir de memoria, pero conservar control humano sobre cambios de entorno/instalaciones y sobre conflictos entre fuentes externas y realidad local.

Proximo paso: aplicar la politica desde `AGENTS.md` y `docs/topics/pi-agentic-os.md`.

### 2026-07-04 - Simplificar continuidad Pi a `/aos-continuar` post-guardado

Estado: accepted

Decision: AOS deja un unico comando Pi para abrir una sesion/thread nuevo: `/aos-continuar [objetivo]`. JP se hace cargo de correr `/aos-guardar-sesion` primero cuando haya valor durable. `/aos-continuar` no guarda, no compacta, no ejecuta `gol` y no duplica docs: crea una sesion nueva con `ctx.newSession()` y le pasa un prompt de continuidad que referencia `docs/.generated/context-index.md`, `docs/WORKING_MEMORY.md`, `docs/TOPICS.md`, topic/track/spec puntual y estado git. `--preview` abre la sesion nueva con el prompt en el editor sin enviarlo automaticamente.

Motivo: los comandos previos (`/aos-nueva-sesion`, `/aos-continuar-sesion`, `/aos-nueva-sesion-con-gol`, `/aos-continuar-con-gol`, `/aos-siguiente`) mezclaban guardado, handoff y ejecucion, generando ambiguedad. JP quiere revisar/controlar el guardado por separado y tener una continuidad confiable basada en docs vivos.

Proximo paso: usar `/aos-continuar` despues de `/aos-guardar-sesion` y ejecutar `/reload` tras actualizar el adapter Pi.

