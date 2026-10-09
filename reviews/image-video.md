# 🎨 Image and video reviews · Best of Open-Source AI

Generation UIs and pipelines for images and video, usually around diffusion models. Back to the [leaderboard](../README.md#-image-and-video).

<a name="comfyui"></a>
### 🥇 [ComfyUI](https://github.com/comfy-org/comfyui) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: fair (77) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 137k · GPL-3.0 · Oct 2026</sub>

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

<sub>RAM ≥ 8 GB · GPU optional · Models: Stable Diffusion 1.5, SDXL, SD3.5, Flux.1 and Flux.2, Qwen Image and Qwen Image Edit, Wan 2.1/2.2, LTX-Video 2 · [Repo](https://github.com/comfy-org/comfyui) · [📖 Docs ↗](https://docs.comfy.org/) · [🌐 Site ↗](https://www.comfy.org/)</sub>

<a name="moneyprinterturbo"></a>
### 🥈 [MoneyPrinterTurbo](https://github.com/harry0703/moneyprinterturbo) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (95) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 129k · MIT · Oct 2026</sub>

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

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Needs LLM API (OpenAI-compatible) or Ollama, Stock footage API (Pexels, Pixabay, Coverr) or a video generation API · Models: OpenAI, Anthropic Claude, Google Gemini, DeepSeek, Qwen (DashScope) · [Repo](https://github.com/harry0703/moneyprinterturbo)</sub>

<a name="invokeai"></a>
### 🥉 [InvokeAI](https://github.com/invoke-ai/invokeai) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

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

<sub>Docker + Compose · Models: SD 1.5, SD 2.0, SDXL, SD 3.5 Medium/Large, CogView 4 · [Repo](https://github.com/invoke-ai/invokeai) · [📖 Docs ↗](https://invoke.ai/start-here/installation/) · [🌐 Site ↗](https://invoke.ai)</sub>

<a name="ai-toolkit"></a>
### #&#8288;4 [AI Toolkit](https://github.com/ostris/ai-toolkit) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (53) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Oct 2026</sub>

**Fine-tuning suite for image, video and audio diffusion models, with GUI and CLI.**

AI Toolkit trains LoRA and LoKr adapters for diffusion models, covering FLUX.1, FLUX.2, Qwen-Image, Wan 2.1/2.2, LTX-2 and SDXL, plus audio models like ACE-Step 1.5. Jobs are defined in YAML and run with `python run.py`, or started and monitored from a web UI on port 8675. The UI can be protected with an AI_TOOLKIT_AUTH token, and training can also run on Modal or RunPod.

- **+** Supports a wide range of image, edit, video and audio models in one tool
- **+** Same YAML configs work from the CLI or the web UI
- **+** Training resumes from the last checkpoint after interruption
- **+** Layer targeting via only_if_contains and ignore_if_contains, plus LoKr support
- **−** Manual install requires an Nvidia GPU; Mac support is experimental
- **−** Install manager is labeled experimental by the author
- **−** Dataset images must be jpg, jpeg or png; webp has known issues
- **−** Ctrl+C during a checkpoint save can corrupt that checkpoint

<sub>GPU required · Docker + Compose · Needs PyTorch, Node.js, Hugging Face · Models: FLUX.1, FLUX.2, Qwen-Image, Wan 2.1/2.2, LTX-2 · port 8675 · [Repo](https://github.com/ostris/ai-toolkit)</sub>

<a name="kohya-ss"></a>
### #&#8288;5 [Kohya's GUI](https://github.com/bmaltais/kohya_ss) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (42) · Freshness: active (100) · Maintenance: weak (9) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Jul 2026</sub>

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

<a name="pixelle-video"></a>
### #&#8288;6 [Pixelle-Video](https://github.com/ath-maas/pixelle-video) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (65) · Freshness: active (87) · Maintenance: weak (2) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Jun 2026</sub>

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

<sub>Docker + Compose · Needs uv, ffmpeg, ComfyUI or RunningHub (workflow-based generation), LLM API or Ollama · Models: OpenAI GPT, Qwen (DashScope), DeepSeek, Ollama, Flux via ComfyUI (default image_flux.json) · port 8501 · [Repo](https://github.com/ath-maas/pixelle-video) · [📖 Docs ↗](https://aidc-ai.github.io/Pixelle-Video/zh)</sub>

<a name="biniou"></a>
### #&#8288;7 [biniou](https://github.com/woolverine94/biniou) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: fair (67) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · GPL-3.0 · Oct 2026</sub>

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

<sub>RAM ≥ 8 GB · GPU optional · Docker · Needs ffmpeg, git, gcc, perl, openssl · Models: GGUF LLMs via llama.cpp, LLaVA GGUF, Whisper, NLLB-200, SD 1.5/2.1/Turbo · [Repo](https://github.com/woolverine94/biniou) · [📖 Docs ↗](https://github.com/Woolverine94/biniou/wiki)</sub>

<a name="fluxgym"></a>
### #&#8288;8 [FluxGym](https://github.com/cocktailpeanut/fluxgym) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: weak (21) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Jul 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
