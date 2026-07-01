# Dense vs. Sparse Embedding Models

Modern search engines often combine dense and sparse representations to balance keyword match precision with conceptual semantic understanding.

## Core Mechanism

- **Dense Models:** Generate low-dimensional, continuous floating-point vectors (e.g., 768 or 1536 dimensions) capturing abstract meaning.
- **Sparse Models:** Generate high-dimensional, vocabulary-aligned vectors where most values are zero (e.g., mapping to vocabulary token weights like SPLADE).

```mermaid
flowchart TD
    Input["Input Sentence"] --> Dense["Dense Model (e.g., BERT/OpenAI)"]
    Input --> Sparse["Sparse Model (e.g., SPLADE/BM25)"]
    Dense --> DenseVec["[0.12, -0.45, ..., 0.89] (768d)"]
    Sparse --> SparseVec["{'bank': 3.2, 'account': 1.8} (30000d)"]
```

[Back to README](../README.md)
