# CMO Agents

- **Dates:** mar 2026 → jun 2026
- **Status:** En producción para Maiteego
- **Stack:** Python, FastAPI, LangGraph, PostgreSQL, pgvector, Langfuse, Telegram

Un equipo autónomo de marketing de contenidos para Maiteego en siete plataformas: Instagram (feed, reels y stories), TikTok, X, Threads y LinkedIn, con Facebook y Pinterest derivados de ellas.

- Unos 25 jobs programados: scouts de competidores, del sector y de tendencias globales (con análisis de reels mediante modelos de visión), investigación de keywords, un analista de rendimiento y un estratega semanal que deduplica ideas semánticamente contra todo lo publicado antes.
- Producción de imágenes y vídeo, un guionista de reels, un revisor de marca y un adaptador por plataforma, y después la publicación programada.
- Human in the loop en Telegram, con botones de aprobar, editar y rechazar en dos puntos: el plan semanal y cada borrador. No se genera nada caro antes de que esté aprobado.
- Un grafo supervisor con subagentes y una cadena principal y de fallback entre OpenAI, Anthropic, Gemini y Fireworks.

En once semanas produjo 378 borradores, de los que se programaron 65.
