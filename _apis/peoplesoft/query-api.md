---
aid: peoplesoft:query-api
baseURL: https://{hostname}:{port}/psft/api/query/v1
description: Execute PeopleSoft Query definitions and retrieve results via REST including the Query Access Service operations for listing, executing, and managing queries.
humanURL: https://docs.oracle.com/en/applications/peoplesoft/query-api/
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Query API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E92519_02/pt856pbr3/eng/pt/trws/concept_QueryAccessServiceOperations-1f7e36.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/query.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: query-api
source_filename: query.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Query API\n  description: Execute PeopleSoft Query definitions and retrieve results via REST including the Query Access Service operations for listing, executing, and managing queries.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/query/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: Query Access Service Operations\n  url: https://docs.oracle.com/cd/E92519_02/pt856pbr3/eng/pt/trws/concept_QueryAccessServiceOperations-1f7e36.html\ntags:\n- name: Queries\n  description: Query execution and management operations\npaths:\n  /queries:\n\
  \    get:\n      summary: PeopleSoft List Queries\n      description: Retrieve a list of available PeopleSoft Query definitions.\n      operationId: listQueries\n      tags:\n      - Queries\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with query list\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  queries:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        queryName:\n                          type: string\n                        description:\n                          type: string\n                        folder:\n                          type: string\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /queries/{queryName}:\n\
  \    get:\n      summary: PeopleSoft Execute Query\n      description: Execute a PeopleSoft Query by name and retrieve results.\n      operationId: executeQuery\n      tags:\n      - Queries\n      security:\n      - basicAuth: []\n      parameters:\n      - name: queryName\n        in: path\n        required: true\n        description: The PeopleSoft Query name\n        schema:\n          type: string\n        example: Example Record\n      - name: isConnectedQuery\n        in: query\n        description: Whether this is a Connected Query\n        schema:\n          type: boolean\n          default: false\n        example: true\n      - name: maxRows\n        in: query\n        description: Maximum number of rows to return\n        schema:\n          type: integer\n        example: 42\n      - name: offset\n        in: query\n        description: Row offset for pagination\n        schema:\n          type: integer\n        example: 42\n      responses:\n        '200':\n          description:\
  \ Query results\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  rows:\n                    type: array\n                    items:\n                      type: object\n                  totalRows:\n                    type: integer\n        '401':\n          description: Unauthorized\n        '404':\n          description: Query not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/query.yml
tags:
- Data Access
- QAS
- Query
- Reporting
---
