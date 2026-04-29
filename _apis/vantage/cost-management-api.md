---
aid: vantage:cost-management-api
baseURL: https://api.vantage.sh/v2
description: The Vantage Cost Management API (v2) provides programmatic access to cloud cost data and enables automation of cost management workflows. Create and manage Cost Reports, Folders, Dashboards, Saved Filters, Teams, Budgets, Anomaly Alerts, Business Metrics, Network Flow Reports, Financial Commitment Reports, Resource Reports, Segments, Integrations, and more. Supports the Vantage Query Language (VQL) for filtering cost data across multiple cloud providers.
humanURL: https://docs.vantage.sh/api
image: ''
layout: api
name: Vantage Cost Management API
properties:
- type: Documentation
  url: https://vantage.readme.io/reference/general
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/openapi/vantage-cost-management-api-openapi.yml
- type: OpenAPI
  url: https://api.vantage.sh/v2/oas_v3.json
- type: OpenAPI
  url: https://api.vantage.sh/v2/swagger.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/cost-report.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/cost.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/folder.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/dashboard.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/saved-filter.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/workspace.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/team.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/access-grant.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/budget-alert.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/anomaly-alert.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/recommendation.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/segment.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/integration.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/managed-account.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/cost-provider.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/business-metric.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/resource-report.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/resource.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/network-flow-report.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/financial-commitment-report.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-schema/kubernetes-efficiency-report.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/json-ld/vantage-context.jsonld
provider_name: Vantage
provider_slug: vantage
slug: cost-management-api
source_yaml: "aid: vantage:cost-management-api\nname: Vantage Cost Management API\ntags:\n- Anomaly Detection\n- Budgets\n- Cloud Costs\n- Cost Reports\n- Dashboards\n- FinOps\nhumanURL: https://docs.vantage.sh/api\nproperties:\n- url: https://vantage.readme.io/reference/general\n  type: Documentation\n- url: openapi/vantage-cost-management-api-openapi.yml\n  type: OpenAPI\n- url: https://api.vantage.sh/v2/oas_v3.json\n  type: OpenAPI\n- url: https://api.vantage.sh/v2/swagger.json\n  type: OpenAPI\n- url: json-schema/cost-report.json\n  type: JSONSchema\n- url: json-schema/cost.json\n  type: JSONSchema\n- url: json-schema/folder.json\n  type: JSONSchema\n- url: json-schema/dashboard.json\n  type: JSONSchema\n- url: json-schema/saved-filter.json\n  type: JSONSchema\n- url: json-schema/workspace.json\n  type: JSONSchema\n- url: json-schema/team.json\n  type: JSONSchema\n- url: json-schema/access-grant.json\n  type: JSONSchema\n- url: json-schema/budget-alert.json\n  type: JSONSchema\n- url:\
  \ json-schema/anomaly-alert.json\n  type: JSONSchema\n- url: json-schema/recommendation.json\n  type: JSONSchema\n- url: json-schema/segment.json\n  type: JSONSchema\n- url: json-schema/integration.json\n  type: JSONSchema\n- url: json-schema/managed-account.json\n  type: JSONSchema\n- url: json-schema/cost-provider.json\n  type: JSONSchema\n- url: json-schema/business-metric.json\n  type: JSONSchema\n- url: json-schema/resource-report.json\n  type: JSONSchema\n- url: json-schema/resource.json\n  type: JSONSchema\n- url: json-schema/network-flow-report.json\n  type: JSONSchema\n- url: json-schema/financial-commitment-report.json\n  type: JSONSchema\n- url: json-schema/kubernetes-efficiency-report.json\n  type: JSONSchema\n- url: json-ld/vantage-context.jsonld\n  type: JSONLD\ndescription: The Vantage Cost Management API (v2) provides programmatic access to cloud cost data and\n  enables automation of cost management workflows. Create and manage Cost Reports, Folders, Dashboards,\n  Saved\
  \ Filters, Teams, Budgets, Anomaly Alerts, Business Metrics, Network Flow Reports, Financial Commitment\n  Reports, Resource Reports, Segments, Integrations, and more. Supports the Vantage Query Language (VQL)\n  for filtering cost data across multiple cloud providers.\nbaseURL: https://api.vantage.sh/v2\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vantage/refs/heads/main/apis.yml
tags:
- Anomaly Detection
- Budgets
- Cloud Costs
- Cost Reports
- Dashboards
- FinOps
---
