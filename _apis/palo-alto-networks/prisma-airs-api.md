---
aid: palo-alto-networks:prisma-airs-api
baseURL: https://service.api.aisecurity.paloaltonetworks.com
description: The AI Runtime Security API (API Intercept) for securing generative AI applications, AI models, AI data, and AI agents against prompt injection, data leakage, toxic content, malicious URLs, database security attacks, malicious code, and other AI-specific threats. Provides Scan APIs for real-time threat detection on prompts and model responses, and Management APIs for configuring security profiles, API keys, and deployments. Supports Secure MCP, custom topic guardrails, contextual grounding, and data masking. Available in US, EU (Germany), India, and Singapore regions. Integrates via REST API or the pan-aisecurity Python SDK with API key or OAuth 2.0 authentication.
humanURL: https://pan.dev/airs/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Prisma AIRS AI Runtime Security API
properties:
- type: Documentation
  url: https://pan.dev/airs/
- type: APIReference
  url: https://pan.dev/prisma-airs/api/airuntimesecurity/airuntimesecurityapi/
- type: GettingStarted
  url: https://docs.paloaltonetworks.com/ai-runtime-security/activation-and-onboarding/ai-runtime-security-api-intercept-overview
- title: Python SDK
  type: SDK
  url: https://pan.dev/prisma-airs/api/airuntimesecurity/pythonsdk/
- type: GitHubRepository
  url: https://github.com/PaloAltoNetworks/aisecurity-python-sdk
- title: AIRS Management Python SDK
  type: SDK
  url: https://github.com/PaloAltoNetworks/airs-api-mgmt-sdk
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-prisma-airs-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-airs-api-ai-profile-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-airs-api-content-scan-result-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-airs-api-scan-content-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-airs-api-scan-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-airs-api-scan-response-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-airs-api-ai-profile-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-airs-api-content-scan-result-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-airs-api-scan-content-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-airs-api-scan-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-airs-api-scan-response-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-prisma-airs-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-airs-api-ai-profile-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-airs-api-content-scan-result-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-airs-api-scan-content-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-airs-api-scan-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-airs-api-scan-response-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: prisma-airs-api
source_yaml: "aid: palo-alto-networks:prisma-airs-api\nname: Prisma AIRS AI Runtime Security API\ntags:\n- AI Runtime\n- AI Security\n- API Intercept\n- GenAI\n- LLM Security\n- MCP Security\n- Prompt Injection\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://service.api.aisecurity.paloaltonetworks.com\nhumanURL: https://pan.dev/airs/\nproperties:\n- url: https://pan.dev/airs/\n  type: Documentation\n- url: https://pan.dev/prisma-airs/api/airuntimesecurity/airuntimesecurityapi/\n  type: APIReference\n- url: https://docs.paloaltonetworks.com/ai-runtime-security/activation-and-onboarding/ai-runtime-security-api-intercept-overview\n  type: GettingStarted\n- url: https://pan.dev/prisma-airs/api/airuntimesecurity/pythonsdk/\n  type: SDK\n  title: Python SDK\n- url: https://github.com/PaloAltoNetworks/aisecurity-python-sdk\n  type: GitHubRepository\n- url: https://github.com/PaloAltoNetworks/airs-api-mgmt-sdk\n  type: SDK\n  title: AIRS Management\
  \ Python SDK\n- url: openapi/palo-alto-prisma-airs-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/prisma-airs-api-ai-profile-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-airs-api-content-scan-result-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-airs-api-scan-content-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-airs-api-scan-request-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-airs-api-scan-response-schema.json\n  type: JSONSchema\n- url: json-structure/prisma-airs-api-ai-profile-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-airs-api-content-scan-result-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-airs-api-scan-content-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-airs-api-scan-request-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-airs-api-scan-response-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-prisma-airs-api-context.jsonld\n\
  \  type: JSON-LD\n- url: examples/prisma-airs-api-ai-profile-example.json\n  type: Example\n- url: examples/prisma-airs-api-content-scan-result-example.json\n  type: Example\n- url: examples/prisma-airs-api-scan-content-example.json\n  type: Example\n- url: examples/prisma-airs-api-scan-request-example.json\n  type: Example\n- url: examples/prisma-airs-api-scan-response-example.json\n  type: Example\ndescription: The AI Runtime Security API (API Intercept) for securing generative AI applications, AI models,\n  AI data, and AI agents against prompt injection, data leakage, toxic content, malicious URLs, database\n  security attacks, malicious code, and other AI-specific threats. Provides Scan APIs for real-time threat\n  detection on prompts and model responses, and Management APIs for configuring security profiles, API\n  keys, and deployments. Supports Secure MCP, custom topic guardrails, contextual grounding, and data\n  masking. Available in US, EU (Germany), India, and Singapore regions.\
  \ Integrates via REST API or the\n  pan-aisecurity Python SDK with API key or OAuth 2.0 authentication.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- AI Runtime
- AI Security
- API Intercept
- GenAI
- LLM Security
- MCP Security
- Prompt Injection
---
