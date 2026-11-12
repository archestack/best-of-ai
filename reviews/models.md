# 🧬 Open models reviews · Best of Open-Source AI

Repositories of open-weight models with the code to run them: LLMs, vision, speech and embedding models. Back to the [leaderboard](../README.md#-open-models).

<sub>🌐 Also on the web: [Open models on archestack.com](https://archestack.com/best-of-ai/models/), each project on its own page.</sub>

<a name="ruview"></a>
### 🥇 [ruview](https://github.com/ruvnet/ruview) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 104k · MIT · Nov 2026</sub>

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

<a name="laya"></a>
### 🥈 [laya](https://github.com/nandhakishorm/laya) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Nov 2026</sub>

**Single-pass multilingual classifier returning typed decisions with calibrated odds.**

Laya answers structured questions (choice, score, yes/no) about text in one non-autoregressive forward pass, using ModernBERT-based checkpoints of about 150M to 421M parameters, or a 0.8B reader via the vegaml option. Each answer carries probabilities, a conformal prediction set, an abstain flag and an auto/review route. It can fit small heads and calibrate on your own labels (35 rows minimum in the example) without changing the base model.

- **+** Answers carry conformal prediction sets, abstain and out-of-distribution flags, and a route field
- **+** Reports 33 ms per decision on a T4 with the English checkpoint
- **+** Covers 100+ languages; vegaml mode takes images, audio, video and 73,728-token documents
- **+** Fits heads on your labels in seconds without gradient updates to the reader
- **−** Returns typed decisions only; it does not generate free text
- **−** In the 40-row fit example, all 20 held-out rows routed to review
- **−** Long-document accuracy on laya-multilingual varies beyond about 4,000 tokens
- **−** Base English checkpoint scored 0.362 on typed-decisions; fine-tuning needed for domain accuracy

<sub>GPU optional · Docker + Compose · Needs PyTorch, Hugging Face Hub, ffmpeg (video input) · Models: laya (English), laya-multilingual, laya-typed-decisions, vega-U 0.8B, Qwen3.5-4B reader · [Repo](https://github.com/nandhakishorm/laya) · [▶️ Demo ↗](https://huggingface.co/spaces/convaiinnovations/laya-demo) · [📖 Docs ↗](https://nandhakishorm.github.io/laya/) · [🌐 Site ↗](https://huggingface.co/convaiinnovations/laya) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/laya/)</sub>

<a name="rf-detr"></a>
### 🥉 [rf-detr](https://github.com/roboflow/rf-detr) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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

<a name="timesfm"></a>
### #&#8288;4 [timesfm](https://github.com/google-research/timesfm) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Sep 2026</sub>

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

<a name="open-clip"></a>
### #&#8288;5 [open_clip](https://github.com/mlfoundations/open_clip) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · custom license · Nov 2026</sub>

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

<a name="yue"></a>
### #&#8288;6 [yue](https://github.com/multimodal-art-projection/yue) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

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

<a name="yolov5"></a>
### #&#8288;7 [yolov5](https://github.com/ultralytics/yolov5) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (96) · Freshness: recent (70) · Maintenance: fair (63) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · AGPL-3.0 · Nov 2026</sub>

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

<a name="speech"></a>
### #&#8288;8 [speech](https://github.com/nvidia-nemo/speech) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: patchy (42) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Nov 2026</sub>

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

<a name="kev"></a>
### #&#8288;9 [kev](https://github.com/jaredpalmer/kev) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10.0k · Apache-2.0 · Oct 2026</sub>

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

<a name="ace-step-1-5"></a>
### #&#8288;10 [ace-step-1.5](https://github.com/ace-step/ace-step-1.5) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Aug 2026</sub>

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

<a name="cosmos"></a>
### #&#8288;11 [cosmos](https://github.com/nvidia/cosmos) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · custom license · Nov 2026</sub>

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

<a name="flagembedding"></a>
### #&#8288;12 [flagembedding](https://github.com/flagopen/flagembedding) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Oct 2026</sub>

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

<a name="unlimited-ocr"></a>
### #&#8288;13 [unlimited-ocr](https://github.com/baidu/unlimited-ocr) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: patchy (31) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Nov 2026</sub>

**OCR model that parses long documents and multi-page PDFs in one pass.**

Unlimited-OCR is a Baidu document-parsing vision-language model, building on DeepSeek-OCR, with weights on Hugging Face. The repo ships inference code for Transformers, vLLM and SGLang, the last exposing an OpenAI-compatible chat API. It handles single images and multi-page input, with PDFs converted to images first.

- **+** Multi-page parsing in one request, with 32768 max context length in the examples
- **+** Three inference paths: Transformers, vLLM (Docker images), and SGLang with OpenAI-compatible API
- **+** infer.py batch script launches SGLang and sends concurrent requests for image dirs or PDFs
- **+** MIT license; training supported through ms-swift
- **−** Requires an NVIDIA GPU; examples tested only on CUDA 12.9 with Python 3.12
- **−** PDFs must be rasterized to images with PyMuPDF before parsing
- **−** SGLang setup needs a bundled dev wheel and custom logit processor flags

<sub>GPU required · Needs PyTorch 2.10.0, transformers 4.57.1, PyMuPDF, vLLM or SGLang (optional) · Models: baidu/Unlimited-OCR (safetensors) · port 10000 · [Repo](https://github.com/baidu/unlimited-ocr) · [▶️ Demo ↗](https://huggingface.co/spaces/baidu/Unlimited-OCR) · [📖 Docs ↗](https://recipes.vllm.ai/baidu/Unlimited-OCR) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unlimited-ocr/)</sub>

<a name="alphafold3"></a>
### #&#8288;14 [alphafold3](https://github.com/google-deepmind/alphafold3) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.8k · Apache-2.0 · Nov 2026</sub>

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

<a name="insightface"></a>
### #&#8288;15 [insightface](https://github.com/deepinsight/insightface) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 30k · no license · Oct 2026</sub>

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

<a name="minicpm"></a>
### #&#8288;16 [minicpm](https://github.com/openbmb/minicpm) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;17 [yolov3](https://github.com/ultralytics/yolov3) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (58) · Freshness: recent (70) · Maintenance: fair (63) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · AGPL-3.0 · Nov 2026</sub>

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

<a name="lingbot-map"></a>
### #&#8288;18 [lingbot-map](https://github.com/robbyant/lingbot-map) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: weak (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Oct 2026</sub>

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

<a name="minicpm-v"></a>
### #&#8288;19 [minicpm-v](https://github.com/openbmb/minicpm-v) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: widely used (85) · Freshness: recent (71) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · Apache-2.0 · Nov 2026</sub>

**Open-weight multimodal models for image, video, document and speech understanding.**

Repository for the MiniCPM-V 4.7 vision-language models (35B-A3B MoE and 1B) and MiniCPM-o 4.5, a 9B omnimodal model with full-duplex video, audio and speech output. It provides weights, inference and fine-tuning docs, and on-device deployment paths for iOS, Android and HarmonyOS. Code and weights are Apache-2.0.

- **+** Two size classes: 1B and 35B-A3B MoE for vision, plus a 9B omnimodal model
- **+** README reports 13+ tokens/s with 3 GB memory for 35B-A3B on iPhone 17 Pro Max
- **+** Covers iOS, Android, HarmonyOS and Intel, AMD, Arm, Rockchip and Houmo chips
- **+** Apache-2.0 for code and weights; fine-tuning via LLaMA-Factory and SWIFT, plus SRFT
- **−** No Docker or compose files; setup follows per-model docs
- **−** Last tagged release is 2025-05-27, while model updates are announced in the README
- **−** Benchmark claims are the authors' own, shown as images

<sub>RAM ≥ 3 GB · GPU optional · Needs Hugging Face Transformers, llama.cpp-omni, Ollama · Models: MiniCPM-V 4.7 35B-A3B, MiniCPM-V 4.7 1B, MiniCPM-o 4.5 9B, GGUF, BF16 · [Repo](https://github.com/openbmb/minicpm-v) · [▶️ Demo ↗](https://huggingface.co/spaces/openbmb/MiniCPM-V-4.7-Demo) · [📖 Docs ↗](https://minicpm-o.readthedocs.io/en/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/minicpm-v/)</sub>

<a name="sensenova-u1"></a>
### #&#8288;20 [sensenova-u1](https://github.com/opensensenova/sensenova-u1) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Nov 2026</sub>

**Open 8B multimodal model for image generation, editing and visual Q&A.**

SenseNova-U1 and U1.5 are open-weight native multimodal models (8B-MoT, plus an A3B variant) that handle text-to-image, image editing, interleaved image-text generation and visual question answering in one model. The repo ships Python inference scripts for Transformers, optional GGUF checkpoint loading, 8-step LoRA checkpoints, a ComfyUI workflow and full-parameter fine-tuning code. Production serving is documented separately with LightLLM and LightX2V.

- **+** One checkpoint covers text-to-image, editing, interleaved generation and VQA
- **+** Native 4K generation and bounding-box or reference-based visual control in U1.5
- **+** 8-step LoRA and GGUF checkpoints reduce latency and VRAM use
- **+** Training code, technical reports and a ComfyUI workflow are included
- **−** README admits dense text, hands, small faces and multi-turn edits can still fail
- **−** Official GGUF weights for U1.5 are not out yet; current GGUFs are community-made
- **−** No tagged release; weights are distributed via Hugging Face and ModelScope

<sub>Needs PyTorch, Transformers, LightLLM (production serving), LightX2V (production serving), gguf and diffusers (optional GGUF) · Models: SenseNova-U1.5-8B-MoT, SenseNova-U1-8B-MoT, SenseNova-U1-A3B-MoT, safetensors LoRA, GGUF Q8 · [Repo](https://github.com/opensensenova/sensenova-u1) · [▶️ Demo ↗](https://unify.light-ai.top/) · [📖 Docs ↗](https://github.com/OpenSenseNova/SenseNova-U1/blob/main/docs/deployment.md) · [🌐 Site ↗](https://huggingface.co/blog/sensenova/neo-unify) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sensenova-u1/)</sub>

<a name="glm-5"></a>
### #&#8288;21 [glm-5](https://github.com/zai-org/glm-5) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: known (45) · Freshness: active (100) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Oct 2026</sub>

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

<a name="trellis"></a>
### #&#8288;22 [trellis](https://github.com/microsoft/trellis) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

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

<a name="chronos-forecasting"></a>
### #&#8288;23 [chronos-forecasting](https://github.com/amazon-science/chronos-forecasting) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (39) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Oct 2026</sub>

**Pretrained zero-shot time series forecasting models with a Python pipeline.**

Python package that loads the Chronos family of pretrained time series models (Chronos-2, Chronos-Bolt, original T5-based Chronos) from Hugging Face and produces probabilistic quantile forecasts. Chronos-2 handles univariate, multivariate and covariate-informed forecasting zero-shot and takes pandas DataFrames through predict_df. Model sizes range from 8M to 710M parameters.

- **+** Zero-shot forecasting with covariates and multivariate series in Chronos-2 (120M parameters)
- **+** Size range of 8M to 710M parameters across three model generations
- **+** DataFrame-based predict_df API returns quantile forecasts; installs with pip
- **+** Apache-2.0, with notebooks and AWS deployment guides (SageMaker JumpStart, AutoGluon-Cloud)
- **−** README gives no RAM or VRAM requirements
- **−** Production deployment guidance centers on AWS
- **−** No hosted demo; quick start runs in Colab or SageMaker Studio Lab notebooks

<sub>GPU optional · Needs Hugging Face model hub, pandas[pyarrow] · Models: Chronos-2, Chronos-Bolt, Chronos-T5 · [Repo](https://github.com/amazon-science/chronos-forecasting) · [📖 Docs ↗](https://auto.gluon.ai/cloud/stable/tutorials/foundation-model-timeseries.html) · [🌐 Site ↗](https://huggingface.co/collections/amazon/chronos-models-65f1791d630a8d57cb718444) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chronos-forecasting/)</sub>

<a name="gpt-oss"></a>
### #&#8288;24 [gpt-oss](https://github.com/openai/gpt-oss) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (80) · Freshness: active (90) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;25 [mamba](https://github.com/state-spaces/mamba) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (78) · Freshness: active (94) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Jul 2026</sub>

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

<a name="deepanalyze"></a>
### #&#8288;26 [deepanalyze](https://github.com/ruc-datalab/deepanalyze) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · MIT · Nov 2026</sub>

**8B agentic LLM that runs data science tasks and writes analyst-style reports.**

DeepAnalyze is an 8B model (DeepAnalyze-8B, on Hugging Face and ModelScope) trained to plan, write and execute code for data preparation, analysis, modeling, visualization and report generation. It takes CSV, Excel, JSON, XML, YAML, TXT, Markdown and database sources and produces a research report. The repo includes a vLLM-based Python API, an HTTP API server, two web UIs, a Jupyter UI, a CLI, training code and the 500K-sample training dataset.

- **+** Weights, training data (DataScience-Instruct-500K) and training code are all published
- **+** Handles structured, semi-structured and unstructured inputs in one open-ended run
- **+** README gives vLLM settings per GPU size, including 4-bit and 8-bit variants
- **+** Multiple frontends: web UI, Jupyter, CLI, and a Python API
- **−** No Docker or compose setup for the main demo; needs npm, vLLM and shell scripts
- **−** README labels the demo UI an initial version
- **−** Needs a GPU of 16GB or more for local inference, with reduced context on smaller cards
- **−** Quick-start example uses hardcoded author-specific paths that must be replaced

<sub>GPU required · Docker + Compose · Needs vLLM >=0.8.5, PyTorch, Transformers, Node.js/npm (web UI), Python 3.12 · Models: DeepAnalyze-8B, 4-bit quantized, 8-bit quantized, OpenAI-style API endpoints · port 4000 · [Repo](https://github.com/ruc-datalab/deepanalyze) · [▶️ Demo ↗](https://deepanalyze.net) · [📖 Docs ↗](https://github.com/ruc-datalab/DeepAnalyze/blob/main/docs/DeepAnalyze_API_Key_Usage_Guide.md) · [🌐 Site ↗](https://ruc-deepanalyze.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepanalyze/)</sub>

<a name="open-model-zoo"></a>
### #&#8288;27 [open_model_zoo](https://github.com/openvinotoolkit/open_model_zoo) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (23) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · Apache-2.0 · Oct 2026</sub>

**Pre-trained OpenVINO vision models with demos, downloader and accuracy checker.**

Repository of Intel and public pre-trained deep learning models prepared for OpenVINO inference, plus demo applications showing how to run them. It also ships a Model Downloader and other automation tools, and an Accuracy Checker for validating model accuracy. The README states the project is in maintenance mode as a source of models and points to OpenVINO Jupyter notebooks instead.

- **+** Includes both Intel-trained and public pre-trained model collections with indexed documentation
- **+** Model Downloader tool automates fetching models
- **+** Accuracy Checker validates model accuracy
- **+** Demos show end-to-end inference usage with OpenVINO
- **−** In maintenance mode as a source of models; README redirects to notebooks
- **−** Documentation links point to the 2023.0 OpenVINO docs
- **−** No tagged release published
- **−** Tied to the OpenVINO runtime; not a general-purpose model hub

<sub>Needs OpenVINO Toolkit · Models: OpenVINO · [Repo](https://github.com/openvinotoolkit/open_model_zoo) · [📖 Docs ↗](https://docs.openvino.ai/2023.0/model_zoo.html) · [🌐 Site ↗](https://docs.openvino.ai/2023.0/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-model-zoo/)</sub>

<a name="ailia-models"></a>
### #&#8288;28 [ailia-models](https://github.com/ailia-ai/ailia-models) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · custom license · Nov 2026</sub>

**427 pre-trained vision, audio and NLP models with runnable ailia scripts.**

A repository of per-model sample scripts for 427 pre-trained models covering detection, segmentation, depth estimation, speech recognition, text to speech, diffusion, embeddings and more. Each script downloads its weights automatically and runs through the ailia inference SDK installed from PyPI. It targets Python 3.9 to 3.12 on Windows, macOS, Linux, iOS, Android, Jetson and Raspberry Pi.

- **+** Every model runs the same way: no arguments, weights download automatically
- **+** Wide coverage across vision, audio, diffusion, NLP and embeddings in one repo
- **+** Lists mobile and edge targets such as Jetson and Raspberry Pi
- **+** Includes recent models such as Qwen3-TTS, SAM 3.1 and Depth Anything v3
- **−** Requires the ailia SDK, a separate runtime from the sample scripts
- **−** License is reported as NOASSERTION, so terms are unclear from repo metadata
- **−** No release tags, so versions are tied to commits
- **−** Standalone per-model scripts, not a served API or unified library

<sub>Needs ailia (PyPI), Python 3.9-3.12 · [Repo](https://github.com/ailia-ai/ailia-models) · [▶️ Demo ↗](https://www.ailia.ai/launch_to_colab) · [📖 Docs ↗](https://docs.ailia.ai/en/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ailia-models/)</sub>

<a name="moss"></a>
### #&#8288;29 [moss](https://github.com/openmoss/moss) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Sep 2026</sub>

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

<a name="moss-tts"></a>
### #&#8288;30 [moss-tts](https://github.com/openmoss/moss-tts) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (22) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Sep 2026</sub>

**Open-weight TTS model family for cloning, dialogue, realtime speech and sound effects.**

MOSS-TTS is a family of open-weight speech and sound generation models from MOSI.AI and OpenMOSS, built on the MossTTSDelay, MossTTSLocal and MossTTSRealtime architectures. It covers long-form multilingual TTS with voice cloning (31 languages in v1.5), multi-speaker dialogue, voice design from text prompts, realtime synthesis at 180 ms TTFB, and sound effects. The repo has inference code, fine-tuning tutorials, and llama.cpp/ONNX, SGLang-Omni and vLLM-Omni backends.

- **+** Covers cloning, dialogue, voice design, realtime and sound effects, from ~100M to 8B parameters
- **+** Torch-free path via llama.cpp GGUF weights plus ONNX codec; 8B fits on 8 GB GPUs
- **+** Serving via SGLang-Omni (OpenAI-compatible /v1/audio/speech), vLLM-Omni and mlx-audio
- **+** Fine-tuning tutorials for the Delay, Local and Realtime architectures
- **−** Separate checkpoints on different architectures; no single unified entry point
- **−** 8B flagship models need a sizable GPU; CPU use means the separate MOSS-TTS-Nano
- **−** No release tags and no Docker or compose files in the repo
- **−** Several components live in other repos (TTSD, Nano, llama.cpp fork, tokenizer)

<sub>GPU optional · Needs PyTorch, Hugging Face Transformers, FlashAttention 2 (optional), llama.cpp (optional), ONNX Runtime (optional) · Models: MOSS-TTS-v1.5 (8B), MOSS-TTS-Local-Transformer-v1.5 (4B), MOSS-TTSD-v1.0, MOSS-VoiceGenerator, MOSS-TTS-Realtime · [Repo](https://github.com/openmoss/moss-tts) · [▶️ Demo ↗](https://huggingface.co/spaces/OpenMOSS-Team/MOSS-TTS) · [📖 Docs ↗](https://studio.mosi.cn/docs/moss-tts) · [🌐 Site ↗](https://mosi.cn/#models) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moss-tts/)</sub>

<a name="spleeter"></a>
### #&#8288;31 [spleeter](https://github.com/deezer/spleeter) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: widely used (87) · Freshness: recent (70) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Oct 2026</sub>

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

<a name="unilm"></a>
### #&#8288;32 [unilm](https://github.com/microsoft/unilm) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: widely used (82) · Freshness: recent (70) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Sep 2026</sub>

**Microsoft research code and weights for pre-trained text, vision, speech and document AI.**

A monorepo of Microsoft Research projects on large-scale self-supervised pre-training across languages, vision, speech and multimodal tasks. Each subdirectory holds code and checkpoints for a separate model family, including UniLM, MiniLM, BEiT, LayoutLM, WavLM, TrOCR, VALL-E, Kosmos and E5. It is a research collection, not a single installable tool.

- **+** Covers text, vision, speech and document models in one repo, from UniLM to Kosmos-2.5
- **+** Document AI line (LayoutLM v1-v3, LayoutXLM, DiT, TrOCR) has pretrained models and code
- **+** MIT license
- **+** Some models have hosted demos, such as TextDiffuser-2 and DiT on Hugging Face Spaces
- **−** Not one library: each subfolder has its own setup, dependencies and README
- **−** Last tagged release is May 2024, and most listed model releases date from 2021-2023
- **−** Top-level README is a news and paper index with little install or usage guidance

<sub>Models: PyTorch, Hugging Face Transformers · [Repo](https://github.com/microsoft/unilm) · [▶️ Demo ↗](https://huggingface.co/spaces/JingyeChen22/TextDiffuser-2) · [🌐 Site ↗](https://aka.ms/GeneralAI) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unilm/)</sub>

<a name="glm-v"></a>
### #&#8288;33 [glm-v](https://github.com/zai-org/glm-v) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · Apache-2.0 · Nov 2026</sub>

**Open-weight GLM-4.6V, 4.5V and 4.1V vision-language models with examples.**

Repository for Zhipu/Z.ai's GLM-4.6V, GLM-4.5V and GLM-4.1V vision-language models, linking weights on Hugging Face and ModelScope (including FP8 and GGUF variants). It adds example code for GUI agents, a desktop chat helper, a VLM reward system, and LLaMA-Factory fine-tuning notes. The maintainers state the repo is no longer maintained as of 2026/09/02.

- **+** Covers 106B GLM-4.6V, 9B GLM-4.6V-Flash and 9B GLM-4.1V-9B-Thinking checkpoints
- **+** GLM-4.6V offers native multimodal function calling and 128K context
- **+** Serving supported in SGLang, vLLM and Transformers; GGUF and FP8 weights available
- **+** Includes bounding-box grounding, GUI agent examples and Midscene.js demos
- **−** Repository declared unmaintained as of 2026/09/02; newer work moved to the GLM-5 repo
- **−** No tagged releases; weights live on external hosts
- **−** Known issues: repetitive thinking, weak text-only QA, counting errors

<sub>Needs SGLang, vLLM, Transformers, LLaMA-Factory · Models: GLM-4.6V, GLM-4.6V-FP8, GLM-4.6V-Flash, GLM-4.5V, GLM-4.5V-FP8 · [Repo](https://github.com/zai-org/glm-v) · [▶️ Demo ↗](https://huggingface.co/spaces/zai-org/GLM-4.5V-Demo-App) · [📖 Docs ↗](https://arxiv.org/abs/2507.01006) · [🌐 Site ↗](https://z.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/glm-v/)</sub>

<a name="rwkv-lm"></a>
### #&#8288;34 [rwkv-lm](https://github.com/blinkdl/rwkv-lm) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (71) · Freshness: recent (70) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Nov 2026</sub>

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

<a name="weathernext"></a>
### #&#8288;35 [weathernext](https://github.com/google-deepmind/weathernext) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (46) · Freshness: active (100) · Maintenance: weak (18) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · Apache-2.0 · Sep 2026</sub>

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

<a name="onnx-models"></a>
### #&#8288;36 [models](https://github.com/onnx/models) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · Apache-2.0 · Oct 2026</sub>

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

<a name="lingbot-world"></a>
### #&#8288;37 [lingbot-world](https://github.com/robbyant/lingbot-world) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (25) · Freshness: active (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · Apache-2.0 · Jul 2026</sub>

**Image-to-video world model with camera or action control, built on Wan2.2.**

LingBot-World generates interactive video from an input image and text prompt, steered by camera poses or action inputs, with minute-level horizons. Weights are released for Base (Cam), Base (Act) and Fast variants at 480P and 720P, run through torchrun scripts on top of Wan2.2. The README states this repository is no longer maintained and points to lingbot-world-v2.

- **+** Three open-weight variants: Base (Cam), Base (Act) and Fast, at 480P and 720P
- **+** Fast variant uses chunked causal inference with KV caching; README claims under 1 s latency at 16 FPS
- **+** Camera control accepts poses.npy and intrinsics.npy, which can be estimated from video with ViPE
- **+** Community 4-bit NF4 quantized checkpoint exists for limited GPU memory, inference only
- **−** Repository is marked no longer maintained; development moved to lingbot-world-v2
- **−** Reference commands assume 8 GPUs with FSDP and Ulysses parallelism
- **−** Setup defers to Wan2.2 docs and needs flash-attn built from source
- **−** Quantized variant shows minor loss in visual fidelity and temporal consistency

<sub>GPU required · Needs PyTorch >= 2.4.0, flash-attn, Wan2.2 codebase, ViPE (optional, for camera poses) · Models: LingBot-World-Base (Cam), LingBot-World-Base (Act), LingBot-World-Fast, NF4 4-bit quantized Base (Cam), community · [Repo](https://github.com/robbyant/lingbot-world) · [▶️ Demo ↗](https://www.reactor.inc/) · [🌐 Site ↗](https://technology.robbyant.com/lingbot-world) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lingbot-world/)</sub>

<a name="omniparser"></a>
### #&#8288;38 [omniparser](https://github.com/microsoft/omniparser) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: widely used (84) · Freshness: recent (73) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · CC-BY-4.0 · Jul 2026</sub>

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

<a name="kronos"></a>
### #&#8288;39 [kronos](https://github.com/shiyu-coder/kronos) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: widely used (95) · Freshness: recent (55) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · MIT · Apr 2026</sub>

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

<a name="qwen"></a>
### #&#8288;40 [qwen](https://github.com/qwenlm/qwen) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: widely used (81) · Freshness: slowing (41) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Mar 2026</sub>

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

<a name="trellis-2"></a>
### #&#8288;41 [trellis.2](https://github.com/microsoft/trellis.2) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (65) · Freshness: recent (75) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Jun 2026</sub>

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

<a name="chinese-bert-wwm"></a>
### #&#8288;42 [chinese-bert-wwm](https://github.com/ymcui/chinese-bert-wwm) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (57) · Freshness: recent (57) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Apr 2026</sub>

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

<a name="pinto-model-zoo"></a>
### #&#8288;43 [pinto_model_zoo](https://github.com/pinto0309/pinto_model_zoo) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (26) · Freshness: recent (70) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · MIT · Oct 2026</sub>

**Pre-converted vision models across TFLite, ONNX, OpenVINO, CoreML and more.**

A repository of models converted between frameworks, mostly image classification and other vision models such as face, person re-identification, gaze and attribute recognition. Formats include TensorFlow, TFLite (FP32/FP16/INT8), EdgeTPU, OpenVINO IR, CoreML, TF.js, TF-TRT and ONNX. The README links to the author's conversion tools, such as onnx2tf, and ONNX processing utilities.

- **+** Same model offered in many formats: TFLite, EdgeTPU, OpenVINO, CoreML, TF.js, TF-TRT, ONNX
- **+** Table lists per-model quantization variants (FP16, INT8, dynamic range, weight) and input sizes
- **+** Links to the author's conversion tools like onnx2tf and ONNX editing utilities
- **+** Edge-oriented models, including EdgeTPU and Raspberry Pi targets
- **−** Each model folder has its own license; source model terms apply, not MIT
- **−** Author states sample code to verify operation is largely skipped
- **−** Last release is 2023-11-30; repo has no tagged releases since
- **−** Early notes say MobileNetV3 and full integer quantization models do not return correctly

<sub>Models: TensorFlow, TFLite, EdgeTPU, OpenVINO, CoreML · [Repo](https://github.com/pinto0309/pinto_model_zoo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pinto-model-zoo/)</sub>

<a name="evo2"></a>
### #&#8288;44 [evo2](https://github.com/arcinstitute/evo2) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (21) · Freshness: recent (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Jun 2026</sub>

**DNA language model for scoring, embedding and generating sequences up to 1M bp.**

Evo 2 is a DNA language model trained on OpenGenome2 (8.8 trillion tokens across all domains of life) using the StripedHyena 2 architecture at single-nucleotide resolution. This repo runs inference through Vortex: scoring sequence likelihoods, extracting intermediate-layer embeddings and generating DNA from prompts, with checkpoints from 1B to 40B parameters on HuggingFace. Example notebooks cover BRCA1 variant effect prediction, exon classification and sparse autoencoder features.

- **+** Context up to 1M base pairs on the 7B, 20B and 40B checkpoints
- **+** 7B models run in bfloat16 without Transformer Engine or FP8 hardware
- **+** Notebooks for BRCA1 zero-shot variant scoring, exon classification, generation and SAE features
- **+** Open training data (OpenGenome2) and training path via Savanna or BioNeMo
- **−** 20B, 40B and 1B models need FP8 via Transformer Engine on Hopper GPUs
- **−** 40B model needs multiple H100 GPUs
- **−** Linux only officially; WSL2 limited, requires CUDA 12.1+ and Flash Attention build
- **−** Forward passes on very long sequences may be slow in Vortex

<sub>GPU required · Docker · Needs Vortex, PyTorch, Flash Attention 2.8.0.post2, Transformer Engine 2.3.0 (20B, 40B, 1B), CUDA 12.1+, cuDNN 9.3+ · Models: evo2_40b, evo2_20b, evo2_7b, evo2_40b_base, evo2_7b_base · [Repo](https://github.com/arcinstitute/evo2) · [▶️ Demo ↗](https://build.nvidia.com/arc/evo2-40b) · [📖 Docs ↗](https://docs.nvidia.com/nim/bionemo/evo2/latest/overview.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/evo2/)</sub>

<a name="clip"></a>
### #&#8288;45 [clip](https://github.com/openai/clip) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: widely used (90) · Freshness: slowing (48) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · MIT · Mar 2026</sub>

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

<a name="d-fine"></a>
### #&#8288;46 [d-fine](https://github.com/peterande/d-fine) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · Apache-2.0 · Aug 2026</sub>

**Real-time DETR object detector with COCO and Objects365 checkpoints.**

Official PyTorch implementation of D-FINE, a real-time DETR-style object detector that treats box regression as fine-grained distribution refinement with self-distillation. It ships five sizes (N to X, 4M to 62M parameters) with training, testing and fine-tuning configs for COCO, Objects365 and custom COCO-format datasets. The N model reports 42.8 AP on COCO and the X model 55.8 AP, or 59.3 AP with Objects365 pretraining.

- **+** Five model sizes, N to X, with COCO AP from 42.8 to 55.8
- **+** Latency listed per model on a T4 with TensorRT 10.4.0, fp16
- **+** Configs and commands for fine-tuning on custom COCO-format datasets
- **+** Checkpoints and training logs published for every listed model
- **−** Objects365-trained checkpoints may not be cleared for commercial use
- **−** Training commands assume a 4-GPU torchrun setup
- **−** Object detection only, no segmentation or language features
- **−** Objects365 data prep needs several manual remap and resize steps

<sub>GPU required · Docker · Needs PyTorch, conda, Python 3.11.9, TensorRT (for latency benchmarks) · Models: D-FINE N/S/M/L/X (HGNetv2), COCO, Objects365, custom COCO-format datasets · [Repo](https://github.com/peterande/d-fine) · [▶️ Demo ↗](https://huggingface.co/spaces/developer0hye/D-FINE) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/d-fine/)</sub>

<a name="deepresearch"></a>
### #&#8288;47 [deepresearch](https://github.com/alibaba-nlp/deepresearch) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (79) · Freshness: slowing (39) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Feb 2026</sub>

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

<a name="hunyuan3d-1"></a>
### #&#8288;48 [hunyuan3d-1](https://github.com/tencent-hunyuan/hunyuan3d-1) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · custom license · Nov 2026</sub>

**Text-to-3D and image-to-3D mesh generation from multi-view diffusion.**

Hunyuan3D-1.0 generates textured 3D meshes from a text prompt or a single image. It runs a multi-view diffusion model, then a sparse-view reconstruction model, with Hunyuan-DiT handling text-to-image. Lite and standard variants ship with a CLI and a Gradio demo; the README cites about 10 s (lite) and 25 s (standard) per mesh.

- **+** Accepts text or image input, with bilingual Chinese and English prompts
- **+** Lite and standard variants; split-module scripts fit 10-16 GB GPUs
- **+** Includes CLI, Gradio demo, texture mapping and optional texture baking
- **+** Checkpoints on Hugging Face plus a hosted demo space
- **−** Needs 30 GB VRAM for standard, 22 GB for lite; --save_memory slows inference
- **−** Heavy install: CUDA 12.1 PyTorch, pytorch3d, nvdiffrast and a dust3r checkout
- **−** Baking depends on DUSt3R under CC BY-NC-SA 4.0, so non-commercial only
- **−** Gradio demo has no auth; pinned torch 2.6.0 has a known CVE

<sub>GPU required · Needs PyTorch (CUDA 12.1), pytorch3d, nvdiffrast, DUSt3R, Hunyuan-DiT weights, huggingface-cli · Models: Hunyuan3D-1 lite, Hunyuan3D-1 std, Hunyuan3D-1 svrm, HunyuanDiT-v1.1-Diffusers-Distilled · port 8080 · [Repo](https://github.com/tencent-hunyuan/hunyuan3d-1) · [▶️ Demo ↗](https://huggingface.co/spaces/Tencent/Hunyuan3D-1) · [🌐 Site ↗](http://3d-models.hunyuan.tencent.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hunyuan3d-1/)</sub>

<a name="nba-machine-learning-sports-betting"></a>
### #&#8288;49 [nba-machine-learning-sports-betting](https://github.com/kyleskom/nba-machine-learning-sports-betting) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 1.8k · no license · Nov 2026</sub>

**NBA game winner and over/under predictor using XGBoost and neural nets.**

Predicts NBA moneyline and totals outcomes from team stats (2007-08 onward) and sportsbook odds scraped from SBR, storing data in SQLite. It trains XGBoost, neural network and logistic regression models, then prints win probabilities, expected value and optional Kelly Criterion stake sizing for today's games. A small Flask app browses outputs.

- **+** Full pipeline in one repo: data pull, feature build, training and daily prediction
- **+** Fetches live odds from seven named sportsbooks, with manual odds entry as fallback
- **+** Outputs expected value and Kelly Criterion fractions, not just win probabilities
- **+** Backfill flags fill missing stats and odds by date or season
- **−** No license file, so reuse terms are unclear
- **−** NN training scripts use hard-coded dataset and model paths
- **−** Depends on scraped NBA endpoints and SBR odds, which can change or break
- **−** No Docker setup; requires Python 3.11 with TensorFlow installed manually

<sub>Needs Python 3.11, TensorFlow, XGBoost, SQLite, Flask, NBA stats endpoints, SBR odds data · Models: XGBoost, TensorFlow neural network, Logistic regression · [Repo](https://github.com/kyleskom/nba-machine-learning-sports-betting) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nba-machine-learning-sports-betting/)</sub>

<a name="sketch-code"></a>
### #&#8288;50 [sketch-code](https://github.com/ashnkumar/sketch-code) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: known (32) · Freshness: active (97) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · MIT · Aug 2026</sub>

**CNN-LSTM model that turns hand-drawn wireframe images into HTML.**

SketchCode is a 2018 proof-of-concept that treats HTML as the caption of a wireframe image, using a CNN encoder and LSTM decoder trained on a 1,700-image synthetic dataset derived from pix2code. The repo has Python scripts to convert single images or folders to HTML, train from scratch or from pretrained weights, and score output with BLEU. The README says the code targets TensorFlow 1.x and Keras and is no longer maintained.

- **+** Ships pretrained weights and a download script for the 1,700-image dataset (342 MB)
- **+** CLI scripts cover single and batch conversion, training, and BLEU evaluation
- **+** Training can start from scratch or from pretrained weights, with optional Keras augmentation
- **+** MIT licensed, with a linked write-up of the approach
- **−** No longer maintained; targets TensorFlow 1.x and Keras of 2018
- **−** Only works on wireframes resembling the synthetic training set
- **−** No accuracy figures given; evaluation is a BLEU script only
- **−** Portions derive from Apache-2.0 pix2code, adding attribution terms beyond MIT

<sub>Needs Python 3, TensorFlow 1.x, Keras · Models: CNN encoder + LSTM decoder (Keras JSON + H5 weights) · [Repo](https://github.com/ashnkumar/sketch-code) · [📖 Docs ↗](https://medium.com/insight-data/automated-front-end-development-using-deep-learning-3169dd086e82) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sketch-code/)</sub>

<a name="vipe"></a>
### #&#8288;51 [vipe](https://github.com/nv-tlabs/vipe) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · custom license · Nov 2026</sub>

**Estimates camera pose, intrinsics and dense depth from raw video.**

ViPE is a Python pipeline from NVIDIA that estimates camera intrinsics, camera motion and near-metric dense depth from unconstrained video, including wide-angle and 360-degree panorama footage. It installs from PyPI (nvidia-vipe) and runs through a `vipe infer` CLI. Newer pipelines handle long videos with bounded memory (`pose_only_long`) and streaming metric reconstruction with loop closure and point cloud export (`metrictrail`).

- **+** Handles pinhole, wide-angle and 360-degree panorama video in one tool
- **+** `pose_only_long` keeps GPU and CPU memory roughly constant regardless of video length
- **+** Outputs pose, intrinsics and depth per video; MetricTrail adds PLY point cloud export
- **+** Release 1.2.0 reports a 2.7x speed-up from CUDA fused kernels and caching
- **−** Mixed licensing: Apache 2.0 source, but Unik3D is BY-NC-SA 4.0 and MetricTrail weights are noncommercial
- **−** MetricTrail needs custom CUDA kernel builds, a pinned xformers and CUDA 12.8 toolchain
- **−** MetricTrail weights are obtained separately; the Hugging Face release is described as planned
- **−** Loop closure needs external SALAD candidates exported from a separate environment

<sub>GPU required · Needs CUDA 12.8, conda, uv, xformers 0.0.33.post1, PyPose (optional, loop closure), SALAD (optional, loop closure) · Models: MoGe v2 (moge2-l), Depth-Anything 3, DINO-DPVO, DINOv3 ViT-S/16, Unik3D · [Repo](https://github.com/nv-tlabs/vipe) · [📖 Docs ↗](https://nv-tlabs.github.io/vipe/) · [🌐 Site ↗](https://research.nvidia.com/labs/toronto-ai/vipe) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vipe/)</sub>

<a name="moondream"></a>
### #&#8288;52 [moondream](https://github.com/m87-labs/moondream) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (56) · Freshness: recent (58) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Apr 2026</sub>

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

<a name="deimv2"></a>
### #&#8288;53 [deimv2](https://github.com/intellindust-ai-lab/deimv2) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · custom license · Oct 2026</sub>

**Real-time object detector family built on DINOv3 and HGNetv2 backbones.**

DEIMv2 is a PyTorch object detection codebase with eight COCO-trained variants, from Atto (0.5M params, 23.8 AP) to X (50.3M params, 57.8 AP). The S, M, L and X models use DINOv3-derived backbones; the smaller ones use HGNetv2. It includes training, testing and fine-tuning via torchrun, custom COCO-format datasets, ONNX and TensorRT deployment tools, and Hugging Face checkpoints.

- **+** Eight sizes, from Atto at 0.8 GFLOPs to X at 57.8 COCO AP
- **+** S model reaches 50.9 AP with 9.7M params and 5.78 ms latency
- **+** Checkpoints, configs and logs published, plus Hugging Face weights
- **+** Custom datasets supported in COCO format via YAML config
- **−** Custom DEIMv2 License, not a standard OSI license
- **−** Object detection only; pose and segmentation are in EdgeCrafter
- **−** DINOv3 and distilled ViT backbones must be downloaded manually into ckpts/
- **−** No Docker setup; documented training uses multi-GPU torchrun

<sub>GPU required · Needs PyTorch 2.5.1 or 2.4.1, Python 3.11, DINOv3 checkpoints, onnx, onnxsim, TensorRT >= 10.6 for FP16 · Models: DEIMv2 Atto/Femto/Pico/N (HGNetv2), DEIMv2 S/M/L/X (DINOv3), COCO-format datasets, ONNX, TensorRT · [Repo](https://github.com/intellindust-ai-lab/deimv2) · [🌐 Site ↗](https://intellindust-ai-lab.github.io/projects/DEIMv2/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deimv2/)</sub>

<a name="hy-world-2-0"></a>
### #&#8288;54 [hy-world-2.0](https://github.com/tencent-hunyuan/hy-world-2.0) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (13) · Freshness: active (99) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · custom license · Aug 2026</sub>

**Generates and reconstructs 3D worlds (meshes, Gaussian splats) from text, images or video.**

HY-World 2.0 is Tencent Hunyuan's PyTorch code and weights for two jobs: reconstructing 3D from multi-view images or video with WorldMirror 2.0 (~1.2B), and generating navigable 3DGS or mesh worlds from text or one image. Generation chains panorama synthesis (HY-Pano 2.0), trajectory planning, WorldStereo 2.0 expansion and 3DGS training. It includes a Gradio demo for reconstruction.

- **+** Outputs editable 3DGS, meshes and point clouds that can be imported into Blender, Unity or Unreal
- **+** WorldMirror 2.0 predicts depth, normals, cameras, point clouds and 3DGS in one forward pass
- **+** Optional camera and depth priors can be injected to improve reconstruction accuracy
- **+** Diffusers-like Python API, multi-GPU CLI, and Gradio app for reconstruction
- **−** Heavy install: CUDA 12.8, FlashAttention build, custom gsplat, git submodule and navmesh extension
- **−** HY-Pano-2 is ~80B and WorldStereo-2 ~17B, so generation needs large multi-GPU hardware
- **−** World generation is a five-script pipeline, not a single command
- **−** License is not identified (NOASSERTION), so usage terms need manual review

<sub>GPU required · Needs CUDA 12.8, Python 3.11+, PyTorch, FlashAttention, gsplat, recastnavigation · Models: WorldMirror 2.0 (~1.2B), HY-Pano 2.0 (~80B), HY-Pano-2-Qwen LoRA (~425M), WorldStereo 2.0 (~17B), Hugging Face safetensors · [Repo](https://github.com/tencent-hunyuan/hy-world-2.0) · [▶️ Demo ↗](https://3d.hunyuan.tencent.com/sceneTo3D) · [📖 Docs ↗](https://arxiv.org/abs/2604.14268) · [🌐 Site ↗](https://3d-models.hunyuan.tencent.com/world/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hy-world-2-0/)</sub>

<a name="chinese-llama-alpaca"></a>
### #&#8288;55 [chinese-llama-alpaca](https://github.com/ymcui/chinese-llama-alpaca) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: popular (77) · Freshness: slowing (40) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Apr 2026</sub>

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
### #&#8288;56 [wan2.1](https://github.com/wan-video/wan2.1) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: popular (74) · Freshness: slowing (41) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Mar 2026</sub>

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
### #&#8288;57 [alphafold](https://github.com/google-deepmind/alphafold) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: popular (71) · Freshness: slowing (41) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Apr 2026</sub>

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

<a name="huatuo-llama-med-chinese"></a>
### #&#8288;58 [huatuo-llama-med-chinese](https://github.com/scir-hi/huatuo-llama-med-chinese) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: known (30) · Freshness: active (85) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · Apache-2.0 · Jul 2026</sub>

**LoRA-tuned Chinese medical Q&A models on LLaMA, Alpaca, Bloom and Huozi.**

BenTsao (formerly HuaTuo) releases LoRA adapters that instruction-tune 7B base models (LLaMA, Alpaca-Chinese, Bloom, Huozi) for Chinese medical question answering. Training data is about 8,000 Q&A pairs generated with the GPT-3.5 API from the cMeKG knowledge base, plus 1k multi-turn liver cancer samples from literature. The repo includes inference and fine-tuning scripts and a knowledge-tuning method.

- **+** Ships LoRA adapters for four base models, on Hugging Face and Baidu Netdisk
- **+** Includes infer and finetune shell scripts plus the dataset format for custom data
- **+** Documents training cost: one A100 80GB, 10 epochs, about 2h17m, around 40GB VRAM
- **+** Knowledge-tuning method is described in an ACM TKDD paper
- **−** Training data is mostly GPT-generated and the authors admit it contains errors
- **−** Literature model covers only liver cancer; other diseases are planned, not released
- **−** Resources are for academic use only; the disclaimer prohibits commercial use
- **−** Base models are 2023-era 7B; authors say LLaMA-based results are limited

<sub>GPU required · Needs PyTorch, Hugging Face Transformers, PEFT, CUDA · Models: LLaMA-7B, Alpaca-Chinese-7B, Bloom-7B, Huozi 1.0 · [Repo](https://github.com/scir-hi/huatuo-llama-med-chinese) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/huatuo-llama-med-chinese/)</sub>

<a name="boltz"></a>
### #&#8288;59 [boltz](https://github.com/jwohlwend/boltz) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (20) · Freshness: recent (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · May 2026</sub>

**Open biomolecular structure and binding affinity prediction models.**

Boltz is a family of open biomolecular interaction models, Boltz-1 and Boltz-2, run through a `boltz predict` CLI that reads YAML inputs. Boltz-2 predicts complex structures and ligand binding affinity, reporting a binder probability and a log10(IC50) value. Code and weights are MIT licensed and install from PyPI.

- **+** Code and weights both MIT-licensed, usable commercially
- **+** Boltz-2 outputs affinity: binder probability and log10(IC50) value
- **+** Batch prediction from a directory of YAML files with one CLI command
- **+** Uses NVIDIA cuEquivariance kernels on recent GPUs; Tenstorrent via a fork
- **−** Boltz-2 training code and evaluation scripts are not yet released
- **−** CPU mode works but is significantly slower than GPU
- **−** The --use_msa_server option sends sequences to a remote MSA server
- **−** No Docker image or compose file provided

<sub>GPU optional · Needs Python, MSA server (via --use_msa_server), NVIDIA cuEquivariance (optional) · Models: Boltz-1, Boltz-2 · [Repo](https://github.com/jwohlwend/boltz) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/boltz/)</sub>

<a name="coreml-models"></a>
### #&#8288;60 [coreml-models](https://github.com/john-rocky/coreml-models) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: partly (70) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 1.9k · no license · Oct 2026</sub>

**Converted Core ML models for iOS and macOS, with sample apps.**

A model zoo of pre-converted Core ML (.mlpackage) models covering image classification, object detection (YOLO, D-FINE, RF-DETR), segmentation, super resolution, depth, Stable Diffusion, TTS, source separation and small LLMs such as Gemma 4 and Qwen3.5. Models are downloaded from Google Drive or GitHub releases and bundled into an Xcode project, and some link to Swift sample apps. Each model keeps the license of its original project.

- **+** Wide coverage: vision, audio, diffusion and LLMs in one catalog of Core ML models
- **+** Detector entries document input size, output shape and whether NMS is included
- **+** Some models have Swift sample apps or Colab conversion scripts
- **+** Used by xLights on macOS for HTDemucs stem separation
- **−** No repository license; each model follows its upstream license, including GPL and AGPL
- **−** Many downloads are Google Drive links, which are hard to script or pin
- **−** Apple platforms only; .mlpackage format, not the newer .aimodel format
- **−** Sample apps cover only some models; many entries are download-only

<sub>Needs Xcode, Core ML · Models: Core ML .mlpackage · [Repo](https://github.com/john-rocky/coreml-models) · [📖 Docs ↗](https://john-rocky.github.io/core-ai/) · [🌐 Site ↗](https://john-rocky.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/coreml-models/)</sub>

<a name="skywork-r1v"></a>
### #&#8288;61 [skywork-r1v](https://github.com/skyworkai/skywork-r1v) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (15) · Freshness: active (94) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · MIT · Jul 2026</sub>

**Open-weight 38B multimodal reasoning model with inference and eval code.**

Skywork-R1V3 is a 38B vision-language reasoning model post-trained mainly with reinforcement learning on top of InternVL3-38B. The repository holds inference scripts for Transformers and vLLM, plus evaluation code for reproducing the reported benchmarks. The README reports 76.0 on MMMU (val), and weights are hosted on Hugging Face.

- **+** Reports 76.0 MMMU and tops MathVista, MathVerse and MMK12 in its own comparison table
- **+** Includes eval code to reproduce the benchmark results
- **+** Inference scripts for both Transformers and vLLM with tensor parallelism
- **+** MIT-licensed code on an MIT-licensed InternVL3-38B base
- **−** Benchmark numbers are self-reported; some baseline scores come from the authors' own framework
- **−** 38B size needs multiple GPUs for the full model
- **−** Trails Claude 3.7 on EMMA, MathVision and SeePhys in the README table
- **−** No Docker image or packaged server; setup is conda plus shell scripts

<sub>GPU required · Needs conda, Python 3.10, Transformers, vLLM · Models: Skywork-R1V3-38B, Skywork-R1V2-38B, Skywork-R1V2-38B-AWQ, Skywork-R1V-38B, Skywork-R1V-38B-AWQ · [Repo](https://github.com/skyworkai/skywork-r1v) · [📖 Docs ↗](https://arxiv.org/abs/2507.06167) · [🌐 Site ↗](https://huggingface.co/Skywork/Skywork-R1V3-38B) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skywork-r1v/)</sub>

<a name="cogagent"></a>
### #&#8288;62 [cogagent](https://github.com/zai-org/cogagent) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Oct 2026</sub>

**Open 9B vision-language model that reads screenshots and outputs GUI actions.**

CogAgent-9B-20241220 is a GLM-4V-9B-based vision-language model that takes a screenshot, a task and step history, and returns a grounded GUI operation such as CLICK with a bounding box. It supports Windows, macOS and Android screens in Chinese and English. The repo provides transformers inference scripts, a Gradio-style web demo, and SFT/LoRA fine-tuning code.

- **+** Returns grounded actions with box coordinates for Windows, macOS and Android screenshots
- **+** Selectable output formats, e.g. Action-Operation-Sensitive flags sensitive operations
- **+** Includes SFT and LoRA fine-tuning code plus INT4/INT8 inference options
- **+** Weights on HuggingFace, ModelScope, WiseModel and Ascend-targeted Modelers
- **−** Needs about 29GB VRAM at BF16; INT4 (about 8GB) is discouraged for quality loss
- **−** Not conversational: no continuous dialogue, caller must build the history string
- **−** Output is a strict-format string, not JSON, so callers must parse it themselves
- **−** Online demo cannot control a computer; LoRA fine-tuning needs 70GB on one GPU

<sub>GPU required · Needs PyTorch, transformers · Models: cogagent-9b-20241220, GLM-4V-9B base, BF16, INT8, INT4 · port 7860 · [Repo](https://github.com/zai-org/cogagent) · [▶️ Demo ↗](https://huggingface.co/spaces/THUDM-HF-SPACE/CogAgent-Demo) · [📖 Docs ↗](https://cogagent.aminer.cn/blog#/articles/cogagent-9b-20241220-technical-report) · [🌐 Site ↗](https://cogagent.aminer.cn/home) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cogagent/)</sub>

<a name="gorilla"></a>
### #&#8288;63 [gorilla](https://github.com/shishirpatil/gorilla) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: popular (66) · Freshness: slowing (38) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Mar 2026</sub>

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

<a name="deepvariant"></a>
### #&#8288;64 [deepvariant](https://github.com/google/deepvariant) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (18) · Freshness: recent (56) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · BSD-3-Clause · Mar 2026</sub>

**CNN-based germline variant caller that turns BAM/CRAM reads into VCF/gVCF.**

DeepVariant builds pileup image tensors from aligned reads (BAM or CRAM), classifies each with a convolutional neural network, and writes VCF or gVCF. Pretrained models cover Illumina/Element WGS and WES, PacBio HiFi, ONT R10.4.1 and hybrid PacBio+Illumina, all trained on human data. It also includes DeepTrio for trio and duo calling. It is research code, not intended for clinical use.

- **+** Model types for WGS, WES, PACBIO, ONT_R104 and HYBRID_PACBIO_ILLUMINA via one run_deepvariant command
- **+** Documented case studies per sequencing platform, plus pangenome-aware and RNA-seq modes
- **+** Won 2020 PrecisionFDA Truth Challenge V2 in several categories, per the README
- **+** Official Docker image; GPU optional, with an experimental CPU/GPU pipelined mode
- **−** Diploid organisms only; genotypes limited to hom-ref, het and hom-alt
- **−** Bundled models trained on human data only; other species need extra care
- **−** Germline only; somatic calling lives in the separate DeepSomatic repo
- **−** Unix-like systems only; source build scripts target Ubuntu 20.04; external PRs not merged directly

<sub>GPU optional · Docker · Needs Docker, TensorFlow, Nucleus, GLnexus (DeepTrio merging) · Models: BAM, CRAM, VCF, gVCF, WGS · [Repo](https://github.com/google/deepvariant) · [🌐 Site ↗](https://goo.gl/deepvariant) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepvariant/)</sub>

<a name="z-image"></a>
### #&#8288;65 [z-image](https://github.com/tongyi-mai/z-image) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: popular (62) · Freshness: slowing (32) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Feb 2026</sub>

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

<a name="bagel"></a>
### #&#8288;66 [bagel](https://github.com/bytedance-seed/bagel) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: known (38) · Freshness: recent (63) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · May 2026</sub>

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

<a name="qwen-image"></a>
### #&#8288;67 [qwen-image](https://github.com/qwenlm/qwen-image) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: known (49) · Freshness: slowing (33) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · Apache-2.0 · Feb 2026</sub>

**20B MMDiT image generation and editing model with strong text rendering.**

Qwen-Image is a 20B MMDiT image foundation model from the Qwen team, covering text-to-image, single and multi-image editing, and layered output. The repo holds diffusers quick-start code, prompt-enhancement helpers that call DashScope, and a Gradio demo server that spreads work across multiple GPUs. Weights are on Hugging Face and ModelScope.

- **+** Text-to-image and editing variants (2512, Edit-2511, Layered) published as open weights
- **+** Strong text rendering, with Chinese called out specifically
- **+** Runs through diffusers pipelines; ComfyUI, vLLM-Omni and SGLang-Diffusion support noted
- **+** Gradio server with multi-GPU workers and a task queue, set by env vars
- **−** Needs diffusers installed from git main and transformers>=4.51.3
- **−** Prompt enhancement needs a DashScope API key, an external paid service
- **−** Qwen-Image-2.0 is announced for Qwen Chat; README does not link open weights

<sub>GPU optional · Needs diffusers, transformers>=4.51.3, PyTorch, DashScope API (optional, prompt enhancement) · Models: Qwen-Image, Qwen-Image-2512, Qwen-Image-Edit, Qwen-Image-Edit-2509, Qwen-Image-Edit-2511 · [Repo](https://github.com/qwenlm/qwen-image) · [▶️ Demo ↗](https://huggingface.co/spaces/Qwen/Qwen-Image) · [📖 Docs ↗](https://arxiv.org/abs/2508.02324) · [🌐 Site ↗](https://qwenlm.github.io/blog/qwen-image/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwen-image/)</sub>

<a name="chinese-clip"></a>
### #&#8288;68 [chinese-clip](https://github.com/ofa-sys/chinese-clip) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: known (36) · Freshness: recent (51) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Mar 2026</sub>

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

<a name="qwen3"></a>
### #&#8288;69 [qwen3](https://github.com/qwenlm/qwen3) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: widely used (86) · Freshness: quiet (21) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 28k · no license · Jan 2026</sub>

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

<a name="chinese-llama-alpaca-2"></a>
### #&#8288;70 [chinese-llama-alpaca-2](https://github.com/ymcui/chinese-llama-alpaca-2) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: known (43) · Freshness: slowing (40) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Apr 2026</sub>

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

<a name="rex-omni"></a>
### #&#8288;71 [rex-omni](https://github.com/idea-research/rex-omni) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: niche (5) · Freshness: slowing (37) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · custom license · Feb 2026</sub>

**3B multimodal model for detection, pointing, OCR and keypoints.**

Rex-Omni is a 3B-parameter multimodal LLM, based on Qwen2.5-VL, that emits boxes, points, polygons and keypoints as text tokens. The repo provides a Python wrapper with transformers and vLLM backends, tutorials for each task, a Gradio demo, evaluation code, and SFT/GRPO fine-tuning for pointing. An AWQ-quantized checkpoint is also published.

- **+** One model covers detection, pointing, visual prompting, OCR boxes/polygons, keypoints and GUI grounding
- **+** Two backends: transformers for simplicity, vLLM for batch throughput
- **+** AWQ checkpoint published, which the README says halves storage
- **+** Includes evaluation code, fine-tuning code, and a SAM pairing for masks
- **−** Custom IDEA License 1.0 on a Qwen research-licensed base; not a standard OSI license
- **−** Install pins torch 2.7.0 with CUDA 12.8 wheels, so it targets NVIDIA GPUs
- **−** Gradio demo default server_name is a hardcoded private IP and needs overriding
- **−** No release tags and no Docker setup

<sub>GPU required · Needs PyTorch 2.7.0, CUDA 12.8, transformers, vLLM (optional), Gradio · Models: Rex-Omni 3B, Rex-Omni-AWQ, Hugging Face checkpoints · port 5211 · [Repo](https://github.com/idea-research/rex-omni) · [▶️ Demo ↗](https://huggingface.co/spaces/Mountchicken/Rex-Omni) · [🌐 Site ↗](https://rex-omni.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rex-omni/)</sub>

<a name="needle"></a>
### #&#8288;72 [needle](https://github.com/cactus-compute/needle) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 7 · no license · Nov 2026</sub>

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

<a name="ernie"></a>
### #&#8288;73 [ernie](https://github.com/paddlepaddle/ernie) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: known (47) · Freshness: quiet (15) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · Apache-2.0 · Dec 2025</sub>

**Open-weight ERNIE 4.5 multimodal MoE models with ERNIEKit fine-tuning tools.**

Baidu's ERNIE 4.5 repository covers ten open-weight models: MoE LLMs (300B-A47B, 21B-A3B), vision-language MoE models (424B-A47B, 28B-A3B) and a 0.3B dense model. It ships ERNIEKit, a PaddlePaddle toolkit for SFT, DPO, LoRA and QAT with CLI and WebUI. Inference is handled by the separate FastDeploy project, which provides an OpenAI-compatible server.

- **+** Apache-2.0 weights across 10 variants, from 0.3B dense to 424B MoE
- **+** ERNIEKit covers SFT, DPO, LoRA variants and QAT with CLI and WebUI
- **+** VL models support thinking and non-thinking modes; 128K context window
- **+** Cookbook notebooks with Gradio demos for chat, search, RAG, OCR and fine-tuning
- **−** Training and inference depend on PaddlePaddle rather than PyTorch-native tooling
- **−** Inference lives in a separate project, FastDeploy, so setup spans two repos
- **−** Training for the ERNIE-4.5-VL base and 424B models was listed as coming soon
- **−** Post-training quantization (PTQ) is marked work in progress; last release was June 2025

<sub>GPU required · Docker · Needs PaddlePaddle, FastDeploy, Hugging Face CLI · Models: ERNIE-4.5-300B-A47B, ERNIE-4.5-21B-A3B, ERNIE-4.5-VL-424B-A47B, ERNIE-4.5-VL-28B-A3B, ERNIE-4.5-0.3B · port 9904 · [Repo](https://github.com/paddlepaddle/ernie) · [📖 Docs ↗](https://github.com/PaddlePaddle/ERNIE/blob/develop/docs/erniekit.md) · [🌐 Site ↗](https://ernie.baidu.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ernie/)</sub>

<a name="text2vec"></a>
### #&#8288;74 [text2vec](https://github.com/shibing624/text2vec) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (30) · Freshness: quiet (24) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · Apache-2.0 · Feb 2026</sub>

**Python library for sentence embeddings and Chinese text similarity models.**

text2vec is a PyTorch-based Python library that encodes words, sentences and paragraphs into vectors. It implements Word2Vec, SBERT, CoSENT and BGE training and inference, and links pretrained Chinese and multilingual CoSENT models on Hugging Face, benchmarked with Spearman scores on ATEC, BQ, LCQMC, PAWSX and STS-B. It also supports multi-GPU/CPU inference and a CLI for batch encoding.

- **+** Pretrained Chinese and multilingual CoSENT models, with published Spearman scores on seven test sets
- **+** Covers training and inference for SBERT, CoSENT and BGE in one package
- **+** Multi-GPU and multi-CPU inference, plus a CLI for batch encoding
- **+** Models also load via plain transformers or sentence-transformers, so the library is optional
- **−** Last release v1.2.9 is from September 2023; newer embedding models are not covered
- **−** README and docs are mostly in Chinese; English version is a separate file
- **−** Word2Vec vector file link points to Baidu Pan, awkward outside China
- **−** Released models are 2023-era BERT-base size, except one bge-large variant

<sub>GPU optional · Needs PyTorch, transformers, gensim · Models: Word2Vec, SBERT, CoSENT, BGE, Hugging Face transformers models · [Repo](https://github.com/shibing624/text2vec) · [▶️ Demo ↗](https://huggingface.co/spaces/shibing624/text2vec) · [📖 Docs ↗](https://github.com/shibing624/text2vec/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/text2vec/)</sub>

<a name="alphageometry"></a>
### #&#8288;75 [alphageometry](https://github.com/google-deepmind/alphageometry) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: niche (29) · Freshness: quiet (20) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · Apache-2.0 · Jan 2026</sub>

**Research code for DDAR and AlphaGeometry olympiad geometry theorem provers.**

Reproduces the two geometry provers from the 2024 Nature paper: DDAR, a symbolic deduction engine (DD plus algebraic reasoning), and AlphaGeometry, which adds a 150M-parameter transformer that proposes auxiliary constructions via beam search in JAX. It prints numbered, fully justified proofs and ships the IMO-AG-30 and JGEX-AG-231 problem sets. DDAR solves 14 of 30 IMO-AG-30 problems and AlphaGeometry solves 25.

- **+** DDAR runs standalone without meliad or sentencepiece, so no checkpoint is needed
- **+** Proofs are printed step by step with numbered, traceable predicates
- **+** Includes benchmark problem files and a test suite for checking reproduced results
- **+** Checkpoint and vocabulary are provided via download.sh under CC BY 4.0
- **−** Paper-scale results need 4 V100 GPUs and 250 CPU workers; parallelism code was removed
- **−** Meliad must be cloned manually because it is not on pip
- **−** Issue #14 reports LM scores differ between users, though top beams match
- **−** README says Google will not maintain or support the code

<sub>GPU optional · Needs meliad, JAX, Flax, TensorFlow, gin-config, SentencePiece, Python 3.10 · Models: AlphaGeometry 150M transformer checkpoint · [Repo](https://github.com/google-deepmind/alphageometry) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/alphageometry/)</sub>

<a name="mambavision"></a>
### #&#8288;76 [mambavision](https://github.com/nvlabs/mambavision) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: niche (10) · Freshness: slowing (35) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · custom license · Mar 2026</sub>

**Hybrid Mamba-Transformer vision backbone with pretrained ImageNet checkpoints.**

Official PyTorch implementation of MambaVision, a hierarchical vision backbone that mixes Mamba-style mixer blocks with self-attention. It ships ImageNet-1K and 21K classification checkpoints from 31.8M to 739.6M parameters, loadable via the `mambavision` pip package or Hugging Face with `trust_remote_code`. Code and models for COCO detection (Cascade Mask R-CNN) and ADE20K segmentation (UPerNet) are included.

- **+** Checkpoints from 31.8M to 739.6M params; L3-512-21K reports 88.1% ImageNet top-1
- **+** Accepts any input resolution; returns 4-stage multi-scale features for downstream tasks
- **+** Loads via pip package or Hugging Face; Colab notebook provided
- **+** Includes detection and segmentation configs, logs and checkpoints
- **−** Vision backbone only; no chat, serving API or UI
- **−** License is not a standard SPDX identifier; business use goes through NVIDIA licensing
- **−** Examples assume CUDA; CPU or Apple Silicon use is not documented
- **−** Detection and segmentation live in separate subfolders with their own setup

<sub>GPU required · Docker · Needs PyTorch, timm, transformers · Models: PyTorch .pth.tar checkpoints, Hugging Face transformers · [Repo](https://github.com/nvlabs/mambavision) · [▶️ Demo ↗](https://colab.research.google.com/drive/1WR8LAzRMoK19RiFA-Br0Xxir_Htb3pLf) · [📖 Docs ↗](https://arxiv.org/abs/2407.08083) · [🌐 Site ↗](https://huggingface.co/collections/nvidia/mambavision-66943871a6b36c9e78b327d3) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mambavision/)</sub>

<a name="omdet"></a>
### #&#8288;77 [omdet](https://github.com/om-ai-lab/omdet) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: niche (4) · Freshness: slowing (44) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · Apache-2.0 · Mar 2026</sub>

**Real-time open-vocabulary object detector driven by text prompts.**

Official PyTorch implementation of OmDet-Turbo, a transformer-based open-vocabulary detector that finds objects from class names given as text. It uses an Efficient Fusion Head to reduce multimodal fusion cost. The repo provides a Tiny Swin-T model, a demo script, an API server on port 8000, and ONNX export, with zero-shot scores of 42.5 AP on COCO and 30.3 on LVIS.

- **+** Tiny model reports 21.5 FPS in PyTorch and 140.0 FPS with TensorRT
- **+** Detects arbitrary text-prompted classes zero-shot (COCO 42.5, LVIS 30.3 AP)
- **+** Ships demo script, HTTP API server with /docs page, and ONNX export
- **+** Integrated into Hugging Face Transformers 4.45.0; weights also on ModelScope
- **−** Model zoo lists only the Tiny Swin-T weights; Base weights are not linked
- **−** ONNX export has fixed input sizes and no post-processing by default
- **−** No training instructions, inference and export only
- **−** Model and CLIP checkpoints must be downloaded manually into a resources folder

<sub>Needs PyTorch, CLIP ViT-B-16 checkpoint · Models: OmDet-Turbo-Tiny (Swin-T), ONNX export · port 8000 · [Repo](https://github.com/om-ai-lab/omdet) · [🌐 Site ↗](https://arxiv.org/abs/2403.06892) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/omdet/)</sub>

<a name="dreamdojo"></a>
### #&#8288;78 [dreamdojo](https://github.com/nvidia/dreamdojo) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: niche (1) · Freshness: slowing (47) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · Apache-2.0 · Mar 2026</sub>

**Robot world model trained on 44k hours of human egocentric video.**

DreamDojo is NVIDIA's interactive world model for robots, pretrained on 44k hours of human egocentric video and post-trained on robot data. The repo has code for latent action model training, pretraining, post-training, distillation and evaluation. Distilled models are reported to generate autoregressively at 10 FPS for over 1 minute. 2B and 14B checkpoints and GR-1 datasets are on Hugging Face.

- **+** Covers the full pipeline: latent action model, pretraining, post-training, distillation, evaluation
- **+** Releases 2B and 14B pretrained and post-trained checkpoints
- **+** Includes GR-1 post-training datasets and evaluation sets
- **+** Apache-2.0 source code with paper and project website
- **−** README gives no hardware requirements; setup details are only in linked docs
- **−** Research code for robotics, not a general-purpose video generation tool
- **−** No tagged releases
- **−** Pretraining on 44k hours of video implies heavy compute, but no figures are given

<sub>Docker · Needs Hugging Face · Models: DreamDojo 2B, DreamDojo 14B · [Repo](https://github.com/nvidia/dreamdojo) · [📖 Docs ↗](https://github.com/NVIDIA/DreamDojo/blob/main/docs/SETUP.md) · [🌐 Site ↗](https://dreamdojo-world.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dreamdojo/)</sub>

<a name="joycaption"></a>
### #&#8288;79 [joycaption](https://github.com/fpgaminer/joycaption) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: niche (3) · Freshness: slowing (38) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · Apache-2.0 · Feb 2026</sub>

**Llama 3.1-based image captioning VLM for building diffusion training datasets.**

JoyCaption is an open-weight vision-language model built on Llama 3.1 that writes captions for images, aimed at preparing diffusion model training data. It supports prompt modes such as descriptive, straightforward, Stable Diffusion and MidJourney prompts, and Danbooru, e621 and Rule34 tag lists. The repo holds usage examples (Transformers, vLLM) and finetuning scripts; the current model is Beta One.

- **+** Covers SFW and NSFW content, unlike the censored captioners it is compared against
- **+** Eleven prompt modes, including booru tag lists and Stable Diffusion prompt styles
- **+** Serves through vLLM with an OpenAI-compatible API
- **+** Includes finetuning scripts and a ComfyUI node with 8-bit and 4-bit support
- **−** Needs about 17GB VRAM at bfloat16; lower memory requires quantization
- **−** Glitches on 1.5 to 3% of outputs, such as repetition loops
- **−** Tag-list modes (Danbooru, e621, Rule34) have lower accuracy than caption modes
- **−** Not a general instruction follower; left/right and OCR errors are expected

<sub>GPU required · Needs PyTorch, Hugging Face Transformers, vLLM (optional) · Models: Llama 3.1 LLaVA-style HF checkpoint (bfloat16), 8-bit and 4-bit quantization · [Repo](https://github.com/fpgaminer/joycaption) · [▶️ Demo ↗](https://huggingface.co/spaces/fancyfeast/joy-caption-beta-one) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/joycaption/)</sub>

<a name="basic-pitch"></a>
### #&#8288;80 [basic-pitch](https://github.com/spotify/basic-pitch) <sub>score [11](../README.md#-how-we-rank "Score 11/100. Adoption: known (37) · Freshness: quiet (0) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Nov 2025</sub>

**Python library that transcribes audio to MIDI with pitch bends.**

Basic Pitch is a Spotify Audio Intelligence Lab library for automatic music transcription. It runs a lightweight neural network that turns an audio file into polyphonic MIDI with pitch bends, without being tied to one instrument. It ships as a pip package with a CLI and a Python API, and includes TensorFlow, CoreML, TFLite and ONNX versions of the model.

- **+** Instrument-agnostic polyphonic transcription to MIDI, including pitch bends
- **+** Model ships in TensorFlow, CoreML, TensorFlowLite and ONNX formats
- **+** CLI can also save a WAV rendering, raw NPZ outputs and CSV note events
- **+** Installs with pip and does not require TensorFlow by default
- **−** Meant for one instrument at a time; multi-instrument mixes are not the target
- **−** Stereo input is down-mixed to mono and resampled to 22050 Hz
- **−** Mac M1 supported only on Python 3.10; README lists Python up to 3.11
- **−** Last release was August 2024

<sub>Docker · Needs librosa, TensorFlow (optional) · Models: TensorFlow, CoreML, TensorFlow Lite, ONNX · [Repo](https://github.com/spotify/basic-pitch) · [▶️ Demo ↗](https://basicpitch.io) · [🌐 Site ↗](https://basicpitch.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/basic-pitch/)</sub>

<a name="show-o"></a>
### #&#8288;81 [show-o](https://github.com/showlab/show-o) <sub>score [9](../README.md#-how-we-rank "Score 9/100. Adoption: niche (8) · Freshness: quiet (21) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Jan 2026</sub>

**Unified transformer for multimodal understanding and image generation.**

Show-o and Show-o2 are research models from NUS Show Lab and ByteDance that use one transformer for multimodal understanding and generation. Show-o (1.3B) handles captioning, VQA, text-to-image, inpainting and extrapolation, mixing autoregressive text with discrete diffusion on image tokens. Show-o2 (1.5B and 7B) works in a 3D causal VAE space, adds video understanding, and uses autoregressive and flow-matching heads.

- **+** One model covers VQA, captioning, text-to-image, inpainting and extrapolation
- **+** Checkpoints on Hugging Face for Show-o (256 and 512 res) and Show-o2 (1.5B, 7B)
- **+** Training code for pre-training and instruction tuning, with accelerate and DeepSpeed configs
- **+** Hugging Face Space demo available; Apache-2.0 license
- **−** Research code driven by CLI scripts and YAML configs; no server or UI
- **−** Stage 1 training needs manual edits because RefinedWeb loading uses internal packages
- **−** Inference demos log results to wandb, which requires a login
- **−** Mixed-modal generation and visual tokenizer training are listed as pending features

<sub>Needs PyTorch, wandb, accelerate, Hugging Face Hub · Models: Show-o 1.3B, Show-o2 1.5B, Show-o2 7B · [Repo](https://github.com/showlab/show-o) · [▶️ Demo ↗](https://huggingface.co/spaces/showlab/Show-o) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/show-o/)</sub>

<a name="star-vector"></a>
### #&#8288;82 [star-vector](https://github.com/joanrod/star-vector) <sub>score [8](../README.md#-how-we-rank "Score 8/100. Adoption: niche (26) · Freshness: quiet (0) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · Apache-2.0 · Nov 2025</sub>

**Vision-language model that converts images and text into SVG code.**

StarVector is a multimodal model built on StarCoder that generates SVG code directly from an image (image2SVG) or a text prompt (text2SVG). The repo has inference code, 1B and 8B checkpoints on Hugging Face, training scripts (DeepSpeed for 1B, FSDP for 8B), the SVG-Stack dataset and the SVG-Bench evaluation suite. A Gradio demo runs on the HF backend or a vLLM fork.

- **+** Outputs SVG code using primitives like ellipses, polygons and text, not only path curves
- **+** Ships 1B and 8B checkpoints plus SVG-Stack (2.1M train) and SVG-Bench datasets
- **+** Includes training and evaluation scripts, with HF and vLLM generation backends
- **+** 8B has the highest listed DinoScore on all five SVG-Bench sets in the README table
- **−** Not trained on natural images or illustrations; suited to icons, logos, diagrams, charts
- **−** vLLM backend needs a separate StarVector fork of vLLM
- **−** Demo needs three processes (controller, web server, worker) started by hand
- **−** Reference training commands assume 8 GPUs

<sub>GPU required · Docker · Needs PyTorch, Hugging Face Transformers, Gradio, vLLM fork (optional), DeepSpeed and Accelerate (training) · Models: starvector-1b-im2svg, starvector-8b-im2svg, Hugging Face Transformers, vLLM · port 7000 · [Repo](https://github.com/joanrod/star-vector) · [🌐 Site ↗](https://starvector.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/star-vector/)</sub>

<a name="yolov13"></a>
### #&#8288;83 [yolov13](https://github.com/imoonlab/yolov13) <sub>score [3](../README.md#-how-we-rank "Score 3/100. Adoption: niche (6) · Freshness: quiet (4) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · AGPL-3.0 · Nov 2025</sub>

**YOLOv13 real-time object detection models built on the Ultralytics codebase.**

YOLOv13 is a research implementation of a real-time object detector, forked from Ultralytics, with Nano, Small, Large and X-Large variants. It adds hypergraph-based feature correlation (HyperACE), a full-pipeline feature distribution scheme (FullPAD) and depthwise-separable blocks. Training, validation, prediction and export to ONNX or TensorRT go through the Ultralytics YOLO Python API, with pretrained COCO weights on the releases page.

- **+** Reported COCO AP50:95 of 41.6 (N), 48.0 (S), 53.4 (L), 54.8 (X), above YOLOv12 at each size
- **+** Pretrained weights for four sizes, usable through the familiar Ultralytics YOLO API
- **+** Exports to ONNX and TensorRT; community ports to Ascend, RKNN and Android are linked
- **+** Includes a FastAPI REST example and public demos on Hugging Face Spaces and HyperAI
- **−** Latency in the README table is higher than YOLOv12 at every size, e.g. 14.67 ms vs 12.46 ms for X
- **−** AGPL-3.0 license restricts closed-source and network-service use
- **−** Install instructions pin a Flash Attention wheel for Python 3.11, CUDA 11 and Linux
- **−** Last release was 2025-06-22; the README gives no versioned release notes

<sub>GPU optional · Docker · Needs Ultralytics, PyTorch, Flash Attention, Python 3.11 · Models: YOLOv13 N/S/L/X .pt weights, ONNX export, TensorRT export · [Repo](https://github.com/imoonlab/yolov13) · [▶️ Demo ↗](https://huggingface.co/spaces/atalaydenknalbant/Yolov13) · [📖 Docs ↗](https://arxiv.org/abs/2506.17733) · [🌐 Site ↗](https://github.com/iMoonLab) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yolov13/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
