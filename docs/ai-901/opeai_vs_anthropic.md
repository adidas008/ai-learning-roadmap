# OpenAI API vs. Anthropic API Comparison

## 1. Feature Comparison Matrix

| Feature / Model | OpenAI API (`gpt-4o`, `gpt-4o-mini`) | Anthropic API (`claude-3-5-sonnet`) |
| :--- | :--- | :--- |
| **Primary Strength** | Multimodal reasoning, Speed, Ecosystem | Complex coding, Extended reasoning, Nuanced prose |
| **Max Context Window** | 128,000 tokens | 200,000 tokens |
| **Output Capabilities** | Structured Outputs (JSON Schema enforcement) | Extended Thinking, Artifacts generation |
| **Python SDK** | `openai` package (`OpenAI()`) | `anthropic` package (`Anthropic()`) |

## 2. Basic Python Implementation Snippets

### OpenAI SDK Sample
```python
from openai import OpenAI

client = OpenAI()
response = client.chat.completions.create(
    model="gpt-4o-mini",
    messages=[{"role": "user", "content": "Hello world!"}]
)
print(response.choices[0].message.content)

import anthropic

client = anthropic.Anthropic()
message = client.messages.create(
    model="claude-3-5-sonnet-20241022",
    max_tokens=1000,
    messages=[{"role": "user", "content": "Hello world!"}]
)
print(message.content[0].text)