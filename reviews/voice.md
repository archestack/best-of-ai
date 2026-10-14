# 🎙️ Voice reviews · Best of Open-Source AI

Speech-to-text, text-to-speech, voice agents and meeting tools that run locally. Back to the [leaderboard](../README.md#%EF%B8%8F-voice).

<sub>🌐 Also on the web: [Voice on archestack.com](https://archestack.com/best-of-ai/voice/), each project on its own page.</sub>

<a name="whisper-cpp"></a>
### 🥇 [whisper.cpp](https://github.com/ggml-org/whisper.cpp) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 54k · MIT · Oct 2026</sub>

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
### 🥈 [Voicebox](https://github.com/jamiepine/voicebox) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (54) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 57k · MIT · Oct 2026</sub>

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

<a name="speech-to-speech"></a>
### 🥉 [Speech-to-Speech](https://github.com/huggingface/speech-to-speech) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**Modular voice-agent pipeline exposed through the OpenAI Realtime API.**

Runs a VAD, STT, LLM and TTS cascade, with each stage in its own thread and every backend swappable by CLI flag. It serves the core OpenAI Realtime event set over WebSocket and WebRTC, so existing Realtime clients can point at it. Defaults are Parakeet TDT for speech recognition and Qwen3-TTS for speech output, with the LLM running locally or through any OpenAI-compatible endpoint.

- **+** Implements core OpenAI Realtime events over WebSocket and WebRTC, so client swaps are easy
- **+** Fully local on Apple Silicon (MLX) or NVIDIA CUDA, with no API key needed
- **+** Many interchangeable STT and TTS backends, including Whisper, Kokoro, Pocket TTS and OmniVoice
- **+** Apache-2.0, installable from PyPI, with a packaged microphone client
- **−** Qwen3-TTS GGML wheel targets CUDA 12.8 and glibc 2.39 by default
- **−** Fully local NVIDIA setup budgets about 24 GB VRAM; the README calls this an estimate
- **−** Only the core Realtime event set is implemented, not the full API
- **−** Some extras conflict, e.g. DeepFilterNet needs numpy<2 while Pocket TTS needs numpy>=2

<sub>RAM ≥ 16 GB · GPU optional · Docker + Compose · Needs OpenAI-compatible LLM server (optional), PortAudio and libsndfile on Ubuntu · Models: Parakeet TDT, Qwen3-TTS, Whisper, Kokoro-82M, Transformers LLMs · port 8765 · [Repo](https://github.com/huggingface/speech-to-speech) · [📖 Docs ↗](https://github.com/huggingface/speech-to-speech/blob/main/docs/configuration.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/speech-to-speech/)</sub>

<a name="kokoro-fastapi"></a>
### #&#8288;4 [Kokoro-FastAPI](https://github.com/remsky/kokoro-fastapi) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.5k · Apache-2.0 · Oct 2026</sub>

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

<a name="pocket-tts"></a>
### #&#8288;5 [Pocket TTS](https://github.com/kyutai-labs/pocket-tts) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · MIT · Oct 2026</sub>

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

<a name="openreader"></a>
### #&#8288;6 [OpenReader](https://github.com/richardr1126/openreader) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 540 · MIT · Oct 2026</sub>

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

<a name="index-tts"></a>
### #&#8288;7 [IndexTTS](https://github.com/index-tts/index-tts) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: known (49) · Freshness: active (100) · Maintenance: fair (77) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Sep 2026</sub>

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

<a name="gpt-sovits"></a>
### #&#8288;8 [GPT-SoVITS](https://github.com/rvc-boss/gpt-sovits) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (85) · Freshness: recent (74) · Maintenance: patchy (34) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 63k · MIT · Oct 2026</sub>

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
### #&#8288;9 [vibevoice](https://github.com/microsoft/vibevoice) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: patchy (36) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 55k · MIT · Oct 2026</sub>

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
### #&#8288;10 [F5-TTS](https://github.com/swivid/f5-tts) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (42) · Freshness: active (100) · Maintenance: patchy (49) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Oct 2026</sub>

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
### #&#8288;11 [Speakr](https://github.com/murtaza-nasir/speakr) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · AGPL-3.0 · Oct 2026</sub>

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

<a name="whisper"></a>
### #&#8288;12 [whisper](https://github.com/openai/whisper) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: widely used (96) · Freshness: recent (75) · Maintenance: weak (20) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 110k · MIT · Aug 2026</sub>

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

<a name="whisperlive"></a>
### #&#8288;13 [WhisperLive](https://github.com/collabora/whisperlive) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: fair (68) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Oct 2026</sub>

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
### #&#8288;14 [chattts](https://github.com/2noise/chattts) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (62) · Freshness: recent (75) · Maintenance: weak (19) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · AGPL-3.0 · Apr 2026</sub>

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

<a name="speaches"></a>
### #&#8288;15 [Speaches](https://github.com/speaches-ai/speaches) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (8) · Freshness: recent (68) · Maintenance: weak (8) · Easy to run: easy (67) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Apr 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
