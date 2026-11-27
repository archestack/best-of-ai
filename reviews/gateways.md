# 🔀 Gateways and observability reviews · Best of Open-Source AI

LLM gateways and proxies for routing, caching and cost control, and tracing, evaluation and prompt management for LLM apps. Back to the [leaderboard](../README.md#-gateways-and-observability).

<sub>🌐 Also on the web: [Gateways and observability on archestack.com](https://archestack.com/best-of-ai/gateways/), each project on its own page.</sub>

<a name="omniroute"></a>
### 🥇 [OmniRoute](https://github.com/cheaper-inference/omniroute) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 91k · MIT · Nov 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs Provider accounts or API keys, Node.js (npm) or Docker · Models: OpenAI API, Claude API, Gemini API, Responses API · port 20128 · [Repo](https://github.com/cheaper-inference/omniroute) · [🌐 Site ↗](https://omniroute.online) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/omniroute/)</sub>

<a name="headroom"></a>
### 🥈 [headroom](https://github.com/headroomlabs-ai/headroom) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 81k · Apache-2.0 · Nov 2026</sub>

**Compresses tool outputs, logs and history before they reach the LLM.**

Headroom is a Python library, local proxy and CLI that shrinks agent context before it is sent to an LLM provider. It routes JSON, source code and text to separate compressors and keeps originals locally so the model can retrieve them. `headroom wrap` configures coding agents such as Claude Code, Codex, Aider and Cline to go through the proxy.

- **+** Seeded, offline benchmark: 21–57% fewer input tokens across four agent scenarios
- **+** One-command `headroom wrap` for many coding agents, reversible with `headroom unwrap`
- **+** Compression runs locally; reported 0.21 ms p50 on a 10K-token JSON result
- **+** Originals cached locally and retrievable by the model via `headroom_retrieve`
- **−** Little savings on prose or already-dense output; gains depend on repetitive payloads
- **−** Cursor and ZCode need manual base-URL setup; Cortex Code is library-only
- **−** Third-party OpenAI-compatible providers need an extra flag or the key goes to OpenAI
- **−** Output token reduction is off by default and reported as an estimate

<sub>no GPU · Docker + Compose · Needs Python 3.13 (for uv tool install), Serena (installed by headroom wrap), Kompress-v2-base model from Hugging Face · Models: OpenAI, Anthropic, Bedrock, Gemini, OpenAI-compatible providers · port 8787 · [Repo](https://github.com/headroomlabs-ai/headroom) · [📖 Docs ↗](https://docs.headroomlabs.ai/docs) · [🌐 Site ↗](https://headroomlabs.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/headroom/)</sub>

<a name="mlflow"></a>
### 🥉 [MLflow](https://github.com/mlflow/mlflow) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Nov 2026</sub>

**Tracing, evaluation and prompt registry for LLM apps, plus ML tracking.**

MLflow is a Python platform that records OpenTelemetry-based traces of LLM and agent apps, runs evaluations with 50+ built-in metrics and LLM judges, and versions prompts. It also includes an OpenAI-compatible AI Gateway for routing and rate limits, plus classic ML experiment tracking, a model registry and deployment tools. A local server starts with `uvx mlflow server`, and the UI is at port 5000.

- **+** One-line autologging for more than 60 agent frameworks and model providers
- **+** Covers both LLM tracing and evaluation and classic ML tracking and model registry
- **+** Native OpenTelemetry support; works from Python, TypeScript/JavaScript and Java
- **+** Public demo instance with example traces, evaluations and prompts
- **−** Broad scope across LLM and classic ML makes the surface area large to learn
- **−** Setup wizard assumes Claude Code, Codex or OpenCode is installed
- **−** AI Gateway is one component of the platform, not a standalone proxy
- **−** Backing store and artifact storage requirements for production are not detailed in the README excerpt

<sub>no GPU · Docker + Compose · Models: OpenAI, Anthropic, Gemini, Amazon Bedrock, Databricks · port 5000 · [Repo](https://github.com/mlflow/mlflow) · [▶️ Demo ↗](https://demo.mlflow.org/) · [📖 Docs ↗](https://mlflow.org/docs/latest) · [🌐 Site ↗](https://mlflow.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlflow/)</sub>

<a name="new-api"></a>
### #&#8288;4 [new-api](https://github.com/quantumnous/new-api) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · AGPL-3.0 · Nov 2026</sub>

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

<a name="experiential"></a>
### #&#8288;5 [experiential](https://github.com/experientiallabs/experiential) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;6 [llm-gateway](https://github.com/mnfst/llm-gateway) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · MIT · Nov 2026</sub>

**OpenAI-compatible gateway routing requests across providers, subscriptions, local models.**

Manifest LLM Gateway exposes one OpenAI-compatible endpoint in front of 35 built-in provider connections, 18 subscription flows, local runtimes and custom endpoints. Sending "model": "auto" lets it pick the model. It logs full request bodies for successes and errors, tracks spend with limits and notifications, and falls back to other models when a query fails.

- **+** Supports 35 provider connections plus any custom /v1/chat/completions or /v1/messages endpoint
- **+** Can route through 18 subscription flows (e.g. ChatGPT, Claude, Copilot), not only API keys
- **+** Connects local runtimes: Ollama, LM Studio (port 1234), llama.cpp (port 8080)
- **+** Full body logs, cost tracking, limits and model fallback on failure
- **−** Self-hosting is Docker-only; the npm-based path is no longer supported
- **−** Volume-backed templates are single-instance; scaling out needs S3-compatible storage
- **−** Needs a database and recording storage; Postgres appears in the hosted templates

<sub>no GPU · Docker + Compose · Needs Docker, PostgreSQL, S3-compatible storage (for scaled deployments) · Models: OpenAI, Anthropic, Google Gemini, AWS Bedrock, OpenRouter · port 2099 · [Repo](https://github.com/mnfst/llm-gateway) · [📖 Docs ↗](https://manifest.build/llm-gateway/docs/introduction/) · [🌐 Site ↗](https://app.manifest.build) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-gateway/)</sub>

<a name="litellm"></a>
### #&#8288;7 [LiteLLM](https://github.com/berriai/litellm) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · custom license · Nov 2026</sub>

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

<sub>no GPU · Models: OpenAI, Anthropic, Gemini, AWS Bedrock, Azure · port 4000 · [Repo](https://github.com/berriai/litellm) · [📖 Docs ↗](https://docs.litellm.ai/docs/simple_proxy) · [🌐 Site ↗](https://www.litellm.ai/ai-gateway) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/litellm/)</sub>

<a name="freellmapi"></a>
### #&#8288;8 [freellmapi](https://github.com/tashfeenahmed/freellmapi) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Nov 2026</sub>

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
### #&#8288;9 [Langfuse](https://github.com/langfuse/langfuse) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · custom license · Nov 2026</sub>

**LLM tracing, evaluation, prompt management and cost tracking for agent apps.**

Langfuse ingests OpenTelemetry traces from LLM apps and agents and shows them next to cost, latency and quality metrics. It also provides versioned prompt management with a playground, LLM-as-a-judge and manual evaluations, datasets and experiments, and a beta AI gateway. It runs as Langfuse Cloud or self-hosted via Docker Compose, Helm, or Terraform templates for AWS, Azure and GCP.

- **+** Built on OpenTelemetry, so any OTLP-instrumented app or collector can send traces
- **+** Python and JS/TS SDKs plus integrations for LangChain, LlamaIndex, OpenAI, LiteLLM and others
- **+** Covers tracing, prompt versioning, evals, datasets and dashboards in one platform
- **+** Self-host options: Docker Compose, Helm, and Terraform for AWS, Azure and GCP
- **−** Docker Compose suits a single machine or VM; Helm is the preferred production path
- **−** AI Gateway and Skill Management are marked beta
- **−** Detected license is NOASSERTION, while the README badge says MIT
- **−** Self-hosting runs a multi-service stack rather than a single binary

<sub>no GPU · Compose · Compose runs ClickHouse, MinIO, Redis, PostgreSQL · Models: OpenAI, Anthropic, Amazon Bedrock, Ollama, LiteLLM (100+ LLMs) · [Repo](https://github.com/langfuse/langfuse) · [▶️ Demo ↗](https://langfuse.com/docs/demo) · [📖 Docs ↗](https://langfuse.com/docs) · [🌐 Site ↗](https://langfuse.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langfuse/)</sub>

<a name="opik"></a>
### #&#8288;10 [Opik](https://github.com/comet-ml/opik) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Nov 2026</sub>

**LLM tracing, evaluation and prompt management platform for agents and LLM apps.**

Opik records traces of LLM calls and multi-step agent runs through Python and TypeScript SDKs, OpenTelemetry, or framework integrations. It adds datasets, experiments, LLM-as-a-judge metrics, online evaluation rules, a prompt playground and production dashboards. The full server and web app can be self-hosted with a Docker Compose script or a Helm chart, or used on Comet Cloud.

- **+** Full platform, backend included, is Apache-2.0 and self-hostable without a commercial license
- **+** Accepts traces via Python/TypeScript SDKs, OpenTelemetry, and many framework integrations
- **+** Evaluation built in: datasets, experiments, LLM-judge metrics, PyTest integration for CI
- **+** Helm chart for Kubernetes; README claims scale of 40M+ traces/day
- **−** Local self-host runs several containers (databases, backend, UI), heavier than a single binary
- **−** Docker Compose path is described for local development and testing, not production
- **−** Guardrails are an optional extra profile that must be enabled separately
- **−** Opik Cloud is the README's recommended option over self-hosting

<sub>no GPU · Compose · Needs Docker Compose, Kubernetes and Helm (optional) · Models: Provider-agnostic via SDK, OpenTelemetry and integrations (Google ADK, Autogen, AG2, Flowise) · port 5173 · [Repo](https://github.com/comet-ml/opik) · [📖 Docs ↗](https://www.comet.com/docs/opik/) · [🌐 Site ↗](https://www.comet.com/site/products/opik/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opik/)</sub>

<a name="promptfoo"></a>
### #&#8288;11 [promptfoo](https://github.com/promptfoo/promptfoo) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · MIT · Nov 2026</sub>

**CLI and library for evaluating and red-teaming LLM apps.**

Promptfoo runs prompt and model evaluations from a config file, compares providers such as OpenAI, Anthropic, Azure, Bedrock and Ollama side by side, and shows results in the CLI or a web viewer. It also runs red-team vulnerability scans against LLM apps and can scan pull requests for LLM-related security issues. Evals run locally and can be wired into CI/CD.

- **+** Evals run locally, so prompts stay on your machine
- **+** Installs via npm, brew or pip; npx runs it without installing
- **+** Covers both quality evals and red-team scans in one tool
- **+** CI/CD integration and PR code scanning for LLM issues
- **−** Most providers need an API key from the vendor
- **−** Project is now part of OpenAI, though README says it stays MIT
- **−** Config and CLI driven; no hosted demo linked
- **−** Red-team and code-scanning details live only on the external docs site

<sub>no GPU · Docker · Needs Node.js, LLM provider API keys · Models: OpenAI, Anthropic, Azure, Bedrock, Ollama · [Repo](https://github.com/promptfoo/promptfoo) · [📖 Docs ↗](https://www.promptfoo.dev/docs/) · [🌐 Site ↗](https://www.promptfoo.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/promptfoo/)</sub>

<a name="phoenix"></a>
### #&#8288;12 [arize-ai/phoenix](https://github.com/arize-ai/phoenix) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · custom license · Nov 2026</sub>

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

<a name="clawrouter"></a>
### #&#8288;13 [clawrouter](https://github.com/blockrunai/clawrouter) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.7k · MIT · Nov 2026</sub>

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

<a name="axonhub"></a>
### #&#8288;14 [axonhub](https://github.com/looplj/axonhub) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.5k · Apache-2.0 · Nov 2026</sub>

**LLM gateway that translates between OpenAI, Anthropic and Gemini APIs.**

AxonHub is a Go gateway that accepts requests in OpenAI, Anthropic or Gemini format and translates them for the configured provider channel, so a client SDK can call another vendor's model without code changes. It adds request tracing, RBAC with usage quotas, per-request cost tracking and load balancing with failover. Embedding, rerank and image generation endpoints are also supported.

- **+** Cross-format translation: call Claude with the OpenAI SDK or GPT with the Anthropic SDK
- **+** Per-request cost breakdown for input, output and cached tokens, plus thread-level tracing
- **+** Covers text, image generation, embedding and rerank APIs across about a dozen providers
- **+** Public demo instance with a demo account for trying the admin UI
- **−** Realtime API is listed as Todo; AWS Bedrock and Google Cloud channels are still in testing
- **−** Mixed licensing: Apache-2.0 plus LGPL-3.0 for the llm directory
- **−** Deployment is delegated to an agent skill; the README gives no manual install steps
- **−** Main README is mostly Chinese, with sponsor blocks taking much of the page

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL · Models: OpenAI, Anthropic, Gemini, DeepSeek, Zhipu · port 8090 · [Repo](https://github.com/looplj/axonhub) · [▶️ Demo ↗](https://axonhub.reveric.app) · [📖 Docs ↗](https://deepwiki.com/looplj/axonhub) · [🌐 Site ↗](https://github.com/looplj/axonhub) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/axonhub/)</sub>

<a name="ragas"></a>
### #&#8288;15 [ragas](https://github.com/vibrantlabsai/ragas) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="bifrost"></a>
### #&#8288;16 [Bifrost](https://github.com/maximhq/bifrost) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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

<a name="treg"></a>
### #&#8288;17 [treg](https://github.com/superdesigndev/treg) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.8k · custom license · Nov 2026</sub>

**Tool registry proxy giving agents one token for a priced API catalog.**

treg is a proxy and CLI that lets an agent call a catalog of third-party endpoints (SEO, enrichment, scraping, ads, media generation) with one token, billed per call from a prepaid balance. Teams can also register their own API keys, vendor CLIs and SKILL.md bundles, with credentials injected server-side so callers never hold them. It can be self-hosted as a Python server with SQLite, or used via the hosted treg.to.

- **+** Credentials are injected server-side; callers and agents never see provider keys
- **+** Own key takes precedence over treg's and is never metered
- **+** Per-call pricing shown in catalog; 402 response carries balance and top-up URL
- **+** Ships CLI, Claude Code plugin, MCP endpoint and ready-made workflow skills
- **−** Catalog access relies on treg's provider accounts via hosted treg.to, not self-hosting alone
- **−** License is NOASSERTION, so reuse terms are unclear
- **−** Server-side CLI execution is disabled globally; CLIs run locally only
- **−** Sends anonymous usage to PostHog by default when using treg.to

<sub>no GPU · Needs uv, tmux, Node 22.12+ (dashboard build), SQLite, PostHog (CLI telemetry, optional) · port 18790 · [Repo](https://github.com/superdesigndev/treg) · [📖 Docs ↗](https://treg.to/llms.txt) · [🌐 Site ↗](https://treg.to) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/treg/)</sub>

<a name="agenta"></a>
### #&#8288;18 [Agenta](https://github.com/agenta-ai/agenta) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · custom license · Nov 2026</sub>

**Shared team workspace for building and running chat-built agents.**

Agenta is a multi-user workspace where agents are built by chatting, then shared with a team and used in the web app, Slack, Telegram or WhatsApp Business. Agents run on schedules or app events, each session in its own sandbox with a browser and file system, and every run is traced with cost tracking. Integrations go through MCP or Composio (1,000+ apps); models can be hosted APIs or Ollama.

- **+** Multi-user by design: roles, shared agents and chat sessions, per-agent tool permissions
- **+** Each session runs in its own sandbox; model credentials are not exposed to the agent
- **+** Every run is traced and costs are tracked per agent, with versions visible
- **+** Works with hosted model APIs or self-hosted models via Ollama, plus Claude and ChatGPT subscriptions
- **−** Supports only Claude Code, Pi and Codex harnesses today; more are on the roadmap
- **−** Not a visual workflow builder; agents decide steps, so execution is less predictable
- **−** License reported as NOASSERTION by tooling, though the README states MIT

<sub>Needs Composio (optional, for 1,000+ app integrations), Ollama (optional, for self-hosted models) · Models: Hosted model APIs, Ollama, Claude subscription, ChatGPT subscription · [Repo](https://github.com/agenta-ai/agenta) · [▶️ Demo ↗](https://cloud.agenta.ai) · [📖 Docs ↗](https://agenta.ai/docs/) · [🌐 Site ↗](https://agenta.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agenta/)</sub>

<a name="higress"></a>
### #&#8288;19 [Higress](https://github.com/higress-group/higress) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · Apache-2.0 · Nov 2026</sub>

**Istio and Envoy API gateway with LLM proxying and MCP server hosting.**

Higress is a cloud-native API gateway built on Istio and Envoy, extended through Wasm plugins written in Go, Rust or JS. For AI use it proxies many LLM providers behind a unified protocol with token rate limiting, caching, load balancing and observability. It can also host remote MCP servers, including ones converted from OpenAPI specs, and doubles as a Kubernetes ingress controller.

- **+** Wasm plugins in Go/Rust/JS with hot updates, no connection drops on config change
- **+** Streams request and response bodies, including SSE, for LLM traffic
- **+** Hosts MCP servers with auth, rate limiting and audit logs; OpenAPI-to-MCP conversion
- **+** Also a Kubernetes ingress and Gateway API implementation; one-command Docker start
- **−** Heavier to operate than a lightweight LLM proxy; Istio/Envoy concepts apply
- **−** Default images are pulled from Alibaba Cloud registries; mirrors needed in some regions
- **−** Plugin hub and much of the documentation are hosted on higress.cn

<sub>no GPU · Docker · Needs Docker or Kubernetes · Models: multiple domestic and international LLM providers via ai-proxy plugin · port 8001 · [Repo](https://github.com/higress-group/higress) · [▶️ Demo ↗](https://demo.higress.io/) · [📖 Docs ↗](https://higress.cn/en/docs/latest/overview/what-is-higress/) · [🌐 Site ↗](https://higress.ai/en/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/higress/)</sub>

<a name="harbor"></a>
### #&#8288;20 [harbor-framework/harbor](https://github.com/harbor-framework/harbor) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Nov 2026</sub>

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

<a name="langwatch"></a>
### #&#8288;21 [LangWatch](https://github.com/langwatch/langwatch) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · Apache-2.0 · Nov 2026</sub>

**Tracing, evals, prompt management and an LLM gateway for AI apps and coding agents.**

LangWatch traces LLM calls and runs evaluations, agent simulation tests and prompt management. It also includes an OpenAI and Anthropic compatible gateway with virtual keys and budgets, plus coding-agent tracking (cost per pull request) and governance views of AI tool usage. It runs as LangWatch Cloud or self-hosted via `npx @langwatch/server`, and integrates with LangChain, Vercel AI SDK, OpenTelemetry and others.

- **+** Covers tracing, evals, simulation tests, prompt management and a gateway in one platform
- **+** Gateway exposes OpenAI and Anthropic compatible endpoint with virtual keys and budgets
- **+** Works with OpenTelemetry, LangChain, LangGraph, Vercel AI SDK, CrewAI, DSPy and no-code tools
- **+** Quick self-host start with one npx command; Python and npm SDKs under MIT
- **−** Open-core: modules under enterprise/ need a commercial license in production
- **−** Self-host quick start needs Node.js 24+; macOS or glibc Linux only
- **−** Production self-hosting requirements are only in external docs, not the README
- **−** Broad scope (governance, coding agents, gateway) beyond plain observability

<sub>no GPU · Needs Node.js 24+ · Models: OpenAI, Anthropic, Azure OpenAI, Vertex AI, Bedrock · [Repo](https://github.com/langwatch/langwatch) · [📖 Docs ↗](https://langwatch.ai/docs/introduction) · [🌐 Site ↗](https://langwatch.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langwatch/)</sub>

<a name="openllmetry"></a>
### #&#8288;22 [openllmetry](https://github.com/traceloop/openllmetry) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="mcp-context-forge"></a>
### #&#8288;23 [ContextForge MCP Gateway](https://github.com/ibm/mcp-context-forge) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="latitude-llm"></a>
### #&#8288;24 [Latitude](https://github.com/latitude-dev/latitude-llm) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · MIT · Nov 2026</sub>

**Agent observability that groups failures and dispatches coding agents to fix them.**

Captures traces, sessions and tool calls via a one-line SDK (TypeScript, Python) or OpenTelemetry, groups failing traces into tracked signals, then dispatches Claude Code or Cursor with those traces to open a fix PR and replays fixes against regression datasets. The UI is also reachable from an MCP server and CLI; self-hosts from Docker Hub images via Compose or Helm. For teams operating agents in production.

- **+** Signals auto-group failing traces with status, size and trend
- **+** Agent Dispatch sends sample traces to Claude Code or Cursor via Linear or webhooks
- **+** Regression datasets replay fixes against the real failing traces
- **+** MIT license; Compose and Helm paths plus Railway one-click
- **−** README quickstart targets the cloud; self-host steps are in external docs
- **−** Automatic fixing depends on third-party coding agents and their subscriptions
- **−** Claude Code session capture is a separate telemetry package

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL, ClickHouse, Redis · Models: OpenAI, Anthropic, Bedrock, Vercel AI SDK and LangChain apps, any OpenTelemetry source · [Repo](https://github.com/latitude-dev/latitude-llm) · [📖 Docs ↗](https://docs.latitude.so) · [🌐 Site ↗](https://latitude.so) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/latitude-llm/)</sub>

<a name="logfire"></a>
### #&#8288;25 [logfire](https://github.com/pydantic/logfire) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · MIT · Nov 2026</sub>

**Python SDK for OpenTelemetry tracing, with a SQL-queryable hosted backend.**

Logfire is a Python SDK wrapping OpenTelemetry that emits traces, metrics and logs, with instrumentation helpers for packages such as FastAPI and for Pydantic validation. Data goes to the Logfire platform, where it can be queried with SQL. The UI and backend are closed source; self-hosting requires an enterprise license, though the SDK can export to any OTel-compatible backend.

- **+** Built on OpenTelemetry; supports traces, metrics and logs, with TypeScript and Rust SDKs
- **+** Query recorded data with standard SQL, usable from existing BI tools
- **+** One-line integrations like logfire.instrument_fastapi(app), plus Pydantic validation analytics
- **+** SDK can export to any OTel-compatible backend instead of Logfire
- **−** Server, UI and backend are closed source; this repo holds only the SDK and docs
- **−** Self-hosting the platform requires purchasing an enterprise license
- **−** Richest features are Python-centric; other languages use separate SDK repos

<sub>no GPU · Needs Logfire platform or other OTel-compatible backend · [Repo](https://github.com/pydantic/logfire) · [📖 Docs ↗](https://pydantic.dev/docs/logfire/) · [🌐 Site ↗](https://pydantic.dev/logfire) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/logfire/)</sub>

<a name="archestra"></a>
### #&#8288;26 [archestra](https://github.com/archestra-ai/archestra) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · custom license · Nov 2026</sub>

**Self-hosted LLM and MCP gateway with chat, agents, and guardrails.**

Archestra is a self-hosted platform that puts an LLM gateway (Anthropic, OpenAI, Azure, Bedrock, DeepSeek and others) and an MCP gateway with OAuth On-Behalf-Of behind one URL. It adds a private MCP registry, a Kubernetes-based MCP orchestrator, an agent runtime with scheduled, email and webhook triggers, and deterministic tool-call guardrails. Chat front-ends include web, Slack, MS Teams and email, with SSO, RBAC, OpenTelemetry traces and Prometheus metrics.

- **+** Covers LLM, MCP and A2A traffic with cost limits and virtual API keys
- **+** MCP tools run as the calling user via OAuth On-Behalf-Of, not a shared account
- **+** SSO (OIDC, SAML, Okta, Entra), RBAC with team sync, per-environment egress policies
- **+** OpenTelemetry and Prometheus built in; Helm chart and Terraform provider available
- **−** Open core: AGPL-3.0 plus enterprise licensing, free only for teams under 30 users
- **−** Quickstart mounts the Docker socket, which grants broad host access
- **−** The latest tag usually points to a release candidate; production needs pinned versions
- **−** Broad scope (chat, agents, RAG, app builder) makes it heavier than a plain proxy

<sub>no GPU · Needs Docker, PostgreSQL (bundled in quickstart image), Kubernetes (for MCP orchestrator and Helm) · Models: Anthropic, OpenAI, Azure, Bedrock, DeepSeek · port 3000 · [Repo](https://github.com/archestra-ai/archestra) · [📖 Docs ↗](https://archestra.ai/docs/get-started) · [🌐 Site ↗](https://archestra.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/archestra/)</sub>

<a name="giskard-oss"></a>
### #&#8288;27 [giskard-oss](https://github.com/giskard-ai/giskard-oss) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Nov 2026</sub>

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

<a name="tokscale"></a>
### #&#8288;28 [tokscale](https://github.com/junhoyeo/tokscale) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · MIT · Nov 2026</sub>

**CLI and dashboard that tallies token usage and cost across AI coding agents.**

Tokscale is a Rust CLI, distributed on npm, that reads the local session files of dozens of AI coding agents and totals token usage and cost. Supported sources include Claude Code, Codex CLI, OpenCode, Gemini CLI, Copilot CLI, Cursor, Cline and LM Studio. It shows the results in a terminal UI with overview, model, daily, hourly and session views, and can submit them to a public leaderboard on tokscale.ai.

- **+** Reads local session files from 50+ coding agents, so no proxy or code changes are needed
- **+** Terminal UI with overview, models, daily, hourly and session breakdowns
- **+** Covers local inference sources like LM Studio and Unsloth Studio, costed at $0
- **+** MIT license, Rust core, frequent releases
- **−** Some clients need a manual sync step first, such as Amp, Trae, Warp and Antigravity
- **−** Warp data is aggregate requests and spend only, with no token transcripts
- **−** Freebuff token usage is estimated from transcripts, not measured
- **−** Leaderboard submission sends usage data to a hosted service

<sub>no GPU · Docker + Compose · Needs Bun or Node.js (npm package) · Models: Claude Code, Codex CLI, OpenCode, Gemini CLI, GitHub Copilot CLI · [Repo](https://github.com/junhoyeo/tokscale) · [🌐 Site ↗](https://tokscale.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tokscale/)</sub>

<a name="optillm"></a>
### #&#8288;29 [optillm](https://github.com/algorithmicsuperintelligence/optillm) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Nov 2026</sub>

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

<a name="deepeval"></a>
### #&#8288;30 [deepeval](https://github.com/confident-ai/deepeval) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Nov 2026</sub>

**Pytest-style framework for evaluating LLM apps, agents and RAG pipelines.**

DeepEval is a Python library that runs LLM app tests through `deepeval test run`, in the style of Pytest. It ships metrics for RAG, agents, multi-turn chats, MCP, voice and multimodal output, scored by an LLM judge, statistical methods or local NLP models. It also supports tracing for component-level and trajectory evals, synthetic dataset generation, and benchmarks such as MMLU and GSM8K.

- **+** Metrics cover RAG, agent trajectories, multi-turn, MCP, voice and multimodal use cases
- **+** Pytest-style assert_test and deepeval test run fit into existing CI pipelines
- **+** Integrates with LangChain, LangGraph, CrewAI, OpenAI Agents, LlamaIndex, Pydantic AI
- **+** Judge model is configurable, including custom LLMs; some metrics use local NLP models
- **−** Quickstart expects an OPENAI_API_KEY for the LLM-as-a-judge metrics
- **−** README pushes login to the hosted Confident AI platform, a separate commercial product
- **−** Judge-based metrics add LLM calls and cost to every test run
- **−** Library only, installed with pip; no Docker or compose setup

<sub>GPU optional · Needs Python>=3.10, OpenAI API key or custom LLM judge · Models: OpenAI, Anthropic, custom LLMs · [Repo](https://github.com/confident-ai/deepeval) · [📖 Docs ↗](https://deepeval.com/docs/getting-started) · [🌐 Site ↗](https://www.confident-ai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepeval/)</sub>

<a name="switchyard"></a>
### #&#8288;31 [switchyard](https://github.com/nvidia-nemo/switchyard) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · Apache-2.0 · Nov 2026</sub>

**Rust library that routes each agent request to an efficient or capable model.**

Switchyard is a Rust routing library (libsy) that decides which model handles each agent request, mixing efficient and more capable models to trade off task success, cost and latency. Algorithms include Auto (a Stage preset), Task (LLM classifier), Execution (tool-activity signals) and Composite. It embeds in your gateway or harness, with integrations for Agent Router (Envoy), LiteLLM, NeMo Relay and OpenRouter, plus Python and TypeScript bindings.

- **+** Routing can change mid-run using recent tool activity, not only the first prompt
- **+** You keep model clients and credentials; the library only returns the routing decision
- **+** Several algorithms: Auto, Task, Execution, Composite, escalation, advisor, sub-agent, random
- **+** Integrations for Agent Router, LiteLLM, NeMo Relay, OpenRouter; Python and TypeScript bindings
- **−** Pre-1.0: libsy is Beta and its API will change before v1.0
- **−** Standalone server is demo-only, not a supported production path
- **−** LiteLLM integration is experimental and cannot serve classifier or escalation algorithms
- **−** Cheaper calls may not mean cheaper completed tasks; needs your own evaluation

<sub>Docker · Needs Rust toolchain, Python 3 (NeMo Relay plugin source build) · Models: OpenAI-compatible APIs, Anthropic-compatible APIs · [Repo](https://github.com/nvidia-nemo/switchyard) · [📖 Docs ↗](https://nvidia-nemo.github.io/Switchyard/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/switchyard/)</sub>

<a name="semantic-router"></a>
### #&#8288;32 [vllm-project/semantic-router](https://github.com/vllm-project/semantic-router) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · Apache-2.0 · Nov 2026</sub>

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

<sub>Docker · Models: local, private and cloud backends · [Repo](https://github.com/vllm-project/semantic-router) · [📖 Docs ↗](https://vllm-sr.ai/docs/intro/) · [🌐 Site ↗](https://vllm-sr.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/semantic-router/)</sub>

<a name="agentgateway"></a>
### #&#8288;33 [agentgateway](https://github.com/agentgateway/agentgateway) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · Apache-2.0 · Nov 2026</sub>

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

<a name="plano"></a>
### #&#8288;34 [Plano](https://github.com/katanemo/plano) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

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

<a name="evalscope"></a>
### #&#8288;35 [evalscope](https://github.com/modelscope/evalscope) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · Apache-2.0 · Nov 2026</sub>

**Evaluation and stress-testing framework for LLM, VLM and embedding models.**

EvalScope is a Python CLI and library from the ModelScope community that runs benchmarks (MMLU, C-Eval, GSM8K, SWE-bench and many others) against OpenAI-compatible or Anthropic APIs. It also load-tests model services, reporting TTFT and TPOT, and shows results in a web dashboard with model comparison. It can run agent benchmarks in Docker or E2B sandboxes and wraps OpenCompass, VLMEvalKit and RAGEval as backends.

- **+** Large built-in benchmark set covering text, multimodal, embedding, reranker, code and agent tasks
- **+** Evaluates any OpenAI-compatible endpoint with one command, no local GPU required
- **+** Includes perf stress testing with TTFT/TPOT and multi-turn trace replay
- **+** Web dashboard, arena pairwise mode, and extension points for custom datasets and metrics
- **−** Requires Python 3.11 or newer
- **−** Agent and code benchmarks need Docker or an E2B sandbox
- **−** Fast-moving feature set with past breaking changes, such as the v1.0 refactor
- **−** No Docker image or compose file provided in the repository

<sub>GPU optional · Needs Docker or E2B (agent/code benchmarks), OpenCompass, VLMEvalKit, RAGEval (optional backends) · Models: OpenAI-compatible API, Anthropic API, LLM, VLM, Embedding · [Repo](https://github.com/modelscope/evalscope) · [📖 Docs ↗](https://evalscope.readthedocs.io/en/latest/) · [🌐 Site ↗](https://modelscope.github.io/evalscope/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/evalscope/)</sub>

<a name="router"></a>
### #&#8288;36 [weave-os/router](https://github.com/weave-os/router) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Nov 2026</sub>

**Proxy that picks a model per request across Anthropic, OpenAI and Gemini APIs.**

Weave Router is a Go proxy that chooses a model for each request using an embedding and cluster scorer based on Avengers-Pro. It accepts Anthropic Messages, OpenAI Chat Completions and Gemini requests, and forwards to Anthropic, OpenAI, Gemini, OpenRouter or any OpenAI-compatible endpoint. A hosted router is offered, or it can be self-hosted with Postgres and a dashboard.

- **+** Accepts Anthropic, OpenAI and Gemini request formats, with streaming, tool calls and vision
- **+** Installer configures Claude Code, Codex, Copilot, opencode and pi, with on/off switching
- **+** POST /v1/route shows a routing decision without calling a model
- **+** Self-hosted mode includes a dashboard, rk_ keys and OpenTelemetry tracing
- **−** README recommends the Weave-managed router over self-hosting
- **−** Self-hosted HMM policy is frozen, without training, online learning or registry
- **−** Cursor cannot reach a localhost router; needs a public URL and a paid seat
- **−** Multi-replica deployments additionally need Pub/Sub for cache invalidation

<sub>no GPU · Docker + Compose · Needs Docker, Postgres, Go 1.26+, Node 18+ (installer), Provider API key, Pub/Sub (multi-replica) · Models: Anthropic, OpenAI, Gemini, OpenRouter, OpenAI-compatible endpoints · port 8080 · [Repo](https://github.com/weave-os/router) · [📖 Docs ↗](https://github.com/weave-os/router/blob/main/docs/README.md) · [🌐 Site ↗](https://weaveos.com/router/quickstart) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/router/)</sub>

<a name="inspect-ai"></a>
### #&#8288;37 [inspect_ai](https://github.com/ukgovernmentbeis/inspect_ai) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Nov 2026</sub>

**Python framework for running and scoring LLM evaluations.**

Inspect is an evaluation framework from the UK AI Security Institute. It provides built-in components for prompt engineering, tool use, multi-turn dialog and model-graded scoring, and can be extended through separate Python packages. It also ships a collection of over 200 pre-built evaluations that can be run against any model.

- **+** Over 200 pre-built evaluations ready to run on any model
- **+** Extensible through third-party Python packages for new elicitation and scoring techniques
- **+** Built-in support for tool use, multi-turn dialog and model-graded evaluation
- **+** Docs published as Markdown with llms.txt indexes for coding agents
- **−** README covers only development setup, not install or usage; users must go to external docs
- **−** Web UI frontend lives in a git submodule with separate TypeScript setup
- **−** Dev environment requires uv 0.13.4 or later

<sub>Needs uv (for development) · [Repo](https://github.com/ukgovernmentbeis/inspect_ai) · [📖 Docs ↗](https://inspect.aisi.org.uk/) · [🌐 Site ↗](https://inspect.aisi.org.uk/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/inspect-ai/)</sub>

<a name="openlit"></a>
### #&#8288;38 [OpenLIT](https://github.com/openlit/openlit) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · Apache-2.0 · Nov 2026</sub>

**OpenTelemetry-based tracing, evals and guardrails for LLM apps and coding agents.**

OpenLIT is a self-hosted dashboard plus Python and TypeScript SDKs that auto-instrument LLM providers, frameworks and vector databases, and export OpenTelemetry GenAI traces and metrics to ClickHouse. It adds cost tracking, LLM-as-a-judge evals, a versioned Prompt Hub, a Rule Engine, Vault for API keys, runtime guardrails, and GPU monitoring. A CLI installs tracing for Claude Code, Cursor, Codex and OpenCode.

- **+** Follows OpenTelemetry GenAI conventions; OTLP on 4317 (gRPC) and 4318 (HTTP)
- **+** One-line openlit.init() instruments 70+ providers, frameworks and vector DBs
- **+** Covers evals, prompt versioning, guardrails, secrets and cost in one tool
- **+** CLI adds tracing for Claude Code, Cursor, Codex and OpenCode sessions
- **−** Wide scope (Vault, OpenGround, Rule Engine) means more to deploy and learn than a tracer
- **−** Storage is ClickHouse, adding a database to operate
- **−** Guardrails cover only prompt injection, sensitive topics and topic restriction

<sub>GPU optional · Compose · Needs ClickHouse, Docker Compose · Models: OpenAI, Anthropic, Ollama, vLLM, Amazon Bedrock · port 3000 · [Repo](https://github.com/openlit/openlit) · [📖 Docs ↗](https://docs.openlit.io/) · [🌐 Site ↗](https://openlit.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openlit/)</sub>

<a name="trulens"></a>
### #&#8288;39 [trulens](https://github.com/truera/trulens) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Nov 2026</sub>

**Tracing and LLM-judge evaluation for agents and RAG apps on OpenTelemetry.**

TruLens instruments Python LLM apps with an `@instrument` decorator that records each step as an OpenTelemetry span, including latency, inputs, outputs, tokens and cost. It scores those spans with LLM-judge metrics, such as the RAG triad and seven agent evaluators, either inline as the app runs or in batch over a dataset. A leaderboard compares scores, latency and cost across app versions.

- **+** Traces are OTel spans, exportable to any OTLP backend such as Jaeger or Datadog
- **+** Seven agent evaluators, including plan adherence, tool selection and tool calling
- **+** Runs inline or as batch evals over a dataset via the Run API
- **+** Judge providers include OpenAI, Bedrock, Gemini, LiteLLM, HuggingFace and Snowflake Cortex
- **−** Evaluation relies on LLM judges, so most setups need an external model provider
- **−** Python only; instrumentation is by decorator or framework package
- **−** Each provider and app integration is a separate pip package to install
- **−** Headline accuracy figures come from the maintainers' own papers and cited benchmarks

<sub>no GPU · Needs LLM provider for judges (OpenAI, Bedrock, Gemini, LiteLLM, HuggingFace, Snowflake Cortex) · Models: OpenAI, Azure OpenAI, LiteLLM, Google Gemini, AWS Bedrock · [Repo](https://github.com/truera/trulens) · [📖 Docs ↗](https://www.trulens.org/getting_started/) · [🌐 Site ↗](https://www.trulens.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trulens/)</sub>

<a name="inferencex"></a>
### #&#8288;40 [inferencex](https://github.com/semianalysisai/inferencex) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · Apache-2.0 · Nov 2026</sub>

**Continuous inference benchmarks across GPUs and serving frameworks, with public dashboard.**

InferenceX runs automated, repeated benchmarks of open-source inference stacks (SGLang, vLLM, TensorRT-LLM) on NVIDIA, AMD and TPU hardware, so results track software releases instead of going stale. The repo holds end-to-end serving benchmarks, the AgentX long-context multi-turn benchmark, plus experimental collective, kernel, microbenchmark, power-model and video-generation suites. Results are published on a separate open-source dashboard.

- **+** Covers many SKUs: H100/H200, B200/B300, GB200/GB300 NVL72, MI300X to MI355X, TPUv7x
- **+** Benchmarks rerun continuously, with new models added on release day per the news log
- **+** Apache-2.0, with an open-source dashboard in a separate repo
- **+** Includes AgentX, an open long-context multi-turn benchmark, and a standalone harness to test your own server
- **−** Not a tool for serving models; it measures other engines
- **−** Official results need the SemiAnalysis repo and their hardware; forks are labelled unofficial
- **−** Collective, operator, microbenchmark suites are marked experimental beta
- **−** Full runs rely on CI and Slurm clusters with datacenter GPUs

<sub>GPU required · Needs SGLang, vLLM, TensorRT-LLM, Slurm · Models: DeepSeek V4, Kimi K3, Qwen3.5, GLM5, MiniMax M3 · [Repo](https://github.com/semianalysisai/inferencex) · [▶️ Demo ↗](https://inferencex.semianalysis.com/) · [📖 Docs ↗](https://deepwiki.com/SemiAnalysisAI/InferenceX) · [🌐 Site ↗](https://inferencex.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/inferencex/)</sub>

<a name="mcpo"></a>
### #&#8288;41 [mcpo](https://github.com/open-webui/mcpo) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · MIT · Nov 2026</sub>

**Proxy that exposes MCP servers as OpenAPI HTTP endpoints.**

mcpo runs an MCP server (stdio, SSE or Streamable HTTP) and serves its tools as a standard OpenAPI HTTP server with per-tool endpoints, schemas and live docs at /docs. It supports bearer API key auth, a Claude Desktop-style config file for multiple servers with hot reload, and OAuth 2.1 for Streamable HTTP servers. It is aimed at clients like Open WebUI that speak OpenAPI but not stdio MCP.

- **+** Wraps stdio, SSE and Streamable HTTP MCP servers behind one OpenAPI interface
- **+** One instance serves many servers from a config file, each with its own /docs
- **+** API key auth, optional strict auth on docs, HTTPS and root-path options
- **+** Installs with uvx or pip, and a non-root Docker image is provided
- **−** Open WebUI already connects to Streamable HTTP MCP servers natively, reducing need for it
- **−** Default CORS origin is `*`, so it needs tightening for exposed deployments
- **−** OAuth flow opens a local browser and stores tokens in ~/.mcpo/tokens by default
- **−** Setting MCPO_API_KEY through --env or --env-path has no effect

<sub>no GPU · Docker · Needs Python 3.11+, uv (optional), the MCP server being proxied · port 8000 · [Repo](https://github.com/open-webui/mcpo) · [📖 Docs ↗](https://docs.openwebui.com/features/extensibility/plugin/tools/openapi-servers/mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcpo/)</sub>

<a name="lmnr"></a>
### #&#8288;42 [Laminar](https://github.com/lmnr-ai/lmnr) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · Apache-2.0 · Nov 2026</sub>

**Observability platform for AI agents with tracing, evals and SQL-queryable traces.**

Laminar is a Rust-based observability backend for AI agents. Its OpenTelemetry-native TypeScript and Python SDKs trace calls to OpenAI, Anthropic, Gemini, LangChain, Vercel AI SDK, Browser Use and Stagehand. It adds plain-English signals that alert in Slack, an eval SDK and CLI, dashboards, datasets, and MCP/CLI access for SQL queries over traces.

- **+** SDKs for TypeScript and Python start tracing with one initialize call
- **+** Query traces, spans, metrics and events with SQL, including via MCP and CLI
- **+** Signals describe agent behavior in plain English and notify in Slack
- **+** Rust backend with 20x trace compression and full-text search over spans
- **−** README recommends the managed platform or the full compose file for production
- **−** Chat-with-trace and SQL-with-AI need a separately configured LLM provider
- **−** Self-hosted deployments send anonymous telemetry unless disabled by env variable

<sub>no GPU · Compose · Needs ClickHouse, Postgres, Docker Compose · Models: OpenAI, Anthropic, Gemini, AWS Bedrock, Azure AI Foundry · port 5667 · [Repo](https://github.com/lmnr-ai/lmnr) · [📖 Docs ↗](https://laminar.sh/docs) · [🌐 Site ↗](https://laminar.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmnr/)</sub>

<a name="octopus"></a>
### #&#8288;43 [octopus](https://github.com/bestruirui/octopus) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · AGPL-3.0 · Nov 2026</sub>

**LLM API gateway that aggregates provider channels behind one endpoint.**

Octopus is a self-hosted gateway written in Go with a bundled web panel. It groups upstream channels (OpenAI Chat, OpenAI Responses, Anthropic, Gemini) under one model name, converts between OpenAI and Anthropic API formats, and fails over when a channel errors. It also syncs model lists and prices from models.dev, and records request statistics, token use and cost.

- **+** Converts between OpenAI Chat, OpenAI Responses and Anthropic formats; README shows Claude Code and Codex setup
- **+** Single binary with embedded frontend; SQLite by default, MySQL or PostgreSQL optional
- **+** Groups map several provider channels to one model name, with automatic failover
- **+** Syncs model lists and pricing from models.dev, with manual price overrides
- **−** Statistics are batched in memory; kill -9 can lose them
- **−** Default login is admin/admin and must be changed manually
- **−** AGPL-3.0 license may restrict use in proprietary networked services
- **−** Aimed at individuals; README describes no team or multi-user access control

<sub>no GPU · Compose · Needs SQLite (default), MySQL or PostgreSQL · Models: OpenAI Chat, OpenAI Responses, Anthropic, Gemini · port 8080 · [Repo](https://github.com/bestruirui/octopus) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/octopus/)</sub>

<a name="gomodel"></a>
### #&#8288;44 [GoModel](https://github.com/enterpilot/gomodel) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Nov 2026</sub>

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

<a name="cost-xray"></a>
### #&#8288;45 [cost-xray](https://github.com/tigerless-labs/cost-xray) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · MIT · Nov 2026</sub>

**Per-source token and cost breakdown of Claude Code and Codex API requests.**

cost-xray captures the real API traffic from Claude Code and Codex through a local mitmproxy hop. It attributes tokens and dollars to system prompts, tool schemas, MCP servers and individual tool calls, split by cache read, write, fresh and output. Results are browsed in a terminal UI opened with `cx`, and raw traffic is redacted and deduplicated under ~/.cost-xray/.

- **+** Reads raw requests, so system prompt and tool schemas are visible, unlike log-based usage tools
- **+** Prices individual tool calls with cache read/write/fresh split and flags unused MCP servers
- **+** Local only: binds to 127.0.0.1, no telemetry, secrets redacted before writing to disk
- **+** Wrapper falls back to running the agent directly if the proxy is down
- **−** Only Claude Code and Codex supported; other agents need a new adapter module
- **−** Claude per-source split is estimated via tiktoken calibration; only the total is exact
- **−** Forward-only: past sessions are not captured, only runs started after install
- **−** Codex capture needs a scoped local CA; installer runs via curl-pipe-bash, macOS/Linux only

<sub>no GPU · Needs mitmproxy, Claude Code or Codex, systemd (optional, Linux) · Models: Claude Code (Anthropic wire), Codex (OpenAI Responses wire) · [Repo](https://github.com/tigerless-labs/cost-xray) · [🌐 Site ↗](https://tigerless.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cost-xray/)</sub>

<a name="claude-tap"></a>
### #&#8288;46 [claude-tap](https://github.com/liaohch3/claude-tap) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (40) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Nov 2026</sub>

**Local proxy and trace viewer for inspecting AI coding agent API traffic.**

claude-tap wraps a coding-agent CLI (Claude Code, Codex CLI, Gemini CLI, Kimi, OpenCode, Pi, Hermes and others) in a reverse or forward proxy and records the real API requests. A browser viewer shows system prompts, message history, tool schemas, tool calls, reconstructed streaming responses, token usage and diffs between adjacent requests. Traces stay local and can be exported to a self-contained HTML file.

- **+** Covers about 15 clients, including Claude Code, Codex CLI and App, Gemini CLI, and OpenCode
- **+** Structured diff between adjacent requests shows which prompt, tool or parameter changed
- **+** Traces stay on the local machine; common auth headers are redacted before recording
- **+** Exports a session to a self-contained HTML viewer for sharing or archiving
- **−** Codex App capture needs a local CA trusted in the macOS login keychain
- **−** Native AWS Bedrock and Vertex require forward proxy mode; reverse mode breaks SigV4
- **−** Requires Python 3.11+ plus the client being traced; no Docker image
- **−** Tracing only; no routing, caching or cost control as in a full gateway

<sub>no GPU · Needs Python 3.11+, The agent CLI to trace (e.g. Claude Code, Codex CLI) · Models: Anthropic API, OpenAI API, AWS Bedrock, Google Vertex AI, DeepSeek · [Repo](https://github.com/liaohch3/claude-tap) · [📖 Docs ↗](https://github.com/liaohch3/claude-tap/blob/main/docs/guides/agent-trace-viewer.md) · [🌐 Site ↗](https://liaohch3.com/claude-tap/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/claude-tap/)</sub>

<a name="agent-router"></a>
### #&#8288;47 [agent-router](https://github.com/theagentrouter/agent-router) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Nov 2026</sub>

**Envoy-based OpenAI-compatible gateway for LLM providers, self-hosted models and MCP.**

Agent Router, formerly Envoy AI Gateway, exposes one OpenAI-compatible API in front of hosted providers such as OpenAI, Anthropic, Bedrock, Vertex AI and Gemini, plus self-hosted inference and MCP servers. Envoy and Envoy Gateway enforce credentials, routing, quotas, failover and usage attribution on Kubernetes. A standalone `aigw run` CLI starts a local router on port 1975.

- **+** Built on Envoy and Envoy Gateway, with Kubernetes CRDs like AIGatewayRoute and AIServiceBackend
- **+** Two-tier pattern: global auth and rate limits, plus endpoint picker for self-hosted inference
- **+** Supports about 20 listed providers, including OpenAI, Anthropic, Bedrock, Vertex AI, Azure OpenAI and Groq
- **+** Standalone `aigw run` starts a local OpenAI-compatible router on port 1975
- **−** Full deployment requires Kubernetes and Envoy Gateway, which is heavy for small setups
- **−** Renamed from Envoy AI Gateway, so images, CRDs and module paths keep the old names
- **−** README gives no hardware sizing or performance figures
- **−** README lists no built-in tracing or evaluation UI, so observability setup is not described

<sub>no GPU · Docker · Needs Envoy Gateway, Kubernetes · Models: OpenAI, Azure OpenAI, Google Gemini, Vertex AI, AWS Bedrock · port 1975 · [Repo](https://github.com/theagentrouter/agent-router) · [📖 Docs ↗](https://theagentrouter.ai/docs) · [🌐 Site ↗](https://theagentrouter.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-router/)</sub>

<a name="openinference"></a>
### #&#8288;48 [openinference](https://github.com/arize-ai/openinference) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · Apache-2.0 · Nov 2026</sub>

**OpenTelemetry tracing spec and instrumentation libraries for LLM apps and agents.**

OpenInference defines a specification for recording LLM calls, agents, tools, retrievers and embeddings as OpenTelemetry spans, with attributes for inputs, outputs and token counts. It ships auto-instrumentation packages for model providers and agent frameworks in Python, JavaScript, Java and Go. Traces work natively with Arize Phoenix and Arize AX, and with any OpenTelemetry-compatible backend.

- **+** Built on OpenTelemetry, so traces go to any OTel-compatible backend
- **+** Separate packages for many frameworks: LangChain, LlamaIndex, CrewAI, OpenAI Agents, DSPy, MCP
- **+** Published spec and schema registry keep traces consistent across languages
- **+** Covers Python, JavaScript, Java and Go
- **−** Library only: needs a separate backend such as Phoenix to store and view traces
- **−** One package per framework or provider, so each integration is installed separately
- **−** Native support is centered on Arize products (Phoenix, AX)

<sub>no GPU · Needs OpenTelemetry-compatible backend (e.g. Arize Phoenix) · Models: OpenAI, Anthropic, AWS Bedrock, VertexAI, Google GenAI · [Repo](https://github.com/arize-ai/openinference) · [🌐 Site ↗](https://openinf.dev/spec/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openinference/)</sub>

<a name="future-agi"></a>
### #&#8288;49 [Future AGI](https://github.com/future-agi/future-agi) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · Apache-2.0 · Nov 2026</sub>

**Evaluation, tracing, simulation and gateway platform for LLM agents.**

Future AGI is a self-hostable platform that traces agents over OpenTelemetry, scores outputs with 50+ evaluation metrics, simulates multi-turn text and voice conversations, and applies guardrails. It includes a Go OpenAI-compatible gateway (Agent Command Center) and six prompt-optimization algorithms. The backend is Django with PostgreSQL, ClickHouse, Redis and Temporal.

- **+** Covers tracing, evals, simulation, guardrails and gateway in one deployment
- **+** OTLP tracing with instrumentors for 50+ frameworks, Python and TypeScript SDKs
- **+** Gateway lists 100+ providers, 15 routing strategies, semantic caching and a benchmark harness
- **+** Standalone install runs from published images with one command on 2 vCPUs and 4 GB
- **−** Standalone data cannot be moved to Distributed or Helm later
- **−** Distributed setup needs 4+ vCPUs, 12-16 GB, plus Kafka and PeerDB
- **−** Many moving parts to operate: Postgres, ClickHouse, Redis, Temporal, Django and Go services
- **−** Some features and support, such as air-gapped help, go through sales or the Enterprise edition

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Needs Docker Compose v2.24+, PostgreSQL, ClickHouse, Redis, Temporal · Models: OpenAI-compatible HTTP, 100+ providers via gateway · port 3000 · [Repo](https://github.com/future-agi/future-agi) · [▶️ Demo ↗](https://www.youtube.com/watch?v=6keOTAOUUWI) · [📖 Docs ↗](https://docs.futureagi.com) · [🌐 Site ↗](https://futureagi.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/future-agi/)</sub>

<a name="clawmetry"></a>
### #&#8288;50 [clawmetry](https://github.com/vivekchand/clawmetry) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 440 · MIT · Nov 2026</sub>

**Dashboard for agent session timelines, tool calls and cost.**

ClawMetry tails the session files and logs that agent runtimes already write. It shows session timelines, tool-by-tool replay, token and cost breakdowns, and looping or repeated-failure signals in a web dashboard on localhost:8900. It supports 32 runtimes, including Claude Code, Codex, Cursor and Goose, with no SDK or code change. The MIT package reads only four runtimes; the rest need a closed-source companion on a paid plan.

- **+** Reads existing session files; no SDK or instrumentation, and no added overhead in the agent process
- **+** Covers 32 agent runtimes in one dashboard with a per-runtime switcher
- **+** Context-window usage is sized per provider, and /api/context-coverage reports where it cannot see compaction
- **+** Egress is documented in docs/EGRESS.md; no session data leaves unless `clawmetry connect` is run
- **−** Free package reads only OpenClaw, NemoClaw, Goose and Qwen Code; the other 28 need a paid plan
- **−** Support for the other 28 runtimes lives in a closed-source `clawmetry-pro` companion
- **−** Anonymous install ping and PyPI version check run by default, opt-out
- **−** Daemon sustains about 12% of one core, above the project's own 5-10% budget

<sub>no GPU · Docker + Compose · Needs Python 3.8+, at least one supported agent runtime on the same machine · Models: Anthropic, OpenAI, Google, xAI, DeepSeek · port 8900 · [Repo](https://github.com/vivekchand/clawmetry) · [🌐 Site ↗](https://clawmetry.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clawmetry/)</sub>

<a name="search2ai"></a>
### #&#8288;51 [search2ai](https://github.com/fatwang2/search2ai) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Nov 2026</sub>

**Search gateway with provider fallback, exposed over MCP, HTTP API and a JS library.**

search2ai routes search, news and page-extraction calls to the providers you configure (Search1API, Tavily, Brave, Exa, SearXNG, Firecrawl and others). It tries them in a per-operation order, falls back on rate limits, timeouts or errors, and reports which one answered in `warnings`. It runs as a Node 22.18+ CLI, a Hono-mountable service, or a library, and has an optional chat proxy for tool-calling models.

- **+** Per-operation fallback chains for search, news and crawl, with failure reasons returned in warnings
- **+** Same gateway usable as stdio or Streamable HTTP MCP, REST API, library, or Hono routes
- **+** Compatibility endpoints for Exa, Tavily, Search1API, SearXNG and Firecrawl single-page clients
- **+** In-memory cache, Cloudflare KV cache, and optional bearer-key auth via AUTH_KEYS
- **−** Search returns 503 until at least one provider is configured
- **−** Filter support varies by adapter; unsupported filters may be silently ignored without fallback
- **−** Queries only the first working provider, so no result merging across providers
- **−** Compatibility endpoints cover single-page scrape only; no whole-site crawl or task APIs

<sub>no GPU · Docker · Needs Node.js >= 22.18, At least one search provider (Search1API, Tavily, Brave, Exa, SearXNG, etc.), Cloudflare KV (optional cache) · Models: Optional chat proxy for tool-calling models via configured upstream · port 3014 · [Repo](https://github.com/fatwang2/search2ai) · [📖 Docs ↗](https://github.com/fatwang2/search2ai/blob/main/docs/compatibility.md) · [🌐 Site ↗](https://s1.dev/open-source/search2ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/search2ai/)</sub>

<a name="dashclaw"></a>
### #&#8288;52 [dashclaw](https://github.com/ucsandman/dashclaw) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 318 · MIT · Nov 2026</sub>

**Approval and policy layer that blocks risky agent tool calls before they run.**

DashClaw scores each agent tool call against policies and returns allow, warn, allow_contained, require_approval or block. Hooks for Claude Code, Codex and Hermes, plus the OpenClaw gateway, can cancel the call, and approvals can be resolved remotely from a web inbox, CLI, PWA, Telegram or Discord. Decisions go to a ledger with Ed25519 receipts where issued. SDK, REST and generic MCP integrations are cooperative only.

- **+** Fail-closed PreToolUse hooks (exit 2) for Claude Code, Codex and Hermes
- **+** Remote approval via web inbox, CLI, phone PWA, Telegram or Discord
- **+** Signed decision ledger with Ed25519 receipts and signed exports
- **+** `npx dashclaw up` provisions Postgres, secrets, API key and hooks locally
- **−** Enforcement is cooperative for bare SDK, REST and ordinary MCP callers
- **−** Hook runs at the agent's privilege; tamper resistance needs container or separate OS user
- **−** First commit February 2026; README says it is not battle-tested at scale
- **−** Day-to-day maintenance is done by an AI agent under a human charter

<sub>no GPU · Docker + Compose · Needs Postgres (Docker or embedded), Node 20+ · port 3000 · [Repo](https://github.com/ucsandman/dashclaw) · [▶️ Demo ↗](https://www.dashclaw.io/demo) · [📖 Docs ↗](https://dashclaw.io/docs) · [🌐 Site ↗](https://dashclaw.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dashclaw/)</sub>

<a name="evidently"></a>
### #&#8288;53 [evidently](https://github.com/evidentlyai/evidently) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · Apache-2.0 · Sep 2026</sub>

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

<a name="harvey-labs"></a>
### #&#8288;54 [harvey-labs](https://github.com/harveyai/harvey-labs) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Nov 2026</sub>

**Benchmark and harness for evaluating LLM agents on legal tasks.**

Harvey LAB is a dataset of 2,010 legal tasks across 24 practice areas plus contracting, each with agent instructions, documents and rubrics. It also ships an execution harness and grader as the `lab-core` Python package, which runs agents against the tasks and scores them with all-pass rubrics and an LLM judge. Reports and comparison dashboards are covered in the tutorial.

- **+** 2,010 tasks with documents and rubrics across 24 practice areas plus contracting
- **+** Harness and grader installable as a `lab-core` wheel, usable outside the repo
- **+** Tutorial walks one M&A data-room task from setup through scoring and reports
- **+** Releases are tagged and a changelog lists changes that move scores
- **−** Scores from different releases are not always comparable
- **−** Grading .docx output requires pandoc 3.5 or later installed separately
- **−** Domain-specific to legal work; not a general agent benchmark
- **−** Grading relies on an LLM judge, so results depend on the judge model

<sub>Needs pandoc >= 3.5 (for .docx grading), uv · [Repo](https://github.com/harveyai/harvey-labs) · [🌐 Site ↗](https://www.harvey.ai/blog/introducing-harveys-legal-agent-benchmark) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/harvey-labs/)</sub>

<a name="helicone"></a>
### #&#8288;55 [Helicone](https://github.com/helicone/helicone) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (64) · Freshness: recent (76) · Maintenance: patchy (37) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Nov 2026</sub>

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

<a name="weave"></a>
### #&#8288;56 [wandb/weave](https://github.com/wandb/weave) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Nov 2026</sub>

**Python tracing and evaluation toolkit for LLM apps and agents.**

Weave is a Python library from Weights & Biases that traces agent conversations, turns, LLM calls and tool calls, and runs evaluations on LLM applications. It autopatches the OpenAI Agents SDK, Claude Agent SDK, Google ADK and the OpenAI client after weave.init(), and offers @weave.op and a Conversation SDK for custom code. Traces are sent to a W&B project and viewed in its Agents and Calls tabs.

- **+** Autopatches OpenAI Agents SDK, Claude Agent SDK and Google ADK with one weave.init() call
- **+** @weave.op traces arbitrary Python functions, including evaluations and scorers
- **+** Conversation SDK (start_conversation, start_turn, start_llm) covers custom agent loops
- **+** Apache-2.0 client library installable with pip, Python 3.10+
- **−** Needs a W&B account and WANDB_API_KEY; README describes no self-hosted trace server
- **−** Trace server is developed in wandb/core, not in this repository
- **−** Repo still holds paused 'Weave engine' and 'boards' code being cleaned up
- **−** Provider name must be passed explicitly in custom agent tracing; it is not inferred

<sub>no GPU · Needs Weights & Biases account and API key, Python 3.10+ · Models: OpenAI, OpenAI Agents SDK, Claude Agent SDK, Google ADK · [Repo](https://github.com/wandb/weave) · [📖 Docs ↗](https://wandb.me/weave) · [🌐 Site ↗](https://wandb.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/weave/)</sub>

<a name="traceroot"></a>
### #&#8288;57 [traceroot](https://github.com/traceroot-ai/traceroot) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · custom license · Nov 2026</sub>

**LLM tracing, detectors and evals that feed fixes back to your coding agent.**

Traceroot records model calls, tool calls and responses from agent applications, with inputs, outputs, latency and cost. Detectors flag production runs that miss defined behavior, and flagged runs are clustered into signals. A background agent investigates traces and connected GitHub code in a sandbox, and offline evals check the changes. Python and TypeScript SDKs cover frameworks such as LangChain, CrewAI and the OpenAI Agents SDK.

- **+** Closes the loop: tracing, detectors, signals and dataset evals in one tool
- **+** Python and TypeScript SDKs with integrations for 14 agent frameworks and 5 providers
- **+** CLI setup command has a coding agent add instrumentation and waits for first trace
- **+** Self-hostable with Docker Compose via make prod-lite; hosted cloud also available
- **−** Mixed licensing: Apache 2.0 outside ee directories, Enterprise License inside them
- **−** Several provider integrations (Gemini, Mistral) are Python only
- **−** Signals feature relies on a sandboxed coding agent and GitHub connection
- **−** Self-hosting needs Git, Docker Compose and Make; resource requirements not documented

<sub>no GPU · Docker + Compose · Needs Docker Compose, Make, Git · Models: OpenAI, Anthropic, Google Gemini, Mistral, OpenRouter · port 3000 · [Repo](https://github.com/traceroot-ai/traceroot) · [📖 Docs ↗](https://traceroot.ai/docs) · [🌐 Site ↗](https://traceroot.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/traceroot/)</sub>

<a name="coze-loop"></a>
### #&#8288;58 [coze-loop](https://github.com/coze-dev/coze-loop) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (61) · Freshness: active (89) · Maintenance: patchy (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Nov 2026</sub>

**Prompt playground, evaluation and tracing platform for developing and monitoring AI agents.**

Coze Loop is the open-source edition of ByteDance's agent development and operations platform. It covers prompt authoring with a playground and version management, evaluation sets, evaluators and experiments, and trace reporting through SDKs in three languages. Models are connected through the Eino framework, with OpenAI and Volcengine Ark named in the README.

- **+** Combines prompt versioning, evaluation experiments and trace observation in one deployable service
- **+** Side-by-side playground comparison of output from different LLMs
- **+** Deploys via Docker Compose (make compose-up) or a Helm chart for Kubernetes
- **+** SDK works with both the commercial and open-source editions
- **−** Open-source edition exposes only core modules of the commercial product
- **−** README setup examples centre on Volcengine Ark; other providers are documented only in the wiki
- **−** README warns of SSRF, open registration and some privilege-escalation risks on public networks

<sub>no GPU · Needs Docker Engine, Docker Compose, Kubernetes and Helm (optional), LLM provider API key · Models: OpenAI, Volcengine Ark, BytePlus ModelArk, Models supported via Eino · port 8082 · [Repo](https://github.com/coze-dev/coze-loop) · [📖 Docs ↗](https://github.com/coze-dev/coze-loop/wiki/2.-Quickstart) · [🌐 Site ↗](https://www.coze.cn/loop) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/coze-loop/)</sub>

<a name="openevals"></a>
### #&#8288;59 [openevals](https://github.com/langchain-ai/openevals) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Nov 2026</sub>

**Prebuilt LLM-as-judge and other evaluators for LLM apps, in Python and TypeScript.**

OpenEvals is a Python and TypeScript library of evaluators for LLM applications. It provides a create_llm_as_judge factory with prebuilt prompts (correctness, conciseness, RAG groundedness, safety and others), plus exact match, Levenshtein, embedding similarity, structured-output, code type-check and agent trajectory evaluators. It also supports multiturn simulation with simulated users and can log results to LangSmith.

- **+** Same evaluator API in Python and TypeScript
- **+** Judge prompts are plain f-strings you can print and edit
- **+** Judge model configurable via LangChain chat models or the OpenAI client
- **+** Covers RAG, code, extraction, trajectory and multiturn evals beyond LLM-as-judge
- **−** LLM-as-judge evaluators need an external model and API key, OpenAI in the quickstart
- **−** Prebuilt prompts do not define score meanings for continuous or choices scoring
- **−** Agent-specific evals are pointed to the separate agentevals package
- **−** Defaults to LangChain integrations; judge models must support structured output

<sub>no GPU · Needs LLM provider API key (OpenAI in quickstart), langchain_openai (installed by default), LangSmith (optional) · Models: OpenAI, Anthropic, LangChain chat models · [Repo](https://github.com/langchain-ai/openevals) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openevals/)</sub>

<a name="chainforge"></a>
### #&#8288;60 [chainforge](https://github.com/ianarawjo/chainforge) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · MIT · Oct 2026</sub>

**Visual node editor for comparing prompts and models across LLMs.**

ChainForge is a node-based web app for testing prompts against several LLMs at once. It takes the cross product of prompt template variables, models and settings, then scores responses with Python or LLM-based evaluators and plots the results. Built on ReactFlow and Flask, it installs with pip and serves on localhost:8000, with a feature-limited hosted version online.

- **+** Expands prompt templates into every combination of inputs, models and settings in one run
- **+** Evaluator nodes, plots and an inspector table, with export to Excel xlsx
- **+** Covers OpenAI, Anthropic, Gemini, Bedrock, Ollama, plus custom provider scripts
- **+** Installs with pip install chainforge; ships 188 example flows from OpenAI evals
- **−** Plots support only numeric and boolean metrics
- **−** Hosted web version lacks Python evaluators, env-var keys and Ollama
- **−** Local server refuses non-localhost hostnames unless added with --allowed-hosts
- **−** FAISS retrieval needs a manual install and limits OpenMP to one thread

<sub>no GPU · Docker + Compose · Needs Python 3.10+, LLM provider API keys or Ollama · Models: OpenAI, Anthropic, Google Gemini, DeepSeek, HuggingFace · port 8000 · [Repo](https://github.com/ianarawjo/chainforge) · [▶️ Demo ↗](https://chainforge.ai/play/) · [📖 Docs ↗](https://chainforge.ai/docs/) · [🌐 Site ↗](https://chainforge.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chainforge/)</sub>

<a name="orcarouter-lite"></a>
### #&#8288;61 [orcarouter-lite](https://github.com/continuum-ai-corp/orcarouter-lite) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (40) · Freshness: active (98) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Nov 2026</sub>

**LLM router that tracks and caps coding-agent spend, with a menu-bar app.**

OrcaRouter Lite is a local or self-hosted router that accepts OpenAI, Anthropic and Gemini API requests and forwards them to your provider keys. A menu-bar desktop app connects coding agents such as Claude Code, Codex, Gemini CLI and OpenCode, splits spend per agent against a daily budget, and falls back to other providers or hosted OrcaRouter on failure. model="auto" picks the cheapest model that supports the required capabilities.

- **+** Per-agent keys split spend, and disconnecting an agent revokes its access at once
- **+** Native Anthropic, Responses, Gemini and OpenAI endpoints share one routing pipeline
- **+** SQLite by default; Postgres and Redis are optional
- **+** One-click connect edits agent configs for many agents, with backup and restore
- **−** SSO/SCIM, role-based access and fleet-wide budgets are only in paid hosted OrcaRouter
- **−** Desktop installers ship only from the next tagged release; until then use uvx
- **−** Cline, Cursor, Zed and OpenHands need a manual paste of URL and key
- **−** Hosted fallback needs an OrcaRouter account and routes those requests through their service

<sub>no GPU · Docker + Compose · Needs Provider API keys (e.g. OpenAI) or an OrcaRouter key, SQLite (default), Postgres (optional), Redis (optional) · Models: OpenAI API, Anthropic API, Gemini API, 100+ models from LiteLLM pricing catalog · port 8000 · [Repo](https://github.com/continuum-ai-corp/orcarouter-lite) · [📖 Docs ↗](https://docs.orcarouter.ai/introduction) · [🌐 Site ↗](https://www.orcarouter.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/orcarouter-lite/)</sub>

<a name="llmrouter"></a>
### #&#8288;62 [llmrouter](https://github.com/ulab-uiuc/llmrouter) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (36) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · MIT · Nov 2026</sub>

**Python library for training and running routers that pick an LLM per query.**

LLMRouter is a Python library and CLI for training, evaluating and running routers that choose which LLM answers each query, based on cost and expected quality. It ships 16+ routers (KNN, SVM, MLP, matrix factorization, Elo, graph-based, personalized, multi-round), a data pipeline over 11 benchmarks, a Gradio chat UI, and an OpenAI-compatible server for OpenClaw.

- **+** 16+ router implementations behind one llmrouter CLI for training, inference and chat
- **+** Data pipeline builds routing training data from 11 benchmarks, plus multimodal tasks
- **+** Works with OpenAI-compatible endpoints, including Ollama, vLLM and SGLang on localhost
- **+** Custom routers can be added through a plugin workflow; installable from PyPI
- **−** Learned routers need a data generation run that calls paid or rate-limited model APIs
- **−** No Docker or compose files; install is pip or conda only
- **−** Router-R1 support needs a GPU and pins vllm 0.6.3 with torch 2.4.0
- **−** No tagged GitHub release; versions are tracked on PyPI only

<sub>GPU optional · Needs Python 3.10, LLM provider API keys (NVIDIA, OpenAI, Anthropic) or a local OpenAI-compatible server · Models: OpenAI-compatible APIs, NVIDIA endpoints, OpenAI, Anthropic, Ollama · [Repo](https://github.com/ulab-uiuc/llmrouter) · [📖 Docs ↗](https://ulab-uiuc.github.io/LLMRouter/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llmrouter/)</sub>

<a name="metorial"></a>
### #&#8288;63 [metorial](https://github.com/metorial/metorial) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: known (41) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · custom license · Nov 2026</sub>

**MCP gateway with SSO, per-user OAuth, permissions and audit logs for agents.**

Metorial sits between AI clients or agents (Claude, Cursor, Codex, custom agents) and the systems they call, exposing MCP servers, tools and skills behind one URL. It handles OAuth and API-key lifecycles, RBAC, SAML SSO, scoped credentials and audit logs recording which agent acted with whose credentials. TypeScript and Python SDKs ship adapters for Vercel AI SDK, OpenAI, Anthropic, Gemini, LangChain and PydanticAI.

- **+** Per-user OAuth, RBAC and SAML SSO with audit trail of agent actions
- **+** Claims 1200+ integrations; the linked index lists 5000+ MCP servers
- **+** SDK adapters for about ten frameworks, in TypeScript and Python
- **+** Dashboard has an MCP explorer and recorded sessions for debugging
- **−** Self-hosting engine lives in a separate repo (metorial-platform), not this one
- **−** Stack needs PostgreSQL, Redis and MongoDB plus Docker for MCP servers
- **−** License is reported as NOASSERTION; README says Apache 2.0 for the catalog only
- **−** README pushes the hosted platform; quick starts require a Metorial API key

<sub>no GPU · Needs Docker, PostgreSQL, Redis, MongoDB, Bun · Models: OpenAI, Anthropic, Google Gemini, Mistral, DeepSeek · [Repo](https://github.com/metorial/metorial) · [📖 Docs ↗](https://metorial.com/docs) · [🌐 Site ↗](https://metorial.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/metorial/)</sub>

<a name="gptcache"></a>
### #&#8288;64 [gptcache](https://github.com/zilliztech/gptcache) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (73) · Freshness: recent (70) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · MIT · Sep 2026</sub>

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

<a name="paritok-4b-v1"></a>
### #&#8288;65 [paritok-4b-v1](https://github.com/paritok-official/paritok-4b-v1) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · Apache-2.0 · Nov 2026</sub>

**Compression proxy that shrinks coding-agent prompts before they reach the LLM API.**

Paritok is a proxy between a coding agent (Claude Code, Cursor, Codex, OpenHands) and the Anthropic or OpenAI-compatible API. It filters tool schemas with a local embedding model, compresses tool results and file reads with a fine-tuned Qwen3-4B model, and summarizes old history. Compressed segments are tagged [REF:id] and the agent can fetch the originals with read_original. Savings figures come from the project's own tests.

- **+** Works by setting ANTHROPIC_BASE_URL or OPENAI_BASE_URL; no agent code changes
- **+** Compressed content stays recoverable through read_original, so nothing is permanently dropped
- **+** Tool-schema filter runs locally on CPU with bge-small (~130MB); README reports ~29K to ~8K tokens
- **+** Self-hosted via Ollama (~2.5GB q4) or vLLM LoRA serving; hosted GPU option exists
- **−** Savings figures come from the authors' own tests, with long-session numbers partly projected
- **−** Content compression gives only a few percent on a single turn
- **−** Needs Ollama or a vLLM server (24GB GPU) running alongside the proxy
- **−** First request waits ~10-15s while the embedding model downloads

<sub>GPU optional · Needs Ollama, vLLM (alternative), sentence-transformers (toolselect extra), Anthropic or OpenAI-compatible upstream API · Models: Anthropic API, OpenAI-compatible APIs (Groq, OpenRouter), Qwen3-4B LoRA (paritok-4b-v1) · port 8080 · [Repo](https://github.com/paritok-official/paritok-4b-v1) · [🌐 Site ↗](https://paritok.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paritok-4b-v1/)</sub>

<a name="orcareplay"></a>
### #&#8288;66 [orcareplay](https://github.com/continuum-ai-corp/orcareplay) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Oct 2026</sub>

**Record coding-agent runs and replay or fork them offline onto other models.**

OrcaReplay puts a local proxy in front of an unmodified coding agent (Claude Code, Codex, Agents SDK, AI SDK) and writes the run to a trace file. `orca replay` serves the run back byte-for-byte with egress blocked, and `orca compare` forks it from a checkpoint onto several models, graded by a command you choose. It also captures shell exit codes, file changes and a causal graph, and exports an HTML timeline.

- **+** Replays a recorded run with no network and no tokens, with egress blocked
- **+** Forks from a checkpoint onto other models and grades each with your own verify command
- **+** Captures shell exit codes and file writes, not only model API calls
- **+** Needs no agent changes: a local proxy and two environment variables
- **−** Replay still runs recorded tool calls for real; it is not a sandbox
- **−** Model comparison needs a gateway or provider keys; OrcaRouter is the default
- **−** PNG and GIF card export needs playwright-core, pngjs and gifenc installed separately
- **−** No tagged release; trace spec is v0

<sub>no GPU · Docker · Needs Node.js 20+, Provider API keys or an OpenAI-compatible gateway (for fork and compare) · Models: Anthropic, OpenAI, OpenAI-compatible gateways (OrcaRouter default) · [Repo](https://github.com/continuum-ai-corp/orcareplay) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/orcareplay/)</sub>

<a name="portkey-gateway"></a>
### #&#8288;67 [Portkey Gateway](https://github.com/portkey-ai/gateway) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: widely used (82) · Freshness: recent (64) · Maintenance: weak (2) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · May 2026</sub>

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

<a name="livebench"></a>
### #&#8288;68 [livebench](https://github.com/livebench/livebench) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · custom license · Oct 2026</sub>

**Contamination-limited LLM benchmark with monthly questions and automatic scoring.**

LiveBench is a Python benchmark harness that runs LLMs through 18 tasks in 6 categories (reasoning, math, coding, language, data analysis, instruction following). Questions are refreshed monthly and have objective ground-truth answers, so scoring needs no LLM judge. It evaluates any OpenAI-compatible endpoint, plus Anthropic, Cohere, Mistral, Together and Google, and prints per-category and per-task results.

- **+** Ground-truth answers are scored automatically, with no LLM judge
- **+** Works with any OpenAI-compatible endpoint via --api-base, plus several native providers
- **+** Questions and model answers are published as Hugging Face datasets
- **+** Custom questions and scoring functions can be added through question.jsonl
- **−** Latest release's questions are not all public; older release 2024-11-25 is needed
- **−** Agentic coding tasks need Docker and up to 150GB of images
- **−** Local model inference is unmaintained; vLLM server is recommended instead
- **−** Parallel mode requires tmux

<sub>no GPU · Needs Python, Docker (agentic coding tasks), tmux (parallel mode), vLLM (optional, for local models) · Models: OpenAI-compatible APIs, Anthropic, Cohere, Mistral, Together · [Repo](https://github.com/livebench/livebench) · [🌐 Site ↗](https://livebench.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/livebench/)</sub>

<a name="openclaw-bot-review"></a>
### #&#8288;69 [openclaw-bot-review](https://github.com/xmanrui/openclaw-bot-review) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (22) · Freshness: active (89) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · MIT · Jul 2026</sub>

**Web dashboard for monitoring OpenClaw agents, models, sessions and token usage.**

A Next.js dashboard that reads ~/.openclaw/openclaw.json and local session files to show OpenClaw agents, their models, platform bindings (Feishu, Discord), sessions and gateway health. It adds token and response-time charts, connectivity tests, Feishu alert rules, and an animated pixel-art office where agents appear as characters. No database is used.

- **+** No database; derives everything from the OpenClaw config and local session files
- **+** Per-model, per-session and per-platform connectivity tests from the UI
- **+** Token and response-time charts with daily, weekly and monthly views
- **+** Operator write APIs require a token by default
- **−** Only works with OpenClaw; needs its config at ~/.openclaw/openclaw.json or OPENCLAW_HOME
- **−** Alert notifications are delivered only through Feishu
- **−** Built-in model metadata lists only MiniMax models
- **−** Docker run needs the OpenClaw directory mounted to read real config

<sub>no GPU · Docker · Needs OpenClaw, Node.js 18+ · Models: MiniMax-M2.7, MiniMax-M2.7-highspeed, OpenAI-compatible providers via OpenClaw config · port 3000 · [Repo](https://github.com/xmanrui/openclaw-bot-review) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openclaw-bot-review/)</sub>

<a name="evals"></a>
### #&#8288;70 [evals](https://github.com/openai/evals) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: widely used (88) · Freshness: recent (50) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Apr 2026</sub>

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

<a name="agentops"></a>
### #&#8288;71 [agentops](https://github.com/agentops-ai/agentops) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (62) · Freshness: recent (61) · Maintenance: weak (4) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Jun 2026</sub>

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

<sub>no GPU · Needs AgentOps API key (hosted dashboard) · Models: OpenAI, Anthropic, Mistral, Cohere, LiteLLM · [Repo](https://github.com/agentops-ai/agentops) · [🌐 Site ↗](https://agentops.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentops/)</sub>

<a name="terminal-bench-1"></a>
### #&#8288;72 [terminal-bench-1](https://github.com/harbor-framework/terminal-bench-1) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (29) · Freshness: active (82) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · Apache-2.0 · Jul 2026</sub>

**Benchmark of about 100 terminal tasks with a harness for testing LLM agents.**

Terminal-Bench is a dataset of command-line tasks plus an execution harness that connects a language model to a sandboxed terminal. Each task has an English instruction, a test script and a reference solution. The `tb` CLI, installed from pip, runs agents such as `terminus` against terminal-bench-core v0.1.1, which matches the leaderboard. The README points new users to harbor for Terminal-Bench 2.0.

- **+** Each task ships an instruction, a test script and an oracle solution
- **+** Installs as a pip package and runs through the `tb run` CLI
- **+** Versioned dataset (core 0.1.1) tied to a public leaderboard
- **+** Runs tasks in a Docker sandbox with configurable concurrency (--n-concurrent)
- **−** README marks it beta with roughly 100 tasks
- **−** New users are directed to harbor for Terminal-Bench 2.0
- **−** Requires Docker and uv installed on the host
- **−** README example uses a hosted model API; local model setup is not described

<sub>no GPU · Docker + Compose · Needs Docker, uv · Models: anthropic/claude-3-7-latest (README example) · [Repo](https://github.com/harbor-framework/terminal-bench-1) · [📖 Docs ↗](https://www.tbench.ai/docs) · [🌐 Site ↗](https://www.tbench.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/terminal-bench-1/)</sub>

<a name="coai"></a>
### #&#8288;73 [CoAI](https://github.com/coaidev/coai) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: popular (75) · Freshness: slowing (38) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · Mar 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs MySQL, Redis, SearXNG (optional web search), CoAI blob-service (optional file parsing) · Models: OpenAI, Azure OpenAI, Anthropic, Gemini, Midjourney, SparkDesk, Zhipu, Qwen, Hunyuan, Baichuan, Moonshot, DeepSeek, Skylark, Groq, OpenRouter, 360, LocalAI, Ollama · port 8000 · [Repo](https://github.com/coaidev/coai) · [🌐 Site ↗](https://coai.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/coai/)</sub>

<a name="pezzo"></a>
### #&#8288;74 [Pezzo](https://github.com/pezzolabs/pezzo) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: known (38) · Freshness: recent (70) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Nov 2026</sub>

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

<sub>no GPU · Compose · Needs PostgreSQL, ClickHouse, Redis, SuperTokens, Node.js 18+ · port 4200 · [Repo](https://github.com/pezzolabs/pezzo) · [📖 Docs ↗](https://docs.pezzo.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pezzo/)</sub>

<a name="simple-evals"></a>
### #&#8288;75 [simple-evals](https://github.com/openai/simple-evals) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: popular (53) · Freshness: recent (53) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · MIT · Apr 2026</sub>

**Reference implementations of zero-shot LLM benchmarks such as MMLU, GPQA and SimpleQA.**

A small Python library from OpenAI that runs language-model evals (MMLU, MATH, GPQA, DROP, MGSM, HumanEval, SimpleQA, BrowseComp, HealthBench) with zero-shot chain-of-thought prompts. Samplers exist for the OpenAI and Anthropic APIs, driven by a CLI. Since July 2025 it is no longer updated for new models and only keeps the HealthBench, BrowseComp and SimpleQA reference implementations.

- **+** Covers nine benchmarks behind one CLI: --model and --examples flags
- **+** Zero-shot chain-of-thought prompts with simple instructions, documented in the README
- **+** Official reference code for SimpleQA, BrowseComp and HealthBench
- **+** Published results table gives baseline numbers for many OpenAI and third-party models
- **−** Deprecated: no updates for new models or benchmark results after July 2025
- **−** Maintainers do not monitor issues or PRs, and no new evals are accepted
- **−** No unified setup; each eval and sampler needs its own pip install
- **−** Samplers only for OpenAI and Claude APIs; no local model backend

<sub>no GPU · Needs openai, anthropic, human-eval · Models: OpenAI API, Anthropic Claude API · [Repo](https://github.com/openai/simple-evals) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/simple-evals/)</sub>

<a name="one-hub"></a>
### #&#8288;76 [one-hub](https://github.com/martialbe/one-hub) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: known (33) · Freshness: slowing (37) · Maintenance: weak (19) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Feb 2026</sub>

**OpenAI-compatible gateway for routing, pricing and billing across LLM providers.**

One Hub is a Go fork of one-api that proxies requests to providers such as OpenAI, Azure OpenAI, Anthropic, Gemini, Bedrock, Ollama and several Chinese vendors. It adds per-user quotas, per-call or ratio-based pricing, group RPM limits, payments, a user dashboard and an admin analytics view. It also accepts Gemini and Claude format requests and exports Prometheus metrics.

- **+** Covers about 24 providers, including Azure, Anthropic, Gemini, Bedrock, Ollama, Midjourney and Suno
- **+** Per-channel http/socks5 proxy, model wildcards, per-call pricing and automatic price updates
- **+** Prometheus metrics, Uptime Kuma checks, monthly bills and Telegram bot support
- **+** Accepts Gemini and Claude format API requests as well as OpenAI format
- **−** Database is incompatible with upstream one-api, so it cannot be mixed or swapped in place
- **−** Maintainer states no stability guarantee and no technical support
- **−** Bundled model list is no longer refreshed; new models need a manual price update
- **−** README and main docs are in Chinese; the English README is a separate file

<sub>no GPU · Docker + Compose · Compose runs Redis, MySQL · Models: OpenAI, Azure OpenAI, Anthropic, Gemini, Amazon Bedrock · [Repo](https://github.com/martialbe/one-hub) · [▶️ Demo ↗](https://one-hub.xiao5.info/) · [📖 Docs ↗](https://one-hub-doc.vercel.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/one-hub/)</sub>

<a name="openclaw-control-center"></a>
### #&#8288;77 [openclaw-control-center](https://github.com/tianyidatascience/openclaw-control-center) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: known (47) · Freshness: slowing (50) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · MIT · Apr 2026</sub>

**Local dashboard for monitoring and coordinating an existing OpenClaw agent setup.**

A TypeScript web UI that reads an existing OpenClaw installation and shows health, usage and spend, staff activity, tasks, approvals, documents and agent memory. A Collaboration page lets agents discuss, assign, hand off and review work in one shared thread, dispatched through the real `openclaw agent` runtime. It starts read-only with local token auth and mutation routes disabled.

- **+** Safe defaults: read-only mode, local token auth, mutation and approval actions disabled
- **+** Uses the live OpenClaw roster from openclaw.json; no agent renaming needed
- **+** Usage page covers spend, subscription windows, and per-session context pressure
- **+** Dockerfile and compose example included, plus build, test and smoke scripts
- **−** Works only with OpenClaw; not a dashboard for other agent stacks
- **−** Requires a running OpenClaw Gateway and read access to its home directory
- **−** No tagged releases; installed from a git clone with npm
- **−** Docker needs OpenClaw data paths mounted and Gateway URL wired by hand

<sub>no GPU · Docker + Compose · Needs OpenClaw, OpenClaw Gateway, Node.js, npm · port 4310 · [Repo](https://github.com/tianyidatascience/openclaw-control-center) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openclaw-control-center/)</sub>

<a name="skill"></a>
### #&#8288;78 [skill](https://github.com/pinchbench/skill) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: niche (13) · Freshness: recent (73) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · May 2026</sub>

**Benchmark suite that scores LLMs as the model behind an OpenClaw agent.**

PinchBench runs 53 real-world tasks (calendar scheduling, email triage, research, coding, spreadsheet and PDF analysis, memory) against a model driving an OpenClaw agent. Tasks are graded automatically, by an LLM judge, or both. Results can be uploaded to the public leaderboard at pinchbench.com or kept local with --no-upload.

- **+** Tasks check outcomes such as a created file or scheduled event, not just text answers
- **+** Judge can be an OpenClaw session or a direct API call (OpenRouter, Anthropic, OpenAI, Kilo, Claude CLI)
- **+** CLI supports per-task suites, repeated runs for averaging, timeout scaling and thinking levels
- **+** Full agent transcripts are saved per task as JSONL for post-run analysis
- **−** Requires a running OpenClaw instance, so results only reflect that agent harness
- **−** Does not produce the official leaderboard results; those come from a separate scripts repo
- **−** LLM-judge grading adds API cost and may vary between judge models
- **−** Only 53 tasks, and the README does not describe how scores are aggregated

<sub>Docker · Needs OpenClaw, uv, Python 3.10+, OpenRouter API key (default provider) · Models: OpenRouter, Anthropic, OpenAI, Kilo Gateway · [Repo](https://github.com/pinchbench/skill) · [🌐 Site ↗](https://pinchbench.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skill/)</sub>

<a name="intellagent"></a>
### #&#8288;79 [intellagent](https://github.com/plurai-ai/intellagent) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: niche (7) · Freshness: recent (70) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · Apache-2.0 · Sep 2026</sub>

**Simulates users to stress-test conversational agents with generated edge-case scenarios.**

IntellAgent decomposes an agent's system prompt into a policy graph, samples policies, and generates scenarios (including mock databases) for a simulated user agent to run against your chatbot. A critic step then scores each conversation per policy, and results can be viewed in a Streamlit dashboard. It calls hosted LLMs (OpenAI, Azure, Vertex, Anthropic) and is configured through YAML files.

- **+** Generates scenarios from the agent's own prompt, with optional tools and database schema
- **+** Per-policy critique of each simulated conversation, with a Streamlit results dashboard
- **+** Simulator and chatbot LLM providers are set separately in YAML config
- **+** cost_limit setting; README estimates about $0.10 per sample at default parameters
- **−** Only LangGraph integration is done; CrewAI and AutoGen are unfinished roadmap items
- **−** API integration for external conversational agents is still on the roadmap
- **−** Prompt, tool and graph optimization is limited to premium access
- **−** Install is git clone plus requirements.txt; last release was January 2025

<sub>no GPU · Needs Python >= 3.9, LLM API key (OpenAI, Azure, Vertex or Anthropic), Streamlit · Models: OpenAI, Azure OpenAI, Vertex, Anthropic · [Repo](https://github.com/plurai-ai/intellagent) · [📖 Docs ↗](https://intellagent-doc.plurai.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/intellagent/)</sub>

<a name="prompttools"></a>
### #&#8288;80 [prompttools](https://github.com/hegelai/prompttools) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: known (35) · Freshness: quiet (19) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · Apache-2.0 · Feb 2026</sub>

**Python library for testing prompts, LLMs and vector databases in notebooks.**

prompttools runs prompt and parameter grids across LLM APIs such as OpenAI, Anthropic, Mistral, Gemini and LLaMA.cpp, then shows results side by side in a notebook or a local Streamlit playground. It also tests retrieval against vector databases like Chroma, Weaviate, Qdrant, LanceDB and Pinecone. Results export to CSV, JSON or MongoDB.

- **+** Covers many providers: OpenAI, Anthropic, Mistral, Gemini, Vertex AI, Azure, Replicate, LLaMA.cpp, HuggingFace
- **+** Also tests vector database retrieval (Chroma, Weaviate, Qdrant, LanceDB, Pinecone)
- **+** Runs locally; LLM calls go straight from your machine, with no forwarding server
- **+** Exports results via to_csv, to_json, to_lora_json and to_mongo_db
- **−** Last release was 2024-01-02, so newer provider APIs may be missing
- **−** Ollama support is in progress; Milvus and LlamaIndex are only exploratory
- **−** Sends usage and error data to Sentry unless SENTRY_OPT_OUT is set
- **−** Hosted playground does not support LlamaCpp

<sub>GPU optional · Needs Jupyter notebook, Streamlit, LLM provider API keys · Models: OpenAI, Anthropic, Mistral AI, Google Gemini, Vertex AI · [Repo](https://github.com/hegelai/prompttools) · [▶️ Demo ↗](https://prompttools.streamlit.app/) · [📖 Docs ↗](http://prompttools.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/prompttools/)</sub>

<a name="deepchecks"></a>
### #&#8288;81 [deepchecks](https://github.com/deepchecks/deepchecks) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: known (48) · Freshness: quiet (0) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · custom license · Nov 2025</sub>

**Python checks for validating tabular, NLP and vision data and models.**

Deepchecks is a Python package of built-in Checks and Suites that test data integrity, drift, leakage and model performance for tabular, NLP and computer vision projects. Results can be saved as HTML, shown in Jupyter, read as JSON or Python values, and gated with pass/fail conditions in CI. A separate repo, deepchecks/monitoring, reuses the same checks for production models.

- **+** Built-in checks for drift, leakage, conflicting labels and weak segments across three data types
- **+** Checks take configurable parameters and conditions, and custom checks can be written
- **+** Results export to HTML, Jupyter, JSON or Python values for CI gating
- **+** Installs with pip or conda, with optional nlp and vision extras
- **−** AGPL 3.0 licensing may block use in some commercial products
- **−** Managed CI and testing management is a closed preview, not open source
- **−** Self-hosted open-source monitoring supports only one model per deployment
- **−** Monitoring repo has a commercial-licensed ee directory; last release was Dec 2024

<sub>Needs Docker (self-hosted monitoring only) · Models: Tabular, NLP, Computer vision · [Repo](https://github.com/deepchecks/deepchecks) · [📖 Docs ↗](https://docs.deepchecks.com/) · [🌐 Site ↗](https://deepchecks.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepchecks/)</sub>

<a name="langtrace"></a>
### #&#8288;82 [langtrace](https://github.com/scale3-labs/langtrace) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: niche (5) · Freshness: quiet (0) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · AGPL-3.0 · Nov 2025</sub>

**OpenTelemetry-based tracing for LLM apps, with Python and TypeScript SDKs.**

Langtrace captures OpenTelemetry-compatible traces and metrics from applications that call LLM APIs, vector databases and LLM frameworks. Python and TypeScript SDKs instrument providers such as OpenAI, Anthropic and Bedrock, and the web app shows latency, cost and usage. Self-hosting runs a Next.js app with Postgres and ClickHouse via Docker Compose, and a managed cloud is also offered.

- **+** Instruments many LLM providers, frameworks and vector DBs through two SDKs
- **+** Traces follow OpenTelemetry standards
- **+** Self-hosted version sends no telemetry; data stays on your servers
- **+** SDKs are Apache 2.0, separate from the AGPL server
- **−** Self-hosting needs three services: Next.js, Postgres and ClickHouse
- **−** TypeScript SDK lacks Langchain, LangGraph, LiteLLM, CrewAI, Ollama and Mistral
- **−** Server is AGPL-3.0, which may constrain modified hosted deployments
- **−** Last release was April 2025, months behind the latest commit

<sub>no GPU · Docker + Compose · Needs Docker, Docker Compose, Postgres, ClickHouse · Models: OpenAI, Anthropic, Azure OpenAI, Cohere, DeepSeek · port 3000 · [Repo](https://github.com/scale3-labs/langtrace) · [📖 Docs ↗](https://docs.langtrace.ai/hosting/overview) · [🌐 Site ↗](https://www.langtrace.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langtrace/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
