# Input to Output Flow Diagram

## Text to Transformer Block

```text
Input Text
    ↓
Tokenizer (BPE / SentencePiece)
    ↓
Token IDs
    ↓
Token Embedding Lookup
    ↓
Input Embeddings
    ↓

┌─────────────────────────────┐
│      Transformer Block 1    │
│                             │
│  Multi-Head Self-Attention  │
│            ↓                │
│      Add & LayerNorm        │
│            ↓                │
│   Feed Forward Network      │
│            ↓                │
│      Add & LayerNorm        │
└─────────────────────────────┘
            ↓

┌─────────────────────────────┐
│      Transformer Block 2    │
│                             │
│  Multi-Head Self-Attention  │
│            ↓                │
│      Add & LayerNorm        │
│            ↓                │
│   Feed Forward Network      │
│            ↓                │
│      Add & LayerNorm        │
└─────────────────────────────┘
            ↓

            ...

            ↓

┌─────────────────────────────┐
│      Transformer Block N    │
│                             │
│  Multi-Head Self-Attention  │
│            ↓                │
│      Add & LayerNorm        │
│            ↓                │
│   Feed Forward Network      │
│            ↓                │
│      Add & LayerNorm        │
└─────────────────────────────┘

            ↓
Final Hidden State
            ↓
Linear Layer (Vocabulary Projection)
            ↓
Logits
            ↓
Softmax
            ↓
Probability Distribution
            ↓
Next Token Selection
            ↓
Generated Token
```