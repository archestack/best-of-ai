# 🎙️ Voice reviews · Best of Open-Source AI

Speech-to-text, text-to-speech, voice agents and meeting tools that run locally. Back to the [leaderboard](../README.md#%EF%B8%8F-voice).

<sub>🌐 Also on the web: [Voice on archestack.com](https://archestack.com/best-of-ai/voice/), each project on its own page.</sub>

<a name="voicestudio"></a>
### 🥇 [voicestudio](https://github.com/debpalash/voicestudio) <sub>score [97](../README.md#-how-we-rank "Score 97/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 95k · AGPL-3.0 · Oct 2026</sub>

**Desktop app for voice cloning, dubbing, dictation and audiobooks.**

VoiceStudio is an Electron desktop app with a Python backend for voice cloning, voice design from text descriptions, timed video dubbing, dictation, transcription and audiobook creation. The default engine is k2-fsa/OmniVoice, and other engines can be selected. It also exposes a local API and an MCP server for agents.

- **+** Covers cloning, voice design, dubbing, dictation and audiobooks in one app
- **+** Runs on NVIDIA CUDA, Apple Silicon (MPS) or CPU only
- **+** Local API and MCP server for agent integration
- **+** Installers for macOS, Windows and Linux, plus Docker
- **−** Model weights and voices carry licence terms separate from the AGPL-3.0 app
- **−** CPU-only use is slower; the CPU PyTorch build needs about 5 GB disk
- **−** Intel Mac runs the UI only and needs a remote backend
- **−** Windows on ARM support is experimental and CPU only

<sub>GPU optional · Docker + Compose · Needs Python, PyTorch, Electron · Models: k2-fsa/OmniVoice · [Repo](https://github.com/debpalash/voicestudio) · [📖 Docs ↗](https://github.com/debpalash/VoiceStudio/blob/main/docs/engines/README.md) · [🌐 Site ↗](https://voicestudio.sh/?utm_source=github&utm_medium=readme&utm_campaign=project) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voicestudio/)</sub>

<a name="whisper-cpp"></a>
### 🥈 [whisper.cpp](https://github.com/ggml-org/whisper.cpp) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 55k · MIT · Oct 2026</sub>

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

<a name="handy"></a>
### 🥉 [handy](https://github.com/cjpais/handy) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · MIT · Oct 2026</sub>

**Offline push-to-talk dictation app that pastes transcripts into any text field.**

Handy is a cross-platform desktop app (Rust, Tauri) for local speech-to-text. Hold or toggle a global shortcut, speak, and the transcript is pasted into the focused app. Silero VAD filters silence, and transcription runs locally on Whisper models (Small, Medium, Turbo, Large) or Parakeet, with no audio sent to the cloud.

- **+** Runs fully offline on Windows, macOS and Linux with Whisper or Parakeet models
- **+** Hold-to-talk or toggle shortcuts, plus CLI flags and signals for remote control
- **+** Accepts custom Whisper GGML models and manually downloaded GGUF files
- **+** Release artifacts are signed, with documented minisign verification steps
- **−** Linux Wayland support is limited and needs wtype, dotool or ydotool for text input
- **−** Clipboard paste can insert stale clipboard content; Reliable Paste is still experimental
- **−** fn/Globe key shortcuts work only on Apple keyboards on macOS
- **−** Model downloads are large, from 487 MB to 1.6 GB for Whisper variants

<sub>GPU optional · Needs xdotool (X11), wtype or dotool (Wayland), libgtk-layer-shell (Linux) · Models: Whisper GGML (.bin), Parakeet (GGUF), Silero VAD · [Repo](https://github.com/cjpais/handy) · [🌐 Site ↗](https://handy.computer) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/handy/)</sub>

<a name="xiaozhi-esp32"></a>
### #&#8288;4 [xiaozhi-esp32](https://github.com/78/xiaozhi-esp32) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Oct 2026</sub>

**ESP32 firmware for a voice chatbot with MCP device and cloud tool control.**

C++ firmware that turns ESP32 boards into a voice chatbot. It does offline wake-word detection with ESP-SR and streams Opus audio over WebSocket or MQTT+UDP to a server that handles ASR, LLM and TTS. MCP is used on the device (speaker, LED, servo, GPIO) and in the cloud (smart home, email, search). It connects to the hosted xiaozhi.me server by default, and self-hosted server projects are listed.

- **+** Supports 138 board directories and 171 release variants across ESP32, C3, C5, C6, S3 and P4
- **+** Documented WebSocket and MQTT+UDP protocols let third-party servers and clients interoperate
- **+** Offline wake-word detection with customizable wake words; Wi-Fi, Ethernet and Cat.1 4G networking
- **+** Prebuilt firmware can be flashed without setting up a development environment
- **−** Models do not run on the device; a server is needed for ASR, LLM and TTS
- **−** Default setup depends on the hosted xiaozhi.me service and an account
- **−** Requires ESP-IDF 6.0.1 or later; 5.x is unsupported and the v6.1 tag has a reported C3 Wi-Fi bug
- **−** Beginner tutorials are on Feishu and bilibili, mostly in Chinese

<sub>no GPU · Docker · Needs ESP-IDF 6.0.1+, ESP32 board, xiaozhi.me or compatible server · Models: Qwen, DeepSeek, Realtime end-to-end voice models · [Repo](https://github.com/78/xiaozhi-esp32) · [📖 Docs ↗](https://github.com/78/xiaozhi-esp32/blob/main/docs/custom-board.md) · [🌐 Site ↗](https://xiaozhi.me) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xiaozhi-esp32/)</sub>

<a name="buzz"></a>
### #&#8288;5 [buzz](https://github.com/chidiwilliams/buzz) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Oct 2026</sub>

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

<a name="agents"></a>
### #&#8288;6 [agents](https://github.com/livekit/agents) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

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

<a name="ebook2audiobook"></a>
### #&#8288;7 [ebook2audiobook](https://github.com/drewthomasson/ebook2audiobook) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Oct 2026</sub>

**Converts ebooks to chaptered audiobooks with local TTS and voice cloning.**

Converts ebooks (epub, mobi, pdf, txt and about 20 other formats, with OCR for image pages) into audiobooks with chapters and metadata. It runs local TTS engines such as XTTSv2, Bark, Fairseq, VITS, Tacotron2, Tortoise, GlowTTS and YourTTS, with optional voice cloning. It offers a Gradio web UI and a headless CLI, and outputs m4b, mp3, flac, wav and other formats.

- **+** Supports 1158 languages via Fairseq/MMS models, plus optional voice cloning from a voice file
- **+** Gradio GUI and headless CLI with batch directory mode and per-book voice map
- **+** Runs on CPU, CUDA, ROCm, Apple MPS, Intel XPU and Jetson
- **+** SML tags for pauses and voice switching; Audiobookshelf upload options in the CLI
- **−** README says modern TTS engines are very slow on CPU; lower-quality engines are advised
- **−** EPUB has no standard chapter structure, so unwanted text must be removed manually
- **−** Non-DRM ebooks only; DRM-protected files are not supported
- **−** Docker on Windows requires virtualization enabled

<sub>RAM ≥ 2 GB · GPU optional · Docker + Compose · Needs Docker (optional), Homebrew on macOS (auto-installed), Scoop on Windows (auto-installed) · Models: XTTSv2, Bark, Fairseq, VITS, Tacotron2 · port 7860 · [Repo](https://github.com/drewthomasson/ebook2audiobook) · [▶️ Demo ↗](https://huggingface.co/spaces/drewThomasson/ebook2audiobook) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ebook2audiobook/)</sub>

<a name="pyvideotrans"></a>
### #&#8288;8 [pyvideotrans](https://github.com/jianchang512/pyvideotrans) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · GPL-3.0 · Oct 2026</sub>

**Video translation and AI dubbing pipeline with ASR, subtitle translation and TTS.**

pyVideoTrans translates videos between languages by chaining speech recognition, subtitle translation, speech synthesis and audio-video merging. It runs as a PySide6 desktop GUI, a CLI, or a Gradio WebUI, and works with local models (Faster-Whisper, Ollama, F5-TTS) or online APIs. Pipeline stages can be paused for manual proofreading, and speaker diarization allows different dubbing voices per speaker.

- **+** Full pipeline in one tool: ASR, translation, TTS and video merge
- **+** Mixes local engines (Faster-Whisper, Ollama) with many commercial APIs
- **+** Pause and edit between recognition, translation and dubbing stages
- **+** GUI, CLI for batch jobs, WebUI, and a prebuilt Windows exe
- **−** GPU acceleration is NVIDIA only; AMD needs the Whisper.NET route
- **−** Windows GPU use requires manually installing CUDA 12.8 and cuDNN 9.11
- **−** WebUI is an optional extra and Docker image must be built locally
- **−** GPL-3.0 license; README lists no RAM or VRAM requirements

<sub>GPU optional · Docker · Needs FFmpeg, Python 3.10, uv, CUDA 12.8 and cuDNN 9.11 (NVIDIA GPU only) · Models: Faster-Whisper, WhisperX, OpenAI Whisper, Ollama, DeepSeek · port 7860 · [Repo](https://github.com/jianchang512/pyvideotrans) · [📖 Docs ↗](https://pyvideotrans.com) · [🌐 Site ↗](https://pyvideotrans.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyvideotrans/)</sub>

<a name="sherpa-onnx"></a>
### #&#8288;9 [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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

<a name="meetily"></a>
### #&#8288;10 [meetily](https://github.com/zackriya-solutions/meetily) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Sep 2026</sub>

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
### #&#8288;11 [Speech-to-Speech](https://github.com/huggingface/speech-to-speech) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

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

<a name="index-tts"></a>
### #&#8288;12 [IndexTTS](https://github.com/index-tts/index-tts) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Sep 2026</sub>

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

<a name="speechbrain"></a>
### #&#8288;13 [speechbrain](https://github.com/speechbrain/speechbrain) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Oct 2026</sub>

**PyTorch toolkit for training and running speech and text models.**

SpeechBrain is a PyTorch toolkit with over 200 training recipes on more than 40 datasets, covering ASR, speaker recognition, speech separation and enhancement, TTS, vocoding, diarization and EEG classification. Training is driven by a Python script plus a YAML hyperparameter file, and over 100 pretrained models on HuggingFace load through a short inference API. It targets research and prototyping rather than turnkey deployment.

- **+** Over 200 recipes on 40+ datasets, with a consistent layout across tasks
- **+** Over 100 pretrained models on HuggingFace; ASR inference in three lines of Python
- **+** Single and multi-GPU training, dynamic batching and mixed precision built in
- **+** Over 30 tutorials; Apache-2.0 license permits commercial use
- **−** Library and research toolkit, not a ready-to-run server or app
- **−** No Docker image or HTTP API provided
- **−** Hardware requirements for training recipes are not stated
- **−** Real-time and streaming support is listed only as a future plan

<sub>GPU optional · Needs PyTorch, HuggingFace · Models: Whisper, Wav2Vec2, WavLM, Hubert, GPT2 · [Repo](https://github.com/speechbrain/speechbrain) · [📖 Docs ↗](https://speechbrain.readthedocs.io/en/latest/index.html) · [🌐 Site ↗](https://speechbrain.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speechbrain/)</sub>

<a name="whisperlivekit"></a>
### #&#8288;14 [whisperlivekit](https://github.com/quentinfuxa/whisperlivekit) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**Real-time streaming speech-to-text server with diarization and translation.**

WhisperLiveKit is a Python server that transcribes microphone or browser audio in real time using simultaneous-decoding policies (SimulStreaming, LocalAgreement) instead of re-running Whisper on fixed chunks. It exposes a native WebSocket at /asr, an OpenAI-compatible transcription endpoint and a Deepgram-compatible WebSocket, and ships a web UI and a Chrome extension. Backends include Whisper, MLX Whisper, Voxtral, Qwen3-ASR, Canary and FunASR SenseVoice.

- **+** Serves OpenAI-style /v1/audio/transcriptions, Deepgram-style WebSocket and native /asr WebSocket
- **+** Many backends: Whisper, MLX Whisper, Voxtral, Qwen3-ASR, Canary, SenseVoiceSmall
- **+** Optional Sortformer speaker diarization and translation to and from 200 languages
- **+** One shared engine serves multiple concurrent sessions with per-session language
- **−** Heavy extras (voxtral-hf, vLLM stacks) conflict and need separate environments
- **−** Qwen3 causal mode is English-only; vLLM causal and Metal paths are experimental
- **−** Qwen3 streaming plans one realtime session per GPU and needs an explicit language
- **−** Canary on CPU is slow; GPU strongly recommended for larger backends

<sub>GPU optional · Docker + Compose · Needs PyTorch, NeMo (diarization, Canary), vLLM (optional Qwen3 backend) · Models: Whisper, MLX Whisper, Voxtral Mini, Qwen3-ASR, Canary-1b-v2 · port 8000 · [Repo](https://github.com/quentinfuxa/whisperlivekit) · [📖 Docs ↗](https://github.com/QuentinFuxa/WhisperLiveKit/blob/main/docs/API.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisperlivekit/)</sub>

<a name="voicebox"></a>
### #&#8288;15 [Voicebox](https://github.com/jamiepine/voicebox) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (92) · Freshness: active (99) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker + Compose · Models: Qwen3-TTS 0.6B/1.7B, Qwen CustomVoice, Qwen VoiceDesign, LuxTTS, Chatterbox Multilingual · port 17493 · README: alternative to ElevenLabs, Wispr Flow · [Repo](https://github.com/jamiepine/voicebox) · [📖 Docs ↗](https://docs.voicebox.sh) · [🌐 Site ↗](https://voicebox.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voicebox/)</sub>

<a name="funasr"></a>
### #&#8288;16 [funasr](https://github.com/modelscope/funasr) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Oct 2026</sub>

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

<a name="openwhispr"></a>
### #&#8288;17 [openwhispr](https://github.com/openwhispr/openwhispr) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

**Cross-platform voice dictation and meeting transcription app with local or cloud models.**

OpenWhispr is an Electron desktop app for macOS, Windows and Linux. A global hotkey records speech and pastes the transcript at the cursor, using local models (Whisper via whisper.cpp, NVIDIA Parakeet via sherpa-onnx) or cloud providers. It also covers meeting transcription with speaker diarization, notes with semantic search, and a voice assistant that talks to GPT, Claude, Gemini or local models.

- **+** Offline transcription with Whisper and Parakeet; audio stays on the device
- **+** GPU-accelerated local Whisper on Metal, CUDA and Vulkan
- **+** Local speaker diarization and voice fingerprinting across meetings
- **+** Public API and MCP server for notes and transcriptions
- **−** Intel Macs lack live speaker identification and semantic notes search
- **−** Cloud sync, sharing and team spaces depend on OpenWhispr Cloud
- **−** Source setup requires Node.js 24+; no Docker or server deployment
- **−** Enterprise SSO and SCIM controls are listed, with no edition details in the README

<sub>GPU optional · Needs Node.js 24+ · Models: Whisper, NVIDIA Parakeet, Cohere Transcribe, llama.cpp local LLMs, OpenAI · README: alternative to Granola, Wispr Flow · [Repo](https://github.com/openwhispr/openwhispr) · [📖 Docs ↗](https://docs.openwhispr.com) · [🌐 Site ↗](https://openwhispr.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openwhispr/)</sub>

<a name="pocket-tts"></a>
### #&#8288;18 [Pocket TTS](https://github.com/kyutai-labs/pocket-tts) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

**CPU-only text-to-speech model with voice cloning and streaming output.**

Pocket TTS is a roughly 100M-parameter text-to-speech model from Kyutai that runs on CPU using about 2 cores, with a Python API, a CLI and a local HTTP server with a web UI. It streams audio with about 200ms to first chunk, clones voices from a wav file, and supports English, French, German, Portuguese, Italian, Spanish and Dutch. Small English variants (18.2M, 6.9M, 1.9M parameters) and training code are also published.

- **+** Runs on CPU with 2 cores; about 6x real time on a MacBook Air M4
- **+** Voice cloning from a wav file, with export to fast-loading safetensors
- **+** Standalone Rust binaries for Linux, macOS and Windows need no Python or PyTorch
- **+** Training code released, plus 1.9M to 18.2M parameter English models
- **−** GPU is not officially supported; serve and the Docker image always run on CPU
- **−** No way to insert silence or pauses in the input text
- **−** Linux pip install pulls CUDA PyTorch (about 3 GB) unless the CPU index is set
- **−** Rust binary is CPU-only and cannot load training checkpoints

<sub>GPU optional · Docker + Compose · Needs PyTorch 2.5+, Python 3.10-3.14, Hugging Face (model and voice downloads) · Models: Pocket TTS 100M, english_18m_2026-10, english_7m_2026-10, english_2m_2026-10, community models via --config · port 8000 · [Repo](https://github.com/kyutai-labs/pocket-tts) · [▶️ Demo ↗](https://kyutai.org/pocket-tts) · [📖 Docs ↗](https://kyutai-labs.github.io/pocket-tts/) · [🌐 Site ↗](https://kyutai.org/pocket-tts) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pocket-tts/)</sub>

<a name="moonshine"></a>
### #&#8288;19 [moonshine](https://github.com/moonshine-ai/moonshine) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Aug 2026</sub>

**On-device speech-to-text and voice agent toolkit with streaming models.**

Moonshine Voice is a C++ library with bindings for Python, JavaScript/WASM, iOS, Android, macOS, Linux, Windows and Raspberry Pi. It runs streaming speech-to-text models trained by the project, from tiny 1MB models up to ones the README says beat Whisper Large V3 on the Open ASR leaderboard. It also covers text to speech and conversational agents, all on-device without accounts or API keys.

- **+** Runs fully on-device, no account or API keys required
- **+** One library across Python, WASM, mobile, desktop and Raspberry Pi
- **+** Streaming design does work while the user is still speaking
- **+** Model sizes range from about 1MB up to Whisper Large V3-class accuracy
- **−** Legacy non-English non-streaming models use a non-commercial community license
- **−** Repo license detected as NOASSERTION although README states MIT
- **−** RAM and latency figures are not stated in the README
- **−** No Docker image or live demo link in the README

<sub>no GPU · Models: Moonshine speech-to-text models, Moonshine tiny 1MB models · [Repo](https://github.com/moonshine-ai/moonshine) · [📖 Docs ↗](https://moonshine-voice.readthedocs.io/) · [🌐 Site ↗](https://moonshine.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moonshine/)</sub>

<a name="realtimestt"></a>
### #&#8288;20 [realtimestt](https://github.com/koljab/realtimestt) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

**Python speech-to-text library with VAD, wake words and realtime transcription.**

RealtimeSTT is a Python library that detects speech with WebRTC and Silero VAD and transcribes it, from a microphone or from audio chunks you feed in. The default engine is faster-whisper; sherpa-onnx, Kroko-ONNX, Moonshine, whisper.cpp, Parakeet NeMo and others are install extras. It also ships a FastAPI production server with HTTP and WebSocket endpoints and bearer-token auth.

- **+** Many selectable engines: faster-whisper, sherpa-onnx, Kroko-ONNX, Moonshine, whisper.cpp, Parakeet NeMo
- **+** Documented CPU INT8 streaming profile: Nemotron for live text, Parakeet for the final transcript
- **+** Optional wake words via Porcupine or OpenWakeWord, plus callbacks for VAD and recording events
- **+** Packaged server binds to loopback by default; non-loopback needs bearer token and TLS
- **−** CI covers only Python 3.11 and 3.12; 3.13 and newer are not release targets
- **−** Uses multiprocessing, so scripts need a __main__ guard, especially on Windows
- **−** Linux needs PortAudio headers installed before the pip install
- **−** CPU streaming recommendation is stated only for Linux x86-64

<sub>GPU optional · Docker + Compose · Needs PortAudio, Python 3.11 or 3.12, Porcupine or OpenWakeWord (optional, for wake words) · Models: faster-whisper, sherpa-onnx, Kroko-ONNX, Moonshine, whisper.cpp · port 8010 · [Repo](https://github.com/koljab/realtimestt) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/realtimestt/)</sub>

<a name="edge-tts"></a>
### #&#8288;21 [edge-tts](https://github.com/rany2/edge-tts) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · custom license · Oct 2026</sub>

**Python module and CLI for Microsoft Edge's online text-to-speech service.**

edge-tts calls Microsoft Edge's online text-to-speech service from Python code or through the `edge-tts` and `edge-playback` commands. It writes audio and optional SRT subtitles, lets you pick a voice with `--list-voices` and `--voice`, and adjusts rate, volume and pitch. Synthesis runs on Microsoft's servers, so it needs network access and is not a local model.

- **+** Installs with pip or pipx; the README mentions no API key
- **+** Writes audio and SRT subtitles in a single command
- **+** Many voices across languages, listed with --list-voices
- **+** Usable as a Python module; used by hass-edge-tts and Podcastfy
- **−** Depends on Microsoft's online service; not offline or local
- **−** Custom SSML removed; service allows only one voice and prosody tag
- **−** edge-playback needs the mpv player except on Windows
- **−** License is reported as NOASSERTION, so terms need checking

<sub>no GPU · Needs Microsoft Edge online TTS service, mpv (edge-playback, non-Windows) · Models: Microsoft Edge neural voices (hosted) · [Repo](https://github.com/rany2/edge-tts) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/edge-tts/)</sub>

<a name="vibevoice"></a>
### #&#8288;22 [vibevoice](https://github.com/microsoft/vibevoice) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 55k · MIT · Oct 2026</sub>

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

<a name="voxcpm"></a>
### #&#8288;23 [voxcpm](https://github.com/openbmb/voxcpm) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: patchy (35) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Oct 2026</sub>

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

<a name="vibe"></a>
### #&#8288;24 [vibe](https://github.com/thewh1teagle/vibe) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · MIT · Oct 2026</sub>

**Desktop app that transcribes audio and video offline with Whisper models.**

Vibe is a Tauri desktop app for macOS, Windows and Linux that transcribes audio and video locally using Whisper, Nemotron 3.5 or Parakeet TDT v3. It supports batch files, microphone and system audio, speaker diarization, and export to SRT, VTT, TXT, HTML, PDF, JSON and DOCX. Summaries can be made through the Claude API or a local Ollama instance.

- **+** Runs transcription fully offline; no audio leaves the device
- **+** GPU acceleration via Vulkan or CoreML on Nvidia, AMD, Intel and Apple
- **+** Exports seven formats including SRT, VTT, DOCX and PDF
- **+** Includes a CLI and an HTTP API with Swagger docs
- **−** Pull requests are limited to a few collaborators
- **−** Cloud summaries need the Claude API; local ones need a separate Ollama install
- **−** Stable timestamps mode is slower because it uses VAD
- **−** RAM and VRAM requirements are not documented in the README

<sub>GPU optional · Needs Ollama (optional), Claude API (optional) · Models: Whisper, Nemotron 3.5, Parakeet TDT v3 · [Repo](https://github.com/thewh1teagle/vibe) · [📖 Docs ↗](https://github.com/thewh1teagle/vibe/tree/main/docs) · [🌐 Site ↗](https://thewh1teagle.github.io/vibe/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vibe/)</sub>

<a name="faster-whisper"></a>
### #&#8288;25 [faster-whisper](https://github.com/systran/faster-whisper) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (74) · Freshness: active (85) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

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

<a name="rtranslator"></a>
### #&#8288;26 [rtranslator](https://github.com/niedev/rtranslator) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (38) · Freshness: active (94) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**Offline real-time speech translator for Android using on-device Whisper and NLLB.**

RTranslator is an Android app that translates speech and text on the phone using Whisper for speech recognition and NLLB for translation, both converted to ONNX and int8-quantized. Conversation mode links phones over Bluetooth LE, with Bluetooth headset support, and WalkieTalkie mode handles two languages on a single phone. Text-to-speech uses the system TTS engine. The 3.0 beta replaces NLLB with Bergamot, Madlad 400 3B or HY-MT 1.5 1.8B.

- **+** Runs speech recognition and translation on the phone, usable offline with no server
- **+** Conversation mode supports more than two phones and Bluetooth headsets
- **+** WalkieTalkie mode works with one phone and detects which of two languages is spoken
- **+** Models are ONNX int8 with KV cache; NLLB uses 1.3 GB RAM versus 2.5 GB baseline
- **−** Needs at least 6 GB RAM and a fast CPU; weaker phones may crash
- **−** First launch downloads 1.2 GB of models from GitHub, slow in some regions
- **−** Android only; README lists Bluetooth connection drops as a known bug
- **−** NLLB is non-commercial licensed and Google ML Kit is closed source in the 2.x README

<sub>RAM ≥ 6 GB · no GPU · Needs Android system TTS (Google TTS recommended), ONNX Runtime, Bluetooth LE · Models: Whisper-Small-244M (ONNX int8), NLLB-Distilled-600M (ONNX int8), Mozilla Bergamot (3.0 beta), Madlad 400 3B (3.0 beta), HY-MT 1.5 1.8B (3.0 beta) · [Repo](https://github.com/niedev/rtranslator) · [📖 Docs ↗](https://github.com/niedev/RTranslator/blob/v2.00/Sideloading.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rtranslator/)</sub>

<a name="kokoro-fastapi"></a>
### #&#8288;27 [Kokoro-FastAPI](https://github.com/remsky/kokoro-fastapi) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Oct 2026</sub>

**OpenAI-compatible text-to-speech server for the Kokoro-82M model.**

FastAPI wrapper around the Kokoro-82M TTS model that exposes an OpenAI-style /v1/audio/speech endpoint with streaming and six output formats. It supports voice mixing with weights, inline multi-speaker tags, pause and rate tokens, SSML, and per-word timestamped captions. Prebuilt images exist for CPU, NVIDIA CUDA and experimental AMD ROCm, and an optional web UI is served at /web.

- **+** Drop-in for OpenAI speech clients: set base_url to localhost:8880/v1
- **+** Weighted voice mixing, aliases and inline [voice:] tags for multi-speaker audio
- **+** Streams audio; README cites ~300ms first-token latency on GPU
- **+** Prebuilt CPU and CUDA images for amd64 and arm64, with models baked in
- **−** ROCm image is experimental and amd64 only
- **−** Apple Silicon GPU (MPS) works only via uv scripts, not Docker
- **−** Smaller chunks for low latency can add intonation artifacts
- **−** Voice tuning from a reference clip is English-only and off by default

<sub>GPU optional · Docker + Compose · Needs Docker, uv, espeak-ng · Models: Kokoro-82M · port 8880 · [Repo](https://github.com/remsky/kokoro-fastapi) · [▶️ Demo ↗](https://huggingface.co/spaces/Remsky/FastKoko) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kokoro-fastapi/)</sub>

<a name="fish-speech"></a>
### #&#8288;28 [fish-speech](https://github.com/fishaudio/fish-speech) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: widely used (80) · Freshness: recent (72) · Maintenance: fair (62) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · custom license · Oct 2026</sub>

**Expressive multi-speaker text-to-speech models with voice cloning.**

Fish Speech is the code and weights for Fish Audio's TTS models: Drama 3 (35B-A3B, 3B active per token) and S2-Pro (4B parameters). Both clone voices from reference audio, accept inline tags such as [whisper] and [angry], and share one command line and API server. Drama 3 adds infilling and multi-turn revision of earlier takes.

- **+** Voice cloning from 10-30 seconds of reference audio (S2-Pro)
- **+** Inline tags like [whisper], [excited], [laughing] control emotion and prosody
- **+** Drama 3 can replace single words in audio and revise earlier takes
- **+** S2-Pro reports RTF 0.195 and about 100 ms to first audio on one H200
- **−** Custom Fish Audio community license; S2-Pro weights under a separate research license
- **−** Drama 3 is 35B total parameters; hardware requirements are not stated in the README
- **−** Last tagged release is 2025-05-31, older than the current models
- **−** README recommends SGLang-Omni or vLLM-Omni for efficient serving

<sub>Docker + Compose · Needs PyTorch, Hugging Face model weights · Models: Drama 3 (35B-A3B), S2-Pro (4B) · [Repo](https://github.com/fishaudio/fish-speech) · [▶️ Demo ↗](https://fish.audio/) · [📖 Docs ↗](https://speech.fish.audio/install/) · [🌐 Site ↗](https://fish.audio/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fish-speech/)</sub>

<a name="mlx-audio"></a>
### #&#8288;29 [mlx-audio](https://github.com/blaizzy/mlx-audio) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · MIT · Oct 2026</sub>

**Python library for TTS, STT and speech models on Apple Silicon via MLX.**

MLX-Audio runs text-to-speech, speech-to-text, speech-to-speech, voice activity detection/diarization and music generation models on Apple Silicon using Apple's MLX framework. It offers a CLI, a Python API, an OpenAI-compatible REST API with a web interface, and a Swift package for iOS/macOS. Quantization from 3-bit to 8-bit is supported, and the README lists dozens of models such as Kokoro, Qwen3-TTS, Whisper and Parakeet.

- **+** Covers TTS, STT, diarization, enhancement and music generation in one library
- **+** Quantized models (3-bit to 8-bit) for Apple Silicon, with many mlx-community weights
- **+** CLI, Python API, OpenAI-compatible REST server and Swift package
- **+** Supports voice cloning and streaming output on several models
- **−** Apple Silicon only, since it is built on MLX
- **−** Some listed models are large (e.g. 35B MoE, 8B), so memory needs vary widely
- **−** Server and web UI need the extra [server] install; no Docker provided
- **−** README does not give RAM requirements or web port

<sub>GPU required · Needs Apple MLX, Hugging Face model weights · Models: Kokoro, Qwen3-TTS, Whisper, Parakeet, Chatterbox · [Repo](https://github.com/blaizzy/mlx-audio) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlx-audio/)</sub>

<a name="voiceink"></a>
### #&#8288;30 [voiceink](https://github.com/beingpax/voiceink) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · custom license · Oct 2026</sub>

**Native macOS dictation app using local speech-to-text models.**

VoiceInk is a Swift macOS app that transcribes speech to text on-device using whisper.cpp, Parakeet via FluidAudio, and GGUF models through transcribe.cpp. It adds global push-to-talk shortcuts, a personal dictionary, and per-app modes that switch settings by the active app or URL. A built-in voice assistant mode is also included.

- **+** Offline transcription; README states audio never leaves the device
- **+** Supports whisper.cpp, Parakeet and GGUF local models, plus SenseVoice Small
- **+** Per-app modes apply settings automatically by app or URL
- **+** Installable via Homebrew cask or buildable from source with BUILDING.md
- **−** macOS 15.0 or later only; no Windows or Linux builds
- **−** Not accepting pull requests; contributions limited to issues
- **−** Auto-updates and priority support only in the paid compiled build
- **−** Context-aware and assistant features: README does not say which AI providers they use

<sub>Needs macOS 15.0+ · Models: whisper.cpp (Whisper), Parakeet (FluidAudio), GGUF via transcribe.cpp, SenseVoice Small · [Repo](https://github.com/beingpax/voiceink) · [🌐 Site ↗](https://tryvoiceink.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voiceink/)</sub>

<a name="dograh"></a>
### #&#8288;31 [dograh](https://github.com/dograh-hq/dograh) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · BSD-2-Clause · Oct 2026</sub>

**Visual builder for voice agents with telephony, a Vapi and Retell alternative.**

Dograh is a self-hostable platform for building inbound and outbound voice agents in a visual workflow editor, with a browser Test Audio and Test Chat panel. It integrates telephony providers such as Twilio, Vonage, Telnyx, Plivo and Asterisk ARI, and accepts your own LLM, TTS and STT providers. It also ships an MCP server so coding agents can create and edit workflows.

- **+** Built-in telephony: Twilio, Vonage, Telnyx, Plivo, Vobiz, Cloudonix, Asterisk ARI
- **+** Bring your own LLM, TTS, STT, or use the bundled stack with no keys
- **+** MCP server lets coding agents create and edit workflows
- **+** Python and Node SDKs for agent creation and outbound calls
- **−** Quickstart opens a public trycloudflare.com tunnel by default
- **−** Anonymous telemetry is on by default; opt out via ENABLE_TELEMETRY=false
- **−** Signup is enabled by default and must be closed through .env
- **−** RAM and hardware requirements are not stated in the README

<sub>Compose · Needs Docker Compose, MinIO or S3-compatible storage, Telephony provider (optional) · Models: Any LLM, TTS and STT provider, Bundled Dograh LLM/TTS/STT stack · port 3010 · [Repo](https://github.com/dograh-hq/dograh) · [▶️ Demo ↗](https://app.dograh.com) · [📖 Docs ↗](https://docs.dograh.com) · [🌐 Site ↗](https://www.dograh.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dograh/)</sub>

<a name="openreader"></a>
### #&#8288;32 [OpenReader](https://github.com/richardr1126/openreader) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 551 · MIT · Oct 2026</sub>

**Text-to-speech reader for EPUB, PDF, TXT, MD and DOCX with read-along highlighting.**

OpenReader is a Next.js document reader that narrates EPUB, PDF, TXT, MD and DOCX files with synchronized read-along highlighting. It supports local Kokoro, self-hosted OpenAI-compatible TTS servers and cloud APIs, and exports audiobooks as M4B or MP3. It runs as a self-hosted web app or as a desktop app for macOS, Windows and Linux.

- **+** Word-by-word highlighting via ONNX Whisper alignment; layout-aware PDF parsing with PP-DocLayoutV3
- **+** Many TTS backends: local Kokoro, Kokoro-FastAPI, Orpheus-FastAPI, OpenAI, Replicate, DeepInfra, ElevenLabs
- **+** Audiobook export to M4B or MP3 from the cached playback audio
- **+** Desktop installers need no server, Docker or account; self-host supports SQLite or Postgres
- **−** Full self-host stack involves a compute worker on NATS JetStream and S3-compatible storage
- **−** Available languages depend on the chosen TTS provider and voice
- **−** Native iPhone, iPad and Mac app is a separate TestFlight build
- **−** RAM and GPU requirements are not stated in the README

<sub>GPU optional · Docker · Needs NATS JetStream, SeaweedFS or S3-compatible storage, SQLite or Postgres · Models: Kokoro, KittenTTS, Orpheus, Supertonic, OpenAI TTS · [Repo](https://github.com/richardr1126/openreader) · [📖 Docs ↗](https://docs.openreader.richardr.dev/) · [🌐 Site ↗](https://openreader.richardr.dev/download) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openreader/)</sub>

<a name="gpt-sovits"></a>
### #&#8288;33 [GPT-SoVITS](https://github.com/rvc-boss/gpt-sovits) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: widely used (94) · Freshness: recent (72) · Maintenance: patchy (35) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · MIT · Oct 2026</sub>

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

<a name="retrieval-based-voice-conversion-webui"></a>
### #&#8288;34 [retrieval-based-voice-conversion-webui](https://github.com/rvc-project/retrieval-based-voice-conversion-webui) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · MIT · Aug 2026</sub>

**Web UI for training and running retrieval-based voice conversion models.**

Gradio web UI for training RVC voice models and converting speech or singing to a target voice. It replaces input features with top-1 retrieved training-set features to reduce timbre leakage, and uses RMVPE for pitch extraction. It includes a real-time voice changer GUI, vocal/accompaniment separation via pymss/MSST, and checkpoint merging. The README recommends at least 10 minutes of clean voice data.

- **+** Trains usable models from about 10 minutes of low-noise audio, per the README
- **+** Separate real-time GUI: 170 ms end-to-end latency, 90 ms with ASIO devices
- **+** Includes vocal separation (pymss/MSST) and ckpt-merge in the same tool
- **+** CPU, DirectML (Windows) and CUDA 11.8/12.8 install paths
- **−** Manual setup: Python 3.12 venv, separate Torch install, and several model downloads
- **−** No Docker or compose files in the repo
- **−** Main README is in Chinese; English docs live in docs/en
- **−** Low latency depends on ASIO hardware drivers; RVCv3 base models are not released yet

<sub>GPU optional · Needs Python 3.12, PyTorch, FFmpeg, Gradio, Hugging Face model weights (hubert_base, rmvpe, pretrained) · Models: RVC v1/v2 .pth, RMVPE, HuBERT/ContentVec, FAISS .index, pymss/MSST · port 7865 · [Repo](https://github.com/rvc-project/retrieval-based-voice-conversion-webui) · [▶️ Demo ↗](https://modelscope.cn/studios/FlowerCry/RVCv2demo) · [📖 Docs ↗](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI/wiki/%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98%E8%A7%A3%E7%AD%94) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/retrieval-based-voice-conversion-webui/)</sub>

<a name="whisperx"></a>
### #&#8288;35 [whisperx](https://github.com/m-bain/whisperx) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: weak (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · BSD-2-Clause · Oct 2026</sub>

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

<a name="speakr"></a>
### #&#8288;36 [Speakr](https://github.com/murtaza-nasir/speakr) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · AGPL-3.0 · Oct 2026</sub>

**Self-hosted transcription with speaker labels, summaries and chat over recordings.**

Speakr is a Flask and Vue web app that records or imports audio, transcribes it through a configurable ASR backend (WhisperX, OpenAI, Mistral Voxtral, AssemblyAI and others), and generates summaries, action items and events with an LLM. It adds per-recording chat, semantic search across the library, multi-user OIDC login, sharing, retention policies and a REST API with webhooks. Storage is SQLite by default or PostgreSQL.

- **+** Many ASR connectors, auto-detected from config, including self-hosted WhisperX and VibeVoice
- **+** Speaker diarization, plus cross-recording voice profiles with the WhisperX backend
- **+** Multi-user with OIDC SSO, groups, sharing, per-user quotas and retention policies
- **+** REST API with Swagger, signed webhooks, watched import folder and templated auto-export
- **−** Voice profiles and top-quality diarization need a separate WhisperX container with a GPU
- **−** Summaries and chat need an external LLM endpoint, cloud or local
- **−** Lite image replaces Inquire semantic search with basic text search
- **−** Versioned 0.10.x alpha; MOSI and other cloud connectors send audio to third parties

<sub>GPU optional · Docker · Needs OpenAI-compatible LLM endpoint (OpenRouter, OpenAI or local), ASR backend (WhisperX service or cloud API), SQLite or PostgreSQL · Models: WhisperX, OpenAI Whisper and gpt-4o-transcribe-diarize, Mistral Voxtral, AssemblyAI, VibeVoice ASR · port 8899 · [Repo](https://github.com/murtaza-nasir/speakr) · [📖 Docs ↗](https://murtaza-nasir.github.io/speakr/getting-started) · [🌐 Site ↗](https://murtaza-nasir.github.io/speakr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speakr/)</sub>

<a name="kittentts"></a>
### #&#8288;37 [kittentts](https://github.com/kittenml/kittentts) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (60) · Freshness: active (94) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Oct 2026</sub>

**Text-to-speech library with voice cloning and CPU-capable models.**

Python library for text-to-speech. The main model, KittenTTS 2 (1.7B parameters), has 47 built-in voices, 20 languages, voice cloning from 5-30 seconds of audio, and emotion tags. It also ships 15M-80M parameter ONNX models that run on CPU. Backends include a llama.cpp fork, MLX on Apple silicon, and vLLM on NVIDIA GPUs.

- **+** Voice cloning from a 5-30 second clip, no fine-tuning
- **+** Small ONNX models (25-80 MB) run on CPU without a GPU
- **+** Backends for CPU (GGUF/C++), Apple MLX and vLLM CUDA
- **+** Docs describe a Docker setup with an OpenAI-compatible speech API
- **−** KittenTTS 2 weights use the Stellon Labs Community License, not Apache-2.0
- **−** Streaming is chunk-level; first audio arrives after a real delay
- **−** Expression control and the C++ CPU backend are marked beta
- **−** KittenTTS 2 needs about 8 GB GPU memory or 6 GB RAM

<sub>RAM ≥ 6 GB · GPU optional · Needs Python 3.9+, ONNX runtime, Whisper (auto-transcribes cloning reference) · Models: KittenTTS 2 (1.7B), kitten-tts-mini 80M ONNX, kitten-tts-micro 40M ONNX, kitten-tts-nano 15M ONNX, GGUF (C++ backend) · [Repo](https://github.com/kittenml/kittentts) · [▶️ Demo ↗](https://huggingface.co/spaces/KittenML/KittenTTS-Demo) · [📖 Docs ↗](https://github.com/KittenML/KittenTTS/blob/main/docs/api.md) · [🌐 Site ↗](https://kittenml.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kittentts/)</sub>

<a name="argmax-oss-swift"></a>
### #&#8288;38 [argmax-oss-swift](https://github.com/argmaxinc/argmax-oss-swift) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · MIT · Oct 2026</sub>

**Swift SDK for on-device speech-to-text, diarization and TTS on Apple devices.**

Swift package with three Core ML libraries: WhisperKit for Whisper transcription, SpeakerKit for Pyannote speaker diarization, and TTSKit for Qwen3-TTS speech synthesis. It also ships a CLI and an optional local server that implements the OpenAI Audio API transcription and translation endpoints. Real-time transcription with speakers and Android support are in the separate Pro SDK.

- **+** Runs Whisper, Pyannote and Qwen3-TTS on-device via Core ML, no server required
- **+** Local server exposes /v1/audio/transcriptions and /v1/audio/translations for OpenAI SDK clients
- **+** Incremental loading streams long audio from disk in bounded memory using VAD chunking
- **+** whisperkittools converts and publishes your own fine-tuned Whisper models in Core ML
- **−** Apple platforms only: macOS 14+ and Xcode 16+; TTSKit needs macOS 15 or iOS 18
- **−** Local server supports only json and verbose_json, no SRT, VTT or plain text
- **−** Server needs a BUILD_ALL=1 build and one model chosen at launch with --model
- **−** Real-time transcription with speakers and custom vocabulary are Pro SDK only

<sub>Needs Xcode 16+, macOS 14+, git-lfs (CLI model download) · Models: OpenAI Whisper (Core ML), Pyannote, Qwen3-TTS 0.6B and 1.7B · port 50060 · [Repo](https://github.com/argmaxinc/argmax-oss-swift) · [📖 Docs ↗](https://swiftpackageindex.com/argmaxinc/argmax-oss-swift) · [🌐 Site ↗](https://argmaxinc.com/blog) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/argmax-oss-swift/)</sub>

<a name="f5-tts"></a>
### #&#8288;39 [F5-TTS](https://github.com/swivid/f5-tts) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

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

<a name="sensevoice"></a>
### #&#8288;40 [sensevoice](https://github.com/qwenaudio/sensevoice) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: known (32) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · MIT · Sep 2026</sub>

**Multilingual speech recognition model with emotion and audio-event tags.**

SenseVoice is a speech model that does ASR, spoken language ID, speech emotion recognition and audio event detection in one non-autoregressive model. The released SenseVoiceSmall checkpoint covers Mandarin, Cantonese, English, Japanese and Korean. It runs through FunASR in Python, as ONNX or Libtorch exports, as a FastAPI service, or as a GGUF binary on CPU.

- **+** One model outputs transcript, language ID, emotion tag and audio-event tag
- **+** README reports over 5x faster than Whisper-Small in its benchmark setup
- **+** Multiple runtimes: FunASR Python, ONNX, Libtorch, FastAPI, and a GGUF binary without Python
- **+** Includes finetuning scripts and a bounded-memory long-audio script that needs no VAD
- **−** Released checkpoint supports only 5 languages, not the 50+ cited for the research work
- **−** Speaker diarization needs separate FSMN-VAD and CAM++ models; accuracy not validated
- **−** Direct inference limited to 30 seconds; longer audio needs VAD or windowing
- **−** Event detection is weaker than specialized AED models, per the README

<sub>GPU optional · Docker + Compose · Needs funasr, ffmpeg, FSMN-VAD, CAM++ (diarization only) · Models: SenseVoiceSmall, ONNX, Libtorch, GGUF · port 50000 · [Repo](https://github.com/qwenaudio/sensevoice) · [▶️ Demo ↗](https://huggingface.co/spaces/FunAudioLLM/SenseVoice) · [📖 Docs ↗](https://github.com/modelscope/FunASR/blob/main/docs/tutorial/README.md) · [🌐 Site ↗](https://www.funasr.com/en/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sensevoice/)</sub>

<a name="whisper"></a>
### #&#8288;41 [whisper](https://github.com/openai/whisper) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: widely used (99) · Freshness: recent (74) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 112k · MIT · Aug 2026</sub>

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

<a name="funclip"></a>
### #&#8288;42 [funclip](https://github.com/modelscope/funclip) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Oct 2026</sub>

**Clip videos by selecting text or speakers from an ASR transcript.**

FunClip runs FunASR Paraformer speech recognition on a video, then lets you pick transcript segments or speaker IDs and cuts the matching clips, with SRT subtitles for the full video and the clip. It runs as a local Gradio app on port 7860, with a command-line mode and optional LLM-assisted segment selection. Backends include Paraformer, Fun-ASR-Nano, SenseVoice and a MOSS vLLM path.

- **+** Paraformer gives token-level timestamps, so clips cut precisely on selected text
- **+** CAM++ speaker recognition allows clipping all segments from one speaker
- **+** Gradio UI plus a two-stage CLI (recognize, then clip) for scripting
- **+** Optional LLM clipping via OpenAI-compatible gateways or TwelveLabs Pegasus video model
- **−** Default models are tuned for Chinese; English uses a separate Paraformer model via -l en
- **−** MOSS backend has only segment-level timestamps and needs a separate vLLM service
- **−** No Docker setup in the repo; Python environment and PyTorch must be installed manually
- **−** Reverse period selection and silence removal are still unchecked on the roadmap

<sub>GPU optional · Needs Python 3.12, PyTorch and torchaudio, funasr>=1.4.9, Gradio 4, Pillow, vLLM (MOSS backend only) · Models: Paraformer-Large, SeACo-Paraformer, CAM++, Fun-ASR-Nano, SenseVoice · port 7860 · [Repo](https://github.com/modelscope/funclip) · [▶️ Demo ↗](https://huggingface.co/spaces/FunAudioLLM/FunClip) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/funclip/)</sub>

<a name="whisperlive"></a>
### #&#8288;43 [WhisperLive](https://github.com/collabora/whisperlive) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Oct 2026</sub>

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

<a name="omnivoice"></a>
### #&#8288;44 [omnivoice](https://github.com/k2-fsa/omnivoice) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Aug 2026</sub>

**Multilingual zero-shot text-to-speech model with voice cloning and voice design.**

OmniVoice is a diffusion language model-style TTS model covering 600+ languages. It clones a voice from a 3–10 second reference clip, or builds one from attributes such as gender, age, pitch and accent. It ships a Python API, three CLIs (Gradio demo, single and multi-GPU batch inference) and training recipes.

- **+** Covers 600+ languages, with a full list in the docs
- **+** Reported RTF of 0.025; FlashInfer path reaches 0.0115 at batch 8 on H100
- **+** Supports CUDA, Apple Silicon (mps) and Intel Arc (xpu) backends
- **+** Inline tags for non-verbal sounds and pinyin or CMU phoneme pronunciation fixes
- **−** Voice design trained on Chinese and English only; other languages may be unstable
- **−** Cross-lingual cloning carries the reference audio's accent
- **−** No Docker image or compose file; installed via pip or uv
- **−** FlashInfer speedup is NVIDIA-only; flash_attn unavailable on XPU

<sub>GPU optional · Needs PyTorch, torchaudio, Whisper (auto-transcribes reference audio), FlashInfer (optional) · Models: k2-fsa/OmniVoice (Hugging Face) · port 8001 · [Repo](https://github.com/k2-fsa/omnivoice) · [▶️ Demo ↗](https://huggingface.co/spaces/k2-fsa/OmniVoice) · [🌐 Site ↗](https://zhu-han.github.io/omnivoice) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/omnivoice/)</sub>

<a name="chattts"></a>
### #&#8288;45 [chattts](https://github.com/2noise/chattts) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: widely used (86) · Freshness: recent (69) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · AGPL-3.0 · Apr 2026</sub>

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

<a name="cosyvoice"></a>
### #&#8288;46 [cosyvoice](https://github.com/qwenaudio/cosyvoice) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (70) · Freshness: recent (75) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · May 2026</sub>

**Zero-shot multilingual text-to-speech with voice cloning and streaming output.**

CosyVoice is an LLM-based text-to-speech system from the FunAudioLLM team. Fun-CosyVoice 3.0 (0.5B) clones voices zero-shot across 9 languages and 18+ Chinese dialects, and supports text-in and audio-out streaming with latency as low as 150ms. The repo includes inference and training scripts, a web demo, gRPC and FastAPI servers, and vLLM and TensorRT-LLM runtimes.

- **+** Covers 9 languages and 18+ Chinese dialects, with cross-lingual zero-shot voice cloning
- **+** Bi-streaming (text in, audio out) with latency as low as 150ms
- **+** Pinyin and CMU phoneme inpainting; instructions for emotion, speed and volume
- **+** Ships training scripts, FastAPI and gRPC servers, plus vLLM and TensorRT-LLM runtimes
- **−** Setup is manual: conda env, git submodules, separate model downloads, sox install
- **−** README gives no RAM or VRAM requirements
- **−** vLLM supported only on 0.9.0 and 0.11.x+; versions in between are untested
- **−** No tagged releases; install commands default to Chinese PyPI mirrors

<sub>Docker · Needs Python 3.10, conda, sox, vLLM (optional), TensorRT-LLM (optional), ttsfrd (optional) · Models: Fun-CosyVoice3-0.5B-2512, CosyVoice2-0.5B, CosyVoice-300M, CosyVoice-300M-SFT, CosyVoice-300M-Instruct · port 50000 · [Repo](https://github.com/qwenaudio/cosyvoice) · [▶️ Demo ↗](https://funaudiollm.github.io/cosyvoice3/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cosyvoice/)</sub>

<a name="pyannote-audio"></a>
### #&#8288;47 [pyannote-audio](https://github.com/pyannote/pyannote-audio) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (39) · Freshness: active (100) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**Python toolkit for speaker diarization with pretrained PyTorch pipelines.**

pyannote.audio is a PyTorch-based Python toolkit that labels who speaks when in an audio file. It loads pretrained pipelines such as community-1 from Hugging Face and runs them locally, and the pipelines and models can be fine-tuned on your own data. A separate premium precision-2 pipeline runs on pyannoteAI servers through an API key.

- **+** Pretrained community-1 runs locally; README reports lower DER than 3.1 on 11 of 12 listed benchmarks
- **+** Pipelines and models can be fine-tuned, with multi-GPU training via pytorch-lightning
- **+** Python-first API with a progress hook and optional GPU placement via pipeline.to()
- **+** MIT license, with notebook tutorials for applying, adapting and training pipelines
- **−** Needs a Hugging Face token and acceptance of user conditions to download community-1
- **−** precision-2, with lower reported DER than community-1, is premium and needs a pyannoteAI key
- **−** Some tutorials were written for older versions and are described as needing updates
- **−** Optional anonymous telemetry exists; README does not say whether it is on by default

<sub>GPU optional · Needs ffmpeg, torchcodec, PyTorch, Hugging Face access token, pyannoteAI API key (precision-2 only) · Models: pyannote/speaker-diarization-community-1, pyannote/speaker-diarization-3.1, pyannote/speaker-diarization-precision-2 (hosted) · [Repo](https://github.com/pyannote/pyannote-audio) · [📖 Docs ↗](https://docs.pyannote.ai) · [🌐 Site ↗](https://pyannote.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyannote-audio/)</sub>

<a name="so-vits-svc-fork"></a>
### #&#8288;48 [so-vits-svc-fork](https://github.com/voicepaw/so-vits-svc-fork) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (31) · Freshness: active (93) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · custom license · Oct 2026</sub>

**Singing voice conversion with realtime mic input, GUI and CLI training.**

Fork of so-vits-svc 4.0 (v1) that converts a voice to a trained target speaker, from files or live microphone input, using the `svcg` GUI or the `svc` CLI. It adds CREPE pitch estimation, a ContentVec fix, QuickVC's MS-iSTFT decoder and pip installation with automatic pretrained model download. The README states it is no longer maintained and has been in maintenance only since Spring 2023.

- **+** Realtime conversion from microphone via `svc vc`, plus file inference with `svc infer`
- **+** Installs with pip; pretrained models download automatically, no fairseq needed
- **+** Full CLI pipeline for preprocessing, splitting, diarization and training
- **+** CPU inference supported; GPU inference and training need at least 4 GB VRAM
- **−** README declares the project no longer maintained, since Spring 2023
- **−** Only 4.0v1 models are compatible; 4.1 and other models are unsupported
- **−** ONNX export is listed as currently not working
- **−** AMD GPUs unsupported on Windows; Linux needs a ROCm build of PyTorch

<sub>GPU optional · Docker · Needs PyTorch, torchaudio, Python 3.11, pyannote.audio (optional, for diarization) · Models: so-vits-svc 4.0v1, QuickVC (MS-iSTFT decoder), ContentVec, HuBERT, CREPE · [Repo](https://github.com/voicepaw/so-vits-svc-fork) · [📖 Docs ↗](https://so-vits-svc-fork.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/so-vits-svc-fork/)</sub>

<a name="speech-recognition"></a>
### #&#8288;49 [speech_recognition](https://github.com/uberi/speech_recognition) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · BSD-3-Clause · Sep 2026</sub>

**Python library wrapping many speech-to-text engines and APIs behind one interface.**

SpeechRecognition is a Python library that transcribes audio from files or a microphone through a common Recognizer API. It wraps offline engines (CMU Sphinx, Vosk, Whisper, Faster Whisper) and cloud APIs (Google, Azure, Wit.ai, Houndify, IBM, OpenAI, Groq, Cohere). Install with pip, using per-engine extras.

- **+** One recognizer interface across offline engines and a dozen cloud APIs
- **+** Offline options: Sphinx, Vosk, Whisper, Faster Whisper
- **+** OpenAI-compatible self-hosted endpoints (vLLM, Ollama) work via OPENAI_BASE_URL
- **+** Per-engine pip extras; FLAC bundled on x86 Windows, Linux and Intel macOS
- **−** Microphone input needs PyAudio, which requires PortAudio setup on Linux and macOS
- **−** Google Cloud support is V1 only; V2 is not supported
- **−** README documents no streaming transcription, only phrase and file recognition
- **−** Sphinx needs a specific PocketSphinx build; repository packages are outdated

<sub>GPU optional · Needs PyAudio (microphone), PocketSphinx, FLAC encoder (non-x86 systems), Vosk models, Cloud API keys · Models: CMU Sphinx, Vosk, OpenAI Whisper, Faster Whisper, OpenAI Transcription API · [Repo](https://github.com/uberi/speech_recognition) · [📖 Docs ↗](https://github.com/Uberi/speech_recognition/blob/master/reference/library-reference.rst) · [🌐 Site ↗](https://pypi.python.org/pypi/SpeechRecognition/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speech-recognition/)</sub>

<a name="voice-pro"></a>
### #&#8288;50 [voice-pro](https://github.com/abus-aikorea/voice-pro) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (49) · Freshness: active (95) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · GPL-3.0 · Jul 2026</sub>

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

<a name="vosk-api"></a>
### #&#8288;51 [vosk-api](https://github.com/alphacep/vosk-api) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (55) · Freshness: recent (70) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

**Offline speech recognition toolkit with streaming API and many language bindings.**

Vosk is an offline speech recognition toolkit covering 20+ languages and dialects. It exposes a streaming API with continuous large-vocabulary transcription, reconfigurable vocabulary and speaker identification, with bindings for Python, Java, Node.js, C#, C++, Rust, Go and others. Models are described as about 50 MB, and it runs from Raspberry Pi and Android up to clusters.

- **+** Runs fully offline; no cloud service needed for transcription
- **+** Small models (about 50 MB) suit Raspberry Pi and Android
- **+** Bindings for Python, Java, Node.js, C#, C++, Rust, Go and more
- **+** Streaming API with reconfigurable vocabulary and speaker identification
- **−** README gives no accuracy or word error rate figures
- **−** Last release was April 2024, despite recent commits
- **−** Install steps, examples and model downloads live on an external site
- **−** Speech-to-text only; no synthesis or diarization details in the README

<sub>Models: Vosk offline speech recognition models (20+ languages) · [Repo](https://github.com/alphacep/vosk-api) · [📖 Docs ↗](https://alphacephei.com/vosk) · [🌐 Site ↗](https://alphacephei.com/vosk) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vosk-api/)</sub>

<a name="abogen"></a>
### #&#8288;52 [abogen](https://github.com/denizsafak/abogen) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (10) · Freshness: active (93) · Maintenance: patchy (41) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Oct 2026</sub>

**Converts ePub, PDF and text files to audiobooks with subtitles using Kokoro-82M.**

Abogen turns ePub, PDF, text, markdown and subtitle files into speech with the Kokoro-82M model, and generates synced subtitles in SRT or ASS. It ships a PyQt6 desktop app (`abogen`) and a Flask web UI (`abogen-web`, port 8808) with a background job queue. Output formats include WAV, FLAC, MP3, OPUS and M4B with chapters.

- **+** Outputs M4B with chapters, plus WAV, FLAC, MP3 and OPUS, with optional per-chapter files
- **+** Subtitles by line, sentence or N words, in SRT or ASS
- **+** Voice mixer blends Kokoro voices into saved profiles; batch queue with per-file settings
- **+** Models can be pre-downloaded for fully offline use
- **−** Requires a separate espeak-ng install on every platform
- **−** Web UI has features missing from the desktop app, such as Supertonic TTS and LLM normalization
- **−** Setup is fiddly: CUDA-specific extras, pinned PyTorch, AMD GPU only on Linux
- **−** Apple Silicon install needs Kokoro from git and numpy<2

<sub>GPU optional · Compose · Needs espeak-ng, PyTorch · Models: Kokoro-82M, Supertonic TTS · port 8808 · [Repo](https://github.com/denizsafak/abogen) · [▶️ Demo ↗](https://github.com/user-attachments/assets/094ba3df-7d66-494a-bc31-0e4b41d0b865) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/abogen/)</sub>

<a name="real-time-voice-cloning"></a>
### #&#8288;53 [real-time-voice-cloning](https://github.com/corentinj/real-time-voice-cloning) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: widely used (93) · Freshness: slowing (47) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · custom license · Mar 2026</sub>

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

<a name="chatterbox"></a>
### #&#8288;54 [chatterbox](https://github.com/resemble-ai/chatterbox) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (75) · Freshness: recent (70) · Maintenance: weak (1) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · MIT · Jul 2026</sub>

**Open text-to-speech models with zero-shot voice cloning in 23+ languages.**

Chatterbox is a family of Python text-to-speech models from Resemble AI that clone a voice from a short reference clip. It includes a 500M multilingual V3 model covering 23 languages, a 350M English Turbo model for low-latency agents, and a 110M Nano model for CPU inference. Turbo and Nano support paralinguistic tags such as [laugh] and [cough].

- **+** Model sizes from 110M (Nano) to 500M (Multilingual V3) cover CPU through GPU use
- **+** Zero-shot voice cloning from a reference clip, including across languages
- **+** Turbo decoder distilled from 10 steps to one for lower latency
- **+** Every output carries a Perth watermark, with a documented extraction script
- **−** Turbo and Nano are English only; multilingual needs the 500M model
- **−** Tested only on Python 3.11 on Debian 11; dependencies pinned
- **−** No built-in server, web UI or Docker setup; Python API only
- **−** Last tagged release is 2025-06-13, while newer models ship from main

<sub>GPU optional · Needs PyTorch, torchaudio, Hugging Face model weights · Models: Chatterbox-Turbo 350M, Chatterbox-Nano 110M, Chatterbox-Multilingual V3 500M, Single Language Pack (6 finetunes), Chatterbox 500M English · [Repo](https://github.com/resemble-ai/chatterbox) · [▶️ Demo ↗](https://huggingface.co/spaces/ResembleAI/Chatterbox-Multilingual-TTS) · [🌐 Site ↗](https://resemble.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatterbox/)</sub>

<a name="silero-models"></a>
### #&#8288;55 [silero-models](https://github.com/snakers4/silero-models) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · custom license · Oct 2026</sub>

**Pretrained PyTorch text-to-speech models for Russian, CIS and Indic languages.**

Silero Models provides pretrained TTS models loaded through torch.hub or the `silero` pip package, with models downloaded on demand. V5 models support SSML and 8000, 24000 and 48000 Hz sampling rates. Russian models add automatic stress and homograph handling, and separate models cover Turkic, Caucasian, other CIS and Indic languages.

- **+** Covers many minority CIS languages (Turkic, Caucasian) rarely supported elsewhere
- **+** Russian models include automatic stress, homographs and question intonation
- **+** Loads in a few lines via pip or torch.hub; models fetched on demand
- **+** V5 models support SSML and three sampling rates (8k, 24k, 48k)
- **−** Main license is CC BY-NC 4.0, non-commercial; only the CIS base models are MIT
- **−** Only TTS is described in the visible README; no speech-to-text covered
- **−** No Docker image or HTTP server provided; you wrap the Python API yourself
- **−** V5 CIS base models need manually placed stress marks, or use the nostress variant

<sub>GPU optional · Needs PyTorch · Models: PyTorch TTS models, SSML · [Repo](https://github.com/snakers4/silero-models) · [📖 Docs ↗](https://github.com/snakers4/silero-models/wiki/SSML) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/silero-models/)</sub>

<a name="emotivoice"></a>
### #&#8288;56 [emotivoice](https://github.com/netease-youdao/emotivoice) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · Apache-2.0 · Sep 2026</sub>

**Text-to-speech engine with emotion and style prompts, English and Chinese.**

EmotiVoice synthesizes speech in English and Chinese from over 2000 voices, with emotion (happy, sad, angry, excited and others) controlled through text prompts. It ships a Streamlit demo page on port 8501, a batch inference script, and an OpenAI-compatible TTS API with speed control. Voice cloning on personal data is documented on the wiki.

- **+** Prompt-controlled emotion and style across 2000+ voices in English and Chinese
- **+** OpenAI-compatible TTS API on port 8000, with speed tuning
- **+** Batch scripting interface plus Streamlit web demo
- **+** Voice cloning recipes for DataBaker and LJSpeech datasets
- **−** Only English and Chinese; Japanese and Korean are still under development
- **−** Manual setup needs separate pretrained model downloads from ModelScope or Hugging Face
- **−** Inference input uses a pipe-delimited phoneme format that needs a frontend step
- **−** Docker quickstart requires an NVIDIA GPU and container toolkit; no release tags published

<sub>GPU required · Docker · Needs Docker, NVIDIA container toolkit, PyTorch, Streamlit, FastAPI, Git LFS · Models: PromptTTS-based acoustic model with HiFi-GAN vocoder, SimBERT Chinese · port 8501 · [Repo](https://github.com/netease-youdao/emotivoice) · [▶️ Demo ↗](https://replicate.com/bramhooimeijer/emotivoice) · [📖 Docs ↗](https://github.com/netease-youdao/EmotiVoice/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/emotivoice/)</sub>

<a name="qwen3-tts"></a>
### #&#8288;57 [qwen3-tts](https://github.com/qwenlm/qwen3-tts) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: popular (51) · Freshness: recent (50) · Maintenance: weak (21) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Mar 2026</sub>

**Open-weight multilingual text-to-speech models with voice cloning and voice design.**

Qwen3-TTS is a family of 0.6B and 1.7B text-to-speech models from Qwen, with a Python package (qwen-tts) for custom-voice, voice-design and voice-clone generation. It covers 10 languages, supports streaming with a stated end-to-end latency as low as 97ms, and clones a voice from a 3-second reference clip. The repo also has a local web UI demo, vLLM usage notes and fine-tuning instructions.

- **+** Three modes in one family: preset speakers, text-described voices, and 3-second voice cloning
- **+** Covers 10 languages plus dialect voices such as Beijing and Sichuan Chinese
- **+** Streaming and non-streaming from one model; README cites 97ms end-to-end latency
- **+** Apache-2.0 weights on Hugging Face and ModelScope, with fine-tuning and vLLM docs
- **−** Examples assume a CUDA GPU; CPU-only use is not documented in the README
- **−** Instruction control is only listed for the 1.7B CustomVoice and VoiceDesign models
- **−** Only 9 preset speakers in the CustomVoice models
- **−** No Docker image or release tags; install is via pip in a Python 3.12 environment

<sub>GPU required · Needs PyTorch, FlashAttention 2 (recommended), Hugging Face Transformers, soundfile · Models: Qwen3-TTS-12Hz-1.7B-VoiceDesign, Qwen3-TTS-12Hz-1.7B-CustomVoice, Qwen3-TTS-12Hz-1.7B-Base, Qwen3-TTS-12Hz-0.6B-CustomVoice, Qwen3-TTS-12Hz-0.6B-Base · port 8000 · [Repo](https://github.com/qwenlm/qwen3-tts) · [▶️ Demo ↗](https://huggingface.co/spaces/Qwen/Qwen3-TTS) · [🌐 Site ↗](https://qwen.ai/blog?id=qwen3tts-0115) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwen3-tts/)</sub>

<a name="paddlespeech"></a>
### #&#8288;58 [paddlespeech](https://github.com/paddlepaddle/paddlespeech) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: known (47) · Freshness: recent (57) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Jun 2026</sub>

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

<a name="mockingbird"></a>
### #&#8288;59 [mockingbird](https://github.com/babysor/mockingbird) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: widely used (83) · Freshness: slowing (32) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · custom license · Mar 2026</sub>

**Mandarin voice cloning toolbox built on SV2TTS.**

Clones a speaker's voice from a short audio sample and synthesizes Mandarin speech from text. It reuses the pretrained SV2TTS encoder and vocoder (WaveRNN, HiFi-GAN) and needs a separately trained Tacotron-based synthesizer. Inference runs through a PyQt toolbox, a web server on port 8080, or a command-line script. The author no longer actively updates the repo.

- **+** Full pipeline: encoder, synthesizer and vocoder training scripts plus three inference interfaces
- **+** Mandarin synthesizer tested on aidatatang_200zh, magicdata, aishell3 and data_aishell
- **+** Supports both WaveRNN and HiFi-GAN vocoders
- **+** Community-shared pretrained synthesizers are listed, so training is optional
- **−** Author says the repo is no longer actively updated; last release is 2021-11-07
- **−** Recommended environment is old: PyTorch 1.9.0, CUDA 10.2
- **−** Pretrained synthesizer links are on Baidu and Aliyun; some only work with version 0.0.1
- **−** M1 Mac setup needs Rosetta and manual compilation of pyworld and ctc-segmentation

<sub>GPU optional · Docker + Compose · Needs PyTorch, ffmpeg, webrtcvad-wheels, PyQt5, visdom · Models: SV2TTS encoder, Tacotron synthesizer, WaveRNN, HiFi-GAN · port 8080 · [Repo](https://github.com/babysor/mockingbird) · [▶️ Demo ↗](https://www.bilibili.com/video/BV17Q4y1B7mY/) · [🌐 Site ↗](https://noiz.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mockingbird/)</sub>

<a name="neutts"></a>
### #&#8288;60 [neutts](https://github.com/neuphonic/neutts) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (12) · Freshness: active (96) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · custom license · Jul 2026</sub>

**On-device text-to-speech models with voice cloning from short reference audio.**

NeuTTS is a family of small LLM-backbone speech models (about 120m to 360m active parameters) that synthesize speech and clone a voice from a 3-15 second reference clip. Models ship as PyTorch weights and Q4/Q8 GGUF files, paired with the NeuCodec audio codec, and run through a Python package. Variants cover English, French, German and Spanish, plus NeuTTS-2E with six emotions plus neutral.

- **+** GGUF Q4/Q8 builds run on CPU; README benchmarks include a Galaxy A25 phone and an M4 iMac
- **+** Voice cloning from about 3 seconds of reference audio, with pre-encoded sample voices bundled
- **+** Streaming via llama-cpp-python, ONNX codec decoder for lower latency, and a finetune script
- **+** Generated audio carries a Perth watermark by default
- **−** Context window is 2048 tokens, roughly 30 seconds of audio including the prompt
- **−** Nano and 2E models use NeuTTS Open License 1.0; only Air is Apache 2.0
- **−** Streaming works only with GGUF backbones, which need llama-cpp-python built for your hardware
- **−** NeuTTS-2E has four fixed speakers and no cloning; uv sync install skips watermarking

<sub>GPU optional · Needs llama-cpp-python, onnxruntime, PortAudio, OpenBLAS · Models: NeuTTS-Air, NeuTTS-Nano, NeuTTS-Nano French/German/Spanish, NeuTTS-2E, GGUF Q4/Q8 · [Repo](https://github.com/neuphonic/neutts) · [▶️ Demo ↗](https://huggingface.co/spaces/neuphonic/neutts-air) · [🌐 Site ↗](http://neuphonic.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/neutts/)</sub>

<a name="voicecraft"></a>
### #&#8288;61 [voicecraft](https://github.com/jasonppy/voicecraft) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (27) · Freshness: recent (77) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · custom license · May 2026</sub>

**Zero-shot voice cloning TTS and speech editing from seconds of reference audio.**

VoiceCraft is a token-infilling neural codec language model that does zero-shot text-to-speech and speech editing, cloning an unseen voice from a few seconds of reference audio. The repo includes inference notebooks, command-line demos, a Gradio app on port 7860, and scripts for training and fine-tuning. Weights for 330M and 830M models are on Hugging Face.

- **+** Covers both zero-shot TTS and speech editing in one model
- **+** Gradio app with TTS, Edit and Long TTS modes, plus CLI scripts
- **+** Training and fine-tuning scripts and RealEdit manifests are included
- **+** Hosted demos on Hugging Face Spaces, Colab and Replicate
- **−** Code is CC BY-NC-SA 4.0 and weights use Coqui license: non-commercial
- **−** Pinned old stack: Python 3.9, torch 2.0.1, CUDA 11.7, MFA, espeak
- **−** Fine-tuned models limit prompt plus generation to 16 seconds
- **−** Manual, heavy setup; the Docker route only launches Jupyter

<sub>GPU required · Docker · Needs Python 3.9, PyTorch 2.0.1, audiocraft, ffmpeg, espeak-ng, Montreal Forced Aligner, Docker with NVIDIA container toolkit (optional) · Models: VoiceCraft giga330M, VoiceCraft giga830M, 330M/830M TTS Enhanced, Encodec 56M · port 7860 · [Repo](https://github.com/jasonppy/voicecraft) · [▶️ Demo ↗](https://huggingface.co/spaces/pyp1/VoiceCraft_gradio) · [🌐 Site ↗](https://jasonppy.github.io/VoiceCraft_web/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voicecraft/)</sub>

<a name="megatts3"></a>
### #&#8288;62 [megatts3](https://github.com/bytedance/megatts3) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (8) · Freshness: active (83) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · Apache-2.0 · Jun 2026</sub>

**Zero-shot Chinese and English voice-cloning TTS with a 0.45B diffusion transformer.**

MegaTTS 3 is ByteDance's PyTorch implementation of a latent diffusion transformer for zero-shot speech synthesis in Chinese, English and code-switched text. It ships a CLI and a Gradio web UI, plus an aligner, a Qwen2.5-0.5B grapheme-to-phoneme model and a WaveVAE that can be used on their own. The WaveVAE encoder is not released, so cloning needs pre-extracted .npy latents for each voice.

- **+** Diffusion Transformer backbone is only 0.45B parameters
- **+** Accent strength adjustable through p_w and t_w inference weights
- **+** Aligner, G2P and WaveVAE submodules are reusable outside TTS
- **+** CPU inference works, about 30 seconds for 10 steps
- **−** WaveVAE encoder withheld; custom voices need .npy latents supplied by the authors
- **−** Only Chinese and English supported
- **−** Windows and Docker setups are marked as under testing
- **−** Fine-grained pronunciation and duration control is listed as coming soon

<sub>GPU optional · Docker · Needs Python 3.10, PyTorch 2.6.0, Gradio, ffmpeg, WeTextProcessing · Models: MegaTTS3 checkpoints (Hugging Face, Google Drive), Qwen2.5-0.5B G2P, WaveVAE · port 7860 · [Repo](https://github.com/bytedance/megatts3) · [▶️ Demo ↗](https://huggingface.co/spaces/ByteDance/MegaTTS3) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/megatts3/)</sub>

<a name="speaches"></a>
### #&#8288;63 [Speaches](https://github.com/speaches-ai/speaches) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: niche (2) · Freshness: recent (63) · Maintenance: weak (7) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Apr 2026</sub>

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

<a name="amphion"></a>
### #&#8288;64 [amphion](https://github.com/open-mmlab/amphion) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: known (36) · Freshness: slowing (37) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Mar 2026</sub>

**PyTorch toolkit for training and running speech, singing and audio generation models.**

Amphion is a research toolkit with recipes and pretrained checkpoints for text-to-speech, voice conversion, accent conversion, singing voice conversion and text-to-audio. It includes models such as FastSpeech2, VITS, VALL-E, MaskGCT, Vevo and DualCodec, plus several vocoders and evaluation metrics. It also ships the Emilia multilingual speech dataset and its preprocessing pipeline.

- **+** Covers TTS, VC, AC, SVC and TTA in one codebase with per-task recipes
- **+** Includes many vocoders (HiFi-GAN, BigVGAN, DiffWave, WaveNet) and evaluation metrics
- **+** Pretrained checkpoints on Hugging Face and ModelScope, including MaskGCT, Vevo and Metis
- **+** Releases the Emilia dataset (over 200k hours with Emilia-Large) and its preprocessing pipeline
- **−** Research-oriented; no packaged end-user app or server API in the README
- **−** Last tagged release is 2024-02-23, though commits continue
- **−** Text-to-music is listed as still in development
- **−** Emilia original data is CC BY-NC 4.0, unlike the MIT code

<sub>Docker · Needs PyTorch · Models: FastSpeech2, VITS, VALL-E, NaturalSpeech2, MaskGCT · [Repo](https://github.com/open-mmlab/amphion) · [▶️ Demo ↗](https://huggingface.co/spaces/amphion/maskgct) · [📖 Docs ↗](https://github.com/open-mmlab/Amphion/blob/main/egs/tts/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/amphion/)</sub>

<a name="dia"></a>
### #&#8288;65 [dia](https://github.com/nari-labs/dia) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: popular (63) · Freshness: quiet (7) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Nov 2025</sub>

**1.6B text-to-speech model that generates two-speaker dialogue from a transcript.**

Dia is a 1.6B parameter English text-to-speech model from Nari Labs that turns a script tagged with [S1] and [S2] into multi-speaker dialogue. It supports nonverbal tags such as (laughs) and (coughs), and voice cloning from a 5-10 second audio prompt with transcript. The repo ships inference code, a Gradio UI and a CLI, and the model also loads through Hugging Face Transformers.

- **+** Generates two-speaker dialogue in one pass using [S1]/[S2] tags
- **+** Voice cloning from an audio prompt plus transcript
- **+** About 4.4GB VRAM in bfloat16/float16, ~2x realtime on RTX 4090 with compile
- **+** Apache-2.0 weights on Hugging Face, with a Transformers integration and Gradio UI
- **−** English only
- **−** Tested on GPUs only; CPU support listed as not yet available
- **−** No fixed voice: speakers differ per run unless seed or audio prompt is set
- **−** Very short or long inputs sound unnatural; unlisted nonverbal tags cause artifacts

<sub>GPU required · Docker · Needs PyTorch 2.0+, CUDA 12.6, Descript Audio Codec · Models: Dia-1.6B-0626, Hugging Face Transformers · [Repo](https://github.com/nari-labs/dia) · [▶️ Demo ↗](https://huggingface.co/spaces/nari-labs/Dia-1.6B-0626) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dia/)</sub>

<a name="asrt-speechrecognition"></a>
### #&#8288;66 [asrt_speechrecognition](https://github.com/nl8590687/asrt_speechrecognition) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (25) · Freshness: slowing (41) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · GPL-3.0 · Apr 2026</sub>

**Mandarin speech recognition on TensorFlow Keras, with HTTP and gRPC servers.**

ASRT is a Chinese speech recognition system. A DCNN+CTC acoustic model maps audio of up to 16 seconds to pinyin, and a maximum-entropy hidden Markov language model converts pinyin to Chinese characters. The repo includes training and evaluation scripts, HTTP and gRPC API servers, and client SDKs for several languages.

- **+** Full pipeline in one repo: training, evaluation, single-file prediction and API servers
- **+** Serves recognition over HTTP and gRPC, with client SDKs for Python, Go, Java and Windows
- **+** Docker image runs CPU-only inference, exposing ports 20001 and 20002
- **+** Default config covers six public Chinese datasets, including THCHS30, AIShell-1 and MagicData
- **−** Chinese only; the README mentions no other languages
- **−** README reports about 85% pinyin accuracy on the test set for the top model
- **−** Training needs an NVIDIA GPU with 11 GB+ VRAM, 16 GB RAM and 500 GB disk
- **−** Last release was 2022-05; README and docs are mainly in Chinese

<sub>RAM ≥ 16 GB · GPU optional · Docker · Needs TensorFlow 2.5+, Python 3.9+, Flask, Waitress, grpcio, CUDA 11.2 and cuDNN 8.1 for GPU training · Models: DCNN+CTC acoustic models 24, 25, 251, 251bn, pinyin-to-text statistical language model · port 20001 · [Repo](https://github.com/nl8590687/asrt_speechrecognition) · [▶️ Demo ↗](https://www.ailemon.net/asrt/demo) · [📖 Docs ↗](https://wiki.ailemon.net/docs/asrt-doc) · [🌐 Site ↗](https://www.ailemon.net/asrt) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/asrt-speechrecognition/)</sub>

<a name="orpheus-tts"></a>
### #&#8288;67 [orpheus-tts](https://github.com/canopyai/orpheus-tts) <sub>score [8](../README.md#-how-we-rank "Score 8/100. Adoption: niche (13) · Freshness: quiet (13) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Dec 2025</sub>

**Llama-3B-based text-to-speech model with emotion tags and streaming output.**

Orpheus TTS is a speech synthesis model built on a Llama-3B backbone, released as pretrained and finetuned English checkpoints plus a multilingual research family on Hugging Face. The orpheus-speech Python package streams audio through vLLM, with a stated latency of about 200ms. The repo also includes finetuning and pretraining scripts, a watermarking option, and a llama.cpp path for running without a GPU.

- **+** Streaming generation with stated ~200ms latency, ~100ms with input streaming
- **+** Emotive tags such as <laugh>, <sigh> and <gasp>, plus 8 named English voices
- **+** Finetuning scripts and dataset prep notebook; README cites good results from ~50 examples
- **+** Apache-2.0 code with a llama.cpp option for no-GPU inference
- **−** Streaming package occasionally skips frames, listed as an open checklist item
- **−** Voice cloning Colab notebook is listed as needing a fix
- **−** vLLM version problems; README suggests pinning vllm==0.7.3 as a workaround
- **−** Smaller 1b, 400m and 150m models unreleased; multilingual models are research preview

<sub>GPU optional · Needs vllm, transformers, trl, accelerate, wandb (finetuning) · Models: orpheus-tts-0.1-finetune-prod, orpheus-tts-0.1-pretrained, Orpheus multilingual research models · [Repo](https://github.com/canopyai/orpheus-tts) · [▶️ Demo ↗](https://huggingface.co/spaces/MohamedRashad/Orpheus-TTS) · [🌐 Site ↗](https://canopylabs.ai/model-releases) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/orpheus-tts/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
