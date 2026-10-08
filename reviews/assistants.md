# 🤖 Assistants — reviews

Personal AI assistants you run yourself and talk to through chat apps, with memory and the ability to act. Back to the [leaderboard](../README.md#-assistants).

<a name="openclaw"></a>
### 🥇 94 [OpenClaw](https://github.com/openclaw/openclaw) <sub>⭐ 392k · MIT · Oct 2026</sub>

**Personal assistant gateway that answers in Discord, Slack, WhatsApp and Telegram.**

OpenClaw runs a local Gateway that connects one assistant to Discord, iMessage, Slack, Teams, Telegram, WhatsApp and 20+ other channels, plus native apps for macOS, iOS, Android, Windows and Linux. Model providers and agent harnesses (Claude, Codex, local models) are swappable plugins; state, memory and credentials stay on the host. The same Gateway serves one person or a team, differing only in configuration.

- **+** Channels for Discord, iMessage, Slack, Teams, Telegram, WhatsApp and 20+ more from one Gateway
- **+** Native companion apps on macOS, iOS, Android, Windows and Linux add voice, camera and screen
- **+** No paid tier or hosted service; stewarded by a 501(c)(3) foundation
- **+** Model providers and agent harnesses are plugins; swap Claude, Codex or local models
- **−** Tools run on the host for the main session unless sandboxing is configured
- **−** Requires Node 24.16+ or 26.1+; the repo is pnpm-only, plain npm install is unsupported
- **−** Daily version check phones home by default; disable with update.checkOnStart: false

<sub>no GPU · Docker + Compose · Models: Claude, Codex, local models · [Repo](https://github.com/openclaw/openclaw) · [📖 Docs ↗](https://docs.openclaw.ai) · [🌐 Site ↗](https://openclaw.ai)</sub>

<a name="hermes-agent"></a>
### 🥇 91 [Hermes Agent](https://github.com/NousResearch/hermes-agent) <sub>⭐ 252k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: Nous Portal, OpenRouter, OpenAI, custom endpoint · [Repo](https://github.com/NousResearch/hermes-agent) · [📖 Docs ↗](https://hermes-agent.nousresearch.com/docs/) · [🌐 Site ↗](https://hermes-agent.nousresearch.com/)</sub>

<a name="nanobot"></a>
### 🥇 89 [nanobot](https://github.com/HKUDS/nanobot) <sub>⭐ 49k · MIT · Oct 2026</sub>

**Small Python agent runtime with bundled WebUI, TUI and chat channels.**

nanobot is a Python 3.11+ personal agent running as a local gateway with a bundled WebUI on 127.0.0.1:8765, a terminal UI, and connectors for Telegram, Discord, Slack, WeChat, Feishu, Teams, email, Mattermost and Linear. Tools cover files, shell, web search, MCP servers, cron automations, image generation and subagents, with long-term memory and an OpenAI-compatible API. Deploys via pip, Docker Compose or Render.

- **+** WebUI ships inside the PyPI wheel; no separate frontend build needed
- **+** Exposes a Python SDK and an OpenAI-compatible API for integrations
- **+** Groups up to four conversations in one workbench and shares context between them
- **+** First-run WebUI binds to localhost only; not exposed to the LAN by default
- **−** Channels and automations stop when local clients exit unless gateway --background is used
- **−** Native TUI wheels cover macOS 13+, glibc 2.17+ Linux and Windows x64 only
- **−** Source install requires Bun to run the terminal UI

<sub>no GPU · Docker + Compose · Models: OpenAI-compatible APIs, Anthropic, Ollama, vLLM · port 8765 · [Repo](https://github.com/HKUDS/nanobot) · [📖 Docs ↗](https://nanobot.wiki/docs/latest/getting-started/nanobot-overview)</sub>

<a name="zeroclaw"></a>
### 🥇 86 [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) <sub>⭐ 33k · Apache-2.0 · Oct 2026</sub>

**Single Rust binary agent runtime with 30+ channels and hardware access.**

ZeroClaw is one Rust binary that routes messages from 30+ channels (Discord, Telegram, Matrix, email, voice, webhooks, CLI) to an agent loop backed by Anthropic, OpenAI, Ollama or any OpenAI-compatible provider, with fallback chains. Tools cover shell, browser, HTTP, MCP servers and GPIO/I2C/SPI/USB on Raspberry Pi, STM32 and ESP32. Supervised autonomy, OS sandboxes and signed tool receipts gate each action.

- **+** Default supervised mode: medium-risk operations need approval, high-risk ones are blocked
- **+** Hardware peripherals on Raspberry Pi, STM32, Arduino and ESP32 via a Peripheral trait
- **+** HTTP/WebSocket gateway plus web dashboard for chat, memory, config and cron
- **+** Dual-licensed MIT or Apache-2.0; installs as systemd, launchctl or Windows service
- **−** Hand-written TOML config; a minimal V3 config needs four sections before it runs
- **−** README states no RAM figures and no gateway port
- **−** Unix installer places the binary under the Cargo bin directory

<sub>no GPU · Docker + Compose · Models: Anthropic, OpenAI, OpenAI Codex, Ollama, OpenAI-compatible endpoints · [Repo](https://github.com/zeroclaw-labs/zeroclaw) · [📖 Docs ↗](https://docs.zeroclaw.com/master/en/introduction.html) · [🌐 Site ↗](https://www.zeroclaw.com)</sub>

<a name="ironclaw"></a>
### 🥇 80 [IronClaw](https://github.com/nearai/ironclaw) <sub>⭐ 13k · Apache-2.0 · Sep 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs PostgreSQL · Models: OpenAI · [Repo](https://github.com/nearai/ironclaw)</sub>

<a name="khoj"></a>
### 🥈 72 [Khoj](https://github.com/khoj-ai/khoj) <sub>⭐ 38k · AGPL-3.0 · Aug 2026</sub>

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

<sub>Docker + Compose · Models: llama3, qwen, gemma, mistral, OpenAI GPT · [Repo](https://github.com/khoj-ai/khoj) · [▶️ Demo ↗](https://app.khoj.dev) · [📖 Docs ↗](https://docs.khoj.dev) · [🌐 Site ↗](https://khoj.dev)</sub>

<a name="astrbot"></a>
### 🥈 71 [AstrBot](https://github.com/AstrBotDevs/AstrBot) <sub>⭐ 42k · AGPL-3.0 · Oct 2026</sub>

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

<sub>no GPU · Docker · Models: OpenAI-compatible, Anthropic, Google Gemini, DeepSeek, Moonshot · [Repo](https://github.com/AstrBotDevs/AstrBot) · [📖 Docs ↗](https://astrbot.app/)</sub>

<a name="qwenpaw"></a>
### 🥈 66 [QwenPaw](https://github.com/agentscope-ai/QwenPaw) <sub>⭐ 36k · Apache-2.0 · Oct 2026</sub>

**AgentScope-based personal assistant with local Qwen models and chat channels.**

QwenPaw is a Python (3.11 to 3.13) assistant built on AgentScope that serves a browser Console on 127.0.0.1:8088 and connects to DingTalk, Lark, WeChat, Discord, Telegram, iMessage and QQ. It bundles a local runtime for QwenPaw-Flash models (2B, 4B, 9B) and also uses Ollama, LM Studio or 14+ cloud providers, with three-layer memory via ReMe, a kernel-level sandbox, MCP and A2A connectors, skills and plugins.

- **+** Runs without an API key using bundled QwenPaw-Flash 2B, 4B or 9B models
- **+** Memory stored as readable, editable, linked Markdown through ReMe
- **+** Docker image on Docker Hub and Alibaba ACR; config, secrets and backups in separate volumes
- **+** Self-hosted multi-user Hub since v2.2.0
- **−** Desktop app is beta, unnotarized on macOS; first launch takes 10 to 60 seconds
- **−** Script installer may fail behind corporate firewalls or in PowerShell Constrained Language Mode
- **−** Channel lineup leans toward DingTalk, Lark, WeChat and QQ; no Slack or WhatsApp listed

<sub>no GPU · Compose · Models: QwenPaw-Flash (local), Ollama, LM Studio, DashScope, 14+ cloud providers · port 8088 · [Repo](https://github.com/agentscope-ai/QwenPaw) · [▶️ Demo ↗](https://platform.agentscope.io/) · [📖 Docs ↗](https://qwenpaw.agentscope.io/)</sub>

<a name="moltis"></a>
### 🥉 59 [Moltis](https://github.com/moltis-org/moltis) <sub>⭐ 2.9k · MIT · Sep 2026</sub>

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

<sub>no GPU · Docker · Needs Docker, Podman or Apple Container (sandbox) · Models: OpenAI Codex, GitHub Copilot, local models · port 13131 · [Repo](https://github.com/moltis-org/moltis) · [📖 Docs ↗](https://docs.moltis.org/quickstart.html) · [🌐 Site ↗](https://moltis.org)</sub>

<a name="spacebot"></a>
### 51 [Spacebot](https://github.com/spacedriveapp/spacebot) <sub>⭐ 2.4k · NOASSERTION · Sep 2026</sub>

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

<sub>no GPU · Docker · Models: OpenAI-compatible, Anthropic-compatible, Ollama, Azure OpenAI, Gemini · [Repo](https://github.com/spacedriveapp/spacebot) · [📖 Docs ↗](https://docs.spacebot.sh) · [🌐 Site ↗](https://spacebot.sh)</sub>

<a name="picoclaw"></a>
### 40 [PicoClaw](https://github.com/sipeed/picoclaw) <sub>⭐ 30k · MIT · Aug 2026</sub>

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

<sub>RAM ≥ 0.02 GB · no GPU · Models: OpenAI, Anthropic, Google Gemini, OpenRouter, DeepSeek · port 18800 · [Repo](https://github.com/sipeed/picoclaw) · [📖 Docs ↗](https://docs.picoclaw.io/) · [🌐 Site ↗](https://picoclaw.io)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
