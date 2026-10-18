# 🕸️ Data and scraping for AI reviews · Best of Open-Source AI

Tools that turn web pages, PDFs and documents into clean text or structured data that models can use. Back to the [leaderboard](../README.md#%EF%B8%8F-data-and-scraping-for-ai).

<sub>🌐 Also on the web: [Data and scraping for AI on archestack.com](https://archestack.com/best-of-ai/data-tools/), each project on its own page.</sub>

<a name="mineru"></a>
### 🥇 [mineru](https://github.com/opendatalab/mineru) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 82k · custom license · Oct 2026</sub>

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

<a name="crawl4ai"></a>
### 🥈 [Crawl4AI](https://github.com/unclecode/crawl4ai) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 86k · Apache-2.0 · Oct 2026</sub>

**Python web crawler that converts pages to LLM-ready Markdown and JSON.**

Crawl4AI is a Python library, CLI (`crwl`) and Docker REST server that drives Playwright browsers (Chromium, Firefox, WebKit) to turn web pages into clean or filtered Markdown. It extracts structured data with CSS/XPath/regex schemas without an LLM, or through any LiteLLM-supported provider into a typed JSON schema. It also supports deep crawls, adaptive crawling and batch fetching. A hosted Crawl4AI Cloud with search and answer endpoints is sold separately.

- **+** Schema-based CSS/XPath extraction runs without any LLM call
- **+** Fit Markdown filters (pruning, BM25, LLM) strip menus and boilerplate
- **+** Persistent profiles, CDP remote browsers, rotating proxies and stealth mode
- **+** Docker server exposes /md, /crawl, /screenshot, /pdf, plus MCP, dashboard and playground
- **−** Search, SERP and answer endpoints exist only in the paid hosted cloud
- **−** Bot-wall handling when self-hosted depends on your own proxies and settings
- **−** Needs a Playwright browser install via crawl4ai-setup
- **−** README asks for attribution when you use it

<sub>no GPU · Docker + Compose · Needs Playwright browsers (Chromium), Docker (optional), LLM provider API key (optional) · Models: LiteLLM providers, OpenAI, Ollama · port 11235 · [Repo](https://github.com/unclecode/crawl4ai) · [📖 Docs ↗](https://docs.crawl4ai.com) · [🌐 Site ↗](https://crawl4ai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/crawl4ai/)</sub>

<a name="docling"></a>
### 🥉 [docling](https://github.com/docling-project/docling) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 69k · MIT · Oct 2026</sub>

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
### #&#8288;4 [markitdown](https://github.com/microsoft/markitdown) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 191k · MIT · Oct 2026</sub>

**Python tool that converts PDF, Office, HTML and audio files to Markdown for LLMs.**

MarkItDown is a Python library and CLI that converts PDF, Word, PowerPoint, Excel, images, audio, HTML, CSV/JSON/XML, ZIP, EPUB and YouTube URLs into Markdown, keeping headings, lists, tables and links. Optional backends add LLM image descriptions, Azure Document Intelligence, Azure Content Understanding, and OCR via the markitdown-ocr plugin. Output targets LLM pipelines rather than high-fidelity human-facing documents.

- **+** Covers many formats through one CLI and Python API (convert, convert_local, convert_stream)
- **+** Built-in converters run offline; install only needed formats via extras like [pdf,docx,pptx]
- **+** Third-party plugin system, plus an LLM-vision OCR plugin using any OpenAI-compatible client
- **+** MIT license, active releases, Python 3.10 through 3.14
- **−** Not meant for high-fidelity conversion; output is tuned for text analysis tools
- **−** Video and structured field extraction need billable Azure Content Understanding
- **−** convert() accepts URIs and files with process privileges; untrusted input must be sanitized
- **−** LLM image descriptions currently limited to pptx and image files; OCR needs a plugin

<sub>no GPU · Docker · Needs Python 3.10-3.14, Azure Document Intelligence (optional), Azure Content Understanding (optional), OpenAI-compatible client (optional) · Models: OpenAI-compatible vision models (e.g. gpt-4o) · [Repo](https://github.com/microsoft/markitdown) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/markitdown/)</sub>

<a name="label-studio"></a>
### #&#8288;5 [label-studio](https://github.com/humansignal/label-studio) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (75) · Easy to run: very easy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 28k · Apache-2.0 · Oct 2026</sub>

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

<a name="firecrawl"></a>
### #&#8288;6 [Firecrawl](https://github.com/firecrawl/firecrawl) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: patchy (45) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 193k · AGPL-3.0 · Oct 2026</sub>

**Web scraping and crawling API that returns LLM-ready markdown.**

API that turns URLs into markdown, HTML, screenshots or schema-based JSON, with endpoints for search, scrape, crawl, map, batch scrape, page interaction and a prompt-driven agent. Handles JS-rendered pages and parses hosted PDFs and DOCX. SDKs for Python, Node, Go, Java, Elixir, Rust and Ruby plus an MCP server and CLI, for teams feeding web content to RAG pipelines and agents.

- **+** Seven SDKs plus CLI and MCP server; SDKs poll async crawl jobs automatically
- **+** Crawl, map and batch-scrape endpoints return job IDs for large sites
- **+** Scrape supports actions (click, scroll, write, wait) before extraction
- **+** Compose file at the repo root for self-hosting
- **−** README is written around the hosted API and keys; self-hosting lives in separate docs
- **−** AGPL-3.0 license; network use of a modified version triggers source obligations
- **−** Agent endpoint runs the hosted spark-2 model, not a local LLM
- **−** Proxy rotation and anti-bot handling are hosted-service features

<sub>no GPU · Compose · [Repo](https://github.com/firecrawl/firecrawl) · [▶️ Demo ↗](https://firecrawl.dev/playground) · [📖 Docs ↗](https://docs.firecrawl.dev) · [🌐 Site ↗](https://firecrawl.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/firecrawl/)</sub>

<a name="scrapegraph-ai"></a>
### #&#8288;7 [scrapegraph-ai](https://github.com/scrapegraphai/scrapegraph-ai) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (90) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Oct 2026</sub>

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

<a name="langextract"></a>
### #&#8288;8 [langextract](https://github.com/google/langextract) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Oct 2026</sub>

**Python library that extracts source-grounded structured data from text using LLMs.**

LangExtract is a Python library that takes a prompt and few-shot examples, runs an LLM over unstructured text, and returns structured extractions mapped to exact character spans in the source. Long documents are handled by chunking, parallel workers and multiple passes. Results save to JSONL and render as an interactive HTML review page. Backends include Gemini, OpenAI and local Ollama models.

- **+** Each extraction is grounded to a character span; ungrounded results get char_interval = None
- **+** Chunking, parallel workers and multiple passes for long documents (max_workers, extraction_passes)
- **+** Gemini, OpenAI and Ollama supported, plus a plugin system for custom providers
- **+** Generates a self-contained interactive HTML view of extractions in context
- **−** Output schema is driven by few-shot examples; poor examples cause alignment warnings and weaker results
- **−** Ollama provider does not support output_schema
- **−** Controlled generation is documented mainly for Gemini; cloud models need an API key
- **−** Library only, with no server or UI beyond the HTML visualization

<sub>GPU optional · Docker · Needs Gemini, OpenAI or Vertex AI API key for cloud models, Ollama for local models · Models: Gemini, OpenAI, Ollama, Vertex AI, OpenAI-compatible endpoints · [Repo](https://github.com/google/langextract) · [▶️ Demo ↗](https://google-langextract.hf.space/) · [📖 Docs ↗](https://github.com/google/langextract/blob/main/docs/examples/longer_text_example.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langextract/)</sub>

<a name="marker"></a>
### #&#8288;9 [marker](https://github.com/datalab-to/marker) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: patchy (49) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Oct 2026</sub>

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

<a name="pdfmathtranslate"></a>
### #&#8288;10 [pdfmathtranslate](https://github.com/pdfmathtranslate/pdfmathtranslate) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (59) · Freshness: recent (76) · Maintenance: patchy (40) · Easy to run: very easy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · AGPL-3.0 · Oct 2026</sub>

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

<a name="moli"></a>
### #&#8288;11 [moli](https://github.com/lexmount/moli) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · Apache-2.0 · Oct 2026</sub>

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

<a name="paddleocr"></a>
### #&#8288;12 [paddleocr](https://github.com/paddlepaddle/paddleocr) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: weak (29) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 91k · Apache-2.0 · Sep 2026</sub>

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

<a name="unstructured"></a>
### #&#8288;13 [unstructured](https://github.com/unstructured-io/unstructured) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

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

<a name="opendataloader-pdf"></a>
### #&#8288;14 [opendataloader-pdf](https://github.com/opendataloader-project/opendataloader-pdf) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: hard (0) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

**PDF parser that outputs Markdown, JSON with bounding boxes, and Tagged PDF.**

Java-based PDF parser with Python, Node.js and Java SDKs. The default local mode extracts text, tables, headings and images with bounding boxes and XY-Cut++ reading order. An optional hybrid mode runs a Docling-based backend server for OCR, complex tables, LaTeX formulas and chart descriptions. It can also auto-tag untagged PDFs into Tagged PDF; PDF/UA export is an enterprise add-on.

- **+** Local mode is deterministic and runs without GPU; README lists 0.015 s/page
- **+** JSON output includes bounding boxes for every element, useful for source citations
- **+** Hybrid mode adds OCR (several engines), borderless tables, LaTeX formulas and picture descriptions
- **+** Auto-tags untagged PDFs to Tagged PDF under Apache-2.0
- **−** Requires Java 11+ on the host in addition to Python or Node
- **−** Each convert() call spawns a JVM, so calls must be batched
- **−** PDF/UA-1/2 export and the accessibility studio are enterprise-only
- **−** Hybrid mode needs a separate backend server; no Word, Excel or PowerPoint support

<sub>GPU optional · Needs Java 11+, Python 3.10+ (Python SDK), Docling-based hybrid backend (optional) · Models: SmolVLM 256M (picture description), EasyOCR, RapidOCR, Tesseract · port 5002 · [Repo](https://github.com/opendataloader-project/opendataloader-pdf) · [📖 Docs ↗](https://opendataloader.org/docs/quick-start-python) · [🌐 Site ↗](https://opendataloader.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opendataloader-pdf/)</sub>

<a name="jina-reader"></a>
### #&#8288;15 [Jina Reader](https://github.com/jina-ai/reader) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (7) · Freshness: recent (79) · Maintenance: weak (14) · Easy to run: easy (67) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · May 2026</sub>

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

<a name="easyocr"></a>
### #&#8288;16 [easyocr](https://github.com/jaidedai/easyocr) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: known (47) · Freshness: quiet (12) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Dec 2025</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
