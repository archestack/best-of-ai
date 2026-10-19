# 🎙️ Voice reviews · Best of Open-Source AI

Speech-to-text, text-to-speech, voice agents and meeting tools that run locally. Back to the [leaderboard](../README.md#%EF%B8%8F-voice).

<sub>🌐 Also on the web: [Voice on archestack.com](https://archestack.com/best-of-ai/voice/), each project on its own page.</sub>

<a name="voicestudio"></a>
### 🥇 [voicestudio](https://github.com/debpalash/voicestudio) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (95) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 75k · AGPL-3.0 · Oct 2026</sub>

**Desktop app for voice cloning, dubbing and dictation with local speech models.**

VoiceStudio is an Electron desktop app with a Python backend for voice cloning, text-described voice design, timed video dubbing, dictation, transcription and audiobook creation. The default engine is k2-fsa/OmniVoice, with other engines selectable and models installed through a Model Manager. It also exposes a local API and an MCP server for agents.

- **+** Covers cloning, voice design, dubbing, dictation and audiobooks in one app
- **+** CUDA on NVIDIA, Metal on Apple Silicon, and a CPU fallback
- **+** Local API and MCP for agents, plus watch folders and reusable recipes
- **+** Installers for macOS, Windows and Linux, plus Docker
- **−** AGPL-3.0 app licence; model weights and voices carry separate terms
- **−** CPU-only use is slower; CPU PyTorch setup needs about 5 GB disk
- **−** Intel Mac runs the UI only and needs a remote backend
- **−** Windows on ARM is experimental and CPU only

<sub>GPU optional · Docker + Compose · Needs Electron, Python, PyTorch, Bun (source build), Node.js 22+ (source build) · Models: k2-fsa/OmniVoice · [Repo](https://github.com/debpalash/voicestudio) · [📖 Docs ↗](https://github.com/debpalash/VoiceStudio/blob/main/docs/engines/README.md) · [🌐 Site ↗](https://voicestudio.sh/?utm_source=github&utm_medium=readme&utm_campaign=project) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voicestudio/)</sub>

<a name="whisper-cpp"></a>
### 🥈 [whisper.cpp](https://github.com/ggml-org/whisper.cpp) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 54k · MIT · Oct 2026</sub>

**C/C++ port of OpenAI Whisper for local speech-to-text transcription.**

whisper.cpp runs OpenAI's Whisper speech recognition models in plain C/C++ on top of the ggml library, with a C-style API in whisper.h and a whisper-cli example for transcribing 16-bit WAV files. It runs on CPU or can offload to Metal, Core ML, CUDA, Vulkan, ROCm, OpenVINO, Ascend CANN, Moore Threads MUSA and AMD Ryzen AI NPUs. It supports integer quantization and voice activity detection, and builds for desktop, mobile, WebAssembly and Docker.

- **+** No dependencies in core; zero memory allocations at runtime
- **+** Wide backend coverage: Metal, Core ML, CUDA, Vulkan, ROCm, OpenVINO, CANN, MUSA, NPU
- **+** Runs on iOS, Android, WebAssembly, Raspberry Pi, and Java bindings exist
- **+** Q5_0-style integer quantization shrinks models; base model needs about 388 MB RAM
- **−** whisper-cli accepts only 16-bit WAV unless built with optional FFmpeg support
- **−** Core ML, OpenVINO and VitisAI encoders need a separate Python conversion step
- **−** Models must be in ggml format; downloaded via script, not bundled
- **−** Library and CLI only; no built-in web UI or multi-user features

<sub>GPU optional · Docker · Needs CMake, ffmpeg (optional), CUDA / ROCm / Vulkan / OpenVINO (optional backends) · Models: Whisper ggml (tiny, base, small, medium, large-v1/v2/v3, large-v3-turbo), Quantized ggml (e.g. q5_0) · [Repo](https://github.com/ggml-org/whisper.cpp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisper-cpp/)</sub>

<a name="voicebox"></a>
### 🥉 [Voicebox](https://github.com/jamiepine/voicebox) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: fair (53) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · MIT · Oct 2026</sub>

**Local voice studio for cloning, TTS, dictation and agent speech.**

Desktop app (Tauri) and Docker service that clones voices from a short sample and generates speech through eight TTS engines, including Qwen3-TTS, Chatterbox and Kokoro, in 23 languages. Adds Whisper dictation with a global hotkey, a REST API on port 17493 and an MCP server so coding agents can speak in a cloned voice. For individuals who want ElevenLabs-style voice I/O on their own machine.

- **+** Eight switchable TTS engines; Chatterbox Multilingual covers 23 languages
- **+** REST API plus HTTP and stdio MCP server for Claude Code, Cursor, Windsurf
- **+** Runs on MLX, CUDA, ROCm, DirectML, Intel Arc or CPU
- **+** Auto-chunking with crossfade handles scripts up to 50,000 characters
- **−** No prebuilt Linux binaries; build from source or use Docker
- **−** Only Chatterbox Turbo honors tags like [laugh]; other engines read them aloud
- **−** Dictation auto-paste and the permission flow are macOS-specific
- **−** Docker deployment gets one line in the README; details are in external docs

<sub>GPU optional · Docker + Compose · Models: Qwen3-TTS 0.6B/1.7B, Qwen CustomVoice, Qwen VoiceDesign, LuxTTS, Chatterbox Multilingual · port 17493 · README: alternative to ElevenLabs · [Repo](https://github.com/jamiepine/voicebox) · [📖 Docs ↗](https://docs.voicebox.sh) · [🌐 Site ↗](https://voicebox.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voicebox/)</sub>

<a name="buzz"></a>
### #&#8288;4 [buzz](https://github.com/chidiwilliams/buzz) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (47) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Oct 2026</sub>

**Offline desktop app for transcribing and translating audio with Whisper.**

Buzz is a desktop app that transcribes and translates audio and video files, YouTube links, or live microphone input with OpenAI's Whisper, on the local machine. It supports several Whisper backends (Whisper.cpp with Vulkan, CUDA, Apple Silicon, Hugging Face models) and exports to TXT, SRT and VTT. It also has a CLI, a watch folder and a plugin system.

- **+** Runs offline; transcription and translation stay on the local machine
- **+** Several Whisper backends: Whisper.cpp with Vulkan, CUDA, Apple Silicon, Hugging Face models
- **+** Speaker identification and speech separation for noisy audio
- **+** CLI and watch folder allow scripted or automatic transcription
- **−** Current releases require Apple silicon; last Intel Mac version is 1.4.5
- **−** Windows installer is unsigned and triggers a security warning
- **−** PyPI install needs ffmpeg, Python 3.12 and manual torch CUDA setup for GPU
- **−** Export formats listed are only TXT, SRT and VTT

<sub>GPU optional · Needs ffmpeg (PyPI install), Python 3.12 (PyPI install) · Models: Whisper, Whisper.cpp, Hugging Face Whisper-type models · [Repo](https://github.com/chidiwilliams/buzz) · [📖 Docs ↗](https://chidiwilliams.github.io/buzz/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/buzz/)</sub>

<a name="meetily"></a>
### #&#8288;5 [meetily](https://github.com/zackriya-solutions/meetily) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: fair (64) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Sep 2026</sub>

**Desktop app that records, transcribes and summarizes meetings locally.**

Meetily is a Tauri desktop app with a Rust backend and a Next.js frontend. It captures microphone and system audio, transcribes on-device with Whisper or Parakeet models, and generates summaries through Ollama, Claude, Groq, OpenRouter, or any OpenAI-compatible endpoint. Installers exist for Windows and macOS; Linux requires a source build.

- **+** Transcription runs on-device with Whisper or Parakeet; no cloud needed
- **+** Summary provider is selectable, including local Ollama or a custom OpenAI-compatible endpoint
- **+** Records microphone and system audio together with mixing
- **+** Imports existing audio files and re-transcribes with another model or language (beta)
- **−** No prebuilt Linux package; must build from source
- **−** Speaker diarization is not in the community edition; planned for PRO
- **−** Custom summary templates, advanced exports and auto-join are PRO-only
- **−** Standard Windows installer uses Vulkan; CUDA needs a source build

<sub>GPU optional · Needs Ollama (optional, for local summaries) · Models: Whisper, Parakeet (ONNX), Ollama, Claude, Groq · [Repo](https://github.com/zackriya-solutions/meetily) · [▶️ Demo ↗](https://youtu.be/6FnhSC_eSz8) · [🌐 Site ↗](https://meetily.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/meetily/)</sub>

<a name="speech-to-speech"></a>
### #&#8288;6 [Speech-to-Speech](https://github.com/huggingface/speech-to-speech) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

**Local voice agent pipeline with an OpenAI Realtime-compatible server.**

Runs a cascaded voice pipeline (Silero VAD, Parakeet TDT, Qwen3.5-4B, Qwen3-TTS) on your own machine, with each stage swappable. The server speaks the OpenAI Realtime protocol over WebSocket and WebRTC at ws://127.0.0.1:8765/v1/realtime, so Realtime clients can be pointed at it. It also ships a packaged mic/speaker client and can use llama.cpp or hosted OpenAI-compatible LLMs.

- **+** Core OpenAI Realtime events over WebSocket and WebRTC; CI tests the OpenAI Agents SDK
- **+** Many swappable backends: Whisper variants, Parakeet, Kokoro, Pocket TTS, OpenAI-compatible endpoints
- **+** Works offline after first model download; no API key needed for default pipeline
- **+** Apple Silicon runs all three models through MLX; CUDA and CPU paths also exist
- **−** Realtime support is a tested core subset, not full OpenAI Realtime API parity
- **−** Default Linux Qwen3-TTS wheel targets CUDA 12.8 and Ubuntu 24.04; others need manual wheels
- **−** Plan for 24 GB VRAM on NVIDIA; CPU-only runs give slow replies
- **−** LLM proxy has no authentication or throttling; needs a trusted network or gateway

<sub>RAM ≥ 16 GB · GPU optional · Docker + Compose · Needs PortAudio and libsndfile (Ubuntu), NVIDIA Container Toolkit (Docker), llama.cpp server (Docker compose) · Models: Qwen3.5-4B, Parakeet TDT, Qwen3-TTS, Whisper, Kokoro-82M · port 8765 · [Repo](https://github.com/huggingface/speech-to-speech) · [📖 Docs ↗](https://github.com/huggingface/speech-to-speech/blob/main/docs/configuration.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speech-to-speech/)</sub>

<a name="funasr"></a>
### #&#8288;7 [funasr](https://github.com/modelscope/funasr) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Oct 2026</sub>

**Speech recognition toolkit with VAD, punctuation, speaker labels and streaming.**

FunASR is a Python toolkit that runs speech recognition checkpoints (Fun-ASR-Nano, SenseVoiceSmall, Paraformer) through an AutoModel API, with optional FSMN-VAD, punctuation and CAM++ speaker clustering. It also ships a CLI, an OpenAI-compatible transcription server (funasr-server), a streaming runtime, and llama.cpp/GGUF binaries for CPU and edge devices without Python.

- **+** Offline and chunked streaming ASR (Paraformer-zh-streaming) in one toolkit
- **+** GGUF/llama.cpp binaries run SenseVoice on CPU, Vulkan or CUDA without Python
- **+** Composable pipeline: VAD, punctuation, anonymous speaker labels, emotion and event tags
- **+** OpenAI-style /v1/audio/transcriptions endpoint plus MCP server and CLI with SRT/JSON output
- **−** Speaker labels are anonymous per recording, not known-person identification
- **−** Language coverage is per checkpoint; base Nano is only zh/en/ja plus Chinese dialects
- **−** Bundled server is unauthenticated and should stay on loopback
- **−** Runtime support differs by backend; GGUF weights are not usable from Python AutoModel

<sub>GPU optional · Needs PyTorch, torchaudio, FastAPI, uvicorn, vLLM (optional, Nano GPU serving) · Models: Fun-ASR-Nano, Fun-ASR-MLT-Nano, SenseVoiceSmall, Paraformer-zh, Whisper-large-v3 · port 8000 · [Repo](https://github.com/modelscope/funasr) · [▶️ Demo ↗](https://huggingface.co/spaces/FunAudioLLM/Fun-ASR-Nano) · [📖 Docs ↗](https://www.funasr.com/en/docs/) · [🌐 Site ↗](https://www.funasr.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/funasr/)</sub>

<a name="kokoro-fastapi"></a>
### #&#8288;8 [Kokoro-FastAPI](https://github.com/remsky/kokoro-fastapi) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Oct 2026</sub>

**OpenAI-compatible text-to-speech server for the Kokoro-82M model.**

Wraps the Kokoro-82M TTS model in a FastAPI server that implements the OpenAI /v1/audio/speech endpoint, with streaming and output in mp3, wav, opus, flac, aac or pcm. It adds weighted voice mixing, inline multi-speaker tags, pause/rate/pronunciation tokens, per-word timestamps and phoneme endpoints. Prebuilt images cover CPU, NVIDIA CUDA and experimental AMD ROCm; Apple Silicon runs natively via uv.

- **+** Drop-in for the OpenAI speech API; works with the stock OpenAI Python client
- **+** Prebuilt CPU and CUDA images for amd64 and arm64 with models baked in
- **+** Voice mixing, aliases, inline speaker tags and timestamped captions
- **+** Bundled web UI at /web and Swagger docs at /docs
- **−** Tied to one model, Kokoro-82M; no other TTS engines
- **−** ROCm support is experimental and amd64 only
- **−** Apple Silicon GPU (MPS) needs a native uv run, not Docker
- **−** Voice tuning from a reference clip is off by default, English only, and approximate

<sub>GPU optional · Docker + Compose · Needs Docker or uv, espeak-ng (direct run, fallback) · Models: Kokoro-82M · port 8880 · [Repo](https://github.com/remsky/kokoro-fastapi) · [▶️ Demo ↗](https://huggingface.co/spaces/Remsky/FastKoko) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kokoro-fastapi/)</sub>

<a name="sherpa-onnx"></a>
### #&#8288;9 [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

**Offline speech recognition, TTS, diarization and VAD runtime built on ONNX Runtime.**

sherpa-onnx runs speech-to-text (streaming and non-streaming), text-to-speech, speaker diarization, speaker identification and verification, VAD, keyword spotting, speech enhancement and source separation locally. It is written in C++ with bindings for C, Python, JavaScript, Java, C#, Kotlin, Swift, Go, Dart, Rust and Pascal. Targets include Android, iOS, HarmonyOS, Windows, macOS, Linux, WebAssembly and several NPUs.

- **+** Covers ASR, TTS, diarization, VAD, keyword spotting and enhancement in one library
- **+** Bindings for 12 languages, plus Flutter and Tauri demo apps
- **+** Runs on x64, x86, arm32, arm64 and riscv64, including Android, iOS and WebAssembly
- **+** NPU support for Rockchip, Qualcomm, Ascend, Axera and Intel; many pre-built APKs and browser demos
- **−** Library and SDK, not an end-user app; you integrate it in code
- **−** Models are downloaded separately, and you choose among many ASR and TTS variants
- **−** No Docker or compose files detected
- **−** RAM and VRAM requirements are not stated in the README; they depend on the model

<sub>GPU optional · Needs ONNX Runtime · Models: ONNX, Zipformer, Paraformer, Whisper, SenseVoice · [Repo](https://github.com/k2-fsa/sherpa-onnx) · [▶️ Demo ↗](https://huggingface.co/spaces/k2-fsa/automatic-speech-recognition) · [📖 Docs ↗](https://k2-fsa.github.io/sherpa/onnx/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sherpa-onnx/)</sub>

<a name="agents"></a>
### #&#8288;10 [agents](https://github.com/livekit/agents) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

**Python framework for realtime voice and multimodal agents on LiveKit WebRTC.**

LiveKit Agents is a Python framework for building server-side agents that join LiveKit rooms as realtime participants. It wires together VAD, STT, LLM and TTS (or a realtime model API) through plugins, with tool calling, multi-agent handoff, job dispatch, SIP telephony and MCP tool support. A built-in test framework can run agent sessions and judge replies with an LLM.

- **+** Mix STT, LLM, TTS or realtime APIs via plugins (OpenAI, Deepgram, Cartesia, Google)
- **+** Built-in job dispatch and AgentServer for scheduling sessions across processes
- **+** Telephony via LiveKit SIP for inbound and outbound calls
- **+** Test framework asserts on tool calls and uses LLM judges for replies
- **−** Needs a LiveKit server (Cloud or self-hosted) and credentials beyond console mode
- **−** README examples default to LiveKit Inference, a LiveKit Cloud service
- **−** Turn detection models use the LiveKit Model License, not Apache-2.0
- **−** This repo is Python only; the JS/TS library is a separate repository

<sub>no GPU · Needs LiveKit server or LiveKit Cloud, STT/LLM/TTS provider API keys or LiveKit Inference · Models: OpenAI, Deepgram, Cartesia, Google Gemini, OpenAI Realtime API · [Repo](https://github.com/livekit/agents) · [▶️ Demo ↗](https://agents-playground.livekit.io/) · [📖 Docs ↗](https://docs.livekit.io/agents/) · [🌐 Site ↗](https://livekit.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agents/)</sub>

<a name="pocket-tts"></a>
### #&#8288;11 [Pocket TTS](https://github.com/kyutai-labs/pocket-tts) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · MIT · Oct 2026</sub>

**CPU-only text-to-speech model with voice cloning and streaming.**

Pocket TTS is a 100M-parameter text-to-speech model from Kyutai that runs on CPU, using about 2 cores. It ships a Python API and a CLI with generate, serve and export-voice commands, and clones voices from a wav sample. It supports seven languages, streams audio with roughly 200ms to first chunk, and reaches about 6x real-time on a MacBook Air M4.

- **+** Runs on 2 CPU cores, no GPU required; about 6x real-time on a MacBook Air M4
- **+** Voice cloning from a wav file, with export to safetensors for fast reloads
- **+** Seven languages (en, fr, de, pt, it, es, nl) plus community models such as Czech, Hindi and Korean
- **+** Installs with pip or uvx; serve command gives a local web UI and HTTP endpoint
- **−** GPU use is unofficial: no device argument on load_model, and serve and Docker image are CPU-only
- **−** Cannot insert silence in the text input to create pauses
- **−** Default Linux pip install pulls CUDA PyTorch (~3 GB) unless the CPU index is passed
- **−** Pre-made voice embeddings do not work with community-trained models

<sub>no GPU · Docker + Compose · Needs PyTorch 2.5+, Python 3.10-3.14 · Models: Pocket TTS 100M, English, French, German, Portuguese · port 8000 · [Repo](https://github.com/kyutai-labs/pocket-tts) · [▶️ Demo ↗](https://kyutai.org/pocket-tts) · [📖 Docs ↗](https://kyutai-labs.github.io/pocket-tts/) · [🌐 Site ↗](https://kyutai.org/pocket-tts) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pocket-tts/)</sub>

<a name="index-tts"></a>
### #&#8288;12 [IndexTTS](https://github.com/index-tts/index-tts) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: fair (77) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Sep 2026</sub>

**Zero-shot TTS with emotion, speed and pronunciation control.**

Clones a voice from one reference clip and synthesizes speech in Chinese, English, Japanese, Spanish and Arabic (IndexTTS-2.5). Emotion comes from a second reference clip, an 8-value vector or the text itself; speed is set by duration_factor (0.5x to 2.0x) and pronunciation by inline Pinyin, CMU phonemes or Kana. Ships a Gradio web UI on port 7860 and a Python API; a vLLM recipe covers production serving.

- **+** Emotion control via reference audio, an 8-value vector or a text description
- **+** Inline pronunciation overrides: Pinyin, CMU phonemes and Japanese Kana
- **+** BF16 inference with optional DeepSpeed and compiled CUDA kernels
- **+** Published vLLM recipe for production deployment
- **−** No Dockerfile or compose file; install is uv plus CUDA Toolkit 12.8 or newer
- **−** Model weights (IndexTTS-2.5, IndexTTS-2) are separate multi-GB downloads
- **−** Five languages only; no streaming API is documented in the README
- **−** License is non-standard (GitHub reports NOASSERTION); check terms before commercial use

<sub>Needs uv · Models: IndexTTS-2.5, IndexTTS-2, IndexTTS-1.5 (legacy) · port 7860 · [Repo](https://github.com/index-tts/index-tts) · [▶️ Demo ↗](https://huggingface.co/spaces/IndexTeam/IndexTTS-2.5-Demo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/index-tts/)</sub>

<a name="voxcpm"></a>
### #&#8288;13 [voxcpm](https://github.com/openbmb/voxcpm) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: patchy (35) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · Apache-2.0 · Oct 2026</sub>

**2B-parameter text-to-speech model with voice design and voice cloning.**

VoxCPM2 is a 2B-parameter, tokenizer-free TTS model built on a MiniCPM-4 backbone. It synthesizes 48kHz speech in 30 languages, creates voices from a text description, and clones voices from a short reference clip, optionally with a transcript for continuation cloning. It ships as a pip package with a Python API, CLI and web demo, and can be served through Nano-vLLM, vLLM-Omni or llama.cpp-omni.

- **+** Voice design from a text description, no reference audio needed
- **+** 30 languages plus nine Chinese dialects, no language tag required
- **+** Apache-2.0 weights and code, with SFT and LoRA fine-tuning support
- **+** Serving options: Nano-vLLM, vLLM-Omni (OpenAI-style endpoint), GGUF on llama.cpp-omni
- **−** Standard install requires CUDA 12.0 or newer and PyTorch 2.5.0 or newer
- **−** Python support limited to 3.10 through 3.12
- **−** RTF about 0.3 on RTX 4090 with the default PyTorch path
- **−** llama.cpp-omni path is slower: RTF about 1.76 on Apple M4 Pro

<sub>GPU required · Docker + Compose · Needs PyTorch >= 2.5.0, CUDA >= 12.0, Python 3.10-3.12 · Models: VoxCPM2, VoxCPM1.5, VoxCPM-0.5B, GGUF (llama.cpp-omni) · port 8808 · [Repo](https://github.com/openbmb/voxcpm) · [▶️ Demo ↗](https://huggingface.co/spaces/OpenBMB/VoxCPM-Demo) · [📖 Docs ↗](https://voxcpm.readthedocs.io/en/latest/) · [🌐 Site ↗](https://github.com/OpenBMB/VoxCPM/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voxcpm/)</sub>

<a name="openreader"></a>
### #&#8288;14 [OpenReader](https://github.com/richardr1126/openreader) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 544 · MIT · Oct 2026</sub>

**Reads EPUB, PDF and DOCX aloud with synced word highlighting.**

Next.js server that narrates EPUB, PDF, TXT, Markdown and DOCX files with synchronized read-along, generating audio ahead of playback through a self-hosted OpenAI-compatible TTS server (Kokoro-FastAPI, KittenTTS-FastAPI, Orpheus-FastAPI) or OpenAI, Replicate and DeepInfra. PDF layout is parsed with PP-DocLayoutV3 and words aligned with ONNX Whisper in a NATS JetStream worker. Exports M4B or MP3 audiobooks.

- **+** Layout-aware PDF parsing and word-by-word highlighting
- **+** Audio cache reused across seeks, reloads and audiobook export
- **+** Storage on embedded SeaweedFS or S3; SQLite or Postgres; built-in auth
- **+** amd64 and arm64 Docker images with automatic startup migrations
- **−** Needs a separate TTS server or cloud TTS API; nothing is bundled
- **−** Word alignment and DOCX conversion run in a NATS JetStream compute worker you deploy
- **−** Setup details (ports, env vars) are only in the external docs

<sub>no GPU · Docker · Needs OpenAI-compatible TTS server or cloud TTS API, NATS JetStream (compute worker), SQLite or PostgreSQL, SeaweedFS (embedded) or S3-compatible storage · Models: Kokoro-FastAPI, KittenTTS-FastAPI, Orpheus-FastAPI, OpenAI TTS, Replicate · [Repo](https://github.com/richardr1126/openreader) · [📖 Docs ↗](https://docs.openreader.richardr.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openreader/)</sub>

<a name="gpt-sovits"></a>
### #&#8288;15 [GPT-SoVITS](https://github.com/rvc-boss/gpt-sovits) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (90) · Freshness: recent (73) · Maintenance: patchy (34) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 63k · MIT · Oct 2026</sub>

**Few-shot voice cloning and TTS with a training web UI.**

Clones a voice from a 5-second sample (zero-shot) or fine-tunes GPT and SoVITS models on about one minute of audio, then synthesizes speech in Chinese, English, Japanese, Korean and Cantonese. The Gradio web UI bundles dataset tools: UVR5 vocal separation, slicing, ASR and label proofreading. Aimed at hobbyists and studios building custom voices locally.

- **+** Zero-shot cloning from 5 s of audio; few-shot fine-tune from about 1 minute
- **+** Cross-lingual synthesis across zh, en, ja, ko and yue
- **+** Compose services for CUDA 12.6 and 12.8, plus Lite images without ASR and UVR5 models
- **+** Reported RTF 0.028 on an RTX 4060 Ti for v2 ProPlus
- **−** Pretrained weights are separate downloads from Hugging Face or ModelScope
- **−** Docker images lag the code; README says to pull latest source before using them
- **−** Training on Apple Silicon GPUs gives lower quality; macOS falls back to CPU
- **−** Five model generations (v1 to v5) with different tradeoffs to choose between

<sub>GPU optional · Docker + Compose · Needs ffmpeg · Models: GPT-SoVITS v1-v5 pretrained models, UVR5 vocal separation models, Faster Whisper large-v3 (ASR), FunASR Paraformer (Chinese ASR) · [Repo](https://github.com/rvc-boss/gpt-sovits) · [▶️ Demo ↗](https://lj1995-gpt-sovits-proplus.hf.space/) · [📖 Docs ↗](https://rentry.co/GPT-SoVITS-guide#/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpt-sovits/)</sub>

<a name="vibevoice"></a>
### #&#8288;16 [vibevoice](https://github.com/microsoft/vibevoice) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: patchy (36) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 55k · MIT · Oct 2026</sub>

**Microsoft's open speech models for long-form ASR and streaming TTS.**

VibeVoice is a family of speech models built on 7.5 Hz continuous tokenizers and next-token diffusion. The ASR models transcribe up to 60 minutes of audio in one pass with speaker, timestamp and hotword support, plus a streaming variant and a CPU build. The TTS side includes a 0.5B real-time model with about 300 ms first-audio latency. The 1.5B long-form TTS code was removed from the repository after misuse.

- **+** ASR handles 60 minutes in one pass, returning speaker, timestamps and text together
- **+** Streaming ASR, vLLM serving and ASR fine-tuning code are documented
- **+** BitNet CPU build shrinks ASR from 4.62 GB to 1.58 GB, RTF under 1 on 3+ threads
- **+** Realtime TTS is 0.5B with about 300 ms first audible latency and streaming text input
- **−** VibeVoice-TTS code was removed; the 1.5B TTS model is listed as Disabled
- **−** README says it is for research only, not recommended for commercial use
- **−** Realtime TTS long-form output is about 10 minutes
- **−** README gives no RAM or VRAM requirements for the full models

<sub>GPU optional · Needs Hugging Face model weights, vLLM (optional, for serving) · Models: VibeVoice-ASR-7B, VibeVoice-ASR-Streaming, VibeVoice-ASR-BitNet, VibeVoice-Realtime-0.5B, VibeVoice-TTS-1.5B · [Repo](https://github.com/microsoft/vibevoice) · [▶️ Demo ↗](https://aka.ms/vibevoice-asr) · [📖 Docs ↗](https://github.com/microsoft/VibeVoice/blob/main/docs/vibevoice-asr.md) · [🌐 Site ↗](https://microsoft.github.io/VibeVoice) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vibevoice/)</sub>

<a name="f5-tts"></a>
### #&#8288;17 [F5-TTS](https://github.com/swivid/f5-tts) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (52) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

**Flow-matching TTS and voice cloning with Gradio and CLI.**

Synthesizes speech from a reference clip and its transcript using the F5-TTS diffusion transformer (plus an E2 TTS reproduction). Runs as a pip package with a Gradio web app on port 7860, a CLI and a Docker image; a Triton and TensorRT-LLM runtime reaches RTF 0.039 on an L20 GPU. Suited to researchers and builders who want a trainable open TTS model.

- **+** pip install f5-tts; Gradio UI, CLI and a ghcr.io Docker image
- **+** Triton plus TensorRT-LLM runtime: 253 ms average latency at concurrency 2 on L20
- **+** Training and fine-tuning via Accelerate or a Gradio finetune app
- **+** PyTorch install documented for NVIDIA, AMD ROCm, Intel XPU and Apple Silicon
- **−** Pretrained weights are CC-BY-NC (Emilia data); code is MIT, models are non-commercial
- **−** Reference audio needs a transcript, or an ASR model runs and uses more GPU memory
- **−** No compose file in the repo; the README's compose example assumes an NVIDIA GPU
- **−** Base checkpoints cover Chinese and English; other languages need community models

<sub>Docker · Needs ffmpeg · Models: F5-TTS v1 Base, E2 TTS, Vocos and BigVGAN vocoders · port 7860 · [Repo](https://github.com/swivid/f5-tts) · [▶️ Demo ↗](https://huggingface.co/spaces/mrfakename/E2-F5-TTS) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/f5-tts/)</sub>

<a name="speakr"></a>
### #&#8288;18 [Speakr](https://github.com/murtaza-nasir/speakr) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · AGPL-3.0 · Oct 2026</sub>

**Self-hosted audio transcription with speaker labels, summaries and chat over recordings.**

Speakr is a Flask and Vue web app that records or imports audio, transcribes it through a configurable engine (WhisperX, OpenAI, Mistral Voxtral, AssemblyAI and others), and generates summaries, titles and action items. It adds per-recording chat, semantic search across the library, tags with custom prompts, groups, OIDC SSO, a REST API and signed webhooks. Storage is SQLite by default or PostgreSQL.

- **+** Many ASR connectors, auto-detected from config, including fully self-hosted WhisperX and VibeVoice
- **+** Speaker diarization and cross-recording voice profiles with the WhisperX backend
- **+** Multi-user with OIDC SSO, groups, sharing, retention policies and per-user usage budgets
- **+** REST API with Swagger UI and HMAC-signed webhooks for n8n, Zapier or Make
- **−** Voice profiles and WhisperX diarization need a separate ASR container with a GPU
- **−** Version is 0.10.14-alpha; the release is labeled alpha
- **−** Summaries and chat need an external LLM API key, or a local model such as Ollama
- **−** Full image is about 4.4GB; lite image falls back to basic text search

<sub>GPU optional · Docker · Needs WhisperX ASR service (optional, GPU), OpenAI-compatible LLM API (OpenRouter, OpenAI or Ollama), SQLite or PostgreSQL · Models: WhisperX, OpenAI Transcribe, Mistral Voxtral, AssemblyAI, VibeVoice · port 8899 · [Repo](https://github.com/murtaza-nasir/speakr) · [📖 Docs ↗](https://murtaza-nasir.github.io/speakr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speakr/)</sub>

<a name="faster-whisper"></a>
### #&#8288;19 [faster-whisper](https://github.com/systran/faster-whisper) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (57) · Freshness: active (86) · Maintenance: fair (57) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

**Python Whisper speech-to-text library built on CTranslate2.**

Reimplementation of OpenAI's Whisper on the CTranslate2 inference engine, installed with pip and used from Python. The README reports up to 4x faster transcription than openai/whisper with lower memory, with int8 quantization on CPU and GPU. It supports batched transcription, word-level timestamps, Silero VAD filtering, and Distil-Whisper checkpoints.

- **+** README benchmark: 13 min audio in 1m03s fp16 on RTX 3070 Ti, 17s with batch_size=8
- **+** int8 quantization on CPU and GPU cuts memory (2926MB vs 4525MB VRAM for large-v2)
- **+** No system FFmpeg needed; audio decoded through PyAV bundled libraries
- **+** Converts any Transformers-compatible Whisper model, including fine-tuned ones, with ct2-transformers-converter
- **−** Library only; no built-in server, UI or CLI (these come from community projects)
- **−** GPU needs separately installed cuBLAS for CUDA 12 and cuDNN 9
- **−** Older CUDA 11 or cuDNN 8 setups require downgrading ctranslate2
- **−** whisper.cpp was faster on the README's CPU fp32 benchmark (2m05s vs 2m37s)

<sub>GPU optional · Docker · Needs CTranslate2, PyAV, cuBLAS for CUDA 12 (GPU), cuDNN 9 (GPU), Silero VAD · Models: Whisper (CTranslate2 format), Distil-Whisper, Hugging Face Transformers Whisper conversion · [Repo](https://github.com/systran/faster-whisper) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/faster-whisper/)</sub>

<a name="whisper"></a>
### #&#8288;20 [whisper](https://github.com/openai/whisper) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: widely used (98) · Freshness: recent (75) · Maintenance: weak (20) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 111k · MIT · Aug 2026</sub>

**Multilingual speech recognition and translation model with Python and CLI interfaces.**

Whisper is a Transformer sequence-to-sequence model for speech recognition, speech-to-English translation, and language identification. It ships as a pip package with a `whisper` command and a Python API, in six sizes from tiny (39M parameters) to large (1550M), plus a turbo variant. Code and weights are MIT licensed.

- **+** Six model sizes (39M to 1550M parameters) trade accuracy for speed and VRAM
- **+** Handles transcription, translation to English and language identification in one model
- **+** Simple `whisper audio.mp3 --model turbo` CLI and a short Python API
- **+** Code and weights both under MIT license
- **−** No built-in HTTP server or web UI; you wrap it yourself
- **−** The turbo model is not trained for translation and returns the original language
- **−** Requires ffmpeg, and possibly Rust for tiktoken if no prebuilt wheel exists
- **−** Accuracy varies widely by language; large model needs about 10 GB VRAM

<sub>GPU optional · Needs ffmpeg, PyTorch, tiktoken, Rust (if no prebuilt tiktoken wheel) · Models: tiny, base, small, medium, large · [Repo](https://github.com/openai/whisper) · [📖 Docs ↗](https://github.com/openai/whisper/blob/main/model-card.md) · [🌐 Site ↗](https://openai.com/blog/whisper) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisper/)</sub>

<a name="whisperx"></a>
### #&#8288;21 [whisperx](https://github.com/m-bain/whisperx) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: weak (27) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · BSD-2-Clause · Oct 2026</sub>

**Batched Whisper transcription with word-level timestamps and speaker diarization.**

WhisperX transcribes audio with Whisper through a faster-whisper backend, using VAD-based batching. It then aligns words to the audio with language-specific wav2vec2 models and labels speakers with pyannote diarization. It runs as a CLI or Python library, and the README claims 70x realtime with large-v2.

- **+** Word-level timestamps via wav2vec2 forced alignment, not Whisper's utterance-level timing
- **+** Batched inference; README claims 70x realtime with large-v2 on GPU
- **+** large-v2 with beam_size=5 needs under 8GB GPU memory per README
- **+** Runs on CPU with --compute_type int8, including macOS
- **−** Diarization needs a Hugging Face token and accepting the pyannote model agreement
- **−** Words like "2014." or "£13.60" cannot be aligned and get no timing
- **−** Overlapping speech is handled poorly; README says diarization is far from perfect
- **−** Each language needs its own wav2vec2 alignment model; unsupported ones need manual setup

<sub>GPU optional · Needs CUDA toolkit 12.8 (GPU only), ffmpeg, Hugging Face token (diarization), pyannote-audio, faster-whisper · Models: Whisper (faster-whisper/CTranslate2), wav2vec2 alignment models, pyannote speaker-diarization-community-1, silero-vad · [Repo](https://github.com/m-bain/whisperx) · [▶️ Demo ↗](https://replicate.com/victor-upmeet/whisperx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisperx/)</sub>

<a name="whisperlive"></a>
### #&#8288;22 [WhisperLive](https://github.com/collabora/whisperlive) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: fair (66) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Oct 2026</sub>

**Near-real-time Whisper transcription server over WebSocket.**

Streams audio from a microphone, file, RTSP or HLS source to a server on port 9090 and returns partial and committed Whisper transcripts over WebSocket, with an optional OpenAI-compatible REST endpoint. Backends are faster-whisper (CPU, CUDA, ROCm), TensorRT-LLM and OpenVINO; extras include word timestamps, hotwords, pyannote diarization and translation. For teams embedding live captions or dictation.

- **+** Three inference backends: faster-whisper, TensorRT-LLM, OpenVINO (Intel iGPU/dGPU)
- **+** Prebuilt GPU, CPU and OpenVINO Docker images; ROCm Dockerfile
- **+** Word-level timestamps, hotword boosting and batched multi-client inference
- **+** Chrome, Firefox and iOS clients; Python streaming client for raw PCM
- **−** Defaults allow 4 clients and 600 s per connection; must be tuned for more
- **−** Without a fixed model, a new Whisper instance loads per client connection
- **−** TensorRT backend requires building engines and is recommended only via Docker
- **−** Diarization needs the optional pyannote.audio dependency

<sub>GPU optional · Docker · Needs PortAudio (client microphone input) · Models: Whisper via faster-whisper (CTranslate2), Whisper TensorRT-LLM engines, OpenVINO Whisper models · port 9090 · [Repo](https://github.com/collabora/whisperlive) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisperlive/)</sub>

<a name="chattts"></a>
### #&#8288;23 [chattts](https://github.com/2noise/chattts) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (74) · Freshness: recent (73) · Maintenance: weak (19) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · AGPL-3.0 · Apr 2026</sub>

**Text-to-speech model for dialogue, with laughter and pause control.**

ChatTTS is a Python text-to-speech model trained for conversational speech in English and Chinese, with multi-speaker support and token-level control over laughter, pauses and interjections. It installs from PyPI, outputs 24 kHz audio, and ships a simple WebUI and command-line example. The released weights are a 40,000-hour pretrained model without SFT, licensed CC BY-NC 4.0 for research use.

- **+** Token-level prosody control: [laugh], [uv_break], [lbreak], plus sentence-level oral/laugh/break prompts
- **+** Random speaker sampling with saved embeddings for timbre recovery
- **+** Streaming generation and zero-shot inference code are included
- **+** Runs with about 4 GB GPU memory for a 30-second clip; RTF around 0.3 on a 4090
- **−** Model weights are CC BY-NC 4.0, academic use only; no commercial use
- **−** Only English and Chinese supported; English is described as experimental
- **−** Autoregressive output is unstable: speaker drift and quality vary between samples
- **−** Repo is the algorithm and examples; no packaged server or Docker image

<sub>GPU optional · Needs PyTorch, torchaudio, vLLM (optional, Linux only) · Models: ChatTTS 40k-hour base model (Hugging Face) · [Repo](https://github.com/2noise/chattts) · [▶️ Demo ↗](https://colab.research.google.com/github/2noise/ChatTTS/blob/main/examples/ipynb/colab.ipynb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chattts/)</sub>

<a name="voice-pro"></a>
### #&#8288;24 [voice-pro](https://github.com/abus-aikorea/voice-pro) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (22) · Freshness: active (98) · Maintenance: weak (0) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · GPL-3.0 · Jul 2026</sub>

**Gradio web app for transcribing, translating and dubbing video with voice cloning.**

Voice-Pro is a Windows-oriented Gradio web UI that downloads YouTube media with yt-dlp, separates vocals with Demucs, transcribes with Whisper variants, translates, and re-voices with TTS. Voice cloning uses F5-TTS, E2-TTS and CosyVoice; Edge-TTS and kokoro cover standard synthesis. The README says development is paused, and only Windows with an NVIDIA GPU is verified.

- **+** Covers download, vocal separation, ASR, translation and TTS in one UI
- **+** Zero-shot cloning via F5-TTS, E2-TTS and CosyVoice, including Fun-CosyVoice3
- **+** uv installer keeps everything in installer_files/; no CUDA Toolkit or admin rights needed
- **+** Translates subtitle files (ASS, SSA, SRT) and supports live recognition and translation
- **−** README states development and updates are not possible for the time being
- **−** Only Windows with an NVIDIA GPU is verified; Mac and Linux are untested
- **−** No Docker or compose files; install is via start.bat
- **−** Free Google translation endpoint can rate-limit; Azure needs your own keys

<sub>GPU optional · Needs ffmpeg (auto-downloaded by start.bat), yt-dlp, uv, Azure TTS/Translator (optional) · Models: Whisper, Faster-Whisper, Whisper-Timestamped, F5-TTS, E2-TTS · README: alternative to ElevenLabs · [Repo](https://github.com/abus-aikorea/voice-pro) · [📖 Docs ↗](https://deepwiki.com/abus-aikorea/voice-pro) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voice-pro/)</sub>

<a name="real-time-voice-cloning"></a>
### #&#8288;25 [real-time-voice-cloning](https://github.com/corentinj/real-time-voice-cloning) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: widely used (87) · Freshness: recent (51) · Maintenance: weak (8) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · custom license · Mar 2026</sub>

**SV2TTS voice cloning toolbox: speech from a few seconds of reference audio.**

Implements the SV2TTS pipeline: a GE2E speaker encoder, a Tacotron synthesizer and a WaveRNN vocoder. It builds a voice representation from a short audio sample and generates speech from arbitrary text, through a GUI toolbox or a command-line demo. The README says the project is dated and points to newer options such as Chatterbox for higher quality.

- **+** Implements the full SV2TTS pipeline: encoder, synthesizer and vocoder in one repo
- **+** GUI toolbox and CLI entry points (demo_toolbox.py, demo_cli.py)
- **+** Pretrained models download automatically, with a Hugging Face fallback
- **+** Windows and Linux support, with CPU and CUDA extras via uv
- **−** README says audio quality is behind current SaaS and newer open-source models
- **−** No tagged releases and no Docker setup
- **−** Requires ffmpeg installed separately
- **−** License is not identified (NOASSERTION)

<sub>GPU optional · Needs ffmpeg, uv, Python · Models: SV2TTS, GE2E encoder, Tacotron synthesizer, WaveRNN vocoder · [Repo](https://github.com/corentinj/real-time-voice-cloning) · [▶️ Demo ↗](https://www.youtube.com/watch?v=-O_hYhToKoA) · [📖 Docs ↗](https://github.com/CorentinJ/Real-Time-Voice-Cloning/wiki/Training#datasets) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/real-time-voice-cloning/)</sub>

<a name="speaches"></a>
### #&#8288;26 [Speaches](https://github.com/speaches-ai/speaches) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (4) · Freshness: recent (66) · Maintenance: weak (8) · Easy to run: easy (67) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Apr 2026</sub>

**OpenAI-compatible STT and TTS server with faster-whisper, Kokoro and Piper.**

Exposes OpenAI-style audio endpoints: streaming transcription and translation through faster-whisper, speech generation through Kokoro and Piper, plus a Realtime API and audio chat completions. Models load on first request and unload after inactivity, on CPU or GPU, via Docker Compose. For self-hosters who want one container that OpenAI SDKs can talk to for speech.

- **+** Works with any OpenAI SDK; transcription streams over SSE
- **+** Dynamic model loading and unloading after idle time
- **+** Supports the Realtime API and audio-in, audio-out chat completions
- **+** CPU and GPU Docker images with Compose files
- **−** Last commit April 2026; development has slowed
- **−** README is short; port, env vars and limits live only in the external docs
- **−** TTS limited to Kokoro and Piper models
- **−** Streaming transcription demo is marked TODO in the README

<sub>GPU optional · Docker + Compose · Models: faster-whisper (CTranslate2 Whisper), Kokoro, Piper · [Repo](https://github.com/speaches-ai/speaches) · [📖 Docs ↗](https://speaches.ai/) · [🌐 Site ↗](https://speaches.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speaches/)</sub>

<a name="paddlespeech"></a>
### #&#8288;27 [paddlespeech](https://github.com/paddlepaddle/paddlespeech) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (19) · Freshness: recent (60) · Maintenance: weak (17) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Jun 2026</sub>

**Speech toolkit on PaddlePaddle for ASR, TTS, translation and speaker verification.**

PaddleSpeech is a Python toolkit built on PaddlePaddle that covers speech recognition, text-to-speech, English-to-Chinese speech translation, speaker verification, audio classification and punctuation restoration. It provides a CLI, a Python API, and a server and streaming server (the client example uses port 8090). It includes a rule-based Chinese text frontend and training recipes for datasets such as LibriSpeech, AISHELL and CSMSC.

- **+** One toolkit covers ASR, TTS, speech translation, speaker verification, audio classification and punctuation
- **+** Streaming ASR and TTS servers, plus C++ U2/U2++ streaming ASR deployment
- **+** Rule-based Chinese text normalization and G2P; Cantonese and Chinese-English mixed TTS
- **+** All TTS models support ONNX; CPU install is documented
- **−** Requires PaddlePaddle, a smaller ecosystem than PyTorch
- **−** Speech translation supports only English to Chinese and is documented for Ubuntu only
- **−** Last release was 2025-03-05, though commits continue
- **−** No Docker image or compose file; install is via pip or source build

<sub>GPU optional · Docker · Needs paddlepaddle, python>=3.8, gcc>=4.8.5 · Models: Whisper large v3 and turbo, wav2vec2, HuBERT, WavLM, U2/U2++ conformer · port 8090 · [Repo](https://github.com/paddlepaddle/paddlespeech) · [▶️ Demo ↗](https://huggingface.co/spaces/KPatrick/PaddleSpeechTTS) · [📖 Docs ↗](https://paddlespeech.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddlespeech/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
