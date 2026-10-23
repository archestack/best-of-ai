# 🎨 Image and video reviews · Best of Open-Source AI

Generation UIs and pipelines for images and video, usually around diffusion models. Back to the [leaderboard](../README.md#-image-and-video).

<sub>🌐 Also on the web: [Image and video on archestack.com](https://archestack.com/best-of-ai/image-video/), each project on its own page.</sub>

<a name="moneyprinterturbo"></a>
### 🥇 [MoneyPrinterTurbo](https://github.com/harry0703/moneyprinterturbo) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 134k · MIT · Oct 2026</sub>

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
### 🥈 [ComfyUI](https://github.com/comfy-org/comfyui) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 142k · GPL-3.0 · Oct 2026</sub>

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

<a name="invokeai"></a>
### 🥉 [InvokeAI](https://github.com/invoke-ai/invokeai) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

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

<a name="toonflow-app"></a>
### #&#8288;4 [toonflow-app](https://github.com/hbai-ltd/toonflow-app) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

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

<a name="open-generative-ai"></a>
### #&#8288;5 [open-generative-ai](https://github.com/anil-matcha/open-generative-ai) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

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

<a name="stable-diffusion-cpp"></a>
### #&#8288;6 [stable-diffusion.cpp](https://github.com/leejet/stable-diffusion.cpp) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · MIT · Oct 2026</sub>

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
### #&#8288;7 [infinite-canvas](https://github.com/basketikun/infinite-canvas) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · MIT · Oct 2026</sub>

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

<a name="ltx-2"></a>
### #&#8288;8 [ltx-2](https://github.com/lightricks/ltx-2) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.8k · custom license · Oct 2026</sub>

**Text and image to video model with synchronized audio, plus pipelines and trainer.**

LTX-2 is a 22B-parameter DiT model from Lightricks that generates video with synchronized audio from text, images or input audio. The repo is a Python monorepo with ltx-core, ltx-pipelines (distilled, DFR, two-stage, retake, IC-LoRA, HDR, dubbing) and ltx-trainer for LoRA and full fine-tuning. Weights are downloaded separately from Hugging Face, about 66 GiB for the quick-start set.

- **+** Generates audio and video together in one model, including speech
- **+** Many pipelines: distilled, DFR, keyframe, audio-to-video, retake, HDR/EXR, dubbing
- **+** Includes a trainer for LoRA, full fine-tuning and IC-LoRA
- **+** FP8 quantization and CPU or disk offload flags for limited GPU memory
- **−** Quick-start weights are about 66 GiB and gated behind Hugging Face terms
- **−** Exact VRAM requirements are not stated in the README
- **−** License is not identified by tooling (NOASSERTION); check the repo terms
- **−** Fastest VAE backend (natten) is Linux and CUDA only; CLI-driven, no built-in UI

<sub>GPU required · Needs uv, Hugging Face CLI, PyTorch, CUDA · Models: LTX-2.5 22B distilled, LTX-2.5 22B dev, LTX-2.3, Gemma 4 12B text encoder, safetensors · [Repo](https://github.com/lightricks/ltx-2) · [▶️ Demo ↗](https://console.ltx.video/playground) · [🌐 Site ↗](https://ltx.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ltx-2/)</sub>

<a name="modly"></a>
### #&#8288;9 [modly](https://github.com/lightningpixel/modly) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · custom license · Oct 2026</sub>

**Desktop app that generates 3D meshes from photos using local models.**

Modly is an Electron and TypeScript desktop app with a Python FastAPI backend that turns an image into a 3D mesh using open models on your own GPU. Models such as Hunyuan3D 2 Mini, TripoSG and Trellis2 GGUF are installed as extensions from GitHub repositories. It has a node-based workflow editor, in-app mesh smoothing and decimation, and a CLI for scripts and agents.

- **+** Model extensions install from a GitHub URL; official ones cover Hunyuan3D 2 Mini, TripoSG, Trellis2 GGUF
- **+** Runs on Windows, Linux and Apple Silicon macOS; AMD GPUs supported via ROCm
- **+** Node-based workflows are validated before run; meshes can be smoothed and decimated in-app
- **+** Stdlib-only CLI exposes generate, workflow-run and model commands for scripts and agents
- **−** Focused on image-to-3D; no general image or video generation described
- **−** Hugging Face is the only supported model weight provider
- **−** RAM and VRAM requirements are not stated in the README
- **−** Detected license is NOASSERTION; README says MIT with a required attribution credit for forks

<sub>GPU required · Needs Node.js, Python, Hugging Face (model weights) · Models: Hunyuan3D 2 Mini, Hunyuan3D 2 Mini Turbo, Hunyuan3D 2 Mini Fast, TripoSG, Trellis2 GGUF · [Repo](https://github.com/lightningpixel/modly) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/modly/)</sub>

<a name="faceswap"></a>
### #&#8288;10 [faceswap](https://github.com/deepfakes/faceswap) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: widely used (91) · Freshness: active (90) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · GPL-3.0 · Aug 2026</sub>

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

<a name="ai-toolkit"></a>
### #&#8288;11 [AI Toolkit](https://github.com/ostris/ai-toolkit) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Oct 2026</sub>

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

<a name="diffsynth-studio"></a>
### #&#8288;12 [diffsynth-studio](https://github.com/modelscope/diffsynth-studio) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (47) · Freshness: active (87) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

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

<a name="sdnext"></a>
### #&#8288;13 [sdnext](https://github.com/vladmandic/sdnext) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Oct 2026</sub>

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

<a name="wan2-2"></a>
### #&#8288;14 [wan2.2](https://github.com/wan-video/wan2.2) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: weak (14) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Sep 2026</sub>

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

<a name="biniou"></a>
### #&#8288;15 [biniou](https://github.com/woolverine94/biniou) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · GPL-3.0 · Oct 2026</sub>

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

<a name="pixelle-video"></a>
### #&#8288;16 [Pixelle-Video](https://github.com/ath-maas/pixelle-video) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (75) · Freshness: active (82) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Jun 2026</sub>

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
### #&#8288;17 [vimax](https://github.com/hkuds/vimax) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (42) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Sep 2026</sub>

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

<a name="open-sora"></a>
### #&#8288;18 [open-sora](https://github.com/hpcaitech/open-sora) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (78) · Freshness: slowing (43) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Apr 2026</sub>

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

<a name="hunyuanvideo"></a>
### #&#8288;19 [hunyuanvideo](https://github.com/tencent-hunyuan/hunyuanvideo) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: known (40) · Freshness: active (100) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · custom license · Oct 2026</sub>

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

<a name="upscayl"></a>
### #&#8288;20 [upscayl](https://github.com/upscayl/upscayl) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: widely used (89) · Freshness: slowing (39) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · AGPL-3.0 · Mar 2026</sub>

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

<a name="kohya-ss"></a>
### #&#8288;21 [Kohya's GUI](https://github.com/bmaltais/kohya_ss) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (38) · Freshness: active (96) · Maintenance: weak (2) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Jul 2026</sub>

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

<a name="liveportrait"></a>
### #&#8288;22 [liveportrait](https://github.com/klingairesearch/liveportrait) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (60) · Freshness: active (80) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · custom license · Jun 2026</sub>

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

<a name="hivisionidphotos"></a>
### #&#8288;23 [hivisionidphotos](https://github.com/zeyi-lin/hivisionidphotos) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (63) · Freshness: recent (64) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Jul 2026</sub>

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
### #&#8288;24 [FluxGym](https://github.com/cocktailpeanut/fluxgym) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Jul 2026</sub>

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

<a name="video2x"></a>
### #&#8288;25 [video2x](https://github.com/k4yt3x/video2x) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: popular (66) · Freshness: slowing (34) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · AGPL-3.0 · Mar 2026</sub>

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

<a name="generative-models"></a>
### #&#8288;26 [generative-models](https://github.com/stability-ai/generative-models) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: popular (71) · Freshness: quiet (14) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · MIT · Dec 2025</sub>

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

<a name="ltx-video"></a>
### #&#8288;27 [ltx-video](https://github.com/lightricks/ltx-video) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: niche (30) · Freshness: quiet (27) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Jan 2026</sub>

**Reference code and weights for the LTX-Video DiT text/image-to-video model.**

Official repository for LTX-Video, a diffusion-transformer video generation model in 2B and 13B sizes, with distilled and FP8 variants. It provides an inference.py script and Python API for text-to-video, image-to-video, keyframe conditioning and video extension, plus ComfyUI and Diffusers integrations. The README says active development has moved to LTX-2, which adds synchronized audio.

- **+** Multiple checkpoints: 13B dev, 13B and 2B distilled, plus FP8 quantized versions
- **+** Supports image-to-video, multi-keyframe conditioning, video extension and video-to-video
- **+** Depth, pose and canny IC-LoRA control models published on Hugging Face
- **+** Works through ComfyUI and Diffusers as well as its own inference script
- **−** README states LTX-2 is now the primary home for development
- **−** README says inference.py does not yet match ComfyUI output quality
- **−** No release tags; setup is a manual pip install in a venv
- **−** VRAM and RAM requirements are not stated in the README

<sub>GPU required · Needs PyTorch >= 2.1.2, CUDA 12.2 (tested), ComfyUI (optional), Diffusers (optional) · Models: ltxv-13b-0.9.8-dev, ltxv-13b-0.9.8-distilled, ltxv-2b-0.9.8-distilled, FP8 variants, ltxv-2b-0.9.6 · [Repo](https://github.com/lightricks/ltx-video) · [▶️ Demo ↗](https://app.ltx.studio/ltx-2-playground/t2v) · [📖 Docs ↗](https://docs.ltx.video) · [🌐 Site ↗](https://ltx.video) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ltx-video/)</sub>

<a name="open-sora-plan"></a>
### #&#8288;28 [open-sora-plan](https://github.com/pku-yuangroup/open-sora-plan) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: known (34) · Freshness: slowing (38) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Mar 2026</sub>

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

<a name="skyreels-v2"></a>
### #&#8288;29 [skyreels-v2](https://github.com/skyworkai/skyreels-v2) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (11) · Freshness: slowing (36) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · custom license · Jan 2026</sub>

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

<a name="cogvideo"></a>
### #&#8288;30 [cogvideo](https://github.com/zai-org/cogvideo) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: known (45) · Freshness: quiet (3) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2025</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
