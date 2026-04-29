---
aid: microsoft-azure:privateaccesses-types
baseURL: ''
description: Microsoft Azure Private Accesses Types provides users with secure and private access to Azure resources. This feature allows organizations to control access to their resources, ensuring that only authorized users can connect to them. There are several types of private access methods available, including Azure Private Link, Virtual Network Service Endpoints, and Azure ExpressRoute.
humanURL: https://learn.microsoft.com/en-us/azure/private-link/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Private Accesses Types
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/privateaccesses-types-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/private-link/
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/private-link/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: privateaccesses-types
source_filename: privateaccesses-types-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure PrivateAccesses types\n  version: 2023-10-27-preview\npaths: {}\ndefinitions:\n  PrivateAccess:\n    type: object\n    description: PrivateAccesses tracked resource.\n    allOf:\n      - $ref: >-\n          ../../../../../../common-types/resource-management/v5/types.json#/definitions/TrackedResource\n    properties:\n      properties:\n        $ref: '#/definitions/PrivateAccessProperties'\n        x-ms-client-flatten: true\n        description: The resource-specific properties for this resource.\n    required:\n      - properties\n  PrivateAccessProperties:\n    type: object\n    description: The properties of a private access resource\n    properties:\n      privateEndpointConnections:\n        type: array\n        readOnly: true\n        items:\n          $ref: >-\n            ../../../../../../common-types/resource-management/v5/privatelinks.json#/definitions/PrivateEndpointConnection\n        description: >-\n          A readonly\
  \ collection of private endpoint connection. Currently only\n          one endpoint connection is supported.\n  PrivateAccessListResult:\n    type: object\n    description: >-\n      Model that represents a list of private access resources and a link for\n      pagination.\n    properties:\n      value:\n        type: array\n        items:\n          $ref: '#/definitions/PrivateAccess'\n        description: List of private access resources.\n        readOnly: true\n      nextLink:\n        $ref: ./common.json#/definitions/urlNullable\n        description: URL to retrieve the next page of private access resources.\n        readOnly: true\n  PrivateLinkResourceListResult:\n    properties:\n      value:\n        type: array\n        description: Array of private link resources\n        items:\n          $ref: >-\n            ../../../../../../common-types/resource-management/v5/privatelinks.json#/definitions/PrivateLinkResource\n      nextLink:\n        $ref: ./common.json#/definitions/urlNullable\n\
  \        description: >-\n          The uri to fetch the next page of snapshots. Call ListNext() with this\n          to fetch the next page of snapshots.\n        readOnly: true\n    description: A list of private link resources\n  PrivateEndpointConnectionListResult:\n    properties:\n      value:\n        type: array\n        description: Array of private endpoint connections\n        items:\n          $ref: >-\n            ../../../../../../common-types/resource-management/v5/privatelinks.json#/definitions/PrivateEndpointConnection\n      nextLink:\n        $ref: ./common.json#/definitions/urlNullable\n        description: >-\n          The uri to fetch the next page of snapshots. Call ListNext() with this\n          to fetch the next page of snapshots.\n        readOnly: true\n    description: A list of private link resources\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/privateaccesses-types-openapi-original.yml
tags: []
---
