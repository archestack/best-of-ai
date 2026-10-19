# 🔬 ML frameworks and libraries reviews · Best of Open-Source AI

The libraries models are built and run with: tensor frameworks, model zoos and the tooling around them. Back to the [leaderboard](../README.md#-ml-frameworks-and-libraries).

<sub>🌐 Also on the web: [ML frameworks and libraries on archestack.com](https://archestack.com/best-of-ai/ml-frameworks/), each project on its own page.</sub>

<a name="transformers"></a>
### 🥇 [transformers](https://github.com/huggingface/transformers) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 168k · Apache-2.0 · Oct 2026</sub>

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
### 🥈 [pytorch](https://github.com/pytorch/pytorch) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 105k · custom license · Oct 2026</sub>

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

<a name="ultralytics"></a>
### 🥉 [ultralytics](https://github.com/ultralytics/ultralytics) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 63k · AGPL-3.0 · Oct 2026</sub>

**Python library and CLI for training and running YOLO vision models.**

Ultralytics provides the `ultralytics` Python package and `yolo` CLI for training, validating, predicting, tracking and exporting YOLO models. Tasks include detection, instance and semantic segmentation, depth estimation, classification, pose and oriented boxes. Pretrained YOLO26 weights download on first use, and models export to formats such as ONNX.

- **+** One package and CLI cover train, val, predict, track and export across seven vision tasks
- **+** Pretrained YOLO26 n/s/m/l/x weights with published COCO mAP and CPU/T4 latency tables
- **+** Supports older YOLO versions back to YOLOv3, plus export to ONNX
- **+** Install via pip, Conda or Docker; docs in multiple languages
- **−** AGPL-3.0 license; commercial use needs a paid Enterprise License
- **−** Vision only; no LLM or language model support
- **−** Pretrained weights download from Ultralytics releases at first use
- **−** YOLO27 is announced but unavailable, with no launch date

<sub>GPU optional · Docker · Needs Python>=3.8, PyTorch>=1.8 · Models: YOLO26, YOLOv3, ONNX export, TensorRT export · [Repo](https://github.com/ultralytics/ultralytics) · [📖 Docs ↗](https://docs.ultralytics.com) · [🌐 Site ↗](https://www.ultralytics.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ultralytics/)</sub>

<a name="pytorch-image-models"></a>
### #&#8288;4 [pytorch-image-models](https://github.com/huggingface/pytorch-image-models) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;5 [supervision](https://github.com/roboflow/supervision) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · MIT · Oct 2026</sub>

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

<a name="keras"></a>
### #&#8288;6 [keras](https://github.com/keras-team/keras) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Oct 2026</sub>

**Multi-backend deep learning library running on JAX, TensorFlow and PyTorch.**

Keras 3 is a high-level Python API for building and training neural networks. The backend is chosen with the KERAS_BACKEND variable or ~/.keras/keras.json. It trains on JAX, TensorFlow or PyTorch, and OpenVINO is supported for inference only. It is meant as a drop-in replacement for tf.keras and accepts tf.data pipelines and PyTorch DataLoaders as input.

- **+** Same model code runs on JAX, TensorFlow or PyTorch by switching one environment variable
- **+** Keras models can be used inside native PyTorch Modules or JAX functions
- **+** Accepts tf.data.Dataset and PyTorch DataLoader inputs regardless of backend
- **+** Drop-in replacement for tf.keras when models are saved in the .keras format
- **−** Backend must be set before import and cannot be changed afterwards
- **−** OpenVINO backend only supports model.predict(), no training
- **−** Only Linux and macOS are listed as compatible; Windows needs WSL2
- **−** Custom layers or train_step() need conversion to be backend-agnostic

<sub>GPU optional · Needs tensorflow >=2.16.1, jax >=0.4.20, or torch >=2.1.0 (one backend), openvino 2026.2.0 (inference only) · Models: JAX, TensorFlow, PyTorch, OpenVINO (inference only) · [Repo](https://github.com/keras-team/keras) · [🌐 Site ↗](https://keras.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/keras/)</sub>

<a name="ray"></a>
### #&#8288;7 [ray](https://github.com/ray-project/ray) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · Apache-2.0 · Oct 2026</sub>

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

<a name="diffusers"></a>
### #&#8288;8 [diffusers](https://github.com/huggingface/diffusers) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Oct 2026</sub>

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

<a name="tensorflow"></a>
### #&#8288;9 [tensorflow](https://github.com/tensorflow/tensorflow) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (100) · Freshness: active (96) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 201k · Apache-2.0 · Oct 2026</sub>

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

<a name="mediapipe"></a>
### #&#8288;10 [mediapipe](https://github.com/google-ai-edge/mediapipe) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

**Cross-platform on-device ML pipelines and ready-made vision, text and audio tasks.**

MediaPipe is Google's C++ framework for building on-device ML pipelines from packets, graphs and calculators. It also ships MediaPipe Solutions: Tasks APIs with pre-trained models for vision, text and audio, Model Maker for customizing models with your data, and MediaPipe Studio for browser-based evaluation. Targets are Android, iOS, web, desktop, edge devices and IoT.

- **+** Tasks APIs cover vision, text and audio with pre-trained models, targeting Android, iOS, web and Python
- **+** Input data is processed on device and not sent to Google servers
- **+** Model Maker customizes models on your data; Studio benchmarks them in the browser
- **+** Low-level Framework lets you build custom C++ graphs from calculators
- **−** Tasks APIs send performance and usage metrics to Google; app developers must obtain user consent
- **−** Several legacy solutions are no longer supported; code is kept as-is
- **−** README marks MediaPipe Solutions as a preview, early release
- **−** Primary docs live on a separate Google site; the README is mostly links

<sub>GPU optional · Docker · Models: MediaPipe pre-trained task models, custom models via Model Maker · [Repo](https://github.com/google-ai-edge/mediapipe) · [▶️ Demo ↗](https://goo.gle/mediapipe-studio) · [📖 Docs ↗](https://developers.google.com/mediapipe/solutions) · [🌐 Site ↗](https://developers.google.com/mediapipe) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mediapipe/)</sub>

<a name="genesis-world"></a>
### #&#8288;11 [genesis-world](https://github.com/genesis-embodied-ai/genesis-world) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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

<a name="scikit-learn"></a>
### #&#8288;12 [scikit-learn](https://github.com/scikit-learn/scikit-learn) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · BSD-3-Clause · Oct 2026</sub>

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

<a name="mlx"></a>
### #&#8288;13 [mlx](https://github.com/ml-explore/mlx) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Oct 2026</sub>

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

<a name="jax"></a>
### #&#8288;14 [jax](https://github.com/jax-ml/jax) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · Apache-2.0 · Oct 2026</sub>

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

<a name="tinygrad"></a>
### #&#8288;15 [tinygrad](https://github.com/tinygrad/tinygrad) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Oct 2026</sub>

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

<a name="lerobot"></a>
### #&#8288;16 [lerobot](https://github.com/huggingface/lerobot) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;17 [flash-attention](https://github.com/dao-ailab/flash-attention) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · BSD-3-Clause · Oct 2026</sub>

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

<a name="onnx"></a>
### #&#8288;18 [onnx](https://github.com/onnx/onnx) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Oct 2026</sub>

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

<a name="models"></a>
### #&#8288;19 [models](https://github.com/tensorflow/models) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (93) · Freshness: active (94) · Maintenance: fair (61) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · custom license · Oct 2026</sub>

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

<a name="xgboost"></a>
### #&#8288;20 [xgboost](https://github.com/dmlc/xgboost) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

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

<a name="deepface"></a>
### #&#8288;21 [deepface](https://github.com/serengil/deepface) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Oct 2026</sub>

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

<a name="shap"></a>
### #&#8288;22 [shap](https://github.com/shap/shap) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

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

<a name="onnxruntime"></a>
### #&#8288;23 [onnxruntime](https://github.com/microsoft/onnxruntime) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Oct 2026</sub>

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

<a name="burn"></a>
### #&#8288;24 [burn](https://github.com/tracel-ai/burn) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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

<a name="fastai"></a>
### #&#8288;25 [fastai](https://github.com/fastai/fastai) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · Apache-2.0 · Sep 2026</sub>

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

<a name="spacy"></a>
### #&#8288;26 [spacy](https://github.com/explosion/spacy) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Sep 2026</sub>

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

<a name="paddle"></a>
### #&#8288;27 [paddle](https://github.com/paddlepaddle/paddle) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Oct 2026</sub>

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

<a name="sentence-transformers"></a>
### #&#8288;28 [sentence-transformers](https://github.com/huggingface/sentence-transformers) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Oct 2026</sub>

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

<a name="transformers-js"></a>
### #&#8288;29 [transformers.js](https://github.com/huggingface/transformers.js) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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

<a name="pytorch-lightning"></a>
### #&#8288;30 [pytorch-lightning](https://github.com/lightning-ai/pytorch-lightning) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · Apache-2.0 · Sep 2026</sub>

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

<a name="mnn"></a>
### #&#8288;31 [mnn](https://github.com/alibaba/mnn) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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

<a name="datasets"></a>
### #&#8288;32 [datasets](https://github.com/huggingface/datasets) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (44) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Oct 2026</sub>

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

<a name="triton"></a>
### #&#8288;33 [triton](https://github.com/triton-lang/triton) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (39) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Oct 2026</sub>

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

<a name="optuna"></a>
### #&#8288;34 [optuna](https://github.com/optuna/optuna) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

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

<a name="ncnn"></a>
### #&#8288;35 [ncnn](https://github.com/tencent/ncnn) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (49) · Freshness: active (100) · Maintenance: patchy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Oct 2026</sub>

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
### #&#8288;36 [vision](https://github.com/pytorch/vision) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (32) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · BSD-3-Clause · Oct 2026</sub>

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

<a name="tvm"></a>
### #&#8288;37 [tvm](https://github.com/apache/tvm) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

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

<a name="vit-pytorch"></a>
### #&#8288;38 [vit-pytorch](https://github.com/lucidrains/vit-pytorch) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (54) · Freshness: active (94) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

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

<a name="pytorch-geometric"></a>
### #&#8288;39 [pytorch_geometric](https://github.com/pyg-team/pytorch_geometric) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Sep 2026</sub>

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

<a name="ggml"></a>
### #&#8288;40 [ggml](https://github.com/ggml-org/ggml) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Oct 2026</sub>

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

<a name="candle"></a>
### #&#8288;41 [candle](https://github.com/huggingface/candle) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: known (40) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;42 [lightgbm](https://github.com/lightgbm-org/lightgbm) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: known (35) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

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

<a name="finrl"></a>
### #&#8288;43 [finrl](https://github.com/ai4finance-foundation/finrl) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (30) · Freshness: active (97) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Oct 2026</sub>

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

<a name="dlib"></a>
### #&#8288;44 [dlib](https://github.com/davisking/dlib) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (16) · Freshness: active (98) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · BSL-1.0 · Oct 2026</sub>

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

<a name="gymnasium"></a>
### #&#8288;45 [gymnasium](https://github.com/farama-foundation/gymnasium) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Oct 2026</sub>

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

<a name="detectron2"></a>
### #&#8288;46 [detectron2](https://github.com/facebookresearch/detectron2) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (72) · Freshness: recent (70) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Sep 2026</sub>

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

<a name="lm-evaluation-harness"></a>
### #&#8288;47 [lm-evaluation-harness](https://github.com/eleutherai/lm-evaluation-harness) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Sep 2026</sub>

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

<a name="recommenders"></a>
### #&#8288;48 [recommenders](https://github.com/recommenders-team/recommenders) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (43) · Freshness: recent (70) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Sep 2026</sub>

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
### #&#8288;49 [carla](https://github.com/carla-simulator/carla) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (17) · Freshness: active (82) · Maintenance: patchy (47) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

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

<a name="face-recognition"></a>
### #&#8288;50 [face_recognition](https://github.com/ageitgey/face_recognition) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: widely used (86) · Freshness: recent (63) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 57k · MIT · Jun 2026</sub>

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

<a name="stable-baselines3"></a>
### #&#8288;51 [stable-baselines3](https://github.com/dlr-rm/stable-baselines3) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

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

<a name="dvc"></a>
### #&#8288;52 [dvc](https://github.com/treeverse/dvc) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (23) · Freshness: active (98) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Aug 2026</sub>

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

<a name="openmythos"></a>
### #&#8288;53 [openmythos](https://github.com/kyegomez/openmythos) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: niche (19) · Freshness: recent (79) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · May 2026</sub>

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
### #&#8288;54 [paddledetection](https://github.com/paddlepaddle/paddledetection) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: niche (15) · Freshness: recent (65) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Mar 2026</sub>

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

<a name="time-series-library"></a>
### #&#8288;55 [time-series-library](https://github.com/thuml/time-series-library) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: niche (9) · Freshness: recent (66) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Apr 2026</sub>

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

<a name="gensim"></a>
### #&#8288;56 [gensim](https://github.com/piskvorky/gensim) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (28) · Freshness: quiet (14) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · LGPL-2.1 · Oct 2025</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
