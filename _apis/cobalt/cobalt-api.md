---
aid: cobalt:cobalt-api
baseURL: https://api.gocobalt.io/api/v2
description: The Cobalt API enables developers to programmatically manage integrations, linked accounts, configurations, events, webhooks, executions, public workflows, and datastores within the Cobalt embedded integration platform. Cobalt helps product and engineering teams build native integrations, deploy them within days, and monetize them with the help of AI agents.
humanURL: https://docs.gocobalt.io/api-reference/overview
image: ''
layout: api
name: Cobalt API
properties:
- type: Documentation
  url: https://docs.gocobalt.io/api-reference/overview
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/openapi/cobalt-api-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/json-schema/linked-account.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/json-schema/application.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/json-schema/config.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/json-schema/webhook.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/json-schema/execution.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/json-schema/workflow.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/json-schema/datastore.json
- type: JSONLDContext
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/json-ld/cobalt-context.jsonld
- type: SpectralRuleset
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/rules/cobalt-rules.yml
- type: NaftikoCapabilities
  url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/capabilities/cobalt-api-capabilities.yml
provider_name: Cobalt
provider_slug: cobalt
slug: cobalt-api
source_yaml: "aid: cobalt:cobalt-api\nname: Cobalt API\ntags:\n- Automation\n- Embedded SaaS Integration\n- Integrations\n- iPaaS\nhumanURL: https://docs.gocobalt.io/api-reference/overview\nbaseURL: https://api.gocobalt.io/api/v2\nproperties:\n- url: https://docs.gocobalt.io/api-reference/overview\n  type: Documentation\n- url: openapi/cobalt-api-openapi.yml\n  type: OpenAPI\n- url: json-schema/linked-account.json\n  type: JSONSchema\n- url: json-schema/application.json\n  type: JSONSchema\n- url: json-schema/config.json\n  type: JSONSchema\n- url: json-schema/webhook.json\n  type: JSONSchema\n- url: json-schema/execution.json\n  type: JSONSchema\n- url: json-schema/workflow.json\n  type: JSONSchema\n- url: json-schema/datastore.json\n  type: JSONSchema\n- url: json-ld/cobalt-context.jsonld\n  type: JSONLDContext\n- url: rules/cobalt-rules.yml\n  type: SpectralRuleset\n- url: capabilities/cobalt-api-capabilities.yml\n  type: NaftikoCapabilities\nx-features:\n- name: Linked Accounts\n  description:\
  \ Manage end-customer linked accounts representing each tenant of your SaaS.\n- name: Applications Catalog\n  description: Browse the 1,000+ third-party applications Cobalt can connect to.\n- name: Configurations\n  description: Per-linked-account configuration of integration settings and dynamic fields.\n- name: Events and Webhooks\n  description: Trigger Cobalt events and subscribe to webhooks for real-time notifications.\n- name: Workflows\n  description: Build, deploy, and execute integration workflows publicly or per-tenant.\n- name: Executions\n  description: Inspect workflow execution history and logs.\n- name: Datastores\n  description: Persist integration state with Cobalt-managed datastores.\n- name: Cobalt Hosted Portal\n  description: Generate hosted portal URLs to embed Cobalt UI for end customers.\n- name: Session Tokens\n  description: Short-lived tokens to authenticate frontend SDK calls per linked account.\nx-useCases:\n- name: Embedded Integrations Marketplace\n  description:\
  \ Offer customers a turnkey integrations marketplace inside your SaaS product.\n- name: Per-Tenant Workflow Automation\n  description: Run customer-specific automations across CRM, billing, support, and HR systems.\n- name: AI Integration Agents\n  description: Use Cobalt's AI capabilities to build agentic workflows over connected SaaS apps.\n- name: Native Connector Replacement\n  description: Replace dozens of point-to-point connectors with one embedded iPaaS.\ndescription: The Cobalt API enables developers to programmatically manage integrations, linked accounts,\n  configurations, events, webhooks, executions, public workflows, and datastores within the Cobalt embedded\n  integration platform. Cobalt helps product and engineering teams build native integrations, deploy them\n  within days, and monetize them with the help of AI agents.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cobalt/refs/heads/main/apis.yml
tags:
- Automation
- Embedded SaaS Integration
- Integrations
- iPaaS
---
