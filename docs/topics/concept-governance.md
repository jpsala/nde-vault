---
id: concept-governance
status: active
kind: how-to
triggers:
  - gobernanza de conceptos
  - concepto nuevo
  - conceptos aprobados
  - fusionar conceptos
  - dividir conceptos
  - revision humana
primary_refs:
  - docs/concept-lifecycle.md
  - docs/workflow-url-a-caso.md
  - vault/05-preguntas/
  - vault/02-conceptos/
---

# Gobernanza de conceptos

## Problema

El vault va a crecer mucho. Si cada video crea conceptos nuevos sin control, el sistema se vuelve caótico. Pero si somos demasiado rígidos, perdemos descubrimientos importantes.

Necesitamos una gobernanza liviana para que los conceptos puedan nacer, cambiar, fusionarse, dividirse o madurar sin perder trazabilidad.

## Solución propuesta

Usar tres niveles:

### 1. Evidencia

Fragmentos concretos de casos con timestamps.

Ejemplo:

```txt
Caso 0001 — 00:07:10 — cuerpo como vehículo
```

### 2. Propuesta

Una hipótesis conceptual detectada en uno o varios fragmentos.

Vive primero en:

```txt
vault/05-preguntas/revision-conceptos-caso-XXXX.md
```

### 3. Concepto aprobado

Nota estable del paradigma en:

```txt
vault/02-conceptos/
```

## Regla de oro

> Ningún concepto nuevo entra al paradigma definitivo sin revisión humana.

## Tipos de documentos

### Documento de revisión por caso

Uno por video/caso.

Contiene:

- conceptos existentes que podrían recibir evidencia;
- conceptos nuevos sugeridos;
- evidencia;
- timestamps;
- checkboxes;
- comentarios del usuario.

### Nota de concepto

Una por concepto aprobado.

Contiene:

- definición provisional;
- lectura desde el paradigma NDE/ECM;
- contraste con paradigma clásico;
- evidencia acumulada;
- síntesis acumulada;
- tensiones;
- preguntas abiertas;
- aliases y metadata.

### Propuesta de cambio conceptual

Cuando haya que renombrar, fusionar o dividir conceptos, crear una nota en:

```txt
vault/05-preguntas/cambio-conceptual-YYYYMMDD-<slug>.md
```

Debe contener:

- cambio propuesto;
- motivo;
- conceptos afectados;
- evidencia;
- riesgos;
- decisión del usuario.

## Riesgos

### Inflación conceptual

Demasiados conceptos pequeños dificultan navegar.

Mitigación:

- crear primero conceptos raíz;
- usar etiquetas/subconceptos antes de notas nuevas;
- revisar cada 5 videos al inicio.

### Conceptos demasiado grandes

Un concepto amplio puede volverse una bolsa de todo.

Mitigación:

- detectar subtipos;
- dividir cuando haya evidencia suficiente;
- mantener `parent` y `subconceptos`.

### Nombres prematuros

El primer nombre puede no ser el mejor.

Mitigación:

- usar `id` estable;
- agregar `aliases`;
- registrar renombres en `docs/DECISIONS.md`.

### Mezcla de testimonio e interpretación

Un concepto puede volverse demasiado interpretativo.

Mitigación:

- separar evidencia literal, patrón e interpretación;
- marcar nivel de confianza;
- registrar tensiones.

## Próximo experimento

Aplicar este sistema al Caso 0001:

```txt
vault/05-preguntas/revision-conceptos-caso-0001.md
```

Objetivo:

- no crear todos los conceptos todavía;
- revisar nombres y jerarquías;
- elegir primeros conceptos raíz;
- dejar el resto como propuestas/observaciones.
