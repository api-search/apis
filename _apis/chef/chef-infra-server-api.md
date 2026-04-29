---
aid: chef:chef-infra-server-api
baseURL: https://chef.example.com/organizations/example
description: REST API for managing nodes, cookbooks, roles, environments, data bags, clients, and users on the Chef Infra Server. Authentication uses Chef signed-header authentication with an RSA client key.
humanURL: https://docs.chef.io/server/api_chef_server/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Chef Infra Server API
properties:
- type: Documentation
  url: https://docs.chef.io/server/api_chef_server/
- type: Authentication
  url: https://docs.chef.io/server/server_security/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chef/refs/heads/main/openapi/chef-infra-server-api-openapi.yml
provider_name: Chef
provider_slug: chef
slug: chef-infra-server-api
source_filename: chef-infra-server-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Chef Infra Server API\n  description: >-\n    REST API for the Chef Infra Server. Manages nodes, cookbooks, roles,\n    environments, data bags, clients, and users that drive Chef's\n    infrastructure automation. Authentication uses RSA-signed request\n    headers per the Chef Infra Server signed-header authentication scheme.\n  version: '1.0'\n  contact:\n    name: Chef Software\n    url: https://www.chef.io/support\nexternalDocs:\n  description: Chef Infra Server API Documentation\n  url: https://docs.chef.io/server/api_chef_server/\nservers:\n  - url: https://{server}/organizations/{org}\n    description: Chef Infra Server (per-organization)\n    variables:\n      server:\n        default: chef.example.com\n      org:\n        default: example\ntags:\n  - name: Nodes\n  - name: Cookbooks\n  - name: Roles\n  - name: Environments\n  - name: Data Bags\n  - name: Clients\n  - name: Users\nsecurity:\n  - chefSignedAuth: []\npaths:\n  /nodes:\n\
  \    get:\n      operationId: listNodes\n      summary: List nodes\n      tags: [Nodes]\n      responses:\n        '200':\n          description: Node list\n    post:\n      operationId: createNode\n      summary: Create a node\n      tags: [Nodes]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '201':\n          description: Node created\n  /nodes/{nodeName}:\n    get:\n      operationId: getNode\n      summary: Get a node\n      tags: [Nodes]\n      parameters:\n        - name: nodeName\n          in: path\n          required: true\n          schema: { type: string }\n      responses:\n        '200':\n          description: Node\n    put:\n      operationId: updateNode\n      summary: Update a node\n      tags: [Nodes]\n      parameters:\n        - name: nodeName\n          in: path\n          required: true\n          schema: { type: string }\n      requestBody:\n \
  \       required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '200':\n          description: Node updated\n    delete:\n      operationId: deleteNode\n      summary: Delete a node\n      tags: [Nodes]\n      parameters:\n        - name: nodeName\n          in: path\n          required: true\n          schema: { type: string }\n      responses:\n        '200':\n          description: Node deleted\n  /cookbooks:\n    get:\n      operationId: listCookbooks\n      summary: List cookbooks\n      tags: [Cookbooks]\n      responses:\n        '200':\n          description: Cookbook list\n  /cookbooks/{cookbookName}:\n    get:\n      operationId: getCookbook\n      summary: Get cookbook versions\n      tags: [Cookbooks]\n      parameters:\n        - name: cookbookName\n          in: path\n          required: true\n          schema: { type: string }\n      responses:\n        '200':\n          description: Cookbook\
  \ versions\n  /roles:\n    get:\n      operationId: listRoles\n      summary: List roles\n      tags: [Roles]\n      responses:\n        '200':\n          description: Role list\n    post:\n      operationId: createRole\n      summary: Create a role\n      tags: [Roles]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '201':\n          description: Role created\n  /roles/{roleName}:\n    get:\n      operationId: getRole\n      summary: Get a role\n      tags: [Roles]\n      parameters:\n        - name: roleName\n          in: path\n          required: true\n          schema: { type: string }\n      responses:\n        '200':\n          description: Role\n  /environments:\n    get:\n      operationId: listEnvironments\n      summary: List environments\n      tags: [Environments]\n      responses:\n        '200':\n          description: Environment list\n  /data:\n    get:\n\
  \      operationId: listDataBags\n      summary: List data bags\n      tags: [Data Bags]\n      responses:\n        '200':\n          description: Data bag list\n  /clients:\n    get:\n      operationId: listClients\n      summary: List API clients\n      tags: [Clients]\n      responses:\n        '200':\n          description: Client list\n  /users:\n    get:\n      operationId: listUsers\n      summary: List users\n      tags: [Users]\n      responses:\n        '200':\n          description: User list\ncomponents:\n  securitySchemes:\n    chefSignedAuth:\n      type: apiKey\n      in: header\n      name: X-Ops-Authorization\n      description: Chef signed-header authentication using an RSA key associated with a client.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chef/refs/heads/main/openapi/chef-infra-server-api-openapi.yml
tags:
- Configuration Management
- Infrastructure
---
