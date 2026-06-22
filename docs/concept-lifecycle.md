# Ciclo de vida de conceptos

## Decisión

Los conceptos del paradigma no son etiquetas fijas: son hipótesis vivas que se refinan con cada caso nuevo.

Por eso necesitamos separar:

```txt
fragmentos de evidencia → propuestas de concepto → conceptos aprobados → evolución/renombre/fusión/división
```

## Principio central

> La IA puede detectar, agrupar y proponer; el usuario aprueba cambios conceptuales fuertes.

Esto incluye:

- crear conceptos nuevos;
- cambiar nombres;
- fusionar conceptos;
- dividir un concepto en subconceptos;
- cambiar el sentido de una definición;
- declarar un concepto maduro o deprecado.

## Estados de un concepto

### `propuesto`

Surge de uno o varios casos, pero todavía no fue aprobado como nota conceptual definitiva.

Lugar típico:

```txt
docs/tracks/conceptos-caso-XXXX-<slug>.md
```

Opcionalmente puede haber artefactos auxiliares en `vault/05-preguntas/`, pero el trabajo vivo se retoma desde tracks.

### `aprobado`

El usuario aprobó crear una nota en:

```txt
vault/02-conceptos/<slug>.md
```

Todavía puede estar en desarrollo.

### `en-desarrollo`

Tiene evidencia, definición provisional y vínculos, pero sigue cambiando con nuevos casos.

### `maduro`

Tiene suficiente evidencia, definición estable, relaciones claras y tensiones documentadas.

### `fusionado`

El concepto fue absorbido por otro. Debe quedar una nota o alias que apunte al concepto vigente.

### `dividido`

El concepto original se separó en subconceptos más precisos.

### `deprecado`

Se conserva por trazabilidad, pero ya no se usa como concepto activo.

## Identidad estable vs nombre visible

Cada concepto debe tener un `id` estable. El título visible puede cambiar.

Ejemplo:

```yaml
id: identidad-mas-alla-del-cuerpo
titulo: Identidad más allá del cuerpo
aliases:
  - No soy el cuerpo
  - El yo real no es el cuerpo
estado: en-desarrollo
```

Si cambiamos el nombre visible, no necesariamente cambiamos el `id`.

Esto evita romper links, referencias y evidencia acumulada.

## Metadata mínima de concepto

```yaml
tipo: concepto
id: 
titulo: 
aliases: []
estado: propuesto | aprobado | en-desarrollo | maduro | fusionado | dividido | deprecado
categoria: 
parent: 
subconceptos: []
conceptos_relacionados: []
contrasta_con: []
evidencia_casos: 0
nivel_confianza: bajo | medio | alto | pendiente
ultima_revision: YYYY-MM-DD
creado_desde: caso-XXXX
supersede_a: []
supersedido_por: 
```

## Tipos de relación evidencia ↔ concepto

No toda evidencia “apoya” igual. En tracks conceptuales y notas de concepto usar estas relaciones:

- `apoya`: el fragmento expresa claramente el concepto.
- `ejemplifica`: el fragmento muestra un caso concreto del concepto.
- `matiza`: agrega una variante o detalle.
- `tensiona`: complica o contradice parcialmente el concepto.
- `contradice`: va contra el concepto.
- `requiere_revision`: hay ambigüedad o mala transcripción.

## Flujo por cada video

1. Crear caso.
2. Crear o actualizar transcripción visible.
3. Crear o actualizar track conceptual conversacional en `docs/tracks/`.
4. Separar en el track:
   - conceptos existentes a referenciar;
   - conceptos nuevos propuestos;
   - temas en observación;
   - dudas de naming/jerarquía.
5. Conversar con el usuario sobre los núcleos conceptuales.
6. Registrar en el track solo valor durable: decisiones, dudas, próximos pasos y evidencia clave.
7. El agente aplica decisiones explícitas:
   - actualiza evidencia en conceptos aprobados;
   - crea conceptos aprobados;
   - registra fusiones/divisiones/renombres;
   - deja pendientes los no aprobados.

## Cambios conceptuales fuertes

Requieren aprobación explícita:

- crear concepto definitivo;
- renombrar concepto;
- fusionar conceptos;
- dividir concepto;
- cambiar definición manual;
- cambiar categoría raíz;
- declarar concepto maduro/deprecado.

No requieren aprobación previa, salvo que el usuario indique lo contrario:

- agregar evidencia a bloques `AUTO` de conceptos ya aprobados;
- corregir links/timestamps;
- mejorar formato;
- actualizar conteos automáticos.

## Registro de decisiones conceptuales

Toda decisión durable debe registrarse en:

```txt
docs/DECISIONS.md
```

Formato sugerido:

```md
## YYYY-MM-DD — Título de decisión

Decisión: ...
Motivo: ...
Afecta: ...
Casos/evidencia: ...
```

## Revisión periódica

Cada cierto número de videos, conviene hacer una revisión de ontología:

- cada 5 videos al inicio;
- luego cada 10–20 videos;
- siempre que aparezcan muchas propuestas similares.

Preguntas de revisión:

- ¿Hay conceptos duplicados?
- ¿Hay nombres confusos?
- ¿Un concepto se volvió demasiado grande?
- ¿Un subconcepto merece nota propia?
- ¿Hay conceptos sin evidencia suficiente?
- ¿Hay conceptos con evidencia contradictoria?
