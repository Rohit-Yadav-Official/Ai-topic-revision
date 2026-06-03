

# input to output flow diagram

### text to transformer block
-  Input Text
    ↓
    Tokenizer
    (BPE / SentencePiece)
        ↓
    Token IDs
        ↓
    Token Embedding Lookup
        ↓
    RoPE (Rotary Positional Encoding)
        ↓
    Input Embeddings
        ↓
    ┌─────────────────────────────┐
    │      Transformer Block 1    │
    │  ├─ Multi-Head Attention    │
    │  ├─ Add & LayerNorm         │
    │  ├─ Feed Forward Network    │
    │  └─ Add & LayerNorm         │
    └─────────────────────────────┘
        ↓
    ┌─────────────────────────────┐
    │      Transformer Block 2    │
    │  ├─ Multi-Head Attention    │
    │  ├─ Add & LayerNorm         │
    │  ├─ Feed Forward Network    │
    │  └─ Add & LayerNorm         │
    └─────────────────────────────┘
        ↓
            ...
        ↓
    ┌─────────────────────────────┐
    │      Transformer Block N    │
    │  ├─ Multi-Head Attention    │
    │  ├─ Add & LayerNorm         │
    │  ├─ Feed Forward Network    │
    │  └─ Add & LayerNorm         │
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
