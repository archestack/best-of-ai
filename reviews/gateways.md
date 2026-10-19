# 🔀 Gateways reviews · Best of Open-Source AI

LLM gateways and proxies for routing, caching, rate limits and cost control across providers. Back to the [leaderboard](../README.md#-gateways).

<sub>🌐 Also on the web: [Gateways on archestack.com](https://archestack.com/best-of-ai/gateways/), each project on its own page.</sub>

<a name="litellm"></a>
### 🥇 [LiteLLM](https://github.com/berriai/litellm) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: very easy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 62k · custom license · Oct 2026</sub>

**OpenAI-format gateway and Python SDK for calling 100+ LLM providers.**

LiteLLM translates requests in the OpenAI format to more than 100 LLM providers, and runs either as a Python SDK or as a proxy server. The proxy adds virtual keys, spend tracking, guardrails, load balancing and an admin dashboard. It also fronts A2A agents and MCP servers, and the README cites 8ms P95 latency at 1k RPS.

- **+** Covers chat, responses, embeddings, images, audio, batches and rerank endpoints across many providers
- **+** Works as an in-process Python SDK or a standalone proxy server
- **+** Proxy includes virtual keys, spend tracking, guardrails and load balancing
- **+** Also fronts MCP servers and A2A agents through the same gateway
- **−** Endpoint support varies per provider; the README table shows many gaps
- **−** License is detected as NOASSERTION; check the repo's license files before use
- **−** An Enterprise tier exists; the README excerpt does not say which features are paid
- **−** Two SDK packages (litellm, litellm-core) overlap and cannot be installed together

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL · Models: OpenAI, Anthropic, Gemini, AWS Bedrock, Azure · port 4000 · [Repo](https://github.com/berriai/litellm) · [📖 Docs ↗](https://docs.litellm.ai/docs/simple_proxy) · [🌐 Site ↗](https://www.litellm.ai/ai-gateway) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/litellm/)</sub>

<a name="omniroute"></a>
### 🥈 [OmniRoute](https://github.com/diegosouzapw/omniroute) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (99) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · MIT · Oct 2026</sub>

**LLM gateway routing one OpenAI-compatible endpoint across 372 providers.**

OmniRoute is a TypeScript gateway that exposes one endpoint at localhost:20128/v1 and routes requests to 372 providers, including many free tiers, with automatic fallback between them. It accepts OpenAI, Claude, Gemini and Responses API formats, and a dashboard handles keys and free-tier quota tracking. Users bring their own provider accounts; the README's free-token figures are estimates, not a grant.

- **+** Single /v1 endpoint covers 372 providers with automatic fallback to healthy targets
- **+** Dashboard tracks free-tier pools and quota use at /dashboard/free-tiers
- **+** Works with coding CLIs such as Claude Code, Codex, Cline and Cursor via one config
- **+** Installable via npm, Docker or Electron; MIT licensed; includes MCP and A2A support
- **−** Free-token headline is an estimate; provider limits and terms change and can lower it
- **−** Providers flagged tos: avoid are excluded from automatic routing by default
- **−** Fresh install may have no eligible route until you connect a provider account
- **−** Large surface (372 providers, 19 routing strategies) makes setup and review heavy

<sub>no GPU · Docker + Compose · Needs Provider accounts or API keys, Node.js (npm) or Docker · Models: OpenAI API, Claude API, Gemini API, Responses API · port 20128 · [Repo](https://github.com/diegosouzapw/omniroute) · [🌐 Site ↗](https://omniroute.online) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/omniroute/)</sub>

<a name="new-api"></a>
### 🥉 [new-api](https://github.com/quantumnous/new-api) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · AGPL-3.0 · Oct 2026</sub>

**Gateway that unifies LLM providers behind OpenAI, Anthropic and Gemini APIs.**

New API is a Go and Gin gateway that connects upstream providers such as OpenAI, Anthropic, Gemini, Azure OpenAI, AWS Bedrock, Vertex AI, DeepSeek and Qwen. It exposes them through OpenAI Chat/Responses, Anthropic Messages and Gemini endpoints. A web console handles channel routing, users, quotas, pricing and usage logs. It runs on SQLite by default, or on MySQL or PostgreSQL with optional Redis.

- **+** Converts between OpenAI, Anthropic Messages and Gemini request formats via RelayKit
- **+** Channel priorities, weights, retries and multiple upstream keys per channel
- **+** Per-user quotas, subscriptions, usage logs and expression-based pricing
- **+** Starts on SQLite with one container; Compose file adds PostgreSQL and Redis
- **−** AGPL-3.0 with extra terms requiring attribution and a visible project link in modified UIs
- **−** Protocol conversion is not exact; tools and fields may not map across protocols
- **−** Multi-node setups need shared database, secrets and Redis, or rate limits count per node
- **−** Public or resale use brings filing and compliance duties the README leaves to the operator

<sub>no GPU · Docker + Compose · Needs SQLite, MySQL >= 5.7.8 or PostgreSQL >= 9.6, Redis (optional), ClickHouse (optional, log database) · Models: OpenAI, Anthropic, Google Gemini, Azure OpenAI, AWS Bedrock · port 3000 · [Repo](https://github.com/quantumnous/new-api) · [📖 Docs ↗](https://docs.newapi.ai/en/docs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/new-api/)</sub>

<a name="freellmapi"></a>
### #&#8288;4 [freellmapi](https://github.com/tashfeenahmed/freellmapi) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · MIT · Oct 2026</sub>

**OpenAI-compatible router that pools free LLM provider tiers behind one endpoint.**

FreeLLMAPI exposes a single /v1 API (chat, responses, embeddings, images, audio, plus Anthropic Messages, Gemini and Ollama surfaces) and routes requests across free tiers from 34 providers. It stores provider keys AES-256-GCM encrypted in SQLite, tracks RPM/RPD/TPM/TPD per key, and fails over to the next model on 429/5xx. A React dashboard manages keys and the fallback chain; a desktop app is also available.

- **+** Per-key rate counters and automatic failover on 429/5xx across providers
- **+** Covers chat, embeddings, images, video, speech, Anthropic, Gemini and Ollama APIs
- **+** Keys encrypted at rest in SQLite; clients only see one unified token
- **+** Setup commands for Claude Code, Codex, Cursor, Aider and other agents
- **−** Free installs get new models 30 days late; same-day catalog needs $19/yr premium
- **−** Local-first and single-user by design; no multi-user support
- **−** Depends on free-tier quotas that providers change without notice
- **−** Model catalog sync pulls a signed feed from freellmapi.co

<sub>no GPU · Docker + Compose · Needs Node.js 20+, SQLite, Docker (optional), provider API keys · Models: OpenAI-compatible APIs, Anthropic Messages, Gemini API, Ollama API, custom OpenAI-compatible endpoints · port 3001 · [Repo](https://github.com/tashfeenahmed/freellmapi) · [📖 Docs ↗](https://github.com/tashfeenahmed/freellmapi/blob/main/docs/en/README.md) · [🌐 Site ↗](https://freellmapi.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/freellmapi/)</sub>

<a name="mcp-context-forge"></a>
### #&#8288;5 [ContextForge MCP Gateway](https://github.com/ibm/mcp-context-forge) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (90) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · Apache-2.0 · Oct 2026</sub>

**Registry and proxy federating MCP, A2A, REST and gRPC behind one endpoint.**

ContextForge is IBM's Python registry and proxy that federates MCP servers, A2A agents and REST or gRPC APIs into one MCP-compliant endpoint with auth, rate limiting, retries, an Admin UI and OpenTelemetry tracing. It installs from PyPI (mcpgateway on port 4444), as a GHCR container, via Docker Compose with PostgreSQL, Redis and nginx, or with a Helm chart, and virtualizes legacy REST services as MCP tools.

- **+** Federates MCP, A2A, REST and gRPC (via reflection) behind one MCP endpoint
- **+** Transports: HTTP, JSON-RPC, WebSocket, SSE, Streamable HTTP, stdio
- **+** Admin UI with live log viewer; OpenTelemetry to Phoenix, Jaeger, Zipkin
- **+** Helm chart with HPA, Redis clustering and Grafana dashboards
- **−** arm64 containers unsupported in production; Apple Silicon needs Rosetta or PyPI
- **−** Local Docker builds fail without the CI-only wheel closure; pull the GHCR image
- **−** Will not start without generated JWT_SECRET_KEY and AUTH_ENCRYPTION_SECRET
- **−** Large surface: 55+ tables, 40+ plugins, nginx and pgAdmin in the Compose stack

<sub>no GPU · Docker + Compose · Needs PostgreSQL (production; SQLite for dev), Redis (caching and federation) · Models: A2A agents: OpenAI, Anthropic, custom · port 4444 · [Repo](https://github.com/ibm/mcp-context-forge) · [📖 Docs ↗](https://ibm.github.io/mcp-context-forge/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-context-forge/)</sub>

<a name="gomodel"></a>
### #&#8288;6 [GoModel](https://github.com/enterpilot/gomodel) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Oct 2026</sub>

**Go AI gateway with OpenAI and Anthropic APIs, caching and budgets.**

GoModel is a Go AI gateway (install script or container on port 8080) exposing OpenAI-compatible /v1 and Anthropic /v1/messages endpoints in front of OpenAI, Anthropic, Gemini, Bedrock, Azure, Ollama, vLLM, SGLang and more. It adds exact and semantic caching, cost tracking, budgets, rate limits, failover, an MCP gateway, guardrails and a dashboard with playground. Compose adds Redis, PostgreSQL, MongoDB and Prometheus.

- **+** Single Go binary or container; official OpenAI and Anthropic SDKs work unchanged
- **+** Budgets, rate limits, cost tracking and a usage API per user, team or key
- **+** Exact and semantic caching, failover with circuit breakers, provider key rotation
- **+** Dashboard with playground, live request stream, Prometheus and OpenTelemetry
- **−** Prompt compression, intelligent routing and OIDC SSO are in the paid Pro build
- **−** Pre-1.0; roadmap points to an upcoming 0.2.0 release
- **−** Full Compose stack pulls in Redis, PostgreSQL, MongoDB and Prometheus
- **−** Benchmarks against LiteLLM and Portkey are self-run

<sub>no GPU · Docker + Compose · Needs Redis, PostgreSQL, MongoDB (Compose infrastructure) · Models: OpenAI, Anthropic, xAI, Gemini, Vertex AI, Cohere, DeepSeek, Groq, Fireworks, OpenRouter, Azure OpenAI, Bedrock, Ollama, SGLang, vLLM, llm-d, ElevenLabs and any OpenAI-compatible provider · port 8080 · [Repo](https://github.com/enterpilot/gomodel) · [▶️ Demo ↗](https://demo.enterpilot.io/admin/dashboard) · [📖 Docs ↗](https://gomodel.enterpilot.io/docs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gomodel/)</sub>

<a name="bifrost"></a>
### #&#8288;7 [Bifrost](https://github.com/maximhq/bifrost) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Oct 2026</sub>

**Go AI gateway with web UI, fallbacks, budgets and semantic caching.**

Bifrost is a Go AI gateway that fronts 23+ providers (OpenAI, Anthropic, Bedrock, Vertex and more) with one OpenAI-compatible API and drop-in paths for the OpenAI, Anthropic and GenAI SDKs. It starts with npx or Docker on port 8080 with a web UI, and adds fallbacks, load balancing, semantic caching, MCP tool access, virtual keys, budgets and Prometheus metrics. Clustering, guardrails and the MCP gateway are enterprise features.

- **+** Single Go binary via npx or Docker with zero-config web UI on 8080
- **+** Drop-in base URLs for OpenAI, Anthropic and Google GenAI SDKs
- **+** Virtual keys, team budgets, OIDC provisioning and Prometheus metrics
- **+** 11 microsecond added latency at 5k RPS in its own benchmark
- **−** Guardrails, clustering, adaptive load balancing and MCP gateway are enterprise-only
- **−** Benchmarks are self-reported on t3 instances
- **−** 23+ providers, fewer than LiteLLM or Portkey
- **−** Semantic caching needs a vector store backend

<sub>no GPU · Models: OpenAI, Anthropic, AWS Bedrock, Google Vertex, Azure, Cerebras, Cohere, Mistral, Ollama, Groq and more · port 8080 · [Repo](https://github.com/maximhq/bifrost) · [📖 Docs ↗](https://docs.getbifrost.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bifrost/)</sub>

<a name="plano"></a>
### #&#8288;8 [Plano](https://github.com/katanemo/plano) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: easy (50) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

**Envoy-based data plane that routes, traces and guards agent traffic.**

Plano is an Envoy-based proxy for agentic apps: a YAML file declares agents (HTTP servers with an OpenAI chat endpoint), model providers and listeners, and Plano routes each turn to the right agent with its 4B orchestrator model (hosted free or run locally). It also routes LLM calls by model name, alias or preference, captures OpenTelemetry traces with no instrumentation and applies guardrails via filter chains.

- **+** Declarative multi-agent orchestration; agents are plain OpenAI-compatible HTTP servers
- **+** Zero-code OpenTelemetry traces and agentic signals for every request
- **+** Filter chains add moderation, jailbreak checks and memory out of process
- **+** Model routing by name, alias or preference across providers
- **−** Agent routing depends on Plano's own orchestrator model; hosted by default
- **−** Install prerequisites live in external docs; README shows only YAML and curl
- **−** Envoy underneath; heavier than a single-binary proxy
- **−** No port or resource guidance beyond example listeners

<sub>no GPU · Docker · Needs Plano-Orchestrator routing model (hosted or local) · Models: OpenAI, Anthropic and other providers configured as model_providers · [Repo](https://github.com/katanemo/plano) · [📖 Docs ↗](https://docs.planoai.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/plano/)</sub>

<a name="higress"></a>
### #&#8288;9 [Higress](https://github.com/higress-group/higress) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (77) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

**Envoy-based API gateway with LLM proxy plugins and MCP server hosting.**

Higress is a CNCF sandbox API gateway on Istio and Envoy, extended with Wasm plugins in Go, Rust or JS. Its AI plugins proxy mainstream LLM providers with token rate limiting, load balancing, caching and observability, and host remote MCP servers, including ones generated from OpenAPI specs. A Docker all-in-one image exposes the console on 8001 and the gateway on 8080/8443; Helm covers Kubernetes.

- **+** Envoy-based with millisecond config reloads and no connection drops
- **+** Hosts MCP servers with auth, rate limits and audit; OpenAPI-to-MCP converter
- **+** Token rate limiting, multi-model load balancing and caching for LLM routes
- **+** Also a Kubernetes ingress controller and Gateway API implementation
- **−** Images only on Alibaba Cloud registries; pulls can time out outside the mirrors
- **−** Istio and Envoy underneath; heavier than single-binary LLM proxies
- **−** AI features are Wasm plugins on a general API gateway
- **−** Docs split across higress.ai and higress.cn

<sub>no GPU · Docker · Models: mainstream LLM providers, domestic and international, via the ai-proxy plugin · port 8001 · [Repo](https://github.com/higress-group/higress) · [▶️ Demo ↗](https://demo.higress.io/) · [📖 Docs ↗](https://higress.cn/en/docs/latest/overview/what-is-higress/) · [🌐 Site ↗](https://higress.ai/en/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/higress/)</sub>

<a name="agentgateway"></a>
### #&#8288;10 [agentgateway](https://github.com/agentgateway/agentgateway) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · Apache-2.0 · Oct 2026</sub>

**One proxy for LLM, MCP and A2A traffic with auth and RBAC.**

Agentgateway is a Linux Foundation proxy for agent traffic: an LLM gateway (OpenAI-compatible API, budgets, failover), an MCP gateway federating tools over stdio, HTTP, SSE and Streamable HTTP, and an A2A gateway. It adds JWT, API key and OAuth auth, CEL RBAC, rate limits, guardrails and OpenTelemetry, and runs standalone from YAML or as a Kubernetes controller with Gateway API.

- **+** One proxy for LLM, MCP and A2A traffic with an OpenAI-compatible API
- **+** MCP federation over stdio, HTTP, SSE and Streamable HTTP plus OpenAPI tools
- **+** JWT, API key and OAuth auth with CEL-based RBAC and rate limits
- **+** Standalone YAML mode or Kubernetes controller with Gateway API
- **−** README has no install command, ports or resource needs; quickstart is external
- **−** Inference routing assumes Kubernetes Inference Gateway extensions
- **−** Marked in active development; roadmap is the issue tracker
- **−** Guardrail backends beyond regex are cloud services (OpenAI, Bedrock, Model Armor)

<sub>no GPU · Docker · Models: OpenAI, Anthropic, Gemini, Bedrock and other providers; self-hosted models via inference routing · [Repo](https://github.com/agentgateway/agentgateway) · [📖 Docs ↗](https://agentgateway.dev/docs/standalone/latest) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentgateway/)</sub>

<a name="optillm"></a>
### #&#8288;11 [optillm](https://github.com/algorithmicsuperintelligence/optillm) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: fair (61) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Oct 2026</sub>

**OpenAI-compatible proxy applying inference-time reasoning techniques.**

OptiLLM is an OpenAI-compatible proxy (pip or Docker, port 8000) that applies inference-time techniques such as mixture of agents, N-sample selection, self-consistency, MCTS, CePO and MARS to any upstream model, selected by a model-name prefix like moa-gpt-4o-mini. Plugins add an MCP client, memory, PII anonymization, code execution, JSON outputs and provider failover; upstreams are OpenAI, Cerebras, Azure or anything LiteLLM supports.

- **+** 20+ techniques selected by model-name prefix, e.g. moa-gpt-4o-mini
- **+** Per-technique benchmarks listed (MARS +30 points on AIME 2025 with Gemini 2.5 Flash Lite)
- **+** Plugins for MCP client, memory, PII anonymization, code execution, JSON output
- **+** Works with any OpenAI-compatible endpoint; LiteLLM covers other providers
- **−** Techniques multiply upstream calls (bon, MoA, MCTS), raising cost and latency
- **−** Runs on Flask's development server by default
- **−** Decoding techniques (cot_decoding, AutoThink) need the local inference path
- **−** Web search plugin drives Chrome through Selenium

<sub>GPU optional · Docker + Compose · Models: OpenAI, Cerebras, Azure OpenAI, any OpenAI-compatible endpoint, LiteLLM providers, local models via the built-in inference server · port 8000 · [Repo](https://github.com/algorithmicsuperintelligence/optillm) · [▶️ Demo ↗](https://huggingface.co/spaces/codelion/optillm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/optillm/)</sub>

<a name="portkey-gateway"></a>
### #&#8288;12 [Portkey Gateway](https://github.com/portkey-ai/gateway) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: known (44) · Freshness: recent (77) · Maintenance: weak (3) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · May 2026</sub>

**Node.js LLM gateway with fallbacks, load balancing and guardrails.**

Portkey Gateway is a Node.js proxy that routes requests to 250+ LLM providers through an OpenAI-style API on port 8787, runnable with npx, Docker or Cloudflare Workers. Config objects add retries, fallbacks, load balancing, conditional routing, timeouts and 40+ guardrails; a console at /public shows local logs. Semantic caching, prompt management and RBAC are hosted or enterprise features.

- **+** Runs with npx in Node.js; 122 KB footprint, sub-millisecond overhead claimed
- **+** Fallbacks, retries, load balancing, conditional routing and timeouts via config
- **+** 40+ built-in guardrails plus bring-your-own
- **+** Works with OpenAI, LangChain, LlamaIndex, CrewAI and Autogen SDKs
- **−** Semantic caching, prompt management and provider optimization are hosted or enterprise only
- **−** Last commit 2026-05-25; Gateway 2.0 enterprise merge still pre-release
- **−** Docs links are portkey.wiki short links
- **−** RBAC, PII redaction and compliance features are enterprise

<sub>no GPU · Docker + Compose · Models: OpenAI, Azure OpenAI, Anthropic, Gemini, Cohere, Mistral, Together, Perplexity, Ollama, Bedrock, Groq and 45+ providers · port 8787 · [Repo](https://github.com/portkey-ai/gateway) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/portkey-gateway/)</sub>

<a name="metamcp"></a>
### #&#8288;13 [MetaMCP](https://github.com/metatool-ai/metamcp) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (5) · Freshness: active (82) · Maintenance: weak (3) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · MIT · Jun 2026</sub>

**Aggregates MCP servers into namespaced endpoints with auth and middleware.**

MetaMCP groups MCP servers into namespaces and publishes each as one MCP endpoint over SSE, Streamable HTTP or OpenAPI, with API-key or OAuth auth, per-tool toggles, name overrides and middleware. It runs with Docker Compose beside PostgreSQL on port 12008, adds OIDC SSO, multi-tenancy and rate limits, and includes an inspector with saved configs. The author reports maintenance delays.

- **+** Namespaces group servers, toggle tools and override names and annotations
- **+** Endpoints over SSE, Streamable HTTP and OpenAPI with API key or MCP OAuth
- **+** OIDC SSO, multi-tenancy and registration controls for organizations
- **+** Built-in inspector with saved server configs
- **−** Author notes maintenance delays; a community fork exists
- **−** Endpoints are remote-only; stdio clients like Claude Desktop need mcp-proxy
- **−** Rate-limit counters are in-memory per instance, not cluster-wide
- **−** MCP servers needing more than uvx or npx require a custom Dockerfile

<sub>no GPU · Docker + Compose · Needs PostgreSQL · port 12008 · [Repo](https://github.com/metatool-ai/metamcp) · [📖 Docs ↗](https://docs.metamcp.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/metamcp/)</sub>

<a name="mcpo"></a>
### #&#8288;14 [mcpo](https://github.com/open-webui/mcpo) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (13) · Freshness: recent (59) · Maintenance: weak (0) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · MIT · Feb 2026</sub>

**Exposes any MCP server as an OpenAPI HTTP endpoint.**

mcpo wraps an MCP server command, SSE or Streamable HTTP endpoint and exposes its tools as an OpenAPI REST server on port 8000 with generated docs, so HTTP clients such as Open WebUI can call MCP tools. A Claude Desktop-style config serves several servers under separate routes with hot reload; OAuth 2.1 dynamic client registration handles protected upstreams. Runs via uvx, pip or Docker.

- **+** One command turns any MCP server into an OpenAPI server with /docs
- **+** stdio, SSE and Streamable HTTP upstreams; OAuth 2.1 with dynamic registration
- **+** Config file in Claude Desktop format with hot reload
- **+** Docker image and --root-path for reverse proxies
- **−** Last commit 2026-02-27
- **−** Single shared API key; no users or RBAC
- **−** Converts to OpenAPI only; does not aggregate servers into one MCP endpoint
- **−** Python 3.8+ process per deployment; no clustering

<sub>no GPU · Docker · Needs MCP servers to proxy · port 8000 · [Repo](https://github.com/open-webui/mcpo) · [📖 Docs ↗](https://docs.openwebui.com/openapi-servers/open-webui/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcpo/)</sub>

<a name="coai"></a>
### #&#8288;15 [CoAI](https://github.com/coaidev/coai) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: known (35) · Freshness: recent (52) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · Mar 2026</sub>

**Multi-user chat site plus OpenAI-compatible proxy with billing.**

CoAI pairs a multi-user chat frontend with an OpenAI-compatible API proxy and billing for operators of commercial AI sites. A Go backend on MySQL and Redis routes across channels with priority, weight, retries and model redirection for OpenAI, Anthropic, Gemini, Midjourney, Ollama and more; the React UI adds file parsing, SearXNG search and image generation. Docker Compose serves it on port 8000.

- **+** Chat UI and OpenAI-compatible proxy in one deployment
- **+** Channel priorities, weights, retries and model redirection for routing
- **+** Subscription and per-token billing with gift and redemption codes
- **+** Midjourney, DALL-E and Stable Diffusion image generation in chat
- **−** Default admin login root / chatnio123456 must be changed after deploy
- **−** RAG, TTS/STT, OAuth login and rate limiting are in the paid Pro version
- **−** Needs MySQL and Redis
- **−** Last commit 2026-03-12

<sub>no GPU · Docker + Compose · Needs MySQL, Redis, SearXNG (optional web search), CoAI blob-service (optional file parsing) · Models: OpenAI, Azure OpenAI, Anthropic, Gemini, Midjourney, SparkDesk, Zhipu, Qwen, Hunyuan, Baichuan, Moonshot, DeepSeek, Skylark, Groq, OpenRouter, 360, LocalAI, Ollama · port 8000 · [Repo](https://github.com/coaidev/coai) · [📖 Docs ↗](https://coai.dev/docs/deploy) · [🌐 Site ↗](https://coai.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/coai/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
