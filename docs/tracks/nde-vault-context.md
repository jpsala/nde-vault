---
status: active
started: 2026-06-22
updated: 2026-06-22
priority: high
related:
  - docs/topics/paradigma-confianza-creatividad.md
  - docs/topics/concept-priorities.md
  - docs/topics/nde-vault.md
  - docs/topics/agentic-os-local.md
  - docs/workflow-url-a-caso.md
  - docs/transcription-policy.md
---

# Proyecto confianza/creatividad — Contexto retomable

## Objetivo

Mantener el proyecto retomable para agentes: reglas claras, memoria viva corta, docs indexados y checks de contexto.

Norte actual: construir un corpus trazable que ayude a pasar del paradigma de miedo/desconfianza/soledad a creatividad, confianza, paz, cuidado y universo/Dios confiable. NDE/ECM sigue siendo fuente privilegiada, pero no exclusiva.

## Estado actual

- AOS local adoptado como capa mínima/adaptada el 2026-06-22.
- Norte reencuadrado el 2026-06-24: `docs/topics/paradigma-confianza-creatividad.md` y `docs/topics/concept-priorities.md` son referencias centrales.
- El workflow acepta fuentes ECM y no-ECM; para no-ECM registrar `tipo_fuente`, `es_ecm: false` y `relacion_norte`.
- Casos 0001-0005 ya tienen `tipo_fuente`, `es_ecm` y `relacion_norte`.
- Revisión transversal de conceptos desde transcripciones: `docs/tracks/reevaluacion-conceptos-transcripciones-2026-06-24.md`.
- No tocar `.env`, `.tmp/`, raw transcripts, audios ni plugins Obsidian salvo pedido explícito.

## Próximo paso

Objetivo de continuidad explícito: procesar pendientes de `manifestacion`, `confianza`, `creencias`, `salud`, `miedo` y `estamos-siendo-cuidados`.

Ruta recomendada:

1. Abrir `docs/WORKING_MEMORY.md`, `docs/topics/paradigma-confianza-creatividad.md`, `docs/topics/concept-priorities.md` y `docs/tracks/reevaluacion-conceptos-transcripciones-2026-06-24.md`.
2. Aprobar/ajustar propuestas: `manifestacion-como-alineamiento-y-entrega`, `confianza-en-el-universo`, `creencias-que-crean-experiencia`, `salud-y-conciencia`, `miedo-como-contraccion-o-separacion`, `estamos-siendo-cuidados`.
3. Crear/actualizar conceptos con evidencia trazable y bloques AUTO, priorizando el paso miedo/desconfianza → creatividad/confianza.
4. Si entra un nuevo video/doc ECM o no-ECM, usar `docs/workflow-url-a-caso.md` y marcar `relacion_norte`.

## Evidencia / Source Refs

- `bun scripts/context-index.ts`
- `bun scripts/agent-context-audit.ts`
