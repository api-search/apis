---
aid: bunq:bunq-server-error-api
baseURL: ''
description: Bunq Server Error API is a tool designed to help developers troubleshoot issues and debug server errors within the Bunq banking platform. This API provides detailed information about server errors, including error codes, error messages, and possible solutions. By integrating this API into their applications, developers can quickly identify and resolve server errors to ensure a smooth and seamless user experience.
humanURL: ''
image: ''
layout: api
name: Bunq Server Error API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-server-error--openapi-original.yml
- type: Documentation
  url: https://beta.doc.bunq.com/basics/errors
provider_name: Bunq
provider_slug: bunq
slug: bunq-server-error-api
source_filename: bunq-server-error--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq server-error/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths: {}\ntags: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-server-error--openapi-original.yml
tags: []
---
