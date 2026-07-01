# Multiple Negatives Ranking Loss (MNRL / InfoNCE)

MNRL is a widely adopted contrastive learning objective that treats matched pairs in a batch as positives, and all other cross-pair combinations as negatives.

## Core Mechanism

For a batch of $(A_i, B_i)$ pairs, $B_j$ (where $j \neq i$) serves as a negative candidate for $A_i$.

```mermaid
flowchart TD
    A1["Anchor A1"] --> P1["Positive B1 (Similarity High)"]
    A1 --> N2["In-Batch Negative B2 (Similarity Low)"]
    A1 --> N3["In-Batch Negative B3 (Similarity Low)"]
    P1 --> MNRL["MNRL / InfoNCE Optimization"]
    N2 --> MNRL
    N3 --> MNRL
```

[Back to README](../README.md)
