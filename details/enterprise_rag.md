# Enterprise Retrieval-Augmented Generation (RAG)

Retrieval-Augmented Generation (RAG) integrates search retrieval databases with large language models to ground generation in factual context.

## Core Mechanism

```mermaid
flowchart TD
    Query["User Query"] --> Embed["Embedding Model"]
    Embed --> Vec["Query Vector"]
    Vec --> VDB["Vector DB (Qdrant/Pinecone)"]
    VDB --> Context["Top-K Relevant Documents"]
    Context --> LLM["LLM Generator"]
    Query --> LLM
    LLM --> Response["Grounded Answer"]
```

[Back to README](../README.md)
