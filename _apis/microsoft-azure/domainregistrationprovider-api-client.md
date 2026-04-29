---
aid: microsoft-azure:domainregistrationprovider-api-client
baseURL: ''
description: The Microsoft Azure Domain Registration Provider API Client is a tool that allows users to manage their domain registrations through the Microsoft Azure platform. This client provides an easy and convenient way to register, renew, and manage domain names directly within the Azure environment. Users can access their domain settings, update contact information, configure DNS records, and view important domain details all from a single interface.
humanURL: https://learn.microsoft.com/en-us/rest/api/azure/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Domain Registration Provider API Client
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/domainregistrationprovider-api-client-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/rest/api/azure/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: domainregistrationprovider-api-client
source_filename: domainregistrationprovider-api-client-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: '2023-01-01'\n  title: Microsoft Azure DomainRegistrationProvider API Client\nhost: management.azure.com\nschemes:\n  - https\nconsumes:\n  - application/json\nproduces:\n  - application/json\npaths:\n  /providers/Microsoft.DomainRegistration/operations:\n    get:\n      tags:\n        - DomainRegistrationProvider\n      summary: >-\n        Microsoft Azure Implements Csm Operations Api To Exposes The List Of Available Csm Apis Under The Resource Provider\n      description: >-\n        Description for Implements Csm operations Api to exposes the list of\n        available Csm Apis under the resource provider\n      operationId: microsoftAzureDomainregistrationproviderListoperations\n      parameters:\n        - $ref: '#/parameters/apiVersionParameter'\n      responses:\n        '200':\n          description: OK\n          schema:\n            $ref: >-\n              ../../../Microsoft.Web/stable/2023-01-01/CommonDefinitions.json#/definitions/CsmOperationCollection\n\
  \        default:\n          description: App Service error response.\n          schema:\n            $ref: >-\n              ../../../Microsoft.Web/stable/2023-01-01/CommonDefinitions.json#/definitions/DefaultErrorResponse\n      x-ms-examples:\n        List operations:\n          $ref: ./examples/ListOperations.json\n      x-ms-pageable:\n        nextLinkName: nextLink\ndefinitions: {}\nparameters:\n  subscriptionIdParameter:\n    name: subscriptionId\n    in: path\n    description: >-\n      Your Azure subscription ID. This is a GUID-formatted string (e.g.\n      00000000-0000-0000-0000-000000000000).\n    required: true\n    type: string\n  apiVersionParameter:\n    name: api-version\n    in: query\n    description: API Version\n    required: true\n    type: string\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    description: Azure Active Directory OAuth2 Flow\n    flow: implicit\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    scopes:\n\
  \      user_impersonation: impersonate your user account\nsecurity:\n  - azure_auth:\n      - user_impersonation\ntags:\n  - name: DomainRegistrationProvider\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/domainregistrationprovider-api-client-openapi-original.yml
tags: []
---
