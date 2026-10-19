# 🔀 Gateways and observability reviews · Best of Open-Source AI

LLM gateways and proxies for routing, caching and cost control, and tracing, evaluation and prompt management for LLM apps. Back to the [leaderboard](../README.md#-gateways-and-observability).

<sub>🌐 Also on the web: [Gateways and observability on archestack.com](https://archestack.com/best-of-ai/gateways/), each project on its own page.</sub>

<a name="litellm"></a>
### 🥇 [LiteLLM](https://github.com/berriai/litellm) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: very easy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 62k · custom license · Oct 2026</sub>

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
### 🥉 [new-api](https://github.com/quantumnous/new-api) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · AGPL-3.0 · Oct 2026</sub>

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
### #&#8288;4 [freellmapi](https://github.com/tashfeenahmed/freellmapi) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · MIT · Oct 2026</sub>

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

<a name="langfuse"></a>
### #&#8288;5 [Langfuse](https://github.com/langfuse/langfuse) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · custom license · Oct 2026</sub>

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

<a name="mlflow"></a>
### #&#8288;6 [MLflow](https://github.com/mlflow/mlflow) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · Apache-2.0 · Oct 2026</sub>

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

<a name="promptfoo"></a>
### #&#8288;7 [promptfoo](https://github.com/promptfoo/promptfoo) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

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

<a name="phoenix"></a>
### #&#8288;8 [Phoenix](https://github.com/arize-ai/phoenix) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (37) · Freshness: active (100) · Maintenance: fair (78) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · custom license · Oct 2026</sub>

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

<a name="mcp-context-forge"></a>
### #&#8288;9 [ContextForge MCP Gateway](https://github.com/ibm/mcp-context-forge) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (90) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · Apache-2.0 · Oct 2026</sub>

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

<a name="opik"></a>
### #&#8288;10 [Opik](https://github.com/comet-ml/opik) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · Apache-2.0 · Oct 2026</sub>

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

<a name="openlit"></a>
### #&#8288;11 [OpenLIT](https://github.com/openlit/openlit) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (80) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Oct 2026</sub>

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

<a name="gomodel"></a>
### #&#8288;12 [GoModel](https://github.com/enterpilot/gomodel) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Oct 2026</sub>

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
### #&#8288;13 [Bifrost](https://github.com/maximhq/bifrost) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;14 [Plano](https://github.com/katanemo/plano) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: easy (50) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

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

<a name="future-agi"></a>
### #&#8288;15 [Future AGI](https://github.com/future-agi/future-agi) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: fair (72) · Easy to run: very easy (83) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Oct 2026</sub>

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

<a name="langwatch"></a>
### #&#8288;16 [LangWatch](https://github.com/langwatch/langwatch) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · Apache-2.0 · Oct 2026</sub>

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

<a name="latitude-llm"></a>
### #&#8288;17 [Latitude](https://github.com/latitude-dev/latitude-llm) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · MIT · Oct 2026</sub>

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

<a name="agentgateway"></a>
### #&#8288;18 [agentgateway](https://github.com/agentgateway/agentgateway) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · Apache-2.0 · Oct 2026</sub>

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

<a name="higress"></a>
### #&#8288;19 [Higress](https://github.com/higress-group/higress) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (77) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

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

<a name="deepeval"></a>
### #&#8288;20 [deepeval](https://github.com/confident-ai/deepeval) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (69) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Oct 2026</sub>

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

<a name="lmnr"></a>
### #&#8288;21 [Laminar](https://github.com/lmnr-ai/lmnr) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: fair (75) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · Apache-2.0 · Oct 2026</sub>

**Rust-based agent tracing with SQL queries, signals and evals.**

OpenTelemetry-native tracing for Vercel AI SDK, LangChain, OpenAI, Anthropic, Gemini and more with one line of SDK code, stored in ClickHouse and queried with SQL from the UI, MCP server or CLI. Signals watch every run for behaviors described in plain English and ping Slack; evals run from an SDK and CLI. docker compose up serves the UI on port 5667, for teams debugging browser and tool-using agents.

- **+** Signals: describe a failure in plain English and get a Slack ping when it occurs
- **+** SQL over traces, spans, metrics and events, also from your coding agent via MCP
- **+** Rust backend with 20x trace compression and a realtime trace viewer
- **+** Custom Postgres schema support for shared database deployments
- **−** Anonymous usage telemetry is on by default; LAMINAR_TELEMETRY_DISABLED=true opts out
- **−** Production is steered to the managed platform or the heavier docker-compose-full stack
- **−** AI features (chat-with-trace, SQL-with-AI) need a configured LLM provider
- **−** ClickHouse upgrades need manual container recreation and log-table truncation

<sub>no GPU · Compose · Needs ClickHouse, PostgreSQL, LLM provider (optional, for AI features) · Models: Gemini, OpenAI and OpenAI-compatible gateways (LiteLLM, OpenRouter, vLLM), AWS Bedrock, Azure AI Foundry · port 5667 · [Repo](https://github.com/lmnr-ai/lmnr) · [📖 Docs ↗](https://laminar.sh/docs) · [🌐 Site ↗](https://laminar.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmnr/)</sub>

<a name="optillm"></a>
### #&#8288;22 [optillm](https://github.com/algorithmicsuperintelligence/optillm) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: fair (61) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Oct 2026</sub>

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

<a name="agenta"></a>
### #&#8288;23 [Agenta](https://github.com/agenta-ai/agenta) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: hard (0) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · custom license · Oct 2026</sub>

**Team workspace for building chat-driven agents that run in Slack and WhatsApp.**

Lets teams create agents by describing work in chat, connect tools through MCP or Composio, set per-agent read or write permissions, and talk to them from the web app, Slack, Telegram or WhatsApp. Agents keep memory and skills, run on schedules or events, and each session gets a sandbox with a browser and filesystem; every run is traced and costed. Runs Claude Code, Pi or Codex harnesses on API models, Ollama or a Claude or ChatGPT subscription.

- **+** Runs on an existing Claude or ChatGPT subscription instead of metered API billing
- **+** Per-agent tool permissions with read or write scopes and human-in-the-loop gates
- **+** Every run traced and cost-tracked; configurations and versions are visible
- **+** Agents reachable from Slack, Telegram and WhatsApp Business
- **−** README no longer covers the earlier prompt-management and evaluation product
- **−** Self-host instructions are delegated to an agent skill, not written out
- **−** Harness support limited to Claude Code, Pi and Codex today
- **−** No Dockerfile or compose file at the repo root

<sub>no GPU · Needs Claude Code, Pi or Codex harness, LLM API, Ollama, or a Claude or ChatGPT subscription, Composio (optional, 1,000+ app integrations) · Models: hosted models via API, Ollama, Claude and ChatGPT subscriptions · [Repo](https://github.com/agenta-ai/agenta) · [📖 Docs ↗](https://agenta.ai/docs/) · [🌐 Site ↗](https://agenta.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agenta/)</sub>

<a name="helicone"></a>
### #&#8288;24 [Helicone](https://github.com/helicone/helicone) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (26) · Freshness: recent (80) · Maintenance: patchy (34) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;25 [Portkey Gateway](https://github.com/portkey-ai/gateway) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (40) · Freshness: recent (77) · Maintenance: weak (3) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · May 2026</sub>

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

<a name="evals"></a>
### #&#8288;26 [evals](https://github.com/openai/evals) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: popular (56) · Freshness: recent (64) · Maintenance: weak (3) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Apr 2026</sub>

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
### #&#8288;27 [ragas](https://github.com/vibrantlabsai/ragas) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: known (47) · Freshness: recent (54) · Maintenance: weak (2) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Feb 2026</sub>

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

<a name="metamcp"></a>
### #&#8288;28 [MetaMCP](https://github.com/metatool-ai/metamcp) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (4) · Freshness: active (82) · Maintenance: weak (3) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · MIT · Jun 2026</sub>

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

<a name="pezzo"></a>
### #&#8288;29 [Pezzo](https://github.com/pezzolabs/pezzo) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (8) · Freshness: recent (70) · Maintenance: weak (27) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Aug 2026</sub>

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

<a name="mcpo"></a>
### #&#8288;30 [mcpo](https://github.com/open-webui/mcpo) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (14) · Freshness: recent (59) · Maintenance: weak (0) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · MIT · Feb 2026</sub>

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
### #&#8288;31 [CoAI](https://github.com/coaidev/coai) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: known (33) · Freshness: recent (52) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · Mar 2026</sub>

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
