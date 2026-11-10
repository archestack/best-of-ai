# 🔁 Workflow automation with AI reviews · Best of Open-Source AI

Workflow and integration platforms with AI steps or agent nodes, for wiring models into the rest of your tools. Back to the [leaderboard](../README.md#-workflow-automation-with-ai).

<sub>🌐 Also on the web: [Workflow automation with AI on archestack.com](https://archestack.com/best-of-ai/automation/), each project on its own page.</sub>

<a name="n8n"></a>
### 🥇 [n8n](https://github.com/n8n-io/n8n) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 210k · custom license · Nov 2026</sub>

**Visual workflow automation with AI agent nodes and 1500+ integrations.**

n8n is a node-based canvas for building workflows and multi-step AI agents, with JavaScript, Python and npm packages usable inside nodes. It connects to OpenAI, Anthropic, Google and open-source models, and lists 1500+ integrations and 9,000+ workflow templates. It runs self-hosted or on n8n Cloud, under the Sustainable Use License rather than an OSI license.

- **+** 1500+ integrations and 9,000+ templates cover most common SaaS wiring
- **+** Visual canvas with JavaScript, Python and npm code when needed
- **+** Model-agnostic: OpenAI, Anthropic, Google or open-source models
- **+** Supports human approvals and observability for multi-step AI workflows
- **−** Fair-code Sustainable Use License, not OSI open source; use is restricted
- **−** Role-based access and audit trails fall under the Enterprise License
- **−** Documented quick start requires Docker

<sub>no GPU · Needs Docker · Models: OpenAI, Anthropic, Google, open-source models · port 5678 · [Repo](https://github.com/n8n-io/n8n) · [📖 Docs ↗](https://docs.n8n.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/n8n/)</sub>

<a name="activepieces"></a>
### 🥈 [Activepieces](https://github.com/activepieces/activepieces) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Nov 2026</sub>

**Self-hosted workflow automation with TypeScript integrations, alternative to Zapier.**

Activepieces is a no-code workflow builder with loops, branches, auto retries, HTTP calls and npm-backed code steps, and flows are versioned. Integrations are called pieces: TypeScript npm packages, 280+ of which are exposed as MCP servers for Claude Desktop, Cursor or Windsurf. It also has AI pieces for several providers, human-in-the-loop approvals, and chat and form triggers.

- **+** Pieces are open-source TypeScript npm packages with hot reloading for local development
- **+** 280+ pieces usable as MCP servers from Claude Desktop, Cursor or Windsurf
- **+** Flows are versioned and support loops, branches and auto retries
- **+** Built-in approval, delay, chat and form triggers for human-in-the-loop flows
- **−** Enterprise features sit under a separate commercial license, not MIT
- **−** Automation-first; AI agents are one feature rather than the core design
- **−** README claims of 200+ and 280+ pieces are inconsistent

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL, Redis · Models: OpenAI · [Repo](https://github.com/activepieces/activepieces) · [📖 Docs ↗](https://www.activepieces.com/docs) · [🌐 Site ↗](https://activepieces.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/activepieces/)</sub>

<a name="trendradar"></a>
### 🥉 [trendradar](https://github.com/sansan0/trendradar) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · GPL-3.0 · Nov 2026</sub>

**Aggregates trending news and RSS, filters it, pushes digests to chat apps.**

TrendRadar pulls hot-list data from Chinese platforms (via the newsnow API) and RSS feeds. It filters items by keywords or AI-scored interest descriptions, then pushes digests to WeChat Work, Telegram, DingTalk, Feishu, email, ntfy, Bark, Slack or a webhook. AI analysis and translation go through LiteLLM, and a separate MCP server exposes the data to AI clients.

- **+** Nine push channels, with long messages split to each channel's byte limit
- **+** LiteLLM integration supports 100+ providers, with retries and fallback models
- **+** Timeline scheduling with presets, plus a browser-based visual config editor
- **+** Separate MCP server lets AI clients search news and read articles
- **−** Hot-list data depends on the third-party newsnow API unless self-hosted
- **−** Main README and docs are in Chinese; English README is separate
- **−** GPL-3.0 license restricts reuse in closed-source derivatives
- **−** Platform sources are oriented toward Chinese-language sites

<sub>no GPU · Docker + Compose · Needs newsnow API, LLM API via LiteLLM (optional) · Models: LiteLLM providers (OpenAI, Anthropic, Gemini, DeepSeek) · [Repo](https://github.com/sansan0/trendradar) · [▶️ Demo ↗](https://sansan0.github.io/TrendRadar) · [📖 Docs ↗](https://trendradar.sandev.cc/zh/docs/quick-start/) · [🌐 Site ↗](https://trendradar.sandev.cc/zh/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trendradar/)</sub>

<a name="sellbird"></a>
### #&#8288;4 [sellbird](https://github.com/ethanplusai/sellbird) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · AGPL-3.0 · Nov 2026</sub>

**Cold outreach pipeline that finds prospects, verifies emails, drafts and sends.**

Sellbird finds businesses matching your customer profile (OpenStreetMap or a paid source), reads their websites for buying signals, finds the decision maker and verifies one email address. It then drafts a short sequence, sends from Gmail, Microsoft 365 or SMTP, and drafts replies. Model calls go through the Claude Code CLI or Codex CLI on a subscription instead of an API key. Sends wait in an Outbox for approval unless autopilot is enabled.

- **+** Uses Claude Pro/Max or ChatGPT plan via CLI; no API key or per-token billing
- **+** Default approval gate plus a no-model pre-send check for merge tags, links and bad addresses
- **+** Can stop after verification and export a CSV for another sequencer
- **+** Signal detection reads company sites with plain HTTP requests, no model calls
- **−** Needs your own mailbox and warmup; README recommends a separate sending domain
- **−** Depends on a signed-in Claude Code or Codex CLI; subscription limits apply
- **−** AGPL-3.0 since 0.4.0; earlier Harvey releases were MIT
- **−** Docker is documented for Linux only; macOS needs Python 3.11+ installed

<sub>no GPU · Docker + Compose · Needs Claude Code CLI or Codex CLI, Gmail, Microsoft 365 or SMTP mailbox, Python 3.11+, SQLite database file · Models: Claude (via Claude Code CLI), ChatGPT plans (via Codex CLI) · port 5555 · [Repo](https://github.com/ethanplusai/sellbird) · [🌐 Site ↗](https://sellbird.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sellbird/)</sub>

<a name="clearcam"></a>
### #&#8288;5 [clearcam](https://github.com/roryclear/clearcam) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · GPL-3.0 · Nov 2026</sub>

**Self-hosted NVR adding object detection and phone alerts to RTSP cameras.**

Clearcam is a Python network video recorder that runs object detection and tracking on RTSP camera streams, records events, and serves a web UI on port 8080. Alerts can go to its iOS and Android apps or to a custom URL, such as Home Assistant, Pushover or n8n. Notification summaries use Qwen3 VL. Remote viewing and push alerts through its own service need a paid premium account.

- **+** Notification URL is configurable, so alerts can go to Home Assistant, Pushover or n8n
- **+** Web UI on localhost:8080 for live view, events and recording playback
- **+** Runs from source with pip install and one command; AMD and NVIDIA selectable via DEV
- **+** Sample Pushover notification server included in utils/sample_server.py
- **−** Windows is not supported; the README says an ffmpeg fix is needed
- **−** Remote streams and app push notifications require a paid premium account
- **−** No Docker image or compose file in the repository
- **−** Requires Python 3.11 or later and ffmpeg installed on the host

<sub>GPU optional · Needs ffmpeg, python3.11+ · Models: Qwen3 VL · port 8080 · [Repo](https://github.com/roryclear/clearcam) · [🌐 Site ↗](https://www.clearcam.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clearcam/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
