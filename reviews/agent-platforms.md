# 🧩 Agent platforms reviews · Best of Self-Hosted AI

Visual or code-first builders for agents and workflows, with orchestration, tools and deployment. Back to the [leaderboard](../README.md#-agent-platforms).

<a name="n8n"></a>
### 🥇 [n8n](https://github.com/n8n-io/n8n) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 207k · custom license · Oct 2026</sub>

**Visual workflow automation with code steps, AI agent nodes and 1500+ integrations.**

n8n is a fair-code workflow platform that runs as one Docker container (docker.n8n.io/n8nio/n8n, port 5678) and combines a visual canvas with JavaScript, Python and npm code nodes. AI agent and workflow nodes connect to OpenAI, Anthropic, Google or open-source models, with human-approval steps and observability, and 1500+ integrations plus 9,000+ templates cover the rest of the stack.

- **+** 1500+ integrations and 9,000+ ready-made workflow templates
- **+** Code nodes run JavaScript or Python and can pull npm packages
- **+** Single container on port 5678 with one data volume
- **+** Switch model providers without rebuilding the workflow
- **−** Sustainable Use License (fair-code, source-available), not an OSI license
- **−** Some features require a separate n8n Enterprise License
- **−** README states no database, RAM or CPU requirements

<sub>no GPU · Models: OpenAI, Anthropic, Google, open-source models · port 5678 · [Repo](https://github.com/n8n-io/n8n) · [📖 Docs ↗](https://docs.n8n.io)</sub>

<a name="dify"></a>
### 🥈 [Dify](https://github.com/langgenius/dify) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 158k · custom license · Oct 2026</sub>

**Visual LLM app platform with workflows, RAG pipeline, agents and APIs.**

Dify is an LLM app platform started with Docker Compose (dashboard on port 80) that needs 2 CPU cores and 4 GiB RAM. One canvas covers visual workflows, a prompt IDE, a RAG pipeline that ingests PDFs and PPTs, sandboxed agents using Marketplace tools, MCP servers or your own APIs, plus LLMOps tracing via Opik, Langfuse or Arize Phoenix. Hundreds of models work, including OpenAI-compatible endpoints.

- **+** Workflow, RAG, agents, prompt IDE and model management in one canvas
- **+** Hundreds of models: GPT, Mistral, Llama3 and any OpenAI-compatible API
- **+** Observability through Opik, Langfuse and Arize Phoenix
- **+** Every feature is exposed through an API (backend-as-a-service)
- **−** Dify Open Source License adds conditions on top of Apache 2.0
- **−** SSO, RBAC and support SLAs are reserved for Dify Enterprise
- **−** Minimum 2 CPU cores and 4 GiB RAM for the Compose stack
- **−** Dashboard binds to port 80 by default

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Models: OpenAI GPT, Mistral, Llama 3, OpenAI-compatible APIs, dozens of inference providers · port 80 · [Repo](https://github.com/langgenius/dify) · [▶️ Demo ↗](https://cloud.dify.ai) · [📖 Docs ↗](https://docs.dify.ai) · [🌐 Site ↗](https://dify.ai)</sub>

<a name="langflow"></a>
### 🥉 [Langflow](https://github.com/langflow-ai/langflow) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 155k · MIT · Oct 2026</sub>

**Visual flow builder that deploys agents as APIs or MCP servers.**

Langflow is a Python 3.10 to 3.14 visual builder (uv pip install langflow, or the langflowai/langflow Docker image on port 7860) for agents and LLM workflows. Every component is editable Python, flows run in an interactive playground, and a finished flow can be served as an API, exported as JSON for Python apps or exposed as an MCP server. Multi-agent orchestration and LangSmith or LangFuse tracing are built in.

- **+** Any flow becomes an API endpoint or an MCP server for MCP clients
- **+** Component source is Python you can edit inside the builder
- **+** One container on port 7860; no other service in the quick start
- **+** MIT license; desktop builds for Windows and macOS
- **−** README names no model providers, vector stores or resource needs
- **−** No root Dockerfile or compose file; container config lives in the docs
- **−** Enterprise-ready claim is not detailed in the README

<sub>no GPU · Docker + Compose · port 7860 · [Repo](https://github.com/langflow-ai/langflow) · [📖 Docs ↗](https://docs.langflow.org/get-started-installation) · [🌐 Site ↗](https://langflow.org)</sub>

<a name="sim"></a>
### #&#8288;4 [Sim](https://github.com/simstudioai/sim) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

**Workspace to build, deploy and monitor agents with 1,000+ integrations.**

Sim is a Next.js and Bun app on PostgreSQL that builds agents visually, by chat or in code, with monitoring, schedules and logs. The npx sim-setup wizard (Node.js 20+ and Docker) provisions the database, secrets and images and serves port 3000. Tables, files and knowledge bases share the workspace, 1,000+ integrations such as Slack, Notion and HubSpot are available, and local models run via Ollama or vLLM.

- **+** Built-in tables, file store and knowledge bases alongside workflows and chat
- **+** 1,000+ integrations including Slack, Notion, HubSpot, Salesforce and databases
- **+** Local models via Ollama and vLLM; Apache-2.0 license
- **+** sim-setup wizard adds email, storage, sandbox, jobs, cache or knowledge later
- **−** Chat is a Sim-managed service; self-hosted installs need a Chat API key from sim.ai
- **−** Setup prompt in the README notes the Compose stack needs 12 GB+ RAM
- **−** Background jobs use Trigger.dev and remote code execution uses E2B
- **−** Self-hosting goes through an npx wizard rather than a documented compose file

<sub>RAM ≥ 12 GB · no GPU · Docker + Compose · Needs PostgreSQL, Docker, Sim Chat API key · Models: Ollama, vLLM · port 3000 · [Repo](https://github.com/simstudioai/sim) · [📖 Docs ↗](https://docs.sim.ai) · [🌐 Site ↗](https://sim.ai)</sub>

<a name="autogpt"></a>
### #&#8288;5 [AutoGPT](https://github.com/significant-gravitas/autogpt) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: fair (79) · Easy to run: hard (17) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 187k · custom license · Oct 2026</sub>

**Block-based builder for agents that run on demand, schedule or trigger.**

AutoGPT Platform lets you describe a job in plain English (AutoPilot) or wire blocks on a visual canvas, then run the agent on demand, on a schedule or from a trigger, with a dashboard of runs and costs and a marketplace of shared agents. It connects to 45+ platforms such as Gmail, Slack, GitHub and Notion. Self-hosting is free with your own Docker host and model API keys; the hosted platform is paid.

- **+** Plain-English AutoPilot and a drag-and-connect block builder for the same agent
- **+** Agents run on demand, on schedules or from triggers with a run and cost dashboard
- **+** 45+ integrations including Gmail, Google Sheets, GitHub, Slack, Notion, Jira, Salesforce
- **+** Classic standalone agent still shipped under MIT in classic/
- **−** Platform code is Polyform Shield: no offering it as a competing hosted service
- **−** README has no self-host commands; the single-container installer is still unreleased
- **−** Windows self-hosting is manual-guide only
- **−** Hosted platform charges per agent run; README is largely marketing

<sub>no GPU · Needs Docker · [Repo](https://github.com/significant-gravitas/autogpt) · [▶️ Demo ↗](https://platform.agpt.co/tour) · [📖 Docs ↗](https://docs.agpt.co)</sub>

<a name="multica"></a>
### #&#8288;6 [Multica](https://github.com/multica-ai/multica) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 52k · custom license · Oct 2026</sub>

**Issue board where AI coding agents take assignments like teammates.**

Multica is a workspace where issues are assigned to AI coding agents, which run through locally installed agent CLIs such as Claude Code, Codex, Cursor and Copilot (26 listed). A daemon on your own machine executes the work next to your code and reports progress back to the issue, which ends in review rather than main. The backend is Go with PostgreSQL 17, and clients cover web, Electron desktop and an Expo mobile app.

- **+** Drives 26 existing agent CLIs, so no model or API lock-in
- **+** Execution log replays every tool call, command and error per run
- **+** Daemon runs on your own machine, so code stays there
- **+** Self-host via Docker Compose or Helm; works with GitHub, GitLab, Gitea, Forgejo
- **−** Does not ship agents; each runtime needs a CLI installed and signed in
- **−** Custom Multica License (Apache 2.0 plus conditions on hosting, embedding, branding)
- **−** Requires Docker, a Go backend and PostgreSQL 17 to self-host
- **−** iOS app builds from source only; DingTalk, WeCom, Telegram are community-maintained

<sub>no GPU · Docker + Compose · Needs PostgreSQL 17, Docker, agent CLI (Claude Code, Codex, etc.) · Models: Claude Code, OpenAI Codex, Cursor Agent, GitHub Copilot CLI, OpenCode · [Repo](https://github.com/multica-ai/multica) · [📖 Docs ↗](https://multica.ai/docs) · [🌐 Site ↗](https://multica.ai)</sub>

<a name="activepieces"></a>
### #&#8288;7 [Activepieces](https://github.com/activepieces/activepieces) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Oct 2026</sub>

**Self-hosted workflow automation with TypeScript integrations, alternative to Zapier.**

Activepieces is a no-code workflow builder with loops, branches, auto retries, HTTP calls and npm-backed code steps, and flows are versioned. Integrations are called pieces: TypeScript npm packages, 280+ of which are exposed as MCP servers for Claude Desktop, Cursor or Windsurf. It also has AI pieces for several providers, human-in-the-loop approvals, and chat and form triggers.

- **+** Pieces are open-source TypeScript npm packages with hot reloading for local development
- **+** 280+ pieces usable as MCP servers from Claude Desktop, Cursor or Windsurf
- **+** Flows are versioned and support loops, branches and auto retries
- **+** Built-in approval, delay, chat and form triggers for human-in-the-loop flows
- **−** Enterprise features sit under a separate commercial license, not MIT
- **−** README does not state RAM, CPU or database requirements
- **−** Automation-first; AI agents are one feature rather than the core design
- **−** README claims of 200+ and 280+ pieces are inconsistent

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL, Redis · Models: OpenAI · [Repo](https://github.com/activepieces/activepieces) · [📖 Docs ↗](https://www.activepieces.com/docs) · [🌐 Site ↗](https://activepieces.com)</sub>

<a name="paperclip"></a>
### #&#8288;8 [Paperclip](https://github.com/paperclipai/paperclip) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (75) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 99k · MIT · Oct 2026</sub>

**Task manager and org chart for teams of AI agents with budgets.**

Paperclip is a Node.js server and React UI that coordinates external agents (OpenClaw, Claude Code, Codex, Cursor, Gemini CLI and custom HTTP adapters) through tasks, approvals, org charts, budgets and routines. Agents wake on heartbeats, check out tasks atomically, and report work and spend to a dashboard; multi-org support, skills, GitHub, Notion and MCP connectors, and company export/import are built in.

- **+** Company, agent and project budgets with alerts and automatic pause at limits
- **+** Atomic task checkout with execution locks prevents duplicate runs
- **+** Adapters for OpenClaw, Claude Code, Codex, Cursor, Gemini CLI, OpenCode, Hermes, Kimi
- **+** Export and import whole organizations with secret scrubbing
- **−** Does no agent work itself; needs external agent runtimes installed and authenticated
- **−** Agent Chat and Slack, Discord, Telegram, AgentMail connectors are experimental
- **−** Paperclip Cloud is waitlist-only
- **−** Quickstart, ports and database are beyond the README's first 20,000 characters

<sub>no GPU · Docker + Compose · [Repo](https://github.com/paperclipai/paperclip) · [📖 Docs ↗](https://docs.paperclip.ing) · [🌐 Site ↗](https://paperclip.ing)</sub>

<a name="skyvern"></a>
### #&#8288;9 [Skyvern](https://github.com/skyvern-ai/skyvern) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (80) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · AGPL-3.0 · Oct 2026</sub>

**Browser automation agent driven by vision LLMs over Playwright.**

Skyvern drives websites with vision LLMs instead of selectors: a Playwright-compatible Python/TypeScript SDK adds page.act, page.extract and page.validate, and a no-code builder chains tasks into workflows with loops, HTTP and code blocks. pip install skyvern[all] serves API and UI on port 8080 with SQLite by default; Docker Compose bundles Postgres. TOTP 2FA, Bitwarden, browser livestreaming and MCP are supported.

- **+** Works on sites it has never seen; no XPath or CSS selectors to maintain
- **+** SQLite default means the pip path needs neither Postgres nor Docker
- **+** TOTP, email and SMS 2FA plus Bitwarden and custom credential services
- **+** Python and TypeScript SDKs extend standard Playwright calls with a prompt argument
- **−** AGPL-3.0 license
- **−** Anti-bot measures, proxy network and CAPTCHA solving exist only in the paid cloud
- **−** Windows pip install needs Rust plus VS C++ tools and the Windows SDK
- **−** Authentication features are offered by email request; 1Password and LastPass unsupported

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL · port 8080 · [Repo](https://github.com/skyvern-ai/skyvern) · [▶️ Demo ↗](https://app.skyvern.com) · [📖 Docs ↗](https://www.skyvern.com/docs/) · [🌐 Site ↗](https://www.skyvern.com)</sub>

<a name="agent-zero"></a>
### #&#8288;10 [Agent Zero](https://github.com/agent0ai/agent-zero) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · custom license · Sep 2026</sub>

**Agent framework that gives the model a full Linux desktop in Docker.**

Agent Zero runs as the agent0ai/agent-zero Docker image (port 80) and gives the agent an XFCE desktop, a browser with DOM annotation, LibreOffice and a shell in the container, all visible in a Canvas the user can take over. Projects isolate memory, secrets and repos, subagents split work, a Plugin Hub lists 100+ plugins, MCP and A2A are supported, and an A0 CLI connector bridges it to repos on the host.

- **+** Full XFCE desktop and browser in the container; you can intervene with mouse and keyboard
- **+** Time Travel snapshots with diff inspection and revert for the agent workspace
- **+** 100+ community plugins installable from the Web UI
- **+** Runs on a $6 VPS or Raspberry Pi; A0 CLI connects host repositories
- **−** Container listens on port 80 by default
- **−** README warns to keep it isolated and never mount your home directory
- **−** License is not stated in the README
- **−** Maintainers point to Space Agent as the more polished product direction

<sub>no GPU · Docker + Compose · Needs Docker · Models: OpenAI Codex plan (OAuth) · port 80 · [Repo](https://github.com/agent0ai/agent-zero) · [🌐 Site ↗](https://agent-zero.ai)</sub>

<a name="fastgpt"></a>
### #&#8288;11 [FastGPT](https://github.com/labring/fastgpt) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

**Knowledge-base Q&A and visual workflow platform for LLM apps.**

FastGPT builds agents and LLM apps from a visual Flow editor on top of a knowledge base that ingests TXT, MD, HTML, PDF, Docx, PPTX, CSV, XLSX and URLs with hybrid retrieval and reranking. A one-script Docker Compose install serves port 3000 (default login root / 1234), supports bidirectional MCP, chat and plugin workflows, evaluation, call-chain logs, login-free share pages and iframe embedding.

- **+** Loaders for TXT, MD, HTML, PDF, Docx, PPTX, CSV, XLSX and URLs
- **+** Hybrid retrieval with reranking; chunks can be edited and deleted
- **+** Bidirectional MCP and RPA-style workflow nodes
- **+** One-script Docker Compose install
- **−** FastGPT Open Source License forbids offering it as SaaS and requires kept copyright notices
- **−** Default credentials root / 1234 after install
- **−** Default README is Chinese; English lives in README_en.md
- **−** Debug mode, node logs and auto-generated workflows are still unchecked roadmap items

<sub>no GPU · Compose · port 3000 · [Repo](https://github.com/labring/fastgpt) · [📖 Docs ↗](https://doc.fastgpt.io/guide/getting-started) · [🌐 Site ↗](https://fastgpt.io)</sub>

<a name="botpress"></a>
### #&#8288;12 [Botpress](https://github.com/botpress/botpress) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (22) · Freshness: recent (70) · Maintenance: patchy (40) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

**SDK, CLI and open-source integrations for the Botpress Cloud bot platform.**

This repository holds the TypeScript devtools for Botpress Cloud: the @botpress/cli (bp init, bp deploy), the @botpress/sdk and typed client, every public integration on the Botpress Hub, and example bots written as code. Bots themselves are built in the hosted Botpress Studio and powered by OpenAI; the on-premise server is the separate Botpress v12 repository. Everything here is MIT.

- **+** All public Hub integrations are open source and contributable with bp init and bp deploy
- **+** Typed TypeScript SDK and API client for building integrations and bots as code
- **+** MIT license for every package in the repository
- **−** The chatbot platform (Studio, runtime) is Botpress Cloud, not something you host from here
- **−** Self-hosted server is the separate, older Botpress v12 repository
- **−** Bots-as-code is described as not the recommended way to build bots
- **−** Plugins section is marked coming soon

<sub>no GPU · Docker · Models: OpenAI · [Repo](https://github.com/botpress/botpress) · [▶️ Demo ↗](https://app.botpress.cloud) · [📖 Docs ↗](https://botpress.com/docs) · [🌐 Site ↗](https://botpress.com)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
