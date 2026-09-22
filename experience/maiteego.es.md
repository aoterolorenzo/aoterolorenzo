# Maiteego AI

- **Role:** Lead & Co-founder
- **Dates:** oct 2024 → actualidad
- **Location:** Remoto, A Coruña
- **Type:** Jornada completa
- **Stack:** Go, React Native, LangGraph, Kubernetes, ArgoCD, Terraform, PostgreSQL, Grafana LGTM

Maiteego es una app de viajes con IA multiplataforma que planifica itinerarios a medida. Está publicada en App Store, Google Play y la web. Construyo y opero su motor, con dos socios que llevan el diseño y la financiación, y coordino un equipo de cinco personas.

- Un backend en Go donde un solo itinerario mueve hasta 30 goroutines concurrentes repartidas en tres pools de procesamiento.
- Dos clusters de Kubernetes en Hetzner Cloud, GitOps con ArgoCD para más de 30 servicios y observabilidad LGTM completa.
- Un chatbot en LangGraph con cinco agentes especialistas, sobre modelos elegidos con mi propio benchmark de latencia, coste y fiabilidad del tool calling.

## Plataforma

- Dos clusters de Kubernetes en Hetzner Cloud sobre openSUSE MicroOS, uno para la app y otro para datos, en una red privada segmentada con cluster autoscaler.
- Terraform dividido por ciclo de vida, de modo que los volúmenes y los balanceadores de carga se mantienen mientras los servidores se recrean.
- GitOps con ArgoCD para más de 30 servicios como Helm charts, values por entorno para dev, staging y producción, y Sealed Secrets para todos los secretos.
- Servicios de datos operados por nosotros: Crunchy Postgres con backups continuos a S3, ClickHouse, Dragonfly y Redpanda.
- Observabilidad LGTM completa (Prometheus, Grafana, Loki, Tempo) con las tres señales correladas por trace id, y Langfuse para las trazas de LLM.
- Herramientas internas detrás de OAuth2 Proxy con Azure AD, y una tailnet de Headscale autoalojada con ACL declarativas. Cinco postmortems escritos.

## Backend

- Go con Gin y GORM sobre una arquitectura hexagonal, autenticación JWT con rotación de refresh tokens, e inicio de sesión con Google y Apple.
- Un solo itinerario mueve hasta 30 goroutines concurrentes repartidas en tres pools de procesamiento. Las llamadas al LLM pasan por un worker pool basado en tokens con rate limiting sobre Redis.
- Server-sent events para el streaming, pagos con Stripe y RevenueCat, e integraciones con Google Places, TripAdvisor, Viator y Agoda.

## Agentes

- Un chatbot con FastAPI y LangGraph con un supervisor y cinco agentes especialistas (alojamiento, comida, vuelos, visados, lugares), con checkpoints en Postgres.
- Modelos elegidos con mi propio benchmark de tiempo hasta el primer token, throughput, tokens de razonamiento, coste y fiabilidad del tool calling, con un modelo de fallback y un kill switch.
- Cada respuesta se contrasta con proveedores reales, y la calidad la protegen guardas automáticas y un test de alucinaciones evaluado por un LLM.

## App

- Expo y React Native con TypeScript estricto para iOS, Android y web, builds de EAS por entorno con actualizaciones over-the-air, y nueve idiomas.
