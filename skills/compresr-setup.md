---
name: compresr-setup
description: Install the Compresr SDK and make a query-specific context-compression call (latte_v1).
user-invocable: true
allowed-tools: Bash(pip:*), Bash(python:*), Bash(uv:*)
metadata:
  author: compresr
  homepage: https://compresr.ai
  docs: https://compresr.ai/docs/quick-start.md
---

# Compresr setup

Compresr is an LLM context-compression API: you send long context plus the query
you want answered, and get back a shorter context that keeps the answer-bearing
spans and drops the rest. The documented public model is `latte_v1`
(query-specific); `query` is required on every call.

This file is meant to be read by an agent and executed step by step.

## 1. Install

```bash
pip install compresr
```

## 2. Authenticate

Get an API key at https://compresr.ai (keys start with `cmp_`; $10 free credits,
no card). Export it — never hardcode it.

```bash
export COMPRESR_API_KEY="cmp_..."
```

## 3. Compress context for an LLM call

```python
import os
from compresr import CompressionClient

client = CompressionClient(api_key=os.environ["COMPRESR_API_KEY"])

result = client.compress(
    context=retrieved_docs,            # the long context you would send the model
    query=user_question,               # REQUIRED for latte_v1
    compression_model_name="latte_v1", # the public model
    target_compression_ratio=4,        # 0–1 = removal strength; >1 = Nx factor
    coarse=True,                       # True = paragraph-level/faster; False = token-level
)

compressed = result.data.compressed_context  # send THIS to your LLM instead of the raw context
# result.data also exposes: original/compressed tokens, tokens_saved,
# actual_compression_ratio, duration_ms
```

## Notes

- `query` is required — calling `latte_v1` without it raises `ValidationError`.
- `target_compression_ratio`: values `0–1` are removal strength; values `>1` are an
  Nx factor (not a keep-fraction).
- Honest framing: the accuracy win lives at LIGHT (~2x) compression. High ratios
  (~10x) are a cost/latency play, not an accuracy claim.
- Batch / stream / async: `compress_batch(...)`, `compress_stream(...)`, and
  `*_async` variants exist. Exceptions: `CompresrError`, `AuthenticationError`,
  `RateLimitError`, `ValidationError`.

## More

- Quick start: https://compresr.ai/docs/quick-start.md
- Models & parameters: https://compresr.ai/docs/api-reference/models.md
- Machine site map: https://compresr.ai/llms.txt
