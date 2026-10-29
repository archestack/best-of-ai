# 🕸️ Data and scraping for AI reviews · Best of Open-Source AI

Tools that turn web pages, PDFs and documents into clean text or structured data that models can use. Back to the [leaderboard](../README.md#%EF%B8%8F-data-and-scraping-for-ai).

<sub>🌐 Also on the web: [Data and scraping for AI on archestack.com](https://archestack.com/best-of-ai/data-tools/), each project on its own page.</sub>

<a name="mineru"></a>
### 🥇 [mineru](https://github.com/opendatalab/mineru) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 83k · custom license · Oct 2026</sub>

**Document parser that converts PDFs, images and Office files to Markdown and JSON.**

MinerU parses PDFs, scanned images, Office, OpenDocument, EPUB, OFD, HTML and CSV files into Markdown, HTML, LaTeX, DOCX and structured content lists. It offers four parsing tiers (flash, basic, standard, advanced), a local document library with search, and page/block locators for citations. It ships a CLI, Python SDK, API, router and Gradio WebUI, plus an agent skill.

- **+** Handles scanned PDFs, tables and formulas, with four quality tiers from fast preview to advanced
- **+** Stable doc/tier/page/block locators allow paged reading and citation of long documents
- **+** Small models run on ONNX CPU; the VLM can run on llama.cpp, vLLM or LMDeploy
- **+** Documents are not uploaded to the official service unless remote parsing is configured
- **−** Office, HTML, EPUB, OFD and CSV files only get flash-tier parsing; higher tiers are PDF and image only
- **−** Docker deployment for non-NVIDIA devices is pending an update
- **−** Highest throughput needs an NVIDIA GPU and mineru[full]; Windows needs torch installed separately
- **−** License is reported as NOASSERTION, so terms need checking before use

<sub>GPU optional · Docker + Compose · Needs Python >=3.10,<3.15, llama.cpp, vLLM or LMDeploy (VLM runtime), ONNX or Torch · Models: MinerU VLM, ONNX small models, Torch small models, llama.cpp, vLLM · [Repo](https://github.com/opendatalab/mineru) · [▶️ Demo ↗](https://huggingface.co/spaces/opendatalab/MinerU) · [📖 Docs ↗](https://opendatalab.github.io/MinerU/) · [🌐 Site ↗](https://mineru.net/OpenSourceTools/Extractor?source=github) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mineru/)</sub>

<a name="docling"></a>
### 🥈 [docling](https://github.com/docling-project/docling) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 70k · MIT · Oct 2026</sub>

**Python library and CLI that converts PDFs, Office files and more into structured text.**

Docling parses PDF, DOCX, PPTX, XLSX, HTML, EPUB, images, audio and other formats into a unified DoclingDocument, with PDF layout, reading order, table structure, code and formula recognition. It exports to Markdown, HTML, DocLang, DocTags and lossless JSON. It runs locally via a CLI or Python API, with OCR, VLM support (GraniteDocling), an MCP server and a docling-serve API server.

- **+** Wide input coverage: PDF, Office, ODF, EPUB, email, Apple iWork, XBRL, audio, video
- **+** Local execution suits sensitive data and air-gapped environments
- **+** Integrations with LangChain, LlamaIndex, Crew AI and Haystack
- **+** Ships a CLI, Python API, MCP server and docling-serve HTTP server
- **−** Hardware requirements (RAM, GPU) are not stated in the README
- **−** Individual models carry their own licenses, separate from the MIT codebase
- **−** Metadata extraction and chemistry understanding are listed as coming soon
- **−** Requires Python 3.10 or higher; 3.9 support was dropped in 2.70.0

<sub>GPU optional · Docker · Models: GraniteDocling, VLMs, OCR engines, ASR models · [Repo](https://github.com/docling-project/docling) · [📖 Docs ↗](https://docling-project.github.io/docling/) · [🌐 Site ↗](https://docling-project.github.io/docling/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/docling/)</sub>

<a name="markitdown"></a>
### 🥉 [markitdown](https://github.com/microsoft/markitdown) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 193k · MIT · Oct 2026</sub>

**Python library and CLI that converts office files, PDFs and audio to Markdown.**

MarkItDown converts PDF, Word, PowerPoint, Excel, images, audio, HTML, CSV/JSON/XML, ZIP, EPub and YouTube URLs into Markdown that keeps headings, lists, tables and links. It runs as a Python library or the `markitdown` CLI. It can optionally call an OpenAI-compatible LLM for image descriptions, or Azure Document Intelligence and Content Understanding for higher-quality extraction. Output targets LLM pipelines, not human-facing fidelity.

- **+** Covers many formats (PDF, DOCX, PPTX, XLSX, EPub, ZIP, YouTube) through one convert call
- **+** Built-in converters run offline; install only needed formats via extras like [pdf,docx,pptx]
- **+** Plugin system, plus a markitdown-ocr plugin that uses an LLM vision client for embedded images
- **+** Optional Azure Document Intelligence and Content Understanding backends with YAML front matter fields
- **−** Not meant for high-fidelity conversion for human reading, per the README
- **−** Runs with the calling process's privileges; untrusted input must be sanitized by the caller
- **−** Azure backends are billable; Content Understanding is the only route for video
- **−** Repo accepts no web server, REST API or GUI; those must be separate projects

<sub>no GPU · Docker · Needs Python 3.10-3.14, Azure Document Intelligence (optional), Azure Content Understanding (optional), OpenAI-compatible client (optional) · Models: OpenAI-compatible vision models (gpt-4o in examples) · [Repo](https://github.com/microsoft/markitdown) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/markitdown/)</sub>

<a name="opendataloader-pdf"></a>
### #&#8288;4 [opendataloader-pdf](https://github.com/opendataloader-project/opendataloader-pdf) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

**PDF parser that outputs Markdown, JSON with bounding boxes, and Tagged PDF.**

Java-based PDF parser with Python, Node.js and Java SDKs. It extracts Markdown, JSON with per-element bounding boxes, and HTML, using XY-Cut++ reading order in a deterministic local mode. An optional hybrid mode sends complex pages to a Docling-based backend for OCR, borderless tables, LaTeX formulas and chart descriptions. It also auto-tags untagged PDFs into Tagged PDF.

- **+** Bounding boxes and element types for every extracted item, usable for source citations
- **+** Local mode needs no GPU; README reports 0.015 s/page
- **+** Hybrid mode adds OCR, LaTeX formulas and chart descriptions; OCR engine is selectable
- **+** Reports 0.907 overall on its own 200-PDF benchmark, ahead of docling and marker
- **−** Requires Java 11+ on the host, even when using the Python package
- **−** Each convert() call spawns a JVM, so calls must be batched
- **−** PDF/UA export and accessibility studio are enterprise-only
- **−** Does not process Word, Excel or PowerPoint; benchmark is run by the project itself

<sub>no GPU · Needs Java 11+, Python 3.10+ (Python SDK), Docling backend (hybrid mode) · Models: Docling, EasyOCR, RapidOCR, Tesseract, SmolVLM (256M) · port 5002 · [Repo](https://github.com/opendataloader-project/opendataloader-pdf) · [📖 Docs ↗](https://opendataloader.org/docs/quick-start-python) · [🌐 Site ↗](https://opendataloader.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opendataloader-pdf/)</sub>

<a name="crawl4ai"></a>
### #&#8288;5 [Crawl4AI](https://github.com/unclecode/crawl4ai) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 86k · Apache-2.0 · Oct 2026</sub>

**Async Python web crawler that outputs LLM-ready Markdown and structured JSON.**

Crawl4AI drives Playwright browsers (Chromium, Firefox, WebKit) to fetch pages and convert them to filtered Markdown or JSON, using CSS/XPath schemas or an LLM. It ships as a pip library, a `crwl` CLI and a Docker REST server with MCP, a dashboard and a playground on port 11235. A separate hosted cloud adds search, SERP and answer endpoints.

- **+** Schema-based CSS/XPath extraction works without any LLM call
- **+** Fit Markdown filters (pruning, BM25, LLM) strip menus and boilerplate
- **+** Deep crawl with BFS, DFS and score-ordered strategies, resumable after crashes
- **+** Docker server has REST endpoints, MCP and token auth by default
- **−** Search, SERP and answer endpoints exist only in the hosted cloud
- **−** Self-hosted bot-wall handling relies on your own proxies and settings
- **−** Needs a Playwright browser install, so heavier than plain HTTP scrapers
- **−** LLM extraction requires an external provider key or a local model endpoint

<sub>no GPU · Docker + Compose · Needs Playwright browsers (Chromium), Docker (optional), LLM provider via LiteLLM (optional) · Models: any LiteLLM provider (OpenAI, Ollama) · port 11235 · [Repo](https://github.com/unclecode/crawl4ai) · [📖 Docs ↗](https://docs.crawl4ai.com) · [🌐 Site ↗](https://crawl4ai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/crawl4ai/)</sub>

<a name="firecrawl"></a>
### #&#8288;6 [Firecrawl](https://github.com/firecrawl/firecrawl) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 197k · AGPL-3.0 · Oct 2026</sub>

**Web API that turns sites and searches into markdown or JSON for LLMs.**

Firecrawl exposes REST endpoints to search the web, scrape a URL, crawl a site, map its URLs, batch-scrape, parse documents (PDF, DOCX) and run page actions such as click and scroll. Output is markdown, HTML, screenshots or schema-based JSON. SDKs cover Python, Node.js, Go, Java, Elixir, Rust and Ruby, plus a CLI and an MCP server. The README examples use the hosted API with a key; self-hosting details are not in the excerpt.

- **+** Endpoints for search, scrape, crawl, map, batch scrape and document parsing
- **+** Official SDKs for seven languages, plus a CLI and MCP server
- **+** Outputs markdown, HTML, screenshots or schema-based structured JSON
- **+** Page actions and an interact endpoint for JS-heavy pages
- **−** README examples target the hosted API and require an API key
- **−** AGPL-3.0 license restricts use in closed-source network services
- **−** Agent endpoint runs the spark-2 model; self-hosted availability is unknown
- **−** Self-hosting requirements (RAM, ports, proxies) not stated in the README excerpt

<sub>Compose · Needs Firecrawl API key (hosted service) · Models: spark-2 · [Repo](https://github.com/firecrawl/firecrawl) · [▶️ Demo ↗](https://firecrawl.dev/playground) · [📖 Docs ↗](https://docs.firecrawl.dev) · [🌐 Site ↗](https://firecrawl.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/firecrawl/)</sub>

<a name="agent-reach"></a>
### #&#8288;7 [agent-reach](https://github.com/panniantong/agent-reach) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 106k · MIT · Oct 2026</sub>

**CLI that gives coding agents read access to login-gated and Chinese web platforms.**

Agent Reach is a Python CLI that wraps upstream tools such as bili-cli, yt-dlp, Jina Reader and Exa behind one command format: `agent-reach <channel> <action>`. It covers Bilibili, V2EX, GitHub, YouTube, Xiaohongshu, Xueqiu, Reddit, Twitter and others, trying an ordered list of tools per action with fallbacks. It is read-only, and login-gated sites use a dedicated background browser that copies your Chrome session for that site.

- **+** Covers Chinese platforms (Bilibili, Xiaohongshu, V2EX, Xueqiu) that generic agent search handles poorly
- **+** Per-action ordered tool list with automatic fallback when an upstream tool breaks
- **+** Read-only by design: no posting, commenting, liking or messaging
- **+** All tools, logins and settings live in `~/.agent-reach/`, so removal is contained
- **−** Twitter, Facebook and Instagram channels are labeled experimental and may break at any time
- **−** Login-gated channels copy your Chrome session, usually the main account; README advises a spare account
- **−** YouTube and Xiaoyuzhou transcription needs a Groq or OpenAI key
- **−** README is mainly in Chinese; the English docs are a separate file

<sub>no GPU · Needs uv, Python 3.10+, bili-cli, yt-dlp, Jina Reader, Exa, Groq or OpenAI API key (transcription) · [Repo](https://github.com/panniantong/agent-reach) · [📖 Docs ↗](https://github.com/Panniantong/Agent-Reach/blob/main/docs/README_en.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-reach/)</sub>

<a name="labelme"></a>
### #&#8288;8 [labelme](https://github.com/wkentaro/labelme) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · GPL-3.0 · Oct 2026</sub>

**Desktop image annotation tool with polygon labeling and SAM-assisted masks.**

Labelme is a Qt (PySide6) desktop app for annotating images with polygon, rectangle, circle, line and point shapes, saved as JSON files. It exports VOC and COCO datasets and offers AI-assisted annotation: SAM and EfficientSAM for point-to-polygon, YOLO-world and SAM3 for text-to-annotation. It is an application, not a library, with no stable Python API.

- **+** Supports polygon, rectangle, circle, line, point shapes plus image-level flags
- **+** Exports VOC and COCO datasets for segmentation and detection
- **+** Built-in SAM, EfficientSAM, YOLO-world and SAM3 assisted labeling
- **+** Installs with pip; UI translated into 20 languages
- **−** v7 requires Python 3.12+ and PySide6; Qt5 users must pin labelme<7
- **−** No stable Python API; internal modules were made private in v7
- **−** Standalone no-Python app is a paid one-time purchase
- **−** Single-user desktop GUI; no team or review workflow described

<sub>Needs Python 3.12+, PySide6 (Qt6) · Models: SAM, EfficientSAM, YOLO-world, SAM3 · [Repo](https://github.com/wkentaro/labelme) · [📖 Docs ↗](https://www.labelme.io/docs/install-labelme-terminal) · [🌐 Site ↗](https://labelme.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/labelme/)</sub>

<a name="langextract"></a>
### #&#8288;9 [langextract](https://github.com/google/langextract) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Oct 2026</sub>

**Python library that extracts grounded structured data from text using LLMs.**

LangExtract is a Python library that takes a prompt and a few examples and uses an LLM to pull structured entities and attributes out of unstructured text. Each extraction is mapped to its character span in the source, and results can be rendered as an interactive HTML review page. Long documents are handled with chunking, parallel workers and multiple passes, using Gemini, OpenAI or local Ollama models.

- **+** Each extraction carries a char_interval into the source; ungrounded results get None
- **+** Long-document handling via chunking, max_workers and extraction_passes for recall
- **+** Supports Gemini, OpenAI (with Batch API), Vertex AI batch and local Ollama models
- **+** Plugin system for custom model providers, plus a community provider registry
- **−** Needs few-shot examples; misaligned examples trigger prompt alignment warnings
- **−** Ollama provider does not support output_schema
- **−** Controlled generation is described for supported models like Gemini; quality depends on the LLM
- **−** Library only, no server or UI; visualization is a static HTML file

<sub>no GPU · Docker · Needs Gemini, OpenAI or Vertex AI API key, or a local Ollama server · Models: Gemini, OpenAI, Ollama, Vertex AI, OpenAI-compatible endpoints · [Repo](https://github.com/google/langextract) · [▶️ Demo ↗](https://google-langextract.hf.space/) · [📖 Docs ↗](https://github.com/google/langextract/blob/main/docs/examples/longer_text_example.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langextract/)</sub>

<a name="scrapegraph-ai"></a>
### #&#8288;10 [scrapegraph-ai](https://github.com/scrapegraphai/scrapegraph-ai) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Oct 2026</sub>

**Python library that builds LLM-driven scraping pipelines from a prompt and a URL.**

ScrapeGraphAI is a Python library that extracts structured data from websites and local files (XML, HTML, JSON, Markdown) given a natural-language prompt. It provides graph pipelines such as SmartScraperGraph, SearchGraph and ScriptCreatorGraph, with multi-page variants that call the LLM in parallel. It works with OpenAI, Groq, Azure, Gemini, MiniMax or local models through Ollama, and uses Playwright to fetch pages.

- **+** Prompt plus URL returns a JSON dict; no per-site selectors to write
- **+** Runs against local Ollama models or hosted APIs by changing the llm config
- **+** Several pipelines: single page, multi-page, search results, Python script generation
- **+** Multi-page graph variants run LLM calls in parallel
- **−** Proxies, anti-bot handling and scaling are left to the user in the open-source version
- **−** Needs a separate `playwright install` step to fetch page content
- **−** Anonymous telemetry is on by default; opt out via SCRAPEGRAPHAI_TELEMETRY_ENABLED=false
- **−** README steers users to the paid managed API for crawl and monitor features

<sub>GPU optional · Docker + Compose · Needs Playwright, Ollama (for local models), LLM provider API key (for hosted models) · Models: Ollama, OpenAI, Groq, Azure, Gemini · [Repo](https://github.com/scrapegraphai/scrapegraph-ai) · [📖 Docs ↗](https://docs.scrapegraphai.com/introduction) · [🌐 Site ↗](https://scrapegraphai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scrapegraph-ai/)</sub>

<a name="tesseract"></a>
### #&#8288;11 [tesseract](https://github.com/tesseract-ocr/tesseract) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 77k · Apache-2.0 · Oct 2026</sub>

**OCR engine and command-line tool with LSTM recognition for 100+ languages.**

Tesseract is a C++ OCR engine (libtesseract) with a tesseract command-line program. Version 4 and later use an LSTM line-recognition engine, and the legacy Tesseract 3 engine is available with --oem 0. It reads PNG, JPEG and TIFF through Leptonica and writes plain text, hOCR, PDF, TSV, ALTO and PAGE.

- **+** Recognizes more than 100 languages with UTF-8 support using downloadable traineddata files
- **+** Outputs plain text, hOCR, PDF, invisible-text PDF, TSV, ALTO and PAGE
- **+** C and C++ APIs plus a CLI; wrappers for other languages are listed in the docs
- **+** Can be trained for additional languages; Apache-2.0 licensed
- **−** No GUI included; third-party front-ends are needed
- **−** Accuracy depends on input image quality; preprocessing is often required
- **−** Leptonica opens images only, not documents like PDF
- **−** Legacy engine mode needs separate legacy-compatible traineddata files

<sub>no GPU · Needs Leptonica, traineddata files · Models: LSTM traineddata, legacy Tesseract 3 traineddata · [Repo](https://github.com/tesseract-ocr/tesseract) · [📖 Docs ↗](https://tesseract-ocr.github.io/tessdoc/) · [🌐 Site ↗](https://tesseract-ocr.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tesseract/)</sub>

<a name="moli"></a>
### #&#8288;12 [moli](https://github.com/lexmount/moli) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Oct 2026</sub>

**Headless browser in Rust for AI agents, with CDP and WebDriver support.**

Moli is a standalone browser kernel written in Rust (V8, Stylo, Taffy, Parley), not a Chromium wrapper. The CLI fetches pages as HTML, Markdown, JSON or a semantic tree, and `moli serve` exposes CDP, WebDriver Classic and WebDriver BiDi on one endpoint. Layout and painting run only when `--layout` is set and an operation needs them.

- **+** Single binary serves CDP, WebDriver Classic and BiDi; no ChromeDriver or Chrome install needed
- **+** Reported median RSS of 73 MiB on a 192-URL crawl, versus 773 MiB for Chrome Headless
- **+** CLI dumps Markdown, semantic tree text, PNG screenshots and PDF directly
- **+** Playwright connects over CDP; Linux, macOS and Windows supported
- **−** Lexbench pass rate is 81.9% against Chrome's 99.8%, so some sites will fail
- **−** No GUI, GPU compositor, or high-fidelity Canvas, WebGL or media playback
- **−** Screenshot and print modes are partial; real layout needs the `--layout` flag
- **−** Benchmarks are published by the project's own authors

<sub>no GPU · Needs libcurl · port 9222 · [Repo](https://github.com/lexmount/moli) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moli/)</sub>

<a name="cocoindex"></a>
### #&#8288;13 [cocoindex](https://github.com/cocoindex-io/cocoindex) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Oct 2026</sub>

**Incremental Python pipelines that keep vector indexes and agent context fresh.**

CocoIndex is a Python framework with a Rust core for declaring how source data (files, code, PDFs, Slack, databases) maps to a target such as Postgres/pgvector or LanceDB. It memoizes by input and code hash, so after a change only the affected rows are recomputed and re-embedded. It also tracks lineage from each target row back to its source.

- **+** Memoization keyed on input and code hash re-embeds only changed files
- **+** Pipelines are plain Python functions, not a DAG or YAML config
- **+** Per-row lineage traces target vectors back to source content
- **+** Rust core with retries, back-off and dead-letter queues, per the README
- **−** Library only: no UI, you write and run the pipeline code yourself
- **−** Python 3.10-3.13 supported; other languages are not mentioned
- **−** Quickstart needs an external target store such as Postgres
- **−** README is marketing-heavy; connector and scale details are only in the docs

<sub>Needs Python 3.10-3.13, Postgres (pgvector) or LanceDB as target · Models: sentence-transformers · [Repo](https://github.com/cocoindex-io/cocoindex) · [📖 Docs ↗](https://cocoindex.io/docs) · [🌐 Site ↗](https://cocoindex.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cocoindex/)</sub>

<a name="label-studio"></a>
### #&#8288;14 [label-studio](https://github.com/humansignal/label-studio) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

**Multi-user data labeling tool for audio, text, images, video and time series.**

Label Studio is a web-based annotation tool for preparing and correcting ML training data across images, audio, text, HTML, video and time series. Labeling interfaces are defined in a configuration language, with included templates, and results export to various model formats. It can connect to an ML backend for pre-labeling, online learning and active learning, and has a REST API for pipelines.

- **+** Handles images, audio, text, HTML, video and time series in one instance
- **+** Installs via pip, Docker, or a Compose stack with Nginx and PostgreSQL
- **+** ML backend SDK supports pre-labeling, online learning and active learning
- **+** Imports from S3, GCS and files; REST API for pipeline integration
- **−** Default install stores data in SQLite; PostgreSQL needs the Compose setup
- **−** Some features are tied to paid editions; README links a comparison page
- **−** ML integration needs a separately run backend server
- **−** Windows install requires manually downloading a prebuilt lxml wheel

<sub>no GPU · Docker + Compose · Needs PostgreSQL (optional, Compose), Nginx (optional, Compose), MinIO (optional) · Models: Custom ML backends via Label Studio ML SDK · port 8080 · [Repo](https://github.com/humansignal/label-studio) · [📖 Docs ↗](https://labelstud.io/guide/) · [🌐 Site ↗](https://labelstud.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/label-studio/)</sub>

<a name="unstructured"></a>
### #&#8288;15 [unstructured](https://github.com/unstructured-io/unstructured) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

**Python library that parses PDFs, Office files and HTML into typed elements.**

The unstructured library parses documents such as PDF, HTML, Word, email and images into typed elements (titles, narrative text, tables). A single `partition` function detects the file type and routes it to a format-specific parser. It installs from PyPI with per-format extras or runs from a Docker image, and some formats need system packages such as poppler, tesseract and libreoffice.

- **+** One `partition` call auto-detects file type and dispatches to format-specific parsers
- **+** Per-format pip extras (docx, pptx, pdf) keep installs smaller for narrow use cases
- **+** Apache-2.0 licensed; multi-platform Docker images for x86_64 and Apple silicon
- **+** Batch ingestion and connectors are available through the separate unstructured-ingest project
- **−** README's own benchmark lists table cell content accuracy of 0.426 versus 0.866 for the paid API
- **−** PDF, image and Office parsing needs system packages: poppler, tesseract, libreoffice
- **−** Sends anonymous telemetry by default; opt out with DO_NOT_TRACK or SCARF_NO_ANALYTICS
- **−** Highest-quality output is only in the hosted Transform API, not this library

<sub>Docker · Needs poppler-utils, tesseract-ocr, libmagic-dev, libreoffice · [Repo](https://github.com/unstructured-io/unstructured) · [📖 Docs ↗](https://docs.unstructured.io) · [🌐 Site ↗](https://unstructured.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unstructured/)</sub>

<a name="x-anylabeling"></a>
### #&#8288;16 [x-anylabeling](https://github.com/cvhub520/x-anylabeling) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · GPL-3.0 · Oct 2026</sub>

**Desktop app for AI-assisted annotation of images, video, text and point clouds.**

X-AnyLabeling is a cross-platform desktop annotation tool for building datasets for detection, segmentation, pose, OCR, tracking, VQA and 3D point clouds. It integrates models such as YOLO variants, SAM 1/2/3, Grounding DINO and several VLMs for auto-labeling, run locally via ONNX Runtime, TensorRT or OpenCV DNN, or remotely via vLLM, SGLang or its own server. It imports and exports COCO, VOC, YOLO, DOTA, MOT and others.

- **+** Wide model library: YOLO family, SAM 1/2/3, Grounding DINO, RF-DETR, PP-OCR, Qwen3-VL
- **+** Exports COCO, VOC, YOLO, DOTA, MOT, PPOCR, ShareGPT and other formats
- **+** Covers many tasks in one tool: boxes, polygons, rotated boxes, tracking, OCR, VQA, 3D point clouds
- **+** Runs on Windows, Linux and macOS; remote inference via X-AnyLabeling-Server, vLLM or SGLang
- **−** GPL-3.0 license imposes copyleft terms on derived or redistributed code
- **−** Requires Python 3.11+ for source or PyPI install
- **−** RAM and VRAM requirements are not stated in the README
- **−** Contributions require signing a Contributor License Agreement

<sub>GPU optional · Needs ONNX Runtime, TensorRT, OpenCV DNN, vLLM, SGLang · Models: ONNX, YOLO, SAM, Grounding DINO, Qwen3-VL · [Repo](https://github.com/cvhub520/x-anylabeling) · [📖 Docs ↗](https://xanylabeling.com/docs/x-anylabeling/user_guide) · [🌐 Site ↗](https://xanylabeling.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/x-anylabeling/)</sub>

<a name="paddleocr"></a>
### #&#8288;17 [paddleocr](https://github.com/paddlepaddle/paddleocr) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: weak (21) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 92k · Apache-2.0 · Sep 2026</sub>

**OCR and document parsing toolkit that outputs Markdown and JSON from PDFs and images.**

PaddleOCR runs text recognition (PP-OCRv6) and document parsing (PaddleOCR-VL 0.9B VLM, PP-StructureV3) on PDFs and images, producing Markdown or JSON for RAG pipelines. It runs on CPU, NVIDIA GPU, Kunlunxin XPU and other accelerators, with ONNX, OpenVINO, TensorRT and Transformers backends. Models are on HuggingFace and ModelScope.

- **+** Three PP-OCRv6 tiers (1.5M, 7.7M, 34.5M params) cover edge to server
- **+** One PP-OCRv6 model handles 50 languages; PaddleOCR-VL covers 111
- **+** Outputs Markdown, JSON and DOCX; PP-StructureV3 returns table cell and text coordinates
- **+** Multiple inference backends: Paddle, Transformers, ONNX Runtime, OpenVINO, TensorRT, plus C++ deployment
- **−** Depends on the PaddlePaddle framework; GPU installs need matching CUDA builds
- **−** Benchmark claims such as 96.3% on OmniDocBench are the authors' own
- **−** Python support listed as 3.8 to 3.12 only
- **−** Several pipelines and models, so choosing between PP-OCR, VL and StructureV3 takes reading

<sub>GPU optional · Needs PaddlePaddle · Models: PP-OCRv6, PaddleOCR-VL-1.6, PP-StructureV3, HPD-Parsing, ONNX · [Repo](https://github.com/paddlepaddle/paddleocr) · [▶️ Demo ↗](https://www.paddleocr.com) · [📖 Docs ↗](https://www.paddleocr.ai/latest/en/version3.x/pipeline_usage/pipeline_overview.html) · [🌐 Site ↗](https://www.paddleocr.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddleocr/)</sub>

<a name="marker"></a>
### #&#8288;18 [marker](https://github.com/datalab-to/marker) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Oct 2026</sub>

**Converts PDFs, Office files and images to markdown, JSON, HTML or chunks.**

Marker is a Python library and CLI that converts PDF, image, PPTX, DOCX, XLSX, HTML and EPUB files to markdown, JSON, HTML or chunks, handling tables, equations, code blocks and image extraction. Layout, OCR and table recognition run through a surya VLM served by a local vLLM (Docker, NVIDIA) or llama.cpp server that starts automatically. An optional --use_llm mode adds Gemini, Claude, OpenAI-compatible, Azure, Vertex, OpenRouter or Ollama for higher accuracy.

- **+** Outputs markdown, JSON block tree with polygons, HTML or chunks, plus extracted images
- **+** Fast mode uses text layer and rf-detr layout on CPU; --disable_ocr starts no server
- **+** Batch CLI with worker pool, --skip_existing and chunk sharding across multiple machines
- **+** Reports 76.0% on olmocr-bench in balanced mode, ahead of MinerU and docling
- **−** Model weights use a modified OpenRAIL-M license; commercial use above startup limits needs a paid license
- **−** Balanced mode needs Docker with NVIDIA Container Toolkit, or llama.cpp on CPU and Apple Silicon
- **−** Non-PDF formats require the marker-pdf[full] extra install
- **−** README says the hosted Chandra model is more accurate than Marker

<sub>GPU optional · Needs PyTorch, Python 3.10+, vLLM via Docker with NVIDIA Container Toolkit (GPU), llama.cpp llama-server (CPU / Apple Silicon), optional LLM service for --use_llm · Models: surya VLM, Gemini, Claude, OpenAI-compatible, Azure · [Repo](https://github.com/datalab-to/marker) · [▶️ Demo ↗](https://www.datalab.to/playground) · [📖 Docs ↗](https://documentation.datalab.to) · [🌐 Site ↗](https://www.datalab.to) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/marker/)</sub>

<a name="dataflow"></a>
### #&#8288;19 [dataflow](https://github.com/opendcai/dataflow) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · Apache-2.0 · Oct 2026</sub>

**Operator-based Python pipelines for generating and cleaning LLM training data.**

DataFlow is a Python framework that turns noisy sources (PDFs, plain text, low-quality QA pairs) into datasets for pre-training, SFT and RL, using composable operators grouped into pipelines. It ships ready-made pipelines for text, reasoning, Text2SQL, knowledge-base cleaning and agentic RAG, plus a visual WebUI started with `dataflow webui` and an agent that assembles pipelines.

- **+** Pipeline → Operator → Prompt structure, with custom operators packaged via GitHub or PyPI
- **+** Ready-made pipelines for text, reasoning, Text2SQL, knowledge-base cleaning and agentic RAG
- **+** Works with API LLMs or local vLLM inference (`open-dataflow[vllm]`)
- **+** Visual WebUI via `dataflow webui`, plus a DataFlow Agent that builds pipelines
- **−** Output quality depends on the LLM backend you configure; API use needs a DF_API_KEY
- **−** Local GPU inference needs the vllm extra and a CUDA Docker image (cu124)
- **−** Several pieces (WebUI, Skills, RayOrch, MM) live in separate repos
- **−** Some tutorials are hosted on Bilibili and Feishu, with a Chinese-language focus

<sub>GPU optional · Docker · Needs OpenAI-compatible LLM API or vLLM, uv · Models: OpenAI-compatible APIs, vLLM local models · [Repo](https://github.com/opendcai/dataflow) · [▶️ Demo ↗](https://colab.research.google.com/drive/1haosl2QS4N4HM7u7HvSsz_MnLabxexXl?usp=sharing) · [📖 Docs ↗](https://OpenDCAI.github.io/DataFlow-Doc/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dataflow/)</sub>

<a name="data-juicer"></a>
### #&#8288;20 [data-juicer](https://github.com/datajuicer/data-juicer) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Oct 2026</sub>

**Operator-based pipelines for cleaning and deduplicating multimodal training data.**

Data-Juicer is a Python library and CLI (dj-process) that runs YAML-defined pipelines of 200+ operators over text, image, audio and video data, covering filtering, mapping, deduplication and analysis. It runs locally or on Ray clusters, and the README cites 70B samples in 2h on 50 Ray nodes and 5TB deduplicated in 2.8h on 1280 cores. It also ships LLM-based operators and a natural-language refinement model, Juicer.

- **+** 200+ operators across text, image, audio, video and multimodal data
- **+** Reproducible YAML recipes, plus a Python API for composing operators
- **+** Ray-based distributed execution with partitioning, checkpoints and OP fusion
- **+** Supports S3 and HDFS I/O, and loads Hugging Face datasets and gz JSONL
- **−** Many operators need extra dependencies or GPUs; the install is split into extras
- **−** Large-scale performance figures come from big clusters (1280 to 6400 cores)
- **−** Frequent releases with many operator behavior fixes; pin versions for reproducibility
- **−** Docs and several tools are spread across separate repos (hub, agents, sandbox)

<sub>GPU optional · Docker · Needs Ray (distributed mode), S3 or HDFS (optional), Hugging Face / ModelScope models (optional) · Models: Hugging Face models, OpenAI-compatible API, LiteLLM, Juicer-35B-A3B · [Repo](https://github.com/datajuicer/data-juicer) · [▶️ Demo ↗](http://8.138.149.181/) · [📖 Docs ↗](https://datajuicer.github.io/data-juicer/en/main/docs_index.html) · [🌐 Site ↗](https://datajuicer.github.io/data-juicer/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/data-juicer/)</sub>

<a name="pdfmathtranslate"></a>
### #&#8288;21 [pdfmathtranslate](https://github.com/pdfmathtranslate/pdfmathtranslate) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (75) · Freshness: recent (75) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · AGPL-3.0 · Oct 2026</sub>

**Translates scientific PDFs while keeping formulas, figures and layout intact.**

pdf2zh translates scientific PDFs and writes a translated-only and a bilingual (dual) PDF, preserving formulas, charts, table of contents and annotations. It runs as a CLI, a Gradio web UI on port 7860, a Python or HTTP API, or an MCP server, and calls a configurable translation service (Google by default). Layout detection uses a DocLayout-YOLO ONNX model, with optional OCR and an --ultrafast mode.

- **+** Outputs both translated-only and side-by-side bilingual PDFs from one command
- **+** Many interfaces: CLI, Gradio GUI, Docker, Python API, HTTP API, MCP stdio/SSE
- **+** Selectable translation backends via -s, with Google as the default
- **+** Optional OCR for scanned pages and --ultrafast mode for native-text PDFs
- **−** Python limited to 3.11 to 3.12
- **−** OCR is experimental and targets white-background scans; handwriting may fail
- **−** Last release is 2025-07-11; v2 work lives in a separate PDFMathTranslate-next repo
- **−** --ultrafast is CLI fast mode only and is weaker on complex tables or formulas

<sub>no GPU · Docker + Compose · Needs DocLayout-YOLO ONNX model (Hugging Face download), Translation service (Google default, others configurable) · Models: ONNX · port 7860 · [Repo](https://github.com/pdfmathtranslate/pdfmathtranslate) · [▶️ Demo ↗](https://pdf2zh.com/) · [📖 Docs ↗](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pdfmathtranslate/)</sub>

<a name="unstract"></a>
### #&#8288;22 [unstract](https://github.com/zipstack/unstract) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · AGPL-3.0 · Oct 2026</sub>

**Extracts structured JSON from PDFs and scans using LLM prompts.**

Unstract extracts structured JSON from documents such as PDFs, images and scans. Extraction schemas are defined as natural-language prompts in Prompt Studio, then deployed as a REST API or an ETL pipeline that loads results into a warehouse. It also offers an MCP server and an n8n node, and works with OpenAI, Anthropic, Bedrock, Ollama and other LLM providers.

- **+** Prompt Studio defines extraction schemas in natural language instead of per-vendor templates
- **+** Deploys as a REST API or ETL pipeline from S3, GCS, Drive, SFTP to Snowflake, BigQuery, Postgres
- **+** Supports many LLMs, including local Ollama, and vector DBs such as Qdrant, Weaviate, Milvus
- **+** Ships an MCP server and an n8n custom node for agent and workflow integration
- **−** Heavy stack: Django, Celery, FastAPI, Redis, RabbitMQ and PostgreSQL; 8 GB RAM minimum
- **−** LLMChallenge, SinglePass extraction, human review and SSO/RBAC are cloud or enterprise only
- **−** README lists Linux or macOS only; no Windows setup is documented
- **−** Default login unstract/unstract must be changed; losing ENCRYPTION_KEY locks adapter credentials

<sub>RAM ≥ 8 GB · no GPU · Docker + Compose · Needs Docker, Docker Compose, PostgreSQL, Redis, RabbitMQ, LLM provider, Vector database, Text extractor (LLMWhisperer, Unstructured.io or LlamaIndex Parse) · Models: OpenAI, Azure OpenAI, OpenAI Compatible, Anthropic Claude, AWS Bedrock · [Repo](https://github.com/zipstack/unstract) · [📖 Docs ↗](https://docs.unstract.com) · [🌐 Site ↗](https://unstract.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unstract/)</sub>

<a name="doctr"></a>
### #&#8288;23 [doctr](https://github.com/mindee/doctr) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Oct 2026</sub>

**Two-stage OCR library for PDFs and images, built on PyTorch.**

docTR is a Python library that extracts text from PDFs and images by running a text detection model, then a text recognition model on each detected word. It returns a structured Document (pages, blocks, lines, words) that can be exported as JSON, and also offers a KIE predictor, optional layout detection and a FastAPI template. Detection and recognition architectures are selectable, with pretrained weights.

- **+** Swappable detection (DBNet, LinkNet, FAST) and recognition (CRNN, SAR, MASTER, ViTSTR, PARSeq, VIPTR) models
- **+** Handles rotated pages and returns nested page/block/line/word output exportable to JSON
- **+** Includes KIE predictor, layout detection and a FastAPI template with OCR and KIE routes
- **+** Hosted Hugging Face Space and Streamlit demo for trying it before installing
- **−** Python 3.11 or higher required; PyTorch is the only supported framework
- **−** API template is minimal; README example uses port 8080 while the server runs on 8002
- **−** Docker GPU images need host CUDA 12.2 or newer
- **−** Default pipeline is OCR only; table structure and layout models are listed but sparsely documented in README

<sub>GPU optional · Docker · Needs PyTorch, Streamlit (demo), FastAPI (API template), weasyprint (URL input) · Models: DBNet, LinkNet, FAST, CRNN, SAR · port 8002 · [Repo](https://github.com/mindee/doctr) · [▶️ Demo ↗](https://huggingface.co/spaces/mindee/doctr) · [📖 Docs ↗](https://mindee.github.io/doctr/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/doctr/)</sub>

<a name="chandra"></a>
### #&#8288;24 [chandra](https://github.com/datalab-to/chandra) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: known (42) · Freshness: active (96) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**OCR model that converts PDFs and images to Markdown, HTML or JSON with layout.**

Chandra OCR 2 is a vision-language OCR model and Python CLI that turns images and PDFs into Markdown, HTML or JSON while keeping layout, tables, math, forms and handwriting. It runs locally through HuggingFace or against a vLLM server, and ships a Streamlit demo app. Weights use a modified OpenRAIL-M license, separate from the Apache-2.0 code.

- **+** Outputs Markdown, HTML and JSON with layout, extracted images and captions
- **+** Supports 90+ languages; README reports 77.8% average on its own 43-language benchmark
- **+** Two backends: local HuggingFace or vLLM server with parallel workers
- **+** Handles handwriting, math, tables and checkbox forms; CLI takes page ranges and directories
- **−** Weights are OpenRAIL-M: free only for research, personal use and startups under $2M
- **−** Hosted Datalab API is stated to be more accurate than the open weights
- **−** Benchmarks are mostly self-published; throughput is 1.44 pages/s on an H100
- **−** The chandra_vllm launcher depends on Docker; VRAM and RAM requirements are unknown

<sub>GPU required · Needs vLLM, Docker, HuggingFace Transformers, PyTorch · Models: datalab-to/chandra-ocr-2, HuggingFace, vLLM · port 8000 · [Repo](https://github.com/datalab-to/chandra) · [▶️ Demo ↗](https://www.datalab.to/playground) · [📖 Docs ↗](https://documentation.datalab.to) · [🌐 Site ↗](https://www.datalab.to) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chandra/)</sub>

<a name="tesseract-js"></a>
### #&#8288;25 [tesseract.js](https://github.com/naptha/tesseract.js) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (77) · Freshness: recent (69) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · May 2026</sub>

**JavaScript OCR library that runs Tesseract in the browser and Node.js.**

Tesseract.js wraps a WebAssembly port of the Tesseract OCR engine and extracts text from images in the browser or on Node.js. It exposes a worker API (createWorker, recognize, terminate) plus schedulers for parallel processing, and supports a long list of languages. It does not read PDFs or change Tesseract's recognition model.

- **+** Runs client-side in browsers via webpack, ESM or CDN script tag, so images can stay local
- **+** Also runs on Node.js (v7 needs v16 or newer) with the same worker API
- **+** Schedulers allow parallel recognition across multiple workers
- **+** Supports almost any language through Tesseract language data, chosen in createWorker
- **−** No PDF support; the README points to Scribe.js for that
- **−** Does not modify the Tesseract model, so accuracy is that of upstream Tesseract
- **−** Since v6, output formats other than text (e.g. hocr) are off by default
- **−** Breaking API changes across v4, v5 and v6 complicate upgrades

<sub>no GPU · Docker · Needs Node.js 16+ (v7, server use), tesseract.js-core (WebAssembly port of Tesseract) · Models: Tesseract traineddata language files · [Repo](https://github.com/naptha/tesseract.js) · [▶️ Demo ↗](http://tesseract.projectnaptha.com/) · [📖 Docs ↗](https://github.com/naptha/tesseract.js/blob/master/docs/api.md) · [🌐 Site ↗](https://tesseract.projectnaptha.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tesseract-js/)</sub>

<a name="jina-reader"></a>
### #&#8288;26 [Jina Reader](https://github.com/jina-ai/reader) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: known (40) · Freshness: recent (75) · Maintenance: weak (14) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · May 2026</sub>

**Converts any URL or search query into LLM-friendly markdown.**

Open-source branch of the service behind r.jina.ai and s.jina.ai: fetches a page with headless Chrome or curl-impersonate, parses PDFs and Office files, and returns markdown, text, HTML, screenshots or JSON controlled by request headers (engine, timeout, token limits). The ghcr.io image bundles Chrome, LibreOffice and CJK fonts, serves HTTP/1.1 on 8081 and h2c on 8080, and runs stateless or with S3-compatible caching.

- **+** Prebuilt image with Chrome, LibreOffice and CJK fonts; stateless by default
- **+** Fine-grained headers: x-respond-timing, x-max-tokens, x-token-budget, x-target-selector
- **+** Optional VLM captions for images without alt text
- **+** Semantic markdown chunking by heading or block level
- **−** Hosted proxy pool, rate limiting and MongoDB storage layer are not in the OSS branch
- **−** Needs non-redistributable assets (MaxMind GeoLite2, Source Han Sans) fetched at build
- **−** Last commit May 2026; the SaaS resync was April 2026
- **−** Default h2c port 8080 needs --http2-prior-knowledge from curl; use 8081 otherwise

<sub>no GPU · Docker + Compose · Needs Headless Chrome and LibreOffice (bundled in image), S3-compatible bucket (optional cache), VLM endpoint for image captions (optional) · port 8081 · [Repo](https://github.com/jina-ai/reader) · [▶️ Demo ↗](https://jina.ai/reader#demo) · [📖 Docs ↗](https://r.jina.ai/docs) · [🌐 Site ↗](https://jina.ai/reader) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jina-reader/)</sub>

<a name="babeldoc"></a>
### #&#8288;27 [babeldoc](https://github.com/funstory-ai/babeldoc) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.8k · AGPL-3.0 · Aug 2026</sub>

**PDF paper translator that keeps layout and outputs bilingual PDFs.**

BabelDOC translates scientific PDFs through an OpenAI-compatible LLM endpoint and rebuilds the layout, producing monolingual and bilingual PDFs. It ships a CLI and a Python API and is mainly meant to be embedded in other programs. It supports glossary CSVs with automatic term extraction, page selection, split translation for large files, and an OCR workaround for scanned documents.

- **+** Outputs monolingual and bilingual PDFs, side by side or on alternating pages
- **+** Glossary CSV support plus automatic term extraction for consistent terminology
- **+** Works with any OpenAI-compatible endpoint, including local servers such as Ollama
- **+** Offline asset package for air-gapped installs; TOML config file
- **−** Only OpenAI-compatible LLMs supported; not optimized for Bing or Google engines
- **−** Mainly tested on English-to-Chinese; other language pairs untested
- **−** README says the CLI is for debugging and gets no end-user support
- **−** No built-in web UI; self-hosted WebUI is in PDFMathTranslate-next

<sub>Needs OpenAI-compatible LLM API, uv, Python 3.12 · Models: OpenAI-compatible APIs, gpt-4o-mini (default), glm-4-flash, deepseek-chat, Ollama · [Repo](https://github.com/funstory-ai/babeldoc) · [▶️ Demo ↗](https://app.immersivetranslate.com/babel-doc/) · [📖 Docs ↗](https://funstory-ai.github.io/BabelDOC/supported_languages/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/babeldoc/)</sub>

<a name="olmocr"></a>
### #&#8288;28 [olmocr](https://github.com/allenai/olmocr) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: popular (56) · Freshness: recent (63) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Mar 2026</sub>

**PDF and image to Markdown converter built on a 7B vision-language model.**

olmOCR converts PDFs, PNGs and JPEGs into Markdown using a 7B vision-language model served through vLLM. It handles equations, tables, handwriting and multi-column layouts, and strips headers and footers. It runs on a local NVIDIA GPU, against a remote OpenAI-compatible server, or across many nodes coordinated through an S3 workspace.

- **+** Scores 82.4 on olmOCR-Bench (v0.4.0), near the top of the README table
- **+** Accepts any OpenAI-compatible server via --server, so no local GPU is required
- **+** Multi-node batch mode with an S3 work queue for millions of PDFs
- **+** Ships benchmark suite and trainer code for reproducing or fine-tuning the model
- **−** Local inference needs an NVIDIA GPU with at least 12 GB VRAM and 30 GB disk
- **−** README advises a clean conda environment because dependencies are hard to install
- **−** System setup needs poppler-utils and extra fonts; instructions cover only Ubuntu/Debian
- **−** Docker image with the model is about 30 GB

<sub>GPU required · Docker · Needs vLLM, poppler-utils, NVIDIA GPU (12 GB+ VRAM), AWS S3 (optional, multi-node) · Models: olmOCR-2-7B-1025-FP8, olmOCR-7B-0825-FP8, olmOCR-7B-0725-FP8 · [Repo](https://github.com/allenai/olmocr) · [▶️ Demo ↗](https://olmocr.allenai.org/) · [🌐 Site ↗](https://olmocr.allenai.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/olmocr/)</sub>

<a name="glm-ocr"></a>
### #&#8288;29 [glm-ocr](https://github.com/zai-org/glm-ocr) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (16) · Freshness: active (98) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Oct 2026</sub>

**0.9B OCR model and SDK that parses documents into Markdown and JSON.**

GLM-OCR is a 0.9B-parameter document OCR model (CogViT encoder, GLM-0.5B decoder) paired with a Python SDK. The SDK runs layout analysis with PP-DocLayout-V3, then recognizes regions in parallel and returns Markdown and JSON. It can call the Zhipu hosted API or a self-hosted vLLM, SGLang, Ollama or MLX server, and ships a CLI and a Flask service.

- **+** Small 0.9B model; README lists deployment on vLLM, SGLang, Ollama and Apple Silicon via mlx-vlm
- **+** Reports 94.62 on OmniDocBench V1.5, ranked #1 overall by the authors
- **+** CLI, Python API and Flask endpoint (port 5002) with swappable pipeline modules
- **+** Cloud mode needs no GPU; layout model can be placed on CPU or a chosen GPU
- **−** Self-hosted pipeline needs a separate vLLM or SGLang server plus transformers>=5.3.0
- **−** Hosted mode depends on a Zhipu API key from open.bigmodel.cn
- **−** Code is Apache-2.0 but model is MIT, and PP-DocLayoutV3 adds a third license to follow
- **−** VRAM and RAM requirements are not stated in the README

<sub>GPU optional · Needs vLLM or SGLang or Ollama (self-hosted), PP-DocLayout-V3, Zhipu MaaS API (cloud mode) · Models: zai-org/GLM-OCR (BF16) · port 5002 · [Repo](https://github.com/zai-org/glm-ocr) · [📖 Docs ↗](https://docs.z.ai/guides/vlm/glm-ocr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/glm-ocr/)</sub>

<a name="llm-scraper"></a>
### #&#8288;30 [llm-scraper](https://github.com/mishushakov/llm-scraper) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: niche (9) · Freshness: active (83) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · MIT · Jun 2026</sub>

**TypeScript library that extracts structured data from web pages with LLMs.**

LLM Scraper loads a page through Playwright and asks an LLM to fill a Zod or JSON Schema, returning typed objects. It runs on the Vercel AI SDK, so OpenAI, Anthropic, Google, Groq and Ollama models plug in. It can also stream partial objects or generate a reusable Playwright script for a schema.

- **+** Schemas in Zod or JSON Schema give type-safe output in TypeScript
- **+** Six input formats: html, raw_html, markdown, text, image, custom
- **+** Code generation produces a reusable Playwright script, avoiding an LLM call per page
- **+** Works with hosted providers and local models via Ollama
- **−** Library only: no CLI, server or UI
- **−** Needs Playwright and a separately installed AI SDK provider package
- **−** README gives no cost, token-limit or accuracy guidance for large pages
- **−** No tagged release published

<sub>no GPU · Needs Playwright, Zod, Vercel AI SDK provider package, LLM provider API or Ollama · Models: OpenAI GPT, Anthropic Claude, Google Gemini, Groq Llama, Ollama · [Repo](https://github.com/mishushakov/llm-scraper) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-scraper/)</sub>

<a name="doccano"></a>
### #&#8288;31 [doccano](https://github.com/doccano/doccano) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: known (31) · Freshness: slowing (41) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Jan 2026</sub>

**Web-based text annotation tool for labeling NLP datasets.**

doccano is a web application for annotating text for classification, sequence labeling (such as named entity recognition) and sequence-to-sequence tasks like summarization. Teams create a project, upload data, and label it collaboratively, with a REST API for automation. It runs from pip with SQLite by default, or with PostgreSQL, Docker or Docker Compose.

- **+** Covers text classification, sequence labeling and seq2seq annotation in one tool
- **+** Installs with pip and uses SQLite by default, so no database setup to start
- **+** Collaborative annotation with multiple users per project and a RESTful API
- **+** Deploy options include pip, Docker, Docker Compose, AWS CloudFormation and Heroku
- **−** Text only; the README lists no image, audio or video annotation
- **−** README mentions no built-in model-assisted pre-labeling
- **−** Compose setup needs RabbitMQ and PostgreSQL; pip setup needs a separate task queue process
- **−** Admin password is passed in plain environment variables or CLI arguments in the examples

<sub>no GPU · Docker + Compose · Needs SQLite (default), PostgreSQL (optional), RabbitMQ (Docker Compose) · port 8000 · [Repo](https://github.com/doccano/doccano) · [▶️ Demo ↗](http://doccano.herokuapp.com) · [📖 Docs ↗](https://doccano.github.io/doccano/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/doccano/)</sub>

<a name="easyocr"></a>
### #&#8288;32 [easyocr](https://github.com/jaidedai/easyocr) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: popular (69) · Freshness: quiet (9) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Dec 2025</sub>

**Python OCR library for text detection and recognition in 80+ languages.**

EasyOCR is a Python package that detects text regions with the CRAFT model and reads them with a CRNN recognizer, built on PyTorch. It returns bounding boxes, text and confidence scores from file paths, URLs, bytes or numpy arrays, and also has a CLI. Model weights download automatically per language, and it runs on GPU or CPU.

- **+** Two-line Python API returns boxes, text and confidence from paths, URLs, bytes or arrays
- **+** 80+ languages across Latin, Chinese, Arabic, Devanagari and Cyrillic scripts
- **+** CPU-only mode via gpu=False; also ships a command-line tool
- **+** Documents custom recognition and CRAFT detection model training
- **−** Not every language combination works together in one Reader; English works with all
- **−** Handwritten text support is listed as upcoming, not available
- **−** Last release 1.7.2 was September 2024
- **−** Issues older than 6 months are auto-closed; maintainers cite limited resources

<sub>GPU optional · Docker · Needs PyTorch, torchvision · Models: CRAFT detection, CRNN recognition (ResNet/VGG, LSTM, CTC) · [Repo](https://github.com/jaidedai/easyocr) · [▶️ Demo ↗](https://huggingface.co/spaces/tomofi/EasyOCR) · [📖 Docs ↗](https://www.jaided.ai/easyocr/documentation) · [🌐 Site ↗](https://www.jaided.ai/easyocr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/easyocr/)</sub>

<a name="cleanlab"></a>
### #&#8288;33 [cleanlab](https://github.com/cleanlab/cleanlab) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: known (36) · Freshness: slowing (40) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Jan 2026</sub>

**Python library that finds label errors and outliers in ML datasets.**

cleanlab uses predictions and embeddings from your existing model to detect label errors, outliers, duplicates and other issues in text, image, audio and tabular datasets. It is based on confident learning and also offers CleanLearning, a wrapper that trains a classifier on the cleaned data, plus tools for multi-annotator consensus and active learning.

- **+** Model-agnostic: works with outputs from PyTorch, TensorFlow, JAX, HuggingFace, XGBoost, scikit-learn
- **+** Dedicated support for multi-label, token classification, regression, segmentation and object detection
- **+** Datalab API reports issues in a few lines: find_issues() then report()
- **+** Algorithms are backed by published peer-reviewed papers
- **−** Needs pred_probs or embeddings from a trained model; it does not train a base model for you
- **−** Aimed at supervised ML datasets; not a general document or web data cleaner
- **−** Other ML tasks beyond the listed ones require adapting the methods
- **−** Library only; no hosted UI or web app in the open-source package

<sub>no GPU · Needs Python 3.10+ · Models: PyTorch, TensorFlow, Keras, JAX, HuggingFace · [Repo](https://github.com/cleanlab/cleanlab) · [📖 Docs ↗](https://docs.cleanlab.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cleanlab/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
