---
name: compresr-compress-for-rag
description: Compress retrieved RAG chunks against the user's question before they reach the LLM, cutting input tokens 30-70% while keeping answer-bearing spans.
api: openapi/compresr-openapi-original.json
operations:
- compress_query_specific_api_compress_question_specific__post
- compress_query_specific_batch_api_compress_question_specific_batch_post
- list_compression_models_api_compress_models_get
method: generated
source: openapi/compresr-openapi-original.json + https://compresr.ai/docs/quick-start
---

# Compress retrieved context for RAG

Use Compresr as a pre-LLM filter: after retrieval, compress each chunk (or the
concatenated context) against the user's question so you only pay for tokens that
carry the answer.

## Auth
- Send `X-API-Key: cmp_...` on every request (keys from the dashboard).
- Read the key from `COMPRESR_API_KEY`; never hardcode it. HTTPS only.

## Steps
1. Retrieve your chunks as usual.
2. Call `compress_query_specific_api_compress_question_specific__post`
   (`POST /api/compress/question-specific/`) with:
   - `context`: the retrieved text you would otherwise send the model.
   - `query`: the user's actual question (be specific — vague queries degrade to
     generic compression).
   - `compression_model_name`: `"latte_v2"` (default) or `"latte_v1"`.
   - `target_compression_ratio`: `0.5` to start (`0<r<=1` = fraction removed;
     `r>1` = Nx target, max 200). Or set `dynamic: true` (latte_v2 only) to auto-pick.
3. Forward `data.compressed_context` to your LLM in place of the raw context.
4. Track savings from `data.original_tokens`, `data.compressed_tokens`,
   `data.tokens_saved`.

For many chunks, use `compress_query_specific_batch_api_compress_question_specific_batch_post`
(`POST /api/compress/question-specific/batch`, up to 100 rows in one call).

## Rules (from conventions/ + errors/)
- `actual_compression_ratio` is the fraction REMOVED, not a keep-fraction and not an Nx factor.
- Retry only on `429`/`500`/`503`, honouring `Retry-After`. Never retry other 4xx.
- Empty `query` or `target_compression_ratio` outside 0-200 => `422 validation_error`.
- The accuracy win lives at light (~2x) compression; high ratios are a cost/latency play.
