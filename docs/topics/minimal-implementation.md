---
id: minimal-implementation
status: active
kind: how-to
triggers:
  - ponytail
  - minimal implementation
  - implementacion minima
  - solucion minima
  - yagni
  - over-engineering
  - bloat
  - boilerplate
  - dependencias innecesarias
  - diff minimo
  - revisar complejidad
primary_refs:
  - AGENTS.md
  - docs/topics/agentic-os-local.md
  - docs/topics/agentic-os-operations.md
  - docs/topics/pi-agentic-os.md
---

# Implementacion Minima Y Ponytail

AOS puede usar disciplina minimalista para implementar o revisar cambios, pero no la convierte en gobierno obligatorio del sistema.

## Regla local

AOS gobierna contexto, memoria durable, continuidad, trazabilidad, aprobaciones humanas, verificaciones, ask-before y seguridad downstream. La disciplina minimalista gobierna solo la forma de implementar una solucion una vez entendido el flujo y las reglas del repo.

Antes de escribir codigo o docs nuevos, preferir en este orden:

1. No construir si la necesidad es especulativa.
2. Reusar patrones, scripts, topics o convenciones existentes del repo.
3. Usar Markdown/docs simples cuando alcancen.
4. Usar stdlib o capacidades nativas de la plataforma.
5. Usar dependencias ya instaladas.
6. Resolver con el diff mas chico que siga siendo correcto, trazable y mantenible.
7. Solo entonces escribir codigo nuevo minimo.

La escalera corre despues de leer el contexto necesario. Un diff chico en el lugar equivocado no es una mejora.

## Ponytail

Ponytail (`DietrichGebert/ponytail`) queda aprobado solo como capacidad opcional / modo bajo demanda para implementacion y review minimalista.

Uso recomendado:

- bugs y fixes con root cause compartida;
- refactors pequenos;
- reviews de over-engineering;
- reduccion de dependencias, wrappers, boilerplate o abstracciones especulativas;
- auditorias read-only del tipo "que podemos borrar/simplificar".

No usarlo como regla obligatoria always-on en AOS ni en este repo. No instalar paquetes ni agregar dependencias locales de Ponytail salvo pedido explicito.

## No recortar

Nunca simplificar quitando:

- trazabilidad a fuentes, citas o timestamps;
- separacion entre fuente, interpretacion y patron;
- aprobacion humana para conceptos definitivos o cambios conceptuales fuertes;
- validacion en limites de confianza;
- manejo de errores que evita perdida de datos;
- seguridad o proteccion de secretos;
- memoria durable, topics, tracks o docs necesarios para continuidad AOS;
- requisitos explicitamente pedidos por JP.

## Uso downstream

En este repo, esta politica viaja como regla liviana subordinada a AOS. Si se invoca Ponytail o una revision minimalista, reportar que fue usada como apoyo opcional y mantener las validaciones normales del proyecto.
