# 🧠 Model serving reviews · Best of Open-Source AI

Inference engines and model servers that expose local models over an API. Back to the [leaderboard](../README.md#-model-serving).

<sub>🌐 Also on the web: [Model serving on archestack.com](https://archestack.com/best-of-ai/model-serving/), each project on its own page.</sub>

<a name="localai"></a>
### 🥇 [LocalAI](https://github.com/mudler/localai) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Oct 2026</sub>

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

<a name="llama-cpp"></a>
### 🥈 [llama.cpp](https://github.com/ggml-org/llama.cpp) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 131k · MIT · Oct 2026</sub>

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
### 🥉 [Ollama](https://github.com/ollama/ollama) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 183k · MIT · Oct 2026</sub>

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

<a name="vllm"></a>
### #&#8288;4 [vLLM](https://github.com/vllm-project/vllm) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 94k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;5 [colibri](https://github.com/justvugg/colibri) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · Apache-2.0 · Oct 2026</sub>

**C inference engine that runs huge MoE models by streaming experts from disk.**

colibri runs large mixture-of-experts models such as GLM-5.2 (744B) and Kimi K3 (2.8T) on ordinary hardware. It keeps the dense weights in RAM and reads routed experts from disk through a cache, with optional Vulkan or CUDA offload. It serves a browser dashboard plus OpenAI- and Anthropic-compatible HTTP endpoints, and ships guided setup scripts for Windows, Linux and macOS.

- **+** Pure C engines, no GPU required; 8 GB RAM minimum for the smallest model
- **+** Serves OpenAI and Anthropic-style APIs on port 8000, plus a web dashboard
- **+** Vulkan works on AMD, Intel and NVIDIA; CUDA path for NVIDIA on Linux and Windows
- **+** Setup script detects hardware, recommends a model, and resumes interrupted downloads
- **−** Large models stream from disk: 0.05-3 tok/s on typical machines, per README tables
- **−** Discrete-GPU performance mostly unmeasured by the authors; relies on user reports
- **−** Supports a fixed list of model families, one engine each; other architectures need new code
- **−** Some models need manual conversion or preparation steps after download

<sub>RAM ≥ 8 GB · GPU optional · Docker + Compose · Models: GLM-5.2, GLM-5.3, GLM-5.3-Flash, Inkling, Kimi K3 · port 8000 · [Repo](https://github.com/justvugg/colibri) · [📖 Docs ↗](https://github.com/JustVugg/colibri/blob/main/docs/quickstart.md) · [🌐 Site ↗](https://justvugg.github.io/colibri) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/colibri/)</sub>

<a name="sglang"></a>
### #&#8288;6 [SGLang](https://github.com/sgl-project/sglang) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: easy (50) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

**Inference server for LLM, vision-language and diffusion models.**

SGLang is a Python inference framework for serving large language, vision-language and diffusion models, aimed at agentic workloads, large-scale serving and RL rollouts. It runs on NVIDIA, AMD, Google TPU, Intel, Apple Silicon, Huawei Ascend and Moore Threads hardware, and includes a built-in engine for image and video generation. Install via the lmsysorg/sglang Docker image or uv pip.

- **+** Supports NVIDIA, AMD, TPU, Intel, Apple Silicon, Ascend and Moore Threads hardware
- **+** Image and video diffusion engine ships in the same package
- **+** Integrated by RL training frameworks such as verl and slime for rollouts
- **+** Apache-2.0 license, with a Docker image and a cookbook of launch commands
- **−** Audio TTS/ASR serving lives in a separate project, SGLang Omni
- **−** Install requires --prerelease=allow with uv, suggesting prerelease dependencies
- **−** Several hardware backends (Trainium, Cambricon, MetaX) are still in progress
- **−** README gives no RAM or VRAM requirements; sizing depends on model and hardware

<sub>Docker + Compose · Models: LLMs, vision-language models, diffusion models · [Repo](https://github.com/sgl-project/sglang) · [📖 Docs ↗](https://docs.sglang.io/) · [🌐 Site ↗](https://www.sglang.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sglang/)</sub>

<a name="lemonade"></a>
### #&#8288;7 [Lemonade](https://github.com/lemonade-sdk/lemonade) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

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

<a name="exo"></a>
### #&#8288;8 [exo](https://github.com/exo-explore/exo) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: patchy (39) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · Apache-2.0 · Oct 2026</sub>

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

<a name="llama-swap"></a>
### #&#8288;9 [llama-swap](https://github.com/mostlygeek/llama-swap) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (90) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Oct 2026</sub>

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

<a name="xinference"></a>
### #&#8288;10 [Xinference](https://github.com/xorbitsai/inference) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (30) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

**Serves LLM, embedding, speech and image models behind one OpenAI-compatible API.**

Xinference is a Python library and server that runs language, embedding, speech recognition, image and multimodal models from a single command, with built-in model definitions and support for custom ones. It exposes an OpenAI-compatible REST API with function calling, plus RPC, a CLI and a web UI, and can spread models across multiple workers. It runs on GPUs and CPUs through backends including vLLM and its own llama.cpp binding.

- **+** One server covers LLM, embedding, audio, image and multimodal models
- **+** OpenAI-compatible REST API with function calling
- **+** Distributed inference across workers; Helm chart for Kubernetes
- **+** Install via pip, one-line script, Docker or Helm
- **−** Enterprise, Cloud and managed Model API offerings are commercial; edition differences not listed
- **−** 3.0.0 release notes mention breaking changes and migration steps
- **−** RAM and VRAM requirements are not stated; they depend on the model
- **−** README feature list is dense; hardware and backend support per model is unclear

<sub>GPU optional · Models: vLLM, ggml, llama.cpp (xllamacpp), TensorRT, embedding models · port 9997 · [Repo](https://github.com/xorbitsai/inference) · [📖 Docs ↗](https://inference.readthedocs.io/) · [🌐 Site ↗](https://xinference.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xinference/)</sub>

<a name="mistral-rs"></a>
### #&#8288;11 [mistral.rs](https://github.com/ericlbuehler/mistral.rs) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: fair (75) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · MIT · Oct 2026</sub>

**Rust inference server with OpenAI and Anthropic APIs and agent tools.**

mistral.rs is a Rust engine whose single binary runs and serves Hugging Face, GGUF and UQFF models (text, vision, video, audio, speech, image generation; 45+ architectures) with auto-detected architecture and chat template. The serve command exposes OpenAI /v1 and Anthropic Messages endpoints, a web UI at /ui and Prometheus metrics on port 1234, with paged attention, ISQ, LoRA and a built-in agent loop.

- **+** One binary for chat, server, benchmarks and web UI; prebuilt for Metal, CUDA, CPU
- **+** In-situ quantization of any Hugging Face model plus GGUF 2-8 bit, GPTQ, AWQ, FP8
- **+** Server-side agent loop with Python, shell, web search, skills and MCP client
- **+** mistralrs tune recommends quantization and device mapping for your hardware
- **−** BF16 prefill trails vLLM by 5-10x on the 26B MoE in its own benchmarks
- **−** Install script is curl piped to sh, falling back to a source build
- **−** cuTile acceleration needs NVIDIA's separately installed tileiras tool
- **−** Not affiliated with Mistral AI despite the name

<sub>GPU optional · Docker · Models: Hugging Face safetensors, GGUF, UQFF, Qwen3, Gemma 4, Muse Glimmer, DiffusionGemma and 45+ architectures · port 1234 · [Repo](https://github.com/ericlbuehler/mistral.rs) · [📖 Docs ↗](https://docs.mistralrs.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mistral-rs/)</sub>

<a name="gpustack"></a>
### #&#8288;12 [GPUStack](https://github.com/gpustack/gpustack) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Oct 2026</sub>

**GPU cluster manager that deploys models on vLLM, SGLang and TensorRT-LLM.**

GPUStack is a GPU cluster manager that deploys models across on-prem, Kubernetes and cloud workers, configuring vLLM, SGLang, TensorRT-LLM or custom engines behind OpenAI-compatible APIs with auth, API keys and token metering. The server is one Docker container on port 80 and can run CPU-only; Linux workers join with a privileged Docker command. It supports NVIDIA, AMD, Ascend and six Chinese accelerator families.

- **+** Multi-cluster: on-prem, Kubernetes and cloud GPUs under one server
- **+** Auto-selects and tunes vLLM, SGLang or TensorRT-LLM per model
- **+** Built-in auth, API keys, token metering, Grafana and Prometheus dashboards
- **+** SSH-accessible GPU instances on demand for fine-tuning
- **−** Workers are Linux-only; macOS cannot be a worker, Windows needs WSL2
- **−** Worker container runs privileged with the Docker socket mounted
- **−** Cluster topology view is in the paid GPUStack Enterprise
- **−** Quick start assumes an NVIDIA GPU; other vendors need extra steps

<sub>GPU required · Compose · Models: catalog models (e.g. Qwen3.5-0.8B) via vLLM, SGLang, TensorRT-LLM, LLM, voice, image and video models · port 80 · [Repo](https://github.com/gpustack/gpustack) · [📖 Docs ↗](https://docs.gpustack.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpustack/)</sub>

<a name="triton-inference-server"></a>
### #&#8288;13 [Triton Inference Server](https://github.com/triton-inference-server/server) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · BSD-3-Clause · Oct 2026</sub>

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

<a name="laya-mlx"></a>
### #&#8288;14 [laya-mlx](https://github.com/mizorewww/laya-mlx) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Oct 2026</sub>

**MLX port of Laya typed-decision models for Apple Silicon.**

Runs the Laya encoder checkpoints (322M to 421M parameters) natively on Apple Silicon with MLX. It answers typed questions (choice, score, true/false probability) in one forward pass with zero output tokens. Reported M3 Max median latency is 13.4 ms for the English model and 7.4 ms for the multilingual one. It is an independent port covering inference and conversion, not training.

- **+** Single forward pass, no token decoding or JSON generation; P50 13.42 ms English on M3 Max
- **+** Matched upstream answers on 63/63 validation questions in FP32 and FP16 per checkpoint
- **+** No PyTorch, Transformers runtime or cloud API; runs locally after first weight download
- **+** Includes language router, confidence gating, shortlist and tournament helpers for large choice sets
- **−** Apple Silicon only (macOS 14+, Python 3.11+); no CUDA or Linux path
- **−** Limited to choice, score and noul questions; not a general text-generation server
- **−** No training or fine-tuning; upstream batch, HTTP/MCP server and hooks APIs are not included
- **−** Context capped at 512 or 1,024 tokens; many-label choices need shortlisting or tournament

<sub>GPU required · Needs MLX, Hugging Face Hub (checkpoint download) · Models: convaiinnovations/laya (ModernBERT-large, 421M), convaiinnovations/laya-multilingual (mmBERT-base, 322M), convaiinnovations/laya-typed-decisions (ModernBERT-large, 421M) · [Repo](https://github.com/mizorewww/laya-mlx) · [📖 Docs ↗](https://github.com/mizorewww/laya-mlx/blob/main/BENCHMARKS.md) · [🌐 Site ↗](https://huggingface.co/aac6fef/laya-mlx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/laya-mlx/)</sub>

<a name="ktransformers"></a>
### #&#8288;15 [KTransformers](https://github.com/kvcache-ai/ktransformers) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (79) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Oct 2026</sub>

**CPU-GPU hybrid inference and LoRA fine-tuning for large MoE models.**

KTransformers runs large Mixture-of-Experts models by keeping hot experts on the GPU and cold experts on the CPU, using AMX/AVX512/AVX2 INT4/INT8 kernels with NUMA-aware memory. The kt-kernel package plugs into SGLang for serving. A second path integrates with LLaMA-Factory for LoRA and full fine-tuning of MoE models such as DeepSeek-V3/R1 and Kimi K2.5 on limited GPU memory.

- **+** Runs very large MoE models with experts offloaded to CPU RAM, so fewer GPUs are needed
- **+** CPU kernels cover Intel AMX, AVX512 and AVX2-only machines
- **+** Fine-tuning via LLaMA-Factory; README lists DeepSeek-V3 at ~80GB total GPU memory on 4x RTX 4090
- **+** Fast support for new models, with tutorials for GLM-5, Kimi K2.5, MiniMax and DeepSeek-V4-Flash
- **−** Needs large system RAM for big MoE models; exact minimum is not stated in the README
- **−** Original integrated framework is archived; the current docs are split across kt-kernel and SFT
- **−** Serving depends on SGLang integration rather than a standalone server in this README
- **−** Research-oriented project; setup is manual, with per-model tutorials and hardware-specific steps

<sub>GPU required · Docker · Needs SGLang, LLaMA-Factory, PyTorch · Models: DeepSeek-V3/R1, DeepSeek-V4-Flash, Kimi K2/K2.5/K2.6, GLM-5, MiniMax-M2.5/M3 · [Repo](https://github.com/kvcache-ai/ktransformers) · [📖 Docs ↗](https://kvcache-ai.github.io/ktransformers/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ktransformers/)</sub>

<a name="lmdeploy"></a>
### #&#8288;16 [LMDeploy](https://github.com/internlm/lmdeploy) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: some setup (33) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · Apache-2.0 · Oct 2026</sub>

**LLM and VLM serving toolkit with the TurboMind and PyTorch engines.**

LMDeploy compresses and serves LLMs and VLMs with two engines: TurboMind (CUDA, persistent batching, blocked KV cache, AWQ W4A16, MXFP4) and a pure-Python PyTorch engine that also runs on Huawei Ascend. pip install lmdeploy adds an API server plus a proxy for multi-model, multi-machine serving. Models span Llama, Qwen3, DeepSeek-V3/V4, GLM-5, InternVL and Qwen3-VL.

- **+** TurboMind engine with persistent batching, blocked KV cache and 4-bit AWQ inference
- **+** Online INT8/INT4 KV cache quantization and prefix caching usable together
- **+** Wide VLM list: InternVL 1 to 3.5, Qwen2/2.5/3-VL, LLaVA, Gemma3, Llama4
- **+** PyTorch engine supports Huawei Ascend NPUs with graph mode
- **−** The two engines support different model sets and dtypes; check the matrix
- **−** Prebuilt wheels target CUDA 12.8; other CUDA versions need source builds
- **−** No port, VRAM or web UI details in the README
- **−** Community channels are WeChat-centric alongside Discord

<sub>GPU required · Docker · Models: Llama 1-4, Qwen1.5-3.5, InternLM2/3, DeepSeek V2-V4, GLM-4/5, Mixtral, Gemma, Phi-3/4, gpt-oss, VLMs: InternVL, Qwen-VL, LLaVA, DeepSeek-VL, CogVLM, MiniCPM-V, Molmo, Gemma3, Llama4 · [Repo](https://github.com/internlm/lmdeploy) · [📖 Docs ↗](https://lmdeploy.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmdeploy/)</sub>

<a name="text-generation-webui"></a>
### #&#8288;17 [Text Generation Web UI](https://github.com/oobabooga/textgen) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: weak (14) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · AGPL-3.0 · Aug 2026</sub>

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

<a name="airllm"></a>
### #&#8288;18 [airllm](https://github.com/lyogavin/airllm) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: fair (69) · Easy to run: hard (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Oct 2026</sub>

**Python library that runs large LLMs on small GPUs by streaming layers from disk.**

AirLLM splits a Hugging Face model into per-layer shards and keeps only one decoder layer on the GPU at a time, so VRAM need tracks layer size rather than total model size. The README reports Llama 3.x 70B in about 4GB, DeepSeek-V3 671B in about 12GB, and LoRA training of Qwen3.8-Flash-Next 125B under 6GB. Loading goes through a single AutoModel.from_pretrained call, with optional 4bit/8bit compression.

- **+** Runs 70B models in about 4GB VRAM without quantization, distillation or pruning, per the README
- **+** One AutoModel.from_pretrained call covers Llama, Qwen, DeepSeek, Mistral, Mixtral, Phi, Gemma and others
- **+** Includes LoRA training that streams frozen weights layer by layer, with example scripts
- **+** Supports Apple silicon via mlx and CPU inference, besides CUDA GPUs
- **−** Splitting the model needs large disk space, for example about 360GB for Flash-Next
- **−** Speed is bound by disk loading; the README gives no tokens-per-second figures
- **−** No HTTP API or server; it is a Python library used with generate()
- **−** Newer models need specific transformers versions, and Kimi K3 needs flash-attn on CUDA 12

<sub>GPU optional · Needs PyTorch, transformers, bitsandbytes (for 4bit/8bit compression), mlx (macOS), flash-attn and compressed-tensors (Kimi K3) · Models: Llama 2/3/3.1/3.3/4, Qwen 1/2/2.5/3/3.5/3.8, DeepSeek V2/V3/R1, Mistral, Mixtral · [Repo](https://github.com/lyogavin/airllm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/airllm/)</sub>

<a name="llamafile"></a>
### #&#8288;19 [llamafile](https://github.com/mozilla-ai/llamafile) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: known (47) · Freshness: active (100) · Maintenance: fair (79) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · custom license · Oct 2026</sub>

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

<a name="text-embeddings-inference"></a>
### #&#8288;20 [Text Embeddings Inference](https://github.com/huggingface/text-embeddings-inference) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: patchy (49) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · Apache-2.0 · Oct 2026</sub>

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

<a name="tabbyapi"></a>
### #&#8288;21 [TabbyAPI](https://github.com/theroyallab/tabbyapi) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: fair (58) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Oct 2026</sub>

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

<a name="bitnet"></a>
### #&#8288;22 [bitnet](https://github.com/microsoft/bitnet) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: weak (19) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Jul 2026</sub>

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
### #&#8288;23 [OpenLLM](https://github.com/bentoml/openllm) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (37) · Freshness: recent (58) · Maintenance: patchy (33) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · May 2026</sub>

**One-command OpenAI-compatible endpoints for curated open LLMs.**

OpenLLM serves open LLMs as OpenAI-compatible APIs with one command: pip install openllm, then openllm serve llama3.2:1b starts a vLLM-backed server on port 3000 with a chat UI at /chat. Models come as prebuilt Bentos from a curated repository (Llama 3.x and 4, Qwen2.5, Mistral, Phi-4, Gemma, DeepSeek R1) and the catalog states the GPU each needs. openllm deploy pushes the same Bento to BentoCloud.

- **+** One command gives an OpenAI API plus /chat UI on port 3000
- **+** Catalog lists the required GPU per model tag (12 GB to 16x80 GB)
- **+** vLLM backend for serving
- **+** Same Bento deploys to Docker, Kubernetes or BentoCloud
- **−** Every catalog model requires a GPU; no CPU-only entries
- **−** Custom model repositories must be public
- **−** Catalog tops out around Llama 3.3 and Qwen2.5; last commit 2026-05-29
- **−** Adding models means building BentoML Bentos

<sub>GPU required · Models: Llama 3.1/3.2/3.3/4, Qwen2.5, Qwen2.5-Coder, QwQ, Mistral, Mistral Large, Pixtral, Phi-4, Gemma 2/3, Jamba 1.5, DeepSeek R1 · port 3000 · [Repo](https://github.com/bentoml/openllm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openllm/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
