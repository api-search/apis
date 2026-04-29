---
aid: peoplesoft:chatbot-integration-framework-api
baseURL: https://{hostname}:{port}/psft/api/chatbot/v1
description: Integration framework for connecting PeopleSoft with Oracle Digital Assistant (ODA) including REST services for chatbot data retrieval and embedded chatbot UI on Fluid pages (PICASO). Requires PeopleTools 8.57.07+.
humanURL: https://docs.oracle.com/cd/E52319_01/infoportal/chatbot.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Chatbot Integration Framework API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E52319_01/infoportal/chatbot.html
- type: FAQ
  url: https://docs.oracle.com/cd/E52319_01/infoportal/peoplesoft_chatbot_faq.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/chatbot-integration.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: chatbot-integration-framework-api
source_filename: chatbot-integration.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Chatbot Integration Framework API\n  description: Integration framework for connecting PeopleSoft with Oracle Digital Assistant (ODA) including REST services for chatbot data retrieval and embedded chatbot UI on Fluid pages (PICASO). \n    Requires PeopleTools 8.57.07+.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/chatbot/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: Chatbot Integration Framework Documentation\n  url: https://docs.oracle.com/cd/E52319_01/infoportal/chatbot.html\ntags:\n- name: Chatbot\n  description: Chatbot\
  \ integration operations\npaths:\n  /intents:\n    get:\n      summary: PeopleSoft List Intents\n      description: Retrieve available chatbot intents and their configurations.\n      operationId: listIntents\n      tags:\n      - Chatbot\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with intents\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  intents:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        intentName:\n                          type: string\n                        description:\n                          type: string\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /fulfill:\n    post:\n      summary: PeopleSoft Fulfill\
  \ Intent\n      description: Process a chatbot intent fulfillment request from Oracle Digital Assistant.\n      operationId: fulfillIntent\n      tags:\n      - Chatbot\n      security:\n      - basicAuth: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                intent:\n                  type: string\n                  description: The intent to fulfill\n                parameters:\n                  type: object\n                  description: Intent parameters\n                userId:\n                  type: string\n                  description: The user identifier\n      responses:\n        '200':\n          description: Intent fulfilled\n          content:\n            application/json:\n              schema:\n                type: object\n        '400':\n          description: Bad request\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n\
  \        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/chatbot-integration.yml
tags:
- Chatbot
- Conversational AI
- Digital Assistant
- PICASO
---
