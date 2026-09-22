# Crank

- **Dates:** 2026 → actualidad
- **Status:** Activo
- **Stack:** Python, Claude Code, GLM, YAML pipelines

Un ejecutor de pipelines para agentes de código en el que deciden los gates, no el modelo.

Cada tarea pasa por requisitos escritos en EARS, diseño, tareas, implementación, validación, una fase "metahuman" y documentación. Cada fase termina en una revisión adversarial a cargo de un revisor de solo lectura: un hallazgo de severidad media o superior devuelve la fase atrás, con la revisión como feedback. Unos validadores de fidelidad comprueban los requisitos contra el código existente, el diseño contra los requisitos y la implementación contra la spec, y la suite de tests real actúa como gate mecánico.

## Metahuman

La fase que viene después de todos los quality gates, tests y umbrales de cobertura. Un agente prueba la funcionalidad como lo haría un ingeniero de QA: abre Chrome y la usa, lee capturas de pantalla, llama a la API y busca casos límite. No puede tocar el código, y la severidad de cada hallazgo decide a qué punto vuelve la tarea.

## Detalles

- Las pipelines y los backends de modelo se declaran en YAML, con Claude Code y GLM como backends.
- Un panel web sigue varios proyectos a la vez.
- 94% de cobertura de tests.
