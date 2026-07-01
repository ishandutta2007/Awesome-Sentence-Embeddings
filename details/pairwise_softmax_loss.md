# Pairwise Softdev Cross-Entropy Loss

Commonly used in supervised sentence embedding training, particularly with Natural Language Inference (NLI) datasets consisting of premises, entailments, and contradictions.

## Core Mechanism

The network optimizes the embeddings such that the cosine similarity between the premise and entailment is maximized while the similarity between the premise and contradiction is minimized.

```mermaid
flowchart TD
    Premise["Premise Vector"] --> Sim1["Cosine Sim"]
    Entailment["Entailment Vector"] --> Sim1
    Premise --> Sim2["Cosine Sim"]
    Contradiction["Contradiction Vector"] --> Sim2
    Sim1 --> Softmax["Softmax Cross-Entropy Loss"]
    Sim2 --> Softmax
```

[Back to README](../README.md)
