---
aid: bunq:bunq-session-server-api
baseURL: ''
description: The Bunq Session Server API is a powerful tool that allows developers to easily manage user sessions within the Bunq platform. By utilizing this API, developers can create and manage user sessions, including logins, access tokens, and session cookies. This makes it easier for users to securely access their accounts and perform transactions within the Bunq app. The Session Server API also provides tools for managing session expiration, refreshing access tokens, and monitoring user activity.
humanURL: ''
image: ''
layout: api
name: Bunq Session Server API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-session-server--openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-session-server-api
source_filename: bunq-session-server--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq session-server/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths: {}\ntags: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-session-server--openapi-original.yml
tags: []
---
