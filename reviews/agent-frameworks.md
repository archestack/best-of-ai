# 🧰 Agent frameworks and SDKs reviews · Best of Open-Source AI

Libraries for building agents and LLM apps in code: tool calling, planning, multi-agent setups and browser control. Back to the [leaderboard](../README.md#-agent-frameworks-and-sdks).

<sub>🌐 Also on the web: [Agent frameworks and SDKs on archestack.com](https://archestack.com/best-of-ai/agent-frameworks/), each project on its own page.</sub>

<a name="langchain"></a>
### 🥇 [langchain](https://github.com/langchain-ai/langchain) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 148k · MIT · Oct 2026</sub>

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
### 🥈 [browser-use](https://github.com/browser-use/browser-use) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 118k · MIT · Oct 2026</sub>

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

<a name="metagpt"></a>
### 🥉 [metagpt](https://github.com/foundationagents/metagpt) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: popular (57) · Freshness: quiet (25) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · MIT · Jan 2026</sub>

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

<a name="autogen"></a>
### #&#8288;4 [autogen](https://github.com/microsoft/autogen) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: known (37) · Freshness: recent (58) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 61k · CC-BY-4.0 · Apr 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
