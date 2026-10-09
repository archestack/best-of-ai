# 🔀 Gateways reviews · Best of Self-Hosted AI

LLM gateways and proxies for routing, caching, rate limits and cost control across providers. Back to the [leaderboard](../README.md#-gateways).

<a name="omniroute"></a>
### [🥇 86](../README.md#-how-we-rank "Score 86/100 (gold, 80+). Adoption 93 · Freshness 100 · Maintenance 98 · Easy to run 67 · Agent-ready 70 (each out of 100, weighted). Click for how we rank.") [OmniRoute](https://github.com/diegosouzapw/omniroute) <sub>⭐ 74k · MIT · Oct 2026</sub>

**Free-tier-aware AI gateway routing coding agents across 350+ providers.**

OmniRoute is a Node.js gateway (npm, Docker or Electron app) exposing one OpenAI, Claude, Gemini and Responses-compatible endpoint on port 20128 in front of 350+ providers, 150+ with free tiers, with automatic fallback and 19 routing strategies. It targets coding agents such as Claude Code, Codex, Cursor and Cline, adds RTK and Caveman prompt compression and tracks free-tier quotas on a dashboard.

- **+** Zero-config start: a keyless provider answers model auto right after install
- **+** OpenAI, Claude, Gemini and Responses API compatibility at one /v1 endpoint
- **+** Prompt compression (RTK plus Caveman) claims 15 to 95 percent token savings
- **+** Dashboard tracks free-tier quota use per provider pool
- **−** Provider counts in the README disagree (357 vs 364) and change every two weeks
- **−** Free-token headline depends on third-party tiers; 13 providers flagged as terms risk
- **−** README is mostly marketing graphics; architecture lives in docs
- **−** Compression and routing claims are self-reported

<sub>no GPU · Docker + Compose · Models: 350+ providers incl. free tiers (OpenCode Free, Groq, Mistral) via OpenAI, Claude and Gemini-style APIs · port 20128 · [Repo](https://github.com/diegosouzapw/omniroute) · [🌐 Site ↗](https://omniroute.online)</sub>

<a name="litellm"></a>
### [🥇 84](../README.md#-how-we-rank "Score 84/100 (gold, 80+). Adoption 88 · Freshness 100 · Maintenance 83 · Easy to run 83 · Agent-ready 30 (each out of 100, weighted). Click for how we rank.") [LiteLLM](https://github.com/berriai/litellm) <sub>⭐ 60k · NOASSERTION · Oct 2026</sub>

**Proxy and SDK that calls 100+ LLM providers in OpenAI format.**

LiteLLM is a Python AI gateway that calls 100+ providers (OpenAI, Anthropic, Gemini, Bedrock, Azure and more) in OpenAI format, as a library or as a proxy server on port 4000. The proxy adds virtual keys, spend tracking, guardrails, load balancing and an admin dashboard, plus an MCP gateway and A2A agent routing. Endpoints cover chat, responses, embeddings, images, audio, rerank and Anthropic messages.

- **+** 100+ providers behind /chat/completions, /responses, /embeddings, /rerank and /messages
- **+** Virtual keys, spend tracking, guardrails, load balancing and admin UI built in
- **+** MCP gateway and A2A agent routing through the same proxy
- **+** Same code usable as a Python SDK without the proxy
- **−** Custom license (NOASSERTION); enterprise features sit behind a paid tier
- **−** 8 ms P95 latency figure is self-benchmarked at 1k RPS
- **−** Endpoint coverage is uneven across the 100+ providers
- **−** MCP OAuth may need pre-registered client credentials; dynamic registration can 401

<sub>no GPU · Docker + Compose · Models: OpenAI, Anthropic, Gemini, Vertex AI, Bedrock, Azure, Cohere, Groq, Mistral, DeepSeek, Hugging Face, Ollama, vLLM and 100+ more · port 4000 · [Repo](https://github.com/berriai/litellm) · [📖 Docs ↗](https://docs.litellm.ai/docs/simple_proxy) · [🌐 Site ↗](https://www.litellm.ai/ai-gateway)</sub>

<a name="mcp-context-forge"></a>
### [🥈 69](../README.md#-how-we-rank "Score 69/100 (silver, 65-79). Adoption 25 · Freshness 100 · Maintenance 90 · Easy to run 67 · Agent-ready 70 (each out of 100, weighted). Click for how we rank.") [ContextForge MCP Gateway](https://github.com/ibm/mcp-context-forge) <sub>⭐ 4.6k · Apache-2.0 · Oct 2026</sub>

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
### [🥉 61](../README.md#-how-we-rank "Score 61/100 (bronze, 55-64). Adoption 55 · Freshness 100 · Maintenance 78 · Easy to run 33 · Agent-ready 45 (each out of 100, weighted). Click for how we rank.") [Higress](https://github.com/higress-group/higress) <sub>⭐ 9.5k · Apache-2.0 · Oct 2026</sub>

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
### [🥉 60](../README.md#-how-we-rank "Score 60/100 (bronze, 55-64). Adoption 45 · Freshness 100 · Maintenance 82 · Easy to run 33 · Agent-ready 45 (each out of 100, weighted). Click for how we rank.") [Bifrost](https://github.com/maximhq/bifrost) <sub>⭐ 8.7k · Apache-2.0 · Oct 2026</sub>

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
### [🥉 58](../README.md#-how-we-rank "Score 58/100 (bronze, 55-64). Adoption 38 · Freshness 100 · Maintenance 76 · Easy to run 33 · Agent-ready 55 (each out of 100, weighted). Click for how we rank.") [Plano](https://github.com/katanemo/plano) <sub>⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

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
### [🥉 57](../README.md#-how-we-rank "Score 57/100 (bronze, 55-64). Adoption 1 · Freshness 100 · Maintenance 87 · Easy to run 50 · Agent-ready 70 (each out of 100, weighted). Click for how we rank.") [GoModel](https://github.com/enterpilot/gomodel) <sub>⭐ 1.2k · MIT · Oct 2026</sub>

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
### [54](../README.md#-how-we-rank "Score 54/100. Adoption 32 · Freshness 100 · Maintenance 88 · Easy to run 33 · Agent-ready 0 (each out of 100, weighted). Click for how we rank.") [agentgateway](https://github.com/agentgateway/agentgateway) <sub>⭐ 5.2k · Apache-2.0 · Oct 2026</sub>

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
### [49](../README.md#-how-we-rank "Score 49/100. Adoption 16 · Freshness 100 · Maintenance 60 · Easy to run 33 · Agent-ready 40 (each out of 100, weighted). Click for how we rank.") [optillm](https://github.com/algorithmicsuperintelligence/optillm) <sub>⭐ 4.3k · Apache-2.0 · Sep 2026</sub>

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
### [47](../README.md#-how-we-rank "Score 47/100. Adoption 63 · Freshness 81 · Maintenance 3 · Easy to run 33 · Agent-ready 40 (each out of 100, weighted). Click for how we rank.") [Portkey Gateway](https://github.com/portkey-ai/gateway) <sub>⭐ 13k · MIT · May 2026</sub>

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
### [37](../README.md#-how-we-rank "Score 37/100. Adoption 7 · Freshness 86 · Maintenance 5 · Easy to run 50 · Agent-ready 0 (each out of 100, weighted). Click for how we rank.") [MetaMCP](https://github.com/metatool-ai/metamcp) <sub>⭐ 2.7k · MIT · Jun 2026</sub>

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
### [35](../README.md#-how-we-rank "Score 35/100. Adoption 50 · Freshness 55 · Maintenance 0 · Easy to run 33 · Agent-ready 0 (each out of 100, weighted). Click for how we rank.") [CoAI](https://github.com/coaidev/coai) <sub>⭐ 9.3k · Apache-2.0 · Mar 2026</sub>

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
### [29](../README.md#-how-we-rank "Score 29/100. Adoption 21 · Freshness 62 · Maintenance 0 · Easy to run 33 · Agent-ready 0 (each out of 100, weighted). Click for how we rank.") [mcpo](https://github.com/open-webui/mcpo) <sub>⭐ 4.4k · MIT · Feb 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
