---
aid: microsoft-azure-one:workbookclient
baseURL: ''
description: Microsoft Azure Workbook Client is a powerful tool that allows users to visualize and analyze data from their Azure environment. This tool enables users to create custom interactive dashboards and reports to monitor the performance and health of their resources. With Azure Workbook Client, users can easily track key metrics, trends, and anomalies, making it easier to identify and address issues before they impact the overall system.
humanURL: https://learn.microsoft.com/en-us/azure/azure-monitor/visualize/workbooks-overview
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Workbook Client
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/workbookclient-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/azure-monitor/visualize/workbooks-overview
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: workbookclient
source_filename: workbookclient-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: 2018-06-17-preview\n  title: Microsoft Azure WorkbookClient\n  description: Azure client for Workbook.\nhost: management.azure.com\nschemes:\n  - https\nsecurity:\n  - azure_auth:\n      - user_impersonation\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Azure Active Directory OAuth2 Flow.\n    scopes:\n      user_impersonation: impersonate your user account\npaths:\n  /providers/Microsoft.Insights/operations:\n    get:\n      tags:\n        - Operations\n      description: Lists all of the available insights REST API operations.\n      operationId: microsoftAzureOperationsList\n      parameters:\n        - $ref: >-\n            ../../../../../common-types/resource-management/v1/types.json#/parameters/ApiVersionParameter\n      responses:\n        '200':\n          description: OK. The request has succeeded.\n     \
  \     schema:\n            $ref: '#/definitions/OperationListResult'\n        default:\n          description: Insights error response describing why the operation failed.\n          schema:\n            $ref: '#/definitions/ErrorResponse'\n      x-ms-pageable:\n        nextLinkName: nextLink\n      produces:\n        - application/json\n      consumes:\n        - application/json\n      summary: Microsoft Azure Get Providers Microsoft Insights Operations\ndefinitions:\n  ErrorResponse:\n    description: >-\n      Error response indicates Insights service is not able to process the\n      incoming request. The reason is provided in the error message.\n    type: object\n    properties:\n      code:\n        description: Error code.\n        type: string\n      message:\n        description: Error message indicating why the operation failed.\n        type: string\n  Operation:\n    description: CDN REST API operation\n    type: object\n    properties:\n      name:\n        description: 'Operation\
  \ name: {provider}/{resource}/{operation}'\n        type: string\n      display:\n        description: The object that represents the operation.\n        properties:\n          provider:\n            description: 'Service provider: Microsoft.Cdn'\n            type: string\n          resource:\n            description: >-\n              Resource on which the operation is performed: Profile, endpoint,\n              etc.\n            type: string\n          operation:\n            description: 'Operation type: Read, write, delete, etc.'\n            type: string\n  OperationListResult:\n    description: >-\n      Result of the request to list CDN operations. It contains a list of\n      operations and a URL link to get the next set of results.\n    properties:\n      value:\n        type: array\n        items:\n          $ref: '#/definitions/Operation'\n        description: List of CDN operations supported by the CDN resource provider.\n      nextLink:\n        type: string\n        description:\
  \ URL to get the next set of operation list results if there are any.\ntags:\n  - name: Operations\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/workbookclient-openapi-original.yml
tags: []
---
