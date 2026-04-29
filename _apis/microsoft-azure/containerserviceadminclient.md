---
aid: microsoft-azure:containerserviceadminclient
baseURL: ''
description: Microsoft Azure Container Service Admin Client is a powerful tool that allows administrators to manage and monitor their containerized applications in the Azure cloud environment. This client provides a user-friendly interface for deploying, scaling, and updating container instances, as well as managing network configurations and workload scheduling.
humanURL: https://learn.microsoft.com/en-us/azure/containers/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Container Service Admin Client
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/containerserviceadminclient-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/containers/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: containerserviceadminclient
source_filename: containerserviceadminclient-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: '2019-11-01'\n  title: Microsoft Azure ContainerServiceAdminClient\n  description: Admin Container Service Management Client.\nhost: management.azure.com\nschemes:\n  - https\nconsumes:\n  - application/json\nproduces:\n  - application/json\npaths:\n  /subscriptions/{subscriptionId}/providers/Microsoft.ContainerService.Admin/locations/{location}/quotas:\n    get:\n      x-ms-examples:\n        Returns a list of container service quotas at the given location.:\n          $ref: ./examples/Quotas/List.json\n      tags:\n        - ContainerServiceQuotas\n      description: Returns a list of container service quotas at the given location.\n      operationId: microsoftAzureContainerservicequotaList\n      parameters:\n        - $ref: >-\n            ../../../../../../common-types/resource-management/v2/types.json#/parameters/SubscriptionIdParameter\n        - $ref: >-\n            ../../../../../../common-types/resource-management/v2/types.json#/parameters/LocationParameter\n\
  \        - $ref: >-\n            ../../../../../../common-types/resource-management/v2/types.json#/parameters/ApiVersionParameter\n      responses:\n        '200':\n          description: OK -- The list of container service quotas has been returned.\n          schema:\n            $ref: '#/definitions/ContainerServiceQuotaList'\n        default:\n          description: Error Response.\n          schema:\n            $ref: >-\n              ../../../../../../common-types/resource-management/v2/types.json#/definitions/ErrorResponse\n      x-ms-pageable:\n        nextLinkName: nextLink\n      summary: >-\n        Microsoft Azure Get Subscriptions Subscriptionid Providers Microsoft Containerservice Admin Locations Location Quotas\ndefinitions:\n  ContainerServiceQuotaProperties:\n    description: Container service quota properties.\n    type: object\n    properties:\n      name:\n        description: Container service storage capacity\n        type: string\n        default: unlimited\n  ContainerServiceQuotaList:\n\
  \    description: List of container service quotas.\n    type: object\n    properties:\n      value:\n        description: List of container service quotas.\n        type: array\n        items:\n          description: Container service quota.\n          type: object\n          properties:\n            properties:\n              description: Container service quota properties.\n              x-ms-client-flatten: true\n              $ref: '#/definitions/ContainerServiceQuotaProperties'\n          allOf:\n            - $ref: >-\n                ../../../../../../common-types/resource-management/v2/types.json#/definitions/Resource\n      nextLink:\n        description: URI to the next page.\n        type: string\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Authorization uses an Azure Active Directory OAuth2 flow.\n    scopes:\n      user_impersonation: impersonate\
  \ your user account\nsecurity:\n  - azure_auth:\n      - user_impersonation\ntags:\n  - name: ContainerServiceQuotas\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/containerserviceadminclient-openapi-original.yml
tags: []
---
