---
aid: peoplesoft:component-interface-api
baseURL: https://{hostname}:{port}/psft/api/componentinterface/v1
description: Programmatic access to PeopleSoft components for data manipulation providing CRUD operations on component data via REST.
humanURL: https://docs.oracle.com/en/applications/peoplesoft/component-interfaces/
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Component Interface API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E92519_02/pt856pbr3/eng/pt/tcpi/index.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/component-interface.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: component-interface-api
source_filename: component-interface.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Component Interface API\n  description: Programmatic access to PeopleSoft components for data manipulation providing CRUD operations on component data via REST.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/componentinterface/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: Component Interface Documentation\n  url: https://docs.oracle.com/cd/E92519_02/pt856pbr3/eng/pt/tcpi/index.html\ntags:\n- name: Component Interfaces\n  description: Component interface operations\npaths:\n  /{componentInterface}:\n    get:\n      summary: PeopleSoft\
  \ Get Component Data\n      description: Retrieve data from a PeopleSoft component interface.\n      operationId: getComponentData\n      tags:\n      - Component Interfaces\n      security:\n      - basicAuth: []\n      parameters:\n      - name: componentInterface\n        in: path\n        required: true\n        description: The component interface name\n        schema:\n          type: string\n        example: example_value\n      responses:\n        '200':\n          description: Successful response with component data\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized\n        '404':\n          description: Component interface not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    post:\n      summary: PeopleSoft Create Component Data\n      description: Create a new record via a PeopleSoft component interface.\n      operationId: createComponentData\n\
  \      tags:\n      - Component Interfaces\n      security:\n      - basicAuth: []\n      parameters:\n      - name: componentInterface\n        in: path\n        required: true\n        description: The component interface name\n        schema:\n          type: string\n        example: example_value\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '201':\n          description: Record created\n          content:\n            application/json:\n              schema:\n                type: object\n        '400':\n          description: Bad request\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    put:\n      summary: PeopleSoft Update Component Data\n      description: Update an existing record via a PeopleSoft component interface.\n      operationId: updateComponentData\n      tags:\n \
  \     - Component Interfaces\n      security:\n      - basicAuth: []\n      parameters:\n      - name: componentInterface\n        in: path\n        required: true\n        description: The component interface name\n        schema:\n          type: string\n        example: example_value\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '200':\n          description: Record updated\n          content:\n            application/json:\n              schema:\n                type: object\n        '400':\n          description: Bad request\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/component-interface.yml
tags:
- Component Interface
- CRUD Operations
- Data Access
---
