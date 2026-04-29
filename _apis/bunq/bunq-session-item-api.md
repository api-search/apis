---
aid: bunq:bunq-session-item-api
baseURL: ''
description: The Bunq Session Item API is a tool that allows developers to securely manage and access user-specific data within the Bunq banking platform. This API enables users to create and modify session items, which are essentially temporary containers for storing extra information related to a user's session. By utilizing this API, developers can enhance the functionality of their applications by storing and retrieving additional data that is relevant to a particular user session.
humanURL: ''
image: ''
layout: api
name: Bunq Session Item API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-session-itemid--openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-session-item-api
source_filename: bunq-session-itemid--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq session/{itemId}/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths: {}\ntags: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-session-itemid--openapi-original.yml
tags: []
---
