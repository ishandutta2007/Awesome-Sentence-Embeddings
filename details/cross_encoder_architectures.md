# Cross-Encoder Architectures (Full-Attention Fusion)

Cross-Encoder architectures process the query and document simultaneously by concatenating them and passing them through the transformer network together.

## Core Mechanism

```mermaid
flowchart TD
    Concat["[CLS] Query [SEP] Document [SEP]"] --> Transformer["Transformer Model (Full Attention)"]
    Transformer --> Classification["Classification / Regression Head"]
    Classification --> Score["Relevance Score"]
```

## Comparison

- **Pros:** Extremely high accuracy due to full cross-attention between every token in the query and document.
- **Cons:** High latency; cannot pre-compute embeddings offline, making it impractical for first-stage retrieval on large datasets.

[Back to README](../README.md)
