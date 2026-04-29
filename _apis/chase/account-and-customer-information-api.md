---
aid: chase:account-and-customer-information-api
baseURL: https://api.chase.com/aggregation/fdx
description: FDX-aligned API that allows authorized data recipients to securely retrieve account and customer information for Chase customers. Supports account profiles, balances, transactions, statements, and customer details using OAuth 2.0 with FDX consent flows.
humanURL: https://developer.chase.com/products/aggregation-fdx/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Chase Account and Customer Information API
properties:
- type: Documentation
  url: https://developer.chase.com/products/aggregation-fdx/guides/using-the-account-and-customer-information-api/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-account-and-customer-information-api-openapi.yml
provider_name: Chase
provider_slug: chase
slug: account-and-customer-information-api
source_filename: chase-account-and-customer-information-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Chase Account and Customer Information API\n  description: >-\n    FDX-aligned API for retrieving Chase customer account information,\n    balances, transactions, statements, and tax forms with explicit\n    customer consent.\n  version: '5.2'\n  contact:\n    name: Chase Developer Support\n    url: https://developer.chase.com/support\nexternalDocs:\n  description: Account and Customer Information API Guide\n  url: https://developer.chase.com/products/aggregation-fdx/guides/using-the-account-and-customer-information-api/\nservers:\n  - url: https://api.chase.com/aggregation/fdx\n    description: Chase FDX Aggregation Production\ntags:\n  - name: Accounts\n  - name: Transactions\n  - name: Statements\n  - name: Tax Forms\n  - name: Customers\nsecurity:\n  - oauth2: []\npaths:\n  /accounts:\n    get:\n      operationId: listAccounts\n      summary: List accessible accounts\n      tags: [Accounts]\n      responses:\n        '200':\n          description:\
  \ Accounts list\n  /accounts/{accountId}:\n    get:\n      operationId: getAccount\n      summary: Get account details\n      tags: [Accounts]\n      parameters:\n        - name: accountId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Account details\n  /accounts/{accountId}/transactions:\n    get:\n      operationId: listAccountTransactions\n      summary: List account transactions\n      tags: [Transactions]\n      parameters:\n        - name: accountId\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: startTime\n          in: query\n          schema:\n            type: string\n            format: date-time\n        - name: endTime\n          in: query\n          schema:\n            type: string\n            format: date-time\n      responses:\n        '200':\n          description: Transactions list\n  /accounts/{accountId}/statements:\n\
  \    get:\n      operationId: listStatements\n      summary: List account statements\n      tags: [Statements]\n      parameters:\n        - name: accountId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Statements list\n  /accounts/{accountId}/tax-forms:\n    get:\n      operationId: listTaxForms\n      summary: List tax forms for an account\n      tags: [Tax Forms]\n      parameters:\n        - name: accountId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Tax forms list\n  /customers/current:\n    get:\n      operationId: getCurrentCustomer\n      summary: Get the current authenticated customer\n      tags: [Customers]\n      responses:\n        '200':\n          description: Customer profile\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: oauth2\n      flows:\n        authorizationCode:\n\
  \          authorizationUrl: https://api.chase.com/oauth2/authorize\n          tokenUrl: https://api.chase.com/oauth2/token\n          scopes:\n            accounts.read: Read account data\n            transactions.read: Read transactions\n            statements.read: Read statements\n            tax-forms.read: Read tax forms\n            customers.read: Read customer profile\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-account-and-customer-information-api-openapi.yml
tags:
- Account Aggregation
- FDX
- Open Banking
---
