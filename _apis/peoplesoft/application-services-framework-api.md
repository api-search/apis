---
aid: peoplesoft:application-services-framework-api
baseURL: https://{hostname}:{port}/psft/asf/v1
description: Modern REST API layer introduced in PeopleTools 8.59 that produces fully compliant OpenAPI/Swagger specifications, supports proper HTTP status codes, uniform URLs, and JSON payloads for integration with Oracle Integration Cloud, mobile apps, and microservices.
humanURL: https://docs.oracle.com/cd/E52319_01/infoportal/asf.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Application Services Framework API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E52319_01/infoportal/asf.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/application-services-framework.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: application-services-framework-api
source_filename: application-services-framework.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Application Services Framework API\n  description: Modern REST API layer introduced in PeopleTools 8.59 that produces fully compliant OpenAPI/Swagger specifications, supports proper HTTP status codes, uniform URLs, and JSON payloads for\n    integration with Oracle Integration Cloud, mobile apps, and microservices.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/asf/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: Application Services Framework Documentation\n  url: https://docs.oracle.com/cd/E52319_01/infoportal/asf.html\ntags:\n- name:\
  \ Services\n  description: ASF service operations\npaths:\n  /{serviceName}:\n    get:\n      summary: PeopleSoft Get Service Resource\n      description: Retrieve data from an ASF-defined service with OpenAPI-compliant response.\n      operationId: getServiceResource\n      tags:\n      - Services\n      security:\n      - basicAuth: []\n      - oauth2: []\n      parameters:\n      - name: serviceName\n        in: path\n        required: true\n        description: The ASF service name\n        schema:\n          type: string\n        example: Example Record\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized\n        '404':\n          description: Service not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    post:\n      summary: PeopleSoft Create Service Resource\n \
  \     description: Create a resource via an ASF-defined service.\n      operationId: createServiceResource\n      tags:\n      - Services\n      security:\n      - basicAuth: []\n      - oauth2: []\n      parameters:\n      - name: serviceName\n        in: path\n        required: true\n        description: The ASF service name\n        schema:\n          type: string\n        example: Example Record\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '201':\n          description: Resource created\n          content:\n            application/json:\n              schema:\n                type: object\n        '400':\n          description: Bad request\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n    oauth2:\n\
  \      type: oauth2\n      flows:\n        authorizationCode:\n          authorizationUrl: https://{hostname}:{port}/psft/oauth/authorize\n          tokenUrl: https://{hostname}:{port}/psft/oauth/token\n          scopes: {}\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/application-services-framework.yml
tags:
- Integration
- Modern
- OpenAPI
- REST
---
