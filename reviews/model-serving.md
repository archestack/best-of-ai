# 🧠 Model serving reviews · Best of Open-Source AI

Inference engines and model servers that expose local models over an API. Back to the [leaderboard](../README.md#-model-serving).

<sub>🌐 Also on the web: [Model serving on archestack.com](https://archestack.com/best-of-ai/model-serving/), each project on its own page.</sub>

<a name="llama-cpp"></a>
### 🥇 [llama.cpp](https://github.com/ggml-org/llama.cpp) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 135k · MIT · Nov 2026</sub>

**C/C++ inference engine for GGUF LLMs and VLMs with an OpenAI-compatible server.**

llama.cpp runs quantized LLMs and vision-language models on CPUs and GPUs from a plain C/C++ codebase built on ggml. It ships a CLI (`llama cli`) and an OpenAI-compatible HTTP server (`llama serve`) with a built-in web UI, and can pull models directly from Hugging Face. Backends cover CUDA, HIP, Metal, Vulkan, SYCL, CANN, OpenCL and others, with CPU+GPU hybrid offload for models larger than VRAM.

- **+** Many backends: CUDA, HIP, Metal, Vulkan, SYCL, CANN, MUSA, OpenCL, RPC, WebGPU
- **+** 1.5-bit to 8-bit integer quantization reduces memory use
- **+** CPU+GPU hybrid inference for models larger than VRAM
- **+** No dependencies in the core; prebuilt binaries, Docker and winget available
- **−** OpenVINO backend is marked in progress
- **−** Building from source needs backend-specific toolchains such as CUDA or Vulkan SDKs
- **−** Built-in web UI is minimal next to dedicated chat front-ends
- **−** Interfaces are CLI and C API; no managed model library in the README

<sub>GPU optional · Docker · Models: GGUF, LLM, VLM, Hugging Face download · [Repo](https://github.com/ggml-org/llama.cpp) · [📖 Docs ↗](https://github.com/ggml-org/llama.cpp/blob/master/docs/build.md) · [🌐 Site ↗](https://llama.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llama-cpp/)</sub>

<a name="ollama"></a>
### 🥈 [Ollama](https://github.com/ollama/ollama) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 187k · MIT · Nov 2026</sub>

**Runs open models locally through a CLI and REST API.**

Ollama downloads and runs open models locally or in the cloud through a CLI (`ollama run gemma4`) and a REST API on localhost:11434. It is written in Go, lists llama.cpp as its backend, and ships official Python and JavaScript client libraries. `ollama launch` can also connect it to tools such as Claude Code, Codex, OpenCode and OpenClaw.

- **+** Installs via shell script, manual download on macOS/Windows, or the ollama/ollama Docker image
- **+** REST API with a chat endpoint plus official ollama-python and ollama-js libraries
- **+** `ollama launch` connects it to coding agents and the OpenClaw assistant
- **+** Large list of community integrations: chat UIs, RAG tools, SDKs, observability
- **−** Only llama.cpp is listed as a supported backend
- **−** Models come from the ollama.com library; custom ones need import via Modelfile
- **−** Cloud option is mentioned, but its limits and pricing are not covered in the README
- **−** No built-in web chat UI described; front-ends are third-party projects

<sub>Docker · Models: Gemma 4, llama.cpp backend, Modelfile import · port 11434 · [Repo](https://github.com/ollama/ollama) · [📖 Docs ↗](https://docs.ollama.com) · [🌐 Site ↗](https://ollama.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ollama/)</sub>

<a name="localai"></a>
### 🥉 [LocalAI](https://github.com/mudler/localai) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Nov 2026</sub>

**Self-hosted model server with OpenAI, Anthropic and ElevenLabs-compatible APIs.**

LocalAI is a Go server that runs LLMs, vision, speech, image and video models behind OpenAI-, Anthropic- and ElevenLabs-compatible HTTP APIs. Each of its 60+ backends (llama.cpp, vLLM, whisper.cpp, diffusers, MLX and others) ships as a separate OCI image, pulled when a model needs it. It also has a web UI, API key auth with quotas, MCP support and an optional distributed mode on PostgreSQL and NATS.

- **+** Covers text, vision, speech, image and video models behind one API
- **+** Backends install on demand as OCI images, so unused engines are not pulled
- **+** Runs on CPU, NVIDIA CUDA 12/13, AMD ROCm, Intel oneAPI, Vulkan, Apple Silicon
- **+** Multi-user auth with API keys, quotas and roles; distributed mode for scaling out
- **−** Distributed mode requires running PostgreSQL and NATS alongside the server
- **−** Broad scope: 60+ backends and frequent releases to keep up with
- **−** macOS DMG is not signed by Apple and needs a manual quarantine removal
- **−** vllm.cpp backend is described as alpha development builds

<sub>GPU optional · Docker + Compose · Needs PostgreSQL and NATS (distributed mode only) · Models: GGUF, safetensors, Hugging Face, Ollama OCI registry, OCI images · port 8080 · [Repo](https://github.com/mudler/localai) · [📖 Docs ↗](https://localai.io/basics/getting_started/) · [🌐 Site ↗](https://localai.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/localai/)</sub>

<a name="vllm"></a>
### #&#8288;4 [vLLM](https://github.com/vllm-project/vllm) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 97k · Apache-2.0 · Nov 2026</sub>

**Inference engine serving LLMs with PagedAttention and an OpenAI-compatible API.**

vLLM is a Python library and server for LLM inference. It manages attention KV memory with PagedAttention, batches requests continuously, and exposes an OpenAI-compatible API, plus Anthropic Messages API and gRPC. It runs 200+ Hugging Face model architectures on NVIDIA, AMD and Intel GPUs, several CPU types, and hardware plugins such as TPUs and Gaudi.

- **+** Continuous batching, chunked prefill, prefix caching and speculative decoding (n-gram, EAGLE and others)
- **+** Tensor, pipeline, data, expert and context parallelism for multi-GPU serving
- **+** Many quantization formats: FP8, NVFP4, INT4, GPTQ/AWQ, GGUF and more
- **+** Wide hardware coverage: NVIDIA, AMD, Intel GPUs, x86/ARM/PowerPC CPUs, plus plugins
- **−** Aimed at server-scale deployments; distributed features need tuning knowledge
- **−** TPU, Gaudi, Ascend and other hardware run through separate plugins
- **−** No built-in chat UI or user management; API server only
- **−** Install has an extra step to download precompiled kernels

<sub>GPU optional · Docker · Models: Hugging Face models, Llama, Qwen, Gemma, Mixtral · [Repo](https://github.com/vllm-project/vllm) · [📖 Docs ↗](https://docs.vllm.ai) · [🌐 Site ↗](https://vllm.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vllm/)</sub>

<a name="strata"></a>
### #&#8288;5 [strata](https://github.com/niko1221/strata) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · MIT · Nov 2026</sub>

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

<a name="llmfit"></a>
### #&#8288;6 [llmfit](https://github.com/alexsjones/llmfit) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · MIT · Nov 2026</sub>

**Terminal tool that checks which LLMs and quantizations fit your hardware.**

llmfit detects CPU, RAM, GPU and VRAM (CUDA, ROCm, Apple Silicon, Intel oneAPI), then scores a catalog of models on memory fit, estimated speed, quality and context. It ships a TUI, a CLI with JSON output, and an HTTP server with a web dashboard and REST API. It estimates rather than serves models, and can measure real tok/s against a running provider.

- **+** Detects NVIDIA, AMD, Apple Silicon and Intel accelerators, including multi-GPU and unified memory
- **+** Handles MoE models and GGUF, AWQ, GPTQ and EXL2 quantizations in estimates
- **+** JSON CLI output and REST endpoints (/api/v1/system, /api/v1/models) suit scripts and pipelines
- **+** Installs via winget, Scoop, Homebrew, MacPorts, uv or cargo; ships a multi-arch Docker image
- **−** Speed and memory figures are estimates unless you benchmark on your own hardware
- **−** Cluster mode for Ray is a preview, tested only against a mock dashboard
- **−** Recommends models but does not serve them for inference
- **−** Model catalog is built in; unlisted models need a custom entry

<sub>GPU optional · Docker · Needs Ollama (optional), llama.cpp (optional), MLX (optional), LM Studio (optional), Docker Model Runner (optional) · Models: GGUF, AWQ, GPTQ, EXL2 · port 8787 · [Repo](https://github.com/alexsjones/llmfit) · [📖 Docs ↗](https://github.com/AlexsJones/llmfit/blob/main/docs/cli.md) · [🌐 Site ↗](https://llmfit.axjns.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llmfit/)</sub>

<a name="modular"></a>
### #&#8288;7 [modular](https://github.com/modular/modular) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Nov 2026</sub>

**Mojo language and MAX inference framework with an OpenAI-compatible server.**

Monorepo for the open-source parts of the Modular Platform: the Mojo compiler and standard library, plus MAX, which includes a graph compiler, runtime, Mojo GPU kernels, Python model authoring and prebuilt model pipelines. MAX serves models through an OpenAI-compatible endpoint. Running from the repo uses Bazel via ./bazelw.

- **+** Includes an OpenAI-compatible inference server under max/python/max/serve
- **+** Open Mojo compute kernels and GPU programming abstractions, source available since May 2025
- **+** Models can be authored in Python on the MAX framework, with ready-made pipelines
- **+** Mojo compiler and standard library source are included
- **−** Mixed licensing: parts of MAX source and binaries fall under a separate MAX license
- **−** Only some components are open source; more are being released over time
- **−** The example text generation command requires a compatible GPU
- **−** Repo workflow depends on Bazel and the Mojo language, unlike typical Python servers

<sub>GPU required · Needs Bazel (via ./bazelw) · Models: Hugging Face models (e.g. Qwen/Qwen3.5-0.8B) · [Repo](https://github.com/modular/modular) · [📖 Docs ↗](https://max.modular.com/) · [🌐 Site ↗](https://www.modular.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/modular/)</sub>

<a name="colibri"></a>
### #&#8288;8 [colibri](https://github.com/justvugg/colibri) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · Apache-2.0 · Oct 2026</sub>

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

<a name="sglang"></a>
### #&#8288;9 [SGLang](https://github.com/sgl-project/sglang) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;10 [tensorrt-llm](https://github.com/nvidia/tensorrt-llm) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (70) · Freshness: active (98) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · Nov 2026</sub>

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
### #&#8288;11 [lmcache](https://github.com/lmcache/lmcache) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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

<a name="xinference"></a>
### #&#8288;12 [Xinference](https://github.com/xorbitsai/inference) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.7k · Apache-2.0 · Nov 2026</sub>

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

<a name="omlx"></a>
### #&#8288;13 [omlx](https://github.com/jundot/omlx) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Nov 2026</sub>

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

<a name="freetoken"></a>
### #&#8288;14 [freetoken](https://github.com/flashml-org/freetoken) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

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

<a name="airllm"></a>
### #&#8288;15 [airllm](https://github.com/lyogavin/airllm) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · Apache-2.0 · Nov 2026</sub>

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

<a name="web-llm"></a>
### #&#8288;16 [web-llm](https://github.com/mlc-ai/web-llm) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;17 [dynamo](https://github.com/ai-dynamo/dynamo) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · custom license · Nov 2026</sub>

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

<a name="magnitude"></a>
### #&#8288;18 [magnitude](https://github.com/magnitudedev/magnitude) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · Apache-2.0 · Nov 2026</sub>

**Local inference engine that tunes kernels per model on your hardware.**

Magnitude is a desktop app and CLI inference engine that runs open-weight models on Apple Silicon, NVIDIA, AMD or CPU. When a model is downloaded it spends up to a minute tuning kernels on the local chip, and ships a speculative decoding drafter per model. It connects to agents such as Pi, OpenCode, Codex, Claude Code and Cline, or any client through an OpenAI-compatible API.

- **+** Per-model kernel tuning at download time; README reports ~2.2x faster decode than Ollama on Mac and NVIDIA
- **+** Runs on Apple Silicon, NVIDIA, AMD or CPU across macOS, Windows and Linux
- **+** One-click connection to eight named agents; OpenAI-compatible API for the rest
- **+** `magnitude server setup` installs a self-updating boot service for remote use
- **−** Optimized kernels cover popular open-weight families only; full model list is on the website
- **−** Benchmarks are the project's own and compare mainly against Ollama
- **−** No Docker or compose setup mentioned in the README

<sub>GPU optional · Models: Open-weight LLM families listed at magnitude.dev/models, OpenAI-compatible API · [Repo](https://github.com/magnitudedev/magnitude) · [📖 Docs ↗](https://docs.magnitude.dev) · [🌐 Site ↗](https://magnitude.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/magnitude/)</sub>

<a name="vllm-omni"></a>
### #&#8288;19 [vllm-omni](https://github.com/vllm-project/vllm-omni) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · Apache-2.0 · Nov 2026</sub>

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

<a name="ktransformers"></a>
### #&#8288;20 [KTransformers](https://github.com/kvcache-ai/ktransformers) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Nov 2026</sub>

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

<a name="cog"></a>
### #&#8288;21 [cog](https://github.com/replicate/cog) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · Apache-2.0 · Oct 2026</sub>

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

<a name="mlx-lm"></a>
### #&#8288;22 [mlx-lm](https://github.com/ml-explore/mlx-lm) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · MIT · Nov 2026</sub>

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

<a name="exo"></a>
### #&#8288;23 [exo](https://github.com/exo-explore/exo) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (93) · Freshness: active (98) · Maintenance: patchy (39) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · Apache-2.0 · Nov 2026</sub>

**Pools Macs and other devices into one cluster to run large models.**

exo discovers devices on the same network and splits a model across them using topology-aware parallelism, so models too large for one machine can run. It uses MLX for inference and MLX distributed for communication, with optional RDMA over Thunderbolt 5 on macOS 26.2 or later. It exposes OpenAI Chat Completions, Claude Messages, OpenAI Responses and Ollama-compatible APIs plus a built-in dashboard.

- **+** Automatic device discovery, no manual cluster configuration
- **+** Tensor parallelism: up to 1.8x on 2 devices, 3.2x on 4 devices
- **+** Serves OpenAI, Claude Messages, Responses and Ollama-style APIs from one endpoint
- **+** Ships a macOS menu bar app and a built-in dashboard with chat
- **−** On Linux it currently runs on CPU only; GPU support is under development
- **−** All devices must run the same exo version and build, or they do not join
- **−** RDMA needs Thunderbolt 5 Macs, macOS 26.2+, Recovery-mode setup and full-mesh cabling
- **−** Source install needs Xcode, Rust, Node and uv; no Docker image provided

<sub>GPU optional · Needs MLX, uv, Node.js, Rust, Xcode (macOS source build) · Models: MLX, HuggingFace hub custom models · port 52415 · [Repo](https://github.com/exo-explore/exo) · [📖 Docs ↗](https://github.com/exo-explore/exo/blob/main/docs/api.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/exo/)</sub>

<a name="edge0"></a>
### #&#8288;24 [edge0](https://github.com/edge0-ai/edge0) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

**Streaming MoE inference that serves 35B models from SSD on Apple Silicon.**

edge0 streams mixture-of-experts weights from SSD on demand, so peak memory tracks the active expert set rather than total parameters. It pairs int4 checkpoints with Recover-LoRA adapters and a trained prerouter that predicts expert routing one step ahead. The Python/MLX framework runs on Apple Silicon and serves an OpenAI-compatible /v1/chat/completions endpoint; macOS, iOS, Android and Windows engines live in the same repo.

- **+** Reported 2.9 GiB peak MLX allocator memory for the 35B tier on a Mac mini M4 Pro
- **+** Ships trained LoRA and prerouter adapters with the checkpoints, ready to serve
- **+** Separate engines for macOS (Rust), iOS (Swift), Android (Kotlin) and Windows (C++/Vulkan)
- **+** Self-run OpenCompass results: int4 averages 3.9 points below fp16 for the 35B tier
- **−** Python framework supports only macOS on Apple Silicon; CUDA backend is roadmap only
- **−** Decode speed is 14.9-17.7 tok/s for the 35B tier, 23.9-25.3 for the 8B
- **−** Only two preview model tiers, built on Qwen3.6-35B-A3B and Ling 3.0
- **−** Unified cross-platform framework is unreleased; platform engines use separate stacks

<sub>GPU required · Needs MLX 0.30.6, mlx-lm 0.31.0, Python 3.10+ · Models: Edge0-35B-A3B-preview, Edge0-8B-A1B-preview, int4 safetensors · port 8000 · [Repo](https://github.com/edge0-ai/edge0) · [🌐 Site ↗](https://edge0.ai/discord) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/edge0/)</sub>

<a name="apfel"></a>
### #&#8288;25 [apfel](https://github.com/arthur-ficial/apfel) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · MIT · Nov 2026</sub>

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

<a name="openvino"></a>
### #&#8288;26 [openvino](https://github.com/openvinotoolkit/openvino) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="triton-inference-server"></a>
### #&#8288;27 [Triton Inference Server](https://github.com/triton-inference-server/server) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · BSD-3-Clause · Nov 2026</sub>

**Multi-framework inference server with dynamic batching and HTTP/gRPC APIs.**

Triton Inference Server serves models from TensorRT, PyTorch, ONNX Runtime, OpenVINO, Python and RAPIDS FIL backends from a single model repository. It exposes KServe-style HTTP/REST and gRPC endpoints, plus a C API and Java API for in-process use. Scheduling features include dynamic and sequence batching, concurrent model execution, ensembles and Business Logic Scripting.

- **+** Backends for TensorRT, PyTorch, ONNX, OpenVINO, Python and RAPIDS FIL in one server
- **+** Dynamic batching, sequence batching and concurrent model execution built in
- **+** HTTP/REST and gRPC based on the KServe v2 protocol, plus in-process C and Java APIs
- **+** Runs on NVIDIA GPUs, x86 and ARM CPUs, and AWS Inferentia; exposes metrics
- **−** Backend support varies by platform; a support matrix must be checked
- **−** Needs model repository layout and per-model configuration, more setup than simple LLM servers
- **−** Recommended install is the large NGC container; non-Docker builds are documented separately
- **−** Main branch is under development; releases track NGC container versions

<sub>GPU optional · Docker · Needs Docker, NVIDIA Container Toolkit · Models: TensorRT, PyTorch, ONNX, OpenVINO, Python · [Repo](https://github.com/triton-inference-server/server) · [📖 Docs ↗](https://github.com/triton-inference-server/server/blob/main/docs/README.md) · [🌐 Site ↗](https://developer.nvidia.com/nvidia-triton-inference-server) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/triton-inference-server/)</sub>

<a name="geniex"></a>
### #&#8288;28 [geniex](https://github.com/qualcomm/geniex) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · BSD-3-Clause · Nov 2026</sub>

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
### #&#8288;29 [mistral.rs](https://github.com/ericlbuehler/mistral.rs) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (47) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · MIT · Nov 2026</sub>

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
### #&#8288;30 [mooncake](https://github.com/kvcache-ai/mooncake) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · Apache-2.0 · Nov 2026</sub>

**KV cache transfer engine and distributed cache store for LLM inference clusters.**

Mooncake is the serving platform behind Kimi, built around a KV cache-centric split of prefill and decode clusters. It provides a Transfer Engine for batched data movement over RDMA, TCP, NVLink, EFA and other transports, plus Mooncake Store, a distributed KV cache and weight store spanning DRAM and SSD. It is integrated into SGLang, vLLM, TensorRT-LLM, LMDeploy and others.

- **+** Transfer Engine reports up to 190 GB/s on 8x400 Gbps RoCE, about 4.6x faster than TCP
- **+** Integrated upstream in SGLang, vLLM, TensorRT-LLM, LMDeploy, NIXL and vLLM-Ascend
- **+** Mooncake Store pools KV cache across DRAM and SSD/NVMe with replication and eviction
- **+** Separate PyPI wheels for CUDA, ROCm, NPU, MUSA, EFA and non-CUDA builds
- **−** Infrastructure component, not a standalone server; needs a serving engine such as vLLM or SGLang
- **−** Reported bandwidth figures assume RDMA NICs and multi-node GPU clusters
- **−** Several wheel variants by CUDA version make installation choice non-trivial

<sub>GPU optional · Docker · Needs RDMA NICs (for high-bandwidth transport), SGLang or vLLM (integration) · Models: LLMs via SGLang, vLLM, TensorRT-LLM, LMDeploy integrations · [Repo](https://github.com/kvcache-ai/mooncake) · [📖 Docs ↗](https://kvcache-ai.github.io/Mooncake/) · [🌐 Site ↗](https://kvcache.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mooncake/)</sub>

<a name="llamafile"></a>
### #&#8288;31 [llamafile](https://github.com/mozilla-ai/llamafile) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · custom license · Nov 2026</sub>

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

<a name="llama-swap"></a>
### #&#8288;32 [llama-swap](https://github.com/mostlygeek/llama-swap) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Nov 2026</sub>

**Go proxy that starts and swaps local model servers per request.**

llama-swap is a single Go binary that reads the `model` field of incoming OpenAI- or Anthropic-style requests and starts the matching upstream server from a YAML config, stopping the previous one. It works with llama.cpp and forks, vllm, stable-diffusion.cpp, audio.cpp and ComfyUI. A `matrix` option allows concurrent models, and a built-in web UI offers a playground, logs and manual load/unload.

- **+** One binary and one YAML file; no external dependencies
- **+** Covers chat, embeddings, rerank, audio, image and Anthropic messages endpoints
- **+** Per-model ttl auto-unload, API keys, Prometheus /metrics and log streaming endpoints
- **+** Upstream servers can be upgraded independently since each model is just a cmd
- **−** Does not run inference itself; needs separate upstream servers like llama-server
- **−** Python servers like vllm are recommended to run in Docker or Podman for clean shutdown
- **−** Default mode holds one model at a time; concurrency needs matrix DSL setup
- **−** Swapping means a full model reload, adding latency on the first request after a switch

<sub>GPU optional · Docker · Needs llama-server or another OpenAI-compatible inference server · Models: GGUF via llama.cpp, vllm, stable-diffusion.cpp, whisper.cpp, audio.cpp · port 8080 · [Repo](https://github.com/mostlygeek/llama-swap) · [📖 Docs ↗](https://github.com/mostlygeek/llama-swap/tree/main/docs/kb) · [🌐 Site ↗](https://llama-swap.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llama-swap/)</sub>

<a name="kimi-k3-in-c"></a>
### #&#8288;33 [kimi-k3-in-c](https://github.com/fareedkhan-dev/kimi-k3-in-c) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Oct 2026</sub>

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

<a name="turbo-fieldfare"></a>
### #&#8288;34 [turbo-fieldfare](https://github.com/drumih/turbo-fieldfare) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;35 [kserve](https://github.com/kserve/kserve) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="gpustack"></a>
### #&#8288;36 [GPUStack](https://github.com/gpustack/gpustack) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Nov 2026</sub>

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

<a name="rapid-mlx"></a>
### #&#8288;37 [rapid-mlx](https://github.com/raullenchai/rapid-mlx) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · custom license · Nov 2026</sub>

**MLX-based LLM inference server for Apple Silicon with coding-agent tool calling.**

Rapid-MLX serves MLX models on Apple Silicon over OpenAI-compatible (/v1/chat/completions, /v1/responses) and Anthropic Messages (/v1/messages) APIs. It uses continuous batching, a radix prefix cache and 27 tool-call parser modules, and `rapid-mlx launch <agent>` configures Codex, Claude Code, OpenCode and others against a local model. It also serves image generation and editing models through an Images API.

- **+** OpenAI and Anthropic-compatible endpoints, so most local-endpoint clients work without an adapter
- **+** `rapid-mlx launch <agent>` sets up a private profile without editing existing agent settings
- **+** 27 tool-call parser modules with auto-detect fallback, aimed at coding agents
- **+** README benchmarks show higher decode tok/s than oMLX and LM Studio (single run, vendor-measured)
- **−** Apple Silicon only; Windows and Linux desktop builds are not available
- **−** Speed comparisons are the project's own, single run per engine
- **−** License is reported as NOASSERTION by detection, although the README badge says Apache 2.0
- **−** Audio (TTS, STT) and embeddings need opt-in extras beyond the base install

<sub>RAM ≥ 8 GB · GPU required · Needs Homebrew or uv/pip for install, Apple Silicon Mac, MLX · Models: MLX 4-bit LLMs (Qwen3.5, Qwen3.6, LFM2.5), vision models, image generation (FLUX, SDXL, Qwen Image), video generation, TTS/STT (extra) · port 8000 · [Repo](https://github.com/raullenchai/rapid-mlx) · [📖 Docs ↗](https://rapidmlx.com/docs/) · [🌐 Site ↗](https://rapidmlx.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rapid-mlx/)</sub>

<a name="laya-mlx"></a>
### #&#8288;38 [laya-mlx](https://github.com/mizorewww/laya-mlx) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

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

<a name="cactus"></a>
### #&#8288;39 [cactus](https://github.com/cactus-compute/cactus) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Nov 2026</sub>

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

<a name="lemonade"></a>
### #&#8288;40 [Lemonade](https://github.com/lemonade-sdk/lemonade) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Nov 2026</sub>

**Local multi-modal AI server with OpenAI, Anthropic and Ollama APIs.**

Lemonade is a C++ local inference server that exposes text generation, speech-to-text, text-to-speech and image generation through OpenAI-, Anthropic- and Ollama-compatible APIs. It wraps several engines (llama.cpp, FastFlowLM, Ryzen AI, whisper.cpp, stable-diffusion.cpp, Kokoro) across CPU, GPU and XDNA2 NPU, with AMD-focused optimizations. It also ships a CLI, a Model Manager and an embeddable binary for bundling into other apps.

- **+** Covers text, speech, TTS and image generation behind one server
- **+** Backends for AMD XDNA2 NPU, ROCm, Vulkan, CUDA and Apple Metal
- **+** OpenAI, Anthropic and Ollama API compatibility, so existing apps connect
- **+** Packages for Windows, macOS, Ubuntu, Debian, Fedora, Arch, Snap and Docker
- **−** Many backends are marked experimental or guest, mostly AMD Strix Halo on Linux
- **−** NPU paths need XDNA2 hardware; ryzenai-llm NPU backend is Windows only
- **−** Cloud offload to external providers is labelled experimental
- **−** Several TTS and audio backends have no macOS support

<sub>GPU optional · Docker · Models: GGUF, ONNX, FLM, Whisper, Stable Diffusion · [Repo](https://github.com/lemonade-sdk/lemonade) · [📖 Docs ↗](https://github.com/lemonade-sdk/lemonade/blob/main/docs/README.md) · [🌐 Site ↗](https://lemonade-server.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lemonade/)</sub>

<a name="llama-cpp-python"></a>
### #&#8288;41 [llama-cpp-python](https://github.com/abetlen/llama-cpp-python) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Nov 2026</sub>

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

<a name="lmdeploy"></a>
### #&#8288;42 [LMDeploy](https://github.com/internlm/lmdeploy) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (49) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · Apache-2.0 · Nov 2026</sub>

**LLM and VLM inference server with quantization, TurboMind and PyTorch engines.**

LMDeploy compresses, deploys and serves LLMs and vision-language models through two engines: TurboMind (CUDA-kernel focused) and a pure-Python PyTorch engine. It offers an offline pipeline API, an API server, a proxy server for multi-model and multi-machine setups, and AWQ, weight-only and KV cache quantization. Installed via pip on Python 3.10 to 3.13.

- **+** Two engines: TurboMind for throughput, pure-Python PyTorch engine for easier extension
- **+** Supports 4-bit AWQ, weight-only and int8/int4 KV cache quantization, usable together with prefix caching
- **+** Proxy server distributes requests across multiple models, machines and GPUs
- **+** Broad model list including DeepSeek, Qwen3, gpt-oss, InternVL; Huawei Ascend supported via PyTorch engine
- **−** Supported models and data types differ per engine; must check a table to pick one
- **−** Throughput claims (1.8x vLLM) come from older benchmarks and are not re-verified here
- **−** Default wheels target CUDA 12.8; other platforms need extra setup

<sub>GPU required · Docker · Needs Python 3.10-3.13, CUDA 12.8 (default wheels) · Models: Llama, Qwen, InternLM, InternVL, DeepSeek · [Repo](https://github.com/internlm/lmdeploy) · [📖 Docs ↗](https://lmdeploy.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmdeploy/)</sub>

<a name="libretranslate"></a>
### #&#8288;43 [libretranslate](https://github.com/libretranslate/libretranslate) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: patchy (41) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · AGPL-3.0 · Nov 2026</sub>

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

<a name="litert-lm"></a>
### #&#8288;44 [litert-lm](https://github.com/google-ai-edge/litert-lm) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Nov 2026</sub>

**On-device LLM runtime with CLI and APIs for Android, iOS, web and desktop.**

LiteRT-LM is Google's C++ orchestration layer for running LLMs on top of LiteRT on phones, browsers, desktops and Raspberry Pi. It ships a CLI (run, serve, import, describe) and language bindings, with GPU and NPU acceleration, vision and audio input, and function calling. It powers on-device GenAI in Chrome, Chromebook Plus and Pixel Watch.

- **+** Python, Kotlin and C++ APIs marked stable; Swift, JavaScript and Flutter also available
- **+** Runs on Android, iOS, web, desktop and Raspberry Pi with GPU and NPU backends
- **+** CLI serve exposes an OpenAI-compatible /v1/embeddings endpoint for embedding models
- **+** Supports vision and audio input, function calling and speculative decoding
- **−** Models use the .litertlm format, so other formats likely need conversion
- **−** Swift and JavaScript APIs are early preview; Flutter is community-maintained
- **−** No Docker image or compose file; source build is a separate guide

<sub>GPU optional · Needs LiteRT, uv (for CLI install) · Models: Gemma, Llama, Phi-4, Qwen, EmbeddingGemma 2 · [Repo](https://github.com/google-ai-edge/litert-lm) · [▶️ Demo ↗](https://google-ai-edge.github.io/LiteRT-LM/web_demos/chat/index.html) · [📖 Docs ↗](https://ai.google.dev/edge/litert-lm/overview) · [🌐 Site ↗](https://ai.google.dev/edge/litert-lm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/litert-lm/)</sub>

<a name="ds4"></a>
### #&#8288;45 [ds4](https://github.com/antirez/ds4) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Nov 2026</sub>

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

<a name="tensorrt"></a>
### #&#8288;46 [tensorrt](https://github.com/nvidia/tensorrt) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

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

<a name="shimmy"></a>
### #&#8288;47 [shimmy](https://github.com/michael-a-kuykendall/shimmy) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · Apache-2.0 · Nov 2026</sub>

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

<a name="mlx-vlm"></a>
### #&#8288;48 [mlx-vlm](https://github.com/neywa-labs/mlx-vlm) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (30) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · MIT · Nov 2026</sub>

**Run and fine-tune vision, audio and text models on Apple Silicon with MLX.**

MLX-VLM is a Python package that runs multimodal models (text, image, video, audio in) on Macs via MLX. It provides a CLI (mlx_vlm.generate), a Python API, a Gradio chat UI, and a FastAPI server with continuous batching, prefix caching and KV cache quantization. It also supports speculative decoding with DFlash, MTP and EAGLE-3 drafters, model conversion and quantization, and fine-tuning.

- **+** Covers many model families with per-model docs, including OCR, Gemma 4, MiniCPM-o and Qwen VL
- **+** Speculative decoding with DFlash, MTP and EAGLE-3 drafters; README reports up to 3.94x on Gemma 4 26B-A4B
- **+** Server adds continuous batching, automatic prefix caching and KV cache quantization
- **+** Includes mlx_vlm.convert for quantizing Hugging Face models, plus a fine-tuning section
- **−** Targets macOS on Apple silicon; the only CUDA mention is activation quantization
- **−** Gradio chat UI needs the separate mlx-vlm[ui] extra
- **−** DSpark speculative decoding requires greedy sampling (temperature=0)
- **−** No Docker or compose files provided

<sub>GPU required · Needs MLX, Hugging Face model hub · Models: MLX, Hugging Face safetensors (converted via mlx_vlm.convert), Qwen2-VL, Qwen3.5, Gemma 4 · [Repo](https://github.com/neywa-labs/mlx-vlm) · [📖 Docs ↗](https://neywa-labs.github.io/mlx-vlm/) · [🌐 Site ↗](https://runnativ.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlx-vlm/)</sub>

<a name="serving"></a>
### #&#8288;49 [serving](https://github.com/tensorflow/serving) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="llm-d"></a>
### #&#8288;50 [llm-d](https://github.com/llm-d/llm-d) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

**Kubernetes stack for distributed LLM inference on top of vLLM and SGLang.**

llm-d sits above model servers such as vLLM and SGLang and adds prefix-cache and load-aware routing, tiered KV-cache offload to CPU or disk, and prefill/decode disaggregation with wide expert-parallelism. It also covers multi-tenant flow control, session-aware routing for agents, OpenAI-compatible batch APIs and SLO-aware autoscaling. It deploys through benchmarked Helm-chart guides and is a CNCF sandbox project.

- **+** Prefix-cache-aware routing reported at 3x output throughput versus round-robin on Llama 3.1 70B
- **+** Supports NVIDIA, AMD and Intel GPUs and Google TPUs, with vLLM and SGLang backends
- **+** Prefill/decode disaggregation and tiered KV offload for large models like gpt-oss-120b
- **+** Tested Helm-chart guides with reproducible benchmarks published on Prism
- **−** Requires a Kubernetes cluster; not a single-node or laptop server
- **−** Needs a separate model server (vLLM or SGLang) underneath
- **−** Predicted-latency scheduling is described as experimental in the README
- **−** Many components (router, flow control, KV indexing) add operational overhead for small deployments

<sub>GPU required · Docker · Needs Kubernetes, vLLM or SGLang, Helm · Models: DeepSeek-V4, Kimi K3, gpt-oss-120b, Llama 3.3 70B, Llama 3.1 70B · [Repo](https://github.com/llm-d/llm-d) · [📖 Docs ↗](https://llm-d.ai/docs/getting-started/quickstart) · [🌐 Site ↗](https://www.llm-d.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-d/)</sub>

<a name="mesh-llm"></a>
### #&#8288;51 [mesh-llm](https://github.com/mesh-llm/mesh-llm) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · Apache-2.0 · Nov 2026</sub>

**Pools GPUs across machines behind one OpenAI-compatible API.**

Mesh LLM joins machines into a mesh and serves GGUF models through a single OpenAI-compatible API on port 9337. Requests route by the model field to a peer that can serve it. Models too large for one node are split by layer across nodes using the Skippy runtime, a patched llama.cpp. Peer traffic is encrypted over QUIC, and a web console runs on port 3131.

- **+** Splits models too large for one machine into layer stages across peers
- **+** Same /v1 endpoint on every node, routed by model name
- **+** Prebuilt bundles for macOS Metal, plus Linux and Windows on CUDA, ROCm, Vulkan, CPU
- **+** Private meshes via invite token, or public discovery over Nostr
- **−** Mixture-of-Agents mode (model: mesh) is experimental and needs at least two models
- **−** Native Windows CUDA runtime does not cover RTX 50-series (Blackwell) yet
- **−** Local-only mode needs absolute, non-symlink GGUF paths and skips mesh features
- **−** Source build needs just, cmake, Rust, sccache, mold or lld, and Node.js 24

<sub>GPU optional · Models: GGUF, Qwen, Llama, Gemma, Mistral · port 3131 · [Repo](https://github.com/mesh-llm/mesh-llm) · [📖 Docs ↗](https://meshllm.cloud/docs/pages/installing-mesh/) · [🌐 Site ↗](https://meshllm.cloud) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mesh-llm/)</sub>

<a name="audio-cpp"></a>
### #&#8288;52 [audio.cpp](https://github.com/0xshug0/audio.cpp) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · custom license · Nov 2026</sub>

**C++ ggml runtime for local TTS, ASR, voice cloning and separation models.**

audio.cpp is a native C++ inference framework on ggml that runs 143 audio model families (250+ variants) for TTS, ASR, voice cloning, music generation, separation, VAD and diarization. It exposes them through a shared CLI, a server API, a C ABI and a built-in WebUI, with CUDA, HIP/ROCm, Vulkan, Metal, WebGPU, SYCL and CPU backends. Most models ship as GGUF packages, many with Q8 variants.

- **+** Covers TTS, ASR, VAD, diarization, separation and music models under one CLI and server API
- **+** Backends span CUDA, ROCm, Vulkan, Metal, WebGPU, SYCL and CPU, so no Python environments
- **+** Built-in WebUI with Studio, Arena, voice library and TTS narration editor
- **+** Q8 GGUF packages reported up to 1.53x faster and 37% lower peak VRAM than 16-bit
- **−** License is reported as NOASSERTION; model weights carry separate per-family licenses
- **−** Fast-moving 0.9.x releases; HIP gfx1151_v1 kernels, avatar voice chat and LatentSync are experimental
- **−** Model ports vary in maturity; some families are still under testing
- **−** No Docker or compose files detected; builds are per-backend from source or portable builds

<sub>GPU optional · Docker · Needs ggml, GGUF model files (Hugging Face / ModelScope) · Models: GGUF, Safetensors, Qwen3-TTS, Kokoro, Fish Audio S2 · [Repo](https://github.com/0xshug0/audio.cpp) · [▶️ Demo ↗](https://colab.research.google.com/github/0xShug0/audio.cpp/blob/main/Notebooks/colab_audio_cpp.ipynb) · [📖 Docs ↗](https://huggingface.co/spaces/audio-cpp/Audio-Model-Architecture-Atlas) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/audio-cpp/)</sub>

<a name="text-generation-webui"></a>
### #&#8288;53 [Text Generation Web UI](https://github.com/oobabooga/textgen) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · AGPL-3.0 · Aug 2026</sub>

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

<a name="deepinfer"></a>
### #&#8288;54 [deepinfer](https://github.com/deepseek-ai/deepinfer) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;55 [mlc-llm](https://github.com/mlc-ai/mlc-llm) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: patchy (31) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · Apache-2.0 · Oct 2026</sub>

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

<a name="ctranslate2"></a>
### #&#8288;56 [ctranslate2](https://github.com/opennmt/ctranslate2) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · MIT · Nov 2026</sub>

**C++ and Python inference engine for Transformer models on CPU and GPU.**

CTranslate2 is a C++ runtime with Python bindings that runs converted Transformer models (NLLB, Whisper, Llama, Mistral, T5, BERT and others) using quantization, layer fusion and batch reordering. Models are converted from OpenNMT-py, OpenNMT-tf, Fairseq, Marian or Transformers into its own format. It is a library rather than a server; faster-whisper is built on it.

- **+** Supports FP16, BF16, INT16, INT8 and AWQ INT4 quantization
- **+** README benchmarks show lower memory than PyTorch and Marian on the same models
- **+** One binary selects CPU backend (MKL, oneDNN, OpenBLAS, Ruy, Accelerate) at runtime
- **+** Tensor parallelism splits large models across multiple GPUs
- **−** Models must be converted first; no direct loading of original checkpoints
- **−** Library only; an HTTP API needs the separate ctranslate2-web-server project
- **−** Limited to listed Transformer architectures; new models need explicit support
- **−** Apple Metal backend is experimental and never chosen by device=auto

<sub>GPU optional · Docker · Models: Transformer base/big, NLLB, M2M-100, BART, T5 · [Repo](https://github.com/opennmt/ctranslate2) · [📖 Docs ↗](https://opennmt.net/CTranslate2) · [🌐 Site ↗](https://opennmt.net/CTranslate2) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ctranslate2/)</sub>

<a name="olares"></a>
### #&#8288;57 [olares](https://github.com/beclab/olares) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · AGPL-3.0 · Nov 2026</sub>

**Kubernetes-based personal cloud OS for running local LLMs and AI agents.**

Olares installs a Kubernetes-based personal cloud on your own machines and manages apps, files, networking and GPUs from a browser desktop. It ships an app market with local AI apps and models, a Model Console for local LLMs, and the Lares assistant, and it can host agents such as OpenClaw. The olares-cli tool and Agent Skills let AI agents install and operate the system.

- **+** Pools GPUs across nodes with time-slicing, memory-slicing and exclusive modes
- **+** Bundles files, VPN, reverse proxy, Vault and app market in one system
- **+** Multiple install paths: shell script, ISO image, Docker Compose
- **+** olares-cli with Agent Skills lets agents install and operate the system
- **−** Needs 4 CPU cores, 8 GB RAM and 150 GB SSD; installation fails on HDD
- **−** Script install supports only Ubuntu 22.04 to 25.04 and Debian 12 or 13
- **−** Full Kubernetes stack is heavy for someone who only wants to serve one model
- **−** Installer is run as curl piped to bash with sudo

<sub>RAM ≥ 8 GB · GPU optional · Needs Ubuntu or Debian Linux, Kubernetes (bundled), 150 GB SSD · Models: local LLMs via Model Console and Olares Market · [Repo](https://github.com/beclab/olares) · [📖 Docs ↗](https://www.olares.com/docs/manual/get-started/install-olares) · [🌐 Site ↗](https://www.olares.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/olares/)</sub>

<a name="aibrix"></a>
### #&#8288;58 [aibrix](https://github.com/vllm-project/aibrix) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

**Kubernetes control plane for routing and scaling vLLM, SGLang and TensorRT-LLM.**

AIBrix runs on Kubernetes and sits in front of existing inference engines (vLLM, SGLang, TensorRT-LLM). It provides an OpenAI-compatible gateway that routes requests using live engine state such as prefix cache and load, and controllers that autoscale on engine metrics and manage models, LoRA adapters, warmup and KV cache. It targets teams running many models or replicas across mixed GPU types.

- **+** Routes by prefix-cache, load and prefill/decode placement, with session affinity
- **+** Autoscales on engine metrics: queue depth, KV cache usage, tokens
- **+** One gateway fronts vLLM, SGLang and TensorRT-LLM
- **+** Packs many LoRA adapters onto shared base-model pods
- **−** Kubernetes only; no standalone or single-host install path described
- **−** Installs Envoy Gateway and KubeRay as dependencies, adding cluster footprint
- **−** Heterogeneous GPU support is marked experimental
- **−** Does not run inference itself; an external engine is required

<sub>GPU required · Compose · Needs Kubernetes, Envoy Gateway, KubeRay, vLLM, SGLang or TensorRT-LLM · Models: vLLM, SGLang, TensorRT-LLM, LoRA adapters · [Repo](https://github.com/vllm-project/aibrix) · [📖 Docs ↗](https://aibrix.readthedocs.io/latest/) · [🌐 Site ↗](https://aibrix.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aibrix/)</sub>

<a name="yolo-ros"></a>
### #&#8288;59 [yolo_ros](https://github.com/mgonzs13/yolo_ros) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Nov 2026</sub>

**ROS 2 node running Ultralytics YOLO ONNX models for detection, pose and segmentation.**

C++ ROS 2 package that runs Ultralytics-exported YOLO ONNX models through ONNX Runtime, with no Python or ultralytics dependency at run time. A single yolo_node loads detection, tracking, 3D lifting from depth images and debug rendering as pluginlib plugins, configured from one YAML file. It supports detect, segment, pose, OBB and classify tasks on CPU, CUDA or TensorRT.

- **+** Pure C++ and ONNX Runtime; no Python runtime or ultralytics install needed at run time
- **+** One process with ordered plugin chain (detection, tracking, 3D, debug) configured by one YAML
- **+** Covers detect, segment, pose, OBB and classify; YOLOv3 through YOLO26 models
- **+** CPU on x64 and aarch64, CUDA, TensorRT, plus a QNN Hexagon NPU path
- **−** Ultralytics weights are AGPL-3.0, so the MIT license does not cover the models
- **−** Prebuilt GPU ONNX Runtime is x64-only and limited to CUDA 11, 12 and 13
- **−** QNN NPU support requires building ONNX Runtime from source
- **−** Needs a ROS 2 colcon workspace; not usable outside ROS 2

<sub>GPU optional · Docker · Needs ROS 2, colcon, ONNX Runtime 1.20.0 (vendored), CUDA and cuDNN (GPU only), TensorRT 10 (optional) · Models: YOLOv3, YOLOv5, YOLOv8, YOLOv9, YOLOv10 · [Repo](https://github.com/mgonzs13/yolo_ros) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yolo-ros/)</sub>

<a name="bentoml"></a>
### #&#8288;60 [bentoml](https://github.com/bentoml/bentoml) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Oct 2026</sub>

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

<a name="metarank"></a>
### #&#8288;61 [metarank](https://github.com/metarank/metarank) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Oct 2026</sub>

**Ranking service that reranks search and recommendation results from click signals.**

Metarank is a Scala service that reranks items from an existing search or recommendation system using LambdaMART models trained on visitor events such as clicks and purchases. It exposes HTTP endpoints for ranking and feedback, computes built-in ranking features (CTR, referer, User-Agent, session), and supports trending and similar-item recommendations via matrix factorization (ALS). State lives in Redis for horizontal scaling; a standalone mode trains and serves in one process.

- **+** Reranks large result sets in 10-20ms, per the project's benchmarks
- **+** Dozens of built-in ranking features, so little custom feature code
- **+** Standalone mode trains and serves in one command with in-memory store
- **+** Stateless service with Redis state, scales horizontally on Kubernetes
- **−** Needs a click and impression event stream to train useful models
- **−** README leaves semantic search and recommendation guides as TODO placeholders
- **−** Reranks results only; you still need a separate retrieval engine
- **−** Not a drop-in for LLM or RAG pipelines despite the LLM encoder features

<sub>Needs Redis (production state store), Elasticsearch/OpenSearch (optional, for LTR integration) · Models: LambdaMART (XGBoost), Matrix factorization ALS, LLM bi-encoder and cross-encoder text features · port 8080 · [Repo](https://github.com/metarank/metarank) · [▶️ Demo ↗](https://demo.metarank.ai) · [📖 Docs ↗](https://docs.metarank.ai) · [🌐 Site ↗](https://metarank.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/metarank/)</sub>

<a name="text-embeddings-inference"></a>
### #&#8288;62 [Text Embeddings Inference](https://github.com/huggingface/text-embeddings-inference) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · Apache-2.0 · Nov 2026</sub>

**Rust server for embedding, re-ranking and sequence classification models.**

Text Embeddings Inference (TEI) serves open text embedding, re-ranker and sequence classification models over HTTP and gRPC. It uses token-based dynamic batching with Flash Attention, Candle and cuBLASLt kernels, and loads Safetensors or ONNX weights without a graph compilation step. It exports OpenTelemetry traces and Prometheus metrics, and ships separate images for CPU and several NVIDIA GPU generations.

- **+** No model graph compilation step; small images and fast boot
- **+** Token-based dynamic batching with tunable --max-batch-tokens
- **+** Built-in OpenTelemetry tracing, Prometheus metrics and optional API key auth
- **+** Per-architecture images for CPU, Ampere, Ada, Hopper and Blackwell; Metal on Macs
- **−** Only embedding, re-ranking and classification models; no text generation
- **−** Volta GPUs not supported; Turing and Blackwell images are experimental
- **−** Limited to listed architectures such as BERT, XLM-RoBERTa, Qwen, Gemma3 and Mistral
- **−** Flash Attention disabled by default on Turing due to precision issues

<sub>GPU optional · Docker · Needs Docker, NVIDIA Container Toolkit (GPU images) · Models: Safetensors, ONNX, BERT, XLM-RoBERTa, Qwen2 · port 8080 · [Repo](https://github.com/huggingface/text-embeddings-inference) · [📖 Docs ↗](https://huggingface.github.io/text-embeddings-inference) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/text-embeddings-inference/)</sub>

<a name="bitnet"></a>
### #&#8288;63 [bitnet](https://github.com/microsoft/bitnet) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: widely used (89) · Freshness: active (93) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · MIT · Jul 2026</sub>

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

<a name="openllm"></a>
### #&#8288;64 [OpenLLM](https://github.com/bentoml/openllm) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (66) · Freshness: recent (70) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

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

<a name="zml"></a>
### #&#8288;65 [zml](https://github.com/zml/zml) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (16) · Freshness: active (98) · Maintenance: patchy (48) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Nov 2026</sub>

**Zig and MLIR inference stack compiling models for GPUs, TPUs and Trainium.**

ZML is an inference stack written in Zig on top of MLIR and built with Bazel. Models are written in Zig with tagged tensors and compiled for CUDA, ROCm, Intel OneAPI, Google TPU and AWS Trainium/Inferentia 2 from one codebase. The bundled LLM example runs Llama 3.1/3.2, Qwen 3.5 and LFM 2.5 from Hugging Face, local directories or S3.

- **+** One Zig codebase targets CUDA, ROCm, OneAPI, TPU and Trainium via build flags
- **+** Loads weights from hf://, local paths, https:// and s3:// through a VFS layer
- **+** Bazel is the only prerequisite; examples run with a single bazel run command
- **+** Includes sharding, profiler and benchmark examples for multi-device use
- **−** LLM example supports only Llama 3.1/3.2, Qwen 3.5 and LFM 2.5
- **−** Models must be written in Zig; much smaller ecosystem than PyTorch
- **−** Examples are CLIs; README shows no OpenAI-compatible HTTP server
- **−** Bazel build adds setup and build-time overhead for casual use

<sub>GPU optional · Needs Bazel (via bazelisk), Hugging Face token for gated models · Models: Llama 3.1, Llama 3.2, Qwen 3.5, LFM 2.5, MNIST · [Repo](https://github.com/zml/zml) · [🌐 Site ↗](https://zml.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/zml/)</sub>

<a name="litserve"></a>
### #&#8288;66 [litserve](https://github.com/lightning-ai/litserve) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · Apache-2.0 · Oct 2026</sub>

**Python framework for writing custom inference servers on FastAPI.**

LitServe is a Python library where you subclass LitAPI, implement setup() and predict(), and serve it through a FastAPI-based LitServer. It covers batching, streaming, multi-worker and GPU device handling, OpenAI-spec compatibility and MCP server support. It suits multi-model pipelines, agents and RAG APIs. The README says it is not a drop-in vLLM or Ollama replacement.

- **+** Arbitrary Python in setup() and predict(), so multi-model, agent and RAG pipelines fit in one class
- **+** Built-in batching, streaming, worker autoscaling and OpenAI-spec endpoint support
- **+** Framework-agnostic: PyTorch, JAX, TensorFlow, or an external engine such as vLLM
- **+** Runs locally with pip install litserve and python server.py
- **−** Not a ready-to-run LLM server; you write the serving code for each model
- **−** Authentication is DIY when self-hosted; token and password auth are listed for managed only
- **−** Load balancing, scale-to-zero and multi-node inference are listed as managed-only features
- **−** The 2x-faster-than-FastAPI claim comes from the project's own benchmarks

<sub>GPU optional · Needs FastAPI · Models: PyTorch, JAX, TensorFlow, Hugging Face, vLLM · port 8000 · [Repo](https://github.com/lightning-ai/litserve) · [📖 Docs ↗](https://lightning.ai/docs/litserve) · [🌐 Site ↗](https://lightning.ai/litserve) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/litserve/)</sub>

<a name="lightllm"></a>
### #&#8288;67 [lightllm](https://github.com/modeltc/lightllm) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: patchy (41) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · Apache-2.0 · Nov 2026</sub>

**Python LLM inference server with token-level KV cache management.**

LightLLM is a pure-Python inference and serving framework for large language models. It builds on ideas and kernels from FasterTransformer, TGI, vLLM, SGLang, FlashAttention and OpenAI Triton. The README highlights DeepSeek-R1 serving on a single H200 machine, constrained decoding for structured output, a Past-Future request scheduler, and prefix KV cache transfer between data-parallel ranks.

- **+** Pure-Python code with token-level KV cache management, easy to modify for research
- **+** Some kernels are reused by vLLM, SGLang and Aphrodite, per the README
- **+** Published scheduler (ASPLOS'25) and constrained decoding (ACL2025) research
- **+** Docs include a DeepSeek deployment tutorial
- **−** README lists no supported model families or quantization formats
- **−** No Dockerfile or compose file detected in the repository
- **−** README gives no benchmark numbers, only links to blog posts
- **−** README shows no API endpoints or launch commands

<sub>Docker · Needs Triton, FlashAttention, flashinfer · Models: DeepSeek-R1, Qwen3-8B · [Repo](https://github.com/modeltc/lightllm) · [📖 Docs ↗](https://lightllm-en.readthedocs.io/en/latest/) · [🌐 Site ↗](https://modeltc.github.io/lightllm-blog/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lightllm/)</sub>

<a name="tabbyapi"></a>
### #&#8288;68 [TabbyAPI](https://github.com/theroyallab/tabbyapi) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Nov 2026</sub>

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

<a name="chatrwkv"></a>
### #&#8288;69 [chatrwkv](https://github.com/blinkdl/chatrwkv) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: popular (54) · Freshness: active (90) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · Apache-2.0 · Jul 2026</sub>

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

<a name="nano-vllm"></a>
### #&#8288;70 [nano-vllm](https://github.com/geeeekexplorer/nano-vllm) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (72) · Freshness: recent (60) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Apr 2026</sub>

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

<a name="tensorrt-yolo"></a>
### #&#8288;71 [tensorrt-yolo](https://github.com/laugh12321/tensorrt-yolo) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (3) · Freshness: active (87) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · GPL-3.0 · Sep 2026</sub>

**C++ and Python TensorRT inference for YOLO models on NVIDIA GPUs.**

TensorRT-YOLO deploys YOLO models (YOLOv3 through YOLO26, plus YOLO-World, YOLOE and YOLO-Master) as TensorRT engines. It uses TensorRT plugins for post-processing, CUDA kernels for preprocessing and CUDA Graphs, and covers detect, segment, classify, pose and OBB tasks from C++ (single header) or Python. This repo is the community edition (6.4) with a frozen inference interface; a closed-source pro edition is announced but not yet purchasable.

- **+** Covers detect, segment, classify, pose and OBB with one API per task
- **+** C++ header-only client, no CUDA or TensorRT linking needed when using the module
- **+** CUDA preprocessing replicates OpenCV letterbox; most pixel errors are 0
- **+** Runs on Linux and Windows, x64 and ARM, with Jetson zero-copy mode
- **−** NVIDIA GPUs only; requires TensorRT and CUDA
- **−** Community edition frozen; no new runtime features, pipelining or ensembles
- **−** Pose, segment and OBB engines need custom plugins built into the engine
- **−** GPL-3.0 license; docs and tutorials are mainly in Chinese

<sub>GPU required · Docker · Needs CUDA, TensorRT, CMake, pybind11, trtyolo-export, OpenCV (examples) · Models: YOLOv3 to YOLO26, YOLO-World, YOLOE, YOLO-Master, YOLO12 · [Repo](https://github.com/laugh12321/tensorrt-yolo) · [🌐 Site ↗](https://trtyolo.laugh12321.cn/pro/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorrt-yolo/)</sub>

<a name="powerinfer"></a>
### #&#8288;72 [powerinfer](https://github.com/tiiny-ai/powerinfer) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: popular (57) · Freshness: recent (65) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · MIT · May 2026</sub>

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

<a name="mini-sglang"></a>
### #&#8288;73 [mini-sglang](https://github.com/sgl-project/mini-sglang) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: niche (28) · Freshness: recent (67) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · MIT · May 2026</sub>

**Compact SGLang reimplementation for serving LLMs, in about 5,000 lines of Python.**

Mini-SGLang is a compact Python reimplementation of SGLang. It serves Hugging Face models over an OpenAI-compatible API and has a terminal chat shell mode. It includes radix cache, chunked prefill, overlap scheduling, tensor parallelism and FlashAttention/FlashInfer kernels. It is meant as a readable reference for how LLM serving works.

- **+** Small, type-annotated codebase (~5,000 lines of Python) that is practical to read and modify
- **+** Implements radix cache, chunked prefill, overlap scheduling and tensor parallelism via --tp
- **+** OpenAI-compatible server plus a terminal chat shell via --shell
- **+** README includes benchmarks against SGLang on H200 GPUs with Qwen3 models
- **−** Linux only (x86_64, aarch64); macOS and Windows need WSL2 or Docker
- **−** Needs an NVIDIA GPU and a CUDA Toolkit matching the driver; kernels are JIT-compiled
- **−** No tagged release; installed from source with uv pip install -e .
- **−** Documented as a compact subset, so likely narrower in features than full SGLang

<sub>GPU required · Docker · Needs NVIDIA CUDA Toolkit, FlashInfer, sgl-kernel, uv · Models: Hugging Face models, Qwen3, Llama 3.1, ModelScope download · port 1919 · [Repo](https://github.com/sgl-project/mini-sglang) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mini-sglang/)</sub>

<a name="seldon-core"></a>
### #&#8288;74 [seldon-core](https://github.com/seldonio/seldon-core) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (22) · Freshness: slowing (35) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · custom license · Jan 2026</sub>

**Kubernetes framework for serving ML models and Kafka-connected pipelines.**

Seldon Core 2 deploys and scales models on Kubernetes, with multi-model serving on shared inference servers and overcommit to host more models than fit in memory. Pipelines chain models and custom components using Kafka for streaming data, and experiments route traffic for A/B tests and shadow deployments. It is written in Go and distributed under the Business Source License.

- **+** Multi-model serving consolidates several models on shared inference servers
- **+** Overcommit lets you deploy more models than memory allows
- **+** Experiments support A/B tests and shadow deployments between models or pipelines
- **+** Pipelines stream data between components over Kafka
- **−** Business Source License, not OSI open source; commercial use may require Seldon
- **−** Requires a Kubernetes cluster; no standalone or Docker quick start in the README
- **−** Pipelines depend on Kafka, adding another system to operate
- **−** No hardware requirements or model format list in the README

<sub>Needs Kubernetes, Kafka · [Repo](https://github.com/seldonio/seldon-core) · [📖 Docs ↗](https://docs.seldon.ai/seldon-core-2) · [🌐 Site ↗](https://www.seldon.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/seldon-core/)</sub>

<a name="gemma-cpp"></a>
### #&#8288;75 [gemma.cpp](https://github.com/google/gemma.cpp) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: known (41) · Freshness: quiet (0) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2025</sub>

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

<a name="deepstream-yolo"></a>
### #&#8288;76 [deepstream-yolo](https://github.com/marcoslucianops/deepstream-yolo) <sub>score [9](../README.md#-how-we-rank "Score 9/100. Adoption: niche (5) · Freshness: quiet (27) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · MIT · Jan 2026</sub>

**NVIDIA DeepStream configs and GPU parsers for running YOLO and DETR detectors.**

Configuration and custom TensorRT parsing library (nvdsinfer_custom_impl_Yolo) for running YOLO-family detectors inside NVIDIA DeepStream, from SDK 5.1 to 8.0 on x86 and Jetson. It converts Darknet cfg/weights or ONNX exports into TensorRT engines and does bbox post-processing on the GPU. It also supports INT8 PTQ calibration, non-square input and dynamic batch size.

- **+** Covers about 27 detector families, including YOLOv5 to YOLO26, RT-DETR, D-FINE and RF-DETR
- **+** GPU bbox parser, INT8 PTQ calibration, dynamic batch size and non-square models
- **+** Per-model usage docs plus benchmarks and a custom ONNX model guide
- **+** Supports DeepStream 5.1 to 8.0 on both x86 and Jetson
- **−** Tied to NVIDIA DeepStream, TensorRT and CUDA; no use outside the NVIDIA stack
- **−** Author says updates are currently limited
- **−** TensorRT engine generation can take more than 10 minutes
- **−** Needs manual CUDA_VER matching and a make build of the library; no release published

<sub>GPU required · Needs NVIDIA DeepStream SDK, CUDA, TensorRT, GStreamer, NVIDIA driver, JetPack (Jetson) · Models: Darknet (YOLOv4, etc.), YOLOv5, YOLOv6, YOLOv7, YOLOv8 · [Repo](https://github.com/marcoslucianops/deepstream-yolo) · [📖 Docs ↗](https://github.com/marcoslucianops/DeepStream-Yolo/blob/master/docs/customModels.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepstream-yolo/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
