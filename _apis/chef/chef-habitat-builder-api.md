---
aid: chef:chef-habitat-builder-api
baseURL: https://bldr.habitat.sh/v1
description: REST API for Chef Habitat Builder, the package management service for Habitat application packages. Manages origins, packages, channels, and deployment events.
humanURL: https://docs.habitat.sh/docs/using-builder/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Chef Habitat Builder API
properties:
- type: Documentation
  url: https://docs.habitat.sh/docs/using-builder/
- type: Authentication
  url: https://docs.habitat.sh/docs/using-builder/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chef/refs/heads/main/openapi/chef-habitat-builder-api-openapi.yml
provider_name: Chef
provider_slug: chef
slug: chef-habitat-builder-api
source_filename: chef-habitat-builder-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Chef Habitat Builder API\n  description: >-\n    REST API for Chef Habitat Builder, the package management service for\n    Habitat application packages. Manages origins, packages, channels,\n    and deployment events.\n  version: '1.0'\n  contact:\n    name: Chef Software\n    url: https://www.chef.io/support\nexternalDocs:\n  description: Habitat Builder Documentation\n  url: https://docs.habitat.sh/docs/using-builder/\nservers:\n  - url: https://bldr.habitat.sh/v1\n    description: Public Habitat Builder\ntags:\n  - name: Origins\n  - name: Packages\n  - name: Channels\nsecurity:\n  - habitatToken: []\npaths:\n  /depot/origins/{origin}/pkgs:\n    get:\n      operationId: listOriginPackages\n      summary: List packages for an origin\n      tags: [Packages]\n      parameters:\n        - name: origin\n          in: path\n          required: true\n          schema: { type: string }\n      responses:\n        '200':\n          description: Packages\n\
  \  /depot/pkgs/{origin}/{pkg}:\n    get:\n      operationId: getPackage\n      summary: Get a package\n      tags: [Packages]\n      parameters:\n        - name: origin\n          in: path\n          required: true\n          schema: { type: string }\n        - name: pkg\n          in: path\n          required: true\n          schema: { type: string }\n      responses:\n        '200':\n          description: Package versions\n  /depot/channels/{origin}:\n    get:\n      operationId: listChannels\n      summary: List channels for an origin\n      tags: [Channels]\n      parameters:\n        - name: origin\n          in: path\n          required: true\n          schema: { type: string }\n      responses:\n        '200':\n          description: Channels\ncomponents:\n  securitySchemes:\n    habitatToken:\n      type: http\n      scheme: bearer\n      bearerFormat: HabitatBuilderToken\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chef/refs/heads/main/openapi/chef-habitat-builder-api-openapi.yml
tags:
- Application Packaging
- Deployment
- Habitat
---
