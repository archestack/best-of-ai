# 🧰 Agent frameworks and SDKs reviews · Best of Open-Source AI

Libraries for building agents and LLM apps in code: tool calling, planning, multi-agent setups and browser control. Back to the [leaderboard](../README.md#-agent-frameworks-and-sdks).

<sub>🌐 Also on the web: [Agent frameworks and SDKs on archestack.com](https://archestack.com/best-of-ai/agent-frameworks/), each project on its own page.</sub>

<a name="ppt-master"></a>
### 🥇 [ppt-master](https://github.com/hugohe3/ppt-master) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 65k · MIT · Oct 2026</sub>

**Agent skill that turns documents into natively editable PowerPoint decks.**

PPT Master is a workflow ("skill") that runs inside an agent-capable AI tool such as Claude Code, Cursor or Codex CLI. It reads source material like PDFs, DOCX and web pages, plans the argument, and exports a .pptx with native shapes, data-backed charts and tables, and slide masters via the template route. It can also fill existing decks, extract templates, and add transitions, animations and narration.

- **+** Exports native PowerPoint objects (shapes, charts, tables), not flattened images
- **+** Runs on your machine; only model API calls leave it
- **+** Works with any agent-capable tool and model: Claude, GPT, Gemini, Kimi
- **+** Also fills existing .pptx files and distills reusable templates
- **−** Output quality depends on the driving model; README recommends Kimi K3 or Claude with ~1M context
- **−** Image-heavy decks need a separate AI image generation API such as gpt-image-2
- **−** Needs an agent tool installed plus Python 3.10+; no standalone UI
- **−** SmartArt is deliberately unsupported; one-shot decks still need manual polish

<sub>no GPU · Needs Python 3.10+, An agent-capable AI tool (Claude Code, Cursor, Codex CLI, etc.), pandoc (only for legacy formats like .doc, .odt, .rtf) · Models: Kimi K3, Claude, GPT, Gemini, gpt-image-2 · [Repo](https://github.com/hugohe3/ppt-master) · [▶️ Demo ↗](https://hugohe3.github.io/ppt-master-examples/) · [📖 Docs ↗](https://github.com/hugohe3/ppt-master/blob/main/docs/getting-started.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ppt-master/)</sub>

<a name="langchain"></a>
### 🥈 [langchain](https://github.com/langchain-ai/langchain) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 148k · MIT · Oct 2026</sub>

**Python framework for building LLM agents and apps from interoperable components.**

LangChain is a Python library that gives a standard interface to chat models, embeddings, vector stores and tools, so providers can be swapped with little code change. Models load through init_chat_model with a provider:model string. For lower-level agent orchestration it points to LangGraph, and for tracing and evals to LangSmith.

- **+** Common interface across model providers, embeddings and vector stores
- **+** Large integrations library covering tools, retrievers and vector stores
- **+** Companions: LangGraph for orchestration, Deep Agents for planning and subagents
- **+** MIT license; JS/TS counterpart available as LangChain.js
- **−** Observability, evals and managed deployment sit in LangSmith, a separate product
- **−** Controllable stateful agent workflows need LangGraph, not core LangChain
- **−** README gives no hardware requirements or list of supported providers
- **−** Abstraction layer is another API to learn on top of provider SDKs

<sub>Needs Model provider API or other model backend · Models: OpenAI (README example), Other providers via integrations · [Repo](https://github.com/langchain-ai/langchain) · [📖 Docs ↗](https://docs.langchain.com/oss/python/langchain/overview) · [🌐 Site ↗](https://www.langchain.com/langsmith) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langchain/)</sub>

<a name="browser-use"></a>
### 🥉 [browser-use](https://github.com/browser-use/browser-use) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 119k · MIT · Oct 2026</sub>

**Python library that lets an LLM agent control a web browser.**

Browser Use runs an LLM-driven agent that opens a browser, reads pages and completes tasks such as searching, filling forms and booking slots. It is used as a Python library (3.11+), as a CLI skill for agents like Claude Code, or through a hosted cloud API. It works with OpenAI, Anthropic, Google, Ollama and its own BU2 model, on local or cloud browsers.

- **+** Works with a local Chrome profile, a cloud browser, or a remote browser over CDP
- **+** Custom tools register with a decorator; system prompt can be extended or overridden
- **+** Supports OpenAI, Anthropic and Google wrappers, plus local models via Ollama
- **+** Ships a CLI skill so existing coding agents can drive a browser
- **−** README recommends BU2, which needs a paid Browser Use API key
- **−** CAPTCHA and stealth handling rely on the paid cloud browser, with no guarantee
- **−** Profile sync copies cookies only, not local storage, IndexedDB or extensions
- **−** Hardware needs for local models are not stated in the README

<sub>GPU optional · Docker · Needs Python >= 3.11, Chromium-based browser, LLM provider API key or Ollama, Browser Use API key (optional) · Models: OpenAI, Anthropic, Google, Ollama, BU2 (ChatBrowserUse) · [Repo](https://github.com/browser-use/browser-use) · [▶️ Demo ↗](https://browser-use.com/showcase) · [📖 Docs ↗](https://docs.browser-use.com) · [🌐 Site ↗](https://browser-use.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/browser-use/)</sub>

<a name="tradingagents"></a>
### #&#8288;4 [tradingagents](https://github.com/tauricresearch/tradingagents) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 112k · Apache-2.0 · Oct 2026</sub>

**LangGraph multi-agent framework simulating a trading firm to analyze tickers.**

TradingAgents runs a team of LLM agents (fundamentals, sentiment, news and technical analysts, bull and bear researchers, trader, risk team, portfolio manager) that debate and produce a trading decision for a ticker and date. It is built on LangGraph, with a CLI and a Python API, and works with many hosted providers plus Ollama and OpenAI-compatible servers. The README states it is for research, not financial advice.

- **+** Many LLM providers, plus Ollama and any OpenAI-compatible endpoint such as vLLM or llama.cpp
- **+** Quick and deep model tiers, each configurable with its own provider
- **+** Point-in-time data for backtests, with SEC EDGAR statements as originally filed
- **+** Interactive CLI, flag-driven non-interactive runs, and a Python API
- **−** Approved orders go only to a simulated exchange; no live broker execution described
- **−** Results vary with model, temperature and data quality; README says research use only
- **−** Past-dated runs withhold Yahoo fundamentals and insider trades for non-SEC companies
- **−** Needs a provider API key; import paths changed in v0.5.1

<sub>GPU optional · Docker + Compose · Needs Python 3.11+, LangGraph, LLM provider API key or Ollama, Yahoo Finance, SEC EDGAR, Alpha Vantage (optional), FRED (optional) · Models: OpenAI, Anthropic, Google Gemini, xAI, DeepSeek · [Repo](https://github.com/tauricresearch/tradingagents) · [▶️ Demo ↗](https://www.youtube.com/watch?v=90gr5lwjIho) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tradingagents/)</sub>

<a name="copilotkit"></a>
### #&#8288;5 [copilotkit](https://github.com/copilotkit/copilotkit) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Oct 2026</sub>

**SDK for adding agent chat, generative UI and shared state to apps.**

CopilotKit is a TypeScript SDK that connects agents to user-facing front ends over the AG-UI protocol. It provides a chat UI, generative UI, shared agent state, human-in-the-loop approvals and a useAgent hook for React, Angular, Vue and React Native, plus a Channels SDK for Slack and Microsoft Teams. Persistent threads, memories and automatic learning are in a separate product, CopilotKit Intelligence.

- **+** Covers React, Angular, Vue and React Native, with Slack and Teams via Channels SDK
- **+** Agents can pause for user confirmation or edits (human-in-the-loop)
- **+** Shared state is readable and writable by both agent and UI through useAgent
- **+** MIT-licensed source; AG-UI protocol is adopted by several agent frameworks
- **−** Rich threads, user memories and automatic learning belong to the Intelligence product, not the MIT repo
- **−** Vue docs say quickstart is coming soon; Angular is source-only
- **−** Discord, WhatsApp and Telegram managed connections are not yet available
- **−** Does not run models; needs your own agent backend and LLM provider

<sub>no GPU · Needs Agent backend (AG-UI compatible), LLM provider · [Repo](https://github.com/copilotkit/copilotkit) · [📖 Docs ↗](https://docs.copilotkit.ai) · [🌐 Site ↗](https://www.copilotkit.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/copilotkit/)</sub>

<a name="openai-agents-python"></a>
### #&#8288;6 [openai-agents-python](https://github.com/openai/openai-agents-python) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Oct 2026</sub>

**Python SDK for multi-agent workflows with handoffs, guardrails and tracing.**

Python library from OpenAI for building agents with instructions, tools, guardrails and handoffs between agents. It supports the OpenAI Responses and Chat Completions APIs and, per the README, 100+ other LLMs. It also includes sandbox agents, realtime and voice agents, sessions for conversation history, human-in-the-loop controls and built-in tracing.

- **+** Small API: Agent and Runner cover a text agent in a few lines
- **+** Tools can be Python functions, MCP servers or hosted tools
- **+** Built-in tracing, guardrails, sessions and human-in-the-loop support
- **+** Includes sandbox, realtime and voice agents; MIT license, Python 3.10+
- **−** Examples assume OPENAI_API_KEY; non-OpenAI models go through optional LiteLLM or any-llm
- **−** Pull requests limited to repository collaborators
- **−** Python only; JS/TS version is a separate repository
- **−** Realtime agents use gpt-realtime-2.1, an OpenAI-hosted model

<sub>no GPU · Needs OpenAI API key, Python 3.10+, optional: Redis, optional: SQLAlchemy, optional: websockets, optional: LiteLLM or any-llm, optional: Docker · Models: OpenAI Responses API, OpenAI Chat Completions API, 100+ other LLMs via LiteLLM or any-llm · [Repo](https://github.com/openai/openai-agents-python) · [📖 Docs ↗](https://openai.github.io/openai-agents-python/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openai-agents-python/)</sub>

<a name="mastra"></a>
### #&#8288;7 [mastra](https://github.com/mastra-ai/mastra) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · custom license · Oct 2026</sub>

**TypeScript framework for building AI agents and workflows.**

Mastra is a TypeScript framework for building agents and graph-based workflows, with model routing across 40+ providers. It adds suspend/resume human-in-the-loop, memory, RAG, MCP server authoring, evals and observability. It embeds in React, Next.js or Node apps, or runs as a standalone server, with a local Studio UI at port 4111.

- **+** Workflow engine with .then(), .branch() and .parallel() control flow
- **+** Suspend and resume runs via storage, so approvals can wait indefinitely
- **+** Built-in evals, observability, memory and RAG in one package set
- **+** Authors MCP servers exposing agents and tools; scaffold with npm create mastra@latest
- **−** TypeScript only; no Python SDK mentioned
- **−** Dual license: code in ee/ directories needs an enterprise license for production
- **−** Storage backends and hardware requirements not listed in the README
- **−** No Docker or compose files detected in the repo

<sub>no GPU · Needs Node.js, LLM provider API key · Models: OpenAI, Anthropic, Google Gemini, xAI, 40+ providers via model router · port 4111 · [Repo](https://github.com/mastra-ai/mastra) · [📖 Docs ↗](https://mastra.ai/docs) · [🌐 Site ↗](https://mastra.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mastra/)</sub>

<a name="crewai"></a>
### #&#8288;8 [crewai](https://github.com/crewaiinc/crewai) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · MIT · Oct 2026</sub>

**Python framework for multi-agent workflows with role-based Crews and event-driven Flows.**

CrewAI is a Python framework for building multi-agent workflows. Crews are teams of role-based agents with goals, tools and tasks, run sequentially or under a hierarchical manager. Flows are event-driven workflows with typed state, branching and routing that can embed Crews. A CLI scaffolds JSON-defined crew projects, with a classic YAML scaffold still available.

- **+** Two models: autonomous Crews and explicit Flows with state, branching and or_/and_ triggers
- **+** CLI scaffolds projects; agents and tasks declared in JSONC or classic YAML
- **+** Covers tools, memory, knowledge, checkpointing, async execution and MCP/A2A support
- **+** MIT license; recent commit and release within days of listing
- **−** Managed deployment, governance and enterprise support are in the commercial AMP Suite
- **−** README has a telemetry section; opt-out details are not in the excerpt
- **−** Requires Python >=3.10 and <3.14 and uv; Windows may need C++ build tools
- **−** Web search example needs a separate Serper.dev API key

<sub>no GPU · Needs Python >=3.10,<3.14, uv, LLM provider API key, Serper.dev API key (optional, web search) · Models: OpenAI (e.g. openai/gpt-4o), other providers via LLM setup · [Repo](https://github.com/crewaiinc/crewai) · [📖 Docs ↗](https://docs.crewai.com) · [🌐 Site ↗](https://crewai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/crewai/)</sub>

<a name="agno"></a>
### #&#8288;9 [agno](https://github.com/agno-agi/agno) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Oct 2026</sub>

**Python SDK and runtime for building and serving agents behind a REST API.**

Agno is a Python framework for defining agents, plus the AgentOS runtime that serves them through a REST API with 50+ endpoints, SSE and websockets. Sessions, memory, knowledge and traces are stored in your own database, and a web UI manages the running platform. It includes JWT-based RBAC, human approval steps, cron scheduling, and interfaces for Slack, Telegram, WhatsApp, Discord, AG-UI and A2A.

- **+** Runtime ships a REST API with 50+ endpoints, SSE and websockets
- **+** JWT-based RBAC and multi-tenant isolation included
- **+** 100+ prebuilt toolkits plus OpenTelemetry tracing and audit logs
- **+** Starter templates for Docker, AWS, GCP, Azure, Fly, Render, Modal and Helm
- **−** Sends a telemetry event per agent run unless AGNO_TELEMETRY=false is set
- **−** README gives no RAM, GPU or port requirements
- **−** Starter templates live in separate repos, not in this one
- **−** Management UI hosting and licensing terms are not described in the README

<sub>Needs Postgres, Docker · Models: unknown · [Repo](https://github.com/agno-agi/agno) · [📖 Docs ↗](https://docs.agno.com) · [🌐 Site ↗](https://agno.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agno/)</sub>

<a name="agent-browser"></a>
### #&#8288;10 [agent-browser](https://github.com/vercel-labs/agent-browser) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · Apache-2.0 · Oct 2026</sub>

**Native Rust CLI that lets AI agents drive Chrome via accessibility snapshots.**

agent-browser is a Rust command-line tool that controls Chrome for AI agents. It exposes an accessibility-tree snapshot with element refs (@e1, @e2) that commands like click, fill and get text can target, alongside CSS and semantic locators. It also covers screenshots, network interception, HAR recording, cookies, batch execution, an optional MCP profile and experimental WebMCP support.

- **+** Snapshot refs let agents target elements without writing selectors
- **+** Native Rust binary; daemon needs no Playwright or Node.js
- **+** Batch mode runs multiple commands in one process invocation
- **+** Detects existing Chrome, Brave, Playwright and Puppeteer installs
- **−** Requires downloading Chrome via a separate install step
- **−** WebMCP support is marked experimental
- **−** Linux needs extra system libraries via install --with-deps
- **−** Refs go stale after page changes and need a fresh snapshot

<sub>no GPU · Docker + Compose · Needs Chrome (Chrome for Testing), Node.js 24+ and pnpm 11+ (source build only), Rust (source build only) · [Repo](https://github.com/vercel-labs/agent-browser) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-browser/)</sub>

<a name="langgraph"></a>
### #&#8288;11 [langgraph](https://github.com/langchain-ai/langgraph) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · MIT · Oct 2026</sub>

**Python framework for building long-running, stateful agents as graphs.**

LangGraph is a low-level Python library for orchestrating stateful agents and workflows as graphs, inspired by Pregel and Apache Beam. It provides durable execution that resumes after failures, human-in-the-loop interrupts to inspect and edit state, and short-term and long-term memory. It can be used without LangChain; tracing and managed deployment go through the separate LangSmith products.

- **+** Durable execution resumes agents from where they stopped after a failure
- **+** Interrupts allow inspecting and modifying agent state mid-run
- **+** Built-in short-term and long-term memory across sessions
- **+** Usable without LangChain; a JS/TS port (LangGraph.js) also exists
- **−** Low-level API; higher-level agent building is pushed to the separate Deep Agents package
- **−** Tracing UI and managed deployment rely on LangSmith, a commercial LangChain product
- **−** No visual builder in this repo; agents are defined in code only
- **−** README gives no RAM, storage or persistence backend requirements

<sub>no GPU · Models: model-agnostic; LangChain integrations optional · [Repo](https://github.com/langchain-ai/langgraph) · [📖 Docs ↗](https://docs.langchain.com/oss/python/langgraph/overview) · [🌐 Site ↗](https://www.langchain.com/langgraph) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langgraph/)</sub>

<a name="deepagents"></a>
### #&#8288;12 [deepagents](https://github.com/langchain-ai/deepagents) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Oct 2026</sub>

**Python agent harness with sub-agents, filesystem tools and context management.**

Deep Agents is a Python library whose create_deep_agent() returns a ready-to-run agent built on LangChain's create_agent and LangGraph. It bundles planning, sub-agents with isolated context, a pluggable filesystem and shell backend, context summarization, skills, human-in-the-loop approval and persistent memory. It works with any tool-calling LangChain chat model, including Ollama, vLLM and llama.cpp.

- **+** Sub-agents, filesystem, context summarization and skills are bundled and work out of the box
- **+** Any LangChain chat model with tool calling works, including Ollama, vLLM and llama.cpp
- **+** Any LangGraph CompiledStateGraph can be passed in as a sub-agent
- **+** Human-in-the-loop approval of tool calls; tools can be custom functions or MCP servers
- **−** Opinionated defaults sit on top of LangChain and LangGraph, adding layers to learn
- **−** Trust-the-LLM security model: boundaries must be enforced via tools or sandbox
- **−** Tracing and evaluation are documented around LangSmith, a separate hosted product
- **−** Python only here; the JavaScript version is a separate repository

<sub>no GPU · Needs LangChain, LangGraph, LLM provider or local model server · Models: OpenAI, Anthropic, Google, Baseten, Fireworks · [Repo](https://github.com/langchain-ai/deepagents) · [📖 Docs ↗](https://docs.langchain.com/oss/python/deepagents/overview) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepagents/)</sub>

<a name="ai"></a>
### #&#8288;13 [ai](https://github.com/vercel/ai) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · custom license · Oct 2026</sub>

**Provider-agnostic TypeScript toolkit for text, structured output, agents and chat UIs.**

The AI SDK is a TypeScript library with one API for generating text and structured data across model providers such as OpenAI, Anthropic and Google. It includes a ToolLoopAgent for tool-calling agents and UI hooks (useChat) for React, Svelte, Vue and Angular. Model strings route through the Vercel AI Gateway by default, or you can install per-provider @ai-sdk packages.

- **+** Single generateText API across OpenAI, Anthropic, Google and other providers
- **+** Typed structured output via Output.object with Zod schemas
- **+** UI hooks for React, Svelte, Vue and Angular, with Next.js route helpers
- **+** Direct provider packages available, so the Vercel gateway is optional
- **−** TypeScript and JavaScript only; requires Node.js 22+
- **−** Default model-string path goes through the Vercel AI Gateway, a hosted service
- **−** Library only: no hosted UI, no model serving, no local inference of its own
- **−** License is not stated in the README; detection reports NOASSERTION

<sub>no GPU · Needs Node.js 22+, Vercel AI Gateway or provider API keys · Models: OpenAI, Anthropic, Google · [Repo](https://github.com/vercel/ai) · [📖 Docs ↗](https://ai-sdk.dev/docs) · [🌐 Site ↗](https://ai-sdk.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai/)</sub>

<a name="haystack"></a>
### #&#8288;14 [haystack](https://github.com/deepset-ai/haystack) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · Apache-2.0 · Oct 2026</sub>

**Python framework for building RAG pipelines and agents from modular components.**

Haystack is a Python framework for composing LLM applications as pipelines of components covering retrieval, routing, memory, tool calling and generation. One Pipeline runs sync or async and streams tokens, and the Agent class supports lifecycle hooks and concurrent tool calls. It integrates with OpenAI, Anthropic, Mistral, Cohere, Hugging Face, Google, Azure OpenAI, AWS Bedrock and local models.

- **+** Pipelines support loops, branches and conditional routing, so context flow is explicit and traceable
- **+** Agent hooks (before_llm, before_tool, on_exit) plus step_count and token_usage tracking
- **+** Model-agnostic: many hosted providers and local models, swappable without rewriting pipelines
- **+** Installs with pip install haystack-ai; Apache-2.0 licensed
- **−** Collects anonymous component-usage telemetry by default; opt-out is documented separately
- **−** Serving as REST or MCP needs the separate Hayhooks project
- **−** Governance, access controls and managed observability are in the paid Enterprise Platform
- **−** Many integrations live in a separate haystack-core-integrations repo

<sub>GPU optional · Docker · Needs Python, LLM provider or local model · Models: OpenAI, Anthropic, Mistral, Cohere, Hugging Face · [Repo](https://github.com/deepset-ai/haystack) · [📖 Docs ↗](https://docs.haystack.deepset.ai) · [🌐 Site ↗](https://haystack.deepset.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/haystack/)</sub>

<a name="llama-index"></a>
### #&#8288;15 [llama_index](https://github.com/run-llama/llama_index) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · MIT · Oct 2026</sub>

**Python framework for RAG and agent apps over your own data.**

LlamaIndex is a Python toolkit that loads data from files, APIs and SQL, builds indices such as a vector store index, and exposes query engines and retrievers for LLM apps. The llama-index-core package is extended by over 300 integration packages for LLMs, embeddings and vector stores. The maintainers say their main focus has moved to the commercial LlamaParse platform, while the framework stays available as open source.

- **+** Over 300 integration packages for LLM, embedding and vector store providers
- **+** Small core package plus a starter bundle; install only the integrations needed
- **+** High-level API indexes and queries a directory in a few lines
- **+** Works with local models, e.g. Ollama LLMs and Hugging Face embeddings
- **−** README says company focus has shifted to the paid LlamaParse platform
- **−** README is noted as less up to date than the documentation
- **−** Index storage is in-memory by default; persistence to ./storage is manual
- **−** Library only: no UI, server or Docker setup included

<sub>GPU optional · Needs Python, LLM provider API key or local Ollama, LlamaParse account (optional) · Models: OpenAI, Ollama, Hugging Face embeddings · [Repo](https://github.com/run-llama/llama_index) · [📖 Docs ↗](https://developers.llamaindex.ai/python/framework/) · [🌐 Site ↗](https://llamaindex.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llama-index/)</sub>

<a name="agentscope"></a>
### #&#8288;16 [agentscope](https://github.com/agentscope-ai/agentscope) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Oct 2026</sub>

**Python agent framework with a multi-tenant FastAPI agent service.**

AgentScope 2.0 is a Python 3.11+ SDK for composing ReAct agents from a toolkit (Python tools, MCP servers, skills, shell and file tools), model adapters, context compaction, middleware and permission checks. It also ships an agent service: a FastAPI backend with a sample web UI, multi-tenant sessions, agent teams, Feishu and Discord channels, RAG, scheduling and SQL/NoSQL persistence.

- **+** Wide model support: OpenAI, Anthropic, Gemini, DashScope, DeepSeek, Moonshot, Volcengine, xAI, Ollama, MiniMax
- **+** Sandbox backends include Docker, Bubblewrap, E2B, Daytona, K8s and Apple Container
- **+** Built-in permission system with human confirmation and composable middleware
- **+** Agent service adds multi-tenancy, scheduling, agent teams and A2A support beyond the SDK
- **−** Realtime voice and SOP features are marked Experimental
- **−** Web UI needs a separate pnpm/Node setup from the Python backend
- **−** README gives no hardware requirements and no Docker or compose files
- **−** 2.0 is a new major version; README does not cover migration from 1.x

<sub>no GPU · Needs Python 3.11+, pnpm (web UI), LLM provider API key · Models: OpenAI, Anthropic, Gemini, DashScope, DeepSeek · [Repo](https://github.com/agentscope-ai/agentscope) · [📖 Docs ↗](https://docs.agentscope.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentscope/)</sub>

<a name="adk-python"></a>
### #&#8288;17 [adk-python](https://github.com/google/adk-python) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Oct 2026</sub>

**Code-first Python framework for building, evaluating and deploying multi-agent apps.**

ADK is Google's Python framework for defining agents and graph-based workflows in code, with tool calling (custom functions, OpenAPI specs, MCP), multi-agent hierarchies and a Task API for agent-to-agent delegation. It ships a CLI (`adk run`, `adk web`, `adk eval`, `adk deploy`) and a built-in dev UI. Optimized for Gemini but described as model-agnostic; deploy targets include Docker, Cloud Run and Vertex AI Agent Engine.

- **+** Graph-based Workflow runtime with routing, fan-out/fan-in, loops, retry and human-in-the-loop
- **+** Built-in CLI for running, evaluating (`adk eval`) and deploying agents
- **+** Dev web UI included for testing and debugging agents
- **+** Tool confirmation flow guards tool execution; MCP and OpenAPI tools supported
- **−** Optimized for Gemini and Google Cloud; other model providers are not enumerated in the README
- **−** Requires Python 3.11 or newer
- **−** Roughly bi-weekly releases; main branch may contain experimental changes
- **−** Managed scaling path points to Vertex AI Agent Engine, a Google Cloud service

<sub>no GPU · Needs Python 3.11+, Gemini API or Vertex AI (default models), Docker (optional, for deploy), Google Cloud Run (optional) · Models: Gemini, model-agnostic (providers unknown) · [Repo](https://github.com/google/adk-python) · [📖 Docs ↗](https://adk.dev/) · [🌐 Site ↗](https://adk.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/adk-python/)</sub>

<a name="dspy"></a>
### #&#8288;18 [dspy](https://github.com/stanfordnlp/dspy) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · MIT · Oct 2026</sub>

**Python framework for programming LMs and optimizing their prompts and weights.**

DSPy lets you describe LM-based systems as modular Python code instead of hand-written prompts. It includes optimizers that tune prompts and model weights against a metric, and targets classifiers, RAG pipelines and agent loops. It installs with pip; the README defers all usage details to dspy.ai.

- **+** Optimizers tune prompts and weights against a metric, including GEPA
- **+** Programs are composed as Python modules rather than prompt strings
- **+** Backed by published Stanford NLP research papers
- **+** Single pip install; MIT license
- **−** README has no quickstart or code example; usage lives on the external docs site
- **−** Optimization needs a metric and example data, adding setup versus plain prompting
- **−** Supported model providers are not listed in the README
- **−** Library only: no UI, server or deployment tooling

<sub>[Repo](https://github.com/stanfordnlp/dspy) · [📖 Docs ↗](https://dspy.ai) · [🌐 Site ↗](https://dspy.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dspy/)</sub>

<a name="page-agent"></a>
### #&#8288;19 [page-agent](https://github.com/alibaba/page-agent) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Sep 2026</sub>

**In-page JavaScript agent that controls a web page's DOM from natural language.**

Page Agent is a TypeScript library that embeds an LLM-driven agent in a web page via a script tag or the npm package. It reads the DOM as text, with no screenshots or multimodal models, and executes instructions such as clicking or filling forms. An optional Chrome extension handles multi-page tasks, and a beta MCP server allows external control.

- **+** Runs entirely in-page; no Python, headless browser or extension needed for single-page use
- **+** Text-based DOM control, so no vision model or screenshot permissions needed
- **+** Bring your own LLM via baseURL and apiKey config, including locally deployed models
- **+** Installs from npm or a single CDN script
- **−** Multi-page tasks require the optional Chrome extension
- **−** MCP server is marked Beta
- **−** Demo CDN script uses a free testing LLM API, for technical evaluation only
- **−** API key is passed in client-side config; README gives no guidance on securing it

<sub>no GPU · Needs LLM API endpoint (OpenAI-compatible), zod (peer dependency) · Models: qwen3.5-plus, OpenAI-compatible APIs, locally deployed models · [Repo](https://github.com/alibaba/page-agent) · [▶️ Demo ↗](https://alibaba.github.io/page-agent/) · [📖 Docs ↗](https://alibaba.github.io/page-agent/docs/introduction/overview) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/page-agent/)</sub>

<a name="pydantic-ai"></a>
### #&#8288;20 [pydantic-ai](https://github.com/pydantic/pydantic-ai) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Oct 2026</sub>

**Typed Python SDK for building agents with swappable model providers.**

Pydantic AI is a Python agent framework where tools, dependencies and outputs are typed with Pydantic models, and the model is chosen by a provider string (OpenAI, Anthropic, Google, Bedrock, Ollama and others). The same agent can run as a CLI, web chat, realtime voice session, or on durable execution engines such as Temporal, DBOS and Prefect. A separate Harness package adds memory, guardrails, sub-agents and a coding agent as composable capabilities.

- **+** Validated structured output and typed dependency injection checked by IDE and type checker
- **+** Model swap by string across OpenAI, Anthropic, Google, Bedrock, Ollama and many more
- **+** Durable execution integrations for Temporal, DBOS, Prefect, Restate and others
- **+** OpenTelemetry instrumentation works with any OTel backend, not only Logfire
- **−** Python only
- **−** Memory, guardrails, sub-agents and coding agent live in a separate pydantic-ai-harness package
- **−** Pydantic Graph and Pydantic Evals are separate packages to install
- **−** README promotes Logfire and the Gateway, which are commercial Pydantic products

<sub>no GPU · Needs Model provider API key or local model server such as Ollama, Temporal, DBOS or Prefect (optional, for durable execution) · Models: OpenAI, Anthropic, Google, Bedrock, Azure AI Foundry · [Repo](https://github.com/pydantic/pydantic-ai) · [📖 Docs ↗](https://pydantic.dev/docs/ai/) · [🌐 Site ↗](https://pydantic.dev/docs/ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pydantic-ai/)</sub>

<a name="eliza"></a>
### #&#8288;21 [eliza](https://github.com/elizaos/eliza) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Oct 2026</sub>

**TypeScript agent runtime and personal assistant app with a plugin system.**

elizaOS is a TypeScript monorepo containing an agent runtime (@elizaos/core), a standalone agent HTTP host, the Eliza app for web, desktop and mobile, and first-party plugins for connectors, wallets and device bridges. Models can be routed per capability to on-device Eliza-1 (Gemma 4 based, 2B to 27B), direct providers, or the optional Eliza Cloud. It also includes Linux and Android distribution tooling under packages/os.

- **+** Plugins can register actions, providers, evaluators, services, model handlers, routes and app views
- **+** Per-capability routing across local, direct-provider and Eliza Cloud backends; Cloud is optional
- **+** Ships an app, CLI, standalone agent host and OS distribution tooling in one MIT repo
- **+** On-device Eliza-1 text tiers (2B, 4B, 9B, 27B) plus embeddings, speech, vision and image generation
- **−** Large monorepo; setup needs pinned Bun and Node versions and runs submodule and native build steps
- **−** Third-party plugins and registry submissions are no longer accepted
- **−** Strict contribution rules: human-written issues only, UI PRs require video and screenshots
- **−** Capability availability varies by OS, plugins and permissions; hardware requirements not stated

<sub>GPU optional · Needs Bun, Node.js, Python 3.11+ (benchmarks only) · Models: Eliza-1 (Gemma 4 based, 2B/4B/9B/27B), GGUF embeddings, Direct model providers, Eliza Cloud · [Repo](https://github.com/elizaos/eliza) · [▶️ Demo ↗](https://cloud.eliza.app) · [📖 Docs ↗](https://docs.elizaos.ai/) · [🌐 Site ↗](https://eliza.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/eliza/)</sub>

<a name="stagehand"></a>
### #&#8288;22 [stagehand](https://github.com/browserbase/stagehand) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

**SDK for driving browsers with natural-language act, observe and extract calls.**

Stagehand is a browser automation SDK for TypeScript, Python and Go with Playwright-style page and locator methods. It adds LLM-driven act(), observe() and extract() calls, with schema-validated extraction and selectors returned so credentials stay out of the model. It runs against local Chrome or Browserbase's hosted browsers, where a model gateway and server-side caching are also available.

- **+** Same browser driver API across TypeScript, Python and Go SDKs
- **+** observe() returns real selectors, so credentials can be filled without the model seeing them
- **+** extract() validates output against Zod or Pydantic schemas, or Go types
- **+** Deep locators for nested iframes and closed Shadow DOM; OTel traces
- **−** Local runs require Chrome installed
- **−** Model gateway, server-side caching, proxies and session replay need a Browserbase account
- **−** Local use needs an LLM provider API key, and each action costs tokens
- **−** Fetch and Search add-ons use the Browserbase API key

<sub>no GPU · Needs Chrome, LLM provider API key (e.g. OpenAI), Browserbase API key (optional, for cloud) · Models: OpenAI (openai/gpt-5.4-mini in examples), Browserbase Model Gateway · [Repo](https://github.com/browserbase/stagehand) · [📖 Docs ↗](https://docs.stagehand.dev) · [🌐 Site ↗](https://stagehand.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/stagehand/)</sub>

<a name="pipecat"></a>
### #&#8288;23 [pipecat](https://github.com/pipecat-ai/pipecat) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · BSD-2-Clause · Oct 2026</sub>

**Python framework for real-time voice and multimodal agent pipelines.**

Pipecat is a Python framework that chains speech-to-text, LLM, text-to-speech and speech-to-speech services into streaming pipelines, with WebSocket and WebRTC transports. It also supports multi-agent setups with handoff, parallel fan-out and a shared bus, locally or distributed. A CLI scaffolds and deploys projects, and client SDKs cover JavaScript, React, Swift, Kotlin, C++ and ESP32.

- **+** Many pluggable services: 23 STT, 25 LLM and 30+ TTS providers listed, including local Whisper and Ollama
- **+** Official client SDKs for JS, React, React Native, Swift, Kotlin, C++ and ESP32
- **+** Structured conversation flows (Pipecat Flows) built in, plus Whisker debugger and Tail dashboard
- **+** Multi-agent support: handoff, parallel fan-out and distributed deployment over a shared bus
- **−** Library, not a ready app: you write Python pipeline code to get a working bot
- **−** Most listed STT, LLM and TTS services are hosted APIs needing separate keys
- **−** No Docker or compose files detected in the repo
- **−** Hardware requirements for local models are not stated in the visible README

<sub>GPU optional · Needs Python, STT/LLM/TTS provider API keys (e.g. Deepgram, OpenAI, Cartesia, ElevenLabs), WebRTC/WebSocket transport · Models: Whisper, Moonshine, Ollama, OpenAI, Anthropic · [Repo](https://github.com/pipecat-ai/pipecat) · [📖 Docs ↗](https://docs.pipecat.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pipecat/)</sub>

<a name="semantic-kernel"></a>
### #&#8288;24 [semantic-kernel](https://github.com/microsoft/semantic-kernel) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Oct 2026</sub>

**Microsoft SDK for building LLM agents and plugins in C#, Python and Java.**

Semantic Kernel is a model-agnostic SDK for building agents and multi-agent systems in .NET, Python and Java. It provides chat completion agents, plugins (native functions, prompt templates, OpenAPI, MCP), vector store connectors and a process framework for structured workflows. The README states it has been succeeded by Microsoft Agent Framework, which reached 1.0, and links a migration guide.

- **+** Same agent and plugin model across Python, .NET and Java
- **+** Connectors for OpenAI, Azure OpenAI, Hugging Face, NVIDIA, Ollama, LMStudio and ONNX
- **+** Plugins can come from native code, prompt templates, OpenAPI specs or MCP
- **+** Vector store integrations include Azure AI Search, Elasticsearch and Chroma
- **−** README says it is superseded by Microsoft Agent Framework 1.0
- **−** Java support lives in a separate repository with its own build steps
- **−** Requires .NET 10.0+ or Python 3.10+, which may exceed existing stacks
- **−** Library only: no UI, server or hosted deployment included

<sub>no GPU · Needs OpenAI or Azure OpenAI API key, or a local model runtime · Models: OpenAI, Azure OpenAI, Hugging Face, NVIDIA NIM, Ollama · [Repo](https://github.com/microsoft/semantic-kernel) · [📖 Docs ↗](https://learn.microsoft.com/en-us/semantic-kernel/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/semantic-kernel/)</sub>

<a name="nanobrowser"></a>
### #&#8288;25 [nanobrowser](https://github.com/nanobrowser/nanobrowser) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

**Browser agent in a Chrome/Edge side panel that clicks and types for you.**

Nanobrowser is a Chrome and Edge extension. You give a task in a side panel, and an LLM agent reads pages, clicks, types and switches tabs. It uses your own API key or a local model (Ollama, LM Studio, OpenAI-compatible servers). In the default Ask mode it asks before submit, send, delete or upload, and per-site Allow, Ask and Block rules are set in Settings.

- **+** Per-site Allow/Ask/Block rules; Ask mode confirms submit, send, delete and upload
- **+** Supports Anthropic, OpenAI, Gemini, OpenRouter, xAI, DeepSeek, Mistral, Ollama and LM Studio
- **+** Several tasks run in parallel, each in its own tab group
- **+** Deterministic control layer on chrome.debugger with element IDs tied to exact elements
- **−** Only Chrome and Edge are supported; other browsers are untested
- **−** Models must support tool calling; local models suit only simple tasks
- **−** Local models need 16k+ context plus Ollama origin or LM Studio CORS setup
- **−** README says prompt-injection protection is imperfect and the agent can miss steps needing approval

<sub>GPU optional · Needs Chrome or Edge, LLM provider API key or local model server, Node.js 24 and pnpm 10 (build from source) · Models: Anthropic, OpenAI, Google Gemini, OpenRouter, xAI Grok · [Repo](https://github.com/nanobrowser/nanobrowser) · [🌐 Site ↗](https://chromewebstore.google.com/detail/nanobrowser/imbddededgmcgfhfpcjmijokokekbkal) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nanobrowser/)</sub>

<a name="langchainjs"></a>
### #&#8288;26 [langchainjs](https://github.com/langchain-ai/langchainjs) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

**TypeScript framework for building LLM apps and agents with swappable model integrations.**

LangChain.js is a TypeScript library that gives agents, chat models, embeddings, vector stores and retrievers a common interface, with integrations for many providers. It runs on Node.js 20, 22 and 24, Cloudflare Workers, Deno, Bun, Vercel/Next.js and in the browser. Deep Agents (higher-level) and LangGraph.js (lower-level orchestration) are separate packages built on or alongside it.

- **+** Runs on Node.js (ESM and CommonJS), Deno, Bun, Cloudflare Workers, Supabase Edge and browsers
- **+** Common interface across models, embeddings, vector stores and retrievers makes providers swappable
- **+** Large integration library covering model providers, tools and vector stores
- **+** Pairs with LangGraph.js for orchestration and Deep Agents for planning and subagents
- **−** Monitoring and evaluation depend on LangSmith, a separate hosted product
- **−** Abstraction layers add indirection over direct provider SDK calls
- **−** Advanced orchestration requires learning a second package, LangGraph.js
- **−** README gives no resource requirements or version-compatibility details for integrations

<sub>no GPU · Needs Node.js 20/22/24 or Deno/Bun, LLM provider API · Models: Multiple providers via integrations · [Repo](https://github.com/langchain-ai/langchainjs) · [📖 Docs ↗](https://docs.langchain.com/oss/javascript/langchain/overview) · [🌐 Site ↗](https://www.langchain.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langchainjs/)</sub>

<a name="instructor"></a>
### #&#8288;27 [instructor](https://github.com/567-labs/instructor) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

**Python library that returns validated Pydantic objects from LLM calls.**

Instructor wraps LLM provider clients so a chat completion call takes a Pydantic model as response_model and returns a validated, typed object. Failed validations are retried with the error message sent back to the model, and partial objects can be streamed. It uses one interface across OpenAI, Anthropic, Google, Groq and Ollama, with ports in TypeScript, Ruby, Go, Elixir and Rust.

- **+** Same from_provider call works across OpenAI, Anthropic, Google, Groq and Ollama
- **+** Automatic retries feed Pydantic validation errors back to the model via max_retries
- **+** Streams partial objects with Partial[Model], including nested models
- **+** Installs with pip, uv or poetry; MIT license
- **−** Scoped to structured extraction; no agent runtime, README points to PydanticAI for that
- **−** Retries add extra LLM calls, so cost and latency rise on failed validations
- **−** Non-Python ports are linked separately; feature parity is not documented in README
- **−** Adoption figures in README (3M+ downloads, named companies) are unsourced

<sub>no GPU · Needs Pydantic, LLM provider API or local Ollama · Models: OpenAI, Anthropic, Google Gemini, Groq, Ollama · [Repo](https://github.com/567-labs/instructor) · [📖 Docs ↗](https://python.useinstructor.com) · [🌐 Site ↗](https://python.useinstructor.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/instructor/)</sub>

<a name="browseros"></a>
### #&#8288;28 [browseros](https://github.com/browseros-ai/browseros) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · AGPL-3.0 · Oct 2026</sub>

**Secondary Chromium browser that AI coding agents drive over MCP with your logins.**

BrowserOS neo is a Chromium-based browser that sits next to Chrome and exposes an MCP endpoint on 127.0.0.1, so agents such as Claude Code, Codex and Cursor can run web tasks in your logged-in sessions. It imports logins, bookmarks and extensions from Chrome, runs agents in parallel tabs, and saves each session as a replayable video with an action timeline. The repo also ships BrowserOS, a separate Chromium fork with a built-in agent.

- **+** Imports Chrome logins, bookmarks and extensions in one click, so agents use real accounts
- **+** Works with any MCP client; one-click connect for Claude Code, Codex, Cursor, VS Code and others
- **+** Sessions saved locally as scrubbable video with step-by-step action timeline
- **+** Runs on 127.0.0.1 with local-only session data under ~/.browserclaw/
- **−** Linux builds are x64 only
- **−** Sends anonymous usage events by default; opt-out via a Settings toggle
- **−** Not a Chrome replacement; needs a separate agent harness to issue tasks
- **−** AGPL-3.0 license may restrict some commercial or embedded use

<sub>no GPU · Needs MCP-compatible agent (Claude Code, Codex, Cursor, etc.) · Models: Any MCP client, Claude Code, Codex, Cursor, Ollama (BrowserOS only) · [Repo](https://github.com/browseros-ai/browseros) · [📖 Docs ↗](https://docs.browseros.com) · [🌐 Site ↗](https://www.browseros.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/browseros/)</sub>

<a name="openmanus"></a>
### #&#8288;29 [openmanus](https://github.com/foundationagents/openmanus) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: widely used (85) · Freshness: recent (70) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Aug 2026</sub>

**Python agent that carries out terminal-entered tasks with LLM tools and a browser.**

OpenManus is a Python agent framework, an open reimplementation of Manus, that takes a task typed in the terminal and carries it out with tools. It drives a browser through the Browser Use CLI MCP server and calls an LLM endpoint configured in config.toml. Extra entry points cover an MCP tool version, an experimental multi-agent flow, and an optional data analysis agent.

- **+** Browser automation via Browser Use MCP server; local Chrome mode needs no API key
- **+** Separate entry points: main.py, run_mcp.py and run_flow.py for multi-agent
- **+** Simple config.toml with separate LLM and vision model settings
- **+** MIT license, active commits, and a Hugging Face demo space
- **−** Multi-agent flow is described by the README as unstable
- **−** Terminal-only interface, no web UI or user accounts
- **−** No tagged release since 2025-04-10
- **−** README shows only OpenAI-style API setup, no local model guidance

<sub>no GPU · Docker · Needs Python 3.12, uv or conda, LLM API key, Browser Use CLI (uvx), Chrome or Chromium, Playwright (BrowserGym) · Models: OpenAI-compatible API (gpt-4o in example config) · [Repo](https://github.com/foundationagents/openmanus) · [▶️ Demo ↗](https://huggingface.co/spaces/lyh-917/OpenManusDemo) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmanus/)</sub>

<a name="camel"></a>
### #&#8288;30 [camel](https://github.com/camel-ai/camel) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (29) · Freshness: active (97) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

**Python framework for multi-agent systems, role-playing and synthetic data generation.**

CAMEL is a Python library, installed with pip install camel-ai, for building LLM agents and multi-agent societies. It provides ChatAgent, role-playing and workforce modules, toolkits, memory, retrievers, interpreters and benchmarks, plus data generation pipelines such as CoT, Self-Instruct and Source2Synth. It is run by a research community studying agent scaling behavior.

- **+** Covers agents, societies, memory, retrievers, interpreters and benchmarks in one package
- **+** Built-in synthetic data generation: CoT, Self-Instruct, Source2Synth, self-improving CoT
- **+** Cookbooks and Hugging Face datasets published (AI Society, Code, Math, Physics)
- **+** Installs from PyPI with optional extras such as web_tools
- **−** Research-oriented; production deployment guidance is not in the README
- **−** Quick start example uses OpenAI and needs an API key
- **−** Claim of simulating up to 1M agents is given without numbers or benchmarks
- **−** No Docker image or compose file

<sub>no GPU · Needs Python, LLM provider API key (e.g. OpenAI) · Models: OpenAI, multiple LLM backends via ModelFactory · [Repo](https://github.com/camel-ai/camel) · [▶️ Demo ↗](https://colab.research.google.com/drive/1AzP33O8rnMW__7ocWJhVBXjKziJXPtim?usp=sharing) · [📖 Docs ↗](https://docs.camel-ai.org) · [🌐 Site ↗](https://www.camel-ai.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/camel/)</sub>

<a name="agent-framework"></a>
### #&#8288;31 [agent-framework](https://github.com/microsoft/agent-framework) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

**Microsoft's Python and .NET framework for agents and multi-agent workflows.**

Microsoft Agent Framework is a code-first library for building agents and graph-based multi-agent workflows in Python and .NET. Workflows support sequential, concurrent, handoff and group patterns, with checkpointing, streaming and human-in-the-loop. It includes middleware, OpenTelemetry tracing, YAML declarative agents, and a DevUI for testing. It is positioned as the successor path for Semantic Kernel and AutoGen users.

- **+** Same agent and workflow APIs in Python and .NET, with a separate Go SDK
- **+** Graph workflows with checkpointing, streaming, human-in-the-loop and time-travel
- **+** Built-in OpenTelemetry tracing and a middleware pipeline
- **+** Migration guides from Semantic Kernel and AutoGen
- **−** Quickstarts target Microsoft Foundry and Azure credentials; other providers need extra setup
- **−** Durable Task and Azure Functions hosting live in a separate extension repo
- **−** Experimental features sit in a separate lab package
- **−** Go SDK is maintained in a different repository

<sub>no GPU · Needs Microsoft Foundry or Azure OpenAI or OpenAI (LLM provider), Azure CLI (for az login in quickstart) · Models: Microsoft Foundry, Azure OpenAI, OpenAI, GitHub Copilot SDK · [Repo](https://github.com/microsoft/agent-framework) · [📖 Docs ↗](https://learn.microsoft.com/en-us/agent-framework/) · [🌐 Site ↗](https://devblogs.microsoft.com/agent-framework/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-framework/)</sub>

<a name="llm"></a>
### #&#8288;32 [llm](https://github.com/simonw/llm) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**CLI and Python library for prompting local and hosted LLMs, logging to SQLite.**

LLM runs prompts and interactive chats against OpenAI, Anthropic, Gemini and other remote APIs, or local models through plugins such as llm-ollama. It logs prompts and responses to SQLite, and supports attachments, schemas for structured output, tool execution, templates, fragments and embeddings. It installs with pip, Homebrew, pipx or uv.

- **+** Plugin system adds remote providers, local models, tools, fragments and embedding models
- **+** Stores prompts and responses in SQLite for later querying
- **+** Works as both a shell command (pipes, stdin, system prompts) and a Python library
- **+** Schemas extract structured JSON from text and images; embeddings commands included
- **−** Command-line only; no built-in web UI or user accounts
- **−** Anthropic, Gemini and Ollama access each need a separate plugin install
- **−** Does not run models itself; local inference depends on plugins or external servers
- **−** Tool support is basic compared with dedicated agent frameworks

<sub>no GPU · Needs SQLite, Provider API keys or a local model server (e.g. Ollama, LM Studio) via plugins · Models: OpenAI, Anthropic Claude (plugin), Google Gemini (plugin), Ollama (plugin), OpenAI-compatible endpoints · [Repo](https://github.com/simonw/llm) · [▶️ Demo ↗](https://www.youtube.com/watch?v=QUXQNi6jQ30) · [📖 Docs ↗](https://llm.datasette.io/en/stable/) · [🌐 Site ↗](https://llm.datasette.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm/)</sub>

<a name="smolagents"></a>
### #&#8288;33 [smolagents](https://github.com/huggingface/smolagents) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

**Python agent library where the model writes its actions as code.**

smolagents is a Python library from Hugging Face for building agents. Its main class, CodeAgent, has the LLM write each action as a Python snippet, so tool calls become function calls. The core logic in agents.py is under 1,000 lines. It also ships ToolCallingAgent (JSON tool calls), multi-agent hierarchies, and the smolagent and webagent CLIs.

- **+** Core agent logic fits in under 1,000 lines, easy to read and modify
- **+** Works with local transformers, Ollama, HF providers, OpenAI, Anthropic, Azure, Bedrock, LiteLLM
- **+** Tools can come from MCP servers, LangChain or Hub Spaces
- **+** Sandboxed execution via E2B, Blaxel, Modal or Docker
- **−** Built-in LocalPythonExecutor is not a security boundary and can be bypassed
- **−** Safe code execution needs an external sandbox or Docker setup
- **−** Library only: no web UI, server or deployment layer included
- **−** Efficiency claims (30% fewer steps) come from linked papers, not reproduced in the README

<sub>GPU optional · Needs E2B, Blaxel, Modal or Docker (for sandboxing), LLM provider or local model · Models: transformers, Ollama, HF Inference Providers, OpenAI-compatible APIs, Azure OpenAI · [Repo](https://github.com/huggingface/smolagents) · [📖 Docs ↗](https://huggingface.co/docs/smolagents/index) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/smolagents/)</sub>

<a name="langchain4j"></a>
### #&#8288;34 [langchain4j](https://github.com/langchain4j/langchain4j) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**Java library for building LLM apps with unified provider and vector store APIs.**

LangChain4j is a Java library that puts 20+ LLM providers and 30+ embedding stores behind one API, so providers can be swapped without rewriting code. It covers prompt templating, chat memory, function calling, RAG pipelines and agents, with integrations for Quarkus, Spring Boot, Helidon and Micronaut. It is independent of the Python LangChain project.

- **+** Unified API across 20+ LLM providers and 30+ embedding stores
- **+** Integrates with Quarkus, Spring Boot, Helidon and Micronaut
- **+** Covers prompt templates, chat memory, tool calling, RAG and agents
- **+** Separate examples repo with plain Java and framework samples
- **−** JVM only; no Python or JavaScript support
- **−** README says some features are still being worked on
- **−** Quarkus, Helidon and Micronaut support is in separate dependencies
- **−** Documentation chatbot is marked experimental

<sub>no GPU · Needs JVM, LLM provider API · Models: OpenAI, Google Vertex AI, Pinecone, Milvus · [Repo](https://github.com/langchain4j/langchain4j) · [📖 Docs ↗](https://docs.langchain4j.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langchain4j/)</sub>

<a name="chatterbot"></a>
### #&#8288;35 [chatterbot](https://github.com/gunthercox/chatterbot) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · BSD-3-Clause · Aug 2026</sub>

**Python library for retrieval-based chatbots trained on example conversations.**

ChatterBot is a Python library that builds a conversational engine from collections of known conversations. It stores each input and the statement it responded to, then replies by finding the closest known statement and returning the most frequent response to it. It ships training corpora for over a dozen languages and installs with pip.

- **+** Installs with pip; a basic bot takes a few lines of Python
- **+** Bundled corpus training data for over a dozen languages
- **+** Language-independent design, trainable on custom conversation data
- **+** BSD-3-Clause license; last release 2026-08-25
- **−** Replies come from matching past statements, not an LLM; no generative output
- **−** Untrained bot has no knowledge; quality depends on training data volume
- **−** README mentions no tool calling or LLM provider integration
- **−** No web UI or server included; README shows library usage only

<sub>no GPU · Models: ChatterBot corpus training data · [Repo](https://github.com/gunthercox/chatterbot) · [📖 Docs ↗](https://docs.chatterbot.us) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chatterbot/)</sub>

<a name="eino"></a>
### #&#8288;36 [eino](https://github.com/cloudwego/eino) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**Go framework for building LLM agents and graph-based workflows.**

Eino is a Go framework for LLM applications, modeled on LangChain and Google ADK but following Go conventions. It provides component interfaces (ChatModel, Tool, Retriever, Embedding), an Agent Development Kit with ReAct agents, a multi-agent DeepAgent and interrupt/resume, and a compose package for typed graphs and workflows. Component implementations live in the separate eino-ext repo.

- **+** Typed graph and workflow composition, with graphs exposable as agent tools
- **+** Handles stream concatenation, merging and copying between nodes automatically
- **+** Interrupt/resume with checkpoints for human-in-the-loop agents
- **+** Official integrations for OpenAI, Claude, Gemini, Ark, Ollama and Elasticsearch
- **−** Go only; no Python or TypeScript bindings
- **−** Component implementations are in a separate eino-ext repository
- **−** README documentation links point to the Chinese-language manual path
- **−** No built-in UI; visual debugging is a separate devops module

<sub>no GPU · Needs Go 1.18+ · Models: OpenAI, Claude, Gemini, Ark, Ollama · [Repo](https://github.com/cloudwego/eino) · [📖 Docs ↗](https://www.cloudwego.io/zh/docs/eino/) · [🌐 Site ↗](https://www.cloudwego.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/eino/)</sub>

<a name="parlant"></a>
### #&#8288;37 [parlant](https://github.com/emcie-co/parlant) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: known (32) · Freshness: active (97) · Maintenance: weak (29) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Jul 2026</sub>

**Python framework for controlling behavior of customer-facing conversational agents.**

Parlant is a Python SDK where agent behavior is defined as guidelines, observations, journeys, glossary terms and tools instead of one large system prompt. On each turn its engine matches only the relevant rules and tools and builds a narrowed context before generating a reply. It also supports canned-response templates for strict output and OpenTelemetry tracing of every match.

- **+** Per-turn matching keeps only relevant guidelines and tools in the LLM context
- **+** Strict mode with canned responses gives exact, pre-approved wording at critical moments
- **+** OpenTelemetry tracing logs guideline matches and decisions for auditing
- **+** External workflows (LangGraph, LlamaIndex, Agno) can be wrapped as tools
- **−** README says small off-the-shelf models tend to give inconsistent results
- **−** Extra matching step per turn; latency and token cost are not documented
- **−** Not a workflow builder; README points to LangGraph for workflow automation
- **−** Recommended Emcie models are a vendor-specific service; pricing is unknown

<sub>no GPU · Needs LLM provider (Emcie, OpenAI, Anthropic or LiteLLM) · Models: Emcie, OpenAI, Anthropic, LiteLLM · [Repo](https://github.com/emcie-co/parlant) · [📖 Docs ↗](https://www.parlant.io/docs/quickstart/installation) · [🌐 Site ↗](https://www.parlant.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/parlant/)</sub>

<a name="jev-ultrafast"></a>
### #&#8288;38 [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: known (47) · Freshness: active (100) · Maintenance: weak (14) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · MIT · Sep 2026</sub>

**Browser agent that picks an operation and element per step from an indexed element table.**

Python browser agent that reads a numbered table of visible page controls and asks TypeSafe's Jev for an operation (CLICK, TYPE_TEXT, SELECT, SCROLL, WAIT, DONE, BLOCKED) and a target in one request. A small LLM generates text only for TYPE_TEXT. The README reports a Google Flights search in 7.1 s and a 25% median speedup over its earlier version on one task.

- **+** One network request per decision; operation and target heads share the same observed state
- **+** Default loop uses structured DOM state, not screenshots; browser protocol calls dropped 1,092 to 101
- **+** Model output never becomes selectors, coordinates or JavaScript; executor rechecks freshness and occlusion
- **+** Small codebase with a local inspector UI and offline tests; MIT licensed
- **−** Requires a TypeSafe API key and a separate text-model key (OpenRouter in the example)
- **−** Shadow roots, frames, canvas, uploads, pop-up tabs and nested scrolling are unsupported
- **−** Benchmark is three repeats of one task on one browser profile, not a reliability test
- **−** Shares the existing Chrome profile and needs remote debugging allowed; no release published

<sub>no GPU · Needs TypeSafe API (Jev), OpenRouter or other OpenAI-compatible text model API, Chrome, Browser Harness, uv · Models: TypeSafe Jev, inception/mercury-2.5 via OpenRouter, Gemini, GLM, DeepSeek · port 8766 · [Repo](https://github.com/browser-use/jev-ultrafast) · [📖 Docs ↗](https://docs.typesafe.ai/introduction) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jev-ultrafast/)</sub>

<a name="outlines"></a>
### #&#8288;39 [outlines](https://github.com/dottxt-ai/outlines) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Aug 2026</sub>

**Python library that constrains LLM output to a type, schema or grammar.**

Outlines enforces structured output during generation. You pass a Python type, such as Literal, int, a Pydantic model or a function signature, and the model returns output matching it. The same call works across transformers, llama.cpp, vLLM, Ollama, OpenAI and Gemini backends, and it includes Jinja-based prompt templates.

- **+** Output type is a plain Python type: Literal, int, Pydantic model, union or function signature
- **+** Same model(prompt, output_type) call across transformers, llama.cpp, vLLM, Ollama, OpenAI and Gemini
- **+** Constrains generation itself, so no post-hoc JSON parsing or retry loop
- **+** Built-in Jinja prompt templates, loadable from strings or files
- **−** Library only: no server, UI or deployment tooling of its own
- **−** Dottxt API is early access and requires a request form
- **−** README does not detail constraint limits for hosted API backends
- **−** Hardware requirements for local models are not documented in the README

<sub>GPU optional · Needs transformers, pydantic · Models: transformers, llama.cpp, vLLM, Ollama, OpenAI · [Repo](https://github.com/dottxt-ai/outlines) · [📖 Docs ↗](https://dottxt-ai.github.io/outlines/latest/features/models/) · [🌐 Site ↗](https://dottxt.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/outlines/)</sub>

<a name="metagpt"></a>
### #&#8288;40 [metagpt](https://github.com/foundationagents/metagpt) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: widely used (92) · Freshness: quiet (23) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · MIT · Jan 2026</sub>

**Python multi-agent framework that turns one-line requirements into a software repo.**

MetaGPT assigns LLM-backed roles (product manager, architect, project manager, engineer) to follow predefined SOPs, turning a one-line requirement into user stories, designs, APIs and code. It runs as a CLI (`metagpt "Create a 2048 game"`) or a Python library, and also ships a Data Interpreter role for data analysis. LLM providers such as OpenAI, Azure, Ollama and Groq are set in `~/.metagpt/config2.yaml`.

- **+** Role and SOP model produces requirements, design docs and code repo from one prompt
- **+** Usable as CLI or Python library; pip install metagpt
- **+** Provider set in one YAML file: OpenAI, Azure, Ollama, Groq and others
- **+** MIT license with tutorials, agent and multi-agent guides, and research papers
- **−** Python 3.9 to below 3.12 only
- **−** Requires Node and pnpm installed before actual use
- **−** Last release was 2024-04-22; the PyPI package may lag the main branch
- **−** README calls the software-company schematic 'gradually implementing'

<sub>no GPU · Docker · Needs Python 3.9-3.11, Node.js, pnpm, LLM API key or local LLM endpoint · Models: OpenAI, Azure, Ollama, Groq · [Repo](https://github.com/foundationagents/metagpt) · [▶️ Demo ↗](https://huggingface.co/spaces/deepwisdom/MetaGPT-SoftwareCompany) · [📖 Docs ↗](https://docs.deepwisdom.ai/main/en/) · [🌐 Site ↗](https://mgx.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/metagpt/)</sub>

<a name="aisuite"></a>
### #&#8288;41 [aisuite](https://github.com/andrewyng/aisuite) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Sep 2026</sub>

**Python library with one chat API across LLM providers, plus an agents layer.**

aisuite is a Python library that exposes an OpenAI-style Chat Completions interface across providers such as OpenAI, Anthropic, Google, Mistral, Ollama and AWS, selected with a "provider:model" string. On top of that it adds tool calling from plain Python functions with max_turns, an Agents API with a Runner, toolkits for files, git and shell, and MCP server support. The desktop app OpenWorker now lives in a separate repository.

- **+** Switch providers by changing one model string, e.g. openai:gpt-4o to anthropic:...
- **+** Plain Python functions become tools; schemas generated and calls executed automatically via max_turns
- **+** Agents API includes tool policies, state stores (memory, file, Postgres) and tracing
- **+** Native MCP client support and streaming, with async variant
- **−** Library only, no server, proxy, UI, rate limiting or caching
- **−** Streaming is limited to some providers and cannot be combined with max_turns
- **−** Provider SDKs and API keys are installed and managed separately by you
- **−** OpenWorker app moved out; only an archived snapshot remains in this repo

<sub>no GPU · Needs Provider API keys, Provider SDKs (optional extras), Node/npx for some MCP servers · Models: OpenAI, Anthropic, Google, Mistral, Hugging Face · [Repo](https://github.com/andrewyng/aisuite) · [📖 Docs ↗](https://github.com/andrewyng/aisuite/blob/main/docs/chat-completions-quickstart.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aisuite/)</sub>

<a name="owl"></a>
### #&#8288;42 [owl](https://github.com/camel-ai/owl) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (37) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 20k · no license · Oct 2026</sub>

**Multi-agent framework on CAMEL for browser, search, code and document tasks.**

OWL is a Python multi-agent framework built on CAMEL-AI that runs a society of agents with toolkits for Playwright browser control, web search, document parsing, code execution and MCP servers. It reports a 69.09 average on the GAIA benchmark and ships example scripts for OpenAI, Claude, Gemini, Qwen, Deepseek and Ollama, plus a web UI. The README recommends OpenAI models and says other models score lower on complex tasks.

- **+** Reports 69.09 average on GAIA, with a separate branch for reproducing benchmark runs
- **+** Many built-in toolkits: Playwright browser, search engines, Office/PDF parsing, code execution, MCP
- **+** Example scripts for OpenAI, Claude, Gemini, Qwen, Deepseek, Azure and Ollama
- **+** Training dataset and model checkpoints released on Hugging Face
- **−** No license detected in the repository metadata
- **−** README says non-OpenAI models perform significantly worse on complex tasks
- **−** Needs models with strong tool calling; multimodal toolkits also need multimodal models
- **−** Training code is listed as coming soon; GAIA runs need separate branches

<sub>no GPU · Needs Python 3.10-3.12, CAMEL-AI, Playwright, Node.js (for MCP), LLM API key (e.g. OPENAI_API_KEY) · Models: OpenAI, Claude, Gemini, Qwen, Deepseek · [Repo](https://github.com/camel-ai/owl) · [📖 Docs ↗](https://docs.camel-ai.org/key_modules/models.html#supported-model-platforms-in-camel) · [🌐 Site ↗](https://www.camel-ai.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/owl/)</sub>

<a name="guidance"></a>
### #&#8288;43 [guidance](https://github.com/guidance-ai/guidance) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (42) · Freshness: active (81) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · May 2026</sub>

**Python library for constrained generation and control flow with LLMs.**

Guidance is a Python library that constrains language model output with regex, select lists, JSON schemas (including Pydantic models) and context-free grammars. It interleaves Python control flow with generation and works with backends such as Transformers, llama.cpp and OpenAI. When a grammar fixes upcoming tokens, it inserts them without a model forward pass.

- **+** Regex, select, JSON schema and CFG constraints guarantee output syntax
- **+** Token fast-forwarding skips forward passes when the grammar fixes the next tokens
- **+** Mock model and grammar.match() allow offline grammar debugging without API calls
- **+** @guidance functions compose into larger grammars; model objects are immutable
- **−** Full CFG support depends on the backend; README does not list which qualify
- **−** Not a full agent framework: no orchestration, memory or deployment tooling
- **−** README gives no hardware requirements or benchmarks
- **−** Jupyter widget gives the richer view; command line output is plain text

<sub>GPU optional · Needs Python, pip, Transformers, llama.cpp or OpenAI backend · Models: Transformers, llama.cpp, OpenAI · [Repo](https://github.com/guidance-ai/guidance) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/guidance/)</sub>

<a name="swarm"></a>
### #&#8288;44 [swarm](https://github.com/openai/swarm) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (45) · Freshness: recent (64) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Apr 2026</sub>

**Educational Python library for multi-agent handoffs on Chat Completions.**

Swarm is a small Python library built around two primitives: Agents (instructions plus Python functions) and handoffs, where a function returns another Agent to take over. client.run() loops over completions, tool calls, agent switches and context variable updates, and keeps no state between calls. The README marks it experimental and educational, and says the OpenAI Agents SDK has replaced it.

- **+** Two primitives, Agent and handoff, keep the whole run loop easy to read
- **+** Python functions become tool JSON schemas from type hints and docstrings
- **+** Stateless client.run() with streaming, max_turns and an execute_tools switch
- **+** Examples cover airline, support bot and triage agents, with eval samples
- **−** Superseded by the OpenAI Agents SDK, which the README recommends for production
- **−** Built on the Chat Completions API; README mentions no other providers
- **−** No persistence or memory; caller must pass state back in each run
- **−** Installed from GitHub with pip; no release published

<sub>no GPU · Needs OpenAI API, Python 3.10+ · Models: OpenAI Chat Completions models (default gpt-4o) · [Repo](https://github.com/openai/swarm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/swarm/)</sub>

<a name="pandas-ai"></a>
### #&#8288;45 [pandas-ai](https://github.com/sinaptik-ai/pandas-ai) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: known (49) · Freshness: quiet (15) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Oct 2025</sub>

**Python library for asking natural-language questions about DataFrames.**

PandasAI adds a chat method to DataFrames. It sends questions to an LLM through LiteLLM, runs the generated code, and returns answers or charts, including across multiple DataFrames. An optional pandasai-docker package runs the generated code in a Docker sandbox. The repo is MIT except the pandasai/ee directory, which has a separate license.

- **+** Two-line usage: read a CSV, then call df.chat() with a question
- **+** Handles questions across several DataFrames and generates charts
- **+** Optional Docker sandbox isolates execution of LLM-generated code
- **+** LLM backend is swappable via the pandasai-litellm package
- **−** Without the Docker sandbox, generated code runs in your own Python process
- **−** Python 3.8 to 3.11 only, per the README
- **−** pandasai/ee directory is under a separate license; managed and enterprise tiers are paid
- **−** Needs an LLM API key or provider; local model setup is not covered in the README

<sub>no GPU · Compose · Needs pandasai-litellm, LLM provider API key (e.g. OpenAI), Docker (optional, for sandbox via pandasai-docker) · Models: LiteLLM-supported providers, OpenAI gpt-4.1-mini (example) · [Repo](https://github.com/sinaptik-ai/pandas-ai) · [📖 Docs ↗](https://docs.pandas-ai.com/) · [🌐 Site ↗](https://pandas-ai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pandas-ai/)</sub>

<a name="qwen-agent"></a>
### #&#8288;46 [qwen-agent](https://github.com/qwenlm/qwen-agent) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (27) · Freshness: slowing (37) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Mar 2026</sub>

**Python framework for building tool-using LLM agents on Qwen models.**

Qwen-Agent is a Python library for building agents on Qwen models, with function calling, MCP tools, RAG over documents and a Docker-based code interpreter. It talks to Alibaba DashScope or any OpenAI-compatible server such as vLLM or Ollama. It includes a Gradio web UI and example apps like BrowserQwen, and serves as the backend of Qwen Chat.

- **+** Built-in function calling with parallel calls, plus MCP server support
- **+** Works with DashScope or any OpenAI-compatible endpoint, including vLLM and Ollama
- **+** Gradio WebUI launches with one line around an existing agent
- **+** Includes RAG examples for question answering over very long documents
- **−** Tool-call templates and examples are tuned for Qwen models specifically
- **−** Code interpreter needs local Docker; README advises caution in production
- **−** GUI requires Python 3.10 or higher
- **−** Last release is 2025-05-29, well behind recent commits

<sub>GPU optional · Needs DashScope API or OpenAI-compatible model server (vLLM, Ollama), Docker (code interpreter), Node.js, uv (MCP examples) · Models: Qwen3.5, Qwen3, Qwen3-Coder, Qwen3-VL, Qwen2.5 · [Repo](https://github.com/qwenlm/qwen-agent) · [📖 Docs ↗](https://qwenlm.github.io/Qwen-Agent/en/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qwen-agent/)</sub>

<a name="rasa"></a>
### #&#8288;47 [rasa](https://github.com/rasahq/rasa) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: known (40) · Freshness: quiet (15) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Dec 2025</sub>

**Python framework for building contextual text and voice assistants.**

Rasa Open Source is a Python framework for building contextual text and voice assistants, with connectors for Slack, Telegram, Twilio, Facebook Messenger, Microsoft Bot Framework and others. The repository is in maintenance mode. The README points new work to Hello Rasa, a browser playground built on the CALM engine, where an LLM handles dialogue understanding and flows enforce business logic.

- **+** Built-in connectors for Slack, Telegram, Twilio, Mattermost, Rocket.Chat, Webex and custom channels
- **+** Apache-2.0 license, installable from PyPI, buildable from source with Poetry
- **+** Handles layered multi-turn conversations with business logic kept in code
- **+** Semantic Versioning with a published release and maintenance policy
- **−** Maintenance mode; README directs new development to Hello Rasa and CALM
- **−** Last release is 2025-01-14, so releases have slowed
- **−** Hello Rasa is a hosted playground; scaling path leads to the Rasa Platform
- **−** README gives no hardware requirements, ports or supported model list

<sub>Docker + Compose · Needs Python, Poetry (for development) · [Repo](https://github.com/rasahq/rasa) · [▶️ Demo ↗](https://hello.rasa.ai/) · [📖 Docs ↗](https://rasa.com/docs/rasa/) · [🌐 Site ↗](https://rasa.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rasa/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
