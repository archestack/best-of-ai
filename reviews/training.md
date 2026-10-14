# 🏋️ Training and fine-tuning reviews · Best of Open-Source AI

Tools to fine-tune, train or distill models on your own data and GPUs, from LoRA scripts to full training stacks. Back to the [leaderboard](../README.md#%EF%B8%8F-training-and-fine-tuning).

<sub>🌐 Also on the web: [Training and fine-tuning on archestack.com](https://archestack.com/best-of-ai/training/), each project on its own page.</sub>

<a name="llamafactory"></a>
### 🥇 [llamafactory](https://github.com/hiyouga/llamafactory) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 75k · Apache-2.0 · Oct 2026</sub>

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

<a name="deepspeed"></a>
### 🥈 [deepspeed](https://github.com/deepspeedai/deepspeed) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Oct 2026</sub>

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

<a name="minimind"></a>
### 🥉 [minimind](https://github.com/jingyaogong/minimind) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (78) · Freshness: active (85) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Sep 2026</sub>

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

<a name="nanochat"></a>
### #&#8288;4 [nanochat](https://github.com/karpathy/nanochat) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: popular (63) · Freshness: active (95) · Maintenance: weak (2) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Jul 2026</sub>

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

<a name="colossalai"></a>
### #&#8288;5 [colossalai](https://github.com/hpcaitech/colossalai) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: known (32) · Freshness: recent (74) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Oct 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
