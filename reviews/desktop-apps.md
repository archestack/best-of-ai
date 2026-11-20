# 🖥️ Desktop AI apps reviews · Best of Open-Source AI

Apps you install on your own computer to chat with local or API models, often with document chat and agents built in. Back to the [leaderboard](../README.md#%EF%B8%8F-desktop-ai-apps).

<sub>🌐 Also on the web: [Desktop AI apps on archestack.com](https://archestack.com/best-of-ai/desktop-apps/), each project on its own page.</sub>

<a name="cherry-studio"></a>
### 🥇 [cherry-studio](https://github.com/cherryhq/cherry-studio) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 54k · AGPL-3.0 · Nov 2026</sub>

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
### 🥈 [screenpipe](https://github.com/screenpipe/screenpipe) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · custom license · Nov 2026</sub>

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

<sub>RAM ≥ 8 GB · GPU optional · Needs Node.js (npx CLI), Ollama (optional local LLM), Deepgram (optional cloud transcription) · Models: Whisper Large-V3-Turbo, Deepgram, Ollama, OpenAI-compatible servers · port 3030 · [Repo](https://github.com/screenpipe/screenpipe) · [📖 Docs ↗](https://docs.screenpi.pe) · [🌐 Site ↗](https://screenpi.pe) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/screenpipe/)</sub>

<a name="dsh-desktop"></a>
### 🥉 [dsh-desktop](https://github.com/anywhere-labs/dsh-desktop) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Nov 2026</sub>

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

<sub>Needs DeepSeek Harness (bundled, pinned) · Models: unknown · [Repo](https://github.com/anywhere-labs/dsh-desktop) · [📖 Docs ↗](https://github.com/anywhere-labs/dsh-desktop/blob/HEAD/docs/user-guide.md) · [🌐 Site ↗](https://dshdesktop.cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dsh-desktop/)</sub>

<a name="hermes-desktop"></a>
### #&#8288;4 [hermes-desktop](https://github.com/fathah/hermes-desktop) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

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
### #&#8288;5 [artcraft](https://github.com/storytold/artcraft) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;6 [aionui](https://github.com/iofficeai/aionui) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;7 [openwork](https://github.com/different-ai/openwork) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Nov 2026</sub>

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

<a name="prompt-optimizer"></a>
### #&#8288;8 [prompt-optimizer](https://github.com/linshenkx/prompt-optimizer) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · custom license · Nov 2026</sub>

**Prompt optimization and testing workspace with model comparison and an MCP server.**

Prompt Optimizer is a TypeScript app that rewrites system prompts, user prompts and variable templates, then tests the original and optimized versions against configured models. It adds an Arena for comparing models side by side, evaluation of results, image-prompt workspaces, and a favorites library with version history. It runs as a web app, desktop app, Chrome extension or Docker container, and exposes three tools over MCP.

- **+** Arena compares one prompt across multiple models side by side
- **+** Ships as web, desktop, Chrome extension, Docker and MCP server
- **+** App data stays in the browser or locally; model calls go to your provider
- **+** Supports Ollama and custom OpenAI-compatible endpoints via environment variables
- **−** Browser builds hit CORS limits with many providers; desktop app or proxy needed
- **−** VITE_* API keys are exposed in browser assets on public deployments
- **−** AGPL-3.0 badge, but license detected as NOASSERTION, so terms need checking
- **−** Workspace and project management is still unchecked on the roadmap

<sub>no GPU · Docker + Compose · Needs Model provider API key or local Ollama endpoint · Models: OpenAI, Gemini, DeepSeek, Grok, Zhipu AI · port 28081 · [Repo](https://github.com/linshenkx/prompt-optimizer) · [▶️ Demo ↗](https://prompt.always200.com) · [📖 Docs ↗](https://docs.always200.com) · [🌐 Site ↗](https://always200.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/prompt-optimizer/)</sub>

<a name="dsh-go"></a>
### #&#8288;9 [dsh-go](https://github.com/ccch1mneyyy/dsh-go) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · AGPL-3.0 · Nov 2026</sub>

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
### #&#8288;10 [openmausbot](https://github.com/milind-soni/openmausbot) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;11 [anarlog](https://github.com/fastrepl/anarlog) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · MIT · Nov 2026</sub>

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

<a name="deep-live-cam"></a>
### #&#8288;12 [deep-live-cam](https://github.com/hacksider/deep-live-cam) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 98k · AGPL-3.0 · Nov 2026</sub>

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
### #&#8288;13 [jan](https://github.com/janhq/jan) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 46k · custom license · Nov 2026</sub>

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

<a name="dataelement-dsh-desktop"></a>
### #&#8288;14 [dsh-desktop](https://github.com/dataelement/dsh-desktop) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Nov 2026</sub>

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

<a name="chatbox"></a>
### #&#8288;15 [chatbox](https://github.com/chatboxai/chatbox) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · GPL-3.0 · Nov 2026</sub>

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

<a name="read-frog"></a>
### #&#8288;16 [read-frog](https://github.com/mengxi-ream/read-frog) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · GPL-3.0 · Nov 2026</sub>

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

<a name="open-codesign"></a>
### #&#8288;17 [open-codesign](https://github.com/opencoworkai/open-codesign) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · MIT · Nov 2026</sub>

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
### #&#8288;18 [deepchat](https://github.com/thinkinaixyz/deepchat) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="eigent"></a>
### #&#8288;19 [eigent](https://github.com/eigent-ai/eigent) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<sub>GPU optional · Needs Node.js 18-22, npm, uv · Models: vLLM, Ollama, LM Studio, cloud APIs, enterprise gateways · [Repo](https://github.com/eigent-ai/eigent) · [🌐 Site ↗](https://www.eigent.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/eigent/)</sub>

<a name="pocketpal-ai"></a>
### #&#8288;20 [pocketpal-ai](https://github.com/a-ghorbani/pocketpal-ai) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · MIT · Nov 2026</sub>

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

<a name="lobsterai"></a>
### #&#8288;21 [lobsterai](https://github.com/netease-youdao/lobsterai) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Nov 2026</sub>

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

<a name="presenton"></a>
### #&#8288;22 [presenton](https://github.com/presenton/presenton) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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

<a name="nightly-labs-openbot"></a>
### #&#8288;23 [openbot](https://github.com/nightly-labs/openbot) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · custom license · Nov 2026</sub>

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

<a name="gallery"></a>
### #&#8288;24 [gallery](https://github.com/google-ai-edge/gallery) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · Apache-2.0 · Nov 2026</sub>

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

<a name="openworker"></a>
### #&#8288;25 [openworker](https://github.com/andrewyng/openworker) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

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

<a name="clawx"></a>
### #&#8288;26 [clawx](https://github.com/valuecell-ai/clawx) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · MIT · Nov 2026</sub>

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

<a name="koharu"></a>
### #&#8288;27 [koharu](https://github.com/koharu-rs/koharu) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.8k · Apache-2.0 · Nov 2026</sub>

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

<a name="kun"></a>
### #&#8288;28 [kun](https://github.com/kunagent/kun) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · custom license · Nov 2026</sub>

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

<a name="learnharness"></a>
### #&#8288;29 [learnharness](https://github.com/amosblomqvist/learnharness) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · AGPL-3.0 · Nov 2026</sub>

**Desktop tutoring app that plans lessons from a model of what you understand.**

LearnHarness is a desktop app (macOS Apple Silicon, Windows x64, Linux x64) where AI agents measure your current understanding, plan a dependency map to your goal, teach step by step, and run separate practice sessions. Answers and free-text "thinking" fields drive what comes next, and a persistent knowledge graph of propositions and reasoning chains carries across sessions. It uses your own provider API keys, Claude Code CLI, or an OpenAI-compatible endpoint; data is stored locally.

- **+** Persistent knowledge graph links claims to source sessions and can import notes
- **+** Works with provider keys, Claude Code CLI, or custom OpenAI-compatible endpoints including local servers
- **+** Chats, graph and settings stored locally as inspectable plain files; system prompts editable
- **+** Signed installers for three platforms with in-app updates
- **−** AGPL-3.0 license restricts use in proprietary or hosted derivatives
- **−** Web research and dictation need separate external service keys
- **−** Windows installer is unsigned and triggers SmartScreen warnings
- **−** Cost meter only estimates known API costs, not subscription, CLI or custom-endpoint charges

<sub>Needs LLM provider API key, Claude Code CLI, or OpenAI-compatible endpoint, Optional: Tavily, Brave, Exa, Firecrawl or Ollama key for web search, Optional: dictation service key · Models: Provider APIs, Claude Code CLI, Custom OpenAI-compatible endpoints, Local model servers · port 3000 · [Repo](https://github.com/amosblomqvist/learnharness) · [📖 Docs ↗](https://github.com/amosblomqvist/learnharness/blob/main/docs/README.md) · [🌐 Site ↗](https://learnharness.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/learnharness/)</sub>

<a name="open-science"></a>
### #&#8288;30 [open-science](https://github.com/aipoch/open-science) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="coopanion"></a>
### #&#8288;31 [coopanion](https://github.com/pal-ai-lab/coopanion) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · custom license · Nov 2026</sub>

**Desktop pet that chats, listens, and can operate your computer with an LLM.**

Coopanion is a desktop app for Windows, macOS and Linux that shows an animated pet, Coo, along the bottom of the screen. It talks through speech bubbles, takes push-to-talk voice input with local FunASR or Whisper recognition, and keeps memory in PARTNER.md. With permission it can take screenshots, click and type, using an API key for one of 14 listed providers or a ChatGPT sign-in.

- **+** Local speech recognition by default: FunASR (about 230 MB) or Whisper (about 360 MB)
- **+** Supports 14 listed providers including OpenAI, Anthropic, Gemini, DeepSeek, plus ChatGPT sign-in
- **+** Computer use is off by default, asks first, and pauses when you touch mouse or keyboard
- **+** Memory is plain text in PARTNER.md, with Git history of changes when Git is installed
- **−** Installers are unsigned and not notarized; Windows and macOS warn on first launch
- **−** Only DeepSeek, Anthropic and StepFun Step Plan tested with real keys
- **−** Linux runs under X11/XWayland; cursor tracking and screenshots are limited on Wayland
- **−** Needs a paid cloud API key or ChatGPT plan; no local LLM backend listed

<sub>no GPU · Needs Git (optional, for memory history), xdotool and zenity (Linux computer use), API key from a model provider or ChatGPT account · Models: OpenAI, Anthropic, Gemini, xAI, OpenRouter · [Repo](https://github.com/pal-ai-lab/coopanion) · [🌐 Site ↗](https://coo.palailab.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/coopanion/)</sub>

<a name="everywhere"></a>
### #&#8288;32 [everywhere](https://github.com/sylinko/everywhere) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · custom license · Nov 2026</sub>

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

<a name="smartsub"></a>
### #&#8288;33 [smartsub](https://github.com/buxuku/smartsub) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · MIT · Nov 2026</sub>

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

<a name="youdub-webui"></a>
### #&#8288;34 [youdub-webui](https://github.com/liuzhao1225/youdub-webui) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (50) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="ogam"></a>
### #&#8288;35 [ogam](https://github.com/off-grid-ai/ogam) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Nov 2026</sub>

**Offline mobile app for local LLM chat, image generation, vision and voice input.**

React Native app for Android, iOS and Apple Silicon Macs that runs GGUF models on-device through llama.cpp, with Whisper speech-to-text, on-device Stable Diffusion and vision models. It adds tool calling, a SQLite-backed project knowledge base, and can connect to OpenAI-compatible servers such as Ollama or LM Studio on your network. Voice replies, personas, and Calendar, email and MCP actions are in a paid Pro tier.

- **+** Runs any GGUF model on-device, with OpenCL GPU on Adreno and Metal on Apple Silicon
- **+** Covers text, Stable Diffusion images, vision, Whisper input and PDF knowledge base in one app
- **+** Can also use remote OpenAI-compatible servers (Ollama, LM Studio, LocalAI), keys stored in system keychain
- **+** Model manager shows per-model RAM use, with Lean, Balanced and Aggressive loading policies
- **−** Text-to-speech, personas, MCP and calendar/email actions require the paid Pro tier
- **−** Hexagon NPU support is experimental and only accelerates Q4_0 and Q8_0 quants
- **−** Mac support is the iOS build via Catalyst; a separate Desktop app is a different repo
- **−** Performance figures are from Snapdragon 8 Gen 2/3 and A17 Pro only

<sub>GPU optional · Models: GGUF, Stable Diffusion, Whisper, SmolVLM, Qwen3-VL · [Repo](https://github.com/off-grid-ai/ogam) · [📖 Docs ↗](https://github.com/off-grid-ai/OGAM/blob/main/docs/ARCHITECTURE.md) · [🌐 Site ↗](https://getoffgridai.co/pro/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ogam/)</sub>

<a name="go-stock"></a>
### #&#8288;36 [go-stock](https://github.com/arvinlovegood/go-stock) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · GPL-3.0 · Nov 2026</sub>

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

<a name="chaterm"></a>
### #&#8288;37 [chaterm](https://github.com/chaterm/chaterm) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · custom license · Nov 2026</sub>

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

<a name="ipollowork"></a>
### #&#8288;38 [ipollowork](https://github.com/devin-axis/ipollowork) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · custom license · Nov 2026</sub>

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

<a name="digup"></a>
### #&#8288;39 [digup](https://github.com/arahim3/digup) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Oct 2026</sub>

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

<a name="locally-uncensored"></a>
### #&#8288;40 [locally-uncensored](https://github.com/purpledoubled/locally-uncensored) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · AGPL-3.0 · Nov 2026</sub>

**Desktop app for local chat, image and video generation, and a coding agent.**

Tauri-based desktop app (TypeScript) that puts chat, a coding agent, tool-using agents, and image and video generation in one window. It uses an existing Ollama or LM Studio engine or installs one, and installs and manages ComfyUI for image and video. Optional paid LU Cloud runs larger models on hosted GPUs; local mode is free.

- **+** Installers for Windows, Linux and macOS, plus an Android APK; no Docker or config files
- **+** Installs and updates ComfyUI itself, with text-to-image, image-to-video and LoRA lanes
- **+** Coding agent shows diffs before applying; Local API is OpenAI-compatible behind a token
- **+** Agent tool calls pass a permission gate; supports your own MCP servers
- **−** macOS build is Apple Silicon only, beta, and has run on one Mac so far
- **−** Windows installer is not yet code-signed, so SmartScreen warns on first run
- **−** Voice and Computer control are beta and mainly tested on Windows
- **−** Upscale, Erase Object and the largest models need the paid cloud tier

<sub>RAM ≥ 8 GB · GPU optional · Needs Ollama or LM Studio (installed by the app if missing), ComfyUI (installed by the app) · Models: Ollama models, LM Studio models, GGUF, SDXL, FLUX · [Repo](https://github.com/purpledoubled/locally-uncensored) · [📖 Docs ↗](https://locallyuncensored.com/guide/) · [🌐 Site ↗](https://locallyuncensored.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/locally-uncensored/)</sub>

<a name="natively-cluely-ai-assistant"></a>
### #&#8288;41 [natively-cluely-ai-assistant](https://github.com/natively-ai-assistant/natively-cluely-ai-assistant) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · custom license · Nov 2026</sub>

**Desktop overlay that transcribes meetings and drafts live interview answers.**

Desktop app for macOS 12+ and Windows 10/11 that captures system and microphone audio, transcribes it, and shows LLM-written answers in an overlay hidden from screen shares. It runs on a paid Natively plan, your own API keys, or local Ollama models with on-device Whisper/Parakeet STT. Meetings are stored locally with SQLite vector search for later questions.

- **+** Fully offline option: local Ollama models plus on-device ONNX STT (Whisper, Moonshine, Parakeet)
- **+** Bring-your-own-key support across several providers, with a model picker grouped by provider
- **+** Local SQLite vector search over past meetings, plus PDF, DOCX and TXT reference files
- **+** Connectors to Gmail, Slack, Notion, Zapier, webhooks and CRMs, plus a local MCP server
- **−** Custom personal/non-commercial license, not OSI open source (detected as NOASSERTION)
- **−** Built to hide from screen shares in interviews, which may breach employer or proctoring rules
- **−** Stealth is not guaranteed; proctoring software and phone cameras can still see the user's screen
- **−** Some features (Auto Answer, answer length options) are Pro; hosted mode needs a paid plan after trial

<sub>GPU optional · Needs Ollama (optional, for local LLMs), Chrome (optional, for Browser Companion) · Models: OpenAI, Anthropic Claude, Google Gemini, Ollama local models, Sidrune AI · [Repo](https://github.com/natively-ai-assistant/natively-cluely-ai-assistant) · [🌐 Site ↗](https://heynatively.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/natively-cluely-ai-assistant/)</sub>

<a name="tgpt"></a>
### #&#8288;42 [tgpt](https://github.com/aandrew-me/tgpt) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (30) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · GPL-3.0 · Nov 2026</sub>

**Terminal client for chatting with AI providers from the command line.**

tgpt is a Go command-line client that sends prompts to a set of AI providers from the terminal. It ships as a single cross-platform binary, installable via script, Homebrew, pacman, Scoop, Chocolatey, FreeBSD ports or `go install`. HTTP and SOCKS5 proxies are configured through an environment variable or a proxy.txt file.

- **+** Single Go binary for Linux, macOS, Windows and FreeBSD
- **+** Packaged in Homebrew, pacman, Scoop, Chocolatey and FreeBSD ports
- **+** Proxy support: HTTP, HTTP auth, SOCKS5 and SOCKS5 auth
- **+** Self-update with `tgpt -u` for script installs
- **−** Client for remote providers; README does not describe running local models
- **−** Prompts go to third-party providers, so queries leave your host
- **−** Provider list and usage docs are in separate files, not the README
- **−** Terminal only, with no web UI or user accounts

<sub>no GPU · Needs Remote AI providers · [Repo](https://github.com/aandrew-me/tgpt) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tgpt/)</sub>

<a name="pagekin"></a>
### #&#8288;43 [pagekin](https://github.com/ethanyoq/pagekin) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · GPL-3.0 · Nov 2026</sub>

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

<a name="oh-my-ppt"></a>
### #&#8288;44 [oh-my-ppt](https://github.com/arcsin1/oh-my-ppt) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · Apache-2.0 · Nov 2026</sub>

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

<a name="craft-agents-oss"></a>
### #&#8288;45 [craft-agents-oss](https://github.com/craft-ai-agents/craft-agents-oss) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;46 [agentero](https://github.com/poco-ai/agentero) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · MIT · Nov 2026</sub>

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

<a name="translatebookswithllms"></a>
### #&#8288;47 [translatebookswithllms](https://github.com/hydropix/translatebookswithllms) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · AGPL-3.0 · Nov 2026</sub>

**Translates EPUB, SRT, DOCX, PDF, TXT and PGN files with local or cloud LLMs.**

TBL splits a document into token-based chunks (450 by default), sends each to an LLM, and rebuilds the file with EPUB structure and SRT timecodes intact. It runs as a downloadable app with a web UI on port 5000, plus a Python CLI. Providers include Ollama, OpenAI, Gemini, Mistral, DeepSeek, OpenRouter, Poe, NVIDIA NIM and any OpenAI-compatible endpoint.

- **+** Checkpointing lets interrupted translations resume where they stopped
- **+** Glossary and style presets, with an auto mode that derives both from the document
- **+** Nine provider options, including local Ollama and any OpenAI-compatible server
- **+** Preserves EPUB formatting and SRT timecodes; also handles PGN chess comments
- **−** PDF output is reflowed, so the original page layout is lost
- **−** No OCR, so scanned PDFs are unsupported
- **−** No user accounts; every browser on one server shares the same workspace
- **−** Refinement pass is unavailable for PDF and PGN

<sub>GPU optional · Docker + Compose · Needs Ollama (for local models), Python 3.8+ (source install) · Models: Ollama, OpenAI, Gemini, Mistral, DeepSeek · port 5000 · [Repo](https://github.com/hydropix/translatebookswithllms) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/translatebookswithllms/)</sub>

<a name="everroom"></a>
### #&#8288;48 [everroom](https://github.com/nxcoreai/everroom) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · custom license · Sep 2026</sub>

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

<a name="holaos"></a>
### #&#8288;49 [holaos](https://github.com/holaboss-ai/holaos) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: weak (27) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Nov 2026</sub>

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

<a name="tutti"></a>
### #&#8288;50 [tutti](https://github.com/tutti-os/tutti) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · Apache-2.0 · Oct 2026</sub>

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

<a name="ohmygame"></a>
### #&#8288;51 [ohmygame](https://github.com/whitetowerai/ohmygame) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Nov 2026</sub>

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

<a name="local-studio"></a>
### #&#8288;52 [local-studio](https://github.com/sybil-solutions/local-studio) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Oct 2026</sub>

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

<a name="codex-desktop-linux"></a>
### #&#8288;53 [codex-desktop-linux](https://github.com/ilysenko/codex-desktop-linux) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · MIT · Nov 2026</sub>

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

<a name="liveagent"></a>
### #&#8288;54 [liveagent](https://github.com/stack-cairn/liveagent) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · MIT · Nov 2026</sub>

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

<a name="baocut"></a>
### #&#8288;55 [baocut](https://github.com/jimliu/baocut) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · custom license · Nov 2026</sub>

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

<a name="beav"></a>
### #&#8288;56 [beav](https://github.com/jamailar/beav) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · custom license · Nov 2026</sub>

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

<a name="oterm"></a>
### #&#8288;57 [oterm](https://github.com/ggozad/oterm) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Nov 2026</sub>

**Terminal chat client for Ollama, OpenAI, Anthropic and pydantic-ai providers.**

oterm is a Python terminal client for chatting with models from Ollama, OpenAI, Anthropic, and any provider supported by pydantic-ai. It starts with `uvx oterm`. Configuration and usage details live on the external documentation site, not in the README.

- **+** Runs in the terminal, no web server or browser needed
- **+** Covers Ollama, OpenAI, Anthropic and any pydantic-ai provider
- **+** One-command start with uvx oterm
- **+** MIT licensed, with CI test and coverage badges
- **−** Terminal-only interface, no web UI or multi-user accounts
- **−** README has no feature list; details are only in external docs
- **−** Needs a separate model backend such as Ollama or an API key
- **−** No Docker or compose files detected

<sub>Needs Ollama or an OpenAI/Anthropic/pydantic-ai provider, uv · Models: Ollama, OpenAI, Anthropic, pydantic-ai providers · [Repo](https://github.com/ggozad/oterm) · [📖 Docs ↗](https://ggozad.github.io/oterm/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/oterm/)</sub>

<a name="easy-stock"></a>
### #&#8288;58 [easy-stock](https://github.com/jundizhou/easy-stock) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · custom license · Nov 2026</sub>

**A-share research desktop app with AI stock analysis and portfolio checks.**

Electron desktop app with a Go backend and React frontend that aggregates A-share quotes, themes, limit-up ladders and news. It runs tiered AI stock research and portfolio inspection with scored reports, and syncs market-author articles from Xueqiu and Taoguba into daily consensus summaries. AI runs through a Hermes or Codex runtime against OpenAI, DeepSeek, Qwen, Moonshot, Anthropic or compatible endpoints, with data kept in local SQLite.

- **+** Four research depths, including a quantitative overview that needs no model call
- **+** Portfolio score uses fixed weights of 35/25/25/15 across four dimensions
- **+** Long tasks save checkpoints and resume; inspections reuse stock reports under 24 hours old
- **+** Research, articles and AI sessions stored locally; Feishu and DingTalk notifications supported
- **−** PolyForm Noncommercial license: source-available, not OSI open source, no commercial use
- **−** Covers China A-shares only, with Chinese-language UI and data sources
- **−** Scheduled runs need the app open and the computer awake
- **−** WeChat articles import only by pasted link; Zsxq sync needs zsxq-cli Skill permission

<sub>no GPU · Needs LLM API key, Xueqiu/Taoguba login for article sync, Hermes or Codex runtime (bundled) · Models: OpenAI, DeepSeek, Qwen, Moonshot, Anthropic · [Repo](https://github.com/jundizhou/easy-stock) · [📖 Docs ↗](https://github.com/jundizhou/easy-stock/blob/main/docs/user-guide.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/easy-stock/)</sub>

<a name="ai4s-research-open-science"></a>
### #&#8288;59 [open-science](https://github.com/ai4s-research/open-science) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (11) · Freshness: active (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · custom license · Nov 2026</sub>

**Desktop AI research workbench with agents, notebooks, and provenance tracking.**

Open Science Desktop is a Tauri 2 and React app for macOS, Windows and Linux that runs a bundled OpenCode sidecar to drive research agents. Bundled skills chain literature survey, experiment code, figures and paper writing, and a local provenance log links artifacts to the code and inputs that produced them. It also ships a headless `osd` CLI and server, plus a token-authenticated web gateway.

- **+** Provenance log links figures and reports to the exact code, inputs and run
- **+** Model-agnostic via OpenCode catalog, OAuth/API keys, and custom OpenAI-compatible endpoints
- **+** `osd server` runs headless with the same web UI; no-root Linux install script
- **+** Runs locally, over SSH/Slurm or Modal; supports ACP agents and MCP connectors
- **−** Windows and Linux builds are not signed
- **−** Detected license is NOASSERTION, while the README badge says MIT
- **−** Install section lists Linux x86_64 only; ARM64 appears only in the news
- **−** No local inference engine bundled; results depend on the chosen model

<sub>Needs OpenCode (bundled), uv (bundled, for Jupyter), WebKitGTK 4.1 (Linux desktop without root) · Models: OpenCode provider catalog, Anthropic, custom OpenAI-compatible endpoints, ACP agents (Codex, Gemini CLI, Claude Code) · [Repo](https://github.com/ai4s-research/open-science) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai4s-research-open-science/)</sub>

<a name="openfic"></a>
### #&#8288;60 [openfic](https://github.com/syrizelink/openfic) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · Apache-2.0 · Nov 2026</sub>

**AI-assisted editor for writing novels, with configurable agents and retrieval.**

OpenFic is a novel-writing app that pairs an editor with configurable AI agents. It keeps worldbuilding, character and chapter data in local project storage and uses vector-based agentic RAG to retrieve earlier material in long projects. It runs as a Docker container, a pip package (Python 3.12+) or a desktop build, and connects to OpenAI-compatible providers.

- **+** Prompts, agents and workflows are editable, so the writing process can be customized
- **+** Vector retrieval aimed at projects of a million characters or more
- **+** Project data stays local, with no cloud storage dependency
- **+** Three install paths: Docker, pip, and desktop releases
- **−** Aimed at fiction writing only; not suited to short copy or general text generation
- **−** Main README is in Chinese; English is in a separate file
- **−** Needs an external model provider or API key; no bundled local runtime is described
- **−** No live demo or dedicated docs site is linked

<sub>no GPU · Docker + Compose · Needs OpenAI-compatible LLM provider API · Models: OpenAI-compatible APIs, ChatGPT, Claude, Gemini, Kimi · port 8000 · [Repo](https://github.com/syrizelink/openfic) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openfic/)</sub>

<a name="open-cowork"></a>
### #&#8288;61 [open-cowork](https://github.com/opencoworkai/open-cowork) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · MIT · Oct 2026</sub>

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

<a name="knowledge"></a>
### #&#8288;62 [knowledge](https://github.com/robroyce/knowledge) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · Apache-2.0 · Oct 2026</sub>

**Desktop app for saving, organizing and chatting with websites and documents.**

Knowledge is a desktop app with a built-in Chromium browser for saving web pages and files into projects, viewed as inbox, graph or grid. A Chat feature lets you ask an LLM questions about your projects and sources, and the browser can summarize pages, extract topics or turn content into notes. The README states development has stopped.

- **+** Built-in Chromium browser with right-click summarize, topic extraction and note creation
- **+** Inbox, graph and grid views for organizing saved sources into projects
- **+** Chat over projects and sources inside the same app
- **+** Companion Chrome extension for saving pages
- **−** No longer developed, per the README note
- **−** No tagged release on the repository
- **−** Disclaimer warns of possible data loss and no warranty

<sub>[Repo](https://github.com/robroyce/knowledge) · [📖 Docs ↗](https://github.com/KnowledgeCanvas/knowledge/wiki/Getting-Started) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/knowledge/)</sub>

<a name="enchanted"></a>
### #&#8288;63 [enchanted](https://github.com/gluonfield/enchanted) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (51) · Freshness: active (88) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Jul 2026</sub>

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

<a name="sidekick"></a>
### #&#8288;64 [sidekick](https://github.com/johnbean393/sidekick) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: known (31) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Sep 2026</sub>

**macOS app for chatting with local GGUF models over your files and websites.**

Sidekick is a native Swift macOS app that runs GGUF models through a built-in llama.cpp backend and answers from files, folders and websites grouped into "experts" using RAG. It also offers function calling, a Deep Research agent, memory across conversations, web search, and OpenAI-compatible APIs with provider presets. It requires Apple Silicon and at least 8 GB RAM.

- **+** Built-in llama.cpp engine with speculative decoding; no separate model server to install
- **+** Answers cite sources, and clicking a reference opens the original file
- **+** Presets for OpenAI, Anthropic, Google AI Studio, DeepSeek, Groq, Mistral, xAI and others
- **+** Deep Research agent reads 50-80 webpages to produce a report
- **−** macOS on Apple Silicon only; no Windows or Linux builds
- **−** Image generation needs macOS 15.2+ and Apple Intelligence
- **−** No tagged releases; install is via Homebrew cask or manual download
- **−** Building from source needs Xcode and a team name set through setup.sh

<sub>RAM ≥ 8 GB · GPU optional · Models: GGUF (llama.cpp), OpenAI-compatible APIs · [Repo](https://github.com/johnbean393/sidekick) · [📖 Docs ↗](https://johnbean393.github.io/Sidekick/Markdown/gettingStarted/) · [🌐 Site ↗](https://johnbean393.github.io/Sidekick/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sidekick/)</sub>

<a name="maid"></a>
### #&#8288;65 [maid](https://github.com/mobile-artificial-intelligence/maid) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (25) · Freshness: active (94) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · MIT · Oct 2026</sub>

**Android app for chatting with on-device GGUF models or remote APIs.**

Maid is a React Native Android app that runs GGUF models on-device through llama.cpp. It also connects to remote providers such as OpenAI, Anthropic, Mistral, DeepSeek and Ollama with your own API key. Models can be downloaded from Hugging Face in-app or loaded from local storage, with per-session sampling parameters and a global system prompt. Text-to-speech needs the separate Maise app.

- **+** Runs GGUF models fully on-device via llama.cpp, no internet needed
- **+** Supports OpenAI, Anthropic, Mistral, DeepSeek, Ollama and a LiteLLM proxy as remote backends
- **+** Chats can be exported and imported as JSON
- **+** MIT licensed, with no telemetry or ads stated
- **−** Android only; no iOS or desktop builds listed
- **−** Text-to-speech requires installing the separate Maise app
- **−** No document chat, agents or RAG in the feature list
- **−** Last tagged release is March 2026, behind recent commits

<sub>Needs llama.cpp, Hugging Face (model downloads) · Models: GGUF, OpenAI, Anthropic, Mistral, DeepSeek · [Repo](https://github.com/mobile-artificial-intelligence/maid) · [📖 Docs ↗](https://github.com/Mobile-Artificial-Intelligence/maid/releases/latest) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/maid/)</sub>

<a name="ultimatevocalremovergui"></a>
### #&#8288;66 [ultimatevocalremovergui](https://github.com/anjok07/ultimatevocalremovergui) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: widely used (88) · Freshness: recent (70) · Maintenance: weak (9) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · MIT · Oct 2026</sub>

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
### #&#8288;67 [5ire](https://github.com/nanbingxyz/5ire) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (47) · Freshness: active (94) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · custom license · Nov 2026</sub>

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

<a name="justhireme"></a>
### #&#8288;68 [justhireme](https://github.com/vasu-devs/justhireme) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (14) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · AGPL-3.0 · Sep 2026</sub>

**Desktop app that scrapes job leads, ranks fit, and drafts tailored applications.**

JustHireMe is a Tauri desktop app with a Python FastAPI sidecar. It collects job leads from ATS boards, RSS, Hacker News, Reddit and APIs, filters them with a deterministic quality gate, and scores fit against your imported résumé. Matching uses a Kuzu profile graph, LanceDB vectors and a bundled ONNX MiniLM embedding model. It then generates a résumé PDF, a cover letter PDF and outreach drafts.

- **+** Runs with no API key: Ollama, Claude Code CLI or Codex CLI can power LLM steps
- **+** Data stays local: SQLite CRM, Kuzu graph, LanceDB vectors, generated PDFs
- **+** Fit scores come with reasons from deterministic rules and graph evidence
- **+** Installers for Windows, macOS and Linux with built-in auto-update
- **−** Auto-apply browser automation is experimental, off by default and unsupported
- **−** macOS build is ad-hoc signed, not notarized; Gatekeeper needs a manual override
- **−** First launch downloads a runtime pack: browser, vector libraries, embedding model
- **−** AGPL-3.0 license limits use in closed-source derivatives

<sub>GPU optional · Needs Ollama (optional), Claude Code CLI (optional), Codex CLI (optional), Playwright (experimental automation only) · Models: Ollama, Claude Code CLI, Codex CLI, OpenAI, Anthropic · [Repo](https://github.com/vasu-devs/justhireme) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/justhireme/)</sub>

<a name="noi"></a>
### #&#8288;69 [noi](https://github.com/lencx/noi) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: popular (66) · Freshness: active (89) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 9.1k · no license · Aug 2026</sub>

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
### #&#8288;70 [b](https://github.com/ahmadhassan-bted/b) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: known (45) · Freshness: active (83) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · MIT · Jul 2026</sub>

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

<a name="ai-dev-gallery"></a>
### #&#8288;71 [ai-dev-gallery](https://github.com/microsoft/ai-dev-gallery) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: weak (21) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · MIT · Nov 2026</sub>

**Windows app with 25+ local AI samples and exportable C# projects.**

AI Dev Gallery is a WinUI app for Windows developers that runs more than 25 interactive samples against local AI models. Models can be browsed and downloaded from Hugging Face and GitHub, and each sample's C# source can be exported as a standalone Visual Studio project. It is in public preview and logs basic telemetry.

- **+** Exports any sample as a standalone Visual Studio project with C# source
- **+** Works offline once models are downloaded; no Microsoft account required
- **+** Downloads models from Hugging Face and GitHub inside the app
- **+** Supports x64 and ARM64, including Copilot+ PCs
- **−** Windows only; Windows 10 1809 or newer required
- **−** Building from source needs Visual Studio 2022 with Windows application development workload
- **−** App must be running to try any sample, even a single one
- **−** Still in public preview and sends basic telemetry

<sub>RAM ≥ 16 GB · GPU optional · Needs Windows 10 1809+, Visual Studio 2022 (to build), Windows App SDK · Models: Hugging Face models, GitHub models, Microsoft Foundry on Windows APIs · [Repo](https://github.com/microsoft/ai-dev-gallery) · [📖 Docs ↗](https://learn.microsoft.com/windows/ai/overview) · [🌐 Site ↗](http://aka.ms/ai-dev-gallery-store) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-dev-gallery/)</sub>

<a name="minecontext"></a>
### #&#8288;72 [minecontext](https://github.com/volcengine/minecontext) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: known (48) · Freshness: recent (63) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · May 2026</sub>

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

<a name="open-interface"></a>
### #&#8288;73 [open-interface](https://github.com/ambersahdev/open-interface) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (24) · Freshness: recent (70) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · GPL-3.0 · Nov 2026</sub>

**Desktop app that drives your mouse and keyboard from LLM screenshot feedback.**

Open Interface is a Python desktop app that sends a goal and a screenshot to an LLM backend, then executes the returned steps by simulating keyboard and mouse input. It re-sends updated screenshots to course-correct. It supports GPT-4o, Gemini and any OpenAI-style API endpoint such as Llava, and ships binaries for macOS, Linux and Windows.

- **+** Prebuilt binaries for macOS, Linux and Windows, or run as a Python 3.12 script
- **+** Backend is configurable: OpenAI, Gemini, or a custom OpenAI-compatible base URL
- **+** Stop button or dragging the cursor to a screen corner interrupts a run
- **+** README gives a cost estimate of $0.0005 to $0.002 per LLM request
- **−** Only sees the primary display; may retry actions if focus is on a second monitor
- **−** README lists weak spatial reasoning, so clicking buttons and spreadsheets are error-prone
- **−** Last release is 2025-03-16; binaries tested only on Ubuntu 20.04 and Windows 10
- **−** Acts directly on your desktop; README mentions no sandboxing of actions

<sub>no GPU · Needs OpenAI or Gemini API key, or an OpenAI-compatible LLM endpoint, Python 3.12+ (script mode), tkinter · Models: GPT-4o, Google Gemini, OpenAI-compatible APIs (e.g. Llava) · [Repo](https://github.com/ambersahdev/open-interface) · [🌐 Site ↗](https://AmberSah.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-interface/)</sub>

<a name="surf"></a>
### #&#8288;74 [surf](https://github.com/deta/surf) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (36) · Freshness: recent (76) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · May 2026</sub>

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
### #&#8288;75 [open-claude-cowork](https://github.com/composio-community/open-claude-cowork) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: known (41) · Freshness: recent (60) · Maintenance: weak (0) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · May 2026</sub>

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

<a name="aichat"></a>
### #&#8288;76 [aichat](https://github.com/sigoden/aichat) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: popular (71) · Freshness: quiet (27) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Feb 2026</sub>

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

<a name="my-translator"></a>
### #&#8288;77 [my-translator](https://github.com/phuc-nt/my-translator) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (3) · Freshness: active (89) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Jul 2026</sub>

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

<a name="llmfarm"></a>
### #&#8288;78 [llmfarm](https://github.com/guinmoon/llmfarm) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: niche (10) · Freshness: quiet (18) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · MIT · Jan 2026</sub>

**iOS and macOS app for running llama.cpp-based LLMs on-device.**

LLMFarm is a native iOS (16+) and macOS (13+) app that loads local LLMs through ggml and llama.cpp, with per-model settings, several sampling methods and Metal acceleration. It also supports multimodal models such as LLaVA, saved context state, Apple Shortcuts and RAG. The README says the app is temporarily unavailable on TestFlight and the App Store.

- **+** Runs on both iOS 16+ and macOS 13+ with Metal offload
- **+** Supports many architectures plus LLaVA, BakLLaVA, Moondream and MobileVLM vision models
- **+** Sampling options include Mirostat, TFS, locally typical sampling and grammar
- **+** Apple Shortcuts integration, RAG, and saved context state
- **−** App currently unavailable on TestFlight and App Store, so it must be built from source
- **−** Metal does not work on Intel Macs
- **−** Apple platforms only; no Windows, Linux or Android build
- **−** Build needs a recursive submodule clone; core library lives in a separate repo

<sub>GPU optional · Needs llama.cpp, ggml, llmfarm_core.swift · Models: LLaMA, Gemma, Phi, Qwen, Mixtral · [Repo](https://github.com/guinmoon/llmfarm) · [📖 Docs ↗](https://llmfarm.tech/docs) · [🌐 Site ↗](https://llmfarm.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llmfarm/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
