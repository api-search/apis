---
aid: microsoft-azure:security-insights
baseURL: ''
description: Microsoft Azure Security Insights is a comprehensive security solution that provides deep visibility into the security posture of an organization's Azure environment. It monitors and analyzes security events and alerts from various sources, such as Azure Security Center, Azure Sentinel, and third-party security tools, to detect potential threats and vulnerabilities.
humanURL: https://learn.microsoft.com/en-us/dotnet/api/overview/azure/resourcemanager.securityinsights-readme?view=azure-dotnet
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Security Insights
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/security-insights-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/dotnet/api/overview/azure/resourcemanager.securityinsights-readme?view=azure-dotnet
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: security-insights
source_filename: security-insights-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Security Insights\n  description: >-\n    API spec for Microsoft.SecurityInsights (Azure Security Insights) resource\n    provider\n  version: 2024-01-01-preview\nhost: management.azure.com\nschemes:\n  - https\nconsumes:\n  - application/json\nproduces:\n  - application/json\nsecurity:\n  - azure_auth:\n      - user_impersonation\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Azure Active Directory OAuth2 Flow\n    scopes:\n      user_impersonation: impersonate your user account\npaths:\n  /providers/Microsoft.SecurityInsights/operations:\n    get:\n      x-ms-examples:\n        Get all operations.:\n          $ref: ./examples/operations/ListOperations.json\n      operationId: microsoftAzureOperationsList\n      description: >-\n        Lists all operations available Azure Security Insights Resource\n\
  \        Provider.\n      parameters:\n        - $ref: >-\n            ../../../../../common-types/resource-management/v3/types.json#/parameters/ApiVersionParameter\n      produces:\n        - application/json\n      responses:\n        '200':\n          description: OK. Successfully retrieved operations list.\n          schema:\n            $ref: '#/definitions/OperationsList'\n        default:\n          description: Error response describing why the operation failed.\n          schema:\n            $ref: ../../../common/2.0/types.json#/definitions/CloudError\n      x-ms-pageable:\n        nextLinkName: nextLink\n      summary: Microsoft Azure Get Providers Microsoft Securityinsights Operations\n      tags:\n        - Providers\ndefinitions:\n  OperationsList:\n    description: Lists the operations available in the SecurityInsights RP.\n    properties:\n      nextLink:\n        description: URL to fetch the next set of operations.\n        type: string\n        readOnly: true\n     \
  \ value:\n        description: Array of operations\n        items:\n          $ref: '#/definitions/Operation'\n        type: array\n    required:\n      - value\n    type: object\n  Operation:\n    description: Operation provided by provider\n    properties:\n      display:\n        description: Properties of the operation\n        properties:\n          description:\n            description: Description of the operation\n            type: string\n          operation:\n            description: Operation name\n            type: string\n          provider:\n            description: Provider name\n            type: string\n          resource:\n            description: Resource name\n            type: string\n        type: object\n      name:\n        description: Name of the operation\n        type: string\n      origin:\n        description: The origin of the operation\n        type: string\n      isDataAction:\n        description: Indicates whether the operation is a data action\n    \
  \    type: boolean\n    type: object\nparameters: {}\ntags:\n  - name: Providers\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/security-insights-openapi-original.yml
tags: []
---
