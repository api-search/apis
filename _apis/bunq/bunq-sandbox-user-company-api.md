---
aid: bunq:bunq-sandbox-user-company-api
baseURL: ''
description: The Bunq Sandbox User Company API is a tool that allows developers to easily create and manage sample company accounts within the Bunq financial platform for testing purposes. This API provides developers with the ability to simulate various company profiles, including employees, bank accounts, transactions, and more, in order to test and debug their applications in a controlled environment.
humanURL: ''
image: ''
layout: api
name: Bunq Sandbox User Company API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-sandbox-user-company--openapi-original.yml
- type: Documentation
  url: https://beta.doc.bunq.com/basics/sandbox
provider_name: Bunq
provider_slug: bunq
slug: bunq-sandbox-user-company-api
source_filename: bunq-sandbox-user-company--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq sandbox-user-company/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths: {}\ntags: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-sandbox-user-company--openapi-original.yml
tags: []
---
