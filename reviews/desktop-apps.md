# 🖥️ Desktop AI apps reviews · Best of Open-Source AI

Apps you install on your own computer to chat with local or API models, often with document chat and agents built in. Back to the [leaderboard](../README.md#%EF%B8%8F-desktop-ai-apps).

<sub>🌐 Also on the web: [Desktop AI apps on archestack.com](https://archestack.com/best-of-ai/desktop-apps/), each project on its own page.</sub>

<a name="cherry-studio"></a>
### 🥇 [cherry-studio](https://github.com/cherryhq/cherry-studio) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · AGPL-3.0 · Oct 2026</sub>

**Cross-platform desktop chat client for many cloud and local LLM providers.**

Cherry Studio is a desktop app for Windows, macOS and Linux that talks to cloud providers such as OpenAI, Gemini and Anthropic, and to local models through Ollama and LM Studio. It includes 300+ preset assistants, simultaneous multi-model chats, document handling (text, images, Office, PDF), WebDAV backup and an MCP server integration. An Enterprise Edition with admin backend and shared knowledge bases is sold separately.

- **+** Supports cloud providers plus local Ollama and LM Studio in one client
- **+** Runs the same prompt against multiple models in a single conversation
- **+** Installs as a desktop app with no environment setup, on Windows, Mac and Linux
- **+** 300+ preconfigured assistants plus custom assistant creation
- **−** AGPL-3.0; commercial use outside AGPL terms needs a separate license
- **−** Admin backend, team knowledge base and access control are Enterprise-only
- **−** Plugin system, OCR, TTS and ASR are listed as roadmap items, not shipped
- **−** No Docker or web deployment; desktop only, so no multi-user server in Community Edition

<sub>GPU optional · Needs Ollama or LM Studio (optional, for local models), WebDAV (optional, for backup) · Models: OpenAI, Gemini, Anthropic, Ollama, LM Studio · [Repo](https://github.com/cherryhq/cherry-studio) · [▶️ Demo ↗](https://enterprise.cherry-ai.com) · [📖 Docs ↗](https://docs.cherry-ai.com/docs/en-us) · [🌐 Site ↗](https://cherry-ai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cherry-studio/)</sub>

<a name="prompt-optimizer"></a>
### 🥈 [prompt-optimizer](https://github.com/linshenkx/prompt-optimizer) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: very easy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · custom license · Oct 2026</sub>

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

<a name="deep-live-cam"></a>
### 🥉 [deep-live-cam](https://github.com/hacksider/deep-live-cam) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 97k · AGPL-3.0 · Oct 2026</sub>

**Real-time webcam face swap from a single source image.**

Deep-Live-Cam is a Python desktop GUI that swaps a face from one source image onto a webcam feed, video or image, using ONNX models (inswapper_128_fp16, gfpgan-1024). It supports mouth masking, mapping different faces to multiple subjects, and CPU, CUDA, CoreML, DirectML and OpenVINO execution providers. A paid pre-built edition with extra features is sold on the project website.

- **+** Live webcam mode plus image and video file processing from one GUI
- **+** Execution providers for CPU, CUDA, CoreML, DirectML and OpenVINO
- **+** Mouth mask and face mapping for multiple subjects in one frame
- **+** Needs only a single source image, no per-face training
- **−** Manual install needs Python, ffmpeg, CUDA/cuDNN pinning; README says not for beginners
- **−** CPU-only mode is slower; live preview takes 10-30 seconds to appear
- **−** Command-line arguments are marked unmaintained in the README
- **−** insightface models are limited to non-commercial research use

<sub>GPU optional · Needs Python 3.11-3.14, ffmpeg, onnxruntime, CUDA Toolkit 12.8 (NVIDIA), tkinter, OBS (for streaming output) · Models: inswapper_128_fp16.onnx, gfpgan-1024.onnx, ONNX · [Repo](https://github.com/hacksider/deep-live-cam) · [📖 Docs ↗](https://deeplivecam.net/index.php/quickstart) · [🌐 Site ↗](https://deeplivecam.net) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deep-live-cam/)</sub>

<a name="jan"></a>
### #&#8288;4 [jan](https://github.com/janhq/jan) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 45k · custom license · Oct 2026</sub>

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

<a name="screenpipe"></a>
### #&#8288;5 [screenpipe](https://github.com/screenpipe/screenpipe) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · custom license · Oct 2026</sub>

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

<sub>RAM ≥ 8 GB · GPU optional · Needs Node.js (npx CLI), Ollama (optional local LLM), Deepgram (optional cloud transcription) · Models: Whisper Large-V3-Turbo, Deepgram, Ollama, OpenAI-compatible servers · port 3030 · README: alternative to Otter.ai · [Repo](https://github.com/screenpipe/screenpipe) · [📖 Docs ↗](https://docs.screenpi.pe) · [🌐 Site ↗](https://screenpi.pe) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/screenpipe/)</sub>

<a name="dsh-desktop"></a>
### #&#8288;6 [dsh-desktop](https://github.com/anywhere-labs/dsh-desktop) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

**Native Windows and macOS desktop client for DeepSeek Harness.**

DSH Desktop wraps the pinned, unmodified upstream DeepSeek Harness web UI, host service and plugin system in a native desktop app with window, tray, terminal and auto-update. The desktop shell is itself a DSH plugin, and the app includes a plugin market and phone remote control (iOS/Android, from 2.0.9). Installers cover Windows x64 and macOS Universal; no Node.js is needed.

- **+** Installers for Windows x64 and macOS Universal, no separate Node.js install
- **+** Runs a pinned, unmodified upstream DeepSeek Harness version
- **+** Built-in plugin market and desktop services for third-party plugins
- **+** Web service listens on loopback only by default
- **−** No Linux build listed
- **−** LAN access option has no authentication, per the README
- **−** Tied to DeepSeek Harness; independent project, not affiliated with DeepSeek
- **−** README and docs are primarily in Chinese

<sub>Needs DeepSeek Harness (bundled, pinned) · Models: DeepSeek Harness models · [Repo](https://github.com/anywhere-labs/dsh-desktop) · [📖 Docs ↗](https://github.com/anywhere-labs/dsh-desktop/blob/main/docs/user-guide.md) · [🌐 Site ↗](https://dshdesktop.cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dsh-desktop/)</sub>

<a name="chatbox"></a>
### #&#8288;7 [chatbox](https://github.com/chatboxai/chatbox) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (75) · Easy to run: easy (50) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · GPL-3.0 · Sep 2026</sub>

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

<a name="aionui"></a>
### #&#8288;8 [aionui](https://github.com/iofficeai/aionui) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (77) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Oct 2026</sub>

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

<a name="hermes-desktop"></a>
### #&#8288;9 [hermes-desktop](https://github.com/fathah/hermes-desktop) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

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

<a name="openworker"></a>
### #&#8288;10 [openworker](https://github.com/andrewyng/openworker) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: fair (73) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

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
### #&#8288;11 [eigent](https://github.com/eigent-ai/eigent) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: fair (73) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
