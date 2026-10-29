# 💬 Chat UIs reviews · Best of Open-Source AI

Web front-ends for local or API models, usually with user accounts, chat history and file upload. Back to the [leaderboard](../README.md#-chat-uis).

<sub>🌐 Also on the web: [Chat UIs on archestack.com](https://archestack.com/best-of-ai/chat-ui/), each project on its own page.</sub>

<a name="open-webui"></a>
### 🥇 [Open WebUI](https://github.com/open-webui/open-webui) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 157k · custom license · Oct 2026</sub>

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

<a name="lobehub"></a>
### 🥈 [LobeHub](https://github.com/lobehub/lobehub) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · custom license · Oct 2026</sub>

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

<a name="onyx"></a>
### 🥉 [Onyx](https://github.com/onyx-dot-app/onyx) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · custom license · Oct 2026</sub>

**Team knowledge search and chat that indexes 50+ connected apps with permissions.**

Onyx indexes content from 50+ applications along with metadata and permissions, then serves it through a chat UI with agentic RAG, deep research, custom agents, web search, MCP actions and a code sandbox. It works with self-hosted and hosted LLM providers such as Ollama, vLLM, LiteLLM, OpenAI, Anthropic and Gemini. A Lite mode runs the chat and agents without document indexing.

- **+** Indexes 50+ connectors with source permissions, so answers respect existing access controls
- **+** Hybrid vector and keyword index plus a retrieval-tuned agent for search
- **+** Works with Ollama, vLLM, LiteLLM and major hosted LLM providers
- **+** Exposes an MCP server, Slack and Discord bots, Chrome extension and embeddable widget
- **−** Standard mode needs a multi-service stack: index, workers, Redis, MinIO and model inference servers
- **−** SSO, SCIM, RBAC and analytics are in the Enterprise Edition
- **−** Lite mode cannot index documents
- **−** License detected as NOASSERTION; README claims MIT for Community Edition only

<sub>GPU optional · Compose · Needs Redis, MinIO, vector and keyword index, Docker or Kubernetes · Models: Ollama, vLLM, LiteLLM, OpenAI, Anthropic · [Repo](https://github.com/onyx-dot-app/onyx) · [▶️ Demo ↗](https://cloud.onyx.app/auth/signup) · [📖 Docs ↗](https://docs.onyx.app/welcome) · [🌐 Site ↗](https://www.onyx.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/onyx/)</sub>

<a name="anything-llm"></a>
### #&#8288;4 [AnythingLLM](https://github.com/mintplex-labs/anything-llm) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · MIT · Oct 2026</sub>

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

<a name="librechat"></a>
### #&#8288;5 [LibreChat](https://github.com/librechat-ai/librechat) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 46k · MIT · Oct 2026</sub>

**Self-hosted multi-provider chat UI with agents, MCP tools and multi-user auth.**

LibreChat is a ChatGPT-style web interface that connects to Anthropic, OpenAI, Azure, Google, AWS Bedrock, Ollama and any OpenAI-compatible endpoint. It adds multi-user login (OAuth2, LDAP, email), conversation search and branching, no-code agents with MCP tools, a sandboxed code interpreter, artifacts and web search. An admin panel manages users, roles and settings.

- **+** Many providers in one UI, plus custom OpenAI-compatible endpoints without a proxy
- **+** Multi-user auth via OAuth2, LDAP and email, with admin panel and token spend tools
- **+** Agents with MCP servers, Skills, subagents, file search and code execution
- **+** Resumable streams and Redis support for horizontally scaled deployments
- **−** Large feature surface; the README lists many components to configure and operate
- **−** Some features, such as attached code workspaces, are marked highly experimental
- **−** Code interpreter relies on a separate ClickHouse/code-interpreter service
- **−** README gives no RAM or hardware requirements and no default port

<sub>no GPU · Docker + Compose · Needs Docker Compose (optional), Redis (for scaled deployments), ClickHouse/code-interpreter (for code execution), LibreChat RAG API (for file chat) · Models: Anthropic, OpenAI, Azure OpenAI, Google, Vertex AI · [Repo](https://github.com/librechat-ai/librechat) · [📖 Docs ↗](https://www.librechat.ai/docs) · [🌐 Site ↗](https://librechat.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/librechat/)</sub>

<a name="hermes-webui"></a>
### #&#8288;6 [Hermes WebUI](https://github.com/nesquena/hermes-webui) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Oct 2026</sub>

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

<a name="odysseus"></a>
### #&#8288;7 [odysseus](https://github.com/odysseus-dev/odysseus) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 95k · AGPL-3.0 · Oct 2026</sub>

**Self-hosted workspace for chat, agents, email, documents and calendar.**

Odysseus is a self-hosted web workspace that combines chat with local or API models, tool-using agents, deep research, a document editor, an IMAP/SMTP email client and a CalDAV-synced calendar. Agents can use MCP, files, shell, skills and memory. It runs through Docker Compose on port 7011 and prints the first admin password to the container logs.

- **+** Covers chat, agents, email, documents, notes, tasks and calendar in one app
- **+** Agents support MCP, shell, files, skills and memory
- **+** Includes blind side-by-side model comparison and a hardware-aware model cookbook
- **+** Official multi-arch image with immutable version-plus-SHA tags for pinning
- **−** Agents have shell and local tool access, so auth must stay enabled
- **−** AGPL-3.0 license limits closed-source network deployments
- **−** No tagged releases; default dev branch gets the newest changes first
- **−** README gives no RAM or GPU requirements

<sub>GPU optional · Docker + Compose · Needs Docker, Docker Compose · Models: local models, API models, MCP · port 7011 · [Repo](https://github.com/odysseus-dev/odysseus) · [▶️ Demo ↗](https://odysseus-dev.github.io/odysseus/) · [📖 Docs ↗](https://github.com/odysseus-dev/odysseus/blob/dev/website/setup.md) · [🌐 Site ↗](https://odysseus-dev.github.io/odysseus/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/odysseus/)</sub>

<a name="sillytavern"></a>
### #&#8288;8 [SillyTavern](https://github.com/sillytavern/sillytavern) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · AGPL-3.0 · Sep 2026</sub>

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

<a name="ekko-studio"></a>
### #&#8288;9 [ekko-studio](https://github.com/ekkolearnai/ekko-studio) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (43) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · custom license · Oct 2026</sub>

**Desktop and web workspace for chatting with Hermes, Ekko and coding agents.**

Ekko Studio (formerly Hermes Web UI) is an Electron desktop app and self-hosted Node web console that puts Hermes Agent, a built-in Ekko Agent and 14 coding-agent CLIs, including Claude Code and Codex, behind one chat UI. It adds group chat, a visual workflow editor with approval gates, scheduled jobs, a file browser, web terminal, voice and platform channels such as Telegram and Slack. Sessions are stored in local SQLite.

- **+** One UI for Hermes, Ekko and 14 coding-agent CLIs, shared by chat, group chat and workflows
- **+** Visual workflows support conditions, loops, approval gates, run budgets and execution history
- **+** Ships as desktop app (Windows/macOS/Linux), npm CLI and Docker image
- **+** Many TTS and STT provider adapters, plus 10 chat platform channels
- **−** License is reported as NOASSERTION, so terms need manual checking
- **−** Coding agents must be installed on the backend host; some need manual installation
- **−** Default bootstrap login is admin / 123456 until changed
- **−** Very broad scope; README gives no RAM or hardware requirements

<sub>no GPU · Docker + Compose · Needs Node.js (npm install), Hermes Agent (npm installs discover an existing install), Coding-agent CLIs installed on the host, pnpm (DSH native plugins) · Models: OpenAI-compatible providers, OpenAI Codex, Claude, GitHub Copilot, Nous Portal · [Repo](https://github.com/ekkolearnai/ekko-studio) · [📖 Docs ↗](https://ekkostudio.xyz/#/docs/getting-started) · [🌐 Site ↗](https://ekkostudio.xyz) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ekko-studio/)</sub>

<a name="big-agi"></a>
### #&#8288;10 [big-AGI](https://github.com/enricoros/big-agi) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · MIT · Oct 2026</sub>

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
### #&#8288;11 [NextChat](https://github.com/chatgptnextweb/nextchat) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: widely used (93) · Freshness: recent (77) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 89k · MIT · Oct 2026</sub>

**Web and desktop chat client for OpenAI, Claude, Gemini and other model APIs.**

NextChat is a Next.js chat front-end that talks to hosted APIs (OpenAI, Azure, Anthropic, Google, DeepSeek, Baidu, ByteDance, Alibaba and others) and to self-hosted backends such as LocalAI and RWKV-Runner. Chat history is stored in the browser, with optional sync via UpStash or WebDAV. It runs as a Vercel or Docker deployment on port 3000 and as a Tauri desktop client, with prompt templates (masks), plugins, artifacts and optional MCP support.

- **+** Supports many providers via env vars, including Azure, Anthropic, Gemini, DeepSeek and SiliconFlow
- **+** Chat data stays in the browser by default; no database required
- **+** Deploys via one-click Vercel or a single Docker container
- **+** Also ships a Tauri desktop client of about 5MB for Linux, Windows and macOS
- **−** Access control is a shared password list (CODE), not per-user accounts
- **−** Admin panel, permissions, knowledge base and auditing are only in the paid Enterprise Edition
- **−** Local knowledge base is unchecked on the roadmap
- **−** Last release is 2025-07-29; README docs partly Chinese-only or marked deprecated

<sub>no GPU · Docker + Compose · Needs OpenAI or other LLM API key, Node.js >= 18, Docker >= 20 (optional), UpStash (optional, chat sync) · Models: OpenAI, Azure OpenAI, Anthropic Claude, Google Gemini, DeepSeek · port 3000 · [Repo](https://github.com/chatgptnextweb/nextchat) · [▶️ Demo ↗](https://app.nextchat.club) · [🌐 Site ↗](https://nextchat.club) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nextchat/)</sub>

<a name="page-assist"></a>
### #&#8288;12 [page-assist](https://github.com/n4ze3m/page-assist) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · MIT · Oct 2026</sub>

**Browser extension with a sidebar and web UI for local models.**

Page Assist is a browser extension that adds a chat sidebar and a full-tab web UI for talking to local models from any webpage. It connects to Ollama, Chrome AI (Gemini Nano) or any OpenAI-compatible endpoint such as LM Studio or llamafile. A chat-with-webpage mode lets you ask questions about the current page, and data is stored in browser storage.

- **+** Sidebar opens on any page via Ctrl+Shift+Y; web UI opens in a tab via Ctrl+Shift+L
- **+** Chat with the current webpage, toggled with Ctrl+E
- **+** Works with Ollama, Chrome AI (Gemini Nano) and OpenAI-compatible endpoints
- **+** Chat data stays in browser storage; README states no personal data is collected
- **−** Sidebar and chat-with-webpage unsupported on Opera and Arc; only the web UI works
- **−** Needs a separate model backend such as Ollama; it does not run models itself
- **−** No user accounts or server-side history, since everything lives in the browser
- **−** Share feature contacts a server; it can be disabled in settings

<sub>Needs Ollama or an OpenAI-compatible endpoint, Bun (manual build only) · Models: Ollama, Chrome AI (Gemini Nano), OpenAI-compatible endpoints (LM Studio, llamafile) · [Repo](https://github.com/n4ze3m/page-assist) · [▶️ Demo ↗](https://www.youtube.com/watch?v=8VTjlLGXA4s) · [📖 Docs ↗](https://docs.pageassist.xyz) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/page-assist/)</sub>

<a name="huggingface-chat-ui"></a>
### #&#8288;13 [HuggingChat UI](https://github.com/huggingface/chat-ui) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: known (40) · Freshness: active (100) · Maintenance: patchy (35) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

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

<a name="chathub"></a>
### #&#8288;14 [chathub](https://github.com/chathub-dev/chathub) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: known (36) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · GPL-3.0 · Oct 2026</sub>

**Browser extension that chats with several AI chatbots side by side.**

ChatHub is a Chromium browser extension that puts multiple chatbots in one window so their answers to the same prompt can be compared. It supports ChatGPT and Claude via web app or API, plus Gemini, Grok, DeepSeek, Qianwen and Llama. Conversation history is stored locally, with a prompt library and data export and import.

- **+** Sends one prompt to several chatbots at once for side-by-side comparison
- **+** Conversation history stored locally, with export and import of all data
- **+** Supports both web app and API access for ChatGPT and Claude
- **+** Includes a prompt library and a shortcut to open it from any page
- **−** Chromium browsers only (Chrome, Edge); no other platforms listed
- **−** No self-hosted server, user accounts or Docker image
- **−** Bot list in the README is open-ended and partly unspecified
- **−** No tagged releases; install from the web store or build from source

<sub>no GPU · Needs Chromium-based browser, Node.js with corepack and yarn (build only) · Models: ChatGPT, Gemini, Claude, Grok, DeepSeek · [Repo](https://github.com/chathub-dev/chathub) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chathub/)</sub>

<a name="claraverse"></a>
### #&#8288;15 [ClaraVerse](https://github.com/claraverse-space/claraverse) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: patchy (48) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · custom license · Aug 2026</sub>

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

<a name="chuanhuchatgpt"></a>
### #&#8288;16 [chuanhuchatgpt](https://github.com/gaizhenbiao/chuanhuchatgpt) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (52) · Freshness: recent (78) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · GPL-3.0 · Sep 2026</sub>

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

<a name="lollms-webui"></a>
### #&#8288;17 [LoLLMs WebUI](https://github.com/parisneo/lollms-webui) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (7) · Freshness: recent (70) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · Apache-2.0 · Oct 2026</sub>

**Web UI for chatting with local and API LLMs, plus image and music generation.**

LoLLMs WebUI is a Python web interface that connects to many LLM backends (GGUF, ExLlamaV2, Hugging Face, Ollama, vLLM, OpenAI, Anthropic, OpenRouter and others) through installable bindings. It adds selectable personalities, local discussion storage, image, video and music generation, and prompt routing across models by cost or speed. The README says the project has minimal support and will be replaced by the newer lollms project.

- **+** Many bindings: GGUF, ExLlamaV2, Hugging Face, Ollama, vLLM, OpenAI, Anthropic, OpenRouter, Gemini, Groq
- **+** Covers text, image, video and music generation in one UI
- **+** Smart routing can pick a model per prompt by cost or speed
- **+** Install via scripts, manual venv or Docker; chats kept in a local database
- **−** Maintainer states minimal support; being replaced by the separate lollms project
- **−** No built-in user authentication; remote use needs a tunnel and headless mode
- **−** Last release is 2024-11-11, though commits continue
- **−** README gives no hardware requirements and no docs link

<sub>GPU optional · Docker + Compose · Needs Python 3.11, git submodules · Models: GGUF/GGML, ExLlamaV2, Hugging Face, Ollama, vLLM · port 9600 · [Repo](https://github.com/parisneo/lollms-webui) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lollms-webui/)</sub>

<a name="gpt-academic"></a>
### #&#8288;18 [gpt_academic](https://github.com/binary-husky/gpt_academic) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: widely used (87) · Freshness: quiet (22) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 72k · GPL-3.0 · Jan 2026</sub>

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

<a name="chatgpt-ui"></a>
### #&#8288;19 [ChatGPT UI](https://github.com/wongsaang/chatgpt-ui) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: niche (0) · Freshness: recent (70) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Oct 2026</sub>

**Multi-user ChatGPT web client with multilingual UI and selectable database backends.**

A Vue front-end for ChatGPT-style chat that supports multiple users, multiple interface languages and several database connections for persisting data. It needs the separate chatgpt-ui-server project as its backend. The README is short and defers setup, model and provider details to the external documentation site.

- **+** Multi-user accounts with persistent chat data
- **+** Supports multiple database connections for storage
- **+** Multilingual interface with English and Chinese docs
- **+** MIT license
- **−** Requires a separate backend repository (chatgpt-ui-server)
- **−** Last release is 2023-09-07
- **−** README lacks supported models, ports and resource requirements
- **−** Setup details only on external docs site

<sub>Docker + Compose · Needs chatgpt-ui-server · [Repo](https://github.com/wongsaang/chatgpt-ui) · [📖 Docs ↗](https://wongsaang.github.io/chatgpt-ui/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatgpt-ui/)</sub>

<a name="chatany"></a>
### #&#8288;20 [chatany](https://github.com/chatanyteam/chatany) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (13) · Freshness: slowing (39) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Apr 2026</sub>

**ChatGPT-Next-Web fork adding Midjourney and Stability AI image generation.**

ChatAny is a web chat client forked from ChatGPT-Next-Web that adds an image generation view for Midjourney and Stability AI (Stable Image Ultra, Core, Stable Diffusion 3). Midjourney access goes through a self-hosted midjourney-proxy or a third-party relay API. The README states the project is no longer maintained and points to the desktop client AQBot.

- **+** Midjourney operations supported: Imagine, Upscale, Variation, Zoom, Pan, Reroll, Describe, Blend, Vary Region
- **+** Shows generation progress percentage and live image preview
- **+** Keeps all ChatGPT-Next-Web features, plus Stability AI models
- **+** Deploys via Docker, Vercel, Railway, Sealos or npm build
- **−** README marks the project as no longer maintained; last release was 2024-10-30
- **−** Midjourney needs a separate midjourney-proxy service or third-party relay
- **−** Midjourney support is unofficial and depends on the proxy
- **−** Operations features such as plans and invites are only in the separate PRO version

<sub>no GPU · Docker + Compose · Needs midjourney-proxy (for Midjourney), OpenAI-compatible API · Models: OpenAI API, Midjourney (via proxy), Stable Image Ultra, Stable Image Core, Stable Diffusion 3 · port 3000 · [Repo](https://github.com/chatanyteam/chatany) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatany/)</sub>

<a name="aidea"></a>
### #&#8288;21 [aidea](https://github.com/mylxsw/aidea) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: niche (17) · Freshness: slowing (32) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · MIT · Mar 2026</sub>

**Flutter client for chatting with LLMs and generating images.**

AIdea is a Flutter app for mobile, macOS and Windows that gives one interface to several large language models and image generation models. This repo holds the client only; the Go backend lives in aidea-server, with a separate aidea-docker repo. The main branch is v2 and under active development, and the README directs self-hosters to the v1.x branch.

- **+** Single Flutter codebase with screenshots for mobile, macOS and Windows
- **+** Client, Go server and Docker deployment are separate MIT-licensed repos
- **+** Covers both chat and image generation in one app
- **−** Self-hosting needs the separate aidea-server repo and the older v1.x branch
- **−** Default v2 branch is under active development; last release is 2025-02-20
- **−** README gives no list of supported models or providers
- **−** README says Flutter builds often fail as versions change

<sub>Docker · Needs aidea-server (Go backend) · [Repo](https://github.com/mylxsw/aidea) · [📖 Docs ↗](https://github.com/mylxsw/aidea-server/blob/main/docs/deploy.md) · [🌐 Site ↗](https://aidea.aicode.cc) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aidea/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
