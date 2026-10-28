# 🖥️ Desktop AI apps reviews · Best of Open-Source AI

Apps you install on your own computer to chat with local or API models, often with document chat and agents built in. Back to the [leaderboard](../README.md#%EF%B8%8F-desktop-ai-apps).

<sub>🌐 Also on the web: [Desktop AI apps on archestack.com](https://archestack.com/best-of-ai/desktop-apps/), each project on its own page.</sub>

<a name="cherry-studio"></a>
### 🥇 [cherry-studio](https://github.com/cherryhq/cherry-studio) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · AGPL-3.0 · Oct 2026</sub>

**Desktop client for chatting with many LLM providers, with agents and knowledge bases.**

Cherry Studio is an Electron-style desktop app for Windows, macOS and Linux that connects to cloud providers (OpenAI, Anthropic, Gemini, custom compatible endpoints) and local models via Ollama and LM Studio. It adds agents with tool permissions, Skills and MCP servers, local knowledge bases, image generation, translation and an API Gateway. Conversation history and knowledge bases stay on the device, with local and WebDAV backup.

- **+** Supports many cloud providers plus Ollama and LM Studio in one app
- **+** Agents can use files, commands, browser automation, Skills and MCP servers
- **+** Local knowledge bases from files, folders and web pages, with OCR options
- **+** Runs on Windows, macOS and Linux; mobile apps exist for iOS and Android
- **−** AGPL-3.0; a commercial license is needed to avoid AGPL terms
- **−** Centralized management and access controls are in the separate Enterprise Edition
- **−** Many features need API keys, downloaded models or extra dependencies
- **−** Community themes written for v1 need adaptation for the v2 interface

<sub>GPU optional · Needs Ollama (optional), LM Studio (optional), Provider API keys (for cloud models) · Models: OpenAI, Anthropic, Gemini, Ollama, LM Studio · [Repo](https://github.com/cherryhq/cherry-studio) · [📖 Docs ↗](https://cherryai.com/docs/en/) · [🌐 Site ↗](https://cherryai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cherry-studio/)</sub>

<a name="screenpipe"></a>
### 🥈 [screenpipe](https://github.com/screenpipe/screenpipe) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · custom license · Oct 2026</sub>

**Records screen and audio locally, makes it searchable for you and your agents.**

Screenpipe captures screen content (accessibility tree, with OCR as fallback), system audio and microphone with local Whisper transcription, and stores it in a local SQLite database. It exposes a localhost REST API on port 3030, an MCP server, and pipes, which are scheduled agents defined in markdown that query this history. Newer versions also target teams, with central config and per-pipe data permissions.

- **+** Event-driven capture uses the accessibility tree first, OCR only as fallback
- **+** Local REST API on port 3030, raw SQLite access and an MCP server
- **+** Pipes are markdown files with per-pipe app, window and endpoint permissions
- **+** Runs on macOS, Windows and Linux; works with local models such as Ollama
- **−** Source-available license: commercial use requires a paid commercial license
- **−** Continuous capture of everything on screen raises privacy and compliance concerns
- **−** Capture alone takes about 5-20% CPU and 0.5-3 GB RAM; storage use is unspecified
- **−** Some features depend on paid plans; Linux capture varies by desktop environment

<sub>RAM ≥ 8 GB · GPU optional · Needs Node.js (npx CLI), Ollama (optional local LLM), Deepgram (optional cloud transcription) · Models: Whisper Large-V3-Turbo, Deepgram, Ollama, OpenAI-compatible servers · port 3030 · README: alternative to Otter.ai, Granola · [Repo](https://github.com/screenpipe/screenpipe) · [📖 Docs ↗](https://docs.screenpi.pe) · [🌐 Site ↗](https://screenpi.pe) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/screenpipe/)</sub>

<a name="deep-live-cam"></a>
### 🥉 [deep-live-cam](https://github.com/hacksider/deep-live-cam) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 97k · AGPL-3.0 · Oct 2026</sub>

**Real-time webcam face swap and video deepfake from a single source image.**

Python desktop app (Tkinter GUI, with a CLI) that swaps a face from one source image onto a live webcam feed, a video or an image, using ONNX models (inswapper_128_fp16, gfpgan-1024). It offers mouth masking, multi-face mapping, and execution providers for CUDA, CoreML, DirectML, OpenVINO and CPU. A pre-built edition with extra features is offered separately on the project website.

- **+** Live webcam mode needs only one source image; output can be streamed via OBS
- **+** Mouth Mask and face mapping handle multiple subjects with different faces
- **+** Execution providers for CUDA, CoreML, DirectML, OpenVINO and CPU
- **+** Also processes images and video files, with keep-fps and keep-audio options
- **−** Manual install is technical: Python, ffmpeg, CUDA 12.8 and cuDNN 8.9.7 for NVIDIA
- **−** CPU-only runs are slower; live preview takes 10-30 seconds to appear
- **−** Command-line arguments section is labeled unmaintained
- **−** Depends on insightface models, which are non-commercial research only

<sub>GPU optional · Needs Python 3.11-3.14, ffmpeg, onnxruntime, gfpgan-1024.onnx, inswapper_128_fp16.onnx, CUDA 12.8 (NVIDIA) · Models: ONNX, inswapper_128_fp16, GFPGAN · [Repo](https://github.com/hacksider/deep-live-cam) · [📖 Docs ↗](https://deeplivecam.net/index.php/quickstart) · [🌐 Site ↗](https://deeplivecam.net) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deep-live-cam/)</sub>

<a name="dsh-desktop"></a>
### #&#8288;4 [dsh-desktop](https://github.com/anywhere-labs/dsh-desktop) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Oct 2026</sub>

**Native Windows and macOS desktop client for DeepSeek Harness, built on plugins.**

Wraps the pinned upstream DeepSeek Harness local Web UI, host service and plugin system in a desktop app with window, tray, terminal, auto-update and work profiles. The desktop shell is itself a DSH plugin. It includes a plugin market and phone remote control (2.0.9 and later). Installers cover Windows x64 and macOS Universal, and no Node.js install is needed.

- **+** Installers for Windows x64 and macOS Universal; the app starts and manages the local Harness service
- **+** Runs a pinned, unmodified upstream version, with desktop features added as plugins
- **+** Built-in plugin market and iOS/Android remote control from 2.0.9
- **+** Web service listens on loopback only by default
- **−** No Linux build listed
- **−** Optional LAN access has no authentication; anyone on the network can operate the machine
- **−** Independent community project, not affiliated with DeepSeek; tied to the pinned upstream version
- **−** Update checks send version, channel and a persistent random installation ID

<sub>Needs DeepSeek Harness (bundled, pinned) · Models: unknown · [Repo](https://github.com/anywhere-labs/dsh-desktop) · [📖 Docs ↗](https://github.com/anywhere-labs/dsh-desktop/blob/main/docs/user-guide.md) · [🌐 Site ↗](https://dshdesktop.cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dsh-desktop/)</sub>

<a name="prompt-optimizer"></a>
### #&#8288;5 [prompt-optimizer](https://github.com/linshenkx/prompt-optimizer) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · custom license · Oct 2026</sub>

**Prompt rewriting and testing tool for web, desktop, Chrome and MCP.**

Prompt Optimizer rewrites system and user prompts with an LLM you configure, then lets you test, compare and save the results as versioned favorites. It runs as a browser app, desktop app, Chrome extension or Docker container, and exposes an MCP server at /mcp with optimize-user-prompt, optimize-system-prompt and iterate-prompt tools. Model calls go straight from the client to the provider, including text-to-image and image-to-image modes.

- **+** Ships as web app, desktop app, Chrome extension and Docker image
- **+** Built-in MCP server at /mcp for Claude Desktop and other MCP clients
- **+** Analysis and compare evaluation, variables, multi-turn and function-calling tests
- **+** Client-side processing; requests go directly to the configured provider
- **−** Web version may hit browser CORS limits with local endpoints such as Ollama
- **−** VITE_* API keys are exposed in browser assets on public deployments
- **−** Chrome Web Store version can lag behind the latest release
- **−** Workspace/project management is still unchecked on the roadmap

<sub>no GPU · Docker + Compose · Needs LLM provider API key or compatible endpoint · Models: OpenAI, Gemini, DeepSeek, Grok, Zhipu AI · port 8081 · [Repo](https://github.com/linshenkx/prompt-optimizer) · [▶️ Demo ↗](https://prompt.always200.com) · [📖 Docs ↗](https://docs.always200.com) · [🌐 Site ↗](https://always200.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/prompt-optimizer/)</sub>

<a name="aionui"></a>
### #&#8288;6 [aionui](https://github.com/iofficeai/aionui) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Oct 2026</sub>

**Desktop and WebUI app that runs a built-in agent plus external CLI agents.**

AionUi is a TypeScript desktop app for macOS, Windows and Linux. It bundles an agent engine (aionrs) that reads and writes files, searches the web and calls MCP tools using any of 30+ API providers or local Ollama and LM Studio. It also detects installed CLI agents such as Claude Code, Codex and Qwen Code, runs them in parallel sessions, and is reachable through a WebUI or chat bots, with scheduled tasks.

- **+** Auto-detects installed CLI agents (Claude Code, Codex, Qwen Code and others) in one interface
- **+** Built-in agent works after pasting an API key, with no separate CLI install
- **+** Scheduled tasks support cron with timezone, fixed intervals and one-time triggers
- **+** Remote access via browser WebUI or Telegram, Lark, DingTalk and WeChat bots
- **−** Local models are reached through a custom API endpoint, not a bundled runtime
- **−** Slack, Discord and WeCom channels are listed as coming soon
- **−** Unattended YOLO mode and permissions vary by selected agent
- **−** README excerpt gives no RAM, port or hardware requirements

<sub>no GPU · Docker · Needs Optional CLI agents (Claude Code, Codex, etc.), LLM API key or local Ollama/LM Studio · Models: Gemini, OpenAI, Anthropic, AWS Bedrock, Ollama · [Repo](https://github.com/iofficeai/aionui) · [🌐 Site ↗](https://www.aionui.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aionui/)</sub>

<a name="jan"></a>
### #&#8288;7 [jan](https://github.com/janhq/jan) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 45k · custom license · Oct 2026</sub>

**Desktop app that runs local models or cloud APIs, with a local server.**

Jan is a Tauri desktop app for Windows, macOS and Linux that downloads LLMs from Hugging Face and runs them through a bundled llama.cpp engine. It can also connect to cloud providers such as OpenAI, Anthropic, Mistral and Groq. It exposes an OpenAI-compatible API at localhost:1337 and supports MCP for agent tools.

- **+** Runs local models and cloud providers from one app
- **+** OpenAI-compatible local server at localhost:1337 for other applications
- **+** MCP integration for agentic tool use
- **+** Engine variants for CPU, Vulkan, Metal, CUDA and ROCm builds
- **−** Desktop only; no Docker image or multi-user web deployment
- **−** README says Apache 2.0, but license detection reports NOASSERTION
- **−** Source build needs Node, Yarn, Rust; Windows also needs LLVM, Ninja, CMake
- **−** Linux Arm64 is a linked how-to, not a packaged download

<sub>RAM ≥ 8 GB · GPU optional · Models: GGUF via llama.cpp, Hugging Face models, OpenAI, Anthropic, Mistral · port 1337 · [Repo](https://github.com/janhq/jan) · [📖 Docs ↗](https://jan.ai/docs) · [🌐 Site ↗](https://jan.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jan/)</sub>

<a name="hermes-desktop"></a>
### #&#8288;8 [hermes-desktop](https://github.com/fathah/hermes-desktop) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

**Desktop GUI for installing and chatting with Hermes Agent.**

Community-maintained desktop app that installs Hermes Agent into ~/.hermes with the official script, then provides a GUI for chat, sessions, profiles, memory, skills, toolsets, cron schedules and messaging gateways. It can run Hermes locally on 127.0.0.1:8642 or connect to a remote Hermes API server with a URL and key. Not affiliated with Nous Research.

- **+** Guided first-run install resolves Git, uv and Python 3.11+ for the Hermes backend
- **+** Local or remote Hermes backend, with presets for Ollama, LM Studio, vLLM and llama.cpp
- **+** 16 messaging gateways and cron scheduling with delivery targets configurable in the UI
- **+** Optional command-based secrets provider for pass, 1Password, Bitwarden and similar helpers
- **−** Depends on upstream Hermes Agent for all agent behavior and tool execution
- **−** Windows installer is unsigned; Fedora RPM is not GPG-signed and has no auto-update
- **−** README says the project is in active development and some things may break
- **−** Command secrets provider is POSIX-only; Windows stays on plaintext .env keys

<sub>GPU optional · Needs Hermes Agent, Git, uv, Python 3.11+ · Models: OpenRouter, Anthropic, OpenAI, Google Gemini, xAI Grok · port 8642 · [Repo](https://github.com/fathah/hermes-desktop) · [🌐 Site ↗](https://hermesone.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hermes-desktop/)</sub>

<a name="chatbox"></a>
### #&#8288;9 [chatbox](https://github.com/chatboxai/chatbox) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · GPL-3.0 · Sep 2026</sub>

**Desktop and mobile chat client for OpenAI, Claude, Gemini and Ollama models.**

Chatbox is an Electron app (TypeScript, React) that connects to hosted LLM APIs and local models through Ollama. Chat data is stored on the device. It ships installers for Windows, macOS and Linux, plus iOS and Android apps and a web version.

- **+** Installers for Windows, macOS, Linux (AppImage), plus iOS, Android and a web version
- **+** Supports OpenAI, Azure OpenAI, Claude, Gemini, Ollama and ChatGLM-6B from one client
- **+** Chat data stays on the device; no server deployment needed
- **+** Prompt library, Markdown, LaTeX and code highlighting, DALL-E-3 image generation
- **−** README lists no document chat, RAG or agent features
- **−** Community Edition is synced with a separate pro repo; feature parity is unclear
- **−** Provider list in README is dated (llama2, ChatGLM-6B); current coverage is unclear
- **−** GPL-3.0 license may restrict embedding in proprietary products

<sub>no GPU · Needs Ollama (optional, for local models), API keys for hosted providers · Models: OpenAI, Azure OpenAI, Claude, Google Gemini Pro, Ollama · [Repo](https://github.com/chatboxai/chatbox) · [🌐 Site ↗](https://chatboxai.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatbox/)</sub>

<a name="openworker"></a>
### #&#8288;10 [openworker](https://github.com/andrewyng/openworker) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

**Desktop AI coworker for approval-gated work across files, terminal and apps.**

OpenWorker is a macOS and Windows desktop app backed by a local Python agent server built on aisuite. It works across local files, a terminal and 25+ connectors such as GitHub, Slack, Jira and Gmail, plus any MCP tool, and asks for approval before writes, sends or shell commands. Security-review coworkers ship first, and commands can run in an NVIDIA OpenShell, macOS or Windows sandbox.

- **+** Approval gating with hard floors, standing rules and a per-tool-call audit trail
- **+** Optional sandboxing: NVIDIA OpenShell, built-in macOS sandbox, or Windows local account
- **+** Works with OpenAI, Anthropic, Gemini, DeepSeek, Qwen, Together, Fireworks or local Ollama
- **+** 25+ connectors plus MCP, scheduled automations, and Slack mentions that open desktop sessions
- **−** Open beta; README says rough edges remain
- **−** Windows builds are not code-signed, so SmartScreen warns
- **−** Prebuilt installers cover only Apple Silicon macOS and Windows x64; Linux not mentioned
- **−** Connector OAuth goes through a cloud broker; manual keys avoid it

<sub>no GPU · Needs Python 3.10+ (source), Node 20+ (source), Rust toolchain (desktop build from source), Ollama (optional), NVIDIA OpenShell (optional) · Models: OpenAI, Anthropic, Google Gemini, DeepSeek, Qwen · port 8765 · [Repo](https://github.com/andrewyng/openworker) · [🌐 Site ↗](https://openworker.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openworker/)</sub>

<a name="eigent"></a>
### #&#8288;11 [eigent](https://github.com/eigent-ai/eigent) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

**Desktop app running single agents or parallel multi-agent teams on your machine.**

Eigent is an Electron and React desktop app with a FastAPI backend that runs AI agents on your computer, either as one agent or as a CAMEL-based workforce of specialized agents working in parallel. Agents get built-in browser, terminal and document toolkits, plus MCP and skill integration, and workflows can be scheduled. It works with cloud APIs, gateways or local inference such as vLLM, Ollama and LM Studio.

- **+** Single-agent mode and multi-agent workforce mode in one desktop workspace
- **+** Built-in browser, terminal and document toolkits, with MCP and skill integration
- **+** Local backend supports vLLM, Ollama and LM Studio, with no cloud account required
- **+** Recurring workflows can be scheduled to run while you are away
- **−** Quick start connects to Eigent cloud services and requires account registration
- **−** Local deployment is a separate server setup documented in another README
- **−** SSO and access control are enterprise-only features, via sales contact
- **−** No Docker or compose files detected; running from source needs Node 18-22 and uv

<sub>GPU optional · Needs Node.js 18-22, npm, uv · Models: vLLM, Ollama, LM Studio, cloud APIs, enterprise gateways · [Repo](https://github.com/eigent-ai/eigent) · [📖 Docs ↗](https://docs.eigent.ai) · [🌐 Site ↗](https://www.eigent.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/eigent/)</sub>

<a name="holaos"></a>
### #&#8288;12 [holaos](https://github.com/holaboss-ai/holaos) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (41) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Aug 2026</sub>

**Electron desktop workspace that runs agents beside live apps, with local memory.**

holaOS is an Electron desktop app where agents (Claude Code, Codex, or a built-in holaOS agent) run next to interactive apps such as Notion or a browser. It connects Slack, Feishu, DingTalk and WeChat, 50+ OAuth integrations and MCP servers, and keeps memory as plain local files. Models are either built in through a holaOS account or supplied with your own OpenAI/Anthropic-compatible keys.

- **+** Runs Claude Code, Codex and its own agent over shared memory, skills and tools
- **+** Memory, embeddings and session history stored locally as readable, editable files
- **+** Supports MCP servers, 50+ OAuth integrations and bring-your-own-key providers
- **+** Runs on macOS (Apple Silicon and Intel), Windows and Linux
- **−** Modified Apache 2.0 license with commercial-distribution and branding conditions
- **−** Built-in models and marketplace tie into a holaOS account; sign-in required for those
- **−** Source install needs Node 24.14.1 and an Electron dev build; no Docker or compose
- **−** SSO, per-role permissions and audit logs are in the Enterprise tier

<sub>no GPU · Needs Node.js 24.14.1, npm, git, Electron · Models: Kimi K3, GLM 5.2, GPT 5.6, Claude Opus 5, OpenAI-compatible endpoints · [Repo](https://github.com/holaboss-ai/holaos) · [📖 Docs ↗](https://www.holaos.ai/docs/getting-started) · [🌐 Site ↗](https://www.holaos.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/holaos/)</sub>

<a name="presenton"></a>
### #&#8288;13 [presenton](https://github.com/presenton/presenton) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**Generates editable PPTX and PDF slide decks from prompts or documents.**

Presenton is a self-hosted presentation generator that builds slides from a prompt, an uploaded document, or a PowerPoint-derived template, and exports editable PPTX or PDF. It runs as a Docker web app or an Electron desktop app, exposes a generation API and a built-in MCP server, and connects to OpenAI, Anthropic, Gemini, Ollama, LM Studio, Bedrock and other providers.

- **+** Exports fully editable PPTX as well as PDF
- **+** Many text LLM providers, including local Ollama and LM Studio, plus any OpenAI-compatible endpoint
- **+** Includes a generation API, a built-in MCP server and multi-user workspaces with an admin panel
- **+** Custom templates in HTML and Tailwind, or generated from an existing PowerPoint file
- **−** SSO, SCIM, audit logs and Helm charts are only in the Enterprise edition
- **−** Community template gallery calls a cloud service by default; air-gapped setups must disable it
- **−** README gives no RAM, VRAM or model-size guidance for local models
- **−** README documents only a source build for the desktop app; installers are on the website

<sub>GPU optional · Docker + Compose · Needs Docker, or Node.js, Python 3.11 and uv for Electron, LLM provider or API key · Models: OpenAI, Anthropic, Google Gemini, Vertex AI, Azure OpenAI · port 5001 · [Repo](https://github.com/presenton/presenton) · [📖 Docs ↗](https://docs.presenton.ai/) · [🌐 Site ↗](https://presenton.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/presenton/)</sub>

<a name="deepchat"></a>
### #&#8288;14 [deepchat](https://github.com/thinkinaixyz/deepchat) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Oct 2026</sub>

**Electron desktop client for cloud and Ollama models with MCP, Skills and ACP.**

DeepChat is an Electron desktop app for Windows, macOS and Linux that connects to cloud providers (OpenAI, Anthropic, Gemini, DeepSeek and others) and to local Ollama models. It adds MCP tools, installable Skills, ACP agents in the model selector, and a session Tape with request tracing. Sessions can also be driven remotely from Telegram, Feishu/Lark, QQBot, Discord and WeChat iLink.

- **+** Supports MCP Resources, Prompts and Tools over StreamableHTTP, SSE and Stdio, with one-click DeepLink install
- **+** Skills can be imported and exported with Claude Code, Codex, Cursor and similar tools
- **+** Session Tape and Trace preview show request sequences, provider metadata and token budgets
- **+** Remote control of sessions from five messaging apps, with commands like /new, /stop and /model
- **−** Desktop-only Electron app; no web or server deployment described in the README
- **−** Encryption and obfuscation are described as reserved interfaces, not enabled features
- **−** Messaging integrations lean toward Chinese platforms; no Slack or Matrix mentioned
- **−** RAM and hardware requirements are not stated

<sub>GPU optional · Docker · Needs Ollama (optional, for local models), Node.js toolchain (installed from Settings for npx-style MCP services) · Models: OpenAI, Anthropic, Gemini, DeepSeek, Moonshot · [Repo](https://github.com/thinkinaixyz/deepchat) · [🌐 Site ↗](https://deepchatai.cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepchat/)</sub>

<a name="pocketpal-ai"></a>
### #&#8288;15 [pocketpal-ai](https://github.com/a-ghorbani/pocketpal-ai) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.8k · MIT · Oct 2026</sub>

**Phone app that runs GGUF language models offline on iOS and Android.**

PocketPal AI is a React Native app for iOS and Android that runs quantized GGUF language models on the phone through llama.rn and llama.cpp. It adds on-device text-to-speech via ONNX Runtime (Kokoro and others), configurable Pals with their own system prompts, and a tool-use loop with calculator, date/time and HTML-render tools. Models are downloaded from Hugging Face, and a built-in benchmark reports tokens/sec and memory.

- **+** Chat, TTS and tool calls run on-device with no account or internet after model download
- **+** Searches and downloads GGUF models from Hugging Face, including gated ones with a token
- **+** CPU, Metal, OpenCL (Adreno) and Qualcomm Hexagon NPU paths with graceful fallback
- **+** Built-in benchmark for tokens/sec and memory, with optional public leaderboard
- **−** Only three built-in tools: calculate, datetime and render_html
- **−** Mobile only; no desktop or server build is described
- **−** Model size is limited by phone RAM; the README gives no minimum
- **−** Some Pals on PalsHub are premium via in-app purchase

<sub>GPU optional · Needs llama.rn, llama.cpp, ONNX Runtime, WatermelonDB · Models: GGUF, ONNX (TTS) · [Repo](https://github.com/a-ghorbani/pocketpal-ai) · [🌐 Site ↗](https://pocketpal.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pocketpal-ai/)</sub>

<a name="clawx"></a>
### #&#8288;16 [clawx](https://github.com/valuecell-ai/clawx) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · MIT · Oct 2026</sub>

**Electron desktop app for running and managing OpenClaw agents without a terminal.**

ClawX is an Electron and React desktop client that embeds the OpenClaw runtime and gives it a GUI for chat, agents, skills, model providers, messaging channels and cron schedules. Provider credentials are kept in the native system keychain. An optional Developer Mode feature lets agents operate the local desktop through a bundled CUA driver on macOS 13+ and Windows x64.

- **+** Embeds the OpenClaw runtime, so no separate install is needed
- **+** Setup wizard and settings UI replace config files and CLI use
- **+** Channels support multiple accounts, per-account agent binding and cron delivery
- **+** Provider API keys are stored in the native system keychain
- **−** Depends on OpenClaw upstream, which the README describes as iterating rapidly
- **−** OpenClaw's general web_search tool is disabled in ClawX
- **−** Computer Use is off by default and needs Developer Mode and a vision model
- **−** Overwrites edits to ~/.openclaw/skills/computer-use on every startup

<sub>RAM ≥ 4 GB · no GPU · Needs OpenClaw (bundled), Electron, pnpm (build from source) · Models: OpenAI, Anthropic, Z.AI / GLM, custom providers · [Repo](https://github.com/valuecell-ai/clawx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clawx/)</sub>

<a name="lobsterai"></a>
### #&#8288;17 [lobsterai](https://github.com/netease-youdao/lobsterai) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Oct 2026</sub>

**Electron desktop agent that edits files, drives a browser, and takes tasks from chat apps.**

LobsterAI is an Electron app for macOS and Windows where an agent works on a local folder: it reads and edits files, runs shell commands, drives a built-in browser and previews Office documents in a side panel. It runs on a bundled, pinned OpenClaw runtime, stores sessions in local SQLite, and can take tasks from WeChat, Feishu, DingTalk, Telegram and other chat apps or from scheduled jobs. Models come from built-in providers after sign-in or from your own API keys.

- **+** Permission prompts gate file, shell and network actions; sessions stored locally in SQLite
- **+** Built-in Word, Excel and PowerPoint editing and previews for HTML, PDF, images and video
- **+** Eleven IM channels incl. WeChat, Feishu, DingTalk, Telegram, Discord; bots can route to different agents
- **+** Supports own keys for OpenAI, Anthropic, Gemini, Ollama, LM Studio and OpenAI-compatible endpoints
- **−** Desktop only: macOS and Windows, no Linux build listed
- **−** Built-in models require sign-in; the README does not say what account is needed
- **−** Computer use limited to Windows x64 and macOS 13 or later
- **−** Building from source needs Node 24.15+, npm 11.17+, pnpm and a fetched OpenClaw checkout

<sub>no GPU · Needs OpenClaw runtime (bundled), SQLite (local), Node.js >=24.15.0 <25 (build from source) · Models: DeepSeek, GLM, Kimi, Qwen, MiniMax · [Repo](https://github.com/netease-youdao/lobsterai) · [🌐 Site ↗](https://lobsterai.youdao.com/#/download-list) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lobsterai/)</sub>

<a name="everywhere"></a>
### #&#8288;18 [everywhere](https://github.com/sylinko/everywhere) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · custom license · Oct 2026</sub>

**Hotkey-invoked desktop AI assistant that reads on-screen context in Windows and macOS apps.**

Everywhere is a C# desktop app (.NET 10, Avalonia) for Windows and macOS. A global hotkey opens a chat overlay that pulls context from the active app through accessibility APIs and UI automation, so no screenshot or copy-paste is needed. It connects to OpenAI, Anthropic, Gemini, DeepSeek, Moonshot, MiniMax, Ollama or a custom API endpoint, and agents can use a web browser, the file system, terminal scripts, sub-agents and MCP tools.

- **+** Reads active-app context via accessibility APIs and UI automation, not only screenshots
- **+** Supports Ollama and custom API endpoints alongside OpenAI, Anthropic, Gemini and DeepSeek
- **+** Agent tools include browser, file system, terminal scripts, sub-agents and MCP
- **+** Installers for Windows x64 and macOS (arm64 and Intel), plus a portable Windows zip
- **−** No Linux build yet; listed as in development
- **−** Memory system, voice interaction and mouse shortcuts are still work in progress
- **−** License is not identified as a standard SPDX license (NOASSERTION); check the LICENSE file
- **−** README gives no RAM or hardware requirements for local models

<sub>Needs Ollama (optional, for local models) · Models: OpenAI, Anthropic, Google Gemini, DeepSeek, Moonshot (Kimi) · [Repo](https://github.com/sylinko/everywhere) · [📖 Docs ↗](https://everywhere.sylinko.com) · [🌐 Site ↗](https://everywhere.sylinko.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/everywhere/)</sub>

<a name="enchanted"></a>
### #&#8288;19 [enchanted](https://github.com/gluonfield/enchanted) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (3) · Freshness: active (94) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Jul 2026</sub>

**Native iOS, macOS and visionOS chat client for Ollama servers.**

Enchanted is a Swift app for macOS, iOS and visionOS that connects to an Ollama server (v0.1.14 or later) and gives a ChatGPT-style interface to your own models. It supports image attachments, voice prompts, read-aloud, Markdown rendering and a macOS Spotlight-style panel. Conversation history is stored on the device. The README says the same author's newer project, Jaz, is the next iteration.

- **+** Native Swift app covering macOS, iOS and visionOS
- **+** Conversation history stored on the device
- **+** Image attachments, voice prompts, read-aloud and custom system prompt
- **+** macOS Spotlight panel (Ctrl+Cmd+K) with reusable prompt templates
- **−** Only talks to Ollama; no other backends are documented
- **−** Needs your own Ollama server, reachable from the phone
- **−** Local-server setup relies on an ngrok tunnel, per the README
- **−** README points to Jaz as the new iteration of the project

<sub>Needs Ollama v0.1.14 or later, ngrok (to expose a local Ollama server) · Models: Ollama models (Llama 2, Mistral, Vicuna, Starling) · [Repo](https://github.com/gluonfield/enchanted) · [▶️ Demo ↗](https://www.youtube.com/watch?v=zW3roZ_vM5Q) · [🌐 Site ↗](https://apps.apple.com/gb/app/enchanted-llm/id6474268307) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/enchanted/)</sub>

<a name="aichat"></a>
### #&#8288;20 [aichat](https://github.com/sigoden/aichat) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: known (34) · Freshness: slowing (35) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Feb 2026</sub>

**Rust command-line LLM client with shell assistant, REPL, RAG and agents.**

AIChat is a Rust CLI that talks to over 20 LLM providers through one interface, in single-prompt CMD mode or an interactive REPL. It adds roles, sessions, macros, RAG over local documents, function calling and agents, plus a built-in HTTP server exposing chat, embeddings and rerank endpoints with a playground and arena.

- **+** Single Rust binary, installable via cargo, brew, pacman, scoop or Termux
- **+** Covers OpenAI, Claude, Gemini, Ollama, Bedrock, VertexAI and any OpenAI-compatible API
- **+** Built-in server exposes chat, embeddings and rerank endpoints plus a web playground and arena
- **+** Accepts stdin, files, directories, URLs and command output as input
- **−** Terminal-first; the web playground is the only graphical interface
- **−** No multi-user accounts or chat history UI described
- **−** Last release 2025-07-06, older than the latest commit
- **−** Tool and agent setup relies on the separate llm-functions repository

<sub>no GPU · Needs LLM provider API key or local Ollama, llm-functions (optional, for tools and agents) · Models: OpenAI, Claude, Gemini, Ollama, Groq · port 8000 · [Repo](https://github.com/sigoden/aichat) · [📖 Docs ↗](https://github.com/sigoden/aichat/wiki/Command-Line-Guide) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aichat/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
