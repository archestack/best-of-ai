# 🎨 Image and video reviews · Best of Open-Source AI

Generation UIs and pipelines for images and video, usually around diffusion models. Back to the [leaderboard](../README.md#-image-and-video).

<sub>🌐 Also on the web: [Image and video on archestack.com](https://archestack.com/best-of-ai/image-video/), each project on its own page.</sub>

<a name="moneyprinterturbo"></a>
### 🥇 [MoneyPrinterTurbo](https://github.com/harry0703/moneyprinterturbo) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 132k · MIT · Oct 2026</sub>

**Turns a topic into a short video with script, footage, voiceover and subtitles.**

MoneyPrinterTurbo takes a topic or keywords and produces a finished short video. An LLM writes the script, footage comes from Pexels, Pixabay, Coverr, local files or text-to-video APIs, and TTS, subtitles and background music are added before the final render. It offers a WebUI, HTTP API, CLI and an agent skill, and outputs 9:16, 16:9 or 1:1.

- **+** Covers the whole pipeline: script, footage, voiceover, subtitles, music and render
- **+** Many LLM providers, including OpenAI, Claude, Gemini, DeepSeek, and Ollama for local models
- **+** Edge TTS needs no API key; Pexels and Pixabay stock footage are free
- **+** WebUI, API, CLI and batch generation; Docker and compose files included
- **−** Most LLMs and stock sources need API keys; AI video generation uses paid services
- **−** Footage relevance depends on keyword matching against stock libraries
- **−** README is dominated by sponsor and promotional sections
- **−** Web port and Docker setup details are not visible in the provided README

<sub>RAM ≥ 4 GB · GPU optional · Docker + Compose · Needs Python 3.11+, LLM API key or Ollama, Pexels/Pixabay/Coverr API keys, Edge TTS or other TTS service · Models: OpenAI, Anthropic Claude, Google Gemini, DeepSeek, Qwen · [Repo](https://github.com/harry0703/moneyprinterturbo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moneyprinterturbo/)</sub>

<a name="comfyui"></a>
### 🥈 [ComfyUI](https://github.com/comfy-org/comfyui) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: fair (77) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 138k · GPL-3.0 · Oct 2026</sub>

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

<sub>RAM ≥ 8 GB · GPU optional · Models: Stable Diffusion 1.5, SDXL, SD3.5, Flux.1 and Flux.2, Qwen Image and Qwen Image Edit, Wan 2.1/2.2, LTX-Video 2 · [Repo](https://github.com/comfy-org/comfyui) · [📖 Docs ↗](https://docs.comfy.org/) · [🌐 Site ↗](https://www.comfy.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/comfyui/)</sub>

<a name="toonflow-app"></a>
### 🥉 [toonflow-app](https://github.com/hbai-ltd/toonflow-app) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

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
### #&#8288;4 [InvokeAI](https://github.com/invoke-ai/invokeai) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

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

<sub>Docker + Compose · Models: SD 1.5, SD 2.0, SDXL, SD 3.5 Medium/Large, CogView 4 · [Repo](https://github.com/invoke-ai/invokeai) · [📖 Docs ↗](https://invoke.ai/start-here/installation/) · [🌐 Site ↗](https://invoke.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/invokeai/)</sub>

<a name="open-generative-ai"></a>
### #&#8288;5 [open-generative-ai](https://github.com/anil-matcha/open-generative-ai) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: fair (58) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Oct 2026</sub>

**Image, video and lip-sync studio UI that calls MuAPI, with optional local engines.**

A JavaScript app, available as a web build and an Electron desktop app, that front-ends hosted image, video, audio and lip-sync models through the MuAPI service. The desktop app can also run local inference: a bundled stable-diffusion.cpp engine for SD 1.5, SDXL and Z-Image, or a user-installed Wan2GP for video models and Flux. Most generation depends on a MuAPI account, and the README promotes a paid white-label offering.

- **+** Desktop app can run sd.cpp locally with Metal, CUDA, Vulkan or ROCm, no API key
- **+** Wan2GP integration runs video models locally or on a remote GPU box via MCP
- **+** Multi-image input accepts up to 14 reference images on compatible edit models
- **+** Installers provided for macOS (arm64, x64), Windows and Linux (AppImage, .deb)
- **−** Cloud generation requires MuAPI; the 600+/200+ model claims run through that paid service
- **−** Local inference is desktop-only; the hosted web version always uses cloud APIs
- **−** Installers are unsigned, so macOS Gatekeeper and Windows SmartScreen need manual bypass
- **−** Z-Image needs about 16 GB RAM and is reported to hang 8 GB Macs

<sub>RAM ≥ 16 GB · GPU optional · Docker + Compose · Needs MuAPI account/API key, Wan2GP (optional, for local video), stable-diffusion.cpp (bundled), Node.js (for source builds) · Models: Flux, Nano Banana, Kling, Sora, Veo · [Repo](https://github.com/anil-matcha/open-generative-ai) · [▶️ Demo ↗](https://muapi.ai/open-generative-ai?utm_source=github&utm_medium=readme&utm_campaign=open-generative-ai) · [🌐 Site ↗](https://muapi.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-generative-ai/)</sub>

<a name="ai-toolkit"></a>
### #&#8288;6 [AI Toolkit](https://github.com/ostris/ai-toolkit) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: fair (52) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Oct 2026</sub>

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

<a name="biniou"></a>
### #&#8288;7 [biniou](https://github.com/woolverine94/biniou) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: fair (67) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · GPL-3.0 · Oct 2026</sub>

**Gradio web UI for local text, image, audio, video and 3D generation.**

biniou is a self-hosted Gradio web UI that bundles many generative modules: a llama-cpp chatbot for GGUF models, Whisper speech-to-text, Stable Diffusion and Flux image generation, MusicGen audio, video and Shap-E 3D. It runs on CPU from 8GB RAM, with optional CUDA or experimental ROCm, and can work offline once models are downloaded. Installers exist for several Linux distributions and Windows, plus a Dockerfile.

- **+** Covers text, image, audio, video and 3D generation in one UI
- **+** Runs on CPU only, from 8GB RAM; CUDA and experimental ROCm optional
- **+** One-click installers for several Linux distros and Windows; Dockerfile provided
- **+** Modules can pass outputs to each other; generation settings saved as metadata
- **−** AMD64 only; macOS support is experimental and untested
- **−** Many modules need 16GB+ RAM; about 200GB of disk with default models
- **−** Python 3.10 or 3.11 required; Windows install adds Visual Studio Build tools
- **−** Chatbot has no stated agents, tools or document chat; the README lists only chat and multimodal

<sub>RAM ≥ 8 GB · GPU optional · Docker · Needs Python 3.10/3.11, git, ffmpeg, openssl, Hugging Face model downloads · Models: GGUF (llama-cpp), Stable Diffusion 1.5/2.1/XL/3.5, Flux, LoRA, safetensors · [Repo](https://github.com/woolverine94/biniou) · [📖 Docs ↗](https://github.com/Woolverine94/biniou/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/biniou/)</sub>

<a name="faceswap"></a>
### #&#8288;8 [faceswap](https://github.com/deepfakes/faceswap) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: widely used (85) · Freshness: active (90) · Maintenance: weak (11) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · GPL-3.0 · Aug 2026</sub>

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

<a name="pixelle-video"></a>
### #&#8288;9 [Pixelle-Video](https://github.com/ath-maas/pixelle-video) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (61) · Freshness: active (85) · Maintenance: weak (3) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Jun 2026</sub>

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

<a name="vimax"></a>
### #&#8288;10 [vimax](https://github.com/hkuds/vimax) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: patchy (39) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Sep 2026</sub>

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

<a name="kohya-ss"></a>
### #&#8288;11 [Kohya's GUI](https://github.com/bmaltais/kohya_ss) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (18) · Freshness: active (98) · Maintenance: weak (6) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Jul 2026</sub>

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

<a name="hivisionidphotos"></a>
### #&#8288;12 [hivisionidphotos](https://github.com/zeyi-lin/hivisionidphotos) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (43) · Freshness: recent (66) · Maintenance: weak (0) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Jul 2026</sub>

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

<a name="fluxgym"></a>
### #&#8288;13 [FluxGym](https://github.com/cocktailpeanut/fluxgym) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: weak (19) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Jul 2026</sub>

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

<a name="upscayl"></a>
### #&#8288;14 [upscayl](https://github.com/upscayl/upscayl) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: widely used (80) · Freshness: slowing (41) · Maintenance: weak (22) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · AGPL-3.0 · Mar 2026</sub>

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

<a name="video2x"></a>
### #&#8288;15 [video2x](https://github.com/k4yt3x/video2x) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: known (48) · Freshness: slowing (36) · Maintenance: weak (2) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · AGPL-3.0 · Mar 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
