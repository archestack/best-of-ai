# 🏋️ Training and fine-tuning reviews · Best of Open-Source AI

Tools to fine-tune, train or distill models on your own data and GPUs, from LoRA scripts to full training stacks. Back to the [leaderboard](../README.md#%EF%B8%8F-training-and-fine-tuning).

<sub>🌐 Also on the web: [Training and fine-tuning on archestack.com](https://archestack.com/best-of-ai/training/), each project on its own page.</sub>

<a name="unsloth"></a>
### 🥇 [unsloth](https://github.com/unslothai/unsloth) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 79k · Apache-2.0 · Nov 2026</sub>

**Desktop and web app to run and fine-tune local models.**

Unsloth ships as a native desktop app, a web UI (Unsloth Studio) and a Python library (Unsloth Core). It runs GGUF, MLX, diffusion, audio and embedding models, serves them over an OpenAI-compatible API, and fine-tunes them with LoRA, QLoRA, full fine-tuning, GRPO, DPO and FP8. The README claims 2x faster training with 70% less VRAM.

- **+** Covers both running and fine-tuning models, with export to GGUF, NVFP4 and FP8
- **+** Supports NVIDIA, AMD, Intel GPUs, CPU and Vulkan on Windows, Linux, WSL and macOS
- **+** Free Colab and Kaggle notebooks for many models, including GRPO and TTS
- **+** `unsloth start` connects Claude Code, Codex and other agents to local models
- **−** Speed and VRAM figures (2x, 70% less) are the project's own claims
- **−** Server-side tools are on by default; exposing it needs a password or --disable-tools
- **−** Three install paths (Desktop, Studio, Core) with many environment flags add complexity

<sub>GPU optional · Docker · Needs PyTorch, llama.cpp, Cloudflare (optional remote access), Docker (optional) · Models: GGUF, MLX, LLMs, diffusion, audio/TTS · port 8000 · [Repo](https://github.com/unslothai/unsloth) · [▶️ Demo ↗](https://colab.research.google.com/github/unslothai/unsloth/blob/main/studio/Unsloth_Studio_Colab.ipynb) · [📖 Docs ↗](https://unsloth.ai/docs) · [🌐 Site ↗](https://unsloth.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unsloth/)</sub>

<a name="peft"></a>
### 🥈 [peft](https://github.com/huggingface/peft) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Nov 2026</sub>

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

<a name="deepspeed"></a>
### 🥉 [deepspeed](https://github.com/deepspeedai/deepspeed) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;4 [verl](https://github.com/verl-project/verl) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Nov 2026</sub>

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

<a name="trl"></a>
### #&#8288;5 [trl](https://github.com/huggingface/trl) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;6 [megatron-lm](https://github.com/nvidia/megatron-lm) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · custom license · Nov 2026</sub>

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

<a name="heretic"></a>
### #&#8288;7 [heretic](https://github.com/p-e-w/heretic) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · AGPL-3.0 · Nov 2026</sub>

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

<a name="axolotl"></a>
### #&#8288;8 [axolotl](https://github.com/axolotl-ai-cloud/axolotl) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;9 [ms-swift](https://github.com/modelscope/ms-swift) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="weclone"></a>
### #&#8288;10 [weclone](https://github.com/xming521/weclone) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · AGPL-3.0 · Nov 2026</sub>

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

<a name="soup"></a>
### #&#8288;11 [soup](https://github.com/makazhanalpamys/soup) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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

<a name="art"></a>
### #&#8288;12 [art](https://github.com/openpipe/art) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

**Python RL framework that trains LLM agents with GRPO from rollout rewards.**

ART wraps GRPO reinforcement learning around existing Python agent code. An OpenAI-compatible client runs rollouts and records trajectories with rewards, while a separate server runs vLLM inference and trains LoRAs on a GPU. It can also use W&B's hosted Serverless RL backend instead of local GPUs.

- **+** Client/server split: run the client on a laptop, train on a remote or local GPU
- **+** OpenAI-compatible client drops into existing agent code, with a LangGraph integration
- **+** RULER automatic reward generation and notebooks for 2048, email search, MCP and SFT
- **+** Optional W&B Serverless RL backend avoids managing GPU infrastructure
- **−** Inference is blocked while each training step runs
- **−** Gemma 3 does not appear to be supported
- **−** You must define rewards and rollout environments yourself, unless using RULER
- **−** Serverless path depends on a W&B account and API key

<sub>GPU required · Docker · Needs vLLM, Unsloth, W&B (optional, Serverless RL) · Models: vLLM/HuggingFace causal LMs, Qwen, LoRA · [Repo](https://github.com/openpipe/art) · [📖 Docs ↗](https://art.openpipe.ai) · [🌐 Site ↗](https://art.openpipe.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/art/)</sub>

<a name="llamafactory"></a>
### #&#8288;13 [llamafactory](https://github.com/hiyouga/llamafactory) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 76k · Apache-2.0 · Nov 2026</sub>

**Fine-tuning toolkit for 100+ LLMs with a CLI and Gradio web UI.**

LlamaFactory fine-tunes LLMs and multimodal models through YAML-driven CLI runs or the LLaMA Board Gradio UI. It covers pre-training, SFT, reward modeling, PPO, DPO, KTO and ORPO, with full-tuning, freeze, LoRA and 2 to 8-bit QLoRA. Trained models can be served through an OpenAI-style API using vLLM or SGLang workers.

- **+** Covers SFT, reward modeling, PPO, DPO, KTO and ORPO in one framework
- **+** Supports QLoRA via AQLM, AWQ, GPTQ, LLM.int8, HQQ and EETQ
- **+** Integrates FlashAttention-2, Unsloth, Liger Kernel, GaLore, BAdam, APOLLO and Muon
- **+** Web UI plus OpenAI-style API with vLLM or SGLang inference backends
- **−** Official documentation is marked WIP in the README
- **−** Many features are toggled through YAML flags, so you need to know the options
- **−** Newer backends such as Megatron-core are documented mainly through PR links

<sub>GPU required · Docker + Compose · Needs PyTorch, Hugging Face Transformers, vLLM (optional), SGLang (optional) · Models: LLaMA, LLaVA, Mistral, Mixtral-MoE, Qwen3 · [Repo](https://github.com/hiyouga/llamafactory) · [▶️ Demo ↗](https://huggingface.co/spaces/hiyouga/LLaMA-Board) · [📖 Docs ↗](https://llamafactory.readthedocs.io/en/latest/) · [🌐 Site ↗](https://blog.llamafactory.net/en/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llamafactory/)</sub>

<a name="oumi"></a>
### #&#8288;14 [oumi](https://github.com/oumi-ai/oumi) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (50) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="agent-lightning"></a>
### #&#8288;15 [agent-lightning](https://github.com/microsoft/agent-lightning) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

**Reinforcement learning framework for training agents through a model-request proxy.**

Agent Lightning is a roughly 3,500-line Python framework that trains agents with RL while they run in their real harnesses. A gateway proxies the agent's model requests and records them as training data, a rollout controller runs agents locally or as Kubernetes Jobs, and a trainer built on verl and vLLM updates the policy. Examples include a Qwen3.5-9B coding agent, which the README reports going from 41.8% to 56.4% on SWE-bench Verified.

- **+** Agents run unchanged; the gateway captures model calls as training data
- **+** Runs rollouts as Kubernetes Jobs without an external sandbox service
- **+** Full coding-agent pipeline released: data cleaning, reward-hacking prevention, training scripts
- **+** Examples cover Calc-X, GSM8K, ScienceWorld, Search-R1, LLM-in-Sandbox and coding agents
- **−** Requires a verl and vLLM GPU stack; install shown for CUDA 13.0 only
- **−** No Docker or compose setup shipped in the repo
- **−** v1.0 is a full refactor; older releases live on a separate v0.x branch

<sub>GPU required · Needs verl, vLLM, uv, Kubernetes (optional, for rollouts) · Models: Qwen3.5-9B, Qwen3.5-35B-A3B · [Repo](https://github.com/microsoft/agent-lightning) · [📖 Docs ↗](https://microsoft.github.io/agent-lightning/stable/) · [🌐 Site ↗](https://www.microsoft.com/en-us/research/project/agent-lightning/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-lightning/)</sub>

<a name="areal"></a>
### #&#8288;16 [areal](https://github.com/areal-project/areal) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="fingpt"></a>
### #&#8288;17 [fingpt](https://github.com/ai4finance-foundation/fingpt) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (78) · Freshness: active (97) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Oct 2026</sub>

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

<a name="openrlhf"></a>
### #&#8288;18 [openrlhf](https://github.com/openrlhf/openrlhf) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

**Ray and vLLM based RLHF training framework for LLMs and VLMs.**

OpenRLHF trains language and vision-language models with reinforcement learning from human feedback. It uses Ray to schedule actor, reward, reference and critic models across GPUs, vLLM for sample generation, and DeepSpeed ZeRO-3 for training. It implements PPO, REINFORCE++, GRPO and RLOO, plus SFT, DPO and reward model training, with single-turn or multi-turn agent rollouts.

- **+** Several RL algorithms (PPO, REINFORCE++, GRPO, RLOO) selectable via one estimator flag
- **+** Hybrid engine lets models and vLLM share GPUs; README cites 70B+ scale
- **+** Multi-turn agent mode with reset/step environments, async training and VLM support
- **+** Also covers SFT, DPO and reward models, with LoRA/QLoRA and sample packing
- **−** Needs NVIDIA GPUs and a Ray, vLLM and DeepSpeed stack; setup is involved
- **−** README recommends a specific NVIDIA PyTorch container and removing conflicting pip packages
- **−** Large CLI flag surface; configuration lives mostly in example shell scripts

<sub>GPU required · Needs Ray, vLLM, DeepSpeed, HuggingFace Transformers, NCCL · Models: HuggingFace Transformers models, VLMs (e.g. Qwen3.5), MoE, LoRA/QLoRA · [Repo](https://github.com/openrlhf/openrlhf) · [📖 Docs ↗](https://openrlhf.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openrlhf/)</sub>

<a name="torchtitan"></a>
### #&#8288;19 [torchtitan](https://github.com/pytorch/torchtitan) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · BSD-3-Clause · Nov 2026</sub>

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

<a name="minimind"></a>
### #&#8288;20 [minimind](https://github.com/jingyaogong/minimind) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: widely used (94) · Freshness: active (83) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 65k · Apache-2.0 · Oct 2026</sub>

**Train a 64M-parameter LLM from scratch in plain PyTorch.**

MiniMind is a from-scratch training stack for small language models: a Qwen3-style dense (64M) and MoE (198M-A64M) architecture, tokenizer training, pretrain, SFT, LoRA, DPO, PPO/GRPO/CISPO and agentic RL. Core algorithms are written in native PyTorch rather than through transformers/trl/peft. The README reports about 2 hours on one RTX 3090 for the SFT epoch, and it ships datasets, an OpenAI-compatible server and a Streamlit chat UI.

- **+** Covers pretrain, SFT, LoRA, DPO, PPO/GRPO/CISPO and agentic RL in one repo
- **+** Core training code is native PyTorch, readable without trl or peft abstractions
- **+** Published datasets and checkpoints; mini data pair reproduces a chat model on one GPU
- **+** Exports to transformers, llama.cpp, vllm and ollama; DDP and DeepSpeed multi-GPU supported
- **−** Models are 64M-198M parameters with a 6,400-token vocabulary, so output quality is limited
- **−** Full pretrain and SFT datasets are 10GB and 14GB, a heavy download
- **−** Main README is Chinese; English version is a separate file
- **−** Latest tagged release is from 2025-10, while minimind-3 weights are newer

<sub>GPU optional · Needs PyTorch, Streamlit (optional web UI), wandb or SwanLab (optional logging) · Models: PyTorch .pth, Transformers format, llama.cpp, vllm, ollama · [Repo](https://github.com/jingyaogong/minimind) · [▶️ Demo ↗](https://www.modelscope.cn/studios/gongjy/MiniMind) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/minimind/)</sub>

<a name="ludwig"></a>
### #&#8288;21 [ludwig](https://github.com/ludwig-ai/ludwig) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Oct 2026</sub>

**YAML-configured training and fine-tuning for LLMs, multimodal and tabular models.**

Ludwig trains, fine-tunes and serves models from a YAML config and a CLI, with no training loop code. It covers LLM fine-tuning (SFT, DPO, KTO, ORPO, GRPO, LoRA and other PEFT adapters, 4-bit QLoRA, torchao QAT), plus multimodal, tabular, timeseries and image models. Runs scale from local to multi-GPU and Ray clusters by changing the backend setting.

- **+** Whole experiment defined in one YAML file; ludwig train, predict and serve cover the workflow
- **+** Wide LLM tuning coverage: SFT, DPO, KTO, ORPO, GRPO, many PEFT adapters, QLoRA
- **+** Mixes text, image, audio, number and timeseries inputs in one config
- **+** Distributed training via Accelerate (DDP, FSDP, DeepSpeed) and Ray; Optuna and Ray Tune for HPO
- **−** Requires Python 3.12+ and recent PyTorch, Transformers and Ray versions
- **−** Config schema is large; advanced options need reading the docs
- **−** Gated base models such as Llama need a Hugging Face token

<sub>GPU optional · Docker · Needs PyTorch 2.7+, Transformers 5, Ray 2.54, Hugging Face Hub token (gated models) · Models: Hugging Face Transformers, LoRA, QLoRA, DoRA, VeRA · port 8000 · [Repo](https://github.com/ludwig-ai/ludwig) · [📖 Docs ↗](https://ludwig.ai/latest/getting_started/) · [🌐 Site ↗](https://ludwig.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ludwig/)</sub>

<a name="liger-kernel"></a>
### #&#8288;22 [liger-kernel](https://github.com/linkedin/liger-kernel) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.7k · BSD-2-Clause · Nov 2026</sub>

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

<a name="model-optimizer"></a>
### #&#8288;23 [model-optimizer](https://github.com/nvidia/model-optimizer) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Nov 2026</sub>

**Python library for quantizing, pruning and distilling models for NVIDIA inference.**

NVIDIA Model Optimizer (ModelOpt) is a Python library that applies post-training quantization, quantization-aware training and distillation, pruning, NAS, speculative decoding and sparsity to Hugging Face, PyTorch or ONNX models. It exports quantized checkpoints (FP8, NVFP4 and others) for deployment in TensorRT-LLM, TensorRT, vLLM or SGLang. It integrates with Megatron-Bridge, Megatron-LM and Hugging Face Accelerate for techniques that need training.

- **+** Covers PTQ, QAT/QAD, pruning, NAS, distillation, speculative decoding and sparsity in one library
- **+** Exports to TensorRT-LLM, TensorRT, vLLM and SGLang; unified HF export covers transformers and diffusers
- **+** Publishes pre-quantized checkpoints on Hugging Face, including NVFP4 and FP8 variants
- **+** Installable from PyPI as nvidia-modelopt; Apache-2.0 with per-technique examples and support matrices
- **−** Pre-1.0 API; deprecated features are removed after about one release
- **−** Tuned for the NVIDIA stack; NVFP4 and TensorRT paths target NVIDIA GPUs
- **−** Pulls in additional third-party packages whose licenses need separate review
- **−** QAT, QAD and pruning workflows depend on Megatron or Accelerate setups

<sub>GPU required · Needs PyTorch, Hugging Face Transformers, ONNX, TensorRT-LLM, vLLM, SGLang, Megatron-Bridge · Models: Hugging Face, PyTorch, ONNX, Diffusers, FP8 · [Repo](https://github.com/nvidia/model-optimizer) · [📖 Docs ↗](https://nvidia.github.io/Model-Optimizer) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/model-optimizer/)</sub>

<a name="colossalai"></a>
### #&#8288;24 [colossalai](https://github.com/hpcaitech/colossalai) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (89) · Freshness: recent (71) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Nov 2026</sub>

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

<a name="skillopt"></a>
### #&#8288;25 [skillopt](https://github.com/microsoft/skillopt) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

**Trains agent skill documents against a frozen model with validation-gated edits.**

SkillOpt treats a single skill document as the trainable state of a frozen agent. A separate optimizer model turns scored rollouts into bounded add/delete/replace edits, and in the default path an edit is kept only if it strictly improves a held-out validation score. The output is a compact best_skill.md (typically 300-2,000 tokens) with no extra inference-time model calls. It installs from PyPI and includes a nightly SkillOpt-Sleep CLI and an optional Gradio dashboard.

- **+** Validation-gated edits with a textual learning-rate budget and rejected-edit buffer
- **+** Deployed skill is one markdown file, with no added inference-time model calls
- **+** Backends for OpenAI, Azure, Claude, Qwen, MiniMax, plus any OpenAI-compatible endpoint
- **+** Also drives Codex CLI and Claude Code harnesses; six built-in benchmarks
- **−** Training needs a separate optimizer model and scored rollouts, so API cost scales with epochs
- **−** Claude Code, Codex, Copilot and Devin integration files are in the repo, not the PyPI wheel
- **−** Main CLI does not expose every experimental control (multi-objective, replay, dream rollouts) as flags
- **−** Reported gains come from the authors' own benchmarks; no independent reproduction is cited

<sub>no GPU · Needs Python 3.10+, LLM API access (OpenAI, Azure, Claude, Qwen, MiniMax or OpenAI-compatible) · Models: OpenAI, Azure OpenAI, Claude, Qwen, MiniMax · port 7860 · [Repo](https://github.com/microsoft/skillopt) · [▶️ Demo ↗](https://youtu.be/JUBMDTCiM0M) · [📖 Docs ↗](https://github.com/microsoft/SkillOpt/blob/main/docs/index.md) · [🌐 Site ↗](https://microsoft.github.io/SkillOpt/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skillopt/)</sub>

<a name="slime"></a>
### #&#8288;26 [slime](https://github.com/thudm/slime) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (45) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.8k · Apache-2.0 · Nov 2026</sub>

**RL post-training framework connecting Megatron training with SGLang rollout.**

slime is a reinforcement-learning post-training framework for LLMs. It runs Megatron for training and SGLang for rollout generation, coordinated by Ray and a shared Data Buffer. Custom generate functions, reward functions, verifiers and environments plug in through documented interfaces. The README says it is the RL framework behind the GLM-4.5 through GLM-5.3 releases.

- **+** Used for RL training of GLM-4.5 through GLM-5.3, per the README
- **+** Megatron args pass through directly; SGLang args use the --sglang- prefix
- **+** Custom generate and reward hooks cover multi-turn, tool-use and agentic rollouts
- **+** Supports fully async rollout, PD disaggregation, delta weight sync, external rollout engines
- **−** Requires Megatron, SGLang and Ray together; setup is involved
- **−** No Dockerfile or compose file detected in the repository
- **−** Aimed at multi-GPU RL runs, not small single-machine fine-tuning

<sub>GPU required · Docker · Needs Megatron-LM, SGLang, Ray · Models: GLM, Qwen3.8, Qwen3.6, Qwen3.5, Qwen3-Next · [Repo](https://github.com/thudm/slime) · [📖 Docs ↗](https://thudm.github.io/slime/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/slime/)</sub>

<a name="fractalworkspace"></a>
### #&#8288;27 [fractalworkspace](https://github.com/fractal-compute-orchestrations/fractalworkspace) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: known (48) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · custom license · Nov 2026</sub>

**Federated training and split-model inference across Android phones.**

Fractal pairs a Python Flask control plane (FractalCore) with a Kotlin Android node app. The server splits datasets into segments, aggregates checkpoint deltas with FedAvg, and slices models such as Llama 3 8B or TinyLlama into INT4 .pte partitions of 150MB or less that phones run as a pipeline over Wi-Fi. Nodes pause when battery is under 50%, not charging, or battery temperature exceeds 40 C.

- **+** Covers both on-device federated training and layer-sliced inference across phones
- **+** Raw datasets stay on devices; only checkpoint deltas go to the server
- **+** Explicit limits: 150MB partitions, 4,100-byte activation frames, single-use task_Id
- **+** Per-tenant storage isolation and X-Auth-Token auth on tenant and admin routes
- **−** Proprietary non-commercial license; commercial use needs written authorization
- **−** Requires a Firebase project with Firestore for the token and reward ledger
- **−** Needs a physical Android device (API 24+); no iOS or desktop nodes documented
- **−** No release published; README gives no benchmarks or latency figures

<sub>Needs Firebase Firestore, Android Studio, Python 3.10+, Docker Compose, TFLite, ExecuTorch, torchao, XNNPACK · Models: Llama 3 8B, TinyLlama, TFLite (.tflite), ExecuTorch (.pte) · port 5000 · [Repo](https://github.com/fractal-compute-orchestrations/fractalworkspace) · [🌐 Site ↗](https://www.behance.net/gallery/221459335/Fractal) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fractalworkspace/)</sub>

<a name="rlinf"></a>
### #&#8288;28 [rlinf](https://github.com/rlinf/rlinf) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Nov 2026</sub>

**Distributed RL training framework for robot VLA policies and LLM agents.**

RLinf is a Python RL training infrastructure for embodied and agentic AI. It runs PPO, GRPO, SFT, DAgger and related methods on VLA policies (OpenPI π₀/π₀.₅, GR00T, OpenVLA-OFT), world models and LLMs, in simulators such as LIBERO, RoboTwin and Isaac Lab, and on real robots. It supports several accelerator backends and Megatron-based actor training, and installs from PyPI.

- **+** Covers simulated and real-robot RL, including teleoperation, SFT and deployment pipeline
- **+** Wide model support: π₀/π₀.₅, GR00T, OpenVLA-OFT, Cosmos3, Wan2.2, Moonlight-16B
- **+** Eight accelerator backends, including AMD ROCm, Ascend CANN, Moore Threads and MetaX
- **+** Adopted by Isaac Lab v3.0.0; installable from PyPI; docs in English and Chinese
- **−** Each model and simulator integration has its own setup; the feature set is large
- **−** No Docker or compose files detected in the repository
- **−** Aimed at robotics and RL researchers, not general LLM fine-tuning
- **−** Real-robot workflows depend on specific supported hardware such as Franka

<sub>GPU required · Docker · Needs PyTorch, Megatron, SGLang, Simulators (LIBERO, RoboTwin, Isaac Lab) · Models: OpenPI π₀ / π₀.₅, π₀-FAST, OpenVLA-OFT, GR00T-N1.6/N1.7, Cosmos3 · [Repo](https://github.com/rlinf/rlinf) · [📖 Docs ↗](https://rlinf.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rlinf/)</sub>

<a name="litgpt"></a>
### #&#8288;29 [litgpt](https://github.com/lightning-ai/litgpt) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

**PyTorch LLM implementations with recipes to pretrain, finetune, evaluate and serve.**

LitGPT reimplements 20+ open LLM families (Llama, Gemma, Phi, Qwen, Mistral and others) from scratch in PyTorch, without abstraction layers. A single CLI covers download, chat, finetune (LoRA, QLoRA, adapter), pretrain, continued pretraining, evaluate and serve, plus a Python `LLM` API. Training supports FSDP, flash attention and reduced precision (fp4/8/16/32) across 1 to 1000+ GPUs or TPUs.

- **+** Single CLI covers download, finetune, pretrain, evaluate, chat and serve
- **+** Readable single-file model implementations, easy to debug and modify
- **+** Supports LoRA, QLoRA, adapter finetuning and full pretraining from scratch
- **+** Apache-2.0 license with YAML training recipes
- **−** Only the listed model families are supported; new architectures need code added
- **−** No Docker or compose files in the repo
- **−** README promotes Lightning Cloud for GPUs; hardware requirements per model not stated

<sub>GPU optional · Needs PyTorch, Hugging Face Hub (weight download) · Models: Llama 2/3.x, Gemma 1/2/3, Phi 1.5-4, Qwen2.5/Qwen3, Mistral/Mixtral · port 8000 · [Repo](https://github.com/lightning-ai/litgpt) · [🌐 Site ↗](https://lightning.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/litgpt/)</sub>

<a name="h2o-llmstudio"></a>
### #&#8288;30 [h2o-llmstudio](https://github.com/h2oai/h2o-llmstudio) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

**No-code GUI and CLI for fine-tuning LLMs with LoRA and DPO.**

H2O LLM Studio is a Python framework with an H2O Wave web GUI and a CLI for fine-tuning LLMs on your own datasets. It supports LoRA, 8-bit training, DPO/IPO/KTO optimization, and classification and regression problem types, with DeepSpeed or DDP for multi-GPU runs. Experiments can be tracked and compared in the UI, chatted with, and exported to the Hugging Face Hub.

- **+** GUI covers dataset import, experiment tracking, comparison, chat and Hugging Face export
- **+** Supports LoRA, 8-bit training, DPO/IPO/KTO, plus causal classification and regression
- **+** Multi-GPU via DDP or DeepSpeed; YAML-configured CLI for scripted runs
- **+** Official Docker image on Docker Hub and a ready RunPod template
- **−** Requires an NVIDIA GPU with drivers >= 580; no CPU or non-NVIDIA path documented
- **−** Backwards compatibility not guaranteed; README advises pinning versions
- **−** DeepSpeed needs NVLink and a system CUDA Toolkit install
- **−** RLHF was removed; reinforcement learning is limited to DPO/IPO/KTO

<sub>GPU required · Docker · Needs NVIDIA drivers >= 580, CUDA 13 (PyTorch), H2O Wave, uv, Python 3.12, nvidia-container-toolkit (Docker) · Models: Hugging Face LLMs, LoRA, 8-bit training, DPO/IPO/KTO · port 10101 · [Repo](https://github.com/h2oai/h2o-llmstudio) · [📖 Docs ↗](https://docs.h2o.ai/h2o-llmstudio/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/h2o-llmstudio/)</sub>

<a name="ml-agents"></a>
### #&#8288;31 [ml-agents](https://github.com/unity-technologies/ml-agents) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (76) · Freshness: recent (79) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Oct 2026</sub>

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

<a name="mergekit"></a>
### #&#8288;32 [mergekit](https://github.com/arcee-ai/mergekit) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · LGPL-3.0 · Oct 2026</sub>

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

<a name="nnunet"></a>
### #&#8288;33 [nnunet](https://github.com/mic-dkfz/nnunet) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (47) · Freshness: recent (70) · Maintenance: fair (60) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · Apache-2.0 · Nov 2026</sub>

**Self-configuring U-Net framework for biomedical image segmentation.**

nnU-Net analyzes a training dataset, builds a fingerprint, and configures 2D and 3D U-Net variants with matching preprocessing, training, model selection and inference. It targets supervised semantic segmentation, mainly biomedical images, and doubles as a baseline for segmentation research. Installed with pip install nnunetv2 on top of PyTorch.

- **+** Derives preprocessing and network configuration from a dataset fingerprint, with little manual tuning
- **+** Covers the full workflow: preprocessing, training, model selection and inference
- **+** Supports 2D and 3D data, arbitrary channel definitions and multiple image formats
- **+** Documented residual encoder presets and finetuning from nnssl checkpoints
- **−** Supervised semantic segmentation only; not a general vision or LLM toolkit
- **−** Requires setting up nnUNet_raw, nnUNet_preprocessed and nnUNet_results paths
- **−** Last tagged release is 2024-04-21, though commits continue

<sub>Needs PyTorch · Models: U-Net (2D, 3D fullres, cascade), Residual encoder U-Net presets · [Repo](https://github.com/mic-dkfz/nnunet) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nnunet/)</sub>

<a name="nanochat"></a>
### #&#8288;34 [nanochat](https://github.com/karpathy/nanochat) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (93) · Freshness: active (85) · Maintenance: weak (3) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · MIT · Jul 2026</sub>

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

<a name="medicalgpt"></a>
### #&#8288;35 [medicalgpt](https://github.com/shibing624/medicalgpt) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (24) · Freshness: active (98) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Sep 2026</sub>

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

<a name="transformerlab-app"></a>
### #&#8288;36 [transformerlab-app](https://github.com/transformerlab/transformerlab-app) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (13) · Freshness: active (98) · Maintenance: weak (27) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · AGPL-3.0 · Aug 2026</sub>

**ML research workbench for training, fine-tuning, evaluating and chatting with models.**

Transformer Lab is a web UI and Python backend for downloading LLMs, fine-tuning them (LoRA/QLoRA, DPO, ORPO, SIMPO), evaluating them, and running diffusion and TTS models. It runs on a single machine with MLX, CUDA or ROCm trainers. A Teams edition submits jobs to Slurm or SkyPilot clusters from the same UI and CLI.

- **+** Covers training, evaluation, chat, diffusion and TTS in one UI
- **+** Trainers for Apple Silicon (MLX), NVIDIA (CUDA) and AMD (ROCm)
- **+** Teams edition schedules jobs on Slurm or SkyPilot clouds (AWS, GCP, Azure)
- **+** Lab SDK and CLI add job tracking to existing Python training scripts
- **−** Requires Apple Silicon, or an NVIDIA or AMD GPU; no CPU-only path listed
- **−** AGPL-3.0 license may restrict use in proprietary or hosted products
- **−** Windows support only through WSL2 and only with NVIDIA GPUs
- **−** Install is a curl-piped shell script into ~/.transformerlab

<sub>GPU required · Compose · Needs Conda, Node.js 22 (frontend development), Slurm or SkyPilot (Teams edition) · Models: Llama 3, DeepSeek, Mistral, Qwen, Phi · port 8338 · [Repo](https://github.com/transformerlab/transformerlab-app) · [▶️ Demo ↗](https://youtu.be/tY5TAvKviLo) · [📖 Docs ↗](https://lab.cloud/for-teams/) · [🌐 Site ↗](https://lab.cloud) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transformerlab-app/)</sub>

<a name="lightly-train"></a>
### #&#8288;37 [lightly-train](https://github.com/lightly-ai/lightly-train) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · AGPL-3.0 · Nov 2026</sub>

**Python library for pretraining, distilling and fine-tuning computer vision models.**

LightlyTrain is a Python package for training computer vision models: self-supervised pretraining and distillation (DINOv2/v3) on unlabeled data, plus fine-tuning for object detection, instance, semantic and panoptic segmentation, and depth estimation. Detection uses LTDETR/LTDETRv2 and segmentation uses EoMT, with ONNX and TensorRT export and C++ inference recipes. It is AGPL-3.0; commercial use needs a separate license.

- **+** Covers pretraining, distillation and fine-tuning for detection and several segmentation tasks in one package
- **+** Pretrained COCO checkpoints with published mAP and TensorRT T4 latency tables
- **+** ONNX and TensorRT export, plus C++ inference recipes for ONNX Runtime and TensorRT
- **+** Single pip install; runs on Windows, Linux and macOS with Python 3.8+
- **−** AGPL-3.0; production or proprietary use requires a commercial license from Lightly
- **−** Vision only; no language model training or fine-tuning
- **−** Benchmarks are on COCO, Cityscapes and NYUv2; custom-data results are not documented in the README
- **−** Pretraining results depend on data; the README points struggling users to paid expert contact

<sub>GPU optional · Needs PyTorch, TensorRT (optional, for export), ONNX Runtime (optional) · Models: DINOv2, DINOv3, LTDETR, LTDETRv2, EoMT · [Repo](https://github.com/lightly-ai/lightly-train) · [📖 Docs ↗](https://docs.lightly.ai/train/stable/) · [🌐 Site ↗](https://www.lightly.ai/lightly-train) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lightly-train/)</sub>

<a name="rllm"></a>
### #&#8288;38 [rllm](https://github.com/rllm-org/rllm) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (27) · Freshness: active (99) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

**RL training framework for language agents, on any harness or sandbox.**

rLLM trains language agents with reinforcement learning (GRPO, REINFORCE, RLOO, SFT, on-policy distillation). A model gateway captures token IDs and logprobs from your existing agent code, so the same agent runs for eval and training. Backends are verl, tinker and fireworks, chosen with one flag, and 60+ benchmarks run through `rllm eval`.

- **+** Same agent code for eval and training; gateway captures token IDs and logprobs
- **+** Switches between verl, tinker and fireworks backends with one flag
- **+** 60+ benchmarks, including SWE-bench and Terminal-Bench 2.0, via `rllm eval`
- **+** Wraps LangGraph, OpenAI Agents SDK or plain OpenAI client code with @rllm.rollout
- **−** Default install targets the tinker backend; multi-GPU needs the verl extra
- **−** README installs from a git URL, not from PyPI
- **−** Training recipes and results live mostly in external blog posts

<sub>GPU optional · Docker · Needs Python >= 3.11, verl with vLLM or SGLang (multi-GPU), Tinker API, Fireworks, Docker, Daytona or Modal (sandboxes) · Models: OpenAI-compatible endpoints, vLLM, SGLang · [Repo](https://github.com/rllm-org/rllm) · [📖 Docs ↗](https://docs.rllm-project.com/) · [🌐 Site ↗](https://rllm-project.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rllm/)</sub>

<a name="easy-dataset"></a>
### #&#8288;39 [easy-dataset](https://github.com/conardli/easy-dataset) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (66) · Freshness: recent (71) · Maintenance: weak (5) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · May 2026</sub>

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

<a name="gpt-neox"></a>
### #&#8288;40 [gpt-neox](https://github.com/eleutherai/gpt-neox) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: known (39) · Freshness: recent (70) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Nov 2026</sub>

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

<a name="lmflow"></a>
### #&#8288;41 [lmflow](https://github.com/optimalscale/lmflow) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: known (43) · Freshness: recent (74) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · Apache-2.0 · Aug 2026</sub>

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

<a name="alignment-handbook"></a>
### #&#8288;42 [alignment-handbook](https://github.com/huggingface/alignment-handbook) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · Apache-2.0 · Sep 2026</sub>

**Training scripts and YAML recipes for SFT, DPO and ORPO of LLMs.**

Hugging Face's reference repo for post-training language models. It provides scripts for continued pretraining, SFT, DPO and ORPO, plus YAML recipes that reproduce models such as Zephyr 7B, StarChat2, SmolLM2 and SmolLM3. Each script supports full-weight training with DeepSpeed ZeRO-3 or LoRA/QLoRA.

- **+** One YAML file per training run, so published models can be reproduced
- **+** Covers continued pretraining, SFT, DPO and ORPO, with full-weight (ZeRO-3) or LoRA/QLoRA
- **+** Recipes for Zephyr, StarChat2, SmolLM2, SmolLM3 and a Constitutional AI setup
- **+** Apache-2.0 licensed, maintained by Hugging Face
- **−** Pins PyTorch 2.6.0 and flash-attn 2.7.4.post1, so setup is tied to specific CUDA builds
- **−** Requires Flash Attention 2, which needs a compatible NVIDIA GPU
- **−** Reference recipes, not a general trainer; guides on DPO and preferences are still in progress
- **−** No Docker image or release; installed from source with uv

<sub>GPU required · Needs PyTorch 2.6.0, Flash Attention 2 (2.7.4.post1), DeepSpeed, Hugging Face Hub account, Git LFS · Models: Zephyr 7B, Gemma 7B, Mixtral 8x22B, SmolLM / SmolLM2 / SmolLM3, StarChat2 15B · [Repo](https://github.com/huggingface/alignment-handbook) · [📖 Docs ↗](https://arxiv.org/abs/2310.16944) · [🌐 Site ↗](https://huggingface.co/collections/alignment-handbook/handbook-v01-models-and-datasets-654e424d22e6880da5ebc015) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/alignment-handbook/)</sub>

<a name="xtuner"></a>
### #&#8288;43 [xtuner](https://github.com/internlm/xtuner) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (15) · Freshness: recent (74) · Maintenance: patchy (38) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

**Training engine for fine-tuning and RL of large MoE and dense LLMs.**

XTuner V1 is a PyTorch training engine for pre-training, instruction fine-tuning and reinforcement learning of large MoE models. It uses FSDP with optional DeepSpeed Ulysses sequence parallelism instead of 3D parallelism, and the README claims 200B MoE training without expert parallelism and support up to 1T parameters. It covers Intern S1, Intern VL, Qwen3, GPT OSS, DeepSeek V3 and Kimi K2 on NVIDIA GPUs and Ascend NPUs.

- **+** FSDP-based MoE training without expert parallelism at 200B scale, per the README
- **+** Supports FP8 and BF16 on GPU and BF16 on Ascend NPU
- **+** Includes multimodal pre-training, multimodal SFT and GRPO
- **+** DeepSpeed Ulysses sequence parallelism for long sequences, with 64k claimed on 200B MoE
- **−** Last tagged release is July 2025, older than the V1 announcement
- **−** MPO, DAPO and multi-turn agentic RL are still listed as coming soon
- **−** GPT OSS, DeepSeek V3 and Kimi K2 are not yet supported on NPU
- **−** Inference integration covers only LMDeploy; vLLM and SGLang are unchecked

<sub>GPU required · Docker · Needs PyTorch · Models: Intern S1, Intern VL, Qwen3 Dense, Qwen3 MoE, GPT OSS · [Repo](https://github.com/internlm/xtuner) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xtuner/)</sub>

<a name="autoresearch"></a>
### #&#8288;44 [autoresearch](https://github.com/karpathy/autoresearch) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: widely used (99) · Freshness: slowing (49) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 100k · no license · Mar 2026</sub>

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

<a name="paddlenlp"></a>
### #&#8288;45 [paddlenlp](https://github.com/paddlepaddle/paddlenlp) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (61) · Freshness: slowing (49) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · May 2026</sub>

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
### #&#8288;46 [deepspec](https://github.com/deepseek-ai/deepspec) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (37) · Freshness: active (87) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · MIT · Jul 2026</sub>

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

<a name="qwen-vl-series-finetune"></a>
### #&#8288;47 [qwen-vl-series-finetune](https://github.com/2u1/qwen-vl-series-finetune) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Sep 2026</sub>

**Fine-tuning scripts for Qwen2-VL, Qwen2.5-VL, Qwen3-VL and Qwen3.5.**

Training scripts built on HuggingFace and Liger-Kernel for fine-tuning Qwen vision-language models. They cover full fine-tuning, LoRA/QLoRA/DoRA, DPO, GRPO and classification, with DeepSpeed, multi-image and video inputs, and a Gradio inference UI. Data uses the LLaVA JSON format, with an optional reasoning field for Qwen3-VL-Thinking and Qwen3.5.

- **+** Covers SFT, DPO, GRPO and classification in one repo
- **+** Supports Qwen2-VL through Qwen3.5, including Qwen3-VL-MoE
- **+** Separate learning rates for vision tower, merger and LLM; top-k layer unfreezing
- **+** Image, multi-image, video and mixed-modality data with DeepSpeed zero2/zero3
- **−** Qwen3.5 needs Flash Attention 2 disabled; it raised CUDA errors in testing
- **−** QLoRA cannot be combined with vision training or Liger kernel
- **−** Full fine-tuning of dense Qwen3-VL with Liger can be slow
- **−** Limited to Qwen-VL family; other models live in separate repos

<sub>GPU required · Needs PyTorch, HuggingFace Transformers 5.3.0, Liger-Kernel 0.8.0, DeepSpeed, flash-attn, qwen-vl-utils, CUDA 12.8 · Models: Qwen2-VL, Qwen2.5-VL, Qwen3-VL, Qwen3-VL-MoE, Qwen3.5 · [Repo](https://github.com/2u1/qwen-vl-series-finetune) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwen-vl-series-finetune/)</sub>

<a name="text-to-text-transfer-transformer"></a>
### #&#8288;48 [text-to-text-transfer-transformer](https://github.com/google-research/text-to-text-transfer-transformer) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: known (33) · Freshness: recent (70) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · Apache-2.0 · Oct 2026</sub>

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

<a name="easyr1"></a>
### #&#8288;49 [easyr1](https://github.com/hiyouga/easyr1) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (14) · Freshness: active (80) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

**RL post-training framework for LLMs and vision-language models, forked from veRL.**

EasyR1 is a fork of veRL that adds vision-language model support to RL post-training. It runs GRPO, DAPO, Reinforce++, ReMax, RLOO, GSPO and CISPO on Llama3, Qwen2 to Qwen3 and Qwen-VL models, using vLLM for rollouts and Ray for multi-node runs. Example scripts cover Geometry3K, with full and LoRA training and checkpoint merging to Hugging Face format.

- **+** Supports GRPO, DAPO, Reinforce++, ReMax, RLOO, GSPO and CISPO in one codebase
- **+** Handles Qwen2-VL, Qwen2.5-VL and Qwen3-VL alongside text-only LLMs
- **+** README gives estimated GPU counts per model size from 1.5B to 72B
- **+** Ray multi-node setup documented for 70B+ models; LoRA and padding-free training supported
- **−** Ulysses parallelism does not work with vision-language models yet
- **−** No supervised fine-tuning or inference scripts; README points to LlamaFactory
- **−** Needs multiple GPUs for most model sizes; hardware figures are estimates
- **−** Pins a specific stack: flash-attn, vLLM 0.8.3+, transformers 4.54+

<sub>GPU required · Docker · Needs Ray, vLLM, flash-attn, transformers, Docker or Apptainer (optional) · Models: Llama3, Qwen2, Qwen2.5, Qwen3, Qwen2-VL · [Repo](https://github.com/hiyouga/easyr1) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/easyr1/)</sub>

<a name="vlm-r1"></a>
### #&#8288;50 [vlm-r1](https://github.com/om-ai-lab/vlm-r1) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (29) · Freshness: recent (61) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Jul 2026</sub>

**GRPO reinforcement-learning training for Qwen2.5-VL and InternVL models.**

VLM-R1 applies R1-style GRPO reinforcement learning to vision-language models, with scripts for full fine-tuning, LoRA, multi-node and multi-image training. It supports QwenVL and InternVL, loads custom jsonl data, and ships 3B checkpoints trained for referring expression comprehension, open-vocabulary detection and multimodal math. An SFT baseline via LLaMA-Factory and Ascend inference guides are included.

- **+** Full, LoRA, frozen-vision, multi-node and multi-image GRPO training with ready run scripts
- **+** Released 3B checkpoints for OVD, Math and REC, plus Hugging Face demos
- **+** Custom jsonl loader and documented steps for adding new VLMs and reward functions
- **+** Includes SFT comparison setup and Ascend 910B/300I Duo inference guides
- **−** Recipes centre on REC, OVD and a few tasks; other tasks need your own reward functions
- **−** Last tagged release is 2025-04-15; later changes exist only as commits
- **−** Setup is a conda Python 3.10 env plus setup.sh; no compose file
- **−** Only 3B checkpoints are listed; larger model results are not documented

<sub>GPU required · Docker · Needs PyTorch, DeepSpeed, LLaMA-Factory (SFT baseline), Hugging Face datasets · Models: Qwen2.5-VL, InternVL · [Repo](https://github.com/om-ai-lab/vlm-r1) · [▶️ Demo ↗](https://huggingface.co/spaces/omlab/VLM-R1-Referral-Expression) · [📖 Docs ↗](https://arxiv.org/abs/2504.07615) · [🌐 Site ↗](https://om-ai-lab.github.io/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vlm-r1/)</sub>

<a name="torchtune"></a>
### #&#8288;51 [torchtune](https://github.com/meta-pytorch/torchtune) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (22) · Freshness: recent (70) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · BSD-3-Clause · Nov 2026</sub>

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

<a name="autodistill"></a>
### #&#8288;52 [autodistill](https://github.com/autodistill/autodistill) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: niche (8) · Freshness: recent (70) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · Apache-2.0 · Sep 2026</sub>

**Label images with foundation models, then train small YOLO or DETR detectors.**

Autodistill is a Python package that uses a large base model (Grounded SAM, Grounding DINO, OWLv2 and others) to auto-label unlabeled images from text prompts, then trains a smaller supervised model such as YOLOv8, YOLO-NAS, YOLOv5 or DETR on the result. Base and target models are separate pip plugins, and there is a CLI one-liner as well as a Python API. Supported tasks are object detection and instance segmentation; classification is listed as upcoming.

- **+** Modular plugins per base and target model keep dependencies and licenses separate
- **+** Goes from unlabeled images to a trained detector without manual labeling
- **+** One CLI command covers labeling and training: autodistill images --base --target
- **+** Many base models: Grounded SAM 2, OWLv2, Kosmos-2, LLaVA-1.5, cloud vision APIs
- **−** Vision only; language and other model types are described as future work
- **−** Last release was 2024-02-13, despite recent commits
- **−** Classification and several targets (YOLOv6, YOLOv7) are unfinished or in progress
- **−** Label quality depends on prompts; README says base models are not perfect yet

<sub>Needs Python, pip plugins per base/target model, Roboflow (optional, for deployment) · Models: Grounded SAM, Grounding DINO, Grounded SAM 2, OWLv2, OWL-ViT · [Repo](https://github.com/autodistill/autodistill) · [▶️ Demo ↗](https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/how-to-auto-train-yolov8-model-with-autodistill.ipynb) · [📖 Docs ↗](https://docs.autodistill.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autodistill/)</sub>

<a name="openclaw-rl"></a>
### #&#8288;53 [openclaw-rl](https://github.com/gen-verse/openclaw-rl) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (21) · Freshness: recent (70) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · Apache-2.0 · May 2026</sub>

**Asynchronous RL framework that trains agents from live conversation feedback.**

OpenClaw-RL wraps a self-hosted model as an OpenAI-compatible API for OpenClaw, intercepts multi-turn conversations, and trains the policy in the background using Binary RL (GRPO), on-policy distillation, or a hybrid of both. Built on the Slime framework, it also includes RL recipes for terminal, GUI, SWE and tool-call agents. Training can run on local GPUs or on Tinker (LoRA).

- **+** Serving, rollout, judge scoring and training run as separate async loops, so serving continues during training
- **+** Supports Binary RL, on-policy distillation and a combined method, with LoRA and Qwen3.5 support
- **+** Includes launch scripts for terminal, GUI, SWE and tool-call agent RL
- **+** Policy, judge and trainer run on your own infrastructure; no third-party model API required
- **−** Default setup assumes 8 GPUs, CUDA 12.9 and Python 3.12
- **−** Depends on Slime and Ray-style launch scripts; setup is involved
- **−** Personal-agent flow is tied to OpenClaw and needs an extension for your own install
- **−** No Docker or compose files, and no tagged releases

<sub>GPU required · Needs Slime, OpenClaw, CUDA 12.9, Python 3.12 · Models: Qwen3 4B/8B, Qwen3.5 4B/9B/27B, Qwen3-VL 8B · port 30000 · [Repo](https://github.com/gen-verse/openclaw-rl) · [📖 Docs ↗](https://arxiv.org/abs/2603.10165) · [🌐 Site ↗](https://yinjjiew.github.io/projects/openclawrl1) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openclaw-rl/)</sub>

<a name="snorkel"></a>
### #&#8288;54 [snorkel](https://github.com/snorkel-team/snorkel) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: niche (28) · Freshness: slowing (38) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Apr 2026</sub>

**Python library for programmatic labeling of machine learning training data.**

Snorkel is a Python library for building and managing training data programmatically, using weak supervision instead of hand labeling. It started at Stanford in 2015 and installs with pip or conda. The team now focuses on the commercial Snorkel Flow platform, and the last release was 2024-02-27.

- **+** Installs with pip or conda; requires Python 3.11 or later
- **+** Apache-2.0 licensed, with docs and a separate tutorials repository
- **+** Backed by over sixty peer-reviewed publications on weak supervision
- **+** Tutorials cover several tasks, domains and labeling techniques
- **−** Team focus has moved to proprietary Snorkel Flow, not this library
- **−** Last release was 2024-02-27
- **−** Limited Windows testing; Docker or WSL recommended

<sub>Needs Python 3.11+ · [Repo](https://github.com/snorkel-team/snorkel) · [📖 Docs ↗](https://snorkel.readthedocs.io/) · [🌐 Site ↗](https://snorkel.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/snorkel/)</sub>

<a name="modernbert"></a>
### #&#8288;55 [modernbert](https://github.com/answerdotai/modernbert) <sub>score [13](../README.md#-how-we-rank "Score 13/100. Adoption: niche (3) · Freshness: slowing (40) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Mar 2026</sub>

**Research code for pre-training and evaluating ModernBERT encoder models.**

Research repository behind ModernBERT, a BERT-style bidirectional encoder. It provides FlexBERT, a modular set of encoder building blocks configured through YAML, plus pre-training on the Composer framework and GLUE evaluation scripts. Example scripts train dense retrievers with Sentence Transformers and ColBERT models with PyLate.

- **+** Full pre-training and GLUE evaluation code, stated to be the code used in the paper
- **+** YAML-configured FlexBERT blocks with example configs in the yamls folder
- **+** Example scripts for Sentence Transformers dense retrieval and PyLate ColBERT training
- **+** Supports Flash Attention 3 on H100 with Flash Attention 2 fallback
- **−** README describes itself as barebones and under construction
- **−** Intermediate checkpoints are listed as release pending
- **−** Setup needs a GPU machine, conda environment and flash-attn 2.6.3 build or wheel
- **−** Streaming dataset class distributes memory unevenly across accelerators, per the README

<sub>GPU required · Needs conda, composer, flash-attn 2.6.3, Sentence Transformers, PyLate · Models: ModernBERT, FlexBERT, BERT (GLUE evals), ColBERT (PyLate) · [Repo](https://github.com/answerdotai/modernbert) · [📖 Docs ↗](https://arxiv.org/abs/2412.13663) · [🌐 Site ↗](https://huggingface.co/collections/answerdotai/modernbert-67627ad707a4acbf33c41deb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/modernbert/)</sub>

<a name="search-r1"></a>
### #&#8288;56 [search-r1](https://github.com/petergriffinjin/search-r1) <sub>score [10](../README.md#-how-we-rank "Score 10/100. Adoption: niche (17) · Freshness: quiet (1) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Nov 2025</sub>

**RL framework that trains LLMs to interleave reasoning with search engine calls.**

Search-R1 is a training pipeline built on veRL that uses rule-based outcome rewards to teach base LLMs, such as Llama-3.2-3B and Qwen2.5-7B, to reason and call a search engine over multiple turns. It supports PPO, GRPO and reinforce, with retrieval from local BM25, dense retrievers with flat or ANN indexes, or online search APIs. The search engine runs as a separate HTTP server that training calls.

- **+** Supports PPO, GRPO and reinforce training methods
- **+** Pluggable retrievers: BM25, dense flat/ANN, online search APIs, rerankers
- **+** Multinode training documented for 30B+ models
- **+** Two papers and public wandb logs for reproducing experiments
- **−** Pinned older stack: Python 3.9, torch 2.4.0, vllm 0.6.3
- **−** Needs two separate conda environments plus a running retrieval server
- **−** No Docker or compose setup provided
- **−** Quick start downloads a Wikipedia corpus and index before training

<sub>GPU required · Needs veRL, vLLM 0.6.3, PyTorch 2.4.0, flash-attn, faiss-gpu 1.8.0, pyserini, FastAPI, wandb · Models: Llama-3.2-3B, Qwen2.5-3B, Qwen2.5-7B · port 8000 · [Repo](https://github.com/petergriffinjin/search-r1) · [📖 Docs ↗](https://github.com/PeterGriffinJin/Search-R1/blob/main/docs/retriever.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/search-r1/)</sub>

<a name="agentflow"></a>
### #&#8288;57 [agentflow](https://github.com/lupantech/agentflow) <sub>score [10](../README.md#-how-we-rank "Score 10/100. Adoption: niche (6) · Freshness: quiet (28) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · MIT · Jan 2026</sub>

**Agent system with an RL-trained planner, executor, verifier and generator.**

AgentFlow is a research framework that splits an agent into Planner, Executor, Verifier and Generator modules sharing an evolving memory and a toolkit (python_coder, google_search, wikipedia_search, web_search). The planner is trained online with Flow-GRPO on verl, using NQ and DeepMath-103K. The repo includes inference scripts, benchmark runners and a 7B planner model on Hugging Face.

- **+** Trains only the planner in-system with Flow-GRPO; hyperparameters are in train/config.yaml
- **+** Each module can use a different engine: OpenAI, DashScope, Gemini, DeepSeek, Together or local vLLM
- **+** Ships a 7B planner checkpoint, benchmark scripts and a Gradio demo
- **+** Paper accepted at ICLR 2026; README reports gains on 10 benchmarks
- **−** Changing the Executor, Verifier or Generator engine requires editing source files
- **−** Needs several API keys (OpenAI for judging, Google for search) even for basic runs
- **−** No tagged release and no Docker setup; install is via setup.sh
- **−** Research code with no general-purpose deployment or UI beyond the demo

<sub>GPU optional · Needs OpenAI API, Google Search API, DashScope or Together API, vLLM, verl, tmux · Models: Qwen2.5-7B-Instruct, AgentFlow planner 7B, GPT-4o, Gemini, DeepSeek · [Repo](https://github.com/lupantech/agentflow) · [▶️ Demo ↗](https://huggingface.co/spaces/AgentFlow/agentflow) · [📖 Docs ↗](https://deepwiki.com/lupantech/AgentFlow) · [🌐 Site ↗](https://agentflow.stanford.edu/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentflow/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
