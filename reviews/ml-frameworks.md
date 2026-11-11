# 🔬 ML frameworks and libraries reviews · Best of Open-Source AI

The libraries models are built and run with: tensor frameworks, model zoos and the tooling around them. Back to the [leaderboard](../README.md#-ml-frameworks-and-libraries).

<sub>🌐 Also on the web: [ML frameworks and libraries on archestack.com](https://archestack.com/best-of-ai/ml-frameworks/), each project on its own page.</sub>

<a name="transformers"></a>
### 🥇 [transformers](https://github.com/huggingface/transformers) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 169k · Apache-2.0 · Nov 2026</sub>

**Python library defining open models for text, vision, audio and multimodal tasks.**

Transformers is a Python model-definition library for text, vision, audio, video and multimodal models, covering inference and training. It provides a high-level Pipeline API and loads checkpoints from the Hugging Face Hub (README cites over 1M). Training frameworks and inference engines such as vLLM, SGLang, Axolotl and llama.cpp reuse its model definitions.

- **+** Pipeline API runs text, audio, vision and multimodal tasks in a few lines
- **+** Model definitions are reused by vLLM, SGLang, Axolotl, DeepSpeed and others
- **+** Loads checkpoints from the Hugging Face Hub, which the README says has over 1M
- **+** Model files are deliberately unabstracted, so they can be edited or used standalone
- **−** README says it is not a modular toolbox of neural net building blocks
- **−** Training API is optimized for Transformers' own PyTorch models
- **−** Requires Python 3.10+ and PyTorch 2.6+
- **−** Installing from source may give unstable code, per the README

<sub>GPU optional · Docker · Needs Python 3.10+, PyTorch 2.6+ · Models: Hugging Face Hub checkpoints, PyTorch · [Repo](https://github.com/huggingface/transformers) · [📖 Docs ↗](https://huggingface.co/docs/transformers/index) · [🌐 Site ↗](https://huggingface.co/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transformers/)</sub>

<a name="pytorch"></a>
### 🥈 [pytorch](https://github.com/pytorch/pytorch) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 105k · custom license · Nov 2026</sub>

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

<a name="ultralytics"></a>
### 🥉 [ultralytics](https://github.com/ultralytics/ultralytics) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 63k · AGPL-3.0 · Nov 2026</sub>

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
### #&#8288;4 [pytorch-image-models](https://github.com/huggingface/pytorch-image-models) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Nov 2026</sub>

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

<a name="supervision"></a>
### #&#8288;5 [supervision](https://github.com/roboflow/supervision) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 52k · MIT · Nov 2026</sub>

**Python toolkit for loading, annotating and counting computer vision detections.**

Supervision is a model-agnostic Python library that wraps detection, classification and segmentation outputs in a common sv.Detections object. It has connectors for Ultralytics, Transformers, MMDetection and Inference, annotators for drawing results, and utilities to load, split, merge and convert YOLO, Pascal VOC and COCO datasets. Tracking, zone counting and speed estimation appear in the linked tutorials.

- **+** Connectors for Ultralytics, Transformers, MMDetection and Inference; rfdetr returns sv.Detections directly
- **+** Dataset utils load, split, merge and convert YOLO, Pascal VOC and COCO
- **+** Configurable annotators such as BoxAnnotator for drawing detections on frames
- **+** Installs with pip; docs, cookbooks and a cheatsheet are available
- **−** Does not train or run models itself; a separate detection model is required
- **−** Requires Python 3.10 or newer
- **−** Inference and dataset download examples need a Roboflow API key
- **−** Tracking and zone features are shown in video tutorials, not the README text

<sub>GPU optional · Needs Python>=3.10, rfdetr (optional), Roboflow Inference (optional), Roboflow API key (optional) · Models: Ultralytics, Transformers, MMDetection, Inference, rfdetr · [Repo](https://github.com/roboflow/supervision) · [▶️ Demo ↗](https://huggingface.co/spaces/Roboflow/Annotators) · [📖 Docs ↗](https://supervision.roboflow.com) · [🌐 Site ↗](https://supervision.roboflow.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/supervision/)</sub>

<a name="diffusers"></a>
### #&#8288;6 [diffusers](https://github.com/huggingface/diffusers) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Nov 2026</sub>

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

<a name="genesis-world"></a>
### #&#8288;7 [genesis-world](https://github.com/genesis-embodied-ai/genesis-world) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Nov 2026</sub>

**Python multi-physics simulator for robotics and physical AI research.**

Genesis World is a Python simulation platform that combines a multi-physics engine (rigid, FEM, MPM, PBD, SPH, IPC, SAP), three renderers (Nyx, Luisa, Pyrender) and the Quadrants compiler. Quadrants lowers Python kernels to CUDA, ROCm, Metal, Vulkan, x86 and ARM64. It loads URDF, MJCF, OBJ, GLB and USD assets, and supports parallel and heterogeneous environments, sensors and a built-in GUI.

- **+** Rigid, FEM, MPM, SPH, PBD and IPC solvers share one scene and state
- **+** Quadrants compiles to CUDA, ROCm, Metal, Vulkan, x86 and ARM64
- **+** Many runnable examples: sensors, controllers, domain randomization, heterogeneous envs
- **+** Parses URDF, MJCF, OBJ, GLB and USD assets
- **−** IPC solver needs pyuipc on Linux or Windows x86 with an NVIDIA GPU
- **−** PyTorch must be installed separately before the package
- **−** Python limited to >=3.10,<3.14
- **−** Nyx renderer is a separate package (gs-nyx) with its own install

<sub>GPU optional · Needs PyTorch, pyuipc (optional), gs-nyx (optional) · Models: URDF, MJCF, OBJ, GLB, USD · [Repo](https://github.com/genesis-embodied-ai/genesis-world) · [📖 Docs ↗](https://genesis-world.readthedocs.io/en/latest/) · [🌐 Site ↗](https://www.genesis.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/genesis-world/)</sub>

<a name="mlx"></a>
### #&#8288;8 [mlx](https://github.com/ml-explore/mlx) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Nov 2026</sub>

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

<a name="ray"></a>
### #&#8288;9 [ray](https://github.com/ray-project/ray) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · Apache-2.0 · Nov 2026</sub>

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

<a name="mediapipe"></a>
### #&#8288;10 [mediapipe](https://github.com/google-ai-edge/mediapipe) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;11 [netron](https://github.com/lutzroeder/netron) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Nov 2026</sub>

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

<a name="onnx"></a>
### #&#8288;12 [onnx](https://github.com/onnx/onnx) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Nov 2026</sub>

**Open model format and operator spec for exchanging ML models between frameworks.**

ONNX defines an extensible computation graph format, built-in operators and standard data types for deep learning and traditional ML models, with a focus on inference. The Python package provides model loading and saving, shape and type inference, opset version conversion and a reference implementation. It is a spec and toolkit, not a runtime; execution is left to other engines.

- **+** Framework-neutral model format with documented IR spec, operator list and versioning rules
- **+** Python API includes shape and type inference and opset version conversion
- **+** Supported across many frameworks, tools and hardware, per the project
- **+** abi3 wheels from Python 3.12; releases published to PyPI with weekly builds
- **−** Does not run models in production; a separate inference runtime is needed
- **−** Scope is inference; training is not a stated focus
- **−** Graph optimizer lives in a separate repository (onnx/optimizer)
- **−** Reference implementation needs the optional onnx[reference] extra

<sub>no GPU · Needs pytest (tests only) · Models: ONNX, deep learning models, traditional ML models · [Repo](https://github.com/onnx/onnx) · [📖 Docs ↗](https://onnx.ai/onnx/) · [🌐 Site ↗](https://onnx.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onnx/)</sub>

<a name="burn"></a>
### #&#8288;13 [burn](https://github.com/tracel-ai/burn) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="flash-attention"></a>
### #&#8288;14 [flash-attention](https://github.com/dao-ailab/flash-attention) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · BSD-3-Clause · Nov 2026</sub>

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
### #&#8288;15 [deepface](https://github.com/serengil/deepface) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Nov 2026</sub>

**Python library for face verification, search and attribute analysis.**

DeepFace wraps face recognition models (VGG-Face, FaceNet, ArcFace, Dlib, SFace, GhostFaceNet, Buffalo_L) and about 20 detector backends behind single calls such as verify, find, analyze and represent. It also covers age, gender, emotion and race prediction, anti-spoofing, webcam streaming, and registering embeddings in databases such as Postgres, Mongo, Pinecone or Milvus. A gunicorn-based REST API ships in the repo.

- **+** One-line calls cover detect, align, represent and verify; model and detector swap by argument
- **+** Database-backed register, identify and search with ANN support across many vector and SQL stores
- **+** Runs on onnxruntime by default; TensorFlow or PyTorch available as install extras
- **+** Anti-spoofing, webcam streaming and a REST API are included in the same repo
- **−** Built-in race and ethnicity prediction carries bias and misuse concerns
- **−** Defaults are VGG-Face and the OpenCV detector, which the README does not rank as most accurate
- **−** Browser UI is a separate repository (deepface-react-ui)

<sub>GPU optional · Docker + Compose · Needs onnxruntime, TensorFlow (optional), PyTorch (optional), Postgres, Mongo or other vector DB (optional) · Models: VGG-Face, Facenet, Facenet512, OpenFace, DeepFace · [Repo](https://github.com/serengil/deepface) · [🌐 Site ↗](https://deepface.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepface/)</sub>

<a name="jax"></a>
### #&#8288;16 [jax](https://github.com/jax-ml/jax) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Nov 2026</sub>

**Python library for composable autodiff, JIT and vectorization of NumPy-style code.**

JAX is a Python array library that transforms NumPy-style functions with grad (forward and reverse-mode autodiff), jit (XLA compilation) and vmap (auto-vectorization). The transformations compose, and code runs on CPU, NVIDIA GPU, Google TPU and AMD GPU, with experimental Apple and Intel GPU support. Scaling across devices uses automatic, explicit or manual (shard_map) sharding.

- **+** grad, jit and vmap compose arbitrarily, including higher-order derivatives and per-example gradients
- **+** Differentiates through Python loops, branches, recursion and closures
- **+** Three sharding modes (auto, explicit, manual) for scaling across many devices
- **+** Compiles via XLA to CPU, NVIDIA, TPU and AMD targets using pip extras
- **−** README calls it a research project with sharp edges; not an official Google product
- **−** jit restricts the Python control flow a function can use
- **−** No native Windows GPU support; WSL2 GPU is experimental
- **−** Apple and Intel GPU backends are experimental

<sub>GPU optional · Needs XLA, NumPy · [Repo](https://github.com/jax-ml/jax) · [📖 Docs ↗](https://docs.jax.dev/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jax/)</sub>

<a name="lerobot"></a>
### #&#8288;17 [lerobot](https://github.com/huggingface/lerobot) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Nov 2026</sub>

**PyTorch library for robot control, datasets and policy training.**

LeRobot provides a Python Robot interface for arms and humanoids (SO100, Koch, Reachy2, Unitree G1 and others), a Parquet plus MP4 dataset format hosted on the Hugging Face Hub, and PyTorch implementations of imitation learning, RL, VLA, world and reward models. CLI tools cover recording, training and evaluation on benchmarks such as LIBERO and MetaWorld.

- **+** One Robot interface covers many arms, humanoids and teleop devices; plugins auto-discovered by package prefix
- **+** LeRobotDataset format streams from the Hub, with tools to split, merge and edit episodes
- **+** Many policies in pure PyTorch: ACT, Diffusion, Pi0, SmolVLA, GR00T N1.7, HIL-SERL
- **+** One CLI flow for record, train and eval, including simulated benchmarks
- **−** README gives no RAM or VRAM figures; it points to a separate hardware guide
- **−** Real-world use needs supported physical hardware; named simulation benchmarks are LIBERO and MetaWorld
- **−** Some items, such as QC-FQL, are marked coming soon
- **−** Custom robots or policies require implementing the interfaces yourself

<sub>Docker + Compose · Needs PyTorch, Hugging Face Hub · Models: ACT, Diffusion, VQ-BeT, HIL-SERL, TDMPC · [Repo](https://github.com/huggingface/lerobot) · [▶️ Demo ↗](https://huggingface.co/spaces/lerobot/robot-folding) · [📖 Docs ↗](https://huggingface.co/docs/lerobot/index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lerobot/)</sub>

<a name="tinygrad"></a>
### #&#8288;18 [tinygrad](https://github.com/tinygrad/tinygrad) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Nov 2026</sub>

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

<a name="onnxruntime"></a>
### #&#8288;19 [onnxruntime](https://github.com/microsoft/onnxruntime) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Nov 2026</sub>

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

<sub>GPU optional · Docker · Models: ONNX, PyTorch, TensorFlow/Keras, scikit-learn, LightGBM · [Repo](https://github.com/microsoft/onnxruntime) · [📖 Docs ↗](https://onnxruntime.ai/docs) · [🌐 Site ↗](https://onnxruntime.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onnxruntime/)</sub>

<a name="scikit-learn"></a>
### #&#8288;20 [scikit-learn](https://github.com/scikit-learn/scikit-learn) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · BSD-3-Clause · Nov 2026</sub>

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

<a name="triton"></a>
### #&#8288;21 [triton](https://github.com/triton-lang/triton) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Nov 2026</sub>

**Python-based language and compiler for writing custom GPU kernels.**

Triton is a Python DSL and MLIR/LLVM-based compiler for writing tiled deep-learning kernels that compile to NVIDIA and AMD GPU code. It aims for higher productivity than CUDA and more flexibility than other DSLs. It installs via pip, with wheels for CPython 3.10-3.14, and includes a CPU interpreter mode for debugging.

- **+** Kernels are written in Python and compiled through MLIR and LLVM to PTX or AMDGCN
- **+** TRITON_INTERPRET=1 runs kernels without a GPU, allowing Python breakpoints
- **+** Many debug knobs: per-pass MLIR IR dumps, kernel IR override, reproducer files, autotune printing
- **+** Targets both NVIDIA (compute capability 8.0+) and AMD (ROCm 6.2+) GPUs
- **−** Linux only; CPU backend is listed as under development
- **−** Building from source needs a matching LLVM version; LLVM has no stable API
- **−** No single command to run all tests; running them needs a GPU or the nogpu subset
- **−** Aimed at kernel authors, not a ready-made model runner

<sub>GPU required · Needs LLVM, PyTorch (for tests), CUDA or ROCm · [Repo](https://github.com/triton-lang/triton) · [📖 Docs ↗](https://triton-lang.org) · [🌐 Site ↗](https://triton-lang.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/triton/)</sub>

<a name="kornia"></a>
### #&#8288;22 [kornia](https://github.com/kornia/kornia) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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

<a name="tensorflow"></a>
### #&#8288;23 [tensorflow](https://github.com/tensorflow/tensorflow) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (100) · Freshness: active (94) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 202k · Apache-2.0 · Nov 2026</sub>

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

<a name="xgboost"></a>
### #&#8288;24 [xgboost](https://github.com/dmlc/xgboost) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Nov 2026</sub>

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

<a name="transformers-js"></a>
### #&#8288;25 [transformers.js](https://github.com/huggingface/transformers.js) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="shap"></a>
### #&#8288;26 [shap](https://github.com/shap/shap) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Nov 2026</sub>

**Python library that explains ML model predictions with Shapley values.**

SHAP computes per-feature attributions for model predictions using Shapley values. It has specialised explainers for tree ensembles (XGBoost, LightGBM, CatBoost, scikit-learn, pyspark), deep networks (TensorFlow/Keras, preliminary PyTorch), linear models and Hugging Face transformers, plus a model-agnostic Kernel explainer. Results are shown with waterfall, force, beeswarm, scatter, bar and text plots.

- **+** Tree SHAP is an exact algorithm with C++ implementations for major gradient boosting libraries
- **+** Covers trees, deep nets, linear models, transformers and arbitrary functions through one Explainer API
- **+** Built-in plots for single predictions and whole datasets, interactive in notebooks
- **+** Installs from PyPI or conda-forge
- **−** KernelExplainer is slower than the model-specific explainers because it makes no model assumptions
- **−** DeepExplainer is approximate; PyTorch support is described as preliminary
- **−** GPU Tree SHAP needs a source build with CUDA toolkit and SHAP_ENABLE_CUDA set
- **−** Some README examples use older Keras/TensorFlow session APIs

<sub>GPU optional · Needs CUDA toolkit (optional, for GPU Tree SHAP) · Models: XGBoost, LightGBM, CatBoost, scikit-learn, pyspark · [Repo](https://github.com/shap/shap) · [▶️ Demo ↗](https://mybinder.org/v2/gh/shap/shap/main) · [📖 Docs ↗](https://shap.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/shap/)</sub>

<a name="sentence-transformers"></a>
### #&#8288;27 [sentence-transformers](https://github.com/huggingface/sentence-transformers) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Nov 2026</sub>

**Python library for computing, training and reranking with text embedding models.**

Sentence Transformers is a Python library that computes dense embeddings, sparse (SPLADE-style) embeddings, ColBERT-style multi-vector embeddings and Cross-Encoder reranker scores through one API. It loads models from the 15,000+ on the Hugging Face Hub and includes trainers and loss functions for fine-tuning on your own data.

- **+** Four model types (dense, sparse, multi-vector, cross-encoder) behind one consistent encode/similarity/rank API
- **+** Loads 15,000+ pretrained models from the Hugging Face Hub, including MTEB leaderboard models
- **+** Built-in training with 20+ embedding losses and evaluation during training
- **+** Optional extras for image, audio, video, ONNX and OpenVINO
- **−** Library only: no HTTP server, UI or vector store included
- **−** Requires Python 3.10+, PyTorch 2.2+ and transformers v5.0+
- **−** Model weights download from the Hugging Face Hub; gated models need login
- **−** README states no RAM or GPU requirements

<sub>GPU optional · Needs PyTorch 2.2+, transformers 5.0+, Hugging Face Hub · Models: Sentence Transformer, Cross-Encoder, Sparse Encoder, Multi-Vector Encoder, BERT · [Repo](https://github.com/huggingface/sentence-transformers) · [📖 Docs ↗](https://www.sbert.net/docs/quickstart.html) · [🌐 Site ↗](https://www.sbert.net) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sentence-transformers/)</sub>

<a name="mnn"></a>
### #&#8288;28 [mnn](https://github.com/alibaba/mnn) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="isaaclab"></a>
### #&#8288;29 [isaaclab](https://github.com/isaac-sim/isaaclab) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · BSD-3-Clause · Nov 2026</sub>

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

<a name="nltk"></a>
### #&#8288;30 [nltk](https://github.com/nltk/nltk) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Nov 2026</sub>

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

<a name="fiftyone"></a>
### #&#8288;31 [fiftyone](https://github.com/voxel51/fiftyone) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="autogluon"></a>
### #&#8288;32 [autogluon](https://github.com/autogluon/autogluon) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="skypilot"></a>
### #&#8288;33 [skypilot](https://github.com/skypilot-org/skypilot) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="spacy"></a>
### #&#8288;34 [spacy](https://github.com/explosion/spacy) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Oct 2026</sub>

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
### #&#8288;35 [fastai](https://github.com/fastai/fastai) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · Apache-2.0 · Sep 2026</sub>

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

<a name="paddle"></a>
### #&#8288;36 [paddle](https://github.com/paddlepaddle/paddle) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Nov 2026</sub>

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

<a name="keras"></a>
### #&#8288;37 [keras](https://github.com/keras-team/keras) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Nov 2026</sub>

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

<a name="datasets"></a>
### #&#8288;38 [datasets](https://github.com/huggingface/datasets) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Nov 2026</sub>

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

<a name="prophet"></a>
### #&#8288;39 [prophet](https://github.com/meta/prophet) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Oct 2026</sub>

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

<a name="tvm"></a>
### #&#8288;40 [tvm](https://github.com/apache/tvm) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;41 [tokenizers](https://github.com/huggingface/tokenizers) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="metaflow"></a>
### #&#8288;42 [metaflow](https://github.com/netflix/metaflow) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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

<a name="tabpfn"></a>
### #&#8288;43 [tabpfn](https://github.com/priorlabs/tabpfn) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="feast"></a>
### #&#8288;44 [feast](https://github.com/feast-dev/feast) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="models"></a>
### #&#8288;45 [models](https://github.com/tensorflow/models) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: widely used (97) · Freshness: active (92) · Maintenance: fair (55) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · custom license · Nov 2026</sub>

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

<a name="pytorch-lightning"></a>
### #&#8288;46 [pytorch-lightning](https://github.com/lightning-ai/pytorch-lightning) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · Apache-2.0 · Sep 2026</sub>

**PyTorch training framework that removes loop, device and distributed boilerplate.**

PyTorch Lightning wraps PyTorch models in a LightningModule and a Trainer that handles the training loop, mixed precision, checkpointing, logging and multi-device scaling. The same package ships Lightning Fabric, a lower-level API that keeps your own loop and adds device placement and distributed strategies (DDP, FSDP, DeepSpeed). Runs on CPU, CUDA, Apple Silicon (MPS) and TPU.

- **+** Same code scales from CPU to multi-node GPU or TPU by changing Trainer arguments
- **+** Fabric offers a minimal-diff path for existing PyTorch loops, with DDP, FSDP and DeepSpeed
- **+** Built-in early stopping and checkpointing callbacks; loggers for TensorBoard, W&B, Comet, MLflow
- **+** Exports to TorchScript and ONNX; README cites about 300 ms per epoch overhead
- **−** Training only; serving needs the separate LitServe project
- **−** Trainer requires restructuring code into LightningModule hooks
- **−** README promotes Lightning Cloud, and most examples run as Lightning Studios
- **−** Abstraction layer over PyTorch can complicate debugging unusual loops

<sub>GPU optional · Needs PyTorch · Models: PyTorch nn.Module, TorchScript export, ONNX export · [Repo](https://github.com/lightning-ai/pytorch-lightning) · [📖 Docs ↗](https://pytorch-lightning.readthedocs.io/en/stable/) · [🌐 Site ↗](https://lightning.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-lightning/)</sub>

<a name="ncnn"></a>
### #&#8288;47 [ncnn](https://github.com/tencent/ncnn) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Nov 2026</sub>

**C++ neural network inference library for mobile, embedded and desktop devices.**

ncnn runs neural network inference on CPU or Vulkan GPU with no third-party runtime dependencies. It ships prebuilt packages for Android, iOS, HarmonyOS, macOS, Linux, Windows and WebAssembly, plus cross-compile guides for ARM, MIPS, RISC-V and LoongArch boards. The pnnx tool converts PyTorch and ONNX models to ncnn's param/bin format, and C++ and Python APIs are provided.

- **+** No third-party runtime dependencies; CPU and Vulkan GPU backends
- **+** Prebuilt packages for Android, iOS, HarmonyOS, Windows, Linux, macOS and WebAssembly
- **+** Builds for many architectures: ARM, MIPS, ppc64, riscv64, loongarch64
- **+** pnnx converts PyTorch and ONNX models; C++ and Python APIs
- **−** Inference only; training is not covered
- **−** Models must be converted to ncnn param/bin format first
- **−** No HTTP serving layer; it is an embedded library
- **−** License detected as NOASSERTION; README badge says BSD 3-Clause

<sub>GPU optional · Models: PyTorch (via pnnx), ONNX (via pnnx), ncnn param/bin · [Repo](https://github.com/tencent/ncnn) · [📖 Docs ↗](https://github.com/Tencent/ncnn/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ncnn/)</sub>

<a name="ggml"></a>
### #&#8288;48 [ggml](https://github.com/ggml-org/ggml) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Nov 2026</sub>

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

<a name="vowpal-wabbit"></a>
### #&#8288;49 [vowpal_wabbit](https://github.com/vowpalwabbit/vowpal_wabbit) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · custom license · Sep 2026</sub>

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

<a name="vision"></a>
### #&#8288;50 [vision](https://github.com/pytorch/vision) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · BSD-3-Clause · Nov 2026</sub>

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

<a name="optuna"></a>
### #&#8288;51 [optuna](https://github.com/optuna/optuna) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

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

<a name="sentencepiece"></a>
### #&#8288;52 [sentencepiece](https://github.com/google/sentencepiece) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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

<a name="modelscope"></a>
### #&#8288;53 [modelscope](https://github.com/modelscope/modelscope) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Nov 2026</sub>

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

<sub>GPU optional · Docker · Needs PyTorch, TensorFlow, ONNX, mmcv-full, libsndfile, ModelScope Hub · Models: PyTorch, TensorFlow, ONNX, LLM, multi-modal · [Repo](https://github.com/modelscope/modelscope) · [📖 Docs ↗](https://modelscope.cn/docs/%E7%8E%AF%E5%A2%83%E5%AE%89%E8%A3%85) · [🌐 Site ↗](https://www.modelscope.cn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/modelscope/)</sub>

<a name="smile"></a>
### #&#8288;54 [smile](https://github.com/haifengl/smile) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · custom license · Nov 2026</sub>

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
### #&#8288;55 [pytorch-metric-learning](https://github.com/kevinmusgrave/pytorch-metric-learning) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Nov 2026</sub>

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

<a name="wandb"></a>
### #&#8288;56 [wandb](https://github.com/wandb/wandb) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Nov 2026</sub>

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
### #&#8288;57 [cutlass](https://github.com/nvidia/cutlass) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Nov 2026</sub>

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

<a name="sktime"></a>
### #&#8288;58 [sktime](https://github.com/sktime/sktime) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · BSD-3-Clause · Nov 2026</sub>

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

<a name="darts"></a>
### #&#8288;59 [darts](https://github.com/unit8co/darts) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (49) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="opencompass"></a>
### #&#8288;60 [opencompass](https://github.com/open-compass/opencompass) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="flashinfer"></a>
### #&#8288;61 [flashinfer](https://github.com/flashinfer-ai/flashinfer) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (30) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="river"></a>
### #&#8288;62 [river](https://github.com/online-ml/river) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · BSD-3-Clause · Nov 2026</sub>

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

<a name="dlib"></a>
### #&#8288;63 [dlib](https://github.com/davisking/dlib) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (65) · Freshness: active (96) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · BSL-1.0 · Nov 2026</sub>

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

<a name="gymnasium"></a>
### #&#8288;64 [gymnasium](https://github.com/farama-foundation/gymnasium) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Nov 2026</sub>

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

<a name="pyod"></a>
### #&#8288;65 [pyod](https://github.com/yzhao062/pyod) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · BSD-2-Clause · Oct 2026</sub>

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

<a name="qlib"></a>
### #&#8288;66 [qlib](https://github.com/microsoft/qlib) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: patchy (35) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Oct 2026</sub>

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
### #&#8288;67 [candle](https://github.com/huggingface/candle) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Nov 2026</sub>

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

<a name="lightgbm"></a>
### #&#8288;68 [lightgbm](https://github.com/lightgbm-org/lightgbm) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2026</sub>

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

<a name="umap"></a>
### #&#8288;69 [umap](https://github.com/lmcinnes/umap) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · BSD-3-Clause · Nov 2026</sub>

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

<a name="pytorch-geometric"></a>
### #&#8288;70 [pytorch_geometric](https://github.com/pyg-team/pytorch_geometric) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Nov 2026</sub>

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

<a name="monai"></a>
### #&#8288;71 [monai](https://github.com/project-monai/monai) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (44) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.8k · Apache-2.0 · Nov 2026</sub>

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

<a name="lm-evaluation-harness"></a>
### #&#8288;72 [lm-evaluation-harness](https://github.com/eleutherai/lm-evaluation-harness) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Sep 2026</sub>

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

<a name="accelerate"></a>
### #&#8288;73 [accelerate](https://github.com/huggingface/accelerate) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="flax"></a>
### #&#8288;74 [flax](https://github.com/google/flax) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="transformerengine"></a>
### #&#8288;75 [transformerengine](https://github.com/nvidia/transformerengine) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="hanlp"></a>
### #&#8288;76 [hanlp](https://github.com/hankcs/hanlp) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: widely used (89) · Freshness: recent (70) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

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

<a name="finrl"></a>
### #&#8288;77 [finrl](https://github.com/ai4finance-foundation/finrl) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (71) · Freshness: active (95) · Maintenance: fair (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Oct 2026</sub>

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

<a name="stable-baselines3"></a>
### #&#8288;78 [stable-baselines3](https://github.com/dlr-rm/stable-baselines3) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

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

<a name="bitsandbytes"></a>
### #&#8288;79 [bitsandbytes](https://github.com/bitsandbytes-foundation/bitsandbytes) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · MIT · Oct 2026</sub>

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

<a name="flower"></a>
### #&#8288;80 [flower](https://github.com/flwrlabs/flower) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (33) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="anomalib"></a>
### #&#8288;81 [anomalib](https://github.com/open-edge-platform/anomalib) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="dali"></a>
### #&#8288;82 [dali](https://github.com/nvidia/dali) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Nov 2026</sub>

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

<a name="sahi"></a>
### #&#8288;83 [sahi](https://github.com/obss/sahi) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · MIT · Nov 2026</sub>

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

<a name="clearml"></a>
### #&#8288;84 [clearml](https://github.com/clearml/clearml) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="vit-pytorch"></a>
### #&#8288;85 [vit-pytorch](https://github.com/lucidrains/vit-pytorch) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: widely used (81) · Freshness: active (92) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Nov 2026</sub>

**PyTorch implementations of Vision Transformer and many of its variants.**

A pip-installable PyTorch library with compact implementations of ViT and dozens of variants, including SimpleViT, NaViT, CaiT, CrossViT, MaxViT and MobileViT, plus masked autoencoder and DINO wrappers. Each model is a plain nn.Module built from hyperparameters, with a short usage snippet in the README. It ships no pretrained weights; the README points to timm for those.

- **+** Covers many ViT variants (NaViT, CaiT, CrossViT, LeViT, CvT, MaxViT) with similar constructors
- **+** Includes distillation, masked autoencoder and DINO wrappers for training
- **+** Installs with pip install vit-pytorch; MIT licensed
- **+** Each model has a runnable snippet showing input and output shapes
- **−** No pretrained weights; README refers to timm for pretrained models
- **−** No training scripts, datasets or benchmark results in the README
- **−** README is a list of snippets; no API reference or docs site
- **−** NaViT nested-tensor variant requires PyTorch 2.5

<sub>GPU optional · Needs PyTorch, torchvision · Models: ViT, SimpleViT, NaViT, CaiT, CrossViT · [Repo](https://github.com/lucidrains/vit-pytorch) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vit-pytorch/)</sub>

<a name="bayesianoptimization"></a>
### #&#8288;86 [bayesianoptimization](https://github.com/bayesian-optimization/bayesianoptimization) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (43) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · MIT · Oct 2026</sub>

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

<a name="corenlp"></a>
### #&#8288;87 [corenlp](https://github.com/stanfordnlp/corenlp) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · GPL-3.0 · Sep 2026</sub>

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

<a name="skorch"></a>
### #&#8288;88 [skorch](https://github.com/skorch-dev/skorch) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · BSD-3-Clause · Nov 2026</sub>

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
### #&#8288;89 [flash-linear-attention](https://github.com/fla-org/flash-linear-attention) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Nov 2026</sub>

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

<a name="carla"></a>
### #&#8288;90 [carla](https://github.com/carla-simulator/carla) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (66) · Freshness: recent (80) · Maintenance: patchy (45) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

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

<a name="recommenders"></a>
### #&#8288;91 [recommenders](https://github.com/recommenders-team/recommenders) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (77) · Freshness: recent (70) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Nov 2026</sub>

**Python recommender-system library with notebooks for classic and deep learning models.**

Recommenders is a Python package and set of Jupyter notebooks for building, evaluating and tuning recommendation models. It includes about 30 algorithms (ALS, SAR, NCF, LightGCN, SASRec, xDeepFM, BPR, VAEs and others), plus utilities for dataset loading, train/test splitting and offline metrics. It is a Linux Foundation AI & Data project and ships a MovieLens benchmark notebook.

- **+** About 30 algorithms, each with a quick-start or deep-dive notebook
- **+** Includes data splitters, loaders and offline metrics (MAP, nDCG, precision, recall, RMSE)
- **+** Benchmark notebook compares algorithms on MovieLens 100k with reported results
- **+** Core package installs with pip or uv and runs all CPU notebooks
- **−** Not a serving system; the operationalization example targets Azure only
- **−** Spark and GPU models need extra installs via [spark] or [gpu] extras
- **−** Some models sit under an [experimental] extra and are not thoroughly tested
- **−** Last release 1.2.1 (Dec 2024); no LLM-based recommenders listed

<sub>GPU optional · Needs Python 3.11, gcc, Jupyter, PySpark (optional) · Models: ALS, SAR, NCF, LightGCN, SASRec · [Repo](https://github.com/recommenders-team/recommenders) · [📖 Docs ↗](https://readthedocs.org/projects/microsoft-recommenders/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/recommenders/)</sub>

<a name="stanza"></a>
### #&#8288;92 [stanza](https://github.com/stanfordnlp/stanza) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (39) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · custom license · Oct 2026</sub>

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

<a name="h2o-3"></a>
### #&#8288;93 [h2o-3](https://github.com/h2oai/h2o-3) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (36) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Nov 2026</sub>

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

<a name="causalml"></a>
### #&#8288;94 [causalml](https://github.com/uber/causalml) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · custom license · Oct 2026</sub>

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
### #&#8288;95 [deeplabcut](https://github.com/deeplabcut/deeplabcut) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · LGPL-3.0 · Sep 2026</sub>

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

<a name="dvc"></a>
### #&#8288;96 [dvc](https://github.com/treeverse/dvc) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (69) · Freshness: active (96) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="cv-cuda"></a>
### #&#8288;97 [cv-cuda](https://github.com/cvcuda/cv-cuda) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · custom license · Oct 2026</sub>

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

<a name="ivy"></a>
### #&#8288;98 [ivy](https://github.com/unifyai/ivy) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (64) · Freshness: recent (72) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · custom license · Nov 2026</sub>

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

<sub>Needs PyTorch, TensorFlow, JAX, NumPy · Models: PyTorch (source), TensorFlow (target), JAX (target), NumPy (target) · [Repo](https://github.com/unifyai/ivy) · [📖 Docs ↗](https://ivy-llc.github.io/docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ivy/)</sub>

<a name="xformers"></a>
### #&#8288;99 [xformers](https://github.com/facebookresearch/xformers) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (54) · Freshness: active (93) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Oct 2026</sub>

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

<a name="interpret"></a>
### #&#8288;100 [interpret](https://github.com/interpretml/interpret) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (31) · Freshness: active (95) · Maintenance: fair (54) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · MIT · Nov 2026</sub>

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

<a name="cuml"></a>
### #&#8288;101 [cuml](https://github.com/nvidia/cuml) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · Apache-2.0 · Nov 2026</sub>

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

<a name="detectron2"></a>
### #&#8288;102 [detectron2](https://github.com/facebookresearch/detectron2) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (88) · Freshness: recent (70) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Oct 2026</sub>

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

<a name="pysyft"></a>
### #&#8288;103 [pysyft](https://github.com/openmined/pysyft) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: popular (51) · Freshness: recent (70) · Maintenance: fair (59) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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

<a name="pytorch3d"></a>
### #&#8288;104 [pytorch3d](https://github.com/facebookresearch/pytorch3d) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: popular (51) · Freshness: active (86) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10.0k · custom license · Nov 2026</sub>

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

<a name="catboost"></a>
### #&#8288;105 [catboost](https://github.com/catboost/catboost) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (46) · Freshness: active (93) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="pytorch-grad-cam"></a>
### #&#8288;106 [pytorch-grad-cam](https://github.com/jacobgil/pytorch-grad-cam) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Nov 2026</sub>

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

<a name="pyro"></a>
### #&#8288;107 [pyro](https://github.com/pyro-ppl/pyro) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (45) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.1k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;108 [dowhy](https://github.com/py-why/dowhy) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (41) · Freshness: active (84) · Maintenance: patchy (43) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · MIT · Nov 2026</sub>

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

<a name="swe-bench"></a>
### #&#8288;109 [swe-bench](https://github.com/swe-bench/swe-bench) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Sep 2026</sub>

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

<a name="synapseml"></a>
### #&#8288;110 [synapseml](https://github.com/microsoft/synapseml) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (15) · Freshness: active (97) · Maintenance: fair (56) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · MIT · Nov 2026</sub>

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

<a name="apex"></a>
### #&#8288;111 [apex](https://github.com/nvidia/apex) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (45) · Freshness: active (100) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · BSD-3-Clause · Sep 2026</sub>

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

<a name="deepep"></a>
### #&#8288;112 [deepep](https://github.com/deepseek-ai/deepep) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (54) · Freshness: recent (80) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

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

<a name="autograd"></a>
### #&#8288;113 [autograd](https://github.com/hips/autograd) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (37) · Freshness: active (100) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · MIT · Nov 2026</sub>

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

<a name="retinexformer"></a>
### #&#8288;114 [retinexformer](https://github.com/caiyuanhao1998/retinexformer) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Nov 2026</sub>

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

<a name="xuance"></a>
### #&#8288;115 [xuance](https://github.com/agi-brain/xuance) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · MIT · Oct 2026</sub>

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

<a name="mlpack"></a>
### #&#8288;116 [mlpack](https://github.com/mlpack/mlpack) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · custom license · Nov 2026</sub>

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

<a name="dopamine"></a>
### #&#8288;117 [dopamine](https://github.com/google/dopamine) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (56) · Freshness: recent (70) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="open-spiel"></a>
### #&#8288;118 [open_spiel](https://github.com/google-deepmind/open_spiel) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="tensorboard"></a>
### #&#8288;119 [tensorboard](https://github.com/tensorflow/tensorboard) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (33) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="face-recognition"></a>
### #&#8288;120 [face_recognition](https://github.com/ageitgey/face_recognition) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: widely used (94) · Freshness: recent (58) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 57k · MIT · Jun 2026</sub>

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

<a name="jetson-containers"></a>
### #&#8288;121 [jetson-containers](https://github.com/dusty-nv/jetson-containers) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: weak (13) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · custom license · Oct 2026</sub>

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

<a name="airsim"></a>
### #&#8288;122 [airsim](https://github.com/microsoft/airsim) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (73) · Freshness: recent (70) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · custom license · Sep 2026</sub>

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

<a name="deepgemm"></a>
### #&#8288;123 [deepgemm](https://github.com/deepseek-ai/deepgemm) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (46) · Freshness: active (82) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · MIT · Oct 2026</sub>

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

<a name="captum"></a>
### #&#8288;124 [captum](https://github.com/meta-pytorch/captum) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (19) · Freshness: active (98) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · BSD-3-Clause · Oct 2026</sub>

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

<a name="textblob"></a>
### #&#8288;125 [textblob](https://github.com/sloria/textblob) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (48) · Freshness: recent (70) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · MIT · Nov 2026</sub>

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

<a name="coremltools"></a>
### #&#8288;126 [coremltools](https://github.com/apple/coremltools) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (17) · Freshness: active (85) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.5k · BSD-3-Clause · Sep 2026</sub>

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

<a name="mlxtend"></a>
### #&#8288;127 [mlxtend](https://github.com/rasbt/mlxtend) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: patchy (31) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · custom license · Sep 2026</sub>

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

<a name="torchio"></a>
### #&#8288;128 [torchio](https://github.com/torchio-project/torchio) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · Apache-2.0 · Oct 2026</sub>

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

<a name="sonnet"></a>
### #&#8288;129 [sonnet](https://github.com/google-deepmind/sonnet) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (50) · Freshness: recent (70) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10.0k · Apache-2.0 · Oct 2026</sub>

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

<a name="pyaudioanalysis"></a>
### #&#8288;130 [pyaudioanalysis](https://github.com/tyiannak/pyaudioanalysis) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Oct 2026</sub>

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

<a name="openmythos"></a>
### #&#8288;131 [openmythos](https://github.com/kyegomez/openmythos) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (67) · Freshness: recent (70) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · May 2026</sub>

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

<a name="paddledetection"></a>
### #&#8288;132 [paddledetection](https://github.com/paddlepaddle/paddledetection) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (65) · Freshness: recent (57) · Maintenance: weak (14) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Mar 2026</sub>

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

<a name="tsfresh"></a>
### #&#8288;133 [tsfresh](https://github.com/blue-yonder/tsfresh) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: known (48) · Freshness: active (90) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · MIT · Jul 2026</sub>

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

<a name="surprise"></a>
### #&#8288;134 [surprise](https://github.com/nicolashug/surprise) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (30) · Freshness: recent (73) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.8k · BSD-3-Clause · May 2026</sub>

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

<a name="object-detection-metrics"></a>
### #&#8288;135 [object-detection-metrics](https://github.com/rafaelpadilla/object-detection-metrics) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · MIT · Oct 2026</sub>

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

<a name="hyperopt"></a>
### #&#8288;136 [hyperopt](https://github.com/hyperopt/hyperopt) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: known (37) · Freshness: active (93) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · custom license · Jul 2026</sub>

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

<a name="gluonts"></a>
### #&#8288;137 [gluonts](https://github.com/awslabs/gluonts) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · Apache-2.0 · Oct 2026</sub>

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

<a name="react-native-fast-tflite"></a>
### #&#8288;138 [react-native-fast-tflite](https://github.com/margelo/react-native-fast-tflite) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (3) · Freshness: active (98) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Sep 2026</sub>

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
### #&#8288;139 [time-series-library](https://github.com/thuml/time-series-library) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (62) · Freshness: recent (57) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Apr 2026</sub>

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

<a name="kaolin"></a>
### #&#8288;140 [kaolin](https://github.com/nvidiagameworks/kaolin) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (14) · Freshness: recent (77) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Oct 2026</sub>

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

<a name="pycaret"></a>
### #&#8288;141 [pycaret](https://github.com/pycaret/pycaret) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: known (50) · Freshness: slowing (47) · Maintenance: weak (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · custom license · May 2026</sub>

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

<a name="tsai"></a>
### #&#8288;142 [tsai](https://github.com/timeseriesai/tsai) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (23) · Freshness: active (84) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · Apache-2.0 · Jun 2026</sub>

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

<a name="gsplat"></a>
### #&#8288;143 [gsplat](https://github.com/nerfstudio-project/gsplat) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (21) · Freshness: recent (74) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Sep 2026</sub>

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

<a name="morph-net"></a>
### #&#8288;144 [morph-net](https://github.com/google-research/morph-net) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · Apache-2.0 · Nov 2026</sub>

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

<a name="deepchem"></a>
### #&#8288;145 [deepchem](https://github.com/deepchem/deepchem) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: known (32) · Freshness: recent (70) · Maintenance: weak (14) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Aug 2026</sub>

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

<a name="imbalanced-learn"></a>
### #&#8288;146 [imbalanced-learn](https://github.com/scikit-learn-contrib/imbalanced-learn) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: known (32) · Freshness: active (83) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Jun 2026</sub>

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

<a name="paddlex"></a>
### #&#8288;147 [paddlex](https://github.com/paddlepaddle/paddlex) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (26) · Freshness: active (88) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Jun 2026</sub>

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

<a name="deeplearning4j"></a>
### #&#8288;148 [deeplearning4j](https://github.com/deeplearning4j/deeplearning4j) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: popular (64) · Freshness: slowing (38) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Feb 2026</sub>

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

<a name="paddleclas"></a>
### #&#8288;149 [paddleclas](https://github.com/paddlepaddle/paddleclas) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (21) · Freshness: recent (70) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Oct 2026</sub>

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

<a name="tiny-cuda-nn"></a>
### #&#8288;150 [tiny-cuda-nn](https://github.com/nvlabs/tiny-cuda-nn) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (12) · Freshness: recent (74) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · custom license · Sep 2026</sub>

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

<a name="weighted-boxes-fusion"></a>
### #&#8288;151 [weighted-boxes-fusion](https://github.com/zfturbo/weighted-boxes-fusion) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (6) · Freshness: recent (70) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Oct 2026</sub>

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

<a name="cleanrl"></a>
### #&#8288;152 [cleanrl](https://github.com/vwxyzjn/cleanrl) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: popular (55) · Freshness: slowing (41) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Apr 2026</sub>

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

<a name="face-alignment"></a>
### #&#8288;153 [face-alignment](https://github.com/1adrianb/face-alignment) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: known (36) · Freshness: recent (64) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · BSD-3-Clause · Apr 2026</sub>

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

<a name="argos-translate"></a>
### #&#8288;154 [argos-translate](https://github.com/argosopentech/argos-translate) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (29) · Freshness: recent (69) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · MIT · Aug 2026</sub>

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

<a name="mmf"></a>
### #&#8288;155 [mmf](https://github.com/facebookresearch/mmf) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: niche (18) · Freshness: recent (70) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · custom license · Oct 2026</sub>

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

<a name="mish"></a>
### #&#8288;156 [mish](https://github.com/digantamisra98/mish) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: niche (3) · Freshness: active (91) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Jul 2026</sub>

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

<a name="gensim"></a>
### #&#8288;157 [gensim](https://github.com/piskvorky/gensim) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: popular (70) · Freshness: quiet (12) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · LGPL-2.1 · Oct 2025</sub>

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

<a name="bertviz"></a>
### #&#8288;158 [bertviz](https://github.com/jessevig/bertviz) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: known (40) · Freshness: quiet (16) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · Apache-2.0 · Jan 2026</sub>

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

<a name="jenly1314-mlkit"></a>
### #&#8288;159 [mlkit](https://github.com/jenly1314/mlkit) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: niche (2) · Freshness: active (84) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Jun 2026</sub>

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

<a name="slowfast"></a>
### #&#8288;160 [slowfast](https://github.com/facebookresearch/slowfast) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: known (35) · Freshness: slowing (45) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Mar 2026</sub>

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

<a name="tensortrade"></a>
### #&#8288;161 [tensortrade](https://github.com/tensortrade-org/tensortrade) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: known (34) · Freshness: slowing (45) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Feb 2026</sub>

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

<a name="internnav"></a>
### #&#8288;162 [internnav](https://github.com/internrobotics/internnav) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: niche (2) · Freshness: recent (53) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Mar 2026</sub>

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

<a name="autokeras"></a>
### #&#8288;163 [autokeras](https://github.com/keras-team/autokeras) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: known (47) · Freshness: quiet (18) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · Nov 2025</sub>

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

<a name="torchquantum"></a>
### #&#8288;164 [torchquantum](https://github.com/mit-han-lab/torchquantum) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (5) · Freshness: recent (60) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Jul 2026</sub>

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
### #&#8288;165 [py-motmetrics](https://github.com/cheind/py-motmetrics) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (4) · Freshness: recent (63) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · MIT · Jul 2026</sub>

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

<a name="videopipe"></a>
### #&#8288;166 [videopipe](https://github.com/sherlockchou86/videopipe) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (10) · Freshness: quiet (27) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · Apache-2.0 · Feb 2026</sub>

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

<a name="deepo"></a>
### #&#8288;167 [deepo](https://github.com/ufoym/deepo) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (26) · Freshness: slowing (34) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Mar 2026</sub>

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

<a name="pinns"></a>
### #&#8288;168 [pinns](https://github.com/maziarraissi/pinns) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (25) · Freshness: slowing (33) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Feb 2026</sub>

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

<a name="transmogrifai"></a>
### #&#8288;169 [transmogrifai](https://github.com/salesforce/transmogrifai) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (8) · Freshness: recent (52) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · BSD-3-Clause · Jun 2026</sub>

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

<sub>no GPU · Needs Apache Spark 2.4, Scala 2.11, Java 1.8 · Models: Spark MLlib logistic regression, Spark MLlib random forest · [Repo](https://github.com/salesforce/transmogrifai) · [📖 Docs ↗](https://docs.transmogrif.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transmogrifai/)</sub>

<a name="raster-vision"></a>
### #&#8288;170 [raster-vision](https://github.com/azavea/raster-vision) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (7) · Freshness: recent (52) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Jun 2026</sub>

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

<a name="oc-sort"></a>
### #&#8288;171 [oc_sort](https://github.com/noahcao/oc_sort) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (1) · Freshness: recent (59) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Apr 2026</sub>

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

<a name="deim"></a>
### #&#8288;172 [deim](https://github.com/intellindust-ai-lab/deim) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (5) · Freshness: slowing (48) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · custom license · Mar 2026</sub>

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

<a name="paddleseg"></a>
### #&#8288;173 [paddleseg](https://github.com/paddlepaddle/paddleseg) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: known (47) · Freshness: quiet (3) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · Apache-2.0 · Nov 2025</sub>

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

<a name="lightautoml"></a>
### #&#8288;174 [lightautoml](https://github.com/sb-ai-lab/lightautoml) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: niche (3) · Freshness: quiet (22) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · Apache-2.0 · Dec 2025</sub>

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

<a name="aim"></a>
### #&#8288;175 [aim](https://github.com/aimhubio/aim) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: niche (27) · Freshness: quiet (13) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Dec 2025</sub>

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

<sub>no GPU · Docker · [Repo](https://github.com/aimhubio/aim) · [▶️ Demo ↗](https://play.aimstack.io/nmt/metrics) · [📖 Docs ↗](https://aimstack.readthedocs.io/en/latest/) · [🌐 Site ↗](https://aimstack.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aim/)</sub>

<a name="ltp"></a>
### #&#8288;176 [ltp](https://github.com/hit-scir/ltp) <sub>score [9](../README.md#-how-we-rank "Score 9/100. Adoption: niche (15) · Freshness: slowing (31) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 5.3k · no license · Mar 2026</sub>

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

<a name="jeelizfacefilter"></a>
### #&#8288;177 [jeelizfacefilter](https://github.com/jeeliz/jeelizfacefilter) <sub>score [3](../README.md#-how-we-rank "Score 3/100. Adoption: niche (9) · Freshness: quiet (1) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · Apache-2.0 · Nov 2025</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
