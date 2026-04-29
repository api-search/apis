---
aid: microsoft-azure:ingestion-using-data-collection-rules
baseURL: ''
description: Microsoft Azure Ingestion Using Data Collection Rules is a feature that allows organizations to easily and efficiently ingest large amounts of data into their Azure environment. By creating data collection rules, users can specify how data should be collected, transformed, and stored, making the ingestion process more streamlined and automated.
humanURL: https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/data-collection-rule-overview
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Ingestion Using Data Collection Rules
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/ingestion-using-data-collection-rules-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/data-collection-rule-overview
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: ingestion-using-data-collection-rules
source_filename: ingestion-using-data-collection-rules-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Ingestion Using Data Collection Rules\n  version: '2023-01-01'\nx-ms-parameterized-host:\n  hostTemplate: '{endpoint}'\n  useSchemePrefix: false\n  parameters:\n    - $ref: '#/parameters/Endpoint'\nschemes:\n  - https\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Azure Active Directory OAuth2 Flow\n    scopes:\n      user_impersonation: impersonate your user account\nsecurity:\n  - azure_auth:\n      - user_impersonation\npaths:\n  /dataCollectionRules/{ruleId}/streams/{stream}:\n    post:\n      tags:\n        - Data Collection Rules\n      summary: Microsoft Azure Ingestion Api Used To Directly Ingest Data Using Data Collection Rules\n      description: See error response code and error response message for more detail.\n      operationId: microsoftAzureUpload\n      consumes:\n        - application/json\n\
  \      produces:\n        - application/json\n      parameters:\n        - in: path\n          name: ruleId\n          description: The immutable Id of the Data Collection Rule resource.\n          required: true\n          type: string\n        - in: path\n          name: stream\n          description: The streamDeclaration name as defined in the Data Collection Rule.\n          required: true\n          type: string\n        - in: query\n          name: api-version\n          required: true\n          type: string\n          description: The API version to use for this operation.\n        - in: header\n          name: Content-Encoding\n          description: gzip\n          type: string\n        - in: header\n          name: x-ms-client-request-id\n          description: Client request Id\n          type: string\n        - in: body\n          name: body\n          description: >-\n            An array of objects matching the schema defined by the provided\n            stream.\n     \
  \     required: true\n          schema:\n            type: array\n            items:\n              type: object\n      x-ms-examples:\n        postIngestUsingDataCollectionRule:\n          $ref: ./examples/post_IngestUsingDataCollectionRule.json\n      responses:\n        '204':\n          description: Ingestion request accepted\n        default:\n          description: An error response object.\n          schema:\n            $ref: >-\n              ../../../../../common-types/data-plane/v1/types.json#/definitions/ErrorResponse\n          headers:\n            x-ms-error-code:\n              description: A value that indicates the ingestion service error code.\n              type: string\ndefinitions: {}\nparameters:\n  Endpoint:\n    name: endpoint\n    description: >-\n      The Data Collection Endpoint for the Data Collection Rule, for example\n      https://dce-name.eastus-2.ingest.monitor.azure.com.\n    required: true\n    type: string\n    in: path\n    x-ms-skip-url-encoding:\
  \ true\n    x-ms-parameter-location: client\ntags:\n  - name: Data Collection Rules\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/ingestion-using-data-collection-rules-openapi-original.yml
tags: []
---
