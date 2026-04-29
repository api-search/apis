---
aid: zendesk:accounts
baseURL: https://api.getbase.com
description: The Zendesk Sell Accounts API lets you programmatically manage the company records (accounts) in your CRM. It provides REST endpoints to create, read, update, and delete accounts; search and filter them; and work with related data such as associated contacts, deals, activities, notes, tags, and custom fields.
humanURL: https://developer.zendesk.com/api-reference/sales-crm/resources/account/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Accounts API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/sales-crm/resources/account/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/accounts-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: accounts
source_filename: accounts-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Accounts\n  description: Needs a description.\npaths:\n  /api/v2/accounts:\n    post:\n      operationId: CreateTrialAccount\n      tags:\n        - Reseller\n      summary: Zendesk Post  Api V2 Accounts\n      responses:\n        '201':\n          description: Created response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TrialAccountResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TrialAccountResponseExample'\n  /api/v2/accounts/available:\n    get:\n      operationId: VerifySubdomainAvailability\n      tags:\n        - Reseller\n      summary: Zendesk Get  Api V2 Accounts Available\n      description: >\n        Zendesk Support credentials are not required to access this endpoint.\n        You can use any Zendesk Support subdomain.\n\n\n        Returns \"true\" if the subdomain is available.\n      parameters:\n\
  \        - name: subdomain\n          in: query\n          description: >\n            Specify the name of the subdomain you want to verify. The name can't\n            contain underscores, hyphens, or spaces.\n          required: true\n          schema:\n            type: string\n          example: z3ndesk\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  success:\n                    type: boolean\n              example:\n                success: true\ncomponents:\n  schemas: {}\ntags:\n  - name: Reseller\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/accounts-openapi-original.yml
tags:
- Accounts
---
