# 🎙️ Voice — reviews

Speech-to-text, text-to-speech, voice agents and meeting tools that run locally. Back to the [leaderboard](../README.md#%EF%B8%8F-voice).

<a name="speech-to-speech"></a>
### 🥈 75 [Speech-to-Speech](https://github.com/huggingface/speech-to-speech) <sub>⭐ 13k · Apache-2.0 · Oct 2026</sub>

**Modular voice-agent pipeline behind an OpenAI Realtime-compatible server.**

Runs a VAD, speech-to-text, LLM and text-to-speech cascade and exposes it through the OpenAI Realtime event set over WebSocket and WebRTC at ws://127.0.0.1:8765/v1/realtime. Defaults are Silero VAD, Parakeet TDT and Qwen3-TTS, with the LLM slot pointed at any OpenAI-compatible server, Transformers or mlx-lm. For teams building voice agents or devices that already speak the Realtime protocol.

- **+** Every stage is swappable: 12+ STT backends, 3 LLM backends, 7 TTS backends
- **+** OpenAI Agents SDK tested against both WebSocket and WebRTC transports
- **+** Fully local presets for Apple Silicon (MLX) and NVIDIA CUDA; no API key needed
- **+** pip install; one command runs the server and microphone client together
- **−** Fully local NVIDIA setup budgets 24 GB VRAM; Apple Silicon 16 GB unified memory
- **−** Default LLM is a hosted OpenAI model, so transcripts leave the machine unless changed
- **−** Linux Qwen3-TTS wheel targets CUDA 12.8 and glibc 2.39; older systems need manual wheels
- **−** DeepFilterNet audio enhancement conflicts with Pocket TTS (numpy<2 vs numpy>=2)

<sub>GPU optional · Docker + Compose · Needs libportaudio2, libsndfile1 · Models: Parakeet TDT, Whisper and Faster Whisper, Qwen3-ASR, Qwen3-TTS, Kokoro-82M · port 8765 · [Repo](https://github.com/huggingface/speech-to-speech)</sub>

<a name="voicebox"></a>
### 🥈 72 [Voicebox](https://github.com/jamiepine/voicebox) <sub>⭐ 57k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker + Compose · Models: Qwen3-TTS 0.6B/1.7B, Qwen CustomVoice, Qwen VoiceDesign, LuxTTS, Chatterbox Multilingual · port 17493 · [Repo](https://github.com/jamiepine/voicebox) · [📖 Docs ↗](https://docs.voicebox.sh) · [🌐 Site ↗](https://voicebox.sh)</sub>

<a name="pocket-tts"></a>
### 🥈 72 [Pocket TTS](https://github.com/kyutai-labs/pocket-tts) <sub>⭐ 9.8k · MIT · Oct 2026</sub>

**100M-parameter CPU text-to-speech with streaming and voice cloning.**

Generates speech on CPU with a 100M-parameter model: about 200 ms to the first audio chunk and roughly 6x real time on an M4 MacBook Air using two cores. Covers English, French, German, Portuguese, Italian, Spanish and Dutch, clones a voice from a WAV file, and runs as a CLI, a Python library or an HTTP server with a web UI on port 8000. For developers who want TTS without a GPU.

- **+** Runs on 2 CPU cores; no CUDA build of PyTorch needed
- **+** Streaming output with about 200 ms first-chunk latency
- **+** Voice cloning from any WAV; export voices to safetensors for fast loading
- **+** Training code released; community models load via --config
- **−** Seven European languages; others depend on community-trained models
- **−** No pause or silence markup in text input
- **−** serve command and Docker image are CPU-only; GPU use is unsupported and manual
- **−** Linux pip pulls CUDA PyTorch (about 3 GB) unless the CPU index is set

<sub>no GPU · Docker + Compose · Models: Pocket TTS 100M, 24-layer language variants, community checkpoints via --config · port 8000 · [Repo](https://github.com/kyutai-labs/pocket-tts) · [▶️ Demo ↗](https://kyutai.org/pocket-tts) · [📖 Docs ↗](https://kyutai-labs.github.io/pocket-tts/)</sub>

<a name="gpt-sovits"></a>
### 🥈 67 [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS) <sub>⭐ 63k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker + Compose · Needs ffmpeg · Models: GPT-SoVITS v1-v5 pretrained models, UVR5 vocal separation models, Faster Whisper large-v3 (ASR), FunASR Paraformer (Chinese ASR) · [Repo](https://github.com/RVC-Boss/GPT-SoVITS) · [▶️ Demo ↗](https://lj1995-gpt-sovits-proplus.hf.space/) · [📖 Docs ↗](https://rentry.co/GPT-SoVITS-guide#/)</sub>

<a name="kokoro-fastapi"></a>
### 🥉 64 [Kokoro-FastAPI](https://github.com/remsky/Kokoro-FastAPI) <sub>⭐ 5.5k · Apache-2.0 · Oct 2026</sub>

**OpenAI-compatible Kokoro-82M speech API in CPU and GPU images.**

Serves the Kokoro-82M model behind an OpenAI-compatible /v1/audio/speech endpoint on port 8880, streaming mp3, wav, opus, flac, aac or pcm. Covers English (US/GB), Spanish, French, Hindi, Italian, Japanese, Brazilian Portuguese and Mandarin, with weighted voice mixing, inline [voice:] and [pause:] tags, word timestamps and phoneme endpoints. Prebuilt images exist for CPU, CUDA (amd64 and arm64) and experimental ROCm.

- **+** Drop-in for the OpenAI Python client; models baked into the images
- **+** Weighted voice mixing and inline speaker, pause, rate and IPA tags
- **+** Per-word timestamp captions and phoneme in/out endpoints
- **+** First-token latency about 300 ms on GPU
- **−** CPU first-token latency: 3.5 s on an older i7, under 1 s on M3 Pro
- **−** No true voice cloning; /dev/tune only nudges toward a reference clip
- **−** ROCm image is experimental and amd64 only
- **−** Apple Silicon GPU (MPS) only when run natively via uv, not in Docker

<sub>GPU optional · Needs espeak-ng (optional fallback) · Models: Kokoro-82M v1.0 · port 8880 · [Repo](https://github.com/remsky/Kokoro-FastAPI) · [▶️ Demo ↗](https://huggingface.co/spaces/Remsky/FastKoko)</sub>

<a name="f5-tts"></a>
### 🥉 58 [F5-TTS](https://github.com/SWivid/F5-TTS) <sub>⭐ 15k · MIT · Sep 2026</sub>

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

<sub>Docker · Needs ffmpeg · Models: F5-TTS v1 Base, E2 TTS, Vocos and BigVGAN vocoders · port 7860 · [Repo](https://github.com/SWivid/F5-TTS) · [▶️ Demo ↗](https://huggingface.co/spaces/mrfakename/E2-F5-TTS)</sub>

<a name="index-tts"></a>
### 🥉 56 [IndexTTS](https://github.com/index-tts/index-tts) <sub>⭐ 24k · NOASSERTION · Sep 2026</sub>

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

<sub>Needs uv · Models: IndexTTS-2.5, IndexTTS-2, IndexTTS-1.5 (legacy) · port 7860 · [Repo](https://github.com/index-tts/index-tts) · [▶️ Demo ↗](https://huggingface.co/spaces/IndexTeam/IndexTTS-2.5-Demo)</sub>

<a name="whisperlive"></a>
### 52 [WhisperLive](https://github.com/collabora/WhisperLive) <sub>⭐ 4.3k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Needs PortAudio (client microphone input) · Models: Whisper via faster-whisper (CTranslate2), Whisper TensorRT-LLM engines, OpenVINO Whisper models · port 9090 · [Repo](https://github.com/collabora/WhisperLive)</sub>

<a name="openreader"></a>
### 51 [OpenReader](https://github.com/richardr1126/openreader) <sub>⭐ 539 · MIT · Oct 2026</sub>

**Reads EPUB, PDF and DOCX aloud with synced word highlighting.**

Next.js server that narrates EPUB, PDF, TXT, Markdown and DOCX files with synchronized read-along, generating audio ahead of playback through a self-hosted OpenAI-compatible TTS server (Kokoro-FastAPI, KittenTTS-FastAPI, Orpheus-FastAPI) or OpenAI, Replicate and DeepInfra. PDF layout is parsed with PP-DocLayoutV3 and words aligned with ONNX Whisper in a NATS JetStream worker. Exports M4B or MP3 audiobooks.

- **+** Layout-aware PDF parsing and word-by-word highlighting
- **+** Audio cache reused across seeks, reloads and audiobook export
- **+** Storage on embedded SeaweedFS or S3; SQLite or Postgres; built-in auth
- **+** amd64 and arm64 Docker images with automatic startup migrations
- **−** Needs a separate TTS server or cloud TTS API; nothing is bundled
- **−** Word alignment and DOCX conversion run in a NATS JetStream compute worker you deploy
- **−** Setup details (ports, env vars) are only in the external docs

<sub>no GPU · Docker · Needs OpenAI-compatible TTS server or cloud TTS API, NATS JetStream (compute worker), SQLite or PostgreSQL, SeaweedFS (embedded) or S3-compatible storage · Models: Kokoro-FastAPI, KittenTTS-FastAPI, Orpheus-FastAPI, OpenAI TTS, Replicate · [Repo](https://github.com/richardr1126/openreader) · [📖 Docs ↗](https://docs.openreader.richardr.dev/)</sub>

<a name="speakr"></a>
### 50 [Speakr](https://github.com/murtaza-nasir/speakr) <sub>⭐ 4.1k · AGPL-3.0 · Oct 2026</sub>

**Transcribe, summarize and search recordings with pluggable ASR and LLMs.**

Web app that records or ingests audio, transcribes it through a connector (self-hosted WhisperX, OpenAI, Mistral Voxtral, AssemblyAI, OpenASR, FunASR), then writes summaries, action items and per-recording chat with an OpenAI-compatible LLM, OpenRouter or Ollama. Adds diarization, voice profiles, OIDC SSO, groups, a Swagger REST API and signed webhooks. Flask app on port 8899 with SQLite or PostgreSQL.

- **+** Eight ASR connectors auto-detected from config; WhisperX enables voice profiles
- **+** Multi-user with OIDC SSO (Keycloak, Azure AD, Google, Auth0), groups and sharing
- **+** REST API v1 with Swagger UI, HMAC-signed webhooks, per-user token budgets
- **+** Lite image (about 725 MB) skips PyTorch; full image is about 4.4 GB
- **−** Still alpha (v0.10.13-alpha) with frequent feature churn between releases
- **−** No bundled ASR; needs an API key or a separate GPU WhisperX container
- **−** Dual-licensed: AGPLv3, or a paid commercial license for proprietary use
- **−** Lite image downgrades Inquire semantic search to basic text search

<sub>no GPU · Docker · Needs ASR service or API (WhisperX, OpenAI, Mistral, AssemblyAI, OpenASR, FunASR), LLM API (OpenAI-compatible, OpenRouter or Ollama), SQLite or PostgreSQL · Models: WhisperX, OpenAI gpt-4o-transcribe-diarize, Mistral Voxtral, AssemblyAI, VibeVoice via vLLM · port 8899 · [Repo](https://github.com/murtaza-nasir/speakr) · [📖 Docs ↗](https://murtaza-nasir.github.io/speakr)</sub>

<a name="speaches"></a>
### 48 [Speaches](https://github.com/speaches-ai/speaches) <sub>⭐ 3.7k · MIT · Apr 2026</sub>

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

<sub>GPU optional · Docker + Compose · Models: faster-whisper (CTranslate2 Whisper), Kokoro, Piper · [Repo](https://github.com/speaches-ai/speaches) · [📖 Docs ↗](https://speaches.ai/) · [🌐 Site ↗](https://speaches.ai/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
