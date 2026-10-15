# 🧩 Agent platforms reviews · Best of Open-Source AI

Visual or code-first builders for agents and workflows, with orchestration, tools and deployment. Back to the [leaderboard](../README.md#-agent-platforms).

<sub>🌐 Also on the web: [Agent platforms on archestack.com](https://archestack.com/best-of-ai/agent-platforms/), each project on its own page.</sub>

<a name="langflow"></a>
### 🥇 [Langflow](https://github.com/langflow-ai/langflow) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 156k · MIT · Oct 2026</sub>

**Visual builder for AI agents and workflows, exposed as API or MCP server.**

Langflow is a Python platform for assembling agents and workflows on a visual canvas, with Python source access to customize any component. Each flow can be served as an HTTP API, exported as JSON, or deployed as an MCP server so MCP clients can call it as a tool. It installs via uv/pip, Docker, or a Windows and macOS desktop app, and serves its UI on port 7860.

- **+** Every flow can be called as a REST API or exposed as an MCP server
- **+** Component source is editable in Python, so custom nodes need no fork
- **+** Built-in playground for step-by-step testing of flows
- **+** Observability integrations with LangSmith and LangFuse; MIT license
- **−** Official releases require setting LANGFLOW_SUPERUSER_PASSWORD; dev branches default to auto-login
- **−** Python 3.10–3.14 required for the pip install path
- **−** README gives no RAM or hardware requirements
- **−** Specific supported models and vector databases are not listed in the README

<sub>Docker + Compose · Needs Python 3.10–3.14, uv · Models: major LLM providers, vector databases · port 7860 · [Repo](https://github.com/langflow-ai/langflow) · [📖 Docs ↗](https://docs.langflow.org) · [🌐 Site ↗](https://langflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langflow/)</sub>

<a name="daily-stock-analysis"></a>
### 🥈 [daily_stock_analysis](https://github.com/zhulinsen/daily_stock_analysis) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 66k · MIT · Oct 2026</sub>

**Daily LLM stock analysis for A-share, HK, US and other markets, pushed to chat apps.**

Python app that pulls quotes, K-lines, news and fundamentals for a watchlist across A-share, HK, US, Japan, Korea and Taiwan markets. It has an LLM write a decision report with score, trend, buy/sell levels and risks, then pushes it to WeCom, Feishu, Telegram, Discord, Slack or email. It runs on GitHub Actions, Docker or locally, with a FastAPI web workbench for history, backtests and strategy chat.

- **+** Runs on a GitHub Actions fork with no server; default schedule is weekdays 18:00 Beijing time
- **+** Free data sources (AkShare, Baostock, YFinance) work with zero configuration
- **+** Supports Gemini, Claude, OpenAI-compatible APIs, DeepSeek, Qwen and local Ollama models
- **+** Six push channels plus a web UI with history, backtest, portfolio and 15 built-in chat strategies
- **−** README is mainly Chinese; English docs are in a separate file
- **−** Free data sources are subject to rate limits and upstream changes; stability not guaranteed
- **−** Report quality depends on a paid news-search API key; a search service is recommended
- **−** Output is for study only; the disclaimer excludes investment advice and liability

<sub>no GPU · Docker + Compose · Needs LLM API key or Ollama, News search API (Anspire, SerpAPI, Tavily, Bocha, Brave, MiniMax or SearXNG), Market data sources (AkShare, Baostock, YFinance; optional TickFlow, Tushare, Longbridge), Notification channel · Models: Gemini, OpenAI-compatible, DeepSeek, Qwen, Claude · port 8000 · [Repo](https://github.com/zhulinsen/daily_stock_analysis) · [📖 Docs ↗](https://github.com/ZhuLinsen/daily_stock_analysis/blob/main/docs/INDEX.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/daily-stock-analysis/)</sub>

<a name="deer-flow"></a>
### 🥉 [deer-flow](https://github.com/bytedance/deer-flow) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · MIT · Oct 2026</sub>

**Agent harness that runs sub-agents, memory and sandboxed skills for long tasks.**

DeerFlow 2.0 is a ByteDance agent harness where a lead agent delegates to sub-agents, backed by long-term memory, a sandboxed file system and extensible skills. It includes a web UI, a Gateway, MCP support, IM channels, scheduled tasks, a terminal UI and an embedded Python client. It is a ground-up rewrite that shares no code with v1.

- **+** Interactive `make setup` wizard generates config.yaml and .env in about 2 minutes
- **+** Web UI model registration for OpenAI, Anthropic, DeepSeek, Qwen, Doubao, Kimi, Zhipu, MiniMax
- **+** Tracing via LangSmith, Langfuse and Monocle, plus `make doctor` and `make support-bundle`
- **+** Many search and fetch backends: Brave, Tavily, Jina, Firecrawl, Crawl4AI, InfoQuest
- **−** README warns improper deployment carries security risks; Gateway admin equals code execution
- **−** Local development needs Python 3.12+ and Node.js 22+
- **−** README is dense with config detail; RAM and hardware needs are not stated
- **−** v2 shares no code with v1; v1 users must stay on the 1.x branch

<sub>no GPU · Docker + Compose · Needs LLM provider API key, Python 3.12+, Node.js 22+ · Models: OpenAI, Anthropic, DeepSeek, Qwen, Doubao · [Repo](https://github.com/bytedance/deer-flow) · [🌐 Site ↗](https://deerflow.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deer-flow/)</sub>

<a name="dify"></a>
### #&#8288;4 [Dify](https://github.com/langgenius/dify) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 158k · custom license · Oct 2026</sub>

**Visual builder for LLM workflows, RAG pipelines and agents, with APIs.**

Dify is an LLM app development platform with a visual workflow canvas, a prompt IDE, a RAG pipeline that extracts text from PDFs and PPTs, and agents that run in their own sandbox. Every app is exposed through an API. Model providers include GPT, Mistral, Llama3 and any OpenAI-compatible endpoint. It runs via Docker Compose or as the hosted Dify Cloud.

- **+** Visual workflow canvas, prompt IDE and RAG pipeline in one platform
- **+** Every app exposes an API, so it works as a backend service
- **+** Supports hundreds of LLMs plus any OpenAI API-compatible model
- **+** Agents can use Marketplace tools, MCP servers or your own APIs
- **−** License is the Dify Open Source License (Apache 2.0 plus extra conditions)
- **−** SSO, RBAC and support SLAs are in the Enterprise edition
- **−** Docker Compose self-hosting needs at least 2 CPU cores and 4 GiB RAM
- **−** Observability relies on external tools such as Opik, Langfuse and Arize Phoenix

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Needs Docker, Docker Compose v2.24.0+ · Models: GPT, Mistral, Llama3, OpenAI API-compatible models · port 80 · [Repo](https://github.com/langgenius/dify) · [▶️ Demo ↗](https://cloud.dify.ai) · [📖 Docs ↗](https://docs.dify.ai) · [🌐 Site ↗](https://dify.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dify/)</sub>

<a name="multica"></a>
### #&#8288;5 [Multica](https://github.com/multica-ai/multica) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · custom license · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs PostgreSQL 17, Docker, agent CLI (Claude Code, Codex, etc.) · Models: Claude Code, OpenAI Codex, Cursor Agent, GitHub Copilot CLI, OpenCode · [Repo](https://github.com/multica-ai/multica) · [📖 Docs ↗](https://multica.ai/docs) · [🌐 Site ↗](https://multica.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/multica/)</sub>

<a name="autogpt"></a>
### #&#8288;6 [AutoGPT](https://github.com/significant-gravitas/autogpt) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: hard (17) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 188k · custom license · Oct 2026</sub>

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

<sub>no GPU · Needs Docker · [Repo](https://github.com/significant-gravitas/autogpt) · [▶️ Demo ↗](https://platform.agpt.co/tour) · [📖 Docs ↗](https://docs.agpt.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autogpt/)</sub>

<a name="vibe-trading"></a>
### #&#8288;7 [vibe-trading](https://github.com/hkuds/vibe-trading) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (99) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Oct 2026</sub>

**Finance research agent for backtests, market data and broker connectors.**

Vibe-Trading is a Python agent (FastAPI backend, React 19 web UI, CLI, MCP) for trading research. It pulls market data across many exchanges, runs backtests and factor analysis, and checks figures in generated reports against tool evidence. It also connects to 18 brokers and sends scheduled reports through channels such as Email, Slack, Discord and Feishu.

- **+** Grounding gate checks each reported figure against session tool evidence and cuts failures
- **+** Backtest run cards cite metrics only where saved CSV output agrees
- **+** 18 broker connectors, several read-only, with paper/live permissions documented
- **+** Active: v0.1.16 shipped 116 merged PRs, with near-daily fixes afterward
- **−** Narrow domain: finance research only, not a general agent builder
- **−** Some broker features are unavailable, e.g. Robinhood options execution
- **−** Data quality depends on public sources such as Stooq, which can block requests
- **−** Frequent backtest-correctness fixes in the changelog; verify results independently

<sub>no GPU · Docker + Compose · Needs LLM provider (OpenRouter is the default), Market data sources, Broker APIs (optional) · Models: OpenRouter, Codex, Copilot, custom model endpoints · [Repo](https://github.com/hkuds/vibe-trading) · [📖 Docs ↗](https://vibetrading.wiki/docs/) · [🌐 Site ↗](https://vibetrading.wiki/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vibe-trading/)</sub>

<a name="paperclip"></a>
### #&#8288;8 [Paperclip](https://github.com/paperclipai/paperclip) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (75) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 102k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · [Repo](https://github.com/paperclipai/paperclip) · [📖 Docs ↗](https://docs.paperclip.ing) · [🌐 Site ↗](https://paperclip.ing) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paperclip/)</sub>

<a name="openmaic"></a>
### #&#8288;9 [openmaic](https://github.com/thu-maic/openmaic) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (90) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Oct 2026</sub>

**Generates interactive classes with AI teachers and classmates from a topic or file.**

OpenMAIC turns a topic or attached documents into a lesson made of slides, quizzes, interactive HTML simulations and project-based learning activities. AI teacher and classmate agents speak via TTS, draw on a whiteboard and discuss with the learner. Built on Next.js 16, React 19 and LangGraph. Since 1.2.0, course generation runs on the server and courses are stored in PostgreSQL.

- **+** Exports lessons as editable .pptx or interactive .html pages
- **+** Many providers: OpenAI, Anthropic, Bedrock, Gemini, Ollama, Lemonade, any OpenAI-compatible API
- **+** Models set once per slot in openmaic.yml, with lock and allowUserKeys: false options
- **+** OpenMAIC Skill lets OpenClaw and similar workbenches generate classrooms from chat apps
- **−** 1.2.0 needs PostgreSQL 16 and a long-running server; Vercel and serverless are unsupported
- **−** Latest 1.2.0 line is a release candidate; changelog must be read before upgrading
- **−** README recommends image, video, TTS and web search keys for full function
- **−** Compose install is single-user; shared access needs ACCESS_CODE and manual network publishing

<sub>GPU optional · Docker + Compose · Needs PostgreSQL 16, Node.js >= 22.19, pnpm >= 10, LLM provider API key · Models: OpenAI, Anthropic, Amazon Bedrock, Google Gemini, DeepSeek · port 3000 · [Repo](https://github.com/thu-maic/openmaic) · [▶️ Demo ↗](https://open.maic.chat/) · [📖 Docs ↗](https://lcn6dqn3m0yr.feishu.cn/wiki/CkQSwHFdzibQFvkGzwPcmUOfnXg) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmaic/)</sub>

<a name="sim"></a>
### #&#8288;10 [Sim](https://github.com/simstudioai/sim) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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

<sub>RAM ≥ 12 GB · no GPU · Docker + Compose · Needs PostgreSQL, Docker, Sim Chat API key · Models: Ollama, vLLM · port 3000 · [Repo](https://github.com/simstudioai/sim) · [📖 Docs ↗](https://docs.sim.ai) · [🌐 Site ↗](https://sim.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sim/)</sub>

<a name="skyvern"></a>
### #&#8288;11 [Skyvern](https://github.com/skyvern-ai/skyvern) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · AGPL-3.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL · port 8080 · [Repo](https://github.com/skyvern-ai/skyvern) · [▶️ Demo ↗](https://app.skyvern.com) · [📖 Docs ↗](https://www.skyvern.com/docs/) · [🌐 Site ↗](https://www.skyvern.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skyvern/)</sub>

<a name="openmontage"></a>
### #&#8288;12 [openmontage](https://github.com/calesthio/openmontage) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: patchy (42) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · AGPL-3.0 · Oct 2026</sub>

**Agent-driven video production pipelines run from your AI coding assistant.**

OpenMontage is a set of pipelines, tools and stage skills that let a coding assistant (Claude Code, Cursor, Copilot, Windsurf, Codex) research, script, generate assets, edit and render a video. Rendering uses Remotion or HyperFrames plus FFmpeg. It works with no API keys using Piper TTS and free footage from Archive.org, NASA and Wikimedia, and adds paid image, video and voice providers when keys are set.

- **+** Works with zero API keys: Piper TTS, free archival footage, Remotion/HyperFrames, FFmpeg
- **+** Many providers via optional keys: fal.ai, Atlas Cloud, Kling, Runway, ElevenLabs, Suno, Google
- **+** Backlot local board shows pipeline progress, costs, and a storyboard approval gate before render
- **+** Can start from a reference YouTube, TikTok or local video and give cost estimates first
- **−** Needs an external AI coding assistant to drive it; no standalone prompting UI
- **−** AGPL-3.0 license restricts closed-source network use
- **−** Setup needs Python 3.10+, Node.js 18+ and FFmpeg; no Docker image
- **−** Local video generation needs a GPU; VRAM requirements are not stated in the README

<sub>GPU optional · Needs Python 3.10+, FFmpeg, Node.js 18+, AI coding assistant, Remotion, HyperFrames · Models: wan2.2-ti2v-5b, wan2.1, hunyuan-1.5, ltx2-local, cogvideo-5b · [Repo](https://github.com/calesthio/openmontage) · [🌐 Site ↗](https://openmontage.video) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmontage/)</sub>

<a name="agent-zero"></a>
### #&#8288;13 [Agent Zero](https://github.com/agent0ai/agent-zero) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · custom license · Oct 2026</sub>

**Agent framework with a Linux desktop, browser and document editing.**

Agent Zero runs an agent inside a Docker container with an XFCE desktop, a built-in browser with DOM annotation, and LibreOffice editing, all shown in a web UI Canvas. It adds projects with isolated memory and secrets, subordinate agents, a Plugin Hub, MCP and A2A support, and an A0 CLI connector for working on host files.

- **+** Real XFCE desktop in the container; agent drives GUI apps and you share the mouse
- **+** Projects isolate files, memory, secrets, repositories and model presets per workspace
- **+** Prompts and tools are editable files; MCP, A2A and a 100+ plugin catalog supported
- **+** Time Travel snapshots and diffs the /a0/usr workspace so edits can be reverted
- **−** Requires Docker; default run maps port 80, which often needs remapping
- **−** Agent has shell and desktop access; README warns to isolate it and limit mounts
- **−** License is reported as NOASSERTION, so terms need checking before use
- **−** RAM and VRAM requirements are not stated in the README

<sub>GPU optional · Docker + Compose · Needs Docker, LLM provider · Models: OpenAI Codex plan via OAuth, Local models, API LLM providers · port 80 · [Repo](https://github.com/agent0ai/agent-zero) · [📖 Docs ↗](https://www.agent-zero.ai/p/docs/a0-cli-connector/) · [🌐 Site ↗](https://agent-zero.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-zero/)</sub>

<a name="fastgpt"></a>
### #&#8288;14 [FastGPT](https://github.com/labring/fastgpt) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (95) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

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

<sub>no GPU · Compose · port 3000 · [Repo](https://github.com/labring/fastgpt) · [📖 Docs ↗](https://doc.fastgpt.io/guide/getting-started) · [🌐 Site ↗](https://fastgpt.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fastgpt/)</sub>

<a name="mirofish"></a>
### #&#8288;15 [mirofish](https://github.com/666ghj/mirofish) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (78) · Freshness: active (96) · Maintenance: fair (58) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 79k · AGPL-3.0 · Oct 2026</sub>

**Multi-agent social simulation engine that predicts outcomes from seed documents.**

MiroFish builds a GraphRAG knowledge graph from uploaded seed material such as news, policy drafts or novels, then generates agent personas and runs a parallel social simulation on the OASIS engine. A ReportAgent writes a prediction report, and you can chat with individual simulated agents afterward. It uses any OpenAI-format LLM API plus Zep Cloud for memory.

- **+** End-to-end pipeline: graph building, persona generation, simulation, report, and agent chat
- **+** Works with any OpenAI-SDK-compatible LLM endpoint via LLM_BASE_URL
- **+** Public live demo available without installing anything
- **+** Docker Compose and source install both documented, ports 3000 and 5001
- **−** Requires Zep Cloud API key, so memory is not fully self-hosted
- **−** README warns of high LLM token consumption; suggests under 40 rounds first
- **−** AGPL-3.0 license restricts closed-source network use
- **−** README gives no evidence of prediction accuracy or benchmarks

<sub>no GPU · Docker + Compose · Needs Zep Cloud, OpenAI-compatible LLM API, Node.js 18+, Python 3.11-3.12, uv · Models: OpenAI-compatible APIs, Qwen-plus (recommended) · port 3000 · [Repo](https://github.com/666ghj/mirofish) · [▶️ Demo ↗](https://666ghj.github.io/mirofish-demo/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mirofish/)</sub>

<a name="ui-tars-desktop"></a>
### #&#8288;16 [ui-tars-desktop](https://github.com/bytedance/ui-tars-desktop) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: known (48) · Freshness: active (100) · Maintenance: patchy (39) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Oct 2026</sub>

**Multimodal agent stack: terminal/Web UI agent and a desktop GUI agent.**

Monorepo with two projects. Agent TARS is a CLI and Web UI agent that controls a browser via GUI vision, DOM, or a hybrid, and mounts MCP servers as tools. UI-TARS Desktop is an app that operates the local or a remote computer and browser through the UI-TARS and Seed-1.5-VL/1.6 vision-language models.

- **+** Browser control by GUI vision, DOM, or hybrid strategy
- **+** MCP kernel; external MCP servers can be mounted as tools
- **+** Agent TARS runs headful (Web UI) or headless as a server
- **+** Works with providers such as Volcengine and Anthropic via CLI flags
- **−** Two products in one repo; README splits setup across external docs
- **−** Desktop app targets Windows and macOS; Linux support not stated
- **−** RAM and GPU needs for local UI-TARS models are not stated
- **−** Agent TARS CLI requires Node.js 22 or newer

<sub>Needs Node.js >= 22, model provider API key · Models: UI-TARS-1.5, Seed-1.5-VL, Volcengine Doubao, Anthropic Claude · [Repo](https://github.com/bytedance/ui-tars-desktop) · [📖 Docs ↗](https://agent-tars.com/guide/get-started/introduction.html) · [🌐 Site ↗](https://agent-tars.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ui-tars-desktop/)</sub>

<a name="botpress"></a>
### #&#8288;17 [Botpress](https://github.com/botpress/botpress) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (12) · Freshness: recent (70) · Maintenance: patchy (39) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

**SDK, CLI and open-source integrations for the Botpress Cloud bot platform.**

This repository holds the TypeScript devtools for Botpress Cloud: the @botpress/cli (bp init, bp deploy), the @botpress/sdk and typed client, every public integration on the Botpress Hub, and example bots written as code. Bots themselves are built in the hosted Botpress Studio and powered by OpenAI; the on-premise server is the separate Botpress v12 repository. Everything here is MIT.

- **+** All public Hub integrations are open source and contributable with bp init and bp deploy
- **+** Typed TypeScript SDK and API client for building integrations and bots as code
- **+** MIT license for every package in the repository
- **−** The chatbot platform (Studio, runtime) is Botpress Cloud, not something you host from here
- **−** Self-hosted server is the separate, older Botpress v12 repository
- **−** Bots-as-code is described as not the recommended way to build bots
- **−** Plugins section is marked coming soon

<sub>no GPU · Docker · Models: OpenAI · [Repo](https://github.com/botpress/botpress) · [▶️ Demo ↗](https://app.botpress.cloud) · [📖 Docs ↗](https://botpress.com/docs) · [🌐 Site ↗](https://botpress.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/botpress/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
