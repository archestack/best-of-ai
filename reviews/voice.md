# 🎙️ Voice reviews · Best of Open-Source AI

Speech-to-text, text-to-speech, voice agents and meeting tools that run locally. Back to the [leaderboard](../README.md#%EF%B8%8F-voice).

<sub>🌐 Also on the web: [Voice on archestack.com](https://archestack.com/best-of-ai/voice/), each project on its own page.</sub>

<a name="voicestudio"></a>
### 🥇 [voicestudio](https://github.com/debpalash/voicestudio) <sub>score [98](../README.md#-how-we-rank "Score 98/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 119k · AGPL-3.0 · Nov 2026</sub>

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

<a name="handy"></a>
### 🥈 [handy](https://github.com/cjpais/handy) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Nov 2026</sub>

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

<a name="whisper-cpp"></a>
### 🥉 [whisper.cpp](https://github.com/ggml-org/whisper.cpp) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 56k · MIT · Nov 2026</sub>

**C/C++ speech-to-text engine running OpenAI Whisper models locally.**

whisper.cpp is a dependency-free C/C++ port of OpenAI's Whisper ASR model, built on ggml, with a C-style API in whisper.h and a whisper-cli example for transcribing 16-bit WAV files. It runs on CPU or on accelerators including Metal, Core ML, CUDA, Vulkan, ROCm, OpenVINO, Ascend CANN, MUSA and AMD Ryzen AI NPU, and supports integer quantization and VAD.

- **+** No runtime dependencies; CPU-only inference works, with zero memory allocations at runtime
- **+** Broad backend coverage: Metal, Core ML, CUDA, Vulkan, ROCm, OpenVINO, CANN, MUSA, Ryzen AI NPU
- **+** Runs on macOS, iOS, Android, Linux, Windows, WebAssembly and Raspberry Pi
- **+** Quantized models and small footprints: tiny needs ~273 MB, large ~3.9 GB
- **−** whisper-cli accepts only 16-bit WAV unless built with the FFmpeg option
- **−** Core ML, OpenVINO and ANEForge need Python-side model conversion before use
- **−** Each accelerator needs its own CMake flag and SDK; no single universal GPU build
- **−** Transcription only; no built-in diarization or translation to non-English targets is described

<sub>RAM ≥ 0.3 GB · GPU optional · Docker · Needs CMake, ffmpeg (optional, for audio conversion), CUDA / ROCm / OpenVINO / CANN / MUSA SDKs (optional) · Models: Whisper ggml models (tiny, base, small, medium, large-v1/v2/v3, large-v3-turbo), Q5_0 and other integer quantization, Core ML and OpenVINO encoder models · [Repo](https://github.com/ggml-org/whisper.cpp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisper-cpp/)</sub>

<a name="meetily"></a>
### #&#8288;4 [meetily](https://github.com/zackriya-solutions/meetily) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · MIT · Nov 2026</sub>

**Desktop app that records, transcribes and summarizes meetings locally.**

Meetily is a Tauri desktop app with a Rust backend and Next.js frontend. It captures microphone and system audio, transcribes live with Whisper or Parakeet models on-device, and generates summaries through Ollama, Claude, Groq, OpenRouter, or any OpenAI-compatible endpoint. Audio and transcripts stay local; only transcript text is sent if a cloud summary provider is chosen.

- **+** Local Whisper or Parakeet transcription; audio never leaves the machine
- **+** Summary providers include Ollama, Claude, Groq, OpenRouter, and custom OpenAI-compatible endpoints
- **+** Records microphone and system audio together, with ducking and clipping prevention
- **+** Imports existing audio files and can re-transcribe with a different model or language
- **−** Speaker identification, custom templates, and PDF/DOCX export are only in paid PRO
- **−** Prebuilt installers cover Windows and Apple Silicon macOS only; Linux needs a source build
- **−** Standard Windows installer uses Vulkan; CUDA requires a custom source build
- **−** Import and Enhance feature is marked Beta

<sub>GPU optional · Needs Ollama (optional, for local summaries) · Models: Whisper, Parakeet (ONNX), Ollama, Claude, Groq · [Repo](https://github.com/zackriya-solutions/meetily) · [▶️ Demo ↗](https://youtu.be/6FnhSC_eSz8) · [📖 Docs ↗](https://github.com/Zackriya-Solutions/meetily/blob/main/docs/BUILDING.md) · [🌐 Site ↗](https://meetily.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/meetily/)</sub>

<a name="agents"></a>
### #&#8288;5 [livekit/agents](https://github.com/livekit/agents) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;6 [ebook2audiobook](https://github.com/drewthomasson/ebook2audiobook) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Nov 2026</sub>

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

<a name="xiaozhi-esp32"></a>
### #&#8288;7 [xiaozhi-esp32](https://github.com/78/xiaozhi-esp32) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Nov 2026</sub>

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

<a name="sherpa-onnx"></a>
### #&#8288;8 [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

**Local speech recognition, TTS, diarization and VAD runtime on ONNX.**

sherpa-onnx runs speech-to-text (streaming and non-streaming), text-to-speech, speaker diarization and identification, VAD, keyword spotting, speech enhancement, source separation and forced alignment locally. It is written in C++ with bindings for C, Python, JavaScript, Java, C#, Kotlin, Swift, Go, Dart, Rust and Pascal. Targets include Android, iOS, HarmonyOS, WebAssembly, desktop OSes, embedded boards and several NPUs.

- **+** Covers ASR, TTS, diarization, VAD, keyword spotting and enhancement in one runtime
- **+** Bindings for 12 languages, including C, Python, Swift, Kotlin, Go and Rust
- **+** Runs on x64, arm32/64 and riscv64, plus Rockchip, Qualcomm, Ascend, Axera and Intel NPUs
- **+** Browser demos on Hugging Face Spaces, plus prebuilt Android APKs and Flutter apps
- **−** Library and SDK, not a ready-to-use server or desktop app
- **−** Models are downloaded separately; many pre-trained ASR and TTS models to choose from
- **−** No Docker image or compose file detected
- **−** Many platform and language combinations, so build steps vary by target

<sub>GPU optional · Needs ONNX Runtime · Models: Zipformer, Paraformer, Whisper, SenseVoice, Moonshine · [Repo](https://github.com/k2-fsa/sherpa-onnx) · [▶️ Demo ↗](https://huggingface.co/spaces/k2-fsa/automatic-speech-recognition) · [📖 Docs ↗](https://k2-fsa.github.io/sherpa/onnx/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sherpa-onnx/)</sub>

<a name="speech-to-speech"></a>
### #&#8288;9 [Speech-to-Speech](https://github.com/huggingface/speech-to-speech) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

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

<a name="whisperlivekit"></a>
### #&#8288;10 [whisperlivekit](https://github.com/quentinfuxa/whisperlivekit) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="pyvideotrans"></a>
### #&#8288;11 [pyvideotrans](https://github.com/jianchang512/pyvideotrans) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · GPL-3.0 · Nov 2026</sub>

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

<a name="openwhispr"></a>
### #&#8288;12 [openwhispr](https://github.com/openwhispr/openwhispr) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Nov 2026</sub>

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

<a name="voicebox"></a>
### #&#8288;13 [Voicebox](https://github.com/jamiepine/voicebox) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 61k · MIT · Nov 2026</sub>

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

<a name="buzz"></a>
### #&#8288;14 [chidiwilliams/buzz](https://github.com/chidiwilliams/buzz) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · MIT · Nov 2026</sub>

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

<a name="funasr"></a>
### #&#8288;15 [funasr](https://github.com/modelscope/funasr) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Nov 2026</sub>

**Speech recognition toolkit with VAD, punctuation, speaker labeling and streaming.**

FunASR is a Python toolkit that runs offline and streaming speech recognition through an AutoModel API, a CLI and an OpenAI-compatible transcription server (funasr-server). It bundles ASR checkpoints (Fun-ASR-Nano, SenseVoiceSmall, Paraformer), plus VAD, punctuation, CAM++ speaker clustering and emotion models. GGUF builds run through a llama.cpp binary on CPU or Vulkan/CUDA without Python.

- **+** Composable pipeline: ASR, FSMN-VAD, ct-punc and CAM++ speaker clustering in one AutoModel call
- **+** Streaming Paraformer with chunked input and per-session cache
- **+** GGUF llama.cpp binaries run SenseVoice on CPU with no Python at runtime
- **+** OpenAI-compatible /v1/audio/transcriptions server, plus CLI with SRT and JSON output
- **−** Language coverage differs per checkpoint; Fun-ASR-Nano is only zh/en/ja plus Chinese dialects
- **−** Speaker labels are anonymous per recording, not known-speaker identification
- **−** Bundled server is unauthenticated and meant for loopback use only
- **−** Model weights carry their own licenses, separate from the MIT toolkit

<sub>GPU optional · Needs PyTorch, torchaudio, FastAPI and uvicorn (server), vLLM (optional, Nano GPU serving) · Models: Fun-ASR-Nano, Fun-ASR-MLT-Nano, SenseVoiceSmall, Paraformer-zh, Paraformer-zh-streaming · port 8000 · [Repo](https://github.com/modelscope/funasr) · [▶️ Demo ↗](https://huggingface.co/spaces/FunAudioLLM/Fun-ASR-Nano) · [📖 Docs ↗](https://www.funasr.com/en/docs/) · [🌐 Site ↗](https://www.funasr.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/funasr/)</sub>

<a name="pocket-tts"></a>
### #&#8288;16 [Pocket TTS](https://github.com/kyutai-labs/pocket-tts) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Nov 2026</sub>

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

<a name="espnet"></a>
### #&#8288;17 [espnet](https://github.com/espnet/espnet) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

**PyTorch toolkit for speech recognition, synthesis, translation and enhancement.**

ESPnet is a PyTorch speech toolkit covering ASR, TTS, speech translation, enhancement, diarization, singing synthesis and speech language models. It provides Kaldi-style run.sh recipes for 200+ corpora and hundreds of pretrained models on Hugging Face. Inference is available through a CLI (espnet transcribe, synthesize, enhance), a Python API and an MCP server.

- **+** One recipe structure and trainer across ASR, TTS, ST, enhancement, SLU and more
- **+** 200+ corpus recipes with run.sh from data prep to scoring
- **+** Hundreds of pretrained models on Hugging Face, including OWSM v4 multilingual ASR
- **+** pip install espnet gives CLI, Python and MCP inference without the training stack
- **−** Full recipe and training setup needs Kaldi-style tooling beyond pip install
- **−** Recipe workflow assumes research familiarity with stages, corpora and configs
- **−** ESPnet1 is unsupported; ESPnet2 and ESPnet3 recipes coexist

<sub>GPU optional · Docker · Needs PyTorch, Kaldi-style tooling (full recipe setup) · Models: OWSM, Whisper, Conformer, E-Branchformer, VITS · [Repo](https://github.com/espnet/espnet) · [▶️ Demo ↗](https://huggingface.co/spaces/espnet/owsm-ctc-v4) · [📖 Docs ↗](https://espnet.github.io/espnet/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/espnet/)</sub>

<a name="kokoro-fastapi"></a>
### #&#8288;18 [Kokoro-FastAPI](https://github.com/remsky/kokoro-fastapi) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · Apache-2.0 · Nov 2026</sub>

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

<a name="realtimestt"></a>
### #&#8288;19 [realtimestt](https://github.com/koljab/realtimestt) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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

<a name="dograh"></a>
### #&#8288;20 [dograh](https://github.com/dograh-hq/dograh) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · BSD-2-Clause · Nov 2026</sub>

**Visual builder for voice agents with telephony, a Vapi and Retell alternative.**

Dograh is a self-hostable platform for building inbound and outbound voice agents in a visual workflow editor, with a browser Test Audio and Test Chat panel. It integrates telephony providers such as Twilio, Vonage, Telnyx, Plivo and Asterisk ARI, and accepts your own LLM, TTS and STT providers. It also ships an MCP server so coding agents can create and edit workflows.

- **+** Built-in telephony: Twilio, Vonage, Telnyx, Plivo, Vobiz, Cloudonix, Asterisk ARI
- **+** Bring your own LLM, TTS, STT, or use the bundled stack with no keys
- **+** MCP server lets coding agents create and edit workflows
- **+** Python and Node SDKs for agent creation and outbound calls
- **−** Quickstart opens a public trycloudflare.com tunnel by default
- **−** Anonymous telemetry is on by default; opt out via ENABLE_TELEMETRY=false
- **−** Signup is enabled by default and must be closed through .env

<sub>Compose · Needs Docker Compose, MinIO or S3-compatible storage, Telephony provider (optional) · Models: Any LLM, TTS and STT provider, Bundled Dograh LLM/TTS/STT stack · port 3010 · [Repo](https://github.com/dograh-hq/dograh) · [▶️ Demo ↗](https://app.dograh.com) · [📖 Docs ↗](https://docs.dograh.com) · [🌐 Site ↗](https://www.dograh.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dograh/)</sub>

<a name="speechbrain"></a>
### #&#8288;21 [speechbrain](https://github.com/speechbrain/speechbrain) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

**PyTorch toolkit for training and running speech and text models.**

SpeechBrain is a PyTorch toolkit with over 200 training recipes on more than 40 datasets, covering ASR, speaker recognition, speech separation and enhancement, TTS, vocoding, diarization and EEG classification. Training is driven by a Python script plus a YAML hyperparameter file, and over 100 pretrained models on HuggingFace load through a short inference API. It targets research and prototyping rather than turnkey deployment.

- **+** Over 200 recipes on 40+ datasets, with a consistent layout across tasks
- **+** Over 100 pretrained models on HuggingFace; ASR inference in three lines of Python
- **+** Single and multi-GPU training, dynamic batching and mixed precision built in
- **+** Over 30 tutorials; Apache-2.0 license permits commercial use
- **−** Library and research toolkit, not a ready-to-run server or app
- **−** No Docker image or HTTP API provided
- **−** Real-time and streaming support is listed only as a future plan

<sub>GPU optional · Needs PyTorch, HuggingFace · Models: Whisper, Wav2Vec2, WavLM, Hubert, GPT2 · [Repo](https://github.com/speechbrain/speechbrain) · [📖 Docs ↗](https://speechbrain.readthedocs.io/en/latest/index.html) · [🌐 Site ↗](https://speechbrain.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speechbrain/)</sub>

<a name="mlx-audio"></a>
### #&#8288;22 [mlx-audio](https://github.com/blaizzy/mlx-audio) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · MIT · Nov 2026</sub>

**Python library for TTS, STT and speech models on Apple Silicon via MLX.**

MLX-Audio runs text-to-speech, speech-to-text, speech-to-speech, voice activity detection/diarization and music generation models on Apple Silicon using Apple's MLX framework. It offers a CLI, a Python API, an OpenAI-compatible REST API with a web interface, and a Swift package for iOS/macOS. Quantization from 3-bit to 8-bit is supported, and the README lists dozens of models such as Kokoro, Qwen3-TTS, Whisper and Parakeet.

- **+** Covers TTS, STT, diarization, enhancement and music generation in one library
- **+** Quantized models (3-bit to 8-bit) for Apple Silicon, with many mlx-community weights
- **+** CLI, Python API, OpenAI-compatible REST server and Swift package
- **+** Supports voice cloning and streaming output on several models
- **−** Apple Silicon only, since it is built on MLX
- **−** Some listed models are large (e.g. 35B MoE, 8B), so memory needs vary widely
- **−** Server and web UI need the extra [server] install; no Docker provided

<sub>GPU required · Needs Apple MLX, Hugging Face model weights · Models: Kokoro, Qwen3-TTS, Whisper, Parakeet, Chatterbox · [Repo](https://github.com/blaizzy/mlx-audio) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlx-audio/)</sub>

<a name="vibe"></a>
### #&#8288;23 [vibe](https://github.com/thewh1teagle/vibe) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · MIT · Nov 2026</sub>

**Desktop app that transcribes audio and video offline with Whisper models.**

Vibe is a Tauri desktop app for macOS, Windows and Linux that transcribes audio and video locally using Whisper, Nemotron 3.5 or Parakeet TDT v3. It supports batch files, microphone and system audio, speaker diarization, and export to SRT, VTT, TXT, HTML, PDF, JSON and DOCX. Summaries can be made through the Claude API or a local Ollama instance.

- **+** Runs transcription fully offline; no audio leaves the device
- **+** GPU acceleration via Vulkan or CoreML on Nvidia, AMD, Intel and Apple
- **+** Exports seven formats including SRT, VTT, DOCX and PDF
- **+** Includes a CLI and an HTTP API with Swagger docs
- **−** Pull requests are limited to a few collaborators
- **−** Cloud summaries need the Claude API; local ones need a separate Ollama install
- **−** Stable timestamps mode is slower because it uses VAD

<sub>GPU optional · Needs Ollama (optional), Claude API (optional) · Models: Whisper, Nemotron 3.5, Parakeet TDT v3 · [Repo](https://github.com/thewh1teagle/vibe) · [📖 Docs ↗](https://github.com/thewh1teagle/vibe/tree/main/docs) · [🌐 Site ↗](https://thewh1teagle.github.io/vibe/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vibe/)</sub>

<a name="fluidaudio"></a>
### #&#8288;24 [fluidaudio](https://github.com/fluidinference/fluidaudio) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Nov 2026</sub>

**Swift SDK for on-device speech, TTS and diarization on Apple devices.**

FluidAudio is a Swift package that runs CoreML-converted audio models on the Apple Neural Engine for macOS and iOS. It covers ASR (Parakeet TDT v3 for 25 European languages plus Japanese, Parakeet EOU for English streaming), TTS (Kokoro, PocketTTS), Silero VAD, and online and offline speaker diarization. Models are hosted on Hugging Face under MIT or Apache 2.0 licenses.

- **+** Inference runs on the Neural Engine, avoiding GPU/MPS and keeping CPU use low
- **+** One SDK covers ASR, TTS, VAD, diarization, speaker embeddings and echo cancellation
- **+** Used by many shipping dictation and meeting apps, listed in a showcase table
- **+** Streaming ASR with end-of-utterance detection and streaming diarization are included
- **−** Apple platforms only (macOS and iOS); no Linux, Windows or Android support
- **−** Requires Swift 6.0+; dropping the ITN engine needs Swift 6.2+
- **−** Streaming Parakeet EOU ASR is English only
- **−** Chatterbox, Paradee and LocalVQE are marked beta

<sub>no GPU · Needs Swift 6.0+, Apple Neural Engine, CoreML, Hugging Face model downloads · Models: Parakeet TDT v3, Parakeet EOU, SenseVoice, Paraformer, Nemotron 3.5 Transcribe Lite · [Repo](https://github.com/fluidinference/fluidaudio) · [📖 Docs ↗](https://docs.fluidinference.com/introduction) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fluidaudio/)</sub>

<a name="edge-tts"></a>
### #&#8288;25 [edge-tts](https://github.com/rany2/edge-tts) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · custom license · Nov 2026</sub>

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

<a name="xiaozhi-esp32-server"></a>
### #&#8288;26 [xiaozhi-esp32-server](https://github.com/xinnan-tech/xiaozhi-esp32-server) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Nov 2026</sub>

**Backend server for xiaozhi-esp32 voice devices with ASR, LLM and TTS pipeline.**

Self-hosted backend for the open-source xiaozhi-esp32 hardware, implemented in Python, Java and Vue per the Xiaozhi communication protocol. It connects devices over WebSocket or MQTT+UDP to configurable ASR, LLM, VLLM and TTS providers, with VAD, voiceprint speaker ID, MCP tool calling and RAGFlow knowledge bases. A minimal mode keeps config in files; the full mode adds a web console with multi-user and multi-agent management.

- **+** Many swappable providers for ASR, TTS, LLM and VLLM, plus any OpenAI-compatible endpoint
- **+** Streaming ASR/TTS configuration; README claims about 2.5 s faster responses since 0.5.2
- **+** Minimal install stores config in files and needs no database
- **+** Supports MCP (client, server, access point), plugins, mem0ai/PowerMem memory and RAGFlow
- **−** Needs ESP32 hardware running xiaozhi-esp32 firmware to be useful
- **−** README says features are incomplete and not security-tested; not for production
- **−** Voiceprint needs a separate voiceprint-api service plus MySQL
- **−** README is primarily Chinese; local FunASR is memory-heavy

<sub>GPU optional · Needs voiceprint-api (optional), MySQL (voiceprint), database (full-module install), RAGFlow (optional), third-party ASR/LLM/TTS APIs · Models: FunASR, SherpaASR, VoskASR, SileroVAD, EdgeTTS · [Repo](https://github.com/xinnan-tech/xiaozhi-esp32-server) · [▶️ Demo ↗](https://2662r3426b.vicp.fun) · [📖 Docs ↗](https://github.com/xinnan-tech/xiaozhi-esp32-server/blob/main/docs/Deployment.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xiaozhi-esp32-server/)</sub>

<a name="pyannote-audio"></a>
### #&#8288;27 [pyannote-audio](https://github.com/pyannote/pyannote-audio) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Nov 2026</sub>

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

<a name="auto-subs"></a>
### #&#8288;28 [auto-subs](https://github.com/tmoroney/auto-subs) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · MIT · Oct 2026</sub>

**Offline subtitle generator with Resolve, Premiere Pro and After Effects integration.**

AutoSubs is a desktop app that transcribes audio or video to timestamped subtitles on-device, using Whisper (GGML), Moonshine, Parakeet, Canary, SenseVoice and other ONNX models downloaded on demand. It labels speakers via diarization, exports SRT or text, and can send styled subtitles into DaVinci Resolve, Premiere Pro and After Effects. A CLI is also available.

- **+** Runs fully offline; models downloaded on demand from an in-app Model Manager
- **+** Many engines: Whisper, Moonshine, Parakeet, Canary, SenseVoice, Cohere, GigaAM, Omni-ASR
- **+** Direct integration with DaVinci Resolve, Premiere Pro and After Effects
- **+** Speaker diarization and a CLI alongside the GUI
- **−** Optional MMS word-alignment weights are CC BY-NC 4.0, noncommercial only
- **−** Mac App Store build of DaVinci Resolve is not supported
- **−** Larger models need much memory, e.g. Whisper large-v3 about 10 GB RAM
- **−** Standalone export lists only SRT, text and clipboard

<sub>RAM ≥ 1 GB · Needs DaVinci Resolve (optional), Adobe Premiere Pro / After Effects (optional) · Models: Whisper (GGML), Moonshine, Parakeet, Canary, SenseVoice · [Repo](https://github.com/tmoroney/auto-subs) · [📖 Docs ↗](https://deepwiki.com/tmoroney/auto-subs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/auto-subs/)</sub>

<a name="speakr"></a>
### #&#8288;29 [Speakr](https://github.com/murtaza-nasir/speakr) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · AGPL-3.0 · Nov 2026</sub>

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

<a name="applio"></a>
### #&#8288;30 [applio](https://github.com/iahispano/applio) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · MIT · Nov 2026</sub>

**Voice conversion tool with a Gradio UI, training and plugin support.**

Applio converts the voice in an audio clip to another voice and includes model training with TensorBoard monitoring. It runs locally through install and run scripts for Windows, Linux and macOS, and opens a Gradio interface in the browser. Plugins extend it, and Colab notebooks are provided with and without the UI.

- **+** Install and run scripts for Windows, Linux and macOS, plus precompiled Windows releases
- **+** Windows updater keeps models, logs, audio, presets and settings across upgrades
- **+** Plugin repository, hosted playground and Colab notebooks with and without UI
- **+** MIT-licensed code and weights, commercial use allowed
- **−** Maintainers say updates will be infrequent: security patches, dependencies, occasional features
- **−** Official version requires accepting a separate Terms of Use in addition to MIT
- **−** Commercial users are advised to contact maintainers to confirm ethical alignment
- **−** Updater script is documented only for compiled Windows releases

<sub>Docker + Compose · Needs Gradio, TensorBoard · [Repo](https://github.com/iahispano/applio) · [▶️ Demo ↗](https://applio.org/playground) · [📖 Docs ↗](https://docs.applio.org) · [🌐 Site ↗](https://applio.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/applio/)</sub>

<a name="voiceink"></a>
### #&#8288;31 [voiceink](https://github.com/beingpax/voiceink) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · custom license · Nov 2026</sub>

**Native macOS dictation app using local speech-to-text models.**

VoiceInk is a Swift macOS app that transcribes speech to text on-device using whisper.cpp, Parakeet via FluidAudio, and GGUF models through transcribe.cpp. It adds global push-to-talk shortcuts, a personal dictionary, and per-app modes that switch settings by the active app or URL. A built-in voice assistant mode is also included.

- **+** Offline transcription; README states audio never leaves the device
- **+** Supports whisper.cpp, Parakeet and GGUF local models, plus SenseVoice Small
- **+** Per-app modes apply settings automatically by app or URL
- **+** Installable via Homebrew cask or buildable from source with BUILDING.md
- **−** macOS 15.0 or later only; no Windows or Linux builds
- **−** Not accepting pull requests; contributions limited to issues
- **−** Auto-updates and priority support only in the paid compiled build

<sub>Needs macOS 15.0+ · Models: whisper.cpp (Whisper), Parakeet (FluidAudio), GGUF via transcribe.cpp, SenseVoice Small · [Repo](https://github.com/beingpax/voiceink) · [🌐 Site ↗](https://tryvoiceink.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voiceink/)</sub>

<a name="openless"></a>
### #&#8288;32 [openless](https://github.com/open-less/openless) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · AGPL-3.0 · Nov 2026</sub>

**Push-to-talk dictation that inserts AI-polished text at the cursor.**

OpenLess is a Tauri 2 and Rust voice-input app for macOS, Windows and Linux, with Android and iOS apps also in the repo. You hold a global hotkey and speak. It transcribes, rewrites the text in a chosen style, and types it at the cursor, falling back to the clipboard if insertion fails. ASR and polish models are bring-your-own: cloud providers, any OpenAI-compatible endpoint, or local Qwen3-ASR on macOS.

- **+** Many ASR and polish providers plus any OpenAI-compatible endpoint; no single vendor required
- **+** Four output modes, including a structured AI-prompt mode, and custom style packs switchable by hotkey
- **+** Streaming insertion to the cursor, with automatic one-shot paste fallback
- **+** Local ASR option: bundled Qwen3-ASR 0.6B/1.7B on macOS, Foundry Local Whisper on Windows
- **−** Linux uses a separate native host and has no in-app updater
- **−** macOS build is ad-hoc signed; needs xattr -cr to bypass Gatekeeper
- **−** Project is in a stability freeze and rejects new-feature PRs
- **−** Windows local ASR is experimental; most providers are cloud services

<sub>Needs Cloud ASR/LLM API credentials (unless using local ASR), Microphone and accessibility permissions · Models: Qwen3-ASR 0.6B/1.7B, Whisper (Foundry Local), sherpa-onnx, OpenAI-compatible endpoints · [Repo](https://github.com/open-less/openless) · [🌐 Site ↗](https://openless.top) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openless/)</sub>

<a name="whisper-asr-webservice"></a>
### #&#8288;33 [whisper-asr-webservice](https://github.com/ahmetoner/whisper-asr-webservice) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Nov 2026</sub>

**REST API server for Whisper speech-to-text with three selectable engines.**

Wraps OpenAI Whisper, faster-whisper or WhisperX behind a REST API on port 9000, with Swagger UI for trying endpoints. It transcribes and translates audio or video via FFmpeg and returns text, JSON, VTT, SRT or TSV. Engine, model size, device and idle unload timeout are set through environment variables.

- **+** Switch between openai_whisper, faster_whisper and whisperx with one environment variable
- **+** Outputs text, JSON, VTT, SRT and TSV, with word-level timestamps
- **+** Speaker diarization available through the WhisperX engine
- **+** Models can unload after an idle timeout to free memory
- **−** Speaker diarization works only with the WhisperX engine
- **−** README documents no authentication or access control for the API
- **−** Separate CPU and GPU image tags; GPU build needs a CUDA-capable host
- **−** Transcription only; no web UI beyond the Swagger docs

<sub>GPU optional · Docker + Compose · Needs Docker, FFmpeg · Models: openai/whisper, faster-whisper, whisperX · port 9000 · [Repo](https://github.com/ahmetoner/whisper-asr-webservice) · [📖 Docs ↗](https://ahmetoner.github.io/whisper-asr-webservice) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisper-asr-webservice/)</sub>

<a name="transcribe-cpp"></a>
### #&#8288;34 [transcribe.cpp](https://github.com/handy-computer/transcribe.cpp) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · MIT · Nov 2026</sub>

**C++ speech-to-text library running many ASR models from GGUF files.**

transcribe.cpp is a C/C++ inference library and CLI for speech-to-text. It loads GGUF models from 16 families (Whisper, Parakeet, Canary, Moonshine, Qwen3-ASR, Voxtral and others) on the ggml runtime, with Metal, Vulkan, CUDA and HIP/ROCm backends plus a tinyBLAS CPU path. It also covers diarization, language ID and VAD models, with Python, TypeScript, Rust and Swift bindings.

- **+** Covers 16 ASR families and 60+ variants through one C API and CLI
- **+** GPU backends for Metal, Vulkan, CUDA and ROCm, plus a CPU path
- **+** Published models are WER-tested against reference implementations, per the README
- **+** Official bindings for Python, TypeScript, Rust and Swift; includes a quantization tool
- **−** Input must be 16 kHz mono WAV; other formats need ffmpeg or sox first
- **−** Built from source with CMake; no Docker image or prebuilt binaries described
- **−** No HTTP server or UI described; it is a library and CLI
- **−** Converter script is documented only for NeMo checkpoints (Parakeet)

<sub>GPU optional · Needs CMake, OpenBLAS (optional), Vulkan SDK, CUDA toolkit or ROCm (optional), ffmpeg or sox (audio conversion) · Models: GGUF, Whisper, Parakeet, Canary, Moonshine · [Repo](https://github.com/handy-computer/transcribe.cpp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transcribe-cpp/)</sub>

<a name="whisperjav"></a>
### #&#8288;35 [whisperjav](https://github.com/meizhong986/whisperjav) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · MIT · Nov 2026</sub>

**Local subtitle generator for Japanese video with scene, VAD and ASR pipelines.**

WhisperJAV turns Japanese adult video audio into SRT or WebVTT subtitles on your own machine. It splits audio into scenes, applies VAD, runs an ASR engine (Faster-Whisper, OpenAI Whisper, Qwen3-ASR, anime-whisper, HF transformers, or experimental CrispASR GGUF models), then applies Japanese-specific cleanup. It also has a two-pass ensemble with merge strategies, a GUI and CLI, and optional translation via Ollama or API providers.

- **+** Two-pass ensemble with seven merge strategies and savable presets
- **+** Japanese post-processing: hallucination removal, sound-only line removal, timing repair
- **+** Scene detection, enhancement, VAD and ASR model are swappable per pass
- **+** Built-in SRT translation via local Ollama or paid APIs, resumable
- **−** Tuned for one domain; results vary with source audio quality
- **−** GGUF CrispASR pipelines are experimental and Japanese only
- **−** Balanced mode rejects --speech-segmenter and other VAD options
- **−** Qwen3-ASR and anime-whisper give no native timestamps; timing comes from the VAD

<sub>GPU optional · Needs FFmpeg, Ollama (optional, for translation) · Models: Faster-Whisper, OpenAI Whisper, Qwen3-ASR, anime-whisper, HuggingFace Whisper/Kotoba · [Repo](https://github.com/meizhong986/whisperjav) · [📖 Docs ↗](https://meizhong986.github.io/WhisperJAV/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisperjav/)</sub>

<a name="yovoice"></a>
### #&#8288;36 [yovoice](https://github.com/leemysw/yovoice) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · Apache-2.0 · Nov 2026</sub>

**Desktop studio for local speech, voice cloning, song and score generation.**

yovoice is a desktop app for macOS, Windows and Linux that generates speech, cloned voices, vocal songs, sound effects and multi-track MIDI scores locally. It runs models such as IndexTTS, Kokoro, VoxCPM2, ACE-Step 1.5 and YuE2 through the audio.cpp C++ engine. It also ships a CLI, an agent skill, and a `yovoice serve` HTTP API and MCP server.

- **+** Covers TTS, cloning, music, stem separation, transcription and MIDI scoring in one app
- **+** Native C++ engine with Metal and bundled CUDA 12.4/13.3 runtimes; no Python setup
- **+** Includes CLI, agent skill and authenticated HTTP API/MCP server
- **+** Optional assistant panel works with Ollama or hosted APIs; keys stay on the machine
- **−** Several model weights (OmniVoice, YuE2, Breeze TTS 2, Voxtral) are non-commercial only
- **−** Linux build does not self-update and uses CPU unless a Vulkan runtime is downloaded
- **−** macOS build supports Apple Silicon only
- **−** Hardware requirements per model are deferred to a separate doc, not the README

<sub>GPU optional · Docker · Needs audio.cpp, WebView2 Runtime (Windows), WebKitGTK 4.1 (Linux) · Models: IndexTTS 2.0/2.5, Qwen3-TTS, VoxCPM2, Kokoro-82M, XTTS v2 · [Repo](https://github.com/leemysw/yovoice) · [📖 Docs ↗](https://github.com/leemysw/yovoice/blob/main/docs/cli.md) · [🌐 Site ↗](https://yovoice.leemysw.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yovoice/)</sub>

<a name="faster-whisper"></a>
### #&#8288;37 [faster-whisper](https://github.com/systran/faster-whisper) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: widely used (90) · Freshness: active (82) · Maintenance: fair (61) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · MIT · Nov 2026</sub>

**Python Whisper speech-to-text library built on CTranslate2.**

Reimplements OpenAI's Whisper inference on CTranslate2, as a Python library installed from PyPI. It runs on CPU or NVIDIA GPU with fp16 or int8 quantization, and supports batched transcription, word-level timestamps and a Silero VAD filter. The README reports 13 minutes of audio on large-v2 in 1m03s at fp16, versus 2m23s for openai/whisper on an RTX 3070 Ti.

- **+** Benchmark: 1m03s vs 2m23s for openai/whisper; int8 uses 2926MB VRAM vs 4708MB
- **+** BatchedInferencePipeline cut large-v2 time to 17s at batch_size=8 in the README benchmark
- **+** Bundles FFmpeg libraries via PyAV, so no system FFmpeg install is needed
- **+** Converts Transformers Whisper models, including fine-tunes; Distil-Whisper checkpoints work
- **−** Library only: no server or UI; an OpenAI-compatible API needs a separate project like speaches
- **−** GPU use needs cuBLAS for CUDA 12 and cuDNN 9; older CUDA requires pinning ctranslate2
- **−** No speaker diarization built in; README points to WhisperX and others
- **−** transcribe returns a lazy generator, so work only runs once you iterate it

<sub>GPU optional · Docker · Needs CTranslate2, PyAV, Silero VAD, cuBLAS (CUDA 12), cuDNN 9 · Models: Whisper (CTranslate2 format), large-v3, turbo, distil-large-v3, Transformers Whisper fine-tunes via converter · [Repo](https://github.com/systran/faster-whisper) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/faster-whisper/)</sub>

<a name="moonshine"></a>
### #&#8288;38 [moonshine](https://github.com/moonshine-ai/moonshine) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: patchy (47) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · custom license · Nov 2026</sub>

**On-device speech-to-text and voice agent toolkit with streaming models.**

Moonshine Voice is a C++ library with bindings for Python, JavaScript/WASM, iOS, Android, macOS, Linux, Windows and Raspberry Pi. It runs streaming speech-to-text models trained by the project, from tiny 1MB models up to ones the README says beat Whisper Large V3 on the Open ASR leaderboard. It also covers text to speech and conversational agents, all on-device without accounts or API keys.

- **+** Runs fully on-device, no account or API keys required
- **+** One library across Python, WASM, mobile, desktop and Raspberry Pi
- **+** Streaming design does work while the user is still speaking
- **+** Model sizes range from about 1MB up to Whisper Large V3-class accuracy
- **−** Legacy non-English non-streaming models use a non-commercial community license
- **−** Repo license detected as NOASSERTION although README states MIT
- **−** No Docker image or live demo link in the README

<sub>no GPU · Models: Moonshine speech-to-text models, Moonshine tiny 1MB models · [Repo](https://github.com/moonshine-ai/moonshine) · [📖 Docs ↗](https://moonshine-voice.readthedocs.io/) · [🌐 Site ↗](https://moonshine.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moonshine/)</sub>

<a name="rtranslator"></a>
### #&#8288;39 [rtranslator](https://github.com/niedev/rtranslator) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (73) · Freshness: active (92) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

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

<a name="whisperlive"></a>
### #&#8288;40 [WhisperLive](https://github.com/collabora/whisperlive) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (50) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · MIT · Nov 2026</sub>

**Near-real-time Whisper transcription server with WebSocket and REST clients.**

WhisperLive runs a WebSocket server that streams microphone, file, RTSP or HLS audio through Whisper and returns partial and committed segments. It supports faster_whisper, TensorRT and OpenVINO backends, plus an OpenAI-style REST endpoint, word timestamps, hotwords, translation and optional diarization. Python clients, browser extensions and an iOS client are included.

- **+** Three backends: faster_whisper, TensorRT and OpenVINO, with an AMD ROCm guide
- **+** Accepts mic, files, RTSP, HLS and raw PCM streams over WebSocket
- **+** Optional batch inference groups multiple client sessions into single GPU calls
- **+** Word timestamps, hotwords, translation and diarization (diarization not on TensorRT)
- **−** TensorRT backend needs separate TensorRT-LLM setup and manual engine builds
- **−** Diarization needs optional pyannote.audio and is unsupported on TensorRT
- **−** Default mode loads a new model per client connection, raising (V)RAM use
- **−** Local microphone use requires PortAudio and Python 3.12

<sub>GPU optional · Docker · Needs PortAudio, Python 3.12, faster-whisper, TensorRT-LLM (tensorrt backend), OpenVINO (openvino backend), pyannote.audio (optional, diarization) · Models: Whisper, faster-whisper (CTranslate2), TensorRT engines, OpenVINO Whisper models · port 9090 · [Repo](https://github.com/collabora/whisperlive) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisperlive/)</sub>

<a name="voxtype"></a>
### #&#8288;41 [voxtype](https://github.com/peteonrails/voxtype) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Nov 2026</sub>

**Push-to-talk voice dictation for Linux that types text at the cursor.**

Voxtype is a Rust daemon for Linux that records while a hotkey is held, transcribes locally, and types the result at the cursor via wtype, dotool, ydotool or the clipboard. It supports nine engines (Whisper, Parakeet, Moonshine, SenseVoice, Paraformer, Dolphin, Omnilingual, Cohere Transcribe, OpenVINO Whisper) with optional Vulkan, CUDA, MIGraphX or Intel NPU acceleration. A meeting mode adds speaker attribution and export.

- **+** Nine local engines switchable with one config line, loaded on demand to save memory
- **+** Compositor keybindings for Hyprland, Sway, River, KDE and GNOME, with typing fallback chain
- **+** Meeting mode exports Markdown, JSON, SRT or VTT; optional LLM post-processing via a pipe
- **+** Packages for AUR, .deb and .rpm; separate CUDA 12, CUDA 13 and Vulkan binaries
- **−** Linux-focused; requires glibc 2.38+ (Ubuntu 24.04+, Fedora 39+, Debian Trixie+)
- **−** Built-in hotkey on X11 needs input group membership, which exposes all keystrokes
- **−** KDE has no key-release events, so only toggle mode works there
- **−** Whisper and ONNX engines ship as separate binaries; Metal and ROCm need source builds

<sub>GPU optional · Docker + Compose · Needs PipeWire or PulseAudio, wtype, dotool or ydotool (fallback), Vulkan runtime (optional), OpenVINO GenAI SDK (optional), Ollama (optional, post-processing and summaries) · Models: Whisper (whisper.cpp), Parakeet, Moonshine, SenseVoice, Paraformer · [Repo](https://github.com/peteonrails/voxtype) · [🌐 Site ↗](https://voxtype.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voxtype/)</sub>

<a name="speech-recognition"></a>
### #&#8288;42 [speech_recognition](https://github.com/uberi/speech_recognition) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · BSD-3-Clause · Nov 2026</sub>

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

<a name="neuralnote"></a>
### #&#8288;43 [neuralnote](https://github.com/damrsn/neuralnote) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · Apache-2.0 · Nov 2026</sub>

**Audio plugin that transcribes audio to multi-instrument MIDI locally in a DAW.**

NeuralNote is a VST3/AU/Standalone plugin that transcribes audio to MIDI inside a DAW using MuScriptor models (small, medium, large) run through a C++/ggml engine. It handles full mixes with notes grouped per instrument, includes a built-in synth for playback, and runs on GPU (Metal, Vulkan) or CPU. Audio stays on the machine; the app goes online only to download models and check for updates.

- **+** Multi-instrument transcription of full mixes, with per-instrument gain, mute and solo in a built-in synth
- **+** Runs locally on Metal, Vulkan or CPU; audio never leaves the machine
- **+** Transcription can be paused and resumed, even after reopening the DAW session
- **+** Engine is a separate MIT-licensed C++/ggml library (muscriptor.cpp) that can be reused
- **−** MuScriptor weights are CC BY-NC 4.0, so non-commercial use only
- **−** Large model runs about 0.5x real time on an M1 Pro GPU; CPU not recommended
- **−** No prebuilt Linux binaries yet; only Clang builds have been tested
- **−** Windows installer is not code signed, and only a few GPUs are tested

<sub>GPU optional · Needs Hugging Face (model download), Vulkan SDK (Windows GPU build), Metal toolchain (macOS build), CMake, C++23 compiler · Models: MuScriptor small (~210 MB), MuScriptor medium (~620 MB), MuScriptor large (~2.7 GB), GGUF · [Repo](https://github.com/damrsn/neuralnote) · [🌐 Site ↗](https://neuralnote.co/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/neuralnote/)</sub>

<a name="vibevoice"></a>
### #&#8288;44 [vibevoice](https://github.com/microsoft/vibevoice) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Needs Hugging Face model weights, vLLM (optional, for serving) · Models: VibeVoice-ASR-7B, VibeVoice-ASR-Streaming, VibeVoice-ASR-BitNet, VibeVoice-Realtime-0.5B, VibeVoice-TTS-1.5B · [Repo](https://github.com/microsoft/vibevoice) · [📖 Docs ↗](https://github.com/microsoft/VibeVoice/blob/main/docs/vibevoice-asr.md) · [🌐 Site ↗](https://microsoft.github.io/VibeVoice) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vibevoice/)</sub>

<a name="voxcpm"></a>
### #&#8288;45 [voxcpm](https://github.com/openbmb/voxcpm) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (95) · Freshness: active (98) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Nov 2026</sub>

**Tokenizer-free multilingual text-to-speech with voice design and cloning.**

VoxCPM2 is a 2B-parameter text-to-speech model on a MiniCPM-4 backbone that generates continuous speech representations with a diffusion autoregressive architecture. It covers 30 languages, creates voices from a text description, clones voices from a short reference clip, and outputs 48kHz audio. It ships as a Python package with a CLI, a web demo, streaming, and LoRA/SFT fine-tuning.

- **+** Voice design from a text description, with no reference audio needed
- **+** Three cloning modes, including transcript-based continuation cloning
- **+** 30 languages plus nine Chinese dialects, no language tag required
- **+** RTF ~0.3 on RTX 4090, ~0.13 with Nano-vLLM or vLLM-Omni
- **−** Documented requirements are CUDA 12.0+ and PyTorch 2.5+; CPU use only via GGUF port
- **−** GGUF on Apple M4 Pro runs at RTF ~1.76, slower than real time
- **−** Production serving relies on separate projects (Nano-vLLM, vLLM-Omni, llama.cpp-omni)
- **−** Python limited to 3.10 through 3.12

<sub>GPU required · Docker + Compose · Needs PyTorch >= 2.5.0, CUDA >= 12.0, Python 3.10-3.12 · Models: VoxCPM2, VoxCPM1.5, VoxCPM-0.5B, GGUF (via llama.cpp-omni) · port 8808 · [Repo](https://github.com/openbmb/voxcpm) · [▶️ Demo ↗](https://huggingface.co/spaces/OpenBMB/VoxCPM-Demo) · [📖 Docs ↗](https://voxcpm.readthedocs.io/en/latest/) · [🌐 Site ↗](https://github.com/OpenBMB/VoxCPM/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voxcpm/)</sub>

<a name="f5-tts"></a>
### #&#8288;46 [F5-TTS](https://github.com/swivid/f5-tts) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Nov 2026</sub>

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

<a name="so-vits-svc-fork"></a>
### #&#8288;47 [so-vits-svc-fork](https://github.com/voicepaw/so-vits-svc-fork) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · custom license · Nov 2026</sub>

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

<a name="funclip"></a>
### #&#8288;48 [funclip](https://github.com/modelscope/funclip) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · MIT · Nov 2026</sub>

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

<a name="realtimetts"></a>
### #&#8288;49 [realtimetts](https://github.com/koljab/realtimetts) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (47) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · MIT · Nov 2026</sub>

**Python library that streams LLM text into low-latency speech across many TTS engines.**

RealtimeTTS is a Python text-to-speech library that takes strings, generators or LLM token streams and plays audio as sentences arrive, writes WAV files, or hands chunks to another process. It wraps about 30 engines (system voices, cloud APIs, local neural models) with fallback between them. The recommended QwenEngine runs Qwen3-TTS natively on an NVIDIA GPU or CPU, and can also run as an OpenAI-compatible HTTP server.

- **+** One TextToAudioStream API over about 30 engines, local and cloud, with fallback engines
- **+** feed() accepts generators, so speech starts while an LLM is still streaming
- **+** Qwen server exposes /v1/audio/speech with voice cloning and a browser studio page
- **+** Qwen CPU engine runs on Windows, Linux x86-64 and macOS without Torch or CUDA
- **−** Each engine has its own license and terms; users must verify them separately
- **−** Local playback needs PyAudio and PortAudio; Linux and macOS require a manual install
- **−** Qwen workflows require Python 3.11 or 3.12; CPU needs AVX2 on x86
- **−** Several engines need external setup such as mpv, a Piper binary or a separate server

<sub>GPU optional · Docker · Needs PortAudio, mpv (some engines), NVIDIA driver (Qwen GPU mode) · Models: Qwen3-TTS, Inflect, Coqui XTTS, Kokoro, Piper · port 8080 · [Repo](https://github.com/koljab/realtimetts) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/realtimetts/)</sub>

<a name="typewhisper-mac"></a>
### #&#8288;50 [typewhisper-mac](https://github.com/typewhisper/typewhisper-mac) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · GPL-3.0 · Nov 2026</sub>

**macOS menu bar dictation with local or cloud speech-to-text and workflows.**

TypeWhisper is a native Swift menu bar app for macOS 14+ that transcribes speech via a global hotkey and pastes the text into the active app. It runs local engines (WhisperKit, Parakeet, Qwen3 ASR, Voxtral, Granite) or cloud APIs (Groq, OpenAI, xAI/Grok), then post-processes text with workflows using local or cloud LLMs. It also offers a local HTTP API, a CLI and a plugin system.

- **+** Many local ASR engines, so audio can stay on the Mac
- **+** Workflows trigger per app, per website or from a hotkey
- **+** Local REST API and CLI for scripting transcription
- **+** Plugin system for LLM, ASR and TTS providers; Homebrew install
- **−** macOS only, 14.0 or later; Apple Silicon recommended
- **−** Speaker detection, iCloud sync and meeting automation are Premium features
- **−** 8 GB RAM minimum; larger models want 16 GB or more
- **−** Apple Intelligence and SpeechAnalyzer require macOS 26 or later

<sub>RAM ≥ 8 GB · GPU optional · Needs macOS 14.0+, Groq, OpenAI or xAI API keys (optional, for cloud engines) · Models: WhisperKit, Parakeet, Qwen3 ASR, Voxtral, Granite Speech · [Repo](https://github.com/typewhisper/typewhisper-mac) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/typewhisper-mac/)</sub>

<a name="minutes"></a>
### #&#8288;51 [minutes](https://github.com/silverstein/minutes) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Nov 2026</sub>

**Local meeting recorder that stores Markdown transcripts and exposes them to MCP clients.**

Minutes records and transcribes meetings, calls, voice memos and dictation on-device, saving each as a Markdown file with YAML frontmatter in ~/meetings/. A Rust CLI (60 commands), a desktop app, and an MCP server (34 tools) let Claude Code, Codex, Cursor or other MCP clients search that history. Summaries and agent queries use a cloud provider only if you choose one.

- **+** Transcription and speaker processing run on-device; audio stays local
- **+** Plain Markdown with YAML frontmatter works with Obsidian, grep and Logseq
- **+** MCP server with 34 tools, plus CLI, TypeScript SDK and Claude Code plugin
- **+** MIT licensed, with a stated no-paid-tier commitment for this repo
- **−** Cloud summarizers or agents receive meeting text once you authorize them
- **−** Linux support is a prebuilt CLI for x86-64 Ubuntu 24.04; older distros build from source
- **−** Opt-in automatic call recording is documented only for Teams and Zoom on macOS
- **−** MCP setup recommends Node.js 22 as an extra dependency

<sub>Needs Node.js 22 (for MCP server), Ollama (optional, dictation local edits) · Models: Local transcription, Ollama, Cloud summarizers (optional) · [Repo](https://github.com/silverstein/minutes) · [📖 Docs ↗](https://github.com/silverstein/minutes/blob/main/docs/features.md) · [🌐 Site ↗](https://useminutes.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/minutes/)</sub>

<a name="fish-speech"></a>
### #&#8288;52 [fish-speech](https://github.com/fishaudio/fish-speech) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (92) · Freshness: recent (70) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · custom license · Oct 2026</sub>

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

<a name="whisperx"></a>
### #&#8288;53 [whisperx](https://github.com/m-bain/whisperx) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: patchy (35) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · BSD-2-Clause · Nov 2026</sub>

**Batched Whisper transcription with word timestamps and speaker diarization.**

WhisperX is a Python CLI and library that transcribes audio with Whisper through a faster-whisper backend, using VAD-based batching. It then aligns words to the audio with wav2vec2 phoneme models and labels speakers with pyannote diarization. The README claims 70x realtime with large-v2 and under 8GB GPU memory at beam_size=5.

- **+** Word-level timestamps via wav2vec2 forced alignment, not just utterance-level timing
- **+** Batched faster-whisper inference; README claims 70x realtime with large-v2
- **+** Runs on CPU with int8 or on GPU; memory tunable via batch size and compute type
- **+** Optional Numba install speeds up alignment on long audio
- **−** Diarization needs a Hugging Face token and accepting the pyannote model agreement
- **−** Words like "2014." or "£13.60" get no timing because the aligner cannot place them
- **−** Overlapping speech is handled poorly; README calls diarization far from perfect
- **−** Each language needs its own wav2vec2 alignment model; untested languages need manual choice

<sub>GPU optional · Needs CUDA toolkit 12.8 (GPU only), ffmpeg, Hugging Face token (diarization), pyannote-audio, faster-whisper · Models: Whisper (large-v2, large-v3, medium, small, base), wav2vec2 alignment models, pyannote speaker-diarization-community-1, silero-vad · [Repo](https://github.com/m-bain/whisperx) · [▶️ Demo ↗](https://replicate.com/victor-upmeet/whisperx) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisperx/)</sub>

<a name="vieneu-tts"></a>
### #&#8288;54 [vieneu-tts](https://github.com/pnnbao97/vieneu-tts) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Nov 2026</sub>

**Vietnamese text-to-speech with voice cloning and an OpenAI-compatible streaming API.**

VieNeu-TTS is a Vietnamese (and bilingual Vietnamese-English) TTS model with a Python SDK, a Gradio web UI and an API server exposing POST /v1/audio/speech. v3 Turbo outputs 48 kHz audio, ships 25 preset voices, clones a voice from a 3–8 s clip, and runs on CPU via ONNX Runtime or on CUDA via PyTorch. LoRA fine-tuning is supported; the newer v4 is proprietary and only available through vieneu.io.

- **+** Torch-free CPU install via ONNX Runtime; RTF about 0.5 on a 12th-gen Core i5
- **+** OpenAI-compatible /v1/audio/speech with streaming; first audio about 115 ms on RTX 3060
- **+** Voice cloning from a 3–8 s clip with automatic denoising, plus 25 preset voices
- **+** LoRA fine-tuning on a single consumer GPU; v3 Nano option for weak CPUs
- **−** Focused on Vietnamese; the README describes no other languages beyond English
- **−** Newer v4 with closer cloning fidelity is proprietary and API-only
- **−** Dubbing, Lecture, Tiktok Reel and Audiobook features are only in the official app
- **−** int8 CPU mode needs VNNI support and can produce garbled audio on older CPUs

<sub>GPU optional · Docker + Compose · Needs ONNX Runtime, PyTorch (GPU path), uv · Models: VieNeu-TTS v3 Turbo, VieNeu-TTS v3 Nano, VieNeu-TTS v2, VieNeu-TTS v1 · port 7860 · [Repo](https://github.com/pnnbao97/vieneu-tts) · [▶️ Demo ↗](https://colab.research.google.com/drive/1b9PO-lcGZX9pEkEwQmu8MfhSnjxKrALW?usp=sharing) · [🌐 Site ↗](https://www.vieneu.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vieneu-tts/)</sub>

<a name="tts-webui"></a>
### #&#8288;55 [tts-webui](https://github.com/rsxdalv/tts-webui) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Nov 2026</sub>

**Web UI that runs many open text-to-speech and audio models.**

TTS WebUI puts dozens of open speech and audio models (Bark, Tortoise, StyleTTS2, MusicGen, RVC, Whisper, Demucs and others) behind a Gradio UI on port 7770 and a React UI on port 3000. Models beyond the core set install as pip-based extensions. An OpenAI-compatible TTS extension serves /v1/audio/speech for clients such as Silly Tavern and OpenWebUI.

- **+** Covers TTS, music generation, voice conversion and transcription models in one interface
- **+** Extension system with in-app marketplace; most models install on demand
- **+** OpenAI-compatible speech endpoint works with Silly Tavern and OpenWebUI
- **+** Installer, Docker Compose and manual install paths are all documented
- **−** Base install is about 10.7 GB, plus 2-8 GB per model
- **−** Combined dependencies trigger pip conflict warnings; README calls them normal
- **−** Python 3.12 not supported; manual install needs 3.10 or 3.11
- **−** Extension updates are manual and need an app restart

<sub>GPU optional · Docker + Compose · Needs Python 3.10/3.11, PyTorch, ffmpeg, NodeJS 22.9.0 (React UI), SQLite · Models: Bark, Tortoise, StyleTTS2, XTTSv2, F5-TTS · port 7770 · [Repo](https://github.com/rsxdalv/tts-webui) · [📖 Docs ↗](https://github.com/rsxdalv/tts-webui/blob/main/documentation/manual_installation.md) · [🌐 Site ↗](https://rsxdalv.github.io/tts-webui-extension-catalog/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tts-webui/)</sub>

<a name="sokuji"></a>
### #&#8288;56 [sokuji](https://github.com/kizuna-ai-lab/sokuji) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Nov 2026</sub>

**Live two-way speech translation for meetings, with cloud or on-device models.**

Sokuji is an Electron desktop app and Chrome/Edge extension that translates speech in real time and routes the translated voice to Zoom, Meet, Teams or any app through a virtual microphone. It supports eight providers, including OpenAI, Gemini, Soniox and Palabra.ai, plus a local mode that runs ASR, translation and TTS on-device via sherpa-onnx, Transformers.js, WASM and WebGPU. Two-way mode auto-detects the speaker's language through Soniox.

- **+** Local mode runs ASR, translation and TTS offline with no API key or GPU
- **+** Ships 44 ASR, 75 translation and 137 TTS models, with one-click download
- **+** Virtual microphone and live subtitles work with any meeting app
- **+** Same features in desktop app and Chrome/Edge extension
- **−** Two-way auto language detection depends on the Soniox cloud provider
- **−** OpenAI-compatible provider is Electron only, not in the extension
- **−** Sends anonymous usage analytics to PostHog
- **−** AGPL-3.0 license restricts closed-source and network-service reuse

<sub>GPU optional · Needs OpenAI, Gemini, Palabra.ai, Soniox or Doubao API (cloud mode only) · Models: sherpa-onnx, Whisper, Opus-MT, Qwen, TranslateGemma · [Repo](https://github.com/kizuna-ai-lab/sokuji) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sokuji/)</sub>

<a name="index-tts"></a>
### #&#8288;57 [IndexTTS](https://github.com/index-tts/index-tts) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Sep 2026</sub>

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

<a name="argmax-oss-swift"></a>
### #&#8288;58 [argmax-oss-swift](https://github.com/argmaxinc/argmax-oss-swift) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Oct 2026</sub>

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

<a name="kittentts"></a>
### #&#8288;59 [kittentts](https://github.com/kittenml/kittentts) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: widely used (83) · Freshness: active (92) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

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

<a name="abogen"></a>
### #&#8288;60 [abogen](https://github.com/denizsafak/abogen) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (60) · Freshness: active (91) · Maintenance: patchy (49) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Nov 2026</sub>

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

<a name="amical"></a>
### #&#8288;61 [amical](https://github.com/amicalhq/amical) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Nov 2026</sub>

**Push-to-talk dictation app for macOS and Windows with local Whisper and Parakeet.**

Amical is an Electron desktop app that transcribes speech and inserts the text at the cursor in any application. It runs Whisper and Parakeet v3 models locally through whisper.cpp, with Metal on macOS and Vulkan on Windows. Optional formatting can use Ollama, an OpenAI-compatible server such as LM Studio, or a hosted provider like OpenRouter with your own key.

- **+** Transcribes offline after a one-time model download; no account required
- **+** Choice of Parakeet v3 and Whisper models from ~78 MB to ~3.1 GB
- **+** Optional LLM formatting via Ollama, LM Studio or OpenRouter
- **+** Vocabulary, snippets, notes and history alongside dictation
- **−** No Linux support; the app has no Linux native helper yet
- **−** Local speech models require macOS 15 or later
- **−** Parakeet v3 covers only 25 European languages
- **−** Building from source needs CMake, Swift or .NET toolchains and submodules

<sub>GPU optional · Needs Ollama (optional), LM Studio or OpenAI-compatible server (optional), OpenRouter (optional) · Models: Whisper (Tiny to Large v3 Turbo), Parakeet v3, Ollama, OpenAI-compatible APIs · [Repo](https://github.com/amicalhq/amical) · [📖 Docs ↗](https://amical.ai/docs) · [🌐 Site ↗](https://amical.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/amical/)</sub>

<a name="porcupine"></a>
### #&#8288;62 [porcupine](https://github.com/picovoice/porcupine) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (54) · Freshness: active (86) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · Apache-2.0 · Nov 2026</sub>

**On-device wake word detection engine with SDKs for many platforms.**

Porcupine is a wake word engine that runs a neural network on-device to detect one or several always-listening keywords in a live audio stream. It ships bindings for Python, .NET, Java, Node, C, Flutter, React Native, Android, iOS, web browsers and microcontrollers (Cortex-M, STM32, Arduino), plus Raspberry Pi. Custom keywords are trained in the Picovoice Console, and every SDK requires an AccessKey from it.

- **+** Runs on Cortex-M, STM32, Arduino, Raspberry Pi Zero through 5, mobile and browsers
- **+** Detects multiple keywords with no added runtime footprint
- **+** Official SDKs for about ten languages and frameworks, each with a runnable demo
- **+** Supports nine languages including Mandarin, Japanese, Korean and German
- **−** Every SDK needs an AccessKey from Picovoice Console, so it is not fully self-contained
- **−** Custom wake words are trained in the hosted Console, not locally
- **−** Built for a few static keywords, not natural-language commands
- **−** Further languages only for commercial customers, case by case

<sub>no GPU · Needs Picovoice AccessKey (Picovoice Console) · Models: Porcupine keyword files (.ppn), porcupine_params.pv model · [Repo](https://github.com/picovoice/porcupine) · [▶️ Demo ↗](https://picovoice.ai/demos/lamp/) · [🌐 Site ↗](https://picovoice.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/porcupine/)</sub>

<a name="openreader"></a>
### #&#8288;63 [OpenReader](https://github.com/richardr1126/openreader) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 600 · MIT · Nov 2026</sub>

**Text-to-speech reader for EPUB, PDF, TXT, MD and DOCX with read-along highlighting.**

OpenReader is a Next.js document reader that narrates EPUB, PDF, TXT, MD and DOCX files with synchronized read-along highlighting. It supports local Kokoro, self-hosted OpenAI-compatible TTS servers and cloud APIs, and exports audiobooks as M4B or MP3. It runs as a self-hosted web app or as a desktop app for macOS, Windows and Linux.

- **+** Word-by-word highlighting via ONNX Whisper alignment; layout-aware PDF parsing with PP-DocLayoutV3
- **+** Many TTS backends: local Kokoro, Kokoro-FastAPI, Orpheus-FastAPI, OpenAI, Replicate, DeepInfra, ElevenLabs
- **+** Audiobook export to M4B or MP3 from the cached playback audio
- **+** Desktop installers need no server, Docker or account; self-host supports SQLite or Postgres
- **−** Full self-host stack involves a compute worker on NATS JetStream and S3-compatible storage
- **−** Available languages depend on the chosen TTS provider and voice
- **−** Native iPhone, iPad and Mac app is a separate TestFlight build

<sub>GPU optional · Docker · Needs NATS JetStream, SeaweedFS or S3-compatible storage, SQLite or Postgres · Models: Kokoro, KittenTTS, Orpheus, Supertonic, OpenAI TTS · [Repo](https://github.com/richardr1126/openreader) · [📖 Docs ↗](https://docs.openreader.richardr.dev/) · [🌐 Site ↗](https://openreader.richardr.dev/download) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openreader/)</sub>

<a name="sensevoice"></a>
### #&#8288;64 [sensevoice](https://github.com/qwenaudio/sensevoice) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.8k · MIT · Sep 2026</sub>

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

<a name="tensorflowasr"></a>
### #&#8288;65 [tensorflowasr](https://github.com/tensorspeech/tensorflowasr) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · Apache-2.0 · Nov 2026</sub>

**Train and run speech recognition models in TensorFlow 2, with TFLite export.**

TensorFlowASR implements ASR architectures in TensorFlow 2: Conformer, ContextNet, RNN Transducer and Streaming Conformer (RNNT loss), plus DeepSpeech2 and Jasper (CTC loss). It includes feature extraction, augmentations, greedy and beam search decoders, and training and testing tutorials. Models can be exported to TFLite and run through an ASRInference/ASREngine API, one-shot or streaming.

- **+** Covers Conformer, ContextNet, RNN-T, DeepSpeech2 and Jasper in one codebase
- **+** TFLite export turns a model into audio-in, text-and-tokens-out
- **+** Streaming inference; one shared ASREngine decodes many sessions, e.g. one per websocket
- **+** Installs with uv; extras for CUDA GPU and a script for Cloud TPU
- **−** TensorFlow-only; no PyTorch or ONNX path mentioned
- **−** Training needs a git clone to get ctc_decoders and rnnt_loss packages
- **−** Python 3.12 or 3.13 required, while the badge still says >=3.8
- **−** Pretrained model results live in per-example folders, not the main README

<sub>GPU optional · Docker + Compose · Needs TensorFlow, tensorflow-text, uv · Models: Conformer, Streaming Conformer, ContextNet, RNN Transducer, DeepSpeech2 · [Repo](https://github.com/tensorspeech/tensorflowasr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tensorflowasr/)</sub>

<a name="elevenlabs-python"></a>
### #&#8288;66 [elevenlabs-python](https://github.com/elevenlabs/elevenlabs-python) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 3.2k · no license · Nov 2026</sub>

**Official Python SDK for the ElevenLabs speech, voice and agents API.**

Python client for the hosted ElevenLabs HTTP API, with sync and async clients. It covers text-to-speech (including streaming), voice search and cloning, and ElevenAgents conversational agents, with helpers to define agent workflows and tools in code. It calls ElevenLabs cloud models and needs an API key; nothing runs locally.

- **+** Sync ElevenLabs and async AsyncElevenLabs clients, plus streaming text-to-speech
- **+** Agent workflows and tools defined as chained code, validated by build() and storable as JSON
- **+** @client_tool builds a tool schema from a typed function; check_client_tools() flags schema drift
- **+** Installs with pip install elevenlabs; README has runnable snippets for each feature
- **−** Requires the hosted ElevenLabs service and an API key; models cannot be self-hosted
- **−** No license detected in the repository metadata
- **−** SDK is generated by Fern, so much of the API surface is generated code
- **−** Changing a shared client tool schema affects already-deployed clients immediately

<sub>no GPU · Needs ElevenLabs API key, ElevenLabs cloud API · Models: eleven_v4, eleven_v4_turbo, eleven_multilingual_v2, eleven_flash_v2_5, scribe_v2 · [Repo](https://github.com/elevenlabs/elevenlabs-python) · [📖 Docs ↗](https://elevenlabs.io/docs/api-reference) · [🌐 Site ↗](https://elevenlabs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/elevenlabs-python/)</sub>

<a name="retrieval-based-voice-conversion-webui"></a>
### #&#8288;67 [retrieval-based-voice-conversion-webui](https://github.com/rvc-project/retrieval-based-voice-conversion-webui) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: widely used (94) · Freshness: active (94) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · MIT · Aug 2026</sub>

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

<a name="omnivoice"></a>
### #&#8288;68 [omnivoice](https://github.com/k2-fsa/omnivoice) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

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

<a name="crisperwhisper"></a>
### #&#8288;69 [crisperwhisper](https://github.com/nyrahealth/crisperwhisper) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · custom license · Nov 2026</sub>

**Whisper-based speech recognition with verbatim or clean output and word-level timings.**

CrisperWhisper 2.0 is a Python package around fine-tuned Whisper models. It transcribes audio either verbatim (fillers, repetitions, stutters, vocal events) or in a cleaned "intended" form, with word-level timestamps. It can also add real disfluencies to an existing clean transcript and handles long audio by conditioning each window on prior text. Inference runs on CTranslate2 (NVIDIA GPU, speculative decoding) or plain PyTorch (CPU, macOS, Windows).

- **+** Verbatim and intended transcripts selectable per call, with a single-pass dual mode on ct2
- **+** Reports about 30 ms mean word-boundary error on TIMIT, lowest in its own comparison table
- **+** Verbatimize inserts real disfluencies into a trusted clean transcript
- **+** Four model sizes and a PyTorch backend, so CPU, macOS and Windows work
- **−** Standard weights are non-commercial research only; commercial use needs a separate license
- **−** Pro models, which add hotword boosting, are commercial-license only
- **−** Forced aligner for the most precise timings supports English only
- **−** Benchmark rankings come from the authors' own benchmark

<sub>GPU optional · Needs CTranslate2, PyTorch, Transformers, Hugging Face model hub · Models: CrisperWhisper 2.0 large, CrisperWhisper 2.0 turbo, CrisperWhisper 2.0 medium, CrisperWhisper 2.0 small, Pro variants (commercial license) · [Repo](https://github.com/nyrahealth/crisperwhisper) · [▶️ Demo ↗](https://www.nyra-labs.com/crisperwhisper) · [📖 Docs ↗](https://github.com/nyrahealth/crisperwhisper/blob/main/DOCS.md) · [🌐 Site ↗](https://www.nyra-labs.com/crisperwhisper) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/crisperwhisper/)</sub>

<a name="montreal-forced-aligner"></a>
### #&#8288;70 [montreal-forced-aligner](https://github.com/montrealcorpustools/montreal-forced-aligner) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Nov 2026</sub>

**Command-line forced aligner that maps speech audio to word and phone timings.**

Montreal Forced Aligner is a Python command-line tool that aligns speech datasets to transcripts using Kaldi, producing time-aligned words and phones. It installs from conda-forge, with Kaldi and Pynini as conda dependencies, and pretrained models live in a separate mfa-models repository. The README points to ReadTheDocs for usage and cites an MFA 3.0 paper.

- **+** Built on Kaldi, so alignment can be run with your own trained models
- **+** Pretrained models are maintained in the separate mfa-models repository
- **+** Installs from conda-forge as a single package
- **+** MIT license with user guide, API reference and changelog on ReadTheDocs
- **−** Command-line only, no GUI or web interface
- **−** Needs conda for Kaldi and Pynini, so plain pip is not enough
- **−** Output is alignment data, not transcription or speech synthesis

<sub>Docker · Needs conda, Kaldi, Pynini, OpenFst · Models: Kaldi acoustic models, MFA pretrained models · [Repo](https://github.com/montrealcorpustools/montreal-forced-aligner) · [📖 Docs ↗](http://montreal-forced-aligner.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/montreal-forced-aligner/)</sub>

<a name="chattts"></a>
### #&#8288;71 [chattts](https://github.com/2noise/chattts) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (94) · Freshness: recent (60) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · AGPL-3.0 · Apr 2026</sub>

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

<a name="whisper"></a>
### #&#8288;72 [whisper](https://github.com/openai/whisper) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: widely used (99) · Freshness: recent (72) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 114k · MIT · Aug 2026</sub>

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

<a name="cosyvoice"></a>
### #&#8288;73 [cosyvoice](https://github.com/qwenaudio/cosyvoice) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: widely used (88) · Freshness: recent (65) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · Apache-2.0 · May 2026</sub>

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

<sub>Docker · Needs Python 3.10, conda, sox, vLLM (optional), TensorRT-LLM (optional), ttsfrd (optional) · Models: Fun-CosyVoice3-0.5B-2512, CosyVoice2-0.5B, CosyVoice-300M, CosyVoice-300M-SFT, CosyVoice-300M-Instruct · port 50000 · [Repo](https://github.com/qwenaudio/cosyvoice) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cosyvoice/)</sub>

<a name="vosk-api"></a>
### #&#8288;74 [vosk-api](https://github.com/alphacep/vosk-api) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: widely used (81) · Freshness: recent (70) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

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

<a name="voice-pro"></a>
### #&#8288;75 [voice-pro](https://github.com/abus-aikorea/voice-pro) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (79) · Freshness: active (88) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · GPL-3.0 · Jul 2026</sub>

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

<a name="audio8-tts"></a>
### #&#8288;76 [audio8_tts](https://github.com/edge0-ai/audio8_tts) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (34) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · Apache-2.0 · Nov 2026</sub>

**Compact zero-shot voice-cloning text-to-speech models, 0.6B and 0.1B.**

Audio8 TTS provides two families of text-to-speech models with zero-shot voice cloning: 0.6B Realistic Air (23 languages) and 0.1B Preview (mainly Chinese and English). Inference runs through a Python script on a CUDA GPU, a llama.cpp/GGUF C++ runtime for Realistic Air, an ONNX INT8 runtime for CPU with the 0.1B model, or SGLang Omni with an OpenAI-compatible speech API.

- **+** Several runtimes: Python, llama.cpp/GGUF, ONNX INT8 on CPU, SGLang Omni
- **+** Realistic Air covers 23 languages and clones a voice from reference audio plus transcript
- **+** 0.6B models and repository code are Apache-2.0
- **+** Includes supervised fine-tuning guide and live listening demos
- **−** 0.1B checkpoint uses a community license; companies at US$2M revenue or more need a paid license
- **−** No ONNX export for Realistic Air; ONNX INT4 is Preview 0.6B only
- **−** Per-language quality varies; benchmarks do not cover every supported language
- **−** macOS needs CPU (Metal experimental); Windows build steps untested

<sub>GPU optional · Needs Python 3.10+, PyTorch (via requirements.txt), llama.cpp (patched, for GGUF), SGLang Omni (optional serving), ONNX Runtime (CPU path) · Models: Audio8-TTS-Realistic-Air 0.6B, Audio8-TTS-Preview 0.6B, Audio8-TTS-Preview 0.1B, GGUF F32, ONNX INT8 · [Repo](https://github.com/edge0-ai/audio8_tts) · [▶️ Demo ↗](https://edge0-ai.github.io/Audio8_TTS/realistic-0.6b/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/audio8-tts/)</sub>

<a name="rhvoice"></a>
### #&#8288;77 [rhvoice](https://github.com/rhvoice/rhvoice) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · GPL-2.0 · Nov 2026</sub>

**Offline statistical speech synthesizer with SAPI5, Speech Dispatcher and Android support.**

RHVoice is a C++ text-to-speech engine that uses HTS-based statistical parametric synthesis. Voices are built from natural speech recordings and stored as small statistical models, so footprints stay low. It started with Russian and now covers about a dozen languages, and plugs into SAPI5, Speech Dispatcher, Android TTS and NVDA.

- **+** Integrates with SAPI5, Speech Dispatcher, Android TTS APIs and the NVDA screen reader
- **+** Small voice footprint because only statistical models are stored locally
- **+** Covers Russian, Ukrainian, Polish, Georgian, Esperanto, Kyrgyz, Tatar and more
- **+** Installable on Android from F-Droid or Google Play
- **−** Less natural than concatenative synthesizers, per the README
- **−** Not a neural TTS engine; no voice cloning or neural models mentioned
- **−** Adding a new language needs resources that may be hard to find
- **−** Windows binaries and Linux build steps are in the docs, not the README

<sub>no GPU · Needs HTS, SAPI5, Speech Dispatcher, NVDA · Models: HTS statistical parametric voices · [Repo](https://github.com/rhvoice/rhvoice) · [▶️ Demo ↗](https://data2data.ru/tts/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rhvoice/)</sub>

<a name="wenet"></a>
### #&#8288;78 [wenet](https://github.com/wenet-e2e/wenet) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (55) · Freshness: recent (70) · Maintenance: fair (51) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · Apache-2.0 · Oct 2026</sub>

**Speech recognition toolkit for training and deploying ASR models.**

WeNet is a PyTorch toolkit for end-to-end speech recognition, with training recipes, a pip package for transcription and a C++ runtime for deployment. The pip package offers a CLI and Python API with Paraformer, FireRed and WeNetSpeech models for Chinese and Whisper large-v3 variants for English. Language model integration uses WFST decoding, which needs the runtime built from source.

- **+** Covers training, Python inference and a separate C++ runtime in one repository
- **+** Supports both streaming and non-streaming recognition models
- **+** Huawei Ascend NPU install path documented alongside CUDA
- **+** Pretrained models and a HuggingFace demo are linked
- **−** CLI runs on CPU by default; GPU needs an explicit --device cuda flag
- **−** Unpinned torch dependency can install a build that mismatches the GPU driver
- **−** Last tagged release is 2024-05-23; pip install pulls from git
- **−** Runtime and LM decoding need a manual cmake build; no Docker image

<sub>GPU optional · Needs PyTorch, torchaudio, sox, conda, CUDA 12.1 (recommended for training), cmake 3.14+ (runtime build) · Models: paraformer, firered, wenetspeech, whisper-large-v3, whisper-large-v3-turbo · [Repo](https://github.com/wenet-e2e/wenet) · [▶️ Demo ↗](https://huggingface.co/spaces/wenet/wenet_demo) · [📖 Docs ↗](https://wenet-e2e.github.io/wenet) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/wenet/)</sub>

<a name="elatoai"></a>
### #&#8288;79 [elatoai](https://github.com/akdeb/elatoai) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · custom license · Nov 2026</sub>

**Firmware and servers for realtime voice AI on ESP32 devices and toys.**

ElatoAI connects an ESP32-S3 running Arduino/PlatformIO firmware to speech-to-speech providers over secure WebSockets, using Deno Edge or Cloudflare Workers as the relay. A Next.js web app handles agent personalities, voices, device registration and conversation history, backed by Supabase. Supported providers include OpenAI Realtime, Gemini Live, xAI Grok, ElevenLabs, Hume EVI-4 and Boson Higgs, plus a FastAPI pipeline option.

- **+** Supports six speech-to-speech providers, plus Cloudflare STT/LLM/TTS and FastAPI pipelines
- **+** Covers the full stack: ESP32 firmware, edge server, Next.js app and Supabase schema
- **+** Runs without PSRAM; includes OTA updates, captive-portal WiFi setup and Opus audio at 12kbps
- **+** Tool calling from the device to edge functions
- **−** Depends on cloud provider APIs; the local-model variant lives in a separate repository
- **−** No speech interruption detection on the ESP32
- **−** 2-3s cold start; conversations tested only up to about 17 minutes
- **−** Needs ESP32-S3 hardware plus Supabase, Vercel and an edge host to run

<sub>no GPU · Needs Supabase, Deno Edge or Cloudflare Workers, Vercel, ESP32-S3, Voice provider API key · Models: OpenAI Realtime, Gemini Live, xAI Grok Voice Agent, ElevenLabs Conversational AI, Hume EVI-4 · [Repo](https://github.com/akdeb/elatoai) · [▶️ Demo ↗](https://www.youtube.com/watch?v=o1eIAwVll5I) · [📖 Docs ↗](https://www.elatoai.com/docs) · [🌐 Site ↗](https://elatoai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/elatoai/)</sub>

<a name="breeze-tts"></a>
### #&#8288;80 [breeze-tts](https://github.com/breezeblue-ai/breeze-tts) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Nov 2026</sub>

**Open-weight English and Chinese TTS with voice cloning, design and streaming.**

Breeze TTS 2 is a PyTorch text-to-speech model with inference code. It supports voice cloning from reference audio, voice design from a text description, and voice direction that steers a cloned voice. It ships a CLI and a single-concurrency HTTP API with streaming and batch endpoints that return 24 kHz PCM. Code is Apache-2.0, but model weights and self-hosted outputs are research and non-commercial only.

- **+** Clone, instruction-based voice design and directed cloning, plus inline events like (laugh)
- **+** Streaming API returns 24 kHz PCM; README reports under 40 ms time to first audio on H100
- **+** Eager inference needs about 7.7 GiB GPU memory; optional --fast-all CUDA Graph path
- **+** Batch endpoint accepts up to 128 texts per request
- **−** Weights and self-hosted outputs are non-commercial only, despite Apache-2.0 code
- **−** Requires Linux and an NVIDIA CUDA GPU; no CPU path documented
- **−** Only English and Chinese are supported
- **−** API serves one request at a time; a concurrent request returns 409

<sub>GPU required · Docker · Needs Python 3.10+, PyTorch, CUDA-capable NVIDIA GPU, Breeze TTS 2 checkpoint (Hugging Face) · Models: Breeze TTS 2 (safetensors checkpoint) · port 7860 · [Repo](https://github.com/breezeblue-ai/breeze-tts) · [🌐 Site ↗](https://breezeblue.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/breeze-tts/)</sub>

<a name="emotivoice"></a>
### #&#8288;81 [emotivoice](https://github.com/netease-youdao/emotivoice) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · Apache-2.0 · Sep 2026</sub>

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

<a name="silero-models"></a>
### #&#8288;82 [silero-models](https://github.com/snakers4/silero-models) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · custom license · Oct 2026</sub>

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

<a name="opensuperwhisper"></a>
### #&#8288;83 [opensuperwhisper](https://github.com/starmel/opensuperwhisper) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (40) · Freshness: active (93) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · MIT · Sep 2026</sub>

**macOS dictation app that transcribes with Whisper or Parakeet models.**

OpenSuperWhisper is a Swift macOS app that records audio and transcribes it with either whisper.cpp or Parakeet (via FluidAudio). It is triggered by global shortcuts, single modifier keys or a mouse button, with a hold-to-record mode. It also transcribes dropped audio files through a queue and lets you pick the microphone from the menu bar.

- **+** Two engines, Whisper and Parakeet, with models downloadable inside the app
- **+** Flexible triggers: key combos, single modifier keys such as Fn, or a thumb mouse button
- **+** Hold-to-record mode and drag-and-drop file transcription with a queue
- **+** Installable with Homebrew; MIT licensed
- **−** Apple Silicon only; Intel macOS support is an open TODO
- **−** No streaming transcription yet; listed as a TODO
- **−** No custom dictionary or keyword boosting yet
- **−** Building from source needs cmake, Rust, Ruby and git submodules

<sub>Needs macOS on Apple Silicon (ARM64) · Models: Whisper (whisper.cpp .bin), Parakeet (FluidAudio) · [Repo](https://github.com/starmel/opensuperwhisper) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opensuperwhisper/)</sub>

<a name="dsnote"></a>
### #&#8288;84 [dsnote](https://github.com/mkiol/dsnote) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MPL-2.0 · Nov 2026</sub>

**Offline speech-to-text, text-to-speech and translation notes app for Linux.**

Speech Note is a Linux and Sailfish OS desktop app for dictating, reading aloud and translating notes entirely offline. It wraps many engines: Whisper, Faster Whisper, Vosk, Coqui STT, april-asr and Qwen3-ASR for speech-to-text; Piper, Kokoro, espeak-ng, RHVoice and F5-TTS among others for speech output; and Bergamot for translation. Model checkpoints are not bundled and are downloaded through a built-in model browser.

- **+** Combines STT, TTS and machine translation in one app, all processed locally
- **+** Supports many engines, including Whisper, Vosk, Piper, Kokoro and Bergamot
- **+** Built-in model browser downloads checkpoints per language on demand
- **+** Distributed through Flathub as a Flatpak
- **−** Targets Linux and Sailfish OS only; no Windows or macOS builds mentioned
- **−** Model checkpoints are not included, so models must be downloaded after install
- **−** Language coverage varies widely by engine; many languages lack some engines
- **−** Limited to speech and translation; no LLM chat or agent features

<sub>Needs Flatpak · Models: Whisper, Faster Whisper, Vosk, Coqui STT, april-asr · [Repo](https://github.com/mkiol/dsnote) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dsnote/)</sub>

<a name="auk"></a>
### #&#8288;85 [auk](https://github.com/tencent-hunyuan/auk) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · custom license · Nov 2026</sub>

**1.5B speech model for TTS, speech editing, enhancement and separation.**

AuK is a 1.5B speech foundation model from Tencent Hunyuan that handles zero-shot and instruction TTS, content, acoustic and paralinguistic editing, enhancement and source separation through one natural-language instruction interface. It ships as a Python package with an `auk-infer` CLI, a Gradio demo, ComfyUI nodes and a Python API, in a base variant and a 4-step distilled AuK-Flash variant. It needs Qwen2.5-Omni-3B as a separate encoder.

- **+** One instruction interface covers TTS, editing, enhancement and separation tasks
- **+** AuK-Flash uses 4 fixed steps with CFG=0 for faster generation
- **+** Runs via CLI, Gradio, ComfyUI, vLLM-Omni, SGLang-Omni, audio.cpp GGUF and MLX
- **+** Fine-tuning and distillation pipelines included; weights on Hugging Face and ModelScope
- **−** Peak VRAM about 25 GiB in bf16; CPU offload lowers it to about 17 GiB
- **−** Requires a separate Qwen2.5-Omni-3B download; Qwen3-Omni is not supported
- **−** Prompt Enhancer needs an external OpenAI-compatible LLM API
- **−** License not identified by detection (NOASSERTION); no tagged release

<sub>GPU required · Needs PyTorch, Qwen2.5-Omni-3B, Gradio (optional), OpenAI-compatible LLM (Prompt Enhancer, optional), SenseVoiceSmall or Tencent Cloud ASR (optional) · Models: AuK, AuK-Flash, Qwen2.5-Omni-3B · port 7860 · [Repo](https://github.com/tencent-hunyuan/auk) · [▶️ Demo ↗](https://huggingface.co/spaces/tencent/AuK) · [🌐 Site ↗](https://auk-project.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/auk/)</sub>

<a name="xiaozhi-esp32-server-java"></a>
### #&#8288;86 [xiaozhi-esp32-server-java](https://github.com/joey-zhou/xiaozhi-esp32-server-java) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (9) · Freshness: active (97) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · Nov 2026</sub>

**Java backend and admin console for Xiaozhi ESP32 voice devices.**

Java server for Xiaozhi ESP32 hardware, split into two Spring Boot processes: an admin backend (port 8091, REST API, users, devices, OTA) and a dialogue service (port 8092, WebSocket/MQTT audio streams and the STT, LLM, TTS pipeline). It includes a Vue web console and integrates OpenAI, Zhipu, Xunfei, Ollama, Dify and Coze, plus local and cloud speech engines. Data is stored in MySQL, Redis and Qdrant.

- **+** Dialogue and admin run as separate processes; dialogue instances register with the server and scale out
- **+** Local STT/TTS via sherpa-onnx and Vosk, plus Edge TTS and several cloud providers
- **+** README includes a 100-device concurrency benchmark on 8 cores / 8 GB
- **+** Covers OTA rollout, MQTT wake-up, voiceprint recognition, RAG, long-term memory and MCP
- **−** Some features are not open source; a commercial edition exists
- **−** README and docs are mostly in Chinese
- **−** Needs MySQL, Redis and downloaded model/native library files before first run
- **−** No LLM API key is bundled; you must supply your own to chat

<sub>Compose · Needs MySQL 8.0, Redis 7, Qdrant, JDK 21 (source build), Node 22 (source build) · Models: OpenAI, Zhipu AI, Xunfei Spark, Volcengine Ark, Ollama · port 8084 · [Repo](https://github.com/joey-zhou/xiaozhi-esp32-server-java) · [📖 Docs ↗](https://github.com/joey-zhou/xiaozhi-esp32-server-java/blob/main/docs/DOCKER.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xiaozhi-esp32-server-java/)</sub>

<a name="chatterbox"></a>
### #&#8288;87 [chatterbox](https://github.com/resemble-ai/chatterbox) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: widely used (90) · Freshness: recent (71) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · MIT · Nov 2026</sub>

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

<a name="epub-to-audiobook"></a>
### #&#8288;88 [epub_to_audiobook](https://github.com/p0n1/epub_to_audiobook) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: patchy (41) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · MIT · Oct 2026</sub>

**Converts EPUB books to per-chapter MP3 audiobooks using cloud or local TTS.**

Command-line tool, with a Gradio web UI, that splits an EPUB into chapters and renders each as an MP3 through Azure TTS, OpenAI TTS, Edge TTS or a local Piper executable. Chapter titles are written as metadata for import into Audiobookshelf. It also has a preview mode that prints character counts, regex search-and-replace for pronunciation, parallel workers and chapter range selection.

- **+** Supports Azure, OpenAI, Edge (no key) and Piper local TTS from one CLI
- **+** Preview mode prints per-chapter character counts before any paid TTS call
- **+** Regex search-and-replace file fixes pronunciations and abbreviations
- **+** Parallel chapters via --worker_count; titles embedded for Audiobookshelf
- **−** WebUI has no authentication and should not be exposed to the internet
- **−** Azure and OpenAI voices need paid API keys; Piper needs a separate install
- **−** Chapter title extraction can fail on EPUBs with unusual structure
- **−** Kokoro works only via a local OpenAI-compatible endpoint with a dummy API key

<sub>no GPU · Docker + Compose · Needs Azure Speech key (Azure TTS), OpenAI API key (OpenAI TTS), Piper executable and voice models (Piper), Audiobookshelf (optional) · Models: Azure TTS, OpenAI TTS, Edge TTS, Piper, Kokoro (via OpenAI-compatible endpoint) · port 7860 · [Repo](https://github.com/p0n1/epub_to_audiobook) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/epub-to-audiobook/)</sub>

<a name="whisper-ctranslate2"></a>
### #&#8288;89 [whisper-ctranslate2](https://github.com/softcatala/whisper-ctranslate2) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · Nov 2026</sub>

**Faster-whisper command line client that mirrors the OpenAI Whisper CLI.**

whisper-ctranslate2 is a Python command line tool for transcribing and translating audio with Whisper models, running on CTranslate2 and faster-whisper. It keeps the OpenAI Whisper CLI options and adds batched inference, int8/float16 quantization, a Silero VAD filter, live microphone transcription and pyannote-based speaker labels. It runs on x86-64 and ARM64 CPUs or NVIDIA GPUs.

- **+** Same command line as OpenAI Whisper, so migrating scripts is simple
- **+** Batched inference and int8 quantization for faster runs on CPU or GPU
- **+** Loads your own fine-tuned Whisper models in CTranslate2 format
- **+** Prebuilt Docker image includes small, medium and large-v2 models
- **−** Translation targets English only
- **−** Diarization works at segment level and needs a Hugging Face token plus pyannote.audio 4.0
- **−** GPU use requires cuBLAS and cuDNN 9 for CUDA 12 installed separately
- **−** Batched mode ignores several options such as condition_on_previous_text

<sub>GPU optional · Docker · Needs CTranslate2, faster-whisper, pyannote.audio (diarization), Silero VAD, NVIDIA cuBLAS and cuDNN 9 (GPU) · Models: Whisper (CTranslate2 format), Fine-tuned Whisper models · [Repo](https://github.com/softcatala/whisper-ctranslate2) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisper-ctranslate2/)</sub>

<a name="nomily-app"></a>
### #&#8288;90 [nomily-app](https://github.com/nomily-ai/nomily-app) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · custom license · Nov 2026</sub>

**Voice recorder companion that transcribes and summarizes with your own API keys.**

Nomily AI is a bring-your-own-key voice recording workflow for the Vobot V05E BLE recorder, Apple Watch and audio imported on iPhone. It transcribes through Azure Speech or a local faster-whisper-compatible endpoint, then produces summaries, titles and translations via OpenAI, Anthropic, Gemini, OpenRouter, Ollama or a custom OpenAI-compatible endpoint. This repository is only the project entry point; the native clients live in nomily-ios and nomily-android.

- **+** Local ASR reference server included (Python 3.10+, ports 12300/12301) plus Ollama support for LAN-only use
- **+** Wide LLM provider choice, including any custom OpenAI-compatible endpoint
- **+** Native SwiftUI and Jetpack Compose clients, not a cross-platform wrapper
- **+** Azure transcription supports speaker diarization for up to 10 speakers
- **−** Source-available Nomily Small Team License, not OSI open source; teams over 10 need a paid licence
- **−** This repo has no installable client; builds happen in separate iOS and Android repos
- **−** No shared self-hosted sync, RAG or MCP; Azure Speech is needed for diarization
- **−** Primary recorder input is the Vobot V05E; other recorders have no compatibility claim

<sub>Needs Azure Speech or local faster-whisper-compatible ASR endpoint, LLM provider API key or Ollama, ffmpeg and Python 3.10+ (local ASR server), Vobot V05E recorder (optional) · Models: Azure Speech, faster-whisper, OpenAI, Anthropic, Gemini · [Repo](https://github.com/nomily-ai/nomily-app) · [▶️ Demo ↗](https://geekis.com/demo/) · [📖 Docs ↗](https://github.com/nomily-ai/nomily-app/blob/main/examples/local-asr-server/README.md) · [🌐 Site ↗](https://geekis.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nomily-app/)</sub>

<a name="moss-tts-nano"></a>
### #&#8288;91 [moss-tts-nano](https://github.com/openmoss/moss-tts-nano) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · Apache-2.0 · Sep 2026</sub>

**0.1B multilingual text-to-speech model with voice cloning that runs on CPU.**

MOSS-TTS-Nano is a 0.1B-parameter autoregressive TTS model (audio tokenizer plus LLM) that outputs 48 kHz stereo audio in 20 languages. It supports voice cloning from a reference clip and streaming generation. It runs through Python scripts, a packaged CLI, a FastAPI web demo, or an ONNX Runtime CPU path without PyTorch. Fine-tuning code and an Android ONNX example are included.

- **+** Streaming generation runs on a 4-core CPU; ONNX path needs no PyTorch
- **+** Voice cloning from a reference clip, with automatic chunking for long text
- **+** Covers 20 languages; ships fine-tuning code and an Android ONNX example
- **+** Optional CUDA through onnxruntime-gpu; weights on Hugging Face and ModelScope
- **−** Bundled web app is a local demo; OpenAI-compatible endpoint needs vLLM-Omni
- **−** Install can fail on pynini and WeTextProcessing, requiring manual steps
- **−** No Docker or compose files in the repository
- **−** No tagged releases published

<sub>GPU optional · Needs Python 3.12, PyTorch, ONNX Runtime, pynini, WeTextProcessing · Models: MOSS-TTS-Nano (0.1B, Hugging Face), MOSS-TTS-Nano-100M-ONNX, MOSS-Audio-Tokenizer-Nano · port 18083 · [Repo](https://github.com/openmoss/moss-tts-nano) · [▶️ Demo ↗](https://huggingface.co/spaces/OpenMOSS-Team/MOSS-TTS-Nano) · [🌐 Site ↗](https://openmoss.github.io/MOSS-TTS-Nano-Demo/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moss-tts-nano/)</sub>

<a name="gpt-sovits"></a>
### #&#8288;92 [GPT-SoVITS](https://github.com/rvc-boss/gpt-sovits) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35 · MIT · Nov 2026</sub>

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

<a name="irodori-tts"></a>
### #&#8288;93 [irodori-tts](https://github.com/aratako/irodori-tts) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Nov 2026</sub>

**Japanese flow-matching TTS with voice cloning and caption-based voice design.**

Training and inference code for Irodori-TTS, a Japanese text-to-speech model that uses a rectified-flow diffusion transformer over DACVAE latents and outputs 48kHz audio. It clones voices zero-shot from up to 120 seconds of reference audio, accepts caption text for voice design, and predicts output duration automatically. It ships a CLI and Gradio UIs, plus full fine-tuning, LoRA, speaker inversion and MeanFlow distillation.

- **+** Covers inference and training: full fine-tune, LoRA, speaker inversion, MeanFlow distillation
- **+** Zero-shot cloning from multiple reference clips, plus caption-only voice design
- **+** Quantized checkpoints (int8, int4, fp8) and a 4-step MeanFlow variant reduce inference cost
- **+** uv extras for CUDA 12.8, ROCm, Intel XPU, and CPU or macOS MPS
- **−** Released checkpoints use a Japanese codec; other languages are not documented
- **−** No Docker or compose files; setup relies on uv and PyTorch backend extras
- **−** OpenAI-compatible API server is a separate repository
- **−** v4-Large is described as forthcoming; v1 checkpoints are incompatible with v2 and later

<sub>GPU optional · Needs uv, PyTorch, Hugging Face Hub, DACVAE, SilentCipher · Models: Irodori-TTS-v4.1-Small, Irodori-TTS-v4.1-Small-MF, Irodori-TTS-v4.1-Small-Quantized, Irodori-TTS v2/v3 checkpoints, safetensors · port 7860 · [Repo](https://github.com/aratako/irodori-tts) · [▶️ Demo ↗](https://huggingface.co/spaces/Aratako/Irodori-TTS-v4.1-Small-Demo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/irodori-tts/)</sub>

<a name="whisper-diarization"></a>
### #&#8288;94 [whisper-diarization](https://github.com/mahmoudashraf97/whisper-diarization) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (57) · Freshness: active (95) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · BSD-2-Clause · Aug 2026</sub>

**Whisper transcription with per-sentence speaker labels using NeMo diarization.**

A Python pipeline that transcribes audio with Whisper and labels the speaker of each sentence. It extracts vocals with Demucs, aligns timestamps with ctc-forced-aligner, then uses NeMo MarbleNet for VAD and TitaNet for speaker embeddings. It runs from the command line via diarize.py, and a Colab notebook is provided.

- **+** Combines Whisper, Demucs vocal separation, MarbleNet VAD and TitaNet embeddings in one script
- **+** Forced alignment and punctuation realignment reduce speaker errors from timestamp drift
- **+** Colab notebook available for trying it without a local setup
- **+** CLI flags for model, language, device, batch size and disabling stem separation
- **−** Overlapping speech is not handled, per the README's known limitations
- **−** Whisper and NeMo parameters are hardcoded in diarize.py and helpers.py
- **−** diarize_parallel.py is experimental and wants 10 GB or more of VRAM
- **−** Needs ffmpeg and Cython installed before the requirements will install

<sub>GPU optional · Needs Python >= 3.10, ffmpeg, Cython, NVIDIA NeMo, Demucs, ctc-forced-aligner · Models: Whisper (default medium.en), Faster Whisper, NeMo MarbleNet, NeMo TitaNet · [Repo](https://github.com/mahmoudashraf97/whisper-diarization) · [▶️ Demo ↗](https://colab.research.google.com/github/MahmoudAshraf97/whisper-diarization/blob/main/Whisper_Transcription_%2B_NeMo_Diarization.ipynb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisper-diarization/)</sub>

<a name="moss-transcribe-diarize"></a>
### #&#8288;95 [moss-transcribe-diarize](https://github.com/openmoss/moss-transcribe-diarize) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (30) · Freshness: active (100) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · Apache-2.0 · Oct 2026</sub>

**Speech model that transcribes multi-speaker audio with speaker labels and timestamps.**

A 0.9B-parameter audio model (Qwen3-0.6B-style decoder with a Whisper-Medium encoder) that transcribes long recordings and labels speakers in one pass. It emits `[start][Sxx]text[end]` segments. It runs through Transformers, SGLang Omni or vLLM, which expose an OpenAI-compatible /v1/audio/transcriptions endpoint. The repo also ships a local subtitle web app and CLI that export JSON, SRT and ASS.

- **+** One model outputs text, timestamps and speaker labels, so no separate VAD or diarization stage
- **+** Supports 50+ languages; reports lower cpCER than listed baselines on AISHELL-4 and Movies
- **+** Serves via SGLang Omni or vLLM with an OpenAI-style transcription endpoint
- **+** Includes a local subtitle web app and batch CLI with SRT/ASS export and FFmpeg burn-in
- **−** Stronger Pro model is only available in the hosted playground, not as open weights
- **−** SGLang Omni targets CUDA 13; vLLM needs a pinned nightly wheel
- **−** Default prompt is in Chinese; long audio needs a raised max_new_tokens
- **−** Benchmark comparisons are self-reported, and some baseline results are missing

<sub>GPU optional · Needs Python 3.12, PyTorch, Transformers 5.x, SGLang Omni or vLLM (for serving), FFmpeg (optional, for burn-in) · Models: OpenMOSS-Team/MOSS-Transcribe-Diarize (0.9B, Hugging Face) · port 7860 · [Repo](https://github.com/openmoss/moss-transcribe-diarize) · [▶️ Demo ↗](https://platform.mosi.cn/app/playground) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moss-transcribe-diarize/)</sub>

<a name="voiceprintrecognition-pytorch"></a>
### #&#8288;96 [voiceprintrecognition-pytorch](https://github.com/yeyupiaoling/voiceprintrecognition-pytorch) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (6) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · Apache-2.0 · Sep 2026</sub>

**PyTorch toolkit for training and running speaker verification and identification models.**

Training and inference code for speaker embeddings (voiceprints) in PyTorch. It implements EcapaTdnn, TDNN, Res2Net, ResNetSE, ERes2Net and CAM++ with several pooling layers, loss functions (AAMLoss, SphereFace2 and others) and feature front-ends (Fbank, MFCC, WavLM). It covers voiceprint comparison, recognition and speaker diarization. Pretrained weights are distributed through the author's paid community group.

- **+** Six backbones, seven loss functions and six feature front-ends are selectable through YAML configs
- **+** Reports EER and MinDCF on CN-Celeb and VoxCeleb1&2 for each model, plus loss and preprocessing ablations
- **+** Includes data augmentation: speed, volume, noise, reverb and SpecAugment
- **+** Supports single-GPU and multi-GPU training via torchrun, with optional precomputed feature extraction
- **−** Pretrained model files require joining the author's paid knowledge community
- **−** README and docs are primarily in Chinese, with a separate English README
- **−** Training needs a manually downloaded dataset such as CN-Celeb, plus data-list preparation scripts
- **−** No release tags; the pip package name in the README (mvector) differs from the project name

<sub>GPU optional · Needs PyTorch 2.4.0, torchaudio, VisualDL, CN-Celeb or VoxCeleb dataset · Models: EcapaTdnn, TDNN, Res2Net, ResNetSE, ERes2Net · [Repo](https://github.com/yeyupiaoling/voiceprintrecognition-pytorch) · [▶️ Demo ↗](https://tools.yeyupiaoling.cn/speech/voiceprint_compare) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voiceprintrecognition-pytorch/)</sub>

<a name="neutts"></a>
### #&#8288;97 [neutts](https://github.com/neuphonic/neutts) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (60) · Freshness: active (87) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · custom license · Jul 2026</sub>

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

<a name="transcribe-anything"></a>
### #&#8288;98 [transcribe-anything](https://github.com/zackees/transcribe-anything) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · MIT · Oct 2026</sub>

**Whisper CLI that routes to CUDA, MLX, Intel XPU or WhisperX backends.**

Python CLI and API that transcribes local files or YouTube/URL inputs with Whisper variants, writing txt, srt, vtt and json. A --device flag selects the backend (openai-whisper, insanely-fast-whisper, WhisperX, SenseVoice, lightning-whisper-mlx, Intel XPU), each built in its own uv virtualenv on first use. Diarizing backends also write a speaker.json with per-speaker text.

- **+** Per-backend isolated venvs keep CUDA/torch dependencies out of your Python environment
- **+** Covers NVIDIA CUDA, Apple Silicon MLX, Intel Arc XPU and CPU from one CLI
- **+** Writes speaker.json with de-chunked speaker-labelled text when diarization is enabled
- **+** Runs locally; accepts local files and URLs via yt-dlp and bundled ffmpeg
- **−** Insane backend can run out of memory; a 12 GB card needs --batch-size 8 or lower
- **−** First run of the insane backend downloads about 10 GB of dependencies
- **−** Diarization requires your own Hugging Face token and accepting pyannote terms
- **−** Batched large-v3 mode may repeat text and misalign srt/vtt timestamps

<sub>GPU optional · Docker + Compose · Needs uv, yt-dlp, ffmpeg (bundled via static-ffmpeg), Hugging Face token (diarization only) · Models: openai-whisper, insanely-fast-whisper, WhisperX, SenseVoice, lightning-whisper-mlx · [Repo](https://github.com/zackees/transcribe-anything) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transcribe-anything/)</sub>

<a name="qwen3-tts"></a>
### #&#8288;99 [qwen3-tts](https://github.com/qwenlm/qwen3-tts) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (80) · Freshness: slowing (40) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Mar 2026</sub>

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

<a name="fireredtts3"></a>
### #&#8288;100 [fireredtts3](https://github.com/fireredteam/fireredtts3) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · Apache-2.0 · Sep 2026</sub>

**Multilingual zero-shot voice cloning, voice design and speech editing TTS models.**

FireRedTTS3 is PyTorch code and pretrained weights for text-to-speech. The Base model does zero-shot voice cloning across 24 languages and 21 Chinese dialects from a reference clip. The Instruct model adds voice design from a text description and speech editing (insert, delete, substitute, plus speed, pitch and volume). It ships a Python API and Gradio demos for both models.

- **+** Clones voices zero-shot in 24 languages and 21 Chinese dialects from a prompt clip
- **+** Instruct model designs new voices from text descriptions, no reference audio needed
- **+** Semantic and acoustic speech editing in the same model
- **+** Gradio demo scripts for both Base and Instruct, Apache-2.0 weights on Hugging Face and ModelScope
- **−** Acoustic edits only accept fixed instruction templates, not free-form phrasing
- **−** Full-language text normalization needs an external LLM API (30B+ model suggested)
- **−** Local TN covers only Chinese and English; other languages get basic cleaning
- **−** Base model needs explicit language tags or a separate FastText model for detection

<sub>Needs PyTorch, torchaudio, wetext, FastText lid.176 (optional), OpenAI-compatible LLM API for LLM TN (optional), Gradio (demo) · Models: FireRedTTS3-Base, FireRedTTS3-Instruct · port 7860 · [Repo](https://github.com/fireredteam/fireredtts3) · [▶️ Demo ↗](https://fireredteam.github.io/demos/firered_tts_3/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fireredtts3/)</sub>

<a name="dots-tts"></a>
### #&#8288;101 [dots.tts](https://github.com/studio-dots-ai/dots.tts) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: weak (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · Apache-2.0 · Oct 2026</sub>

**2B text-to-speech model with voice cloning and instruction-based speech editing.**

dots.tts is a 2B-parameter autoregressive text-to-speech system that generates 48 kHz audio from continuous representations (semantic encoder, LLM, flow-matching acoustic head), with no discrete tokens. The repo ships a CLI, Python runtimes, a Gradio demo, fine-tuning and MeanFlow distillation scripts, and seven checkpoints, including 1- and 2-step variants, a double-streaming variant and a speech-editing model.

- **+** Zero-shot voice cloning from reference audio, with or without a transcript
- **+** Distilled checkpoints run in 1, 2 or 4 steps; RTF p50 0.13-0.20 with --optimize
- **+** Separate dots.tts.edit model edits speech via XML-style tags (sub, del, emo, pitch, pause)
- **+** Includes fine-tuning, MeanFlow distillation, streaming API and SGLang Omni serving
- **−** Speed and throughput figures come from GPU setups; CPU use is not documented
- **−** Random-voice sampling is only meaningful on a fine-tuned single-speaker checkpoint
- **−** Double-streaming checkpoint has no CLI entry point, only a Python API
- **−** Fixed-step checkpoints reject sampling overrides, so step and CFG tuning is limited to other models

<sub>Needs PyTorch, conda (Python 3.10-3.12), Hugging Face Hub, Node.js 20+ (Edit Playground frontend), SGLang Omni (optional) · Models: dots.tts-base, dots.tts-soar, dots.tts-mf, dots.tts-mf-2steps, dots.tts-mf-1step · port 7860 · [Repo](https://github.com/studio-dots-ai/dots.tts) · [▶️ Demo ↗](https://huggingface.co/spaces/dots-studio/dots.tts) · [📖 Docs ↗](https://sgl-project.github.io/sglang-omni/cookbook/dots_tts.html) · [🌐 Site ↗](https://studio-dots-ai.github.io/dots.tts-demo/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dots-tts/)</sub>

<a name="scriberr"></a>
### #&#8288;102 [scriberr](https://github.com/rishikanthc/scriberr) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: known (39) · Freshness: active (86) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · MIT · Sep 2026</sub>

**Offline audio transcription server with speaker diarization and LLM chat.**

Scriberr is a self-hosted web app, written in Go, that transcribes audio and video locally using NVIDIA Parakeet, Canary or Whisper models, with word-level timing. It adds speaker diarization, a folder watcher, a REST API, a built-in recorder, notes, and summaries or chat over transcripts via Ollama or OpenAI-compatible endpoints. Data is stored in SQLite, and it installs via Docker (CPU or CUDA images) or Homebrew.

- **+** Runs transcription locally with Parakeet, Canary or Whisper; no cloud provider required
- **+** Speaker diarization and word-level timestamps with seek-from-text playback
- **+** Folder watcher and API allow integration with tools like n8n
- **+** Separate Docker images for CPU, CUDA and RTX 50-series Blackwell GPUs
- **−** First start takes several minutes while Python environments and models download
- **−** Upgrading from v1.1.0 requires splitting volumes and deleting the old whisperx-env
- **−** Plain HTTP access needs SECURE_COOKIES=false or audio streaming fails
- **−** Maintainer reported a development pause; last release was December 2025

<sub>GPU optional · Docker + Compose · Needs Docker or Homebrew, uv, SQLite, Ollama or OpenAI-compatible API (optional, for chat) · Models: NVIDIA Parakeet, NVIDIA Canary, Whisper, PyAnnote (diarization), Ollama · port 8080 · [Repo](https://github.com/rishikanthc/scriberr) · [🌐 Site ↗](https://scriberr.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scriberr/)</sub>

<a name="obs-localvocal"></a>
### #&#8288;103 [obs-localvocal](https://github.com/royshil/obs-localvocal) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (17) · Freshness: active (97) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · GPL-2.0 · Nov 2026</sub>

**OBS plugin for real-time local speech transcription and caption translation.**

LocalVocal is an OBS Studio plugin that transcribes audio in real time with whisper.cpp and shows the result as on-screen captions. It can translate captions with local CTranslate2 NMT models, Whisper's built-in translation, or cloud providers. Captions can also be written to .txt or .srt files or sent on an RTMP stream.

- **+** Runs Whisper locally on CPU, with CUDA, ROCm, Metal, CoreML, Vulkan and OpenCL backends
- **+** Accepts any GGML Whisper model; ships Tiny.en and downloads others from a dropdown
- **+** Outputs captions as OBS text sources, .txt/.srt files, or an RTMP caption stream
- **+** Installers for Windows, macOS (Intel and ARM) and Ubuntu, in generic, NVIDIA and AMD builds
- **−** Requires OBS Studio; not usable as a standalone transcription tool
- **−** Defaults to CPU only; GPU backend must be chosen manually in plugin settings
- **−** Linux packages are Ubuntu 22.04 .deb on x86_64 only; other distros must build from source
- **−** NVIDIA variant likely needs CUDA toolkit 12.8 or newer installed separately

<sub>GPU optional · Needs OBS Studio, MSVC runtime (Windows), CUDA toolkit 12.8+ (NVIDIA builds), Vulkan runtime/SDK (optional) · Models: Whisper GGML, CTranslate2 NMT, CoreML encoder · [Repo](https://github.com/royshil/obs-localvocal) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/obs-localvocal/)</sub>

<a name="real-time-voice-cloning"></a>
### #&#8288;104 [real-time-voice-cloning](https://github.com/corentinj/real-time-voice-cloning) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: widely used (97) · Freshness: slowing (37) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · custom license · Mar 2026</sub>

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

<a name="voicecraft"></a>
### #&#8288;105 [voicecraft](https://github.com/jasonppy/voicecraft) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (68) · Freshness: recent (67) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · custom license · May 2026</sub>

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

<a name="asrt-speechrecognition"></a>
### #&#8288;106 [asrt_speechrecognition](https://github.com/nl8590687/asrt_speechrecognition) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (67) · Freshness: slowing (34) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · GPL-3.0 · Apr 2026</sub>

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

<a name="diffsinger"></a>
### #&#8288;107 [diffsinger](https://github.com/moonintheriver/diffsinger) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (53) · Freshness: recent (61) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · MIT · Jul 2026</sub>

**Official PyTorch code for DiffSinger singing synthesis and DiffSpeech TTS.**

Research implementation of the AAAI-2022 DiffSinger paper: a shallow diffusion acoustic model that generates mel-spectrograms for singing voice synthesis, plus DiffSpeech for text-to-speech. It covers PopCS and OpenCpop pipelines (cascade, end-to-end, PNDM-accelerated) with NSF-HiFiGAN or HiFiGAN vocoders. Training and inference run from Python scripts documented per pipeline.

- **+** Several SVS pipelines: PopCS, OpenCpop cascade, end-to-end, and PNDM variants
- **+** Includes DiffSpeech for TTS on LJSpeech alongside singing synthesis
- **+** Hugging Face Spaces demos for both SVS and TTS
- **+** MIT license with official code matching the paper
- **−** Pinned to Python 3.8, torch 1.9 and CUDA 10.2/11.4 requirements files
- **−** Last release is January 2022; README updates stop at September 2022
- **−** No Docker image or packaged app; research-style scripts and dataset prep
- **−** Training depends on external datasets such as OpenCpop and LJSpeech

<sub>Needs Python 3.8, PyTorch 1.9, PyTorch Lightning, OpenCpop dataset, LJSpeech dataset · Models: DiffSinger, DiffSpeech, FFT-Singer, NSF-HiFiGAN, HiFiGAN · [Repo](https://github.com/moonintheriver/diffsinger) · [▶️ Demo ↗](https://huggingface.co/spaces/Silentlin/DiffSinger) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/diffsinger/)</sub>

<a name="willow"></a>
### #&#8288;108 [willow](https://github.com/heywillow/willow) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: known (39) · Freshness: active (94) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · Apache-2.0 · Aug 2026</sub>

**Voice assistant for dedicated hardware, paired with a self-hosted inference server.**

Willow is a C project for voice assistant hardware, with users receiving physical devices. The README is short: it points to heywillow.io for documentation and to the separate Willow Inference Server, which handles self-hosted STT, TTS and LLM tasks. Supported devices, wake words and integrations are not described in the README.

- **+** Self-hostable backend through the separate Willow Inference Server project
- **+** Inference server covers STT, TTS and LLM tasks, and works over WebRTC
- **+** Runs on dedicated hardware rather than a general-purpose PC
- **−** README has no install or setup steps; they are only in the external docs
- **−** Self-hosted inference needs a second repository to be deployed
- **−** Requires physical hardware to use as intended

<sub>Docker · Needs Willow Inference Server · [Repo](https://github.com/heywillow/willow) · [📖 Docs ↗](https://heywillow.io) · [🌐 Site ↗](https://heywillow.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/willow/)</sub>

<a name="megatts3"></a>
### #&#8288;109 [megatts3](https://github.com/bytedance/megatts3) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: popular (58) · Freshness: recent (73) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · Apache-2.0 · Jun 2026</sub>

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

<a name="ekho"></a>
### #&#8288;110 [ekho](https://github.com/hgneng/ekho) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (4) · Freshness: recent (70) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · GPL-2.0 · Nov 2026</sub>

**Chinese text-to-speech engine using recorded Mandarin voice files.**

Ekho is a Chinese text-to-speech engine from the eGuideDog project, forked from SourceForge at r2418 with patches to r2478. Voice files are not bundled and come from a distribution package or the Ekho Voice Data download page. Mandarin voices can be replaced by swapping the pinyin folder and deleting pinyin.index and pinyin.voice, which are regenerated on the next run.

- **+** Custom voices can be added; a guide for making new voices is linked
- **+** Mandarin voice swap needs only a folder replacement and index regeneration
- **+** Repository has a recent commit (2026-09-02)
- **−** Voice files are not in the repository and must be downloaded separately
- **−** README mentions only Chinese; other languages are not covered
- **−** README is minimal and defers build steps to an INSTALL file
- **−** Last tagged release is from 2023-08-08

<sub>Docker · Needs Ekho voice data files · Models: pinyin voice files (pinyin.index, pinyin.voice) · [Repo](https://github.com/hgneng/ekho) · [📖 Docs ↗](http://eguidedog.net/doc/doc_make_new_voice_cn.php) · [🌐 Site ↗](http://www.eguidedog.net/ekho.php) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ekho/)</sub>

<a name="paddlespeech"></a>
### #&#8288;111 [paddlespeech](https://github.com/paddlepaddle/paddlespeech) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (78) · Freshness: recent (50) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Jun 2026</sub>

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

<a name="luxtts"></a>
### #&#8288;112 [luxtts](https://github.com/ysharma3501/luxtts) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (56) · Freshness: recent (69) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · Apache-2.0 · Jun 2026</sub>

**Text-to-speech model with voice cloning and 48 kHz output.**

LuxTTS is a ZipVoice-based text-to-speech model that clones a voice from a short reference clip (wav or mp3, at least 3 seconds recommended). It is distilled to 4 sampling steps and uses a custom 48 kHz vocoder instead of the default 24 kHz one. It runs from Python on CUDA, CPU or Apple MPS, and the README claims 150x realtime on a single GPU.

- **+** Outputs 48 kHz audio rather than the usual 24 kHz
- **+** README says it fits in 1 GB VRAM and runs faster than realtime on CPU
- **+** Supports CUDA, CPU and Apple MPS devices
- **+** Tunable sampling parameters: num_steps, t_shift, speed, return_smooth, ref_duration
- **−** Python library only; web UIs and ComfyUI nodes are community projects
- **−** Runs in float32; float16 inference code is still on the roadmap
- **−** Needs a 3+ second reference clip; artifacts may require tuning
- **−** No tagged releases; speed and quality claims are not benchmarked in the README

<sub>GPU optional · Needs Python, Hugging Face model YatharthS/LuxTTS, librosa, soundfile · Models: LuxTTS (ZipVoice-based, 4-step distilled), 48 kHz vocoder · [Repo](https://github.com/ysharma3501/luxtts) · [▶️ Demo ↗](https://huggingface.co/spaces/YatharthS/LuxTTS) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/luxtts/)</sub>

<a name="whisper-timestamped"></a>
### #&#8288;113 [whisper-timestamped](https://github.com/linto-ai/whisper-timestamped) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (36) · Freshness: recent (78) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · AGPL-3.0 · Sep 2026</sub>

**Whisper extension that adds word-level timestamps and confidence to transcripts.**

whisper-timestamped extends the openai-whisper Python package to output start/end times and a confidence score for each word, using Dynamic Time Warping on cross-attention weights. It runs as a Python function (`transcribe`) or a CLI, and can load fine-tuned Whisper models from Hugging Face. Optional VAD (silero, auditok) runs before decoding to reduce hallucinations on silence.

- **+** Word timestamps and confidence scores without a separate wav2vec alignment model
- **+** Alignment happens on the fly with greedy decoding, so no second inference pass
- **+** Optional silero or auditok VAD avoids hallucinated text on silence
- **+** Loads fine-tuned Whisper models from Hugging Face or a local folder
- **−** README disclaimer calls it experimental and says it may significantly impact performance
- **−** Defaults use greedy decoding without temperature fallback, which can hurt hard audio
- **−** AGPL-3.0 license restricts use in closed-source network services
- **−** Library and CLI only, no server or web UI; GPU Docker image is about 9GB

<sub>GPU optional · Docker · Needs python3, ffmpeg, openai-whisper, torch, onnxruntime (VAD), torchaudio (VAD), transformers (HF models), matplotlib (plots) · Models: OpenAI Whisper models, Hugging Face fine-tuned Whisper models, local Whisper model folders · [Repo](https://github.com/linto-ai/whisper-timestamped) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisper-timestamped/)</sub>

<a name="speaches"></a>
### #&#8288;114 [Speaches](https://github.com/speaches-ai/speaches) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (46) · Freshness: recent (54) · Maintenance: weak (10) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · MIT · Apr 2026</sub>

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

<a name="genie-tts"></a>
### #&#8288;115 [genie-tts](https://github.com/high-logic/genie-tts) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (22) · Freshness: active (86) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Nov 2026</sub>

**CPU-oriented ONNX inference engine for GPT-SoVITS text-to-speech.**

Genie runs GPT-SoVITS V2 and V2ProPlus voices through ONNX on CPU, with a Python API for synthesis and playback. It includes a converter from original .pth/.ckpt models to ONNX and a small FastAPI server. The README reports 1.13s first-inference latency on an i7-13620H, a runtime of about 200MB and a model of about 230MB.

- **+** Reported 1.13s first-inference latency on CPU versus 1.35s for the official PyTorch model
- **+** Runtime of about 200MB, compared with several GB for PyTorch
- **+** Built-in converter from GPT-SoVITS V2/V2ProPlus checkpoints to ONNX
- **+** Predefined characters allow trying it without training a model
- **−** Supports only GPT-SoVITS V2 and V2ProPlus; V3 and V4 are not yet supported
- **−** No official Docker image; it is listed as unfinished on the roadmap
- **−** First run downloads about 391MB of resource files
- **−** Latency figures come from one CPU and one Japanese test set

<sub>no GPU · Needs Python >= 3.10, torch (model conversion only), HuggingFace resource download (~391MB) · Models: GPT-SoVITS V2, GPT-SoVITS V2ProPlus, ONNX · port 8000 · [Repo](https://github.com/high-logic/genie-tts) · [▶️ Demo ↗](https://www.bilibili.com/video/BV1d2hHzJEz9) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/genie-tts/)</sub>

<a name="audionotes"></a>
### #&#8288;116 [audionotes](https://github.com/harry0703/audionotes) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: known (33) · Freshness: active (87) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · MIT · Jul 2026</sub>

**Local audio and video transcription with Markdown notes and Q&A.**

AudioNotes transcribes uploaded audio, video or browser recordings with FunASR (Fun-ASR-Nano-2512 by default), then uses an Ollama model (qwen3.5:2b by default) to turn the transcript into Markdown notes and answer follow-up questions. It runs on Chainlit with login, history and domain hot words, and stores data locally in a folder. Audio and notes are not sent to third-party AI APIs by default.

- **+** Transcription and LLM both run locally via FunASR and Ollama
- **+** No database service needed; data lives in one folder
- **+** Optional NVIDIA GPU compose file for faster recognition on Linux
- **+** Web UI binds to localhost by default
- **−** Docker needs 12GB RAM or more; 8GB reportedly insufficient for long audio
- **−** Default login is admin/admin until .env is edited
- **−** Cannot switch ASR model at runtime; multilingual needs .env change and restart
- **−** README is Chinese only; default models are tuned for Chinese

<sub>RAM ≥ 12 GB · GPU optional · Docker + Compose · Needs Ollama, Docker Desktop, ffmpeg (source install), Python 3.12 (source install) · Models: FunAudioLLM/Fun-ASR-Nano-2512, FunAudioLLM/Fun-ASR-MLT-Nano-2512, qwen3.5:2b (Ollama) · port 15433 · [Repo](https://github.com/harry0703/audionotes) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/audionotes/)</sub>

<a name="parlor"></a>
### #&#8288;117 [parlor](https://github.com/fikrikarim/parlor) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (27) · Freshness: active (94) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · Apache-2.0 · Aug 2026</sub>

**On-device voice and camera assistant using Gemma 4, llama.cpp and Kokoro TTS.**

Parlor is a browser-based voice assistant that runs a cascade locally: Silero VAD and smart-turn-v3 detect turn ends, Gemma 4 (E2B, E4B or 12B) via llama.cpp hears audio and sees camera frames, and Kokoro speaks the reply sentence by sentence. It supports barge-in, server-side timers, live translation and listen-only modes, and optional background web research through an OpenAI-compatible endpoint. Labeled a research preview, and partly AI-written.

- **+** Runs fully on-device by default; research calls only happen if REASONER_API_KEY is set
- **+** Streams replies sentence by sentence; README reports ~0.7s to first audio on M3 Pro (e2b)
- **+** Separate grammar-forced JSON action head keeps timers and mode switches out of spoken text
- **+** Includes end-to-end tests and latency benchmarks you can rerun
- **−** Research preview; the README warns of rough edges and bugs
- **−** Needs Apple Silicon or Linux with a supported GPU; no Windows or CPU-only path stated
- **−** Requires a recent llama.cpp build (b9503 or newer, b9512 for 12b)
- **−** Downloads about 5.7 GB of models on first run, plus TTS models

<sub>RAM ≥ 6 GB · GPU required · Needs llama.cpp, uv, Python 3.12+, OpenAI-compatible endpoint (optional, for research) · Models: Gemma 4 E2B, Gemma 4 E4B, Gemma 4 12B, Kokoro TTS, smart-turn-v3 · port 8000 · [Repo](https://github.com/fikrikarim/parlor) · [📖 Docs ↗](https://github.com/fikrikarim/parlor/blob/main/docs/configuration.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/parlor/)</sub>

<a name="moss-ttsd"></a>
### #&#8288;118 [moss-ttsd](https://github.com/openmoss/moss-ttsd) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · Apache-2.0 · Sep 2026</sub>

**Multi-speaker dialogue speech synthesis model with zero-shot voice cloning.**

MOSS-TTSD turns scripts tagged [S1]–[S5] into spoken conversation for 1 to 5 speakers, cloning each voice from a short reference clip. It supports 20 languages and up to 60 minutes of audio in one session. Inference runs through Hugging Face Transformers, a batch script, or a fused model served with OpenMOSS's SGLang fork.

- **+** Handles 1 to 5 speakers with [S1]–[S5] tags and per-speaker voice cloning
- **+** Up to 60 minutes of audio in a single session, 20 languages
- **+** Apache-2.0 weights on Hugging Face, with a hosted Hugging Face Space demo
- **+** Optional SGLang serving path; README publishes SIM, ACC and WER benchmarks against other models
- **−** Needs reference audio and transcript for each speaker to clone voices
- **−** SGLang serving requires a custom OpenMOSS fork and a model fusion step
- **−** Server exposes a /generate endpoint, not an OpenAI-compatible TTS API
- **−** No GPU, VRAM or RAM requirements are given in the README, and the install needs flash-attn

<sub>GPU optional · Needs PyTorch 2.0+, Transformers, flash-attn, MOSS-Audio-Tokenizer, SGLang (OpenMOSS fork, optional) · Models: MOSS-TTSD-v1.0, MOSS-TTSD v0.7 (legacy), MOSS-Audio-Tokenizer · port 30000 · [Repo](https://github.com/openmoss/moss-ttsd) · [▶️ Demo ↗](https://huggingface.co/spaces/OpenMOSS-Team/MOSS-TTSD) · [🌐 Site ↗](https://mosi.cn/models/moss-ttsd) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moss-ttsd/)</sub>

<a name="mockingbird"></a>
### #&#8288;119 [mockingbird](https://github.com/babysor/mockingbird) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: widely used (93) · Freshness: quiet (25) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · custom license · Mar 2026</sub>

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

<a name="bert-vits2"></a>
### #&#8288;120 [bert-vits2](https://github.com/fishaudio/bert-vits2) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: popular (68) · Freshness: slowing (47) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.8k · AGPL-3.0 · May 2026</sub>

**Multilingual text-to-speech model combining VITS2 with BERT text features.**

Bert-VITS2 is a text-to-speech training and inference codebase that pairs the VITS2 backbone with multilingual BERT embeddings. The README points to webui_preprocess.py for a quick guide and expects users to read the code to learn training. The maintainers say the project will not be maintained in the short term and recommend Fish-Speech as the replacement.

- **+** VITS2 backbone with multilingual BERT features, building on MassTTS and vits2_pytorch
- **+** Includes a preprocessing web UI script (webui_preprocess.py) as a starting point
- **+** Demo and tech-slide videos are linked for judging output quality
- **−** Maintainers say it is unmaintained short term and recommend Fish-Speech instead
- **−** Last release is February 2024
- **−** README has no install steps, requirements or API docs; users must read the code
- **−** AGPL-3.0 license, plus usage restrictions stated in the README

<sub>Models: VITS2, multilingual BERT · [Repo](https://github.com/fishaudio/bert-vits2) · [▶️ Demo ↗](https://www.bilibili.com/video/BV18E421371Q) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bert-vits2/)</sub>

<a name="patter"></a>
### #&#8288;121 [patter](https://github.com/patterai/patter) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (3) · Freshness: active (99) · Maintenance: weak (0) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · MIT · Aug 2026</sub>

**SDK that connects an AI voice agent to phone calls via Twilio, Telnyx or Plivo.**

Patter is a Python and TypeScript SDK that runs the agent loop for phone calls, covering LLM, speech-to-text, text-to-speech, realtime voice engines and the telephony carrier. Each layer is a swappable provider, and calls run in Realtime, Pipeline or Hybrid mode. A built-in Cloudflare tunnel and dashboard support local development, and calls can be simulated from the terminal.

- **+** Python and TypeScript SDKs with the same API, hooks and events
- **+** Swappable providers per layer: 5 LLMs, 7 STT, 7 TTS, 4 realtime engines
- **+** Works with Twilio, Telnyx and Plivo; tools, transfer and guardrails are carrier-independent
- **+** LLM fallback chain mid-call and OpenTelemetry traces per call
- **−** Depends on paid cloud providers and a carrier account; no local model path is documented
- **−** Anonymous telemetry is on by default and must be disabled by opt-out
- **−** Quick tunnel is for development; production needs a static webhook URL or ngrok
- **−** Templates live in separate repos, not in this one

<sub>no GPU · Docker + Compose · Needs Twilio, Telnyx or Plivo account, LLM/STT/TTS provider API keys, Cloudflare quick tunnel or ngrok · Models: OpenAI, Anthropic, Google Gemini, Groq, Cerebras · [Repo](https://github.com/patterai/patter) · [📖 Docs ↗](https://docs.getpatter.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/patter/)</sub>

<a name="misotts"></a>
### #&#8288;122 [misotts](https://github.com/misolabsai/misotts) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (41) · Freshness: recent (71) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · custom license · Jun 2026</sub>

**8B-parameter English text-to-dialogue speech model with voice cloning from prompt audio.**

Miso TTS 8B is an RVQ Transformer, inspired by Sesame CSM, that generates Mimi audio codes from text and optional audio context. It uses a Llama 8B backbone with a 300M audio decoder, and this repo holds the inference code and a Python API. Output is watermarked with SilentCipher by default, and weights load from Hugging Face.

- **+** Voice cloning by passing prior audio and transcript as context segments
- **+** Conversational generation conditioned on interleaved text and audio history
- **+** Weights on Hugging Face; first run downloads them automatically
- **+** Output watermarked by default via SilentCipher
- **−** English only
- **−** Needs about 24 GB VRAM in bf16; 4–16 GB GPUs are insufficient
- **−** First run downloads roughly 30–40 GB
- **−** No server or HTTP API; only a script and Python interface

<sub>RAM ≥ 20 GB · GPU required · Needs PyTorch, torchaudio, Hugging Face Hub, Mimi codec, SilentCipher (sony/silentcipher), Llama 3.2 tokenizer, uv · Models: Miso TTS 8B (MisoLabs/MisoTTS), bfloat16, float32 · [Repo](https://github.com/misolabsai/misotts) · [▶️ Demo ↗](https://misolabs.ai) · [🌐 Site ↗](https://misolabs.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/misotts/)</sub>

<a name="wespeaker"></a>
### #&#8288;123 [wespeaker](https://github.com/wenet-e2e/wespeaker) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (11) · Freshness: recent (70) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · Apache-2.0 · Sep 2026</sub>

**Speaker embedding training and verification toolkit with diarization recipes.**

WeSpeaker is a PyTorch toolkit for training speaker embedding models and using them for speaker verification and diarization. It ships recipes for VoxCeleb, CNCeleb, NIST SRE16 and VoxConverse, plus a pip package and CLI for extracting embeddings, scoring similarity and diarizing audio with pretrained models. A runtime directory covers deployment, including MNN inference.

- **+** Recipes for VoxCeleb, CNCeleb, SRE16 and VoxConverse with published EER/minDCF results
- **+** Pip package and CLI cover embedding, similarity and diarization with pretrained models
- **+** Supports many architectures and frontends: ResNet, ECAPA-TDNN, ERes2Net, WavLM, Whisper encoder
- **+** Active development: U³-xi and ReDimNet2 models added in 2026
- **−** Last tagged release is from 2023-07; pip install pulls from the git master branch
- **−** Speaker tasks only; no speech recognition or synthesis
- **−** Dev setup is involved: pinned torch, sox, and a torchnet build workaround
- **−** README badges list Python 3.8 and 3.9 only

<sub>GPU optional · Needs PyTorch, torchaudio, sox · Models: ResNet, ECAPA-TDNN, ERes2Net, Res2Net, SimAM_ResNet · [Repo](https://github.com/wenet-e2e/wespeaker) · [▶️ Demo ↗](https://huggingface.co/spaces/wenet/wespeaker_demo) · [📖 Docs ↗](http://wenet.org.cn/wespeaker) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/wespeaker/)</sub>

<a name="amphion"></a>
### #&#8288;124 [amphion](https://github.com/open-mmlab/amphion) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: popular (72) · Freshness: slowing (30) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Mar 2026</sub>

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

<a name="gpa"></a>
### #&#8288;125 [gpa](https://github.com/autoark/gpa) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: known (38) · Freshness: recent (65) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · Apache-2.0 · May 2026</sub>

**Single autoregressive audio model for speech recognition and voice-cloning TTS.**

GPA is a 0.6B-parameter autoregressive transformer that handles both ASR and TTS in one checkpoint (GPA-v1.5), with native PyTorch inference and Hugging Face Trainer fine-tuning. It also ships GPA-TTS, a standalone ONNX Runtime TTS with INT4 Qwen and INT8/FP16/FP32 decoders for CPU voice cloning. Voice conversion is in the paper but not yet in the v1.5 native path.

- **+** One 0.6B model does ASR and TTS; reports 1.43 WER on test-en TTS
- **+** GPA-TTS runs zero-shot voice cloning on CPU via ONNX Runtime with selectable decoder precision
- **+** ONNX runtime offers CLI, FastAPI service and browser UI
- **+** Training code included; backends listed: torch, vllm, llama-cpp, sglang, mlx-lm
- **−** Voice conversion is not yet supported in v1.5; listed as a next step
- **−** ASR error rates trail Fun-ASR, FireRed-ASR and Whisper-L on several benchmarks
- **−** Interactive demo and vLLM/FastAPI service deployment are still unchecked on the roadmap
- **−** TTS speaker similarity is below most listed open models, e.g. 63.5 on test-en

<sub>GPU optional · Needs PyTorch, Hugging Face, ONNX Runtime · Models: PyTorch, Hugging Face, ONNX, vLLM, llama.cpp · [Repo](https://github.com/autoark/gpa) · [▶️ Demo ↗](https://autoark.github.io/GPA/) · [📖 Docs ↗](https://github.com/autoark/gpa/blob/main/GPA_1.5/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpa/)</sub>

<a name="chatterbox-tts-server"></a>
### #&#8288;126 [chatterbox-tts-server](https://github.com/devnen/chatterbox-tts-server) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (13) · Freshness: recent (74) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · MIT · May 2026</sub>

**OpenAI-compatible TTS server and web UI for Resemble AI's Chatterbox models.**

FastAPI server that wraps the Chatterbox TTS family (Original, Multilingual with 23 languages, and the 350M-parameter Turbo) behind an OpenAI-compatible speech API and a web UI. It adds zero-shot voice cloning from .wav or .mp3 references, predefined voices, a seed parameter, and sentence-based chunking for long texts such as audiobooks. Runs on CUDA, ROCm, Apple MPS or CPU.

- **+** Hot-swaps Original, Multilingual and Turbo engines from a UI dropdown without restart
- **+** Voice cloning from a reference file, plus predefined voices and a fixed seed for repeatable output
- **+** Chunks long text and joins the audio, so whole books can go in one request
- **+** Supports CUDA, ROCm, Apple MPS and CPU, with separate Docker compose files per GPU stack
- **−** Python 3.10 is required; 3.11+ may fail on missing wheels
- **−** Only serves Chatterbox models, no other TTS engines
- **−** Streaming output is opt-in on /tts and not the default
- **−** Installation depends on pinned torch and CUDA variants chosen per GPU generation

<sub>GPU optional · Docker + Compose · Needs PyTorch, FastAPI, Docker (optional) · Models: Chatterbox Original (0.5B), Chatterbox Multilingual (23 languages), Chatterbox Turbo (350M) · port 8004 · [Repo](https://github.com/devnen/chatterbox-tts-server) · [▶️ Demo ↗](https://colab.research.google.com/github/devnen/Chatterbox-TTS-Server/blob/main/Chatterbox_TTS_Colab_Demo.ipynb) · [📖 Docs ↗](https://github.com/devnen/Chatterbox-TTS-Server/blob/main/README_Colab.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatterbox-tts-server/)</sub>

<a name="sonitranslate"></a>
### #&#8288;127 [sonitranslate](https://github.com/r3gm/sonitranslate) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (9) · Freshness: recent (70) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · Apache-2.0 · Aug 2026</sub>

**Gradio web UI that translates and dubs videos with synced audio.**

SoniTranslate transcribes a video or audio file with WhisperX/faster-whisper, diarizes speakers with pyannote, translates the text, and re-synthesizes speech in the target language. TTS options include edge-tts, Piper, Coqui XTTS, Bark, Facebook MMS and OpenAI, with optional RVC, FreeVC and OpenVoiceV2 voice imitation. It outputs dubbed video, audio or subtitles (SRT, ASS) and runs as a Gradio app on port 7860.

- **+** Full pipeline in one UI: transcription, diarization, translation, TTS and remux
- **+** Many TTS and voice-cloning backends, up to 12 speakers per job
- **+** Accepts YouTube URLs and playlists, local files, SRT input, and batch jobs
- **+** Has a CPU mode flag and a Colab notebook for running without a local GPU
- **−** Local install is manual: conda, CUDA 11.8, pinned PyTorch 2.5.1, no Docker
- **−** Pyannote diarization needs a Hugging Face token and license acceptance, with commercial limits
- **−** Install tested on Linux only; other platforms are not documented
- **−** Last release is May 2024; README notes some features are obsolete

<sub>GPU optional · Needs ffmpeg, Hugging Face token, CUDA 11.8, conda, OpenAI API key (optional) · Models: WhisperX, faster-whisper, pyannote, edge-tts, Piper TTS · port 7860 · [Repo](https://github.com/r3gm/sonitranslate) · [▶️ Demo ↗](https://huggingface.co/spaces/r3gm/video_dubbing_sonitr_demo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sonitranslate/)</sub>

<a name="bailing"></a>
### #&#8288;128 [bailing](https://github.com/wwbin2017/bailing) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: niche (21) · Freshness: slowing (33) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Apr 2026</sub>

**Voice conversation assistant chaining FunASR, silero-vad, an LLM and TTS.**

Bailing is a Python voice assistant that passes microphone audio through silero-vad and FunASR (SenseVoiceSmall) to text, sends it to an LLM (DeepSeek by default), and speaks the reply with edge-tts, Kokoro-82M, ChatTTS or macOS say. It supports barge-in, memory, scheduled tasks and tool calls, with OpenClaw as an execution backend. It runs locally or as a server with a browser client on port 8000.

- **+** Modular ASR, VAD, LLM and TTS stages that can be swapped independently
- **+** Runs without a GPU; README claims about 800ms end-to-end latency
- **+** Handles barge-in by keyword or speech while audio is playing
- **+** Built-in tools: weather, web search, scheduled reminders, OpenClaw task execution
- **−** No Docker or compose files; install is pip plus manual model download
- **−** Requires Python 3.12+ and a separate OpenManus requirements install
- **−** Voice wake-up is still unchecked on the roadmap
- **−** README says personal study use only, not for production or commercial use

<sub>no GPU · Needs DeepSeek API key (or OpenAI, Qwen, Gemini, 01yi), SenseVoiceSmall model weights, OpenClaw (optional), OpenSSL self-signed cert for server mode · Models: FunASR SenseVoiceSmall, silero-vad, DeepSeek, OpenAI, Qwen · port 8000 · [Repo](https://github.com/wwbin2017/bailing) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bailing/)</sub>

<a name="dia"></a>
### #&#8288;129 [dia](https://github.com/nari-labs/dia) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: widely used (85) · Freshness: quiet (0) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Nov 2025</sub>

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

<a name="soulx-podcast"></a>
### #&#8288;130 [soulx-podcast](https://github.com/soul-ailab/soulx-podcast) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: known (45) · Freshness: quiet (5) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · Apache-2.0 · Dec 2025</sub>

**Multi-speaker podcast speech synthesis with dialects and voice cloning.**

Inference code and 1.7B checkpoints for generating multi-turn, multi-speaker dialogue speech with zero-shot voice cloning. It supports Mandarin and English, plus Sichuanese, Henanese and Cantonese through a separate dialect model. Paralinguistic tags such as laughter, sigh and breathing can be inserted. A WebUI and an optional vLLM Docker runtime are included.

- **+** Generates long-form dialogue with multiple speakers, not only single-voice TTS
- **+** Zero-shot voice cloning works across Chinese dialects from Mandarin prompts
- **+** Paralinguistic tags: laughter, sigh, breathing, coughing, throat clearing
- **+** Apache-2.0 code and weights; WebUI and optional vLLM Docker runtime provided
- **−** Streaming inference is not implemented yet (listed in TODOs)
- **−** Dialects need the separate dialect checkpoint rather than the base model
- **−** Languages limited to Mandarin, English and three Chinese dialects
- **−** No tagged releases; install is a manual conda and pip setup

<sub>Needs Python 3.11, Conda, Hugging Face model weights, Docker with NVIDIA runtime (optional vLLM) · Models: SoulX-Podcast-1.7B, SoulX-Podcast-1.7B-dialect · port 7860 · [Repo](https://github.com/soul-ailab/soulx-podcast) · [▶️ Demo ↗](https://huggingface.co/Soul-AILab/spaces) · [🌐 Site ↗](https://soul-ailab.github.io/soulx-podcast/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/soulx-podcast/)</sub>

<a name="stt"></a>
### #&#8288;131 [stt](https://github.com/jianchang512/stt) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: popular (53) · Freshness: quiet (20) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · GPL-3.0 · Jan 2026</sub>

**Offline speech-to-text web app and API built on faster-whisper.**

Transcribes audio and video files locally with faster-whisper models (tiny to large-v3) and outputs plain text, JSON or timestamped SRT. It runs a Flask web UI and exposes a POST /api endpoint plus an OpenAI-compatible /v1 transcription endpoint on port 9977. A prebuilt Windows package is provided; Linux and macOS run from source with Python 3.9-3.11.

- **+** OpenAI-compatible /v1 transcription endpoint works with the official OpenAI Python client
- **+** Outputs text, JSON or SRT subtitles with timestamps
- **+** Prebuilt Windows package with the tiny model bundled; start.exe opens the UI
- **+** Uses CUDA when configured, with CPU as the default
- **−** No Docker image or compose file; source install needs venv, ffmpeg and manual model download
- **−** CUDA setup is manual: cuDNN, cuBLAS DLLs and editing set.ini
- **−** Chinese output can come out in Traditional characters
- **−** large-v3 on CPU or under 8 GB VRAM can exhaust memory or crash

<sub>GPU optional · Needs Python 3.9-3.11, ffmpeg, PyTorch, CUDA and cuDNN (for GPU) · Models: faster-whisper tiny, faster-whisper base, faster-whisper small, faster-whisper medium, faster-whisper large-v3 · port 9977 · [Repo](https://github.com/jianchang512/stt) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/stt/)</sub>

<a name="speech-ai-forge"></a>
### #&#8288;132 [speech-ai-forge](https://github.com/lenml/speech-ai-forge) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: niche (8) · Freshness: recent (65) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · AGPL-3.0 · May 2026</sub>

**TTS and ASR server with Gradio WebUI wrapping many open speech models.**

Speech-AI-Forge runs several open text-to-speech models (ChatTTS, CosyVoice, FishSpeech, F5-TTS, Index-TTS, Qwen3-TTS, GPT-SoVITS and others) behind one HTTP API and a Gradio WebUI. It also covers Whisper and SenseVoice ASR, OpenVoice voice cloning, a resemble-enhance step, and a MiniMax cloud TTS option. The WebUI adds long-text splitting, SSML and podcast scripting, and voice management.

- **+** Many TTS backends in one tool, including Index-TTS, CosyVoice v2/v3 and Qwen3-TTS
- **+** Separate API-only entrypoint (launch.py) with Swagger docs at /docs on port 7870
- **+** Long-text splitting, SSML, podcast and subtitle-to-speech workflows in the WebUI
- **+** Models download from Hugging Face or ModelScope, with optional auto-download on first use
- **−** AGPL-3.0 license restricts use in closed-source network services
- **−** README and most docs are in Chinese
- **−** Each backend needs its own weights, so disk and dependency load grows with models used
- **−** Built-in voices are only ChatTTS and CosyVoice; other models need reference audio

<sub>Docker + Compose · Needs Gradio, Docker (optional), Hugging Face or ModelScope model downloads · Models: ChatTTS, CosyVoice, FishSpeech, F5-TTS, Index-TTS · port 7870 · [Repo](https://github.com/lenml/speech-ai-forge) · [▶️ Demo ↗](https://colab.research.google.com/github/lenML/Speech-AI-Forge/blob/main/colab.ipynb) · [📖 Docs ↗](https://github.com/lenML/Speech-AI-Forge/blob/main/docs/api.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speech-ai-forge/)</sub>

<a name="subsai"></a>
### #&#8288;133 [subsai](https://github.com/absadiki/subsai) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: niche (18) · Freshness: recent (53) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · GPL-3.0 · Apr 2026</sub>

**Subtitle generator with Web UI, CLI and Python API on Whisper backends.**

Subs AI transcribes audio and video into subtitle files using Whisper and several variants, including whisper.cpp, faster-whisper, WhisperX and stable-ts, or an OpenAI-compatible API. It has a web UI with subtitle editing, translation, auto-sync and video merging, plus a batch-capable CLI and a Python package. Output formats include SRT, VTT, ASS, SSA, MicroDVD, MPL2 and TMP.

- **+** Eight transcription backends selectable from the UI, CLI or Python call
- **+** Built-in translation (NLLB, M2M100, mBART), ffsubsync auto-sync and subtitle merging into video
- **+** Web UI runs offline with local models; no third-party service required
- **+** CLI accepts a text file of paths for batch processing
- **−** Installs from git via pip; no tagged release
- **−** Python 3.12+ may have compatibility issues; 3.10 or 3.11 recommended
- **−** Large dependency set; trimming backends means editing requirements.txt by hand
- **−** Needs ffmpeg, possibly Rust for tokenizers; CUDA torch may need manual install

<sub>GPU optional · Docker + Compose · Needs ffmpeg, Python 3.10/3.11, PyTorch, Rust (if no tokenizers wheel) · Models: openai/whisper, whisper-timestamped, whisper.cpp, faster-whisper, WhisperX · port 8501 · [Repo](https://github.com/absadiki/subsai) · [📖 Docs ↗](https://absadiki.github.io/subsai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/subsai/)</sub>

<a name="agnentic-voice-ai-sdk"></a>
### #&#8288;134 [agnentic-voice-ai-sdk](https://github.com/ahmedeltaher/agnentic-voice-ai-sdk) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: known (33) · Freshness: recent (68) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 2.6k · no license · Jun 2026</sub>

**Kotlin library for voice conversations with Claude in Android apps.**

An Android library that chains microphone capture, voice activity detection, speech-to-text, Anthropic Claude and text-to-speech into one session, configured through a single VoiceAISDK.Builder. It includes Jetpack Compose components such as VoiceButton and ConversationView. STT and TTS engines are swappable (Android built-in, OpenAI Whisper, ElevenLabs), and it has optional PII redaction and emotion detection.

- **+** Swappable STT and TTS engines behind interfaces: Android built-in, Whisper, ElevenLabs
- **+** Ships Compose UI pieces and a runtime RECORD_AUDIO permission gate
- **+** Optional PII redaction, certificate pinning and encrypted key storage via EncryptedSharedPreferences
- **+** Works without Hilt by building the SDK directly with the Builder
- **−** Claude is the only AI engine; no local or other LLM provider
- **−** Requires an Anthropic API key and network; default Android STT also needs network
- **−** Android only; the repo is flagged as a template and no release is published
- **−** Tooling detected no license file despite the README's MIT badge and text

<sub>Needs Anthropic API key, OpenAI API key (optional, Whisper), ElevenLabs API key (optional), Hume AI API key (optional), Android 7.0+ (minSdk 24) · Models: Anthropic Claude (default claude-3-5-sonnet-20241022) · [Repo](https://github.com/ahmedeltaher/agnentic-voice-ai-sdk) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agnentic-voice-ai-sdk/)</sub>

<a name="orpheus-tts"></a>
### #&#8288;135 [orpheus-tts](https://github.com/canopyai/orpheus-tts) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: popular (61) · Freshness: quiet (3) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Dec 2025</sub>

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

<a name="auto-synced-translated-dubs"></a>
### #&#8288;136 [auto-synced-translated-dubs](https://github.com/thiojoe/auto-synced-translated-dubs) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (20) · Freshness: slowing (42) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · AGPL-3.0 · May 2026</sub>

**Translates SRT subtitles and dubs videos with synced cloud TTS.**

Takes an existing SRT subtitle file, translates it with Google Cloud or DeepL, then synthesizes speech per line with Azure, Google Cloud or Eleven Labs. Each clip is fitted to its subtitle's duration, by stretching or a second synthesis pass at a computed speed, and placed at the original timestamp. Extra scripts add audio tracks with ffmpeg and handle YouTube titles, descriptions and captions.

- **+** Fits each TTS clip to subtitle timings, so dubs stay aligned with the original video
- **+** Batch-processes multiple languages from per-language presets in batch.ini
- **+** Supports Azure, Google Cloud and Eleven Labs voices, with DeepL or Google for translation
- **+** Includes scripts for adding audio tracks and updating YouTube localized titles and captions
- **−** Needs paid cloud API accounts for translation and TTS; nothing runs locally
- **−** Assumes a single speaker per SRT; multiple voices need separate SRT files
- **−** Needs a human-made SRT with gaps between lines, or pauses come out too short
- **−** Configured by editing .ini files and script headers; no GUI; last release January 2025

<sub>no GPU · Needs ffmpeg, Google Cloud, Azure, DeepL or Eleven Labs API keys, rubberband (optional) · Models: Azure TTS, Google Cloud TTS, Eleven Labs, Google Translate, DeepL · [Repo](https://github.com/thiojoe/auto-synced-translated-dubs) · [📖 Docs ↗](https://github.com/ThioJoe/Auto-Synced-Translated-Dubs/wiki/Instructions:-Obtaining-an-API-Key) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/auto-synced-translated-dubs/)</sub>

<a name="fireredasr"></a>
### #&#8288;137 [fireredasr](https://github.com/fireredteam/fireredasr) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (25) · Freshness: slowing (33) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Feb 2026</sub>

**Mandarin, dialect and English speech recognition models with Python inference code.**

FireRedASR provides two speech recognition models, an 1.1B attention encoder-decoder (AED) and an 8.3B encoder-adapter-LLM variant built on Qwen2-7B-Instruct. It targets Mandarin, Chinese dialects and English, and ships a command-line script and a Python API for transcribing 16kHz WAV files. The README points to FireRedASR2S as the newer successor.

- **+** Reports 3.05 average CER on four Mandarin benchmarks (LLM) and 3.18 (AED), versus Whisper-Large-v3 at 9.86
- **+** Two variants: 1.1B AED for efficiency, 8.3B LLM for accuracy
- **+** Covers Mandarin, Chinese dialects and English; LibriSpeech test-clean WER 1.73 (LLM)
- **+** Apache-2.0 weights and code, with a Hugging Face demo space
- **−** AED input limited to 60s; over 200s triggers positional encoding errors
- **−** LLM variant supports only 30s of audio; longer behavior is undocumented
- **−** Batch beam search with LLM repeats text on short utterances unless lengths are sorted
- **−** Manual setup: download weights, symlink Qwen2-7B-Instruct, set PATH and PYTHONPATH, convert audio with ffmpeg

<sub>Needs Python 3.10, ffmpeg, Qwen2-7B-Instruct (for LLM variant), Hugging Face model weights · Models: FireRedASR-AED-L, FireRedASR-LLM-L, Qwen2-7B-Instruct · [Repo](https://github.com/fireredteam/fireredasr) · [▶️ Demo ↗](https://huggingface.co/spaces/FireRedTeam/FireRedASR) · [🌐 Site ↗](https://fireredteam.github.io/demos/firered_asr/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fireredasr/)</sub>

<a name="whisper-webui"></a>
### #&#8288;138 [whisper-webui](https://github.com/jhj0517/whisper-webui) <sub>score [17](../README.md#-how-we-rank "Score 17/100. Adoption: known (36) · Freshness: quiet (20) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Dec 2025</sub>

**Gradio web UI for generating subtitles with Whisper models.**

Whisper-WebUI is a Gradio browser interface that transcribes audio from files, YouTube or a microphone and exports SRT, WebVTT or plain txt. It can run openai/whisper, faster-whisper (the default) or insanely-fast-whisper, and adds optional Silero VAD, UVR background-music separation and pyannote speaker diarization. Subtitles can be translated with NLLB models or the DeepL API.

- **+** Switches between openai/whisper, faster-whisper and insanely-fast-whisper backends
- **+** Optional VAD, BGM separation and diarization steps before and after transcription
- **+** Subtitle translation via local NLLB models or the DeepL API
- **+** Install paths: Pinokio, Docker Compose, install scripts, plus a FastAPI backend
- **−** Real-time microphone transcription is still an unchecked TODO
- **−** Default requirements assume Nvidia CUDA 12.8; other devices need manual edits
- **−** Diarization needs a Hugging Face token and manually accepted model terms
- **−** Docker image is about 7GB; CLI usage is still on the TODO list

<sub>GPU optional · Docker + Compose · Needs FFmpeg, Python 3.10-3.12, Hugging Face token (diarization), DeepL API key (optional translation) · Models: openai/whisper, faster-whisper, insanely-fast-whisper, NLLB, pyannote · port 7860 · [Repo](https://github.com/jhj0517/whisper-webui) · [▶️ Demo ↗](https://colab.research.google.com/github/jhj0517/Whisper-WebUI/blob/master/notebook/whisper-webui.ipynb) · [📖 Docs ↗](https://github.com/jhj0517/Whisper-WebUI/wiki/Command-Line-Arguments) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/whisper-webui/)</sub>

<a name="chattts-colab"></a>
### #&#8288;139 [chattts_colab](https://github.com/6drf21e/chattts_colab) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: known (34) · Freshness: slowing (47) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 2.6k · no license · May 2026</sub>

**Gradio web UI for ChatTTS with voice sampling and multi-role reading.**

A Gradio web UI built on ChatTTS for text-to-speech. It adds streaming output, batch generation of random speaker voices that can be saved, long-text synthesis, and multi-role reading with LLM-generated scripts. It runs from a Colab notebook that exposes a gradio.live URL, locally on macOS via conda, or from a Windows offline bundle.

- **+** Colab notebook gives a public Gradio URL without local setup
- **+** Voice 'gacha' generates many speakers in batch and saves chosen ones
- **+** Streaming playback while audio is still being generated
- **+** Offline Windows bundle and local model loading when Hugging Face is unreachable
- **−** Pins ChatTTS to commit e6412b1, copied into the project by hand
- **−** README is in Chinese; setup steps cover only Colab and macOS
- **−** Failed first model download must be fixed by clearing the cache manually
- **−** Last release is June 2024; no Docker image provided

<sub>Needs ChatTTS, Gradio, Conda, Hugging Face model download · Models: ChatTTS · [Repo](https://github.com/6drf21e/chattts_colab) · [▶️ Demo ↗](https://colab.research.google.com/github/6drf21e/ChatTTS_colab/blob/main/chattts_webui_mix.ipynb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chattts-colab/)</sub>

<a name="vibevoice-comfyui"></a>
### #&#8288;140 [vibevoice-comfyui](https://github.com/enemyx-net/vibevoice-comfyui) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: niche (14) · Freshness: slowing (31) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Feb 2026</sub>

**ComfyUI custom nodes for VibeVoice text-to-speech with voice cloning.**

Wraps Microsoft's VibeVoice TTS model as ComfyUI nodes for single-speaker and multi-speaker (up to 4, [N]: labels) speech generation. It supports voice cloning from reference audio, LoRA adapters, 4-bit/8-bit quantization, automatic text chunking and wrapper-specific [pause:ms] tags. Models and the Qwen2.5-1.5B tokenizer must be downloaded manually into ComfyUI/models/vibevoice/.

- **+** Multi-speaker dialogue with up to 4 voices, each optionally cloned from a reference sample
- **+** Quantized options: Large-Q8 needs ~12GB VRAM, Large-Q4 ~8GB, per the README
- **+** Supports LoRA adapters with per-component toggles and strength control
- **+** Runs on CUDA, CPU and Apple Silicon (MPS); embeds VibeVoice code
- **−** Since v1.6.0 models and tokenizer must be downloaded and placed manually
- **−** Pause tags split text into chunks, which can hurt prosody across boundaries
- **−** LoRA tested only with transformers 4.51.3; newer versions not guaranteed
- **−** Dynamic 4-bit/8-bit LLM quantization requires CUDA; full Large model needs ~20GB VRAM

<sub>GPU optional · Needs ComfyUI, transformers>=4.51.3, Qwen2.5-1.5B tokenizer · Models: VibeVoice-1.5B, VibeVoice-Large, VibeVoice-Large-Q8, VibeVoice-Large-Q4, LoRA adapters · [Repo](https://github.com/enemyx-net/vibevoice-comfyui) · [▶️ Demo ↗](https://www.youtube.com/watch?v=fIBMepIBKhI) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vibevoice-comfyui/)</sub>

<a name="vits-simple-api"></a>
### #&#8288;141 [vits-simple-api](https://github.com/artrajz/vits-simple-api) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: niche (3) · Freshness: slowing (44) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · AGPL-3.0 · May 2026</sub>

**HTTP API and web UI for VITS-family text-to-speech models.**

Wraps VITS, Bert-VITS2, GPT-SoVITS, HuBert-soft VITS and W2V2 emotional VITS models behind an HTTP API (GET/POST under /voice/) and a browser inference page. It loads multiple models from data/models, detects text language automatically, and supports voice conversion, long-text batching, streaming and optional GPU inference. An admin panel handles loading and unloading models.

- **+** Serves several VITS variants, including Bert-VITS2 and GPT-SoVITS, from one API
- **+** Output formats include wav, ogg, silk, mp3 and flac, with a streaming option
- **+** Auto-loads every model folder in data/models; admin panel for load and unload
- **+** Optional API key auth; admin backend can be disabled in config.yaml
- **−** No models bundled; you download and place VITS models yourself
- **−** Bert-VITS2 models need a version field in config.json for compatibility
- **−** Linux GPU setup is untested by the author, per the README
- **−** Last release is 2025-02-03; AGPL-3.0 license limits closed-source network use

<sub>GPU optional · Docker + Compose · Needs Python 3.10, PyTorch, Docker (optional), CUDA (for GPU) · Models: VITS, Bert-VITS2, GPT-SoVITS, HuBert-soft VITS, W2V2-VITS · port 23456 · [Repo](https://github.com/artrajz/vits-simple-api) · [▶️ Demo ↗](https://huggingface.co/spaces/Artrajz/vits-simple-api) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vits-simple-api/)</sub>

<a name="ims-toucan"></a>
### #&#8288;142 [ims-toucan](https://github.com/digitalphonetics/ims-toucan) <sub>score [13](../README.md#-how-we-rank "Score 13/100. Adoption: niche (29) · Freshness: quiet (15) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Jan 2026</sub>

**Text-to-speech toolkit for training and running TTS in 7000+ languages.**

IMS Toucan is a PyTorch toolkit from the University of Stuttgart for training, fine-tuning and running ToucanTTS, a multilingual text-to-speech system covering over 7000 languages. A Python inference interface writes speech to file or plays it aloud, with controls for duration, pitch and energy variance. Recipe-based training pipelines support multi-GPU runs, and pretrained models download automatically from Hugging Face.

- **+** Covers over 7000 languages, with a published language list
- **+** Inference runs without a GPU; pretrained models download automatically
- **+** Fine-tuning recipes, multi-GPU training via torchrun, optional Weights & Biases logging
- **+** Hosted Hugging Face Space demo to try it without installing
- **−** No Docker image or HTTP API; use is through Python scripts
- **−** Last release is 2024-10-07, though commits continue
- **−** Training needs a CUDA GPU; new datasets require editing recipe and path files
- **−** Needs system packages like espeak-ng and libsndfile; Mac setup is involved

<sub>GPU optional · Needs Python 3.10, PyTorch, espeak-ng, libsndfile1, ffmpeg, libportaudio2, Hugging Face (model download) · Models: ToucanTTS, FastSpeech 2, HiFi-GAN, Matcha-TTS style flow-matching PostNet · [Repo](https://github.com/digitalphonetics/ims-toucan) · [▶️ Demo ↗](https://huggingface.co/spaces/Flux9665/MassivelyMultilingualTTS) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ims-toucan/)</sub>

<a name="outetts"></a>
### #&#8288;143 [outetts](https://github.com/edwko/outetts) <sub>score [12](../README.md#-how-we-rank "Score 12/100. Adoption: niche (10) · Freshness: quiet (30) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · Apache-2.0 · Mar 2026</sub>

**Python text-to-speech library with voice cloning from a reference clip.**

OuteTTS is a Python library that runs the OuteAI text-to-speech models (1.0 in 0.6B and 1B sizes) and clones a voice from a reference audio clip saved as a reusable speaker profile. It runs on llama.cpp bindings, llama.cpp server, Transformers, ExLlamaV2 or experimental vLLM, with batched async modes for throughput. Output is saved as WAV.

- **+** Multiple backends: llama.cpp (CPU, CUDA, ROCm, Vulkan, Metal), Transformers, ExLlamaV2, vLLM
- **+** Voice cloning from a reference clip, saved as a reusable JSON speaker profile
- **+** Batched async backends for 1.0 models, with RTF benchmarks on an L40S
- **+** Required sampler settings and 64-token repetition window are applied automatically
- **−** Only one default English speaker ships; other voices need your own reference audio
- **−** Cloned voice keeps the reference accent when speaking other languages
- **−** Recommended single generation is about 42 seconds (about 8,192 tokens), less with a long reference
- **−** GPU builds of llama.cpp require setting CMAKE_ARGS at install time

<sub>GPU optional · Needs llama-cpp-python, transformers, DAC (Descript Audio Codec) · Models: OuteTTS 1.0 1B, OuteTTS 1.0 0.6B, OuteTTS 0.2, OuteTTS 0.3 · [Repo](https://github.com/edwko/outetts) · [📖 Docs ↗](https://github.com/edwko/OuteTTS/blob/main/docs/interface_usage.md) · [🌐 Site ↗](https://www.outeai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/outetts/)</sub>

<a name="soprano"></a>
### #&#8288;144 [soprano](https://github.com/ekwek1/soprano) <sub>score [10](../README.md#-how-we-rank "Score 10/100. Adoption: niche (16) · Freshness: quiet (18) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · Apache-2.0 · Jan 2026</sub>

**80M-parameter English text-to-speech model with streaming and CPU support.**

Soprano is an 80M-parameter text-to-speech model that outputs 32kHz audio and runs on CUDA, CPU and Apple MPS. It ships a Gradio-style WebUI on port 7860, a CLI, a Python API with batched and streaming inference, and an OpenAI-compatible /v1/audio/speech server. The README claims under 1 GB memory use and up to 20x real-time on CPU.

- **+** Runs on CUDA, CPU and MPS; README claims under 1 GB memory
- **+** Streaming output with claimed under 250 ms latency on CPU
- **+** Several interfaces: WebUI, CLI, Python API, OpenAI-style endpoint
- **+** Fine-tuning supported through the separate Soprano-Factory repo
- **−** English only; no voice cloning or multilingual support yet
- **−** OpenAI-compatible endpoint supports non-streaming output only
- **−** Trained on about 1,000 hours; uncommon words and numbers may be mispronounced
- **−** No ROCm support; Windows CUDA needs manual PyTorch reinstall

<sub>RAM ≥ 1 GB · GPU optional · Needs PyTorch, lmdeploy (CUDA backend) · Models: Soprano-1.1-80M, Soprano-80M · port 7860 · [Repo](https://github.com/ekwek1/soprano) · [▶️ Demo ↗](https://huggingface.co/spaces/ekwek/Soprano-TTS) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/soprano/)</sub>

<a name="audino"></a>
### #&#8288;145 [audino](https://github.com/midas-research/audino) <sub>score [6](../README.md#-how-we-rank "Score 6/100. Adoption: niche (4) · Freshness: quiet (18) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · custom license · Feb 2026</sub>

**Audio annotation tool for transcription and labeling, built on CVAT.**

Audino v2.0 is a web tool for annotating audio with transcriptions and labels, used for tasks such as voice activity detection, diarization, speaker identification and emotion recognition. It is built on a CVAT backend (Django server, OPA, Redis, a database) with a React frontend, and organizes work into projects, tasks and jobs. It runs through docker compose on port 8080, and the README says it is still under active development.

- **+** Projects, tasks and jobs with custom label creation for audio annotation
- **+** Reuses CVAT's server, user groups and admin panel for access control
- **+** Exports annotations in several formats for use in other tools
- **+** Docker compose file brings up the full stack on port 8080
- **−** License is unclear: README has an MIT badge but a CC BY-NC 4.0 footer
- **−** README says v2.0 is under development, with the older version on the master branch
- **−** New users cannot view tasks until a superuser assigns groups in the admin panel
- **−** Last tagged release is from 2020; docs list no export format names

<sub>Compose · Needs Docker, Docker Compose, CVAT, Redis, OPA · port 8080 · [Repo](https://github.com/midas-research/audino) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/audino/)</sub>

<a name="pykaldi"></a>
### #&#8288;146 [pykaldi](https://github.com/pykaldi/pykaldi) <sub>score [1](../README.md#-how-we-rank "Score 1/100. Adoption: niche (2) · Freshness: quiet (1) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · Apache-2.0 · Nov 2025</sub>

**Python wrappers for the Kaldi speech recognition and OpenFst C++ libraries.**

PyKaldi is a Python scripting layer over Kaldi and OpenFst, generated with CLIF and extended in Python. It exposes Kaldi matrices, vectors, FSTs, lattices, feature extraction, decoders and nnet3 models, with NumPy conversion that does not copy buffers. High-level asr, alignment and segmentation modules run pre-trained Kaldi models, or a PyTorch acoustic model with Kaldi decoding.

- **+** Wraps most public Kaldi and OpenFst C++ APIs: decoders, lattices, nnet3, GMM/HMM, RNNLM
- **+** Matrices and vectors convert to NumPy arrays without copying memory buffers
- **+** Can decode with a PyTorch acoustic model using Kaldi decoding graphs
- **+** Reads and writes Kaldi archives and pipe-based read/write specifiers directly
- **−** No high-level ASR training API; models come from Kaldi recipes or pre-trained downloads
- **−** Last release was 2022-02-22, well behind the latest commit
- **−** Online ASR section of the README is a placeholder pointing to a script
- **−** Examples need Kaldi binaries such as compute-mfcc-feats on PATH

<sub>GPU optional · Docker · Needs Kaldi, OpenFst, CLIF, NumPy, PyTorch (optional) · Models: Kaldi nnet3 chain models, Kaldi RNNLM, PyTorch acoustic models · [Repo](https://github.com/pykaldi/pykaldi) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pykaldi/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
