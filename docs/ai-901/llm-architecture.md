# LLM Architecture & Fundamentals

## 1. Key Concepts
* **Tokenization**: Breaking raw text into smaller tokens (words or sub-words) processed as numerical IDs.
* **Transformer Architecture**: Uses **Self-Attention Mechanisms** to weight the importance of different words in a sequence regardless of distance.
* **Context Window**: The maximum number of tokens an LLM can process simultaneously in a single prompt + completion cycle.

## 2. Model Training Phases
1. **Pre-training**: Unsupervised learning on massive text datasets to predict the next token.
2. **Supervised Fine-Tuning (SFT)**: Instruction-following dataset training for conversational chat.
3. **RLHF / DPO**: Alignment phase using human feedback or direct preference optimization to improve safety and helpfulness.

## 3. Key LLM Design Patterns
* **Prompt Engineering**: Zero-shot, Few-shot, and Chain-of-Thought (CoT) prompting techniques.
* **RAG (Retrieval-Augmented Generation)**: Fetching external document chunks via vector search to reduce hallucinations.