---
aid: openai:openai-batch-api
baseURL: https://api.openai.com
description: The Batch API enables asynchronous processing of requests with 50% cost discount, higher rate limits, and completion within 24 hours. It supports /v1/responses, /v1/chat/completions, /v1/embeddings, /v1/completions, and /v1/moderations endpoints. A single batch may include up to 50,000 requests with a batch input file size up to 200 MB.
humanURL: https://platform.openai.com/docs/api-reference/batch
image: ''
layout: api
name: OpenAI Batch API
properties:
- type: Documentation
  url: https://platform.openai.com/docs/api-reference/batch
- type: Documentation
  url: https://platform.openai.com/docs/guides/batch
provider_name: OpenAI
provider_slug: openai
slug: openai-batch-api
source_yaml: "aid: openai:openai-batch-api\nname: OpenAI Batch API\ntags:\n- Async\n- Batch\nscore: 100\nbaseURL: https://api.openai.com\nhumanURL: https://platform.openai.com/docs/api-reference/batch\nproperties:\n- url: https://platform.openai.com/docs/api-reference/batch\n  type: Documentation\n- url: https://platform.openai.com/docs/guides/batch\n  type: Documentation\ndescription: The Batch API enables asynchronous processing of requests with 50% cost discount, higher\n  rate limits, and completion within 24 hours. It supports /v1/responses, /v1/chat/completions, /v1/embeddings,\n  /v1/completions, and /v1/moderations endpoints. A single batch may include up to 50,000 requests with\n  a batch input file size up to 200 MB.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/apis.yml
tags:
- Async
- Batch
---
