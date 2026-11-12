# 🧰 Agent frameworks and SDKs reviews · Best of Open-Source AI

Libraries for building agents and LLM apps in code: tool calling, planning, multi-agent setups and browser control. Back to the [leaderboard](../README.md#-agent-frameworks-and-sdks).

<sub>🌐 Also on the web: [Agent frameworks and SDKs on archestack.com](https://archestack.com/best-of-ai/agent-frameworks/), each project on its own page.</sub>

<a name="ppt-master"></a>
### 🥇 [ppt-master](https://github.com/hugohe3/ppt-master) <sub>score [96](../README.md#-how-we-rank "Score 96/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 76k · MIT · Nov 2026</sub>

**Agent skill that turns documents into natively editable PowerPoint decks.**

PPT Master is a workflow ("skill") that runs inside an agent-capable AI tool such as Claude Code, Cursor or Codex CLI. Given a PDF, DOCX, web page or topic, it plans the argument and exports a .pptx with native shapes, data-backed charts, tables and slide masters rather than images. It can also fill an existing .pptx, extract templates from references, and add transitions, animations and narration.

- **+** Exports native PowerPoint objects: shapes, charts, tables and slide masters stay editable
- **+** Runs locally; only model, search, image and speech calls leave the machine
- **+** Works with any agent-capable tool and models like Claude, GPT, Gemini and Kimi
- **+** Also fills existing .pptx files and adds transitions, animations and narration
- **−** Output quality depends on the driving model; cheaper models need more manual polish
- **−** Needs a separate agent tool and model access; it is not a standalone app
- **−** SmartArt is deliberately unsupported
- **−** Recommended setup (~1M-token context model plus image generation API) adds usage cost

<sub>no GPU · Needs Python 3.10+, agent-capable AI tool (Claude Code, Cursor, Codex CLI, etc.), pandoc (only for legacy formats like .doc, .rtf), image generation API (optional) · Models: Kimi K3, Claude, GPT, Gemini, gpt-image-2 · [Repo](https://github.com/hugohe3/ppt-master) · [▶️ Demo ↗](https://hugohe3.github.io/ppt-master-examples/) · [📖 Docs ↗](https://github.com/hugohe3/ppt-master/blob/main/docs/getting-started.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ppt-master/)</sub>

<a name="openai-agents-python"></a>
### 🥈 [openai-agents-python](https://github.com/openai/openai-agents-python) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Nov 2026</sub>

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
### 🥉 [mastra](https://github.com/mastra-ai/mastra) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · custom license · Nov 2026</sub>

**TypeScript framework for building AI agents, workflows and MCP servers.**

Mastra is a TypeScript framework for building agents and graph-based workflows, with model routing across 40+ providers. It adds suspend/resume with stored state, memory, RAG, evals and observability, and runs inside React, Next.js or Node apps or as a standalone server. A local Studio on port 4111 is used to build and test agents, workflows and tools.

- **+** Graph workflow engine with .then(), .branch() and .parallel() control flow
- **+** Suspend and resume agents or workflows, with execution state kept in storage
- **+** Built-in evals, observability, memory and RAG alongside agents
- **+** Can author MCP servers exposing agents and tools
- **−** TypeScript only; no other language SDKs mentioned
- **−** Code in ee/ directories needs an enterprise license for production use
- **−** Pull requests limited to collaborators
- **−** No Docker or compose files in the repo

<sub>no GPU · Needs Node.js, LLM provider API key · Models: OpenAI, Anthropic, Gemini, xAI, 40+ providers via model router · port 4111 · [Repo](https://github.com/mastra-ai/mastra) · [📖 Docs ↗](https://mastra.ai/docs) · [🌐 Site ↗](https://mastra.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mastra/)</sub>

<a name="browser-use"></a>
### #&#8288;4 [browser-use](https://github.com/browser-use/browser-use) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 121k · MIT · Nov 2026</sub>

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
### #&#8288;5 [copilotkit](https://github.com/copilotkit/copilotkit) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · MIT · Nov 2026</sub>

**React and Angular SDK for adding agent chat and generative UI to apps.**

CopilotKit is a TypeScript SDK and runtime that connects an existing agent (LangGraph, CrewAI, Mastra, Google ADK, PydanticAI and others) to a frontend over the AG-UI protocol. It provides chat components, generative UI, shared agent/UI state, human-in-the-loop approvals and frontend tools for React, Angular, Vue, React Native, Slack and Teams. A separate Intelligence layer adds memory, thread persistence and Continual Learning.

- **+** Works with many agent backends: LangGraph, CrewAI, Mastra, Google ADK, PydanticAI, Strands, LlamaIndex
- **+** Covers React, Angular, Vue, React Native, plus Slack and Teams channels
- **+** Three generative UI modes: registered components, A2UI specs, sandboxed MCP Apps
- **+** Hooks such as useAgent give programmatic control beneath the prebuilt chat components
- **−** Memory, persistent threads and Continual Learning sit in Intelligence, not the MIT SDK
- **−** Slack and Teams are GA only on cloud-hosted Intelligence
- **−** Needs a separately built agent or the built-in agent plus an LLM API key
- **−** Angular, Vue and React Native are listed as supported, while React/Next.js is the GA surface

<sub>no GPU · Needs Node.js/npm, LLM provider API key (e.g. OpenAI) · Models: OpenAI (built-in agent), LangGraph, CrewAI, Mastra, Google ADK · [Repo](https://github.com/copilotkit/copilotkit) · [📖 Docs ↗](https://docs.copilotkit.ai) · [🌐 Site ↗](https://www.copilotkit.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/copilotkit/)</sub>

<a name="tradingagents"></a>
### #&#8288;6 [tradingagents](https://github.com/tauricresearch/tradingagents) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 122k · Apache-2.0 · Nov 2026</sub>

**Multi-agent LLM framework that simulates a trading firm's analysis process.**

TradingAgents is a LangGraph-based Python framework in which LLM agents act as analysts, bull and bear researchers, trader, risk team and portfolio manager to produce a trading decision for a ticker and date. It runs from an interactive or flag-driven CLI or from Python via TradingAgentsGraph.propagate(), and saves reports including one HTML page. It is described as research software, not financial advice.

- **+** Many providers: OpenAI, Anthropic, Google, DeepSeek, Qwen, Bedrock, Azure, Ollama, OpenAI-compatible
- **+** Past-dated runs read SEC EDGAR statements as filed, which avoids look-ahead in backtests
- **+** Separate provider and model for quick-think and deep-think tiers
- **+** Non-interactive CLI flags and TRADINGAGENTS_* env vars suit scheduled jobs
- **−** Approved orders go only to a simulated exchange; no live broker execution is described
- **−** Research use only; results vary with model, temperature and data quality
- **−** Non-US fundamentals come from Yahoo Finance and are withheld for past-dated runs
- **−** Needs an LLM API key or ChatGPT plan unless run on local models

<sub>GPU optional · Docker + Compose · Needs LLM provider API key or Ollama, Yahoo Finance, SEC EDGAR, FRED (optional), Alpha Vantage (optional) · Models: OpenAI, Anthropic, Google Gemini, xAI Grok, DeepSeek · [Repo](https://github.com/tauricresearch/tradingagents) · [▶️ Demo ↗](https://www.youtube.com/watch?v=90gr5lwjIho) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tradingagents/)</sub>

<a name="gradio"></a>
### #&#8288;7 [gradio](https://github.com/gradio-app/gradio) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 44k · Apache-2.0 · Nov 2026</sub>

**Python library for building web UIs around ML models and functions.**

Gradio wraps any Python function in a browser UI using Interface, Blocks for custom layouts, or ChatInterface for chatbots, with more than 30 built-in components. It can create a temporary public gradio.live URL via share=True while computation stays on the local machine. Python and JavaScript clients can query running apps programmatically.

- **+** Few lines of Python give a working UI; no JavaScript or CSS needed
- **+** share=True creates a public gradio.live link while compute stays local
- **+** Python and JavaScript clients can call any Gradio app programmatically
- **+** Hot reload mode via `gradio app.py` speeds up iteration
- **−** Blocks layouts are limited to Gradio's component set unless you write custom components
- **−** Not a hosted chat product; no user accounts or chat history described
- **−** Requires Python 3.10 or higher
- **−** Shared links depend on Gradio's relay service rather than your own hosting

<sub>no GPU · Needs Python 3.10+ · Models: any Python function, Hugging Face models · port 7860 · [Repo](https://github.com/gradio-app/gradio) · [📖 Docs ↗](https://gradio.app/docs/) · [🌐 Site ↗](https://gradio.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gradio/)</sub>

<a name="haystack"></a>
### #&#8288;8 [haystack](https://github.com/deepset-ai/haystack) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · Apache-2.0 · Nov 2026</sub>

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

<a name="langchain"></a>
### #&#8288;9 [langchain](https://github.com/langchain-ai/langchain) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 149k · MIT · Nov 2026</sub>

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

<a name="agent-browser"></a>
### #&#8288;10 [agent-browser](https://github.com/vercel-labs/agent-browser) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · Apache-2.0 · Nov 2026</sub>

**Native Rust CLI that lets AI agents drive a browser via accessibility snapshots.**

agent-browser is a Rust CLI that controls Chrome over the DevTools Protocol through a background daemon. `snapshot` returns the page as compact text with refs like `@e1`, and the agent clicks or fills those refs one shell command at a time. It also ships version-matched skills for agent harnesses and an MCP server over stdio.

- **+** Compact ref-based accessibility snapshots keep each agent step to one short shell call
- **+** Clicks fail explicitly when the target is hidden, disabled, or covered by a banner
- **+** Attaches to running Chrome, Lightpanda, Obscura, iOS Simulator, or cloud providers like Browserbase
- **+** Native binaries for macOS, Linux (glibc and musl) and Windows; also exposes an MCP server
- **−** Refs go stale after navigation or DOM changes, so agents must re-snapshot
- **−** Default setup downloads Chrome for Testing; Linux needs extra system libraries
- **−** Headless daemon exits after one hour idle by default, unless session persistence is configured
- **−** Command-line only; no Python or in-process library API is described

<sub>no GPU · Docker + Compose · Needs Chrome for Testing, Node.js (npm install) · [Repo](https://github.com/vercel-labs/agent-browser) · [📖 Docs ↗](https://agent-browser.dev) · [🌐 Site ↗](https://agent-browser.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-browser/)</sub>

<a name="agno"></a>
### #&#8288;11 [agno](https://github.com/agno-agi/agno) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Nov 2026</sub>

**Python SDK and runtime for building and serving agents and workflows.**

Agno is a Python framework for building agents, teams and workflows, plus AgentOS, a runtime that serves them as a REST API and MCP server. AgentOS adds authentication, role-based access, scheduling, human approvals, tracing and durable background execution, using PostgreSQL storage in the starter templates. Company OS organizes work into projects, tasks and recurring routines.

- **+** Serves agents over REST API and MCP, with Slack and other chat interfaces
- **+** Built-in durable execution, scheduling, human approval and resume/replay
- **+** Deployment templates for Docker, AWS, GCP, Azure, Railway, Fly.io, Render, Modal, Helm
- **+** Role-based access and per-user data isolation in the runtime
- **−** Management UI is the hosted os.agno.com, not a bundled self-hosted frontend
- **−** Sends a telemetry event per agent unless AGNO_TELEMETRY=false is set
- **−** Setup runs through external templates and coding-agent prompts, not this repo alone
- **−** Company OS and AgentOS add concepts beyond a plain agent SDK

<sub>Needs PostgreSQL · Models: Agno SDK, Claude Agent SDK, Codex SDK · [Repo](https://github.com/agno-agi/agno) · [📖 Docs ↗](https://docs.agno.com) · [🌐 Site ↗](https://agno.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agno/)</sub>

<a name="openai-python"></a>
### #&#8288;12 [openai-python](https://github.com/openai/openai-python) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Nov 2026</sub>

**Official Python client for the OpenAI REST API, sync and async.**

Typed Python 3.10+ SDK for the OpenAI API, generated from the OpenAPI spec. It covers the Responses and Chat Completions APIs, streaming, Realtime over WebSocket, file uploads, pagination, webhook verification and workload identity auth. Sync and async clients run on HTTPX2, with an optional aiohttp transport.

- **+** Type definitions for all request params; responses are Pydantic models
- **+** Sync and async clients with identical interfaces, plus optional aiohttp transport
- **+** Workload identity auth for Kubernetes, Azure, GCP and X.509 mTLS instead of static keys
- **+** Auto-paginating iterators and built-in webhook signature verification
- **−** Client for OpenAI's hosted API; it does not run or serve models locally
- **−** Requires an OpenAI API key or workload identity credentials
- **−** Custom HTTP clients need migration to HTTPX2 per the migration guide
- **−** X.509 workload identity supports HTTP only, not Realtime or WebSockets

<sub>no GPU · Needs OpenAI API, HTTPX2, websockets (Realtime), aiohttp (optional) · Models: OpenAI hosted models via Responses API, Chat Completions API, Realtime API · [Repo](https://github.com/openai/openai-python) · [📖 Docs ↗](https://platform.openai.com/docs/api-reference) · [🌐 Site ↗](https://platform.openai.com/docs/api-reference) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openai-python/)</sub>

<a name="ai"></a>
### #&#8288;13 [ai](https://github.com/vercel/ai) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · custom license · Nov 2026</sub>

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

<a name="crewai"></a>
### #&#8288;14 [crewai](https://github.com/crewaiinc/crewai) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 61k · MIT · Nov 2026</sub>

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

<a name="langgraph"></a>
### #&#8288;15 [langgraph](https://github.com/langchain-ai/langgraph) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 45k · MIT · Nov 2026</sub>

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
### #&#8288;16 [deepagents](https://github.com/langchain-ai/deepagents) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Nov 2026</sub>

**Python agent harness on LangGraph with sub-agents, filesystem and context management.**

Deep Agents is a Python library whose create_deep_agent() call returns a preconfigured LangGraph agent for long, multi-step tasks. It bundles planning, sub-agents with isolated context, a pluggable filesystem backend, shell access, context summarization, skills, human-in-the-loop approval and MCP tool support. It works with any tool-calling LangChain chat model, including Ollama, vLLM and llama.cpp.

- **+** Sub-agents run with isolated context windows; any LangGraph CompiledStateGraph can be a sub-agent
- **+** Works with any tool-calling LangChain chat model, including Ollama, vLLM and llama.cpp
- **+** Filesystem and memory backends are pluggable: local, sandboxed or remote
- **+** Human approval can gate tool calls; tools can be custom functions or MCP servers
- **−** Follows a trust-the-LLM model; boundaries must be enforced in tools or sandbox
- **−** Tracing, evaluation and deployment integrations point to LangSmith, a separate product
- **−** Built on the LangChain and LangGraph stack; no standalone runtime or UI
- **−** Python only here; the JavaScript version is a separate repository

<sub>GPU optional · Needs LangGraph, LangChain, LLM provider or local model server, LangSmith (optional) · Models: OpenAI, Anthropic, Google, Baseten, Fireworks · [Repo](https://github.com/langchain-ai/deepagents) · [📖 Docs ↗](https://docs.langchain.com/oss/python/deepagents/overview) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepagents/)</sub>

<a name="pydantic-ai"></a>
### #&#8288;17 [pydantic-ai](https://github.com/pydantic/pydantic-ai) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · MIT · Nov 2026</sub>

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

<a name="pipecat"></a>
### #&#8288;18 [pipecat](https://github.com/pipecat-ai/pipecat) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · BSD-2-Clause · Nov 2026</sub>

**Python framework for real-time voice and multimodal agent pipelines.**

Pipecat is a Python framework that chains speech-to-text, LLM, text-to-speech and speech-to-speech services into streaming pipelines, with WebSocket and WebRTC transports. It also supports multi-agent setups with handoff, parallel fan-out and a shared bus, locally or distributed. A CLI scaffolds and deploys projects, and client SDKs cover JavaScript, React, Swift, Kotlin, C++ and ESP32.

- **+** Many pluggable services: 23 STT, 25 LLM and 30+ TTS providers listed, including local Whisper and Ollama
- **+** Official client SDKs for JS, React, React Native, Swift, Kotlin, C++ and ESP32
- **+** Structured conversation flows (Pipecat Flows) built in, plus Whisker debugger and Tail dashboard
- **+** Multi-agent support: handoff, parallel fan-out and distributed deployment over a shared bus
- **−** Library, not a ready app: you write Python pipeline code to get a working bot
- **−** Most listed STT, LLM and TTS services are hosted APIs needing separate keys
- **−** No Docker or compose files detected in the repo

<sub>GPU optional · Needs Python, STT/LLM/TTS provider API keys (e.g. Deepgram, OpenAI, Cartesia, ElevenLabs), WebRTC/WebSocket transport · Models: Whisper, Moonshine, Ollama, OpenAI, Anthropic · [Repo](https://github.com/pipecat-ai/pipecat) · [📖 Docs ↗](https://docs.pipecat.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pipecat/)</sub>

<a name="adk-python"></a>
### #&#8288;19 [adk-python](https://github.com/google/adk-python) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Nov 2026</sub>

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

<a name="eliza"></a>
### #&#8288;20 [eliza](https://github.com/elizaos/eliza) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Nov 2026</sub>

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

<a name="parlant"></a>
### #&#8288;21 [parlant](https://github.com/emcie-co/parlant) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Nov 2026</sub>

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

<a name="nanobrowser"></a>
### #&#8288;22 [nanobrowser](https://github.com/nanobrowser/nanobrowser) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

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

<a name="agentscope"></a>
### #&#8288;23 [agentscope](https://github.com/agentscope-ai/agentscope) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;24 [page-agent](https://github.com/alibaba/page-agent) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Sep 2026</sub>

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

<a name="ego-lite"></a>
### #&#8288;25 [ego-lite](https://github.com/citrolabs/ego-lite) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · MIT · Nov 2026</sub>

**Desktop browser that AI agents drive through isolated per-agent Spaces.**

ego lite is a Chromium-based desktop browser for macOS and Windows that gives each AI agent its own isolated Space, so agents work in the background while you keep browsing. Agents such as Claude Code, Codex or Cursor connect through the `ego-browser` skill, which exposes snapshot, fill, click, wait, navigate and capture as in-page JavaScript functions. The repository holds the MIT-licensed skill and docs; the browser itself is a separate free download.

- **+** Per-agent Spaces let several agents run in parallel without taking over your tabs
- **+** Agent writes one JavaScript snippet per multi-step task, not a command-by-command loop
- **+** Optional Chrome data migration gives agents your existing logins, cookies and extensions
- **+** Works with any agent CLI that supports skills, installable via npx skills add
- **−** Runs on macOS and Windows only; Linux is just on the roadmap
- **−** Browser binary is a separate download, not built from this MIT repository
- **−** Benchmark of 31 tasks is self-run by the authors against four other tools
- **−** Experience-accumulation reusable skills feature is marked coming soon

<sub>Needs Agent CLI (Claude Code, Codex, Cursor or custom), ego lite desktop browser app · Models: Model-agnostic; depends on the agent CLI · [Repo](https://github.com/citrolabs/ego-lite) · [📖 Docs ↗](https://lite.ego.app/document/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ego-lite/)</sub>

<a name="instructor"></a>
### #&#8288;26 [instructor](https://github.com/567-labs/instructor) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Nov 2026</sub>

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

<a name="dspy"></a>
### #&#8288;27 [dspy](https://github.com/stanfordnlp/dspy) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · MIT · Nov 2026</sub>

**Python framework for building LM programs and optimizing their prompts and weights.**

DSPy lets you write LM pipelines as modular Python code instead of hand-written prompts. It includes optimizers that tune prompts and weights against a metric, covering use cases from classifiers to RAG pipelines and agent loops. LM access goes through bundled native lm15 engines, with no LiteLLM dependency.

- **+** Optimizers tune prompts and weights from code and metrics, replacing manual prompt editing
- **+** Compositional Python modules for classifiers, RAG pipelines and agent loops
- **+** Backed by published papers, including GEPA and MIPRO
- **+** Installs with a single pip command, MIT licensed
- **−** README defers nearly all usage detail to the external docs site
- **−** LM layer moved off LiteLLM to lm15, with breaking changes to provider options
- **−** Custom LMs, text completions and embeddings need migration per the guide
- **−** Declarative module and optimizer model has a learning curve versus plain prompting

<sub>Needs Python, lm15 (bundled) · Models: provider LMs via bundled lm15 engines · [Repo](https://github.com/stanfordnlp/dspy) · [📖 Docs ↗](https://dspy.ai) · [🌐 Site ↗](https://dspy.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dspy/)</sub>

<a name="ag-ui"></a>
### #&#8288;28 [ag-ui](https://github.com/ag-ui-protocol/ag-ui) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Nov 2026</sub>

**Event-based protocol connecting agent backends to user-facing apps.**

AG-UI defines about 16 standard event types that agent backends emit during a run, plus a simple input format, so front-ends can render streaming chat, shared state, generative UI and frontend tool calls. It works over any transport (SSE, WebSockets, webhooks) and ships a reference HTTP implementation and a default connector. Integrations cover LangGraph, CrewAI, Microsoft Agent Framework, Google ADK, Mastra, Pydantic AI and others.

- **+** Transport-agnostic: SSE, WebSockets or webhooks, with loose event format matching
- **+** Many framework integrations: LangGraph, CrewAI, Google ADK, Mastra, Pydantic AI, Agno
- **+** Community SDKs for Kotlin, Go, Dart, Java, Rust, Ruby, C++ and .NET
- **+** Dojo viewer shows each building block in 50-200 lines of code
- **−** A protocol, not an agent runtime; you still need an agent framework and a UI client
- **−** OpenAI Agents SDK, AWS Bedrock Agents, Nim, Flowise and Langflow integrations are still in progress
- **−** Docs and many integrations are hosted under CopilotKit, tying the ecosystem to one vendor
- **−** Non-TypeScript SDKs are listed as community-maintained

<sub>no GPU · Needs Node.js (npx create-ag-ui-app), An agent framework or backend · [Repo](https://github.com/ag-ui-protocol/ag-ui) · [▶️ Demo ↗](https://dojo.ag-ui.com/) · [📖 Docs ↗](https://docs.ag-ui.com/) · [🌐 Site ↗](https://ag-ui.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ag-ui/)</sub>

<a name="llama-index"></a>
### #&#8288;29 [llama_index](https://github.com/run-llama/llama_index) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · MIT · Nov 2026</sub>

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

<a name="semantic-kernel"></a>
### #&#8288;30 [semantic-kernel](https://github.com/microsoft/semantic-kernel) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Nov 2026</sub>

**Model-agnostic SDK for building agents and plugins in C#, Python and Java.**

Semantic Kernel is a Microsoft SDK for building LLM agents and multi-agent systems in Python, .NET and Java. It provides chat-completion agents, plugins (native functions, prompt templates, OpenAPI, MCP), vector store connectors and a process framework for workflows. The README states it has been succeeded by Microsoft Agent Framework 1.0 and links a migration guide.

- **+** Same agent and plugin model across Python, .NET and Java
- **+** Connectors for OpenAI, Azure OpenAI, Hugging Face, NVIDIA, Ollama, LMStudio and ONNX
- **+** Plugins from native code, prompt templates, OpenAPI specs or MCP
- **+** Vector store integrations include Azure AI Search, Elasticsearch and Chroma
- **−** README says Microsoft Agent Framework is the successor, so new work points elsewhere
- **−** Java support lives in a separate repository with its own build steps
- **−** Examples use Azure OpenAI and OpenAI; local model setup is not shown
- **−** Requires .NET 10+ or Python 3.11 to 3.14, which excludes older runtimes

<sub>no GPU · Needs OpenAI or Azure OpenAI API key, or a local model runtime · Models: OpenAI, Azure OpenAI, Hugging Face, NVIDIA, Ollama · [Repo](https://github.com/microsoft/semantic-kernel) · [📖 Docs ↗](https://learn.microsoft.com/en-us/semantic-kernel/get-started/quick-start-guide) · [🌐 Site ↗](https://aka.ms/sk/learn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/semantic-kernel/)</sub>

<a name="stagehand"></a>
### #&#8288;31 [stagehand](https://github.com/browserbase/stagehand) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · MIT · Nov 2026</sub>

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

<a name="agent-desktop"></a>
### #&#8288;32 [agent-desktop](https://github.com/vercel-labs/agent-desktop) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · Apache-2.0 · Nov 2026</sub>

**Desktop app control for AI agents via the OS accessibility tree.**

agent-desktop is a Rust CLI and C library that reads a desktop app's accessibility tree (AX API on macOS, UI Automation on Windows, AT-SPI on Linux) and returns it as JSON with a ref per actionable element. The calling agent clicks or types on refs and re-reads the UI to verify; no model is bundled. It also serves its commands as MCP tools over stdio.

- **+** Uses accessibility tree refs instead of screenshots or pixel matching
- **+** Runs on macOS 13+, Windows 10 1809+, and Ubuntu 24.04+
- **+** Ref actions are headless by default, without moving the pointer or taking focus
- **+** Ships a CLI, a C library, and an MCP server (agent-desktop mcp)
- **−** No model or agent loop included; you must supply and drive the agent
- **−** Refs go stale when the UI changes, so snapshots must be retaken
- **−** Four commands (key-down, key-up, mouse-down, mouse-up) refuse to run without a daemon
- **−** Linux support is documented only for Ubuntu 24.04 or later

<sub>no GPU · Needs OS accessibility permissions · [Repo](https://github.com/vercel-labs/agent-desktop) · [📖 Docs ↗](https://agent-browser.dev/desktop) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-desktop/)</sub>

<a name="camofox-browser"></a>
### #&#8288;33 [camofox-browser](https://github.com/jo-inc/camofox-browser) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Nov 2026</sub>

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

<a name="sandcastle"></a>
### #&#8288;34 [sandcastle](https://github.com/mattpocock/sandcastle) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · MIT · Nov 2026</sub>

**TypeScript library that runs coding agents in isolated sandboxes on git branches.**

Sandcastle is a TypeScript library where a single `sandcastle.run()` call starts an AI coding agent inside a sandbox, works on a configurable branch strategy, and merges the resulting commits back. Sandbox providers include Bubblewrap (Linux, WSL2), Seatbelt (macOS), Docker, Podman, and cloud options (Daytona, E2B, Fly.io Sprites, Modal, Vercel), plus custom ones.

- **+** Native OS sandboxes (Bubblewrap, Seatbelt) need no container runtime
- **+** Many providers: Docker, Podman, Daytona, E2B, Fly.io Sprites, Modal, Vercel
- **+** Branch strategies and merge-back suit parallel agents and review pipelines
- **+** Custom sandbox providers can be written; hooks and structured output are documented
- **−** Library only: no UI, you write TypeScript to orchestrate runs
- **−** Cloud providers require accounts with third-party services
- **−** No Windows-native sandbox listed; Windows users need WSL2

<sub>no GPU · Needs Node.js, Bubblewrap (Linux/WSL2), Docker or Podman (optional), Daytona, E2B, Fly.io Sprites, Modal or Vercel (optional) · [Repo](https://github.com/mattpocock/sandcastle) · [📖 Docs ↗](https://www.aihero.dev/sandcastle) · [🌐 Site ↗](https://www.aihero.dev/sandcastle) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sandcastle/)</sub>

<a name="langchainjs"></a>
### #&#8288;35 [langchainjs](https://github.com/langchain-ai/langchainjs) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Nov 2026</sub>

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

<a name="runanywhere-sdks"></a>
### #&#8288;36 [runanywhere-sdks](https://github.com/runanywhereai/runanywhere-sdks) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · custom license · Nov 2026</sub>

**On-device LLM, speech, vision and RAG SDKs for mobile, web and desktop.**

Eight SDKs (Swift, Kotlin, Flutter, React Native, Web, Electron, Python, and the wally CLI) over one C++ core. A capability registry picks an engine per device: QHexRT on Snapdragon Hexagon NPU, MLX on Apple silicon, llama.cpp, sherpa + ONNX, or Core ML. It covers LLM chat, VLM, STT, TTS, voice agents, embeddings, RAG and image generation, all run locally.

- **+** One API across Swift, Kotlin, Flutter, React Native, Web, Electron and Python
- **+** Engine routing per device: Hexagon NPU, MLX, llama.cpp (Metal, CUDA opt-in, WebGPU)
- **+** Covers LLM, VLM, STT, TTS, VAD, embeddings, RAG, structured output and tool calling
- **+** wally CLI serves an OpenAI-compatible API on :8080
- **−** Maturity varies: Flutter, React Native and Web are beta, Electron preview, Python alpha
- **−** Python SDK has stubs for voice agent, image generation and LoRA
- **−** Wake-word detection is not implemented in any SDK
- **−** Custom license (NOASSERTION detected); terms need review before commercial use

<sub>GPU optional · Models: GGUF, safetensors (MLX), ONNX, Core ML · port 8080 · [Repo](https://github.com/runanywhereai/runanywhere-sdks) · [📖 Docs ↗](https://docs.runanywhere.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/runanywhere-sdks/)</sub>

<a name="adk-go"></a>
### #&#8288;37 [adk-go](https://github.com/google/adk-go) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · Apache-2.0 · Nov 2026</sub>

**Code-first Go toolkit for building and orchestrating multi-agent applications.**

ADK Go is Google's Agent Development Kit for Go, installed as the module google.golang.org/adk/v2. Agent logic, tools and multi-agent composition are defined directly in Go code. It is optimized for Gemini but described as model-agnostic and deployment-agnostic, with containerized deployment aimed at Google Cloud Run.

- **+** Agents, tools and orchestration are plain Go, so they can be tested and versioned like other code
- **+** Composes multiple specialized agents into larger systems
- **+** Sibling ADKs exist for Python, Java, Kotlin and TypeScript
- **+** Apache-2.0 licensed, with recent commits and a release in October 2026
- **−** README names no model providers besides Gemini optimization
- **−** Requires a very recent Go toolchain (1.26.10 or later)
- **−** README has no code example or quickstart, only links to docs and samples
- **−** Deployment guidance in the README centers on Google Cloud Run

<sub>Needs Go 1.26.10+ · Models: Gemini · [Repo](https://github.com/google/adk-go) · [📖 Docs ↗](https://google.github.io/adk-docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/adk-go/)</sub>

<a name="harness-sdk"></a>
### #&#8288;38 [harness-sdk](https://github.com/strands-agents/harness-sdk) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Nov 2026</sub>

**Python and TypeScript SDK for building agents, with a prebuilt harness.**

Monorepo for the Strands Agents SDKs in Python (3.10+) and TypeScript (Node.js 22+), plus a prebuilt harness created with create_harness() or createHarness(). The SDK covers the agent loop with turn and token limits, tools, MCP, structured output, multi-agent patterns, sessions, guardrails, tracing and evals. It runs in your process with no hosted control plane.

- **+** Same agent model in Python and TypeScript, with a CLI and an MCP docs server
- **+** Providers include Bedrock, Anthropic, OpenAI, Gemini and Ollama, plus custom ones
- **+** Hooks can intercept any step of the loop; tracing is on by default
- **+** Harness gives a working agent in one call, and you can drop to the SDK
- **−** TypeScript Agent defaults to Amazon Bedrock, so AWS credentials are needed unless you set a model
- **−** Several packages (harness, SDK, tools, CLI) to choose between; the split takes time to learn
- **−** Harness defaults are described as benchmarked, but the README gives no numbers

<sub>no GPU · Needs Python 3.10+ or Node.js 22+, Model provider credentials (Amazon Bedrock is the TypeScript SDK default) · Models: Amazon Bedrock, Anthropic, OpenAI, Gemini, Ollama · [Repo](https://github.com/strands-agents/harness-sdk) · [📖 Docs ↗](https://strandsagents.com/docs/user-guide/harness/) · [🌐 Site ↗](https://strandsagents.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/harness-sdk/)</sub>

<a name="browseros"></a>
### #&#8288;39 [browseros](https://github.com/browseros-ai/browseros) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · AGPL-3.0 · Nov 2026</sub>

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

<a name="llm"></a>
### #&#8288;40 [llm](https://github.com/simonw/llm) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

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

<a name="tambo"></a>
### #&#8288;41 [tambo](https://github.com/tambo-ai/tambo) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**React toolkit where an agent picks and renders your components.**

Tambo is a React SDK plus backend for generative UI. You register components with Zod schemas, and the agent chooses one and streams its props to it. The backend runs the LLM loop and conversation state, supports MCP servers and browser-side tools, and works with OpenAI, Anthropic, Gemini, Mistral, Cerebras or OpenAI-compatible providers. Tambo Cloud shuts down October 31, 2026, so new use means self-hosting.

- **+** Zod-schema components become LLM tool definitions; props stream to the UI
- **+** Supports MCP tools, prompts, elicitations and sampling
- **+** Browser-side local tools can touch the DOM or React state
- **+** SDK and backend are MIT; some workspaces such as apps/api are Apache-2.0
- **−** Hosted Tambo Cloud closes October 31, 2026; user data is deleted November 30
- **−** New signups are closed, and the team has moved on to a different product
- **−** React only; no other frontend frameworks are mentioned

<sub>no GPU · Compose · Needs LLM provider API key · Models: OpenAI, Anthropic, Google Gemini, Mistral, Cerebras · [Repo](https://github.com/tambo-ai/tambo) · [📖 Docs ↗](https://docs.tambo.co) · [🌐 Site ↗](https://tambo.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tambo/)</sub>

<a name="praisonai"></a>
### #&#8288;42 [praisonai](https://github.com/mervinpraison/praisonai) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · MIT · Nov 2026</sub>

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

<a name="rig"></a>
### #&#8288;43 [rig](https://github.com/0xplaygrounds/rig) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.1k · MIT · Nov 2026</sub>

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

<a name="open-connector"></a>
### #&#8288;44 [open-connector](https://github.com/oomol-lab/open-connector) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · custom license · Nov 2026</sub>

**Connector gateway exposing 1,000+ SaaS providers to agents via MCP, HTTP and SDK.**

OpenConnector stores user credentials for third-party apps (API key, OAuth2, custom, no-auth) and exposes a shared catalog of 1,000+ providers and 10,000+ prebuilt Actions through MCP, HTTP/OpenAPI, a TypeScript SDK and the oo CLI. Provider secrets stay inside the runtime; agents get schemas, scopes and results. It runs on Node.js or Docker with SQLite or PostgreSQL, on Helm, or on Cloudflare, with a web console for debugging and run logs.

- **+** Large catalog: 1,000+ providers and 10,000+ Actions with inspectable request/response schemas and scopes
- **+** Built-in OAuth 2.1 server with PKCE S256 and revocable, policy-scoped tokens for remote MCP clients
- **+** Many deployment targets: Docker, Node.js, Helm, Cloudflare Workers, SQLite or PostgreSQL 15+
- **+** Action allow/block policies and redacted run logs keep provider credentials out of the agent process
- **−** Modified Apache-2.0 license: offering it to third parties as a hosted service needs a commercial license
- **−** Self-hosting requires registering your own OAuth apps per provider; managed OAuth is only on OOMOL hosted
- **−** PostgreSQL migrations must be run manually with npm run runtime:migrate before upgrading
- **−** Requires recent Node.js (22.23.4+, 24.22.1+ or 26.12.1+) outside Docker

<sub>no GPU · Docker + Compose · Needs Node.js 22+, SQLite or PostgreSQL 15+, S3-compatible storage (optional), Docker (optional) · port 3000 · [Repo](https://github.com/oomol-lab/open-connector) · [📖 Docs ↗](https://oomol.com/docs/openconnector-self-hosting/) · [🌐 Site ↗](https://oomol.com/apps) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-connector/)</sub>

<a name="agent-framework"></a>
### #&#8288;45 [agent-framework](https://github.com/microsoft/agent-framework) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

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

<a name="flowgram-ai"></a>
### #&#8288;46 [flowgram.ai](https://github.com/bytedance/flowgram.ai) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (43) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · MIT · Nov 2026</sub>

**TypeScript toolkit for embedding visual workflow editors in your own product.**

FlowGram is a set of TypeScript packages for building a node-based workflow editor: free-layout and fixed-layout canvases, a node form engine, and a variable scope engine with type inference. It includes prebuilt nodes such as LLM, Condition and Code Editor. A separate FlowGram Desktop preview for macOS and Windows builds and runs workflows through chat and a canvas.

- **+** Two canvas modes: free layout and fixed layout with branch and loop nodes
- **+** Form engine covers validation, linkage and side effects for node config
- **+** Variable engine provides scope chains and type inference across nodes
- **+** Scaffold with npx @flowgram.ai/create-app; MIT license; used by Coze Studio
- **−** Front-end toolkit, not a hosted workflow server; you build the platform around it
- **−** Desktop app is a preview; installers are unsigned and macOS builds not notarized
- **−** Desktop installers listed only for macOS and Windows, no Linux build

<sub>no GPU · Needs Node.js, npm · port 3000 · [Repo](https://github.com/bytedance/flowgram.ai) · [▶️ Demo ↗](https://codesandbox.io/p/github/louisyoungx/flowgram-demo/main) · [📖 Docs ↗](https://flowgram.ai/guide/getting-started/introduction.html) · [🌐 Site ↗](https://flowgram.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flowgram-ai/)</sub>

<a name="open-multi-agent"></a>
### #&#8288;47 [open-multi-agent](https://github.com/open-multi-agent/open-multi-agent) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Nov 2026</sub>

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

<a name="langchain4j"></a>
### #&#8288;48 [langchain4j](https://github.com/langchain4j/langchain4j) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

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

<a name="ten-framework"></a>
### #&#8288;49 [ten-framework](https://github.com/ten-framework/ten-framework) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · custom license · Nov 2026</sub>

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

<a name="openui"></a>
### #&#8288;50 [openui](https://github.com/thesysdev/openui) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

**Generative UI framework that streams model-written UI via a compact language.**

OpenUI defines OpenUI Lang, a compact streaming-first language that models emit to describe UI, and renders it progressively as tokens arrive. You register a component library, generate a system prompt from it, and a renderer for React, Vue, Svelte or Angular draws the output. React also gets prebuilt chat layouts and two component libraries. The README reports up to 67% fewer tokens than equivalent JSON formats.

- **+** Renderers for React, Vue, Svelte and Angular on a framework-agnostic core
- **+** System prompt is generated from the component library you allow
- **+** Benchmarked at 4800 tokens vs 10180 for Vercel JSON-Render across seven scenarios
- **+** Scaffold CLI plus LangChain, assistant-ui and A2UI integrations
- **−** Prebuilt chat UI and component libraries ship for React only
- **−** Requires adopting a new language that models must be prompted to emit
- **−** Benchmark and comparison figures come from the project itself
- **−** Hosted observability package depends on the Thesys console and gateway

<sub>no GPU · Needs Node.js, LLM provider · Models: unknown · [Repo](https://github.com/thesysdev/openui) · [▶️ Demo ↗](https://www.openui.com/playground) · [📖 Docs ↗](https://openui.com) · [🌐 Site ↗](https://www.openui.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openui/)</sub>

<a name="voltagent"></a>
### #&#8288;51 [voltagent](https://github.com/voltagent/voltagent) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Nov 2026</sub>

**TypeScript framework for building multi-agent apps with workflows and memory.**

VoltAgent is a TypeScript framework for defining agents with typed tools, memory adapters, workflows, supervisor and sub-agent teams, guardrails, evals, voice and MCP support. Providers such as OpenAI, Anthropic and Google are swapped through config. A separate VoltOps Console adds traces, logs, prompts, deployment and triggers, offered as cloud or self-hosted.

- **+** Workflow engine with suspend/resume for human-in-the-loop steps
- **+** Supervisor and sub-agent orchestration, Zod-typed tools and MCP client built in
- **+** Durable memory adapters, e.g. LibSQL with a local file database
- **+** create-voltagent-app scaffolds an agent, workflow and Hono server on port 3141
- **−** TypeScript/Node only; no Python SDK mentioned in the README
- **−** Tracing, deployment and managed knowledge base tie into the VoltOps Console
- **−** No Docker or compose files detected in the repository

<sub>no GPU · Needs Node.js, LLM provider API (e.g. OpenAI), VoltOps Console (optional) · Models: OpenAI, Anthropic, Google · port 3141 · [Repo](https://github.com/voltagent/voltagent) · [▶️ Demo ↗](https://console.voltagent.dev/demo) · [📖 Docs ↗](https://voltagent.dev/docs/) · [🌐 Site ↗](https://voltagent.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voltagent/)</sub>

<a name="copilot-sdk"></a>
### #&#8288;52 [copilot-sdk](https://github.com/github/copilot-sdk) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Nov 2026</sub>

**SDKs that embed the GitHub Copilot CLI agent runtime in your own apps.**

Official SDKs for Python, TypeScript, Go, .NET, Java and Rust that drive the Copilot CLI agent runtime over JSON-RPC, so an application can run planning, tool calls and file edits without building its own orchestration. Custom agents, skills and tools can be defined, and an experimental in-process transport loads the native runtime through a C ABI instead of spawning the CLI. Requires a Copilot subscription unless you use BYOK with your own provider keys.

- **+** Six official language SDKs: Node.js, Python, Go, .NET, Java, Rust
- **+** Node.js, .NET and Rust bundle the CLI; Python downloads it on first use
- **+** BYOK mode supports OpenAI, Microsoft Foundry and Anthropic keys without GitHub auth
- **+** Per-SDK permission handler lets the app approve or deny tool calls
- **−** Standard use needs a GitHub Copilot subscription; usage counts against Copilot allowance
- **−** Go and Java do not bundle the CLI; it must be embedded or installed manually
- **−** BYOK is key-only; Entra ID and managed identities are not supported
- **−** In-process transport is experimental; elicitation schema handling differs across languages

<sub>no GPU · Needs GitHub Copilot CLI, GitHub Copilot subscription or BYOK API key · Models: Models available via Copilot CLI, BYOK: OpenAI, BYOK: Microsoft Foundry, BYOK: Anthropic · [Repo](https://github.com/github/copilot-sdk) · [📖 Docs ↗](https://github.com/github/copilot-sdk/blob/main/docs/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/copilot-sdk/)</sub>

<a name="mobilerun"></a>
### #&#8288;53 [mobilerun](https://github.com/droidrun/mobilerun) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Nov 2026</sub>

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

<a name="agentscope-java"></a>
### #&#8288;54 [agentscope-java](https://github.com/agentscope-ai/agentscope-java) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: niche (30) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Nov 2026</sub>

**Java framework for building multi-tenant agents with sandboxes and tool approvals.**

AgentScope Java 2.0 is a JDK 17+ library for building agents on a ReAct core. Its HarnessAgent layer adds workspace files, layered memory, subagents and context compaction. It streams 32 typed events, gates tool calls with allow, approve or deny rules, and runs tools in local, Docker, Kubernetes or E2B sandboxes. Session state can live in Redis, MySQL or PostgreSQL for stateless scaling.

- **+** Three-state tool permission engine with human approval built into the event stream
- **+** Session state in Redis, MySQL or PostgreSQL allows cross-replica recovery
- **+** Sandbox options: local subprocess, Docker, Kubernetes and E2B, with snapshot and resume
- **+** Separate model modules for DashScope, OpenAI, Anthropic, Gemini and Ollama
- **−** Library only: requires JDK 17+ and Maven, no standalone app or UI
- **−** Quickstart uses DashScope and the docs link Aliyun pages, leaning on that ecosystem
- **−** Some features, such as OpenAI Decisions, are only in 2.1.0-SNAPSHOT builds
- **−** No Docker image or compose file provided

<sub>no GPU · Needs JDK 17+, Maven, Redis (optional), MySQL (optional), PostgreSQL (optional), Docker or Kubernetes (optional sandbox) · Models: DashScope, OpenAI, Anthropic, Gemini, Ollama · [Repo](https://github.com/agentscope-ai/agentscope-java) · [📖 Docs ↗](https://java.agentscope.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentscope-java/)</sub>

<a name="camel"></a>
### #&#8288;55 [camel](https://github.com/camel-ai/camel) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (70) · Freshness: active (95) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Nov 2026</sub>

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

<a name="spring-ai"></a>
### #&#8288;56 [spring-ai](https://github.com/spring-projects/spring-ai) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (49) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Nov 2026</sub>

**Spring-style Java API for chat models, embeddings, vector stores and tool calling.**

Spring AI is a Java library that gives Spring Boot applications a portable API over model providers such as Anthropic, OpenAI, Amazon Bedrock, Google, Ollama, Mistral AI and DeepSeek. It covers chat, embedding, image, transcription, speech and moderation models, plus vector stores, tool calling, structured output to POJOs, chat memory, RAG and MCP starters. Version 2.x targets Spring Boot 4.x; 1.1.x targets Boot 3.5.x.

- **+** Portable ChatClient API across many providers, with sync and streaming modes
- **+** Boot starters and auto-configuration for models and vector stores
- **+** About 20 vector stores behind one SQL-like metadata filter API
- **+** MCP client and server starters with STDIO, SSE and Streamable-HTTP transports
- **−** Java and Spring Boot only; no support for other languages or frameworks
- **−** 2.x requires Spring Boot 4; Boot 3.5 users must stay on 1.1.x
- **−** A library, not a runnable app: no UI or hosted agent runtime
- **−** Major-version split means upgrades need migration work per the upgrade notes

<sub>no GPU · Needs Spring Boot, Maven, Model provider API or local runtime such as Ollama, Optional vector store · Models: Anthropic, OpenAI, Amazon Bedrock, Google, Ollama · [Repo](https://github.com/spring-projects/spring-ai) · [📖 Docs ↗](https://docs.spring.io/spring-ai/reference/getting-started.html) · [🌐 Site ↗](https://docs.spring.io/spring-ai/reference/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/spring-ai/)</sub>

<a name="flue"></a>
### #&#8288;57 [flue](https://github.com/withastro/flue) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · Apache-2.0 · Oct 2026</sub>

**TypeScript framework for building autonomous agents with sandboxes, skills and tools.**

Flue is a TypeScript agent harness where an agent is a function that composes a model, a sandbox, skills and tools through hooks such as useModel and useSandbox. It provides sessions, subagents, MCP tool connections, durable recovery of accepted work and channel events from Slack, Teams, Discord and GitHub. Agents run locally via CLI or deploy to Node.js, Cloudflare Workers, GitHub Actions, GitLab CI/CD, Daytona or Render.

- **+** Agent defined as a single function composing model, sandbox, skills and tools
- **+** Deploys to Node.js, Cloudflare Workers, GitHub Actions, GitLab CI/CD, Daytona and Render
- **+** Durable recovery of accepted work after failures and restarts
- **+** OpenTelemetry, Braintrust and Sentry observability; optional Postgres persistence adapter
- **−** TypeScript only; no other language runtimes mentioned
- **−** No Docker image or compose file in the repository
- **−** Example uses a hosted Anthropic model; local model support is not shown
- **−** Split across several packages (runtime, vite, cli, sdk, postgres), adding setup surface

<sub>no GPU · Needs Node.js, Postgres (optional persistence adapter) · Models: Anthropic (claude-sonnet-4-6 in example) · [Repo](https://github.com/withastro/flue) · [📖 Docs ↗](https://flueframework.com/docs/guide/building-agents/) · [🌐 Site ↗](https://flueframework.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flue/)</sub>

<a name="atomic-agents"></a>
### #&#8288;58 [atomic-agents](https://github.com/eigenwise/atomic-agents) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Nov 2026</sub>

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

<a name="eve"></a>
### #&#8288;59 [eve](https://github.com/vercel/eve) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · Apache-2.0 · Nov 2026</sub>

**TypeScript framework for durable agents defined as files in an agent/ directory.**

eve is a TypeScript framework where an agent is defined by a conventional directory: instructions.md, typed tools, on-demand skills, message channels (HTTP, Slack, Discord) and cron schedules. It scaffolds with `npx eve@latest init` and picks models by AI Gateway model ID. Web Chat can be added with Vercel sign-in, and `eve deploy` publishes the agent.

- **+** Agent layout is plain files: instructions.md, tools/, skills/, channels/, schedules/
- **+** Tools are typed functions defined with defineTool and Zod input schemas
- **+** Built-in channels for HTTP, Slack and Discord, plus cron schedules
- **+** Package ships its docs in node_modules/eve/docs for coding agents
- **−** Models are selected by AI Gateway model ID, tying setup to that gateway
- **−** Web Chat sign-in and deploy flow are built around Vercel projects
- **−** No Docker or compose files provided for self-hosting
- **−** Local model support is not described in the README

<sub>no GPU · Needs Node.js and npm, Vercel AI Gateway, Vercel project (for Web Chat and deploy) · Models: AI Gateway model IDs (e.g. openai/gpt-5.6-terra) · [Repo](https://github.com/vercel/eve) · [📖 Docs ↗](https://eve.dev/docs) · [🌐 Site ↗](https://eve.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/eve/)</sub>

<a name="baml"></a>
### #&#8288;60 [baml](https://github.com/boundaryml/baml) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · Apache-2.0 · Nov 2026</sub>

**Typed programming language for writing LLM functions and agents.**

BAML is a statically typed language with TypeScript-like syntax, implemented in Rust, for defining agent logic and LLM calls. It has a type system that persists at runtime, typed errors, green-thread concurrency, and a built-in test and eval framework. It can run standalone or be called from TypeScript, Python, Go, C# and Java.

- **+** Can be adopted incrementally by calling BAML functions from TS, Python, Go, C#, Java
- **+** Built-in test and eval framework plus a stdlib for agents
- **+** Typed, statically analyzed errors and no `any` type
- **+** Installs via Homebrew, with IDE and agent install commands
- **−** Requires learning a new language and toolchain instead of a library in your existing one
- **−** Claims of faster compiles than Go are given without benchmarks
- **−** Only a Homebrew install is shown; other platforms are not described in the README
- **−** Needs a separate editor extension and tooling setup for IDE support

<sub>[Repo](https://github.com/boundaryml/baml) · [📖 Docs ↗](https://boundaryml.com/quickstart) · [🌐 Site ↗](https://www.boundaryml.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/baml/)</sub>

<a name="eino"></a>
### #&#8288;61 [eino](https://github.com/cloudwego/eino) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

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

<a name="agent-native"></a>
### #&#8288;62 [agent-native](https://github.com/builderio/agent-native) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: ready (85) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 7.7k · no license · Nov 2026</sub>

**TypeScript framework for agents that share actions and state with an app UI.**

Agent-Native is a TypeScript framework where each capability is defined once as a zod-validated action. The agent calls it as a tool, and the React UI calls it through hooks such as useActionQuery. The same action is also exposed over HTTP, MCP, A2A and CLI. It ships agent chat, auth and permissions, skills and memory, scheduled automations, and PostgreSQL storage (PGlite for local development).

- **+** One action definition serves agent tool, UI call, HTTP, MCP, A2A and CLI
- **+** Agent and UI share validation, permissions, data and current UI state
- **+** Includes auth, memory, automations and agent teams out of the box
- **+** Sample apps (Mail, Calendar, Slides, Analytics and others) to fork as starting points
- **−** Examples and hooks are React-oriented; other front-ends are not documented in the README
- **−** No Docker or compose setup shown in the README
- **−** Production database is PostgreSQL only, per the README

<sub>Docker · Needs Node.js, PostgreSQL (production), PGlite (local development), LLM provider · [Repo](https://github.com/builderio/agent-native) · [📖 Docs ↗](https://agent-native.com/docs) · [🌐 Site ↗](https://agent-native.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-native/)</sub>

<a name="a2a"></a>
### #&#8288;63 [a2a](https://github.com/a2aproject/a2a) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 27k · Apache-2.0 · Nov 2026</sub>

**Open protocol for agent-to-agent communication over JSON-RPC and HTTP.**

A2A is a specification, not an application, for letting agents built on different frameworks talk to each other. It uses JSON-RPC 2.0 over HTTP(S), with Agent Cards for discovery, plus SSE streaming and asynchronous push notifications. SDKs exist for Python, Go, JavaScript, Java, .NET and Rust, and the project is hosted by the Linux Foundation.

- **+** SDKs in six languages: Python, Go, JS, Java, .NET, Rust
- **+** Agents collaborate without exposing internal memory, tools or logic
- **+** Supports sync requests, SSE streaming and async push notifications
- **+** Linux Foundation project with a written specification and docs site
- **−** Protocol spec only; this repo has no runnable agent or server
- **−** Roadmap still lists open items such as authorization schemes in AgentCard
- **−** Interoperability depends on each framework implementing the protocol correctly
- **−** SDKs and samples live in separate repositories

<sub>no GPU · [Repo](https://github.com/a2aproject/a2a) · [📖 Docs ↗](https://a2a-protocol.org/latest/specification/) · [🌐 Site ↗](https://a2a-protocol.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/a2a/)</sub>

<a name="pinchtab"></a>
### #&#8288;64 [pinchtab](https://github.com/pinchtab/pinchtab) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Sep 2026</sub>

**HTTP server and CLI that lets AI agents drive Chrome with compact snapshots.**

PinchTab is a single Go binary (about 30 MB) that runs a control-plane HTTP server on port 9867 and manages headless or headed Chrome instances with persistent profiles. Agents navigate, snapshot the accessibility tree, click by stable element refs and extract text through a CLI or REST API. It also ships site audit and visual compare commands, and an agent skill for Claude, Cursor, Windsurf and Codex.

- **+** Text extraction at about 800 tokens per page, versus roughly 10,000 for raw output
- **+** Persistent named profiles keep logins across restarts; multiple isolated instances run in parallel
- **+** Binds to 127.0.0.1 by default, with sensitive endpoints off and a local-only site allowlist
- **+** CLI and HTTP API, plus audit and compare commands usable as a CI gate
- **−** Needs a locally installed Chrome or Chromium; none is bundled in the binary
- **−** Not designed for multi-tenant or public-internet exposure; remote setups must be secured manually
- **−** Default allowlist blocks public websites until the operator widens it
- **−** Windows support is limited and less tested; the daemon workflow is not recommended there

<sub>no GPU · Docker + Compose · Needs Chrome or Chromium, Docker (optional) · port 9867 · [Repo](https://github.com/pinchtab/pinchtab) · [📖 Docs ↗](https://pinchtab.com/docs) · [🌐 Site ↗](https://pinchtab.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pinchtab/)</sub>

<a name="langchaingo"></a>
### #&#8288;65 [langchaingo](https://github.com/tmc/langchaingo) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (50) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.8k · MIT · Oct 2026</sub>

**Go port of LangChain for building LLM applications.**

LangChainGo is the Go implementation of LangChain, a library for composing LLM calls in Go programs. The README shows an OpenAI example using the llms package and points to a docs site, a pkg.go.dev reference and an examples directory. Provider, vector store and feature coverage are not listed in the README.

- **+** Native Go library that compiles into your service binary
- **+** MIT license with a docs site, API reference and examples directory
- **+** Common llms interface across providers, shown with OpenAI in the README
- **+** Linked blog posts cover Gemini and Ollama usage from Go
- **−** README says development is moving to a community effort and seeks maintainers
- **−** README shows only a basic completion example, no agents or RAG

<sub>no GPU · Needs Go toolchain, LLM provider API (e.g. OpenAI) · Models: OpenAI, Gemini, Ollama · [Repo](https://github.com/tmc/langchaingo) · [📖 Docs ↗](https://tmc.github.io/langchaingo/docs/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langchaingo/)</sub>

<a name="client"></a>
### #&#8288;66 [client](https://github.com/openai-php/client) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · MIT · Nov 2026</sub>

**PHP client library for the OpenAI API, with typed responses and streaming.**

Community-maintained PHP client for the OpenAI API, installed with Composer and requiring PHP 8.2+. It covers Responses, Conversations, Chat, Audio, Embeddings, Files, Images, Vector Stores, Batches and Fine-tuning, plus newer Agents, Skills and Containers resources. A factory sets base URI, organization, project, headers and a custom PSR-18 HTTP client, and an Azure service is listed.

- **+** Covers Responses, Conversations, Containers, Skills, Agents, Vaults, Batches and Realtime ephemeral keys
- **+** Streaming supported via createStreamed and retrieveStreamed methods
- **+** Factory accepts custom base URI, headers, query params and any PSR-18 HTTP client
- **+** Response objects expose typed properties and a toArray() method
- **−** Targets the OpenAI API; other providers only via a custom base URI or the Azure service
- **−** Requires PHP 8.2+ and a PSR-18 HTTP client such as Guzzle
- **−** Hosted shell and containers run on OpenAI; local command execution is left to your app
- **−** Several resources (Assistants, Threads, FineTunes, Edits, Completions) are deprecated or legacy

<sub>no GPU · Needs PHP 8.2+, Composer, PSR-18 HTTP client (e.g. guzzlehttp/guzzle), OpenAI API key · Models: OpenAI API models · [Repo](https://github.com/openai-php/client) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/client/)</sub>

<a name="ag2"></a>
### #&#8288;67 [ag2](https://github.com/ag2ai/ag2) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · Apache-2.0 · Nov 2026</sub>

**Python framework for building single agents and multi-agent networks.**

AG2 v1.0 is an async Python library (import ag2) where an Agent calls a model provider, runs @tool functions and returns a reply. Multiple agents coordinate through a Network: a Hub with a write-ahead log and typed channels (conversation, consulting, discussion, workflow). Optional harness pieces add a knowledge store, memory injection and history compaction. The older autogen API now lives in ag2-classic.

- **+** Typed Network channels with a hub write-ahead log and audit trail for multi-agent runs
- **+** Opt-in knowledge store and summarizing history compaction, with disk-backed persistence
- **+** Human-in-the-loop via context.input() inside tools, with a pluggable hitl_hook
- **+** Provider extras for OpenAI, Anthropic, Gemini and Ollama; minimal default dependencies
- **−** v1.0 is not a drop-in upgrade from the autogen-based classic API
- **−** Requires Python 3.11 or newer
- **−** Async-only API; no synchronous entry point shown
- **−** Maintained by volunteers across organizations, per the README

<sub>no GPU · Needs Python >= 3.11, LLM provider API key (OpenAI, Anthropic, Gemini) or Ollama · Models: OpenAI, Anthropic, Gemini, Ollama · [Repo](https://github.com/ag2ai/ag2) · [▶️ Demo ↗](https://playground.ag2.ai) · [📖 Docs ↗](https://docs.ag2.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ag2/)</sub>

<a name="dimos"></a>
### #&#8288;68 [dimos](https://github.com/dimensionalos/dimos) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · custom license · Nov 2026</sub>

**Python runtime and SDK for controlling robots with agents and MCP skills.**

DimOS is a Python runtime for robots (quadrupeds, humanoids, arms, drones) built from modules that exchange typed streams and are wired together with composable blueprints. It ships navigation, mapping, perception, spatial memory and manipulation primitives that an LLM agent can call as MCP tools, driven through a `dimos` CLI. Replay and MuJoCo simulation modes run without hardware; a hosted teleop service (dimTELE) is optional.

- **+** Replay and MuJoCo simulation modes run blueprints without robot hardware
- **+** Hardware list with stability tiers: Unitree Go2, xArm and Piper marked stable
- **+** Agent skills exposed over MCP and callable from the dimos CLI
- **+** Transports include Zenoh, LCM, DDS and ROS 2; C++, Lua, TypeScript interop examples
- **−** Most hardware support is beta, alpha or experimental; only a few platforms are stable
- **−** Ubuntu is the CI-tested platform; macOS is alpha and Nix is not CI-tested
- **−** dimTELE teleop depends on a hosted broker and an API key from Dimensional
- **−** License is reported as NOASSERTION, so terms need checking in the repo

<sub>Docker + Compose · Needs Python 3.12, Git LFS (replay data), MuJoCo (simulation), Ollama (optional, local LLM) · Models: LLM agents via MCP, Ollama (local LLM) · [Repo](https://github.com/dimensionalos/dimos) · [📖 Docs ↗](https://docs.dimensional.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dimos/)</sub>

<a name="agency-swarm"></a>
### #&#8288;69 [agency-swarm](https://github.com/vrsen/agency-swarm) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · MIT · Nov 2026</sub>

**Python multi-agent framework built on the OpenAI Agents SDK.**

Agency Swarm is a Python framework for building multi-agent applications on top of the OpenAI Agents SDK and Responses API. Agents get roles, instructions and Pydantic-typed tools, and an Agency object defines which agents may start conversations with which using directional communication flows (`ceo > dev`). Thread persistence is handled through save/load callbacks, and agencies can be run via a web demo, a terminal UI or async code.

- **+** Explicit directional communication_flows control which agents can message each other
- **+** Tools can be written with @function_tool, BaseTool or generated from OpenAPI schemas
- **+** Non-OpenAI models (Claude, Gemini, Grok, OpenRouter) reachable through LiteLLM
- **+** Built-in web demo, terminal UI and async API for running agencies
- **−** Tied to the OpenAI Agents SDK and Responses API; other providers go through LiteLLM
- **−** Requires Python 3.12 or newer
- **−** v1.x is a breaking rewrite from v0.x; existing projects need migration
- **−** Persistence is manual: you implement the load and save thread callbacks

<sub>no GPU · Needs OpenAI API key, OpenAI Agents SDK, LiteLLM (for non-OpenAI models) · Models: OpenAI GPT-5 family, GPT-4o, Anthropic Claude via LiteLLM, Google Gemini via LiteLLM, xAI Grok via LiteLLM · [Repo](https://github.com/vrsen/agency-swarm) · [📖 Docs ↗](https://agency-swarm.ai/welcome/installation) · [🌐 Site ↗](https://agency-swarm.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agency-swarm/)</sub>

<a name="smolagents"></a>
### #&#8288;70 [smolagents](https://github.com/huggingface/smolagents) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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

<a name="spring-ai-alibaba"></a>
### #&#8288;71 [spring-ai-alibaba](https://github.com/alibaba/spring-ai-alibaba) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: popular (55) · Freshness: active (94) · Maintenance: patchy (45) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

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

<a name="openmanus"></a>
### #&#8288;72 [openmanus](https://github.com/foundationagents/openmanus) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: widely used (94) · Freshness: recent (70) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Aug 2026</sub>

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

<a name="dexter"></a>
### #&#8288;73 [dexter](https://github.com/virattt/dexter) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: minimal (30) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 28k · no license · Sep 2026</sub>

**Terminal agent that plans and runs financial research using live market data.**

Dexter is a TypeScript agent that runs on Bun. It breaks a financial question into research steps, calls tools for income statements, balance sheets and cash flow data from Financial Datasets, and checks its own results before answering. It supports OpenAI, Anthropic, Google, xAI, OpenRouter and Ollama models, and can also be reached through a WhatsApp gateway.

- **+** Logs every tool call and agent step to JSONL scratchpad files for inspection
- **+** Includes loop detection and step limits against runaway execution
- **+** Eval suite with LangSmith tracking and LLM-as-judge scoring
- **+** Multiple model providers, including local Ollama
- **−** Needs a Financial Datasets API key, a third-party data service
- **−** Setup lists an OpenAI key as a prerequisite; fully local use is not documented
- **−** Focused on financial research, not a general-purpose agent library
- **−** README says it is not intended for real trading or investment

<sub>no GPU · Needs Bun, Financial Datasets API, Exa or Tavily (optional, web search), LangSmith (evals) · Models: OpenAI, Anthropic, Google, xAI, OpenRouter · [Repo](https://github.com/virattt/dexter) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dexter/)</sub>

<a name="gepa"></a>
### #&#8288;74 [gepa](https://github.com/gepa-ai/gepa) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · MIT · Nov 2026</sub>

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

<a name="kungfu"></a>
### #&#8288;75 [kungfu](https://github.com/kungfu-systems/kungfu) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · Apache-2.0 · Sep 2026</sub>

**Durable Work layer that keeps tasks intact across coding agents and failures.**

Kungfu is a C++ CLI, TUI and GUI that stores a task (Work) outside any agent session, with its objective, progress, evidence and next action. It wraps agents such as Codex, Claude, OpenCode and Amp via `kungfu run <agent>`, records each Attempt including failures, and blocks a second live writer on the same Work. Completion is decided by independent review and settlement, not by the agent that did the work. Alpha.

- **+** Work state persists across agent switches, crashes and disconnects without copying chat context
- **+** Blocks a second live agent from writing to the same Work
- **+** Built-in deterministic Mock Agent needs no provider credentials to try recovery scenarios
- **+** Agent cannot mark its own work complete; independent review and settlement decide
- **−** Alpha prerelease; README says it is not stable or generally available
- **−** Regular onboarding still needs a supported real agent for independent review
- **−** Creates a project-local .kungfu/ directory with Git-staging rules you must follow
- **−** Heavy custom vocabulary (Project, Work, Attempt, KFD, Shifu) raises the learning curve

<sub>no GPU · Needs Codex, Claude, OpenCode or Amp (for real agent runs and review) · Models: Codex, Claude, OpenCode, Amp · [Repo](https://github.com/kungfu-systems/kungfu) · [📖 Docs ↗](https://libkungfu.dev) · [🌐 Site ↗](https://kungfu.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kungfu/)</sub>

<a name="chatterbot"></a>
### #&#8288;76 [chatterbot](https://github.com/gunthercox/chatterbot) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · BSD-3-Clause · Nov 2026</sub>

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

<a name="rivet"></a>
### #&#8288;77 [rivet](https://github.com/rivet-dev/rivet) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (33) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · Apache-2.0 · Nov 2026</sub>

**Stateful Actor runtime with SQLite and WebSockets for durable agents and realtime apps.**

Rivet runs long-lived Actors with in-memory state, a per-Actor SQLite database, WebSockets and scheduling, one per agent, user or session. A Rust control plane schedules and persists them, using an S3-compatible bucket as the only dependency. Actors are written with the RivetKit TypeScript library (Rust SDK also available) on plain Node.js or Bun, and the project pitches them as a lighter place to run agent loops than per-agent sandboxes.

- **+** Only external dependency is an S3-compatible bucket; no Postgres, NATS or FoundationDB
- **+** Runs on stock Node.js or Bun, not a custom runtime
- **+** Per-Actor SQLite, hibernation, cron scheduling and Actor-to-Actor calls built in
- **+** Self-host on Docker Compose, Kubernetes, VMs, or use Rivet Cloud or BYOC
- **−** General actor platform; agent features come from optional libraries, not core
- **−** Headline latency and memory figures are vendor benchmarks against E2B and Durable Objects
- **−** Python and Swift clients are experimental; Dynamic Apps is in preview
- **−** Running the control plane adds operational work compared with an in-process library

<sub>no GPU · Docker · Needs S3-compatible object storage (S3, GCS, Azure Blob, MinIO, R2); local filesystem backend for single-machine trials · Models: Vercel AI SDK (README example uses OpenAI) · [Repo](https://github.com/rivet-dev/rivet) · [📖 Docs ↗](https://www.rivet.dev/docs) · [🌐 Site ↗](https://www.rivet.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rivet/)</sub>

<a name="genkit"></a>
### #&#8288;78 [genkit](https://github.com/genkit-ai/genkit) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="opengui"></a>
### #&#8288;79 [opengui](https://github.com/core-mate/opengui) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · custom license · Nov 2026</sub>

**Android GUI agent framework that operates real phones via screenshots.**

OpenGUI lets a vision-capable model see Android screens and perform taps, swipes, typing and navigation on real devices or emulators, for phone tasks and app testing. It ships as a WorkBuddy plugin (macOS), a DeepSeek Harness plugin, or a full self-hosted stack with a backend, Android client, CLI and IM dispatch via Feishu, Telegram and Discord. The source is under BUSL-1.1, so production use needs a commercial license.

- **+** Plugin install for WorkBuddy or DeepSeek Harness avoids deploying the full backend
- **+** Full stack adds CLI, REST API, and Feishu, Telegram and Discord task dispatch
- **+** Works on real devices over USB debugging, or on a local Android emulator
- **+** Routes to Claude, GPT, Gemini, Kimi, MiniMax or compatible models
- **−** BUSL-1.1 license: production and commercial use require a paid license; not OSI open source
- **−** WorkBuddy plugin is macOS only and is a public-testing prerelease
- **−** OpenGUI SMS sign-in currently requires a mainland-China phone number
- **−** Android only; needs a model with image input and tool calling

<sub>no GPU · Needs Android device with USB debugging or emulator, ADB / scrcpy, Node.js 22.19+ or 24+ (DSH plugin), WorkBuddy 5.5.3+ or DeepSeek Harness, Redis and PostgreSQL (full stack) · Models: Claude, GPT, Gemini, Kimi, MiniMax · [Repo](https://github.com/core-mate/opengui) · [📖 Docs ↗](https://github.com/core-mate/opengui/blob/main/docs/get-started.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opengui/)</sub>

<a name="jev-ultrafast"></a>
### #&#8288;80 [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: weak (17) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Nov 2026</sub>

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

<a name="agent-squad"></a>
### #&#8288;81 [agent-squad](https://github.com/2fastlabs/agent-squad) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (39) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · Apache-2.0 · Oct 2026</sub>

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

<a name="video-use"></a>
### #&#8288;82 [video-use](https://github.com/browser-use/video-use) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

**Agent skill that edits raw video footage into a finished cut via ffmpeg.**

A skill for Claude Code, Codex and similar shell-capable agents that turns a folder of raw takes into edit/final.mp4. It transcribes each source with ElevenLabs Scribe, packs word-level transcripts into a text file the LLM reads, and renders cuts with ffmpeg. Filler removal, color grading, subtitles and animation overlays are included, followed by a self-evaluation pass on the rendered output.

- **+** Works from a ~12KB text transcript plus on-demand timeline images instead of dumping frames
- **+** Cuts on word boundaries with 30ms audio fades and silence-gap detection
- **+** Self-eval loop re-checks rendered cut boundaries and re-renders up to 3 times
- **+** Session notes persist in project.md so work resumes across sessions
- **−** Requires an ElevenLabs API key; transcription is a cloud call
- **−** Needs a separate agent such as Claude Code or Codex; not standalone
- **−** No release published; install is a git clone plus symlink
- **−** Animation overlays depend on extra tools like HyperFrames, Remotion or Manim

<sub>no GPU · Needs ffmpeg, ElevenLabs API (Scribe), Claude Code or Codex, uv or pip, yt-dlp (optional) · Models: Claude Code, Codex, Hermes, Openclaw · [Repo](https://github.com/browser-use/video-use) · [🌐 Site ↗](https://video-use.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/video-use/)</sub>

<a name="marvin"></a>
### #&#8288;83 [marvin](https://github.com/prefecthq/marvin) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Oct 2026</sub>

**Python framework for structured LLM outputs and task-based agent workflows.**

Marvin is a Python library that turns LLM calls into typed results (extract, cast, classify, generate) and runs agentic workflows built from tasks, agents and threads. Version 3.0 ports the ControlFlow engine and uses Pydantic AI for model access, so it works with the providers Pydantic AI supports. Thread and message history is stored in SQLite.

- **+** Typed, validated results via Pydantic types, e.g. result_type=int or custom models
- **+** Works with all Pydantic AI model providers; OpenAI is the default
- **+** Small API: run, Task, Agent, Thread, plus extract, cast, classify, generate
- **+** Threads share context and history across tasks; marvin.plan breaks goals into tasks
- **−** No database migrations yet; README says to expect resetting data on updates
- **−** README's tool example runs untrusted shell commands; no sandboxing described
- **−** 3.0 renamed ControlFlow concepts (Flow to Thread, @flow removed), so migration is needed
- **−** No web UI or deployment tooling in README; observability is console output

<sub>no GPU · Needs LLM provider API key (OpenAI by default), SQLite (thread history) · Models: OpenAI, Anthropic, All Pydantic AI models · [Repo](https://github.com/prefecthq/marvin) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/marvin/)</sub>

<a name="fast-agent"></a>
### #&#8288;84 [fast-agent](https://github.com/evalstate/fast-agent) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · Apache-2.0 · Nov 2026</sub>

**Python framework and CLI for building MCP-enabled agents and workflows.**

fast-agent is a Python framework and CLI for defining agents with decorators and connecting them to MCP servers. It provides chain, parallel, router, orchestrator, evaluator-optimizer and MAKER workflows. It also runs as an interactive shell-enabled coding agent or as an ACP-compatible agent. Native providers are Anthropic, OpenAI and Google, plus Azure, Ollama and others via TensorZero.

- **+** Covers MCP features: sampling, elicitations, OAuth with keyring storage, Streamable HTTP diagnostics
- **+** Agents defined with short decorators; prompts and config live in plain files for version control
- **+** Built-in workflows: chain, parallel, router, orchestrator, evaluator-optimizer, MAKER, agents-as-tools
- **+** Passthrough and Playback LLMs let you test glue code without calling a real model
- **−** CLI-first; no web UI or visual workflow builder
- **−** Python only; setup instructions assume the uv package manager
- **−** No Docker or compose files provided
- **−** Providers beyond the native ones depend on TensorZero as an intermediary

<sub>no GPU · Needs uv, MCP servers, LLM provider API or local model server (Ollama, llama.cpp) · Models: Anthropic, OpenAI, Google, Azure, Ollama · [Repo](https://github.com/evalstate/fast-agent) · [📖 Docs ↗](https://fast-agent.ai) · [🌐 Site ↗](https://fast-agent.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fast-agent/)</sub>

<a name="agent-governance-toolkit"></a>
### #&#8288;85 [agent-governance-toolkit](https://github.com/microsoft/agent-governance-toolkit) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · MIT · Nov 2026</sub>

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

<a name="skill-recorder"></a>
### #&#8288;86 [skill-recorder](https://github.com/microsoft/skill-recorder) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · MIT · Nov 2026</sub>

**Electron app that turns a screen recording into an agent skill.**

Skill Recorder captures a screen session (window switches, browser URLs, clipboard previews, optional recorded terminal and narration), or imports an MP4/WebM file. GitHub Copilot CLI then reconstructs an intent and ordered steps, from which it generates a SKILL.md or a scheduled automation that prefers native tools over UI replay. Capture and Whisper transcription run locally; analysis sends data to GitHub's cloud.

- **+** Generates SKILL.md files or scheduled automations from a single recorded demonstration
- **+** Narration is transcribed on-device with Whisper, covering 99 languages
- **+** Imports MP4/WebM recordings, so no live capture or screen permission is needed
- **+** Fixture-based eval suite for the describer and builders (npm run eval)
- **−** Analysis requires a GitHub account with Copilot access; no other model provider is documented
- **−** Analyze uploads frames, URLs, clipboard previews and terminal output to GitHub's cloud
- **−** Source release only: installer builds the app locally and takes several minutes
- **−** Import limited to 512 MiB, 15 minutes and 4K; peak memory about 4.6 GB measured

<sub>no GPU · Needs GitHub Copilot CLI 1.0.78 (bundled), GitHub account with Copilot access, Node.js 24 (development only) · Models: GitHub Copilot, Whisper (local transcription) · [Repo](https://github.com/microsoft/skill-recorder) · [📖 Docs ↗](https://github.com/microsoft/skill-recorder/blob/main/INSTALL.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skill-recorder/)</sub>

<a name="stickman-video-director"></a>
### #&#8288;87 [stickman-video-director](https://github.com/kaomei/stickman-video-director) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · MIT · Nov 2026</sub>

**Agent Skill that turns a topic or script into stickman explainer videos.**

An installable Skill for AI assistants (Codex, Claude Code, Cursor and similar) that plans stickman videos from a topic, link or script. Director Mode produces a treatment, storyboards and per-scene prompts for an external video generator such as Google Flow, Runway, Luma or Kling. Autopilot Mode runs inside a coding agent to generate illustrated scenes, voiceover, captions and sound effects, then renders a finished video.

- **+** Two workflows: prompt-only Director Mode and end-to-end Autopilot rendering for 10+ minute videos
- **+** Ten visual styles, each with animated example clips
- **+** Supports 9:16, 16:9 and 1:1 aspect ratios and a choice of narration language
- **+** Script and 20-second preview approval steps before the full render
- **−** Director Mode clips must be generated in third-party video tools, then edited by hand
- **−** Autopilot needs a coding agent with file and terminal access; results vary by agent
- **−** Image generation and voiceover providers are not named in the visible README
- **−** Author recommends Codex; other agents may differ from the showcase output

<sub>Needs Codex, Claude Code, Cursor or similar coding agent, Google Flow, Runway, Luma or Kling (Director Mode), CapCut or Premiere (Director Mode editing) · [Repo](https://github.com/kaomei/stickman-video-director) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/stickman-video-director/)</sub>

<a name="koog"></a>
### #&#8288;88 [koog](https://github.com/jetbrains/koog) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · Apache-2.0 · Oct 2026</sub>

**Kotlin framework for building tool-calling AI agents on JVM and multiplatform.**

Koog is a Kotlin library for writing AI agents with a type-safe DSL, usable from Kotlin and Java. It supports graph-based workflows, custom tools, MCP and ACP, history compression, agent state persistence, and OpenTelemetry export to W&B Weave and Langfuse. It integrates with Spring Boot and Ktor and targets JVM, JS, WasmJS and iOS.

- **+** Idiomatic Kotlin DSL with Java API, plus Spring Boot and Ktor integrations
- **+** Multiplatform targets: JVM, JS, WasmJS and iOS from one codebase
- **+** Agent persistence, retries and history compression for long-running agents
- **+** Switch LLM providers mid-conversation while keeping history
- **−** Kotlin and Java only; no Python or TypeScript SDK
- **−** Requires JDK 17+ and Kotlin 2.3.10+ in existing projects
- **−** Additions module is published as a beta version (1.3.0-beta)
- **−** Library only: no UI, server or hosted runtime included

<sub>no GPU · Needs JDK 17+, Kotlin 2.3.10+, Gradle or Maven · Models: OpenAI, Anthropic, Google, DeepSeek, OpenRouter · [Repo](https://github.com/jetbrains/koog) · [📖 Docs ↗](https://docs.koog.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/koog/)</sub>

<a name="behaviortree-cpp"></a>
### #&#8288;89 [behaviortree.cpp](https://github.com/behaviortree/behaviortree.cpp) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Nov 2026</sub>

**C++17 library for building behavior trees for robots and game AI.**

BehaviorTree.CPP 4.9 is a C++17 library for defining behavior trees in XML and loading them at run time. Custom nodes can be linked statically or loaded as plugins. It targets robotics, with ROS2 builds through colcon, but also suits game AI or replacing finite state machines. It has no LLM features.

- **+** Asynchronous, non-blocking actions are first-class, with reactive concurrent execution
- **+** Tree structure lives in XML loaded at run time, not hard-coded in C++
- **+** Type-safe dataflow between nodes; custom nodes can be run-time plugins
- **+** Built-in logging and profiling to record, replay and analyze state transitions
- **−** No LLM, model or tool-calling integration; fits the agent category only loosely
- **−** Requires a C++17 compiler; Conan builds need CMake 3.23 or newer
- **−** Graphical editing needs the separate Groot2 tool
- **−** Commercial support is only by contacting the primary author

<sub>no GPU · Needs C++17 compiler, CMake, Conan, ZeroMQ, SQLite · [Repo](https://github.com/behaviortree/behaviortree.cpp) · [📖 Docs ↗](https://www.behaviortree.dev/) · [🌐 Site ↗](https://www.behaviortree.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/behaviortree-cpp/)</sub>

<a name="rust-sdk"></a>
### #&#8288;90 [rust-sdk](https://github.com/modelcontextprotocol/rust-sdk) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · custom license · Nov 2026</sub>

**Official Rust SDK for building MCP servers and clients on tokio.**

RMCP is the official Rust implementation of the Model Context Protocol, built on tokio and serde. It provides the `rmcp` core crate and `rmcp-macros`, whose `#[tool]`, `#[prompt]` and router macros generate tool and prompt handlers with JSON Schema 2020-12 schemas via schemars. It implements MCP 2026-07-28 and stays compatible with 2025-11-25 and earlier, and covers tools, resources, prompts, sampling, elicitation, tasks, and OAuth.

- **+** Official SDK from the modelcontextprotocol org, tracking the 2026-07-28 spec and older versions
- **+** Proc macros derive tool and prompt schemas from typed Rust structs
- **+** Supports stdio, child-process and streamable HTTP transports, including stateless HTTP
- **+** Client lifecycle modes allow discover, legacy initialize, or automatic fallback
- **−** 3.x release has breaking changes; upgrading from earlier versions requires the migration guide
- **−** Requires tokio; no other async runtime is mentioned
- **−** Library only; no ready-made server, so you write and build your own binary
- **−** License is reported as NOASSERTION by detection, so terms need checking

<sub>no GPU · Needs tokio, serde, schemars · [Repo](https://github.com/modelcontextprotocol/rust-sdk) · [📖 Docs ↗](https://docs.rs/rmcp/latest/rmcp) · [🌐 Site ↗](https://modelcontextprotocol.io/specification/2026-07-28) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rust-sdk/)</sub>

<a name="java-sdk"></a>
### #&#8288;91 [java-sdk](https://github.com/modelcontextprotocol/java-sdk) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · MIT · Nov 2026</sub>

**Official Java SDK for building MCP clients and servers.**

Java implementation of the Model Context Protocol, covering both client and server sides with synchronous and asynchronous APIs. The core module ships STDIO, JDK HttpClient and Jakarta Servlet transports, with Jackson for JSON behind a pluggable abstraction. Spring WebClient, WebFlux and WebMVC transports live in Spring AI 2.0+.

- **+** Reactive Streams API on Project Reactor, with a blocking synchronous facade
- **+** Modular artifacts: BOM, core, Jackson 2 and Jackson 3 bindings, bundled `mcp`
- **+** Server conformance suite passes 40/40 at conformance version 0.1.15
- **+** Transport-agnostic APIs with pluggable authorization hooks for servers
- **−** No built-in authorization; it must be supplied by the application or Spring
- **−** Client conformance 3/4 scenarios; Spring auth suite 12/14 scenarios fully passing
- **−** Spring transports are not in this repo; they require Spring AI 2.0+
- **−** Running the tests requires Docker and npx

<sub>no GPU · Needs Java 17+, Maven, Project Reactor, Jackson, SLF4J · [Repo](https://github.com/modelcontextprotocol/java-sdk) · [📖 Docs ↗](https://java.sdk.modelcontextprotocol.io/latest/quickstart/) · [🌐 Site ↗](https://modelcontextprotocol.io/docs/concepts/architecture) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/java-sdk/)</sub>

<a name="evolver"></a>
### #&#8288;92 [evolver](https://github.com/evomap/evolver) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (44) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · GPL-3.0 · Sep 2026</sub>

**CLI that turns agent logs into reusable Gene and Capsule evolution prompts.**

Evolver is a Node.js CLI that scans a project's memory/ logs, selects a matching Gene or Capsule from a local asset store, and prints a protocol-bound GEP prompt to stdout. It records an EvolutionEvent for audit and does not edit source code itself. Hooks exist for Cursor, Claude Code, Codex, Kiro and opencode; connecting to the EvoMap Hub is optional.

- **+** Core features run fully offline; the EvoMap Hub connection is optional
- **+** setup-hooks wires into Cursor, Claude Code, Codex, Kiro and opencode
- **+** Every cycle writes an auditable EvolutionEvent, with a --review confirmation mode
- **+** Strategy presets (balanced, innovate, harden, repair-only) set the intent mix
- **−** Only generates prompts; it does not patch code or run changes itself
- **−** Requires a git repository; fails in non-git directories
- **−** Maintainers say future releases move from GPL-3.0 to source-available
- **−** Loop mode output is not picked up by a live host agent session

<sub>no GPU · Needs Node.js >= 18, Git · [Repo](https://github.com/evomap/evolver) · [📖 Docs ↗](https://evomap.ai/wiki) · [🌐 Site ↗](https://evomap.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/evolver/)</sub>

<a name="guardrails"></a>
### #&#8288;93 [guardrails](https://github.com/guardrails-ai/guardrails) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (37) · Freshness: active (100) · Maintenance: patchy (41) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Aug 2026</sub>

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

<a name="csharp-sdk"></a>
### #&#8288;94 [csharp-sdk](https://github.com/modelcontextprotocol/csharp-sdk) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · custom license · Nov 2026</sub>

**Official C# SDK for building MCP clients and servers on .NET.**

Official .NET implementation of the Model Context Protocol, split into NuGet packages: Core for client and low-level server APIs, a hosting/DI package, and an ASP.NET Core package for HTTP-based servers. Extension packages cover MCP Apps, Skills and Tasks. It also supports the Identity Assertion Authorization Grant flow via IdentityAssertionGrantProvider.

- **+** Maintained under the modelcontextprotocol organization as the official C# SDK
- **+** Modular packages: Core has minimal dependencies, separate hosting and ASP.NET Core packages
- **+** Extension packages for MCP Apps, Skills and long-running Tasks
- **+** Covers both client and server roles, including HTTP servers via ASP.NET Core
- **−** Choosing among six NuGet packages requires reading the docs first
- **−** Limited to .NET; no other language bindings
- **−** Repository license is detected as NOASSERTION although README cites Apache 2.0
- **−** README has no code examples; usage lives in external docs and samples

<sub>no GPU · Needs .NET, NuGet, ASP.NET Core (HTTP servers) · [Repo](https://github.com/modelcontextprotocol/csharp-sdk) · [📖 Docs ↗](https://csharp.sdk.modelcontextprotocol.io/) · [🌐 Site ↗](https://modelcontextprotocol.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/csharp-sdk/)</sub>

<a name="sprix-sage-router"></a>
### #&#8288;95 [sprix-sage-router](https://github.com/wang2122/sprix-sage-router) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · MIT · Aug 2026</sub>

**Python router that picks continue, collaborate or hand off for in-flight A2A tasks.**

SAGE is a Python reference implementation of a routing layer between A2A agent discovery and task execution. Given a partially completed task DAG, it scores three routes (SELF, COLLABORATE, HANDOFF) under budget and deadline limits, using per-requirement trust and artifact reuse, and returns an auditable decision. It is a research preview, and its benchmarks use synthetic evaluators written with the project.

- **+** No runtime dependencies; Python 3.10+ and `python demo.py` to try it
- **+** Decision traces list excluded agents and alternatives, so routing choices are auditable
- **+** Learned trust state can be exported as versioned JSON snapshots
- **+** Deterministic seeded benchmarks with JSON output; README states their synthetic limits
- **−** Does not send tasks, authenticate endpoints or verify signatures; client handles A2A transport
- **−** Benchmarks use synthetic evaluators only; no real A2A endpoint evaluation yet
- **−** Real A2A adapters and signed Agent Card ingestion are unchecked on the roadmap
- **−** Labelled early-stage research preview with no production SLA

<sub>no GPU · [Repo](https://github.com/wang2122/sprix-sage-router) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sprix-sage-router/)</sub>

<a name="agenui"></a>
### #&#8288;96 [agenui](https://github.com/agenui/agenui) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Nov 2026</sub>

**Native iOS, Android and HarmonyOS renderer for streamed A2UI generative UI.**

AGenUI is a mobile SDK that implements Google's A2UI v0.9 protocol. A shared C++ core parses streamed LLM output, keeps a virtual component tree and diffs changes, and native renderers on iOS, Android and HarmonyOS draw 22 built-in components. It also ships a catalog JSON schema, an agent skill for generating A2UI messages, and a local bring-your-own-key studio.

- **+** One C++ core shared across iOS, Android and HarmonyOS renderers
- **+** Implements A2UI v0.9 with 18 protocol components plus 4 SDK extensions
- **+** Custom component and function-call APIs let the LLM emit app-specific components
- **+** Ships a freestanding catalog schema and an installable A2UI generation skill
- **−** Mobile only; no web or desktop renderer is mentioned
- **−** Building from source needs Android Studio with NDK, Xcode with CocoaPods, or DevEco Studio
- **−** Output quality depends on the LLM chosen; README only advises testing several models
- **−** Chart, Markdown and Lottie components exist only in the playground, not the SDK

<sub>no GPU · Needs Android Studio Hedgehog+, NDK 27.3.13750724, Xcode 15+, CocoaPods, CMake, DevEco Studio 4.0+, ohpm · Models: DeepSeek, Qwen, GLM, OpenAI, Gemini · [Repo](https://github.com/agenui/agenui) · [📖 Docs ↗](https://github.com/AGenUI/AGenUI/blob/main/docs/QuickStart.md) · [🌐 Site ↗](https://genui.amap.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agenui/)</sub>

<a name="agent-s"></a>
### #&#8288;97 [agent-s](https://github.com/simular-ai/agent-s) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: popular (60) · Freshness: active (87) · Maintenance: patchy (35) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

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

<a name="mobileagent"></a>
### #&#8288;98 [mobileagent](https://github.com/x-plug/mobileagent) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (47) · Freshness: active (100) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · MIT · Nov 2026</sub>

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

<a name="vision-agents"></a>
### #&#8288;99 [vision-agents](https://github.com/getstream/vision-agents) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (41) · Freshness: active (100) · Maintenance: weak (26) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="swarms"></a>
### #&#8288;100 [swarms](https://github.com/kyegomez/swarms) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (35) · Freshness: recent (70) · Maintenance: fair (54) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · Apache-2.0 · Nov 2026</sub>

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

<a name="aisuite"></a>
### #&#8288;101 [aisuite](https://github.com/andrewyng/aisuite) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Sep 2026</sub>

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

<a name="outlines"></a>
### #&#8288;102 [outlines](https://github.com/dottxt-ai/outlines) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: weak (9) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Aug 2026</sub>

**Python library that constrains LLM output to a type, schema or grammar.**

Outlines enforces structured output during generation. You pass a Python type, such as Literal, int, a Pydantic model or a function signature, and the model returns output matching it. The same call works across transformers, llama.cpp, vLLM, Ollama, OpenAI and Gemini backends, and it includes Jinja-based prompt templates.

- **+** Output type is a plain Python type: Literal, int, Pydantic model, union or function signature
- **+** Same model(prompt, output_type) call across transformers, llama.cpp, vLLM, Ollama, OpenAI and Gemini
- **+** Constrains generation itself, so no post-hoc JSON parsing or retry loop
- **+** Built-in Jinja prompt templates, loadable from strings or files
- **−** Library only: no server, UI or deployment tooling of its own
- **−** Dottxt API is early access and requires a request form
- **−** README does not detail constraint limits for hosted API backends

<sub>GPU optional · Needs transformers, pydantic · Models: transformers, llama.cpp, vLLM, Ollama, OpenAI · [Repo](https://github.com/dottxt-ai/outlines) · [📖 Docs ↗](https://dottxt-ai.github.io/outlines/latest/features/models/) · [🌐 Site ↗](https://dottxt.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/outlines/)</sub>

<a name="sensenova-skills"></a>
### #&#8288;103 [sensenova-skills](https://github.com/opensensenova/sensenova-skills) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: patchy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · MIT · Nov 2026</sub>

**Agent Skills for office tasks: infographics, PPT, Excel analysis, deep research.**

A collection of SKILL.md-based skills that extend agent runtimes such as OpenClaw and hermes-agent with office workflows: image and infographic generation, HTML/PPTX slide decks, Excel analysis, multi-source deep research, code-driven video, and project tracking. They are designed to pair with the SenseNova Platform API and are installed by copying skill directories into the agent's skills folder.

- **+** Follows the Agent Skills convention; each skill is a self-contained directory with SKILL.md
- **+** Covers a full chain: Excel analysis, deep research, then PPT generation, with an end-to-end example
- **+** Install is a plain copy into ~/.openclaw/skills/ or ~/.hermes/skills/
- **+** Search skills aggregate ArXiv, Semantic Scholar, PubMed, GitHub, Stack Overflow, Reddit and YouTube
- **−** Needs a separate agent runtime (OpenClaw or hermes-agent); not usable standalone
- **−** Recommended LLM is the SenseNova Platform API, which needs a regional API key
- **−** Proactive agent still requires a model-configured Hermes CLI for background processing
- **−** Per-category Python dependencies and keys are scattered across separate docs pages

<sub>Needs OpenClaw or hermes-agent, SenseNova Platform API key, Python, Node Playwright and Chromium (PPT export) · Models: SenseNova Platform API, SenseNova U1.5 Lite, SenseNova 6.7 Flash · [Repo](https://github.com/opensensenova/sensenova-skills) · [▶️ Demo ↗](https://office.xiaohuanxiong.com/home) · [📖 Docs ↗](https://platform.sensenova.ai/docs) · [🌐 Site ↗](https://sensenova.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sensenova-skills/)</sub>

<a name="oasis"></a>
### #&#8288;104 [oasis](https://github.com/camel-ai/oasis) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · Apache-2.0 · Nov 2026</sub>

**LLM-agent social media simulator for Twitter and Reddit-style platforms.**

OASIS is a Python library that simulates Twitter and Reddit-like platforms populated by LLM-driven agents, storing state in a database file. Agents choose from 23 actions (post, comment, follow, repost, search and others) and see content ranked by interest-based or hot-score recommenders. It targets research on information spread, polarization and herd behavior, with a stated scale of up to one million agents.

- **+** 23 agent actions, including follow, repost, quote, group chat and interview
- **+** Interest-based and hot-score recommendation algorithms built into the simulated platform
- **+** Per-agent model, tools and prompt customization, with a PettingZoo-style env interface
- **+** Installs from PyPI as camel-oasis; paper, dataset and docs site published
- **−** Token cost grows with agents and steps: 100 agents, one step used about 336k input tokens
- **−** Quick start only shows OpenAI; other providers go through CAMEL's model factory
- **−** Multi-modal platform support is still an open issue, not shipped
- **−** Last tagged release is December 2025, well behind the latest commits

<sub>no GPU · Needs camel-ai, LLM API key (OpenAI in quick start) · Models: OpenAI GPT-4o-mini, Qwen (via CAMEL), OpenAI embeddings for Twhin-Bert recommender · [Repo](https://github.com/camel-ai/oasis) · [▶️ Demo ↗](https://www.youtube.com/watch?v=lprGHqkApus&t=2s) · [📖 Docs ↗](https://docs.oasis.camel-ai.org/) · [🌐 Site ↗](https://www.camel-ai.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/oasis/)</sub>

<a name="claude-trading-skills"></a>
### #&#8288;105 [claude-trading-skills](https://github.com/tradermonty/claude-trading-skills) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · MIT · Nov 2026</sub>

**Claude Skills for market review, trade planning and journaling by individual investors.**

A collection of Claude Skills (SKILL.md folders with Python helpers) for market breadth checks, dividend and swing screeners, position sizing, trade journaling and post-trade review. Workflow manifests in workflows/ chain skills into daily, weekly and monthly routines. It installs into Claude Code's skills directory or uploads as .skill packages to the Claude web app. It is not a signal service and does not place orders.

- **+** Workflow YAML manifests name exact skills, decision gates and artifacts in order
- **+** Five-skill starter path needs no paid market-data API
- **+** skills-index.yaml is a validator-enforced canonical index of every skill
- **+** Supports Python 3.11-3.13 on Linux, Windows and macOS, checked in CI
- **−** Requires Claude (web or Code); not usable with other models
- **−** Many screeners require an FMP key; some workflows need FINVIZ Elite or Alpaca
- **−** US-equity focused, built around one author's Core + Satellite style
- **−** No GitHub release yet; web app users may need to build packages locally

<sub>no GPU · Needs Claude (web app or Claude Code), Python 3.11-3.13, FMP API (optional), FINVIZ Elite (optional), Alpaca (optional) · Models: Claude · [Repo](https://github.com/tradermonty/claude-trading-skills) · [📖 Docs ↗](https://tradermonty.github.io/claude-trading-skills/) · [🌐 Site ↗](https://tradermonty.github.io/claude-trading-skills/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/claude-trading-skills/)</sub>

<a name="seedance-2-0"></a>
### #&#8288;106 [seedance-2.0](https://github.com/emily2040/seedance-2.0) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (40) · Freshness: active (100) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.2k · MIT · Sep 2026</sub>

**Agent skill that turns ideas into shot-by-shot Seedance 2.0 video prompts.**

Seedance 2.0 Skill OS is an agent skill that plans shots, binds reference assets and continues from an accepted clip, producing structured prompts for the Seedance 2.0 video model. Each prompt is rendered from a published shot table and passes a moderation pre-screen. Generation and its costs stay with your video provider.

- **+** Prompts ship with a shot table, so camera and eye-line geometry can be checked before paying for a render
- **+** Includes a moderation pre-screen step for prompts before submission
- **+** Example prompts in English, Chinese, Korean, Japanese and Russian; docs in six languages
- **+** MIT licensed, versioned (v6.7.0) with a changelog
- **−** Targets one video model, Seedance 2.0; other generators are not covered
- **−** Needs a separate video provider account; generation costs are paid there
- **−** Showcase clips shown are marked not rendered yet, with slates in their place
- **−** Prompts are long and prescriptive, repeating a lock line in every shot

<sub>no GPU · Needs Seedance 2.0 video provider account · Models: Seedance 2.0 · [Repo](https://github.com/emily2040/seedance-2.0) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/seedance-2-0/)</sub>

<a name="deep-chat"></a>
### #&#8288;107 [deep-chat](https://github.com/ovidijusparsiunas/deep-chat) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Oct 2026</sub>

**Embeddable web component that adds a chat UI to any website.**

Deep Chat is a front-end web component (<deep-chat>, installed via npm) that you embed in a page and point at your own backend or at one of 20+ AI APIs such as OpenAI and Claude. It handles file upload, webcam and microphone capture, speech-to-text, text-to-speech and Markdown rendering. It has examples for React, Vue, Svelte, Angular, Solid, Next and Nuxt, and can run a model in the browser through a separate web-llm module.

- **+** One custom element works across React, Vue, Svelte, Angular, Solid and plain JS
- **+** directConnection covers 20+ AI APIs, including OpenAI, Claude, Open WebUI, LiteLLM and Dify
- **+** Built-in camera, microphone, speech-to-text, text-to-speech and file upload
- **+** Server templates provided for Express, Nest, Flask, Spring, Go, SvelteKit and Next
- **−** Front-end component only; no user accounts or server-side chat history included
- **−** directConnection exposes the API key in the browser; README says prototyping only
- **−** Custom backends must match Deep Chat's request and response format, or use interceptors
- **−** In-browser model needs the separate deep-chat-web-llm module

<sub>GPU optional · Needs npm · Models: OpenAI, Claude, Open WebUI, LiteLLM, Dify · [Repo](https://github.com/ovidijusparsiunas/deep-chat) · [▶️ Demo ↗](https://deepchat.dev/playground) · [📖 Docs ↗](https://deepchat.dev/docs/connect) · [🌐 Site ↗](https://deepchat.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deep-chat/)</sub>

<a name="tuyaopen"></a>
### #&#8288;108 [tuyaopen](https://github.com/tuya/tuyaopen) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · custom license · Nov 2026</sub>

**C/C++ SDK for building AI voice and agent hardware on Tuya, ESP32 and others.**

TuyaOpen is a cross-platform C/C++ SDK for firmware on Tuya T2/T3/T5 modules, ESP32 variants, LN882H, BK7231N and Ubuntu hosts. It covers speech features (ASR, KWS, TTS, STT) and connects devices to Tuya Cloud for remote control, OTA updates and hosted LLM workflows. Cloud-side models named in the README include ChatGPT, Gemini, Claude, Qwen, Doubao and Deepseek.

- **+** Targets real MCU hardware: Tuya T2/T3/T5, ESP32/C3/S3, LN882H, BK7231N
- **+** Can also be built for Ubuntu hosts, which helps with development
- **+** Ships speech building blocks (ASR, KWS, TTS, STT) plus Arduino and Lua companion projects
- **+** Documents debug serial ports and supported modules for each target platform
- **−** AI agent workflows and OTA depend on Tuya Cloud, not a fully self-hosted stack
- **−** Aimed at hardware firmware; not a general LLM app or agent library
- **−** Tuya modules are the primary targets; other chips have less documented support
- **−** README links to third-party submodules that may lag behind upstream

<sub>Docker · Needs Tuya Cloud · Models: ChatGPT, Gemini, Claude, Qwen, Doubao · [Repo](https://github.com/tuya/tuyaopen) · [📖 Docs ↗](https://tuyaopen.ai/docs/about-tuyaopen) · [🌐 Site ↗](https://tuyaopen.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tuyaopen/)</sub>

<a name="owl"></a>
### #&#8288;109 [owl](https://github.com/camel-ai/owl) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 20k · no license · Nov 2026</sub>

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

<a name="cuawright"></a>
### #&#8288;110 [cuawright](https://github.com/microsoft/cuawright) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: weak (26) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · MIT · Oct 2026</sub>

**Coding-model agent that writes Playwright scripts and runs desktop tasks in a VM.**

CUAWright gives a coding model a terminal to automate browsers and desktop applications. The browser runtime (formerly Webwright) writes and debugs Playwright scripts, with OpenAI, Anthropic and OpenRouter backends. The desktop runtime runs custom or official OSWorld-V2 tasks in an Ubuntu VM through a Responses-compatible API. It also ships Claude Code and Codex plugin manifests.

- **+** Browser runs leave reusable Playwright scripts, with trajectories and screenshots saved to disk
- **+** Reports 88.1% on Online-Mind2Web and 67.9% partial score on OSWorld-V2
- **+** Plugin manifests for Claude Code and Codex reuse the host agent, no extra API key
- **+** Browser core is small: httpx, pydantic, playwright and typer, with three model backends
- **−** Desktop mode needs Python 3.12+, Docker and gated Hugging Face task and asset access
- **−** Desktop runs do not export screenshot files or copy VM files to the host
- **−** Persistent live-browser config depends on a Browserbase cloud account
- **−** Desktop runtime is Apache-2.0 while the rest is MIT, so licensing is split

<sub>no GPU · Needs Python 3.10+ (3.12+ for desktop), Playwright Chromium, Docker (desktop), Hugging Face gated datasets (desktop), Browserbase (live-browser config) · Models: OpenAI, Anthropic, OpenRouter, Responses-compatible APIs · [Repo](https://github.com/microsoft/cuawright) · [📖 Docs ↗](https://arxiv.org/abs/2610.04116) · [🌐 Site ↗](https://microsoft.github.io/CUAWright/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cuawright/)</sub>

<a name="semif-openjev"></a>
### #&#8288;111 [semif-openjev](https://github.com/theoleecj/semif-openjev) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · MIT · Sep 2026</sub>

**Reads typed option probabilities from a local LLM instead of generating text.**

SemIf scores runtime-defined decisions (routing, retry, evidence checks) by reading the logits of declared options in one forward pass, with no sampled answer or JSON parsing. It runs on CUDA, Apple Silicon (MLX or PyTorch/MPS) and CPU through llama.cpp GGUF, and can reuse a shared state across many criteria. It reproduces the interface pattern of TypeSafe's closed Jev service, not its model.

- **+** Direct logits took 1.023 s versus 5.332 s for a JSON array on 21 criteria
- **+** Shared-state mode reached 20.03 decisions/s on a 37x21 workload versus 2.33 fresh
- **+** Backends for CUDA, MLX, PyTorch/MPS and CPU-only llama.cpp GGUF
- **+** Fixtures, row-level outputs, prompt hashes and model revisions are committed, plus per-workload calibration
- **−** Prefix-reuse paths are experimental; BF16 changed 5-6 of 777 argmaxes
- **−** 4B baseline reaches 0.845 agreement on the TypeSafe subset versus 0.883 for Jev
- **−** Probabilities are conditional on the supplied options and need calibration per workload
- **−** Research baseline with no release and no server or API

<sub>GPU optional · Needs PyTorch, Hugging Face model weights, llama.cpp (CPU backend), MLX (Apple Silicon backend) · Models: Qwen3.5-4B, MiniCPM5-2B, Qwen3-0.6B, Qwen3.8-27B EXL3, GGUF (llama.cpp) · [Repo](https://github.com/theoleecj/semif-openjev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/semif-openjev/)</sub>

<a name="roast-room"></a>
### #&#8288;112 [roast-room](https://github.com/nateherkai/roast-room) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: patchy (33) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · custom license · Oct 2026</sub>

**Claude Code skill that runs a council of AI advisors on business decisions.**

Roast Room is a set of Claude Code skills and sub-agents that debate a business decision. Twelve advisor personas, each built from a person's public work, score your options in rounds, and the Chair writes a verdict to verdict.md plus a PDF. A zero-dependency Node app on localhost:4730 replays the sessions as a table view, and /newroaster builds additional advisors.

- **+** Runs on a Claude plan through Claude Code, no API key needed by default
- **+** Quotes are checked against each advisor's sources with check_quotes.py
- **+** /newroaster builds custom advisors from public or personal material
- **+** Web app has no npm dependencies and saves every session with PDF export
- **−** Full council uses 21 sub-agent runs for seven seats, a heavy bite of plan usage
- **−** Advisors are simulations of real people, not endorsed by them
- **−** Portrait generation needs a kie.ai key and opencv-python
- **−** License is reported as NOASSERTION; README says code is MIT

<sub>no GPU · Needs Claude Code, Node.js 20+, kie.ai API key (optional, portraits), yt-dlp (optional), pdftotext (optional), Anthropic API key (optional, api mode) · Models: Claude (via Claude Code), Anthropic API (optional) · port 4730 · [Repo](https://github.com/nateherkai/roast-room) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/roast-room/)</sub>

<a name="promptflow"></a>
### #&#8288;113 [promptflow](https://github.com/microsoft/promptflow) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (56) · Freshness: recent (70) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**Python toolkit for building, tracing and evaluating LLM flows from a CLI.**

Prompt flow defines LLM apps as executable flows in a flow.dag.yaml that link LLM calls, prompts and Python code. It provides a pf CLI for testing flows, managing OpenAI and Azure OpenAI connections, tracing LLM calls and batch-evaluating against datasets, plus a VS Code flow designer. Microsoft has announced retirement on April 20, 2027 and no longer recommends it for new development.

- **+** Flows are YAML DAGs linking LLM, prompt and Python nodes, runnable with `pf flow test`
- **+** Batch runs and evaluation over datasets can be wired into CI/CD
- **+** Built-in tracing of LLM interactions for debugging flows
- **+** VS Code extension offers a visual flow designer
- **−** Retirement announced for April 20, 2027; not recommended for new development
- **−** Runtime container images no longer receive security or package updates
- **−** Last release was 2025-01-09; migration to Microsoft Agent Framework is advised
- **−** Telemetry is on by default; opt out with `pf config set telemetry.enabled=false`

<sub>no GPU · Needs Python 3.9-3.11 recommended, OpenAI or Azure OpenAI API key · Models: OpenAI, Azure OpenAI · [Repo](https://github.com/microsoft/promptflow) · [📖 Docs ↗](https://microsoft.github.io/promptflow/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/promptflow/)</sub>

<a name="guidance"></a>
### #&#8288;114 [guidance](https://github.com/guidance-ai/guidance) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (75) · Freshness: recent (73) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · May 2026</sub>

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

<a name="pocketflow"></a>
### #&#8288;115 [pocketflow](https://github.com/the-pocket/pocketflow) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (57) · Freshness: active (93) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Jul 2026</sub>

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

<a name="upsonic"></a>
### #&#8288;116 [upsonic](https://github.com/upsonic/upsonic) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (39) · Freshness: active (85) · Maintenance: weak (13) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · MIT · Jun 2026</sub>

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

<a name="skills"></a>
### #&#8288;117 [skills](https://github.com/browser-act/skills) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Nov 2026</sub>

**Browser automation skill that gives coding agents stealth and local Chrome control.**

BrowserAct Skills adds a `browser-act` CLI and Skill that agents such as Claude Code, Cursor and Codex load to drive a real browser. It supports local Chrome profile reuse and stealth browsers with fingerprint and proxy handling, and exposes indexed page state (`state`, `click 3`, `input 2`). It also offers CAPTCHA solving, human handoff via `remote-assist`, and Skill Forge, which generates site-specific scraping Skills.

- **+** Indexed text page state lets agents click and type by number, without parsing the DOM
- **+** Three browser modes: local Chrome, stealth privacy, and stealth fixed identity
- **+** Sensitive actions like browser creation and proxy changes need fresh user approval, enforced in the Skill
- **+** Works with any agent that can run shell commands and load Skills; Windows, macOS, Linux
- **−** Stealth browsers, solve-captcha and remote-assist require a BrowserAct login
- **−** Managed proxies and more than 5 stealth browsers are paid
- **−** Anti-bot and CAPTCHA features depend on BrowserAct's hosted services, not only local code
- **−** Cloud scraping-Bot mode is a commercial product, separate from the MIT-licensed Skills

<sub>no GPU · Needs Chrome, BrowserAct account (for stealth features), AI agent that can run shell commands · [Repo](https://github.com/browser-act/skills) · [▶️ Demo ↗](https://www.youtube.com/watch?v=sTUD4drYYrk) · [📖 Docs ↗](https://docs.browseract.com) · [🌐 Site ↗](https://www.browseract.com/?co-from=github) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skills/)</sub>

<a name="rlm"></a>
### #&#8288;118 [rlm](https://github.com/alexzhang13/rlm) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: weak (17) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · MIT · Nov 2026</sub>

**Python library that lets an LLM recursively call itself from a REPL.**

rlms replaces a plain llm.completion call with rlm.completion. The prompt is loaded as a variable in a REPL, and the model writes code to inspect it and launch sub-LM calls. It supports OpenAI, Anthropic, OpenRouter and Portkey clients, plus local models through vLLM's OpenAI interface. The repo also includes a verifiers/prime-rl training environment and a trajectory visualizer.

- **+** Handles long contexts by keeping the prompt as a REPL variable with recursive sub-calls
- **+** REPL backends: local, ipython, docker, modal, prime, daytona, e2b
- **+** Includes a prime-rl/verifiers training setup with an OOLONG example
- **+** JSONL trajectory logging with a local visualizer for inspecting sub-calls
- **−** Default local REPL runs Python exec in the host process; README says not for production
- **−** Prime Sandboxes are beta, with slow runtimes noted as an open issue
- **−** Cloud sandbox environments need separate accounts and API keys (Modal, Prime, Daytona, E2B)
- **−** Training harness uses unsandboxed local REPL, which the README says is not ideal for safety

<sub>no GPU · Needs Python 3.11+, LLM API or vLLM server, Docker (optional), Modal/Prime/Daytona/E2B (optional), Node.js (visualizer) · Models: OpenAI, Anthropic, OpenRouter, Portkey, vLLM · port 3001 · [Repo](https://github.com/alexzhang13/rlm) · [📖 Docs ↗](https://alexzhang13.github.io/rlm/) · [🌐 Site ↗](https://alexzhang13.github.io/blog/2025/rlm/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rlm/)</sub>

<a name="metagpt"></a>
### #&#8288;119 [metagpt](https://github.com/foundationagents/metagpt) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: widely used (96) · Freshness: quiet (18) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · MIT · Jan 2026</sub>

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

<a name="instagram-agent-skill"></a>
### #&#8288;120 [instagram-agent-skill](https://github.com/jakeschincariol/instagram-agent-skill) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: weak (12) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Sep 2026</sub>

**Thirteen Claude skills for writing Instagram Reels, captions, carousels and DMs.**

A set of thirteen Claude skills that draft Instagram content: Reel scripts from 26 hook formulas, captions, carousels, stories, profile rewrites, comments, replies and DMs. Five local Python scripts with no dependencies score hooks, time beat sheets, lint captions, strip AI tells from text and rank outlier reels. Nothing is posted; every skill ends with copy-ready text.

- **+** Five Python tools run locally with no dependencies, no network and no uploads
- **+** Author publishes measured results: hook scorer AUC 0.83 on bad hooks, 0.56 on winners
- **+** Caption linter previews the 125-character feed cutoff and enforces the five-hashtag cap
- **+** Humanizer lexicon in slop.json (154 terms) is editable; installs as skills or plugin
- **−** Hook scorer barely separates a creator's hits from misses (AUC 0.56)
- **−** Validated on 74 YouTube Shorts hooks, not Instagram Reels
- **−** Does not post, comment or DM; you publish everything manually
- **−** Full tooling needs Claude Code; pasted into plain chat it loses the Python tools

<sub>no GPU · Needs Claude Code, Python 3 · Models: Claude · [Repo](https://github.com/jakeschincariol/instagram-agent-skill) · [🌐 Site ↗](https://opusjake.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/instagram-agent-skill/)</sub>

<a name="x"></a>
### #&#8288;121 [x](https://github.com/ant-design/x) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 4.8k · no license · Oct 2026</sub>

**React component library for building LLM chat and agent interfaces.**

Ant Design X is a set of npm packages for building AI front-ends in React on top of Ant Design. It includes UI components for conversation stages, an SDK for managing model data streams, a streaming Markdown renderer, and an A2UI-based card renderer for agent-generated interfaces. A separate skill package supplies agent skills for developing with the library.

- **+** Split into packages: components, SDK, Markdown renderer, card renderer, skills
- **+** Markdown renderer supports streaming formulas, code highlighting and mermaid
- **+** Card renderer builds interfaces from A2UI structured JSON message streams
- **+** Used in AI interfaces inside Ant Group, per the README
- **−** Front-end library only; no model serving or backend included
- **−** Tied to React and the Ant Design ecosystem
- **−** No license detected in the repository metadata

<sub>no GPU · Needs React, Ant Design, npm · [Repo](https://github.com/ant-design/x) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/x/)</sub>

<a name="self-operating-computer"></a>
### #&#8288;122 [self-operating-computer](https://github.com/othersideai/self-operating-computer) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (52) · Freshness: recent (70) · Maintenance: weak (15) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · MIT · Oct 2026</sub>

**CLI that lets multimodal models control a computer through screenshots, mouse and keyboard.**

Python framework, installed with pip and run as `operate`, that sends screenshots to a multimodal model and executes the mouse and keyboard actions it returns until an objective is met. It supports GPT-4o, GPT-4.1, o1, Gemini Pro Vision, Claude 3, Qwen-VL and LLaVA via Ollama, with OCR and Set-of-Mark modes for locating click targets. Runs on macOS, Windows and Linux with X server.

- **+** Works with hosted models and a local LLaVA via Ollama, selected with the `-m` flag
- **+** OCR and Set-of-Mark modes ground clicks in on-screen text or detected buttons
- **+** Installs with `pip install self-operating-computer`; runs on macOS, Windows and Linux with X server
- **+** Optional voice input for the objective via `--voice`
- **−** README says LLaVA error rates are very high; local use is only a base to build on
- **−** Last release was 2025-02-28, and the README still lists older models like Claude 3
- **−** README says gpt-4o is required and needs $5 of OpenAI API spend to unlock
- **−** Needs Screen Recording and Accessibility permissions; no sandbox, actions run on the host

<sub>GPU optional · Needs OpenAI API key (default gpt-4o), Ollama (for LLaVA), portaudio (voice mode) · Models: GPT-4o, GPT-4.1, o1, Gemini Pro Vision, Claude 3 · [Repo](https://github.com/othersideai/self-operating-computer) · [▶️ Demo ↗](https://github.com/OthersideAI/self-operating-computer/assets/42594239/9e8abc96-c76a-46fb-9b13-03678b3c67e0) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/self-operating-computer/)</sub>

<a name="youtube-agent-skill"></a>
### #&#8288;123 [youtube-agent-skill](https://github.com/jakeschincariol/youtube-agent-skill) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · MIT · Sep 2026</sub>

**Eleven Claude skills for scripting, packaging and analyzing YouTube videos.**

A set of eleven Claude skills (/yt-script, /yt-package, /yt-edit, /yt-retention, /yt-viral and others) that draft scripts, lint title and thumbnail pairs, build edit decision lists and read retention exports. Six of them are backed by dependency-free Python 3 scripts, such as a hook scorer built on 21 hook formulas. Nothing is published; each skill outputs text for the creator to upload.

- **+** Six Python tools run on plain Python 3 with no dependencies
- **+** No API key or account connection needed; MIT licensed
- **+** Installs via git copy, Claude Code plugin, or pasted SKILL.md
- **+** README states hookscore.py limits: calibrated on 74 hooks, a heuristic only
- **−** Built for Claude; without Claude Code the Python tools are lost
- **−** Does not upload or publish; every output is copy-and-paste
- **−** Hook score separates bad hooks from real ones, not a creator's hits from misses
- **−** Needs a hand-written voice.md for good output

<sub>no GPU · Needs Claude, Claude Code, Python 3 · Models: Claude · [Repo](https://github.com/jakeschincariol/youtube-agent-skill) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/youtube-agent-skill/)</sub>

<a name="swarm"></a>
### #&#8288;124 [swarm](https://github.com/openai/swarm) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: popular (76) · Freshness: recent (56) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Apr 2026</sub>

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

<a name="julep"></a>
### #&#8288;125 [julep](https://github.com/julep-ai/julep) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (31) · Freshness: active (94) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · Apache-2.0 · Jul 2026</sub>

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

<a name="xagent"></a>
### #&#8288;126 [xagent](https://github.com/openbmb/xagent) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (42) · Freshness: recent (66) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · Apache-2.0 · Jul 2026</sub>

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

<a name="qwen-agent"></a>
### #&#8288;127 [qwen-agent](https://github.com/qwenlm/qwen-agent) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: popular (69) · Freshness: quiet (29) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Mar 2026</sub>

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

<a name="openbrowser"></a>
### #&#8288;128 [openbrowser](https://github.com/ntegrals/openbrowser) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: known (49) · Freshness: recent (50) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · MIT · Mar 2026</sub>

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

<a name="clawteam"></a>
### #&#8288;129 [clawteam](https://github.com/hkuds/clawteam) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: niche (21) · Freshness: recent (71) · Maintenance: weak (0) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · MIT · May 2026</sub>

**CLI that lets a leader agent spawn and coordinate CLI coding agents.**

ClawTeam is a Python CLI (Typer) that lets a leader agent spawn worker agents such as Claude Code, Codex, nanobot or any CLI agent. Each worker gets its own git worktree, tmux window and identity. Coordination runs through CLI commands for tasks with dependencies and inbox messages, over a filesystem transport or optional ZeroMQ P2P, with a tmux board or web dashboard to watch progress.

- **+** Works with any CLI agent that runs in a directory, including Claude Code, Codex and nanobot
- **+** Each worker is isolated in a git worktree with real branches and diffs
- **+** No database or queue needed: filesystem and tmux, with optional ZeroMQ P2P
- **+** TOML team templates, e.g. a 7-agent hedge-fund team launched with one command
- **−** Requires tmux and a separately installed, working agent CLI; no Docker image
- **−** Headline results (8 H100 autoresearch run) are self-reported and need external GPUs
- **−** Leader behavior depends on the underlying agent following the injected skill and prompts
- **−** Last release v0.2.0 is from March 2026, while commits continue

<sub>no GPU · Needs Python 3.10+, tmux, git, a CLI coding agent (claude, codex, nanobot), ZeroMQ (optional, P2P) · Models: Claude Code, Codex, nanobot, OpenClaw, Cursor · port 8080 · [Repo](https://github.com/hkuds/clawteam) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clawteam/)</sub>

<a name="pandas-ai"></a>
### #&#8288;130 [pandas-ai](https://github.com/sinaptik-ai/pandas-ai) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: popular (78) · Freshness: quiet (12) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Oct 2025</sub>

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

<a name="rasa"></a>
### #&#8288;131 [rasa](https://github.com/rasahq/rasa) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: popular (74) · Freshness: quiet (9) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Dec 2025</sub>

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

<a name="ai-scientist"></a>
### #&#8288;132 [ai-scientist](https://github.com/sakanaai/ai-scientist) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: popular (65) · Freshness: quiet (13) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · Dec 2025</sub>

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

<a name="latentmas"></a>
### #&#8288;133 [latentmas](https://github.com/gen-verse/latentmas) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: niche (1) · Freshness: recent (79) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Jun 2026</sub>

**Multi-agent LLM reasoning that passes latent states between agents instead of text.**

LatentMAS is the reference code for an ICML 2026 paper on multi-agent systems in which agents hand off latent thoughts and KV-cache working memory rather than text. It works with Hugging Face models, with an optional hybrid vLLM backend, and ships single-agent and text-based multi-agent baselines. The repo reproduces experiments on GSM8K, AIME24/25, GPQA, ARC, MBPP+, HumanEval+ and MedQA.

- **+** Baseline, TextMAS and LatentMAS methods side by side for comparison on nine benchmarks
- **+** Paper reports about 50-80% fewer tokens and 3x-7x faster wall-clock than text multi-agent baselines
- **+** Training-free; works with any Hugging Face model, with optional vLLM backend
- **+** Example logs include full agent interaction traces
- **−** Experiment runner (run.py), not an installable library or agent-building SDK
- **−** vLLM path relies on patched vLLM internals and can differ numerically from HF results
- **−** Recommended vLLM setup uses two GPUs
- **−** No release published; example commands only cover Qwen3 models

<sub>GPU required · Needs PyTorch, Hugging Face Transformers, vLLM (optional), conda · Models: Hugging Face models, Qwen3-4B, Qwen3-8B, Qwen3-14B, vLLM · [Repo](https://github.com/gen-verse/latentmas) · [📖 Docs ↗](https://arxiv.org/abs/2511.20639) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/latentmas/)</sub>

<a name="autohedge"></a>
### #&#8288;134 [autohedge](https://github.com/the-swarm-corporation/autohedge) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: known (32) · Freshness: slowing (41) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.7k · MIT · Mar 2026</sub>

**Multi-agent Python pipeline that analyzes markets and trades on Solana.**

AutoHedge chains four agents (Director, Quant, Risk Manager, Execution) built on the Swarms framework. They generate a trading thesis, run technical analysis, size the position and place orders on Solana, with JSON-structured output and configurable logging. Coinbase and other exchanges are listed as planned, not available.

- **+** Clear four-stage pipeline: thesis, quant analysis, risk sizing, execution
- **+** Structured JSON output suitable for downstream systems
- **+** Installs with pip; built on the Swarms agent framework
- **+** Configurable logging for audit and debugging
- **−** Only Solana is supported; Coinbase and other exchanges are not yet available
- **−** Needs a wallet private key in environment variables to trade
- **−** Basic usage section is just `autohedge`, with no real code example
- **−** No backtesting or performance results documented

<sub>no GPU · Needs Swarms, Jupiter API key, OpenAI API key, Anthropic API key, Solana wallet private key · Models: OpenAI, Anthropic · [Repo](https://github.com/the-swarm-corporation/autohedge) · [🌐 Site ↗](https://swarms.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autohedge/)</sub>

<a name="paper2code"></a>
### #&#8288;135 [paper2code](https://github.com/going-doer/paper2code) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: niche (17) · Freshness: slowing (48) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · Apache-2.0 · Mar 2026</sub>

**Multi-agent pipeline that turns ML papers into code repositories.**

PaperCoder is the reference implementation of the Paper2Code ICLR 2026 paper. It takes a paper as PDF-derived JSON or LaTeX source and runs three LLM-agent stages (planning, analysis, code generation) to write a code repository. It works with the OpenAI API (o3-mini) or open models served through vLLM, and includes a benchmark dataset and a model-based evaluation script.

- **+** Runs against OpenAI API or local vLLM models, default DeepSeek-Coder-V2-Lite-Instruct
- **+** Accepts LaTeX source directly, skipping PDF conversion
- **+** Ships the Paper2Code benchmark on Hugging Face and reference-free and reference-based eval scripts
- **+** Saves planning, analyzing and coding artifacts per paper for inspection
- **−** PDF input needs a separate s2orc-doc2json and GROBID setup to produce JSON
- **−** Evaluation relies on o3-mini via the OpenAI API, so it is not fully local
- **−** Research code driven by shell scripts; no packaged CLI, release or Docker image
- **−** Scoped to ML papers; output quality varies by model and is not guaranteed

<sub>GPU optional · Needs OpenAI API, vLLM, s2orc-doc2json, GROBID, tiktoken · Models: OpenAI o3-mini, deepseek-ai/DeepSeek-Coder-V2-Lite-Instruct, vLLM-served open models · [Repo](https://github.com/going-doer/paper2code) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paper2code/)</sub>

<a name="eko"></a>
### #&#8288;136 [eko](https://github.com/fellouai/eko) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (17) · Freshness: slowing (47) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · MIT · Mar 2026</sub>

**JavaScript framework for natural-language agent workflows in browsers and Node.js.**

Eko is a TypeScript/JavaScript framework that turns a natural-language task into a multi-step agent workflow. It runs in browser extensions, web apps and Node.js, with built-in browser and file agents, MCP tool support, and configurable LLM providers such as Anthropic, Google, OpenAI and OpenAI-compatible endpoints. Version 3.0 added dependency-aware parallel execution, plus pause, resume and interrupt controls.

- **+** Runs in browser extensions, web apps and Node.js through one API
- **+** Native MCP support and custom agents or tools
- **+** Parallel agent execution, pause/resume and task_snapshot workflow recovery
- **+** Works with Anthropic, Google, OpenAI and OpenAI-compatible endpoints like Qwen
- **−** Browser use needs a backend proxy to keep API keys out of frontend code
- **−** Observable chain and native A2A are listed as not yet implemented
- **−** Upgrading from 3.x requires regenerating saved workflows to the new schema
- **−** Comparison table in the README is self-reported and unsourced

<sub>no GPU · Needs Node.js, pnpm, Playwright (Node.js example), LLM provider API key · Models: Anthropic, Google Gemini, OpenAI, OpenAI-compatible (Qwen, Doubao) · [Repo](https://github.com/fellouai/eko) · [📖 Docs ↗](https://eko.fellou.ai/docs) · [🌐 Site ↗](https://eko.fellou.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/eko/)</sub>

<a name="promptify"></a>
### #&#8288;137 [promptify](https://github.com/promptslab/promptify) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (13) · Freshness: slowing (49) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · Apache-2.0 · Mar 2026</sub>

**Python library for typed NLP tasks like NER and classification via LLMs.**

Promptify is a Python library that wraps LLM calls into task classes (NER, Classify, QA, Summarize, relation extraction, SQL generation) that return Pydantic objects. It routes requests through LiteLLM, so changing the model string switches between OpenAI, Anthropic, Ollama and other providers. It also includes batch and async calls, an evaluation module (precision, recall, F1, ROUGE) and token cost tracking.

- **+** Task classes return Pydantic objects instead of raw strings
- **+** LiteLLM backend: switching provider is a model string change, including ollama/
- **+** Built-in evaluation: precision, recall, F1, accuracy, exact match, ROUGE
- **+** Batch with max_concurrent, async acall(), and get_cost_summary() for token cost
- **−** No GitHub release published; install is from PyPI or a git URL
- **−** Evaluation metrics need the separate promptify[eval] extra
- **−** No web UI, server or hosted API; use is in-process Python only
- **−** No benchmark results given; accuracy depends on the chosen LLM

<sub>no GPU · Needs LiteLLM, Pydantic, LLM provider API key or local Ollama · Models: OpenAI, Anthropic, Google, Azure, Ollama · [Repo](https://github.com/promptslab/promptify) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/promptify/)</sub>

<a name="ai-data-science-team"></a>
### #&#8288;138 [ai-data-science-team](https://github.com/business-science/ai-data-science-team) <sub>score [17](../README.md#-how-we-rank "Score 17/100. Adoption: niche (20) · Freshness: slowing (37) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.5k · MIT · Jan 2026</sub>

**Python library of data science agents with a Streamlit pipeline app.**

A Python library of LangChain-based agents for data loading, cleaning, wrangling, feature engineering, visualization, SQL and H2O/MLflow modeling, plus a supervisor agent that coordinates them. It ships AI Pipeline Studio, a Streamlit app that records manual and AI steps as a visual pipeline with lineage and reproducible scripts. Works with OpenAI or local models through Ollama.

- **+** Agents cover the data science loop: cleaning, EDA, feature engineering, SQL, H2O modeling, MLflow
- **+** Pipeline Studio keeps lineage and exports reproducible scripts for each step
- **+** Runs with OpenAI or local Ollama models such as llama3.1:8b
- **+** Includes example apps: EDA Explorer, Pandas Data Analyst, Pipeline Studio
- **−** Beta status; README warns of breaking changes until 0.1.0
- **−** No Docker or compose files; install is a clone plus pip install -e
- **−** Model setup uses LangChain chat classes, so LangChain is required
- **−** Quickstart documents only OpenAI and Ollama as model providers

<sub>GPU optional · Needs Python 3.10+, Streamlit, OpenAI API key or Ollama, H2O, MLflow · Models: OpenAI, Ollama · [Repo](https://github.com/business-science/ai-data-science-team) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-data-science-team/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
