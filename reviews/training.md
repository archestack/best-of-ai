# 🏋️ Training and fine-tuning reviews · Best of Open-Source AI

Tools to fine-tune, train or distill models on your own data and GPUs, from LoRA scripts to full training stacks. Back to the [leaderboard](../README.md#%EF%B8%8F-training-and-fine-tuning).

<sub>🌐 Also on the web: [Training and fine-tuning on archestack.com](https://archestack.com/best-of-ai/training/), each project on its own page.</sub>

<a name="llamafactory"></a>
### 🥇 [llamafactory](https://github.com/hiyouga/llamafactory) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 75k · Apache-2.0 · Oct 2026</sub>

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

<a name="minimind"></a>
### 🥈 [minimind](https://github.com/jingyaogong/minimind) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (38) · Freshness: active (85) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Sep 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
