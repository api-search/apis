---
aid: microsoft-azure:storage
baseURL: ''
description: Microsoft Azure Storage is a cloud storage solution that allows users to store and manage large amounts of data in a secure and scalable way. It provides a range of storage options, including blob storage for unstructured data, table storage for structured data, file storage for file-based data, and queue storage for message-based communication. Azure Storage also offers features such as data encryption, replication, and access control, ensuring that data is protected and always available.
humanURL: https://learn.microsoft.com/en-us/azure/storage/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Storage
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/storage-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/storage/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: storage
source_filename: storage-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Storage\n  description: Storage Resource Provider API Common Types\n  version: 2020-08-01-preview\npaths: {}\ndefinitions:\n  CorsRules:\n    properties:\n      corsRules:\n        type: array\n        items:\n          description: 'Specifies a CORS rule for the Blob service. '\n          $ref: '#/definitions/CorsRule'\n        description: >-\n          The List of CORS rules. You can include up to five CorsRule elements\n          in the request. \n    description: >-\n      Sets the CORS rules. You can include up to five CorsRule elements in the\n      request. \n  CorsRule:\n    properties:\n      allowedOrigins:\n        type: array\n        items:\n          type: string\n        description: >-\n          Required if CorsRule element is present. A list of origin domains that\n          will be allowed via CORS, or \"*\" to allow all domains\n      allowedMethods:\n        type: array\n        items:\n          type: string\n\
  \          enum:\n            - DELETE\n            - GET\n            - HEAD\n            - MERGE\n            - POST\n            - OPTIONS\n            - PUT\n        description: >-\n          Required if CorsRule element is present. A list of HTTP methods that\n          are allowed to be executed by the origin.\n      maxAgeInSeconds:\n        type: integer\n        description: >-\n          Required if CorsRule element is present. The number of seconds that\n          the client/browser should cache a preflight response.\n      exposedHeaders:\n        type: array\n        items:\n          type: string\n        description: >-\n          Required if CorsRule element is present. A list of response headers to\n          expose to CORS clients.\n      allowedHeaders:\n        type: array\n        items:\n          type: string\n        description: >-\n          Required if CorsRule element is present. A list of headers allowed to\n          be part of the cross-origin request.\n\
  \    required:\n      - allowedOrigins\n      - allowedMethods\n      - maxAgeInSeconds\n      - exposedHeaders\n      - allowedHeaders\n    description: Specifies a CORS rule for the Blob service.\n  DeleteRetentionPolicy:\n    properties:\n      enabled:\n        type: boolean\n        description: Indicates whether DeleteRetentionPolicy is enabled.\n      days:\n        type: integer\n        minimum: 1\n        maximum: 365\n        description: >-\n          Indicates the number of days that the deleted item should be retained.\n          The minimum specified value can be 1 and the maximum value can be 365.\n    description: The service properties for soft delete.\n  Sku:\n    properties:\n      name:\n        $ref: '#/definitions/SkuName'\n      tier:\n        $ref: '#/definitions/Tier'\n    required:\n      - name\n    description: The SKU of the storage account.\n  SkuName:\n    type: string\n    description: >-\n      The SKU name. Required for account creation; optional for\
  \ update. Note\n      that in older versions, SKU name was called accountType.\n    enum:\n      - Standard_LRS\n      - Standard_GRS\n      - Standard_RAGRS\n      - Standard_ZRS\n      - Premium_LRS\n      - Premium_ZRS\n      - Standard_GZRS\n      - Standard_RAGZRS\n    x-ms-enum:\n      name: SkuName\n      modelAsString: true\n  Tier:\n    readOnly: true\n    type: string\n    description: The SKU tier. This is based on the SKU name.\n    enum:\n      - Standard\n      - Premium\n    x-ms-enum:\n      name: SkuTier\n      modelAsString: false\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/storage-openapi-original.yml
tags: []
---
