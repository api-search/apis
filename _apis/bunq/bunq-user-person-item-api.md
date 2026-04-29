---
aid: bunq:bunq-user-person-item-api
baseURL: ''
description: The Bunq User Person Item API is a tool designed to allow users to interact with and manage their personal financial data within the Bunq platform. This API enables users to access and retrieve information about their accounts, transactions, and other financial activities, as well as perform various actions such as making payments, transferring funds, and managing standing orders.
humanURL: ''
image: ''
layout: api
name: Bunq User Person Item API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-person-itemid--openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-user-person-item-api
source_filename: bunq-user-person-itemid--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user-person/{itemId}/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths: {}\ntags: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-person-itemid--openapi-original.yml
tags: []
---
