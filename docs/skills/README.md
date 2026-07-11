# Skill local

`aos-gol-lite/` es la única skill específica de este repo. El adapter `.agents/skills` se mantiene como junction estable a esta carpeta para que el harness la descubra.

## Skills AOS portables

Las skills AOS portables, incluido `aos-orquestar` con su prompt de worker y patrón de un worker por repo, viven en la fuente global AOS: C:/dev/os/docs/skills. Usar esa ruta, no una copia local.

## Regla

Las instrucciones durables del vault viven en la documentación del repo; esta skill es una entrada operativa fina, no memoria paralela.
