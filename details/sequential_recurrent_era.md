# The Sequential Recurrent & Supervised Task Era

Transitioning from flat averaging (~2016–2019), this era leveraged deep sequence models like Recurrent Neural Networks (RNNs), Long Short-Term Memory (LSTM) networks, and Gated Recurrent Units (GRUs) to encode sentences sequentially.

## Core Mechanism

The sentence is processed token-by-token. The hidden state at the final step (or a max-pooled representation across steps) serves as the sentence embedding. Models like **InferSent (2017)** were trained on supervised Natural Language Inference (NLI) tasks to learn high-quality embeddings.

```mermaid
flowchart LR
    Token1["Word 1"] --> RNN1["RNN Cell 1"]
    Token2["Word 2"] --> RNN2["RNN Cell 2"]
    Token3["Word 3"] --> RNN3["RNN Cell 3"]
    
    RNN1 --> RNN2
    RNN2 --> RNN3
    RNN3 --> Embed["Sentence Embedding (Final Hidden State)"]
```

## Advantages & Limitations

- **Advantage:** Captures sequential order and temporal dependencies.
- **Limitation:** Sequential processing bottlenecks GPUs, capping performance and scalability for long documents.

[Back to README](../README.md)
