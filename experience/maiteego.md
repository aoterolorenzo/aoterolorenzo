# Maiteego AI

- **Role:** Lead & Co-founder
- **Dates:** Oct 2024 → present
- **Location:** Remote, A Coruña
- **Type:** Full-time
- **Stack:** Go, React Native, LangGraph, Kubernetes (RKE2), ArgoCD, Terraform, PostgreSQL, Grafana LGTM

Maiteego is a multiplatform AI travel app that plans tailor-made itineraries. It is live on the App Store, Google Play and the web. I build and run its engine, with two partners on design and funding, and I coordinate a team of five.

- A Go backend where a single itinerary drives up to 30 concurrent goroutines across three processing pools.
- Two RKE2 clusters on Hetzner Cloud, GitOps with ArgoCD for more than 30 services, and full LGTM observability.
- A LangGraph chatbot with five specialist agents, on models chosen with my own benchmark of latency, cost and tool-calling reliability.

## Platform

- Two RKE2 clusters on Hetzner Cloud over openSUSE MicroOS, one for the app and one for data, on a segmented private network with a cluster autoscaler.
- Terraform split by lifecycle, so volumes and load balancers survive while servers are recreated.
- GitOps with ArgoCD for more than 30 services as Helm charts, per-environment values for dev, staging and production, and Sealed Secrets for every secret.
- Operated data services: Crunchy Postgres with continuous backups to S3, ClickHouse, Dragonfly and Redpanda.
- Full LGTM observability (Prometheus, Grafana, Loki, Tempo) with the three signals correlated by trace id, and Langfuse for LLM traces.
- Internal tools behind OAuth2 Proxy with Azure AD, and a self-hosted Headscale tailnet with declarative ACLs. Five postmortems written.

## Backend

- Go with Gin and GORM on a hexagonal architecture, JWT auth with refresh rotation, and Google and Apple sign-in.
- A single itinerary drives up to 30 concurrent goroutines across three processing pools. LLM calls go through a token-based worker pool with rate limiting on Redis.
- Server-sent events for streaming, Stripe and RevenueCat payments, and integrations with Google Places, TripAdvisor, Viator and Agoda.

## Agents

- A FastAPI and LangGraph chatbot with a supervisor and five specialist agents (stays, food, flights, visas, spots), checkpointed in Postgres.
- Models chosen with my own benchmark of time to first token, throughput, reasoning tokens, cost and tool-calling reliability, with a fallback model and a kill switch.
- Every answer is checked against real providers, and automatic guards plus an LLM-judged hallucination test protect quality.

## App

- Expo and React Native with strict TypeScript for iOS, Android and web, EAS builds per environment with over-the-air updates, and nine languages.
