# Transformers Resources

## Articles

### Introduction to Transformers
- Link: https://t.tyrionurl.com/bs
- Notes:
  - Transformers use self-attention
  - Replaced RNNs in many NLP tasks
  - Backbone of GPT, BERT, Llama

### Difference between Self-Attention and Multi-head Self-Attention
- Link: https://t.tyrionurl.com/bt
- Notes:
  - multi-head self-Attention  
## Official / Deep Dive Resources
- AWS Explanation
- NVIDIA Blog
- Hugging Face Docs



### Masked Multi Head Attention 
- Link: https://t.tyrionurl.com/bu
- Notes:
  - Masked multi-head Attention  
## Official / Deep Dive Resources
- there is encoder and decoder in transformer 
- masked multi head attention is the imp part for that 
- used for next token prediction 






### RoPE Positional Encoding in AI Language Models
- Link: https://t.tyrionurl.com/by
- Noted:
  - it combines both positional and rotatinal encoding. 
  - it uses rotation matrix 
  ![rotation matrix](https://medium.com/@himankvjain/the-rope-effect-untangling-positional-encoding-in-ai-language-models-1bf0ab46776b)
   
### Grouped Query Attention
- Link: https://t.tyrionurl.com/bv
- Notes:
  - it is an optimization technique for transformer models that balances the high computational cost of Multi-Head Attention (MHA) with the memory efficiency of Multi-Query Attention (MQA)
## Official / Deep Dive Resources
- Optimized KV Cache: By reducing the total number of key and value heads (often by a    factor of 8, e.g., \(GQA8\)), the size of the KV cache decreases significantly
- Faster Inference: Smaller KV caches require less memory to be loaded by hardware
- Industry Standard: GQA is heavily adopted in modern, high-load LLMs, including LLaMA 2, Mistral, and Gemma 2

