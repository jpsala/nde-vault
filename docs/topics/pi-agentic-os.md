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
  - /aos-gol
  - /aos-orquestar
  - /aos-fanout
  - continuar sesion
  - computer use
  - cua-driver
  - background computer use
  - web research
  - internet
  - instalar paquetes
  - instalar cli
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

## Web, Internet E Instalaciones

- Usar web/internet libremente por defecto cuando conocimiento externo o cambiante evite adivinar: documentacion oficial, changelogs/releases, issues/source, metadata de paquetes, errores, APIs, ejemplos y comparativas.
- Si evidencia online contradice el repo local, docs del proyecto o comportamiento observado, pausar y consultar a JP antes de decidir; presentar ambas evidencias con fuentes y el impacto practico.
- No enviar secretos, `.env`, codigo privado sensible, datos personales ni credenciales a servicios externos.
- Priorizar fuentes oficiales y citar fuentes cuando afecten decisiones tecnicas.
- Antes de instalar dependencias, CLIs globales, paquetes de sistema, herramientas de package-manager o binarios/scripts remotos, pedir autorizacion explicita con comando exacto, alcance, motivo, riesgos, alternativa, cambios esperados y rollback.
- Tratar `curl | sh`, binarios remotos y scripts de instalacion no auditados como alto riesgo; preferir package managers, checksums, docs oficiales o pasos inspeccionables.

## Regla local

- `.pi/` viaja por defecto en repos de JP salvo razon explicita para omitirlo.
- No contiene secretos; es un shim fino sobre docs/scripts locales.
- `docs/skills/` conserva solo `aos-gol-lite`; `.agents/skills` debe mantenerse como junction estable para descubrirla. Las skills AOS portables se resuelven desde `C:/dev/os/docs/skills/`; los `/aos-*` visibles vienen de `.pi/prompts/`, `.pi/extensions/` y/o skills.
- Si se agregan o cambian prompts/extensiones/skills, correr `/reload` en Pi y luego `/aos-sync`.

## Comandos clave

| Comando | Uso |
| --- | --- |
| `/aos-help` | Ver comandos AOS locales. |
| `/aos-guardar-sesion` | Persistir valor durable en docs sin transcript. |
| `/aos-sync` | Regenerar index/audit y revisar skills link. |
| `/aos-status audit` | Ver estado operativo y audit. |
| `/aos-continuar [objetivo]` | Abrir una sesión nueva desde docs vivos; `--preview` permite revisar antes de enviar. |
| `/aos-plan-implementar` | Planificar/ejecutar eligiendo un solo motor principal. |
| `/aos-gol` | Preparar un `/until-done` acotado cuando se quiera loop revisable. |
| `/aos-orquestar` / `/aos-fanout` | Usar subagentes/threads cuando aporte valor real. |
| `/aos-fleet-update` | Para fleet AOS, lanzarlo desde `C:/dev/os`; usa `pi_long_task`, no `dgoal`. |

## Checks

```powershell
bun scripts/context-index.ts
bun scripts/agent-context-audit.ts
powershell -ExecutionPolicy Bypass -File scripts/ensure-skills-link.ps1
```

## Routing Pi

- Para trabajos medianos/grandes, elegir un motor principal con `/aos-plan-implementar` y documentar el routing si importa.
- `advisor()` queda reservado para arquitectura/storage/prod/security, decisiones `DECISIONS.md`-worthy o loops largos; no usarlo para orientación barata, checks ni pasos chicos de un playbook decidido.
- Para fleet updates AOS usar `pi_long_task`/`/aos-fleet-update` desde `C:/dev/os`, no `dgoal`.
- `pi-dynamic-workflows` es solo piloto opt-in con trigger seguro; no reemplaza por defecto a `taskflow`.

Routing GPT-5.6: Sol medium para Pi normal/plan compacto; Sol high para
planificacion, arquitectura, advisor y conformidad; Luna medium para mecanica
barata; Luna xhigh para implementacion background acotada, con retry Luna max;
Terra high para implementacion interactiva sensible a latencia; Terra max para
alta garantia, validado por Sol xhigh. Tests, conformidad y riesgo prevalecen
sobre costo. Los cambios de settings requieren reload o sesion nueva cuando
aplique.

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

