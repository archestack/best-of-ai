# 🧬 Open models reviews · Best of Open-Source AI

Repositories of open-weight models with the code to run them: LLMs, vision, speech and embedding models. Back to the [leaderboard](../README.md#-open-models).

<sub>🌐 Also on the web: [Open models on archestack.com](https://archestack.com/best-of-ai/models/), each project on its own page.</sub>

<a name="llmfit"></a>
### 🥇 [llmfit](https://github.com/alexsjones/llmfit) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Oct 2026</sub>

**Rust tool that checks which LLMs fit your RAM, CPU and GPU.**

llmfit detects CPU cores, RAM, GPU and VRAM (NVIDIA CUDA, AMD ROCm, Intel OneAPI, Apple Silicon), then scores a model catalog on fit, speed, quality and context across quantizations such as GGUF, AWQ, GPTQ and EXL2. It runs as a TUI, a CLI with JSON output, or an HTTP API and web dashboard via `llmfit serve`. Speed figures are estimates from a memory-bandwidth model, and `llmfit bench` can measure real tok/s against a running provider.

- **+** Detects NVIDIA, AMD, Intel and Apple Silicon hardware, including multi-GPU and unified memory
- **+** Handles MoE models, so memory estimates reflect active parameters rather than total size
- **+** JSON CLI output and REST endpoints (/api/v1/system, /api/v1/models) suit scripts and pipelines
- **+** Installs via Scoop, Homebrew, MacPorts, uv/pip, cargo or a multi-arch Docker image
- **−** Speed and fit numbers are estimates unless measured on your hardware or matched to community results
- **−** Does not serve models itself; it recommends and benchmarks against Ollama, llama.cpp, MLX and similar
- **−** Windows binaries may ship unsigned if the signing job fails
- **−** Model catalog is built in, so new models need a release or a custom-model entry

<sub>GPU optional · Docker · Needs Ollama, llama.cpp, MLX, Docker Model Runner or LM Studio (optional, for downloads and benchmarks) · Models: GGUF, AWQ, GPTQ, EXL2 · port 8787 · [Repo](https://github.com/alexsjones/llmfit) · [📖 Docs ↗](https://github.com/AlexsJones/llmfit/blob/main/docs/cli.md) · [🌐 Site ↗](https://llmfit.axjns.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llmfit/)</sub>

<a name="laya"></a>
### 🥈 [laya](https://github.com/nandhakishorm/laya) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Oct 2026</sub>

**Single-pass multilingual classifier for typed choice, score and yes/no decisions.**

Laya answers typed questions (choice, score, noul) about a text, email, ticket or JSON state in one forward pass of an encoder model, with no text generation. A Router picks between three checkpoints (ModernBERT-large English, mmBERT-base multilingual for 100+ languages, and a typed-decisions fine-tune). It ships as a Python package with a CLI, optional HTTP and MCP servers, and LangChain, LlamaIndex and CrewAI integrations.

- **+** One forward pass: 33 ms per question, 7.2 ms/question batched, measured on a T4
- **+** No generation, so no output parsing; answers are typed choice, score or probability
- **+** Router selects English or multilingual checkpoint per request; 100+ languages covered
- **+** Fine-tuning notebooks provided; typed-decisions checkpoint scores 0.766 vs 0.362 for base English
- **−** Zero-shot accuracy is low on domain tasks; fine-tuning is needed for good results
- **−** Multilingual checkpoint ships with a 1,024-token limit; beyond about 4,000 tokens accuracy varies
- **−** Only classifies fixed question types; cannot generate or explain text
- **−** Checkpoints download from Hugging Face on first use, so offline setups need preparation

<sub>GPU optional · Docker + Compose · Needs Hugging Face Hub (checkpoint download), PyTorch, transformers · Models: ModernBERT-large (421M), mmBERT-base (322M), ONNX Runtime · [Repo](https://github.com/nandhakishorm/laya) · [▶️ Demo ↗](https://huggingface.co/spaces/convaiinnovations/laya-demo) · [📖 Docs ↗](https://nandhakishorm.github.io/laya/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/laya/)</sub>

<a name="timesfm"></a>
### 🥉 [timesfm](https://github.com/google-research/timesfm) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Sep 2026</sub>

**Pretrained time-series foundation model for zero-shot forecasting from Google Research.**

TimesFM is a pretrained decoder-only model for time-series forecasting, installed as a Python package with PyTorch or MLX (Apple silicon) backends. Version 3.0 forecasts univariate and multivariate series with past-only and past-and-future covariates, returning point forecasts plus nine quantiles (0.1 to 0.9). The code is Apache-2.0, but 3.0 weights carry a non-commercial license.

- **+** Zero-shot forecasting of univariate and multivariate series with past-only and future covariates
- **+** Returns point forecast plus 9 quantiles (0.1 to 0.9) per step
- **+** MLX backend runs 3.0 on Apple silicon without PyTorch, numerically matched to PyTorch
- **+** Includes LoRA fine-tuning example (HF Transformers + PEFT), unit tests and an agent SKILL.md
- **−** TimesFM 3.0 weights are non-commercial and non-production; commercial use only via Google Cloud services
- **−** Not an officially supported Google product
- **−** Forecasting only; contexts beyond 15,360 points are truncated to the most recent
- **−** README code imports differ between 3.0 examples and the PyPI 2.0.2 note, which is unclear

<sub>GPU optional · Needs PyTorch or MLX, Hugging Face checkpoints · Models: TimesFM 3.0 (PyTorch checkpoint), TimesFM 2.5 (200M params, 16k context), TimesFM 1.0 and 2.0 (v1 archive) · [Repo](https://github.com/google-research/timesfm) · [🌐 Site ↗](https://research.google/blog/timesfm-3-a-zero-shot-foundation-model-for-multivariate-forecasting/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/timesfm/)</sub>

<a name="speech"></a>
### #&#8288;4 [speech](https://github.com/nvidia-nemo/speech) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (32) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Oct 2026</sub>

**PyTorch toolkit for training and deploying ASR, TTS and speech LLM models.**

NVIDIA NeMo Speech is a Python/PyTorch toolkit for building speech models: automatic speech recognition, text-to-speech and speech LLMs. It ships training code and pre-trained checkpoints such as Parakeet, Canary, Nemotron-Speech-Streaming and MagpieTTS, published on Hugging Face. Install from source with uv, from PyPI as nemo-toolkit, or use the NGC container.

- **+** Covers ASR, TTS and speech LLMs in one codebase with pre-trained open checkpoints
- **+** Streaming ASR checkpoint with 80ms-1s configurable latency and 40 languages
- **+** MagpieTTS v2607 supports 12 languages; Parakeet V3 and Canary V2 cover 25 European languages
- **+** Installs over an existing PyTorch 2.7+ build via pip without replacing it
- **−** NVIDIA GPU with CUDA required for training; only recommended for inference
- **−** Requires Python 3.12 or newer
- **−** Tested stack is pinned to PyTorch 2.11/2.12 with CUDA 12.9 or 13.2
- **−** Not an inference server; no HTTP API or web UI described in the README

<sub>GPU required · Docker · Needs PyTorch 2.7+, CUDA, Python 3.12+ · Models: Parakeet, Canary, Nemotron-Speech-Streaming, MagpieTTS, Canary-Qwen-2.5B · [Repo](https://github.com/nvidia-nemo/speech) · [▶️ Demo ↗](https://huggingface.co/spaces/nvidia/magpie_tts_multilingual_demo) · [📖 Docs ↗](https://docs.nvidia.com/nemo/speech/nightly/) · [🌐 Site ↗](https://huggingface.co/collections/nvidia/nemotron-speech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speech/)</sub>

<a name="insightface"></a>
### #&#8288;5 [insightface](https://github.com/deepinsight/insightface) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 30k · no license · Oct 2026</sub>

**Face detection, recognition and alignment toolbox with ArcFace and RetinaFace models.**

InsightFace is a 2D and 3D face analysis toolbox built on PyTorch and MXNet. It includes training code, datasets and pretrained models for recognition (ArcFace, PartialFC), detection (RetinaFace, SCRFD) and alignment, plus a Python package, a desktop GUI and a self-hosted server with REST API. Code is MIT, but training data and the models trained on it are non-commercial research only.

- **+** Covers recognition, detection and alignment with training code, datasets and IJB/Megaface evaluation scripts
- **+** Python package runs inference with automatic CoreML, CUDA or CPU provider selection
- **+** InsightFace Server offers a Web UI, REST API and SQLite storage in one Linux x86_64 container
- **+** PrivateFrame blurs or mosaics faces in local video and can redact selectively from reference photos
- **−** Models and training data are non-commercial research only; commercial use needs separate licensing
- **−** Inswapper and buffalo_l models require contacting the maintainers for a license
- **−** Repository mixes many research subprojects on PyTorch and MXNet, so setup differs per module
- **−** Server runs on Linux x86_64 only and needs operator-supplied, manifest-verified models

<sub>GPU optional · Needs PyTorch, MXNet, ONNX Runtime, SQLite · Models: ONNX, PyTorch, MXNet · [Repo](https://github.com/deepinsight/insightface) · [▶️ Demo ↗](http://demo.insightface.ai:7007/) · [📖 Docs ↗](https://github.com/deepinsight/insightface/blob/master/python-package/README.md) · [🌐 Site ↗](https://www.insightface.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/insightface/)</sub>

<a name="unlimited-ocr"></a>
### #&#8288;6 [unlimited-ocr](https://github.com/baidu/unlimited-ocr) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · MIT · Oct 2026</sub>

**OCR model that parses long documents and multi-page PDFs in one pass.**

Unlimited-OCR is a Baidu document-parsing vision-language model, building on DeepSeek-OCR, with weights on Hugging Face. The repo ships inference code for Transformers, vLLM and SGLang, the last exposing an OpenAI-compatible chat API. It handles single images and multi-page input, with PDFs converted to images first.

- **+** Multi-page parsing in one request, with 32768 max context length in the examples
- **+** Three inference paths: Transformers, vLLM (Docker images), and SGLang with OpenAI-compatible API
- **+** infer.py batch script launches SGLang and sends concurrent requests for image dirs or PDFs
- **+** MIT license; training supported through ms-swift
- **−** Requires an NVIDIA GPU; examples tested only on CUDA 12.9 with Python 3.12
- **−** PDFs must be rasterized to images with PyMuPDF before parsing
- **−** SGLang setup needs a bundled dev wheel and custom logit processor flags
- **−** VRAM requirement is not stated in the README

<sub>GPU required · Needs PyTorch 2.10.0, transformers 4.57.1, PyMuPDF, vLLM or SGLang (optional) · Models: baidu/Unlimited-OCR (safetensors) · port 10000 · [Repo](https://github.com/baidu/unlimited-ocr) · [▶️ Demo ↗](https://huggingface.co/spaces/baidu/Unlimited-OCR) · [📖 Docs ↗](https://recipes.vllm.ai/baidu/Unlimited-OCR) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unlimited-ocr/)</sub>

<a name="needle"></a>
### #&#8288;7 [needle](https://github.com/cactus-compute/needle) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

**8-29 MB on-device model for tool calling, extraction and embeddings.**

Needle is a small model from Cactus Compute that picks functions and fills their arguments from user text, extracts typed fields from messy text, and returns sentence embeddings. A grammar compiled from your schemas constrains decoding, and each response carries a confidence score. It ships with a C++ engine for many platforms, a Python package, and the Whistle speech-to-text model that runs on the same engine.

- **+** Whole model is an 8-29 MB file, with depths from 2 to 20 layers deployable
- **+** Grammar-constrained decoding guarantees output parses against your schemas
- **+** Returns empty call list for off-topic requests, plus a calibrated confidence score
- **+** Local LoRA fine-tuning or hosted full fine-tuning from the same package
- **−** Trades general chat capacity for tool calls and extraction; not a chat model
- **−** Full fine-tuning runs on Cactus GPUs and needs an API key
- **−** Binary telemetry is on by default; opt out via environment variables
- **−** JavaScript/WASM package is community-maintained, not first-party

<sub>no GPU · Needs Python (pip install cactus-needle), JAX (for local fine-tuning) · Models: Needle 3 (.cact), Needle 2, Whistle speech-to-text (.cact) · [Repo](https://github.com/cactus-compute/needle) · [▶️ Demo ↗](https://cactuscompute.com/needle) · [📖 Docs ↗](https://cactuscompute.com/blog/needle-python-docs) · [🌐 Site ↗](https://cactuscompute.com/needle) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/needle/)</sub>

<a name="minicpm-v"></a>
### #&#8288;8 [minicpm-v](https://github.com/openbmb/minicpm-v) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (59) · Freshness: recent (73) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · Apache-2.0 · Oct 2026</sub>

**Open-weight multimodal models for image, video, document and speech understanding.**

Repository for the MiniCPM-V 4.7 vision-language models (35B-A3B MoE and 1B) and MiniCPM-o 4.5, a 9B omnimodal model with full-duplex video, audio and speech output. It provides weights, inference and fine-tuning docs, and on-device deployment paths for iOS, Android and HarmonyOS. Code and weights are Apache-2.0.

- **+** Two size classes: 1B and 35B-A3B MoE for vision, plus a 9B omnimodal model
- **+** README reports 13+ tokens/s with 3 GB memory for 35B-A3B on iPhone 17 Pro Max
- **+** Covers iOS, Android, HarmonyOS and Intel, AMD, Arm, Rockchip and Houmo chips
- **+** Apache-2.0 for code and weights; fine-tuning via LLaMA-Factory and SWIFT, plus SRFT
- **−** No Docker or compose files; setup follows per-model docs
- **−** Last tagged release is 2025-05-27, while model updates are announced in the README
- **−** Benchmark claims are the authors' own, shown as images
- **−** Hardware requirements for desktop or server use are not stated in the README

<sub>RAM ≥ 3 GB · GPU optional · Needs Hugging Face Transformers, llama.cpp-omni, Ollama · Models: MiniCPM-V 4.7 35B-A3B, MiniCPM-V 4.7 1B, MiniCPM-o 4.5 9B, GGUF, BF16 · [Repo](https://github.com/openbmb/minicpm-v) · [▶️ Demo ↗](https://huggingface.co/spaces/openbmb/MiniCPM-V-4.7-Demo) · [📖 Docs ↗](https://minicpm-o.readthedocs.io/en/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/minicpm-v/)</sub>

<a name="ace-step-1-5"></a>
### #&#8288;9 [ace-step-1.5](https://github.com/ace-step/ace-step-1.5) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: patchy (49) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Aug 2026</sub>

**Text-to-music model with LM planner, DiT decoder, Gradio UI and REST API.**

ACE-Step 1.5 generates full songs from text prompts and lyrics using a Qwen3-based language model that plans the song and a diffusion transformer (2B or 4B XL) that renders audio. It also does cover generation, repainting, stem separation, vocal-to-accompaniment and LoRA training. It ships a Gradio UI on port 7860, a REST API on port 8001, a CLI and a Python API.

- **+** Runs locally with under 4GB VRAM using the DiT-only turbo model; README claims under 10s per song on RTX 3090
- **+** Covers text-to-music, cover, repaint, stem separation, and vocal-to-BGM in one model family
- **+** LoRA training from a few songs: 8 songs in about 1 hour on a 12GB 3090, from the Gradio UI
- **+** Several interfaces: Gradio UI, REST API, CLI, Python API, and a separate VST3 plugin
- **−** XL 4B models need at least 12GB VRAM with offload and quantization, 20GB for comfortable use
- **−** Low-VRAM setups (6GB or less) run without the LM, losing planning and query rewriting
- **−** Quality claims (between Suno v4.5 and v5) are the authors' own, with no numbers in the README
- **−** Python 3.11-3.12 only; CUDA recommended, other backends (MPS, ROCm, XPU, CPU) are secondary

<sub>GPU optional · Docker + Compose · Needs uv, Python 3.11-3.12, Gradio · Models: ACE-Step DiT 2B (base, sft, turbo), ACE-Step XL DiT 4B (base, sft, turbo), acestep-5Hz-lm 0.6B/1.7B/4B (Qwen3-based), LoRA adapters · port 7860 · [Repo](https://github.com/ace-step/ace-step-1.5) · [▶️ Demo ↗](https://huggingface.co/spaces/ACE-Step/Ace-Step-v1.5) · [📖 Docs ↗](https://github.com/ace-step/ACE-Step-1.5/blob/main/docs/en/INSTALL.md) · [🌐 Site ↗](https://ace-step.github.io/ace-step-v1.5.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ace-step-1-5/)</sub>

<a name="open-clip"></a>
### #&#8288;10 [open_clip](https://github.com/mlfoundations/open_clip) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (17) · Freshness: active (96) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · custom license · Sep 2026</sub>

**PyTorch library for training and running CLIP-style image-text models.**

OpenCLIP is an open implementation of OpenAI's CLIP. It loads many pretrained image-text models (LAION-2B, DataComp-1B, DFN, SigLIP, SigLIP2, PE-Core) and trains new ones with DDP or FSDP2. The main branch also adds NaFlex variable-resolution towers, CoCa, MaMMUT and CLAP audio-text training, with breaking changes from the 3.x releases.

- **+** Large zoo of pretrained checkpoints with ImageNet zero-shot results, up to 85.4% in the README table
- **+** Loads OpenAI, SigLIP, SigLIP2, DFN and PE-Core weights through one API
- **+** Training supports DDP, FSDP2, torch.compile strategies and SigLIP loss chunking
- **+** Model cards for the checkpoints are on the Hugging Face Hub
- **−** Main branch breaks the training API; older scripts need the v3 branch or a 3.x release
- **−** Horovod, torchscript and trace support were removed on main
- **−** Requires torch>=2.6
- **−** Many new model families on main are labelled experimental

<sub>GPU optional · Needs PyTorch >=2.6, timm, Hugging Face Hub · Models: CLIP, SigLIP, SigLIP2, CoCa, MaMMUT · [Repo](https://github.com/mlfoundations/open_clip) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-clip/)</sub>

<a name="kronos"></a>
### #&#8288;11 [kronos](https://github.com/shiyu-coder/kronos) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: widely used (88) · Freshness: recent (65) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Apr 2026</sub>

**Pretrained decoder-only models that forecast financial candlestick (K-line) series.**

Kronos is a family of decoder-only Transformers pretrained on OHLCV candlestick data from over 45 exchanges. A tokenizer quantizes K-lines into hierarchical discrete tokens, and the model forecasts future bars through a KronosPredictor class with temperature and top-p sampling. Weights for mini, small and base are on Hugging Face, and the repo includes a Qlib-based fine-tuning and backtest pipeline.

- **+** Open weights at 4.1M, 24.7M and 102.3M params on Hugging Face
- **+** Few-line predict and predict_batch API returning pandas DataFrames
- **+** Includes tokenizer and predictor fine-tuning scripts with a Qlib backtest example
- **+** MIT license; paper accepted at AAAI 2026
- **−** Kronos-large (499.2M) weights are not released
- **−** Context limited to 512 tokens, except 2048 for Kronos-mini
- **−** Batch prediction requires identical lookback and pred_len across all series
- **−** Fine-tuning example is a demo, not a production trading system; no releases tagged

<sub>GPU optional · Needs PyTorch, Hugging Face Hub, pyqlib (fine-tuning only), Comet.ml (optional) · Models: Kronos-mini, Kronos-small, Kronos-base, Hugging Face · [Repo](https://github.com/shiyu-coder/kronos) · [▶️ Demo ↗](https://shiyu-coder.github.io/Kronos-demo/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kronos/)</sub>

<a name="lingbot-map"></a>
### #&#8288;12 [lingbot-map](https://github.com/robbyant/lingbot-map) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

**Feed-forward streaming 3D reconstruction and camera pose model for video.**

LingBot-Map is a PyTorch model, the Geometric Context Transformer, that reconstructs 3D point clouds and camera poses from a video or image folder in a streaming fashion. It uses paged KV cache attention via FlashInfer, with an SDPA fallback, and the README reports about 20 FPS at 518×378 over sequences beyond 10,000 frames. It ships an interactive viser viewer, a windowed mode for long inputs, and an offline renderer that produces flythrough MP4s.

- **+** Streaming inference reported at ~20 FPS on 518×378 over sequences above 10,000 frames
- **+** Windowed mode and keyframe interval handle very long videos, e.g. a ~25,000-frame demo
- **+** Includes evaluation scripts for KITTI and Oxford Spires, plus an interactive viser viewer
- **+** Checkpoints on Hugging Face and ModelScope under Apache-2.0
- **−** Quality degrades when the KV cache holds more than 320 views, so long videos need tuning
- **−** Offline renderer needs Kaolin, ffmpeg and a manually built CUDA extension
- **−** Pinned to PyTorch 2.8.0 with CUDA 12.8 for prebuilt Kaolin wheels
- **−** No GPU memory figures stated; low-VRAM use points to a third-party fork

<sub>GPU required · Needs PyTorch 2.8.0 (CUDA 12.8), FlashInfer (recommended, SDPA fallback), viser, onnxruntime, NVIDIA Kaolin (offline renderer), ffmpeg (offline renderer), open3d (offline renderer) · Models: lingbot-map checkpoint (.pt), lingbot-map-stage1 checkpoint · port 8080 · [Repo](https://github.com/robbyant/lingbot-map) · [🌐 Site ↗](https://technology.robbyant.com/lingbot-map) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lingbot-map/)</sub>

<a name="omniparser"></a>
### #&#8288;13 [omniparser](https://github.com/microsoft/omniparser) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (56) · Freshness: active (82) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · CC-BY-4.0 · Jul 2026</sub>

**Screenshot parser that turns GUI screens into labeled elements for vision LLM agents.**

OmniParser detects interactable regions in UI screenshots with a YOLO-based detector and captions each icon with a Florence-based model. The structured output lets a vision LLM ground its actions on screen elements. The repo ships a demo notebook, a Gradio demo, and OmniTool, which drives a Windows 11 VM with OpenAI, DeepSeek, Qwen or Anthropic models.

- **+** Outputs structured, captioned UI elements that any vision-capable LLM can use for grounding
- **+** Model weights published on Hugging Face, with V1.5 and V2 checkpoints
- **+** Includes a Gradio demo and a hosted Hugging Face Space to try it
- **+** OmniTool supports OpenAI, DeepSeek, Qwen 2.5VL and Anthropic Computer Use
- **−** Weights must be fetched manually with huggingface-cli, including a PR revision for the newest detector
- **−** Mixed licensing: older Ultralytics-based detectors are AGPL, and the README badge says MIT
- **−** OmniTool documentation is marked work in progress
- **−** No Docker setup; requires a conda environment with Python 3.12

<sub>Needs conda, Python 3.12, Hugging Face model weights, Gradio · Models: YOLOv9-E icon detector, Florence icon captioner, OpenAI 4o/o1/o3-mini, DeepSeek R1, Qwen 2.5VL · [Repo](https://github.com/microsoft/omniparser) · [▶️ Demo ↗](https://huggingface.co/spaces/microsoft/OmniParser-v2) · [🌐 Site ↗](https://microsoft.github.io/OmniParser/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/omniparser/)</sub>

<a name="gpt-oss"></a>
### #&#8288;14 [gpt-oss](https://github.com/openai/gpt-oss) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (43) · Freshness: active (92) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Oct 2026</sub>

**OpenAI's open-weight gpt-oss-120b and 20b models with reference inference code.**

Repository for OpenAI's gpt-oss-120b (117B parameters, 5.1B active) and gpt-oss-20b (21B, 3.6B active) open-weight MoE models, with reference PyTorch, Triton and Metal inference code. It also includes browser and python tool implementations, a terminal chat client and an example Responses API server. Weights are downloaded from Hugging Face, and the models require the harmony response format.

- **+** Apache-2.0 license with weights on Hugging Face for both model sizes
- **+** MXFP4 MoE weights: 120b fits one 80GB GPU, 20b runs within 16GB memory
- **+** Configurable reasoning effort (low, medium, high) and full chain-of-thought output
- **+** Runs via Transformers, vLLM, Ollama and LM Studio, plus native function calling
- **−** Torch, Triton and Metal implementations are reference code, not for production
- **−** Models only work correctly with the harmony response format
- **−** Torch reference needs at least 4x H100; Linux reference code requires CUDA
- **−** Browser tool is educational and needs a You.com or Exa API key

<sub>RAM ≥ 16 GB · GPU optional · Needs Hugging Face Hub, openai-harmony, You.com or Exa API (browser tool) · Models: gpt-oss-120b, gpt-oss-20b, MXFP4, SafeTensors · [Repo](https://github.com/openai/gpt-oss) · [▶️ Demo ↗](https://gpt-oss.com) · [📖 Docs ↗](https://cookbook.openai.com/topic/gpt-oss) · [🌐 Site ↗](https://openai.com/open-models/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpt-oss/)</sub>

<a name="mamba"></a>
### #&#8288;15 [mamba](https://github.com/state-spaces/mamba) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (35) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Jul 2026</sub>

**Reference PyTorch code for Mamba, Mamba-2 and Mamba-3 state space models.**

Official implementation of the Mamba selective state space architecture, with Mamba, Mamba-2 and Mamba-3 blocks as PyTorch modules and CUDA kernels for the selective scan. It includes a sample language model backbone, generation and benchmark scripts, and pointers to pretrained 130M to 2.8B checkpoints on Hugging Face.

- **+** Official code from the authors for Mamba, Mamba-2 and Mamba-3 blocks
- **+** Pretrained checkpoints from 130M to 2.8B, auto-downloaded by the generation script
- **+** Includes lm-evaluation-harness commands to reproduce paper zero-shot results
- **+** Drop-in Mamba, Mamba2 and Mamba3 modules for your own PyTorch networks
- **−** Linux only; GPU use needs NVIDIA with CUDA 11.6+, AMD needs extra setup
- **−** Pretrained models are base models only, no instruction tuning
- **−** CUDA selective scan is opt-in and may compile locally with --no-build-isolation
- **−** Research code: no model server or chat interface included

<sub>GPU required · Needs PyTorch 1.12+, Python 3.10+, CUDA 11.6+, causal-conv1d (optional), lm-evaluation-harness (for evals) · Models: Mamba, Mamba-2, Mamba-3, Hugging Face checkpoints (state-spaces) · [Repo](https://github.com/state-spaces/mamba) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mamba/)</sub>

<a name="clip"></a>
### #&#8288;16 [clip](https://github.com/openai/clip) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (77) · Freshness: recent (59) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Mar 2026</sub>

**OpenAI's reference PyTorch code and weights for contrastive image-text embeddings.**

CLIP is a Python package that loads OpenAI's pretrained image-text models and exposes encode_image, encode_text and a similarity forward pass. It supports zero-shot image classification from natural-language labels and feature extraction for linear-probe training. The README targets PyTorch 1.7.1 or later on CUDA or CPU, with weights downloaded on demand.

- **+** Small API: clip.load, clip.tokenize, encode_image, encode_text
- **+** Zero-shot classification from text labels without task-specific training
- **+** MIT license; runs on CPU or CUDA GPU
- **+** README has runnable zero-shot and linear-probe examples on CIFAR-100
- **−** Inference and evaluation only; no training code in this repo
- **−** Installed from git via pip; no tagged releases
- **−** Text context length defaults to 77 tokens
- **−** Larger independently trained models are in OpenCLIP, not here

<sub>GPU optional · Needs PyTorch 1.7.1+, torchvision, ftfy, regex, tqdm · Models: CLIP ViT-B/32, other names via clip.available_models() · [Repo](https://github.com/openai/clip) · [▶️ Demo ↗](https://colab.research.google.com/github/openai/clip/blob/master/notebooks/Interacting_with_CLIP.ipynb) · [🌐 Site ↗](https://openai.com/blog/clip/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clip/)</sub>

<a name="unilm"></a>
### #&#8288;17 [unilm](https://github.com/microsoft/unilm) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (50) · Freshness: recent (70) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Sep 2026</sub>

**Microsoft research code and weights for pre-trained text, vision, speech and document AI.**

A monorepo of Microsoft Research projects on large-scale self-supervised pre-training across languages, vision, speech and multimodal tasks. Each subdirectory holds code and checkpoints for a separate model family, including UniLM, MiniLM, BEiT, LayoutLM, WavLM, TrOCR, VALL-E, Kosmos and E5. It is a research collection, not a single installable tool.

- **+** Covers text, vision, speech and document models in one repo, from UniLM to Kosmos-2.5
- **+** Document AI line (LayoutLM v1-v3, LayoutXLM, DiT, TrOCR) has pretrained models and code
- **+** MIT license
- **+** Some models have hosted demos, such as TextDiffuser-2 and DiT on Hugging Face Spaces
- **−** Not one library: each subfolder has its own setup, dependencies and README
- **−** Last tagged release is May 2024, and most listed model releases date from 2021-2023
- **−** Top-level README is a news and paper index with little install or usage guidance
- **−** Hardware requirements are not stated at the top level

<sub>Models: PyTorch, Hugging Face Transformers · [Repo](https://github.com/microsoft/unilm) · [▶️ Demo ↗](https://huggingface.co/spaces/JingyeChen22/TextDiffuser-2) · [🌐 Site ↗](https://aka.ms/GeneralAI) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unilm/)</sub>

<a name="spleeter"></a>
### #&#8288;18 [spleeter](https://github.com/deezer/spleeter) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (65) · Freshness: recent (63) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · MIT · Jun 2026</sub>

**Music source separation library with pretrained TensorFlow stem-splitting models.**

Spleeter is Deezer's Python library and CLI for splitting music into stems using pretrained TensorFlow models. It ships 2-stem (vocals/accompaniment), 4-stem (vocals/drums/bass/other) and 5-stem (adds piano) models, and can train new separation models given a dataset of isolated sources. It installs with pip or runs from a Docker image.

- **+** Pretrained 2, 4 and 5 stem models, usable from CLI or Python API
- **+** README claims 4-stem separation about 100x faster than real-time on a GPU
- **+** MIT-licensed; pip install, Docker image and Colab notebook provided
- **+** Includes training code for custom separation models given isolated-source data
- **−** Last release is 2.1.0 from 2021-09; that release made breaking CLI changes
- **−** Known issues on Apple M1 due to TensorFlow compatibility; workaround needed
- **−** Requires ffmpeg and libsndfile installed separately
- **−** Faster, more precise processing is offered only in the commercial Spleeter Pro

<sub>GPU optional · Docker · Needs ffmpeg, libsndfile, TensorFlow · Models: spleeter:2stems, spleeter:4stems, spleeter:5stems · [Repo](https://github.com/deezer/spleeter) · [▶️ Demo ↗](https://colab.research.google.com/github/deezer/spleeter/blob/master/spleeter.ipynb) · [📖 Docs ↗](https://github.com/deezer/spleeter/wiki/1.-Installation) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/spleeter/)</sub>

<a name="qwen"></a>
### #&#8288;19 [qwen](https://github.com/qwenlm/qwen) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (47) · Freshness: recent (51) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Mar 2026</sub>

**First-generation Qwen open-weight LLMs, 1.8B to 72B, with inference and finetuning code.**

Repository for the original Qwen base and chat models at 1.8B, 7B, 14B and 72B, with Int4 and Int8 quantized chat variants on Hugging Face and ModelScope. It includes Transformers inference examples, LoRA and Q-LoRA finetuning, vLLM and FastChat deployment, and a web demo. The repo is no longer actively maintained; development moved to QwenLM/Qwen2.

- **+** Four sizes (1.8B, 7B, 14B, 72B) with base, chat, Int4 and Int8 checkpoints
- **+** Context up to 32K on 1.8B, 7B and 72B; Q-LoRA finetune of 1.8B needs 5.8GB
- **+** Includes finetuning scripts: full-parameter, LoRA and Q-LoRA
- **+** Chat models support tool use, agent and code interpreter modes
- **−** No longer actively maintained; README points to QwenLM/Qwen2
- **−** Requires trust_remote_code=True to load models
- **−** Qwen-14B context is 8K; Qwen-72B Int4 generation needs 48.9GB GPU memory
- **−** No tagged releases; README says RLHF chat models not released yet

<sub>GPU optional · Docker · Needs PyTorch, Transformers, flash-attention (optional), vLLM (optional), FastChat (optional) · Models: Qwen-1.8B, Qwen-7B, Qwen-14B, Qwen-72B, Qwen-Chat · [Repo](https://github.com/qwenlm/qwen) · [▶️ Demo ↗](https://modelscope.cn/studios/qwen/Qwen-72B-Chat-Demo/summary) · [📖 Docs ↗](https://arxiv.org/abs/2309.16609) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwen/)</sub>

<a name="rwkv-lm"></a>
### #&#8288;20 [rwkv-lm](https://github.com/blinkdl/rwkv-lm) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (21) · Freshness: recent (70) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Sep 2026</sub>

**Reference code for training and running RWKV, an attention-free RNN language model.**

Reference implementation of RWKV-7 (and earlier v5/v6), an RNN-style language model that trains in parallel like a GPT and decodes with constant-size state and no KV cache. The repo has PyTorch and CUDA training scripts for MiniPile and Pile, demo inference in GPT and RNN modes, and fine-tuning notes such as state-tuning. Weights, GUIs and servers live in linked separate projects.

- **+** Constant-memory decoding with no KV cache; state is about 1.6M params at 24 layers, 1024 dim
- **+** Reference training code with CUDA kernels; default config needs one GPU with about 7 GB VRAM
- **+** Same model runs in parallel GPT mode or sequential RNN mode
- **+** Links to weights, GGUF builds, mobile runtime, Runner GUI and PEFT/RLHF forks
- **−** No packaged RWKV-7 layer; init, weight decay and per-parameter LR must be copied from train_temp
- **−** README says the FLA RWKV-7 implementation is not aligned with the reference and performs worse
- **−** Research-style repo: no Docker, no API server, last tagged release is from 2023-12
- **−** README is a long list of links; RWKV-5/6 and RWKV-7 instructions are mixed together

<sub>GPU required · Needs PyTorch 2.5+, CUDA 12.4+, DeepSpeed, pytorch-lightning 1.9.5, wandb, ninja · Models: RWKV-7, RWKV-6, RWKV-5, PyTorch .pth, GGUF (linked) · [Repo](https://github.com/blinkdl/rwkv-lm) · [▶️ Demo ↗](https://huggingface.co/spaces/BlinkDL/RWKV-Gradio-1) · [📖 Docs ↗](https://wiki.rwkv.com) · [🌐 Site ↗](https://rwkv.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rwkv-lm/)</sub>

<a name="deepresearch"></a>
### #&#8288;21 [deepresearch](https://github.com/alibaba-nlp/deepresearch) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: known (41) · Freshness: slowing (49) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Feb 2026</sub>

**Open 30B-A3B web research agent model with ReAct inference scripts.**

Tongyi DeepResearch is a 30.5B-parameter mixture-of-experts model (3.3B active per token, 128K context) trained for long-horizon web information seeking. The repo provides inference scripts that run it in ReAct or an IterResearch-based Heavy mode, plus benchmark evaluation scripts. Weights are on HuggingFace and ModelScope, and the model is also on OpenRouter.

- **+** Open weights on HuggingFace and ModelScope, 128K context, 3.3B parameters active per token
- **+** Two inference modes: ReAct and a test-time-scaling Heavy mode
- **+** Includes evaluation scripts for agentic benchmarks such as BrowseComp and HLE
- **+** Can be called through OpenRouter without a local GPU
- **−** Needs several external API keys: Serper, Jina, an OpenAI-compatible endpoint, DashScope
- **−** Python interpreter tool requires a separate SandboxFusion endpoint
- **−** Research scripts, not a packaged app; no Docker or web UI
- **−** OpenRouter use requires editing react_agent.py; README gives no hardware requirements

<sub>GPU optional · Needs Serper, Jina, OpenAI-compatible API, DashScope, SandboxFusion · Models: Tongyi-DeepResearch-30B-A3B, OpenRouter · [Repo](https://github.com/alibaba-nlp/deepresearch) · [▶️ Demo ↗](https://huggingface.co/spaces/Alibaba-NLP/Tongyi-DeepResearch) · [🌐 Site ↗](https://tongyi-agent.github.io/blog/introducing-tongyi-deep-research/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepresearch/)</sub>

<a name="chinese-llama-alpaca"></a>
### #&#8288;22 [chinese-llama-alpaca](https://github.com/ymcui/chinese-llama-alpaca) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: known (37) · Freshness: slowing (47) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Apr 2026</sub>

**Chinese-vocabulary LLaMA and Alpaca LoRA weights with pretraining and tuning scripts.**

Releases LoRA weights that extend LLaMA with a Chinese vocabulary (49,953 tokens) and add Chinese pretraining and instruction tuning, in 7B, 13B and 33B sizes. The LoRA files must be merged with the original LLaMA weights, which are not distributed. Includes merge, quantization, inference and training scripts. The authors recommend moving to their later Llama-3-based project.

- **+** Extended Chinese vocabulary improves Chinese encoding efficiency over the original LLaMA tokenizer
- **+** Pretraining and instruction-tuning scripts are published, so models can be trained further
- **+** Works with llama.cpp, transformers, text-generation-webui, LlamaChat, LangChain and privateGPT
- **+** Weights on Hugging Face and ModelScope, with SHA256 checksums listed
- **−** Original LLaMA weights are required and not provided; LoRA merge is a manual step
- **−** Built on first-generation LLaMA, whose license forbids commercial use
- **−** Superseded by the authors' Alpaca-2 and Alpaca-3 projects; last release July 2023
- **−** README is Chinese-first; C-Eval scores for the 7B models are low

<sub>GPU optional · Needs Original LLaMA weights, transformers, PEFT, llama.cpp · Models: LLaMA 7B/13B/33B LoRA, Alpaca Plus/Pro, HF transformers, llama.cpp 8-bit and 4-bit quantized · [Repo](https://github.com/ymcui/chinese-llama-alpaca) · [▶️ Demo ↗](http://llm-arena.ymcui.com/) · [📖 Docs ↗](https://github.com/ymcui/Chinese-LLaMA-Alpaca/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chinese-llama-alpaca/)</sub>

<a name="gorilla"></a>
### #&#8288;23 [gorilla](https://github.com/shishirpatil/gorilla) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (8) · Freshness: slowing (48) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Mar 2026</sub>

**Function-calling LLMs, API dataset, and the Berkeley Function Calling Leaderboard.**

Gorilla is a Berkeley research project on getting LLMs to call APIs correctly. The repo holds fine-tuned Gorilla and OpenFunctions models, the APIBench dataset (1,600+ APIs), and the Berkeley Function Calling Leaderboard (BFCL) evaluation code. It also includes GoEx, a runtime for LLM-generated actions, RAFT fine-tuning recipes, and Agent Arena.

- **+** Apache 2.0 models, including OpenFunctions-V2 with an OpenAI-compatible function-calling interface
- **+** BFCL covers single-turn, multi-turn and agentic (V4) function calling, with cost and latency metrics
- **+** Includes APIBench dataset and paper evaluation code for reproducing results
- **+** GoEx adds post-facto validation, undo and damage confinement for LLM actions
- **−** Several unrelated sub-projects in one repo; each has its own setup and README
- **−** Original Gorilla models date from 2023 and may trail newer function-calling models
- **−** Last tagged release is 2025-07-17; roadmap items such as OpenFunctions-v3 remain unchecked
- **−** README gives no RAM or VRAM requirements for running models locally

<sub>Models: Gorilla 7B (Hugging Face), Gorilla OpenFunctions-V2, OpenAI-compatible endpoints · [Repo](https://github.com/shishirpatil/gorilla) · [▶️ Demo ↗](https://huggingface.co/spaces/gorilla-llm/gorilla-demo/) · [🌐 Site ↗](https://gorilla.cs.berkeley.edu/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gorilla/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
