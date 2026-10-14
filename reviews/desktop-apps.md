# 🖥️ Desktop AI apps reviews · Best of Open-Source AI

Apps you install on your own computer to chat with local or API models, often with document chat and agents built in. Back to the [leaderboard](../README.md#%EF%B8%8F-desktop-ai-apps).

<sub>🌐 Also on the web: [Desktop AI apps on archestack.com](https://archestack.com/best-of-ai/desktop-apps/), each project on its own page.</sub>

<a name="deep-live-cam"></a>
### 🥇 [deep-live-cam](https://github.com/hacksider/deep-live-cam) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 97k · AGPL-3.0 · Oct 2026</sub>

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

<a name="cherry-studio"></a>
### 🥈 [cherry-studio](https://github.com/cherryhq/cherry-studio) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · AGPL-3.0 · Oct 2026</sub>

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

<a name="jan"></a>
### 🥉 [jan](https://github.com/janhq/jan) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 45k · custom license · Oct 2026</sub>

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

<a name="chatbox"></a>
### #&#8288;4 [chatbox](https://github.com/chatboxai/chatbox) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (75) · Easy to run: easy (50) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · GPL-3.0 · Sep 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
