# 🤖 Assistants reviews · Best of Open-Source AI

Personal AI assistants you run yourself and talk to through chat apps, with memory and the ability to act. Back to the [leaderboard](../README.md#-assistants).

<sub>🌐 Also on the web: [Assistants on archestack.com](https://archestack.com/best-of-ai/assistants/), each project on its own page.</sub>

<a name="openclaw"></a>
### 🥇 [OpenClaw](https://github.com/openclaw/openclaw) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (67) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 392k · MIT · Oct 2026</sub>

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
### 🥈 [nanobot](https://github.com/hkuds/nanobot) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: very easy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 49k · MIT · Oct 2026</sub>

**Self-hosted Python personal agent with WebUI, TUI and chat-app channels.**

nanobot is a Python agent framework you run yourself and use from a browser WebUI, a terminal TUI, or chat apps such as Telegram, Discord, Slack and Email. It keeps session history and long-term memory (Dream), runs shell, web, MCP and cron tools, and supports long-running goals. It also exposes a Python SDK and an OpenAI-compatible API, and needs an external model provider or local server.

- **+** Many channels: Telegram, Discord, Slack, WeChat, Email, Mattermost, Linear, Teams, Feishu
- **+** Built-in long-term memory, cron automations and /goal long-running tasks
- **+** Works with OpenAI-compatible APIs, Ollama and vLLM, with fallback models
- **+** Installs via script, uv or pip; Python SDK and OpenAI-compatible API included
- **−** Supplies no model; needs a provider account or local model server
- **−** Background gateway does not restart after reboot or crash without an OS service
- **−** Interrupted subagent tasks and missed scheduled runs are not replayed after restart
- **−** Source install needs Git and Bun; native TUI wheels cover limited platforms

<sub>no GPU · Docker + Compose · Needs Python 3.11+, model provider or local model server · Models: OpenAI-compatible APIs, Ollama, vLLM · port 8765 · [Repo](https://github.com/hkuds/nanobot) · [📖 Docs ↗](https://nanobot.wiki/docs/latest/getting-started/nanobot-overview) · [🌐 Site ↗](https://nanobot.wiki/docs/latest/getting-started/nanobot-overview) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nanobot/)</sub>

<a name="openhuman"></a>
### 🥉 [openhuman](https://github.com/tinyhumansai/openhuman) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: easy (67) · Agent-ready: ready (100) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · GPL-3.0 · Oct 2026</sub>

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

<a name="career-ops"></a>
### #&#8288;4 [career-ops](https://github.com/career-ops-hq/career-ops) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (95) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 75k · MIT · Oct 2026</sub>

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

<a name="zeroclaw"></a>
### #&#8288;5 [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Oct 2026</sub>

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

<a name="hermes-agent"></a>
### #&#8288;6 [Hermes Agent](https://github.com/nousresearch/hermes-agent) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 255k · MIT · Oct 2026</sub>

**Terminal and chat-app agent that writes its own skills and remembers you.**

Hermes Agent is a Python agent with a terminal UI and a gateway for Telegram, Discord, Slack, WhatsApp, Signal and email. It creates skills from completed tasks, keeps agent-curated memory, searches past sessions with FTS5, runs cron jobs and spawns subagents; tools execute locally or in Docker, SSH, Modal, Daytona or Vercel Sandbox. Works with Nous Portal, OpenRouter, OpenAI or a custom endpoint.

- **+** Seven execution backends: local, Docker, SSH, Singularity, Modal, Daytona and Vercel Sandbox
- **+** Built-in cron scheduler delivers results to any connected messaging platform
- **+** Imports settings, memories, skills and API keys from an existing OpenClaw install
- **+** MCP server support plus 40+ built-in tools grouped into toolsets
- **−** Installer pulls Python 3.14, Node.js, npm, ripgrep and FFmpeg onto the host
- **−** No bundled browser UI; interfaces are the TUI and the messaging gateway
- **−** Web search, image generation, TTS and cloud browser steer toward the paid Nous Portal
- **−** Antivirus on Windows may quarantine the bundled uv.exe; whitelisting is documented

<sub>no GPU · Docker + Compose · Models: Nous Portal, OpenRouter, OpenAI, custom endpoint · [Repo](https://github.com/nousresearch/hermes-agent) · [📖 Docs ↗](https://hermes-agent.nousresearch.com/docs/) · [🌐 Site ↗](https://hermes-agent.nousresearch.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hermes-agent/)</sub>

<a name="cowagent"></a>
### #&#8288;7 [cowagent](https://github.com/zhayujie/cowagent) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 47k · MIT · Oct 2026</sub>

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

<a name="langbot"></a>
### #&#8288;8 [langbot](https://github.com/langbot-app/langbot) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

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

<a name="airi"></a>
### #&#8288;9 [airi](https://github.com/moeru-ai/airi) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: hard (17) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Oct 2026</sub>

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

<a name="astrbot"></a>
### #&#8288;10 [AstrBot](https://github.com/astrbotdevs/astrbot) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · AGPL-3.0 · Oct 2026</sub>

**Chatbot platform bridging LLMs to QQ, Telegram, Discord, Slack and more.**

AstrBot is a Python 3.12+ chatbot platform that connects LLM providers (OpenAI-compatible, Anthropic, Gemini, DeepSeek, Ollama, LM Studio) to QQ, OneBot, Telegram, WeCom, Feishu, DingTalk, Slack, Discord, LINE, KOOK, Misskey and Mattermost. It adds a WebUI, web chat, MCP, skills, a knowledge base, personas and a code sandbox, and can hand conversations to Dify or Coze. Installs via uv or Docker.

- **+** 14 officially maintained messaging adapters, including QQ, Feishu, DingTalk and WeCom
- **+** 1000+ plugins installable from the built-in marketplace
- **+** Agent sandbox isolates code and shell execution per session
- **+** STT and TTS providers built in: Whisper, SenseVoice, Edge TTS, GPT-SoVITS, Azure and more
- **−** AGPL-3.0 license
- **−** WhatsApp adapter still marked coming soon
- **−** Docker setup is documented only in the external docs, not the README
- **−** Several model-provider links in the README are referral or affiliate links

<sub>no GPU · Docker + Compose · Models: OpenAI-compatible, Anthropic, Google Gemini, DeepSeek, Moonshot · [Repo](https://github.com/astrbotdevs/astrbot) · [📖 Docs ↗](https://astrbot.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/astrbot/)</sub>

<a name="qwenpaw"></a>
### #&#8288;11 [QwenPaw](https://github.com/agentscope-ai/qwenpaw) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · Apache-2.0 · Oct 2026</sub>

**Personal AI agent with memory, skills, and chat-channel connectors.**

QwenPaw is a personal agent runtime installed with pip, a script, Docker, or a desktop app, with a web Console on port 8088 and a terminal UI. It keeps layered memory as Markdown via ReMe, runs skills, plugins, and MCP tools, and replies through DingTalk, Lark, WeChat, Discord, Telegram, iMessage, and QQ. Models can be local (built-in runtime, Ollama, LM Studio) or any of 14+ cloud providers.

- **+** One instance serves DingTalk, Lark, WeChat, Discord, Telegram, iMessage, and QQ
- **+** Works with Ollama, LM Studio, a built-in local runtime, or 14+ cloud providers
- **+** Sandbox, Tool Guard, File Guard, and Skill Scanner gate commands before they run
- **+** Supports MCP, plus ACP for cross-system agent orchestration
- **−** Requires Python 3.11 to below 3.14 for the pip install path
- **−** Desktop app is beta and the macOS build is not notarized
- **−** RAM and VRAM requirements are unknown; the README does not state them
- **−** Major versions shipped monthly since 2.0, so expect fast-changing behavior

<sub>GPU optional · Docker + Compose · Models: QwenPaw-Flash local models, Ollama, LM Studio, 14+ cloud providers · port 8088 · [Repo](https://github.com/agentscope-ai/qwenpaw) · [▶️ Demo ↗](https://platform.agentscope.io/) · [📖 Docs ↗](https://qwenpaw.agentscope.io/) · [🌐 Site ↗](https://qwenpaw.agentscope.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwenpaw/)</sub>

<a name="ironclaw"></a>
### #&#8288;12 [IronClaw](https://github.com/nearai/ironclaw) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Sep 2026</sub>

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

<a name="nanoclaw"></a>
### #&#8288;13 [nanoclaw](https://github.com/nanocoai/nanoclaw) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

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

<a name="invisible-dots"></a>
### #&#8288;14 [invisible_dots](https://github.com/feder-cr/invisible_dots) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Oct 2026</sub>

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

<a name="moltis"></a>
### #&#8288;15 [Moltis](https://github.com/moltis-org/moltis) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Oct 2026</sub>

**Persistent personal agent server in one Rust binary with sandboxed execution.**

Moltis is a single Rust binary that serves a web UI (port 13131), Telegram, Signal, Discord, Slack, Teams, Matrix, WhatsApp and Nostr from one gateway, and runs every command in a Docker, Podman or WASM sandbox. It keeps memory in SQLite with full-text and vector search, supports MCP (stdio and HTTP/SSE), ACP, cron, CalDAV and email, 8 TTS and 7 STT providers, and password, passkey and API-key auth.

- **+** Every command runs in a Docker, Podman, Apple Container or WASM sandbox
- **+** Passkey (WebAuthn), password and API-key auth; vault encrypted with XChaCha20-Poly1305
- **+** Signed releases with Sigstore attestations and GPG; verifiable with gh attestation
- **+** Langfuse, OTLP and Prometheus instrumentation built in
- **−** Docker deployment mounts the host Docker socket into the container
- **−** Serves HTTPS with its own certificate; browsers need TLS trust setup
- **−** Source build needs just and Node.js for Tailwind on top of Rust 1.91+
- **−** Constrained devices need a custom build with --no-default-features --features lightweight

<sub>no GPU · Docker + Compose · Needs Docker, Podman or Apple Container (sandbox) · Models: OpenAI Codex, GitHub Copilot, local models · port 13131 · [Repo](https://github.com/moltis-org/moltis) · [📖 Docs ↗](https://docs.moltis.org/quickstart.html) · [🌐 Site ↗](https://moltis.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moltis/)</sub>

<a name="spacebot"></a>
### #&#8288;16 [Spacebot](https://github.com/spacedriveapp/spacebot) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: fair (60) · Easy to run: easy (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · custom license · Sep 2026</sub>

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

<a name="picoclaw"></a>
### #&#8288;17 [PicoClaw](https://github.com/sipeed/picoclaw) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (50) · Freshness: active (100) · Maintenance: patchy (42) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Aug 2026</sub>

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

<a name="khoj"></a>
### #&#8288;18 [Khoj](https://github.com/khoj-ai/khoj) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (67) · Freshness: active (98) · Maintenance: weak (19) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · AGPL-3.0 · Aug 2026</sub>

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

<a name="agenticseek"></a>
### #&#8288;19 [agenticseek](https://github.com/fosowl/agenticseek) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: known (44) · Freshness: active (100) · Maintenance: fair (61) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · GPL-3.0 · Oct 2026</sub>

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
### #&#8288;20 [rowboat](https://github.com/rowboatlabs/rowboat) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: fair (73) · Easy to run: hard (17) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

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

<a name="leon"></a>
### #&#8288;21 [leon](https://github.com/leon-ai/leon) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: fair (50) · Easy to run: hard (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

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

<a name="open-llm-vtuber"></a>
### #&#8288;22 [open-llm-vtuber](https://github.com/open-llm-vtuber/open-llm-vtuber) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (17) · Freshness: recent (63) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · custom license · May 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
