# 🔬 ML frameworks and libraries reviews · Best of Open-Source AI

The libraries models are built and run with: tensor frameworks, model zoos and the tooling around them. Back to the [leaderboard](../README.md#-ml-frameworks-and-libraries).

<sub>🌐 Also on the web: [ML frameworks and libraries on archestack.com](https://archestack.com/best-of-ai/ml-frameworks/), each project on its own page.</sub>

<a name="transformers"></a>
### 🥇 [transformers](https://github.com/huggingface/transformers) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 168k · Apache-2.0 · Oct 2026</sub>

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
### 🥈 [pytorch](https://github.com/pytorch/pytorch) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 105k · custom license · Oct 2026</sub>

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

<a name="tensorflow"></a>
### 🥉 [tensorflow](https://github.com/tensorflow/tensorflow) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (99) · Freshness: active (97) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 201k · Apache-2.0 · Oct 2026</sub>

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

<a name="ultralytics"></a>
### #&#8288;4 [ultralytics](https://github.com/ultralytics/ultralytics) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 62k · AGPL-3.0 · Oct 2026</sub>

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

<a name="keras"></a>
### #&#8288;5 [keras](https://github.com/keras-team/keras) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;6 [scikit-learn](https://github.com/scikit-learn/scikit-learn) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · BSD-3-Clause · Oct 2026</sub>

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

<a name="models"></a>
### #&#8288;7 [models](https://github.com/tensorflow/models) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (67) · Freshness: active (95) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · custom license · Oct 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
