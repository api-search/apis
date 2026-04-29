---
aid: cmic:cmic-api
baseURL: https://api.cmic.ca
description: CMiC provides enterprise ERP and project management software for the construction industry. The REST API uses OAuth 2.0 (client credentials flow) with support for third-party identity providers like Microsoft Azure. APIs enable access to project financials, subcontractor management, job costing, equipment tracking, and document management. Application-level security is enforced across all endpoints respecting company, job, project, and employee access rules.
humanURL: https://developers.cmicglobal.com/
image: https://raw.githubusercontent.com/api-evangelist/cmic/refs/heads/main/image.png
layout: api
name: CMiC Construction ERP API
properties:
- type: Documentation
  url: https://developers.cmicglobal.com/docs/overview
- type: Authentication
  url: https://developers.cmicglobal.com/v1/docs/authentication
- type: GettingStarted
  url: https://developers.cmicglobal.com/docs/developer-api-account
- type: Reference
  url: https://docs.cmicglobal.com/portal/Content/E_Reference_Material/CMiC_API/Reference/API_and_OAuth2/API_and_OAuth2.htm
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cmic/refs/heads/main/openapi/cmic-construction-erp-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cmic/refs/heads/main/json-schema/cmic-project-schema.json
- type: JSONLDContext
  url: https://raw.githubusercontent.com/api-evangelist/cmic/refs/heads/main/json-ld/cmic-context.jsonld
- type: SpectralRuleset
  url: https://raw.githubusercontent.com/api-evangelist/cmic/refs/heads/main/rules/cmic-rules.yml
- type: NaftikoCapabilities
  url: https://raw.githubusercontent.com/api-evangelist/cmic/refs/heads/main/capabilities/cmic-construction-erp-capabilities.yml
provider_name: CMiC
provider_slug: cmic
slug: cmic-api
source_yaml: "aid: cmic:cmic-api\nname: CMiC Construction ERP API\ntags:\n- Construction\n- ERP\n- Finance\n- OAuth2\n- Project Management\nimage: https://raw.githubusercontent.com/api-evangelist/cmic/refs/heads/main/image.png\nhumanURL: https://developers.cmicglobal.com/\nbaseURL: https://api.cmic.ca\nproperties:\n- url: https://developers.cmicglobal.com/docs/overview\n  type: Documentation\n- url: https://developers.cmicglobal.com/v1/docs/authentication\n  type: Authentication\n- url: https://developers.cmicglobal.com/docs/developer-api-account\n  type: GettingStarted\n- url: https://docs.cmicglobal.com/portal/Content/E_Reference_Material/CMiC_API/Reference/API_and_OAuth2/API_and_OAuth2.htm\n  type: Reference\n- url: openapi/cmic-construction-erp-openapi.yml\n  type: OpenAPI\n- url: json-schema/cmic-project-schema.json\n  type: JSONSchema\n- url: json-ld/cmic-context.jsonld\n  type: JSONLDContext\n- url: rules/cmic-rules.yml\n  type: SpectralRuleset\n- url: capabilities/cmic-construction-erp-capabilities.yml\n\
  \  type: NaftikoCapabilities\ndescription: CMiC provides enterprise ERP and project management software for the construction industry.\n  The REST API uses OAuth 2.0 (client credentials flow) with support for third-party identity providers\n  like Microsoft Azure. APIs enable access to project financials, subcontractor management, job costing,\n  equipment tracking, and document management. Application-level security is enforced across all endpoints\n  respecting company, job, project, and employee access rules.\nx-features:\n- name: Project Management\n  description: List, create, retrieve, and update construction projects.\n- name: Job Cost Tracking\n  description: Track jobs, cost codes, budgets, and committed costs.\n- name: Subcontractor and Vendor Management\n  description: List and manage vendors and subcontractors per company.\n- name: Equipment Tracking\n  description: Track equipment, usage, and assignment.\n- name: Document Management\n  description: List and retrieve project\
  \ documents and approvals.\n- name: OAuth 2.0 Authentication\n  description: Client credentials flow with Microsoft Azure / external IdP support.\nx-useCases:\n- name: Project Financials Dashboard\n  description: Surface project, job, and cost-code data in BI tools.\n- name: Subcontractor Onboarding\n  description: Sync vendor and subcontractor records into procurement systems.\n- name: Equipment Utilization\n  description: Drive equipment-utilization reporting and predictive maintenance.\n- name: Document Workflow Automation\n  description: Push and pull project documents into external review workflows.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cmic/refs/heads/main/apis.yml
tags:
- Construction
- ERP
- Finance
- OAuth2
- Project Management
---
