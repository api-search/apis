---
aid: bigcommerce:bigcommerce-storefront-customers
baseURL: https://api.example.com
description: BigCommerce Storefront Customers is a platform that provides a user-friendly interface for online merchants to create and manage their e-commerce websites. With a variety of customizable templates, integrations, and marketing tools, BigCommerce Storefront Customers allows businesses to easily showcase their products, process transactions, and drive sales.
humanURL: https://developer.bigcommerce.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Big Commerce Storefront Customers
properties:
- type: Documentation
  url: https://developer.bigcommerce.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bigcommerce/refs/heads/main/openapi/storefront-customers-openapi-original.yml
- type: API Reference
  url: https://developer.bigcommerce.com/docs/rest-storefront/customers
provider_name: BigCommerce
provider_slug: bigcommerce
slug: bigcommerce-storefront-customers
source_filename: storefront-customers-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.1\ninfo:\n  version: Storefront\n  title: BigCommerce Storefront Customers\n  description: >-\n    Manage customers and data via front-end JavaScript on BigCommerce\n    Stencil-powered storefronts.\n\n\n    For info about API accounts, see our [Guide to API\n    Accounts](/docs/start/authentication/api-accounts).\n        \n    For info about authenticating BigCommerce APIs, see [Authentication and\n    Example\n    Requests](/docs/start/authentication#same-origin-cors-authentication).\nservers:\n  - url: https://{store_domain}/api/storefront\n    variables:\n      store_domain:\n        default: your_store.example.com\n        description: >-\n          The [URL\n          authority](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL#authority)\n          of the storefront.\ntags:\n  - name: Customers\npaths:\n  /customers:\n    post:\n      tags:\n        - Customers\n      description: >-\n        Create a *Customer*.\n\
  \n\n        > #### Note\n\n        > * Substitute your storefront domain for `yourstore.example.com`. \n\n        > * The Send a Test Request feature is not currently supported for this\n        endpoint.\n      responses:\n        '204':\n          description: Customer successfully created.\n        '400':\n          description: Could not create customer.\n        '409':\n          description: >-\n            Thereʼs already an account for the provided email. Please enter a\n            different email address or sign in.\n        '422':\n          description: Missing Required Fields.\n        '429':\n          description: Spam Protection Failed.\n      summary: BigCommerce Create a Customer\n      operationId: createCustomer\n      requestBody:\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/CustomerCreateData'\n            examples:\n              application/json:\n                value:\n                  firstName:\
  \ Jane\n                  lastName: Doe\n                  email: janedoe@example.com\n                  password: string\n                  acceptsMarketingEmails: true\n                  customFields:\n                    - fieldId: '25'\n                      fieldValue: Leave in backyard\n        description: >-\n          Data sent the the customer endpoint when creating a customer during\n          checkout.\ncomponents:\n  schemas:\n    CustomerCreateData:\n      title: CustomerCreateData\n      type: object\n      properties:\n        firstName:\n          type: string\n          description: First name of customer.\n        lastName:\n          type: string\n          description: Last name of customer.\n        email:\n          type: string\n          description: Email of customer.\n        password:\n          type: string\n          description: Password of customer.\n        acceptsMarketingEmails:\n          type: boolean\n          description: >-\n            Indicates\
  \ whether customer provided consent to receive marketing\n            emails.\n        customFields:\n          type: array\n          items:\n            $ref: '#/components/schemas/CustomFields'\n      x-internal: false\n    CustomFields:\n      title: CustomFields\n      type: object\n      x-internal: false\n      properties:\n        fieldId:\n          type: string\n        fieldValue:\n          oneOf:\n            - type: string\n            - type: number\n            - type: array\n              items:\n                type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bigcommerce/refs/heads/main/openapi/storefront-customers-openapi-original.yml
tags:
- Customers
- Storefronts
---
