# 🧠 Model serving — reviews

Inference engines and model servers that expose local models over an API. Back to the [leaderboard](../README.md#-model-serving).

<a name="ollama"></a>
### 🥇 [Ollama](https://github.com/ollama/ollama) <sub>⭐ 183k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker · Models: Ollama library models (e.g. gemma4), GGUF via llama.cpp · port 11434 · [Repo](https://github.com/ollama/ollama) · [📖 Docs](https://docs.ollama.com/quickstart) · [🌐 Site](https://ollama.com)</sub>

<a name="llama-cpp"></a>
### 🥈 [llama.cpp](https://github.com/ggml-org/llama.cpp) <sub>⭐ 131k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Models: GGUF models from Hugging Face (e.g. Qwen3.5-0.8B-GGUF) · [Repo](https://github.com/ggml-org/llama.cpp) · [🌐 Site](https://llama.app)</sub>

<a name="vllm"></a>
### 🥉 [vLLM](https://github.com/vllm-project/vllm) <sub>⭐ 93k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU optional · Models: 200+ Hugging Face architectures: Llama, Qwen, Gemma, Mixtral, DeepSeek-V3, GPT-OSS, LLaVA, Qwen-VL, E5-Mistral · [Repo](https://github.com/vllm-project/vllm) · [📖 Docs](https://docs.vllm.ai) · [🌐 Site](https://vllm.ai)</sub>

<a name="localai"></a>
### 4 [LocalAI](https://github.com/mudler/LocalAI) <sub>⭐ 49k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker + Compose · Needs PostgreSQL and NATS (distributed mode only) · Models: GGUF via llama.cpp, vLLM, SGLang, transformers, MLX, diffusers, whisper.cpp backends, models from gallery, Hugging Face, Ollama registry, OCI images, YAML · port 8080 · [Repo](https://github.com/mudler/LocalAI) · [📖 Docs](https://localai.io/basics/getting_started/) · [🌐 Site](https://localai.io/)</sub>

<a name="text-generation-webui"></a>
### 5 [Text Generation Web UI](https://github.com/oobabooga/textgen) <sub>⭐ 48k · AGPL-3.0 · Aug 2026</sub>

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

<sub>GPU optional · Models: GGUF via llama.cpp and ik_llama.cpp, Transformers safetensors, EXL3 via ExLlamaV3, TensorRT-LLM · port 7860 · [Repo](https://github.com/oobabooga/textgen)</sub>

<a name="sglang"></a>
### 6 [SGLang](https://github.com/sgl-project/sglang) <sub>⭐ 37k · Apache-2.0 · Oct 2026</sub>

**Inference framework for LLMs, VLMs and diffusion models on many accelerators.**

SGLang is an inference framework for language, vision-language and diffusion models aimed at agentic workloads, RL rollouts and large-scale serving, shipped as a Docker image or Python package. It runs on NVIDIA (A100 to B300, RTX 30/40/50, Jetson), AMD MI300, Google TPU, Intel Arc and Xeon, Apple Silicon, Ascend and Moore Threads. SGLang Diffusion adds image and video generation.

- **+** Hardware from NVIDIA and AMD to TPU, Intel, Apple Silicon and Ascend NPUs
- **+** Hierarchical KV cache across GPU, host memory and storage (HiCache, Mooncake, LMCache)
- **+** Diffusion image and video generation in the same package
- **+** Integrations with verl, slime, AReaL, Ray Serve, llm-d and NVIDIA Dynamo
- **−** README has no launch command; quickstart and cookbook are external
- **−** uv install requires --prerelease=allow
- **−** No port, VRAM or model-size guidance in the README
- **−** Trainium, Cambricon and Qualcomm support still in progress

<sub>GPU optional · Models: large language, vision-language and diffusion models (see cookbook) · [Repo](https://github.com/sgl-project/sglang) · [📖 Docs](https://docs.sglang.io/) · [🌐 Site](https://www.sglang.io/)</sub>

<a name="llamafile"></a>
### 7 [llamafile](https://github.com/mozilla-ai/llamafile) <sub>⭐ 26k · NOASSERTION · Sep 2026</sub>

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

<sub>GPU optional · Models: GGUF (bundled or external), e.g. Qwen3.5-0.8B · [Repo](https://github.com/mozilla-ai/llamafile) · [📖 Docs](https://docs.mozilla.ai/llamafile)</sub>

<a name="ktransformers"></a>
### 8 [KTransformers](https://github.com/kvcache-ai/ktransformers) <sub>⭐ 20k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU required · Needs SGLang (serving), LLaMA-Factory (fine-tuning) · Models: DeepSeek-V3/R1/V4-Flash, Kimi K2 to K2.6, GLM-5 to 5.3, MiniMax-M2.x/M3, Qwen3-MoE, Qwen3-Next · [Repo](https://github.com/kvcache-ai/ktransformers) · [📖 Docs](https://kvcache-ai.github.io/ktransformers/)</sub>

<a name="openllm"></a>
### 9 [OpenLLM](https://github.com/bentoml/OpenLLM) <sub>⭐ 13k · Apache-2.0 · May 2026</sub>

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

<sub>GPU required · Models: Llama 3.1/3.2/3.3/4, Qwen2.5, Qwen2.5-Coder, QwQ, Mistral, Mistral Large, Pixtral, Phi-4, Gemma 2/3, Jamba 1.5, DeepSeek R1 · port 3000 · [Repo](https://github.com/bentoml/OpenLLM)</sub>

<a name="triton-inference-server"></a>
### 10 [Triton Inference Server](https://github.com/triton-inference-server/server) <sub>⭐ 11k · BSD-3-Clause · Oct 2026</sub>

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

<sub>GPU optional · Models: TensorRT, PyTorch, ONNX, OpenVINO, Python, RAPIDS FIL backends · [Repo](https://github.com/triton-inference-server/server) · [🌐 Site](https://developer.nvidia.com/nvidia-triton-inference-server)</sub>

<a name="xinference"></a>
### 11 [Xinference](https://github.com/xorbitsai/inference) <sub>⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

**Serves LLM, embedding, speech and image models behind one OpenAI-style API.**

Xinference serves LLM, embedding, rerank, speech, image and multimodal models behind one OpenAI-compatible API, RPC, CLI and web UI, via pip or the xprobe/xinference image on port 9997. It runs vLLM, its own Xllamacpp llama.cpp binding and other engines across GPUs and CPUs, and scales to multi-node clusters with a Helm chart. Version 3.0 brought breaking changes.

- **+** One API for LLM, embedding, rerank, speech, image and multimodal models
- **+** Auto-batching of concurrent requests; Xllamacpp adds continuous batching to llama.cpp
- **+** Multi-node distributed inference with a Helm chart for Kubernetes
- **+** Built-in model catalog with frequent additions (OCR, TTS, image editing)
- **−** Docker image targets NVIDIA GPUs; CPU and Metal need a pip install
- **−** 3.0.0 release carries breaking changes and migration notes
- **−** Commercial Enterprise edition exists alongside the community edition
- **−** README gives no RAM or VRAM guidance

<sub>GPU optional · Models: built-in catalog of LLM, embedding, rerank, speech, image and video models, custom models, engines: vLLM, Xllamacpp (llama.cpp), transformers, TensorRT · port 9997 · [Repo](https://github.com/xorbitsai/inference) · [📖 Docs](https://inference.readthedocs.io/) · [🌐 Site](https://xinference.co)</sub>

<a name="lmdeploy"></a>
### 12 [LMDeploy](https://github.com/InternLM/lmdeploy) <sub>⭐ 8.1k · Apache-2.0 · Sep 2026</sub>

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

<sub>GPU required · Models: Llama 1-4, Qwen1.5-3.5, InternLM2/3, DeepSeek V2-V4, GLM-4/5, Mixtral, Gemma, Phi-3/4, gpt-oss, VLMs: InternVL, Qwen-VL, LLaVA, DeepSeek-VL, CogVLM, MiniCPM-V, Molmo, Gemma3, Llama4 · [Repo](https://github.com/InternLM/lmdeploy) · [📖 Docs](https://lmdeploy.readthedocs.io/en/latest/)</sub>

<a name="mistral-rs"></a>
### 13 [mistral.rs](https://github.com/EricLBuehler/mistral.rs) <sub>⭐ 7.7k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker · Models: Hugging Face safetensors, GGUF, UQFF, Qwen3, Gemma 4, Muse Glimmer, DiffusionGemma and 45+ architectures · port 1234 · [Repo](https://github.com/EricLBuehler/mistral.rs) · [📖 Docs](https://docs.mistralrs.dev/)</sub>

<a name="llama-swap"></a>
### 14 [llama-swap](https://github.com/mostlygeek/llama-swap) <sub>⭐ 5.9k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Needs an upstream inference server (llama-server, vLLM, etc.) · Models: any model served by the configured upstream (GGUF via llama-server, etc.) · port 8080 · [Repo](https://github.com/mostlygeek/llama-swap)</sub>

<a name="lemonade"></a>
### 15 [Lemonade](https://github.com/lemonade-sdk/lemonade) <sub>⭐ 5.8k · Apache-2.0 · Oct 2026</sub>

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

<a name="gpustack"></a>
### 16 [GPUStack](https://github.com/gpustack/gpustack) <sub>⭐ 5.8k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU required · Models: catalog models (e.g. Qwen3.5-0.8B) via vLLM, SGLang, TensorRT-LLM, LLM, voice, image and video models · port 80 · [Repo](https://github.com/gpustack/gpustack) · [📖 Docs](https://docs.gpustack.ai)</sub>

<a name="text-embeddings-inference"></a>
### 17 [Text Embeddings Inference](https://github.com/huggingface/text-embeddings-inference) <sub>⭐ 5.1k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU optional · Docker · Models: Qwen3-Embedding, gte-Qwen2, multilingual-e5, embeddinggemma, arctic-embed, nomic-embed, ModernBERT, jina-embeddings-v2, bge-reranker, gte rerankers · port 3000 · [Repo](https://github.com/huggingface/text-embeddings-inference) · [📖 Docs](https://huggingface.github.io/text-embeddings-inference)</sub>

<a name="tabbyapi"></a>
### 18 [TabbyAPI](https://github.com/theroyallab/tabbyAPI) <sub>⭐ 1.5k · AGPL-3.0 · Oct 2026</sub>

**OpenAI-compatible API server for ExLlamaV3 models.**

TabbyAPI is a FastAPI server exposing an OpenAI-compatible API for the ExLlamaV3 backend, serving EXL3 and FP16/BF16 models with continuous batching via paged attention on NVIDIA Ampere or newer, speculative decoding, constrained output and tool calling. A CUDA Docker image runs on port 5000 and needs --shm-size=8g. The maintainers call it a hobby project not meant for production.

- **+** Official API server for ExLlamaV3 with EXL3 quantized models
- **+** Continuous batching with paged attention; speculative decoding via draft models
- **+** JSON schema, regex and EBNF constrained output plus OpenAI-style tool calling
- **+** Optional embeddings stack in the latest-extras image
- **−** Marked hobby project, rolling release, not for production servers
- **−** NVIDIA only; batching needs Ampere or newer; Docker needs --shm-size=8g
- **−** EXL3 and FP16/BF16 only; no GGUF
- **−** AGPL-3.0 license

<sub>GPU required · Models: EXL3 (recommended), FP16/BF16 Hugging Face models · port 5000 · [Repo](https://github.com/theroyallab/tabbyAPI) · [📖 Docs](https://theroyallab.github.io/tabbyAPI)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
