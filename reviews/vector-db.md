# 🧮 Vector databases reviews · Best of Self-Hosted AI

Vector stores and hybrid search engines for embeddings. Back to the [leaderboard](../README.md#-vector-databases).

<a name="milvus"></a>
### [🥇 81](../README.md#-how-we-rank "Score 81/100 (gold, 80+). Adoption 83 · Freshness 100 · Maintenance 84 · Easy to run 67 · Agent-ready 70 (each out of 100, weighted). Click for how we rank.") [Milvus](https://github.com/milvus-io/milvus) <sub>⭐ 46k · Apache-2.0 · Oct 2026</sub>

**Distributed vector database with dense, sparse and hybrid search at scale.**

Milvus is a distributed vector database (Go and C++, LF AI & Data Foundation) that separates compute and storage on Kubernetes, with a Standalone Docker mode and pip-installable Milvus Lite. It offers HNSW, IVF, FLAT, SCANN and DiskANN indexes, GPU CAGRA, sparse BM25 and learned-sparse vectors for hybrid search, metadata filtering, multi-tenancy, hot/cold storage, auth, TLS and RBAC.

- **+** Index types HNSW, IVF, FLAT, SCANN, DiskANN plus GPU CAGRA
- **+** Dense, sparse (BM25, SPLADE, BGE-M3) and hybrid search in one collection
- **+** Multi-tenancy at database, collection, partition or partition-key level
- **+** Mandatory auth, TLS and RBAC; Milvus Lite via pip for local dev
- **−** Distributed mode is Kubernetes-native with several microservices to operate
- **−** No port, RAM or Docker command in the README; install lives in docs
- **−** Zilliz is the major contributor and promotes its managed cloud
- **−** Source build needs Go 1.21+, CMake, GCC 11+ and Python 3.8 to 3.11

<sub>GPU optional · Compose · Models: any embedding model or service; pymilvus[model] wraps embedding and reranking models · [Repo](https://github.com/milvus-io/milvus) · [▶️ Demo ↗](https://milvus.io/milvus-demos) · [📖 Docs ↗](https://milvus.io/docs) · [🌐 Site ↗](https://milvus.io/)</sub>

<a name="meilisearch"></a>
### [🥈 69](../README.md#-how-we-rank "Score 69/100 (silver, 65-79). Adoption 92 · Freshness 100 · Maintenance 81 · Easy to run 33 · Agent-ready 30 (each out of 100, weighted). Click for how we rank.") [Meilisearch](https://github.com/meilisearch/meilisearch) <sub>⭐ 60k · NOASSERTION · Oct 2026</sub>

**Rust search engine API with full-text, vector and hybrid search.**

Meilisearch is a Rust search engine with a REST API that combines full-text search (typo tolerance, facets, geosearch) with vector and hybrid search, returning results as you type. It adds API keys with fine-grained permissions, tenant tokens for multi-tenancy, conversational search and MCP and LangChain integrations. The Community Edition is MIT; sharding and S3 snapshots require the Enterprise Edition.

- **+** Search-as-you-type under 50 ms with typo tolerance and faceting
- **+** Hybrid semantic plus full-text ranking in one engine
- **+** API keys with fine-grained permissions and tenant tokens for multi-tenancy
- **+** REST API with official SDKs; MCP and LangChain integrations
- **−** Sharding, S3 snapshots and search-rule previews are Enterprise Edition (BSL or commercial)
- **−** Anonymized telemetry is on by default and must be disabled
- **−** No port, RAM or install details in the README; docs only
- **−** Vector search is documented under experimental features

<sub>no GPU · Docker · [Repo](https://github.com/meilisearch/meilisearch) · [▶️ Demo ↗](https://where2watch.meilisearch.com/) · [📖 Docs ↗](https://www.meilisearch.com/docs) · [🌐 Site ↗](https://www.meilisearch.com)</sub>

<a name="chroma"></a>
### [🥉 64](../README.md#-how-we-rank "Score 64/100 (bronze, 55-64). Adoption 62 · Freshness 100 · Maintenance 37 · Easy to run 50 · Agent-ready 70 (each out of 100, weighted). Click for how we rank.") [Chroma](https://github.com/chroma-core/chroma) <sub>⭐ 29k · Apache-2.0 · Oct 2026</sub>

**Embedding database with a four-function API for Python and JavaScript.**

Chroma is an embedding database with a four-function API (create collection, add, query, get) that tokenizes, embeds and indexes documents itself or accepts your own vectors, with metadata and document filters. It runs in-memory or persisted from the Python or JavaScript client, or as a server via chroma run; the repo ships a Dockerfile and compose file. Chroma Cloud is the hosted serverless version.

- **+** Four-function API: create collection, add, query, get
- **+** Handles tokenization, embedding and indexing; own vectors optional
- **+** Python and JavaScript clients; chroma run for client-server mode
- **+** Weekly tagged releases on Mondays with hotfixes in between
- **−** README is thin: no port, resource or auth guidance
- **−** Hosted Chroma Cloud is the headline; self-hosting detail lives in docs
- **−** Row-based API marked coming soon
- **−** No multi-user auth described in the README

<sub>no GPU · Docker + Compose · Models: built-in embedding or user-supplied vectors · [Repo](https://github.com/chroma-core/chroma) · [📖 Docs ↗](https://docs.trychroma.com/) · [🌐 Site ↗](https://www.trychroma.com/)</sub>

<a name="qdrant"></a>
### [🥉 63](../README.md#-how-we-rank "Score 63/100 (bronze, 55-64). Adoption 73 · Freshness 100 · Maintenance 82 · Easy to run 33 · Agent-ready 0 (each out of 100, weighted). Click for how we rank.") [Qdrant](https://github.com/qdrant/qdrant) <sub>⭐ 35k · Apache-2.0 · Oct 2026</sub>

**Rust vector database with payload filtering, REST and gRPC.**

Qdrant is a Rust vector database exposing REST (OpenAPI 3.0) and gRPC on port 6333 for storing points (vectors plus JSON payload) and searching with dense, sparse and multivector (ColBERT) embeddings, rich payload filters and hybrid fusion (RRF, DBSF). It adds quantization, on-disk storage, sharding and replication, multitenancy, GPU-accelerated indexing and a web UI. Qdrant Edge runs the same engine embedded in-process.

- **+** Dense, sparse and multivector (ColBERT) search with RRF and DBSF fusion
- **+** Quantization cuts RAM up to 97 percent; on-disk storage and io_uring
- **+** REST with OpenAPI 3.0 spec plus gRPC; six official clients
- **+** Sharding and replication with zero-downtime collection resize
- **−** Default docker run has no auth and binds all interfaces
- **−** GPU acceleration covers indexing only; search runs on CPU
- **−** Qdrant Edge embedded mode is Python and Rust only
- **−** Sharding and tenant isolation require upfront design

<sub>GPU optional · Docker · Models: any embedding model; dense, sparse and late-interaction (ColBERT) vectors · port 6333 · [Repo](https://github.com/qdrant/qdrant) · [▶️ Demo ↗](https://qdrant.to/semantic-search-demo) · [📖 Docs ↗](https://qdrant.tech/documentation/)</sub>

<a name="pgvector"></a>
### [🥉 59](../README.md#-how-we-rank "Score 59/100 (bronze, 55-64). Adoption 52 · Freshness 100 · Maintenance 58 · Easy to run 50 · Agent-ready 0 (each out of 100, weighted). Click for how we rank.") [pgvector](https://github.com/pgvector/pgvector) <sub>⭐ 23k · NOASSERTION · Oct 2026</sub>

**PostgreSQL extension for vector similarity search with HNSW and IVFFlat.**

pgvector is a PostgreSQL extension (Postgres 13+) that adds vector, halfvec, bit and sparsevec column types with L2, inner product, cosine, L1, Hamming and Jaccard distance operators, exact search by default and HNSW or IVFFlat indexes for approximate search. Vectors sit beside ordinary rows with ACID, joins and backups, and Postgres full-text search can be combined for hybrid retrieval. It installs via make, Docker or OS packages.

- **+** Vectors live next to relational data with ACID, joins and point-in-time recovery
- **+** HNSW and IVFFlat indexes with six distance operators
- **+** Half-precision, binary and sparse vector types plus binary quantization
- **+** Installs via make, Docker, Homebrew, APT, Yum; preinstalled on many hosted Postgres
- **−** vector type capped at 2,000 dimensions (halfvec 4,000)
- **−** Approximate indexes filter after scanning; filtered recall needs iterative scan tuning
- **−** HNSW builds slow down sharply once the graph exceeds maintenance_work_mem
- **−** No server of its own; capacity depends on your Postgres tuning

<sub>no GPU · Docker · Needs PostgreSQL 13+ · Models: any embedding model; stores precomputed vectors · [Repo](https://github.com/pgvector/pgvector)</sub>

<a name="weaviate"></a>
### [🥉 57](../README.md#-how-we-rank "Score 57/100 (bronze, 55-64). Adoption 43 · Freshness 100 · Maintenance 72 · Easy to run 33 · Agent-ready 40 (each out of 100, weighted). Click for how we rank.") [Weaviate](https://github.com/weaviate/weaviate) <sub>⭐ 17k · NOASSERTION · Oct 2026</sub>

**Go vector database with built-in vectorizers, hybrid search and RAG.**

Weaviate is a Go vector database that stores objects with their vectors and serves hybrid BM25 plus semantic search, filtering, built-in RAG and reranking through REST, gRPC and GraphQL APIs. It can vectorize data at import using modules for OpenAI, Cohere, HuggingFace, Google or a local model2vec image, or accept precomputed vectors. Docker Compose runs it on ports 8080 and 50051; production adds multi-tenancy, replication and RBAC.

- **+** Vectorizes at import with OpenAI, Cohere, HuggingFace, Google or a local model2vec container
- **+** Hybrid BM25 plus vector, image search, filtering, RAG and reranking in one query
- **+** Multi-tenancy, replication, RBAC, horizontal scaling and vector compression
- **+** REST, gRPC and GraphQL with Python, TypeScript, Java, Go and C# clients
- **−** Enterprise features in wl/ need a commercial license key; one image mixes both
- **−** Vectorization needs a module container or external API keys
- **−** No RAM or sizing guidance in the README
- **−** Both REST 8080 and gRPC 50051 must be exposed

<sub>no GPU · Docker + Compose · Needs optional embedding inference container (e.g. model2vec) or external embedding APIs · Models: OpenAI, Cohere, HuggingFace, Google and other integrated model providers, local model2vec (minishlab/potion-base-32M), precomputed vectors · port 8080 · [Repo](https://github.com/weaviate/weaviate) · [▶️ Demo ↗](https://elysia.weaviate.io) · [📖 Docs ↗](https://docs.weaviate.io)</sub>

<a name="helix-db"></a>
### [🥉 55](../README.md#-how-we-rank "Score 55/100 (bronze, 55-64). Adoption 19 · Freshness 100 · Maintenance 96 · Easy to run 33 · Agent-ready 30 (each out of 100, weighted). Click for how we rank.") [HelixDB](https://github.com/helixdb/helix-db) <sub>⭐ 6.1k · Apache-2.0 · Oct 2026</sub>

**Rust graph database with native vector and BM25 search.**

HelixDB is a Rust database that combines a labeled property graph, approximate nearest-neighbor vector search and BM25 full-text search in one transactional engine. A CLI starts a local instance in Docker or Podman on port 6969 (in-memory by default, --disk to persist) or the engine runs embedded, and Rust, TypeScript, Python and Go SDKs send the same JSON queries to POST /v2/query.

- **+** Graph traversal, vector ANN and BM25 in one transactional engine
- **+** Vector search prefiltered by graph traversal
- **+** SDKs for Rust, TypeScript, Python and Go sending the same JSON query
- **+** Embedded mode runs inside your process without a server
- **−** Local data is in-memory unless started with --disk
- **−** Python and Go SDKs are 0.x while Rust and TypeScript are 3.x
- **−** Cypher support only in source builds
- **−** Install is a curl piped to bash script

<sub>no GPU · Docker · Needs Docker or Podman for the local instance · Models: any embedding model; stores precomputed vectors · port 6969 · [Repo](https://github.com/helixdb/helix-db) · [📖 Docs ↗](https://docs.helix-db.com) · [🌐 Site ↗](https://helix-db.com)</sub>

<a name="vespa"></a>
### [41](../README.md#-how-we-rank "Score 41/100. Adoption 26 · Freshness 100 · Maintenance 80 · Easy to run 0 · Agent-ready 0 (each out of 100, weighted). Click for how we rank.") [Vespa](https://github.com/vespa-engine/vespa) <sub>⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

**Serving engine for vectors, tensors, text and ML ranking at scale.**

Vespa is a serving platform that indexes vectors, tensors, text and structured data, selects a subset at query time, evaluates machine-learned ranking models over it and returns results in under 100 ms while the corpus changes, across many nodes. The Java and C++ engine builds from this repo with a release every morning Monday to Thursday. Getting started and self-hosting live in docs.vespa.ai; Vespa Cloud is the hosted option.

- **+** Vectors, tensors, text and structured data queried and ranked together
- **+** Machine-learned ranking models evaluated at serving time
- **+** Runs hundreds of thousands of queries per second on large internet services
- **+** Sample applications repo plus detailed docs
- **−** README covers building, not running; install details live in docs
- **−** Heavy platform (Java and C++ engine) sized for multi-node clusters
- **−** C++ builds require AlmaLinux 8; Java needs JDK 17 and Maven
- **−** A new release every weekday morning Monday to Thursday; versions churn

<sub>no GPU · Models: machine-learned ranking models evaluated in Vespa · [Repo](https://github.com/vespa-engine/vespa) · [📖 Docs ↗](https://docs.vespa.ai) · [🌐 Site ↗](https://vespa.ai)</sub>

<a name="marqo"></a>
### [33](../README.md#-how-we-rank "Score 33/100. Adoption 10 · Freshness 76 · Maintenance 0 · Easy to run 33 · Agent-ready 40 (each out of 100, weighted). Click for how we rank.") [Marqo](https://github.com/marqo-ai/marqo) <sub>⭐ 5.0k · Apache-2.0 · Apr 2026</sub>

**Vector search engine with built-in embedding, now deprecated upstream.**

Marqo was a vector search engine that generated embeddings and stored them in one service, so you indexed raw text or images and queried in natural language. Its README now states the open-source project is deprecated and will receive no updates, pointing to the commercial Marqo ecommerce search platform instead. The Apache-2.0 code and docs remain available.

- **+** Apache-2.0 code remains available for forks
- **+** Docs at docs.marqo.ai still describe the API
- **−** Open-source project declared deprecated; no further updates
- **−** README no longer documents installation, API or supported models
- **−** Last commit 2026-04-10
- **−** Only the commercial platform is maintained

<sub>Compose · [Repo](https://github.com/marqo-ai/marqo) · [📖 Docs ↗](https://docs.marqo.ai) · [🌐 Site ↗](https://www.marqo.ai)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
