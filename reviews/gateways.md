# 🔀 Gateways reviews · Best of Open-Source AI

LLM gateways and proxies for routing, caching, rate limits and cost control across providers. Back to the [leaderboard](../README.md#-gateways).

<a name="omniroute"></a>
### 🥇 [OmniRoute](https://github.com/diegosouzapw/omniroute) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 75k · MIT · Oct 2026</sub>

**OpenAI-compatible gateway that routes requests across hundreds of AI providers.**

OmniRoute exposes one OpenAI-compatible endpoint at localhost:20128/v1 and routes requests to a catalog of 357+ providers, including many free tiers, with automatic fallback between them. It also accepts Claude, Gemini and Responses API formats, supports MCP and A2A, and has a dashboard for keys, quotas and free-tier usage. Providers are connected with your own accounts or API keys.

- **+** Single endpoint with automatic fallback across many providers and model IDs
- **+** Dashboard page tracks free-tier pools and remaining quota
- **+** Install via npm, Docker or Electron; MIT license
- **+** Documents the free-tier token math and flags providers with risky terms
- **−** Provider count in the README varies (290, 357, 370) across sections
- **−** The 'auto' model needs at least one eligible connected provider to route
- **−** Providers marked tos:avoid, such as Kiro, are excluded from auto routing by default
- **−** Free-tier token estimate depends on third-party limits that change

<sub>no GPU · Docker + Compose · Compose runs Redis, Qdrant · Models: OpenAI API, Claude API, Gemini API, Responses API · port 20128 · [Repo](https://github.com/diegosouzapw/omniroute) · [🌐 Site ↗](https://omniroute.online)</sub>

<a name="litellm"></a>
### 🥈 [LiteLLM](https://github.com/berriai/litellm) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: very easy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 61k · custom license · Oct 2026</sub>

**OpenAI-format gateway and Python SDK for calling 100+ LLM providers.**

LiteLLM translates calls to 100+ providers (OpenAI, Anthropic, Gemini, Bedrock, Azure and others) into the OpenAI format, either as a Python SDK or as a proxy server. The proxy adds virtual keys, spend tracking, guardrails, load balancing and an admin dashboard, and it also exposes A2A agent and MCP server gateways. The README reports 8ms P95 latency at 1k RPS.

- **+** One OpenAI-style API across 100+ providers and many endpoint types
- **+** Proxy includes virtual keys, spend tracking, load balancing and admin dashboard
- **+** Also gateways A2A agents and MCP servers
- **+** Use as a Python library or as a standalone proxy
- **−** License reported as NOASSERTION; an enterprise tier exists, feature split unclear from README
- **−** Proxy listens on port 4000 and its database requirements are not stated in the README excerpt
- **−** Provider coverage varies by endpoint; many providers support only chat-style endpoints
- **−** Python-based, so latency figures depend on the benchmark setup

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL · Models: OpenAI, Anthropic, Gemini, AWS Bedrock, Azure · port 4000 · [Repo](https://github.com/berriai/litellm) · [📖 Docs ↗](https://docs.litellm.ai/docs/simple_proxy) · [🌐 Site ↗](https://www.litellm.ai/ai-gateway)</sub>

<a name="freellmapi"></a>
### 🥉 [freellmapi](https://github.com/tashfeenahmed/freellmapi) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · MIT · Oct 2026</sub>

**OpenAI-compatible router that fails over across free LLM provider tiers.**

FreeLLMAPI exposes one /v1 endpoint (chat, responses, completions, embeddings, images, video, audio) and routes requests across free tiers from 34 providers, plus custom OpenAI-compatible endpoints. Provider keys are AES-256-GCM encrypted in SQLite, per-key RPM/RPD/TPM/TPD counters keep requests under quotas, and a 429 or 5xx triggers fallover to the next model. It also serves Anthropic Messages, Gemini and opt-in Ollama surfaces, and ships a React dashboard and desktop apps.

- **+** Also speaks Anthropic, Gemini and Ollama formats, so Claude Code and Codex CLI connect
- **+** Per-key rate counters and automatic fallover on 429/5xx across providers
- **+** Keys AES-256-GCM encrypted in SQLite; apps only see one unified token
- **+** Runs on Node 20+ at about 40 MB idle RSS, or via Docker
- **−** Free installs get new models 30 days after premium; same-day catalog costs $19/yr
- **−** Single-user by design; no multi-user setup described
- **−** Depends on free tiers that providers can change or retire without notice
- **−** Catalog sync pulls a signed feed from freellmapi.co

<sub>no GPU · Docker + Compose · Needs SQLite, Node 20+, provider API keys · Models: OpenAI-compatible API, Anthropic Messages API, Gemini API, Ollama API · port 3001 · [Repo](https://github.com/tashfeenahmed/freellmapi) · [📖 Docs ↗](https://github.com/tashfeenahmed/freellmapi/blob/main/docs/en/README.md) · [🌐 Site ↗](https://freellmapi.co)</sub>

<a name="mcp-context-forge"></a>
### #&#8288;4 [ContextForge MCP Gateway](https://github.com/ibm/mcp-context-forge) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (90) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs PostgreSQL (production; SQLite for dev), Redis (caching and federation) · Models: A2A agents: OpenAI, Anthropic, custom · port 4444 · [Repo](https://github.com/ibm/mcp-context-forge) · [📖 Docs ↗](https://ibm.github.io/mcp-context-forge/)</sub>

<a name="higress"></a>
### #&#8288;5 [Higress](https://github.com/higress-group/higress) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: fair (78) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker · Models: mainstream LLM providers, domestic and international, via the ai-proxy plugin · port 8001 · [Repo](https://github.com/higress-group/higress) · [▶️ Demo ↗](https://demo.higress.io/) · [📖 Docs ↗](https://higress.cn/en/docs/latest/overview/what-is-higress/) · [🌐 Site ↗](https://higress.ai/en/)</sub>

<a name="bifrost"></a>
### #&#8288;6 [Bifrost](https://github.com/maximhq/bifrost) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Models: OpenAI, Anthropic, AWS Bedrock, Google Vertex, Azure, Cerebras, Cohere, Mistral, Ollama, Groq and more · port 8080 · [Repo](https://github.com/maximhq/bifrost) · [📖 Docs ↗](https://docs.getbifrost.ai)</sub>

<a name="plano"></a>
### #&#8288;7 [Plano](https://github.com/katanemo/plano) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: some setup (33) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker · Needs Plano-Orchestrator routing model (hosted or local) · Models: OpenAI, Anthropic and other providers configured as model_providers · [Repo](https://github.com/katanemo/plano) · [📖 Docs ↗](https://docs.planoai.dev)</sub>

<a name="gomodel"></a>
### #&#8288;8 [GoModel](https://github.com/enterpilot/gomodel) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs Redis, PostgreSQL, MongoDB (Compose infrastructure) · Models: OpenAI, Anthropic, xAI, Gemini, Vertex AI, Cohere, DeepSeek, Groq, Fireworks, OpenRouter, Azure OpenAI, Bedrock, Ollama, SGLang, vLLM, llm-d, ElevenLabs and any OpenAI-compatible provider · port 8080 · [Repo](https://github.com/enterpilot/gomodel) · [▶️ Demo ↗](https://demo.enterpilot.io/admin/dashboard) · [📖 Docs ↗](https://gomodel.enterpilot.io/docs)</sub>

<a name="agentgateway"></a>
### #&#8288;9 [agentgateway](https://github.com/agentgateway/agentgateway) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (30) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker · Models: OpenAI, Anthropic, Gemini, Bedrock and other providers; self-hosted models via inference routing · [Repo](https://github.com/agentgateway/agentgateway) · [📖 Docs ↗](https://agentgateway.dev/docs/standalone/latest)</sub>

<a name="optillm"></a>
### #&#8288;10 [optillm](https://github.com/algorithmicsuperintelligence/optillm) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: fair (73) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU optional · Docker + Compose · Models: OpenAI, Cerebras, Azure OpenAI, any OpenAI-compatible endpoint, LiteLLM providers, local models via the built-in inference server · port 8000 · [Repo](https://github.com/algorithmicsuperintelligence/optillm) · [▶️ Demo ↗](https://huggingface.co/spaces/codelion/optillm)</sub>

<a name="portkey-gateway"></a>
### #&#8288;11 [Portkey Gateway](https://github.com/portkey-ai/gateway) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (60) · Freshness: active (80) · Maintenance: weak (3) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · May 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: OpenAI, Azure OpenAI, Anthropic, Gemini, Cohere, Mistral, Together, Perplexity, Ollama, Bedrock, Groq and 45+ providers · port 8787 · [Repo](https://github.com/portkey-ai/gateway)</sub>

<a name="metamcp"></a>
### #&#8288;12 [MetaMCP](https://github.com/metatool-ai/metamcp) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (7) · Freshness: active (85) · Maintenance: weak (5) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · MIT · Jun 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs PostgreSQL · port 12008 · [Repo](https://github.com/metatool-ai/metamcp) · [📖 Docs ↗](https://docs.metamcp.com)</sub>

<a name="coai"></a>
### #&#8288;13 [CoAI](https://github.com/coaidev/coai) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: known (48) · Freshness: recent (55) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · Mar 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs MySQL, Redis, SearXNG (optional web search), CoAI blob-service (optional file parsing) · Models: OpenAI, Azure OpenAI, Anthropic, Gemini, Midjourney, SparkDesk, Zhipu, Qwen, Hunyuan, Baichuan, Moonshot, DeepSeek, Skylark, Groq, OpenRouter, 360, LocalAI, Ollama · port 8000 · [Repo](https://github.com/coaidev/coai) · [📖 Docs ↗](https://coai.dev/docs/deploy) · [🌐 Site ↗](https://coai.dev)</sub>

<a name="mcpo"></a>
### #&#8288;14 [mcpo](https://github.com/open-webui/mcpo) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: niche (20) · Freshness: recent (62) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · MIT · Feb 2026</sub>

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

<sub>no GPU · Docker · Needs MCP servers to proxy · port 8000 · [Repo](https://github.com/open-webui/mcpo) · [📖 Docs ↗](https://docs.openwebui.com/openapi-servers/open-webui/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
