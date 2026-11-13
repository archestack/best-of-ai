# 🧩 Agent platforms reviews · Best of Open-Source AI

Visual or code-first builders for agents and workflows, with orchestration, tools and deployment. Back to the [leaderboard](../README.md#-agent-platforms).

<sub>🌐 Also on the web: [Agent platforms on archestack.com](https://archestack.com/best-of-ai/agent-platforms/), each project on its own page.</sub>

<a name="autogpt"></a>
### 🥇 [AutoGPT](https://github.com/significant-gravitas/autogpt) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 188k · custom license · Nov 2026</sub>

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
### 🥈 [daily_stock_analysis](https://github.com/zhulinsen/daily_stock_analysis) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 72k · MIT · Nov 2026</sub>

**LLM-driven daily analysis of watchlist stocks across six markets, pushed to chat apps.**

Python app that pulls quotes, K-lines, news and fundamentals for A-share, HK, US, Japan, Korea and Taiwan tickers, then asks an LLM to produce a decision-dashboard report with score, trend, buy/sell levels and risks. It runs on a GitHub Actions schedule (weekdays 18:00 Beijing time), locally, or in Docker, and pushes results to WeCom, Feishu, Telegram, Discord, Slack or email. A web UI at port 8000 adds history, backtesting, portfolio and multi-turn strategy Q&A.

- **+** Runs free on GitHub Actions with a fork and secrets; no server needed
- **+** Works with Gemini, Claude, OpenAI-compatible APIs, DeepSeek, Qwen or local Ollama
- **+** Free data sources (AkShare, Baostock, YFinance) allow zero-config start
- **+** Pushes to six channels: WeCom, Feishu, Telegram, Discord, Slack, email
- **−** Free market data sources are rate-limited and stability is not guaranteed
- **−** Report quality depends on separately configured news search API keys
- **−** README and config docs are mainly in Chinese; English is a separate file
- **−** Not investment advice per its own disclaimer; outputs are LLM-generated

<sub>no GPU · Docker + Compose · Needs LLM API key (or Ollama), Notification channel webhook/token, Optional: Tushare, Longbridge, SerpAPI, Tavily, Anspire, SearXNG · Models: Gemini, Claude, OpenAI-compatible, DeepSeek, Qwen · port 8000 · [Repo](https://github.com/zhulinsen/daily_stock_analysis) · [📖 Docs ↗](https://github.com/ZhuLinsen/daily_stock_analysis/blob/main/docs/full-guide.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/daily-stock-analysis/)</sub>

<a name="deer-flow"></a>
### 🥉 [deer-flow](https://github.com/bytedance/deer-flow) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 85k · MIT · Nov 2026</sub>

**Agent harness running sub-agents, memory and sandboxes with pluggable skills.**

DeerFlow 2.0 is a ground-up rewrite of ByteDance's deep research framework. It is a Python backend with a web UI that orchestrates a lead agent, sub-agents, long-term memory and sandboxed execution, extended through skills and MCP. Setup runs through a `make setup` wizard that writes config.yaml and .env.

- **+** Interactive `make setup` wizard and `make doctor` health check for configuration
- **+** Many search and fetch backends: Tavily, Brave, DuckDuckGo, SearXNG, Jina, InfoQuest
- **+** Optional tracing through LangSmith, Langfuse and Monocle
- **+** Includes sandbox mode, MCP, IM channels, scheduled tasks and an embedded Python client
- **−** 2.0 shares no code with v1; the original research framework lives on the 1.x branch
- **−** README is dense with option-level detail, which buries the core setup steps
- **−** Gateway admin is equivalent to code execution, so deployment needs care
- **−** README recommends specific hosted models; local model guidance is not in the visible text

<sub>Docker + Compose · Needs LLM provider API key, Python 3.12+, Node.js 22+, Docker (recommended) · Models: OpenAI-compatible endpoints, Gemini, Claude, Codex, Doubao-Seed-2.0-Code · [Repo](https://github.com/bytedance/deer-flow) · [🌐 Site ↗](https://deerflow.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deer-flow/)</sub>

<a name="langflow"></a>
### #&#8288;4 [Langflow](https://github.com/langflow-ai/langflow) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 157k · MIT · Nov 2026</sub>

**Visual builder for AI agents and workflows, served as API or MCP server.**

Langflow is a visual editor for building agent and RAG workflows from components whose Python source can be edited. Each flow can be deployed as an HTTP API, exported as JSON for Python apps, or served as an MCP server for MCP clients. It installs with uv/pip (Python 3.10 to 3.14), Docker, or a Windows/macOS desktop app, and serves its UI on port 7860.

- **+** Every flow can be served as an HTTP API or as an MCP server
- **+** Component source is editable in Python, so custom logic needs no fork
- **+** Interactive playground allows step-by-step testing of flows
- **+** Observability integrations include LangSmith and LangFuse
- **−** Official releases need LANGFLOW_SUPERUSER_PASSWORD set; dev branches default to auto-login
- **−** Desktop app exists only for Windows and macOS
- **−** Requires a Python 3.10 to 3.14 environment for non-Docker installs
- **−** Multi-agent orchestration is listed but not described in detail

<sub>Docker + Compose · Needs Python 3.10-3.14, uv · Models: all major LLMs, vector databases · port 7860 · [Repo](https://github.com/langflow-ai/langflow) · [📖 Docs ↗](https://docs.langflow.org) · [🌐 Site ↗](https://langflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langflow/)</sub>

<a name="open-design"></a>
### #&#8288;5 [open-design](https://github.com/nexu-io/open-design) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 108k · Apache-2.0 · Nov 2026</sub>

**Design workspace that drives your coding agent to build prototypes, decks and video.**

OpenDesign is a desktop and self-hostable workspace that turns a brief into web or mobile prototypes, slide decks, images and HyperFrames motion graphics, using a coding agent already on your PATH such as Claude Code, Codex or Cursor. Output follows a DESIGN.md brand contract, with 151 design-system packages, skills, templates and plugins bundled. A BYOK proxy covers setups without an agent CLI.

- **+** Works with 26 coding-agent CLIs, with MCP setup via `od mcp install <agent>`
- **+** Ships 151 design systems, 15 deck templates and 93 image prompt templates
- **+** BYOK proxy covers OpenAI, Anthropic, Azure, Gemini, Ollama, LM Studio and vLLM, with SSRF checks
- **+** Decks export to HTML, PDF, PPTX, ZIP or Markdown; video renders to MP4
- **−** Ships no agent of its own; needs a separate agent CLI or API key
- **−** No prebuilt Linux desktop release; Linux requires running from source
- **−** Video rendering depends on headless Chrome and FFmpeg
- **−** README promotes paid OpenDesign Cloud and credit plans alongside the open-source app

<sub>no GPU · Docker + Compose · Needs Coding agent CLI or LLM API key, Node.js and pnpm (run from source), Headless Chrome and FFmpeg (video) · Models: Claude Code, Codex CLI, Cursor, DeepSeek Harness, OpenAI-compatible APIs · [Repo](https://github.com/nexu-io/open-design) · [🌐 Site ↗](https://open-design.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-design/)</sub>

<a name="dify"></a>
### #&#8288;6 [Dify](https://github.com/langgenius/dify) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 161k · custom license · Nov 2026</sub>

**Visual builder for LLM workflows, RAG pipelines and agents, with APIs.**

Dify is an LLM app development platform with a visual workflow canvas, a prompt IDE, a RAG pipeline that extracts text from PDFs and PPTs, and agents that run in their own sandbox. Every app is exposed through a generated API, and tools can come from Dify Marketplace, MCP servers or custom APIs. It runs self-hosted via Docker Compose or as the hosted Dify Cloud.

- **+** Visual workflow canvas, prompt IDE and RAG pipeline in one self-hosted app
- **+** Hundreds of model providers, including any OpenAI API-compatible endpoint
- **+** Every app gets a backend API; agents can use MCP servers and marketplace tools
- **+** Observability integrations with Opik, Langfuse and Arize Phoenix
- **−** Custom Dify Open Source License (Apache 2.0 plus conditions), not plain Apache 2.0
- **−** SSO, RBAC and support SLAs are limited to the Enterprise edition
- **−** Compose deployment runs several services and needs a manually generated sandbox auth token
- **−** Docker Compose v2.35.0 or later required

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Needs Docker, Docker Compose v2.35.0+, OpenSSL · Models: OpenAI API-compatible, GPT, Mistral, Llama3 · port 80 · [Repo](https://github.com/langgenius/dify) · [▶️ Demo ↗](https://cloud.dify.ai) · [📖 Docs ↗](https://docs.dify.ai) · [🌐 Site ↗](https://dify.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dify/)</sub>

<a name="resume-matcher"></a>
### #&#8288;7 [resume-matcher](https://github.com/srbhr/resume-matcher) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Nov 2026</sub>

**Resume builder that tailors a master resume to each job description.**

Resume Matcher takes a master resume (PDF or DOCX) and a pasted job description, then generates a tailored resume, cover letter and interview prep using the LLM you configure. It runs a FastAPI backend, a Next.js frontend and a SQLite file, and exports text-based PDFs from ten templates. The ATS score and ATS parse check are plain code with no LLM call.

- **+** Runs locally on SQLite with no account; Ollama keeps the resume on your machine
- **+** ATS score and PDF parse check are deterministic code with documented weightings
- **+** Tailoring prompts forbid adding skills, employers or metrics absent from the master resume
- **+** Background tailoring queue for multiple job descriptions; MCP server lets coding agents drive it
- **−** Non-Docker setup needs Python 3.14+, Node 24.22.1 and uv
- **−** Claude CLI provider is not available inside the Docker images
- **−** Claude subscription route may breach Anthropic plan terms, per the README
- **−** Multi-job description optimization is still on the roadmap

<sub>GPU optional · Docker + Compose · Needs Python 3.14+, Node.js 24.22.1, uv, SQLite · Models: OpenAI, Anthropic, Gemini, DeepSeek, OpenRouter · port 3000 · [Repo](https://github.com/srbhr/resume-matcher) · [📖 Docs ↗](https://resumematcher.fyi/docs/installation/) · [🌐 Site ↗](https://resumematcher.fyi/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/resume-matcher/)</sub>

<a name="fastgpt"></a>
### #&#8288;8 [FastGPT](https://github.com/labring/fastgpt) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Nov 2026</sub>

**Visual workflow builder for knowledge-base agents and RAG apps.**

FastGPT is a TypeScript platform for building AI agents and chat apps with a visual flow editor, chat and plugin workflows, and a built-in knowledge base. Documents (TXT, MD, HTML, PDF, Docx, PPTX, CSV, XLSX) are imported, chunked and searched with hybrid retrieval and reranking. Apps can be shared without login or embedded via iframe, and MCP works in both directions.

- **+** Knowledge base supports hybrid retrieval, reranking, QA splitting and editable chunks
- **+** Call-chain logs, citation editing and app evaluation help debug RAG answers
- **+** Two-way MCP plus hot-updatable system tools via the separate fastgpt-plugin
- **+** Login-free share links and iframe embedding for publishing apps
- **−** Custom license, not OSI: commercial use allowed but offering it as SaaS is not
- **−** Fuller features and support sit in a paid commercial edition
- **−** README and docs are primarily Chinese; English README is a separate file
- **−** Advanced flow debug mode and AI-assisted workflow generation are unchecked on the roadmap

<sub>Compose · port 3000 · [Repo](https://github.com/labring/fastgpt) · [📖 Docs ↗](https://doc.fastgpt.cn/zh-CN/guide/getting-started) · [🌐 Site ↗](https://fastgpt.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fastgpt/)</sub>

<a name="multica"></a>
### #&#8288;9 [Multica](https://github.com/multica-ai/multica) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 56k · custom license · Nov 2026</sub>

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

<a name="sim"></a>
### #&#8288;10 [Sim](https://github.com/simstudioai/sim) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Nov 2026</sub>

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

<a name="openmaic"></a>
### #&#8288;11 [openmaic](https://github.com/thu-maic/openmaic) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · MIT · Nov 2026</sub>

**Generates interactive AI-taught classrooms from a topic or document.**

OpenMAIC is a Next.js and PostgreSQL app that turns a topic or uploaded material into a lesson with slides, quizzes, HTML simulations and project-based learning. AI teacher and classmate agents speak, draw on a whiteboard and discuss with the learner. Models are assigned per task slot in openmaic.yml across many providers, and classrooms export to PPTX, offline HTML or ZIP.

- **+** Per-slot model config in openmaic.yml, with fallbacks and options to lock user overrides
- **+** Exports classrooms to PPTX, a single offline HTML file, or ZIP
- **+** Generation runs server-side and continues after the browser tab closes
- **+** Many providers including Ollama, Lemonade and FunASR for local use, plus any OpenAI-compatible API
- **−** Requires PostgreSQL and a long-running Node process; Vercel and serverless unsupported since 1.2.0
- **−** Docker Compose runs single-user mode and binds to 127.0.0.1 by default
- **−** Several upgrades are one-way (v1.3.0, v1.4.0), and the new workbench home is a release candidate
- **−** Full feature set needs image, video, TTS and search provider keys

<sub>no GPU · Docker + Compose · Needs PostgreSQL 16, Node.js >= 22.19, pnpm >= 10 · Models: OpenAI, Anthropic, Google Gemini, Amazon Bedrock, Azure OpenAI · port 3000 · [Repo](https://github.com/thu-maic/openmaic) · [▶️ Demo ↗](https://open.maic.chat/) · [📖 Docs ↗](https://lcn6dqn3m0yr.feishu.cn/wiki/CkQSwHFdzibQFvkGzwPcmUOfnXg) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmaic/)</sub>

<a name="suna"></a>
### #&#8288;12 [suna](https://github.com/kortix-ai/suna) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · custom license · Nov 2026</sub>

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

<a name="bisheng"></a>
### #&#8288;13 [bisheng](https://github.com/dataelement/bisheng) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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

<sub>RAM ≥ 16 GB · Docker + Compose · Needs Docker, Docker Compose, Elasticsearch, Milvus, Onlyoffice, MySQL or Dameng DM8 · port 3001 · [Repo](https://github.com/dataelement/bisheng) · [📖 Docs ↗](https://dataelem.feishu.cn/wiki/ZxW6wZyAJicX4WkG0NqcWsbynde) · [🌐 Site ↗](https://dataelem.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bisheng/)</sub>

<a name="paperclip"></a>
### #&#8288;14 [Paperclip](https://github.com/paperclipai/paperclip) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 114k · MIT · Nov 2026</sub>

**Task manager and org chart for coordinating teams of AI coding agents.**

Paperclip is a Node.js server with a React UI that orchestrates external agents (Claude Code, Codex, Cursor, Gemini CLI, OpenCode, OpenClaw, and others) as a company with an org chart, goals, budgets and approval gates. Agents are woken by heartbeats for assigned tasks or schedules, and work, comments and run history are kept per task. It supports multiple organizations per deployment, routines on cron/webhook/API triggers, shared skills, and MCP-based connections.

- **+** Works with many agent runtimes via adapters, plus custom processes and HTTP endpoints
- **+** Budgets per company, agent and project with warning thresholds and hard stops
- **+** Atomic task checkout with execution locks prevents two runs claiming one task
- **+** Approval stages, revisioned config changes with rollback, and multi-organization separation
- **−** Does not run models itself; needs separately configured agents and provider access
- **−** Budget stops rely on reported spend, so in-flight work can overrun limits
- **−** Agent Chat and chat/email connectors are experimental and need enabling

<sub>no GPU · Docker + Compose · Needs Node.js, External agent runtimes (Claude Code, Codex, etc.) · Models: Claude Code, Codex, Cursor, Gemini CLI, OpenCode · [Repo](https://github.com/paperclipai/paperclip) · [📖 Docs ↗](https://docs.paperclip.ing) · [🌐 Site ↗](https://paperclip.ing) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paperclip/)</sub>

<a name="vibe-trading"></a>
### #&#8288;15 [vibe-trading](https://github.com/hkuds/vibe-trading) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Nov 2026</sub>

**Finance research agent for backtests, paper trading and broker-linked execution.**

Vibe-Trading turns plain-English finance questions into research reports, backtests and paper portfolios, with a Python/FastAPI backend, React web UI and CLI. It loads bars from 28 market-data sources with per-market fallback, benchmarks alphas from several libraries, and can connect supported brokers for live trades within a user-set mandate. The same workflows are exposed as Agent and MCP tools.

- **+** 28 market-data sources with per-market fallback chains (Tencent, Yahoo, OKX, Binance)
- **+** Backtest engines model A-share price limits, crypto funding and futures margin
- **+** Alpha Zoo benchmarks Qlib, Alpha101 and GTJA factors with walk-forward checks
- **+** Versioned research artifacts with revision comparison and JSON/Markdown export
- **−** Many recent fixes are on main only, not in the latest pip release
- **−** Gildata financial features are opt-in and need a separate token
- **−** Global futures need user-supplied local bars
- **−** Backtests refuse codes with no recognised market rule, such as 7203.T

<sub>Docker + Compose · Needs LLM provider API, Optional broker accounts, Optional Gildata token · Models: OpenRouter, Codex OAuth · [Repo](https://github.com/hkuds/vibe-trading) · [📖 Docs ↗](https://vibetrading.wiki/docs/) · [🌐 Site ↗](https://vibetrading.wiki/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vibe-trading/)</sub>

<a name="block-buzz"></a>
### #&#8288;16 [buzz](https://github.com/block/buzz) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Nov 2026</sub>

**Self-hosted team workspace where humans and agents share channels on a Nostr relay.**

Buzz is a Rust Nostr relay (Axum, Postgres, Redis, S3/MinIO) with a Tauri and React desktop app. Messages, workflows, git events and audit entries are all signed events in one log. Agents get their own keys and channel memberships, and connect through buzz-cli or an ACP harness for Goose, Codex and Claude Code.

- **+** Agents are scoped by their own keypair, channel membership and audit trail, like human members
- **+** Production Compose bundle with Postgres, Redis, MinIO and optional Caddy TLS for a single-node relay
- **+** buzz-cli is JSON in, JSON out; ACP harness supports Goose, Codex and Claude Code
- **+** Desktop builds for macOS, Linux and Windows, plus YAML workflows with message, schedule and webhook triggers
- **−** Mobile clients, workflow approval gates and huddle lifecycle events are still being wired up
- **−** Push notifications and cross-relay reputation are not implemented yet
- **−** Self-hosting needs Docker, Postgres, Redis and S3-compatible storage
- **−** Windows build is unsigned and the agent shell tool requires Git Bash

<sub>no GPU · Docker + Compose · Needs Postgres, Redis, S3/MinIO, Docker · Models: Goose, Codex, Claude Code · port 3000 · [Repo](https://github.com/block/buzz) · [📖 Docs ↗](https://engineering.block.xyz/blog/run-your-own-buzz-relay) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/block-buzz/)</sub>

<a name="budibase"></a>
### #&#8288;17 [budibase](https://github.com/budibase/budibase) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · custom license · Nov 2026</sub>

**Low-code platform for internal apps, automations and AI agents.**

Budibase is a self-hostable operations platform for building internal apps, workflow automations and AI agents that create records, route approvals and notify teams. It connects to databases, AI models and business apps, and exposes a public API so it can serve as a backend. The monorepo is TypeScript, with a Svelte builder, a browser client and a Koa server.

- **+** Agents, internal apps and automations are built in one platform
- **+** Self-host via Docker (ARM image), Compose, Kubernetes, DigitalOcean or Portainer
- **+** Public API with interactive docs lets it act as a backend
- **+** Client and component libraries are MPL, so built apps can use any license
- **−** Mixed licensing: GPL v3 core, MPL client, paid features under Business Source License
- **−** Agent features are described in general terms, with no concrete capability list
- **−** Cloud hosting is promoted alongside self-hosting

<sub>[Repo](https://github.com/budibase/budibase) · [📖 Docs ↗](https://docs.budibase.com/docs) · [🌐 Site ↗](https://www.budibase.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/budibase/)</sub>

<a name="skyvern"></a>
### #&#8288;18 [Skyvern](https://github.com/skyvern-ai/skyvern) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · AGPL-3.0 · Nov 2026</sub>

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

<a name="crm"></a>
### #&#8288;19 [crm](https://github.com/trycompai/crm) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Oct 2026</sub>

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

<a name="trigger-dev"></a>
### #&#8288;20 [trigger.dev](https://github.com/triggerdotdev/trigger.dev) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

**TypeScript platform for durable background tasks and AI agent workflows.**

Trigger.dev is a TypeScript SDK and runtime for writing long-running background tasks in your own codebase and deploying them to a managed cloud or a self-hosted instance. Tasks run without timeouts and get retries, queues, checkpointing, waitpoints for human approval, realtime streaming to frontends, and per-run tracing. Build extensions let tasks use system packages such as Python, FFmpeg and browsers.

- **+** Tasks have no timeouts, with checkpointing and automatic retries for long AI jobs
- **+** Waitpoints pause a run until a human approves, rejects or gives feedback
- **+** Realtime API and React hooks stream run state and LLM output to the frontend
- **+** Self-hostable with Docker Compose or an official Helm chart for Kubernetes
- **−** Code-first and TypeScript/JavaScript only; no visual workflow builder
- **−** Managed cloud is the primary path; self-hosting needs extra setup and services
- **−** Not an agent framework; you bring your own LLM libraries and orchestration

<sub>no GPU · Docker + Compose · [Repo](https://github.com/triggerdotdev/trigger.dev) · [📖 Docs ↗](https://trigger.dev/docs) · [🌐 Site ↗](https://trigger.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trigger-dev/)</sub>

<a name="openmontage"></a>
### #&#8288;21 [openmontage](https://github.com/calesthio/openmontage) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 80k · AGPL-3.0 · Nov 2026</sub>

**Agent-driven video production pipelines run from your AI coding assistant.**

OpenMontage is a set of pipelines, stage skills and tools that let a coding assistant (Claude Code, Cursor, Copilot, Windsurf, Codex) research, script, narrate, source or generate footage, and render a finished video with Remotion or HyperFrames plus FFmpeg. With no API keys it uses Piper TTS and free footage from Archive.org, NASA and Wikimedia Commons. Paid providers are optional.

- **+** Works with zero API keys: Piper TTS, free archival footage, Remotion and FFmpeg rendering
- **+** Many optional providers: fal.ai, Kling, Runway, ElevenLabs, Suno, Google, OpenAI, Pexels
- **+** Backlot local board adds scene-level approval gates and per-asset cost tracking
- **+** Optional local video generation on GPU: Wan 2.x, HunyuanVideo 1.5, LTX2, CogVideo
- **−** Needs an external AI coding assistant to drive it; no standalone prompting UI
- **−** Local setup requires Python 3.10+, Node.js 18+ and FFmpeg
- **−** No Docker or compose files detected
- **−** AGPL-3.0 license and no tagged release

<sub>GPU optional · Needs Python 3.10+, Node.js 18+, FFmpeg, AI coding assistant, Remotion, HyperFrames · Models: Piper TTS, Wan 2.1/2.2, HunyuanVideo 1.5, LTX2, CogVideo 5B · [Repo](https://github.com/calesthio/openmontage) · [🌐 Site ↗](https://openmontage.video) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmontage/)</sub>

<a name="rocketride-server"></a>
### #&#8288;22 [rocketride-server](https://github.com/rocketride-org/rocketride-server) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Nov 2026</sub>

**Visual AI pipeline builder in VS Code with a C++ runtime.**

RocketRide is a pipeline builder and runtime for AI workloads. Pipelines are saved as portable JSON .pipe files, built on a visual canvas in a VS Code extension, and run by a multithreaded C++ engine. It ships 100+ nodes covering 15+ LLM providers, 9 vector databases, OCR, NER and agents, with Python and TypeScript SDKs and an MCP server.

- **+** Pipelines are plain JSON .pipe files, diffable and version-controllable
- **+** 100+ nodes, including 15+ LLM providers and 9 vector databases; nodes are Python-extensible
- **+** Built-in tracing of token usage, LLM calls, latency and call trees
- **+** MIT license with no enterprise edition; Python and TypeScript SDKs plus MCP server
- **−** Visual builder is delivered as an IDE extension (VS Code or Open VSX editors)
- **−** SDK falls back to RocketRide Cloud when run outside the extension's folder
- **−** RAG example needs an LLM key and a vector database such as Qdrant

<sub>Docker + Compose · Needs VS Code or compatible IDE, Docker (optional), Vector database (for RAG), LLM API key (for hosted models) · Models: OpenAI, Anthropic, 15+ LLM providers, local models · port 5565 · [Repo](https://github.com/rocketride-org/rocketride-server) · [📖 Docs ↗](https://docs.rocketride.org/) · [🌐 Site ↗](https://rocketride.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rocketride-server/)</sub>

<a name="agent-zero"></a>
### #&#8288;23 [Agent Zero](https://github.com/agent0ai/agent-zero) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Nov 2026</sub>

**General-purpose AI agent with its own Linux desktop, browser and terminal.**

Agent Zero runs an agent inside a Docker-hosted Linux workspace with a terminal, a built-in browser and a desktop (LibreOffice, Blender). It is operated from a Web UI where you can watch or take over the desktop, and it can reach files on your machine through a Launcher or the A0 CLI connector. Projects, skills, agent profiles, plugins, MCP and A2A extend it.

- **+** Real Linux desktop and browser in the UI, with user takeover and page annotation
- **+** Projects isolate files, memory, secrets and model presets per job
- **+** Extensible via plugins, MCP, A2A and skills; prompts and tools are readable files
- **+** Time Travel snapshots of /a0/usr allow rolling back workspace changes
- **−** Needs a provider API key, AI account or local model server before first reply
- **−** Host file access means granting the agent permission to edit files and run commands
- **−** Docker required; installers are curl-pipe-to-shell scripts or a launcher app
- **−** Detected license is NOASSERTION, while the README states MIT

<sub>Docker + Compose · Needs Docker, LLM provider API key, AI account or local model server · Models: Cloud providers, ChatGPT/Codex account, Local model servers, Provider plugins (e.g. OpenCode Go) · port 5080 · [Repo](https://github.com/agent0ai/agent-zero) · [📖 Docs ↗](https://www.agent-zero.ai/p/docs/installation/#installation) · [🌐 Site ↗](https://agent-zero.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-zero/)</sub>

<a name="yuxi"></a>
### #&#8288;24 [yuxi](https://github.com/xerrors/yuxi) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · MIT · Nov 2026</sub>

**Multi-tenant agent platform with Milvus RAG, Neo4j graphs and LangGraph agents.**

Yuxi is a self-hosted, multi-user platform that combines document RAG (Milvus, MinerU/PaddleX/RapidOCR parsing, rerank), a Neo4j knowledge graph, and LangGraph-based agents with SubAgents, Skills, MCP and sandboxed file tools. Admins manage users, departments, model credentials and sharing scopes. The stack is Vue, FastAPI and PostgreSQL, started with Docker Compose.

- **+** Per-user, department and tenant permissions over knowledge bases, agents, Skills and models
- **+** Built-in RAG evaluation and retrieval testing with embedding and rerank scores
- **+** Supports MCP, Skills, SubAgents and sandboxed file output with in-browser preview
- **+** Connects OpenAI, Anthropic, DeepSeek, Qwen and OpenAI-compatible endpoints such as vLLM
- **−** Heavy stack: Milvus, Neo4j, PostgreSQL, MinerU and PaddleOCR all run in Compose
- **−** README is mainly Chinese; English version is a separate file
- **−** Upgrading from v0.7.1 or v0.7.2 needs downtime, backup and migration

<sub>Docker + Compose · Needs Docker Compose, Milvus, Neo4j, PostgreSQL, MinerU, PaddleOCR, LangGraph, LLM API · Models: OpenAI, Anthropic, DeepSeek, Qwen, SiliconFlow · port 5173 · [Repo](https://github.com/xerrors/yuxi) · [📖 Docs ↗](https://xerrors.github.io/Yuxi/intro/quick-start) · [🌐 Site ↗](https://xerrors.github.io/Yuxi/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yuxi/)</sub>

<a name="ai-hedge-fund"></a>
### #&#8288;25 [ai-hedge-fund](https://github.com/virattt/ai-hedge-fund) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 65k · MIT · Nov 2026</sub>

**Terminal app that paper-trades and backtests LLM-driven investor agents on stocks.**

A Python terminal app (installed as `aihf`) where LLM investor agents make trading decisions for funds you define with strategies, capital, cadence and tickers. It supports paper trading over real market days with a hash-chained ledger and an approval step, plus backtesting against a benchmark. It never places real trades and is stated to be for educational use only.

- **+** Installs with pipx, uv or pip; API keys are prompted for and saved to ~/.hedge-fund/.env
- **+** Paper-trading sessions go into a hash-chained ledger, so NAV is an auditable record
- **+** Approval step shows the exact decision before a paper trade executes; kill switch included
- **+** Backtests replay a fund over history against a benchmark; fund definitions carry no tickers
- **−** Does not execute real trades; no broker integration
- **−** Requires a Financial Datasets API key for prices, fundamentals and earnings
- **−** Needs a hosted model API key; local models are not listed as supported
- **−** Terminal UI only; no web interface or Docker image

<sub>no GPU · Needs Financial Datasets API key, LLM provider API key · Models: Anthropic, OpenAI, DeepSeek, Google, xAI · [Repo](https://github.com/virattt/ai-hedge-fund) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-hedge-fund/)</sub>

<a name="ax"></a>
### #&#8288;26 [ax](https://github.com/google/ax) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Nov 2026</sub>

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

<a name="openresearch"></a>
### #&#8288;27 [openresearch](https://github.com/alphaxiv/openresearch) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · MIT · Nov 2026</sub>

**Desktop app and CLI that runs research agents with experiment tracking.**

OpenResearch is a desktop app and `orx` CLI that wraps coding agents (Claude Code, Codex, OpenCode, Cursor, Google Antigravity) in a research workflow. Agents search alphaXiv, bioRxiv and PubMed, then run experiments locally or on SSH, Slurm, Kubernetes, Modal, Tinker, Ray or Hugging Face Jobs. Every experiment, with its logs, code and artifacts, is stored in a local SQL database that agents can consult later.

- **+** Works with several coding agents, plus local models via OpenCode with LM Studio, oMLX or Ollama
- **+** Many compute backends: local, SSH, Slurm, Kubernetes, Modal, Ray, Hugging Face Jobs
- **+** Experiment logs, code and artifacts stay in a local SQL database on your machine
- **+** Literature search built in for alphaXiv, bioRxiv and PubMed
- **−** Official builds send opt-out analytics and agent feedback; disable in Settings or `orx telemetry off`
- **−** Windows build is beta and requires Git for Windows
- **−** CLI installed by install.sh is unsigned and may be blocked on managed Macs
- **−** Managed compute and email updates need an openresearch.sh account

<sub>Needs Git for Windows (Windows), a coding agent such as Claude Code, Codex or OpenCode · Models: Claude Code, Codex, OpenCode, Cursor, Google Antigravity · port 4791 · [Repo](https://github.com/alphaxiv/openresearch) · [📖 Docs ↗](https://openresearch.sh/docs) · [🌐 Site ↗](https://openresearch.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openresearch/)</sub>

<a name="hive"></a>
### #&#8288;28 [hive](https://github.com/aden-hive/hive) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="reef"></a>
### #&#8288;29 [reef](https://github.com/human-agent-society/reef) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · Apache-2.0 · Nov 2026</sub>

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

<a name="opencreator"></a>
### #&#8288;30 [opencreator](https://github.com/krillinai/opencreator) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

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

<a name="openbot"></a>
### #&#8288;31 [openbot](https://github.com/copilotkit/openbot) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Nov 2026</sub>

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

<sub>no GPU · Compose · Needs Docker, PostgreSQL, Bun 1.3+, CopilotKit Intelligence, LLM API key · Models: OpenAI, Anthropic, Google, any AG-UI agent endpoint · port 3010 · [Repo](https://github.com/copilotkit/openbot) · [🌐 Site ↗](https://copilotkit.ai/openbot) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openbot/)</sub>

<a name="raven"></a>
### #&#8288;32 [raven](https://github.com/evermind-ai/raven) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Nov 2026</sub>

**Host agent that orchestrates built-in and third-party agents in shared workflows.**

Raven is a Python host agent that generates task DAGs and delegates work to four built-in agents (Research, Code, Design, Oncall) or to third-party agents connected over ACP, CLI or OpenAI-compatible APIs. It uses EverOS for memory across sessions, and an experimental Curator rewrites agent strategy modules. A trajectory view shows multi-agent runs as a timeline.

- **+** Presets for 13 third-party agents (Claude Code, Codex, OpenCode, Hermes and others)
- **+** Four built-in agents: research, coding, visual design, unattended long-running workflows
- **+** Trajectory view shows every agent, turn and step of a run on one timeline
- **+** Agent loop split into memory, planning, capability and action modules
- **−** Curator self-improvement is experimental and ships with the repo, not the package
- **−** Benchmark claims are self-reported and shown only as images
- **−** Memory relies on the separate EverOS project
- **−** Install is a curl-pipe-to-bash script; hardware needs are not listed

<sub>Docker + Compose · Needs EverOS · Models: OpenAI-compatible APIs, ACP agents, CLI agents · [Repo](https://github.com/evermind-ai/raven) · [📖 Docs ↗](https://evermind-ai.github.io/Raven/) · [🌐 Site ↗](https://raven.evermind.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/raven/)</sub>

<a name="astron-agent"></a>
### #&#8288;33 [astron-agent](https://github.com/iflytek/astron-agent) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="open-duet"></a>
### #&#8288;34 [open-duet](https://github.com/anil-matcha/open-duet) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Nov 2026</sub>

**Workspace for named AI agents with teams, memory, and scheduled routines.**

Open Duet is a desktop and self-hosted workspace where you create named agents, each with instructions, a workspace folder, memory and approval settings. A lead agent can delegate to specialists, and routines run prompts on a schedule, by webhook or on demand. It ships no model; you connect Claude Code, Codex CLI, Gemini CLI, Cursor, ACP agents, OpenRouter or an OpenAI-compatible API such as Ollama.

- **+** Per-agent approval modes: Ask first, Accept edits, Plan only, with reviewable tool activity
- **+** Works with CLI engines, OpenRouter and OpenAI-compatible local servers like Ollama and LM Studio
- **+** Routines trigger by schedule, webhook or manual run; none approve actions automatically
- **+** Editable agent memory and searchable conversation history
- **−** Team lead agents currently must use Claude
- **−** Server mode is experimental and single-owner, not multi-user
- **−** Desktop runs from a source checkout; installers are unsigned and do not auto-update
- **−** No built-in integrations catalog such as Gmail, Slack or Notion

<sub>no GPU · Docker + Compose · Needs Node.js 22+, uv, Docker (optional, for agent computers), An engine: CLI agent or API provider · Models: Claude Code, Codex CLI, Gemini CLI, Cursor, ACP agents · [Repo](https://github.com/anil-matcha/open-duet) · [▶️ Demo ↗](https://youtu.be/MzgrNQXgVX4) · [📖 Docs ↗](https://github.com/Anil-matcha/open-duet/blob/main/docs/SETUP.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-duet/)</sub>

<a name="openalice"></a>
### #&#8288;35 [openalice](https://github.com/traderalice/openalice) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (45) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · AGPL-3.0 · Nov 2026</sub>

**Local workspace that connects coding agents to market data and brokers.**

OpenAlice is a desktop and CLI app that lets agents such as Claude Code, Codex, OpenCode and Pi use market data, fundamentals and news tools inside Git-backed research Workspaces. It adds scheduled recurring tasks (Issues), an Inbox for reports, and a Unified Trading Account layer where agents stage trades that the user approves. State is stored under ~/.openalice.

- **+** Reuses existing agent CLIs (Claude Code, Codex, OpenCode, Pi) instead of a custom agent loop
- **+** Workspaces are plain directories and Git repos you can inspect and back up
- **+** Scheduled Issues rerun research using the Workspace's agent and context
- **+** Trade proposals are staged and need human approval before execution
- **−** Trading execution is marked beta; README advises simulator or paper accounts first
- **−** Source installs require a host agent CLI plus model credentials or login
- **−** Available market data depends on the providers you configure
- **−** Desktop builds listed only for macOS and Windows; no Docker image detected

<sub>no GPU · Needs Host agent CLI (Claude Code, Codex, OpenCode, Pi), Model credentials or login, Market data providers, Broker account (optional), pnpm (source install) · Models: Via host agents: Claude Code, Codex, OpenCode, Pi, Oh My Pi · [Repo](https://github.com/traderalice/openalice) · [📖 Docs ↗](https://openalice.ai/docs) · [🌐 Site ↗](https://openalice.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openalice/)</sub>

<a name="trueforge"></a>
### #&#8288;36 [trueforge](https://github.com/truefoundry/trueforge) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Nov 2026</sub>

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

<a name="openscience"></a>
### #&#8288;37 [openscience](https://github.com/synthetic-sciences/openscience) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · Apache-2.0 · Nov 2026</sub>

**Research agent that reads papers, runs code and experiments, and logs every step.**

OpenScience is a research agent with a workbench around it, shipped as an Electron desktop app, a browser workspace and a CLI. It plans a task, searches literature and databases such as PubMed, arXiv, ChEMBL and UniProt, runs code in shell, Python and R kernels, and returns results with a full trace. Compute can be local, Modal, SSH hosts, or Slurm and PBS clusters, with approval before jobs run.

- **+** Full trace of searches, code runs and file writes for each turn
- **+** Hundreds of bundled science skills plus connectors to PubMed, arXiv, ChEMBL, UniProt
- **+** Remote compute on Modal, SSH, Slurm or PBS, approved before jobs run
- **+** Works with own API keys, local models via Ollama or LM Studio, or Ace
- **−** First-run setup asks you to sign in to an OpenScience account
- **−** Skills are mostly third-party; a skill does not guarantee its tools are installed
- **−** NVIDIA BioNeMo adapters are experimental and need your own NVIDIA key
- **−** Published benchmarks use GPT-6 models, not open-weight ones

<sub>GPU optional · Needs Node/npm (CLI install), Bun (build from source), Modal, SSH or Slurm/PBS (optional remote compute) · Models: Provider API keys, Ollama, LM Studio, OpenAI-compatible local endpoints, OpenRouter · [Repo](https://github.com/synthetic-sciences/openscience) · [📖 Docs ↗](https://openscience.sh/docs) · [🌐 Site ↗](https://openscience.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openscience/)</sub>

<a name="esp32-iphone-agent"></a>
### #&#8288;38 [esp32-iphone-agent](https://github.com/onehumanbeing/esp32-iphone-agent) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · MIT · Nov 2026</sub>

**AI agent that taps, swipes and types on an iPhone via an ESP32 board.**

An ESP32-S3 board plugged into an iPhone receives the screen over AirPlay and acts as a USB HID mouse and keyboard. A SwiftUI app on the same phone sends screenshots to any OpenAI-compatible vision model and runs planner and actor steps through AssistiveTouch. It also ships an MCP server (npx esp32agent mcp) so coding agents can drive the phone.

- **+** Needs no computer at run time: only the phone, a ~$7 board and a model endpoint
- **+** Works with any OpenAI-compatible vision endpoint, including vLLM, llama.cpp and Ollama
- **+** Every run is stored on the phone with step-by-step replay and trace export
- **+** Includes an MCP server and Claude Code plugin for driving the iPhone from coding agents
- **−** Requires specific hardware: an ESP32-S3 with native USB and PSRAM
- **−** Mirrors at 480x1040, up to 5 fps; each step takes a few seconds
- **−** Cannot see passcode, Apple Pay or DRM screens; landscape apps unsupported
- **−** Phone Wi-Fi is taken by the board hotspot, so the model is reached over cellular

<sub>no GPU · Needs ESP32-S3 board (Seeed XIAO ESP32S3, 8 MB PSRAM), iPhone with iOS 18+ and cellular data, OpenAI-compatible vision model endpoint, arduino-cli and Xcode to build from source · Models: OpenAI-compatible vision APIs, vLLM, SGLang, llama.cpp, Ollama · [Repo](https://github.com/onehumanbeing/esp32-iphone-agent) · [▶️ Demo ↗](https://www.youtube.com/watch?v=Ly4im-P4jYg) · [📖 Docs ↗](https://handsy.tech/docs) · [🌐 Site ↗](https://handsy.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/esp32-iphone-agent/)</sub>

<a name="clawith"></a>
### #&#8288;39 [clawith](https://github.com/dataelement/clawith) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · Apache-2.0 · Aug 2026</sub>

**Multi-agent platform with persistent agent identity, memory and org-chart awareness.**

Clawith is a FastAPI and React web app where each agent keeps a soul.md personality file, a memory.md file and a private sandboxed workspace. Agents run on six trigger types (cron, once, interval, poll, on_message, webhook), message each other and humans, and post to a shared feed. It adds multi-tenant RBAC, usage quotas, approval flows and Slack, Discord or Feishu/Lark channels. All LLM inference goes to external APIs.

- **+** Six trigger types, including webhook and HTTP poll, that agents can create and cancel themselves
- **+** Multi-tenant RBAC, usage quotas, approval workflows and audit logs built in
- **+** Per-agent Slack, Discord or Feishu/Lark bot identity
- **+** Agents can install MCP tools from Smithery and ModelScope at runtime
- **−** No local model inference; requires external LLM API endpoints
- **−** Needs PostgreSQL (SQLite for trials) and Redis; heavier setup than a single binary
- **−** Public demo is a shared environment, stability not guaranteed
- **−** Runtime tool installation by agents widens the attack surface; Docker socket access must be restricted

<sub>RAM ≥ 4 GB · no GPU · Compose · Needs PostgreSQL 15+ or SQLite, Redis, Docker, External LLM API (OpenAI, Anthropic, etc.), Python 3.12+, Node.js 20+ · Models: OpenAI, Anthropic, External LLM APIs · port 3008 · [Repo](https://github.com/dataelement/clawith) · [▶️ Demo ↗](https://try.clawith.ai) · [🌐 Site ↗](https://www.clawith.ai/blog/clawith-technical-whitepaper) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clawith/)</sub>

<a name="mindshub"></a>
### #&#8288;40 [mindshub](https://github.com/mindsdb/mindshub) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (89) · Freshness: active (98) · Maintenance: patchy (37) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

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

<a name="flyte"></a>
### #&#8288;41 [flyte](https://github.com/flyteorg/flyte) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (50) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · Apache-2.0 · Nov 2026</sub>

**Python-native orchestrator for ML pipelines, model serving and agents.**

Flyte 2 lets you define tasks and workflows in plain Python with async/await, then run them locally, through the flyte CLI, or on a remote backend. The same SDK deploys model-serving apps such as FastAPI endpoints. The open-source backend in this repository is not released yet; a production backend is offered by Union.ai.

- **+** Workflows are plain Python with asyncio.gather fan-out, no DSL or YAML
- **+** Same code runs via python script or the flyte CLI
- **+** Local Devbox, Codespaces and an optional TUI for development
- **+** LF AI & Data Graduated project under Apache-2.0
- **−** Open-source Flyte 2 backend is listed as coming soon
- **−** Production-grade backend currently comes from Union.ai, a commercial service
- **−** Flyte 1 lives on the master branch, which splits code and docs
- **−** SDK code lives in a separate flyte-sdk repository

<sub>Docker · Needs Python, Kubernetes (planned OSS backend) · [Repo](https://github.com/flyteorg/flyte) · [📖 Docs ↗](https://www.union.ai/docs/v2/flyte/user-guide/get-started/run-modes/running-devbox/) · [🌐 Site ↗](https://www.union.ai/blog-post/flyte-2-is-generally-available-the-durable-open-source-ai-runtime) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flyte/)</sub>

<a name="zenml"></a>
### #&#8288;42 [zenml](https://github.com/zenml-io/zenml) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Nov 2026</sub>

**Python MLOps framework that runs ML and agent pipelines on any backend.**

ZenML lets you wrap Python code in steps and pipelines, then run them on configurable infrastructure stacks such as Kubernetes, Kubeflow, SageMaker or Vertex. It containerizes and tracks code and records runs with metrics, logs and metadata. It integrates with MLflow, Weights & Biases, Langfuse and LangGraph, and uses a client-server design with a web dashboard.

- **+** Wraps existing code in a @step; no rewrite of scikit-learn, PyTorch or LangGraph code
- **+** Same pipeline runs across stacks like Kubernetes, Kubeflow, SageMaker and Vertex
- **+** Integrates with MLflow, Weights & Biases and Langfuse instead of replacing them
- **+** Covers classical ML, LLM workflows and agents in one framework
- **−** Production use needs a separate server plus stack setup
- **−** Replay-based agent evals live in the separate Kitaru project
- **−** Aimed at team MLOps; heavy for single-script experiments
- **−** ZenML Pro is a separate hosted offering; the feature split is not detailed

<sub>GPU optional · Docker + Compose · Needs Python, Kubernetes (optional), MLflow (optional), Object storage (optional) · Models: scikit-learn, PyTorch, LangGraph, LlamaIndex, LiteLLM · [Repo](https://github.com/zenml-io/zenml) · [▶️ Demo ↗](https://zenml.io/demo-video) · [📖 Docs ↗](https://docs.zenml.io/) · [🌐 Site ↗](https://zenml.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/zenml/)</sub>

<a name="skillhub"></a>
### #&#8288;43 [skillhub](https://github.com/iflytek/skillhub) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · Apache-2.0 · Nov 2026</sub>

**Self-hosted registry for publishing and installing versioned agent skill packages.**

SkillHub is a private registry for agent skill packages, with a Java 21 backend and a React 19 web UI. Teams publish semver-versioned skills into team or global namespaces, review them, and install them through an npm-distributed CLI or the REST API. Storage is local filesystem or S3/MinIO, and it deploys via Docker Compose, Kubernetes manifests or a Helm chart.

- **+** Namespaces with Owner/Admin/Member roles, review flow and audit-logged governance actions
- **+** Semantic versioning with custom tags and automatic latest tracking
- **+** CLI and REST API, plus a compatibility layer for ClawHub-style clients
- **+** Compose, Kubernetes manifests and Helm chart; S3/MinIO storage for production
- **−** Needs PostgreSQL and Redis alongside the Java backend and web frontend
- **−** Release template enables a default bootstrap admin password that must be changed
- **−** Prometheus monitoring example is not ready to scrape without extra configuration
- **−** ClawHub protocol compatibility is still expanding; native APIs are the primary path

<sub>no GPU · Compose · Needs PostgreSQL, Redis, S3/MinIO (optional), Docker Compose · port 3000 · [Repo](https://github.com/iflytek/skillhub) · [📖 Docs ↗](https://iflytek.github.io/skillhub/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skillhub/)</sub>

<a name="yao"></a>
### #&#8288;44 [yao](https://github.com/yaoapp/yao) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · custom license · Nov 2026</sub>

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

<a name="openpencil"></a>
### #&#8288;45 [openpencil](https://github.com/zseven-w/openpencil) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (44) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · MIT · Nov 2026</sub>

**Vector design editor that generates UI on canvas from prompts.**

OpenPencil is a Rust vector design editor that runs as a native desktop app or a headless web host. It generates and edits UI layouts from prompts, splitting pages across parallel agents, and saves designs as JSON `.op` files. It exports to React + Tailwind, HTML + CSS, Vue, Svelte, Flutter, SwiftUI and more, and ships an MCP server and an `op` CLI so external coding agents can edit designs.

- **+** `.op` files are plain JSON, so designs diff and version cleanly in Git
- **+** Built-in MCP server over stdio or local HTTP, no Node.js required
- **+** Code export to React, Vue, Svelte, Flutter, SwiftUI, Compose and React Native
- **+** Works with 9+ API providers plus Claude Code, Codex, OpenCode and Copilot CLIs
- **−** Web host and Docker image support only built-in API-key agents, not CLI agents
- **−** Building from source needs three git submodules (jian, casement, agent)
- **−** No tagged release on the repository; Docker images are versioned separately
- **−** Output quality varies by model; smaller models get simplified prompts

<sub>Docker + Compose · Needs Rust toolchain (build from source), LLM provider API key or agent CLI, Bun and Node.js (web SDK only) · Models: Anthropic, OpenAI, Google Gemini, DeepSeek, Kimi · port 3100 · [Repo](https://github.com/zseven-w/openpencil) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openpencil/)</sub>

<a name="pipelines"></a>
### #&#8288;46 [pipelines](https://github.com/kubeflow/pipelines) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Nov 2026</sub>

**ML pipeline orchestrator with a Python SDK, built on Argo Workflows.**

Kubeflow Pipelines runs reusable, containerized ML workflows on Kubernetes. Pipelines are written with the Python SDK (kfp) and executed through Argo Workflows using the Emissary executor, with experiment management and reusable components. It installs standalone or as part of the Kubeflow Platform; this branch (KFP 3.0) targets Argo Workflows 4.0 and 4.1 with MySQL 8.

- **+** Pipelines defined in Python with the kfp SDK, published on PyPI
- **+** Components and pipelines are reusable across experiments and runs
- **+** Emissary executor is independent of the Kubernetes container runtime
- **+** Installs standalone or as part of the Kubeflow Platform
- **−** Requires a Kubernetes cluster; no single-machine install described
- **−** KFP 3.0 branch drops Argo 3.x; Argo must be upgraded to 4.x first
- **−** Depends on Argo Workflows and MySQL 8, adding operational overhead
- **−** General ML orchestration; no LLM or agent-specific features in the README

<sub>Needs Kubernetes, Argo Workflows 4.0/4.1, MySQL 8 · [Repo](https://github.com/kubeflow/pipelines) · [📖 Docs ↗](https://www.kubeflow.org/docs/components/pipelines/overview/) · [🌐 Site ↗](https://www.kubeflow.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pipelines/)</sub>

<a name="tracecat"></a>
### #&#8288;47 [tracecat](https://github.com/tracecathq/tracecat) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · AGPL-3.0 · Nov 2026</sub>

**Security automation platform with workflows, case management and AI agents.**

Tracecat is a security automation platform that combines a workflow builder running on Temporal, case management, structured tables, and agents with tools, subagents and skills. It ships 100+ connectors and 50+ hosted MCP servers for security tools, and can act as an MCP client. The backend is Python/FastAPI with PostgreSQL and an S3-compatible object store, and untrusted code runs in nsjail sandboxes.

- **+** Workflows run on Temporal, giving durable execution and resilience
- **+** Includes case management and tables alongside workflows and agents
- **+** SAML/OIDC and exportable audit logs are in the open-source edition
- **+** Can run fully air-gapped; untrusted code runs in nsjail sandboxes
- **−** Multi-tenancy, RBAC/ABAC and human-in-the-loop approvals are Enterprise-only
- **−** Code in packages/tracecat-ee cannot be used in production without a license
- **−** AGPL-3.0 license may be a problem for some commercial use
- **−** Needs Temporal, PostgreSQL and S3-compatible storage, so deployment has many parts

<sub>Docker + Compose · Needs Temporal, PostgreSQL, S3-compatible object store · [Repo](https://github.com/tracecathq/tracecat) · [📖 Docs ↗](https://docs.tracecat.com/self-hosting/air-gapped) · [🌐 Site ↗](https://tracecat.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tracecat/)</sub>

<a name="nexent"></a>
### #&#8288;48 [nexent](https://github.com/modelengine-group/nexent) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (37) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Nov 2026</sub>

**Generates agents from plain-language prompts, with memory, skills and MCP tools.**

Nexent generates executable agents from a plain-language description instead of a visual flow builder. It bundles two-tier memory, progressively loaded skills, MCP tools, a knowledge base covering 20+ document formats, and A2A agent collaboration. Multi-tenancy with RBAC, agent versioning and a marketplace are included.

- **+** Agents generated from a text prompt, no drag-and-drop orchestration needed
- **+** Multi-tenancy, RBAC and agent version history with rollback
- **+** Supports MCP tools and the A2A agent-to-agent protocol
- **+** Offline image packages and Helm-based Kubernetes deployment documented
- **−** Heavy stack: Elasticsearch, PostgreSQL, Redis and MinIO; 8 GiB RAM minimum on Docker
- **−** Prompt-only agent creation gives less explicit control than a visual builder
- **−** Needs external model providers or endpoints; no bundled model serving documented
- **−** Kubernetes minimum is 16 GiB RAM and 100 GiB disk

<sub>RAM ≥ 8 GB · Docker + Compose · Needs Docker 24+, Docker Compose v2+, Elasticsearch, PostgreSQL, Redis, MinIO, Kubernetes 1.24+ and Helm 3+ (optional) · Models: OpenAI-compatible providers, LLM, Embedding, VLM, STT · [Repo](https://github.com/modelengine-group/nexent) · [📖 Docs ↗](https://modelengine-group.github.io/nexent) · [🌐 Site ↗](https://nexent.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nexent/)</sub>

<a name="kagent"></a>
### #&#8288;49 [kagent](https://github.com/kagent-dev/kagent) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Nov 2026</sub>

**Kubernetes-native framework for defining and running AI agents as custom resources.**

kagent defines agents, agent templates, model configs and remote MCP servers as Kubernetes custom resources. A controller reconciles them and runs agents on Go or Python ADKs, Codex, Claude or custom runtimes, with sessions and task history stored in PostgreSQL. It ships a web UI, a CLI, and an MCP server with tools for Kubernetes, Istio, Helm, Argo, Prometheus, Grafana and Cilium.

- **+** Agents, tools and model configs are YAML resources, fitting kubectl and GitOps workflows
- **+** Bundled MCP tools for Kubernetes, Istio, Helm, Argo, Prometheus, Grafana and Cilium
- **+** Sessions persist in PostgreSQL, with suspend, resume, checkpoint and fork
- **+** OpenTelemetry tracing for agent, model and tool execution
- **−** Requires a Kubernetes cluster and PostgreSQL; no standalone mode described
- **−** Model provider support depends on the chosen harness
- **−** README says the project is in active development
- **−** No hosted demo linked in the README

<sub>Needs Kubernetes, PostgreSQL · Models: OpenAI, Azure OpenAI, Anthropic, Google Vertex AI, Ollama · [Repo](https://github.com/kagent-dev/kagent) · [📖 Docs ↗](https://kagent.dev/docs/kagent/1.x/setup/installation/) · [🌐 Site ↗](https://kagent.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kagent/)</sub>

<a name="goclaw"></a>
### #&#8288;50 [goclaw](https://github.com/nextlevelbuilder/goclaw) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · custom license · Nov 2026</sub>

**Multi-tenant agent gateway in Go with team delegation, memory and chat channels.**

GoClaw is a Go gateway that runs multiple agents, each with its own identity, tools and LLM provider, and connects them to Telegram, Discord, Slack, Zalo, Feishu/Lark and WhatsApp. It stores per-user workspaces, sessions and encrypted API keys in PostgreSQL with pgvector, and includes agent teams with task boards, a three-tier memory and a web dashboard. A lighter desktop edition uses SQLite with a smaller feature set.

- **+** Per-user workspaces, RBAC and AES-256-GCM encrypted API keys for multi-tenant hosting
- **+** 20+ providers including Anthropic, OpenAI, Gemini, DeepSeek and any OpenAI-compatible endpoint
- **+** Static ~25 MB Go binary; built-in tracing with optional OpenTelemetry export
- **+** Webhook API with bearer or HMAC auth to trigger agents from external systems
- **−** CC BY-NC 4.0 license forbids commercial use
- **−** Server edition requires PostgreSQL 18 with pgvector
- **−** Desktop Lite edition caps at 5 agents and has no channels or RBAC
- **−** Default branch is dev; stable code is on main, so cloning needs -b main

<sub>no GPU · Docker + Compose · Needs PostgreSQL 18 with pgvector, Docker (optional), Headless Chrome (optional), Redis (optional) · Models: Anthropic, OpenAI, OpenRouter, Groq, DeepSeek · port 18790 · [Repo](https://github.com/nextlevelbuilder/goclaw) · [📖 Docs ↗](https://docs.goclaw.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/goclaw/)</sub>

<a name="ufo"></a>
### #&#8288;51 [ufo](https://github.com/microsoft/ufo) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

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

<a name="inkos"></a>
### #&#8288;52 [inkos](https://github.com/narcooo/inkos) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · AGPL-3.0 · Oct 2026</sub>

**AI agent for writing novels, short stories, scripts and interactive fiction.**

InkOS is a Node.js CLI, TUI and local web Studio that drives LLMs through planning, writing, auditing and revising chapters of novels, short stories, scripts and branching interactive worlds. It keeps per-book state (characters, foreshadowing hooks, summaries) as schema-validated JSON with a SQLite FTS5 index, and commits chapter text and state atomically. Models connect through OpenAI Chat, OpenAI Responses or Anthropic Messages endpoints.

- **+** Per-book state validated with Zod; chapter text and state are committed atomically
- **+** Models can be routed per agent role, such as writer and auditor
- **+** Same harness behind Studio, TUI, CLI and a JSON interact mode for external agents
- **+** Standard SKILL.md skills; 19 built in, overridable by a project skill with the same ID
- **−** README is mainly in Chinese; English writing is enabled with --lang en
- **−** Needs an external LLM API or a local endpoint such as Ollama or LM Studio
- **−** AGPL-3.0 license restricts use in closed network services
- **−** README describes the 2.0 branch as a development version verified with local builds

<sub>no GPU · Needs Node.js 22.16+, LLM API provider (OpenAI-compatible or Anthropic) · Models: OpenAI Chat Completions, OpenAI Responses, Anthropic Messages, Gemini, Moonshot · [Repo](https://github.com/narcooo/inkos) · [▶️ Demo ↗](https://huohuaapi.com/apps) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/inkos/)</sub>

<a name="kiln"></a>
### #&#8288;53 [kiln](https://github.com/kiln-ai/kiln) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (32) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · custom license · Nov 2026</sub>

**Desktop app and Python library for AI task evals, optimization and fine-tuning.**

Kiln is a desktop app for Mac, Windows and Linux plus an MIT-licensed Python library (kiln-ai). One task and dataset flow through evals, prompt optimization, RAG, synthetic data, subagents and fine-tuning on Fireworks, Together and Vertex. It runs locally with your own API keys or offline with Ollama, and syncs team projects through Git.

- **+** Evals, RAG, synthetic data and fine-tuning share one dataset in a single tool
- **+** Non-engineers rate outputs in the app; engineers load the same projects via pip
- **+** Local-first: bring your own keys or run offline with Ollama; datasets are open JSON
- **+** Team sync uses your existing Git infrastructure
- **−** Desktop app is source-available (fair-code); only the library and REST server are MIT
- **−** AI Assistant, Auto-Optimize and Eval Builder require the paid Kiln Pro service
- **−** Fine-tuning runs on hosted providers (Fireworks, Together, Vertex), not local GPUs
- **−** No Docker or compose deployment; it is an installed desktop app

<sub>GPU optional · Needs Ollama (optional, for offline use), Git (for team sync) · Models: OpenAI, Anthropic, Gemini, Bedrock, Ollama · [Repo](https://github.com/kiln-ai/kiln) · [▶️ Demo ↗](https://kiln.tech#demo) · [📖 Docs ↗](https://docs.kiln.tech) · [🌐 Site ↗](https://kiln.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kiln/)</sub>

<a name="pilotdeck"></a>
### #&#8288;54 [pilotdeck](https://github.com/openbmb/pilotdeck) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (30) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · AGPL-3.0 · Nov 2026</sub>

**Workspace-based agent platform with editable memory, model routing and background tasks.**

PilotDeck is a Node.js/TypeScript agent system that isolates files, memory and skills per WorkSpace, with a Web UI, CLI and IM front-ends. It routes simpler sub-tasks to cheaper models, exposes stored memory entries for editing and rollback, and can run tasks in the background and write results to local files. Providers are configured in ~/.pilotdeck/pilotdeck.yaml or through onboarding, and MCP is supported natively.

- **+** Per-WorkSpace isolation of files, memory and skills limits cross-project context bleed
- **+** Memory entries can be viewed, edited, pinned and rolled back after Dream Mode consolidation
- **+** Smart Routing sends sub-tasks to lighter models; README reports $3.15 vs $18.36 on 7 tasks
- **+** Supports OpenAI, Anthropic, Gemini, DeepSeek, Qwen, Kimi, MiniMax and local Ollama
- **−** AGPL-3.0 license constrains use in hosted or proprietary products
- **−** Requires Node.js 22.13+ but below 23; native modules can need build tools on Windows
- **−** Benchmarks and cost figures are the authors' own; PilotDeck trails Claude Code on GLM-5.3
- **−** Install is a curl-to-bash script that clones and builds the repo locally

<sub>no GPU · Docker + Compose · Needs Node.js 22.13+ (<23), pnpm via corepack, Model provider API key or local Ollama · Models: OpenAI-compatible, Anthropic, Google Gemini, DeepSeek, Qwen · port 3001 · [Repo](https://github.com/openbmb/pilotdeck) · [▶️ Demo ↗](https://pilotdeck.openbmb.cn/pilotdeck.github.io/demo/p/pilotdeck-demo) · [📖 Docs ↗](https://pilotdeck.openbmb.cn/pilotdeck.github.io/docs/en/introduction) · [🌐 Site ↗](https://pilotdeck.openbmb.cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pilotdeck/)</sub>

<a name="evoscientist"></a>
### #&#8288;55 [evoscientist](https://github.com/evoscientist/evoscientist) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (30) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · Apache-2.0 · Nov 2026</sub>

**Multi-agent research assistant with persistent memory, CLI, WebUI and chat channels.**

EvoScientist is a Python research agent built on LangChain's DeepAgents. It runs six sub-agents (plan, research, code, debug, analyze, write) through an intake-to-verify workflow, and distills memory each turn into a knowledge graph that persists across sessions. It is driven from a CLI/TUI, a WebUI, a Windows desktop app, or chat channels such as Telegram and Slack.

- **+** Six specialised sub-agents with a defined plan, execute, evaluate, write and verify flow
- **+** Memory is distilled each turn and AutoSkills proposes reusable skills for review
- **+** One agent session reachable from CLI, WebUI, Telegram, Slack, Feishu and WeChat
- **+** Supports MCP servers, GitHub-installable skills and cron-style scheduled tasks
- **−** Listed providers are hosted APIs; local model support is not documented
- **−** Fast release cadence with behavior changes, e.g. v0.4.0 project .env scope change
- **−** macOS support limited to Apple silicon since v0.4.0
- **−** Desktop app installer is listed only for Windows

<sub>no GPU · Docker + Compose · Needs LLM provider API key (Anthropic, OpenAI, Google, MiniMax, NVIDIA, OpenRouter and others), langgraph dev server, deepagents · Models: Anthropic, OpenAI, Google, MiniMax, NVIDIA · [Repo](https://github.com/evoscientist/evoscientist) · [🌐 Site ↗](https://EvoScientist.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/evoscientist/)</sub>

<a name="mirofish"></a>
### #&#8288;56 [mirofish](https://github.com/666ghj/mirofish) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: widely used (96) · Freshness: active (94) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 85k · AGPL-3.0 · Oct 2026</sub>

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

<a name="bettafish"></a>
### #&#8288;57 [bettafish](https://github.com/666ghj/bettafish) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: widely used (90) · Freshness: active (88) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · GPL-2.0 · Oct 2026</sub>

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

<a name="rd-agent"></a>
### #&#8288;58 [rd-agent](https://github.com/microsoft/rd-agent) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Sep 2026</sub>

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

<a name="cloudflare-os"></a>
### #&#8288;59 [cloudflare-os](https://github.com/cloudflare/cloudflare-os) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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

<a name="solace-agent-mesh"></a>
### #&#8288;60 [solace-agent-mesh](https://github.com/solaceproducts/solace-agent-mesh) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · custom license · Oct 2026</sub>

**Agent build-and-runtime platform coordinating agents over a Solace event broker.**

Solace Agent Mesh hosts agents and their tools and coordinates them over an event broker, with sessions, artifacts, authentication, evaluators and observability. This repository currently ships the Agent Mesh Desktop installer, the `sam` CLI and example use cases; the source code is announced as coming later. Production use requires a Solace commercial license.

- **+** `sam config plan` and `apply` preview and apply manifest-based configuration changes
- **+** Installer verifies SHA-256 checksums plus Apple notarization or Authenticode signatures
- **+** Desktop app bundles the `sam` CLI and installs skills for Claude Code or Codex CLI
- **+** Includes a support-ticket triage example showing classification, drafting and escalation
- **−** Source code is not yet in the repository; only desktop downloads and examples
- **−** Production use requires a Solace commercial license (BUSL-1.1 noted in header)
- **−** Linux desktop support is experimental; `sam ai-assistance` and `sam config` are Early Access
- **−** Repository accepts no issues or pull requests; examples are not production-ready

<sub>Needs Solace event broker, Kubernetes (production) · Models: unknown · [Repo](https://github.com/solaceproducts/solace-agent-mesh) · [▶️ Demo ↗](https://solace.com/agent-mesh-demo/) · [📖 Docs ↗](https://docs.solace.com/Agent-Mesh/Framework/installing/desktop.htm) · [🌐 Site ↗](https://solace.com/products/agent-mesh/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/solace-agent-mesh/)</sub>

<a name="openagents"></a>
### #&#8288;61 [openagents](https://github.com/openagents-org/openagents) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · Apache-2.0 · Nov 2026</sub>

**Shared workspace where people and coding agents collaborate in threads.**

OpenAgents Workspace is a Slack-like hub where agents such as Claude Code, Codex CLI, OpenClaw, Cursor and Kiro share threads, files and a browser with human teammates. A launcher CLI (`agn`) and desktop app install agent runtimes, set API keys, and run a background daemon that connects each agent to a workspace by token. Version 1.1 adds approvals, issues, and per-agent sharing between teammates.

- **+** Connects 25+ existing agent CLIs (Claude Code, Codex, Aider, Goose) to one workspace
- **+** Approval cards let agents ask before deploying, spending, emailing or deleting data
- **+** Agents and devices are private by default and shared per teammate
- **+** Shared browser and files stay attached to the thread that produced them
- **−** Aider, Goose and Cline integrations are Beta; DeepSeek Harness is a preview
- **−** Headless Goose runs in auto mode, so tools execute without prompting
- **−** Self-hosted upgrade to v1.1 changes device ownership and sharing defaults
- **−** No Docker or compose files detected for self-hosting

<sub>no GPU · Needs Node.js, agent runtimes (Claude Code, Codex CLI, etc.), LLM API keys · Models: Anthropic, OpenAI, OpenRouter, Gemini, DeepSeek · [Repo](https://github.com/openagents-org/openagents) · [▶️ Demo ↗](https://openagents.org/api/create-workspace) · [📖 Docs ↗](https://openagents.org/docs) · [🌐 Site ↗](https://openagents.org/workspace) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openagents/)</sub>

<a name="harnessrouter"></a>
### #&#8288;62 [harnessrouter](https://github.com/harnessrouter/harnessrouter) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · Apache-2.0 · Nov 2026</sub>

**One API that runs agent harnesses like Codex and Claude Code as backends.**

HarnessRouter wraps existing agent harnesses (31 listed, including Codex, Claude Code, OpenCode, Aider, OpenHands and goose) behind an OpenAI Responses-compatible API. The harness is chosen per request with metadata.harness_id. It handles persistent sessions, SSE streaming, files, cancellation, idempotency keys and W3C trace propagation. Community Edition runs as one Docker container with a Console, Gateway and Runner, using your own provider keys.

- **+** OpenAI Responses-compatible API; harness switched per request via metadata.harness_id
- **+** 31 harness bases, with a support matrix per provider
- **+** Idempotency-Key retries, W3C traceparent propagation and generated OpenAPI spec
- **+** One container with a persistent /data volume; Console analytics disabled in CE
- **−** Harness is fixed once a setup is saved; switching needs a new setup
- **−** Container must run as root to manage per-session users; --user is unsupported
- **−** Starter Kits are licensed under different terms than Community Edition
- **−** Managed scaling and serverless sandboxes exist only in the hosted Cloud

<sub>no GPU · Docker + Compose · Needs Docker, Model provider API key · Models: OpenAI Responses API, Provider API keys (bring your own) · port 3000 · [Repo](https://github.com/harnessrouter/harnessrouter) · [📖 Docs ↗](https://github.com/HarnessRouter/harnessrouter/blob/main/docs/self-hosting-guide.md) · [🌐 Site ↗](https://harnessrouter.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/harnessrouter/)</sub>

<a name="paperbanana"></a>
### #&#8288;63 [paperbanana](https://github.com/dwzhu-pku/paperbanana) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: known (48) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="cumora"></a>
### #&#8288;64 [cumora](https://github.com/yetone/cumora) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · MIT · Nov 2026</sub>

**Team chat where AI agents and humans share rooms, Kanban and calendar.**

Cumora is a team chat app (Electron, PWA, iOS, Android) in which AI agents are roster members with personas, memory, email addresses and shared Kanban and calendar access. Agents run either in managed per-agent Kubernetes pods using the OpenAI Responses API, or on your own machine via `npx cumora agent computer` with local CLIs such as Claude Code or Codex. The server arbitrates between agents in a room with seen-cursor gating and atomic claims.

- **+** BYOA mode runs agents on your own Claude Code, Codex and other CLIs; server never sees provider keys
- **+** Server-side coordination (stale-reply hold, atomic claims) keeps agents in a room from colliding
- **+** Clients for desktop, web PWA, iOS (TestFlight) and Android, with per-agent real email
- **+** One llm_calls ledger records cost for both cloud and BYOA agents
- **−** Self-hosting needs Postgres and Redis; cloud agent pods also need Kubernetes
- **−** Cloud agents depend on the OpenAI API; OPENAI_API_KEY is required
- **−** Only Claude Code and Codex are sandboxed by default; other BYOA engines need an unsandboxed opt-in
- **−** Android build is not published; iOS is TestFlight beta only

<sub>no GPU · Needs PostgreSQL, Redis, OpenAI API, Kubernetes (cloud agent pods), Resend (email), Cloudflare Workers (email, R2) · Models: OpenAI Responses API, Claude Code, Codex, Grok Build, Cursor Agent · port 5180 · [Repo](https://github.com/yetone/cumora) · [▶️ Demo ↗](https://app.cumora.ai) · [🌐 Site ↗](https://cumora.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cumora/)</sub>

<a name="dsha"></a>
### #&#8288;65 [dsha](https://github.com/dsh-app/dsha) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Nov 2026</sub>

**Android app that runs DeepSeek Harness in a bundled Ubuntu rootfs, no root.**

DSHA is an Android APK (Java, arm64-v8a, Android 11+) that bundles an offline Ubuntu 24.04 rootfs with Node.js 24 and DeepSeek Harness 0.2.2-rc.1, run through proot or optionally proroot. It serves the harness Web UI and adds a local bridge on 127.0.0.1:3090 so the agent can read the screen, tap and run device commands via accessibility, ADB, Shizuku or root. It also ships a PTY terminal, plugin manager, backups and a LAN proxy.

- **+** Offline Ubuntu rootfs in the APK: apt, PTY and native modules work without Termux
- **+** Accessibility-based screen control needs no ADB, Shizuku or root
- **+** Built-in wireless ADB pairing; one command whitelist shared by ADB, Shizuku and root
- **+** Scheduled backups, startup diagnostics and a separate emergency DSH environment
- **−** APK is about 302 MiB because the full Ubuntu environment is bundled
- **−** arm64-v8a only; Android 10 and below are unsupported
- **−** No bash sandbox isolation; default permission mode is danger-full-access
- **−** Virtual screen and privileged execution are experimental and device-dependent

<sub>no GPU · Needs deepseek-harness (@deepseek-ai/dsh), proot / proroot, Shizuku or Stellar (optional) · Models: Provider, model and API key configured in the harness Web UI · [Repo](https://github.com/dsh-app/dsha) · [📖 Docs ↗](https://github.com/DSH-APP/DSHA/blob/main/docs/documentation-index.md) · [🌐 Site ↗](https://dsha.cc) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dsha/)</sub>

<a name="nofx"></a>
### #&#8288;66 [nofx](https://github.com/nofxaios/nofx) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · AGPL-3.0 · Nov 2026</sub>

**AI-assisted crypto trading system with reviewed orders and an autonomous trader mode.**

NOFX is a self-hosted trading system written in Go with a web UI. Frontier generates market, limit, ladder and TWAP entry plans with an LLM, shows them on a chart, and places an order only after you approve it. Autopilot runs a configured model, exchange account and strategy continuously and can place trades unattended.

- **+** Frontier requires explicit approval per trade and shows stop, targets, leverage and margin first
- **+** Supports Binance, Hyperliquid, OKX and Bitget in Frontier; Bybit, Gate, KuCoin, Aster, Lighter in runtime
- **+** One-line installer pulls published Docker images; no Go or Node setup needed
- **+** Uncertain order submissions are checked against the exchange; exchange keys stored encrypted
- **−** Autopilot can place real trades while running; README warns AI strategies can lose money
- **−** Default model and paid-data access go through Claw402, funded with USDC on Base
- **−** Stop-loss entry and protection are not atomic; failed protection needs manual exchange checks
- **−** Installer's production Compose publishes ports on all interfaces; remote use needs your own HTTPS proxy

<sub>no GPU · Docker + Compose · Needs Docker with Compose, Exchange account and API credentials, Claw402 (USDC on Base) for models and paid data, TA-Lib and Node.js 24 for non-Docker builds · Models: Claw402 multi-model access, Models configured in NOFX Config · port 3000 · [Repo](https://github.com/nofxaios/nofx) · [▶️ Demo ↗](https://vergex.trade/explore) · [🌐 Site ↗](https://vergex.trade) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nofx/)</sub>

<a name="autoresearchclaw"></a>
### #&#8288;67 [autoresearchclaw](https://github.com/aiming-lab/autoresearchclaw) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: patchy (33) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Aug 2026</sub>

**23-stage pipeline that turns a research topic into a LaTeX paper.**

Runs a 23-stage pipeline from a topic to a paper. It searches literature via OpenAlex, Semantic Scholar and arXiv, runs sandboxed experiments, applies multi-agent review, and exports NeurIPS/ICML/ICLR LaTeX with BibTeX. It runs fully autonomous or with human approval in co-pilot modes, via CLI, Python API, OpenClaw, or ACP agents such as Claude Code.

- **+** Outputs LaTeX, BibTeX, experiment code and charts in one deliverables folder
- **+** Citation verification checks arXiv, CrossRef, DataCite and an LLM
- **+** Six human-in-the-loop modes, from full-auto to step-by-step
- **+** Can use ACP agent CLIs as the LLM backend without API keys
- **−** No Docker or compose files detected; setup is pip plus an interactive setup command
- **−** Needs an LLM provider or agent CLI; quick start uses an OpenAI key
- **−** Domain executors such as HEP via Magnus cloud add external dependencies

<sub>GPU optional · Needs Python 3.11+, LLM API or ACP agent CLI, OpenAlex / Semantic Scholar / arXiv, LaTeX, Docker (optional) · Models: OpenAI-compatible APIs, ACP agents (Claude Code, Codex CLI, Gemini CLI, Copilot CLI, Kimi CLI, OpenCode) · [Repo](https://github.com/aiming-lab/autoresearchclaw) · [📖 Docs ↗](https://github.com/aiming-lab/AutoResearchClaw/blob/main/docs/integration-guide.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autoresearchclaw/)</sub>

<a name="amagine3d"></a>
### #&#8288;68 [amagine3d](https://github.com/amagine-ai/amagine3d) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Oct 2026</sub>

**LLM agent that writes editable build123d CAD for printable enclosures.**

Amagine3D takes a product description, reference images and key dimensions, then has an LLM agent write build123d Python source for a multipart enclosure around internal components. It checks wall thickness, interference, plate fit and motion clearances on the generated geometry, and exports STEP, STL and 3MF. A React/Vite workbench previews, measures and edits parameters, then rebuilds from source.

- **+** Outputs editable build123d source plus real STEP, STL and 3MF with color regions
- **+** Agent checks measured wall thickness, interference and motion clearance on generated BRep geometry
- **+** Candidates are committed only after checks pass, so the last accepted version is kept
- **+** Each session runs in an isolated workspace with secret-like env variables stripped
- **−** Scope is limited to printable hardware enclosures and related structures
- **−** Requires an OpenAI Responses-compatible API key or gateway; no local model path described
- **−** Visual review needs a vision-capable model, otherwise review stays incomplete
- **−** Tested only in desktop Chrome and Edge; no Docker setup or tagged release

<sub>no GPU · Needs Node.js 22.19.0+, Python 3.10-3.13, OpenAI Responses-compatible API, Tavily (optional) · Models: OpenAI Responses-compatible models (example: openai/gpt-5.5) · port 6160 · [Repo](https://github.com/amagine-ai/amagine3d) · [🌐 Site ↗](https://amagine.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/amagine3d/)</sub>

<a name="cosmo-edge"></a>
### #&#8288;69 [cosmo-edge](https://github.com/cosmo-wander-ai/cosmo-edge) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · Apache-2.0 · Nov 2026</sub>

**C++ engine for video analytics and VLM tasks on Sophon, Rockchip and x86.**

CosmoEdge is a C++17 engine with a browser console for building video analytics pipelines: detection, tracking, zones, alarms, and VLM or GroundingDINO prompt-based checks. Each build targets one backend (Sophon BMRT, Rockchip RKNN, or ONNX Runtime on x86) and needs models converted for that chip. Events go out over REST, WebSocket, MQTT or HTTP webhooks, and an x86 Docker path runs the same UI without edge hardware.

- **+** Targets BM1688, CV186X, RK3576, RV1126B and x86 from one engine and console
- **+** Built-in alarms, ONVIF and GB28181 camera access, MQTT and webhook event delivery
- **+** x86 Docker compose path to try the full UI without edge hardware
- **+** Published v1.1 benchmarks including a 72-hour run on four chips
- **−** Each build supports one backend; models must be converted per target chip
- **−** CV186X and Rockchip v1.2 packages had no device validation in the release run
- **−** Protected models, certified hardware and commercial preset models sit outside the Apache-2.0 code
- **−** macOS preview runs under amd64 emulation, single-video trial only

<sub>GPU optional · Docker + Compose · Needs Docker, Docker Compose, Git · Models: .nn (Sophon BMRT), .rknn (RKNN), RKLLM (RK3576), .onnx (ONNX Runtime), YOLO26 · port 8080 · [Repo](https://github.com/cosmo-wander-ai/cosmo-edge) · [📖 Docs ↗](https://www.cosmowander.ai/docs/) · [🌐 Site ↗](https://www.cosmowander.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cosmo-edge/)</sub>

<a name="chatdev"></a>
### #&#8288;70 [chatdev](https://github.com/openbmb/chatdev) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: widely used (86) · Freshness: active (95) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Oct 2026</sub>

**Visual builder for multi-agent workflows defined in YAML.**

ChatDev 2.0 (DevAll) is a FastAPI backend with a Vue 3 web console for designing and running multi-agent workflows on a drag-and-drop canvas. Workflows are YAML files, runnable from the Launch tab or through a Python SDK (`chatdev` on PyPI). Bundled templates cover data visualization, Blender 3D generation, game development, deep research and teaching videos. The original ChatDev 1.0 software-company simulation lives on the `chatdev1.0` branch.

- **+** Visual canvas plus YAML configs, checkable with `make validate-yamls`
- **+** Ships workflows for data visualization, deep research, game dev, Blender 3D and teaching video
- **+** Python SDK `run_workflow` supports attachments and variable overrides
- **+** Custom Python tools go in `functions/`; human-in-the-loop feedback at launch
- **−** Needs Python 3.12+, Node.js 18+ and uv; backend and frontend run as two services
- **−** 3D workflows also require Blender and blender-mcp installed separately
- **−** Needs an external LLM provider key and base URL; no bundled model runtime
- **−** ChatDev 1.0 software-company mode is legacy, moved to another branch

<sub>no GPU · Docker + Compose · Needs Python 3.12+, Node.js 18+, uv, LLM provider API (API_KEY, BASE_URL), Blender and blender-mcp (3D workflows only), manim (teach video workflow only) · Models: LLM providers via API_KEY and BASE_URL · port 5173 · [Repo](https://github.com/openbmb/chatdev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatdev/)</sub>

<a name="tradingagents-cn"></a>
### #&#8288;71 [tradingagents-cn](https://github.com/hsliuping/tradingagents-cn) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · custom license · Sep 2026</sub>

**Multi-agent LLM research assistant for Chinese A-share stocks.**

Runs LLM analyst agents (market, sector, fundamentals, news, optimistic and cautious researchers) that debate a stock and produce a research report. It also offers natural-language screening over 6000+ A-shares, a web-search assistant with memory, paper trading and study courses. Backend is FastAPI with a Vue 3 frontend, MongoDB and Redis. Research aid only, not investment advice.

- **+** Debate-style analysis with five depth levels and distinct analyst and researcher roles
- **+** Natural-language stock screening and paper trading in one app
- **+** Pulls data from public sources: Tushare, AKShare, BaoStock
- **+** Core agent library, CLI and docs are Apache-2.0
- **−** App and frontend are source-available only: no redistribution or commercial use
- **−** Batch and scheduled analysis, PDF/Word export and custom agents are Pro-only
- **−** MongoDB and Redis must be installed and secured separately; no compose file
- **−** A-share market only; UI and docs are mainly Chinese

<sub>no GPU · Needs MongoDB 7.0+, Redis 6+, Node.js 18+, Python 3.11, Tushare/AKShare/BaoStock data access · Models: OpenAI, DeepSeek, Qwen · port 3000 · [Repo](https://github.com/hsliuping/tradingagents-cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tradingagents-cn/)</sub>

<a name="leptonai"></a>
### #&#8288;72 [leptonai](https://github.com/leptonai/leptonai) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · Apache-2.0 · Nov 2026</sub>

**Python SDK and lep CLI for managing NVIDIA DGX Cloud Lepton workloads.**

Client library and `lep` command-line tool for the NVIDIA DGX Cloud Lepton platform. It creates and manages endpoints, Dynamo graph deployments (vLLM, SGLang, TensorRT-LLM), batch jobs, dev pods, Ray clusters, and Slurm inspection. A Python `Client` calls deployed endpoints as functions, and a bundled skill lets Claude Code or Codex drive the CLI.

- **+** Single CLI covers endpoints, jobs, dev pods, Ray clusters, Dynamo deployments and Slurm inspection
- **+** Dynamo commands support multi-node and disaggregated prefill/decode with vLLM, SGLang or TensorRT-LLM
- **+** Shell access through workspace API over HTTPS, no SSH keys needed; Teleport SSH also supported
- **+** Ships a Claude Code and Codex plugin that asks confirmation before modifying workloads
- **−** Only works against NVIDIA DGX Cloud Lepton; it is not a self-hostable serving stack
- **−** Requires a Lepton workspace account and login to do anything useful
- **−** Teleport SSH needs a local tsh v18+ and workspace-side Teleport enablement
- **−** Slurm job submission and cancellation stay outside the CLI; it only inspects

<sub>Needs NVIDIA DGX Cloud Lepton workspace, tsh v18+ (optional, for Teleport SSH) · Models: vLLM, SGLang, TensorRT-LLM · [Repo](https://github.com/leptonai/leptonai) · [📖 Docs ↗](https://docs.nvidia.com/dgx-cloud/lepton/reference/cli/get-started/) · [🌐 Site ↗](https://docs.nvidia.com/dgx-cloud/lepton) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/leptonai/)</sub>

<a name="eigenflux"></a>
### #&#8288;73 [eigenflux](https://github.com/phronesis-io/eigenflux) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · custom license · Nov 2026</sub>

**Broadcast network where AI agents publish signals and receive matched ones.**

EigenFlux is a Go hub (CloudWeGo Kitex/Hertz microservices) that lets agents publish broadcasts and receive a personalized feed matched to a natural-language profile. Content is enriched by an async LLM pipeline and matched with Elasticsearch and Redis caching. A CLI and skills connect agents on OpenClaw, Codex or Claude Code to the public hub or a self-hosted one.

- **+** Same production codebase as the public hub, so self-hosting matches the hosted service
- **+** Agent identity is a local Ed25519 key; credentials stay out of prompts
- **+** Plugins for OpenClaw, Claude Code and Codex, plus a bare CLI for other hosts
- **+** Swagger UI and design docs for feed, sort and item pipelines are included
- **−** Self-hosting needs Go 1.25+, Docker Compose, Elasticsearch and Redis plus LLM and embedding API keys
- **−** Commission payments and payouts support only Alipay in CNY
- **−** License is custom (Apache 2.0 with extra conditions), not a standard OSI license
- **−** Privacy boundary is enforced by agent instructions, not by technical filtering

<sub>no GPU · Compose · Needs Docker Compose, Elasticsearch, Redis, LLM API (OpenAI by default), Embedding API, Go 1.25+ · Models: OpenAI-compatible LLM and embedding APIs · port 8080 · [Repo](https://github.com/phronesis-io/eigenflux) · [▶️ Demo ↗](https://www.eigenflux.ai/live) · [📖 Docs ↗](https://github.com/phronesis-io/eigenflux/blob/main/docs/architecture_overview.md) · [🌐 Site ↗](https://www.eigenflux.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/eigenflux/)</sub>

<a name="brainpilot"></a>
### #&#8288;74 [brainpilot](https://github.com/neuroaihub/brainpilot) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · AGPL-3.0 · Oct 2026</sub>

**Multi-agent research workspace for brain science with an inspectable trace graph.**

BrainPilot is a human-in-the-loop research system for neuroscience. A PI agent plans the work and coordinates librarian, experimentalist, engineer, writer and auditor agents, using 72 bundled domain skills, MCP tools and paper databases. Each session is recorded as a Graph of Trace. It installs via npm (Node.js 22+) and serves a local web UI backed by an Anthropic, OpenAI or Azure provider.

- **+** Auditor agent checks claims and citations; Graph of Trace records each session
- **+** 72 bundled neuroscience skills, user-editable, loaded on demand from SKILL.md files
- **+** One npm install; BP_MOCK=1 allows a smoke run without an API key
- **+** Anthropic, OpenAI Completions/Responses and Azure providers; context up to 1M tokens
- **−** Local npm mode has no container isolation; agents read and write directly on the host
- **−** Specific to brain science, a poor fit as a general agent builder
- **−** Each runtime is single-user; multi-user hosting needs a separate data dir per user
- **−** AGPL-3.0 license restricts closed-source network deployments

<sub>no GPU · Docker + Compose · Needs Node.js >= 22, Model provider API key, Docker (optional, for sandbox) · Models: Anthropic Messages, OpenAI Completions, OpenAI Responses, Azure OpenAI Responses · [Repo](https://github.com/neuroaihub/brainpilot) · [▶️ Demo ↗](https://brainpilot.chat) · [📖 Docs ↗](https://brainpilot.chat/docs) · [🌐 Site ↗](https://brainpilot.chat) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/brainpilot/)</sub>

<a name="intentkit"></a>
### #&#8288;75 [intentkit](https://github.com/crestalnetwork/intentkit) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: known (41) · Freshness: active (100) · Maintenance: weak (29) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Sep 2026</sub>

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

<a name="opendots"></a>
### #&#8288;76 [opendots](https://github.com/copilotkit/opendots) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (42) · Freshness: active (100) · Maintenance: patchy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · MIT · Nov 2026</sub>

**Template for persistent AI agents with their own browser, files, and Slack access.**

OpenDots is a TypeScript starter for a single-owner agent workspace: specialist "Dots" with per-Dot roles, tool permissions, and optional isolated computers via OpenBot services. It adds Spaces with a page editor, text and WebRTC voice chat, Slack via Channels SDK, MCP and Composio connections, and approval cards for writes. Chat requires CopilotKit Intelligence (hosted, local Docker evaluation, or licensed self-hosted). Status is alpha.

- **+** Per-Dot computers with persistent browser profile, files, shell, and human takeover
- **+** Human-in-the-loop approval cards for page saves and non-read-only MCP tools
- **+** Per-Dot permissions for tools, MCP servers, and Composio toolkits
- **+** Manual page editing works before any conversation service is configured
- **−** Chat requires CopilotKit Intelligence, which needs CopilotKit sign-in or a licensed deployment
- **−** Alpha and single-owner only; no multi-user sharing, invitations, or file uploads
- **−** Slack and spoken compute delegation are not yet verified against live services
- **−** Telemetry is on by default; web search sends queries to Parallel unless disabled

<sub>no GPU · Docker + Compose · Needs CopilotKit Intelligence, OpenAI-compatible model provider, Node.js 24, SQLite, OpenBot computer services, Composio (optional), Slack (optional), Realtime speech provider (calls) · Models: OpenAI-compatible providers · port 5173 · [Repo](https://github.com/copilotkit/opendots) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opendots/)</sub>

<a name="mission-control"></a>
### #&#8288;77 [mission-control](https://github.com/builderz-labs/mission-control) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (40) · Freshness: active (100) · Maintenance: patchy (35) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Oct 2026</sub>

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

<a name="dr-claw"></a>
### #&#8288;78 [dr-claw](https://github.com/openlair/dr-claw) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · custom license · Nov 2026</sub>

**Research workspace that drives Claude Code, Gemini CLI or Codex through a paper pipeline.**

Dr. Claw is a Node.js web and Electron desktop workspace that wraps Claude Code, Gemini CLI, Codex and OpenRouter models as execution agents for research projects. It tracks a Survey, Ideation, Experiment, Publication and Promotion pipeline, with 121 built-in skills, a news feed, a file and Git explorer, and one-click Auto Research. Local models can run on Ollama, vLLM or SGLang.

- **+** Switches between Claude Code, Gemini CLI, Codex and OpenRouter as execution backends
- **+** Produces stage-organized artifacts: survey reports, experiment code, LaTeX paper draft, slides
- **+** Installs via desktop app (macOS arm64, Windows x64), npx, or source
- **+** Terminal options: dr-claw chat for OpenRouter models and a drclaw CLI harness
- **−** Needs an external agent CLI or OpenRouter key; it is not a standalone model runner
- **−** Desktop installers cover only Apple Silicon macOS and Windows x64; no Linux or Intel Mac
- **−** macOS build is not notarized; first launch needs an xattr command
- **−** npm package can lag behind the desktop release; license is a GPL-3.0 and AGPL-3.0 mix

<sub>GPU optional · Needs Node.js 20+ (22 LTS recommended), Claude Code CLI, Gemini CLI, Codex CLI or OpenRouter API key · Models: Claude Code, Gemini CLI, Codex, OpenRouter, Ollama · port 3001 · [Repo](https://github.com/openlair/dr-claw) · [📖 Docs ↗](https://github.com/OpenLAIR/dr-claw/blob/main/docs/configuration.md) · [🌐 Site ↗](https://openlair.github.io/dr-claw) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dr-claw/)</sub>

<a name="panwatch"></a>
### #&#8288;79 [panwatch](https://github.com/tnt-likely/panwatch) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · MIT · Nov 2026</sub>

**Stock and portfolio monitor for A-share, HK and US markets with AI analysis.**

PanWatch tracks multi-account portfolios, quotes and price alerts across mainland China, Hong Kong and US markets. Scheduled agents run pre-market, intraday and closing analysis, and a TradingAgents integration runs a multi-agent debate and risk review on a chosen holding. It uses any OpenAI-compatible provider or Ollama, and sends reports to Telegram, WeCom, DingTalk, Feishu, Bark or webhooks.

- **+** Covers A-share, HK and US markets with exchange calendars and holiday-aware scheduling
- **+** Works with OpenAI-compatible providers or local models through Ollama
- **+** Six notification channels including webhooks; installable PWA for mobile
- **+** Optional OpenTelemetry export of agent runs and LLM calls, off by default
- **−** ETF holdings, NAV, fees and tracking error are not yet supplied as structured data
- **−** Paper trading does not model ETF T+0 exceptions, margin, FX or broker fees
- **−** Bundled exchange calendars need yearly updates; unpublished dates block automatic runs
- **−** TradingAgents runs take 3-5 minutes and use model quota; cost depends on the model

<sub>no GPU · Docker · Needs OpenAI-compatible LLM provider or Ollama, Playwright Chromium (downloaded on first start) · Models: OpenAI-compatible APIs, Ollama · port 8000 · [Repo](https://github.com/tnt-likely/panwatch) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/panwatch/)</sub>

<a name="finrobot"></a>
### #&#8288;80 [finrobot](https://github.com/ai4finance-foundation/finrobot) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · Apache-2.0 · Oct 2026</sub>

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

<a name="onecli"></a>
### #&#8288;81 [onecli](https://github.com/onecli/onecli) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Nov 2026</sub>

**Runs a sandboxed agent per employee behind a credential-injecting gateway.**

OneCLI creates one sandboxed agent per team member, reachable from a Next.js dashboard or Slack. Outbound traffic passes through a Rust gateway that injects credentials, so agents never see secrets, and enforces a shared policy with human approval for sensitive actions. Secrets are stored AES-256-GCM encrypted, or fetched on demand from Bitwarden or 1Password.

- **+** Gateway injects credentials via MITM proxy, so agents never hold secrets
- **+** Per-agent sandbox, memory, skills and schedule, managed from one dashboard
- **+** Runner is outbound-only: works behind NAT with no ingress or tunnel
- **+** Helm chart for Kubernetes plus a pnpm-based self-host path
- **−** Enterprise features in ee/ directories need a paid subscription for production use
- **−** Multi-component stack: dashboard, API server, gateway, runner, supervisor, Postgres
- **−** Self-host setup uses pnpm and mise; no Docker or Compose file detected
- **−** Slack is the only chat channel mentioned besides the dashboard

<sub>Docker + Compose · Needs PostgreSQL, pnpm, Slack (optional), Bitwarden or 1Password (optional), Kubernetes (optional) · port 10254 · [Repo](https://github.com/onecli/onecli) · [📖 Docs ↗](https://onecli.sh/docs) · [🌐 Site ↗](https://onecli.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onecli/)</sub>

<a name="video-search-and-summarization"></a>
### #&#8288;82 [video-search-and-summarization](https://github.com/nvidia-ai-blueprints/video-search-and-summarization) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Nov 2026</sub>

**NVIDIA reference stack for searching and summarizing video with VLMs.**

Reference implementation of NVIDIA's Video Search and Summarization blueprint. It includes microservices for RTSP/ONVIF ingest, real-time VLM captioning and embeddings, behavior analytics, alert verification and long-video summarization, plus an MCP-based agent. It uses NVIDIA NIM models (Cosmos3 Nano Reasoner, Nemotron 3.5 Lightning 30B A3B) and deploys with Docker Compose, Helm or a Brev launchable.

- **+** Covers ingest, embeddings, analytics, alert verification and summarization in one repository
- **+** Agent exposes video tools over MCP; ships agentskills.io-compatible skills
- **+** Separate reference workflows for Q&A, alerts, search and long video summarization
- **+** Documents validated OS, driver and Docker versions, including Jetson and DGX targets
- **−** Tied to NVIDIA GPUs, NIM microservices and NGC-hosted images
- **−** Hosting NIM locally requires an NVIDIA AI Enterprise developer license
- **−** Video embedding search workflow is marked alpha
- **−** Many services (Elasticsearch, Redis, Kafka) make setup heavy; README says it needs technical expertise

<sub>GPU required · Compose · Needs NVIDIA NIM, NGC API key, Docker Engine 28.3.3 to below 29.5.0, Docker Compose v2.39.1+, NVIDIA Container Toolkit 1.17.8+, Elasticsearch, Redis, Kafka · Models: Cosmos3 Nano Reasoner, NVIDIA Nemotron 3.5 Lightning 30B A3B · [Repo](https://github.com/nvidia-ai-blueprints/video-search-and-summarization) · [▶️ Demo ↗](https://build.nvidia.com/nvidia/video-search-and-summarization) · [📖 Docs ↗](https://docs.nvidia.com/vss/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/video-search-and-summarization/)</sub>

<a name="botpress"></a>
### #&#8288;83 [Botpress](https://github.com/botpress/botpress) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (70) · Freshness: recent (70) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

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

<a name="openfang"></a>
### #&#8288;84 [openfang](https://github.com/rightnow-ai/openfang) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (74) · Freshness: recent (75) · Maintenance: weak (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · May 2026</sub>

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

<a name="claude-for-legal"></a>
### #&#8288;85 [claude-for-legal](https://github.com/anthropics/claude-for-legal) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (57) · Freshness: active (92) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 10.0k · Apache-2.0 · Jul 2026</sub>

**Claude plugins for in-house, litigation and law-school legal workflows.**

Claude Cowork and Claude Code plugins covering twelve legal areas, including commercial, corporate, employment, privacy, IP, litigation, a law clinic and law students. Each plugin ships skills as slash commands, such as /commercial-legal:review, and reads a CLAUDE.md practice profile filled in by a cold-start interview. Five scheduled workflows can also be deployed through the Claude Managed Agents API.

- **+** Around 90 named agents, each mapped to a plugin and a slash command
- **+** Same skills and system prompt run as a plugin or through the Managed Agents API
- **+** Per-plugin CLAUDE.md practice profile built from a cold-start interview of your playbook
- **+** MCP connectors for Slack, Box, DocuSign, Ironclad, iManage, Everlaw and CourtListener
- **−** Requires Claude Cowork, Claude Code or the Managed Agents API; no local model support
- **−** Outputs are drafts for attorney review; the README disclaims legal advice
- **−** Legal-specific connectors depend on separate commercial systems and their credentials
- **−** No tagged releases; installed from a marketplace path or GitHub URL

<sub>no GPU · Needs Claude Cowork or Claude Code, Claude Managed Agents API, MCP connectors (Slack, Google Drive, Box, Ironclad, DocuSign, iManage, Everlaw, CourtListener) · Models: Claude · [Repo](https://github.com/anthropics/claude-for-legal) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/claude-for-legal/)</sub>

<a name="refly"></a>
### #&#8288;86 [refly](https://github.com/refly-ai/refly) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (47) · Freshness: active (91) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · custom license · Nov 2026</sub>

**Builder for versioned agent skills, exported as REST APIs, webhooks or MCP.**

Refly is a workflow builder where you describe a process in natural language (Vibe Mode) or wire nodes on a canvas, then save it as a versioned skill. Skills can be called through a REST API, triggered by webhooks (Lark/Feishu), or installed into Claude Code via the refly CLI. It supports MCP servers and lists 3,000+ tool integrations, with a hosted workspace and a self-deployment guide.

- **+** Workflows publish as REST endpoints, webhooks, or Claude Code skills via the refly CLI
- **+** Runtime can be paused and re-steered mid-run, with repair of failing workflows
- **+** Central skill registry with versioning, sharing and audit logs for teams
- **+** Supports MCP servers and a tool/provider catalog in config/provider-catalog.json
- **−** Custom ReflyAI license: Apache 2.0 plus extra restrictions, not OSI-standard
- **−** Cursor export is marked coming soon; the Lark/Feishu guide is unfinished
- **−** No Docker or compose files detected in the repo; deployment is only in linked docs
- **−** Claims such as 100% reliability and 3-minute builds come with no benchmarks

<sub>Compose · Needs LLM provider API key (e.g. OpenAI, Anthropic) · Models: OpenAI, Anthropic, providers in config/provider-catalog.json · port 5700 · [Repo](https://github.com/refly-ai/refly) · [▶️ Demo ↗](https://refly.ai/workspace) · [📖 Docs ↗](https://docs.refly.ai/) · [🌐 Site ↗](https://refly.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/refly/)</sub>

<a name="alta"></a>
### #&#8288;87 [alta](https://github.com/kyky2347/alta) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · Apache-2.0 · Sep 2026</sub>

**Multi-agent LLM market research system with simulated and broker execution.**

ALTA runs four specialist LLM Scouts that research market opportunities. Each thesis then goes to independent reviewers, code-based ranking and a strategy desk that compares instruments. Every handoff is saved as a versioned record in PostgreSQL and shown in a React operator console. Execution is either an internal Shadow simulation or a broker API (Tiger, Alpaca, IBKR, Futu). The README labels it research-only software.

- **+** Reviewers commit assessments independently; code, not an Agent, handles ranking and execution gates
- **+** Evidence, reviews and outcomes are linked records traceable by ID, with event time kept separate
- **+** Shadow mode simulates fills and exits without sending broker orders
- **+** Console in English, Simplified and Traditional Chinese; model assignable per agent role
- **−** Live-account acceptance not established; Longbridge and Schwab connectors are authorization-blocked
- **−** Broker lifecycle limited to one plan per account, long USD stocks/ETFs, whole shares, DAY limits
- **−** Exits are software-managed, so downtime can delay them; stopping ALTA leaves positions open
- **−** Needs Node 22, Python 3.12, uv, Docker and a Rust toolchain; macOS or Linux only

<sub>Needs PostgreSQL, Redis, Docker/OrbStack, Node.js 22+, Python 3.12, uv, Rust toolchain, Codex App Server · Models: Codex App Server sessions, configurable models per agent role · [Repo](https://github.com/kyky2347/alta) · [📖 Docs ↗](https://github.com/kyky2347/ALTA/blob/main/docs/architecture/overview.md) · [🌐 Site ↗](https://alta.silment.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/alta/)</sub>

<a name="edict"></a>
### #&#8288;88 [edict](https://github.com/cft0808/edict) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: popular (73) · Freshness: recent (63) · Maintenance: weak (21) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · May 2026</sub>

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

<a name="magentic-ui"></a>
### #&#8288;89 [magentic-ui](https://github.com/microsoft/magentic-ui) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (58) · Freshness: active (94) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Jul 2026</sub>

**Browser and file-system agent built for small orchestrator and browser-use models.**

MagenticLite is the successor to Magentic-UI from Microsoft AI Frontiers. It pairs an orchestrator model (MagenticBrain) with a browser-use model (Fara) to automate web research, form filling and local file management from a web UI. Browser sessions run in a lightweight VM sandbox (Quicksand), and the agent pauses for approval before critical actions.

- **+** Designed for small models rather than frontier-scale ones
- **+** Browser sessions isolated in a Quicksand VM sandbox
- **+** Approve, steer or take over mid-task; stops before critical actions
- **+** Installs from PyPI with uv and serves a web UI on port 8081
- **−** You must host or connect a model endpoint yourself
- **−** Quick start covers only macOS and Windows via WSL
- **−** A limitations doc lists tasks it does not handle well

<sub>Needs uv, Python 3.12, Quicksand VM sandbox, model endpoint · Models: MagenticBrain, Fara · port 8081 · [Repo](https://github.com/microsoft/magentic-ui) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/magentic-ui/)</sub>

<a name="cultivation-world-simulator"></a>
### #&#8288;90 [cultivation-world-simulator](https://github.com/4thfever/cultivation-world-simulator) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: weak (28) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · custom license · Aug 2026</sub>

**Xianxia world simulator where every NPC is driven by an LLM.**

A simulation game in which each cultivator is an independent LLM agent with personality, memory, relationships and goals, bounded by a rule system covering realms, sects, techniques, pills and events. The player acts as an observer who can intervene. It runs from source (FastAPI backend, Vue/PixiJS frontend), via docker-compose, or as an Epic Games Store desktop build, and exposes a query/command HTTP API for external agents.

- **+** Per-NPC LLM agents with short and long-term memory, goals and relationships, bounded by game rules
- **+** Model presets for DeepSeek, MiniMax and Ollama, so local models work
- **+** Versioned /api/v1 query and command endpoints let external agents observe and intervene
- **+** Three install paths: source, docker-compose, or Epic Games Store desktop build
- **−** Docker deployment is labeled untested in the README
- **−** Many concurrent LLM agents imply heavy API usage; cost and throughput are not documented
- **−** Mobile UI is not fully adapted
- **−** Main README is in Chinese; license is not identified (NOASSERTION)

<sub>GPU optional · Docker + Compose · Needs Python 3.10+, Node.js 18+, LLM provider or Ollama · Models: DeepSeek, MiniMax, Ollama, custom LLM API · port 8123 · [Repo](https://github.com/4thfever/cultivation-world-simulator) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cultivation-world-simulator/)</sub>

<a name="kubectl-ai"></a>
### #&#8288;91 [kubectl-ai](https://github.com/googlecloudplatform/kubectl-ai) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: known (47) · Freshness: active (88) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Jul 2026</sub>

**Kubernetes CLI agent that turns plain-language requests into kubectl operations.**

kubectl-ai is a Go CLI and kubectl plugin that sends a prompt to an LLM, which proposes and runs kubectl and bash commands against your cluster. It supports Gemini (default), Vertex AI, OpenAI, Azure OpenAI, Grok, Bedrock, Ollama and llama.cpp. It can also act as an MCP server or client, and offers a terminal or web UI.

- **+** Works with many providers, including local Ollama and llama.cpp models
- **+** Runs interactively, one-shot, or from stdin pipes, and as a `kubectl ai` plugin
- **+** Acts as MCP server and client; custom tools are defined in YAML
- **+** Opt-in session save and resume across runs
- **−** Not an officially supported Google product
- **−** MCP streamable-http endpoint is unauthenticated unless OAuth 2.1 flags are set
- **−** Local models need --enable-tool-use-shim for tool calling
- **−** Runs kubectl and bash, so cluster changes depend on LLM output and permission prompts

<sub>no GPU · Needs kubectl, LLM provider API key or local Ollama/llama.cpp · Models: gemini, vertexai, openai, azopenai, grok · port 8888 · [Repo](https://github.com/googlecloudplatform/kubectl-ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kubectl-ai/)</sub>

<a name="kocoro-lab-shannon"></a>
### #&#8288;92 [shannon](https://github.com/kocoro-lab/shannon) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · MIT · Sep 2026</sub>

**Multi-agent orchestration on Temporal with token budgets and replay debugging.**

Shannon is a multi-agent orchestration stack with a Go gateway and orchestrator, a Rust agent core with a WASI sandbox, and a Python LLM service. Tasks are submitted over REST, an OpenAI-compatible API or a Python SDK, then routed by complexity to strategies such as DAG, ReAct, research and swarm. Temporal provides workflow replay, and per-task token budgets fall back to cheaper models.

- **+** Temporal workflows allow step-by-step replay of failed runs via scripts/replay_workflow.sh
- **+** Hard per-task token budgets via budget_max, with fallback to cheaper models
- **+** Code runs in a WASI sandbox; OPA policies can gate actions behind human approval
- **+** OpenAI-compatible endpoint plus REST, SSE, WebSocket and a Python SDK
- **−** Many moving parts: gateway, orchestrator, agent core, LLM service, Temporal, PostgreSQL, Redis
- **−** Needs an external LLM API key or a separately hosted local model endpoint
- **−** Playwright browser image is 3.4GB and is not started by default
- **−** Source build needs Go, Rust and Python toolchains; quick install is a curl-pipe-bash script

<sub>no GPU · Compose · Needs Docker Compose, Temporal, PostgreSQL, Redis, LLM provider API key · Models: OpenAI, Anthropic, Google Gemini, xAI, DeepSeek · port 8080 · [Repo](https://github.com/kocoro-lab/shannon) · [▶️ Demo ↗](https://shannon.run) · [📖 Docs ↗](https://docs.shannon.run) · [🌐 Site ↗](https://shannon.run) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kocoro-lab-shannon/)</sub>

<a name="ai-trader"></a>
### #&#8288;93 [ai-trader](https://github.com/hkuds/ai-trader) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: popular (79) · Freshness: recent (76) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 23k · no license · Jun 2026</sub>

**Trading platform where AI agents publish signals, discuss, and copy trades.**

AI-Trader is a platform where AI agents register by reading a SKILL.md file, publish trading signals, discuss strategies and copy other agents' trades. It offers $100K paper trading and Polymarket paper trading. The repo holds a FastAPI backend, a React frontend, agent skill definitions and OpenAPI specs, and can be self-hosted with PostgreSQL or SQLite. A hosted instance runs at ai4trade.ai.

- **+** Agents join by reading a SKILL.md; works with Claude Code, Codex, Cursor, OpenClaw and others
- **+** Paper trading with simulated capital and Polymarket paper trading, so no real funds at risk
- **+** FastAPI web service runs separately from background workers; OpenAPI specs are included
- **+** Self-hosting supports PostgreSQL for production or SQLite for local use
- **−** No license detected by tooling, despite the README's MIT badge; reuse terms unclear
- **−** Self-hosting docs cover only the database choice; no Docker or compose setup
- **−** Price data depends on Alpha Vantage or yfinance fallback, so rate limits apply
- **−** A social signal-sharing platform, not a standalone trading bot or backtester

<sub>no GPU · Needs PostgreSQL or SQLite, Alpha Vantage (optional), yfinance · [Repo](https://github.com/hkuds/ai-trader) · [▶️ Demo ↗](https://ai4trade.ai) · [🌐 Site ↗](https://ai4trade.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-trader/)</sub>

<a name="karpathy"></a>
### #&#8288;94 [karpathy](https://github.com/k-dense-ai/karpathy) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Aug 2026</sub>

**ML engineer agent that trains models in a local sandbox using Agent Skills.**

Runs an agent built on the Claude Agent SDK and Google ADK that writes and runs ML training code inside a local sandbox directory. Setup creates a Python virtualenv with PyTorch, transformers and scikit-learn, and loads skills from the Scientific Agent Skills collection. You drive it from the ADK web interface and collect outputs from the sandbox folder.

- **+** start.py builds the sandbox, ML virtualenv and skills in one step
- **+** Reuses the open Agent Skills standard via Scientific Agent Skills (130+ skills)
- **+** Outputs land in a plain sandbox directory you can inspect while the agent works
- **+** MIT licensed, small Python codebase
- **−** Requires an authenticated Claude Code install plus an OpenRouter API key
- **−** Sandbox is a local directory; Modal compute integration is only listed as upcoming
- **−** Datasets and scripts must be copied into the sandbox by hand
- **−** README calls it a simple demo; fuller capabilities point to the paid K-Dense service

<sub>Needs Python 3.13+, uv, Claude Code, OpenRouter API key, Google ADK · Models: OpenRouter models via AGENT_MODEL · port 8000 · [Repo](https://github.com/k-dense-ai/karpathy) · [🌐 Site ↗](https://www.k-dense.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/karpathy/)</sub>

<a name="firered-openstoryline"></a>
### #&#8288;95 [firered-openstoryline](https://github.com/fireredteam/firered-openstoryline) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (16) · Freshness: active (95) · Maintenance: weak (0) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · Apache-2.0 · Jul 2026</sub>

**Chat-driven video editor that finds media, writes scripts, adds music and voiceover.**

FireRed-OpenStoryline is a Python agent that edits videos through natural-language conversation. It searches and downloads media, segments clips, generates a script and narration, picks BGM, voiceover and fonts, and renders with MoviePy and FFmpeg. It runs behind an MCP server with a CLI or FastAPI web UI, and ships Skills for OpenClaw and Claude Code.

- **+** Edits are done by chat: cut, swap, reorder clips, adjust color, font and position
- **+** Saved editing workflows can be reused as Skills for batch creation with new media
- **+** Offers CLI, web UI, MCP server, plus OpenClaw and Claude Code Skills
- **+** Hosted HuggingFace demo available to try before installing
- **−** Requires API keys set in config.toml; supported LLM providers are not listed
- **−** AI transitions need third-party video generation services, which the README calls costly
- **−** Default open-source fonts and music are basic; better results need a custom asset library
- **−** Setup needs Conda, downloaded model and resource archives, and a separately started MCP server

<sub>Docker · Needs Python 3.11+, FFmpeg, MoviePy, LangChain, Conda, third-party LLM API keys, third-party AIGC video service (AI transitions) · port 8005 · [Repo](https://github.com/fireredteam/firered-openstoryline) · [▶️ Demo ↗](https://fireredteam-firered-openstoryline.hf.space/) · [🌐 Site ↗](https://fireredteam.github.io/demos/firered_openstoryline/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/firered-openstoryline/)</sub>

<a name="ai-market-maker"></a>
### #&#8288;96 [ai-market-maker](https://github.com/olaxbt/ai-market-maker) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · AGPL-3.0 · Aug 2026</sub>

**LangGraph multi-agent crypto trading stack with a Risk Guard veto.**

Runs specialist LLM trading desks (technical, macro, news, pattern, statistical) through a LangGraph workflow, fuses their signals with weighted math, and sends proposals through a Risk Guard veto before execution on Binance Testnet. It includes a bar-by-bar perp backtester with buy-and-hold benchmarks, pinned historical data with a sha256 manifest, and a Next.js dashboard backed by Postgres.

- **+** Risk Guard has final veto before any trade executes
- **+** Pinned data/ with sha256 manifest allows offline --csv-only backtests
- **+** Every backtest reports Sharpe, Sortino, profit factor and buy-and-hold excess return
- **+** Strategy lives in deploy JSON; .env holds secrets only
- **−** Agentic mode and backtests require an OpenAI or Atlas Cloud API key
- **−** LLM path dependence means backtest re-runs are not bit-identical
- **−** Execution limited to Binance Testnet; Hyperliquid adapter is dry-run only
- **−** TA-Lib C library must be installed separately for CLI use

<sub>no GPU · Docker + Compose · Needs Docker Compose, PostgreSQL, TA-Lib, Binance Testnet API keys, OpenAI or Atlas Cloud API key · Models: OpenAI-compatible API, Atlas Cloud · port 3000 · [Repo](https://github.com/olaxbt/ai-market-maker) · [🌐 Site ↗](https://www.olaxbt.xyz/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-market-maker/)</sub>

<a name="hyper-alpha-arena"></a>
### #&#8288;97 [hyper-alpha-arena](https://github.com/hammergpt/hyper-alpha-arena) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Nov 2026</sub>

**LLM-driven crypto perpetual trading on Hyperliquid and Binance Futures.**

Runs LLM-based traders that place perpetual futures orders on Hyperliquid (testnet and mainnet) and Binance Futures. It includes 86 built-in quant factors with IC/ICIR scoring, a custom expression engine, market-flow signal triggers (order flow, open interest, funding rate), and a Python Program Trader with backtesting. Helper agents assist with configuration, and Hyper AI is also reachable via Telegram and Discord.

- **+** Hyperliquid testnet allows paper trading before committing real funds
- **+** Two modes: natural-language AI Trader and Python Program Trader with backtesting
- **+** 86 built-in factors plus a 69-function custom expression engine
- **+** Works with any OpenAI-compatible endpoint, including Deepseek, GPT and Claude
- **−** Hosted login service is shut down; auth code still depends on it
- **−** Self-hosted multi-user access needs your own identity and authorization work
- **−** No per-user data isolation; README advises localhost or a private network only
- **−** No tagged releases; updates come from git pull on main

<sub>no GPU · Docker + Compose · Needs Docker, PostgreSQL, Hyperliquid or Binance Futures account, OpenAI-compatible LLM API · Models: Deepseek, OpenAI GPT-5/o1/GPT-4o, Claude via compatible endpoints, Any OpenAI-compatible API · port 8802 · [Repo](https://github.com/hammergpt/hyper-alpha-arena) · [📖 Docs ↗](https://www.akooi.com/docs/) · [🌐 Site ↗](https://www.akooi.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hyper-alpha-arena/)</sub>

<a name="valuecell"></a>
### #&#8288;98 [valuecell](https://github.com/valuecell-ai/valuecell) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: popular (60) · Freshness: slowing (42) · Maintenance: weak (0) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Feb 2026</sub>

**Multi-agent platform for stock research and crypto strategy trading.**

ValueCell runs a set of finance-focused agents: DeepResearch for fundamental documents, a Strategy agent that executes crypto trading strategies, and a News agent for scheduled delivery. It ships as a macOS/Windows app or runs from source with start.sh, and connects to several LLM providers and exchanges. API keys and data are stored locally in LanceDB and SQLite.

- **+** Live routing to Binance, Hyperliquid and OKX, each marked tested in the README
- **+** Supports OpenRouter, SiliconFlow, Azure, Google, OpenAI, DeepSeek and OpenAI-compatible endpoints
- **+** Secrets and data stay on the local device, stored in LanceDB and SQLite
- **+** Prebuilt macOS and Windows apps, plus a start.sh/start.ps1 source launcher
- **−** Trading is contract-only; spot is implemented as 1X contracts
- **−** Coinbase, Gate.io, MEXC and Blockchain support is only partially tested
- **−** Agent set is fixed; plugin architecture, SDK and agent registry are still roadmap items
- **−** Depends on external LLM APIs; local model support is not documented

<sub>no GPU · Docker · Needs LLM provider API key, Exchange API credentials (Binance, Hyperliquid, OKX), LanceDB, SQLite · Models: OpenRouter, SiliconFlow, Azure, OpenAI-compatible, Google · port 1420 · [Repo](https://github.com/valuecell-ai/valuecell) · [📖 Docs ↗](https://github.com/ValueCell-ai/valuecell/blob/main/docs/CONFIGURATION_GUIDE.md) · [🌐 Site ↗](https://valuecell.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/valuecell/)</sub>

<a name="aiagents-stock"></a>
### #&#8288;99 [aiagents-stock](https://github.com/oficcejo/aiagents-stock) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (6) · Freshness: active (81) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 2.1k · no license · Oct 2026</sub>

**Streamlit app where AI analyst agents research A-share, HK and US stocks.**

Streamlit app that runs six LLM analyst roles (technical, fundamental, fund flow, risk, sentiment, news) on a stock, then produces a team discussion, a rating and a PDF report. It adds iwencai-based screeners, price alerts via email, DingTalk or Feishu, and optional MiniQMT order placement. Works with any OpenAI-compatible model, defaulting to DeepSeek.

- **+** Covers analysis, screening, monitoring, portfolio schedules and notifications in a single app
- **+** Any OpenAI-compatible model via DEFAULT_MODEL_NAME; optional OrcaRouter gateway
- **+** Data source fallback chain TDX, Tushare, AKShare; Compose file included
- **+** API keys and notifications configurable from a web settings page
- **−** Screeners need an iwencai login cookie and Playwright Chromium
- **−** README and UI are Chinese only; targets Chinese market data and brokers
- **−** No license file detected by tooling, though the README says MIT
- **−** Auto trading needs a locally running MiniQMT client; not investment advice per its disclaimer

<sub>no GPU · Docker + Compose · Needs DeepSeek or OpenAI-compatible API key, Node.js 16+ (pywencai), Playwright Chromium, SQLite, Tushare token (optional), MiniQMT (optional) · Models: DeepSeek, Qwen, GPT-4o, OpenAI-compatible APIs, OrcaRouter · port 8503 · [Repo](https://github.com/oficcejo/aiagents-stock) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aiagents-stock/)</sub>

<a name="ai-scientist-v2"></a>
### #&#8288;100 [ai-scientist-v2](https://github.com/sakanaai/ai-scientist-v2) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: known (46) · Freshness: quiet (13) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · custom license · Dec 2025</sub>

**Agentic tree-search pipeline that generates ML experiments and writes research papers.**

Takes a research topic in Markdown, brainstorms ideas with literature-based novelty checks, then runs a tree search over LLM-written experiment code. It analyzes results and writes a LaTeX paper PDF, with an LLM review step. Unlike v1 it needs no human-authored templates, but the README says success rates are lower than v1 with a strong template.

- **+** End-to-end pipeline: ideation, experiments, plots, LaTeX write-up and review in one repo
- **+** Tree search settings (workers, steps, debug depth, drafts) are configurable in bfts_config.yaml
- **+** Supports OpenAI, Gemini and Claude via AWS Bedrock; README gives per-run cost estimates
- **+** No human-written templates required, unlike v1
- **−** Executes LLM-written code; README tells users to sandbox it themselves, no Docker provided
- **−** Custom license (NOASSERTION) requires disclosing AI use in resulting manuscripts
- **−** Linux with NVIDIA GPU and CUDA assumed; installation can take up to an hour
- **−** Lower success rate than v1; runs often finish without a PDF

<sub>GPU required · Needs PyTorch with CUDA, conda, poppler, chktex, LaTeX tools, Semantic Scholar API (optional) · Models: OpenAI, Gemini, Claude via AWS Bedrock · [Repo](https://github.com/sakanaai/ai-scientist-v2) · [📖 Docs ↗](https://pub.sakana.ai/ai-scientist-v2/paper) · [🌐 Site ↗](https://sakana.ai/ai-scientist-first-publication/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-scientist-v2/)</sub>

<a name="biomni"></a>
### #&#8288;101 [biomni](https://github.com/snap-stanford/biomni) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: niche (20) · Freshness: quiet (29) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · Apache-2.0 · Jan 2026</sub>

**Biomedical research agent that plans and runs code across bio tools and databases.**

Biomni is a Python agent (class A1) that takes natural-language biomedical tasks, such as CRISPR screen planning, scRNA-seq annotation or ADMET prediction, and runs LLM-generated code against bundled tools, software and an ~11GB data lake. It works with Anthropic, OpenAI, Azure, Gemini, Bedrock, Groq, Ollama or custom endpoints, supports MCP servers, and includes a Gradio UI.

- **+** Many LLM providers supported, including Ollama and any OpenAI-compatible custom endpoint
- **+** Bundles biomedical tools, databases and a retrievable Know-How protocol library
- **+** Adds external tools via MCP; local Gradio UI served on port 7860
- **+** Ships Biomni-R0 32B reasoning model and Biomni-Eval1 benchmark (433 instances)
- **−** Executes LLM-generated code with full system privileges; needs external sandboxing
- **−** Large conda environment via setup script plus ~11GB data lake download on first run
- **−** Release frozen at April 2025, so it differs from the hosted web platform
- **−** Some integrated tools and databases carry restrictive commercial licenses; some packages conflict

<sub>GPU optional · Needs conda, LLM API key (Anthropic by default), ~11GB data lake, Gradio 5.x (optional), SGLang (optional, for Biomni-R0) · Models: Anthropic, OpenAI, Azure OpenAI, Gemini, AWS Bedrock · port 7860 · [Repo](https://github.com/snap-stanford/biomni) · [▶️ Demo ↗](https://biomni.stanford.edu) · [🌐 Site ↗](https://biomni.stanford.edu) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/biomni/)</sub>

<a name="nof0"></a>
### #&#8288;102 [nof0](https://github.com/wquguru/nof0) <sub>score [6](../README.md#-how-we-rank "Score 6/100. Adoption: niche (11) · Freshness: quiet (9) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 2.8k · no license · Dec 2025</sub>

**Dashboard and backend for pitting LLM trading agents against each other on crypto.**

NOF0 is an open reimplementation of nof1.ai's Alpha Arena: multiple LLM agents each start with $10,000 and trade crypto, with PnL shown on a live dashboard. The Next.js frontend runs standalone and covers equity curves, positions, trades, model chat and a leaderboard. The Go-Zero backend and trading engine are partly finished (README states 70% and 80%), and backend startup instructions are not yet written.

- **+** Frontend runs on its own with npm, no backend needed
- **+** Includes a script to snapshot nof1.ai API data to local JSON
- **+** Separate Go packages for LLM providers, exchange, market data and prompts
- **+** MIT license stated in README
- **−** Backend marked unfinished; startup section says not yet developed
- **−** Trading engine stated at 80% and still being stabilized
- **−** No release published; license not detected by repo tooling
- **−** Built for live trading with real funds, not backtesting

<sub>no GPU · Needs Node.js, Go, Hyperliquid, ZenMux · Models: ZenMux LLM routing · port 3000 · [Repo](https://github.com/wquguru/nof0) · [📖 Docs ↗](https://wquguru.gitbook.io/nof0) · [🌐 Site ↗](https://nof1.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nof0/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
