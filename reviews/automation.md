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
### 🥈 [Activepieces](https://github.com/activepieces/activepieces) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Nov 2026</sub>

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
### 🥉 [youtube-automation-agent](https://github.com/darkzogx/youtube-automation-agent) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · MIT · Oct 2026</sub>

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

<sub>no GPU · Needs Node.js 18.17+, YouTube Data API v3 credentials, Playwright Chromium, ffmpeg-static, text provider API key · Models: Gemini, OpenAI, OpenRouter, Kimi, MiMo · port 3456 · [Repo](https://github.com/darkzogx/youtube-automation-agent) · [📖 Docs ↗](https://github.com/darkzOGx/youtube-automation-agent/blob/main/docs/features.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/youtube-automation-agent/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
