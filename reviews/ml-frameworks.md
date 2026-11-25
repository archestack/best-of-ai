# 🔬 ML frameworks and libraries reviews · Best of Open-Source AI

The libraries models are built and run with: tensor frameworks, model zoos and the tooling around them. Back to the [leaderboard](../README.md#-ml-frameworks-and-libraries).

<sub>🌐 Also on the web: [ML frameworks and libraries on archestack.com](https://archestack.com/best-of-ai/ml-frameworks/), each project on its own page.</sub>

<a name="transformers"></a>
### 🥇 [transformers](https://github.com/huggingface/transformers) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 169k · Apache-2.0 · Nov 2026</sub>

**Model-definition library for pretrained text, vision, audio and multimodal models.**

Transformers defines model architectures for text, vision, audio, video and multimodal models, and loads checkpoints from the Hugging Face Hub (README cites 1M+). It offers a high-level Pipeline API for inference, a training API built for PyTorch, and a `transformers chat` and `transformers serve` CLI. Other training frameworks and inference engines reuse its model definitions.

- **+** Pipeline API covers text, audio, vision and multimodal tasks in a few lines
- **+** Model definitions are reused by vLLM, SGLang, TGI, Axolotl, Unsloth and DeepSpeed
- **+** Loads from 1M+ Hub checkpoints across hundreds of architectures
- **+** Apache-2.0, with frequent releases and recent commits
- **−** Not a modular toolbox for neural nets; model files avoid shared abstractions on purpose
- **−** Training API targets its own PyTorch models; generic loops need Accelerate
- **−** Requires Python 3.11+ and PyTorch 2.6+
- **−** Pipeline inference is not a production server; serving needs `transformers serve` or another engine

<sub>GPU optional · Docker · Needs Python 3.11+, PyTorch 2.6+, Hugging Face Hub · Models: PyTorch, Hugging Face Hub checkpoints · [Repo](https://github.com/huggingface/transformers) · [📖 Docs ↗](https://huggingface.co/docs/transformers/index) · [🌐 Site ↗](https://huggingface.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transformers/)</sub>

<a name="ultralytics"></a>
### 🥈 [ultralytics](https://github.com/ultralytics/ultralytics) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · AGPL-3.0 · Nov 2026</sub>

**Python library and CLI for training and running YOLO vision models.**

Ultralytics provides the YOLO model family (YOLOv3 through YOLO26) with a `yolo` CLI and Python API for training, validation, prediction, tracking and export. Tasks covered are detection, instance and semantic segmentation, depth estimation, classification, pose and oriented boxes. Pretrained weights download automatically on first use, and models export to formats such as ONNX.

- **+** One API and CLI covers train, val, predict, track and export across seven vision tasks
- **+** Pretrained YOLO26 n/s/m/l/x weights with published COCO mAP and CPU/T4 latency tables
- **+** Installs via pip, Conda or Docker; reproduction commands given for benchmark numbers
- **+** Active: release and commit within the last two days
- **−** AGPL-3.0; commercial use requires a separate Enterprise License
- **−** Vision only; no LLM or language model support
- **−** YOLO27 is listed as coming soon, with no models or launch date

<sub>GPU optional · Docker · Needs Python>=3.8, PyTorch>=1.8 · Models: YOLOv3 to YOLO26, PyTorch .pt, ONNX export, TensorRT export · [Repo](https://github.com/ultralytics/ultralytics) · [📖 Docs ↗](https://docs.ultralytics.com) · [🌐 Site ↗](https://www.ultralytics.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ultralytics/)</sub>

<a name="pytorch-image-models"></a>
### 🥉 [pytorch-image-models](https://github.com/huggingface/pytorch-image-models) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Nov 2026</sub>

**PyTorch library of image models, pretrained weights and training scripts.**

timm is a Python library of image model architectures (ViT, EVA, ConvNeXt, Swin, EfficientNet and many more) with pretrained weights loaded from the Hugging Face Hub. It also ships optimizers, LR schedulers, data loaders and augmentations, plus reference train, validate, inference and sweep scripts for reproducing ImageNet results. Recent releases add multi-label training, NaFlexViT variable-resolution input, and forward_intermediates support in every model.

- **+** Broad model zoo with pretrained weights for nearly every listed architecture family
- **+** Includes train.py, validate.py, inference.py and sweep.py for reproducible ImageNet-style runs
- **+** forward_intermediates and prune_intermediate_layers supported across all models
- **+** Large optimizer set, including Muon, Kron, LAMB and foreach implementations
- **−** Image models only; no text or LLM support
- **−** Some model variants ship without pretrained weights
- **−** RoPE and low-precision fixes can change existing model outputs between releases
- **−** Jan 2026 compat break in ParallelScalingBlock bias handling may affect downstream code

<sub>GPU optional · Needs PyTorch · Models: PyTorch, Hugging Face Hub weights · [Repo](https://github.com/huggingface/pytorch-image-models) · [📖 Docs ↗](https://huggingface.co/docs/timm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-image-models/)</sub>

<a name="pytorch"></a>
### #&#8288;4 [pytorch](https://github.com/pytorch/pytorch) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 106k · custom license · Nov 2026</sub>

**Python tensor library with GPU support and tape-based autograd.**

PyTorch provides NumPy-style tensors that run on CPU or GPU, plus a reverse-mode autograd system and torch.nn for building neural networks imperatively in Python. It supports CUDA, AMD ROCm and Intel GPU backends, and layers can be extended in Python or through a C++ extension API. Binaries install via pip or Conda, or it can be built from source.

- **+** Dynamic graphs run line by line, so stack traces point at user code
- **+** GPU backends for NVIDIA CUDA, AMD ROCm (Linux only) and Intel GPUs
- **+** Custom layers can be written in Python or C++ via an extension API
- **+** Pip and Conda binaries plus pre-built Docker images on Docker Hub
- **−** Source build needs a C++20 compiler, 10 GB disk and 30-60 minutes first time
- **−** ROCm is Linux only; Windows distributed support is a prototype
- **−** Jetson wheels are maintained outside the project and need JetPack 4.2 or later
- **−** Low-level library only; no model serving or UI included

<sub>GPU optional · Docker · Needs Python 3.11+ (source build), C++20 compiler (gcc 11.3+), CUDA, cuDNN 9.0+, ROCm, Intel MKL · Models: Python-defined torch.nn models · [Repo](https://github.com/pytorch/pytorch) · [📖 Docs ↗](https://pytorch.org/docs/stable/torch.html) · [🌐 Site ↗](https://pytorch.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch/)</sub>

<a name="supervision"></a>
### #&#8288;5 [supervision](https://github.com/roboflow/supervision) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 52k · MIT · Nov 2026</sub>

**Python toolkit for annotating detections, tracking and managing vision datasets.**

Supervision is a Python library that wraps model output in a common sv.Detections object, with connectors for Ultralytics, Transformers, MMDetection and Inference. It provides annotators for drawing boxes and other overlays, and utilities to load, split, merge and convert datasets in YOLO, Pascal VOC and COCO formats. It does not ship detection models itself; it sits around whichever model you use.

- **+** Model-agnostic: sv.Detections connectors for Ultralytics, Transformers, MMDetection and Inference
- **+** Converts datasets between YOLO, Pascal VOC and COCO, with split and merge helpers
- **+** Configurable annotators for drawing detections on images and video frames
- **+** MIT license, installs with pip on Python 3.10 or newer
- **−** Does not include detection models; you supply and run your own
- **−** Inference connector example needs a Roboflow API key
- **−** Library only, with no UI or server; you write the application code

<sub>Needs Python>=3.10 · Models: Ultralytics, Transformers, MMDetection, Roboflow Inference, rfdetr · [Repo](https://github.com/roboflow/supervision) · [▶️ Demo ↗](https://huggingface.co/spaces/Roboflow/Annotators) · [📖 Docs ↗](https://supervision.roboflow.com) · [🌐 Site ↗](https://supervision.roboflow.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/supervision/)</sub>

<a name="kornia"></a>
### #&#8288;6 [kornia](https://github.com/kornia/kornia) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

**Differentiable computer vision and geometry operators for PyTorch.**

Kornia is a PyTorch library of over 500 differentiable image processing, augmentation and geometry ops, including filters, homographies, camera models, epipolar geometry and Lie groups. It also ships pretrained models such as LoFTR, LightGlue, SAM and YuNet, plus an ONNXSequential helper for chaining ONNX models. The README publishes per-module float16/bfloat16 test status and known failures.

- **+** Batched, differentiable ops that run on GPU tensors inside PyTorch training pipelines
- **+** Covers filters, augmentation, feature matching, cameras, epipolar geometry and Lie groups in one library
- **+** Publishes CPU and CUDA test pass rates and known half-precision failures per module
- **+** Installs with pip install kornia; Apache-2.0 licensed
- **−** Half precision is incomplete: about 95% pass in float16 and bfloat16 on CPU
- **−** Epipolar solvers raise NotImplementedError in half precision on CPU
- **−** No CI job covers CUDA or MPS half precision; CUDA results are a local run
- **−** Roadmap favors conformance and benchmarks over new API growth

<sub>GPU optional · Needs PyTorch 2.5.1+, kornia_rs (used in quick start), onnx (optional extra) · Models: PyTorch, ONNX, LoFTR, LightGlue, SAM · [Repo](https://github.com/kornia/kornia) · [▶️ Demo ↗](https://www.kornia.org/playground/) · [📖 Docs ↗](https://kornia.readthedocs.io) · [🌐 Site ↗](https://www.kornia.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kornia/)</sub>

<a name="genesis-world"></a>
### #&#8288;7 [genesis-world](https://github.com/genesis-embodied-ai/genesis-world) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Nov 2026</sub>

**Python multi-physics simulator and renderer for robotics and physical AI research.**

Genesis World is a Python simulation platform that couples rigid, FEM, MPM, SPH and PBD solvers in one scene, with a Python-to-GPU compiler (Quadrants) targeting CUDA, ROCm, Metal, Vulkan, x86 and ARM64. It loads URDF, MJCF, OBJ, GLB and USD assets, supports parallel and heterogeneous environments, sensors, and three renderers (Nyx, Luisa, Pyrender).

- **+** Rigid, FEM, MPM, SPH, PBD and IPC solvers share one scene and state
- **+** Compiler backends cover CUDA, ROCm, Metal, Vulkan and CPU (x86, ARM64)
- **+** Many runnable examples: sensors (IMU, lidar, tactile), controllers, domain randomization, drones
- **+** Three render paths as camera sensors, including 3D Gaussian splat support in Nyx
- **−** Requires Python 3.12 to 3.14 and a separate PyTorch install
- **−** IPC solver (pyuipc) limited to Linux/Windows x86 with an NVIDIA GPU
- **−** Nyx renderer and IPC demos need extra packages beyond the base install
- **−** Renamed from Genesis; older tutorials and package names may not match

<sub>GPU optional · Needs PyTorch, Python>=3.12,<3.15, pyuipc (optional, IPC solver), gs-nyx (optional, Nyx renderer) · Models: URDF, MJCF, OBJ, GLB, USD · [Repo](https://github.com/genesis-embodied-ai/genesis-world) · [📖 Docs ↗](https://genesis-world.readthedocs.io/en/latest/) · [🌐 Site ↗](https://www.genesis.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/genesis-world/)</sub>

<a name="onnx"></a>
### #&#8288;8 [onnx](https://github.com/onnx/onnx) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Nov 2026</sub>

**Open model format and operator spec for exchanging ML models between frameworks.**

ONNX defines an extensible computation graph format, built-in operators and standard data types for deep learning and traditional ML models. The Python package (pip install onnx) provides APIs to build, load and check models, plus shape and type inference and opset version conversion. The spec focuses on inference (scoring); runtimes and converters live in other projects.

- **+** Vendor-neutral spec with documented IR, operator set and versioning rules
- **+** Installs from PyPI; abi3 wheels work across Python 3.12 and later
- **+** Includes shape and type inference and opset version conversion utilities
- **+** Build workflows set SOURCE_DATE_EPOCH for reproducible-build comparison
- **−** Not a runtime; running models needs a separate inference engine
- **−** Scope is inference; training is not a focus
- **−** Graph optimization lives in a separate repository (onnx/optimizer)
- **−** Converters from source frameworks are separate projects, not in this repo

<sub>no GPU · Models: ONNX · [Repo](https://github.com/onnx/onnx) · [📖 Docs ↗](https://onnx.ai/onnx/) · [🌐 Site ↗](https://onnx.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onnx/)</sub>

<a name="burn"></a>
### #&#8288;9 [burn](https://github.com/tracel-ai/burn) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

**Rust tensor library and deep learning framework for training and inference.**

Burn is a Rust tensor library and deep learning framework with dynamic graphs, autodiff and automatic kernel fusion. Backends built on CubeCL target CUDA, ROCm, Metal, Vulkan, WebGPU and CPU, plus a pure-Rust Flex backend for Wasm and no_std. The same model code is used for training and deployment, and ONNX, PyTorch and Safetensors weights can be imported.

- **+** Same code trains and runs inference; no export step to ONNX or other runtimes
- **+** Backends for CUDA, ROCm, Metal, Vulkan, WebGPU, CPU, Wasm and no_std
- **+** Swap backends at runtime via Device; autodiff and fusion work as decorators
- **+** Terminal training dashboard built on Ratatui, no external service needed
- **−** Rust only; smaller ecosystem and model zoo than PyTorch
- **−** ONNX import supports only a limited set of operators
- **−** Remote execution backend is marked Beta
- **−** LibTorch backend was deprecated in 0.22.0 and removed from main

<sub>GPU optional · Needs Rust toolchain · Models: ONNX (import), PyTorch weights, Safetensors · [Repo](https://github.com/tracel-ai/burn) · [📖 Docs ↗](https://burn.dev/docs/burn) · [🌐 Site ↗](https://burn.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/burn/)</sub>

<a name="diffusers"></a>
### #&#8288;10 [diffusers](https://github.com/huggingface/diffusers) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Nov 2026</sub>

**PyTorch library of diffusion pipelines and schedulers for image generation.**

Diffusers is a Python library from Hugging Face for running and training diffusion models. It provides pipelines loaded with from_pretrained, interchangeable noise schedulers, and pretrained model classes that can be combined into custom systems. It covers text-to-image, image-to-image, inpainting, super resolution and unconditional generation, plus audio and 3D molecule structures.

- **+** Loads any of 30,000+ Hub checkpoints with a few lines via from_pretrained
- **+** Schedulers, models and pipelines are separate, so custom sampling loops are possible
- **+** Docs include training and memory/speed optimization guides
- **+** Used by InvokeAI, kohya_ss and BentoML, among 14,000+ repositories
- **−** Library only: no web UI or HTTP server included
- **−** README documents PyTorch installs only
- **−** README gives no VRAM or RAM figures per model
- **−** Quickstart assumes CUDA; Apple Silicon is in a separate guide

<sub>GPU optional · Docker · Needs PyTorch · Models: Stable Diffusion, DDPM, ControlNet, InstructPix2Pix, DeepFloyd IF · [Repo](https://github.com/huggingface/diffusers) · [📖 Docs ↗](https://huggingface.co/docs/diffusers/quicktour) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/diffusers/)</sub>

<a name="mlx"></a>
### #&#8288;11 [mlx](https://github.com/ml-explore/mlx) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Nov 2026</sub>

**NumPy-style array framework for machine learning on Apple silicon.**

MLX is an array framework from Apple machine learning research with Python, C++, C and Swift APIs. It builds lazy, dynamic computation graphs, offers composable transforms for autodiff and vectorization, and includes PyTorch-like mlx.nn and mlx.optimizers packages. Arrays live in unified memory, so CPU and GPU ops share data without copies. Linux CUDA and CPU-only packages exist.

- **+** Python API follows NumPy; mlx.nn and mlx.optimizers follow PyTorch
- **+** Unified memory: CPU and GPU ops share arrays without transfers
- **+** Composable transforms for autodiff, vectorization and graph optimization
- **+** Python, C++, C and Swift APIs; installs via pip on macOS and Linux
- **−** Designed for Apple silicon; Linux CUDA and CPU backends are add-on installs
- **−** Example models live in a separate mlx-examples repo
- **−** Supported devices are only CPU and GPU per the README

<sub>GPU optional · Models: LLaMA, Stable Diffusion, Whisper, LoRA fine-tuning · [Repo](https://github.com/ml-explore/mlx) · [📖 Docs ↗](https://ml-explore.github.io/mlx/build/html/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlx/)</sub>

<a name="mediapipe"></a>
### #&#8288;12 [mediapipe](https://github.com/google-ai-edge/mediapipe) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · Apache-2.0 · Nov 2026</sub>

**On-device ML task APIs and a C++ pipeline framework for mobile, web and desktop.**

MediaPipe provides prebuilt Tasks APIs with pre-trained models for vision, audio, text, retrieval and LLM inference, targeting Android, iOS, web and Python. Underneath is MediaPipe Framework, a C++ graph system built from packets, graphs and calculators for custom perception pipelines. Input data is processed on device, though the Tasks APIs send performance and usage metrics to Google.

- **+** Prebuilt Tasks for vision, audio, text, retrieval and LLM inference, with ready-to-run models
- **+** Targets Android, iOS, web, Python and C++ from one project
- **+** Input data stays on device; no images, video or text sent to Google servers
- **+** MediaPipe Studio lets you test and benchmark solutions in the browser
- **−** Tasks APIs send performance and usage metrics to Google; app developers must obtain user consent
- **−** Framework layer requires learning packets, graphs and calculators, and a C++ build setup
- **−** README is a pointer page; real documentation lives on developers.google.com

<sub>GPU optional · Docker · Models: MediaPipe pre-trained models, LLM inference (genai) · [Repo](https://github.com/google-ai-edge/mediapipe) · [▶️ Demo ↗](https://google-ai-edge.github.io/mediapipe-samples-web/#/home) · [📖 Docs ↗](https://developers.google.com/edge/mediapipe/solutions) · [🌐 Site ↗](https://developers.google.com/edge/mediapipe) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mediapipe/)</sub>

<a name="netron"></a>
### #&#8288;13 [netron](https://github.com/lutzroeder/netron) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Nov 2026</sub>

**Viewer for neural network and machine learning model graphs.**

Netron opens model files and renders their layer graphs, with node attributes and tensor details. It reads ONNX, TensorFlow Lite, PyTorch, TorchScript, TensorFlow, Core ML, OpenVINO, Keras, Caffe, Darknet, Safetensors and NumPy, with experimental support for GGUF, MLIR, JAX and others. It runs in the browser, as a desktop app on macOS, Linux and Windows, or as a Python package.

- **+** Covers many formats: ONNX, TFLite, PyTorch, Core ML, OpenVINO, Keras, Safetensors and more
- **+** Hosted browser version at netron.app can open a model from a URL
- **+** Also ships as macOS, Linux and Windows installers and a pip package
- **+** MIT license
- **−** GGUF, MLIR, JAX, ncnn, MNN, PaddlePaddle and scikit-learn support is experimental
- **−** Viewer only: does not edit, convert or run models
- **−** No Docker image or compose file provided

<sub>no GPU · Models: ONNX, TensorFlow Lite, PyTorch, torch.export, ExecuTorch · [Repo](https://github.com/lutzroeder/netron) · [▶️ Demo ↗](https://netron.app) · [🌐 Site ↗](https://www.lutzroeder.com/ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/netron/)</sub>

<a name="flash-attention"></a>
### #&#8288;14 [flash-attention](https://github.com/dao-ailab/flash-attention) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · BSD-3-Clause · Nov 2026</sub>

**Fused GPU kernels for exact attention in PyTorch, FlashAttention 2 through 4.**

Official implementation of FlashAttention and FlashAttention-2 as CUDA and ROCm kernels exposed through a PyTorch Python API (flash_attn_func, varlen, and KV-cache variants). The repo also ships FlashAttention-3 (beta, Hopper) and FlashAttention-4 (CuTeDSL, Hopper and Blackwell). Supports causal masks, sliding window, ALiBi, MQA/GQA, and paged KV cache.

- **+** Official reference implementation with papers for FA1, FA2 and FA3
- **+** Covers NVIDIA (Ampere, Ada, Hopper, Blackwell via FA4) and AMD ROCm (CK and Triton backends)
- **+** Decoding-oriented API: in-place KV cache update, rotary, paged cache, GQA/MQA
- **+** Head dimensions up to 256 with fp16 and bf16; FP8 forward in FA3
- **−** Source build is slow without ninja: about 2h versus 3-5 minutes on 64 cores
- **−** FA3 is a beta, requires H100/H800 and CUDA 12.3 or newer
- **−** Linux only; Windows support is untested and unconfirmed
- **−** flash_attn_with_kvcache has no backward pass; Turing GPUs need a separate repo

<sub>GPU required · Needs PyTorch 2.2+, CUDA 12.0+ or ROCm 6.0+, ninja, packaging, psutil · Models: fp16, bf16, fp8 (FA3 forward), fp32 (ROCm Triton) · [Repo](https://github.com/dao-ailab/flash-attention) · [📖 Docs ↗](https://github.com/Dao-AILab/flash-attention/blob/main/usage.md) · [🌐 Site ↗](https://tridao.me/blog/2024/flash3/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flash-attention/)</sub>

<a name="deepface"></a>
### #&#8288;15 [deepface](https://github.com/serengil/deepface) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Nov 2026</sub>

**Python library for face verification, search and age/gender/emotion analysis.**

DeepFace wraps face detection, alignment, embedding and matching behind calls such as verify, find, analyze and represent. It supports models including VGG-Face, FaceNet, ArcFace, Dlib, SFace and Buffalo_L. It runs on ONNX Runtime by default, with optional TensorFlow or PyTorch backends. Embeddings can be registered in databases such as Postgres, Mongo, Pinecone and Milvus, and a gunicorn-served REST API is included.

- **+** Single-call API for verify, find, analyze, represent and extract_faces
- **+** Wraps 10 recognition models and many detectors, switchable by argument
- **+** ONNX Runtime default keeps the install to a few hundred MB
- **+** Database-backed search with ANN support across Postgres, Mongo, Qdrant and others
- **−** Race and gender prediction raise bias and ethics concerns in production use
- **−** Defaults are VGG-Face and the OpenCV detector, not the most accurate options
- **−** Browser UI is a separate repository, deepface-react-ui
- **−** Webcam stream function is a demo, not a production video pipeline

<sub>GPU optional · Docker + Compose · Needs onnxruntime, tensorflow (optional), pytorch (optional), gunicorn (API) · Models: VGG-Face, FaceNet, OpenFace, DeepFace, DeepID · [Repo](https://github.com/serengil/deepface) · [🌐 Site ↗](https://deepface.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepface/)</sub>

<a name="ray"></a>
### #&#8288;16 [ray](https://github.com/ray-project/ray) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · Apache-2.0 · Nov 2026</sub>

**Distributed Python runtime with libraries for data, training, tuning, RL and serving.**

Ray is a distributed runtime for Python built on tasks, actors and shared objects, so the same code can run on a laptop or a cluster. On top of the core it ships libraries for data processing (Data), distributed training (Train), hyperparameter tuning (Tune), reinforcement learning (RLlib) and model serving (Serve). It includes a dashboard and a distributed debugger, and runs on VMs, cloud providers and Kubernetes.

- **+** One runtime covers data loading, training, tuning, RL and serving in Python
- **+** Core primitives are small: tasks, actors and objects, for scaling arbitrary Python code
- **+** Runs on a laptop, any cluster, cloud providers and Kubernetes
- **+** Ships a dashboard and a distributed debugger for cluster apps
- **−** Python-centric; the README offers no path for non-Python applications
- **−** Several libraries to learn (Core, Data, Train, Tune, RLlib, Serve) before productive use
- **−** Cluster setup and operations are left to the user or the paid Anyscale platform
- **−** Not an LLM server by itself; Serve is a library you build on

<sub>GPU optional · Docker · [Repo](https://github.com/ray-project/ray) · [📖 Docs ↗](https://docs.ray.io/en/latest/index.html) · [🌐 Site ↗](https://www.ray.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ray/)</sub>

<a name="tensorflow"></a>
### #&#8288;17 [tensorflow](https://github.com/tensorflow/tensorflow) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (100) · Freshness: active (93) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 202k · Apache-2.0 · Nov 2026</sub>

**Tensor and neural network framework with Python and C++ APIs.**

TensorFlow is a machine learning framework for building, training and deploying models, with stable Python and C++ APIs and non-guaranteed APIs for other languages. It installs via pip, with CUDA GPU support on Ubuntu and Windows and a smaller CPU-only package. Related tooling includes TensorBoard and LiteRT for Android.

- **+** Stable Python and C++ APIs
- **+** CUDA GPU support via pip on Ubuntu and Windows; separate tensorflow-cpu package
- **+** Device plugins for DirectX and macOS Metal
- **+** Surrounding tooling: TensorBoard, LiteRT for Android, official models and tutorials
- **−** APIs for languages other than Python and C++ have no backward compatibility guarantee
- **−** Built-in GPU support is CUDA only; other devices need separate plugins
- **−** Linux XLA build artifacts listed as TBA

<sub>GPU optional · Needs Python, CUDA (for GPU) · Models: LiteRT (Android) · [Repo](https://github.com/tensorflow/tensorflow) · [📖 Docs ↗](https://www.tensorflow.org/api_docs/) · [🌐 Site ↗](https://www.tensorflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorflow/)</sub>

<a name="lerobot"></a>
### #&#8288;18 [lerobot](https://github.com/huggingface/lerobot) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Nov 2026</sub>

**PyTorch library for robot control, datasets and policy training.**

LeRobot is Hugging Face's PyTorch library for real-world robotics. It provides a Python Robot interface for arms, humanoids and teleoperation devices, a LeRobotDataset format (Parquet plus MP4 or images) hosted on the Hub, and implementations of imitation learning, RL, VLA and world-model policies. CLI tools cover recording, training, simulation evaluation and real-robot rollout.

- **+** Covers the full loop: record, train (lerobot-train), evaluate (lerobot-eval), deploy (lerobot-rollout)
- **+** Many policies in pure PyTorch: ACT, Diffusion, Pi0, SmolVLA, GR00T N1.7, HIL-SERL
- **+** Native SO101, Koch, LeKiwi, Unitree G1, Reachy2 support, plus auto-discovered third-party plugins
- **+** Datasets stream from the Hugging Face Hub, with tools to merge, split and edit episodes
- **−** Useful results need a physical robot or simulation benchmarks such as LIBERO or MetaWorld
- **−** Install depends on optional extras (dataset, training, feetech) that vary by robot and policy
- **−** Per-policy GPU and RAM needs live in a separate hardware guide, not the README
- **−** Some listed policies are marked coming soon, so maturity varies by model

<sub>GPU optional · Docker + Compose · Needs PyTorch, Hugging Face Hub · Models: ACT, Diffusion, VQ-BeT, TDMPC, HIL-SERL · [Repo](https://github.com/huggingface/lerobot) · [▶️ Demo ↗](https://huggingface.co/spaces/lerobot/robot-folding) · [📖 Docs ↗](https://huggingface.co/docs/lerobot/index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lerobot/)</sub>

<a name="onnxruntime"></a>
### #&#8288;19 [onnxruntime](https://github.com/microsoft/onnxruntime) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (88) · Freshness: active (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Oct 2026</sub>

**Cross-platform inference engine for ONNX models with hardware accelerator support.**

ONNX Runtime runs ONNX models across different hardware, drivers and operating systems, applying graph optimizations and using hardware accelerators where available. It takes models exported from PyTorch, TensorFlow/Keras and classical libraries such as scikit-learn, LightGBM and XGBoost. A separate training mode accelerates multi-node NVIDIA GPU training of transformer models with a one-line change to existing PyTorch scripts.

- **+** Accepts models from PyTorch, TensorFlow/Keras, scikit-learn, LightGBM and XGBoost via ONNX
- **+** Runs on multiple hardware targets and operating systems with graph optimizations
- **+** MIT license, with docs, roadmap and companion example repositories
- **+** Training acceleration needs one added line in existing PyTorch scripts
- **−** Library, not a server: README describes no built-in HTTP API
- **−** Models must be converted to ONNX format first
- **−** README lists no execution providers, language bindings or system requirements
- **−** May collect usage data and send it to Microsoft; see privacy statement

<sub>GPU optional · Models: ONNX, PyTorch, TensorFlow/Keras, scikit-learn, LightGBM · [Repo](https://github.com/microsoft/onnxruntime) · [📖 Docs ↗](https://onnxruntime.ai/docs) · [🌐 Site ↗](https://onnxruntime.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onnxruntime/)</sub>

<a name="isaaclab"></a>
### #&#8288;20 [isaaclab](https://github.com/isaac-sim/isaaclab) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · BSD-3-Clause · Nov 2026</sub>

**Robot learning framework for RL and imitation learning in GPU simulation.**

Isaac Lab is a Python framework for robotics research that runs reinforcement learning, imitation learning and post-training in GPU-accelerated simulation. It supports Newton, OVRTX, OVPhysX and NVIDIA Isaac Sim as physics and rendering backends, and ships more than 16 robot models and more than 30 environments. Environments train with RSL RL, SKRL, RL Games or Stable Baselines, plus multi-agent RL.

- **+** More than 30 ready-to-train environments and 16+ robot models, from manipulators to humanoids
- **+** Works with RSL RL, SKRL, RL Games and Stable Baselines, and supports multi-agent RL
- **+** Sensor simulation covers RTX cameras, LIDAR, IMU, contact sensors and ray casters
- **+** Multiple backends; kit-less Newton workflows do not need Isaac Sim
- **−** Isaac Sim workflows need a matching Isaac Sim version (6.2 for main) and carry proprietary license terms
- **−** The isaaclab_mimic extension is Apache 2.0 and requires cuRobo, which is proprietary
- **−** Not a general ML library; scope is limited to robotics simulation and learning

<sub>GPU required · Docker + Compose · Needs NVIDIA Isaac Sim 6.2 (for Isaac Sim workflows), Newton, OVRTX, OVPhysX, cuRobo (isaaclab_mimic) · Models: RSL RL, SKRL, RL Games, Stable Baselines · [Repo](https://github.com/isaac-sim/isaaclab) · [📖 Docs ↗](https://isaac-sim.github.io/IsaacLab/main/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/isaaclab/)</sub>

<a name="jax"></a>
### #&#8288;21 [jax](https://github.com/jax-ml/jax) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Nov 2026</sub>

**Python library for autodiff, JIT compilation and vectorization of NumPy-style code.**

JAX runs NumPy-style Python functions on CPU, GPU and TPU by compiling them with XLA. It provides composable transformations (grad, jit, vmap) and three sharding modes (auto, explicit, manual) for scaling across many devices. It is a numerical and ML library rather than a model runner, and the README calls it a research project with sharp edges.

- **+** grad, jit and vmap compose arbitrarily, including higher-order derivatives and per-example gradients
- **+** Three sharding modes: compiler-automatic, explicit in types, and manual per-device with collectives
- **+** Compiles through XLA to CPU, NVIDIA, AMD and Google TPU targets
- **+** Differentiates through Python loops, branches, recursion and closures
- **−** README calls it a research project, not an official Google product, and warns of sharp edges
- **−** jit restricts Python control flow, so some code needs rewriting
- **−** No NVIDIA GPU support on native Windows; Apple and Intel GPU support is experimental
- **−** Provides arrays and transformations only; neural network layers need separate libraries

<sub>GPU optional · Needs XLA, NumPy · [Repo](https://github.com/jax-ml/jax) · [📖 Docs ↗](https://docs.jax.dev/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jax/)</sub>

<a name="triton"></a>
### #&#8288;22 [triton](https://github.com/triton-lang/triton) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Nov 2026</sub>

**Python-based language and compiler for writing custom GPU kernels for deep learning.**

Triton is a language and MLIR/LLVM-based compiler for writing deep-learning kernels in Python and compiling them for NVIDIA and AMD GPUs. It aims for higher productivity than CUDA and more flexibility than other DSLs. It installs with `pip install triton` and includes an interpreter mode and many debug and IR-dump knobs.

- **+** Supports NVIDIA (compute capability 8.0+) and AMD (ROCm 6.2+) GPUs
- **+** TRITON_INTERPRET=1 runs kernels without a GPU, so Python breakpoints work
- **+** Extensive debug knobs: per-pass MLIR dumps, reproducers, kernel IR override
- **+** Prebuilt wheels on pip for CPython 3.10-3.14
- **−** Linux only; CPU backend is still under development
- **−** Source builds depend on LLVM, which has no stable API and builds slowly
- **−** No single command runs all tests; the full suite needs a GPU
- **−** Kernel authors still need to understand GPU memory and tiling

<sub>GPU required · Needs LLVM (prebuilt download or custom build), CUDA or ROCm 6.2+, Python 3.10-3.14 · [Repo](https://github.com/triton-lang/triton) · [📖 Docs ↗](https://triton-lang.org) · [🌐 Site ↗](https://triton-lang.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/triton/)</sub>

<a name="transformers-js"></a>
### #&#8288;23 [transformers.js](https://github.com/huggingface/transformers.js) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

**Runs Hugging Face models in browser or Node via ONNX Runtime.**

Transformers.js mirrors the Python transformers `pipeline` API in JavaScript and runs ONNX-converted models client-side with ONNX Runtime. It covers NLP, vision, audio and multimodal tasks such as text generation, speech recognition, text-to-speech, embeddings and object detection. It runs on CPU via WASM by default, with optional WebGPU and quantized dtypes (fp32, fp16, q8, q4).

- **+** Pipeline API closely matches Python transformers, easing code translation
- **+** Runs in the browser with no server; models load from the Hugging Face Hub
- **+** Optional WebGPU and q4/q8/fp16 dtypes to cut download size and speed up inference
- **+** Wide task coverage: NLP, vision, audio, embeddings, document QA, background removal
- **−** Models must be in ONNX format; others need conversion with Optimum
- **−** README calls WebGPU experimental in many browsers
- **−** Unsupported tasks include text-to-image, visual QA, mask generation and tabular tasks
- **−** Default setup fetches models and WASM binaries from remote hosts unless configured locally

<sub>GPU optional · Needs ONNX Runtime, Hugging Face Hub (default model source) · Models: ONNX, Hugging Face Hub models · [Repo](https://github.com/huggingface/transformers.js) · [📖 Docs ↗](https://huggingface.co/docs/transformers.js) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transformers-js/)</sub>

<a name="skypilot"></a>
### #&#8288;24 [skypilot](https://github.com/skypilot-org/skypilot) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

**Run and scale AI jobs across Kubernetes, Slurm and 20+ clouds.**

SkyPilot takes a YAML or Python task spec (resources, workdir, setup, run) and launches it on the cheapest available infra among your Kubernetes clusters, Slurm clusters or cloud accounts. It provisions GPUs, TPUs or CPUs with auto-failover, syncs code, runs setup and streams logs. It also handles job queueing, autostop of idle clusters, and a shared API server for teams.

- **+** One task spec runs on Kubernetes, Slurm, or 20+ listed clouds without code changes
- **+** Auto-failover on capacity errors and cheapest-available placement across infra
- **+** Autostop of idle clusters and binpacking on shared clusters reduce idle GPU spend
- **+** Runs inside your own cloud accounts, VPCs and clusters (BYOC)
- **−** Infra orchestrator, not a model library or trainer; you bring your own training code
- **−** Needs cloud credentials and GPU quota set up per provider before use
- **−** Sandboxes feature is early access via a signup form
- **−** Team deployment requires running a separate API server

<sub>GPU optional · Docker · Needs Kubernetes, Slurm or a cloud account (AWS, GCP, Azure, etc.) · Models: vLLM, SGLang, Ollama · [Repo](https://github.com/skypilot-org/skypilot) · [📖 Docs ↗](https://docs.skypilot.co/) · [🌐 Site ↗](https://skypilot.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skypilot/)</sub>

<a name="autogluon"></a>
### #&#8288;25 [autogluon](https://github.com/autogluon/autogluon) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

**AutoML library for tabular, time series and multimodal data in Python.**

AutoGluon trains and ensembles models for tabular, time series and multimodal prediction through predictor classes such as TabularPredictor, TimeSeriesPredictor and MultiModalPredictor. It selects and combines models, from classic ML algorithms to foundation models, so a working pipeline takes a few lines of Python. It installs with pip on Python 3.10 to 3.13 across Linux, macOS and Windows.

- **+** Three task APIs (tabular, time series, multimodal) share a fit/predict pattern
- **+** Combines classic ML models and foundation models in one ensemble
- **+** Installs with pip or conda on Linux, macOS and Windows
- **+** Cloud options: AutoGluon Cloud, official Docker image, AWS Deep Learning Containers
- **−** README gives no RAM, VRAM or training-time figures
- **−** Not an LLM app; no chat UI, model server or agent runtime
- **−** Supports Python 3.10 to 3.13 only

<sub>GPU optional · Models: tabular models, time series forecasting, multimodal models · [Repo](https://github.com/autogluon/autogluon) · [📖 Docs ↗](https://auto.gluon.ai/stable/index.html) · [🌐 Site ↗](https://auto.gluon.ai/stable/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autogluon/)</sub>

<a name="xgboost"></a>
### #&#8288;26 [xgboost](https://github.com/dmlc/xgboost) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Nov 2026</sub>

**Gradient boosted decision tree library for tabular machine learning.**

XGBoost implements parallel tree boosting (GBDT/GBM) under the gradient boosting framework. Per the README, the same code runs on Kubernetes, Hadoop, SGE, Dask, Spark and PySpark, and scales to billions of examples. It is distributed through PyPI, CRAN and conda-forge.

- **+** Same code runs on Kubernetes, Hadoop, SGE, Dask, Spark and PySpark
- **+** Packaged on PyPI, CRAN and conda-forge
- **+** Backed by a KDD 2016 paper; Apache-2.0 licensed
- **+** Active: release on 2026-09-15 and recent commits
- **−** Tree boosting only; not a general deep learning framework
- **−** README has no install or quick-start example; relies on external docs
- **−** Aimed at tabular data; no LLM or generative model support

<sub>Models: gradient boosted decision trees · [Repo](https://github.com/dmlc/xgboost) · [📖 Docs ↗](https://xgboost.readthedocs.io) · [🌐 Site ↗](https://xgboost.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xgboost/)</sub>

<a name="sentence-transformers"></a>
### #&#8288;27 [sentence-transformers](https://github.com/huggingface/sentence-transformers) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Nov 2026</sub>

**Python library for text embeddings, rerankers, and sparse and ColBERT-style models.**

Sentence Transformers is a Python library that computes dense embeddings, cross-encoder rerank scores, sparse (SPLADE-style) embeddings and multi-vector late-interaction embeddings. It loads any of the 15,000+ compatible models from the Hugging Face Hub and trains or fine-tunes all four model types. Install is via pip, with extras for image, audio, video, ONNX and OpenVINO.

- **+** Four model types behind one API: dense, cross-encoder, sparse and multi-vector
- **+** Loads 15,000+ pretrained models from the Hugging Face Hub, including MTEB leaderboard entries
- **+** Built-in training with 20+ embedding loss functions and evaluation during training
- **+** Extras for ONNX, OpenVINO, image, audio and video inputs
- **−** Library only: no server, vector store or retrieval pipeline included
- **−** Requires Python 3.10+, PyTorch 2.2+ and transformers v5.0+
- **−** README calls the repo experimental software tied to the original publication
- **−** Gated or private models need a Hugging Face login

<sub>GPU optional · Needs PyTorch 2.2+, transformers 5.0+, Hugging Face Hub · Models: Sentence Transformer, Cross-Encoder, Sparse Encoder, Multi-Vector Encoder, BERT · [Repo](https://github.com/huggingface/sentence-transformers) · [📖 Docs ↗](https://www.sbert.net/docs/quickstart.html) · [🌐 Site ↗](https://www.sbert.net) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sentence-transformers/)</sub>

<a name="mnn"></a>
### #&#8288;28 [mnn](https://github.com/alibaba/mnn) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

**On-device inference and training engine for phones, embedded and PC.**

MNN is a C++ deep learning engine from Alibaba that runs and trains models on phones, embedded devices and PCs. It converts TensorFlow, Caffe, ONNX and TorchScript models and runs them on ARM/x86 CPUs and on Metal, OpenCL, Vulkan and CUDA GPUs, with a Hexagon backend added in 3.6.1. MNN-LLM and MNN-Diffusion run LLMs and Stable Diffusion locally, and Android and iOS chat apps are included.

- **+** Small footprint: about 800KB core .so on Android, about 12MB iOS static library with all options
- **+** Backends for ARM/x86 CPU, Metal, OpenCL, Vulkan, CUDA, CoreML, NNAPI and Hexagon
- **+** Converter covers TensorFlow, Caffe, ONNX and TorchScript, with FP16/Int8 quantization
- **+** Includes MNN-LLM, MNN-Diffusion and Android/iOS demo apps
- **−** Community discussion is on DingTalk groups, predominantly in Chinese
- **−** QNN is rated B or C in the README support table
- **−** No Docker or HTTP server deployment described; it is a library and toolchain
- **−** Native CPU and NNAPI paths are rated B (bugs or not optimized)

<sub>GPU optional · Models: TensorFlow, Caffe, ONNX, TorchScript, Qwen · [Repo](https://github.com/alibaba/mnn) · [📖 Docs ↗](https://mnn-docs.readthedocs.io/en/latest/) · [🌐 Site ↗](http://www.mnn.zone) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mnn/)</sub>

<a name="fiftyone"></a>
### #&#8288;29 [fiftyone](https://github.com/voxel51/fiftyone) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

**Dataset visualization, curation and model evaluation tool for computer vision.**

FiftyOne is a Python library with a browser-based App for exploring image, video and 3D datasets together with their labels. It supports 2D and 3D annotation, an embeddings panel, model evaluation to find failure modes, and a Brain module for finding data and annotation issues. It integrates with PyTorch, Hugging Face and Ultralytics, and can be extended with plugins.

- **+** Installs with pip install fiftyone; supports Python 3.10 to 3.13
- **+** Built-in dataset zoo and model zoo for quick starts
- **+** Embeddings panel and evaluation tools to locate failure modes and label errors
- **+** Plugin system to extend the App and workflows
- **−** Team collaboration and cloud-native workloads are in the separate commercial Voxel51 product
- **−** Focused on computer vision; not aimed at text or LLM workflows
- **−** Video datasets need FFmpeg installed separately

<sub>GPU optional · Docker · Needs Python 3.10-3.13, MongoDB (fiftyone-db package; self-managed instance optional), FFmpeg (for video), Node.js and Yarn (source install only) · Models: PyTorch, Hugging Face, Ultralytics · [Repo](https://github.com/voxel51/fiftyone) · [▶️ Demo ↗](https://colab.research.google.com/github/voxel51/fiftyone-examples/blob/master/examples/quickstart.ipynb) · [📖 Docs ↗](https://docs.voxel51.com) · [🌐 Site ↗](https://voxel51.com/fiftyone) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fiftyone/)</sub>

<a name="feast"></a>
### #&#8288;30 [feast](https://github.com/feast-dev/feast) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Nov 2026</sub>

**Feature store that serves consistent ML features for training and online inference.**

Feast manages an offline store for historical data, an online store for low-latency lookups, and a feature server on top of existing infrastructure. It generates point-in-time correct training sets to prevent data leakage and materializes feature values into the online store. Offline and online backends are pluggable (BigQuery, Snowflake, Redshift, Redis, DynamoDB, Postgres and others), many as contrib plugins.

- **+** Point-in-time correct joins for training sets, avoiding future-value leakage
- **+** Wide backend list: Snowflake, BigQuery, Redshift, Redis, DynamoDB, Postgres, Cassandra and more
- **+** Python, Java and Go feature servers plus a Kubernetes operator
- **+** Custom offline and online store support via documented extension points
- **−** Many components are alpha or beta: Java/Go servers, operator, streaming transformations, web UI
- **−** Many backends are contrib or community plugins with varying support
- **−** Needs existing data infrastructure; it is not a standalone compute engine
- **−** Batch transformation is still in progress; Lineage Explorer is not built

<sub>no GPU · Docker · Needs Offline store (e.g. BigQuery, Snowflake, Redshift, Postgres, DuckDB), Online store (e.g. Redis, DynamoDB, SQLite, Postgres) · [Repo](https://github.com/feast-dev/feast) · [📖 Docs ↗](https://docs.feast.dev/) · [🌐 Site ↗](https://feast.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/feast/)</sub>

<a name="scikit-learn"></a>
### #&#8288;31 [scikit-learn](https://github.com/scikit-learn/scikit-learn) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · BSD-3-Clause · Nov 2026</sub>

**Python library of classical machine learning algorithms built on NumPy and SciPy.**

scikit-learn is a Python module for machine learning built on SciPy, started in 2007 as a Google Summer of Code project. It installs with pip or conda and requires Python 3.12 or newer, NumPy, SciPy, Narwhals, joblib and threadpoolctl. Plotting helpers need Matplotlib. The README does not list the algorithms; those are documented on the website.

- **+** Installs with one pip or conda command; six required dependencies, all listed with minimum versions
- **+** BSD-3-Clause license; test suite runs with pytest sklearn
- **+** Volunteer community with institutional support; benchmarked with asv
- **+** Test randomness is controllable through the SKLEARN_SEED environment variable
- **−** Requires Python 3.12 or newer, which excludes older environments
- **−** Plotting needs Matplotlib, installed separately
- **−** README gives no algorithm list; readers must consult the website

<sub>Needs Python >= 3.12, NumPy >= 1.26.0, SciPy >= 1.11.4, Narwhals >= 2.0.1, joblib >= 1.4.0, threadpoolctl >= 3.5.0 · [Repo](https://github.com/scikit-learn/scikit-learn) · [📖 Docs ↗](https://scikit-learn.org/stable/) · [🌐 Site ↗](https://scikit-learn.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scikit-learn/)</sub>

<a name="shap"></a>
### #&#8288;32 [shap](https://github.com/shap/shap) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Nov 2026</sub>

**Python library that explains ML model predictions with Shapley values.**

SHAP computes per-feature attributions for model predictions using Shapley values. It has model-specific explainers (Tree, Deep, Gradient, Linear) and a model-agnostic Kernel explainer, plus plots such as waterfall, force, beeswarm, scatter and text. Tree SHAP has C++ implementations for XGBoost, LightGBM, CatBoost, scikit-learn and pyspark; transformers pipelines are supported for NLP.

- **+** Exact, fast Tree SHAP in C++ for XGBoost, LightGBM, CatBoost, scikit-learn, pyspark
- **+** KernelExplainer works on any model that exposes a prediction function
- **+** Built-in plots: waterfall, force, beeswarm, scatter, bar, text, image
- **+** Optional GPU Tree SHAP via the separate shap-cuda package
- **−** KernelExplainer is slower than the model-specific explainers
- **−** DeepExplainer supports TensorFlow/Keras; PyTorch support is described as preliminary
- **−** Some README examples use older Keras APIs such as K.get_session
- **−** Explains models but does not train, serve or monitor them

<sub>GPU optional · Needs XGBoost, LightGBM, CatBoost, scikit-learn, TensorFlow/Keras, PyTorch, transformers · Models: XGBoost, LightGBM, CatBoost, scikit-learn, pyspark · [Repo](https://github.com/shap/shap) · [▶️ Demo ↗](https://mybinder.org/v2/gh/shap/shap/main) · [📖 Docs ↗](https://shap.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/shap/)</sub>

<a name="pysyft"></a>
### #&#8288;33 [pysyft](https://github.com/openmined/pysyft) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

**Python library for running data-owner-approved jobs on private data.**

PySyft lets a data scientist submit Python jobs that a data owner reviews, approves and runs against private datasets, returning only approved outputs. Peers sync through cloud storage they already use, currently Google Drive, or through WebRTC channels. The client is split into packages for datasets, jobs, permissions and background services, with enclave tutorials for private LLM evaluation.

- **+** Private data stays on the owner's machine; scientists work on mock data until a job is approved
- **+** Needs no new server; syncs over Google Drive, with Microsoft 365 and WebRTC also named
- **+** Each collaborator and each job requires explicit data owner approval
- **+** Includes tutorials for double-blind LLM evals in enclaves and LLM user log analysis
- **−** README describes only Google Drive as a working transport; others are called extensible
- **−** Local or Jupyter use needs a Google Cloud OAuth token, about 15 minutes to set up
- **−** Each role needs its own Google account
- **−** Breaking API change: legacy PySyft 0.9 users must pin syft<0.10

<sub>Needs Python 3.10+, Google Drive, Google Cloud OAuth token (local/Jupyter) · [Repo](https://github.com/openmined/pysyft) · [📖 Docs ↗](https://github.com/OpenMined/PySyft/blob/dev/docs/workflow.md) · [🌐 Site ↗](https://openmined.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pysyft/)</sub>

<a name="accelerate"></a>
### #&#8288;34 [accelerate](https://github.com/huggingface/accelerate) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10.0k · Apache-2.0 · Nov 2026</sub>

**Thin PyTorch wrapper that runs your training loop on CPU, GPU, TPU or multi-node.**

Accelerate adds an Accelerator class to a plain PyTorch training script, handling device placement, distributed setup and mixed precision (fp16, bf16, fp8) with about five changed lines. It includes an optional `accelerate config` and `accelerate launch` CLI, a notebook launcher, and plugins for DeepSpeed, FSDP and Megatron-LM, which the README marks experimental. It is not a high-level trainer: you still write the loop yourself.

- **+** Whole API is one Accelerator class; the rest of the training loop stays unchanged
- **+** Same script runs on CPU, single or multi-GPU, multi-node and TPU
- **+** Optional CLI wraps torchrun, MPI and DeepSpeed launch config; plain python also works
- **+** Mixed precision includes fp8 via Transformer Engine or MS-AMP
- **−** No built-in trainer; you must write and maintain your own training loop
- **−** DeepSpeed, FSDP and Megatron-LM support are labeled experimental in the README
- **−** PyTorch only; needs Python 3.8+ and PyTorch 1.10.0+ installed separately
- **−** With DeepSpeed you still handle gradient accumulation yourself

<sub>GPU optional · Docker · Needs PyTorch, DeepSpeed (optional), Open MPI (optional), Transformer Engine or MS-AMP (optional, fp8) · Models: PyTorch models, Hugging Face Transformers · [Repo](https://github.com/huggingface/accelerate) · [📖 Docs ↗](https://huggingface.co/docs/accelerate) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/accelerate/)</sub>

<a name="tabpfn"></a>
### #&#8288;35 [tabpfn](https://github.com/priorlabs/tabpfn) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · Apache-2.0 · Nov 2026</sub>

**Pretrained transformer for tabular classification and regression, no per-dataset training.**

TabPFN is a Python library with scikit-style TabPFNClassifier and TabPFNRegressor estimators built on a transformer pretrained on synthetic datasets. Calling fit stores the training data and predict runs a single forward pass, so no per-dataset gradient training is needed. The default TabPFN-3.5 checkpoint accepts up to 1,000,000 rows and 20,000 features. Model weights carry non-commercial licenses, separate from the Apache-2.0 code.

- **+** Drop-in fit/predict estimators for classification and regression, installed with pip
- **+** Data stays local; works offline once weights are downloaded
- **+** Several checkpoints selectable, including smaller TabPFN-3.5-Fast and older V2, V3
- **+** Runs on Nvidia, AMD ROCm and Apple Silicon GPUs, with CPU fallback
- **−** TabPFN-2.5 to 3.5 weights are non-commercial; commercial use needs a license
- **−** First use requires browser login and license acceptance, or a TABPFN_TOKEN
- **−** CPU use capped at 5000 samples for recent models unless overridden
- **−** Fast distillation inference mode is Enterprise-only

<sub>GPU optional · Needs PyTorch, PriorLabs account token for weight download · Models: TabPFN-3.5, TabPFN-3.5-Fast, TabPFN-3, TabPFN-2 · [Repo](https://github.com/priorlabs/tabpfn) · [▶️ Demo ↗](https://colab.research.google.com/github/PriorLabs/TabPFN/blob/main/examples/notebooks/TabPFN_Demo_Local.ipynb) · [📖 Docs ↗](https://priorlabs.ai/docs) · [🌐 Site ↗](https://ux.priorlabs.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tabpfn/)</sub>

<a name="optuna"></a>
### #&#8288;36 [optuna](https://github.com/optuna/optuna) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

**Python hyperparameter optimization library with define-by-run search spaces and pruning.**

Optuna runs studies made of trials: you write an objective function in Python, declare hyperparameters inside it with suggest_* calls, and the library samples values and prunes unpromising trials. Search spaces can use conditionals and loops, and studies can be stored in a database such as SQLite and run across many workers. Companion projects cover a web dashboard (optuna-dashboard), a plugin registry (OptunaHub) and an experimental Rust port (Rustuna).

- **+** Search spaces are plain Python, so conditionals and loops work inside the objective
- **+** Pruning of unpromising trials, multi-objective and constrained optimization are supported
- **+** Installs from pip or conda with few requirements; MIT license
- **+** Studies persist to a database like SQLite and can run across many workers
- **−** Web dashboard is a separate package (optuna-dashboard), not part of core
- **−** Requires Python 3.10 or newer
- **−** Rust port Rustuna is experimental and lacks some Optuna features and APIs
- **−** Some OptunaHub samplers need extra dependencies such as torch, scipy and cmaes

<sub>no GPU · Needs Python 3.10+, SQLite or other database (optional storage) · Models: scikit-learn · [Repo](https://github.com/optuna/optuna) · [📖 Docs ↗](https://optuna.readthedocs.io/en/stable/) · [🌐 Site ↗](https://optuna.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/optuna/)</sub>

<a name="nltk"></a>
### #&#8288;37 [nltk](https://github.com/nltk/nltk) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Nov 2026</sub>

**Python library of classic NLP modules, corpora and tutorials.**

NLTK is a suite of Python modules, datasets and tutorials for natural language processing research and teaching. It requires Python 3.11 up to 3.15 and its source is Apache 2.0, with corpora under per-corpus terms. It accompanies the book "Natural Language Processing with Python" and is documented at nltk.org.

- **+** Backed by a published book and tutorials, suited to teaching NLP
- **+** Ships with corpora and datasets alongside the code
- **+** Apache 2.0 source license; last release 2026-10-21
- **+** Python library distributed on PyPI
- **−** Corpora are redistributable for non-commercial use only, per each corpus README
- **−** Documentation license is non-commercial and no-derivatives
- **−** README gives no feature list or API examples

<sub>Needs Python 3.11-3.15 · [Repo](https://github.com/nltk/nltk) · [📖 Docs ↗](https://www.nltk.org/) · [🌐 Site ↗](https://www.nltk.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nltk/)</sub>

<a name="metaflow"></a>
### #&#8288;38 [metaflow](https://github.com/netflix/metaflow) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

**Python framework for building, scaling and deploying ML and AI workflows.**

Metaflow is a Python library for writing ML and AI pipelines as flows of steps, which run locally or in a notebook and then scale out to cloud compute on CPUs and GPUs. It tracks experiments, versions artifacts, manages dependencies, and deploys flows to production orchestrators with event-based triggering. Originally built at Netflix, now supported by Outerbounds.

- **+** Same flow code runs on a laptop, in a notebook, on cloud compute and in production
- **+** Built-in experiment tracking, artifact versioning and a client API for inspecting past runs
- **+** Supports foreach parallelism and gang-scheduled distributed jobs on CPUs and GPUs
- **+** Apache-2.0, installable from PyPI or conda-forge
- **−** Cloud scaling and production orchestration need separate infrastructure setup beyond pip install
- **−** Not LLM-specific; README describes no model serving or agent features
- **−** No Docker or compose setup in the repository

<sub>GPU optional · Needs Python, Cloud compute cluster (for scaling), Production workflow orchestrator (for deployment) · [Repo](https://github.com/netflix/metaflow) · [▶️ Demo ↗](https://outerbounds.com/sandbox) · [📖 Docs ↗](https://docs.metaflow.org) · [🌐 Site ↗](https://metaflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/metaflow/)</sub>

<a name="vowpal-wabbit"></a>
### #&#8288;39 [vowpal_wabbit](https://github.com/vowpalwabbit/vowpal_wabbit) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · custom license · Sep 2026</sub>

**Online machine learning library with contextual bandits and hashed features.**

Vowpal Wabbit is a C++ online learning system that trains with sparse gradient descent and other optimizers, streaming data so memory stays bounded regardless of training set size. It uses the hashing trick for features and supports reductions, allreduce, active learning and several contextual bandit algorithms. It is a classic ML tool, not an LLM project.

- **+** Memory footprint is bounded; training data is not loaded into RAM
- **+** Hashing trick bounds feature set size independent of data volume
- **+** Several contextual bandit algorithms for reinforcement learning
- **+** Runs on Windows, macOS and Linux; Python notebooks and CLI demos included
- **−** Not an LLM or deep learning tool; no neural model serving described
- **−** README gives no hardware requirements or benchmark numbers
- **−** License is detected as NOASSERTION; check the repository license file
- **−** Most documentation lives in the wiki, not the README

<sub>Models: sparse gradient descent, contextual bandits, bag-of-words text features · [Repo](https://github.com/vowpalwabbit/vowpal_wabbit) · [📖 Docs ↗](https://github.com/VowpalWabbit/vowpal_wabbit/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vowpal-wabbit/)</sub>

<a name="smile"></a>
### #&#8288;40 [smile](https://github.com/haifengl/smile) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · custom license · Nov 2026</sub>

**JVM machine learning library with classic ML, deep learning and LLM inference.**

SMILE is a machine learning library for the JVM with Java, Scala and Kotlin APIs. It covers classification, regression, clustering, manifold learning, NLP and plotting, plus a LibTorch-backed deep module with LLaMA-3 and Qwen3.5 inference. It also ships a Quarkus inference server (SMILE models, ONNX, OpenAI-compatible chat) and an agentic desktop IDE, SMILE Studio.

- **+** Broad classic ML coverage: SVM, random forest, GBDT, t-SNE, UMAP, HMM, CRF, FP-growth
- **+** Serve module exposes SMILE, ONNX and OpenAI-compatible chat endpoints with a bundled web UI
- **+** Idiomatic Scala and Kotlin APIs plus a Spark integration module
- **+** Per-module docs and Maven Central releases (7.1.0)
- **−** Multi-product license with commercial terms; not a single standard open-source license
- **−** v5+ requires Java 25, which limits use on older JVM stacks
- **−** Several algorithms need native BLAS/LAPACK and ARPACK installed separately
- **−** Deep and LLM features need LibTorch; LLM support lists only LLaMA-3 and Qwen3.5

<sub>GPU optional · Needs Java 25, OpenBLAS, ARPACK, LibTorch (deep module) · Models: SMILE .sml, ONNX, LLaMA-3, Qwen3.5, EfficientNet-V2 · [Repo](https://github.com/haifengl/smile) · [📖 Docs ↗](https://www.aihalo.dev/) · [🌐 Site ↗](https://www.aihalo.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/smile/)</sub>

<a name="pytorch-metric-learning"></a>
### #&#8288;41 [pytorch-metric-learning](https://github.com/kevinmusgrave/pytorch-metric-learning) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Nov 2026</sub>

**PyTorch library of metric learning losses, miners, and distances for embedding models.**

A PyTorch library for training embedding models with composable losses, hard-example miners, distances, reducers, and regularizers. Components drop into an existing training loop, taking embeddings and integer labels where equal labels mark positive pairs. Retrieval metrics are included, with an optional Faiss backend and scikit-learn for NMI/AMI clustering metrics.

- **+** Losses, miners, distances and reducers are separate components that can be combined
- **+** Fits into a plain PyTorch loop; core needs only PyTorch and NumPy
- **+** Each component's docs page states its signature, defaults, tensor contract, and paper
- **+** Optional extras for Faiss retrieval and scikit-learn clustering metrics
- **−** Version 3 requires Python 3.12+, PyTorch 2.14.0+ and NumPy 2.5.3+
- **−** Upgrading from version 2 requires a migration guide because names changed
- **−** Library only: no training CLI, pretrained models, or serving layer
- **−** Pair and triplet setup relies on integer labels in batches

<sub>GPU optional · Needs PyTorch, NumPy, Faiss (optional), scikit-learn (optional) · Models: Any torch.nn.Module that outputs embeddings · [Repo](https://github.com/kevinmusgrave/pytorch-metric-learning) · [📖 Docs ↗](https://kevinmusgrave.github.io/pytorch-metric-learning/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-metric-learning/)</sub>

<a name="paddle"></a>
### #&#8288;42 [paddle](https://github.com/paddlepaddle/paddle) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Nov 2026</sub>

**Deep learning framework with dynamic/static graphs and automatic parallel training.**

PaddlePaddle is a C++ deep learning framework that covers training and inference of large models in one codebase. It supports dynamic and static graphs, derives distributed parallel strategies from single-card code with tensor partition annotations, and offers high-order differentiation for scientific computing plus a neural network compiler. A pluggable interface adapts it to multiple chip types.

- **+** Automatic parallelism from minimal tensor partition annotations on single-card code
- **+** Same framework handles both large-model training and inference
- **+** High-order autodiff, complex numbers and Fourier transforms for scientific computing
- **+** Pluggable multi-chip adaptation layer and a neural network compiler
- **−** README gives no hardware requirements or supported Python versions
- **−** README refers to both 3.2 and 3.3, so the current feature set is unclear
- **−** No Docker or compose files detected in the repository
- **−** Practice tutorials link to the Chinese docs, so English coverage may be thinner

<sub>GPU optional · Models: dynamic graph, static graph, large models, generative models, scientific computing models · [Repo](https://github.com/paddlepaddle/paddle) · [📖 Docs ↗](https://www.paddlepaddle.org.cn/documentation/docs/en/guides/index_en.html) · [🌐 Site ↗](https://www.paddlepaddle.org.cn/install/quick) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddle/)</sub>

<a name="carla"></a>
### #&#8288;43 [carla](https://github.com/carla-simulator/carla) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

**Autonomous driving simulator built on Unreal Engine 5.5 with a Python API.**

CARLA is a simulator for developing, training and validating autonomous driving systems. It ships open urban maps, buildings and vehicles, and lets you configure sensor suites and weather through a Python API. This branch (ue5-dev) targets Unreal Engine 5.5 and must be built from source against the CARLA fork of Unreal Engine.

- **+** Open assets (maps, vehicles, buildings) included, code MIT and assets CC-BY
- **+** Configurable sensor suites and environmental conditions, driven through a Python API
- **+** Ecosystem repos for ROS bridge, Scenario_Runner, Autoware bridge and a driving leaderboard
- **+** Optional ROS2 support via the -DENABLE_ROS2=ON CMake flag
- **−** Heavy hardware: 32 GB+ RAM and an RTX 3070-class GPU with 16 GB+ VRAM recommended
- **−** Build needs GitHub-linked Epic Games access to the Unreal Engine 5.5 fork
- **−** UE5.5 build supports only Ubuntu 22.04/24.04 and Windows 11; Ubuntu 20.04 and Windows 10 unsupported
- **−** Parallel ue4-dev branch has significant differences; last release dated 2025-09-16

<sub>RAM ≥ 32 GB · GPU required · Needs Unreal Engine 5.5 (CARLA fork), CMake, Ninja, Python 3, Visual Studio 2022 (Windows), PROJ, Xerces-C, Eigen · [Repo](https://github.com/carla-simulator/carla) · [📖 Docs ↗](https://carla-ue5.readthedocs.io) · [🌐 Site ↗](http://carla.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/carla/)</sub>

<a name="dlib"></a>
### #&#8288;44 [dlib](https://github.com/davisking/dlib) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · BSL-1.0 · Nov 2026</sub>

**C++ machine learning toolkit with Python bindings.**

Dlib is a C++17 library of machine learning algorithms and general-purpose tools for building software in C++. It is built with CMake, can be installed through vcpkg, and has a Python API available with pip install dlib. The README points to dlib.net for the API reference and does not list individual algorithms or models.

- **+** Boost Software License permits use in closed-source commercial software
- **+** Installs via CMake, vcpkg, or pip for the Python API
- **+** Ships a unit test suite (dtest) and many example programs
- **+** Optional AVX build flag speeds up some operations
- **−** Requires a C++17 compiler and CMake to build from source
- **−** pip install from source needs a local compiler toolchain
- **−** Not a server or UI; used only as a library

<sub>Needs C++17 compiler, CMake · [Repo](https://github.com/davisking/dlib) · [📖 Docs ↗](http://dlib.net/compile.html) · [🌐 Site ↗](http://dlib.net) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dlib/)</sub>

<a name="tvm"></a>
### #&#8288;45 [tvm](https://github.com/apache/tvm) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

**Python-first machine learning compiler for optimizing and deploying models.**

Apache TVM is a machine learning compilation framework that uses TensorIR for tensor programs and Relax for computational graphs. Compiler transformations are customizable in Python, and the aim is to package models into minimal deployable modules. It also serves as a base for building domain-specific compilers, such as for LLMs.

- **+** Cross-level design: TensorIR for tensor programs and Relax for graphs, optimized jointly
- **+** Most compiler transformations can be customized in Python
- **+** Apache-2.0 license under the Apache committer governance model
- **+** Documentation site includes a getting-started tutorial and contributor guide
- **−** README lists no supported hardware targets or model formats
- **−** README gives no install steps, version requirements or benchmarks
- **−** Compiler workflow has a steeper learning curve than ready-made inference servers
- **−** No ready-to-run model server or UI is described in the README

<sub>Docker · [Repo](https://github.com/apache/tvm) · [📖 Docs ↗](https://tvm.apache.org/docs) · [🌐 Site ↗](https://tvm.apache.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tvm/)</sub>

<a name="tokenizers"></a>
### #&#8288;46 [tokenizers](https://github.com/huggingface/tokenizers) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

**Rust tokenizer library with Python and Node.js bindings.**

Rust tokenization engine that loads tokenizer.json files or Hub tokenizers and encodes and decodes text with BPE, Unigram, WordPiece and WordLevel models. It ships Python and Node.js bindings and is split into sub-crates so serving builds can leave out training and legacy converters. The v1.0.0 release candidate does not yet include all of the 0.23 Python API.

- **+** Every kernel has a portable scalar path; SIMD (NEON, AVX-512, SSE, wasm SIMD128) is optional
- **+** Sub-crates let serving builds omit training and legacy conversion code
- **+** Bindings for Rust, Python and Node.js; loads from file or Hugging Face Hub
- **+** Byte-exact pre-tokenizer grammars for gpt2, cl100k, o200k, tekken, deepseek and kimi-k2
- **−** v1.0.0 is a release candidate; Python install needs pip --pre
- **−** Python training, save, offsets, pair input and decode_stream are not back yet
- **−** C, C++, Java and Go bindings are only planned
- **−** Known load failure for ModernBERT and OLMo tokenizers (64-bit hash collision)

<sub>no GPU · Models: BPE, Unigram, WordPiece, WordLevel, tokenizer.json · [Repo](https://github.com/huggingface/tokenizers) · [📖 Docs ↗](https://huggingface.co/docs/tokenizers/index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tokenizers/)</sub>

<a name="executorch"></a>
### #&#8288;47 [executorch](https://github.com/pytorch/executorch) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · custom license · Nov 2026</sub>

**PyTorch runtime for running exported models on phones, browsers and microcontrollers.**

ExecuTorch takes a PyTorch model captured with torch.export, lowers it to a backend-specific .pte file, and runs it through C++, Python, Swift/Objective-C, Kotlin/Java or JavaScript APIs. Backends include XNNPACK, Core ML, Vulkan, Qualcomm, MediaTek, OpenVINO, Arm Cortex-M and Ethos-U. It also ships LLM, speech and vision examples and an experimental OpenAI-compatible local server.

- **+** Starts from torch.export, so existing PyTorch models need no separate framework
- **+** Backends span XNNPACK, Core ML, Vulkan, Qualcomm, MediaTek, OpenVINO, Arm Ethos-U, Cadence
- **+** Selective build links only the operators, kernels and delegates a deployment needs
- **+** Stable-API .pte files are guaranteed to load for at least one following non-patch release
- **−** Each hardware target needs its own backend-specific .pte export
- **−** Deployment depends on torch.export capture and operator coverage; some models need decompositions
- **−** CUDA, Metal, MLX, WebGPU and WASM paths are labeled experimental
- **−** Features described on main/nightly may change before release

<sub>GPU optional · Needs PyTorch (torch.export), Python 3.11-3.15 · Models: PyTorch models via torch.export (.pte), LLMs, speech models, vision models, Hugging Face models via Optimum ExecuTorch · [Repo](https://github.com/pytorch/executorch) · [📖 Docs ↗](https://docs.pytorch.org/executorch/main/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/executorch/)</sub>

<a name="transformerlens"></a>
### #&#8288;48 [transformerlens](https://github.com/transformerlensorg/transformerlens) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · MIT · Nov 2026</sub>

**Python library for inspecting and editing activations in language models.**

TransformerLens is a Python library for mechanistic interpretability. It loads open models from HuggingFace through TransformerBridge, caches any internal activation, and lets you add hooks that edit, remove or replace activations during a forward pass. The README lists 15,000+ models across 140+ architecture families, plus experimental Mamba-1 and Mamba-2 adapters.

- **+** Caches and hooks any internal activation, enabling ablation and activation patching
- **+** Covers 15,000+ models across 140+ architecture families via TransformerBridge
- **+** Default bridge output matches raw HuggingFace logits and activations
- **+** Extensive tutorials, ARENA exercises and a research gallery built on it
- **−** 4.0 removed HookedTransformer.from_pretrained, so older code needs migration
- **−** HookedSAETransformer was removed in 2.0; SAE work moved to SAELens
- **−** Mamba/SSM support is labeled experimental
- **−** Gated models such as Llama and Gemma need an HF_TOKEN

<sub>GPU optional · Needs HuggingFace Hub · Models: HuggingFace transformers models, GPT-2, Llama, Mistral, Gemma · [Repo](https://github.com/transformerlensorg/transformerlens) · [📖 Docs ↗](https://TransformerLensOrg.github.io/TransformerLens/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transformerlens/)</sub>

<a name="datasets"></a>
### #&#8288;49 [huggingface/datasets](https://github.com/huggingface/datasets) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Nov 2026</sub>

**Python library for loading, streaming and preprocessing ML datasets on Apache Arrow.**

Hugging Face Datasets loads public datasets from the Hub or local files (CSV, JSON, Parquet, Arrow, XML, text, audio, image, video, PDF, NIfTI) with `load_dataset()`. Data is stored as memory-mapped Apache Arrow, so datasets larger than RAM work, and `map()` results are cached and can run in parallel with `num_proc`. A streaming mode iterates over remote data without downloading it.

- **+** Memory-mapped Arrow storage lets datasets exceed available RAM
- **+** Streaming mode with `streaming=True` avoids downloading full datasets
- **+** Converts to NumPy, Pandas, Polars, PyTorch, TensorFlow, JAX and Spark
- **+** Automatic caching of map results; parallel processing via `map(num_proc=N)`
- **−** Tied to the Hugging Face Hub for the one-line public dataset loading
- **−** Audio, vision, PDF and NIfTI support need optional extras installed
- **−** Built-in similarity search depends on separate FAISS or Elasticsearch setups
- **−** Pinning dataset revisions is left to the user for reproducibility

<sub>no GPU · Needs Hugging Face Hub, Apache Arrow, FAISS (optional), Elasticsearch (optional) · [Repo](https://github.com/huggingface/datasets) · [📖 Docs ↗](https://huggingface.co/docs/datasets/) · [🌐 Site ↗](https://huggingface.co/datasets) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/datasets/)</sub>

<a name="modelscope"></a>
### #&#8288;50 [modelscope](https://github.com/modelscope/modelscope) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Nov 2026</sub>

**Python library for running and fine-tuning ModelScope Hub models.**

The core ModelScope Python library gives a unified `pipeline` interface for inference and a `Trainer` interface for fine-tuning and evaluation across NLP, CV, audio, multi-modal and science models. It also handles model and dataset download, versioning and caching against the ModelScope Hub. It runs on PyTorch, TensorFlow or ONNX, with per-domain pip extras.

- **+** Inference in a few lines via `pipeline`; fine-tuning via `build_trainer` and `trainer.train()`
- **+** Covers NLP, CV, audio, multi-modal and AI-for-science tasks under one API
- **+** Built-in Model-Hub and Dataset-Hub access with version control and cache management
- **+** Official CPU and GPU Docker images published for each release
- **−** README examples and Docker tags reference old stacks (Python 3.7/3.8, TF 1.15, torch 1.11/2.0.1)
- **−** Some audio models only support Python 3.7 and TensorFlow 1.15.4 on Linux
- **−** Vision models may need mmcv-full; audio models need libsndfile on Linux
- **−** Model catalog and many docs links center on modelscope.cn, in Chinese

<sub>GPU optional · Docker · Needs PyTorch, TensorFlow, ONNX, mmcv-full, libsndfile, ModelScope Hub · Models: PyTorch, TensorFlow, ONNX, LLM, multi-modal · [Repo](https://github.com/modelscope/modelscope) · [🌐 Site ↗](https://www.modelscope.cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/modelscope/)</sub>

<a name="monai"></a>
### #&#8288;51 [monai](https://github.com/project-monai/monai) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Nov 2026</sub>

**PyTorch framework for deep learning on medical imaging data.**

MONAI is a PyTorch-based Python library for training and evaluating deep learning models on healthcare imaging data. It provides pre-processing for multi-dimensional medical images, plus networks, losses and metrics specific to the domain, with multi-GPU and multi-node data parallelism. Pretrained models are shared in a separate Model Zoo using the MONAI Bundle format.

- **+** Domain-specific networks, losses and metrics for medical imaging, not generic vision only
- **+** Supports multi-GPU and multi-node data parallel training
- **+** Installs with pip, conda-forge or a Docker image; Apache-2.0 licensed
- **+** Separate Model Zoo and tutorials repo with Colab notebooks, plus Read the Docs API docs
- **−** Tied to PyTorch; supports the current release plus three previous minor versions
- **−** Scope is healthcare imaging; not a general-purpose ML or LLM library
- **−** README gives no hardware requirements such as RAM or VRAM
- **−** Many features depend on optional dependencies that need separate installation

<sub>GPU optional · Docker · Needs PyTorch, NumPy · Models: PyTorch, MONAI Bundle · [Repo](https://github.com/project-monai/monai) · [▶️ Demo ↗](https://colab.research.google.com/github/Project-MONAI/tutorials/blob/main/2d_classification/mednist_tutorial.ipynb) · [📖 Docs ↗](https://monai.readthedocs.io/) · [🌐 Site ↗](https://project-monai.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/monai/)</sub>

<a name="flashinfer"></a>
### #&#8288;52 [flashinfer](https://github.com/flashinfer-ai/flashinfer) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · Apache-2.0 · Nov 2026</sub>

**CUDA kernel library for LLM attention, GEMM, MoE and sampling.**

FlashInfer is a Python and CUDA library that provides GPU kernels for LLM inference: paged and ragged KV-cache attention, FP8/FP4 GEMM, fused MoE, and sorting-free Top-K/Top-P sampling. It selects among backends such as FlashAttention-2/3, cuDNN, CUTLASS and TensorRT-LLM, and runs on Turing through Blackwell GPUs. It is a building block for inference engines; the README lists SGLang, vLLM, TensorRT-LLM and TGI among adopters.

- **+** Covers attention, GEMM, MoE, sampling, RoPE and norm kernels behind one Python API
- **+** Supports SM 7.5 to SM 12.1, including FP8 and NVFP4/MXFP4 on Blackwell
- **+** Compatible with CUDAGraph and torch.compile for low-latency serving
- **+** Used by SGLang, vLLM, TensorRT-LLM, TGI and MLC-LLM per the README
- **−** Not a server or end-user tool; needs an inference engine or custom PyTorch code
- **−** NVIDIA GPUs only; not all features work on all compute capabilities
- **−** Kernels compile or download on first use unless cubin and JIT-cache wheels are installed
- **−** CUDA support limited to 12.9, 13.0 and 13.4; 13.4 runtime CI not covered

<sub>GPU required · Docker · Needs PyTorch, CUDA 12.9 or 13.0 · Models: DeepSeek MLA, Llama-4 MoE routing, DeepSeek-V3 MoE routing, LLaMA 3.1 RoPE · [Repo](https://github.com/flashinfer-ai/flashinfer) · [📖 Docs ↗](https://docs.flashinfer.ai) · [🌐 Site ↗](https://flashinfer.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flashinfer/)</sub>

<a name="huggingface-hub"></a>
### #&#8288;53 [huggingface_hub](https://github.com/huggingface/huggingface_hub) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · Apache-2.0 · Nov 2026</sub>

**Official hf CLI and Python client for the Hugging Face Hub.**

huggingface_hub is the official Python library and `hf` command-line tool for the Hugging Face Hub. It downloads and uploads models, datasets and Spaces, manages repos, searches the Hub, runs inference on deployed models and launches Jobs on Hugging Face infrastructure. It also ships an `hf` CLI skill that coding agents such as Claude Code, Codex and Cursor can load.

- **+** One package provides both the `hf` CLI and a Python API for downloads, uploads and repos
- **+** Local cache for downloaded files; Xet chunk-deduplicated storage on the Hub handles large files
- **+** `hf skills add` installs a command reference for Claude Code, Codex, Cursor and others
- **+** Optional extras such as `[mcp]` keep the default install minimal
- **−** Tied to the Hugging Face Hub; it is a client, not a self-hostable server
- **−** Inference and Jobs run on Hugging Face infrastructure, not locally
- **−** Uploads and private repos require an access token
- **−** Does not run models locally; a separate framework is needed for that

<sub>no GPU · Needs Hugging Face Hub account and access token · Models: Hub-hosted models and datasets, safetensors · [Repo](https://github.com/huggingface/huggingface_hub) · [📖 Docs ↗](https://huggingface.co/docs/huggingface_hub) · [🌐 Site ↗](https://huggingface.co/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/huggingface-hub/)</sub>

<a name="spacy"></a>
### #&#8288;54 [spacy](https://github.com/explosion/spacy) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Nov 2026</sub>

**Python and Cython NLP library with pretrained pipelines for 70+ languages.**

spaCy is a Python/Cython library for tokenization, tagging, dependency parsing, named entity recognition, text classification, lemmatization and entity linking. It ships pretrained pipelines installed as Python packages and a config-driven training system, and can use transformers such as BERT or custom PyTorch and TensorFlow models. LLMs can be added to pipelines through a documented integration.

- **+** Pretrained pipelines install as ordinary Python packages via `python -m spacy download`
- **+** Tokenization and training support for 70+ languages
- **+** Built-in training system, model packaging, and syntax and NER visualizers
- **+** Extensible with custom components; accepts PyTorch and TensorFlow models
- **−** README lists Python >=3.7, <3.13 only, 64-bit
- **−** Models may need re-downloading or retraining after spaCy upgrades
- **−** Library only; no model server or HTTP API included
- **−** Support is public only (GitHub, Stack Overflow); no individual email support

<sub>GPU optional · Needs Python >=3.7,<3.13, pip or conda · Models: spaCy pretrained pipelines, transformers (BERT), PyTorch, TensorFlow, word vectors · [Repo](https://github.com/explosion/spacy) · [📖 Docs ↗](https://spacy.io/usage) · [🌐 Site ↗](https://spacy.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/spacy/)</sub>

<a name="fastai"></a>
### #&#8288;55 [fastai](https://github.com/fastai/fastai) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · Apache-2.0 · Sep 2026</sub>

**High-level deep learning library on PyTorch for vision, text, tabular and recommenders.**

fastai is a Python deep learning library built on PyTorch. It offers high-level APIs that train image classifiers, segmentation, text sentiment, tabular and recommendation models in about 5 lines, on top of layered lower-level components for researchers. Core pieces include a data block API, a two-way callback system and an optimizer refactored into small composable parts.

- **+** Layered API: 5-line high-level training down to low-level building blocks
- **+** Two-way callbacks can modify data, model or optimizer at any point in training
- **+** Docs are runnable notebooks, with a free course and a book
- **+** Migration guides for plain PyTorch, Ignite, Lightning and Catalyst
- **−** Jupyter on Windows forces num_workers to 0, making vision training much slower
- **−** Covers classic deep learning domains; README does not mention LLM or diffusion workflows
- **−** README advises installing PyTorch separately before fastai

<sub>GPU optional · Compose · Needs PyTorch, fastcore · Models: PyTorch · [Repo](https://github.com/fastai/fastai) · [📖 Docs ↗](https://docs.fast.ai) · [🌐 Site ↗](https://docs.fast.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fastai/)</sub>

<a name="ggml"></a>
### #&#8288;56 [ggml](https://github.com/ggml-org/ggml) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Nov 2026</sub>

**C/C++ tensor library for ML inference with quantization and many backends.**

ggml is a dependency-free C/C++ tensor library that runs machine learning models on CPU, GPU, NPU and in the browser. It provides SIMD-optimized kernels and 2- to 8-bit integer quantization, plus MXFP4 and NVFP4, and it defines the GGUF file format. Changes to the core library are directed to llama.cpp rather than this repository.

- **+** Plain C/C++ with no dependencies; builds with CMake
- **+** Targets x86, ARM, RISC-V, LoongArch, PowerPC, s390x and WebAssembly
- **+** 2- to 8-bit integer quantization, plus MXFP4 and NVFP4 formats
- **+** Zero memory allocations at runtime
- **−** Low-level library, not a ready-to-use model server or app
- **−** Core changes are submitted via llama.cpp, not this repo
- **−** README gives no hardware requirements or list of supported models
- **−** Documentation is a GGUF spec plus a few external links

<sub>GPU optional · Models: GGUF · [Repo](https://github.com/ggml-org/ggml) · [📖 Docs ↗](https://huggingface.co/blog/introduction-to-ggml) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ggml/)</sub>

<a name="gymnasium"></a>
### #&#8288;57 [gymnasium](https://github.com/farama-foundation/gymnasium) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Nov 2026</sub>

**Python API and environment set for reinforcement learning research.**

Gymnasium is a Python library that defines a standard environment API (make, reset, step, action and observation spaces) for connecting reinforcement learning algorithms to environments. It ships Classic Control, Box2D, Toy Text, MuJoCo and Atari families. It is the maintained fork of OpenAI's Gym, run by the Farama Foundation.

- **+** Small, uniform env API with terminated and truncated flags
- **+** Environment families install separately via extras like gymnasium[atari] or gymnasium[all]
- **+** Strict -vN environment versioning to keep learning results reproducible
- **+** Third-party environments and libraries (CleanRL, PettingZoo) use the same API
- **−** Provides environments and an interface only; no RL algorithms included
- **−** Older Gym-based third-party environments may need apply_env_compatibility
- **−** Some environment families are hard to install on certain systems

<sub>Needs Python · [Repo](https://github.com/farama-foundation/gymnasium) · [📖 Docs ↗](https://gymnasium.farama.org) · [🌐 Site ↗](https://gymnasium.farama.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gymnasium/)</sub>

<a name="darts"></a>
### #&#8288;58 [darts](https://github.com/unit8co/darts) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Nov 2026</sub>

**Python library for time series forecasting and anomaly detection.**

Darts is a Python library that gives forecasting models, from ARIMA and exponential smoothing to deep networks such as N-BEATS, a common scikit-learn-style fit() and predict() interface. It also covers backtesting, probabilistic and conformal forecasts, covariates, and a darts.ad module of anomaly scorers and detectors, including PyOD wrappers. Deep learning models are built on PyTorch Lightning.

- **+** One fit()/predict() interface across statistical, ML and deep learning forecasting models
- **+** Built-in backtesting, probabilistic and conformal forecasts, and past, future and static covariates
- **+** Anomaly detection module with scorers, detectors, PyOD and forecast-model wrappers
- **+** Global models train on multiple series; TimeSeries converts to pandas, polars, numpy and others
- **−** Requires Python 3.11 or newer
- **−** Deep learning models depend on PyTorch Lightning, which adds a heavy install
- **−** Local statistical models such as ARIMA are fitted on one series at a time
- **−** Not LLM-related; fits this list only as a general ML library

<sub>GPU optional · Docker · Needs PyTorch Lightning, scikit-learn, pandas · Models: ARIMA, VARIMA, ExponentialSmoothing, N-BEATS, TCN · [Repo](https://github.com/unit8co/darts) · [📖 Docs ↗](https://unit8co.github.io/darts/userguide.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/darts/)</sub>

<a name="flux-jl"></a>
### #&#8288;59 [flux.jl](https://github.com/fluxml/flux.jl) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · custom license · Nov 2026</sub>

**Pure-Julia machine learning library with layers, losses and pluggable autodiff.**

Flux is a machine learning library written entirely in Julia. It provides layers and losses for MLP, convolutional, recurrent and attention models, and trains with Zygote by default, or Enzyme or Mooncake. It runs on NVIDIA, AMD and Apple GPUs, can compile a training step through Reactant to XLA, and supports MPI and NCCL distributed training.

- **+** Models are plain Julia: any parameterised callable, such as a closure, works as a model
- **+** Selectable AD engine: Zygote default, Enzyme or Mooncake as alternatives
- **+** GPU support for NVIDIA, AMD and Apple through CUDA, AMDGPU or Metal packages
- **+** Reactant integration fuses the training step into one XLA program for CPU, GPU or TPU
- **−** Requires Julia, so Python-based model code and tooling do not carry over
- **−** License is reported as NOASSERTION, so terms need manual checking
- **−** GPU use needs a separate backend package loaded alongside Flux
- **−** Model zoo and larger examples live in separate repos or folders, not the core package

<sub>GPU optional · Needs Julia 1.10 or later · Models: MLP, convolutional, recurrent, attention · [Repo](https://github.com/fluxml/flux.jl) · [📖 Docs ↗](https://fluxml.ai/Flux.jl/stable/) · [🌐 Site ↗](https://fluxml.ai/Flux.jl/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flux-jl/)</sub>

<a name="pytorch-lightning"></a>
### #&#8288;60 [pytorch-lightning](https://github.com/lightning-ai/pytorch-lightning) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · Apache-2.0 · Nov 2026</sub>

**PyTorch training framework that automates multi-GPU, precision and logging boilerplate.**

PyTorch Lightning structures PyTorch code into a LightningModule and a Trainer that handles the training loop, mixed precision, checkpointing, early stopping and logging. The same code runs on CPU, GPU, TPU or multi-node setups by changing Trainer arguments. The repo also ships Lightning Fabric, a lower-level API that keeps your own training loop while handling device placement, DDP, FSDP and DeepSpeed.

- **+** Scales from CPU to multi-node GPU or TPU by changing Trainer arguments, not model code
- **+** Fabric keeps a custom training loop with few changes to plain PyTorch
- **+** Built-in loggers for TensorBoard, Weights & Biases, Comet and MLflow
- **+** Exports trained modules to TorchScript and ONNX
- **−** Requires restructuring code into LightningModule and Trainer conventions
- **−** README states about 300 ms per epoch overhead versus plain PyTorch
- **−** README promotes Lightning Cloud and Studios for examples and GPUs
- **−** PyTorch only; no support for other tensor frameworks

<sub>GPU optional · Needs PyTorch, torchvision (for examples) · Models: PyTorch nn.Module, TorchScript export, ONNX export, DDP, FSDP · [Repo](https://github.com/lightning-ai/pytorch-lightning) · [📖 Docs ↗](https://pytorch-lightning.readthedocs.io/en/stable/) · [🌐 Site ↗](https://lightning.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-lightning/)</sub>

<a name="sentencepiece"></a>
### #&#8288;61 [sentencepiece](https://github.com/google/sentencepiece) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

**Unsupervised BPE and unigram subword tokenizer trained from raw text.**

SentencePiece trains BPE or unigram language model tokenizers directly from raw sentences, treating whitespace as the symbol ▁ so detokenization is lossless and language-independent. The core is C++ with a Python module installed via pip. The repo also ships SentencePiece Lite, a zero-dependency C++20 runtime that memory-maps FlatBuffers model files.

- **+** Lossless, reversible tokenization with no language-specific pre-tokenizer, incl. Chinese, Japanese, Thai
- **+** Supports subword regularization (unigram) and BPE-Dropout via enable_sampling, alpha and nbest_size
- **+** Single .model file holds normalization, vocabulary and segmentation; same results in C++ and Python
- **+** README benchmark: 27.41 MB/s single-thread on T5-base unigram vs 3.78 for Hugging Face Fast
- **−** Tokenizer only; no model training or inference beyond tokenization
- **−** README states it is not an official Google product
- **−** Multi-thread scaling flattens because Python object conversion holds the GIL
- **−** Benchmarks are the project's own, on one dataset and one 24-core machine

<sub>no GPU · Models: BPE, Unigram language model · [Repo](https://github.com/google/sentencepiece) · [📖 Docs ↗](https://google.github.io/sentencepiece/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sentencepiece/)</sub>

<a name="sktime"></a>
### #&#8288;62 [sktime](https://github.com/sktime/sktime) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · BSD-3-Clause · Nov 2026</sub>

**Python library with one scikit-learn-style API for time series tasks.**

sktime provides a unified fit/predict interface for forecasting, time series classification, regression, clustering, and anomaly and changepoint detection. It includes native algorithms and interfaces to statsmodels, tsfresh, PyOD, and Prophet. Pipelining, ensembling, tuning, and reduction let an algorithm built for one task be applied to another.

- **+** Covers forecasting, classification, regression, clustering, and detection under one API
- **+** Composition tools: pipelines, ensembles, tuning, and reduction to scikit-learn regressors
- **+** Interfaces to statsmodels, tsfresh, PyOD, and Prophet behind the same API
- **+** Extension templates for custom estimators; installs via pip or conda-forge
- **−** Detection, clustering, and distances modules are maturing; alignment is experimental
- **−** Task extras install only a curated subset of soft dependencies
- **−** conda offers only base or all-extras, no flexible dependency sets

<sub>Needs scikit-learn, statsmodels, tsfresh, PyOD, fbprophet · Models: scikit-learn estimators, ThetaForecaster, TimeSeriesForestClassifier · [Repo](https://github.com/sktime/sktime) · [▶️ Demo ↗](https://mybinder.org/v2/gh/sktime/sktime/main?filepath=examples) · [📖 Docs ↗](https://www.sktime.net/en/stable/users.html) · [🌐 Site ↗](https://www.sktime.net) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sktime/)</sub>

<a name="umap"></a>
### #&#8288;63 [umap](https://github.com/lmcinnes/umap) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · BSD-3-Clause · Nov 2026</sub>

**Python UMAP dimension reduction with a scikit-learn API.**

umap-learn implements Uniform Manifold Approximation and Projection as a scikit-learn-style transformer, usable for 2D visualisation or general non-linear dimension reduction. It supports many distance metrics, sparse input, supervised fitting, transform on new points, densMAP, and Parametric UMAP via TensorFlow. Numba provides the speed, and pynndescent handles nearest neighbours.

- **+** Drop-in sklearn fit/transform API, works inside pipelines
- **+** Embeds 70000x784 MNIST in about 42 seconds on a 3.1 GHz i7, per README
- **+** Many metrics incl. cosine and correlation; custom numba-JITed functions; sparse input
- **+** Supervised and semi-supervised embedding by passing labels as y
- **−** Runs on CPU only; GPU use requires the separate torchdr package
- **−** Numba JIT warmup adds delay on first run
- **−** Parametric UMAP needs TensorFlow installed separately
- **−** Plotting needs extra dependencies (matplotlib, datashader, holoviews)

<sub>no GPU · Needs numpy, scipy, scikit-learn, numba, tqdm, pynndescent · [Repo](https://github.com/lmcinnes/umap) · [📖 Docs ↗](https://umap-learn.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/umap/)</sub>

<a name="sahi"></a>
### #&#8288;64 [sahi](https://github.com/obss/sahi) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · MIT · Nov 2026</sub>

**Sliced inference library for detecting small objects in large images.**

SAHI splits large images into overlapping slices, runs an object detection or instance segmentation model on each slice, and merges the results. It wraps Ultralytics YOLO, MMDetection, Hugging Face, TorchVision, Roboflow RF-DETR, YOLOv5, Detectron2 and GroundingDINO models behind one Python API and a `sahi` CLI. The CLI also slices COCO datasets, evaluates COCO AP/AR, produces error analysis plots and converts COCO to YOLO format.

- **+** Works with many detectors: Ultralytics, MMDetection, Hugging Face, TorchVision, RF-DETR, Detectron2
- **+** CLI covers prediction, COCO slicing, evaluation, error analysis and COCO-to-YOLO conversion
- **+** Installs with pip install sahi; detection frameworks are optional extras
- **+** Backed by an ICIP 2022 paper and Colab notebooks per framework
- **−** Does not ship models; you install torch and a detection framework yourself
- **−** mmdet support requires torch 2.1.2, and YOLOv5 needs the pinned sahi 0.12.1
- **−** Library only: no web UI, server or hosted API
- **−** Slicing runs one forward pass per tile, so large images cost more inference time

<sub>Needs torch, torchvision, ultralytics, transformers, mmdet, yolov5 or rfdetr (one of, as needed) · Models: Ultralytics YOLO, MMDetection, Hugging Face, TorchVision, Roboflow RF-DETR · [Repo](https://github.com/obss/sahi) · [▶️ Demo ↗](https://huggingface.co/spaces/fcakyon/sahi-yolox) · [📖 Docs ↗](https://github.com/obss/sahi/blob/main/docs/cli.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sahi/)</sub>

<a name="tinygrad"></a>
### #&#8288;65 [tinygrad](https://github.com/tinygrad/tinygrad) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Nov 2026</sub>

**Small deep learning stack with tensors, autograd, and a readable compiler.**

tinygrad is a Python tensor library with autograd, an IR and compiler that fuses and lowers kernels, a JIT (TinyJit) with graph execution, and nn, optim and dataset modules for training. It targets OpenCL, CPU, Metal, CUDA, AMD, NV, QCOM and WebGPU, and a new backend needs about 25 low-level ops. The API follows PyTorch, but the compiler and IR are kept small enough to read and modify.

- **+** Whole compiler and IR are visible and hackable, unlike PyTorch
- **+** Eager Tensor API and autograd close to PyTorch, so training loops look familiar
- **+** Backends for OpenCL, CPU, Metal, CUDA, AMD, NV, QCOM and WebGPU
- **+** New accelerator needs only about 25 low-level ops
- **−** Fewer functional transforms than JAX: no full vmap or pmap yet
- **−** README says the library is not 1.0 yet
- **−** Recommended install is from source; no PyPI instructions in the README
- **−** Strict contribution rules: AI-looking PRs from new contributors are closed

<sub>GPU optional · Models: OpenCL, CPU, Metal, CUDA, AMD · [Repo](https://github.com/tinygrad/tinygrad) · [📖 Docs ↗](https://docs.tinygrad.org/) · [🌐 Site ↗](https://tinygrad.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tinygrad/)</sub>

<a name="ncnn"></a>
### #&#8288;66 [ncnn](https://github.com/tencent/ncnn) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Nov 2026</sub>

**C++ neural network inference library for mobile, embedded and desktop devices.**

ncnn runs neural network inference in C++ (with a Python binding) on CPU or Vulkan GPU backends, with no third-party runtime dependencies. Models are converted from PyTorch or ONNX with the pnnx tool into .param and .bin files. It targets phones, PCs, browsers via WebAssembly and edge devices, and is used in Tencent apps such as QQ and WeChat.

- **+** No third-party runtime dependencies; CPU and Vulkan GPU backends
- **+** Prebuilt packages for Android, iOS, HarmonyOS, macOS, Linux, Windows and WebAssembly
- **+** pnnx converts PyTorch and ONNX models; C++ and Python APIs
- **+** Build guides for Raspberry Pi, Jetson, MIPS, POWER, AllWinner D1, Loongson
- **−** Library only: no HTTP server or OpenAI-compatible API included
- **−** Models must be converted to ncnn's own param/bin format first
- **−** Embedded targets need cross-compiling with manual steps from the wiki
- **−** License reported as NOASSERTION, although the README badge says BSD 3-Clause

<sub>GPU optional · Models: PyTorch (via pnnx), ONNX, ncnn param/bin · [Repo](https://github.com/tencent/ncnn) · [📖 Docs ↗](https://github.com/Tencent/ncnn/wiki/use-ncnn-with-pytorch-or-onnx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ncnn/)</sub>

<a name="wandb"></a>
### #&#8288;67 [wandb](https://github.com/wandb/wandb) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Nov 2026</sub>

**Python SDK for tracking ML experiments and versioning datasets and models.**

The wandb Python client logs hyperparameters and metrics from training scripts or notebooks to a W&B server, where runs are visualized and compared. It also covers dataset and model versioning, with integrations for common ML frameworks. The backend is a hosted service or a W&B Server install on AWS, GCP, Azure or on-premises.

- **+** Adds tracking with wandb.init() and run.log() in an existing training script
- **+** Integrates with popular ML frameworks and libraries for tracking and data versioning
- **+** Hosted multi-tenant, dedicated cloud, or self-managed server options
- **+** Weave, a separate suite, covers tracing and evaluation of LLM apps
- **−** This repo is the client SDK; the server and dashboard are not included
- **−** Needs a W&B account and API key for the default hosted setup
- **−** Self-managed server requirements and licensing are not described in the README
- **−** LLM tracing lives in Weave, a separate project

<sub>no GPU · Needs W&B account and API key, W&B Cloud or W&B Server · [Repo](https://github.com/wandb/wandb) · [📖 Docs ↗](https://docs.wandb.ai) · [🌐 Site ↗](https://wandb.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/wandb/)</sub>

<a name="cutlass"></a>
### #&#8288;68 [cutlass](https://github.com/nvidia/cutlass) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Nov 2026</sub>

**CUDA C++ templates and Python DSL for writing GEMM and tensor kernels.**

CUTLASS is a library of CUDA C++ template abstractions for building matrix-multiply (GEMM) and related kernels, with CuTe layout and tensor primitives at its core. Version 4 adds CuTe DSL, a Python interface (public beta) for writing kernels against the same concepts with faster compile times. It covers FP64 down to FP4 and block-scaled types on Volta through Blackwell, with initial Rubin (SM107) support.

- **+** Supports FP64, FP32, TF32, FP16, BF16, FP8, NVFP4, MXFP4/6/8 and integer types
- **+** CuTe DSL lets kernels be written in Python without deep C++ template expertise
- **+** Covers Volta, Turing, Ampere, Ada, Hopper and Blackwell, with initial Rubin support
- **+** Tested against FlashAttention, FlashInfer, PyTorch and TensorRT-LLM
- **−** NVIDIA GPUs only; requires CUDA Toolkit 11.4 or newer and a C++17 compiler
- **−** CuTe DSL is in public beta, and the extension compiler is an opt-in preview
- **−** Rubin kernels need the R615 driver; some packed ops miscompile on Rubin
- **−** Low-level kernel library, not a ready-to-use inference or training tool

<sub>GPU required · Needs CUDA Toolkit 11.4+ (12.8 recommended), C++17 compiler, NVIDIA GPU, compute capability 7.0+ · [Repo](https://github.com/nvidia/cutlass) · [📖 Docs ↗](https://docs.nvidia.com/cutlass/latest/media/docs/cpp/quickstart.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cutlass/)</sub>

<a name="pyod"></a>
### #&#8288;69 [pyod](https://github.com/yzhao062/pyod) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · BSD-2-Clause · Nov 2026</sub>

**Python library of 61 anomaly detectors with fit/predict API and agent skill.**

PyOD is a Python library for outlier detection covering tabular, time series, graph, text, image and audio data through a scikit-style fit/decision_function/predict API. Version 3 adds ADEngine, which selects, compares and assesses detectors automatically, plus an od-expert skill for Claude Code and Codex and an MCP server exposing ten stateless tools.

- **+** 61 detectors across six modalities behind one fit/predict interface
- **+** Classic API unchanged in v3, so existing code keeps working
- **+** Optional MCP server and Claude Code/Codex skill for agent-driven detection
- **+** Benchmark-backed model selection using ADBench, TSB-AD, BOND and NLP-ADBench
- **−** MCP investigate and iterate tools are stateful and deferred, not yet available
- **−** Full multi-turn agentic flow needs Claude Code or Codex via the skill
- **−** Models persist via joblib or pickle, with the usual pickle trust caveats
- **−** README excerpt gives no RAM, GPU or per-detector scaling figures

<sub>Needs numba, SUOD, mcp (optional extra) · Models: tabular, time series, graph, text, image · [Repo](https://github.com/yzhao062/pyod) · [▶️ Demo ↗](https://htmlpreview.github.io/?https://github.com/yzhao062/pyod/blob/development/examples/agentic_demo.html) · [📖 Docs ↗](https://pyod.readthedocs.io/en/latest/) · [🌐 Site ↗](https://pyod.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyod/)</sub>

<a name="dali"></a>
### #&#8288;70 [dali](https://github.com/nvidia/dali) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Nov 2026</sub>

**GPU-accelerated data loading and preprocessing library for deep learning pipelines.**

DALI moves image, video and audio decoding and augmentation (crop, resize, normalize) from the CPU to the GPU, using its own execution engine with prefetching and parallel execution. Pipelines are written in a Python functional API, in pipeline mode or the newer dynamic mode, and plug into PyTorch, TensorFlow, PaddlePaddle and JAX. It also has a Triton Inference Server backend.

- **+** Decodes JPEG, JPEG 2000, H.264, VP9, HEVC and audio formats on the GPU
- **+** One pipeline definition retargets to PyTorch, TensorFlow, PaddlePaddle or JAX
- **+** Supports GPUDirect Storage and multi-GPU scaling
- **+** Custom operators and a Triton Inference Server backend
- **−** Requires an NVIDIA driver and CUDA Toolkit; README documents no AMD or Apple GPU path
- **−** Pipeline mode and dynamic mode are two separate APIs to learn
- **−** Installation is tied to a CUDA major version via separate pip packages
- **−** Roadmap link in the README refers to a 2024 plan

<sub>GPU required · Docker · Needs NVIDIA driver, CUDA Toolkit · Models: PyTorch, TensorFlow, PaddlePaddle, JAX · [Repo](https://github.com/nvidia/dali) · [📖 Docs ↗](https://docs.nvidia.com/deeplearning/dali/user-guide/docs/index.html) · [🌐 Site ↗](https://developer.nvidia.com/DALI) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dali/)</sub>

<a name="isaacsim"></a>
### #&#8288;71 [isaacsim](https://github.com/isaac-sim/isaacsim) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (49) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · custom license · Nov 2026</sub>

**NVIDIA robotics simulator on Omniverse with RTX sensors and GPU physics.**

Isaac Sim is a robot simulator built on NVIDIA Omniverse. It imports robots from URDF, MJCF and CAD, and simulates them with GPU-accelerated physics and RTX-rendered sensors. It includes ROS 2 integration, synthetic data generation and Isaac Lab for reinforcement and imitation learning. It is built from source with build.sh or build.bat, or installed as Python wheels from pypi.nvidia.com.

- **+** Imports URDF, MJCF and CAD robot descriptions for simulation
- **+** Covers RL, synthetic data generation and ROS bridge in one platform
- **+** Runs on Linux x86_64, Linux aarch64 and Windows; pip wheels for releases
- **+** Docs include quickstart tutorials and a USD asset catalog
- **−** Needs an RTX-class GPU; stated minimum is an RTX 4080 or A40
- **−** Linux build requires GCC/G++ 11; newer compilers are unsupported
- **−** Build downloads Omniverse Kit SDK and extensions, so internet access is required
- **−** First launch can take several minutes while extensions and shaders cache

<sub>GPU required · Needs NVIDIA Omniverse Kit SDK, Git LFS, GCC/G++ 11 (Linux), Visual Studio 2022 (Windows C++), NVIDIA driver, Python 3.12 · Models: URDF, MJCF, CAD, USD · [Repo](https://github.com/isaac-sim/isaacsim) · [📖 Docs ↗](https://docs.isaacsim.omniverse.nvidia.com/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/isaacsim/)</sub>

<a name="keras"></a>
### #&#8288;72 [keras](https://github.com/keras-team/keras) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Nov 2026</sub>

**Multi-backend deep learning framework running on JAX, TensorFlow and PyTorch.**

Keras 3 is a high-level Python deep learning library that runs the same model code on JAX, TensorFlow or PyTorch, with an inference-only OpenVINO backend. The backend is chosen with the KERAS_BACKEND variable or ~/.keras/keras.json before import. It is meant as a drop-in replacement for tf.keras and accepts tf.data and PyTorch DataLoader inputs.

- **+** Same model code runs on JAX, TensorFlow or PyTorch by changing one environment variable
- **+** Drop-in replacement for tf.keras on the TensorFlow backend using the .keras format
- **+** Keras models can be used inside PyTorch Modules, JAX functions or native training loops
- **+** Accepts tf.data.Dataset and PyTorch DataLoader inputs on any backend
- **−** Backend must be set before import and cannot be changed afterward
- **−** OpenVINO backend supports only model.predict(), no training
- **−** Windows not directly supported; README recommends WSL2
- **−** Custom layers or train_step may need rewriting to be backend-agnostic

<sub>GPU optional · Needs One backend: TensorFlow >=2.16.1, JAX >=0.4.20 or PyTorch >=2.6.0, OpenVINO 2026.2.0 (inference only), NVIDIA driver for CUDA GPU use · Models: JAX, TensorFlow, PyTorch, OpenVINO (inference only) · [Repo](https://github.com/keras-team/keras) · [🌐 Site ↗](https://keras.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/keras/)</sub>

<a name="vision"></a>
### #&#8288;73 [vision](https://github.com/pytorch/vision) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · BSD-3-Clause · Nov 2026</sub>

**PyTorch library of vision datasets, model architectures and image transforms.**

torchvision is the computer vision companion package to PyTorch. It provides dataset loaders, pre-trained model architectures and image transformations, working on torch tensors or PIL images (Pillow or Pillow-SIMD). Each release is paired with a specific torch version, for example torchvision 0.28 with torch 2.13 on Python 3.10 to 3.14.

- **+** Maintained in the pytorch organization, with releases matched to each torch version
- **+** Supports torch tensor and PIL image backends, with optional Pillow-SIMD
- **+** Bundles datasets, model architectures and transforms in one package
- **+** API reference published on pytorch.org
- **−** Each release only works with its matching torch version
- **−** Requires PyTorch; not usable with other tensor frameworks
- **−** Some pre-trained weights have separate licenses, e.g. SWAG is CC-BY-NC 4.0
- **−** Dataset loaders only download public data; license checks are left to the user

<sub>Needs torch, Pillow (optional Pillow-SIMD) · Models: PyTorch, torch tensors, PIL images · [Repo](https://github.com/pytorch/vision) · [📖 Docs ↗](https://pytorch.org/vision/stable/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vision/)</sub>

<a name="stanza"></a>
### #&#8288;74 [stanza](https://github.com/stanfordnlp/stanza) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · custom license · Nov 2026</sub>

**Python NLP toolkit for tokenizing, tagging and parsing text in 60+ languages.**

Stanza is the Stanford NLP Group's Python library with a PyTorch neural pipeline for tokenization, multi-word token expansion, POS and morphological tagging, lemmatization, Universal Dependencies parsing and NER. It also includes a wrapper for calling the Java Stanford CoreNLP software from Python. Biomedical and clinical English model packages are available.

- **+** Models for 60+ languages, covering all Universal Dependencies v2.8 treebanks
- **+** Each neural module can be retrained on your own CoNLL-U or BIOES data
- **+** Official Python client for Java CoreNLP, including Semgrex and Ssurgeon
- **+** Separate biomedical and clinical English models for syntax and NER
- **−** Training is not supported through the Pipeline interface; requires a source checkout
- **−** Per-sentence calls are slow; documents must be concatenated and batched manually
- **−** NER models exist only for a few widely spoken languages
- **−** CoreNLP use needs a separate Java download and CORENLP_HOME setup

<sub>GPU optional · Needs PyTorch, Stanford CoreNLP (Java, optional) · Models: Universal Dependencies treebank models, NER models, Biomedical and clinical English models · [Repo](https://github.com/stanfordnlp/stanza) · [📖 Docs ↗](https://stanfordnlp.github.io/stanza/installation_usage.html) · [🌐 Site ↗](https://stanfordnlp.github.io/stanza/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/stanza/)</sub>

<a name="flax"></a>
### #&#8288;75 [flax](https://github.com/google/flax) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Nov 2026</sub>

**Neural network library for JAX built around mutable Python objects.**

Flax is a neural network library for JAX. Its current API, Flax NNX, lets you define models as regular Python objects with reference sharing and mutability, and ships layers such as Linear, Conv, BatchNorm, LayerNorm, MultiHeadAttention, LSTMCell and Dropout. It also includes utilities for replicated training, checkpointing and metrics, plus MNIST and Gemma inference examples.

- **+** Flax NNX models are plain Python objects, so they can be inspected and debugged directly
- **+** Developed with the JAX team; runs on CPU, GPU and TPU through JAX
- **+** Includes common layers plus checkpointing, serialization, metrics and device prefetching
- **+** Built for forking examples and editing the training loop, not extending a framework
- **−** Two APIs exist, Linen and NNX, with separate docs sites and a migration guide
- **−** Requires JAX and its own accelerator setup, which Flax does not handle
- **−** Only MNIST and Gemma inference are listed as built-in examples
- **−** Described as not an official Google product

<sub>GPU optional · Needs JAX, Python 3.8+ · Models: Gemma (inference example), MLP, CNN, autoencoder · [Repo](https://github.com/google/flax) · [📖 Docs ↗](https://flax.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flax/)</sub>

<a name="flower"></a>
### #&#8288;76 [flower](https://github.com/flwrlabs/flower) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Nov 2026</sub>

**Python framework for federated learning across clients with any ML library.**

Flower (`flwr`) is a Python framework for building federated learning and federated analytics systems, where training runs on client devices and a server aggregates the results. It works with PyTorch, TensorFlow, Hugging Face Transformers, JAX, scikit-learn, MLX, XGBoost and others. The repo ships tutorials, quickstart examples, and community baselines that reproduce published federated learning papers.

- **+** Framework-agnostic: documented quickstarts for PyTorch, TensorFlow, JAX, scikit-learn, MLX, XGBoost and more
- **+** Baselines reproduce papers such as FedProx, FedAvg, FedBN, MOON and FedNova
- **+** Examples cover Android (TFLite), iOS (CoreML), Raspberry Pi and Jetson clients
- **+** Examples include federated fine-tuning of LLMs, Whisper and vision transformers
- **−** README gives no hardware requirements; RAM and GPU needs depend on the chosen ML framework
- **−** Privacy and security and scaling tutorials are listed as not yet written
- **−** Focused on federated training; not a general-purpose model server or app
- **−** README does not describe deployment setup; Docker images are only linked via a badge

<sub>GPU optional · Models: PyTorch, TensorFlow, Hugging Face Transformers, PyTorch Lightning, scikit-learn · [Repo](https://github.com/flwrlabs/flower) · [📖 Docs ↗](https://flower.ai/docs/) · [🌐 Site ↗](https://flower.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flower/)</sub>

<a name="river"></a>
### #&#8288;77 [river](https://github.com/online-ml/river) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · BSD-3-Clause · Nov 2026</sub>

**Python library for online machine learning on streaming data.**

River implements online machine learning algorithms in Python, where models update one sample at a time through learn_one and predict_one. It covers linear models, decision trees, nearest neighbors, anomaly and drift detection, clustering, bandits and time series forecasting, plus metrics and progressive validation. It resulted from merging creme and scikit-multiflow.

- **+** Models learn per sample without revisiting past data, suited to event-based streams
- **+** Broad algorithm set: trees, linear models, drift detection, clustering, bandits, forecasting
- **+** Core learn_one/predict_one interface has no pandas dependency
- **+** Wheels for Linux, macOS and Windows; BSD-3-Clause license
- **−** README states it favors clarity over performance
- **−** Requires Python 3.11 or newer
- **−** Mini-batch methods need the optional pandas extra
- **−** Building from source needs Cython and Rust

<sub>no GPU · Needs Python 3.11+, pandas (optional, for mini-batch) · Models: linear models, decision trees, random forests, nearest neighbors, clustering · [Repo](https://github.com/online-ml/river) · [📖 Docs ↗](https://riverml.xyz) · [🌐 Site ↗](https://riverml.xyz) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/river/)</sub>

<a name="nlpaug"></a>
### #&#8288;78 [nlpaug](https://github.com/makcedward/nlpaug) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (50) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · MIT · Oct 2026</sub>

**Python library for augmenting text, audio and spectrogram training data.**

nlpaug is a Python library that generates synthetic training data by applying augmenters to text, audio waveforms and spectrograms. Text augmenters work at character, word and sentence level, using keyboard and OCR error simulation, WordNet/PPDB synonyms, word embeddings, BERT-family and GPT2 models, and back-translation. Augmenters can be chained with Sequential or Sometimes flows. Version 2.0.x requires Python 3.12+.

- **+** Covers character, word and sentence text augmentation plus audio and spectrogram in one API
- **+** Sequential and Sometimes flows chain augmenters; change-log records what was modified
- **+** Optional extras (transformers, nltk, word-embs, audio, lambada) keep core install light
- **+** Default pytest suite runs offline with mocked transformer models
- **−** Requires Python 3.12+ in 2.x, excluding older environments
- **−** WordEmbsAug needs manual download of word2vec, GloVe or fasttext files
- **−** Transformer-based augmenters pull heavy dependencies such as torch
- **−** Does not generate data with modern instruction-tuned LLMs; relies on classic models like BERT and GPT2

<sub>GPU optional · Needs nltk, transformers, torch, gensim, librosa, PPDB language pack (optional) · Models: BERT, DistilBERT, RoBERTa, XLNet, GPT2 · [Repo](https://github.com/makcedward/nlpaug) · [📖 Docs ↗](https://nlpaug.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nlpaug/)</sub>

<a name="prophet"></a>
### #&#8288;79 [prophet](https://github.com/meta/prophet) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Nov 2026</sub>

**Additive time series forecasting library for Python and R.**

Prophet fits an additive model to time series, combining a non-linear trend with yearly, weekly and daily seasonality and holiday effects. It runs on Stan (cmdstan via cmdstanpy in Python, rstan in R) and includes cross-validation, performance metrics and plotting. It suits series with strong seasonality and several seasons of history. The project has been in maintenance mode since v1.4.0.

- **+** Python (PyPI, conda-forge) and R packages with matching APIs
- **+** Handles missing data, trend shifts and holiday effects
- **+** Built-in cross-validation, performance metrics and custom metrics
- **+** Pre-built Python wheels bundle model binaries, including macOS arm64
- **−** Maintenance mode since v1.4.0: bug fixes only, no new features planned
- **−** CRAN release is outdated; latest R version installs from GitHub
- **−** Installing from source needs a C++ compiler and at least 4GB memory
- **−** Suited to series with strong seasonality and several seasons of history

<sub>RAM ≥ 2 GB · no GPU · Docker + Compose · Needs cmdstan, cmdstanpy, rstan, C++ compiler · Models: additive time series model (Stan) · [Repo](https://github.com/meta/prophet) · [📖 Docs ↗](https://facebook.github.io/prophet/docs/quick_start.html) · [🌐 Site ↗](https://facebook.github.io/prophet/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/prophet/)</sub>

<a name="anomalib"></a>
### #&#8288;80 [anomalib](https://github.com/open-edge-platform/anomalib) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Nov 2026</sub>

**Library for training and benchmarking visual anomaly detection models.**

Anomalib collects image and video anomaly detection algorithms such as Patchcore, Padim and Stfpm, with benchmark datasets like MVTec AD. It offers a Python API and an `anomalib` CLI for training, prediction and benchmarking, and most models export to OpenVINO. It also includes Anomalib Studio, a pre-release low-code web app for training and deploying models from cameras or image folders.

- **+** Many ready-made anomaly detection models and benchmark datasets behind one API and CLI
- **+** Most models export to OpenVINO for inference on Intel hardware
- **+** Install extras for CPU, CUDA 12.6/13.0, ROCm and Intel XPU
- **+** Built-in benchmark command and Lightning loggers (W&B, Comet, TensorBoard)
- **−** Focused on visual anomaly detection; not for tabular or time-series data
- **−** Anomalib Studio is pre-release and may be incomplete or unstable
- **−** Intel GPU training supports a single GPU only
- **−** v2.7.0 raised minimum PyTorch to 2.10+ and removed the legacy ONNX exporter

<sub>GPU optional · Needs PyTorch 2.10+, Lightning 2.2+, OpenVINO 2024.0+ (optional) · Models: Patchcore, Padim, Stfpm, WinCLIP, MH-PatchCore · port 3000 · [Repo](https://github.com/open-edge-platform/anomalib) · [📖 Docs ↗](https://anomalib.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/anomalib/)</sub>

<a name="transformerengine"></a>
### #&#8288;81 [transformerengine](https://github.com/nvidia/transformerengine) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Nov 2026</sub>

**NVIDIA library for FP8 and FP4 Transformer training in PyTorch and JAX.**

Transformer Engine provides fused kernels and drop-in modules for attention, linear layers, normalization and MoE, with autocast-style APIs for PyTorch and JAX. It manages scaling factors and amax histories for FP8, MXFP8 and NVFP4 recipes, so low-precision training can be added without rewriting a training stack. It also supports tensor, sequence, context and expert parallelism with communication overlap.

- **+** Handles FP8 scaling factors and amax histories automatically via configurable recipes
- **+** Supports both PyTorch and JAX with autocast-style contexts
- **+** FP8 on Hopper, Ada, Blackwell, Rubin; MXFP8 and NVFP4 on Blackwell
- **+** Integrated with Megatron-LM, Hugging Face Accelerate, Lightning and NeMo Megatron Bridge
- **−** NVIDIA GPUs only; low-precision modes depend on specific GPU generations
- **−** Training-focused; the README describes no inference or serving path
- **−** Install needs --no-build-isolation; source builds have extra prerequisites
- **−** No Docker image in the repo; ready-to-run setup relies on NGC containers

<sub>GPU required · Needs PyTorch or JAX, NVIDIA CUDA · Models: Transformer models, MoE, FP8, MXFP8, NVFP4 · [Repo](https://github.com/nvidia/transformerengine) · [📖 Docs ↗](https://docs.nvidia.com/deeplearning/transformer-engine/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transformerengine/)</sub>

<a name="tract"></a>
### #&#8288;82 [tract](https://github.com/sonos/tract) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · custom license · Nov 2026</sub>

**Rust inference engine for ONNX and NNEF models on embedded, GPU and WASM targets.**

tract loads ONNX, NNEF and TensorFlow Lite models, optimises them, and runs them on CPU (x86, ARM, hand-written SIMD kernels), Apple Metal, NVIDIA CUDA or WebAssembly. Sonos uses it in production for wake-word and streaming speech recognition. Models can be converted once to NNEF (tract-OPL) so only a small runtime ships. Rust and Python APIs are provided.

- **+** Targets Cortex-A7 to x86, RISC-V, Metal, CUDA and WebAssembly, benchmarked nightly
- **+** Convert to NNEF once, then ship only tract-core and tract-nnef without protobuf
- **+** Pulsification turns sequence models into fixed-size streaming ones for real-time audio
- **+** Original code dual-licensed MIT/Apache-2.0; Rust crate and Python package on PyPI
- **−** Library and CLI only; no HTTP server or OpenAI-compatible API
- **−** ONNX is load-only; saving a converted model goes through NNEF
- **−** Only the top-level tract crate is a stable API; internal crates are not
- **−** tract-OPL extensions still change; compatibility only promised within 0.x patch releases

<sub>GPU optional · Models: ONNX, NNEF, TensorFlow Lite, TensorFlow 1 frozen graph · [Repo](https://github.com/sonos/tract) · [📖 Docs ↗](https://sonos.github.io/tract) · [🌐 Site ↗](https://sonos.github.io/tract/bench/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tract/)</sub>

<a name="lmms-eval"></a>
### #&#8288;83 [lmms-eval](https://github.com/evolvinglmms-lab/lmms-eval) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · custom license · Nov 2026</sub>

**Evaluation harness for multimodal models across image, video and audio benchmarks.**

lmms-eval is a Python evaluation harness that runs 100+ benchmarks (MMMU, MME, MMBench, VideoMME and others) against multimodal models over image, video and audio inputs. It supports 30+ model families plus vLLM, SGLang, Ollama and OpenAI-compatible endpoints, and reports confidence intervals and paired comparisons. It also ships a FastAPI-style HTTP eval server with job queue and an optional Web UI.

- **+** 100+ tasks across image, video and audio, with YAML task definitions for custom datasets
- **+** Runs models via vLLM, SGLang, Ollama, OpenAI-compatible APIs or native wrappers
- **+** Reports confidence intervals, clustered standard errors and paired t-tests, not just accuracy
- **+** HTTP eval server with job queue lets training loops submit checkpoint evaluations asynchronously
- **−** Eval server has no authentication; README says trusted networks only
- **−** Caption tasks (coco, refcoco, nocaps) need Java 1.8 installed
- **−** Web UI requires Node.js 18+ and builds the frontend on first run
- **−** License detected as NOASSERTION, so terms need manual checking

<sub>GPU optional · Needs uv, Python, Node.js 18+ (Web UI), Java 1.8 (caption tasks), Hugging Face datasets, OpenAI API key (some tasks) · Models: Qwen2.5-VL, Qwen3-VL, Qwen3.5, LLaVA-OneVision, InternVL-2 · port 8000 · [Repo](https://github.com/evolvinglmms-lab/lmms-eval) · [📖 Docs ↗](https://github.com/EvolvingLMMs-Lab/lmms-eval/blob/main/docs/README.md) · [🌐 Site ↗](https://www.lmms-lab.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lmms-eval/)</sub>

<a name="models"></a>
### #&#8288;84 [tensorflow/models](https://github.com/tensorflow/models) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: widely used (98) · Freshness: active (91) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · custom license · Nov 2026</sub>

**Reference TensorFlow 2 model implementations, plus the Orbit training-loop library.**

Repository of TensorFlow model implementations split into official (maintained by the TensorFlow team), research (maintained by researchers, TF1 or TF2) and a curated community list. It also includes Orbit, a lightweight library for custom TF2 training loops that works with tf.distribute on CPU, GPU and TPU. Installable as tf-models-official or the nightly tf-models-nightly package.

- **+** Official directory is maintained by the TensorFlow team against current TF2 APIs
- **+** Orbit supports custom training loops with tf.distribute on CPU, GPU and TPU
- **+** Published on PyPI as tf-models-official, with a daily nightly build
- **+** Training logs on TensorBoard.dev provided for some models
- **−** Research directory is researcher-maintained and mixes TensorFlow 1 and 2 code
- **−** tf-models-official may lag master; nightly package needed for latest changes
- **−** Source install needs manual PYTHONPATH setup and extra requirements
- **−** GitHub reports license as NOASSERTION, although the README states Apache 2.0

<sub>GPU optional · Needs TensorFlow 2, tensorflow-text-nightly (NLP packages) · Models: TensorFlow, TensorFlow 1 (research) · [Repo](https://github.com/tensorflow/models) · [📖 Docs ↗](https://www.tensorflow.org/tfmodels) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/models/)</sub>

<a name="xformers"></a>
### #&#8288;85 [xformers](https://github.com/facebookresearch/xformers) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Nov 2026</sub>

**PyTorch library of memory-efficient attention and fused transformer kernels.**

xFormers is a PyTorch library of transformer building blocks for research, including exact memory-efficient attention (xformers.ops.memory_efficient_attention), sparse and block-sparse attention, and fused softmax, linear, layer norm, dropout and SwiGLU ops. It ships its own CUDA kernels and dispatches to other libraries such as Flash-Attention where relevant. Wheels are published for CUDA 12.6, 12.8 and 13.0, with an experimental ROCm 7.1 build on Linux.

- **+** Exact (not approximate) memory-efficient attention via a single function call
- **+** Fused ops include softmax, layer norm, dropout(activation(x+bias)) and SwiGLU
- **+** Prebuilt pip wheels for CUDA 12.6, 12.8 and 13.0 on Linux and Windows
- **+** Includes python -m xformers.info to list which kernels are built
- **−** Tied to a specific PyTorch version (2.10.0 for the current stable wheels)
- **−** Source builds can take dozens of minutes and may run out of memory
- **−** ROCm support is marked experimental and Linux only
- **−** License is BSD-style but detected as NOASSERTION; includes code from triton-lang/kernels

<sub>GPU required · Needs PyTorch 2.10.0, CUDA 12.6/12.8/13.0 or ROCm 7.1, ninja (source builds) · Models: PyTorch transformer models · [Repo](https://github.com/facebookresearch/xformers) · [📖 Docs ↗](https://facebookresearch.github.io/xformers/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xformers/)</sub>

<a name="opencompass"></a>
### #&#8288;86 [opencompass](https://github.com/open-compass/opencompass) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Nov 2026</sub>

**Evaluation harness for benchmarking LLMs and VLMs on 100+ datasets.**

OpenCompass runs benchmark evaluations for language models across knowledge, reasoning, coding, science, long-context and safety datasets. It covers dataset and model configuration, inference, scoring and result summaries, using HuggingFace, LMDeploy or vLLM backends and API models from OpenAI, Anthropic, Gemini and others. Scoring can be rule-based or LLM-as-judge, and VLMEvalKit is integrated for vision-language sets.

- **+** Over 100 datasets plus VLMEvalKit integration in one config-driven workflow
- **+** Supports HuggingFace, LMDeploy and vLLM backends and hosted API models
- **+** Task partitioning, concurrent and distributed execution for large evaluation runs
- **+** LLM-as-judge, math verification and cascaded evaluators for custom scoring
- **−** Inference backends have conflicting dependencies; separate virtual environments recommended
- **−** Pyext-based code datasets (APPS, TACO, LiveCodeBench) need Python 3.10, not 3.12
- **−** No Docker or compose files provided in the repository
- **−** README documents no web UI; evaluations are configured and run from Python files

<sub>GPU optional · Needs conda, HuggingFace, LMDeploy, vLLM · Models: HuggingFace, LMDeploy, vLLM, OpenAI, Anthropic · [Repo](https://github.com/open-compass/opencompass) · [📖 Docs ↗](https://opencompass.readthedocs.io/en/latest/) · [🌐 Site ↗](https://opencompass.org.cn/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opencompass/)</sub>

<a name="lightgbm"></a>
### #&#8288;87 [lightgbm](https://github.com/lightgbm-org/lightgbm) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

**Gradient boosting library for tree-based models on tabular data.**

LightGBM is a gradient boosting framework using tree-based learning, written in C++ with Python, R and command-line interfaces, plus a SWIG wrapper. It supports parallel, distributed and GPU training and targets large tabular datasets. The project moved from Microsoft/LightGBM to lightgbm-org in March 2026.

- **+** Parallel, distributed and GPU training are supported, with a guide for each
- **+** Official packages on PyPI, conda-forge, CRAN and NuGet, plus a CLI
- **+** Many listed integrations: Spark, Ray, Kubernetes, ONNX, PMML, AutoML tuners
- **+** MIT license with exhaustive parameter and feature documentation
- **−** Covers gradient boosted trees only, not neural networks or general tensor work
- **−** Most integrations and extra language bindings are unofficial, not team-maintained
- **−** README gives no RAM or GPU sizing, so hardware needs are unknown
- **−** Org move in March 2026 means older links may point to the old location

<sub>GPU optional · Docker · Models: gradient boosting decision trees · [Repo](https://github.com/lightgbm-org/lightgbm) · [📖 Docs ↗](https://lightgbm.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lightgbm/)</sub>

<a name="lm-evaluation-harness"></a>
### #&#8288;88 [lm-evaluation-harness](https://github.com/eleutherai/lm-evaluation-harness) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Sep 2026</sub>

**Benchmark harness that runs 60+ academic LLM evals across many model backends.**

Command-line and Python framework that runs generative language models through over 60 standard academic benchmarks, with hundreds of subtasks and variants. It loads models via Hugging Face transformers, vLLM, SGLang, NeMo, GPT-NeoX, llama.cpp servers and commercial APIs. Tasks and prompts are defined in YAML with Jinja2 templates, so results stay comparable across papers.

- **+** Over 60 benchmarks with hundreds of subtasks, using public prompts for reproducible comparisons
- **+** Backends include HF transformers, vLLM, SGLang, NeMo, llama.cpp server and OpenAI-style APIs
- **+** YAML task configs with Jinja2 prompts; plugins register backends, filters and metrics without forking
- **+** Multi-GPU via accelerate data parallelism, model sharding or native PyTorch tensor parallelism
- **−** No native multi-node evaluation for the hf backend; needs an external server or custom integration
- **−** Base install has no model backend; extras like hf, vllm and api must be added
- **−** llama.cpp gguf backend does not implement loglikelihood_rolling, so perplexity tasks like wikitext fail
- **−** GGUF via hf can hang for hours on tokenizer reconstruction unless a tokenizer path is given

<sub>GPU optional · Needs transformers, vLLM, SGLang, accelerate, PyTorch · Models: Hugging Face transformers, GGUF, vLLM, SGLang, NVIDIA NeMo · [Repo](https://github.com/eleutherai/lm-evaluation-harness) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lm-evaluation-harness/)</sub>

<a name="skorch"></a>
### #&#8288;89 [skorch](https://github.com/skorch-dev/skorch) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (59) · Freshness: active (99) · Maintenance: fair (55) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · BSD-3-Clause · Nov 2026</sub>

**scikit-learn compatible wrapper for training PyTorch models.**

skorch wraps PyTorch modules in estimators such as NeuralNetClassifier, so they expose fit, predict_proba and set_params and work inside sklearn Pipeline and GridSearchCV. It adds callbacks for LR scheduling, early stopping, checkpointing, parameter freezing and sklearn scoring, plus integrations with GPyTorch and Hugging Face.

- **+** Drop-in sklearn API: Pipeline and GridSearchCV work with PyTorch modules
- **+** Callbacks for early stopping, checkpointing, LR schedulers and sklearn scoring
- **+** Documented integrations with GPyTorch and Hugging Face
- **+** Officially supports the last four minor PyTorch versions
- **−** PyTorch is not a declared dependency; users must install a matching version
- **−** Requires Python 3.9 or higher
- **−** Conda package is maintained by conda-forge, not the skorch maintainers
- **−** PyTorch only; no other tensor backends

<sub>GPU optional · Docker · Needs PyTorch, scikit-learn · Models: PyTorch nn.Module, Hugging Face, GPyTorch · [Repo](https://github.com/skorch-dev/skorch) · [📖 Docs ↗](https://skorch.readthedocs.io/en/latest/?badge=latest) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skorch/)</sub>

<a name="flash-linear-attention"></a>
### #&#8288;90 [flash-linear-attention](https://github.com/fla-org/flash-linear-attention) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · MIT · Nov 2026</sub>

**Triton kernels and PyTorch layers for linear attention and hybrid sequence models.**

Library of Triton kernels, `fla.layers` token-mixing modules and model implementations for linear attention, sparse attention, state space models and hybrids. It covers RetNet, GLA, DeltaNet, Gated DeltaNet, KDA, RWKV7, Mamba2/3, NSA and MoBA, and the layers can replace standard multihead attention. The README states the implementations are verified on NVIDIA, AMD and Intel hardware.

- **+** Covers about 40 architectures, from RetNet and GLA to Mamba3, KDA and Gated DeltaNet
- **+** Layers can replace standard attention in an existing model, with hybrid model support
- **+** Backend extras for CUDA, ROCm, XPU, NPU and CPU installs
- **+** Variable-length kernels, fused linear cross-entropy, context parallel for KDA and GDN
- **−** Bare pip install does not pull torch or triton; a backend extra is required
- **−** Full training loop lives in a separate repo (flame), not here
- **−** Input layout changed from head-first to seq-first in 2024, which can break older code

<sub>GPU optional · Needs PyTorch, Triton · Models: RetNet, GLA, DeltaNet, Gated DeltaNet, KDA · [Repo](https://github.com/fla-org/flash-linear-attention) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flash-linear-attention/)</sub>

<a name="sdv"></a>
### #&#8288;91 [sdv](https://github.com/sdv-dev/sdv) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · custom license · Nov 2026</sub>

**Python library that generates synthetic tabular data from real datasets.**

SDV is a Python library that fits models such as GaussianCopula and CTGAN to real tabular data, then samples synthetic rows for single tables, multiple connected tables or sequential data. It includes quality reports and column plots to compare real and synthetic data, plus controls for preprocessing, anonymization and logical constraints. Installed with pip or conda; the code is under the Business Source License.

- **+** Supports single-table, multi-table and sequential data, preserving primary and foreign key relationships
- **+** Built-in quality report scores column shapes and column pair trends from 0 to 100%
- **+** Offers classical (GaussianCopula) and deep learning (CTGAN) synthesizers behind one API
- **+** Anonymization and business-rule constraints are configurable during preprocessing
- **−** Business Source License, not an OSI-approved open-source license
- **−** Tabular data only; no text, image or other modalities mentioned
- **−** Several related libraries are split out of the main package, adding ecosystem complexity

<sub>Models: GaussianCopula, CTGAN · [Repo](https://github.com/sdv-dev/sdv) · [▶️ Demo ↗](https://docs.sdv.dev/sdv/demos) · [📖 Docs ↗](https://bit.ly/sdv-docs) · [🌐 Site ↗](https://sdv.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sdv/)</sub>

<a name="lazypredict"></a>
### #&#8288;92 [lazypredict](https://github.com/shankarpandala/lazypredict) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Oct 2026</sub>

**Python library that benchmarks dozens of scikit-learn-style models in one call.**

Lazy Predict fits 40+ scikit-learn-compatible models on a dataset with default parameters and returns a metrics table, so you can see which model families suit the data before tuning. It provides LazyClassifier, LazyRegressor and LazyForecaster, the last covering 20+ time series models from ETS and ARIMA to LSTM/GRU and TimesFM. Options include categorical encoders, per-model timeouts, cross-validation, MLflow tracking and optional GPU use.

- **+** One fit() call returns a metrics table across classifiers, regressors or forecasters
- **+** Per-model timeout and cv options; slow models are logged as errors instead of blocking
- **+** Optional GPU path for XGBoost, LightGBM, CatBoost, cuML, LSTM/GRU and TimesFM, with CPU fallback
- **+** Installable from PyPI or conda-forge, with extras for boosting, time series and deep learning
- **−** Runs models with default parameters only, so rankings are a rough screen, not tuned results
- **−** Timeout interruption works on Linux and macOS only, per the README
- **−** Time series and boosting models need optional extras such as statsmodels, pmdarima or PyTorch
- **−** Covers tabular and time series data only; no text or image models

<sub>GPU optional · Needs scikit-learn, xgboost (optional), lightgbm (optional), catboost (optional), statsmodels (optional), pmdarima (optional), PyTorch (optional), MLflow (optional) · Models: scikit-learn classifiers and regressors, XGBoost, LightGBM, CatBoost, ARIMA/ETS · [Repo](https://github.com/shankarpandala/lazypredict) · [📖 Docs ↗](https://shankarpandala.github.io/lazypredict/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lazypredict/)</sub>

<a name="qlib"></a>
### #&#8288;93 [qlib](https://github.com/microsoft/qlib) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · MIT · Oct 2026</sub>

**Python platform for ML-based quantitative investment research and backtesting.**

Qlib is a Python library covering the quant research pipeline: data handling, model training, backtesting, portfolio optimization and order execution. It ships a zoo of paper-implemented forecasting models (LightGBM, TCN, Transformer, TabNet, HIST, TRA and others), plus meta-learning and reinforcement learning frameworks. Workflows run from YAML configs via qrun or are built in code.

- **+** Covers data, modeling, backtesting, portfolio optimization and execution in one codebase
- **+** Includes many published quant models, with example configs run through qrun
- **+** Components are loosely coupled and can be used stand-alone
- **+** Supports supervised, market-adaptation (DDG-DA) and reinforcement learning workflows
- **−** Official dataset is disabled for now; README points to a community data source
- **−** Bundled data comes from Yahoo Finance and the README says it may be imperfect
- **−** Unreleased main-branch change restricts recorder loads and needs trusted=True opt-in
- **−** Examples target China A-share data; other markets need your own data

<sub>Docker · Needs Python 3.8-3.12, Yahoo Finance or community market data · Models: LightGBM, TCN, Transformer, TabNet, HIST · [Repo](https://github.com/microsoft/qlib) · [▶️ Demo ↗](https://terminalizer.com/view/3f24561a4470) · [📖 Docs ↗](https://qlib.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qlib/)</sub>

<a name="candle"></a>
### #&#8288;94 [candle](https://github.com/huggingface/candle) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Nov 2026</sub>

**Minimalist Rust ML framework with PyTorch-like tensors and CPU, CUDA and WASM backends.**

Candle is a Rust tensor and neural-network library from Hugging Face, with an API modeled on PyTorch. It runs on an optimized CPU backend (optional MKL or Accelerate), CUDA with NCCL multi-GPU, and WASM in the browser. The repo includes example implementations of LLaMA, Mistral, Mixtral, Gemma, Phi, Whisper, Stable Diffusion, YOLO and others, and it loads safetensors, npz, ggml and PyTorch files.

- **+** Builds into small Rust binaries without Python, aimed at serverless inference
- **+** Many model examples: LLaMA 1-3, Mistral, Mixtral, Gemma, Phi, Whisper, Stable Diffusion, YOLO
- **+** Loads safetensors, npz, ggml and PyTorch files; supports llama.cpp quantized types
- **+** WASM backend runs models in the browser, with hosted demos for Whisper, LLaMA2, T5 and SAM
- **−** Library, not a server; OpenAI-compatible APIs come from external projects like candle-vllm
- **−** Requires writing Rust; no Python bindings or ready-made UI
- **−** Model list in the README is mostly 2023-2024 era architectures
- **−** MKL and Accelerate builds can hit linker errors that need manual crate imports

<sub>GPU optional · Needs Rust toolchain, CUDA (optional), cuDNN (optional), Intel MKL (optional), trunk (WASM examples) · Models: safetensors, npz, ggml, PyTorch, llama.cpp quantized types · [Repo](https://github.com/huggingface/candle) · [▶️ Demo ↗](https://huggingface.co/spaces/lmz/candle-whisper) · [📖 Docs ↗](https://huggingface.github.io/candle/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/candle/)</sub>

<a name="flaml"></a>
### #&#8288;95 [flaml](https://github.com/microsoft/flaml) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · MIT · Nov 2026</sub>

**Python AutoML and hyperparameter tuning library with a scikit-learn style API.**

FLAML is a Python library that searches for models and hyperparameters under a compute or time budget. AutoML().fit() handles classification and regression with learners such as LightGBM, XGBoost and Random Forest, and flaml.tune runs generic tuning of any user-defined function. It also offers zero-shot wrappers that set LightGBM and XGBoost hyperparameters from the training data.

- **+** Three-line scikit-learn style AutoML fit with time budget control
- **+** Generic tune.run for arbitrary functions, with cost-aware search and early stopping
- **+** Zero-shot LGBMRegressor drop-in picks hyperparameters from the data
- **+** Installs via pip with minimal core dependencies; extras are optional
- **−** The autogen module was removed; agent use now requires the separate AutoGen repo
- **−** Requires Python >= 3.10 and < 3.14; other versions not guaranteed
- **−** Focused on tabular AutoML and tuning; not for LLM chat or serving
- **−** Some notebook examples need specific extras installed

<sub>GPU optional · Docker · Needs Python >= 3.10, < 3.14, MLflow (optional) · Models: LightGBM, XGBoost, Random Forest, custom learners · [Repo](https://github.com/microsoft/flaml) · [📖 Docs ↗](https://microsoft.github.io/FLAML/docs/Installation) · [🌐 Site ↗](https://microsoft.github.io/FLAML/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flaml/)</sub>

<a name="pysr"></a>
### #&#8288;96 [pysr](https://github.com/astroautomata/pysr) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Nov 2026</sub>

**Symbolic regression library that finds equations from data.**

PySR searches for interpretable symbolic expressions that fit a dataset, using an evolutionary search implemented in the Julia library SymbolicRegression.jl. It exposes a scikit-learn-style PySRRegressor in Python, with custom operators and losses written in Julia syntax. Fitted equations can be exported to SymPy, JAX or PyTorch, and runs can be distributed over a cluster such as Slurm.

- **+** scikit-learn-style fit/predict API with a table of equations by complexity and loss
- **+** Exports equations to SymPy, callable functions, and differentiable JAX and PyTorch
- **+** Custom operators, losses, constraints and per-operator complexity are configurable
- **+** Multithreaded Julia search backend, with cluster support such as Slurm
- **−** Julia dependencies install on first import, which slows initial setup
- **−** Suited to low-dimensional data; high dimensions need symbolic distillation of a neural net
- **−** Possible GLIBCXX import crash needs an LD_LIBRARY_PATH workaround
- **−** Warm-start state breaks if operators or search settings change between fits

<sub>no GPU · Docker · Needs Julia, SymbolicRegression.jl, SymPy, pandas · Models: symbolic regression, scikit-learn-style estimator, JAX export, PyTorch export · [Repo](https://github.com/astroautomata/pysr) · [▶️ Demo ↗](https://colab.research.google.com/github/astroautomata/PySR/blob/master/examples/pysr_demo.ipynb) · [📖 Docs ↗](https://pysr.ai/) · [🌐 Site ↗](https://pysr.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pysr/)</sub>

<a name="nixtla"></a>
### #&#8288;97 [nixtla](https://github.com/nixtla/nixtla) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · custom license · Nov 2026</sub>

**Python client SDK for the hosted TimeGPT time series forecasting API.**

Nixtla is the Python SDK (NixtlaClient) for TimeGPT, a closed-source transformer foundation model for time series. It sends data to the hosted model for zero-shot forecasting, anomaly detection, fine-tuning, cross-validation and prediction intervals, with exogenous variables and multi-series support. The model does not run locally, so an API key is required.

- **+** Forecast or detect anomalies in a few lines using pandas DataFrames
- **+** Zero-shot inference, plus fine-tuning, cross-validation and prediction intervals
- **+** Handles exogenous variables, multiple series and irregular timestamps
- **+** Docs cover Spark, Dask and Ray scaling; Snowflake install script included
- **−** Model is closed source; the repo holds only the client SDK
- **−** Every call needs an API key; access starts with a free trial
- **−** detect_anomalies() is removed in 1.0 with no drop-in replacement

<sub>no GPU · Needs Nixtla TimeGPT API key, pandas · Models: TimeGPT · [Repo](https://github.com/nixtla/nixtla) · [📖 Docs ↗](https://docs.nixtla.io) · [🌐 Site ↗](https://nixtla.io/free-trial) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nixtla/)</sub>

<a name="mljar-supervised"></a>
### #&#8288;98 [mljar-supervised](https://github.com/mljar/mljar-supervised) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Nov 2026</sub>

**Python AutoML for tabular data with automatic reports and explanations.**

mljar-supervised is a Python AutoML package that trains and compares models on tabular data, including Linear, Random Forest, XGBoost, LightGBM and CatBoost. Optional extras add RealMLP, TabM mini, and the Kumo and TabICLv2 foundation models. It writes a leaderboard and per-model reports with feature importance and SHAP, and can export a trained model as a Mercury web app.

- **+** Four modes (Explain, Perform, Compete, Optuna) set defaults for search depth and budget
- **+** Generates HTML leaderboard and model reports with SHAP, learning curves and confusion matrices
- **+** Includes golden features, feature discovery, fairness-aware training and custom metrics or folds
- **+** Compares classic, neural and tabular foundation models in one leaderboard
- **−** README install commands pin a 1.4.0 release candidate (rc6), not a stable release
- **−** Tabular data only; no text or image modeling described
- **−** Neural and foundation models need extras, a matching PyTorch build and first-use weight downloads
- **−** Feature discovery does not support custom, grouped or time-ordered validation

<sub>GPU optional · Needs Python 3.11+, PyTorch (optional extras), Mercury (optional apps extra) · Models: Linear, Decision Tree, Random Forest, XGBoost, LightGBM · [Repo](https://github.com/mljar/mljar-supervised) · [📖 Docs ↗](https://supervised.mljar.com/api/) · [🌐 Site ↗](https://supervised.mljar.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mljar-supervised/)</sub>

<a name="pytorch-geometric"></a>
### #&#8288;99 [pytorch_geometric](https://github.com/pyg-team/pytorch_geometric) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Nov 2026</sub>

**Graph neural network library built on PyTorch.**

PyG (PyTorch Geometric) is a Python library for writing and training graph neural networks on PyTorch. It provides a MessagePassing interface for custom layers, a large set of published GNN layers and models, mini-batch loaders and samplers for many small graphs or one large graph, and benchmark datasets. It also covers heterogeneous graphs, 3D meshes and point clouds, multi-GPU training and torch.compile.

- **+** Unified MessagePassing API keeps custom GNN layers short, as the EdgeConv example shows
- **+** Large catalog of published GNN layers, each linked to its paper and often an example script
- **+** Covers heterogeneous graphs, dynamic graphs, and sampling for graphs with millions of nodes
- **+** Supports torch.compile, TorchScript, multi-GPU examples and optional pyg-lib sparse kernels
- **−** Requires PyTorch; install steps and version matching are not in the visible README
- **−** Focused on graph learning only, not a general ML or LLM toolkit
- **−** Some acceleration comes from separate packages such as pyg-lib

<sub>GPU optional · Docker · Needs PyTorch, pyg-lib (optional) · Models: GCN, GAT, GraphSAGE, GIN, RGCN · [Repo](https://github.com/pyg-team/pytorch_geometric) · [📖 Docs ↗](https://pytorch-geometric.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-geometric/)</sub>

<a name="finrl"></a>
### #&#8288;100 [finrl](https://github.com/ai4finance-foundation/finrl) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: widely used (84) · Freshness: active (94) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Nov 2026</sub>

**Deep reinforcement learning pipeline for stock and crypto trading research.**

FinRL is a Python library for training deep reinforcement learning agents on financial market environments, organized into market environments, DRL agents and applications. It wraps Stable Baselines3, ElegantRL and RLlib agents (A2C, DDPG, PPO, TD3, SAC) behind a train-test-trade pipeline with many data source processors. This repository is the original educational and research version; the maintainers point production use to FinRL-X / FinRL-Trading.

- **+** Example scripts cover data download, training five DRL agents and backtesting against MVO and DJIA
- **+** Data processors for Yahoo Finance, Alpaca, Binance, CCXT, WRDS, Tushare and others
- **+** Supports Stable Baselines3, ElegantRL and RLlib agent backends
- **+** Backed by several published papers and a Dow 30 tutorial
- **−** README steers new users to FinRL-X; this repo is for education and research
- **−** Live trading support is basic, limited to Alpaca
- **−** Risk management is limited to Gym environment constraints
- **−** README badge lists Python 3.6; supported versions are unclear

<sub>Docker · Needs Yahoo Finance, Alpaca, Stable Baselines3 · Models: A2C, DDPG, PPO, TD3, SAC · [Repo](https://github.com/ai4finance-foundation/finrl) · [📖 Docs ↗](https://finrl.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/finrl/)</sub>

<a name="bayesianoptimization"></a>
### #&#8288;101 [bayesianoptimization](https://github.com/bayesian-optimization/bayesianoptimization) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · MIT · Oct 2026</sub>

**Gaussian-process Bayesian optimization of black-box functions in pure Python.**

A Python library that maximizes an unknown function within bounded parameters, using a Gaussian process and an acquisition strategy such as UCB or EI to choose each next point. You pass a function and a pbounds dict, then call maximize with init_points and n_iter. It suits expensive evaluations such as hyperparameter tuning, and the README cites support for constrained optimization and non-float parameters.

- **+** Minimal API: a function plus parameter bounds, then maximize()
- **+** Pure Python, installs from PyPI or conda-forge
- **+** Supports inequality constraints and domain reduction via SequentialDomainTransformer
- **+** Works on any function returning a real number, not tied to ML
- **−** Bounds are required for every parameter
- **−** Only maximizes; minimizing means negating the target
- **−** Non-float parameter support is described only through a citation in the README
- **−** README example is a toy function; no benchmarks or scaling limits given

<sub>no GPU · [Repo](https://github.com/bayesian-optimization/bayesianoptimization) · [📖 Docs ↗](https://bayesian-optimization.github.io/BayesianOptimization/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bayesianoptimization/)</sub>

<a name="causalml"></a>
### #&#8288;102 [causalml](https://github.com/uber/causalml) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · custom license · Nov 2026</sub>

**Python library for uplift modeling and causal inference with ML estimators.**

Causal ML is a Python package that estimates the Conditional Average Treatment Effect (CATE) of an intervention on an outcome, from experimental or observational data, through a common estimator interface. It implements uplift trees, meta-learners, doubly robust and neural-network methods from the cited literature. It also ships loaders for the LaLonde, IHDP and Twins benchmarks, with PEHE, ATE error and policy risk metrics.

- **+** Common interface across uplift trees, meta-learners, doubly robust and neural CATE estimators
- **+** Benchmark loaders (LaLonde, IHDP, Twins) with SHA256-verified downloads and ground-truth metrics
- **+** Docs include an estimator decision guide, tutorial, quickstart and example notebooks
- **+** Published on PyPI with an API reference and changelog
- **−** README warns some experimental code has APIs subject to change
- **−** Tabular causal estimation only; no LLM or generative model features
- **−** Install steps are not in the README, only linked to the docs
- **−** GitHub detects license as NOASSERTION, though README states Apache 2.0

<sub>Models: uplift trees, meta-learners, doubly robust estimators, neural network CATE estimators · [Repo](https://github.com/uber/causalml) · [📖 Docs ↗](https://causalml.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/causalml/)</sub>

<a name="deeplabcut"></a>
### #&#8288;103 [deeplabcut](https://github.com/deeplabcut/deeplabcut) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · LGPL-3.0 · Nov 2026</sub>

**Markerless animal pose estimation toolbox with GUI and Python API.**

DeepLabCut trains and runs pose estimation models that track user-labeled body parts of animals or objects in video. It offers a GUI and Python API, a PyTorch engine (v3.0+) with ResNet, HRNet and RTMPose backbones, and a legacy TensorFlow engine slated for deprecation in 3.2. It also ships SuperAnimal-Quadruped and SuperAnimal-TopViewMouse pretrained models, which are research-use only.

- **+** Works on any animal or object you can label; multi-animal and 3D pose supported
- **+** Pretrained SuperAnimal models with published mAP tables on held-out datasets
- **+** Both GUI and Python API; pip install with optional [gui] and [tf] extras
- **+** Colab demo notebook and Nature Protocols workflow guide
- **−** SuperAnimal models are non-commercial, research use only
- **−** TensorFlow backend is planned for deprecation in version 3.2
- **−** Requires Python 3.10+ and a manual PyTorch/CUDA install for GPU
- **−** Needs manual frame labeling to train on new subjects

<sub>GPU optional · Docker · Needs PyTorch, TensorFlow (optional legacy engine) · Models: ResNet, HRNet, RTMPose, DLCRNet, MobileNetV2 · [Repo](https://github.com/deeplabcut/deeplabcut) · [▶️ Demo ↗](https://colab.research.google.com/github/DeepLabCut/DeepLabCut/blob/master/examples/COLAB/COLAB_DEMO_mouse_openfield.ipynb) · [📖 Docs ↗](https://deeplabcut.github.io/DeepLabCut/README.html) · [🌐 Site ↗](https://www.deeplabcut.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deeplabcut/)</sub>

<a name="cuml"></a>
### #&#8288;104 [cuml](https://github.com/nvidia/cuml) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · Apache-2.0 · Nov 2026</sub>

**GPU-accelerated scikit-learn-style machine learning library.**

cuML provides GPU-native estimators with scikit-learn-style fit/predict/transform APIs, covering clustering, dimensionality reduction, regression, classification, preprocessing and nearest neighbors. Its cuml.accel module runs existing scikit-learn, UMAP and HDBSCAN scripts on the GPU without code changes, falling back to CPU for unsupported estimators. cuml.dask adds multi-GPU and multi-node execution for selected algorithms.

- **+** cuml.accel runs unmodified scikit-learn, UMAP and HDBSCAN code via `python -m cuml.accel`
- **+** Falls back to the CPU implementation when an estimator cannot be accelerated
- **+** cuml.dask gives multi-GPU and multi-node execution for selected algorithms
- **+** Logging and profiling tools show which operations ran on the GPU
- **−** Targets NVIDIA GPUs only; no AMD or other accelerator support mentioned
- **−** Speedups vary by algorithm and dataset; the 50x figure is an upper bound
- **−** Distributed support covers only selected algorithms, not the full API
- **−** Models are saved with pickle or joblib, which is unsafe for untrusted files

<sub>GPU required · Needs CUDA, scikit-learn >=1.6, Dask (for multi-GPU) · Models: scikit-learn-style estimators, UMAP, HDBSCAN · [Repo](https://github.com/nvidia/cuml) · [📖 Docs ↗](https://docs.nvidia.com/cuml/) · [🌐 Site ↗](https://developer.nvidia.com/topics/ai/data-science/cuda-x-data-science-libraries/cuml) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cuml/)</sub>

<a name="neuralforecast"></a>
### #&#8288;105 [neuralforecast](https://github.com/nixtla/neuralforecast) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Nov 2026</sub>

**Python library of 30+ neural time-series forecasting models with sklearn-style API.**

NeuralForecast is a Python library that implements neural forecasting models, from MLP, LSTM and TCN to NHITS, NBEATSx, TFT, PatchTST and iTransformer, behind a fit/predict interface. It supports exogenous variables, static covariates, probabilistic forecasts and hyperparameter tuning through Ray or Optuna. It shares input and output formats with StatsForecast, MLForecast and HierarchicalForecast.

- **+** Over 30 forecasting models behind one fit/predict API
- **+** Official NHITS and NBEATSx implementations from the papers' authors
- **+** Auto models tune hyperparameters with Ray or Optuna
- **+** Since 3.3.0, saves safetensors plus JSON, so loading runs no code
- **−** Models saved before 3.3.0 need allow_pickle=True or a migration step
- **−** TimeLLM cannot be saved or loaded; train and predict in one process
- **−** Custom losses, optimizers and schedulers must be registered before save and load
- **−** Time-series forecasting only; no general LLM or chat features

<sub>Needs Ray, Optuna, utilsforecast, coreforecast · Models: NBEATS, NBEATSx, NHITS, TFT, PatchTST · [Repo](https://github.com/nixtla/neuralforecast) · [📖 Docs ↗](https://nixtlaverse.nixtla.io/neuralforecast/docs/getting-started/introduction.html) · [🌐 Site ↗](https://nixtlaverse.nixtla.io/neuralforecast/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/neuralforecast/)</sub>

<a name="spark-nlp"></a>
### #&#8288;106 [spark-nlp](https://github.com/johnsnowlabs/spark-nlp) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · Apache-2.0 · Nov 2026</sub>

**Distributed NLP library running pretrained transformer pipelines on Apache Spark.**

Spark NLP is an NLP library built natively on Apache Spark. It provides annotators for tokenization, NER, classification, embeddings, translation, question answering and speech recognition, usable from Python, Scala, Java and R. It ships pretrained pipelines and models and can import models from TensorFlow, ONNX, OpenVINO and llama.cpp GGUF. Version 7.0.0 supports Spark 3.x on Scala 2.12 and Spark 4 on Scala 2.13.

- **+** Runs NLP pipelines natively inside Spark, so jobs scale across a cluster
- **+** Imports models from TensorFlow, ONNX, OpenVINO and llama.cpp GGUF
- **+** Documented setup for Databricks, EMR, EMR Serverless and GCP Dataproc
- **+** Works fully offline once models and pipelines are downloaded
- **−** Needs Java and Spark, which is heavy for single-machine use
- **−** Separate Maven artifacts per Spark and Scala version, including a Spark 4.0.0 build
- **−** Apple Silicon and AArch64 builds are marked experimental
- **−** No HTTP API or chat interface included; it is a library

<sub>GPU optional · Needs Apache Spark, Java 8 or 11 (Spark 3.x), Java 17 (Spark 4.x) · Models: TensorFlow, ONNX, OpenVINO, GGUF (llama.cpp) · [Repo](https://github.com/johnsnowlabs/spark-nlp) · [▶️ Demo ↗](https://sparknlp.org/demos) · [📖 Docs ↗](https://sparknlp.org/docs/en/install) · [🌐 Site ↗](https://sparknlp.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/spark-nlp/)</sub>

<a name="onednn"></a>
### #&#8288;107 [onednn](https://github.com/uxlfoundation/onednn) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · Apache-2.0 · Nov 2026</sub>

**Optimized CPU and GPU deep learning primitives library used inside PyTorch and TensorFlow.**

oneDNN is a C++ library of optimized deep learning operations such as matmul, convolution, attention and normalization for x86-64, AArch64, RISC-V CPUs and Intel GPUs. It detects the ISA at runtime and JIT-generates specialized kernels, with post-op fusion and a Graph API for patterns like SDPA and GQA. The README says most practitioners should use it through a framework (PyTorch, ONNX Runtime, llama.cpp, others) rather than directly.

- **+** Runtime ISA detection with JIT kernels for Intel 64/AMD64, AArch64 and RV64 CPUs
- **+** Data types from f32 down to f4 and s4, including OCP microscaling formats
- **+** Graph API fuses larger patterns such as SDPA and GQA; post-ops fuse into matmul and convolution
- **+** Integrated in PyTorch, TensorFlow, ONNX Runtime, OpenVINO, llama.cpp and others
- **−** Low-level C/C++ API; README advises most users to go through a framework instead
- **−** NVIDIA and AMD GPU backends are experimental; PPC64 and s390x have limited validation
- **−** GPU engine is off by default and needs a vendor-specific SYCL or OpenCL toolchain
- **−** Optimized GPU targets listed are Intel only; other vendors are experimental

<sub>GPU optional · Needs CMake 3.13+, C++11 compiler, OpenMP or TBB (CPU runtime), SYCL/OpenCL/Level Zero (GPU), Arm Compute Library (optional, AArch64) · Models: f32, bf16, f16, f8, f4 · [Repo](https://github.com/uxlfoundation/onednn) · [📖 Docs ↗](https://uxlfoundation.github.io/oneDNN) · [🌐 Site ↗](https://www.uxlfoundation.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onednn/)</sub>

<a name="litert"></a>
### #&#8288;108 [litert](https://github.com/google-ai-edge/litert) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Nov 2026</sub>

**Google's on-device ML runtime, successor to TensorFlow Lite.**

LiteRT is a C++ runtime that runs .tflite models on Android, iOS, Linux, macOS, Windows, web and IoT targets. Its Compiled Model API selects accelerators automatically across CPU (XNNPACK), GPU (ML Drift) and vendor NPUs. It continues TensorFlow Lite, which is now in maintenance mode, and pairs with separate projects for PyTorch conversion, quantization and LLM inference (LiteRT-LM).

- **+** Compiled Model API picks accelerators automatically, no manual delegate setup
- **+** NPU support from several vendors: Qualcomm, MediaTek, Google Tensor, Intel, Broadcom, S.LSI
- **+** Covers Android, iOS, Linux, macOS, Windows and web (WebGPU/WASM via LiteRT.js)
- **+** Conversion path from PyTorch, TensorFlow and JAX, plus a separate quantizer
- **−** Embedded runtime library, not a server; no HTTP API for serving models
- **−** LLM inference lives in a separate repo, LiteRT-LM
- **−** Apple Neural Engine, WebNN and Raspberry Pi NPU support are marked coming soon
- **−** TensorFlow Lite Interpreter API is deprecated; existing code needs migration to V2

<sub>GPU optional · Needs Bazel or CMake (build from source), XNNPACK · Models: .tflite, .litertlm, PyTorch (via LiteRT Torch), TensorFlow, JAX · [Repo](https://github.com/google-ai-edge/litert) · [📖 Docs ↗](https://ai.google.dev/edge/litert/overview) · [🌐 Site ↗](https://ai.google.dev/edge/litert) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/litert/)</sub>

<a name="hanlp"></a>
### #&#8288;109 [hanlp](https://github.com/hankcs/hanlp) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (94) · Freshness: recent (70) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Nov 2026</sub>

**Multilingual NLP toolkit for tokenization, tagging, parsing and NER, mainly Chinese.**

HanLP is a Python NLP toolkit with pretrained PyTorch and TensorFlow 2.x models for tokenization, POS tagging, NER, dependency and constituency parsing, semantic role labeling, AMR and more. It offers a native API that loads models locally, and a RESTful client (Python, Go, Java) that calls a hosted server. Output is a uniform JSON-compatible Document. The README states support for 130 languages through joint multi-task models.

- **+** Covers many classic NLP tasks with pretrained models: tok, POS, NER, dep, con, SRL, SDP, AMR
- **+** Native and RESTful APIs share the same semantics, so code ports between them
- **+** Custom trie dictionaries with force, merge and correct rules feed into downstream models
- **+** Multi-task models save speed and memory; single-task models can be chained in a pipeline
- **−** Native API requires Python 3.6 to 3.10, which is dated
- **−** Last release is 2025-01-13; the README is Chinese-first
- **−** Native API takes sentences as input, so sentence splitting is a separate step
- **−** Hosted RESTful API gives anonymous users limited quota; an auth key is recommended

<sub>GPU optional · Needs PyTorch, TensorFlow 2.x · Models: PyTorch, TensorFlow 2.x, ELECTRA, mMiniLMv2 · [Repo](https://github.com/hankcs/hanlp) · [▶️ Demo ↗](https://mybinder.org/v2/gh/hankcs/HanLP/doc-zh?filepath=plugins%2Fhanlp_demo%2Fhanlp_demo%2Fzh%2Ftutorial.ipynb) · [📖 Docs ↗](https://hanlp.hankcs.com/docs/) · [🌐 Site ↗](https://hanlp.hankcs.com/docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hanlp/)</sub>

<a name="stable-baselines3"></a>
### #&#8288;110 [stable-baselines3](https://github.com/dlr-rm/stable-baselines3) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

**PyTorch implementations of reinforcement learning algorithms with a scikit-learn-like API.**

Stable Baselines3 provides tested PyTorch implementations of RL algorithms including PPO, A2C, DQN, DDPG, SAC, TD3 and HER, driven through a sklearn-style `learn()` and `predict()` interface. It works with Gymnasium environments, supports Dict observation spaces, custom policies and callbacks, and logs to TensorBoard. Development is limited to maintenance; newer algorithms live in SB3 Contrib and a Jax port, SBX.

- **+** Consistent sklearn-like API across algorithms; a PPO run is a one-line call
- **+** Supports Gymnasium envs, Dict observations, custom policies, callbacks and TensorBoard
- **+** Type hints, high test coverage, and benchmark results documented per algorithm
- **+** Companion RL Zoo provides training scripts and tuned hyperparameters
- **−** Assumes prior RL knowledge; README says not to use it without practice
- **−** Maintenance mode only; no major new features planned for the core
- **−** TRPO, QR-DQN, TQC, RecurrentPPO live in the separate SB3 Contrib repo
- **−** No technical support or consulting offered by maintainers

<sub>GPU optional · Docker · Needs PyTorch >= 2.8, Gymnasium, Python 3.10+ · Models: PPO, A2C, DQN, DDPG, SAC · [Repo](https://github.com/dlr-rm/stable-baselines3) · [📖 Docs ↗](https://stable-baselines3.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/stable-baselines3/)</sub>

<a name="corenlp"></a>
### #&#8288;111 [corenlp](https://github.com/stanfordnlp/corenlp) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · GPL-3.0 · Sep 2026</sub>

**Java NLP toolkit for tagging, parsing, named entities and coreference.**

Stanford CoreNLP is a Java library that takes raw text and produces lemmas, parts of speech, named entities, normalized dates and quantities, constituency and dependency parses, and coreference chains. It combines rule-based, probabilistic and deep learning components in one pipeline. English is the main language, with varying support for Arabic, Chinese, French, German, Hungarian, Italian and Spanish.

- **+** One pipeline runs tokenizing, tagging, NER, parsing and coreference from two lines of code
- **+** Published on Maven Central; builds with Ant or Maven, and Gradle dependency snippets are given
- **+** Model jars for nine languages, also hosted on Hugging Face Hub
- **+** Active: release on 2026-09-25 and long-established use in academia and industry
- **−** GPL license rules out use in proprietary software you distribute
- **−** Models ship as separate jars; the shift-reduce parser and WikiDict need extra English downloads
- **−** Non-English support is uneven; README only says 'varying levels'
- **−** README gives no memory or hardware requirements

<sub>Needs Java, Ant or Maven, CoreNLP model jars · Models: Stanford CoreNLP model jars, Arabic, Chinese, English, French · [Repo](https://github.com/stanfordnlp/corenlp) · [📖 Docs ↗](http://stanfordnlp.github.io/CoreNLP/) · [🌐 Site ↗](http://stanfordnlp.github.io/CoreNLP/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/corenlp/)</sub>

<a name="djl"></a>
### #&#8288;112 [djl](https://github.com/deepjavalibrary/djl) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · Apache-2.0 · Nov 2026</sub>

**Engine-agnostic Java framework for training and running deep learning models.**

Deep Java Library (DJL) is a Java API for deep learning that covers both inference and training. It loads pre-trained models from a model zoo through a Criteria builder, and the underlying engine can be swapped without changing application code. The README says it picks CPU or GPU automatically based on the hardware.

- **+** Native Java API that works like any regular library in an IDE and build
- **+** Engine-agnostic: switch deep learning engines without rewriting application code
- **+** Model zoo with Criteria-based loading, plus built-in training and datasets such as MNIST
- **+** Automatic CPU/GPU selection based on detected hardware
- **−** Java-centric, while most ML tooling and examples are in Python
- **−** README shows only classic deep learning examples, no LLM serving or agent features

<sub>GPU optional · Docker · Needs Java, Gradle (build from source) · [Repo](https://github.com/deepjavalibrary/djl) · [📖 Docs ↗](https://docs.djl.ai/) · [🌐 Site ↗](https://djl.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/djl/)</sub>

<a name="mteb"></a>
### #&#8288;113 [mteb](https://github.com/embeddings-benchmark/mteb) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · Apache-2.0 · Nov 2026</sub>

**Python toolkit for benchmarking embedding models on retrieval and other tasks.**

MTEB is a Python library and CLI that evaluates text and multimodal embedding models across a catalog of tasks and named benchmarks, such as MTEB(eng, v2). Models load through mteb.get_model, which falls back to SentenceTransformer for models not implemented in MTEB. It also backs the public MTEB leaderboard on Hugging Face.

- **+** Installs with pip or uv and runs from Python or the `mteb run` CLI
- **+** Named benchmarks carry citations and can export task tables as LaTeX
- **+** Feeds the public Hugging Face MTEB leaderboard, with documented steps to add models
- **+** Falls back to SentenceTransformer for models without a custom MTEB implementation
- **−** Evaluation only; it does not train, fine-tune or serve embedding models
- **−** Task and model catalogs live in external docs, not the README

<sub>Docker · Needs sentence-transformers · Models: SentenceTransformer models, custom model definitions · [Repo](https://github.com/embeddings-benchmark/mteb) · [▶️ Demo ↗](https://huggingface.co/spaces/mteb/leaderboard) · [📖 Docs ↗](https://embeddings-benchmark.github.io/mteb/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mteb/)</sub>

<a name="physicsnemo"></a>
### #&#8288;114 [physicsnemo](https://github.com/nvidia/physicsnemo) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · Apache-2.0 · Nov 2026</sub>

**PyTorch framework for training physics and scientific ML models.**

PhysicsNeMo is a PyTorch library of physics ML models, layers, datapipes and training recipes for CFD, weather, structural mechanics, geophysics and healthcare. Models are plain torch.nn.Module objects (FNO, MeshGraphNet, Transolver, GeoTransolver, DoMINO, GraphCast, diffusion U-Nets and others). ShardTensor domain parallelism splits a single high-resolution sample across GPUs, alongside DDP or FSDP2.

- **+** Models are ordinary torch.nn.Module objects, usable inside existing PyTorch code
- **+** ShardTensor domain parallelism shards one large sample across GPUs, with DDP or FSDP2
- **+** Wide model coverage: FNO, MeshGraphNet, Transolver, DoMINO, GraphCast, Pangu, FengWu, TopoDiff
- **+** Many end-to-end recipes for aerodynamics, weather, crash dynamics, geophysics and healthcare
- **−** Install extras target CUDA 12 or 13, so it is built around NVIDIA GPUs
- **−** Narrow domain focus; not meant for LLM or general deep learning work
- **−** Some models, such as AeroJEPA, are experimental and their API may change
- **−** Recipes need domain datasets; separate repos (Curator, CFD) handle data prep and inference

<sub>GPU required · Docker · Needs PyTorch, CUDA 12 or 13 · Models: FNO, MeshGraphNet, Transolver, GeoTransolver, DoMINO · [Repo](https://github.com/nvidia/physicsnemo) · [📖 Docs ↗](https://docs.nvidia.com/physicsnemo/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/physicsnemo/)</sub>

<a name="fastembed"></a>
### #&#8288;115 [fastembed](https://github.com/qdrant/fastembed) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Nov 2026</sub>

**Python library that generates text and image embeddings with ONNX Runtime.**

FastEmbed is a Python library that produces dense, sparse (SPLADE++), late-interaction (ColBERT, ColPali) and image embeddings, plus cross-encoder reranking, using ONNX Runtime instead of PyTorch. It runs on CPU by default, with a separate fastembed-gpu package for CUDA. It is maintained by Qdrant and integrates with qdrant-client, but also works standalone.

- **+** No PyTorch dependency; ONNX Runtime keeps installs small and suits serverless runtimes like AWS Lambda
- **+** Covers dense, sparse, ColBERT, ColPali, image embeddings and cross-encoder rerankers in one API
- **+** add_custom_model registers unlisted Hugging Face ONNX models for embeddings and reranking
- **+** Default model BAAI/bge-small-en-v1.5 outputs 384-dim vectors; data parallelism for large datasets
- **−** Only models with ONNX exports are supported; custom models need pooling and file settings
- **−** GPU use needs the separate fastembed-gpu package and a matching CUDA setup
- **−** Library only: no HTTP server or CLI for serving embeddings
- **−** Accuracy claim versus OpenAI Ada-002 is stated without benchmark numbers in the README

<sub>GPU optional · Needs ONNX Runtime, Hugging Face model downloads, Qdrant (optional) · Models: ONNX, BAAI/bge-small-en-v1.5, SPLADE++, ColBERT, ColPali · [Repo](https://github.com/qdrant/fastembed) · [📖 Docs ↗](https://qdrant.github.io/fastembed/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fastembed/)</sub>

<a name="category-encoders"></a>
### #&#8288;116 [category_encoders](https://github.com/scikit-learn-contrib/category_encoders) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · BSD-3-Clause · Nov 2026</sub>

**scikit-learn transformers that encode categorical columns as numeric features.**

A Python library of scikit-learn-compatible transformers that convert categorical variables to numbers. It covers unsupervised methods (one-hot, binary, BaseN, hashing, count, ordinal, contrast codings) and supervised ones (target, CatBoost, leave-one-out, James-Stein, weight of evidence, GLMM). Encoders accept numpy arrays and pandas DataFrames and work inside sklearn pipelines.

- **+** About 23 encoding methods behind one sklearn transformer API
- **+** Works with numpy arrays and pandas DataFrames, and drops into sklearn pipelines
- **+** NestedCVWrapper and PolynomialWrapper add overfitting control and polynomial target support
- **+** Each method cites a reference, and the repo includes examples and benchmarks
- **−** Supervised encoders need fit_transform on training data; fit().transform() can give different results
- **−** GLMMEncoder needs the optional statsmodels dependency via the glmm extra
- **−** Requires Python 3.11 or newer
- **−** Tabular preprocessing only; no model training or serving

<sub>no GPU · Needs numpy, pandas, scikit-learn, scipy, statsmodels (optional, for GLMMEncoder) · [Repo](https://github.com/scikit-learn-contrib/category_encoders) · [📖 Docs ↗](http://contrib.scikit-learn.org/category_encoders/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/category-encoders/)</sub>

<a name="bitsandbytes"></a>
### #&#8288;117 [bitsandbytes](https://github.com/bitsandbytes-foundation/bitsandbytes) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: patchy (37) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · MIT · Nov 2026</sub>

**8-bit and 4-bit quantization and 8-bit optimizers for PyTorch models.**

bitsandbytes is a PyTorch library that provides LLM.int8() 8-bit inference, QLoRA 4-bit quantization and block-wise 8-bit optimizers. It exposes Linear8bitLt and Linear4bit layers plus a bitsandbytes.optim module, and is documented as a quantization backend for Hugging Face Transformers, Diffusers and PEFT. Backends cover CPU, NVIDIA, AMD, Intel GPU and Gaudi, and Apple Metal.

- **+** Drop-in Linear8bitLt and Linear4bit layers plus 8-bit optimizers in bitsandbytes.optim
- **+** Documented integrations with Hugging Face Transformers, Diffusers and PEFT
- **+** Wide hardware matrix: x86-64 and aarch64 CPU, NVIDIA, AMD, Intel XPU, Windows, macOS
- **+** Backed by published papers: LLM.int8(), QLoRA and 8-bit optimizers
- **−** Library only, no model server, UI or CLI; requires writing PyTorch code
- **−** Gaudi has partial 4-bit support and no 8-bit optimizers
- **−** Metal 8-bit optimizers only planned; some CPU and Metal paths lack optimizations
- **−** Requires Python 3.10+ and PyTorch 2.4+

<sub>GPU optional · Needs PyTorch 2.4+, Python 3.10+ · Models: PyTorch models, Hugging Face Transformers, Diffusers, PEFT · [Repo](https://github.com/bitsandbytes-foundation/bitsandbytes) · [📖 Docs ↗](https://huggingface.co/docs/bitsandbytes/main) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bitsandbytes/)</sub>

<a name="h2o-3"></a>
### #&#8288;118 [h2o-3](https://github.com/h2oai/h2o-3) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Nov 2026</sub>

**Distributed in-memory machine learning platform with AutoML and R/Python clients.**

H2O-3 is a JVM-based, in-memory platform for distributed machine learning on tabular data. It implements GLM, GBM (including XGBoost), Random Forest, deep neural networks, Stacked Ensembles, K-Means, PCA, Word2Vec and an AutoML routine, driven from R, Python, Scala, Java, REST/JSON or the Flow web notebook. Models can be exported as POJO or MOJO for production scoring, and it integrates with Hadoop and Spark.

- **+** Broad classic algorithm set plus AutoML, accessed from R, Python, Scala, Java and REST
- **+** Exports models as POJO or MOJO for fast scoring in production
- **+** Runs as a cluster across nodes, with Hadoop and Sparkling Water (Spark) integration
- **+** Installs via pip or CRAN; the jar serves Flow UI on port 54321
- **−** Not an LLM or generative AI toolkit; focused on classic tabular ML
- **−** Building from source needs JDK, Node.js, Gradle, Python and R
- **−** No tagged release on the repository; stable builds come from h2o.ai/download
- **−** Full test suite needs at least 8 GB RAM, 16 GB preferred

<sub>Docker · Needs JDK 1.8+, Node.js (build), Gradle (build), R (build), Python (build) · Models: GLM, GBM, XGBoost, Random Forest, Deep Learning · port 54321 · [Repo](https://github.com/h2oai/h2o-3) · [📖 Docs ↗](http://docs.h2o.ai/h2o/latest-stable/h2o-docs/index.html) · [🌐 Site ↗](http://h2o.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/h2o-3/)</sub>

<a name="clearml"></a>
### #&#8288;119 [clearml](https://github.com/clearml/clearml) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Nov 2026</sub>

**Experiment tracking, pipelines and dataset versioning for ML jobs.**

ClearML is a Python SDK plus server for tracking ML experiments, running remote jobs through agents, and versioning datasets on object storage. Adding Task.init() to a script logs git state, packages, hyperparameters, console output, resource use and framework metrics. Pipelines, hyperparameter optimization, model serving and an orchestration dashboard are separate modules.

- **+** Two-line Task.init() captures git state, packages, parameters, console output and GPU/CPU metrics
- **+** Auto-logs PyTorch, TensorFlow, Keras, XGBoost, LightGBM, scikit-learn, Matplotlib and TensorBoard
- **+** Dataset versioning on S3, GS, Azure or NAS, with a clearml-data CLI
- **+** Agents run jobs on Kubernetes, cloud or bare metal; pipelines and hyperparameter optimization included
- **−** Full use needs a ClearML server, hosted or self-deployed
- **−** Serving, agent, session and fractional GPU modules live in separate repositories
- **−** Centered on classic ML/DL training; LLM features are only briefly described
- **−** README gives no RAM, port or server dependency details

<sub>GPU optional · Needs ClearML Server (hosted or self-hosted), clearml-agent, S3/GS/Azure/NAS (optional storage) · Models: PyTorch, TensorFlow, Keras, FastAI, XGBoost · [Repo](https://github.com/clearml/clearml) · [📖 Docs ↗](https://clear.ml/docs) · [🌐 Site ↗](https://clear.ml) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clearml/)</sub>

<a name="mujoco-menagerie"></a>
### #&#8288;120 [mujoco_menagerie](https://github.com/google-deepmind/mujoco_menagerie) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (47) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · custom license · Nov 2026</sub>

**Curated MuJoCo robot models for arms, quadrupeds, humanoids and drones.**

A Google DeepMind collection of MJCF robot models for the MuJoCo physics engine, covering Unitree, ANYmal, Franka Panda, UR5e, Cassie and others. Each model directory has meshes, an MJCF XML, a scene.xml, a license and a README on how the model was built. It installs with `pip install mujoco-menagerie` or by cloning the repo, and gallery thumbnails open in a browser viewer.

- **+** Every model follows the same layout: model XML, scene.xml, meshes, LICENSE and build README
- **+** Python package loads a model with mm.load('unitree_go2') and exposes an editable MjSpec
- **+** Some models ship MJX variants for JAX-based simulation
- **+** In-browser previews through live.mujoco.org need no install
- **−** Quality grades (A+ to C) are defined but not yet applied to models
- **−** Licenses differ per model (BSD-3-Clause, Apache-2.0, MIT), so check each LICENSE file
- **−** Not all models have an MJX variant
- **−** Only useful with MuJoCo; each model sets its own minimum MuJoCo version

<sub>Needs mujoco · Models: MJCF XML, STL meshes, OBJ meshes, MJX · [Repo](https://github.com/google-deepmind/mujoco_menagerie) · [▶️ Demo ↗](https://live.mujoco.org) · [📖 Docs ↗](https://mujoco.readthedocs.io/en/latest/models.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mujoco-menagerie/)</sub>

<a name="iree"></a>
### #&#8288;121 [iree](https://github.com/iree-org/iree) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (43) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · Apache-2.0 · Nov 2026</sub>

**MLIR-based compiler and runtime for deploying ML models from datacenter to edge.**

IREE compiles machine learning models to a unified MLIR-based IR and executes them with a runtime, targeting hardware from datacenter systems to mobile and edge devices. It is distributed as the PyPI packages iree-base-compiler and iree-base-runtime, and can be built from source. User guides and build instructions are on iree.dev.

- **+** One compiler and runtime path covering datacenter through mobile and edge targets
- **+** Installable from PyPI as iree-base-compiler and iree-base-runtime
- **+** Nightly CI on Linux arm64 and macOS arm64
- **+** AMD submitted an IREE-based SDXL implementation to MLPerf inference
- **−** Compiler toolchain, not a ready-to-use model server or chat app
- **−** Extending or debugging it requires MLIR and compiler knowledge
- **−** README lists no supported model formats or hardware backends
- **−** Source builds need a C++ toolchain; no Docker setup provided

<sub>GPU optional · [Repo](https://github.com/iree-org/iree) · [📖 Docs ↗](https://iree.dev/) · [🌐 Site ↗](https://iree.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/iree/)</sub>

<a name="geoai"></a>
### #&#8288;122 [geoai](https://github.com/opengeos/geoai) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · MIT · Nov 2026</sub>

**Python package for training and running deep learning models on satellite imagery.**

GeoAI is a Python package that covers the geospatial ML workflow: downloading imagery (Sentinel, Landsat, NAIP), building image chips and labels, training segmentation, classification and detection models, and running inference. It wraps PyTorch, Transformers and segmentation_models.pytorch, and visualizes results with Leafmap and MapLibre. A QGIS plugin exposes the workflows without code.

- **+** Covers the full pipeline: data download, chip generation, training, inference and export
- **+** Reads and writes GeoTIFF, GeoJSON, Shapefile, GeoPackage and GeoParquet
- **+** Catalog of 20 remote sensing foundation models, with TerraTorch backbone loading
- **+** QGIS plugin, book, docs and video tutorials; installs via pip or conda
- **−** Narrow domain: geospatial raster and vector data only, not a general ML library
- **−** Builds on PyTorch and other packages, so installs carry heavy dependencies
- **−** Foundation model loading is limited to TerraTorch-supported backbones

<sub>GPU optional · Docker · Needs PyTorch, Transformers, segmentation_models.pytorch, Leafmap, MapLibre, TerraTorch · Models: PyTorch, Hugging Face Transformers, segmentation_models.pytorch, torchange, TerraTorch backbones · [Repo](https://github.com/opengeos/geoai) · [📖 Docs ↗](https://opengeoai.org) · [🌐 Site ↗](https://opengeoai.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/geoai/)</sub>

<a name="aimet"></a>
### #&#8288;123 [aimet](https://github.com/qualcomm/aimet) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · custom license · Nov 2026</sub>

**Quantization and compression toolkit for PyTorch and ONNX models.**

AIMET quantizes trained PyTorch and ONNX models to lower precision (for example INT8, or INT4 weights) using post-training methods such as AdaRound, SeqMSE, Cross Layer Equalization and SpinQuant. It also supports quantization-aware training in aimet-torch, plus spatial SVD and channel pruning for compression. It is maintained by Qualcomm and targets edge deployment on phones and laptops.

- **+** Broad PTQ set: AdaRound, SeqMSE, CLE, AdaScale, SpinQuant, BatchNorm folding
- **+** Separate aimet-onnx and aimet-torch packages installable from PyPI
- **+** Also covers QAT and compression (spatial SVD, channel pruning, per-layer ratios)
- **+** README gives numbers, e.g. DeepLabv3 INT4 weights at 70.86 mIOU vs 72.94 FP32
- **−** Supports only PyTorch and ONNX models
- **−** QAT is available only through aimet-torch, not ONNX
- **−** OmniQuant is PyTorch-only, so the ONNX feature set is narrower
- **−** Speed claims cite Qualcomm Hexagon DSP and Kryo CPU, so tuned for Qualcomm targets

<sub>Needs PyTorch, ONNX · Models: PyTorch, ONNX · [Repo](https://github.com/qualcomm/aimet) · [📖 Docs ↗](https://qualcomm.github.io/aimet-pages/releases/latest/index.html) · [🌐 Site ↗](https://qualcomm.github.io/aimet-pages/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aimet/)</sub>

<a name="vit-pytorch"></a>
### #&#8288;124 [vit-pytorch](https://github.com/lucidrains/vit-pytorch) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: widely used (90) · Freshness: active (91) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Nov 2026</sub>

**PyTorch implementations of Vision Transformer and many of its variants.**

A pip-installable Python library with compact PyTorch implementations of ViT and dozens of variants, including SimpleViT, NaViT, CaiT, CrossViT, LeViT, CvT, MaxViT and MobileViT. It also includes a distillation wrapper and self-supervised modules such as MAE, Dino and masked patch prediction. Each model is a plain nn.Module with a short usage snippet.

- **+** Covers about 30 ViT variants behind similar constructor-style APIs
- **+** Includes a distillation wrapper and self-supervised options (MAE, Dino, EsViT, masked patch prediction)
- **+** Single pip package; models are plain PyTorch modules
- **+** NaViT handles mixed-resolution batches, with a nested-tensor variant for PyTorch 2.5
- **−** No pretrained weights; README points to timm for pretrained ViTs
- **−** Examples use random tensors; no training scripts or benchmarks in the README
- **−** ViT requires more than 16 patches per image
- **−** NaViT needs manual image grouping unless group_images is set

<sub>GPU optional · Needs PyTorch, torchvision · Models: ViT, SimpleViT, NaViT, CaiT, CrossViT · [Repo](https://github.com/lucidrains/vit-pytorch) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vit-pytorch/)</sub>

<a name="safetensors"></a>
### #&#8288;125 [safetensors](https://github.com/safetensors/safetensors) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · Apache-2.0 · Nov 2026</sub>

**Tensor file format and library that avoids pickle, with zero-copy lazy loading.**

Safetensors defines a simple file layout for tensors: an 8-byte little-endian header size, a JSON header with dtype, shape and offsets, then a raw byte buffer. The Rust core ships with Python bindings (pip install safetensors) that save and load tensors via safe_open and save_file, including PyTorch. Loading never executes code, the header is capped at 100MB, and tensors can be read individually without scanning the whole file.

- **+** Loading a file cannot run arbitrary code, unlike pickle-based PyTorch checkpoints
- **+** Lazy loading of single tensors; README reports BLOOM on 8 GPUs dropping from 10 min to 45 s
- **+** Native bfloat16 and fp8 dtypes, and no file size limit
- **+** Format is small and documented; Rust crate plus Python bindings on PyPI and crates.io
- **−** Stores only tensors and string metadata, no custom code or arbitrary structures
- **−** No strided tensors; everything must be packed before serialization
- **−** Sub-byte dtypes error out on unaligned reads
- **−** Not fully zero-copy: header is JSON and GPU loads still copy from disk

<sub>no GPU · Docker · Needs Rust toolchain (build from source only), setuptools_rust (build from source only) · Models: PyTorch, TensorFlow, Flax, NumPy · [Repo](https://github.com/safetensors/safetensors) · [📖 Docs ↗](https://huggingface.co/docs/safetensors/index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/safetensors/)</sub>

<a name="interpret"></a>
### #&#8288;126 [interpret](https://github.com/interpretml/interpret) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (63) · Freshness: active (94) · Maintenance: patchy (47) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · MIT · Nov 2026</sub>

**Python library for training interpretable models and explaining blackbox ML models.**

InterpretML is a Python package that trains glassbox models, mainly the Explainable Boosting Machine (a boosted GA2M-style additive model), and wraps blackbox explainers such as SHAP, LIME, Morris sensitivity and partial dependence. It produces global and local explanations and a comparison dashboard via show(), and includes differentially private EBMs. The core is C++ with a Python API for tabular data.

- **+** EBM AUROC is on par with XGBoost on the README's five benchmark datasets, with exact explanations
- **+** One API covers glassbox models plus SHAP, LIME, Morris and partial dependence explainers
- **+** Includes differentially private EBMs with epsilon and delta parameters
- **+** README reports EBMs fitting 100 million samples in several hours; distributed option on Azure SynapseML
- **−** Aimed at tabular classification and regression; no LLM or deep network interpretability in the README
- **−** EBMs use pairwise interactions by default; 3-way and higher need a custom notebook
- **−** Distributed training for larger workloads relies on Azure SynapseML
- **−** Blackbox explainers are wrappers around existing packages such as shap and lime

<sub>no GPU · Needs Python 3.10+, scikit-learn, plotly, dash · Models: Explainable Boosting Machine, APLR, Decision Tree, Decision Rule List, Linear/Logistic Regression · [Repo](https://github.com/interpretml/interpret) · [▶️ Demo ↗](https://mybinder.org/v2/gh/interpretml/interpret/main?labpath=docs%2Finterpret%2Fpython%2Fexamples%2Finterpretable-classification.ipynb) · [📖 Docs ↗](https://interpret.ml/docs) · [🌐 Site ↗](https://interpret.ml) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/interpret/)</sub>

<a name="torchgeo"></a>
### #&#8288;127 [torchgeo](https://github.com/torchgeo/torchgeo) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: known (45) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · MIT · Nov 2026</sub>

**PyTorch library of geospatial datasets, samplers and pretrained models.**

TorchGeo is a PyTorch domain library, modeled on torchvision, for training models on remote sensing data. It provides geospatial datasets that match CRS and resolution, samplers that draw patches by coordinates, benchmark datasets with download and checksum, and pretrained weights for multispectral sensors. Lightning datamodules, tasks and a CLI cover standard training runs.

- **+** Union (|) and intersection (&) operators combine datasets with differing CRS and resolution
- **+** Pretrained weights for multispectral sensors, using torchvision's multi-weight API
- **+** Lightning datamodules with fixed splits and a YAML-driven `torchgeo` CLI
- **+** Benchmark datasets download and checksum like torchvision, returning dicts of tensors
- **−** Geospatial imagery such as Landsat must be downloaded by the user; only some datasets auto-download
- **−** Tied to PyTorch and Lightning; no support for other tensor frameworks
- **−** Library only, with no UI or hosted service
- **−** Built-in tasks cover classification, regression and segmentation; other tasks need custom code

<sub>GPU optional · Needs PyTorch, Lightning, kornia, timm · Models: PyTorch, U-Net, ResNet, Mask R-CNN · [Repo](https://github.com/torchgeo/torchgeo) · [📖 Docs ↗](https://docs.torchgeo.org/en/stable/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/torchgeo/)</sub>

<a name="torchrec"></a>
### #&#8288;128 [torchrec](https://github.com/meta-pytorch/torchrec) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · BSD-3-Clause · Nov 2026</sub>

**PyTorch library for training recommender models with sharded embedding tables.**

TorchRec is a PyTorch domain library providing sparsity and parallelism primitives for large-scale recommender systems. It shards large embedding tables across many GPUs using several strategies, with a planner that generates sharding plans automatically and FBGEMM-based kernels. It powers production RecSys models at Meta and includes quantization, pipelined training, and Criteo and MovieLens datasets.

- **+** Sharding strategies: data-parallel, table-wise, row-wise, column-wise, and combined variants
- **+** Automatic planner generates sharding plans for a given model
- **+** Pipelined training overlaps data transfer, communication and compute
- **+** Used in production at Meta; Meta's DLRM is built on it
- **−** Focused on recommender systems; not meant for LLMs or general model work
- **−** Source install needs PyTorch nightly builds and a separate FBGEMM install
- **−** Multi-GPU setups are the main use case; install test runs through TorchX
- **−** Bundled examples limited to DLRM, Criteo and MovieLens

<sub>GPU optional · Needs PyTorch, FBGEMM, TorchX · Models: DLRM, PyTorch embedding-table recommender models · [Repo](https://github.com/meta-pytorch/torchrec) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/torchrec/)</sub>

<a name="pypots"></a>
### #&#8288;129 [pypots](https://github.com/wenjiedu/pypots) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · BSD-3-Clause · Nov 2026</sub>

**Python library for imputation and forecasting on time series with missing values.**

PyPOTS is a Python toolbox for machine learning on partially-observed multivariate time series. It offers one API for imputation, forecasting, classification, clustering and anomaly detection, with about 50 models including SAITS, BRITS, CSDI and TimesNet, plus naive baselines such as mean and LOCF. Hyperparameter tuning uses Optuna, and companion libraries cover dataset loading (TSDB) and missingness simulation (PyGrinder).

- **+** Five task types behind one unified API
- **+** Runnable example script for each algorithm and task in the model table
- **+** Optuna-based hyperparameter tuning; companion TSDB supports 172 datasets
- **+** Includes naive baselines (mean, median, LOCF/NOCB, Lerp) for comparison
- **−** Many models (Transformer, iTransformer) are adapted to missing data, not built for it
- **−** Task coverage is uneven; many models support only imputation
- **−** Time-Series.AI foundation model entry is a waitlist, not usable code
- **−** Library only: no server, UI or hosted API

<sub>Needs PyTorch, Optuna · Models: SAITS, BRITS, CSDI, TimesNet, MOMENT · [Repo](https://github.com/wenjiedu/pypots) · [📖 Docs ↗](https://docs.pypots.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pypots/)</sub>

<a name="behavior-1k"></a>
### #&#8288;130 [behavior-1k](https://github.com/stanfordvl/behavior-1k) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Nov 2026</sub>

**Simulation benchmark of 1,000 household activities for embodied AI agents.**

BEHAVIOR-1K is a monolithic repository for training and evaluating embodied AI agents on 1,000 everyday household tasks such as cleaning, cooking and organizing. The activities were chosen from human time-use surveys and preference studies. An installation script handles dependencies and supports installing only selected components.

- **+** Covers 1,000 household activities drawn from time-use surveys and preference studies
- **+** Single monorepo with a modular install script for choosing components
- **+** MIT license, with a paper (arXiv:2403.09227) and project website for reference
- **−** README gives no hardware, simulator or dependency details; these are only in the external guide
- **−** No Docker or compose files in the repository
- **−** README has no usage example or description of the training and evaluation API

<sub>Docker · [Repo](https://github.com/stanfordvl/behavior-1k) · [📖 Docs ↗](https://behavior.stanford.edu/getting_started/installation.html) · [🌐 Site ↗](https://behavior.stanford.edu/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/behavior-1k/)</sub>

<a name="kitops"></a>
### #&#8288;131 [kitops](https://github.com/kitops-ml/kitops) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · Apache-2.0 · Nov 2026</sub>

**CLI that packages AI/ML models and datasets as versioned OCI artifacts.**

KitOps packs model weights, datasets, code, prompts and config into a ModelKit, an immutable OCI artifact described by a Kitfile and pushed to any existing container registry. The Kit CLI covers pack, push, pull, unpack, diff and inspect, with selective layer unpacking and Cosign signing. It also reads and writes the CNCF ModelPack format, and a PyKitOps Python SDK is available.

- **+** Stores models in existing OCI registries, so no new artifact server is required
- **+** SHA-256 digests per layer plus Cosign signing for tamper detection and provenance
- **+** Pull only needed layers, such as model weights without the dataset
- **+** Integrations with KServe, Kubeflow Pipelines, MLflow, GitHub Actions, Dagger and a Kubernetes init container
- **−** Packages and distributes artifacts only; it does not train or serve models itself
- **−** Policy administration, multi-layer scanning and audit logs are in Jozu Hub, a separate product
- **−** Needs an OCI registry and Cosign setup to get signing and gating workflows
- **−** Teams must adopt the Kitfile and ModelKit formats alongside ModelPack

<sub>no GPU · Needs OCI container registry, Cosign (optional, for signing) · Models: ModelKit, CNCF ModelPack, Hugging Face import · [Repo](https://github.com/kitops-ml/kitops) · [📖 Docs ↗](https://kitops.org/docs/get-started/) · [🌐 Site ↗](https://kitops.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kitops/)</sub>

<a name="pytorch3d"></a>
### #&#8288;132 [pytorch3d](https://github.com/facebookresearch/pytorch3d) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (73) · Freshness: active (85) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · custom license · Nov 2026</sub>

**PyTorch library for differentiable 3D mesh operations and rendering.**

PyTorch3D provides triangle mesh data structures, mesh operations (projective transforms, graph convolution, sampling, losses) and a differentiable mesh renderer, all built on PyTorch tensors with heterogeneous minibatch support. It also includes Implicitron, a framework for novel-view synthesis with implicit representations. It targets 3D computer vision research, with tutorial notebooks for mesh fitting, NeRF and bundle adjustment.

- **+** All operators are differentiable, batch heterogeneous data and can run on GPU
- **+** Differentiable mesh renderer plus point cloud and volume rendering
- **+** Tutorial notebooks cover NeRF, bundle adjustment, textured mesh fitting and ShapeNet loading
- **+** Includes Implicitron framework for implicit-representation view synthesis
- **−** No backward-compatibility guarantee between releases
- **−** main branch and nightly builds may break at any time
- **−** README news list stops at v0.7.5 (Oct 2023)
- **−** License detected as NOASSERTION; README says BSD

<sub>GPU optional · Needs PyTorch · Models: triangle meshes, point clouds, volumes, implicit representations (NeRF) · [Repo](https://github.com/facebookresearch/pytorch3d) · [📖 Docs ↗](https://pytorch3d.readthedocs.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch3d/)</sub>

<a name="mlpack"></a>
### #&#8288;133 [mlpack](https://github.com/mlpack/mlpack) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · custom license · Nov 2026</sub>

**Header-only C++ machine learning library with CLI and multi-language bindings.**

mlpack is a header-only C++17 library implementing classical machine learning methods, built on Armadillo for linear algebra and ensmallen for optimization. It is also usable through command-line programs and Python, Julia, Go and R bindings. It targets researchers and production C++ deployments rather than LLM workloads.

- **+** Header-only: install headers and include <mlpack.hpp>, no separate library to build
- **+** Bindings for Python, Julia, Go and R, plus command-line programs
- **+** Fiscally sponsored by NumFOCUS with an open governance model
- **+** Quickstart guides exist for each interface, plus an examples repository
- **−** Template-heavy code leads to long compile times unless mitigated
- **−** Serializing neural networks needs a macro that significantly increases compile time
- **−** Older pthreads-based OpenBLAS (0.3.26 and older) can oversubscribe threads and slow down
- **−** Requires Armadillo, ensmallen and cereal installed alongside a C++17 compiler

<sub>Needs C++17 compiler, Armadillo >= 10.8, ensmallen >= 2.10.0, cereal >= 1.1.2, LAPACK/BLAS · [Repo](https://github.com/mlpack/mlpack) · [📖 Docs ↗](https://www.mlpack.org/doc/index.html) · [🌐 Site ↗](https://mlpack.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlpack/)</sub>

<a name="synapseml"></a>
### #&#8288;134 [synapseml](https://github.com/microsoft/synapseml) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (54) · Freshness: active (96) · Maintenance: patchy (49) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · MIT · Nov 2026</sub>

**Distributed ML pipelines on Apache Spark with LightGBM, Vowpal Wabbit and ONNX.**

SynapseML is a Scala library, with Python, R, Java and .NET bindings, that adds distributed ML estimators to Apache Spark and shares the SparkML API. It includes LightGBM, Vowpal Wabbit, ONNX inference, Azure AI service transformers, HTTP-on-Spark, Isolation Forest, and Spark Serving for exposing Spark computations as web services. Separate Maven builds exist for Spark 3.5 (Scala 2.12) and Spark 4.0/4.1 (Scala 2.13).

- **+** Same API as SparkML, so models drop into existing Spark pipelines
- **+** Bundles LightGBM, Vowpal Wabbit, ONNX, Isolation Forest and model interpretability tools
- **+** Preinstalled in Microsoft Fabric; documented for Databricks, Synapse, EMR and spark-submit
- **+** Separate builds for Spark 3.5, 4.0 and 4.1
- **−** Requires a Spark cluster or local Spark; not usable standalone
- **−** PyPI package lacks JVM jars; mismatched Scala artifacts cause missing-class errors
- **−** Spark 4 artifacts need a custom Maven repository on Azure blob storage
- **−** Master targets Spark 3.5 only; Spark 4 lives on separate branches

<sub>GPU optional · Needs Apache Spark 3.5 / 4.0 / 4.1, Maven repository mmlspark.blob.core.windows.net/maven · Models: LightGBM, Vowpal Wabbit, ONNX, SparkML · [Repo](https://github.com/microsoft/synapseml) · [📖 Docs ↗](https://microsoft.github.io/SynapseML/) · [🌐 Site ↗](https://aka.ms/spark) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/synapseml/)</sub>

<a name="shapash"></a>
### #&#8288;135 [shapash](https://github.com/maif/shapash) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Oct 2026</sub>

**Python library that explains tabular ML predictions via a web app and reports.**

Shapash wraps Shap or Lime to compute feature contributions for supervised tabular models, then presents them with readable labels. It launches a web app for moving between global and local explanations and generates a standalone HTML report for model audits. A SmartPredictor object carries local explanations into API or batch deployment.

- **+** Web app links global feature importance with per-sample explanations, filtering and sample picking
- **+** Standalone HTML audit report, customizable through a YAML block configuration
- **+** Built-in stability, consistency and compacity metrics to check explanation quality
- **+** SmartPredictor is a lighter object for serving explanations via API or batch
- **−** Limited to supervised regression, binary and multiclass problems
- **−** Native support covers Catboost, Xgboost, LightGBM, sklearn ensembles, linear models and SVM
- **−** Other models need contributions precomputed with Shap or similar and passed in manually
- **−** Needs Python 3.11 to 3.14; report generation requires the shapash[report] extra

<sub>no GPU · Needs Python 3.11-3.14, Shap, Lime · Models: Catboost, Xgboost, LightGBM, Sklearn Ensemble, Linear models · [Repo](https://github.com/maif/shapash) · [▶️ Demo ↗](https://shapash-demo.ossbymaif.fr/) · [📖 Docs ↗](https://shapash.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/shapash/)</sub>

<a name="cv-cuda"></a>
### #&#8288;136 [cv-cuda](https://github.com/cvcuda/cv-cuda) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · custom license · Oct 2026</sub>

**GPU-accelerated image processing operators for vision pipelines.**

CV-CUDA is an NVIDIA library of CUDA-based computer vision operators, such as resize, for pre- and post-processing images and video in AI pipelines. It has C/C++ and Python APIs and works with tools like nvImageCodec, so decoded data can stay on the GPU. Wheels are published on PyPI for CUDA 12 and CUDA 13.

- **+** Wheels for CUDA 12 and 13 on x86_64 and aarch64 SBSA, Python 3.10 to 3.14
- **+** C/C++ and Python APIs; tensors can come from GPU decoders like nvImageCodec
- **+** Jetson Orin and Thor builds are available alongside server GPUs
- **+** Compatibility table lists driver, compute capability and compiler per build
- **−** Requires an NVIDIA GPU with compute capability 7.5 or higher
- **−** No native Windows support, only WSL2
- **−** Only one CUDA major version of the packages can be installed at a time
- **−** Not accepting external contributions; OSD text rendering has known issues on Jetson

<sub>GPU required · Docker · Needs CUDA 12.2+ or 13.x, NVIDIA driver r525+ (r580+ for CUDA 13), CMake 3.24.3+ and gcc 10+ to build from source · [Repo](https://github.com/cvcuda/cv-cuda) · [📖 Docs ↗](https://cvcuda.github.io/CV-CUDA/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cv-cuda/)</sub>

<a name="ml"></a>
### #&#8288;137 [ml](https://github.com/rubixml/ml) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · MIT · Nov 2026</sub>

**Machine learning and deep learning library for PHP.**

Rubix ML is a PHP 8.3+ library, installed with Composer, covering the ML workflow from ETL and preprocessing to training and cross-validation. It ships more than 40 supervised and unsupervised algorithms. An optional Tensor extension speeds up matrix and vector math.

- **+** Brings ML training and inference into PHP codebases without a separate Python service
- **+** 40+ supervised and unsupervised algorithms plus preprocessing and cross-validation
- **+** Optional extensions: Tensor for fast math, Swoole for multiprocessing, GD for images
- **+** Docs site and a dozen example projects with pre-cleaned datasets
- **−** Fast matrix math needs compiling the Tensor extension with a C toolchain and BLAS libraries
- **−** Requires PHP 8.3 or newer
- **−** Docs are licensed CC BY-NC 4.0, which restricts commercial reuse
- **−** Ecosystem is far smaller than Python ML libraries

<sub>Needs PHP 8.3+, Composer, Tensor Ext 4.1+ (recommended), Swoole (optional), GD (optional), SVM extension (optional), PDO (optional), GraphViz (optional) · [Repo](https://github.com/rubixml/ml) · [📖 Docs ↗](https://rubixml.github.io/ML/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ml/)</sub>

<a name="pyts"></a>
### #&#8288;138 [pyts](https://github.com/johannfaouzi/pyts) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · BSD-3-Clause · Nov 2026</sub>

**Python library for time series classification with scikit-learn-style transformers.**

pyts is a Python package that implements time series classification algorithms and the transformations they rely on, using the scikit-learn API. It covers approximation (PAA, SAX, DFT, SFA), bag-of-words methods (BOSS, WEASEL), shapelets, ROCKET, image encodings (Gramian Angular Field, Recurrence Plot) and DTW metrics. Numba handles optimization, and datasets can be fetched from the UEA & UCR repository.

- **+** Scikit-learn-style estimators that fit into existing pipelines and cross-validation
- **+** Wide algorithm coverage: BOSSVS, SAXVSM, shapelets, TimeSeriesForest, ROCKET, WEASEL+MUSE
- **+** Includes DTW variants and time-series-to-image transforms (GAF, MTF, recurrence plot)
- **+** Fetches UEA & UCR benchmark datasets; installs from pip or conda-forge
- **−** No deep learning classifiers listed; algorithms are classical ML and feature-based
- **−** README says main-branch features may be missing from the latest release
- **−** Decomposition module offers only Singular Spectrum Analysis
- **−** Not an LLM or generative AI tool; scope is time series classification

<sub>no GPU · Needs Python >=3.11,<3.16, NumPy, SciPy, scikit-learn, Joblib, Numba · [Repo](https://github.com/johannfaouzi/pyts) · [📖 Docs ↗](https://pyts.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyts/)</sub>

<a name="dvc"></a>
### #&#8288;139 [dvc](https://github.com/treeverse/dvc) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: widely used (83) · Freshness: active (95) · Maintenance: weak (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

**Git-based versioning for data, models and ML pipelines.**

DVC is a Python command line tool that keeps data and model files in a cache and remote storage while tracking small metafiles in Git. It defines pipelines as stages with dependencies and outputs, reruns only the steps affected by a change, and tracks experiments in the local Git repo without a server. A VS Code extension provides a GUI for experiments and data management.

- **+** No server needed: experiments and data versions live in your Git repo
- **+** Remote storage on S3, Azure, Google Cloud, SSH and other backends
- **+** Pipelines rerun only stages whose dependencies changed
- **+** Installs via pip, brew, conda, choco, snap, deb or rpm
- **−** Command line first; the GUI is a separate VS Code extension that needs core DVC
- **−** Remote backends require optional extras such as dvc[s3] or dvc[azure]
- **−** Requires Git; no built-in hosted UI for team experiment comparison
- **−** README gives no hardware requirements or scale limits

<sub>no GPU · Needs Git, Remote storage (S3, Azure, Google Cloud, SSH, etc.) · [Repo](https://github.com/treeverse/dvc) · [📖 Docs ↗](https://dvc.org/doc) · [🌐 Site ↗](https://dvc.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dvc/)</sub>

<a name="ivy"></a>
### #&#8288;140 [ivy](https://github.com/unifyai/ivy) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: widely used (80) · Freshness: recent (71) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · custom license · Nov 2026</sub>

**Transpiler that converts ML code from PyTorch to TensorFlow, JAX or NumPy.**

ivy provides `ivy.transpile`, which converts functions, classes or whole libraries (e.g. kornia) from one ML framework to another, and `ivy.trace_graph`, which traces a functional graph from code. Per the support table, PyTorch is the only source framework; TensorFlow, JAX and NumPy are targets. Functions and classes are transpiled eagerly, modules lazily on first use.

- **+** Transpiles whole libraries lazily, e.g. kornia from PyTorch to TensorFlow
- **+** Single call API: ivy.transpile(fn, source, target)
- **+** Targets TensorFlow, JAX and NumPy from PyTorch code
- **+** Installs with pip; docs include examples and demos
- **−** Only PyTorch is a supported source today; other sources are marked planned
- **−** PyTorch as a target is only planned
- **−** License is NOASSERTION, so terms need manual checking
- **−** README examples contain errors, e.g. undefined jax_fn and test_fn

<sub>Needs PyTorch, TensorFlow, JAX, NumPy · Models: PyTorch (source), TensorFlow (target), JAX (target), NumPy (target) · [Repo](https://github.com/unifyai/ivy) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ivy/)</sub>

<a name="catboost"></a>
### #&#8288;141 [catboost](https://github.com/catboost/catboost) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (70) · Freshness: active (92) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Nov 2026</sub>

**Gradient boosting library over decision trees with categorical feature support.**

CatBoost is a C++ gradient boosting on decision trees library with Python, R, command-line and Apache Spark interfaces. It handles numerical and categorical features directly, trains on GPU and multi-GPU, and supports distributed training via Spark and the CLI. Models can be evaluated in applications through a C++ model API.

- **+** Native categorical feature handling without manual encoding
- **+** GPU and multi-GPU training supported out of the box
- **+** Distributed training through Apache Spark and a CLI
- **+** Python, R, CLI and Spark packages plus a C++ model API
- **−** Tabular gradient boosting only; not for LLMs or generative models
- **−** Quality and speed claims link to the project's own benchmarks
- **−** Documentation is hosted externally and may need Yandex domains allowed
- **−** README states no RAM or GPU requirements

<sub>GPU optional · Needs Apache Spark (optional, for distributed training) · Models: gradient boosted decision trees · [Repo](https://github.com/catboost/catboost) · [📖 Docs ↗](https://catboost.ai/docs/) · [🌐 Site ↗](https://catboost.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/catboost/)</sub>

<a name="pyro"></a>
### #&#8288;142 [pyro](https://github.com/pyro-ppl/pyro) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.1k · Apache-2.0 · Oct 2026</sub>

**Probabilistic programming library for Bayesian modeling and inference on PyTorch.**

Pyro is a Python probabilistic programming library built on PyTorch. It lets you write generative models as Python programs and run inference on them, with high-level abstractions and hooks for customizing inference. Originally developed at Uber AI, it is now a Linux Foundation project maintained by community contributors, including a team at the Broad Institute.

- **+** Built on PyTorch, so models can use tensors and neural networks directly
- **+** Described as universal: can represent any computable probability distribution
- **+** High-level inference abstractions, with easy access for customizing inference
- **+** Linux Foundation project with published JMLR paper, docs and a community forum
- **−** Requires knowledge of probabilistic modeling and Bayesian inference to be useful
- **−** Tied to PyTorch; no other tensor backend is mentioned in the README
- **−** Example and tutorial models need the separate [extras] install
- **−** README gives no hardware requirements or benchmark figures

<sub>GPU optional · Docker · Needs PyTorch · [Repo](https://github.com/pyro-ppl/pyro) · [📖 Docs ↗](http://docs.pyro.ai/) · [🌐 Site ↗](http://pyro.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyro/)</sub>

<a name="dowhy"></a>
### #&#8288;143 [dowhy](https://github.com/py-why/dowhy) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (68) · Freshness: active (83) · Maintenance: patchy (44) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · MIT · Nov 2026</sub>

**Python library for causal effect estimation, refutation and root cause analysis.**

DoWhy is a Python library for causal inference. It walks through modeling, identifying, estimating and refuting causal effects, and its graphical causal model module supports interventions, counterfactuals and anomaly attribution. It is not an LLM tool: it works on tabular data with NetworkX graphs and can call EconML estimators.

- **+** Four-step API (model, identify, estimate, refute) with refutation tests for any estimator
- **+** Graphical causal model module covers counterfactuals, interventional sampling and root cause analysis
- **+** Can use EconML CATE estimators such as DML through the same interface
- **+** Many example notebooks and a user guide; installs via pip, poetry or conda
- **−** No LLM or agent features; unrelated to model serving or chat tooling
- **−** Needs a causal graph or explicit causal assumptions from the user
- **−** pygraphviz install can fail on some platforms
- **−** Last release is 2025-11-08, so newer commits are not in a release

<sub>no GPU · Needs Python 3.8+, NetworkX, pandas, numpy, scikit-learn, EconML (optional), pydot or pygraphviz (optional) · [Repo](https://github.com/py-why/dowhy) · [📖 Docs ↗](https://py-why.github.io/dowhy/) · [🌐 Site ↗](https://www.pywhy.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dowhy/)</sub>

<a name="tslearn"></a>
### #&#8288;144 [tslearn](https://github.com/tslearn-team/tslearn) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (33) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · BSD-2-Clause · Nov 2026</sub>

**Time series clustering and classification in Python, scikit-learn style.**

tslearn is a Python library of time series algorithms behind a scikit-learn style API: k-means and KShape clustering, KNN, SVM and shapelet classifiers, regression, and metrics such as DTW, Global Alignment Kernel and matrix profile. Data is held as 3D numpy arrays, and variable-length series are supported. It includes UCR dataset loaders, synthetic generators and scalers.

- **+** Models follow the scikit-learn API and work with its pipelines and tuning
- **+** Covers DTW, Global Alignment Kernel, barycenters and matrix profile
- **+** Supports variable-length series and loads UCR datasets directly
- **+** Installs from PyPI or conda-forge; docs include an example gallery
- **−** Requires data as 3D numpy arrays, so conversion from other formats is needed
- **−** Scope is classical time series ML; no forecasting models are listed
- **−** Requires Python 3.11 or newer

<sub>no GPU · Needs numpy, scikit-learn · Models: KNN, TimeSeriesKMeans, KShape, KernelKMeans, TimeSeriesSVC · [Repo](https://github.com/tslearn-team/tslearn) · [📖 Docs ↗](https://tslearn.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tslearn/)</sub>

<a name="hls4ml"></a>
### #&#8288;145 [hls4ml](https://github.com/fastmachinelearning/hls4ml) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Nov 2026</sub>

**Converts trained ML models into FPGA firmware via high-level synthesis.**

hls4ml is a Python package that translates trained models from open-source ML frameworks into HLS projects for ultra-low-latency inference on FPGAs. It supports Vivado HLS, Vitis HLS, Intel HLS, Catapult HLS and Altera HLS IP Gen as synthesis backends. It originated in CERN trigger systems and is also used for quantum control, fusion feedback loops and biomedical signals.

- **+** Supports several HLS backends: Vivado, Vitis, Intel, Catapult and Altera HLS IP Gen
- **+** Installs with pip or conda-forge; conversion to an HLS project takes a few Python calls
- **+** Backed by published papers, a tutorial repository and a documentation site
- **+** Has features for CNNs, binary/ternary networks, distributed arithmetic and spiking networks
- **−** Synthesis needs a separate vendor HLS toolchain, such as Xilinx Vivado HLS
- **−** README says builds can take several minutes per model
- **−** Targets FPGA firmware only; not a general inference server or UI
- **−** README example shows only Keras v2 conversion; other frameworks are not listed

<sub>no GPU · Needs Vivado HLS, Vitis HLS, Intel HLS, Catapult HLS or Altera HLS IP Gen, FPGA target · Models: Keras · [Repo](https://github.com/fastmachinelearning/hls4ml) · [📖 Docs ↗](https://fastmachinelearning.org/hls4ml/) · [🌐 Site ↗](https://fastmachinelearning.org/hls4ml/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hls4ml/)</sub>

<a name="scvi-tools"></a>
### #&#8288;146 [scvi-tools](https://github.com/scverse/scvi-tools) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · BSD-3-Clause · Nov 2026</sub>

**PyTorch library of probabilistic models for single-cell omics analysis.**

scvi-tools is a Python package of probabilistic models for single-cell, multi-omic and spatial omics data, built on PyTorch and AnnData. It covers dimensionality reduction, data integration, automated annotation, doublet detection and spatial deconvolution, with a high-level API that works with Scanpy. It also provides building blocks on PyTorch Lightning and Pyro for writing new models.

- **+** Models share one API with save/load and GPU acceleration, and work with Scanpy and AnnData
- **+** Building blocks on PyTorch Lightning and Pyro for writing custom probabilistic models
- **+** Covers integration, annotation, doublet detection, factor analysis and spatial deconvolution
- **+** Published in Nature Biotechnology; part of scverse, with a skeleton repo for new models
- **−** Domain-specific to single-cell omics; not a general-purpose ML or LLM tool
- **−** PyTorch must be installed separately to match your GPU
- **−** Assumes familiarity with the Scanpy and AnnData workflow

<sub>GPU optional · Docker · Needs PyTorch, AnnData, PyTorch Lightning, Pyro, Scanpy · Models: PyTorch, Pyro · [Repo](https://github.com/scverse/scvi-tools) · [📖 Docs ↗](https://docs.scvi-tools.org/) · [🌐 Site ↗](https://scvi-tools.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scvi-tools/)</sub>

<a name="apex"></a>
### #&#8288;147 [apex](https://github.com/nvidia/apex) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · BSD-3-Clause · Nov 2026</sub>

**NVIDIA PyTorch utilities for mixed precision and distributed training.**

Apex is an NVIDIA-maintained PyTorch extension library with fused CUDA kernels and utilities for mixed precision and distributed training. It provides FusedAdam, FusedLayerNorm, FusedRMSNorm, SyncBatchNorm, DistributedDataParallel and amp, plus many optional apex.contrib modules. Some of the code is intended to land in upstream PyTorch eventually.

- **+** Fused CUDA kernels for Adam, LayerNorm, RMSNorm and SyncBatchNorm
- **+** Maintained by NVIDIA; extensions come preinstalled in NGC PyTorch containers
- **+** Python-only build available when CUDA extensions cannot be compiled
- **+** Many optional contrib modules, each enabled by its own build flag
- **−** Source install compiles C++/CUDA extensions, which can be slow and memory-heavy
- **−** Contrib modules may only work with PyTorch nightlies, not stable releases
- **−** Python-only build drops fused kernels, so some components run slower
- **−** Windows support is experimental; no tagged release

<sub>GPU required · Needs PyTorch, CUDA, Ninja (recommended), cuDNN >=8.4/8.5 (some modules), NCCL >=2.10/2.19 (some modules) · [Repo](https://github.com/nvidia/apex) · [📖 Docs ↗](https://docs.nvidia.com/deeplearning/frameworks/pytorch-release-notes/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/apex/)</sub>

<a name="numpyro"></a>
### #&#8288;148 [numpyro](https://github.com/pyro-ppl/numpyro) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · Apache-2.0 · Nov 2026</sub>

**Probabilistic programming library on JAX with NUTS/HMC and variational inference.**

NumPyro is a Python probabilistic programming library that provides a NumPy/JAX backend for Pyro's model API (sample, param, plate, effect handlers). It JIT-compiles inference, including the full NUTS tree-building step, through XLA to CPU, GPU or TPU. Inference covers MCMC variants (NUTS, HMC, MixedHMC, HMCECS, BarkerMH, SA) and stochastic variational inference with autoguides.

- **+** JIT-compiles the whole NUTS tree build with JAX, removing Python overhead
- **+** Broad MCMC set: NUTS, HMC, MixedHMC, HMCECS, BarkerMH, HMCGibbs, SA
- **+** Pyro-like API and torch.distributions-style distributions; TFP distributions usable in models
- **+** Automatically sums out finite discrete latents so NUTS/HMC can run on the rest
- **−** README warns of brittleness, bugs and API changes under active development
- **−** No global param store or random state; models must be written functionally
- **−** Requires explicit PRNG key handling, unfamiliar to PyTorch/Pyro users
- **−** Inference gets harder as latent dimension grows; may need reparameterization

<sub>GPU optional · Docker · Needs JAX · Models: NUTS, HMC, MixedHMC, HMCECS, BarkerMH · [Repo](https://github.com/pyro-ppl/numpyro) · [📖 Docs ↗](https://num.pyro.ai/en/stable/getting_started.html#installation) · [🌐 Site ↗](https://num.pyro.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/numpyro/)</sub>

<a name="detectron2"></a>
### #&#8288;149 [detectron2](https://github.com/facebookresearch/detectron2) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: widely used (94) · Freshness: recent (70) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Oct 2026</sub>

**PyTorch library for object detection and segmentation research.**

Detectron2 is Facebook AI Research's PyTorch library for object detection and segmentation, successor to Detectron and maskrcnn-benchmark. It covers panoptic segmentation, DensePose, Cascade R-CNN, rotated boxes, PointRend, DeepLab, ViTDet and MViTv2, and ships a Model Zoo of baselines. Models can be exported to TorchScript or Caffe2.

- **+** Wide algorithm coverage: panoptic segmentation, DensePose, PointRend, ViTDet, MViTv2, rotated boxes
- **+** Model Zoo with downloadable baselines and trained weights
- **+** Export to TorchScript or Caffe2 for deployment
- **+** Modular design for building research projects on top; Apache-2.0
- **−** Last tagged release is 2021-11-15, though commits continue
- **−** Not a model server; no inference API or UI included
- **−** Install steps live in external docs, not the README

<sub>Docker + Compose · Needs PyTorch · Models: Mask R-CNN, Cascade R-CNN, Panoptic segmentation, DensePose, PointRend · [Repo](https://github.com/facebookresearch/detectron2) · [▶️ Demo ↗](https://colab.research.google.com/drive/16jcaJoc6bCFAQ96jDe2HwtXj7BMD_-m5) · [📖 Docs ↗](https://detectron2.readthedocs.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/detectron2/)</sub>

<a name="recommenders"></a>
### #&#8288;150 [recommenders-team/recommenders](https://github.com/recommenders-team/recommenders) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: widely used (88) · Freshness: recent (70) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Nov 2026</sub>

**Recommender-system algorithms and Jupyter notebooks in Python.**

Recommenders is a Python package and notebook collection for building recommendation systems. It includes about 30 algorithm implementations, such as ALS, SAR, NCF, LightGCN, SASRec and xDeepFM. It also has utilities for dataset loading, train/test splitting and offline metrics. A MovieLens benchmark notebook compares the collaborative filtering models. The project is hosted by the Linux Foundation of AI and Data.

- **+** Covers classic and deep recommenders: ALS, SAR, BPR, LightGCN, SASRec, xDeepFM, Wide and Deep
- **+** Most algorithms have a quick start or deep dive notebook
- **+** Shared utilities for data loading, splitting and ranking/rating metrics
- **+** Core pip package runs CPU notebooks; extras for gpu, spark and dev
- **−** Notebook-driven examples, not a serving system or hosted API
- **−** Operationalization examples target Azure only
- **−** Some models sit in an experimental extra and may need extra install steps
- **−** Last tagged release is 2024-12-24, while main has newer commits

<sub>GPU optional · Needs Python 3.11, gcc, Jupyter, Spark (optional, for ALS) · Models: ALS, SAR, NCF, LightGCN, SASRec · [Repo](https://github.com/recommenders-team/recommenders) · [📖 Docs ↗](https://readthedocs.org/projects/microsoft-recommenders/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/recommenders/)</sub>

<a name="pytorch-grad-cam"></a>
### #&#8288;151 [pytorch-grad-cam](https://github.com/jacobgil/pytorch-grad-cam) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Nov 2026</sub>

**PyTorch library of CAM methods for explaining vision model predictions.**

pytorch-grad-cam implements pixel attribution methods such as GradCAM, HiResCAM, ScoreCAM, AblationCAM, LayerCAM and FullGrad for PyTorch vision models. It works with CNNs and vision transformers on classification, object detection, segmentation and embedding-similarity tasks, using a reshape transform and custom model targets. It also includes metrics such as ROAD and ARCC for checking explanation quality.

- **+** Around 20 CAM methods behind one API, including gradient-free ones like AblationCAM and ScoreCAM
- **+** Batch support in all methods; reshape_transform adapts it to ViT and Swin
- **+** Built-in metrics (ROAD, ARCC) to evaluate and tune explanations
- **+** Tutorials cover Faster-RCNN, YOLO5, segmentation, HuggingFace and embeddings
- **−** Vision only; no text or LLM explainability
- **−** Target layer must be chosen manually per architecture
- **−** aug_smooth multiplies run time by 6; ScoreCAM and AblationCAM need many forward passes
- **−** No tagged releases; installed from PyPI as grad-cam

<sub>GPU optional · Needs PyTorch, torchvision, OpenCV · Models: ResNet, VGG, DenseNet, MobileNet, Vision Transformer · [Repo](https://github.com/jacobgil/pytorch-grad-cam) · [📖 Docs ↗](https://jacobgil.github.io/pytorch-gradcam-book) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-grad-cam/)</sub>

<a name="lite-ai-toolkit"></a>
### #&#8288;152 [lite.ai.toolkit](https://github.com/xlite-dev/lite.ai.toolkit) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (48) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · GPL-3.0 · Nov 2026</sub>

**C++ library running 100+ pretrained vision models via ONNXRuntime, MNN and TensorRT.**

Lite.Ai.ToolKit is a C++ library that wraps pretrained computer-vision models (YOLO variants, face detection and recognition, segmentation, matting) behind a consistent API such as lite::cv::detection::YoloV5. It runs on ONNXRuntime by default, with optional MNN and TensorRT (10.x, CUDA 12.x) backends. The README claims 300+ C++ implementations and 500+ weights, distributed through ONNX, MNN, NCNN and TNN model hubs.

- **+** Default dependencies are only OpenCV and ONNXRuntime
- **+** Same C++ call pattern across detection, face, segmentation and matting models
- **+** Optional TensorRT backend for YOLO, face models, StableDiffusion and FaceFusion
- **+** Prebuilt Linux library and sample weights published on the v0.2.0 release
- **−** Build script officially supports Linux only; macOS and Windows are marked unofficial
- **−** GPL-3.0 license restricts use in closed-source products
- **−** Last release was 2025-07; maintainer says his focus moved to LLM inference
- **−** Mostly vision models; no LLM serving or text generation

<sub>GPU optional · Needs OpenCV, ONNXRuntime 1.17.1, MNN 2.8.2 (optional), TensorRT 10.x (optional), CUDA 12.x (optional) · Models: ONNX, MNN, NCNN, TNN, TensorRT engine · [Repo](https://github.com/xlite-dev/lite.ai.toolkit) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lite-ai-toolkit/)</sub>

<a name="pyslam"></a>
### #&#8288;153 [pyslam](https://github.com/luigifreda/pyslam) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (37) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · GPL-3.0 · Nov 2026</sub>

**Visual SLAM framework for mono, stereo and RGBD cameras in Python and C++.**

pySLAM is a research framework for visual odometry and SLAM with monocular, stereo and RGBD input. It has a sparse-SLAM core in both Python and C++ (pybind11, with maps interchangeable), plus loop closing, volumetric reconstruction (TSDF, Gaussian splatting), depth prediction and semantic segmentation. It also runs feed-forward 3D inference models such as DUSt3R and VGGT.

- **+** Python and C++ SLAM cores share a map format, so maps load in either
- **+** Many swappable local features, global descriptors and depth models behind one interface
- **+** Reads over 10 dataset types, including KITTI, TUM, EuRoC, ScanNet and ROS bags
- **+** Supports both g2o and GTSAM for graph optimization
- **−** Install is a long script run that builds OpenCV and many dependencies
- **−** Gaussian splatting and dust3r-based methods require CUDA
- **−** Self-described research framework and work in progress
- **−** Docker only via a third-party repo; Windows needs WSL2

<sub>GPU optional · Needs Python 3.11.9, OpenCV >=4.10, PyTorch >=2.3.1, TensorFlow >=2.13.1, Kornia, Rerun, g2o, GTSAM · Models: DepthPro, DepthAnythingV2, DepthAnythingV3, RAFT-Stereo, CREStereo · [Repo](https://github.com/luigifreda/pyslam) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyslam/)</sub>

<a name="minari"></a>
### #&#8288;154 [minari](https://github.com/farama-foundation/minari) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · custom license · Nov 2026</sub>

**Python library for creating and loading offline reinforcement learning datasets.**

Minari is a Python library from the Farama Foundation for offline RL research, described as an offline version of Gymnasium. It provides a CLI and Python API to list, download and read remote datasets such as D4RL/door/human-v2, and a DataCollector wrapper that records Gymnasium environment episodes into new datasets. Datasets work with TorchRL, d3rlpy and AgileRL.

- **+** DataCollector wraps any Gymnasium env to record episodes into a dataset
- **+** CLI covers list, download and show for remote and local datasets
- **+** Integrates with TorchRL, d3rlpy and AgileRL training libraries
- **+** Tutorial recreates the D4RL Maze2D datasets with Pointmaze
- **−** Provides datasets only; no training algorithms of its own
- **−** Built around Gymnasium environments and its episode format
- **−** License is detected as NOASSERTION, so terms need manual checking
- **−** Extra dependencies are installed per use case, not by default

<sub>Needs gymnasium · [Repo](https://github.com/farama-foundation/minari) · [📖 Docs ↗](https://minari.farama.org/main/) · [🌐 Site ↗](https://minari.farama.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/minari/)</sub>

<a name="neuralpde-jl"></a>
### #&#8288;155 [neuralpde.jl](https://github.com/sciml/neuralpde.jl) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · custom license · Nov 2026</sub>

**Julia package for solving PDEs with physics-informed neural networks.**

NeuralPDE.jl is a Julia solver library that trains neural networks (PINNs) to solve ODEs, SDEs, RODEs and PDEs. PDEs are written in a symbolic ModelingToolkit interface and discretized into an optimization problem, with the physics-informed loss built automatically. It works with Flux.jl and Lux.jl layers and with NeuralOperators.jl.

- **+** Builds physics-informed loss automatically from a symbolic PDESystem definition
- **+** Supports extra loss terms to combine equation solving with data fitting
- **+** Works with both Flux.jl and Lux.jl, including their GPU layers
- **+** Mixes neural operators (DeepONet, FNO, GNO) with physics-informed losses via NeuralOperators.jl
- **−** Julia only; requires the Julia ecosystem (ModelingToolkit, Lux, Optimization.jl)
- **−** License is reported as NOASSERTION, so terms need checking in the repository
- **−** Niche scientific use; not a general LLM or generative AI tool
- **−** README example needs two Adam stages (4000 and 2000 iterations) for a simple 2D Poisson problem

<sub>GPU optional · Needs Julia, ModelingToolkit.jl, Lux.jl or Flux.jl, OptimizationOptimisers · Models: Lux.jl, Flux.jl, NeuralOperators.jl · [Repo](https://github.com/sciml/neuralpde.jl) · [📖 Docs ↗](https://docs.sciml.ai/NeuralPDE/stable/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/neuralpde-jl/)</sub>

<a name="open-spiel"></a>
### #&#8288;156 [open_spiel](https://github.com/google-deepmind/open_spiel) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Nov 2026</sub>

**Game environments and algorithms for reinforcement learning and search research.**

OpenSpiel is a DeepMind library of game environments and RL/search algorithms covering n-player, zero-sum, cooperative and general-sum games, with perfect and imperfect information, turn-based and simultaneous moves. The core API and games are written in C++ and exposed to Python, and it includes tools for analyzing learning dynamics and evaluation metrics. Pretrained baseline checkpoints and game datasets are published on a public storage bucket.

- **+** Wide game coverage: extensive-form, simultaneous-move, imperfect-information, grid worlds, social dilemmas
- **+** C++ core with Python bindings; algorithms available in both languages
- **+** Colab notebooks and video tutorials cover CFR and REINFORCE on Kuhn and Leduc poker
- **+** Semantic versioning; pretrained checkpoints and datasets published
- **−** Research library for games, not a general LLM or agent toolkit
- **−** Separate install paths for Linux/macOS and Windows; core is C++
- **−** README does not list games or algorithms; readers must consult the docs
- **−** No turnkey app; using the environments requires writing code

<sub>Docker · [Repo](https://github.com/google-deepmind/open_spiel) · [▶️ Demo ↗](https://colab.research.google.com/github/deepmind/open_spiel/blob/master/open_spiel/colabs/install_open_spiel.ipynb) · [📖 Docs ↗](https://openspiel.readthedocs.io/en/latest/?badge=latest) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-spiel/)</sub>

<a name="linfa"></a>
### #&#8288;157 [linfa](https://github.com/rust-ml/linfa) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: patchy (47) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · Apache-2.0 · Nov 2026</sub>

**Rust toolkit of classical ML algorithms, modeled on scikit-learn.**

Linfa is a collection of Rust crates implementing preprocessing and classical machine learning algorithms, in the spirit of scikit-learn. It covers clustering, linear and logistic regression, SVMs, decision trees, ensembles, PCA and t-SNE, each as a separate sub-crate. It uses a pure-Rust linear algebra backend by default, with optional OpenBLAS, Netlib or Intel MKL.

- **+** Modular crates: depend only on the algorithms you need, such as clustering or svm
- **+** Pure-Rust default backend, with optional OpenBLAS, Netlib or Intel MKL via features
- **+** Browser WASM on wasm32-unknown-unknown through the wasm-bindgen feature
- **+** Broad classical coverage: K-Means, DBSCAN, random forest, AdaBoost, PCA, t-SNE, TF-IDF
- **−** No neural network or deep learning crate in the algorithm list
- **−** Logistic regression is described as two-class only
- **−** OpenBLAS and Netlib backends are listed for Linux only
- **−** Rust only, with no Python bindings mentioned

<sub>no GPU · Needs Rust toolchain, optional OpenBLAS/Netlib/Intel MKL · Models: K-Means, DBSCAN, random forest, SVM, linear regression · [Repo](https://github.com/rust-ml/linfa) · [📖 Docs ↗](https://docs.rs/linfa) · [🌐 Site ↗](https://rust-ml.github.io/linfa/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/linfa/)</sub>

<a name="neural-compressor"></a>
### #&#8288;158 [neural-compressor](https://github.com/intel/neural-compressor) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · Apache-2.0 · Nov 2026</sub>

**Python library for quantizing PyTorch and JAX models, tuned for Intel hardware.**

Intel Neural Compressor is a Python library that applies static and dynamic quantization, SmoothQuant, weight-only quantization, quantization-aware training and mixed precision to PyTorch and JAX models. It covers FP8, MXFP8/MXFP4 and NVFP4 formats, and integrates with AutoRound for LLM and VLM quantization. Intel Gaudi, Xeon, Core Ultra and Intel GPUs are the extensively tested targets.

- **+** Covers many methods: static, dynamic, SmoothQuant, weight-only, FP8, MX, NVFP4, mixed precision
- **+** AutoRound integration for LLM and VLM quantization (LLaMA, Qwen, DeepSeek)
- **+** Separate pip packages for PyTorch (neural-compressor-pt) and JAX (neural-compressor-jax)
- **+** FP8 support on Intel Gaudi, including DeepSeek V3/R1 static quantization
- **−** AMD CPU, ARM CPU and NVIDIA GPU have only limited testing
- **−** MXFP, NVFP4, FP8 KV cache and Keras/JAX FP8 are marked experimental
- **−** Gaudi use needs a matching Gaudi software stack version, per a version map
- **−** Requires Python 3.11 or newer

<sub>GPU optional · Needs PyTorch, JAX, intel_extension_for_pytorch, AutoRound, Intel Gaudi software stack (for HPU) · Models: PyTorch, JAX, Keras, Hugging Face transformers, GPTQ · [Repo](https://github.com/intel/neural-compressor) · [📖 Docs ↗](https://intel.github.io/neural-compressor) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/neural-compressor/)</sub>

<a name="autograd"></a>
### #&#8288;159 [autograd](https://github.com/hips/autograd) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · MIT · Nov 2026</sub>

**Automatic differentiation for native Python and NumPy code.**

Autograd differentiates Python and NumPy functions, including code with loops, ifs, recursion and closures. It supports reverse-mode and forward-mode differentiation, which can be composed to any derivative order. It is aimed at gradient-based optimization, with examples for neural nets, LSTMs, Gaussian processes and a fluid simulation.

- **+** Differentiates plain Python and NumPy code, including loops, recursion and closures
- **+** Reverse- and forward-mode can be composed for higher-order derivatives
- **+** Installs with pip; SciPy support is an optional extra
- **+** Examples cover CNN, RNN, LSTM, Bayesian neural net and Gaussian process
- **−** README does not mention GPU support; it is built around NumPy
- **−** Reverse-mode is efficient only for scalar-valued functions of array arguments
- **−** Requires importing the thinly-wrapped autograd.numpy instead of plain numpy
- **−** No built-in neural network layers or optimizers described in the README

<sub>Needs numpy, scipy (optional) · [Repo](https://github.com/hips/autograd) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autograd/)</sub>

<a name="swe-bench"></a>
### #&#8288;160 [swe-bench](https://github.com/swe-bench/swe-bench) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: patchy (35) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Sep 2026</sub>

**Benchmark and Docker harness for scoring LLM patches on real GitHub issues.**

SWE-bench is a dataset and evaluation harness that gives a model a codebase and a GitHub issue, then runs the generated patch in Docker containers to check whether it resolves the issue. It covers the full, Lite, Verified (500 tasks), Multimodal and Multilingual sets, and has a `swebench` CLI for evaluation, image builds, inference and result reports. It also ships SWE-Llama checkpoints and BM25 retrieval datasets.

- **+** Containerized Docker harness gives reproducible pass/fail grading of patches
- **+** Covers full, Lite, Verified, Multimodal and Multilingual task sets from one `swebench` CLI
- **+** Cloud evaluation available through Modal or the separate sb-cli on AWS
- **+** Includes SWE-Llama 7b/13b weights and BM25 retrieval datasets on Hugging Face
- **−** Needs about 120GB free disk, 16GB RAM and 8 CPU cores for local runs
- **−** arm64 support is experimental; v5 CLI builds images locally from a task repo
- **−** Results are cached by run_id and instance_id, so changed patches need a new run_id
- **−** Support for creating new SWE-bench instances is temporarily paused

<sub>RAM ≥ 16 GB · Needs Docker, Hugging Face datasets, Modal (optional), sb-cli (optional) · Models: SWE-Llama 7b, SWE-Llama 13b, API models via mini-SWE-agent · [Repo](https://github.com/swe-bench/swe-bench) · [📖 Docs ↗](https://swebench.com/SWE-bench/) · [🌐 Site ↗](https://swebench.com/SWE-bench/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/swe-bench/)</sub>

<a name="pytorch-forecasting"></a>
### #&#8288;161 [pytorch-forecasting](https://github.com/sktime/pytorch-forecasting) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · MIT · Nov 2026</sub>

**PyTorch library for time series forecasting with neural network architectures.**

Python package that trains deep learning forecasting models on pandas DataFrames through a TimeSeriesDataSet class and PyTorch Lightning. It includes Temporal Fusion Transformer, N-BEATS, N-HiTS, DeepAR, PatchTST, LSTM/GRU and MLP baselines, plus multi-horizon metrics and Optuna hyperparameter tuning. Training runs on CPU or on one or more GPUs, with TensorBoard logging.

- **+** TimeSeriesDataSet handles transformations, missing values and variable history lengths
- **+** Ships TFT, N-BEATS, N-HiTS, DeepAR and PatchTST with interpretation plots
- **+** Lightning-based training on CPU, single or multi-GPU with TensorBoard logging
- **+** Built-in Optuna tuning and a tutorial for implementing custom models
- **−** Forecasting only; no general-purpose model or LLM support
- **−** Requires PyTorch and Lightning; Windows needs a manual PyTorch install step
- **−** Input must be a pandas DataFrame with integer time index and string series IDs
- **−** Model set is limited to the listed architectures plus custom implementations

<sub>GPU optional · Needs PyTorch, PyTorch Lightning, pandas, Optuna, TensorBoard · Models: Temporal Fusion Transformer, N-BEATS, N-HiTS, DeepAR, PatchTST · [Repo](https://github.com/sktime/pytorch-forecasting) · [📖 Docs ↗](https://pytorch-forecasting.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-forecasting/)</sub>

<a name="jetson-containers"></a>
### #&#8288;162 [jetson-containers](https://github.com/dusty-nv/jetson-containers) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: weak (14) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · custom license · Oct 2026</sub>

**Modular container build system for AI/ML packages on NVIDIA Jetson.**

Build and run CUDA-enabled Docker images for NVIDIA Jetson (JetPack 6.2 and 7) and ARM SBSA servers (GH200/GB200). The `jetson-containers` CLI composes packages such as PyTorch, vLLM, llama.cpp, ROS, ComfyUI and Whisper into one image, and `autotag` picks a prebuilt image matching the installed L4T version. A pip/devpi server caches wheels to shorten rebuilds.

- **+** Composes multiple packages into one image: `jetson-containers build pytorch transformers ros:humble-desktop`
- **+** Covers LLM, VLM, speech, diffusion, robotics and simulation packages in one repo
- **+** `autotag` selects a prebuilt image compatible with the device's JetPack/L4T version
- **+** CUDA_VERSION and related variables rebuild the stack for other CUDA, cuDNN, TensorRT or Python versions
- **−** Only JetPack 6.2 (CUDA 12.6) and JetPack 7 (CUDA 13.x) are stated as tested
- **−** Source builds of PyTorch and similar packages are slow without the wheel cache
- **−** Targets NVIDIA Jetson and SBSA ARM; no x86 or non-NVIDIA support is described
- **−** License is reported as NOASSERTION, so terms need checking per package

<sub>GPU required · Compose · Needs Docker, NVIDIA container runtime, JetPack/L4T · Models: PyTorch, TensorFlow, JAX, ONNX Runtime, llama.cpp · [Repo](https://github.com/dusty-nv/jetson-containers) · [📖 Docs ↗](https://github.com/dusty-nv/jetson-containers/blob/master/docs/setup.md) · [🌐 Site ↗](https://www.jetson-ai-lab.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jetson-containers/)</sub>

<a name="fairlearn"></a>
### #&#8288;163 [fairlearn](https://github.com/fairlearn/fairlearn) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · MIT · Nov 2026</sub>

**Python library for measuring and reducing group unfairness in ML models.**

Fairlearn is a Python package with two parts: metrics that show which groups a model harms, and mitigation algorithms that reduce unfairness under several group-fairness definitions. It also ships Jupyter example notebooks and a user guide. It addresses allocation harms and quality-of-service harms, with the relevant groups specified by the data scientist.

- **+** Covers both assessment metrics and mitigation algorithms in one package
- **+** Installs with pip install fairlearn; no services or database needed
- **+** Docs include user guide, quickstart, API reference and example gallery
- **+** MIT license; recent release and commits
- **−** Group fairness only; individual fairness is not covered by the README
- **−** Groups must be chosen and specified by the user for each application
- **−** Example notebooks from main may not match pip-installed versions
- **−** Quantitative metrics cannot capture justice or due process

<sub>[Repo](https://github.com/fairlearn/fairlearn) · [📖 Docs ↗](https://fairlearn.org/main/user_guide/index.html) · [🌐 Site ↗](https://fairlearn.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fairlearn/)</sub>

<a name="drawdata"></a>
### #&#8288;164 [drawdata](https://github.com/koaning/drawdata) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Nov 2026</sub>

**Notebook widget for drawing a scatter dataset with the mouse.**

drawdata is a small Python library built on anywidget that lets you draw a 2D scatter dataset in a notebook. The drawn points are available as a list of dicts, a pandas or polars dataframe, or as scikit-learn style X, y arrays. It runs in marimo, Jupyter, VSCode and Colab, and is aimed at teaching machine learning.

- **+** Exports drawn data as dicts, pandas, polars, or sklearn X, y
- **+** Works in marimo, Jupyter, VSCode and Colab through anywidget
- **+** Browser demo page requires no installation
- **+** data_as_X_y infers classification from multiple colors, regression from one
- **−** Only a scatter widget is documented; no other chart or data types
- **−** Drawing is a manual 2D interaction, so no high-dimensional or large datasets
- **−** README has no API reference beyond a few properties
- **−** Last tagged release is January 2026

<sub>no GPU · Needs anywidget, Python notebook environment (marimo, Jupyter, VSCode or Colab) · [Repo](https://github.com/koaning/drawdata) · [▶️ Demo ↗](https://koaning.github.io/drawdata) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/drawdata/)</sub>

<a name="deepep"></a>
### #&#8288;165 [deepep](https://github.com/deepseek-ai/deepep) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (75) · Freshness: recent (79) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

**GPU communication kernels for MoE expert-parallel dispatch and combine.**

DeepEP is a CUDA and PyTorch library providing all-to-all kernels for MoE expert parallelism, including FP8 dispatch, behind a single EPBuffer API for training, prefill and decoding. It also offers NVLink weight prefetch and gradient reduction for redundant experts, plus experimental pipeline-parallel, Engram and bucketed collective primitives. Kernels are JIT-compiled at runtime through DeepJIT and use an NCCL Gin backend.

- **+** One EPBuffer API covers training, prefill and decoding, with FP8 dispatch support
- **+** Analytical SM and QP count estimate replaces auto-tuning
- **+** Reuses existing NCCL communicators; NVSHMEM is no longer a dependency
- **+** Redundant-expert weight prefetch and FP32 gradient reduction over NVLink
- **−** Requires Hopper or newer NVIDIA GPUs, NVLink, and RDMA for multi-node
- **−** Needs CUDA Toolkit 13.1+, NCCL 2.32.3+, PyTorch 2.10+, and a C++20 compiler
- **−** Bucket, Engram and PP features are experimental
- **−** Dispatch and combine consume GPU SMs; zero-SM RDMA EP is unsupported

<sub>GPU required · Needs PyTorch 2.10+, NCCL 2.32.3+, CUDA Toolkit 13.1+, DeepJIT, NVLink, RDMA network · Models: MoE models (BF16, FP8 dispatch) · [Repo](https://github.com/deepseek-ai/deepep) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepep/)</sub>

<a name="deepxde"></a>
### #&#8288;166 [deepxde](https://github.com/lululxvi/deepxde) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (48) · Freshness: active (100) · Maintenance: patchy (41) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · LGPL-2.1 · Nov 2026</sub>

**Python library for physics-informed neural networks and operator learning.**

DeepXDE is a Python library for scientific machine learning. It solves forward and inverse ODEs, PDEs, integro-differential, fractional and stochastic PDEs with PINNs, and learns operators with DeepONet variants and multifidelity networks. It runs on TensorFlow 1.x, TensorFlow 2.x, PyTorch, JAX or PaddlePaddle backends.

- **+** Five selectable backends: TensorFlow 1.x/2.x, PyTorch, JAX, PaddlePaddle
- **+** Geometry primitives plus CSG and point clouds, so no mesh generation is needed
- **+** Covers PINN variants (fPINN, gPINN, hPINN) and DeepONet, MIONet, multifidelity networks
- **+** Documented demos for forward, inverse and operator-learning problems; installs via pip or conda
- **−** Requires installing a backend framework separately before DeepXDE works
- **−** LGPL-2.1 license may constrain some proprietary or bundled use
- **−** Library only: no GUI, server or pretrained model hub

<sub>GPU optional · Docker · Needs TensorFlow, PyTorch, JAX, Flax, Optax, PaddlePaddle · Models: PINN, DeepONet, MIONet, MFNN, FNN · [Repo](https://github.com/lululxvi/deepxde) · [📖 Docs ↗](https://deepxde.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepxde/)</sub>

<a name="textblob"></a>
### #&#8288;167 [textblob](https://github.com/sloria/textblob) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: popular (72) · Freshness: recent (70) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · MIT · Nov 2026</sub>

**Python library for part-of-speech tagging, sentiment and noun phrase extraction.**

TextBlob is a Python library that wraps NLTK and pattern behind a small API for classic NLP tasks. It covers part-of-speech tagging, noun phrase extraction, sentiment polarity, Naive Bayes and Decision Tree classification, tokenization, n-grams, lemmatization, spelling correction and WordNet lookups. It is a rule- and statistics-based toolkit, not an LLM library.

- **+** Small API: a TextBlob object exposes tags, noun_phrases, sentences and sentiment as attributes
- **+** Installs with pip; no model server or database needed
- **+** Tagging, sentiment, classification, n-grams, inflection and spelling correction in one package
- **+** MIT licensed; new models or languages can be added through extensions
- **−** Built on NLTK and pattern, so accuracy is limited to classic non-neural methods
- **−** Needs a separate corpora download step after pip install
- **−** README describes no LLM, embedding or transformer support
- **−** Last tagged release is 2013-09-26, though commits continue

<sub>no GPU · Needs NLTK, pattern, NLTK corpora (python -m textblob.download_corpora) · Models: Naive Bayes classifier, Decision Tree classifier · [Repo](https://github.com/sloria/textblob) · [📖 Docs ↗](https://textblob.readthedocs.io/) · [🌐 Site ↗](https://textblob.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/textblob/)</sub>

<a name="tensorboard"></a>
### #&#8288;168 [tensorboard](https://github.com/tensorflow/tensorboard) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Nov 2026</sub>

**Web dashboards for inspecting TensorFlow training runs, graphs and embeddings.**

TensorBoard reads tfevents files from a log directory and serves a local web UI, by default on port 6006, for inspecting training runs. It has scalar, histogram, distribution, image, audio, text and time series dashboards, plus a graph explorer and an embedding projector. It runs offline and supports third-party plugins published on PyPI.

- **+** Runs fully offline against a local log directory with one `tensorboard --logdir` command
- **+** Compares runs by recursively loading every subdirectory that contains tfevents data
- **+** Plugin system documented in ADDING_A_PLUGIN, with example plugins and PyPI distribution
- **+** Covers scalars, histograms, images, audio, text, model graphs and an embedding projector
- **−** Reads one events file at a time; multiple writers need the experimental --reload_multifile flag
- **−** Reservoir-samples data to fit in RAM, so plots may not show every point
- **−** No native scatterplots or custom plots; workaround is writing matplotlib images
- **−** README names only Chrome and Firefox as supported browsers

<sub>no GPU · Docker · Needs TensorFlow summary event files (tfevents), Bazel (only to build from source) · Models: TensorFlow · port 6006 · [Repo](https://github.com/tensorflow/tensorboard) · [📖 Docs ↗](https://www.tensorflow.org/tensorboard/get_started) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorboard/)</sub>

<a name="ao"></a>
### #&#8288;169 [ao](https://github.com/pytorch/ao) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: known (31) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · custom license · Nov 2026</sub>

**PyTorch quantization, QAT and float8 training library for HF models.**

TorchAO quantizes PyTorch model weights and activations (int4, int8, float8, MXFP8, NVFP4) through a `quantize_` API with config objects, and works with `torch.compile` and FSDP2. It also covers quantization-aware training, float8 training and low-bit optimizers. Per the README, new feature development is being minimized, with primitives moving into `torch` and workflows into frameworks such as torchtitan.

- **+** Integrated as a quantization backend in transformers, diffusers, vLLM, Axolotl, Unsloth and torchtitan
- **+** Covers PTQ, QAT, float8 training and 4/8-bit optimizers in one library
- **+** Pre-quantized models published on the Hugging Face Hub under pytorch
- **+** Reported int4 Llama-3-8B result: 1.89x faster inference with 58% less memory
- **−** New feature development is being minimized; only compatibility updates and case-by-case fixes
- **−** Fastest kernels need optional MSLK, CUTLASS DSL and tvm-ffi installs
- **−** Some workflows are prototype and hardware-specific, such as MXFP8 MoE training
- **−** Torch version compatibility is tracked in a separate GitHub issue table

<sub>GPU optional · Needs PyTorch, MSLK (optional), apache-tvm-ffi (optional), nvidia-cutlass-dsl (optional) · Models: Hugging Face transformers models, diffusers pipelines (FLUX.1, CogVideoX), Llama, Qwen3, Gemma3 · [Repo](https://github.com/pytorch/ao) · [📖 Docs ↗](https://docs.pytorch.org/ao/stable/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ao/)</sub>

<a name="meta-ax"></a>
### #&#8288;170 [meta/ax](https://github.com/meta/ax) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · MIT · Nov 2026</sub>

**Python library for Bayesian and bandit optimization of adaptive experiments.**

Ax is a Python platform for running adaptive experiments: it proposes parameter configurations, records results, and iterates toward an optimum. Bayesian optimization is provided by BoTorch on PyTorch, alongside bandit optimization. It supports multiple objectives, parameter and outcome constraints, noisy observations, parallel trials and early stopping.

- **+** Handles multi-objective problems, outcome constraints and noisy observations in one API
- **+** Built on BoTorch with sensible defaults, so little tuning is needed to start
- **+** Suggests parallel trials, synchronous or asynchronous, with early stopping support
- **+** Installs from PyPI wheels for macOS, Linux and Windows; MIT licensed
- **−** Requires Python 3.11 or newer
- **−** Fully Bayesian SAAS models need the separate fully_bayesian extra with JAX/NumPyro
- **−** Not an LLM tool; no model serving or agent features
- **−** Latest release (2026-06-09) is older than recent commits, so main may differ from PyPI

<sub>Needs BoTorch, PyTorch, GPyTorch, MySQL (optional storage extra), JAX/NumPyro (optional extra) · [Repo](https://github.com/meta/ax) · [📖 Docs ↗](https://ax.dev) · [🌐 Site ↗](https://ax.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/meta-ax/)</sub>

<a name="responsible-ai-toolbox"></a>
### #&#8288;171 [responsible-ai-toolbox](https://github.com/microsoft/responsible-ai-toolbox) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Nov 2026</sub>

**Dashboards for debugging model errors, fairness and explanations in Jupyter.**

Responsible AI Toolbox ships the raiwidgets Python package, which renders interactive dashboards for error analysis, fairness, interpretability, counterfactuals, causal analysis and data balance. It wraps Fairlearn, InterpretML, DiCE and EconML behind one dashboard for tabular, text and vision models. It installs with pip and is used from notebooks.

- **+** Combines error analysis, fairness, explanations, counterfactuals and causal inference in one dashboard
- **+** Built on Fairlearn, InterpretML, DiCE and EconML rather than reimplementing them
- **+** Notebook examples cover tabular, text and vision models, including object detection
- **+** Accepts scikit-style models plus PyTorch, TensorFlow and Keras
- **−** Mitigations, tracker and GenBit live in three separate repositories
- **−** Aimed at classic ML debugging; LLM examples are limited to QA notebooks
- **−** Runs inside Jupyter notebooks; no standalone server or deployment described
- **−** Models need scikit-style predict or predict_proba, or a wrapper function

<sub>Needs Jupyter, Fairlearn, InterpretML, DiCE, EconML · Models: scikit-learn style predict/predict_proba, PyTorch, TensorFlow, Keras, numpy.ndarray · [Repo](https://github.com/microsoft/responsible-ai-toolbox) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/responsible-ai-toolbox/)</sub>

<a name="skrub"></a>
### #&#8288;172 [skrub](https://github.com/skrub-data/skrub) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · BSD-3-Clause · Nov 2026</sub>

**Python library for machine learning on dataframes.**

skrub is a Python library that facilitates machine learning with dataframes. It installs with pip or conda, and its docs and examples ship inside the package (see skrub.__docs_dir__). The README gives few feature details and points to the website, examples gallery and learning materials for scope.

- **+** Installable with pip or conda; no services or containers required
- **+** Docs and examples are bundled in the package under skrub/_docs
- **+** BSD-3-Clause license with CI and coverage badges and a PyPI release
- **+** Examples gallery and learning materials are linked from the README
- **−** README lists no concrete features or APIs; readers must go to the docs
- **−** Targets tabular dataframe work; no LLM or model-serving features described
- **−** No live demo is linked

<sub>[Repo](https://github.com/skrub-data/skrub) · [📖 Docs ↗](https://skrub-data.org/stable/install.html) · [🌐 Site ↗](https://skrub-data.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skrub/)</sub>

<a name="botorch"></a>
### #&#8288;173 [botorch](https://github.com/meta-pytorch/botorch) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (40) · Freshness: active (100) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Nov 2026</sub>

**Bayesian optimization library built on PyTorch and GPyTorch.**

BoTorch is a Python library for composing Bayesian optimization loops from Gaussian process models, acquisition functions and optimizers. It uses PyTorch autodiff and supports Monte Carlo acquisition functions via the reparameterization trick, with GPyTorch models underneath. The README positions it as a low-level API for researchers and recommends Ax for end-users.

- **+** Modular primitives: models, acquisition functions and optimizers compose separately
- **+** Monte Carlo acquisition functions via reparameterization, no restrictive model assumptions
- **+** First-class GPyTorch support, including multi-task GPs, deep kernel learning and deep GPs
- **+** Device-agnostic PyTorch code runs on GPUs with autodiff
- **−** README describes it as beta and under active development
- **−** Aimed at researchers; non-researchers are directed to Ax instead
- **−** Requires Python 3.11+ plus gpytorch, linear_operator and pyro-ppl
- **−** Official Anaconda package stopped after 0.12; conda-forge only

<sub>GPU optional · Needs PyTorch >= 2.0.1, gpytorch >= 1.14, linear_operator >= 0.6, pyro-ppl >= 1.8.4, scipy, multiple-dispatch · Models: Gaussian processes (GPyTorch), multi-task GPs, deep kernel learning, deep GPs · [Repo](https://github.com/meta-pytorch/botorch) · [📖 Docs ↗](https://botorch.org/docs/introduction) · [🌐 Site ↗](https://botorch.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/botorch/)</sub>

<a name="optimum"></a>
### #&#8288;174 [optimum](https://github.com/huggingface/optimum) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (38) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · Apache-2.0 · Nov 2026</sub>

**Hugging Face toolkit for exporting and running models on specific accelerators.**

Optimum extends Transformers, Diffusers, TIMM and Sentence-Transformers with export, quantization and hardware-specific inference and training wrappers. It covers ONNX Runtime, OpenVINO, ExecuTorch, Intel Gaudi, AWS Inferentia/Trainium, NVIDIA TensorRT-LLM, AMD and FuriosaAI through pip extras. Export and optimization run from Python or the optimum-cli.

- **+** Covers many backends: ONNX Runtime, OpenVINO, ExecuTorch, Gaudi, Inferentia, Trainium, TensorRT-LLM
- **+** Export and optimization available both as Python API and optimum-cli
- **+** Per-accelerator pip extras, e.g. optimum[openvino], optimum[neuronx]
- **+** Trainer wrappers for Gaudi and Trainium alongside inference tooling
- **−** ONNX support moved to the separate optimum-onnx package, splitting docs and installs
- **−** Much of the functionality lives in sibling repos such as optimum-intel and optimum-habana
- **−** Library only; no model server or HTTP API included
- **−** Each backend needs its own dependencies and hardware, so setup differs per target

<sub>GPU optional · Needs Transformers, ONNX Runtime, OpenVINO, ExecuTorch, optimum-onnx · Models: Transformers, Diffusers, TIMM, Sentence-Transformers, ONNX · [Repo](https://github.com/huggingface/optimum) · [📖 Docs ↗](https://huggingface.co/docs/optimum/index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/optimum/)</sub>

<a name="lingvo"></a>
### #&#8288;175 [lingvo](https://github.com/tensorflow/lingvo) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Oct 2026</sub>

**TensorFlow framework for building sequence models, with reference ASR, MT and LM tasks.**

Lingvo is a TensorFlow framework for defining, training and evaluating neural networks, aimed at sequence models. It ships a trainer/evaler job runner and model configs for speech recognition, machine translation, language modelling, 3D object detection and MNIST. Installs from PyPI (0.14.0) or builds from source with bazel and g++.

- **+** Reference configs for Listen-Attend-Spell ASR, Transformer MT, StarNet and DeepFusion 3D detection
- **+** GShard config for a 1T-parameter language model on CloudTPU v3-512
- **+** Pip install plus a Colab codelab and API docs for getting started
- **+** Trainer and evaler run as separate jobs, with MNIST runnable on CPU in about 20 seconds
- **−** No backwards compatibility guarantees between releases; breaking changes are listed as non-comprehensive
- **−** Tied to TensorFlow; source builds need bazel and officially only g++ 7.3
- **−** Modifying the framework or adding custom ops is difficult with the pip package
- **−** MT, giant LM and 3D detection models need GPU or TPU clusters

<sub>GPU optional · Docker · Needs TensorFlow, bazel, g++ · Models: TensorFlow checkpoints, ASR, machine translation, language models, 3D object detection · [Repo](https://github.com/tensorflow/lingvo) · [📖 Docs ↗](https://tensorflow.github.io/lingvo/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lingvo/)</sub>

<a name="dopamine"></a>
### #&#8288;176 [dopamine](https://github.com/google/dopamine) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (76) · Freshness: recent (70) · Maintenance: patchy (35) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

**Reinforcement learning research framework with compact JAX agent implementations.**

Dopamine is a small Python codebase for prototyping reinforcement learning algorithms, built to be read and modified directly. It ships JAX implementations of DQN, C51, Rainbow, IQN, SAC and PPO, with legacy TensorFlow versions of many, and targets Atari and Mujoco environments. Baseline results and Colab notebooks are provided, and the setup follows Machado et al. (2018) for reproducibility.

- **+** Small codebase meant to be edited directly for research experiments
- **+** Covers DQN, C51, Rainbow, IQN, SAC and PPO in JAX
- **+** Published baseline results and Colab notebooks for each agent
- **+** Evaluation setup follows Machado et al. (2018) recommendations
- **−** Last tagged release is from 2019-09-26
- **−** Only a few algorithms; not a broad RL library
- **−** Mujoco setup references mujoco-py and a license step, which is dated
- **−** TensorFlow agents are legacy; new agents are likely JAX-only

<sub>Docker · Needs jax, tensorflow (legacy agents), ale_py, mujoco-py, openai baselines · Models: DQN, C51, Rainbow, IQN, SAC · [Repo](https://github.com/google/dopamine) · [📖 Docs ↗](https://google.github.io/dopamine/docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dopamine/)</sub>

<a name="mlxtend"></a>
### #&#8288;177 [mlxtend](https://github.com/rasbt/mlxtend) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · custom license · Sep 2026</sub>

**Python library of scikit-learn extensions for ensembles, feature selection and plotting.**

mlxtend is a Python library that adds data science utilities on top of the scientific Python stack. It provides stacking and voting classifiers, feature selection and extraction, decision-region and confusion-matrix plots, and Apriori-based frequent pattern mining for association rules. It installs from PyPI and works with scikit-learn estimators.

- **+** Covers stacking, voting, feature selection and association rule mining in one package
- **+** Decision-region plotting works with scikit-learn-style classifiers
- **+** Published in JOSS with a DOI, documentation and changelog
- **+** BSD license, stated as commercially usable
- **−** Classical ML only; no LLM, deep learning or agent features
- **−** Scope is broad and loosely related, with no single focus
- **−** Plotting example uses only two features of the iris data
- **−** Repo license detected as NOASSERTION, while README states BSD

<sub>no GPU · Needs scikit-learn, numpy, matplotlib · Models: scikit-learn estimators · [Repo](https://github.com/rasbt/mlxtend) · [📖 Docs ↗](https://rasbt.github.io/mlxtend) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlxtend/)</sub>

<a name="pgmpy"></a>
### #&#8288;178 [pgmpy](https://github.com/pgmpy/pgmpy) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (36) · Freshness: active (98) · Maintenance: patchy (37) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Nov 2026</sub>

**Python library for causal discovery and inference with Bayesian networks.**

pgmpy is a Python library with data structures for DAGs, PDAGs, MAGs, PAGs, Bayesian Networks, Dynamic Bayesian Networks and Structural Equation Models. It covers structure learning (for example the PC estimator), parameter estimation, probabilistic and causal inference, model validation and data simulation. Estimators follow a composable API that is scikit-learn compatible where possible.

- **+** Covers discrete, linear Gaussian and functional (mixed) Bayesian networks in one API
- **+** Includes structure learning, parameter fitting, inference and simulation in the same library
- **+** Ships example datasets and models, such as bnlearn alarm and ecoli70
- **+** Installs from PyPI or conda-forge; MIT license
- **−** Functional Bayesian Networks need the torch backend and pyro
- **−** Not an LLM tool; no agent, model-serving or LLM integration
- **−** Learning and inference examples for functional networks live in a separate notebook, not the README

<sub>Needs torch and pyro (Functional Bayesian Networks only) · Models: DAG, PDAG, MAG, PAG, Discrete Bayesian Network · [Repo](https://github.com/pgmpy/pgmpy) · [📖 Docs ↗](https://pgmpy.org/) · [🌐 Site ↗](https://pgmpy.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pgmpy/)</sub>

<a name="colabfold"></a>
### #&#8288;179 [colabfold](https://github.com/sokrypton/colabfold) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · MIT · Nov 2026</sub>

**Protein structure prediction with AlphaFold2 and other models using MMseqs2 MSAs.**

ColabFold packages AlphaFold2 and related folding models (OpenFold3, ESMFold, RoseTTAFold2, Boltz, BioEmu) as Google Colab notebooks and as a pip-installable colabfold_batch / colabfold_search CLI. MSAs come from the public MMseqs2 server or from locally built databases, and can be exported as AlphaFold3 JSON. Local runs use JAX, with optional fused kernels and a compilation cache.

- **+** Runs in Google Colab notebooks with no local setup
- **+** MMseqs2 MSAs from the public server or local databases, with optional GPU search
- **+** Fused-kernel option runs AlphaFold2 about 2.5x faster on Ampere or newer GPUs
- **+** Exports MSAs as AlphaFold3 JSON, with DNA, RNA and ligands via FASTA syntax
- **−** Local MSA databases need about 940GB of disk and roughly 128GB RAM for searches
- **−** Public MSA server allows only serial queries from a single IP
- **−** Several notebooks are marked beta or in development
- **−** Each new sequence length or MSA depth triggers a slow recompile

<sub>RAM ≥ 128 GB · GPU optional · Docker · Needs MMseqs2 18 (8cc5c), JAX, OpenMM, conda, CUDA 12 or 13 · Models: AlphaFold2, AlphaFold2-multimer, OpenFold3, ESMFold, RoseTTAFold2 · [Repo](https://github.com/sokrypton/colabfold) · [▶️ Demo ↗](https://colab.research.google.com/github/sokrypton/ColabFold/blob/main/AlphaFold2.ipynb) · [📖 Docs ↗](https://github.com/sokrypton/ColabFold/wiki/Running-ColabFold-in-Docker) · [🌐 Site ↗](https://colabfold.mmseqs.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/colabfold/)</sub>

<a name="vizdoom"></a>
### #&#8288;180 [vizdoom](https://github.com/farama-foundation/vizdoom) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 2.1k · no license · Nov 2026</sub>

**Doom-based environment for training reinforcement learning agents from screen pixels.**

ViZDoom wraps the ZDoom engine so agents can play Doom using only the screen buffer, with Python and C++ APIs and Gymnasium/Gym wrappers. It exposes depth, audio, object labels and map geometry, and supports sync and async single-player and multiplayer modes. It targets visual reinforcement learning research, with custom scenarios built through map editors and ACS scripting.

- **+** Up to 7000 steps per second in sync mode, single-threaded
- **+** Gymnasium wrappers install with pip; wheels for Linux, macOS and Windows
- **+** Exposes depth buffer, audio, labeled objects and map geometry beyond raw pixels
- **+** Custom scenarios via standard Doom map editors and ACS scripting
- **−** Ships with Freedoom graphics; original Doom assets need your own WAD files
- **−** Windows is less tested than Linux and macOS, per the README
- **−** macOS wheels from 1.3.0 cover Apple Silicon only; Intel needs 1.2.4
- **−** Bundles ZDoom code under mixed licenses, not a single MIT license

<sub>no GPU · Needs Python 3.10+, OpenAL (optional, for audio), C++11 compiler, CMake 3.12+, Boost 1.54+, SDL2 (source builds only) · Models: Gymnasium, Gym · [Repo](https://github.com/farama-foundation/vizdoom) · [📖 Docs ↗](https://vizdoom.farama.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vizdoom/)</sub>

<a name="argos-translate"></a>
### #&#8288;181 [argos-translate](https://github.com/argosopentech/argos-translate) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (62) · Freshness: recent (70) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.7k · MIT · Nov 2026</sub>

**Offline machine translation library for Python, built on OpenNMT.**

Argos Translate translates text offline using OpenNMT models run through CTranslate2. It works as a Python library, a command-line tool (argospm, argos-translate) or a separate GUI, and installs language models as .argosmodel packages. When no direct pair is installed, it pivots through an intermediate language, such as es to en to fr, at some cost in quality.

- **+** Runs fully offline once language packages are installed
- **+** Installs with pip; usable from Python, CLI or GUI
- **+** Automatic pivoting through intermediate languages covers pairs without a direct model
- **+** Optional GPU via ARGOS_DEVICE_TYPE=cuda or auto, passed to CTranslate2
- **−** Last tagged release is 2021-08-24, though commits continue
- **−** Pivot translations lose quality compared with direct pairs
- **−** GUI, HTML and file translation live in separate repositories
- **−** Custom models cost $1000 per language, per the README

<sub>GPU optional · Needs OpenNMT, CTranslate2 · Models: .argosmodel packages (OpenNMT) · [Repo](https://github.com/argosopentech/argos-translate) · [▶️ Demo ↗](https://libretranslate.com) · [📖 Docs ↗](https://argos-translate.readthedocs.io) · [🌐 Site ↗](https://www.argosopentech.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/argos-translate/)</sub>

<a name="pyaudioanalysis"></a>
### #&#8288;182 [pyaudioanalysis](https://github.com/tyiannak/pyaudioanalysis) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Oct 2026</sub>

**Python library for audio feature extraction, classification and segmentation.**

pyAudioAnalysis extracts audio features such as MFCCs, spectrograms and chromagrams, and trains classifiers and regression models on WAV segments. It also covers silence removal, supervised and unsupervised segmentation including speaker diarization, and audio thumbnails. Functions are callable from Python or through the audioAnalysis.py command line.

- **+** Covers features, classification, regression, diarization and silence detection in one library
- **+** Every function is also exposed through a command-line script
- **+** Train a classifier from folders of WAV files in one call
- **+** Backed by a peer-reviewed PLoS ONE paper and a wiki with tutorials
- **−** Install is a git clone plus pip install -e, with no PyPI package mentioned
- **−** No tagged releases
- **−** Examples use classical models like SVM; no deep learning, which the group's other repos cover
- **−** Docs split between a short README and a separate wiki

<sub>Models: SVM classifiers, audio regression models, WAV files · [Repo](https://github.com/tyiannak/pyaudioanalysis) · [📖 Docs ↗](https://github.com/tyiannak/pyAudioAnalysis/wiki) · [🌐 Site ↗](https://magcil.github.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyaudioanalysis/)</sub>

<a name="captum"></a>
### #&#8288;183 [captum](https://github.com/meta-pytorch/captum) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (56) · Freshness: active (96) · Maintenance: weak (26) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · BSD-3-Clause · Nov 2026</sub>

**Model interpretability library for PyTorch with attribution algorithms.**

Captum is a Python library that explains PyTorch model predictions. It implements attribution methods such as Integrated Gradients, DeepLift, GradientShap, SmoothGrad and VarGrad via NoiseTunnel, layer and neuron conductance, TCAV and TracIn influence functions, plus adversarial attack and perturbation tools. It installs with pip and requires Python 3.10+ and PyTorch 2.3+.

- **+** Wide set of attribution methods: IG, DeepLift, GradientShap, TCAV, TracIn, conductance
- **+** Works on any PyTorch nn.Module, with layer- and neuron-level attribution
- **+** Convergence delta gives a checkable approximation error for several methods
- **+** Plain pip install, BSD-3-Clause, with tutorials and paper references per algorithm
- **−** PyTorch only; no support for other frameworks
- **−** DeepLift supports only the Rescale rule and not all non-linear activations
- **−** Captum Insights visualization UI was retired after v0.8.0
- **−** A research library, not an app; users write Python to apply it

<sub>GPU optional · Needs Python >= 3.10, PyTorch >= 2.3 · Models: PyTorch models, torchvision, torchtext · [Repo](https://github.com/meta-pytorch/captum) · [🌐 Site ↗](https://captum.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/captum/)</sub>

<a name="tensorflow-datasets"></a>
### #&#8288;184 [tensorflow/datasets](https://github.com/tensorflow/datasets) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: known (49) · Freshness: active (98) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · Apache-2.0 · Nov 2026</sub>

**Python library that loads public datasets as tf.data pipelines.**

TensorFlow Datasets (TFDS) is a Python library that downloads and prepares public datasets, such as MNIST, and returns them as tf.data.Dataset objects through tfds.load. It aims for the same examples in the same order for every user, and it has a guide for adding custom datasets. It does not host the datasets; it fetches them from their original sources.

- **+** One call, tfds.load, returns a tf.data.Dataset with split, shuffle and as_supervised options
- **+** Deterministic: all users get the same examples in the same order
- **+** Public catalog plus documented process for adding or requesting datasets
- **+** Apache-2.0, published on PyPI, requires Python 3.11+
- **−** Output is built around tf.data; other frameworks are not covered in the README
- **−** Does not host data; each dataset's license is left to the user to check
- **−** No guarantee of dataset quality or fairness, per the project disclaimer
- **−** Dataset catalog and API docs live on tensorflow.org, not in the repo README

<sub>Needs tensorflow, Python 3.11+ · [Repo](https://github.com/tensorflow/datasets) · [▶️ Demo ↗](https://colab.research.google.com/github/tensorflow/datasets/blob/master/docs/overview.ipynb) · [📖 Docs ↗](https://www.tensorflow.org/datasets/overview) · [🌐 Site ↗](https://www.tensorflow.org/datasets) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorflow-datasets/)</sub>

<a name="parl"></a>
### #&#8288;185 [parl](https://github.com/paddlepaddle/parl) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: known (37) · Freshness: active (100) · Maintenance: patchy (41) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · Apache-2.0 · Nov 2026</sub>

**Reinforcement learning framework with a decorator-based distributed training API.**

PARL is a Python reinforcement learning framework built around Model, Algorithm and Agent abstractions. It ships reference implementations of DQN, DDPG, TD3, SAC, PPO, A2C, IMPALA, QMIX, MADDPG, CQL and ES. The xparl module distributes actors across CPUs or machines by decorating a class with parl.remote_class and calling parl.connect.

- **+** Many reference RL algorithms (DQN, PPO, SAC, IMPALA, QMIX) with examples
- **+** Distributed actors via @parl.remote_class and parl.connect, little code change
- **+** Parallelization API usable without paddlepaddle installed
- **+** xparl uses CURVE-authenticated, encrypted ZeroMQ and binds to loopback by default
- **−** Training algorithms depend on paddlepaddle (>=2.3.1), not PyTorch
- **−** xparl executes submitted Python, so only for trusted machines
- **−** Security fixes require upgrading all nodes and clients together
- **−** Focused on RL only, not LLM agents or serving

<sub>GPU optional · Needs paddlepaddle>=2.3.1 (optional, for training), Python 3.6+ · [Repo](https://github.com/paddlepaddle/parl) · [📖 Docs ↗](https://parl.readthedocs.io/en/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/parl/)</sub>

<a name="nx"></a>
### #&#8288;186 [elixir-nx/nx](https://github.com/elixir-nx/nx) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: minimal (30) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 2.9k · no license · Nov 2026</sub>

**Tensors and numerical definitions for Elixir, with XLA and LibTorch backends.**

Nx is a multi-dimensional array (tensor) library for Elixir with numerical definitions. This repository also holds EXLA, a backend built on Google's XLA compiler, and Torchx, a backend built on LibTorch. Each subproject has its own README, and the README says they will later be extracted into separate repositories.

- **+** Brings tensors and numerical definitions to the Elixir ecosystem
- **+** Two backends to choose from: XLA via EXLA, LibTorch via Torchx
- **+** Examples and benchmarks are available in the EXLA project
- **−** Elixir only, so usable just from BEAM-based projects
- **−** Top-level README is a pointer; details live in subproject READMEs
- **−** Subprojects are planned to move out of this repository
- **−** No license detected in the repository metadata

<sub>Needs Elixir, XLA (EXLA), LibTorch (Torchx) · [Repo](https://github.com/elixir-nx/nx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nx/)</sub>

<a name="thinc"></a>
### #&#8288;187 [thinc](https://github.com/explosion/thinc) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: patchy (47) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Oct 2026</sub>

**Functional, type-checked Python library for composing deep learning models.**

Thinc is a lightweight deep learning library from the makers of spaCy and Prodigy. Models are built by composing layers rather than subclassing, with a mypy plugin for type checking and a config system that describes object trees and hyperparameters. It can wrap PyTorch, TensorFlow and MXNet layers, and runs on numpy or cupy backends.

- **+** Composition-based model definition with mypy plugin for type-checking model graphs
- **+** Wraps PyTorch, TensorFlow and MXNet models as layers inside one network
- **+** Integrated config system and function registry for hyperparameters and object trees
- **+** Used in production via spaCy and Prodigy; MIT licensed
- **−** Optimizers limited to vanilla SGD, Adam and RAdam
- **−** Backends limited to numpy and cupy
- **−** Building from source needs a C compiler for the extensions
- **−** Examples center on tagging and MNIST; no LLM-scale recipes

<sub>GPU optional · Needs numpy, cupy (optional, GPU), PyTorch (optional), TensorFlow (optional), MXNet (optional), Ray (optional, example) · Models: PyTorch, TensorFlow, MXNet · [Repo](https://github.com/explosion/thinc) · [📖 Docs ↗](https://thinc.ai/docs) · [🌐 Site ↗](https://thinc.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/thinc/)</sub>

<a name="tfx"></a>
### #&#8288;188 [tfx](https://github.com/tensorflow/tfx) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Nov 2026</sub>

**TensorFlow-based framework for building production ML pipelines from components.**

TFX is a Python framework from the TensorFlow project for defining ML pipelines out of standard components, with run records kept in an ML Metadata backend. Pipelines can be orchestrated with Apache Airflow or Kubeflow Pipelines, and both components and orchestrator integrations are extensible. Each release is tied to specific versions of TensorFlow, Apache Beam, TFDV, TFT and related packages.

- **+** ML Metadata backend records runs, artifacts and config, enabling experiment tracking and warmstarting
- **+** Orchestrates on Apache Airflow or Kubeflow Pipelines; components and integrations are extensible
- **+** Compatibility table maps each tfx release to tested dependency versions
- **+** Ships a Chicago Taxi example pipeline, tutorials and a user guide
- **−** Built around TensorFlow; the README names no other training framework
- **−** Many pinned dependencies (Beam, tfx-bsl, TFDV, TFT) complicate upgrades
- **−** Compatibility table lists Python 3.10-3.12, while the badge also shows 3.13
- **−** README names only Airflow and Kubeflow Pipelines as orchestrators

<sub>Needs TensorFlow, Apache Beam, ML Metadata, Apache Airflow, Kubeflow Pipelines · Models: TensorFlow · [Repo](https://github.com/tensorflow/tfx) · [📖 Docs ↗](https://github.com/tensorflow/tfx/blob/master/docs/guide/index.md) · [🌐 Site ↗](https://www.tensorflow.org/tfx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tfx/)</sub>

<a name="intelligent-trading-bot"></a>
### #&#8288;189 [intelligent-trading-bot](https://github.com/asavinov/intelligent-trading-bot) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Nov 2026</sub>

**Python ML pipeline for crypto trading signals with offline training and online service.**

Config-driven Python pipeline that downloads Binance or Yahoo market data, builds technical-indicator features and future-looking labels, trains classification or regression models, and combines predictions into a score between -1 and +1. A service script runs the same features online at a set interval, such as every minute, and sends signals to Telegram or other outputs. It includes rolling walk-forward backtesting and a trade simulator.

- **+** Same feature definitions used in offline training and the online service, by design
- **+** Rolling walk-forward retraining in predict_rolling gives more realistic backtests
- **+** Features, labels, signals and outputs are defined as Python functions in a JSON config
- **+** Includes talib, tsfresh and custom feature generators and a simulate script for trade rules
- **−** Data download supports only Binance and Yahoo; sources are not extendable
- **−** Feature generation is non-incremental and can take hours on complex configs
- **−** Training is eight separate scripts run by hand, with no packaged workflow
- **−** No Docker image and no tagged releases

<sub>Needs Binance API, Yahoo Finance, Telegram, TA-Lib, tsfresh · [Repo](https://github.com/asavinov/intelligent-trading-bot) · [▶️ Demo ↗](https://t.me/intelligent_trading_signals) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/intelligent-trading-bot/)</sub>

<a name="deepgemm"></a>
### #&#8288;190 [deepgemm](https://github.com/deepseek-ai/deepgemm) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (71) · Freshness: active (81) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · MIT · Oct 2026</sub>

**CUDA tensor core kernels for FP8, FP4 and BF16 GEMMs and fused MoE.**

DeepGEMM is a CUDA kernel library for NVIDIA SM90 and SM100 GPUs, called from Python through PyTorch. It provides dense and grouped FP8/FP4/BF16 GEMMs, MQA logits kernels for the DeepSeek V3.2 indexer, and a fused Mega MoE kernel that overlaps expert-parallel communication with compute. Kernels are compiled at runtime by its own JIT, so installation needs no CUDA compilation.

- **+** Covers dense, contiguous and masked grouped GEMMs, MQA logits and fused Mega MoE in one library
- **+** Runtime JIT compilation, so install does not compile CUDA kernels
- **+** Small set of core kernels without heavy CUTLASS templates, readable for learning
- **+** MIT license; supports both SM90 and SM100 GPUs
- **−** Only NVIDIA SM90 or SM100 GPUs are supported
- **−** Needs CUDA Toolkit 12.9+, PyTorch 2.3+ and a C++20 compiler; Mega MoE needs PyTorch 2.9+
- **−** Caller must handle input transposition, FP8 casting and scaling-factor layout
- **−** SM90 supports only the NT memory layout

<sub>GPU required · Needs CUDA Toolkit 12.9+, PyTorch 2.3+, CUTLASS 4.0+, Python 3.8+ · Models: FP8, FP4, BF16, DeepSeek V3.2 MQA indexer · [Repo](https://github.com/deepseek-ai/deepgemm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepgemm/)</sub>

<a name="coremltools"></a>
### #&#8288;191 [coremltools](https://github.com/apple/coremltools) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (55) · Freshness: active (83) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.5k · BSD-3-Clause · Sep 2026</sub>

**Python converter from TensorFlow, PyTorch and scikit-learn models to Core ML.**

coremltools is Apple's Python package for converting trained models from TensorFlow 1.x/2.x, PyTorch, scikit-learn, XGBoost and LibSVM into the Core ML format. It can also read, write and optimize Core ML models, and on macOS it can run predictions to verify a conversion. The converted models are meant to be integrated into apps through Xcode.

- **+** Maintained by Apple, the owner of the Core ML format
- **+** Converts TensorFlow 1.x/2.x, PyTorch, scikit-learn, XGBoost and LibSVM models
- **+** Installs with a single pip command
- **+** Can check converted models against Core ML predictions on macOS
- **−** Output targets only Core ML, so deployment is limited to Apple platforms
- **−** Prediction-based verification requires macOS
- **−** Last stable release is 2025-11-10; newer builds are dev releases only

<sub>Needs Python, Xcode (for app integration) · Models: TensorFlow 1.x, TensorFlow 2.x, PyTorch, scikit-learn, XGBoost · [Repo](https://github.com/apple/coremltools) · [📖 Docs ↗](https://apple.github.io/coremltools/docs-guides/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/coremltools/)</sub>

<a name="object-detection-metrics"></a>
### #&#8288;192 [object-detection-metrics](https://github.com/rafaelpadilla/object-detection-metrics) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · MIT · Oct 2026</sub>

**Python functions for computing object detection metrics like PASCAL VOC AP.**

Reference implementation of object detection evaluation metrics: IOU, precision x recall curves, and average precision with all-point or 11-point interpolation. It takes ground truth and detected bounding boxes in a simple format, without conversion to XML or JSON. The README says results match the official competition implementations, and that a newer tool (review_object_detection_metrics) supersedes this one.

- **+** Implements PASCAL VOC AP with both all-point and 11-point interpolation
- **+** Simple box input; no XML or JSON conversion of detections required
- **+** README explains the metrics with a worked numeric example
- **+** Backed by a peer-reviewed paper (Electronics, 2021) for citation
- **−** Superseded by review_object_detection_metrics, per the README's own notice
- **−** Fewer metrics than the newer tool, which adds all COCO metrics
- **−** No UI and no STT-AP video metric; both are only in the newer tool
- **−** No tagged releases

<sub>no GPU · [Repo](https://github.com/rafaelpadilla/object-detection-metrics) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/object-detection-metrics/)</sub>

<a name="highwayenv"></a>
### #&#8288;193 [highwayenv](https://github.com/farama-foundation/highwayenv) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (35) · Freshness: active (100) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Nov 2026</sub>

**Gymnasium environments for autonomous driving and tactical decision-making.**

HighwayEnv is a Python collection of Gymnasium-compatible simulation environments for driving tasks. It covers 10 scenario families (highway, merge, roundabout, parking, intersection, racetrack, lane-keeping, two-way, exit, u-turn), several with fast, continuous-control, multi-agent or other variants. It is used to train and evaluate reinforcement learning and planning agents, with examples for Stable Baselines3, DQN, DDPG, Value Iteration and MCTS.

- **+** Standard Gymnasium API: gym.make("highway-v0", config=...) works with existing RL libraries
- **+** 10 scenario families with per-environment configuration options documented
- **+** Installs with pip or uv; no simulator binary or Docker needed
- **+** Documented agent examples and Colab notebooks for Stable Baselines3 and planners
- **−** Simplified 2D kinematic simulation, not a high-fidelity driving simulator
- **−** Windows support is secondary; Linux and macOS are the main targets
- **−** Provides environments only; agents and training code live in other libraries
- **−** Single-maintainer lineage; roadmap tracked in a GitHub issue

<sub>Needs gymnasium · [Repo](https://github.com/farama-foundation/highwayenv) · [📖 Docs ↗](https://highway-env.farama.org/quickstart/) · [🌐 Site ↗](https://highway-env.farama.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/highwayenv/)</sub>

<a name="retinexformer"></a>
### #&#8288;194 [retinexformer](https://github.com/caiyuanhao1998/retinexformer) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Nov 2026</sub>

**PyTorch toolbox for low-light image enhancement with a Retinex-based transformer.**

Retinexformer is the ICCV 2023 code base for a transformer that brightens low-light images. It has training and testing scripts for over 15 benchmarks, including LOL, SID, SMID, SDSD and MIT Adobe FiveK. It adds DDP and mixed-precision training, self-ensemble testing, and a split-and-test mode for images up to 4000x6000. Weights are on Hugging Face and a Gradio demo runs on Spaces.

- **+** Covers over 15 benchmarks, with pretrained weights, training logs and result downloads
- **+** Adaptive split-and-test inference handles images up to 4000x6000
- **+** Supports DDP, mixed-precision training and self-ensemble testing
- **+** Second place in NTIRE 2024 low-light challenge; later winners built on it
- **−** Research code: setup needs conda, pinned PyTorch 1.11 or 2.5.1, and a BasicSR install
- **−** Datasets are mostly on Baidu Disk and Google Drive, with manual unzip steps
- **−** No tagged releases and no packaged library or API
- **−** Scope is low-light enhancement only, not general image generation

<sub>Needs PyTorch 1.11 or 2.5.1, BasicSR, Conda, Gradio · Models: Retinexformer, MST++, PyTorch checkpoints · [Repo](https://github.com/caiyuanhao1998/retinexformer) · [▶️ Demo ↗](https://huggingface.co/spaces/CaiYuanhao/Retinexformer) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/retinexformer/)</sub>

<a name="gluonts"></a>
### #&#8288;195 [gluonts](https://github.com/awslabs/gluonts) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · Apache-2.0 · Oct 2026</sub>

**Python library for probabilistic time series forecasting with PyTorch models.**

GluonTS is a Python package for training and evaluating probabilistic time series models, focused on deep learning and built on PyTorch. The README example trains a DeepAR estimator on the AirPassengers dataset and plots forecasts with 50% and 90% prediction intervals. It includes a pandas dataset wrapper and train/test splitting utilities.

- **+** Forecasts are probability distributions with prediction intervals, not only point estimates
- **+** Provides PandasDataset and a split utility for backtest windows
- **+** Installs from PyPI with a torch extra; supports Python 3.10 to 3.14
- **+** Stable and dev docs plus several conference tutorials with videos
- **−** Library only: requires writing Python, no UI or server component
- **−** README shows only DeepAR; the full model list is in the docs
- **−** Pretrained zero-shot forecasting lives in a separate project, Chronos
- **−** Torch models need the optional gluonts[torch] extra

<sub>Needs PyTorch, pandas, matplotlib · Models: DeepAR, PyTorch · [Repo](https://github.com/awslabs/gluonts) · [📖 Docs ↗](https://ts.gluon.ai/stable/) · [🌐 Site ↗](https://ts.gluon.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gluonts/)</sub>

<a name="hdbscan"></a>
### #&#8288;196 [hdbscan](https://github.com/scikit-learn-contrib/hdbscan) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: known (33) · Freshness: active (100) · Maintenance: patchy (39) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · BSD-3-Clause · Nov 2026</sub>

**Python HDBSCAN clustering library with a scikit-learn API.**

Implements HDBSCAN density-based clustering in Python as a scikit-learn-compatible estimator (fit_predict). It accepts arrays, dataframes, sparse matrices or precomputed distance matrices. It also provides GLOSH outlier scores, soft cluster membership, robust single linkage and a BranchDetector for branching cluster shapes. Hierarchies can be plotted or exported to Pandas and NetworkX.

- **+** Drop-in sklearn estimator API; main parameter is min_cluster_size
- **+** Finds clusters of varying density, unlike DBSCAN
- **+** Includes GLOSH outlier scores, soft clustering and robust single linkage
- **+** Joblib caching makes re-clustering with new parameters cheap
- **−** Classical clustering library, not an LLM or generative AI tool
- **−** README still references Travis CI, nose and Python 2 support
- **−** Performance claims rest on external notebooks, including v0.7 benchmarks

<sub>no GPU · Needs numpy, scipy, scikit-learn, cython · [Repo](https://github.com/scikit-learn-contrib/hdbscan) · [📖 Docs ↗](http://hdbscan.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hdbscan/)</sub>

<a name="audio"></a>
### #&#8288;197 [audio](https://github.com/pytorch/audio) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (30) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · BSD-2-Clause · Nov 2026</sub>

**PyTorch library for audio loading, transforms, and datasets for ML.**

torchaudio provides audio building blocks on top of PyTorch: dataset loaders, transforms such as MelSpectrogram, MFCC, and Resample, forced alignment, and Kaldi-compatible spectrogram, fbank, and mfcc functions. All computation uses PyTorch ops, so it runs on GPU and supports autograd. The project is in maintenance phase, and several features deprecated in 2.8 were removed in 2.9.

- **+** Transforms are PyTorch ops, so they run on GPU and are differentiable
- **+** Kaldi-compliant spectrogram, fbank, and mfcc functions for matching Kaldi features
- **+** Installs with pip; 2.11 does not pin a specific torch version
- **+** Includes dataset loaders and forced_align for speech pipelines
- **−** In maintenance phase; features deprecated in 2.8 were removed in 2.9
- **−** Scoped to ML audio processing, not general signal processing
- **−** Some pre-trained models carry separate licenses, e.g. SquimSubjective is CC-BY-NC 4.0
- **−** Library only; no ready-to-use app, server, or UI

<sub>GPU optional · Needs torch · Models: PyTorch · [Repo](https://github.com/pytorch/audio) · [📖 Docs ↗](https://pytorch.org/audio/main/) · [🌐 Site ↗](https://pytorch.org/audio/main/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/audio/)</sub>

<a name="mirage"></a>
### #&#8288;198 [mirage-project/mirage](https://github.com/mirage-project/mirage) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: patchy (39) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · Apache-2.0 · Nov 2026</sub>

**Compiler that fuses LLM inference into a single persistent CUDA megakernel.**

Mirage Persistent Kernel (MPK) compiles a Hugging Face LLM's computation graph into one fused GPU kernel that handles compute and communication in a single launch. The README reports 1.2x to 6.7x lower inference latency and covers multi-GPU setups. You define the graph in Python with fused ops such as rmsnorm_linear_layer, and a Qwen3-8B demo script is included.

- **+** Fuses compute and inter-GPU communication into one kernel launch, cutting launch overhead
- **+** README reports 1.2x to 6.7x lower latency than baseline inference
- **+** Python API with a runnable Qwen3-8B demo and a task timeline profiler
- **+** Backed by OSDI papers; Apache-2.0 licensed
- **−** Source install only; pre-built wheels were still pending in the README
- **−** Graph is defined by hand with fused ops; only a Qwen3 demo is shown
- **−** Worker and scheduler counts must match the physical SM count
- **−** No HTTP API or serving layer described; it is a compiler and runtime

<sub>GPU required · Docker · Needs PyTorch, CUDA, Triton, FlashInfer, NVSHMEM, MPI · Models: Hugging Face models, Qwen3-8B · [Repo](https://github.com/mirage-project/mirage) · [🌐 Site ↗](https://zhihaojia.medium.com/compiling-llms-into-a-megakernel-a-path-to-low-latency-inference-cf7840913c17) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mirage/)</sub>

<a name="xuance"></a>
### #&#8288;199 [xuance](https://github.com/agi-brain/xuance) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · MIT · Nov 2026</sub>

**Deep reinforcement learning library with single- and multi-agent algorithms.**

XuanCe is a Python library of deep reinforcement learning implementations covering DQN variants, policy-gradient and actor-critic methods, model-based (DreamerV2/V3), contrastive, and multi-agent algorithms such as QMIX, MAPPO and MADDPG. It runs on PyTorch, TensorFlow2 or MindSpore and works with Gymnasium and PettingZoo environments, including Atari, MuJoCo, SMAC and MPE. It is installed with pip and documented at xuance.org.

- **+** Covers DRL, model-based, contrastive and MARL algorithms in one codebase
- **+** Supports PyTorch, TensorFlow2 and MindSpore backends
- **+** Works with many environments: Atari, MuJoCo, Box2D, MiniGrid, SMAC, MPE, drones
- **+** Supports parallel environments, multi-GPU training, and TensorBoard or wandb logging
- **−** Reinforcement learning only; not for LLM or generative model work
- **−** Each environment family needs its own extra packages
- **−** Recommended Python 3.8 is old and may conflict with newer tooling

<sub>GPU optional · Needs PyTorch, TensorFlow, MindSpore, Gymnasium, PettingZoo · [Repo](https://github.com/agi-brain/xuance) · [📖 Docs ↗](https://xuance.org) · [🌐 Site ↗](https://xuance.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xuance/)</sub>

<a name="paddlex"></a>
### #&#8288;200 [paddlex](https://github.com/paddlepaddle/paddlex) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Nov 2026</sub>

**Low-code toolkit for training and deploying PaddlePaddle OCR and vision models.**

PaddleX 3.0 wraps 200+ PaddlePaddle models into 33 task pipelines (OCR, document parsing, detection, segmentation, time series, speech) callable through a Python API or a unified command line. It covers training, inference, high-performance inference, serving and on-device deployment. Hardware support extends beyond NVIDIA GPUs to Kunlunxin, Ascend, Cambricon and Hygon chips.

- **+** 33 prebuilt pipelines over 200+ models, including PP-OCRv5 and PP-StructureV3 document parsing
- **+** Same toolkit covers training, high-performance inference, serving and on-device deployment
- **+** Runs on CPU, NVIDIA GPU, Kunlunxin, Ascend, Cambricon and Hygon hardware
- **+** Per-pipeline benchmarks measure end-to-end and per-module inference time
- **−** Tied to the PaddlePaddle framework (3.0.0 or newer); not usable with PyTorch models
- **−** Main README is in Chinese; the English version is a separate file
- **−** Many pipelines marked unfinished for on-device deployment or secondary development
- **−** Online demos and the graphical pipeline builder run on Baidu AI Studio, not locally

<sub>GPU optional · Docker · Needs PaddlePaddle >= 3.0.0, Python 3.8-3.13 · Models: PaddlePaddle models, ONNX (via Paddle2ONNX), PP-OCRv5, PP-StructureV3, PaddleOCR-VL · [Repo](https://github.com/paddlepaddle/paddlex) · [▶️ Demo ↗](https://aistudio.baidu.com/application/center/app?tag=%E5%85%A8%E9%83%A8&flod=86503) · [📖 Docs ↗](https://paddlepaddle.github.io/PaddleX/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddlex/)</sub>

<a name="kaolin"></a>
### #&#8288;201 [kaolin](https://github.com/nvidiagameworks/kaolin) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: popular (53) · Freshness: recent (76) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

**PyTorch library for 3D deep learning: meshes, splats, rendering, physics.**

Kaolin is NVIDIA's PyTorch library of GPU-optimized modules for 3D deep learning research. It covers differentiable rendering (DIB-R, nvdiffrast, easy_render PBR), 3D Gaussian splat containers with PLY/USD I/O, Structured Point Clouds (GPU octrees), representation conversions, quaternion math, and Warp-based Simplicits physics for meshes, splats and point clouds.

- **+** Covers rendering, conversions, physics, and USD I/O in one PyTorch API
- **+** Many tutorial notebooks plus API docs on readthedocs
- **+** Apache-2.0 including FlexiCubes, now relicensed from non-commercial
- **+** Prebuilt pip wheels for specific torch/CUDA combinations
- **−** Wheels are published per torch/CUDA pair; other combinations need a source build
- **−** Web client-server framework only on a prerelease branch, not merged to master
- **−** Newton coupling is marked experimental
- **−** Last release 0.18.0 is from 2025-08; recent features exist only on master

<sub>GPU required · Needs PyTorch, CUDA, NVIDIA Warp · Models: PLY, USD, OBJ, GLTF · [Repo](https://github.com/nvidiagameworks/kaolin) · [📖 Docs ↗](https://kaolin.readthedocs.io/en/latest/) · [🌐 Site ↗](https://developer.nvidia.com/kaolin) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kaolin/)</sub>

<a name="vlmevalkit"></a>
### #&#8288;202 [vlmevalkit](https://github.com/open-compass/vlmevalkit) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (48) · Freshness: recent (70) · Maintenance: patchy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · Apache-2.0 · Nov 2026</sub>

**Evaluation toolkit that runs vision-language models on 70+ image and video benchmarks.**

VLMEvalKit (Python package vlmeval) runs large vision-language models through benchmark suites with one command, handling dataset download, preprocessing, inference and scoring. It uses generation-based evaluation and reports both exact-match and LLM-based answer extraction results. It covers 200+ models, including commercial APIs, and backs the OpenCompass multimodal leaderboards.

- **+** Covers 70+ image and video benchmarks and 200+ models behind one command
- **+** Adding a custom model needs only a single generate_inner() function
- **+** Multi-node inference via LMDeploy or vLLM for large or thinking models
- **+** Reports both exact-match and LLM-extracted scores for comparison
- **−** Models need different pinned transformers versions, from 4.33.0 to 5.2+, so several environments are needed
- **−** Scores may not match original benchmark papers because prompts are shared across models
- **−** Last tagged release is March 2025, while the main branch keeps changing
- **−** Full model and benchmark lists live in an external Feishu page, not the repo

<sub>GPU optional · Needs transformers, torchvision, LMDeploy (optional), vLLM (optional), flash-attn (some models) · Models: Qwen2.5-VL, InternVL3, LLaVA, Gemini-2.5-Pro, Llama 4 · [Repo](https://github.com/open-compass/vlmevalkit) · [📖 Docs ↗](https://github.com/open-compass/VLMEvalKit/blob/main/docs/en/Quickstart.md) · [🌐 Site ↗](https://rank.opencompass.org.cn/leaderboard-multimodal) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vlmevalkit/)</sub>

<a name="segment-geospatial"></a>
### #&#8288;203 [segment-geospatial](https://github.com/opengeos/segment-geospatial) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (45) · Freshness: active (100) · Maintenance: weak (21) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · MIT · Nov 2026</sub>

**Python package for segmenting satellite imagery and GeoTIFFs with SAM models.**

SamGeo wraps Meta's Segment Anything Model (SAM, SAM 2, SAM 3), HQ-SAM and Fast SAM for geospatial rasters. It downloads TMS map tiles to GeoTIFF, segments with point, box or text prompts (text via Grounding DINO), and exports masks as GeoPackage, Shapefile or GeoJSON. It also offers an optional FastAPI REST server and a separate QGIS plugin.

- **+** Exports results to GeoPackage, Shapefile and GeoJSON for use in GIS tools
- **+** Optional pip extras (samgeo2, samgeo3, hq, fast, text, api) keep installs smaller
- **+** Supports text prompts, box prompts, interactive markers and timeseries imagery
- **+** Also available as a QGIS plugin and an ArcGIS toolbox
- **−** Large rasters need a GPU; README recommends at least 8 GB of GPU memory
- **−** SAM 3 install on Windows needs manual steps, including triton-windows
- **−** Interactive mapping and examples assume Jupyter; no standalone web UI
- **−** Bulk tile downloads may require permission from the basemap provider

<sub>GPU optional · Docker · Needs PyTorch, Grounding DINO (text prompts), FastAPI and Uvicorn (REST API), Jupyter (examples) · Models: SAM, SAM 2, SAM 3, HQ-SAM, Fast SAM · [Repo](https://github.com/opengeos/segment-geospatial) · [📖 Docs ↗](https://samgeo.gishub.org) · [🌐 Site ↗](https://samgeo.gishub.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/segment-geospatial/)</sub>

<a name="gigatoken"></a>
### #&#8288;204 [gigatoken](https://github.com/marcelroed/gigatoken) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (44) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · MIT · Nov 2026</sub>

**Rust BPE tokenizer for Python, with HuggingFace and tiktoken compatibility.**

Gigatoken is a Rust tokenizer library, installed with pip, that encodes text files using SIMD pretokenization and a pretoken cache across all CPU cores. It accepts HuggingFace model names and can wrap existing HF tokenizers or tiktoken encoders. The README reports 24.5 GB/s on GPT-2 on a 144-core EPYC, against 24.8 MB/s for HF tokenizers.

- **+** Compatibility mode wraps HF tokenizers or tiktoken with a one-line change
- **+** Built-in bench command with --validate checks output against HF on your tokenizer
- **+** Covers many BPE tokenizers: Llama 3/4, Qwen 2/3/3.5, GPT-OSS, DeepSeek, GLM
- **+** Runs on modern x86 and ARM CPUs
- **−** Compatibility mode is slower than the native API that gives the headline speedup
- **−** SentencePiece models (Gemma, Mistral, Llama 2) are only about 7-22x faster than HF
- **−** WordPiece is not supported and file sinks are not implemented
- **−** Windows is lightly tested (WSL advised); CJK-heavy data is much slower

<sub>no GPU · Needs Python, pip · Models: GPT-2, Llama 3/4, Qwen 2/3/3.5, GPT-OSS, DeepSeek V3/R1 · [Repo](https://github.com/marcelroed/gigatoken) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gigatoken/)</sub>

<a name="thunderkittens"></a>
### #&#8288;205 [thunderkittens](https://github.com/hazyresearch/thunderkittens) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (41) · Freshness: active (100) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · MIT · Sep 2026</sub>

**Header-only CUDA library of tile primitives for writing fast GPU kernels.**

ThunderKittens is a header-only C++/CUDA library that provides register and shared-memory tile and vector types, plus operations on them, for writing deep learning kernels. It wraps tensor core calls (WGMMA on H100, TCGEN05 on B200), TMA loads and stores, and NVLink transfers. The repo includes pre-implemented kernels (GEMM, attention) with per-kernel Makefiles and PyTorch bindings, and demos for LLM training and inference.

- **+** Header-only: clone and include kittens.cuh, no install step
- **+** Covers Hopper and Blackwell features: WGMMA, TCGEN05, TMA, MXFP8, NVFP4
- **+** Compile-time layout checks catch invalid tile operations early
- **+** Example H100 GEMM in under 100 lines reaches about 855 TFLOPs (86% of peak)
- **−** NVIDIA only; AMD GPUs need the separate HipKittens project
- **−** Ampere no longer actively supported
- **−** Requires CUDA 12.8+ and C++20; older gcc causes compile errors
- **−** No top-level Python package since 2.0; each kernel is built separately with make

<sub>GPU required · Needs CUDA 12.8+, C++20 compiler (gcc 11+), PyTorch 2.8+ and PyBind11 for bundled kernels · [Repo](https://github.com/hazyresearch/thunderkittens) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/thunderkittens/)</sub>

<a name="equinox"></a>
### #&#8288;206 [equinox](https://github.com/patrick-kidger/equinox) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (31) · Freshness: active (98) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · Apache-2.0 · Oct 2026</sub>

**JAX library for neural networks as PyTrees, with filtered transformations.**

Equinox adds PyTorch-like model definition to JAX through eqx.Module, which registers a class as a PyTree so models pass directly through jit, grad and vmap. It also provides filtered transformations, PyTree manipulation routines and runtime errors. It is a library rather than a framework, so code stays compatible with other JAX tools.

- **+** Models are plain PyTrees, so they cross jit/grad/vmap boundaries without wrappers
- **+** Filtered transformations and PyTree utilities go beyond what core JAX offers
- **+** Runtime errors are supported, which core JAX lacks
- **+** Installs with pip; docs and an MNIST CNN example are provided
- **−** Requires JAX knowledge; newcomers are pointed to an example, not a full tutorial
- **−** No built-in optimisers or checkpointing; the README points to Optax and Orbax
- **−** Requires Python 3.10 or newer
- **−** JAX-only, so models do not carry over to PyTorch code

<sub>GPU optional · Needs JAX, Python 3.10+ · [Repo](https://github.com/patrick-kidger/equinox) · [📖 Docs ↗](https://docs.kidger.site/equinox) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/equinox/)</sub>

<a name="torchinfo"></a>
### #&#8288;207 [torchinfo](https://github.com/tyleryep/torchinfo) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (29) · Freshness: recent (70) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Nov 2026</sub>

**Keras-style model.summary() for PyTorch modules, with shapes, params and mult-adds.**

torchinfo prints a layer-by-layer table for a PyTorch nn.Module: input and output shapes, parameter counts, kernel size, trainable flag and mult-adds, plus estimated memory size. It runs a forward pass from either an input shape or real input data, and returns a ModelStatistics object. It is a rewrite of torchsummary and torchsummaryX, installable from PyPI or conda-forge.

- **+** Takes an input shape or real input data, including dicts and multiple inputs with different dtypes
- **+** Configurable columns, nesting depth and row settings; handles RNNs, LSTMs, Sequential and ModuleList
- **+** Returns a ModelStatistics object, so summary data can be used as a string or in code
- **+** Works in Jupyter and Colab; installs with pip or conda
- **−** Needs a forward pass to show shapes and mult-adds; without input only layer names and params appear
- **−** Mixed train/eval layers can alter batchnorm or dropout statistics during the summary
- **−** cache_forward_pass does not detect model or input changes and can give stale summaries
- **−** Last release was 2023-05-14; older versions get no backported fixes

<sub>GPU optional · Needs PyTorch · Models: PyTorch nn.Module · [Repo](https://github.com/tyleryep/torchinfo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/torchinfo/)</sub>

<a name="quantum"></a>
### #&#8288;208 [quantum](https://github.com/tensorflow/quantum) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (18) · Freshness: active (92) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Nov 2026</sub>

**Python library for hybrid quantum-classical ML on TensorFlow and Cirq.**

TensorFlow Quantum lets you define quantum circuits in Cirq and train them inside Keras models, with circuit operations implemented as C++ TensorFlow Ops. It simulates circuits through qsim and supports gradient methods including parameter shift and adjoint. It is aimed at quantum machine learning research that needs fast simulation of many moderately sized circuits.

- **+** Quantum ops are C++ TensorFlow Ops, so they sit in the normal TF compute graph
- **+** Keras abstractions for quantum ML layers and models
- **+** Several gradient methods, including parameter shift and adjoint, plus an extensible differentiation system
- **+** Official tutorials as notebooks, plus API docs on tensorflow.org
- **−** Built and tested on Linux only, per the compatibility notes
- **−** Pinned to Python 3.10-3.12, TensorFlow 2.19.1, TF-Keras 2.19.0, NumPy 2.0 and Cirq 1.5.0
- **−** Not an officially supported Google product
- **−** Narrow use case: quantum ML research, not general LLM or deep learning work

<sub>Needs TensorFlow 2.19.1, TF-Keras 2.19.0, Cirq 1.5.0, qsim, NumPy 2.0 · Models: Cirq quantum circuits, Keras quantum ML models · [Repo](https://github.com/tensorflow/quantum) · [📖 Docs ↗](https://www.tensorflow.org/quantum/overview) · [🌐 Site ↗](https://www.tensorflow.org/quantum) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/quantum/)</sub>

<a name="roboverse"></a>
### #&#8288;209 [roboverse](https://github.com/roboverseorg/roboverse) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: patchy (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · Apache-2.0 · Sep 2026</sub>

**Robot simulation platform with one API across simulators, plus tasks and training code.**

RoboVerse pairs MetaSim, a simulator abstraction layer, with a content pack of tasks, robots and scenes, plus RL, imitation learning and VLA training code. The same scenario config can target backends such as Isaac Lab, Isaac Gym, MuJoCo, SAPIEN, PyBullet and Genesis. It also integrates data and benchmarks like LIBERO, ManiSkill, RLBench and robosuite.

- **+** One scenario config spans many simulators, including MuJoCo, Isaac Lab, SAPIEN, PyBullet and Genesis
- **+** Bundles RL, imitation learning and VLA training and evaluation code with the tasks
- **+** Integrates existing benchmarks: LIBERO, ManiSkill, robosuite, RoboTwin, RLBench and others
- **+** Numbered tutorial chain in examples/ and a Sphinx documentation site
- **−** README says the codebase is still evolving, so APIs may change
- **−** No tagged release; install is from a git clone with pip -e
- **−** Each simulator backend needs its own setup, deferred to external docs
- **−** Vendored third-party code under mixed licenses, tracked in THIRD_PARTY_NOTICES.md

<sub>Needs MuJoCo, Isaac Lab, Isaac Gym, SAPIEN, PyBullet, Genesis, cuRobo · [Repo](https://github.com/roboverseorg/roboverse) · [📖 Docs ↗](https://roboverse.wiki) · [🌐 Site ↗](https://roboverseorg.github.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/roboverse/)</sub>

<a name="airsim"></a>
### #&#8288;210 [airsim](https://github.com/microsoft/airsim) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: widely used (85) · Freshness: recent (70) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · custom license · Sep 2026</sub>

**Unreal Engine drone and car simulator for autonomous vehicle research.**

AirSim is an Unreal Engine plugin, with an experimental Unity version, that simulates drones and cars. It supports software-in-the-loop with PX4 and ArduPilot, hardware-in-the-loop with PX4, and an RPC API for C++, Python, C# and Java to pull images and state and to control vehicles. It is aimed at deep learning, computer vision and reinforcement learning work.

- **+** Integrates with PX4 and ArduPilot for software-in-the-loop, plus PX4 hardware-in-the-loop
- **+** RPC API in C++, Python, C# and Java; client library can run on a companion computer
- **+** Computer Vision mode returns depth, disparity, normals and segmentation without vehicle physics
- **+** Built-in recording of pose and images, plus weather controls
- **−** Last release is 2022-07-18; the README points to a separate Project AirSim
- **−** Requires Unreal Engine; the Unity release is described as experimental
- **−** README lists no prebuilt binaries for macOS, only a build guide

<sub>Needs Unreal Engine, Unity (experimental), PX4, ArduPilot · [Repo](https://github.com/microsoft/airsim) · [▶️ Demo ↗](https://youtu.be/-WfTr1-OBGQ) · [📖 Docs ↗](https://microsoft.github.io/AirSim/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/airsim/)</sub>

<a name="dm-haiku"></a>
### #&#8288;211 [dm-haiku](https://github.com/google-deepmind/dm-haiku) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (35) · Freshness: active (100) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Oct 2026</sub>

**Neural network library for JAX with Sonnet-style object-oriented modules.**

Haiku is a Python neural network library for JAX from Google DeepMind, written by some of the Sonnet authors. It provides `hk.Module` for objects that hold parameters and `hk.transform` to turn them into pure `init`/`apply` functions usable with `jax.jit`, `jax.grad` and `jax.pmap`. The project is in maintenance mode: DeepMind recommends Flax for new projects, and Haiku gets only bug fixes and JAX compatibility updates.

- **+** API mirrors Sonnet 2, easing moves from TensorFlow/Sonnet to JAX
- **+** Small scope: manages params and state, no custom optimizers or checkpoint formats
- **+** `hk.next_rng_key()` derives unique RNG keys deterministically from one initial key
- **+** Transformed functions work with jax.pmap; ResNet-50 ImageNet example included
- **−** Maintenance mode: no new features, and PRs adding features are not accepted
- **−** DeepMind recommends Flax for new projects; Flax has a larger team and community
- **−** `hk.next_rng_key()` is impure and needs Haiku wrappers inside JAX transforms
- **−** JAX is not a pip dependency; install it separately to match your CUDA version

<sub>GPU optional · Needs JAX · [Repo](https://github.com/google-deepmind/dm-haiku) · [📖 Docs ↗](https://dm-haiku.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dm-haiku/)</sub>

<a name="tensorflow-onnx"></a>
### #&#8288;212 [tensorflow-onnx](https://github.com/onnx/tensorflow-onnx) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (24) · Freshness: active (93) · Maintenance: patchy (47) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · Apache-2.0 · Nov 2026</sub>

**Converts TensorFlow, Keras, TFLite and tfjs models to ONNX.**

tf2onnx converts TensorFlow 2.x models (saved model, checkpoint, graphdef), Keras, TFLite and experimental tensorflow.js models to ONNX. It runs as `python -m tf2onnx.convert` or through a Python API (from_keras, from_function, from_graph_def, from_tflite). Default output opset is 15; opsets 14-18 are tested. The README says the project is looking for a new maintainer.

- **+** Handles saved model, checkpoint, graphdef, Keras, TFLite and tfjs inputs from one CLI
- **+** Python API with custom op handlers, graph rewriters and shape overrides
- **+** Large-model mode writes external tensor storage for models over 2 GB
- **+** Includes a pretrained-model test runner comparing TensorFlow and ONNX Runtime outputs
- **−** README asks for a new maintainer, which signals uncertain upkeep
- **−** Tested only on TensorFlow 2.13-2.15 and Python 3.10-3.12
- **−** tensorflow.js and quantized TFLite dequantize support are experimental
- **−** TensorFlow has more ops than ONNX, so some models fail to convert

<sub>no GPU · Needs tensorflow, onnx, onnxruntime (optional, for testing) · Models: TensorFlow SavedModel, TensorFlow checkpoint, TensorFlow graphdef, Keras, TFLite · [Repo](https://github.com/onnx/tensorflow-onnx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorflow-onnx/)</sub>

<a name="chemprop"></a>
### #&#8288;213 [chemprop](https://github.com/chemprop/chemprop) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: patchy (39) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · custom license · Nov 2026</sub>

**Message passing neural networks for molecular property prediction.**

Chemprop is a Python package that trains message passing neural networks to predict properties of molecules and, through condensed graph of reaction representations, of reactions. Version 2 is a ground-up rewrite with a CLI, tutorial notebooks and a v1-to-v2 transition guide. It has been used in published antibiotic discovery work and in the ADMET-AI platform.

- **+** Used in peer-reviewed antibiotic discovery work (Cell 2020, Nature 2023)
- **+** Supports both molecule and reaction property prediction
- **+** Tutorial notebooks in examples/ and hosted Read the Docs documentation
- **+** Published on PyPI and conda-forge
- **−** v1 is discontinued; v1 bug reports are only tagged v1-wontfix
- **−** Some v1 CLI arguments are not yet implemented in v2
- **−** Interpretation is only available as an example notebook in v2
- **−** Edge update uses preactivation hidden states, unlike the cited papers

<sub>Docker · Models: message passing neural networks, molecules, reactions (condensed graph of reaction) · [Repo](https://github.com/chemprop/chemprop) · [📖 Docs ↗](https://chemprop.readthedocs.io/en/main/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chemprop/)</sub>

<a name="tsfresh"></a>
### #&#8288;214 [tsfresh](https://github.com/blue-yonder/tsfresh) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (72) · Freshness: active (87) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · MIT · Jul 2026</sub>

**Python library that extracts and filters features from time series.**

tsfresh is a Python package that computes hundreds of statistical, signal-processing and nonlinear-dynamics features from time series. It then filters them with a multiple hypothesis-testing procedure (FRESH) that controls the share of irrelevant features for a given regression or classification target. It works with pandas, numpy and scikit-learn, and can run locally or on a cluster.

- **+** Extracts hundreds of features per series, such as peak counts and time reversal symmetry
- **+** Built-in feature selection based on hypothesis tests with multiple-test control
- **+** Compatible with pandas, numpy and scikit-learn pipelines
- **+** Custom feature calculators can be added; documented on Read the Docs
- **−** Matrixprofile feature calculators require a Python 3.8 environment
- **−** Feature selection is described only against a regression or classification target
- **−** Classical feature engineering for tabular ML, not an LLM or generative AI tool
- **−** Cluster execution details are only in the external docs, not the README

<sub>no GPU · Docker · Needs pandas, numpy, scikit-learn · [Repo](https://github.com/blue-yonder/tsfresh) · [▶️ Demo ↗](https://mybinder.org/v2/gh/blue-yonder/tsfresh/main?filepath=notebooks) · [📖 Docs ↗](http://tsfresh.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tsfresh/)</sub>

<a name="hyperopt"></a>
### #&#8288;215 [hyperopt](https://github.com/hyperopt/hyperopt) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (66) · Freshness: active (89) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · custom license · Jul 2026</sub>

**Python library for hyperparameter search over conditional, mixed search spaces.**

Hyperopt is a Python library that minimizes an objective function over search spaces with real-valued, discrete and conditional dimensions. It implements random search, Tree of Parzen Estimators (TPE) and Adaptive TPE, and can parallelize evaluations through Apache Spark or MongoDB. The README states no RAM or GPU requirements.

- **+** Search spaces can nest conditional branches, as in the hp.choice example
- **+** Three algorithms: random search, TPE and Adaptive TPE
- **+** Parallel evaluation via SparkTrials or MongoTrials extras
- **+** Installs from PyPI with pip or uv; fmin API is small
- **−** Gaussian-process and regression-tree optimizers are designed for but not implemented
- **−** Documentation is split between a docs site and the GitHub wiki
- **−** Parallel runs need an external Spark cluster or MongoDB server
- **−** License is not identified automatically (NOASSERTION)

<sub>no GPU · Needs Apache Spark (optional), MongoDB (optional) · [Repo](https://github.com/hyperopt/hyperopt) · [📖 Docs ↗](http://hyperopt.github.io/hyperopt) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hyperopt/)</sub>

<a name="scenic"></a>
### #&#8288;216 [scenic](https://github.com/google-research/scenic) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: known (41) · Freshness: active (100) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · Apache-2.0 · Oct 2026</sub>

**JAX/Flax library for training attention-based vision models at scale.**

Scenic is a JAX and Flax codebase for research on attention-based computer vision models. It provides shared libraries for multi-host, multi-device training (input pipelines, losses, metrics, bipartite matchers, trainers) plus project directories with full training and evaluation loops. It includes reimplemented baselines such as ViT, DETR, CLIP, U-Net and SAM, and code for research projects like ViViT.

- **+** Includes reproduced baselines: ViT, DETR, Deformable DETR, CLIP, MAE, ResNet, U-Net, SAM
- **+** Input pipelines handle multi-host and multi-device splitting, caching and prefetching
- **+** Projects can be config-only or fork the trainers, losses and models entirely
- **+** Hosts code for published research such as ViViT, TokenLearner and OWL-ViT
- **−** JAX/Flax only, no PyTorch or TensorFlow support
- **−** Philosophy favors forking and copy-pasting, so code is duplicated across projects
- **−** Many projects need extra packages from their own requirements files
- **−** No tagged releases; install is from a git clone

<sub>Needs JAX, Flax, Python 3.9+ · Models: ViT, DETR, CLIP, ResNet, U-Net · [Repo](https://github.com/google-research/scenic) · [▶️ Demo ↗](https://colab.research.google.com/github/google-research/scenic/blob/main/scenic/common_lib/colabs/scenic_playground.ipynb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scenic/)</sub>

<a name="deepopen"></a>
### #&#8288;217 [deepopen](https://github.com/deepopen-com/deepopen) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: patchy (31) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Nov 2026</sub>

**Python SDK for non-generative text classification, scoring and routing decisions.**

DeepOpen is a Python SDK that answers predefined choice, score and true/false questions over text or JSON and returns labels, probabilities and confidence instead of generated text. It wraps the upstream Laya checkpoints (ModernBERT-large and mmBERT-base encoders) with a language-aware router, and adds Banking77 and CLINC150 training workflows. Reported test accuracy is 94.1234% on Banking77 and 98.0222% on in-scope CLINC150 (four-encoder ensemble).

- **+** Returns constrained outputs (choice, score, noul) with probabilities, not free-form text
- **+** Router loads English, multilingual or typed-decisions checkpoints; cache size and preload are configurable
- **+** Banking77 and CLINC150 results come with training guides, seeds and source manifests
- **+** Runs on CPU or CUDA; routing unit tests need no model downloads
- **−** Base checkpoints are overconfident and near chance on typed-decisions zero-shot; calibration needed
- **−** Reported moderation accuracy is 0.530 and ordinal scoring is described as weak
- **−** Benchmark guides are in Chinese; CLINC150 score excludes out-of-scope detection
- **−** No PyPI release; installed from Git, and SDK derives from upstream Laya

<sub>GPU optional · Needs PyTorch, Hugging Face Hub (checkpoint download) · Models: ModernBERT-large (Laya), mmBERT-base (Laya multilingual), DeBERTa-v3-large (CLINC150 ensemble) · [Repo](https://github.com/deepopen-com/deepopen) · [▶️ Demo ↗](https://c41-laya-evaluation.static.hf.space/index.html?version=ensemble-2#comparison) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepopen/)</sub>

<a name="torchmetrics"></a>
### #&#8288;218 [torchmetrics](https://github.com/lightning-ai/torchmetrics) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (23) · Freshness: active (93) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Nov 2026</sub>

**PyTorch metrics library with automatic accumulation and multi-device sync.**

TorchMetrics is a Python library of 100+ metric implementations for PyTorch, covering audio, classification, detection, retrieval, image, multimodal, nominal, regression, segmentation and text. Metrics are stateful modules that accumulate over batches and synchronize across devices in DDP, with functional versions as well. Custom metrics are written by subclassing Metric and implementing update and compute.

- **+** Module metrics accumulate over batches and sync across GPUs and nodes automatically
- **+** Both stateful module and stateless functional APIs for most metrics
- **+** Custom metrics need only add_state, update and compute on a Metric subclass
- **+** Built-in .plot method for most module metrics; works with plain PyTorch or Lightning
- **−** PyTorch only; no support for other tensor frameworks
- **−** Audio, image and text metrics need extra pip dependency groups
- **−** Plotting requires a separate optional install (torchmetrics[visual])
- **−** README notes the Lightning framework is Patent Pending, alongside Apache-2.0

<sub>GPU optional · Needs PyTorch · [Repo](https://github.com/lightning-ai/torchmetrics) · [📖 Docs ↗](https://lightning.ai/docs/torchmetrics/stable/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/torchmetrics/)</sub>

<a name="sonnet"></a>
### #&#8288;219 [sonnet](https://github.com/google-deepmind/sonnet) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: popular (73) · Freshness: recent (70) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10.0k · Apache-2.0 · Oct 2026</sub>

**Module-based neural network library on top of TensorFlow 2.**

Sonnet is a DeepMind library that provides a single abstraction, snt.Module, for building neural networks in TensorFlow 2. It ships predefined modules such as Linear, Conv2D, BatchNorm and nets.MLP, and deliberately includes no training framework. Serialization goes through TensorFlow checkpoints and SavedModel, and distributed training uses TensorFlow distribution strategies.

- **+** Small API centered on one concept, snt.Module, with parameters created on first call
- **+** Modules work with tf.train.Checkpoint and tf.saved_model without extra glue
- **+** Behaves identically under distribution strategies; gradient reduction is left to the user
- **+** Colab examples for MNIST MLP, GAN and multi-GPU CIFAR-10
- **−** Requires TensorFlow 2; no other backend is mentioned in the README
- **−** No built-in training loop, so users write their own optimizer and training code
- **−** Last release was 2024-01-02, despite recent commits
- **−** Distributed training needs manual gradient all-reduce or distribution-aware modules

<sub>GPU optional · Needs tensorflow, tensorflow-probability · Models: TensorFlow checkpoints, TensorFlow SavedModel, pickle · [Repo](https://github.com/google-deepmind/sonnet) · [📖 Docs ↗](https://sonnet.readthedocs.io/) · [🌐 Site ↗](https://sonnet.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sonnet/)</sub>

<a name="donkeycar"></a>
### #&#8288;220 [donkeycar](https://github.com/autorope/donkeycar) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (38) · Freshness: active (100) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · MIT · Nov 2026</sub>

**Python library for building and training self-driving RC cars.**

Donkeycar is a modular Python library for building small self-driving cars, aimed at hobbyists and students. A car is a pipeline of parts (camera, GPS, controller, motors, data store, autopilot) run in order on each vehicle-loop pass, configured mostly through myconfig.py. It supports deep-learning, GPS path-following and computer-vision autopilots, and ships a GUI and a simulator.

- **+** Deep-learning autopilots on TensorFlow, TensorFlow Lite or PyTorch, plus GPS and computer-vision autopilots
- **+** Includes a simulator, so you can train and test before building hardware
- **+** Parts pipeline lets you write custom parts and add them to templates
- **+** Broad hardware support: several camera types, lidar, game controllers, ESC/servo and differential drive
- **−** Raspberry Pi is the preferred target, and camera support needs system packages outside PyPI
- **−** Real use assumes building a physical RC car; hardware setup is outside this README
- **−** Separate install extras for Pi, Mac and PC, with different Python versions (3.13 on Pi, 3.12 elsewhere)
- **−** Narrow scope: small-scale RC driving, not a general robotics or ML framework

<sub>Docker · Needs uv, Raspberry Pi (preferred on-board computer), picamera2, libcamera · Models: TensorFlow, TensorFlow Lite, PyTorch · [Repo](https://github.com/autorope/donkeycar) · [📖 Docs ↗](http://docs.donkeycar.com) · [🌐 Site ↗](http://donkeycar.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/donkeycar/)</sub>

<a name="mlj-jl"></a>
### #&#8288;221 [mlj.jl](https://github.com/juliaai/mlj.jl) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · custom license · Oct 2026</sub>

**Julia toolbox with a common interface for tuning and evaluating ML models.**

MLJ is a Julia umbrella package that gives over 200 machine learning models, written in Julia and other languages, one common interface. It adds meta-algorithms for selecting, tuning, evaluating, composing and comparing those models. Components are distributed across separate packages in the JuliaAI ecosystem.

- **+** Single interface over 200+ models, including ones wrapped from non-Julia libraries
- **+** Built-in tuning, evaluation, composition and model comparison
- **+** Documented model interface for integrating new models (MLJModelInterface)
- **+** Stable and dev docs, plus a browsable model catalog
- **−** Julia only, so it does not fit teams working in Python
- **−** Umbrella package: functionality is spread across many separate packages
- **−** Aimed at classical ML; the README does not mention LLMs or deep learning
- **−** GitHub reports license as NOASSERTION, though the README badge says MIT

<sub>Needs Julia · Models: 200+ machine learning models in Julia and other languages · [Repo](https://github.com/juliaai/mlj.jl) · [📖 Docs ↗](https://JuliaAI.github.io/MLJ.jl/stable/) · [🌐 Site ↗](https://juliaml.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlj-jl/)</sub>

<a name="tsai"></a>
### #&#8288;222 [tsai](https://github.com/timeseriesai/tsai) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (58) · Freshness: active (80) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Jun 2026</sub>

**PyTorch and fastai library for time series classification and forecasting.**

tsai is a Python package built on PyTorch and fastai for training deep learning models on time series: classification, regression, forecasting and imputation. It bundles about 30 architectures (InceptionTime, TST, PatchTST, MiniRocket, TCN and others), dataset downloaders and tutorial notebooks. Models take a 3D array of samples x variables x sequence length and export to a pickled learner for inference.

- **+** Ships many time series architectures, including PatchTST, InceptionTime, TST and MiniRocket
- **+** Downloads 128 univariate and 30 multivariate classification datasets, plus regression and forecasting sets
- **+** Plus models auto-configure the output head to match the forecasting target shape
- **+** Tutorial notebooks, including a Colab intro to time series classification
- **−** Tied to the fastai training loop and API, which adds a learning curve
- **−** ROCKET models need sktime installed separately or via the extras install
- **−** Requires Python 3.10 or newer; conda channel is no longer updated
- **−** Library only: no serving layer, UI or deployment tooling

<sub>GPU optional · Compose · Needs PyTorch, fastai, Python 3.10+, sktime (optional), tsfresh (optional) · Models: PatchTST, InceptionTime, TST, TSiT, MiniRocket · [Repo](https://github.com/timeseriesai/tsai) · [📖 Docs ↗](https://timeseriesai.github.io/tsai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tsai/)</sub>

<a name="finrl-trading"></a>
### #&#8288;223 [finrl-trading](https://github.com/ai4finance-foundation/finrl-trading) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: known (42) · Freshness: active (95) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · Apache-2.0 · Sep 2026</sub>

**Weight-based quant trading framework: backtest and Alpaca execution.**

FinRL-X is a Python trading framework in which every strategy outputs a target portfolio weight vector. The same weights feed a bt-based backtest engine and Alpaca execution. It includes a data layer (Yahoo Finance, FMP, WRDS, SQLite cache), a Random Forest stock selector, PPO/SAC allocators and an adaptive multi-asset rotation strategy. It succeeds the original FinRL.

- **+** Single weight-vector interface lets selection, allocation, timing and risk modules be swapped independently
- **+** Same weights run through backtest and Alpaca paper/live execution, with multi-account support
- **+** Yahoo Finance works as a free default data source; FMP and WRDS are optional
- **+** deploy.sh runs data download, backtest and paper trading in one command
- **−** Live execution is limited to Alpaca; no other brokers listed
- **−** Reported results are the authors' own backtests plus a short paper-trading window
- **−** Manual backtest runs need daily CSVs under data/fmp_daily/ first
- **−** README states it is for educational and research use only

<sub>Docker + Compose · Needs Alpaca API, Yahoo Finance, FMP API (optional), WRDS (optional), SQLite · Models: Random Forest, PPO, SAC · [Repo](https://github.com/ai4finance-foundation/finrl-trading) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/finrl-trading/)</sub>

<a name="gpytorch"></a>
### #&#8288;224 [gpytorch](https://github.com/cornellius-gp/gpytorch) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: known (42) · Freshness: active (93) · Maintenance: weak (18) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · MIT · Oct 2026</sub>

**Gaussian process library built on PyTorch with GPU-accelerated inference.**

GPyTorch is a Python library for building Gaussian process models on PyTorch. Most inference uses numerical linear algebra such as preconditioned conjugate gradients, via the LinearOperator interface, instead of Cholesky decomposition. It includes implementations of SKI/KISS-GP, stochastic Lanczos expansions, LOVE, SKIP, stochastic variational GPs and deep kernel learning.

- **+** Matrix-multiplication-based inference makes better use of GPUs than Cholesky solvers
- **+** Implements SKI/KISS-GP, LOVE, SKIP, stochastic variational GPs and deep kernel learning
- **+** New scalable methods can be added by supplying a kernel matrix multiply via LinearOperator
- **+** Integrates with PyTorch models; optional KeOps and Pyro extras
- **−** Requires Python 3.10+, PyTorch 2.4.1+ and NumPy 2.0+
- **−** Library only: no UI, server or hosted service
- **−** Iterative solvers add approximation and tuning concerns versus exact Cholesky GPs
- **−** Focused on Gaussian processes; not a general-purpose probabilistic modeling toolkit

<sub>GPU optional · Needs PyTorch >= 2.4.1, NumPy >= 2.0, linear_operator · Models: Gaussian processes, SKI/KISS-GP, stochastic variational GP, deep kernel learning · [Repo](https://github.com/cornellius-gp/gpytorch) · [📖 Docs ↗](https://gpytorch.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpytorch/)</sub>

<a name="torchio"></a>
### #&#8288;225 [torchio](https://github.com/torchio-project/torchio) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Oct 2026</sub>

**PyTorch library for loading, augmenting and patch-sampling 3D medical images.**

TorchIO is a Python package for reading, preprocessing, sampling, augmenting and writing 3D medical images in PyTorch training pipelines. It provides intensity and spatial transforms, including random affine and elastic deformation, plus MRI-specific artifact simulation (bias field, motion, spike, ghosting). A Queue class supports patch-based training.

- **+** MRI-specific augmentations: bias field, k-space motion, spike and ghosting artifacts
- **+** Queue for patch-based training on large 3D volumes
- **+** Peer-reviewed paper (2021), docs and Colab tutorials
- **+** Installable from PyPI and conda-forge
- **−** Scoped to 3D medical imaging, not a general vision augmentation library
- **−** Tied to PyTorch; no other tensor framework mentioned
- **−** Data pipeline only; no models or training loop included

<sub>Needs PyTorch · [Repo](https://github.com/torchio-project/torchio) · [📖 Docs ↗](https://docs.torchio.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/torchio/)</sub>

<a name="tenseal"></a>
### #&#8288;226 [tenseal](https://github.com/openmined/tenseal) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · Apache-2.0 · Sep 2026</sub>

**Python library for homomorphic encryption on tensors, built on Microsoft SEAL.**

TenSEAL wraps Microsoft SEAL with a Python API and a C++ tensor layer. It encrypts integer vectors with BFV and real-number vectors with CKKS, and supports element-wise arithmetic, dot product, vector-matrix multiplication and N-dimensional encrypted tensors. Contexts, keys and ciphertexts can be serialized, and the full SEAL API is exposed under `tenseal.sealapi`.

- **+** Supports both BFV (integers) and CKKS (real numbers) schemes
- **+** Prebuilt wheels for Linux (glibc, musl), macOS arm64 and Windows x64
- **+** Tutorials cover encrypted logistic regression training and MNIST convolution
- **+** Full SEAL API exposed under tenseal.sealapi for lower-level control
- **−** Requires Python 3.11 or newer
- **−** Docker Hub images are unmaintained, last published in 2021
- **−** Bazel build is broken; C++ microbenchmarks cannot currently be run
- **−** Source builds fail on AppleClang 17+ and need a CMake 4 policy workaround

<sub>no GPU · Needs Microsoft SEAL, NumPy · [Repo](https://github.com/openmined/tenseal) · [🌐 Site ↗](https://www.openmined.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tenseal/)</sub>

<a name="face-recognition"></a>
### #&#8288;227 [face_recognition](https://github.com/ageitgey/face_recognition) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: widely used (97) · Freshness: recent (54) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 57k · MIT · Jun 2026</sub>

**Python library and CLI for face detection, landmarks and matching, built on dlib.**

Python library built on dlib that finds faces in images, returns landmarks for eyes, nose, mouth and chin, and compares face encodings to identify people. It also installs `face_recognition` and `face_detection` CLI tools that process folders of images, with a `--tolerance` setting (default 0.6) and `--cpus` for parallel runs. The README cites 99.38% accuracy on Labeled Faces in the Wild.

- **+** Few-line Python API: face_locations, face_landmarks, face_encodings, compare_faces
- **+** CLI tools identify faces across image folders, with --cpus for multi-core runs
- **+** Many runnable examples: webcam, video file, Raspberry Pi, Flask service, KNN and SVM
- **+** Optional CNN detector with GPU batch support when dlib is built with CUDA
- **−** Last release is 2018-04-02, so PyPI lags the repository
- **−** Requires building dlib with cmake; Windows is not officially supported
- **−** README says accuracy is weaker on children and varies between ethnic groups
- **−** CNN detection model needs a GPU for good performance

<sub>GPU optional · Docker + Compose · Needs dlib, cmake, Python 3.3+ or 2.7, OpenCV (webcam/video examples), Flask (web service example) · Models: dlib HOG face detector, dlib CNN face detector, dlib ResNet face encodings · [Repo](https://github.com/ageitgey/face_recognition) · [▶️ Demo ↗](https://beta.deepnote.org/launch?template=face_recognition) · [📖 Docs ↗](https://face-recognition.readthedocs.io/en/latest/face_recognition.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/face-recognition/)</sub>

<a name="paddledetection"></a>
### #&#8288;228 [paddledetection](https://github.com/paddlepaddle/paddledetection) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: widely used (81) · Freshness: recent (52) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Mar 2026</sub>

**Object detection toolkit on PaddlePaddle with tracking, keypoints and export tools.**

PaddleDetection is an end-to-end object detection suite built on PaddlePaddle. It bundles modular backbones, necks and losses with a model zoo covering 2D detection, instance segmentation, rotated boxes, multi-object tracking and keypoints, plus pipelines such as PP-Human and PP-Vehicle. Models export to Paddle Inference, Paddle Lite, Paddle Serving and ONNX.

- **+** Wide model zoo: Faster RCNN, YOLOX, PP-YOLOE, RT-DETR, PicoDet, DETR variants
- **+** Deploys via Paddle Inference (Python/C++), Paddle Lite, Paddle Serving or ONNX export
- **+** Ready-made pedestrian and vehicle analysis, tracking and keypoint pipelines
- **+** Training supports FP16, multi-machine runs, and PaddleSlim pruning, quantization, distillation
- **−** Requires the PaddlePaddle framework rather than PyTorch
- **−** README and many docs are primarily in Chinese
- **−** README quick start now points to PaddleX, not the native workflow
- **−** No Docker or compose files detected in the repository

<sub>GPU optional · Needs PaddlePaddle, PaddleSlim, Paddle Lite, Paddle Serving · Models: PP-YOLOE, RT-DETR, PP-PicoDet, Faster RCNN, YOLOX · [Repo](https://github.com/paddlepaddle/paddledetection) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddledetection/)</sub>

<a name="handwired"></a>
### #&#8288;229 [handwired](https://github.com/chenglou/handwired) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · MIT · Nov 2026</sub>

**Compiles plain JavaScript into an exact, differentiable matmul-and-ReGLU network.**

Handwired rewrites JavaScript control flow (if-else, loops, state) as matrix multiplications plus ReGLU over floats, with hand-written weights and no training. The resulting network runs on plain JS or WebGPU and stays differentiable, so weights can be unfrozen and trained, or a frozen program attached to a generic neural net. It is an experimental project with live demos, including a JSON search over 100k documents.

- **+** Program output is exact, with weights written by hand rather than trained
- **+** Only two primitives (matmul, ReGLU), so GPU fusion and sparsity optimizations apply
- **+** Runs on JS or WebGPU; JSON search demo covers 100k documents in milliseconds
- **+** Differentiable end to end, so frozen programs can combine with trainable nets
- **−** Experimental; README describes use cases as fun to try, not production
- **−** Both branches of every conditional are computed, which adds work
- **−** No releases published; the supported JavaScript subset is not documented in the README
- **−** Setup requires Bun and cloning the repo; no package install shown

<sub>GPU optional · Needs Bun · [Repo](https://github.com/chenglou/handwired) · [▶️ Demo ↗](https://chenglou.me/handwired/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/handwired/)</sub>

<a name="openmythos"></a>
### #&#8288;230 [openmythos](https://github.com/kyegomez/openmythos) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: widely used (82) · Freshness: recent (65) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · May 2026</sub>

**PyTorch looped-depth MoE transformer with switchable MLA or GQA attention.**

OpenMythos is a PyTorch implementation of a Recurrent-Depth Transformer: a Prelude, a Recurrent Block looped up to max_loop_iters, and a Coda, with a sparse MoE feed-forward using routed and shared experts. It ships configs from 1B to 1T parameters and a DDP training script for a 3B model on FineWeb-Edu. The README calls it a speculative reconstruction unaffiliated with Anthropic, and it mentions no pretrained weights.

- **+** Attention switchable between MLA and GQA, with optional Flash Attention 2 for GQA
- **+** Preset configs from mythos_1b to mythos_1t, installable with pip install open-mythos
- **+** Includes a 3B FineWeb-Edu training script with single-GPU and torchrun multi-GPU modes
- **+** Loop stability constrained by construction, with spectral radius of A checkable in code
- **−** Theoretical reconstruction based on speculation, not a replica of any real model
- **−** No pretrained weights or benchmark results mentioned in the README
- **−** Flash Attention 2 needs CUDA and build tools
- **−** README example imports mythos_7b, which is not in the listed variants

<sub>GPU optional · Needs PyTorch, flash-attn (optional) · Models: Recurrent-Depth Transformer, MoE, MLA, GQA · [Repo](https://github.com/kyegomez/openmythos) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmythos/)</sub>

<a name="surprise"></a>
### #&#8288;231 [surprise](https://github.com/nicolashug/surprise) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (62) · Freshness: recent (68) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.8k · BSD-3-Clause · May 2026</sub>

**Python scikit for building and evaluating rating-based recommender systems.**

Surprise is a Python scikit with recommender algorithms for explicit rating data: baselines, k-NN variants, SVD, SVD++, NMF, PMF, Slope One and Co-Clustering. It has built-in MovieLens and Jester loaders, scikit-learn-style cross-validation iterators and GridSearchCV for tuning. The maintainer says it only gets bugfixes and occasional performance work.

- **+** Ships SVD, SVD++, NMF, k-NN, Slope One and Co-Clustering with documented details
- **+** Built-in cross_validate and GridSearchCV; same folds across algorithms for comparison
- **+** Loads MovieLens and Jester built in, or custom rating datasets
- **+** README gives RMSE, MAE and runtime benchmarks on MovieLens 100k and 1M
- **−** No support for implicit feedback or content-based information
- **−** Maintenance mode since 1.1.0 (2019); new features are not considered
- **−** SVD++ took about 35-41 minutes on MovieLens 1M in the README benchmark
- **−** No tagged release listed in the repository metadata

<sub>no GPU · Needs numpy, Cython (source builds) · Models: SVD, SVD++, NMF, PMF, k-NN · [Repo](https://github.com/nicolashug/surprise) · [📖 Docs ↗](https://surprise.readthedocs.io/en/stable/index.html) · [🌐 Site ↗](https://surpriselib.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/surprise/)</sub>

<a name="gsplat"></a>
### #&#8288;232 [gsplat](https://github.com/nerfstudio-project/gsplat) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (57) · Freshness: recent (73) · Maintenance: weak (18) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Sep 2026</sub>

**CUDA library for rasterizing 3D Gaussians with PyTorch bindings.**

gsplat is a Python library with CUDA kernels for differentiable rasterization of 3D Gaussians, based on the 3D Gaussian Splatting paper. It includes training examples for COLMAP and NCore v4 captures, 3DGUT support, MCMC densification, LiDAR and fisheye camera models, and an experimental fp16 inference renderer. The README reports up to 4x less GPU memory and 15% less training time than the official implementation.

- **+** Reports up to 4x less GPU memory and 15% less time than the official implementation
- **+** Supports 3DGUT, MCMC densification, batching, and multiple camera and LiDAR sensor models
- **+** Pre-compiled wheels for Linux and Windows on selected Python, torch and CUDA combinations
- **+** Apache-2.0 with a JMLR paper, docs site and benchmark scripts
- **−** Requires CUDA; PyPI install compiles kernels on first run via JIT
- **−** v1.6.0 features are on main only and not yet on PyPI
- **−** Library, not an app: no GUI for capture-to-splat beyond example scripts
- **−** Last tagged release was July 2025; main will require PyTorch 2.7+

<sub>GPU required · Needs PyTorch, CUDA, ninja, numpy, jaxtyping, rich · Models: 3D Gaussian Splatting, 3DGUT, COLMAP datasets, NCore v4 · [Repo](https://github.com/nerfstudio-project/gsplat) · [📖 Docs ↗](https://docs.gsplat.studio/main/) · [🌐 Site ↗](http://www.gsplat.studio/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gsplat/)</sub>

<a name="probability"></a>
### #&#8288;233 [probability](https://github.com/tensorflow/probability) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (47) · Freshness: recent (70) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · Apache-2.0 · Nov 2026</sub>

**Probabilistic modeling and Bayesian inference library for TensorFlow and JAX.**

TensorFlow Probability provides probability distributions, bijectors, joint distribution models and probabilistic neural network layers, plus inference through MCMC (including Hamiltonian Monte Carlo), variational inference and stochastic optimizers. It runs on TensorFlow, and a JAX substrate is available via tensorflow_probability.substrates.jax. Examples are mostly Jupyter notebooks covering hierarchical models, Bayesian neural networks and mixture models.

- **+** Covers distributions, bijectors, MCMC and variational inference in one library
- **+** Runs on TensorFlow or pure JAX through a substrates import
- **+** Batch and broadcasting semantics on distributions allow GPU-accelerated vectorized computation
- **+** Many tutorial notebooks, including Eight Schools and Bayesian mixture models
- **−** README warns interfaces may change at any time
- **−** TensorFlow is not a pip dependency; it must be installed separately
- **−** Last tagged release is 2024-11-08, well behind recent commits
- **−** Building from source needs Bazel, and only up to 6.4.0 is supported

<sub>GPU optional · Needs TensorFlow or tensorflow-cpu, JAX (optional substrate), Bazel 6.4.0 (source builds only) · [Repo](https://github.com/tensorflow/probability) · [📖 Docs ↗](https://www.tensorflow.org/probability/api_docs/python/tfp) · [🌐 Site ↗](https://www.tensorflow.org/probability) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/probability/)</sub>

<a name="brax"></a>
### #&#8288;234 [brax](https://github.com/google/brax) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (34) · Freshness: active (94) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Oct 2026</sub>

**JAX physics engine and RL training library for massively parallel simulation.**

Brax is a differentiable rigid-body physics engine written in JAX, with four swappable pipelines (MJX, Generalized, Positional, Spring) behind one API. It also ships RL training code: PPO, SAC, ARS, evolutionary strategies and analytic policy gradients. As of 0.13.0 only brax/training is actively maintained; the README points to MuJoCo Playground for environments and MJX or MuJoCo Warp for physics.

- **+** Four physics pipelines share one API and can run side by side
- **+** Includes PPO, SAC, ARS, ES and differentiable analytic policy gradients
- **+** Runs on TPU, and on NVIDIA GPU with JAX CUDA support
- **+** Colab notebooks cover basics, training, MJX and PyTorch usage
- **−** brax/envs and the physics engines are no longer maintained; only brax/training is
- **−** README recommends MuJoCo Playground and MJX instead of Brax for simulation
- **−** Future direction is uncertain; may be repurposed purely as an RL library
- **−** GPU use requires separately installing CUDA, CuDNN and GPU-enabled JAX

<sub>GPU optional · Needs JAX, CUDA and CuDNN (for NVIDIA GPU) · Models: PPO, SAC, ARS, evolutionary strategies, analytic policy gradients · [Repo](https://github.com/google/brax) · [▶️ Demo ↗](https://colab.research.google.com/github/google/brax/blob/main/notebooks/training.ipynb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/brax/)</sub>

<a name="gpflow"></a>
### #&#8288;235 [gpflow](https://github.com/gpflow/gpflow) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · Apache-2.0 · Oct 2026</sub>

**Gaussian process modelling library for Python built on TensorFlow.**

GPflow is a Python package for building Gaussian process models with composable kernels and likelihoods. It runs on TensorFlow 2.4+ and TensorFlow Probability, so computation can run on GPUs. It also includes a framework for interdomain approximations and multioutput priors, described in an arXiv paper.

- **+** Composable kernels and likelihoods for building custom Gaussian process models
- **+** Supports interdomain approximations and multioutput priors, documented in a published paper
- **+** Installs from PyPI with pip; GPU execution comes through TensorFlow
- **+** Intro notebook and a GPflow 1 upgrade guide are provided
- **−** Tied to TensorFlow and TensorFlow Probability; version mismatches cause import errors
- **−** No backward compatibility for models; the TF graph can change between versions
- **−** GPflow 1.x on TensorFlow 1 is discontinued; last such release is v1.5.1
- **−** Develop branch changes regularly and may break code

<sub>GPU optional · Needs TensorFlow >= 2.4, TensorFlow Probability >= 0.12 · Models: Gaussian processes · [Repo](https://github.com/gpflow/gpflow) · [📖 Docs ↗](https://gpflow.github.io/GPflow/) · [🌐 Site ↗](https://gpflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpflow/)</sub>

<a name="imbalanced-learn"></a>
### #&#8288;236 [imbalanced-learn](https://github.com/scikit-learn-contrib/imbalanced-learn) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (63) · Freshness: recent (79) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Jun 2026</sub>

**Re-sampling methods for imbalanced classification datasets, scikit-learn compatible.**

imbalanced-learn is a Python package of re-sampling techniques for classification datasets with strong between-class imbalance. It follows the scikit-learn API and is part of the scikit-learn-contrib projects. Optional support exists for pandas dataframes and TensorFlow/Keras models.

- **+** Follows the scikit-learn API, so it fits existing estimators
- **+** Installable from PyPI and conda-forge
- **+** Documentation with API reference and examples; JMLR paper to cite
- **+** MIT license; last release 2026-06-07
- **−** Aimed at tabular classification; not for LLM or text workflows
- **−** Requires Python 3.10+, scikit-learn 1.4.2+ and NumPy 1.25.2+
- **−** README lists Pytest as a hard dependency
- **−** README does not list the algorithms; docs must be consulted

<sub>no GPU · Needs Python >= 3.10, NumPy >= 1.25.2, SciPy >= 1.11.4, scikit-learn >= 1.4.2, pandas >= 2.0.3 (optional), TensorFlow >= 2.16.1 (optional), Keras >= 3.3.3 (optional) · Models: scikit-learn estimators, Keras, TensorFlow · [Repo](https://github.com/scikit-learn-contrib/imbalanced-learn) · [📖 Docs ↗](https://imbalanced-learn.org/stable/user_guide.html) · [🌐 Site ↗](https://imbalanced-learn.org/stable/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/imbalanced-learn/)</sub>

<a name="paddleclas"></a>
### #&#8288;237 [paddleclas](https://github.com/paddlepaddle/paddleclas) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (57) · Freshness: recent (70) · Maintenance: weak (18) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

**Image classification and recognition toolkit on PaddlePaddle, with PP-ShiTuV2 and PULC.**

PaddleClas is a PaddlePaddle toolkit for training and deploying image classification and image retrieval models. It ships the PP-LCNet, PP-LCNetV2 and PP-HGNet backbones, the PULC lightweight classifiers (13 tasks listed, such as person, vehicle and text orientation), and PP-ShiTuV2, a detection, feature extraction and vector search pipeline. Since 2024-11 the low-code PaddleX tool wraps 98 of its models as six pipelines.

- **+** Covers training, SSLD distillation, pruning and quantization in one toolkit
- **+** Deployment paths: Python and C++ inference, Paddle Serving, Paddle Lite, Paddle2ONNX
- **+** PULC claims 3 ms CPU inference; PP-LCNet targets Intel CPUs with MKLDNN
- **+** PP-ShiTuV2 includes a gallery management tool and an Android demo
- **−** Requires the PaddlePaddle framework, not PyTorch; weights are .pdparams
- **−** README and most docs are primarily in Chinese
- **−** Last release was 2024-11-05; newer work is directed to PaddleX
- **−** Image classification and retrieval only; no LLM or generative support

<sub>GPU optional · Needs PaddlePaddle · Models: PP-LCNet, PP-LCNetV2, PP-HGNet, PULC, PP-ShiTuV2 · [Repo](https://github.com/paddlepaddle/paddleclas) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddleclas/)</sub>

<a name="augly"></a>
### #&#8288;238 [augly](https://github.com/facebookresearch/augly) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (52) · Freshness: recent (70) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · custom license · Nov 2026</sub>

**Python library of audio, image, text and video data augmentations.**

AugLy is a Python library from Meta AI with over 100 augmentations across audio, image, text and video. Each modality is a separate sub-library with function and class transforms, composition operators, and optional metadata on the applied transform. It focuses on augmentations common on social platforms, such as memes, text or emoji overlays and screenshot reposts, for training and robustness evaluation.

- **+** Covers four modalities (audio, image, text, video) with per-modality pip installs
- **+** Includes social-media style transforms: memes, screenshot overlays, emoji and text overlays
- **+** Transforms can return metadata, including intensity, about what was applied
- **+** Ships emoji, font and screenshot template assets for its overlay augmentations
- **−** Last release was 2022-03-29, so the PyPI version lags the repository
- **−** README states Python 3.6+ and does not mention newer Python versions
- **−** python-magic may need a separate conda or apt install
- **−** Licence detected as NOASSERTION although the README says MIT

<sub>Needs python-magic · [Repo](https://github.com/facebookresearch/augly) · [▶️ Demo ↗](https://colab.research.google.com/github/facebookresearch/AugLy/blob/main/examples/AugLy_image.ipynb) · [📖 Docs ↗](https://augly.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/augly/)</sub>

<a name="nevergrad"></a>
### #&#8288;239 [nevergrad](https://github.com/facebookresearch/nevergrad) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: known (45) · Freshness: recent (70) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · MIT · Nov 2026</sub>

**Python library for gradient-free optimization of continuous and discrete parameters.**

Nevergrad is a Python 3.8+ library that minimizes black-box functions without gradients. It provides optimizers such as NGOpt and differential evolution variants, plus a parametrization API for bounded, log-scaled, integer and categorical variables, including functions with keyword arguments. Typical use is hyperparameter search under a fixed evaluation budget.

- **+** Parametrization mixes log-scaled, integer-cast, bounded and categorical variables in one search space
- **+** Installs with pip; minimize() takes a parametrization and an evaluation budget
- **+** NGOpt selects an algorithm automatically, so no optimizer tuning is needed to start
- **+** MIT licensed, with a documentation site and published benchmark data
- **−** Last release is 2025-04-23, well behind recent commits
- **−** README gives no benchmark numbers or comparison with other optimizer libraries
- **−** Black-box optimizer only; not an LLM, agent or model-serving tool
- **−** Authors describe the documentation as a work in progress

<sub>no GPU · [Repo](https://github.com/facebookresearch/nevergrad) · [📖 Docs ↗](https://facebookresearch.github.io/nevergrad/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nevergrad/)</sub>

<a name="neuraloperator"></a>
### #&#8288;240 [neuraloperator](https://github.com/neuraloperator/neuraloperator) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: known (43) · Freshness: active (82) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · MIT · Oct 2026</sub>

**PyTorch library of neural operator models, including Fourier Neural Operators.**

NeuralOperator is a PyTorch library for training neural operators, which learn mappings between function spaces and can be applied at different data resolutions. It includes the official Fourier Neural Operator (FNO) implementation, a Tucker-factorized variant (TFNO) and other operator architectures. Optional Weights & Biases logging is set up through a key file in the config directory.

- **+** Official FNO implementation, with a JMLR paper and a library paper behind it
- **+** TFNO uses Tucker factorization to cut Fourier layer parameters to about 10%
- **+** Installable from PyPI with pip install neuraloperator
- **+** Part of the PyTorch Ecosystem; MIT licensed
- **−** Scoped to operator learning for PDE-style data, not general deep learning
- **−** README quickstart only constructs models; no training example is shown
- **−** Last tagged release is October 2025, so main may be ahead of PyPI

<sub>Needs PyTorch, Weights & Biases (optional) · Models: FNO, TFNO · [Repo](https://github.com/neuraloperator/neuraloperator) · [📖 Docs ↗](https://neuraloperator.github.io/dev/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/neuraloperator/)</sub>

<a name="open3d-ml"></a>
### #&#8288;241 [open3d-ml](https://github.com/isl-org/open3d-ml) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (21) · Freshness: active (98) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · custom license · Aug 2026</sub>

**3D point cloud segmentation and detection models for PyTorch and TensorFlow.**

Open3D-ML extends Open3D with datasets, models, training pipelines and a visualizer for 3D machine learning. It covers semantic segmentation (RandLA-Net, KPConv, SparseConvUnet) and object detection (PointPillars) on datasets such as SemanticKITTI, S3DIS, ScanNet and KITTI, with pretrained weights in a model zoo. It runs on PyTorch or TensorFlow through the open3d.ml namespace.

- **+** Pretrained weights linked per model and dataset, with mIoU scores in a table
- **+** Same pipeline API for PyTorch and TensorFlow, driven by YAML configs
- **+** Built-in visualizer for datasets, predictions and bounding boxes
- **+** scripts/run_pipeline.py trains and tests from a config with CLI overrides
- **−** Pinned to PyTorch 2.0 and TensorFlow 2.13; other versions need a source build
- **−** Since Open3D 0.18, Linux PyPI wheels lack TensorFlow ops; needs a custom Docker build
- **−** The Docker TensorFlow build excludes PyTorch ops, so one wheel cannot serve both
- **−** Task coverage limited to point cloud segmentation and object detection

<sub>GPU optional · Needs open3d, PyTorch 2.0, TensorFlow 2.13, CUDA 10.1/11 (optional) · Models: RandLA-Net, KPConv, SparseConvUnet, PointPillars · [Repo](https://github.com/isl-org/open3d-ml) · [📖 Docs ↗](http://www.open3d.org/docs/release/compilation.html) · [🌐 Site ↗](http://www.open3d.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open3d-ml/)</sub>

<a name="feature-engine"></a>
### #&#8288;242 [feature_engine](https://github.com/feature-engine/feature_engine) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · BSD-3-Clause · Sep 2026</sub>

**Scikit-learn-style transformers for feature engineering and selection.**

Feature-engine is a Python library of transformers for imputation, categorical encoding, discretisation, outlier handling, variable transformation and feature selection. Each transformer follows the Scikit-learn fit() and transform() API, so it works inside Scikit-learn pipelines. It also covers datetime, text and time-series features (lags and window features), and includes a SklearnWrapper.

- **+** Scikit-learn fit/transform API, so it drops into existing pipelines
- **+** Wide coverage: imputers, encoders, discretisers, outlier cappers, selectors, time-series features
- **+** Selection methods include MRMR, recursive elimination, PSI-based dropping and probe features
- **+** Installable with pip or conda; docs and example notebook gallery provided
- **−** Classical tabular ML only; no LLM or deep learning functionality
- **−** Scaling support is thin: only MeanNormalisationScaler is listed
- **−** Library only, with no CLI, server or UI

<sub>no GPU · Models: scikit-learn · [Repo](https://github.com/feature-engine/feature_engine) · [📖 Docs ↗](https://feature-engine.readthedocs.io/en/latest/index.html) · [🌐 Site ↗](https://feature-engine.trainindata.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/feature-engine/)</sub>

<a name="snntorch"></a>
### #&#8288;243 [snntorch](https://github.com/jeshraghian/snntorch) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (16) · Freshness: recent (70) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · MIT · Oct 2026</sub>

**PyTorch library for training spiking neural networks with surrogate gradients.**

snnTorch extends PyTorch with spiking neuron models such as Leaky integrate-and-fire, used as activation layers inside nn.Sequential-style networks. It provides surrogate gradient functions, spike encoding, spike-aware loss and weight init, plotting, and import/export to other SNN libraries through NIR. Neurons are implemented as recursive functions, so membrane potential traces need not be stored for gradients.

- **+** Spiking neurons drop into PyTorch models alongside conv, linear and residual layers
- **+** Includes surrogate gradients, spike encoding, loss functions and weight init in one package
- **+** NIR import and export for moving networks to other SNN libraries
- **+** Seven tutorial notebooks plus advanced ones, with Colab links
- **−** Last tagged release is 2024-03-17, well behind recent commits
- **−** Requires a separately installed, version-matched PyTorch for CUDA
- **−** Research-oriented; no deployment or neuromorphic hardware runtime included
- **−** NIR features need extra packages (nir, nirtorch); plotting needs matplotlib

<sub>GPU optional · Needs PyTorch, numpy, pandas, nir>=1.0.6 (optional), nirtorch>=2.0.5 (optional), matplotlib (optional) · Models: Leaky integrate-and-fire neurons, 2nd order spiking neurons, recurrent LIF neurons, NIR import/export · [Repo](https://github.com/jeshraghian/snntorch) · [▶️ Demo ↗](https://colab.research.google.com/github/jeshraghian/snntorch/blob/master/examples/quickstart.ipynb) · [📖 Docs ↗](https://snntorch.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/snntorch/)</sub>

<a name="react-native-fast-tflite"></a>
### #&#8288;244 [react-native-fast-tflite](https://github.com/margelo/react-native-fast-tflite) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (3) · Freshness: active (97) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Sep 2026</sub>

**TensorFlow Lite inference for React Native with zero-copy buffers.**

A React Native library that runs .tflite models on-device through the TensorFlow Lite C/C++ core API, built on Nitro Modules. Inputs and outputs are passed as ArrayBuffers without copying, models can be loaded from the bundle, a file or a URL, and CoreML, Android GPU and NNAPI delegates are optional. It integrates with VisionCamera frame processors for real-time camera inference.

- **+** Zero-copy ArrayBuffer input and output via the low-level TFLite C/C++ API
- **+** Models load from bundle, file:// or http(s) URL and can be swapped at runtime
- **+** Optional CoreML, Android GPU and NNAPI delegates, with an Expo config plugin
- **+** Synchronous runSync works inside VisionCamera frame processors
- **−** You must interpret raw tensor bytes yourself; shapes are inspected manually, e.g. in Netron
- **−** Camera frames need a separate resizer package to match the model input size
- **−** CoreML delegate does not support all model operations
- **−** NNAPI is deprecated on Android 15; GPU libraries may need manifest entries

<sub>GPU optional · Needs react-native-nitro-modules, react-native-vision-camera (optional), react-native-vision-camera-resizer (optional) · Models: TensorFlow Lite (.tflite) · [Repo](https://github.com/margelo/react-native-fast-tflite) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/react-native-fast-tflite/)</sub>

<a name="time-series-library"></a>
### #&#8288;245 [time-series-library](https://github.com/thuml/time-series-library) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (79) · Freshness: recent (52) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Apr 2026</sub>

**PyTorch benchmark library of deep time series models for research.**

TSLib is a PyTorch code base that implements dozens of deep time series models (TimesNet, iTransformer, PatchTST, DLinear, Mamba and others) under one training and evaluation interface. It covers forecasting, imputation, anomaly detection and classification, and supports zero-shot evaluation of pretrained models such as Chronos, TimesFM and Moirai. Maintainers state in April 2026 that no new features will be added.

- **+** One run.py entry point covers five tasks across many reference model implementations
- **+** Includes zero-shot evaluation for Chronos, TimesFM, Moirai, Sundial and TiRex
- **+** Docker and compose files provided, plus a TimesNet tutorial notebook
- **+** Preprocessed datasets hosted on Google Drive, Baidu and Hugging Face
- **−** Maintainers will not actively add features; README calls many benchmarks no longer meaningful
- **−** Leaderboard dates from March 2024 and is not current
- **−** Datasets must be downloaded manually into ./dataset
- **−** Mamba needs a Linux, CUDA-specific wheel; torch must match local CUDA

<sub>GPU optional · Docker + Compose · Needs PyTorch 2.5.1, Conda (Python 3.11), mamba_ssm (for Mamba), uni2ts (for Moirai) · Models: TimesNet, iTransformer, PatchTST, DLinear, TimeXer · [Repo](https://github.com/thuml/time-series-library) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/time-series-library/)</sub>

<a name="pycaret"></a>
### #&#8288;246 [pycaret](https://github.com/pycaret/pycaret) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (73) · Freshness: slowing (44) · Maintenance: weak (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · custom license · May 2026</sub>

**Self-hosted AutoML platform with experiment tracking, model registry and deployment UI.**

PyCaret 4.0 combines a scikit-learn-based AutoML engine with a FastAPI control plane and a React web UI. You upload a dataset, run an experiment that trains about 12 algorithms, promote the winner to a model registry and deploy it behind a prediction endpoint. The README marks 4.0 as work in progress; the default setup runs in-process with SQLite.

- **+** Covers train, register, deploy and predict in one UI and API
- **+** Two-container docker compose setup, web UI on port 3020
- **+** Optional Postgres and S3 storage via environment variables
- **+** Engine is MIT; supports classification, regression, clustering, anomaly and time series
- **−** 4.0 is work in progress; most Protocol extractions for splitting services are unfinished
- **−** Default setup runs scheduler and compute in the API process with SQLite
- **−** Control plane is BUSL-1.1, not OSI open source; only the engine is MIT
- **−** Last release is 2024-04-28; the 3.x line on PyPI is frozen

<sub>RAM ≥ 6 GB · no GPU · Compose · Needs Docker Compose, SQLite (default), Postgres (optional), S3 (optional) · Models: scikit-learn algorithms, Anthropic API (optional copilots), OpenAI API (optional copilots) · port 3020 · [Repo](https://github.com/pycaret/pycaret) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pycaret/)</sub>

<a name="cube-studio"></a>
### #&#8288;247 [tencentmusic/cube-studio](https://github.com/tencentmusic/cube-studio) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (52) · Freshness: active (86) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · custom license · Jul 2026</sub>

**Archived Cube Studio repository, development moved to data-infra/cube-studio.**

Cube Studio is a Tencent Music project whose README contains only an architecture diagram and a link to a wiki. The repository was archived on 2026-05-18 and is no longer maintained, with development moved to data-infra/cube-studio. The README does not describe features, install steps or supported models.

- **+** Help documentation is kept in a GitHub wiki
- **+** README includes an overall architecture diagram
- **+** A successor repository (data-infra/cube-studio) is named in the README
- **−** Repository archived 2026-05-18 and no longer maintained
- **−** License is not detected (NOASSERTION), so reuse terms are unclear
- **−** README gives no install steps, requirements or feature list
- **−** No Docker or compose files detected in the repository

<sub>[Repo](https://github.com/tencentmusic/cube-studio) · [📖 Docs ↗](https://github.com/data-infra/cube-studio/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cube-studio/)</sub>

<a name="tiny-cuda-nn"></a>
### #&#8288;248 [tiny-cuda-nn](https://github.com/nvlabs/tiny-cuda-nn) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: known (49) · Freshness: recent (73) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · custom license · Sep 2026</sub>

**CUDA library of fused small MLPs and hash encodings, with PyTorch bindings.**

tiny-cuda-nn is a C++/CUDA framework for training and querying small neural networks, built around a fully fused MLP and multiresolution hash encoding. It also ships other encodings, losses and optimizers, an optional JIT fusion mode (v2.0+) using CUDA runtime compilation, and a PyTorch extension. It underlies Instant NGP and related neural graphics work.

- **+** Fully fused MLP kernels, benchmarked in the README against TensorFlow 2.5 with XLA on an RTX 3090
- **+** JIT fusion gives a stated 1.5x to 2.5x speedup, more on newer GPUs
- **+** Hash grid, frequency, oneblob and spherical harmonics encodings, plus Adam and Shampoo optimizers
- **+** Usable from C++ or from PyTorch via the tinycudann package
- **−** Requires an NVIDIA GPU and CUDA toolchain; no other backends are listed
- **−** Default fully fused MLP needs large shared memory; RTX 2080 Ti or better
- **−** PyTorch binding is about 2x slower than native CUDA at 64k batch size
- **−** JIT fusion can slow training on RTX 3000 or older, or with very large grids

<sub>GPU required · Needs CUDA, CMake 3.21+, C++17 compiler, PyTorch (optional bindings) · Models: FullyFusedMLP, CutlassMLP, multiresolution hash grid encoding · [Repo](https://github.com/nvlabs/tiny-cuda-nn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tiny-cuda-nn/)</sub>

<a name="acme"></a>
### #&#8288;249 [acme](https://github.com/google-deepmind/acme) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: known (44) · Freshness: recent (70) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · Apache-2.0 · Nov 2026</sub>

**Reinforcement learning library with reference agents in JAX and TensorFlow.**

Acme is a DeepMind Python library of reinforcement learning building blocks and readable reference agents, meant as baselines and a starting point for new research. Agents run on JAX or TensorFlow depending on the agent, and the components are designed to run either single-stream or distributed. Example environments from gym, dm_control and bsuite install through an extra.

- **+** Reference agents written to be readable and usable as research baselines
- **+** Same building blocks run single-process or distributed
- **+** Quickstart and tutorial Colab notebooks plus an examples directory
- **+** Pip extras for JAX, TensorFlow and example environments (gym, dm_control, bsuite)
- **−** README warns things may break occasionally; it is a research codebase
- **−** Last tagged release is from 2022-02-10, so PyPI lags the repository
- **−** Core install is minimal; JAX or TensorFlow must be installed separately
- **−** Not aimed at LLM or agent apps; focused on classic RL

<sub>Needs JAX, TensorFlow, gym, dm_control, bsuite · [Repo](https://github.com/google-deepmind/acme) · [📖 Docs ↗](https://dm-acme.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/acme/)</sub>

<a name="gin-config"></a>
### #&#8288;250 [gin-config](https://github.com/google/gin-config) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Oct 2026</sub>

**Python config library using decorators and .gin files for dependency injection.**

Gin lets you decorate Python functions or classes with `@gin.configurable` and override their default parameters from `.gin` files or the command line. It supports references to other configurables, scopes, macros, file includes and logging of the operative config. It targets ML experiments with many nested parameters, with optional `gin.tf` and `gin.torch` modules.

- **+** Needs only a decorator and a parse call; no config objects or protos to maintain
- **+** Scopes let one function be configured differently, e.g. generator and discriminator networks
- **+** Logs the operative config, with TensorBoard integration
- **+** Installs with pip; core import works without TensorFlow
- **−** README says it is in alpha; corner-case behavior may change incompatibly
- **−** Evaluated references are not cached, which can surprise users, especially with macros
- **−** Nested scopes have ongoing debate over ordering and behavior
- **−** Heavily hierarchical configs reduce readability; no tagged releases

<sub>no GPU · Models: TensorFlow (optional gin.tf), PyTorch (optional gin.torch) · [Repo](https://github.com/google/gin-config) · [📖 Docs ↗](https://github.com/google/gin-config/tree/master/docs/index.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gin-config/)</sub>

<a name="deepchem"></a>
### #&#8288;251 [deepchem](https://github.com/deepchem/deepchem) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (63) · Freshness: recent (68) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · MIT · Aug 2026</sub>

**Python library for deep learning on molecules, materials and biological data.**

DeepChem is a Python toolchain for machine learning in drug discovery, materials science, quantum chemistry and biology. It offers models with TensorFlow, PyTorch and JAX backends, built on rdkit, scikit-learn and NumPy. Colab-ready tutorials and examples take users from beginner level up.

- **+** Supports TensorFlow, PyTorch and JAX through separate pip extras
- **+** Large set of tutorials and examples that run on Google Colab
- **+** Installable via pip, conda-forge or deepchemio Docker images
- **+** Integrates with Weights & Biases for tracking training metrics
- **−** README lists Python 3.7 through 3.10 only
- **−** Last tagged release is 2024-04-03, though commits continue
- **−** Some features need extra soft dependencies installed by hand
- **−** GPU use requires installing CUDA and the framework separately

<sub>GPU optional · Docker · Needs rdkit, NumPy, pandas, scikit-learn, SciPy, joblib · Models: TensorFlow, PyTorch, JAX · [Repo](https://github.com/deepchem/deepchem) · [📖 Docs ↗](https://deepchem.readthedocs.io/en/latest/) · [🌐 Site ↗](https://deepchem.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepchem/)</sub>

<a name="mmf"></a>
### #&#8288;252 [mmf](https://github.com/facebookresearch/mmf) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (56) · Freshness: recent (70) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · custom license · Oct 2026</sub>

**PyTorch framework for vision and language multimodal research.**

MMF is a PyTorch codebase from Facebook AI Research with reference implementations of vision and language models and support for distributed training. It also serves as a starter codebase for challenges such as Hateful Memes, TextVQA, TextCaps and VQA. It was formerly called Pythia.

- **+** Reference implementations of vision and language models from FAIR research projects
- **+** Distributed training supported on PyTorch
- **+** Starter code for Hateful Memes, TextVQA, TextCaps and VQA challenges
- **+** Documentation site with feature list and video overview
- **−** Last tagged release is from 2019-08-26
- **−** Research codebase, not a packaged app or inference server
- **−** License detected as NOASSERTION; README only says BSD
- **−** README gives no hardware requirements or model list inline

<sub>Needs PyTorch · [Repo](https://github.com/facebookresearch/mmf) · [📖 Docs ↗](https://mmf.sh/docs) · [🌐 Site ↗](https://mmf.sh/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mmf/)</sub>

<a name="neural-prophet"></a>
### #&#8288;253 [neural_prophet](https://github.com/ourownstory/neural_prophet) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: known (46) · Freshness: recent (70) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Oct 2026</sub>

**PyTorch time series forecasting library inspired by Facebook Prophet and AR-Net.**

NeuralProphet is a Python library for interpretable time series forecasting, built on PyTorch. It combines Prophet-style components (piecewise linear trend, Fourier seasonality, holidays and events) with autoregression and lagged or future regressors that can be linear or neural networks. It supports multiple series with global or 'glocal' components and quantile-based uncertainty.

- **+** Prophet-like API: fit, predict and plot forecasts and components in a few lines
- **+** Autoregression and lagged or future regressors can be linear or neural (AR-Net)
- **+** Global and 'glocal' modelling across multiple series, plus quantile regression
- **+** Includes cross-validation utility, checkpointing and regularization of components
- **−** README says it is still in beta and may not be most accurate out of the box
- **−** Docs page may be out of date; README points to docstrings instead
- **−** README recommends higher-frequency data covering at least two full periods
- **−** Last release is 2024-06-21; logistic growth trend still listed as coming soon

<sub>Needs PyTorch, Python 3.9+ · Models: Prophet-style trend and seasonality, AR-Net autoregression, Quantile regression · [Repo](https://github.com/ourownstory/neural_prophet) · [📖 Docs ↗](https://neuralprophet.com) · [🌐 Site ↗](https://neuralprophet.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/neural-prophet/)</sub>

<a name="ddsp"></a>
### #&#8288;254 [ddsp](https://github.com/magenta/ddsp) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: known (36) · Freshness: recent (70) · Maintenance: weak (26) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · Apache-2.0 · Oct 2026</sub>

**TensorFlow library of differentiable synthesizers and effects for neural audio.**

DDSP provides differentiable versions of common DSP building blocks, such as harmonic and filtered-noise synthesizers, reverb and spectral losses, as TensorFlow Keras layers. They serve as interpretable output layers for audio generation models. The repo also includes a gin-configured training library and Colab demos for timbre transfer, autoencoder training and pitch detection.

- **+** ProcessorGroup lets a synth and effects chain be defined as a DAG in gin files
- **+** Colab demos cover timbre transfer, autoencoder training and pitch detection
- **+** Five tutorial notebooks and per-module test files show usage of core functions
- **+** Installs with pip; core library runs in TensorFlow eager or graph mode
- **−** TensorFlow only; requires TensorFlow 2.1.0 or newer
- **−** Last release was April 2023, so the PyPI package may lag the main branch
- **−** Heavy gin global configuration can cause side effects, as the README admits
- **−** Functions marked EXPERIMENTAL may change and are not guaranteed to be maintained

<sub>Needs TensorFlow >= 2.1.0, libsndfile, gin-config · Models: DDSP autoencoder, pretrained timbre transfer models · [Repo](https://github.com/magenta/ddsp) · [▶️ Demo ↗](https://colab.research.google.com/github/magenta/ddsp/blob/main/ddsp/colab/demos/timbre_transfer.ipynb) · [🌐 Site ↗](https://magenta.tensorflow.org/ddsp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ddsp/)</sub>

<a name="lighteval"></a>
### #&#8288;255 [lighteval](https://github.com/huggingface/lighteval) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (24) · Freshness: active (85) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · MIT · Oct 2026</sub>

**Python toolkit for running LLM benchmarks across many inference backends.**

Lighteval runs 1000+ evaluation tasks (MMLU, GPQA, GSM8K, IFEval, AIME and others) against models loaded in memory or served remotely. Backends include inspect-ai, Accelerate, vLLM, SGLang, Nanotron, TGI, LiteLLM and Hugging Face Inference Endpoints and Providers. It saves sample-by-sample results and supports custom tasks and metrics.

- **+** 1000+ tasks across many languages, with an online benchmark index to search them
- **+** Many backends: inspect-ai, Accelerate, vLLM, SGLang, Nanotron, TGI, LiteLLM, HF endpoints
- **+** Saves per-sample results for debugging, with optional push to the Hugging Face Hub
- **+** Custom tasks and metrics can be added; Python API evaluates already-loaded models
- **−** Untested on Windows and not supported there; Mac and Linux only
- **−** Many overlapping entry points, with inspect-ai marked preferred, so picking a backend takes reading
- **−** Last release is 2025-11-24, a year behind recent commits
- **−** CLI and Python API only, no web UI

<sub>GPU optional · Needs inspect-ai, Hugging Face Accelerate, vLLM, SGLang, Nanotron, LiteLLM, Text Generation Inference, Hugging Face Hub · Models: Transformers models, vLLM, SGLang, TGI, LiteLLM-compatible APIs · [Repo](https://github.com/huggingface/lighteval) · [📖 Docs ↗](https://huggingface.co/docs/lighteval/main/en/index) · [🌐 Site ↗](https://huggingface.co/spaces/OpenEvals/open_benchmark_index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lighteval/)</sub>

<a name="maniskill"></a>
### #&#8288;256 [maniskill](https://github.com/mani-skill/maniskill) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: known (38) · Freshness: active (90) · Maintenance: weak (1) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · Apache-2.0 · Aug 2026</sub>

**GPU-parallelized robot simulation and learning framework for manipulation tasks.**

ManiSkill 3 is a Python framework built on SAPIEN for simulating robots and training manipulation policies. It runs many environments in parallel on the GPU, including heterogeneous scenes, and the README claims 30,000+ FPS for RGBD plus segmentation data on a 4090. It ships tasks for humanoids, mobile manipulators and single-arm robots, plus RL, imitation learning and VLA baselines.

- **+** GPU-parallelized simulation and rendering, with 30,000+ FPS RGBD collection claimed on a 4090
- **+** Heterogeneous parallel simulation: each environment can hold different scenes and objects
- **+** Tuned baselines for PPO, SAC, TD-MPC2, Diffusion Policy, Octo, RDT-1B and RT-x
- **+** Includes real2sim evaluation environments and sim2real deployment examples
- **−** GPU simulation works only on Linux with an NVIDIA GPU
- **−** Requires a separate Vulkan setup for rendering
- **−** WSL has no rendering; Windows and macOS lack GPU sim
- **−** Assets are licensed CC BY-NC 4.0, which restricts commercial use

<sub>GPU optional · Docker · Needs SAPIEN, PyTorch, Vulkan · Models: PPO, SAC, TD-MPC2, Behavior Cloning, Diffusion Policy · [Repo](https://github.com/mani-skill/maniskill) · [▶️ Demo ↗](https://colab.research.google.com/github/mani-skill/ManiSkill/blob/main/examples/tutorials/1_quickstart.ipynb) · [📖 Docs ↗](https://maniskill.readthedocs.io/en/latest/user_guide) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/maniskill/)</sub>

<a name="pykeen"></a>
### #&#8288;257 [pykeen](https://github.com/pykeen/pykeen) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (15) · Freshness: recent (70) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · MIT · Nov 2026</sub>

**Python library for training and evaluating knowledge graph embedding models.**

PyKEEN is a Python package for training and evaluating knowledge graph embedding models. Its pipeline function trains a named model on a named dataset and returns the trained model, training loop and rank-based evaluation results. It ships 40 models, 37 built-in datasets plus 5 inductive ones, and Optuna integration for hyperparameter search.

- **+** Single pipeline() call trains and evaluates a model on a built-in dataset
- **+** 40 models and 37 datasets share one API, so components are swappable
- **+** Custom datasets supported via TriplesFactory and a bring-your-own-data tutorial
- **+** Optuna integration for hyperparameter search; MIT licensed
- **−** Limited to knowledge graph link prediction; not for LLMs or text generation
- **−** Last release (2025-04-24) is older than the latest commits
- **−** Requires Python 3.11 or newer

<sub>Needs Optuna (optional integration), PyTorch Lightning (optional integration) · Models: TransE, 40 knowledge graph embedding models · [Repo](https://github.com/pykeen/pykeen) · [📖 Docs ↗](https://pykeen.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pykeen/)</sub>

<a name="evalai"></a>
### #&#8288;258 [evalai](https://github.com/cloud-cv/evalai) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (15) · Freshness: recent (70) · Maintenance: patchy (35) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · custom license · Oct 2026</sub>

**Host ML challenges with submissions, evaluation workers and public leaderboards.**

EvalAI is a Django and Node.js platform for running AI benchmark challenges. Organizers define evaluation phases and dataset splits, participants submit results or Docker images, and workers score them into public or private leaderboards. Organizers can attach their own worker clusters for remote evaluation, and an evalai-cli client covers command-line use.

- **+** Arbitrary evaluation phases and dataset splits, with public and private leaderboards
- **+** Remote evaluation: organizers can attach their own worker nodes for heavy challenges
- **+** Participants can submit Docker images evaluated against test environments
- **+** Separate evalai-cli project for submissions from the terminal
- **−** Last tagged release is from 2018, so there are no recent versioned releases
- **−** Built for challenge hosting, not for evaluating LLM prompts or apps
- **−** Local setup needs Postgres, SQS and Django containers, with workers as an extra profile
- **−** Seeded default accounts use the password 'password' and must be changed

<sub>Compose · Needs Docker, docker-compose, PostgreSQL, SQS, Node.js · port 8888 · [Repo](https://github.com/cloud-cv/evalai) · [📖 Docs ↗](https://evalai.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/evalai/)</sub>

<a name="jittor"></a>
### #&#8288;259 [jittor](https://github.com/jittor/jittor) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (34) · Freshness: recent (75) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · Apache-2.0 · Nov 2026</sub>

**Python deep learning framework that JIT-compiles meta-operators to C++ and CUDA.**

Jittor is a deep learning framework with a Python front end (modules, dynamic graph execution) and a C++/CUDA back end. The framework and its meta-operators are compiled just-in-time, with an integrated op compiler and tuner generating code specialized to the model. It ships model libraries for recognition, detection, segmentation, generation, differentiable rendering and reinforcement learning, and is maintained by the Tsinghua CSCG Group.

- **+** Custom ops can be written in C++ and CUDA and JIT-compiled, per the notebooks
- **+** Runs on Linux and Windows, on x86, ARM and loongson CPUs
- **+** GPU back ends: NVIDIA CUDA, AMD ROCm and Hygon DCU
- **+** Includes a profiler and the Jtune performance tuning tool
- **−** Needs a local C++ compiler (g++ >= 5.4 or clang) at runtime for JIT
- **−** README states Jittor is young and may contain bugs
- **−** Install docs target Python 3.7; last release was 2025-07-28
- **−** Much community material is in Chinese (QQ groups, CN README)

<sub>GPU optional · Docker · Needs Python >= 3.7 (>= 3.8 on Windows), g++ >= 5.4 or clang++, libomp, CUDA >= 10.0 and cuDNN (optional) · Models: image recognition, detection, segmentation, generation, differentiable rendering · [Repo](https://github.com/jittor/jittor) · [📖 Docs ↗](https://cg.cs.tsinghua.edu.cn/jittor/assets/docs/index.html) · [🌐 Site ↗](https://cg.cs.tsinghua.edu.cn/jittor/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jittor/)</sub>

<a name="alphapy"></a>
### #&#8288;260 [alphapy](https://github.com/scottfreellc/alphapy) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (9) · Freshness: recent (70) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Oct 2026</sub>

**Python ML pipeline for tabular models, market analysis and sports prediction.**

AlphaPy is a Python framework built on scikit-learn and pandas that runs model pipelines with Keras, xgboost, LightGBM and CatBoost, and builds blended or stacked ensembles. It adds MarketFlow for market models and trading systems (portfolio analysis via pyfolio) and SportFlow for predicting sporting events. This is the legacy repo; active development has moved to AlphaPy Pro.

- **+** Supports scikit-learn, Keras, xgboost, LightGBM and CatBoost in one pipeline
- **+** Blended and stacked ensembles built in
- **+** Domain pipelines for financial markets (MarketFlow) and sports (SportFlow)
- **+** Installs from PyPI with hosted documentation on Read the Docs
- **−** Legacy edition; README says active development moved to AlphaPy Pro
- **−** Last release was 2020-08-29
- **−** XGBoost does not install automatically via pip on Mac and Windows
- **−** Pyfolio tear sheets may need a manual install from git to avoid an error

<sub>Needs scikit-learn, pandas, pyfolio, XGBoost, LightGBM, CatBoost · Models: scikit-learn, Keras, xgboost, LightGBM, CatBoost · [Repo](https://github.com/scottfreellc/alphapy) · [📖 Docs ↗](http://alphapy.readthedocs.io/en/latest/) · [🌐 Site ↗](https://www.scottfreellc.com/gamept) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/alphapy/)</sub>

<a name="geomstats"></a>
### #&#8288;261 [geomstats](https://github.com/geomstats/geomstats) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (6) · Freshness: recent (70) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · MIT · Nov 2026</sub>

**Python library for statistics and machine learning on Riemannian manifolds.**

Geomstats is a Python package with two modules: geometry, which implements manifolds, Lie groups, fiber bundles, shape spaces, information manifolds and Riemannian metrics, and learning, which provides statistics and ML algorithms such as tangent PCA for data on those manifolds. Computations run on NumPy, Autograd or PyTorch backends, selected with the GEOMSTATS_BACKEND environment variable.

- **+** Same learning algorithms work across the implemented manifolds and metrics
- **+** Switchable NumPy, Autograd or PyTorch backends via one environment variable
- **+** Backed by peer-reviewed papers (JMLR 2020, ACM TOMS 2023 and 2025)
- **+** Installable from PyPI or conda-forge; NumPy-only use needs no optional dependencies
- **−** Visualizations only work with the NumPy backend
- **−** Needs some Riemannian geometry background to choose spaces and metrics
- **−** Last tagged release is 2024-09-09, while commits continue on main
- **−** Niche scope: no general-purpose deep learning layers or model zoo

<sub>GPU optional · Needs Python 3.11+, NumPy, Autograd (optional), PyTorch (optional) · Models: NumPy, Autograd, PyTorch · [Repo](https://github.com/geomstats/geomstats) · [▶️ Demo ↗](https://mybinder.org/v2/gh/geomstats/geomstats/main?filepath=notebooks) · [📖 Docs ↗](https://geomstats.github.io/) · [🌐 Site ↗](https://geomstats.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/geomstats/)</sub>

<a name="deeplearning4j"></a>
### #&#8288;262 [deeplearning4j](https://github.com/deeplearning4j/deeplearning4j) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: widely used (81) · Freshness: slowing (33) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Feb 2026</sub>

**JVM deep learning stack with ND4J tensors, SameDiff autodiff and DataVec ETL.**

Deeplearning4j is a set of JVM libraries for building and training neural networks in Java, Scala or Kotlin. It includes a high-level network API (DL4J), the ND4J array library backed by C++ LibND4J with CPU and CUDA support, the SameDiff autodiff framework, and DataVec for data loading. It imports Keras h5 models and TensorFlow frozen .pb graphs, and trains on Apache Spark.

- **+** Runs natively on the JVM; usable from Java, Scala, Kotlin and Clojure
- **+** ND4J backends cover x86 AVX2/512, ARM, ppc64le and CUDA GPUs
- **+** Imports Keras h5 and TensorFlow frozen .pb models
- **+** Distributed training on Apache Spark; DataVec reads HDFS, CSV, image and audio data
- **−** No release listed; README pins 1.0.0-M2.1, a milestone version
- **−** SameDiff import for ONNX, SavedModel and Keras is listed as planned
- **−** SameDiff is graph-mode only; eager execution is planned
- **−** Tests only run on JDK 11; README lists CUDA 10.x versions

<sub>GPU optional · Needs Maven or other JVM build tool, JavaCPP, Apache Spark (optional) · Models: Keras h5, TensorFlow frozen .pb · [Repo](https://github.com/deeplearning4j/deeplearning4j) · [📖 Docs ↗](https://deeplearning4j.konduit.ai/) · [🌐 Site ↗](https://deeplearning4j.konduit.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deeplearning4j/)</sub>

<a name="face-alignment"></a>
### #&#8288;263 [face-alignment](https://github.com/1adrianb/face-alignment) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: popular (65) · Freshness: recent (59) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · BSD-3-Clause · Apr 2026</sub>

**Python library that detects 2D and 3D facial landmarks with the FAN network.**

PyTorch-based Python package that returns 2D or 3D facial landmarks for images or whole directories, using the FAN face alignment network. Face detection is pluggable: SFD by default, with BlazeFace, YuNet, RetinaFace, SCRFD or precomputed boxes as alternatives. It runs on CPU, CUDA or Apple MPS and compiles the landmark network with torch.compile by default.

- **+** Installs with pip; same API for 2D and 3D landmarks
- **+** Six detector options, with per-detector CPU/MPS timings in the README
- **+** Runs on CPU, CUDA or Apple MPS; bfloat16 and batch size configurable
- **+** Can load precomputed bounding boxes, useful for evaluation
- **−** README recommends the Lua version for numerical evaluation, since it matches the paper's models
- **−** Default SFD detector is slow on CPU (138.8 ms on Apple M2)
- **−** First run with torch.compile takes about 25 seconds
- **−** dlib detector is deprecated; SCRFD needs the extra onnxruntime package

<sub>GPU optional · Docker · Needs PyTorch >=2.0, Python 3.9+, onnxruntime (optional, for SCRFD) · Models: FAN 2D landmarks, FAN 3D landmarks, SFD, BlazeFace, YuNet · [Repo](https://github.com/1adrianb/face-alignment) · [🌐 Site ↗](https://www.adrianbulat.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/face-alignment/)</sub>

<a name="tensorflow-recommenders"></a>
### #&#8288;264 [tensorflow/recommenders](https://github.com/tensorflow/recommenders) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (14) · Freshness: active (90) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Nov 2026</sub>

**Keras-based library for building TensorFlow recommender models.**

TensorFlow Recommenders is a Python library on top of Keras for building recommender models in TensorFlow 2.x. It covers data preparation, model definition, training, evaluation and deployment, with built-in retrieval tasks and factorized top-K metrics. The README's quick start trains a Movielens 100K factorization model with embedding layers in a short script.

- **+** Subclass tfrs.Model and implement compute_loss; works with standard Keras compile and fit
- **+** Built-in Retrieval task and FactorizedTopK metrics for evaluating over a full candidate set
- **+** Installs with pip; tutorials, API reference and a Colab quick start are published
- **+** Apache-2.0 licensed, maintained under the tensorflow GitHub organization
- **−** Tied to TensorFlow 2.x and Keras; no PyTorch or JAX support
- **−** Library only: no serving component or UI, deployment is left to TensorFlow tooling
- **−** Last release (2026-01-23) is older than the latest commit (2026-11-11)
- **−** Quick start covers only a toy retrieval model on Movielens 100K

<sub>GPU optional · Needs TensorFlow 2.x, tensorflow_datasets (for the quick start) · Models: Keras models, Retrieval, Factorization models · [Repo](https://github.com/tensorflow/recommenders) · [📖 Docs ↗](https://www.tensorflow.org/recommenders/api_docs/python/tfrs/) · [🌐 Site ↗](https://www.tensorflow.org/recommenders) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorflow-recommenders/)</sub>

<a name="titans-pytorch"></a>
### #&#8288;265 [titans-pytorch](https://github.com/lucidrains/titans-pytorch) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (14) · Freshness: active (91) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · MIT · Nov 2026</sub>

**Unofficial PyTorch implementation of the Titans neural memory architecture.**

PyTorch implementation of the Titans paper's test-time-learned neural memory, installable as `titans-pytorch`. It provides a standalone `NeuralMemory` layer and a `MemoryAsContextTransformer` (MAC configuration) with persistent and long-term memory tokens. It also holds experiments with memory architectures beyond the paper's 1-4 layer MLP.

- **+** Standalone `NeuralMemory` layer usable separately from the transformer
- **+** Includes a MAC transformer with sampling and a `train_mac.py` experiment script
- **+** Installable from PyPI with `pip install titans-pytorch`
- **+** MIT license, with a Colab notebook for a quick run
- **−** Unofficial implementation, not from the paper's authors
- **−** Research code: no benchmarks or pretrained weights listed
- **−** Training is done by editing `train_mac.py`; no config or CLI
- **−** Documentation is limited to two usage snippets

<sub>Needs PyTorch, uv · [Repo](https://github.com/lucidrains/titans-pytorch) · [▶️ Demo ↗](https://colab.research.google.com/drive/11cGgSABykte3qbK-hjzPgLif3-9UUejm?usp=sharing) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/titans-pytorch/)</sub>

<a name="cleanrl"></a>
### #&#8288;266 [cleanrl](https://github.com/vwxyzjn/cleanrl) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: popular (75) · Freshness: slowing (37) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Apr 2026</sub>

**Single-file PyTorch and JAX implementations of deep RL algorithms.**

CleanRL provides standalone training scripts for PPO, DQN, C51, SAC, DDPG, TD3, PPG, RND and Qdagger, each holding all implementation details in one file (ppo_atari.py is about 340 lines). Scripts log to TensorBoard and optionally Weights and Biases, support seeding and gameplay video capture, and can run on AWS Batch. The README states it is not a modular library and is not meant to be imported.

- **+** Each algorithm variant is one self-contained file, easy to read and modify
- **+** Benchmarked on 7+ algorithms and 34+ games with public W&B reports
- **+** TensorBoard, W&B tracking, seeding and video capture built into the scripts
- **+** Includes JAX variants and envpool-based Atari scripts for faster training
- **−** Not importable as a library; code is duplicated across files by design
- **−** README states Python >=3.7.1,<3.11
- **−** Last release is 2022-11-14; gymnasium migration noted as in progress
- **−** License detected as NOASSERTION while README badge says MIT

<sub>GPU optional · Docker · Needs PyTorch, JAX, Gymnasium, TensorBoard, Weights and Biases, uv, envpool, AWS Batch · Models: PPO, DQN, C51, SAC, DDPG · [Repo](https://github.com/vwxyzjn/cleanrl) · [📖 Docs ↗](https://docs.cleanrl.dev/) · [🌐 Site ↗](https://benchmark.cleanrl.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cleanrl/)</sub>

<a name="pytorchvideo"></a>
### #&#8288;267 [pytorchvideo](https://github.com/facebookresearch/pytorchvideo) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: known (39) · Freshness: recent (70) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Oct 2026</sub>

**PyTorch library of video models, datasets and transforms for research.**

PyTorchVideo is a PyTorch library for video understanding research. It provides a model zoo of pretrained video models (including X3D, SlowFast and Multiscale Vision Transformers), data loaders for video datasets, and video-specific transforms. It installs with pip and includes tutorials and a Hugging Face Spaces demo of X3D.

- **+** Model zoo with pretrained video models and published benchmarks
- **+** Modular components built on PyTorch, so they fit existing PyTorch code
- **+** Data loaders for several video datasets plus video-specific transforms
- **+** Installs with pip install pytorchvideo; tutorials included
- **−** Last PyPI release was 2021-09-10, despite later commits
- **−** Research-oriented; no serving layer or application UI
- **−** README lists only a 2021 update, so newer model coverage is unclear
- **−** No Docker image provided

<sub>Needs PyTorch, Python >=3.7 · Models: X3D, SlowFast, Multiscale Vision Transformers · [Repo](https://github.com/facebookresearch/pytorchvideo) · [▶️ Demo ↗](https://huggingface.co/spaces/pytorch/X3D) · [📖 Docs ↗](https://pytorchvideo.org/docs/tutorial_overview) · [🌐 Site ↗](https://pytorchvideo.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorchvideo/)</sub>

<a name="graphics"></a>
### #&#8288;268 [graphics](https://github.com/tensorflow/graphics) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (27) · Freshness: recent (70) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · Apache-2.0 · Nov 2026</sub>

**Differentiable graphics and geometry layers for TensorFlow, with a 3D TensorBoard plugin.**

TensorFlow Graphics provides differentiable graphics and geometry layers (cameras, reflectance models, spatial transformations, mesh convolutions) that can be inserted into TensorFlow networks. It targets self-supervised 3D vision work using analysis by synthesis. It also includes a TensorBoard plugin for viewing 3D meshes and point clouds, and Colab tutorials covering pose estimation, spherical harmonics and mesh segmentation.

- **+** Functions work in both graph and eager execution
- **+** Colab notebooks for pose estimation, reflectance, spherical harmonics and mesh segmentation
- **+** Optional input-range and normalization checks for debugging during training
- **+** Apache-2.0 licensed, maintained by Google researchers
- **−** Last release was 2019-05-09; the README still lists a differentiable rasterizer as upcoming
- **−** TensorBoard 3D plugin is incompatible with eager execution and TensorFlow 2
- **−** Tutorials are explicitly unstable and not part of the API
- **−** Input checks are off by default and must be enabled manually

<sub>GPU optional · Needs TensorFlow · [Repo](https://github.com/tensorflow/graphics) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/graphics/)</sub>

<a name="evaluate"></a>
### #&#8288;269 [evaluate](https://github.com/huggingface/evaluate) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (23) · Freshness: recent (79) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Oct 2026</sub>

**Python library of standardized ML evaluation metrics and comparisons.**

Hugging Face Evaluate is a Python library that loads metrics with `evaluate.load("accuracy")` and computes scores from predictions and references. It covers dozens of metrics across NLP and computer vision, plus comparisons between models and measurements on datasets. New modules can be scaffolded with `evaluate-cli create` and pushed to a Space on the Hugging Face Hub. The README recommends LightEval for newer LLM evaluation.

- **+** One load/compute interface across dozens of metrics, usable with NumPy, Pandas, PyTorch, TensorFlow, JAX
- **+** Input type checking, and metric cards documenting value ranges and limitations
- **+** Community metrics shared as Hub Spaces, with a CLI template to add your own
- **+** Installs with pip, no server or extra services needed
- **−** README points to LightEval as the more actively maintained option for LLM evaluation
- **−** Last release is 2025-09-18, well behind the latest commit
- **−** Scoring functions only, not an LLM benchmark harness or judge setup
- **−** Sharing modules requires a Hugging Face Hub account and Space

<sub>no GPU · Needs Python, Hugging Face Hub (for community modules and sharing) · Models: Framework-agnostic: NumPy, Pandas, PyTorch, TensorFlow, JAX · [Repo](https://github.com/huggingface/evaluate) · [📖 Docs ↗](https://huggingface.co/docs/evaluate/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/evaluate/)</sub>

<a name="morph-net"></a>
### #&#8288;270 [morph-net](https://github.com/google-research/morph-net) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · Apache-2.0 · Nov 2026</sub>

**TensorFlow library that learns smaller CNN layer widths under FLOP or size limits.**

MorphNet adds a resource regularizer (FLOPs, model size or device-specific latency) to the training loss of a TensorFlow convolutional network. Channels whose influence falls below an alive threshold are marked for removal, and a StructureExporter writes the proposed per-layer channel counts as JSON. You then rebuild the model with those widths and retrain from scratch. The recommended LogisticSigmoid (FiGS) regularizer requires inserting gating ops after prunable layers.

- **+** Targets specific costs: FLOPs, model size or hardware-based latency estimates
- **+** Keeps layer count and connectivity; only output channel counts change
- **+** Gamma and GroupLasso regularizers work without modifying the model, though GroupLasso is deprecated
- **+** Exports learned structure as JSON for retraining without the regularizer
- **−** Examples use TF1 graph APIs (tf.Session, tf.layers); the Keras example is a TODO
- **−** Two-stage workflow: structure learning, then manual rebuild and full retrain
- **−** Recommended regularizer requires adding gating ops to the model
- **−** No tagged release, and the README only covers convolutional image classification

<sub>Needs TensorFlow · Models: convolutional neural networks (TensorFlow) · [Repo](https://github.com/google-research/morph-net) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/morph-net/)</sub>

<a name="hummingbird"></a>
### #&#8288;271 [hummingbird](https://github.com/microsoft/hummingbird) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: known (38) · Freshness: recent (70) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · MIT · Sep 2026</sub>

**Compiles trained scikit-learn, LightGBM and XGBoost models into PyTorch tensor ops.**

Hummingbird converts trained traditional ML models, such as scikit-learn decision trees and random forests and LightGBM and XGBoost classifiers and regressors, into tensor computations. Targets are PyTorch, TorchScript, ONNX and TVM, so the models can run on GPU and be served with TorchServe. It keeps a scikit-learn-style inference API, so a converted model can replace the original with one convert() call.

- **+** One convert(model, 'pytorch') call keeps the sklearn-style predict API unchanged
- **+** Converted tree models run on GPU via model.to('cuda')
- **+** Exports to PyTorch, TorchScript, ONNX and TVM
- **+** Compilation strategies described in OSDI 2020 and PVLDB 2021 papers
- **−** Supports a fixed operator set; other backends and models are only on the roadmap
- **−** Last release was 2024-10-24; tested on Python 3.9 to 3.11 only
- **−** TVM backend only works through Python 3.10
- **−** PyTorch >= 1.6.0 must be installed separately

<sub>GPU optional · Docker · Needs PyTorch >= 1.6.0, scikit-learn, LightGBM (optional), XGBoost (optional) · Models: scikit-learn Decision Trees and Random Forest, LightGBM, XGBoost, PyTorch, TorchScript · [Repo](https://github.com/microsoft/hummingbird) · [📖 Docs ↗](https://microsoft.github.io/hummingbird/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hummingbird/)</sub>

<a name="diffrax"></a>
### #&#8288;272 [diffrax](https://github.com/patrick-kidger/diffrax) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (17) · Freshness: active (92) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · Apache-2.0 · Sep 2026</sub>

**JAX library of ODE, SDE and CDE solvers with autodiff.**

Diffrax provides numerical solvers for ordinary, stochastic and controlled differential equations in JAX. All equation types go through one interface, `diffeqsolve`. It includes explicit solvers such as Tsit5, Dopri5 and Dopri8, plus symplectic and implicit solvers, and offers several adjoint methods for backpropagation.

- **+** Single API covers ODEs, SDEs and CDEs, including neural differential equations
- **+** Autodifferentiable and vmappable, with multiple adjoint methods for backpropagation
- **+** Supports PyTrees as state and dense solutions
- **+** Installs with pip; hosted documentation site
- **−** Requires JAX and Python 3.10+; not usable from other array frameworks
- **−** Aimed at scientific computing, not LLM or generative model workflows
- **−** No benchmarks against other solver libraries in the README

<sub>GPU optional · Needs JAX, Python 3.10+ · [Repo](https://github.com/patrick-kidger/diffrax) · [📖 Docs ↗](https://docs.kidger.site/diffrax) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/diffrax/)</sub>

<a name="bertviz"></a>
### #&#8288;273 [bertviz](https://github.com/jessevig/bertviz) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: popular (67) · Freshness: quiet (11) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · Apache-2.0 · Jan 2026</sub>

**Interactive attention visualizer for Transformer models in Jupyter and Colab.**

BertViz renders attention weights from Hugging Face Transformer models inside Jupyter or Colab notebooks through a Python API. It offers a head view, a model view across all layers and heads, and a neuron view of query/key vectors. Encoder-decoder models are supported in the head and model views.

- **+** Three views: per-layer head view, all-layer model view, and neuron view of query/key vectors
- **+** Works with most Hugging Face models that return attention via output_attentions=True
- **+** Handles encoder, decoder and cross attention for models such as BART and MarianMT
- **+** Can export visualizations as standalone HTML via html_action='return'
- **−** Designed for short inputs; slow on long text or large models
- **−** Neuron view only works with bundled custom BERT, GPT-2 and RoBERTa
- **−** Needs a notebook environment; Colab can disconnect on long inputs
- **−** Attention weights are not necessarily an explanation of predictions, per the README

<sub>GPU optional · Needs Jupyter, ipywidgets, Hugging Face transformers · Models: Hugging Face Transformers, BERT, GPT-2, RoBERTa, BART · [Repo](https://github.com/jessevig/bertviz) · [▶️ Demo ↗](https://colab.research.google.com/drive/1hXIQ77A4TYS4y3UthWF-Ci7V7vVUoxmQ?usp=sharing) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bertviz/)</sub>

<a name="gym-pybullet-drones"></a>
### #&#8288;274 [gym-pybullet-drones](https://github.com/learnsyslab/gym-pybullet-drones) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (18) · Freshness: recent (70) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · MIT · Nov 2026</sub>

**PyBullet quadcopter simulator with Gymnasium environments for RL and control.**

A Python simulation of one or many quadcopters on PyBullet physics, exposed as Gymnasium environments. It includes PID, velocity and MRAC controller examples, a downwash effect demo, and PPO training scripts using Stable-Baselines3 for single and multi-drone hover. A PettingZoo wrapper supports MARL libraries, and Betaflight SITL can be run on Ubuntu.

- **+** Works with Gymnasium, Stable-Baselines3 2.0 and a PettingZoo Parallel API wrapper
- **+** Ships classical control examples (PID, MRAC) beside RL examples
- **+** Models multi-drone aerodynamics such as downwash
- **+** Betaflight SITL example runs one executable per drone
- **−** No pre-built pybullet wheel beyond Python 3.10; needs a compiler to install
- **−** Betaflight SITL example is Ubuntu only
- **−** Last tagged release is from 2021; development happens on the main branch
- **−** Motor delay and advanced ESC modeling are still unimplemented TODOs

<sub>Needs pybullet, gymnasium, stable-baselines3, PettingZoo, Betaflight SITL (optional), gcc · [Repo](https://github.com/learnsyslab/gym-pybullet-drones) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gym-pybullet-drones/)</sub>

<a name="weighted-boxes-fusion"></a>
### #&#8288;275 [weighted-boxes-fusion](https://github.com/zfturbo/weighted-boxes-fusion) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (10) · Freshness: recent (70) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Nov 2026</sub>

**Python library for ensembling bounding boxes from multiple object detection models.**

ensemble-boxes is a Python package that merges predictions from several object detection models using NMS, Soft-NMS, Non-maximum weighted and Weighted Boxes Fusion (WBF). WBF also has 3D, 1D line-segment, rotated-box and quadrangle variants. Inputs are normalized box coordinates, scores and labels per model, with optional per-model weights.

- **+** Four ensembling methods behind one call signature: nms, soft_nms, non_maximum_weighted, weighted_boxes_fusion
- **+** WBF variants for 3D, 1D segments, rotated and quadrangle boxes
- **+** Installs with pip; requires only Numpy and Numba
- **+** Benchmarks provided for Open Images, COCO and an NLP dataset
- **−** Boxes must be pre-normalized to [0, 1] in x1, y1, x2, y2 order
- **−** Rotated boxes need the same scale on both axes, or a square image
- **−** Last tagged release is from 2022-03-24
- **−** Library only; no model inference or training included

<sub>no GPU · Needs Numpy, Numba · Models: object detection box outputs (boxes, scores, labels) · [Repo](https://github.com/zfturbo/weighted-boxes-fusion) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/weighted-boxes-fusion/)</sub>

<a name="implicit"></a>
### #&#8288;276 [implicit](https://github.com/benfred/implicit) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (41) · Freshness: recent (70) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · MIT · May 2026</sub>

**Python library for recommender systems on implicit feedback data.**

Implicit provides Python implementations of ALS, Bayesian Personalized Ranking, Logistic Matrix Factorization and item-item nearest neighbour models (cosine, TFIDF, BM25) for implicit feedback datasets. Training is multi-threaded on CPU via Cython and OpenMP, and ALS and BPR also have custom CUDA kernels. Annoy, NMSLIB or Faiss can be plugged in to speed up recommendation lookups.

- **+** Multi-threaded CPU training using Cython and OpenMP across all cores
- **+** Custom CUDA kernels for ALS and BPR on GPU
- **+** Prebuilt pip wheels for x86_64 Linux, Windows and OSX; conda packages available
- **+** Optional Annoy, NMSLIB or Faiss integration for faster recommendations
- **−** Limited to implicit-feedback collaborative filtering; no explicit-rating or deep-learning recommenders
- **−** GPU support requires CUDA Toolkit 13 and a separate rmm-cu13 install
- **−** Prebuilt wheels listed only for x86_64; other architectures not mentioned
- **−** CPU speed depends on tuning BLAS threads, such as OPENBLAS_NUM_THREADS=1

<sub>GPU optional · Needs SciPy, NVIDIA CUDA Toolkit 13 (GPU only), rmm-cu13 (GPU only), Annoy/NMSLIB/Faiss (optional) · Models: Alternating Least Squares, Bayesian Personalized Ranking, Logistic Matrix Factorization, Item-item nearest neighbours (cosine, TFIDF, BM25) · [Repo](https://github.com/benfred/implicit) · [📖 Docs ↗](https://benfred.github.io/implicit/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/implicit/)</sub>

<a name="helm"></a>
### #&#8288;277 [helm](https://github.com/stanford-crfm/helm) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (30) · Freshness: recent (76) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · Apache-2.0 · Jun 2026</sub>

**Python framework for reproducible benchmarking of LLMs and multimodal models.**

HELM is a Python framework from Stanford CRFM that runs standardized benchmarks (e.g. MMLU-Pro, GPQA, IFEval, WildBench) against models from providers such as OpenAI, Anthropic and Google through one interface. It scores more than accuracy, including efficiency, bias and toxicity, and ships a local web UI for inspecting prompts and responses. The project entered maintenance mode on June 1, 2026.

- **+** Covers text, vision-language, text-to-image and audio-language evaluations, with published leaderboards
- **+** Three-step CLI: helm-run, helm-summarize, helm-server for local results browsing
- **+** Metrics go beyond accuracy: efficiency, bias and toxicity
- **+** Can reproduce results from the associated papers, per the docs
- **−** In maintenance mode since June 1, 2026, so expect limited new features
- **−** Evaluation only; does not serve or train models
- **−** Setup details live in external docs, not the README

<sub>Models: OpenAI, Anthropic Claude, Google Gemini · port 8000 · [Repo](https://github.com/stanford-crfm/helm) · [▶️ Demo ↗](https://crfm.stanford.edu/helm/) · [📖 Docs ↗](https://crfm-helm.readthedocs.io/) · [🌐 Site ↗](https://crfm.stanford.edu/helm/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/helm/)</sub>

<a name="finrl-meta"></a>
### #&#8288;278 [finrl-meta](https://github.com/ai4finance-foundation/finrl-meta) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (13) · Freshness: recent (70) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · MIT · Nov 2026</sub>

**Market environments and data pipelines for financial reinforcement learning research.**

FinRL-Meta is a Python library that provides market environments and a data layer for training and benchmarking reinforcement learning trading agents. It pulls data from 12 listed sources, including Yahoo Finance, Alpaca, Binance, CCXT and several Chinese market APIs, and adds technical indicators. Agents from ElegantRL, Stable-Baselines3 and RLlib plug into the same environments, so results can be compared on one dataset.

- **+** Unified data layer over 12 sources covering US, China and crypto markets
- **+** Works with ElegantRL, Stable-Baselines3 and RLlib agents in the same environments
- **+** Train/test/trade split is meant to limit information leakage and allow fair comparisons
- **+** Colab notebook demonstrates plugging agents into the environments
- **−** Last release was June 2022, so the packaged version is old
- **−** README badge lists Python 3.6, which is long out of support
- **−** Covers only data and environment layers; production trading moved to FinRL-X
- **−** Several data sources need paid or account-specific API access

<sub>GPU optional · Docker · Needs Akshare, Alpaca, Baostock, Binance, CCXT, IEXCloud, JoinQuant, QuantConnect, RiceQuant, Tushare, WRDS, yfinance · Models: ElegantRL, Stable-Baselines3, RLlib · [Repo](https://github.com/ai4finance-foundation/finrl-meta) · [▶️ Demo ↗](https://colab.research.google.com/github/AI4Finance-Foundation/FinRL-Meta/blob/main/Demo_Plug_and_Play_with_DRL_Libraries.ipynb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/finrl-meta/)</sub>

<a name="slowfast"></a>
### #&#8288;279 [slowfast](https://github.com/facebookresearch/slowfast) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: popular (65) · Freshness: slowing (40) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Mar 2026</sub>

**PyTorch codebase for training video classification and detection backbones.**

PySlowFast is FAIR's PyTorch codebase for video understanding research. It implements SlowFast, I3D, C2D, Non-local, X3D, MViTv1/v2 and Rev-ViT/Rev-MViT backbones, plus self-supervised methods such as MaskFeat and MAE for video. It ships a model zoo of baselines and trained weights, and visualization tools for training, evaluation and inference.

- **+** Covers many video backbones (SlowFast, X3D, MViTv2, Rev-ViT) in one codebase
- **+** Includes self-supervised recipes: MaskFeat, MAE for video, contrastive SSL
- **+** Model zoo with baseline results and downloadable trained weights
- **+** Supports multigrid training and PyTorchVideo models and datasets
- **−** Research code; no tagged release published
- **−** Datasets must be prepared manually following DATASET.md
- **−** No Docker or compose files provided
- **−** README gives no hardware requirements for training

<sub>Needs PyTorch, PyTorchVideo · Models: SlowFast, Slow, C2D, I3D, Non-local · [Repo](https://github.com/facebookresearch/slowfast) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/slowfast/)</sub>

<a name="ml-ane-transformers"></a>
### #&#8288;280 [ml-ane-transformers](https://github.com/apple-aiml-research/ml-ane-transformers) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (26) · Freshness: recent (70) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · custom license · Sep 2026</sub>

**Reference PyTorch Transformer code optimized for the Apple Neural Engine.**

A Python package with a standalone reference Transformer implementation and ANE-optimized Hugging Face DistilBERT classes. The README walks through tracing the model with TorchScript and converting it to a Core ML mlprogram with coremltools. Apple reports up to 10x lower latency and 14x lower peak memory versus baseline on A14/M1 or newer; the tutorial case (seq length 128, batch 1) shows 2.84x.

- **+** Equivalent DistilBERT that loads baseline Hugging Face weights via load_state_dict
- **+** Tutorial covers the full path: trace, coremltools conversion, Xcode performance report
- **+** Backed by a published Apple research article with latency and memory data
- **+** Installs with pip install ane_transformers
- **−** Only DistilBERT is shown as a Hugging Face example
- **−** Targets A14/M1 or newer; speed-up tests only warn on other devices
- **−** Last release was 2022-08-09; README benchmarks use iOS 16.0
- **−** License is not identified (NOASSERTION)

<sub>Needs PyTorch, transformers, coremltools, Xcode · Models: DistilBERT, Core ML mlprogram, TorchScript · [Repo](https://github.com/apple-aiml-research/ml-ane-transformers) · [🌐 Site ↗](https://machinelearning.apple.com/research/apple-neural-engine) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ml-ane-transformers/)</sub>

<a name="ampligraph"></a>
### #&#8288;281 [ampligraph](https://github.com/accenture/ampligraph) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (19) · Freshness: active (87) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Jul 2026</sub>

**TensorFlow 2 library for knowledge graph embeddings and link prediction.**

AmpliGraph trains knowledge graph embedding models (TransE, DistMult, ComplEx, HolE, RotatE) through a Keras-style API on TensorFlow 2. It predicts missing links between entities and produces standalone embeddings. Submodules cover dataset loading, evaluation metrics such as filtered MRR, and discovery helpers for clustering entities and finding near duplicates.

- **+** Keras-style API in AmpliGraph 2 reduces code needed to train link-prediction models
- **+** Reports filtered MRR on FB15K-237, WN18RR, YAGO3-10, FB15k and WN18
- **+** Runs on CPU or GPU; pip install on Linux, macOS and Windows
- **+** Base estimators can be extended to build custom embedding models
- **−** Python 3.9 to 3.11 only, per the stated prerequisites
- **−** AmpliGraph 2 dropped ConvE and ConvKB, which exist only in 1.x
- **−** Library only: no server, UI or LLM integration
- **−** Reported MRR is below the cited literature results on FB15K-237, FB15k and WN18

<sub>GPU optional · Needs TensorFlow 2, Python 3.9-3.11 · Models: TransE, DistMult, ComplEx, HolE, RotatE · [Repo](https://github.com/accenture/ampligraph) · [📖 Docs ↗](http://docs.ampligraph.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ampligraph/)</sub>

<a name="tensortrade"></a>
### #&#8288;282 [tensortrade](https://github.com/tensortrade-org/tensortrade) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: popular (64) · Freshness: slowing (40) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Feb 2026</sub>

**Python framework for training reinforcement learning agents on trading environments.**

TensorTrade provides composable pieces for RL trading: environments, action schemes (default Buy/Sell/Hold), reward schemes (default Position-Based Returns), observers, data feeds, and a simulated exchange with configurable commission. Training scripts use Ray RLlib and Optuna. The README reports PPO agents on BTC/USD beating buy-and-hold at 0% commission but losing at 0.1%.

- **+** Swappable action, reward, observer and exchange components with documented defaults
- **+** Example scripts for Ray RLlib training and Optuna hyperparameter search
- **+** Tutorial curriculum plus a published experiments log with negative results
- **+** Simulated exchange has configurable commission for testing cost sensitivity
- **−** README results show the agent losing to buy-and-hold at 0.1% commission
- **−** Python version stated inconsistently: 3.12+ in badge and quick start, 3.11 or 3.12 in install
- **−** Simulation only; README describes no live trading or broker integration
- **−** Install pins and TensorFlow/NumPy conflicts are listed in troubleshooting

<sub>GPU optional · Docker · Needs Ray RLlib, Optuna, TensorFlow, Jupyter · Models: PPO · [Repo](https://github.com/tensortrade-org/tensortrade) · [📖 Docs ↗](https://www.tensortrade.org/en/latest/) · [🌐 Site ↗](https://www.tensortrade.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensortrade/)</sub>

<a name="habitat-lab"></a>
### #&#8288;283 [habitat-lab](https://github.com/facebookresearch/habitat-lab) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: known (33) · Freshness: recent (70) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · MIT · May 2026</sub>

**Python library for training embodied AI agents in simulated indoor scenes.**

Habitat-Lab is a Python library for defining embodied AI tasks (navigation, rearrangement, instruction following, question answering, human following) and training agents on them in Habitat-Sim. It configures robots and humanoids with sensors, and ships PPO reinforcement learning baselines in habitat-baselines plus a human-in-the-loop framework. Meta stopped official development after v0.3.4.

- **+** Covers single and multi-agent tasks, with YAML configs and command-line overrides
- **+** Supports commercial robots and humanoids with configurable sensors and capabilities
- **+** Includes PPO baselines and standard benchmark metrics in habitat-baselines
- **+** Exposes tasks through a Gym interface, e.g. gym.make("HabitatRenderPick-v0")
- **−** No official development or maintenance by Meta beyond v0.3.4
- **−** Requires Habitat-Sim from conda, with Python 3.9 and cmake 3.14 or newer
- **−** Interactive example fails on Ubuntu 20.04 with an X BadAccess error
- **−** Matterport3D and Gibson datasets and models are under non-commercial CC BY-NC-SA terms

<sub>Docker · Needs habitat-sim, conda, cmake>=3.14, Python 3.9 · Models: PPO (reinforcement learning baselines) · [Repo](https://github.com/facebookresearch/habitat-lab) · [▶️ Demo ↗](https://aihabitat.org/demo) · [📖 Docs ↗](https://aihabitat.org/docs/habitat-lab/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/habitat-lab/)</sub>

<a name="robosuite"></a>
### #&#8288;284 [robosuite](https://github.com/arise-initiative/robosuite) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (25) · Freshness: recent (75) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · custom license · Jul 2026</sub>

**MuJoCo-based robot learning simulator with benchmark manipulation tasks.**

robosuite is a Python simulation framework built on the MuJoCo physics engine for robot learning research. It provides standardized manipulation benchmark tasks, modular APIs for composing robots, arenas and objects into new environments, and several controller types including operational space and whole body control. Version 1.5 added humanoid embodiments, custom robot composition, more teleoperation devices and photorealistic rendering.

- **+** Standardized manipulation benchmark tasks with RL results for reproducible comparisons
- **+** Modular APIs to compose robots, arenas and parameterized objects into new environments
- **+** Multiple controllers: joint velocity, inverse kinematics, operational space, whole body
- **+** Keyboard, SpaceMouse and viewer drag-drop teleoperation plus demonstration collection
- **−** Simulation only; no real-robot deployment described
- **−** Depends on MuJoCo; photorealistic rendering needs extra tools such as Isaac Sim
- **−** No Docker image or compose setup
- **−** License is not identified by detection (NOASSERTION)

<sub>Needs MuJoCo · [Repo](https://github.com/arise-initiative/robosuite) · [📖 Docs ↗](https://robosuite.ai/docs/overview.html) · [🌐 Site ↗](https://robosuite.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/robosuite/)</sub>

<a name="tsne-cuda"></a>
### #&#8288;285 [tsne-cuda](https://github.com/cannylab/tsne-cuda) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (13) · Freshness: active (91) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · BSD-3-Clause · Jul 2026</sub>

**CUDA implementation of t-SNE with a scikit-learn-style Python API.**

TSNE-CUDA is a GPU port of the FIt-SNE algorithm, exposed through Python wrappers that follow the sklearn.manifold.TSNE interface and also usable as a C++ library. The README reports up to 1200x speedup over scikit-learn and up to 50x over Multicore-TSNE, with MNIST (60,000 points) embedded in under 7 seconds. Only two-dimensional output is supported.

- **+** Drop-in API matching sklearn.manifold.TSNE: fit_transform(X)
- **+** Benchmarked in a published paper (JPDC 2019) against sklearn, BH-TSNE and Multicore-TSNE
- **+** Usable from Python or as a C++ library
- **+** Conda binaries available for CUDA 10.1 and 10.2
- **−** Only n_components=2 is supported, with no plans for more dimensions
- **−** Requires an NVIDIA CUDA GPU; no CPU fallback is described
- **−** Conda binaries cover only CUDA 10.1/10.2; newer CUDA needs a source build
- **−** Bundles components under other licenses (FAISS, Lonestar GPU, others)

<sub>GPU required · Needs CUDA, FAISS · [Repo](https://github.com/cannylab/tsne-cuda) · [📖 Docs ↗](https://github.com/CannyLab/tsne-cuda/wiki/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tsne-cuda/)</sub>

<a name="openmldb"></a>
### #&#8288;286 [openmldb](https://github.com/4paradigm/openmldb) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (7) · Freshness: recent (70) · Maintenance: weak (26) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · Apache-2.0 · Nov 2026</sub>

**SQL feature platform giving consistent ML features for training and inference.**

OpenMLDB is a C++ database for ML feature engineering. Features are written once in extended SQL (for example LAST JOIN and WINDOW UNION), run offline on a tailored Spark distribution, and deployed online with one command to a real-time SQL engine built for time-series data. A shared execution plan generator keeps offline and online results consistent.

- **+** One SQL definition serves both offline training and online inference, avoiding a rewrite for production
- **+** Real-time engine reports millisecond latency, with benchmarks in a VLDB 2021 paper
- **+** Connectors and plugins for Kafka, Pulsar, RocketMQ, Airflow, DolphinScheduler and Byzer
- **+** Includes distributed storage, fault recovery, high availability and monitoring
- **−** Last tagged release is February 2025, well behind recent commits
- **−** Unrelated to LLMs; targets tabular and time-series features, not generative AI
- **−** Offline batch engine needs a custom Spark build, adding operational weight
- **−** Features must be expressed in SQL dialect extensions, which means learning the extra syntax

<sub>Docker · Needs Tailored Spark distribution (batch engine) · [Repo](https://github.com/4paradigm/openmldb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmldb/)</sub>

<a name="neuralgcm"></a>
### #&#8288;287 [neuralgcm](https://github.com/neuralgcm/neuralgcm) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (1) · Freshness: recent (75) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · Apache-2.0 · Nov 2026</sub>

**Python library for hybrid ML/physics weather and climate models.**

NeuralGCM is a Python library for building hybrid atmospheric models that combine machine-learned components with physics-based simulation, for weather and climate prediction. Code is Apache-2.0, and trained model weights are released separately under CC BY-SA 4.0. The README is short and points to a paper and hosted documentation for usage.

- **+** Combines ML components with physics-based atmospheric simulation in one Python library
- **+** Trained model weights are published alongside the code
- **+** Paper and hosted documentation cover the method and API
- **−** Weights are CC BY-SA 4.0, with share-alike terms unlike the Apache-2.0 code
- **−** Specific to atmospheric modeling, not a general-purpose ML library
- **−** Last tagged release is July 2025, well behind recent commits
- **−** README has no install steps or example; usage is only in the docs

<sub>Models: NeuralGCM trained weights (CC BY-SA 4.0) · [Repo](https://github.com/neuralgcm/neuralgcm) · [📖 Docs ↗](https://neuralgcm.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/neuralgcm/)</sub>

<a name="gensim"></a>
### #&#8288;288 [gensim](https://github.com/piskvorky/gensim) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: widely used (84) · Freshness: quiet (11) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · LGPL-2.1 · Oct 2025</sub>

**Python library for topic modelling and document similarity on large corpora.**

Gensim implements streamed, out-of-core versions of LSA/LSI, LDA, Random Projections, HDP and word2vec, plus document indexing and similarity retrieval. Corpora are read through Python generators, so input can exceed RAM. Heavy computation goes through NumPy and BLAS. The project is in stable maintenance mode: bug and documentation fixes only, no new features.

- **+** Memory-independent streaming: processes corpora larger than RAM via generators
- **+** Multicore LSA, LDA, HDP, Random Projections and word2vec implementations
- **+** LSA and LDA can run distributed on a cluster of computers
- **+** Simple streaming and transformation APIs for custom corpora and algorithms
- **−** Maintenance mode: no new features accepted
- **−** Classic topic models and word2vec only; no transformer or LLM tooling in the README
- **−** Speed depends on a fast BLAS; building NumPy from source is non-trivial
- **−** Python 2.7 support dropped after 3.8.3

<sub>no GPU · Needs NumPy, BLAS (MKL, ATLAS or OpenBLAS recommended) · Models: LSA/LSI, LDA, HDP, Random Projections, word2vec · [Repo](https://github.com/piskvorky/gensim) · [📖 Docs ↗](https://radimrehurek.com/gensim/auto_examples/) · [🌐 Site ↗](https://radimrehurek.com/gensim/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gensim/)</sub>

<a name="flow-forecast"></a>
### #&#8288;289 [flow-forecast](https://github.com/aistream-peelout/flow-forecast) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (20) · Freshness: recent (66) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · GPL-3.0 · Aug 2026</sub>

**Deep learning library for time series forecasting, classification and anomaly detection.**

Flow Forecast is a Python framework for training deep learning models on time series data. It includes LSTM, GRU, several transformer variants (Informer, Crossformer, Inverted Transformer), DeepAR, DLinear, TSMixer and Anomaly Transformer. It integrates with Google Cloud Platform and Weights and Biases, and installs with `pip install flood-forecast`.

- **+** Lists 17 models, from LSTM and GRU to Informer, Crossformer and TSMixer
- **+** Covers forecasting, classification and anomaly detection in one framework
- **+** Weights and Biases and Google Cloud Platform integrations are built in
- **+** Installs from PyPI with a single pip command
- **−** Last release was 2022-05-10, so the PyPI package may lag the master branch
- **−** Docs live on Confluence and a wiki, not in the repository
- **−** GPL-3.0 license restricts use in closed-source products
- **−** PyPI package name (flood-forecast) differs from the repo name

<sub>Needs Google Cloud Platform (optional), Weights and Biases (optional) · Models: LSTM, GRU, Transformer, Informer, DeepAR · [Repo](https://github.com/aistream-peelout/flow-forecast) · [📖 Docs ↗](https://flow-forecast.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flow-forecast/)</sub>

<a name="singa"></a>
### #&#8288;290 [singa](https://github.com/apache/singa) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: known (39) · Freshness: recent (57) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Jul 2026</sub>

**Distributed deep learning system with a C++ core.**

Apache SINGA is a distributed deep learning system written mainly in C++, maintained under the Apache Software Foundation. The README gives only a one-line description and points to the website for installation and to an examples directory. CI badges cover Ubuntu, macOS and conda builds, and a Docker Hub image is linked.

- **+** Apache Software Foundation project under the Apache-2.0 license
- **+** CI builds on Ubuntu and macOS, with conda packages and a Docker Hub image
- **+** Examples directory and hosted installation docs
- **+** Repository still active: last commit 2026-07-07
- **−** Last tagged release was 2020-04-21, so releases lag the main branch
- **−** README gives no feature list, supported hardware or model formats
- **−** Far smaller community than PyTorch or TensorFlow, at about 3.6k stars
- **−** Issues are tracked in JIRA rather than GitHub

<sub>[Repo](https://github.com/apache/singa) · [📖 Docs ↗](http://singa.apache.org/docs/installation/) · [🌐 Site ↗](http://singa.apache.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/singa/)</sub>

<a name="graphembedding"></a>
### #&#8288;291 [graphembedding](https://github.com/shenweichen/graphembedding) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: known (41) · Freshness: recent (52) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · MIT · Apr 2026</sub>

**Python graph embedding library: DeepWalk, LINE, Node2Vec, SDNE, Struc2Vec.**

A Python library that learns node embeddings from a networkx graph, following a "graph in, embedding out" design. It implements five published methods: DeepWalk, LINE, Node2Vec, SDNE and Struc2Vec. Each model is initialised with a graph, trained with train(), and returns vectors through get_embeddings().

- **+** Five classic embedding methods share one init/train/get_embeddings interface
- **+** Reads plain networkx graphs from edge-list files, with optional edge weights
- **+** Example scripts included, run after pip install -e .[tf]
- **+** MIT license
- **−** No tagged release; install is from a cloned repo only
- **−** Covers only 2014-2017 methods; no GNN-based or newer embedding models
- **−** Docs are README snippets; linked method write-ups are in Chinese

<sub>Needs networkx, TensorFlow (tf extra) · Models: DeepWalk, LINE, Node2Vec, SDNE, Struc2Vec · [Repo](https://github.com/shenweichen/graphembedding) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/graphembedding/)</sub>

<a name="nuscenes-devkit"></a>
### #&#8288;292 [nuscenes-devkit](https://github.com/nutonomy/nuscenes-devkit) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: niche (27) · Freshness: recent (65) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · custom license · Aug 2026</sub>

**Python devkit for loading and evaluating the nuScenes and nuImages driving datasets.**

Python SDK for the nuScenes and nuImages autonomous-driving datasets from Motional. It provides database classes, lidar/radar/camera tooling, map expansion APIs, and evaluation code for detection, tracking, prediction, lidarseg and panoptic tasks. Datasets are downloaded separately after account registration and acceptance of the Terms of Use.

- **+** Covers detection, tracking, prediction, lidarseg and panoptic evaluation code in one package
- **+** Installable with pip install nuscenes-devkit; tested on Python 3.9 and 3.12
- **+** Jupyter tutorials for nuScenes, nuImages, maps, CAN bus, prediction and lidarseg/panoptic
- **+** Map expansion API with 11 semantic layers and lane connectivity for prediction
- **−** Datasets require account registration and Terms of Use acceptance; they are not bundled
- **−** nuScenes needs all archives downloaded for the devkit to work
- **−** Last tagged release is from 2021 per repo metadata, though the README lists v1.2.0
- **−** License is reported as NOASSERTION, so terms need manual checking

<sub>no GPU · Needs nuScenes or nuImages dataset download, Jupyter (for tutorials) · [Repo](https://github.com/nutonomy/nuscenes-devkit) · [📖 Docs ↗](https://github.com/nutonomy/nuscenes-devkit/blob/master/docs/installation.md) · [🌐 Site ↗](https://www.nuscenes.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nuscenes-devkit/)</sub>

<a name="aix360"></a>
### #&#8288;293 [aix360](https://github.com/trusted-ai/aix360) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: niche (9) · Freshness: recent (70) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Sep 2026</sub>

**Python library of explainability algorithms and metrics for ML models and data.**

AI Explainability 360 is a Python package from IBM Research that bundles explainability algorithms for tabular, text, image and time series data. It covers data explanations, local and global post-hoc methods, directly interpretable models (BRCG, GLRM, Ripper, CoFrNets), LIME and SHAP, plus faithfulness and monotonicity metrics. Algorithms install separately through pip extras, with example notebooks and a taxonomy to help choose.

- **+** Broad algorithm set: ProtoDash, CEM, BRCG, GLRM, Ripper, ProfWeight, time-series LIME and saliency
- **+** Per-algorithm pip extras limit installed dependencies to what you use
- **+** Tutorials, example notebooks and a taxonomy tree help pick an explainer
- **+** Dockerfile starts JupyterLab on port 8888 for the tutorials
- **−** Python requirements differ per algorithm (3.6, 3.7, 3.10), so some extras cannot share an environment
- **−** Last release is v0.3.0 from 2023-07
- **−** LLM explainability lives in the separate ICX360 toolkit, not here
- **−** IMD is not supported on Windows; some extras pin end-of-life Python versions

<sub>Docker · Needs TensorFlow, PyTorch, scikit-learn, conda (recommended), cmake (for some extras) · Models: tabular, text, image, time series · port 8888 · [Repo](https://github.com/trusted-ai/aix360) · [📖 Docs ↗](https://aix360.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aix360/)</sub>

<a name="deepo"></a>
### #&#8288;294 [deepo](https://github.com/ufoym/deepo) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: popular (60) · Freshness: slowing (31) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Mar 2026</sub>

**Dockerfile generator and prebuilt images for deep learning environments.**

Deepo generates Dockerfiles for deep learning environments from one command, resolving compatible CUDA, cuDNN, Python and framework versions and ordering installs by topological sort. It also publishes prebuilt Docker Hub images: an all-in-one image with TensorFlow, PyTorch, Keras, MXNet, Chainer, Darknet and PaddlePaddle, plus per-framework tags for CUDA 11.3 and CPU-only.

- **+** Generator resolves CUDA, cuDNN, Python and framework compatibility and install order automatically
- **+** Per-framework tags let you pull one framework instead of the all-in-one image
- **+** CPU-only images run on Linux, Windows and macOS; GPU images run on Linux
- **+** Jupyter Lab can be launched from the same image on port 8888
- **−** Current tags target only CUDA 11.3 and Python 3.8, which are old
- **−** Last release is 2017-11-27; Theano, Caffe, CNTK and Torch tags are deprecated
- **−** Custom builds compile some libraries from source and can take several minutes
- **−** GPU use requires the NVIDIA Container Toolkit on the host

<sub>GPU optional · Docker · Needs Docker, NVIDIA Container Toolkit (GPU only) · Models: TensorFlow, PyTorch, Keras, MXNet, Chainer · port 8888 · [Repo](https://github.com/ufoym/deepo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepo/)</sub>

<a name="orbit"></a>
### #&#8288;295 [orbit](https://github.com/uber/orbit) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (15) · Freshness: recent (75) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · custom license · May 2026</sub>

**Python library for Bayesian time series forecasting with a fit-predict API.**

Orbit is a Python package from Uber for probabilistic time series forecasting. It exposes an initialize-fit-predict interface over Stan-based models: ETS, LGT, DLT and KTR. Estimation can use MCMC, MAP or variational inference. It is a statistical forecasting library, not an LLM tool.

- **+** Four model families (ETS, LGT, DLT, KTR) behind one fit/predict interface
- **+** Three estimation modes: MCMC, MAP and variational inference
- **+** Installable from PyPI or conda-forge, with Colab tutorials and M3 backtest example
- **−** Requires cmdstanpy for Bayesian sampling, adding a Stan toolchain dependency
- **−** README says some experimental code has APIs subject to change
- **−** Covers time series forecasting only, with no deep learning models
- **−** Default page is the dev branch; stable code lives on master

<sub>Docker · Needs cmdstanpy, Stan, Pyro · Models: ETS, LGT, DLT, KTR · [Repo](https://github.com/uber/orbit) · [▶️ Demo ↗](https://colab.research.google.com/github/edwinnglabs/ts-playground/blob/master/Orbit_Tutorial.ipynb) · [📖 Docs ↗](https://orbit-ml.readthedocs.io/en/stable/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/orbit/)</sub>

<a name="webdnn"></a>
### #&#8288;296 [webdnn](https://github.com/mil-tokyo/webdnn) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (14) · Freshness: recent (62) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · custom license · Jul 2026</sub>

**In-browser neural network inference for ONNX models via WebGPU, WebGL and WebAssembly.**

WebDNN 2.x is a TypeScript library that loads ONNX models directly in the browser and runs inference on WebGPU (WGSL), WebGL2 with a WebGL1 fallback, or WebAssembly. Models can be loaded unoptimized without Python preprocessing, or optimized offline with a Python transpiler for use with a smaller core bundle. Operators ship as separate bundles loaded at runtime.

- **+** Loads ONNX files directly in the browser, no Python step required
- **+** Three backends: WebGPU, WebGL2 (WebGL1 fallback), and WebAssembly
- **+** Optional offline optimizer produces models for the smaller webdnn-core.js bundle
- **+** Operator bundles load dynamically; TypeScript type declarations are included
- **−** WebAssembly backend is not in build:all and needs an emscripten 3.1+ build
- **−** No prebuilt dist in the README; you must build from source with Node 20+
- **−** Optimizer and fixture generation require Python 3.10+ with uv
- **−** License is reported as NOASSERTION; last release was 2024-12-01

<sub>GPU optional · Needs Node.js 20+, Python 3.10+ with uv (optimizer only), emscripten 3.1+ (WebAssembly backend only) · Models: ONNX · port 8080 · [Repo](https://github.com/mil-tokyo/webdnn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/webdnn/)</sub>

<a name="mish"></a>
### #&#8288;297 [mish](https://github.com/digantamisra98/mish) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (4) · Freshness: active (86) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Jul 2026</sub>

**Reference code and benchmarks for the Mish activation function.**

Research repository for Mish, the activation f(x) = x·tanh(softplus(x)), from the BMVC 2020 paper. It collects ImageNet and MS-COCO results, loss landscape visualizations, DarkNet cfg files with pretrained weights, PyTorch benchmarks, and a list of frameworks that adopted Mish. It is a reference and benchmark collection, not an installable library.

- **+** DarkNet cfg files and weights for ResNet-50, DarkNet-53, DenseNet-201 and ResNeXt-50 with Mish
- **+** Ablation tables compare Mish with Swish, ReLU and Leaky ReLU on several CSP networks
- **+** Links a PyTorch benchmarks folder, a CUDA version and a Weights & Biases integration
- **+** Lists framework adoptions, including PyTorch, MXNet, TF.js and OpenVINO
- **−** Not a packaged library; Mish is now built into major frameworks
- **−** Pretrained weights are hosted on Google Drive links, which can break
- **−** Benchmarks date from 2019-2020 and use older architectures
- **−** README is mostly changelog and media coverage, with little usage guidance

<sub>GPU optional · Needs DarkNet (AlexeyAB), PyTorch · Models: DarkNet cfg, PyTorch · [Repo](https://github.com/digantamisra98/mish) · [▶️ Demo ↗](https://losslandscape.com/explorer?model=mish) · [📖 Docs ↗](https://arxiv.org/abs/1908.08681v3) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mish/)</sub>

<a name="pinns"></a>
### #&#8288;298 [pinns](https://github.com/maziarraissi/pinns) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: popular (59) · Freshness: quiet (28) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Feb 2026</sub>

**Reference code for physics-informed neural networks solving and discovering PDEs.**

Original research code from the Raissi, Perdikaris and Karniadakis papers on physics-informed neural networks. It trains networks that respect nonlinear partial differential equations, covering data-driven solution and data-driven discovery of PDEs, in continuous-time and discrete-time forms. The repository is no longer maintained, and the README points to PyTorch, JAX and TensorFlow v2 ports.

- **+** Reference implementation of the 2019 Journal of Computational Physics PINN paper
- **+** Covers both forward solution and inverse discovery of nonlinear PDEs
- **+** Continuous-time and discrete-time model variants are both described
- **+** MIT license with an accompanying project website
- **−** README states the repository is no longer under active maintenance
- **−** No install instructions, requirements or usage steps in the README
- **−** Research scripts rather than a packaged library; no tagged releases
- **−** Maintained ports exist in PyTorch, JAX and TensorFlow v2

<sub>Models: physics-informed neural networks · [Repo](https://github.com/maziarraissi/pinns) · [🌐 Site ↗](https://maziarraissi.github.io/PINNs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pinns/)</sub>

<a name="synonyms"></a>
### #&#8288;299 [synonyms](https://github.com/chatopera/synonyms) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: popular (53) · Freshness: quiet (17) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · custom license · Feb 2026</sub>

**Chinese synonym lookup and sentence similarity library built on word2vec vectors.**

Python package for Chinese NLP that returns nearest-neighbor words, sentence similarity scores, word vectors, jieba-based segmentation and keyword extraction. It uses a word2vec vector file with a 435,729-word vocabulary. The vector model download requires a paid license id from the Chatopera store, set through the SYNONYMS_DL_LICENSE environment variable.

- **+** Small API: nearby, compare, v, sv, bow, seg, keywords
- **+** Benchmark reports 0.209 usec per nearby call on a 4-core MacBook with 8GB
- **+** Installs from PyPI; env vars let you swap the vector file and segmentation dictionary
- **+** Vocabulary of 435,729 words built from Wikipedia-derived data
- **−** Model download needs a paid license purchased from the Chatopera store
- **−** License is Chunsong v1.0, but the README statement still says MIT
- **−** Cannot add words to the vocabulary; out-of-vocabulary words return empty results
- **−** Chinese only, static word2vec vectors; last release was January 2021

<sub>Needs Chatopera license store (paid license id), jieba · Models: word2vec binary vectors · [Repo](https://github.com/chatopera/synonyms) · [🌐 Site ↗](https://store.chatopera.com/product/syns001) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/synonyms/)</sub>

<a name="autokeras"></a>
### #&#8288;300 [autokeras](https://github.com/keras-team/autokeras) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: popular (71) · Freshness: quiet (13) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · Nov 2025</sub>

**AutoML library that searches Keras models with a fit/predict API.**

AutoKeras is a Python AutoML library built on Keras. It exposes task classes such as ImageClassifier with a fit/predict interface and searches for a suitable model. It is developed by DATA Lab at Texas A&M University and has a JMLR paper, tutorials and a book.

- **+** Three-line API: ak.ImageClassifier(), fit(), predict()
- **+** Installs with pip3 install autokeras
- **+** Official tutorials, a JMLR paper and a book are available
- **+** Apache-2.0 licensed, latest release 2025-11-12
- **−** README states support only for Python >= 3.7 and TensorFlow >= 2.8.0
- **−** README lists no supported tasks beyond the image classifier example
- **−** README gives no hardware requirements or search-time guidance
- **−** Not aimed at LLMs or generative models

<sub>Docker · Needs Python >= 3.7, TensorFlow >= 2.8.0 · Models: Keras · [Repo](https://github.com/keras-team/autokeras) · [📖 Docs ↗](https://autokeras.com/tutorial/overview/) · [🌐 Site ↗](https://autokeras.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autokeras/)</sub>

<a name="tensorwatch"></a>
### #&#8288;301 [tensorwatch](https://github.com/microsoft/tensorwatch) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: known (37) · Freshness: slowing (45) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · MIT · Mar 2026</sub>

**Real-time training visualization and live-query debugging for ML in Jupyter.**

TensorWatch is a Python library from Microsoft Research that streams logged metrics from a training script into Jupyter Notebook charts as they are written. Its lazy logging mode lets a client send a Python expression to the running process and plot the resulting stream without prior logging. It also draws model graphs, reports per-layer FLOPs and parameters, runs t-SNE on datasets, and provides CNN prediction explainers.

- **+** Lazy logging queries a live training process with lambda expressions, no pre-logging needed
- **+** Streams can feed multiple visualizers, files or sockets, and custom widgets are plain Python classes
- **+** Also covers model graphs, layer stats, t-SNE and CNN prediction explainers in one package
- **+** Installs with pip; example notebooks for MNIST, fruits and architecture views
- **−** Lazy logging runs eval() on client expressions; README says not for production or multi-tenant use
- **−** Messages and log files use pickle; only open trusted .log and .pkl files
- **−** Tested with PyTorch 0.4-1.x; TensorFlow support limited to eager tensors
- **−** Needs Jupyter Notebook for viewing; graphviz may require a manual install

<sub>GPU optional · Needs Jupyter Notebook, graphviz, pyzmq · Models: PyTorch 0.4-1.x, TensorFlow eager tensors · [Repo](https://github.com/microsoft/tensorwatch) · [📖 Docs ↗](https://github.com/microsoft/tensorwatch/blob/master/docs/simple_logging.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorwatch/)</sub>

<a name="texar"></a>
### #&#8288;302 [texar](https://github.com/asyml/texar) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: niche (21) · Freshness: recent (61) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · Apache-2.0 · Jul 2026</sub>

**TensorFlow toolkit for text generation and NLP model building.**

Texar is a modular TensorFlow 1.x library for building text generation and other NLP models, with components for data loading, encoders, decoders, losses and agents. It supports maximum likelihood, adversarial and reinforcement learning, and wraps pretrained BERT, GPT2 and XLNet. A PyTorch sibling, texar-pytorch, is maintained in a separate repo.

- **+** Same model can switch between MLE, adversarial and RL training with small code changes
- **+** Wraps pretrained BERT, GPT2 and XLNet behind uniform module interfaces
- **+** Multi-GPU distributed training and a documented examples directory
- **+** Compatible with native TensorFlow APIs, so external modules can be plugged in
- **−** Requires tensorflow below 2.0 and tensorflow_probability below 0.8
- **−** Needs Python 3.6 or 3.7 for versions above 0.2.3
- **−** Last release was November 2019; pretrained model list stops at XLNet
- **−** TensorFlow version is a separate codebase from the PyTorch port

<sub>GPU optional · Needs tensorflow >=1.10,<2.0, tensorflow_probability >=0.3.0,<0.8.0, Python 3.6 or 3.7 · Models: BERT, GPT2, XLNet, Transformer encoder-decoder · [Repo](https://github.com/asyml/texar) · [📖 Docs ↗](https://texar.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/texar/)</sub>

<a name="eo-learn"></a>
### #&#8288;303 [eo-learn](https://github.com/sentinel-hub/eo-learn) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: niche (4) · Freshness: recent (70) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Sep 2026</sub>

**Python library for chaining satellite imagery processing tasks on NumPy arrays.**

eo-learn is a set of Python packages for accessing and processing spatio-temporal satellite image sequences. Data is held in EOPatch objects as NumPy arrays, and steps such as cloud masking, co-registration, feature extraction and vector/raster conversion are EOTask units chained into an EOWorkflow. It reads from Sentinel Hub services or local files and hands results to the Python machine learning ecosystem.

- **+** Modular EOPatch/EOTask/EOWorkflow design lets tasks be reused and chained
- **+** Includes cloud masking, co-registration, geometry and ML-prep modules
- **+** Optional extras (Ray, Zarr, visualization) keep the base install light
- **+** Installs from PyPI or conda-forge; Docker image includes Jupyter and examples
- **−** Needs system geospatial libraries (GDAL, PROJ, spatialindex); Windows needs unofficial wheels
- **−** Data input is oriented to Sentinel Hub services, which may need an account
- **−** Many older contributed tasks were moved to a separate examples repository
- **−** Last release was 2024-09-27; examples repo is described as not always up to date

<sub>no GPU · Docker · Needs Python >=3.8, GDAL, PROJ, graphviz, libspatialindex, Sentinel Hub services · port 8888 · [Repo](https://github.com/sentinel-hub/eo-learn) · [📖 Docs ↗](https://eo-learn.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/eo-learn/)</sub>

<a name="jenly1314-mlkit"></a>
### #&#8288;304 [jenly1314/mlkit](https://github.com/jenly1314/mlkit) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: niche (2) · Freshness: active (80) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Jun 2026</sub>

**Kotlin Android library wrapping Google ML Kit vision APIs with camera-scan helpers.**

MLKit is a set of Android Gradle modules built on Google ML Kit and the CameraScan library. They cover barcode and QR scanning, face detection, face mesh, image labeling, object detection, pose detection, selfie segmentation and text recognition. Each module provides an Analyzer plus ready-made camera scan Activity and Fragment base classes. The project is published to Maven Central and JitPack, and a sample app is included.

- **+** Separate modules per feature, so apps pull in only the ML Kit parts they use
- **+** Each module ships an Analyzer plus Activity and Fragment base classes for camera scanning
- **+** Published on Maven Central and JitPack, with API docs and a sample APK
- **+** Supports 13 barcode formats, including QR Code, Data Matrix, PDF417 and EAN-13
- **−** Android only; minimum API level 23
- **−** Version 2.4.0 and later require compileSdk 35 or higher
- **−** Depends on the separate CameraScan library, whose package names differ from 1.x
- **−** README and docs are mostly in Chinese

<sub>Needs Google ML Kit, CameraScan, ViewfinderView, Android compileSdk 35+ (v2.4.0+), JDK 8+ · Models: Google ML Kit on-device vision models · [Repo](https://github.com/jenly1314/mlkit) · [📖 Docs ↗](https://jenly1314.github.io/MLKit/api/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jenly1314-mlkit/)</sub>

<a name="aif360"></a>
### #&#8288;305 [aif360](https://github.com/trusted-ai/aif360) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: niche (28) · Freshness: recent (51) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Jun 2026</sub>

**Python and R library for measuring and reducing bias in ML models.**

AIF360 is a library of fairness metrics and bias mitigation algorithms for datasets and classifiers, available for Python (3.10–3.13) and R. It implements about 15 published mitigation methods across preprocessing, in-processing and postprocessing, plus group fairness metrics, Generalized Entropy Index and bias scan. Tutorials are provided as Jupyter notebooks.

- **+** Covers preprocessing, in-processing and postprocessing mitigation, with papers cited for each algorithm
- **+** Metrics work out of the box; heavy algorithm dependencies are optional pip extras
- **+** Available on PyPI and CRAN, with example notebooks and an interactive web demo
- **+** Extensible design that accepts contributed metrics and algorithms
- **−** Last tagged release is April 2024, despite more recent commits
- **−** Some algorithms need TensorFlow or CVXPY, which can be hard to install
- **−** Example datasets must be downloaded manually and placed in specific folders
- **−** Targets classical tabular classifiers; no LLM-specific fairness tooling described

<sub>no GPU · Needs TensorFlow (AdversarialDebiasing only), CVXPY (OptimPreproc only) · Models: scikit-learn style classifiers, TensorFlow · [Repo](https://github.com/trusted-ai/aif360) · [📖 Docs ↗](https://aif360.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aif360/)</sub>

<a name="vbench"></a>
### #&#8288;306 [vbench](https://github.com/vchitect/vbench) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: niche (11) · Freshness: recent (68) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · Apache-2.0 · Aug 2026</sub>

**Benchmark suite for scoring video generation models across quality dimensions.**

VBench is a Python evaluation toolkit for video generative models. It scores generated videos on 16 text-to-video dimensions such as subject consistency, motion smoothness and aesthetic quality. It extends to image-to-video, long video and trustworthiness (VBench++), and to 18 intrinsic-faithfulness dimensions (VBench-2.0). It ships prompt suites, sampled videos and a Hugging Face leaderboard, and can score your own videos.

- **+** Covers 16 T2V dimensions, plus I2V, long-video, trustworthiness and VBench-2.0 modules
- **+** Installable from PyPI with `pip install vbench`; can evaluate custom videos
- **+** Releases prompt suites and sampled videos, with a public leaderboard and video arenas
- **+** Paper-backed (CVPR 2024, TPAMI 2025) with human-preference alignment reported
- **−** Last tagged release is 2024-09; newer modules live in repo subfolders
- **−** VBench++ code sits under legacy vbench2_beta_* paths, which is confusing
- **−** Install instructions assume PyTorch with CUDA, plus extra per-dimension dependencies
- **−** Evaluates videos only; it does not generate them

<sub>Needs PyTorch, torchvision · Models: text-to-video, image-to-video, long video · [Repo](https://github.com/vchitect/vbench) · [▶️ Demo ↗](https://huggingface.co/spaces/Vchitect/VBench_Video_Arena) · [🌐 Site ↗](https://vchitect.github.io/VBench-project/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vbench/)</sub>

<a name="vadersentiment"></a>
### #&#8288;307 [vadersentiment](https://github.com/cjhutto/vadersentiment) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: popular (53) · Freshness: quiet (25) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · MIT · Mar 2026</sub>

**Rule-based sentiment scorer for short social media text, in Python.**

VADER is a Python library that scores text sentiment using a human-rated lexicon of about 7,500 tokens plus grammatical rules for negation, punctuation, ALL CAPS, degree modifiers and emoticons. SentimentIntensityAnalyzer.polarity_scores() returns pos, neu, neg and a normalized compound score from -1 to +1. It needs no training and runs on CPU; the repo also ships the rated tweet, NYT, movie and Amazon datasets.

- **+** Installs with pip install vaderSentiment; no model download or training step
- **+** Handles negation, punctuation, capitalization, slang, emoticons and emoji via explicit rules
- **+** Lexicon rated by 10 human raters; ground-truth datasets included for evaluation
- **+** Linear-time scoring after the O(N^4) to O(N) refactor; already part of NLTK
- **−** English only; non-English text must be translated first, and the demo relies on an external service
- **−** Lexicon and rules, not a learned model, so context and sarcasm are missed
- **−** Last tagged release is 2014-11-17, so version history is stale
- **−** Returns sentence-level scores only; longer texts need external sentence splitting such as NLTK

<sub>no GPU · Needs NLTK and requests (demo only), MyMemory Translation Service (demo only) · Models: vader_lexicon.txt rule-based lexicon · [Repo](https://github.com/cjhutto/vadersentiment) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vadersentiment/)</sub>

<a name="pytorch-geometric-temporal"></a>
### #&#8288;308 [pytorch_geometric_temporal](https://github.com/benedekrozemberczki/pytorch_geometric_temporal) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: known (30) · Freshness: slowing (47) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · MIT · May 2026</sub>

**Temporal graph neural network layers and datasets for PyTorch Geometric.**

An extension library for PyTorch Geometric that implements dynamic and temporal graph neural networks from published papers, such as DCRNN, GConvGRU, A3T-GCN, STGCN, MTGNN and EvolveGCN. It includes dataset loaders, a train-test splitter and a temporal snapshot iterator, with benchmark datasets for epidemiological forecasting, web traffic and energy production. Recent versions add index-batching and Dask-DDP distributed training.

- **+** Implements about 20 temporal GNN layers from cited papers, including DCRNN, AGCRN, GMAN and MTGNN
- **+** Bundled benchmark datasets plus loader, splitter and snapshot iterator for temporal graphs
- **+** Index-batching reduces memory for spatiotemporal training; Dask-DDP adds distributed training
- **+** Works with PyTorch Lightning for CPU, single-GPU and multi-GPU training
- **−** Requires PyTorch and PyTorch Geometric to be installed separately before pip install
- **−** Last release is 2025-03-28, older than the latest commit
- **−** Distributed training needs the separate [ddp] extra and Dask setup
- **−** Covers graph time-series models only, not LLMs or general-purpose deep learning

<sub>GPU optional · Needs PyTorch, PyTorch Geometric, PyTorch Lightning (optional), Dask (optional, DDP) · Models: DCRNN, GConvGRU, GConvLSTM, A3T-GCN, AGCRN · [Repo](https://github.com/benedekrozemberczki/pytorch_geometric_temporal) · [📖 Docs ↗](https://pytorch-geometric-temporal.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-geometric-temporal/)</sub>

<a name="eli5"></a>
### #&#8288;309 [eli5](https://github.com/teamhg-memex/eli5) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: niche (28) · Freshness: slowing (49) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Apr 2026</sub>

**Python library for explaining scikit-learn, XGBoost and other ML classifier predictions.**

ELI5 is a Python package that inspects machine learning classifiers and regressors and explains their weights and predictions. It supports scikit-learn, Keras (Grad-CAM), XGBoost, LightGBM, CatBoost, lightning and sklearn-crfsuite, and adds LIME-based TextExplainer and permutation importance for black-box models. Output can be text, HTML, a pandas DataFrame or JSON.

- **+** Covers scikit-learn, Keras, XGBoost, LightGBM, CatBoost, lightning and sklearn-crfsuite
- **+** Black-box tools: LIME-based TextExplainer and permutation importance
- **+** Explanation and formatting are separate: text, HTML, DataFrame or JSON output
- **+** Highlights text features and can undo HashingVectorizer in scikit-learn pipelines
- **−** Keras support is limited to Grad-CAM for image classifiers
- **−** CatBoost support covers feature importances only, not prediction explanations
- **−** LIME for non-text data is marked experimental
- **−** No tagged release; README CI badge points to Travis, so maintenance status is unclear

<sub>no GPU · Needs scikit-learn, pandas · Models: scikit-learn, Keras, XGBoost, LightGBM, CatBoost · [Repo](https://github.com/teamhg-memex/eli5) · [📖 Docs ↗](https://eli5.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/eli5/)</sub>

<a name="easyrec"></a>
### #&#8288;310 [easyrec](https://github.com/alibaba/easyrec) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: niche (21) · Freshness: recent (52) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · Apache-2.0 · Apr 2026</sub>

**TensorFlow framework for training and deploying recommendation models from config files.**

EasyRec is a TensorFlow-based framework from Alibaba for building recommender systems: candidate generation (DSSM, MIND), ranking (DeepFM, DCN, DIN) and multi-task models (MMoE, ESMM, PLE). Models are defined through config files, with built-in hyperparameter search, feature selection and knowledge distillation. It reads from MaxCompute, HDFS, Hive, OSS, CSV, Parquet, Datahub and Kafka. The README points to TorchEasyRec as the PyTorch successor.

- **+** Many built-in models: DSSM, MIND, DeepFM, DCN, DIN, MMoE, ESMM, PLE and more
- **+** Reads MaxCompute, HDFS, Hive, OSS, CSV, Parquet, Datahub and Kafka inputs
- **+** Parameter server, mirrored and multi-worker training, plus online learning support
- **+** Models built from config and reusable backbone components, without custom data pipelines
- **−** Built on TF 1.12-1.15 / TF2.x; Alibaba points new work to TorchEasyRec
- **−** Deployment and quick-start paths centre on Alibaba Cloud (MaxCompute, EMR, EAS, PAI)
- **−** Web interface and NAS are listed as still in development
- **−** No Docker or compose files detected in the repository

<sub>Docker · Needs TensorFlow, MaxCompute (optional), HDFS/Hive (optional), Kafka/Datahub (optional) · Models: DSSM, MIND, DropoutNet, PDN, Wide&Deep · [Repo](https://github.com/alibaba/easyrec) · [▶️ Demo ↗](https://dsw-dev.data.aliyun.com/#/?fileUrl=http://easyrec.oss-cn-beijing.aliyuncs.com/dsw/easy_rec_demo.ipynb&fileName=EasyRec_DeepFM.ipynb) · [📖 Docs ↗](https://easyrec.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/easyrec/)</sub>

<a name="kubetorch"></a>
### #&#8288;311 [kubetorch](https://github.com/run-house/kubetorch) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: niche (3) · Freshness: recent (69) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · May 2026</sub>

**Python SDK for running ML workloads on Kubernetes with 1-3 second iteration.**

Kubetorch is a Python client plus Helm chart that sends local functions to compute launched on a Kubernetes cluster, with no local runtime or code serialization. Logs, exceptions and hardware faults are streamed back to the calling process. The README claims 1-3 second iteration for workloads like RL and distributed training, and it runs from IDEs, notebooks, CI or production code.

- **+** Remote calls from plain Python via kt.fn(...).to(compute), with no local runtime
- **+** Logs, exceptions and hardware faults stream back to the caller in real time
- **+** Works from notebooks, IDEs, CI and production code
- **+** Repo ships the SDK, Helm chart, controller, data store and base images
- **−** Requires an existing Kubernetes cluster and a Helm install of the chart
- **−** Claims of 100x, 50% and 95% improvements come with no methodology
- **−** Managed serverless option is contact-only, no self-serve signup
- **−** Last release (2026-02-18) predates the latest commit by about three months

<sub>GPU optional · Needs Kubernetes, Helm · [Repo](https://github.com/run-house/kubetorch) · [📖 Docs ↗](https://www.run.house/kubetorch/introduction) · [🌐 Site ↗](https://www.run.house) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kubetorch/)</sub>

<a name="paddleseg"></a>
### #&#8288;312 [paddleseg](https://github.com/paddlepaddle/paddleseg) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: popular (71) · Freshness: quiet (0) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · Apache-2.0 · Nov 2025</sub>

**Image segmentation toolkit on PaddlePaddle, from training to deployment.**

PaddleSeg is a PaddlePaddle-based toolkit for image segmentation with 45+ model algorithms and 140+ pretrained models. It covers semantic, interactive, matting and panoptic segmentation, driven by YAML configs or a Python API, and includes compression and deployment tooling. The README also points to PaddleX for low-code use of 19 segmentation and anomaly-detection models.

- **+** Large model zoo: 45+ segmentation networks with Cityscapes and ADE20K benchmark tables
- **+** Covers semantic, interactive (EISeg), matting and panoptic segmentation in one repo
- **+** Includes quantization-aware distillation and deployment paths such as PaddleInference and PaddleLite
- **+** Modular configs separate backbones, losses, datasets and augmentations
- **−** Requires the PaddlePaddle framework, not PyTorch, which limits reuse with PyTorch tooling
- **−** Primary README is in Chinese, with English in a separate file
- **−** Last release was 2024-11-05; no Docker or compose files detected

<sub>GPU optional · Needs PaddlePaddle · Models: PP-LiteSeg, PP-MobileSeg, DeepLabV3P, OCRNet, SegFormer · [Repo](https://github.com/paddlepaddle/paddleseg) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddleseg/)</sub>

<a name="aim"></a>
### #&#8288;313 [aim](https://github.com/aimhubio/aim) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: popular (60) · Freshness: quiet (9) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Dec 2025</sub>

**Self-hosted ML experiment tracker with a web UI and Python query API.**

Aim logs training runs and other metadata through a Python SDK. Its web UI groups, aggregates and compares runs, and queries are written as Python expressions. The README says it is built to handle tens of thousands of runs, and the SDK gives programmatic access to tracked data, for example from Jupyter notebooks.

- **+** Query runs with Python expressions in the UI and through the SDK
- **+** Public live demos on play.aimstack.io with real training logs
- **+** Tracks system info and resource usage; supports alerting and notifications
- **+** Integrates with popular ML frameworks and offers migration from other trackers
- **−** README lists Linux and macOS only; no Windows support stated
- **−** Last release 2025-05-08, while the latest commit is 2025-12-31
- **−** Enterprise support is sold separately; README does not describe multi-user auth
- **−** Focused on training experiments; LLM tracing and prompt management are not described

<sub>no GPU · Docker · [Repo](https://github.com/aimhubio/aim) · [📖 Docs ↗](https://aimstack.readthedocs.io/en/latest/) · [🌐 Site ↗](https://aimstack.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aim/)</sub>

<a name="robosat"></a>
### #&#8288;314 [robosat](https://github.com/mapbox/robosat) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: niche (15) · Freshness: recent (55) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · MIT · Jun 2026</sub>

**Pipeline for extracting buildings and roads from satellite imagery as GeoJSON.**

RoboSat is a Python 3 command-line pipeline (`rs`) that builds training sets from OpenStreetMap geometries and Slippy Map imagery, trains fully convolutional segmentation nets, and converts predictions into simplified GeoJSON polygons. It also covers ONNX export, an on-demand segmentation tile server, and deduplication against OpenStreetMap. The README states Mapbox no longer maintains it.

- **+** Covers the full path: OSM extraction, imagery download, training, prediction, GeoJSON output
- **+** Works on any geo-referenced imagery converted to Slippy Map tiles
- **+** ONNX export allows inference without PyTorch, for example on AWS Lambda
- **+** Feature handlers for pre- and post-processing are small and registered in one file
- **−** Not maintained by Mapbox; main developers have left; last release was 2019
- **−** Training recommended on GPUs; the README cites p2/p3 instances and GTX 1080 Ti
- **−** Default imagery source is the Mapbox Maps API, which needs an access token
- **−** No pretrained models or demo mentioned; datasets must be built by the user

<sub>GPU optional · Docker · Needs PyTorch, osmium, Mapbox Maps API (default imagery), OpenStreetMap .osm.pbf extracts · Models: fully convolutional segmentation nets (.pth), ONNX export · [Repo](https://github.com/mapbox/robosat) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/robosat/)</sub>

<a name="sageattention"></a>
### #&#8288;315 [sageattention](https://github.com/thu-ml/sageattention) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: known (43) · Freshness: quiet (19) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · Apache-2.0 · Jan 2026</sub>

**8-bit quantized attention GPU kernels that replace PyTorch scaled_dot_product_attention.**

SageAttention provides CUDA and Triton attention kernels that quantize QK^T to INT8 and PV to FP8 or FP16, targeting Ampere, Ada and Hopper GPUs. Its `sageattn` function picks a kernel per GPU and can be swapped in for `F.scaled_dot_product_attention` in video and image diffusion models. The repo also holds SageAttention2++ and a Blackwell-targeted SageAttention3 (FP4) directory.

- **+** Drop-in `sageattn` call; one-line patch of scaled_dot_product_attention shown for CogVideoX
- **+** Kernels for Ampere, Ada and Hopper, with RTX 5090 compile support
- **+** Supports GQA, varlen, differing q and kv lengths, torch.compile and distributed inference
- **+** Includes benchmark scripts against FlashAttention2 and FlashAttention3, plus model examples
- **−** NVIDIA CUDA only; needs CUDA 12.0 to 12.8 depending on GPU generation
- **−** Global SDPA patch does not work for every model; attention class may need editing
- **−** Inputs must be FP16 or BF16; building from source needs a CUDA toolchain
- **−** SageAttention3 is FP4 for Blackwell; README advises SageAttention2 where precision matters

<sub>GPU required · Needs python>=3.9, torch>=2.3.0, triton>=3.0.0, CUDA>=12.0, flash-attn (benchmarking only) · Models: CogVideoX, Mochi, FP16/BF16 PyTorch attention · [Repo](https://github.com/thu-ml/sageattention) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sageattention/)</sub>

<a name="transmogrifai"></a>
### #&#8288;316 [transmogrifai](https://github.com/salesforce/transmogrifai) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (19) · Freshness: slowing (48) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · BSD-3-Clause · Jun 2026</sub>

**Scala AutoML library on Apache Spark for structured data.**

TransmogrifAI is a Scala library that runs on Apache Spark and automates feature engineering, feature validation and model selection for structured data. Its API is type-checked at compile time, and workflows are built from reusable stages. Users can accept the automated defaults or specify every feature and algorithm by hand.

- **+** One-line feature engineering, sanity checks and model selection on Spark DataFrames
- **+** Compile-time type-safe feature API with modular, reusable workflow stages
- **+** Model summary reports metrics, chosen hyperparameters and feature insights (correlation, CramersV)
- **+** Automation is optional: features and algorithms can be specified explicitly
- **−** Last release 0.7.0 in June 2020; targets Spark 2.4 and Scala 2.11 only
- **−** Requires Java 1.8 and a Spark/Scala stack, a poor fit for Python teams
- **−** Aimed at structured data; no LLM or deep learning support described
- **−** README example only shows logistic regression and random forest selection

<sub>no GPU · Needs Apache Spark 2.4, Scala 2.11, Java 1.8 · Models: Spark MLlib logistic regression, Spark MLlib random forest · [Repo](https://github.com/salesforce/transmogrifai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transmogrifai/)</sub>

<a name="raster-vision"></a>
### #&#8288;317 [raster-vision](https://github.com/azavea/raster-vision) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (19) · Freshness: slowing (49) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Jun 2026</sub>

**Python library for training vision models on satellite and aerial imagery.**

Raster Vision is a Python library and low-code framework for chip classification, object detection and semantic segmentation on satellite, aerial and drone imagery, using PyTorch backends. It runs a configurable pipeline: analyze data, create chips, train, predict, evaluate and bundle the model. Experiments can run locally or on AWS Batch and AWS SageMaker.

- **+** Reads and writes geo-referenced data, so predictions come out in geospatial formats
- **+** Repeatable pipeline from chip creation through evaluation and model bundling
- **+** Built-in AWS Batch and SageMaker support for cloud runs
- **+** Installable with pip or prebuilt Docker images on quay.io
- **−** Limited to three tasks: chip classification, object detection, semantic segmentation
- **−** Built-in cloud execution covers AWS only
- **−** Last release is 2024-08-30, well behind recent commits
- **−** PyTorch is the only backend mentioned

<sub>Docker · Needs PyTorch, AWS Batch (optional), AWS SageMaker (optional) · Models: PyTorch · [Repo](https://github.com/azavea/raster-vision) · [📖 Docs ↗](https://docs.rastervision.io/en/stable/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/raster-vision/)</sub>

<a name="onnxstream"></a>
### #&#8288;318 [onnxstream](https://github.com/vitoplantamura/onnxstream) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (16) · Freshness: recent (52) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · custom license · Jun 2026</sub>

**Memory-minimal C++ ONNX inference library that runs Stable Diffusion on 512MB devices.**

OnnxStream is a small C++ inference library for ONNX models that decouples the engine from a WeightsProvider, so weights can stream from disk, RAM or a custom source. It runs Stable Diffusion 1.5 and SDXL (including Turbo) in under 300MB of RAM on a Raspberry Pi Zero 2, using attention slicing, quantization and tiled VAE decoding. It also includes an LLM chat app (TinyLlama 1.1B, Mistral 7B) and WebAssembly builds.

- **+** README reports up to 55x less memory than OnnxRuntime on SD 1.5 UNET
- **+** SDXL 1.0 runs in under 300MB RAM via tiled VAE decoding and quantization
- **+** Single implementation file plus header; Python and C# bindings available
- **+** WebAssembly builds with demos for YOLOv8 and Whisper in the browser
- **−** Latency is 50% to 200% higher than OnnxRuntime on SD 1.5 UNET
- **−** Implements only 41 ONNX operators; models using others will not run
- **−** No dynamic input shapes and no batch size other than 1
- **−** GPU support is limited to cuBLAS in the LLM app, FP16 and FP32 only

<sub>GPU optional · Docker · Needs XNNPACK, CMake · Models: ONNX, Stable Diffusion 1.5, SDXL 1.0 Base, SDXL Turbo 1.0, TinyLlama 1.1B · [Repo](https://github.com/vitoplantamura/onnxstream) · [▶️ Demo ↗](https://yolo.vitoplantamura.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onnxstream/)</sub>

<a name="keras-tcn"></a>
### #&#8288;319 [keras-tcn](https://github.com/philipperemy/keras-tcn) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (14) · Freshness: recent (52) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · MIT · Jun 2026</sub>

**Keras layer implementing Temporal Convolutional Networks for sequence modeling.**

keras-tcn provides a TCN layer for Keras built from dilated causal convolutions in residual blocks. It is an alternative to LSTM/GRU for time series and sequence tasks, with configurable filters, kernel size, dilations, stacks, normalization and causal or non-causal padding. The repo includes example tasks (adding problem, copy memory, sequential MNIST, word-level PTB) and is tested with TensorFlow 2.9 to 2.19.

- **+** Single Keras layer with LSTM-like arguments such as nb_filters and return_sequences
- **+** Supports causal and non-causal padding, batch or layer norm, and variable-length input
- **+** Runnable example tasks: adding problem, copy memory, sequential MNIST, word PTB
- **+** Tested against TensorFlow 2.9 through 2.19; installs with pip
- **−** Tied to TensorFlow/Keras; no PyTorch implementation in this repo
- **−** Last tagged release is from 2021-02-16
- **−** Inputs longer than the receptive field lose earlier values, which are replaced with zeros
- **−** Parameter guidance is the author's notes, not systematic benchmarks

<sub>GPU optional · Needs TensorFlow · Models: Keras TCN layer, dilated causal convolutions · [Repo](https://github.com/philipperemy/keras-tcn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/keras-tcn/)</sub>

<a name="pytorch-scatter"></a>
### #&#8288;320 [pytorch_scatter](https://github.com/rusty1s/pytorch_scatter) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (8) · Freshness: slowing (48) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Jun 2026</sub>

**PyTorch extension for scatter and segment reduce operations.**

torch-scatter adds sparse scatter and segment reductions (sum, mean, min, max) to PyTorch, driven by a group-index tensor. It provides scatter, segment_coo and segment_csr, plus composite ops such as scatter_std, scatter_logsumexp, scatter_softmax and scatter_log_softmax. Operations run on CPU and GPU with backward implementations, and a C++ API is available.

- **+** Covers sum, mean, min and max reductions via scatter, segment_coo and segment_csr
- **+** CPU and CUDA implementations with backward passes and broadcasting
- **+** Prebuilt pip wheels for Linux, Windows and macOS across many PyTorch versions
- **+** Includes a C++ API built with CMake, plus MIT license
- **−** Last release is 2023-10-06; newer PyTorch support relies on wheels at data.pyg.org
- **−** macOS wheels are CPU only; no CUDA builds there
- **−** Building from source needs a matching CUDA toolchain and PyTorch 1.4.0 or newer
- **−** Narrow scope: reduce operations only, not a general sparse library

<sub>GPU optional · Needs PyTorch, CUDA toolkit (source builds with GPU) · [Repo](https://github.com/rusty1s/pytorch_scatter) · [📖 Docs ↗](https://pytorch-scatter.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-scatter/)</sub>

<a name="ltp"></a>
### #&#8288;321 [ltp](https://github.com/hit-scir/ltp) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: popular (54) · Freshness: quiet (27) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 5.3k · no license · Mar 2026</sub>

**Chinese NLP toolkit for word segmentation, POS tagging, NER and parsing.**

LTP (Language Technology Platform) from HIT-SCIR runs six Chinese NLP tasks: word segmentation, POS tagging, named entity recognition, semantic role labeling, dependency parsing and semantic dependency parsing. It ships PyTorch multi-task models (Base, Small, Tiny) and a Rust perceptron "legacy" model limited to segmentation, POS and NER. Models download from Hugging Face and can be retrained with the provided scripts.

- **+** Six Chinese NLP tasks through one Pipeline API on a shared pre-trained model
- **+** Rust perceptron model: README claims 3.55x LTP3 speed, 17.17x with multithreading
- **+** Training scripts and hydra configs allow training on private data
- **+** Tiny, Small and Base models trade accuracy for speed; custom word lists supported
- **−** Commercial use requires a paid license; free only for academic and individual research
- **−** No standard open-source license detected; terms are custom text in the README
- **−** Last release is 2022-08
- **−** Chinese only; legacy model covers just segmentation, POS and NER

<sub>GPU optional · Needs PyTorch, Transformers, Hugging Face Hub · Models: PyTorch, Hugging Face Hub, Rust perceptron (Avro) · [Repo](https://github.com/hit-scir/ltp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ltp/)</sub>

<a name="deep-person-reid"></a>
### #&#8288;322 [deep-person-reid](https://github.com/kaiyangzhou/deep-person-reid) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: popular (51) · Freshness: quiet (11) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · MIT · Jan 2026</sub>

**PyTorch library for training and evaluating person re-identification models.**

Torchreid is a PyTorch library for person re-identification, covering both image and video re-ID. It provides data managers for datasets such as Market1501, CUHK03, MSMT17 and MARS, plus implementations of ReID models including OSNet, OSNet-AIN, PCB, HACNN and MLFN, and ImageNet backbones like ResNet. Training runs from Python code or a config-driven script, with multi-GPU, cross-dataset evaluation and export to ONNX, OpenVINO and TFLite.

- **+** Many standard re-ID datasets, image and video, with multi-dataset training and cross-dataset evaluation
- **+** Includes OSNet and OSNet-AIN plus other ReID and ImageNet backbones, with a pretrained model zoo
- **+** Feature extractor API and export script for ONNX, OpenVINO and TFLite
- **+** YAML configs and scripts/main.py give a reproducible train and test interface
- **−** Last release is v1.4.0 from 2019-10-23 per tracker data; README install targets Python 3.7
- **−** Install guide pins cudatoolkit=9.0 with conda, which is outdated for current GPUs
- **−** Research-oriented: no inference server or tracking pipeline, only training, evaluation and feature extraction
- **−** Datasets must be downloaded and prepared separately; some model weights are hosted on Google Drive

<sub>GPU optional · Docker · Needs PyTorch, torchvision, conda, Cython · Models: OSNet, OSNet-AIN, ResNet, PCB, HACNN · [Repo](https://github.com/kaiyangzhou/deep-person-reid) · [📖 Docs ↗](https://kaiyangzhou.github.io/deep-person-reid/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deep-person-reid/)</sub>

<a name="explainerdashboard"></a>
### #&#8288;323 [explainerdashboard](https://github.com/oegedijk/explainerdashboard) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (23) · Freshness: slowing (41) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · MIT · Feb 2026</sub>

**Dash web dashboard that explains scikit-learn-style model predictions with SHAP.**

Python library that wraps a fitted scikit-learn-compatible model in a Plotly Dash web app. It shows feature importances, SHAP values and interactions, partial dependence plots, what-if analysis and individual decision trees. It runs from a script, notebook or CLI, exports static HTML, and lets you combine several dashboards in an ExplainerHub with logins.

- **+** Dashboard launches in one line from a fitted model and test set
- **+** Works with scikit-learn, xgboost, catboost, lightgbm and skorch models
- **+** Modular components and per-tab switches allow custom dashboard layouts
- **+** Exports static HTML and runs from CLI using joblib or YAML config
- **−** SHAP interaction values and permutation importances are slow on large data or complex models
- **−** Aimed at tabular scikit-learn-style models; no LLM explanation support described
- **−** Explainer must be dumped to joblib to avoid recomputing calculated properties
- **−** GPU Tree SHAP needs an NVIDIA GPU and a CUDA-enabled SHAP build

<sub>GPU optional · Needs plotly dash, dash-bootstrap-components, shap, scikit-learn · Models: scikit-learn, xgboost, catboost, lightgbm, skorch · port 8050 · [Repo](https://github.com/oegedijk/explainerdashboard) · [▶️ Demo ↗](https://titanicexplainer.fly.dev) · [📖 Docs ↗](http://explainerdashboard.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/explainerdashboard/)</sub>

<a name="phiflow"></a>
### #&#8288;324 [phiflow](https://github.com/tum-pbs/phiflow) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (13) · Freshness: recent (52) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · MIT · May 2026</sub>

**Differentiable PDE and fluid simulation toolkit for PyTorch, Jax and TensorFlow.**

Φ-Flow is a Python library for physics simulation that runs on NumPy, PyTorch, Jax or TensorFlow, so simulations can be differentiated and combined with neural networks. It includes grid, mesh and particle examples (fluids, SPH, FLIP, heat, Burgers), a sparse linear solver, and an optional Dash web UI for live visualization. It builds on the PhiML tensor library with named dimensions.

- **+** Same simulation code runs on NumPy, PyTorch, Jax or TensorFlow, in 2D or 3D
- **+** End-to-end differentiable physics for training networks through solvers
- **+** Covers grids, FVM meshes and particles, with many runnable example notebooks
- **+** High-level linear solver generates sparse matrices automatically
- **−** Built-in physics focuses on fluids; other PDE domains need user code
- **−** GPU use needs a separate ML framework; custom CUDA ops need manual compilation
- **−** Requires learning PhiML named and typed dimensions before code reads naturally
- **−** Whitepaper still listed as upcoming; citation points to older papers

<sub>GPU optional · Needs NumPy, PyTorch, Jax, TensorFlow, Dash, PhiML · [Repo](https://github.com/tum-pbs/phiflow) · [▶️ Demo ↗](https://colab.research.google.com/drive/1zBlQbmNguRt-Vt332YvdTqlV4DBcus2S#offline=true&sandboxMode=true) · [📖 Docs ↗](https://tum-pbs.github.io/PhiFlow/) · [🌐 Site ↗](https://tum-pbs.github.io/PhiFlow/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/phiflow/)</sub>

<a name="torchquantum"></a>
### #&#8288;325 [torchquantum](https://github.com/mit-han-lab/torchquantum) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (7) · Freshness: recent (57) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Jul 2026</sub>

**PyTorch library for simulating and training parameterized quantum circuits.**

TorchQuantum simulates quantum circuits as PyTorch modules, using statevector simulation on CPU or GPU with batched tensors and autograd gradients. It targets quantum machine learning, VQE and QAOA research, and includes converters to deploy circuits on real IBMQ devices via Qiskit. The README says it scales to 30+ qubits with multiple GPUs.

- **+** Circuits are PyTorch modules, so hybrid quantum-classical models train with standard autograd
- **+** Batched statevector simulation on CPU or CUDA, with multi-GPU scaling to 30+ qubits
- **+** Exports to QASM and Qiskit for running on real IBMQ hardware
- **+** Examples cover MNIST QNN, VQE, QAOA, quantum kernels and on-chip parameter-shift training
- **−** Pulse-level simulation is listed as coming soon in the feature list
- **−** Last release is v0.1.8 from February 2024; newer features sit on a dev branch
- **−** Documented Python support is 3.7 to 3.9, with a Qiskit issue noted on 3.10
- **−** Install is a git clone and editable install from source in the README

<sub>GPU optional · Needs PyTorch >= 1.8.0, configargparse >= 0.14, Qiskit (for IBMQ deployment) · Models: statevector simulation, parameterized quantum circuits · [Repo](https://github.com/mit-han-lab/torchquantum) · [📖 Docs ↗](https://torchquantum.readthedocs.io/) · [🌐 Site ↗](https://qmlsys.mit.edu) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/torchquantum/)</sub>

<a name="py-motmetrics"></a>
### #&#8288;326 [py-motmetrics](https://github.com/cheind/py-motmetrics) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (5) · Freshness: recent (60) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · MIT · Jul 2026</sub>

**Python library for scoring multiple object tracking with MOTChallenge metrics.**

py-motmetrics evaluates multi-object tracker output against ground truth, computing CLEAR MOT (MOTA, MOTP), Identity (IDF1) and HOTA-related metrics. It reads MOTChallenge text, VATIC text and UA-DETRAC MAT/XML files, and returns a pandas-backed summary table. It can be called from Python or run as a command-line evaluator over a folder of sequences.

- **+** Results aligned with the MOTChallenge devkit, with a parity test against TrackEval 1.3.0
- **+** Auto-detects MOTChallenge, VATIC and UA-DETRAC input formats
- **+** Summary keeps raw pandas data, exportable with to_csv
- **+** MOTAccumulator and MetricsHost allow lower-level custom metric selection
- **−** MOTP reports average distance, so it needs conversion to match MOTChallenge percentages
- **−** Evaluation only: it does not run or train trackers
- **−** Last release 2024-10-30, well behind recent commits

<sub>no GPU · Docker · Needs pandas · [Repo](https://github.com/cheind/py-motmetrics) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/py-motmetrics/)</sub>

<a name="hierarchical-localization"></a>
### #&#8288;327 [hierarchical-localization](https://github.com/cvg/hierarchical-localization) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: known (46) · Freshness: quiet (4) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · Apache-2.0 · Dec 2025</sub>

**Python toolbox for 6-DoF visual localization and Structure-from-Motion.**

hloc implements Hierarchical Localization: image retrieval picks candidate database images, local features are matched, and a camera pose is estimated against a COLMAP-built 3D SfM model. It wraps extractors (SuperPoint, DISK, D2-Net, SIFT, R2D2), matchers (SuperGlue, LightGlue, LoFTR, nearest neighbor) and retrieval models (NetVLAD, AP-GeM, OpenIBL, MegaLoc). Ready-made pipelines cover Aachen, InLoc, RobotCar, Cambridge Landmarks and 7-Scenes.

- **+** Pluggable extractor, matcher and retrieval interfaces via a BaseModel subclass
- **+** Pipeline scripts for Aachen, InLoc, CMU Seasons, RobotCar, 4Seasons, Cambridge and 7-Scenes
- **+** Since v1.3 pycolmap is enough; no separate COLMAP install
- **+** Colab demo notebook runs SfM and localization on a free GPU
- **−** Last tagged release is v1.4 from July 2023
- **−** Research toolbox of scripts and notebooks, not a packaged service or GUI
- **−** Needs git submodules for external feature repos
- **−** TensorFlow-based features require manual HDF5 export or code changes

<sub>GPU optional · Docker · Needs PyTorch >=1.1, pycolmap >=0.3.0, kornia >=0.6.11, Python >=3.7 · Models: SuperPoint, DISK, D2-Net, SIFT, R2D2 · [Repo](https://github.com/cvg/hierarchical-localization) · [▶️ Demo ↗](https://colab.research.google.com/drive/1Eqoz-uLTCGeEWtH95FZyVs2vI-qkTOWr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hierarchical-localization/)</sub>

<a name="audioflux"></a>
### #&#8288;328 [audioflux](https://github.com/libaudioflux/audioflux) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: known (36) · Freshness: quiet (26) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Mar 2026</sub>

**C library with Python bindings for audio time-frequency transforms and feature extraction.**

audioFlux is a C library with a Python package that computes time-frequency transforms (BFT, NSGT, CWT, PWT, CQT, VQT, DWT and others) across Linear, Mel, Bark, Erb, Octave and Log scales. On top of these it provides spectral, cepstral (MFCC-style) and chroma features, plus MIR functions for pitch, onset detection and harmonic-percussive separation. Output is meant as input for training audio models for classification, separation or ASR.

- **+** Broad transform set: BFT, NSGT, CWT, PWT, CQT, VQT, ST, DWT, WPT, SWT
- **+** Core in C; builds for Linux, macOS, Windows, iOS and Android
- **+** Installs with pip or conda; MIT licensed
- **+** Includes pitch (YIN and others), onset, HPSS, pitch shift and time stretch
- **−** Feature extraction only; no models, training loops or pretrained weights
- **−** Last tagged release is 2024-05-24, while commits continue into 2026
- **−** iOS, Android and source builds need manual steps from the docs
- **−** Benchmark shown only on one CPU; GPU support is not documented

<sub>[Repo](https://github.com/libaudioflux/audioflux) · [📖 Docs ↗](https://audioflux.top) · [🌐 Site ↗](https://audioflux.top) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/audioflux/)</sub>

<a name="internnav"></a>
### #&#8288;329 [internnav](https://github.com/internrobotics/internnav) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (3) · Freshness: slowing (48) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Mar 2026</sub>

**Toolbox for training and evaluating embodied navigation models in Habitat and Isaac Sim.**

InternNav is a PyTorch toolbox for vision-language navigation (VLN-CE, VLN-PE) and visual navigation with point, image or trajectory goals. It runs training and evaluation against Habitat and Isaac Sim, and ships a model zoo of 10+ baselines, including the InternVLA-N1 dual-system navigation model, plus the InternData-N1 dataset. Real-world deployment code for Unitree Go2 is included.

- **+** Covers VLN-CE, VLN-PE and visual navigation benchmarks with published result tables
- **+** Model zoo includes Seq2Seq, CMA, RDP, NavDP and InternVLA-N1 checkpoints on Hugging Face
- **+** Supports both Habitat and Isaac Sim, with distributed VLN-PE evaluation since v0.2.0
- **+** Training code for InternVLA-N1 and real-world Go2 deployment code are released
- **−** InternData-N1 dataset is CC BY-NC-SA 4.0, so non-commercial only
- **−** StreamVLN support is listed as coming soon
- **−** Needs Habitat or Isaac Sim setup; no Docker or compose files provided
- **−** README defers installation and hardware requirements to external docs

<sub>Needs PyTorch, Habitat, Isaac Sim, InternUtopia · Models: InternVLA-N1, NavDP, Seq2Seq, CMA, RDP · [Repo](https://github.com/internrobotics/internnav) · [▶️ Demo ↗](https://www.youtube.com/watch?v=fD0F1jIax5Y) · [📖 Docs ↗](https://internrobotics.github.io/user_guide/internnav/index.html) · [🌐 Site ↗](https://internrobotics.github.io/internvla-n1.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/internnav/)</sub>

<a name="pmdarima"></a>
### #&#8288;330 [pmdarima](https://github.com/alkaline-ml/pmdarima) <sub>score [17](../README.md#-how-we-rank "Score 17/100. Adoption: niche (8) · Freshness: quiet (14) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Nov 2025</sub>

**Python auto-ARIMA time series forecasting library with a scikit-learn style API.**

pmdarima is a Python statistics library that provides the equivalent of R's auto.arima, wrapping statsmodels behind a scikit-learn style fit/predict interface. It also includes stationarity and seasonality tests, differencing, Box-Cox and Fourier transformers, seasonal decomposition, cross-validation utilities, and bundled datasets. Pipelines can be pickled and reloaded for prediction.

- **+** Automatic ARIMA order selection, including seasonal models, via a single auto_arima call
- **+** Scikit-learn style pipelines combine transformers like Box-Cox with the ARIMA estimator
- **+** Bundled datasets and cross-validation utilities for time series prototyping
- **+** Prebuilt wheels for Linux, Mac and Windows on Python 3.10+
- **−** Covers ARIMA-family models only; no neural or gradient-boosted forecasters
- **−** Built on statsmodels, so fitting speed and model coverage depend on it
- **−** Conda packages are maintained by conda-forge, not the project
- **−** Source builds need cython>=0.29 and gcc or MinGW; 32-bit wheels stop at 2.0.0

<sub>no GPU · Needs statsmodels, Python 3.10+ · Models: ARIMA, SARIMA, auto_arima · [Repo](https://github.com/alkaline-ml/pmdarima) · [📖 Docs ↗](https://www.alkaline-ml.com/pmdarima) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pmdarima/)</sub>

<a name="pycm"></a>
### #&#8288;331 [pycm](https://github.com/sepandhaghighi/pycm) <sub>score [17](../README.md#-how-we-rank "Score 17/100. Adoption: niche (5) · Freshness: slowing (50) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · MIT · Mar 2026</sub>

**Python library for multi-class confusion matrices and classifier metrics.**

PyCM builds a confusion matrix from actual and predicted vectors or from a matrix directly, then computes per-class and overall statistics such as ACC, F1, PPV, TPR, AUC and Kappa. It also provides ROC, precision-recall, precision, recall and F1 curves using one-vs-rest binarization for multi-class output. It is a classifier-evaluation library, not an LLM tool.

- **+** Computes many per-class and overall metrics from one ConfusionMatrix object
- **+** Accepts prediction vectors or a ready-made matrix, with sample weights and thresholds
- **+** combine() merges matrices, useful for mini-batch evaluation
- **+** Installs from PyPI, Conda or source; MATLAB usage is documented
- **−** Evaluation only; no training, inference or LLM-specific metrics
- **−** Plotting needs Matplotlib (>= 3.0.0) or Seaborn (>= 0.9.1) installed separately
- **−** Pure Python; performance on very large datasets is not documented
- **−** Older Python versions need pinned releases (4.3 is last for 3.6)

<sub>no GPU · Docker · Needs Matplotlib (optional, plotting), Seaborn (optional, plotting) · [Repo](https://github.com/sepandhaghighi/pycm) · [🌐 Site ↗](http://www.pycm.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pycm/)</sub>

<a name="oc-sort"></a>
### #&#8288;332 [oc_sort](https://github.com/noahcao/oc_sort) <sub>score [17](../README.md#-how-we-rank "Score 17/100. Adoption: niche (2) · Freshness: recent (53) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Apr 2026</sub>

**Motion-based multi-object tracker for crowded scenes and non-linear movement.**

OC-SORT (CVPR 2023) is a PyTorch multi-object tracker that fixes Kalman filter drift in SORT by re-updating tracks from observations. It takes detections, with YOLOX weights provided, and can be combined with BYTE association and cost metrics such as GIoU and CIoU. Deployment paths cover ONNX, TensorRT, ncnn and C++.

- **+** Association alone runs at about 700 FPS on an i9 CPU when detections are given
- **+** Reported results on MOT17, MOT20, KITTI, DanceTrack and CroHD in the README
- **+** Deployment docs for ONNX, TensorRT and ncnn, plus a C++ implementation
- **+** Pluggable cost metrics (GIoU, CIoU) and BYTE integration
- **−** Pure motion model; appearance matching needs the separate Deep OC-SORT project
- **−** Detection stage is tied to YOLOX codebase and weights
- **−** No tagged releases; install and usage steps live in separate docs files
- **−** Benchmarks use shared hyper-parameters, so per-dataset tuning is left to the user

<sub>GPU optional · Docker · Needs PyTorch, YOLOX, filterpy · Models: YOLOX · [Repo](https://github.com/noahcao/oc_sort) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/oc-sort/)</sub>

<a name="videopipe"></a>
### #&#8288;333 [videopipe](https://github.com/sherlockchou86/videopipe) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: known (31) · Freshness: quiet (23) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · Apache-2.0 · Feb 2026</sub>

**C++ pipeline framework for video analysis with pluggable inference nodes.**

VideoPipe is a C++17 framework for building video analysis apps by linking independent nodes: stream sources, inference, tracking, behavior analysis, OSD, recording and outputs. Inference defaults to OpenCV::DNN, with TensorRT, PaddleInference, ONNXRuntime or multimodal LLM services (Ollama, vLLM, OpenAI-compatible) as alternatives. It ships over 40 sample pipelines and positions itself as a lighter alternative to DeepStream and mxVision.

- **+** Runs CPU-only by default via OpenCV::DNN; CUDA and TensorRT are opt-in CMake flags
- **+** Reads and pushes UDP, RTSP, RTMP and file streams, with Kafka or socket data output
- **+** Includes tracking (IOU, SORT) and line-crossing and parking behavior analysis nodes
- **+** Over 40 sample pipelines, plus a live pipeline status board
- **−** Must be built from source with CMake; no Docker image, last release 2024-04
- **−** Model files and test data are downloaded from Google Drive or Baidu Drive
- **−** Code for Cambricon, Rockchip and Ascend backends is not provided
- **−** Self-rated medium performance; you write C++ to parse each model's output

<sub>GPU optional · Needs OpenCV >= 4.6, GStreamer 1.14.5, GCC >= 7.5, CMake, CUDA (optional), TensorRT (optional), Paddle Inference (optional), ONNX Runtime (optional), Kafka (optional) · Models: OpenCV::DNN, ONNX, TensorRT, PaddleInference, ONNXRuntime · [Repo](https://github.com/sherlockchou86/videopipe) · [📖 Docs ↗](http://www.videopipe.cool/index.php/2024/09/11/videopipetutorials/) · [🌐 Site ↗](http://www.videopipe.cool) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/videopipe/)</sub>

<a name="keras-attention"></a>
### #&#8288;334 [keras-attention](https://github.com/philipperemy/keras-attention) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (27) · Freshness: quiet (27) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · Apache-2.0 · Mar 2026</sub>

**Keras attention layer with Luong and Bahdanau score functions.**

A PyPI package (`attention`) that adds a single Attention layer to Keras models on TensorFlow 2.x. It takes a 3D tensor (batch, timesteps, input_dim), such as LSTM output, and returns a 2D attention vector, with a choice of Luong multiplicative or Bahdanau additive scoring. The README includes an IMDB comparison and toy examples that visualize attention weights.

- **+** Drop-in Keras layer: Attention(units=32, score='luong') after an RNN layer
- **+** Supports both Luong and Bahdanau score functions
- **+** Examples visualize attention weights on toy tasks (add two numbers, find max)
- **+** Tested against TensorFlow 2.8 through 2.14
- **−** Last tested TensorFlow version is 2.14 (Sep 2023); newer versions not listed
- **−** Last release was March 2023
- **−** Returns a pooled 2D vector, not a sequence, limiting seq2seq decoder use
- **−** Only two score functions; no multi-head or transformer-style attention

<sub>GPU optional · Needs TensorFlow 2.0+, Keras · [Repo](https://github.com/philipperemy/keras-attention) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/keras-attention/)</sub>

<a name="tensorflow-agents"></a>
### #&#8288;335 [tensorflow/agents](https://github.com/tensorflow/agents) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: known (31) · Freshness: quiet (19) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · Apache-2.0 · Jan 2026</sub>

**TensorFlow library of reinforcement learning and contextual bandit algorithms.**

TF-Agents implements reinforcement learning agents (DQN, DDQN, DDPG, TD3, REINFORCE, PPO, SAC) and a multi-armed bandits suite as modular TensorFlow components. Each agent bundles a policy with the logic to train it from collected experience, with per-agent train_eval examples and Colab tutorials. It targets classic RL and bandit problems such as CartPole, not LLM agents.

- **+** Seven RL algorithms plus bandit environments and agents in one library
- **+** Modular, tested components with Colab tutorials and runnable train_eval examples
- **+** Stable and nightly PyPI builds, with a table mapping releases to TensorFlow versions
- **−** README says interfaces may change at any time
- **−** Reverb replay buffer works only on Linux
- **−** Needs Keras 2 (TF_USE_LEGACY_KERAS=1); latest listed release 0.19.0 targets TF 2.15
- **−** Not for LLM agents despite the name; no last release tagged

<sub>GPU optional · Needs TensorFlow, tf-keras, TensorFlow Probability, dm-reverb · Models: DQN, DDQN, DDPG, TD3, REINFORCE · [Repo](https://github.com/tensorflow/agents) · [📖 Docs ↗](https://www.tensorflow.org/agents/api_docs/python/tf_agents) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorflow-agents/)</sub>

<a name="deim"></a>
### #&#8288;336 [deim](https://github.com/intellindust-ai-lab/deim) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: niche (6) · Freshness: slowing (43) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · custom license · Mar 2026</sub>

**Training framework for real-time DETR object detectors with faster convergence.**

DEIM is the CVPR 2025 reference code for a DETR training method that improves query matching (Dense O2O) so detectors converge faster. It trains and evaluates D-FINE and RT-DETRv2 based models in sizes N to X on COCO or custom COCO-format datasets. Tooling covers ONNX and TensorRT export, inference scripts, latency benchmarks and FiftyOne visualization.

- **+** COCO results published: DEIM-D-FINE N 43.0 AP at 4M params, X 56.5 AP at 62M
- **+** Exports to ONNX and TensorRT, with onnxruntime, TensorRT and torch inference scripts
- **+** Custom COCO-format datasets, input size and batch size handled through YAML configs
- **+** Also re-implements D-FINE and RT-DETR, with checkpoints for each size
- **−** Object detection only; not an LLM or general-purpose AI tool
- **−** Checkpoints are hosted on Google Drive, not a model hub
- **−** Training examples assume 4 GPUs via torchrun; single-GPU guidance is thin
- **−** License metadata is NOASSERTION while the README badge says Apache 2.0

<sub>GPU required · Needs PyTorch, conda, Python 3.11.9, onnx, onnxsim, TensorRT (optional), FiftyOne (optional) · Models: DEIM-D-FINE (N, S, M, L, X), DEIM-RT-DETRv2 (S, M, M*, L, X), COCO-format datasets, ONNX, TensorRT · [Repo](https://github.com/intellindust-ai-lab/deim) · [🌐 Site ↗](https://www.shihuahuang.cn/DEIM/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deim/)</sub>

<a name="lightautoml"></a>
### #&#8288;337 [lightautoml](https://github.com/sb-ai-lab/lightautoml) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: niche (5) · Freshness: quiet (18) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · Apache-2.0 · Dec 2025</sub>

**AutoML library for tabular, text, image and time series data.**

LightAutoML (LAMA) is a Python AutoML library that trains models from a few lines using presets such as TabularAutoML, or from composable pipeline blocks for feature generation, selection, ML algorithms and hyperparameter optimization. It handles tabular, time series, image and text data, and includes an interpretable WhiteBox (AutoWoE) preset and uplift modeling. Install from PyPI with optional nlp, cv and report extras.

- **+** Preset API trains and predicts on tabular data in a few lines
- **+** Custom pipelines can be assembled from feature, selection and tuning blocks
- **+** Eleven tutorial notebooks cover NLP, uplift, time series, SQL sources and neural nets
- **+** Interpretability tools: WhiteBox preset, ICE/PDP plots, LIME for text
- **−** Full GPU and Spark pipelines live in separate repositories, described as still in progress
- **−** PDF report generation needs system libraries such as cairo and pango
- **−** Classical AutoML only, with no language-model or agent features
- **−** Some courses and video guides are Russian-only

<sub>GPU optional · Needs cairo, pango, gdk-pixbuf, libffi · Models: tabular, time series, text, image · [Repo](https://github.com/sb-ai-lab/lightautoml) · [📖 Docs ↗](https://lightautoml.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lightautoml/)</sub>

<a name="alibi-detect"></a>
### #&#8288;338 [alibi-detect](https://github.com/seldonio/alibi-detect) <sub>score [13](../README.md#-how-we-rank "Score 13/100. Adoption: niche (24) · Freshness: quiet (20) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · custom license · Dec 2025</sub>

**Python library for outlier, adversarial and drift detection on model data.**

Alibi Detect is a Python library with online and offline detectors for outliers, adversarial examples and data drift. It covers tabular, text, image and time series data, and its drift detectors run on TensorFlow, PyTorch or KeOps backends. Detectors use a fit/predict API and can be saved and loaded. The license is reported as NOASSERTION, and the README calls it source-available.

- **+** Broad detector set: Isolation Forest, VAE, MMD, Kolmogorov-Smirnov, Cramér-von Mises, Chi-Squared and more
- **+** Drift detectors run on TensorFlow, PyTorch or KeOps backends
- **+** Built-in preprocessing: hidden-layer extraction and transformers text embeddings
- **+** save_detector and load_detector persist fitted detectors; docs link example notebooks
- **−** Source-available license, not a standard open-source one; check terms before commercial use
- **−** TensorFlow, PyTorch and KeOps backends are not installed by default; extras needed
- **−** Library only; no server, UI or monitoring dashboard included
- **−** Detector coverage is uneven across data types, e.g. no text outlier detectors

<sub>GPU optional · Needs TensorFlow (optional), PyTorch (optional), KeOps (optional), Prophet (optional) · Models: TensorFlow, PyTorch, transformers embeddings · [Repo](https://github.com/seldonio/alibi-detect) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/alibi-detect/)</sub>

<a name="gplearn"></a>
### #&#8288;339 [gplearn](https://github.com/trevorstephens/gplearn) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: niche (12) · Freshness: quiet (30) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · BSD-3-Clause · Jan 2026</sub>

**Symbolic regression with genetic programming and a scikit-learn API.**

gplearn is a Python library that evolves mathematical expressions to fit data using genetic programming. It provides SymbolicRegressor, a binary SymbolicClassifier and SymbolicTransformer for automated feature engineering, all with scikit-learn fit/predict semantics, so they work in scikit-learn pipelines and grid search.

- **+** Drop-in scikit-learn estimators: works with pipelines and grid search
- **+** Produces explicit mathematical expressions instead of opaque model weights
- **+** SymbolicTransformer generates engineered features for downstream models
- **+** Documented on Read the Docs, with CI and coverage badges
- **−** Deliberately limited to symbolic regression, not general genetic programming
- **−** Classification is binary only
- **−** Many parameters to tune to get good results
- **−** Requires a fairly recent scikit-learn version

<sub>no GPU · Needs scikit-learn · Models: SymbolicRegressor, SymbolicClassifier, SymbolicTransformer · [Repo](https://github.com/trevorstephens/gplearn) · [📖 Docs ↗](http://gplearn.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gplearn/)</sub>

<a name="petastorm"></a>
### #&#8288;340 [petastorm](https://github.com/uber/petastorm) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: niche (11) · Freshness: quiet (27) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · Apache-2.0 · Jan 2026</sub>

**Parquet data loader for TensorFlow, PyTorch and Spark training.**

Petastorm is a Python library from Uber ATG that reads Apache Parquet datasets for single-machine or distributed deep learning training and evaluation. It adds a schema layer (Unischema) with codecs for multidimensional arrays and images, and provides readers for TensorFlow, PyTorch and plain Python. A Spark converter materializes DataFrames to Parquet and returns a tf.data.Dataset or PyTorch DataLoader.

- **+** Reads Parquet into tf.data.Dataset, PyTorch DataLoader or plain Python iterators
- **+** Reader supports column selection, row predicates, shuffling, multi-GPU partitioning and local caching
- **+** Spark converter turns a DataFrame into a training dataset in a few calls
- **+** make_batch_reader reads existing non-Petastorm Parquet stores
- **−** Writing Petastorm datasets requires PySpark
- **−** README examples use TF1-style sessions and one-shot iterators, which are dated
- **−** make_batch_reader does not support some native Parquet column types
- **−** Documented URL protocols are only hdfs:// and file://

<sub>GPU optional · Docker · Needs PySpark, Apache Parquet, TensorFlow, PyTorch · Models: TensorFlow, PyTorch · [Repo](https://github.com/uber/petastorm) · [📖 Docs ↗](https://petastorm.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/petastorm/)</sub>

<a name="igel"></a>
### #&#8288;341 [igel](https://github.com/nidhaloff/igel) <sub>score [11](../README.md#-how-we-rank "Score 11/100. Adoption: known (32) · Freshness: quiet (3) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · MIT · Dec 2025</sub>

**YAML-driven CLI to train, evaluate and serve scikit-learn models without code.**

igel wraps scikit-learn and auto-ML backends behind a CLI driven by a YAML or JSON config. Commands cover init, fit, evaluate, predict, experiment, ONNX export and serve, which starts a FastAPI/uvicorn REST endpoint for a trained model. It handles regression, classification and clustering, plus auto-ML tasks such as image and text classification.

- **+** Full workflow from one YAML file: fit, evaluate, predict, experiment, export
- **+** Built-in serve command exposes a FastAPI REST endpoint for a trained model
- **+** Many sklearn regression, classification and clustering algorithms, plus auto-ML tasks
- **+** Reads csv, txt, excel, json and html data; exports sklearn models to ONNX
- **−** Last release was 2021-11-19; the PyPI package may lag the repository
- **−** Served API needs all training columns and equal-length lists; mixed scalars and lists fail
- **−** Auto-ML mode tries many models and is computationally expensive
- **−** Classical ML only; no LLM or deep-learning fine-tuning workflow

<sub>Docker · Needs Python, scikit-learn, FastAPI, uvicorn · Models: scikit-learn regression/classification/clustering, auto-ML image/text/structured data models, ONNX export · port 8000 · [Repo](https://github.com/nidhaloff/igel) · [📖 Docs ↗](https://igel.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/igel/)</sub>

<a name="audiomentations"></a>
### #&#8288;342 [audiomentations](https://github.com/iver56/audiomentations) <sub>score [11](../README.md#-how-we-rank "Score 11/100. Adoption: niche (21) · Freshness: quiet (17) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · MIT · Dec 2025</sub>

**Python library for augmenting audio waveforms in ML training pipelines.**

Audiomentations is a CPU-based Python library that applies randomized transforms to mono or multichannel audio held in NumPy arrays. It offers about 37 waveform transforms, including noise mixing, pitch shift, time stretch, filters, impulse response convolution, room simulation and MP3 compression, chained with a Compose API modeled on albumentations. It fits into TensorFlow/Keras or PyTorch data pipelines.

- **+** Broad transform set: noise, filters, reverb, impulse responses, MP3 compression, pitch and tempo changes
- **+** Albumentations-style Compose API with per-transform probability, installed with pip
- **+** Runs on CPU with mono and multichannel audio, no GPU needed
- **+** Documentation site with guides, example code and example sounds
- **−** CPU only; GPU augmentation needs the separate torch-audiomentations project
- **−** Waveform transforms only; no spectrogram-level augmentation is listed
- **−** Listed platforms: Linux (arm, x86), macOS (arm), Windows (x86) only
- **−** Examples use NumPy float32 arrays, so tensors in PyTorch pipelines need conversion

<sub>no GPU · Needs numpy · [Repo](https://github.com/iver56/audiomentations) · [📖 Docs ↗](https://iver56.github.io/audiomentations/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/audiomentations/)</sub>

<a name="circuit-training"></a>
### #&#8288;343 [circuit_training](https://github.com/google-research/circuit_training) <sub>score [11](../README.md#-how-we-rank "Score 11/100. Adoption: niche (8) · Freshness: quiet (28) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Feb 2026</sub>

**Reinforcement learning framework for placing macros in chip floorplans.**

AlphaChip reproduces the Nature 2021 graph placement method: a PPO agent built on TF-Agents and TensorFlow 2.x that places macros in chip netlists, computing location and orientation. It optimizes wirelength, congestion and density, and uses DREAMPlace for standard-cell placement. Training is distributed across multiple GPUs, with data collection scaling to hundreds of actors.

- **+** Places netlists with hundreds of macros and millions of clustered stdcells, with orientation and fixed macros
- **+** Supports grid alignment, macro spacing constraints and user-defined routing technology parameters
- **+** Distributed training over multiple GPUs; data collection scales to 100s of actors
- **+** Ships a checkpoint pre-trained on 20 TPU blocks, plus pre-training docs
- **−** Linux only; Docker image is Python 3.9 only, local install supports 3.9 to 3.11
- **−** Needs a precompiled placement cost binary and a DREAMPlace build that may need compiling
- **−** Research code with no PyPI package; HEAD breaks when nightly upstream libraries change
- **−** Inputs must be Netlist Protocol Buffer; LEF/DEF conversion is a third-party script

<sub>GPU required · Needs TensorFlow 2.x, TF-Agents, Reverb, DREAMPlace, plc_wrapper_main placement cost binary, PyTorch 1.13.1 · Models: PPO policy checkpoints (TensorFlow SavedModel) · [Repo](https://github.com/google-research/circuit_training) · [📖 Docs ↗](https://github.com/google-research/circuit_training/blob/main/docs/ARIANE.md) · [🌐 Site ↗](https://deepmind.google/discover/blog/how-alphachip-transformed-computer-chip-design/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/circuit-training/)</sub>

<a name="jeelizfacefilter"></a>
### #&#8288;344 [jeelizfacefilter](https://github.com/jeeliz/jeelizfacefilter) <sub>score [9](../README.md#-how-we-rank "Score 9/100. Adoption: niche (30) · Freshness: quiet (0) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · Apache-2.0 · Nov 2025</sub>

**WebGL face detection and head-pose tracking from webcam video, for AR filters.**

JavaScript library that runs a neural network in WebGL to detect and track faces in a WebRTC camera feed. It outputs raw data: detection state, face position and scale, rotation Euler angles, and mouth opening. It ships no 3D engine, with demos for THREE.js, Babylon.js, A-Frame, CSS3D, Canvas2D and Cesium.

- **+** Framework-agnostic raw outputs: detection flag, position, scale, Euler angles
- **+** Tracks multiple faces and supports several simultaneous video sources
- **+** Many demos with source: face swap, glasses try-on, head-controlled cursor
- **+** Alternate neural net files, e.g. NN_4EXPR_1.json for four expressions
- **−** Last tagged release is from 2021-11-12
- **−** Outputs only pose and mouth opening, not dense facial landmarks
- **−** Demos and repository content fall under a separate FaceFilter license note
- **−** Some listed demos are marked as no longer maintained

<sub>Needs WebGL, WebRTC camera · Models: NN_DEFAULT.json, NN_4EXPR_1.json · [Repo](https://github.com/jeeliz/jeelizfacefilter) · [▶️ Demo ↗](https://jeeliz.com/demos/faceFilter/demos/threejs/cube2cv/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jeelizfacefilter/)</sub>

<a name="pyldavis"></a>
### #&#8288;345 [pyldavis](https://github.com/bmabey/pyldavis) <sub>score [8](../README.md#-how-we-rank "Score 8/100. Adoption: niche (10) · Freshness: quiet (2) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · BSD-3-Clause · Dec 2025</sub>

**Interactive visualization of fitted LDA topic models in Python notebooks.**

pyLDAvis is a Python port of the R package LDAvis. It takes a fitted LDA topic model and builds an interactive web visualization for interpreting its topics. The result displays inline in an IPython notebook or saves as a stand-alone HTML file for sharing.

- **+** Saves visualizations as stand-alone HTML files that can be shared without Python
- **+** Installs with pip and renders inline in IPython notebooks
- **+** Based on a published method (Sievert and Shirley, 2014 ACL workshop paper)
- **+** Docs on Read the Docs, plus an overview notebook and video talks
- **−** Visualizes LDA topic models only, not embedding-based or LLM topic methods
- **−** Last release was 2023-04-23, though commits continued into December 2025
- **−** Build badge points to Travis CI, which suggests dated project infrastructure
- **−** Development install instructions are minimal: clone and run setup.py

<sub>no GPU · Needs IPython notebook · Models: LDA topic models · [Repo](https://github.com/bmabey/pyldavis) · [▶️ Demo ↗](http://nbviewer.ipython.org/github/bmabey/pyLDAvis/blob/master/notebooks/pyLDAvis_overview.ipynb) · [📖 Docs ↗](https://pyLDAvis.readthedocs.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyldavis/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
