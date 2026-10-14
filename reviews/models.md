# 🧬 Open models reviews · Best of Open-Source AI

Repositories of open-weight models with the code to run them: LLMs, vision, speech and embedding models. Back to the [leaderboard](../README.md#-open-models).

<sub>🌐 Also on the web: [Open models on archestack.com](https://archestack.com/best-of-ai/models/), each project on its own page.</sub>

<a name="timesfm"></a>
### 🥇 [timesfm](https://github.com/google-research/timesfm) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Sep 2026</sub>

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

<a name="clip"></a>
### 🥈 [clip](https://github.com/openai/clip) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: niche (27) · Freshness: recent (59) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Mar 2026</sub>

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
