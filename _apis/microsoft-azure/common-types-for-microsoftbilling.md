---
aid: microsoft-azure-one:common-types-for-microsoftbilling
baseURL: ''
description: Microsoft Azure Common Types For Microsoft Billing is a comprehensive tool that provides users with a variety of options for managing their billing and invoicing needs within the Microsoft Azure platform. This tool allows users to easily track and monitor their usage and spending, as well as set up automated billing processes to ensure accurate and timely payments.
humanURL: https://learn.microsoft.com/en-us/azure/cost-management-billing/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Common Types for Microsoft Billing
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-types-for-microsoftbilling-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/cost-management-billing/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: common-types-for-microsoftbilling
source_filename: common-types-for-microsoftbilling-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: '2021-10-01'\n  title: Microsoft Azure Common types for Microsoft.Billing\npaths: {}\ndefinitions:\n  ErrorResponse:\n    description: >-\n      Error response indicates that the service is not able to process the\n      incoming request. The reason is provided in the error message.\n    type: object\n    properties:\n      error:\n        description: The details of the error.\n        $ref: '#/definitions/ErrorDetails'\n  ErrorDetails:\n    description: The details of the error.\n    type: object\n    properties:\n      code:\n        description: Error code.\n        type: string\n        readOnly: true\n      message:\n        description: Error message indicating why the operation failed.\n        type: string\n        readOnly: true\n      target:\n        description: The target of the particular error.\n        type: string\n        readOnly: true\n      details:\n        description: The sub details of the error.\n        $ref: '#/definitions/ErrorSubDetails'\n\
  \  ErrorSubDetails:\n    description: The sub details of the error.\n    type: array\n    items:\n      type: object\n      properties:\n        code:\n          description: Error code.\n          type: string\n          readOnly: true\n        message:\n          description: Error message indicating why the operation failed.\n          type: string\n          readOnly: true\n        target:\n          description: The target of the particular error.\n          type: string\n          readOnly: true\n  Resource:\n    description: The resource model definition.\n    type: object\n    properties:\n      id:\n        readOnly: true\n        type: string\n        description: Resource Id.\n      name:\n        readOnly: true\n        type: string\n        description: Resource name.\n      type:\n        readOnly: true\n        type: string\n        description: Resource type.\n    x-ms-azure-resource: true\nparameters:\n  apiVersionParameter:\n    name: api-version\n    in: query\n    required:\
  \ true\n    type: string\n    description: >-\n      The version of the API to be used with the client request. The current\n      version is 2021-10-01.\nsecurity:\n  - azure_auth:\n      - user_impersonation\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Azure Active Directory OAuth2 Flow.\n    scopes:\n      user_impersonation: impersonate your user account\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-types-for-microsoftbilling-openapi-original.yml
tags: []
---
