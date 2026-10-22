# 🤖 Assistants reviews · Best of Open-Source AI

Personal AI assistants you run yourself and talk to through chat apps, with memory and the ability to act. Back to the [leaderboard](../README.md#-assistants).

<sub>🌐 Also on the web: [Assistants on archestack.com](https://archestack.com/best-of-ai/assistants/), each project on its own page.</sub>

<a name="openclaw"></a>
### 🥇 [OpenClaw](https://github.com/openclaw/openclaw) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (67) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 393k · MIT · Oct 2026</sub>

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

<a name="nanobot"></a>
### 🥈 [nanobot](https://github.com/hkuds/nanobot) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: very easy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 49k · MIT · Oct 2026</sub>

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

<a name="openhuman"></a>
### 🥉 [openhuman](https://github.com/tinyhumansai/openhuman) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (95) · Easy to run: easy (67) · Agent-ready: ready (100) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · GPL-3.0 · Oct 2026</sub>

**Rust agent harness with desktop app, built-in memory and embeddable library.**

OpenHuman is a single-process Rust agent harness shipped as a desktop app (macOS, Windows, Linux), a terminal app, a headless server and an embeddable Rust crate. It bundles memory recalled with citations, browser and desktop control, MCP and skills, 14 messaging channels, durable workflows, and local or BYOK models. The README reports its own benchmark on ten SWE-bench tasks and claims 500 agents fit on a $10 VPS; it is labelled early beta.

- **+** Embeds as a typed Rust library, no sidecar or daemon needed
- **+** Public benchmark repo; reports 68 MB peak memory and 19.8 s median task time
- **+** Local models (Ollama, LM Studio, MLX) or BYOK across 26 providers
- **+** Approval gate, OS-jail or Docker sandboxing, secrets stored in OS keyring
- **−** Labelled early beta; README warns of rough edges
- **−** Benchmark is self-run on only ten tasks
- **−** GPL-3.0 license constrains embedding in proprietary products
- **−** 119 OAuth app integrations go through Composio, an external service

<sub>GPU optional · Docker + Compose · Needs Composio (OAuth integrations), Ollama / LM Studio / MLX (optional local models), Docker (optional sandbox) · Models: Ollama, LM Studio, MLX, OpenAI-compatible APIs, 26 BYOK providers · [Repo](https://github.com/tinyhumansai/openhuman) · [📖 Docs ↗](https://tinyhumans.gitbook.io/openhuman/) · [🌐 Site ↗](https://tinyhumans.ai/openhuman) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openhuman/)</sub>

<a name="zeroclaw"></a>
### #&#8288;4 [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Oct 2026</sub>

**Single Rust binary agent runtime with 30+ channels and hardware access.**

ZeroClaw is one Rust binary that routes messages from 30+ channels (Discord, Telegram, Matrix, email, voice, webhooks, CLI) to an agent loop backed by Anthropic, OpenAI, Ollama or any OpenAI-compatible provider, with fallback chains. Tools cover shell, browser, HTTP, MCP servers and GPIO/I2C/SPI/USB on Raspberry Pi, STM32 and ESP32. Supervised autonomy, OS sandboxes and signed tool receipts gate each action.

- **+** Default supervised mode: medium-risk operations need approval, high-risk ones are blocked
- **+** Hardware peripherals on Raspberry Pi, STM32, Arduino and ESP32 via a Peripheral trait
- **+** HTTP/WebSocket gateway plus web dashboard for chat, memory, config and cron
- **+** Dual-licensed MIT or Apache-2.0; installs as systemd, launchctl or Windows service
- **−** Hand-written TOML config; a minimal V3 config needs four sections before it runs
- **−** README states no RAM figures and no gateway port
- **−** Unix installer places the binary under the Cargo bin directory

<sub>no GPU · Docker + Compose · Models: Anthropic, OpenAI, OpenAI Codex, Ollama, OpenAI-compatible endpoints · [Repo](https://github.com/zeroclaw-labs/zeroclaw) · [📖 Docs ↗](https://docs.zeroclaw.com/master/en/introduction.html) · [🌐 Site ↗](https://www.zeroclaw.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/zeroclaw/)</sub>

<a name="career-ops"></a>
### #&#8288;5 [career-ops](https://github.com/career-ops-hq/career-ops) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 76k · MIT · Oct 2026</sub>

**Job-search agent that scores postings against your CV and drafts applications.**

Runs inside an AI coding CLI (Claude Code, Codex, OpenCode, Qwen and others). You paste a job URL or text and it checks the posting is still live, scores fit against your CV, and drafts a tailored ATS PDF, cover letter and form answers. It never submits or sends anything; data stays local apart from calls to the AI provider you choose. It also has a portal scanner, a terminal dashboard and batch evaluation.

- **+** Drafts only: no auto-submit and no mail transport in the code, per the README
- **+** No telemetry or backend; CV goes only to your chosen AI provider
- **+** Portal scanner preconfigured for 100+ companies across Ashby, Greenhouse, Lever and Wellfound
- **+** Works with several AI CLIs and can use local or free-tier models
- **−** Requires an AI CLI and a model provider; output quality depends on the model
- **−** README says early runs are rough until it learns your profile
- **−** CV rewording check cannot catch every fabrication; manual review required
- **−** Playwright Chromium needed for PDF generation

<sub>GPU optional · Docker + Compose · Needs Node.js, Playwright Chromium, AI CLI (Claude Code, Codex, OpenCode, Qwen) · Models: Claude, Codex, OpenCode, Qwen, local models · [Repo](https://github.com/career-ops-hq/career-ops) · [🌐 Site ↗](https://career-ops.org/manifesto) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/career-ops/)</sub>

<a name="hermes-agent"></a>
### #&#8288;6 [Hermes Agent](https://github.com/nousresearch/hermes-agent) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 256k · MIT · Oct 2026</sub>

**Self-hosted agent with skill learning, memory and Telegram/Discord/Slack gateway.**

Hermes Agent is a Python agent from Nous Research that runs from a terminal UI or a single gateway process serving Telegram, Discord, Slack, WhatsApp, Signal and email. It keeps persistent memory, creates and refines skills after complex tasks, searches past sessions with FTS5, and runs cron-scheduled jobs. Model providers are switchable with `hermes model`, and tools can run on seven backends including local, Docker, SSH and Modal.

- **+** One gateway process serves Telegram, Discord, Slack, WhatsApp, Signal and email with shared history
- **+** Seven terminal backends, including Docker, SSH, Modal, Daytona and Vercel Sandbox
- **+** Built-in cron scheduler, FTS5 session search and agent-created skills compatible with agentskills.io
- **+** Works with Nous Portal, OpenRouter, OpenAI or any custom endpoint; MCP servers supported
- **−** Hardware requirements (RAM, disk) are not stated in the README
- **−** Windows installer may trigger antivirus false positives on the bundled uv.exe
- **−** Installs via a curl-piped shell script rather than a pinned package on desktop
- **−** Skill self-improvement and user modeling behavior is described, but no benchmarks are given

<sub>no GPU · Docker + Compose · Needs Python, Node.js, ripgrep, FFmpeg, Honcho (user modeling) · Models: Nous Portal, OpenRouter, OpenAI, custom endpoints · [Repo](https://github.com/nousresearch/hermes-agent) · [📖 Docs ↗](https://hermes-agent.nousresearch.com/docs/) · [🌐 Site ↗](https://hermes-agent.nousresearch.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hermes-agent/)</sub>

<a name="langbot"></a>
### #&#8288;7 [langbot](https://github.com/langbot-app/langbot) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

**Platform for running LLM agents as bots on Slack, Discord, Telegram and WeChat.**

LangBot runs AI bots on messaging platforms such as Discord, Telegram, Slack, LINE, QQ, WeChat, WeCom, Lark and DingTalk from one codebase. It adds a web management panel, multiple pipelines, a built-in knowledge base, plugins and MCP support, and can hand conversations to Dify, n8n, Coze or Langflow. It starts with `uvx langbot` on port 5300 or through Docker.

- **+** Covers about a dozen chat platforms, including QQ, WeCom, DingTalk and Lark, from one deployment
- **+** Web panel for configuring and monitoring bots, so no YAML editing is needed
- **+** Connects to Dify, n8n, Coze and Langflow, and to Ollama and LM Studio for local models
- **+** Exposes an MCP endpoint at /mcp and a CLI (lbctl), so other agents can manage it
- **−** Many supported platforms and providers are China-focused, which may matter for Western teams
- **−** Some integrations need an external service or account, such as Dify, n8n or Lark
- **−** RAM and other resource requirements are not stated in the README
- **−** Plugin market and cloud option are hosted services outside the self-hosted core

<sub>no GPU · Docker + Compose · Needs uv or Docker, LLM provider API, or local Ollama or LM Studio · Models: OpenAI, Anthropic, DeepSeek, Google Gemini, xAI · port 5300 · [Repo](https://github.com/langbot-app/langbot) · [📖 Docs ↗](https://langbot.app/docs/en/insight/guide) · [🌐 Site ↗](https://langbot.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langbot/)</sub>

<a name="cowagent"></a>
### #&#8288;8 [cowagent](https://github.com/zhayujie/cowagent) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · MIT · Oct 2026</sub>

**Self-hosted agent assistant with memory, skills and many chat channels.**

CowAgent is a Python agent that plans tasks, calls built-in tools (file I/O, bash, browser, scheduler, web search) and MCP servers, and replies through Web, Telegram, Slack, Discord, WeChat, Feishu, DingTalk, QQ and other channels. It keeps three-tier long-term memory, a Markdown knowledge base, installable skills and multi-agent teams. Models are configured per capability from a web console on port 9899.

- **+** Many channels at once: Web, Telegram, Slack, Discord, WeChat, Feishu, DingTalk, QQ, WeCom
- **+** Chat, vision, image generation, ASR, TTS and embeddings can route to different providers
- **+** MCP support over stdio, SSE and Streamable HTTP, plus a skill hub and GitHub skill installs
- **+** Three-tier memory with nightly distillation and hybrid keyword and vector retrieval
- **−** Agent mode uses substantially more tokens than plain chat, per the README
- **−** Local models only via the Custom provider, which lists chat support only
- **−** Console is reachable externally once web_host is 0.0.0.0, so a password is needed
- **−** Hosted runtime and enterprise features are tied to the vendor's LinkAI service

<sub>no GPU · Docker + Compose · Needs LLM provider API key or custom model endpoint · Models: Claude, OpenAI GPT, Gemini, DeepSeek, Qwen · port 9899 · [Repo](https://github.com/zhayujie/cowagent) · [📖 Docs ↗](https://docs.cowagent.ai/intro/index) · [🌐 Site ↗](https://cowagent.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cowagent/)</sub>

<a name="inbox-zero"></a>
### #&#8288;9 [inbox-zero](https://github.com/elie222/inbox-zero) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · custom license · Oct 2026</sub>

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

<a name="ironclaw"></a>
### #&#8288;10 [IronClaw](https://github.com/nearai/ironclaw) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Sep 2026</sub>

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

<a name="astrbot"></a>
### #&#8288;11 [AstrBot](https://github.com/astrbotdevs/astrbot) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · AGPL-3.0 · Oct 2026</sub>

**Agent chatbot platform connecting LLMs to QQ, Telegram, Slack and other chat apps.**

AstrBot is a Python chatbot platform that connects LLM providers to messaging apps such as QQ, Telegram, Feishu, DingTalk, Slack and Discord. It supports agents, MCP, skills, a knowledge base, personas and automatic context compression, with a WebUI and web chat. Behavior is extended through a plugin marketplace, and code execution can run in an agent sandbox.

- **+** Official adapters for 15 messaging platforms, including QQ, Telegram, Slack, Discord, LINE and Feishu
- **+** Works with OpenAI-compatible APIs, Anthropic, Gemini, Ollama and LM Studio, plus Dify, Coze and Bailian
- **+** Speech-to-text and text-to-speech integrations such as Whisper, SenseVoice, Edge TTS and FishAudio
- **+** Installs via uv, Docker or Compose, or a desktop app; has a WebUI and plugin marketplace
- **−** AGPL-3.0 license carries copyleft obligations for network-hosted modifications
- **−** Platform list leans toward Chinese services such as QQ and WeChat
- **−** WhatsApp support is listed as coming soon
- **−** RAM needs and web port are not stated in the README

<sub>no GPU · Docker + Compose · Needs Python 3.12+, uv, Docker (optional) · Models: OpenAI-compatible, Anthropic, Google Gemini, DeepSeek, Moonshot AI · [Repo](https://github.com/astrbotdevs/astrbot) · [📖 Docs ↗](https://docs.astrbot.app/) · [🌐 Site ↗](https://astrbot.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/astrbot/)</sub>

<a name="qwenpaw"></a>
### #&#8288;12 [QwenPaw](https://github.com/agentscope-ai/qwenpaw) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · Apache-2.0 · Oct 2026</sub>

**Self-hosted personal AI assistant with memory, skills, and many chat channels.**

QwenPaw is a Python assistant you run yourself, with a web Console on port 8088. It keeps three-layer memory (via ReMe), runs skills, plugins and MCP tools, and answers through DingTalk, Lark, WeChat, Discord, Telegram, iMessage and QQ. It works with a built-in local runtime, Ollama, LM Studio or 14+ cloud providers, and includes sandbox and tool-guard protections.

- **+** One instance serves DingTalk, Lark, WeChat, Discord, Telegram, iMessage and QQ
- **+** Runs with built-in local runtime, Ollama, LM Studio or 14+ cloud providers
- **+** Includes Tool Guard, File Guard, Skill Scanner and a kernel-level sandbox
- **+** Install via pip, script, Docker, or a Tauri desktop app for Windows and macOS
- **−** Desktop app is Beta and the macOS build is not notarized
- **−** Requires Python >= 3.11 and < 3.14 for pip install
- **−** Hardware requirements for local QwenPaw-Flash models are not stated
- **−** Many bundled subsystems (Hub, Mail, Creator, Data) add surface area to learn

<sub>GPU optional · Docker + Compose · Needs Python 3.11-3.13, Docker (optional), Ollama or LM Studio (optional) · Models: QwenPaw-Flash (2B/4B/9B/35B-A3B/27B), Ollama, LM Studio, 14+ cloud providers · port 8088 · [Repo](https://github.com/agentscope-ai/qwenpaw) · [▶️ Demo ↗](https://platform.agentscope.io/) · [📖 Docs ↗](https://qwenpaw.agentscope.io/docs/channels) · [🌐 Site ↗](https://qwenpaw.agentscope.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwenpaw/)</sub>

<a name="airi"></a>
### #&#8288;13 [airi](https://github.com/moeru-ai/airi) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: hard (17) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · MIT · Oct 2026</sub>

**Self-hosted AI virtual character with voice, VRM/Live2D avatars and game-playing.**

AIRI is an attempt to re-create Neuro-sama as a self-owned digital companion. It runs as a web app, an Electron desktop app (Tamagotchi) and a Capacitor mobile app (Pocket), and drives VRM or Live2D avatars with speech input, multi-provider TTS and an LLM backend. It can chat on Discord and Telegram and play Minecraft and Factorio, and the README describes it as early-stage.

- **+** Runs in browser, desktop (Electron) and mobile (PWA/Capacitor) from one TypeScript monorepo
- **+** Supports 25+ LLM providers including Ollama, vLLM, SGLang, OpenAI, Anthropic and Gemini
- **+** Controls VRM and Live2D avatars with auto blink, look-at and idle eye movement
- **+** Connectors for Discord voice and text, Telegram, Minecraft and Factorio
- **−** README states development is at an early stage
- **−** Long-term memory (Memory Alaya) and in-browser WebGPU inference are unfinished
- **−** Factorio and Helldivers 2 support are WIP or proof of concept
- **−** No Docker or compose setup; self-hosting means building with pnpm or using release binaries

<sub>GPU optional · Needs pnpm, Electron, Capacitor · Models: OpenAI-compatible APIs, Ollama, vLLM, SGLang, Anthropic · [Repo](https://github.com/moeru-ai/airi) · [▶️ Demo ↗](https://airi.moeru.ai) · [📖 Docs ↗](https://airi.moeru.ai/docs/en/) · [🌐 Site ↗](https://airi.moeru.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/airi/)</sub>

<a name="nanoclaw"></a>
### #&#8288;14 [nanoclaw](https://github.com/nanocoai/nanoclaw) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

**Small personal assistant that runs each agent in its own Linux container.**

NanoClaw is a self-hosted assistant built on the Claude Agent SDK. A single Node host routes messages from channels such as Slack, Telegram, Discord and WhatsApp to per-agent containers, exchanging them through two SQLite files per session. Channels and alternative providers are installed per fork with /add-<name> skills, and customization is done by changing code with Claude Code rather than editing config files.

- **+** Agents run in Docker containers and only see explicitly mounted directories
- **+** Credentials are injected by a gateway, so agents never hold raw API keys
- **+** Small codebase: one host process, no microservices, two SQLite files per session
- **+** Per-agent-group memory, CLAUDE.md and scheduled tasks; many channels via skills
- **−** Default setup depends on Claude Code and an Anthropic credential
- **−** No config files or dashboard; customization and debugging go through Claude Code
- **−** Channels and non-Claude providers are not in trunk; each needs a skill install
- **−** Prebuilt hardened image and managed Slack app require a free account

<sub>no GPU · Needs Docker, Node.js 22+, pnpm 10+, Claude Code, Anthropic API credential, OneCLI Agent Vault (credential gateway) · Models: Claude (default), OpenAI Codex, OpenRouter, Google, DeepSeek via OpenCode, Ollama local models · [Repo](https://github.com/nanocoai/nanoclaw) · [📖 Docs ↗](https://docs.nanoclaw.dev) · [🌐 Site ↗](https://nanoclaw.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nanoclaw/)</sub>

<a name="ai-job-search"></a>
### #&#8288;15 [ai-job-search](https://github.com/ai-job-search-dev/ai-job-search) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: hard (0) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 63k · MIT · Oct 2026</sub>

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

<a name="invisible-dots"></a>
### #&#8288;16 [invisible_dots](https://github.com/feder-cr/invisible_dots) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Oct 2026</sub>

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

<a name="xiaobei"></a>
### #&#8288;17 [xiaobei](https://github.com/teamwiseflow/xiaobei) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · custom license · Oct 2026</sub>

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

<a name="octop"></a>
### #&#8288;18 [octop](https://github.com/tencentcloud/octop) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

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

<a name="nullclaw"></a>
### #&#8288;19 [nullclaw](https://github.com/nullclaw/nullclaw) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: fair (53) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · MIT · Oct 2026</sub>

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

<a name="opensquilla"></a>
### #&#8288;20 [opensquilla](https://github.com/tokenrhythm/opensquilla) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

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

<a name="moltis"></a>
### #&#8288;21 [Moltis](https://github.com/moltis-org/moltis) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Oct 2026</sub>

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

<a name="brigade"></a>
### #&#8288;22 [brigade](https://github.com/spinabot/brigade) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Sep 2026</sub>

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

<a name="ods"></a>
### #&#8288;23 [ods](https://github.com/osmantic/ods) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Oct 2026</sub>

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

<a name="picoclaw"></a>
### #&#8288;24 [PicoClaw](https://github.com/sipeed/picoclaw) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: patchy (36) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Aug 2026</sub>

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

<a name="agenticseek"></a>
### #&#8288;25 [agenticseek](https://github.com/fosowl/agenticseek) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: fair (61) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · GPL-3.0 · Oct 2026</sub>

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

<a name="rowboat"></a>
### #&#8288;26 [rowboat](https://github.com/rowboatlabs/rowboat) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (72) · Easy to run: hard (17) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

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

<a name="khoj"></a>
### #&#8288;27 [Khoj](https://github.com/khoj-ai/khoj) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: popular (78) · Freshness: active (97) · Maintenance: weak (19) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · AGPL-3.0 · Aug 2026</sub>

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

<a name="spacebot"></a>
### #&#8288;28 [Spacebot](https://github.com/spacedriveapp/spacebot) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: fair (60) · Easy to run: easy (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · custom license · Sep 2026</sub>

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

<a name="operit"></a>
### #&#8288;29 [operit](https://github.com/aaswordman/operit) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: hard (17) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · LGPL-3.0 · Sep 2026</sub>

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

<a name="osaurus"></a>
### #&#8288;30 [osaurus](https://github.com/osaurus-ai/osaurus) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: hard (17) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · MIT · Oct 2026</sub>

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

<a name="leon"></a>
### #&#8288;31 [leon](https://github.com/leon-ai/leon) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: fair (50) · Easy to run: hard (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

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

<a name="jev-chat-jarvis"></a>
### #&#8288;32 [jev-chat-jarvis](https://github.com/jev-chat/jev-chat-jarvis) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · MIT · Oct 2026</sub>

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

<a name="wechat-bot"></a>
### #&#8288;33 [wechat-bot](https://github.com/wangrongding/wechat-bot) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (36) · Freshness: recent (70) · Maintenance: weak (22) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Sep 2026</sub>

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

<a name="moltworker"></a>
### #&#8288;34 [moltworker](https://github.com/cloudflare/moltworker) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (28) · Freshness: recent (57) · Maintenance: patchy (33) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · Apache-2.0 · Mar 2026</sub>

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

<a name="open-llm-vtuber"></a>
### #&#8288;35 [open-llm-vtuber](https://github.com/open-llm-vtuber/open-llm-vtuber) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: known (45) · Freshness: recent (62) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · custom license · May 2026</sub>

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

<a name="gpt-ai-assistant"></a>
### #&#8288;36 [gpt-ai-assistant](https://github.com/memochou1993/gpt-ai-assistant) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: niche (12) · Freshness: recent (58) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · MIT · Jun 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
