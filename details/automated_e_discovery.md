# Automated Corporate E-Discovery & Legal Audit Reranking

E-Discovery pipelines utilize semantic sentence/passage embeddings to automate audit and compliance scanning of unstructured corporate communications.

## Core Mechanism

```mermaid
flowchart TD
    Contracts["Corporate Emails & Contracts"] --> BiEncoder["Bi-Encoder (Fast Recall)"]
    BiEncoder --> Candidates["Top 100 Document Candidates"]
    Candidates --> CrossEncoder["Cross-Encoder (High Precision Rerank)"]
    CrossEncoder --> Sorted["Final Flagged Documents for Audit"]
```

[Back to README](../README.md)
