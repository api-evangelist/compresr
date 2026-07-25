---
name: compresr-compress-tool-output
description: Compress noisy agent tool results (web search hits, API responses, file dumps) against the tool call's intent before they re-enter the prompt.
api: openapi/compresr-openapi-original.json
operations:
- compress_tool_output_api_compress_tool_output__post
- compress_tool_output_batch_api_compress_tool_output_batch_post
method: generated
source: openapi/compresr-openapi-original.json + https://compresr.ai/docs/introduction
---

# Compress agent tool outputs

In an agent loop, tool results are the biggest source of token bloat. Compress each
tool result against the intent of the call that produced it before feeding it back
into the model's context.

## Auth
- `X-API-Key: cmp_...` header on every request (from `COMPRESR_API_KEY`). HTTPS only.

## Steps
1. Run the tool (web search, API call, file read) and capture its raw output.
2. Call `compress_tool_output_api_compress_tool_output__post`
   (`POST /api/compress/tool-output/`) with:
   - `context`: the raw tool output.
   - `query`: the intent of the tool call — what the agent was trying to learn.
   - `compression_model_name`: `"toc_latte_v2"` (tool-output model, faster backbone)
     or `"toc_latte_v1"`.
3. Insert `data.compressed_context` back into the agent's working context instead of
   the raw output.
4. For a fan-out of tool calls, batch with
   `compress_tool_output_batch_api_compress_tool_output_batch_post`
   (`POST /api/compress/tool-output/batch`, up to 100 rows).

## Rules (from conventions/ + errors/)
- Response envelope is `{ success, data, error }`; switch on `error.code`, log the code
  not the message.
- Honour `Retry-After` on `429`; back off exponentially. Retry only 429/500/503.
- A demo-scoped key on this paid endpoint returns `403 scope_error` — use a user key.
