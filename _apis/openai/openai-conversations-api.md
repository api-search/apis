---
aid: openai:openai-conversations-api
baseURL: https://api.openai.com
description: The Conversations API allows you to create and manage stateful conversations for use with the Responses API. A conversation object contains an id, a created_at timestamp, and metadata. Because conversations are stateful, managing context across conversations is handled automatically, and the /responses/compact endpoint can shrink context for long-running conversations.
humanURL: https://platform.openai.com/docs/api-reference/conversations/create
image: ''
layout: api
name: OpenAI Conversations API
properties:
- type: Documentation
  url: https://platform.openai.com/docs/api-reference/conversations/create
- type: Documentation
  url: https://developers.openai.com/api/docs/guides/conversation-state/
provider_name: OpenAI
provider_slug: openai
slug: openai-conversations-api
source_yaml: "aid: openai:openai-conversations-api\nname: OpenAI Conversations API\ntags:\n- Conversations\n- State Management\nscore: 100\nbaseURL: https://api.openai.com\nhumanURL: https://platform.openai.com/docs/api-reference/conversations/create\nproperties:\n- url: https://platform.openai.com/docs/api-reference/conversations/create\n  type: Documentation\n- url: https://developers.openai.com/api/docs/guides/conversation-state/\n  type: Documentation\ndescription: The Conversations API allows you to create and manage stateful conversations for use with\n  the Responses API. A conversation object contains an id, a created_at timestamp, and metadata. Because\n  conversations are stateful, managing context across conversations is handled automatically, and the\n  /responses/compact endpoint can shrink context for long-running conversations.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/apis.yml
tags:
- Conversations
- State Management
---
