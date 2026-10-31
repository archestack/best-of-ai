# 🧬 Open models reviews · Best of Open-Source AI

Repositories of open-weight models with the code to run them: LLMs, vision, speech and embedding models. Back to the [leaderboard](../README.md#-open-models).

<sub>🌐 Also on the web: [Open models on archestack.com](https://archestack.com/best-of-ai/models/), each project on its own page.</sub>

<a name="ruview"></a>
### 🥇 [ruview](https://github.com/ruvnet/ruview) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 102k · MIT · Oct 2026</sub>

**WiFi CSI sensing on ESP32 for presence, breathing, heart rate and pose.**

RuView reads Channel State Information from ESP32-S3/C6 nodes and derives presence, person count, breathing (6–30 BPM), heart rate (40–120 BPM), falls and 17-keypoint pose without cameras. It is written in Rust, with pretrained models on Hugging Face, Home Assistant, Matter and HomeKit integration, and an npm MCP toolkit for AI-guided setup. Several accuracy figures are self-reported, and the README says the on-device pose model is a first cut.

- **+** Runs on roughly $9 ESP32 nodes; the pretrained encoder fits in 8 KB at 4-bit
- **+** Publishes 21 Home Assistant MQTT entities per node, plus Matter and Apple Home bridges
- **+** Pretrained weights on Hugging Face, plus a phase-variance presence fallback needing no model
- **+** README retracts an earlier accuracy claim and flags unvalidated vitals and synthetic RF accuracy
- **−** Live sensing needs ESP32-S3/C6 CSI firmware; the Docker image runs simulated data
- **−** Committed on-device pose model scores PCK@20 of 3.0% and its runtime path is a stub
- **−** Through-wall range is about 5 m and signal-dependent
- **−** Very large README and feature surface; hard to tell which parts are production-ready

<sub>GPU optional · Docker + Compose · Needs ESP32-S3 or ESP32-C6 boards, Cognitum Seed (optional), Home Assistant / MQTT (optional) · Models: safetensors, RVF, Candle · port 3000 · [Repo](https://github.com/ruvnet/ruview) · [📖 Docs ↗](https://github.com/ruvnet/RuView/blob/main/docs/user-guide.md) · [🌐 Site ↗](https://cognitum.one/seed) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ruview/)</sub>

<a name="llmfit"></a>
### 🥈 [llmfit](https://github.com/alexsjones/llmfit) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · MIT · Oct 2026</sub>

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
### 🥉 [laya](https://github.com/nandhakishorm/laya) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;4 [timesfm](https://github.com/google-research/timesfm) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Sep 2026</sub>

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
### #&#8288;5 [speech](https://github.com/nvidia-nemo/speech) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Oct 2026</sub>

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

<a name="yolov5"></a>
### #&#8288;6 [yolov5](https://github.com/ultralytics/yolov5) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (94) · Freshness: recent (70) · Maintenance: fair (61) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · AGPL-3.0 · Oct 2026</sub>

**PyTorch YOLOv5 object detection, segmentation and classification models with training code.**

YOLOv5 provides pretrained COCO checkpoints (n/s/m/l/x, plus 1280px P6 variants) and PyTorch scripts for detection, instance segmentation and classification. detect.py runs on webcams, files, folders, screen capture, YouTube and RTSP/RTMP/HTTP streams, train.py trains on custom data, and models can be exported to ONNX, TensorRT, CoreML and TFLite. The README points newer work to the separate ultralytics package.

- **+** Five model sizes, from 1.9M to 86.7M params, with published CPU and V100 latency
- **+** detect.py accepts webcam, video, screen, YouTube and RTSP/RTMP/HTTP sources
- **+** Export to ONNX, TensorRT, CoreML and TFLite, with a Jetson deployment guide
- **+** Training extras: AutoBatch, multi-GPU, hyperparameter evolution, frozen layers, ClearML and Comet logging
- **−** Last tagged release is v7.0 from 2022-11-22
- **−** AGPL-3.0 license; commercial use needs a paid Enterprise License
- **−** No pose estimation or oriented boxes (OBB); README directs those to the ultralytics package
- **−** COCO training takes about 1 to 8 days per model on one V100

<sub>GPU optional · Needs Python>=3.8, PyTorch>=1.8 · Models: PyTorch .pt, ONNX, TensorRT, CoreML, TFLite · [Repo](https://github.com/ultralytics/yolov5) · [📖 Docs ↗](https://docs.ultralytics.com/yolov5) · [🌐 Site ↗](https://www.ultralytics.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yolov5/)</sub>

<a name="rf-detr"></a>
### #&#8288;7 [rf-detr](https://github.com/roboflow/rf-detr) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · Apache-2.0 · Oct 2026</sub>

**Real-time transformer models for object detection, segmentation and keypoints.**

RF-DETR is a Python package (`pip install rfdetr`, Python 3.10+) from Roboflow that provides pretrained DINOv2-based transformer models for object detection, instance segmentation and keypoint detection (preview). Models come in sizes from Nano to 2XLarge, run through one API via classes like `RFDETRMedium`, and can be fine-tuned on custom datasets. Some sizes (Atto, Femto, Pico, XL, 2XL) are under the PML 1.0 license rather than Apache 2.0.

- **+** Detection, segmentation and keypoints share one Python API across Nano to 2XLarge sizes
- **+** Apache 2.0 for the package and N/S/M/L detection and all segmentation models
- **+** README benchmarks on COCO and RF100-VL, with T4 TensorRT FP16 latency per size
- **+** Fine-tuning supported, with Colab notebook and Hugging Face Space provided
- **−** Atto, Femto, Pico, XL and 2XL detection models use PML 1.0, not Apache 2.0
- **−** Keypoint detection is labeled preview
- **−** Latency figures are T4 TensorRT only; CPU and edge numbers not given in the visible README
- **−** NAS for your own dataset requires the Roboflow platform

<sub>GPU optional · Needs PyTorch, supervision · Models: RF-DETR detection (Atto to 2XL), RF-DETR instance segmentation (Seg-N to Seg-2XL), RF-DETR keypoint (preview), DINOv2 backbone, COCO and custom datasets · [Repo](https://github.com/roboflow/rf-detr) · [▶️ Demo ↗](https://huggingface.co/spaces/SkalskiP/RF-DETR) · [🌐 Site ↗](https://blog.roboflow.com/rf-detr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rf-detr/)</sub>

<a name="yue"></a>
### #&#8288;8 [yue](https://github.com/multimodal-art-projection/yue) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**Lyrics-to-song model that writes an editable melody and chord score first.**

YuE2 generates full songs with vocals and accompaniment from lyrics and a style prompt. It first plans an editable ABC score (melody and chords), then renders semantic tokens and acoustic latents to 48 kHz stereo audio with an AR–NAR Mixture-of-Transformers and a VAE. The repo also covers zero-shot covers via SheetSage2 transcription, score editing, and an agent skill. Code is Apache-2.0; model weights are CC BY-NC 4.0 with an additional creator permission.

- **+** Editable ABC score between prompt and audio lets you inspect and change melody and chords
- **+** Staged Python API: plan, generate_semantic, synthesize, decode; artifacts saved per run
- **+** Zero-shot covers via SheetSage2 transcription with the same checkpoint, no cover fine-tuning
- **+** Reports WildSongBench results against Suno, Mureka and others, with a reproduction guide
- **−** Needs Linux, Python 3.12 and an NVIDIA BF16 GPU with 24 GB VRAM
- **−** Weights are CC BY-NC 4.0; commercial company use requires a separate license
- **−** Editing renders a new recording; the original waveform is not preserved
- **−** Benchmark numbers are automatic metrics from the authors; gaps between top means are not significant

<sub>GPU required · Needs Hugging Face model downloads, SheetSage2 (separate environment, for covers), PyTorch · Models: YuE2-3B, YuE2-Vae, YuE2-Vae-legacy, SheetSage2, MERT-v2 · [Repo](https://github.com/multimodal-art-projection/yue) · [▶️ Demo ↗](https://yue.noizai.net/) · [📖 Docs ↗](https://github.com/multimodal-art-projection/YuE/blob/main/docs/generation.md) · [🌐 Site ↗](https://map-yue2.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yue/)</sub>

<a name="espnet"></a>
### #&#8288;9 [espnet](https://github.com/espnet/espnet) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Oct 2026</sub>

**PyTorch toolkit for speech recognition, synthesis, translation and enhancement.**

ESPnet is a PyTorch speech toolkit covering ASR, TTS, speech translation, enhancement, diarization, singing synthesis and speech language models. It provides Kaldi-style run.sh recipes for 200+ corpora and hundreds of pretrained models on Hugging Face. Inference is available through a CLI (espnet transcribe, synthesize, enhance), a Python API and an MCP server.

- **+** One recipe structure and trainer across ASR, TTS, ST, enhancement, SLU and more
- **+** 200+ corpus recipes with run.sh from data prep to scoring
- **+** Hundreds of pretrained models on Hugging Face, including OWSM v4 multilingual ASR
- **+** pip install espnet gives CLI, Python and MCP inference without the training stack
- **−** Full recipe and training setup needs Kaldi-style tooling beyond pip install
- **−** Recipe workflow assumes research familiarity with stages, corpora and configs
- **−** ESPnet1 is unsupported; ESPnet2 and ESPnet3 recipes coexist
- **−** Hardware requirements for training are not stated in the README

<sub>GPU optional · Docker · Needs PyTorch, Kaldi-style tooling (full recipe setup) · Models: OWSM, Whisper, Conformer, E-Branchformer, VITS · [Repo](https://github.com/espnet/espnet) · [▶️ Demo ↗](https://huggingface.co/spaces/espnet/owsm-ctc-v4) · [📖 Docs ↗](https://espnet.github.io/espnet/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/espnet/)</sub>

<a name="needle"></a>
### #&#8288;10 [needle](https://github.com/cactus-compute/needle) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

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

<a name="ace-step-1-5"></a>
### #&#8288;11 [ace-step-1.5](https://github.com/ace-step/ace-step-1.5) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (50) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Aug 2026</sub>

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

<a name="kev"></a>
### #&#8288;12 [kev](https://github.com/jaredpalmer/kev) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.7k · Apache-2.0 · Oct 2026</sub>

**Small decision models answering yes/no, choice and score questions over text.**

Kev is a family of four fine-tuned Qwen-based models (0.8B, 4B, 9B, 27B) that answer yes/no, multiple-choice and rating questions about a text and return calibrated probabilities. The server exposes an API matching TypeSafe's System One, so the TypeSafe Python SDK works against it. The repo includes training, evaluation and serving code, plus a Modal deploy script and fine-tuning skill.

- **+** Calibrated probabilities: each checkpoint ships with a fitted temperature
- **+** Works with the TypeSafe Python SDK unchanged via the /v1/systemone endpoint
- **+** Four sizes; 0.8B runs on a 4 GB GPU, 27B scores within a point of Jev on new sources
- **+** Fine-tune from released checkpoints; about $1 for a Kev-4B run on a Modal H100
- **−** Not on PyPI; install from source with uv, Python 3.12 or 3.13 only
- **−** Kev-27B is 51 GB of full weights and needs an 80 GB-class GPU
- **−** Trails Jev on harder knowledge tasks, e.g. MMLU-Pro 0.675 vs 0.840 for Kev-27B
- **−** Validated context is 8,192 tokens for 0.8B to 9B, despite a 65,536 server limit

<sub>GPU optional · Needs Modal (optional, for deploy and fine-tune skill), uv, Hugging Face Hub · Models: Kev-0.8B, Kev-4B, Kev-9B, Kev-27B, Qwen3.5 base · port 8009 · [Repo](https://github.com/jaredpalmer/kev) · [▶️ Demo ↗](https://huggingface.co/spaces/jaredpalmer/kev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kev/)</sub>

<a name="unlimited-ocr"></a>
### #&#8288;13 [unlimited-ocr](https://github.com/baidu/unlimited-ocr) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: weak (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Oct 2026</sub>

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

<a name="insightface"></a>
### #&#8288;14 [insightface](https://github.com/deepinsight/insightface) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 30k · no license · Oct 2026</sub>

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

<a name="flagembedding"></a>
### #&#8288;15 [flagembedding](https://github.com/flagopen/flagembedding) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (41) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Oct 2026</sub>

**BGE embedding and reranker models with inference, fine-tuning and evaluation code.**

FlagEmbedding is the Python package and code repository for BAAI's BGE embedding and reranker models. It covers inference, fine-tuning and evaluation for dense, sparse and multi-vector retrieval. The model list includes BGE-M3 (100+ languages, 8192 tokens), bge-en-icl and several cross-encoder rerankers. Tutorials and research code are included.

- **+** Embedders and rerankers with inference, fine-tuning and evaluation scripts in one package
- **+** BGE-M3 supports dense, sparse and multi-vector retrieval, 100+ languages, 8192-token input
- **+** MIT license; models published on Hugging Face and package installable via pip
- **+** Includes hard-negative mining, fine-tune scripts and retrieval/RAG tutorials
- **−** Library only: no server, UI or vector store, so retrieval pipeline is yours to wire
- **−** README is a long news log; some research code lives in separate repos
- **−** Fine-tuning needs the extra [finetune] install; hardware requirements are unknown
- **−** Query instructions differ per model and must be set correctly

<sub>GPU optional · Models: BGE embedding models (Hugging Face), BGE rerankers, BGE-M3, bge-en-icl, bge-multilingual-gemma2 · [Repo](https://github.com/flagopen/flagembedding) · [📖 Docs ↗](https://www.bge-model.com) · [🌐 Site ↗](https://flagopen.baai.ac.cn/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flagembedding/)</sub>

<a name="open-clip"></a>
### #&#8288;16 [open_clip](https://github.com/mlfoundations/open_clip) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (51) · Freshness: active (95) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · custom license · Oct 2026</sub>

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

<a name="minicpm-v"></a>
### #&#8288;17 [minicpm-v](https://github.com/openbmb/minicpm-v) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (75) · Freshness: recent (72) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · Apache-2.0 · Oct 2026</sub>

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

<a name="cosmos"></a>
### #&#8288;18 [cosmos](https://github.com/nvidia/cosmos) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: known (40) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · custom license · Oct 2026</sub>

**Open world foundation models for robotics and driving: video, reasoning, policies.**

Landing repo for Cosmos 3, a family of omnimodal world models with a Reasoner (text and vision to text) and a Generator (text, vision, audio, action to vision, audio, action). Ships three base sizes (Super 64B, Nano 16B, Edge 4B) plus post-trained checkpoints for driving simulation, transfer and DROID robot policies. The repo holds a cookbook of notebooks; training, curation and evaluation live in separate Cosmos repos.

- **+** Three sizes: 64B Super, 16B Nano, 4B Edge for Jetson and RTX Pro 6000
- **+** Runs on Diffusers, Transformers, vLLM, vLLM-Omni, SGLang, TensorRT-LLM and NIM
- **+** Post-trained checkpoints for driving simulation, multi-view transfer and DROID robot policy
- **+** Companion repos cover SFT, LoRA, RL, distillation, data curation and evaluation
- **−** Target hardware is H100, H200, B200, Jetson or RTX Pro 6000 class GPUs
- **−** Quickstart needs gated access to the Cosmos-1.0-Guardrail repo on Hugging Face
- **−** License is OpenMDW-1.1, not a common OSI license; custom licensing by email
- **−** README warns of artifacts in long, high-resolution or physically complex outputs

<sub>GPU required · Needs Hugging Face account and token, Cosmos-1.0-Guardrail (gated), PyTorch, diffusers · Models: Cosmos3-Super 64B, Cosmos3-Nano 16B, Cosmos3-Edge 4B, Diffusers, Transformers · [Repo](https://github.com/nvidia/cosmos) · [▶️ Demo ↗](https://build.nvidia.com/nvidia/cosmos3-nano-reasoner) · [📖 Docs ↗](https://github.com/NVIDIA/cosmos/blob/main/COOKBOOK.md) · [🌐 Site ↗](https://research.nvidia.com/labs/cosmos-lab/cosmos3/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cosmos/)</sub>

<a name="alphafold3"></a>
### #&#8288;19 [alphafold3](https://github.com/google-deepmind/alphafold3) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · Apache-2.0 · Oct 2026</sub>

**Inference pipeline for AlphaFold 3 biomolecular structure prediction.**

Runs the AlphaFold 3 inference pipeline, predicting structures of proteins, nucleic acids, ligands and their complexes from a JSON input. The pipeline has a CPU-only genetic and template search stage and a GPU inference stage, which can be run separately. Model parameters are not included and must be requested from Google under separate terms of use.

- **+** Code is Apache-2.0 and covers the full inference path from JSON input to structure output
- **+** Data pipeline and inference can run separately via --run_data_pipeline and --run_inference
- **+** Alternative weights offered: SynthID Bio watermarked and Leaving Atom fine-tuned variants
- **+** Built on JAX and Haiku, with separate input, output and performance docs
- **−** Weights are not open: use only if received directly from Google, under terms of use
- **−** Requires separate genetic databases to be downloaded; sizes not stated in the README
- **−** Inference needs a GPU; the README gives no VRAM or RAM figures
- **−** Only the inference pipeline is included, no training code

<sub>GPU required · Docker · Needs Docker, Model parameters from Google, Genetic sequence databases (BFD, MGnify, UniRef90, UniProt, PDB, NT, RFam, RNACentral), HMMER · Models: AlphaFold 3, AlphaFold 3 SynthID Bio, AlphaFold 3 Leaving Atom · [Repo](https://github.com/google-deepmind/alphafold3) · [▶️ Demo ↗](https://alphafoldserver.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/alphafold3/)</sub>

<a name="lingbot-map"></a>
### #&#8288;20 [lingbot-map](https://github.com/robbyant/lingbot-map) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

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

<a name="minicpm"></a>
### #&#8288;21 [minicpm](https://github.com/openbmb/minicpm) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (37) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Sep 2026</sub>

**Small open-weight LLM family for on-device use, latest is MiniCPM5-2B.**

Weights and code for the MiniCPM series of compact dense LLMs. The current release, MiniCPM5-2B, is a 2.5B-parameter Llama-architecture model with a 131,072-token context, published in BF16, GGUF, MLX and GPTQ builds. The repo also links the training datasets (UltraData family), a DSpark speculative-decoding draft model, and deployment and fine-tuning agent skills.

- **+** Standard LlamaForCausalLM architecture, so it loads in vLLM, SGLang, llama.cpp and Transformers
- **+** Ships GGUF, MLX and GPTQ builds plus a DSpark draft model for speculative decoding
- **+** Pretraining, code, SFT, agent and RL datasets are released alongside the model
- **+** 131,072-token context in a 2B-class model; 1B and older sizes also available
- **−** Benchmark claims come from the authors' own comparison set; no independent results cited
- **−** Repo is mostly docs and notebooks; weights are hosted on Hugging Face and ModelScope
- **−** Needs separate inference software; no bundled server or chat UI
- **−** Wiki is in Chinese only; RAM and VRAM requirements are not stated in the README

<sub>GPU optional · Needs vLLM, SGLang, llama.cpp, Transformers · Models: BF16, GGUF, MLX, GPTQ, MiniCPM5-2B · [Repo](https://github.com/openbmb/minicpm) · [▶️ Demo ↗](https://huggingface.co/spaces/openbmb/MiniCPM5-2B-Demo) · [📖 Docs ↗](https://modelbest.feishu.cn/wiki/UtWxwcERfiRIpIkBOjuc3h9tn1D?fromScene=spaceOverview) · [🌐 Site ↗](https://ultradata.openbmb.cn/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/minicpm/)</sub>

<a name="yolov3"></a>
### #&#8288;22 [yolov3](https://github.com/ultralytics/yolov3) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (33) · Freshness: recent (70) · Maintenance: fair (62) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · AGPL-3.0 · Oct 2026</sub>

**PyTorch implementation of YOLOv3, YOLOv3-SPP and YOLOv3-tiny object detectors.**

PyTorch code for the three classic YOLOv3 object detection models, with scripts for training, validation, inference and export. Pretrained COCO checkpoints (80 classes) download automatically, and models can be exported to TorchScript, ONNX, OpenVINO, TensorRT, CoreML and PaddlePaddle. It reuses shared utilities from the ultralytics package.

- **+** Three variants (YOLOv3, SPP, tiny) with COCO-pretrained weights that download automatically
- **+** Export to ONNX, TensorRT, OpenVINO, CoreML, TorchScript and PaddlePaddle via export.py
- **+** detect.py accepts webcam, video, screenshot, glob and RTSP/RTMP/HTTP stream sources
- **+** Models defined in YAML files, so architectures can be edited without Python changes
- **−** AGPL-3.0; commercial use without AGPL obligations needs a paid Enterprise License
- **−** Last release was 2021-11-14, though commits continue
- **−** Covers only the 2018-era YOLOv3 architecture; newer Ultralytics models live in a separate repo
- **−** README gives no VRAM or RAM figures and no benchmark numbers

<sub>GPU optional · Needs Python>=3.8, PyTorch>=1.8 · Models: YOLOv3, YOLOv3-SPP, YOLOv3-tiny, COCO, ONNX · [Repo](https://github.com/ultralytics/yolov3) · [📖 Docs ↗](https://docs.ultralytics.com/models/yolov3) · [🌐 Site ↗](https://www.ultralytics.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yolov3/)</sub>

<a name="gpt-oss"></a>
### #&#8288;23 [gpt-oss](https://github.com/openai/gpt-oss) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (68) · Freshness: active (91) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;24 [mamba](https://github.com/state-spaces/mamba) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: popular (64) · Freshness: active (97) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Jul 2026</sub>

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

<a name="weathernext"></a>
### #&#8288;25 [weathernext](https://github.com/google-deepmind/weathernext) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · Apache-2.0 · Sep 2026</sub>

**JAX code and weights for DeepMind's WeatherNext 2 and cyclone forecast models.**

Research code to run WeatherNext 2, WeatherNext Cyclones, and the earlier GraphCast and GenCast models for global medium-range weather and tropical cyclone forecasting. Pretrained weights are in a Google Cloud bucket, and a Colab notebook covers loading weights, autoregressive rollouts, plotting and the cyclone tracker. Full-size 0.25° models need an H100 or TPU; the 1° Mini models are meant for smaller hardware.

- **+** Includes weights for operational 0.25° models and checkpoints that reproduce the Nature cyclone paper
- **+** Colab notebook defaults to the 1° Mini model on a free v5e-1 TPU runtime
- **+** Also contains GraphCast and GenCast code plus shared rollout and loss utilities
- **+** Includes training loss and gradient-step code, not just inference
- **−** README calls it research code with no API stability guarantees; pinning a release is advised
- **−** Non-Mini models need an H100 or TPU v5p; Mini models run on a P100
- **−** Optimised for TPU; GPU use requires switching the attention implementation
- **−** Non-code materials are CC BY 4.0; only code and notebooks are Apache 2.0

<sub>GPU required · Needs JAX, Google Cloud Storage (weights), ERA5 (training), ECMWF HRES (initial conditions), WeatherBench2 · Models: WeatherNext 2, WeatherNext Cyclones, WeatherNext Cyclones Mini, GraphCast, GenCast · [Repo](https://github.com/google-deepmind/weathernext) · [▶️ Demo ↗](https://colab.research.google.com/github/google-deepmind/weathernext/blob/master/docs/weathernext2/wn2_demo.ipynb) · [📖 Docs ↗](https://developers.google.com/weathernext/guides/models) · [🌐 Site ↗](https://deepmind.google.com/science/weatherlab) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/weathernext/)</sub>

<a name="glm-5"></a>
### #&#8288;26 [glm-5](https://github.com/zai-org/glm-5) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Oct 2026</sub>

**Open-weight GLM-5 series LLMs for coding and long-horizon agent tasks.**

Release repository for the GLM-5, 5.1, 5.2 and 5.3 model families from Z.ai, with Hugging Face and ModelScope links in FP8 and BF16. The large models are 744B parameters (40B active); GLM-5.3-Flash is 320B (18B active) with hybrid sparse and linear attention. The README covers serving through SGLang, vLLM, Transformers, KTransformers and Unsloth, and fine-tuning with Slime and ms-swift.

- **+** Apache-2.0 repo; weights offered in both FP8 and BF16 for each release
- **+** Serving guides for SGLang, vLLM, Transformers, KTransformers, Unsloth and Ascend NPU
- **+** GLM-5.2 documented with a 1M-token context
- **+** Adjustable reasoning_effort (low, high, max) on GLM-5.3 models
- **−** 744B-parameter models need multi-GPU servers; README gives no hardware requirements
- **−** Repo holds docs and links only; weights live on Hugging Face and ModelScope
- **−** Benchmark claims are Z.ai's own, including its in-house Code Bench
- **−** reasoning_effort defaults to max; clear_thinking must be set explicitly for chat

<sub>GPU required · Needs SGLang, vLLM, Transformers, KTransformers, Unsloth · Models: GLM-5, GLM-5.1, GLM-5.2, GLM-5.3, GLM-5.3-Flash · [Repo](https://github.com/zai-org/glm-5) · [▶️ Demo ↗](https://z.ai) · [📖 Docs ↗](https://docs.z.ai/guides/llm/glm-5.3) · [🌐 Site ↗](https://z.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/glm-5/)</sub>

<a name="spleeter"></a>
### #&#8288;27 [spleeter](https://github.com/deezer/spleeter) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (78) · Freshness: recent (70) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Oct 2026</sub>

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

<a name="trellis"></a>
### #&#8288;28 [trellis](https://github.com/microsoft/trellis) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (48) · Freshness: active (100) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

**Image- and text-to-3D asset generation model from Microsoft Research.**

TRELLIS generates 3D assets from an image or text prompt using a structured latent (SLat) representation and rectified flow transformers. One latent decodes to 3D Gaussians, radiance fields or meshes, with GLB and PLY export. Pretrained models range from 342M to 2.0B parameters, and the repo includes training code and TRELLIS-500K dataset tooling.

- **+** One latent decodes to Gaussians, radiance fields or meshes; GLB and PLY export
- **+** Training code, configs and TRELLIS-500K dataset tooling are included
- **+** Supports variant generation, local editing and multi-image conditioning
- **+** MIT license, weights on Hugging Face, hosted live demo
- **−** Requires an NVIDIA GPU with at least 16GB memory
- **−** Tested only on Linux; Windows setup is not fully tested
- **−** Install compiles several CUDA submodules and needs a CUDA Toolkit
- **−** Text-conditioned models are less detailed than the image-conditioned model

<sub>GPU required · Needs CUDA Toolkit 11.8 or 12.2, Conda, PyTorch 2.4.0, flash-attn or xformers, spconv, kaolin, nvdiffrast, Gradio (demo) · Models: TRELLIS-image-large (1.2B), TRELLIS-text-base (342M), TRELLIS-text-large (1.1B), TRELLIS-text-xlarge (2.0B) · [Repo](https://github.com/microsoft/trellis) · [▶️ Demo ↗](https://huggingface.co/spaces/Microsoft/TRELLIS) · [🌐 Site ↗](https://microsoft.github.io/TRELLIS/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trellis/)</sub>

<a name="moss"></a>
### #&#8288;29 [moss](https://github.com/openmoss/moss) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (42) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Sep 2026</sub>

**Bilingual Chinese-English 16B chat model with plugins, data and fine-tuning code.**

MOSS-003 is a 16B-parameter Chinese/English conversational language model from Fudan University, released as base, SFT and plugin-tuned checkpoints on Hugging Face. The repo includes the roughly 1.1M-dialogue SFT data, Transformers inference examples, GPTQ int4/int8 variants and fine-tuning code. The plugin variant calls web search, calculator, equation solver and text-to-image through a text command format.

- **+** Int4 checkpoints run on one GPU at about 12GB VRAM for a single turn
- **+** Releases SFT conversation data, including about 300k plugin-augmented dialogues
- **+** Plugin model emits explicit Search/Calculate/Solve/Text2Image commands you wire up yourself
- **+** Includes both single-GPU and multi-GPU (accelerate) inference examples
- **−** Model weights are AGPL-3.0 and data is CC BY-NC 4.0, unlike the Apache-2.0 code
- **−** FP16 needs about 31GB to load and 81GB at the 2048-token maximum
- **−** Quantized models run on a single card only and need triton, so Linux or WSL only
- **−** Preference-tuned moss-moon-003 models are listed as coming soon, not released

<sub>GPU required · Needs PyTorch, transformers, accelerate, triton (quantized models), conda · Models: moss-moon-003-base, moss-moon-003-sft, moss-moon-003-sft-plugin, GPTQ int4, GPTQ int8 · [Repo](https://github.com/openmoss/moss) · [🌐 Site ↗](https://txsun1997.github.io/blogs/moss.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moss/)</sub>

<a name="sensenova-u1"></a>
### #&#8288;30 [sensenova-u1](https://github.com/opensensenova/sensenova-u1) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Oct 2026</sub>

**Open 8B multimodal model for image generation, editing and visual Q&A.**

SenseNova-U1 and U1.5 are open-weight native multimodal models (8B-MoT, plus an A3B variant) that handle text-to-image, image editing, interleaved image-text generation and visual question answering in one model. The repo ships Python inference scripts for Transformers, optional GGUF checkpoint loading, 8-step LoRA checkpoints, a ComfyUI workflow and full-parameter fine-tuning code. Production serving is documented separately with LightLLM and LightX2V.

- **+** One checkpoint covers text-to-image, editing, interleaved generation and VQA
- **+** Native 4K generation and bounding-box or reference-based visual control in U1.5
- **+** 8-step LoRA and GGUF checkpoints reduce latency and VRAM use
- **+** Training code, technical reports and a ComfyUI workflow are included
- **−** README admits dense text, hands, small faces and multi-turn edits can still fail
- **−** Official GGUF weights for U1.5 are not out yet; current GGUFs are community-made
- **−** VRAM and RAM requirements are not stated in the visible README
- **−** No tagged release; weights are distributed via Hugging Face and ModelScope

<sub>Needs PyTorch, Transformers, LightLLM (production serving), LightX2V (production serving), gguf and diffusers (optional GGUF) · Models: SenseNova-U1.5-8B-MoT, SenseNova-U1-8B-MoT, SenseNova-U1-A3B-MoT, safetensors LoRA, GGUF Q8 · [Repo](https://github.com/opensensenova/sensenova-u1) · [▶️ Demo ↗](https://unify.light-ai.top/) · [📖 Docs ↗](https://github.com/OpenSenseNova/SenseNova-U1/blob/main/docs/deployment.md) · [🌐 Site ↗](https://huggingface.co/blog/sensenova/neo-unify) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sensenova-u1/)</sub>

<a name="chronos-forecasting"></a>
### #&#8288;31 [chronos-forecasting](https://github.com/amazon-science/chronos-forecasting) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Oct 2026</sub>

**Pretrained zero-shot time series forecasting models with a Python pipeline.**

Python package that loads the Chronos family of pretrained time series models (Chronos-2, Chronos-Bolt, original T5-based Chronos) from Hugging Face and produces probabilistic quantile forecasts. Chronos-2 handles univariate, multivariate and covariate-informed forecasting zero-shot and takes pandas DataFrames through predict_df. Model sizes range from 8M to 710M parameters.

- **+** Zero-shot forecasting with covariates and multivariate series in Chronos-2 (120M parameters)
- **+** Size range of 8M to 710M parameters across three model generations
- **+** DataFrame-based predict_df API returns quantile forecasts; installs with pip
- **+** Apache-2.0, with notebooks and AWS deployment guides (SageMaker JumpStart, AutoGluon-Cloud)
- **−** README gives no RAM or VRAM requirements
- **−** Fine-tuning is not documented in the README
- **−** Production deployment guidance centers on AWS
- **−** No hosted demo; quick start runs in Colab or SageMaker Studio Lab notebooks

<sub>GPU optional · Needs Hugging Face model hub, pandas[pyarrow] · Models: Chronos-2, Chronos-Bolt, Chronos-T5 · [Repo](https://github.com/amazon-science/chronos-forecasting) · [📖 Docs ↗](https://auto.gluon.ai/cloud/stable/tutorials/foundation-model-timeseries.html) · [🌐 Site ↗](https://huggingface.co/collections/amazon/chronos-models-65f1791d630a8d57cb718444) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chronos-forecasting/)</sub>

<a name="kronos"></a>
### #&#8288;32 [kronos](https://github.com/shiyu-coder/kronos) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: widely used (91) · Freshness: recent (60) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · MIT · Apr 2026</sub>

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

<a name="unilm"></a>
### #&#8288;33 [unilm](https://github.com/microsoft/unilm) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (71) · Freshness: recent (70) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Sep 2026</sub>

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

<a name="omniparser"></a>
### #&#8288;34 [omniparser](https://github.com/microsoft/omniparser) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (74) · Freshness: recent (77) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · CC-BY-4.0 · Jul 2026</sub>

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

<a name="rwkv-lm"></a>
### #&#8288;35 [rwkv-lm](https://github.com/blinkdl/rwkv-lm) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (54) · Freshness: recent (70) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

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

<a name="qwen"></a>
### #&#8288;36 [qwen](https://github.com/qwenlm/qwen) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (69) · Freshness: slowing (45) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Mar 2026</sub>

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

<a name="clip"></a>
### #&#8288;37 [clip](https://github.com/openai/clip) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: widely used (84) · Freshness: recent (53) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · MIT · Mar 2026</sub>

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

<a name="onnx-models"></a>
### #&#8288;38 [models](https://github.com/onnx/models) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.8k · Apache-2.0 · Oct 2026</sub>

**Archived collection of pre-trained models exported to ONNX format.**

Git LFS repository of pre-trained ONNX models for image classification, object detection and segmentation, face analysis, style transfer, machine comprehension, translation and language modelling. Models come from timm, torchvision, torch_hub and transformers, exported with TurnkeyML, with INT8 variants from Intel Neural Compressor. The repo is deprecated: LFS downloads ended July 1, 2025, and the models are now at huggingface.co/onnxmodelzoo.

- **+** Per-model folders with .onnx files and test data (.pb, .npz) for validating outputs
- **+** Includes INT8 quantized variants generated by Intel Neural Compressor
- **+** Covers classic vision models (ResNet, YOLOv4, Mask-RCNN, ArcFace) with paper references
- **−** Deprecated and kept for historical purposes only
- **−** Git LFS model downloads ended July 1, 2025; files must come from Hugging Face
- **−** Mostly older CNN-era models; no current LLMs in the visible README
- **−** No releases published

<sub>GPU optional · Needs Git LFS · Models: ONNX, INT8 (QDQ) · [Repo](https://github.com/onnx/models) · [🌐 Site ↗](https://huggingface.co/onnxmodelzoo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onnx-models/)</sub>

<a name="deepresearch"></a>
### #&#8288;39 [deepresearch](https://github.com/alibaba-nlp/deepresearch) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (66) · Freshness: slowing (43) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Feb 2026</sub>

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

<a name="trellis-2"></a>
### #&#8288;40 [trellis.2](https://github.com/microsoft/trellis.2) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (43) · Freshness: recent (79) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Jun 2026</sub>

**Image-to-3D generator producing PBR-textured meshes from a 4B-parameter model.**

TRELLIS.2 is Microsoft's 4B-parameter image-to-3D model built on a sparse voxel representation called O-Voxel. It generates textured assets at 512³ to 1536³ resolution with base color, roughness, metallic and opacity, and exports GLB. The repo includes inference scripts, a web demo, shape-conditioned texturing, and full training code.

- **+** Handles open surfaces, non-manifold geometry and internal structures without iso-surface conversion
- **+** Reported H100 times: about 3s at 512³, 17s at 1024³, 60s at 1536³
- **+** Full training code and data toolkit included, plus shape-conditioned PBR texturing
- **+** MIT license for code and model; weights on Hugging Face with a hosted demo
- **−** Needs an NVIDIA GPU with at least 24GB memory; tested only on A100 and H100
- **−** Tested only on Linux; setup compiles CUDA packages and may be slow
- **−** GLB exports as OPAQUE; transparency must be wired up manually in 3D software
- **−** nvdiffrast and nvdiffrec dependencies carry separate license terms

<sub>GPU required · Needs CUDA Toolkit 12.4, PyTorch 2.6.0, Conda, flash-attn, nvdiffrast, nvdiffrec, CuMesh, FlexGEMM · Models: TRELLIS.2-4B · [Repo](https://github.com/microsoft/trellis.2) · [▶️ Demo ↗](https://huggingface.co/spaces/microsoft/TRELLIS.2) · [🌐 Site ↗](https://microsoft.github.io/TRELLIS.2) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trellis-2/)</sub>

<a name="chinese-llama-alpaca"></a>
### #&#8288;41 [chinese-llama-alpaca](https://github.com/ymcui/chinese-llama-alpaca) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: popular (63) · Freshness: slowing (43) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Apr 2026</sub>

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

<a name="wan2-1"></a>
### #&#8288;42 [wan2.1](https://github.com/wan-video/wan2.1) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: popular (59) · Freshness: slowing (45) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Mar 2026</sub>

**Open-weight video generation models with PyTorch inference code for text and image input.**

Wan2.1 is a set of open-weight video diffusion models (T2V 1.3B and 14B, I2V 14B, first-last-frame 14B, VACE 1.3B and 14B) with a generate.py CLI, Gradio demos and multi-GPU inference via FSDP and xDiT. The T2V-1.3B model needs 8.19 GB VRAM and makes a 5-second 480P clip on an RTX 4090 in about 4 minutes. Weights are on Hugging Face and ModelScope, and Diffusers and ComfyUI integrations exist.

- **+** T2V-1.3B runs in 8.19 GB VRAM on consumer GPUs, 480P
- **+** Covers text-to-video, image-to-video, first-last-frame, and VACE editing in one repo
- **+** Multi-GPU inference with FSDP and xDiT Ulysses/Ring parallelism
- **+** Diffusers and ComfyUI integrations; Apache-2.0 weights on Hugging Face and ModelScope
- **−** 14B models need far more VRAM; the README gives no figure
- **−** 1.3B model is less stable at 720P; 480P recommended
- **−** Prompt extension needs a Dashscope API key or a local Qwen model
- **−** Diffusers multi-GPU and FLF2V Diffusers/ComfyUI support are unchecked in the todo list

<sub>GPU required · Needs PyTorch >= 2.4.0, Hugging Face Hub or ModelScope for weights, xfuser >= 0.4.1 for multi-GPU, Dashscope API or local Qwen (optional, prompt extension) · Models: Wan2.1-T2V-1.3B, Wan2.1-T2V-14B, Wan2.1-I2V-14B-480P/720P, Wan2.1-FLF2V-14B-720P, Wan2.1-VACE-1.3B/14B · [Repo](https://github.com/wan-video/wan2.1) · [🌐 Site ↗](https://wan.video) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/wan2-1/)</sub>

<a name="alphafold"></a>
### #&#8288;43 [alphafold](https://github.com/google-deepmind/alphafold) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: popular (55) · Freshness: slowing (44) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Apr 2026</sub>

**Protein structure prediction inference pipeline from AlphaFold v2, including Multimer.**

Runs the AlphaFold v2 inference pipeline: takes FASTA sequences, searches genetic databases for MSAs and templates, and predicts 3D structures with monomer, pTM and Multimer model presets. It is driven by a Docker wrapper (run_docker.py) and requires a Linux machine with an NVIDIA GPU. Code is Apache-2.0; the model parameters are CC BY 4.0.

- **+** Presets for monomer, CASP14 ensemble, pTM and AlphaFold-Multimer complexes
- **+** Reduced_dbs preset runs with 8 CPU cores, 8 GB RAM and 600 GB disk
- **+** Download scripts fetch databases and parameters; MSAs can be reused via --use_precomputed_msas
- **+** README publishes A100 runtimes by residue count, from 4.9 s at 100 to 18,824 s at 5,000
- **−** Full databases need about 556 GB download and 2.62 TB unpacked
- **−** Linux only; requires a modern NVIDIA GPU and the NVIDIA Container Toolkit
- **−** Last release was 2023-04-05; Multimer described as work in progress
- **−** Model parameters are CC BY 4.0, separate from the Apache-2.0 code

<sub>RAM ≥ 8 GB · GPU required · Docker · Needs Docker, NVIDIA Container Toolkit, aria2c, rsync, BFD, MGnify, PDB70, PDB mmCIF, UniRef30, UniRef90, UniProt · Models: AlphaFold v2 monomer, monomer_casp14, monomer_ptm, AlphaFold-Multimer · [Repo](https://github.com/google-deepmind/alphafold) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/alphafold/)</sub>

<a name="moondream"></a>
### #&#8288;44 [moondream](https://github.com/m87-labs/moondream) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: known (31) · Freshness: recent (62) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Apr 2026</sub>

**Small vision language model for captioning, visual Q&A and object detection.**

Moondream is an open-weight vision language model that answers questions about images, writes captions and detects objects. It comes in two sizes: a 2B-parameter general model and a 0.5B model meant as a distillation target for edge devices. It can be run locally or through a hosted cloud service, with setup covered in the external quickstart docs.

- **+** Two sizes: 2B for general use, 0.5B for resource-constrained edge devices
- **+** Covers captioning, visual question answering and object detection in one model
- **+** Apache-2.0 license, with a hosted playground for trying it before installing
- **−** README gives no RAM, VRAM or latency figures
- **−** README has no install or run steps; it points to external docs
- **−** No Docker setup or tagged release in the repository
- **−** No benchmark results in the README

<sub>Models: Moondream 2B, Moondream 0.5B · [Repo](https://github.com/m87-labs/moondream) · [▶️ Demo ↗](https://moondream.ai/playground) · [📖 Docs ↗](https://moondream.ai/c/docs/quickstart) · [🌐 Site ↗](https://moondream.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moondream/)</sub>

<a name="chinese-bert-wwm"></a>
### #&#8288;45 [chinese-bert-wwm](https://github.com/ymcui/chinese-bert-wwm) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: known (32) · Freshness: recent (62) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Apr 2026</sub>

**Chinese BERT and RoBERTa checkpoints pre-trained with whole word masking.**

Pre-trained Chinese BERT-wwm, BERT-wwm-ext, RoBERTa-wwm-ext (base and large), RBT3 and RBTL3 checkpoints from HFL. Whole word masking uses LTP word segmentation so all characters of a word are masked together. Weights are TensorFlow checkpoints (Baidu Netdisk) and PyTorch weights on Hugging Face, loadable with BertTokenizer/BertModel; the README includes benchmark tables on CMRC 2018, DRCD, XNLI and others.

- **+** Hugging Face and PaddleHub loading, via BertTokenizer/BertModel with hfl/ model names
- **+** Includes 3-layer RBT3 (38M) and RBTL3 (61M) models for lower-cost inference
- **+** Benchmark tables report max and mean over 10 seeds on eight Chinese datasets
- **+** Same vocab and config as Google's Chinese BERT, so existing BERT code works unchanged
- **−** Pre-training code is not provided; the FAQ points to issue threads only
- **−** Released weights omit the MLM head, so masked-LM use needs further pre-training
- **−** Original checkpoints are TensorFlow; PyTorch needs conversion or the HF download
- **−** README is mostly Chinese, and the repo is a 2019-era encoder line, with a banner promoting newer LLM projects

<sub>GPU optional · Needs transformers, TensorFlow or PyTorch, PaddleHub (optional) · Models: BERT-wwm, BERT-wwm-ext, RoBERTa-wwm-ext, RoBERTa-wwm-ext-large, RBT3 · [Repo](https://github.com/ymcui/chinese-bert-wwm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chinese-bert-wwm/)</sub>

<a name="gorilla"></a>
### #&#8288;46 [gorilla](https://github.com/shishirpatil/gorilla) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: known (46) · Freshness: slowing (42) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Mar 2026</sub>

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

<a name="z-image"></a>
### #&#8288;47 [z-image](https://github.com/tongyi-mai/z-image) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: known (38) · Freshness: slowing (37) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Feb 2026</sub>

**6B-parameter text-to-image diffusion model family with an 8-step Turbo variant.**

Z-Image is a family of 6B-parameter image generation models built on a single-stream diffusion transformer (S3-DiT), with PyTorch and diffusers inference code. Z-Image-Turbo is a distilled variant that runs in 8 function evaluations and fits in 16 GB VRAM, while Z-Image is the 50-step base model with CFG and negative prompts. Omni-Base and Edit variants are listed as not yet released.

- **+** Turbo variant needs 8 NFEs and fits in 16 GB VRAM consumer GPUs
- **+** Base Z-Image supports CFG and negative prompts, and is aimed at fine-tuning
- **+** Renders English and Chinese text in images
- **+** Community ports: stable-diffusion.cpp runs it on 4 GB VRAM, plus vllm-omni and SGLang support
- **−** Omni-Base and Edit checkpoints are marked 'To be released' in the model zoo
- **−** Turbo has low output diversity and no CFG, per the README table
- **−** Diffusers support requires installing from source per the README
- **−** No release tags; inference is a script plus library, not a server or UI

<sub>GPU required · Needs PyTorch, diffusers · Models: Z-Image, Z-Image-Turbo, Hugging Face safetensors checkpoints, diffusers ZImagePipeline · [Repo](https://github.com/tongyi-mai/z-image) · [▶️ Demo ↗](https://huggingface.co/spaces/Tongyi-MAI/Z-Image-Turbo) · [🌐 Site ↗](https://tongyi-mai.github.io/Z-Image-blog/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/z-image/)</sub>

<a name="qwen3"></a>
### #&#8288;48 [qwen3](https://github.com/qwenlm/qwen3) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: popular (77) · Freshness: quiet (25) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 28k · no license · Jan 2026</sub>

**Open-weight Qwen3 LLM family with dense and MoE models, 0.6B to 235B.**

Qwen3 is Alibaba's open-weight LLM series, with dense models from 0.6B to 32B and MoE models at 30B-A3B and 235B-A22B. The repo is mainly a README that links to checkpoints on Hugging Face and ModelScope, plus run and deploy instructions for Transformers, llama.cpp, Ollama, vLLM, SGLang and TensorRT-LLM. The 2507 update splits the line into Instruct and Thinking variants with 256K context, extendable to 1M tokens.

- **+** Wide size range: 0.6B, 1.7B, 4B, 8B, 14B, 32B, 30B-A3B, 235B-A22B
- **+** Run guides for llama.cpp, Ollama, LM Studio, MLX, OpenVINO, ExecuTorch and MNN
- **+** Serving examples for vLLM, SGLang and TensorRT-LLM expose an OpenAI-compatible API
- **+** 256K native context in 2507 models, extendable to 1M tokens
- **−** No license detected in the repo; terms must be checked on each model card
- **−** Repo holds docs and snippets, not the training code or data
- **−** Multi-step tool use with thinking models may degrade in vLLM and SGLang
- **−** Qwen3-2507 evaluation blog is listed as coming soon

<sub>GPU optional · Needs transformers>=4.51.0, llama.cpp>=b5401, vllm>=0.9.0, sglang>=0.4.6.post1 · Models: Transformers, GGUF, GPTQ, AWQ, MLX · [Repo](https://github.com/qwenlm/qwen3) · [▶️ Demo ↗](https://huggingface.co/spaces/Qwen/Qwen3-Demo) · [📖 Docs ↗](https://qwen.readthedocs.io/) · [🌐 Site ↗](https://chat.qwen.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwen3/)</sub>

<a name="bagel"></a>
### #&#8288;49 [bagel](https://github.com/bytedance-seed/bagel) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: niche (5) · Freshness: recent (67) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · May 2026</sub>

**Open multimodal model for image understanding, text-to-image and image editing.**

BAGEL is a 7B-active (14B total) Mixture-of-Transformer-Experts model that handles visual understanding, text-to-image generation and image editing in one checkpoint. The repo provides inference code, a Gradio web app with NF4 and INT8 quantization modes, and training and evaluation scripts. Weights are on Hugging Face as BAGEL-7B-MoT.

- **+** One checkpoint covers understanding, generation and editing; reports GenEval 0.82 and MMBench 85.0
- **+** Includes training (scripts/train.sh) and evaluation scripts for VLM, T2I and editing benchmarks
- **+** Gradio app offers an NF4 mode for 12-32GB VRAM GPUs
- **+** Apache-2.0; community ComfyUI node, Dockerfiles and DF11/INT8 weights exist
- **−** Full-precision app needs a 32GB+ VRAM GPU or multiple GPUs
- **−** Requires flash_attn==2.5.8, which complicates setup
- **−** README advises against the INT8 mode; quantized inference is community-contributed
- **−** No tagged release; Dockerfiles are linked from issues, not shipped in the repo

<sub>GPU required · Needs Python 3.10, conda, flash_attn 2.5.8, Hugging Face Hub · Models: BAGEL-7B-MoT safetensors, NF4, INT8, DF11 · [Repo](https://github.com/bytedance-seed/bagel) · [▶️ Demo ↗](https://demo.bagel-ai.org/) · [🌐 Site ↗](https://bagel-ai.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bagel/)</sub>

<a name="chinese-clip"></a>
### #&#8288;50 [chinese-clip](https://github.com/ofa-sys/chinese-clip) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: niche (3) · Freshness: recent (55) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Mar 2026</sub>

**Chinese-language CLIP models for image-text embedding and cross-modal retrieval.**

Chinese-CLIP provides CLIP models trained on about 200M Chinese image-text pairs, in five sizes from RN50 (77M parameters) to ViT-H/14 (958M). It offers a Python API for image and text features and similarity, plus scripts for finetuning, feature extraction, KNN retrieval and zero-shot classification. Code is built on open_clip.

- **+** Five model sizes, RN50 to ViT-H/14, on Hugging Face and ModelScope
- **+** Reports zero-shot and finetuned results on MUGE, Flickr30K-CN and COCO-CN
- **+** Finetune options include FlashAttention, gradient accumulation, FLIP masking and gradient checkpointing
- **+** ONNX, TensorRT and Core ML conversion scripts for deployment
- **−** Datasets must be converted to base64 TSV, JSONL and LMDB before training
- **−** Feature extraction script supports a single GPU only
- **−** No packaged retrieval server; the demo relies on external clip-retrieval
- **−** Stated requirements list CUDA 10.2 or later; no Docker image

<sub>GPU optional · Needs PyTorch >= 1.8.0, torchvision >= 0.9.0, modelscope (optional, for model download) · Models: ViT-B/16, ViT-L/14, ViT-L/14-336, ViT-H/14, RN50 · [Repo](https://github.com/ofa-sys/chinese-clip) · [▶️ Demo ↗](https://www.modelscope.cn/studios/damo/chinese_clip_applications/summary) · [📖 Docs ↗](https://arxiv.org/abs/2211.01335) · [🌐 Site ↗](https://qwenlm.github.io/zh/blog/chinese-clip/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chinese-clip/)</sub>

<a name="qwen-image"></a>
### #&#8288;51 [qwen-image](https://github.com/qwenlm/qwen-image) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (20) · Freshness: slowing (37) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · Apache-2.0 · Feb 2026</sub>

**20B MMDiT image generation and editing model with strong text rendering.**

Qwen-Image is a 20B MMDiT image foundation model from the Qwen team, covering text-to-image, single and multi-image editing, and layered output. The repo holds diffusers quick-start code, prompt-enhancement helpers that call DashScope, and a Gradio demo server that spreads work across multiple GPUs. Weights are on Hugging Face and ModelScope.

- **+** Text-to-image and editing variants (2512, Edit-2511, Layered) published as open weights
- **+** Strong text rendering, with Chinese called out specifically
- **+** Runs through diffusers pipelines; ComfyUI, vLLM-Omni and SGLang-Diffusion support noted
- **+** Gradio server with multi-GPU workers and a task queue, set by env vars
- **−** VRAM and RAM requirements for a 20B model are not stated in the README
- **−** Needs diffusers installed from git main and transformers>=4.51.3
- **−** Prompt enhancement needs a DashScope API key, an external paid service
- **−** Qwen-Image-2.0 is announced for Qwen Chat; README does not link open weights

<sub>GPU optional · Needs diffusers, transformers>=4.51.3, PyTorch, DashScope API (optional, prompt enhancement) · Models: Qwen-Image, Qwen-Image-2512, Qwen-Image-Edit, Qwen-Image-Edit-2509, Qwen-Image-Edit-2511 · [Repo](https://github.com/qwenlm/qwen-image) · [▶️ Demo ↗](https://huggingface.co/spaces/Qwen/Qwen-Image) · [📖 Docs ↗](https://arxiv.org/abs/2508.02324) · [🌐 Site ↗](https://qwenlm.github.io/blog/qwen-image/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwen-image/)</sub>

<a name="chinese-llama-alpaca-2"></a>
### #&#8288;52 [chinese-llama-alpaca-2](https://github.com/ymcui/chinese-llama-alpaca-2) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (12) · Freshness: slowing (43) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Apr 2026</sub>

**Llama-2 models with extended Chinese vocabulary, plus training scripts.**

Releases Chinese-LLaMA-2 base and Chinese-Alpaca-2 instruction models (1.3B, 7B, 13B) built on Llama-2, with a 55,296-token Chinese vocabulary and incremental pretraining on 120 GB of Chinese text. Long-context variants reach 16K (PI) and 64K (YaRN), and RLHF versions exist for 1.3B and 7B. Includes pretraining and fine-tuning scripts and guides for llama.cpp, transformers, vLLM and LangChain.

- **+** Full, LoRA, GGUF and AWQ weights published on Hugging Face and ModelScope
- **+** Context options of 4K, 16K and 64K, with NTK extension beyond that
- **+** Pretraining and instruction-tuning scripts included, with FlashAttention-2 support
- **+** Documented paths for llama.cpp, transformers, vLLM, text-generation-webui and LangChain
- **−** Superseded: README recommends upgrading to the Llama-3-based Chinese-LLaMA-Alpaca-3
- **−** Last release was 2024-01-23 (v4.1)
- **−** LoRA weights cannot be used alone and must be merged with original Llama-2
- **−** Vocabulary differs from first-generation models, so the two cannot be mixed

<sub>GPU optional · Needs Llama-2 base weights (for LoRA merge), transformers, llama.cpp · Models: Chinese-LLaMA-2, Chinese-Alpaca-2, GGUF, AWQ, LoRA · [Repo](https://github.com/ymcui/chinese-llama-alpaca-2) · [▶️ Demo ↗](http://llm-arena.ymcui.com/) · [📖 Docs ↗](https://github.com/ymcui/Chinese-LLaMA-Alpaca-2/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chinese-llama-alpaca-2/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
