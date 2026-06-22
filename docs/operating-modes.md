# Modos de operación del proyecto

## Modo actual: manual/asistido por chat

Vamos a empezar sin interfaz propia.

Motivos:

- permite aprender qué datos importan realmente;
- evita construir una UI prematura;
- facilita ajustar prompts, categorías y templates;
- permite curaduría humana desde el inicio;
- mantiene el vault como centro.

## Cómo trabajamos

1. El usuario pasa una URL o idea por chat.
2. El agente procesa o registra la fuente.
3. El agente crea/actualiza archivos Markdown.
4. El usuario revisa en Obsidian.
5. Ajustamos criterios y templates.
6. Cuando el proceso sea estable, automatizamos con scripts.
7. Recién después diseñamos interfaz/chat/web.

## Cuándo automatizar

Automatizar cuando hayamos repetido manualmente el proceso suficientes veces para conocer:

- estructura real de casos;
- conceptos recurrentes;
- formato útil de citas;
- problemas de transcripción;
- criterios de calidad;
- necesidades de revisión humana.

## Futuras interfaces

Posibles capas futuras:

- CLI: `process-youtube-url <url>`;
- panel local para revisar propuestas;
- plugin o flujo compatible con Obsidian;
- sitio web de lectura;
- chat RAG con referencias al vault.
