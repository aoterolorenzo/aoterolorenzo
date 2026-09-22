# CMO Agents

- **Dates:** Mar 2026 → Jun 2026
- **Status:** Used in production for Maiteego
- **Stack:** Python, FastAPI, LangGraph, PostgreSQL, pgvector, Langfuse, Telegram

An autonomous content marketing team for Maiteego across seven platforms: Instagram (feed, reels and stories), TikTok, X, Threads and LinkedIn, with Facebook and Pinterest derived from them.

- About 25 scheduled jobs: scouts for competitors, the sector and global trends (including reel analysis with vision models), keyword research, a performance analyst and a weekly strategist that deduplicates ideas semantically against everything published before.
- Production of images and video, a reel scriptwriter, a brand reviewer and an adapter per platform, then scheduled publishing.
- Human in the loop on Telegram, with approve, edit and reject buttons at two points: the weekly plan and every draft. Nothing expensive is generated before it is approved.
- A supervisor graph with sub-agents and a primary and fallback chain across OpenAI, Anthropic, Gemini and Fireworks.

In eleven weeks it produced 378 drafts, of which 65 were scheduled.
