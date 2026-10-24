# 🏋️ Training and fine-tuning reviews · Best of Open-Source AI

Tools to fine-tune, train or distill models on your own data and GPUs, from LoRA scripts to full training stacks. Back to the [leaderboard](../README.md#%EF%B8%8F-training-and-fine-tuning).

<sub>🌐 Also on the web: [Training and fine-tuning on archestack.com](https://archestack.com/best-of-ai/training/), each project on its own page.</sub>

<a name="unsloth"></a>
### 🥇 [unsloth](https://github.com/unslothai/unsloth) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · Apache-2.0 · Oct 2026</sub>

**Desktop and web app to run and fine-tune local models.**

Unsloth ships as a native desktop app, a web UI (Unsloth Studio) and a Python library (Unsloth Core). It runs GGUF, MLX, diffusion, audio and embedding models, serves them over an OpenAI-compatible API, and fine-tunes them with LoRA, QLoRA, full fine-tuning, GRPO, DPO and FP8. The README claims 2x faster training with 70% less VRAM.

- **+** Covers both running and fine-tuning models, with export to GGUF, NVFP4 and FP8
- **+** Supports NVIDIA, AMD, Intel GPUs, CPU and Vulkan on Windows, Linux, WSL and macOS
- **+** Free Colab and Kaggle notebooks for many models, including GRPO and TTS
- **+** `unsloth start` connects Claude Code, Codex and other agents to local models
- **−** Speed and VRAM figures (2x, 70% less) are the project's own claims
- **−** Server-side tools are on by default; exposing it needs a password or --disable-tools
- **−** Three install paths (Desktop, Studio, Core) with many environment flags add complexity
- **−** RAM and VRAM minimums are not stated in the README

<sub>GPU optional · Docker · Needs PyTorch, llama.cpp, Cloudflare (optional remote access), Docker (optional) · Models: GGUF, MLX, LLMs, diffusion, audio/TTS · port 8000 · [Repo](https://github.com/unslothai/unsloth) · [▶️ Demo ↗](https://colab.research.google.com/github/unslothai/unsloth/blob/main/studio/Unsloth_Studio_Colab.ipynb) · [📖 Docs ↗](https://unsloth.ai/docs) · [🌐 Site ↗](https://unsloth.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unsloth/)</sub>

<a name="deepspeed"></a>
### 🥈 [deepspeed](https://github.com/deepspeedai/deepspeed) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Oct 2026</sub>

**PyTorch library for distributed training of very large models with ZeRO.**

DeepSpeed is a PyTorch library that makes large-model training fit and scale across GPUs using ZeRO, ZeRO-Infinity offload, 3D parallelism, Ulysses sequence parallelism and DeepSpeed-MoE. It is configured through a JSON file and integrates with Hugging Face Transformers, Accelerate, Lightning, MosaicML Composer, Determined and MMEngine. C++/CUDA ops are built just-in-time with ninja by default.

- **+** Used to train models such as BLOOM 176B and Megatron-Turing NLG 530B
- **+** Integrates with Hugging Face Transformers and Accelerate, Lightning, Composer and Determined
- **+** Supports NVIDIA, AMD, Intel Gaudi and XPU, Huawei Ascend NPU and CPU accelerators
- **+** Installs with pip install deepspeed; ds_report checks which ops are compatible
- **−** PyTorch must be installed first, and a CUDA or ROCm compiler is needed for JIT ops
- **−** Windows lacks async IO and GDS support
- **−** Tested mainly on NVIDIA Pascal to Hopper and AMD MI100/MI200; other hardware is less validated
- **−** Training-focused; tuning requires understanding the JSON config and ZeRO stages

<sub>GPU optional · Docker · Needs PyTorch, CUDA or ROCm compiler (nvcc/hipcc), ninja · Models: PyTorch models, Hugging Face Transformers · [Repo](https://github.com/deepspeedai/deepspeed) · [📖 Docs ↗](https://www.deepspeed.ai/getting-started/) · [🌐 Site ↗](https://www.deepspeed.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepspeed/)</sub>

<a name="verl"></a>
### 🥉 [verl](https://github.com/verl-project/verl) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;4 [peft](https://github.com/huggingface/peft) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Oct 2026</sub>

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

<a name="trl"></a>
### #&#8288;5 [trl](https://github.com/huggingface/trl) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;6 [megatron-lm](https://github.com/nvidia/megatron-lm) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · custom license · Oct 2026</sub>

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

<a name="axolotl"></a>
### #&#8288;7 [axolotl](https://github.com/axolotl-ai-cloud/axolotl) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**YAML-driven fine-tuning framework for LLMs with LoRA, QLoRA, RL and multi-GPU.**

Axolotl runs LLM post-training from a single YAML config covering dataset preprocessing, training, evaluation, quantization and inference. It supports full fine-tuning, LoRA/QLoRA, QAT, DPO/KTO/ORPO, GRPO and reward modelling, with FSDP2, DeepSpeed, and Torchrun or Ray multi-node. Models come from the Hugging Face Hub, including multimodal and audio ones.

- **+** One YAML config reused across preprocessing, training, evaluation, quantization and inference
- **+** Broad methods: full FT, LoRA/QLoRA, QAT, DPO/KTO/ORPO, GRPO, reward models
- **+** Multi-GPU and multi-node via FSDP2, DeepSpeed, Torchrun and Ray, plus context and expert parallelism
- **+** Fast model support updates; GGUF export via `axolotl export` for llama.cpp and Ollama
- **−** Requires NVIDIA (Ampere or newer for bf16) or AMD GPU; no CPU path stated
- **−** Needs Python 3.12+ and PyTorch 2.13+, a narrow environment
- **−** Configuration surface is large; many options and fast-moving features
- **−** No web UI; command-line and YAML only

<sub>GPU required · Compose · Needs PyTorch, Hugging Face Hub, DeepSpeed (optional), uv · Models: Llama, Mistral, Mixtral, GPT-OSS, Qwen · [Repo](https://github.com/axolotl-ai-cloud/axolotl) · [▶️ Demo ↗](https://colab.research.google.com/github/axolotl-ai-cloud/axolotl/blob/main/examples/colab-notebooks/colab-axolotl-example.ipynb) · [📖 Docs ↗](https://docs.axolotl.ai/docs/getting-started.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/axolotl/)</sub>

<a name="ms-swift"></a>
### #&#8288;8 [ms-swift](https://github.com/modelscope/ms-swift) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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

<a name="llamafactory"></a>
### #&#8288;9 [llamafactory](https://github.com/hiyouga/llamafactory) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: patchy (39) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 76k · Apache-2.0 · Oct 2026</sub>

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

<a name="soup"></a>
### #&#8288;10 [soup](https://github.com/makazhanalpamys/soup) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

**CLI for fine-tuning and post-training LLMs from a single YAML config.**

Soup is a Python CLI that runs LoRA/QLoRA fine-tuning and preference or RL post-training (SFT, DPO, GRPO, PPO, KTO, ORPO and others) from one soup.yaml. It also covers batch inference, an OpenAI-compatible server, merge and GGUF export, and a local web dashboard. An opt-in beta layer-streaming mode trains an 8B NF4 model in about 3.3 GB peak VRAM.

- **+** Many tasks in one config: SFT, DPO, GRPO, PPO, KTO, ORPO, SimPO, IPO, vision, audio
- **+** Layer streaming trains Llama-3.1-8B NF4 in 3.32 GB peak on a 4 GB laptop GPU
- **+** Same tool merges adapters, exports GGUF, serves an OpenAI-compatible API, has a web UI
- **+** Light install without PyTorch for data tools; 100+ ready-made model recipes
- **−** Python 3.10-3.12 only; 3.13+ is unsupported
- **−** Layer streaming is opt-in and still beta; a correctness repair changed its benchmark numbers
- **−** Recent releases are breaking: unused settings and unknown config keys now fail at load
- **−** AWQ and GPTQ export are deprecated and slated for removal in v0.77

<sub>GPU optional · Docker + Compose · Needs PyTorch, transformers, peft, trl, HuggingFace Hub · Models: HuggingFace Hub causal LMs, Llama 3.x/4, Qwen 2.5/3, Gemma 3, Mistral · port 7860 · [Repo](https://github.com/makazhanalpamys/soup) · [🌐 Site ↗](https://trysoup.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/soup/)</sub>

<a name="heretic"></a>
### #&#8288;11 [heretic](https://github.com/p-e-w/heretic) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · AGPL-3.0 · Oct 2026</sub>

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

<a name="agent-lightning"></a>
### #&#8288;12 [agent-lightning](https://github.com/microsoft/agent-lightning) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

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

<a name="fingpt"></a>
### #&#8288;13 [fingpt](https://github.com/ai4finance-foundation/fingpt) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (69) · Freshness: active (98) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Sep 2026</sub>

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

<a name="oumi"></a>
### #&#8288;14 [oumi](https://github.com/oumi-ai/oumi) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · Apache-2.0 · Oct 2026</sub>

**CLI and Python toolkit for fine-tuning, evaluating and deploying foundation models.**

Oumi covers the model lifecycle from one YAML-driven CLI: data synthesis with LLM judges, training (SFT, LoRA, QLoRA, DPO, GRPO), evaluation, and inference through vLLM, SGLang or commercial APIs. Recent versions add tool-calling SFT, executable tool environments and GRPO via verl. Jobs can run locally or be launched on AWS, Azure, GCP, Lambda, Modal or Slurm. The README labels it beta.

- **+** Ready-made YAML recipes for many model families (Qwen, Gemma, Llama, gpt-oss, Phi)
- **+** Supports SFT, LoRA, QLoRA, DPO, KTO and GRPO, with FSDP, DeepSpeed and DDP
- **+** `oumi launch` runs jobs on AWS, Azure, GCP, Lambda and Slurm
- **+** Includes eval, LLM-as-judge, data synthesis and an `oumi-mcp` MCP server
- **−** README says beta; some advanced features may change
- **−** Broad scope means many dependencies (Transformers, TRL, vLLM, verl) to keep aligned
- **−** GPU extras needed for most real training; hardware requirements not stated
- **−** Dedicated endpoint deploy targets specific providers (Fireworks, Parasail)

<sub>GPU optional · Docker · Needs PyTorch, Transformers, TRL, vLLM, SGLang, verl · Models: Llama, Gemma, Qwen, DeepSeek, GLM · [Repo](https://github.com/oumi-ai/oumi) · [📖 Docs ↗](https://oumi.ai/docs/en/latest/index.html) · [🌐 Site ↗](https://oumi.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/oumi/)</sub>

<a name="openrlhf"></a>
### #&#8288;15 [openrlhf](https://github.com/openrlhf/openrlhf) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (39) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Sep 2026</sub>

**Ray and vLLM based RLHF training framework for LLMs and VLMs.**

OpenRLHF trains language and vision-language models with reinforcement learning from human feedback. It uses Ray to schedule actor, reward, reference and critic models across GPUs, vLLM for sample generation, and DeepSpeed ZeRO-3 for training. It implements PPO, REINFORCE++, GRPO and RLOO, plus SFT, DPO and reward model training, with single-turn or multi-turn agent rollouts.

- **+** Several RL algorithms (PPO, REINFORCE++, GRPO, RLOO) selectable via one estimator flag
- **+** Hybrid engine lets models and vLLM share GPUs; README cites 70B+ scale
- **+** Multi-turn agent mode with reset/step environments, async training and VLM support
- **+** Also covers SFT, DPO and reward models, with LoRA/QLoRA and sample packing
- **−** Needs NVIDIA GPUs and a Ray, vLLM and DeepSpeed stack; setup is involved
- **−** README recommends a specific NVIDIA PyTorch container and removing conflicting pip packages
- **−** Large CLI flag surface; configuration lives mostly in example shell scripts
- **−** Hardware requirements per model size are not stated in the README

<sub>GPU required · Needs Ray, vLLM, DeepSpeed, HuggingFace Transformers, NCCL · Models: HuggingFace Transformers models, VLMs (e.g. Qwen3.5), MoE, LoRA/QLoRA · [Repo](https://github.com/openrlhf/openrlhf) · [📖 Docs ↗](https://openrlhf.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openrlhf/)</sub>

<a name="minimind"></a>
### #&#8288;16 [minimind](https://github.com/jingyaogong/minimind) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (92) · Freshness: active (84) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Sep 2026</sub>

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

<a name="weclone"></a>
### #&#8288;17 [weclone](https://github.com/xming521/weclone) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (62) · Freshness: active (91) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · AGPL-3.0 · Oct 2026</sub>

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

<a name="ludwig"></a>
### #&#8288;18 [ludwig](https://github.com/ludwig-ai/ludwig) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (44) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Sep 2026</sub>

**YAML-configured training and fine-tuning for LLMs, multimodal and tabular models.**

Ludwig trains, fine-tunes and serves models from a YAML config and a CLI, with no training loop code. It covers LLM fine-tuning (SFT, DPO, KTO, ORPO, GRPO, LoRA and other PEFT adapters, 4-bit QLoRA, torchao QAT), plus multimodal, tabular, timeseries and image models. Runs scale from local to multi-GPU and Ray clusters by changing the backend setting.

- **+** Whole experiment defined in one YAML file; ludwig train, predict and serve cover the workflow
- **+** Wide LLM tuning coverage: SFT, DPO, KTO, ORPO, GRPO, many PEFT adapters, QLoRA
- **+** Mixes text, image, audio, number and timeseries inputs in one config
- **+** Distributed training via Accelerate (DDP, FSDP, DeepSpeed) and Ray; Optuna and Ray Tune for HPO
- **−** Requires Python 3.12+ and recent PyTorch, Transformers and Ray versions
- **−** Config schema is large; advanced options need reading the docs
- **−** Gated base models such as Llama need a Hugging Face token
- **−** GPU, VRAM and RAM requirements are not stated in the README

<sub>GPU optional · Docker · Needs PyTorch 2.7+, Transformers 5, Ray 2.54, Hugging Face Hub token (gated models) · Models: Hugging Face Transformers, LoRA, QLoRA, DoRA, VeRA · port 8000 · [Repo](https://github.com/ludwig-ai/ludwig) · [📖 Docs ↗](https://ludwig.ai/latest/getting_started/) · [🌐 Site ↗](https://ludwig.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ludwig/)</sub>

<a name="slime"></a>
### #&#8288;19 [slime](https://github.com/thudm/slime) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · Apache-2.0 · Oct 2026</sub>

**RL post-training framework connecting Megatron training with SGLang rollout.**

slime is a reinforcement-learning post-training framework for LLMs. It runs Megatron for training and SGLang for rollout generation, coordinated by Ray and a shared Data Buffer. Custom generate functions, reward functions, verifiers and environments plug in through documented interfaces. The README says it is the RL framework behind the GLM-4.5 through GLM-5.3 releases.

- **+** Used for RL training of GLM-4.5 through GLM-5.3, per the README
- **+** Megatron args pass through directly; SGLang args use the --sglang- prefix
- **+** Custom generate and reward hooks cover multi-turn, tool-use and agentic rollouts
- **+** Supports fully async rollout, PD disaggregation, delta weight sync, external rollout engines
- **−** Requires Megatron, SGLang and Ray together; setup is involved
- **−** No Dockerfile or compose file detected in the repository
- **−** Hardware, RAM and VRAM requirements are not stated in the README
- **−** Aimed at multi-GPU RL runs, not small single-machine fine-tuning

<sub>GPU required · Docker · Needs Megatron-LM, SGLang, Ray · Models: GLM, Qwen3.8, Qwen3.6, Qwen3.5, Qwen3-Next · [Repo](https://github.com/thudm/slime) · [📖 Docs ↗](https://thudm.github.io/slime/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/slime/)</sub>

<a name="liger-kernel"></a>
### #&#8288;20 [liger-kernel](https://github.com/linkedin/liger-kernel) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.7k · BSD-2-Clause · Oct 2026</sub>

**Triton kernels that cut memory and raise throughput for LLM training.**

Liger Kernel is a PyTorch library of Triton kernels for RMSNorm, RoPE, SwiGLU, CrossEntropy and FusedLinearCrossEntropy, plus chunked post-training losses such as DPO, ORPO, SimPO, KTO and JSD. A one-line patch swaps them into Hugging Face models. The README reports about 20% higher multi-GPU throughput and 60% lower memory on LLaMA 3-8B, with exact (non-approximated) computation.

- **+** One-line patching of Hugging Face models; also usable as standalone modules
- **+** Works with FSDP, DeepSpeed and DDP, and integrates with Axolotl, LLaMA-Factory and TRL
- **+** Exact computation, checked by unit and convergence tests against runs without Liger
- **+** Chunked post-training losses (DPO, ORPO, SimPO, KTO) claim up to 80% memory savings
- **−** Benchmarks come from one setup: LLaMA 3-8B on 8 A100s with FSDP1
- **−** Model patching APIs need transformers >= 5.0.0, and per-model support varies
- **−** cuTile and CuTe DSL backends are opt-in and CUDA-only, with newer-GPU targets (Hopper, Blackwell)
- **−** Training-side only; it does not serve or run inference

<sub>GPU required · Needs torch >= 2.1.2, triton >= 2.3.1, transformers >= 5.0.0 (optional) · Models: Hugging Face transformers models, LLaMA 3, Qwen2-VL, Llama 3.2-Vision · [Repo](https://github.com/linkedin/liger-kernel) · [📖 Docs ↗](https://linkedin.github.io/Liger-Kernel/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/liger-kernel/)</sub>

<a name="areal"></a>
### #&#8288;21 [areal](https://github.com/areal-project/areal) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

**Asynchronous reinforcement learning system for training reasoning and agentic LLMs.**

AReaL trains LLMs with reinforcement learning using a fully asynchronous rollout and training loop. It ships GRPO, PPO, DAPO, GSPO, DPO, SFT and related algorithms, with SGLang or vLLM for inference and Megatron or PyTorch FSDP for training. Agentic RL works with black-box agents by pointing them at an AReaL endpoint through base_url.

- **+** Asynchronous RL; setting max_head_offpolicyness=0 gives the synchronous variant
- **+** Many algorithms with example configs: GRPO, GSPO, PPO, DAPO, RLOO, M2PO, DPO, SFT
- **+** Agentic RL for existing agents by swapping base_url; examples for SWE, search and tau2
- **+** Backends: SGLang or vLLM inference; Megatron, FSDP or Archon training; Ray and local schedulers
- **−** Needs CUDA GPUs; install requires a matching flash-attn wheel
- **−** Model support varies by training backend; other Hugging Face LLMs only on FSDP
- **−** 2.0 microservice refactor and v1/v2 options add configuration complexity
- **−** Ascend NPU support lives on a separate branch

<sub>GPU required · Docker · Needs SGLang or vLLM, Megatron or PyTorch FSDP, flash-attn, Ray (optional) · Models: Qwen2/3, Qwen3-MoE, Qwen3.5, Qwen2.5-VL, Qwen3-VL · [Repo](https://github.com/areal-project/areal) · [📖 Docs ↗](https://areal-project.github.io/AReaL/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/areal/)</sub>

<a name="colossalai"></a>
### #&#8288;22 [colossalai](https://github.com/hpcaitech/colossalai) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: widely used (85) · Freshness: recent (73) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Oct 2026</sub>

**Distributed training library for large models with many parallelism strategies.**

Colossal-AI is a PyTorch-based library for distributed training and inference of large models. It provides data, pipeline, 1D/2D/2.5D/3D tensor and sequence parallelism, ZeRO, auto-parallelism and heterogeneous memory management. The repo also hosts applications such as Colossal-LLaMA-2, ColossalChat (RLHF) and Stable Diffusion acceleration examples.

- **+** Covers data, pipeline, tensor (1D to 3D), sequence parallelism and ZeRO in one library
- **+** Includes worked examples for LLaMA, GPT-2/3, BERT, ViT, MoE and Stable Diffusion
- **+** Publishes H200 and B200 benchmarks for 7B and 70B Llama-like training with parallel configs
- **+** Ships reference apps: Colossal-LLaMA-2 weights, ColossalChat RLHF pipeline
- **−** README opens with HPC-AI Cloud and Model API promotions, mixed into the project docs
- **−** Last tagged release is 2025-06-04, well behind recent commits
- **−** Benchmarks are vendor-run; no comparison against other training frameworks in the visible README
- **−** Many news and example items date from 2023-2024 and may be stale

<sub>GPU required · Docker · Needs PyTorch · Models: LLaMA, GPT-2, GPT-3, BERT, ViT · [Repo](https://github.com/hpcaitech/colossalai) · [▶️ Demo ↗](https://colossalai.org/zh-Hans/docs/get_started/bonus/) · [📖 Docs ↗](https://www.colossalai.org/) · [🌐 Site ↗](https://www.colossalai.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/colossalai/)</sub>

<a name="ml-agents"></a>
### #&#8288;23 [ml-agents](https://github.com/unity-technologies/ml-agents) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (67) · Freshness: active (80) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Oct 2026</sub>

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

<a name="torchtitan"></a>
### #&#8288;24 [torchtitan](https://github.com/pytorch/torchtitan) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · BSD-3-Clause · Oct 2026</sub>

**PyTorch-native training stack for pretraining, fine-tuning and RL of large models.**

torchtitan is a PyTorch codebase for training large generative models, covering pretraining, SFT/LoRA and RL (TitanRL). It composes FSDP2, tensor, pipeline, context and expert parallelism through DeviceMesh and DTensor, and runs are defined as Python recipe functions. It supports Llama 3, Qwen3, DeepSeek V3, gpt-oss, Kimi and FLUX, with MXFP8 and NVFP4 low-precision training.

- **+** Stacks FSDP2, TP, PP, CP and EP into N-D layouts without rewriting the model
- **+** Config is a Python recipe function, so runs are readable and copyable
- **+** TitanRL shares model definitions and kernels with vLLM, with a bitwise-parity mode
- **+** Reads and writes Hugging Face safetensors; async distributed checkpointing
- **−** Needs a recent PyTorch nightly; stable releases pin nightly torch and torchao
- **−** Verified recipes exist for only some models; others have CI debug configs only
- **−** Low-precision and RL features need extra nightly installs (torchao, vLLM, Monarch)
- **−** Aimed at multi-GPU clusters; README shows only a debug model on one GPU

<sub>GPU required · Needs PyTorch nightly, torchao (optional), vLLM (RL), Monarch (RL), TorchStore (RL) · Models: Llama 3, Qwen3, Qwen3.5, DeepSeek V3, gpt-oss · [Repo](https://github.com/pytorch/torchtitan) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/torchtitan/)</sub>

<a name="nanochat"></a>
### #&#8288;25 [nanochat](https://github.com/karpathy/nanochat) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: widely used (90) · Freshness: active (92) · Maintenance: weak (2) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Jul 2026</sub>

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

<a name="mergekit"></a>
### #&#8288;26 [mergekit](https://github.com/arcee-ai/mergekit) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · LGPL-3.0 · Oct 2026</sub>

**Merge pre-trained language models in weight space from YAML configs.**

mergekit combines pre-trained language models by operating on their weights, driven by a YAML config and the `mergekit-yaml` command. Tensors load lazily, so merges run on CPU or with as little as 8 GB of VRAM. It supports many methods (linear, SLERP, TIES, DARE, DELLA, SCE, Model Stock), plus layer-wise frankenmerges, MoE merging and LoRA extraction.

- **+** Lazy tensor loading: merges run on CPU or with as little as 8 GB VRAM
- **+** Many methods: linear, SLERP, TIES, DARE, DELLA, SCE, Model Stock and others
- **+** Also covers MoE merging, LoRA extraction, evolutionary merging and tokenizer transplantation
- **+** Declarative YAML configs with per-layer and per-tensor parameter gradients
- **−** Command-line only; no bundled UI
- **−** No Docker image or compose file provided
- **−** Install is from a git clone with pip install -e; no PyPI install documented
- **−** Models with different vocabularies need manual tokenizer configuration

<sub>GPU optional · Needs PyTorch, Hugging Face Hub (optional, for upload) · Models: Llama, Mistral, GPT-NeoX, StableLM, raw PyTorch models · [Repo](https://github.com/arcee-ai/mergekit) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mergekit/)</sub>

<a name="litgpt"></a>
### #&#8288;27 [litgpt](https://github.com/lightning-ai/litgpt) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Sep 2026</sub>

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

<a name="nnunet"></a>
### #&#8288;28 [nnunet](https://github.com/mic-dkfz/nnunet) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: known (32) · Freshness: recent (70) · Maintenance: patchy (45) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · Apache-2.0 · Oct 2026</sub>

**Self-configuring U-Net framework for biomedical image segmentation.**

nnU-Net analyzes a training dataset, builds a fingerprint, and configures 2D and 3D U-Net variants with matching preprocessing, training, model selection and inference. It targets supervised semantic segmentation, mainly biomedical images, and doubles as a baseline for segmentation research. Installed with pip install nnunetv2 on top of PyTorch.

- **+** Derives preprocessing and network configuration from a dataset fingerprint, with little manual tuning
- **+** Covers the full workflow: preprocessing, training, model selection and inference
- **+** Supports 2D and 3D data, arbitrary channel definitions and multiple image formats
- **+** Documented residual encoder presets and finetuning from nnssl checkpoints
- **−** Supervised semantic segmentation only; not a general vision or LLM toolkit
- **−** Requires setting up nnUNet_raw, nnUNet_preprocessed and nnUNet_results paths
- **−** Last tagged release is 2024-04-21, though commits continue
- **−** README does not state RAM or VRAM requirements

<sub>Needs PyTorch · Models: U-Net (2D, 3D fullres, cascade), Residual encoder U-Net presets · [Repo](https://github.com/mic-dkfz/nnunet) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nnunet/)</sub>

<a name="medicalgpt"></a>
### #&#8288;29 [medicalgpt](https://github.com/shibing624/medicalgpt) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (5) · Freshness: active (99) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Sep 2026</sub>

**Training scripts for medical LLMs: pretraining, SFT, RLHF, DPO, GRPO.**

MedicalGPT is a set of Python scripts that train domain LLMs through continued pretraining, supervised fine-tuning, reward modeling with PPO/RLOO, DPO, ORPO, GRPO and on-policy distillation. It supports Qwen, Llama-3, Mixtral and other model families, with LoRA/QLoRA and DeepSpeed ZeRO configs. Gradio, FastAPI and OpenAI-style demo servers are included for inference.

- **+** Covers PT, SFT, RM, PPO, DPO, ORPO, GRPO and OPD in one repo with shell launchers
- **+** Ships DeepSpeed ZeRO-1/2/3 configs and a VRAM table (QLoRA 4-bit 7B about 6GB)
- **+** Supports tool-call fine-tuning via SFT and DPO using ShareGPT-format jsonl
- **+** Colab notebooks run full PT+SFT+DPO or PPO pipelines in roughly 15-20 minutes
- **−** Script collection, not a packaged library or UI; you edit shell scripts and arguments
- **−** Stages are chained by hand, merging LoRA adapters between each one
- **−** README is mostly Chinese; the English version is a separate file
- **−** No Docker or compose files; setup is pip install -r requirements.txt

<sub>GPU required · Needs PyTorch, Hugging Face Transformers, PEFT, DeepSpeed · Models: Qwen 2/2.5/3.5, Llama-3, Mixtral 8x7B, Baichuan, ChatGLM · [Repo](https://github.com/shibing624/medicalgpt) · [📖 Docs ↗](https://github.com/shibing624/MedicalGPT/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/medicalgpt/)</sub>

<a name="easy-dataset"></a>
### #&#8288;30 [easy-dataset](https://github.com/conardli/easy-dataset) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (54) · Freshness: recent (77) · Maintenance: weak (4) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · May 2026</sub>

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

<a name="rllm"></a>
### #&#8288;31 [rllm](https://github.com/rllm-org/rllm) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

**RL training framework for language agents, on any harness or sandbox.**

rLLM trains language agents with reinforcement learning (GRPO, REINFORCE, RLOO, SFT, on-policy distillation). A model gateway captures token IDs and logprobs from your existing agent code, so the same agent runs for eval and training. Backends are verl, tinker and fireworks, chosen with one flag, and 60+ benchmarks run through `rllm eval`.

- **+** Same agent code for eval and training; gateway captures token IDs and logprobs
- **+** Switches between verl, tinker and fireworks backends with one flag
- **+** 60+ benchmarks, including SWE-bench and Terminal-Bench 2.0, via `rllm eval`
- **+** Wraps LangGraph, OpenAI Agents SDK or plain OpenAI client code with @rllm.rollout
- **−** Default install targets the tinker backend; multi-GPU needs the verl extra
- **−** README installs from a git URL, not from PyPI
- **−** Hardware requirements for training are not stated
- **−** Training recipes and results live mostly in external blog posts

<sub>GPU optional · Docker · Needs Python >= 3.11, verl with vLLM or SGLang (multi-GPU), Tinker API, Fireworks, Docker, Daytona or Modal (sandboxes) · Models: OpenAI-compatible endpoints, vLLM, SGLang · [Repo](https://github.com/rllm-org/rllm) · [📖 Docs ↗](https://docs.rllm-project.com/) · [🌐 Site ↗](https://rllm-project.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rllm/)</sub>

<a name="lmflow"></a>
### #&#8288;32 [lmflow](https://github.com/optimalscale/lmflow) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (27) · Freshness: recent (76) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · Apache-2.0 · Aug 2026</sub>

**Toolbox for full, LoRA and LISA finetuning of large language models.**

LMFlow is a Python toolbox that finetunes decoder language models with full-parameter training, LoRA/QLoRA or LISA, driven by shell scripts and Accelerate. It adds conversation templates, optional DeepSpeed, FlashAttention-2, vLLM or SGLang inference, DPO via TRL, and a Gradio chatbot demo. The README lists estimated memory per model size, for example 16GB for 7B with LoRA.

- **+** Covers full, LoRA, QLoRA and LISA finetuning from ready-made shell scripts
- **+** README gives memory estimates per method, from 0.5B to 70B models
- **+** Optional extras for DeepSpeed, FlashAttention, vLLM, SGLang and TRL-based DPO
- **+** Preset conversation templates such as llama3, llama2, phi3 and chatml
- **−** Tested only on Ubuntu 20.04; macOS and Windows may hit unexpected errors
- **−** vLLM and SGLang need incompatible CUDA/PyTorch versions, so separate envs are required
- **−** LISA script is only tested on a single GPU
- **−** Last release is 2025-07-11; no Docker image or compose file

<sub>GPU required · Needs Python 3.9+, conda, mpi4py, PyTorch, WandB (optional, on by default) · Models: Hugging Face decoder models, LLaMA, Llama-2, Llama-3, Qwen · [Repo](https://github.com/optimalscale/lmflow) · [📖 Docs ↗](https://optimalscale.github.io/LMFlow/) · [🌐 Site ↗](https://lmflow.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmflow/)</sub>

<a name="autoresearch"></a>
### #&#8288;33 [autoresearch](https://github.com/karpathy/autoresearch) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: widely used (99) · Freshness: recent (56) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 98k · no license · Mar 2026</sub>

**Agent loop that edits a small GPT training script and keeps changes that lower val_bpb.**

A coding agent (Claude, Codex or similar) is pointed at a single-GPU nanochat-derived training setup and edits train.py in a loop. Each experiment trains for a fixed 5 minutes and is kept or discarded based on validation bits per byte (val_bpb). The human edits program.md, the agent instructions, rather than the Python code.

- **+** Fixed 5-minute budget makes runs comparable: about 12 experiments per hour, around 100 overnight
- **+** Small codebase: agent edits only train.py, so diffs stay reviewable
- **+** val_bpb is vocab-size independent, so architecture changes compare fairly
- **+** Works with any coding agent that can read program.md
- **−** Requires a single NVIDIA GPU (tested on H100); no CPU, MPS or AMD support in main repo
- **−** Results are not comparable across different hardware because of the fixed time budget
- **−** Default program.md is a bare baseline for one agent; multi-agent setups are left to the user
- **−** README says to disable agent permissions, which is a safety risk without extra sandboxing

<sub>GPU required · Needs uv, PyTorch, Python 3.10+, a coding agent (Claude, Codex or similar) · Models: GPT (nanochat-style, trained from scratch), Muon + AdamW optimizer · [Repo](https://github.com/karpathy/autoresearch) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autoresearch/)</sub>

<a name="gpt-neox"></a>
### #&#8288;34 [gpt-neox](https://github.com/eleutherai/gpt-neox) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (23) · Freshness: recent (70) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Oct 2026</sub>

**EleutherAI's Megatron/DeepSpeed library for pretraining large language models.**

GPT-NeoX is a training library for autoregressive language models with billions of parameters, built on NVIDIA Megatron and DeepSpeed with ZeRO and 3D parallelism. It launches through Slurm, MPI, pdsh or the IBM Job Step Manager and runs on NVIDIA and AMD GPUs. The README says it targets from-scratch large-scale training and recommends Hugging Face transformers for generic inference.

- **+** Used by 40+ organizations to train 50+ models, including Pythia and StableLM
- **+** ZeRO and 3D parallelism, flash attention, Transformer Engine, rotary and ALiBi embeddings
- **+** Preset configs for Pythia, PaLM, Falcon and LLaMA 1 and 2
- **+** Exports to Hugging Face; logs to WandB, Comet or TensorBoard
- **−** Not meant for small-scale training or generic inference, per the README
- **−** Depends on DeeperSpeed, a DeepSpeed fork; environment isolation strongly advised
- **−** Tested on Python 3.8-3.10 and PyTorch 1.8-2.0; other versions not guaranteed
- **−** Last tagged release is from March 2023

<sub>GPU required · Docker + Compose · Needs PyTorch, DeeperSpeed, Slurm, MPI or pdsh for multi-node, Flash Attention (optional), Transformer Engine (optional), WandB, Comet or TensorBoard (optional) · Models: GPT-NeoX, Pythia, LLaMA 1 and 2, Falcon, PaLM · [Repo](https://github.com/eleutherai/gpt-neox) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpt-neox/)</sub>

<a name="paddlenlp"></a>
### #&#8288;35 [paddlenlp](https://github.com/paddlepaddle/paddlenlp) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: known (48) · Freshness: recent (54) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · May 2026</sub>

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

<a name="deepspec"></a>
### #&#8288;36 [deepspec](https://github.com/deepseek-ai/deepspec) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (19) · Freshness: active (94) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · MIT · Jul 2026</sub>

**Training and evaluation code for speculative-decoding draft models.**

DeepSpec is a Python codebase for training and evaluating draft models used in speculative decoding. It covers data preparation (prompt download, answer regeneration with the target model, target cache), a training script that spawns one worker per GPU, and an eval script measuring acceptance on benchmarks such as gsm8k, math500 and humaneval. It implements DSpark, DFlash and Eagle3 and links released checkpoints on Hugging Face for Qwen3 and Gemma 4 targets.

- **+** Implements three draft algorithms (DSpark, DFlash, Eagle3) in one pipeline with per-model configs
- **+** Released checkpoints on Hugging Face for Qwen3 4B/8B/14B and Gemma 4 12B
- **+** Eval covers nine benchmarks, including gsm8k, humaneval, mt-bench and arena-hard-v2
- **+** MIT license
- **−** Target cache for the default Qwen3-4B setup needs roughly 38 TB of storage
- **−** Default configs assume a single node with 8 GPUs
- **−** Data preparation needs a separately served inference engine for the target model
- **−** No release tags; only four target models are covered by released checkpoints

<sub>GPU required · Needs Inference engine to serve the target model (data prep), Hugging Face models and datasets · Models: Qwen/Qwen3-4B, Qwen/Qwen3-8B, Qwen/Qwen3-14B, google/gemma-4-12B-it · [Repo](https://github.com/deepseek-ai/deepspec) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepspec/)</sub>

<a name="text-to-text-transfer-transformer"></a>
### #&#8288;37 [text-to-text-transfer-transformer](https://github.com/google-research/text-to-text-transfer-transformer) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (14) · Freshness: recent (70) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · Apache-2.0 · Oct 2026</sub>

**Reference code for the T5 text-to-text transformer, with dataset and training tooling.**

The t5 library is the code behind the T5 paper. It defines text-to-text Tasks and Mixtures on tf.data, evaluates them with built-in metrics, and trains or fine-tunes released checkpoints through Mesh TensorFlow (TPU or GPU) or an experimental Hugging Face PyTorch shim. The README says it is no longer actively developed and recommends T5X (JAX/Flax) for new work.

- **+** Task and Mixture classes bundle data, preprocessors, tokenizer and metrics for multi-task training
- **+** Operative configs for the paper's experiments are published in gs://t5-data/experiments
- **+** Fine-tunes released T5 checkpoints from the command line via t5_mesh_transformer and gin configs
- **+** Exports a SavedModel for serving; Colab tutorial runs on a free TPU
- **−** TensorFlow/MeshTF version is no longer actively developed; README points to T5X
- **−** Hugging Face PyTorch shim is experimental, single-GPU, and subject to change
- **−** Workflow assumes GCP TPUs and GCS buckets; GPU use is a secondary path
- **−** Building C4 needs about 7 TB download and 335 CPU-days of preprocessing

<sub>GPU optional · Needs TensorFlow, Mesh TensorFlow, TensorFlow Datasets, SentencePiece, gin-config, Google Cloud TPU and GCS (for TPU use) · Models: T5 pre-trained checkpoints, Mesh TensorFlow Transformer, Hugging Face Transformers (PyTorch, experimental) · [Repo](https://github.com/google-research/text-to-text-transfer-transformer) · [▶️ Demo ↗](https://colab.research.google.com/github/google-research/text-to-text-transfer-transformer/blob/main/notebooks/t5-trivia.ipynb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/text-to-text-transfer-transformer/)</sub>

<a name="snorkel"></a>
### #&#8288;38 [snorkel](https://github.com/snorkel-team/snorkel) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (10) · Freshness: slowing (43) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Apr 2026</sub>

**Python library for programmatic labeling of machine learning training data.**

Snorkel is a Python library for building and managing training data programmatically, using weak supervision instead of hand labeling. It started at Stanford in 2015 and installs with pip or conda. The team now focuses on the commercial Snorkel Flow platform, and the last release was 2024-02-27.

- **+** Installs with pip or conda; requires Python 3.11 or later
- **+** Apache-2.0 licensed, with docs and a separate tutorials repository
- **+** Backed by over sixty peer-reviewed publications on weak supervision
- **+** Tutorials cover several tasks, domains and labeling techniques
- **−** Team focus has moved to proprietary Snorkel Flow, not this library
- **−** Last release was 2024-02-27
- **−** README does not mention LLM or foundation model workflows
- **−** Limited Windows testing; Docker or WSL recommended

<sub>Needs Python 3.11+ · [Repo](https://github.com/snorkel-team/snorkel) · [📖 Docs ↗](https://snorkel.readthedocs.io/) · [🌐 Site ↗](https://snorkel.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/snorkel/)</sub>

<a name="torchtune"></a>
### #&#8288;39 [torchtune](https://github.com/meta-pytorch/torchtune) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: niche (2) · Freshness: slowing (46) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · BSD-3-Clause · Apr 2026</sub>

**PyTorch library of LLM fine-tuning recipes driven by YAML configs.**

torchtune provides PyTorch-native recipes for SFT (full, LoRA/QLoRA), knowledge distillation, DPO, PPO, GRPO and quantization-aware training, run through a `tune` CLI and YAML configs. It includes model implementations for Llama, Gemma, Mistral, Phi and Qwen families. The README states development wound down in 2025 and the library is no longer actively maintained.

- **+** Covers SFT, KD, DPO, PPO, GRPO and QAT recipes; multi-GPU and multi-node support varies
- **+** README gives measured memory figures, e.g. Llama 3.1 8B QLoRA at 7.4 GiB peak on one 4090
- **+** YAML configs with CLI overrides, plus `tune cp` to copy and edit configs locally
- **+** Runs on NVIDIA, Intel XPU, AMD ROCm, Apple MPS and Ascend NPU devices
- **−** No longer actively maintained; development wound down in 2025
- **−** Last release was 2025-04-07; newest models listed are Qwen3 and Llama 4
- **−** Tested only against latest stable PyTorch (2.6.0 in README) and nightlies
- **−** Many recipe gaps, e.g. no full-weight KD and no LoRA for PPO or GRPO

<sub>GPU required · Needs PyTorch, torchvision, torchao, Hugging Face Hub · Models: Llama 3.1/3.2/3.3/4, Llama 3.2 Vision, Mistral 7B, Gemma2, Phi3 · [Repo](https://github.com/meta-pytorch/torchtune) · [📖 Docs ↗](https://pytorch.org/torchtune/main/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/torchtune/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
