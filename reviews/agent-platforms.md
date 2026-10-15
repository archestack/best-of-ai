# 🧩 Agent platforms reviews · Best of Open-Source AI

Visual or code-first builders for agents and workflows, with orchestration, tools and deployment. Back to the [leaderboard](../README.md#-agent-platforms).

<sub>🌐 Also on the web: [Agent platforms on archestack.com](https://archestack.com/best-of-ai/agent-platforms/), each project on its own page.</sub>

<a name="langflow"></a>
### 🥇 [Langflow](https://github.com/langflow-ai/langflow) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 156k · MIT · Oct 2026</sub>

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
### 🥈 [daily_stock_analysis](https://github.com/zhulinsen/daily_stock_analysis) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 66k · MIT · Oct 2026</sub>

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

<a name="mindshub"></a>
### 🥉 [mindshub](https://github.com/mindsdb/mindshub) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (69) · Freshness: active (100) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Sep 2026</sub>

**Agent workspace for knowledge work, with swappable open agent harnesses.**

Superproject that builds the MindsHub desktop (Electron) and web app, agent backend and data vault from git submodules. Agents handle research, reports, scheduled tasks and app or document artifacts, using the Anton (default) or Hermes harness and a model router across Claude, GPT, Gemini, DeepSeek, Qwen and Kimi. Also offered as a hosted web app and macOS/Windows installers.

- **+** Swappable open-source agent harnesses (Anton, Hermes) selectable from a dropdown
- **+** Connectors for BigQuery, Postgres, Gmail, Drive, HubSpot, Notion and Linear with per-connection credentials
- **+** Cross-session memory, skill library and scheduled tasks included
- **+** MIT license; deployable locally, in a VPC, on-prem or air-gapped
- **−** Linux has no installer; requires building from source with make and submodules
- **−** Pro tier needed for all frontier models and private artifacts
- **−** README gives no RAM, GPU or port requirements
- **−** Bundled submodules carry their own licenses

<sub>Compose · Needs make, uv, Python 3.10-3.13, Electron · Models: Claude, GPT, Gemini, DeepSeek, Qwen · [Repo](https://github.com/mindsdb/mindshub) · [▶️ Demo ↗](https://console.mindshub.ai/) · [📖 Docs ↗](https://docs.mindshub.ai/) · [🌐 Site ↗](https://mindshub.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mindshub/)</sub>

<a name="deer-flow"></a>
### #&#8288;4 [deer-flow](https://github.com/bytedance/deer-flow) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · MIT · Oct 2026</sub>

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
### #&#8288;5 [Dify](https://github.com/langgenius/dify) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 158k · custom license · Oct 2026</sub>

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
### #&#8288;6 [Multica](https://github.com/multica-ai/multica) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · custom license · Oct 2026</sub>

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

<a name="vibe-trading"></a>
### #&#8288;7 [vibe-trading](https://github.com/hkuds/vibe-trading) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (99) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Oct 2026</sub>

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

<a name="autogpt"></a>
### #&#8288;8 [AutoGPT](https://github.com/significant-gravitas/autogpt) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: hard (17) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 188k · custom license · Oct 2026</sub>

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

<a name="sim"></a>
### #&#8288;9 [Sim](https://github.com/simstudioai/sim) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

**Visual workspace for building and running AI agents and workflows.**

Sim is a Next.js and PostgreSQL workspace for building agents and workflows visually, conversationally or in code. It connects 270+ integrations (5,400+ actions, 520+ triggers) and major LLMs, with built-in tables, files and knowledge bases plus run logs and schedules. Self-hosting uses `npx sim-setup`, which starts published images with Docker Compose. Ollama and vLLM are supported for local models.

- **+** 270+ integrations with 5,400+ actions and 520+ triggers
- **+** Tables, files and knowledge bases live in the same workspace as workflows
- **+** Setup wizard with start, update, status, logs and doctor commands
- **+** Supports local models through Ollama and vLLM; Apache-2.0 licensed
- **−** Chat is a Sim-managed service and needs a Chat API key from sim.ai
- **−** Setup prompt in the README says the Docker stack needs 12GB+ RAM
- **−** Stack has many parts: Postgres, Socket.io, Trigger.dev and E2B
- **−** Desktop app is macOS only

<sub>RAM ≥ 12 GB · GPU optional · Docker + Compose · Needs Docker, Node.js 20+, PostgreSQL, Trigger.dev, E2B · Models: Ollama, vLLM, major hosted LLMs · port 3000 · [Repo](https://github.com/simstudioai/sim) · [📖 Docs ↗](https://docs.sim.ai) · [🌐 Site ↗](https://sim.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sim/)</sub>

<a name="paperclip"></a>
### #&#8288;10 [Paperclip](https://github.com/paperclipai/paperclip) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: fair (75) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 102k · MIT · Oct 2026</sub>

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
### #&#8288;11 [openmaic](https://github.com/thu-maic/openmaic) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (90) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Oct 2026</sub>

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

<a name="suna"></a>
### #&#8288;12 [suna](https://github.com/kortix-ai/suna) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (39) · Freshness: active (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Oct 2026</sub>

**Git-repo-based agent platform running each session in its own cloud sandbox.**

Kortix keeps agents, skills, memory, connectors and triggers as files in a git repo (kortix.yaml). Each session runs an OpenCode agent in an isolated sandbox on its own branch, and its work reaches main only through a change request a person approves. It is used from the web app, CLI, Slack and Microsoft Teams, with cron and webhook triggers. Self-hosting uses a Docker Compose stack started by the CLI.

- **+** Per-session sandbox on its own branch; merge to main needs human approval
- **+** Per-tool Allow/Ask/Block rules, audit trail, SAML SSO and SCIM
- **+** Any model provider with your own keys; config lives in git
- **+** Slack and Teams channels, cron and signed webhook triggers
- **−** License reported as NOASSERTION; terms need checking before commercial use
- **−** Self-host setup asks for integration credentials for managed git, GitHub and Pipedream
- **−** Self-host pulls images from Docker Hub, so it is not an offline install
- **−** Default provider isolates with containers; microVMs only on the Platinum provider

<sub>no GPU · Needs Docker, Docker Hub, Pipedream, GitHub · Models: Any provider with your own API keys, ChatGPT subscription · [Repo](https://github.com/kortix-ai/suna) · [📖 Docs ↗](https://kortix.com/docs) · [🌐 Site ↗](https://kortix.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/suna/)</sub>

<a name="skyvern"></a>
### #&#8288;13 [Skyvern](https://github.com/skyvern-ai/skyvern) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · AGPL-3.0 · Oct 2026</sub>

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

<a name="fastgpt"></a>
### #&#8288;14 [FastGPT](https://github.com/labring/fastgpt) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (95) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

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

<a name="resume-matcher"></a>
### #&#8288;15 [resume-matcher](https://github.com/srbhr/resume-matcher) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (51) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

**Tailors resumes and cover letters to job descriptions using local or hosted LLMs.**

Resume Matcher takes a master resume (PDF or DOCX) and a pasted job description, then generates a tailored resume, cover letter and optional interview prep. It scores the match, highlights keywords, and exports PDFs from 10 templates through headless Chromium. The backend is FastAPI with LiteLLM, the frontend is Next.js, and storage is SQLite by default with optional PostgreSQL.

- **+** Works with Ollama locally and with OpenAI, Anthropic, Gemini, OpenRouter, DeepSeek and Groq
- **+** SQLite by default, so no separate database is required
- **+** Tailoring queue processes several job descriptions in the background and resumes after restart
- **+** Multi-arch Docker images (amd64, arm64) serve app and API on port 3000
- **−** Manual setup needs Python 3.13+, Node.js 24+ and uv
- **−** Claude CLI and ChatGPT sign-in providers do not work in the default Docker setup
- **−** Subscription-based providers depend on unofficial third-party access and may stop working
- **−** RAM and GPU requirements are not stated

<sub>GPU optional · Docker + Compose · Needs Python 3.13+, Node.js 24+, uv, Playwright Chromium, SQLite or PostgreSQL · Models: Ollama, OpenAI, Anthropic, Google Gemini, OpenRouter · port 3000 · [Repo](https://github.com/srbhr/resume-matcher) · [📖 Docs ↗](https://resumematcher.fyi/docs/installation) · [🌐 Site ↗](https://resumematcher.fyi) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/resume-matcher/)</sub>

<a name="agent-zero"></a>
### #&#8288;16 [Agent Zero](https://github.com/agent0ai/agent-zero) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · custom license · Oct 2026</sub>

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

<a name="openmontage"></a>
### #&#8288;17 [openmontage](https://github.com/calesthio/openmontage) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: patchy (42) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · AGPL-3.0 · Oct 2026</sub>

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

<a name="trigger-dev"></a>
### #&#8288;18 [trigger.dev](https://github.com/triggerdotdev/trigger.dev) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (24) · Freshness: active (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Oct 2026</sub>

**TypeScript platform for durable background tasks and AI agent workflows.**

Trigger.dev is a TypeScript SDK and runtime for writing long-running background tasks in your own codebase and deploying them to a managed cloud or a self-hosted instance. Tasks run without timeouts and get retries, queues, checkpointing, waitpoints for human approval, realtime streaming to frontends, and per-run tracing. Build extensions let tasks use system packages such as Python, FFmpeg and browsers.

- **+** Tasks have no timeouts, with checkpointing and automatic retries for long AI jobs
- **+** Waitpoints pause a run until a human approves, rejects or gives feedback
- **+** Realtime API and React hooks stream run state and LLM output to the frontend
- **+** Self-hostable with Docker Compose or an official Helm chart for Kubernetes
- **−** Code-first and TypeScript/JavaScript only; no visual workflow builder
- **−** Managed cloud is the primary path; self-hosting needs extra setup and services
- **−** Not an agent framework; you bring your own LLM libraries and orchestration
- **−** Self-hosting resource requirements are not stated in the README

<sub>no GPU · [Repo](https://github.com/triggerdotdev/trigger.dev) · [📖 Docs ↗](https://trigger.dev/docs) · [🌐 Site ↗](https://trigger.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trigger-dev/)</sub>

<a name="mirofish"></a>
### #&#8288;19 [mirofish](https://github.com/666ghj/mirofish) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: widely used (87) · Freshness: active (96) · Maintenance: fair (58) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 79k · AGPL-3.0 · Oct 2026</sub>

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

<a name="openfang"></a>
### #&#8288;20 [openfang](https://github.com/rightnow-ai/openfang) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (32) · Freshness: active (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · May 2026</sub>

**Rust agent runtime with scheduled autonomous agents and 40 chat channel adapters.**

OpenFang is a Rust agent runtime that ships as a single ~32MB binary with a web dashboard on port 4200. It bundles seven preconfigured autonomous agents ("Hands") such as Researcher, Lead and Browser, which run on schedules and report through 40 messaging adapters. It routes to 27 LLM providers, exposes an OpenAI-compatible API, and runs tool code in a WASM sandbox.

- **+** Single binary with built-in dashboard, SQLite memory and vector embeddings
- **+** 40 channel adapters, including Telegram, Slack, Discord, WhatsApp, Signal and Matrix
- **+** 27 LLM providers including Ollama, vLLM and LM Studio, with fallback and cost tracking
- **+** WASM tool sandbox, approval gates and a Merkle hash-chain audit trail
- **−** Pre-1.0; README warns of breaking changes and advises pinning to a commit
- **−** README says MIT while repository license is Apache-2.0; version numbers also conflict
- **−** Benchmark comparisons are self-reported from public docs, not independently verified
- **−** WhatsApp QR gateway needs Node.js 18+ and a separate process

<sub>no GPU · Docker + Compose · Needs Node.js >= 18 (WhatsApp Web gateway only), FFmpeg and yt-dlp (Clip Hand), Playwright (Browser Hand) · Models: Anthropic, Gemini, OpenAI-compatible, Ollama, vLLM · port 4200 · [Repo](https://github.com/rightnow-ai/openfang) · [📖 Docs ↗](https://openfang.sh/docs) · [🌐 Site ↗](https://openfang.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openfang/)</sub>

<a name="rocketride-server"></a>
### #&#8288;21 [rocketride-server](https://github.com/rocketride-org/rocketride-server) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (30) · Freshness: active (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

**Visual AI pipeline builder in VS Code with a C++ runtime.**

RocketRide is a pipeline builder and runtime for AI workloads. Pipelines are saved as portable JSON .pipe files, built on a visual canvas in a VS Code extension, and run by a multithreaded C++ engine. It ships 100+ nodes covering 15+ LLM providers, 9 vector databases, OCR, NER and agents, with Python and TypeScript SDKs and an MCP server.

- **+** Pipelines are plain JSON .pipe files, diffable and version-controllable
- **+** 100+ nodes, including 15+ LLM providers and 9 vector databases; nodes are Python-extensible
- **+** Built-in tracing of token usage, LLM calls, latency and call trees
- **+** MIT license with no enterprise edition; Python and TypeScript SDKs plus MCP server
- **−** Visual builder is delivered as an IDE extension (VS Code or Open VSX editors)
- **−** SDK falls back to RocketRide Cloud when run outside the extension's folder
- **−** RAM and GPU requirements are not stated in the README
- **−** RAG example needs an LLM key and a vector database such as Qdrant

<sub>Needs VS Code or compatible IDE, Docker (optional), Vector database (for RAG), LLM API key (for hosted models) · Models: OpenAI, Anthropic, 15+ LLM providers, local models · port 5565 · [Repo](https://github.com/rocketride-org/rocketride-server) · [📖 Docs ↗](https://docs.rocketride.org/) · [🌐 Site ↗](https://rocketride.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rocketride-server/)</sub>

<a name="rd-agent"></a>
### #&#8288;22 [rd-agent](https://github.com/microsoft/rd-agent) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (18) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Sep 2026</sub>

**LLM agent that proposes and implements ML experiments for quant and data science.**

RD-Agent splits automated R&D into a research agent that proposes ideas and a development agent that implements and tests them. Scenarios include Qlib-based quant factor and model evolution, Kaggle and MLE-bench data science runs, paper-to-model extraction, and LLM fine-tuning. LLM access goes through LiteLLM, and it runs on Linux with Docker.

- **+** Reports MLE-bench results: 30.22% overall with o3 research and GPT-4.1 development agents
- **+** Ready-made CLI scenarios: fin_quant, fin_factor, fin_model, general_model, data_science
- **+** LiteLLM backend works with OpenAI, Azure OpenAI and DeepSeek, among others
- **+** Published on PyPI with docs, a live demo and several accompanying papers
- **−** Linux only; most scenarios need Docker usable without sudo
- **−** Needs a chat model with json_mode plus an embedding model, so API costs apply
- **−** Data science setup requires manual dataset download and several .env variables
- **−** Web UI excludes the data_science scenario

<sub>Needs Docker, Conda, Qlib, LiteLLM, LLM API with embeddings · Models: OpenAI, Azure OpenAI, DeepSeek, LiteLLM providers, SiliconFlow embeddings · [Repo](https://github.com/microsoft/rd-agent) · [▶️ Demo ↗](https://rdagent.azurewebsites.net) · [📖 Docs ↗](https://rdagent.readthedocs.io/en/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rd-agent/)</sub>

<a name="opencreator"></a>
### #&#8288;23 [opencreator](https://github.com/krillinai/opencreator) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (8) · Freshness: active (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**Creator workspace for video translation, image and video generation, built on Codex CLI.**

OpenCreator (formerly KrillinAI) pairs a visual workspace with an agent chat that uses Codex CLI as its execution engine. It ships creator tools for video translation, video downloading, image and video generation, voiceovers and article or script writing. A desktop app wraps the same web frontend and a local runtime.

- **+** Video translation covers 14 source and 101 target languages, with bilingual subtitles and dubbing
- **+** Reuses Codex agent loop, Skills and MCP config instead of a second engine
- **+** Local transcription via faster-whisper, WhisperKit or whisper.cpp where available
- **+** Every revision is saved as a new version, keeping earlier settings and outputs
- **−** Depends on Codex CLI and a configured model provider or ChatGPT sign-in
- **−** Image, video and voice generation need external services set under AI Services
- **−** Auto Clips and Digital Avatar are still in development
- **−** No Docker or compose files detected; hardware requirements are not stated

<sub>GPU optional · Needs Codex CLI, yt-dlp, OpenAI-compatible LLM provider, Image/video/voice provider APIs · Models: OpenAI GPT, DeepSeek, Qwen, Kimi, GLM · [Repo](https://github.com/krillinai/opencreator) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opencreator/)</sub>

<a name="autoresearchclaw"></a>
### #&#8288;24 [autoresearchclaw](https://github.com/aiming-lab/autoresearchclaw) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (15) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Aug 2026</sub>

**23-stage pipeline that turns a research topic into a LaTeX paper.**

Runs a 23-stage pipeline from a topic to a paper. It searches literature via OpenAlex, Semantic Scholar and arXiv, runs sandboxed experiments, applies multi-agent review, and exports NeurIPS/ICML/ICLR LaTeX with BibTeX. It runs fully autonomous or with human approval in co-pilot modes, via CLI, Python API, OpenClaw, or ACP agents such as Claude Code.

- **+** Outputs LaTeX, BibTeX, experiment code and charts in one deliverables folder
- **+** Citation verification checks arXiv, CrossRef, DataCite and an LLM
- **+** Six human-in-the-loop modes, from full-auto to step-by-step
- **+** Can use ACP agent CLIs as the LLM backend without API keys
- **−** No Docker or compose files detected; setup is pip plus an interactive setup command
- **−** Needs an LLM provider or agent CLI; quick start uses an OpenAI key
- **−** Domain executors such as HEP via Magnus cloud add external dependencies
- **−** RAM and GPU requirements are not stated in the README

<sub>GPU optional · Needs Python 3.11+, LLM API or ACP agent CLI, OpenAlex / Semantic Scholar / arXiv, LaTeX, Docker (optional) · Models: OpenAI-compatible APIs, ACP agents (Claude Code, Codex CLI, Gemini CLI, Copilot CLI, Kimi CLI, OpenCode) · [Repo](https://github.com/aiming-lab/autoresearchclaw) · [📖 Docs ↗](https://github.com/aiming-lab/AutoResearchClaw/blob/main/docs/integration-guide.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autoresearchclaw/)</sub>

<a name="ax"></a>
### #&#8288;25 [ax](https://github.com/google/ax) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (11) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Sep 2026</sub>

**Kubectl-style orchestrator that runs sandboxed agent tasks from YAML manifests.**

AX is a Go CLI and control plane that schedules agent workloads on Kubernetes through ax.io/v1alpha1 manifests (Task, Workspace, Model). Each task runs as a sandboxed actor on Agent Substrate, with Git repos, MCP servers and skills pre-wired. Tasks can be suspended and resumed, and `ax ssh` opens a shell in a running sandbox. The README warns of heavy development and likely breaking changes.

- **+** kubectl-shaped CLI: apply, get, describe, watch, delete, plus suspend/resume and ssh
- **+** Declarative Workspace manifests pre-wire Git repos, MCP servers and skill packages
- **+** Checkpoint and resume of idle agent tasks via ax suspend and ax resume
- **+** Follows the active kube context, so one CLI can target multiple clusters
- **−** README warns of heavy development and major breaking changes before a stable release
- **−** Requires a Kubernetes cluster with Agent Substrate installed first
- **−** Deploy needs Go, ko, kubectl and a container registry; no Docker or compose option
- **−** API is v1alpha1; the README shows only a Google Gemini model example

<sub>Needs Kubernetes, Agent Substrate, Redis, ko, kubectl, container registry · Models: Google Gemini · [Repo](https://github.com/google/ax) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ax/)</sub>

<a name="ui-tars-desktop"></a>
### #&#8288;26 [ui-tars-desktop](https://github.com/bytedance/ui-tars-desktop) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: patchy (39) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Oct 2026</sub>

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

<a name="edict"></a>
### #&#8288;27 [edict](https://github.com/cft0808/edict) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (27) · Freshness: recent (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · May 2026</sub>

**Multi-agent pipeline on OpenClaw with a mandatory review stage and live dashboard.**

Edict runs 12 role-specific agents on OpenClaw, modeled on Tang-dynasty ministries. A triage agent routes messages, a planner splits tasks, a review agent can reject plans, and ministry agents execute in parallel. A Python stdlib dashboard shows a Kanban board, timelines, agent heartbeats and per-agent model switching. A state machine validates task transitions and writes an audit log.

- **+** Mandatory review agent can reject plans and force rework before execution
- **+** Dashboard with Kanban, timelines, heartbeats, and stop/cancel/resume controls
- **+** State machine rejects illegal task transitions; changes are written to an audit log
- **+** Dashboard server uses only the Python standard library
- **−** Full setup requires OpenClaw; the Docker image is a demo with mock data
- **−** Full install supports macOS and Linux only
- **−** README is mostly Chinese; English and Japanese versions are separate files
- **−** Redis Streams backend sits beside the stdlib server; how they fit together is unclear

<sub>no GPU · Docker + Compose · Needs OpenClaw, Python 3.10+, Node.js 18+ (frontend build), Redis (async backend), Feishu/Telegram/Signal (message channels) · Models: Any LLM provider configured in OpenClaw · port 7891 · [Repo](https://github.com/cft0808/edict) · [📖 Docs ↗](https://github.com/cft0808/edict/blob/main/docs/getting-started.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/edict/)</sub>

<a name="botpress"></a>
### #&#8288;28 [Botpress](https://github.com/botpress/botpress) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (20) · Freshness: recent (70) · Maintenance: patchy (39) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

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
