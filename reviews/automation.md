# 🔁 Workflow automation with AI reviews · Best of Open-Source AI

Workflow and integration platforms with AI steps or agent nodes, for wiring models into the rest of your tools. Back to the [leaderboard](../README.md#-workflow-automation-with-ai).

<sub>🌐 Also on the web: [Workflow automation with AI on archestack.com](https://archestack.com/best-of-ai/automation/), each project on its own page.</sub>

<a name="n8n"></a>
### 🥇 [n8n](https://github.com/n8n-io/n8n) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 212k · custom license · Nov 2026</sub>

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
### 🥈 [Activepieces](https://github.com/activepieces/activepieces) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · custom license · Nov 2026</sub>

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

<a name="youtube-automation-agent"></a>
### 🥉 [youtube-automation-agent](https://github.com/darkzogx/youtube-automation-agent) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · MIT · Nov 2026</sub>

**Agent that researches, produces and schedules YouTube videos after your approval.**

Node.js app that runs a YouTube channel pipeline on your own machine: topic research, scripts, narration, images, MP4 assembly, metadata, and scheduled uploads through the YouTube Data API. Every video waits for fact review, media-rights confirmation, and your approval before publishing. A dashboard on port 3456 covers review, scene repair, and analytics-based lessons that apply only after you approve them.

- **+** Nothing uploads without approval; simulated or placeholder media cannot be approved
- **+** Eight text providers or OpenRouter, five AI video providers, plus free local slideshow rendering
- **+** Each generation stage is checkpointed, so a crash resumes instead of restarting
- **+** Built-in schedule for generation, publishing, analytics, comment sync and weekly review
- **−** Requires Google Cloud OAuth setup; Testing-mode sign-in expires every 7 days
- **−** No Docker or compose files; setup is git clone, npm install and Playwright Chromium
- **−** Narration and images need API keys; AI video clips are paid
- **−** Built around a single operator and channel; multi-user support is not described

<sub>no GPU · Needs Node.js 18.17+, YouTube Data API v3 credentials, Playwright Chromium, ffmpeg-static, text provider API key · Models: Gemini, OpenAI, OpenRouter, Kimi, MiMo · port 3456 · [Repo](https://github.com/darkzogx/youtube-automation-agent) · [📖 Docs ↗](https://github.com/darkzOGx/youtube-automation-agent/blob/HEAD/docs/features.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/youtube-automation-agent/)</sub>

<a name="openoutreach"></a>
### #&#8288;4 [openoutreach](https://github.com/eracle/openoutreach) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · GPL-3.0 · Nov 2026</sub>

**CLI that finds B2B leads from a product description and emails them.**

OpenOutreach is a Python CLI that takes a product description and target market, discovers matching people through BetterContact's Lead Finder, and has an LLM qualify each one with a written reason. It then buys verified work emails for the leads that pass a confidence gate and sends openers from your own SMTP/IMAP mailbox. It orchestrates two separate packages, OpenOutFind and OpenOutSend, and can also export leads as CSV.

- **+** No list upload needed; input is a product description and target market
- **+** Each lead exports with a written reason for the fit verdict
- **+** CSV columns match Instantly and Smartlead importers without mapping
- **+** Discovery is free; credits are spent only on verified work emails
- **−** Depends on BetterContact, a paid third-party data provider, for discovery and emails
- **−** Learning loop is stated to be not yet shown to beat random picking
- **−** Needs an LLM API key and a mailbox app password before first run
- **−** README says Apache 2.0 while detected license is GPL-3.0

<sub>no GPU · Needs BetterContact API key, SMTP/IMAP mailbox with app password, uv · Models: OpenAI, Anthropic, OpenAI-compatible endpoints · [Repo](https://github.com/eracle/openoutreach) · [🌐 Site ↗](https://openoutreach.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openoutreach/)</sub>

<a name="flyto-core"></a>
### #&#8288;5 [flyto-core](https://github.com/flytohub/flyto-core) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 483 · Apache-2.0 · Nov 2026</sub>

**Python engine that runs YAML workflows of browser, API and file steps.**

flyto-core is the Python execution engine behind Flyto2. It ships 482 registered modules and 41 built-in recipes covering browser automation, APIs, files and data, and can be driven from Python, YAML workflows, a local HTTP API or an MCP server. Each run keeps a per-step record, with checkpoints and replay where safe.

- **+** Per-step run records, with checkpoints and replay where safe
- **+** Usable from Python, YAML, local HTTP API or MCP
- **+** 482 modules and 41 built-in recipes ready to run
- **+** Checks reported tool evidence against the action's contract
- **−** ROS 2 robot support still lacks full end-to-end hardware sign-off
- **−** Physical device actions need a trusted host to approve them
- **−** Browser recipes need Playwright and a Chromium install
- **−** README gives no LLM or model integration details

<sub>no GPU · Docker · Needs Python, Playwright, Chromium · [Repo](https://github.com/flytohub/flyto-core) · [📖 Docs ↗](https://docs.flyto2.com) · [🌐 Site ↗](https://flyto2.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flyto-core/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
