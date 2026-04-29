---
aid: microsoft-azure:azure-monitor-workspaces-control-plane-api
baseURL: ''
description: The Microsoft Azure Monitor Workspaces Control Plane API is a tool that provides control and management capabilities for monitoring workspaces deployed within the Azure cloud environment. This API allows users to create, manage, and delete monitoring workspaces, as well as configure and customize monitoring settings.
humanURL: https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/monitor-resource-manager
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Monitor Workspaces Control Plane API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/azure-monitor-workspaces-control-plane-api-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/monitor-resource-manager
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: azure-monitor-workspaces-control-plane-api
source_filename: azure-monitor-workspaces-control-plane-api-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Azure Monitor Workspaces Control Plane API\n  description: Provides operations for working with Azure Monitor Workspaces\n  version: '2023-04-03'\n  x-ms-code-generation-settings:\n    name: MonitorManagementClient\n  contact:\n    email: obsaccounts@microsoft.com\nhost: management.azure.com\nschemes:\n  - https\nconsumes:\n  - application/json\nproduces:\n  - application/json\nsecurity:\n  - azure_auth:\n      - user_impersonation\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    flow: implicit\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    scopes:\n      user_impersonation: impersonate your user account\n    description: Azure Active Directory OAuth2 Flow\ntags:\n  - name: Operations\n    description: List available operations API\npaths:\n  /providers/Microsoft.Monitor/operations:\n    get:\n      tags:\n        - Operations\n      description: Lists available Operations for\
  \ this Resource Provider\n      operationId: microsoftAzureMonitoroperationsList\n      produces:\n        - application/json\n      parameters:\n        - $ref: >-\n            ../../../../../common-types/resource-management/v3/types.json#/parameters/ApiVersionParameter\n      responses:\n        '200':\n          description: Success\n          schema:\n            $ref: >-\n              ../../../../../common-types/resource-management/v3/types.json#/definitions/OperationListResult\n        default:\n          description: Error\n          schema:\n            $ref: >-\n              ../../../../../common-types/resource-management/v3/types.json#/definitions/ErrorResponse\n      x-ms-pageable:\n        nextLinkName: nextLink\n      x-ms-examples:\n        Get operations list:\n          $ref: ./examples/OperationsGet.json\n      summary: Microsoft Azure Get Providers Microsoft Monitor Operations\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/azure-monitor-workspaces-control-plane-api-openapi-original.yml
tags: []
---
