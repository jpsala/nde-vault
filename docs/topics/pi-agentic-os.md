---
id: pi-agentic-os
status: active
kind: how-to
triggers:
  - pi
  - pi os
  - slash commands
  - /aos-sync
  - /aos-guardar-sesion
  - /aos-nueva-sesion
  - /aos-gol
  - /aos-orquestar
  - /aos-fanout
  - continuar sesion
  - computer use
  - cua-driver
  - background computer use
primary_refs:
  - .pi/prompts/
  - .pi/extensions/aos-tools.ts
  - .pi/extensions/aos-checkpoint-nudge.ts
  - docs/OS_PLAYBOOK.md
  - scripts/context-index.ts
  - scripts/agent-context-audit.ts
---

# Pi Agentic OS local

Este proyecto incluye el adapter Pi porque JP opera sus repos desde Pi y los comandos conversacionales/slash son parte del valor practico de AOS.

## Regla local

- `.pi/` viaja por defecto en repos de JP salvo razon explicita para omitirlo.
- No contiene secretos; es un shim fino sobre docs/scripts locales.
- `docs/skills/` no aparece como slash por si solo cuando el discovery global esta apagado; los `/aos-*` visibles vienen de `.pi/prompts/` y `.pi/extensions/`.
- Si se agregan o cambian prompts/extensiones, correr `/reload` en Pi y luego `/aos-sync`.

## Comandos clave

| Comando | Uso |
| --- | --- |
| `/aos-help` | Ver comandos AOS locales. |
| `/aos-guardar-sesion` | Persistir valor durable en docs sin transcript. |
| `/aos-nueva-sesion` | Guardar y abrir una sesion limpia con handoff. |
| `/aos-continuar-sesion` | Alias legado de `/aos-nueva-sesion`; tambien guarda y abre sesion. |
| `/aos-nueva-sesion-con-gol` | Guardar, abrir sesion limpia y arrancar con lote chico. |
| `/aos-continuar-con-gol` / `/aos-siguiente` | Aliases de `/aos-nueva-sesion-con-gol`. |
| `/aos-sync` | Regenerar index/audit y revisar skills link. |
| `/aos-status audit` | Ver estado operativo y audit. |
| `/aos-gol` | Preparar un `/until-done` acotado cuando se quiera loop revisable. |
| `/aos-orquestar` / `/aos-fanout` | Usar subagentes/threads cuando aporte valor real. |

## Checks

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
```
## Computer Use Local / Background

Usar computer use solo cuando APIs, tests o browser/DOM no alcancen para validar una UI real. No convertirlo en requisito duro del repo: la infraestructura global de JP vive en `C:\dev\infra`; hoy incluye Cua Driver global via Pi MCP `cua-driver` en modo `eager`/persistente (tras `/reload` o reinicio), y puede incluir browser remoto o VM segun la maquina.

Politica local:

- Documentar la superficie permitida antes de automatizar: app fixture, sandbox, browser remoto, VM o ventana especifica.
- Preferir fixtures efimeras y datos de prueba; no operar sobre documentos, cuentas o apps reales sin confirmacion de JP.
- Mantener evidencia externa: archivo resultado, screenshot, log, estado de DB o comando de verificacion. No alcanza con decir que se clickeo.
- Orden recomendado: API/test directo -> Playwright/DOM/browser tool -> Cua/UIA background -> computer-use visual por screenshots/VM. Subir de nivel solo cuando el anterior no cubre el caso.
- Pedir confirmacion con `ask_user` antes de login, pagos, compras, envios, publicaciones, cambios productivos, aceptacion de terminos, instalar drivers, habilitar autostart/RunLevel Highest, exponer VNC/noVNC o abrir tunnels.
- Cerrar procesos/ventanas y limpiar temporales al finalizar. Registrar limitaciones conocidas por control (por ejemplo combos/selects) en el topic o track del trabajo.

Smoke test minimo por repo:

1. Crear fixture/app efimera con inputs, boton y salida verificable.
2. Lanzarla con computer use sin robar foreground cuando aplique.
3. Leer accessibility tree/screenshot antes de actuar.
4. Completar campos y disparar accion final.
5. Verificar salida por comando/archivo/API y documentar gotchas.
6. Cerrar procesos y borrar datos temporales si corresponde.

Patron probado para E2E real de producto:

- Referencia actual: `C:/dev/dictation-tauri/scripts/desktop-dictation-e2e.ps1`, passing report `artifacts/desktop-control/dictation-e2e/20260624-104246/report.json`.
- Separar aprobaciones por flags: side effects desktop, provider/cloud call y clipboard/paste mutation.
- Usar target fixture editable o sandbox real con salida externa verificable; guardar live output fuera del repo si el dev server watch-ea artifacts y copiarlo al final.
- Validar cadena completa, no solo UI: driver health, app launch, target foreground, trigger/hotkey, input controlado, artifact fresco, provider/runtime, delivery, clipboard restoration y cleanup.
- El reporte versionable/ignorado debe guardar rutas, hashes/longitudes/tokens esperados y checks; no guardar raw transcript, secretos ni contenido privado en docs/chat.

