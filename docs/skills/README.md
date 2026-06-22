# Skills locales

Fuente local de skills portables para harnesses compatibles. El adapter `.agents` puede apuntar a esta carpeta si se habilita discovery; por defecto puede estar ausente.

## Skills incluidas

- `aos-help/`: mostrar comandos AOS útiles.
- `aos-guardar-sesion/`: persistir valor durable en docs.
- `aos-sigamos/`: continuar en la sesión actual.
- `aos-gol-lite/`: ejecutar un lote chico verificable sin `/until-done`.
- `aos-perfect-os/`: optimizar la capa agentica local.
- `aos-realinear-os/`: auditar/reparar drift de contexto local.
- `aos-init-os/`, `aos-adopt-os/`, `aos-update-os/`: operaciones AOS bajo demanda.
- `aos-orquestar/`, `aos-fanout/`: fan-out controlado cuando el harness lo soporte.

## Regla

Las instrucciones durables deben vivir en la carpeta docs; las skills son entrada operativa fina, no memoria paralela.
