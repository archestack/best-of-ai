# 🎨 Image and video reviews · Best of Open-Source AI

Generation UIs and pipelines for images and video, usually around diffusion models. Back to the [leaderboard](../README.md#-image-and-video).

<sub>🌐 Also on the web: [Image and video on archestack.com](https://archestack.com/best-of-ai/image-video/), each project on its own page.</sub>

<a name="frigate"></a>
### 🥇 [frigate](https://github.com/blakeblackshear/frigate) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · MIT · Nov 2026</sub>

**Local NVR with realtime object detection for IP cameras.**

Frigate is a network video recorder that runs object detection locally on IP camera streams using OpenCV and TensorFlow. It uses low-overhead motion detection to decide where to run detection, records video with retention based on detected objects, and re-streams over RTSP. It integrates with Home Assistant through a custom component and publishes events over MQTT.

- **+** Runs detection only where motion is found, which limits CPU use
- **+** Retention rules based on detected objects, plus 24/7 recording
- **+** RTSP re-streaming, plus WebRTC and MSE for low-latency live view
- **+** MQTT and a Home Assistant custom component for integration
- **−** README strongly recommends a GPU or AI accelerator for detection
- **−** Tightly oriented to Home Assistant; other setups rely on MQTT
- **−** Frigate name and logo are trademarks excluded from the MIT license

<sub>GPU optional · Docker + Compose · Needs MQTT, Home Assistant (optional), IP cameras (RTSP) · Models: TensorFlow · [Repo](https://github.com/blakeblackshear/frigate) · [📖 Docs ↗](https://docs.frigate.video) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/frigate/)</sub>

<a name="moneyprinterturbo"></a>
### 🥈 [MoneyPrinterTurbo](https://github.com/harry0703/moneyprinterturbo) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 143k · MIT · Nov 2026</sub>

**Generates short videos from a topic, with script, footage, voiceover and subtitles.**

MoneyPrinterTurbo takes a topic or keywords and produces a finished short video. It writes the script with a configurable LLM, pulls footage from Pexels, Pixabay or Coverr (or generates clips through video APIs), then adds TTS voiceover, subtitles and background music. Output is 9:16, 16:9 or 1:1, driven from a WebUI, API, CLI or AI agent.

- **+** Covers the full pipeline: script, footage, voiceover, subtitles, music and render
- **+** Many LLM providers, including OpenAI, Claude, Gemini, DeepSeek and local Ollama
- **+** Edge TTS voiceover needs no API key; GPU is not required
- **+** WebUI, API and CLI, plus batch generation of multiple videos
- **−** Stock footage sources and AI video generators need their own API keys
- **−** Main README is Chinese-first and carries many sponsor promotions
- **−** Footage is matched by keyword, so clips may not fit the script closely
- **−** Local faster-whisper transcription is slow without a GPU

<sub>RAM ≥ 4 GB · GPU optional · Docker + Compose · Needs Python 3.11+, LLM API or Ollama, Pexels/Pixabay/Coverr API key, Edge TTS or other TTS service · Models: OpenAI, Anthropic Claude, Google Gemini, DeepSeek, Kimi · [Repo](https://github.com/harry0703/moneyprinterturbo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moneyprinterturbo/)</sub>

<a name="toonflow-app"></a>
### 🥉 [toonflow-app](https://github.com/hbai-ltd/toonflow-app) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Nov 2026</sub>

**Infinite-canvas tool for AI short drama and comic video production.**

Toonflow is a Vue/TypeScript app on Bun where scripts, storyboards, character and scene assets, and generated video clips live as nodes on one infinite canvas. Text, image and video generation go through third-party APIs or a local ComfyUI/LLM, and it can be extended with MCP, an agent/A2A interface and a plugin market. It ships as desktop clients, an Android ARM64 APK, Docker and a Linux server install.

- **+** Covers script, storyboard, asset and video-clip steps on a single canvas
- **+** Models are configurable: third-party APIs, local ComfyUI workflows or local LLMs
- **+** MIT license with no commercial restrictions; extensible via MCP, A2A and plugins
- **+** Desktop, Android ARM64, Docker Compose and bare Bun server install paths
- **−** No login or auth on the web UI or API; needs a firewall or authenticated proxy
- **−** Port 3000 is fixed and not configurable
- **−** README, docs and tutorials are primarily in Chinese (Feishu docs)
- **−** Generation quality and cost depend on external paid model APIs; hardware needs for local use unknown

<sub>GPU optional · Docker + Compose · Needs Bun 1.3.14, FFmpeg, Docker (optional), Third-party model APIs or ComfyUI · Models: Third-party LLM, image and video APIs, ComfyUI workflows, Local LLMs · port 3000 · [Repo](https://github.com/hbai-ltd/toonflow-app) · [📖 Docs ↗](https://qcn7xdsqgc4z.feishu.cn/docx/RXFqdgR2Xo0dXZxGfd0cZCGgnwf) · [🌐 Site ↗](https://api.toonflow.net/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/toonflow-app/)</sub>

<a name="invokeai"></a>
### #&#8288;4 [InvokeAI](https://github.com/invoke-ai/invokeai) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Nov 2026</sub>

**Web UI for diffusion image generation with inpainting canvas and node workflows.**

Invoke runs a local web server with a React UI for generating and editing images with diffusion models. It includes a Unified Canvas for in/out-painting, a node-based workflow editor, a gallery with prompt metadata recall, and a model manager. It loads ckpt, diffusers and some GGUF models, covering SD 1.5, SDXL, SD 3.5, Flux.1/Flux.2, Qwen Image and Z-Image.

- **+** Unified Canvas with in/out-painting and brush tools for iterative editing
- **+** Node-based workflow editor for building and sharing generation pipelines
- **+** Broad model list: SD 1.5 through Flux.2, Qwen Image, Z-Image, SAM/SAM2 segmentation
- **+** Gallery stores prompt and settings metadata in images for recall
- **−** README gives no RAM, VRAM or GPU requirements
- **−** Nano Banana, GPT Image and Wan are API-only, not local
- **−** GGUF support is partial, described only as 'some gguf models'
- **−** README points to a separate Launcher app for install, with no manual or Docker steps

<sub>Docker + Compose · Needs Invoke Launcher · Models: SD 1.5, SD 2.0, SDXL, SD 3.5, CogView 4 · [Repo](https://github.com/invoke-ai/invokeai) · [📖 Docs ↗](https://invoke.ai/start-here/installation/) · [🌐 Site ↗](https://invoke.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/invokeai/)</sub>

<a name="comfyui"></a>
### #&#8288;5 [ComfyUI](https://github.com/comfy-org/comfyui) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 147k · GPL-3.0 · Nov 2026</sub>

**Node-graph editor for running diffusion image, video, audio and 3D workflows.**

ComfyUI is a node-graph interface and execution engine for diffusion and other generative models, covering image, video, audio, 3D and text workflows. It runs on NVIDIA, AMD, Intel, Apple Silicon and Ascend hardware, and uses weight streaming and offloading to fit large models in small VRAM. Workflows save as JSON and can be driven through a local API, with custom nodes for extension.

- **+** Native support for many models: SDXL, Flux, Wan 2.x, LTX-Video, HunyuanVideo, ACE-Step
- **+** README claims large models run on 4GB VRAM with 8GB RAM via weight streaming
- **+** Desktop app, Windows portable builds, comfy-cli and manual install; NVIDIA, AMD, Intel, Apple GPUs
- **+** Workflows save as JSON, are recoverable from generated media, and can be called through an API
- **−** Node graph has a learning curve compared with form-based generation UIs
- **−** Commits between stable tags may be unstable and break many custom nodes
- **−** Partner/API nodes for closed models are paid; --offline disables them
- **−** Desktop app only for Windows and macOS; Linux needs manual install

<sub>RAM ≥ 8 GB · GPU optional · Needs PyTorch, Python 3.13 recommended · Models: Stable Diffusion 1.5, SDXL, SD3.5, Flux.1, Flux.2 · [Repo](https://github.com/comfy-org/comfyui) · [📖 Docs ↗](https://docs.comfy.org/) · [🌐 Site ↗](https://www.comfy.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/comfyui/)</sub>

<a name="autoclip"></a>
### #&#8288;6 [autoclip](https://github.com/zhouxiaoka/autoclip) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Nov 2026</sub>

**Turns a video link into short clips with covers and captions.**

AutoClip takes a video URL or local file, transcribes it (author subtitles, local Whisper/SenseVoice, or cloud ASR), and has an LLM pick up to 10 clips per target platform. It renders them locally with FFmpeg, following the speaker in portrait layouts, and adds covers, titles and publish copy. It ships as a desktop app, a Docker web service, and a CLI/MCP server.

- **+** Editing and rendering run locally; cloud is used only for chosen analysis, transcription or image steps
- **+** Same pipeline from desktop, CLI and MCP server, so agents can drive it
- **+** Works with Ollama and LM Studio for local analysis, plus OpenAI-compatible APIs
- **+** README gives measured runs: 1h43m source to 10 clips in 7.5 minutes on Apple Silicon
- **−** Desktop installers only for macOS Apple Silicon and Windows x64; Intel Mac and Linux need Docker or CLI
- **−** Tuned for interviews, podcasts and talking-head video; screen recordings need vision models and manual checks
- **−** Branded end card is on by default and must be turned off in settings
- **−** Cloud analysis and transcription are billed by the provider and need your own API keys

<sub>GPU optional · Docker + Compose · Needs FFmpeg, Python 3.10+, Docker Compose v2, Ollama or LM Studio (optional), Cloud LLM API key (optional) · Models: OpenAI-compatible APIs, Ollama, LM Studio, Whisper, SenseVoice · port 3000 · [Repo](https://github.com/zhouxiaoka/autoclip) · [📖 Docs ↗](https://github.com/zhouxiaoka/autoclip/blob/main/docs/USER_INSTALLATION_GUIDE.md) · [🌐 Site ↗](https://zhouxiaoka.github.io/autoclip_intro/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autoclip/)</sub>

<a name="banana-slides"></a>
### #&#8288;7 [banana-slides](https://github.com/anionex/banana-slides) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (77) · Freshness: active (92) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · AGPL-3.0 · Nov 2026</sub>

**AI slide deck generator that exports PPTX, PDF and narrated video.**

Banana Slides generates presentations from a topic, outline, page descriptions or uploaded PDF/Docx/MD/Txt files, rendering each page as an image with image-generation models such as Nano Banana Pro. Pages can be edited by natural-language instructions or box selection, and exported as PPTX, PDF, editable PPTX (beta) or an MP4 with TTS narration. It runs as a Flask backend plus a web frontend and needs an API key for a text/image provider.

- **+** Several providers: Gemini, OpenAI-format, Volcengine, Vertex AI and LazyLLM vendors like Qwen and DeepSeek
- **+** Exports PPTX, PDF, editable PPTX (beta) and narrated MP4 with subtitles
- **+** Edit pages by natural-language prompt or box selection; per-page templates supported
- **+** Prebuilt Docker Hub images with a docker-compose.prod.yml, plus a CLI and agent skills
- **−** AGPL-3.0 license restricts use in closed-source hosted services
- **−** Needs paid external image-generation API; README warns Nano Banana Pro calls are costly
- **−** Editable PPTX export is beta; better results need a Baidu API key
- **−** README is mostly Chinese; desktop build is at release-candidate stage (v0.9.0-rc.7)

<sub>no GPU · Docker + Compose · Needs Gemini/OpenAI/Volcengine/Vertex or LazyLLM API key, FFmpeg with libass (video export), LibreOffice (optional, PPTX upload), Baidu API key (optional, editable export) · Models: Gemini (Nano Banana Pro), OpenAI-compatible (gpt-image-2), Volcengine Doubao/Seedream, Vertex AI, LazyLLM vendors (Qwen, DeepSeek, GLM, Kimi, MiniMax, SiliconFlow) · port 3011 · [Repo](https://github.com/anionex/banana-slides) · [▶️ Demo ↗](https://bananaslides.online/) · [📖 Docs ↗](https://docs.bananaslides.online/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/banana-slides/)</sub>

<a name="arcreel"></a>
### #&#8288;8 [arcreel](https://github.com/arcreel/arcreel) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · AGPL-3.0 · Nov 2026</sub>

**Self-hosted workbench that turns novels or scripts into short videos.**

ArcReel runs a pipeline from novel, finished script or product material through content analysis, character/scene/prop assets, storyboards, video clips and narration to a final cut. Generation uses text, image, video and TTS providers configured in Settings, with cost tracking before and after each run. Output can be composed directly or exported as a Jianying draft for further editing.

- **+** Reuses asset reference images across storyboards to keep characters consistent
- **+** Stages can be confirmed, single assets regenerated, and versions rolled back
- **+** Shows estimated and actual cost per generation
- **+** Exports Jianying drafts; supports SQLite or PostgreSQL
- **−** Generation depends on external provider APIs that you configure and pay for
- **−** Jianying export targets the mainland China version; CapCut compatibility not verified
- **−** AGPL-3.0; white-label or non-AGPL commercial use needs a separate agreement
- **−** Default Compose publishes port 1241 on all interfaces; add auth and HTTPS for remote use

<sub>no GPU · Docker + Compose · Needs Docker, Docker Compose, text/image/video/TTS provider APIs, SQLite or PostgreSQL · Models: text LLM providers, image generation providers, video generation providers, TTS providers · port 1241 · [Repo](https://github.com/arcreel/arcreel) · [📖 Docs ↗](https://docs.arc-reel.com/guide/getting-started) · [🌐 Site ↗](https://docs.arc-reel.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/arcreel/)</sub>

<a name="stable-diffusion-cpp"></a>
### #&#8288;9 [stable-diffusion.cpp](https://github.com/leejet/stable-diffusion.cpp) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · MIT · Nov 2026</sub>

**C/C++ inference for Stable Diffusion, Flux, Qwen-Image and Wan video models.**

Runs diffusion models for image and video generation in plain C/C++ on top of ggml, the same way llama.cpp does for LLMs. It loads ckpt, safetensors and GGUF weights and runs on CPU, CUDA, Vulkan, Metal, OpenCL or SYCL. The main interface is the sd-cli command-line tool, and the README mentions an embedded web UI.

- **+** Backends: CPU (AVX/AVX2/AVX512), CUDA, Vulkan, Metal, OpenCL and SYCL
- **+** Covers SD1.x to SDXL, SD3, FLUX, Qwen-Image, Z-Image, plus Wan and LTX video
- **+** Reads .ckpt, .safetensors and .gguf; convert mode writes .gguf or .safetensors
- **+** Flash attention, VAE tiling and TAESD cut memory use; bindings for Go, C#, Python, Rust
- **−** README warns API and command-line options may change frequently
- **−** ControlNet support is stated only for SD 1.5
- **−** Shorter sampler list than stable-diffusion-webui
- **−** No node-graph UI in the README; separate projects supply GUIs

<sub>GPU optional · Docker · Models: SD1.x, SD2.x, SDXL, SD3/SD3.5, FLUX.1 · [Repo](https://github.com/leejet/stable-diffusion.cpp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/stable-diffusion-cpp/)</sub>

<a name="infinite-canvas"></a>
### #&#8288;10 [infinite-canvas](https://github.com/basketikun/infinite-canvas) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

**Browser-based infinite canvas for AI image and video generation.**

A React and Vite web workbench where images, prompts and chat nodes are laid out on a pannable canvas and wired together. The browser calls your own OpenAI-compatible Base URL and API Key for text-to-image, image editing, text, audio and video. Canvases, assets and keys are stored in the browser; an optional local Canvas Agent lets Codex or Claude Code edit the canvas over MCP.

- **+** Browser calls the API directly; keys, canvases and assets stay in local browser storage
- **+** Custom scripts adapt image and video calls to non-standard OpenAI-compatible relays
- **+** Remote node plugins installable by URL, with a TypeScript SDK
- **+** Local Canvas Agent exposes the canvas to Codex or Claude Code through MCP
- **−** Generates nothing itself; needs an external OpenAI-compatible image or video API
- **−** README warns of development stage; local storage formats may change without compatibility
- **−** Data lives in the browser, so no server-side sync or multi-user accounts are described
- **−** Docs and README are mostly in Chinese; README is heavy with sponsor ads

<sub>no GPU · Docker + Compose · Needs OpenAI-compatible API endpoint and key · Models: OpenAI-compatible image, text, audio and video APIs · port 3000 · [Repo](https://github.com/basketikun/infinite-canvas) · [📖 Docs ↗](https://github.com/basketikun/infinite-canvas/blob/main/docs/content/docs/overview/quick-start.mdx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/infinite-canvas/)</sub>

<a name="krita-ai-diffusion"></a>
### #&#8288;11 [krita-ai-diffusion](https://github.com/acly/krita-ai-diffusion) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · GPL-3.0 · Oct 2026</sub>

**Krita plugin for inpainting, live painting and upscaling with diffusion models.**

A Krita plugin that adds generative image tools to the painting canvas: selection-based inpainting and expand, live painting, upscaling, and text-instruction edit models. It uses ComfyUI as the backend, either installed automatically from the plugin, pointed at an existing local or remote server, or via cloud generation. Supports Flux 2, Z-Image, Stable Diffusion 1.5, SDXL and Illustrious, with ControlNet, IP-Adapter and per-region prompts.

- **+** Works on Krita selections and layers, with per-region prompts defined by layers
- **+** ControlNet and IP-Adapter support: scribble, line art, depth, pose, style and face reference
- **+** Can install a local ComfyUI server or connect to an existing or remote one
- **+** Custom presets for checkpoints, LoRA and samplers; runs on NVIDIA, AMD, Intel and Apple Silicon
- **−** Requires Krita 5.2.0 or newer; unusable outside Krita
- **−** CPU generation is supported but described as very slow
- **−** Object selection and segmentation need a separate plugin (krita-ai-tools)
- **−** Custom ComfyUI setups need specific extensions and models installed manually

<sub>GPU optional · Needs Krita 5.2.0+, ComfyUI · Models: Flux 2, Z-Image, Stable Diffusion 1.5, SDXL, Illustrious · [Repo](https://github.com/acly/krita-ai-diffusion) · [▶️ Demo ↗](https://youtu.be/Ly6USRwTHe0) · [📖 Docs ↗](https://docs.interstice.cloud) · [🌐 Site ↗](https://www.interstice.cloud) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/krita-ai-diffusion/)</sub>

<a name="dramaclaw"></a>
### #&#8288;12 [dramaclaw](https://github.com/dramaclaw/dramaclaw) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · custom license · Nov 2026</sub>

**Node-canvas and pipeline for producing AI short dramas from script to final cut.**

DramaClaw is a source-available production line for AI short drama. It pairs a node-based canvas (XiaHua) with a series pipeline (XiaJi) that takes a manuscript or screenplay through episode planning, scripts, storyboards, voice-over and video export. A built-in agent, Xia Director, plans and runs canvas workflows. Inference goes through an OpenAI-compatible gateway, not local models.

- **+** Covers the whole chain: ingest, episode planning, storyboards, voice-over, subtitles and video export
- **+** Canvas with 18 node types plus an agent that builds and runs graphs after confirmation
- **+** Light local footprint: 2 vCPU / 4 GB recommended, GPU only for the optional world extra
- **+** Agent Kit exposes workflows to Codex, Claude Code, OpenClaw and other MCP clients
- **−** Elastic License 2.0 with a Powered by DramaClaw notice; hosted SaaS use not permitted
- **−** Previz 3D stage and interactive stories are closed beta, not in the main branch
- **−** Needs an external OpenAI-compatible gateway; no models run locally
- **−** Tuned for drama and short-form video; sample works are in Chinese

<sub>RAM ≥ 4 GB · GPU optional · Docker + Compose · Needs OpenAI-compatible gateway (RelayClaw or dramaclaw-gateway), Docker · Models: OpenAI-compatible API, Seedance 2.5, open-weight models via gateway · [Repo](https://github.com/dramaclaw/dramaclaw) · [📖 Docs ↗](https://github.com/dramaclaw/dramaclaw/blob/main/docs/en/README.md) · [🌐 Site ↗](https://dramaclaw.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dramaclaw/)</sub>

<a name="remove-ai-watermarks"></a>
### #&#8288;13 [remove-ai-watermarks](https://github.com/wiltodelta/remove-ai-watermarks) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Nov 2026</sub>

**CLI that strips visible AI marks, metadata and invisible watermarks from images and video.**

Python CLI and library that finds and removes AI provenance marks from your own images, video and text. It covers visible labels (Gemini sparkle, Veo, Sora, Doubao, Kling and others), C2PA/EXIF/XMP metadata, and invisible pixel watermarks via diffusion regeneration. Visible and metadata paths run without a GPU; invisible image removal needs CUDA.

- **+** Visible and metadata removal run on CPU with OpenCV, MI-GAN or LaMa fill backends
- **+** Handles images, video (MP4, MOV, WebM, MKV) and text provenance from one CLI
- **+** Video path scans all frames for a stable mark and copies audio without re-encoding
- **+** Installable by feature extras, so metadata-only use pulls no torch
- **−** Invisible image removal is CUDA-only, with no CPU or MPS fallback
- **−** No local SynthID pixel detector; detection relies on signed provenance
- **−** qwen21-zimage profile is restricted to non-commercial use by the Qwen Research License
- **−** Some jurisdictions, including China, restrict removing AI labels; legal risk falls on the user

<sub>GPU optional · Needs ffmpeg, NVIDIA CUDA (invisible removal), PyTorch (diffusion extras) · Models: Qwen-Image-2512 Lightning, SDXL, Chroma1, Z-Image, MI-GAN · [Repo](https://github.com/wiltodelta/remove-ai-watermarks) · [📖 Docs ↗](https://github.com/wiltodelta/remove-ai-watermarks/blob/main/docs/cli.md) · [🌐 Site ↗](https://raiw.cc) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/remove-ai-watermarks/)</sub>

<a name="ltx-2"></a>
### #&#8288;14 [ltx-2](https://github.com/lightricks/ltx-2) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

**Text and image to video model with synchronized audio, plus pipelines and trainer.**

LTX-2 is a 22B-parameter DiT model from Lightricks that generates video with synchronized audio from text, images or input audio. The repo is a Python monorepo with ltx-core, ltx-pipelines (distilled, DFR, two-stage, retake, IC-LoRA, HDR, dubbing) and ltx-trainer for LoRA and full fine-tuning. Weights are downloaded separately from Hugging Face, about 66 GiB for the quick-start set.

- **+** Generates audio and video together in one model, including speech
- **+** Many pipelines: distilled, DFR, keyframe, audio-to-video, retake, HDR/EXR, dubbing
- **+** Includes a trainer for LoRA, full fine-tuning and IC-LoRA
- **+** FP8 quantization and CPU or disk offload flags for limited GPU memory
- **−** Quick-start weights are about 66 GiB and gated behind Hugging Face terms
- **−** License is not identified by tooling (NOASSERTION); check the repo terms
- **−** Fastest VAE backend (natten) is Linux and CUDA only; CLI-driven, no built-in UI

<sub>GPU required · Needs uv, Hugging Face CLI, PyTorch, CUDA · Models: LTX-2.5 22B distilled, LTX-2.5 22B dev, LTX-2.3, Gemma 4 12B text encoder, safetensors · [Repo](https://github.com/lightricks/ltx-2) · [▶️ Demo ↗](https://console.ltx.video/playground) · [🌐 Site ↗](https://ltx.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ltx-2/)</sub>

<a name="open-generative-ai"></a>
### #&#8288;15 [open-generative-ai](https://github.com/anil-matcha/open-generative-ai) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Nov 2026</sub>

**Image, video and lip-sync studio app that calls hosted models through MuAPI.**

Generative media studio with separate Image, Video, Audio, Lip Sync and Cinema workspaces. Most generation goes through the MuAPI cloud service, with the README claiming 200+ models (the headline says 600+). The desktop app can also run local models: bundled stable-diffusion.cpp for SD 1.5, SDXL and Z-Image, or a user-installed Wan2GP for video.

- **+** Local inference in desktop app via bundled sd.cpp (Metal, CUDA, Vulkan, ROCm) with no API key
- **+** Wan2GP integration for local video, including a remote MCP server so Macs can offload to a GPU box
- **+** Accepts up to 14 reference images on compatible edit models
- **+** Installers for macOS, Windows and Linux (AppImage, deb) plus a hosted version
- **−** Cloud generation depends on MuAPI, a paid third-party service, not self-hosted models
- **−** Local inference is desktop-only; the web version always uses cloud APIs
- **−** Installers are unsigned: macOS needs xattr workaround, Windows shows SmartScreen warning
- **−** Model count is inconsistent in the README (600+ vs 200+), and README promotes a paid white-label plan

<sub>RAM ≥ 16 GB · GPU optional · Docker + Compose · Needs MuAPI API key (cloud models), Wan2GP (optional, local video; CUDA/ROCm GPU), Node.js (build from source) · Models: MuAPI hosted models (Flux, Kling, Veo, Sora, Wan 2.2), sd.cpp: SD 1.5, SDXL, Z-Image, Wan2GP: Wan 2.1/2.2, Hunyuan Video 1.5, LTX-2, Flux.1 Dev, Qwen Image · README: alternative to Manus · [Repo](https://github.com/anil-matcha/open-generative-ai) · [▶️ Demo ↗](https://muapi.ai/open-generative-ai?utm_source=github&utm_medium=readme&utm_campaign=open-generative-ai) · [🌐 Site ↗](https://muapi.ai?utm_source=github&utm_medium=readme&utm_campaign=open-generative-ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-generative-ai/)</sub>

<a name="mochidiffusion"></a>
### #&#8288;16 [mochidiffusion](https://github.com/mochidiffusion/mochidiffusion) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · GPL-3.0 · Nov 2026</sub>

**Native macOS app for generating images offline with Stable Diffusion and FLUX.2 Klein.**

Mochi Diffusion is a SwiftUI macOS app that generates images locally using Apple's Core ML Stable Diffusion, with optional ControlNet and image-to-image, and the Iris pipeline for FLUX.2 Klein models on Metal. Output is saved as PNG with generation settings embedded, and a built-in gallery handles import, save and sync. It collects no telemetry and sends nothing to the cloud.

- **+** Runs fully offline; README states no data or telemetry is collected
- **+** Uses Neural Engine via Core ML for low memory use on Apple Silicon
- **+** Supports FLUX.2 Klein 4B and 9B without model conversion, with up to 4 input images
- **+** PNG output embeds settings readable by AUTOMATIC1111-compatible tools and Civitai
- **−** macOS only: requires Apple Silicon and macOS 15.6 or later
- **−** Core ML Stable Diffusion models have a fixed image size set at conversion
- **−** Models must be downloaded or converted and placed manually in a model folder
- **−** First use of a model can take up to 2 minutes to compile for the Neural Engine

<sub>GPU required · Needs Apple Core ML Stable Diffusion, iris.c, Xcode 26.0 or later (to build) · Models: Core ML Stable Diffusion (split_einsum, original), ControlNet (Core ML), FLUX.2 Klein 4B, FLUX.2 Klein 9B · [Repo](https://github.com/mochidiffusion/mochidiffusion) · [📖 Docs ↗](https://github.com/MochiDiffusion/MochiDiffusion/wiki/How-to-convert-Stable-Diffusion-models-to-Core-ML) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mochidiffusion/)</sub>

<a name="stabilitymatrix"></a>
### #&#8288;17 [stabilitymatrix](https://github.com/lykosai/stabilitymatrix) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · AGPL-3.0 · Oct 2026</sub>

**Desktop package manager and built-in inference UI for Stable Diffusion tools.**

Stability Matrix is a C# desktop app for Windows, Linux and Apple Silicon macOS that installs and updates Stable Diffusion front-ends such as ComfyUI, Forge, SD.Next, Fooocus, InvokeAI and trainers like Kohya's GUI. It bundles Git and Python, shares one model directory across packages, and includes its own tabbed Inference UI for image generation.

- **+** One-click install and update for many SD front-ends, including ComfyUI, Forge, SD.Next and InvokeAI
- **+** Embedded Git and Python, so neither needs a global install
- **+** Shared checkpoint directory across packages, with CivitAI and HuggingFace model browser
- **+** Portable data directory; downloads can pause and resume after closing the app
- **−** Binaries are under a separate EULA, while source is AGPL-3.0
- **−** Plugin and extension management covers only A1111, ComfyUI, SD Web UI-UX and SD.Next
- **−** No Docker or server deployment; desktop install only

<sub>Models: CivitAI, HuggingFace, Stable Diffusion checkpoints · [Repo](https://github.com/lykosai/stabilitymatrix) · [🌐 Site ↗](https://lykos.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/stabilitymatrix/)</sub>

<a name="modly"></a>
### #&#8288;18 [modly](https://github.com/lightningpixel/modly) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · custom license · Oct 2026</sub>

**Desktop app that generates 3D meshes from photos using local models.**

Modly is an Electron and TypeScript desktop app with a Python FastAPI backend that turns an image into a 3D mesh using open models on your own GPU. Models such as Hunyuan3D 2 Mini, TripoSG and Trellis2 GGUF are installed as extensions from GitHub repositories. It has a node-based workflow editor, in-app mesh smoothing and decimation, and a CLI for scripts and agents.

- **+** Model extensions install from a GitHub URL; official ones cover Hunyuan3D 2 Mini, TripoSG, Trellis2 GGUF
- **+** Runs on Windows, Linux and Apple Silicon macOS; AMD GPUs supported via ROCm
- **+** Node-based workflows are validated before run; meshes can be smoothed and decimated in-app
- **+** Stdlib-only CLI exposes generate, workflow-run and model commands for scripts and agents
- **−** Focused on image-to-3D; no general image or video generation described
- **−** Hugging Face is the only supported model weight provider
- **−** Detected license is NOASSERTION; README says MIT with a required attribution credit for forks

<sub>GPU required · Needs Node.js, Python, Hugging Face (model weights) · Models: Hunyuan3D 2 Mini, Hunyuan3D 2 Mini Turbo, Hunyuan3D 2 Mini Fast, TripoSG, Trellis2 GGUF · [Repo](https://github.com/lightningpixel/modly) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/modly/)</sub>

<a name="openfilm"></a>
### #&#8288;19 [openfilm](https://github.com/openfilm/openfilm) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Nov 2026</sub>

**Video editor and CLI that lets coding agents write films as HTML pages.**

OpenFilm represents a film as a folder with a film.html, where each track is a section of clips (pages, video, images, audio). Each shot is a web page that draws any moment through a frame(t) function. A coding agent such as Claude Code or Codex writes the film, and Studio, a browser-based editor, lets you change it by hand. The CLI renders MP4, GIF, alpha video and timelines for Final Cut Pro, Premiere Pro and DaVinci Resolve.

- **+** Deterministic frame(t) contract; look renders frames twice in shuffled order and flags any that differ
- **+** Studio edits are saved to the film files, so the agent sees and keeps them
- **+** Exports MP4, GIF, stems, subtitles, transparent video and NLE timelines for Premiere, Resolve and FCP
- **+** Works with any coding agent via skills; no account needed to make and render films
- **−** Studio should be used in a Chromium browser so the preview matches the export
- **−** Generated voice, music, images and video need third-party service keys or an OpenFilm sign-in
- **−** Desktop app is only offered for macOS and Windows
- **−** Shots must be pure functions of t; Python, Blender or video-model output has to come in as media files

<sub>Needs Node 22.2+, ffmpeg, git, headless Chromium (about 100 MB, downloaded on first run) · Models: ElevenLabs, OpenAI, Google, OpenRouter, fal · [Repo](https://github.com/openfilm/openfilm) · [🌐 Site ↗](https://openfilm.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openfilm/)</sub>

<a name="claude-code-video-toolkit"></a>
### #&#8288;20 [claude-code-video-toolkit](https://github.com/digitalsamba/claude-code-video-toolkit) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · MIT · Nov 2026</sub>

**Claude Code skills and templates that script, voice, score and render videos.**

A workspace of Claude Code skills, slash commands, Remotion and moviepy templates, and Python tools that take a video from prompt to rendered MP4. Voiceover, images, music, and video clips come from open models (Qwen3-TTS, FLUX.2, ACE-Step, LTX-2.3) deployed to your own Modal or RunPod account, with ElevenLabs as an alternative. Includes brand profiles, project state tracking across sessions, and a transitions library.

- **+** Covers the full pipeline: script, voiceover, music, image and video clips, Remotion render
- **+** Open models run on your own Modal or RunPod account; README quotes about $0.01 per voiceover
- **+** Hello-world example renders an MP4 locally with no API keys
- **+** Many finished example projects with source, plus brand profiles and project.json session tracking
- **−** Requires Claude Code; it is the driver, not a standalone tool
- **−** AI generation needs a cloud GPU account (Modal or RunPod) set up via /setup
- **−** Author states the main use case is narrow: sprint-review style explainer videos
- **−** Blender skill is experimental and needs a separate Blender install

<sub>GPU optional · Docker · Needs Claude Code, Node.js 22+, uv (Python 3.10+), Modal or RunPod, Cloudflare R2, ElevenLabs (optional), FFmpeg (optional) · Models: Qwen3-TTS, FLUX.2, ACE-Step, LTX-2.3, Qwen-Image · [Repo](https://github.com/digitalsamba/claude-code-video-toolkit) · [▶️ Demo ↗](https://www.youtube.com/watch?v=3HjPatdeal4) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/claude-code-video-toolkit/)</sub>

<a name="printfilm"></a>
### #&#8288;21 [printfilm](https://github.com/yi1108/printfilm) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · MIT · Nov 2026</sub>

**Step-by-step AI short video and serial drama maker, from script to final cut.**

PRINTFILM is a FastAPI and React app that turns an idea or script into a finished short video through staged steps: script, storyboard, reference images, image-to-video, and composition. It also has a serialized-drama mode with episodes and a reusable library of characters, scenes and props. Text, image and video generation go through the TokenFree OpenAI-compatible API, so no local GPU is used.

- **+** Pipeline pauses after each stage so script and storyboard can be edited before continuing
- **+** Reusable character, scene and prop library keeps drama episodes consistent
- **+** Compose file pulls prebuilt public images; ARK_MOCK=true shows the UI without a key
- **+** Admin console covers users, task center and model routing; billing is optional and off by default
- **−** Real generation depends on a TokenFree API key and credits; otherwise only mock mode works
- **−** Needs PostgreSQL and Redis alongside the API, web and admin services
- **−** README and UI are mainly Chinese; contribution rules require Simplified Chinese copy
- **−** Static-image mode needs an external TTS service for narration

<sub>no GPU · Compose · Needs PostgreSQL, Redis, TokenFree API, FFmpeg, Docker · Models: kimi-k2.6, seedream-5-0-pro, seedance-2-5, OpenAI-compatible API · port 8080 · [Repo](https://github.com/yi1108/printfilm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/printfilm/)</sub>

<a name="civitai"></a>
### #&#8288;22 [civitai](https://github.com/civitai/civitai) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (49) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Nov 2026</sub>

**Source of the Civitai site for sharing Stable Diffusion models.**

Next.js, tRPC and Prisma/Postgres application behind civitai.com, where users upload and browse Stable Diffusion models (textual inversions, hypernetworks, VAEs and similar), and comment on them. The repo is a web platform for hosting and discussing models, not a generation tool. Local development runs Postgres, Redis, MinIO, Meilisearch, ClickHouse and a mail catcher via Docker Compose.

- **+** Full production site source under Apache-2.0, including Prisma schema and migrations
- **+** Compose file starts all local dependencies; seed script populates an empty database
- **+** Nix flake option bootstraps the toolchain and dev server in one command
- **−** Generation, training, chat, notifications and Buzz do not work locally
- **−** Signals and buzz containers come from private ghcr.io images, internal members only
- **−** Requires exact Node 24 and pnpm; wrong Node version only warns, then fails oddly
- **−** Manual setup: MinIO access keys and env edits, plus slow destructive migrate and reseed steps

<sub>no GPU · Docker + Compose · Needs Docker Compose v2, Node.js 24, pnpm, PostgreSQL, Redis, MinIO, Meilisearch, ClickHouse, Mailpit · Models: Stable Diffusion checkpoints, textual inversions, hypernetworks, VAEs · port 3000 · [Repo](https://github.com/civitai/civitai) · [▶️ Demo ↗](https://civitai.com/) · [🌐 Site ↗](https://civitai.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/civitai/)</sub>

<a name="sana"></a>
### #&#8288;23 [sana](https://github.com/nvlabs/sana) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.8k · Apache-2.0 · Nov 2026</sub>

**Efficient diffusion models and training code for high-resolution image and video.**

SANA is NVIDIA's research codebase for linear-attention diffusion models, covering text-to-image up to 4K, one/few-step SANA-Sprint, and video models (SANA-Video, SANA-Video 2.0, SANA-WM, SANA-Streaming). It includes training and inference pipelines, DDP/FSDP, LoRA, ControlNet, and RL post-training recipes. Weights are on Hugging Face, with diffusers, ComfyUI and SGLang integrations.

- **+** Full training and inference code, not only weights, including DDP/FSDP and RL post-training
- **+** Runs in diffusers, ComfyUI and SGLang (OpenAI-compatible serving)
- **+** 4-bit and 8-bit variants; README says SANA runs within 8GB VRAM
- **+** Public demos for image, ControlNet, Sprint and SANA-Video 2.0
- **−** Research repo with many sub-projects; no single UI or one-command install
- **−** Some newer pieces (Sol-Engine, H3) live on a separate branch
- **−** Large video and world models need high-end GPUs; exact VRAM is not stated
- **−** Docs are spread across project pages and a separate docs site

<sub>GPU required · Docker · Needs PyTorch, diffusers, Hugging Face weights · Models: SANA, SANA-1.5, SANA-Sprint, SANA-Video, SANA-Video 2.0 · [Repo](https://github.com/nvlabs/sana) · [▶️ Demo ↗](https://nv-sana.mit.edu/) · [📖 Docs ↗](https://nvlabs.github.io/Sana/docs/) · [🌐 Site ↗](https://nvlabs.github.io/Sana/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sana/)</sub>

<a name="comfyui-manager"></a>
### #&#8288;24 [comfyui-manager](https://github.com/comfy-org/comfyui-manager) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · GPL-3.0 · Nov 2026</sub>

**Manager menu for installing and updating ComfyUI custom nodes and models.**

ComfyUI-Manager is a custom node for ComfyUI that adds a Manager menu to install, remove, disable and enable custom nodes and download models. It reads a channel-based node database and the registry at registry.comfy.org, and also provides snapshots, missing-node detection and a cm-cli tool that runs without starting ComfyUI.

- **+** Installs, updates, disables and removes custom nodes from a menu inside ComfyUI
- **+** Snapshots save the installed state and restore it on the next startup
- **+** Install Missing Custom Nodes finds extensions needed by the loaded workflow
- **+** cm-cli runs manager functions without ComfyUI; config supports uv, pip overrides and offline mode
- **−** Only works with ComfyUI; not usable standalone
- **−** Snapshot restore is incomplete for custom nodes not managed by Git
- **−** Install outside ComfyUI/custom_nodes/comfyui-manager breaks recognition and updates
- **−** No tagged release; installed by git clone or comfy-cli

<sub>no GPU · Needs ComfyUI, git, Python 3 · [Repo](https://github.com/comfy-org/comfyui-manager) · [📖 Docs ↗](https://docs.comfy.org/registry/overview) · [🌐 Site ↗](https://ltdrdata.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/comfyui-manager/)</sub>

<a name="ai-toolkit"></a>
### #&#8288;25 [AI Toolkit](https://github.com/ostris/ai-toolkit) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Nov 2026</sub>

**LoRA and LoKr training suite for image, video and audio diffusion models.**

AI Toolkit trains LoRA and LoKr adapters for diffusion models, driven by YAML configs through `python run.py` or a web UI on port 8675. It covers image, instruction/edit, video and audio models, including FLUX.1/2, Qwen-Image, Z-Image, Wan 2.1/2.2, LTX-2 and Ace Step. It targets consumer Nvidia GPUs and has setup notes for RunPod and Modal.

- **+** Supports many recent models: FLUX.2, Qwen-Image, Wan 2.2, LTX-2, Ace Step
- **+** Same jobs run from the CLI with YAML configs or from the web UI
- **+** Layer targeting with only_if_contains and ignore_if_contains; LoKr supported
- **+** Bucketing resizes images automatically, so no manual cropping is needed
- **−** Manual install requires an Nvidia GPU; Apple Silicon support is marked experimental
- **−** AI Toolkit Manager installer is labelled experimental
- **−** Datasets limited to jpg, jpeg and png; webp has issues
- **−** Ctrl+C during a checkpoint save will likely corrupt that checkpoint

<sub>GPU required · Docker + Compose · Needs PyTorch, Node.js >20 (UI), Hugging Face model weights, git · Models: FLUX.1, FLUX.2, Qwen-Image, Z-Image, SDXL · port 8675 · [Repo](https://github.com/ostris/ai-toolkit) · [🌐 Site ↗](https://ostris.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-toolkit/)</sub>

<a name="sdnext"></a>
### #&#8288;26 [sdnext](https://github.com/vladmandic/sdnext) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (50) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Oct 2026</sub>

**Web UI for generating and editing images and video with diffusion models.**

SD.Next is a Python web interface, forked from AUTOMATIC1111's Stable Diffusion WebUI, for text-to-image, image-to-image, text-to-video and image-to-video generation. It adds editing, inpainting, outpainting, LoRA, ControlNet, IP-Adapters, captioning and upscaling. It runs on NVIDIA, AMD, Intel Arc, Apple Silicon, OpenVINO devices or CPU, and a built-in installer handles dependencies and updates.

- **+** Covers NVIDIA CUDA, AMD ROCm/ZLUDA, Intel XPU, OpenVINO, Apple MPS and CPU-only
- **+** Handles image and video generation, plus captioning, tagging, upscaling and interpolation
- **+** SDNQ quantization and CPU/GPU offloading help fit models into limited memory
- **+** Built-in installer and updater; Windows launcher exe and Docker recipes available
- **−** README gives no RAM or VRAM minimums
- **−** No tagged release; the quick start installs by cloning the repo
- **−** First launch installs dependencies, which can take a while
- **−** Supported model list lives in external docs, not the README

<sub>GPU optional · Needs Python, Git · Models: Diffusion models, LoRA, ControlNet, IP-Adapter · [Repo](https://github.com/vladmandic/sdnext) · [📖 Docs ↗](https://vladmandic.github.io/sdnext-docs/) · [🌐 Site ↗](https://vladmandic.github.io/sdnext/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sdnext/)</sub>

<a name="lichtfeld-studio"></a>
### #&#8288;27 [lichtfeld-studio](https://github.com/mrnerf/lichtfeld-studio) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · GPL-3.0 · Nov 2026</sub>

**Native desktop app for training and editing 3D Gaussian Splatting scenes.**

LichtFeld Studio is a C++23/CUDA application that trains 3D Gaussian Splatting scenes from COLMAP datasets, resumes checkpoints, and shows the reconstruction in a real-time viewer. It supports editing gaussian selections with undo/redo and exports to PLY, SOG, SPZ or a standalone HTML viewer. Python plugins, embedded Python and MCP resources and tools allow automation, and it can also run headless.

- **+** Training, live viewer, gaussian editing and export in one application
- **+** Exports PLY, SOG, SPZ and a standalone HTML viewer
- **+** Python plugin system plus MCP tools for scripting and agent control
- **+** Includes MCMC, bilateral grid, 3DGUT and optional POPSpa sparsification
- **−** Requires an NVIDIA GPU with compute capability 7.5+; AMD, Intel and older NVIDIA unsupported
- **−** Prebuilt Windows binaries need a paid donation via the Portal, not GitHub Releases
- **−** Needs NVIDIA driver 570+ and CUDA 12.8+; source builds need a C++23 toolchain
- **−** No Docker or compose setup provided

<sub>GPU required · Docker + Compose · Needs NVIDIA driver 570+, CUDA 12.8+, COLMAP dataset input · Models: 3D Gaussian Splatting, PLY, SOG, SPZ · [Repo](https://github.com/mrnerf/lichtfeld-studio) · [📖 Docs ↗](https://github.com/MrNeRF/LichtFeld-Studio/wiki/) · [🌐 Site ↗](https://lichtfeld.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lichtfeld-studio/)</sub>

<a name="infinigen"></a>
### #&#8288;28 [infinigen](https://github.com/princeton-vl/infinigen) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · BSD-3-Clause · Nov 2026</sub>

**Procedural 3D scene generator on Blender with ground-truth renders.**

Infinigen generates 3D scenes procedurally in Python on top of Blender, covering outdoor nature, indoor rooms and articulated simulation assets. It renders images with ground-truth annotations such as depth, surface normals and instance segmentation. Scenes can be exported to formats like OBJ and OpenUSD, or to physics simulators.

- **+** Renders depth, surface normals and instance segmentation alongside RGB images
- **+** Covers nature, indoor scenes and articulated sim assets in one codebase
- **+** Exports to OBJ, OpenUSD and physics simulators
- **+** Scenes are generated procedurally, so output varies by seed instead of fixed assets
- **−** Install and usage steps are split across several version branches and docs pages
- **−** Not a diffusion-model tool; it needs a Blender-based setup and config tuning
- **−** Contributor tutorials and guidelines are marked as coming soon
- **−** Pre-generated data repository is announced but not yet available

<sub>Docker · Needs Blender · [Repo](https://github.com/princeton-vl/infinigen) · [📖 Docs ↗](https://infinigen.cs.princeton.edu/docs/latest/index.html) · [🌐 Site ↗](https://infinigen.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/infinigen/)</sub>

<a name="opensplat"></a>
### #&#8288;29 [opensplat](https://github.com/webodm/opensplat) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · AGPL-3.0 · Oct 2026</sub>

**C++ trainer that turns COLMAP or OpenSfM camera poses into 3D gaussian splats.**

OpenSplat is a command-line C++ implementation of 3D gaussian splatting. It reads camera poses and sparse points from ODX, OpenSfM, COLMAP, OpenMVG or nerfstudio projects and writes a scene as .ply, .splat, .spz or .rad. It trains on NVIDIA (CUDA), AMD (ROCm/HIP) and Apple (Metal) GPUs, or on CPU at roughly 100x slower.

- **+** Runs on CUDA, ROCm/HIP, Metal and plain CPU from one codebase
- **+** Reads ODX, OpenSfM, COLMAP, OpenMVG and nerfstudio projects directly
- **+** Supports image masks, resuming from a .ply and compressed .splat output
- **+** Documents GPU memory use: about 2 GB per million gaussians
- **−** Requires sparse points in the input; random initialization is not supported
- **−** Source build needs OpenCV and a matching libtorch, which takes manual setup
- **−** Pre-built Windows binary is sold; free route is building from source
- **−** AGPL-3.0 license constrains use in closed-source products

<sub>GPU optional · Docker · Needs libtorch, OpenCV, CUDA, ROCm, Xcode Metal toolchain, CMake · Models: COLMAP, OpenSfM, ODX, OpenMVG, nerfstudio · [Repo](https://github.com/webodm/opensplat) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opensplat/)</sub>

<a name="image-to-3dlab"></a>
### #&#8288;30 [image-to-3dlab](https://github.com/bingeljell/image-to-3dlab) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Nov 2026</sub>

**Local pipeline from text or image to rigged, animated 3D game characters.**

AssetFurnace is a browser studio that turns a sentence or picture into a textured 3D model, cleans it up for games, rigs it with SkinTokens and applies one of 21 animation presets, exporting GLB. It wraps Pixal3D, TRELLIS.2, Hunyuan3D and Stable Fast 3D on Apple Silicon, NVIDIA or AMD (ROCm), and ships an MCP server for agents. Source pictures come from FLUX.2 klein 4B or Qwen-Image run locally.

- **+** Full local pipeline: image, 3D model, rig, animation and GLB export in one studio
- **+** Pixel Match restores source-image pixels on low-poly models, keeping text and logos sharp
- **+** Runs on Apple Silicon, NVIDIA and AMD ROCm (Pixal3D only on AMD)
- **+** Built-in MCP server lets Claude Code, Codex and other agents drive it
- **−** Weights run roughly 8 to 20 GB per backend and are downloaded separately
- **−** TRELLIS.2 and Hunyuan3D-2.1 CUDA routes are Linux-only and untested on real hardware
- **−** Windows has limited testing; MCP agent use is untested there
- **−** Several backend weights carry non-OSI licences (Tencent, Stability, DINOv3)

<sub>GPU required · Needs Python 3.11, uv, Xcode (Metal builds on Mac), CUDA toolkit (some NVIDIA builds), ROCm HIP SDK (AMD), Hugging Face access for gated weights · Models: Pixal3D, TRELLIS.2, Hunyuan3D-2.1, Hunyuan3D-MLX, Stable Fast 3D · [Repo](https://github.com/bingeljell/image-to-3dlab) · [📖 Docs ↗](https://assetfurnace.com/blog/how-to-use-assetfurnace) · [🌐 Site ↗](https://assetfurnace.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/image-to-3dlab/)</sub>

<a name="fastvideo"></a>
### #&#8288;31 [fastvideo](https://github.com/hao-ai-lab/fastvideo) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (51) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · Apache-2.0 · Nov 2026</sub>

**Post-training and inference framework for accelerated video diffusion models.**

FastVideo is a Python framework for fine-tuning, distilling and running open video diffusion transformers. It covers full and LoRA finetuning, DMD2 and sparse distillation with Video Sparse Attention (claimed >50x denoising speedup), and inference through a CLI and a VideoGenerator Python API with sequence parallelism. It also ships Dreamverse, a realtime video generation web app, and supports NVIDIA, Apple Silicon (MLX), and AMD ROCm.

- **+** Covers training and inference: LoRA, full finetune, DMD2, Self-Forcing, FSDP2, sequence parallelism
- **+** Runs on NVIDIA CUDA 12/13, DGX Spark, Apple Silicon via MLX, and AMD ROCm
- **+** Publishes distilled checkpoints (FastWan, FastH3) on Hugging Face with cookbook recipes
- **+** Installs with uv pip; includes Dreamverse realtime app with a live demo
- **−** Sparse-attention speedups depend on VSA kernels, which need a separate install step
- **−** Multi-GPU use on low-RAM hosts like Colab risks OOM; README advises num_gpus=1
- **−** Model and hardware support varies; readers must check the support matrix
- **−** No Docker or compose files detected for the core framework

<sub>GPU required · Docker · Needs PyTorch, uv, VSA attention kernels · Models: Wan2.1, FastWan, FastH3 (MiniMax-H3), Kandinsky 6, PAN 2 · [Repo](https://github.com/hao-ai-lab/fastvideo) · [▶️ Demo ↗](https://dreamverse.fastvideo.org/) · [📖 Docs ↗](https://haoailab.com/FastVideo/inference/inference_quick_start/) · [🌐 Site ↗](https://haoailab.com/FastVideo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fastvideo/)</sub>

<a name="diffsynth-studio"></a>
### #&#8288;32 [diffsynth-studio](https://github.com/modelscope/diffsynth-studio) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (73) · Freshness: active (85) · Maintenance: patchy (47) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

**Python engine for running and training diffusion image, video and audio models.**

DiffSynth-Studio is a Python framework from the ModelScope community for inference and training of diffusion models covering image, video and audio generation, plus image quality metrics. It schedules weights across disk, RAM and VRAM and supports NF4 and INT8 quantization so large models run on small GPUs. Most models that support inference also support LoRA or full training.

- **+** Inference and training for most supported models, including LoRA and adapter models
- **+** VRAM offloading and quantization (bitsandbytes, torchao, EntroPack) for low-VRAM GPUs
- **+** Broad model coverage: Wan, LTX-2, Qwen-Image, FLUX, ACE-Step, Stable Diffusion
- **+** Separate ComfyUI node package and LoRA training WebUI built on it
- **−** Code-first library; the README describes no built-in web UI
- **−** Only two main maintainers; README warns of slow issue responses
- **−** Major version update dropped some older features
- **−** Last release was 2025-11-18, while new models land on the main branch

<sub>GPU optional · Needs PyTorch · Models: Wan, LTX-2, Qwen-Image, FLUX.2, Z-Image · [Repo](https://github.com/modelscope/diffsynth-studio) · [▶️ Demo ↗](https://modelscope.cn/studios/DiffSynth-Studio/Diffusion-Templates) · [📖 Docs ↗](https://diffsynth-studio-doc.readthedocs.io/en/latest/README.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/diffsynth-studio/)</sub>

<a name="viseron"></a>
### #&#8288;33 [viseron](https://github.com/roflcoopter/viseron) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Nov 2026</sub>

**Local-only NVR with object, motion and face detection for IP cameras.**

Viseron is a self-hosted network video recorder with computer vision features: object detection, motion detection and face recognition. It is configured through a built-in web interface, and its functionality is split into components listed in a Component Explorer. The README states it runs locally only and is started as a Docker container.

- **+** Runs locally only, so camera footage stays on your own host
- **+** Configuration file is editable from the built-in web interface
- **+** Modular components, with a searchable Component Explorer in the docs
- **+** MIT licensed Python project with an active Discord community
- **−** README gives no hardware, RAM or GPU guidance
- **−** README lists no supported detection models or camera protocols
- **−** Configuration is component-based and has a learning curve
- **−** Support is mainly handled through Discord rather than documented guides

<sub>Docker · Needs Docker · [Repo](https://github.com/roflcoopter/viseron) · [📖 Docs ↗](https://viseron.netlify.app) · [🌐 Site ↗](https://viseron.netlify.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/viseron/)</sub>

<a name="dsh-image-gen"></a>
### #&#8288;34 [dsh-image-gen](https://github.com/shanliuling/dsh-image-gen) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · Apache-2.0 · Nov 2026</sub>

**Image generation plugin for DeepSeek Harness with batch, canvas editing and GIF output.**

A plugin for DeepSeek Harness (DSH) that lets the chat agent generate images through Gemini, OpenAI and compatible relays, Seedream, DashScope, Grok Imagine, GLM-Image or a local ComfyUI. It supports batches of up to 10 images per call, canvas sketch and region edits, GIF and SVG output, a Studio workbench, multi-model comparison, and 500+ reusable prompt templates. ChatGPT, Grok and Google subscriptions can log in instead of using API keys.

- **+** Agent plans and generates up to 10 images per message; one failure does not stop the rest
- **+** Many providers, including subscription login for ChatGPT, Grok and Google without an API key
- **+** Agent reads canvas sketches and circled regions for targeted edits
- **+** Local ComfyUI workflows with {{prompt}}, {{seed}}, {{width}}, {{image}} placeholders
- **−** Works only inside DeepSeek Harness; Node.js ^22.19.0 or >=24 required
- **−** README states no full SSRF target restriction for upstream image downloads by default
- **−** ComfyUI is not available in Studio or multi-model comparison
- **−** GIF output only via OpenAI and compatible relays, and depends on relay support

<sub>GPU optional · Needs DeepSeek Harness, Node.js ^22.19.0 or >=24, pnpm, ComfyUI (optional) · Models: Google Gemini, OpenAI Images, OpenAI-compatible relays, ByteDance Seedream, Aliyun DashScope / Qwen Image · [Repo](https://github.com/shanliuling/dsh-image-gen) · [📖 Docs ↗](https://github.com/shanliuling/dsh-image-gen/blob/main/docs/providers.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dsh-image-gen/)</sub>

<a name="swarmui"></a>
### #&#8288;35 [swarmui](https://github.com/mcmonkeyprojects/swarmui) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (33) · Freshness: active (92) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · MIT · Nov 2026</sub>

**Web UI for image, video and audio generation with a ComfyUI backend.**

SwarmUI is a C# web interface for generating images, video and some audio with diffusion models. It auto-installs ComfyUI as the default backend and can also use AUTOMATIC1111. It has a simple Generate tab, a raw Comfy Workflow tab and tools such as a Grid Generator, and it can spread jobs across multiple GPUs.

- **+** Generate tab for simple use, plus raw ComfyUI graph tab for advanced workflows
- **+** Multi-GPU support for large grid generations, the origin of the Swarm name
- **+** Covers image, video and some audio models (Flux, Wan, LTX-2, ACE-Step)
- **+** Extension system and one-file installers for Windows and Linux
- **−** Still labeled Beta (Almost-Release); some areas are unfinished
- **−** LLM-assisted prompting is only an extension, not built in
- **−** Mac support limited to Apple silicon; Linux desktop app mode untested
- **−** Optional dependencies such as ultralytics (AGPL) can bring in GPL/AGPL terms

<sub>Needs git, Python 3.10-3.13, .NET 8 SDK, ComfyUI (auto-installed) · Models: Stable Diffusion, Flux, Wan, LTX-2, ACE-Step · port 7801 · [Repo](https://github.com/mcmonkeyprojects/swarmui) · [📖 Docs ↗](https://github.com/mcmonkeyprojects/SwarmUI/blob/master/docs/README.md) · [🌐 Site ↗](https://swarmui.net/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/swarmui/)</sub>

<a name="clearcam"></a>
### #&#8288;36 [clearcam](https://github.com/roryclear/clearcam) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · GPL-3.0 · Nov 2026</sub>

**Self-hosted NVR adding object detection and phone alerts to RTSP cameras.**

Clearcam is a Python network video recorder that runs object detection and tracking on RTSP camera streams, records events, and serves a web UI on port 8080. Alerts can go to its iOS and Android apps or to a custom URL, such as Home Assistant, Pushover or n8n. Notification summaries use Qwen3 VL. Remote viewing and push alerts through its own service need a paid premium account.

- **+** Notification URL is configurable, so alerts can go to Home Assistant, Pushover or n8n
- **+** Web UI on localhost:8080 for live view, events and recording playback
- **+** Runs from source with pip install and one command; AMD and NVIDIA selectable via DEV
- **+** Sample Pushover notification server included in utils/sample_server.py
- **−** Windows is not supported; the README says an ffmpeg fix is needed
- **−** Remote streams and app push notifications require a paid premium account
- **−** No Docker image or compose file in the repository
- **−** Requires Python 3.11 or later and ffmpeg installed on the host

<sub>GPU optional · Needs ffmpeg, python3.11+ · Models: Qwen3 VL · port 8080 · [Repo](https://github.com/roryclear/clearcam) · [🌐 Site ↗](https://www.clearcam.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clearcam/)</sub>

<a name="wan2-2"></a>
### #&#8288;37 [wan2.2](https://github.com/wan-video/wan2.2) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: weak (14) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Sep 2026</sub>

**Open-weight video generation models for text, image, speech and animation.**

Wan2.2 is Alibaba's video diffusion model family with a generate.py CLI for text-to-video, image-to-video, speech-to-video and character animation. It ships a MoE A14B pair for 480P/720P and a 5B TI2V model at 720P/24fps with a 16x16x4 compression VAE. Weights are on Hugging Face and ModelScope, and multi-GPU inference uses FSDP with DeepSpeed Ulysses.

- **+** Covers T2V, I2V, TI2V, speech-to-video and character animation in one repo
- **+** TI2V-5B runs 720P at 24fps on a single 24GB GPU such as an RTX 4090
- **+** Multi-GPU inference with FSDP and DeepSpeed Ulysses is included
- **+** Integrated into ComfyUI and Diffusers, with weights on Hugging Face and ModelScope
- **−** A14B single-GPU inference needs at least 80GB VRAM
- **−** CLI scripts only; no built-in web UI or server
- **−** Prompt extension needs a Dashscope API key or a local Qwen model
- **−** Requires torch >= 2.4.0 and flash_attn, which can fail to install

<sub>GPU required · Needs PyTorch >= 2.4.0, flash_attn, Dashscope API (optional, prompt extension), CosyVoice (optional, speech-to-video TTS) · Models: Wan2.2-T2V-A14B, Wan2.2-I2V-A14B, Wan2.2-TI2V-5B, Wan2.2-S2V-14B, Wan2.2-Animate-14B · [Repo](https://github.com/wan-video/wan2.2) · [▶️ Demo ↗](https://huggingface.co/spaces/Wan-AI/Wan-2.2-5B) · [📖 Docs ↗](https://alidocs.dingtalk.com/i/nodes/EpGBa2Lm8aZxe5myC99MelA2WgN7R35y) · [🌐 Site ↗](https://wan.video) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/wan2-2/)</sub>

<a name="local-dream"></a>
### #&#8288;38 [local-dream](https://github.com/xororz/local-dream) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · custom license · Nov 2026</sub>

**Android app that runs Stable Diffusion on-device, with Snapdragon NPU acceleration.**

Local Dream is a Kotlin Android app that generates images with Stable Diffusion 1.5 and SDXL entirely on the phone. It uses the Qualcomm QNN SDK for Snapdragon NPU inference and MNN for CPU/GPU fallback, and includes Real-ESRGAN and UltraSharpV2 upscalers plus an NSFW filter. Guides and documentation live on a separate site.

- **+** NPU inference on Snapdragon: SD1.5 on Hexagon V68 or newer, SDXL on 8 Gen 3+
- **+** CPU/GPU fallback through MNN for devices without a supported NPU
- **+** Built-in upscaling with Real-ESRGAN and UltraSharpV2
- **+** Runs fully on device, no server required
- **−** NPU path limited to Snapdragon; other SoCs only get CPU/GPU
- **−** SDXL needs substantially more memory than SD1.5
- **−** Only SD1.5 and SDXL are supported; SD2.1 is no longer maintained
- **−** License is not a recognized standard identifier (NOASSERTION); check before reuse

<sub>GPU optional · Needs Qualcomm QNN SDK, MNN · Models: SD1.5, SDXL · [Repo](https://github.com/xororz/local-dream) · [📖 Docs ↗](https://ld-guide.chino.icu) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/local-dream/)</sub>

<a name="hunyuanvideo"></a>
### #&#8288;39 [hunyuanvideo](https://github.com/tencent-hunyuan/hunyuanvideo) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · custom license · Oct 2026</sub>

**Text-to-video diffusion model with PyTorch inference code and weights.**

Tencent's 13B-parameter text-to-video model, released with PyTorch model definitions, pretrained weights and inference code. It uses a dual-stream to single-stream transformer, an MLLM text encoder and a causal 3D VAE. The repo includes a Gradio demo, xDiT multi-GPU parallel inference, FP8 weights and a prompt-rewrite model.

- **+** Open weights plus inference code, with Diffusers and ComfyUI integrations
- **+** FP8 weights and xDiT sequence-parallel inference for multi-GPU speedup
- **+** Includes Gradio web demo and prompt-rewrite model with Normal and Master modes
- **+** Active ecosystem of community accelerators, GGUF quantizations and LoRAs
- **−** Needs 45GB GPU memory at 544x960, 60GB at 720x1280 for 129 frames
- **−** NVIDIA CUDA only; tested on Linux only
- **−** License is not a standard SPDX identifier (NOASSERTION); check terms before use
- **−** Tencent has since released HunyuanVideo-1.5, a newer successor model

<sub>GPU required · Needs PyTorch 2.7.1, CUDA 11.8 or 12.6, flash-attention 2.8.3, xfuser 0.4.0, conda · Models: HunyuanVideo T2V (13B), FP8 weights, Diffusers, HunyuanVideo-PromptRewrite · [Repo](https://github.com/tencent-hunyuan/hunyuanvideo) · [▶️ Demo ↗](https://video.hunyuan.tencent.com) · [📖 Docs ↗](https://huggingface.co/docs/diffusers/main/api/pipelines/hunyuan_video) · [🌐 Site ↗](https://aivideo.hunyuan.tencent.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hunyuanvideo/)</sub>

<a name="vimax"></a>
### #&#8288;40 [vimax](https://github.com/hkuds/vimax) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Sep 2026</sub>

**Agent pipeline that turns ideas, scripts or novels into multi-shot videos.**

ViMax chains LLM, image and video generation APIs to turn a short idea, a screenplay or a novel into a multi-scene video. It handles scriptwriting, character references, storyboards, shot design and final assembly. It ships a TUI, a local Web UI with named projects and render previews, and direct Python entrypoints (Idea2Video, Script2Video, Novel2Video, AutoCameo).

- **+** Covers script, storyboard, shot design and assembly in one pipeline, not just clip generation
- **+** Separate entrypoints for idea, screenplay and novel input, plus reference-photo cameo
- **+** Generates 2 keyframe candidates and picks one with a vision chat model; configurable
- **+** Local Web UI and TUI with session resume; MIT licensed
- **−** Needs external LLM, image and video API keys; no local model path documented
- **−** API cost rises with image selection, which generates 2 candidates per keyframe by default
- **−** No Docker or compose files; setup is uv sync plus Node.js 18+ for the Web UI
- **−** README lists Linux and Windows only; hardware requirements and output length limits are unknown

<sub>no GPU · Needs uv, Python 3.12, Node.js 18+ (Web UI), LLM API key, image generation API key, video generation API key · Models: OpenAI-compatible chat APIs, OpenRouter, Google Gemini / Nano Banana, Google Veo, Seedance 2.0 Fast · port 4173 · [Repo](https://github.com/hkuds/vimax) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vimax/)</sub>

<a name="faceswap"></a>
### #&#8288;41 [faceswap](https://github.com/deepfakes/faceswap) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: widely used (96) · Freshness: active (85) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · GPL-3.0 · Aug 2026</sub>

**Python tool that trains neural models to swap faces in images and video.**

FaceSwap is a Python program with three stages run through `faceswap.py`: extract faces from photos or video frames, train a model on two sets of faces, and convert source media with the trained model. It ships a Tkinter-style GUI (`faceswap.py gui`) alongside the CLI, and includes models such as Villain and Phaze-A. It runs on Windows, Linux and macOS, with CUDA GPUs recommended and some AMD support via ROCm on Linux.

- **+** Covers the full workflow: extract, train and convert, via CLI or GUI
- **+** Multiple model architectures named in the README, including Villain, Phaze-A, DFL-H128 and DFaker
- **+** Runs on Windows, Linux and macOS; AMD GPUs supported via ROCm on Linux
- **+** Existing models can be reused to shorten training on new faces
- **−** Training requires a modern CUDA GPU for acceptable speed; exact VRAM needs are unknown
- **−** No Docker or compose setup in the repo
- **−** Setup problems are directed to the forum and Discord, not GitHub issues
- **−** Manual workflow: gathering and curating face data is left to the user

<sub>GPU required · Needs CUDA, ROCm (AMD, Linux), ffmpeg (optional) · Models: Villain, Phaze-A, DFL-H128, DFaker, Unbalanced · [Repo](https://github.com/deepfakes/faceswap) · [📖 Docs ↗](https://faceswap.readthedocs.io/en/latest/) · [🌐 Site ↗](https://faceswap.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/faceswap/)</sub>

<a name="kohya-ss"></a>
### #&#8288;42 [Kohya's GUI](https://github.com/bmaltais/kohya_ss) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (70) · Freshness: active (91) · Maintenance: weak (4) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Jul 2026</sub>

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

<sub>GPU required · Docker + Compose · Needs uv or pip, Python 3.10 with tkinter · Models: SD 1.5/2.x, SDXL, SD3, Flux.1, Lumina Image 2.0 · port 7860 · [Repo](https://github.com/bmaltais/kohya_ss) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kohya-ss/)</sub>

<a name="cadam"></a>
### #&#8288;43 [cadam](https://github.com/adam-cad/cadam) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (39) · Freshness: active (100) · Maintenance: patchy (35) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · GPL-3.0 · Oct 2026</sub>

**Text-to-CAD web app that generates parametric OpenSCAD models.**

CADAM turns plain-language descriptions or reference images into parametric OpenSCAD code, compiles it in the browser with OpenSCAD WebAssembly, and previews the result with Three.js. Extracted parameters appear as sliders, so dimensions can change without another AI call. Models export as STL, SCAD or DXF. Self-hosting uses the Supabase CLI and a TanStack Start dev server with provider API keys.

- **+** Compiles OpenSCAD in the browser via WebAssembly, so no local CAD install is needed
- **+** Parameter sliders adjust dimensions without re-running the model
- **+** Exports STL, SCAD and DXF; bundles BOSL, BOSL2 and MCAD libraries
- **+** Repo includes benchmarks/ with prompts and source for 13 sample models
- **−** Local setup needs Supabase CLI, ngrok for webhooks, and several provider API keys
- **−** No Docker or compose files; setup is manual via npm and Supabase
- **−** Only hosted LLM APIs are listed; no local model support is documented
- **−** GPL-3.0 license limits embedding in closed-source products

<sub>no GPU · Needs Node.js 20.19+ or 22.12+, Supabase CLI, ngrok, Anthropic API key, OpenRouter API key, OpenAI API key, Google API key, FAL API key · Models: Anthropic Claude, OpenRouter, OpenAI, Google · port 3000 · [Repo](https://github.com/adam-cad/cadam) · [▶️ Demo ↗](https://adam.new/cadam) · [🌐 Site ↗](https://adam.new) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cadam/)</sub>

<a name="dream-textures"></a>
### #&#8288;44 [dream-textures](https://github.com/carson-katri/dream-textures) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (56) · Freshness: recent (70) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · GPL-3.0 · Sep 2026</sub>

**Blender add-on that generates textures and images with Stable Diffusion.**

Dream Textures is a Blender add-on that runs Stable Diffusion locally to generate textures, concept art and background assets from text prompts. It adds tileable texture output, depth-to-image texture projection onto scenes, inpaint/outpaint, 4x upscaling, and a render-engine node system for re-styling animations. Tested on CUDA and Apple Silicon GPUs; DreamStudio is available as a cloud fallback.

- **+** Works inside Blender: tileable textures, depth-based texture projection and a Cycles render pass option
- **+** Includes inpaint, outpaint and 4x AI upscaling
- **+** Runs models locally, with DreamStudio as a cloud option for unsupported hardware
- **+** Generation history can be recalled, exported and imported
- **−** Last release was 2024-08-26
- **−** Tested only on CUDA and Apple Silicon GPUs
- **−** Requires Blender; not usable as a standalone tool
- **−** macOS may need a manual quarantine workaround for bundled dependencies

<sub>GPU optional · Needs Blender, PyTorch, DreamStudio (optional cloud) · Models: Stable Diffusion · [Repo](https://github.com/carson-katri/dream-textures) · [📖 Docs ↗](https://github.com/carson-katri/dream-textures/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dream-textures/)</sub>

<a name="pixelle-video"></a>
### #&#8288;45 [Pixelle-Video](https://github.com/ath-maas/pixelle-video) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: widely used (89) · Freshness: recent (75) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Jun 2026</sub>

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

<sub>Docker + Compose · Needs uv, ffmpeg, ComfyUI or RunningHub (workflow-based generation), LLM API or Ollama · Models: OpenAI GPT, Qwen (DashScope), DeepSeek, Ollama, Flux via ComfyUI (default image_flux.json) · port 8501 · [Repo](https://github.com/ath-maas/pixelle-video) · [📖 Docs ↗](https://aidc-ai.github.io/Pixelle-Video/zh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pixelle-video/)</sub>

<a name="biniou"></a>
### #&#8288;46 [biniou](https://github.com/woolverine94/biniou) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · GPL-3.0 · Nov 2026</sub>

**Gradio web UI for local text, image, audio, video and 3D generation.**

biniou is a self-hosted Gradio web UI that bundles dozens of Hugging Face based modules: a llama-cpp chatbot for GGUF models, Whisper speech-to-text, Stable Diffusion and Flux image generation, MusicGen audio, video modules and Shap-E 3D. It runs on CPU from 8GB RAM, with optional CUDA or experimental ROCm, and can work offline once models are downloaded. Install is via one-click scripts for several Linux distributions, a Windows installer, or a Dockerfile.

- **+** Covers text, image, audio, video and 3D generation in one UI
- **+** Runs on CPU only, from 8GB RAM; CUDA and experimental ROCm optional
- **+** Output of one module can be sent as input to another
- **+** Built-in model manager, LoRA and textual inversion support, and offline use after downloads
- **−** AMD64 CPUs only; macOS support is untested and experimental
- **−** Python 3.10 or 3.11 required; Windows install pulls in many system components
- **−** Many modules need 16GB+ RAM; about 200GB disk with default models
- **−** No release tags; updates are weekly commits, mostly new model entries

<sub>RAM ≥ 8 GB · GPU optional · Docker · Needs Python 3.10/3.11, git, ffmpeg, openssl, gcc, Hugging Face model downloads · Models: GGUF, Stable Diffusion, SDXL, Flux, LoRA · [Repo](https://github.com/woolverine94/biniou) · [📖 Docs ↗](https://github.com/Woolverine94/biniou/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/biniou/)</sub>

<a name="open-sora"></a>
### #&#8288;47 [open-sora](https://github.com/hpcaitech/open-sora) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: widely used (89) · Freshness: slowing (37) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Apr 2026</sub>

**Open video generation models with training and inference code.**

Open-Sora is a text-to-video and image-to-video generation project that publishes model checkpoints, inference scripts and training code. The latest release, Open-Sora 2.0, has 11B parameters, and the README reports a training cost of about $200K and VBench results comparable to HunyuanVideo (11B) and Step-Video (30B). Earlier versions (1.0 to 1.3) are kept on separate branches, and a Hugging Face Spaces Gradio demo is linked.

- **+** Checkpoints and training code released together, with a stated ~$200K training cost for 2.0
- **+** Supports text-to-video, image-to-video and video-to-video in earlier versions (1.1 documented)
- **+** Includes a video data processing pipeline and technical reports for each version
- **+** Apache-2.0 license; Hugging Face Spaces demo and sample gallery available
- **−** Last tagged release is 2025-02-21, before the 2.0 announcement in March 2025
- **−** No Docker or compose files detected
- **−** Hardware requirements are not stated in the visible README; 11B model likely needs a large GPU
- **−** Older versions live on separate branches with different checkpoints and instructions

<sub>GPU required · Needs ColossalAI · Models: Open-Sora 2.0 (11B), Open-Sora 1.3 (1B), Open-Sora 1.2, Open-Sora 1.1, Open-Sora 1.0 · [Repo](https://github.com/hpcaitech/open-sora) · [▶️ Demo ↗](https://huggingface.co/spaces/hpcai-tech/open-sora) · [🌐 Site ↗](https://hpcaitech.github.io/Open-Sora/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-sora/)</sub>

<a name="liveportrait"></a>
### #&#8288;48 [liveportrait](https://github.com/klingairesearch/liveportrait) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: widely used (81) · Freshness: recent (73) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · custom license · Jun 2026</sub>

**Animates a still portrait from a driving video, with stitching and retargeting.**

Official PyTorch implementation of the LivePortrait paper. It animates a source image or video of a human, cat or dog using motion from a driving video or a precomputed .pkl motion template. It ships CLI scripts (inference.py, inference_animals.py) and a Gradio app with pose and regional editing, and pretrained weights are hosted on Hugging Face.

- **+** Accepts image or video sources, including portrait video editing and image-driven mode
- **+** Motion templates (.pkl) speed up inference and avoid sharing the driving video
- **+** Gradio UI, Windows one-click installer and a Hugging Face Space demo are provided
- **+** Optional torch.compile gives 20-30% faster inference per the README (not on Windows or macOS)
- **−** Animals mode needs X-Pose and a compiled CUDA op; tested only with NVIDIA GPUs
- **−** Apple Silicon is not supported for Animals mode and is about 20x slower than an RTX 4090
- **−** Needs conda, FFmpeg and a manual weight download; no Docker setup
- **−** License is not detected automatically (NOASSERTION); check the repo before commercial use

<sub>GPU optional · Needs conda, FFmpeg, PyTorch, Gradio, huggingface_hub, X-Pose (Animals mode) · Models: LivePortrait Humans model, LivePortrait Animals model, KlingTeam/LivePortrait weights on Hugging Face · [Repo](https://github.com/klingairesearch/liveportrait) · [▶️ Demo ↗](https://huggingface.co/spaces/KlingTeam/LivePortrait) · [🌐 Site ↗](https://liveportrait.github.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/liveportrait/)</sub>

<a name="upscayl"></a>
### #&#8288;49 [upscayl](https://github.com/upscayl/upscayl) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: widely used (95) · Freshness: slowing (34) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 52k · AGPL-3.0 · Mar 2026</sub>

**Desktop image upscaler using Real-ESRGAN models over Vulkan.**

Upscayl is an Electron desktop app that enlarges low-resolution images with Real-ESRGAN-based models run through an NCNN Vulkan backend. It supports batch upscaling, GPU selection by ID, and custom models converted from other formats. Installers cover Windows 10+, macOS 12+ and Linux (AppImage, Flatpak, Snap, deb, rpm).

- **+** Native installers for Windows, macOS and Linux, including Flatpak, Snap, AUR and Homebrew
- **+** Batch upscaling and selectable GPU ID in the GUI
- **+** Custom models can be added; a separate repo of extra models and a conversion guide exist
- **+** Separate upscayl-ncnn CLI backend is open source under AGPLv3
- **−** Requires a Vulkan-compatible GPU; many integrated GPUs do not work
- **−** Cannot de-blur or fix focus; it only enhances low-resolution or pixelated images
- **−** Last tagged release is 2024-12-25, though commits continue into 2026
- **−** Image upscaling only; no video or generation features described

<sub>GPU required · Needs Vulkan-compatible GPU, upscayl-ncnn backend · Models: Real-ESRGAN, NCNN, custom converted models, HFA2k, Remacri · [Repo](https://github.com/upscayl/upscayl) · [📖 Docs ↗](https://docs.upscayl.org/) · [🌐 Site ↗](https://upscayl.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/upscayl/)</sub>

<a name="cinecode"></a>
### #&#8288;50 [cinecode](https://github.com/sarpstar/cinecode) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Nov 2026</sub>

**Claude Code skill that makes finished MP4 films from code.**

cinecode is a skill kit for Claude Code or Cursor. The coding agent writes the script, builds each frame in code (Canvas 2D or three.js rendered in headless Chrome), designs audio with Web Audio and ffmpeg, and outputs an MP4. A quick mode makes single-file films up to about 3 minutes; a staged film mode handles longer work, alongside ad, explainer and music-video workflows.

- **+** Runs locally with no paid service; outside voiceover is optional (Gemini key, ElevenLabs, free Turkish voices)
- **+** Quick single-file mode, or approval-gated film mode for 10+ minute videos
- **+** Built-in checks and tools: -14 LUFS mastering, hook check, per-scene loudness, 9:16/1:1/16:9 exports
- **+** Supports music-video beat grids, footage editing from Whisper transcripts, and reference-style analysis
- **−** Requires Claude Code or Cursor; plain claude.ai chat cannot run it
- **−** Longer films take more time and usage; film mode needs several GB of disk per film
- **−** A full film on Windows has not been tested end to end, per the README
- **−** Main README is in Turkish; English, Chinese and Japanese versions are separate files

<sub>GPU required · Needs Claude Code or Cursor, Node.js 22+, Python 3.9+, ffmpeg, Google Chrome, Chromium or Edge, Gemini API key (optional), ElevenLabs (optional), Whisper (optional, footage editing) · Models: Claude Code, Cursor, Gemini TTS, ElevenLabs, EMA Lightning · [Repo](https://github.com/sarpstar/cinecode) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cinecode/)</sub>

<a name="openjutsu"></a>
### #&#8288;51 [openjutsu](https://github.com/d3voz/openjutsu) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: patchy (41) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · MIT · Oct 2026</sub>

**Next.js front end for swapping characters and objects in video via ComfyUI.**

Openjutsu replaces the main person in a video with a character from a photo, or edits hair, clothes and objects, while keeping camera, cuts, motion and soundtrack. It is a small Next.js app over ComfyUI workflows that use MiniMax H3 for video, SAM 3.1 for tracking and Qwen3-VL 8B for describing frames. Modes include simple and multi-person swap, object change/remove/add, picture-based relighting, face fixing and colour grading.

- **+** Covers single and multi-person swap, object edit, face fix and colour grading in one UI
- **+** Check mask previews SAM tracking in about a minute before a full render
- **+** Pre-flight check lists missing custom nodes and model files with destinations
- **+** Runs on open weights locally; tested on a 16 GB RTX 4060 Ti
- **−** Needs about a dozen ComfyUI custom node packs plus many large model files
- **−** Slow: a 6 s clip at 480p takes about 6-13 minutes on a 4060 Ti
- **−** Mirrors and reflections do not work; the original person leaks into the result
- **−** Requires ComfyUI 0.41.2+, an NVIDIA GPU and 64 GB RAM in the tested setup

<sub>RAM ≥ 64 GB · GPU required · Needs ComfyUI 0.41.2+, comfy-api-proxy 0.1.6, Node.js 22.6+, Python, ComfyUI custom node packs (SolarRenderer, KJNodes, VideoHelperSuite, comfyui-h3-oneclick-swap and others) · Models: MiniMax H3, SAM 3.1, Qwen3-VL 8B INT8, Qwen3-VL 4B FP8, Gemma 4 E2B INT8 · port 3000 · [Repo](https://github.com/d3voz/openjutsu) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openjutsu/)</sub>

<a name="digital-human-koubo"></a>
### #&#8288;52 [digital-human-koubo](https://github.com/andyhuo520/digital-human-koubo) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · MIT · Oct 2026</sub>

**Agent skill that turns a photo and a prompt into a talking-head video.**

An Agent Skill (SKILL.md plus Python, shell and Remotion scripts) that drives an AI agent through script writing, lip-synced presenter clips via Renoise MCP (Grok Video 1.5), whisper QA, voice unification and Remotion editing. It ships five editing templates and 48 packaging components, and adds a cover as the first frame. Generation is paid through Renoise credits, and the agent quotes the cost before batching.

- **+** Cost quote and first-segment approval before batch generation
- **+** Whisper back-check and frame inspection catch wrong words and burned-in subtitles
- **+** Fixed presenter in persona.json keeps the same face across videos
- **+** Five Remotion style templates with 48 named packaging components, 9:16 adaptive
- **−** Video generation requires a Renoise account and paid credits
- **−** Text-behind-presenter effect needs macOS Apple Vision
- **−** Needs an agent that loads skills, connects MCP and runs local commands
- **−** Swapping in a different voice leaves about 100 ms lip offset

<sub>no GPU · Needs Renoise MCP (renoise.ai account, credits), ffmpeg, Python 3 with numpy and Pillow, Node.js 18+ (Remotion), whisper.cpp with ggml-medium-q5_0 model, Playwright + Chromium, Xiaomi MiMo TTS API (optional) · Models: Grok Video 1.5, Wan 3.0, OmniHuman, GPT Image 2.5, Xiaomi MiMo TTS · [Repo](https://github.com/andyhuo520/digital-human-koubo) · [▶️ Demo ↗](https://github.com/andyhuo520/digital-human-koubo/releases/download/v1.0.0/workbuddy-live-ad.mp4) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/digital-human-koubo/)</sub>

<a name="hivisionidphotos"></a>
### #&#8288;53 [hivisionidphotos](https://github.com/zeyi-lin/hivisionidphotos) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: widely used (84) · Freshness: recent (59) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Jul 2026</sub>

**Offline ID photo maker: portrait matting, background swap, sizing and print layouts.**

HivisionIDPhotos cuts out the person with ONNX matting models (MODNet, hivision_modnet, RMBG-1.4, BiRefNet-v1-lite), detects the face, then crops and resizes to standard ID photo sizes with a chosen background color. It also produces print layout sheets (6-inch, 5-inch, A4, 3R, 4R). It runs as a Gradio demo, a CLI script, or a REST API, and the default models run on CPU.

- **+** Default MODNet + MTCNN runs on CPU: about 410MB RAM and 0.2s per image on an M1 Max
- **+** Gradio UI, inference.py CLI and deploy_api.py REST API all included
- **+** Fully offline; Face++ cloud face detection is optional
- **+** Preset sizes and colors editable through CSV files
- **−** BiRefNet-v1-lite, the most accurate matting option, needs about 6GB RAM and ~16GB VRAM on GPU
- **−** Model weights must be downloaded separately before running
- **−** README and docs are mainly Chinese; English is in a separate file
- **−** Last release is 2025-01-21; the smart outfit-change feature is still marked waiting

<sub>GPU optional · Docker + Compose · Needs onnxruntime, Face++ API (optional) · Models: MODNet, hivision_modnet, RMBG-1.4, BiRefNet-v1-lite, MTCNN · port 7860 · [Repo](https://github.com/zeyi-lin/hivisionidphotos) · [▶️ Demo ↗](https://huggingface.co/spaces/TheEeeeLin/HivisionIDPhotos) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hivisionidphotos/)</sub>

<a name="hunyuandit"></a>
### #&#8288;54 [hunyuandit](https://github.com/tencent-hunyuan/hunyuandit) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · custom license · Oct 2026</sub>

**Bilingual Chinese-English text-to-image diffusion transformer with training and ControlNet.**

PyTorch model definitions, pre-trained weights and inference code for Hunyuan-DiT, a latent diffusion transformer that uses a bilingual CLIP and multilingual T5 text encoder. The repo also covers full-parameter and LoRA training, ControlNet (canny, pose, depth), IP-Adapter, a captioner, and a DialogGen-based multi-turn Gradio demo. Diffusers, ComfyUI and Kohya integrations are provided.

- **+** Handles Chinese and English prompts via bilingual CLIP plus mT5 encoders
- **+** Ships training code: full-parameter and LoRA, plus ControlNet and IP-Adapter
- **+** Integrations for Diffusers, ComfyUI and Kohya; Gradio and CLI demos
- **+** Distillation and TensorRT versions reported at 50% and 47% faster; 6GB VRAM scripts
- **−** Requires an NVIDIA CUDA GPU; minimum 11GB peak memory for the standard pipeline
- **−** Tested only on Linux with V100 and A100 GPUs
- **−** Docker images are tar downloads, not a published registry image or compose file
- **−** Hunyuan-DiT-S checkpoints and a WebUI are still unchecked in the plan

<sub>GPU required · Needs PyTorch, CUDA, Conda, flash-attention, huggingface-cli · Models: Hunyuan-DiT v1.1, Hunyuan-DiT v1.2, Distillation, ControlNet, LoRA · [Repo](https://github.com/tencent-hunyuan/hunyuandit) · [▶️ Demo ↗](https://hunyuan.tencent.com/bot/chat) · [🌐 Site ↗](https://dit.hunyuan.tencent.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hunyuandit/)</sub>

<a name="turbodiffusion"></a>
### #&#8288;55 [turbodiffusion](https://github.com/thu-ml/turbodiffusion) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · Apache-2.0 · Nov 2026</sub>

**Speeds up Wan video diffusion models with distilled 4-step sampling.**

TurboDiffusion accelerates text-to-video and image-to-video generation for Wan2.1 and Wan2.2 models. It combines SageAttention and Sparse-Linear Attention (SageSLA), W8A8 quantized linear layers, and rCM timestep distillation to sample in 1-4 steps. The README reports a 5-second 480p clip in 1.9s versus 184s originally, and a 720p I2V run in 38s versus 4549s, both on one RTX 5090.

- **+** Reported 100-200x end-to-end speedup on one RTX 5090, excluding text encoding and VAE decoding
- **+** Quantized checkpoints for RTX 5090/4090 and unquantized ones for 40GB+ GPUs like H100
- **+** Covers Wan2.1 T2V (1.3B, 14B) and Wan2.2 I2V A14B at 480p and 720p
- **+** Terminal interactive mode allows multi-turn generation without reloading the model
- **−** Models trained only on long English prompts; other prompts need augmentation
- **−** README says checkpoints and paper are not finalized and will be updated
- **−** Builds with pip --no-build-isolation; torch 2.8.0 recommended, newer versions may OOM
- **−** H3 model license excludes the US, EU, UK and Republic of Korea

<sub>GPU required · Needs PyTorch >=2.7.0 (2.8.0 recommended), Python >=3.9, SageAttention, SpargeAttn (optional, for SageSLA), Wan2.1 VAE and umT5 text encoder checkpoints · Models: Wan2.1-T2V-1.3B-480P, Wan2.1-T2V-14B-480P, Wan2.1-T2V-14B-720P, Wan2.2-I2V-A14B-720P, TurboH3-FL2VA-I2VA · [Repo](https://github.com/thu-ml/turbodiffusion) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/turbodiffusion/)</sub>

<a name="rgthree-comfy"></a>
### #&#8288;56 [rgthree-comfy](https://github.com/rgthree/rgthree-comfy) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (17) · Freshness: recent (70) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Oct 2026</sub>

**Custom nodes that tidy and speed up ComfyUI workflows.**

rgthree-comfy is a ComfyUI custom node pack for workflow organization: Seed control, Reroute, Context and Context Switch, Power Lora Loader, Power Prompt, Image Comparer, and Fast Muter/Bypasser nodes. Power Puter evaluates code expressions to compute outputs. The author says the nodes were built for personal use cases.

- **+** Power Lora Loader handles any number of Loras with per-row toggles in one node
- **+** Fast Groups Muter toggles whole groups, with filters by color, title and sort order
- **+** Context Switch picks the first non-empty input, so muted branches skip their work
- **+** Install is a git clone into custom_nodes; settings live in rgthree_config.json
- **−** Author says nodes were made for own use cases, so fit for others varies
- **−** Last tagged release is 2023-09-12, though commits continue
- **−** Requires a working ComfyUI install; not usable standalone
- **−** Muting and switch behavior needs learning; README devotes a section to explaining it

<sub>Needs ComfyUI · Models: SDXL prompt nodes, Loras, embeddings · [Repo](https://github.com/rgthree/rgthree-comfy) · [📖 Docs ↗](https://github.com/rgthree/rgthree-comfy/wiki/Node:-Power-Puter) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rgthree-comfy/)</sub>

<a name="nunchaku"></a>
### #&#8288;57 [nunchaku](https://github.com/nunchux-ai/nunchaku) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (21) · Freshness: active (91) · Maintenance: weak (21) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · Apache-2.0 · Sep 2026</sub>

**4-bit SVDQuant inference engine for FLUX, Qwen-Image and SANA diffusion models.**

Nunchaku is a Python inference engine that runs diffusion models quantized to 4-bit weights and activations using SVDQuant, with fused kernels for the low-rank branch. The README reports a 3.6x memory reduction on 12B FLUX.1-dev and about 3x speedup over an NF4 W4A16 baseline on RTX 4090. It supports INT4 and NVFP4 (RTX 5090), LoRA, ControlNet, CPU offloading, and a ComfyUI plugin.

- **+** Reported 3.6x memory reduction and about 3x speedup over NF4 on FLUX.1-dev
- **+** Supports INT4 and NVFP4 precision, including 20-series and RTX 5090 GPUs
- **+** Offloading cuts Qwen-Image VRAM to about 3 GiB and FLUX to 4 GiB
- **+** ComfyUI plugin, Gradio demo apps and Python examples for many models
- **−** Needs NVIDIA GPU; no CPU-only or non-NVIDIA backend is described
- **−** Models must be pre-quantized, or quantized separately with DeepCompressor
- **−** Covers diffusion models only; no LLM serving or HTTP API
- **−** Last tagged release is January 2026, while main has later commits

<sub>GPU required · Needs PyTorch, ComfyUI (optional plugin), DeepCompressor (optional, for quantization) · Models: FLUX.1-dev, FLUX.1-Kontext, FLUX.1-Krea-dev, FLUX.1-tools, Qwen-Image · [Repo](https://github.com/nunchux-ai/nunchaku) · [▶️ Demo ↗](https://nunchux.ai/) · [📖 Docs ↗](https://nunchaku.tech/docs/nunchaku/) · [🌐 Site ↗](https://hanlab.mit.edu/projects/svdquant) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nunchaku/)</sub>

<a name="duix-avatar"></a>
### #&#8288;58 [duix-avatar](https://github.com/duixcom/duix-avatar) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: popular (78) · Freshness: recent (51) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · custom license · Apr 2026</sub>

**Offline talking-avatar video generator with voice cloning and lip-sync.**

Duix.Avatar clones a person's face and voice from a short video, then renders lip-synced videos driven by text or audio. It runs as an Electron client plus Docker services for ASR (fun-asr), TTS (fish-speech-ziming) and video synthesis, all on a local NVIDIA GPU. The services expose local HTTP endpoints for voice synthesis (port 18180) and video synthesis (port 8383).

- **+** Runs fully offline; all compute is local, so no footage leaves the machine
- **+** Exposes local HTTP APIs for audio synthesis (18180) and video synthesis (8383)
- **+** Scripts supported in eight languages, including English, Chinese, Japanese and Spanish
- **+** Clients for Windows (installer) and Ubuntu 22.04 (AppImage); lite compose file available
- **−** Requires an NVIDIA GPU; services will not start without one
- **−** Heavy setup: about 70GB of image downloads and 100GB free disk recommended
- **−** Non-real-time only; interactive avatars are routed to the paid duix.com service
- **−** Custom license: enterprises above 100,000 users or 10M USD revenue need a commercial agreement

<sub>RAM ≥ 32 GB · GPU required · Compose · Needs Docker, NVIDIA Container Toolkit, Node.js 18, guiji2025/fun-asr, guiji2025/fish-speech-ziming, guiji2025/duix.avatar · Models: fun-asr, fish-speech-ziming · [Repo](https://github.com/duixcom/duix-avatar) · [📖 Docs ↗](https://docs.duix.com/api-reference/api/Introduction) · [🌐 Site ↗](http://www.duix.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/duix-avatar/)</sub>

<a name="personalive"></a>
### #&#8288;59 [personalive](https://github.com/gvclab/personalive) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · Apache-2.0 · Aug 2026</sub>

**Real-time diffusion portrait animation driven by a webcam or video.**

PersonaLive animates a single reference portrait image from a driving video or webcam, using a streaming diffusion pipeline that can produce arbitrarily long output. It ships a web UI on port 7860, an offline inference script, optional TensorRT acceleration and three-stage training code. It is CVPR 2026 research code, and the README limits use to academic research.

- **+** Streaming generation produces long videos on 12GB VRAM in offline mode
- **+** Web UI for live animation; optional TensorRT build gives about 2x speedup
- **+** Includes three-stage training code and weights on Hugging Face and ModelScope
- **+** ComfyUI integration exists as a community project
- **−** README states academic research use only, limiting practical deployment
- **−** TensorRT engine should be rebuilt locally (~20 minutes); shipped one is from an H100
- **−** xformers is incompatible with RTX 50-series; acceleration must be disabled there
- **−** No Docker files; manual conda, Node.js 18+ and weight download setup

<sub>GPU required · Needs conda, Python 3.10, Node.js 18+, xformers or TensorRT (optional) · Models: sd-image-variations-diffusers, sd-vae-ft-mse, PersonaLive .pth weights, ONNX, TensorRT · port 7860 · [Repo](https://github.com/gvclab/personalive) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/personalive/)</sub>

<a name="mochi"></a>
### #&#8288;60 [mochi](https://github.com/genmoai/mochi) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · Apache-2.0 · Oct 2026</sub>

**10B-parameter text-to-video diffusion model with inference code and LoRA trainer.**

Mochi 1 is Genmo's open-weight text-to-video model, a 10B AsymmDiT diffusion transformer paired with a 362M AsymmVAE and a T5-XXL text encoder. The repo provides a Gradio UI, a CLI, a Python pipeline API, and a LoRA fine-tuning trainer. Output is 480p, and the native implementation needs about 60GB VRAM on a single GPU.

- **+** Apache-2.0 weights, with the 10B DiT and VAE both released
- **+** Ships Gradio UI, CLI and a composable Python pipeline API
- **+** LoRA fine-tuning on a single H100 or A100 80GB
- **+** Supports multi-GPU context parallel inference as well as single GPU
- **−** Needs about 60GB VRAM on one GPU; H100 recommended
- **−** Generates 480p only, with warping on extreme motion
- **−** Weak on animated content; tuned for photorealistic styles
- **−** README says GPU inference and fine-tuning still need qualification before deployment

<sub>GPU required · Needs FFmpeg, uv, Python 3.11, T5-XXL text encoder · Models: Mochi 1 preview (AsymmDiT 10B, safetensors), AsymmVAE, LoRA safetensors · [Repo](https://github.com/genmoai/mochi) · [▶️ Demo ↗](https://www.genmo.ai/play) · [🌐 Site ↗](https://www.genmo.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mochi/)</sub>

<a name="comfyui-copilot"></a>
### #&#8288;61 [comfyui-copilot](https://github.com/ath-maas/comfyui-copilot) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (40) · Freshness: recent (77) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · MIT · Sep 2026</sub>

**ComfyUI custom node that generates, debugs and rewrites workflows from chat.**

A ComfyUI custom node that adds a chat panel for building workflows from text, debugging broken ones, rewriting the current canvas, and recommending nodes and models. It also includes GenLab, which batch-runs parameter ranges and shows comparison results. Chat and workflow-generation models are configured separately, with OpenAI and LM Studio named as options.

- **+** Debug button finds parameter and connection errors and prompts download of missing models
- **+** GenLab batch-runs parameter ranges and renders visual comparisons
- **+** Chat and workflow-generation models are set separately; OpenAI and LM Studio supported
- **+** Installs as a custom_nodes git clone plus pip requirements
- **−** Hosted API suspended; users must supply their own API key and base URL
- **−** Node info query, job recommendations and workflow generation are being withdrawn
- **−** Models released after May 2025 (e.g. wan2.2) can break workflow rewriting
- **−** Long rewrite contexts interrupt; user must clear context manually

<sub>Needs ComfyUI, Python 3.10+, OpenAI-compatible LLM API key and base URL · Models: OpenAI, LM Studio · [Repo](https://github.com/ath-maas/comfyui-copilot) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/comfyui-copilot/)</sub>

<a name="watermark-removal"></a>
### #&#8288;62 [watermark-removal](https://github.com/zuruoke/watermark-removal) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (37) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 5.2k · no license · Oct 2026</sub>

**Command-line watermark remover using TensorFlow image inpainting.**

Removes watermarks from single images with a deep inpainting model based on Contextual Attention and Gated Convolution. It runs as a Python CLI (main.py) or a Docker image, taking an input image, an output path, a checkpoint directory and a --watermark_type flag (the example uses istock). Pretrained weights are downloaded manually from Google Drive.

- **+** Dockerfile bundles the TensorFlow 1.15 environment, avoiding a manual legacy install
- **+** Built on published inpainting methods: Contextual Attention (CVPR 2018) and Gated Convolution (ICCV 2019)
- **+** Simple CLI: one image in, one image out, with a checkpoint directory flag
- **−** Pinned to TensorFlow 1.15.0 and neuralgym, which are long out of date
- **−** The Google Colab route is labelled broken in the README
- **−** Pretrained model must be fetched manually from a Google Drive folder
- **−** Only the istock watermark type is shown; other types are undocumented

<sub>Docker · Needs TensorFlow 1.15.0, neuralgym, Docker, Pretrained checkpoint (Google Drive) · Models: Contextual Attention inpainting, Gated Convolution inpainting · [Repo](https://github.com/zuruoke/watermark-removal) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/watermark-removal/)</sub>

<a name="html-video"></a>
### #&#8288;63 [html-video](https://github.com/nexu-io/html-video) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (35) · Freshness: active (80) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · Apache-2.0 · Jun 2026</sub>

**Turns prompts, articles or repos into MP4 videos via a local coding agent.**

html-video has a local coding agent write a storyboard and one animated HTML frame per scene. Each frame is recorded in headless Chromium and the frames are concatenated into an MP4 with ffmpeg (libx264). It ships a browser studio on port 3071, a CLI, 21 license-tagged templates, and optional MiniMax music and narration. Only the Hyperframes engine is implemented; Remotion, Motion Canvas and Revideo adapters are planned.

- **+** Renders MP4 locally with headless Chromium and ffmpeg; no per-render fees
- **+** Supports 14 agent backends, auto-detected on PATH, plus the Anthropic API
- **+** Builds multi-scene videos from a URL or GitHub repo fetched server-side
- **+** Templates carry YAML manifests with SPDX license and attribution flags
- **−** Only the Hyperframes engine works; other engine adapters are roadmap items
- **−** Needs Node 20+, pnpm 9+, ffmpeg and Playwright Chromium installed manually
- **−** Soundtrack requires a MiniMax API key from a third-party service
- **−** No release published and no Docker setup; build from source with pnpm

<sub>no GPU · Needs Node.js 20+, pnpm 9+, ffmpeg, Chromium (Playwright), a coding agent CLI or Anthropic API key, MiniMax API key (optional) · Models: Claude Code, Codex CLI, Gemini CLI, Cursor Agent, Qwen Code · port 3071 · [Repo](https://github.com/nexu-io/html-video) · [🌐 Site ↗](https://open-design.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/html-video/)</sub>

<a name="llmsresearch-paperbanana"></a>
### #&#8288;64 [paperbanana](https://github.com/llmsresearch/paperbanana) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · MIT · Sep 2026</sub>

**Generates academic paper diagrams and plots from method text via a multi-agent pipeline.**

Unofficial implementation of the PaperBanana paper. It turns methodology text or PDFs plus a caption into publication-style diagrams using a retriever, planner, stylist, visualizer and critic loop. Statistical plots are rendered from CSV/JSON via VLM-generated matplotlib code. It ships a CLI, Python API, MCP server, Claude Code skills and a local Gradio UI.

- **+** Supports OpenAI, Azure, Gemini, Atlas Cloud and OpenRouter providers, selectable per run
- **+** Batch manifests (YAML/JSON) with composite multi-panel figures and Markdown/HTML reports
- **+** Accepts PDF input with page selection and reference sketch images to guide the planner
- **+** Plots need only a VLM, no image-generation provider; venue style packs are customizable
- **−** Requires a cloud API key; no local model path is described
- **−** README states it may differ from the original paper's system
- **−** Gemini image model is listed at $0.134 per 1K image, so runs cost money
- **−** Reference retrieval draws on a curated set of only 13 example diagrams

<sub>no GPU · Docker · Needs OpenAI, Azure OpenAI, Google Gemini, Atlas Cloud or OpenRouter API key, PyMuPDF (optional, for PDF input), Gradio (optional, for Studio) · Models: gpt-5.2, gpt-image-1.5, gemini-2.5-flash, gemini-3-pro-image-preview, DeepSeek-V3-0324 (Atlas Cloud) · port 7860 · [Repo](https://github.com/llmsresearch/paperbanana) · [▶️ Demo ↗](https://huggingface.co/spaces/llmsresearch/paperbanana) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llmsresearch-paperbanana/)</sub>

<a name="video2x"></a>
### #&#8288;65 [video2x](https://github.com/k4yt3x/video2x) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: widely used (85) · Freshness: quiet (29) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · AGPL-3.0 · Mar 2026</sub>

**Video upscaler and frame interpolator using Real-ESRGAN, Real-CUGAN, RIFE and Anime4K.**

Video2X is a C/C++ tool that upscales video and interpolates frames using Anime4K v4, Real-ESRGAN, Real-CUGAN and RIFE, running through ncnn and Vulkan. It ships a Qt6 GUI and installer for Windows, plus AUR packages and an AppImage for Linux. The README states it needs no extra disk space during processing beyond the final output.

- **+** Runs on any Vulkan GPU from NVIDIA, AMD or Intel, not just CUDA cards
- **+** Supports upscaling and frame interpolation, plus custom MPV-compatible GLSL shaders
- **+** Windows GUI installer, Linux AppImage and AUR packages, and a container image
- **+** Temporary files are not written during processing, per the README
- **−** Precompiled binaries require a CPU with AVX2 support
- **−** Last tagged release is 2025-01-24, older than recent commits
- **−** AGPL-3.0 license may constrain use in hosted services
- **−** Bundled demo videos are marked outdated in the README

<sub>GPU required · Needs Vulkan, FFmpeg, ncnn · Models: Real-ESRGAN, Real-CUGAN, RIFE, Anime4K v4, MPV GLSL shaders · [Repo](https://github.com/k4yt3x/video2x) · [▶️ Demo ↗](https://colab.research.google.com/drive/1gWEwcA9y57EsxwOjmLNmNMXPsafw0kGo) · [📖 Docs ↗](https://docs.video2x.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/video2x/)</sub>

<a name="open-higgsfield"></a>
### #&#8288;66 [open-higgsfield](https://github.com/wide-trace/open-higgsfield) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (41) · Freshness: active (100) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 5.8k · no license · Sep 2026</sub>

**Next.js studio for generating images and video with 38 hosted models.**

A Next.js 16 web studio with one prompt bar that drives 8 image and 30 video models (Soul, Seedance, Kling, Wan, Flux and others) through a remote generation API. Server actions call that API with your own platform key, and results go into a gallery with reuse, favorites, bulk download and undo. History is kept in browser IndexedDB, and uploads go to Vercel Blob.

- **+** Catalog-driven: a new model entry brings its own settings and media roles without studio changes
- **+** Gallery reuse restores model, settings and prompt, so runs can be re-rendered
- **+** Batch up to 4 results per press, with polling every 4s and a 10-minute deadline
- **+** Hosted version available, so no install is needed to try it
- **−** No local inference: every generation goes to an external API and needs a platform key
- **−** Needs a Vercel Blob token for uploads and a generation API origin to self-host
- **−** No license file detected, so reuse terms are unclear
- **−** History is stored only in one browser, capped at 60 records, and old result URLs can expire

<sub>no GPU · Needs Generation API (HF_API_BASE_URL) and platform key, Vercel Blob, Node.js and pnpm · Models: Soul 2, Seedance, Kling 3, Wan, Flux · port 3000 · [Repo](https://github.com/wide-trace/open-higgsfield) · [▶️ Demo ↗](https://openhiggsfield.ai) · [🌐 Site ↗](https://openhiggsfield.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-higgsfield/)</sub>

<a name="autofigure-edit"></a>
### #&#8288;67 [autofigure-edit](https://github.com/researai/autofigure-edit) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (28) · Freshness: active (93) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · MIT · Jul 2026</sub>

**Turns paper method text into editable SVG figures with a browser editor.**

AutoFigure-Edit generates a raster draft figure from method-section text with an image model. It then segments icons with SAM3, removes backgrounds with RMBG-2.0, and has an LLM write a placeholder SVG that is filled with the cropped icons. The result opens in an embedded SVG-Edit canvas, and an existing stage-1 figure can be imported to skip generation.

- **+** Outputs editable SVG with separate text, shapes and icon crops, not a flat raster
- **+** SAM3 can run through Roboflow or fal.ai, so no local GPU install is needed
- **+** Supports OpenRouter, Gemini, OpenAI Responses and any OpenAI-compatible /v1 endpoint
- **+** Accepts a reference image for style transfer and an existing figure to skip step 1
- **−** Requires paid LLM API keys plus a Hugging Face token with access to RMBG-2.0
- **−** Local SAM3 is not vendored and targets Python 3.12+, PyTorch 2.7+, CUDA 12.6
- **−** Icons are cropped raster images, so only layout and text are fully vector
- **−** Quality depends on the chosen image and SVG models; no offline model path is documented

<sub>GPU optional · Docker + Compose · Needs Hugging Face token (briaai/RMBG-2.0), LLM provider API key (OpenRouter, Gemini, OpenAI, Bianxie or custom), SAM3 locally, or Roboflow / fal.ai API, Docker Compose (optional) · Models: OpenRouter, Google Gemini, OpenAI Responses (gpt-5.5, gpt-image-2), OpenAI-compatible custom endpoints, SAM3 · port 8000 · [Repo](https://github.com/researai/autofigure-edit) · [▶️ Demo ↗](https://deepscientist.cc) · [🌐 Site ↗](https://deepscientist.cc) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autofigure-edit/)</sub>

<a name="generative-models"></a>
### #&#8288;68 [generative-models](https://github.com/stability-ai/generative-models) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: widely used (87) · Freshness: quiet (8) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · MIT · Dec 2025</sub>

**Stability AI reference code for SDXL, Stable Video Diffusion, SV3D and SV4D.**

Config-driven PyTorch codebase (the `sgm` package) from Stability AI for sampling and training diffusion models: SDXL 0.9/1.0, SDXL-Turbo, Stable Video Diffusion, SV3D and SV4D 2.0. It ships Streamlit and Gradio demos plus standalone sampling scripts, with PyTorch Lightning training configs. Weights are downloaded separately from Hugging Face into `checkpoints/`.

- **+** Covers text-to-image, image-to-video, multi-view (SV3D) and video-to-4D (SV4D 2.0) in one repo
- **+** Config-driven modules via YAML and instantiate_from_config, with example training configs
- **+** Streamlit and Gradio demos plus simple CLI sampling scripts
- **+** Low-VRAM flags such as --encoding_t, --decoding_t and --img_size for video models
- **−** Last release was 2023-07-27; newer models are announced only in the README
- **−** Weights not bundled; several have research-only or RAIL++-M licenses separate from the MIT code
- **−** Tested on Python 3.10 only; package does not declare dependencies
- **−** Manual install of PyTorch, requirements and sdata; no Docker image

<sub>GPU required · Needs PyTorch 2.0, PyTorch Lightning, Streamlit, Hugging Face model weights, Stability-AI/datapipelines (sdata), rembg (optional) · Models: SDXL-base-1.0, SDXL-refiner-1.0, SDXL-Turbo, Stable Video Diffusion (SVD, SVD-XT), SV3D_u · [Repo](https://github.com/stability-ai/generative-models) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/generative-models/)</sub>

<a name="fluxgym"></a>
### #&#8288;69 [FluxGym](https://github.com/cocktailpeanut/fluxgym) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (14) · Freshness: active (93) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Jul 2026</sub>

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

<sub>GPU required · Docker + Compose · Needs kohya-ss/sd-scripts (sd3 branch) · Models: Flux1-dev, Flux1-dev2pro, Flux1-schnell, custom bases via models.yaml · port 7860 · [Repo](https://github.com/cocktailpeanut/fluxgym) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fluxgym/)</sub>

<a name="sd-ppp"></a>
### #&#8288;70 [sd-ppp](https://github.com/zombieyang/sd-ppp) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (7) · Freshness: active (91) · Maintenance: weak (9) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · BSD-3-Clause · Nov 2026</sub>

**Photoshop plugin that sends layers to ComfyUI or cloud image APIs.**

SD-PPP is an unofficial Adobe Photoshop plugin that sends selections, layers or documents to an image-generation backend and returns the results into Photoshop. The 2.0 Beta works with ComfyUI without custom nodes, and with models and apps from replicate.com and runninghub.ai. It requires Photoshop 2025 (PS 26.0) or newer.

- **+** Runs inside Photoshop, so results come back to layers and documents
- **+** 2.0 Beta needs no custom nodes when using ComfyUI
- **+** Reaches hosted models via Replicate and RunningHUB, including Nano-banana and Flux-Kontext
- **+** Keyboard shortcuts and quick selection of areas, layers or documents
- **−** 2.0 Beta requires Photoshop 26.0 (2025) or newer
- **−** Requires an Adobe Photoshop installation
- **−** Source code lives in a separate monorepo; this repo has only the README and assets
- **−** README says GPL-3.0 but detected license is BSD-3-Clause

<sub>Needs Adobe Photoshop 2025 (26.0+), ComfyUI, Replicate or RunningHUB backend · Models: ComfyUI workflows, Replicate models, RunningHUB AI apps, Nano-banana, Flux-Kontext-Pro/Max · [Repo](https://github.com/zombieyang/sd-ppp) · [🌐 Site ↗](https://sdppp.zombee.tech/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sd-ppp/)</sub>

<a name="open-sora-plan"></a>
### #&#8288;71 [open-sora-plan](https://github.com/pku-yuangroup/open-sora-plan) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: popular (68) · Freshness: slowing (30) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Mar 2026</sub>

**Open text-to-video diffusion models and training code, reproducing Sora.**

Open-Sora Plan releases text-to-video and image-to-video diffusion transformer checkpoints (v1.0.0 to v1.5.0) along with the WF-VAE video autoencoder and a prompt refiner. Version 1.5.0 uses an 8B sparse DiT (SUV) and an 8x8x8 WF-VAE, and is trained and run on Ascend 910 NPUs via the MindSpeed-MM branch. The GPU version is listed as coming soon.

- **+** Weights published for every version v1.0.0 through v1.5.0 on Hugging Face
- **+** v1.3.0 supports 93x480p generation within 24G VRAM
- **+** WF-VAE with 8x8x8 downsampling; README claims higher PSNR than the Wan2.1 VAE
- **+** Includes image-to-video checkpoints, a prompt refiner, and technical reports per version
- **−** v1.5.0 weights only work with NPU plus MindSpeed-MM; GPU instructions say coming soon
- **−** Main branch has no runnable setup; code lives on the mindspeed_mmdit branch
- **−** No Docker, web UI or hosted demo; research-style checkpoints only
- **−** README license badge says Apache while detected license is MIT

<sub>GPU required · Needs Ascend 910 NPU (v1.5.0), MindSpeed-MM · Models: Text-to-video, Image-to-video, WF-VAE, SUV sparse DiT · [Repo](https://github.com/pku-yuangroup/open-sora-plan) · [📖 Docs ↗](https://github.com/PKU-YuanGroup/Open-Sora-Plan/blob/main/docs/Report-v1.5.0.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-sora-plan/)</sub>

<a name="jaaz"></a>
### #&#8288;72 [jaaz](https://github.com/11cafe/jaaz) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: known (47) · Freshness: slowing (34) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.7k · custom license · Mar 2026</sub>

**Infinite-canvas agent for generating images and video from prompts or sketches.**

Jaaz is a desktop app (Windows, macOS) with an infinite canvas and a chat agent that generates images and video. It calls cloud models such as GPT-4o, Midjourney, VEO3 and Kling, or local ones through ComfyUI and Ollama. The server is Python 3.12+ and the front end is React, so it can also be built manually on Linux.

- **+** Works with both cloud video/image APIs and local ComfyUI models
- **+** Sketch and arrow input on the canvas, so prompts are optional
- **+** Manual build path from source: React front end plus Python server
- **+** Prebuilt Windows and macOS releases on GitHub
- **−** License is not identified (NOASSERTION); commercial terms unclear, with a separate paid enterprise edition
- **−** README gives no RAM, VRAM or hardware requirements
- **−** No Docker image in the repo; Docker is only offered with the paid edition
- **−** Last release is 2025-08-09; manual install steps clone a different repo name (localart)

<sub>GPU optional · Needs Python >=3.12, Node.js/npm, ComfyUI (optional), Ollama (optional) · Models: GPT-4o, Midjourney, VEO3, Kling, Seedance · [Repo](https://github.com/11cafe/jaaz) · [📖 Docs ↗](https://mxnpt25l6k.feishu.cn/docx/LvcTdlVbFoRAZWxnhBYcqVydnpc) · [🌐 Site ↗](https://jaaz.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jaaz/)</sub>

<a name="skyreels-v2"></a>
### #&#8288;73 [skyreels-v2](https://github.com/skyworkai/skyreels-v2) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: popular (53) · Freshness: quiet (28) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · custom license · Jan 2026</sub>

**Open-weight video diffusion models for long text- and image-to-video generation.**

SkyReels V2 provides weights and Python inference scripts for autoregressive diffusion-forcing video models at 1.3B and 14B parameters, at 540P and 720P. It supports text-to-video, image-to-video, video extension and start/end frame control, with clips generated in chunks to reach 30 to 60 seconds. Models are on Hugging Face and ModelScope, and Diffusers pipelines are included.

- **+** Diffusion-forcing models extend length by chunking; README gives frame counts for 10s to 60s clips
- **+** Covers T2V, I2V, video extension and start/end frame control from one script
- **+** Diffusers pipelines provided alongside native scripts
- **+** Peak VRAM documented: about 14.7GB for 1.3B at 540P
- **−** 14B at 540P needs about 43 to 51GB peak VRAM, per the README
- **−** 5B checkpoints and Camera Director models are still listed as coming soon
- **−** Async mode needs frame counts divisible by causal_block_size, and is slower than sync
- **−** No web UI or API server; inference runs through command-line scripts

<sub>GPU required · Needs PyTorch, Hugging Face model weights, diffusers (optional) · Models: SkyReels-V2-DF 1.3B/14B, SkyReels-V2-T2V 14B, SkyReels-V2-I2V 1.3B/14B, SkyCaptioner-V1 · [Repo](https://github.com/skyworkai/skyreels-v2) · [▶️ Demo ↗](https://www.skyreels.ai/home?utm_campaign=github_SkyReels_V2) · [📖 Docs ↗](https://arxiv.org/pdf/2504.13074) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skyreels-v2/)</sub>

<a name="hunyuan3d-2"></a>
### #&#8288;74 [hunyuan3d-2](https://github.com/tencent-hunyuan/hunyuan3d-2) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: popular (75) · Freshness: quiet (0) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · Oct 2025</sub>

**Image-to-3D mesh and texture generation models from Tencent.**

Hunyuan3D 2.0 generates textured 3D assets in two stages: a flow-based diffusion transformer (Hunyuan3D-DiT) produces a mesh from an image, then Hunyuan3D-Paint creates a texture map. It ships a diffusers-style Python API, a Gradio app, an HTTP API server and a Blender addon, with multiview, mini and turbo variants of the shape model. Shape generation needs about 6 GB VRAM, and shape plus texture about 16 GB.

- **+** Two-stage pipeline lets Paint texture handcrafted meshes as well as generated ones
- **+** Variants cover multiview input, 0.6B mini, and turbo/fast distilled models
- **+** Several interfaces: Python API, Gradio app, HTTP API server, Blender addon
- **+** Shape-only generation runs in about 6 GB VRAM
- **−** Texture generation needs custom_rasterizer and differentiable_renderer built from source
- **−** Full shape plus texture generation needs about 16 GB VRAM
- **−** License is reported as NOASSERTION; terms must be checked in the repo
- **−** No Docker image or tagged release; TensorRT version still unchecked in the plan

<sub>GPU required · Needs PyTorch, Gradio, trimesh, Hugging Face model weights · Models: Hunyuan3D-DiT, Hunyuan3D-Paint, Hunyuan3D-2mini, Hunyuan3D-2mv, Hunyuan3D-Delight · port 8080 · [Repo](https://github.com/tencent-hunyuan/hunyuan3d-2) · [▶️ Demo ↗](https://huggingface.co/spaces/tencent/Hunyuan3D-2) · [📖 Docs ↗](https://3d-models.hunyuan.tencent.com/) · [🌐 Site ↗](https://3d.hunyuan.tencent.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hunyuan3d-2/)</sub>

<a name="hunyuanvideo-1-5"></a>
### #&#8288;75 [hunyuanvideo-1.5](https://github.com/tencent-hunyuan/hunyuanvideo-1.5) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: known (30) · Freshness: recent (54) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · custom license · Apr 2026</sub>

**8.3B text-to-video and image-to-video diffusion model with training code.**

HunyuanVideo-1.5 is Tencent's video generation model: an 8.3B-parameter DiT with a 3D causal VAE, producing text-to-video and image-to-video at 480p and 720p, with super-resolution models to 1080p. The repo includes generate.py inference (multi-GPU via torchrun), step- and CFG-distilled checkpoints, caching options, and a train.py with FSDP and LoRA support using the Muon optimizer.

- **+** Runs with as little as 14 GB GPU memory when model offloading is enabled
- **+** Distilled variants: 480p I2V step-distilled in 8 or 12 steps, plus CFG-distilled checkpoints
- **+** Includes training code (FSDP, context parallel) and LoRA tuning, not just inference
- **+** Integrates with ComfyUI, Diffusers and LightX2V
- **−** Requires an NVIDIA CUDA GPU on Linux; no CPU or Mac path described
- **−** Some checkpoints still marked coming soon, e.g. 720p T2V CFG-distill and sparse T2V
- **−** Prompt rewriting expects a separate vLLM endpoint serving a large Qwen3 model
- **−** Optional speedups need extra builds: Flash Attention, SageAttention, flex-block-attn, sgl-kernel

<sub>GPU required · Needs PyTorch, CUDA, Flash Attention, SageAttention, flex-block-attn, sgl-kernel, vLLM (optional, prompt rewrite) · Models: HunyuanVideo-1.5 480p/720p T2V, HunyuanVideo-1.5 480p/720p I2V, 720p and 1080p super-resolution, Diffusers · [Repo](https://github.com/tencent-hunyuan/hunyuanvideo-1.5) · [▶️ Demo ↗](https://hunyuan.tencent.com/video/zh?tabIndex=0) · [📖 Docs ↗](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5/blob/main/assets/HunyuanVideo_1_5_Prompt_Handbook_EN.md) · [🌐 Site ↗](https://hunyuan.tencent.com/video/zh?tabIndex=0) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hunyuanvideo-1-5/)</sub>

<a name="echomimic"></a>
### #&#8288;76 [echomimic](https://github.com/antgroup/echomimic) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: niche (27) · Freshness: recent (53) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Apr 2026</sub>

**Audio-driven talking-head video from a portrait, with editable landmarks.**

EchoMimic is the research code and checkpoints for an AAAI 2025 paper on animating a still portrait from audio, facial landmarks, or both. It is a diffusion pipeline built on Stable Diffusion components (sd-vae-ft-mse, sd-image-variations-diffusers) with Whisper tiny for audio features. Inference runs through Python scripts or a Gradio UI; weights are on Hugging Face and ModelScope.

- **+** Supports audio-only, landmark-only and audio plus selected-landmark driving modes
- **+** Accelerated pipelines cut 240 frames from about 7 minutes to about 50 seconds on a V100
- **+** Hosted Hugging Face and ModelScope demos plus a local Gradio UI (webgui.py)
- **+** Tested on 16 GB V100, 24 GB RTX 4090D and 80 GB A100 cards
- **−** Needs manual download of several checkpoints and a static ffmpeg build with FFMPEG_PATH set
- **−** Stated as academic research only; no Docker image or packaged installer
- **−** Portrait-only; semi-body animation is in the separate EchoMimicV2 repo
- **−** Better singing model and Chinese talking-head dataset are still listed as TBD

<sub>GPU required · Needs CUDA >= 11.7, ffmpeg 4.4 static build, git-lfs, conda · Models: EchoMimic checkpoints (denoising_unet, reference_unet, motion_module, face_locator), sd-vae-ft-mse, sd-image-variations-diffusers, Whisper tiny · port 3000 · [Repo](https://github.com/antgroup/echomimic) · [▶️ Demo ↗](https://huggingface.co/spaces/BadToBest/EchoMimic) · [🌐 Site ↗](https://antgroup.github.io/ai/echomimic/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/echomimic/)</sub>

<a name="waifu2x-ncnn-vulkan"></a>
### #&#8288;77 [waifu2x-ncnn-vulkan](https://github.com/nihui/waifu2x-ncnn-vulkan) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: niche (15) · Freshness: slowing (33) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · MIT · Feb 2026</sub>

**Command-line waifu2x image upscaler and denoiser using ncnn and Vulkan.**

Upscales and denoises anime-style images with the waifu2x models, running inference through ncnn on any Vulkan-capable GPU (Intel, AMD, NVIDIA, Apple Silicon). Ships as a portable Windows/Linux/macOS executable with models bundled, so no CUDA or Caffe install is needed. It takes jpg/png/webp files or directories and supports tiling, multi-GPU and TTA mode.

- **+** Portable binary with models included; no CUDA or Caffe runtime required
- **+** Runs on Intel, AMD, NVIDIA and Apple Silicon GPUs through Vulkan
- **+** README benchmarks show faster times than waifu2x-caffe-cui on images up to 2000x2000
- **+** Tile size and load:proc:save thread counts can be tuned to limit GPU memory
- **−** CLI only; no GUI or web interface
- **−** Slower than waifu2x-caffe-cui at 4000x4000 input in the README benchmarks
- **−** Scope is waifu2x models only; no other upscalers or video pipeline
- **−** Driver crashes are possible; README advises updating the GPU driver

<sub>GPU optional · Needs Vulkan driver, ncnn, libwebp, libjpeg-turbo, libpng · Models: waifu2x cunet, upconv_7_anime_style_art_rgb, jpg, png, webp · [Repo](https://github.com/nihui/waifu2x-ncnn-vulkan) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/waifu2x-ncnn-vulkan/)</sub>

<a name="cogvideo"></a>
### #&#8288;78 [cogvideo](https://github.com/zai-org/cogvideo) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: popular (72) · Freshness: quiet (0) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2025</sub>

**Open-weight text-to-video and image-to-video diffusion models with inference and LoRA code.**

CogVideoX is a family of open text-to-video and image-to-video transformer models (2B and 5B, plus 1.5 versions) from Zhipu AI/THUDM, with inference scripts for diffusers and SAT. The repo also includes LoRA fine-tuning code, a 3D causal VAE and prompt-optimization examples. Diffusers inference runs from about 4GB (2B) or 5GB (5B) VRAM with offloading enabled.

- **+** Low VRAM paths: 2B from 4GB, 5B from 5GB with diffusers offloading, INT8 via torchao
- **+** Covers text-to-video, image-to-video and video continuation; 1.5 adds 10-second clips
- **+** Includes inference, LoRA fine-tuning and DDIM inversion code in one repo
- **+** Two inference stacks: diffusers and SAT, with weights on HuggingFace and ModelScope
- **−** Prompts must be English and long; README recommends LLM rewriting, with a 224-226 token limit
- **−** Slow: CogVideoX1.5-5B takes about 1000 seconds for 5 seconds of video on one A100
- **−** Memory figures only tested on A100/H100; peak is about 3x without offloading
- **−** Last release was 2024-11-08; newer work is moving to the separate CogKit repo

<sub>GPU required · Needs PyTorch, diffusers, SwissArmyTransformer, torchao · Models: CogVideoX-2B, CogVideoX-5B, CogVideoX-5B-I2V, CogVideoX1.5-5B, CogVideoX1.5-5B-I2V · [Repo](https://github.com/zai-org/cogvideo) · [▶️ Demo ↗](https://huggingface.co/spaces/THUDM/CogVideoX-5B) · [📖 Docs ↗](https://zhipu-ai.feishu.cn/wiki/DHCjw1TrJiTyeukfc9RceoSRnCh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cogvideo/)</sub>

<a name="comfyui-to-python-extension"></a>
### #&#8288;79 [comfyui-to-python-extension](https://github.com/pydn/comfyui-to-python-extension) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: niche (9) · Freshness: recent (64) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Apr 2026</sub>

**Exports ComfyUI node workflows as standalone runnable Python scripts.**

A ComfyUI custom node that adds File -> Save As Script to the web UI, downloading the current workflow as a .py file. A CLI (python -m comfyui_to_python) also converts workflows saved in API-format JSON, with a configurable queue size. Generated scripts still need a working ComfyUI install and accept ComfyUI memory flags such as --lowvram and --cpu.

- **+** Adds Save As Script to the ComfyUI File menu, plus a CLI for API-format JSON
- **+** Generated scripts accept ComfyUI flags like --highvram, --lowvram, --cpu and --disable-smart-memory
- **+** Images saved by UI-exported scripts reopen in ComfyUI with the original workflow metadata
- **+** Cleans up models and cache after each run; optional unload via COMFYUI_TOPYTHON_UNLOAD_MODELS=1
- **−** Generated scripts need a full ComfyUI runtime, including torch, to run
- **−** Requires Python 3.12 or newer, installed into the interpreter that launches ComfyUI
- **−** Workflow inputs are not exposed as command-line arguments in the exported script
- **−** Scripts are single-shot runners with no prompt or result caching across repeated calls

<sub>GPU optional · Needs ComfyUI, Python 3.12+, uv, torch · [Repo](https://github.com/pydn/comfyui-to-python-extension) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/comfyui-to-python-extension/)</sub>

<a name="omnigen2"></a>
### #&#8288;80 [omnigen2](https://github.com/vectorspacelab/omnigen2) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: niche (24) · Freshness: slowing (46) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · Apache-2.0 · Mar 2026</sub>

**Multimodal model for image generation, editing and in-context composition.**

OmniGen2 is a multimodal generation model built on a Qwen-VL-2.5 foundation, with separate decoding pathways for text and images. The repo provides PyTorch inference scripts, Gradio demos (image-only and chat), fine-tuning code and the OmniContext benchmark. It covers visual understanding, text-to-image, instruction-guided editing and in-context generation from reference images.

- **+** One model covers understanding, text-to-image, editing and in-context generation
- **+** Model CPU offload cuts VRAM by about half; sequential offload goes under 3GB
- **+** TeaCache (~30% speedup) and TaylorSeer (up to 2X) for faster inference
- **+** Ships fine-tuning code, X2I2 training dataset and OmniContext benchmark
- **−** Needs about 17GB VRAM (RTX 3090 class) without offloading
- **−** Sometimes ignores instructions; README suggests generating several images and picking one
- **−** In-context generation can alter reference objects; README admits a gap versus GPT-4o
- **−** Output size defaults to 1024x1024; English prompts are recommended

<sub>GPU required · Needs PyTorch 2.6.0, Python 3.11, flash-attn (optional), Gradio · Models: OmniGen2 (Hugging Face), OmniGen2-EditScore7B LoRA, Qwen-VL-2.5 base · [Repo](https://github.com/vectorspacelab/omnigen2) · [▶️ Demo ↗](https://huggingface.co/spaces/OmniGen2/OmniGen2) · [🌐 Site ↗](https://vectorspacelab.github.io/OmniGen2) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/omnigen2/)</sub>

<a name="fast-stable-diffusion"></a>
### #&#8288;81 [fast-stable-diffusion](https://github.com/thelastben/fast-stable-diffusion) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: popular (54) · Freshness: quiet (6) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · MIT · Nov 2025</sub>

**Google Colab notebooks for running ComfyUI, AUTOMATIC1111 and DreamBooth.**

Three Jupyter notebooks that launch ComfyUI, AUTOMATIC1111 and a DreamBooth fine-tuning workflow on Google Colab. The README is only badges and links, so it gives no setup steps, model list or requirements. The author also advertises a paid Flux and SDXL trainer via X.

- **+** Separate Colab notebooks for ComfyUI, AUTOMATIC1111 and DreamBooth
- **+** MIT license
- **+** No local GPU needed, since the notebooks target Google Colab
- **−** README has no usage instructions, requirements or supported model list
- **−** Tied to Google Colab; no local or Docker setup documented
- **−** No releases; last commit 2025-11-29
- **−** Advanced Flux and SDXL trainers are sold separately, not in this repo

<sub>Needs Google Colab · Models: Stable Diffusion · [Repo](https://github.com/thelastben/fast-stable-diffusion) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fast-stable-diffusion/)</sub>

<a name="echomimic-v2"></a>
### #&#8288;82 [echomimic_v2](https://github.com/antgroup/echomimic_v2) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: known (31) · Freshness: slowing (37) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · Apache-2.0 · Feb 2026</sub>

**Audio-driven half-body human animation from a reference image and pose sequence.**

EchoMimicV2 generates talking half-body human videos from a reference image, an audio clip and a pose sequence. It is the CVPR 2025 research code from Ant Group, with pretrained English and Mandarin checkpoints on Hugging Face and ModelScope. It ships a Gradio app, inference scripts, an accelerated variant and the EMTD dataset processing scripts.

- **+** Accelerated inference script cuts 120 frames from ~7 min to ~50 s on an A100
- **+** Gradio UI (app.py, app_acc.py) plus a ComfyUI node contributed by the community
- **+** Pretrained checkpoints cover English and Mandarin audio, hosted on Hugging Face and ModelScope
- **+** Apache-2.0 code with a published paper and dataset processing scripts
- **−** Requires an NVIDIA GPU with CUDA >= 11.7; tested only on 16 GB to 80 GB cards
- **−** Setup is manual: conda, pinned torch 2.5.1, static ffmpeg and separate weight downloads
- **−** Stated as academic research only; no hosted demo, the online demos are still TBD
- **−** No Docker image and no tagged releases

<sub>GPU required · Needs CUDA >= 11.7, Python 3.10, PyTorch 2.5.1, xformers, ffmpeg-static 4.4, git-lfs, Whisper tiny audio processor, sd-vae-ft-mse · Models: EchoMimicV2 checkpoints (denoising_unet, reference_unet, motion_module, pose_encoder), sd-vae-ft-mse, Whisper tiny · [Repo](https://github.com/antgroup/echomimic_v2) · [📖 Docs ↗](https://github.com/antgroup/echomimic_v2/discussions/53) · [🌐 Site ↗](https://antgroup.github.io/ai/echomimic_v2/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/echomimic-v2/)</sub>

<a name="comfyui-mixlab-nodes"></a>
### #&#8288;83 [comfyui-mixlab-nodes](https://github.com/mixlabpro/comfyui-mixlab-nodes) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (4) · Freshness: recent (52) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Jun 2026</sub>

**ComfyUI custom node pack for prompts, layers, LLM calls and web-app export.**

A ComfyUI custom node collection that adds LLM nodes (OpenAI-compatible endpoints, Siliconflow, local servers), prompt tools, image layer compositing, background removal, TripoSR 3D, and speech nodes. Its AppInfo node turns a workflow into a web app with chosen input and output nodes. It also adds screen-share input and fal.ai video generation nodes (Kling, RunwayGen3, LumaDreamMachine).

- **+** AppInfo node publishes a workflow as a web app with selectable input and output nodes
- **+** LLM nodes accept any OpenAI-compatible URL, including local servers and Azure OpenAI
- **+** Includes rembg, TripoSR, LaMa inpainting and MiniCPM-V 2.6 int4 (about 7GB GPU memory)
- **+** MIT licensed; installs by cloning into custom_nodes and running pip requirements
- **−** Last tagged release is 2024-10-14, though commits continue
- **−** Requires a running ComfyUI install; not usable standalone
- **−** Several models must be downloaded manually into specific models/ subfolders
- **−** README mixes Chinese and English and has no structured docs; LaMa needs manual install

<sub>GPU optional · Needs ComfyUI, Python 3.11, PyTorch 2.3.1+cu121, fal.ai API (video nodes), Siliconflow API (optional) · Models: OpenAI-compatible LLM APIs, MiniCPM-V 2.6 int4, TripoSR, rembg models, LaMa · port 8189 · [Repo](https://github.com/mixlabpro/comfyui-mixlab-nodes) · [🌐 Site ↗](https://www.mixcomfy.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/comfyui-mixlab-nodes/)</sub>

<a name="stable-diffusion-videos"></a>
### #&#8288;84 [stable-diffusion-videos](https://github.com/nateraw/stable-diffusion-videos) <sub>score [17](../README.md#-how-we-rank "Score 17/100. Adoption: known (32) · Freshness: quiet (26) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · Apache-2.0 · Dec 2025</sub>

**Python library that morphs between Stable Diffusion prompts to make videos.**

Provides a StableDiffusionWalkPipeline that interpolates between prompt and seed pairs in latent space and renders the frames into a video. It can take an audio file so the interpolation rate follows the music, and includes an Interface class that launches a web UI. Installed with pip, with a Colab notebook and example scripts.

- **+** Audio-driven interpolation lets videos move to the beat of a supplied track
- **+** Short API: one walk() call takes prompts, seeds, fps and step counts
- **+** Installs with pip; Colab notebook available for trying it without local setup
- **+** Built-in Interface class launches a UI from an existing pipeline
- **−** README examples use Stable Diffusion v1-4 only; newer model families are not documented
- **−** Real-ESRGAN upsampling is commented out because of package issues
- **−** Apple M1 requires float32 on MPS, since float16 is unavailable
- **−** Documentation is limited to the README and an examples folder

<sub>GPU optional · Needs PyTorch · Models: Stable Diffusion v1-4 (CompVis) · [Repo](https://github.com/nateraw/stable-diffusion-videos) · [▶️ Demo ↗](https://colab.research.google.com/github/nateraw/stable-diffusion-videos/blob/main/stable_diffusion_videos.ipynb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/stable-diffusion-videos/)</sub>

<a name="videocrafter"></a>
### #&#8288;85 [videocrafter](https://github.com/ailab-cvc/videocrafter) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: known (36) · Freshness: quiet (15) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · custom license · Jan 2026</sub>

**Text-to-video and image-to-video diffusion models with inference scripts.**

VideoCrafter is a research toolbox of video diffusion models built on Stable Diffusion code. It provides VideoCrafter2 and VideoCrafter1 text-to-video checkpoints (320x512, 576x1024) and image-to-video checkpoints (320x512, 640x1024), with shell inference scripts and a local Gradio app. Use is restricted to personal, research and non-commercial purposes.

- **+** Ships both text-to-video and image-to-video checkpoints on Hugging Face
- **+** Includes a local Gradio app via python gradio_app.py
- **+** Tech reports on arXiv for VideoCrafter1 and VideoCrafter2
- **+** Plain scripts (run_text2video.sh, run_image2video.sh) for inference
- **−** Non-commercial research-only disclaimer; license is not a standard open-source one
- **−** Last release January 2024; newer I2V work moved to DynamiCrafter
- **−** VideoCrafter2 checkpoint is only 320x512
- **−** Manual checkpoint download and placement; Python 3.8.5 conda environment, no Docker

<sub>Needs conda, Hugging Face checkpoints · Models: VideoCrafter2 T2V 320x512, VideoCrafter1 T2V 576x1024, VideoCrafter1 T2V 320x512, VideoCrafter1 I2V 640x1024, VideoCrafter1 I2V 320x512 · [Repo](https://github.com/ailab-cvc/videocrafter) · [▶️ Demo ↗](https://huggingface.co/spaces/VideoCrafter/VideoCrafter) · [🌐 Site ↗](https://ailab-cvc.github.io/videocrafter2/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/videocrafter/)</sub>

<a name="comfyui-custom-scripts"></a>
### #&#8288;86 [comfyui-custom-scripts](https://github.com/pythongosssss/comfyui-custom-scripts) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: niche (14) · Freshness: slowing (33) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · MIT · Feb 2026</sub>

**ComfyUI extension pack adding UI helpers and utility nodes.**

A collection of front-end scripts and nodes for ComfyUI, installed by cloning into custom_nodes. It adds embedding and custom word autocomplete, auto-arranged graphs, LoRA and checkpoint loaders with preview images, math and string nodes, an image feed panel, and notification nodes. The author notes they are too busy to keep up with issues.

- **+** Install is a single git clone into custom_nodes; git pull updates it
- **+** Loader nodes show preview images and example prompts next to model files
- **+** Math Expression and String Function nodes support graph values and regex replace
- **+** Covers editor quality-of-life: autocomplete, auto-arrange, snap to grid, node finder
- **−** Author states limited time to maintain it; no tagged releases
- **−** Several features are labelled Testing or WIP, such as Repeater and Reroute Primitive
- **−** Only works inside ComfyUI; no standalone use
- **−** Touch support is described by the author as basic and imperfect

<sub>Needs ComfyUI · Models: Stable Diffusion checkpoints, LoRA, embeddings · [Repo](https://github.com/pythongosssss/comfyui-custom-scripts) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/comfyui-custom-scripts/)</sub>

<a name="yolov5-deepsort-inference"></a>
### #&#8288;87 [yolov5-deepsort-inference](https://github.com/sharpiless/yolov5-deepsort-inference) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: niche (3) · Freshness: slowing (48) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · GPL-3.0 · Mar 2026</sub>

**YOLOv5 detection plus DeepSort tracking for counting vehicles and pedestrians.**

Python project that runs YOLOv5 detection and DeepSort tracking on video to track people, cars and trucks. It wraps both in a `Detector` class whose `feedCap` call returns an annotated frame, and `demo.py` runs the example. Custom YOLOv5 weights can be placed in the `weights` folder. The README points to a newer YOLOv11 version as the latest.

- **+** Wrapped `Detector` class with a single `feedCap` call returns an annotated frame
- **+** Custom-trained YOLOv5 weights can be used by placing them in `weights/`
- **+** Includes DeepSort re-ID tracking, not only per-frame detection
- **+** Short setup: `pip install -r requirements.txt` then `python demo.py`
- **−** Detection filter is hardcoded to person, car and truck labels
- **−** Author points to a newer YOLOv11-DeepSort repository as the latest version
- **−** GPL-3.0 license limits use in closed-source products
- **−** README is in Chinese; no tests or benchmarks listed

<sub>GPU optional · Needs PyTorch, YOLOv5 (ultralytics), DeepSort · Models: YOLOv5 .pt weights (default yolov5m.pt) · [Repo](https://github.com/sharpiless/yolov5-deepsort-inference) · [📖 Docs ↗](https://blog.csdn.net/weixin_44936889/article/details/112002152) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yolov5-deepsort-inference/)</sub>

<a name="comfyui-examples"></a>
### #&#8288;88 [comfyui_examples](https://github.com/comfyanonymous/comfyui_examples) <sub>score [11](../README.md#-how-we-rank "Score 11/100. Adoption: known (32) · Freshness: quiet (5) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · custom license · Nov 2025</sub>

**Example workflows for ComfyUI covering image, video, 3D and audio models.**

A collection of example pages for ComfyUI, each with images that embed their workflow metadata. Loading an image with the Load button or dragging it onto the window restores the full node graph. Topics range from hires fix, inpainting, LoRA and ControlNet to SDXL, SD3, Flux, Qwen Image, Wan 2.1/2.2, Mochi and audio models.

- **+** Workflow is embedded in each image's metadata, so one drag reproduces the graph
- **+** Covers many model families: SDXL, SD3, Flux, Flux 2, Wan 2.2, HiDream, Cosmos
- **+** Includes classic techniques: inpainting, LoRA, ControlNet, area composition, model merging
- **−** Not runnable on its own; requires a separate ComfyUI install and downloaded model weights
- **−** Linked basic tutorial is marked early and unfinished
- **−** Node guide and documentation are labeled work in progress
- **−** Per-example explanations are brief and live in subfolders

<sub>Needs ComfyUI · Models: SD1.x, SDXL, SD3, Flux, Flux 2 · [Repo](https://github.com/comfyanonymous/comfyui_examples) · [📖 Docs ↗](https://docs.comfy.org/) · [🌐 Site ↗](https://comfyanonymous.github.io/ComfyUI_Blog/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/comfyui-examples/)</sub>

<a name="omnigen"></a>
### #&#8288;89 [omnigen](https://github.com/vectorspacelab/omnigen) <sub>score [10](../README.md#-how-we-rank "Score 10/100. Adoption: niche (27) · Freshness: quiet (8) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Dec 2025</sub>

**Single model for text-to-image, subject-driven generation and image editing.**

OmniGen is an image generation model that takes interleaved text and image prompts and handles text-to-image, subject-driven generation, identity-preserving generation and editing without ControlNet or IP-Adapter modules. The repo has a Python inference pipeline (OmniGenPipeline), a Gradio app, and a train.py script for LoRA or full fine-tuning. Weights are Shitao/OmniGen-v1 on Hugging Face; a successor, OmniGen2, lives in a separate repo.

- **+** One model covers text-to-image, editing and reference-image generation without extra plugins
- **+** Includes train.py for LoRA and full fine-tuning, with a toy dataset example
- **+** Usable through Hugging Face Diffusers, a local Gradio app, or Colab
- **+** MIT-licensed code with public weights and a Hugging Face demo
- **−** Superseded by OmniGen2, which has its own repository
- **−** No release tags; last commit was December 2025
- **−** Python library and notebooks only; no packaged server or Docker image
- **−** Multi-image prompts need manual image placeholders and can be slow

<sub>GPU required · Needs PyTorch, Hugging Face Hub weights, Gradio (optional demo), accelerate (training) · Models: Shitao/OmniGen-v1 · [Repo](https://github.com/vectorspacelab/omnigen) · [▶️ Demo ↗](https://huggingface.co/spaces/Shitao/OmniGen) · [📖 Docs ↗](https://huggingface.co/docs/diffusers/main/en/using-diffusers/omnigen) · [🌐 Site ↗](https://vectorspacelab.github.io/OmniGen/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/omnigen/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
