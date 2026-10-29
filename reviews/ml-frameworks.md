# 🔬 ML frameworks and libraries reviews · Best of Open-Source AI

The libraries models are built and run with: tensor frameworks, model zoos and the tooling around them. Back to the [leaderboard](../README.md#-ml-frameworks-and-libraries).

<sub>🌐 Also on the web: [ML frameworks and libraries on archestack.com](https://archestack.com/best-of-ai/ml-frameworks/), each project on its own page.</sub>

<a name="pytorch"></a>
### 🥇 [pytorch](https://github.com/pytorch/pytorch) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 105k · custom license · Oct 2026</sub>

**Python tensor library with GPU support and tape-based autograd for deep learning.**

PyTorch is a Python package that provides NumPy-like tensor computation on CPU or GPU, plus a reverse-mode autograd system for building neural networks imperatively. It ships torch.nn, torch.multiprocessing and a DataLoader, and can be extended in Python or C/C++. GPU backends covered in the README are NVIDIA CUDA, AMD ROCm (Linux only) and Intel GPU.

- **+** Dynamic graphs execute line by line, so debuggers and stack traces point at user code
- **+** Backends for NVIDIA CUDA, AMD ROCm and Intel GPU, plus CPU-only builds
- **+** Layers can be written in Python or via a C++ extension API
- **+** Pre-built pip/conda binaries, Docker images and Jetson wheels are available
- **−** Building from source needs a C++20 compiler, 10 GB disk and 30-60 minutes
- **−** ROCm support is Linux only; Windows distributed support is described as a prototype
- **−** Source build with CUDA requires matching cuDNN 9.0+, NVTX and compiler versions
- **−** Low-level framework only; no model serving or application layer included

<sub>GPU optional · Docker · Needs Python 3.10+, C++20 compiler (source builds), CUDA/cuDNN, ROCm or Intel GPU stack (optional), Intel MKL · Models: torch.nn modules, CUDA, ROCm, Intel XPU, CPU · [Repo](https://github.com/pytorch/pytorch) · [📖 Docs ↗](https://pytorch.org/docs/stable/) · [🌐 Site ↗](https://pytorch.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch/)</sub>

<a name="transformers"></a>
### 🥈 [transformers](https://github.com/huggingface/transformers) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 168k · Apache-2.0 · Oct 2026</sub>

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

<a name="ultralytics"></a>
### 🥉 [ultralytics](https://github.com/ultralytics/ultralytics) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 63k · AGPL-3.0 · Oct 2026</sub>

**Python library and CLI for training and running YOLO vision models.**

Ultralytics provides the YOLO model family (YOLOv3 through YOLO26) with a `yolo` CLI and Python API for training, validation, prediction, tracking and export. Tasks covered are detection, instance and semantic segmentation, depth estimation, classification, pose and oriented boxes. Pretrained weights download automatically on first use, and models export to formats such as ONNX.

- **+** One API and CLI covers train, val, predict, track and export across seven vision tasks
- **+** Pretrained YOLO26 n/s/m/l/x weights with published COCO mAP and CPU/T4 latency tables
- **+** Installs via pip, Conda or Docker; reproduction commands given for benchmark numbers
- **+** Active: release and commit within the last two days
- **−** AGPL-3.0; commercial use requires a separate Enterprise License
- **−** Vision only; no LLM or language model support
- **−** YOLO27 is listed as coming soon, with no models or launch date
- **−** RAM and VRAM requirements are not stated

<sub>GPU optional · Docker · Needs Python>=3.8, PyTorch>=1.8 · Models: YOLOv3 to YOLO26, PyTorch .pt, ONNX export, TensorRT export · [Repo](https://github.com/ultralytics/ultralytics) · [📖 Docs ↗](https://docs.ultralytics.com) · [🌐 Site ↗](https://www.ultralytics.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ultralytics/)</sub>

<a name="pytorch-image-models"></a>
### #&#8288;4 [pytorch-image-models](https://github.com/huggingface/pytorch-image-models) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

**PyTorch library of image models, pretrained weights and reference training scripts.**

timm is a Python library of image model architectures (ConvNeXt, EfficientNet, EVA, DINOv3, Swin and many more), most with pretrained weights, plus layers, optimizers, LR schedulers, data loaders and augmentations. It includes train.py, validate.py, inference.py and a sweep.py for hyperparameter search, aimed at reproducing ImageNet results. Recent work covers multi-label training, Muon-family optimizers and NaFlexViT variable-resolution models.

- **+** Very wide architecture coverage; every family has variants with pretrained weights
- **+** Reference train, validate, inference and sweep scripts with YAML config and resume support
- **+** Large optimizer and scheduler set, including Muon, LAMB, Kron and WSD
- **+** Active: release 1.0.30 on 2026-09-22, commits through October 2026
- **−** Some model variants ship without pretrained weights
- **−** Vision backbones only; no serving layer or UI
- **−** Frequent behaviour changes: RoPE precision fixes alter low-precision model outputs
- **−** Maintainer left Hugging Face; maintenance releases continue but project direction is less clear

<sub>GPU optional · Needs PyTorch · Models: PyTorch checkpoints, Hugging Face Hub weights, ONNX export · [Repo](https://github.com/huggingface/pytorch-image-models) · [📖 Docs ↗](https://huggingface.co/docs/timm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-image-models/)</sub>

<a name="supervision"></a>
### #&#8288;5 [supervision](https://github.com/roboflow/supervision) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · MIT · Oct 2026</sub>

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
### #&#8288;6 [diffusers](https://github.com/huggingface/diffusers) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;7 [genesis-world](https://github.com/genesis-embodied-ai/genesis-world) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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

<a name="ray"></a>
### #&#8288;8 [ray](https://github.com/ray-project/ray) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · Apache-2.0 · Oct 2026</sub>

**Distributed Python runtime with libraries for data, training, tuning, RL and serving.**

Ray is a distributed runtime for scaling Python code from a laptop to a cluster, built around tasks, actors and shared objects. On top of the core it ships libraries for datasets (Data), distributed training (Train), hyperparameter tuning (Tune), reinforcement learning (RLlib) and model serving (Serve). It includes a dashboard and a distributed debugger, and runs on local machines, clusters, cloud providers and Kubernetes.

- **+** Same Python code scales from one machine to a cluster without extra infrastructure
- **+** One runtime covers data processing, training, tuning, RL and serving
- **+** Runs on bare clusters, cloud providers and Kubernetes
- **+** Ships a dashboard and a distributed debugger for cluster apps
- **−** Python-centric; README describes scaling Python applications only
- **−** Broad scope with many libraries means a large surface to learn
- **−** README gives no hardware requirements or cluster sizing guidance
- **−** Anyscale managed offering is promoted; OSS versus hosted feature split is unclear

<sub>GPU optional · Docker · [Repo](https://github.com/ray-project/ray) · [📖 Docs ↗](https://docs.ray.io/en/latest/index.html) · [🌐 Site ↗](https://www.ray.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ray/)</sub>

<a name="mediapipe"></a>
### #&#8288;9 [mediapipe](https://github.com/google-ai-edge/mediapipe) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

**On-device ML task APIs and a C++ pipeline framework for mobile, web and desktop.**

MediaPipe provides prebuilt Tasks APIs with pre-trained models for vision, audio, text, retrieval and LLM inference, targeting Android, iOS, web and Python. Underneath is MediaPipe Framework, a C++ graph system built from packets, graphs and calculators for custom perception pipelines. Input data is processed on device, though the Tasks APIs send performance and usage metrics to Google.

- **+** Prebuilt Tasks for vision, audio, text, retrieval and LLM inference, with ready-to-run models
- **+** Targets Android, iOS, web, Python and C++ from one project
- **+** Input data stays on device; no images, video or text sent to Google servers
- **+** MediaPipe Studio lets you test and benchmark solutions in the browser
- **−** Tasks APIs send performance and usage metrics to Google; app developers must obtain user consent
- **−** Framework layer requires learning packets, graphs and calculators, and a C++ build setup
- **−** README is a pointer page; real documentation lives on developers.google.com
- **−** Resource requirements and supported model formats are not stated in the README

<sub>GPU optional · Docker · Models: MediaPipe pre-trained models, LLM inference (genai) · [Repo](https://github.com/google-ai-edge/mediapipe) · [▶️ Demo ↗](https://google-ai-edge.github.io/mediapipe-samples-web/#/home) · [📖 Docs ↗](https://developers.google.com/edge/mediapipe/solutions) · [🌐 Site ↗](https://developers.google.com/edge/mediapipe) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mediapipe/)</sub>

<a name="mlx"></a>
### #&#8288;10 [mlx](https://github.com/ml-explore/mlx) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Oct 2026</sub>

**NumPy-style array framework for machine learning on Apple silicon.**

MLX is an array framework from Apple machine learning research with Python, C++, C and Swift APIs. It builds lazy, dynamic computation graphs, offers composable transforms for autodiff and vectorization, and includes PyTorch-like mlx.nn and mlx.optimizers packages. Arrays live in unified memory, so CPU and GPU ops share data without copies. Linux CUDA and CPU-only packages exist.

- **+** Python API follows NumPy; mlx.nn and mlx.optimizers follow PyTorch
- **+** Unified memory: CPU and GPU ops share arrays without transfers
- **+** Composable transforms for autodiff, vectorization and graph optimization
- **+** Python, C++, C and Swift APIs; installs via pip on macOS and Linux
- **−** Designed for Apple silicon; Linux CUDA and CPU backends are add-on installs
- **−** Example models live in a separate mlx-examples repo
- **−** Supported devices are only CPU and GPU per the README
- **−** Model zoo and ecosystem size compared to PyTorch not stated in README

<sub>GPU optional · Models: LLaMA, Stable Diffusion, Whisper, LoRA fine-tuning · [Repo](https://github.com/ml-explore/mlx) · [📖 Docs ↗](https://ml-explore.github.io/mlx/build/html/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlx/)</sub>

<a name="onnx"></a>
### #&#8288;11 [onnx](https://github.com/onnx/onnx) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Oct 2026</sub>

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

<a name="lerobot"></a>
### #&#8288;12 [lerobot](https://github.com/huggingface/lerobot) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

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

<sub>Docker · Needs PyTorch, Hugging Face Hub · Models: ACT, Diffusion, VQ-BeT, HIL-SERL, TDMPC · [Repo](https://github.com/huggingface/lerobot) · [▶️ Demo ↗](https://huggingface.co/spaces/lerobot/robot-folding) · [📖 Docs ↗](https://huggingface.co/docs/lerobot/index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lerobot/)</sub>

<a name="flash-attention"></a>
### #&#8288;13 [flash-attention](https://github.com/dao-ailab/flash-attention) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · BSD-3-Clause · Oct 2026</sub>

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
### #&#8288;14 [deepface](https://github.com/serengil/deepface) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Oct 2026</sub>

**Python library for face verification, search and attribute analysis.**

DeepFace wraps face recognition models (VGG-Face, FaceNet, ArcFace, Dlib, SFace, GhostFaceNet, Buffalo_L) and about 20 detector backends behind single calls such as verify, find, analyze and represent. It also covers age, gender, emotion and race prediction, anti-spoofing, webcam streaming, and registering embeddings in databases such as Postgres, Mongo, Pinecone or Milvus. A gunicorn-based REST API ships in the repo.

- **+** One-line calls cover detect, align, represent and verify; model and detector swap by argument
- **+** Database-backed register, identify and search with ANN support across many vector and SQL stores
- **+** Runs on onnxruntime by default; TensorFlow or PyTorch available as install extras
- **+** Anti-spoofing, webcam streaming and a REST API are included in the same repo
- **−** Built-in race and ethnicity prediction carries bias and misuse concerns
- **−** Defaults are VGG-Face and the OpenCV detector, which the README does not rank as most accurate
- **−** Browser UI is a separate repository (deepface-react-ui)
- **−** RAM and GPU requirements are not stated in the README

<sub>GPU optional · Docker + Compose · Needs onnxruntime, TensorFlow (optional), PyTorch (optional), Postgres, Mongo or other vector DB (optional) · Models: VGG-Face, Facenet, Facenet512, OpenFace, DeepFace · [Repo](https://github.com/serengil/deepface) · [🌐 Site ↗](https://deepface.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepface/)</sub>

<a name="burn"></a>
### #&#8288;15 [burn](https://github.com/tracel-ai/burn) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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

<a name="scikit-learn"></a>
### #&#8288;16 [scikit-learn](https://github.com/scikit-learn/scikit-learn) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · BSD-3-Clause · Oct 2026</sub>

**Python library of classical machine learning algorithms built on NumPy and SciPy.**

scikit-learn is a Python module for machine learning built on SciPy, started in 2007 as a Google Summer of Code project. It installs with pip or conda and requires Python 3.12 or newer, NumPy, SciPy, Narwhals, joblib and threadpoolctl. Plotting helpers need Matplotlib. The README does not list the algorithms; those are documented on the website.

- **+** Installs with one pip or conda command; six required dependencies, all listed with minimum versions
- **+** BSD-3-Clause license; test suite runs with pytest sklearn
- **+** Volunteer community with institutional support; benchmarked with asv
- **+** Test randomness is controllable through the SKLEARN_SEED environment variable
- **−** README does not mention GPU support
- **−** Requires Python 3.12 or newer, which excludes older environments
- **−** Plotting needs Matplotlib, installed separately
- **−** README gives no algorithm list; readers must consult the website

<sub>Needs Python >= 3.12, NumPy >= 1.26.0, SciPy >= 1.11.4, Narwhals >= 2.0.1, joblib >= 1.4.0, threadpoolctl >= 3.5.0 · [Repo](https://github.com/scikit-learn/scikit-learn) · [📖 Docs ↗](https://scikit-learn.org/stable/) · [🌐 Site ↗](https://scikit-learn.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scikit-learn/)</sub>

<a name="jax"></a>
### #&#8288;17 [jax](https://github.com/jax-ml/jax) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

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

<a name="tensorflow"></a>
### #&#8288;18 [tensorflow](https://github.com/tensorflow/tensorflow) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (100) · Freshness: active (95) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 201k · Apache-2.0 · Oct 2026</sub>

**Tensor and neural network framework with Python and C++ APIs.**

TensorFlow is a machine learning framework for building, training and deploying models, with stable Python and C++ APIs and non-guaranteed APIs for other languages. It installs via pip, with CUDA GPU support on Ubuntu and Windows and a smaller CPU-only package. Related tooling includes TensorBoard and LiteRT for Android.

- **+** Stable Python and C++ APIs
- **+** CUDA GPU support via pip on Ubuntu and Windows; separate tensorflow-cpu package
- **+** Device plugins for DirectX and macOS Metal
- **+** Surrounding tooling: TensorBoard, LiteRT for Android, official models and tutorials
- **−** APIs for languages other than Python and C++ have no backward compatibility guarantee
- **−** Built-in GPU support is CUDA only; other devices need separate plugins
- **−** Linux XLA build artifacts listed as TBA
- **−** RAM and VRAM requirements not stated in the README

<sub>GPU optional · Needs Python, CUDA (for GPU) · Models: LiteRT (Android) · [Repo](https://github.com/tensorflow/tensorflow) · [📖 Docs ↗](https://www.tensorflow.org/api_docs/) · [🌐 Site ↗](https://www.tensorflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorflow/)</sub>

<a name="tinygrad"></a>
### #&#8288;19 [tinygrad](https://github.com/tinygrad/tinygrad) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Oct 2026</sub>

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
### #&#8288;20 [onnxruntime](https://github.com/microsoft/onnxruntime) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Oct 2026</sub>

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

<a name="xgboost"></a>
### #&#8288;21 [xgboost](https://github.com/dmlc/xgboost) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

**Gradient boosted decision tree library for tabular machine learning.**

XGBoost implements parallel tree boosting (GBDT/GBM) under the gradient boosting framework. Per the README, the same code runs on Kubernetes, Hadoop, SGE, Dask, Spark and PySpark, and scales to billions of examples. It is distributed through PyPI, CRAN and conda-forge.

- **+** Same code runs on Kubernetes, Hadoop, SGE, Dask, Spark and PySpark
- **+** Packaged on PyPI, CRAN and conda-forge
- **+** Backed by a KDD 2016 paper; Apache-2.0 licensed
- **+** Active: release on 2026-09-15 and recent commits
- **−** Tree boosting only; not a general deep learning framework
- **−** README does not state GPU support, RAM needs or language bindings
- **−** README has no install or quick-start example; relies on external docs
- **−** Aimed at tabular data; no LLM or generative model support

<sub>Models: gradient boosted decision trees · [Repo](https://github.com/dmlc/xgboost) · [📖 Docs ↗](https://xgboost.readthedocs.io) · [🌐 Site ↗](https://xgboost.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xgboost/)</sub>

<a name="triton"></a>
### #&#8288;22 [triton](https://github.com/triton-lang/triton) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Oct 2026</sub>

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

<a name="transformers-js"></a>
### #&#8288;23 [transformers.js](https://github.com/huggingface/transformers.js) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;24 [shap](https://github.com/shap/shap) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

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
### #&#8288;25 [sentence-transformers](https://github.com/huggingface/sentence-transformers) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Oct 2026</sub>

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

<a name="spacy"></a>
### #&#8288;26 [spacy](https://github.com/explosion/spacy) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Oct 2026</sub>

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
### #&#8288;27 [fastai](https://github.com/fastai/fastai) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · Apache-2.0 · Sep 2026</sub>

**High-level deep learning library on PyTorch for vision, text, tabular and recommenders.**

fastai is a Python deep learning library built on PyTorch. It offers high-level APIs that train image classifiers, segmentation, text sentiment, tabular and recommendation models in about 5 lines, on top of layered lower-level components for researchers. Core pieces include a data block API, a two-way callback system and an optimizer refactored into small composable parts.

- **+** Layered API: 5-line high-level training down to low-level building blocks
- **+** Two-way callbacks can modify data, model or optimizer at any point in training
- **+** Docs are runnable notebooks, with a free course and a book
- **+** Migration guides for plain PyTorch, Ignite, Lightning and Catalyst
- **−** Jupyter on Windows forces num_workers to 0, making vision training much slower
- **−** Covers classic deep learning domains; README does not mention LLM or diffusion workflows
- **−** README advises installing PyTorch separately before fastai
- **−** GPU memory and RAM requirements are not stated

<sub>GPU optional · Compose · Needs PyTorch, fastcore · Models: PyTorch · [Repo](https://github.com/fastai/fastai) · [📖 Docs ↗](https://docs.fast.ai) · [🌐 Site ↗](https://docs.fast.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fastai/)</sub>

<a name="kornia"></a>
### #&#8288;28 [kornia](https://github.com/kornia/kornia) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

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

<a name="paddle"></a>
### #&#8288;29 [paddle](https://github.com/paddlepaddle/paddle) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Oct 2026</sub>

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

<a name="models"></a>
### #&#8288;30 [models](https://github.com/tensorflow/models) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (96) · Freshness: active (93) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · custom license · Oct 2026</sub>

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

<a name="keras"></a>
### #&#8288;31 [keras](https://github.com/keras-team/keras) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Oct 2026</sub>

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

<a name="optuna"></a>
### #&#8288;32 [optuna](https://github.com/optuna/optuna) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

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

<a name="fiftyone"></a>
### #&#8288;33 [fiftyone](https://github.com/voxel51/fiftyone) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (45) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**Dataset visualization, curation and model evaluation tool for computer vision.**

FiftyOne is a Python library with a browser-based App for exploring image, video and 3D datasets together with their labels. It supports 2D and 3D annotation, an embeddings panel, model evaluation to find failure modes, and a Brain module for finding data and annotation issues. It integrates with PyTorch, Hugging Face and Ultralytics, and can be extended with plugins.

- **+** Installs with pip install fiftyone; supports Python 3.10 to 3.13
- **+** Built-in dataset zoo and model zoo for quick starts
- **+** Embeddings panel and evaluation tools to locate failure modes and label errors
- **+** Plugin system to extend the App and workflows
- **−** Team collaboration and cloud-native workloads are in the separate commercial Voxel51 product
- **−** Focused on computer vision; not aimed at text or LLM workflows
- **−** Video datasets need FFmpeg installed separately
- **−** RAM and GPU requirements are not stated in the README

<sub>GPU optional · Docker · Needs Python 3.10-3.13, MongoDB (fiftyone-db package; self-managed instance optional), FFmpeg (for video), Node.js and Yarn (source install only) · Models: PyTorch, Hugging Face, Ultralytics · [Repo](https://github.com/voxel51/fiftyone) · [▶️ Demo ↗](https://colab.research.google.com/github/voxel51/fiftyone-examples/blob/master/examples/quickstart.ipynb) · [📖 Docs ↗](https://docs.voxel51.com) · [🌐 Site ↗](https://voxel51.com/fiftyone) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fiftyone/)</sub>

<a name="isaaclab"></a>
### #&#8288;34 [isaaclab](https://github.com/isaac-sim/isaaclab) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · BSD-3-Clause · Oct 2026</sub>

**Robot learning framework for RL and imitation learning in GPU simulation.**

Isaac Lab is a Python framework for robotics research that runs reinforcement learning, imitation learning and post-training in GPU-accelerated simulation. It supports Newton, OVRTX, OVPhysX and NVIDIA Isaac Sim as physics and rendering backends, and ships more than 16 robot models and more than 30 environments. Environments train with RSL RL, SKRL, RL Games or Stable Baselines, plus multi-agent RL.

- **+** More than 30 ready-to-train environments and 16+ robot models, from manipulators to humanoids
- **+** Works with RSL RL, SKRL, RL Games and Stable Baselines, and supports multi-agent RL
- **+** Sensor simulation covers RTX cameras, LIDAR, IMU, contact sensors and ray casters
- **+** Multiple backends; kit-less Newton workflows do not need Isaac Sim
- **−** Isaac Sim workflows need a matching Isaac Sim version (6.2 for main) and carry proprietary license terms
- **−** The isaaclab_mimic extension is Apache 2.0 and requires cuRobo, which is proprietary
- **−** Not a general ML library; scope is limited to robotics simulation and learning
- **−** Hardware requirements such as RAM and VRAM are not stated in the README

<sub>GPU required · Docker + Compose · Needs NVIDIA Isaac Sim 6.2 (for Isaac Sim workflows), Newton, OVRTX, OVPhysX, cuRobo (isaaclab_mimic) · Models: RSL RL, SKRL, RL Games, Stable Baselines · [Repo](https://github.com/isaac-sim/isaaclab) · [📖 Docs ↗](https://isaac-sim.github.io/IsaacLab/main/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/isaaclab/)</sub>

<a name="mnn"></a>
### #&#8288;35 [mnn](https://github.com/alibaba/mnn) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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

<a name="tvm"></a>
### #&#8288;36 [tvm](https://github.com/apache/tvm) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

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

<a name="pytorch-lightning"></a>
### #&#8288;37 [pytorch-lightning](https://github.com/lightning-ai/pytorch-lightning) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · Apache-2.0 · Sep 2026</sub>

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
### #&#8288;38 [ncnn](https://github.com/tencent/ncnn) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Oct 2026</sub>

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

<a name="vision"></a>
### #&#8288;39 [vision](https://github.com/pytorch/vision) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · BSD-3-Clause · Oct 2026</sub>

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

<a name="ggml"></a>
### #&#8288;40 [ggml](https://github.com/ggml-org/ggml) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Oct 2026</sub>

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

<a name="metaflow"></a>
### #&#8288;41 [metaflow](https://github.com/netflix/metaflow) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (40) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Oct 2026</sub>

**Python framework for building, scaling and deploying ML and AI workflows.**

Metaflow is a Python library for writing ML and AI pipelines as flows of steps, which run locally or in a notebook and then scale out to cloud compute on CPUs and GPUs. It tracks experiments, versions artifacts, manages dependencies, and deploys flows to production orchestrators with event-based triggering. Originally built at Netflix, now supported by Outerbounds.

- **+** Same flow code runs on a laptop, in a notebook, on cloud compute and in production
- **+** Built-in experiment tracking, artifact versioning and a client API for inspecting past runs
- **+** Supports foreach parallelism and gang-scheduled distributed jobs on CPUs and GPUs
- **+** Apache-2.0, installable from PyPI or conda-forge
- **−** Cloud scaling and production orchestration need separate infrastructure setup beyond pip install
- **−** README does not list which cloud providers or orchestrators are supported
- **−** Not LLM-specific; README describes no model serving or agent features
- **−** No Docker or compose setup in the repository

<sub>GPU optional · Needs Python, Cloud compute cluster (for scaling), Production workflow orchestrator (for deployment) · [Repo](https://github.com/netflix/metaflow) · [▶️ Demo ↗](https://outerbounds.com/sandbox) · [📖 Docs ↗](https://docs.metaflow.org) · [🌐 Site ↗](https://metaflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/metaflow/)</sub>

<a name="tabpfn"></a>
### #&#8288;42 [tabpfn](https://github.com/priorlabs/tabpfn) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · Apache-2.0 · Oct 2026</sub>

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

<a name="tokenizers"></a>
### #&#8288;43 [tokenizers](https://github.com/huggingface/tokenizers) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

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

<a name="darts"></a>
### #&#8288;44 [darts](https://github.com/unit8co/darts) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

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

<a name="flashinfer"></a>
### #&#8288;45 [flashinfer](https://github.com/flashinfer-ai/flashinfer) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.8k · Apache-2.0 · Oct 2026</sub>

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

<a name="datasets"></a>
### #&#8288;46 [datasets](https://github.com/huggingface/datasets) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Oct 2026</sub>

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

<a name="autogluon"></a>
### #&#8288;47 [autogluon](https://github.com/autogluon/autogluon) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**AutoML library for tabular, time series and multimodal data in Python.**

AutoGluon trains and ensembles models for tabular, time series and multimodal prediction through predictor classes such as TabularPredictor, TimeSeriesPredictor and MultiModalPredictor. It selects and combines models, from classic ML algorithms to foundation models, so a working pipeline takes a few lines of Python. It installs with pip on Python 3.10 to 3.13 across Linux, macOS and Windows.

- **+** Three task APIs (tabular, time series, multimodal) share a fit/predict pattern
- **+** Combines classic ML models and foundation models in one ensemble
- **+** Installs with pip or conda on Linux, macOS and Windows
- **+** Cloud options: AutoGluon Cloud, official Docker image, AWS Deep Learning Containers
- **−** README gives no RAM, VRAM or training-time figures
- **−** README does not say how much GPU helps or which tasks need it
- **−** Not an LLM app; no chat UI, model server or agent runtime
- **−** Supports Python 3.10 to 3.13 only

<sub>GPU optional · Models: tabular models, time series forecasting, multimodal models · [Repo](https://github.com/autogluon/autogluon) · [📖 Docs ↗](https://auto.gluon.ai/stable/index.html) · [🌐 Site ↗](https://auto.gluon.ai/stable/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autogluon/)</sub>

<a name="vowpal-wabbit"></a>
### #&#8288;48 [vowpal_wabbit](https://github.com/vowpalwabbit/vowpal_wabbit) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · custom license · Sep 2026</sub>

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

<a name="feast"></a>
### #&#8288;49 [feast](https://github.com/feast-dev/feast) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Oct 2026</sub>

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

<a name="sentencepiece"></a>
### #&#8288;50 [sentencepiece](https://github.com/google/sentencepiece) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (48) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Oct 2026</sub>

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

<a name="wandb"></a>
### #&#8288;51 [wandb](https://github.com/wandb/wandb) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (46) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

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
### #&#8288;52 [cutlass](https://github.com/nvidia/cutlass) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Oct 2026</sub>

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

<a name="gymnasium"></a>
### #&#8288;53 [gymnasium](https://github.com/farama-foundation/gymnasium) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (50) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Oct 2026</sub>

**Python API and environment set for reinforcement learning research.**

Gymnasium is a Python library that defines a standard environment API (make, reset, step, action and observation spaces) for connecting reinforcement learning algorithms to environments. It ships Classic Control, Box2D, Toy Text, MuJoCo and Atari families. It is the maintained fork of OpenAI's Gym, run by the Farama Foundation.

- **+** Small, uniform env API with terminated and truncated flags
- **+** Environment families install separately via extras like gymnasium[atari] or gymnasium[all]
- **+** Strict -vN environment versioning to keep learning results reproducible
- **+** Third-party environments and libraries (CleanRL, PettingZoo) use the same API
- **−** Provides environments and an interface only; no RL algorithms included
- **−** Older Gym-based third-party environments may need apply_env_compatibility
- **−** Some environment families are hard to install on certain systems
- **−** Hardware and RAM requirements are not stated in the README

<sub>Needs Python · [Repo](https://github.com/farama-foundation/gymnasium) · [📖 Docs ↗](https://gymnasium.farama.org) · [🌐 Site ↗](https://gymnasium.farama.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gymnasium/)</sub>

<a name="pytorch-geometric"></a>
### #&#8288;54 [pytorch_geometric](https://github.com/pyg-team/pytorch_geometric) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Oct 2026</sub>

**Graph neural network library built on PyTorch.**

PyG (PyTorch Geometric) is a Python library for writing and training graph neural networks on PyTorch. It provides a MessagePassing interface for custom layers, a large set of published GNN layers and models, mini-batch loaders and samplers for many small graphs or one large graph, and benchmark datasets. It also covers heterogeneous graphs, 3D meshes and point clouds, multi-GPU training and torch.compile.

- **+** Unified MessagePassing API keeps custom GNN layers short, as the EdgeConv example shows
- **+** Large catalog of published GNN layers, each linked to its paper and often an example script
- **+** Covers heterogeneous graphs, dynamic graphs, and sampling for graphs with millions of nodes
- **+** Supports torch.compile, TorchScript, multi-GPU examples and optional pyg-lib sparse kernels
- **−** Requires PyTorch; install steps and version matching are not in the visible README
- **−** Focused on graph learning only, not a general ML or LLM toolkit
- **−** Memory and GPU requirements are not stated in the README
- **−** Some acceleration comes from separate packages such as pyg-lib

<sub>GPU optional · Docker · Needs PyTorch, pyg-lib (optional) · Models: GCN, GAT, GraphSAGE, GIN, RGCN · [Repo](https://github.com/pyg-team/pytorch_geometric) · [📖 Docs ↗](https://pytorch-geometric.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pytorch-geometric/)</sub>

<a name="lightgbm"></a>
### #&#8288;55 [lightgbm](https://github.com/lightgbm-org/lightgbm) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

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

<a name="dlib"></a>
### #&#8288;56 [dlib](https://github.com/davisking/dlib) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (55) · Freshness: active (97) · Maintenance: fair (53) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · BSL-1.0 · Oct 2026</sub>

**C++ machine learning toolkit with Python bindings.**

Dlib is a C++17 library of machine learning algorithms and general-purpose tools for building software in C++. It is built with CMake, can be installed through vcpkg, and has a Python API available with pip install dlib. The README points to dlib.net for the API reference and does not list individual algorithms or models.

- **+** Boost Software License permits use in closed-source commercial software
- **+** Installs via CMake, vcpkg, or pip for the Python API
- **+** Ships a unit test suite (dtest) and many example programs
- **+** Optional AVX build flag speeds up some operations
- **−** Requires a C++17 compiler and CMake to build from source
- **−** README does not list algorithms, models, or GPU support
- **−** pip install from source needs a local compiler toolchain
- **−** Not a server or UI; used only as a library

<sub>Needs C++17 compiler, CMake · [Repo](https://github.com/davisking/dlib) · [📖 Docs ↗](http://dlib.net/compile.html) · [🌐 Site ↗](http://dlib.net) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dlib/)</sub>

<a name="pyod"></a>
### #&#8288;57 [pyod](https://github.com/yzhao062/pyod) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · BSD-2-Clause · Oct 2026</sub>

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

<a name="modelscope"></a>
### #&#8288;58 [modelscope](https://github.com/modelscope/modelscope) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Oct 2026</sub>

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

<a name="candle"></a>
### #&#8288;59 [candle](https://github.com/huggingface/candle) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Oct 2026</sub>

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

<a name="smile"></a>
### #&#8288;60 [smile](https://github.com/haifengl/smile) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · custom license · Oct 2026</sub>

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

<a name="hanlp"></a>
### #&#8288;61 [hanlp](https://github.com/hankcs/hanlp) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: widely used (86) · Freshness: recent (70) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Sep 2026</sub>

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
### #&#8288;62 [finrl](https://github.com/ai4finance-foundation/finrl) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (62) · Freshness: active (96) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Oct 2026</sub>

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

<a name="lm-evaluation-harness"></a>
### #&#8288;63 [lm-evaluation-harness](https://github.com/eleutherai/lm-evaluation-harness) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Sep 2026</sub>

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

<a name="river"></a>
### #&#8288;64 [river](https://github.com/online-ml/river) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · BSD-3-Clause · Oct 2026</sub>

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

<a name="accelerate"></a>
### #&#8288;65 [accelerate](https://github.com/huggingface/accelerate) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · Apache-2.0 · Oct 2026</sub>

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

<a name="bitsandbytes"></a>
### #&#8288;66 [bitsandbytes](https://github.com/bitsandbytes-foundation/bitsandbytes) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · MIT · Oct 2026</sub>

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

<a name="clearml"></a>
### #&#8288;67 [clearml](https://github.com/clearml/clearml) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Oct 2026</sub>

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

<a name="dali"></a>
### #&#8288;68 [dali](https://github.com/nvidia/dali) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Oct 2026</sub>

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

<a name="vit-pytorch"></a>
### #&#8288;69 [vit-pytorch](https://github.com/lucidrains/vit-pytorch) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (76) · Freshness: active (93) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

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

<a name="stable-baselines3"></a>
### #&#8288;70 [stable-baselines3](https://github.com/dlr-rm/stable-baselines3) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

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

<a name="sktime"></a>
### #&#8288;71 [sktime](https://github.com/sktime/sktime) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · BSD-3-Clause · Oct 2026</sub>

**Python library with one scikit-learn-style API for time series tasks.**

sktime provides a unified fit/predict interface for forecasting, time series classification, regression, clustering, and anomaly and changepoint detection. It includes native algorithms and interfaces to statsmodels, tsfresh, PyOD, and Prophet. Pipelining, ensembling, tuning, and reduction let an algorithm built for one task be applied to another.

- **+** Covers forecasting, classification, regression, clustering, and detection under one API
- **+** Composition tools: pipelines, ensembles, tuning, and reduction to scikit-learn regressors
- **+** Interfaces to statsmodels, tsfresh, PyOD, and Prophet behind the same API
- **+** Extension templates for custom estimators; installs via pip or conda-forge
- **−** Detection, clustering, and distances modules are maturing; alignment is experimental
- **−** Task extras install only a curated subset of soft dependencies
- **−** conda offers only base or all-extras, no flexible dependency sets
- **−** README does not state GPU or memory requirements

<sub>Needs scikit-learn, statsmodels, tsfresh, PyOD, fbprophet · Models: scikit-learn estimators, ThetaForecaster, TimeSeriesForestClassifier · [Repo](https://github.com/sktime/sktime) · [▶️ Demo ↗](https://mybinder.org/v2/gh/sktime/sktime/main?filepath=examples) · [📖 Docs ↗](https://www.sktime.net/en/stable/users.html) · [🌐 Site ↗](https://www.sktime.net) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sktime/)</sub>

<a name="flax"></a>
### #&#8288;72 [flax](https://github.com/google/flax) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;73 [flower](https://github.com/flwrlabs/flower) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;74 [anomalib](https://github.com/open-edge-platform/anomalib) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Oct 2026</sub>

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

<a name="monai"></a>
### #&#8288;75 [monai](https://github.com/project-monai/monai) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.8k · Apache-2.0 · Oct 2026</sub>

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

<a name="opencompass"></a>
### #&#8288;76 [opencompass](https://github.com/open-compass/opencompass) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Oct 2026</sub>

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

<a name="pytorch-grad-cam"></a>
### #&#8288;77 [pytorch-grad-cam](https://github.com/jacobgil/pytorch-grad-cam) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Aug 2026</sub>

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

<a name="detectron2"></a>
### #&#8288;78 [detectron2](https://github.com/facebookresearch/detectron2) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: widely used (85) · Freshness: recent (70) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Oct 2026</sub>

**PyTorch library for object detection and segmentation research.**

Detectron2 is Facebook AI Research's PyTorch library for object detection and segmentation, successor to Detectron and maskrcnn-benchmark. It covers panoptic segmentation, DensePose, Cascade R-CNN, rotated boxes, PointRend, DeepLab, ViTDet and MViTv2, and ships a Model Zoo of baselines. Models can be exported to TorchScript or Caffe2.

- **+** Wide algorithm coverage: panoptic segmentation, DensePose, PointRend, ViTDet, MViTv2, rotated boxes
- **+** Model Zoo with downloadable baselines and trained weights
- **+** Export to TorchScript or Caffe2 for deployment
- **+** Modular design for building research projects on top; Apache-2.0
- **−** Last tagged release is 2021-11-15, though commits continue
- **−** Not a model server; no inference API or UI included
- **−** Install steps live in external docs, not the README
- **−** Hardware requirements are not stated in the README

<sub>Docker + Compose · Needs PyTorch · Models: Mask R-CNN, Cascade R-CNN, Panoptic segmentation, DensePose, PointRend · [Repo](https://github.com/facebookresearch/detectron2) · [▶️ Demo ↗](https://colab.research.google.com/drive/16jcaJoc6bCFAQ96jDe2HwtXj7BMD_-m5) · [📖 Docs ↗](https://detectron2.readthedocs.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/detectron2/)</sub>

<a name="recommenders"></a>
### #&#8288;79 [recommenders](https://github.com/recommenders-team/recommenders) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (70) · Freshness: recent (70) · Maintenance: fair (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Oct 2026</sub>

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

<a name="carla"></a>
### #&#8288;80 [carla](https://github.com/carla-simulator/carla) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (56) · Freshness: active (81) · Maintenance: patchy (43) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

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

<a name="corenlp"></a>
### #&#8288;81 [corenlp](https://github.com/stanfordnlp/corenlp) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (39) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · GPL-3.0 · Sep 2026</sub>

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

<a name="flash-linear-attention"></a>
### #&#8288;82 [flash-linear-attention](https://github.com/fla-org/flash-linear-attention) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Oct 2026</sub>

**Triton kernels and PyTorch layers for linear attention and hybrid sequence models.**

Library of Triton kernels, `fla.layers` token-mixing modules and model implementations for linear attention, sparse attention, state space models and hybrids. It covers RetNet, GLA, DeltaNet, Gated DeltaNet, KDA, RWKV7, Mamba2/3, NSA and MoBA, and the layers can replace standard multihead attention. The README states the implementations are verified on NVIDIA, AMD and Intel hardware.

- **+** Covers about 40 architectures, from RetNet and GLA to Mamba3, KDA and Gated DeltaNet
- **+** Layers can replace standard attention in an existing model, with hybrid model support
- **+** Backend extras for CUDA, ROCm, XPU, NPU and CPU installs
- **+** Variable-length kernels, fused linear cross-entropy, context parallel for KDA and GDN
- **−** Bare pip install does not pull torch or triton; a backend extra is required
- **−** Full training loop lives in a separate repo (flame), not here
- **−** Input layout changed from head-first to seq-first in 2024, which can break older code
- **−** RAM and VRAM requirements are not stated in the README excerpt

<sub>GPU optional · Needs PyTorch, Triton · Models: RetNet, GLA, DeltaNet, Gated DeltaNet, KDA · [Repo](https://github.com/fla-org/flash-linear-attention) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flash-linear-attention/)</sub>

<a name="skorch"></a>
### #&#8288;83 [skorch](https://github.com/skorch-dev/skorch) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · BSD-3-Clause · Oct 2026</sub>

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

<a name="stanza"></a>
### #&#8288;84 [stanza](https://github.com/stanfordnlp/stanza) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · custom license · Oct 2026</sub>

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
### #&#8288;85 [h2o-3](https://github.com/h2oai/h2o-3) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Sep 2026</sub>

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
### #&#8288;86 [causalml](https://github.com/uber/causalml) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · custom license · Oct 2026</sub>

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

<a name="xformers"></a>
### #&#8288;87 [xformers](https://github.com/facebookresearch/xformers) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (41) · Freshness: active (94) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Oct 2026</sub>

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

<a name="umap"></a>
### #&#8288;88 [umap](https://github.com/lmcinnes/umap) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (25) · Freshness: active (98) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · BSD-3-Clause · Oct 2026</sub>

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

<a name="interpret"></a>
### #&#8288;89 [interpret](https://github.com/interpretml/interpret) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (14) · Freshness: active (96) · Maintenance: fair (61) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · MIT · Oct 2026</sub>

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

<a name="deeplabcut"></a>
### #&#8288;90 [deeplabcut](https://github.com/deeplabcut/deeplabcut) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · LGPL-3.0 · Sep 2026</sub>

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
### #&#8288;91 [dvc](https://github.com/treeverse/dvc) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (59) · Freshness: active (97) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Aug 2026</sub>

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

<a name="pytorch3d"></a>
### #&#8288;92 [pytorch3d](https://github.com/facebookresearch/pytorch3d) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (37) · Freshness: active (87) · Maintenance: patchy (49) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10.0k · custom license · Oct 2026</sub>

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
### #&#8288;93 [catboost](https://github.com/catboost/catboost) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (32) · Freshness: active (94) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;94 [pyro](https://github.com/pyro-ppl/pyro) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (31) · Freshness: active (100) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.1k · Apache-2.0 · Oct 2026</sub>

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

<a name="deepep"></a>
### #&#8288;95 [deepep](https://github.com/deepseek-ai/deepep) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (40) · Freshness: active (81) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

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

<a name="apex"></a>
### #&#8288;96 [apex](https://github.com/nvidia/apex) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: known (30) · Freshness: active (100) · Maintenance: weak (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · BSD-3-Clause · Sep 2026</sub>

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

<a name="face-recognition"></a>
### #&#8288;97 [face_recognition](https://github.com/ageitgey/face_recognition) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: widely used (92) · Freshness: recent (61) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 57k · MIT · Jun 2026</sub>

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

<a name="autograd"></a>
### #&#8288;98 [autograd](https://github.com/hips/autograd) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · MIT · Oct 2026</sub>

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

<a name="airsim"></a>
### #&#8288;99 [airsim](https://github.com/microsoft/airsim) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (65) · Freshness: recent (70) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · custom license · Sep 2026</sub>

**Unreal Engine drone and car simulator for autonomous vehicle research.**

AirSim is an Unreal Engine plugin, with an experimental Unity version, that simulates drones and cars. It supports software-in-the-loop with PX4 and ArduPilot, hardware-in-the-loop with PX4, and an RPC API for C++, Python, C# and Java to pull images and state and to control vehicles. It is aimed at deep learning, computer vision and reinforcement learning work.

- **+** Integrates with PX4 and ArduPilot for software-in-the-loop, plus PX4 hardware-in-the-loop
- **+** RPC API in C++, Python, C# and Java; client library can run on a companion computer
- **+** Computer Vision mode returns depth, disparity, normals and segmentation without vehicle physics
- **+** Built-in recording of pose and images, plus weather controls
- **−** Last release is 2022-07-18; the README points to a separate Project AirSim
- **−** Requires Unreal Engine; the Unity release is described as experimental
- **−** README lists no prebuilt binaries for macOS, only a build guide
- **−** Hardware requirements are not stated in the README

<sub>Needs Unreal Engine, Unity (experimental), PX4, ArduPilot · [Repo](https://github.com/microsoft/airsim) · [▶️ Demo ↗](https://youtu.be/-WfTr1-OBGQ) · [📖 Docs ↗](https://microsoft.github.io/AirSim/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/airsim/)</sub>

<a name="deepgemm"></a>
### #&#8288;100 [deepgemm](https://github.com/deepseek-ai/deepgemm) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: known (31) · Freshness: active (83) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.1k · MIT · Oct 2026</sub>

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

<a name="tensorboard"></a>
### #&#8288;101 [tensorboard](https://github.com/tensorflow/tensorboard) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Oct 2026</sub>

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

<a name="openmythos"></a>
### #&#8288;102 [openmythos](https://github.com/kyegomez/openmythos) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (57) · Freshness: recent (75) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · May 2026</sub>

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
### #&#8288;103 [paddledetection](https://github.com/paddlepaddle/paddledetection) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: popular (55) · Freshness: recent (61) · Maintenance: weak (14) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Mar 2026</sub>

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

<a name="sonnet"></a>
### #&#8288;104 [sonnet](https://github.com/google-deepmind/sonnet) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (37) · Freshness: recent (70) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10.0k · Apache-2.0 · Oct 2026</sub>

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

<a name="time-series-library"></a>
### #&#8288;105 [time-series-library](https://github.com/thuml/time-series-library) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: popular (51) · Freshness: recent (62) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Apr 2026</sub>

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

<a name="hyperopt"></a>
### #&#8288;106 [hyperopt](https://github.com/hyperopt/hyperopt) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (22) · Freshness: active (96) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · custom license · Jul 2026</sub>

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

<a name="deeplearning4j"></a>
### #&#8288;107 [deeplearning4j](https://github.com/deeplearning4j/deeplearning4j) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: popular (54) · Freshness: slowing (43) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Feb 2026</sub>

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

<a name="pycaret"></a>
### #&#8288;108 [pycaret](https://github.com/pycaret/pycaret) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (36) · Freshness: recent (51) · Maintenance: weak (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · custom license · May 2026</sub>

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

<a name="gsplat"></a>
### #&#8288;109 [gsplat](https://github.com/nerfstudio-project/gsplat) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (3) · Freshness: recent (75) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Sep 2026</sub>

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

<a name="deepchem"></a>
### #&#8288;110 [deepchem](https://github.com/deepchem/deepchem) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (15) · Freshness: recent (70) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Aug 2026</sub>

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

<a name="paddlex"></a>
### #&#8288;111 [paddlex](https://github.com/paddlepaddle/paddlex) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (8) · Freshness: active (91) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Jun 2026</sub>

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

<a name="imbalanced-learn"></a>
### #&#8288;112 [imbalanced-learn](https://github.com/scikit-learn-contrib/imbalanced-learn) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (15) · Freshness: active (86) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Jun 2026</sub>

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

<a name="argos-translate"></a>
### #&#8288;113 [argos-translate](https://github.com/argosopentech/argos-translate) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: niche (11) · Freshness: recent (70) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · MIT · Aug 2026</sub>

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

<a name="cleanrl"></a>
### #&#8288;114 [cleanrl](https://github.com/vwxyzjn/cleanrl) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: known (41) · Freshness: slowing (44) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Apr 2026</sub>

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
### #&#8288;115 [face-alignment](https://github.com/1adrianb/face-alignment) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (20) · Freshness: recent (68) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · BSD-3-Clause · Apr 2026</sub>

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

<a name="surprise"></a>
### #&#8288;116 [surprise](https://github.com/nicolashug/surprise) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (13) · Freshness: recent (77) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.8k · BSD-3-Clause · May 2026</sub>

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

<a name="gensim"></a>
### #&#8288;117 [gensim](https://github.com/piskvorky/gensim) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: popular (62) · Freshness: quiet (13) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · LGPL-2.1 · Oct 2025</sub>

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

<a name="dopamine"></a>
### #&#8288;118 [dopamine](https://github.com/google/dopamine) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: known (44) · Freshness: slowing (37) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Mar 2026</sub>

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

<a name="bertviz"></a>
### #&#8288;119 [bertviz](https://github.com/jessevig/bertviz) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: niche (25) · Freshness: quiet (20) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · Apache-2.0 · Jan 2026</sub>

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

<a name="slowfast"></a>
### #&#8288;120 [slowfast](https://github.com/facebookresearch/slowfast) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: niche (19) · Freshness: recent (50) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Mar 2026</sub>

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
### #&#8288;121 [tensortrade](https://github.com/tensortrade-org/tensortrade) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (17) · Freshness: slowing (49) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Feb 2026</sub>

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

<a name="autokeras"></a>
### #&#8288;122 [autokeras](https://github.com/keras-team/autokeras) <sub>score [17](../README.md#-how-we-rank "Score 17/100. Adoption: known (33) · Freshness: quiet (23) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · Nov 2025</sub>

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

<a name="deepo"></a>
### #&#8288;123 [deepo](https://github.com/ufoym/deepo) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: niche (8) · Freshness: slowing (37) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Mar 2026</sub>

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
### #&#8288;124 [pinns](https://github.com/maziarraissi/pinns) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: niche (7) · Freshness: slowing (38) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Feb 2026</sub>

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

<a name="paddleseg"></a>
### #&#8288;125 [paddleseg](https://github.com/paddlepaddle/paddleseg) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: known (34) · Freshness: quiet (6) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · Apache-2.0 · Nov 2025</sub>

**Image segmentation toolkit on PaddlePaddle, from training to deployment.**

PaddleSeg is a PaddlePaddle-based toolkit for image segmentation with 45+ model algorithms and 140+ pretrained models. It covers semantic, interactive, matting and panoptic segmentation, driven by YAML configs or a Python API, and includes compression and deployment tooling. The README also points to PaddleX for low-code use of 19 segmentation and anomaly-detection models.

- **+** Large model zoo: 45+ segmentation networks with Cityscapes and ADE20K benchmark tables
- **+** Covers semantic, interactive (EISeg), matting and panoptic segmentation in one repo
- **+** Includes quantization-aware distillation and deployment paths such as PaddleInference and PaddleLite
- **+** Modular configs separate backbones, losses, datasets and augmentations
- **−** Requires the PaddlePaddle framework, not PyTorch, which limits reuse with PyTorch tooling
- **−** Primary README is in Chinese, with English in a separate file
- **−** Last release was 2024-11-05; no Docker or compose files detected
- **−** Hardware and RAM requirements are not stated in the README excerpt

<sub>GPU optional · Needs PaddlePaddle · Models: PP-LiteSeg, PP-MobileSeg, DeepLabV3P, OCRNet, SegFormer · [Repo](https://github.com/paddlepaddle/paddleseg) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddleseg/)</sub>

<a name="aim"></a>
### #&#8288;126 [aim](https://github.com/aimhubio/aim) <sub>score [8](../README.md#-how-we-rank "Score 8/100. Adoption: niche (9) · Freshness: quiet (16) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Dec 2025</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
