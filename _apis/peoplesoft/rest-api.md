---
aid: peoplesoft:rest-api
baseURL: https://{hostname}:{port}/psft/api/v1
description: RESTful web services for PeopleSoft applications enabling integration with external systems via the PeopleTools platform.
humanURL: https://docs.oracle.com/en/applications/peoplesoft/
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft REST API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E92519_02/pt856pbr3/eng/pt/tpcl/index.html
- type: Authentication
  url: https://docs.oracle.com/cd/F30998_01/pt858pbr2/eng/pt/tsec/concept_UnderstandingOAuth2_0.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/rest-api.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: rest-api
source_filename: rest-api.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft REST API\n  description: RESTful web services for PeopleSoft applications enabling integration with external systems via the PeopleTools platform.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: PeopleSoft REST API Documentation\n  url: https://docs.oracle.com/cd/E92519_02/pt856pbr3/eng/pt/tpcl/index.html\ntags:\n- name: Resources\n  description: PeopleSoft REST resource operations\npaths:\n  /{resource}:\n    get:\n      summary: PeopleSoft Get Resource\n      description: Retrieve\
  \ PeopleSoft resource data via REST.\n      operationId: getResource\n      tags:\n      - Resources\n      security:\n      - basicAuth: []\n      - oauth2: []\n      parameters:\n      - name: resource\n        in: path\n        required: true\n        description: The PeopleSoft resource name\n        schema:\n          type: string\n        example: example_value\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized\n        '404':\n          description: Resource not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    post:\n      summary: PeopleSoft Create Resource\n      description: Create a new PeopleSoft resource via REST.\n      operationId: createResource\n      tags:\n      - Resources\n      security:\n      - basicAuth: []\n      - oauth2: []\n      parameters:\n\
  \      - name: resource\n        in: path\n        required: true\n        description: The PeopleSoft resource name\n        schema:\n          type: string\n        example: example_value\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '201':\n          description: Resource created\n          content:\n            application/json:\n              schema:\n                type: object\n        '400':\n          description: Bad request\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n    oauth2:\n      type: oauth2\n      flows:\n        authorizationCode:\n          authorizationUrl: https://{hostname}:{port}/psft/oauth/authorize\n          tokenUrl: https://{hostname}:{port}/psft/oauth/token\n    \
  \      scopes: {}\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/rest-api.yml
tags:
- Integration
- REST
- Web Services
---
