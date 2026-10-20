# 🏋️ Training and fine-tuning reviews · Best of Open-Source AI

Tools to fine-tune, train or distill models on your own data and GPUs, from LoRA scripts to full training stacks. Back to the [leaderboard](../README.md#%EF%B8%8F-training-and-fine-tuning).

<sub>🌐 Also on the web: [Training and fine-tuning on archestack.com](https://archestack.com/best-of-ai/training/), each project on its own page.</sub>

<a name="unsloth"></a>
### 🥇 [unsloth](https://github.com/unslothai/unsloth) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · Apache-2.0 · Oct 2026</sub>

**Desktop and web app to run, fine-tune and export open models.**

Unsloth ships as a desktop app, a web UI (Studio) and a Python library for running and fine-tuning models. It runs GGUF and other open models locally with an OpenAI-compatible API, and trains with LoRA, QLoRA, full fine-tuning and RL methods such as GRPO and DPO. The README claims 2x faster training with up to 70% less VRAM, and exports to GGUF, FP8 and NVFP4.

- **+** Fine-tuning covers LoRA, QLoRA, full fine-tuning, GRPO, DPO and FP8 pretraining
- **+** Claims 2x faster training with up to 70% less VRAM, per README
- **+** Exports to GGUF, FP8 and NVFP4 and serves an OpenAI-compatible API
- **+** Runs on NVIDIA, AMD, Intel, CPU and Vulkan across Windows, macOS and Linux
- **−** Scope is broad: desktop app, Studio web UI and Core library each install differently
- **−** Server-side tools are on by default; exposing it needs --disable-tools or a strong password
- **−** Install relies on curl or irm piped to shell scripts
- **−** Speed and VRAM figures are the project's own claims; hardware requirements are not listed

<sub>GPU optional · Docker · Needs PyTorch, llama.cpp, audio.cpp, Cloudflare (optional remote access) · Models: GGUF, MLX, LoRA, QLoRA, diffusion · port 8000 · [Repo](https://github.com/unslothai/unsloth) · [▶️ Demo ↗](https://colab.research.google.com/github/unslothai/unsloth/blob/main/studio/Unsloth_Studio_Colab.ipynb) · [📖 Docs ↗](https://unsloth.ai/docs) · [🌐 Site ↗](https://unsloth.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unsloth/)</sub>

<a name="deepspeed"></a>
### 🥈 [deepspeed](https://github.com/deepspeedai/deepspeed) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Oct 2026</sub>

**PyTorch library for distributed training of large models with ZeRO.**

DeepSpeed is a PyTorch optimization library for training large deep learning models across many GPUs. It provides ZeRO memory partitioning with CPU and NVMe offload, 3D parallelism, Ulysses sequence parallelism and MoE support, configured through a JSON file. It integrates with Hugging Face Transformers and Accelerate, Lightning, MosaicML Composer, Determined and MMEngine.

- **+** Used to train models such as BLOOM 176B and Megatron-Turing NLG 530B
- **+** Integrates with Hugging Face Transformers/Accelerate, Lightning, Composer, Determined and MMEngine
- **+** Supports NVIDIA, AMD, Intel Gaudi/XPU/CPU, Huawei Ascend NPU and Tecorigin accelerators
- **+** Installs from PyPI; C++/CUDA ops are JIT-compiled or pre-built
- **−** Needs PyTorch installed first and a CUDA or ROCm compiler for JIT ops
- **−** Mainly tested on NVIDIA Pascal to Hopper and AMD MI100/MI200
- **−** Windows lacks async IO and GDS support
- **−** Large JSON config surface; ZeRO and offload tuning requires reading the docs

<sub>GPU optional · Docker · Needs PyTorch, CUDA or ROCm compiler (nvcc/hipcc), ninja · Models: PyTorch models, Hugging Face Transformers · [Repo](https://github.com/deepspeedai/deepspeed) · [📖 Docs ↗](https://deepspeed.readthedocs.io/en/latest/) · [🌐 Site ↗](https://www.deepspeed.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepspeed/)</sub>

<a name="verl"></a>
### 🥉 [verl](https://github.com/verl-project/verl) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Oct 2026</sub>

**Reinforcement learning training library for LLM post-training with PPO and GRPO.**

verl is the open-source implementation of the HybridFlow paper from ByteDance Seed. It runs RL and supervised fine-tuning for LLMs using FSDP, FSDP2 or Megatron-LM for training and vLLM, SGLang or HF Transformers for rollout generation. It covers PPO, GRPO, RLOO, ReMax and others, with multi-turn tool calling, VLM support and scaling to 671B models.

- **+** Pluggable backends: FSDP/FSDP2/Megatron-LM for training, vLLM/SGLang/HF for rollout
- **+** Many RL algorithms built in: PPO, GRPO, ReMax, RLOO, REINFORCE++
- **+** Scales to 671B models and hundreds of GPUs via expert parallelism
- **+** Supports NVIDIA, AMD and Ascend hardware; LoRA RL to save memory
- **−** Needs multi-GPU clusters in practice; minimum hardware not stated in README
- **−** Many algorithm recipes live in a separate verl-recipe repository and submodule
- **−** Version-sensitive: README warns against vLLM 0.7.x and requires >=0.8.2
- **−** Several features remain under verl/experimental until merged into the main library

<sub>GPU required · Docker · Needs Ray, PyTorch, vLLM, SGLang, Megatron-LM · Models: Qwen3.5, Qwen3, Qwen2.5, Qwen2.5-VL, Kimi-VL · [Repo](https://github.com/verl-project/verl) · [📖 Docs ↗](https://verl.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/verl/)</sub>

<a name="peft"></a>
### #&#8288;4 [peft](https://github.com/huggingface/peft) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (50) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Oct 2026</sub>

**Python library for LoRA and other parameter-efficient fine-tuning of Transformers models.**

PEFT wraps a pretrained model with adapter methods such as LoRA, soft prompts and IA3 so only a small set of extra parameters is trained. Adapters are saved as small checkpoints (19MB versus 11GB for T0_3B in the README's example). It integrates with Transformers, Diffusers, Accelerate and TRL, and can be combined with quantization such as QLoRA.

- **+** Adapter checkpoints are MBs instead of GBs; 19MB vs 11GB for T0_3B
- **+** LoRA trained a 12B model (mt0-xxl) on one 80GB GPU where full finetuning ran out of memory
- **+** Integrates with Transformers, Diffusers, Accelerate and TRL; works with quantized base models
- **+** Install with pip; get_peft_model wraps an existing model in a few lines
- **−** Library only: no training UI, scheduler or serving; training loop is your own or Trainer
- **−** Transformers integration lacks some PEFT features, such as merging adapters into the base model
- **−** Models without official support need manual config for target modules
- **−** Memory figures in the README assume an A100 80GB with over 64GB CPU RAM

<sub>GPU optional · Docker · Needs PyTorch, Transformers · Models: LoRA, Soft prompts, IA3, QLoRA, Transformers models · [Repo](https://github.com/huggingface/peft) · [▶️ Demo ↗](https://huggingface.co/spaces/smangrul/peft-lora-sd-dreambooth) · [📖 Docs ↗](https://huggingface.co/docs/peft/main/en/index) · [🌐 Site ↗](https://huggingface.co/PEFT) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/peft/)</sub>

<a name="llamafactory"></a>
### #&#8288;5 [llamafactory](https://github.com/hiyouga/llamafactory) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 76k · Apache-2.0 · Oct 2026</sub>

**Fine-tuning toolkit for 100+ LLMs with a CLI and Gradio web UI.**

LlamaFactory fine-tunes language and multimodal models through YAML-configured CLI runs or the LLaMA Board Gradio UI. It covers pre-training, SFT, reward modeling, PPO, DPO, KTO and ORPO, with full-tuning, freeze-tuning, LoRA and 2 to 8-bit QLoRA. Trained models can be served through an OpenAI-style API using vLLM or SGLang workers.

- **+** Broad method coverage: SFT, PPO, DPO, KTO, ORPO, LoRA, QLoRA via AQLM/AWQ/GPTQ/HQQ/EETQ
- **+** Supports GaLore, BAdam, APOLLO, Muon, DoRA, PiSSA, plus Unsloth and Liger Kernel speedups
- **+** Covers multimodal and audio models such as Qwen3-VL, LLaVA and Qwen2-Audio
- **+** Runs on NVIDIA, AMD ROCm and Ascend NPU, with hosted Colab and PAI-DSW notebooks
- **−** Official documentation is marked WIP in the README
- **−** No VRAM or RAM figures in the visible README; hardware requirements unknown here
- **−** Web UI is for training and chat, not a production serving layer
- **−** Many optional backends (vLLM, SGLang, Unsloth, KTransformers) add install complexity

<sub>GPU required · Docker + Compose · Needs PyTorch, Hugging Face Transformers, Gradio, vLLM (optional), SGLang (optional) · Models: LLaMA, LLaVA, Mistral, Mixtral-MoE, Qwen3 · [Repo](https://github.com/hiyouga/llamafactory) · [▶️ Demo ↗](https://huggingface.co/spaces/hiyouga/LLaMA-Board) · [📖 Docs ↗](https://llamafactory.readthedocs.io/en/latest/) · [🌐 Site ↗](https://blog.llamafactory.net/en/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llamafactory/)</sub>

<a name="trl"></a>
### #&#8288;6 [trl](https://github.com/huggingface/trl) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Oct 2026</sub>

**Post-training library with SFT, DPO, GRPO and KTO trainers.**

TRL provides trainer classes (SFTTrainer, GRPOTrainer, DPOTrainer, KTOTrainer, RewardTrainer) that wrap the Hugging Face Transformers trainer for post-training language models. It scales through Accelerate with DDP, DeepSpeed ZeRO and FSDP, supports LoRA/QLoRA via PEFT, and ships a `trl` CLI for running SFT, DPO and KTO without code.

- **+** Covers SFT, DPO, GRPO, KTO and reward modeling with one trainer API
- **+** Scales from one GPU to multi-node via Accelerate, DDP, DeepSpeed and FSDP
- **+** Integrates PEFT (LoRA/QLoRA) and Unsloth for training on modest hardware
- **+** CLI commands (trl sft, dpo, kto) run fine-tuning without writing code
- **−** Code-first Python library with no web UI
- **−** Features under trl.experimental may change or be removed without notice
- **−** Built around the Hugging Face Transformers ecosystem
- **−** README gives no RAM or VRAM requirements

<sub>GPU optional · Docker · Needs transformers, accelerate, peft, datasets, deepspeed, unsloth · Models: Hugging Face Transformers models, LoRA/QLoRA adapters, AWS Trainium (TorchNeuron) · [Repo](https://github.com/huggingface/trl) · [📖 Docs ↗](https://huggingface.co/docs/trl/index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trl/)</sub>

<a name="megatron-lm"></a>
### #&#8288;7 [megatron-lm](https://github.com/nvidia/megatron-lm) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · custom license · Oct 2026</sub>

**Distributed training library for large transformer models on NVIDIA GPUs.**

Megatron Core is a Python library of transformer building blocks with tensor, pipeline, data, expert and context parallelism, plus FP16, BF16, FP8 and FP4 mixed precision. The repo also ships Megatron-LM, a reference set of pre-configured training scripts built on it. The README reports training models from 2B to 462B parameters, reaching up to 47% MFU on H100 clusters.

- **+** Supports TP, PP, DP, EP and CP parallelism for multi-node training
- **+** Mixed precision down to FP8 and FP4
- **+** Benchmarked at 462B parameters on 6,144 H100 GPUs, up to 47% MFU
- **+** Includes MoE, hybrid Mamba, post-training and RL code
- **−** Aimed at multi-GPU NVIDIA clusters; not practical for single-machine hobby fine-tuning
- **−** Source builds can run out of memory; MAX_JOBS must be limited
- **−** Python 3.10 support dropped; downstream projects need Python 3.12 or later
- **−** Some features, such as DeepSeek-V4, are only on the experimental dev branch

<sub>GPU required · Docker · Needs PyTorch, NVIDIA GPUs, NGC container (optional) · Models: GPT, Mixture-of-Experts, DeepSeek-V3, Qwen3, Mixtral · [Repo](https://github.com/nvidia/megatron-lm) · [📖 Docs ↗](https://docs.nvidia.com/megatron-core/developer-guide/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/megatron-lm/)</sub>

<a name="minimind"></a>
### #&#8288;8 [minimind](https://github.com/jingyaogong/minimind) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (88) · Freshness: active (85) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Sep 2026</sub>

**Train a 64M-parameter LLM from scratch in plain PyTorch.**

MiniMind is a from-scratch implementation of a small Qwen3-style decoder-only LLM (64M dense, 198M-A64M MoE) with each training stage written in native PyTorch: pretrain, SFT, LoRA, DPO, PPO/GRPO/CISPO, agentic RL and distillation. It ships datasets, a 6,400-token tokenizer, an OpenAI-compatible server and a Streamlit chat UI. The README states one SFT epoch takes about 2 hours on a single 3090.

- **+** Core algorithms (LoRA, DPO, PPO/GRPO) written in plain PyTorch, not wrapped from trl or peft
- **+** Open datasets for each stage, with mini variants (1.2GB pretrain, 1.6GB SFT) for quick runs
- **+** Weights convert to transformers, llama.cpp, vllm and ollama; ollama and vllm usage is documented
- **+** Checkpoint resume, DDP and DeepSpeed multi-GPU, wandb or swanlab logging
- **−** Models are tiny (64M), so output quality is far below mainstream LLMs
- **−** README is primarily in Chinese; the English version is a separate file
- **−** Training data is largely synthetic and distilled, with mixed source licenses
- **−** Native MoE training is about 50% slower than dense, per the README

<sub>GPU optional · Needs PyTorch, transformers, streamlit (optional WebUI), swanlab or wandb (optional) · Models: minimind-3 (64M), minimind-3-moe (198M-A64M), minimind2 series, Transformers format, llama.cpp · [Repo](https://github.com/jingyaogong/minimind) · [▶️ Demo ↗](https://www.modelscope.cn/studios/gongjy/MiniMind) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/minimind/)</sub>

<a name="heretic"></a>
### #&#8288;9 [heretic](https://github.com/p-e-w/heretic) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · AGPL-3.0 · Oct 2026</sub>

**Removes refusal behavior from transformer language models via automated abliteration.**

Heretic applies directional ablation (abliteration) to the attention out-projection and MLP down-projection matrices of a transformer model. An Optuna TPE optimizer searches the ablation parameters, co-minimizing refusals and KL divergence from the original model. After a run it can save the model, upload it to Hugging Face, chat with it, or run benchmarks.

- **+** One command, no configuration needed; Optuna TPE tunes ablation parameters automatically
- **+** README reports 3/100 refusals at 0.16 KL on gemma-3-12b-it, versus 0.45 and 1.04 for manual abliterations
- **+** Supports most dense models, several MoE architectures, and some multimodal and hybrid models
- **+** Optional bitsandbytes 4-bit quantization (bnb_4bit) reduces VRAM needs
- **−** Pure state-space models and some research architectures are not supported out of the box
- **−** AGPL-3.0 license may restrict use in proprietary or networked products
- **−** About 20-30 minutes for a 4B model on an RTX 3090; larger models unknown
- **−** README metrics come from one RTX 5090 setup and may vary by hardware

<sub>GPU optional · Needs Python 3.10+, PyTorch 2.2+, Optuna, bitsandbytes (optional), Hugging Face · Models: Hugging Face transformer models (dense), MoE, multimodal, hybrid (Qwen3.5), MXFP4 (gpt-oss, needs PyTorch 2.6+) · [Repo](https://github.com/p-e-w/heretic) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/heretic/)</sub>

<a name="ms-swift"></a>
### #&#8288;10 [ms-swift](https://github.com/modelscope/ms-swift) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

**Fine-tuning, RL, quantization and serving toolkit for 600+ text and 400+ multimodal LLMs.**

ms-swift is a Python framework from the ModelScope community for training, evaluating, quantizing and serving LLMs and multimodal models through the `swift` CLI, a Gradio Web-UI or Python. It covers LoRA/QLoRA and full-parameter SFT, DPO/KTO and GRPO-family reinforcement learning, with Megatron parallelism (TP/PP/CP/EP) for large and MoE models. Inference and deployment run on Transformers, vLLM, SGLang or LMDeploy, and evaluation uses EvalScope.

- **+** Covers SFT, DPO/KTO/RM, GRPO variants, embedding and reranker training in one CLI
- **+** Megatron TP/PP/CP/EP support for full-parameter and LoRA training of MoE models
- **+** Runs on NVIDIA CUDA, AMD ROCm, Ascend NPU, Apple MPS and CPU
- **+** Quick start LoRA-tunes Qwen3-4B in about 13GB on a single 3090
- **−** Large dependency matrix (torch, transformers, peft, trl, deepspeed, vllm) with version pins
- **−** No Docker image or compose file in the README
- **−** Downloads models and datasets from ModelScope by default; Hugging Face needs --use_hf true
- **−** 4.x/3.x split; the older 3.x line requires checking out a release branch

<sub>GPU optional · Needs PyTorch, transformers, peft, modelscope, datasets, DeepSpeed (training), vLLM/SGLang/LMDeploy (inference), EvalScope (evaluation), Gradio (Web-UI) · Models: Qwen3, Qwen3-VL, Llama4, DeepSeek-R1, GLM4.5 · [Repo](https://github.com/modelscope/ms-swift) · [📖 Docs ↗](https://swift.readthedocs.io/en/latest/) · [🌐 Site ↗](https://modelscope.cn/home) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ms-swift/)</sub>

<a name="fingpt"></a>
### #&#8288;11 [fingpt](https://github.com/ai4finance-foundation/fingpt) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (46) · Freshness: active (99) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Sep 2026</sub>

**LoRA fine-tuned financial LLMs, datasets and notebooks for sentiment and forecasting.**

FinGPT is a collection of LoRA adapters, instruction datasets and training notebooks for financial NLP tasks such as sentiment analysis, relation extraction, headline classification, NER and stock-movement forecasting. Adapters are published on Hugging Face for Llama2, Falcon, BLOOM, MPT, ChatGLM2 and Qwen bases. The README reports a Llama2-13B sentiment adapter trained on one RTX 3090 in about 17 hours.

- **+** Published LoRA adapters and datasets on Hugging Face for several base models
- **+** Notebooks fine-tune on a single RTX 3090 in 8-bit or int4 QLoRA
- **+** Benchmark table reports weighted F1 on FPB, FiQA-SA, TFNS and NWGI with cost per run
- **+** Forecaster has a hosted Hugging Face Space demo, so no install is needed to try it
- **−** Forecaster is trained on US DOW 30 data only; other markets need your own data and fine-tuning
- **−** Most releases date from 2023 and use older bases such as Llama2 and ChatGLM2
- **−** Research and notebook code, not a packaged app or service; no Docker setup
- **−** Cost comparisons with BloombergGPT rely on the project's own GPU-hour assumptions

<sub>GPU optional · Needs Hugging Face Transformers, PEFT, OpenAI API (optional cloud provider) · Models: Llama2-7B, Llama2-13B, Falcon-7B, BLOOM-7B1, MPT-7B · [Repo](https://github.com/ai4finance-foundation/fingpt) · [▶️ Demo ↗](https://huggingface.co/spaces/FinGPT/FinGPT-Forecaster) · [🌐 Site ↗](https://ai4finance.org/research/fingpt-open-source-finllm.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fingpt/)</sub>

<a name="colossalai"></a>
### #&#8288;12 [colossalai](https://github.com/hpcaitech/colossalai) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (74) · Freshness: recent (73) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Oct 2026</sub>

**Distributed training library for large models with many parallelism strategies.**

Colossal-AI is a PyTorch-based library for training and running large models across multiple GPUs. It provides data, pipeline, 1D/2D/2.5D/3D tensor and sequence parallelism, ZeRO, auto-parallelism and heterogeneous memory management. The repo also hosts example applications such as Colossal-LLaMA-2, ColossalChat (RLHF) and Stable Diffusion acceleration, plus an inference module.

- **+** Covers data, pipeline, tensor (1D to 3D), sequence parallelism and ZeRO in one library
- **+** Published benchmarks for 7B and 70B Llama-like models on H200 and B200 GPUs
- **+** Includes worked applications: Colossal-LLaMA-2, ColossalChat RLHF, Stable Diffusion training
- **+** Apache-2.0 license, with a Dockerfile and PyPI install
- **−** Last tagged release is 2025-06-04, older than recent commits
- **−** README is heavily promotional for the vendor's GPU cloud and model APIs
- **−** Multi-GPU focus; RAM and minimum GPU requirements are not stated in the README
- **−** Many example sections are dated, with news items ending in 2025

<sub>GPU required · Docker · Needs PyTorch · Models: Llama, Open-Sora, Stable Diffusion, GPT-2, GPT-3 · [Repo](https://github.com/hpcaitech/colossalai) · [▶️ Demo ↗](https://colossalai.org/zh-Hans/docs/get_started/bonus/) · [📖 Docs ↗](https://www.colossalai.org/) · [🌐 Site ↗](https://www.colossalai.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/colossalai/)</sub>

<a name="agent-lightning"></a>
### #&#8288;13 [agent-lightning](https://github.com/microsoft/agent-lightning) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (35) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

**Reinforcement learning framework for training agents through a model-request proxy.**

Agent Lightning is a roughly 3,500-line Python framework that trains agents with RL while they run in their real harnesses. A gateway proxies the agent's model requests and records them as training data, a rollout controller runs agents locally or as Kubernetes Jobs, and a trainer built on verl and vLLM updates the policy. Examples include a Qwen3.5-9B coding agent, which the README reports going from 41.8% to 56.4% on SWE-bench Verified.

- **+** Agents run unchanged; the gateway captures model calls as training data
- **+** Runs rollouts as Kubernetes Jobs without an external sandbox service
- **+** Full coding-agent pipeline released: data cleaning, reward-hacking prevention, training scripts
- **+** Examples cover Calc-X, GSM8K, ScienceWorld, Search-R1, LLM-in-Sandbox and coding agents
- **−** Requires a verl and vLLM GPU stack; install shown for CUDA 13.0 only
- **−** No Docker or compose setup shipped in the repo
- **−** v1.0 is a full refactor; older releases live on a separate v0.x branch
- **−** Hardware and RAM requirements are not stated in the README

<sub>GPU required · Needs verl, vLLM, uv, Kubernetes (optional, for rollouts) · Models: Qwen3.5-9B, Qwen3.5-35B-A3B · [Repo](https://github.com/microsoft/agent-lightning) · [📖 Docs ↗](https://microsoft.github.io/agent-lightning/stable/) · [🌐 Site ↗](https://www.microsoft.com/en-us/research/project/agent-lightning/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-lightning/)</sub>

<a name="weclone"></a>
### #&#8288;14 [weclone](https://github.com/xming521/weclone) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: known (32) · Freshness: active (91) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · AGPL-3.0 · Oct 2026</sub>

**Fine-tunes a Qwen VL model on your Telegram chats to build a chat avatar.**

WeClone exports Telegram chat history, strips personal data with Microsoft Presidio and a blocklist, then LoRA fine-tunes Qwen2.5-VL-7B-Instruct through LLaMA Factory. The tuned model is served as an OpenAI-style API (README example port 8005) and can be connected through AstrBot or LangBot to Telegram, Discord or Slack. Personal WeChat deployment is listed, based on openclaw-weixin.

- **+** Covers the full pipeline: export, PII filtering, LoRA training, API serving, bot deployment
- **+** Presidio redaction plus a manual blocked_words list; encrypted storage default in new templates
- **+** Handles image data; other models usable through LLaMA Factory
- **+** QLoRA 4-bit on a 7B model needs about 6GB VRAM per the README table
- **−** Only Telegram works as a data source; WhatsApp, Discord and Slack imports are marked planned
- **−** README says 7B results are average; 14B or larger works better
- **−** Fine-tuned model has no tool calling; AstrBot tools must be turned off
- **−** Requires CUDA 12.6+; Windows not rigorously tested (WSL suggested)

<sub>GPU required · Needs CUDA 12.6+, LLaMA Factory, Microsoft Presidio, uv, AstrBot or LangBot (for chat bots) · Models: Qwen2.5-VL-7B-Instruct, LLaMA Factory supported models, LoRA, QLoRA · port 8005 · [Repo](https://github.com/xming521/weclone) · [📖 Docs ↗](https://docs.weclone.love/docs/introduce/what-is-weclone.html) · [🌐 Site ↗](https://www.weclone.love/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/weclone/)</sub>

<a name="nanochat"></a>
### #&#8288;15 [nanochat](https://github.com/karpathy/nanochat) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: widely used (84) · Freshness: active (93) · Maintenance: weak (2) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Jul 2026</sub>

**Minimal PyTorch codebase to train and chat with a small GPT-2-class LLM.**

nanochat covers tokenizer training, pretraining, SFT, RL, evaluation and a CLI chat interface in one small Python codebase. A single `--depth` setting derives width, heads, learning rate and training horizon, so one knob produces a compute-optimal model series. The reference speedrun trains a GPT-2-grade model in about 1.65 hours on an 8xH100 node per the leaderboard.

- **+** Covers tokenizer, pretraining, SFT, RL, eval and inference in one repo
- **+** Single `--depth` dial sets all other hyperparameters automatically
- **+** Public time-to-GPT-2 leaderboard with commits and CORE scores
- **+** Same scripts run on one GPU via gradient accumulation, or on CPU/MPS
- **−** Reference speedrun needs an 8xH100 node, roughly $48 of rented compute
- **−** Under 80GB VRAM requires manually lowering `--device-batch-size`
- **−** CPU/MPS path only trains a tiny model with weak results
- **−** Chat is CLI-only in the README; resulting model is small and hallucinates

<sub>GPU required · Needs PyTorch, uv, wandb · Models: nanochat GPT (depth-scaled), bfloat16, float32, float16 · [Repo](https://github.com/karpathy/nanochat) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nanochat/)</sub>

<a name="ml-agents"></a>
### #&#8288;16 [ml-agents](https://github.com/unity-technologies/ml-agents) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: known (42) · Freshness: active (81) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Oct 2026</sub>

**Train game agents with reinforcement learning inside Unity environments.**

Unity SDK plus a PyTorch-based Python trainer that turns Unity scenes into reinforcement learning environments. It ships PPO, SAC, MA-POCA and self-play, plus BC and GAIL imitation learning, and exposes environments through a Python API, Gym and PettingZoo wrappers. Trained policies run in-game through Unity's Inference Engine.

- **+** Ships PPO, SAC, MA-POCA, self-play, BC and GAIL trainers out of the box
- **+** Gym and PettingZoo wrappers plus a low-level Python API for custom training code
- **+** 17+ example Unity environments and curriculum learning and environment randomization support
- **+** Trained models run natively in Unity across platforms via the Inference Engine
- **−** Requires the Unity editor and a Unity project; not usable standalone
- **−** Last tagged release is from 2025; develop branch is described as unstable
- **−** Web docs are deprecated; docs live in the Unity package documentation
- **−** License shown as NOASSERTION by detection, while the README badge says Apache-2.0

<sub>GPU optional · Docker · Needs Unity (2020.1 or later), Python, PyTorch · Models: PPO, SAC, MA-POCA, BC, GAIL · [Repo](https://github.com/unity-technologies/ml-agents) · [📖 Docs ↗](https://docs.unity3d.com/Packages/com.unity.ml-agents@latest) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ml-agents/)</sub>

<a name="litgpt"></a>
### #&#8288;17 [litgpt](https://github.com/lightning-ai/litgpt) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Sep 2026</sub>

**PyTorch LLM implementations with recipes to pretrain, finetune, evaluate and serve.**

LitGPT reimplements 20+ open LLM families (Llama, Gemma, Phi, Qwen, Mistral and others) from scratch in PyTorch, without abstraction layers. A single CLI covers download, chat, finetune (LoRA, QLoRA, adapter), pretrain, continued pretraining, evaluate and serve, plus a Python `LLM` API. Training supports FSDP, flash attention and reduced precision (fp4/8/16/32) across 1 to 1000+ GPUs or TPUs.

- **+** Single CLI covers download, finetune, pretrain, evaluate, chat and serve
- **+** Readable single-file model implementations, easy to debug and modify
- **+** Supports LoRA, QLoRA, adapter finetuning and full pretraining from scratch
- **+** Apache-2.0 license with YAML training recipes
- **−** Built-in `litgpt serve` exposes a simple /predict endpoint, not documented as OpenAI-compatible
- **−** Only the listed model families are supported; new architectures need code added
- **−** No Docker or compose files in the repo
- **−** README promotes Lightning Cloud for GPUs; hardware requirements per model not stated

<sub>GPU optional · Needs PyTorch, Hugging Face Hub (weight download) · Models: Llama 2/3.x, Gemma 1/2/3, Phi 1.5-4, Qwen2.5/Qwen3, Mistral/Mixtral · port 8000 · [Repo](https://github.com/lightning-ai/litgpt) · [🌐 Site ↗](https://lightning.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/litgpt/)</sub>

<a name="easy-dataset"></a>
### #&#8288;18 [easy-dataset](https://github.com/conardli/easy-dataset) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (18) · Freshness: recent (78) · Maintenance: weak (4) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · May 2026</sub>

**Turns documents into LLM fine-tuning and evaluation datasets.**

Easy Dataset parses PDF, Markdown, DOCX, TXT and EPUB files, splits them into chunks, and uses an LLM to generate questions, answers and chain-of-thought for single-turn, multi-turn or image QA datasets. It also builds evaluation sets with a judge model and a double-blind arena, and exports to Alpaca or ShareGPT, LLaMA Factory configs, or Hugging Face. It runs as a web app on port 1717 or as a desktop client.

- **+** Covers raw documents to Alpaca/ShareGPT export in JSON or JSONL
- **+** Generates evaluation sets with judge-model scoring and a human blind test arena
- **+** Works with any OpenAI-format API, plus Ollama for local models
- **+** Generates LLaMA Factory configs and uploads to Hugging Face Hub
- **−** AGPL-3.0 license restricts closed-source network deployment
- **−** Output quality depends on an external LLM API or separate local model server
- **−** Many tutorials and community guides are Chinese-language video or wiki links
- **−** Local database file storage; no multi-user setup described

<sub>no GPU · Docker + Compose · Needs OpenAI-compatible LLM API or Ollama · Models: OpenAI-compatible APIs, Ollama, OpenRouter, Zhipu AI, Alibaba Bailian · port 1717 · [Repo](https://github.com/conardli/easy-dataset) · [📖 Docs ↗](https://docs.easy-dataset.com/ed/en) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/easy-dataset/)</sub>

<a name="paddlenlp"></a>
### #&#8288;19 [paddlenlp](https://github.com/paddlepaddle/paddlenlp) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: niche (8) · Freshness: recent (55) · Maintenance: weak (18) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · May 2026</sub>

**LLM training, fine-tuning, compression and inference toolkit on PaddlePaddle.**

PaddleNLP is a Python toolkit built on PaddlePaddle for pretraining, fine-tuning, quantizing and serving LLMs. It supports 4D parallel training, Unified Checkpoint for elastic resume, FlashMask-based fine-tuning, and inference with FP8, INT8 and 4-bit quantization. Hardware targets include NVIDIA GPU, Kunlun XPU, Ascend NPU, Enflame GCU and Hygon DCU.

- **+** Runs on NVIDIA GPU plus Kunlun XPU, Ascend NPU, Enflame GCU and Hygon DCU
- **+** Trainer configures data, sharded, tensor and pipeline parallelism through settings
- **+** Unified Checkpoint allows resume after cluster resizing; README claims 78.5% smaller checkpoints
- **+** Covers Llama, Qwen, DeepSeek V3/R1, ChatGLM, Baichuan, Gemma, Mistral and others
- **−** Tied to PaddlePaddle, so it sits outside the PyTorch ecosystem
- **−** Main README is in Chinese; English version is a separate file
- **−** Last release was 2024-12-16, while the news list covers later model support
- **−** No Docker or compose files detected in the repo

<sub>GPU optional · Needs PaddlePaddle · Models: Llama, Qwen, DeepSeek V2/V3/R1, ChatGLM, Baichuan · [Repo](https://github.com/paddlepaddle/paddlenlp) · [📖 Docs ↗](https://paddlenlp.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddlenlp/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
