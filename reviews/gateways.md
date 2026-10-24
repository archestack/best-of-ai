# 🔀 Gateways and observability reviews · Best of Open-Source AI

LLM gateways and proxies for routing, caching and cost control, and tracing, evaluation and prompt management for LLM apps. Back to the [leaderboard](../README.md#-gateways-and-observability).

<sub>🌐 Also on the web: [Gateways and observability on archestack.com](https://archestack.com/best-of-ai/gateways/), each project on its own page.</sub>

<a name="omniroute"></a>
### 🥇 [OmniRoute](https://github.com/diegosouzapw/omniroute) <sub>score [96](../README.md#-how-we-rank "Score 96/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 81k · MIT · Oct 2026</sub>

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
### 🥈 [new-api](https://github.com/quantumnous/new-api) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · AGPL-3.0 · Oct 2026</sub>

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

<a name="mlflow"></a>
### 🥉 [MLflow](https://github.com/mlflow/mlflow) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

**Tracing, evals, prompt registry and AI gateway plus classic ML tracking.**

Single mlflow server (port 5000) that records OpenTelemetry traces from 60+ frameworks via one-line autolog, runs evaluations with 50+ metrics and LLM judges, versions and optimizes prompts, and fronts providers through an OpenAI-compatible AI Gateway with rate limits, fallbacks and traffic splitting. Keeps the original experiment tracking, model registry and deployment tooling. For teams wanting one platform for GenAI and ML.

- **+** One-line autolog for 60+ frameworks in Python, TypeScript and Java; MCP and OTel native
- **+** Starts with uvx mlflow server; no separate database needed to begin
- **+** AI Gateway adds credential management, guardrails and A/B traffic splitting
- **+** Setup wizard lets Claude Code, Codex or OpenCode add tracing to a project
- **−** README covers the quickstart; production backend store and auth setup live in docs
- **−** Broad scope (ML tracking plus GenAI) means a large install and UI surface
- **−** No Dockerfile or compose file at the repo root
- **−** TypeScript and Java coverage is smaller than Python (5 TS and 2 Java frameworks listed)

<sub>no GPU · Docker + Compose · Models: any LLM provider via autolog or the AI Gateway · port 5000 · [Repo](https://github.com/mlflow/mlflow) · [▶️ Demo ↗](https://demo.mlflow.org/) · [📖 Docs ↗](https://mlflow.org/docs/latest) · [🌐 Site ↗](https://mlflow.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlflow/)</sub>

<a name="litellm"></a>
### #&#8288;4 [LiteLLM](https://github.com/berriai/litellm) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 62k · custom license · Oct 2026</sub>

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

<a name="freellmapi"></a>
### #&#8288;5 [freellmapi](https://github.com/tashfeenahmed/freellmapi) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

**OpenAI-compatible gateway pooling free-tier LLM providers with automatic failover.**

FreeLLMAPI serves one OpenAI-compatible /v1 endpoint, plus Anthropic Messages, Gemini and opt-in Ollama surfaces, in front of 34 free-tier providers and custom OpenAI-compatible endpoints. A router ranks models, retries on 429/5xx with key rotation, and tracks RPM/RPD/TPM/TPD per key. Provider keys are AES-256-GCM encrypted in SQLite, and a React dashboard manages keys and the fallback chain.

- **+** Per-key rate counters keep routing under each provider's free-tier caps
- **+** Covers chat, embeddings, images, video and speech, plus Anthropic and Gemini wire formats
- **+** One-command setup for Claude Code, Codex CLI, Cursor, Aider and other agents
- **+** About 40 MB RSS idle on Node 20+, including Raspberry Pi
- **−** Free installs get new models 30 days late; same-day catalog needs $19/yr premium
- **−** Catalog updates depend on a signed feed from freellmapi.co
- **−** Single-user by design; no multi-user setup described
- **−** Quality and limits depend on free tiers that providers change without notice

<sub>no GPU · Docker + Compose · Needs Node.js 20+, SQLite, Provider API keys, Docker (optional) · Models: OpenAI-compatible APIs, Anthropic Messages API, Gemini API, Ollama API (opt-in) · port 3001 · [Repo](https://github.com/tashfeenahmed/freellmapi) · [📖 Docs ↗](https://github.com/tashfeenahmed/freellmapi/blob/main/docs/en/README.md) · [🌐 Site ↗](https://freellmapi.co/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/freellmapi/)</sub>

<a name="langfuse"></a>
### #&#8288;6 [Langfuse](https://github.com/langfuse/langfuse) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · custom license · Oct 2026</sub>

**Tracing, prompt management and evals for LLM apps on ClickHouse.**

Ingests traces of LLM calls, retrieval and agent steps via Python and JS/TS SDKs or drop-in OpenAI, LangChain, LlamaIndex, LiteLLM and Vercel AI SDK integrations, then adds prompt versioning with caching, LLM-as-a-judge and code evaluators, datasets and a playground. Stores data in ClickHouse; deploys with docker compose, Helm on Kubernetes, or Terraform for AWS, Azure and GCP. For teams debugging and evaluating LLM apps.

- **+** Public OpenAPI spec, Postman collection and typed Python and JS/TS SDKs
- **+** Prompt management with server and client caching adds no request latency
- **+** Deployment paths from docker compose to Helm and Terraform templates
- **+** Integrations with Dify, Flowise, Langflow, OpenWebUI, LobeChat, CrewAI, smolagents
- **−** MIT except the ee folders; enterprise features need a commercial license
- **−** Runs on ClickHouse plus other services; heavier than single-binary tools
- **−** Default compose inherits Docker json-file logging with no rotation; disk can fill
- **−** No Dockerfile at the repo root; images come from Docker Hub

<sub>no GPU · Compose · Needs ClickHouse · [Repo](https://github.com/langfuse/langfuse) · [▶️ Demo ↗](https://langfuse.com/demo) · [📖 Docs ↗](https://langfuse.com/docs) · [🌐 Site ↗](https://langfuse.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langfuse/)</sub>

<a name="promptfoo"></a>
### #&#8288;7 [promptfoo](https://github.com/promptfoo/promptfoo) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

**CLI for evaluating and red-teaming prompts, agents and RAG.**

Runs prompt and model evaluations from a YAML config via promptfoo eval, compares providers side by side, and generates red-team vulnerability reports; promptfoo view opens a local web viewer. Installs with npm, Homebrew or pip, runs in CI/CD, and can scan pull requests for LLM security issues, for developers testing prompts and agents before release.

- **+** Evals run locally; prompts stay on your machine
- **+** Red-team scans produce vulnerability reports alongside quality evals
- **+** Live reload and caching for fast iteration; npx usage needs no install
- **+** MIT licensed and still open source after joining OpenAI
- **−** Primarily a CLI; the web viewer is a local results UI, not a multi-user server
- **−** Most providers require an API key; local use needs Ollama or similar
- **−** README is short; config syntax, assertions and providers are only in the docs
- **−** Dockerfile exists at the root but the README gives no Docker instructions

<sub>no GPU · Docker · Needs Node.js (npm) or Python (pip), LLM provider API key or Ollama · Models: OpenAI, Anthropic, Azure, Bedrock, Ollama · [Repo](https://github.com/promptfoo/promptfoo) · [📖 Docs ↗](https://www.promptfoo.dev/docs/) · [🌐 Site ↗](https://www.promptfoo.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/promptfoo/)</sub>

<a name="opik"></a>
### #&#8288;8 [Opik](https://github.com/comet-ml/opik) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · Apache-2.0 · Oct 2026</sub>

**Trace, evaluate and monitor LLM apps and agents, Apache-2.0 end to end.**

Logs trace trees for LLM calls, tool executions and agent steps via Python and TypeScript SDKs, OpenTelemetry or framework integrations, then runs datasets, experiments and LLM-as-a-judge metrics for hallucination, moderation and RAG quality, with online evaluation rules in production. Self-hosts with ./opik.sh (Docker Compose, UI on port 5173) or a Helm chart. For ML engineers moving agents to production.

- **+** Full platform (backend, web app, evals, prompt management) under Apache-2.0
- **+** Designed for 40M+ traces per day; online evaluation rules on production traffic
- **+** PyTest integration gates LLM pipelines in CI
- **+** MCP server lets Claude Code, Cursor, Codex or opencode query traces and run evals
- **−** No Dockerfile or compose file at the repo root; install goes through opik.sh
- **−** Multi-service stack (databases, caches, backend, frontend); not a single binary
- **−** Guardrails and the optimizer are separate profiles and SDKs to enable
- **−** README is heavy with Comet Cloud links and UTM tracking

<sub>no GPU · Compose · Models: any LLM via SDK, OpenTelemetry or framework integrations (Google ADK, AG2, Autogen, Flowise) · port 5173 · [Repo](https://github.com/comet-ml/opik) · [📖 Docs ↗](https://www.comet.com/docs/opik/) · [🌐 Site ↗](https://www.comet.com/site/products/opik/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opik/)</sub>

<a name="experiential"></a>
### #&#8288;9 [experiential](https://github.com/experientiallabs/experiential) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**OpenAI-compatible LLM gateway with per-user budgets and traffic-trained routers.**

Experiential runs a local gateway that exposes hosted, BYOK and local models through one OpenAI-compatible API, with access rules and spend budgets per user and agent. It can also build a custom router from OpenTelemetry traces and fine-tune an open model on them through Tinker. A hosted platform serves the same API, including Anthropic Messages.

- **+** Install with pip and start with `exp`; local gateway listens on 127.0.0.1:8000
- **+** Per-identity model access and budgets (setup wizard defaults to a $50.00 budget)
- **+** Builds a router from OTLP traces and can fine-tune a model from them
- **+** Hosted option accepts BYOK keys for OpenAI, Anthropic, Gemini, Azure, Bedrock, Fireworks, OpenRouter
- **−** Traffic capture is experimental, macOS only, needs Python 3.13+, and has reliability issues
- **−** Model fine-tuning depends on the external Tinker service
- **−** Anonymous PostHog telemetry is on by default and must be disabled manually
- **−** No Docker or compose files detected

<sub>no GPU · Needs Tinker (for model fine-tuning), Provider API keys (OpenAI, Anthropic, Gemini, Azure, Bedrock, Fireworks, OpenRouter) · Models: OpenAI-compatible API, Anthropic Messages API (hosted), hosted models, BYOK models, local models · port 8000 · [Repo](https://github.com/experientiallabs/experiential) · [📖 Docs ↗](https://platform.experientiallabs.ai/docs) · [🌐 Site ↗](https://platform.experientiallabs.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/experiential/)</sub>

<a name="llm-gateway"></a>
### #&#8288;10 [llm-gateway](https://github.com/mnfst/llm-gateway) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · MIT · Oct 2026</sub>

**OpenAI-compatible gateway routing requests across providers, subscriptions, local models.**

Manifest LLM Gateway exposes one OpenAI-compatible endpoint in front of 35 built-in provider connections, 18 subscription flows, local runtimes and custom endpoints. Sending "model": "auto" lets it pick the model. It logs full request bodies for successes and errors, tracks spend with limits and notifications, and falls back to other models when a query fails.

- **+** Supports 35 provider connections plus any custom /v1/chat/completions or /v1/messages endpoint
- **+** Can route through 18 subscription flows (e.g. ChatGPT, Claude, Copilot), not only API keys
- **+** Connects local runtimes: Ollama, LM Studio (port 1234), llama.cpp (port 8080)
- **+** Full body logs, cost tracking, limits and model fallback on failure
- **−** Self-hosting is Docker-only; the npm-based path is no longer supported
- **−** Volume-backed templates are single-instance; scaling out needs S3-compatible storage
- **−** Needs a database and recording storage; Postgres appears in the hosted templates
- **−** RAM and CPU requirements are not stated

<sub>no GPU · Docker + Compose · Needs Docker, PostgreSQL, S3-compatible storage (for scaled deployments) · Models: OpenAI, Anthropic, Google Gemini, AWS Bedrock, OpenRouter · port 2099 · [Repo](https://github.com/mnfst/llm-gateway) · [📖 Docs ↗](https://manifest.build/llm-gateway/docs/introduction/) · [🌐 Site ↗](https://app.manifest.build) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-gateway/)</sub>

<a name="phoenix"></a>
### #&#8288;11 [Phoenix](https://github.com/arize-ai/phoenix) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · custom license · Oct 2026</sub>

**LLM tracing, evaluation and prompt management built on OpenTelemetry.**

Phoenix collects OpenTelemetry/OpenInference traces from LLM applications and provides evaluations, versioned datasets, experiments, a prompt playground and prompt version management. It also includes a built-in agent (PXI) and a remote MCP endpoint at /mcp for clients such as Claude Code and Cursor. It installs with pip or uvx, or runs from a Docker image or Helm chart.

- **+** Auto-instrumentation via OpenInference for OpenAI, Anthropic, LangGraph, LlamaIndex, CrewAI, DSPy and others
- **+** Starts with pip install arize-phoenix and phoenix serve, or uvx arize-phoenix serve
- **+** Covers tracing, evals, datasets, experiments and prompt versioning in one server
- **+** Python and TypeScript packages; Helm chart and cloud deploy templates
- **−** License is reported as NOASSERTION, so terms need checking before commercial use
- **−** Managed production workflows are offered through the separate Arize AX product
- **−** Standalone stdio MCP server is in maintenance mode, replaced by the built-in remote one
- **−** TypeScript evals package is labelled alpha

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL · Models: OpenAI, Anthropic, Google GenAI, AWS Bedrock, OpenRouter · [Repo](https://github.com/arize-ai/phoenix) · [📖 Docs ↗](https://arize.com/docs/phoenix/) · [🌐 Site ↗](https://phoenix.arize.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/phoenix/)</sub>

<a name="bifrost"></a>
### #&#8288;12 [Bifrost](https://github.com/maximhq/bifrost) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.1k · Apache-2.0 · Oct 2026</sub>

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

<a name="clawrouter"></a>
### #&#8288;13 [clawrouter](https://github.com/blockrunai/clawrouter) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · MIT · Oct 2026</sub>

**Local LLM router that picks the cheapest capable model per request.**

ClawRouter runs a local proxy on port 8402 with an OpenAI-compatible endpoint. It scores each request across 15 dimensions and picks the cheapest model that can handle it, from about 90 chat models behind BlockRun's gateway. Payment is USDC over x402 on Solana or Base, or a card-funded API key. Seven free models need no signup. It also installs as an OpenClaw plugin.

- **+** Routing runs locally in under 1 ms, with no external calls for the decision
- **+** OpenAI-compatible proxy works with Cursor, continue.dev and the OpenAI SDK
- **+** Seven free models usable without signup, key or wallet
- **+** Pay by x402 USDC per request or by card-funded API key
- **−** Paid models go through BlockRun's hosted gateway, not directly to each provider
- **−** Savings figures come from the vendor's own published workload mix
- **−** About 90 chat models, fewer than OpenRouter's listed 200+
- **−** Card top-ups cost 5.5% + $0.30; wallet use adds $0.001 per transaction

<sub>no GPU · Needs Node.js, BlockRun gateway (blockrun.ai), USDC wallet (Solana or Base) or BlockRun API key · Models: OpenAI, Anthropic, Google, xAI, DeepSeek · port 8402 · [Repo](https://github.com/blockrunai/clawrouter) · [🌐 Site ↗](https://blockrun.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clawrouter/)</sub>

<a name="higress"></a>
### #&#8288;14 [Higress](https://github.com/higress-group/higress) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (49) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

**Istio and Envoy API gateway with LLM proxying and MCP server hosting.**

Higress is a cloud-native API gateway built on Istio and Envoy, extended through Wasm plugins written in Go, Rust or JS. For AI use it proxies many LLM providers behind a unified protocol with token rate limiting, caching, load balancing and observability. It can also host remote MCP servers, including ones converted from OpenAPI specs, and doubles as a Kubernetes ingress controller.

- **+** Wasm plugins in Go/Rust/JS with hot updates, no connection drops on config change
- **+** Streams request and response bodies, including SSE, for LLM traffic
- **+** Hosts MCP servers with auth, rate limiting and audit logs; OpenAPI-to-MCP conversion
- **+** Also a Kubernetes ingress and Gateway API implementation; one-command Docker start
- **−** Heavier to operate than a lightweight LLM proxy; Istio/Envoy concepts apply
- **−** Default images are pulled from Alibaba Cloud registries; mirrors needed in some regions
- **−** Plugin hub and much of the documentation are hosted on higress.cn
- **−** Resource requirements are not stated in the README

<sub>no GPU · Docker · Needs Docker or Kubernetes · Models: multiple domestic and international LLM providers via ai-proxy plugin · port 8001 · [Repo](https://github.com/higress-group/higress) · [▶️ Demo ↗](https://demo.higress.io/) · [📖 Docs ↗](https://higress.cn/en/docs/latest/overview/what-is-higress/) · [🌐 Site ↗](https://higress.ai/en/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/higress/)</sub>

<a name="deepeval"></a>
### #&#8288;15 [deepeval](https://github.com/confident-ai/deepeval) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Oct 2026</sub>

**Pytest-style framework for unit testing LLM apps, RAG pipelines and agents.**

DeepEval is a Python framework that runs LLM evaluations as pytest-style tests via `deepeval test run`. It ships metrics such as G-Eval, DAG, task completion, tool correctness, faithfulness and hallucination, scored by an LLM judge of your choice or local NLP models. It supports end-to-end, trace-based and component-level evals, synthetic dataset generation, and standard benchmarks like MMLU and GSM8K.

- **+** Metrics for RAG, agents, multi-turn chats, MCP and multimodal outputs
- **+** Pytest-style tests run in CI with `deepeval test run`
- **+** Tracing via @observe supports component-level and agent trajectory evals
- **+** Integrations for LangChain, LangGraph, CrewAI, LlamaIndex, OpenAI Agents, Pydantic AI and others
- **−** LLM-judge metrics need a model; the quickstart uses an OpenAI API key
- **−** Report sharing and production monitoring sit in the hosted Confident AI platform
- **−** README pushes account login; test cases are logged to the cloud once logged in
- **−** Judge-based scores depend on the chosen judge model and vary between runs

<sub>GPU optional · Needs OpenAI API key or custom LLM judge, Confident AI account (optional) · Models: OpenAI, Anthropic, custom LLMs, local NLP models · [Repo](https://github.com/confident-ai/deepeval) · [📖 Docs ↗](https://deepeval.com/docs/getting-started) · [🌐 Site ↗](https://www.confident-ai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepeval/)</sub>

<a name="langwatch"></a>
### #&#8288;16 [LangWatch](https://github.com/langwatch/langwatch) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · Apache-2.0 · Oct 2026</sub>

**LLM tracing, evals, gateway and governance platform for agents and coding assistants.**

LangWatch traces LLM calls and runs agent simulation tests, evaluations and prompt management. It also includes an OpenAI and Anthropic compatible gateway with virtual keys and budgets, plus tracking for coding agents such as Claude Code and Codex. Self-hosting starts with `npx @langwatch/server`, which needs only Node.js.

- **+** Integrates with LangChain, LangGraph, Vercel AI SDK, CrewAI, DSPy and OpenTelemetry
- **+** Tracks coding agents (Claude Code, Codex, Copilot, opencode) with cost per pull request
- **+** Gateway offers virtual keys with budgets and one OpenAI and Anthropic compatible endpoint
- **+** Self-host quickstart needs only Node.js; SDKs for Python and TypeScript
- **−** Enterprise modules under enterprise/ need a commercial license in production
- **−** Broad scope (ops, gateway, governance) makes it heavier than a tracing-only tool
- **−** README gives no RAM, database or port requirements for production self-hosting
- **−** No Docker or compose file detected in the repository

<sub>no GPU · Needs Node.js · Models: OpenAI, Anthropic, Azure OpenAI, Vertex AI, Bedrock · [Repo](https://github.com/langwatch/langwatch) · [📖 Docs ↗](https://langwatch.ai/docs/introduction) · [🌐 Site ↗](https://langwatch.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langwatch/)</sub>

<a name="agenta"></a>
### #&#8288;17 [Agenta](https://github.com/agenta-ai/agenta) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · custom license · Oct 2026</sub>

**Shared team workspace for building and running chat-built agents.**

Agenta is a multi-user workspace where agents are built by chatting, then shared with a team and used in the web app, Slack, Telegram or WhatsApp Business. Agents run on schedules or app events, each session in its own sandbox with a browser and file system, and every run is traced with cost tracking. Integrations go through MCP or Composio (1,000+ apps); models can be hosted APIs or Ollama.

- **+** Multi-user by design: roles, shared agents and chat sessions, per-agent tool permissions
- **+** Each session runs in its own sandbox; model credentials are not exposed to the agent
- **+** Every run is traced and costs are tracked per agent, with versions visible
- **+** Works with hosted model APIs or self-hosted models via Ollama, plus Claude and ChatGPT subscriptions
- **−** Supports only Claude Code, Pi and Codex harnesses today; more are on the roadmap
- **−** Not a visual workflow builder; agents decide steps, so execution is less predictable
- **−** Self-hosting requirements (RAM, ports, dependencies) are not given in the README
- **−** License reported as NOASSERTION by tooling, though the README states MIT

<sub>Needs Composio (optional, for 1,000+ app integrations), Ollama (optional, for self-hosted models) · Models: Hosted model APIs, Ollama, Claude subscription, ChatGPT subscription · [Repo](https://github.com/agenta-ai/agenta) · [▶️ Demo ↗](https://cloud.agenta.ai) · [📖 Docs ↗](https://agenta.ai/docs/) · [🌐 Site ↗](https://agenta.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agenta/)</sub>

<a name="plano"></a>
### #&#8288;18 [Plano](https://github.com/katanemo/plano) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (32) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

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

<a name="harbor"></a>
### #&#8288;19 [harbor](https://github.com/harbor-framework/harbor) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Oct 2026</sub>

**Evaluation harness for running agents and models against container-based benchmarks.**

Harbor is a Python CLI from the Terminal-Bench team that runs agents such as Claude Code, OpenHands and Codex CLI against benchmark datasets in container environments. It runs locally on Docker or fans out to cloud sandbox providers like Daytona and Modal. It is the official harness for Terminal-Bench 2.0 and can also generate rollouts for RL optimization.

- **+** Official harness for Terminal-Bench 2.0; SWE-Bench and Aider Polyglot also listed
- **+** Same `harbor run` command works on local Docker or cloud providers via `--env`
- **+** Parallel runs across sandbox providers including Daytona, Modal, LangSmith and Blaxel
- **+** Supports custom benchmarks and environments, plus rollout generation for RL
- **−** Needs model provider API keys and, for scale-out, a sandbox provider account
- **−** Local runs depend on Docker; no image or compose file in the repo
- **−** README gives no hardware requirements or full list of supported agents
- **−** Evaluation only; not an agent builder or observability dashboard

<sub>no GPU · Needs Docker, Daytona, Modal · Models: Provider/model strings via --model, e.g. anthropic/... · [Repo](https://github.com/harbor-framework/harbor) · [📖 Docs ↗](https://harborframework.com/docs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/harbor/)</sub>

<a name="giskard-oss"></a>
### #&#8288;20 [giskard-oss](https://github.com/giskard-ai/giskard-oss) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

**Python library for evals and red-team scans of LLM agents.**

Giskard v3 is a modular Python library for testing agentic systems. giskard-checks provides a scenario API with string, regex, semantic-similarity and LLM-as-judge checks (Groundedness, Conformity, LLMJudge) for multi-turn evals. giskard-scan generates adversarial suites from a plain-language agent description, covering prompt injection, harmful content and misinformation, and adds RAG knowledge-base quality evaluation.

- **+** Wraps any sync or async callable, so LLMs, black-box agents and pipelines are all testable
- **+** Supports multi-turn scenarios and suites, not just single-prompt assertions
- **+** Scan generates adversarial tests across OWASP LLM Top-10 categories from a text description
- **+** Split into packages, so installs carry only the dependencies needed
- **−** LLM judges and scan generators need a provider extra and API key; default judge is openai/gpt-4o-mini
- **−** Requires Python 3.12+
- **−** Tabular/ML model scan and Hub exist only in v2, which is no longer actively maintained
- **−** Optional telemetry is on unless disabled via environment variable

<sub>no GPU · Needs Python 3.12+, LLM provider API key (e.g. OpenAI) for judges and scan generators · Models: OpenAI, Anthropic, other providers via giskard-llm · [Repo](https://github.com/giskard-ai/giskard-oss) · [📖 Docs ↗](https://docs.giskard.ai/oss) · [🌐 Site ↗](https://www.giskard.ai/?utm_source=github&utm_medium=github&utm_campaign=github_readme&utm_id=readmeblog) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/giskard-oss/)</sub>

<a name="mcp-context-forge"></a>
### #&#8288;21 [ContextForge MCP Gateway](https://github.com/ibm/mcp-context-forge) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · Apache-2.0 · Oct 2026</sub>

**Registry and proxy federating MCP servers, A2A agents and REST/gRPC APIs.**

ContextForge puts MCP servers, A2A agents and REST/gRPC services behind one gateway endpoint with auth, rate limiting, retries and OpenTelemetry tracing. It wraps non-MCP APIs as virtual MCP servers and translates gRPC via reflection. It ships an Admin UI, an optional separate Web UI and 40+ plugins, and runs from PyPI, Docker Compose (PostgreSQL, Redis, Nginx) or a Helm chart.

- **+** Wraps REST and gRPC (via reflection) services as virtual MCP servers
- **+** Exports OpenTelemetry traces to Phoenix, Jaeger, Zipkin and other OTLP backends
- **+** Installs from PyPI or GHCR image; Helm chart and Redis-backed federation available
- **+** Built-in Admin UI plus 40+ plugins for extra transports and integrations
- **−** Gateway refuses to start without JWT_SECRET_KEY and AUTH_ENCRYPTION_SECRET set
- **−** arm64 containers not supported in production; Apple Silicon needs Rosetta or PyPI
- **−** Local Docker image build needs a CI-produced wheel closure; must pull from GHCR
- **−** Full compose stack runs PostgreSQL, Redis and Nginx, heavy for small setups

<sub>no GPU · Docker + Compose · Needs PostgreSQL, Redis, Nginx, Python 3.11+ · port 4444 · [Repo](https://github.com/ibm/mcp-context-forge) · [📖 Docs ↗](https://ibm.github.io/mcp-context-forge/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-context-forge/)</sub>

<a name="openllmetry"></a>
### #&#8288;22 [openllmetry](https://github.com/traceloop/openllmetry) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (35) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Oct 2026</sub>

**OpenTelemetry instrumentations and SDK for tracing LLM calls and vector DBs.**

OpenLLMetry is a set of OpenTelemetry extensions that trace calls to LLM providers, vector databases and agent frameworks. The Traceloop SDK is enabled with `Traceloop.init()` after `pip install traceloop-sdk`, and it emits standard OpenTelemetry data that can be exported to backends such as Datadog, Honeycomb, Grafana, SigNoz and Sentry. A separate repo covers JS/TS.

- **+** Emits standard OpenTelemetry data, so it works with an existing observability stack
- **+** Instruments many providers, including OpenAI, Anthropic, Bedrock, Gemini, Ollama and Mistral
- **+** Covers vector DBs (Chroma, Pinecone, Qdrant, Weaviate) and frameworks like LangChain and CrewAI
- **+** One-line setup with the SDK; instrumentations can also be added individually
- **−** Python only in this repo; JS/TS lives in the separate OpenLLMetry-JS repo
- **−** No bundled UI or storage; you need a separate backend to view traces
- **−** SDK telemetry was collected in earlier versions; the README says it stops at v0.49.2 and above
- **−** No evaluation or prompt management in this repo; the README covers tracing only

<sub>no GPU · Needs OpenTelemetry-compatible backend · Models: OpenAI, Azure OpenAI, Anthropic, AWS Bedrock, Google Gemini · [Repo](https://github.com/traceloop/openllmetry) · [📖 Docs ↗](https://traceloop.com/docs/openllmetry/introduction) · [🌐 Site ↗](https://www.traceloop.com/openllmetry) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openllmetry/)</sub>

<a name="latitude-llm"></a>
### #&#8288;23 [Latitude](https://github.com/latitude-dev/latitude-llm) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · MIT · Oct 2026</sub>

**Agent observability that groups failures and dispatches coding agents to fix them.**

Captures traces, sessions and tool calls via a one-line SDK (TypeScript, Python) or OpenTelemetry, groups failing traces into tracked signals, then dispatches Claude Code or Cursor with those traces to open a fix PR and replays fixes against regression datasets. The UI is also reachable from an MCP server and CLI; self-hosts from Docker Hub images via Compose or Helm. For teams operating agents in production.

- **+** Signals auto-group failing traces with status, size and trend
- **+** Agent Dispatch sends sample traces to Claude Code or Cursor via Linear or webhooks
- **+** Regression datasets replay fixes against the real failing traces
- **+** MIT license; Compose and Helm paths plus Railway one-click
- **−** README quickstart targets the cloud; self-host steps are in external docs
- **−** Automatic fixing depends on third-party coding agents and their subscriptions
- **−** Claude Code session capture is a separate telemetry package
- **−** Storage and service requirements are not stated in the README

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL, ClickHouse, Redis · Models: OpenAI, Anthropic, Bedrock, Vercel AI SDK and LangChain apps, any OpenTelemetry source · [Repo](https://github.com/latitude-dev/latitude-llm) · [📖 Docs ↗](https://docs.latitude.so) · [🌐 Site ↗](https://latitude.so) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/latitude-llm/)</sub>

<a name="gomodel"></a>
### #&#8288;24 [GoModel](https://github.com/enterpilot/gomodel) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Oct 2026</sub>

**Go LLM gateway with OpenAI and Anthropic-compatible APIs, caching and budgets.**

GoModel is a gateway written in Go that exposes OpenAI-compatible (/v1) and Anthropic-compatible (/v1/messages) endpoints in front of many providers, including OpenAI, Anthropic, Gemini, Bedrock, Ollama and vLLM. It adds exact and semantic caching, cost tracking, budgets, rate limits, failover and an admin dashboard on port 8080. Prompt compression, intelligent routing and OIDC SSO are only in the commercial GoModel Pro build.

- **+** Accepts OpenAI and Anthropic SDK requests unchanged by only changing the base URL
- **+** Covers caching, budgets, rate limits, failover, key rotation and guardrails in one gateway
- **+** Exports Prometheus metrics and OpenTelemetry traces, with a built-in dashboard and playground
- **+** Public live demo and self-reproducible benchmarks are linked from the README
- **−** Prompt compression, intelligent routing and OIDC SSO require the paid GoModel Pro
- **−** Speed and efficiency claims come from the project's own benchmarks
- **−** Roadmap points to an upcoming 0.2.0, so the feature set is still changing
- **−** Optional Redis, PostgreSQL and MongoDB setups add infrastructure; resource needs are unknown

<sub>no GPU · Docker + Compose · Needs Redis (optional), PostgreSQL (optional), MongoDB (optional), Prometheus (optional) · Models: OpenAI, Anthropic, Google Gemini, Vertex AI, Amazon Bedrock · port 8080 · [Repo](https://github.com/enterpilot/gomodel) · [▶️ Demo ↗](https://demo.enterpilot.io/admin/dashboard?utm_source=readme) · [📖 Docs ↗](https://gomodel.enterpilot.io/docs?utm_source=readme) · [🌐 Site ↗](https://gomodel.enterpilot.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gomodel/)</sub>

<a name="semantic-router"></a>
### #&#8288;25 [semantic-router](https://github.com/vllm-project/semantic-router) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Oct 2026</sub>

**Policy-driven router that selects or combines models behind one API endpoint.**

vLLM Semantic Router sits between an agent harness and several configured model backends (local, private, cloud) and selects or combines models for each call based on a user-defined policy. Clients call one inference endpoint with a public model ID such as `vllm-sr/auto`. Policy can weigh quality, latency and cost, and keep calls within approved locations. Written in Go.

- **+** One endpoint (vllm-sr/auto) fronts many local, private and cloud backends
- **+** Policy can set quality, latency and cost priorities and location limits
- **+** Publishes its own routing models on Hugging Face and a hallucination detection endpoint
- **+** Hosted playground available; Apache-2.0 with recent commits and releases
- **−** README gives no RAM, GPU or port requirements
- **−** Install is a curl-to-bash script; other methods documented only externally
- **−** README is mostly news and links; configuration details live on the docs site
- **−** Does not run the agent loop or tools; needs a separate agent harness

<sub>Docker · Models: local, private and cloud backends · [Repo](https://github.com/vllm-project/semantic-router) · [▶️ Demo ↗](https://app.vllm-sr.ai/playground) · [📖 Docs ↗](https://vllm-sr.ai/docs/intro/) · [🌐 Site ↗](https://vllm-sr.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/semantic-router/)</sub>

<a name="agentgateway"></a>
### #&#8288;26 [agentgateway](https://github.com/agentgateway/agentgateway) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.5k · Apache-2.0 · Oct 2026</sub>

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

<a name="openlit"></a>
### #&#8288;27 [OpenLIT](https://github.com/openlit/openlit) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Oct 2026</sub>

**OpenTelemetry-based tracing, evals and guardrails for LLM apps and coding agents.**

OpenLIT is a self-hosted dashboard plus Python and TypeScript SDKs that auto-instrument LLM providers, frameworks and vector databases, and export OpenTelemetry GenAI traces and metrics to ClickHouse. It adds cost tracking, LLM-as-a-judge evals, a versioned Prompt Hub, a Rule Engine, Vault for API keys, runtime guardrails, and GPU monitoring. A CLI installs tracing for Claude Code, Cursor, Codex and OpenCode.

- **+** Follows OpenTelemetry GenAI conventions; OTLP on 4317 (gRPC) and 4318 (HTTP)
- **+** One-line openlit.init() instruments 70+ providers, frameworks and vector DBs
- **+** Covers evals, prompt versioning, guardrails, secrets and cost in one tool
- **+** CLI adds tracing for Claude Code, Cursor, Codex and OpenCode sessions
- **−** Wide scope (Vault, OpenGround, Rule Engine) means more to deploy and learn than a tracer
- **−** Storage is ClickHouse, adding a database to operate
- **−** Guardrails cover only prompt injection, sensitive topics and topic restriction
- **−** Resource requirements are not stated in the README

<sub>GPU optional · Compose · Needs ClickHouse, Docker Compose · Models: OpenAI, Anthropic, Ollama, vLLM, Amazon Bedrock · port 3000 · [Repo](https://github.com/openlit/openlit) · [📖 Docs ↗](https://docs.openlit.io/) · [🌐 Site ↗](https://openlit.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openlit/)</sub>

<a name="lmnr"></a>
### #&#8288;28 [Laminar](https://github.com/lmnr-ai/lmnr) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · Apache-2.0 · Oct 2026</sub>

**Observability platform for AI agents with tracing, evals and SQL-queryable traces.**

Laminar is a Rust-based observability backend for AI agents. Its OpenTelemetry-native TypeScript and Python SDKs trace calls to OpenAI, Anthropic, Gemini, LangChain, Vercel AI SDK, Browser Use and Stagehand. It adds plain-English signals that alert in Slack, an eval SDK and CLI, dashboards, datasets, and MCP/CLI access for SQL queries over traces.

- **+** SDKs for TypeScript and Python start tracing with one initialize call
- **+** Query traces, spans, metrics and events with SQL, including via MCP and CLI
- **+** Signals describe agent behavior in plain English and notify in Slack
- **+** Rust backend with 20x trace compression and full-text search over spans
- **−** README recommends the managed platform or the full compose file for production
- **−** Chat-with-trace and SQL-with-AI need a separately configured LLM provider
- **−** Self-hosted deployments send anonymous telemetry unless disabled by env variable
- **−** Self-hosting RAM and disk requirements are not stated

<sub>no GPU · Compose · Needs ClickHouse, Postgres, Docker Compose · Models: OpenAI, Anthropic, Gemini, AWS Bedrock, Azure AI Foundry · port 5667 · [Repo](https://github.com/lmnr-ai/lmnr) · [📖 Docs ↗](https://laminar.sh/docs) · [🌐 Site ↗](https://laminar.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmnr/)</sub>

<a name="optillm"></a>
### #&#8288;29 [optillm](https://github.com/algorithmicsuperintelligence/optillm) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Oct 2026</sub>

**OpenAI-compatible proxy that applies inference-time reasoning techniques to any LLM.**

OptiLLM is a Python proxy that exposes an OpenAI-compatible chat completions endpoint and wraps requests with inference-time techniques such as MoA, MCTS, PlanSearch, CePO and MARS. The technique is chosen by a model-name prefix (e.g. `moa-gpt-4o-mini`), an `extra_body` field or a prompt tag. It forwards to OpenAI, Azure, Cerebras, a local server or LiteLLM providers, and includes plugins for memory, PII anonymization, URL reading, MCP and code execution.

- **+** Technique chosen per request via model prefix, extra_body or prompt tag; chainable with & and |
- **+** Works with any OpenAI-compatible endpoint and LiteLLM providers; clients only change base_url
- **+** Plugins for privacy, memory, MCP client, code execution, JSON output and provider failover
- **+** Binds to 127.0.0.1 by default; Docker images in full, proxy-only and offline variants
- **−** Techniques like MoA, MCTS and N-sample selection multiply API calls, raising latency and token cost
- **−** CoT decoding, entropy decoding and AutoThink are marked not available through the proxy
- **−** Accuracy gains are the project's own benchmark claims and vary by model and task
- **−** Startup log shows the Flask development server, which the README says not to use in production

<sub>GPU optional · Docker + Compose · Needs OpenAI-compatible API or LiteLLM provider, spaCy (privacy plugin), Selenium and Chrome (web_search plugin) · Models: OpenAI, Azure OpenAI, Cerebras, Anthropic, Google Gemini · port 8000 · [Repo](https://github.com/algorithmicsuperintelligence/optillm) · [▶️ Demo ↗](https://huggingface.co/spaces/codelion/optillm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/optillm/)</sub>

<a name="future-agi"></a>
### #&#8288;30 [Future AGI](https://github.com/future-agi/future-agi) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Oct 2026</sub>

**Tracing, evals, simulation, guardrails and an LLM gateway for AI agents.**

Future AGI is a Django and Go platform that traces agents over OpenTelemetry, scores outputs with 50+ evaluators, simulates multi-turn conversations, and applies guardrail scanners. It also ships an OpenAI-compatible gateway with routing, caching and virtual keys, plus prompt-optimization algorithms. The default install runs one app container with Postgres and ClickHouse; a distributed Compose setup and a Helm chart cover larger deployments.

- **+** OTel tracing with instrumentors for 50+ frameworks in Python, TypeScript, Java and C#
- **+** Gateway is OpenAI-compatible with 100+ providers, semantic caching and virtual keys
- **+** Standalone install is one command and needs 2 vCPUs and 4 GB for Docker
- **+** Apache-2.0 core; Compose, production overlay, Helm and air-gapped modes documented
- **−** No supported path to move Standalone data to Distributed or Helm later
- **−** Distributed setup needs 4+ vCPUs and 12-16 GB, plus Kafka and PeerDB
- **−** Many components (Postgres, ClickHouse, Redis, Temporal) make it heavy to operate
- **−** Benchmark figures come from the README; independent verification is unknown

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Needs PostgreSQL, ClickHouse, Redis, Temporal, Docker Compose v2.24+ · Models: OpenAI-compatible providers (100+ via gateway) · port 3000 · [Repo](https://github.com/future-agi/future-agi) · [▶️ Demo ↗](https://www.youtube.com/watch?v=6keOTAOUUWI) · [📖 Docs ↗](https://docs.futureagi.com) · [🌐 Site ↗](https://futureagi.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/future-agi/)</sub>

<a name="evidently"></a>
### #&#8288;31 [evidently](https://github.com/evidentlyai/evidently) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: known (39) · Freshness: active (100) · Maintenance: patchy (31) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · Apache-2.0 · Sep 2026</sub>

**Python library to evaluate, test and monitor ML and LLM systems.**

Evidently is a Python library with 100+ built-in metrics for tabular and text data, covering data drift, data quality, classification, regression, ranking, RAG and LLM-as-a-judge evals. Reports can be turned into pass/fail Test Suites for CI checks, and results can be exported as JSON, dict or HTML. A self-hosted monitoring UI (`evidently ui`, localhost:8000) tracks metrics over time.

- **+** 100+ built-in metrics, including 20+ statistical drift tests and LLM-as-a-judge evals
- **+** Reports convert to Test Suites with gt/lt conditions, or conditions auto-generated from a reference dataset
- **+** Installs with pip or conda; the self-hosted monitoring UI starts with one command
- **+** Custom metrics via Python interface; exports to JSON, dict and HTML
- **−** Supports only tabular and text data; no image or audio evals listed
- **−** Alerting, dataset and user management, and no-code evals are Cloud-only features
- **−** Not a tracing or prompt-management tool; focused on metrics and tests
- **−** Self-hosted UI auth and scaling details are not described in the README

<sub>no GPU · Docker · Needs Python, pandas · Models: tabular data, text, LLM-as-a-judge · port 8000 · [Repo](https://github.com/evidentlyai/evidently) · [▶️ Demo ↗](https://demo.evidentlyai.com) · [📖 Docs ↗](https://docs.evidentlyai.com) · [🌐 Site ↗](https://www.evidentlyai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/evidently/)</sub>

<a name="helicone"></a>
### #&#8288;32 [Helicone](https://github.com/helicone/helicone) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (23) · Freshness: recent (79) · Maintenance: patchy (35) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Oct 2026</sub>

**LLM proxy gateway with request logging, cost tracking and sessions.**

Sits as an OpenAI-compatible gateway in front of 100+ models with routing and automatic fallbacks, logging every request with cost, latency and session traces, plus a playground and prompt versioning. Self-hosts via a compose script that runs six services: web app, Jawn log server, Workers proxy, Supabase, ClickHouse and MinIO. For engineers who want observability by swapping an endpoint.

- **+** One-line integration: point the OpenAI SDK baseURL at the gateway
- **+** Async logging path via OpenLLMetry for apps that cannot proxy
- **+** Open LLM cost database covering 300+ models; MCP server for data export
- **+** Apache-2.0; self-host compose script included
- **−** Six-service stack including Supabase, ClickHouse, MinIO and a Cloudflare Workers proxy
- **−** Production Helm chart is enterprise only, by contacting sales
- **−** Manual deployment is explicitly not recommended
- **−** README quickstart is cloud-first; self-hosting details are in external docs

<sub>no GPU · Docker + Compose · Needs Supabase (database and auth), ClickHouse, MinIO, Cloudflare Workers runtime (proxy) · Models: 100+ providers via gateway (OpenAI, Azure, Anthropic, Bedrock, Gemini, Groq, Together, Fireworks, Ollama) · [Repo](https://github.com/helicone/helicone) · [▶️ Demo ↗](https://helicone.ai/demo) · [📖 Docs ↗](https://docs.helicone.ai/) · [🌐 Site ↗](https://www.helicone.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/helicone/)</sub>

<a name="portkey-gateway"></a>
### #&#8288;33 [Portkey Gateway](https://github.com/portkey-ai/gateway) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (60) · Freshness: recent (75) · Maintenance: weak (3) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · May 2026</sub>

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

<a name="gptcache"></a>
### #&#8288;34 [gptcache](https://github.com/zilliztech/gptcache) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: known (41) · Freshness: recent (70) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · MIT · Sep 2026</sub>

**Python semantic cache for LLM responses using embeddings and vector search.**

GPTCache is a Python library that caches LLM responses and serves them for exact or semantically similar queries. It embeds each query, looks it up in a vector store, and keeps responses in a SQL cache store. It wraps the OpenAI client and integrates with LangChain and llama_index. The README says no new APIs or models will be added.

- **+** Modular: swap embedding model, cache store, vector store and similarity evaluator
- **+** OpenAI adapter needs a few init lines, no changes to existing calls
- **+** Storage options include SQLite, PostgreSQL, MySQL, DynamoDB; vectors in FAISS or Milvus
- **+** Temperature setting can skip the cache; sample benchmark reports hit ratio, latency, recall
- **−** README says no support will be added for new LLM APIs or models
- **−** Last release 2024-08-01; examples use the older openai.ChatCompletion style
- **−** Semantic matching can return false-positive hits; threshold tuning is left to the user
- **−** README warns the API may change at any time

<sub>no GPU · Needs Python 3.8.1+, SQLite or another SQL database, FAISS or Milvus vector store, OpenAI API key (for OpenAI adapter) · Models: OpenAI, LangChain, llama.cpp, MiniGPT-4, Dolly · [Repo](https://github.com/zilliztech/gptcache) · [📖 Docs ↗](https://gptcache.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gptcache/)</sub>

<a name="evals"></a>
### #&#8288;35 [evals](https://github.com/openai/evals) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (72) · Freshness: recent (63) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Apr 2026</sub>

**Python framework and registry for evaluating LLMs and LLM-based systems.**

Runs evals against OpenAI models and LLM-built systems, using a registry of existing evals plus custom ones defined as JSON data and YAML config. Model-graded evals need no evaluation code, and a Completion Function Protocol covers prompt chains and tool-using agents. Results can optionally be logged to Snowflake.

- **+** Basic and model-graded evals need only JSON data and YAML, no code
- **+** Completion Function Protocol supports prompt chains and tool-using agents
- **+** Registry of existing evals, with private evals possible on your own data
- **+** Optional result logging to Snowflake
- **−** Setup is documented around an OpenAI API key; other providers are not described
- **−** Registry data is stored in Git-LFS and must be pulled separately
- **−** Not accepting contributed evals with custom code
- **−** Known issue: runs can hang after the final report until interrupted

<sub>no GPU · Needs OpenAI API key, Git-LFS, Snowflake (optional) · Models: OpenAI models, custom completion functions · [Repo](https://github.com/openai/evals) · [📖 Docs ↗](https://platform.openai.com/docs/guides/evals) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/evals/)</sub>

<a name="ragas"></a>
### #&#8288;36 [ragas](https://github.com/vibrantlabsai/ragas) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (65) · Freshness: recent (53) · Maintenance: weak (2) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Feb 2026</sub>

**Python library for scoring LLM and RAG application outputs with metrics.**

Ragas is a Python package for evaluating LLM applications. It ships pre-built and custom metrics, including LLM-judged ones such as DiscreteMetric, and can generate test datasets when none exist. It integrates with LangChain and observability tools, and a `ragas quickstart rag_eval` command scaffolds an example RAG evaluation project.

- **+** Installs with pip; quickstart command scaffolds a RAG evaluation project
- **+** Custom metrics defined by a prompt and allowed values, scored asynchronously
- **+** Generates test datasets when none are available
- **+** Apache-2.0 licensed; telemetry can be disabled with RAGAS_DO_NOT_TRACK
- **−** LLM-based metrics need an external model, such as an OpenAI key in the example
- **−** Only the rag_eval quickstart template exists; other templates are listed as coming soon
- **−** Collects anonymized usage analytics by default; opt-out required
- **−** No UI or hosted dashboard described in the README

<sub>no GPU · Needs LLM provider API (OpenAI in example) · Models: OpenAI, LangChain · [Repo](https://github.com/vibrantlabsai/ragas) · [📖 Docs ↗](https://docs.ragas.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ragas/)</sub>

<a name="agentops"></a>
### #&#8288;37 [agentops](https://github.com/agentops-ai/agentops) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (19) · Freshness: recent (72) · Maintenance: weak (4) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · MIT · Jun 2026</sub>

**Tracing, session replay and LLM cost tracking for AI agents.**

AgentOps is a Python SDK plus a dashboard and API backend that records agent runs as spans, with session replay, execution graphs and per-provider LLM spend. Decorators (@session, @agent, @operation, @task, @workflow) and integrations for OpenAI Agents SDK, CrewAI, AG2, LangChain, Anthropic, Mistral, Cohere and LiteLLM feed the traces. The app is MIT-licensed and can be self-hosted using app/README.md.

- **+** Two-line init plus span decorators; supports async functions and generators
- **+** Integrations for OpenAI Agents SDK, CrewAI, AG2, LangChain, Anthropic, Mistral, Cohere
- **+** Session replay, execution graphs and LLM cost tracking in one dashboard
- **+** Dashboard and API backend are MIT-licensed and self-hostable
- **−** No Docker or compose files detected; self-hosting steps live in a separate app/README.md
- **−** Quick start points to the hosted dashboard and an API key
- **−** Last release 2025-08-29, well behind recent commits
- **−** README mixes v1 and v2 APIs (end_session vs decorators), which is confusing

<sub>no GPU · Needs AgentOps API key (hosted dashboard) · Models: OpenAI, Anthropic, Mistral, Cohere, LiteLLM · [Repo](https://github.com/agentops-ai/agentops) · [📖 Docs ↗](https://docs.agentops.ai/introduction) · [🌐 Site ↗](https://agentops.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentops/)</sub>

<a name="pezzo"></a>
### #&#8288;38 [Pezzo](https://github.com/pezzolabs/pezzo) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (6) · Freshness: recent (70) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Aug 2026</sub>

**Prompt management, observability and caching for LLM apps.**

Stores and versions prompts, logs requests with cost and latency, and caches LLM responses, exposed through Node.js and Python clients and a LangChain integration. Runs on PostgreSQL, ClickHouse, Redis and SuperTokens via Docker Compose, with a GraphQL API server and a console UI. For small teams that want prompt delivery without code changes.

- **+** Prompts delivered from the console without redeploying application code
- **+** Built-in response caching to cut repeated-call cost and latency
- **+** Node.js and Python clients plus LangChain support
- **+** Apache-2.0; infra is all open source (PostgreSQL, ClickHouse, Redis, SuperTokens)
- **−** Last commit August 2026 with no release notes in the README
- **−** Four backing services for a modest feature set
- **−** README is thin; features are shown as screenshots, details only in docs
- **−** No evaluation or dataset features mentioned

<sub>no GPU · Compose · Needs PostgreSQL, ClickHouse, Redis, SuperTokens, Node.js 18+ · port 4200 · [Repo](https://github.com/pezzolabs/pezzo) · [📖 Docs ↗](https://docs.pezzo.ai/) · [🌐 Site ↗](https://pezzo.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pezzo/)</sub>

<a name="coai"></a>
### #&#8288;39 [CoAI](https://github.com/coaidev/coai) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: known (47) · Freshness: slowing (50) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · Mar 2026</sub>

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

<a name="metamcp"></a>
### #&#8288;40 [MetaMCP](https://github.com/metatool-ai/metamcp) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: niche (3) · Freshness: active (81) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · MIT · Jun 2026</sub>

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
### #&#8288;41 [mcpo](https://github.com/open-webui/mcpo) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (10) · Freshness: recent (57) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · MIT · Feb 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
