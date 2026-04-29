---
aid: bunq:bunq-chat-conversation-api
baseURL: ''
description: Bunq Chat Conversation API is a communication tool that allows users to have real-time conversations within the Bunq banking app. With this API, users can chat with customer support agents, make inquiries about their accounts, or engage in discussions with other Bunq users. The Chat Conversation API also enables users to receive important notifications and updates from Bunq, ensuring that they stay informed about their finances.
humanURL: https://doc.bunq.com/#/content/List_all_Content_for_User_ChatConversation_Attachment
image: ''
layout: api
name: Bunq Chat Conversation API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-chat-conversation-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-chat-conversation-api
source_filename: bunq-user-userid-chat-conversation-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/chat-conversation'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths:\n  /user/{userID}/chat-conversation/{chat-conversationID}/attachment/{attachmentID}/content:\n    get:\n      tags:\n        - User\n      summary: ''\n      operationId: List_all_Content_for_User_ChatConversation_Attachment\n      description: Get the raw content of a specific attachment.\n      parameters:\n        -\
  \ in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - in: path\n          name: chat-conversationID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - in: path\n          name: attachmentID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: >-\n            Fetch the raw content of an attachment with given ID. The\
  \ raw\n            content is the base64 of a file, without any JSON wrapping.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/AttachmentConversationContentListing'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-chat-conversation-openapi-original.yml
tags:
- Attachments
- Chat
- Content
- Conversations
- Users
---
