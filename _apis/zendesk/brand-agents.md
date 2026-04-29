---
aid: zendesk:brand-agents
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Brand Agents API lets you programmatically manage which agents have access to which brands in a multibrand Zendesk Support account. It provides endpoints to list the agents associated with a given brand and to add or remove agents from that brand, so you can automate onboarding/offboarding, sync brand access from external directories, and enforce leastprivilege access at scale.
humanURL: https://developer.zendesk.com/api-reference/ticketing/account-configuration/brand_agents/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Brand Agents API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/account-configuration/brand_agents/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/brand-agents-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: brand-agents
source_filename: brand-agents-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Brand Agents\n  description: Needs a description.\npaths:\n  /api/v2/brand_agents:\n    get:\n      operationId: ListBrandAgents\n      tags:\n        - Brand Agents\n      summary: Zendesk Get  Api V2 Brand_agents\n      description: |\n        Returns a list of all brand agent memberships for your account.\n\n\n        #### Pagination\n\n        * Cursor pagination (recommended)\n        * Offset pagination\n\n        See [Pagination](/api-reference/introduction/pagination/).\n\n        Returns a maximum of 100 records per page.\n\n        #### Allowed For:\n\n        * Admins\n      parameters:\n        - $ref: '#/components/parameters/UserId'\n        - $ref: '#/components/parameters/BrandId'\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/BrandAgentsResponse'\n              examples:\n\
  \                default:\n                  $ref: '#/components/examples/BrandAgentsResponseExample'\n  /api/v2/brand_agents/{brand_agent_id}:\n    get:\n      operationId: ShowBrandAgentById\n      tags:\n        - Brand Agents\n      summary: Zendesk Get  Api V2 Brand_agents Brand_agent_id\n      description: |\n        Returns a brand agent membership for your account.\n\n\n        #### Allowed For\n\n        * Admins\n      parameters:\n        - $ref: '#/components/parameters/BrandAgentId'\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/BrandAgentResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/BrandAgentResponseExample'\ncomponents:\n  schemas:\n    BrandAgentsResponse:\n      type: object\n      properties:\n        brand_agents:\n          type: array\n          items:\n\
  \            $ref: '#/components/schemas/BrandAgentObject'\n    BrandAgentResponse:\n      type: object\n      properties:\n        brand_agent:\n          $ref: '#/components/schemas/BrandAgentObject'\ntags:\n  - name: Brand Agents\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/brand-agents-openapi-original.yml
tags:
- Brand Agents
---
