---
aid: cargodocs:partner-api
baseURL: https://api.essdocs.com
description: The CargoDocs Partner API enables platform providers and trade finance/trade management platforms to embed CargoDocs DocEx functionality, including original electronic bills of lading (eBoL) and warehouse warrants (eWW). The API exposes Partner Exchange endpoints to retrieve customer, counterparty, document, and transaction data using conditions and filters, and Action endpoints to perform operations over transactions such as signing, transferring, and surrendering documents.
humanURL: https://cargodocs-partner.readme.io/
image: ''
layout: api
name: CargoDocs Partner API
properties:
- type: Documentation
  url: https://cargodocs-partner.readme.io/
- type: GettingStarted
  url: https://cargodocs-partner.readme.io/docs/api-environments
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/openapi/cargodocs-partner-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/json-schema/cargodocs-customer.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/json-schema/cargodocs-counterparty.json
provider_name: CargoDocs
provider_slug: cargodocs
slug: partner-api
source_filename: cargodocs-partner-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CargoDocs Partner API\n  description: >-\n    The CargoDocs Partner API enables partners and platform providers to embed\n    CargoDocs DocEx functionality into their trade or trade finance platforms,\n    handling original electronic bills of lading (eBoL) and warehouse warrants\n    (eWW). The Partner Exchange API retrieves customer and partner data to\n    perform specific actions, with endpoints to retrieve data based on\n    conditions and filters and Action endpoints to action over transactions.\n  version: 3.0.0\n  contact:\n    name: ICE Digital Trade (essDOCS)\n    url: https://www.essdocs.com\n  license:\n    name: Proprietary\n    url: https://www.essdocs.com\nservers:\n  - url: https://api-test.cargodocs.com/v3\n    description: Sandbox / Test Environment\n  - url: https://api.uat.cargodocs.com/v3\n    description: UAT Environment\n  - url: https://api.cargodocs.com/v3\n    description: Production Environment\nsecurity:\n  - bearerAuth:\
  \ []\npaths:\n  /exchange/customers:\n    get:\n      operationId: getPartnerCustomerIds\n      summary: CargoDocs Get Partner Customer Ids\n      description: >-\n        Allows a Partner to collect the Customer IDs which they have permission\n        to access in CargoDocs Exchange.\n      tags:\n        - Exchange\n      responses:\n        '200':\n          description: Successful response with list of customer IDs\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/Customer'\n        '401':\n          description: Unauthorized\n        '403':\n          description: Forbidden\n  /exchange/employees:\n    get:\n      operationId: getPartnerCustomerEmployeeIds\n      summary: CargoDocs Get Partner Customer Employee Ids\n      description: >-\n        Allows the Partner to collect the Employee IDs for parties to action a\n        set of electronic documents and for\
  \ auditing purposes.\n      tags:\n        - Exchange\n      responses:\n        '200':\n          description: Successful response with list of employee IDs\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/Employee'\n        '401':\n          description: Unauthorized\n        '403':\n          description: Forbidden\n  /common/counterparties:\n    get:\n      operationId: getCounterparties\n      summary: CargoDocs Get Counterparties\n      description: >-\n        Allows a Partner to retrieve all available counterparties.\n      tags:\n        - Common\n      responses:\n        '200':\n          description: Successful response with list of counterparties\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/Counterparty'\n        '401':\n \
  \         description: Unauthorized\n        '403':\n          description: Forbidden\n  /exchange/documents/{documentId}/pdf:\n    get:\n      operationId: getSinglePdf\n      summary: CargoDocs Get Single PDF\n      description: >-\n        Allows a customer to download a copy of documents within a set. If the\n        customer holds the original eBoL, the partner can download a version of\n        the BoL watermarked Original in CargoDocs.\n      tags:\n        - Documents\n      parameters:\n        - name: documentId\n          in: path\n          required: true\n          description: The unique identifier for the document\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Successful response with PDF document\n          content:\n            application/pdf:\n              schema:\n                type: string\n                format: binary\n        '401':\n          description: Unauthorized\n        '403':\n          description:\
  \ Forbidden\n        '404':\n          description: Document not found\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n  schemas:\n    Customer:\n      type: object\n      properties:\n        customerId:\n          type: string\n          description: The unique identifier for the customer\n        customerName:\n          type: string\n          description: The name of the customer\n    Employee:\n      type: object\n      properties:\n        employeeId:\n          type: string\n          description: The unique identifier for the employee\n        employeeName:\n          type: string\n          description: The name of the employee\n        customerId:\n          type: string\n          description: The customer ID associated with this employee\n    Counterparty:\n      type: object\n      properties:\n        counterpartyId:\n          type: string\n          description: The unique identifier for the counterparty\n\
  \        counterpartyName:\n          type: string\n          description: The name of the counterparty\ntags:\n  - name: Common\n    description: Common API endpoints shared across partner operations\n  - name: Documents\n    description: Document retrieval and management endpoints\n  - name: Exchange\n    description: Partner Exchange API endpoints for customer and employee data\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/openapi/cargodocs-partner-openapi.yml
tags:
- Bills of Lading
- Shipping
- Trade
---
