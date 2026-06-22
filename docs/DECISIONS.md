# Decisiones del proyecto

Registro de decisiones durables del vault NDE/ECM.

## 2026-06-22 — Vault Markdown como fuente canónica

Decisión: El vault Markdown será la fuente primaria del conocimiento. Obsidian, sitio web, buscador y chat derivarán de esa fuente.

Motivo: mantener portabilidad, trazabilidad y control humano.

Afecta: estructura del proyecto, templates, workflow de casos y conceptos.

## 2026-06-22 — Conceptos nuevos requieren aprobación humana

Decisión: La IA puede proponer conceptos, pero no crear conceptos definitivos del paradigma sin aprobación explícita del usuario.

Motivo: evitar inflación conceptual y preservar criterio humano sobre el nuevo paradigma.

Afecta: `vault/02-conceptos/`, documentos de revisión en `vault/05-preguntas/`.

## 2026-06-22 — Transcripción canónica híbrida

Decisión: Para cada video se preservan YouTube raw y Groq raw, pero el usuario ve una transcripción canónica/readable que combina texto mejorado con timestamps clickeables.

Motivo: preservar trazabilidad sin obligar al usuario a leer transcripciones crudas de baja calidad.

Afecta: `docs/transcription-policy.md`, `docs/canonical-transcript-design.md`, fuentes en `vault/06-fuentes/`.

## 2026-06-22 — Revisión conceptual conversacional con tracks

Decisión: Reemplazar el flujo principal de revisión conceptual con checkboxes por una conversación guiada respaldada por tracks activos en `docs/tracks/`.

Motivo: Los conceptos del paradigma son hipótesis vivas; conversarlos permite ajustar nombres, jerarquías y matices mejor que un formulario rígido.

Afecta: `docs/workflow-url-a-caso.md`, `docs/concept-lifecycle.md`, `docs/topics/concept-governance.md`, `docs/tracks/`.
