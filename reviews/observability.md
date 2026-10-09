# 📈 Observability reviews · Best of Self-Hosted AI

Tracing, evaluation and prompt management for LLM applications. Back to the [leaderboard](../README.md#-observability).

<a name="langfuse"></a>
### 🥇 [Langfuse](https://github.com/langfuse/langfuse) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · custom license · Oct 2026</sub>

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

<sub>no GPU · Compose · Needs ClickHouse · [Repo](https://github.com/langfuse/langfuse) · [▶️ Demo ↗](https://langfuse.com/demo) · [📖 Docs ↗](https://langfuse.com/docs) · [🌐 Site ↗](https://langfuse.com)</sub>

<a name="phoenix"></a>
### 🥈 [Phoenix](https://github.com/arize-ai/phoenix) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (79) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · custom license · Oct 2026</sub>

**OpenTelemetry-based LLM tracing, evals and prompt playground.**

Collects traces through OpenInference and OpenTelemetry instrumentation for OpenAI Agents SDK, Claude Agent SDK, LangGraph, CrewAI, LlamaIndex and DSPy, then adds LLM-based response evals, datasets, experiments and a prompt playground. Starts with pip install arize-phoenix and phoenix serve, ships Docker images and a Helm chart, and exposes a remote MCP endpoint at /mcp. For engineers troubleshooting LLM apps.

- **+** Single pip package runs the whole platform; uvx arize-phoenix serve needs no install
- **+** Remote MCP server at /mcp for Claude Code and Cursor; built-in PXI agent
- **+** Vendor and language agnostic via OpenTelemetry and OpenInference
- **+** One-click deploys for Railway, Render, Cloud Run, Azure and AWS CloudFormation
- **−** License is non-standard (GitHub reports NOASSERTION); check terms before deploying
- **−** Managed production workflows are steered to the paid Arize AX product
- **−** Azure template serves plain HTTP; needs a TLS proxy before production
- **−** TypeScript evals package is alpha; stdio MCP package is in maintenance mode

<sub>no GPU · Docker + Compose · Models: OpenAI, Anthropic, Google GenAI and ADK, AWS Bedrock, OpenRouter · port 6006 · [Repo](https://github.com/arize-ai/phoenix) · [📖 Docs ↗](https://arize.com/docs/phoenix/) · [🌐 Site ↗](https://phoenix.arize.com)</sub>

<a name="mlflow"></a>
### 🥉 [MLflow](https://github.com/mlflow/mlflow) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: any LLM provider via autolog or the AI Gateway · port 5000 · [Repo](https://github.com/mlflow/mlflow) · [▶️ Demo ↗](https://demo.mlflow.org/) · [📖 Docs ↗](https://mlflow.org/docs/latest) · [🌐 Site ↗](https://mlflow.org/)</sub>

<a name="promptfoo"></a>
### #&#8288;4 [promptfoo](https://github.com/promptfoo/promptfoo) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: easy (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker · Needs Node.js (npm) or Python (pip), LLM provider API key or Ollama · Models: OpenAI, Anthropic, Azure, Bedrock, Ollama · [Repo](https://github.com/promptfoo/promptfoo) · [📖 Docs ↗](https://www.promptfoo.dev/docs/) · [🌐 Site ↗](https://www.promptfoo.dev)</sub>

<a name="opik"></a>
### #&#8288;5 [Opik](https://github.com/comet-ml/opik) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Compose · Models: any LLM via SDK, OpenTelemetry or framework integrations (Google ADK, AG2, Autogen, Flowise) · port 5173 · [Repo](https://github.com/comet-ml/opik) · [📖 Docs ↗](https://www.comet.com/docs/opik/) · [🌐 Site ↗](https://www.comet.com/site/products/opik/)</sub>

<a name="latitude-llm"></a>
### #&#8288;6 [Latitude](https://github.com/latitude-dev/latitude-llm) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: OpenAI, Anthropic, Bedrock, Vercel AI SDK and LangChain apps, any OpenTelemetry source · [Repo](https://github.com/latitude-dev/latitude-llm) · [📖 Docs ↗](https://docs.latitude.so) · [🌐 Site ↗](https://latitude.so)</sub>

<a name="future-agi"></a>
### #&#8288;7 [Future AGI](https://github.com/future-agi/future-agi) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: fair (72) · Easy to run: very easy (83) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · Apache-2.0 · Oct 2026</sub>

**Evals, tracing, simulations, guardrails and a gateway for agents in one stack.**

Bundles OpenTelemetry tracing for 50+ frameworks, 50+ evaluation metrics, persona-driven text and voice simulations, 18 guardrail scanners, six prompt-optimization algorithms and a Go gateway with 100+ providers. Installs with ./bin/install (Compose v2.24+); Standalone needs 2 vCPUs and 4 GB, Distributed 12 to 16 GB; UI on port 3000, OTLP on 4318. For teams wanting one platform from prototype to production.

- **+** Gateway benchmarks: about 29k req/s on t3.xlarge, P99 under 21 ms with guardrails on
- **+** Voice-agent simulation via LiveKit, VAPI, Retell and Pipecat
- **+** Air-gapped install documented; telemetry off with FUTURE_AGI_TELEMETRY_DISABLED=true
- **+** Signed Helm chart covers both open-source and Enterprise editions
- **−** Marked a nightly release for early testing; stable version pending
- **−** No supported migration from Standalone to Distributed or Helm once data exists
- **−** Distributed profile adds PeerDB and Kafka; needs 4+ vCPUs and 12 to 16 GB
- **−** Images total about 800 MB and first boot takes several minutes

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Needs Docker Compose v2.24+, PostgreSQL, ClickHouse, Redis and Temporal (bundled in compose) · Models: 100+ providers via gateway (OpenAI, Anthropic, Gemini, Bedrock, Azure, Mistral, Groq), Ollama, vLLM, LM Studio, TGI and llamafile · port 3000 · [Repo](https://github.com/future-agi/future-agi) · [📖 Docs ↗](https://docs.futureagi.com) · [🌐 Site ↗](https://futureagi.com)</sub>

<a name="langwatch"></a>
### #&#8288;8 [LangWatch](https://github.com/langwatch/langwatch) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: some setup (33) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · Apache-2.0 · Oct 2026</sub>

**Agent observability, simulation testing, AI gateway and governance in one.**

Traces LLM and agent calls through OpenTelemetry and SDK integrations, runs simulation-based agent tests and evaluations, manages prompts, and adds an OpenAI- and Anthropic-compatible gateway with virtual keys and budgets. Also tracks coding-agent sessions (Claude Code, Codex, Copilot) with cost per pull request, and starts locally with npx @langwatch/server. For platform teams governing AI use across a company.

- **+** npx @langwatch/server starts a local instance with only Node.js installed
- **+** Coding-agent tracking: sessions and cost per PR for Claude Code, Codex, Copilot
- **+** Gateway virtual keys with budgets for customers or employees
- **+** Governance ingests Copilot Studio, Claude and OpenAI compliance APIs, Workato, S3 audit feeds
- **−** Open-core: modules under platform/app/ee need a commercial license in production
- **−** No Dockerfile or compose file at the repo root; production setup is in external docs
- **−** README is a feature index; architecture and storage needs are not described
- **−** Cloud signup is the first call to action; self-host gets one line

<sub>no GPU · Needs Node.js · Models: OpenAI, Anthropic, Azure OpenAI, Vertex AI, Bedrock · [Repo](https://github.com/langwatch/langwatch) · [📖 Docs ↗](https://langwatch.ai/docs/introduction) · [🌐 Site ↗](https://langwatch.ai)</sub>

<a name="openlit"></a>
### #&#8288;9 [OpenLIT](https://github.com/openlit/openlit) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: fair (79) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · Apache-2.0 · Oct 2026</sub>

**OpenTelemetry-native tracing, evals, guardrails and GPU monitoring for agents.**

Receives OTLP on ports 4317 and 4318 from the openlit Python or TypeScript SDK, which auto-instruments 70+ providers, frameworks and vector DBs, and stores GenAI-convention traces in ClickHouse behind a dashboard on port 3000. Adds LLM-as-a-judge evals, prompt-injection guardrails, Prompt Hub, a rule engine, a secrets Vault, OpenGround model comparison and an NVIDIA, AMD and Intel GPU collector. For teams on existing OpenTelemetry stacks.

- **+** Follows OpenTelemetry GenAI semantic conventions; your collector can fan out to other backends
- **+** GPU collector reports utilization, memory, power and temperature correlated with traces
- **+** CLI instruments Claude Code, Cursor, Codex and Windsurf sessions
- **+** Connectors for ClickHouse, Grafana Tempo, Loki, Prometheus and Jaeger
- **−** Coding-agent capture needs a separate CLI install and configure step
- **−** Guardrails run in the SDK, so each app must be updated to use them
- **−** README does not state hardware needs or ClickHouse sizing
- **−** No Dockerfile at the repo root; compose only

<sub>no GPU · Compose · Needs ClickHouse · Models: OpenAI, Ollama, Anthropic, DeepSeek, Cohere · port 3000 · [Repo](https://github.com/openlit/openlit) · [📖 Docs ↗](https://docs.openlit.io/) · [🌐 Site ↗](https://openlit.io)</sub>

<a name="lmnr"></a>
### #&#8288;10 [Laminar](https://github.com/lmnr-ai/lmnr) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · Apache-2.0 · Sep 2026</sub>

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

<sub>no GPU · Compose · Needs ClickHouse, PostgreSQL, LLM provider (optional, for AI features) · Models: Gemini, OpenAI and OpenAI-compatible gateways (LiteLLM, OpenRouter, vLLM), AWS Bedrock, Azure AI Foundry · port 5667 · [Repo](https://github.com/lmnr-ai/lmnr) · [📖 Docs ↗](https://laminar.sh/docs) · [🌐 Site ↗](https://laminar.sh)</sub>

<a name="agenta"></a>
### #&#8288;11 [Agenta](https://github.com/agenta-ai/agenta) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (30) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: hard (0) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · custom license · Oct 2026</sub>

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

<sub>no GPU · Needs Claude Code, Pi or Codex harness, LLM API, Ollama, or a Claude or ChatGPT subscription, Composio (optional, 1,000+ app integrations) · Models: hosted models via API, Ollama, Claude and ChatGPT subscriptions · [Repo](https://github.com/agenta-ai/agenta) · [📖 Docs ↗](https://agenta.ai/docs/) · [🌐 Site ↗](https://agenta.ai)</sub>

<a name="helicone"></a>
### #&#8288;12 [Helicone](https://github.com/helicone/helicone) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (42) · Freshness: active (81) · Maintenance: patchy (33) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Sep 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs Supabase (database and auth), ClickHouse, MinIO, Cloudflare Workers runtime (proxy) · Models: 100+ providers via gateway (OpenAI, Azure, Anthropic, Bedrock, Gemini, Groq, Together, Fireworks, Ollama) · [Repo](https://github.com/helicone/helicone) · [▶️ Demo ↗](https://helicone.ai/demo) · [📖 Docs ↗](https://docs.helicone.ai/) · [🌐 Site ↗](https://www.helicone.ai)</sub>

<a name="pezzo"></a>
### #&#8288;13 [Pezzo](https://github.com/pezzolabs/pezzo) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (13) · Freshness: recent (70) · Maintenance: weak (24) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Aug 2026</sub>

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

<sub>no GPU · Compose · Needs PostgreSQL, ClickHouse, Redis, SuperTokens, Node.js 18+ · port 4200 · [Repo](https://github.com/pezzolabs/pezzo) · [📖 Docs ↗](https://docs.pezzo.ai/) · [🌐 Site ↗](https://pezzo.ai)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
