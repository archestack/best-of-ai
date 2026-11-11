# 🖥️ Desktop AI apps reviews · Best of Open-Source AI

Apps you install on your own computer to chat with local or API models, often with document chat and agents built in. Back to the [leaderboard](../README.md#%EF%B8%8F-desktop-ai-apps).

<sub>🌐 Also on the web: [Desktop AI apps on archestack.com](https://archestack.com/best-of-ai/desktop-apps/), each project on its own page.</sub>

<a name="cherry-studio"></a>
### 🥇 [cherry-studio](https://github.com/cherryhq/cherry-studio) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · AGPL-3.0 · Nov 2026</sub>

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

<a name="dsh-desktop"></a>
### 🥈 [dsh-desktop](https://github.com/anywhere-labs/dsh-desktop) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Nov 2026</sub>

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

<a name="screenpipe"></a>
### 🥉 [screenpipe](https://github.com/screenpipe/screenpipe) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · custom license · Nov 2026</sub>

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
### #&#8288;4 [deep-live-cam](https://github.com/hacksider/deep-live-cam) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 98k · AGPL-3.0 · Nov 2026</sub>

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

<a name="prompt-optimizer"></a>
### #&#8288;5 [prompt-optimizer](https://github.com/linshenkx/prompt-optimizer) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · custom license · Nov 2026</sub>

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

<a name="artcraft"></a>
### #&#8288;6 [artcraft](https://github.com/storytold/artcraft) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Nov 2026</sub>

**Desktop app for staging 2D and 3D scenes before generating images and video.**

ArtCraft is a Rust desktop app for Windows, macOS and Linux that combines a 2D canvas with a 3D scene stage. You pose characters, block scenes and composite layers, then send the result to hosted image, video, 3D mesh, music or world-generation models. Generation goes through providers such as ArtCraft's own catalog, Grok, Midjourney, Sora and World Labs.

- **+** 3D scene staging, character posing and camera placement before generation
- **+** Large catalog: 62 ArtCraft-listed models across image, video, audio, 3D and worlds
- **+** Canvas tools for masks, inpainting, background removal and layer compositing
- **+** Packages for Windows, macOS and Linux, including AppImage, DEB, RPM, Arch and Flatpak
- **−** Generation uses hosted providers; no local model inference is described
- **−** Some catalog models are disabled or restricted in the desktop app
- **−** Kling, Google, Runway and Luma integrations are still only planned
- **−** README says dual MIT or Apache-2.0, while detected license is Apache-2.0 only

<sub>Needs ArtCraft hosted generation service, Grok, Midjourney, Sora, World Labs · Models: Nano Banana, GPT Image, FLUX, Seedream, Seedance · [Repo](https://github.com/storytold/artcraft) · [▶️ Demo ↗](https://www.youtube.com/watch?v=kzvQMdg66Go) · [🌐 Site ↗](https://getartcraft.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/artcraft/)</sub>

<a name="aionui"></a>
### #&#8288;7 [aionui](https://github.com/iofficeai/aionui) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;8 [jan](https://github.com/janhq/jan) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 46k · custom license · Nov 2026</sub>

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

<a name="openwork"></a>
### #&#8288;9 [openwork](https://github.com/different-ai/openwork) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Nov 2026</sub>

**Desktop app where OpenCode-based agents work on your local files.**

OpenWork is an Electron desktop app for macOS, Windows and Linux, built on OpenCode, that runs AI agents against files on your machine. It connects to 50+ providers with your own keys, or to local models via Ollama or any OpenAI-compatible server. A remote MCP server shares skills and connections with Codex, Claude Code and Cursor, and a separate control plane (Den) manages team access.

- **+** Runs on macOS, Windows and Linux; files stay local, cloud is optional
- **+** Works with 50+ providers, own API keys, Ollama or OpenAI-compatible servers
- **+** OpenWork MCP exposes four tools to Codex, Claude Code, OpenCode and other clients
- **+** Imports Claude-compatible plugins, skills and MCP servers from a Cowork setup
- **−** Den control plane (ee/) is source-available; production use above 5 users needs a subscription
- **−** Shared MCP endpoint is hosted at api.openworklabs.com and needs browser sign-in
- **−** Mixed MIT and EE licensing; repository license is detected as NOASSERTION
- **−** Contributor setup needs Node 24 and pnpm 11; npm and yarn are not supported

<sub>GPU optional · Needs OpenCode, Ollama (optional, for local models), Node 24 and pnpm 11 (development only) · Models: Anthropic, OpenAI, Google, Ollama, OpenAI-compatible servers · [Repo](https://github.com/different-ai/openwork) · [📖 Docs ↗](https://openworklabs.com/docs) · [🌐 Site ↗](https://openworklabs.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openwork/)</sub>

<a name="hermes-desktop"></a>
### #&#8288;10 [hermes-desktop](https://github.com/fathah/hermes-desktop) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

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
### #&#8288;11 [chatbox](https://github.com/chatboxai/chatbox) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · GPL-3.0 · Nov 2026</sub>

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

<a name="openmausbot"></a>
### #&#8288;12 [openmausbot](https://github.com/milind-soni/openmausbot) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Nov 2026</sub>

**Chat app where each bot is a Claude, Codex or Grok CLI agent.**

OpenMausBot is a desktop messaging-style app for macOS, Windows and Ubuntu in which each contact is an agent run through your locally installed claude, codex or grok CLI. A harness server on 127.0.0.1:8799 manages the agent processes and routes permission requests to inline Allow/Deny cards. Bots can use a boat.dev cloud desktop, a local VM or your own machine, and connect to apps through Composio.

- **+** Reuses your existing claude, codex and grok CLI logins, with no proxy in between
- **+** Approval cards for shell commands and file edits, for cloud and local computers
- **+** Transcripts, keys and events stay in ~/.openmausbot on your machine
- **+** Stdio MCP server and headless openmausbot CLI for scripts and CI
- **−** Needs the claude, codex or grok CLI installed; local open-weight models are not described
- **−** Cloud computers rely on boat.dev and app connectors on Composio, both hosted
- **−** Windows installer is not code-signed, so SmartScreen warns on install
- **−** Ubuntu Wayland host control is disabled; the Ubuntu AppImage is beta

<sub>no GPU · Docker + Compose · Needs claude CLI, codex CLI, grok CLI, Composio, boat.dev · Models: Claude, Codex, Grok · port 5199 · README: alternative to Manus · [Repo](https://github.com/milind-soni/openmausbot) · [🌐 Site ↗](https://www.openmausbot.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmausbot/)</sub>

<a name="dsh-go"></a>
### #&#8288;13 [dsh-go](https://github.com/ccch1mneyyy/dsh-go) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · AGPL-3.0 · Nov 2026</sub>

**Android client for DeepSeek Harness, local or remote.**

DSH Go is a Flutter Android app that provides a chat UI for DeepSeek Harness (DSH). It installs an Ubuntu and Node.js runtime inside the app, with no root or Termux, or connects over SSH or DSHarness Remote to DSH on a PC or server. It also handles tool approvals, image and voice input, optional phone control, and end-to-end encrypted share links. It is an unofficial third-party project.

- **+** Runs the DSH engine on-device via a bundled Ubuntu runtime, no root or Termux
- **+** Can switch to DSH on a PC or server over SSH or DSHarness Remote
- **+** Phone control reads the screen and taps, with three confirmation levels
- **+** Plugin SDK and examples are MIT-licensed; build-from-source scripts are provided
- **−** Android 8+ only; iOS and HarmonyOS are not yet supported
- **−** Model requests still go to a configured provider; local run is not offline
- **−** Anonymous usage statistics are on by default and must be turned off
- **−** DSHarness Remote lacks web mode, DS Bot and log export; attachments are image-only

<sub>no GPU · Needs DeepSeek Harness, Model provider API, Shizuku or ADB (optional, do-not-disturb phone control) · Models: Models from the provider configured in DeepSeek Harness · [Repo](https://github.com/ccch1mneyyy/dsh-go) · [📖 Docs ↗](https://github.com/ccch1mneyyy/dsh-go/blob/main/docs/guide/README.md) · [🌐 Site ↗](https://go.dshtui.com/download) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dsh-go/)</sub>

<a name="gallery"></a>
### #&#8288;14 [gallery](https://github.com/google-ai-edge/gallery) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · Apache-2.0 · Nov 2026</sub>

**Mobile app for running open LLMs offline on Android and iOS.**

Google AI Edge Gallery is a Kotlin app for Android and iOS, with a macOS download, that runs open models on-device through LiteRT. It bundles chat with speech input and output, image questions, audio transcription, prompt testing, agent skills and on-device semantic media search. Models come from Hugging Face or are loaded as custom files, and can be benchmarked on the device.

- **+** Inference runs on-device via LiteRT, so prompts and media stay offline
- **+** Chat, image Q&A, audio transcription, prompt lab and media search in one app
- **+** Built-in benchmarks show how each model performs on your own hardware
- **+** Loads custom models, pulls from Hugging Face; Agent Skills can load from a URL
- **−** README calls it an experimental Beta release
- **−** Requires Android 12+ or iOS 17+; the macOS build is versioned 0.1.0
- **−** No server or API exposed; usable only through the app UI
- **−** Model choice is limited to formats LiteRT supports

<sub>Needs LiteRT, Hugging Face (model download) · Models: LiteRT models, EmbeddingGemma 2, FunctionGemma 270m finetunes, custom models · [Repo](https://github.com/google-ai-edge/gallery) · [📖 Docs ↗](https://github.com/google-ai-edge/gallery/wiki) · [🌐 Site ↗](https://ai.google.dev/edge) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gallery/)</sub>

<a name="anarlog"></a>
### #&#8288;15 [anarlog](https://github.com/fastrepl/anarlog) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.8k · MIT · Nov 2026</sub>

**Local-first meeting notetaker that records device audio without a bot joining.**

anarlog is a Tauri v2 desktop app (Rust backend, React UI) that captures meeting audio on your device, transcribes it, and generates notes, summaries and chat. Data is stored in local SQLite plus plain files, with Markdown export. Transcription and summarization are configured separately, using on-device models, your own API key, an OpenAI-compatible local server such as Ollama or LM Studio, or optional hosted AI.

- **+** No meeting bot; audio is captured on the device
- **+** Transcription and LLM providers can be swapped independently
- **+** Notes and transcripts in local SQLite; Markdown export
- **+** Works with Ollama, LM Studio or any OpenAI-compatible server
- **−** On-device transcription is described only for supported Macs
- **−** Building from source needs Node 22, pnpm, Rust 1.94, process-compose, Tauri deps
- **−** Hosted AI, CloudSync and sharing depend on the vendor's cloud services
- **−** Enterprise components in enterprise/ are under a commercial license

<sub>GPU optional · Needs SQLite, Ollama or LM Studio (optional), OpenRouter (optional hosted AI), Supabase (optional backend) · Models: Soniqo, Apple Speech, Apple Intelligence, Soniox (cloud), Claude via OpenRouter (cloud) · README: alternative to Granola · [Repo](https://github.com/fastrepl/anarlog) · [📖 Docs ↗](https://docs.anarlog.so) · [🌐 Site ↗](https://anarlog.so) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/anarlog/)</sub>

<a name="openworker"></a>
### #&#8288;16 [openworker](https://github.com/andrewyng/openworker) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs Python 3.10+ (source), Node 20+ (source), Rust toolchain (desktop build from source), Ollama (optional), NVIDIA OpenShell (optional) · Models: OpenAI, Anthropic, Google Gemini, DeepSeek, Qwen · port 8765 · [Repo](https://github.com/andrewyng/openworker) · [🌐 Site ↗](https://openworker.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openworker/)</sub>

<a name="eigent"></a>
### #&#8288;17 [eigent](https://github.com/eigent-ai/eigent) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="read-frog"></a>
### #&#8288;18 [read-frog](https://github.com/mengxi-ream/read-frog) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · GPL-3.0 · Nov 2026</sub>

**Browser extension that translates pages and subtitles for language learners.**

Read Frog is a Chrome, Edge and Firefox extension for language learners. It translates web pages in bilingual or translation-only mode, translates selected text, and adds bilingual subtitles on YouTube, X and Netflix. Saved vocabulary goes to Notebase and is reviewed as flashcards on a spaced-repetition schedule. It connects to 20+ LLM providers through the Vercel AI SDK, plus Google Translate, Microsoft Translate and DeepLX.

- **+** Works with 20+ providers including OpenAI, Anthropic, Gemini, DeepSeek and local Ollama
- **+** Free translation backends available: Google Translate, Microsoft Translate, DeepLX
- **+** Request batching claims up to 70% lower API cost, with retry and per-request fallback
- **+** Custom AI actions with structured output, plus flashcard review of saved words
- **−** Dual-licensed GPLv3 and commercial; closed-source use needs a separate license
- **−** AI transcription for YouTube videos without captions is limited to Pro and Ultra plans
- **−** README says the project is under active development, so behavior may change
- **−** Runs only inside Chrome, Edge or Firefox; no standalone app

<sub>no GPU · Needs Chrome, Edge or Firefox, LLM provider API key or free translation service · Models: OpenAI, Anthropic Claude, Google Gemini, DeepSeek, xAI Grok · [Repo](https://github.com/mengxi-ream/read-frog) · [📖 Docs ↗](https://www.readfrog.app/en/docs) · [🌐 Site ↗](https://www.readfrog.app/en) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/read-frog/)</sub>

<a name="presenton"></a>
### #&#8288;19 [presenton](https://github.com/presenton/presenton) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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

<a name="pocketpal-ai"></a>
### #&#8288;20 [pocketpal-ai](https://github.com/a-ghorbani/pocketpal-ai) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · MIT · Nov 2026</sub>

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

<a name="deepchat"></a>
### #&#8288;21 [deepchat](https://github.com/thinkinaixyz/deepchat) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Nov 2026</sub>

**Electron desktop client for cloud and Ollama models with MCP, Skills and ACP.**

DeepChat is an Electron desktop app for Windows, macOS and Linux that connects to cloud providers (OpenAI, Anthropic, Gemini, DeepSeek and others) and to local Ollama models. It adds MCP tools, installable Skills, ACP agents in the model selector, and a session Tape with request tracing. Sessions can also be driven remotely from Telegram, Feishu/Lark, QQBot, Discord and WeChat iLink.

- **+** Supports MCP Resources, Prompts and Tools over StreamableHTTP, SSE and Stdio, with one-click DeepLink install
- **+** Skills can be imported and exported with Claude Code, Codex, Cursor and similar tools
- **+** Session Tape and Trace preview show request sequences, provider metadata and token budgets
- **+** Remote control of sessions from five messaging apps, with commands like /new, /stop and /model
- **−** Desktop-only Electron app; no web or server deployment described in the README
- **−** Encryption and obfuscation are described as reserved interfaces, not enabled features
- **−** Messaging integrations lean toward Chinese platforms; no Slack or Matrix mentioned

<sub>GPU optional · Docker · Needs Ollama (optional, for local models), Node.js toolchain (installed from Settings for npx-style MCP services) · Models: OpenAI, Anthropic, Gemini, DeepSeek, Moonshot · [Repo](https://github.com/thinkinaixyz/deepchat) · [🌐 Site ↗](https://deepchatai.cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepchat/)</sub>

<a name="lobsterai"></a>
### #&#8288;22 [lobsterai](https://github.com/netease-youdao/lobsterai) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Nov 2026</sub>

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

<a name="clawx"></a>
### #&#8288;23 [clawx](https://github.com/valuecell-ai/clawx) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · MIT · Nov 2026</sub>

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

<a name="nightly-labs-openbot"></a>
### #&#8288;24 [openbot](https://github.com/nightly-labs/openbot) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · custom license · Nov 2026</sub>

**Desktop workspace that runs coding-agent CLIs as persistent teammates.**

OpenBot is an Electron desktop app that wraps local agent CLIs (Codex, Claude Code, Grok, OpenCode, Gemini, Cursor, Cline, Kimi, Devin, Copilot, Mistral Vibe, Hermes) as persistent agents. Each agent gets its own workspace and conversation, with FIFO message queues, agent-to-agent messaging, file transfer and an embedded browser they can control. It also runs headless on Linux servers or in Docker.

- **+** Supports about a dozen agent CLIs, plus custom ACP agents and OpenAI-compatible endpoints
- **+** Per-agent workspaces, crash-safe FIFO queues and automatic context compaction
- **+** Can run headless via a server install script or Docker image (amd64 and arm64)
- **+** Optional Computer Use through a bundled cua-driver on macOS, Windows and Linux
- **−** PolyForm Noncommercial license; not free software and restricted for commercial use
- **−** Agents run with danger-full-access and no per-action approval after first-launch consent
- **−** Depends on hosted providers (OpenAI, Anthropic, Google and others); not offline-only
- **−** Gemini sign-in needs a desktop browser; remote desktop is X11 only on Linux x64

<sub>no GPU · Docker + Compose · Needs Agent CLIs (Codex, Claude Code, etc.), Bun 1.4.2 and Node.js 24 (development only), Cloudflare Workers and D1 (optional accounts) · Models: Codex, Claude Code, Grok CLI, OpenCode, Gemini · [Repo](https://github.com/nightly-labs/openbot) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nightly-labs-openbot/)</sub>

<a name="local-studio"></a>
### #&#8288;25 [local-studio](https://github.com/sybil-solutions/local-studio) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Oct 2026</sub>

**Desktop coding-agent UI, forked from T3 Code, with a local model gateway.**

Local Studio is a thin fork of T3 Code, an Electron app that runs coding agents such as Codex, Claude, Cursor, OpenCode, Pi and Oh My Pi. It adds a bundled controller that discovers vLLM, SGLang, llama.cpp and other /v1/models servers and exposes them through one OpenAI/Anthropic-compatible gateway. Settings can also link machines on a Tailscale tailnet into a fleet.

- **+** Controller serves /v1/chat/completions, /v1/messages and /v1/responses across machines
- **+** Installs a controller on Linux or macOS tailnet machines over ssh as a user service
- **+** Can launch pinned registry recipes on free NVIDIA GPUs
- **+** Local changes capped at 4,000 lines by a check script, easing upstream merges
- **−** Needs at least one agent CLI (pi, omp, or another provider) installed and logged in first
- **−** Windows installer is not code-signed, so SmartScreen warns
- **−** Fleet install requires key-based ssh and Tailscale; Linux and macOS targets only
- **−** Most docs are upstream's and may not describe Local Studio additions

<sub>GPU optional · Needs Tailscale (for fleet), ssh (for remote controller install), Agent CLI such as pi or omp, Node 24, pnpm 11, Bun 1.3.14 (development only) · Models: vLLM, SGLang, llama.cpp, OpenAI-compatible /v1/models servers · port 18091 · [Repo](https://github.com/sybil-solutions/local-studio) · [📖 Docs ↗](https://github.com/sybil-solutions/local-studio/blob/main/docs/local-studio/controller.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/local-studio/)</sub>

<a name="holaos"></a>
### #&#8288;26 [holaos](https://github.com/holaboss-ai/holaos) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (45) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Aug 2026</sub>

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

<a name="koharu"></a>
### #&#8288;27 [koharu](https://github.com/koharu-rs/koharu) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · Apache-2.0 · Nov 2026</sub>

**Desktop manga translator with local detection, OCR, inpainting and LLM translation.**

Koharu is a Rust desktop app that translates manga pages in a pipeline of text and bubble detection, OCR, inpainting to remove source text, and LLM or machine translation. Vision models and GGUF LLMs run locally, with optional hosted providers such as OpenAI, Gemini, Claude, DeepL and OpenAI-compatible endpoints. It includes a WebGPU canvas editor for manual cleanup and typesetting, and exports layered PSD.

- **+** Full pipeline in one app: detection, OCR, inpainting, translation, typesetting and layered PSD export
- **+** Runs vision models and GGUF LLMs locally; hosted LLM and MT providers are optional
- **+** GPU backends: CUDA, ROCm/HIP, Metal and Vulkan; no full CUDA SDK install needed
- **+** Handles images, archives and PDFs, with vertical CJK and right-to-left text layout
- **−** CPU inference is documented as substantially slower than GPU
- **−** Editor canvas needs WebGPU and a current graphics driver even with CPU inference
- **−** Narrow use case: manga translation only, not a general chat or assistant app
- **−** README gives no RAM or VRAM figures; larger local models need extra hardware

<sub>GPU optional · Needs WebGPU-capable graphics driver, Hugging Face model downloads, Rust, Bun and LLVM (build from source only) · Models: GGUF, Gemma 4, Qwen 3.5/3.6/3.8, Ministral 3, LFM 2.5 · [Repo](https://github.com/koharu-rs/koharu) · [📖 Docs ↗](https://koharu.rs/installation) · [🌐 Site ↗](https://koharu.rs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/koharu/)</sub>

<a name="everywhere"></a>
### #&#8288;28 [everywhere](https://github.com/sylinko/everywhere) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · custom license · Oct 2026</sub>

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

<a name="youdub-webui"></a>
### #&#8288;29 [youdub-webui](https://github.com/liuzhao1225/youdub-webui) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Nov 2026</sub>

**Desktop app that transcribes, translates and voice-clones videos into dubbed versions.**

YouDub Desktop is an Electron app that imports a local video or a YouTube/Bilibili link, transcribes it with Whisper, translates it through a configured LLM provider, and clones the original voice sentence by sentence. It outputs subtitles, a dubbed track with optional background audio retained, or both. Workflows are node graphs built on a Cordis plugin runtime, with human review steps and an /api/v2 HTTP interface.

- **+** Per-sentence voice cloning uses the matching source audio clip as reference
- **+** Three output modes: burned-in subtitles, dubbing, or dubbed video with subtitles
- **+** Node workflows support branching, merging and manual correction; tasks can be retried from a given step
- **+** Prebuilt Windows EXE and macOS arm64 DMG installers; Apache-2.0
- **−** Language catalog covers only English, Chinese and Japanese, depending on provider
- **−** Requires a configured translation model provider and API key
- **−** No published plugin marketplace; remote GitHub/npm plugin install not yet verified
- **−** README and docs are primarily in Chinese; macOS build is Apple Silicon only

<sub>Needs FFmpeg, yt-dlp, Node.js, Python, Whisper, Demucs, NLTK Punkt, LLM translation provider · Models: Whisper, Qwen alignment, Demucs · [Repo](https://github.com/liuzhao1225/youdub-webui) · [▶️ Demo ↗](https://liuzhao1225.github.io/YouDub-webui/) · [📖 Docs ↗](https://github.com/liuzhao1225/YouDub-webui/blob/main/docs/upgrade.md) · [🌐 Site ↗](https://liuzhao1225.github.io/YouDub-webui/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/youdub-webui/)</sub>

<a name="digup"></a>
### #&#8288;30 [digup](https://github.com/arahim3/digup) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · MIT · Oct 2026</sub>

**Desktop app that searches local files by meaning across text, images, audio and video.**

DigUp indexes folders you choose (images, PDFs, documents, spreadsheets, audio, video, optionally code) using EmbeddingGemma 2 run through llama.cpp, and stores vectors plus a keyword index in one SQLite file. A global shortcut opens a search panel that ranks by meaning and exact words, then opens PDFs at the page and media at the moment. Indexing and search run locally; the network is used only for the model download and update checks.

- **+** One shared embedding space lets a text query match images, PDF pages, audio and video frames
- **+** Exact-string boost finds invoice numbers and error codes alongside semantic matches
- **+** Opens results at the PDF page, media timestamp or code line in your editor
- **+** No account or telemetry; files are only read, never modified or uploaded
- **−** Mac build needs Apple Silicon and macOS 14+; Windows and Linux builds are beta
- **−** Screenshot text recognition works only on macOS; legacy .doc, RAW and SVG are Mac-only
- **−** CPU-only first index is slow: about 5 seconds per picture on a 2017 Core i5
- **−** Initial 865 MB model download; Windows installer is unsigned

<sub>GPU optional · Needs llama.cpp, SQLite, EmbeddingGemma 2 (865 MB download) · Models: EmbeddingGemma 2 (8-bit GGUF) · [Repo](https://github.com/arahim3/digup) · [🌐 Site ↗](https://digup.arahim.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/digup/)</sub>

<a name="ultimatevocalremovergui"></a>
### #&#8288;31 [ultimatevocalremovergui](https://github.com/anjok07/ultimatevocalremovergui) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (75) · Freshness: recent (70) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · MIT · Oct 2026</sub>

**Desktop app that splits vocals from instrumentals using MDX-Net and Demucs.**

UVR is a Tkinter desktop app that separates audio files into vocal and instrumental stems. It uses models trained by its core developers (MDX-Net, MDX23C, VR) plus Demucs v3/v4 4-stem models. Windows and macOS installers bundle Python and PyTorch, while Linux runs from source. It also includes Time Stretch and Pitch Shift tools that use Rubber Band.

- **+** Windows and macOS installers bundle Python and PyTorch, so no prerequisites
- **+** Supports MDX-Net, MDX23C, Demucs v4 and VR architectures in one interface
- **+** MPS acceleration on Apple M1 for Demucs v4 and all MDX-Net models
- **+** MIT-licensed code; settings are remembered between sessions
- **−** Last tagged release is v5.6 from September 2023; updates are tracked in a GitHub issue
- **−** Windows install must be on the C: drive; other drives cause instability
- **−** AMD GPU support is limited, via a separate branch or a DirectML beta build
- **−** Linux has no installer; needs manual venv setup and running UVR.py

<sub>GPU optional · Needs FFmpeg, Rubber Band, PyTorch, Python 3.9 (Windows manual install) · Models: MDX-Net, MDX23C, Demucs v3, Demucs v4, VR Architecture · [Repo](https://github.com/anjok07/ultimatevocalremovergui) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ultimatevocalremovergui/)</sub>

<a name="enchanted"></a>
### #&#8288;32 [enchanted](https://github.com/gluonfield/enchanted) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (8) · Freshness: active (91) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Jul 2026</sub>

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

<a name="noi"></a>
### #&#8288;33 [noi](https://github.com/lencx/noi) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: known (31) · Freshness: active (90) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 9.1k · no license · Aug 2026</sub>

**Desktop app for running isolated AI chat sessions in multiple windows.**

Noi is a desktop app that runs AI chat sessions in multiple windows with isolated contexts. It keeps history, prompts and settings on the local machine, and adds prompt management, a built-in terminal and a `noi` CLI that tools like Claude Code, Codex and Gemini CLI can call. The README does not list supported sites, platforms or system requirements.

- **+** Multi-window workspaces with per-session isolation
- **+** History, prompts and settings stay on the local device
- **+** `noi` CLI lets coding agents control the app
- **+** Built-in terminal and prompt management
- **−** No license detected in the repository
- **−** README lists no supported AI sites, models or platforms
- **−** CLI is early, with more commands still to come
- **−** No docs link or demo in the README

<sub>[Repo](https://github.com/lencx/noi) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/noi/)</sub>

<a name="aichat"></a>
### #&#8288;34 [aichat](https://github.com/sigoden/aichat) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: known (41) · Freshness: slowing (30) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Feb 2026</sub>

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
