---
aid: microsoft-azure:policy-insights-operations-api
baseURL: ''
description: Microsoft Azure Policy Insights Operations API allows users to monitor and analyze policy compliance across their Azure environment. By providing a central hub for viewing policy insights, users can easily track policy evaluations, view compliance trends, and identify any areas of non-compliance. This API enables users to gain valuable insights into their Azure policies, helping them to make informed decisions and take necessary actions to maintain a secure and compliant cloud environment.
humanURL: https://learn.microsoft.com/en-us/rest/api/policy/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Policy Insights Operations API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/policy-insights-operations-api-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/rest/api/policy/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: policy-insights-operations-api
source_filename: policy-insights-operations-api-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Policy Insights Operations API\n  version: '2022-04-01'\nhost: management.azure.com\nschemes:\n  - https\nconsumes:\n  - application/json\nproduces:\n  - application/json\nsecurity:\n  - azure_auth:\n      - user_impersonation\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Azure Active Directory OAuth2 Flow\n    scopes:\n      user_impersonation: impersonate your user account\npaths:\n  /providers/Microsoft.PolicyInsights/operations:\n    get:\n      operationId: microsoftAzureOperationsList\n      description: Lists available operations.\n      parameters:\n        - $ref: '#/parameters/apiVersionParameter'\n      responses:\n        '200':\n          description: List of available operations.\n          schema:\n            $ref: '#/definitions/OperationsListResults'\n        default:\n          description:\
  \ Error response describing why the operation failed.\n          schema:\n            $ref: ../../stable/2019-10-01/operations.json#/definitions/QueryFailure\n      x-ms-examples:\n        List operations:\n          $ref: ./examples/Operations_ListOperations.json\n      summary: Microsoft Azure Get Providers Microsoft Policyinsights Operations\n      tags:\n        - Providers\ndefinitions:\n  OperationsListResults:\n    description: List of available operations.\n    type: object\n    properties:\n      '@odata.count':\n        description: OData entity count; represents the number of operations returned.\n        type: integer\n        format: int32\n        minimum: 1\n      value:\n        description: List of available operations.\n        type: array\n        items:\n          $ref: '#/definitions/Operation'\n        x-ms-identifiers:\n          - name\n  Operation:\n    description: Operation definition.\n    type: object\n    properties:\n      name:\n        description: Operation\
  \ name.\n        type: string\n      isDataAction:\n        description: Indicates whether the operation is a data action\n        type: boolean\n      display:\n        description: Display metadata associated with the operation.\n        type: object\n        properties:\n          provider:\n            description: Resource provider name.\n            type: string\n          resource:\n            description: Resource name on which the operation is performed.\n            type: string\n          operation:\n            description: Operation name.\n            type: string\n          description:\n            description: Operation description.\n            type: string\nparameters:\n  apiVersionParameter:\n    name: api-version\n    in: query\n    required: true\n    type: string\n    description: API version to use with the client requests.\n    x-ms-parameter-location: client\ntags:\n  - name: Providers\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/policy-insights-operations-api-openapi-original.yml
tags: []
---
