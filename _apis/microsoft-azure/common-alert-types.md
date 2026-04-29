---
aid: microsoft-azure:common-alert-types
baseURL: ''
description: Microsoft Azure Common Alert Types is a feature that allows users to set up alerts for various events and occurrences within their Azure environment. These alerts can be customized to monitor specific metrics, such as CPU usage, storage levels, or connectivity issues. Users can choose from a variety of alert types, such as email notifications or integrations with third-party monitoring tools.
humanURL: https://learn.microsoft.com/en-us/azure/azure-monitor/alerts/alerts-types
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Common Alert Types
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-alert-types-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/azure-monitor/alerts/alerts-types
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: common-alert-types
source_filename: common-alert-types-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: 2024-01-01-preview\n  title: Microsoft Azure Common Alert types\npaths: {}\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Azure Active Directory OAuth2 Flow\n    scopes:\n      user_impersonation: impersonate your user account\ndefinitions:\n  AlertSeverityEnum:\n    description: The severity of the alert\n    enum:\n      - High\n      - Medium\n      - Low\n      - Informational\n    type: string\n    x-ms-enum:\n      modelAsString: true\n      name: AlertSeverity\n      values:\n        - description: High severity\n          value: High\n        - description: Medium severity\n          value: Medium\n        - description: Low severity\n          value: Low\n        - description: Informational severity\n          value: Informational\n  AttackTactic:\n    description: The severity for alerts created by this alert\
  \ rule.\n    enum:\n      - Reconnaissance\n      - ResourceDevelopment\n      - InitialAccess\n      - Execution\n      - Persistence\n      - PrivilegeEscalation\n      - DefenseEvasion\n      - CredentialAccess\n      - Discovery\n      - LateralMovement\n      - Collection\n      - Exfiltration\n      - CommandAndControl\n      - Impact\n      - PreAttack\n      - ImpairProcessControl\n      - InhibitResponseFunction\n    type: string\n    x-ms-enum:\n      modelAsString: true\n      name: AttackTactic\nparameters: {}\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-alert-types-openapi-original.yml
tags: []
---
