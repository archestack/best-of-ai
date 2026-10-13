# 🕸️ Data and scraping for AI reviews · Best of Open-Source AI

Tools that turn web pages, PDFs and documents into clean text or structured data that models can use. Back to the [leaderboard](../README.md#%EF%B8%8F-data-and-scraping-for-ai).

<sub>🌐 Also on the web: [Data and scraping for AI on archestack.com](https://archestack.com/best-of-ai/data-tools/), each project on its own page.</sub>

<a name="crawl4ai"></a>
### 🥇 [Crawl4AI](https://github.com/unclecode/crawl4ai) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 85k · Apache-2.0 · Oct 2026</sub>

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
### 🥈 [docling](https://github.com/docling-project/docling) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 69k · MIT · Oct 2026</sub>

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

<a name="firecrawl"></a>
### 🥉 [Firecrawl](https://github.com/firecrawl/firecrawl) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: patchy (45) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 191k · AGPL-3.0 · Oct 2026</sub>

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

<a name="paddleocr"></a>
### #&#8288;4 [paddleocr](https://github.com/paddlepaddle/paddleocr) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: weak (29) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 91k · Apache-2.0 · Sep 2026</sub>

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

<a name="jina-reader"></a>
### #&#8288;5 [Jina Reader](https://github.com/jina-ai/reader) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (17) · Freshness: active (80) · Maintenance: weak (14) · Easy to run: easy (67) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · May 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
