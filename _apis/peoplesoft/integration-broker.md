---
aid: peoplesoft:integration-broker
baseURL: https://{hostname}:{port}/PSIGW/RESTListeningConnector
description: Message-based integration framework for synchronous and asynchronous communication supporting both SOAP and REST protocols.
humanURL: https://docs.oracle.com/cd/E92519_02/pt856pbr3/eng/pt/tibr/index.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Integration Broker
properties:
- type: Documentation
  url: https://docs.oracle.com/en/applications/peoplesoft/integration-broker/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/integration-broker.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: integration-broker
source_filename: integration-broker.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Integration Broker\n  description: Message-based integration framework for synchronous and asynchronous communication supporting both SOAP and REST protocols.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/PSIGW/RESTListeningConnector\n  description: PeopleSoft Integration Gateway\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: Integration Broker Documentation\n  url: https://docs.oracle.com/en/applications/peoplesoft/integration-broker/\ntags:\n- name: Service Operations\n  description: Integration Broker service operations\npaths:\n  /{serviceOperation}.v1:\n    get:\n     \
  \ summary: PeopleSoft Invoke Service Operation (GET)\n      description: Invoke a synchronous Integration Broker REST service operation using GET.\n      operationId: getServiceOperation\n      tags:\n      - Service Operations\n      security:\n      - basicAuth: []\n      parameters:\n      - name: serviceOperation\n        in: path\n        required: true\n        description: The service operation name\n        schema:\n          type: string\n        example: example_value\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized\n        '404':\n          description: Service operation not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    post:\n      summary: PeopleSoft Invoke Service Operation (POST)\n      description: Invoke a synchronous or asynchronous Integration\
  \ Broker REST service operation using POST.\n      operationId: postServiceOperation\n      tags:\n      - Service Operations\n      security:\n      - basicAuth: []\n      parameters:\n      - name: serviceOperation\n        in: path\n        required: true\n        description: The service operation name\n        schema:\n          type: string\n        example: example_value\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                type: object\n        '400':\n          description: Bad request\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/integration-broker.yml
tags:
- Integration
- Messaging
- REST
- SOAP
---
