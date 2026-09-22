# Agent Jungle

- **Dates:** 2026
- **Status:** Prototipo funcional
- **Stack:** Python, Claude Agent SDK, Mattermost

Un pueblo de agentes de Claude Code que viven en Mattermost. Cada carpeta es un agente y su CLAUDE.md es su identidad; cada hilo de Mattermost es una sesión.

- Personas y agentes hablan entre sí mediante menciones. Un planificador de mesa decide quién habla en cada hilo, y solo los mensajes humanos abren una ronda nueva, así que los agentes nunca entran en bucle.
- Las reuniones tienen un objetivo, participantes y un número fijo de rondas, y terminan en un informe.
- Las aprobaciones de herramientas llegan como preguntas en el hilo.
- Los hooks de Claude Code replican las sesiones de terminal en el chat, lo que convierte Mattermost en el registro permanente del trabajo.
