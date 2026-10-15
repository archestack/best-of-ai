# 🧬 Open models reviews · Best of Open-Source AI

Repositories of open-weight models with the code to run them: LLMs, vision, speech and embedding models. Back to the [leaderboard](../README.md#-open-models).

<sub>🌐 Also on the web: [Open models on archestack.com](https://archestack.com/best-of-ai/models/), each project on its own page.</sub>

<a name="llmfit"></a>
### 🥇 [llmfit](https://github.com/alexsjones/llmfit) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Oct 2026</sub>

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
### 🥈 [laya](https://github.com/nandhakishorm/laya) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Oct 2026</sub>

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
### 🥉 [timesfm](https://github.com/google-research/timesfm) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (49) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Sep 2026</sub>

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

<a name="kronos"></a>
### #&#8288;4 [kronos](https://github.com/shiyu-coder/kronos) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: widely used (81) · Freshness: recent (65) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Apr 2026</sub>

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

<a name="clip"></a>
### #&#8288;5 [clip](https://github.com/openai/clip) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: known (37) · Freshness: recent (59) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Mar 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
