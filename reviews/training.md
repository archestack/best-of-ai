# 🏋️ Training and fine-tuning reviews · Best of Open-Source AI

Tools to fine-tune, train or distill models on your own data and GPUs, from LoRA scripts to full training stacks. Back to the [leaderboard](../README.md#%EF%B8%8F-training-and-fine-tuning).

<sub>🌐 Also on the web: [Training and fine-tuning on archestack.com](https://archestack.com/best-of-ai/training/), each project on its own page.</sub>

<a name="peft"></a>
### 🥇 [peft](https://github.com/huggingface/peft) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Nov 2026</sub>

**Python library for LoRA and other parameter-efficient fine-tuning methods.**

PEFT wraps a pretrained model with adapter methods such as LoRA, soft prompts and IA3 through get_peft_model, so only a small set of extra parameters is trained. Adapters are saved as small checkpoints (19MB versus 11GB for T0_3B in the README) and reloaded with PeftModel.from_pretrained. It integrates with Transformers, Diffusers, Accelerate and TRL, and combines with quantization for QLoRA-style training.

- **+** Adapter checkpoints are a few MB instead of GBs, per the T0_3B and Stable Diffusion examples
- **+** LoRA trains bigscience/mt0-xxl (12B) in 56GB GPU where full fine-tuning runs out of memory
- **+** Integrates with Transformers, Diffusers, Accelerate and TRL; installs with pip
- **+** Combines with quantization, e.g. QLoRA on Llama-2-7b with a 16GB GPU
- **−** Library only: no training UI, you write the loop or use Trainer or TRL
- **−** Transformers integration lacks some PEFT features, such as merging adapters into the base model
- **−** Models not officially supported need manual target-module configuration
- **−** lora-t0-3b scored 0.863 versus 0.892 for Flan-T5 in the README's RAFT table

<sub>GPU optional · Docker · Needs PyTorch, Transformers · Models: LoRA, Soft prompts, IA3, Transformers models, Stable Diffusion · [Repo](https://github.com/huggingface/peft) · [▶️ Demo ↗](https://huggingface.co/spaces/smangrul/peft-lora-sd-dreambooth) · [📖 Docs ↗](https://huggingface.co/docs/peft/main/en/index) · [🌐 Site ↗](https://huggingface.co/PEFT) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/peft/)</sub>

<a name="trl"></a>
### 🥈 [trl](https://github.com/huggingface/trl) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Nov 2026</sub>

**Python library for post-training LLMs with SFT, DPO, GRPO and KTO.**

TRL provides trainer classes (SFTTrainer, GRPOTrainer, AsyncGRPOTrainer, DPOTrainer, KTOTrainer, RewardTrainer) for post-training Hugging Face Transformers models. It builds on Accelerate for DDP, DeepSpeed and FSDP scaling, and on PEFT for LoRA/QLoRA. A `trl` CLI runs SFT, DPO and KTO without writing code.

- **+** Covers SFT, DPO, KTO, GRPO and reward model training behind one trainer API
- **+** Scales from one GPU to multi-node via Accelerate, DDP, DeepSpeed ZeRO and FSDP
- **+** PEFT integration allows LoRA/QLoRA training of large models on modest hardware
- **+** CLI runs sft, dpo and kto jobs from the shell without code
- **−** AsyncGRPOTrainer needs a separate vLLM server on a different GPU than the trainer
- **−** Features under trl.experimental may change or be removed in any release
- **−** Tied to the Hugging Face Transformers ecosystem and its model formats
- **−** accuracy_reward needs the extra math-verify install

<sub>GPU optional · Docker · Needs transformers, accelerate, peft, datasets, vllm (AsyncGRPOTrainer), math-verify (accuracy_reward) · Models: Hugging Face Transformers models, LoRA/QLoRA adapters via PEFT · [Repo](https://github.com/huggingface/trl) · [📖 Docs ↗](https://huggingface.co/docs/trl/index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trl/)</sub>

<a name="unsloth"></a>
### 🥉 [unsloth](https://github.com/unslothai/unsloth) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 80k · Apache-2.0 · Nov 2026</sub>

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

<a name="deepspeed"></a>
### #&#8288;4 [deepspeed](https://github.com/deepspeedai/deepspeed) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Nov 2026</sub>

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

<sub>GPU optional · Needs PyTorch, CUDA or ROCm compiler (nvcc/hipcc), ninja · Models: PyTorch models, Hugging Face Transformers · [Repo](https://github.com/deepspeedai/deepspeed) · [📖 Docs ↗](https://www.deepspeed.ai/getting-started/) · [🌐 Site ↗](https://www.deepspeed.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepspeed/)</sub>

<a name="megatron-lm"></a>
### #&#8288;5 [megatron-lm](https://github.com/nvidia/megatron-lm) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · custom license · Nov 2026</sub>

**NVIDIA's library for training large transformer models across many GPUs.**

Megatron Core is a PyTorch library of transformer building blocks with tensor, pipeline, data, expert and context parallelism, plus FP16, BF16, FP8 and FP4 mixed precision. The repo also ships Megatron-LM, a reference set of pre-configured training scripts, along with distributed checkpointing and post-training tools for quantization, distillation and pruning. Hugging Face checkpoint conversion lives in the separate Megatron Bridge project.

- **+** Supports TP, PP, DP, EP and CP parallelism in one library
- **+** Mixed precision from FP16 and BF16 down to FP8 and FP4
- **+** Distributed checkpointing with resharding, plus MoE and hybrid model support
- **+** Published throughput benchmarks, e.g. DeepSeek-V3 on 256 GB300 GPUs
- **−** Aimed at multi-GPU clusters; no small-scale or CPU workflow described
- **−** Source builds can run out of memory and need MAX_JOBS tuning
- **−** HF checkpoint conversion is in Megatron Bridge, a separate repo for now
- **−** License detected as NOASSERTION while the README badge says Apache

<sub>GPU required · Docker · Needs PyTorch 2.6.0+, Python 3.12+, NVIDIA NGC PyTorch container (for source development) · Models: DeepSeek-V3, Qwen3-235B-A22B, Nemotron 3 Ultra, DeepSeek-V4 (initial, dev branch) · [Repo](https://github.com/nvidia/megatron-lm) · [📖 Docs ↗](https://docs.nvidia.com/megatron-core/developer-guide/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/megatron-lm/)</sub>

<a name="axolotl"></a>
### #&#8288;6 [axolotl](https://github.com/axolotl-ai-cloud/axolotl) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

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

<a name="heretic"></a>
### #&#8288;7 [heretic](https://github.com/p-e-w/heretic) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · AGPL-3.0 · Nov 2026</sub>

**Modifies LLM behavior, such as refusals, without training, via ablation.**

Heretic is a Python CLI that changes how a Hugging Face language model behaves without training it. It runs an Optuna TPE optimizer over a pluggable modifier, by default Arbitrary-Rank Ablation or classic directional ablation, to minimize scores such as refusal rate and KL divergence. The default action removes refusals; config files cover slop, humor, sycophancy and response length.

- **+** One command to process a model: pip install heretic-llm, then heretic <model>
- **+** Custom scorer plugins load from a file path without modifying the package
- **+** Optional 4-bit bitsandbytes quantization lowers VRAM needed to process a model
- **+** Reproducibility manifests (about 9 KB) let others rebuild a model with --reproduce
- **−** Runs are slow: about 30-40 minutes for a 4B model on an RTX 3090
- **−** Heretic 1.x config files are incompatible with 2.x and need migration
- **−** Only one modifier can be used per run
- **−** ARA technique has no published preprint yet; details are in a pull request

<sub>GPU required · Needs Python 3.10+, PyTorch 2.6+, Optuna, bitsandbytes (optional), Hugging Face · Models: Hugging Face dense models, multimodal models, MoE architectures, hybrid models · [Repo](https://github.com/p-e-w/heretic) · [▶️ Demo ↗](https://huggingface.co/spaces/heretic-org/Heretic-Grimoire) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/heretic/)</sub>

<a name="ms-swift"></a>
### #&#8288;8 [ms-swift](https://github.com/modelscope/ms-swift) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="soup"></a>
### #&#8288;9 [soup](https://github.com/makazhanalpamys/soup) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="verl"></a>
### #&#8288;10 [verl](https://github.com/verl-project/verl) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Nov 2026</sub>

**RL post-training library for LLMs with PPO, GRPO, FSDP and Megatron.**

verl is the open-source implementation of the HybridFlow paper from ByteDance Seed. It runs reinforcement learning and supervised fine-tuning for LLMs, using FSDP, FSDP2 or Megatron-LM for training and vLLM, SGLang or HF Transformers for rollout generation. It covers PPO, GRPO, RLOO, ReMax and REINFORCE++ with verifiable or model-based rewards.

- **+** FSDP, FSDP2 and Megatron-LM training with vLLM, SGLang or HF rollout
- **+** Covers PPO, GRPO, RLOO, ReMax and REINFORCE++, plus multi-turn tool-calling RL
- **+** README states scaling to 671B models via expert parallelism, with LoRA RL to save memory
- **+** Runs on NVIDIA, AMD and Huawei Ascend; Intel XPU via a plugin
- **−** Realistic runs need multiple GPUs; not a single-machine tool
- **−** Fully async and one-step-off trainers moved to verl-recipe, pinned to v0.9.1
- **−** Several algorithms (DAPO, GSPO, PRIME) live in the separate verl-recipe repository
- **−** Inference engine versions matter; README warns vLLM 0.7.x has bugs causing OOMs

<sub>GPU required · Docker · Needs PyTorch, vLLM or SGLang, Megatron-LM (optional) · Models: Hugging Face Transformers, ModelScope, Qwen3.5, Qwen3, Qwen2.5 · [Repo](https://github.com/verl-project/verl) · [📖 Docs ↗](https://verl.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/verl/)</sub>

<a name="weclone"></a>
### #&#8288;11 [weclone](https://github.com/xming521/weclone) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · AGPL-3.0 · Nov 2026</sub>

**Builds a life portrait from chat history and fine-tunes a personal chat clone.**

WeClone extracts a reviewable, fact-by-fact profile of you from exported chat history (Telegram today) using Codex or any OpenAI-compatible API. The portrait is exposed to assistants such as Claude Code and Codex over MCP. It also keeps the original workflow of LoRA fine-tuning Qwen2.5-7B-Instruct on your chats, served as an OpenAI-compatible API and connected to chat platforms via AstrBot or LangBot.

- **+** Every portrait fact traces to its source and carries a privacy level
- **+** Per-domain and per-level access control for assistants reading the portrait over MCP
- **+** Encrypted local storage by default; training data filtered with Microsoft Presidio
- **+** Web UI in English and Chinese for reviewing and editing facts
- **−** Only Telegram is supported as a data source; WhatsApp, Discord and Slack are pending
- **−** Portrait and extraction prompts are in Chinese; English chats untested
- **−** Chat content is sent to the configured model service during extraction
- **−** Fine-tuning needs an NVIDIA GPU; agent clone is still in development

<sub>GPU optional · Needs Python 3.12, Codex CLI or OpenAI-compatible API, uv, AstrBot or LangBot (chat bots), Telegram Desktop (data export) · Models: Qwen2.5-7B-Instruct (LoRA), OpenAI-compatible APIs, Codex · port 5175 · [Repo](https://github.com/xming521/weclone) · [📖 Docs ↗](https://docs.weclone.love/en/) · [🌐 Site ↗](https://www.weclone.love/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/weclone/)</sub>

<a name="art"></a>
### #&#8288;12 [art](https://github.com/openpipe/art) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="torchtitan"></a>
### #&#8288;13 [torchtitan](https://github.com/pytorch/torchtitan) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · BSD-3-Clause · Nov 2026</sub>

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

<a name="agent-lightning"></a>
### #&#8288;14 [agent-lightning](https://github.com/microsoft/agent-lightning) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

**Reinforcement learning framework for training agents through a model proxy.**

Agent Lightning v1.0 trains agents with RL while they run in their own harnesses. An API gateway proxies the agent's model requests and records them as training data, and a trainer built on verl and vLLM updates the policy. Rollouts run locally or as Kubernetes Jobs. Examples cover math, search, sandbox and coding agents.

- **+** Agents run unmodified; the gateway captures training data from model calls
- **+** Runs rollouts as Kubernetes Jobs without an external sandbox service
- **+** Ships a full coding-agent pipeline: data cleaning, reward-hacking prevention, training scripts
- **+** Small codebase of about 3,500 lines
- **−** Requires a verl and vLLM GPU stack; setup example targets CUDA 13.0
- **−** v1.0 was a full refactor; earlier releases live on a separate v0.x branch
- **−** RL training only; not a general agent runtime or builder
- **−** No Docker or compose files provided

<sub>GPU required · Needs verl, vLLM, uv, CUDA, Kubernetes (optional) · Models: Qwen3.5-9B, Qwen3.5-35B-A3B · [Repo](https://github.com/microsoft/agent-lightning) · [📖 Docs ↗](https://microsoft.github.io/agent-lightning/stable/) · [🌐 Site ↗](https://www.microsoft.com/en-us/research/project/agent-lightning/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-lightning/)</sub>

<a name="oumi"></a>
### #&#8288;15 [oumi](https://github.com/oumi-ai/oumi) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="model-optimizer"></a>
### #&#8288;16 [model-optimizer](https://github.com/nvidia/model-optimizer) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · Apache-2.0 · Nov 2026</sub>

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

<a name="openrlhf"></a>
### #&#8288;17 [openrlhf](https://github.com/openrlhf/openrlhf) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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

<a name="marin"></a>
### #&#8288;18 [marin](https://github.com/marin-community/marin) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · Apache-2.0 · Nov 2026</sub>

**Python platform for training LLMs from data curation through evaluation.**

Marin is a research program and Python framework for building foundation models: data curation, tokenization, pretraining, posttraining and evaluation. Experiments are written as dependent steps that run in topological order, like a Makefile, and scale from a tiny CPU run to GPU or TPU pods. It has produced an 8B model, a 32B model and the Delphi scaling suite.

- **+** Experiments are declared as dependent steps in Python, executed in topological order
- **+** Scales from a CPU tutorial run to GPU or TPU pods, including multislice TPUs
- **+** Publishes checkpoints, training scripts, mixture pipelines and retrospectives, including failed runs
- **+** Tutorials cover a tiny TinyStories model and a DCLM 1B/1x run
- **−** Research codebase tied to the project's own experiments; not a general fine-tuning tool
- **−** Large-scale runs need TPU or GPU clusters; no small-GPU recipe is given
- **−** No Docker or Compose setup in the repo
- **−** Current focus is a 500B+ MoE, so interfaces may shift with research needs

<sub>GPU optional · Docker · Needs Hugging Face datasets, Google TPU or GPU cluster for large runs · Models: Llama-architecture LLMs, mixture-of-experts LLMs · [Repo](https://github.com/marin-community/marin) · [📖 Docs ↗](https://marin.readthedocs.io/en/latest/) · [🌐 Site ↗](https://marin.community) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/marin/)</sub>

<a name="liger-kernel"></a>
### #&#8288;19 [liger-kernel](https://github.com/linkedin/liger-kernel) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.7k · BSD-2-Clause · Nov 2026</sub>

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
### #&#8288;20 [areal](https://github.com/areal-project/areal) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="simpletuner"></a>
### #&#8288;21 [simpletuner](https://github.com/bghira/simpletuner) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · AGPL-3.0 · Nov 2026</sub>

**Fine-tuning toolkit for diffusion image, video and audio models, with a web UI.**

SimpleTuner trains LoRA, LyCORIS and full-rank fine-tunes of diffusion and flow-matching models, including Flux, SDXL, SD3, Wan, LTX Video, Qwen Image and ACE-Step. It supports multi-GPU training, DeepSpeed and FSDP2, disk caching of embeddings, aspect bucketing and S3 datasets, and runs from a web UI or the command line. A multi-user mode adds SSO, role-based access, quotas and a job queue.

- **+** Covers about 40 model families across image, video and audio, with a quickstart per model
- **+** Memory options: int8/fp8/nf4 quantization, DeepSpeed, FSDP2; most models train on 24G
- **+** Multi-user mode with LDAP/OIDC SSO, RBAC, quotas and audit logging, all free
- **+** pip install with extras for CUDA, ROCm and Apple Silicon
- **−** AGPL-3.0 license carries copyleft obligations for modified network-served versions
- **−** Many supported base models have non-commercial or restricted licenses, varying by checkpoint
- **−** AMD uses more memory than NVIDIA; Apple needs M3 Max with 24GB+ unified memory
- **−** Multi-user and worker orchestration docs sit under an experimental path

<sub>GPU required · Docker + Compose · Needs PyTorch, Hugging Face Accelerate, DeepSpeed (optional) · Models: Flux.1, Flux.2, Stable Diffusion XL, Stable Diffusion 3, Wan Video · [Repo](https://github.com/bghira/simpletuner) · [📖 Docs ↗](https://github.com/bghira/SimpleTuner/blob/main/documentation/QUICKSTART.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/simpletuner/)</sub>

<a name="llamafactory"></a>
### #&#8288;22 [llamafactory](https://github.com/hiyouga/llamafactory) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: patchy (39) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 76k · Apache-2.0 · Nov 2026</sub>

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

<a name="fingpt"></a>
### #&#8288;23 [fingpt](https://github.com/ai4finance-foundation/fingpt) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (88) · Freshness: active (96) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Nov 2026</sub>

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

<a name="rlinf"></a>
### #&#8288;24 [rlinf](https://github.com/rlinf/rlinf) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · Apache-2.0 · Nov 2026</sub>

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

<a name="h2o-llmstudio"></a>
### #&#8288;25 [h2o-llmstudio](https://github.com/h2oai/h2o-llmstudio) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="sagemaker-python-sdk"></a>
### #&#8288;26 [sagemaker-python-sdk](https://github.com/aws/sagemaker-python-sdk) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · Apache-2.0 · Nov 2026</sub>

**Python SDK for training, fine-tuning and deploying models on Amazon SageMaker.**

Python library that wraps the SageMaker APIs to run training jobs, host endpoints, and manage pipelines, processing, tuning and model registry. V3 replaces Estimator/Model/Predictor with ModelTrainer and ModelBuilder, and adds SFT, DPO, RLAIF and RLVR trainers for foundation-model fine-tuning with LoRA or full tuning. It splits into sagemaker-core, -train, -serve and -mlops packages.

- **+** Unified ModelTrainer and ModelBuilder classes replace many framework-specific V2 classes
- **+** Fine-tuning trainers (SFT, DPO, RLAIF, RLVR) with LoRA or full tuning and MLflow metrics
- **+** Modular PyPI packages: sagemaker-core, sagemaker-train, sagemaker-serve, sagemaker-mlops
- **+** Covers pipelines, hyperparameter tuning, model registry, Clarify and batch transform; local mode available
- **−** Tied to AWS: training and hosting run on SageMaker and need IAM roles and S3
- **−** V3 breaks V2 interfaces (Estimator, Model, Predictor); existing code needs migration
- **−** Supports Unix/Linux and macOS only; tested on Python 3.10 to 3.12
- **−** Telemetry is on by default and must be disabled through SDK defaults config

<sub>GPU optional · Needs AWS account, Amazon SageMaker, Amazon S3, AWS IAM role · Models: PyTorch, Apache MXNet, Hugging Face, SageMaker JumpStart, SparkML (MLeap) · [Repo](https://github.com/aws/sagemaker-python-sdk) · [📖 Docs ↗](https://sagemaker.readthedocs.io/en/stable/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sagemaker-python-sdk/)</sub>

<a name="fractalworkspace"></a>
### #&#8288;27 [fractalworkspace](https://github.com/fractal-compute-orchestrations/fractalworkspace) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · custom license · Nov 2026</sub>

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

<a name="slime"></a>
### #&#8288;28 [slime](https://github.com/thudm/slime) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="skillopt"></a>
### #&#8288;29 [skillopt](https://github.com/microsoft/skillopt) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

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

<a name="swanlab"></a>
### #&#8288;30 [swanlab](https://github.com/swanhubx/swanlab) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · Apache-2.0 · Nov 2026</sub>

**Experiment tracking and dashboards for ML training runs.**

SwanLab is a Python SDK and dashboard for tracking ML training runs, similar in role to Weights & Biases. You call swanlab.init and swanlab.log to record metrics, hyperparameters, media and hardware stats, then compare experiments in a web UI. It integrates with PyTorch, Transformers, LLaMA Factory, veRL, Ultralytics and others, and offers a self-hosted community edition via Docker or Kubernetes.

- **+** Two-call integration: swanlab.init and swanlab.log, installed with pip install swanlab
- **+** Hardware monitoring covers Nvidia, AMD, Ascend, Cambricon, Kunlunxin, Hygon, MetaX, Moore Threads and Iluvatar
- **+** Integrations for many training frameworks, including veRL, trl, LLaMA Factory, Ultralytics and TensorBoard
- **+** Logs scalars, images, audio, video, text, 3D point clouds and molecules, plus custom Echarts charts
- **−** Main README and docs are Chinese-first; English README is a separate file
- **−** Default workflow needs a swanlab.cn account and API key for the cloud
- **−** Self-hosted community edition is described as offline dashboard viewing; feature limits vs cloud not detailed
- **−** Self-host setup lives in external docs; no compose file detected in the repo

<sub>Needs Docker or Kubernetes (self-hosting) · Models: PyTorch, HuggingFace Transformers, PyTorch Lightning, LLaMA Factory, veRL · [Repo](https://github.com/swanhubx/swanlab) · [▶️ Demo ↗](https://swanlab.cn/@ZeyiLin/swanlab-echarts-demo/charts) · [📖 Docs ↗](https://docs.swanlab.cn) · [🌐 Site ↗](https://swanlab.cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/swanlab/)</sub>

<a name="minimind"></a>
### #&#8288;31 [minimind](https://github.com/jingyaogong/minimind) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: widely used (97) · Freshness: active (82) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · Apache-2.0 · Nov 2026</sub>

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

<a name="llm-compressor"></a>
### #&#8288;32 [llm-compressor](https://github.com/vllm-project/llm-compressor) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · Apache-2.0 · Nov 2026</sub>

**Python library that quantizes and prunes Hugging Face models for vLLM.**

llmcompressor applies post-training quantization and expert pruning to Hugging Face models through a `oneshot` API driven by recipes. It supports GPTQ, AWQ, SmoothQuant, AutoRound, SpinQuant/QuIP rotations and REAP, across int8, FP8, NVFP4, MXFP4 and related schemes. Output is saved in the compressed-tensors format, which vLLM loads directly.

- **+** Wide scheme coverage: W8A8, W4A16, NVFP4, MXFP4/6/8, plus KV cache and attention quantization
- **+** Multiple algorithms selectable via recipe: GPTQ, AWQ, SmoothQuant, AutoRound, rotations, REAP pruning
- **+** Handles large models with DDP, sequential onloading and disk offloading
- **+** Checkpoints load directly in vLLM; many prebuilt checkpoints published under RedHatAI on Hugging Face
- **−** Output targets vLLM via compressed-tensors; other runtimes are not mentioned
- **−** Some features are labeled experimental, such as NVFP4 attention with SpinQuant
- **−** Users must choose scheme, algorithm and calibration setup themselves
- **−** Architectures without a shipped model definition need the model-free path

<sub>Needs PyTorch, Hugging Face Transformers, compressed-tensors, vLLM (for inference) · Models: Hugging Face Transformers LLMs, MoE models, Vision-language models, Audio-language models, compressed-tensors output · [Repo](https://github.com/vllm-project/llm-compressor) · [📖 Docs ↗](https://docs.vllm.ai/projects/llm-compressor/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-compressor/)</sub>

<a name="lightly"></a>
### #&#8288;33 [lightly](https://github.com/lightly-ai/lightly) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · MIT · Nov 2026</sub>

**PyTorch library for self-supervised vision pretraining and latent world models.**

LightlySSL is a Python framework of modular building blocks (loss functions, model heads, transforms) for self-supervised pretraining of computer vision models. It ships PyTorch and PyTorch Lightning examples for about 25 methods, including SimCLR, MoCo, BYOL, DINO, DINOv2, MAE and LeJEPA, plus LeWM for training world models and planning with them. Custom backbones are supported, and distributed training goes through PyTorch Lightning.

- **+** Covers MoCo (2019) through LeJEPA and Pixio (2025), each with docs and Colab notebooks
- **+** Modular losses and heads that can be mixed with custom backbones
- **+** PyTorch and PyTorch Lightning examples, including distributed, for every listed model
- **+** Adds LeWM for training a world model from frames and actions, with a tutorial
- **−** Computer vision only; no text or speech pretraining
- **−** Docker support and one-command pretraining are in the commercial edition
- **−** Library only: no UI, serving layer or pretrained model hub
- **−** LeWM requires PyTorch 2.0+ and the timm extra

<sub>Needs PyTorch 2.0+, timm, PyTorch Lightning · Models: MoCo, SimCLR, BYOL, SwAV, DINO · [Repo](https://github.com/lightly-ai/lightly) · [📖 Docs ↗](https://docs.lightly.ai/self-supervised-learning/) · [🌐 Site ↗](https://www.lightly.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lightly/)</sub>

<a name="mergekit"></a>
### #&#8288;34 [mergekit](https://github.com/arcee-ai/mergekit) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · LGPL-3.0 · Oct 2026</sub>

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

<a name="colossalai"></a>
### #&#8288;35 [colossalai](https://github.com/hpcaitech/colossalai) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (94) · Freshness: recent (70) · Maintenance: fair (62) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Nov 2026</sub>

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

<a name="maxtext"></a>
### #&#8288;36 [maxtext](https://github.com/ai-hypercomputer/maxtext) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Nov 2026</sub>

**JAX library for pre-training and post-training LLMs on TPUs and GPUs.**

MaxText is a pure Python/JAX reference implementation for training LLMs on Google Cloud TPUs and GPUs. It covers pre-training and post-training (SFT, GRPO, GSPO) for Gemma, Llama, DeepSeek, Qwen, Kimi, Mistral and GPT-OSS models. It is built on Flax, Tunix, Orbax, Optax and Grain, and uses vLLM for RL sampling.

- **+** Large model library: Gemma, Llama, DeepSeek V4, Qwen 3.x, Kimi K2.x, GPT-OSS, Mixtral
- **+** Pre-training and post-training (SFT, GRPO, GSPO) in one codebase
- **+** Scales from a single host to tens of thousands of chips
- **+** Installable from PyPI, with versioned releases and release notes
- **−** Primarily targets Google Cloud TPUs; GPU support is secondary
- **−** README says the main branch is not production-ready; use PyPI releases
- **−** Python 3.12 is the primary supported version; others may have issues
- **−** Diffusion models are in a separate repo (MaxDiffusion)

<sub>GPU optional · Needs JAX, Flax, Tunix, Orbax, Optax, Grain, vLLM, Google Cloud TPU · Models: Gemma, Llama, DeepSeek, Qwen, Kimi · [Repo](https://github.com/ai-hypercomputer/maxtext) · [📖 Docs ↗](https://maxtext.readthedocs.io/en) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/maxtext/)</sub>

<a name="litgpt"></a>
### #&#8288;37 [litgpt](https://github.com/lightning-ai/litgpt) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

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

<a name="miles"></a>
### #&#8288;38 [miles](https://github.com/radixark/miles) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · Apache-2.0 · Nov 2026</sub>

**RL post-training framework pairing SGLang rollout with Megatron-LM training.**

Miles is a Python reinforcement learning framework for post-training large models. It uses SGLang for rollout generation and Megatron-LM for training, with FSDP2 and torchtitan backends also supported. It covers GRPO, GSPO, PPO, REINFORCE++, SFT and on-policy distillation, and runs on Ray or Kubernetes via Helm. It was forked from slime.

- **+** Fully async rollout and training workers, with configurable on- and off-policy schedules
- **+** Recovers a dead SGLang engine in place and resumes the run without a restart
- **+** Supports MXFP8, NVFP4, FP8, INT4 QAT, BF16, FP16, plus LoRA and multi-LoRA
- **+** Runs on NVIDIA (A100 to GB300) and AMD (MI300X to MI355X) GPUs
- **−** Aimed at multi-GPU clusters; the README gives no single-GPU or small-scale path
- **−** Requires SGLang and Megatron-LM stacks, which adds setup work
- **−** No Dockerfile or compose file detected in the repository
- **−** Diffusion RL lives in a separate repository, miles_diffusion

<sub>GPU required · Docker · Needs SGLang, Megatron-LM, Ray, Kubernetes (optional, via Helm) · Models: DeepSeek-V4, Kimi-K2.6, Kimi-K3, Qwen3.5, Qwen3.8 · [Repo](https://github.com/radixark/miles) · [📖 Docs ↗](https://miles.radixark.com/docs) · [🌐 Site ↗](https://miles.radixark.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/miles/)</sub>

<a name="veomni"></a>
### #&#8288;39 [veomni](https://github.com/bytedance-seed/veomni) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · Apache-2.0 · Nov 2026</sub>

**PyTorch distributed training framework for text, vision-language and omni models.**

VeOmni is a PyTorch-native framework for pre-training and post-training text, multimodal and diffusion-transformer models. It uses FSDP2, DeepSpeed Ulysses sequence parallelism and expert parallelism for MoE models, and loads HuggingFace Transformers models. Training runs from linear scripts rather than a mandatory Trainer class, with a basic trainer and an RL trainer backend also provided.

- **+** Combines FSDP2, Ulysses sequence parallelism and expert parallelism for large MoE training
- **+** Example configs for Qwen3, Qwen3-VL, DeepSeek, Llama3, GPT-OSS, Wan and LTX-2.3
- **+** Runs on NVIDIA GPU, AMD ROCm, Ascend NPU and Cambricon MLU
- **+** Linear training scripts expose the full training loop instead of hiding it in a Trainer
- **−** RL post-training for omni models with VeRL is listed as upcoming
- **−** Some model support is marked experimental, such as HunyuanVideo 1.5
- **−** No Docker or compose files detected for setup
- **−** Validation dataset during training is still a planned feature

<sub>GPU required · Docker · Needs PyTorch, HuggingFace Transformers, Liger-Kernel, wandb (optional tracking) · Models: Qwen2/3, Qwen3-VL, Qwen3-MoE, Qwen Omni, DeepSeek · [Repo](https://github.com/bytedance-seed/veomni) · [📖 Docs ↗](https://veomni.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/veomni/)</sub>

<a name="trainer"></a>
### #&#8288;40 [trainer](https://github.com/kubeflow/trainer) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · Apache-2.0 · Nov 2026</sub>

**Kubernetes operator for distributed training and LLM fine-tuning jobs.**

Kubeflow Trainer is a Kubernetes-native system that runs distributed training and fine-tuning through TrainJob and Runtime APIs. It supports PyTorch, MLX, HuggingFace, DeepSpeed, Megatron-LM, JAX and XGBoost, plus MPI for multi-node, multi-GPU jobs. It builds on JobSet and LeaderWorkerSet, and integrates with Kueue, KAI Scheduler and Slurm Bridge.

- **+** Covers PyTorch, JAX, XGBoost, DeepSpeed, MLX and Megatron-LM runtimes under one TrainJob API
- **+** MPI runtime for multi-node, multi-GPU jobs on Kubernetes
- **+** Integrates with Kueue, Slurm Bridge and KAI Scheduler for scheduling
- **+** Distributed data cache streams datasets to GPU nodes
- **−** Project is alpha status; the README warns APIs may change
- **−** Requires a Kubernetes cluster; not usable on a single workstation
- **−** Migration needed from Training Operator V1, which is maintained only on release-1.9
- **−** Python SDK lives in a separate repository (kubeflow/sdk)

<sub>GPU optional · Needs Kubernetes, Helm, JobSet, LeaderWorkerSet · Models: PyTorch, MLX, HuggingFace, DeepSpeed, Megatron-LM · [Repo](https://github.com/kubeflow/trainer) · [📖 Docs ↗](https://trainer.kubeflow.org/en/latest/getting-started/index.html) · [🌐 Site ↗](https://trainer.kubeflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trainer/)</sub>

<a name="prime-rl"></a>
### #&#8288;41 [prime-rl](https://github.com/primeintellect-ai/prime-rl) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · Apache-2.0 · Nov 2026</sub>

**Asynchronous RL trainer for large LLMs, built on FSDP2 and vLLM.**

prime-rl is a Python framework for SFT, asynchronous RL training and evals of LLMs, using FSDP2 for training and vLLM for inference. It targets multi-node Slurm clusters of 1000+ GPUs, with expert and context parallelism for MoE models, and integrates with verifiers environments from the Environments Hub. Small single-GPU examples are included for getting started.

- **+** Async RL with FSDP2 training and vLLM inference, including FP8 inference and PD disaggregation
- **+** Expert and context parallelism for MoE families such as GLM-5, Qwen3 MoE, GPT-OSS
- **+** Examples scale from one consumer GPU to Slurm clusters of 32-2048 GPUs
- **+** SFT, RL and evals in one stack, with verifiers environments
- **−** Requires at least one NVIDIA GPU; no CPU-only training path
- **−** Trainer supports only listed model architectures; others fail at setup
- **−** Full RL stack check needs 2 GPUs (inference plus trainer)
- **−** Environments are opt-in workspace members and need a separate install

<sub>GPU required · Docker · Needs NVIDIA GPU, uv, vLLM, flash-attn, Python 3.12, Slurm (multi-node), W&B (optional) · Models: Llama, Qwen3, Qwen3.5, GLM-4/4.5/5, GPT-OSS · [Repo](https://github.com/primeintellect-ai/prime-rl) · [📖 Docs ↗](https://github.com/PrimeIntellect-ai/prime-rl/tree/main/docs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/prime-rl/)</sub>

<a name="nnunet"></a>
### #&#8288;42 [nnunet](https://github.com/mic-dkfz/nnunet) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (71) · Freshness: recent (70) · Maintenance: fair (64) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.1k · Apache-2.0 · Nov 2026</sub>

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

<a name="ludwig"></a>
### #&#8288;43 [ludwig](https://github.com/ludwig-ai/ludwig) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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

<a name="ml-agents"></a>
### #&#8288;44 [ml-agents](https://github.com/unity-technologies/ml-agents) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: widely used (87) · Freshness: recent (78) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · custom license · Oct 2026</sub>

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

<a name="ignite"></a>
### #&#8288;45 [pytorch/ignite](https://github.com/pytorch/ignite) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: fair (51) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · BSD-3-Clause · Nov 2026</sub>

**PyTorch library for training and evaluating models with engines, events and metrics.**

Ignite is a Python library on top of PyTorch that replaces hand-written epoch and iteration loops with an Engine object plus event handlers. It ships metrics (Precision, Recall, Accuracy, Confusion Matrix, IoU, about 20 regression metrics) and handlers for saving artifacts and logging. It is used as a library, so the training script keeps control flow.

- **+** Handlers can be any callable, with no base class to inherit
- **+** Event filtering (every, once, custom filter), stacking with |, and custom events
- **+** Metrics can be composed with arithmetic and torch methods
- **+** Library approach: no inversion of control over your training script
- **−** Tied to PyTorch; no support for other frameworks
- **−** Full-featured template examples are listed as coming soon
- **−** Reproducible example logs on the Ignite Trains server are listed as coming soon
- **−** You still write the train step yourself; it is not a turnkey trainer

<sub>GPU optional · Docker · Needs PyTorch · Models: PyTorch models · [Repo](https://github.com/pytorch/ignite) · [▶️ Demo ↗](https://code-generator.pytorch-ignite.ai/) · [📖 Docs ↗](https://pytorch.org/ignite/) · [🌐 Site ↗](https://pytorch-ignite.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ignite/)</sub>

<a name="medicalgpt"></a>
### #&#8288;46 [medicalgpt](https://github.com/shibing624/medicalgpt) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (58) · Freshness: active (97) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Sep 2026</sub>

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
### #&#8288;47 [transformerlab-app](https://github.com/transformerlab/transformerlab-app) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (52) · Freshness: active (95) · Maintenance: weak (27) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · AGPL-3.0 · Aug 2026</sub>

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

<a name="rl"></a>
### #&#8288;48 [rl](https://github.com/nvidia-nemo/rl) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Nov 2026</sub>

**Ray-based RL post-training library for LLMs and VLMs.**

NeMo RL is an NVIDIA post-training library that runs GRPO, GSPO, DAPO, DPO, SFT with LoRA, reward modeling and on-policy distillation on LLMs and VLMs. It uses Ray for orchestration, Automodel (PyTorch FSDP2/TP/CP/EP) or Megatron Core for training, and vLLM, SGLang or Megatron inference for rollouts. It scales from one node to multi-node clusters.

- **+** Two training backends: PyTorch-native Automodel and Megatron Core with TP/PP/CP/SP/EP parallelism
- **+** Covers GRPO, GSPO, DAPO, GDPO, PPO, DPO, SFT with LoRA, and distillation
- **+** Rollouts via vLLM, SGLang or Megatron inference, with async RL and multi-turn tool use
- **+** Used to post-train NVIDIA Nemotron models, with reproducible recipes in the repo
- **−** Targets NVIDIA GPUs and CUDA; the README describes no CPU or non-NVIDIA path
- **−** Support for many newer models lives on separate branches, not main
- **−** Resiliency and auto-scaling are listed as not yet available
- **−** Setup involves Ray, git submodules and two backends, which is heavy for small experiments

<sub>GPU required · Docker · Needs Ray, vLLM, SGLang, NeMo Automodel, Megatron Bridge, CUDA, Hugging Face · Models: Qwen3.5, GLM-4.7-Flash, Nemotron 3, Gemma 4, Hugging Face models · [Repo](https://github.com/nvidia-nemo/rl) · [📖 Docs ↗](https://docs.nvidia.com/nemo/rl/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rl/)</sub>

<a name="polyaxon"></a>
### #&#8288;49 [polyaxon](https://github.com/polyaxon/polyaxon) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (41) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · Apache-2.0 · Nov 2026</sub>

**Kubernetes platform for tracking, running and tuning machine learning experiments.**

Polyaxon is a Kubernetes-based platform that runs and tracks ML training jobs, notebooks and TensorBoard from a CLI and a web dashboard. It includes hyperparameter search (grid, random, Hyperband, Bayesian, Hyperopt), distributed job operators for TensorFlow, PyTorch, MPI, Spark and Dask, and container-native DAG pipelines. It targets teams sharing GPU servers.

- **+** Built-in hyperparameter search: grid, random, Hyperband, Bayesian optimization, Hyperopt and custom iterative
- **+** Distributed training via operators for TensorFlow, PyTorch, MPI, Horovod, Spark and Dask
- **+** DAG engine runs jobs, services, distributed jobs and nested DAGs as pipeline steps
- **+** CLI and dashboard launch Jupyter notebooks and TensorBoard per project
- **−** Deployment needs a Kubernetes cluster and Helm; no single-machine path described
- **−** README lists TensorFlow, MXNet, Caffe and Torch; no LLM-specific tooling mentioned
- **−** Distributed jobs need a per-framework operator and code changes before they work
- **−** No GitHub release published, though the README badge shows v2.16.1

<sub>GPU optional · Needs Kubernetes, Helm, kubectl · Models: TensorFlow, PyTorch, MXNet, Caffe, Torch · [Repo](https://github.com/polyaxon/polyaxon) · [📖 Docs ↗](https://polyaxon.com/docs/) · [🌐 Site ↗](https://polyaxon.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/polyaxon/)</sub>

<a name="roll"></a>
### #&#8288;50 [roll](https://github.com/alibaba/roll) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (38) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · Apache-2.0 · Nov 2026</sub>

**Ray-based reinforcement learning library for post-training LLMs on GPU clusters.**

ROLL is an Alibaba library for reinforcement learning on large language models, covering RLVR (math, code, reasoning), multi-turn agentic RL, distillation, DPO and SFT pipelines. It uses Ray to place roles across GPUs, with vLLM or SGLang for generation and FSDP2 or Megatron-Core for training. Algorithms include PPO, GRPO, GSPO, Reinforce++, TOPR and GiGPO.

- **+** Supports Megatron-LM 5D parallelism and FSDP2, scaling from one node to large clusters
- **+** Generation runs on vLLM or SGLang; training on FSDP2 or Megatron
- **+** Async rollout and async training for both RLVR and agentic pipelines
- **+** Runs on NVIDIA, AMD and Huawei Ascend hardware; logs to SwanLab, WandB, TensorBoard
- **−** Needs multi-GPU infrastructure and Ray; not practical on a single consumer GPU
- **−** No Dockerfile or compose file detected in the repository
- **−** Some features are labeled under development, such as FP8 rollout with BF16 training
- **−** Many YAML configs and backend choices make initial setup involved

<sub>GPU required · Docker · Needs Ray, vLLM, SGLang, Megatron-Core, FSDP2 · Models: Qwen2.5, Qwen3, Qwen3-MoE, Qwen3-Next, Qwen3.5 · [Repo](https://github.com/alibaba/roll) · [📖 Docs ↗](https://alibaba.github.io/ROLL/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/roll/)</sub>

<a name="microduck-rl"></a>
### #&#8288;51 [microduck_rl](https://github.com/pollen-robotics/microduck_rl) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (33) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Nov 2026</sub>

**PPO training environments for the Microduck biped robot.**

RL training environments for the ~800 g Microduck biped, built on mjlab (MuJoCo Warp) with PPO at 50 Hz. Tasks include walking, fall recovery, roulade, ball kick and roller-skating, using BAM actuator models, domain randomization and optional gear backlash. Policies export to ONNX with the normalizer baked in and can be published to the Hugging Face Hub for the robot runtime.

- **+** 13 task families, many with Flat/Rough or Backlash variants, sharing one 61-dim observation contract
- **+** Actuator modeled with BAM voltage control law, friction and voltage randomization for sim2real
- **+** ONNX export bakes in the normalizer; publish command checks graph shape and NaNs
- **+** Usable walking gait in about 1-2 h at 4096 envs
- **−** Local training requires a CUDA GPU; the no-GPU path depends on Hugging Face Jobs
- **−** Tied to the Microduck robot; other hardware needs new MJCF models and tasks
- **−** STL mesh assets are CC BY-NC-SA 4.0, not Apache-2.0, so non-commercial
- **−** Deployment relies on the separate microduck runtime repository

<sub>GPU required · Needs uv, mjlab, MuJoCo Warp, BAM, Weights & Biases, Hugging Face Hub · Models: PPO policies, ONNX export · [Repo](https://github.com/pollen-robotics/microduck_rl) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/microduck-rl/)</sub>

<a name="lycoris"></a>
### #&#8288;52 [lycoris](https://github.com/kohakublueleaf/lycoris) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Oct 2026</sub>

**Parameter-efficient fine-tuning library with LoRA, LoHa and LoKr for Stable Diffusion.**

LyCORIS is a PyTorch library implementing LoRA (LoCon), LoHa, LoKr, (IA)^3, DyLoRA and native fine-tuning, mainly for Stable Diffusion. It plugs into kohya-ss/sd-scripts and Naifu, or wraps arbitrary PyTorch modules through a standalone API. Version 4.0.0 adds experimental Triton and TileLang kernels with automatic fallback to PyTorch.

- **+** Many adapter algorithms (LoRA, LoHa, LoKr, IA3, DyLoRA, OFT, DoRA) behind one API
- **+** Works with kohya-ss/sd-scripts, Naifu, or as a wrapper for any PyTorch module
- **+** Output loads in sd-webui 1.5+, ComfyUI, InvokeAI and CivitAI
- **+** Includes extract, merge and conversion scripts; adapters can be stacked and removed
- **−** Triton/TileLang fused kernels are labeled early experimental
- **−** HCP-Diffusion training support was dropped in 3.0.0
- **−** GLoRA and GLoKr are listed as coming soon; library-wide docs are still a todo
- **−** Newer algorithm types may not load in third-party UIs and trainer GUIs

<sub>GPU optional · Needs PyTorch, kohya-ss/sd-scripts (optional), triton or tilelang (optional) · Models: Stable Diffusion 1.x/2.x, SDXL, Phi-1.5, any PyTorch module · [Repo](https://github.com/kohakublueleaf/lycoris) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lycoris/)</sub>

<a name="easyedit"></a>
### #&#8288;53 [easyedit](https://github.com/zjunlp/easyedit) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: known (32) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Nov 2026</sub>

**Python toolkit for editing facts and behavior in LLMs without retraining.**

EasyEdit is a Python framework for knowledge editing of large language models. It implements methods such as ROME, MEMIT, MEND, GRACE, WISE, AlphaEdit and AdaLoRA behind a BaseEditor interface, and evaluates them on the KnowEdit benchmark. EasyEdit2 adds inference-time steering of model behavior without retraining.

- **+** Many editing methods (ROME, MEMIT, MEND, GRACE, WISE, AlphaEdit) behind one API
- **+** Includes KnowEdit benchmark and evaluation scripts
- **+** Supports multimodal editing, multi-GPU editing via Accelerate, and vLLM
- **+** Hosted demo and tutorial notebooks
- **−** Research toolkit: no server, UI or production serving layer
- **−** Each method needs a per-model hyperparameter YAML file
- **−** No tagged release; version badge still reads v0.0.1
- **−** Edits can affect unrelated knowledge, which is why lifelong methods exist

<sub>GPU required · Docker · Needs PyTorch, Hugging Face Transformers · Models: Llama, Mistral, Baichuan2, ChatGLM2, InternLM · [Repo](https://github.com/zjunlp/easyedit) · [▶️ Demo ↗](https://huggingface.co/spaces/zjunlp/EasyEdit) · [📖 Docs ↗](https://ribbon-muskox-3ac.notion.site/EasyEdit1-0-213e624c1c2680318840d9abbdaa83c5) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/easyedit/)</sub>

<a name="rl-baselines3-zoo"></a>
### #&#8288;54 [rl-baselines3-zoo](https://github.com/dlr-rm/rl-baselines3-zoo) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (32) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Nov 2026</sub>

**Training and tuning scripts with tuned hyperparameters for Stable Baselines3.**

RL Baselines3 Zoo wraps Stable Baselines3 with command-line scripts to train, evaluate, tune hyperparameters, plot results and record videos. Per-algorithm YAML files hold tuned hyperparameters for common environments, and 200+ pretrained agents are listed on Hugging Face. It installs as the rl_zoo3 Python package.

- **+** Tuned hyperparameters in per-algorithm YAML files, e.g. hyperparameters/algo_name.yml
- **+** 200+ pretrained agents on Hugging Face, with final scores in benchmark.md
- **+** Covers Atari, Box2D, PyBullet, MuJoCo, MiniGrid and Panda robot environments
- **+** Integrates with Weights & Biases and Hugging Face; Colab notebook included
- **−** Tied to Stable Baselines3 algorithms and Gym-style environments
- **−** Benchmark is one run per agent, not a quantitative comparison
- **−** Pretrained agents need a recursive git clone for the submodule
- **−** Not meant for interactive sessions; notebooks need a sys.argv workaround

<sub>Docker · Needs stable-baselines3, swig, cmake, ffmpeg · Models: A2C, PPO, DQN, QR-DQN, DDPG · [Repo](https://github.com/dlr-rm/rl-baselines3-zoo) · [▶️ Demo ↗](https://colab.research.google.com/github/Stable-Baselines-Team/rl-colab-notebooks/blob/sb3/rl-baselines-zoo.ipynb) · [📖 Docs ↗](https://rl-baselines3-zoo.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rl-baselines3-zoo/)</sub>

<a name="setfit"></a>
### #&#8288;55 [setfit](https://github.com/huggingface/setfit) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Oct 2026</sub>

**Few-shot text classification by fine-tuning Sentence Transformers, no prompts.**

SetFit fine-tunes a pretrained Sentence Transformer body plus a classification head (scikit-learn or a differentiable PyTorch SetFitHead) on a few labeled examples per class. It provides SetFitModel and Trainer classes integrated with the Hugging Face Hub for training, saving, pushing and inference. The README example trains on 8 samples per class on SST-2 and reports 0.869 accuracy.

- **+** No prompts or verbalizers needed; works from embeddings of the raw text
- **+** Trains on as few as 8 labeled examples per class
- **+** Works with any Sentence Transformer on the Hub, including multilingual checkpoints
- **+** Trainer and TrainingArguments API with Hub push and load, installed via pip
- **−** Text classification only; not a general LLM fine-tuning tool
- **−** Built on Sentence Transformers, so results depend on the chosen base checkpoint
- **−** No hardware requirements documented in the README
- **−** README is brief; detailed guides live on the Hugging Face docs site

<sub>Needs sentence-transformers, datasets, scikit-learn, PyTorch, Hugging Face Hub · Models: Sentence Transformers · [Repo](https://github.com/huggingface/setfit) · [📖 Docs ↗](https://huggingface.co/docs/setfit) · [🌐 Site ↗](https://huggingface.co/setfit) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/setfit/)</sub>

<a name="nanochat"></a>
### #&#8288;56 [nanochat](https://github.com/karpathy/nanochat) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: widely used (96) · Freshness: active (80) · Maintenance: weak (3) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 61k · MIT · Jul 2026</sub>

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

<a name="rllm"></a>
### #&#8288;57 [rllm](https://github.com/rllm-org/rllm) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: popular (59) · Freshness: active (98) · Maintenance: weak (26) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

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

<a name="auto-round"></a>
### #&#8288;58 [auto-round](https://github.com/intel/auto-round) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (5) · Freshness: active (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · Apache-2.0 · Oct 2026</sub>

**Post-training quantization toolkit for LLMs and VLMs, with GGUF and GPTQ/AWQ export.**

AutoRound quantizes LLMs and vision-language models after training using SignRound-based rounding optimization, via a CLI or a Python API. It supports W2A16 to W8A16, MXFP4, NVFP4, and FP8 schemes, and exports to AutoRound, AutoGPTQ, AutoAWQ, llm-compressor, and GGUF formats. Quantized models load in Transformers, vLLM, and SGLang on Intel CPUs/XPUs, Gaudi, and NVIDIA GPUs.

- **+** Exports to AutoRound, AutoGPTQ, AutoAWQ, llm-compressor and GGUF from one tool
- **+** Recipes trade speed for accuracy, from pure RTN to a slower fully tuned recipe
- **+** AutoScheme generates mixed-bit recipes with about 1.1-1.5x the BF16 model size in RAM
- **+** Runs on Intel CPU/XPU, Gaudi and CUDA; 7B models quantize in about 10 minutes on one GPU
- **−** Several features are marked experimental or WIP, including RRQ, algorithm composition and the MoE speedup
- **−** MXFP4 has no real inference kernels, per the README
- **−** Highest-accuracy recipe is 3-5x slower than the default
- **−** Default calibration dataset is under review, so results may shift between releases

<sub>GPU optional · Needs PyTorch, Transformers · Models: LLMs, VLMs, GGUF, GPTQ, AWQ · [Repo](https://github.com/intel/auto-round) · [📖 Docs ↗](https://github.com/intel/auto-round/blob/main/docs/step_by_step.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/auto-round/)</sub>

<a name="talos"></a>
### #&#8288;59 [talos](https://github.com/autonomio/talos) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (4) · Freshness: active (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Nov 2026</sub>

**Hyperparameter sweeps for Keras, TensorFlow and PyTorch models.**

Talos runs hyperparameter experiments around a model and training code you already wrote in Keras, TensorFlow or PyTorch. It offers a notebook Scan interface, plus single-file experiment definitions with manifests and a CLI. It records trial histories and checkpoints and can restore trained models. Talos 2 supports Python 3.11-3.13; the 1.x line stays available for Python 3.10/3.11.

- **+** You keep your own model, data splits and training loop; Talos wraps them
- **+** Content-addressed manifests and recorded trial histories support reproducible experiments
- **+** Grid and sampled searches, reducers and custom strategies
- **+** Same executor serves notebooks, single-file definitions and a CLI
- **−** Talos 1.x uses a legacy TensorFlow 2.14.1 dependency set with known advisories
- **−** Talos 2 needs Python 3.11 or newer; older environments must stay on 1.4
- **−** Tuning only: no serving, data tooling or training stack included
- **−** Moving from 1.x to Talos 2 requires following a separate migration guide

<sub>GPU optional · Needs Python 3.11-3.13, Keras, TensorFlow, PyTorch · Models: Keras, TensorFlow/tf.keras, PyTorch · [Repo](https://github.com/autonomio/talos) · [📖 Docs ↗](https://autonomio.github.io/talos/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/talos/)</sub>

<a name="gpt-neox"></a>
### #&#8288;60 [gpt-neox](https://github.com/eleutherai/gpt-neox) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (66) · Freshness: recent (70) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Nov 2026</sub>

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

<a name="alignment-handbook"></a>
### #&#8288;61 [alignment-handbook](https://github.com/huggingface/alignment-handbook) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · Apache-2.0 · Sep 2026</sub>

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
### #&#8288;62 [xtuner](https://github.com/internlm/xtuner) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (54) · Freshness: recent (73) · Maintenance: patchy (41) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="reagent"></a>
### #&#8288;63 [reagent](https://github.com/facebookresearch/reagent) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (41) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · BSD-3-Clause · Nov 2026</sub>

**Archived Meta platform for offline reinforcement learning on PyTorch.**

ReAgent is a Python platform from Meta for applied reinforcement learning, using PyTorch for training and TorchScript for serving. It covers data preprocessing, feature transformation, distributed training and counterfactual policy evaluation, with off-policy algorithms such as DQN variants, SAC, TD3, PPO and bandits. The repository is archived and no longer maintained; the README points to Pearl as the successor.

- **+** Broad algorithm set: DQN variants, TD3, SAC, CRR, PPO, SlateQ, Seq2Slate, bandits
- **+** Counterfactual policy evaluation (Doubly Robust, MAGIC) to test policies without deploying
- **+** Offline batch training workflow with TorchScript model serving
- **+** Includes Domain Analysis Tool and Behavior Cloning for bootstrapping real-world RL
- **−** Officially archived and unmaintained; README directs users to Pearl
- **−** No tagged releases
- **−** Aimed at large-scale offline recommendation tasks, not simulator-based RL
- **−** Copyright notice is 2022, so dependencies may be outdated

<sub>Needs PyTorch, TorchScript · Models: PyTorch, TorchScript · [Repo](https://github.com/facebookresearch/reagent) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/reagent/)</sub>

<a name="deepmd-kit"></a>
### #&#8288;64 [deepmd-kit](https://github.com/deepmodeling/deepmd-kit) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · LGPL-3.0 · Nov 2026</sub>

**Train and fine-tune machine-learning interatomic potentials for molecular dynamics.**

DeePMD-kit trains Deep Potential models from quantum-mechanical reference data and runs them in molecular dynamics engines such as LAMMPS, i-PI and ASE. It ships pretrained DPA4 checkpoints for inorganic materials (OMat24) that can be fine-tuned with `dp --pt train --finetune`. Models can be trained on TensorFlow, PyTorch, JAX or Paddle, depending on the model and feature.

- **+** Pretrained DPA4 checkpoints (Nano to Plus) with matching configs for fine-tuning
- **+** Supports TensorFlow, PyTorch, JAX and Paddle backends, with conversion for compatible models
- **+** Interfaces for Python, C, C++, Node.js, LAMMPS, i-PI, ASE, GROMACS and OpenMM
- **+** Model compression claims over 10x inference speedup on supported descriptors
- **−** Backend and interface support varies by model and feature, so compatibility needs checking per page
- **−** DPA4C needs the separate `--pt-expt` backend; its compressed CUDA path requires float32
- **−** Pretrained models cover the OMat24 inorganic chemical space; other domains need validation
- **−** ROCm is supported only through source builds

<sub>GPU optional · Needs Python 3.10+, LAMMPS (optional), i-PI (optional) · Models: DPA4, DPA4C, DPA-ADAPT, Deep Potential, MACE and NequIP via DeePMD-GNN plugin · [Repo](https://github.com/deepmodeling/deepmd-kit) · [📖 Docs ↗](https://docs.deepmodeling.com/projects/deepmd/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepmd-kit/)</sub>

<a name="lightly-train"></a>
### #&#8288;65 [lightly-train](https://github.com/lightly-ai/lightly-train) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · AGPL-3.0 · Nov 2026</sub>

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

<a name="onetrainer"></a>
### #&#8288;66 [onetrainer](https://github.com/nerogar/onetrainer) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (36) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · AGPL-3.0 · Nov 2026</sub>

**Training tool for fine-tuning and LoRA of diffusion models, with GUI and CLI.**

OneTrainer trains diffusion models through a desktop GUI or command-line scripts. It supports full fine-tuning, LoRA and embeddings for models including SD 1.5, SDXL, SD 3.5, FLUX.1, Flux.2, Qwen Image, Z-Image, Chroma, Sana and Hunyuan Video. It also bundles dataset captioning (BLIP, BLIP2, WD-1.4), mask generation (ClipSeg, Rembg) and model format conversion.

- **+** Covers many diffusion architectures, from SD 1.5 to Flux.2 and Hunyuan Video
- **+** Masked training, aspect ratio bucketing, EMA and multi-resolution training built in
- **+** Includes auto-captioning, mask creation and model conversion tools alongside the trainer
- **+** Automatic backups allow resuming training; TensorBoard integration for monitoring
- **−** Only diffusers and ckpt model formats are listed
- **−** No Docker or compose setup; install is via Python venv scripts
- **−** Requires Python 3.11.1 or newer, below 3.14
- **−** No tagged releases; users track the repository with update scripts

<sub>Needs Python >=3.11.1,<3.14, tkinter, libGL (Linux), TensorBoard · Models: Stable Diffusion 1.5/2.x/3.x, SDXL, FLUX.1, Flux.2, Qwen Image · [Repo](https://github.com/nerogar/onetrainer) · [📖 Docs ↗](https://github.com/Nerogar/OneTrainer/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onetrainer/)</sub>

<a name="easy-dataset"></a>
### #&#8288;67 [easy-dataset](https://github.com/conardli/easy-dataset) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: widely used (81) · Freshness: recent (66) · Maintenance: weak (6) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · May 2026</sub>

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

<a name="lmflow"></a>
### #&#8288;68 [lmflow](https://github.com/optimalscale/lmflow) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (69) · Freshness: recent (69) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · Apache-2.0 · Aug 2026</sub>

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

<sub>GPU required · Needs Python 3.9+, conda, mpi4py, PyTorch, WandB (optional, on by default) · Models: Hugging Face decoder models, LLaMA, Llama-2, Llama-3, Qwen · [Repo](https://github.com/optimalscale/lmflow) · [📖 Docs ↗](https://optimalscale.github.io/LMFlow/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmflow/)</sub>

<a name="the-well"></a>
### #&#8288;69 [the_well](https://github.com/polymathicai/the_well) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (48) · Freshness: active (83) · Maintenance: weak (26) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · BSD-3-Clause · Oct 2026</sub>

**PyTorch datasets and benchmarks of physics simulations for PDE surrogate models.**

The Well is a collection of 16 numerical simulation datasets, 15TB in total, covering fluid dynamics, acoustic scattering, biological systems and astrophysical MHD. The package provides a PyTorch WellDataset class, a download CLI, Hugging Face streaming, and a Hydra-configured training script with baseline models such as FNO and pretrained checkpoints.

- **+** 16 datasets from domain scientists, each between 6.9GB and 5.1TB
- **+** WellDataset plugs into a standard PyTorch DataLoader
- **+** Download with the-well-download or stream from Hugging Face
- **+** Hydra configs and pretrained baseline checkpoints for reproducing the benchmark
- **−** Full collection needs 15TB of disk; streaming is slower for large training
- **−** Benchmark models are simple baselines, not state-of-the-art, per the README
- **−** viscoelastic_instability is deprecated for processing errors; use the v2 dataset
- **−** Limited to physics simulation data, not a general-purpose ML library

<sub>GPU optional · Needs Python >=3.10, PyTorch, Hydra, Hugging Face Hub · Models: FNO · [Repo](https://github.com/polymathicai/the_well) · [📖 Docs ↗](https://polymathic-ai.org/the_well/) · [🌐 Site ↗](https://polymathic-ai.org/the_well/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/the-well/)</sub>

<a name="text-to-text-transfer-transformer"></a>
### #&#8288;70 [text-to-text-transfer-transformer](https://github.com/google-research/text-to-text-transfer-transformer) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (63) · Freshness: recent (70) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · Apache-2.0 · Oct 2026</sub>

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

<a name="angelslim"></a>
### #&#8288;71 [angelslim](https://github.com/tencent/angelslim) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: patchy (39) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · custom license · Nov 2026</sub>

**Quantization, speculative decoding and sparse attention toolkit for compressing LLMs.**

AngelSlim is a Python toolkit from Tencent that compresses models through quantization (FP8, INT8, INT4 GPTQ/AWQ, NVFP4/MXFP4, 1.25-bit and ternary), speculative-decoding training (Eagle3, MTP, DFlare), sparse attention and distillation. It covers LLMs, VLMs, diffusion and speech models, and Tencent publishes quantized weights and GGUF builds on Hugging Face. It installs with pip, and the AngelSpec training framework is bundled as a git submodule.

- **+** Covers FP8, INT4, NVFP4/MXFP4 and sub-2-bit quantization in one toolkit
- **+** Supports LLMs, VLMs, diffusion and speech models, including Qwen, DeepSeek and Hunyuan
- **+** Includes Eagle3 and MTP speculative-decoding training, plus sparse attention and distillation
- **+** Publishes ready quantized weights and GGUF models on Hugging Face
- **−** Compresses models but does not serve them; deployment relies on other engines
- **−** Several newer method links in the README point to a generic readthedocs URL
- **−** License is reported as NOASSERTION, so terms need checking
- **−** Many documentation links point to zh-cn paths

<sub>Needs AngelSpec (git submodule) · Models: Hunyuan, Qwen3, Qwen2.5, Qwen3-VL, DeepSeek-V3/R1 · [Repo](https://github.com/tencent/angelslim) · [📖 Docs ↗](https://angelslim.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/angelslim/)</sub>

<a name="torchdistill"></a>
### #&#8288;72 [torchdistill](https://github.com/yoshitomo-matsubara/torchdistill) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (4) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Aug 2026</sub>

**YAML-configured PyTorch framework for knowledge distillation experiments.**

torchdistill is a PyTorch library for knowledge distillation where experiments are declared in a PyYAML config instead of Python code. A ForwardHookManager extracts intermediate representations from teacher and student models by module path, so models need not be reimplemented. It also trains models without a teacher by omitting teacher entries, and ships example scripts for image classification, detection, segmentation and GLUE/NLP tasks.

- **+** Experiments defined in one YAML file; custom modules need no edits to the package
- **+** Forward hooks extract intermediate features by module path without changing forward
- **+** Sample configs for many published methods (KD, FitNet, AT, RKD, PKT and others)
- **+** Imports teacher models from PyTorch Hub, e.g. timm; PyTorch Ecosystem member since Dec 2023
- **−** Deeply nested YAML with import_call tags is verbose and takes time to learn
- **−** Examples centre on vision and encoder NLP; LLM coverage is one causal LM/Alpaca example
- **−** Training library only; no serving, UI or deployment tooling
- **−** Requires Python 3.9+ and PyTorch; installing from source is marked not recommended

<sub>GPU optional · Needs PyTorch, torchvision, Hugging Face Transformers, PyYAML · Models: torchvision models, PyTorch Hub models, timm, Hugging Face Transformers · [Repo](https://github.com/yoshitomo-matsubara/torchdistill) · [▶️ Demo ↗](https://colab.research.google.com/github/yoshitomo-matsubara/torchdistill/blob/main/demo/cifar_kd.ipynb) · [📖 Docs ↗](https://yoshitomo-matsubara.net/torchdistill/usage.html) · [🌐 Site ↗](https://yoshitomo-matsubara.net/torchdistill/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/torchdistill/)</sub>

<a name="deepspec"></a>
### #&#8288;73 [deepspec](https://github.com/deepseek-ai/deepspec) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (66) · Freshness: active (82) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · MIT · Jul 2026</sub>

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

<a name="easyr1"></a>
### #&#8288;74 [easyr1](https://github.com/hiyouga/easyr1) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (53) · Freshness: recent (79) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="torchtune"></a>
### #&#8288;75 [torchtune](https://github.com/meta-pytorch/torchtune) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (58) · Freshness: recent (70) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · BSD-3-Clause · Nov 2026</sub>

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

<a name="xturing"></a>
### #&#8288;76 [xturing](https://github.com/stochasticai/xturing) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (27) · Freshness: recent (70) · Maintenance: patchy (47) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · Apache-2.0 · Sep 2026</sub>

**Python library for LoRA and INT8/INT4 fine-tuning of open LLMs.**

xTuring is a Python library that fine-tunes open-weight LLMs such as LLaMA 2, Mistral-7B, GPT-OSS, Qwen3 0.6B, GPT-J and Mamba on your own instruction data. LoRA and INT8/INT4 variants are selected by model key. It also provides DeepSpeed with CPU offloading, perplexity evaluation, and a CLI and Gradio playground for chatting with the result.

- **+** Model variants chosen by key: base, _lora, _int8, _lora_int8, plus INT4 via GenericLoraKbitModel
- **+** Published LLaMA-7B numbers: LoRA + DeepSpeed takes about 20 min/epoch on 4xA100 40GB
- **+** Built-in perplexity evaluation, batching and self-instruct dataset generation
- **+** CLI chat and Gradio UI playground for trying fine-tuned models locally
- **−** Last release was 2023-09-07; recent changes are only on the main branch
- **−** Pinned away from transformers 5.x because INT8/INT4 loading kwargs were removed
- **−** Perplexity is the only built-in evaluation metric
- **−** Qwen3-Omni support is unreleased; INT3 and lower precision are still unchecked on the roadmap

<sub>GPU optional · Needs PyTorch, transformers>=4.36.0, DeepSpeed, Intel Extension for Transformers (CPU inference) · Models: LLaMA, LLaMA 2, Mistral-7B, GPT-OSS 20B/120B, Qwen3 0.6B · [Repo](https://github.com/stochasticai/xturing) · [📖 Docs ↗](https://xturing.stochastic.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xturing/)</sub>

<a name="tensorflow-federated"></a>
### #&#8288;77 [tensorflow-federated](https://github.com/google-parfait/tensorflow-federated) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (23) · Freshness: recent (70) · Maintenance: fair (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Nov 2026</sub>

**Federated learning and analytics framework for decentralized data, built on TensorFlow.**

TensorFlow Federated is a Python framework for running machine learning and other computations on data that stays on client devices. It has two layers: tff.learning, with built-in federated training and evaluation for existing TensorFlow models, and the Federated Core API for writing new federated algorithms in a strongly-typed functional style. It ships with a single-machine simulation runtime for experiments.

- **+** Two layers: ready-made federated averaging and evaluation, plus a lower-level core for custom algorithms
- **+** Includes a single-machine simulation runtime for federated experiments
- **+** Building blocks also cover non-learning work such as aggregated analytics
- **+** Apache-2.0 licensed, with install docs, get-started guide and tutorials
- **−** Last tagged release is 2024-09-26, well behind recent commits
- **−** Tied to TensorFlow models; the README mentions no other framework
- **−** Bundled runtime is for simulation; production deployment interfaces are not described
- **−** Strongly-typed federated computation model adds a learning curve beyond plain TensorFlow

<sub>Needs TensorFlow · Models: TensorFlow models · [Repo](https://github.com/google-parfait/tensorflow-federated) · [📖 Docs ↗](https://github.com/google-parfait/tensorflow-federated/blob/main/docs/get_started.md) · [🌐 Site ↗](http://www.tensorflow.org/federated) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorflow-federated/)</sub>

<a name="paddlenlp"></a>
### #&#8288;78 [paddlenlp](https://github.com/paddlepaddle/paddlenlp) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (79) · Freshness: slowing (46) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · May 2026</sub>

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

<a name="axlearn"></a>
### #&#8288;79 [axlearn](https://github.com/apple/axlearn) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (22) · Freshness: active (82) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · Apache-2.0 · Jul 2026</sub>

**JAX-based library for training large-scale deep learning models.**

AXLearn is a Python library on top of JAX and XLA for building and training large deep learning models. Its object-oriented configuration system composes models from reusable building blocks and integrates with Flax and Hugging Face transformers. It uses GSPMD for a global-computation model and includes tools to deploy and manage jobs on public clouds.

- **+** Built on GSPMD; README claims training up to hundreds of billions of parameters
- **+** Composable config system for assembling models from reusable building blocks
- **+** Integrates with Flax and Hugging Face transformers
- **+** Includes baseline configs for NLP, vision and speech models
- **−** README warns the API is under active development and subject to change
- **−** No tagged release; PyPI process is only linked from RELEASE.md
- **−** Requires JAX/XLA familiarity; not a PyTorch-based toolchain
- **−** README gives no hardware requirements or concrete model list

<sub>Docker · Needs JAX, XLA, Flax, Hugging Face transformers · Models: NLP models, vision models, speech recognition models · [Repo](https://github.com/apple/axlearn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/axlearn/)</sub>

<a name="dlrover"></a>
### #&#8288;80 [dlrover](https://github.com/intelligent-machine-learning/dlrover) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (7) · Freshness: active (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · custom license · Nov 2026</sub>

**Fault-tolerant, auto-scaling distributed training on Kubernetes or Ray.**

DLRover manages distributed deep learning training jobs on Kubernetes or Ray. It diagnoses failures, restarts processes or nodes, rescales resources at runtime, and uses dynamic data sharding so failed or slow workers do not stall a job. For PyTorch it provides a torchrun-compatible dlrover-run launcher and Flash Checkpoint, which saves to host memory and persists asynchronously.

- **+** Reports GLM-65B goodput rising from 69% to 95% on thousands of GPUs
- **+** Flash Checkpoint reloads from host memory; APIs for DDP, FSDP, DeepSpeed, Megatron-LM
- **+** dlrover-run replaces torchrun, adding elastic scheduling and node health checks
- **+** Dynamic data sharding reassigns data from failed workers and mitigates stragglers
- **−** Aimed at cluster operators; needs a Kubernetes or Ray environment to be useful
- **−** License is reported as NOASSERTION, so terms need checking in the repo
- **−** Megatron-LM support is tied to a specific pinned commit
- **−** TensorFlow path centers on tf.estimator and parameter-server jobs

<sub>GPU optional · Needs Kubernetes, Ray · Models: PyTorch, TensorFlow, DDP, FSDP, DeepSpeed · [Repo](https://github.com/intelligent-machine-learning/dlrover) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dlrover/)</sub>

<a name="opacus"></a>
### #&#8288;81 [opacus](https://github.com/meta-pytorch/opacus) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (13) · Freshness: active (98) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Sep 2026</sub>

**PyTorch library for training models with DP-SGD differential privacy.**

Opacus trains PyTorch models with differential privacy. You create a PrivacyEngine and call make_private() on the model, optimizer and data loader, setting noise_multiplier and max_grad_norm, and it tracks the privacy budget spent during training. It also includes Fast Gradient Clipping and Ghost Clipping to cut DP-SGD memory use.

- **+** Minimal code change: wrap model, optimizer and data loader with PrivacyEngine.make_private()
- **+** Tracks the privacy budget spent online during training
- **+** Fast Gradient Clipping and Ghost Clipping reduce DP-SGD memory requirements
- **+** Tutorials cover BERT, image and LSTM classifiers, and LoRA with peft
- **−** PyTorch only; no support for other frameworks
- **−** Module Validator and Fixer imply some layers need changes for DP training
- **−** Privacy guarantees depend on noise and clipping values the user chooses
- **−** Training-time library only; no serving or inference features

<sub>Needs PyTorch · Models: PyTorch models · [Repo](https://github.com/meta-pytorch/opacus) · [📖 Docs ↗](https://opacus.ai/docs/faq) · [🌐 Site ↗](https://opacus.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opacus/)</sub>

<a name="vlm-r1"></a>
### #&#8288;82 [vlm-r1](https://github.com/om-ai-lab/vlm-r1) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: popular (61) · Freshness: recent (57) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Jul 2026</sub>

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

<a name="stable-audio-tools"></a>
### #&#8288;83 [stable-audio-tools](https://github.com/stability-ai/stable-audio-tools) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (44) · Freshness: recent (66) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · MIT · May 2026</sub>

**Training and inference code for diffusion-based audio generation models.**

PyTorch Lightning codebase from Stability AI for training, fine-tuning and running audio generation models, configured through JSON model and dataset files. It supports autoencoder, unconditional and conditional diffusion, inpainting, diffusion autoencoder and LM model types. A basic Gradio interface can load pretrained checkpoints such as stable-audio-open-1.0 from Hugging Face.

- **+** Training, fine-tuning and inference in one repo, driven by JSON configs
- **+** Multi-GPU and multi-node training via PyTorch Lightning, with DeepSpeed ZeRO Stage 2 option
- **+** Datasets from local audio directories or WebDataset on Amazon S3
- **+** Unwrap script strips training state to produce smaller inference checkpoints
- **−** Training logs to Weights & Biases, which needs an account and login
- **−** Gradio UI is described as basic, meant for testing models
- **−** Stable Audio Open weights require accepting terms on Hugging Face
- **−** Needs PyTorch 2.5+; Flash Attention must be installed separately

<sub>Needs PyTorch 2.5+, PyTorch Lightning, Weights & Biases (training), Gradio (UI), Flash Attention (recommended), uv · Models: stabilityai/stable-audio-open-1.0, autoencoder, diffusion_uncond, diffusion_cond, diffusion_cond_inpaint · [Repo](https://github.com/stability-ai/stable-audio-tools) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/stable-audio-tools/)</sub>

<a name="ml-hypersim"></a>
### #&#8288;84 [ml-hypersim](https://github.com/apple-aiml-research/ml-hypersim) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · custom license · Sep 2026</sub>

**Synthetic indoor-scene dataset with per-pixel labels, plus a V-Ray rendering toolkit.**

Hypersim is a photorealistic synthetic dataset of 77,400 images across 461 indoor scenes (74,619 in the public release), with depth, normals, semantic instance labels, 3D bounding boxes and camera poses. Images are split into diffuse reflectance, diffuse illumination and a non-diffuse residual. The repo also includes the Hypersim Toolkit, Python tools for generating similar datasets from V-Ray scenes.

- **+** Per-pixel depth, normals, NYU40 semantics, instances and 9-DOF boxes for every image
- **+** Lossless HDR HDF5 images with color = reflectance * illumination + residual
- **+** Standard scene-level train/val/test split (v1) included as CSV
- **+** Toolkit can generate new labeled datasets from V-Ray scenes
- **−** Full dataset is roughly 1.9TB across a few hundred ZIP files
- **−** Ground truth meshes require purchasing scene assets from TurboSquid
- **−** Toolkit depends on V-Ray, which is under Chaos Group's own terms
- **−** Some asset reuse across scenes leaks objects between train and test splits

<sub>Needs V-Ray Standalone, V-Ray AppSDK, curl, unzip, Python · [Repo](https://github.com/apple-aiml-research/ml-hypersim) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ml-hypersim/)</sub>

<a name="katib"></a>
### #&#8288;85 [katib](https://github.com/kubeflow/katib) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (7) · Freshness: active (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · Apache-2.0 · Nov 2026</sub>

**Kubernetes-native hyperparameter tuning and architecture search, now deprecated.**

Katib runs hyperparameter tuning, early stopping and neural architecture search as Kubernetes custom resources. Trials can run on any Kubernetes custom resource, with built-in support for Kubeflow Training Operator, Argo Workflows and Tekton Pipelines, and a Python SDK is available. The README marks the project as deprecated in favor of the OptimizationJob API in Kubeflow Trainer, which is in alpha.

- **+** Algorithms include Random, Grid, Bayesian, TPE, CMA-ES, HyperBand, PBT, ENAS and DARTS
- **+** Framework-agnostic: tunes code in any language; native TensorFlow, PyTorch and XGBoost support
- **+** Trials run as any Kubernetes custom resource, including Argo Workflows and Tekton
- **+** Python SDK (kubeflow-katib) for creating tuning experiments from code
- **−** Deprecated; README directs users to OptimizationJob in Kubeflow Trainer
- **−** Requires a Kubernetes cluster; no standalone local mode described
- **−** Replacement is still behind an alpha feature gate, so migration carries risk
- **−** Needs a separate database and metrics collector sidecar, which OptimizationJob removes

<sub>GPU optional · Docker · Needs Kubernetes, Kubeflow Training Operator (optional), Argo Workflows (optional), Tekton Pipelines (optional) · Models: TensorFlow, PyTorch, XGBoost · [Repo](https://github.com/kubeflow/katib) · [📖 Docs ↗](https://www.kubeflow.org/docs/components/katib/getting-started/) · [🌐 Site ↗](https://www.kubeflow.org/docs/components/katib/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/katib/)</sub>

<a name="openclaw-rl"></a>
### #&#8288;86 [openclaw-rl](https://github.com/gen-verse/openclaw-rl) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: popular (57) · Freshness: recent (65) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · May 2026</sub>

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

<a name="nanotron"></a>
### #&#8288;87 [nanotron](https://github.com/huggingface/nanotron) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (30) · Freshness: recent (70) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Oct 2026</sub>

**Library for pretraining transformer models with 3D parallelism.**

Nanotron is a Python library from Hugging Face for pretraining transformer models on custom datasets, launched with torchrun from YAML configs. It implements data, tensor and pipeline parallelism, expert parallelism for MoEs, and a ZeRO-1 optimizer, with examples for Llama, Mamba, MoE and µTransfer. Benchmark data and a scaling guide (Ultrascale Playbook) are published alongside.

- **+** 3D parallelism (DP+TP+PP) plus expert parallelism for MoE models
- **+** Explicit TP and PP APIs make multi-GPU debugging easier
- **+** Examples for Mamba, MoE, DoReMi, µTransfer, custom dataloaders and S3 checkpoint upload
- **+** Published benchmark configs and logs with an Ultrascale Playbook guide
- **−** ZeRO-3/FSDP, FP8 training, torch.compile and ring attention are only on the roadmap
- **−** Last tagged release is 2024-03-04; README installs from source
- **−** Install needs CUDA PyTorch, flash-attn and Triton; quick start assumes 8 x H100
- **−** Pretraining-focused; README describes no fine-tuning workflow

<sub>GPU required · Needs PyTorch, flash-attn, Triton, datatrove, Weights & Biases, Hugging Face Hub, Git LFS · Models: Llama, Mamba, Mixture-of-Experts · [Repo](https://github.com/huggingface/nanotron) · [📖 Docs ↗](https://huggingface.co/spaces/nanotron/ultrascale-playbook) · [🌐 Site ↗](https://huggingface.co/nanotron) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nanotron/)</sub>

<a name="qwen-vl-series-finetune"></a>
### #&#8288;88 [qwen-vl-series-finetune](https://github.com/2u1/qwen-vl-series-finetune) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Sep 2026</sub>

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

<a name="autoresearch"></a>
### #&#8288;89 [karpathy/autoresearch](https://github.com/karpathy/autoresearch) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: widely used (99) · Freshness: slowing (44) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 101k · no license · Mar 2026</sub>

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

<a name="autodistill"></a>
### #&#8288;90 [autodistill](https://github.com/autodistill/autodistill) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (29) · Freshness: recent (70) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · Apache-2.0 · Sep 2026</sub>

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

<a name="training"></a>
### #&#8288;91 [training](https://github.com/mlcommons/training) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (9) · Freshness: recent (70) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Oct 2026</sub>

**MLPerf Training reference implementations for LLM, image and recommendation benchmarks.**

Reference implementations of the MLPerf Training benchmarks. Each has model code, dataset download instructions, a Dockerfile and a script that trains until a target quality is reached and prints timing. The v6.1 suite covers flux.1, llama3.1 8B, llama2 70B LoRA, gpt_oss_20b, deepseekv3, qwen35 397B GRPO and a DLRM/HSTU recommender.

- **+** Covers LLM pretraining, LoRA fine-tuning, MoE, text-to-image, RL post-training and recommendation
- **+** Each benchmark ships a Dockerfile, dataset instructions and a time-to-target-quality run script
- **+** Updated each MLPerf round; v6.1 submission deadline listed as Oct 16, 2026
- **+** Reference frameworks vary per benchmark: torchtitan, NeMo, Primus, NeMo-RL, PyTorch
- **−** README calls implementations alpha or beta quality and not optimized
- **−** Not intended for real performance measurement of frameworks or hardware
- **−** Setup differs per benchmark; each subdirectory has its own README
- **−** No release since 2024-04-05; benchmarks are run from the master branch

<sub>GPU required · Needs Docker, CUDA, mlcommons-storage dataset downloads · Models: flux.1, llama3.1 8B, llama2 70B LoRA, gpt_oss_20b, deepseekv3 · [Repo](https://github.com/mlcommons/training) · [📖 Docs ↗](https://arxiv.org/abs/1910.01500) · [🌐 Site ↗](https://training.mlcommons-storage.org/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/training/)</sub>

<a name="privacy"></a>
### #&#8288;92 [privacy](https://github.com/tensorflow/privacy) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (15) · Freshness: recent (70) · Maintenance: weak (21) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Nov 2026</sub>

**Differentially private optimizers and privacy analysis tools for TensorFlow models.**

Python library that wraps TensorFlow optimizers (SGD, Adam and others) into differentially private versions for training models. It includes tutorials and analysis tools for computing the privacy guarantees of a training run. Since version 0.9.0, empirical privacy testing ships as a separate PyPI package, tensorflow-empirical-privacy.

- **+** Wraps existing TensorFlow optimizers such as SGD and Adam into DP counterparts
- **+** Includes tools to compute privacy guarantees, plus a tutorial walkthrough
- **+** Per-example gradient clipping for Keras Dense/Embedding models, with little overhead
- **+** Installs with pip install tensorflow-privacy
- **−** Tied to TensorFlow; Keras and Estimator support needs TensorFlow 2.4 or later
- **−** Fast per-example clipping covers only Dense and Embedding layers
- **−** Last release is 2023-10-10, long before the latest commit
- **−** Tutorials are not part of the API and can change without warning

<sub>GPU optional · Needs TensorFlow · Models: TensorFlow, Keras, tf.estimator · [Repo](https://github.com/tensorflow/privacy) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/privacy/)</sub>

<a name="snorkel"></a>
### #&#8288;93 [snorkel](https://github.com/snorkel-team/snorkel) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: popular (60) · Freshness: slowing (35) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Apr 2026</sub>

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

<a name="flagai"></a>
### #&#8288;94 [flagai](https://github.com/flagai-open/flagai) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: known (43) · Freshness: recent (59) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · Apache-2.0 · Jul 2026</sub>

**PyTorch toolkit for training and fine-tuning Chinese and English language models.**

FlagAI is a Python toolkit from BAAI that loads pre-trained models through an AutoLoader and Predictor API, then trains or fine-tunes them with PyTorch, DeepSpeed, Megatron-LM or BMTrain. It covers over 30 models, including Aquila, AltCLIP, AltDiffusion, GLM, OPT, BERT, GPT2 and T5, with a focus on Chinese text tasks such as NER, title generation and semantic matching.

- **+** Switches between PyTorch, DeepSpeed, Megatron-LM and BMTrain parallelism in under ten lines of code
- **+** AutoLoader and Predictor give one API for NER, seq2seq, title generation and semantic matching
- **+** Model table lists train, finetune and inference support per model, with example directories
- **+** Includes BMInf for low-resource inference and Flash Attention for BERT and ViT training
- **−** Model zoo is mostly 2022-era models (GLM, OPT, T5, BERT); no recent LLM families listed
- **−** README news ends at v1.7.0 (June 2023); last GitHub release is 2024-11-07
- **−** Mixed licenses: Megatron-LM, GLM (MIT) and AltDiffusion (Open RAIL-M) differ from Apache-2.0
- **−** Some example links in the toolkit table are malformed (http:/// URLs)

<sub>GPU optional · Docker · Needs Python >= 3.8, PyTorch >= 1.8.0, DeepSpeed >= 0.7.7 (optional), BMTrain >= 0.2.2 (optional), BMInf (optional), NVIDIA apex (optional), flash-attn >= 1.0.2 (optional), CUDA and NCCL (optional, for GPU) · Models: Aquila, AltCLIP, AltDiffusion, GLM, EVA-CLIP · [Repo](https://github.com/flagai-open/flagai) · [🌐 Site ↗](https://flagopen.baai.ac.cn/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flagai/)</sub>

<a name="plexe"></a>
### #&#8288;95 [plexe](https://github.com/plexe-ai/plexe) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (27) · Freshness: slowing (48) · Maintenance: weak (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · Apache-2.0 · Mar 2026</sub>

**Agentic AutoML that builds tabular ML models from a plain-language intent.**

Plexe takes a tabular dataset (Parquet, CSV, ORC or Avro) and a natural-language intent, then runs 14 LLM agents across a 6-phase workflow to analyze the data, pick a metric, search model candidates and evaluate them. Output is a self-contained model package with pickled artifacts, inference code, schemas and metrics that does not depend on plexe. LLM calls go through LiteLLM.

- **+** Output model package has no plexe dependency and ships schemas, metrics and inference code
- **+** Per-agent LLM routing through LiteLLM, configurable in config.yaml
- **+** Supports XGBoost, CatBoost, LightGBM, Keras and PyTorch, with optional PySpark
- **+** Streamlit dashboard for search trees and evaluation reports
- **−** Actively tested only with openai/* and anthropic/* models
- **−** Needs LLM API keys; local providers like Ollama are not actively tested
- **−** Python limited to >= 3.10 and < 3.13
- **−** Documented for tabular data only

<sub>Docker · Needs OpenAI or Anthropic API key (via LiteLLM), PySpark and Java (bundled in Docker image) · Models: XGBoost, CatBoost, LightGBM, Keras, PyTorch · [Repo](https://github.com/plexe-ai/plexe) · [▶️ Demo ↗](https://www.youtube.com/watch?v=bUwCSglhcXY) · [📖 Docs ↗](https://docs.plexe.ai) · [🌐 Site ↗](https://plexe.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/plexe/)</sub>

<a name="adapters"></a>
### #&#8288;96 [adapters](https://github.com/adapter-hub/adapters) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: niche (30) · Freshness: recent (66) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · Apache-2.0 · Apr 2026</sub>

**Parameter-efficient fine-tuning add-on for HuggingFace Transformers models.**

Adapters is a Python library that adds 10+ parameter-efficient fine-tuning methods (LoRA, QLoRA, DoRA, bottleneck adapters, prefix tuning, ReFT and others) to 20+ Transformer models from HuggingFace Transformers. It also supports composing several adapters in one model and merging them via task arithmetic. It replaces the earlier adapter-transformers package, and adapters trained with that package still load.

- **+** Covers many methods (LoRA, DoRA, VeRA, IA3, ReFT, Compacter) behind one interface
- **+** Composition blocks and adapter merging allow multi-adapter setups in a single model
- **+** Adds adapters to existing Transformers models with adapters.init(model)
- **+** Supports quantized training such as QLoRA, with a Llama notebook
- **−** PyTorch only; no other tensor frameworks are supported
- **−** Limited to models on its supported list, not arbitrary architectures
- **−** Library for researchers; no UI, server or hosted training workflow
- **−** Tied to HuggingFace Transformers, so version compatibility must be tracked

<sub>Needs PyTorch 2.0+, HuggingFace Transformers, Python 3.9+ · Models: HuggingFace Transformers (20+ architectures, PyTorch), Q-LoRA quantized training · [Repo](https://github.com/adapter-hub/adapters) · [📖 Docs ↗](https://docs.adapterhub.ml) · [🌐 Site ↗](https://adapterhub.ml) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/adapters/)</sub>

<a name="roboflow-maestro"></a>
### #&#8288;97 [roboflow/maestro](https://github.com/roboflow/maestro) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (28) · Freshness: recent (62) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · Apache-2.0 · Jul 2026</sub>

**Fine-tuning CLI and Python SDK for vision-language models.**

maestro wraps configuration, data loading and the training loop for fine-tuning vision-language models. It ships recipes for Florence-2, PaliGemma 2 and Qwen2.5-VL, with LoRA, QLoRA and graph freezing to limit hardware needs. Training runs through one CLI command or a Python train() function, using a JSONL dataset format.

- **+** Ready recipes for Florence-2, PaliGemma 2 and Qwen2.5-VL
- **+** LoRA and QLoRA support keep hardware requirements down
- **+** Same options via CLI and Python train() function
- **+** Colab notebooks for JSON extraction and object detection
- **−** Only three model families supported
- **−** Florence-2 and Qwen2.5-VL 7B detection recipes are marked experimental
- **−** Per-model dependencies can clash, so separate Python environments are advised
- **−** Last release 1.0.0 dates from February 2025

<sub>Models: Florence-2, PaliGemma 2, Qwen2.5-VL · [Repo](https://github.com/roboflow/maestro) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/roboflow-maestro/)</sub>

<a name="ttt-video-dit"></a>
### #&#8288;98 [ttt-video-dit](https://github.com/test-time-training/ttt-video-dit) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (23) · Freshness: slowing (33) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · MIT · Feb 2026</sub>

**Fine-tuning code for CogVideoX-5B with TTT layers for 63-second videos.**

Training and inference code that adapts the CogVideoX 5B text-to-video diffusion transformer with Test-Time Training layers. The TTT layers handle global context, while the original attention layers handle each 3-second segment. Training runs in stages at 3, 9, 18, 30 and 63 seconds for style transfer and context extension.

- **+** Staged context extension from 3 s to 63 s video, with training and sampling docs
- **+** Reuses pretrained CogVideoX-5B attention for local segments instead of training from scratch
- **+** Architecture described in a CVPR 2025 paper; MIT license
- **−** TTT-MLP kernel needs CUDA toolkit 12.3+ and gcc11+ to build
- **−** TTT-MLP training supported only on H100 GPUs
- **−** Final demo model weights not provided; only base pretrained weights are referenced
- **−** No Docker image; setup needs a manual kernel build and separate CogVideoX downloads

<sub>GPU required · Needs CUDA toolkit 12.3+, gcc 11+, conda, ttt-tk submodule, CogVideoX-5B weights, VAE and T5 encoder · Models: CogVideoX-5B · [Repo](https://github.com/test-time-training/ttt-video-dit) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ttt-video-dit/)</sub>

<a name="search-r1"></a>
### #&#8288;99 [search-r1](https://github.com/petergriffinjin/search-r1) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: popular (55) · Freshness: quiet (0) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Nov 2025</sub>

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

<a name="augmentoolkit"></a>
### #&#8288;100 [augmentoolkit](https://github.com/e-p-armstrong/augmentoolkit) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (12) · Freshness: recent (55) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Jun 2026</sub>

**Generates training datasets from your documents and fine-tunes domain-expert LLMs.**

Augmentoolkit turns uploaded documents into factual SFT and continued-pretraining datasets, then can start a fine-tune on them. It includes pipelines for factual QA, RAG data, GRPO with an LLM as reward function, classifier bootstrapping and roleplay data (RPToolkit). It runs through a local interface or a CLI, and datagen can use a local model or an open-source LLM API.

- **+** Several composable pipelines: factual, RAG data, correction data, classifier bootstrapping, GRPO, roleplay
- **+** Datagen can run offline via a local-model script, or through an open-source LLM API
- **+** Interrupted runs resume automatically; new pipelines are plain Python functions
- **+** MIT license with annotated configs and video walkthroughs
- **−** GRPO pipeline is marked experimental and in beta
- **−** Needs a Redis or Valkey server, which the start scripts may install or build
- **−** Small datasets give too few optimizer steps and need config tuning to train well
- **−** Windows interface support is via WSL; no Docker setup is provided

<sub>GPU optional · Needs Python 3.11, Valkey or Redis, Axolotl · Models: Open-source LLM APIs (e.g. Deepinfra), Deepseek, Llama, Custom 7B datagen model · [Repo](https://github.com/e-p-armstrong/augmentoolkit) · [📖 Docs ↗](https://github.com/e-p-armstrong/augmentoolkit/blob/master/docs/quickstart.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/augmentoolkit/)</sub>

<a name="hivemind"></a>
### #&#8288;101 [learning-at-home/hivemind](https://github.com/learning-at-home/hivemind) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (26) · Freshness: quiet (28) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · MIT · Jan 2026</sub>

**PyTorch library for training one model across volunteer machines over the Internet.**

Hivemind is a PyTorch library for decentralized training across unreliable peers on the Internet. It connects workers through a Distributed Hash Table with no master node, and provides decentralized parameter averaging and a Decentralized Mixture-of-Experts layer. Petals and a PyTorch Lightning integration build on it.

- **+** No master node: peers find each other through a Distributed Hash Table
- **+** Forward and backward passes tolerate slow or unresponsive nodes
- **+** Used by Petals, sahajBERT and CALM; PyTorch Lightning integration exists
- **+** Optional blockwise 8-bit compression for transfers via bitsandbytes
- **−** Linux is the tested OS; macOS is partial, Windows is experimental via WSL
- **−** Tied to PyTorch 1.9.0+ and Python 3.8+
- **−** Needs several networked peers; not a drop-in single-machine trainer
- **−** README describes the project as at an active development stage

<sub>GPU optional · Docker · Needs Python 3.8+, PyTorch 1.9.0+, go-libp2p-daemon (precompiled binary), bitsandbytes (optional) · Models: PyTorch models · [Repo](https://github.com/learning-at-home/hivemind) · [📖 Docs ↗](https://learning-at-home.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hivemind/)</sub>

<a name="distilabel"></a>
### #&#8288;102 [distilabel](https://github.com/argilla-io/distilabel) <sub>score [13](../README.md#-how-we-rank "Score 13/100. Adoption: known (39) · Freshness: quiet (5) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · Apache-2.0 · Dec 2025</sub>

**Python framework for building synthetic data and AI feedback pipelines.**

Distilabel is a Python library for building pipelines that generate synthetic datasets and judge them with LLM feedback. It wraps many LLM providers and local engines behind one API, and results can be pushed to the Hugging Face Hub or exported to Argilla. The original authors have moved on, and community collaborators now maintain it, with recent fixes on the develop branch.

- **+** One API across OpenAI, Anthropic, vLLM, Ollama, llama.cpp, Transformers, MLX and others
- **+** Optional Ray extra distributes pipelines; clustering and minhash dedup extras included
- **+** Structured generation through outlines and instructor extras
- **+** Pushes datasets to the Hugging Face Hub or exports to Argilla
- **−** Original authors have moved on; maintained by community collaborators
- **−** Last release was 2025-01-28; latest fixes only on the develop branch
- **−** Library only, with no UI; pipelines are written in Python
- **−** Each provider integration is an optional extra installed separately

<sub>GPU optional · Needs Python 3.9+ · Models: OpenAI, Anthropic, Cohere, Groq, Mistral AI · [Repo](https://github.com/argilla-io/distilabel) · [📖 Docs ↗](http://distilabel.argilla.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/distilabel/)</sub>

<a name="modernbert"></a>
### #&#8288;103 [modernbert](https://github.com/answerdotai/modernbert) <sub>score [13](../README.md#-how-we-rank "Score 13/100. Adoption: niche (10) · Freshness: slowing (35) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Mar 2026</sub>

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

<a name="agentflow"></a>
### #&#8288;104 [agentflow](https://github.com/lupantech/agentflow) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: niche (17) · Freshness: quiet (23) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · MIT · Jan 2026</sub>

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

<a name="alphagen"></a>
### #&#8288;105 [alphagen](https://github.com/ict-find-lab/alphagen) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: niche (2) · Freshness: recent (69) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 1.3k · no license · Jun 2026</sub>

**Reinforcement-learning miner for formulaic stock alpha factors, from a KDD 2023 paper.**

AlphaGen trains a maskable PPO agent with an LSTM feature extractor to generate formulaic alphas and combine them into a linearly weighted pool, scored by IC and Rank IC against a target such as 20-day return. It includes gplearn and DSO baselines, LLM-driven iterative alpha generation scripts, and experimental Qlib-based backtests. Data comes from Qlib metadata plus baostock stock data, or a custom AlphaCalculator adapter.

- **+** Reproduces a peer-reviewed KDD 2023 method, with a follow-up LLM-assisted variant (HARLA)
- **+** Pluggable AlphaCalculator interface lets you use your own alpha evaluation pipeline
- **+** Checkpoints are stable-baselines3 compatible; alpha pools saved as readable JSON
- **+** Ships modified gplearn and DSO baselines for comparison
- **−** Research code: run via python -m scripts.NAME, with no packaged install or release
- **−** Built-in pipeline needs Qlib metadata setup plus baostock data, which is China A-share focused
- **−** No license file detected, so reuse terms are unclear
- **−** Trading and backtest modules are labelled experimental

<sub>Needs Qlib, baostock, stable-baselines3, PyTorch, TensorBoard, gplearn, DSO · Models: MaskablePPO with LSTM feature extractor, LLM clients (providers not stated) · [Repo](https://github.com/ict-find-lab/alphagen) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/alphagen/)</sub>

<a name="captcha-trainer"></a>
### #&#8288;106 [captcha_trainer](https://github.com/kerlomz/captcha_trainer) <sub>score [11](../README.md#-how-we-rank "Score 11/100. Adoption: known (36) · Freshness: quiet (0) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · Apache-2.0 · Nov 2025</sub>

**Trains CNN+RNN+CTC image captcha recognition models with a GUI config tool.**

TensorFlow-based trainer for image captcha recognition and other fixed-format image classification. A GUI (app.py) or the CLI scripts make_dataset.py and trains.py generate a model.yaml, pack labeled samples into TFRecords, train, and compile a .pb model. The output is meant for the companion captcha_platform serving project.

- **+** Projects are configured through YAML or a GUI with no code changes, one workspace per task
- **+** Offers CNN5, ResNet50 or DenseNet with GRU/LSTM variants or none, using CTC or CrossEntropy
- **+** Built-in augmentation: blur, rotation, perspective warp, salt-and-pepper noise, binarization
- **+** Prebuilt Windows GPU release skips CUDA setup; README reports 1-15 ms CPU inference for CNN5
- **−** Only image classification is supported; the Text field type is not implemented
- **−** Built on old TensorFlow (1.14 stated, 2.8 nightly also mentioned), so setup guidance conflicts
- **−** Labels come from filenames, XML or LMDB, and samples must be packed into TFRecords first
- **−** README badge says MIT while the repository license is Apache-2.0; docs are mostly Chinese

<sub>GPU optional · Needs TensorFlow, Python 3.8, CUDA, cuDNN, captcha_platform (for deployment) · Models: CNN5, ResNet50, DenseNet, LSTM, BiLSTM · [Repo](https://github.com/kerlomz/captcha_trainer) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/captcha-trainer/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
