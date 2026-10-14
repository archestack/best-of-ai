# 🧰 Agent frameworks and SDKs reviews · Best of Open-Source AI

Libraries for building agents and LLM apps in code: tool calling, planning, multi-agent setups and browser control. Back to the [leaderboard](../README.md#-agent-frameworks-and-sdks).

<sub>🌐 Also on the web: [Agent frameworks and SDKs on archestack.com](https://archestack.com/best-of-ai/agent-frameworks/), each project on its own page.</sub>

<a name="langchain"></a>
### 🥇 [langchain](https://github.com/langchain-ai/langchain) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 148k · MIT · Oct 2026</sub>

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
### 🥈 [browser-use](https://github.com/browser-use/browser-use) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 118k · MIT · Oct 2026</sub>

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

<a name="crewai"></a>
### 🥉 [crewai](https://github.com/crewaiinc/crewai) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · MIT · Oct 2026</sub>

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

<a name="openai-agents-python"></a>
### #&#8288;4 [openai-agents-python](https://github.com/openai/openai-agents-python) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Oct 2026</sub>

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

<a name="agno"></a>
### #&#8288;5 [agno](https://github.com/agno-agi/agno) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Oct 2026</sub>

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

<a name="mastra"></a>
### #&#8288;6 [mastra](https://github.com/mastra-ai/mastra) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · custom license · Oct 2026</sub>

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

<a name="llama-index"></a>
### #&#8288;7 [llama_index](https://github.com/run-llama/llama_index) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 52k · MIT · Oct 2026</sub>

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

<a name="langgraph"></a>
### #&#8288;8 [langgraph](https://github.com/langchain-ai/langgraph) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · MIT · Oct 2026</sub>

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
### #&#8288;9 [deepagents](https://github.com/langchain-ai/deepagents) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · MIT · Oct 2026</sub>

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

<a name="agentscope"></a>
### #&#8288;10 [agentscope](https://github.com/agentscope-ai/agentscope) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Oct 2026</sub>

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

<a name="semantic-kernel"></a>
### #&#8288;11 [semantic-kernel](https://github.com/microsoft/semantic-kernel) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · MIT · Oct 2026</sub>

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

<a name="openmanus"></a>
### #&#8288;12 [openmanus](https://github.com/foundationagents/openmanus) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (71) · Freshness: recent (70) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Aug 2026</sub>

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

<a name="smolagents"></a>
### #&#8288;13 [smolagents](https://github.com/huggingface/smolagents) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (30) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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

<a name="autogen"></a>
### #&#8288;14 [autogen](https://github.com/microsoft/autogen) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (79) · Freshness: recent (58) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 61k · CC-BY-4.0 · Apr 2026</sub>

**Python and .NET framework for multi-agent apps, now in maintenance mode.**

AutoGen is a layered framework for building multi-agent applications: a Core API for event-driven message passing, an AgentChat API for two-agent and group-chat patterns, and an Extensions API for model clients, MCP tools and code execution. It also ships AutoGen Studio, a no-code prototyping UI on port 8080, and AgentBench. The project is in maintenance mode and community managed; Microsoft points new users to Microsoft Agent Framework.

- **+** Layered design: Core, AgentChat and Extensions APIs let you pick the abstraction level
- **+** Core runtime supports local and distributed execution, with Python and .NET packages
- **+** MCP tool support through McpWorkbench, e.g. the Playwright MCP server
- **+** Includes AutoGen Studio for no-code prototyping and a benchmarking suite
- **−** Maintenance mode: no new features, only bug fixes, security patches and docs
- **−** Maintainers recommend Microsoft Agent Framework for new projects
- **−** AutoGen Studio is explicitly not production-ready and has no built-in authentication
- **−** Support is community-only and response times may be slow

<sub>no GPU · Needs Python 3.10+, OpenAI API key (for the quickstart samples), Node.js/npx (for the Playwright MCP example) · Models: OpenAI, Azure OpenAI · port 8080 · [Repo](https://github.com/microsoft/autogen) · [📖 Docs ↗](https://microsoft.github.io/autogen/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autogen/)</sub>

<a name="metagpt"></a>
### #&#8288;15 [metagpt](https://github.com/foundationagents/metagpt) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: widely used (85) · Freshness: quiet (25) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · MIT · Jan 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
