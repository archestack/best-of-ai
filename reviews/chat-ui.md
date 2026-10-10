# 💬 Chat UIs reviews · Best of Open-Source AI

Web front-ends for local or API models, usually with user accounts, chat history and file upload. Back to the [leaderboard](../README.md#-chat-uis).

<sub>🌐 Also on the web: [Chat UIs on archestack.github.io](https://archestack.github.io/best-of-ai/chat-ui/), each project on its own page.</sub>

<a name="lobehub"></a>
### 🥇 [LobeHub](https://github.com/lobehub/lobehub) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (67) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 83k · custom license · Oct 2026</sub>

**Agent workspace with builder, groups, scheduling and 10,000+ MCP skills.**

LobeHub is a self-hostable agent workspace that runs on Vercel, Zeabur, Sealos, Alibaba Cloud or Docker Compose. It centres on an Agent Builder, Agent Groups that work a task in parallel, Pages for co-writing, scheduled runs, projects and shared workspaces, plus structured editable memory and an IM gateway, with 10,000+ tools and MCP-compatible plugins. An OpenAI API key is required to start.

- **+** One-click deploy buttons for Vercel, Zeabur, Sealos, RepoCloud and Alibaba Cloud
- **+** 10,000+ tools and MCP-compatible plugins for agents
- **+** Agent Groups, scheduled runs, projects and team workspaces
- **+** Memory is structured and editable rather than a hidden store
- **−** OPENAI_API_KEY is a required environment variable
- **−** Docker setup runs a curl-piped script from lobe.li before docker compose up
- **−** README recommends a third-party API reseller through an affiliate link
- **−** README states no ports, databases or hardware requirements

<sub>no GPU · Docker + Compose · Models: OpenAI, OpenAI-compatible proxy · [Repo](https://github.com/lobehub/lobehub)</sub>

<a name="anything-llm"></a>
### 🥈 [AnythingLLM](https://github.com/mintplex-labs/anything-llm) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 67k · MIT · Oct 2026</sub>

**Document chat and agent app with built-in RAG, MCP and multi-user support.**

AnythingLLM is a Node.js app that ingests PDF, TXT, DOCX and other files into a workspace and chats over them with any of 40+ LLM providers, from llama.cpp, Ollama and LM Studio to OpenAI, Anthropic, Bedrock and Gemini. It ships a native embedder, LanceDB by default plus 8 other vector stores, a no-code agent builder, MCP support, scheduled tasks, model routing and a developer API.

- **+** LanceDB embedded by default; PGVector, Qdrant, Milvus, Chroma, Weaviate, Pinecone optional
- **+** Native embedder and audio transcription run locally with no extra service
- **+** Multi-user instance with per-user permissions in the Docker build
- **+** Embeddable website chat widget and a full developer API
- **−** Anonymous telemetry to PostHog is on by default; opt out with DISABLE_TELEMETRY=true
- **−** Multi-user support and the embed widget are Docker-only, not in the desktop app
- **−** Speech-to-text is limited to the browser built-in engine
- **−** No root Dockerfile; container build lives under docker/

<sub>no GPU · Docker + Compose · Models: llama.cpp-compatible models, OpenAI, Azure OpenAI, AWS Bedrock, Anthropic · [Repo](https://github.com/mintplex-labs/anything-llm) · [📖 Docs ↗](https://docs.anythingllm.com) · [🌐 Site ↗](https://anythingllm.com)</sub>

<a name="open-webui"></a>
### 🥉 [Open WebUI](https://github.com/open-webui/open-webui) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 154k · custom license · Sep 2026</sub>

**Self-hosted chat UI for Ollama and OpenAI-compatible APIs with RBAC and RAG.**

Open WebUI is a Python-served web interface (pip or Docker, port 8080) for Ollama and any OpenAI-compatible API such as LM Studio, vLLM, OpenRouter or Groq. It bundles RAG over 9 vector databases with hybrid BM25 search, web search through 20+ providers, image generation via ComfyUI, AUTOMATIC1111, DALL-E or Gemini, MCP and OpenAPI tool servers, and per-user roles with LDAP, OAuth and SCIM provisioning.

- **+** Images tagged :ollama and :cuda bundle Ollama or CUDA acceleration in one container
- **+** RBAC, user groups, LDAP/AD, OAuth SSO and SCIM 2.0 provisioning built in
- **+** 9 vector databases incl. ChromaDB, PGVector, Qdrant, Milvus and Elasticsearch
- **+** Redis-backed sessions and WebSockets for multi-worker, multi-node deployments
- **−** Custom Open WebUI License requires keeping the Open WebUI branding visible
- **−** Enterprise plan pitched at the top of the README; Terminals isolation is enterprise-only
- **−** pip install is pinned to Python 3.11
- **−** Data is lost unless the /app/backend/data volume is mounted

<sub>GPU optional · Docker + Compose · Models: Ollama, OpenAI-compatible APIs, LM Studio, vLLM, OpenRouter · port 8080 · [Repo](https://github.com/open-webui/open-webui) · [📖 Docs ↗](https://docs.openwebui.com/) · [🌐 Site ↗](https://openwebui.com)</sub>

<a name="big-agi"></a>
### #&#8288;4 [big-AGI](https://github.com/enricoros/big-agi) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (70) · Easy to run: very easy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Oct 2026</sub>

**Multi-model chat workspace with Beam side-by-side model comparison.**

Big-AGI Open is the self-hostable web app behind big-agi.com, deployable via Docker or Vercel. It connects 20+ LLM services and 500+ models with your own API keys, and its Beam feature runs one prompt across several models and merges the answers. Personas, request inspection, web search with citations, image generation and multi-vendor speech are included; data stays local-first in the browser.

- **+** Beam and Merge: fan one prompt out to several models and reconcile the results
- **+** 20+ LLM services incl. Anthropic, OpenAI, Gemini, Ollama, LM Studio, LocalAI, Bedrock, Groq
- **+** AI Inspector shows the exact requests sent to each provider
- **+** MIT license; no usage charges, bring your own keys
- **−** Cross-device sync and 1 GB storage only on the hosted Pro tier at $10.99/month
- **−** No SSO or shared team features in the open build; managed deployments by request
- **−** README omits stack, ports and resource requirements; install guide lives in docs/
- **−** README is mostly badges, taglines and release notes rather than specs

<sub>no GPU · Docker + Compose · Models: Anthropic, OpenAI, Google Gemini, Ollama, LM Studio · [Repo](https://github.com/enricoros/big-agi) · [🌐 Site ↗](https://big-agi.com)</sub>

<a name="hermes-webui"></a>
### #&#8288;5 [Hermes WebUI](https://github.com/nesquena/hermes-webui) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

**Browser UI for Hermes Agent with sessions and file browser.**

Hermes WebUI is a Python server with a vanilla JS frontend (no build step) that gives Hermes Agent a three-panel browser interface: sessions sidebar, streaming chat over SSE, and a workspace file browser with editing. It runs the Hermes agent in-process using the existing HERMES_HOME config, and is typically reached over an SSH tunnel. It is a front end for Hermes Agent, not a standalone chat client.

- **+** No build step; plain Python server and vanilla JS frontend
- **+** Optional auth: password, passkeys/WebAuthn, or native OIDC login
- **+** Inline tool call cards and approval prompts for dangerous shell commands
- **+** Ships bootstrap.py, ctl.sh daemon wrapper, Docker, and a Nix module
- **−** Requires Hermes Agent; the UI does not work standalone
- **−** Native Windows unsupported by bootstrap; Linux, macOS, or WSL2 only
- **−** OIDC state is held in process memory; multi-instance needs sticky sessions
- **−** Gateway-backed chat is optional; full agent-loop delegation is not yet shipped

<sub>Docker + Compose · Needs Hermes Agent, Python 3 · Models: OpenAI, Anthropic, Google, DeepSeek, OpenRouter · port 8787 · [Repo](https://github.com/nesquena/hermes-webui) · [🌐 Site ↗](https://hermes-agent.nousresearch.com/)</sub>

<a name="librechat"></a>
### #&#8288;6 [LibreChat](https://github.com/librechat-ai/librechat) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 45k · MIT · Oct 2026</sub>

**Multi-provider ChatGPT-style app with agents, MCP, code interpreter and auth.**

LibreChat is a self-hosted chat platform that fronts Anthropic, OpenAI, Azure, AWS Bedrock, Google, Vertex AI and any OpenAI-compatible endpoint such as Ollama or OpenRouter. It adds agents with MCP servers, skills and subagents, a sandboxed code interpreter for Python, Node, Go, Rust and more, web search, artifacts, resumable streams, and multi-user login via OAuth2, LDAP or email with an admin panel.

- **+** Admin panel for users, groups, roles and config overrides ships in the Compose stack
- **+** Resumable streams reconnect dropped responses and sync across tabs and devices
- **+** UI translated into 30+ languages
- **+** OpenTelemetry and Langfuse export for traces and logs
- **−** Code interpreter is a separate API service, not part of this repo
- **−** File search (RAG) depends on the separate rag-api service
- **−** Horizontal scaling and resumable streams need Redis
- **−** Attached code workspaces are marked highly experimental

<sub>no GPU · Docker + Compose · Compose runs MongoDB, Meilisearch, PostgreSQL · Models: Anthropic, OpenAI, Azure OpenAI, AWS Bedrock, Google · [Repo](https://github.com/librechat-ai/librechat) · [📖 Docs ↗](https://docs.librechat.ai) · [🌐 Site ↗](https://librechat.ai)</sub>

<a name="onyx"></a>
### #&#8288;7 [Onyx](https://github.com/onyx-dot-app/onyx) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · custom license · Oct 2026</sub>

**Team knowledge chat that indexes 50+ apps for RAG and agents.**

Onyx indexes content and permissions from 50+ apps into a hybrid vector and keyword index, then answers through agentic RAG, deep research and custom agents with web search, MCP actions and a code sandbox. It works with Ollama, LiteLLM, vLLM, Anthropic, OpenAI or Gemini, deploys via Docker, Kubernetes or Helm, and is reachable from the web app, Slack and Discord bots, an MCP server or a Chrome extension.

- **+** Lite mode runs the chat UI and agents in under 1 GB of memory
- **+** Air-gappable: index, database and processing all run inside your environment
- **+** MCP server gives Claude Code, Codex or any MCP client company context with user permissions
- **+** Community Edition is MIT; install script sets up Docker in one command
- **−** SSO (OIDC, SAML), SCIM, RBAC, analytics and whitelabeling are Enterprise Edition only
- **−** Standard mode adds index, worker, inference, Redis and MinIO containers
- **−** Lite mode cannot index documents
- **−** README gives no port or hardware figures for the Standard deployment

<sub>RAM ≥ 1 GB · no GPU · Compose · Needs Redis (standard mode), MinIO (standard mode) · Models: Ollama, LiteLLM, vLLM, Anthropic, OpenAI · [Repo](https://github.com/onyx-dot-app/onyx) · [▶️ Demo ↗](https://cloud.onyx.app/signup) · [📖 Docs ↗](https://docs.onyx.app/) · [🌐 Site ↗](https://www.onyx.app/)</sub>

<a name="nextchat"></a>
### #&#8288;8 [NextChat](https://github.com/chatgptnextweb/nextchat) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: widely used (91) · Freshness: recent (78) · Maintenance: weak (29) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 89k · MIT · Oct 2026</sub>

**Lightweight Next.js chat client for OpenAI, Claude, Gemini and DeepSeek APIs.**

NextChat is a Node.js web client (Docker image yidadaa/chatgpt-next-web on port 3000, or a one-click Vercel deploy) that talks to OpenAI, Azure, Anthropic, Google Gemini, DeepSeek, Baidu, ByteDance, Alibaba, iFlytek, ChatGLM, SiliconFlow and 302.AI through environment variables. Chat history stays in the browser, access is gated by a shared CODE password list, and MCP tools switch on with ENABLE_MCP=true.

- **+** First screen about 100 KB with streaming responses; desktop client about 5 MB
- **+** Providers configured purely by environment variables; CUSTOM_MODELS edits the model list
- **+** UI in 14 languages; PWA, dark mode, Markdown with LaTeX and mermaid
- **+** Hosted demo at app.nextchat.club
- **−** No user accounts; access control is a comma-separated password list in CODE
- **−** Conversations live in browser storage; cross-device sync needs an UpStash setup
- **−** OPENAI_API_KEY is marked required even when another provider is used
- **−** Local knowledge base still unchecked on the roadmap

<sub>no GPU · Docker + Compose · Models: OpenAI, Azure OpenAI, Anthropic, Google Gemini, DeepSeek · port 3000 · [Repo](https://github.com/chatgptnextweb/nextchat) · [▶️ Demo ↗](https://app.nextchat.club) · [🌐 Site ↗](https://nextchat.club)</sub>

<a name="sillytavern"></a>
### #&#8288;9 [SillyTavern](https://github.com/sillytavern/sillytavern) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: fair (62) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · AGPL-3.0 · Sep 2026</sub>

**Local chat front end for role-play across many LLM backends.**

SillyTavern is a locally installed Node.js 20+ interface for text-generation LLMs, image generators and TTS, aimed at character and role-play chat. One UI covers KoboldAI/KoboldCpp, Horde, NovelAI, oobabooga, TabbyAPI, OpenAI, OpenRouter, Claude and Mistral, with Visual Novel Mode, AUTOMATIC1111 and ComfyUI image generation, WorldInfo lorebooks and third-party extensions. No hosted service, no tracking.

- **+** Runs on anything that can run Node.js 20; no GPU needed for the UI itself
- **+** Backends: KoboldCpp, Horde, NovelAI, oobabooga, TabbyAPI, OpenAI, OpenRouter, Claude, Mistral
- **+** WorldInfo lorebooks and deep prompt controls for long-form character chat
- **+** No hosted service and no telemetry; 300+ contributors over 3 years
- **−** AGPL-3.0 license
- **−** Single-user local tool; no accounts or team features
- **−** Maintainers describe the learning curve as steep
- **−** Installation and Docker instructions live only on the docs site

<sub>no GPU · Docker + Compose · Models: KoboldAI/KoboldCpp, Horde, NovelAI, oobabooga, TabbyAPI · [Repo](https://github.com/sillytavern/sillytavern) · [📖 Docs ↗](https://docs.sillytavern.app/)</sub>

<a name="huggingface-chat-ui"></a>
### #&#8288;10 [HuggingChat UI](https://github.com/huggingface/chat-ui) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (35) · Freshness: active (100) · Maintenance: patchy (38) · Easy to run: easy (50) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**SvelteKit chat front end behind HuggingChat for OpenAI-compatible endpoints.**

Chat UI is the SvelteKit app that powers HuggingChat. It talks only to OpenAI-compatible APIs set through OPENAI_BASE_URL, discovering models from the /models endpoint, so llama.cpp server, Ollama, OpenRouter, Poe or the HF router all work. Chat history, users and settings live in MongoDB 6/7, MCP servers can supply tools, and a heuristic Omni router picks per-message routes with fallbacks.

- **+** chat-ui-db Docker image bundles MongoDB; one container on port 3000
- **+** MCP tool calls surfaced as OpenAI function calling with per-model overrides
- **+** Same codebase as the public HuggingChat deployment
- **+** Apache-2.0 license
- **−** OpenAI-compatible endpoints only; legacy provider integrations and GGUF discovery removed
- **−** Embeddings and web-search helpers were removed from this branch
- **−** Router needs a hand-written routes JSON; no sample file ships
- **−** README does not describe authentication or multi-user setup

<sub>no GPU · Docker + Compose · Needs MongoDB · Models: OpenAI-compatible endpoints, Hugging Face Inference Providers, llama.cpp server, Ollama, OpenRouter · port 3000 · [Repo](https://github.com/huggingface/chat-ui) · [▶️ Demo ↗](https://huggingface.co/chat)</sub>

<a name="claraverse"></a>
### #&#8288;11 [ClaraVerse](https://github.com/claraverse-space/claraverse) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: patchy (46) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · custom license · Aug 2026</sub>

**Private AI workspace with chat, agent crews, workflows and Telegram.**

ClaraVerse is a Go and React workspace (Docker Compose, port 3000) that auto-detects Ollama and LM Studio and also uses OpenAI, Claude, Gemini or any OpenAI-compatible endpoint. It combines chat with Crew multi-agent teams with human review, a visual workflow builder with 200+ integrations, layered AES-256-GCM encrypted memory, knowledge bases, a Telegram channel and the claracli terminal agent.

- **+** Auto-detects Ollama and LM Studio every 2 minutes and imports their models
- **+** Per-user AES-256-GCM encrypted memory with pinned and decaying recall tiers
- **+** 150+ built-in integrations shared across chat, workflows, crew and routines
- **+** AGPL-3.0 with no branding clause or user cap
- **−** Full stack runs MySQL, MongoDB, Redis, SearXNG, Qdrant and an embeddings sidecar
- **−** Single-container mode cannot use knowledge bases or search_knowledge
- **−** 4 GB RAM minimum, 8 GB recommended
- **−** Conversations live in browser IndexedDB by default; sync is optional

<sub>RAM ≥ 4 GB · Docker + Compose · Needs MySQL, MongoDB, Redis, SearXNG, Qdrant (knowledge bases) · Models: Ollama, LM Studio, llama.cpp, OpenAI, Anthropic · port 3000 · [Repo](https://github.com/claraverse-space/claraverse) · [🌐 Site ↗](https://claraverse.space)</sub>

<a name="lollms-webui"></a>
### #&#8288;12 [LoLLMs WebUI](https://github.com/parisneo/lollms-webui) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (17) · Freshness: recent (70) · Maintenance: fair (67) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · Apache-2.0 · Sep 2026</sub>

**Single-user web UI for local and remote LLMs with many personalities.**

LoLLMs WebUI is a Python 3.11 web app (port 9600) fronting local models via HF transformers, GGUF/GGML, ExLlama v2, Ollama and vLLM bindings plus OpenAI, Anthropic and OpenRouter APIs. It adds 500+ personalities, cost/speed-based routing, and hooks into Stable Diffusion, ComfyUI, DALL-E, video and musicgen services. The authors say it is in minimal support, to be replaced by the newer lollms project.

- **+** Bindings for local GGUF, ExLlama v2 and transformers plus Ollama, vLLM and hosted APIs
- **+** Image, video and music generation integrations in one UI
- **+** Smart routing picks cheaper or faster models by prompt complexity
- **+** Apache-2.0 license
- **−** Maintainers state it is in minimal support, to be replaced by ParisNeo/lollms
- **−** No built-in authentication; designed for local use only
- **−** Docker image must be built locally; no published image in the README
- **−** Manual install needs submodules plus a per-binding install script

<sub>Docker + Compose · Models: Hugging Face transformers, GGUF/GGML, ExLlama v2, Ollama, vLLM · port 9600 · [Repo](https://github.com/parisneo/lollms-webui)</sub>

<a name="chatgpt-ui"></a>
### #&#8288;13 [ChatGPT UI](https://github.com/wongsaang/chatgpt-ui) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: niche (2) · Freshness: recent (54) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · May 2026</sub>

**Multi-user ChatGPT-style web client with pluggable databases.**

ChatGPT UI is a web client for ChatGPT-style chat that supports multiple users, multiple languages and several database backends for persistent storage. The front end lives in this repo and the API server in the separate chatgpt-ui-server repository; setup is documented on a GitHub Pages site in English and Chinese.

- **+** Multi-user accounts with persistent history
- **+** Several database backends for storage
- **+** Documentation in English and Chinese
- **−** README is a few lines; no install steps, ports or provider list
- **−** Front end and server are split across two repositories
- **−** Last commit 2026-05-11; README carries a sponsor banner for a paid AI platform

<sub>no GPU · Docker + Compose · [Repo](https://github.com/wongsaang/chatgpt-ui) · [📖 Docs ↗](https://wongsaang.github.io/chatgpt-ui/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
