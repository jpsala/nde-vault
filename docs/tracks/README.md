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
