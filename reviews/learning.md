# 📖 Learning and cookbooks reviews · Best of Open-Source AI

Courses, cookbooks and guides with runnable code, for learning to build with AI. Back to the [leaderboard](../README.md#-learning-and-cookbooks).

<sub>🌐 Also on the web: [Learning and cookbooks on archestack.com](https://archestack.com/best-of-ai/learning/), each project on its own page.</sub>

<a name="generative-ai-for-beginners"></a>
### 🥇 [generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 121k · MIT · Oct 2026</sub>

**21-lesson course on building generative AI apps in Python and TypeScript.**

A Microsoft Cloud Advocates course of 21 lessons, each a README with a short video and code samples, split into "Learn" concept lessons and "Build" lessons. Topics include prompt engineering, text and chat apps, embeddings search, image generation, function calling, RAG, agents, fine-tuning, and small, Mistral and Meta models. Code targets Azure OpenAI, OpenAI API, Microsoft Foundry Models or Foundry Local.

- **+** Build lessons ship code in both Python and TypeScript where possible
- **+** Covers RAG, function calling, agents, fine-tuning and security in one sequence
- **+** Lessons are independent, so you can start at any number
- **+** MIT license; translations into 50+ languages
- **−** Samples assume Azure OpenAI, OpenAI API or Foundry access, which may need paid accounts
- **−** Several lessons list video as coming soon
- **−** Cloning includes 50+ translations, so sparse checkout is needed for a small download
- **−** GitHub Models lessons are tied to a service retiring end of July 2026

<sub>no GPU · Needs Azure OpenAI Service, OpenAI API, Microsoft Foundry Models, Foundry Local, GitHub account · Models: Azure OpenAI, OpenAI, Microsoft Foundry Models, Foundry Local, Hugging Face open models · [Repo](https://github.com/microsoft/generative-ai-for-beginners) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/generative-ai-for-beginners/)</sub>

<a name="ai-engineering-from-scratch"></a>
### 🥈 [ai-engineering-from-scratch](https://github.com/rohitg00/ai-engineering-from-scratch) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 69k · MIT · Oct 2026</sub>

**Hands-on curriculum for building AI systems from math to agents.**

A course of 528 lessons across 20 phases, covering math foundations, ML fundamentals, LLM engineering, agents, tools and protocols, and production infrastructure. Lessons are runnable code in Python, TypeScript, Rust and Julia, with three graded projects: retrieval evaluation, agent trace debugging and a tool-call firewall. It can be followed on the website, from a local clone, or through tutor skills installed into a coding agent.

- **+** Lessons ship runnable code; the first ones need only python3 and no extra dependencies
- **+** Three staged projects with local graders (project_test.py --strict) and reference solutions
- **+** Tutor skills install via npx skills and save progress to LEARNING.md
- **+** Code in Python, TypeScript, Rust and Julia; README translated into 30+ languages
- **−** 528 lessons is a large scope; total study time is not stated in the visible README
- **−** Project starters fail by design until you implement the stages
- **−** Tutor skills need Node.js, npx and a skill-capable coding agent host
- **−** GPU and RAM needs for later phases are not stated in the visible README

<sub>Needs Python 3.10+, Node.js 22.18+ (TypeScript project), Rust (Tool Call Firewall project), npx (optional, tutor skills) · [Repo](https://github.com/rohitg00/ai-engineering-from-scratch) · [🌐 Site ↗](https://aiengineeringfromscratch.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-engineering-from-scratch/)</sub>

<a name="llms-from-scratch"></a>
### 🥉 [llms-from-scratch](https://github.com/rasbt/llms-from-scratch) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 106k · custom license · Oct 2026</sub>

**Code for the book on building a GPT-style LLM in PyTorch.**

Official code for the Manning book "Build a Large Language Model (From Scratch)". Notebooks and scripts implement tokenization, attention, a GPT model, pretraining, classification finetuning, instruction finetuning and LoRA in plain PyTorch, without external LLM libraries. Bonus folders add from-scratch Llama 3.2, Qwen3, Gemma 3, Olmo 3, KV cache, MoE and DPO.

- **+** Main chapter code runs on a conventional laptop and uses a GPU automatically if present
- **+** Plain PyTorch with no external LLM libraries, so every component is readable
- **+** Bonus material covers KV cache, GQA, MoE, DPO and several model architectures
- **+** Exercise solutions, a companion video course and CI tests on Linux, Windows and macOS
- **−** Tied to a print book; contributions extending main chapter code are not accepted
- **−** Produces a small educational model, not a production-grade LLM
- **−** License is reported as NOASSERTION; the README states no license terms
- **−** Video course and quiz PDF are hosted by the publisher, not in the repo

<sub>GPU optional · Needs PyTorch, Jupyter, Ollama (optional, ch07 evaluation) · Models: GPT-2, Llama 3.2, Qwen3, Gemma 3, Olmo 3 · [Repo](https://github.com/rasbt/llms-from-scratch) · [🌐 Site ↗](http://mng.bz/orYv) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llms-from-scratch/)</sub>

<a name="hello-agents"></a>
### #&#8288;4 [hello-agents](https://github.com/datawhalechina/hello-agents) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 83k · custom license · Oct 2026</sub>

**Chinese-language course on building LLM agents from scratch.**

A 16-chapter Chinese tutorial from Datawhale covering agent fundamentals, ReAct, Plan-and-Solve and Reflection, low-code platforms (Coze, Dify, n8n) and frameworks (AutoGen, AgentScope, LangGraph). Later chapters build a custom framework on the OpenAI API and cover memory, RAG, context engineering, MCP/A2A/ANP, Agentic-RL (SFT to GRPO) and evaluation. Chapter code is in the repo's code folder.

- **+** 16 chapters from theory to capstone, with runnable code in the code folder
- **+** Includes an Agentic-RL chapter going from SFT to GRPO training
- **+** Builds a custom agent framework on the OpenAI API, not only framework usage
- **+** Free online reading and PDF download, plus extra chapters on interviews and skills
- **−** Written in Chinese; an English README is linked separately
- **−** License is CC BY-NC-SA 4.0, which bars commercial use
- **−** Assumes basic Python and experience calling an LLM API
- **−** Hardware and model requirements for the exercises are unknown

<sub>Needs OpenAI-compatible LLM API · Models: OpenAI API · [Repo](https://github.com/datawhalechina/hello-agents) · [📖 Docs ↗](https://datawhalechina.github.io/hello-agents/) · [🌐 Site ↗](https://hello-agents.datawhale.cc) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hello-agents/)</sub>

<a name="ai-agents-for-beginners"></a>
### #&#8288;5 [ai-agents-for-beginners](https://github.com/microsoft/ai-agents-for-beginners) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 77k · MIT · Oct 2026</sub>

**18-lesson course on building AI agents with Microsoft Agent Framework.**

A Microsoft course of 18 lessons on building AI agents, each with a written README, a short video for most lessons, and Python code samples in Jupyter notebooks. Topics include tool use, agentic RAG, planning, multi-agent patterns, memory, MCP/A2A/NLWeb protocols, computer-use agents, local agents and securing agents. Samples use Microsoft Agent Framework with Microsoft Foundry Agent Service V2, and some also support OpenAI-compatible providers such as MiniMax.

- **+** Each lesson is standalone, so you can start at any topic
- **+** Covers design patterns plus MCP, A2A, NLWeb, memory and deployment
- **+** Text, short videos and runnable Python samples per lesson
- **+** 50+ language translations kept current by GitHub Action
- **−** Samples are built around Microsoft Agent Framework and Foundry, which need an Azure account
- **−** Some later lessons have no video
- **−** Cloning pulls large translation folders unless sparse checkout is used
- **−** Alternative provider support is only partial, per the README

<sub>no GPU · Needs Microsoft Foundry (Azure account), Microsoft Agent Framework, Microsoft Foundry Agent Service V2 · Models: Microsoft Foundry models, OpenAI-compatible providers (MiniMax) · [Repo](https://github.com/microsoft/ai-agents-for-beginners) · [📖 Docs ↗](https://github.com/microsoft/ai-agents-for-beginners/blob/master/00-course-setup/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-agents-for-beginners/)</sub>

<a name="openai-cookbook"></a>
### #&#8288;6 [openai-cookbook](https://github.com/openai/openai-cookbook) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: fair (51) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 77k · MIT · Oct 2026</sub>

**Example notebooks and guides for building with the OpenAI API.**

Collection of runnable Jupyter notebooks and guides showing common tasks with the OpenAI API. Most examples are in Python, and the README says the concepts apply to other languages. Running them requires an OpenAI account and an API key set as OPENAI_API_KEY. The guides are also browsable at cookbook.openai.com.

- **+** Maintained by OpenAI, so examples track the official API
- **+** Runnable notebooks; API key is read from OPENAI_API_KEY or a .env file
- **+** Also browsable as a site at cookbook.openai.com
- **+** MIT license
- **−** Requires an OpenAI account and API key; examples do not target local models
- **−** Most examples are Python only
- **−** README does not list topics, versions or per-notebook dependencies
- **−** No tagged releases

<sub>no GPU · Needs OpenAI API key, Jupyter · Models: OpenAI API models · [Repo](https://github.com/openai/openai-cookbook) · [📖 Docs ↗](https://platform.openai.com/docs/introduction) · [🌐 Site ↗](https://cookbook.openai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openai-cookbook/)</sub>

<a name="ai-for-beginners"></a>
### #&#8288;7 [ai-for-beginners](https://github.com/microsoft/ai-for-beginners) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 70k · MIT · Sep 2026</sub>

**12-week, 24-lesson AI curriculum with PyTorch and TensorFlow notebooks.**

A Microsoft course that teaches AI from symbolic and expert systems through neural networks, computer vision, NLP, genetic algorithms, reinforcement learning, multi-agent systems and ethics. Lessons pair text with Jupyter notebooks in PyTorch and/or TensorFlow/Keras, and several have labs. Translations into 50+ languages are generated by a GitHub Action.

- **+** Covers symbolic AI, deep learning, vision, NLP, RL and ethics in one ordered path
- **+** Most lessons have both PyTorch and TensorFlow/Keras notebooks
- **+** Labs for many lessons, plus a Binder badge to run notebooks in the browser
- **+** 50+ automated translations; MIT license
- **−** NLP stops at transformers/BERT and GPT basics; README admits it lags the state of the art
- **−** Excludes classic ML, cloud services and deep math; it points to other courses
- **−** Not every lesson has a lab; some notebooks are TensorFlow-only or PyTorch-only
- **−** Translations inflate clone size; sparse checkout is needed to skip them

<sub>Needs Jupyter, PyTorch, TensorFlow, Keras, OpenCV · [Repo](https://github.com/microsoft/ai-for-beginners) · [▶️ Demo ↗](https://mybinder.org/v2/gh/microsoft/ai-for-beginners/HEAD) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-for-beginners/)</sub>

<a name="claude-cookbooks"></a>
### #&#8288;8 [claude-cookbooks](https://github.com/anthropics/claude-cookbooks) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (41) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · MIT · Oct 2026</sub>

**Jupyter notebooks of copy-able Claude API recipes in Python.**

Anthropic's collection of runnable notebooks and guides for building with the Claude API. Recipes cover classification, RAG, summarization, tool use, vision, sub-agents, JSON mode, prompt caching, evals and cost optimization. Examples are mainly Python, and a Claude API key is required.

- **+** Covers tool use, RAG, vision, prompt caching and evals with runnable notebooks
- **+** Maintained by Anthropic, so examples target the Claude API directly
- **+** MIT licensed, snippets can be copied into your own projects
- **+** Includes third-party recipes such as Pinecone, Voyage AI embeddings and Wikipedia search
- **−** Requires a Claude API key; examples do not run on local models
- **−** Examples are primarily Python; other languages must be adapted
- **−** Recipe links in the README point to the older anthropic-cookbook repo path
- **−** Reference snippets, not an installable library or application

<sub>no GPU · Needs Claude API key, Pinecone (some recipes), Voyage AI (some recipes) · Models: Claude · [Repo](https://github.com/anthropics/claude-cookbooks) · [📖 Docs ↗](https://docs.claude.com/claude/docs/guide-to-anthropics-prompt-engineering-resources) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/claude-cookbooks/)</sub>

<a name="llm-course"></a>
### #&#8288;9 [llm-course](https://github.com/mlabonne/llm-course) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: widely used (82) · Freshness: slowing (41) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · Apache-2.0 · Feb 2026</sub>

**Free LLM course with roadmaps and Colab notebooks for fine-tuning and quantization.**

A three-part course covering LLM fundamentals (math, Python, neural networks), an LLM Scientist track on building models, and an LLM Engineer track on building and deploying applications. It pairs roadmaps and curated links with Colab notebooks and articles on fine-tuning (Unsloth, ORPO, DPO, QLoRA, Axolotl), quantization (GGUF, GPTQ, EXL2) and model merging with MergeKit.

- **+** Runnable Colab notebooks for fine-tuning, quantization and merging, most with a linked article
- **+** Separate tracks for fundamentals, model building and application deployment
- **+** Quantization notebooks cover GGUF, GPTQ, EXL2, AWQ and HQQ
- **+** Free to use under Apache-2.0
- **−** Mostly curated external links rather than self-contained lessons
- **−** Several notebooks target older models such as Llama 2 and Mistral-7b
- **−** Notebooks run on Google Colab or RunPod, not a documented local setup
- **−** Coverage reflects one author's selection of topics and resources

<sub>GPU optional · Needs Google Colab, RunPod, Hugging Face · Models: Llama 3.1, Llama 3, Llama 2, Mistral-7b, CodeLlama · [Repo](https://github.com/mlabonne/llm-course) · [📖 Docs ↗](https://deepwiki.com/mlabonne/llm-course/) · [🌐 Site ↗](https://mlabonne.github.io/blog) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-course/)</sub>

<a name="made-with-ml"></a>
### #&#8288;10 [made-with-ml](https://github.com/gokumohandas/made-with-ml) <sub>score [29](../README.md#-how-we-rank "Score 29/100. Adoption: known (34) · Freshness: recent (62) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Mar 2026</sub>

**MLOps course with code for training, tuning, and serving a text classifier.**

A course repository that walks through building a text classifier end to end: a Jupyter notebook, then refactored Python scripts for training, tuning, evaluation, inference and serving. It uses Ray for distributed workloads, MLflow for experiment tracking, pytest for code, data and model tests, and Anyscale Jobs and Services for production deployment.

- **+** Covers the full path: notebook, scripts, tests, MLflow tracking, Ray Serve, CI/CD
- **+** Runs on a laptop without a GPU, with configurable worker counts
- **+** Separate pytest suites for code, data and trained models
- **+** Plain Python scripts with documented CLI arguments for each workload
- **−** Production section depends on Anyscale (account, CLI token, S3 upload paths)
- **−** Example task is a small text classifier, not an LLM application
- **−** Setup is built around Ray; other stacks need adaptation
- **−** README promotes a paid live cohort

<sub>GPU optional · Needs Ray, MLflow, Anyscale, AWS S3, pytest, pre-commit · port 8000 · [Repo](https://github.com/gokumohandas/made-with-ml) · [📖 Docs ↗](https://madewithml.com/) · [🌐 Site ↗](https://madewithml.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/made-with-ml/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
