<p align="center"><img src="https://github.com/archestack.png" width="80" alt="Archestack" /></p>
<h1 align="center">Best of Self-Hosted AI</h1>
<p align="center">Open-source AI apps you can run on your own server, VPS or homelab: what each one does, what it needs, where it falls short. Every entry is written from the project README and checked facts, and refreshed by bots.</p>
<p align="center">Looking for starters and templates to build your own AI app? See <a href="https://github.com/archestack/best-of-ai-starters"><b>Best of AI Starters</b></a>.</p>
<p align="center"><sub>159 projects · 14 categories · updated 2026-10-08 · <a href="#how-entries-are-written">how entries are written</a> · <a href="#submit-fix-or-opt-out">submit or fix</a></sub></p>

## Contents

- [Assistants](#assistants) · 11
- [Chat UIs](#chat-uis) · 13
- [Agent platforms](#agent-platforms) · 12
- [RAG and knowledge](#rag-and-knowledge) · 15
- [Model serving](#model-serving) · 18
- [Gateways](#gateways) · 13
- [Memory](#memory) · 11
- [Voice](#voice) · 11
- [Image and video](#image-and-video) · 8
- [Coding](#coding) · 9
- [Search](#search) · 8
- [Observability](#observability) · 13
- [Vector databases](#vector-databases) · 9
- [Sandboxes](#sandboxes) · 8

## Assistants

Personal AI assistants you run yourself and talk to through chat apps, with memory and the ability to act. <sub>11 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Check which channels it supports today (WhatsApp, Telegram, Slack, Discord, email) and whether each needs a paid API.
- Look at how memory is stored and whether you can inspect or wipe it.
- Actions need credentials; prefer assistants that scope them per tool.

</details>

### [OpenClaw](https://github.com/openclaw/openclaw) <sub>★ 391.6k · MIT · Oct 2026</sub>

**Personal assistant gateway that answers in Discord, Slack, WhatsApp and Telegram.**

OpenClaw runs a local Gateway that connects one assistant to Discord, iMessage, Slack, Teams, Telegram, WhatsApp and 20+ other channels, plus native apps for macOS, iOS, Android, Windows and Linux. Model providers and agent harnesses (Claude, Codex, local models) are swappable plugins; state, memory and credentials stay on the host. The same Gateway serves one person or a team, differing only in configuration.

- **+** Channels for Discord, iMessage, Slack, Teams, Telegram, WhatsApp and 20+ more from one Gateway
- **+** Native companion apps on macOS, iOS, Android, Windows and Linux add voice, camera and screen
- **+** No paid tier or hosted service; stewarded by a 501(c)(3) foundation
- **+** Model providers and agent harnesses are plugins; swap Claude, Codex or local models
- **−** Tools run on the host for the main session unless sandboxing is configured
- **−** Requires Node 24.16+ or 26.1+; the repo is pnpm-only, plain npm install is unsupported
- **−** Daily version check phones home by default; disable with update.checkOnStart: false

<sub>no GPU · Docker + Compose · Models: Claude, Codex, local models · [Repo](https://github.com/openclaw/openclaw) · [Docs](https://docs.openclaw.ai) · [Site](https://openclaw.ai)</sub>

### [Hermes Agent](https://github.com/NousResearch/hermes-agent) <sub>★ 252.1k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: Nous Portal, OpenRouter, OpenAI, custom endpoint · [Repo](https://github.com/NousResearch/hermes-agent) · [Docs](https://hermes-agent.nousresearch.com/docs/) · [Site](https://hermes-agent.nousresearch.com/)</sub>

### [nanobot](https://github.com/HKUDS/nanobot) <sub>★ 48.9k · MIT · Oct 2026</sub>

**Small Python agent runtime with bundled WebUI, TUI and chat channels.**

nanobot is a Python 3.11+ personal agent running as a local gateway with a bundled WebUI on 127.0.0.1:8765, a terminal UI, and connectors for Telegram, Discord, Slack, WeChat, Feishu, Teams, email, Mattermost and Linear. Tools cover files, shell, web search, MCP servers, cron automations, image generation and subagents, with long-term memory and an OpenAI-compatible API. Deploys via pip, Docker Compose or Render.

- **+** WebUI ships inside the PyPI wheel; no separate frontend build needed
- **+** Exposes a Python SDK and an OpenAI-compatible API for integrations
- **+** Groups up to four conversations in one workbench and shares context between them
- **+** First-run WebUI binds to localhost only; not exposed to the LAN by default
- **−** Channels and automations stop when local clients exit unless gateway --background is used
- **−** Native TUI wheels cover macOS 13+, glibc 2.17+ Linux and Windows x64 only
- **−** Source install requires Bun to run the terminal UI

<sub>no GPU · Docker + Compose · Models: OpenAI-compatible APIs, Anthropic, Ollama, vLLM · port 8765 · [Repo](https://github.com/HKUDS/nanobot) · [Docs](https://nanobot.wiki/docs/latest/getting-started/nanobot-overview)</sub>

### [AstrBot](https://github.com/AstrBotDevs/AstrBot) <sub>★ 41.5k · AGPL-3.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: OpenAI-compatible, Anthropic, Google Gemini, DeepSeek, Moonshot · [Repo](https://github.com/AstrBotDevs/AstrBot) · [Docs](https://astrbot.app/)</sub>

### [Khoj](https://github.com/khoj-ai/khoj) <sub>★ 37.6k · AGPL-3.0 · Aug 2026</sub>

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

<sub>Docker + Compose · Models: llama3, qwen, gemma, mistral, OpenAI GPT · [Repo](https://github.com/khoj-ai/khoj) · [Demo](https://app.khoj.dev) · [Docs](https://docs.khoj.dev) · [Site](https://khoj.dev)</sub>

### [QwenPaw](https://github.com/agentscope-ai/QwenPaw) <sub>★ 35.5k · Apache-2.0 · Oct 2026</sub>

**AgentScope-based personal assistant with local Qwen models and chat channels.**

QwenPaw is a Python (3.11 to 3.13) assistant built on AgentScope that serves a browser Console on 127.0.0.1:8088 and connects to DingTalk, Lark, WeChat, Discord, Telegram, iMessage and QQ. It bundles a local runtime for QwenPaw-Flash models (2B, 4B, 9B) and also uses Ollama, LM Studio or 14+ cloud providers, with three-layer memory via ReMe, a kernel-level sandbox, MCP and A2A connectors, skills and plugins.

- **+** Runs without an API key using bundled QwenPaw-Flash 2B, 4B or 9B models
- **+** Memory stored as readable, editable, linked Markdown through ReMe
- **+** Docker image on Docker Hub and Alibaba ACR; config, secrets and backups in separate volumes
- **+** Self-hosted multi-user Hub since v2.2.0
- **−** Desktop app is beta, unnotarized on macOS; first launch takes 10 to 60 seconds
- **−** Script installer may fail behind corporate firewalls or in PowerShell Constrained Language Mode
- **−** Channel lineup leans toward DingTalk, Lark, WeChat and QQ; no Slack or WhatsApp listed

<sub>no GPU · Compose · Models: QwenPaw-Flash (local), Ollama, LM Studio, DashScope, 14+ cloud providers · port 8088 · [Repo](https://github.com/agentscope-ai/QwenPaw) · [Demo](https://platform.agentscope.io/) · [Docs](https://qwenpaw.agentscope.io/)</sub>

### [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) <sub>★ 32.9k · Apache-2.0 · Oct 2026</sub>

**Single Rust binary agent runtime with 30+ channels and hardware access.**

ZeroClaw is one Rust binary that routes messages from 30+ channels (Discord, Telegram, Matrix, email, voice, webhooks, CLI) to an agent loop backed by Anthropic, OpenAI, Ollama or any OpenAI-compatible provider, with fallback chains. Tools cover shell, browser, HTTP, MCP servers and GPIO/I2C/SPI/USB on Raspberry Pi, STM32 and ESP32. Supervised autonomy, OS sandboxes and signed tool receipts gate each action.

- **+** Default supervised mode: medium-risk operations need approval, high-risk ones are blocked
- **+** Hardware peripherals on Raspberry Pi, STM32, Arduino and ESP32 via a Peripheral trait
- **+** HTTP/WebSocket gateway plus web dashboard for chat, memory, config and cron
- **+** Dual-licensed MIT or Apache-2.0; installs as systemd, launchctl or Windows service
- **−** Hand-written TOML config; a minimal V3 config needs four sections before it runs
- **−** README states no RAM figures and no gateway port
- **−** Unix installer places the binary under the Cargo bin directory

<sub>no GPU · Docker + Compose · Models: Anthropic, OpenAI, OpenAI Codex, Ollama, OpenAI-compatible endpoints · [Repo](https://github.com/zeroclaw-labs/zeroclaw) · [Docs](https://docs.zeroclaw.com/master/en/introduction.html) · [Site](https://www.zeroclaw.com)</sub>

### [PicoClaw](https://github.com/sipeed/picoclaw) <sub>★ 30.0k · MIT · Aug 2026</sub>

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

<sub>RAM ≥ 0.02 GB · no GPU · Models: OpenAI, Anthropic, Google Gemini, OpenRouter, DeepSeek · port 18800 · [Repo](https://github.com/sipeed/picoclaw) · [Docs](https://docs.picoclaw.io/) · [Site](https://picoclaw.io)</sub>

### [IronClaw](https://github.com/nearai/ironclaw) <sub>★ 12.6k · Apache-2.0 · Sep 2026</sub>

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

### [Moltis](https://github.com/moltis-org/moltis) <sub>★ 2.9k · MIT · Sep 2026</sub>

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

<sub>no GPU · Docker · Needs Docker, Podman or Apple Container (sandbox) · Models: OpenAI Codex, GitHub Copilot, local models · port 13131 · [Repo](https://github.com/moltis-org/moltis) · [Docs](https://docs.moltis.org/quickstart.html) · [Site](https://moltis.org)</sub>

### [Spacebot](https://github.com/spacedriveapp/spacebot) <sub>★ 2.4k · NOASSERTION · Sep 2026</sub>

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

<sub>no GPU · Docker · Models: OpenAI-compatible, Anthropic-compatible, Ollama, Azure OpenAI, Gemini · [Repo](https://github.com/spacedriveapp/spacebot) · [Docs](https://docs.spacebot.sh) · [Site](https://spacebot.sh)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Chat UIs

Web front-ends for local or API models, usually with user accounts, chat history and file upload. <sub>13 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Confirm it talks to your backend (Ollama, OpenAI-compatible, Anthropic) without a plugin.
- Multi-user auth, RBAC and SSO are where free and paid editions differ most.
- Check what the default compose pulls in (database, vector store) before sizing the host.

</details>

### [Open WebUI](https://github.com/open-webui/open-webui) <sub>★ 154.2k · NOASSERTION · Sep 2026</sub>

**Self-hosted chat UI for Ollama and OpenAI-compatible APIs with RBAC and RAG.**

Open WebUI is a Python-served web interface (pip or Docker, port 8080) for Ollama and any OpenAI-compatible API such as LM Studio, vLLM, OpenRouter or Groq. It bundles RAG over 9 vector databases with hybrid BM25 search, web search through 20+ providers, image generation via ComfyUI, AUTOMATIC1111, DALL-E or Gemini, MCP and OpenAPI tool servers, and per-user roles with LDAP, OAuth and SCIM provisioning.

- **+** Images tagged :ollama and :cuda bundle Ollama or CUDA acceleration in one container
- **+** RBAC, user groups, LDAP/AD, OAuth SSO and SCIM 2.0 provisioning built in
- **+** 9 vector databases incl. ChromaDB, PGVector, Qdrant, Milvus and Elasticsearch
- **+** Redis-backed sessions and WebSockets for multi-worker, multi-node deployments
- **−** Custom Open WebUI License requires keeping the Open WebUI branding visible
- **−** Enterprise plan pitched at the top of the README; Terminals isolation is enterprise-only
- **−** pip install is pinned to Python 3.11
- **−** Data is lost unless the /app/backend/data volume is mounted

<sub>GPU optional · Docker + Compose · Models: Ollama, OpenAI-compatible APIs, LM Studio, vLLM, OpenRouter · port 8080 · [Repo](https://github.com/open-webui/open-webui) · [Docs](https://docs.openwebui.com/) · [Site](https://openwebui.com)</sub>

### [NextChat](https://github.com/ChatGPTNextWeb/NextChat) <sub>★ 88.8k · MIT · Aug 2026</sub>

**Lightweight Next.js chat client for OpenAI, Claude, Gemini and DeepSeek APIs.**

NextChat is a Node.js web client (Docker image yidadaa/chatgpt-next-web on port 3000, or a one-click Vercel deploy) that talks to OpenAI, Azure, Anthropic, Google Gemini, DeepSeek, Baidu, ByteDance, Alibaba, iFlytek, ChatGLM, SiliconFlow and 302.AI through environment variables. Chat history stays in the browser, access is gated by a shared CODE password list, and MCP tools switch on with ENABLE_MCP=true.

- **+** First screen about 100 KB with streaming responses; desktop client about 5 MB
- **+** Providers configured purely by environment variables; CUSTOM_MODELS edits the model list
- **+** UI in 14 languages; PWA, dark mode, Markdown with LaTeX and mermaid
- **+** Hosted demo at app.nextchat.club
- **−** No user accounts; access control is a comma-separated password list in CODE
- **−** Conversations live in browser storage; cross-device sync needs an UpStash setup
- **−** OPENAI_API_KEY is marked required even when another provider is used
- **−** Local knowledge base still unchecked on the roadmap

<sub>no GPU · Docker + Compose · Models: OpenAI, Azure OpenAI, Anthropic, Google Gemini, DeepSeek · port 3000 · [Repo](https://github.com/ChatGPTNextWeb/NextChat) · [Demo](https://app.nextchat.club) · [Site](https://nextchat.club)</sub>

### [LobeHub](https://github.com/lobehub/lobehub) <sub>★ 83.1k · NOASSERTION · Oct 2026</sub>

**Agent workspace with builder, groups, scheduling and 10,000+ MCP skills.**

LobeHub is a self-hostable agent workspace that runs on Vercel, Zeabur, Sealos, Alibaba Cloud or Docker Compose. It centres on an Agent Builder, Agent Groups that work a task in parallel, Pages for co-writing, scheduled runs, projects and shared workspaces, plus structured editable memory and an IM gateway, with 10,000+ tools and MCP-compatible plugins. An OpenAI API key is required to start.

- **+** One-click deploy buttons for Vercel, Zeabur, Sealos, RepoCloud and Alibaba Cloud
- **+** 10,000+ tools and MCP-compatible plugins for agents
- **+** Agent Groups, scheduled runs, projects and team workspaces
- **+** Memory is structured and editable rather than a hidden store
- **−** OPENAI_API_KEY is a required environment variable
- **−** Docker setup runs a curl-piped script from lobe.li before docker compose up
- **−** README recommends a third-party API reseller through an affiliate link
- **−** README states no ports, databases or hardware requirements

<sub>no GPU · Docker · Models: OpenAI, OpenAI-compatible proxy · [Repo](https://github.com/lobehub/lobehub)</sub>

### [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm) <sub>★ 66.8k · MIT · Oct 2026</sub>

**Document chat and agent app with built-in RAG, MCP and multi-user support.**

AnythingLLM is a Node.js app that ingests PDF, TXT, DOCX and other files into a workspace and chats over them with any of 40+ LLM providers, from llama.cpp, Ollama and LM Studio to OpenAI, Anthropic, Bedrock and Gemini. It ships a native embedder, LanceDB by default plus 8 other vector stores, a no-code agent builder, MCP support, scheduled tasks, model routing and a developer API.

- **+** LanceDB embedded by default; PGVector, Qdrant, Milvus, Chroma, Weaviate, Pinecone optional
- **+** Native embedder and audio transcription run locally with no extra service
- **+** Multi-user instance with per-user permissions in the Docker build
- **+** Embeddable website chat widget and a full developer API
- **−** Anonymous telemetry to PostHog is on by default; opt out with DISABLE_TELEMETRY=true
- **−** Multi-user support and the embed widget are Docker-only, not in the desktop app
- **−** Speech-to-text is limited to the browser built-in engine
- **−** No root Dockerfile; container build lives under docker/

<sub>no GPU · Models: llama.cpp-compatible models, OpenAI, Azure OpenAI, AWS Bedrock, Anthropic · [Repo](https://github.com/Mintplex-Labs/anything-llm) · [Docs](https://docs.anythingllm.com) · [Site](https://anythingllm.com)</sub>

### [LibreChat](https://github.com/LibreChat-AI/LibreChat) <sub>★ 45.4k · MIT · Oct 2026</sub>

**Multi-provider ChatGPT-style app with agents, MCP, code interpreter and auth.**

LibreChat is a self-hosted chat platform that fronts Anthropic, OpenAI, Azure, AWS Bedrock, Google, Vertex AI and any OpenAI-compatible endpoint such as Ollama or OpenRouter. It adds agents with MCP servers, skills and subagents, a sandboxed code interpreter for Python, Node, Go, Rust and more, web search, artifacts, resumable streams, and multi-user login via OAuth2, LDAP or email with an admin panel.

- **+** Admin panel for users, groups, roles and config overrides ships in the Compose stack
- **+** Resumable streams reconnect dropped responses and sync across tabs and devices
- **+** UI translated into 30+ languages
- **+** OpenTelemetry and Langfuse export for traces and logs
- **−** Code interpreter is a separate API service, not part of this repo
- **−** File search (RAG) depends on the separate rag-api service
- **−** Horizontal scaling and resumable streams need Redis
- **−** Attached code workspaces are marked highly experimental

<sub>no GPU · Docker + Compose · Models: Anthropic, OpenAI, Azure OpenAI, AWS Bedrock, Google · [Repo](https://github.com/LibreChat-AI/LibreChat) · [Docs](https://docs.librechat.ai) · [Site](https://librechat.ai)</sub>

### [SillyTavern](https://github.com/SillyTavern/SillyTavern) <sub>★ 34.2k · AGPL-3.0 · Sep 2026</sub>

**Local chat front end for role-play across many LLM backends.**

SillyTavern is a locally installed Node.js 20+ interface for text-generation LLMs, image generators and TTS, aimed at character and role-play chat. One UI covers KoboldAI/KoboldCpp, Horde, NovelAI, oobabooga, TabbyAPI, OpenAI, OpenRouter, Claude and Mistral, with Visual Novel Mode, AUTOMATIC1111 and ComfyUI image generation, WorldInfo lorebooks and third-party extensions. No hosted service, no tracking.

- **+** Runs on anything that can run Node.js 20; no GPU needed for the UI itself
- **+** Backends: KoboldCpp, Horde, NovelAI, oobabooga, TabbyAPI, OpenAI, OpenRouter, Claude, Mistral
- **+** WorldInfo lorebooks and deep prompt controls for long-form character chat
- **+** No hosted service and no telemetry; 300+ contributors over 3 years
- **−** AGPL-3.0 license
- **−** Single-user local tool; no accounts or team features
- **−** Maintainers describe the learning curve as steep
- **−** Installation and Docker instructions live only on the docs site

<sub>no GPU · Docker · Models: KoboldAI/KoboldCpp, Horde, NovelAI, oobabooga, TabbyAPI · [Repo](https://github.com/SillyTavern/SillyTavern) · [Docs](https://docs.sillytavern.app/)</sub>

### [Onyx](https://github.com/onyx-dot-app/onyx) <sub>★ 32.4k · NOASSERTION · Oct 2026</sub>

**Team knowledge chat that indexes 50+ apps for RAG and agents.**

Onyx indexes content and permissions from 50+ apps into a hybrid vector and keyword index, then answers through agentic RAG, deep research and custom agents with web search, MCP actions and a code sandbox. It works with Ollama, LiteLLM, vLLM, Anthropic, OpenAI or Gemini, deploys via Docker, Kubernetes or Helm, and is reachable from the web app, Slack and Discord bots, an MCP server or a Chrome extension.

- **+** Lite mode runs the chat UI and agents in under 1 GB of memory
- **+** Air-gappable: index, database and processing all run inside your environment
- **+** MCP server gives Claude Code, Codex or any MCP client company context with user permissions
- **+** Community Edition is MIT; install script sets up Docker in one command
- **−** SSO (OIDC, SAML), SCIM, RBAC, analytics and whitelabeling are Enterprise Edition only
- **−** Standard mode adds index, worker, inference, Redis and MinIO containers
- **−** Lite mode cannot index documents
- **−** README gives no port or hardware figures for the Standard deployment

<sub>RAM ≥ 1 GB · no GPU · Needs Redis (standard mode), MinIO (standard mode) · Models: Ollama, LiteLLM, vLLM, Anthropic, OpenAI · [Repo](https://github.com/onyx-dot-app/onyx) · [Demo](https://cloud.onyx.app/signup) · [Docs](https://docs.onyx.app/) · [Site](https://www.onyx.app/)</sub>

### [Hermes WebUI](https://github.com/nesquena/hermes-webui) <sub>★ 18.8k · MIT · Oct 2026</sub>

**Browser front end for Hermes Agent with sessions, files and voice input.**

Hermes WebUI is a Python plus vanilla JavaScript web app (no build step, port 8787) that runs an installed Hermes Agent in-process and shows it in a three-panel layout: sessions and projects, streaming chat, and a workspace file browser. It mirrors the CLI feature set, imports Hermes CLI sessions from SQLite, adds Web Speech voice input, profiles, passkey and OIDC login, and ships a Nix flake and Docker images.

- **+** No build step, framework or bundler; Python and vanilla JS only
- **+** CLI sessions from the Hermes SQLite store appear in the sidebar and can be continued
- **+** Optional password, passkey (WebAuthn) and native OIDC login
- **+** Nix flake, NixOS module and single- or multi-container Docker deploys
- **−** Requires a Hermes Agent install; the bootstrap runs its installer if missing
- **−** Password auth is off by default
- **−** Native Windows is not supported by the bootstrap; Linux, macOS or WSL2 only
- **−** Stop procedure differs per launch method; only ctl.sh writes a PID file

<sub>no GPU · Docker + Compose · Needs Hermes Agent · Models: OpenAI, Anthropic, Google, DeepSeek, Nous Portal · port 8787 · [Repo](https://github.com/nesquena/hermes-webui)</sub>

### [HuggingChat UI](https://github.com/huggingface/chat-ui) <sub>★ 11.0k · Apache-2.0 · Oct 2026</sub>

**SvelteKit chat front end behind HuggingChat for OpenAI-compatible endpoints.**

Chat UI is the SvelteKit app that powers HuggingChat. It talks only to OpenAI-compatible APIs set through OPENAI_BASE_URL, discovering models from the /models endpoint, so llama.cpp server, Ollama, OpenRouter, Poe or the HF router all work. Chat history, users and settings live in MongoDB 6/7, MCP servers can supply tools, and a heuristic Omni router picks per-message routes with fallbacks.

- **+** chat-ui-db Docker image bundles MongoDB; one container on port 3000
- **+** MCP tool calls surfaced as OpenAI function calling with per-model overrides
- **+** Same codebase as the public HuggingChat deployment
- **+** Apache-2.0 license
- **−** OpenAI-compatible endpoints only; legacy provider integrations and GGUF discovery removed
- **−** Embeddings and web-search helpers were removed from this branch
- **−** Router needs a hand-written routes JSON; no sample file ships
- **−** README does not describe authentication or multi-user setup

<sub>no GPU · Docker + Compose · Needs MongoDB · Models: OpenAI-compatible endpoints, Hugging Face Inference Providers, llama.cpp server, Ollama, OpenRouter · port 3000 · [Repo](https://github.com/huggingface/chat-ui) · [Demo](https://huggingface.co/chat)</sub>

### [big-AGI](https://github.com/enricoros/big-AGI) <sub>★ 7.1k · MIT · Oct 2026</sub>

**Multi-model chat workspace with Beam side-by-side model comparison.**

Big-AGI Open is the self-hostable web app behind big-agi.com, deployable via Docker or Vercel. It connects 20+ LLM services and 500+ models with your own API keys, and its Beam feature runs one prompt across several models and merges the answers. Personas, request inspection, web search with citations, image generation and multi-vendor speech are included; data stays local-first in the browser.

- **+** Beam and Merge: fan one prompt out to several models and reconcile the results
- **+** 20+ LLM services incl. Anthropic, OpenAI, Gemini, Ollama, LM Studio, LocalAI, Bedrock, Groq
- **+** AI Inspector shows the exact requests sent to each provider
- **+** MIT license; no usage charges, bring your own keys
- **−** Cross-device sync and 1 GB storage only on the hosted Pro tier at $10.99/month
- **−** No SSO or shared team features in the open build; managed deployments by request
- **−** README omits stack, ports and resource requirements; install guide lives in docs/
- **−** README is mostly badges, taglines and release notes rather than specs

<sub>no GPU · Docker + Compose · Models: Anthropic, OpenAI, Google Gemini, Ollama, LM Studio · [Repo](https://github.com/enricoros/big-AGI) · [Site](https://big-agi.com)</sub>

### [LoLLMs WebUI](https://github.com/ParisNeo/lollms-webui) <sub>★ 4.8k · Apache-2.0 · Sep 2026</sub>

**Single-user web UI for local and remote LLMs with many personalities.**

LoLLMs WebUI is a Python 3.11 web app (port 9600) fronting local models via HF transformers, GGUF/GGML, ExLlama v2, Ollama and vLLM bindings plus OpenAI, Anthropic and OpenRouter APIs. It adds 500+ personalities, cost/speed-based routing, and hooks into Stable Diffusion, ComfyUI, DALL-E, video and musicgen services. The authors say it is in minimal support, to be replaced by the newer lollms project.

- **+** Bindings for local GGUF, ExLlama v2 and transformers plus Ollama, vLLM and hosted APIs
- **+** Image, video and music generation integrations in one UI
- **+** Smart routing picks cheaper or faster models by prompt complexity
- **+** Apache-2.0 license
- **−** Maintainers state it is in minimal support, to be replaced by ParisNeo/lollms
- **−** No built-in authentication; designed for local use only
- **−** Docker image must be built locally; no published image in the README
- **−** Manual install needs submodules plus a per-binding install script

<sub>Docker + Compose · Models: Hugging Face transformers, GGUF/GGML, ExLlama v2, Ollama, vLLM · port 9600 · [Repo](https://github.com/ParisNeo/lollms-webui)</sub>

### [ClaraVerse](https://github.com/claraverse-space/ClaraVerse) <sub>★ 3.9k · NOASSERTION · Aug 2026</sub>

**Private AI workspace with chat, agent crews, workflows and Telegram.**

ClaraVerse is a Go and React workspace (Docker Compose, port 3000) that auto-detects Ollama and LM Studio and also uses OpenAI, Claude, Gemini or any OpenAI-compatible endpoint. It combines chat with Crew multi-agent teams with human review, a visual workflow builder with 200+ integrations, layered AES-256-GCM encrypted memory, knowledge bases, a Telegram channel and the claracli terminal agent.

- **+** Auto-detects Ollama and LM Studio every 2 minutes and imports their models
- **+** Per-user AES-256-GCM encrypted memory with pinned and decaying recall tiers
- **+** 150+ built-in integrations shared across chat, workflows, crew and routines
- **+** AGPL-3.0 with no branding clause or user cap
- **−** Full stack runs MySQL, MongoDB, Redis, SearXNG, Qdrant and an embeddings sidecar
- **−** Single-container mode cannot use knowledge bases or search_knowledge
- **−** 4 GB RAM minimum, 8 GB recommended
- **−** Conversations live in browser IndexedDB by default; sync is optional

<sub>RAM ≥ 4 GB · Docker + Compose · Needs MySQL, MongoDB, Redis, SearXNG, Qdrant (knowledge bases) · Models: Ollama, LM Studio, llama.cpp, OpenAI, Anthropic · port 3000 · [Repo](https://github.com/claraverse-space/ClaraVerse) · [Site](https://claraverse.space)</sub>

### [ChatGPT UI](https://github.com/WongSaang/chatgpt-ui) <sub>★ 1.6k · MIT · May 2026</sub>

**Multi-user ChatGPT-style web client with pluggable databases.**

ChatGPT UI is a web client for ChatGPT-style chat that supports multiple users, multiple languages and several database backends for persistent storage. The front end lives in this repo and the API server in the separate chatgpt-ui-server repository; setup is documented on a GitHub Pages site in English and Chinese.

- **+** Multi-user accounts with persistent history
- **+** Several database backends for storage
- **+** Documentation in English and Chinese
- **−** README is a few lines; no install steps, ports or provider list
- **−** Front end and server are split across two repositories
- **−** Last commit 2026-05-11; README carries a sponsor banner for a paid AI platform

<sub>no GPU · Docker + Compose · [Repo](https://github.com/WongSaang/chatgpt-ui) · [Docs](https://wongsaang.github.io/chatgpt-ui/)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Agent platforms

Visual or code-first builders for agents and workflows, with orchestration, tools and deployment. <sub>12 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Decide between a visual builder (faster to start) and code-first (easier to test and version).
- Check how workflows are exported; vendor-specific JSON makes migration costly.
- Look at the license for the server part; several are AGPL or source-available.

</details>

### [n8n](https://github.com/n8n-io/n8n) <sub>★ 206.9k · NOASSERTION · Oct 2026</sub>

**Visual workflow automation with code steps, AI agent nodes and 1500+ integrations.**

n8n is a fair-code workflow platform that runs as one Docker container (docker.n8n.io/n8nio/n8n, port 5678) and combines a visual canvas with JavaScript, Python and npm code nodes. AI agent and workflow nodes connect to OpenAI, Anthropic, Google or open-source models, with human-approval steps and observability, and 1500+ integrations plus 9,000+ templates cover the rest of the stack.

- **+** 1500+ integrations and 9,000+ ready-made workflow templates
- **+** Code nodes run JavaScript or Python and can pull npm packages
- **+** Single container on port 5678 with one data volume
- **+** Switch model providers without rebuilding the workflow
- **−** Sustainable Use License (fair-code, source-available), not an OSI license
- **−** Some features require a separate n8n Enterprise License
- **−** README states no database, RAM or CPU requirements

<sub>no GPU · Models: OpenAI, Anthropic, Google, open-source models · port 5678 · [Repo](https://github.com/n8n-io/n8n) · [Docs](https://docs.n8n.io)</sub>

### [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) <sub>★ 187.7k · NOASSERTION · Oct 2026</sub>

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

<sub>no GPU · Needs Docker · [Repo](https://github.com/Significant-Gravitas/AutoGPT) · [Demo](https://platform.agpt.co/tour) · [Docs](https://docs.agpt.co)</sub>

### [Dify](https://github.com/langgenius/dify) <sub>★ 158.1k · NOASSERTION · Oct 2026</sub>

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

<sub>RAM ≥ 4 GB · no GPU · Models: OpenAI GPT, Mistral, Llama 3, OpenAI-compatible APIs, dozens of inference providers · port 80 · [Repo](https://github.com/langgenius/dify) · [Demo](https://cloud.dify.ai) · [Docs](https://docs.dify.ai) · [Site](https://dify.ai)</sub>

### [Langflow](https://github.com/langflow-ai/langflow) <sub>★ 155.6k · MIT · Oct 2026</sub>

**Visual flow builder that deploys agents as APIs or MCP servers.**

Langflow is a Python 3.10 to 3.14 visual builder (uv pip install langflow, or the langflowai/langflow Docker image on port 7860) for agents and LLM workflows. Every component is editable Python, flows run in an interactive playground, and a finished flow can be served as an API, exported as JSON for Python apps or exposed as an MCP server. Multi-agent orchestration and LangSmith or LangFuse tracing are built in.

- **+** Any flow becomes an API endpoint or an MCP server for MCP clients
- **+** Component source is Python you can edit inside the builder
- **+** One container on port 7860; no other service in the quick start
- **+** MIT license; desktop builds for Windows and macOS
- **−** README names no model providers, vector stores or resource needs
- **−** No root Dockerfile or compose file; container config lives in the docs
- **−** Enterprise-ready claim is not detailed in the README

<sub>no GPU · port 7860 · [Repo](https://github.com/langflow-ai/langflow) · [Docs](https://docs.langflow.org/get-started-installation) · [Site](https://langflow.org)</sub>

### [Paperclip](https://github.com/paperclipai/paperclip) <sub>★ 98.6k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker · [Repo](https://github.com/paperclipai/paperclip) · [Docs](https://docs.paperclip.ing) · [Site](https://paperclip.ing)</sub>

### [Multica](https://github.com/multica-ai/multica) <sub>★ 52.2k · NOASSERTION · Oct 2026</sub>

**Issue board where coding agents pick up tickets and return pull requests.**

Multica is a Go and Next.js workspace on PostgreSQL 17 where humans and AI coding agents share one issue board. A daemon on your machine spawns any of 26 agent CLIs (Claude Code, Codex, Cursor, Copilot, OpenCode and more); an assigned agent works the issue, comments, and moves it to review, with a replayable execution log, per-run cost, cron autopilots and review gates. Self-host via Docker Compose or Helm.

- **+** Drives 26 agent CLIs; switching providers is a dropdown
- **+** Execution log replays every tool call, command and error with timestamps
- **+** Works with GitHub, GitLab, Gitea and Forgejo, including self-hosted instances
- **+** Roles owner, admin, member plus per-member agent access scopes
- **−** Multica License adds conditions on hosted services, commercial embedding and branding
- **−** Each runtime machine needs agent CLIs installed and signed in; Multica ships no model
- **−** Self-hosted server sends a daily anonymous snapshot unless DO_NOT_TRACK=1
- **−** DingTalk, WeCom and Telegram channels are community-maintained; iOS app is source-only

<sub>no GPU · Docker + Compose · Needs PostgreSQL 17, Docker · [Repo](https://github.com/multica-ai/multica) · [Docs](https://multica.ai/docs) · [Site](https://multica.ai)</sub>

### [Sim](https://github.com/simstudioai/sim) <sub>★ 29.8k · Apache-2.0 · Oct 2026</sub>

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

<sub>RAM ≥ 12 GB · no GPU · Needs PostgreSQL, Docker, Sim Chat API key · Models: Ollama, vLLM · port 3000 · [Repo](https://github.com/simstudioai/sim) · [Docs](https://docs.sim.ai) · [Site](https://sim.ai)</sub>

### [FastGPT](https://github.com/labring/FastGPT) <sub>★ 29.8k · NOASSERTION · Oct 2026</sub>

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

<sub>no GPU · port 3000 · [Repo](https://github.com/labring/FastGPT) · [Docs](https://doc.fastgpt.io/guide/getting-started) · [Site](https://fastgpt.io)</sub>

### [Activepieces](https://github.com/activepieces/activepieces) <sub>★ 24.9k · NOASSERTION · Oct 2026</sub>

**Zapier-style automation whose 280+ pieces double as MCP servers.**

Activepieces is a TypeScript workflow automation tool with a no-code builder (loops, branches, retries, HTTP, npm code steps, versioned flows) and a pieces framework where every integration is an npm package. All 280+ pieces are exposed as MCP servers for Claude Desktop, Cursor or Windsurf, native AI pieces and an AI SDK build agents inside flows, and human-in-the-loop steps, chat and form interfaces are included.

- **+** Every piece is also an MCP server usable from Claude Desktop, Cursor or Windsurf
- **+** Pieces are TypeScript npm packages with hot reload for local development
- **+** 60% of pieces contributed by the community; all published on npmjs.com
- **+** Community Edition is MIT
- **−** Enterprise features ship under a separate commercial license
- **−** README has no install commands, ports or resource figures; deploy is a docs link
- **−** Model providers beyond an OpenAI piece are not named in the README

<sub>no GPU · Docker + Compose · Models: OpenAI · [Repo](https://github.com/activepieces/activepieces) · [Docs](https://www.activepieces.com/docs) · [Site](https://activepieces.com)</sub>

### [Skyvern](https://github.com/Skyvern-AI/skyvern) <sub>★ 23.2k · AGPL-3.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · port 8080 · [Repo](https://github.com/Skyvern-AI/skyvern) · [Demo](https://app.skyvern.com) · [Docs](https://www.skyvern.com/docs/) · [Site](https://www.skyvern.com)</sub>

### [Agent Zero](https://github.com/agent0ai/agent-zero) <sub>★ 19.4k · NOASSERTION · Sep 2026</sub>

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

<sub>no GPU · Needs Docker · Models: OpenAI Codex plan (OAuth) · port 80 · [Repo](https://github.com/agent0ai/agent-zero) · [Site](https://agent-zero.ai)</sub>

### [Botpress](https://github.com/botpress/botpress) <sub>★ 14.9k · MIT · Oct 2026</sub>

**SDK, CLI and open-source integrations for the Botpress Cloud bot platform.**

This repository holds the TypeScript devtools for Botpress Cloud: the @botpress/cli (bp init, bp deploy), the @botpress/sdk and typed client, every public integration on the Botpress Hub, and example bots written as code. Bots themselves are built in the hosted Botpress Studio and powered by OpenAI; the on-premise server is the separate Botpress v12 repository. Everything here is MIT.

- **+** All public Hub integrations are open source and contributable with bp init and bp deploy
- **+** Typed TypeScript SDK and API client for building integrations and bots as code
- **+** MIT license for every package in the repository
- **−** The chatbot platform (Studio, runtime) is Botpress Cloud, not something you host from here
- **−** Self-hosted server is the separate, older Botpress v12 repository
- **−** Bots-as-code is described as not the recommended way to build bots
- **−** Plugins section is marked coming soon

<sub>no GPU · Docker · Models: OpenAI · [Repo](https://github.com/botpress/botpress) · [Demo](https://app.botpress.cloud) · [Docs](https://botpress.com/docs) · [Site](https://botpress.com)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## RAG and knowledge

Document Q&A, knowledge bases and enterprise search over your own files and data. <sub>15 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Match the ingestion formats you need (PDF with tables, Office, web, Confluence) before anything else.
- Check which embedding models and vector stores are supported and whether they can run offline.
- Look for citations in answers; without them, RAG output is hard to trust.

</details>

### [RAGFlow](https://github.com/infiniflow/ragflow) <sub>★ 91.8k · Apache-2.0 · Oct 2026</sub>

**RAG engine with deep document parsing, agentic retrieval and knowledge compilation.**

RAGFlow parses Word, slides, Excel, scans and web pages with in-process layout analysis, OCR and table recognition, chunks by template and answers with traceable citations. Version 1.0 runs as one Go service deployed with Docker Compose beside MySQL, Elasticsearch or Infinity, MinIO, NATS and Kvrocks. For teams building document Q&A and agent workflows over complex enterprise files.

- **+** DeepDoc layout, OCR and table parsing run in-process on CPU
- **+** Chunk visualization and traceable citations let humans check retrieval
- **+** Agentic retrieval with Low to Ultra thinking modes for multi-step questions
- **+** Knowledge Compilation builds wikis, graphs, mind maps and timelines from datasets
- **−** Needs 6 backing services (MySQL, Elasticsearch/Infinity, MinIO, NATS, Kvrocks, ClickHouse)
- **−** Recommended 4 cores, 16 GB RAM and 50 GB disk before any local models
- **−** 1.0 Go rewrite is still rc1 as of 2026-09-29
- **−** Elasticsearch path requires vm.max_map_count >= 262144 on the host

<sub>RAM ≥ 16 GB · no GPU · Docker · Needs MySQL, Elasticsearch or Infinity, MinIO, NATS JetStream, Kvrocks, ClickHouse · Models: external LLM, embedding and reranker providers set by URL and API key · port 80 · [Repo](https://github.com/infiniflow/ragflow) · [Demo](https://cloud.ragflow.io) · [Docs](https://ragflow.io/docs/dev/) · [Site](https://ragflow.io/)</sub>

### [PrivateGPT](https://github.com/zylon-ai/private-gpt) <sub>★ 57.6k · Apache-2.0 · Oct 2026</sub>

**Anthropic-style API layer for private RAG on local inference servers.**

PrivateGPT 1.0 is an API server shaped like the Anthropic Messages API, adding file ingestion, retrieval with citations, web search, code execution, MCP and direct database or CSV querying. It runs no models; it calls any OpenAI-compatible server (Ollama, llama.cpp, vLLM) through OPENAI_API_BASE. A workbench UI at /ui on port 8080 exists for testing; the API is the product.

- **+** Anthropic Messages API shape, so Claude Code, Claude Desktop and Office add-ins can target it
- **+** Backend-agnostic: any OpenAI-compatible inference server via OPENAI_API_BASE
- **+** Built-in database and CSV querying, no extra tool server needed
- **+** Installs with brew or uv tool install; Docker also documented
- **−** Runs no models; a separate inference server and embedding server are required
- **−** No prompt caching and no OAuth or organizations
- **−** Skills support is marked basic; structured output depends on the backend
- **−** RBAC, LDAP, connectors and audit logs exist only in the commercial Zylon platform

<sub>no GPU · Docker · Needs OpenAI-compatible inference server (Ollama, llama.cpp, vLLM) · Models: any model behind an OpenAI-compatible /v1/chat/completions endpoint · port 8080 · [Repo](https://github.com/zylon-ai/private-gpt) · [Docs](https://docs.privategpt.dev/)</sub>

### [LightRAG](https://github.com/HKUDS/LightRAG) <sub>★ 40.0k · MIT · Sep 2026</sub>

**Graph-plus-vector RAG server with web UI and Ollama-compatible API.**

LightRAG indexes documents into a knowledge graph plus vector store and queries both layers, as a lighter alternative to Microsoft GraphRAG. The server package ships a REST API, a web UI for inserting and visualizing the graph, and Ollama-compatible /api routes for chat frontends. Parsing runs via MinerU, Docling or a native engine; production storage goes to PostgreSQL, Neo4j, MongoDB, Milvus or OpenSearch.

- **+** Dual-level graph and vector retrieval with fewer LLM calls than community-report GraphRAG
- **+** Incremental updates and document deletion with graph regeneration from the LLM cache
- **+** Three parsing engines and four chunking strategies, including paragraph-semantic
- **+** Separate LLM settings per role: extract, query, keywords and VLM
- **−** Default KV, vector and graph stores are in-memory with file persistence, not for production
- **−** Server binds 0.0.0.0 with every endpoint public until auth is configured
- **−** Ollama-compatible /api routes stay open even with auth unless WHITELIST_PATHS is set
- **−** docx smart headings and SVG rendering need extra spaCy models and libcairo

<sub>no GPU · Docker + Compose · Needs PostgreSQL (recommended for production), Neo4j (optional), MongoDB (optional), Milvus (optional), OpenSearch (optional) · Models: LLM and embedding providers configured in .env, tested with open models such as Qwen3-30B-A3B · [Repo](https://github.com/HKUDS/LightRAG)</sub>

### [Open Notebook](https://github.com/lfnovo/open-notebook) <sub>★ 39.9k · MIT · Oct 2026</sub>

**Self-hosted NotebookLM alternative with podcasts and 20+ model providers.**

Open Notebook collects PDFs, audio, video, web pages and Office files into notebooks and offers cited chat, full-text and vector search, notes and multi-speaker podcast generation. It runs as two containers (SurrealDB plus a FastAPI/Next.js app) and talks to OpenAI, Anthropic, Google, Mistral, Groq, Ollama, LM Studio or any OpenAI-compatible server. A REST API and MCP integration expose the same features.

- **+** 20+ providers, including Ollama and LM Studio for fully local runs
- **+** Podcasts with 1 to 4 speakers and custom episode profiles
- **+** REST API on port 5055 and an MCP server for Claude Desktop or VS Code
- **+** Two-service Docker Compose; keys stored encrypted with OPEN_NOTEBOOK_ENCRYPTION_KEY
- **−** Single-user; multi-user support is only a future direction in VISION.md
- **−** No password by default and ports 8502/5055 bind to all interfaces
- **−** Anthropic and Groq offer no embeddings, so a second provider is needed
- **−** UI in 14 languages but provider setup is manual per model type

<sub>no GPU · Docker + Compose · Needs SurrealDB · Models: OpenAI, Anthropic, Google, Mistral, Groq, DeepSeek, xAI, OpenRouter, Cohere, Ollama, LM Studio, oMLX and any OpenAI-compatible endpoint · port 8502 · [Repo](https://github.com/lfnovo/open-notebook) · [Site](https://www.open-notebook.ai)</sub>

### [WeKnora](https://github.com/Tencent/WeKnora) <sub>★ 32.6k · NOASSERTION · Oct 2026</sub>

**Enterprise knowledge base combining RAG Q&A, agents and generated wikis.**

WeKnora turns team documents into knowledge bases with three modes: cited RAG answers, an agent that runs multi-step tasks with skills in Docker, E2B or Cube sandboxes, and auto-generated wiki pages with a knowledge graph. It syncs from Feishu, Confluence, GitLab, Notion and RSS, answers in WeCom, Slack and Telegram, and exposes an MCP server. Deploy with Docker Compose, Helm or one Lite binary on SQLite.

- **+** 29 built-in model vendors including OpenAI, DeepSeek, Qwen, Gemini, LiteLLM and Ollama
- **+** Lite single binary with SQLite and in-memory queue for low-resource hosts
- **+** Workspace RBAC with four roles, per-resource ownership and audit log
- **+** Per-workspace MCP endpoints with own token, scope and rate limit
- **−** Many integrations target the Chinese ecosystem (WeChat, Feishu, DingTalk, Yuque)
- **−** Sandbox commands run as root since v0.8.2
- **−** Maintainers advise against exposing it to the public internet
- **−** Desktop app has no published installer; hardware requirements live in external docs

<sub>no GPU · Compose · Needs Neo4j (optional profile), MinIO (optional profile), Langfuse (optional profile) · Models: OpenAI, DeepSeek, Qwen, Zhipu, Hunyuan, Gemini, MiniMax, NVIDIA, LiteLLM, Ollama · port 80 · [Repo](https://github.com/Tencent/WeKnora) · [Docs](https://weknora.weixin.qq.com/docs/) · [Site](https://weknora.weixin.qq.com)</sub>

### [Kotaemon](https://github.com/Cinnamon/kotaemon) <sub>★ 25.8k · Apache-2.0 · May 2026</sub>

**Gradio RAG UI with hybrid retrieval, citations and multi-user login.**

Kotaemon is a Gradio web app for question answering over uploaded documents, with hybrid full-text plus vector retrieval, reranking, citations shown in an in-browser PDF viewer and ReAct or ReWOO agents. It supports OpenAI, Azure, Cohere, Groq, Ollama and GGUF via llama-cpp-python, with Elasticsearch, LanceDB, ChromaDB, Milvus or Qdrant storage. Docker images come in lite, full and ollama variants on port 7860.

- **+** Hybrid retriever plus reranking by default, with low-relevance warnings
- **+** Citations open in a PDF viewer with highlights and relevance scores
- **+** Multi-user login with private and public collections
- **+** GraphRAG options: nano-graphrag, LightRAG or Microsoft GraphRAG
- **−** Default login is admin/admin
- **−** GraphRAG extras cause hnswlib version conflicts that need manual pip fixes
- **−** Only PDF, HTML, MHTML and XLSX without the larger full image
- **−** Last commit 2026-05-30; MS GraphRAG indexing works only with OpenAI or Ollama

<sub>no GPU · Docker · Needs Elasticsearch, LanceDB, ChromaDB, Milvus or Qdrant (optional stores), Unstructured (optional, for .doc/.docx and more) · Models: OpenAI, Azure OpenAI, Cohere, Groq, Ollama · port 7860 · [Repo](https://github.com/Cinnamon/kotaemon) · [Demo](https://huggingface.co/spaces/cin-model/kotaemon-demo) · [Docs](https://cinnamon.github.io/kotaemon/)</sub>

### [MaxKB](https://github.com/1Panel-dev/MaxKB) <sub>★ 22.9k · GPL-3.0 · Oct 2026</sub>

**Enterprise knowledge-base agent platform with RAG, workflows and MCP tools.**

MaxKB runs as one Docker container (port 8080, state in one volume) with a RAG pipeline that uploads or crawls documents, a workflow engine with function library and MCP tool use, and zero-code embedding into other systems. It works with private models (DeepSeek, Llama, Qwen) and public APIs (OpenAI, Claude, Gemini, MiniMax) and handles text, image, audio and video. Built on Django, LangChain and PostgreSQL.

- **+** Single docker run with all data under one mounted volume
- **+** Workflow engine with function library and MCP tool calling
- **+** Crawls online documents into the knowledge base automatically
- **+** Multimodal input and output: text, image, audio, video
- **−** GPL-3.0 limits bundling into proprietary products
- **−** Ships with default admin password MaxKB@123..
- **−** README gives no hardware guidance or provider configuration detail
- **−** Detailed docs are on maxkb.cn, partly in Chinese

<sub>no GPU · Models: OpenAI, Claude, Gemini, MiniMax, DeepSeek, Llama, Qwen as private models · port 8080 · [Repo](https://github.com/1Panel-dev/MaxKB)</sub>

### [DB-GPT](https://github.com/eosphoros-ai/DB-GPT) <sub>★ 20.1k · MIT · Oct 2026</sub>

**Agentic data assistant that writes SQL and code over your databases.**

DB-GPT connects to databases, CSV and Excel files, warehouses and knowledge bases, then plans tasks, writes SQL and Python, runs them in sandboxes and produces charts, dashboards and HTML reports. It installs with pip install dbgpt-app (Python 3.10+) plus a setup wizard and serves a web UI on port 5670, with OpenAI-compatible, DashScope, Moonshot and MiniMax profiles and local models via vLLM or llama.cpp.

- **+** NL-to-SQL plus Python analysis with sandboxed execution
- **+** Outputs charts, dashboards and HTML reports, not only answers
- **+** Skills importable from GitHub for repeatable analysis workflows
- **+** Local serving via vLLM or llama.cpp and a Text2SQL fine-tuning hub
- **−** Recommended install pipes a remote script into bash
- **−** Docs and community largely on dbgpt.cn; Docker and GPU setup only there
- **−** Text2SQL fine-tune list stops at older models such as LLaMA-2 and ChatGLM2
- **−** Default pip install bundles ChromaDB only; other vector stores need extras

<sub>GPU optional · Compose · Models: OpenAI-compatible APIs, DashScope/Tongyi, Moonshot (Kimi), MiniMax, local models via vLLM or llama.cpp: DeepSeek, Qwen, GLM, Llama, Gemma, Yi · port 5670 · [Repo](https://github.com/eosphoros-ai/DB-GPT) · [Docs](http://docs.dbgpt.cn/docs/overview/) · [Site](http://dbgpt.cn/)</sub>

### [DeepWiki-Open](https://github.com/AsyncFuncAI/deepwiki-open) <sub>★ 18.1k · MIT · Sep 2026</sub>

**Generates browsable wikis and diagrams for GitHub, GitLab and Bitbucket repos.**

DeepWiki-Open takes a repository URL from GitHub, GitLab or Bitbucket, analyzes the code structure, generates documentation and diagrams, organizes them into a navigable wiki and builds a codemap for guided tours. The repo ships a Dockerfile and compose file. The README now points to a 2.0 release called Grok Wiki distributed as a download from grok-wiki.com and no longer documents configuration.

- **+** Works with GitHub, GitLab and Bitbucket repositories
- **+** Produces diagrams and codemap guided tours, not only prose
- **+** Dockerfile and docker-compose in the repo; MIT license
- **−** README no longer documents setup, ports or supported model providers
- **−** 2.0 is pushed as a separate download at grok-wiki.com
- **−** No hardware guidance; single-maintainer project

<sub>no GPU · Docker + Compose · [Repo](https://github.com/AsyncFuncAI/deepwiki-open) · [Site](https://grok-wiki.com)</sub>

### [SurfSense](https://github.com/MODSetter/SurfSense) <sub>★ 16.3k · NOASSERTION · Oct 2026</sub>

**Offline NotebookLM alternative that turns documents into decks, reports and podcasts.**

SurfSense indexes local PDFs, Office files and images into SQLite, answers with citations and turns sources into summaries, flashcards, quizzes, mind maps, editable pptx/docx/xlsx and offline podcasts (Kokoro-82M). It runs a local Qwen3 (six sizes from 0.5 GB) or any OpenAI-compatible API, egress off by default. The supported path is a desktop installer; the Docker stack is community-supported.

- **+** Parser, retrieval model and podcast voice ship in the installer; works with networking off
- **+** Egress panel off by default, no telemetry or crash reporting
- **+** Produces editable pptx, docx and xlsx files rather than chat only
- **+** No account required; keys stored in the OS keychain
- **−** Primary product is a desktop app, not a server
- **−** Self-hosted Docker stack has no SLA and no hosted service behind it
- **−** Hosted web app retired; export window closes 2026-10-18
- **−** Plugins and priority support are behind a paid licence; no video overviews

<sub>no GPU · Models: local Qwen3 in six sizes from 0.5 GB, any OpenAI-compatible API · [Repo](https://github.com/MODSetter/SurfSense) · [Docs](https://www.surfsense.com/docs) · [Site](https://www.surfsense.com/)</sub>

### [Paperless-AI](https://github.com/clusterzx/paperless-ai) <sub>★ 6.0k · MIT · Mar 2026</sub>

**Auto-tags Paperless-ngx documents and adds RAG chat over the archive.**

Paperless-AI watches a Paperless-ngx instance, sends new documents to OpenAI, Ollama, DeepSeek, OpenRouter, Gemini or other OpenAI-compatible backends and writes back title, tags, document type and correspondent. It adds RAG chat over the whole archive and a manual review page at /manual. The maintainer has declared the repo unmaintained pending a rewrite.

- **+** Assigns title, tags, document type and correspondent on new documents automatically
- **+** RAG chat answers questions across the full Paperless archive
- **+** Rules limit which documents get processed; manual mode for sensitive files
- **+** Ollama support keeps processing local
- **−** Repo marked not maintained; rewrite and future uncertain
- **−** Container must be restarted after first setup to build the RAG index
- **−** No port, hardware or env var details in the README; see the wiki
- **−** Paperless-ngx is adding native AI, which may supersede it

<sub>no GPU · Docker + Compose · Needs Paperless-ngx · Models: Ollama (Mistral, Llama, Phi-3, Gemma-2), OpenAI, DeepSeek, OpenRouter, Perplexity, Together, LiteLLM, vLLM, Fastchat, Gemini · [Repo](https://github.com/clusterzx/paperless-ai) · [Docs](https://github.com/clusterzx/paperless-ai/wiki/2.-Installation)</sub>

### [PipesHub](https://github.com/pipeshub-ai/pipeshub-ai) <sub>★ 3.8k · Apache-2.0 · Oct 2026</sub>

**Permission-aware search and agent context over 50+ workplace systems.**

PipesHub indexes Slack, Google Drive, GitHub, Microsoft 365, Notion and 50+ systems into a knowledge graph (Neo4j or ArangoDB), Qdrant and MongoDB, then serves permission-aware search with block-level citations and hands the same context to agents over MCP and SDKs. Access is checked against source permissions at query time. A one-command installer writes Compose files and starts the stack on port 3000.

- **+** Permission filtering resolved against the source system at query time
- **+** 50+ connectors with real-time and scheduled indexing
- **+** MCP server plus Python, TypeScript and Go SDKs
- **+** Kubernetes deployment with HA defaults; slim or full Compose profiles
- **−** Needs Neo4j or ArangoDB, Qdrant, MongoDB, Redis, and Kafka at scale
- **−** Installer is curl piped to bash
- **−** Audio and video are stored but not indexed yet
- **−** Plain-HTTP cloud deployments show a white screen; TLS termination required

<sub>no GPU · Docker · Needs Neo4j or ArangoDB, Qdrant, MongoDB, Redis, Kafka (larger deployments) · Models: any LLM provider, bring your own model, Ollama, local embedding server by default · port 3000 · [Repo](https://github.com/pipeshub-ai/pipeshub-ai) · [Docs](https://docs.pipeshub.com/) · [Site](https://www.pipeshub.com/)</sub>

### [Morphik](https://github.com/morphik-org/morphik-core) <sub>★ 3.7k · NOASSERTION · Oct 2026</sub>

**Multimodal retrieval engine for visually rich PDFs, images and video.**

Morphik Core is a retrieval engine for visually rich documents: it embeds page images with ColPali so charts, tables and diagrams are searchable through one endpoint covering PDFs, images and video, and extracts metadata such as bounding boxes and labels by rules. It is used via a Python SDK, REST API, MCP or the Console web UI. Self-hosting is documented separately and offered with limited support.

- **+** ColPali retrieval over page images instead of extracted text
- **+** One search endpoint for images, PDFs and video
- **+** Rule-based metadata extraction with bounding boxes and classification
- **+** Python SDK, REST API and MCP access
- **−** BSL 1.1: commercial use above US $2,000 per month revenue needs a paid key
- **−** Self-hosted deployments get no full support from the maintainers
- **−** README centers on the hosted dev.morphik.ai service, not self-hosting
- **−** Parent company now focuses on back-office AI workers; Core is a side product

<sub>no GPU · Compose · Models: ColPali multimodal embeddings · [Repo](https://github.com/morphik-org/morphik-core) · [Demo](https://dev.morphik.ai) · [Docs](https://dev.morphik.ai/docs) · [Site](https://morphik.ai)</sub>

### [paperless-gpt](https://github.com/icereed/paperless-gpt) <sub>★ 2.7k · MIT · Oct 2026</sub>

**LLM-powered OCR, titles, tags and document links for Paperless-ngx.**

paperless-gpt attaches to Paperless-ngx and uses OpenAI, Ollama, Mistral, Azure or Anthropic models to generate titles, tags, correspondents and custom fields, link related documents by reference number, and run OCR via vision models, Google Document AI, Azure Document Intelligence or Docling. OCR output can be written back as searchable PDFs. One container on port 8080; prompts editable in the web UI.

- **+** LLM or VLM OCR produces searchable PDFs with positioned text layers
- **+** Links invoices, amendments and letters via exact reference-number lookup
- **+** Per-document-type AI workflows with trigger tags, testable before saving
- **+** Four OCR providers including a self-hosted Docling server
- **−** No built-in authentication; listens on all interfaces by default
- **−** OCR limited to 5 pages per document unless OCR_LIMIT_PAGES is raised
- **−** PDF_REPLACE deletes the original document; flagged dangerous by the maintainer
- **−** Requires a running Paperless-ngx 2.20.x or 3.0 beta

<sub>no GPU · Docker + Compose · Needs Paperless-ngx, optional OCR: Google Document AI, Azure Document Intelligence, Docling · Models: OpenAI (gpt-4o), Ollama (qwen3:8b, minicpm-v), Mistral, Azure OpenAI, Anthropic · port 8080 · [Repo](https://github.com/icereed/paperless-gpt)</sub>

### [Docling Serve](https://github.com/docling-project/docling-serve) <sub>★ 1.8k · MIT · Oct 2026</sub>

**Docling document conversion as an HTTP API with playground UI.**

Docling Serve wraps the Docling document converter in a FastAPI service: POST a URL or file to /v1/convert/source and get structured text back, with OpenAPI docs at /docs and a playground UI at /ui on port 5001. Container images cover CPU (4.4 GB), CUDA 12.8 (11.4 GB) and CUDA 13.0 on amd64 and arm64; a ROCm image builds locally. Suited to RAG pipelines that need a document-to-text service.

- **+** Single container with API, OpenAPI docs and a playground UI
- **+** Stable v1 API after migration
- **+** CPU and CUDA 12.8/13.0 images for amd64 and arm64
- **+** Converts from HTTP sources or uploads in one call
- **−** Images are large: 4.4 GB CPU, 8.7 GB base amd64, 11.4 GB CUDA
- **−** CUDA images carry no latest tag; pin explicit versions
- **−** ROCm image is not published; build it yourself
- **−** Slim images without bundled weights are only announced

<sub>GPU optional · Models: bundled Docling parsing models · port 5001 · [Repo](https://github.com/docling-project/docling-serve)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Model serving

Inference engines and model servers that expose local models over an API. <sub>18 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Pick by hardware first (CPU, NVIDIA, AMD, Apple Silicon) and by model format (GGUF, safetensors).
- Throughput engines (continuous batching, paged attention) need GPUs; single-user servers do not.
- An OpenAI-compatible API keeps the rest of your stack portable.

</details>

### [Ollama](https://github.com/ollama/ollama) <sub>★ 182.6k · MIT · Oct 2026</sub>

**Runs open-weight models locally behind a CLI and REST API.**

Ollama runs open-weight models locally with a CLI and a REST API on port 11434, pulling models from its own library (for example gemma4) and using llama.cpp as the inference backend. Install scripts cover macOS, Windows and Linux, and an official Docker image exists. The ollama launch command wires it into coding agents such as Claude Code, Codex, Copilot CLI and OpenCode, or into OpenClaw as a chat assistant.

- **+** One command pulls and runs a model; REST API on 11434
- **+** Official Docker image plus Python and JavaScript libraries
- **+** ollama launch integrates with Claude Code, Codex, Copilot CLI, OpenCode
- **+** Broad ecosystem: dozens of web, desktop and IDE clients listed
- **−** Single inference backend: llama.cpp
- **−** Install is a curl piped to sh script
- **−** README gives no RAM or VRAM guidance per model size
- **−** Models come from Ollama's own registry; others need import steps

<sub>GPU optional · Docker · Models: Ollama library models (e.g. gemma4), GGUF via llama.cpp · port 11434 · [Repo](https://github.com/ollama/ollama) · [Docs](https://docs.ollama.com/quickstart) · [Site](https://ollama.com)</sub>

### [llama.cpp](https://github.com/ggml-org/llama.cpp) <sub>★ 130.7k · MIT · Oct 2026</sub>

**C/C++ inference engine serving GGUF models over an OpenAI-compatible API.**

llama.cpp is a C/C++ inference engine for LLMs and VLMs with no dependencies, built on ggml. llama serve starts an OpenAI-compatible API server with a built-in web UI, pulling GGUF models straight from Hugging Face, with 1.5 to 8-bit quantization and CPU+GPU hybrid offload for models larger than VRAM. Backends cover CUDA, HIP, Metal, Vulkan, SYCL, OpenCL, CANN, MUSA and WebGPU.

- **+** Plain C/C++ with no runtime dependencies; prebuilt binaries and Docker
- **+** Backends for NVIDIA, AMD, Apple Metal, Intel SYCL, Vulkan, Ascend, Moore Threads
- **+** Hybrid CPU+GPU offload runs models larger than available VRAM
- **+** Built-in web UI and OpenAI-compatible server via llama serve
- **−** GGUF model format only
- **−** README gives no port, auth or sizing guidance; see tools/server docs
- **−** Install script is curl piped to sh; otherwise build from source
- **−** OpenVINO backend still in progress

<sub>GPU optional · Models: GGUF models from Hugging Face (e.g. Qwen3.5-0.8B-GGUF) · [Repo](https://github.com/ggml-org/llama.cpp) · [Site](https://llama.app)</sub>

### [vLLM](https://github.com/vllm-project/vllm) <sub>★ 93.4k · Apache-2.0 · Oct 2026</sub>

**High-throughput LLM serving engine with OpenAI and Anthropic APIs.**

vLLM is a Python serving engine for Hugging Face models that batches requests continuously with PagedAttention, prefix caching and speculative decoding, exposing an OpenAI-compatible API plus Anthropic Messages API and gRPC. It covers 200+ architectures (dense, MoE, multimodal, embedding) with FP8, INT8, GPTQ, AWQ and GGUF quantization and tensor, pipeline and expert parallelism.

- **+** Continuous batching with PagedAttention for high multi-user throughput
- **+** 200+ Hugging Face architectures including MoE, multimodal and embedding models
- **+** OpenAI, Anthropic Messages and gRPC endpoints with tool calling and structured output
- **+** Runs on NVIDIA, AMD, Intel GPUs, CPUs, TPUs, Gaudi, Ascend via plugins
- **−** No web UI; API server only
- **−** README gives no VRAM, port or model-size guidance
- **−** Heavy Python, PyTorch and CUDA dependency chain; no single binary
- **−** Most optimized kernels target NVIDIA and AMD GPUs; CPU path is secondary

<sub>GPU optional · Models: 200+ Hugging Face architectures: Llama, Qwen, Gemma, Mixtral, DeepSeek-V3, GPT-OSS, LLaVA, Qwen-VL, E5-Mistral · [Repo](https://github.com/vllm-project/vllm) · [Docs](https://docs.vllm.ai) · [Site](https://vllm.ai)</sub>

### [LocalAI](https://github.com/mudler/LocalAI) <sub>★ 49.4k · MIT · Oct 2026</sub>

**One OpenAI-compatible server for text, speech, image and video models.**

LocalAI is a Go server on port 8080 with OpenAI, Anthropic, ElevenLabs and Ollama-compatible APIs for text, vision, speech, image and video. Backends (llama.cpp, vLLM, SGLang, whisper.cpp, diffusers, MLX, 60+ total) ship as separate OCI images pulled on demand; containers exist for CPU, CUDA, ROCm, Intel and Vulkan. It adds API keys, quotas and OIDC, agents with MCP, and a PostgreSQL/NATS distributed mode.

- **+** Small core; 60+ backends installed on demand as OCI images
- **+** OpenAI, Anthropic, ElevenLabs and Ollama API compatibility in one server
- **+** Multi-user: API keys, per-user quotas, role-based access, OIDC
- **+** Container images for CPU, CUDA 12/13, ROCm, Intel oneAPI, Vulkan, Jetson
- **−** First model load pulls backend images; needs network and disk space
- **−** macOS DMG is unsigned and needs quarantine removal
- **−** Distributed mode requires PostgreSQL and NATS
- **−** Very wide scope (agents, biometrics, video) increases configuration surface

<sub>GPU optional · Docker + Compose · Needs PostgreSQL and NATS (distributed mode only) · Models: GGUF via llama.cpp, vLLM, SGLang, transformers, MLX, diffusers, whisper.cpp backends, models from gallery, Hugging Face, Ollama registry, OCI images, YAML · port 8080 · [Repo](https://github.com/mudler/LocalAI) · [Docs](https://localai.io/basics/getting_started/) · [Site](https://localai.io/)</sub>

### [Text Generation Web UI](https://github.com/oobabooga/textgen) <sub>★ 47.7k · AGPL-3.0 · Aug 2026</sub>

**Local LLM chat UI and API with five switchable loader backends.**

TextGen runs local LLMs behind a chat UI and an OpenAI/Anthropic-compatible API with tool calling and MCP, with llama.cpp, ik_llama.cpp, Transformers, ExLlamaV3 or TensorRT-LLM loaders switchable without restart. Portable builds for Linux, Windows and macOS bundle CUDA, Vulkan, ROCm or CPU dependencies for GGUF; the full install adds LoRA training, image generation and extensions. Web UI on port 7860.

- **+** Portable builds with all dependencies for CUDA, Vulkan, ROCm and CPU
- **+** Five loaders switchable without restarting
- **+** OpenAI and Anthropic-compatible API with tool calling and MCP servers
- **+** LoRA training and diffusers image generation in the same app
- **−** Full install needs ~10 GB disk and PyTorch; portable build is GGUF only
- **−** Multi-user mode does not save chat histories; meant for small trusted teams
- **−** Docker needs per-GPU Dockerfile symlinks and manual .env edits
- **−** AGPL-3.0 license

<sub>GPU optional · Models: GGUF via llama.cpp and ik_llama.cpp, Transformers safetensors, EXL3 via ExLlamaV3, TensorRT-LLM · port 7860 · [Repo](https://github.com/oobabooga/textgen)</sub>

### [SGLang](https://github.com/sgl-project/sglang) <sub>★ 36.9k · Apache-2.0 · Oct 2026</sub>

**Inference framework for LLMs, VLMs and diffusion models on many accelerators.**

SGLang is an inference framework for language, vision-language and diffusion models aimed at agentic workloads, RL rollouts and large-scale serving, shipped as a Docker image or Python package. It runs on NVIDIA (A100 to B300, RTX 30/40/50, Jetson), AMD MI300, Google TPU, Intel Arc and Xeon, Apple Silicon, Ascend and Moore Threads. SGLang Diffusion adds image and video generation.

- **+** Hardware from NVIDIA and AMD to TPU, Intel, Apple Silicon and Ascend NPUs
- **+** Hierarchical KV cache across GPU, host memory and storage (HiCache, Mooncake, LMCache)
- **+** Diffusion image and video generation in the same package
- **+** Integrations with verl, slime, AReaL, Ray Serve, llm-d and NVIDIA Dynamo
- **−** README has no launch command; quickstart and cookbook are external
- **−** uv install requires --prerelease=allow
- **−** No port, VRAM or model-size guidance in the README
- **−** Trainium, Cambricon and Qualcomm support still in progress

<sub>GPU optional · Models: large language, vision-language and diffusion models (see cookbook) · [Repo](https://github.com/sgl-project/sglang) · [Docs](https://docs.sglang.io/) · [Site](https://www.sglang.io/)</sub>

### [llamafile](https://github.com/mozilla-ai/llamafile) <sub>★ 26.2k · NOASSERTION · Sep 2026</sub>

**Single-file executables that bundle llama.cpp with model weights.**

llamafile packages llama.cpp and model weights into one executable using Cosmopolitan Libc, so a downloaded .llamafile runs on Linux, macOS, Windows and BSD across CPU architectures with no install and serves a local web UI and API. Since 0.10 it tracks upstream llama.cpp closely for newer models, and whisperfile applies the same packaging to speech-to-text. Maintained by Mozilla.ai.

- **+** Single file, no installation, runs across OSes and CPU architectures
- **+** 0.10 build system tracks upstream llama.cpp for recent model support
- **+** Can run external GGUF weights with the bare llamafile binary
- **+** whisperfile gives single-file transcription and translation
- **−** Windows cannot run executables above 4 GB; larger models need external weights
- **−** 0.10.x dropped some classic features; older releases remain for those
- **−** Pre-built llamafiles limited to Mozilla.ai's Hugging Face uploads
- **−** One model per file; not a multi-model server

<sub>GPU optional · Models: GGUF (bundled or external), e.g. Qwen3.5-0.8B · [Repo](https://github.com/mozilla-ai/llamafile) · [Docs](https://docs.mozilla.ai/llamafile)</sub>

### [KTransformers](https://github.com/kvcache-ai/ktransformers) <sub>★ 19.6k · Apache-2.0 · Oct 2026</sub>

**CPU-GPU hybrid inference and fine-tuning for very large MoE models.**

KTransformers is a research framework for CPU-GPU heterogeneous inference and fine-tuning of large MoE models. Its kt-kernel package provides Intel AMX and AVX512/AVX2 INT4/INT8 kernels with NUMA-aware expert placement, so DeepSeek-V3/R1, Kimi K2.x and GLM-5.x run with hot experts on GPU and cold ones on CPU, served through SGLang. A LlamaFactory integration fine-tunes the same models with LoRA or full parameters.

- **+** DeepSeek-R1 class models on one 24 GB GPU plus large host RAM
- **+** Day-0 support for DeepSeek-V4, Kimi K2.x, GLM-5.x and MiniMax-M3
- **+** LoRA and full fine-tuning of MoE models on 4x RTX 4090 via LlamaFactory
- **+** Ascend NPU, AMD ROCm and Intel Arc paths beyond NVIDIA
- **−** Serving goes through SGLang (sglang-kt); the standalone framework is archived
- **−** DeepSeek-R1 example needs 382 GB DRAM alongside 24 GB VRAM
- **−** Fastest kernels need Intel AMX or AVX512; AVX2 support is newer
- **−** Research project; some docs and support channels are Chinese-only

<sub>GPU required · Needs SGLang (serving), LLaMA-Factory (fine-tuning) · Models: DeepSeek-V3/R1/V4-Flash, Kimi K2 to K2.6, GLM-5 to 5.3, MiniMax-M2.x/M3, Qwen3-MoE, Qwen3-Next · [Repo](https://github.com/kvcache-ai/ktransformers) · [Docs](https://kvcache-ai.github.io/ktransformers/)</sub>

### [OpenLLM](https://github.com/bentoml/OpenLLM) <sub>★ 12.6k · Apache-2.0 · May 2026</sub>

**One-command OpenAI-compatible endpoints for curated open LLMs.**

OpenLLM serves open LLMs as OpenAI-compatible APIs with one command: pip install openllm, then openllm serve llama3.2:1b starts a vLLM-backed server on port 3000 with a chat UI at /chat. Models come as prebuilt Bentos from a curated repository (Llama 3.x and 4, Qwen2.5, Mistral, Phi-4, Gemma, DeepSeek R1) and the catalog states the GPU each needs. openllm deploy pushes the same Bento to BentoCloud.

- **+** One command gives an OpenAI API plus /chat UI on port 3000
- **+** Catalog lists the required GPU per model tag (12 GB to 16x80 GB)
- **+** vLLM backend for serving
- **+** Same Bento deploys to Docker, Kubernetes or BentoCloud
- **−** Every catalog model requires a GPU; no CPU-only entries
- **−** Custom model repositories must be public
- **−** Catalog tops out around Llama 3.3 and Qwen2.5; last commit 2026-05-29
- **−** Adding models means building BentoML Bentos

<sub>GPU required · Models: Llama 3.1/3.2/3.3/4, Qwen2.5, Qwen2.5-Coder, QwQ, Mistral, Mistral Large, Pixtral, Phi-4, Gemma 2/3, Jamba 1.5, DeepSeek R1 · port 3000 · [Repo](https://github.com/bentoml/OpenLLM)</sub>

### [Triton Inference Server](https://github.com/triton-inference-server/server) <sub>★ 11.1k · BSD-3-Clause · Oct 2026</sub>

**NVIDIA inference server for TensorRT, PyTorch, ONNX and more over HTTP/gRPC.**

Triton serves TensorRT, PyTorch, ONNX, OpenVINO, Python and RAPIDS FIL models over HTTP/REST and gRPC (KServe v2), with concurrent execution, dynamic and sequence batching, ensembles and Business Logic Scripting. NVIDIA ships it as NGC containers (2.73.0 / 26.09) for NVIDIA GPUs, x86 and ARM CPUs, Jetson and AWS Inferentia, with C and Java in-process APIs and a metrics endpoint.

- **+** Serves TensorRT, PyTorch, ONNX, OpenVINO, Python and FIL models together
- **+** Dynamic and sequence batching, ensembles and BLS pipelines
- **+** HTTP/REST and gRPC (KServe v2) plus C and Java in-process APIs
- **+** Metrics for GPU utilization, throughput and latency
- **−** No OpenAI-compatible endpoint in the README; clients speak KServe v2
- **−** Model repository and per-model config files are hand-written
- **−** Containers track NVIDIA's monthly NGC release cycle
- **−** Not every backend is supported on every platform

<sub>GPU optional · Models: TensorRT, PyTorch, ONNX, OpenVINO, Python, RAPIDS FIL backends · [Repo](https://github.com/triton-inference-server/server) · [Site](https://developer.nvidia.com/nvidia-triton-inference-server)</sub>

### [Xinference](https://github.com/xorbitsai/inference) <sub>★ 9.6k · Apache-2.0 · Oct 2026</sub>

**Serves LLM, embedding, speech and image models behind one OpenAI-style API.**

Xinference serves LLM, embedding, rerank, speech, image and multimodal models behind one OpenAI-compatible API, RPC, CLI and web UI, via pip or the xprobe/xinference image on port 9997. It runs vLLM, its own Xllamacpp llama.cpp binding and other engines across GPUs and CPUs, and scales to multi-node clusters with a Helm chart. Version 3.0 brought breaking changes.

- **+** One API for LLM, embedding, rerank, speech, image and multimodal models
- **+** Auto-batching of concurrent requests; Xllamacpp adds continuous batching to llama.cpp
- **+** Multi-node distributed inference with a Helm chart for Kubernetes
- **+** Built-in model catalog with frequent additions (OCR, TTS, image editing)
- **−** Docker image targets NVIDIA GPUs; CPU and Metal need a pip install
- **−** 3.0.0 release carries breaking changes and migration notes
- **−** Commercial Enterprise edition exists alongside the community edition
- **−** README gives no RAM or VRAM guidance

<sub>GPU optional · Models: built-in catalog of LLM, embedding, rerank, speech, image and video models, custom models, engines: vLLM, Xllamacpp (llama.cpp), transformers, TensorRT · port 9997 · [Repo](https://github.com/xorbitsai/inference) · [Docs](https://inference.readthedocs.io/) · [Site](https://xinference.co)</sub>

### [LMDeploy](https://github.com/InternLM/lmdeploy) <sub>★ 8.1k · Apache-2.0 · Sep 2026</sub>

**LLM and VLM serving toolkit with the TurboMind and PyTorch engines.**

LMDeploy compresses and serves LLMs and VLMs with two engines: TurboMind (CUDA, persistent batching, blocked KV cache, AWQ W4A16, MXFP4) and a pure-Python PyTorch engine that also runs on Huawei Ascend. pip install lmdeploy adds an API server plus a proxy for multi-model, multi-machine serving. Models span Llama, Qwen3, DeepSeek-V3/V4, GLM-5, InternVL and Qwen3-VL.

- **+** TurboMind engine with persistent batching, blocked KV cache and 4-bit AWQ inference
- **+** Online INT8/INT4 KV cache quantization and prefix caching usable together
- **+** Wide VLM list: InternVL 1 to 3.5, Qwen2/2.5/3-VL, LLaVA, Gemma3, Llama4
- **+** PyTorch engine supports Huawei Ascend NPUs with graph mode
- **−** The two engines support different model sets and dtypes; check the matrix
- **−** Prebuilt wheels target CUDA 12.8; other CUDA versions need source builds
- **−** No port, VRAM or web UI details in the README
- **−** Community channels are WeChat-centric alongside Discord

<sub>GPU required · Models: Llama 1-4, Qwen1.5-3.5, InternLM2/3, DeepSeek V2-V4, GLM-4/5, Mixtral, Gemma, Phi-3/4, gpt-oss, VLMs: InternVL, Qwen-VL, LLaVA, DeepSeek-VL, CogVLM, MiniCPM-V, Molmo, Gemma3, Llama4 · [Repo](https://github.com/InternLM/lmdeploy) · [Docs](https://lmdeploy.readthedocs.io/en/latest/)</sub>

### [mistral.rs](https://github.com/EricLBuehler/mistral.rs) <sub>★ 7.7k · MIT · Oct 2026</sub>

**Rust inference server with OpenAI and Anthropic APIs and agent tools.**

mistral.rs is a Rust engine whose single binary runs and serves Hugging Face, GGUF and UQFF models (text, vision, video, audio, speech, image generation; 45+ architectures) with auto-detected architecture and chat template. The serve command exposes OpenAI /v1 and Anthropic Messages endpoints, a web UI at /ui and Prometheus metrics on port 1234, with paged attention, ISQ, LoRA and a built-in agent loop.

- **+** One binary for chat, server, benchmarks and web UI; prebuilt for Metal, CUDA, CPU
- **+** In-situ quantization of any Hugging Face model plus GGUF 2-8 bit, GPTQ, AWQ, FP8
- **+** Server-side agent loop with Python, shell, web search, skills and MCP client
- **+** mistralrs tune recommends quantization and device mapping for your hardware
- **−** BF16 prefill trails vLLM by 5-10x on the 26B MoE in its own benchmarks
- **−** Install script is curl piped to sh, falling back to a source build
- **−** cuTile acceleration needs NVIDIA's separately installed tileiras tool
- **−** Not affiliated with Mistral AI despite the name

<sub>GPU optional · Docker · Models: Hugging Face safetensors, GGUF, UQFF, Qwen3, Gemma 4, Muse Glimmer, DiffusionGemma and 45+ architectures · port 1234 · [Repo](https://github.com/EricLBuehler/mistral.rs) · [Docs](https://docs.mistralrs.dev/)</sub>

### [llama-swap](https://github.com/mostlygeek/llama-swap) <sub>★ 5.9k · MIT · Oct 2026</sub>

**Go proxy that hot-swaps local model servers per request.**

llama-swap is one Go binary that proxies OpenAI and Anthropic API calls to local servers (llama-server, vLLM, stable-diffusion.cpp, whisper.cpp) and starts, stops or swaps the right one per model ID from a YAML file. It adds a web UI, log streaming, Prometheus metrics, API keys, TTL unload and a matrix DSL for concurrent models. Unified Docker images bundle the servers for CUDA and Vulkan.

- **+** One binary, one YAML file, zero dependencies
- **+** Hot-swaps any OpenAI or Anthropic-compatible upstream per model ID, with ttl unload
- **+** Unified images bundle llama-server, stable-diffusion.cpp, whisper.cpp, audio.cpp
- **+** Web UI with playground, token metrics, request inspection and live logs
- **−** Basic mode runs one model at a time; concurrency needs the matrix DSL
- **−** Python servers like vLLM or tabbyAPI should run in containers for clean SIGTERM
- **−** nginx needs proxy_buffering off or SSE streaming breaks
- **−** Container listen address must stay 0.0.0.0 when publishing ports

<sub>GPU optional · Needs an upstream inference server (llama-server, vLLM, etc.) · Models: any model served by the configured upstream (GGUF via llama-server, etc.) · port 8080 · [Repo](https://github.com/mostlygeek/llama-swap)</sub>

### [Lemonade](https://github.com/lemonade-sdk/lemonade) <sub>★ 5.8k · Apache-2.0 · Oct 2026</sub>

**Local AI server that targets GPUs and AMD NPUs with OpenAI-style APIs.**

Lemonade is a local AI server with OpenAI, Anthropic and Ollama-compatible APIs on port 13305 that runs GGUF, FLM and ONNX models, Whisper transcription, Kokoro speech and Stable Diffusion images. It picks the backend for the hardware: llama.cpp on CPU, CUDA, Vulkan, ROCm or Metal, plus AMD XDNA2 NPU paths for Ryzen AI. Packages exist for Windows, macOS, Debian, Fedora, Ubuntu, Arch, Snap and Docker.

- **+** NPU backends for AMD XDNA2 (Ryzen AI) alongside CUDA, ROCm, Vulkan, Metal
- **+** Chat, speech-to-text, text-to-speech, image and audio generation in one server
- **+** Native packages: msi, pkg, deb, rpm, Arch, Snap, PPA, Docker
- **+** Model aliases enable active-standby failover between models
- **−** Many engines (vllm, ds4, openmoss, trellis) are marked experimental
- **−** NPU support covers AMD XDNA2 only
- **−** macOS gets Metal only; several backends are Windows or Linux only
- **−** Cloud offload to OpenAI-compatible providers is experimental

<sub>GPU optional · Docker · Models: GGUF, FLM and ONNX LLMs (e.g. Gemma 4, Qwen3), Whisper, Kokoro, SDXL-Turbo · port 13305 · [Repo](https://github.com/lemonade-sdk/lemonade)</sub>

### [GPUStack](https://github.com/gpustack/gpustack) <sub>★ 5.8k · Apache-2.0 · Oct 2026</sub>

**GPU cluster manager that deploys models on vLLM, SGLang and TensorRT-LLM.**

GPUStack is a GPU cluster manager that deploys models across on-prem, Kubernetes and cloud workers, configuring vLLM, SGLang, TensorRT-LLM or custom engines behind OpenAI-compatible APIs with auth, API keys and token metering. The server is one Docker container on port 80 and can run CPU-only; Linux workers join with a privileged Docker command. It supports NVIDIA, AMD, Ascend and six Chinese accelerator families.

- **+** Multi-cluster: on-prem, Kubernetes and cloud GPUs under one server
- **+** Auto-selects and tunes vLLM, SGLang or TensorRT-LLM per model
- **+** Built-in auth, API keys, token metering, Grafana and Prometheus dashboards
- **+** SSH-accessible GPU instances on demand for fine-tuning
- **−** Workers are Linux-only; macOS cannot be a worker, Windows needs WSL2
- **−** Worker container runs privileged with the Docker socket mounted
- **−** Cluster topology view is in the paid GPUStack Enterprise
- **−** Quick start assumes an NVIDIA GPU; other vendors need extra steps

<sub>GPU required · Models: catalog models (e.g. Qwen3.5-0.8B) via vLLM, SGLang, TensorRT-LLM, LLM, voice, image and video models · port 80 · [Repo](https://github.com/gpustack/gpustack) · [Docs](https://docs.gpustack.ai)</sub>

### [Text Embeddings Inference](https://github.com/huggingface/text-embeddings-inference) <sub>★ 5.1k · Apache-2.0 · Oct 2026</sub>

**Rust server for embedding, reranker and classification models.**

TEI is a Rust server from Hugging Face for embedding, reranker and sequence-classification models (BERT, XLM-RoBERTa, Nomic, Jina, GTE, Qwen3, ModernBERT, Gemma3) with token-based dynamic batching and Flash Attention. The router listens on port 3000 with /embed and OpenAI-compatible routes, gRPC, OpenTelemetry tracing and Prometheus metrics. Images cover CPU x86/arm64 and NVIDIA Turing through Blackwell.

- **+** Token-based dynamic batching with Flash Attention, Candle and cuBLASLt
- **+** Small images and fast boot; no graph compilation step
- **+** Rerankers and classifiers served alongside embeddings
- **+** OpenTelemetry tracing, Prometheus metrics, API key auth, gRPC
- **−** No Volta support; Turing image is experimental with Flash Attention off
- **−** GPU images need drivers compatible with CUDA 12.2 or higher
- **−** Only CamemBERT and XLM-RoBERTa for sequence classification
- **−** 7B embedders such as Qwen3-Embedding-8B are flagged very expensive

<sub>GPU optional · Docker · Models: Qwen3-Embedding, gte-Qwen2, multilingual-e5, embeddinggemma, arctic-embed, nomic-embed, ModernBERT, jina-embeddings-v2, bge-reranker, gte rerankers · port 3000 · [Repo](https://github.com/huggingface/text-embeddings-inference) · [Docs](https://huggingface.github.io/text-embeddings-inference)</sub>

### [TabbyAPI](https://github.com/theroyallab/tabbyAPI) <sub>★ 1.5k · AGPL-3.0 · Oct 2026</sub>

**OpenAI-compatible API server for ExLlamaV3 models.**

TabbyAPI is a FastAPI server exposing an OpenAI-compatible API for the ExLlamaV3 backend, serving EXL3 and FP16/BF16 models with continuous batching via paged attention on NVIDIA Ampere or newer, speculative decoding, constrained output and tool calling. A CUDA Docker image runs on port 5000 and needs --shm-size=8g. The maintainers call it a hobby project not meant for production.

- **+** Official API server for ExLlamaV3 with EXL3 quantized models
- **+** Continuous batching with paged attention; speculative decoding via draft models
- **+** JSON schema, regex and EBNF constrained output plus OpenAI-style tool calling
- **+** Optional embeddings stack in the latest-extras image
- **−** Marked hobby project, rolling release, not for production servers
- **−** NVIDIA only; batching needs Ampere or newer; Docker needs --shm-size=8g
- **−** EXL3 and FP16/BF16 only; no GGUF
- **−** AGPL-3.0 license

<sub>GPU required · Models: EXL3 (recommended), FP16/BF16 Hugging Face models · port 5000 · [Repo](https://github.com/theroyallab/tabbyAPI) · [Docs](https://theroyallab.github.io/tabbyAPI)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Gateways

LLM gateways and proxies for routing, caching, rate limits and cost control across providers. <sub>13 projects, by stars.</sub>

<details><summary>How to choose</summary>

- List the providers you call today; check the gateway's native support rather than generic passthrough.
- Key management, per-team budgets and audit logs separate gateways from simple proxies.
- Check latency overhead and whether streaming is passed through unchanged.

</details>

### [OmniRoute](https://github.com/diegosouzapw/OmniRoute) <sub>★ 74.1k · MIT · Oct 2026</sub>

**Free-tier-aware AI gateway routing coding agents across 350+ providers.**

OmniRoute is a Node.js gateway (npm, Docker or Electron app) exposing one OpenAI, Claude, Gemini and Responses-compatible endpoint on port 20128 in front of 350+ providers, 150+ with free tiers, with automatic fallback and 19 routing strategies. It targets coding agents such as Claude Code, Codex, Cursor and Cline, adds RTK and Caveman prompt compression and tracks free-tier quotas on a dashboard.

- **+** Zero-config start: a keyless provider answers model auto right after install
- **+** OpenAI, Claude, Gemini and Responses API compatibility at one /v1 endpoint
- **+** Prompt compression (RTK plus Caveman) claims 15 to 95 percent token savings
- **+** Dashboard tracks free-tier quota use per provider pool
- **−** Provider counts in the README disagree (357 vs 364) and change every two weeks
- **−** Free-token headline depends on third-party tiers; 13 providers flagged as terms risk
- **−** README is mostly marketing graphics; architecture lives in docs
- **−** Compression and routing claims are self-reported

<sub>no GPU · Docker + Compose · Models: 350+ providers incl. free tiers (OpenCode Free, Groq, Mistral) via OpenAI, Claude and Gemini-style APIs · port 20128 · [Repo](https://github.com/diegosouzapw/OmniRoute) · [Site](https://omniroute.online)</sub>

### [LiteLLM](https://github.com/BerriAI/litellm) <sub>★ 60.3k · NOASSERTION · Oct 2026</sub>

**Proxy and SDK that calls 100+ LLM providers in OpenAI format.**

LiteLLM is a Python AI gateway that calls 100+ providers (OpenAI, Anthropic, Gemini, Bedrock, Azure and more) in OpenAI format, as a library or as a proxy server on port 4000. The proxy adds virtual keys, spend tracking, guardrails, load balancing and an admin dashboard, plus an MCP gateway and A2A agent routing. Endpoints cover chat, responses, embeddings, images, audio, rerank and Anthropic messages.

- **+** 100+ providers behind /chat/completions, /responses, /embeddings, /rerank and /messages
- **+** Virtual keys, spend tracking, guardrails, load balancing and admin UI built in
- **+** MCP gateway and A2A agent routing through the same proxy
- **+** Same code usable as a Python SDK without the proxy
- **−** Custom license (NOASSERTION); enterprise features sit behind a paid tier
- **−** 8 ms P95 latency figure is self-benchmarked at 1k RPS
- **−** Endpoint coverage is uneven across the 100+ providers
- **−** MCP OAuth may need pre-registered client credentials; dynamic registration can 401

<sub>no GPU · Docker + Compose · Models: OpenAI, Anthropic, Gemini, Vertex AI, Bedrock, Azure, Cohere, Groq, Mistral, DeepSeek, Hugging Face, Ollama, vLLM and 100+ more · port 4000 · [Repo](https://github.com/BerriAI/litellm) · [Docs](https://docs.litellm.ai/docs/simple_proxy) · [Site](https://www.litellm.ai/ai-gateway)</sub>

### [Portkey Gateway](https://github.com/Portkey-AI/gateway) <sub>★ 13.1k · MIT · May 2026</sub>

**Node.js LLM gateway with fallbacks, load balancing and guardrails.**

Portkey Gateway is a Node.js proxy that routes requests to 250+ LLM providers through an OpenAI-style API on port 8787, runnable with npx, Docker or Cloudflare Workers. Config objects add retries, fallbacks, load balancing, conditional routing, timeouts and 40+ guardrails; a console at /public shows local logs. Semantic caching, prompt management and RBAC are hosted or enterprise features.

- **+** Runs with npx in Node.js; 122 KB footprint, sub-millisecond overhead claimed
- **+** Fallbacks, retries, load balancing, conditional routing and timeouts via config
- **+** 40+ built-in guardrails plus bring-your-own
- **+** Works with OpenAI, LangChain, LlamaIndex, CrewAI and Autogen SDKs
- **−** Semantic caching, prompt management and provider optimization are hosted or enterprise only
- **−** Last commit 2026-05-25; Gateway 2.0 enterprise merge still pre-release
- **−** Docs links are portkey.wiki short links
- **−** RBAC, PII redaction and compliance features are enterprise

<sub>no GPU · Docker + Compose · Models: OpenAI, Azure OpenAI, Anthropic, Gemini, Cohere, Mistral, Together, Perplexity, Ollama, Bedrock, Groq and 45+ providers · port 8787 · [Repo](https://github.com/Portkey-AI/gateway)</sub>

### [Higress](https://github.com/higress-group/higress) <sub>★ 9.5k · Apache-2.0 · Oct 2026</sub>

**Envoy-based API gateway with LLM proxy plugins and MCP server hosting.**

Higress is a CNCF sandbox API gateway on Istio and Envoy, extended with Wasm plugins in Go, Rust or JS. Its AI plugins proxy mainstream LLM providers with token rate limiting, load balancing, caching and observability, and host remote MCP servers, including ones generated from OpenAPI specs. A Docker all-in-one image exposes the console on 8001 and the gateway on 8080/8443; Helm covers Kubernetes.

- **+** Envoy-based with millisecond config reloads and no connection drops
- **+** Hosts MCP servers with auth, rate limits and audit; OpenAPI-to-MCP converter
- **+** Token rate limiting, multi-model load balancing and caching for LLM routes
- **+** Also a Kubernetes ingress controller and Gateway API implementation
- **−** Images only on Alibaba Cloud registries; pulls can time out outside the mirrors
- **−** Istio and Envoy underneath; heavier than single-binary LLM proxies
- **−** AI features are Wasm plugins on a general API gateway
- **−** Docs split across higress.ai and higress.cn

<sub>no GPU · Models: mainstream LLM providers, domestic and international, via the ai-proxy plugin · port 8001 · [Repo](https://github.com/higress-group/higress) · [Demo](https://demo.higress.io/) · [Docs](https://higress.cn/en/docs/latest/overview/what-is-higress/) · [Site](https://higress.ai/en/)</sub>

### [CoAI](https://github.com/coaidev/coai) <sub>★ 9.3k · Apache-2.0 · Mar 2026</sub>

**Multi-user chat site plus OpenAI-compatible proxy with billing.**

CoAI pairs a multi-user chat frontend with an OpenAI-compatible API proxy and billing for operators of commercial AI sites. A Go backend on MySQL and Redis routes across channels with priority, weight, retries and model redirection for OpenAI, Anthropic, Gemini, Midjourney, Ollama and more; the React UI adds file parsing, SearXNG search and image generation. Docker Compose serves it on port 8000.

- **+** Chat UI and OpenAI-compatible proxy in one deployment
- **+** Channel priorities, weights, retries and model redirection for routing
- **+** Subscription and per-token billing with gift and redemption codes
- **+** Midjourney, DALL-E and Stable Diffusion image generation in chat
- **−** Default admin login root / chatnio123456 must be changed after deploy
- **−** RAG, TTS/STT, OAuth login and rate limiting are in the paid Pro version
- **−** Needs MySQL and Redis
- **−** Last commit 2026-03-12

<sub>no GPU · Docker + Compose · Needs MySQL, Redis, SearXNG (optional web search), CoAI blob-service (optional file parsing) · Models: OpenAI, Azure OpenAI, Anthropic, Gemini, Midjourney, SparkDesk, Zhipu, Qwen, Hunyuan, Baichuan, Moonshot, DeepSeek, Skylark, Groq, OpenRouter, 360, LocalAI, Ollama · port 8000 · [Repo](https://github.com/coaidev/coai) · [Docs](https://coai.dev/docs/deploy) · [Site](https://coai.dev)</sub>

### [Bifrost](https://github.com/maximhq/bifrost) <sub>★ 8.6k · Apache-2.0 · Oct 2026</sub>

**Go AI gateway with web UI, fallbacks, budgets and semantic caching.**

Bifrost is a Go AI gateway that fronts 23+ providers (OpenAI, Anthropic, Bedrock, Vertex and more) with one OpenAI-compatible API and drop-in paths for the OpenAI, Anthropic and GenAI SDKs. It starts with npx or Docker on port 8080 with a web UI, and adds fallbacks, load balancing, semantic caching, MCP tool access, virtual keys, budgets and Prometheus metrics. Clustering, guardrails and the MCP gateway are enterprise features.

- **+** Single Go binary via npx or Docker with zero-config web UI on 8080
- **+** Drop-in base URLs for OpenAI, Anthropic and Google GenAI SDKs
- **+** Virtual keys, team budgets, OIDC provisioning and Prometheus metrics
- **+** 11 microsecond added latency at 5k RPS in its own benchmark
- **−** Guardrails, clustering, adaptive load balancing and MCP gateway are enterprise-only
- **−** Benchmarks are self-reported on t3 instances
- **−** 23+ providers, fewer than LiteLLM or Portkey
- **−** Semantic caching needs a vector store backend

<sub>no GPU · Models: OpenAI, Anthropic, AWS Bedrock, Google Vertex, Azure, Cerebras, Cohere, Mistral, Ollama, Groq and more · port 8080 · [Repo](https://github.com/maximhq/bifrost) · [Docs](https://docs.getbifrost.ai)</sub>

### [Plano](https://github.com/katanemo/plano) <sub>★ 7.1k · Apache-2.0 · Oct 2026</sub>

**Envoy-based data plane that routes, traces and guards agent traffic.**

Plano is an Envoy-based proxy for agentic apps: a YAML file declares agents (HTTP servers with an OpenAI chat endpoint), model providers and listeners, and Plano routes each turn to the right agent with its 4B orchestrator model (hosted free or run locally). It also routes LLM calls by model name, alias or preference, captures OpenTelemetry traces with no instrumentation and applies guardrails via filter chains.

- **+** Declarative multi-agent orchestration; agents are plain OpenAI-compatible HTTP servers
- **+** Zero-code OpenTelemetry traces and agentic signals for every request
- **+** Filter chains add moderation, jailbreak checks and memory out of process
- **+** Model routing by name, alias or preference across providers
- **−** Agent routing depends on Plano's own orchestrator model; hosted by default
- **−** Install prerequisites live in external docs; README shows only YAML and curl
- **−** Envoy underneath; heavier than a single-binary proxy
- **−** No port or resource guidance beyond example listeners

<sub>no GPU · Docker · Needs Plano-Orchestrator routing model (hosted or local) · Models: OpenAI, Anthropic and other providers configured as model_providers · [Repo](https://github.com/katanemo/plano) · [Docs](https://docs.planoai.dev)</sub>

### [agentgateway](https://github.com/agentgateway/agentgateway) <sub>★ 5.2k · Apache-2.0 · Oct 2026</sub>

**One proxy for LLM, MCP and A2A traffic with auth and RBAC.**

Agentgateway is a Linux Foundation proxy for agent traffic: an LLM gateway (OpenAI-compatible API, budgets, failover), an MCP gateway federating tools over stdio, HTTP, SSE and Streamable HTTP, and an A2A gateway. It adds JWT, API key and OAuth auth, CEL RBAC, rate limits, guardrails and OpenTelemetry, and runs standalone from YAML or as a Kubernetes controller with Gateway API.

- **+** One proxy for LLM, MCP and A2A traffic with an OpenAI-compatible API
- **+** MCP federation over stdio, HTTP, SSE and Streamable HTTP plus OpenAPI tools
- **+** JWT, API key and OAuth auth with CEL-based RBAC and rate limits
- **+** Standalone YAML mode or Kubernetes controller with Gateway API
- **−** README has no install command, ports or resource needs; quickstart is external
- **−** Inference routing assumes Kubernetes Inference Gateway extensions
- **−** Marked in active development; roadmap is the issue tracker
- **−** Guardrail backends beyond regex are cloud services (OpenAI, Bedrock, Model Armor)

<sub>no GPU · Docker · Models: OpenAI, Anthropic, Gemini, Bedrock and other providers; self-hosted models via inference routing · [Repo](https://github.com/agentgateway/agentgateway) · [Docs](https://agentgateway.dev/docs/standalone/latest)</sub>

### [ContextForge MCP Gateway](https://github.com/IBM/mcp-context-forge) <sub>★ 4.6k · Apache-2.0 · Oct 2026</sub>

**Registry and proxy federating MCP, A2A, REST and gRPC behind one endpoint.**

ContextForge is IBM's Python registry and proxy that federates MCP servers, A2A agents and REST or gRPC APIs into one MCP-compliant endpoint with auth, rate limiting, retries, an Admin UI and OpenTelemetry tracing. It installs from PyPI (mcpgateway on port 4444), as a GHCR container, via Docker Compose with PostgreSQL, Redis and nginx, or with a Helm chart, and virtualizes legacy REST services as MCP tools.

- **+** Federates MCP, A2A, REST and gRPC (via reflection) behind one MCP endpoint
- **+** Transports: HTTP, JSON-RPC, WebSocket, SSE, Streamable HTTP, stdio
- **+** Admin UI with live log viewer; OpenTelemetry to Phoenix, Jaeger, Zipkin
- **+** Helm chart with HPA, Redis clustering and Grafana dashboards
- **−** arm64 containers unsupported in production; Apple Silicon needs Rosetta or PyPI
- **−** Local Docker builds fail without the CI-only wheel closure; pull the GHCR image
- **−** Will not start without generated JWT_SECRET_KEY and AUTH_ENCRYPTION_SECRET
- **−** Large surface: 55+ tables, 40+ plugins, nginx and pgAdmin in the Compose stack

<sub>no GPU · Compose · Needs PostgreSQL (production; SQLite for dev), Redis (caching and federation) · Models: A2A agents: OpenAI, Anthropic, custom · port 4444 · [Repo](https://github.com/IBM/mcp-context-forge) · [Docs](https://ibm.github.io/mcp-context-forge/)</sub>

### [mcpo](https://github.com/open-webui/mcpo) <sub>★ 4.4k · MIT · Feb 2026</sub>

**Exposes any MCP server as an OpenAPI HTTP endpoint.**

mcpo wraps an MCP server command, SSE or Streamable HTTP endpoint and exposes its tools as an OpenAPI REST server on port 8000 with generated docs, so HTTP clients such as Open WebUI can call MCP tools. A Claude Desktop-style config serves several servers under separate routes with hot reload; OAuth 2.1 dynamic client registration handles protected upstreams. Runs via uvx, pip or Docker.

- **+** One command turns any MCP server into an OpenAPI server with /docs
- **+** stdio, SSE and Streamable HTTP upstreams; OAuth 2.1 with dynamic registration
- **+** Config file in Claude Desktop format with hot reload
- **+** Docker image and --root-path for reverse proxies
- **−** Last commit 2026-02-27
- **−** Single shared API key; no users or RBAC
- **−** Converts to OpenAPI only; does not aggregate servers into one MCP endpoint
- **−** Python 3.8+ process per deployment; no clustering

<sub>no GPU · Docker · Needs MCP servers to proxy · port 8000 · [Repo](https://github.com/open-webui/mcpo) · [Docs](https://docs.openwebui.com/openapi-servers/open-webui/)</sub>

### [optillm](https://github.com/algorithmicsuperintelligence/optillm) <sub>★ 4.3k · Apache-2.0 · Sep 2026</sub>

**OpenAI-compatible proxy applying inference-time reasoning techniques.**

OptiLLM is an OpenAI-compatible proxy (pip or Docker, port 8000) that applies inference-time techniques such as mixture of agents, N-sample selection, self-consistency, MCTS, CePO and MARS to any upstream model, selected by a model-name prefix like moa-gpt-4o-mini. Plugins add an MCP client, memory, PII anonymization, code execution, JSON outputs and provider failover; upstreams are OpenAI, Cerebras, Azure or anything LiteLLM supports.

- **+** 20+ techniques selected by model-name prefix, e.g. moa-gpt-4o-mini
- **+** Per-technique benchmarks listed (MARS +30 points on AIME 2025 with Gemini 2.5 Flash Lite)
- **+** Plugins for MCP client, memory, PII anonymization, code execution, JSON output
- **+** Works with any OpenAI-compatible endpoint; LiteLLM covers other providers
- **−** Techniques multiply upstream calls (bon, MoA, MCTS), raising cost and latency
- **−** Runs on Flask's development server by default
- **−** Decoding techniques (cot_decoding, AutoThink) need the local inference path
- **−** Web search plugin drives Chrome through Selenium

<sub>GPU optional · Docker + Compose · Models: OpenAI, Cerebras, Azure OpenAI, any OpenAI-compatible endpoint, LiteLLM providers, local models via the built-in inference server · port 8000 · [Repo](https://github.com/algorithmicsuperintelligence/optillm) · [Demo](https://huggingface.co/spaces/codelion/optillm)</sub>

### [MetaMCP](https://github.com/metatool-ai/metamcp) <sub>★ 2.7k · MIT · Jun 2026</sub>

**Aggregates MCP servers into namespaced endpoints with auth and middleware.**

MetaMCP groups MCP servers into namespaces and publishes each as one MCP endpoint over SSE, Streamable HTTP or OpenAPI, with API-key or OAuth auth, per-tool toggles, name overrides and middleware. It runs with Docker Compose beside PostgreSQL on port 12008, adds OIDC SSO, multi-tenancy and rate limits, and includes an inspector with saved configs. The author reports maintenance delays.

- **+** Namespaces group servers, toggle tools and override names and annotations
- **+** Endpoints over SSE, Streamable HTTP and OpenAPI with API key or MCP OAuth
- **+** OIDC SSO, multi-tenancy and registration controls for organizations
- **+** Built-in inspector with saved server configs
- **−** Author notes maintenance delays; a community fork exists
- **−** Endpoints are remote-only; stdio clients like Claude Desktop need mcp-proxy
- **−** Rate-limit counters are in-memory per instance, not cluster-wide
- **−** MCP servers needing more than uvx or npx require a custom Dockerfile

<sub>no GPU · Docker + Compose · Needs PostgreSQL · port 12008 · [Repo](https://github.com/metatool-ai/metamcp) · [Docs](https://docs.metamcp.com)</sub>

### [GoModel](https://github.com/ENTERPILOT/GoModel) <sub>★ 1.2k · MIT · Oct 2026</sub>

**Go AI gateway with OpenAI and Anthropic APIs, caching and budgets.**

GoModel is a Go AI gateway (install script or container on port 8080) exposing OpenAI-compatible /v1 and Anthropic /v1/messages endpoints in front of OpenAI, Anthropic, Gemini, Bedrock, Azure, Ollama, vLLM, SGLang and more. It adds exact and semantic caching, cost tracking, budgets, rate limits, failover, an MCP gateway, guardrails and a dashboard with playground. Compose adds Redis, PostgreSQL, MongoDB and Prometheus.

- **+** Single Go binary or container; official OpenAI and Anthropic SDKs work unchanged
- **+** Budgets, rate limits, cost tracking and a usage API per user, team or key
- **+** Exact and semantic caching, failover with circuit breakers, provider key rotation
- **+** Dashboard with playground, live request stream, Prometheus and OpenTelemetry
- **−** Prompt compression, intelligent routing and OIDC SSO are in the paid Pro build
- **−** Pre-1.0; roadmap points to an upcoming 0.2.0 release
- **−** Full Compose stack pulls in Redis, PostgreSQL, MongoDB and Prometheus
- **−** Benchmarks against LiteLLM and Portkey are self-run

<sub>no GPU · Docker + Compose · Needs Redis, PostgreSQL, MongoDB (Compose infrastructure) · Models: OpenAI, Anthropic, xAI, Gemini, Vertex AI, Cohere, DeepSeek, Groq, Fireworks, OpenRouter, Azure OpenAI, Bedrock, Ollama, SGLang, vLLM, llm-d, ElevenLabs and any OpenAI-compatible provider · port 8080 · [Repo](https://github.com/ENTERPILOT/GoModel) · [Demo](https://demo.enterpilot.io/admin/dashboard) · [Docs](https://gomodel.enterpilot.io/docs)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Memory

Long-term memory engines that store and retrieve facts for agents across sessions. <sub>11 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Check what gets stored (raw messages, extracted facts, graphs) and how it is retrieved.
- Multi-tenant isolation matters if several users or agents share one store.
- Look at the backing store (Postgres, a vector DB, a graph DB) and whether you already run it.

</details>

### [Mem0](https://github.com/mem0ai/mem0) <sub>★ 66.8k · Apache-2.0 · Oct 2026</sub>

**Memory layer for agents with a self-hosted server, SDKs and CLI.**

Mem0 adds long-term memory to assistants and agents at user, session and agent level. It ships as a Python and npm library, a self-hosted server via docker compose (dashboard on port 3000, auth on by default) and a managed cloud. Memories are extracted by an LLM (gpt-5-mini by default) and retrieved with semantic, BM25 and entity matching; an optional NLP extra adds spaCy for hybrid search.

- **+** Library, self-hosted server with dashboard and API keys, or managed platform share one API
- **+** Multi-signal retrieval: semantic, BM25 keyword and entity matching with temporal reasoning
- **+** CLI and agent skills for Claude Code, Codex, Cursor and others
- **+** Apache-2.0; evaluation framework is open source
- **−** Requires an LLM for extraction; OpenAI gpt-5-mini and text-embedding-3-small are the defaults
- **−** Benchmark scores reflect the managed platform, not the open-source SDK
- **−** Self-hosted server exposes only teasers of advanced features; all included in cloud
- **−** Hybrid search recommends at least a 600M-parameter embedding model

<sub>no GPU · Models: OpenAI gpt-5-mini (default), OpenAI text-embedding-3-small (default), other providers per docs · port 3000 · [Repo](https://github.com/mem0ai/mem0) · [Demo](https://mem0.dev/demo) · [Docs](https://docs.mem0.ai) · [Site](https://mem0.ai)</sub>

### [MemPalace](https://github.com/MemPalace/mempalace) <sub>★ 59.5k · MIT · Oct 2026</sub>

**Local verbatim memory for coding agents on ChromaDB with 45 MCP tools.**

MemPalace stores conversation history verbatim, never summarised, and retrieves it by scoped semantic search over a palace of wings (people, projects), rooms (topics) and drawers. It runs locally with Python 3.9+ and ChromaDB by default, exposes 45 MCP tools plus a CLI, mines Claude Code, Codex and Cursor transcripts via hooks, and needs no API key: 96.6% R@5 on LongMemEval without an LLM.

- **+** Verbatim storage; nothing is summarised or paraphrased
- **+** 96.6% R@5 on LongMemEval with no LLM or API key; results reproducible from the repo
- **+** Pluggable backends: ChromaDB, sqlite, Rust-native, Milvus, Qdrant, pgvector
- **+** Multi-arch Docker image; auto-save hooks for Claude Code, Codex and Cursor
- **−** First run downloads an 80 to 300 MB embedding model; Docker needs network then
- **−** No native Android/Termux; GPU image is x86_64-only and unpublished
- **−** Docker image runs as uid 1000, so bind mounts must be readable by that uid
- **−** README warns about impostor domains distributing malware

<sub>no GPU · Docker + Compose · Models: local embeddings (MiniLM, EmbeddingGemma), OpenAI-compatible embedding endpoints, Ollama · [Repo](https://github.com/MemPalace/mempalace) · [Docs](https://mempalaceofficial.com/guide/getting-started.html) · [Site](https://mempalaceofficial.com)</sub>

### [OpenViking](https://github.com/volcengine/OpenViking) <sub>★ 39.4k · AGPL-3.0 · Oct 2026</sub>

**Context database exposing agent memory, knowledge and skills as a filesystem.**

OpenViking organises everything an agent knows as a viking:// virtual filesystem of resources, memories and skills, browsed with ls, tree, read and grep, with search scoped to a subtree. Each directory carries generated summaries so agents read full content only when needed. The server needs Python 3.10+ plus an embedding model and a VLM; plugins cover Claude Code, Codex, Cursor and OpenClaw.

- **+** Memory is inspectable and editable as Markdown files under viking:// URIs
- **+** LoCoMo accuracy 80 to 83% for OpenClaw, Hermes and Claude Code at far fewer tokens
- **+** Python, Go and TypeScript SDKs plus HTTP API; multi-tenant accounts and ACLs
- **+** Hosted Studio playground at openviking.ai/studio; Railway one-click deploy
- **−** AGPL-3.0 license
- **−** Needs both an embedding model and a vision-language model from a provider
- **−** Memory plugin installer is macOS/Linux only; Windows uses the beta desktop app
- **−** Benchmarks were run with Volcengine Doubao models

<sub>no GPU · Docker + Compose · Models: Volcengine, OpenAI, Codex OAuth, Kimi, GLM · [Repo](https://github.com/volcengine/OpenViking) · [Demo](https://openviking.ai/studio) · [Docs](https://docs.openviking.ai/) · [Site](https://www.openviking.ai)</sub>

### [Cognee](https://github.com/topoteretes/cognee) <sub>★ 31.6k · Apache-2.0 · Oct 2026</sub>

**Memory engine that turns documents and code into a knowledge graph.**

Cognee builds persistent agent memory by extracting entities, relationships and chunks from text, code and sessions into a graph and vector index with hybrid recall. Without an LLM key it uses local GLiNER extraction and embeddings; adding a key enables generated answers via OpenAI, Ollama or other providers. It runs as a library, CLI, REST API (port 8000), UI (3000) and MCP server (8001).

- **+** Keyless mode: local GLiNER extraction and embeddings, no cloud LLM required
- **+** Claude Code and Codex plugins, OpenClaw plugin, MCP server, Python, TypeScript and Rust SDKs
- **+** Imports memory from Mem0, Letta, Zep or Graphiti via the COGX format
- **+** Apache-2.0; research paper and BEAM evaluation published
- **−** Single-Postgres graph store is a demo; production version is a licensed product
- **−** API defaults to multi-tenant mode; local use needs ENABLE_BACKEND_ACCESS_CONTROL=false
- **−** Bundled GLiNER extractor is a demo; higher-accuracy version requires contacting the vendor
- **−** UI launcher needs Node.js/npm and Docker for its MCP service

<sub>no GPU · Docker + Compose · Models: local GLiNER + embeddings (keyless), OpenAI, Ollama, other providers per docs · port 8000 · [Repo](https://github.com/topoteretes/cognee) · [Docs](https://docs.cognee.ai/) · [Site](https://cognee.ai)</sub>

### [Graphiti](https://github.com/getzep/graphiti) <sub>★ 31.5k · Apache-2.0 · Oct 2026</sub>

**Temporal knowledge graph framework for agent memory with REST and MCP servers.**

Graphiti builds context graphs where every fact has a validity window and traces back to its source episode, ingesting text and JSON incrementally. Retrieval fuses embeddings, BM25 and graph traversal. It needs a graph database (Neo4j, FalkorDB or Neptune) and defaults to OpenAI, with Anthropic, Gemini, Groq and OpenAI-compatible servers supported; REST and MCP servers ship in the repo.

- **+** Bi-temporal facts: old facts are invalidated, not deleted, so history stays queryable
- **+** Hybrid retrieval combines embeddings, BM25 and graph traversal with sub-second latency claims
- **+** Custom entity and edge types via Pydantic models
- **+** Docker Compose profiles for Neo4j or FalkorDB; MCP and REST servers included
- **−** Requires Neo4j, FalkorDB or Amazon Neptune plus OpenSearch; Kuzu is deprecated
- **−** Defaults to OpenAI; needs structured-output models, smaller models may fail ingestion
- **−** Default SEMAPHORE_LIMIT of 10 keeps ingestion slow to avoid 429 errors
- **−** Users, threads and dashboards are left to the commercial Zep platform

<sub>no GPU · Docker + Compose · Needs Neo4j 5.26, FalkorDB 1.1.2 or Amazon Neptune · Models: OpenAI (default), Azure OpenAI, Anthropic, Google Gemini, Groq · [Repo](https://github.com/getzep/graphiti)</sub>

### [Supermemory](https://github.com/supermemoryai/supermemory) <sub>★ 31.2k · MIT · Oct 2026</sub>

**Memory and context API with user profiles, connectors and a local server.**

Supermemory extracts facts from conversations, maintains per-user profiles and answers hybrid queries that mix RAG over documents with personal memory, through one API with npm and pip SDKs. The self-hosted path is a single binary (port 6767) with an embedded graph engine and local bge-base embeddings, usable offline with Ollama; the hosted platform adds Drive, Gmail, Notion and GitHub connectors.

- **+** One binary, zero config; local Xenova/bge-base-en-v1.5 embeddings need no API key
- **+** Plugins for Claude Code, Cursor, Codex, OpenCode, OpenClaw and Hermes plus an MCP server
- **+** Framework wrappers for Vercel AI SDK, LangChain, LangGraph, OpenAI Agents SDK and Mastra
- **+** Open-source MemoryBench to compare memory providers
- **−** URL ingestion uses a hosted reader service even in local mode
- **−** Telemetry is on unless SUPERMEMORY_DISABLE_TELEMETRY=1 is set
- **−** Connectors (Drive, Gmail, Notion, GitHub) are described for the platform, not local
- **−** README leads with benchmark rankings; the MCP server URL points to the hosted service

<sub>no GPU · Models: OpenAI, Anthropic, Gemini, Groq, OpenAI-compatible endpoints · port 6767 · [Repo](https://github.com/supermemoryai/supermemory) · [Docs](https://supermemory.ai/docs)</sub>

### [agentmemory](https://github.com/rohitg00/agentmemory) <sub>★ 29.2k · Apache-2.0 · Oct 2026</sub>

**Persistent memory server for coding agents built on the iii engine.**

agentmemory captures agent activity via hooks, compresses it into searchable memory and injects context when the next session starts. One npx command (Node.js 20+) installs the server and pinned iii engine, wires Claude Code, Codex, Cursor and 17 other adapters, and serves REST and MCP on port 3111 with a viewer on 3113. Keyless mode uses BM25; a local MiniLM model or a provider adds semantic recall.

- **+** 20 agent adapters; Claude Code, Codex and Cursor get native plugins with hooks
- **+** No external databases; state lives in a platform data directory
- **+** Keyless by default; EMBEDDING_PROVIDER=local adds on-device semantic search
- **+** Real-time viewer on port 3113; 54 MCP tools and 17 skills
- **−** Pins iii-engine v0.22.1 and refuses to attach to any other engine version
- **−** Native Windows needs iii.exe installed by hand; WSL2 or Docker recommended
- **−** Uses four ports (3111, 3112, 3113, 49134)
- **−** LLM observation compression is off until AGENTMEMORY_AUTO_COMPRESS=true

<sub>no GPU · Compose · Needs iii-engine v0.22.1 (bundled) · Models: keyless BM25, local Xenova/all-MiniLM-L6-v2, LLM provider (optional) · port 3111 · [Repo](https://github.com/rohitg00/agentmemory)</sub>

### [MemOS](https://github.com/MemTensor/MemOS) <sub>★ 11.8k · Apache-2.0 · Sep 2026</sub>

**Memory operating system for agents with cubes, scheduler and hybrid retrieval.**

MemOS gives LLM apps and agents long-term memory via one API over graph-structured memories, grouped into memory cubes per user, project or agent. Self-hosting runs docker compose for the REST API on port 8000 with Neo4j and Qdrant; a local plugin for OpenClaw, Hermes and DeepSeek Harness instead keeps everything in SQLite with FTS5 and vector search.

- **+** Memory cubes isolate or share knowledge across users, projects and agents
- **+** MemScheduler ingests asynchronously for high-concurrency workloads
- **+** Local plugin for OpenClaw, Hermes and DeepSeek Harness is 100% on-device SQLite
- **+** Apache-2.0; two arXiv papers and OmniMemEval benchmark published
- **−** Self-hosted service requires Neo4j and Qdrant
- **−** Local plugin docs are partly in Chinese; cloud dashboard links go to a cn locale
- **−** LLM, embedder and vector DB keys must be filled in .env before start
- **−** Benchmark table lists scores without comparison baselines in the README

<sub>no GPU · Docker · Needs Neo4j, Qdrant · port 8000 · [Repo](https://github.com/MemTensor/MemOS) · [Docs](https://memos-docs.openmem.net/home/overview/) · [Site](https://memos.openmem.net/)</sub>

### [Honcho](https://github.com/plastic-labs/honcho) <sub>★ 7.5k · AGPL-3.0 · Oct 2026</sub>

**Memory service modelling users, agents and groups as evolving peers.**

Honcho is a FastAPI memory server where humans and agents are peers that exchange messages in sessions; a background deriver reasons over them and maintains per-peer representations and summaries you query via peer.chat, hybrid search or prompt-ready context. Run it managed at api.honcho.dev, locally with honcho start (API, deriver, Postgres and Redis in Docker) or from source with Docker Compose on port 8000.

- **+** First-party plugins for Claude Code, Codex, Cursor, DeepSeek Harness, OpenCode, OpenClaw and Hermes
- **+** Peer model handles multi-participant sessions and what one peer knows about another
- **+** Python and TypeScript SDKs with .to_openai and .to_anthropic context helpers
- **+** honcho start --setup brings up the whole local stack with one command
- **−** AGPL-3.0 license
- **−** Needs Postgres with pgvector and Redis plus an LLM key for the deriver
- **−** Background reasoning is asynchronous; new messages are not reflected immediately
- **−** README mixes marketing claims (Pareto frontier, data moats) with the technical content

<sub>no GPU · Docker · Needs PostgreSQL with pgvector, Redis · Models: Gemini, Anthropic, OpenAI · port 8000 · [Repo](https://github.com/plastic-labs/honcho) · [Demo](https://app.honcho.dev) · [Docs](https://honcho.dev/docs/v3/documentation/reference/sdk)</sub>

### [Engram](https://github.com/Gentleman-Programming/engram) <sub>★ 7.1k · MIT · Oct 2026</sub>

**Single Go binary memory for coding agents on SQLite FTS5 with MCP.**

Engram is one Go binary that stores agent memory in a local SQLite database with FTS5 full-text search and exposes it over MCP stdio, a CLI, a local HTTP API and an interactive TUI. The engram setup command configures 14 agents including Claude Code, OpenCode, Gemini CLI, Codex, Cursor and Windsurf; memory is project-aware, can sync through Git as compressed chunks, and optionally replicates to Engram Cloud.

- **+** No Node.js, Python or Docker; one binary and one SQLite file
- **+** engram setup targets 14 agents plus any MCP-compatible client
- **+** Git Sync shares memory across machines without a server
- **+** engram doctor and binary self-tests for diagnostics; MIT license
- **−** Full-text search only; no vector or semantic retrieval mentioned
- **−** Engram Cloud replication is optional and separate from the local store
- **−** Project detection can halt with project_transition_conflict after git init
- **−** Install docs for Windows and Linux live in docs/, not the README

<sub>no GPU · [Repo](https://github.com/Gentleman-Programming/engram) · [Site](https://engram.gentlemanprogramming.com/)</sub>

### [Letta](https://github.com/letta-ai/letta-code) <sub>★ 3.5k · Apache-2.0 · Oct 2026</sub>

**Stateful agent harness with git-tracked memory, channels and remote computers.**

Letta Code is an npm-installed agent harness whose agents keep memory blocks, skills and prompts in a git-tracked MemFS and rewrite them over time. Agents run from a CLI, desktop app, browser (chat.letta.com) or Telegram, Slack and Discord channels, use subagents, hooks and cron schedules, and can run on remote machines via letta server. Letta Cloud is the default backend; local is available.

- **+** All agent context including memory blocks is versioned in git (MemFS)
- **+** Same agent reachable from CLI, desktop, browser, Telegram, Slack and Discord
- **+** Skills installable from GitHub, ClawHub or the Hermes Skills Hub
- **+** Apache-2.0; Nix flake and AUR packages available
- **−** Letta Cloud is the default; remote computers and secrets require signing in
- **−** Self-hosted app server setup is not described in the README; local backend only mentioned
- **−** AgentFile export/import removed; agent registry imports no longer supported
- **−** Automatic dreaming is disabled on native Windows by default

<sub>no GPU · Models: OpenAI / ChatGPT, Anthropic, Z.ai coding plan · [Repo](https://github.com/letta-ai/letta-code) · [Demo](https://chat.letta.com) · [Docs](https://docs.letta.com/letta-code/cli)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Voice

Speech-to-text, text-to-speech, voice agents and meeting tools that run locally. <sub>11 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Latency decides usability for voice agents; check the end-to-end numbers the project publishes.
- Most quality models need a GPU; CPU-only setups are slower and limited to smaller models.
- Check language coverage and whether models are downloaded at build or at first run.

</details>

### [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS) <sub>★ 62.5k · MIT · Oct 2026</sub>

**Few-shot voice cloning and TTS with a training web UI.**

Clones a voice from a 5-second sample (zero-shot) or fine-tunes GPT and SoVITS models on about one minute of audio, then synthesizes speech in Chinese, English, Japanese, Korean and Cantonese. The Gradio web UI bundles dataset tools: UVR5 vocal separation, slicing, ASR and label proofreading. Aimed at hobbyists and studios building custom voices locally.

- **+** Zero-shot cloning from 5 s of audio; few-shot fine-tune from about 1 minute
- **+** Cross-lingual synthesis across zh, en, ja, ko and yue
- **+** Compose services for CUDA 12.6 and 12.8, plus Lite images without ASR and UVR5 models
- **+** Reported RTF 0.028 on an RTX 4060 Ti for v2 ProPlus
- **−** Pretrained weights are separate downloads from Hugging Face or ModelScope
- **−** Docker images lag the code; README says to pull latest source before using them
- **−** Training on Apple Silicon GPUs gives lower quality; macOS falls back to CPU
- **−** Five model generations (v1 to v5) with different tradeoffs to choose between

<sub>GPU optional · Docker + Compose · Needs ffmpeg · Models: GPT-SoVITS v1-v5 pretrained models, UVR5 vocal separation models, Faster Whisper large-v3 (ASR), FunASR Paraformer (Chinese ASR) · [Repo](https://github.com/RVC-Boss/GPT-SoVITS) · [Demo](https://lj1995-gpt-sovits-proplus.hf.space/) · [Docs](https://rentry.co/GPT-SoVITS-guide#/)</sub>

### [Voicebox](https://github.com/jamiepine/voicebox) <sub>★ 56.6k · MIT · Oct 2026</sub>

**Local voice studio for cloning, TTS, dictation and agent speech.**

Desktop app (Tauri) and Docker service that clones voices from a short sample and generates speech through eight TTS engines, including Qwen3-TTS, Chatterbox and Kokoro, in 23 languages. Adds Whisper dictation with a global hotkey, a REST API on port 17493 and an MCP server so coding agents can speak in a cloned voice. For individuals who want ElevenLabs-style voice I/O on their own machine.

- **+** Eight switchable TTS engines; Chatterbox Multilingual covers 23 languages
- **+** REST API plus HTTP and stdio MCP server for Claude Code, Cursor, Windsurf
- **+** Runs on MLX, CUDA, ROCm, DirectML, Intel Arc or CPU
- **+** Auto-chunking with crossfade handles scripts up to 50,000 characters
- **−** No prebuilt Linux binaries; build from source or use Docker
- **−** Only Chatterbox Turbo honors tags like [laugh]; other engines read them aloud
- **−** Dictation auto-paste and the permission flow are macOS-specific
- **−** Docker deployment gets one line in the README; details are in external docs

<sub>GPU optional · Docker + Compose · Models: Qwen3-TTS 0.6B/1.7B, Qwen CustomVoice, Qwen VoiceDesign, LuxTTS, Chatterbox Multilingual · port 17493 · [Repo](https://github.com/jamiepine/voicebox) · [Docs](https://docs.voicebox.sh) · [Site](https://voicebox.sh)</sub>

### [IndexTTS](https://github.com/index-tts/index-tts) <sub>★ 24.4k · NOASSERTION · Sep 2026</sub>

**Zero-shot TTS with emotion, speed and pronunciation control.**

Clones a voice from one reference clip and synthesizes speech in Chinese, English, Japanese, Spanish and Arabic (IndexTTS-2.5). Emotion comes from a second reference clip, an 8-value vector or the text itself; speed is set by duration_factor (0.5x to 2.0x) and pronunciation by inline Pinyin, CMU phonemes or Kana. Ships a Gradio web UI on port 7860 and a Python API; a vLLM recipe covers production serving.

- **+** Emotion control via reference audio, an 8-value vector or a text description
- **+** Inline pronunciation overrides: Pinyin, CMU phonemes and Japanese Kana
- **+** BF16 inference with optional DeepSpeed and compiled CUDA kernels
- **+** Published vLLM recipe for production deployment
- **−** No Dockerfile or compose file; install is uv plus CUDA Toolkit 12.8 or newer
- **−** Model weights (IndexTTS-2.5, IndexTTS-2) are separate multi-GB downloads
- **−** Five languages only; no streaming API is documented in the README
- **−** License is non-standard (GitHub reports NOASSERTION); check terms before commercial use

<sub>Needs uv · Models: IndexTTS-2.5, IndexTTS-2, IndexTTS-1.5 (legacy) · port 7860 · [Repo](https://github.com/index-tts/index-tts) · [Demo](https://huggingface.co/spaces/IndexTeam/IndexTTS-2.5-Demo)</sub>

### [F5-TTS](https://github.com/SWivid/F5-TTS) <sub>★ 15.4k · MIT · Sep 2026</sub>

**Flow-matching TTS and voice cloning with Gradio and CLI.**

Synthesizes speech from a reference clip and its transcript using the F5-TTS diffusion transformer (plus an E2 TTS reproduction). Runs as a pip package with a Gradio web app on port 7860, a CLI and a Docker image; a Triton and TensorRT-LLM runtime reaches RTF 0.039 on an L20 GPU. Suited to researchers and builders who want a trainable open TTS model.

- **+** pip install f5-tts; Gradio UI, CLI and a ghcr.io Docker image
- **+** Triton plus TensorRT-LLM runtime: 253 ms average latency at concurrency 2 on L20
- **+** Training and fine-tuning via Accelerate or a Gradio finetune app
- **+** PyTorch install documented for NVIDIA, AMD ROCm, Intel XPU and Apple Silicon
- **−** Pretrained weights are CC-BY-NC (Emilia data); code is MIT, models are non-commercial
- **−** Reference audio needs a transcript, or an ASR model runs and uses more GPU memory
- **−** No compose file in the repo; the README's compose example assumes an NVIDIA GPU
- **−** Base checkpoints cover Chinese and English; other languages need community models

<sub>Docker · Needs ffmpeg · Models: F5-TTS v1 Base, E2 TTS, Vocos and BigVGAN vocoders · port 7860 · [Repo](https://github.com/SWivid/F5-TTS) · [Demo](https://huggingface.co/spaces/mrfakename/E2-F5-TTS)</sub>

### [Speech-to-Speech](https://github.com/huggingface/speech-to-speech) <sub>★ 13.4k · Apache-2.0 · Oct 2026</sub>

**Modular voice-agent pipeline behind an OpenAI Realtime-compatible server.**

Runs a VAD, speech-to-text, LLM and text-to-speech cascade and exposes it through the OpenAI Realtime event set over WebSocket and WebRTC at ws://127.0.0.1:8765/v1/realtime. Defaults are Silero VAD, Parakeet TDT and Qwen3-TTS, with the LLM slot pointed at any OpenAI-compatible server, Transformers or mlx-lm. For teams building voice agents or devices that already speak the Realtime protocol.

- **+** Every stage is swappable: 12+ STT backends, 3 LLM backends, 7 TTS backends
- **+** OpenAI Agents SDK tested against both WebSocket and WebRTC transports
- **+** Fully local presets for Apple Silicon (MLX) and NVIDIA CUDA; no API key needed
- **+** pip install; one command runs the server and microphone client together
- **−** Fully local NVIDIA setup budgets 24 GB VRAM; Apple Silicon 16 GB unified memory
- **−** Default LLM is a hosted OpenAI model, so transcripts leave the machine unless changed
- **−** Linux Qwen3-TTS wheel targets CUDA 12.8 and glibc 2.39; older systems need manual wheels
- **−** DeepFilterNet audio enhancement conflicts with Pocket TTS (numpy<2 vs numpy>=2)

<sub>GPU optional · Docker + Compose · Needs libportaudio2, libsndfile1 · Models: Parakeet TDT, Whisper and Faster Whisper, Qwen3-ASR, Qwen3-TTS, Kokoro-82M · port 8765 · [Repo](https://github.com/huggingface/speech-to-speech)</sub>

### [Pocket TTS](https://github.com/kyutai-labs/pocket-tts) <sub>★ 9.8k · MIT · Oct 2026</sub>

**100M-parameter CPU text-to-speech with streaming and voice cloning.**

Generates speech on CPU with a 100M-parameter model: about 200 ms to the first audio chunk and roughly 6x real time on an M4 MacBook Air using two cores. Covers English, French, German, Portuguese, Italian, Spanish and Dutch, clones a voice from a WAV file, and runs as a CLI, a Python library or an HTTP server with a web UI on port 8000. For developers who want TTS without a GPU.

- **+** Runs on 2 CPU cores; no CUDA build of PyTorch needed
- **+** Streaming output with about 200 ms first-chunk latency
- **+** Voice cloning from any WAV; export voices to safetensors for fast loading
- **+** Training code released; community models load via --config
- **−** Seven European languages; others depend on community-trained models
- **−** No pause or silence markup in text input
- **−** serve command and Docker image are CPU-only; GPU use is unsupported and manual
- **−** Linux pip pulls CUDA PyTorch (about 3 GB) unless the CPU index is set

<sub>no GPU · Docker + Compose · Models: Pocket TTS 100M, 24-layer language variants, community checkpoints via --config · port 8000 · [Repo](https://github.com/kyutai-labs/pocket-tts) · [Demo](https://kyutai.org/pocket-tts) · [Docs](https://kyutai-labs.github.io/pocket-tts/)</sub>

### [Kokoro-FastAPI](https://github.com/remsky/Kokoro-FastAPI) <sub>★ 5.5k · Apache-2.0 · Oct 2026</sub>

**OpenAI-compatible Kokoro-82M speech API in CPU and GPU images.**

Serves the Kokoro-82M model behind an OpenAI-compatible /v1/audio/speech endpoint on port 8880, streaming mp3, wav, opus, flac, aac or pcm. Covers English (US/GB), Spanish, French, Hindi, Italian, Japanese, Brazilian Portuguese and Mandarin, with weighted voice mixing, inline [voice:] and [pause:] tags, word timestamps and phoneme endpoints. Prebuilt images exist for CPU, CUDA (amd64 and arm64) and experimental ROCm.

- **+** Drop-in for the OpenAI Python client; models baked into the images
- **+** Weighted voice mixing and inline speaker, pause, rate and IPA tags
- **+** Per-word timestamp captions and phoneme in/out endpoints
- **+** First-token latency about 300 ms on GPU
- **−** CPU first-token latency: 3.5 s on an older i7, under 1 s on M3 Pro
- **−** No true voice cloning; /dev/tune only nudges toward a reference clip
- **−** ROCm image is experimental and amd64 only
- **−** Apple Silicon GPU (MPS) only when run natively via uv, not in Docker

<sub>GPU optional · Needs espeak-ng (optional fallback) · Models: Kokoro-82M v1.0 · port 8880 · [Repo](https://github.com/remsky/Kokoro-FastAPI) · [Demo](https://huggingface.co/spaces/Remsky/FastKoko)</sub>

### [WhisperLive](https://github.com/collabora/WhisperLive) <sub>★ 4.3k · MIT · Oct 2026</sub>

**Near-real-time Whisper transcription server over WebSocket.**

Streams audio from a microphone, file, RTSP or HLS source to a server on port 9090 and returns partial and committed Whisper transcripts over WebSocket, with an optional OpenAI-compatible REST endpoint. Backends are faster-whisper (CPU, CUDA, ROCm), TensorRT-LLM and OpenVINO; extras include word timestamps, hotwords, pyannote diarization and translation. For teams embedding live captions or dictation.

- **+** Three inference backends: faster-whisper, TensorRT-LLM, OpenVINO (Intel iGPU/dGPU)
- **+** Prebuilt GPU, CPU and OpenVINO Docker images; ROCm Dockerfile
- **+** Word-level timestamps, hotword boosting and batched multi-client inference
- **+** Chrome, Firefox and iOS clients; Python streaming client for raw PCM
- **−** Defaults allow 4 clients and 600 s per connection; must be tuned for more
- **−** Without a fixed model, a new Whisper instance loads per client connection
- **−** TensorRT backend requires building engines and is recommended only via Docker
- **−** Diarization needs the optional pyannote.audio dependency

<sub>GPU optional · Needs PortAudio (client microphone input) · Models: Whisper via faster-whisper (CTranslate2), Whisper TensorRT-LLM engines, OpenVINO Whisper models · port 9090 · [Repo](https://github.com/collabora/WhisperLive)</sub>

### [Speakr](https://github.com/murtaza-nasir/speakr) <sub>★ 4.1k · AGPL-3.0 · Oct 2026</sub>

**Transcribe, summarize and search recordings with pluggable ASR and LLMs.**

Web app that records or ingests audio, transcribes it through a connector (self-hosted WhisperX, OpenAI, Mistral Voxtral, AssemblyAI, OpenASR, FunASR), then writes summaries, action items and per-recording chat with an OpenAI-compatible LLM, OpenRouter or Ollama. Adds diarization, voice profiles, OIDC SSO, groups, a Swagger REST API and signed webhooks. Flask app on port 8899 with SQLite or PostgreSQL.

- **+** Eight ASR connectors auto-detected from config; WhisperX enables voice profiles
- **+** Multi-user with OIDC SSO (Keycloak, Azure AD, Google, Auth0), groups and sharing
- **+** REST API v1 with Swagger UI, HMAC-signed webhooks, per-user token budgets
- **+** Lite image (about 725 MB) skips PyTorch; full image is about 4.4 GB
- **−** Still alpha (v0.10.13-alpha) with frequent feature churn between releases
- **−** No bundled ASR; needs an API key or a separate GPU WhisperX container
- **−** Dual-licensed: AGPLv3, or a paid commercial license for proprietary use
- **−** Lite image downgrades Inquire semantic search to basic text search

<sub>no GPU · Docker · Needs ASR service or API (WhisperX, OpenAI, Mistral, AssemblyAI, OpenASR, FunASR), LLM API (OpenAI-compatible, OpenRouter or Ollama), SQLite or PostgreSQL · Models: WhisperX, OpenAI gpt-4o-transcribe-diarize, Mistral Voxtral, AssemblyAI, VibeVoice via vLLM · port 8899 · [Repo](https://github.com/murtaza-nasir/speakr) · [Docs](https://murtaza-nasir.github.io/speakr)</sub>

### [Speaches](https://github.com/speaches-ai/speaches) <sub>★ 3.7k · MIT · Apr 2026</sub>

**OpenAI-compatible STT and TTS server with faster-whisper, Kokoro and Piper.**

Exposes OpenAI-style audio endpoints: streaming transcription and translation through faster-whisper, speech generation through Kokoro and Piper, plus a Realtime API and audio chat completions. Models load on first request and unload after inactivity, on CPU or GPU, via Docker Compose. For self-hosters who want one container that OpenAI SDKs can talk to for speech.

- **+** Works with any OpenAI SDK; transcription streams over SSE
- **+** Dynamic model loading and unloading after idle time
- **+** Supports the Realtime API and audio-in, audio-out chat completions
- **+** CPU and GPU Docker images with Compose files
- **−** Last commit April 2026; development has slowed
- **−** README is short; port, env vars and limits live only in the external docs
- **−** TTS limited to Kokoro and Piper models
- **−** Streaming transcription demo is marked TODO in the README

<sub>GPU optional · Docker + Compose · Models: faster-whisper (CTranslate2 Whisper), Kokoro, Piper · [Repo](https://github.com/speaches-ai/speaches) · [Docs](https://speaches.ai/) · [Site](https://speaches.ai/)</sub>

### [OpenReader](https://github.com/richardr1126/openreader) <sub>★ 537 · MIT · Oct 2026</sub>

**Reads EPUB, PDF and DOCX aloud with synced word highlighting.**

Next.js server that narrates EPUB, PDF, TXT, Markdown and DOCX files with synchronized read-along, generating audio ahead of playback through a self-hosted OpenAI-compatible TTS server (Kokoro-FastAPI, KittenTTS-FastAPI, Orpheus-FastAPI) or OpenAI, Replicate and DeepInfra. PDF layout is parsed with PP-DocLayoutV3 and words aligned with ONNX Whisper in a NATS JetStream worker. Exports M4B or MP3 audiobooks.

- **+** Layout-aware PDF parsing and word-by-word highlighting
- **+** Audio cache reused across seeks, reloads and audiobook export
- **+** Storage on embedded SeaweedFS or S3; SQLite or Postgres; built-in auth
- **+** amd64 and arm64 Docker images with automatic startup migrations
- **−** Needs a separate TTS server or cloud TTS API; nothing is bundled
- **−** Word alignment and DOCX conversion run in a NATS JetStream compute worker you deploy
- **−** Setup details (ports, env vars) are only in the external docs

<sub>no GPU · Docker · Needs OpenAI-compatible TTS server or cloud TTS API, NATS JetStream (compute worker), SQLite or PostgreSQL, SeaweedFS (embedded) or S3-compatible storage · Models: Kokoro-FastAPI, KittenTTS-FastAPI, Orpheus-FastAPI, OpenAI TTS, Replicate · [Repo](https://github.com/richardr1126/openreader) · [Docs](https://docs.openreader.richardr.dev/)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Image and video

Generation UIs and pipelines for images and video, usually around diffusion models. <sub>8 projects, by stars.</sub>

<details><summary>How to choose</summary>

- A GPU with enough VRAM is the hard requirement; check the minimum the project states.
- Node-based UIs are flexible but have a learning curve; form-based UIs are quicker to use.
- Check the model licensing separately from the app licensing.

</details>

### [ComfyUI](https://github.com/Comfy-Org/ComfyUI) <sub>★ 136.6k · GPL-3.0 · Oct 2026</sub>

**Node-graph engine for diffusion image, video, audio and 3D models.**

Builds generation pipelines as a visual node graph and runs them locally for image (SD 1.5, SDXL, SD3.5, Flux.1 and Flux.2, Qwen Image), video (Wan 2.x, LTX-Video, HunyuanVideo), audio (ACE-Step, Stable Audio) and 3D (Hunyuan3D) models, with a local API and an App Mode that exposes a workflow as a simple UI. Runs on NVIDIA, AMD, Intel, Apple Silicon and Ascend. For professionals who want control over every parameter.

- **+** Asynchronous weight streaming runs large models on 4 GB VRAM plus 8 GB RAM
- **+** Workflows saved as JSON and recoverable from generated media metadata
- **+** Runs fully offline; --offline disables the paid API nodes
- **+** Loads checkpoints, separate diffusion models, VAEs, text encoders, LoRAs, ControlNets
- **−** Commits outside stable tags can break many custom nodes; stable releases roughly biweekly
- **−** GPL-3.0 license constrains embedding in proprietary products
- **−** NVIDIA 20-series and newer require PyTorch built with CUDA 13.0 or above
- **−** Paid partner and API nodes stay on unless --offline or --disable-partner-nodes is set

<sub>RAM ≥ 8 GB · GPU optional · Models: Stable Diffusion 1.5, SDXL, SD3.5, Flux.1 and Flux.2, Qwen Image and Qwen Image Edit, Wan 2.1/2.2, LTX-Video 2 · [Repo](https://github.com/Comfy-Org/ComfyUI) · [Docs](https://docs.comfy.org/) · [Site](https://www.comfy.org/)</sub>

### [MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo) <sub>★ 129.3k · MIT · Oct 2026</sub>

**Generates short videos from a topic with script, footage, voice and subtitles.**

Takes a topic or keywords, writes a script with an LLM (OpenAI, Claude, Gemini, DeepSeek, Qwen, Ollama), pulls stock clips from Pexels, Pixabay or Coverr or generates them via video APIs, adds TTS narration (Edge TTS needs no key; Azure, ElevenLabs, Kokoro), subtitles and music, then renders 9:16, 16:9 or 1:1 videos. Usable through a WebUI, REST API, CLI or an agent skill. For creators automating short-form content.

- **+** Edge TTS works without any API key; many other TTS and LLM providers supported
- **+** Four entry points: WebUI, API, CLI and an agent skill; batch generation and task history
- **+** Runs on CPU; minimum spec is 4 cores and 4 GB RAM
- **+** One-click publishing to TikTok, Instagram and YouTube Shorts
- **−** README is Chinese first; the English version is a separate file
- **−** Default flow needs external LLM and stock-footage API keys
- **−** README carries heavy sponsor advertising and affiliate links
- **−** Local faster-whisper transcription and batch runs want a 4 GB+ VRAM GPU

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Needs LLM API (OpenAI-compatible) or Ollama, Stock footage API (Pexels, Pixabay, Coverr) or a video generation API · Models: OpenAI, Anthropic Claude, Google Gemini, DeepSeek, Qwen (DashScope) · [Repo](https://github.com/harry0703/MoneyPrinterTurbo)</sub>

### [Pixelle-Video](https://github.com/ATH-MaaS/Pixelle-Video) <sub>★ 28.7k · Apache-2.0 · Jun 2026</sub>

**Topic-to-short-video pipeline built on ComfyUI workflows and TTS.**

Turns a topic into a short video: an LLM (GPT, Qwen, DeepSeek, Ollama) writes the script, ComfyUI or RunningHub workflows or direct APIs (DashScope Wan, GPT Image, Seedream, Seedance, Kling) produce per-sentence images or clips, Edge-TTS or Index-TTS voices it, and HTML templates lay out each frame. Streamlit UI on port 8501, plus digital-human and image-to-video modules. For creators already running ComfyUI.

- **+** Zero-cost path: Ollama for the LLM plus a local ComfyUI instance
- **+** Image, video, TTS and VLM steps are swappable ComfyUI workflows or direct APIs
- **+** Custom HTML templates for static, image-backed and video-backed layouts
- **+** Windows one-click package bundles Python, uv and ffmpeg
- **−** README and docs are Chinese first; an English README exists separately
- **−** Local image or video generation needs a running ComfyUI server (default port 8188)
- **−** Last commit June 2026; update log stops at 2026-06-01
- **−** Heavy local footprint: ComfyUI plus diffusion and TTS models

<sub>Docker + Compose · Needs uv, ffmpeg, ComfyUI or RunningHub (workflow-based generation), LLM API or Ollama · Models: OpenAI GPT, Qwen (DashScope), DeepSeek, Ollama, Flux via ComfyUI (default image_flux.json) · port 8501 · [Repo](https://github.com/ATH-MaaS/Pixelle-Video) · [Docs](https://aidc-ai.github.io/Pixelle-Video/zh)</sub>

### [InvokeAI](https://github.com/invoke-ai/InvokeAI) <sub>★ 28.4k · Apache-2.0 · Oct 2026</sub>

**Canvas-first web UI for Stable Diffusion and Flux image generation.**

Local web server and React UI for image generation with a Unified Canvas (inpainting, outpainting, brushes), a node-based workflow editor and a boards gallery with per-image metadata. Loads SD 1.5 to SD 3.5, SDXL, Flux.1 and Flux.2 variants, Qwen Image, Z-Image, Krea 2 and CogView 4 in ckpt, diffusers and some GGUF formats; Nano Banana, GPT Image and Wan are API-only. For artists iterating on images.

- **+** Unified Canvas with in/outpainting, brush tools and SAM/SAM2 segmentation
- **+** Broad model list including Flux.2 Dev and Klein, SD 3.5 Large, Qwen Image Edit
- **+** Apache-2.0 license; serves as the base for commercial products
- **+** Dedicated launcher application handles install and updates
- **−** No Dockerfile or compose file at the repo root; install goes through the Launcher
- **−** README lists features only; ports, hardware needs and env vars are in external docs
- **−** Video generation (Wan) is API-only, not local
- **−** Nano Banana and GPT Image require third-party API access

<sub>Models: SD 1.5, SD 2.0, SDXL, SD 3.5 Medium/Large, CogView 4 · [Repo](https://github.com/invoke-ai/InvokeAI) · [Docs](https://invoke.ai/start-here/installation/) · [Site](https://invoke.ai)</sub>

### [Kohya's GUI](https://github.com/bmaltais/kohya_ss) <sub>★ 12.6k · Apache-2.0 · Jul 2026</sub>

**Gradio GUI and CLI for Kohya diffusion training scripts.**

Wraps kohya-ss/sd-scripts in a Gradio UI that builds the training command for LoRA, LoHa, LoKr, DreamBooth, full fine-tuning, Textual Inversion and LECO concept erasure. Base models include SD 1.5/2.x, SDXL, SD3, Flux.1, Lumina Image 2.0, Anima and HunyuanImage-2.1. Installs with uv or pip, runs headless over SSH on a port such as 7860, ships Docker, Runpod and Colab paths, and suits people training their own LoRAs.

- **+** Covers LoRA, LoHa, LoKr, DreamBooth, fine-tune, Textual Inversion and LECO
- **+** GUI shell runs offline after install; no CDN assets or analytics by default
- **+** config.toml presets default paths and Gradio allowed_paths
- **+** Sample image generation during training with per-prompt seed, size and CFG flags
- **−** Needs a GPU-equipped machine; README gives no VRAM figures per model
- **−** Without --headless, OS file dialogs on the server can block training over SSH
- **−** macOS support is community-maintained and may vary
- **−** Last commit July 2026; sd-scripts submodule pinned to v0.11.1

<sub>GPU required · Docker + Compose · Needs uv or pip, Python 3.10 with tkinter · Models: SD 1.5/2.x, SDXL, SD3, Flux.1, Lumina Image 2.0 · port 7860 · [Repo](https://github.com/bmaltais/kohya_ss)</sub>

### [AI Toolkit](https://github.com/ostris/ai-toolkit) <sub>★ 12.2k · MIT · Sep 2026</sub>

**Training suite and web UI for image, video and audio diffusion models.**

Trains LoRA, LoKr and full fine-tunes for FLUX.1 and FLUX.2, Chroma, Qwen-Image, HiDream, Z-Image, SDXL, SD 1.5, Wan 2.1 and 2.2, LTX-2 and ACE-Step from YAML configs, with a web UI on port 8675 to start, stop and monitor jobs. A manager script detects hardware, installs PyTorch, Node.js and FFmpeg inside the repo folder and keeps the install updated. For people fine-tuning current open models on NVIDIA GPUs.

- **+** Supports 30 image, 12 video and 3 audio models, including FLUX.2 and LTX-2.5
- **+** Experimental manager sets up PyTorch, Node.js and FFmpeg without system-wide installs
- **+** UI can be locked with AI_TOOLKIT_AUTH; jobs keep running without the UI
- **+** Layer targeting via only_if_contains and ignore_if_contains network kwargs
- **−** NVIDIA GPU required; the example FLUX LoRA configs assume 24 GB VRAM
- **−** No Dockerfile at the root; the manager install is marked experimental
- **−** Pressing Ctrl+C during a checkpoint save can corrupt it
- **−** Apple Silicon support is experimental; datasets limited to jpg, jpeg and png

<sub>GPU required · Compose · Needs Node.js 20+ (UI), FFmpeg, git · Models: FLUX.1-dev, FLUX.2-dev and klein 4B/9B, Flex.1 and Flex.2, Chroma, Lumina-Image-2.0 · port 8675 · [Repo](https://github.com/ostris/ai-toolkit)</sub>

### [FluxGym](https://github.com/cocktailpeanut/fluxgym) <sub>★ 3.3k · MIT · Jul 2026</sub>

**Web UI for training FLUX LoRAs on 12 to 20 GB GPUs.**

Gradio front end (forked from AI-Toolkit) over Kohya sd-scripts that trains FLUX.1-dev LoRAs with 12 GB, 16 GB or 20 GB VRAM presets. Upload images, caption them with a trigger word and press start; base models download automatically and an Advanced tab exposes every sd-scripts flag. Runs via Pinokio, a manual venv or docker compose on port 7860, for hobbyists training FLUX LoRAs on consumer GPUs.

- **+** VRAM presets for 12, 16 and 20 GB cards
- **+** Advanced tab is generated from sd-scripts flags, so every option is reachable
- **+** Sample images every N steps with fixed seeds to watch the LoRA evolve
- **+** Publish trained LoRAs to Hugging Face from the UI
- **−** FLUX.1 only (dev, dev2pro, schnell); schnell results are called not recommended
- **−** Manual install clones sd-scripts separately and uses PyTorch nightly builds
- **−** Docker image must be built locally; PUID and PGID must match your user
- **−** Last commit July 2026

<sub>GPU required · Docker + Compose · Needs kohya-ss/sd-scripts (sd3 branch) · Models: Flux1-dev, Flux1-dev2pro, Flux1-schnell, custom bases via models.yaml · port 7860 · [Repo](https://github.com/cocktailpeanut/fluxgym)</sub>

### [biniou](https://github.com/Woolverine94/biniou) <sub>★ 1.2k · GPL-3.0 · Oct 2026</sub>

**Chat, image, audio, video and 3D generation in one CPU-friendly web UI.**

Gradio web UI bundling 30+ modules: llama.cpp chat and LLaVA with GGUF models, Whisper, NLLB translation, Stable Diffusion 1.5 to 3.5, SDXL, Flux, PixArt, ControlNet, inpainting, MusicGen, Bark, AnimateDiff, Stable Video Diffusion and Shap-E. Runs on CPU from 8 GB RAM, with optional CUDA or experimental ROCm, and works offline once models are downloaded. For hobbyists wanting one install on modest hardware.

- **+** Runs on CPU-only machines from 8 GB RAM; GPU optional
- **+** One-click installers for Debian, RHEL, OpenSUSE, Arch, Windows; CPU and CUDA Docker images
- **+** Modules chain: send one module's output as another's input
- **+** Weekly updates adding GGUF chat models and LoRAs
- **−** Requires Python 3.10 or 3.11 exactly; AMD64 CPUs only
- **−** About 20 GB install without models, around 200 GB with all defaults
- **−** Many modules need 16 GB+ RAM (Kandinsky, AnimateDiff, SVD, outpaint)
- **−** GPL-3.0 license; macOS Intel support is experimental

<sub>RAM ≥ 8 GB · GPU optional · Docker · Needs ffmpeg, git, gcc, perl, openssl · Models: GGUF LLMs via llama.cpp, LLaVA GGUF, Whisper, NLLB-200, SD 1.5/2.1/Turbo · [Repo](https://github.com/Woolverine94/biniou) · [Docs](https://github.com/Woolverine94/biniou/wiki)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Coding

Self-hosted coding assistants and agents, from editor completion to autonomous task runners. <sub>9 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Separate editor completion (needs low latency, small models) from agents that run tasks (need strong models).
- Check sandboxing for agents that execute code or shell commands.
- Look at which editors and model backends are supported without a cloud account.

</details>

### [opencode](https://github.com/anomalyco/opencode) <sub>★ 212.3k · MIT · Oct 2026</sub>

**Terminal coding agent with build and plan modes.**

Runs an AI coding agent in the terminal with two built-in agents: build (full access) and plan (read-only, asks before running bash), plus a general subagent for multi-step searches. Installs via a curl script, npm, Homebrew, Scoop, Chocolatey, pacman, mise or Nix, and ships a beta desktop app for macOS, Windows and Linux. For developers who want an open, configurable coding agent.

- **+** MIT license; installable from npm, Homebrew, Scoop, Chocolatey, pacman, mise and Nix
- **+** Plan agent denies file edits and asks before bash, for safe codebase exploration
- **+** Desktop app (beta) for macOS, Windows and Linux alongside the terminal UI
- **−** README covers install only; providers, config and server mode are in external docs
- **−** No Dockerfile or compose file in the repo
- **−** Desktop app is still beta

<sub>no GPU · [Repo](https://github.com/anomalyco/opencode) · [Docs](https://opencode.ai/docs) · [Site](https://opencode.ai)</sub>

### [OpenHands](https://github.com/OpenHands/OpenHands) <sub>★ 90.3k · MIT · Oct 2026</sub>

**Self-hosted control center for coding agents and automations.**

Web UI and local stack on port 8000 that runs the OpenHands agent or any ACP-compatible agent (Claude Code, Codex, Gemini) on local, Docker, VM or cloud backends. Automations fire on schedules or webhooks and connect to Slack, GitHub and Linear. Installs via npm (Node 24+, uv) or a Docker image, optionally one container per conversation, for teams running coding agents as a shared service.

- **+** Agent-agnostic through ACP: OpenHands, Claude Code, Codex, Gemini
- **+** Per-conversation Docker sandboxes via OH_CONVERSATION_RUNTIME=docker
- **+** Binds to loopback by default; LAN exposure needs an explicit flag and API key
- **+** Scheduled and webhook-driven automations with Slack, GitHub and Linear
- **−** Project status is beta; the Docker quickstart pins image tag 1.25.0
- **−** Non-sandboxed install gives the agent full access to the host filesystem
- **−** No Dockerfile or compose file in the repo; the image is prebuilt on ghcr.io
- **−** Spread across four repos (Canvas, SDK, TypeScript client, automation)

<sub>no GPU · Needs Node.js 24+, uv, Docker (sandbox modes) · Models: any LLM via LLM profiles, OpenHands agent, Claude Code, Codex, Gemini · port 8000 · [Repo](https://github.com/OpenHands/OpenHands) · [Docs](https://docs.openhands.dev/openhands/usage/agent-canvas/backends)</sub>

### [screenshot-to-code](https://github.com/abi/screenshot-to-code) <sub>★ 80.1k · MIT · Jul 2026</sub>

**Turns screenshots and mockups into Tailwind, React or Vue code.**

Takes a screenshot, mockup, Figma export or screen recording and generates HTML with Tailwind or CSS, React, Vue, Bootstrap or Ionic code using Gemini 3, GPT-5.5 or Claude Opus models, with Replicate for image generation and background removal. Runs as a React/Vite frontend on port 5173 and a FastAPI backend on 7001, or via docker-compose. For developers prototyping UIs from designs.

- **+** Six output stacks including React, Vue, Bootstrap and Ionic with Tailwind
- **+** Video mode turns a screen recording into a working prototype (needs Gemini)
- **+** Optional headless Chromium lets the agent render and check its own output
- **+** docker-compose brings up frontend and backend with one env file
- **−** Requires at least one OpenAI, Anthropic or Gemini API key; no bundled local model
- **−** Ollama models are possible but the README calls the results poor quality
- **−** Replicate key must be set in backend/.env, not in the UI
- **−** Docker setup has no hot reload; file changes need a rebuild

<sub>no GPU · Compose · Needs OpenAI, Anthropic or Gemini API key, Replicate API key (optional), Playwright Chromium (optional preview) · Models: Gemini 3 Flash Preview, Gemini 3.1 Pro Preview, GPT-5.5, GPT-5.4 Mini, Claude Opus 4.6/4.8 · port 5173 · [Repo](https://github.com/abi/screenshot-to-code) · [Demo](https://screenshottocode.com/)</sub>

### [Tabby](https://github.com/TabbyML/tabby) <sub>★ 33.9k · NOASSERTION · Jun 2026</sub>

**Self-hosted code completion and chat server for IDEs.**

Serves code completion and chat to VS Code, Vim and JetBrains extensions from one self-contained binary with no external database. Runs local models such as StarCoder-1B and Qwen2-1.5B-Instruct on CUDA or Apple Metal, exposes an OpenAPI interface on port 8080, and adds an Answer Engine, repository and GitLab merge-request indexing and LDAP auth. For teams that want an on-premises Copilot alternative.

- **+** Single binary with embedded storage; no DBMS or cloud service required
- **+** One docker run command starts a server with completion and chat models
- **+** Repository context indexing, GitHub and GitLab integration, LDAP auth, usage reports
- **+** Live demo instance and documented extensions for VS Code, Vim and IntelliJ
- **−** Last commit June 2026; recent news points to the separate Pochi agent
- **−** License is non-standard (GitHub reports NOASSERTION); check terms before deploying
- **−** Model list and hardware guidance live only in the external docs
- **−** Building from source needs Rust, protobuf and OpenBLAS

<sub>GPU optional · Models: StarCoder-1B, Qwen2-1.5B-Instruct, CodeLlama 7B, CodeGemma, CodeQwen · port 8080 · [Repo](https://github.com/TabbyML/tabby) · [Demo](https://tabby.tabbyml.com) · [Docs](https://tabby.tabbyml.com/docs/welcome/)</sub>

### [Onlook](https://github.com/onlook-dev/onlook) <sub>★ 26.9k · Apache-2.0 · Jul 2026</sub>

**Visual editor that edits Next.js and Tailwind apps with AI.**

Browser-based editor that loads a Next.js and Tailwind project into a web container, renders it in an iframe and maps DOM elements back to source so you can drag, restyle and edit visually or through an AI chat. Built on Next.js, tRPC, Supabase, Drizzle and the Vercel AI SDK with OpenRouter for models and CodeSandbox for sandboxes. For designers and front-end developers working on Next.js codebases.

- **+** Edits map directly to code; right-click any element to open its source location
- **+** Branching, checkpoints and a real-time code editor beside the visual canvas
- **+** Apache-2.0 with Dockerfile and compose file for local runs
- **+** Figma-like layers, pages, brand tokens and asset management
- **−** Next.js plus Tailwind only; other frameworks are roadmap items, not supported
- **−** Depends on hosted services: Supabase, OpenRouter, CodeSandbox SDK, Freestyle
- **−** Team comments, MCP support and image references are unchecked roadmap items
- **−** Maintainers are moving to a hosted early-access product; last commit July 2026

<sub>no GPU · Docker + Compose · Needs Supabase (auth, database, storage), OpenRouter API key, CodeSandbox SDK, Bun · Models: OpenRouter-hosted models, Morph Fast Apply, Relace · [Repo](https://github.com/onlook-dev/onlook) · [Demo](https://onlook.com) · [Docs](https://docs.onlook.com)</sub>

### [Archon](https://github.com/coleam00/Archon) <sub>★ 23.6k · MIT · Oct 2026</sub>

**YAML workflow engine that runs coding agents in isolated worktrees.**

Defines development processes (plan, implement, validate, review, PR) as YAML workflows and runs them through Claude Code, Codex or Pi, each run in its own git worktree. Deterministic nodes mix with AI nodes and human approval gates; runs start from the CLI, a web console, Slack, Telegram, Discord or GitHub webhooks, with state in SQLite or PostgreSQL. For teams standardizing how agents ship code.

- **+** Every run isolated in a git worktree; parallel fixes without conflicts
- **+** Bundled sdlc pack: ship, triage, investigate, plan, deliver, review, validate, upkeep
- **+** Adapters for web, CLI, Slack, Telegram, Discord and GitHub webhooks
- **+** Telemetry documented field by field; DO_NOT_TRACK=1 or CI=true disables it
- **−** Requires Claude Code (or Codex, Pi) installed separately; binaries need CLAUDE_BIN_PATH
- **−** Anonymous telemetry is on by default
- **−** x64 quick-install binaries require AVX2; older CPUs must build from source
- **−** Workflows from v0.11.1 and earlier no longer ship and must be copied manually

<sub>no GPU · Docker + Compose · Needs Bun, Claude Code (or Codex or Pi), GitHub CLI, SQLite or PostgreSQL · Models: Claude Code, Codex, Pi · [Repo](https://github.com/coleam00/Archon) · [Docs](https://archon.diy/docs/)</sub>

### [OpenChamber](https://github.com/openchamber/openchamber) <sub>★ 11.3k · MIT · Oct 2026</sub>

**Multi-device workspace for running and reviewing OpenCode agent sessions.**

Front end over the OpenCode CLI that starts agent sessions, shows diffs and takes changes through review from desktop (macOS, Windows, Linux), web/PWA, VS Code, iOS and Android. Adds Session Goals that keep an agent iterating toward an outcome, Multi-run to compare up to five models, GitHub issue and PR context, scheduled prompts and encrypted remote access via Private Relay. For developers who run OpenCode.

- **+** Multi-run compares up to five models; Fusion merges the strongest parts
- **+** Private Relay pairs devices by QR code without opening ports; end-to-end encrypted
- **+** Desktop builds bundle the matching OpenCode CLI
- **+** Scheduled tasks with Session Goals continue until done, blocked or capped
- **−** Tied to OpenCode; no other agent runtime
- **−** CLI and Web need Node.js 22+ and a separately installed OpenCode CLI
- **−** Linux AppImages need FUSE (libfuse.so.2) or APPIMAGE_EXTRACT_AND_RUN=1
- **−** Port and reverse-proxy details are in separate docs, not the README

<sub>no GPU · Docker + Compose · Needs OpenCode CLI (bundled in desktop builds), Node.js 22+ (CLI and Web) · Models: models available through OpenCode · [Repo](https://github.com/openchamber/openchamber)</sub>

### [Open SWE](https://github.com/langchain-ai/open-swe) <sub>★ 10.8k · MIT · Oct 2026</sub>

**LangChain coding agent that plans, implements and reviews pull requests.**

LangGraph-based agent that investigates a repository, implements changes in a per-thread Linux sandbox, validates them and opens a pull request, then reviews PRs and watches CI with /baby-sit. Work starts from a dashboard, GitHub issues or PR comments, Slack or Linear. Deploys into your infrastructure with a backend, dashboard, GitHub and Slack apps, for teams building an internal coding-agent service.

- **+** Covers build, review, investigate and operate flows, with subagents for parallel work
- **+** Durable execution and thread state via LangGraph; sandboxes persist per thread
- **+** Configurable models, reasoning effort, skills, MCP integrations and sandbox providers
- **+** Push approvals gate detected git pushes; PR chat excludes mutation tools
- **−** Production standalone Agent Server deployments require a license key
- **−** Maintainers are not accepting issues or contributions; breaking changes expected
- **−** LangSmith is the default sandbox and tracing provider; alternatives need configuration
- **−** CLI mode executes commands locally as you, with no sandbox isolation

<sub>no GPU · Docker + Compose · Needs LangSmith (default sandbox and tracing), GitHub App, Slack app (optional), model provider credentials · Models: configurable LLM providers · [Repo](https://github.com/langchain-ai/open-swe)</sub>

### [Background Agents](https://github.com/ColeMurray/background-agents) <sub>★ 3.3k · MIT · Oct 2026</sub>

**Background coding agents on cloud sandboxes with Slack, GitHub and Linear triggers.**

Runs coding sessions in cloud sandboxes coordinated by a Cloudflare Workers control plane, driven from a web UI, Slack, GitHub PR comments, Linear issues or webhooks. Sessions use OpenCode or the Claude Agent harness with Anthropic, OpenAI, xAI, DeepSeek or Z.AI models, with multiplayer editing, commit attribution, child sessions and cron or event automations. For single-tenant engineering orgs.

- **+** Snapshot restore, prebuilt images and proactive warming for fast session starts
- **+** Automations from cron, Sentry alerts, GitHub workflow runs and inbound webhooks
- **+** Secrets encrypted with AES-256-GCM and scoped globally, per repo or per environment
- **+** Browser automation, code-server and a web terminal inside each sandbox
- **−** Single-tenant only; all users must be trusted members of one organization
- **−** Control plane requires Cloudflare Workers, Durable Objects and D1
- **−** Sandboxes run on third-party providers (Modal, Daytona, E2B, OpenComputer, Vercel)
- **−** Cached credentials can persist in snapshots; grant removal does not revoke tokens

<sub>no GPU · Compose · Needs Cloudflare Workers, Durable Objects and D1, Sandbox provider (Modal, Daytona, E2B, OpenComputer or Vercel Sandbox), GitHub App, Slack and Linear apps (optional) · Models: Anthropic Claude (API key or subscription), OpenAI Codex via ChatGPT subscription, xAI Grok via SuperGrok, OpenCode Zen and Go, Z.AI Coding Plan · [Repo](https://github.com/ColeMurray/background-agents)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Search

Private search engines and AI answer engines that keep queries on your host. <sub>8 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Metasearch engines need upstream providers; check rate limits and whether results are cached.
- Answer engines call an LLM per query; budget tokens before exposing them to a team.
- Check how results are attributed; answer engines without citations are hard to verify.

</details>

### [Firecrawl](https://github.com/firecrawl/firecrawl) <sub>★ 189.7k · AGPL-3.0 · Oct 2026</sub>

**Web scraping and crawling API that returns LLM-ready markdown.**

API that turns URLs into markdown, HTML, screenshots or schema-based JSON, with endpoints for search, scrape, crawl, map, batch scrape, page interaction and a prompt-driven agent. Handles JS-rendered pages and parses hosted PDFs and DOCX. SDKs for Python, Node, Go, Java, Elixir, Rust and Ruby plus an MCP server and CLI, for teams feeding web content to RAG pipelines and agents.

- **+** Seven SDKs plus CLI and MCP server; SDKs poll async crawl jobs automatically
- **+** Crawl, map and batch-scrape endpoints return job IDs for large sites
- **+** Scrape supports actions (click, scroll, write, wait) before extraction
- **+** Compose file at the repo root for self-hosting
- **−** README is written around the hosted API and keys; self-hosting lives in separate docs
- **−** AGPL-3.0 license; network use of a modified version triggers source obligations
- **−** Agent endpoint runs the hosted spark-2 model, not a local LLM
- **−** Proxy rotation and anti-bot handling are hosted-service features

<sub>no GPU · Compose · [Repo](https://github.com/firecrawl/firecrawl) · [Demo](https://firecrawl.dev/playground) · [Docs](https://docs.firecrawl.dev) · [Site](https://firecrawl.dev)</sub>

### [Crawl4AI](https://github.com/unclecode/crawl4ai) <sub>★ 85.0k · Apache-2.0 · Oct 2026</sub>

**Python crawler that turns pages into LLM-ready markdown, with a Docker API.**

Async Playwright crawler (pip install crawl4ai) that renders pages in Chromium, Firefox or WebKit and emits clean or filtered markdown, with CSS, XPath and regex extraction needing no LLM, or LLM extraction via any LiteLLM provider. Deep crawling (BFS, DFS, priority-scored) and adaptive crawling are built in. A Docker server on port 11235 exposes /md, /html, /crawl, /screenshot, /pdf and MCP behind an API token.

- **+** Structured extraction with CSS, XPath or regex schemas needs no LLM or API key
- **+** Docker server with REST, streaming crawl, MCP, dashboard and playground; amd64 and arm64
- **+** Deep crawl strategies with crash recovery via resume_state
- **+** Persistent browser profiles, CDP remote browsers and an undetected-browser adapter
- **−** Apache-2.0 but requires attribution (badge or text) in your project
- **−** Docker server answers only inside the container until CRAWL4AI_API_TOKEN is set
- **−** Web search and answer endpoints exist only in the paid cloud
- **−** Runs full browsers; the docker run example allocates 1 GB shared memory

<sub>no GPU · Docker + Compose · Needs Playwright Chromium (installed by crawl4ai-setup) · Models: any LiteLLM provider for LLM extraction (OpenAI, Ollama and others) · port 11235 · [Repo](https://github.com/unclecode/crawl4ai) · [Docs](https://docs.crawl4ai.com/)</sub>

### [Vane](https://github.com/ItzCrazyKns/Vane) <sub>★ 37.1k · MIT · Sep 2026</sub>

**Self-hosted answer engine with cited sources over SearXNG.**

Next.js answer engine (formerly Perplexica) that runs searches through a bundled SearXNG instance, then answers with citations using Ollama, OpenAI-compatible servers, OpenAI, Anthropic, Gemini or Groq models. Offers Speed, Balanced and Quality modes, web, discussion and academic sources, image and video search, file uploads and a search API. One container on port 3000; a slim image uses your own SearXNG.

- **+** Single Docker image bundles SearXNG; no search API key needed
- **+** Local models via Ollama or any OpenAI-compatible server, plus cloud providers
- **+** Browser search-engine shortcut via /?q=%s and a REST search API
- **+** Slim image works with an existing SearXNG (JSON format and Wolfram Alpha enabled)
- **−** No authentication yet; listed as an upcoming feature
- **−** Own-SearXNG setups must enable JSON output and Wolfram Alpha or searches fail
- **−** Tavily and Exa search backends are marked coming soon
- **−** Ollama on Linux must listen on 0.0.0.0 for the container to reach it

<sub>no GPU · Docker + Compose · Needs SearXNG (bundled in the default image), LLM provider (Ollama, OpenAI-compatible server or cloud API) · Models: Ollama, OpenAI, Anthropic Claude, Google Gemini, Groq · port 3000 · [Repo](https://github.com/ItzCrazyKns/Vane)</sub>

### [GPT Researcher](https://github.com/assafelovic/gpt-researcher) <sub>★ 29.9k · Apache-2.0 · Sep 2026</sub>

**Research agent that writes cited reports from web and local documents.**

Planner and execution agents generate research questions, scrape 20+ sources, filter passages (Jev by default, BM25 fallback with no key) and write cited reports over 2,000 words, exportable to PDF and Word. Runs as a FastAPI server on port 8000 with a static or Next.js frontend, or as a pip package; local PDF, Office, CSV and Markdown files can be sources. For analysts automating long-form research.

- **+** Deep Research mode: tree-like exploration, about 5 minutes and $0.40 per run on o3-mini
- **+** Hybrid retrievers: Tavily plus MCP servers such as GitHub as research sources
- **+** Works with any OpenAI-compatible endpoint via OPENAI_BASE_URL
- **+** Multi-agent LangGraph and AG2 variants produce 5-6 page PDF, DOCX and Markdown reports
- **−** Default setup needs OpenAI and Tavily API keys
- **−** Jev context filtering needs a TYPESAFE_API_KEY; the fallback is keyword BM25
- **−** Python 3.12 or later required
- **−** Disclaimer labels the project experimental and for academic purposes

<sub>no GPU · Docker + Compose · Needs OpenAI or OpenAI-compatible LLM API, Tavily API key (default retriever), TypeSafe API key (optional Jev filter) · Models: OpenAI models, any OpenAI-compatible endpoint via OPENAI_BASE_URL, Gemini 2.5 Flash Image (inline images) · port 8000 · [Repo](https://github.com/assafelovic/gpt-researcher) · [Docs](https://docs.gptr.dev) · [Site](https://gptr.dev)</sub>

### [Jina Reader](https://github.com/jina-ai/reader) <sub>★ 12.1k · Apache-2.0 · May 2026</sub>

**Converts any URL or search query into LLM-friendly markdown.**

Open-source branch of the service behind r.jina.ai and s.jina.ai: fetches a page with headless Chrome or curl-impersonate, parses PDFs and Office files, and returns markdown, text, HTML, screenshots or JSON controlled by request headers (engine, timeout, token limits). The ghcr.io image bundles Chrome, LibreOffice and CJK fonts, serves HTTP/1.1 on 8081 and h2c on 8080, and runs stateless or with S3-compatible caching.

- **+** Prebuilt image with Chrome, LibreOffice and CJK fonts; stateless by default
- **+** Fine-grained headers: x-respond-timing, x-max-tokens, x-token-budget, x-target-selector
- **+** Optional VLM captions for images without alt text
- **+** Semantic markdown chunking by heading or block level
- **−** Hosted proxy pool, rate limiting and MongoDB storage layer are not in the OSS branch
- **−** Needs non-redistributable assets (MaxMind GeoLite2, Source Han Sans) fetched at build
- **−** Last commit May 2026; the SaaS resync was April 2026
- **−** Default h2c port 8080 needs --http2-prior-knowledge from curl; use 8081 otherwise

<sub>no GPU · Docker + Compose · Needs Headless Chrome and LibreOffice (bundled in image), S3-compatible bucket (optional cache), VLM endpoint for image captions (optional) · port 8081 · [Repo](https://github.com/jina-ai/reader) · [Demo](https://jina.ai/reader#demo) · [Docs](https://r.jina.ai/docs) · [Site](https://jina.ai/reader)</sub>

### [Local Deep Research](https://github.com/LearningCircuit/local-deep-research) <sub>★ 9.2k · MIT · Oct 2026</sub>

**Agentic research assistant with local LLMs, SearXNG and encrypted libraries.**

Runs multi-step research across the web, academic engines and your own documents using Ollama or any OpenAI-compatible endpoint, with a LangGraph agent that picks engines adaptively and writes cited reports. Each user gets an AES-256 SQLCipher database, and egress scopes limit which engines and providers a run may use. Web UI on port 5000 via Docker, Compose or pip, for privacy-focused researchers.

- **+** Reports about 95% SimpleQA fully local on one RTX 3090 with Qwen3.6-27B
- **+** Per-user SQLCipher databases; keys derived from the password, never stored
- **+** No telemetry; Docker images signed with Cosign, with SLSA provenance and SBOMs
- **+** Downloaded sources build a searchable, embedded personal library
- **−** Needs Ollama (or an LLM endpoint) and SearXNG running separately
- **−** Private or localhost engine URLs are blocked unless an operator env var allows them
- **−** Requires an AVX-capable x86-64 CPU; older CPUs crash with Illegal instruction
- **−** docker run --network host only works on native Linux; Docker Desktop needs Compose

<sub>GPU optional · Docker + Compose · Needs Ollama or OpenAI-compatible LLM endpoint, SearXNG, SQLCipher (bundled wheels) · Models: Ollama models (e.g. gpt-oss:20b, Qwen3.6-27B), any OpenAI-compatible endpoint · port 5000 · [Repo](https://github.com/LearningCircuit/local-deep-research)</sub>

### [Morphic](https://github.com/miurla/morphic) <sub>★ 9.2k · Apache-2.0 · Oct 2026</sub>

**AI search engine with generative UI and bundled SearXNG.**

Next.js search app that answers with cited sources and renders results as streamed UI components rather than plain markdown. Works with OpenAI, Anthropic, Google, Ollama, Vercel AI Gateway or OpenAI-compatible providers and Tavily, SearXNG, Brave or Exa search. Docker Compose starts PostgreSQL, Redis, SearXNG and Morphic on port 3000, so no search API key is needed.

- **+** Compose stack includes SearXNG, so no paid search key is needed
- **+** Dynamic provider detection; Ollama works for fully local models
- **+** Chat history in PostgreSQL, shareable result URLs, file uploads
- **+** Supabase Auth with guest mode for anonymous use
- **−** Authentication depends on Supabase; no built-in local auth
- **−** Needs PostgreSQL and Redis even for a single user
- **−** At least one AI provider API key or an Ollama endpoint is required
- **−** Feature configuration lives in a separate CONFIGURATION.md, not the README

<sub>no GPU · Docker + Compose · Needs PostgreSQL, Redis, SearXNG (bundled) or Tavily, Brave, Exa API, Supabase (auth) · Models: OpenAI, Anthropic, Google, Ollama, Vercel AI Gateway · port 3000 · [Repo](https://github.com/miurla/morphic)</sub>

### [MAESTRO](https://github.com/murtaza-nasir/maestro) <sub>★ 1.5k · AGPL-3.0 · Apr 2026</sub>

**Multi-agent research platform that writes long reports from documents and web.**

Planning, Research, Reflection and Writing agents run research missions over uploaded PDF, Word and Markdown documents and web search, producing long reports with visible agent steps. Retrieval uses BGE-M3 embeddings in PostgreSQL with pgvector; any OpenAI-compatible API, including Azure OpenAI, can serve the models. Docker Compose stack on http://localhost with CPU and NVIDIA variants.

- **+** Mission checkpoints allow pause, resume and writing-phase recovery
- **+** Local embeddings (BGE-M3) and pgvector; local LLMs via OpenAI-compatible API
- **+** Search providers: Tavily, LinkUp, Jina and SearXNG
- **+** CPU-only compose file plus automatic NVIDIA GPU detection
- **−** 16 GB RAM minimum (32 GB recommended) and 30 GB disk
- **−** Alpha (v0.1.10-alpha); last commit April 2026
- **−** Dual-licensed AGPLv3 or commercial; proprietary use needs a paid license
- **−** First startup takes 5 to 10 minutes while models download

<sub>RAM ≥ 16 GB · GPU optional · Compose · Needs Docker Compose v2+, API key for an AI provider or an OpenAI-compatible endpoint, PostgreSQL with pgvector (in compose) · Models: OpenAI-compatible APIs, Azure OpenAI (GPT-5), BGE-M3 embeddings · port 80 · [Repo](https://github.com/murtaza-nasir/maestro) · [Docs](https://murtaza-nasir.github.io/maestro/)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Observability

Tracing, evaluation and prompt management for LLM applications. <sub>13 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Confirm SDK support for your framework (OpenTelemetry, LangChain, OpenAI SDK) and your language.
- Evaluation features vary widely; check whether evals run on your data without a cloud account.
- Retention and storage backend decide the host size; traces grow fast.

</details>

### [Langfuse](https://github.com/langfuse/langfuse) <sub>★ 35.5k · NOASSERTION · Oct 2026</sub>

**Tracing, prompt management and evals for LLM apps on ClickHouse.**

Ingests traces of LLM calls, retrieval and agent steps via Python and JS/TS SDKs or drop-in OpenAI, LangChain, LlamaIndex, LiteLLM and Vercel AI SDK integrations, then adds prompt versioning with caching, LLM-as-a-judge and code evaluators, datasets and a playground. Stores data in ClickHouse; deploys with docker compose, Helm on Kubernetes, or Terraform for AWS, Azure and GCP. For teams debugging and evaluating LLM apps.

- **+** Public OpenAPI spec, Postman collection and typed Python and JS/TS SDKs
- **+** Prompt management with server and client caching adds no request latency
- **+** Deployment paths from docker compose to Helm and Terraform templates
- **+** Integrations with Dify, Flowise, Langflow, OpenWebUI, LobeChat, CrewAI, smolagents
- **−** MIT except the ee folders; enterprise features need a commercial license
- **−** Runs on ClickHouse plus other services; heavier than single-binary tools
- **−** Default compose inherits Docker json-file logging with no rotation; disk can fill
- **−** No Dockerfile at the repo root; images come from Docker Hub

<sub>no GPU · Compose · Needs ClickHouse · [Repo](https://github.com/langfuse/langfuse) · [Demo](https://langfuse.com/demo) · [Docs](https://langfuse.com/docs) · [Site](https://langfuse.com)</sub>

### [MLflow](https://github.com/mlflow/mlflow) <sub>★ 28.3k · Apache-2.0 · Oct 2026</sub>

**Tracing, evals, prompt registry and AI gateway plus classic ML tracking.**

Single mlflow server (port 5000) that records OpenTelemetry traces from 60+ frameworks via one-line autolog, runs evaluations with 50+ metrics and LLM judges, versions and optimizes prompts, and fronts providers through an OpenAI-compatible AI Gateway with rate limits, fallbacks and traffic splitting. Keeps the original experiment tracking, model registry and deployment tooling. For teams wanting one platform for GenAI and ML.

- **+** One-line autolog for 60+ frameworks in Python, TypeScript and Java; MCP and OTel native
- **+** Starts with uvx mlflow server; no separate database needed to begin
- **+** AI Gateway adds credential management, guardrails and A/B traffic splitting
- **+** Setup wizard lets Claude Code, Codex or OpenCode add tracing to a project
- **−** README covers the quickstart; production backend store and auth setup live in docs
- **−** Broad scope (ML tracking plus GenAI) means a large install and UI surface
- **−** No Dockerfile or compose file at the repo root
- **−** TypeScript and Java coverage is smaller than Python (5 TS and 2 Java frameworks listed)

<sub>no GPU · Models: any LLM provider via autolog or the AI Gateway · port 5000 · [Repo](https://github.com/mlflow/mlflow) · [Demo](https://demo.mlflow.org/) · [Docs](https://mlflow.org/docs/latest) · [Site](https://mlflow.org/)</sub>

### [promptfoo](https://github.com/promptfoo/promptfoo) <sub>★ 25.8k · MIT · Oct 2026</sub>

**CLI for evaluating and red-teaming prompts, agents and RAG.**

Runs prompt and model evaluations from a YAML config via promptfoo eval, compares providers side by side, and generates red-team vulnerability reports; promptfoo view opens a local web viewer. Installs with npm, Homebrew or pip, runs in CI/CD, and can scan pull requests for LLM security issues, for developers testing prompts and agents before release.

- **+** Evals run locally; prompts stay on your machine
- **+** Red-team scans produce vulnerability reports alongside quality evals
- **+** Live reload and caching for fast iteration; npx usage needs no install
- **+** MIT licensed and still open source after joining OpenAI
- **−** Primarily a CLI; the web viewer is a local results UI, not a multi-user server
- **−** Most providers require an API key; local use needs Ollama or similar
- **−** README is short; config syntax, assertions and providers are only in the docs
- **−** Dockerfile exists at the root but the README gives no Docker instructions

<sub>no GPU · Docker · Needs Node.js (npm) or Python (pip), LLM provider API key or Ollama · Models: OpenAI, Anthropic, Azure, Bedrock, Ollama · [Repo](https://github.com/promptfoo/promptfoo) · [Docs](https://www.promptfoo.dev/docs/) · [Site](https://www.promptfoo.dev)</sub>

### [Opik](https://github.com/comet-ml/opik) <sub>★ 22.4k · Apache-2.0 · Oct 2026</sub>

**Trace, evaluate and monitor LLM apps and agents, Apache-2.0 end to end.**

Logs trace trees for LLM calls, tool executions and agent steps via Python and TypeScript SDKs, OpenTelemetry or framework integrations, then runs datasets, experiments and LLM-as-a-judge metrics for hallucination, moderation and RAG quality, with online evaluation rules in production. Self-hosts with ./opik.sh (Docker Compose, UI on port 5173) or a Helm chart. For ML engineers moving agents to production.

- **+** Full platform (backend, web app, evals, prompt management) under Apache-2.0
- **+** Designed for 40M+ traces per day; online evaluation rules on production traffic
- **+** PyTest integration gates LLM pipelines in CI
- **+** MCP server lets Claude Code, Cursor, Codex or opencode query traces and run evals
- **−** No Dockerfile or compose file at the repo root; install goes through opik.sh
- **−** Multi-service stack (databases, caches, backend, frontend); not a single binary
- **−** Guardrails and the optimizer are separate profiles and SDKs to enable
- **−** README is heavy with Comet Cloud links and UTM tracking

<sub>no GPU · Models: any LLM via SDK, OpenTelemetry or framework integrations (Google ADK, AG2, Autogen, Flowise) · port 5173 · [Repo](https://github.com/comet-ml/opik) · [Docs](https://www.comet.com/docs/opik/) · [Site](https://www.comet.com/site/products/opik/)</sub>

### [Phoenix](https://github.com/Arize-ai/phoenix) <sub>★ 11.8k · NOASSERTION · Oct 2026</sub>

**OpenTelemetry-based LLM tracing, evals and prompt playground.**

Collects traces through OpenInference and OpenTelemetry instrumentation for OpenAI Agents SDK, Claude Agent SDK, LangGraph, CrewAI, LlamaIndex and DSPy, then adds LLM-based response evals, datasets, experiments and a prompt playground. Starts with pip install arize-phoenix and phoenix serve, ships Docker images and a Helm chart, and exposes a remote MCP endpoint at /mcp. For engineers troubleshooting LLM apps.

- **+** Single pip package runs the whole platform; uvx arize-phoenix serve needs no install
- **+** Remote MCP server at /mcp for Claude Code and Cursor; built-in PXI agent
- **+** Vendor and language agnostic via OpenTelemetry and OpenInference
- **+** One-click deploys for Railway, Render, Cloud Run, Azure and AWS CloudFormation
- **−** License is non-standard (GitHub reports NOASSERTION); check terms before deploying
- **−** Managed production workflows are steered to the paid Arize AX product
- **−** Azure template serves plain HTTP; needs a TLS proxy before production
- **−** TypeScript evals package is alpha; stdio MCP package is in maintenance mode

<sub>no GPU · Docker + Compose · Models: OpenAI, Anthropic, Google GenAI and ADK, AWS Bedrock, OpenRouter · port 6006 · [Repo](https://github.com/Arize-ai/phoenix) · [Docs](https://arize.com/docs/phoenix/) · [Site](https://phoenix.arize.com)</sub>

### [Helicone](https://github.com/Helicone/helicone) <sub>★ 6.2k · Apache-2.0 · Sep 2026</sub>

**LLM proxy gateway with request logging, cost tracking and sessions.**

Sits as an OpenAI-compatible gateway in front of 100+ models with routing and automatic fallbacks, logging every request with cost, latency and session traces, plus a playground and prompt versioning. Self-hosts via a compose script that runs six services: web app, Jawn log server, Workers proxy, Supabase, ClickHouse and MinIO. For engineers who want observability by swapping an endpoint.

- **+** One-line integration: point the OpenAI SDK baseURL at the gateway
- **+** Async logging path via OpenLLMetry for apps that cannot proxy
- **+** Open LLM cost database covering 300+ models; MCP server for data export
- **+** Apache-2.0; self-host compose script included
- **−** Six-service stack including Supabase, ClickHouse, MinIO and a Cloudflare Workers proxy
- **−** Production Helm chart is enterprise only, by contacting sales
- **−** Manual deployment is explicitly not recommended
- **−** README quickstart is cloud-first; self-hosting details are in external docs

<sub>no GPU · Docker · Needs Supabase (database and auth), ClickHouse, MinIO, Cloudflare Workers runtime (proxy) · Models: 100+ providers via gateway (OpenAI, Azure, Anthropic, Bedrock, Gemini, Groq, Together, Fireworks, Ollama) · [Repo](https://github.com/Helicone/helicone) · [Demo](https://helicone.ai/demo) · [Docs](https://docs.helicone.ai/) · [Site](https://www.helicone.ai)</sub>

### [LangWatch](https://github.com/langwatch/langwatch) <sub>★ 4.9k · Apache-2.0 · Oct 2026</sub>

**Agent observability, simulation testing, AI gateway and governance in one.**

Traces LLM and agent calls through OpenTelemetry and SDK integrations, runs simulation-based agent tests and evaluations, manages prompts, and adds an OpenAI- and Anthropic-compatible gateway with virtual keys and budgets. Also tracks coding-agent sessions (Claude Code, Codex, Copilot) with cost per pull request, and starts locally with npx @langwatch/server. For platform teams governing AI use across a company.

- **+** npx @langwatch/server starts a local instance with only Node.js installed
- **+** Coding-agent tracking: sessions and cost per PR for Claude Code, Codex, Copilot
- **+** Gateway virtual keys with budgets for customers or employees
- **+** Governance ingests Copilot Studio, Claude and OpenAI compliance APIs, Workato, S3 audit feeds
- **−** Open-core: modules under platform/app/ee need a commercial license in production
- **−** No Dockerfile or compose file at the repo root; production setup is in external docs
- **−** README is a feature index; architecture and storage needs are not described
- **−** Cloud signup is the first call to action; self-host gets one line

<sub>no GPU · Needs Node.js · Models: OpenAI, Anthropic, Azure OpenAI, Vertex AI, Bedrock · [Repo](https://github.com/langwatch/langwatch) · [Docs](https://langwatch.ai/docs/introduction) · [Site](https://langwatch.ai)</sub>

### [Agenta](https://github.com/Agenta-AI/agenta) <sub>★ 4.8k · NOASSERTION · Oct 2026</sub>

**Team workspace for building chat-driven agents that run in Slack and WhatsApp.**

Lets teams create agents by describing work in chat, connect tools through MCP or Composio, set per-agent read or write permissions, and talk to them from the web app, Slack, Telegram or WhatsApp. Agents keep memory and skills, run on schedules or events, and each session gets a sandbox with a browser and filesystem; every run is traced and costed. Runs Claude Code, Pi or Codex harnesses on API models, Ollama or a Claude or ChatGPT subscription.

- **+** Runs on an existing Claude or ChatGPT subscription instead of metered API billing
- **+** Per-agent tool permissions with read or write scopes and human-in-the-loop gates
- **+** Every run traced and cost-tracked; configurations and versions are visible
- **+** Agents reachable from Slack, Telegram and WhatsApp Business
- **−** README no longer covers the earlier prompt-management and evaluation product
- **−** Self-host instructions are delegated to an agent skill, not written out
- **−** Harness support limited to Claude Code, Pi and Codex today
- **−** No Dockerfile or compose file at the repo root

<sub>no GPU · Needs Claude Code, Pi or Codex harness, LLM API, Ollama, or a Claude or ChatGPT subscription, Composio (optional, 1,000+ app integrations) · Models: hosted models via API, Ollama, Claude and ChatGPT subscriptions · [Repo](https://github.com/Agenta-AI/agenta) · [Docs](https://agenta.ai/docs/) · [Site](https://agenta.ai)</sub>

### [Latitude](https://github.com/latitude-dev/latitude-llm) <sub>★ 4.7k · MIT · Oct 2026</sub>

**Agent observability that groups failures and dispatches coding agents to fix them.**

Captures traces, sessions and tool calls via a one-line SDK (TypeScript, Python) or OpenTelemetry, groups failing traces into tracked signals, then dispatches Claude Code or Cursor with those traces to open a fix PR and replays fixes against regression datasets. The UI is also reachable from an MCP server and CLI; self-hosts from Docker Hub images via Compose or Helm. For teams operating agents in production.

- **+** Signals auto-group failing traces with status, size and trend
- **+** Agent Dispatch sends sample traces to Claude Code or Cursor via Linear or webhooks
- **+** Regression datasets replay fixes against the real failing traces
- **+** MIT license; Compose and Helm paths plus Railway one-click
- **−** README quickstart targets the cloud; self-host steps are in external docs
- **−** Automatic fixing depends on third-party coding agents and their subscriptions
- **−** Claude Code session capture is a separate telemetry package
- **−** Storage and service requirements are not stated in the README

<sub>no GPU · Docker + Compose · Models: OpenAI, Anthropic, Bedrock, Vercel AI SDK and LangChain apps, any OpenTelemetry source · [Repo](https://github.com/latitude-dev/latitude-llm) · [Docs](https://docs.latitude.so) · [Site](https://latitude.so)</sub>

### [Laminar](https://github.com/lmnr-ai/lmnr) <sub>★ 3.4k · Apache-2.0 · Sep 2026</sub>

**Rust-based agent tracing with SQL queries, signals and evals.**

OpenTelemetry-native tracing for Vercel AI SDK, LangChain, OpenAI, Anthropic, Gemini and more with one line of SDK code, stored in ClickHouse and queried with SQL from the UI, MCP server or CLI. Signals watch every run for behaviors described in plain English and ping Slack; evals run from an SDK and CLI. docker compose up serves the UI on port 5667, for teams debugging browser and tool-using agents.

- **+** Signals: describe a failure in plain English and get a Slack ping when it occurs
- **+** SQL over traces, spans, metrics and events, also from your coding agent via MCP
- **+** Rust backend with 20x trace compression and a realtime trace viewer
- **+** Custom Postgres schema support for shared database deployments
- **−** Anonymous usage telemetry is on by default; LAMINAR_TELEMETRY_DISABLED=true opts out
- **−** Production is steered to the managed platform or the heavier docker-compose-full stack
- **−** AI features (chat-with-trace, SQL-with-AI) need a configured LLM provider
- **−** ClickHouse upgrades need manual container recreation and log-table truncation

<sub>no GPU · Compose · Needs ClickHouse, PostgreSQL, LLM provider (optional, for AI features) · Models: Gemini, OpenAI and OpenAI-compatible gateways (LiteLLM, OpenRouter, vLLM), AWS Bedrock, Azure AI Foundry · port 5667 · [Repo](https://github.com/lmnr-ai/lmnr) · [Docs](https://laminar.sh/docs) · [Site](https://laminar.sh)</sub>

### [Pezzo](https://github.com/pezzolabs/pezzo) <sub>★ 3.3k · Apache-2.0 · Aug 2026</sub>

**Prompt management, observability and caching for LLM apps.**

Stores and versions prompts, logs requests with cost and latency, and caches LLM responses, exposed through Node.js and Python clients and a LangChain integration. Runs on PostgreSQL, ClickHouse, Redis and SuperTokens via Docker Compose, with a GraphQL API server and a console UI. For small teams that want prompt delivery without code changes.

- **+** Prompts delivered from the console without redeploying application code
- **+** Built-in response caching to cut repeated-call cost and latency
- **+** Node.js and Python clients plus LangChain support
- **+** Apache-2.0; infra is all open source (PostgreSQL, ClickHouse, Redis, SuperTokens)
- **−** Last commit August 2026 with no release notes in the README
- **−** Four backing services for a modest feature set
- **−** README is thin; features are shown as screenshots, details only in docs
- **−** No evaluation or dataset features mentioned

<sub>no GPU · Compose · Needs PostgreSQL, ClickHouse, Redis, SuperTokens, Node.js 18+ · port 4200 · [Repo](https://github.com/pezzolabs/pezzo) · [Docs](https://docs.pezzo.ai/) · [Site](https://pezzo.ai)</sub>

### [OpenLIT](https://github.com/openlit/openlit) <sub>★ 2.8k · Apache-2.0 · Oct 2026</sub>

**OpenTelemetry-native tracing, evals, guardrails and GPU monitoring for agents.**

Receives OTLP on ports 4317 and 4318 from the openlit Python or TypeScript SDK, which auto-instruments 70+ providers, frameworks and vector DBs, and stores GenAI-convention traces in ClickHouse behind a dashboard on port 3000. Adds LLM-as-a-judge evals, prompt-injection guardrails, Prompt Hub, a rule engine, a secrets Vault, OpenGround model comparison and an NVIDIA, AMD and Intel GPU collector. For teams on existing OpenTelemetry stacks.

- **+** Follows OpenTelemetry GenAI semantic conventions; your collector can fan out to other backends
- **+** GPU collector reports utilization, memory, power and temperature correlated with traces
- **+** CLI instruments Claude Code, Cursor, Codex and Windsurf sessions
- **+** Connectors for ClickHouse, Grafana Tempo, Loki, Prometheus and Jaeger
- **−** Coding-agent capture needs a separate CLI install and configure step
- **−** Guardrails run in the SDK, so each app must be updated to use them
- **−** README does not state hardware needs or ClickHouse sizing
- **−** No Dockerfile at the repo root; compose only

<sub>no GPU · Compose · Needs ClickHouse · Models: OpenAI, Ollama, Anthropic, DeepSeek, Cohere · port 3000 · [Repo](https://github.com/openlit/openlit) · [Docs](https://docs.openlit.io/) · [Site](https://openlit.io)</sub>

### [Future AGI](https://github.com/future-agi/future-agi) <sub>★ 2.1k · Apache-2.0 · Oct 2026</sub>

**Evals, tracing, simulations, guardrails and a gateway for agents in one stack.**

Bundles OpenTelemetry tracing for 50+ frameworks, 50+ evaluation metrics, persona-driven text and voice simulations, 18 guardrail scanners, six prompt-optimization algorithms and a Go gateway with 100+ providers. Installs with ./bin/install (Compose v2.24+); Standalone needs 2 vCPUs and 4 GB, Distributed 12 to 16 GB; UI on port 3000, OTLP on 4318. For teams wanting one platform from prototype to production.

- **+** Gateway benchmarks: about 29k req/s on t3.xlarge, P99 under 21 ms with guardrails on
- **+** Voice-agent simulation via LiveKit, VAPI, Retell and Pipecat
- **+** Air-gapped install documented; telemetry off with FUTURE_AGI_TELEMETRY_DISABLED=true
- **+** Signed Helm chart covers both open-source and Enterprise editions
- **−** Marked a nightly release for early testing; stable version pending
- **−** No supported migration from Standalone to Distributed or Helm once data exists
- **−** Distributed profile adds PeerDB and Kafka; needs 4+ vCPUs and 12 to 16 GB
- **−** Images total about 800 MB and first boot takes several minutes

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Needs Docker Compose v2.24+, PostgreSQL, ClickHouse, Redis and Temporal (bundled in compose) · Models: 100+ providers via gateway (OpenAI, Anthropic, Gemini, Bedrock, Azure, Mistral, Groq), Ollama, vLLM, LM Studio, TGI and llamafile · port 3000 · [Repo](https://github.com/future-agi/future-agi) · [Docs](https://docs.futureagi.com) · [Site](https://futureagi.com)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Vector databases

Vector stores and hybrid search engines for embeddings. <sub>9 projects, by stars.</sub>

<details><summary>How to choose</summary>

- If you already run Postgres, check pgvector-based options before adding a new database.
- Hybrid search (keyword + vector) and filtering are where engines differ most.
- Check memory use per million vectors; it decides the host size.

</details>

### [Meilisearch](https://github.com/meilisearch/meilisearch) <sub>★ 59.5k · NOASSERTION · Oct 2026</sub>

**Rust search engine API with full-text, vector and hybrid search.**

Meilisearch is a Rust search engine with a REST API that combines full-text search (typo tolerance, facets, geosearch) with vector and hybrid search, returning results as you type. It adds API keys with fine-grained permissions, tenant tokens for multi-tenancy, conversational search and MCP and LangChain integrations. The Community Edition is MIT; sharding and S3 snapshots require the Enterprise Edition.

- **+** Search-as-you-type under 50 ms with typo tolerance and faceting
- **+** Hybrid semantic plus full-text ranking in one engine
- **+** API keys with fine-grained permissions and tenant tokens for multi-tenancy
- **+** REST API with official SDKs; MCP and LangChain integrations
- **−** Sharding, S3 snapshots and search-rule previews are Enterprise Edition (BSL or commercial)
- **−** Anonymized telemetry is on by default and must be disabled
- **−** No port, RAM or install details in the README; docs only
- **−** Vector search is documented under experimental features

<sub>no GPU · Docker · [Repo](https://github.com/meilisearch/meilisearch) · [Demo](https://where2watch.meilisearch.com/) · [Docs](https://www.meilisearch.com/docs) · [Site](https://www.meilisearch.com)</sub>

### [Milvus](https://github.com/milvus-io/milvus) <sub>★ 46.3k · Apache-2.0 · Oct 2026</sub>

**Distributed vector database with dense, sparse and hybrid search at scale.**

Milvus is a distributed vector database (Go and C++, LF AI & Data Foundation) that separates compute and storage on Kubernetes, with a Standalone Docker mode and pip-installable Milvus Lite. It offers HNSW, IVF, FLAT, SCANN and DiskANN indexes, GPU CAGRA, sparse BM25 and learned-sparse vectors for hybrid search, metadata filtering, multi-tenancy, hot/cold storage, auth, TLS and RBAC.

- **+** Index types HNSW, IVF, FLAT, SCANN, DiskANN plus GPU CAGRA
- **+** Dense, sparse (BM25, SPLADE, BGE-M3) and hybrid search in one collection
- **+** Multi-tenancy at database, collection, partition or partition-key level
- **+** Mandatory auth, TLS and RBAC; Milvus Lite via pip for local dev
- **−** Distributed mode is Kubernetes-native with several microservices to operate
- **−** No port, RAM or Docker command in the README; install lives in docs
- **−** Zilliz is the major contributor and promotes its managed cloud
- **−** Source build needs Go 1.21+, CMake, GCC 11+ and Python 3.8 to 3.11

<sub>GPU optional · Compose · Models: any embedding model or service; pymilvus[model] wraps embedding and reranking models · [Repo](https://github.com/milvus-io/milvus) · [Demo](https://milvus.io/milvus-demos) · [Docs](https://milvus.io/docs) · [Site](https://milvus.io/)</sub>

### [Qdrant](https://github.com/qdrant/qdrant) <sub>★ 35.0k · Apache-2.0 · Oct 2026</sub>

**Rust vector database with payload filtering, REST and gRPC.**

Qdrant is a Rust vector database exposing REST (OpenAPI 3.0) and gRPC on port 6333 for storing points (vectors plus JSON payload) and searching with dense, sparse and multivector (ColBERT) embeddings, rich payload filters and hybrid fusion (RRF, DBSF). It adds quantization, on-disk storage, sharding and replication, multitenancy, GPU-accelerated indexing and a web UI. Qdrant Edge runs the same engine embedded in-process.

- **+** Dense, sparse and multivector (ColBERT) search with RRF and DBSF fusion
- **+** Quantization cuts RAM up to 97 percent; on-disk storage and io_uring
- **+** REST with OpenAPI 3.0 spec plus gRPC; six official clients
- **+** Sharding and replication with zero-downtime collection resize
- **−** Default docker run has no auth and binds all interfaces
- **−** GPU acceleration covers indexing only; search runs on CPU
- **−** Qdrant Edge embedded mode is Python and Rust only
- **−** Sharding and tenant isolation require upfront design

<sub>GPU optional · Docker · Models: any embedding model; dense, sparse and late-interaction (ColBERT) vectors · port 6333 · [Repo](https://github.com/qdrant/qdrant) · [Demo](https://qdrant.to/semantic-search-demo) · [Docs](https://qdrant.tech/documentation/)</sub>

### [Chroma](https://github.com/chroma-core/chroma) <sub>★ 29.5k · Apache-2.0 · Oct 2026</sub>

**Embedding database with a four-function API for Python and JavaScript.**

Chroma is an embedding database with a four-function API (create collection, add, query, get) that tokenizes, embeds and indexes documents itself or accepts your own vectors, with metadata and document filters. It runs in-memory or persisted from the Python or JavaScript client, or as a server via chroma run; the repo ships a Dockerfile and compose file. Chroma Cloud is the hosted serverless version.

- **+** Four-function API: create collection, add, query, get
- **+** Handles tokenization, embedding and indexing; own vectors optional
- **+** Python and JavaScript clients; chroma run for client-server mode
- **+** Weekly tagged releases on Mondays with hotfixes in between
- **−** README is thin: no port, resource or auth guidance
- **−** Hosted Chroma Cloud is the headline; self-hosting detail lives in docs
- **−** Row-based API marked coming soon
- **−** No multi-user auth described in the README

<sub>no GPU · Docker + Compose · Models: built-in embedding or user-supplied vectors · [Repo](https://github.com/chroma-core/chroma) · [Docs](https://docs.trychroma.com/) · [Site](https://www.trychroma.com/)</sub>

### [pgvector](https://github.com/pgvector/pgvector) <sub>★ 23.3k · NOASSERTION · Oct 2026</sub>

**PostgreSQL extension for vector similarity search with HNSW and IVFFlat.**

pgvector is a PostgreSQL extension (Postgres 13+) that adds vector, halfvec, bit and sparsevec column types with L2, inner product, cosine, L1, Hamming and Jaccard distance operators, exact search by default and HNSW or IVFFlat indexes for approximate search. Vectors sit beside ordinary rows with ACID, joins and backups, and Postgres full-text search can be combined for hybrid retrieval. It installs via make, Docker or OS packages.

- **+** Vectors live next to relational data with ACID, joins and point-in-time recovery
- **+** HNSW and IVFFlat indexes with six distance operators
- **+** Half-precision, binary and sparse vector types plus binary quantization
- **+** Installs via make, Docker, Homebrew, APT, Yum; preinstalled on many hosted Postgres
- **−** vector type capped at 2,000 dimensions (halfvec 4,000)
- **−** Approximate indexes filter after scanning; filtered recall needs iterative scan tuning
- **−** HNSW builds slow down sharply once the graph exceeds maintenance_work_mem
- **−** No server of its own; capacity depends on your Postgres tuning

<sub>no GPU · Docker · Needs PostgreSQL 13+ · Models: any embedding model; stores precomputed vectors · [Repo](https://github.com/pgvector/pgvector)</sub>

### [Weaviate](https://github.com/weaviate/weaviate) <sub>★ 16.9k · NOASSERTION · Oct 2026</sub>

**Go vector database with built-in vectorizers, hybrid search and RAG.**

Weaviate is a Go vector database that stores objects with their vectors and serves hybrid BM25 plus semantic search, filtering, built-in RAG and reranking through REST, gRPC and GraphQL APIs. It can vectorize data at import using modules for OpenAI, Cohere, HuggingFace, Google or a local model2vec image, or accept precomputed vectors. Docker Compose runs it on ports 8080 and 50051; production adds multi-tenancy, replication and RBAC.

- **+** Vectorizes at import with OpenAI, Cohere, HuggingFace, Google or a local model2vec container
- **+** Hybrid BM25 plus vector, image search, filtering, RAG and reranking in one query
- **+** Multi-tenancy, replication, RBAC, horizontal scaling and vector compression
- **+** REST, gRPC and GraphQL with Python, TypeScript, Java, Go and C# clients
- **−** Enterprise features in wl/ need a commercial license key; one image mixes both
- **−** Vectorization needs a module container or external API keys
- **−** No RAM or sizing guidance in the README
- **−** Both REST 8080 and gRPC 50051 must be exposed

<sub>no GPU · Docker + Compose · Needs optional embedding inference container (e.g. model2vec) or external embedding APIs · Models: OpenAI, Cohere, HuggingFace, Google and other integrated model providers, local model2vec (minishlab/potion-base-32M), precomputed vectors · port 8080 · [Repo](https://github.com/weaviate/weaviate) · [Demo](https://elysia.weaviate.io) · [Docs](https://docs.weaviate.io)</sub>

### [Vespa](https://github.com/vespa-engine/vespa) <sub>★ 7.1k · Apache-2.0 · Oct 2026</sub>

**Serving engine for vectors, tensors, text and ML ranking at scale.**

Vespa is a serving platform that indexes vectors, tensors, text and structured data, selects a subset at query time, evaluates machine-learned ranking models over it and returns results in under 100 ms while the corpus changes, across many nodes. The Java and C++ engine builds from this repo with a release every morning Monday to Thursday. Getting started and self-hosting live in docs.vespa.ai; Vespa Cloud is the hosted option.

- **+** Vectors, tensors, text and structured data queried and ranked together
- **+** Machine-learned ranking models evaluated at serving time
- **+** Runs hundreds of thousands of queries per second on large internet services
- **+** Sample applications repo plus detailed docs
- **−** README covers building, not running; install details live in docs
- **−** Heavy platform (Java and C++ engine) sized for multi-node clusters
- **−** C++ builds require AlmaLinux 8; Java needs JDK 17 and Maven
- **−** A new release every weekday morning Monday to Thursday; versions churn

<sub>no GPU · Models: machine-learned ranking models evaluated in Vespa · [Repo](https://github.com/vespa-engine/vespa) · [Docs](https://docs.vespa.ai) · [Site](https://vespa.ai)</sub>

### [HelixDB](https://github.com/HelixDB/helix-db) <sub>★ 6.1k · Apache-2.0 · Oct 2026</sub>

**Rust graph database with native vector and BM25 search.**

HelixDB is a Rust database that combines a labeled property graph, approximate nearest-neighbor vector search and BM25 full-text search in one transactional engine. A CLI starts a local instance in Docker or Podman on port 6969 (in-memory by default, --disk to persist) or the engine runs embedded, and Rust, TypeScript, Python and Go SDKs send the same JSON queries to POST /v2/query.

- **+** Graph traversal, vector ANN and BM25 in one transactional engine
- **+** Vector search prefiltered by graph traversal
- **+** SDKs for Rust, TypeScript, Python and Go sending the same JSON query
- **+** Embedded mode runs inside your process without a server
- **−** Local data is in-memory unless started with --disk
- **−** Python and Go SDKs are 0.x while Rust and TypeScript are 3.x
- **−** Cypher support only in source builds
- **−** Install is a curl piped to bash script

<sub>no GPU · Docker · Needs Docker or Podman for the local instance · Models: any embedding model; stores precomputed vectors · port 6969 · [Repo](https://github.com/HelixDB/helix-db) · [Docs](https://docs.helix-db.com) · [Site](https://helix-db.com)</sub>

### [Marqo](https://github.com/marqo-ai/marqo) <sub>★ 5.0k · Apache-2.0 · Apr 2026</sub>

**Vector search engine with built-in embedding, now deprecated upstream.**

Marqo was a vector search engine that generated embeddings and stored them in one service, so you indexed raw text or images and queried in natural language. Its README now states the open-source project is deprecated and will receive no updates, pointing to the commercial Marqo ecommerce search platform instead. The Apache-2.0 code and docs remain available.

- **+** Apache-2.0 code remains available for forks
- **+** Docs at docs.marqo.ai still describe the API
- **−** Open-source project declared deprecated; no further updates
- **−** README no longer documents installation, API or supported models
- **−** Last commit 2026-04-10
- **−** Only the commercial platform is maintained

<sub>Compose · [Repo](https://github.com/marqo-ai/marqo) · [Docs](https://docs.marqo.ai) · [Site](https://www.marqo.ai)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Sandboxes

Isolated runtimes where agents execute code, browse or use tools safely. <sub>8 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Isolation level (container, microVM, gVisor) sets the risk you accept when agents run code.
- Check startup time per sandbox; slow starts limit agent loops.
- Look at what is persisted between runs and how secrets are injected.

</details>

### [Lightpanda](https://github.com/lightpanda-io/browser) <sub>★ 36.1k · AGPL-3.0 · Oct 2026</sub>

**Headless browser in Zig with CDP, MCP and an agent mode.**

Browser engine written in Zig (V8, libcurl, html5ever) with no graphical renderer. Exposes a CDP server on port 9222 for Puppeteer and Playwright plus WebDriver BiDi, a fetch command that dumps HTML, markdown, PNG or PDF, an MCP server over stdio or HTTP with per-client sessions, and an agent mode driven by Anthropic, OpenAI, Gemini, Ollama, llama.cpp or any OpenAI-compatible endpoint. For scraping and agent fleets where Chrome is too heavy.

- **+** 100 pages: 123 MB and 5 s versus 2 GB and 46 s for Chrome
- **+** CDP and WebDriver BiDi servers work with existing Puppeteer and Playwright scripts
- **+** Agent mode records deterministic PandaScript JS you can replay without an LLM
- **+** MCP over HTTP isolates each client in its own browsing session
- **−** No graphical rendering engine; PNG and PDF dumps are text-only renderings
- **−** Nightly builds only via Homebrew, AUR and GitHub releases; no native Windows binary
- **−** Usage telemetry on by default; set LIGHTPANDA_DISABLE_TELEMETRY=true
- **−** AGPL-3.0 license and a CLA for contributions

<sub>no GPU · Docker · Models: Anthropic, OpenAI, Gemini, Google Vertex AI, Mistral · port 9222 · [Repo](https://github.com/lightpanda-io/browser) · [Docs](https://lightpanda.io/docs/usage/agent) · [Site](https://lightpanda.io)</sub>

### [Obscura](https://github.com/h4ckf0r0day/obscura) <sub>★ 28.7k · Apache-2.0 · Oct 2026</sub>

**Rust headless browser with CDP, native rendering and stealth mode.**

Headless browser engine in Rust running V8 that speaks the Chrome DevTools Protocol, so Puppeteer and Playwright connect on port 9222 as if to Chrome. Ships its own layout and paint engine for screenshots, screencasts and PDF export, a stealth build with per-session fingerprint randomization, a parallel scrape command and an MCP server. Claims 30 MB memory and 85 ms page loads against 200+ MB and about 500 ms for Chrome.

- **+** Single binary around 70 MiB, no Chrome or Node.js; distroless Docker image about 57 MB
- **+** Stealth build randomizes fingerprints per session and blocks 3,520 tracker domains
- **+** SSRF protection blocks private IPs by default; CDP token on the Docker image
- **+** Fetch.takeResponseBodyAsStream and IO.read stream large downloads in chunks
- **−** Independent rendering engine; long-tail CSS, media playback and fonts can differ from Chromium
- **−** Stealth builds need CMake, Clang and libclang; first source build takes about 5 minutes
- **−** README carries heavy proxy-vendor sponsorship and discount codes
- **−** Linux binaries target glibc 2.35 or newer (Ubuntu 22.04)

<sub>no GPU · Docker · port 9222 · [Repo](https://github.com/h4ckf0r0day/obscura) · [Docs](https://docs.obscura.sh) · [Site](https://obscura.sh)</sub>

### [NemoClaw](https://github.com/NVIDIA/NemoClaw) <sub>★ 22.7k · Apache-2.0 · Oct 2026</sub>

**NVIDIA reference stack running OpenClaw and Hermes inside OpenShell sandboxes.**

CLI and installer that provision OpenShell sandboxes for OpenClaw (default), Hermes or LangChain Deep Agents Code, with guided onboarding, inference provider selection, baseline network policies with operator approval, managed integrations and persistent sandbox state. Express install targets DGX hosts and Windows WSL; a starter prompt lets Cursor, Claude Code or Codex drive setup. For personal agents with kernel-enforced isolation.

- **+** Three supported agents: OpenClaw, Hermes, LangChain Deep Agents Code
- **+** Network policy with operator approval flow and egress control from OpenShell
- **+** Express preset install on DGX and WSL hosts
- **+** Documented sandbox hardening: capability drops and process limits
- **−** Alpha project; maintainers review issues without guaranteed response times
- **−** Depends on OpenShell as the runtime; details live in NVIDIA docs, not the README
- **−** README is mostly links; no architecture or resource figures in the repo itself
- **−** Supported platforms are limited to those on the prerequisites page

<sub>no GPU · Docker · Needs NVIDIA OpenShell, Inference provider (local or routed) · Models: providers configured through OpenShell routed inference · [Repo](https://github.com/NVIDIA/NemoClaw) · [Docs](https://docs.nvidia.com/nemoclaw/latest/)</sub>

### [Browser Use Web UI](https://github.com/browser-use/web-ui) <sub>★ 16.6k · MIT · May 2026</sub>

**Gradio UI for running browser-use agents with your own Chrome.**

Gradio front end over the browser-use library that takes a task, drives a Playwright browser with an LLM (Google, OpenAI, Azure OpenAI, Anthropic, DeepSeek or Ollama) and shows the run. Can attach to your own Chrome profile to reuse logins, keep the browser open between tasks and record video. Runs with uv and Python 3.11 on port 7788, or via docker compose with a noVNC viewer on port 6080.

- **+** Own-browser mode reuses existing Chrome logins and cookies
- **+** Docker compose includes noVNC so you can watch the agent at localhost:6080
- **+** Persistent browser sessions keep history visible between tasks
- **+** Supports Ollama and DeepSeek-R1 alongside cloud providers
- **−** Changelog stops in January 2025; last commit May 2026
- **−** Default VNC password is published in the README; change VNC_PASSWORD
- **−** Own-browser mode requires closing all Chrome windows and using another browser for the UI
- **−** Gradio single-user UI; no auth or multi-user features described

<sub>no GPU · Docker + Compose · Needs Playwright browsers, LLM API key or Ollama, Chrome (optional, own-browser mode) · Models: Google, OpenAI, Azure OpenAI, Anthropic, DeepSeek · port 7788 · [Repo](https://github.com/browser-use/web-ui) · [Docs](https://docs.browser-use.com)</sub>

### [OpenShell](https://github.com/NVIDIA/OpenShell) <sub>★ 15.4k · Apache-2.0 · Oct 2026</sub>

**Policy-enforced sandbox runtime for autonomous agents with credential brokering.**

Runs each agent in a sandbox with kernel-enforced limits on file access and system calls; every outbound connection passes a policy check, and agents never see real credentials, which a gateway injects only for approved endpoints. Policy changes are checked with formal verification before approval. Installs via a shell script on Linux, Apple Silicon macOS or WSL 2; Helm for Kubernetes; SDKs for Python, TypeScript, Go and Rust.

- **+** Credentials attached by the gateway only to approved endpoints; sandboxes never hold them
- **+** Formal verification flags risky new access before a policy change is applied
- **+** Kubernetes deployment via Helm; GPU use inside sandboxes documented
- **+** Python, TypeScript, Go and Rust SDKs plus agent skills via npx skills add
- **−** Windows support is WSL 2 only and experimental
- **−** Default sandbox image is minimal Ubuntu with no agent; running one follows the docs walkthrough
- **−** Anonymous telemetry on by default; disable with OPENSHELL_TELEMETRY_ENABLED=false
- **−** Kubernetes installs require a CNI that enforces NetworkPolicy

<sub>no GPU · Needs Docker, Podman or host virtualization · Models: any provider via routed inference credentials · [Repo](https://github.com/NVIDIA/OpenShell) · [Docs](https://docs.nvidia.com/openshell/latest/index.html)</sub>

### [microsandbox](https://github.com/superradcompany/microsandbox) <sub>★ 8.6k · Apache-2.0 · Oct 2026</sub>

**Local microVMs for untrusted code with fork, snapshot and SDKs.**

Boots OCI images as hardware-isolated microVMs in under 100 ms on Linux with KVM, Apple Silicon macOS or Windows with WHP, driven by the msb CLI or embedded via TypeScript, Rust, Python, Go and Ruby SDKs with no daemon. Running sandboxes fork live or snapshot and restore; network access is allow-listed per host and secrets are injected only toward an allowed host. For agent-generated code, CI jobs and plugins.

- **+** Sub-100 ms average boot; sandboxes spawn as child processes of your app
- **+** Live fork and full snapshot restore with copy-on-write memory
- **+** Per-sandbox network allow-lists and secrets scoped to one host
- **+** MCP server and agent skills let coding agents create their own sandboxes
- **−** Beta software; breaking changes and missing features expected
- **−** Needs KVM on Linux, Apple Silicon on macOS or WHP on Windows; no Intel Mac
- **−** No Dockerfile or compose file; it replaces containers rather than running in one
- **−** Image pulls on first create add startup time

<sub>no GPU · Needs KVM (Linux), Apple Silicon (macOS) or WHP (Windows) · [Repo](https://github.com/superradcompany/microsandbox) · [Docs](https://docs.microsandbox.dev/cli/overview)</sub>

### [Steel Browser](https://github.com/steel-dev/steel-browser) <sub>★ 7.8k · Apache-2.0 · Oct 2026</sub>

**Browser API that manages Chrome sessions for Puppeteer, Playwright and Selenium.**

REST API and UI on port 3000 that launches Chrome sessions with persisted cookies and storage, proxy chains, stealth plugins and request logging, then hands you a CDP endpoint for Puppeteer or Playwright or a WebDriver endpoint for Selenium. Quick-action endpoints return a page as HTML, markdown, screenshot or PDF. Runs from a prebuilt ghcr.io image or docker compose; Node and Python SDKs target cloud or self-hosted instances.

- **+** One image serves API, UI and console debugger (ports 3000 and 9223)
- **+** Session API persists cookies and storage; Selenium sessions via isSelenium
- **+** Swagger UI at /documentation on the local instance
- **+** Node and Python SDKs switch between cloud and self-host with baseURL
- **−** Public beta; API still changing
- **−** Runs full Chrome; needs a Chrome executable when run outside Docker
- **−** Selenium integration lacks some features of the CDP session API
- **−** Apple Silicon compose needs DOCKER_DEFAULT_PLATFORM=linux/arm64

<sub>no GPU · Docker + Compose · Needs Google Chrome (non-Docker runs), Node.js (non-Docker runs) · port 3000 · [Repo](https://github.com/steel-dev/steel-browser) · [Docs](https://docs.steel.dev/) · [Site](https://steel.dev)</sub>

### [Open Terminal](https://github.com/open-webui/open-terminal) <sub>★ 3.3k · MIT · Sep 2026</sub>

**REST-driven shell and file sandbox for AI agents, from Open WebUI.**

Container or pip package exposing a shell and file management over a REST API with an API key on port 8000, so agents can run commands and code. The latest image (about 4 GB) bundles Python, Node.js, gcc, ffmpeg, LibreOffice, LaTeX and the Docker CLI behind an egress firewall; slim (430 MB) and alpine (230 MB) variants keep git, curl and jq. Integrates with Open WebUI as a terminal with a file sidebar.

- **+** API key auto-generated if unset; interactive API docs at /docs
- **+** Extra apt, pip and npm packages installed at startup via env vars
- **+** Four image variants from 230 MB alpine to a 4 GB full toolkit
- **+** Office previews: DOCX and PPTX rendered to PDF when LibreOffice is present
- **−** Multi-user mode shares one container and is explicitly not a security boundary
- **−** Per-user isolation requires Terminals, which needs an Open WebUI Enterprise license
- **−** Mounting the Docker socket gives the container root-equivalent host access
- **−** Bare-metal mode runs commands directly as your user with no sandbox

<sub>no GPU · Docker · port 8000 · [Repo](https://github.com/open-webui/open-terminal)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## How entries are written

Each entry is written from the project README and facts checked against GitHub (stars, last commit, license, Docker files), in plain language, with strengths and weaknesses stated as checkable claims. Specs say `unknown` rather than guess. Entries are rewritten when the README or the latest release changes, and projects that go quiet for 12 months are marked stale; archived projects are removed.

Within a category, projects are ordered by stars for now. A score that weighs maintenance, deployability and verified builds is in progress and will replace it.

## Sources

Candidates come from these lists and app stores (facts and links only, no text copied), plus community submissions: [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) · [awesome-local-llm](https://github.com/rafska/awesome-local-llm) · [compose-examples](https://github.com/Haxxnet/Compose-Examples) · [awesome-homelab](https://github.com/AwesomeHomelab/awesome-homelab) · [self-hosting-guide](https://github.com/mikeroyal/Self-Hosting-Guide) · [awesome-ai-agent-platforms](https://github.com/Agenta-AI/awesome-ai-agent-platforms) · [awesome-openclaw](https://github.com/alvinreal/awesome-openclaw) · [umbrel-apps](https://github.com/getumbrel/umbrel-apps) · [runtipi-appstore](https://github.com/runtipi/runtipi-appstore) · [casaos-appstore](https://github.com/IceWhaleTech/CasaOS-AppStore) · [dokploy-templates](https://templates.dokploy.com/meta.json) · [awesome-opensource-ai](https://github.com/alvinreal/awesome-opensource-ai) · [awesome-llm-services](https://github.com/av/awesome-llm-services) · [awesome-llmops](https://github.com/tensorchord/Awesome-LLMOps) · [awesome-private-ai](https://github.com/tdi/awesome-private-ai) · [awesome-local-llms](https://github.com/vince-lam/awesome-local-llms) · [awesome-llm-webapps](https://github.com/icefort-ai/awesome-llm-webapps).

## Submit, fix or opt out

Open an issue in [archestack/best-of-selfhosted-ai](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose) to add a project, report wrong data, or ask for removal (honored within 24 hours). The README and `data/` are generated; please do not edit them by hand.

## License

Data (`data/`, this README) is CC BY 4.0; see LICENSE-DATA. Code is MIT; see LICENSE. Project names and descriptions belong to their owners.
