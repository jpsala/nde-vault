---
id: pi-extension-stack
status: active
kind: reference
triggers:
  - extensiones pi
  - paquetes pi
  - pi packages
  - sincronizar pi
  - web_search
  - web_research
  - codemapper
  - fff
  - fffind
  - ffgrep
  - taskflow
  - advisor
  - pi-lens
primary_refs:
  - docs/topics/pi-agentic-os.md
  - docs/OS_PLAYBOOK.md
  - C:/dev/os/docs/topics/pi-extension-stack.md
  - C:/dev/os/docs/topics/agent-tool-routing.md
  - C:/dev/os/docs/reference/tool-routing.yaml
---

# Pi Extension Stack

Referencia local para elegir herramientas Pi en `nde`. El inventario global de
paquetes y routing completo vive en `C:/dev/os`; no duplicarlo acá ni tratarlo
como dependencia local del vault.

## Regla Operativa

1. Elegir la herramienta más chica que cierre el objetivo.
2. Usar web cuando conocimiento externo/versionado evite adivinar.
3. Antes de instalar/remover paquetes globales, pedir permiso y hacer backup de
   `C:/Users/jpsal/.pi/agent/settings.json`.
4. No tocar prod, cuentas reales, credenciales, envíos, deploys ni datos
   privados sin aprobación explícita.

## Superficie Operativa Local

| Nivel | Tools | Uso |
| --- | --- | --- |
| Core diario | `fffind`, `ffgrep`, CodeMapper (`map/search/outline`), `ask_user`, `lens_diagnostics` | Orientación local, búsqueda, feedback técnico y checks. |
| Decisiones fuertes | `advisor` | Arquitectura/storage/prod/security, decisiones `DECISIONS.md`-worthy o loops largos. No usarlo para orientación barata, checks ni pasos chicos ya decididos. |
| Orquestación | `taskflow`, council, `pi-link` si aplica | Auditorías/reviews paralelas con ownership claro; no para trabajo serial chico. |
| Ejecución larga | planner, `/until-done`, `pi_long_task`; `dgoal` solo experimental | Elegir **uno** desde `/aos-plan-implementar`; para fleet updates AOS usar `pi_long_task`/`/aos-fleet-update` desde `C:/dev/os`, no `dgoal`. |
| Research externo | `web_search`, `fetch_content`, `web_answer`, `web_research`, skill `librarian` | Docs oficiales, releases, APIs, issues e internals OSS; no enviar secretos. |
| Piloto opt-in | `pi-dynamic-workflows` solo si JP lo pide explícitamente | Comparar fan-out pesado contra `taskflow`; trigger seguro `pi-workflow`, no reemplazo default. |

## Planning Y Ejecución

Usar `/aos-plan-implementar` para elegir un motor principal: manual, planner,
`dgoal`, `/until-done`, `pi_long_task` o taskflow. Para multi-repo AOS/fleet,
lanzar `/aos-fleet-update` desde `C:/dev/os` o armar un `pi_long_task` serial con
las mismas reglas: sin writers paralelos, sin `dgoal`, sin push y con dirty state
preexistente preservado.
