# AOS Playbook local

Guia breve para aprovechar Agentic OS en este repo desde conversacion y Pi.

## Modelo

AOS es la capa de operacion para agentes: reglas, memoria durable, topics, tracks, skills, scripts y adapter Pi. La memoria principal esta en docs/vault, no en el transcript del chat.

Ruta normal:

```txt
docs/.generated/context-index.md -> docs/WORKING_MEMORY.md -> docs/TOPICS.md -> topic/doc puntual -> vault/scripts
```

## Comandos conversacionales

| Frase | Uso |
| --- | --- |
| `aos-sigamos` | Continuar en la misma sesion. |
| `aos-gol` / `aos-gol-lite` | Ejecutar el proximo lote chico verificable sin `/until-done` salvo pedido. |
| `aos-guardar-sesion` | Guardar valor durable en docs, sin transcript. |
| `aos-nueva-sesion` | Guardar y preparar una sesion nueva con handoff. |
| `aos-siguiente` | Nueva sesion y pedir que arranque con `aos-gol`. |
| `aos-perfect-os` | Optimizar docs/contexto/comandos/audit. |
| `aos-realinear-os` | Reparar drift de la capa agentica local. |
| `aos-orquestar` / `aos-fanout` | Usar subagentes cuando haya frentes independientes. |

## Slash commands Pi

Estos existen porque el repo incluye `.pi/`:

- `/aos-help`
- `/aos-guardar-sesion`
- `/aos-nueva-sesion`
- `/aos-nueva-sesion-con-gol`
- `/aos-sync`
- `/aos-status audit`
- `/aos-compact`
- `/aos-continuar`
- `/aos-skills status|on|off|toggle`
- `/aos-gol`
- `/aos-orquestar`
- `/aos-fanout`

Si no aparecen, ejecutar `/reload`. Despues de cambios de OS, usar `/aos-sync`.

## Guardrails NDE

- No leer ni exponer `.env`.
- No tocar `.tmp/`, audios, raw transcripts ni `vault/.obsidian/plugins/` salvo pedido explicito.
- No crear conceptos definitivos sin aprobacion humana.
- Mantener trazabilidad a casos, citas y timestamps.
