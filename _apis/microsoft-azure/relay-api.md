---
aid: microsoft-azure:relay-api
baseURL: ''
description: Microsoft Azure Relay API provides a secure way to establish communication between on-premises and cloud-based applications, enabling seamless data exchange and interaction between different environments. By acting as a bridge between the two, the Azure Relay API allows for real-time messaging and event-driven scenarios, making it easier for organizations to integrate their systems and services.
humanURL: https://learn.microsoft.com/en-us/rest/api/relay/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Relay API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/relay-api-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/rest/api/relay/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: relay-api
source_filename: relay-api-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Relay API\n  description: >-\n    Use these API to manage Azure Relay resources through Azure Resource\n    Manager.\n  version: 2018-01-01-preview\n  x-ms-code-generation-settings:\n    name: RelayManagementClient\nhost: management.azure.com\nschemes:\n  - https\nconsumes:\n  - application/json\nproduces:\n  - application/json\nsecurity:\n  - azure_auth:\n      - user_impersonation\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Azure Active Directory OAuth2 Flow\n    scopes:\n      user_impersonation: impersonate your user account\npaths:\n  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Relay/namespaces/{namespaceName}/privateLinkResources\n  : get:\n      tags:\n        - PrivateLinkResources\n      operationId: microsoftAzurePrivatelinkresourcesget\n      x-ms-examples:\n\
  \        RelayPrivateLinkResourcesList:\n          $ref: ./examples/PrivateEndpointConnections/ListPrivateLinkResources.json\n      description: Gets the private link resources supported for the Relay namespace\n      parameters:\n        - $ref: >-\n            ../../common/v1/definitions.json#/parameters/ResourceGroupNameParameter\n        - $ref: ../../common/v1/definitions.json#/parameters/NamespaceNameParameter\n        - $ref: ../../common/v1/definitions.json#/parameters/ApiVersionParameter\n        - $ref: ../../common/v1/definitions.json#/parameters/SubscriptionIdParameter\n      responses:\n        '200':\n          description: Successfully retrieved private link resources.\n          schema:\n            $ref: '#/definitions/PrivateLinkResourceListResult'\n        default:\n          description: Relay error response describing why the operation failed.\n          schema:\n            $ref: ../../common/v1/definitions.json#/definitions/ErrorResponse\n      x-ms-pageable:\n \
  \       nextLinkName: nextLink\n      summary: >-\n        Microsoft Azure Get Subscriptions Subscriptionid Resourcegroups Resourcegroupname Providers Microsoft Relay Namespaces Namespacename Privatelinkresources\ndefinitions:\n  PrivateLinkResourceListResult:\n    properties:\n      value:\n        type: array\n        description: Array of private link resources\n        items:\n          $ref: '#/definitions/PrivateLinkResource'\n    description: A list of private link resources\n  PrivateLinkResource:\n    properties:\n      properties:\n        $ref: '#/definitions/PrivateLinkResourceProperties'\n        description: Resource properties.\n        x-ms-client-flatten: true\n    allOf:\n      - $ref: ../../common/v1/definitions.json#/definitions/Resource\n    description: A private link resource\n  PrivateLinkResourceProperties:\n    properties:\n      groupId:\n        description: Group identifier of private link resource.\n        type: string\n        readOnly: true\n      requiredMembers:\n\
  \        description: Required member names of private link resource.\n        type: array\n        items:\n          type: string\n        readOnly: true\n      requiredZoneNames:\n        type: array\n        items:\n          type: string\n        description: Required DNS zone names of the the private link resource.\n    description: Properties of a private link resource.\nparameters: {}\ntags:\n  - name: PrivateLinkResources\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/relay-api-openapi-original.yml
tags: []
---
