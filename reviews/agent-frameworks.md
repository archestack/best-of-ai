# 🧰 Agent frameworks and SDKs reviews · Best of Open-Source AI

Libraries for building agents and LLM apps in code: tool calling, planning, multi-agent setups and browser control. Back to the [leaderboard](../README.md#-agent-frameworks-and-sdks).

<sub>🌐 Also on the web: [Agent frameworks and SDKs on archestack.com](https://archestack.com/best-of-ai/agent-frameworks/), each project on its own page.</sub>

<a name="ppt-master"></a>
### 🥇 [ppt-master](https://github.com/hugohe3/ppt-master) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 66k · MIT · Oct 2026</sub>

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

<a name="openai-agents-python"></a>
### 🥈 [openai-agents-python](https://github.com/openai/openai-agents-python) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Oct 2026</sub>

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

<a name="langchain"></a>
### 🥉 [langchain](https://github.com/langchain-ai/langchain) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 148k · MIT · Oct 2026</sub>

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
### #&#8288;4 [browser-use](https://github.com/browser-use/browser-use) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 119k · MIT · Oct 2026</sub>

**Python library that lets an LLM agent control a web browser.**

Browser Use is a Python library where an Agent takes a natural-language task and drives a local or cloud browser to complete it. It works with OpenAI, Anthropic, Google and Ollama models, or the project's own BU2 model via an API key. The README also describes a CLI skill for coding agents and a paid hosted cloud with stealth browsers.

- **+** Works with several LLM providers, plus local models through Ollama
- **+** Custom actions can be registered with the Tools decorator
- **+** Can reuse a local Chrome profile for authenticated sessions
- **+** Same agent code runs on a local browser or a cloud browser
- **−** Stealth, CAPTCHA solving and residential proxies require paid Browser Use Cloud
- **−** BU2 model needs a Browser Use API key and is not local
- **−** Cloud profile sync transfers cookies only, not local storage or extensions
- **−** Local-model quality and hardware needs are unspecified in the README

<sub>GPU optional · Docker · Needs Chrome or Chromium, LLM provider API key, Browser Use API key (optional) · Models: OpenAI, Anthropic, Google, Ollama, BU2 (ChatBrowserUse) · [Repo](https://github.com/browser-use/browser-use) · [▶️ Demo ↗](https://browser-use.com/showcase) · [📖 Docs ↗](https://docs.browser-use.com) · [🌐 Site ↗](https://browser-use.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/browser-use/)</sub>

<a name="copilotkit"></a>
### #&#8288;5 [copilotkit](https://github.com/copilotkit/copilotkit) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Oct 2026</sub>

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

<a name="mastra"></a>
### #&#8288;6 [mastra](https://github.com/mastra-ai/mastra) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · custom license · Oct 2026</sub>

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

<a name="tradingagents"></a>
### #&#8288;7 [tradingagents](https://github.com/tauricresearch/tradingagents) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 113k · Apache-2.0 · Oct 2026</sub>

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

<a name="haystack"></a>
### #&#8288;8 [haystack](https://github.com/deepset-ai/haystack) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · Apache-2.0 · Oct 2026</sub>

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

<a name="crewai"></a>
### #&#8288;9 [crewai](https://github.com/crewaiinc/crewai) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · MIT · Oct 2026</sub>

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
### #&#8288;10 [agno](https://github.com/agno-agi/agno) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;11 [agent-browser](https://github.com/vercel-labs/agent-browser) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;12 [langgraph](https://github.com/langchain-ai/langgraph) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · MIT · Oct 2026</sub>

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
### #&#8288;13 [deepagents](https://github.com/langchain-ai/deepagents) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

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
### #&#8288;14 [ai](https://github.com/vercel/ai) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · custom license · Oct 2026</sub>

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

<a name="adk-python"></a>
### #&#8288;15 [adk-python](https://github.com/google/adk-python) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Oct 2026</sub>

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

<a name="pydantic-ai"></a>
### #&#8288;16 [pydantic-ai](https://github.com/pydantic/pydantic-ai) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Oct 2026</sub>

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
### #&#8288;17 [eliza](https://github.com/elizaos/eliza) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Oct 2026</sub>

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

<a name="pipecat"></a>
### #&#8288;18 [pipecat](https://github.com/pipecat-ai/pipecat) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · BSD-2-Clause · Oct 2026</sub>

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

<a name="llama-index"></a>
### #&#8288;19 [llama_index](https://github.com/run-llama/llama_index) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · MIT · Oct 2026</sub>

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
### #&#8288;20 [agentscope](https://github.com/agentscope-ai/agentscope) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Oct 2026</sub>

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

<a name="page-agent"></a>
### #&#8288;21 [page-agent](https://github.com/alibaba/page-agent) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Sep 2026</sub>

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

<a name="nanobrowser"></a>
### #&#8288;22 [nanobrowser](https://github.com/nanobrowser/nanobrowser) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

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

<a name="dspy"></a>
### #&#8288;23 [dspy](https://github.com/stanfordnlp/dspy) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · MIT · Oct 2026</sub>

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

<a name="stagehand"></a>
### #&#8288;24 [stagehand](https://github.com/browserbase/stagehand) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Oct 2026</sub>

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

<a name="semantic-kernel"></a>
### #&#8288;25 [semantic-kernel](https://github.com/microsoft/semantic-kernel) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Oct 2026</sub>

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

<a name="langchainjs"></a>
### #&#8288;26 [langchainjs](https://github.com/langchain-ai/langchainjs) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

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

<a name="camofox-browser"></a>
### #&#8288;27 [camofox-browser](https://github.com/jo-inc/camofox-browser) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Oct 2026</sub>

**REST API server that gives AI agents an anti-detection Camoufox browser.**

Wraps Camoufox, a Firefox fork with C++-level fingerprint spoofing, in a REST API for agents. Pages are returned as accessibility snapshots with stable element refs (e1, e2) instead of raw HTML. It adds per-user session isolation, cookie import, proxy with GeoIP, search macros, and an OpenClaw plugin.

- **+** Accessibility snapshots with stable element refs, stated as about 90% smaller than raw HTML
- **+** Per-user session isolation with persisted cookies and localStorage under ~/.camofox/profiles
- **+** Proxy support including backconnect sticky sessions, with GeoIP-derived locale and timezone
- **+** Idle shutdown keeps memory at about 40MB when idle, per the README
- **−** First run downloads the Camoufox binary, about 300MB
- **−** Docker build needs make or build.ps1; plain docker build is explicitly unsupported
- **−** Anonymized crash telemetry to a hosted endpoint is on by default; opt out via env var
- **−** Firefox-based, so Playwright video recording is unavailable; tracing is the substitute

<sub>no GPU · Docker · Needs Camoufox, yt-dlp (optional), Node.js · port 9377 · [Repo](https://github.com/jo-inc/camofox-browser) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/camofox-browser/)</sub>

<a name="tambo"></a>
### #&#8288;28 [tambo](https://github.com/tambo-ai/tambo) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**React toolkit where an agent picks and renders your components.**

Tambo is a React SDK plus backend for generative UI. You register components with Zod schemas, and the agent chooses one and streams its props to it. The backend runs the LLM loop and conversation state, supports MCP servers and browser-side tools, and works with OpenAI, Anthropic, Gemini, Mistral, Cerebras or OpenAI-compatible providers. Tambo Cloud shuts down October 31, 2026, so new use means self-hosting.

- **+** Zod-schema components become LLM tool definitions; props stream to the UI
- **+** Supports MCP tools, prompts, elicitations and sampling
- **+** Browser-side local tools can touch the DOM or React state
- **+** SDK and backend are MIT; some workspaces such as apps/api are Apache-2.0
- **−** Hosted Tambo Cloud closes October 31, 2026; user data is deleted November 30
- **−** New signups are closed, and the team has moved on to a different product
- **−** React only; no other frontend frameworks are mentioned
- **−** Self-hosted resource needs are not given in the README

<sub>no GPU · Compose · Needs LLM provider API key · Models: OpenAI, Anthropic, Google Gemini, Mistral, Cerebras · [Repo](https://github.com/tambo-ai/tambo) · [📖 Docs ↗](https://docs.tambo.co) · [🌐 Site ↗](https://tambo.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tambo/)</sub>

<a name="browseros"></a>
### #&#8288;29 [browseros](https://github.com/browseros-ai/browseros) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · AGPL-3.0 · Oct 2026</sub>

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

<a name="instructor"></a>
### #&#8288;30 [instructor](https://github.com/567-labs/instructor) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (43) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

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

<a name="agent-framework"></a>
### #&#8288;31 [agent-framework](https://github.com/microsoft/agent-framework) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

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
### #&#8288;32 [llm](https://github.com/simonw/llm) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

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

<a name="ten-framework"></a>
### #&#8288;33 [ten-framework](https://github.com/ten-framework/ten-framework) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (33) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Oct 2026</sub>

**Framework for building real-time voice and multimodal conversational agents.**

TEN is a framework for real-time multimodal conversational agents, built from extensions for STT, LLM and TTS that are wired together in a graph. The repo ships example agents: a voice assistant over RTC or WebSocket, speech-to-speech, speaker diarization, lip-sync avatars, SIP calls, transcription and an ESP32-S3 board demo. A TMAN Designer UI on port 49483 edits extension properties.

- **+** Many working voice examples: SIP calls, diarization, Live2D avatars, ESP32-S3 hardware
- **+** Companion projects for VAD and turn detection, plus a memory extension example
- **+** TMAN Designer lets you set STT, LLM and TTS keys in a graph UI
- **+** Frontend and backend can be split, e.g. UI on Vercel or Netlify, backend on port 8080
- **−** License is Apache 2.0 with additional restrictions, not plain Apache 2.0
- **−** Quick start needs Agora credentials plus OpenAI, Deepgram and ElevenLabs keys
- **−** Quick start builds in a dev container and takes about 5-8 minutes
- **−** Examples are mostly tied to hosted APIs; local-model setup is not documented in the README

<sub>RAM ≥ 4 GB · no GPU · Needs Docker, Node.js 18, Agora App ID and Certificate, OpenAI API key, Deepgram API key, ElevenLabs API key · Models: OpenAI, Deepgram, ElevenLabs · port 3000 · [Repo](https://github.com/ten-framework/ten-framework) · [📖 Docs ↗](https://theten.ai/docs) · [🌐 Site ↗](https://theten.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ten-framework/)</sub>

<a name="harness-sdk"></a>
### #&#8288;34 [harness-sdk](https://github.com/strands-agents/harness-sdk) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Oct 2026</sub>

**Python and TypeScript SDK for building agents, with a prebuilt harness.**

Monorepo for the Strands Agents SDKs in Python (3.10+) and TypeScript (Node.js 22+), plus a prebuilt harness created with create_harness() or createHarness(). The SDK covers the agent loop with turn and token limits, tools, MCP, structured output, multi-agent patterns, sessions, guardrails, tracing and evals. It runs in your process with no hosted control plane.

- **+** Same agent model in Python and TypeScript, with a CLI and an MCP docs server
- **+** Providers include Bedrock, Anthropic, OpenAI, Gemini and Ollama, plus custom ones
- **+** Hooks can intercept any step of the loop; tracing is on by default
- **+** Harness gives a working agent in one call, and you can drop to the SDK
- **−** TypeScript Agent defaults to Amazon Bedrock, so AWS credentials are needed unless you set a model
- **−** Several packages (harness, SDK, tools, CLI) to choose between; the split takes time to learn
- **−** Harness defaults are described as benchmarked, but the README gives no numbers
- **−** Resource requirements are not stated in the README

<sub>no GPU · Needs Python 3.10+ or Node.js 22+, Model provider credentials (Amazon Bedrock is the TypeScript SDK default) · Models: Amazon Bedrock, Anthropic, OpenAI, Gemini, Ollama · [Repo](https://github.com/strands-agents/harness-sdk) · [📖 Docs ↗](https://strandsagents.com/docs/user-guide/harness/) · [🌐 Site ↗](https://strandsagents.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/harness-sdk/)</sub>

<a name="langchain4j"></a>
### #&#8288;35 [langchain4j](https://github.com/langchain4j/langchain4j) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

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

<a name="praisonai"></a>
### #&#8288;36 [praisonai](https://github.com/mervinpraison/praisonai) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · MIT · Oct 2026</sub>

**Python SDK and CLI for building multi-agent workflows with tools and MCP.**

PraisonAI is a Python framework (praisonaiagents SDK plus praisonai CLI) for defining agents with instructions, tools, memory, knowledge and guardrails, and chaining them in AgentFlow graphs with routing, parallel steps and loops. Tools can run in remote sandboxes such as Docker, E2B, Modal, Daytona and Fly.io. Optional extras add a Telegram/Slack/Discord dashboard, a visual flow builder and a chat UI.

- **+** Workflows can be written in Python or in YAML with no code
- **+** Tools can run in Docker, E2B, Modal, Daytona, Fly.io, SSH or subprocess
- **+** Explicit loop controls: iteration cap, budget ceiling, doom-loop detection on by default
- **+** Lists 24 providers including Ollama and vLLM; MCP supported
- **−** Large surface (SDK, CLI, Claw, Flow, UI) split across several pip extras
- **−** Quick start assumes an OpenAI API key; local model setup is left to provider examples
- **−** README is marketing-heavy; production deployment and scaling details are unknown
- **−** No Dockerfile or compose file detected in the repository

<sub>no GPU · Docker + Compose · Needs LLM provider API key (e.g. OpenAI) or local Ollama/vLLM, Optional sandbox backends: Docker, E2B, Modal, Daytona, Fly.io · Models: OpenAI, Anthropic, Google Gemini, Ollama, vLLM · [Repo](https://github.com/mervinpraison/praisonai) · [📖 Docs ↗](https://docs.praison.ai) · [🌐 Site ↗](https://praison.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/praisonai/)</sub>

<a name="camel"></a>
### #&#8288;37 [camel](https://github.com/camel-ai/camel) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (55) · Freshness: active (97) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

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

<a name="rig"></a>
### #&#8288;38 [rig](https://github.com/0xplaygrounds/rig) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · MIT · Oct 2026</sub>

**Rust library for building LLM agents, plus a Bevy-based terminal coding agent.**

Rig is a Rust library that puts 20+ model providers and 10+ vector stores behind one interface, with agents that support tools, multi-turn streaming and typed hooks. The same repo ships `rig`, a terminal coding agent built as a Bevy app whose tools, commands and sessions are plugins listed in `plugins.toml`. The library is pre-1.0 and releases contain breaking changes.

- **+** 20+ model providers and 10+ vector stores behind one interface
- **+** Covers completion, embeddings, transcription, audio and image generation
- **+** Core and agent runtime target browser WASM (wasm32-unknown-unknown)
- **+** OpenTelemetry GenAI conventions and replay of agent effects via rig-cassette
- **−** Pre-1.0; each release contains breaking changes, so migration notes must be read
- **−** Rust only; the coding agent needs Rust 1.97.1 or newer
- **−** Coding agent runs on Linux and macOS; Windows is not listed
- **−** Integrations are separate crates enabled by feature flags, adding setup steps

<sub>GPU optional · Needs Rust 1.97.1+, tokio, LLM provider API key · Models: OpenAI, AWS Bedrock, Google Vertex AI, Google Gemini gRPC, Candle (local Llama/SmolLM2/Qwen3) · [Repo](https://github.com/0xplaygrounds/rig) · [📖 Docs ↗](https://rig.rs/docs) · [🌐 Site ↗](https://rig.rs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rig/)</sub>

<a name="open-multi-agent"></a>
### #&#8288;39 [open-multi-agent](https://github.com/open-multi-agent/open-multi-agent) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · MIT · Oct 2026</sub>

**TypeScript runtime for multi-agent teams with approval gates and offline run review.**

OMA is a TypeScript library that coordinates teams of agents. In runTeam(), one model call plans a task graph, a deterministic scheduler executes it, and a second call writes the final answer. It adds durable human approvals, a run journal checked offline with verifyRun(), and an offline Run Viewer. It has no telemetry or hosted backend.

- **+** Three modes: runAgent, runTasks for explicit pipelines, runTeam for goal-planned task graphs
- **+** Approval gates before plans, tasks or tool calls; persistent storage lets restarts resume
- **+** Offline Run Viewer and run journal; no telemetry or hosted control plane
- **+** Egress policy (offline or allowlist) checked before built-in adapters connect
- **−** TypeScript and Node.js only; Node 20 is upstream-EOL and slated for removal
- **−** Approval UI and notifications must be built by the application
- **−** verifyRun() checks consistency only; it does not prove the journal was never edited
- **−** Process and ACP external-agent backends sit outside the egress policy

<sub>no GPU · Needs Node.js 20+ · Models: Anthropic, OpenAI, Azure OpenAI, Bedrock, Gemini · [Repo](https://github.com/open-multi-agent/open-multi-agent) · [📖 Docs ↗](https://open-multi-agent.com/getting-started/introduction/?utm_source=github&utm_medium=readme) · [🌐 Site ↗](https://open-multi-agent.com/?utm_source=github&utm_medium=readme) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-multi-agent/)</sub>

<a name="mobilerun"></a>
### #&#8288;40 [mobilerun](https://github.com/droidrun/mobilerun) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.7k · MIT · Oct 2026</sub>

**LLM agent framework that taps, swipes and types on Android and iOS devices.**

Mobilerun drives Android and iOS devices from natural-language tasks through a CLI, terminal UI or Python API. A Portal app on the device exposes the accessibility tree, screenshots and input actions to the LLM agent, with an optional manager-executor reasoning mode for longer tasks. It works with OpenAI, Anthropic, Gemini, xAI, Ollama, DeepSeek, OpenRouter and OpenAI-compatible endpoints.

- **+** Combines accessibility tree with screenshots; --vision-only covers apps without a11y data
- **+** Many providers supported, including local Ollama models
- **+** Custom tools, structured output and app cards extend agent behavior in Python
- **+** Tracing via Arize Phoenix or Langfuse, plus saved trajectories
- **−** Requires ADB, USB debugging and installing the Portal app on the device
- **−** iOS setup is a separate flow and is documented only briefly
- **−** Python 3.14 is not supported; needs >=3.11,<3.14
- **−** Hosted devices and fleet features are in the paid Mobilerun Cloud, not the framework

<sub>no GPU · Docker · Needs ADB, Mobilerun Portal app, Android device or iOS device/simulator, LLM provider API or Ollama · Models: OpenAI, Anthropic, Gemini, xAI, Ollama · [Repo](https://github.com/droidrun/mobilerun) · [📖 Docs ↗](https://docs.mobilerun.ai) · [🌐 Site ↗](https://mobilerun.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mobilerun/)</sub>

<a name="chatterbot"></a>
### #&#8288;41 [chatterbot](https://github.com/gunthercox/chatterbot) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (47) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · BSD-3-Clause · Aug 2026</sub>

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

<a name="voltagent"></a>
### #&#8288;42 [voltagent](https://github.com/voltagent/voltagent) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Sep 2026</sub>

**TypeScript framework for building multi-agent apps with workflows and memory.**

VoltAgent is a TypeScript framework for defining agents with typed tools, memory adapters, workflows, supervisor and sub-agent teams, guardrails, evals, voice and MCP support. Providers such as OpenAI, Anthropic and Google are swapped through config. A separate VoltOps Console adds traces, logs, prompts, deployment and triggers, offered as cloud or self-hosted.

- **+** Workflow engine with suspend/resume for human-in-the-loop steps
- **+** Supervisor and sub-agent orchestration, Zod-typed tools and MCP client built in
- **+** Durable memory adapters, e.g. LibSQL with a local file database
- **+** create-voltagent-app scaffolds an agent, workflow and Hono server on port 3141
- **−** TypeScript/Node only; no Python SDK mentioned in the README
- **−** Tracing, deployment and managed knowledge base tie into the VoltOps Console
- **−** README does not say which console features are self-hosted versus cloud-only
- **−** No Docker or compose files detected in the repository

<sub>no GPU · Needs Node.js, LLM provider API (e.g. OpenAI), VoltOps Console (optional) · Models: OpenAI, Anthropic, Google · port 3141 · [Repo](https://github.com/voltagent/voltagent) · [▶️ Demo ↗](https://console.voltagent.dev/demo) · [📖 Docs ↗](https://voltagent.dev/docs/) · [🌐 Site ↗](https://voltagent.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voltagent/)</sub>

<a name="smolagents"></a>
### #&#8288;43 [smolagents](https://github.com/huggingface/smolagents) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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

<a name="eino"></a>
### #&#8288;44 [eino](https://github.com/cloudwego/eino) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

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

<a name="atomic-agents"></a>
### #&#8288;45 [atomic-agents](https://github.com/eigenwise/atomic-agents) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Oct 2026</sub>

**Python framework for building agents from typed Pydantic input and output schemas.**

Atomic Agents is a Python library for composing LLM agents and tools from small components, each with Pydantic input and output schemas, built on Instructor. Agents combine a system prompt, history and runtime context providers, and chain by matching one component's output schema to another's input schema. A CLI, Atomic Assembler, downloads tools from the Atomic Forge collection.

- **+** Schema-typed inputs and outputs make agents and tools swappable and chainable
- **+** Works with providers Instructor supports, including OpenAI, Anthropic, Gemini, Groq and Ollama
- **+** Every agent and tool run is an OpenTelemetry span, usable with Phoenix, Langfuse or OTLP
- **+** Atomic Forge provides ready tools such as SearXNG, Tavily, PDF Reader and Calculator
- **−** Code-only: no visual builder or hosted runtime
- **−** Version 2.0 has breaking changes for v1.x users
- **−** CLI downloads only tools; agents and pipelines are listed as coming later
- **−** Non-OpenAI providers need separate Instructor extras installed

<sub>no GPU · Needs Instructor, Pydantic, LLM provider API or local model server · Models: OpenAI, Anthropic, Gemini, Groq, Ollama · [Repo](https://github.com/eigenwise/atomic-agents) · [📖 Docs ↗](https://eigenwise.github.io/atomic-agents/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/atomic-agents/)</sub>

<a name="openmanus"></a>
### #&#8288;46 [openmanus](https://github.com/foundationagents/openmanus) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: widely used (91) · Freshness: recent (70) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Aug 2026</sub>

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

<a name="agent-native"></a>
### #&#8288;47 [agent-native](https://github.com/builderio/agent-native) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: ready (85) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 7.5k · no license · Oct 2026</sub>

**TypeScript framework for agents that share actions and state with an app UI.**

Agent-Native is a TypeScript framework where each capability is defined once as a zod-validated action. The agent calls it as a tool, and the React UI calls it through hooks such as useActionQuery. The same action is also exposed over HTTP, MCP, A2A and CLI. It ships agent chat, auth and permissions, skills and memory, scheduled automations, and PostgreSQL storage (PGlite for local development).

- **+** One action definition serves agent tool, UI call, HTTP, MCP, A2A and CLI
- **+** Agent and UI share validation, permissions, data and current UI state
- **+** Includes auth, memory, automations and agent teams out of the box
- **+** Sample apps (Mail, Calendar, Slides, Analytics and others) to fork as starting points
- **−** README does not list supported LLM providers or models
- **−** Examples and hooks are React-oriented; other front-ends are not documented in the README
- **−** No Docker or compose setup shown in the README
- **−** Production database is PostgreSQL only, per the README

<sub>Needs Node.js, PostgreSQL (production), PGlite (local development), LLM provider · [Repo](https://github.com/builderio/agent-native) · [📖 Docs ↗](https://agent-native.com/docs) · [🌐 Site ↗](https://agent-native.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-native/)</sub>

<a name="spring-ai-alibaba"></a>
### #&#8288;48 [spring-ai-alibaba](https://github.com/alibaba/spring-ai-alibaba) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (32) · Freshness: active (96) · Maintenance: fair (53) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**Java framework for building agents and multi-agent workflows on Spring AI.**

Spring AI Alibaba is a Java framework built on Spring AI for writing agents, graph-based workflows and multi-agent setups. It ships an Agent Framework with ReactAgent and Sequential, Parallel, Routing and Loop agents, plus a Graph runtime for stateful workflows. A separate Admin platform adds visual agent building, tracing, evaluation and MCP management.

- **+** Built-in Sequential, Parallel, Routing and Loop agent patterns plus a lower-level Graph API
- **+** Context engineering hooks: human-in-the-loop, context compaction, tool retry, call limits
- **+** A2A support through Nacos integration for distributed agents
- **+** Supports DashScope and OpenAI models, tool calling and MCP via Spring AI
- **−** Java and Spring only; requires JDK 17+
- **−** Quick start and examples default to a DashScope (Aliyun Bailian) API key
- **−** Admin platform lives in a separate repository
- **−** Community channels listed are DingTalk and WeChat only

<sub>no GPU · Needs JDK 17+, LLM provider API key, Nacos (for A2A and dynamic config) · Models: DashScope, OpenAI, DeepSeek · port 8080 · [Repo](https://github.com/alibaba/spring-ai-alibaba) · [📖 Docs ↗](https://java2ai.com/docs/quick-start/) · [🌐 Site ↗](https://java2ai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/spring-ai-alibaba/)</sub>

<a name="parlant"></a>
### #&#8288;49 [parlant](https://github.com/emcie-co/parlant) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (57) · Freshness: active (96) · Maintenance: weak (29) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Jul 2026</sub>

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

<a name="langchaingo"></a>
### #&#8288;50 [langchaingo](https://github.com/tmc/langchaingo) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.7k · MIT · Oct 2026</sub>

**Go port of LangChain for building LLM applications.**

LangChainGo is the Go implementation of LangChain, a library for composing LLM calls in Go programs. The README shows an OpenAI example using the llms package and points to a docs site, a pkg.go.dev reference and an examples directory. Provider, vector store and feature coverage are not listed in the README.

- **+** Native Go library that compiles into your service binary
- **+** MIT license with a docs site, API reference and examples directory
- **+** Common llms interface across providers, shown with OpenAI in the README
- **+** Linked blog posts cover Gemini and Ollama usage from Go
- **−** README does not list supported providers, vector stores or agent features
- **−** Feature parity with Python LangChain is not stated
- **−** README says development is moving to a community effort and seeks maintainers
- **−** README shows only a basic completion example, no agents or RAG

<sub>no GPU · Needs Go toolchain, LLM provider API (e.g. OpenAI) · Models: OpenAI, Gemini, Ollama · [Repo](https://github.com/tmc/langchaingo) · [📖 Docs ↗](https://tmc.github.io/langchaingo/docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langchaingo/)</sub>

<a name="agent-squad"></a>
### #&#8288;51 [agent-squad](https://github.com/2fastlabs/agent-squad) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · Apache-2.0 · Oct 2026</sub>

**Routes queries to specialized agents in Python, TypeScript and Swift.**

Agent Squad classifies each user query, picks the most suitable agent from those you register, and keeps conversation context across agents and sessions. It ships pre-built agents (Bedrock, Anthropic, OpenAI, Lex, Lambda), classifiers, storage, a SupervisorAgent for parallel team coordination, and a GroundedAgent that separates tool calling from answer writing. Python and TypeScript have feature parity; a Swift runtime targets iOS 16+ and macOS 14+.

- **+** Same orchestration model in Python 3.11+, TypeScript and on-device Swift
- **+** Classifier routing, streaming and non-streaming responses, pluggable storage and retrievers
- **+** SupervisorAgent queries sub-agents in parallel; GroundedAgent limits replies to fetched tool output
- **+** Swift runtime supports MCP tools, realtime voice and OTLP tracing
- **−** Pre-built agents and examples lean toward AWS (Bedrock, Lex, Lambda)
- **−** JevClassifier needs a TypeSafe AI API key and a paid external service
- **−** Swift quick start pins the main branch, not a tagged version
- **−** Moved from awslabs and renamed from multi-agent-orchestrator; old links and dependencies break

<sub>no GPU · Needs LLM provider API (Bedrock, Anthropic or OpenAI), TypeSafe AI API key (JevClassifier only) · Models: Amazon Bedrock, Anthropic, OpenAI, Amazon Lex, AWS Lambda · [Repo](https://github.com/2fastlabs/agent-squad) · [📖 Docs ↗](https://2fastlabs.github.io/agent-squad/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-squad/)</sub>

<a name="outlines"></a>
### #&#8288;52 [outlines](https://github.com/dottxt-ai/outlines) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Aug 2026</sub>

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

<a name="guardrails"></a>
### #&#8288;53 [guardrails](https://github.com/guardrails-ai/guardrails) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Aug 2026</sub>

**Python framework for validating LLM inputs and outputs and generating structured data.**

Guardrails is a Python library that wraps LLM calls with input and output guards built from validators, such as regex match, competitor check and toxic language. It also produces structured output from Pydantic models, using function calling or a schema added to the prompt. Guards run in-process or behind a Flask REST server started with `guardrails start`, which exposes an OpenAI SDK-compatible endpoint.

- **+** Several validators combine in one Guard, each with its own on_fail action
- **+** Structured output from Pydantic models via function calling or prompt schema
- **+** Guard server exposes an OpenAI SDK-compatible base URL for existing clients
- **+** Custom validators supported; works with proprietary and open-source LLMs
- **−** Hosted remote inferencing is being discontinued, planned cutoff August 25, 2026
- **−** Validators are moving to separate PyPI packages, so existing installs need migration
- **−** Hub validators need separate installs and `guardrails configure` setup
- **−** README examples use the legacy OpenAI completions API; one sample output is malformed

<sub>Needs Guardrails Hub validators (pip packages), LLM provider API (e.g. OpenAI) · Models: OpenAI, any LLM, proprietary or open-source · port 8000 · [Repo](https://github.com/guardrails-ai/guardrails) · [📖 Docs ↗](https://guardrailsai.com/guardrails/docs) · [🌐 Site ↗](https://www.guardrailsai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/guardrails/)</sub>

<a name="jev-ultrafast"></a>
### #&#8288;54 [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: weak (14) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Sep 2026</sub>

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

<a name="genkit"></a>
### #&#8288;55 [genkit](https://github.com/genkit-ai/genkit) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · Apache-2.0 · Oct 2026</sub>

**Multi-language SDK for building LLM flows, tools and agents, with a local dev UI.**

Genkit is a framework from Google's Firebase team for adding model calls, structured output, tool calling, RAG and multi-step flows to server-side apps. It has SDKs for JavaScript/TypeScript and Go (production-ready), Python (Beta) and Dart (Preview), with plugins for Google, OpenAI, Anthropic and Ollama. A local CLI and Developer UI run flows, show execution traces and review evaluations.

- **+** Same API across TypeScript, Go, Python and Dart SDKs
- **+** Local Developer UI with playgrounds, execution traces and evaluation results
- **+** Provider plugins for Google, OpenAI, Anthropic and Ollama behind one interface
- **+** Deploys to Firebase, Cloud Run or any host that runs the chosen language
- **−** Python is Beta and Dart is Preview; only JS/TS and Go are production-ready
- **−** Production monitoring dashboard is described in the Firebase console, tying it to Google
- **−** Anthropic plugin is linked from a third-party docs site, not the main docs
- **−** Library only: no hosted UI, user accounts or ready-made agent app

<sub>no GPU · Needs Model provider API key (e.g. Google, OpenAI, Anthropic) or local Ollama · Models: Google Gemini, OpenAI, Anthropic, Ollama, Vertex AI · [Repo](https://github.com/genkit-ai/genkit) · [▶️ Demo ↗](https://examples.genkit.dev) · [📖 Docs ↗](https://genkit.dev/docs/js/get-started/) · [🌐 Site ↗](https://genkit.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/genkit/)</sub>

<a name="gepa"></a>
### #&#8288;56 [gepa](https://github.com/gepa-ai/gepa) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: patchy (47) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Oct 2026</sub>

**Python library that evolves prompts and other text artifacts using LLM reflection.**

GEPA (Genetic-Pareto) optimizes text parameters such as prompts, code and agent configurations against a metric you supply. An LLM reads full execution traces to diagnose failures, proposes mutations, and keeps a Pareto frontier of candidates. It exposes gepa.optimize, a general optimize_anything API, adapters for DSPy, MCP, RAG and LangChain, and is also available as dspy.GEPA.

- **+** Reads full execution traces, not just a scalar score, to guide each mutation
- **+** README reports 100-500 evaluations versus 5,000-25,000+ for GRPO
- **+** Built-in adapters for DSPy, MCP, generic RAG, LangChain and TerminalBench
- **+** Integrated in DSPy, MLflow, Opik, Pydantic AI and Google ADK
- **−** Needs a measurable evaluator and a dataset or metric to optimize against
- **−** Reflection step depends on a strong LLM (examples use openai/gpt-5), adding API cost
- **−** Optimizes text artifacts only; no weight fine-tuning
- **−** Benchmark claims in the README come from the authors and partners

<sub>no GPU · Needs LLM API for task and reflection models (e.g. OpenAI) · Models: OpenAI-style provider/model strings, any LLM via adapter, DSPy programs, LangChain pipelines · [Repo](https://github.com/gepa-ai/gepa) · [📖 Docs ↗](https://gepa-ai.github.io/gepa/guides/quickstart/) · [🌐 Site ↗](https://gepa-ai.github.io/gepa/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gepa/)</sub>

<a name="vision-agents"></a>
### #&#8288;57 [vision-agents](https://github.com/getstream/vision-agents) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · Apache-2.0 · Sep 2026</sub>

**Python framework for real-time voice and video agents with vision models.**

Vision Agents is a Python library for building agents that watch and listen to live video calls over WebRTC. It chains processors such as YOLO or Roboflow with realtime LLMs like Gemini Live and OpenAI Realtime. It also adds STT, TTS, turn detection, MCP tool calling, RAG, and Twilio or Telnyx phone calls. It is built by Stream and uses Stream's edge network by default.

- **+** Pluggable processor pipeline for YOLO, Roboflow, or custom PyTorch/ONNX models alongside LLMs
- **+** Many integrations: OpenAI, Gemini, xAI, Deepgram, ElevenLabs, Cartesia, Kokoro, Twilio, Telnyx
- **+** Guides for HTTP server, Prometheus metrics, horizontal scaling and Kubernetes deployment
- **+** Uses native OpenAI, Gemini and Claude SDK methods rather than a wrapper API
- **−** Quickstart needs a Stream API key; free tier is 333,000 participant minutes per month
- **−** Video understanding struggles with small text and degrades after about 30 seconds
- **−** Realtime models need audio or text to respond; video alone does not trigger output
- **−** No Docker or compose files in the repo

<sub>GPU optional · Needs Stream API key, LLM provider API (OpenAI, Gemini, etc.), uv · Models: OpenAI, Gemini, xAI, OpenRouter, Hugging Face · [Repo](https://github.com/getstream/vision-agents) · [📖 Docs ↗](https://visionagents.ai/introduction/quickstart) · [🌐 Site ↗](https://visionagents.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vision-agents/)</sub>

<a name="agent-governance-toolkit"></a>
### #&#8288;58 [agent-governance-toolkit](https://github.com/microsoft/agent-governance-toolkit) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Oct 2026</sub>

**Policy enforcement, identity and audit for AI agent tool calls.**

Intercepts agent tool calls, messages and delegations in application code and checks them against YAML, OPA or Cedar policies before they execute. Adds agent identity (SPIFFE/DID/mTLS), tamper-evident audit logs, privilege-ring sandboxing, SRE controls such as a kill switch, and an OWASP compliance CLI. SDKs exist for Python, TypeScript, .NET, Rust and Go, with adapters for LangGraph, CrewAI, AutoGen and others.

- **+** Deterministic deny at tool-call level, not prompt-level; two-line `govern()` wrapper to start
- **+** SDKs in Python, TypeScript, .NET, Rust and Go, plus Claude Code and Copilot CLI plugins
- **+** Adapters for Semantic Kernel, LangGraph, CrewAI, OpenAI Agents SDK, LlamaIndex, Haystack and others
- **+** RFC 2119 specs with conformance tests; `agt verify` checks OWASP compliance in CI
- **−** Public preview; README warns of breaking changes before GA
- **−** Python has the full stack; other language SDKs cover only core governance
- **−** Packaging is in flux: 45 packages consolidated into 5, old names deprecated or stubbed
- **−** Only governs actions routed through its hooks; unwrapped tools are not covered

<sub>no GPU · Docker + Compose · Needs Python 3.11+ (quick start), Optional Azure credentials for Azure features · Models: Model-agnostic; governs tool calls for any agent framework · [Repo](https://github.com/microsoft/agent-governance-toolkit) · [📖 Docs ↗](https://microsoft.github.io/agent-governance-toolkit) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-governance-toolkit/)</sub>

<a name="aisuite"></a>
### #&#8288;59 [aisuite](https://github.com/andrewyng/aisuite) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: weak (19) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Sep 2026</sub>

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

<a name="agent-s"></a>
### #&#8288;60 [agent-s](https://github.com/simular-ai/agent-s) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: known (40) · Freshness: active (89) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**Computer-use agent that operates desktop GUIs via screenshots, mouse and keyboard.**

Agent S takes a natural-language task, reads the screen, and completes it by clicking, typing and scrolling in ordinary desktop and web apps on macOS, Windows and Linux. It pairs a main LLM (OpenAI, Anthropic, Gemini, Open Router, vLLM, Azure) with a grounding model such as UI-TARS-1.5-7B, and ships as the gui-agents Python package with a CLI. Agent S4 is a separate package in the same repo.

- **+** Works on any GUI without per-app API integration or scripting
- **+** Runs on macOS, Windows and Linux; pip install gui-agents plus a CLI
- **+** Reports 72.60% on OSWorld using multi-rollout selection; papers are published
- **+** Main and grounding models are configurable, including vLLM and custom endpoints
- **−** Requires a separately hosted grounding model such as UI-TARS-1.5-7B
- **−** Executes generated Python on your machine; no built-in sandbox
- **−** Designed for single-monitor setups only
- **−** Recommended setup uses paid OpenAI models; hosted Sai is the production offering

<sub>GPU optional · Needs Tesseract (pytesseract), Grounding model endpoint (UI-TARS-1.5-7B), LLM API key (OpenAI, Anthropic, etc.) · Models: OpenAI, Azure OpenAI, Anthropic, Gemini, Open Router · [Repo](https://github.com/simular-ai/agent-s) · [▶️ Demo ↗](https://cloud.simular.ai/) · [🌐 Site ↗](https://www.simular.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-s/)</sub>

<a name="julep"></a>
### #&#8288;61 [julep](https://github.com/julep-ai/julep) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · Apache-2.0 · Jul 2026</sub>

**Python library for durable agent flows that compile to a frozen IR.**

Julep 3 lets you write agents in Python with a define-by-construction `@flow` decorator. Tools, pure functions, reasoners, branches, fan-out, retries and timeouts compile to a frozen wire-format IR. Flows run locally with fake reasoners via `dry_run`, or durably on Temporal or DBOS/Postgres. A `julep` CLI handles lint, run, trace, plan and deploy.

- **+** Flows can crash and resume, with retries and timeouts declared per step
- **+** Tools are allow-listed: the model cannot call a tool not registered at deploy
- **+** dry_run executes locally with fake reasoners, so no API key is needed to test
- **+** Temporal and DBOS backends are optional; the base install needs only PyYAML
- **−** Ships as a release candidate; `--pre` is required until 3.0.0 is final
- **−** No migration path from Julep v1; the two are different products
- **−** Production deploy needs Temporal, Helm, kubectl and S3, which adds operational load
- **−** No Docker or compose setup in the repo

<sub>no GPU · Needs Temporal (optional), DBOS/Postgres (optional), Kubernetes, Helm, S3 (production deploy), Langfuse (optional) · Models: Anthropic (example), multi-provider via any-llm · [Repo](https://github.com/julep-ai/julep) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/julep/)</sub>

<a name="owl"></a>
### #&#8288;62 [owl](https://github.com/camel-ai/owl) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 20k · no license · Oct 2026</sub>

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

<a name="pocketflow"></a>
### #&#8288;63 [pocketflow](https://github.com/the-pocket/pocketflow) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (35) · Freshness: active (100) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Jul 2026</sub>

**Python LLM framework built on a 100-line graph abstraction.**

Pocket Flow is a Python library whose core is a single 100-line file implementing a graph of nodes and flows. Agents, workflows, RAG, batch and map-reduce patterns are built on top of it. It ships no vendor or app-specific wrappers, so LLM calls and tools are written by the user, and a large cookbook shows the patterns.

- **+** Core is one 100-line file with zero dependencies; can be copied into a project
- **+** No vendor-specific wrappers, so no lock-in to a provider or vector store
- **+** Cookbook with about 40 runnable examples: agents, RAG, MCP, A2A, voice, parallel batch
- **+** Ports exist for TypeScript, Java, C++, Go, Rust and PHP
- **−** No built-in LLM, vector DB or tool integrations; you write each utility function
- **−** Size and line-count comparison table is the project's own, not independently verified
- **−** No tagged releases listed; installed from PyPI or by copying source
- **−** Minimal abstraction means no built-in tracing, UI or deployment tooling

<sub>no GPU · Models: any (user-written LLM calls) · [Repo](https://github.com/the-pocket/pocketflow) · [📖 Docs ↗](https://the-pocket.github.io/PocketFlow/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pocketflow/)</sub>

<a name="swarms"></a>
### #&#8288;64 [swarms](https://github.com/kyegomez/swarms) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (11) · Freshness: recent (70) · Maintenance: fair (53) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Oct 2026</sub>

**Python framework for orchestrating multi-agent workflows with MCP support.**

Swarms is a Python library for building LLM agents and combining them into multi-agent structures such as sequential, concurrent, DAG-based, hierarchical and mixture-of-agents workflows. Agents can use MCP servers via mcp_url, and MCPDeployer can serve an agent or swarm as an authenticated MCP server. The README claims 60+ multi-agent structures and a SwarmRouter that switches between them.

- **+** Prebuilt structures: Sequential, Concurrent, GraphWorkflow (DAG), Hierarchical, MixtureOfAgents, GroupChat
- **+** SwarmRouter switches swarm type through one swarm_type parameter
- **+** MCP client via mcp_url, plus MCPDeployer to serve agents as MCP servers with auth
- **+** Official Docker image for linux/amd64 and linux/arm64 on Python 3.13
- **−** Last tagged release is 2024-12-27, so the PyPI package may lag master
- **−** README examples use hosted model APIs; local model setup is not shown
- **−** Environment config lists a SWARMS_TELEMETRY_ON variable
- **−** Enterprise-grade and production-ready claims come with no benchmarks in the README

<sub>no GPU · Docker · Needs LLM provider API key (OpenAI, Anthropic or Groq), RouteHub or litellm (optional, swarms[fast]), rustworkx (optional) · Models: OpenAI, Anthropic, Groq · [Repo](https://github.com/kyegomez/swarms) · [📖 Docs ↗](https://docs.swarms.world) · [🌐 Site ↗](https://swarms.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/swarms/)</sub>

<a name="metagpt"></a>
### #&#8288;65 [metagpt](https://github.com/foundationagents/metagpt) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: widely used (95) · Freshness: quiet (23) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · MIT · Jan 2026</sub>

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

<a name="guidance"></a>
### #&#8288;66 [guidance](https://github.com/guidance-ai/guidance) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (63) · Freshness: active (80) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · May 2026</sub>

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
### #&#8288;67 [swarm](https://github.com/openai/swarm) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (65) · Freshness: recent (63) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Apr 2026</sub>

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

<a name="xagent"></a>
### #&#8288;68 [xagent](https://github.com/openbmb/xagent) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (19) · Freshness: recent (70) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.5k · Apache-2.0 · Jul 2026</sub>

**Autonomous LLM agent that plans subtasks and runs tools in a sandbox.**

XAgent is an experimental autonomous agent from OpenBMB. A Dispatcher, Planner and Actor split a task into subtasks and execute them through a Docker-based ToolServer with a file editor, Python notebook, web browser, shell and Rapid API calls. It runs from a CLI (run.py) or a web UI on port 5173, and is configured for OpenAI GPT-4 models.

- **+** Tool actions run inside a Docker ToolServer container, separate from the host
- **+** Runs are recorded and replayable via record_dir; API keys are stripped from records
- **+** Can ask the user for help mid-task through an AskForHumanHelp tool
- **+** Includes a web UI and a CLI; new tools can be added to ToolServer
- **−** README configures OpenAI keys only; no local model support documented
- **−** Last release is 2023-11-22; README calls the project early-stage and experimental
- **−** Web UI ships with default credentials guest / xagent
- **−** Needs Docker plus a separate Python 3.10+ environment for the agent

<sub>no GPU · Docker + Compose · Needs Docker, docker-compose, OpenAI API key, Python 3.10+ · Models: gpt-4-32k, gpt-4, gpt-3.5-turbo-16k (backup) · port 5173 · [Repo](https://github.com/openbmb/xagent) · [▶️ Demo ↗](https://www.x-agent.net/) · [📖 Docs ↗](https://xagent-doc.readthedocs.io/en/latest/) · [🌐 Site ↗](https://www.x-agent.net/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xagent/)</sub>

<a name="upsonic"></a>
### #&#8288;69 [upsonic](https://github.com/upsonic/upsonic) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (16) · Freshness: active (91) · Maintenance: weak (8) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · MIT · Jun 2026</sub>

**Python framework for building autonomous and tool-calling AI agents.**

Upsonic is a Python library with two agent types: an AutonomousAgent that works inside a restricted workspace directory (file and shell operations confined, path traversal and dangerous commands blocked), and a traditional Agent with custom tools via a @tool decorator and MCP support. It also ships a layered OCR pipeline supporting EasyOCR, RapidOCR, Tesseract, PaddleOCR and DeepSeek OCR.

- **+** Autonomous agent confines file and shell operations to a configured workspace
- **+** Plain Python tools via @tool decorator, plus MCP tool integration
- **+** Built-in OCR with six engines, including local ones like Tesseract and EasyOCR
- **+** Community-contributed prebuilt agents bundle a skill, system prompt and first message
- **−** README examples only show Anthropic model strings; other provider support is not listed
- **−** Isolated cloud execution needs an external sandbox provider (E2B)
- **−** No hardware requirements or deployment guidance in the README
- **−** Workspace restriction is described briefly; no detail on how dangerous commands are detected

<sub>Needs E2B (optional sandbox), LLM provider API (e.g. Anthropic) · Models: anthropic/claude-sonnet-4-5, DeepSeek OCR via Ollama · [Repo](https://github.com/upsonic/upsonic) · [📖 Docs ↗](https://docs.upsonic.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/upsonic/)</sub>

<a name="mobileagent"></a>
### #&#8288;70 [mobileagent](https://github.com/x-plug/mobileagent) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (24) · Freshness: active (93) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · MIT · Jul 2026</sub>

**GUI agent models and multi-agent code for operating phones, PCs and browsers.**

Research repository from Tongyi Lab (Alibaba) collecting the Mobile-Agent series, from v1 to v3.5, plus related work such as PC-Agent, UI-S1 and GUI-Critic-R1. It centers on the GUI-Owl vision-language models (2B to 235B, Instruct and Thinking, built on Qwen3-VL) and multi-agent frameworks that plan, reflect and keep memory while driving mobile, desktop and web interfaces. The README mostly links out to per-project subfolders, papers and hosted demos.

- **+** Open GUI-Owl weights in several sizes (2B/4B/8B/32B/235B) on Hugging Face and ModelScope
- **+** Covers mobile, desktop and browser targets, with evaluation code for OSWorld and AndroidWorld
- **+** Each generation (v1 to v3.5, UI-S1, PC-Agent) has its own paper and code folder
- **+** MIT license; hosted demos and a Bailian API exist for trying it without local setup
- **−** Top-level README has no install or quick-start steps; setup lives in subfolders
- **−** Hosted demos and API depend on Alibaba Cloud services, with docs largely in Chinese
- **−** Larger models (32B, 235B) need substantial GPU memory; requirements are not stated
- **−** No tagged releases; the repo is a collection of separate research projects

<sub>Needs Android device or emulator (mobile use), Alibaba Cloud Bailian API (optional hosted inference) · Models: GUI-Owl-1.5 (2B/4B/8B/32B/235B), GUI-Owl-7B, GUI-Owl-32B, UI-S1-7B · [Repo](https://github.com/x-plug/mobileagent) · [▶️ Demo ↗](http://modelscope.cn/studios/MobileAgentTest/computer_use) · [📖 Docs ↗](https://github.com/X-PLUG/MobileAgent/tree/main/Mobile-Agent-v3.5) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mobileagent/)</sub>

<a name="pandas-ai"></a>
### #&#8288;71 [pandas-ai](https://github.com/sinaptik-ai/pandas-ai) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: popular (68) · Freshness: quiet (15) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Oct 2025</sub>

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
### #&#8288;72 [qwen-agent](https://github.com/qwenlm/qwen-agent) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: popular (54) · Freshness: slowing (36) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Mar 2026</sub>

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
### #&#8288;73 [rasa](https://github.com/rasahq/rasa) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: popular (62) · Freshness: quiet (14) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Dec 2025</sub>

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

<a name="openbrowser"></a>
### #&#8288;74 [openbrowser](https://github.com/ntegrals/openbrowser) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: niche (26) · Freshness: recent (57) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · MIT · Mar 2026</sub>

**TypeScript library and CLI that lets an LLM drive a Playwright browser.**

Open Browser is a Bun/TypeScript monorepo where an agent sends page state to an LLM, which picks commands (click, type, scroll, extract, navigate) that run in a Playwright browser. It ships a core library, a CLI with an interactive REPL, and a sandbox package with timeout, memory and domain limits. OpenAI, Anthropic and Google models are supported through the Vercel AI SDK.

- **+** Library, CLI and interactive REPL share one codebase, with 25+ browser commands
- **+** Switches between OpenAI, Anthropic and Google models with a provider flag
- **+** Sandbox package sets timeout, memory limit, allowed domains and step limit
- **+** Includes stall detection, cost tracking and trace/recording output paths
- **−** Requires a third-party LLM API key; no local model provider is listed
- **−** No tagged release and no Docker setup; install is from source with Bun
- **−** README gives no benchmarks or task success rates
- **−** Step limit defaults conflict: CLI says 25, agent settings table says 100

<sub>no GPU · Needs Bun, Playwright, OpenAI, Anthropic or Google API key · Models: OpenAI, Anthropic, Google · [Repo](https://github.com/ntegrals/openbrowser) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openbrowser/)</sub>

<a name="ai-scientist"></a>
### #&#8288;75 [ai-scientist](https://github.com/sakanaai/ai-scientist) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: known (48) · Freshness: quiet (21) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · Dec 2025</sub>

**Pipeline where LLMs propose ideas, run experiments and write LaTeX papers.**

Runs an end-to-end loop in which an LLM generates research ideas, checks novelty via Semantic Scholar or OpenAlex, edits and runs experiment code, and writes a LaTeX paper. It also includes an LLM-based paper reviewer. Three templates ship (NanoGPT, 2D diffusion, grokking), plus community-contributed ones.

- **+** Covers idea generation, experiments, paper write-up and automated review in one pipeline
- **+** Supports OpenAI, Anthropic (including Bedrock and Vertex), DeepSeek, OpenRouter and Gemini
- **+** README cites typical cost under $15 per paper with Claude Sonnet 3.5
- **+** Custom templates follow a documented file layout (experiment.py, plot.py, prompt.json)
- **−** Executes LLM-written code; README says to containerize and restrict web access yourself
- **−** Needs Linux, NVIDIA GPU with CUDA and a full texlive install; CPU-only is impractical
- **−** Ideas limited to those expressible in code; only three templates are maintained
- **−** Custom license requires disclosing AI use in resulting manuscripts

<sub>GPU required · Needs PyTorch, CUDA, texlive-full, conda, Semantic Scholar API (optional), OpenAlex (optional) · Models: OpenAI GPT-4o, OpenAI o1, Claude Sonnet 3.5, DeepSeek, Llama 3.1 via OpenRouter · [Repo](https://github.com/sakanaai/ai-scientist) · [🌐 Site ↗](https://sakana.ai/ai-scientist/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-scientist/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
