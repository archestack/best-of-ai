# 🧩 Agent platforms reviews · Best of Open-Source AI

Visual or code-first builders for agents and workflows, with orchestration, tools and deployment. Back to the [leaderboard](../README.md#-agent-platforms).

<sub>🌐 Also on the web: [Agent platforms on archestack.com](https://archestack.com/best-of-ai/agent-platforms/), each project on its own page.</sub>

<a name="autogpt"></a>
### 🥇 [AutoGPT](https://github.com/significant-gravitas/autogpt) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 188k · custom license · Oct 2026</sub>

**Role-based AI agents coordinated by one lead agent, plus a visual workflow builder.**

AutoGPT is a platform where a coordinator agent (Otto) hands work to configurable specialist agents called Experts, each with its own instructions, skills and connected apps. It also has a block-based visual workflow builder and a workflow marketplace. It runs as a paid hosted service or self-hosted from a single Docker image with your own model credentials.

- **+** Single-container Docker image for self-hosting, plus an installer for Linux, macOS and Windows
- **+** Visual builder with branching logic and a marketplace of reusable workflows
- **+** Per-Expert account access and spending controls
- **+** Self-hosting accepts your own model credentials or a local model
- **−** Platform code is Polyform Shield, not OSI open source; only classic/ is MIT
- **−** Hosted Platform is paid; built-in model access is not included when self-hosting
- **−** README gives no RAM or GPU requirements; they are in the linked guide
- **−** Original standalone agent moved to classic/; main README centers on the platform

<sub>Needs Docker, model provider credentials or a local model · Models: bring-your-own model credentials, local models · port 3000 · [Repo](https://github.com/significant-gravitas/autogpt) · [▶️ Demo ↗](https://agpt.co/videos/otto-team-demo-v1-1080.mp4) · [📖 Docs ↗](https://agpt.co/docs) · [🌐 Site ↗](https://agpt.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autogpt/)</sub>

<a name="daily-stock-analysis"></a>
### 🥈 [daily_stock_analysis](https://github.com/zhulinsen/daily_stock_analysis) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 67k · MIT · Oct 2026</sub>

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

<a name="langflow"></a>
### 🥉 [Langflow](https://github.com/langflow-ai/langflow) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 156k · MIT · Oct 2026</sub>

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

<a name="dify"></a>
### #&#8288;4 [Dify](https://github.com/langgenius/dify) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 159k · custom license · Oct 2026</sub>

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

<a name="deer-flow"></a>
### #&#8288;5 [deer-flow](https://github.com/bytedance/deer-flow) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · MIT · Oct 2026</sub>

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

<a name="multica"></a>
### #&#8288;6 [Multica](https://github.com/multica-ai/multica) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 54k · custom license · Oct 2026</sub>

**Issue board where coding agent CLIs are assigned work like teammates.**

Multica is a workspace with an issue board where you assign tasks to coding agents such as Claude Code, Codex, Cursor and Kimi. A daemon on your own machine spawns the installed agent CLIs, keeps a timestamped execution log, and moves finished work to review. The backend is Go with PostgreSQL 17, with web, Electron desktop and Expo mobile clients.

- **+** Drives 26 existing agent CLIs, so switching providers is a dropdown change
- **+** Code runs on your own daemon machine, not on the Multica server
- **+** Per-run execution log, cost analytics, review gates, retries and timeouts
- **+** Self-host via Docker Compose or Helm; GitHub, GitLab, Gitea and Forgejo supported
- **−** Ships no model; needs at least one agent CLI installed and signed in
- **−** Custom Multica License: Apache 2.0 plus conditions on hosting, embedding, branding
- **−** Self-hosting needs Docker and PostgreSQL 17 alongside the Go backend
- **−** iOS app builds from source only; some chat channels are community-maintained

<sub>no GPU · Docker + Compose · Needs Docker, PostgreSQL 17, Agent CLI (Claude Code, Codex, Cursor, etc.) · Models: Claude Code, OpenAI Codex, Cursor Agent, GitHub Copilot CLI, OpenCode · [Repo](https://github.com/multica-ai/multica) · [📖 Docs ↗](https://multica.ai/docs) · [🌐 Site ↗](https://multica.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/multica/)</sub>

<a name="resume-matcher"></a>
### #&#8288;7 [resume-matcher](https://github.com/srbhr/resume-matcher) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

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

<a name="fastgpt"></a>
### #&#8288;8 [FastGPT](https://github.com/labring/fastgpt) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

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

<a name="suna"></a>
### #&#8288;9 [suna](https://github.com/kortix-ai/suna) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Oct 2026</sub>

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

<sub>no GPU · Needs Docker, Docker Hub, Pipedream, GitHub · Models: Any provider with your own API keys, ChatGPT subscription · README: alternative to ChatGPT · [Repo](https://github.com/kortix-ai/suna) · [📖 Docs ↗](https://kortix.com/docs) · [🌐 Site ↗](https://kortix.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/suna/)</sub>

<a name="sim"></a>
### #&#8288;10 [Sim](https://github.com/simstudioai/sim) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;11 [Paperclip](https://github.com/paperclipai/paperclip) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 106k · MIT · Oct 2026</sub>

**Task manager and org chart for coordinating teams of AI coding agents.**

Paperclip is a Node.js server with a React UI that orchestrates external agents (Claude Code, Codex, Cursor, Gemini CLI, OpenCode, OpenClaw, and others) as a company with an org chart, goals, budgets and approval gates. Agents are woken by heartbeats for assigned tasks or schedules, and work, comments and run history are kept per task. It supports multiple organizations per deployment, routines on cron/webhook/API triggers, shared skills, and MCP-based connections.

- **+** Works with many agent runtimes via adapters, plus custom processes and HTTP endpoints
- **+** Budgets per company, agent and project with warning thresholds and hard stops
- **+** Atomic task checkout with execution locks prevents two runs claiming one task
- **+** Approval stages, revisioned config changes with rollback, and multi-organization separation
- **−** Does not run models itself; needs separately configured agents and provider access
- **−** Budget stops rely on reported spend, so in-flight work can overrun limits
- **−** Agent Chat and chat/email connectors are experimental and need enabling
- **−** Hardware, database and port requirements are not stated in the visible README

<sub>no GPU · Docker + Compose · Needs Node.js, External agent runtimes (Claude Code, Codex, etc.) · Models: Claude Code, Codex, Cursor, Gemini CLI, OpenCode · [Repo](https://github.com/paperclipai/paperclip) · [📖 Docs ↗](https://docs.paperclip.ing) · [🌐 Site ↗](https://paperclip.ing) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paperclip/)</sub>

<a name="vibe-trading"></a>
### #&#8288;12 [vibe-trading](https://github.com/hkuds/vibe-trading) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Oct 2026</sub>

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

<a name="skyvern"></a>
### #&#8288;13 [Skyvern](https://github.com/skyvern-ai/skyvern) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · AGPL-3.0 · Oct 2026</sub>

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

<a name="openmaic"></a>
### #&#8288;14 [openmaic](https://github.com/thu-maic/openmaic) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Oct 2026</sub>

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

<a name="bisheng"></a>
### #&#8288;15 [bisheng](https://github.com/dataelement/bisheng) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Oct 2026</sub>

**Enterprise LLM app platform with visual workflows, knowledge spaces and a task agent.**

BISHENG is an LLM application platform aimed at enterprises. It combines a visual workflow editor (loops, parallel branches, batch runs, human-in-the-loop pauses), a team knowledge base with file-level permissions and cited AI Q&A, and a Task Mode agent that plans work, runs sub-agents in parallel and produces PPT, Excel or Word output. It also ships department management, approvals, audit logs and an open API.

- **+** Workflow editor supports loops, parallel branches and batch runs in one flow with chat
- **+** RBAC plus ReBAC permissions down to single files, with department and user-group grants
- **+** Includes SSO/LDAP, approvals, audit logs and an open API with service accounts
- **+** Document parsing models (OCR, tables, layout, seals) can be deployed privately for free
- **−** Heavy install: Elasticsearch, Milvus and Onlyoffice by default; 16 GB RAM minimum
- **−** Dashboards and DSH Desktop enterprise access are commercial edition only
- **−** Docs and community channels are mostly Chinese (Feishu wiki, WeChat group)
- **−** README lists no supported model providers or GPU requirements

<sub>RAM ≥ 16 GB · Compose · Needs Docker, Docker Compose, Elasticsearch, Milvus, Onlyoffice, MySQL or Dameng DM8 · port 3001 · [Repo](https://github.com/dataelement/bisheng) · [📖 Docs ↗](https://dataelem.feishu.cn/wiki/ZxW6wZyAJicX4WkG0NqcWsbynde) · [🌐 Site ↗](https://dataelem.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bisheng/)</sub>

<a name="openmontage"></a>
### #&#8288;16 [openmontage](https://github.com/calesthio/openmontage) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · AGPL-3.0 · Oct 2026</sub>

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
### #&#8288;17 [Agent Zero](https://github.com/agent0ai/agent-zero) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Oct 2026</sub>

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

<a name="trigger-dev"></a>
### #&#8288;18 [trigger.dev](https://github.com/triggerdotdev/trigger.dev) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · [Repo](https://github.com/triggerdotdev/trigger.dev) · [📖 Docs ↗](https://trigger.dev/docs) · [🌐 Site ↗](https://trigger.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trigger-dev/)</sub>

<a name="crm"></a>
### #&#8288;19 [crm](https://github.com/trycompai/crm) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Oct 2026</sub>

**Single-tenant CRM where a background agent researches and fills in contact records.**

A single-tenant CRM (Next.js, NestJS, Prisma, Postgres) paired with a separate agent deployment built on eve. The agent runs from a Postgres-backed work queue, researches contacts and companies, and writes facts only when evidence is strong; weak evidence becomes a suggestion for a rep. It reads Gmail or Microsoft mail, and outside data sources are optional.

- **+** Agent runs on its own queue (FOR UPDATE SKIP LOCKED leases) and keeps working with the browser closed
- **+** Works with no external API keys by reading your own mail threads, meetings and signatures
- **+** Agent sandbox has deny-all egress and is never given DATABASE_URL
- **+** MIT license; type-safe tRPC from Prisma rows to the front end
- **−** Three deployments plus Postgres; production path assumes Vercel, AI Gateway, Sandbox and Blob
- **−** Single tenant by design; no organizations or multi-workspace support
- **−** Sign-in requires a Google or Microsoft OAuth app, or a custom IdP configured after login
- **−** Agent depends on eve and Vercel AI Gateway; local model support is not documented

<sub>no GPU · Compose · Needs Postgres, Bun, Docker, Vercel AI Gateway, Vercel Sandbox, Vercel Blob, Google or Microsoft OAuth, Redis (optional), Perplexity (optional), Context API (optional) · Models: Vercel AI Gateway · port 3000 · [Repo](https://github.com/trycompai/crm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/crm/)</sub>

<a name="rocketride-server"></a>
### #&#8288;20 [rocketride-server](https://github.com/rocketride-org/rocketride-server) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

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

<sub>Docker + Compose · Needs VS Code or compatible IDE, Docker (optional), Vector database (for RAG), LLM API key (for hosted models) · Models: OpenAI, Anthropic, 15+ LLM providers, local models · port 5565 · [Repo](https://github.com/rocketride-org/rocketride-server) · [📖 Docs ↗](https://docs.rocketride.org/) · [🌐 Site ↗](https://rocketride.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rocketride-server/)</sub>

<a name="mindshub"></a>
### #&#8288;21 [mindshub](https://github.com/mindsdb/mindshub) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

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

<sub>Docker + Compose · Needs make, uv, Python 3.10-3.13, Electron · Models: Claude, GPT, Gemini, DeepSeek, Qwen · [Repo](https://github.com/mindsdb/mindshub) · [▶️ Demo ↗](https://console.mindshub.ai/) · [📖 Docs ↗](https://docs.mindshub.ai/) · [🌐 Site ↗](https://mindshub.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mindshub/)</sub>

<a name="hive"></a>
### #&#8288;22 [hive](https://github.com/aden-hive/hive) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**Runtime where a queen agent spawns parallel worker agents sharing a SQLite tracker.**

Hive runs a persistent "queen" agent that does one unit of a job itself, saves the method as a skill, then fans the rest out to parallel worker clones through tool calls rather than a drawn graph. Workers write results to a shared SQLite tracker the queen queries, and state is saved to disk so runs resume after a crash. It uses LiteLLM providers, MCP servers, and cron or webhook triggers.

- **+** One agent-loop primitive; workers are clones, so no workflow graph to design
- **+** Shared SQLite tracker lets runs be queried, audited and resumed from where they stopped
- **+** Any LiteLLM provider, OpenAI-compatible endpoint, or local Ollama model; workers can use a different model
- **+** Hard per-worker tool-call budgets, default four concurrent workers, and cron or webhook triggers
- **−** No dollar spending limits yet; only turn, tool-call and concurrency caps
- **−** Repo is a uv workspace; pip install -e . does not work, quickstart script required
- **−** Memory scores 88.4% on LongMemEval-S, below the 96.8% of reading full history
- **−** No Docker or compose files detected; needs Python 3.11+ and Node.js 20+

<sub>GPU optional · Needs Python 3.11+, Node.js 20+, git, uv, ripgrep, Ollama (optional, for local models) · Models: Anthropic, OpenAI, Google Gemini, Groq, Cerebras · port 8787 · [Repo](https://github.com/aden-hive/hive) · [📖 Docs ↗](https://docs.adenhq.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hive/)</sub>

<a name="yuxi"></a>
### #&#8288;23 [yuxi](https://github.com/xerrors/yuxi) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · MIT · Oct 2026</sub>

**Multi-tenant agent platform with Milvus RAG, Neo4j graphs and LangGraph agents.**

Yuxi is a self-hosted, multi-user platform that combines document RAG (Milvus, MinerU/PaddleX/RapidOCR parsing, rerank), a Neo4j knowledge graph, and LangGraph-based agents with SubAgents, Skills, MCP and sandboxed file tools. Admins manage users, departments, model credentials and sharing scopes. The stack is Vue, FastAPI and PostgreSQL, started with Docker Compose.

- **+** Per-user, department and tenant permissions over knowledge bases, agents, Skills and models
- **+** Built-in RAG evaluation and retrieval testing with embedding and rerank scores
- **+** Supports MCP, Skills, SubAgents and sandboxed file output with in-browser preview
- **+** Connects OpenAI, Anthropic, DeepSeek, Qwen and OpenAI-compatible endpoints such as vLLM
- **−** Heavy stack: Milvus, Neo4j, PostgreSQL, MinerU and PaddleOCR all run in Compose
- **−** README is mainly Chinese; English version is a separate file
- **−** Upgrading from v0.7.1 or v0.7.2 needs downtime, backup and migration
- **−** Hardware requirements are not stated in the README

<sub>Docker + Compose · Needs Docker Compose, Milvus, Neo4j, PostgreSQL, MinerU, PaddleOCR, LangGraph, LLM API · Models: OpenAI, Anthropic, DeepSeek, Qwen, SiliconFlow · port 5173 · [Repo](https://github.com/xerrors/yuxi) · [📖 Docs ↗](https://xerrors.github.io/Yuxi/intro/quick-start) · [🌐 Site ↗](https://xerrors.github.io/Yuxi/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yuxi/)</sub>

<a name="opencreator"></a>
### #&#8288;24 [opencreator](https://github.com/krillinai/opencreator) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

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

<a name="reef"></a>
### #&#8288;25 [reef](https://github.com/human-agent-society/reef) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · Apache-2.0 · Oct 2026</sub>

**Serves agent traffic, collects feedback, and publishes versioned weight or harness updates.**

Reef is a Python server that exposes OpenAI- and Anthropic-compatible endpoints, records each interaction, and matches later score or feedback reports to it by receipt header. A configured recipe then either trains model weights (Slime with SGLang) or rewrites the agent harness (prompts, rules, skills), and accepted updates are committed to a version history without restarting the server.

- **+** Harness-evolving recipes (Reefine) need only a model endpoint, no training GPUs
- **+** Serves /v1/chat/completions, /v1/responses and /v1/messages while updates roll in live
- **+** Versioned artifact history with candidate evaluation; rejected candidates leave the current release serving
- **+** Recipe catalog with measured benchmarks (AIME 2025, IMOAnswerBench, Terminal-Bench, WildClawBench)
- **−** Weight training needs a supported GPU stack; exact GPU requirements are only in linked docs
- **−** Requires Python 3.12+ and git-lfs; no Docker or compose files provided
- **−** Most recipes live in the repo's recipes/ cookbook and are not shipped in the wheel
- **−** Reefine proposer sandbox needs Linux with bwrap and pasta; pi runs commands unsandboxed

<sub>GPU optional · Docker · Needs git-lfs, Slime, SGLang, uv · Models: Qwen/Qwen2.5-1.5B-Instruct, Ollama-served models (gemma4:26b), OpenAI-compatible upstream providers · port 8900 · [Repo](https://github.com/human-agent-society/reef) · [📖 Docs ↗](https://reefinfra.ai/docs/getting-started/quickstart/) · [🌐 Site ↗](https://reefinfra.ai/docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/reef/)</sub>

<a name="ax"></a>
### #&#8288;26 [ax](https://github.com/google/ax) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

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

<sub>Docker · Needs Kubernetes, Agent Substrate, Redis, ko, kubectl, container registry · Models: Google Gemini · [Repo](https://github.com/google/ax) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ax/)</sub>

<a name="astron-agent"></a>
### #&#8288;27 [astron-agent](https://github.com/iflytek/astron-agent) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Oct 2026</sub>

**Agentic workflow platform with model management, MCP tools and RPA nodes.**

Astron Agent is a platform for building and running agent workflows, with orchestration, model management, MCP and iFLYTEK tool integration, and RPA steps for driving other enterprise systems. It deploys via Docker Compose with a Casdoor authentication service and an nginx-proxied frontend. Published workflows can be called from other projects over HTTP/SSE.

- **+** Apache-2.0 with no stated commercial restrictions
- **+** RPA integration (AstronRPA) lets agents act on other systems
- **+** Published workflows callable over HTTP/SSE from existing projects
- **+** Casdoor authentication included in the compose deployment
- **−** Helm chart is not released; Kubernetes deployment is marked as under development
- **−** Many ready-made tools come from the iFLYTEK Open Platform
- **−** Compose setup requires a manual Casdoor password initialization step first
- **−** README gives no RAM, GPU or model-format requirements

<sub>Compose · Needs Docker Compose, Casdoor, nginx · Models: API-based models, on-premises MaaS clusters · port 80 · [Repo](https://github.com/iflytek/astron-agent) · [▶️ Demo ↗](https://agent.xfyun.cn) · [📖 Docs ↗](https://github.com/iflytek/astron-agent/blob/main/docs/DEPLOYMENT_GUIDE_WITH_AUTH.md) · [🌐 Site ↗](https://iflytek.github.io/astron-agent/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/astron-agent/)</sub>

<a name="mirofish"></a>
### #&#8288;28 [mirofish](https://github.com/666ghj/mirofish) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: widely used (92) · Freshness: active (96) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 81k · AGPL-3.0 · Oct 2026</sub>

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
### #&#8288;29 [ui-tars-desktop](https://github.com/bytedance/ui-tars-desktop) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Oct 2026</sub>

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

<a name="trueforge"></a>
### #&#8288;30 [trueforge](https://github.com/truefoundry/trueforge) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Oct 2026</sub>

**Agent runtime with chat UI, HTTP API and TypeScript SDK.**

TrueForge runs the agent loop server-side: model calls, remote MCP tools, git-backed SKILL.md skills, sandboxed code execution, tool approvals, context compaction and session state. It is used through a bundled chat UI, an HTTP API with a TypeScript SDK, or an embeddable UI package. Local mode runs as one Node process with SQLite; hosted mode uses Postgres and Redis.

- **+** Two run modes: single process with SQLite, or Postgres + Redis via Compose, Helm or Railway
- **+** Works with OpenAI, Anthropic, Gemini or any OpenAI-compatible endpoint
- **+** Remote MCP servers supported with header auth or OAuth, including in-chat authorization
- **+** Includes subagents, deferred tool loading, Code Mode, large-result offloading and compaction
- **−** Only Daytona is supported as a sandbox provider today; others are planned
- **−** Local mode has no login by default and is not meant for exposure beyond localhost
- **−** Hosted mode needs Postgres and Redis; OIDC login is optional and configured separately
- **−** Benchmark claims against Claude Managed Agents and deepagents are the vendor's own

<sub>no GPU · Docker + Compose · Needs Node.js >= 22.14, SQLite (local mode), Postgres (hosted mode), Redis (hosted mode), Daytona (sandbox) · Models: OpenAI, Anthropic, Google Gemini, OpenAI-compatible endpoints · [Repo](https://github.com/truefoundry/trueforge) · [📖 Docs ↗](https://trueforge.dev/introduction) · [🌐 Site ↗](https://trueforge.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trueforge/)</sub>

<a name="bettafish"></a>
### #&#8288;31 [bettafish](https://github.com/666ghj/bettafish) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: widely used (83) · Freshness: active (90) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · GPL-2.0 · Oct 2026</sub>

**Multi-agent public opinion analysis over social media and web search.**

BettaFish (微舆) runs Query, Media and Insight agents in parallel over web search and crawled social media data. A forum mechanism with an LLM moderator steers them across rounds, and a Report agent renders an interactive HTML report, with optional PDF and Markdown export. A Flask app serves the UI, and a bundled crawler (MindSpider) fills a PostgreSQL or MySQL database.

- **+** Bundles crawler, sentiment models (BERT, GPT-2, Qwen3 LoRA) and report renderer in one Python codebase
- **+** Forum engine lets agents exchange findings over several rounds before the report is written
- **+** Any OpenAI-compatible LLM API, configurable per agent through a single .env file
- **+** Each agent also runs standalone as a Streamlit app; a CLI regenerates reports from earlier runs
- **−** Needs a PostgreSQL or MySQL database, and crawling is run separately before there is data
- **−** Main README is in Chinese; English docs live in a separate file
- **−** Built for opinion analysis; other domains require editing agent tools and prompts
- **−** PDF export needs extra system libraries for WeasyPrint

<sub>RAM ≥ 2 GB · GPU optional · Docker + Compose · Needs PostgreSQL or MySQL, OpenAI-compatible LLM API, Playwright Chromium (crawler), WeasyPrint system libraries (PDF export, optional) · Models: OpenAI-compatible API · port 5000 · [Repo](https://github.com/666ghj/bettafish) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bettafish/)</sub>

<a name="openbot"></a>
### #&#8288;32 [openbot](https://github.com/copilotkit/openbot) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · MIT · Oct 2026</sub>

**Self-hosted team assistant where each bot gets its own browser and audited actions.**

OpenBot is a clonable template for a company-run, ChatGPT-style assistant. Any AG-UI agent endpoint becomes a Bot with its own container, Chromium profile and workspace. Every browser, file, shell and MCP action passes a gateway that applies a CEL policy and writes an audit row first. Data is stored in PostgreSQL, and threads go through CopilotKit Intelligence. The README labels it alpha.

- **+** Per-Bot container with own browser profile and workspace volume, optional gVisor (runsc) runtime
- **+** Single gateway applies CEL deny/allow policy and logs every action; refusals name the rule
- **+** Works with any AG-UI endpoint: LangGraph, Mastra, CrewAI, Pydantic AI, Google ADK or custom
- **+** SAML/OIDC, Google, Microsoft and Okta sign-in, plus admin pages for people, audit and credentials
- **−** Marked alpha; README warns of rough edges and changing behavior
- **−** Requires a CopilotKit Intelligence project and license for threads and memory
- **−** Template to clone and customize, not a published package or hosted product
- **−** Local setup defaults to single-user mode with no sign-in until configured

<sub>no GPU · Docker + Compose · Needs Docker, PostgreSQL, Bun 1.3+, CopilotKit Intelligence, LLM API key · Models: OpenAI, Anthropic, Google, any AG-UI agent endpoint · port 3010 · [Repo](https://github.com/copilotkit/openbot) · [🌐 Site ↗](https://copilotkit.ai/openbot) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openbot/)</sub>

<a name="yao"></a>
### #&#8288;33 [yao](https://github.com/yaoapp/yao) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · custom license · Oct 2026</sub>

**Self-hosted agent manager with isolated workspaces and a task board.**

Yao Agents runs agents on machines you own and manages them from one place, through a desktop app, Android beta, browser or API. Conversations become tasks on a kanban board, and each isolated workspace accumulates documents as a knowledge base. Agents are exposed through standard APIs with SSE and WebSocket support.

- **+** Runs agents across multiple devices you add, managed from one place
- **+** Task board turns conversation requests into tracked tasks
- **+** Isolated workspaces keep work separate and build up documents
- **+** API access over SSE and WebSocket for embedding agents in your apps
- **−** README gives no install steps, hardware needs or supported model list
- **−** License is not identified (NOASSERTION), so terms need manual checking
- **−** Android client is labeled beta
- **−** No Docker or compose files detected

<sub>Docker · Models: DeepSeek Harness, Jev · [Repo](https://github.com/yaoapp/yao) · [📖 Docs ↗](https://yaoagents.com/docs) · [🌐 Site ↗](https://yaoagents.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yao/)</sub>

<a name="rd-agent"></a>
### #&#8288;34 [rd-agent](https://github.com/microsoft/rd-agent) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (49) · Freshness: active (100) · Maintenance: patchy (47) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Sep 2026</sub>

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

<a name="ufo"></a>
### #&#8288;35 [ufo](https://github.com/microsoft/ufo) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

**GUI agent for Windows, plus a multi-device DAG orchestrator for agents.**

UFO² drives Windows apps through UI Automation, Win32 and COM, mixing GUI clicks with API calls, using an LLM such as OpenAI or Azure OpenAI. UFO³ Galaxy adds a ConstellationAgent that splits a request into a task DAG and runs it in parallel across Windows, Linux and Android device agents over a WebSocket protocol (AIP).

- **+** Hybrid UIA/Win32/COM control with GUI fallback for Windows automation
- **+** Galaxy decomposes tasks into DAGs and runs them in parallel across devices
- **+** Speculative multi-action batching reported to cut LLM calls by 51%
- **+** Backed by published papers and online docs; MIT license
- **−** UFO² is Windows-only; Galaxy is marked active development with moderate setup
- **−** Needs a hosted LLM API key such as gpt-4o; local model setup not described
- **−** Galaxy setup needs per-device servers and clients plus YAML configs
- **−** No Docker or compose files; setup is pip install and manual config

<sub>no GPU · Needs Python 3.10 or 3.11, LLM API key (OpenAI or Azure OpenAI) · Models: OpenAI, Azure OpenAI, Qwen, Gemini, Claude · [Repo](https://github.com/microsoft/ufo) · [▶️ Demo ↗](https://www.youtube.com/watch?v=NGrVWGcJL8o) · [📖 Docs ↗](https://microsoft.github.io/UFO/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ufo/)</sub>

<a name="cloudflare-os"></a>
### #&#8288;36 [cloudflare-os](https://github.com/cloudflare/cloudflare-os) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (35) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Oct 2026</sub>

**Agent chat workspace where AI builds sandboxed per-user apps with approval-gated access.**

Cloudflare OS is an internal Cloudflare productivity environment, now open source, built on Workers, Durable Objects and Dynamic Workers. Users chat with a Code Mode agent that does tasks directly or builds small private apps called gadgets, each in its own sandbox. External services are reached through Gatekeepers, which log actions and queue side-effecting ones for later human approval. The README labels it early access.

- **+** Gadgets run in Dynamic Worker sandboxes with internet disabled and iframe-isolated clients
- **+** Gatekeepers simulate side effects; users approve or reject queued actions in bulk later
- **+** Capability-based access: agents and gadgets get no resources until explicitly introduced
- **+** Runs locally with `pnpm run-local` on wrangler and workerd; works with many LLM providers
- **−** README calls it early access with many rough edges; this is a version 2 rewrite
- **−** Self-hosting on plain workerd is marked COMING SOON; local mode is not for production
- **−** Depends on Workers features such as Durable Objects, Facets and Dynamic Workers
- **−** Each Gatekeeper needs its own OAuth credentials; outside contributions largely not accepted

<sub>no GPU · Needs pnpm, wrangler, workerd, Cloudflare account (for hosted deploy), LLM provider · Models: Many major LLM providers via pi-agent-core, self-hosted models · port 8787 · [Repo](https://github.com/cloudflare/cloudflare-os) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cloudflare-os/)</sub>

<a name="autoresearchclaw"></a>
### #&#8288;37 [autoresearchclaw](https://github.com/aiming-lab/autoresearchclaw) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: known (46) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Aug 2026</sub>

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

<a name="paperbanana"></a>
### #&#8288;38 [paperbanana](https://github.com/dwzhu-pku/paperbanana) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Oct 2026</sub>

**Multi-agent pipeline that drafts academic paper diagrams and plots from method text.**

PaperBanana turns a paper's method section and figure caption into publication-style diagrams and plots. It chains Retriever, Planner, Stylist, Visualizer and Critic agents, using reference examples from PaperBananaBench and multi-round critic refinement. It runs through a Gradio app, a Streamlit demo or a CLI, calling Gemini or OpenRouter models over API.

- **+** Five-agent pipeline with a Critic-Visualizer refinement loop and selectable pipeline modes
- **+** Gradio app, Streamlit demo with refine/upscale tab, and a CLI
- **+** Hosted Hugging Face Space for trying it without setup
- **+** Generates up to 20 candidates in parallel with Gemini or OpenRouter keys
- **−** Needs external API keys for both the main model and the image generation model
- **−** Output quality relies on PaperBananaBench references, which cover mainly computer science
- **−** Statistical plot code and manual example selection are still on the TODO list
- **−** No tagged release; manual setup with uv and Python 3.12

<sub>no GPU · Docker · Needs Google Gemini or OpenRouter API key, uv, Python 3.12, PaperBananaBench dataset (Hugging Face) · Models: Gemini, OpenRouter, OpenAI gpt-image · [Repo](https://github.com/dwzhu-pku/paperbanana) · [▶️ Demo ↗](https://huggingface.co/spaces/dwzhu/PaperBanana) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paperbanana/)</sub>

<a name="intentkit"></a>
### #&#8288;39 [intentkit](https://github.com/crestalnetwork/intentkit) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: patchy (47) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Sep 2026</sub>

**Self-hosted cluster of collaborating AI agents with a skill system and API.**

IntentKit runs a team of AI agents on your own server, where agents can call each other and use pluggable skills. It can be deployed with Docker, imported as a Python library, or driven from other applications through its built-in API. The README also lists optional Web3 and social media integrations.

- **+** Multiple agents can call and interact with each other
- **+** Usable as a Python library or through built-in API endpoints
- **+** README states agents cannot access your secret keys
- **+** Extensible skill system for adding capabilities
- **−** README gives no hardware, database or model provider requirements
- **−** Does not accept pull requests; issues only
- **−** Setup details live in external docs, not the README
- **−** Crypto and social integrations may add scope you do not need

<sub>Docker + Compose · Compose runs PostgreSQL, Redis · [Repo](https://github.com/crestalnetwork/intentkit) · [📖 Docs ↗](https://intentcat.com/docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/intentkit/)</sub>

<a name="finrobot"></a>
### #&#8288;40 [finrobot](https://github.com/ai4finance-foundation/finrobot) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · Apache-2.0 · Sep 2026</sub>

**Multi-agent equity research with code-computed valuations and LLM-written reports.**

FinRobot is a financial agent project in three generations: an AutoGen library (V0, educational), an OpenAI Agents SDK web app (V1), and a PydanticAI desktop, web and CLI system (V2). V2 runs a lead agent, five pipeline agents and three debate agents. DCF, DDM, LBO and comps figures come from pure-Python operators, and the LLM only writes the narrative.

- **+** Valuation numbers come from 32 deterministic Python operators, not the LLM
- **+** Seven data providers with failover, including SEC EDGAR, FMP, Finnhub and yfinance
- **+** V2 runs as a desktop app, a local web UI or a CLI
- **+** Ships 56 analyst playbooks and 7 research pipelines
- **−** Three separate codebases; pip install finrobot gives only the V0 educational package
- **−** Desktop release is macOS Apple Silicon only and not notarized
- **−** Local API in browser mode is unauthenticated
- **−** Needs external API keys such as FMP and OpenAI; V3 is still in development

<sub>no GPU · Docker · Needs FMP API key, Finnhub, OpenAI API key, SEC EDGAR, Node.js, uv · Models: OpenAI, Azure OpenAI · port 5173 · [Repo](https://github.com/ai4finance-foundation/finrobot) · [▶️ Demo ↗](https://finrobot.ai/v2) · [🌐 Site ↗](https://finrobot.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/finrobot/)</sub>

<a name="openfang"></a>
### #&#8288;41 [openfang](https://github.com/rightnow-ai/openfang) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (56) · Freshness: active (81) · Maintenance: weak (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · May 2026</sub>

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

<a name="botpress"></a>
### #&#8288;42 [Botpress](https://github.com/botpress/botpress) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (47) · Freshness: recent (70) · Maintenance: patchy (39) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

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

<a name="mission-control"></a>
### #&#8288;43 [mission-control](https://github.com/builderz-labs/mission-control) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: patchy (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · MIT · Sep 2026</sub>

**Control plane for dispatching and reviewing work across AI agent runtimes.**

Mission Control is a Next.js control plane that sits above agent runtimes such as OpenClaw, Claude Code and Codex. It tracks tasks through assignment, execution and review, and shows agent presence, activity, token use and cost. State is stored in SQLite, and it exposes a web UI, CLI, MCP server, REST/OpenAPI, WebSocket and SSE. The README labels it alpha software.

- **+** SQLite-only state with WAL mode, no separate database server to run
- **+** Web UI, CLI, MCP server and OpenAPI REST API cover the same control plane
- **+** Task board with an Aegis review gate requiring an approval record before done
- **+** Gateway-free REST loop for registering agents and claiming task queues
- **−** Alpha: APIs, schemas and configuration may change between releases
- **−** Adapter depth varies by runtime; feature parity is not guaranteed
- **−** Live session messaging needs a connected runtime gateway
- **−** Network exposure needs a TLS reverse proxy, MC_ALLOWED_HOSTS and hardening

<sub>no GPU · Docker + Compose · Needs Node.js 22+, pnpm, SQLite (better-sqlite3), Agent runtime gateway (optional) · Models: OpenClaw, Claude Code, Codex, CrewAI, LangGraph · port 3000 · [Repo](https://github.com/builderz-labs/mission-control) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mission-control/)</sub>

<a name="edict"></a>
### #&#8288;44 [edict](https://github.com/cft0808/edict) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (53) · Freshness: recent (71) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · May 2026</sub>

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

<a name="promptflow"></a>
### #&#8288;45 [promptflow](https://github.com/microsoft/promptflow) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: known (33) · Freshness: recent (70) · Maintenance: patchy (31) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**Python toolkit for building, tracing and evaluating LLM flows from a CLI.**

Prompt flow defines LLM apps as executable flows in a flow.dag.yaml that link LLM calls, prompts and Python code. It provides a pf CLI for testing flows, managing OpenAI and Azure OpenAI connections, tracing LLM calls and batch-evaluating against datasets, plus a VS Code flow designer. Microsoft has announced retirement on April 20, 2027 and no longer recommends it for new development.

- **+** Flows are YAML DAGs linking LLM, prompt and Python nodes, runnable with `pf flow test`
- **+** Batch runs and evaluation over datasets can be wired into CI/CD
- **+** Built-in tracing of LLM interactions for debugging flows
- **+** VS Code extension offers a visual flow designer
- **−** Retirement announced for April 20, 2027; not recommended for new development
- **−** Runtime container images no longer receive security or package updates
- **−** Last release was 2025-01-09; migration to Microsoft Agent Framework is advised
- **−** Telemetry is on by default; opt out with `pf config set telemetry.enabled=false`

<sub>no GPU · Needs Python 3.9-3.11 recommended, OpenAI or Azure OpenAI API key · Models: OpenAI, Azure OpenAI · [Repo](https://github.com/microsoft/promptflow) · [📖 Docs ↗](https://microsoft.github.io/promptflow/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/promptflow/)</sub>

<a name="magentic-ui"></a>
### #&#8288;46 [magentic-ui](https://github.com/microsoft/magentic-ui) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (28) · Freshness: active (99) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Jul 2026</sub>

**Browser and file-system agent built for small orchestrator and browser-use models.**

MagenticLite is the successor to Magentic-UI from Microsoft AI Frontiers. It pairs an orchestrator model (MagenticBrain) with a browser-use model (Fara) to automate web research, form filling and local file management from a web UI. Browser sessions run in a lightweight VM sandbox (Quicksand), and the agent pauses for approval before critical actions.

- **+** Designed for small models rather than frontier-scale ones
- **+** Browser sessions isolated in a Quicksand VM sandbox
- **+** Approve, steer or take over mid-task; stops before critical actions
- **+** Installs from PyPI with uv and serves a web UI on port 8081
- **−** You must host or connect a model endpoint yourself
- **−** Quick start covers only macOS and Windows via WSL
- **−** Model hardware requirements are not stated in the README
- **−** A limitations doc lists tasks it does not handle well

<sub>Needs uv, Python 3.12, Quicksand VM sandbox, model endpoint · Models: MagenticBrain, Fara · port 8081 · [Repo](https://github.com/microsoft/magentic-ui) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/magentic-ui/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
