---
name: web-search
description: Search the web, find similar pages, extract content from URLs, and more.
---

1. Read the API spec at `https://exa.ai/docs/exa-spec.yaml` to discover available endpoints, request/response schemas, and parameters.
2. Construct the appropriate curl request based on what the user is asking for:
  - Always use sane defaults unless the user specifies otherwise, including:
    - `neural` search
    - <=10 results (anything above incurs additional costs)
    - No summaries, no subpages, no extras
  - Pass `$EXA_API_KEY` via the `x-api-key` header.
3. Execute the curl command via the `bash` tool.
4. Parse and interpret the response for the user.
