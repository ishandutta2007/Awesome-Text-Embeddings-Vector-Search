# Awesome-Text-Embeddings-Vector-Search

## Top Text Embeddings & Vector Search Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Multilingual Embeddings, Hybrid Retrieval & Dense Vector Search*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Text Embeddings & Vector Search**. These tools convert text, code, and images into dense vector representations that capture semantic meaning, then enable similarity search across millions or billions of items — the foundation layer for RAG pipelines, semantic search, recommendation systems, and classification.



**Examples** include Cohere Embeddings, OpenAI Embeddings, Voyage AI, Google Vertex Embeddings, AWS Titan Embeddings, Jina AI, Mixedbread AI, Nomic AI, BGE (FlagEmbedding), and Hugging Face TEI (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, multilingual retrieval, and hybrid dense-sparse search — ideal for teams prioritizing data sovereignty, developers building RAG infrastructure, and organizations avoiding per-token embedding costs.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Cohere Embeddings](https://cohere.com/)**  

  Enterprise embedding API with multilingual support, compression, and embedding types optimized for search, classification, and clustering.



- **[OpenAI Embeddings](https://platform.openai.com/)**  

  `text-embedding-3-small` and `text-embedding-3-large` models with configurable dimensions. Widely adopted baseline for RAG pipelines.



- **[Voyage AI](https://www.voyageai.com/)**  

  Embedding API optimized for retrieval quality, with domain-specific models for code, law, and finance.



- **[Google Vertex Embeddings](https://cloud.google.com/vertex-ai)**  

  Text embedding models on Vertex AI with multilingual support and integration with Google Cloud.



- **[AWS Titan Embeddings](https://aws.amazon.com/bedrock/)**  

  Amazon Titan embedding models via Bedrock for text and multimodal retrieval.



- **[Jina AI](https://jina.ai/)**  

  Embeddings, rerankers, and Reader API for LLM-friendly content extraction. **Jina-embeddings-v4** (3.8B parameters) outperforms proprietary models from Google, OpenAI, and Voyage AI on visually rich document retrieval . API endpoints match OpenAI's `text-embedding-3-large` schemas for easy switching .



- **[Mixedbread AI](https://www.mixedbread.ai/)**  

  Embedding and reranking API with **Toast-1** search model. Python SDK and Apache-2.0 licensed agent skills for Claude Code, Cursor, and Codex .



- **[Nomic AI](https://www.nomic.ai/)**  

  **Nomic Embed** models via Atlas API, with Python and TypeScript SDKs . Also powers GPT4All for local embedding inference .



- **[BGE Cloud (BAAI)](https://bge-model.com/)**  

  Managed embedding service for BGE models from Beijing Academy of Artificial Intelligence.



- **[Hugging Face Inference Endpoints](https://huggingface.co/)**  

  Managed deployment of any embedding model from the Hugging Face Hub, including BGE, E5, and GTE families.



## Open-Source GitHub Projects



- **[FlagEmbedding (BGE)](https://github.com/FlagOpen/FlagEmbedding)**  

  **The most widely used open-source embedding model family** from BAAI — 12,200+ GitHub stars, MIT licensed . **BGE-M3** is the flagship: multi-lingual (100+ languages), multi-functional (dense, sparse, multi-vector retrieval), and multi-granularity (up to **8,192 tokens**) . **BGE v1.5** models alleviated similarity distribution issues and ranked 1st on both MTEB and C-MTEB benchmarks . Includes **reranker** cross-encoder models (`bge-reranker-v2-m3`, `bge-reranker-v2-gemma`) for improving retrieval precision after embedding search . Integrated into LangChain . Install via `pip install -U FlagEmbedding` .



- **[Sentence Transformers](https://github.com/UKPLab/sentence-transformers)**  

  **The foundational framework for dense text embeddings** — Apache-2.0 licensed . Provides an easy method to compute dense vector representations for sentences, paragraphs, and images using BERT/RoBERTa/XLNet-based models. Text is embedded such that similar text is close in vector space and can be efficiently found using cosine similarity . The standard Python API (`model.encode()`) that most embedding models adopt.



- **[Text Embeddings Inference (TEI)](https://github.com/huggingface/text-embeddings-inference)**  

  **Hugging Face's blazing-fast inference solution for embedding models** — Rust-based, Apache-2.0 licensed . Deploy any Hugging Face model with the `text-embeddings-inference` tag via Docker. Features **dynamic batching** with `--max-batch-tokens`, **flash attention** for supported models, **ONNX** and **Candle** backends, tokenization workers, and distributed tracing via OpenTelemetry . Supports **re-rankers** (BGE reranker large) and **Sequence Classification** models via dedicated endpoints . Includes gRPC API for high-performance deployments and SPLADE pooling for sparse embeddings .



- **[Qwen3-Embedding](https://github.com/QwenLM/Qwen3-Embedding)**  

  **Alibaba's embedding model family** with instruction-aware retrieval . Supports **8,192 token context** and multiple sizes (0.6B, 4B, 8B). Uses a task instruction prefix for queries (`Instruct: task\nQuery: ...`) while documents are embedded without instructions . Available via Transformers, vLLM (`--task embed`), and Sentence Transformers .



- **[USearch](https://github.com/unum-cloud/USearch)**  

  **Smaller & faster single-file similarity search engine** — Apache-2.0 licensed, v2.26.3 . Portable single-header C++ library with **SIMD-optimized** and user-defined metrics. Supports **15+ quantization levels** from f64 to f6 and single-bit. Native bindings for **C++, Python, Rust, JavaScript, Java, Go, Swift, C#, C, Objective-C, and Wolfram**. Trusted by Google, Microsoft, ClickHouse, DuckDB, ScyllaDB, and TiDB . The search engine layer for embedding pipelines.



- **[Mixedbread Skills](https://github.com/mixedbread-ai/skills)**  

  **Apache-2.0 licensed agent skills for search, RAG, and document parsing** with Mixedbread . Compatible with **Claude Code, Cursor, Codex, Gemini CLI, and 20+ other agents**. Includes `mxbai-cli` (store management and search), `mixedbread-search` (Stores API), `mixedbread-parsing` (document parsing and OCR), and `mixedbread-search-agent` (Toast-1 model) .



- **[Nomic SDKs](https://github.com/nomic-ai)**  

  **Python and TypeScript bindings for Nomic Atlas** embedding API . `nomic` Python SDK (1,880 stars) and `ts-nomic` TypeScript bindings. LangChain integration via `langchain-nomic` . Forks of `text-embeddings-inference` and `usearch` are also maintained by Nomic .



- **[local-llm-embed](https://github.com/youichi-uda/local-llm-embed)**  

  **Extract sentence embeddings from any local causal LLM without fine-tuning** . Train-free recipe using **whitening + echo** packaged as a sentence-transformers compatible API. Reuses your existing Llama/Qwen/Phi/Mistral model in memory — no separate ~500MB encoder to load. Honest trade-off: dedicated encoders still beat raw LLM probes on STS by ~6 points, but on classification tasks (Banking77) this library matches or slightly beats the baseline .



- **[Multilingual E5 (Unity)](https://github.com/skykim/multilingual-e5-unity)**  

  **E5 models (Small, Base, Large) for Unity AI Inference Engine** . Supports **100+ languages**. Requires `query:` prefix for searches and `passage:` prefix for documents. ONNX models can be quantized to fp16 or int8 for Unity deployment .



- **[GTE (Alibaba-NLP)](https://github.com/Alibaba-NLP)**  

  **General Text Embeddings** family with multilingual and English-only variants. **GTE-v1.5** (base-en, large-en) and **mGTE-TRM** (multilingual) models. **GTE-Qwen2** uses Qwen2 as backbone for instruction-following embeddings . Integrated into vLLM for high-throughput serving .



- **[Sparse-Dense Joint Retrieval](https://github.com/holi-lab/mm-sparse-retrieval)**  

  **CIKM 2025 research implementation** for jointly optimizing sparse and dense retrievers for text-image retrieval . Uses **Self-Knowledge Distillation** with an integrated similarity score as the shared teacher signal. Sparse retriever achieves performance comparable to or surpassing its dense counterpart while retaining sparse efficiency benefits .



### Additional Strong Open-Source Options



- **text2vec** — Chinese-focused text embedding and semantic matching tool. Supports Word2Vec, BERT, and Sentence-BERT backends for Chinese semantic search.

- **BM25 (rank_bm25, Elasticsearch)** — Sparse lexical retrieval still essential for hybrid search. `rag-hybrid-retrieval` demonstrates dense-only retrieval often fails to rank relevant evidence in Top-K; sparse signals surface evidence that dense retrieval ranks poorly .

- **pgvector** — PostgreSQL extension for vector similarity search. Benchmark at 100M vectors: **0.987 Recall@10, 1,800 QPS, $0.08 cost per 1M queries** — the cheapest option but lowest throughput .

- **Qdrant** — Rust-based vector database optimized for **filter-heavy workloads under 50M vectors**. Benchmark: **0.991 Recall@10, 4,200 QPS, $0.18 cost per 1M queries** . Native hybrid search with excellent payload filtering .

- **Milvus** — **Billions of vectors** with horizontal sharding and disk-backed indexes. Benchmark: **0.988 Recall@10, 4,600 QPS, $0.21 cost per 1M queries** .

- **Weaviate** — Native hybrid (dense + sparse/BM25) retrieval with strong metadata filtering .

- **Vespa** — Yahoo's engine for vector, lexical, and structured search at scale .



**Frameworks for building custom systems**: Combine **FlagEmbedding (BGE-M3)** for multilingual dense+sparse+multi-vector retrieval, **Sentence Transformers** for the standard embedding API, **Text Embeddings Inference** for GPU-accelerated production serving, **USearch** for the similarity search engine layer, and **Qdrant** or **pgvector** for vector storage depending on scale and filtering needs — to build a complete self-hosted text embeddings and vector search stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Text embedding and vector search tools involve trade-offs between retrieval quality, latency, cost, and operational complexity. **Benchmarks are workload-dependent** — MTEB scores and vector database benchmarks do not guarantee performance on your specific data distribution and query patterns . Dedicated encoders still outperform raw LLM probes on pure semantic similarity . Hybrid retrieval resolves evidence presence failures, not prioritization failures — ranking instability remains the dominant bottleneck in RAG systems .

- Self-hosted open-source solutions require proper GPU infrastructure planning, index memory budgeting, and retrieval quality monitoring.



---



**Made for AI engineers, RAG developers, search infrastructure teams, and developers building semantic retrieval systems.**  

Let's make text embeddings and vector search more open, multilingual, and retrieval-efficient.
