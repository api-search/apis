---
aid: microsoft-azure:bicepclient
baseURL: ''
description: The Microsoft Azure Bicep Client is a tool that allows users to author and deploy infrastructure as code on the Azure cloud platform. It enables developers to define and manage Azure resources using a declarative syntax that is easier to read and write than traditional template languages like JSON or ARM templates. With Bicep, users can create reusable modules, parameterize their configurations, and validate their code for best practices and compliance.
humanURL: https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Bicep Client
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/bicepclient-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: bicepclient
source_filename: bicepclient-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure BicepClient\n  description: >-\n    The APIs listed in this specification can be used to manage Bicep related\n    operations through the Azure Resource Manager.\n  version: '2023-11-01'\nhost: management.azure.com\nschemes:\n  - https\nconsumes:\n  - application/json\nproduces:\n  - application/json\nsecurity:\n  - azure_auth:\n      - user_impersonation\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Azure Active Directory OAuth2 Flow\n    scopes:\n      user_impersonation: impersonate your user account\npaths:\n  /subscriptions/{subscriptionId}/providers/Microsoft.Resources/decompileBicep:\n    post:\n      tags:\n        - BicepClient\n      operationId: microsoftAzureDecompileBicep\n      description: Decompiles an ARM json template into a Bicep template\n      x-ms-examples:\n        Decompile an\
  \ ARM json template into a Bicep file:\n          $ref: ./examples/DecompileBicep.json\n      parameters:\n        - $ref: >-\n            ../../../../../common-types/resource-management/v5/types.json#/parameters/SubscriptionIdParameter\n        - $ref: >-\n            ../../../../../common-types/resource-management/v5/types.json#/parameters/ApiVersionParameter\n        - name: decompileOperationRequest\n          in: body\n          required: true\n          schema:\n            $ref: '#/definitions/DecompileOperationRequest'\n          description: Decompile operation request supplied to the operation.\n      responses:\n        '200':\n          description: OK - The decompilation has succeeded.\n          schema:\n            $ref: '#/definitions/DecompileOperationSuccessResponse'\n        default:\n          description: Error response describing why the operation failed.\n          schema:\n            $ref: >-\n              ../../../../../common-types/resource-management/v5/types.json#/definitions/ErrorResponse\n\
  \      summary: >-\n        Microsoft Azure Post Subscriptions Subscriptionid Providers Microsoft Resources Decompilebicep\ndefinitions:\n  DecompileOperationRequest:\n    required:\n      - template\n    type: object\n    description: The body of the request for the decompileBicep operation\n    properties:\n      template:\n        type: string\n        description: The ARM json template to be decompiled into a Bicep file\n  DecompileOperationSuccessResponse:\n    required:\n      - files\n      - entryPoint\n    type: object\n    description: The response of the decompileBicep operation\n    properties:\n      files:\n        type: array\n        items:\n          $ref: '#/definitions/FileDefinition'\n        x-ms-identifiers:\n          - path\n        description: >-\n          An array of key-value pairs containing the entryPoint string as the\n          key for the Bicep file decompiled from the ARM json template\n      entryPoint:\n        type: string\n        description: >-\n\
  \          The file path to the main Bicep file generated from the decompiled ARM\n          json template.\n  FileDefinition:\n    type: object\n    properties:\n      path:\n        type: string\n      contents:\n        type: string\n    description: The definition of a file along with its contents\ntags:\n  - name: BicepClient\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/bicepclient-openapi-original.yml
tags: []
---
