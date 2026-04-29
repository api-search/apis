---
aid: microsoft-azure:workloads-client
baseURL: ''
description: Microsoft Azure Workloads Client is a powerful tool that allows users to manage and monitor their workloads in the Azure cloud environment. With this client, users can easily deploy, scale, and update their applications with just a few clicks. The client also provides detailed insights and analytics into the performance of workloads, helping users optimize their resources and improve efficiency.
humanURL: https://learn.microsoft.com/en-us/dotnet/api/overview/azure/resourcemanager.workloads-readme?view=azure-dotnet
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Workloads Client
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/workloads-client-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/dotnet/api/overview/azure/resourcemanager.workloads-readme?view=azure-dotnet
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: workloads-client
source_filename: workloads-client-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Workloads Client\n  version: 2023-10-01-preview\n  description: Workloads client provides access to various workload operations.\n  x-typespec-generated:\n    - emitter: '@azure-tools/typespec-autorest'\nschemes:\n  - https\nhost: management.azure.com\nproduces:\n  - application/json\nconsumes:\n  - application/json\nsecurity:\n  - azure_auth:\n      - user_impersonation\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    description: Azure Active Directory OAuth2 Flow.\n    flow: implicit\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    scopes:\n      user_impersonation: impersonate your user account\ntags:\n  - name: Operations\npaths:\n  /providers/Microsoft.Workloads/operations:\n    get:\n      operationId: microsoftAzureOperationsList\n      tags:\n        - Operations\n      description: List the operations for the provider\n      parameters:\n        - $ref: >-\n           \
  \ ../../../../../../common-types/resource-management/v3/types.json#/parameters/ApiVersionParameter\n      responses:\n        '200':\n          description: Azure operation completed successfully.\n          schema:\n            $ref: >-\n              ../../../../../../common-types/resource-management/v3/types.json#/definitions/OperationListResult\n        default:\n          description: An unexpected error response.\n          schema:\n            $ref: >-\n              ../../../../../../common-types/resource-management/v3/types.json#/definitions/ErrorResponse\n      x-ms-examples:\n        List the operations for the provider.:\n          $ref: ./examples/Operations_List.json\n      x-ms-pageable:\n        nextLinkName: nextLink\n      summary: Microsoft Azure Get Providers Microsoft Workloads Operations\ndefinitions:\n  Versions:\n    type: string\n    description: The available API versions.\n    enum:\n      - 2023-10-01-preview\n    x-ms-enum:\n      name: Versions\n      modelAsString:\
  \ true\n      values:\n        - name: v2023_10_01_preview\n          value: 2023-10-01-preview\n          description: The 2023-10-01-preview API version.\nparameters: {}\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/workloads-client-openapi-original.yml
tags: []
---
