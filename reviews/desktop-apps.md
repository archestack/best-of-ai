# 🖥️ Desktop AI apps reviews · Best of Open-Source AI

Apps you install on your own computer to chat with local or API models, often with document chat and agents built in. Back to the [leaderboard](../README.md#%EF%B8%8F-desktop-ai-apps).

<sub>🌐 Also on the web: [Desktop AI apps on archestack.com](https://archestack.com/best-of-ai/desktop-apps/), each project on its own page.</sub>

<a name="cherry-studio"></a>
### 🥇 [cherry-studio](https://github.com/cherryhq/cherry-studio) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · AGPL-3.0 · Nov 2026</sub>

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
### 🥈 [screenpipe](https://github.com/screenpipe/screenpipe) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · custom license · Nov 2026</sub>

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

<a name="dsh-desktop"></a>
### 🥉 [dsh-desktop](https://github.com/anywhere-labs/dsh-desktop) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Nov 2026</sub>

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
### #&#8288;4 [prompt-optimizer](https://github.com/linshenkx/prompt-optimizer) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · custom license · Nov 2026</sub>

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

<a name="hermes-desktop"></a>
### #&#8288;5 [hermes-desktop](https://github.com/fathah/hermes-desktop) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

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

<a name="artcraft"></a>
### #&#8288;6 [artcraft](https://github.com/storytold/artcraft) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;7 [aionui](https://github.com/iofficeai/aionui) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Nov 2026</sub>

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

<a name="openwork"></a>
### #&#8288;8 [openwork](https://github.com/different-ai/openwork) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Nov 2026</sub>

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

<a name="deep-live-cam"></a>
### #&#8288;9 [deep-live-cam](https://github.com/hacksider/deep-live-cam) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 98k · AGPL-3.0 · Nov 2026</sub>

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

<a name="jan"></a>
### #&#8288;10 [jan](https://github.com/janhq/jan) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 46k · custom license · Nov 2026</sub>

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

<a name="dsh-go"></a>
### #&#8288;11 [dsh-go](https://github.com/ccch1mneyyy/dsh-go) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · AGPL-3.0 · Nov 2026</sub>

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

<a name="openmausbot"></a>
### #&#8288;12 [openmausbot](https://github.com/milind-soni/openmausbot) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Nov 2026</sub>

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

<a name="anarlog"></a>
### #&#8288;13 [anarlog](https://github.com/fastrepl/anarlog) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · MIT · Nov 2026</sub>

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

<a name="chatbox"></a>
### #&#8288;14 [chatbox](https://github.com/chatboxai/chatbox) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · GPL-3.0 · Nov 2026</sub>

**Electron desktop client for OpenAI, Claude, Gemini and Ollama models.**

Chatbox is a cross-platform desktop chat client (Electron, React, TypeScript) that connects to API providers such as OpenAI, Azure OpenAI, Claude and Gemini, and to local models through Ollama. Chats are stored locally on the device. It also ships iOS, Android and web versions, and this repo is the GPLv3 Community Edition synced with a pro repo.

- **+** Installers for Windows, macOS (Intel and Apple Silicon) and Linux AppImage; no server to deploy
- **+** Supports OpenAI, Azure OpenAI, Claude, Gemini, ChatGLM-6B and Ollama local models
- **+** Chat data stored locally on the device
- **+** Markdown, LaTeX and code highlighting, prompt library, DALL-E 3 image generation
- **−** Community Edition is synced with a separate pro repo, so features may differ
- **−** README documents no built-in local inference; local models require Ollama
- **−** No document chat or agent features described in the README
- **−** GPL-3.0 license restricts use in closed-source derivatives

<sub>no GPU · Needs Ollama (optional, for local models) · Models: OpenAI, Azure OpenAI, Claude, Google Gemini, Ollama · [Repo](https://github.com/chatboxai/chatbox) · [🌐 Site ↗](https://chatboxai.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatbox/)</sub>

<a name="dataelement-dsh-desktop"></a>
### #&#8288;15 [dsh-desktop](https://github.com/dataelement/dsh-desktop) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

**Desktop agent app for macOS and Windows with Office document templates.**

DSH Desktop wraps the DeepSeek Harness agent runtime in a native Electron-style desktop app for macOS (Apple Silicon and Intel) and Windows x64. It adds model provider setup, Word, Excel and PPT template modes that output DOCX, XLSX and PPTX, a workbench app market, safe-mode recovery from broken plugins, and phone pairing over LAN or a tunnel. Sessions and config stay in the local user data directory.

- **+** Generates editable DOCX, XLSX and PPTX from templates; PPT ships 16 templates, 192 layouts
- **+** Bundles Python and Office processing dependencies, so no separate runtime install
- **+** Safe mode (--safe-mode) disables third-party plugins while keeping sessions and model config
- **+** Signed, notarized macOS builds and code-signed Windows installer with auto-update
- **−** No Linux or Windows ARM64 builds
- **−** Built on DeepSeek Harness; depends on its runtime and upstream licenses
- **−** Phone access over the internet relies on Cloudflare or Pinggy tunnels; Pinggy expires after ~60 minutes
- **−** README is primarily Chinese; built-in PPT template previews are English only

<sub>Needs DeepSeek Harness, Cloudflare Quick Tunnel (optional, phone access), Pinggy (optional fallback tunnel) · Models: Third-party model providers via configurable provider setup · [Repo](https://github.com/dataelement/dsh-desktop) · [🌐 Site ↗](https://www.dshdesktop.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dataelement-dsh-desktop/)</sub>

<a name="read-frog"></a>
### #&#8288;16 [read-frog](https://github.com/mengxi-ream/read-frog) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · GPL-3.0 · Nov 2026</sub>

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

<a name="gallery"></a>
### #&#8288;17 [gallery](https://github.com/google-ai-edge/gallery) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · Apache-2.0 · Nov 2026</sub>

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

<a name="eigent"></a>
### #&#8288;18 [eigent](https://github.com/eigent-ai/eigent) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="open-codesign"></a>
### #&#8288;19 [open-codesign](https://github.com/opencoworkai/open-codesign) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · MIT · Nov 2026</sub>

**Desktop app that turns prompts into prototypes and slide decks.**

Open CoDesign is an Electron desktop app for macOS, Windows and Linux in which an agent plans, writes and previews design artifacts such as app prototypes and slide decks from a prompt. It works with your own provider keys, ChatGPT subscription sign-in, or local Ollama, and exports HTML, PDF, PPTX, ZIP and Markdown. Sessions and workspace files are stored locally.

- **+** Bring your own key: Anthropic, OpenAI, Gemini, DeepSeek, OpenRouter, Ollama or OpenAI-compatible endpoints
- **+** Exports HTML, PDF, PPTX, ZIP and Markdown rather than only a hosted preview
- **+** One-click import of existing Claude Code or Codex provider configs
- **+** Agent tool calls are visible and interruptible; designs and sessions are saved locally
- **−** Installers are not notarized or signed; macOS needs an xattr workaround
- **−** Output is interactive prototypes with simulated data, not production backends or auth
- **−** winget, Flathub and Snap Store channels are not yet available
- **−** No bundled model; output quality depends on the provider you connect

<sub>no GPU · Needs API key, ChatGPT subscription, or local Ollama · Models: Claude, GPT, Gemini, DeepSeek, Kimi · [Repo](https://github.com/opencoworkai/open-codesign) · [📖 Docs ↗](https://opencoworkai.github.io/open-codesign/quickstart) · [🌐 Site ↗](https://opencoworkai.github.io/open-codesign/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-codesign/)</sub>

<a name="deepchat"></a>
### #&#8288;20 [deepchat](https://github.com/thinkinaixyz/deepchat) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="presenton"></a>
### #&#8288;21 [presenton](https://github.com/presenton/presenton) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;22 [pocketpal-ai](https://github.com/a-ghorbani/pocketpal-ai) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · MIT · Nov 2026</sub>

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

<a name="openworker"></a>
### #&#8288;23 [openworker](https://github.com/andrewyng/openworker) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

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

<a name="lobsterai"></a>
### #&#8288;24 [lobsterai](https://github.com/netease-youdao/lobsterai) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Nov 2026</sub>

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
### #&#8288;25 [clawx](https://github.com/valuecell-ai/clawx) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · MIT · Nov 2026</sub>

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

<a name="kun"></a>
### #&#8288;26 [kun](https://github.com/kunagent/kun) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · custom license · Nov 2026</sub>

**Desktop AI workbench for coding, documents and multi-agent chats.**

Kun is a desktop app where Code, Work and chat modes share one local runtime. It covers coding with project, terminal, Git and Diff views plus a Design canvas, document and paper workspaces, and chats with personal agents, Codex, Claude Code and OpenCode. Sessions and memory stay on the machine; models come from OpenAI/Anthropic-compatible providers or local models, and a terminal TUI shares the same runtime.

- **+** Installers for macOS (Apple Silicon/Intel), Windows x64 and Linux x64 (.AppImage/.deb)
- **+** Works with OpenAI/Anthropic-compatible APIs, Ollama and presets such as DeepSeek, Kimi, GLM, Qwen
- **+** Tool, directory and workbench actions require approval by default
- **+** Terminal TUI shares threads and approvals with the GUI through one runtime
- **−** PolyForm Noncommercial 1.0.0: commercial use or hosting needs separate written permission
- **−** External contributions require signing a CLA
- **−** README and most linked docs are primarily in Chinese
- **−** Personal assistant workflow sits behind a Lab setting and needs server access

<sub>Needs Node.js 22.19+ (source builds only) · Models: OpenAI-compatible APIs, Anthropic-compatible APIs, Ollama, DeepSeek, Kimi · [Repo](https://github.com/kunagent/kun) · [📖 Docs ↗](https://www.kun-agent.com/docs) · [🌐 Site ↗](https://www.kun-agent.com/docs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kun/)</sub>

<a name="nightly-labs-openbot"></a>
### #&#8288;27 [openbot](https://github.com/nightly-labs/openbot) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · custom license · Nov 2026</sub>

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

<a name="koharu"></a>
### #&#8288;28 [koharu](https://github.com/koharu-rs/koharu) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.7k · Apache-2.0 · Nov 2026</sub>

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

<a name="holaos"></a>
### #&#8288;29 [holaos](https://github.com/holaboss-ai/holaos) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Aug 2026</sub>

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

<a name="everywhere"></a>
### #&#8288;30 [everywhere](https://github.com/sylinko/everywhere) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · custom license · Nov 2026</sub>

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

<a name="open-science"></a>
### #&#8288;31 [open-science](https://github.com/aipoch/open-science) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.5k · Apache-2.0 · Nov 2026</sub>

**Local-first research workbench with provenance tracking and portable .science exports.**

AIPOCH Open-Science is a desktop app (macOS, Windows, Linux) with a standalone CLI and Web UI, also installable via npm on Node.js 22.13.0 or later. An agent works over papers and project data, with Python/R notebooks, Zotero import, literature screening and a Provenance view of inputs, code and execution history. Completed sessions export as portable read-only .science packages that others can import and replay.

- **+** Exports sessions as .science packages; imports are read-only and run no code or credentials
- **+** Provenance view shows inputs, code and execution history per figure or table version
- **+** Installers for macOS, Windows, Linux (x64/ARM64), plus Homebrew, npm and standalone CLI
- **+** Benchmark results published with caveats that they are local runs
- **−** Benchmark scores are AIPOCH's own local runs, not official leaderboard submissions
- **−** Rerunning an imported result needs a complete recipe, inputs and an available runtime
- **−** Remote Web sessions cannot read or write arbitrary local package paths
- **−** Research narration requires a separately installed local voice model

<sub>Needs Node.js 22.13.0+ (npm install only), Python or R (optional, for notebooks) · Models: Codex subscriptions, Claude, DeepSeek, Gemini, configurable provider via API key and endpoint · [Repo](https://github.com/aipoch/open-science) · [▶️ Demo ↗](https://www.youtube.com/watch?v=to_BhE5DDMw) · [📖 Docs ↗](https://aipoch.com/docs/guides/research-packages/) · [🌐 Site ↗](https://aipoch.com/open-science) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-science/)</sub>

<a name="smartsub"></a>
### #&#8288;32 [smartsub](https://github.com/buxuku/smartsub) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Nov 2026</sub>

**Desktop app for subtitle transcription, translation, dubbing and burn-in.**

SmartSub is an Electron desktop app that runs a subtitle pipeline: download online video, transcribe locally (whisper.cpp, faster-whisper, FunASR, Qwen3-ASR, FireRedASR, Parakeet), translate, proofread, dub with TTS and voice cloning, then burn or mux subtitles with ffmpeg. It has an in-app AI assistant and exposes 111 MCP tools and a smartsub CLI so external agents or scripts can drive the same pipeline.

- **+** Full local path: transcription, TTS, voice cloning and ffmpeg burn-in need no API key
- **+** Seven local transcription engines switchable per task, plus 9 optional cloud ASR providers
- **+** 111 MCP tools and a smartsub CLI with headless daemon for Cursor, Claude Code, Codex, CI
- **+** GPU acceleration via CUDA, Vulkan or Core ML/Metal, with CPU fallback on load failure
- **−** Intel Mac build is CPU only, no GPU acceleration
- **−** Free translation uses unofficial Youdao/Bing/Google endpoints; Edge TTS availability not guaranteed
- **−** README is primarily Chinese; English and Japanese READMEs are separate files
- **−** Desktop only; no Docker image or web server deployment

<sub>GPU optional · Needs yt-dlp, lux, Ollama (optional) · Models: whisper.cpp ggml, faster-whisper, FunASR, Qwen3-ASR, FireRedASR · [Repo](https://github.com/buxuku/smartsub) · [🌐 Site ↗](https://smartsub.linxiaodong.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/smartsub/)</sub>

<a name="go-stock"></a>
### #&#8288;33 [go-stock](https://github.com/arvinlovegood/go-stock) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · GPL-3.0 · Nov 2026</sub>

**Desktop stock analysis app with LLM agents for A-share, HK and US markets.**

go-stock is a Wails and NaiveUI desktop app that combines A-share, Hong Kong and US market data with LLM-driven analysis. It includes K-line charting with technical indicators, an AI agent with 150+ data tools, MCP extensions, a knowledge base, prompt and recommendation backtesting, and Feishu/DingTalk push alerts. Models connect through OpenAI-compatible APIs, Ollama, LM Studio and Chinese providers. The UI and docs are in Chinese.

- **+** Agent modes React, PlanExecute and DeepAgents, with 150+ built-in market data tools and MCP support
- **+** Works with local models (Ollama, LM Studio) and many OpenAI-compatible or Chinese cloud providers
- **+** Backtests prompt templates and AI recommendations against historical data and the CSI 300 benchmark
- **+** Pushes alerts to Feishu and DingTalk; signal monitor runs in the background
- **−** Developed mainly on Windows 10+; other platforms untested or have limited features
- **−** README and UI are Chinese-only; market data is focused on China-centric sources
- **−** Background signal monitor and market news sync require paid VIP2 sponsorship
- **−** Project is stated as entertainment only; AI output is not investment advice

<sub>GPU optional · Needs Edge browser for news scraping, LLM provider or local Ollama/LM Studio · Models: OpenAI-compatible, Ollama, LM Studio, AnythingLLM, DeepSeek · [Repo](https://github.com/arvinlovegood/go-stock) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/go-stock/)</sub>

<a name="youdub-webui"></a>
### #&#8288;34 [youdub-webui](https://github.com/liuzhao1225/youdub-webui) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Nov 2026</sub>

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

<a name="ipollowork"></a>
### #&#8288;35 [ipollowork](https://github.com/devin-axis/ipollowork) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (50) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · custom license · Nov 2026</sub>

**Desktop workbench running OpenCode, Codex or DeepSeek Harness agents on shared projects.**

iPolloWork is an Electron desktop app written in TypeScript that puts several agent engines behind one project workspace. OpenCode is the default local runtime, with Codex and DeepSeek Harness as optional adapters. It manages plugins, Skills, tasks and schedules through one lifecycle, and keeps generated documents, decks, designs and video editable. An optional iPolloCloud service handles accounts and organizations.

- **+** One UI over OpenCode, Codex and DeepSeek Harness via a shared engine protocol
- **+** Installers for macOS, Windows and Linux on both x64 and ARM64
- **+** Works locally without an account; the Cloud connection is optional
- **+** ipollowork-ui-mcp lets external MCP clients drive the desktop
- **−** Source-available license, not OSI open source; three or more users need written authorization
- **−** Hosting, SaaS or customer-facing use requires prior written authorization
- **−** Building from source needs Node 22, pnpm 11 and Bun 1.3.10 or newer
- **−** DeepSeek Harness support targets a developer preview and may change between releases

<sub>Needs OpenCode (sidecar), Node.js 22+, pnpm 11, Bun 1.3.10+, Codex (optional), DeepSeek Harness (optional), iPolloCloud (optional) · Models: OpenCode providers, Codex, DeepSeek Harness · [Repo](https://github.com/devin-axis/ipollowork) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ipollowork/)</sub>

<a name="chaterm"></a>
### #&#8288;36 [chaterm](https://github.com/chaterm/chaterm) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · custom license · Nov 2026</sub>

**AI-native SSH terminal that plans and runs ops tasks across servers and Kubernetes.**

Chaterm is an Electron terminal app for macOS, Windows and Linux, with iOS and Android clients, that adds an agent to SSH sessions. The agent plans and runs multi-host tasks such as deployment and fault diagnosis, with audit logs and rollback. It also includes a knowledge base with hybrid vector and keyword retrieval, reusable agent skills, and a database workspace for MySQL, PostgreSQL, SQLite and Oracle.

- **+** Agent works across multiple hosts and Kubernetes clusters, with audit trail and rollback
- **+** Reusable agent skills package ops procedures for repeat use
- **+** Knowledge base uses hybrid vector and keyword retrieval with RRF fusion and reranking
- **+** Built-in database client for MySQL, PostgreSQL, SQLite and Oracle
- **−** License is not identified (NOASSERTION), so reuse terms need checking
- **−** Parts of the agent system are adapted from Cline
- **−** Default reranking models are cloud-hosted (Qwen-Plus, Gemini 2.5 Flash)
- **−** Building from source needs Electron and native module rebuilds for better-sqlite3

<sub>no GPU · Needs Electron, Node.js, LLM API provider · Models: custom models with per-model context and max output limits, Qwen-Plus, Gemini 2.5 Flash · [Repo](https://github.com/chaterm/chaterm) · [📖 Docs ↗](https://chaterm.ai/docs/) · [🌐 Site ↗](https://chaterm.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chaterm/)</sub>

<a name="local-studio"></a>
### #&#8288;37 [local-studio](https://github.com/sybil-solutions/local-studio) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Oct 2026</sub>

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

<a name="digup"></a>
### #&#8288;38 [digup](https://github.com/arahim3/digup) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · MIT · Oct 2026</sub>

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

<a name="oh-my-ppt"></a>
### #&#8288;39 [oh-my-ppt](https://github.com/arcsin1/oh-my-ppt) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Nov 2026</sub>

**Desktop app that generates editable HTML slide decks and exports to PPTX.**

Oh My PPT is an Electron and React desktop app that has an LLM plan an outline, style and layout, then produces HTML slides you can edit visually or by chat. It imports existing PPTX files and exports editable PPTX, PDF, PNG and MP4. Sessions and assets are stored locally, and requests go to whichever text or image provider you configure.

- **+** Imports PPTX and exports editable PPTX, plus PDF, PNG, long PNG and MP4
- **+** Slides are HTML: drag, resize, per-element animation, and per-page chat edits
- **+** Works with any OpenAI-compatible endpoint, including local Ollama
- **+** Ships 90+ style skills, version history with rollback, and a template library
- **−** README is mainly in Chinese; the English version is a separate file
- **−** Release builds may be unsigned, so macOS and Windows show security warnings
- **−** Image generation needs a separate verified provider; Ollama covers text only
- **−** README recommends 14B+ models; PPTX fidelity drops on complex charts and tables

<sub>no GPU · Needs Text LLM API or local Ollama, Image generation provider (optional) · Models: OpenAI-compatible APIs, Ollama, DeepSeek, Kimi, Qwen · [Repo](https://github.com/arcsin1/oh-my-ppt) · [📖 Docs ↗](https://www.ohmyppt.cc/#/help) · [🌐 Site ↗](https://www.ohmyppt.cc) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/oh-my-ppt/)</sub>

<a name="pagekin"></a>
### #&#8288;40 [pagekin](https://github.com/ethanyoq/pagekin) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · GPL-3.0 · Nov 2026</sub>

**Desktop app for writing novels chapter by chapter with your own LLM.**

Pagekin (formerly AI Novel Writer) is a Windows and macOS desktop app that takes a novel through settings, architecture, chapter blueprints, drafting, review, revision and finalization. Works are stored locally in SQLite, and generation uses your own OpenAI-compatible or Gemini API key, or a local Ollama model. It can also import .txt, .md or .epub novels for style analysis or continuation, and load prompt-only SKILL.md writing rules.

- **+** Works stored in a local folder plus SQLite database
- **+** Revisions shown as per-paragraph diffs instead of overwriting the draft
- **+** Each chapter prompt uses blueprint, characters, worldbuilding and summaries, not full chat history
- **+** Presets for DeepSeek, OpenAI, Gemini, xAI and Ollama via OpenAI-compatible /v1
- **−** No bundled model; needs your own API key or local Ollama
- **−** Only OpenAI-compatible and Gemini protocols; Anthropic and Azure need separate adapters
- **−** Windows installer unsigned; macOS builds not notarized and no auto-update there
- **−** Assistant chat hidden in 1.3.0; batch writing capped at 10 chapters per run

<sub>GPU optional · Needs LLM API key or Ollama, Embedding model (optional, for semantic search), Node.js 22.14+ and pnpm (source build only) · Models: OpenAI-compatible Chat Completions, Google Gemini, DeepSeek, SiliconFlow, BigModel · [Repo](https://github.com/ethanyoq/pagekin) · [▶️ Demo ↗](https://www.orz.md/ai-novel-writer/demo/) · [🌐 Site ↗](https://www.orz.md/ai-novel-writer/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pagekin/)</sub>

<a name="craft-agents-oss"></a>
### #&#8288;41 [craft-agents-oss](https://github.com/craft-ai-agents/craft-agents-oss) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (48) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Nov 2026</sub>

**Electron desktop client for Claude and Pi agents with MCP and API sources.**

Craft Agents is an Electron desktop app, built on the Claude Agent SDK and Pi SDK, that manages agent sessions in an inbox with status workflow, permission modes and per-workspace skills. Sources (MCP servers, REST APIs, local files) are configured by asking the agent. It can also run as a headless WebSocket server on port 9100 with a desktop thin client, a CLI and a browser UI.

- **+** Connects to stdio and remote MCP servers, REST APIs and local files, configured by prompting the agent
- **+** Three permission modes (Explore, Ask to Edit, Auto) switchable with Shift+Tab
- **+** Headless server with token auth and optional TLS, plus a scriptable CLI client
- **+** Multiple providers: Anthropic, Google AI Studio, ChatGPT and Copilot OAuth, OpenRouter, Ollama
- **−** Ollama and OpenRouter are reached through the Anthropic-style custom endpoint, not native connections
- **−** Slack and Microsoft OAuth need credentials baked into source builds
- **−** Google sources require creating your own Google Cloud OAuth client
- **−** Docker run command names an image, but the README gives no build or pull steps

<sub>no GPU · Docker · Needs Bun, Electron, LLM provider API key or OAuth login · Models: Anthropic Claude, OpenAI, Google Gemini, GitHub Copilot, OpenRouter · port 9100 · [Repo](https://github.com/craft-ai-agents/craft-agents-oss) · [🌐 Site ↗](https://thecraftagents.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/craft-agents-oss/)</sub>

<a name="agentero"></a>
### #&#8288;42 [agentero](https://github.com/poco-ai/agentero) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · MIT · Nov 2026</sub>

**Desktop reference manager and PDF reader that connects local agents over ACP and MCP.**

Agentero is a desktop app for managing research papers, with a PDF reader, annotations, a Markdown notes editor with [[wiki links]], and translation. It converts formulas, algorithms and tables to Markdown and LaTeX for model context, and connects local agents such as Claude Code, OpenCode or Codex through the Agent Client Protocol. It also runs as an MCP server and ships a headless CLI. It imports Zotero libraries.

- **+** Connects local agents via ACP, including Claude Code, OpenCode and Codex
- **+** Exposes the paper library as an MCP server and through a headless CLI
- **+** Stores papers and notes as plain PDF and Markdown files in local folders
- **+** Imports a full Zotero database and exports BibTeX/BibLaTeX
- **−** README is Chinese-first; English docs are in a separate README.en.md
- **−** Agent features need a separately installed ACP-compatible agent
- **−** No Docker or web deployment; remote library access goes through an SSH tunnel
- **−** Built-in translation channels are unspecified; custom ones need your own API key

<sub>no GPU · Needs ACP-compatible agent (e.g. Claude Code, OpenCode, Codex), webkit2gtk 4.1 on Linux (Ubuntu 22.04+), S3-compatible storage (optional sync) · Models: Any agent via ACP, Local models via ACP agents · [Repo](https://github.com/poco-ai/agentero) · [📖 Docs ↗](https://agentero-docs.poco-ai.com) · [🌐 Site ↗](https://agentero.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentero/)</sub>

<a name="everroom"></a>
### #&#8288;43 [everroom](https://github.com/nxcoreai/everroom) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · custom license · Sep 2026</sub>

**Electron desktop workspace that groups files, memory and agents into project Rooms.**

Everroom is an Electron + React desktop app backed by a local Fastify gateway and SQLite storage. It ingests files, repos, audio and connected apps as versioned evidence, organizes them into per-project Context Rooms with a wiki and layered memory (L0-L3), and runs scoped Agent sessions that edit versioned documents through reviewable operations. The default agent runtime is a fake one; a real model requires configuring an OpenAI-style provider.

- **+** Data, indexes and documents stored locally in SQLite and content-addressed objects by default
- **+** Agents get Room-scoped tools only, with cancellation and reviewable document edits
- **+** Exposes a bearer-protected MCP documents endpoint and OpenAPI docs on the local gateway
- **+** Optional services degrade to explicit fallback states without blocking local documents
- **−** macOS is the development target; Windows installer is unsigned and needs a Rust toolchain
- **−** APIs, storage schemas and agent contracts may change during development
- **−** Memory and knowledge features depend on separate local services and model credentials
- **−** README says Apache-2.0 but detected license is NOASSERTION; verify before use

<sub>no GPU · Needs Node.js 22+, pnpm 11, MemoryCore (optional), Knowledge service (optional), OpenConnector (optional), Nango (optional) · Models: OpenAI-compatible APIs via Pi runtime, OpenAI Responses API · [Repo](https://github.com/nxcoreai/everroom) · [🌐 Site ↗](https://r.nxcore.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/everroom/)</sub>

<a name="ohmygame"></a>
### #&#8288;44 [ohmygame](https://github.com/whitetowerai/ohmygame) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Nov 2026</sub>

**Desktop studio where an AI agent designs, builds and playtests games.**

OhMyGame is an Electron desktop app (TypeScript) that runs the Pi coding agent against a canvas of design docs, images, video, 3D models and audio. The agent writes web games (Three.js, React Three Fiber, Phaser) or interactive stories, plays them in a live preview, and can publish a shareable link. It works with 40+ model providers using your own keys, plus Claude Code, Codex and OpenCode.

- **+** Agent playtests the running game and retries fixes, including canvas and WebGL games
- **+** Bring your own keys: 40+ providers via Pi, or Claude Code, Codex, OpenCode
- **+** Plugins for Godot, Unity, Unreal, Cocos Creator, Blender, Aseprite and Tiled
- **+** Projects are plain files (web project, Markdown, JSON), so they open in any editor
- **−** Beta; README warns of rough edges
- **−** Installers only for macOS Apple silicon and Windows x64; Linux and Intel Mac planned
- **−** Windows build is not code-signed, so SmartScreen warns on install
- **−** Media generation needs separate provider accounts; release builds send telemetry

<sub>no GPU · Needs Bun 1.4.2+ (source build), Node.js 22.19+ (source build), Model provider API key or subscription sign-in · Models: Anthropic, OpenAI, Google, DeepSeek, Qwen · [Repo](https://github.com/whitetowerai/ohmygame) · [📖 Docs ↗](https://github.com/WhiteTowerAI/ohmygame/blob/main/docs/README.md) · [🌐 Site ↗](https://ohmygame.ai/download/mac) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ohmygame/)</sub>

<a name="baocut"></a>
### #&#8288;45 [baocut](https://github.com/jimliu/baocut) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · custom license · Nov 2026</sub>

**Desktop video editor that coding agents drive through a CLI and MCP.**

BaoCut is an Electron desktop video editor with a local Runtime, a `baocut` CLI, an MCP server and an installable agent skill sharing one tool catalog. Agents such as Claude Code or Codex transcribe, subtitle, translate, dub and cut footage, leaving an editable timeline that a human can review in the app or browser. Transcription, TTS and image generation run on local models or on configured API providers.

- **+** Agent and human edit the same timeline with shared undo, not a flat MP4
- **+** Local Whisper, Qwen3-ASR, HTDemucs, Real-ESRGAN and RIFE, plus many API providers
- **+** CLI, MCP server and skill expose one documented tool catalog
- **+** Exports MP4, SRT/WebVTT and a portable .baocut bundle
- **−** Agent features need a signed-in engine such as Codex CLI or Claude Code
- **−** ffmpeg and ffprobe are not bundled and must be installed separately
- **−** Installers only for Apple Silicon macOS and Windows x64; no Linux installer
- **−** Windows packages are unsigned

<sub>GPU optional · Needs ffmpeg, ffprobe, Codex CLI or Claude Code (agent engine) · Models: Whisper large-v3, Qwen3-ASR, HTDemucs, Qwen3-TTS, Qwen-Image · [Repo](https://github.com/jimliu/baocut) · [🌐 Site ↗](https://baocut.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/baocut/)</sub>

<a name="tutti"></a>
### #&#8288;46 [tutti](https://github.com/tutti-os/tutti) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · Apache-2.0 · Oct 2026</sub>

**Desktop workspace where Claude Code, Codex and Hermes share context and files.**

Tutti is a GUI desktop app that connects existing coding agents (Claude Code, Codex, Hermes) so they share conversations, files, running tasks and app outputs instead of relying on manual handoffs. It adds an app center (image canvas, docs, slides, prototype design), @-references across agents, goal-to-task breakdown and a control center for approvals. It reuses your agent subscriptions; multi-user rooms exist only in the separate Tutti VM edition.

- **+** Agents from different providers share context via @ references to past chats, files and tasks
- **+** Runs on your existing Claude Code, Codex and Hermes subscriptions
- **+** Built-in apps (image canvas, docs, slides, prototype design) usable by you or by agents
- **+** GUI-only workflow with a control center for approvals and running tasks
- **−** Group chat, multi-user rooms and cross-device sync are only in Tutti VM, which needs an invite code
- **−** Supported agents are limited to Claude Code, Codex and Hermes; OpenClaw is still in development
- **−** Depends on third-party agent subscriptions; built-in Tutti Agent may become usage-billed
- **−** Desktop downloads for macOS and Windows only; no Docker or server deployment listed

<sub>Needs Claude Code, Codex or Hermes subscription · Models: Claude Code, Codex, Hermes, Tutti Agent · [Repo](https://github.com/tutti-os/tutti) · [🌐 Site ↗](https://tutti.sh/en?tc=25q) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tutti/)</sub>

<a name="liveagent"></a>
### #&#8288;47 [liveagent](https://github.com/stack-cairn/liveagent) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · MIT · Nov 2026</sub>

**Tauri desktop agent with local file and shell tools, MCP and a browser gateway.**

LiveAgent is a Tauri 2 desktop client that talks to Claude, Codex and Gemini protocol endpoints (custom Base URL supported). The model can read and edit files, run Bash and supervise long-running processes on your machine. It also supports stdio and http MCP servers, Skills packages, SQLite-backed memory and cron-style tasks. An optional Go gateway lets you control the desktop agent from a browser.

- **+** Desktop app works standalone; the gateway is only needed for browser access
- **+** Bridges stdio and http MCP servers and loads Skills packages on demand
- **+** Sub-agents run in parallel with worktree isolation and automatic merging
- **+** Installers for macOS (x64, arm64), Windows (exe, msi, portable) and Linux (AppImage, deb, rpm)
- **−** Models are reached via Claude, Codex and Gemini protocols; local model runtimes are not mentioned
- **−** LLM layer is a bundled K-brain executable; the README does not describe it
- **−** Linux builds are x86_64 only and need WebKitGTK 4.1
- **−** Remote access means hosting the gateway and setting up a reverse proxy for TLS

<sub>no GPU · Docker · Needs Docker (gateway only), WebView2 (Windows), WebKitGTK 4.1 (Linux) · Models: Anthropic Claude protocol, OpenAI Codex protocol, Google Gemini protocol, custom Base URL compatible services · port 3000 · [Repo](https://github.com/stack-cairn/liveagent) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/liveagent/)</sub>

<a name="beav"></a>
### #&#8288;48 [beav](https://github.com/jamailar/beav) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · custom license · Nov 2026</sub>

**Desktop workspace for social-media creators: research, drafting, image and video editing.**

Beav is a Tauri and Rust desktop app for solo creators and small teams. It saves links from Xiaohongshu, Douyin, Bilibili and others into a local knowledge base with auto transcription, then drafts posts using per-account memory, generates images from templates, and cuts spoken-word video in a built-in multi-track editor. The public source is frozen at 2.5.0; the maintained release is a separate codebase.

- **+** Covers collection, drafting, image generation and video editing in one app
- **+** Per-account spaces keep positioning, style and published posts as long-term memory
- **+** Connects Codex, Claude Code and Cursor via MCP config that Beav writes for you
- **+** Accepts OpenAI-compatible providers or local models; macOS, Windows and Linux builds
- **−** Open-source code is stuck at 2.5.0 and differs from the current release
- **−** MIT Non-Commercial license; commercial use needs written permission from the author
- **−** README and UI are Chinese only, and supported platforms are mostly Chinese
- **−** No Docker or compose files; server use is only via a Linux build

<sub>Needs Chrome or Edge extension (optional) · Models: OpenAI-compatible APIs, local models, official hosted AI · [Repo](https://github.com/jamailar/beav) · [🌐 Site ↗](https://beav.pro/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/beav/)</sub>

<a name="codex-desktop-linux"></a>
### #&#8288;49 [codex-desktop-linux](https://github.com/ilysenko/codex-desktop-linux) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · MIT · Nov 2026</sub>

**Community repackaging of OpenAI's Linux ChatGPT desktop app with optional add-ons.**

Verifies OpenAI's signed Linux ChatGPT .deb, patches resources/app.asar minimally, and builds deb, RPM, pacman, AppImage and Nix outputs under the name ChatGPT Community (codex-desktop). It adds a framework of disabled-by-default Linux features such as global dictation, Wayland shortcuts, profile isolation and tray start, plus a guided GTK installer and an update manager.

- **+** Verifies the upstream package through a signed chain: pinned key, InRelease, Packages, SHA-256
- **+** Builds deb, RPM, pacman, AppImage, Nix and a local Gentoo ebuild
- **+** Official ELF runtime and bundled tools are preserved byte-for-byte
- **+** Over 40 optional Linux features, all off by default, each with its own README
- **−** Unofficial; supports only the latest signed stable OpenAI package, on amd64 and arm64
- **−** Builds locally and needs Node.js 20+, Python 3, a C/C++ toolchain and Rust
- **−** Shares the upstream Codex profile with the official app unless profile isolation is enabled
- **−** Sends an anonymous daily launch ping to GoatCounter unless disabled by environment variable

<sub>Needs Node.js 20+, npm, Python 3, curl, gpgv, dpkg-deb, Rust, C/C++ toolchain, OpenAI signed Linux ChatGPT .deb · Models: OpenAI ChatGPT/Codex, API-key compatible providers · [Repo](https://github.com/ilysenko/codex-desktop-linux) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/codex-desktop-linux/)</sub>

<a name="open-cowork"></a>
### #&#8288;50 [open-cowork](https://github.com/opencoworkai/open-cowork) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: fair (51) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · MIT · Oct 2026</sub>

**Electron desktop agent that edits files and builds Office documents.**

Open Cowork is an Electron app for Windows and macOS that runs an agent over a chosen workspace folder. It generates PPTX, DOCX, XLSX and PDF files through built-in skills, connects to MCP servers, and accepts remote commands from Feishu or Slack. Shell commands run inside a WSL2 or Lima VM when one is installed, and otherwise natively with path restrictions.

- **+** Optional VM isolation: WSL2 on Windows, Lima on macOS, auto-detected for shell commands
- **+** Built-in skills for PPTX, DOCX, XLSX and PDF, plus a skill-creator for custom ones
- **+** Works with Anthropic, OpenRouter, GLM, MiniMax, Kimi and other OpenAI-compatible endpoints
- **+** MCP connectors and GUI automation, with remote control from Feishu (Lark)
- **−** No Linux installer; Linux users must build from source
- **−** Without WSL2 or Lima, commands run natively with only path-based restrictions
- **−** Needs a third-party API key; no bundled local model runtime
- **−** Roadmap lists a stable release as upcoming, so it is not yet stable

<sub>no GPU · Needs Node.js 18+ (build from source), WSL2 (Windows, optional), Lima (macOS, optional), LLM API key · Models: Claude, OpenAI-compatible APIs, OpenRouter, GLM, MiniMax · [Repo](https://github.com/opencoworkai/open-cowork) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-cowork/)</sub>

<a name="ultimatevocalremovergui"></a>
### #&#8288;51 [ultimatevocalremovergui](https://github.com/anjok07/ultimatevocalremovergui) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: widely used (85) · Freshness: recent (70) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · MIT · Oct 2026</sub>

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

<a name="5ire"></a>
### #&#8288;52 [5ire](https://github.com/nanbingxyz/5ire) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (31) · Freshness: active (95) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · custom license · Nov 2026</sub>

**Desktop chat app and MCP client with local knowledge base.**

5ire is a TypeScript desktop app that chats with models from OpenAI, Azure, Anthropic, Google, Mistral, Doubao, Grok, DeepSeek and Ollama. It works as an MCP client, so models can call tools from MCP servers. It also has a local knowledge base that embeds docx, xlsx, pptx, pdf, txt and csv files with bge-m3 for RAG.

- **+** MCP client with tools and prompts support, plus a linked MCP server directory
- **+** Local RAG over docx, xlsx, pptx, pdf, txt and csv using bge-m3 embeddings
- **+** Nine named providers, including Ollama for local models
- **+** Usage and spend analytics, prompt library with variables, bookmarks, and search
- **−** MCP tools need Python, Node.js and uv installed separately
- **−** Native dependencies mean builds must be packaged on each target platform
- **−** License is reported as NOASSERTION, so terms need checking before reuse
- **−** Desktop app only; no Docker or web deployment for multi-user hosting

<sub>Needs Python, Node.js, uv · Models: OpenAI, Azure, Anthropic, Google, Mistral · [Repo](https://github.com/nanbingxyz/5ire) · [🌐 Site ↗](https://5ire.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/5ire/)</sub>

<a name="enchanted"></a>
### #&#8288;53 [enchanted](https://github.com/gluonfield/enchanted) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: known (37) · Freshness: active (90) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Jul 2026</sub>

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
### #&#8288;54 [noi](https://github.com/lencx/noi) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (57) · Freshness: active (90) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 9.1k · no license · Aug 2026</sub>

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

<a name="b"></a>
### #&#8288;55 [b](https://github.com/ahmadhassan-bted/b) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (30) · Freshness: active (86) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · MIT · Jul 2026</sub>

**Proactive desktop companion that reads your screen and speaks.**

B is a PyQt6 desktop overlay with an animated face. It reads the active window through Windows UI Automation, with Tesseract OCR as a fallback. It sends that context to Groq's cloud API or a local llama-cpp model, and replies by voice (Piper TTS) and chat bubble. Speech input uses Faster-Whisper, and a work mode lets it offer suggestions unprompted.

- **+** Supports both Groq cloud inference and local llama-cpp models
- **+** Screen context via UIA tree walking, with OCR fallback for incompatible apps
- **+** Voice loop: Faster-Whisper input with VAD, Piper TTS output
- **+** Global kill switch registered at Win32 level for instant exit
- **−** Windows 10/11 is the primary target; Linux and macOS are experimental
- **−** UIA screen reading is Windows-specific, so context is weaker elsewhere
- **−** No window close button; the hotkey is the only way to exit
- **−** No tagged releases; README lists status as active development

<sub>RAM ≥ 16 GB · GPU optional · Needs Groq API key, Tesseract OCR, Piper ONNX voices, Faster-Whisper · Models: Groq API, llama-cpp GGUF · [Repo](https://github.com/ahmadhassan-bted/b) · [▶️ Demo ↗](https://raw.githubusercontent.com/Ahmad-Hassan-0/B---desktop-companion/main/docs/assets/demo-video.mp4) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/b/)</sub>

<a name="minecontext"></a>
### #&#8288;56 [minecontext](https://github.com/volcengine/minecontext) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: known (33) · Freshness: recent (65) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.5k · Apache-2.0 · May 2026</sub>

**Desktop app that screenshots your screen and generates summaries and to-dos.**

MineContext is an Electron desktop app with a Python FastAPI backend that captures periodic screenshots, interprets them with a vision-language model, and stores the results in SQLite and ChromaDB. It generates daily and weekly summaries, to-dos and activity records in the background, and offers chat over the collected context. Models come from Doubao, OpenAI, or any OpenAI-compatible endpoint, including local ones such as LM Studio.

- **+** Data stored locally by default; works with any OpenAI-compatible local model endpoint
- **+** Installers for macOS (.dmg) and Windows (.exe); macOS builds are Apple-notarized
- **+** Backend debug page shows token usage and lets you edit task intervals and system prompts
- **+** Backend runs standalone via `uv run opencontext start` with a YAML config
- **−** Only screenshots and note editing are marked done; file upload, link upload, meetings are planned
- **−** Needs a vision-language model and an embedding model; recommended setup uses Doubao cloud API
- **−** Screenshots are sent to the configured model provider unless a local model is used
- **−** First run installs the backend environment, taking about two minutes

<sub>Needs SQLite, ChromaDB, uv, Doubao, OpenAI or OpenAI-compatible API · Models: Doubao, OpenAI, OpenAI-compatible local models (LM Studio) · port 1733 · [Repo](https://github.com/volcengine/minecontext) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/minecontext/)</sub>

<a name="my-translator"></a>
### #&#8288;57 [my-translator](https://github.com/phuc-nt/my-translator) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (1) · Freshness: active (91) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Jul 2026</sub>

**Real-time speech translation overlay for system audio and mic on macOS and Windows.**

Tauri 2 desktop app that captures system audio or microphone input, transcribes and translates it live, and shows the result in a minimal overlay. It supports four engines: Soniox, OpenAI Realtime, Qwen LiveTranslate Flash, and an offline MLX mode (Whisper + Gemma) on Apple Silicon. The app talks directly to the APIs you configure, with no relay server; optional TTS narration is available.

- **+** Four engines, including a fully offline MLX mode on Apple Silicon
- **+** Two-way translation with speaker detection for Zoom, Meet and Teams calls
- **+** Direct API calls with local keys; no account, telemetry or relay server
- **+** Custom term glossary and three TTS providers (Edge, Google, ElevenLabs)
- **−** Local mode is experimental, Apple Silicon only, about 10 s latency
- **−** Local mode covers only JA/EN/ZH/KO to VI/EN
- **−** OpenAI Realtime costs about $4/hr and disables two-way mode and custom TTS
- **−** Qwen engine needs explicit source language and Singapore-region key; no source transcript

<sub>GPU optional · Needs Soniox API key, OpenAI API key, Alibaba DashScope API key, Edge TTS / Google Cloud TTS / ElevenLabs (optional) · Models: Soniox, OpenAI gpt-realtime-translate, qwen3-livetranslate-flash-realtime, MLX Whisper + Gemma · [Repo](https://github.com/phuc-nt/my-translator) · [📖 Docs ↗](https://github.com/phuc-nt/my-translator/blob/main/docs/installation_guide.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/my-translator/)</sub>

<a name="aichat"></a>
### #&#8288;58 [aichat](https://github.com/sigoden/aichat) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: popular (63) · Freshness: quiet (30) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Feb 2026</sub>

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

<a name="surf"></a>
### #&#8288;59 [surf](https://github.com/deta/surf) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: niche (18) · Freshness: recent (78) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · May 2026</sub>

**Desktop AI notebook that combines local files, web pages and notes.**

Surf is an Electron desktop app (Svelte, TypeScript, Rust) for MacOS, Windows and Linux. It keeps a local library of files, links, YouTube videos and PDFs in an open format (SFFS), and generates notes from @-mentioned tabs or resources with citations linked to the source. It can also run web searches and generate small interactive apps called Surflets, using your own API key, a cloud model or a local model.

- **+** Library stored locally in open formats (SFFS), partly usable offline
- **+** Citations link to a webpage section, video timestamp or PDF page
- **+** Accepts bring-your-own-key, cloud or local language models
- **+** Runs on MacOS, Windows and Linux under Apache-2.0
- **−** Desktop Electron app only; no Docker or server deployment for multi-user use
- **−** Deta name and logos are excluded from the Apache-2.0 license
- **−** Supported models and local runtimes are only documented on a linked page
- **−** README gives no sandboxing details for generated Surflet apps

<sub>Models: bring-your-own API key, cloud models, local language models · [Repo](https://github.com/deta/surf) · [🌐 Site ↗](https://deta.surf) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/surf/)</sub>

<a name="open-claude-cowork"></a>
### #&#8288;60 [open-claude-cowork](https://github.com/composio-community/open-claude-cowork) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (24) · Freshness: recent (62) · Maintenance: weak (0) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · May 2026</sub>

**Electron desktop chat app on Claude Agent SDK with Composio app integrations.**

Electron desktop chat client with a Node/Express backend that runs the Claude Agent SDK, or optionally the Opencode SDK, and streams responses over SSE. It reaches 500+ apps (Gmail, Slack, GitHub, Google Drive) through Composio Tool Router and MCP, and loads custom skills from .claude/skills/. The repo also bundles Secure Clawdbot, a separate messaging bot for WhatsApp, Telegram, Signal and iMessage.

- **+** Tool inputs and outputs are shown in a sidebar during streaming responses
- **+** Loads custom SKILL.md files from .claude/skills/
- **+** Opencode SDK provider is available alongside the Claude Agent SDK
- **+** Includes a messaging bot with memory, browser automation and scheduled reminders
- **−** Requires an Anthropic API key and a Composio API key; no local model path described
- **−** Needs a separate backend started in its own terminal before the app
- **−** No Docker image or packaged release; setup is clone and run setup.sh
- **−** Integrations depend on the hosted Composio service

<sub>no GPU · Needs Anthropic API key, Composio API key, Opencode API key (optional), Node.js, Electron · Models: Claude (Claude Agent SDK), Opencode SDK models · port 3001 · [Repo](https://github.com/composio-community/open-claude-cowork) · [📖 Docs ↗](https://docs.composio.dev/tool-router/overview) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-claude-cowork/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
