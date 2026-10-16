# 💬 Chat UIs reviews · Best of Open-Source AI

Web front-ends for local or API models, usually with user accounts, chat history and file upload. Back to the [leaderboard](../README.md#-chat-uis).

<sub>🌐 Also on the web: [Chat UIs on archestack.com](https://archestack.com/best-of-ai/chat-ui/), each project on its own page.</sub>

<a name="lobehub"></a>
### 🥇 [LobeHub](https://github.com/lobehub/lobehub) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: very easy (83) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 83k · custom license · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: OpenAI, OpenAI-compatible proxy · [Repo](https://github.com/lobehub/lobehub) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lobehub/)</sub>

<a name="open-webui"></a>
### 🥈 [Open WebUI](https://github.com/open-webui/open-webui) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 156k · custom license · Oct 2026</sub>

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

<sub>GPU optional · Docker + Compose · Models: Ollama, OpenAI-compatible APIs, LM Studio, vLLM, OpenRouter · port 8080 · [Repo](https://github.com/open-webui/open-webui) · [📖 Docs ↗](https://docs.openwebui.com/) · [🌐 Site ↗](https://openwebui.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-webui/)</sub>

<a name="anything-llm"></a>
### 🥉 [AnythingLLM](https://github.com/mintplex-labs/anything-llm) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: very easy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 67k · MIT · Oct 2026</sub>

**Document chat app with agents, workspaces and many LLM and vector DB backends.**

AnythingLLM ingests PDFs, DOCX and TXT files into workspaces and answers questions over them with source citations. It connects to local or hosted LLMs (llama.cpp-compatible models, Ollama, LM Studio, OpenAI, Anthropic, Bedrock and many more) and stores vectors in LanceDB by default or PGVector, Qdrant, Weaviate, Milvus and others. It also includes a no-code agent builder, MCP support, scheduled tasks, and a desktop app plus a Docker server version.

- **+** Supports roughly 40 LLM providers and 9 vector databases, with LanceDB as the zero-setup default
- **+** Built-in embedder and audio transcription, so a local setup needs no external services
- **+** Includes no-code agent builder, MCP compatibility and cron-scheduled agent tasks
- **+** Available as a desktop app for Mac, Windows and Linux, and as a Docker server
- **−** Multi-user permissions and the embeddable chat widget are Docker version only
- **−** Telemetry is on by default; opt out via DISABLE_TELEMETRY or in-app
- **−** Still makes outbound calls to cdn.anythingllm.com and GitHub with telemetry disabled
- **−** Browser-native STT is the only speech-to-text option listed

<sub>GPU optional · Docker + Compose · Needs LLM provider (local or API), Docker (for server version) · Models: llama.cpp-compatible models, Ollama, LM Studio, OpenAI, Anthropic · [Repo](https://github.com/mintplex-labs/anything-llm) · [📖 Docs ↗](https://docs.anythingllm.com) · [🌐 Site ↗](https://anythingllm.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/anything-llm/)</sub>

<a name="onyx"></a>
### #&#8288;4 [Onyx](https://github.com/onyx-dot-app/onyx) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · custom license · Oct 2026</sub>

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

<sub>RAM ≥ 1 GB · no GPU · Compose · Needs Redis (standard mode), MinIO (standard mode) · Models: Ollama, LiteLLM, vLLM, Anthropic, OpenAI · [Repo](https://github.com/onyx-dot-app/onyx) · [▶️ Demo ↗](https://cloud.onyx.app/signup) · [📖 Docs ↗](https://docs.onyx.app/) · [🌐 Site ↗](https://www.onyx.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onyx/)</sub>

<a name="odysseus"></a>
### #&#8288;5 [odysseus](https://github.com/odysseus-dev/odysseus) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: patchy (39) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 94k · AGPL-3.0 · Oct 2026</sub>

**Self-hosted workspace for chat, agents, email, documents, notes and calendar.**

Odysseus is a self-hosted web workspace that combines chat with local or API models, tool-using agents, deep research, a document editor, an IMAP/SMTP email client, and notes with CalDAV calendar sync. Agents can use MCP, files, shell, skills and memory. A model cookbook recommends, downloads and serves models based on the host hardware.

- **+** Covers chat, email, documents, notes and CalDAV calendar in one app
- **+** Agents support MCP, shell, files, skills and memory
- **+** Built-in blind side-by-side model comparison and multi-step deep research
- **+** Compose file pulls a prebuilt multi-arch image from ghcr.io
- **−** Ships local shell and file tools; auth must stay enabled when exposed
- **−** Default branch is dev; the more curated branch is main
- **−** AGPL-3.0 license restricts closed-source network use
- **−** RAM and VRAM requirements are not stated in the README

<sub>GPU optional · Docker + Compose · Needs Docker, Docker Compose · Models: local models, API models, MCP · port 7011 · [Repo](https://github.com/odysseus-dev/odysseus) · [▶️ Demo ↗](https://odysseus-dev.github.io/odysseus/) · [🌐 Site ↗](https://odysseus-dev.github.io/odysseus/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/odysseus/)</sub>

<a name="hermes-webui"></a>
### #&#8288;6 [Hermes WebUI](https://github.com/nesquena/hermes-webui) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: easy (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

**Browser front-end for Hermes Agent with sessions, workspace files and profiles.**

Hermes WebUI is a three-panel web interface for Nous Research's Hermes Agent, written in Python with vanilla JS and no build step. It runs the agent in-process using your existing Hermes config, and adds streaming chat, tool call cards, session projects and tags, a workspace file browser and profile switching. Optional password, passkey and OIDC login are available; native Windows is not supported by the bootstrap.

- **+** No build step or bundler: Python backend with vanilla JS frontend
- **+** Reuses existing Hermes Agent config, models and memory without extra setup
- **+** Optional password, passkey/WebAuthn and OIDC auth; off by default for localhost
- **+** Includes ctl.sh daemon control, Docker, compose and a Nix flake/module
- **−** Requires Hermes Agent; bootstrap installs it via a curl-piped script if missing
- **−** Native Windows not supported by bootstrap; community guide only
- **−** OIDC state is in process memory, so multi-instance needs sticky sessions
- **−** Full agent-loop delegation to an external gateway is not yet shipped

<sub>no GPU · Docker + Compose · Needs Hermes Agent, Python 3 · Models: OpenAI, Anthropic, Google, DeepSeek, OpenRouter · port 8787 · [Repo](https://github.com/nesquena/hermes-webui) · [📖 Docs ↗](https://github.com/nesquena/hermes-webui/blob/master/docs/onboarding.md) · [🌐 Site ↗](https://get-hermes.ai/setup/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hermes-webui/)</sub>

<a name="big-agi"></a>
### #&#8288;7 [big-AGI](https://github.com/enricoros/big-agi) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: fair (69) · Easy to run: very easy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: Anthropic, OpenAI, Google Gemini, Ollama, LM Studio · [Repo](https://github.com/enricoros/big-agi) · [🌐 Site ↗](https://big-agi.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/big-agi/)</sub>

<a name="nextchat"></a>
### #&#8288;8 [NextChat](https://github.com/chatgptnextweb/nextchat) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (90) · Freshness: recent (78) · Maintenance: patchy (33) · Easy to run: very easy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 89k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: OpenAI, Azure OpenAI, Anthropic, Google Gemini, DeepSeek · port 3000 · [Repo](https://github.com/chatgptnextweb/nextchat) · [▶️ Demo ↗](https://app.nextchat.club) · [🌐 Site ↗](https://nextchat.club) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nextchat/)</sub>

<a name="librechat"></a>
### #&#8288;9 [LibreChat](https://github.com/librechat-ai/librechat) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 46k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Compose runs MongoDB, Meilisearch, PostgreSQL · Models: Anthropic, OpenAI, Azure OpenAI, AWS Bedrock, Google · [Repo](https://github.com/librechat-ai/librechat) · [📖 Docs ↗](https://docs.librechat.ai) · [🌐 Site ↗](https://librechat.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/librechat/)</sub>

<a name="sillytavern"></a>
### #&#8288;10 [SillyTavern](https://github.com/sillytavern/sillytavern) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (62) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · AGPL-3.0 · Sep 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: KoboldAI/KoboldCpp, Horde, NovelAI, oobabooga, TabbyAPI · [Repo](https://github.com/sillytavern/sillytavern) · [📖 Docs ↗](https://docs.sillytavern.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sillytavern/)</sub>

<a name="huggingface-chat-ui"></a>
### #&#8288;11 [HuggingChat UI](https://github.com/huggingface/chat-ui) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: patchy (39) · Easy to run: easy (67) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**SvelteKit chat front-end for any OpenAI-compatible API, behind HuggingChat.**

Chat UI is a SvelteKit web app that talks to any OpenAI-compatible endpoint, discovering models from the /models route. It stores users, history and settings in MongoDB, with an embedded fallback for local development. It also supports MCP tool calling, an optional "Omni" router that picks a model per request, and an experimental ML Intern mode for Hugging Face Hub work.

- **+** Works with llama.cpp, Ollama, OpenRouter, Poe and HF Inference Providers via one base URL
- **+** Embedded MongoDB persisted to ./db when MONGODB_URL is unset, so dev setup needs no database
- **+** MCP server support with per-user servers, health checks and tool call display
- **+** Same codebase that runs HuggingChat in production
- **−** OpenAI-compatible APIs only; legacy provider integrations, GGUF discovery and embeddings were removed
- **−** Requires MongoDB 6/7 for real deployments
- **−** No sample routes file ships for the Omni router; you must write the JSON
- **−** Production deploy may need a SvelteKit adapter; README gives no guidance

<sub>no GPU · Docker + Compose · Needs MongoDB 6/7 (embedded fallback for dev), OpenAI-compatible API endpoint, Node.js/npm · Models: OpenAI-compatible APIs, Hugging Face Inference Providers, llama.cpp server, Ollama, OpenRouter · port 3000 · [Repo](https://github.com/huggingface/chat-ui) · [▶️ Demo ↗](https://huggingface.co/chat) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/huggingface-chat-ui/)</sub>

<a name="claraverse"></a>
### #&#8288;12 [ClaraVerse](https://github.com/claraverse-space/claraverse) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: patchy (46) · Easy to run: easy (67) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · custom license · Aug 2026</sub>

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

<sub>RAM ≥ 4 GB · Docker + Compose · Needs MySQL, MongoDB, Redis, SearXNG, Qdrant (knowledge bases) · Models: Ollama, LM Studio, llama.cpp, OpenAI, Anthropic · port 3000 · [Repo](https://github.com/claraverse-space/claraverse) · [🌐 Site ↗](https://claraverse.space) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/claraverse/)</sub>

<a name="lollms-webui"></a>
### #&#8288;13 [LoLLMs WebUI](https://github.com/parisneo/lollms-webui) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (10) · Freshness: recent (70) · Maintenance: fair (67) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · Apache-2.0 · Oct 2026</sub>

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

<sub>Docker + Compose · Models: Hugging Face transformers, GGUF/GGML, ExLlama v2, Ollama, vLLM · port 9600 · [Repo](https://github.com/parisneo/lollms-webui) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lollms-webui/)</sub>

<a name="gpt-academic"></a>
### #&#8288;14 [gpt_academic](https://github.com/binary-husky/gpt_academic) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: widely used (82) · Freshness: quiet (26) · Maintenance: weak (13) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · GPL-3.0 · Jan 2026</sub>

**Gradio web UI with plugins for translating and polishing papers and code.**

GPT Academic is a Python Gradio app that sends text to OpenAI, Azure, Qwen, GLM, ERNIE, Spark and local models such as ChatGLM and MOSS. It adds one-click buttons and hot-reloadable Python plugins for polishing, translating arXiv, LaTeX and PDF papers, summarizing, code analysis and mermaid diagrams. Configuration is read from config.py, config_private.py or environment variables.

- **+** Plugins for arXiv, LaTeX and PDF paper translation, proofreading and summarization
- **+** Many backends: OpenAI, Azure, Qwen, GLM4, ERNIE, Spark, local ChatGLM and MOSS
- **+** Plugins are plain Python files with hot reload; buttons are defined in core_functional.py
- **+** Several API keys can be listed together in one setting
- **−** Documentation is mostly Chinese; the English README is a separate translated file
- **−** Gradio compatibility issues; requirements.txt versions must be used exactly
- **−** Full-capability Docker image bundles CUDA and LaTeX and is large
- **−** No user accounts mentioned; last tagged release is December 2024

<sub>GPU optional · Docker + Compose · Needs Python 3.9-3.11, Gradio, LaTeX (for LaTeX plugins), Docker (optional) · Models: OpenAI GPT, Azure, Qwen, ChatGLM, GLM4 · [Repo](https://github.com/binary-husky/gpt_academic) · [▶️ Demo ↗](https://huggingface.co/spaces/qingxu98/gpt-academic) · [📖 Docs ↗](https://github.com/binary-husky/gpt_academic/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpt-academic/)</sub>

<a name="chuanhuchatgpt"></a>
### #&#8288;15 [chuanhuchatgpt](https://github.com/gaizhenbiao/chuanhuchatgpt) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (29) · Freshness: recent (79) · Maintenance: weak (16) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · GPL-3.0 · Sep 2026</sub>

**Gradio web chat UI for OpenAI, Claude, Gemini, DeepSeek and local LLMs.**

Chuanhu Chat is a Python and Gradio web interface for hosted APIs (OpenAI, Azure OpenAI, Gemini, Claude, DeepSeek, MiniMax and others) and locally loaded models such as ChatGLM, LLaMA and Qwen. It adds saved per-user chat history, file-based Q&A, web search, an AutoGPT-style assistant and GPT-3.5 fine-tuning. Setup is pip install plus a config.json holding API keys.

- **+** Covers many providers, including Chinese ones such as iFlytek Spark, Inspur Yuan and MiniMax
- **+** Chat history with regex search, renaming, LLM auto-titling and per-user isolation
- **+** Multiple API keys with load balancing, plus custom api-host and proxy settings
- **+** Installable as a PWA with a mobile-friendly layout
- **−** Local model list is older (ChatGLM, LLaMA, StableLM, MOSS, Qwen); no GGUF or Ollama mentioned
- **−** Last release was 2025-08-15, and the main README is in Chinese
- **−** Built on Gradio, so the UI is bounded by that framework
- **−** GPL-3.0 license restricts use in closed-source derivative products

<sub>GPU optional · Docker · Needs Python, Gradio, API keys for hosted providers · Models: OpenAI, Azure OpenAI, Google Gemini, Claude, DeepSeek · [Repo](https://github.com/gaizhenbiao/chuanhuchatgpt) · [▶️ Demo ↗](https://huggingface.co/spaces/JohnSmith9982/ChuanhuChatGPT) · [📖 Docs ↗](https://github.com/GaiZhenbiao/ChuanhuChatGPT/wiki) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chuanhuchatgpt/)</sub>

<a name="chatgpt-ui"></a>
### #&#8288;16 [ChatGPT UI](https://github.com/wongsaang/chatgpt-ui) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: niche (1) · Freshness: recent (53) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · May 2026</sub>

**Multi-user ChatGPT-style web client with pluggable databases.**

ChatGPT UI is a web client for ChatGPT-style chat that supports multiple users, multiple languages and several database backends for persistent storage. The front end lives in this repo and the API server in the separate chatgpt-ui-server repository; setup is documented on a GitHub Pages site in English and Chinese.

- **+** Multi-user accounts with persistent history
- **+** Several database backends for storage
- **+** Documentation in English and Chinese
- **−** README is a few lines; no install steps, ports or provider list
- **−** Front end and server are split across two repositories
- **−** Last commit 2026-05-11; README carries a sponsor banner for a paid AI platform

<sub>no GPU · Docker + Compose · [Repo](https://github.com/wongsaang/chatgpt-ui) · [📖 Docs ↗](https://wongsaang.github.io/chatgpt-ui/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatgpt-ui/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
