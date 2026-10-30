# 🧠 Model serving reviews · Best of Open-Source AI

Inference engines and model servers that expose local models over an API. Back to the [leaderboard](../README.md#-model-serving).

<sub>🌐 Also on the web: [Model serving on archestack.com](https://archestack.com/best-of-ai/model-serving/), each project on its own page.</sub>

<a name="llama-cpp"></a>
### 🥇 [llama.cpp](https://github.com/ggml-org/llama.cpp) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 133k · MIT · Oct 2026</sub>

**C/C++ inference engine serving GGUF models over an OpenAI-compatible API.**

llama.cpp is a C/C++ inference engine for LLMs and VLMs with no dependencies, built on ggml. llama serve starts an OpenAI-compatible API server with a built-in web UI, pulling GGUF models straight from Hugging Face, with 1.5 to 8-bit quantization and CPU+GPU hybrid offload for models larger than VRAM. Backends cover CUDA, HIP, Metal, Vulkan, SYCL, OpenCL, CANN, MUSA and WebGPU.

- **+** Plain C/C++ with no runtime dependencies; prebuilt binaries and Docker
- **+** Backends for NVIDIA, AMD, Apple Metal, Intel SYCL, Vulkan, Ascend, Moore Threads
- **+** Hybrid CPU+GPU offload runs models larger than available VRAM
- **+** Built-in web UI and OpenAI-compatible server via llama serve
- **−** GGUF model format only
- **−** README gives no port, auth or sizing guidance; see tools/server docs
- **−** Install script is curl piped to sh; otherwise build from source
- **−** OpenVINO backend still in progress

<sub>GPU optional · Docker · Models: GGUF models from Hugging Face (e.g. Qwen3.5-0.8B-GGUF) · [Repo](https://github.com/ggml-org/llama.cpp) · [🌐 Site ↗](https://llama.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llama-cpp/)</sub>

<a name="ollama"></a>
### 🥈 [Ollama](https://github.com/ollama/ollama) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 185k · MIT · Oct 2026</sub>

**Local model runner with CLI and REST API for open-weight LLMs.**

Ollama downloads and runs open models from its library (for example Gemma 4) through a CLI and a REST API on localhost:11434. It uses llama.cpp as its backend and ships official Python and JavaScript client libraries. The `ollama launch` command connects it to tools such as Claude Code, Codex, OpenCode and OpenClaw.

- **+** One-line installers for macOS, Windows and Linux, plus an official Docker image
- **+** REST API at /api/chat with official Python and JavaScript clients
- **+** Large community integration list: chat UIs, editors, RAG tools and SDKs in many languages
- **+** Modelfile and model import let you customize or bring your own weights
- **−** README gives no RAM, VRAM or GPU requirements per model
- **−** Backend is llama.cpp only, per the README's supported backends list
- **−** No built-in web chat UI or multi-user accounts mentioned; needs a third-party front-end
- **−** README mentions cloud models but does not detail how they work or what they cost

<sub>Docker · Needs llama.cpp · Models: Ollama model library, Gemma 4, Modelfile, model import · port 11434 · [Repo](https://github.com/ollama/ollama) · [📖 Docs ↗](https://docs.ollama.com) · [🌐 Site ↗](https://ollama.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ollama/)</sub>

<a name="localai"></a>
### 🥉 [LocalAI](https://github.com/mudler/localai) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Oct 2026</sub>

**Self-hosted inference server with OpenAI-compatible API and pluggable backends.**

LocalAI serves LLMs, vision, speech, image and video models behind OpenAI, Anthropic, ElevenLabs and Ollama-compatible APIs. Each backend (llama.cpp, vLLM, whisper.cpp, diffusers, MLX and others) is a separate OCI image pulled on demand. It also ships a web UI, API-key auth with quotas, built-in agents with MCP, and a distributed mode using PostgreSQL and NATS.

- **+** Covers text, vision, speech, image and video models behind one API
- **+** Runs on CPU, CUDA 12/13, ROCm, Intel oneAPI, Vulkan, Apple Silicon and Jetson
- **+** Backends install on demand, so only the engines a model needs are pulled
- **+** Includes API-key auth, user quotas and a distributed mode for horizontal scaling
- **−** Distributed mode requires PostgreSQL and NATS
- **−** macOS DMG is not signed by Apple and needs a manual xattr command
- **−** Wide scope (agents, fine-tuning, UI) makes the feature surface large to evaluate
- **−** vllm.cpp backend is described as alpha development builds

<sub>GPU optional · Docker + Compose · Needs PostgreSQL (distributed mode), NATS (distributed mode) · Models: GGUF, llama.cpp, vLLM, SGLang, transformers · port 8080 · [Repo](https://github.com/mudler/localai) · [📖 Docs ↗](https://localai.io/basics/getting_started/) · [🌐 Site ↗](https://localai.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/localai/)</sub>

<a name="vllm"></a>
### #&#8288;4 [vLLM](https://github.com/vllm-project/vllm) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 96k · Apache-2.0 · Oct 2026</sub>

**Inference engine for Hugging Face LLMs with PagedAttention and continuous batching.**

vLLM is a Python library and server for LLM inference. It manages attention KV memory with PagedAttention, batches requests continuously, and exposes an OpenAI-compatible API, plus the Anthropic Messages API and gRPC. It supports 200+ Hugging Face model architectures and runs on NVIDIA, AMD and Intel GPUs, several CPU types, and other accelerators through plugins.

- **+** Continuous batching, chunked prefill, prefix caching and PagedAttention for high-throughput serving
- **+** Wide quantization support: FP8, NVFP4, INT4/INT8, GPTQ/AWQ, GGUF and others
- **+** Tensor, pipeline, data, expert and context parallelism for multi-GPU inference
- **+** Runs on NVIDIA, AMD, Intel GPUs and x86/ARM/PowerPC CPUs, with plugins for TPU, Gaudi, Ascend
- **−** README gives no minimum RAM or VRAM figures
- **−** Several hardware targets depend on separate plugins rather than the core package
- **−** Large feature surface means many tuning options to learn
- **−** Server and library only, with no built-in chat UI

<sub>GPU optional · Docker · Needs Python, PyTorch · Models: Hugging Face models, Llama, Qwen, Gemma, Mixtral · [Repo](https://github.com/vllm-project/vllm) · [📖 Docs ↗](https://docs.vllm.ai) · [🌐 Site ↗](https://vllm.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vllm/)</sub>

<a name="colibri"></a>
### #&#8288;5 [colibri](https://github.com/justvugg/colibri) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 45k · Apache-2.0 · Oct 2026</sub>

**C inference engine that streams MoE experts from disk to run huge models.**

colibri is a pure-C inference engine for large mixture-of-experts models such as GLM-5.2 (744B), Kimi K3 and DeepSeek V4 Flash. It keeps the dense layers in RAM and reads routed experts from disk through a learned cache, with optional CUDA or Vulkan offload. It serves a browser dashboard plus OpenAI- and Anthropic-style endpoints on port 8000.

- **+** Runs models up to 2.8T parameters on CPU only, with disk streaming of experts
- **+** One-step setup script picks a model that fits RAM and disk, and resumes downloads
- **+** Exposes OpenAI and Anthropic base URLs, plus an MCP server for setup
- **+** README lists measured tok/s per model and machine, with the hardware named
- **−** Large models are slow: GLM-5.2 0.05-0.1 tok/s cold on a 25 GB laptop
- **−** Downloads are big: 23 GB for the smallest chat model, 1.56 TB for Kimi K3
- **−** Discrete GPU path not measured by the authors; only one user report
- **−** Supports a fixed list of model families; other architectures are not covered

<sub>RAM ≥ 8 GB · GPU optional · Docker + Compose · Needs Python 3, C compiler (build-essential or Xcode tools), libomp (macOS), CUDA toolkit or Vulkan driver (optional) · Models: GLM-5.2/5.3, GLM-5.3-Flash, Kimi K3, DeepSeek V4 Flash, MiMo-V2.6 · port 8000 · [Repo](https://github.com/justvugg/colibri) · [📖 Docs ↗](https://github.com/JustVugg/colibri/blob/main/docs/quickstart.md) · [🌐 Site ↗](https://justvugg.github.io/colibri) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/colibri/)</sub>

<a name="strata"></a>
### #&#8288;6 [strata](https://github.com/niko1221/strata) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Oct 2026</sub>

**Runs a 125B-parameter MoE model on one consumer GPU plus system RAM.**

Strata is a C++ inference engine, built on parts of llama.cpp/ggml, that runs Qwen3.8-Flash-Next on a PC with a 12 GB or larger NVIDIA or AMD card. It keeps the most-used experts in VRAM, holds all of them in RAM and uses the CPU for the rest. It serves a browser chat app plus OpenAI-, Anthropic- and Responses-style APIs on port 8080.

- **+** Serves OpenAI /v1, Anthropic /v1/messages and Responses /v1/responses on 127.0.0.1:8080
- **+** Reports 53-94 tokens/s decode on an RTX 5070 12 GB, depending on quantization
- **+** Installer picks a model size by RAM; interrupted downloads resume
- **+** Ships a BENCH script, an MCP server for setup, and multi-GPU support
- **−** Built around one model family (Qwen3.8-Flash-Next), not arbitrary GGUFs
- **−** Needs 32 GB or more RAM and about 80 GB disk; PC may freeze 1-3 minutes at load
- **−** Answers one request at a time by default; parallel mode slows each answer on 12 GB cards
- **−** Intel Arc, Mac, older GPUs and Strix Halo support is experimental and community-tested

<sub>RAM ≥ 32 GB · GPU required · Docker + Compose · Needs NVIDIA or AMD GPU driver, Qwen3.8-Flash-Next model download (about 70 GB) · Models: Qwen3.8-Flash-Next GGUF (Q2_0, IQ2_XS, IQ3_XXS, IQ3_S, Coder, Swift 1.5), Unsloth UD-IQ4_XS to Q8_0 · port 8080 · [Repo](https://github.com/niko1221/strata) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/strata/)</sub>

<a name="modular"></a>
### #&#8288;7 [modular](https://github.com/modular/modular) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

**Mojo language and MAX inference framework with an OpenAI-compatible server.**

Monorepo for the open-source parts of the Modular Platform: the Mojo compiler and standard library, the MAX accelerator kernel library, and MAX Python model pipelines. MAX includes an inference server that exposes an OpenAI-compatible endpoint. The repo code is Apache 2.0 with LLVM Exceptions, while MAX usage and distribution fall under the Modular Community License.

- **+** Serving layer exposes an OpenAI-compatible endpoint, per the README
- **+** Open kernels, Mojo stdlib and model architectures accept outside contributions
- **+** Includes Python-based model pipelines and code examples for MAX and Mojo
- **+** Active: last commit 2026-10-08, release 2026-09-17
- **−** Two licenses: repo is Apache 2.0 with LLVM exceptions, MAX uses Modular Community License
- **−** Mojo compiler is not open to contributions yet
- **−** README gives no hardware requirements or supported model list
- **−** Broad platform repo; serving is one part, so setup is spread across separate docs

<sub>Models: Hugging Face models via MAX pipelines · [Repo](https://github.com/modular/modular) · [📖 Docs ↗](https://max.modular.com/) · [🌐 Site ↗](https://www.modular.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/modular/)</sub>

<a name="sglang"></a>
### #&#8288;8 [SGLang](https://github.com/sgl-project/sglang) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · Apache-2.0 · Oct 2026</sub>

**Inference engine for LLM, vision-language and diffusion models on many hardware types.**

SGLang is an inference framework that serves large language, vision-language and diffusion models, aimed at agentic workloads, large-scale serving and RL rollouts. It includes SGLang Diffusion for image and video generation, and runs on NVIDIA, AMD, Google TPU, Intel, Apple Silicon, Huawei Ascend and Moore Threads hardware. A cookbook generates launch commands per model and hardware pair.

- **+** Supports NVIDIA, AMD, TPU, Intel, Apple Silicon, Ascend and Moore Threads hardware
- **+** Built-in diffusion engine for image and video generation in the same package
- **+** Integrates with RL training stacks such as verl and slime for rollouts
- **+** Cookbook gives ready-to-run launch commands per model and hardware
- **−** README gives no RAM or VRAM requirements; sizing depends on model and hardware
- **−** Several hardware integrations (Trainium, Cambricon, Qualcomm) are still in progress
- **−** TTS and ASR serving live in a separate project, SGLang Omni
- **−** Install uses --prerelease=allow, so dependencies may include prerelease packages

<sub>GPU optional · Docker + Compose · Models: LLMs, vision-language models, diffusion models · [Repo](https://github.com/sgl-project/sglang) · [📖 Docs ↗](https://docs.sglang.io/) · [🌐 Site ↗](https://www.sglang.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sglang/)</sub>

<a name="tensorrt-llm"></a>
### #&#8288;9 [tensorrt-llm](https://github.com/nvidia/tensorrt-llm) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (58) · Freshness: active (99) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · Oct 2026</sub>

**NVIDIA inference engine for LLMs and diffusion models with custom CUDA kernels.**

TensorRT LLM is NVIDIA's inference library for LLMs and visual generation (diffusion) models. It combines optimized kernels, a runtime and a customizable Python framework. The README's blog list covers speculative decoding, disaggregated serving, expert parallelism, sparse attention, KV cache work and DeepSeek on Blackwell. The excerpt gives no install steps or hardware minimums.

- **+** Kernel and parallelism work for Blackwell, NVL72 and NVLink-based expert parallelism
- **+** Documents speculative decoding, disaggregated serving, guided decoding and KV cache reuse
- **+** Day-0 support for models such as GPT-OSS and EXAONE 4.0 is documented
- **+** Extensible Python framework with architecture, performance and quick-start docs
- **−** Tied to NVIDIA GPUs, CUDA 13.4.1 and PyTorch 2.14.0
- **−** Current version shown is a release candidate (1.4.0rc1)
- **−** Detected license is NOASSERTION, while the README badge says Apache 2
- **−** README excerpt lacks install steps, memory requirements and API port

<sub>GPU required · Docker · Needs CUDA 13.4.1, PyTorch 2.14.0, Python 3.10 or 3.12 · Models: LLMs, DeepSeek, Llama, GPT-OSS, EXAONE · [Repo](https://github.com/nvidia/tensorrt-llm) · [📖 Docs ↗](https://nvidia.github.io/TensorRT-LLM/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorrt-llm/)</sub>

<a name="lmcache"></a>
### #&#8288;10 [lmcache](https://github.com/lmcache/lmcache) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (50) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Oct 2026</sub>

**KV cache offloading and reuse layer for LLM serving engines.**

LMCache runs as a standalone daemon that stores LLM KV cache outside the inference engine, in tiers spanning CPU RAM, local disk and remote backends. Cached KV can be reused across requests, sessions and engine instances, which cuts repeated prefill and time-to-first-token on long-context, multi-turn and RAG workloads. It also supports non-prefix reuse via CacheBlend and prefill-to-decode KV transfer over NVLink, RDMA or TCP.

- **+** Runs as a separate daemon, so KV cache survives inference engine crashes
- **+** Backends include CPU RAM, disk, Redis/Valkey, Mooncake, S3-compatible, NIXL and GDS
- **+** Non-prefix KV reuse at any prompt position through CacheBlend
- **+** Exposes KV-cache metrics such as request-level and token-level prefix hits
- **−** Not a standalone server; it needs a supported serving engine in front
- **−** README gives no hardware requirements or supported-engine version list
- **−** Multi-node and PD disaggregation setups need external transports and storage
- **−** No Docker or compose files detected in the repository

<sub>Docker · Needs Redis/Valkey (optional), Mooncake (optional), NIXL (optional), S3-compatible storage (optional) · Models: gpt-oss 20B/120B, multimodal models in vLLM V1 · [Repo](https://github.com/lmcache/lmcache) · [📖 Docs ↗](https://docs.lmcache.ai/) · [🌐 Site ↗](https://blog.lmcache.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmcache/)</sub>

<a name="airllm"></a>
### #&#8288;11 [airllm](https://github.com/lyogavin/airllm) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Oct 2026</sub>

**Python library that runs huge LLMs on small GPUs by streaming layers.**

AirLLM splits a Hugging Face model into per-layer shards on disk and keeps only one decoder layer on the GPU at a time, so VRAM need tracks layer size rather than model size. The README reports Llama 3.x 70B in about 4GB, DeepSeek-V3 671B in about 12GB, and LoRA training of Qwen3.8-Flash-Next 125B under 6GB. Usage is a single `AutoModel.from_pretrained` call with a transformers-style `generate`.

- **+** Runs 70B models in about 4GB VRAM without quantization, per the README
- **+** One AutoModel call covers Llama, Qwen, DeepSeek, Mistral, Gemma, Phi and others
- **+** Optional 4bit/8bit block-wise compression of loaded weights for up to 3x speedup
- **+** Streaming LoRA training for Qwen3.8-27B (~2GB) and Flash-Next 125B (under 6GB)
- **−** Layer-by-layer disk loading makes generation slow; no tokens/s figures given
- **−** Splitting needs large disk space, e.g. ~360GB for Qwen3.8-Flash-Next
- **−** macOS supports only Llama and Mistral architectures, on Apple silicon
- **−** No HTTP API or UI; a Python library only, with newer models needing specific transformers versions

<sub>GPU optional · Needs PyTorch, transformers, bitsandbytes (for compression), mlx (macOS), Hugging Face model downloads · Models: Llama 2/3/3.x/4, Qwen 1–3.8, DeepSeek V2/V3/R1, Mistral/Mixtral, Phi · [Repo](https://github.com/lyogavin/airllm) · [▶️ Demo ↗](https://colab.research.google.com/github/lyogavin/airllm/blob/main/air_llm/examples/run_all_types_of_models.ipynb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/airllm/)</sub>

<a name="omlx"></a>
### #&#8288;12 [omlx](https://github.com/jundot/omlx) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · Apache-2.0 · Oct 2026</sub>

**MLX-based LLM inference server for Apple Silicon with a menu bar app.**

oMLX serves MLX-format LLMs, VLMs, OCR, embedding and reranker models on Apple Silicon through OpenAI- and Anthropic-compatible endpoints on port 8000. It adds continuous batching on mlx-lm and a KV cache split between RAM and SSD that survives restarts. A native SwiftUI menu bar app and a web admin dashboard handle model loading, pinning, TTL and benchmarks.

- **+** Hot RAM plus cold SSD KV cache reuses prefixes, even after a server restart
- **+** Serves OpenAI and Anthropic APIs plus embeddings, rerank and tokenize endpoints
- **+** Multi-model pool with LRU eviction, pinning, per-model TTL and a memory limit
- **+** One-click setup for coding agents such as OpenCode, Codex and Hermes Agent
- **−** Apple Silicon and macOS 15+ only; no Linux, Windows or CUDA support
- **−** Some model families need native kernels, which require full Xcode to build
- **−** Models must be in MLX format; GGUF is not listed as supported
- **−** Multi-Mac distributed inference is experimental and source-build only

<sub>GPU required · Needs macOS 15+, Apple Silicon, Python 3.11-3.13, Xcode (optional, for native kernels) · Models: MLX LLMs (mlx-lm), VLMs (mlx-vlm), OCR, Embeddings, Rerankers · port 8000 · [Repo](https://github.com/jundot/omlx) · [🌐 Site ↗](https://omlx.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/omlx/)</sub>

<a name="xinference"></a>
### #&#8288;13 [Xinference](https://github.com/xorbitsai/inference) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

**Serves LLM, embedding, speech and image models behind an OpenAI-compatible API.**

Xinference runs language, embedding, speech recognition, image and multimodal models from one server started with `xinference-local`. It exposes an OpenAI-compatible REST API (including function calling), plus RPC, a CLI and a web UI, and can spread inference across multiple workers. A Community Edition is self-hosted; Enterprise, Cloud and a hosted Model API are sold separately.

- **+** Covers LLM, embedding, audio, image and multimodal models in one server
- **+** OpenAI-compatible REST API with function calling, plus CLI, RPC and web UI
- **+** Distributed multi-node deployment; Docker image and Helm chart for Kubernetes
- **+** Multiple engines, including vLLM and llama.cpp via the team's xllamacpp binding
- **−** README gives no RAM or VRAM requirements; sizing depends on the chosen model
- **−** Docker instructions target Nvidia GPUs; other accelerators are not described in the README
- **−** Enterprise, Cloud and Model API offerings are commercial; feature differences are not listed
- **−** README is mostly a news and model-support list, with little on configuration

<sub>GPU optional · Models: LLMs, embedding models, speech recognition, text-to-speech, image generation · port 9997 · [Repo](https://github.com/xorbitsai/inference) · [📖 Docs ↗](https://inference.readthedocs.io/) · [🌐 Site ↗](https://xinference.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xinference/)</sub>

<a name="freetoken"></a>
### #&#8288;14 [freetoken](https://github.com/flashml-org/freetoken) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

**MoE inference engine that runs large open models on consumer NVIDIA GPUs.**

FreeToken is a Mixture-of-Experts serving engine that splits work between GPU and CPU and keeps experts in a global LRU cache, so large MoE models can run on gaming PCs and laptops. It exposes Anthropic- and OpenAI-compatible APIs for coding agents. It ships as a Python package with a CLI and as a Windows/Linux desktop app with a GUI.

- **+** Bandwidth-adaptive CPU-GPU co-execution targets MoE models larger than VRAM
- **+** Anthropic and OpenAI-compatible APIs work with Claude Code, Codex and OpenCode
- **+** Re-allocates VRAM between expert cache and KV memory without engine restart
- **+** Supports MXFP4, NVFP4, FP8 and BF16 quantizations
- **−** Focused on MoE models; dense model support is not stated in the README
- **−** Native support listed only for NVIDIA RTX 30, 40 and 50 series
- **−** No Docker or compose files provided
- **−** Uses its own FTW weight format; old checkpoints may need repair

<sub>GPU required · Needs uv or pip, NVIDIA RTX GPU · Models: DeepSeek-V4-Flash, Qwen3.6-35B-A3B, GLM-5.2, MXFP4, NVFP4 · [Repo](https://github.com/flashml-org/freetoken) · [📖 Docs ↗](https://github.com/FlashML-org/FreeToken/blob/main/docs/quickstart.md) · [🌐 Site ↗](https://www.flashml.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/freetoken/)</sub>

<a name="exo"></a>
### #&#8288;15 [exo](https://github.com/exo-explore/exo) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (90) · Freshness: active (99) · Maintenance: patchy (37) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · Apache-2.0 · Oct 2026</sub>

**Distributed inference that pools Macs and other devices into one model-serving cluster.**

exo links devices running it into a cluster, discovers peers automatically, and splits a model across them with topology-aware pipeline or tensor parallelism. It uses MLX as the inference backend, with RDMA over Thunderbolt 5 on macOS 26.2 or later. Each node serves a dashboard and an API on port 52415 compatible with OpenAI Chat Completions, OpenAI Responses, Claude Messages and Ollama.

- **+** Automatic peer discovery, no manual cluster configuration
- **+** Tensor parallelism: 1.8x on 2 devices and 3.2x on 4, per README
- **+** Serves OpenAI, Claude Messages, Responses and Ollama API formats
- **+** Loads custom HuggingFace models; built-in dashboard for cluster and chat
- **−** On Linux it runs on CPU only; GPU support is under development
- **−** RDMA needs Thunderbolt 5 Macs, macOS 26.2+, matching OS versions and full mesh cabling
- **−** Source install needs uv, Node, Rust and, on macOS, Xcode
- **−** macOS app asks to modify system settings and install a network profile

<sub>GPU optional · Needs MLX, uv, Node.js, Rust, Xcode (macOS source build) · Models: MLX models, HuggingFace custom models · port 52415 · [Repo](https://github.com/exo-explore/exo) · [📖 Docs ↗](https://github.com/exo-explore/exo/blob/main/docs/api.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/exo/)</sub>

<a name="cog"></a>
### #&#8288;16 [cog](https://github.com/replicate/cog) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · Apache-2.0 · Oct 2026</sub>

**Packages Python ML models into Docker images with a generated HTTP API.**

Cog builds a Docker image from a cog.yaml file and a Python class that defines a model's setup and run methods. It picks compatible CUDA, cuDNN, PyTorch, TensorFlow and Python versions, generates an OpenAPI schema from the Python type annotations, and serves a REST API from a Rust/Axum server. Images can be run on your own infrastructure or deployed to Replicate.

- **+** Inputs and outputs are declared in Python types; OpenAPI schema is generated and validated
- **+** Resolves CUDA, cuDNN, PyTorch, TensorFlow and Python version combinations automatically
- **+** Same cog.yaml drives local runs (cog run, cog serve) and production builds (cog build)
- **+** Output is a standard Docker image that runs anywhere Docker does
- **−** Requires Docker, plus Buildx if using Docker Engine instead of Docker Desktop
- **−** No native Windows support; Windows 11 needs WSL 2
- **−** Model code must follow the BaseRunner interface, so existing serving code needs porting
- **−** Packages one model per container; README describes no multi-model routing or scheduling

<sub>GPU optional · Needs Docker, Docker Buildx · Models: PyTorch, TensorFlow, arbitrary Python models · port 5000 · [Repo](https://github.com/replicate/cog) · [🌐 Site ↗](https://cog.run) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cog/)</sub>

<a name="ktransformers"></a>
### #&#8288;17 [KTransformers](https://github.com/kvcache-ai/ktransformers) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Oct 2026</sub>

**CPU-GPU hybrid inference and MoE fine-tuning for large models on limited VRAM.**

KTransformers runs and fine-tunes large Mixture-of-Experts models by keeping hot experts on the GPU and cold experts on the CPU, using AMX/AVX512/AVX2 INT4/INT8 kernels with NUMA-aware memory. Inference is exposed as the kt-kernel Python package that integrates with SGLang; fine-tuning works through a LLaMA-Factory integration with LoRA and full-parameter recipes. Backends listed include NVIDIA, AMD ROCm, Intel Arc and Ascend NPU.

- **+** Runs large MoE models such as DeepSeek, Kimi and GLM with experts split across CPU and GPU
- **+** Fine-tuning via LLaMA-Factory: LoRA and BF16 full-parameter, claimed 6-12x faster than ZeRO-Offload
- **+** CPU kernels cover AMX, AVX512 and AVX2-only machines
- **+** Frequent releases with day-0 support for new MoE models
- **−** Needs large host RAM for big models; one earlier DeepSeek-R1 setup cited 382GB DRAM
- **−** README is mostly a changelog; setup lives in scattered sub-docs
- **−** Original integrated framework was archived; current scope is kt-kernel plus SFT
- **−** Performance figures come from high-end hardware such as 8×L20 and 4×RTX 4090

<sub>GPU required · Docker · Needs SGLang, LLaMA-Factory · Models: DeepSeek-V3/R1/V4-Flash, Kimi K2/K2.5/K2.6, GLM-5, MiniMax-M2/M3, Qwen3-MoE · [Repo](https://github.com/kvcache-ai/ktransformers) · [📖 Docs ↗](https://kvcache-ai.github.io/ktransformers/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ktransformers/)</sub>

<a name="llamafile"></a>
### #&#8288;18 [llamafile](https://github.com/mozilla-ai/llamafile) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · custom license · Oct 2026</sub>

**Single-file executables that bundle llama.cpp with model weights.**

llamafile packages llama.cpp and model weights into one executable using Cosmopolitan Libc, so a downloaded .llamafile runs on Linux, macOS, Windows and BSD across CPU architectures with no install and serves a local web UI and API. Since 0.10 it tracks upstream llama.cpp closely for newer models, and whisperfile applies the same packaging to speech-to-text. Maintained by Mozilla.ai.

- **+** Single file, no installation, runs across OSes and CPU architectures
- **+** 0.10 build system tracks upstream llama.cpp for recent model support
- **+** Can run external GGUF weights with the bare llamafile binary
- **+** whisperfile gives single-file transcription and translation
- **−** Windows cannot run executables above 4 GB; larger models need external weights
- **−** 0.10.x dropped some classic features; older releases remain for those
- **−** Pre-built llamafiles limited to Mozilla.ai's Hugging Face uploads
- **−** One model per file; not a multi-model server

<sub>GPU optional · Models: GGUF (bundled or external), e.g. Qwen3.5-0.8B · [Repo](https://github.com/mozilla-ai/llamafile) · [📖 Docs ↗](https://docs.mozilla.ai/llamafile) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llamafile/)</sub>

<a name="web-llm"></a>
### #&#8288;19 [web-llm](https://github.com/mlc-ai/web-llm) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Oct 2026</sub>

**In-browser LLM inference engine with an OpenAI-style JavaScript API.**

WebLLM is an npm package that runs MLC-format language models inside the browser using WebGPU, with no server component. It exposes an OpenAI-style engine.chat.completions interface with streaming, JSON mode and seeding, and supports Web Worker, Service Worker and Chrome extension setups. Custom models must be compiled to MLC format with MLC LLM.

- **+** Runs fully client-side on WebGPU, so no inference server is needed
- **+** OpenAI-style chat API with streaming, JSON mode and seed support
- **+** Worker, Service Worker and Chrome extension engines, with examples for each
- **+** Optional SRI hash verification of model config, WASM and tokenizer files
- **−** Requires a WebGPU-capable browser
- **−** First load downloads full model weights; large models take a long time
- **−** Function calling is marked WIP; the model request parameter is ignored
- **−** Custom models must be compiled to MLC format through MLC LLM

<sub>GPU required · Needs WebGPU-capable browser, MLC LLM (for compiling custom models) · Models: Llama 3, Llama 2, Phi 3, Gemma-2B, Mistral-7B · [Repo](https://github.com/mlc-ai/web-llm) · [▶️ Demo ↗](https://chat.webllm.ai/) · [📖 Docs ↗](https://webllm.mlc.ai/docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/web-llm/)</sub>

<a name="dynamo"></a>
### #&#8288;20 [dynamo](https://github.com/ai-dynamo/dynamo) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (30) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · custom license · Oct 2026</sub>

**Multi-node orchestration layer for vLLM, SGLang and TensorRT-LLM inference.**

Dynamo sits above existing inference engines (vLLM, SGLang, TensorRT-LLM) and coordinates them across GPUs and nodes. It provides disaggregated prefill/decode, KV-cache-aware routing, tiered KV offload (GPU, CPU, SSD, remote storage) and an SLA-driven planner for autoscaling, behind an OpenAI-compatible frontend. The core is written in Rust with Python bindings; Kubernetes is the recommended production target.

- **+** Adds disaggregated prefill/decode and KV-aware routing on top of vLLM, SGLang and TensorRT-LLM
- **+** KV block manager offloads cache across GPU, CPU, SSD and remote storage such as S3 or Azure blob
- **+** SLA-based planner autoscaler and Kubernetes operator with gang scheduling (Grove)
- **+** No etcd or NATS needed for local or Kubernetes deployments
- **−** Not useful for a single model on a single GPU; the README says the engine alone suffices
- **−** Production path assumes Kubernetes and multi-GPU clusters; heavy for small setups
- **−** Zero-config deploy (DGDR) is marked beta
- **−** KVBM support for SGLang is still marked in progress

<sub>GPU required · Docker · Needs vLLM, SGLang or TensorRT-LLM, Kubernetes (production) · Models: vLLM, SGLang, TensorRT-LLM, OpenAI-compatible API, multimodal · port 8000 · [Repo](https://github.com/ai-dynamo/dynamo) · [📖 Docs ↗](https://docs.nvidia.com/dynamo/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dynamo/)</sub>

<a name="openvino"></a>
### #&#8288;21 [openvino](https://github.com/openvinotoolkit/openvino) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**Inference toolkit for converting and running models on Intel CPUs, GPUs and NPUs.**

OpenVINO converts models from PyTorch, TensorFlow, ONNX, TensorFlow Lite, PaddlePaddle and JAX/Flax and runs them on x86 and ARM CPUs, Intel integrated and discrete GPUs, and Intel NPUs. It has C++, Python, C and NodeJS APIs, with a separate GenAI repo for LLM, speech and image pipelines. Quantization (NNCF) and serving (OpenVINO Model Server) are separate repos.

- **+** Converts models from several frameworks, so the original framework is not needed at deploy time
- **+** One API targets x86 and ARM CPUs, Intel GPUs and Intel NPUs
- **+** APIs in C++, Python, C and NodeJS; installs with pip install openvino
- **+** Integrates with Optimum Intel, ONNX Runtime, vLLM, LangChain, LlamaIndex and Keras 3
- **−** GPU and NPU support is limited to Intel hardware
- **−** Core library is not an HTTP server; serving needs OpenVINO Model Server
- **−** GenAI pipelines and quantization live in separate repos from the core
- **−** Collects usage telemetry by default; opting out requires running a command

<sub>GPU optional · Models: PyTorch, TensorFlow, ONNX, TensorFlow Lite, PaddlePaddle · [Repo](https://github.com/openvinotoolkit/openvino) · [📖 Docs ↗](https://docs.openvino.ai/2026/index.html) · [🌐 Site ↗](https://docs.openvino.ai/2026/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openvino/)</sub>

<a name="magnitude"></a>
### #&#8288;22 [magnitude](https://github.com/magnitudedev/magnitude) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Oct 2026</sub>

**Local inference engine that tunes kernels per model on your hardware.**

Magnitude is a desktop app and CLI inference engine that runs open-weight models on Apple Silicon, NVIDIA, AMD or CPU. When a model is downloaded it spends up to a minute tuning kernels on the local chip, and ships a speculative decoding drafter per model. It connects to agents such as Pi, OpenCode, Codex, Claude Code and Cline, or any client through an OpenAI-compatible API.

- **+** Per-model kernel tuning at download time; README reports ~2.2x faster decode than Ollama on Mac and NVIDIA
- **+** Runs on Apple Silicon, NVIDIA, AMD or CPU across macOS, Windows and Linux
- **+** One-click connection to eight named agents; OpenAI-compatible API for the rest
- **+** `magnitude server setup` installs a self-updating boot service for remote use
- **−** Optimized kernels cover popular open-weight families only; full model list is on the website
- **−** Benchmarks are the project's own and compare mainly against Ollama
- **−** No Docker or compose setup mentioned in the README
- **−** Model formats, RAM minimums and API port are not documented in the README

<sub>GPU optional · Models: Open-weight LLM families listed at magnitude.dev/models, OpenAI-compatible API · [Repo](https://github.com/magnitudedev/magnitude) · [📖 Docs ↗](https://docs.magnitude.dev) · [🌐 Site ↗](https://magnitude.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/magnitude/)</sub>

<a name="mlx-lm"></a>
### #&#8288;23 [mlx-lm](https://github.com/ml-explore/mlx-lm) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · MIT · Oct 2026</sub>

**Python package and CLI for running and fine-tuning LLMs on Apple silicon with MLX.**

MLX LM generates text, chats in a terminal REPL, and fine-tunes LLMs on Apple silicon using the MLX framework. It loads models from the Hugging Face Hub, quantizes and uploads them, and supports LoRA and full fine-tuning, including on quantized models. It ships a Python API and command-line tools such as mlx_lm.generate, mlx_lm.chat and mlx_lm.server.

- **+** Pulls MLX-compatible models from Hugging Face, with thousands in the MLX Community org
- **+** Converts, quantizes (e.g. 4-bit) and uploads models with one command
- **+** LoRA and full fine-tuning, including on quantized models
- **+** Rotating KV cache, prompt caching and configurable prefill step size for long contexts
- **−** Targets Apple silicon only, per the README
- **−** Wiring memory for large models needs macOS 15 or higher
- **−** Unsupported model architectures need an issue or a pull request
- **−** Some tokenizers require enabling trust_remote_code

<sub>Needs MLX, Hugging Face Hub · Models: Hugging Face Hub models in MLX format, quantized models, LoRA, full fine-tuning · [Repo](https://github.com/ml-explore/mlx-lm) · [📖 Docs ↗](https://github.com/ml-explore/mlx-lm/blob/main/mlx_lm/LORA.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlx-lm/)</sub>

<a name="vllm-omni"></a>
### #&#8288;24 [vllm-omni](https://github.com/vllm-project/vllm-omni) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Oct 2026</sub>

**Serving engine for omni-modality, diffusion, TTS and robot-policy models, built on vLLM.**

vLLM-Omni extends vLLM beyond text autoregressive models to Diffusion Transformers and other non-autoregressive models, handling text, image, audio, video and action inputs and outputs. It runs multi-stage pipelines with disaggregated stages and exposes an OpenAI-compatible API server, including full-duplex realtime serving with streaming audio. Releases track even-numbered upstream vLLM versions.

- **+** Covers omni, TTS, diffusion (image/video/audio) and robot-policy models in one runtime
- **+** Reuses vLLM KV cache management; supports tensor, pipeline, data and expert parallelism
- **+** OpenAI-compatible server with streaming outputs and full-duplex realtime audio API
- **+** Hardware coverage listed as CUDA, ROCm, MUSA, NPU and XPU; Apache-2.0
- **−** Version and model support tied to specific vLLM releases; needs matching upstream vLLM
- **−** README gives no RAM or VRAM requirements; check per-model recipes
- **−** Setup and model coverage live in external docs, not the README
- **−** Multi-stage disaggregated pipelines add operational complexity over a single-model server

<sub>GPU required · Docker · Needs vLLM · Models: Qwen3-Omni, MiniCPM-o 4.5, Cosmos3, BAGEL, Qwen3-TTS · [Repo](https://github.com/vllm-project/vllm-omni) · [📖 Docs ↗](https://vllm-omni.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vllm-omni/)</sub>

<a name="triton-inference-server"></a>
### #&#8288;25 [Triton Inference Server](https://github.com/triton-inference-server/server) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · BSD-3-Clause · Oct 2026</sub>

**NVIDIA inference server for TensorRT, PyTorch, ONNX and more over HTTP/gRPC.**

Triton serves TensorRT, PyTorch, ONNX, OpenVINO, Python and RAPIDS FIL models over HTTP/REST and gRPC (KServe v2), with concurrent execution, dynamic and sequence batching, ensembles and Business Logic Scripting. NVIDIA ships it as NGC containers (2.73.0 / 26.09) for NVIDIA GPUs, x86 and ARM CPUs, Jetson and AWS Inferentia, with C and Java in-process APIs and a metrics endpoint.

- **+** Serves TensorRT, PyTorch, ONNX, OpenVINO, Python and FIL models together
- **+** Dynamic and sequence batching, ensembles and BLS pipelines
- **+** HTTP/REST and gRPC (KServe v2) plus C and Java in-process APIs
- **+** Metrics for GPU utilization, throughput and latency
- **−** No OpenAI-compatible endpoint in the README; clients speak KServe v2
- **−** Model repository and per-model config files are hand-written
- **−** Containers track NVIDIA's monthly NGC release cycle
- **−** Not every backend is supported on every platform

<sub>GPU optional · Docker · Models: TensorRT, PyTorch, ONNX, OpenVINO, Python, RAPIDS FIL backends · [Repo](https://github.com/triton-inference-server/server) · [🌐 Site ↗](https://developer.nvidia.com/nvidia-triton-inference-server) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/triton-inference-server/)</sub>

<a name="kimi-k3-in-c"></a>
### #&#8288;26 [kimi-k3-in-c](https://github.com/fareedkhan-dev/kimi-k3-in-c) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Oct 2026</sub>

**Kimi K3 inference engine in portable C99 that streams weights from disk.**

Runs the 2.78T-parameter Kimi K3 checkpoint (1.56 TB) on CPU in C99, with no BLAS, framework or GPU. The dense trunk is packed and streamed from disk, and routed experts are multiplied directly from their 4-bit form through an LRU cache. Output is stated to be byte-identical from 8 GB up to 224 GB of RAM; only speed changes, from 26.5 s per token at 8 GB to 5.6 s at 128 GB+.

- **+** Runs a 2.78T-parameter model in 8.24 GB peak RSS, measured
- **+** Small C99 codebase: needs only a compiler, libm and OpenMP
- **+** make test checks the engine against PyTorch fixtures without a checkpoint
- **+** Builds on Linux x86-64, macOS arm64 and Windows; AVX2/FMA and NEON
- **−** Needs about 1.7 TB free disk for checkpoint and packed trunk
- **−** 26.5 s per token at 8 GB and 5.6 s at 128 GB+; too slow for interactive use
- **−** Targets Kimi K3 only; no other model formats mentioned
- **−** No HTTP API or server mode in the visible README

<sub>RAM ≥ 8 GB · no GPU · Needs C99 compiler (GCC >= 9 or Clang >= 10), OpenMP, GNU make or CMake, Python 3.9+ for download and pack tools, Hugging Face token for checkpoint download · Models: Kimi K3 (safetensors, 4-bit packed experts) · [Repo](https://github.com/fareedkhan-dev/kimi-k3-in-c) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kimi-k3-in-c/)</sub>

<a name="geniex"></a>
### #&#8288;27 [geniex](https://github.com/qualcomm/geniex) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · BSD-3-Clause · Oct 2026</sub>

**LLM and VLM inference runtime for Qualcomm Snapdragon NPU, GPU and CPU.**

GenieX is an on-device inference runtime for Snapdragon devices, built on one C SDK. It runs GGUF models through llama.cpp on NPU, GPU or CPU, and pre-compiled Qualcomm AI Hub bundles through Qualcomm AI Engine Direct on the NPU. It is exposed as a CLI, Python package, Android Kotlin/Java SDK, Docker image and an OpenAI-compatible server on port 18181. Status is developer preview.

- **+** Runs GGUF models from Hugging Face, ModelScope or Docker Hub on Hexagon NPU, Adreno GPU or CPU
- **+** Pre-compiled AI Hub bundles use the qairt runtime for NPU-only execution
- **+** One C SDK with CLI, Python, Android, Docker and OpenAI-compatible server wrappers
- **+** Python API mirrors transformers from_pretrained() and generate()
- **−** Runs only on Qualcomm Snapdragon; no x86 or Apple hardware support
- **−** Marked developer preview; interfaces may change between releases
- **−** AI Hub bundles are per-chipset and the available catalogue changes independently
- **−** For llama.cpp on the Hexagon NPU, only the Q4_0 precision is recommended

<sub>GPU optional · Needs Qualcomm Snapdragon device, llama.cpp, Qualcomm AI Engine Direct (QAIRT) · Models: GGUF, Qualcomm AI Hub bundles, LLM, VLM · port 18181 · [Repo](https://github.com/qualcomm/geniex) · [📖 Docs ↗](https://geniex.aihub.qualcomm.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/geniex/)</sub>

<a name="mistral-rs"></a>
### #&#8288;28 [mistral.rs](https://github.com/ericlbuehler/mistral.rs) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · MIT · Oct 2026</sub>

**Rust inference engine with OpenAI and Anthropic compatible APIs.**

mistral.rs is a Rust inference engine that loads Hugging Face models and GGUF files, detects architecture and chat template, and serves them via `mistralrs serve` on OpenAI-compatible /v1 and Anthropic Messages endpoints. It supports CUDA, Metal, PagedAttention, continuous batching, ISQ and UQFF quantization, and multi-GPU. It also includes a built-in web UI, Python and Rust SDKs, and a server-side agentic loop with web search, code and shell execution, and an MCP client.

- **+** Serves both OpenAI /v1 and Anthropic /v1/messages APIs from one process
- **+** Quantization options: ISQ, UQFF, GGUF 2-8 bit, GPTQ, AWQ, HQQ, FP8, BNB
- **+** Python and Rust SDKs allow in-process inference without running a server
- **+** README benchmarks show higher Q8 prefill than llama.cpp on GB10, B200 and H100
- **−** README's BF16 benchmarks show much lower Gemma 4 26B-A4B prefill than vLLM
- **−** v0.9.5 changed memory and device-mapping options, so upgrades need migration
- **−** Install is via a curl-to-shell script; separate wheels per accelerator for Python
- **−** Built-in agent features (shell, code execution) add setup and sandboxing concerns

<sub>GPU optional · Docker · Models: Hugging Face models, GGUF, UQFF, GPTQ, AWQ · port 1234 · [Repo](https://github.com/ericlbuehler/mistral.rs) · [📖 Docs ↗](https://docs.mistralrs.dev/) · [🌐 Site ↗](https://mistralrs.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mistral-rs/)</sub>

<a name="mooncake"></a>
### #&#8288;29 [mooncake](https://github.com/kvcache-ai/mooncake) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Oct 2026</sub>

**KV cache transfer engine and distributed cache store for LLM inference clusters.**

Mooncake is the serving platform behind Kimi, built around a KV cache-centric split of prefill and decode clusters. It provides a Transfer Engine for batched data movement over RDMA, TCP, NVLink, EFA and other transports, plus Mooncake Store, a distributed KV cache and weight store spanning DRAM and SSD. It is integrated into SGLang, vLLM, TensorRT-LLM, LMDeploy and others.

- **+** Transfer Engine reports up to 190 GB/s on 8x400 Gbps RoCE, about 4.6x faster than TCP
- **+** Integrated upstream in SGLang, vLLM, TensorRT-LLM, LMDeploy, NIXL and vLLM-Ascend
- **+** Mooncake Store pools KV cache across DRAM and SSD/NVMe with replication and eviction
- **+** Separate PyPI wheels for CUDA, ROCm, NPU, MUSA, EFA and non-CUDA builds
- **−** Infrastructure component, not a standalone server; needs a serving engine such as vLLM or SGLang
- **−** Reported bandwidth figures assume RDMA NICs and multi-node GPU clusters
- **−** Several wheel variants by CUDA version make installation choice non-trivial
- **−** Hardware requirements and minimum RAM are not stated in the visible README

<sub>GPU optional · Docker · Needs RDMA NICs (for high-bandwidth transport), SGLang or vLLM (integration) · Models: LLMs via SGLang, vLLM, TensorRT-LLM, LMDeploy integrations · [Repo](https://github.com/kvcache-ai/mooncake) · [📖 Docs ↗](https://kvcache-ai.github.io/Mooncake/) · [🌐 Site ↗](https://kvcache.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mooncake/)</sub>

<a name="apfel"></a>
### #&#8288;30 [apfel](https://github.com/arthur-ficial/apfel) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Oct 2026</sub>

**CLI and local OpenAI-compatible server for Apple's on-device Mac language model.**

apfel wraps Apple's FoundationModels on-device LLM as a pipe-friendly UNIX command and as a local server at http://localhost:11434/v1 that implements chat completions, responses, tool calling and JSON-schema output. It also offers a chat REPL, file/PDF/image attachment with on-device OCR, and MCP tool support (local and remote). Inference stays on the machine and needs no API key.

- **+** Drop-in OpenAI-style /v1/chat/completions and /v1/responses endpoints with streaming and tool calling
- **+** Schema-guaranteed JSON output via FoundationModels guided generation
- **+** Installs with brew install apfel; no API keys, inference stays on-device
- **+** Attaches MCP servers (local and Streamable HTTP) and PDFs/images via -f
- **−** Requires macOS 26+ on Apple Silicon with Apple Intelligence enabled
- **−** Single fixed ~3B model; context window is only 4096 tokens (8192 on some macOS 27 Macs)
- **−** No embeddings or legacy completions; n>1, logprobs and stop are rejected
- **−** Apple guardrails can block benign prompts; --permissive only reduces this

<sub>no GPU · Needs macOS 26 Tahoe or newer, Apple Silicon (M1+), Apple Intelligence enabled · Models: apple-foundationmodel (Apple FoundationModels, ~3B on-device) · port 11434 · [Repo](https://github.com/arthur-ficial/apfel) · [📖 Docs ↗](https://github.com/Arthur-Ficial/apfel/blob/main/docs/install.md) · [🌐 Site ↗](https://apfel.franzai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/apfel/)</sub>

<a name="llama-cpp-python"></a>
### #&#8288;31 [llama-cpp-python](https://github.com/abetlen/llama-cpp-python) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (44) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**Python bindings and OpenAI-compatible server for llama.cpp.**

Python package that wraps llama.cpp through ctypes, with a high-level Llama class for completion and chat on GGUF models. It also ships an OpenAI-compatible web server supporting function calling, vision models and multiple models. Installation builds llama.cpp from source via pip, with CMAKE_ARGS selecting backends such as CUDA, Metal, ROCm, Vulkan, SYCL, BLAS and RPC; pre-built wheels exist for some.

- **+** Low-level ctypes access to the C API plus a high-level Llama class
- **+** OpenAI-compatible server with function calling, vision and multi-model config
- **+** JSON and JSON Schema constrained output via response_format
- **+** Pre-built wheels for CPU, CUDA, Metal, ROCm and Vulkan avoid local compilation
- **−** Default pip install compiles llama.cpp and needs a C compiler
- **−** Only GGUF models are supported
- **−** Pre-built GPU wheels cover limited Python versions (3.10 to 3.12) and CUDA versions
- **−** Function calling needs a specific chat format such as chatml-function-calling or functionary

<sub>GPU optional · Docker · Needs Python 3.8+, C compiler, CMake · Models: GGUF, llava, moondream2, minicpm-v-2.6, qwen2.5-vl · [Repo](https://github.com/abetlen/llama-cpp-python) · [📖 Docs ↗](https://llama-cpp-python.readthedocs.io/en/latest) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llama-cpp-python/)</sub>

<a name="turbo-fieldfare"></a>
### #&#8288;32 [turbo-fieldfare](https://github.com/drumih/turbo-fieldfare) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

**Swift and Metal runtime that runs Gemma 4 26B-A4B in about 2 GB RAM.**

TurboFieldfare is a model-specific Swift and Metal inference runtime for Gemma 4 26B-A4B (4-bit MLX affine) on Apple Silicon. It keeps the 1.35 GB shared core and FP16 KV cache in memory and streams only the needed experts from SSD through a 16-slot LFU cache. It ships a native Mac app, a CLI, an experimental loopback OpenAI-compatible server and optional image input.

- **+** Runs a 26B MoE model in about 2 GB of weights plus 4K KV cache on 8 GB Macs
- **+** Measured 5.1-6.3 tok/s on an 8 GB M2 Air and 31-35 tok/s on a 24 GB M5 Pro
- **+** Includes Mac app, CLI and loopback server with Chat Completions, streaming and function tools
- **+** Installer streams and repacks weights with hash-verified manifest, no second full checkpoint on disk
- **−** Supports only one pinned model, Gemma 4 26B-A4B instruction checkpoint
- **−** Requires macOS 26, Metal 4 and Swift 6.2; arm64 only
- **−** Needs about 14.3 GB of SSD space and a roughly 15 GB first download
- **−** Server has no authentication or TLS and is marked experimental; audio and video unsupported

<sub>RAM ≥ 8 GB · GPU required · Needs Swift 6.2+, macOS 26 SDK, Metal 4, Hugging Face (model download) · Models: Gemma 4 26B-A4B IT (MLX 4-bit, .gturbo format) · port 8080 · [Repo](https://github.com/drumih/turbo-fieldfare) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/turbo-fieldfare/)</sub>

<a name="kserve"></a>
### #&#8288;33 [kserve](https://github.com/kserve/kserve) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Oct 2026</sub>

**Kubernetes inference platform for generative and predictive models via InferenceService.**

KServe is a Kubernetes custom-resource platform that deploys LLMs and classic ML models as InferenceService objects. It supports vLLM and llm-d backends with an OpenAI-compatible protocol for generative models, and TensorFlow, PyTorch, scikit-learn, XGBoost and ONNX for predictive ones. Canary rollouts, InferenceGraph pipelines, autoscaling and scale-to-zero are included, depending on the install mode. It is a CNCF incubating project.

- **+** Covers both LLM serving (vLLM, llm-d) and predictive frameworks in one platform
- **+** OpenAI-compatible inference protocol for generative models
- **+** Scale-to-zero, canary rollouts and InferenceGraph pipelines for predictive workloads
- **+** CNCF incubating project; also available as a Kubeflow add-on
- **−** Requires a Kubernetes cluster; not a single-process local server
- **−** Standard Kubernetes install lacks canary and scale-to-zero autoscaling; those need Knative
- **−** Several install modes (Knative, ModelMesh, raw Kubernetes) add operational complexity
- **−** README gives no hardware requirements or example ports

<sub>GPU optional · Docker · Needs Kubernetes, Knative (serverless mode), ModelMesh (optional) · Models: vLLM, llm-d, Hugging Face, TensorFlow, PyTorch · [Repo](https://github.com/kserve/kserve) · [📖 Docs ↗](https://kserve.github.io/website/docs/getting-started/genai-first-isvc) · [🌐 Site ↗](https://kserve.github.io/website/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kserve/)</sub>

<a name="llama-swap"></a>
### #&#8288;34 [llama-swap](https://github.com/mostlygeek/llama-swap) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · MIT · Oct 2026</sub>

**Go proxy that starts and swaps local inference servers per request.**

llama-swap is a single Go binary that sits in front of local inference servers such as llama.cpp, vllm, stable-diffusion.cpp and audio.cpp. It reads the `model` field of each OpenAI- or Anthropic-style request, starts the matching server from a YAML `cmd`, and stops the previous one. It includes a web UI, API keys, TTL unloading and a matrix DSL for running models concurrently.

- **+** One binary and one YAML file, no external dependencies
- **+** Works with any OpenAI- or Anthropic-compatible upstream server, not only llama.cpp
- **+** Matrix DSL runs chosen models concurrently; ttl unloads idle ones
- **+** Built-in web UI with playground, token metrics, log streaming and Prometheus /metrics
- **−** Does not run inference itself; you supply and configure the upstream servers
- **−** Originally designed for llama-server; Python servers like vllm should run in Docker or Podman
- **−** Swapping reloads the model, so the first request after a switch is slow
- **−** Auth is limited to API keys; no user accounts mentioned

<sub>GPU optional · Docker · Needs llama.cpp or another OpenAI-compatible inference server · Models: GGUF via llama.cpp, vllm, stable-diffusion.cpp, whisper.cpp, audio.cpp · port 8080 · [Repo](https://github.com/mostlygeek/llama-swap) · [📖 Docs ↗](https://github.com/mostlygeek/llama-swap/tree/main/docs/kb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llama-swap/)</sub>

<a name="lmdeploy"></a>
### #&#8288;35 [LMDeploy](https://github.com/internlm/lmdeploy) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · Apache-2.0 · Oct 2026</sub>

**LLM and VLM inference server with quantization, TurboMind and PyTorch engines.**

LMDeploy compresses, deploys and serves LLMs and vision-language models through two engines: TurboMind (CUDA-kernel focused) and a pure-Python PyTorch engine. It offers an offline pipeline API, an API server, a proxy server for multi-model and multi-machine setups, and AWQ, weight-only and KV cache quantization. Installed via pip on Python 3.10 to 3.13.

- **+** Two engines: TurboMind for throughput, pure-Python PyTorch engine for easier extension
- **+** Supports 4-bit AWQ, weight-only and int8/int4 KV cache quantization, usable together with prefix caching
- **+** Proxy server distributes requests across multiple models, machines and GPUs
- **+** Broad model list including DeepSeek, Qwen3, gpt-oss, InternVL; Huawei Ascend supported via PyTorch engine
- **−** Supported models and data types differ per engine; must check a table to pick one
- **−** Throughput claims (1.8x vLLM) come from older benchmarks and are not re-verified here
- **−** Default wheels target CUDA 12.8; other platforms need extra setup
- **−** Hardware requirements such as VRAM and RAM are not stated in the README

<sub>GPU required · Docker · Needs Python 3.10-3.13, CUDA 12.8 (default wheels) · Models: Llama, Qwen, InternLM, InternVL, DeepSeek · [Repo](https://github.com/internlm/lmdeploy) · [📖 Docs ↗](https://lmdeploy.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmdeploy/)</sub>

<a name="laya-mlx"></a>
### #&#8288;36 [laya-mlx](https://github.com/mizorewww/laya-mlx) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · Apache-2.0 · Oct 2026</sub>

**MLX port of Laya typed-decision models for Apple Silicon, no token decoding.**

Independent MLX port of Convai Innovations' Laya models, which answer typed questions (choice, score, yes/no probability) about a text state in one bidirectional forward pass instead of generating tokens. It reports 13.4 ms median for a short English question on an M3 Max, with no PyTorch or Transformers dependency. It includes a language router, HTTP and MCP serving extras, and framework integrations.

- **+** Median 13.42 ms (421M) and 7.39 ms (322M multilingual) per short question on M3 Max
- **+** Matched upstream answers on 63/63 validation questions in FP32 and FP16
- **+** Pure MLX and Rust tokenizer; no PyTorch or Transformers needed at inference
- **+** Optional extras for serving, MCP, LangChain, LangGraph, LlamaIndex, CrewAI and Agno
- **−** Apple Silicon only, macOS 14+; CUDA, ONNX and training are not supported
- **−** Constrained choice, score and noul outputs only; it does not generate text
- **−** Training and fine-tuning stay in the upstream project
- **−** Context limit of 512 to 1,024 tokens; language detection is heuristic

<sub>GPU required · Needs Apple Silicon, MLX, Python 3.11+, Hugging Face Hub (checkpoint download) · Models: convaiinnovations/laya (ModernBERT-large, 421M), convaiinnovations/laya-multilingual (mmBERT-base, 322M), convaiinnovations/laya-typed-decisions (ModernBERT-large, 421M) · [Repo](https://github.com/mizorewww/laya-mlx) · [📖 Docs ↗](https://github.com/mizorewww/laya-mlx/blob/main/BENCHMARKS.md) · [🌐 Site ↗](https://huggingface.co/aac6fef/laya-mlx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/laya-mlx/)</sub>

<a name="gpustack"></a>
### #&#8288;37 [GPUStack](https://github.com/gpustack/gpustack) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

**GPU cluster manager that schedules vLLM, SGLang and TensorRT-LLM deployments.**

GPUStack manages GPU workers across on-premises servers, Kubernetes and cloud providers, and deploys models onto them with vLLM, SGLang, TensorRT-LLM or a custom engine. It exposes OpenAI-compatible endpoints with API keys, access control, token metering and Grafana/Prometheus monitoring. It can also launch SSH-accessible GPU instances on demand.

- **+** Pluggable engines: vLLM, SGLang, TensorRT-LLM, or a custom engine
- **+** Supports NVIDIA, AMD, Ascend, Hygon, MThreads, Iluvatar, MetaX, Cambricon and T-Head accelerators
- **+** Built-in auth, API keys, token metering and Grafana/Prometheus dashboards
- **+** Model catalog and chat playground; server can run on a CPU-only node
- **−** Worker nodes are Linux only; macOS is not supported as a worker
- **−** Needs Docker on every node, plus NVIDIA Container Toolkit for NVIDIA workers
- **−** Cluster Topology view is in the Enterprise edition
- **−** Worker container runs privileged with host networking and the Docker socket mounted

<sub>GPU required · Compose · Needs Docker, NVIDIA driver, NVIDIA Container Toolkit · Models: vLLM, SGLang, TensorRT-LLM, custom engines, LLM · port 80 · [Repo](https://github.com/gpustack/gpustack) · [📖 Docs ↗](https://docs.gpustack.ai) · [🌐 Site ↗](https://gpustack.ai/enterprise/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpustack/)</sub>

<a name="libretranslate"></a>
### #&#8288;38 [libretranslate](https://github.com/libretranslate/libretranslate) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · AGPL-3.0 · Oct 2026</sub>

**Self-hosted machine translation API built on Argos Translate.**

LibreTranslate is a self-hosted machine translation API with a web interface for translating text. Translation runs locally on the open-source Argos Translate engine, so it does not call Google, Azure or other proprietary services. The README is short and defers setup and API usage to the external docs site.

- **+** Translates locally through Argos Translate, with no proprietary translation API calls
- **+** Public hosted instance at libretranslate.com to try before installing
- **+** Separate API usage guide and community forum
- **+** Written in Python and published on PyPI
- **−** README gives no hardware requirements, ports or language list
- **−** Setup and API details live only on the external docs site
- **−** AGPL-3.0 license imposes obligations on networked modifications
- **−** Translation quality depends on Argos models, which the README does not benchmark

<sub>Docker + Compose · Needs Argos Translate · Models: Argos Translate · [Repo](https://github.com/libretranslate/libretranslate) · [▶️ Demo ↗](https://libretranslate.com) · [📖 Docs ↗](https://docs.libretranslate.com) · [🌐 Site ↗](https://libretranslate.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/libretranslate/)</sub>

<a name="lemonade"></a>
### #&#8288;39 [Lemonade](https://github.com/lemonade-sdk/lemonade) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Oct 2026</sub>

**Local inference server for LLM, speech and image models on AMD NPU and GPU.**

Lemonade is a C++ local server that exposes OpenAI, Anthropic and Ollama-compatible APIs on http://localhost:13305/v1. It runs text, speech-to-text, text-to-speech, image and audio generation through several backends (llama.cpp, FastFlowLM, Ryzen AI, whisper.cpp, sd.cpp, vLLM) across CPU, GPU and XDNA2 NPU. It also ships a CLI, a Model Manager and an embeddable binary for bundling into other apps.

- **+** Supports NPU, ROCm, CUDA, Vulkan, Metal and CPU backends, selected per modality
- **+** Serves OpenAI, Anthropic and Ollama APIs, so existing clients connect unchanged
- **+** Covers chat, transcription, TTS, image and 3D generation in one server
- **+** Embeddable binary option with no installer, branding or telemetry
- **−** NPU backends are limited to AMD XDNA2; ryzenai-llm is Windows only
- **−** Many backends are marked experimental, including vllm, hrx, openmoss and trellis
- **−** Cloud offload to OpenAI-compatible providers is marked experimental
- **−** Backend support varies by OS and GPU, so check lemonade backends first

<sub>GPU optional · Docker · Models: GGUF, ONNX, FLM, Whisper, Stable Diffusion · port 13305 · [Repo](https://github.com/lemonade-sdk/lemonade) · [🌐 Site ↗](https://lemonade-server.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lemonade/)</sub>

<a name="ds4"></a>
### #&#8288;40 [ds4](https://github.com/antirez/ds4) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Oct 2026</sub>

**Native C inference engine for a few large open models on Mac, CUDA and ROCm.**

DwarfStar is a narrow C inference engine for DeepSeek V4 Flash and PRO, GLM 5.x and Qwen3.8 Flash Next, with Metal, CUDA and ROCm backends. It ships a CLI, an HTTP server (default 127.0.0.1:8000), a native coding agent and an eval tool. It is not a general GGUF runner and only loads the GGUF files the project produces. SSD streaming lets models run beyond RAM.

- **+** Metal, CUDA (DGX Spark, multi-GPU, Ada/L40S) and ROCm on Strix Halo backends
- **+** SSD streaming runs models larger than RAM; tensor and pipeline parallelism across machines
- **+** Includes server, CLI, native coding agent and ds4-eval regression suite in one repo
- **+** Self-contained C code that does not link against GGML
- **−** Not a general GGUF runner; only project-produced GGUF files load
- **−** README calls it beta quality, fast-changing, with possible regressions
- **−** Model support is opportunistic; models may be removed when replaced
- **−** No tagged releases; built from source with make

<sub>RAM ≥ 64 GB · GPU optional · Models: DeepSeek V4 Flash, DeepSeek V4.1 Flash, DeepSeek V4 PRO, GLM 5.2, GLM 5.3 · port 8000 · [Repo](https://github.com/antirez/ds4) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ds4/)</sub>

<a name="text-generation-webui"></a>
### #&#8288;41 [Text Generation Web UI](https://github.com/oobabooga/textgen) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: weak (18) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · AGPL-3.0 · Aug 2026</sub>

**Local LLM chat UI and API with five switchable loader backends.**

TextGen runs local LLMs behind a chat UI and an OpenAI/Anthropic-compatible API with tool calling and MCP, with llama.cpp, ik_llama.cpp, Transformers, ExLlamaV3 or TensorRT-LLM loaders switchable without restart. Portable builds for Linux, Windows and macOS bundle CUDA, Vulkan, ROCm or CPU dependencies for GGUF; the full install adds LoRA training, image generation and extensions. Web UI on port 7860.

- **+** Portable builds with all dependencies for CUDA, Vulkan, ROCm and CPU
- **+** Five loaders switchable without restarting
- **+** OpenAI and Anthropic-compatible API with tool calling and MCP servers
- **+** LoRA training and diffusers image generation in the same app
- **−** Full install needs ~10 GB disk and PyTorch; portable build is GGUF only
- **−** Multi-user mode does not save chat histories; meant for small trusted teams
- **−** Docker needs per-GPU Dockerfile symlinks and manual .env edits
- **−** AGPL-3.0 license

<sub>GPU optional · Docker + Compose · Models: GGUF via llama.cpp and ik_llama.cpp, Transformers safetensors, EXL3 via ExLlamaV3, TensorRT-LLM · port 7860 · [Repo](https://github.com/oobabooga/textgen) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/text-generation-webui/)</sub>

<a name="tensorrt"></a>
### #&#8288;42 [tensorrt](https://github.com/nvidia/tensorrt) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**Open-source plugins, ONNX parser and samples for NVIDIA TensorRT inference.**

This repository holds the open-source parts of NVIDIA TensorRT 11.x: the plugin sources, the ONNX parser and sample applications. It is a subset of the GA release and builds with CMake against a separately downloaded TensorRT package. The Python package installs with `pip install tensorrt`, so building is only needed for the C++ components.

- **+** Build targets cover Linux x86-64, aarch64, Jetson Thor, DriveOS, QNX and Windows
- **+** Import paths documented for ONNX, Torch-TensorRT, HuggingFace/Optimum and the network API
- **+** Per-model support matrix covers LLM, vision, audio, diffusion and multimodal models
- **+** Python package installs with a single pip command
- **−** Only a subset of TensorRT; the core engine is a separate GA download
- **−** Requires an NVIDIA GPU and CUDA 12.9 or 13.4
- **−** 11.x removed weakly-typed networks, implicit quantization, IPluginV2 and TREX, so migration is needed
- **−** Not an HTTP model server; it is a library, so serving needs other tooling

<sub>GPU required · Docker · Needs TensorRT 11.4.0.106 GA build, CUDA 12.9 or 13.4, CMake >= 3.31, Python 3.10-3.14, cuDNN 8.9 (optional), NCCL (optional) · Models: ONNX, Torch-TensorRT, HuggingFace/Optimum · [Repo](https://github.com/nvidia/tensorrt) · [📖 Docs ↗](https://docs.nvidia.com/deeplearning/sdk/tensorrt-developer-guide/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorrt/)</sub>

<a name="deepinfer"></a>
### #&#8288;43 [deepinfer](https://github.com/deepseek-ai/deepinfer) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: weak (26) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Oct 2026</sub>

**Offline inference engine for DeepSeek-V4.1-Flash on NVIDIA SM100 and Ascend 950.**

DeepInfer is the inference framework DeepSeek uses for its production services, released here with offline inference only. It runs DeepSeek-V4.1-Flash with custom kernels, attention data parallelism, MoE expert parallelism with load balancing, draft-token decoding, and structured outputs. A complete serving stack still needs a KV cache system, prefill/decode disaggregation and load balancing, which are not included.

- **+** Batch-invariant inference and deterministic sampling with a fixed seq_seed (NVIDIA only)
- **+** Structured outputs constrained by regex, JSON schema or EBNF grammar
- **+** Supports both NVIDIA SM100 GPUs and Huawei Ascend 950 NPUs
- **+** Asynchronous batch scheduling is on by default; benchmark sweep script is included
- **−** Supports only one model: DeepSeek-V4.1-Flash
- **−** Offline inference only; no HTTP server or API in this release
- **−** KV cache, disaggregation and load balancing are not included
- **−** Needs Python 3.12, GCC 13+, CUDA 13 or CANN 9.2, and a source build

<sub>GPU required · Needs CUDA 13, CANN 9.2, GCC >= 13, Python 3.12, Hugging Face model download · Models: DeepSeek-V4.1-Flash · [Repo](https://github.com/deepseek-ai/deepinfer) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepinfer/)</sub>

<a name="mlc-llm"></a>
### #&#8288;44 [mlc-llm](https://github.com/mlc-ai/mlc-llm) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: patchy (31) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · Apache-2.0 · Oct 2026</sub>

**ML compiler and inference engine for running LLMs on GPUs, phones and browsers.**

MLC LLM compiles language models and runs them through MLCEngine, a single inference engine targeting CUDA, ROCm, Vulkan, Metal, OpenCL and WebGPU/WASM. MLCEngine exposes an OpenAI-compatible API via a REST server and Python, JavaScript, iOS and Android bindings. The README is brief and defers install and usage details to the external docs.

- **+** One engine covers AMD, NVIDIA, Apple and Intel GPUs on Linux, Windows and macOS
- **+** Also targets browsers (WebGPU/WASM), iOS/iPadOS and Android (Adreno, Mali via OpenCL)
- **+** OpenAI-compatible API over REST, Python, JavaScript, iOS and Android
- **+** Apache-2.0 license
- **−** README gives no install steps, model list or memory requirements; docs are external
- **−** No Docker or compose files detected
- **−** No tagged release listed

<sub>GPU optional · [Repo](https://github.com/mlc-ai/mlc-llm) · [📖 Docs ↗](https://llm.mlc.ai/docs/) · [🌐 Site ↗](https://llm.mlc.ai/docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlc-llm/)</sub>

<a name="litert-lm"></a>
### #&#8288;45 [litert-lm](https://github.com/google-ai-edge/litert-lm) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.8k · Apache-2.0 · Oct 2026</sub>

**On-device LLM runtime with CLI and APIs for Android, iOS, web and desktop.**

LiteRT-LM is Google's C++ orchestration layer for running LLMs on top of LiteRT on phones, browsers, desktops and Raspberry Pi. It ships a CLI (run, serve, import, describe) and language bindings, with GPU and NPU acceleration, vision and audio input, and function calling. It powers on-device GenAI in Chrome, Chromebook Plus and Pixel Watch.

- **+** Python, Kotlin and C++ APIs marked stable; Swift, JavaScript and Flutter also available
- **+** Runs on Android, iOS, web, desktop and Raspberry Pi with GPU and NPU backends
- **+** CLI serve exposes an OpenAI-compatible /v1/embeddings endpoint for embedding models
- **+** Supports vision and audio input, function calling and speculative decoding
- **−** Models use the .litertlm format, so other formats likely need conversion
- **−** Swift and JavaScript APIs are early preview; Flutter is community-maintained
- **−** RAM and hardware requirements are not stated in the README
- **−** No Docker image or compose file; source build is a separate guide

<sub>GPU optional · Needs LiteRT, uv (for CLI install) · Models: Gemma, Llama, Phi-4, Qwen, EmbeddingGemma 2 · [Repo](https://github.com/google-ai-edge/litert-lm) · [▶️ Demo ↗](https://google-ai-edge.github.io/LiteRT-LM/web_demos/chat/index.html) · [📖 Docs ↗](https://ai.google.dev/edge/litert-lm/overview) · [🌐 Site ↗](https://ai.google.dev/edge/litert-lm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/litert-lm/)</sub>

<a name="shimmy"></a>
### #&#8288;46 [shimmy](https://github.com/michael-a-kuykendall/shimmy) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Oct 2026</sub>

**OpenAI-compatible inference server for GGUF models, written in Rust on WebGPU.**

Shimmy is a single-binary server that exposes GGUF models through OpenAI-compatible chat completions, text completions, streaming and model endpoints. It runs on Airframe, a pure-Rust WebGPU (WGSL) engine, so it works on NVIDIA, AMD, Intel and Apple GPUs without a C++ toolchain or Python. 26 model/quant combinations across 12 families are certified for math, inference and determinism.

- **+** Pure Rust with WebGPU shaders; no C++ toolchain, Python runtime or backend flags
- **+** Deterministic output for the same model, seed and params
- **+** Runs on NVIDIA, AMD, Intel and Apple Silicon GPUs through one backend
- **+** Optional INT4 KV cache claims about 7x lower KV memory in tested configurations
- **−** v2 removed llama.cpp, MLX and HuggingFace backends; only Airframe remains
- **−** Only 26 certified model/quant combinations; mostly Q4_K_M quants
- **−** SafeTensors native inference and MoE CPU offload are still roadmap items
- **−** README lists MIT while detected license is Apache-2.0; terms need checking

<sub>GPU required · Docker + Compose · Models: GGUF, Llama, Qwen2, Qwen3, Qwen3.5 · port 11435 · [Repo](https://github.com/michael-a-kuykendall/shimmy) · [📖 Docs ↗](https://github.com/Michael-A-Kuykendall/shimmy/blob/main/docs/quickstart.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/shimmy/)</sub>

<a name="bitnet"></a>
### #&#8288;47 [bitnet](https://github.com/microsoft/bitnet) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (87) · Freshness: active (98) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Jul 2026</sub>

**Inference framework for 1.58-bit ternary LLMs on CPU and GPU.**

bitnet.cpp is Microsoft's llama.cpp-based inference framework with optimized I2_S, TL1 and TL2 kernels for ternary BitNet b1.58 models on x86 and ARM CPUs, plus a GPU kernel. It runs GGUF models through Python scripts for setup, chat and benchmarking. The README reports 1.37x to 6.17x CPU speedups over full-precision baselines.

- **+** Reports 2.37x-6.17x speedups on x86 and 1.37x-5.07x on ARM versus full precision
- **+** Runs a 100B BitNet b1.58 model on one CPU at 5-7 tokens per second (per README)
- **+** Supports official 2B-4T and embedding models plus Falcon3, Falcon-E and Llama3-8B ternary variants
- **+** Includes an end-to-end benchmark script and a dummy-model generator
- **−** Only ternary 1-bit models are supported; ordinary GGUF models are out of scope
- **−** No HTTP server or OpenAI-compatible API described; usage is via run_inference.py CLI
- **−** Kernel support is uneven across models; embedding models have no ARM support
- **−** Build needs clang>=18, cmake>=3.22 and Python>=3.10; no Docker or release builds

<sub>GPU optional · Needs python>=3.10, cmake>=3.22, clang>=18, conda, huggingface-cli · Models: BitNet-b1.58-2B-4T, BitNet-embedding-0.6B, BitNet-embedding-270M, bitnet_b1_58-large, bitnet_b1_58-3B · [Repo](https://github.com/microsoft/bitnet) · [▶️ Demo ↗](https://demo-bitnet-h0h8hcfqeqhrf5gf.canadacentral-01.azurewebsites.net/) · [📖 Docs ↗](https://github.com/microsoft/BitNet/blob/main/src/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bitnet/)</sub>

<a name="serving"></a>
### #&#8288;48 [serving](https://github.com/tensorflow/serving) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Oct 2026</sub>

**Inference server for TensorFlow SavedModels with gRPC and REST endpoints.**

TensorFlow Serving loads trained models, manages their versions, and serves them over gRPC and HTTP. It serves multiple models or versions at once, supports canarying and A/B testing, and includes a batching scheduler for joint GPU execution with configurable latency limits. It targets TensorFlow SavedModels but can be extended with custom C++ servables.

- **+** Serves multiple models or versions at once; new versions need no client changes
- **+** Exposes both gRPC and REST predict endpoints
- **+** Batching scheduler groups requests for GPU with configurable latency controls
- **+** Modular C++ design: custom servables and version sources can be added
- **−** Built around TensorFlow SavedModel; other model types need a custom C++ servable
- **−** No LLM-specific features in the README, such as GGUF or an OpenAI-compatible API
- **−** Non-Docker install is marked not recommended in the README
- **−** Extending or building from source requires C++ and a Bazel-based build

<sub>GPU optional · Needs Docker (recommended install) · Models: TensorFlow SavedModel, embeddings, vocabularies, feature transformations · port 8501 · [Repo](https://github.com/tensorflow/serving) · [📖 Docs ↗](https://www.tensorflow.org/tfx/serving/api_docs/cc/) · [🌐 Site ↗](http://tensorflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/serving/)</sub>

<a name="cactus"></a>
### #&#8288;49 [cactus](https://github.com/cactus-compute/cactus) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · custom license · Sep 2026</sub>

**On-device LLM, vision and speech inference engine for phones and wearables.**

Cactus is a C++ inference engine with its own computation graph, ARM/Apple/Android kernels and rotation-based quantization (CQ, 1 to 4 bits). It runs text, vision and speech models on phones, Macs and wearables, and can hand low-confidence queries off to a cloud model. It ships a CLI with an OpenAI-compatible local server (default port 8080) and bindings for Swift, Kotlin, Flutter, React Native, Python and Rust.

- **+** Published benchmarks per device, e.g. Gemma-4-E2B-CQ4 decodes 37 tok/s on iPhone 17 Pro
- **+** Bindings for Swift, Kotlin, Flutter, React Native, Python and Rust for mobile apps
- **+** Quantization accuracy tables across bit widths (CQ4 close to F16 on most listed tasks)
- **+** Confidence-based cloud handoff for hard queries, configurable threshold and timeout
- **−** License is reported as NOASSERTION; terms need checking before commercial use
- **−** Converting arbitrary HuggingFace models is labelled experimental
- **−** Only Liquid, Gemma, Whisper, Parakeet and Qwen families are described as well tested
- **−** Benchmarks cover Apple devices only; no Android or Linux numbers in the README

<sub>GPU optional · Needs HuggingFace (model download/convert), cmake and build-essential (Linux build), Python 3.12 (setup/CLI) · Models: Gemma, Liquid LFM, Qwen, Whisper, Parakeet · port 8080 · [Repo](https://github.com/cactus-compute/cactus) · [📖 Docs ↗](https://cactus-compute.github.io/cactus/) · [🌐 Site ↗](https://cactuscompute.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cactus/)</sub>

<a name="bentoml"></a>
### #&#8288;50 [bentoml](https://github.com/bentoml/bentoml) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (34) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Oct 2026</sub>

**Python library for turning model inference code into batched REST APIs.**

BentoML is a Python library that wraps model inference code in a service class with typed API methods and serves it over HTTP, on port 3000 by default. It packages code, models and dependencies into a Bento artifact and can generate a Docker image from it. Serving features include adaptive batching, multi-model composition and GPU inference.

- **+** Any ML framework or modality works, since the service is plain Python with type hints
- **+** Built-in adaptive batching, worker parallelism and multi-model composition
- **+** bentoml build and containerize generate a reproducible Docker image from one config
- **+** Example repos cover LLMs (vLLM), diffusion, audio, embeddings and vision
- **−** You write the service code yourself; no ready-made model server out of the box
- **−** Requires Python 3.9 or newer
- **−** Collects anonymous usage data by default; opt out via flag or environment variable
- **−** Docker is needed for containerized deploys; no compose file in the repo

<sub>GPU optional · Needs Python 3.9+, Docker (for containerize) · Models: PyTorch, Transformers, vLLM, Stable Diffusion, any Python ML framework · port 3000 · [Repo](https://github.com/bentoml/bentoml) · [📖 Docs ↗](https://docs.bentoml.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bentoml/)</sub>

<a name="openllm"></a>
### #&#8288;51 [OpenLLM](https://github.com/bentoml/openllm) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: popular (51) · Freshness: recent (70) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**CLI that serves open LLMs as OpenAI-compatible APIs with a built-in chat UI.**

OpenLLM starts open-weight LLMs such as Llama, Qwen, Gemma, Phi and DeepSeek with `openllm serve <model>`, exposing an OpenAI-compatible API on port 3000. Models come from a catalog of Bentos in a separate repository, and custom public repositories can be added. It uses vLLM as the inference backend and BentoML for serving, and includes a chat UI at /chat.

- **+** One command, `openllm serve <model>`, starts an OpenAI-compatible server with a /chat web UI
- **+** Catalog lists required GPU memory per model, from 12G to 80Gx16
- **+** Custom models can be added through Bento-based model repositories
- **+** Built on vLLM and BentoML; OpenAI clients and LlamaIndex can call it
- **−** Model weights are not stored; gated models need a Hugging Face token
- **−** Custom model repositories must be public
- **−** Last release was 2025-04-21, well behind recent commits
- **−** Every listed model has a GPU requirement; CPU-only use is not documented

<sub>GPU required · Needs Hugging Face token (gated models), BentoML, vLLM · Models: Llama 3.1/3.2/3.3/4, Qwen2.5, Gemma 2/3, Phi4, Mistral · port 3000 · [Repo](https://github.com/bentoml/openllm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openllm/)</sub>

<a name="tabbyapi"></a>
### #&#8288;52 [TabbyAPI](https://github.com/theroyallab/tabbyapi) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Oct 2026</sub>

**OpenAI-compatible API server for running ExLlamaV3 models.**

TabbyAPI is a FastAPI server that loads and serves LLMs through the ExLlamaV3 backend, exposing an OpenAI-compatible HTTP API. It supports runtime model loading and unloading, HuggingFace downloads, embedding models, constrained output (JSON schema, regex, EBNF), and tool calling. The README describes it as a hobby project for a small user base, not for production servers.

- **+** Continuous batching with paged attention on Nvidia Ampere and newer GPUs
- **+** Speculative decoding with draft models; JSON schema, regex and EBNF constraints
- **+** Load, unload and download models at runtime without restarting the server
- **+** Published Docker images for CUDA 12.8, CUDA 13 and ROCm
- **−** README says it is not meant for production servers
- **−** Only EXL3 and FP16/BF16 models; no GGUF support listed
- **−** Rolling release with no tagged releases; dependencies may need reinstalling
- **−** AGPL-3.0 license may restrict use in some network services

<sub>GPU required · Docker + Compose · Needs ExLlamaV3, NVIDIA container toolkit (Docker) · Models: EXL3, FP16, BF16 · port 5000 · [Repo](https://github.com/theroyallab/tabbyapi) · [📖 Docs ↗](https://theroyallab.github.io/tabbyAPI) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tabbyapi/)</sub>

<a name="text-embeddings-inference"></a>
### #&#8288;53 [Text Embeddings Inference](https://github.com/huggingface/text-embeddings-inference) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: patchy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · Apache-2.0 · Oct 2026</sub>

**Rust server for embedding, reranker and classification models.**

TEI is a Rust server from Hugging Face for embedding, reranker and sequence-classification models (BERT, XLM-RoBERTa, Nomic, Jina, GTE, Qwen3, ModernBERT, Gemma3) with token-based dynamic batching and Flash Attention. The router listens on port 3000 with /embed and OpenAI-compatible routes, gRPC, OpenTelemetry tracing and Prometheus metrics. Images cover CPU x86/arm64 and NVIDIA Turing through Blackwell.

- **+** Token-based dynamic batching with Flash Attention, Candle and cuBLASLt
- **+** Small images and fast boot; no graph compilation step
- **+** Rerankers and classifiers served alongside embeddings
- **+** OpenTelemetry tracing, Prometheus metrics, API key auth, gRPC
- **−** No Volta support; Turing image is experimental with Flash Attention off
- **−** GPU images need drivers compatible with CUDA 12.2 or higher
- **−** Only CamemBERT and XLM-RoBERTa for sequence classification
- **−** 7B embedders such as Qwen3-Embedding-8B are flagged very expensive

<sub>GPU optional · Docker · Models: Qwen3-Embedding, gte-Qwen2, multilingual-e5, embeddinggemma, arctic-embed, nomic-embed, ModernBERT, jina-embeddings-v2, bge-reranker, gte rerankers · port 3000 · [Repo](https://github.com/huggingface/text-embeddings-inference) · [📖 Docs ↗](https://huggingface.github.io/text-embeddings-inference) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/text-embeddings-inference/)</sub>

<a name="nano-vllm"></a>
### #&#8288;54 [nano-vllm](https://github.com/geeeekexplorer/nano-vllm) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (60) · Freshness: recent (65) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Apr 2026</sub>

**Minimal vLLM-style inference engine in about 1,200 lines of Python.**

Nano-vLLM is a from-scratch reimplementation of vLLM for offline batch inference, with an LLM.generate API that mirrors vLLM's. It includes prefix caching, tensor parallelism, Torch compilation and CUDA graphs. The README benchmarks Qwen3-0.6B on an RTX 4070 Laptop (8GB) at 1434 tokens/s against vLLM's 1362 tokens/s.

- **+** Small codebase (~1,200 lines of Python) that is practical to read and modify
- **+** API mirrors vLLM's LLM and SamplingParams interface
- **+** Includes prefix caching, tensor parallelism, Torch compile and CUDA graphs
- **+** README benchmark shows throughput on par with vLLM on one small-model setup
- **−** Offline inference only; README describes no HTTP or OpenAI-compatible server
- **−** Benchmark covers one model and one laptop GPU; broader results are unknown
- **−** README lists only Qwen3-0.6B; other supported architectures are unknown
- **−** No tagged releases; installed directly from the GitHub repository

<sub>Needs Hugging Face model weights · Models: Qwen3-0.6B · [Repo](https://github.com/geeeekexplorer/nano-vllm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nano-vllm/)</sub>

<a name="chatrwkv"></a>
### #&#8288;55 [chatrwkv](https://github.com/blinkdl/chatrwkv) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: known (38) · Freshness: active (95) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · Apache-2.0 · Jul 2026</sub>

**Reference inference code and chat demos for RWKV RNN language models.**

ChatRWKV is the Python reference implementation for running RWKV, an RNN-based language model, as a chatbot. It ships the `rwkv` pip package, a v2 runtime with "stream" and "split" strategies and INT8 (the README says 3 GB VRAM is enough for RWKV 14B), an optional CUDA kernel, and short model files for building your own engine. It is a developer reference rather than a packaged chat app.

- **+** Stream, split and INT8 strategies fit large models into small VRAM
- **+** RNN state lets you carry context forward without re-processing the prompt
- **+** Short readable reference files such as RWKV_in_150_lines.py and src/model_run.py
- **+** Published as the `rwkv` pip package, with links to GGUF and HF-compatible weights
- **−** No built-in web UI or HTTP API; the README points to other projects for those
- **−** Optional CUDA kernel needs a manual build with ninja and a CUDA toolchain
- **−** You must track the text matching the RNN state yourself to avoid bugs
- **−** README is mostly links and older results; much of the work lives in other repos

<sub>GPU optional · Needs PyTorch, ninja (for CUDA kernel), CUDA toolkit (optional) · Models: RWKV-4 Raven, RWKV World (v4/v5/v6), RWKV-7, PyTorch .pth, GGUF (via linked weights) · [Repo](https://github.com/blinkdl/chatrwkv) · [▶️ Demo ↗](https://huggingface.co/spaces/BlinkDL/RWKV-Gradio-1) · [🌐 Site ↗](https://www.rwkv.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatrwkv/)</sub>

<a name="powerinfer"></a>
### #&#8288;56 [powerinfer](https://github.com/tiiny-ai/powerinfer) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (41) · Freshness: recent (70) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · MIT · May 2026</sub>

**CPU/GPU hybrid LLM inference engine exploiting sparse neuron activation.**

PowerInfer is a C++ inference engine, derived from llama.cpp, that keeps frequently activated "hot" neurons on the GPU and computes the rest on the CPU. It runs ReLU-sparse models in a GGUF variant (*.powerinfer.gguf) that bundles predictor weights, and uses --vram-budget in place of -ngl. The README reports up to 11x speedup over llama.cpp on Falcon(ReLU)-40B on one RTX 4090.

- **+** Hot/cold neuron split lets 40B-70B models run on one consumer GPU with CPU offload
- **+** Reports up to 11x over llama.cpp on Falcon-40B (RTX 4090), up to 8x with INT4 on RTX 2080Ti
- **+** Keeps llama.cpp-style examples such as server, batched generation and perplexity
- **+** NVIDIA (CUDA), AMD (ROCm) and CPU-only builds on Linux and Windows
- **−** Only ReLU/ReGLU/Squared ReLU models work; Mistral, original Llama and Qwen are unsupported
- **−** Needs PowerInfer GGUF files with predictor weights; llama.cpp weights give no speedup
- **−** Short model list: Falcon-40B, Llama 2 family, ProSparse Llama 2, Bamboo-7B
- **−** macOS is CPU only with little gain; no tagged release

<sub>GPU optional · Docker · Needs CMake 3.17+, Python 3.8+, pip 19.3+, CUDA or ROCm (for GPU builds) · Models: PowerInfer GGUF, ReluLLaMA 7B/13B/70B, ReluFalcon-40B, ProSparse-LLaMA-2, Bamboo-7B · [Repo](https://github.com/tiiny-ai/powerinfer) · [▶️ Demo ↗](https://powerinfer-gradio.vercel.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/powerinfer/)</sub>

<a name="gemma-cpp"></a>
### #&#8288;57 [gemma.cpp](https://github.com/google/gemma.cpp) <sub>score [8](../README.md#-how-we-rank "Score 8/100. Adoption: niche (19) · Freshness: quiet (0) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2025</sub>

**Minimal C++ CPU inference engine for Gemma 2, Gemma 3 and PaliGemma 2.**

gemma.cpp runs Gemma 2, Gemma 3 and PaliGemma 2 models on CPU using Google Highway portable SIMD. It has a ~2K LoC core and ships an interactive terminal app, C++ APIs with streaming and batching, and basic Python bindings. It targets research and experimentation rather than production deployment, and the README points to JAX, Keras, PyTorch or Transformers for that.

- **+** Small codebase (~2K LoC core, ~4K LoC utilities), easy to read and modify
- **+** Compressed weights: 8-bit switched floating point, bf16, f32 and non-uniform 4-bit
- **+** Embeds as a library via CMake FetchContent with few dependencies
- **+** Includes backward pass (VJP) and Adam optimizer for Gemma research
- **−** CPU-only inference; no GPU support
- **−** Supports only Gemma 2, Gemma 3 and PaliGemma 2 models
- **−** No HTTP server; frontends are a terminal app, C++ API and basic Python bindings
- **−** Weights need Kaggle download with consent form; Safetensors converter not open sourced

<sub>no GPU · Needs CMake, Clang (C++17), Google Highway, SentencePiece · Models: Gemma 2, Gemma 3, PaliGemma 2, .sbs compressed weights · [Repo](https://github.com/google/gemma.cpp) · [📖 Docs ↗](https://github.com/google/gemma.cpp/blob/main/DEVELOPERS.md) · [🌐 Site ↗](https://ai.google.dev/gemma) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gemma-cpp/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
