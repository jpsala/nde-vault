---
status: active
started: 2026-06-22
updated: 2026-06-22
priority: medium
---

# Tracks

Carpeta para trabajos vivos retomables.

## Frontmatter obligatorio

```yaml
---
status: active | paused | blocked | archived
started: YYYY-MM-DD
updated: YYYY-MM-DD
priority: low | medium | high
---
```

## Regla

Una track debe ser estado resumido y retomable, no transcript. Si se cierra, mover a `docs/tracks/archive/` con `status: archived`.

## Tracks conceptuales NDE

Para revisión conceptual de un caso/video, crear tracks como:

```txt
docs/tracks/conceptos-caso-XXXX-<slug>.md
```

Deben contener:

- caso/fuente activa;
- archivos relevantes;
- lectura conceptual inicial;
- preguntas abiertas;
- decisiones conversacionales;
- próximos pasos para retomar.

No deben reemplazar a las notas definitivas de conceptos en `vault/02-conceptos/` ni a los casos en `vault/01-casos/`.
