# 🧠 Model serving reviews · Best of Open-Source AI

Inference engines and model servers that expose local models over an API. Back to the [leaderboard](../README.md#-model-serving).

<a name="localai"></a>
### 🥇 [LocalAI](https://github.com/mudler/localai) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 49k · MIT · Oct 2026</sub>

**One OpenAI-compatible server for text, speech, image and video models.**

LocalAI is a Go server on port 8080 with OpenAI, Anthropic, ElevenLabs and Ollama-compatible APIs for text, vision, speech, image and video. Backends (llama.cpp, vLLM, SGLang, whisper.cpp, diffusers, MLX, 60+ total) ship as separate OCI images pulled on demand; containers exist for CPU, CUDA, ROCm, Intel and Vulkan. It adds API keys, quotas and OIDC, agents with MCP, and a PostgreSQL/NATS distributed mode.

- **+** Small core; 60+ backends installed on demand as OCI images
- **+** OpenAI, Anthropic, ElevenLabs and Ollama API compatibility in one server
- **+** Multi-user: API keys, per-user quotas, role-based access, OIDC
- **+** Container images for CPU, CUDA 12/13, ROCm, Intel oneAPI, Vulkan, Jetson
- **−** First model load pulls backend images; needs network and disk space
- **−** macOS DMG is unsigned and needs quarantine removal
- **−** Distributed mode requires PostgreSQL and NATS
- **−** Very wide scope (agents, biometrics, video) increases configuration surface

<sub>GPU optional · Docker + Compose · Needs PostgreSQL and NATS (distributed mode only) · Models: GGUF via llama.cpp, vLLM, SGLang, transformers, MLX, diffusers, whisper.cpp backends, models from gallery, Hugging Face, Ollama registry, OCI images, YAML · port 8080 · [Repo](https://github.com/mudler/localai) · [📖 Docs ↗](https://localai.io/basics/getting_started/) · [🌐 Site ↗](https://localai.io/)</sub>

<a name="llama-cpp"></a>
### 🥈 [llama.cpp](https://github.com/ggml-org/llama.cpp) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 131k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker · Models: GGUF models from Hugging Face (e.g. Qwen3.5-0.8B-GGUF) · [Repo](https://github.com/ggml-org/llama.cpp) · [🌐 Site ↗](https://llama.app)</sub>

<a name="vllm"></a>
### 🥉 [vLLM](https://github.com/vllm-project/vllm) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 93k · Apache-2.0 · Oct 2026</sub>

**High-throughput LLM serving engine with OpenAI and Anthropic APIs.**

vLLM is a Python serving engine for Hugging Face models that batches requests continuously with PagedAttention, prefix caching and speculative decoding, exposing an OpenAI-compatible API plus Anthropic Messages API and gRPC. It covers 200+ architectures (dense, MoE, multimodal, embedding) with FP8, INT8, GPTQ, AWQ and GGUF quantization and tensor, pipeline and expert parallelism.

- **+** Continuous batching with PagedAttention for high multi-user throughput
- **+** 200+ Hugging Face architectures including MoE, multimodal and embedding models
- **+** OpenAI, Anthropic Messages and gRPC endpoints with tool calling and structured output
- **+** Runs on NVIDIA, AMD, Intel GPUs, CPUs, TPUs, Gaudi, Ascend via plugins
- **−** No web UI; API server only
- **−** README gives no VRAM, port or model-size guidance
- **−** Heavy Python, PyTorch and CUDA dependency chain; no single binary
- **−** Most optimized kernels target NVIDIA and AMD GPUs; CPU path is secondary

<sub>GPU optional · Docker · Models: 200+ Hugging Face architectures: Llama, Qwen, Gemma, Mixtral, DeepSeek-V3, GPT-OSS, LLaVA, Qwen-VL, E5-Mistral · [Repo](https://github.com/vllm-project/vllm) · [📖 Docs ↗](https://docs.vllm.ai) · [🌐 Site ↗](https://vllm.ai)</sub>

<a name="ollama"></a>
### #&#8288;4 [Ollama](https://github.com/ollama/ollama) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 183k · MIT · Oct 2026</sub>

**Runs open-weight models locally behind a CLI and REST API.**

Ollama runs open-weight models locally with a CLI and a REST API on port 11434, pulling models from its own library (for example gemma4) and using llama.cpp as the inference backend. Install scripts cover macOS, Windows and Linux, and an official Docker image exists. The ollama launch command wires it into coding agents such as Claude Code, Codex, Copilot CLI and OpenCode, or into OpenClaw as a chat assistant.

- **+** One command pulls and runs a model; REST API on 11434
- **+** Official Docker image plus Python and JavaScript libraries
- **+** ollama launch integrates with Claude Code, Codex, Copilot CLI, OpenCode
- **+** Broad ecosystem: dozens of web, desktop and IDE clients listed
- **−** Single inference backend: llama.cpp
- **−** Install is a curl piped to sh script
- **−** README gives no RAM or VRAM guidance per model size
- **−** Models come from Ollama's own registry; others need import steps

<sub>GPU optional · Docker · Models: Ollama library models (e.g. gemma4), GGUF via llama.cpp · port 11434 · [Repo](https://github.com/ollama/ollama) · [📖 Docs ↗](https://docs.ollama.com/quickstart) · [🌐 Site ↗](https://ollama.com)</sub>

<a name="colibri"></a>
### #&#8288;5 [colibri](https://github.com/justvugg/colibri) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Oct 2026</sub>

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

<sub>RAM ≥ 8 GB · GPU optional · Docker + Compose · Models: GLM-5.2, GLM-5.3, GLM-5.3-Flash, Inkling, Kimi K3 · port 8000 · [Repo](https://github.com/justvugg/colibri) · [📖 Docs ↗](https://github.com/JustVugg/colibri/blob/main/docs/quickstart.md) · [🌐 Site ↗](https://justvugg.github.io/colibri)</sub>

<a name="sglang"></a>
### #&#8288;6 [SGLang](https://github.com/sgl-project/sglang) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: easy (50) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

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

<sub>Docker + Compose · Models: LLMs, vision-language models, diffusion models · [Repo](https://github.com/sgl-project/sglang) · [📖 Docs ↗](https://docs.sglang.io/) · [🌐 Site ↗](https://www.sglang.io/)</sub>

<a name="lemonade"></a>
### #&#8288;7 [Lemonade](https://github.com/lemonade-sdk/lemonade) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

**Local AI server that targets GPUs and AMD NPUs with OpenAI-style APIs.**

Lemonade is a local AI server with OpenAI, Anthropic and Ollama-compatible APIs on port 13305 that runs GGUF, FLM and ONNX models, Whisper transcription, Kokoro speech and Stable Diffusion images. It picks the backend for the hardware: llama.cpp on CPU, CUDA, Vulkan, ROCm or Metal, plus AMD XDNA2 NPU paths for Ryzen AI. Packages exist for Windows, macOS, Debian, Fedora, Ubuntu, Arch, Snap and Docker.

- **+** NPU backends for AMD XDNA2 (Ryzen AI) alongside CUDA, ROCm, Vulkan, Metal
- **+** Chat, speech-to-text, text-to-speech, image and audio generation in one server
- **+** Native packages: msi, pkg, deb, rpm, Arch, Snap, PPA, Docker
- **+** Model aliases enable active-standby failover between models
- **−** Many engines (vllm, ds4, openmoss, trellis) are marked experimental
- **−** NPU support covers AMD XDNA2 only
- **−** macOS gets Metal only; several backends are Windows or Linux only
- **−** Cloud offload to OpenAI-compatible providers is experimental

<sub>GPU optional · Docker · Models: GGUF, FLM and ONNX LLMs (e.g. Gemma 4, Qwen3), Whisper, Kokoro, SDXL-Turbo · port 13305 · [Repo](https://github.com/lemonade-sdk/lemonade)</sub>

<a name="exo"></a>
### #&#8288;8 [exo](https://github.com/exo-explore/exo) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: weak (12) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · Apache-2.0 · Aug 2026</sub>

**Distributed LLM inference across Macs and other devices, MLX-based.**

exo joins devices on a network into one inference cluster, splitting a model across them with pipeline or tensor parallelism based on a live view of topology. It uses MLX for inference and exposes OpenAI Chat Completions, Claude Messages, OpenAI Responses and Ollama-compatible APIs plus a built-in dashboard on port 52415. On Macs with Thunderbolt 5 and macOS 26.2 or later, it can use RDMA between nodes.

- **+** Runs models too large for one machine by sharding across devices
- **+** Devices discover each other automatically, no manual cluster config
- **+** Serves OpenAI, Claude Messages, Responses and Ollama-style APIs
- **+** Tensor parallelism reported up to 1.8x on 2 devices, 3.2x on 4
- **−** On Linux, inference currently runs on CPU only; GPU support is in development
- **−** RDMA needs macOS 26.2+, Thunderbolt 5, a Recovery-mode setting and identical OS versions
- **−** Source install needs Rust nightly, Node and uv; no Docker image detected
- **−** Models are MLX-format; GGUF support is not mentioned in the README

<sub>GPU optional · Needs uv, Node.js 18+, Rust nightly, MLX, macmon (macOS) · Models: MLX, HuggingFace custom models · port 52415 · [Repo](https://github.com/exo-explore/exo) · [📖 Docs ↗](https://github.com/exo-explore/exo/blob/main/docs/api.md)</sub>

<a name="llama-swap"></a>
### #&#8288;9 [llama-swap](https://github.com/mostlygeek/llama-swap) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (90) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · MIT · Oct 2026</sub>

**Go proxy that hot-swaps local model servers per request.**

llama-swap is one Go binary that proxies OpenAI and Anthropic API calls to local servers (llama-server, vLLM, stable-diffusion.cpp, whisper.cpp) and starts, stops or swaps the right one per model ID from a YAML file. It adds a web UI, log streaming, Prometheus metrics, API keys, TTL unload and a matrix DSL for concurrent models. Unified Docker images bundle the servers for CUDA and Vulkan.

- **+** One binary, one YAML file, zero dependencies
- **+** Hot-swaps any OpenAI or Anthropic-compatible upstream per model ID, with ttl unload
- **+** Unified images bundle llama-server, stable-diffusion.cpp, whisper.cpp, audio.cpp
- **+** Web UI with playground, token metrics, request inspection and live logs
- **−** Basic mode runs one model at a time; concurrency needs the matrix DSL
- **−** Python servers like vLLM or tabbyAPI should run in containers for clean SIGTERM
- **−** nginx needs proxy_buffering off or SSE streaming breaks
- **−** Container listen address must stay 0.0.0.0 when publishing ports

<sub>GPU optional · Docker · Needs an upstream inference server (llama-server, vLLM, etc.) · Models: any model served by the configured upstream (GGUF via llama-server, etc.) · port 8080 · [Repo](https://github.com/mostlygeek/llama-swap)</sub>

<a name="xinference"></a>
### #&#8288;10 [Xinference](https://github.com/xorbitsai/inference) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU optional · Models: vLLM, ggml, llama.cpp (xllamacpp), TensorRT, embedding models · port 9997 · [Repo](https://github.com/xorbitsai/inference) · [📖 Docs ↗](https://inference.readthedocs.io/) · [🌐 Site ↗](https://xinference.co)</sub>

<a name="mistral-rs"></a>
### #&#8288;11 [mistral.rs](https://github.com/ericlbuehler/mistral.rs) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: fair (74) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker · Models: Hugging Face safetensors, GGUF, UQFF, Qwen3, Gemma 4, Muse Glimmer, DiffusionGemma and 45+ architectures · port 1234 · [Repo](https://github.com/ericlbuehler/mistral.rs) · [📖 Docs ↗](https://docs.mistralrs.dev/)</sub>

<a name="text-generation-webui"></a>
### #&#8288;12 [Text Generation Web UI](https://github.com/oobabooga/textgen) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: weak (12) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · AGPL-3.0 · Aug 2026</sub>

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

<sub>GPU optional · Docker + Compose · Models: GGUF via llama.cpp and ik_llama.cpp, Transformers safetensors, EXL3 via ExLlamaV3, TensorRT-LLM · port 7860 · [Repo](https://github.com/oobabooga/textgen)</sub>

<a name="ktransformers"></a>
### #&#8288;13 [KTransformers](https://github.com/kvcache-ai/ktransformers) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: fair (78) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Oct 2026</sub>

**CPU-GPU hybrid inference and fine-tuning for very large MoE models.**

KTransformers is a research framework for CPU-GPU heterogeneous inference and fine-tuning of large MoE models. Its kt-kernel package provides Intel AMX and AVX512/AVX2 INT4/INT8 kernels with NUMA-aware expert placement, so DeepSeek-V3/R1, Kimi K2.x and GLM-5.x run with hot experts on GPU and cold ones on CPU, served through SGLang. A LlamaFactory integration fine-tunes the same models with LoRA or full parameters.

- **+** DeepSeek-R1 class models on one 24 GB GPU plus large host RAM
- **+** Day-0 support for DeepSeek-V4, Kimi K2.x, GLM-5.x and MiniMax-M3
- **+** LoRA and full fine-tuning of MoE models on 4x RTX 4090 via LlamaFactory
- **+** Ascend NPU, AMD ROCm and Intel Arc paths beyond NVIDIA
- **−** Serving goes through SGLang (sglang-kt); the standalone framework is archived
- **−** DeepSeek-R1 example needs 382 GB DRAM alongside 24 GB VRAM
- **−** Fastest kernels need Intel AMX or AVX512; AVX2 support is newer
- **−** Research project; some docs and support channels are Chinese-only

<sub>GPU required · Docker · Needs SGLang (serving), LLaMA-Factory (fine-tuning) · Models: DeepSeek-V3/R1/V4-Flash, Kimi K2 to K2.6, GLM-5 to 5.3, MiniMax-M2.x/M3, Qwen3-MoE, Qwen3-Next · [Repo](https://github.com/kvcache-ai/ktransformers) · [📖 Docs ↗](https://kvcache-ai.github.io/ktransformers/)</sub>

<a name="triton-inference-server"></a>
### #&#8288;14 [Triton Inference Server](https://github.com/triton-inference-server/server) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · BSD-3-Clause · Oct 2026</sub>

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

<sub>GPU optional · Docker · Models: TensorRT, PyTorch, ONNX, OpenVINO, Python, RAPIDS FIL backends · [Repo](https://github.com/triton-inference-server/server) · [🌐 Site ↗](https://developer.nvidia.com/nvidia-triton-inference-server)</sub>

<a name="gpustack"></a>
### #&#8288;15 [GPUStack](https://github.com/gpustack/gpustack) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU required · Compose · Models: catalog models (e.g. Qwen3.5-0.8B) via vLLM, SGLang, TensorRT-LLM, LLM, voice, image and video models · port 80 · [Repo](https://github.com/gpustack/gpustack) · [📖 Docs ↗](https://docs.gpustack.ai)</sub>

<a name="lmdeploy"></a>
### #&#8288;16 [LMDeploy](https://github.com/internlm/lmdeploy) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: some setup (33) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU required · Docker · Models: Llama 1-4, Qwen1.5-3.5, InternLM2/3, DeepSeek V2-V4, GLM-4/5, Mixtral, Gemma, Phi-3/4, gpt-oss, VLMs: InternVL, Qwen-VL, LLaVA, DeepSeek-VL, CogVLM, MiniCPM-V, Molmo, Gemma3, Llama4 · [Repo](https://github.com/internlm/lmdeploy) · [📖 Docs ↗](https://lmdeploy.readthedocs.io/en/latest/)</sub>

<a name="llamafile"></a>
### #&#8288;17 [llamafile](https://github.com/mozilla-ai/llamafile) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: fair (80) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · custom license · Oct 2026</sub>

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

<sub>GPU optional · Models: GGUF (bundled or external), e.g. Qwen3.5-0.8B · [Repo](https://github.com/mozilla-ai/llamafile) · [📖 Docs ↗](https://docs.mozilla.ai/llamafile)</sub>

<a name="text-embeddings-inference"></a>
### #&#8288;18 [Text Embeddings Inference](https://github.com/huggingface/text-embeddings-inference) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: patchy (49) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU optional · Docker · Models: Qwen3-Embedding, gte-Qwen2, multilingual-e5, embeddinggemma, arctic-embed, nomic-embed, ModernBERT, jina-embeddings-v2, bge-reranker, gte rerankers · port 3000 · [Repo](https://github.com/huggingface/text-embeddings-inference) · [📖 Docs ↗](https://huggingface.github.io/text-embeddings-inference)</sub>

<a name="tabbyapi"></a>
### #&#8288;19 [TabbyAPI](https://github.com/theroyallab/tabbyapi) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: fair (57) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Oct 2026</sub>

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

<sub>GPU required · Docker + Compose · Needs ExLlamaV3, NVIDIA container toolkit (Docker) · Models: EXL3, FP16, BF16 · port 5000 · [Repo](https://github.com/theroyallab/tabbyapi) · [📖 Docs ↗](https://theroyallab.github.io/tabbyAPI)</sub>

<a name="openllm"></a>
### #&#8288;20 [OpenLLM](https://github.com/bentoml/openllm) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (44) · Freshness: recent (59) · Maintenance: weak (25) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · May 2026</sub>

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

<sub>GPU required · Models: Llama 3.1/3.2/3.3/4, Qwen2.5, Qwen2.5-Coder, QwQ, Mistral, Mistral Large, Pixtral, Phi-4, Gemma 2/3, Jamba 1.5, DeepSeek R1 · port 3000 · [Repo](https://github.com/bentoml/openllm)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
