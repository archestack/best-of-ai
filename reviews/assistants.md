# 🤖 Assistants reviews · Best of Open-Source AI

Personal AI assistants you run yourself and talk to through chat apps, with memory and the ability to act. Back to the [leaderboard](../README.md#-assistants).

<sub>🌐 Also on the web: [Assistants on archestack.com](https://archestack.com/best-of-ai/assistants/), each project on its own page.</sub>

<a name="ai-job-search"></a>
### 🥇 [ai-job-search](https://github.com/ai-job-search-dev/ai-job-search) <sub>score [97](../README.md#-how-we-rank "Score 97/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · MIT · Nov 2026</sub>

**Claude Code workflow that searches job boards and drafts tailored CVs and cover letters.**

A Claude Code project you fork and fill in with your profile. Slash commands (/setup, /scrape, /rank, /apply, /interview, /outcome) search job portals, score postings against a fit framework, and draft a LaTeX CV and cover letter that a second reviewer agent critiques before final PDF compilation. Portal skills target Danish boards, plus LinkedIn and freehire.me.

- **+** Drafter-reviewer pipeline compiles CV and cover letter PDFs with page-count and ATS checks
- **+** Postings pass a deterministic integrity gate for hidden text and injected instructions
- **+** Tracks applications end to end: /outcome, /gmail-sync, /notion-sync, /html-report, /interview
- **+** Portal CLIs are auto-discovered, and /add-portal scaffolds one for your own market
- **−** Requires Claude Code with a paid subscription or API credits; other agent tools only partly supported
- **−** Most portal skills target Denmark; other markets rely on LinkedIn, freehire.me or a custom portal
- **−** Needs Python 3.10+, Bun and a full LaTeX install, which is a heavy setup
- **−** A public fork exposes personal data in tracked files; a private repo is needed

<sub>no GPU · Needs Claude Code, Python 3.10+, Bun, LaTeX (lualatex, xelatex), pypdf or poppler (optional) · Models: Claude (via Claude Code) · [Repo](https://github.com/ai-job-search-dev/ai-job-search) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-job-search/)</sub>

<a name="career-ops"></a>
### 🥈 [career-ops](https://github.com/career-ops-hq/career-ops) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 82k · MIT · Nov 2026</sub>

**Job-search agent that scores listings, tailors CVs and drafts applications.**

Runs inside an AI coding CLI (Claude Code, Codex, OpenCode, Qwen and others). You paste a job URL or description, and it checks the posting is live, scores fit against your CV, and generates an ATS PDF CV, cover letter and draft answers. It never submits applications or sends email, and keeps data on your machine.

- **+** Drafts only: no auto-submit, and no mail transport in the code
- **+** No telemetry or backend; CV goes only to the AI provider you choose
- **+** Covers evaluation, tailored PDF CV, cover letter, contact drafts, tracker and interview prep
- **+** Portal scanner preconfigured for 100+ companies across Ashby, Greenhouse, Lever and Wellfound
- **−** Needs a separate AI CLI and provider; it does not run models itself
- **−** README says early runs are rough until it learns your profile
- **−** In-code check on CV rewording cannot catch every altered claim
- **−** PDF output needs Playwright Chromium; non-Debian Linux needs manual libraries

<sub>no GPU · Docker + Compose · Needs Node.js, An AI coding CLI (Claude Code, Codex, OpenCode, Qwen), Playwright Chromium (PDF generation) · Models: Claude Code, Codex, OpenCode, Qwen, local models (see docs/RUNNING_ON_A_BUDGET.md) · [Repo](https://github.com/career-ops-hq/career-ops) · [📖 Docs ↗](https://github.com/career-ops-hq/career-ops/blob/main/docs/SETUP.md) · [🌐 Site ↗](https://career-ops.org/manifesto?utm_source=readme) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/career-ops/)</sub>

<a name="openhuman"></a>
### 🥉 [openhuman](https://github.com/tinyhumansai/openhuman) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: ready (100) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · GPL-3.0 · Nov 2026</sub>

**Rust agent harness with desktop app, built-in memory and embeddable library.**

OpenHuman is a single-process Rust agent harness shipped as a desktop app, terminal app, headless server and an embeddable library (openhuman_embed). It bundles memory recalled with citations each turn, browser and desktop control, voice, workflows, MCP and skills, 119 Composio OAuth apps and 14 messaging channels. Models can be local (Ollama, LM Studio, MLX) or BYOK across 26 providers. It is marked early beta.

- **+** Usable as a typed Rust library, with no sidecar or daemon to run
- **+** Ships memory, voice, browser/desktop control, workflows and 14 channels in one app
- **+** Supports local models (Ollama, LM Studio, MLX) and BYOK for 26 providers
- **+** Public benchmark repo lets readers rerun its SWE-bench comparison against six harnesses
- **−** Marked early beta; README warns of rough edges
- **−** GPL-3.0 license may constrain embedding in proprietary products
- **−** Performance claims come from the project's own ten-task benchmark run
- **−** The 119 OAuth integrations go through Composio, a third-party service

<sub>GPU optional · Docker + Compose · Needs Composio (OAuth integrations), Ollama, LM Studio or MLX (optional, local models) · Models: Ollama, LM Studio, MLX, OpenAI-compatible APIs, 26 BYOK providers · [Repo](https://github.com/tinyhumansai/openhuman) · [📖 Docs ↗](https://tinyhumans.gitbook.io/openhuman/) · [🌐 Site ↗](https://tinyhumans.ai/openhuman) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openhuman/)</sub>

<a name="openclaw"></a>
### #&#8288;4 [OpenClaw](https://github.com/openclaw/openclaw) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 394k · MIT · Nov 2026</sub>

**Personal AI assistant reachable through Discord, Slack, Telegram, WhatsApp and more.**

OpenClaw runs a local Gateway that connects an AI assistant to 20+ messaging channels, including iMessage, Teams and Signal, with native apps for macOS, iOS, Android, Windows and Linux. State, memory and credentials stay on your hardware, and models and agent harnesses such as Claude, Codex or local models are swappable plugins. The same Gateway can serve one user or a shared team deployment.

- **+** Connects to 20+ messaging channels plus native apps on five desktop and mobile platforms
- **+** Model providers and agent harnesses are plugins, with hosted and local models supported
- **+** No paid tier or hosted service; only a daily version check phones home, and it can be disabled
- **+** Skills and plugins extend it through a plugin SDK and the ClawHub registry
- **−** Tools run on the host for the main session unless sandboxing is configured
- **−** Prompts still go to whichever model provider and chat platforms you configure
- **−** Requires Node 24.16+ or 26.1+; plain npm install from the source repo is unsupported
- **−** Exposing the Gateway or adding users needs careful reading of the security guides

<sub>GPU optional · Docker + Compose · Needs Node.js 24.16+ or 26.1+, model provider account or local model · Models: Claude, Codex, local models · [Repo](https://github.com/openclaw/openclaw) · [📖 Docs ↗](https://docs.openclaw.ai) · [🌐 Site ↗](https://openclaw.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openclaw/)</sub>

<a name="airi"></a>
### #&#8288;5 [airi](https://github.com/moeru-ai/airi) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · MIT · Nov 2026</sub>

**AI VTuber companion with VRM and Live2D avatars, voice, and game-playing.**

AIRI is a TypeScript/Vue monorepo for an animated AI character modeled on Neuro-sama, with VRM and Live2D bodies, speech input and multi-provider TTS. It ships as a browser PWA, an Electron desktop app and an iOS Capacitor app. The character can chat on Discord and Telegram and play Minecraft and Factorio, using hosted LLM APIs or local servers such as Ollama, vLLM and SGLang.

- **+** Runs as browser PWA, desktop app (Windows, macOS, Linux) and iOS app
- **+** Supports 25+ LLM providers via xsai, including Ollama, vLLM and SGLang
- **+** VRM and Live2D avatars with auto blink, look-at and idle eye movement
- **+** Desktop build uses CUDA or Apple Metal through candle without extra setup
- **−** README describes development as early stage; plugin system is WIP
- **−** Memory system (Memory Alaya) and in-browser WebGPU inference are unfinished on the roadmap
- **−** Game-playing is uneven: Factorio is WIP and Helldivers 2 co-play is not done
- **−** No Docker or compose files; self-hosting means building the pnpm monorepo or using releases

<sub>GPU optional · Needs Node.js, pnpm · Models: OpenAI, Anthropic Claude, Google Gemini, DeepSeek, Ollama · [Repo](https://github.com/moeru-ai/airi) · [▶️ Demo ↗](https://airi.moeru.ai) · [📖 Docs ↗](https://airi.moeru.ai/docs/en/) · [🌐 Site ↗](https://airi.moeru.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/airi/)</sub>

<a name="zeroclaw"></a>
### #&#8288;6 [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Nov 2026</sub>

**Single-binary Rust agent runtime that answers across 30+ chat channels.**

ZeroClaw is a Rust agent runtime configured with one TOML file. It connects to LLM providers (Anthropic, OpenAI, Ollama, about 20 others) and receives messages from 30+ channels such as Discord, Telegram, Matrix and email. The agent acts through shell, browser, HTTP, hardware and MCP tools, gated by a default supervised autonomy level and optional OS-level sandboxes.

- **+** Single Rust binary with one TOML config at ~/.zeroclaw/config.toml
- **+** 30+ channel adapters feed the same agent loop
- **+** Default supervised autonomy, with Landlock, Bubblewrap, Seatbelt or Docker sandboxes
- **+** Provider fallback chains and routing; any OpenAI-compatible endpoint works
- **−** Config needs provider, agent and risk-profile sections plus schema_version = 4
- **−** YOLO mode disables safety gates, so misconfiguration risk sits with the user
- **−** Memory is SQLite with embeddings; no other backends are listed
- **−** Dual MIT or Apache-2.0 licensing, with the name and logo trademarked

<sub>Docker + Compose · Needs SQLite · Models: Anthropic, OpenAI, Ollama, OpenAI-compatible endpoints · [Repo](https://github.com/zeroclaw-labs/zeroclaw) · [📖 Docs ↗](https://docs.zeroclaw.com/master/en/introduction.html) · [🌐 Site ↗](https://www.zeroclaw.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/zeroclaw/)</sub>

<a name="hermes-agent"></a>
### #&#8288;7 [Hermes Agent](https://github.com/nousresearch/hermes-agent) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 263k · MIT · Nov 2026</sub>

**Self-hosted agent with skill learning, memory and Telegram/Discord/Slack gateway.**

Hermes Agent is a Python agent from Nous Research that runs from a terminal UI or a single gateway process serving Telegram, Discord, Slack, WhatsApp, Signal and email. It keeps persistent memory, creates and refines skills after complex tasks, searches past sessions with FTS5, and runs cron-scheduled jobs. Model providers are switchable with `hermes model`, and tools can run on seven backends including local, Docker, SSH and Modal.

- **+** One gateway process serves Telegram, Discord, Slack, WhatsApp, Signal and email with shared history
- **+** Seven terminal backends, including Docker, SSH, Modal, Daytona and Vercel Sandbox
- **+** Built-in cron scheduler, FTS5 session search and agent-created skills compatible with agentskills.io
- **+** Works with Nous Portal, OpenRouter, OpenAI or any custom endpoint; MCP servers supported
- **−** Windows installer may trigger antivirus false positives on the bundled uv.exe
- **−** Installs via a curl-piped shell script rather than a pinned package on desktop
- **−** Skill self-improvement and user modeling behavior is described, but no benchmarks are given

<sub>no GPU · Docker + Compose · Needs Python, Node.js, ripgrep, FFmpeg, Honcho (user modeling) · Models: Nous Portal, OpenRouter, OpenAI, custom endpoints · [Repo](https://github.com/nousresearch/hermes-agent) · [📖 Docs ↗](https://hermes-agent.nousresearch.com/docs/) · [🌐 Site ↗](https://hermes-agent.nousresearch.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hermes-agent/)</sub>

<a name="nanobot"></a>
### #&#8288;8 [nanobot](https://github.com/hkuds/nanobot) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Nov 2026</sub>

**Self-hosted personal AI agent reachable from browser, terminal and chat apps.**

nanobot is a Python (3.11+) personal agent framework that you use through a bundled WebUI, a terminal client, or channels such as Telegram, Discord, Slack, Email and Mattermost. It works with files (PDF, docx, xlsx, pptx), shell, web fetch, MCP tools, cron automations, long-term memory (Dream) and multi-agent delegation. It needs an external model provider or local model server, and exposes a Python SDK and an OpenAI-compatible API.

- **+** Many channels: Telegram, Discord, Slack, WeChat, Email, Mattermost, Linear, Feishu, Teams
- **+** Built-in MCP, cron automations, long-running goals and PDF/Office file tools
- **+** Also usable as a Python SDK and OpenAI-compatible HTTP API
- **+** Platform wheels bundle the WebUI and a native terminal UI
- **−** Supplies no model; needs a provider account or local model server
- **−** Background gateway does not restart after reboot or crash without an OS service
- **−** Interrupted subagent tasks and missed scheduled runs are not replayed after restart
- **−** Source install needs Git and Bun; stable and source docs differ

<sub>no GPU · Docker + Compose · Needs Python 3.11+, model provider or local model server, Bun (source install only) · Models: OpenAI-compatible APIs, local LLMs · port 8765 · [Repo](https://github.com/hkuds/nanobot) · [📖 Docs ↗](https://nanobot.wiki/docs/latest/getting-started/nanobot-overview) · [🌐 Site ↗](https://nanobot.wiki/docs/latest/getting-started/nanobot-overview) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nanobot/)</sub>

<a name="astrbot"></a>
### #&#8288;9 [AstrBot](https://github.com/astrbotdevs/astrbot) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 47k · AGPL-3.0 · Nov 2026</sub>

**Agent chatbot platform connecting LLMs to QQ, Telegram, Slack and other chat apps.**

AstrBot is a Python chatbot platform that connects LLM providers to messaging apps such as QQ, Telegram, Feishu, DingTalk, Slack and Discord. It supports agents, MCP, skills, a knowledge base, personas and automatic context compression, with a WebUI and web chat. Behavior is extended through a plugin marketplace, and code execution can run in an agent sandbox.

- **+** Official adapters for 15 messaging platforms, including QQ, Telegram, Slack, Discord, LINE and Feishu
- **+** Works with OpenAI-compatible APIs, Anthropic, Gemini, Ollama and LM Studio, plus Dify, Coze and Bailian
- **+** Speech-to-text and text-to-speech integrations such as Whisper, SenseVoice, Edge TTS and FishAudio
- **+** Installs via uv, Docker or Compose, or a desktop app; has a WebUI and plugin marketplace
- **−** AGPL-3.0 license carries copyleft obligations for network-hosted modifications
- **−** Platform list leans toward Chinese services such as QQ and WeChat
- **−** WhatsApp support is listed as coming soon

<sub>no GPU · Docker + Compose · Needs Python 3.12+, uv, Docker (optional) · Models: OpenAI-compatible, Anthropic, Google Gemini, DeepSeek, Moonshot AI · [Repo](https://github.com/astrbotdevs/astrbot) · [📖 Docs ↗](https://docs.astrbot.app/) · [🌐 Site ↗](https://astrbot.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/astrbot/)</sub>

<a name="nanoclaw"></a>
### #&#8288;10 [nanoclaw](https://github.com/nanocoai/nanoclaw) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Nov 2026</sub>

**Personal assistant that runs Claude agents in per-agent Linux containers behind chat apps.**

NanoClaw is a small TypeScript host process that routes messages from chat channels (Slack, Telegram, Discord, WhatsApp, iMessage and others) to Claude Agent SDK agents running in separate Docker containers. Each agent group has its own CLAUDE.md, memory and mounts, and API credentials are injected by a gateway rather than held in the container. Channels and alternative providers are added as skills into your own fork.

- **+** Agents run in Docker containers and see only explicitly mounted directories
- **+** Credential gateway injects keys at request time, with per-agent policies and rate limits
- **+** Small codebase: one host process and two SQLite files per session
- **+** Per-agent-group provider choice: Claude, Codex, OpenCode, Cursor or Ollama via skills
- **−** Customization and setup recovery depend on Claude Code, not config files
- **−** Default path is built around Anthropic credentials and the Claude Agent SDK
- **−** Channel adapters are not in trunk; each needs an /add-<channel> skill
- **−** Prebuilt hardened image and managed Slack app require a free account

<sub>no GPU · Needs Docker, Node.js, pnpm, jq, Claude Code, OneCLI Agent Vault · Models: Claude (Agent SDK), OpenAI Codex, OpenRouter, Google, DeepSeek via OpenCode, Cursor Agent SDK, Ollama local models · [Repo](https://github.com/nanocoai/nanoclaw) · [📖 Docs ↗](https://docs.nanoclaw.dev) · [🌐 Site ↗](https://nanoclaw.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nanoclaw/)</sub>

<a name="cowagent"></a>
### #&#8288;11 [cowagent](https://github.com/zhayujie/cowagent) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · MIT · Nov 2026</sub>

**Agent assistant you chat with via web console, Telegram, Slack and more.**

CowAgent is a Python agent that plans tasks, runs built-in tools (file I/O, bash, browser, scheduler, web search) and MCP servers, and replies through the web console, Telegram, Slack, Discord, WeChat, Feishu, DingTalk, WeCom and QQ. It keeps three-tier memory with nightly distillation, a Markdown knowledge base, installable skills and multi-agent teams. Providers are set in the web console, with a Custom option for local models.

- **+** Many channels in one instance, including Telegram, Slack, Discord and Chinese IM platforms
- **+** Native MCP support via mcp.json (stdio, SSE) plus a skill marketplace
- **+** Three-tier memory with hybrid keyword and vector retrieval and a Markdown knowledge base
- **+** Chat, vision, image, ASR, TTS and embeddings can each route to a different provider
- **−** README warns agent mode uses substantially more tokens than regular chat
- **−** Local models only through a generic Custom provider, chat only
- **−** Server exposure needs web_host and web_password set manually
- **−** Hosted and enterprise options are tied to the vendor's LinkAI service

<sub>no GPU · Docker + Compose · Needs LLM provider API key or custom endpoint · Models: Claude, OpenAI, Gemini, DeepSeek, Qwen · port 9899 · [Repo](https://github.com/zhayujie/cowagent) · [📖 Docs ↗](https://docs.cowagent.ai/intro/index) · [🌐 Site ↗](https://cowagent.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cowagent/)</sub>

<a name="langbot"></a>
### #&#8288;12 [langbot](https://github.com/langbot-app/langbot) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Nov 2026</sub>

**Platform for running LLM agents as bots on Slack, Discord, Telegram and WeChat.**

LangBot runs AI bots on messaging platforms such as Discord, Telegram, Slack, LINE, QQ, WeChat, WeCom, Lark and DingTalk from one codebase. It adds a web management panel, multiple pipelines, a built-in knowledge base, plugins and MCP support, and can hand conversations to Dify, n8n, Coze or Langflow. It starts with `uvx langbot` on port 5300 or through Docker.

- **+** Covers about a dozen chat platforms, including QQ, WeCom, DingTalk and Lark, from one deployment
- **+** Web panel for configuring and monitoring bots, so no YAML editing is needed
- **+** Connects to Dify, n8n, Coze and Langflow, and to Ollama and LM Studio for local models
- **+** Exposes an MCP endpoint at /mcp and a CLI (lbctl), so other agents can manage it
- **−** Many supported platforms and providers are China-focused, which may matter for Western teams
- **−** Some integrations need an external service or account, such as Dify, n8n or Lark
- **−** Plugin market and cloud option are hosted services outside the self-hosted core

<sub>no GPU · Docker + Compose · Needs uv or Docker, LLM provider API, or local Ollama or LM Studio · Models: OpenAI, Anthropic, DeepSeek, Google Gemini, xAI · port 5300 · [Repo](https://github.com/langbot-app/langbot) · [📖 Docs ↗](https://langbot.app/docs/en/insight/guide) · [🌐 Site ↗](https://langbot.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langbot/)</sub>

<a name="qwenpaw"></a>
### #&#8288;13 [QwenPaw](https://github.com/agentscope-ai/qwenpaw) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · Apache-2.0 · Nov 2026</sub>

**Self-hosted personal AI assistant with memory, skills, and many chat channels.**

QwenPaw is a Python assistant you run yourself, with a web Console on port 8088. It keeps three-layer memory (via ReMe), runs skills, plugins and MCP tools, and answers through DingTalk, Lark, WeChat, Discord, Telegram, iMessage and QQ. It works with a built-in local runtime, Ollama, LM Studio or 14+ cloud providers, and includes sandbox and tool-guard protections.

- **+** One instance serves DingTalk, Lark, WeChat, Discord, Telegram, iMessage and QQ
- **+** Runs with built-in local runtime, Ollama, LM Studio or 14+ cloud providers
- **+** Includes Tool Guard, File Guard, Skill Scanner and a kernel-level sandbox
- **+** Install via pip, script, Docker, or a Tauri desktop app for Windows and macOS
- **−** Desktop app is Beta and the macOS build is not notarized
- **−** Requires Python >= 3.11 and < 3.14 for pip install
- **−** Many bundled subsystems (Hub, Mail, Creator, Data) add surface area to learn

<sub>GPU optional · Docker + Compose · Needs Python 3.11-3.13, Docker (optional), Ollama or LM Studio (optional) · Models: QwenPaw-Flash (2B/4B/9B/35B-A3B/27B), Ollama, LM Studio, 14+ cloud providers · port 8088 · [Repo](https://github.com/agentscope-ai/qwenpaw) · [▶️ Demo ↗](https://platform.agentscope.io/) · [📖 Docs ↗](https://qwenpaw.agentscope.io/docs/channels) · [🌐 Site ↗](https://qwenpaw.agentscope.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwenpaw/)</sub>

<a name="inbox-zero"></a>
### #&#8288;14 [inbox-zero](https://github.com/elie222/inbox-zero) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · custom license · Nov 2026</sub>

**AI assistant that sorts Gmail and Outlook, drafts replies, and files attachments.**

Inbox Zero runs against a Gmail or Outlook account to organize mail by plain-English rules, pre-draft replies in your style, and save attachments to Google Drive or OneDrive. It also has bulk unsubscribe and archive, cold email blocking, meeting briefs, and a Slack or Telegram chat interface. A separate email client (web and Electron desktop) is included; the iOS app is not open source.

- **+** Supports both Gmail and Outlook, with rules written in plain English
- **+** Chat control from Slack or Telegram
- **+** Local dev mode needs no OAuth credentials or AI API keys
- **+** Self-host setup wizard via npx CLI, plus Docker images per release
- **−** License is detected as NOASSERTION, so terms need manual checking
- **−** Real use needs your own Google or Microsoft OAuth setup
- **−** iOS app is closed source; Android app is an older React Native build
- **−** Needs PostgreSQL and Redis alongside the Next.js app

<sub>no GPU · Docker + Compose · Needs Docker, Node.js 24+, PostgreSQL, Redis, Gmail or Outlook OAuth app · port 3000 · [Repo](https://github.com/elie222/inbox-zero) · [📖 Docs ↗](https://docs.getinboxzero.com) · [🌐 Site ↗](https://www.getinboxzero.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/inbox-zero/)</sub>

<a name="rowboat"></a>
### #&#8288;15 [rowboat](https://github.com/rowboatlabs/rowboat) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Nov 2026</sub>

**Desktop assistant that builds a Markdown knowledge graph from email and meetings.**

Rowboat is an Electron desktop app that indexes email, meetings and Slack into a local, Obsidian-style backlinked Markdown knowledge graph. It adds an email client, browser, meeting note-taker, background agents and a code mode that drives Claude Code or Codex. Spaces, backed by the self-hostable Harbor server on Postgres, let teammates share a channel and files while each person's own Rowboat answers @mentions locally.

- **+** Data stored as plain Markdown on your machine, editable and inspectable
- **+** Works with Ollama, LM Studio or hosted models via your own API key
- **+** Connects external tools through MCP servers or Composio
- **+** Harbor Spaces server is open source, with HTTP, WebSocket and MCP endpoints
- **−** Voice, web search and Composio each need separate third-party API keys
- **−** Google services require manual setup steps
- **−** Harbor contract is still v0; README warns of breaking changes
- **−** Hosted Spaces require a Rowboat account sign-in via Google or Microsoft

<sub>GPU optional · Needs Postgres (Harbor), Deepgram (optional), ElevenLabs (optional), Exa (optional), Composio (optional) · Models: Ollama, LM Studio, Hosted models via API key · port 4272 · [Repo](https://github.com/rowboatlabs/rowboat) · [▶️ Demo ↗](https://www.youtube.com/watch?v=et5yQABJ3xI) · [🌐 Site ↗](https://www.rowboatlabs.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rowboat/)</sub>

<a name="qm"></a>
### #&#8288;16 [qm](https://github.com/yc-software/qm) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Nov 2026</sub>

**Team agent harness for Slack and web with per-scope sandboxes.**

QM is a self-hosted agent for teams, reachable from Slack and a web UI. Each person and each room gets its own scoped memory, files, permissions, crons and durable sandbox, while a Postgres-backed core handles identity, policy and scheduling. The agent loop is Pi, which can use models from many providers, and deployment is driven by a `qm` CLI into your own cloud account.

- **+** Per-person and per-room scopes isolate memory, files, keychain view and sandbox
- **+** Org-wide security postures (Strict, Auto, Dangerous) plus audit log and command policy rules
- **+** Runs crons, watches and inbound webhooks while users are away
- **+** Not tied to one model vendor; admins choose which models are available
- **−** Requires Postgres and cloud infrastructure; deployment is multi-step via the qm CLI
- **−** Upstream accepts contributions only as written proposals in adrs/, not code
- **−** Command policy ships with no rules; operators must write their own
- **−** Needs Node 24.15+ and a separate deployment repository per organization

<sub>Docker · Needs Postgres, Node 24.15+, Slack (optional), Cloud account (Fly or AWS target) · Models: Multiple providers via Pi, Model gateway routing · [Repo](https://github.com/yc-software/qm) · [📖 Docs ↗](https://labs.ycombinator.com/qm/) · [🌐 Site ↗](https://labs.ycombinator.com/qm/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qm/)</sub>

<a name="ironclaw"></a>
### #&#8288;17 [IronClaw](https://github.com/nearai/ironclaw) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Sep 2026</sub>

**Rust assistant that sandboxes every untrusted tool in WebAssembly.**

IronClaw is a Rust take on the OpenClaw idea that runs untrusted tools in WebAssembly sandboxes with capability permissions, endpoint allowlists, host-side credential injection and leak scans. It exposes a REPL, HTTP webhooks, Telegram and Slack channels and a browser gateway with SSE/WebSocket streaming, runs cron and event routines, connects to MCP servers and keeps hybrid-search memory in PostgreSQL.

- **+** WASM sandbox with per-tool rate, memory, CPU and time limits
- **+** Secrets encrypted with AES-256-GCM, never exposed to tool code; full audit log
- **+** Describe a tool in chat and IronClaw builds it as a WASM module
- **+** No telemetry; onboard installs a background service on macOS and Linux
- **−** Requires PostgreSQL for persistence; SQLite is not an option
- **−** Installer needs a release tag chosen by hand; no latest channel
- **−** Slack and Telegram are configured only through the WebUI Extensions page
- **−** Windows has no background service; WebUI runs in the foreground via ironclaw serve

<sub>no GPU · Docker + Compose · Needs PostgreSQL · Models: OpenAI · [Repo](https://github.com/nearai/ironclaw) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ironclaw/)</sub>

<a name="xiaobei"></a>
### #&#8288;18 [xiaobei](https://github.com/teamwiseflow/xiaobei) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · custom license · Nov 2026</sub>

**Self-media marketing agent team on openclaw, controlled through WeChat.**

xiaobei is an openclaw-based agent team for small businesses. It writes and publishes content to WeChat Official Accounts, Xiaohongshu, Douyin, Kuaishou, TikTok, X and others. Separate crews handle video production, customer service and IT repair, and you drive them from WeChat, Feishu or WeCom. It installs from a prebuilt tarball script and defaults to Alibaba Bailian models for chat, image, TTS, ASR and video.

- **+** Drafts and publishes across WeChat, Xiaohongshu, Douyin, Kuaishou, TikTok, X and Weibo
- **+** Crews such as content-producer and it-engineer delegate to each other without user prompts
- **+** Smart-search covers 18 source types with no API key required
- **+** One-line install scripts for macOS, Linux and Windows bundle portable Node and pnpm
- **−** License is NOASSERTION with a custom LICENSE file, so reuse terms need checking
- **−** Defaults to Alibaba Bailian cloud models; README describes no local model setup
- **−** Windows needs Git Bash or WSL; install downloads about 140MB plus a 557MB Firefox build
- **−** Docs are Chinese-only; fixed-IP relay is a paid VIP Club service and WeCom needs awada rental

<sub>RAM ≥ 8 GB · no GPU · Docker + Compose · Needs openclaw, camoufox, Alibaba Bailian API key, WeChat, Feishu or WeCom, Git Bash or WSL on Windows · Models: Alibaba Bailian (Qwen, HappyHorse, Wan), Volcano Ark (Seedance, GLM), MiniMax, OpenAI-compatible embeddings · [Repo](https://github.com/teamwiseflow/xiaobei) · [🌐 Site ↗](https://openclaw-for-business.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xiaobei/)</sub>

<a name="obsidian-copilot"></a>
### #&#8288;19 [obsidian-copilot](https://github.com/logancyang/obsidian-copilot) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · AGPL-3.0 · Nov 2026</sub>

**Obsidian plugin that runs OpenCode, Claude Code and Codex agents on your vault.**

Copilot for Obsidian is a community plugin that adds an Agent chat to Obsidian, backed by OpenCode (downloaded and managed by the plugin), an existing Claude Code install, or Codex via the codex-acp adapter. Agents can read notes, use tools and create files with permissions you control. It also provides Projects, shared Skills, custom Commands, Quick Ask and Quick Chat, with models from Copilot-hosted plans, your own provider keys, or local endpoints.

- **+** Works with Claude Code, Codex or OpenCode using your existing logins, no Copilot plan required
- **+** BYOK supports cloud, local and OpenAI-compatible providers; keys go in the Obsidian Keychain, not data.json
- **+** Skills, Commands and Projects are shared across the installed agents
- **+** Quick Chat, Quick Ask and custom Commands also work on mobile
- **−** Agent mode is desktop-only because backends run as local processes
- **−** Multi-agent requests and hosted models need a paid Plus license
- **−** Backend for hosted features is closed source; hosted requests go to Brevilabs
- **−** Runs only inside Obsidian, so it is not usable standalone

<sub>GPU optional · Needs Obsidian, OpenCode, Claude Code or Codex (via @agentclientprotocol/codex-acp) · Models: OpenCode-reported models, Claude Code, Codex, OpenAI-compatible providers, local models · [Repo](https://github.com/logancyang/obsidian-copilot) · [📖 Docs ↗](https://github.com/logancyang/obsidian-copilot/blob/master/docs/index.md) · [🌐 Site ↗](https://www.obsidiancopilot.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/obsidian-copilot/)</sub>

<a name="octop"></a>
### #&#8288;20 [octop](https://github.com/tencentcloud/octop) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Nov 2026</sub>

**Multi-user, multi-agent assistant for web, CLI and chat apps like Telegram.**

Octop runs as a single Python process (FastAPI) serving a web dashboard, CLI, IM channels and cron jobs. Each user gets multiple agents ("experts") with their own workspace, providers, channels and memory, stored in SQLite by default or PostgreSQL. It also includes a knowledge base, OAuth and MCP connectors, browser and remote desktop control, and ACP delegation to coding agents.

- **+** Single process serves dashboard, CLI, IM channels and cron; state lives under ~/.octop/
- **+** Channels: Feishu, DingTalk, QQ, WeChat, Telegram, Discord and WeCom
- **+** JWT multi-user isolation, tool approval and shell command guardrails
- **+** Workspace backends: local disk, Docker sandbox, PostgreSQL or COS/S3; desktop apps available
- **−** AgentTeams is marked Beta; mobile client is closed beta
- **−** Install one-liner pipes a script hosted on Tencent COS into bash
- **−** Several bundled connectors target Tencent services
- **−** RAM need stated only as 'a few GB'; supported model providers not listed in this excerpt

<sub>no GPU · Docker + Compose · Needs Python 3.12+ (provisioned by uv), SQLite (default) or PostgreSQL, Chromium/Playwright (optional), Docker (optional) · port 8088 · [Repo](https://github.com/tencentcloud/octop) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/octop/)</sub>

<a name="brigade"></a>
### #&#8288;21 [brigade](https://github.com/spinabot/brigade) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Nov 2026</sub>

**Self-hosted crew of AI agents with shared memory, reachable from chat apps.**

Brigade is a Node.js gateway and terminal chat UI that runs multiple isolated agents arranged in an org chart, sharing a file-backed long-term memory called Tideline. Agents are reachable from WhatsApp, Telegram, Slack, Discord, iMessage and BlueBubbles, and can use cron jobs, sub-agents, skills and 1,000+ Composio app connectors. State lives under ~/.brigade/, with an optional self-hosted Convex backend.

- **+** Supports Anthropic, OpenAI, Gemini, OpenRouter, Ollama and any OpenAI-compatible endpoint, switchable mid-chat
- **+** Org-chart agent hierarchy with A2A policy, sub-agent fan-out and depth/child caps
- **+** Default filesystem storage under ~/.brigade/, no database needed; Convex is optional
- **+** Reuses Claude Code or Codex CLI logins, with privileged actions gated by approval
- **−** Install is a curl-pipe-to-shell script; no Docker or compose files detected
- **−** App connectors depend on a Composio platform key (ak_)
- **−** Video rendering needs a separate optional engine (headless Chrome, FFmpeg)
- **−** README is marketing-heavy; hardware requirements and RAM figures are not stated

<sub>no GPU · Needs Node.js 22.12+, Composio (optional), Convex (optional), Ollama (optional), headless Chrome and FFmpeg (optional, video) · Models: Anthropic, OpenAI, Gemini, OpenRouter, Groq · port 7777 · [Repo](https://github.com/spinabot/brigade) · [🌐 Site ↗](https://brigade.spinabot.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/brigade/)</sub>

<a name="rakazo"></a>
### #&#8288;22 [rakazo](https://github.com/elie222/rakazo) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · Apache-2.0 · Nov 2026</sub>

**Self-hosted AI assistant with persistent bots on sandboxed computers.**

Rakazo runs persistent bots that each keep their own conversations, memory, routines and history. Bots work on shared or private computers (Docker, E2B, Daytona, CreateOS, Boat, or a trusted local machine) with browser, terminal, file and desktop access. It ships as a web app, an Electron desktop app and iPhone and Android apps, and is in beta.

- **+** Bots can delegate to peer bots or short-lived subagents
- **+** Installer script sets up the Docker Compose stack with random secrets, no clone needed
- **+** Web, Electron, iOS and Android clients share one API
- **+** Integrations via Composio, Pipedream, remote MCP and OpenAPI, plus voice with your own keys
- **−** Marked beta by the project
- **−** Needs Docker with Compose and PostgreSQL; heavier than a single binary
- **−** Treg is usage-metered; hosted resale needs a written agreement
- **−** Voice and managed app catalogs depend on third-party keys and services

<sub>Needs Docker, PostgreSQL, OpenSSL, curl · Models: Bring-your-own model credentials via Pi, OpenRouter · port 5173 · [Repo](https://github.com/elie222/rakazo) · [🌐 Site ↗](https://rakazo.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rakazo/)</sub>

<a name="osaurus"></a>
### #&#8288;23 [osaurus](https://github.com/osaurus-ai/osaurus) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · MIT · Nov 2026</sub>

**Native macOS agent harness with memory, sandbox and tools over local or cloud models.**

Osaurus is a Swift app for Apple Silicon Macs that runs local MLX models or cloud providers and wraps them with per-agent prompts, memory, tools and a code sandbox. It serves OpenAI, Anthropic and Ollama compatible APIs, acts as an MCP server and client, and includes an on-device privacy filter for cloud requests. Agents can browse, run on schedules and be reached through an encrypted relay.

- **+** Native Swift app with MLX inference; works fully offline with local models
- **+** Agent code runs in an isolated Linux VM (macOS 26+) or a Seatbelt fallback
- **+** On-device privacy filter scrubs PII before cloud sends and blocks the send if anything leaks
- **+** Serves OpenAI, Anthropic and Ollama compatible APIs and acts as an MCP server and client
- **−** macOS 15.5+ on Apple Silicon only; no Linux or Windows build
- **−** Linux VM sandbox needs macOS 26; older systems get weaker Seatbelt confinement
- **−** Crash reporting via Sentry is on by default and must be turned off in settings
- **−** Built-in Orchestrator has no folder, sandbox or browser; file work needs a custom agent

<sub>GPU optional · Needs macOS 15.5+, Apple Silicon · Models: MLX, Apple Foundation Models, Liquid LFM, OpenAI, Anthropic · [Repo](https://github.com/osaurus-ai/osaurus) · [📖 Docs ↗](https://docs.osaurus.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/osaurus/)</sub>

<a name="trendradar"></a>
### #&#8288;24 [trendradar](https://github.com/sansan0/trendradar) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · GPL-3.0 · Nov 2026</sub>

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

<a name="agenticseek"></a>
### #&#8288;25 [agenticseek](https://github.com/fosowl/agenticseek) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · GPL-3.0 · Oct 2026</sub>

**Local agent that browses the web, writes code and plans tasks.**

AgenticSeek is a self-hosted Manus-style assistant that routes each request to a browser, coding or planning agent. It runs against local models via Ollama, LM Studio or OpenAI-compatible servers, or against cloud APIs such as OpenAI, Google, Deepseek and Anthropic. The web UI is served on port 3000, with SearxNG and Redis started through Docker Compose.

- **+** Runs fully local with Ollama, LM Studio or any OpenAI-compatible server such as llama.cpp
- **+** Browser agent uses bundled SearxNG for search, with a stealth-mode Selenium option
- **+** Writes and runs code in Python, C, Go and Java inside a configurable work directory
- **+** Also supports cloud providers: OpenAI, Google, Deepseek, Hugging Face, TogetherAI, OpenRouter, MiniMax
- **−** README calls it an early prototype; agent routing may pick the wrong agent
- **−** Web form filling is described as experimental and may fail
- **−** Voice input is experimental and CLI-only; speech is marked in progress
- **−** Prompts are tuned for Deepseek; OpenAI and Gemini models may handle browsing poorly

<sub>GPU optional · Docker + Compose · Needs Docker Compose, SearxNG, Redis, Python 3.10, Ollama or LM Studio (for local models) · Models: Ollama, LM Studio, OpenAI-compatible (llama.cpp), OpenAI, Google Gemini · port 3000 · README: alternative to Manus · [Repo](https://github.com/fosowl/agenticseek) · [🌐 Site ↗](https://fosowl.github.io/agenticSeek.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agenticseek/)</sub>

<a name="anymodelbot"></a>
### #&#8288;26 [anymodelbot](https://github.com/modelflare-ai/anymodelbot) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Nov 2026</sub>

**Multi-bot desktop assistant with memory, file access and chat-app channels.**

AnyModelBot is an Electron/Node.js app for Windows, macOS and Linux that runs several bots, each with its own persona, default model, workspace and Markdown memory. Bots chat in-app or via WeChat, Feishu, Telegram, Slack and Discord, read and write files, run commands in a sandbox, and ask before writing outside the workspace. Models come from the Modelflare gateway (pay per use) or direct official API keys.

- **+** Per-bot memory, persona and workspace, three permission levels, approval cards for outside writes
- **+** Connects to WeChat, Feishu, Telegram, Slack and Discord with shared account setup
- **+** Background tasks and scheduled rules with per-task budgets, quiet hours and daily message caps
- **+** Direct keys for OpenAI, Anthropic, Gemini, xAI, DeepSeek, Kimi, GLM, Qwen, MiniMax, Mistral
- **−** Default model route goes through hosted Modelflare, which keeps request logs
- **−** Image and video generation only work through Modelflare, not direct API keys
- **−** Chat channels handle one-to-one chats only; group chat exists only inside the app
- **−** Rules do not run while the computer is off; macOS computer use is Beta

<sub>no GPU · Docker · Needs Modelflare account or official provider API keys, Node.js 22.13+ and Go 1.26.8+ (source builds only), Python 3.10+ and FFmpeg (video studio bot only) · Models: Modelflare-hosted models, OpenAI, Anthropic, Google Gemini, xAI · port 3600 · [Repo](https://github.com/modelflare-ai/anymodelbot) · [📖 Docs ↗](https://github.com/modelflare-ai/AnyModelBot/blob/master/docs/development.md) · [🌐 Site ↗](https://anymodel.bot/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/anymodelbot/)</sub>

<a name="leon"></a>
### #&#8288;27 [leon](https://github.com/leon-ai/leon) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Nov 2026</sub>

**Self-hosted personal assistant with tools, layered memory and agent-style execution.**

Leon is a Node.js personal assistant that runs locally on Linux, macOS or Windows and serves a web app on port 5366. It runs in smart, controlled (deterministic native skills) or agent (step-by-step planning) mode, with tools, layered memory, and desktop and browser computer use. The 2.0 Developer Preview is on the develop branch; the legacy version is on master.

- **+** Three execution modes: smart, controlled (deterministic skills), and agent (step-by-step planning)
- **+** Layered memory for durable preferences, daily context and recent discussion
- **+** Supports both local and remote AI providers
- **+** Extensible through native skills, SKILL.md agent skills, toolkits and bridges
- **−** 2.0 is a Developer Preview; new documentation is not ready
- **−** Public docs site mostly describes the legacy architecture
- **−** Installs from source with pnpm; no Docker or release builds
- **−** Few contributors; developed mostly in spare time, so progress is uneven

<sub>Needs Node.js >= 24, pnpm, Python (bridges and tcp_server) · Models: local models, remote AI providers · port 5366 · [Repo](https://github.com/leon-ai/leon) · [🌐 Site ↗](https://getleon.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/leon/)</sub>

<a name="mika"></a>
### #&#8288;28 [mika](https://github.com/wangzan101/mika) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · Apache-2.0 · Nov 2026</sub>

**Android assistant that operates phone apps and the web from one sentence.**

Mika is a Kotlin Android app that takes a plain-language request and carries it out across other apps and a built-in browser. It reads the screen like a person and works on a hidden background screen, so the main display stays usable. There is no Mika server: requests go to the model provider you configure with an API key or account sign-in.

- **+** Drives any app by reading the screen, with no per-app integration or app APIs
- **+** Runs on a hidden background screen while you keep using the phone
- **+** Many provider presets plus a Custom endpoint, including Ollama and LM Studio
- **+** Ask mode confirms before payments; schedules, memory and learned skills included
- **−** Android only; phone control needs Android 12+, 14+ recommended
- **−** Phone control needs wireless debugging pairing, which can switch off on Wi-Fi change or reboot
- **−** Built-in app and website knowledge is written in Chinese
- **−** Linux sandbox for Python, Node and shell works only on arm64 devices

<sub>no GPU · Needs Android 11+ (12+ for phone control), Model provider API key or account sign-in, Wireless debugging pairing for app control · Models: OpenAI, Anthropic, Gemini, xAI, Mistral · [Repo](https://github.com/wangzan101/mika) · [📖 Docs ↗](https://github.com/wangzan101/Mika/blob/main/docs/README.en.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mika/)</sub>

<a name="orkas"></a>
### #&#8288;29 [orkas](https://github.com/orkas-ai/orkas) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (49) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · MIT · Nov 2026</sub>

**Desktop app where a Commander agent delegates to specialist and CLI agents.**

Orkas is a local-first Electron desktop app in which a Commander agent plans work and delegates it to 16 built-in specialists (research, video, office files, e-commerce) and to installed CLI agents: Claude Code, Codex, OpenCode, OpenClaw and Hermes-Agent. Projects hold goals, memory and files across conversations, with to-dos, auto-advance and scheduled automations. It runs from source on macOS, Windows or Linux.

- **+** Orchestrates Claude Code, Codex, OpenCode, OpenClaw and Hermes-Agent under one plan
- **+** Projects keep memory and files; to-dos, auto-advance and scheduled automations
- **+** Data stays on disk; model calls go direct to your provider or local endpoint
- **+** 16 bundled specialist agents plus a marketplace of 30+ more
- **−** Shared projects, cloud sync and web-app publishing only in the packaged app
- **−** Scheduled automations need the computer awake; missed runs catch up within 12 hours
- **−** Source first launch downloads Python, FFmpeg, whisper.cpp and a ~95 MB embedding model
- **−** Built-in Orkas model runs through a managed service and uses credits

<sub>no GPU · Needs Node 22.12+, Python 3 and C/C++ toolchain (native-module fallback), glibc 2.34+ on Linux · Models: Claude, OpenAI, Gemini, DeepSeek, Kimi · [Repo](https://github.com/orkas-ai/orkas) · [🌐 Site ↗](https://orkas.ai/?source=gh-orkas) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/orkas/)</sub>

<a name="sellbird"></a>
### #&#8288;30 [sellbird](https://github.com/ethanplusai/sellbird) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · AGPL-3.0 · Nov 2026</sub>

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

<a name="operit"></a>
### #&#8288;31 [operit](https://github.com/aaswordman/operit) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · LGPL-3.0 · Nov 2026</sub>

**Android AI agent app that controls the phone, browser and a terminal.**

Operit is a Kotlin Android app that connects cloud or local models to device tools: Accessibility, Shizuku or Root UI automation, a built-in browser agent, files, and an Ubuntu 24.04 ARM64 userspace via PRoot. It runs local models through MNN or llama.cpp (GGUF) and extends through ToolPkg, MCP and Skills. It also has graph-based memory, character cards and visual workflows.

- **+** Runs on-device: MNN and GGUF via llama.cpp, plus Ollama and LM Studio endpoints
- **+** Per-tool permission control; default setting asks before each tool call
- **+** Extensible through ToolPkg, MCP (uvx/npx), Skills and a unified marketplace
- **+** Includes Ubuntu 24.04 terminal, SSH/SFTP workspaces and a visual workflow builder
- **−** Android 8.0+ and ARM64 devices only; no iOS or desktop in this repo
- **−** Building requires external subpack.zip, jniLibs.zip and libs.zip archives plus a submodule
- **−** Some docs, such as script and ToolPkg guides, are in Chinese only
- **−** Marketplace, MCP, speech and drawing features may call third-party services

<sub>GPU optional · Needs Android 8.0+ (API 26), ARM64 device, Shizuku or Root (optional, for automation) · Models: OpenAI Chat/Responses, Anthropic, Gemini, MNN, GGUF (llama.cpp) · [Repo](https://github.com/aaswordman/operit) · [📖 Docs ↗](https://operit.app/) · [🌐 Site ↗](https://operit.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/operit/)</sub>

<a name="jev-chat-jarvis"></a>
### #&#8288;32 [jev-chat-jarvis](https://github.com/jev-chat/jev-chat-jarvis) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · MIT · Oct 2026</sub>

**Chat reply assistant that judges intent and risk before drafting replies.**

Reads a conversation on screen, works out the other person's intent and the risk in the moment, then drafts and ranks replies that fill into the message box. The Android apps in this repo overlay WhatsApp, QQ, Feishu and X via the accessibility service. Separate repos cover Windows, macOS and an iOS keyboard. Requests go only to the model provider you configure with your own key.

- **+** Never sends messages itself; it only fills the input box
- **+** Requests go only to your configured provider with your own key; no vendor server
- **+** Covers Android, Windows, macOS and iOS, MIT-licensed
- **+** Drafts are checked against the intent and risk judgment and ranked
- **−** Use inside WhatsApp, QQ, Feishu or X may breach their terms and risk bans
- **−** Chinese Android edition needs an ARM64 phone; macOS build is Apple Silicon only
- **−** iOS keyboard has no App Store build; you must compile it in Xcode
- **−** Windows, macOS and iOS code live in other repos; data handling documented there

<sub>Needs Model provider API key (user-configured), Android accessibility service and overlay permission · Models: User-configured model provider via own API key, Local model on macOS · [Repo](https://github.com/jev-chat/jev-chat-jarvis) · [🌐 Site ↗](https://chatjevs.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jev-chat-jarvis/)</sub>

<a name="ds-bot"></a>
### #&#8288;33 [ds-bot](https://github.com/fei2411/ds-bot) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Nov 2026</sub>

**Desktop app and DeepSeek Harness plugin for bots that collaborate in group chats.**

DS Bot is a desktop app and a plugin for DeepSeek Harness (DSH) for creating multiple bots, each with its own memory and model. Bots work together in group chats led by an admin bot, hand off tasks with @mentions, and can use MCP servers, connectors, local coding-agent CLIs, Office files and IM apps. It is a community project, not an official DeepSeek product.

- **+** Group chats with admin bot, @ handoffs, per-group memory and staged goals
- **+** Links bots to Telegram, WeChat, Feishu, DingTalk, WeCom, QQ, Discord, Slack with no open port
- **+** Data stays in the local DSH home folder; connector credentials never reach a bot
- **+** Installers for Windows, macOS, Linux, plus a DSH plugin and Docker image
- **−** Windows installer is unsigned and can be blocked by SmartScreen or Smart App Control
- **−** Labeled v0.3 preview
- **−** Built on DSH; the README names DeepSeek as the main model provider
- **−** Docker image is configured for linux/amd64 only; old-glibc systems must use Docker

<sub>no GPU · Docker + Compose · Needs DeepSeek Harness (bundled in desktop app), DeepSeek account or API key, Node.js 22.19+ (source run or DSH Web only) · Models: DeepSeek, Claude Code, Codex CLI, OpenCode and other ACP agents via Local agents · [Repo](https://github.com/fei2411/ds-bot) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ds-bot/)</sub>

<a name="ods"></a>
### #&#8288;34 [ods](https://github.com/osmantic/ods) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · Apache-2.0 · Nov 2026</sub>

**Installer that sets up a local AI server stack on Linux, macOS and Windows.**

ODS installs and wires together llama-server inference, Open WebUI, a control dashboard, Whisper and Kokoro voice, n8n, Qdrant, SearXNG and ComfyUI, picking a model for the detected hardware. It runs on Linux, macOS Apple Silicon and Windows via WSL2, with an optional cloud mode using OpenAI, Anthropic or Together. The current release is a V3 pre-release installed from the main branch.

- **+** One command installs inference, chat UI, dashboard, voice, workflows, RAG and image generation
- **+** Detects GPU and picks a model; bootstrap mode lets you chat while the full model downloads
- **+** Supports NVIDIA, AMD Strix Halo and Apple Silicon Metal; cloud mode for hosts without a GPU
- **+** States no telemetry; default outbound traffic limited to downloads, release checks and agent web searches
- **−** V3 pre-release: installers pull current main, not a signed release
- **−** Requires Docker on Linux and macOS; Windows needs WSL2 and Docker Desktop
- **−** Intel Arc (SYCL) support is experimental
- **−** License is Apache 2.0 plus a Pixel ODS-only term; check LICENSING.md

<sub>GPU optional · Needs Docker, WSL2 (Windows), Docker Desktop (Windows/macOS) · Models: GGUF, llama.cpp, OpenAI API, Anthropic API, Together API · port 3001 · [Repo](https://github.com/osmantic/ods) · [▶️ Demo ↗](https://youtu.be/nO8xFNHX-HA) · [🌐 Site ↗](https://osmantic.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ods/)</sub>

<a name="opensquilla"></a>
### #&#8288;35 [opensquilla](https://github.com/tokenrhythm/opensquilla) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Nov 2026</sub>

**Personal AI agent that routes each turn to the cheapest capable model.**

OpenSquilla is a Python agent that runs through a CLI, a Web UI, a desktop app and chat channels, all sharing one turn loop. An on-device router (SquillaRouter) sends each turn to the cheapest model that can handle it, and it adds persistent memory, a layered sandbox and built-in web search. It connects to 20+ LLM providers including OpenAI, Anthropic, Ollama, OpenRouter and Gemini.

- **+** Local model router picks a cheaper model per turn to cut token spend
- **+** Same turn loop for CLI, Web UI and chat channels
- **+** Supports 20+ providers, including Ollama for local models
- **+** Desktop installers for macOS and Windows, plus a uv-based terminal install
- **−** Usage statistics reporting is enabled by default and must be turned off
- **−** Router needs native libraries (libomp, VC++ runtime) on terminal installs, or it falls back
- **−** Source install needs Git LFS, Node.js 22.12+ and uv
- **−** Desktop installers cover only macOS Apple Silicon and Windows x64

<sub>no GPU · Docker + Compose · Needs Python 3.12+, uv, Git LFS (source install), Node.js 22.12+ (source install) · Models: OpenAI, Anthropic, OpenRouter, Ollama, DeepSeek · [Repo](https://github.com/tokenrhythm/opensquilla) · [🌐 Site ↗](https://opensquilla.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opensquilla/)</sub>

<a name="openagent"></a>
### #&#8288;36 [openagent](https://github.com/the-open-agent/openagent) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · Apache-2.0 · Nov 2026</sub>

**Self-hosted AI assistant with RAG, browser-use agents and MCP tools.**

OpenAgent is a Go application that combines a chat front-end, a document knowledge base and agent loops in one service. Agents can drive a browser, run shell commands, edit Office files, search the web and call MCP servers (SSE, Stdio, StreamableHTTP). It connects to 30+ model providers and adds SSO, multi-tenancy, audit logs and a BPMN-style workflow editor.

- **+** Ships as a single binary; native Windows support without WSL or Docker
- **+** 30+ model providers including Ollama, switchable per conversation
- **+** Agent tool calls show arguments and return values step by step
- **+** Built-in SSO (OIDC, OAuth2, LDAP, SAML), multi-tenancy, audit logs and usage tracking
- **−** Shell and browser tools run from the agent loop; sandboxing is not described
- **−** Broad scope (RAG, workflows, admin, media) makes it heavier than a focused assistant
- **−** No chat-app integrations such as Telegram or Discord are listed

<sub>no GPU · Docker + Compose · Compose runs MySQL · Models: OpenAI, Azure OpenAI, Anthropic Claude, Google Gemini, DeepSeek · port 14000 · [Repo](https://github.com/the-open-agent/openagent) · [▶️ Demo ↗](https://demo.openagentai.org) · [📖 Docs ↗](https://www.openagentai.org) · [🌐 Site ↗](https://www.openagentai.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openagent/)</sub>

<a name="moltis"></a>
### #&#8288;37 [Moltis](https://github.com/moltis-org/moltis) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · MIT · Oct 2026</sub>

**Self-hosted personal agent server in Rust with chat channels and sandboxing.**

Moltis is a single Rust binary that runs a persistent agent server. It connects LLM providers to a web UI and chat channels (Telegram, Signal, Discord, Slack, Teams, Matrix, Nostr), keeps sessions and memory in SQLite, and runs commands in Docker, Podman or Apple Container sandboxes. It also has voice I/O, cron scheduling, MCP servers and a skill system.

- **+** Single Rust binary with no Node.js or Python runtime; lightweight feature flag for Raspberry Pi
- **+** Commands run in per-session containers (Docker, Podman, Apple Container), not on the host
- **+** Many channels built in: Telegram, Signal, Discord, Slack, Teams, Matrix, Nostr, WhatsApp, web PWA
- **+** Password, passkey and API key auth, plus an encrypted vault for secrets
- **−** Large codebase (~270K lines, 59 crates) despite the auditability claim
- **−** Source build needs just and Node.js for Tailwind CSS
- **−** Docker example mounts the host Docker socket, which widens container privileges
- **−** README names few providers (Codex, Copilot, Local); full list unknown

<sub>no GPU · Docker + Compose · Needs Docker, Podman or Apple Container (sandbox), just and Node.js (source build only) · Models: OpenAI Codex, GitHub Copilot, Local models · port 13131 · [Repo](https://github.com/moltis-org/moltis) · [📖 Docs ↗](https://docs.moltis.org) · [🌐 Site ↗](https://moltis.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moltis/)</sub>

<a name="picoclaw"></a>
### #&#8288;38 [PicoClaw](https://github.com/sipeed/picoclaw) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Aug 2026</sub>

**Go assistant agent that runs in under 20 MB on $10 boards.**

PicoClaw is a single Go binary for x86_64, ARM64, MIPS, RISC-V and LoongArch that runs a personal agent in roughly 10 to 20 MB of RAM and boots in under a second on a 0.6 GHz core. It talks to 30+ LLM providers via a model_list config, supports MCP, image input and rule-based model routing, and reaches Telegram, Discord, Matrix, IRC and WeChat. A WebUI launcher on port 18800 handles setup.

- **+** Single static binary for RISC-V, ARM, MIPS and x86; runs on $10 Linux boards
- **+** 10 to 20 MB resident memory; boots in under 1 s on 0.6 GHz
- **+** 30+ providers including OpenAI, Anthropic, Gemini, Ollama, vLLM, Bedrock and Copilot
- **+** Android APK turns old phones into an assistant host
- **−** README warns of unresolved security issues; not for production before v1.0
- **−** Gateway binds 127.0.0.1 by default; Docker needs PICOCLAW_GATEWAY_HOST=0.0.0.0
- **−** AWS Bedrock support requires a custom build with -tags bedrock
- **−** No root Dockerfile; compose file lives under docker/ and needs a first-run bootstrap

<sub>RAM ≥ 0.02 GB · no GPU · Docker + Compose · Models: OpenAI, Anthropic, Google Gemini, OpenRouter, DeepSeek · port 18800 · [Repo](https://github.com/sipeed/picoclaw) · [📖 Docs ↗](https://docs.picoclaw.io/) · [🌐 Site ↗](https://picoclaw.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/picoclaw/)</sub>

<a name="nullclaw"></a>
### #&#8288;39 [nullclaw](https://github.com/nullclaw/nullclaw) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (43) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · MIT · Oct 2026</sub>

**Personal AI assistant runtime in a single 678 KB static Zig binary.**

NullClaw is a self-hosted autonomous assistant written in Zig that connects 50+ model providers to 19 chat channels such as Telegram, Discord, Signal, Slack and Matrix. It ships 35+ tools, subagents, MCP support, cron and heartbeat tasks, and SQLite-backed memory with FTS5 plus vector hybrid search. Config follows the OpenClaw layout, and a migrate command imports existing OpenClaw memory.

- **+** README reports a 678 KB static binary, about 1 MB peak RSS, and under 8 ms startup
- **+** Gateway binds 127.0.0.1 by default, requires pairing, and encrypts API keys with ChaCha20-Poly1305
- **+** Sandbox backends: Landlock, Firejail, Bubblewrap and Docker, auto-detected
- **+** Memory backends include SQLite, Markdown, PostgreSQL, Redis, ClickHouse and LanceDB
- **−** Source builds need exactly Zig 0.16.0; other versions are unsupported
- **−** Benchmark comparisons are the project's own, from a single macOS arm64 run
- **−** Nostr channel requires the external nak tool in PATH
- **−** Vertex AI service-account auth requires openssl in PATH

<sub>no GPU · Docker + Compose · Needs Zig 0.16.0 (source builds), nak (Nostr channel), openssl (Vertex service-account auth) · Models: OpenRouter, Anthropic, OpenAI, Azure OpenAI, Gemini · port 3000 · [Repo](https://github.com/nullclaw/nullclaw) · [📖 Docs ↗](https://nullclaw.github.io) · [🌐 Site ↗](https://nullclaw.github.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nullclaw/)</sub>

<a name="invisible-dots"></a>
### #&#8288;40 [invisible_dots](https://github.com/feder-cr/invisible_dots) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 48 · MIT · Nov 2026</sub>

**Self-hosted agent that works on its own VM desktop with a patched Firefox.**

invisible_dots runs each agent (a "Dot") on its own hardware-accelerated QEMU VM with a Linux desktop, persistent disk and a patched Firefox that keeps per-identity logins. Dots write their own notes and skills, accept MCP servers, queue tasks and recurring automations, and gate tools with allow/ask/deny permissions. It is reachable via web UI, CLI, HTTP API, Telegram and optional WhatsApp, and uses an OpenRouter key for models. Status is alpha.

- **+** Each Dot gets its own VM with desktop, persistent disk and sleep/wake on demand
- **+** Per-tool allow/ask/deny permissions, with pending asks kept in an Inbox across restarts
- **+** Accepts user-declared MCP servers and reaches the agent via web, CLI, API, Telegram
- **+** Crash-safe: accepted messages and tasks survive kill -9, and cut-short tool calls are not rerun
- **−** Marked alpha in the README badge
- **−** Requires x86-64 hardware virtualization plus Node 24+, Go 1.25+ and QEMU
- **−** No Docker or Compose files; setup is built from source
- **−** Model access documented only via an OpenRouter key; local models not mentioned

<sub>no GPU · Needs Node 24+, Go 1.25+, Git, QEMU, KVM or Windows Hypervisor Platform, OpenRouter API key · Models: OpenRouter · port 3000 · [Repo](https://github.com/feder-cr/invisible_dots) · [📖 Docs ↗](https://github.com/feder-cr/invisible_dots/blob/main/docs/guide.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/invisible-dots/)</sub>

<a name="cloddsbot"></a>
### #&#8288;41 [cloddsbot](https://github.com/alsk1992/cloddsbot) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · MIT · Sep 2026</sub>

**Chat-driven trading assistant for prediction markets, crypto and perp futures.**

Clodds is a Node.js/TypeScript gateway that lets you place and monitor trades by chatting with Claude. It connects to 21 messaging channels plus a built-in WebChat, 10 prediction markets, 7 perpetual futures exchanges, and Solana and EVM DEXs. It adds a risk engine, arbitrage detection, copy trading and backtesting, and can run as an MCP server for Claude Desktop and Claude Code.

- **+** Trades on Polymarket, Kalshi, Betfair and others, plus Binance, Bybit and Hyperliquid perps
- **+** Risk controls include circuit breaker, daily loss limits and kill switch; arbitrage defaults to dry-run
- **+** `clodds mcp` exposes its skills as MCP tools for Claude Desktop and Claude Code
- **+** Local SQLite storage, encrypted credentials (AES-256-GCM), shell commands need approval
- **−** Claude is the primary model; the other seven providers are secondary
- **−** Live trading with leverage up to 200x puts real funds at risk
- **−** Very broad scope (token launches, Bittensor mining, marketplace) widens the attack surface
- **−** Built in 12 days for a hackathon; README gives no test or audit information

<sub>no GPU · Docker + Compose · Needs Node.js 22+, Anthropic API key, SQLite, LanceDB, PostgreSQL (optional, analytics) · Models: Claude, GPT-4, Gemini, Groq, Together · port 18789 · [Repo](https://github.com/alsk1992/cloddsbot) · [▶️ Demo ↗](https://cloddsbot.com/onboard.mp4) · [🌐 Site ↗](https://cloddsbot.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cloddsbot/)</sub>

<a name="goutoujunshi"></a>
### #&#8288;42 [goutoujunshi](https://github.com/shengjidaguai-china/goutoujunshi) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · MIT · Sep 2026</sub>

**Codex Skill that analyzes relationship chats and suggests concrete next steps.**

Goutoujunshi is a Codex Skill for dating and relationship advice, covering attraction, conflict, breakup and reconciliation. It builds profiles of the user and the other person, separates facts from inference, reads chat screenshots or exports (optionally via ChatLab), and returns a sendable message, an invitation plan and stop conditions. With explicit consent it keeps a limited local memory through a Python script.

- **+** Consent-gated local memory that can be viewed, paused, revoked or cleared
- **+** Separates facts, inference and unknowns when analyzing chat screenshots or exports
- **+** Knowledge base of 135 references classified by evidence strength
- **+** Includes validate_skill.py integrity check and a CI validation workflow
- **−** Documentation is primarily in Chinese; English is in a separate README_EN
- **−** Tied to Codex-style Skill installation; no standalone app or API
- **−** No tagged releases; installed by asking an AI assistant to download the repo
- **−** No evaluation of advice quality is given; output depends on the host model

<sub>Needs Codex-compatible AI assistant, ChatLab (optional) · [Repo](https://github.com/shengjidaguai-china/goutoujunshi) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/goutoujunshi/)</sub>

<a name="khoj"></a>
### #&#8288;43 [Khoj](https://github.com/khoj-ai/khoj) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: widely used (85) · Freshness: active (93) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · AGPL-3.0 · Aug 2026</sub>

**Personal assistant that chats with your documents and the web.**

Khoj answers questions from the web and your files (PDF, Markdown, org-mode, Word, Notion, images) using local or hosted LLMs such as llama3, qwen, gemma, mistral, GPT, Claude, Gemini and DeepSeek. It is reachable from a browser, Obsidian, Emacs, desktop and phone apps and WhatsApp, supports custom agents with their own knowledge and tools, and runs scheduled automations that deliver newsletters by email.

- **+** Clients for browser, Obsidian, Emacs, desktop, phone and WhatsApp
- **+** Reads PDF, Markdown, org-mode, Word, Notion and image files
- **+** Hosted instance at app.khoj.dev to try before self-hosting
- **+** Custom agents with their own knowledge, persona, model and tools
- **−** AGPL-3.0 license
- **−** README gives no hardware requirements or ports; setup lives entirely in the docs
- **−** Maintainers now promote a newer project, Pipali, at the top of the README
- **−** Enterprise and cloud tiers exist; feature parity with self-hosting is not stated

<sub>Docker + Compose · Compose runs PostgreSQL, SearXNG · Models: llama3, qwen, gemma, mistral, OpenAI GPT · [Repo](https://github.com/khoj-ai/khoj) · [▶️ Demo ↗](https://app.khoj.dev) · [📖 Docs ↗](https://docs.khoj.dev) · [🌐 Site ↗](https://khoj.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/khoj/)</sub>

<a name="openmuse"></a>
### #&#8288;44 [openmuse](https://github.com/copilotkit/openmuse) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (30) · Freshness: active (100) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · MIT · Oct 2026</sub>

**Personal agent with browser, terminal and durable tasks for mobile and web.**

OpenMuse is a personal-agent app built on CopilotKit React Native (Expo) with a Hono API, a SQL-leased task worker and a Playwright Chromium worker with persistent profiles. The agent can browse, fill PDFs, search the web and optionally run commands in a Docker Linux container. Gmail and Calendar writes require a stored review first. The README labels it alpha.

- **+** Take-control console lets you continue the agent's Chromium session yourself
- **+** Tasks support pause, resume, retry and approvals; SQL leases recover interrupted work
- **+** Each Gmail or Calendar write needs its own stored review; credentials encrypted at rest
- **+** Embedded PGlite by default, so no separate database for local use
- **−** Needs a CopilotKit Intelligence project key in every mode; that service is not MIT-licensed
- **−** Alpha: live Google accounts and open-ended reasoning need extra configuration
- **−** Single owner behind a shared access key; not multi-tenant
- **−** Terminal container has no network and a 30-second command limit; no graphical desktop

<sub>no GPU · Needs CopilotKit Intelligence API key, Node 24, pnpm 11.19.0, Playwright Chromium, Docker (optional, Linux computer), Google OAuth client (optional), Parallel Search MCP (web search) · Models: OpenAI, Anthropic, Google · port 8081 · [Repo](https://github.com/copilotkit/openmuse) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmuse/)</sub>

<a name="openduet"></a>
### #&#8288;45 [openduet](https://github.com/copilotkit/openduet) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · MIT · Nov 2026</sub>

**Proactive personal agent with its own browser, morning brief and approval prompts.**

OpenDuet is a self-hosted personal agent built on OpenBot and CopilotKit. It reads Gmail and Google Calendar, posts a daily brief, sorts mail into needs-you and can-wait, and runs tasks in a per-Bot computer with a browser, files and shell. Sending, paying or deleting pauses for approval. It is a community-maintained starter, with branding, Bots and skills in one folder.

- **+** Approval prompts (Refuse, Allow once, Always allow) gate actions that send, pay, sign or delete
- **+** Each Bot gets its own Docker computer with browser, /workspace and shell
- **+** Branding, Bots, channels, model and skills live in one copyable folder
- **+** Passwords go through a masked secret box and never enter the agent conversation
- **−** Requires a CopilotKit Intelligence project; server will not start without its key
- **−** README labels it early development; no deploy guide and no published image
- **−** Default model is OpenAI; others limited to Anthropic or OpenAI-compatible endpoints
- **−** Team sign-in, Slack and Teams come from OpenBot, not this repo

<sub>no GPU · Needs Docker, Bun 1.3+, Node (npx), Postgres, CopilotKit Intelligence project, Model API key · Models: OpenAI, Anthropic, OpenAI-compatible endpoints · port 3010 · [Repo](https://github.com/copilotkit/openduet) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openduet/)</sub>

<a name="shell-gpt"></a>
### #&#8288;46 [shell_gpt](https://github.com/ther1d/shell_gpt) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: popular (60) · Freshness: active (88) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Jul 2026</sub>

**Command-line tool that generates shell commands and code from LLM prompts.**

ShellGPT installs as `sgpt` via pip and sends prompts from arguments or stdin to an LLM, defaulting to the OpenAI API. It generates OS- and shell-aware commands with an execute/describe/abort prompt, code-only output, named chat sessions, a REPL mode, custom roles, and function calling. Local models work through backends such as Ollama, but the README says it is not optimized for them.

- **+** Reads stdin and redirects, so it composes with pipes such as `git diff | sgpt`
- **+** Shell mode detects OS and `$SHELL` and asks to execute, describe or abort
- **+** Bash and Zsh hotkey integration puts suggested commands into the input line
- **+** Custom roles and Python function definitions live in `~/.config/shell_gpt`
- **−** README says it is not optimized for local models and may not work as expected
- **−** Defaults to the paid OpenAI API and needs an API key
- **−** Function calling can run destructive shell commands; README warns to use at your own risk
- **−** Request cache applies only to OpenAI API requests

<sub>no GPU · Docker · Needs OpenAI API key or a local backend such as Ollama, Python and pip · Models: OpenAI GPT models, Ollama (via LiteLLM) · [Repo](https://github.com/ther1d/shell_gpt) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/shell-gpt/)</sub>

<a name="spacebot"></a>
### #&#8288;47 [Spacebot](https://github.com/spacedriveapp/spacebot) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (6) · Freshness: active (99) · Maintenance: patchy (42) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · custom license · Sep 2026</sub>

**Multi-user agent harness for Discord, Slack and Telegram communities.**

Spacebot is a Rust agent server built for many concurrent users: channel processes hold conversations while branches think and workers execute, so replies never block on tool calls. It ships adapters for Discord, Slack, Telegram, Signal, Mattermost and email, a typed memory graph in SQLite and LanceDB, a task system with approvals, cron jobs, and model routing over any OpenAI- or Anthropic-compatible endpoint.

- **+** Per-guild, per-channel and per-DM permissions; identity anchors track users across platforms
- **+** Compaction runs in a separate worker, so long sessions never pause the conversation
- **+** Tasks created autonomously wait in pending_approval; nothing runs unapproved
- **+** Embedded SQLite and LanceDB only; no external database service
- **−** Licensed FSL-1.1-ALv2 (source-available), not an OSI license
- **−** Coding tasks run only on the built-in worker or OpenCode today
- **−** Web search requires a Brave Search API key
- **−** Browser automation needs headless Chrome

<sub>no GPU · Docker · Models: OpenAI-compatible, Anthropic-compatible, Ollama, Azure OpenAI, Gemini · [Repo](https://github.com/spacedriveapp/spacebot) · [📖 Docs ↗](https://docs.spacebot.sh) · [🌐 Site ↗](https://spacebot.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/spacebot/)</sub>

<a name="wechat-intelligence-hub"></a>
### #&#8288;48 [wechat-intelligence-hub](https://github.com/rion-wu-tech/wechat-intelligence-hub) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (7) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · AGPL-3.0 · Oct 2026</sub>

**Turns local WeChat history into daily reports, follow-ups and commitments.**

Read-only toolkit that indexes a user's own local WeChat databases and produces Markdown and interactive HTML reports: daily digests, pending replies, commitments, business leads and per-contact summaries. It ships as two Codex skills (wechat-cli, wechat-intelligence-hub), a deterministic Python engine and a clean-room Reader using SQLCipher. Full history needs user-authorized key material; the repo does not bundle a key-extraction tool.

- **+** Read-only Reader: no message sending, no WeChat UI automation, no hooking in the core
- **+** Outputs Markdown and searchable interactive HTML for any user-specified time range
- **+** Fictional demo runs without WeChat access (run_demo.sh)
- **+** Personal profile and WeChat labels are used to rank report items
- **−** Full database mode needs the user's own key material; first-time capture unverified on new machines
- **−** Windows first-time key acquisition is not merged; macOS path untested on fresh machines
- **−** Preview release (v0.9.2-preview.2); may break when WeChat updates
- **−** AGPL-3.0; closed-source use needs a separate commercial license

<sub>Needs Codex, SQLCipher, Zstandard, Pandoc (HTML reports), nh3 (HTML sanitizing), Local WeChat database and key material · [Repo](https://github.com/rion-wu-tech/wechat-intelligence-hub) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/wechat-intelligence-hub/)</sub>

<a name="mimiclaw"></a>
### #&#8288;49 [mimiclaw](https://github.com/memovai/mimiclaw) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (26) · Freshness: active (95) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · MIT · Oct 2026</sub>

**C firmware that runs a Telegram-controlled AI agent on an ESP32-S3 board.**

MimiClaw is ESP-IDF firmware that turns an ESP32-S3 board with 16 MB flash and 8 MB PSRAM into a personal assistant reached through Telegram. It runs a ReAct agent loop against Anthropic or OpenAI APIs, with web search, cron scheduling and a periodic heartbeat. Memory, chat history and config are kept as plain text files on the chip's flash.

- **+** Runs on a single ESP32-S3 board with no Linux or Node.js; written in C
- **+** Memory, personality and tasks are plain editable files (SOUL.md, MEMORY.md, HEARTBEAT.md)
- **+** Switches between Anthropic and OpenAI at runtime via serial CLI, stored in NVS
- **+** Persistent cron jobs and a 30-minute heartbeat let the agent act unprompted
- **−** Requires specific hardware: ESP32-S3 with 16 MB flash and 8 MB PSRAM
- **−** Needs ESP-IDF v5.5+ toolchain; build-time secrets changes require a full rebuild
- **−** Telegram is the only chat channel; models are remote APIs, no local inference
- **−** Small tool set: web search, current time and cron management only

<sub>no GPU · Needs ESP32-S3 board (16 MB flash, 8 MB PSRAM), ESP-IDF v5.5+, Telegram bot token, Anthropic or OpenAI API key, Tavily or Brave Search API key (optional) · Models: Anthropic Claude, OpenAI GPT · port 18789 · [Repo](https://github.com/memovai/mimiclaw) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mimiclaw/)</sub>

<a name="wechat-bot"></a>
### #&#8288;50 [wechat-bot](https://github.com/wangrongding/wechat-bot) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (58) · Freshness: recent (70) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Sep 2026</sub>

**Wechaty bot that routes WeChat, Lark, Telegram and WhatsApp chats to LLMs.**

Node.js CLI (`wb`) that logs into WeChat by QR code through Wechaty and replies to allowlisted contacts and groups using a chosen backend such as ChatGPT, DeepSeek, Ollama, Claude, Dify or the Pi agent. It also handles Lark events, Telegram Bot API polling and WhatsApp Cloud API webhooks, and wraps OpenCLI `wx-cli` for local WeChat history and group or friend analysis.

- **+** Many backends via --serve: ChatGPT, DeepSeek, Ollama, Claude, Kimi, Doubao, Tongyi, Dify, Pi
- **+** Same agent works over WeChat, Lark, Telegram and WhatsApp
- **+** Contact and group allowlists plus mention triggers limit unwanted replies
- **+** Local group and friend statistics work without calling any LLM
- **−** README warns the default WeChat Web protocol can trigger account warnings or bans
- **−** Underlying wechaty is not actively maintained; padlocal author stopped maintaining it
- **−** Non-text messages are not sent to the reply pipeline
- **−** Last release was 2024-03-26; no persistent memory described

<sub>no GPU · Docker · Needs Node.js >= 18, Wechaty, OpenCLI wx-cli, lark-cli, Pi agent · Models: ChatGPT, DeepSeek, Ollama, Claude, Kimi · port 3000 · [Repo](https://github.com/wangrongding/wechat-bot) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/wechat-bot/)</sub>

<a name="open-llm-vtuber"></a>
### #&#8288;51 [open-llm-vtuber](https://github.com/open-llm-vtuber/open-llm-vtuber) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (66) · Freshness: recent (55) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · May 2026</sub>

**Voice-chat AI companion with a Live2D avatar and desktop pet mode.**

Open-LLM-VTuber is a Python server with web and desktop clients for real-time voice conversations with a Live2D character. It plugs in LLM, speech recognition and text-to-speech backends through a config file, and can run fully offline with local models. It also supports camera and screen input, voice interruption, and a transparent desktop pet mode.

- **+** Many swappable backends: Ollama, OpenAI-compatible, Claude, Gemini, vLLM, GGUF for LLMs
- **+** ASR and TTS options include sherpa-onnx, Faster-Whisper, Edge TTS, GPTSoVITS, Fish Audio
- **+** Runs fully offline on Windows, macOS and Linux, with CPU or cloud API fallback
- **+** Pluggable Agent interface and custom Live2D models for characters
- **−** Long-term memory feature is temporarily removed
- **−** v1 is in maintenance; a full v2 rewrite is planned and v1 feature requests are refused
- **−** Remote access needs https via reverse proxy, or the browser microphone will not start
- **−** License is NOASSERTION; bundled Live2D sample models carry separate terms for commercial use

<sub>GPU optional · Docker · Needs uv, ffmpeg · Models: Ollama, OpenAI-compatible, Gemini, Claude, Mistral · [Repo](https://github.com/open-llm-vtuber/open-llm-vtuber) · [📖 Docs ↗](https://open-llm-vtuber.github.io/docs/quick-start) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-llm-vtuber/)</sub>

<a name="moltworker"></a>
### #&#8288;52 [moltworker](https://github.com/cloudflare/moltworker) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: popular (53) · Freshness: slowing (50) · Maintenance: weak (11) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · Apache-2.0 · Mar 2026</sub>

**Cloudflare Worker that runs the OpenClaw assistant inside a Cloudflare Sandbox container.**

Packages the OpenClaw personal assistant (formerly Moltbot/Clawdbot) to run in a Cloudflare Sandbox container fronted by a Worker. It adds an admin UI at /_admin/ for device pairing, Cloudflare Access auth, optional R2 backups every 5 minutes, and Telegram, Discord and Slack channels. The README labels it an unsupported proof of concept.

- **+** Always-on hosting without managing a server; deploys with wrangler and npm run deploy
- **+** Admin UI for approving devices, restarting the gateway and triggering R2 backups
- **+** Model routing through Cloudflare AI Gateway: Anthropic, OpenAI, Groq or Workers AI
- **+** Includes a CDP shim and a cloudflare-browser skill for screenshots and video
- **−** Marked experimental proof of concept, not officially supported, may break without notice
- **−** Needs Workers Paid plan; README estimates about $34.50/month running 24/7
- **−** Data is lost on container restart unless R2 is configured
- **−** Cold start takes 1-2 minutes; setup requires Cloudflare Access and device pairing

<sub>RAM ≥ 4 GB · no GPU · Docker · Needs Cloudflare Workers Paid plan, Cloudflare Sandbox/Containers, Cloudflare Access, Anthropic API key or Cloudflare AI Gateway, R2 (optional) · Models: Anthropic Claude, OpenAI, Groq, Workers AI · [Repo](https://github.com/cloudflare/moltworker) · [📖 Docs ↗](https://developers.cloudflare.com/sandbox/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moltworker/)</sub>

<a name="gpt-ai-assistant"></a>
### #&#8288;53 [gpt-ai-assistant](https://github.com/memochou1993/gpt-ai-assistant) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: known (37) · Freshness: recent (53) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · MIT · Jun 2026</sub>

**LINE chatbot backed by the OpenAI API.**

JavaScript application that lets you chat with an OpenAI-backed assistant through the LINE mobile app, using the LINE Messaging API as the chat channel. The README mentions commands such as sum and search, but setup details live on a separate documentation site. The author points to a newer successor, fermi, built on Supabase and OpenRouter.

- **+** Uses LINE as the chat front end, so no custom client app is needed
- **+** MIT license; Dockerfile and Compose file are present in the repo
- **+** Documentation published in English and Chinese
- **−** Tied to the OpenAI API and LINE; other providers or chat apps are not described
- **−** Last release was 2024-07-09; the author points to fermi as the successor
- **−** README has no setup steps or requirements; it defers to the docs site
- **−** Long-term memory and tool actions are not described in the README

<sub>no GPU · Docker + Compose · Needs OpenAI API, LINE Messaging API · Models: OpenAI · [Repo](https://github.com/memochou1993/gpt-ai-assistant) · [📖 Docs ↗](https://memochou1993.github.io/gpt-ai-assistant-docs/en) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpt-ai-assistant/)</sub>

<a name="paperdebugger"></a>
### #&#8288;54 [paperdebugger](https://github.com/paperdebugger/paperdebugger) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: niche (2) · Freshness: recent (79) · Maintenance: weak (0) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · AGPL-3.0 · Jul 2026</sub>

**Chrome extension that adds an AI writing and review assistant to Overleaf.**

PaperDebugger is a Chrome extension that adds a chat panel to Overleaf projects. It reads the LaTeX project, suggests edits, inserts responses or comments, and offers prompt templates. The Go backend (Gin, gRPC, MongoDB, OpenAI API) can be self-hosted, and the XtraMCP engine adds literature-grounded research, review-style critique and citation checks.

- **+** Works inside the Overleaf editor with one-click insertion of responses and comments
- **+** Read-only access to the project: it suggests changes but does not modify files
- **+** XtraMCP adds citation verification and conference-style review passes
- **+** Backend can be self-hosted by setting a custom endpoint in the extension
- **−** Tied to Overleaf and Chrome; no standalone or other-editor use
- **−** Backend lists only the OpenAI API for AI; local models are not mentioned
- **−** Self-hosting needs Go services and MongoDB; setup is deferred to DEVELOPMENT.md
- **−** README notes ongoing work on long-term reliability issues

<sub>no GPU · Docker · Needs Chrome, Overleaf, MongoDB, OpenAI API · Models: OpenAI API · [Repo](https://github.com/paperdebugger/paperdebugger) · [🌐 Site ↗](https://chromewebstore.google.com/detail/paperdebugger/dfkedikhakpapbfcnbpmfhpklndgiaog) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paperdebugger/)</sub>

<a name="openclawinstaller"></a>
### #&#8288;55 [openclawinstaller](https://github.com/miaoxworld/openclawinstaller) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (13) · Freshness: slowing (47) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 3.4k · no license · Mar 2026</sub>

**Shell installer and config menu for the OpenClaw personal AI assistant.**

A Shell script that installs OpenClaw through npm on macOS and Linux, then walks through model provider, identity and messaging channel setup. It starts the OpenClaw gateway and provides a menu (config-menu.sh) for providers such as Anthropic, OpenAI, Gemini, OpenRouter, Groq, Mistral and Ollama, and channels such as Telegram, Discord, WhatsApp, Slack and Feishu. The assistant itself lives in the separate OpenClaw repository.

- **+** One curl-pipe command installs dependencies and OpenClaw, then starts the gateway
- **+** Menu covers 7 provider families, with custom base URLs for OneAPI/NewAPI proxies
- **+** Step-by-step setup guides for Telegram, Discord, Feishu and WhatsApp
- **+** Feishu uses WebSocket long connection, so no public webhook endpoint is needed
- **−** Only an installer; the assistant itself is the separate openclaw/openclaw project
- **−** README is written mainly in Chinese
- **−** Needs Node.js 22+ and supports only macOS and Linux
- **−** README warns the assistant needs full computer access; avoid your main machine

<sub>RAM ≥ 2 GB · no GPU · Docker + Compose · Needs Node.js 22+, npm, openclaw · Models: Anthropic Claude, OpenAI GPT, Google Gemini, OpenRouter, Groq · [Repo](https://github.com/miaoxworld/openclawinstaller) · [📖 Docs ↗](https://clawd.bot/docs) · [🌐 Site ↗](https://clawd.bot) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openclawinstaller/)</sub>

<a name="open-health"></a>
### #&#8288;56 [open-health](https://github.com/openhealthforall/open-health) <sub>score [9](../README.md#-how-we-rank "Score 9/100. Adoption: niche (15) · Freshness: quiet (14) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · AGPL-3.0 · Jan 2026</sub>

**Web app that parses personal health records and chats about them with an LLM.**

OpenHealth is a Next.js app that takes health inputs such as blood tests, checkup data, family history and symptoms, parses them into structured data, and uses that as context for chat with an LLM. It supports hosted models (GPT, Claude, Gemini, DeepSeek-V3) and local ones through Ollama, and can parse documents locally with docling. Parsing currently runs in a separate Python server.

- **+** Can run fully local: docling for parsing, Ollama for the LLM
- **+** Works with LLaMA, DeepSeek-V3, GPT, Claude and Gemini
- **+** Docker/Podman Compose setup with a .env file, served on port 3000
- **+** Converts uploaded health data into structured files used as chat context
- **−** Parsing runs in a separate Python server, with a planned TypeScript migration
- **−** Last release was 2025-02-21, so tagged releases lag behind recent commits
- **−** Apple Health, Google Fit and wearable sources appear only in the diagram, not the source list
- **−** AGPL-3.0 license restricts closed-source network deployments

<sub>GPU optional · Docker + Compose · Needs Docker or Podman Compose, Ollama (for local LLMs), docling (for local parsing), Python parsing server · Models: LLaMA, DeepSeek-V3, GPT, Claude, Gemini · port 3000 · [Repo](https://github.com/openhealthforall/open-health) · [▶️ Demo ↗](https://qna.open-health.me/) · [🌐 Site ↗](https://www.open-health.me/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-health/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
