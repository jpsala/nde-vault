# Working Memory

Estado vivo corto del proyecto. Mantener liviano.

Última actualización manual: 2026-06-24.

## Lectura rápida

| Área | Estado | Abrir primero | Siguiente acción |
| --- | --- | --- | --- |
| Proyecto confianza/creatividad | active | `docs/topics/paradigma-confianza-creatividad.md`, `docs/topics/nde-vault.md` | Procesar fuentes ECM y no-ECM con trazabilidad hacia el norte vivencial. |
| Workflow URL a caso | active | `docs/workflow-url-a-caso.md` | Usar para nuevas URLs de YouTube/NDE. |
| Transcripciones | active | `docs/transcription-policy.md` | Preservar raw y crear readable auditable. |
| Tracks de casos | active | `docs/tracks/conceptos-caso-0001..0007-*.md` | 0007 incorporado en conceptos principales; Dios cercano/no punitivo aprobado. |
| Prioridades conceptuales | active | `docs/topics/concept-priorities.md`, `docs/topics/paradigma-confianza-creatividad.md` | Integrar manifestación/creencias/confianza como eje central. |
| AOS local | active | `docs/topics/agentic-os-local.md`, `docs/topics/docs-knowledge-system.md` | Mantener docs livianos, índice y audit. |

## Estado actual

- Vault Markdown/Obsidian para construir el paradigma de confianza/creatividad; NDE/ECM es fuente privilegiada pero no exclusiva. `vault/` es fuente canónica y el trabajo es chat + Markdown + Obsidian.
- Se pueden incorporar videos/docs no-ECM si aportan al norte vivencial; registrar `tipo_fuente`, `es_ecm: false` y `relacion_norte`.
- Conceptos definitivos requieren aprobación humana explícita; el trabajo previo vive en `docs/tracks/`. El 2026-06-24 el usuario aprobó crear el paquete central del norte confianza/creatividad.
- Casos procesados: 0001 Mary Helen Hensley, 0002 Kevin Mohatt, 0003 Anita Moorjani, 0004 James E, 0005 Peter Anthony, 0006 Jane Thompson, 0007 Tricia Barker, 0008 Landon Dennis. Ver tracks para detalles.
- 0004 James E ya está incorporado a `curacion-extrema-post-ecm` con matiz de fuente textual NDERF; 0005 Peter Anthony es fuerte para manifestación/confianza/universo.
- Norte vivencial/prioridades: pasar de miedo/desconfianza/soledad a creatividad/confianza/paz en universo-Dios-cuidado. Temas: `manifestacion`, `creencias`, `confianza`, `salud`, `miedo`, `creacion`, `dios-como-padre-cercano`, `jesus-como-hermano`, `estamos-siendo-cuidados`. Cuanto más relacionado, más importante. `salud` queda remarcado como eje central, especialmente ligado a manifestación/confianza/creencias, miedo, cuerpo, coherencia interior, recuperación y cuidado. Ver `docs/topics/paradigma-confianza-creatividad.md` y `docs/topics/concept-priorities.md`.
- Subconceptos/aliases delicados, incluido `cuerpo-como-senal-de-desalineacion`, quedan en observación; no crear notas separadas ni afirmaciones médicas/culpabilizantes sin conversación.
- Preservar raw transcripts/metadata; para fuentes textuales usar `source-notes.md`; en videos separar thumbnail, foto del experienciador y avatar del canal.
- Criterio testimonial: tratar casos elegidos por el usuario como testimonios de buena fe; separar relato, percepción subjetiva, elemento verificable, patrón e interpretación.
- AOS/Pi local activo; repo público: `https://github.com/jpsala/nde-vault`.

## Riesgos

- No exponer ni leer `.env` salvo necesidad explícita; `GROQ_API_KEY` es secreto local.
- No tocar `.tmp/`, audios, raw transcripts ni `vault/.obsidian/plugins/` salvo pedido concreto.
- No convertir interpretaciones en afirmaciones absolutas; mantener trazabilidad a citas/timestamps.
- No crear conceptos definitivos sin aprobación humana.

## Próximo paso probable

Objetivo de continuidad: consolidar `manifestacion`, `confianza`, `creencias`, `salud`, `miedo` y `estamos-siendo-cuidados`; salud es eje central.

1. Paquete central aprobado y creado en `vault/02-conceptos/`; Caso 0006 Jane Thompson ya fue incorporado al paquete y a la ruta `vivir-en-confianza-y-creatividad`.
2. Caso 0007 Tricia Barker procesado inicial: muy fuerte para salud/cuidado/confianza; abre observación para `dios-como-presencia-cercana-y-no-punitiva`.
3. Actualización realizada: Tricia ya fue incorporada en el paquete central del norte (`salud-y-conciencia`, `estamos-siendo-cuidados`, `confianza-en-el-universo`, `miedo-como-contraccion-o-separacion`, `creencias-que-crean-experiencia`, `manifestacion-como-alineamiento-y-entrega`).
4. Ruta `vivir-en-confianza-y-creatividad` actualizada con el Caso 0007.
5. Conceptos fenomenológicos principales actualizados con Tricia: `identidad-mas-alla-del-cuerpo`, `percepcion-extracorporal-de-la-realidad-fisica`, `no-es-tu-momento`, `reentrada-al-cuerpo`, `continuidad-de-vinculos-con-fallecidos`, `ausencia-de-juicio-externo`, `conocimiento-directo-no-verbal`, `acompanamiento-no-fisico`.
6. Conceptos de soporte actualizados con Tricia: `muerte-como-transicion`, `unidad-e-interconexion-de-los-seres`.
7. Concepto aprobado y creado: `dios-como-presencia-cercana-y-no-punitiva`; decisión/propuesta registrada en `vault/05-preguntas/cambio-conceptual-20260624-dios-presencia-cercana-no-punitiva.md`. El usuario indicó que le interesa y que aparecerá seguido.
8. Caso 0008 Landon Dennis ingresado con transcripción YouTube automática, caso inicial y track; fuerte para oración/cuidado, Dios-Padre cercano, no-soledad, continuidad de vínculos, miedo/estado intermedio, recuperación y servicio. Conceptos seguros ya integrados en notas existentes: cuidado, Dios cercano/no punitivo, confianza, continuidad de vínculos, percepción extracorporal, miedo, acompañamiento, conocimiento directo, identidad, muerte, salud, ausencia de juicio y reentrada. No se crearon conceptos nuevos.
9. Próximo paso probable: decidir si `oracion-como-linea-de-cuidado`, `jesus-como-ancla` o `seres-oscuros-o-estado-intermedio-de-angustia` quedan como observaciones recurrentes/subconceptos futuros; o seguir buscando evidencia directa para `dios-como-padre-cercano`/`jesus-como-hermano`.

## Comandos de contexto

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```
