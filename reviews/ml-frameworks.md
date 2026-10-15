# 🔬 ML frameworks and libraries reviews · Best of Open-Source AI

The libraries models are built and run with: tensor frameworks, model zoos and the tooling around them. Back to the [leaderboard](../README.md#-ml-frameworks-and-libraries).

<sub>🌐 Also on the web: [ML frameworks and libraries on archestack.com](https://archestack.com/best-of-ai/ml-frameworks/), each project on its own page.</sub>

<a name="transformers"></a>
### 🥇 [transformers](https://github.com/huggingface/transformers) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 168k · Apache-2.0 · Oct 2026</sub>

**Model-definition library for text, vision, audio and multimodal models.**

Transformers is a Python library that defines model architectures for text, vision, audio, video and multimodal models and loads pretrained checkpoints from the Hugging Face Hub. It offers a Pipeline API for inference, a PyTorch-based training API, and `transformers serve` and `transformers chat` commands. Other training frameworks and inference engines reuse its model definitions.

- **+** Hundreds of architectures and 1M+ Hub checkpoints behind one unified API
- **+** Pipeline API covers text, audio, vision and multimodal tasks in a few lines
- **+** Definitions are reused by Axolotl, Unsloth, DeepSpeed, vLLM, SGLang, TGI and others
- **+** Model files are deliberately flat and usable independently of the library
- **−** Not a modular toolbox of neural net building blocks, per the README
- **−** Training API targets Transformers' PyTorch models; generic loops should use Accelerate
- **−** Example scripts are only examples and may need adapting
- **−** Requires Python 3.10+ and PyTorch 2.6+; RAM and GPU needs are not stated

<sub>GPU optional · Docker · Needs Python 3.10+, PyTorch 2.6+, Hugging Face Hub · Models: PyTorch, Hugging Face Hub checkpoints, text, vision, audio · [Repo](https://github.com/huggingface/transformers) · [📖 Docs ↗](https://huggingface.co/docs/transformers/index) · [🌐 Site ↗](https://huggingface.co/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transformers/)</sub>

<a name="pytorch"></a>
### 🥈 [pytorch](https://github.com/pytorch/pytorch) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 105k · custom license · Oct 2026</sub>

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
### 🥉 [ultralytics](https://github.com/ultralytics/ultralytics) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 63k · AGPL-3.0 · Oct 2026</sub>

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

<a name="supervision"></a>
### #&#8288;4 [supervision](https://github.com/roboflow/supervision) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · MIT · Oct 2026</sub>

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

<a name="pytorch-image-models"></a>
### #&#8288;5 [pytorch-image-models](https://github.com/huggingface/pytorch-image-models) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

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

<a name="tensorflow"></a>
### #&#8288;6 [tensorflow](https://github.com/tensorflow/tensorflow) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (99) · Freshness: active (96) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 201k · Apache-2.0 · Oct 2026</sub>

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

<a name="keras"></a>
### #&#8288;7 [keras](https://github.com/keras-team/keras) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Oct 2026</sub>

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

<a name="scikit-learn"></a>
### #&#8288;8 [scikit-learn](https://github.com/scikit-learn/scikit-learn) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · BSD-3-Clause · Oct 2026</sub>

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

<a name="ray"></a>
### #&#8288;9 [ray](https://github.com/ray-project/ray) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;10 [mediapipe](https://github.com/google-ai-edge/mediapipe) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · Apache-2.0 · Oct 2026</sub>

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

<a name="models"></a>
### #&#8288;11 [models](https://github.com/tensorflow/models) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: widely used (86) · Freshness: active (95) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · custom license · Oct 2026</sub>

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

<a name="diffusers"></a>
### #&#8288;12 [diffusers](https://github.com/huggingface/diffusers) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (41) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Oct 2026</sub>

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

<a name="jax"></a>
### #&#8288;13 [jax](https://github.com/jax-ml/jax) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · Apache-2.0 · Oct 2026</sub>

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

<a name="genesis-world"></a>
### #&#8288;14 [genesis-world](https://github.com/genesis-embodied-ai/genesis-world) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;15 [mlx](https://github.com/ml-explore/mlx) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Oct 2026</sub>

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

<a name="tinygrad"></a>
### #&#8288;16 [tinygrad](https://github.com/tinygrad/tinygrad) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: known (35) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Oct 2026</sub>

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

<a name="xgboost"></a>
### #&#8288;17 [xgboost](https://github.com/dmlc/xgboost) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

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

<a name="spacy"></a>
### #&#8288;18 [spacy](https://github.com/explosion/spacy) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Sep 2026</sub>

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
### #&#8288;19 [fastai](https://github.com/fastai/fastai) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · Apache-2.0 · Sep 2026</sub>

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

<a name="pytorch-lightning"></a>
### #&#8288;20 [pytorch-lightning](https://github.com/lightning-ai/pytorch-lightning) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · Apache-2.0 · Sep 2026</sub>

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

<a name="detectron2"></a>
### #&#8288;21 [detectron2](https://github.com/facebookresearch/detectron2) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (44) · Freshness: recent (70) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Sep 2026</sub>

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

<a name="face-recognition"></a>
### #&#8288;22 [face_recognition](https://github.com/ageitgey/face_recognition) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (70) · Freshness: recent (64) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 57k · MIT · Jun 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
