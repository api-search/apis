---
aid: peoplesoft:pivot-grid-api
baseURL: https://{hostname}:{port}/psft/api/pivotgrid/v1
description: Operational dashboard reporting using PS Query, Composite Query, or component data sources accessible via web services for analytics and visualization.
humanURL: https://docs.oracle.com/cd/F28299_01/pt857pbr3/eng/pt/tpvg/concept_PeopleSoftPivotGridOverview-1e7c6b.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Pivot Grid API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/F28299_01/pt857pbr3/eng/pt/tpvg/concept_PeopleSoftPivotGridOverview-1e7c6b.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/pivot-grid.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: pivot-grid-api
source_filename: pivot-grid.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Pivot Grid API\n  description: Operational dashboard reporting using PS Query, Composite Query, or component data sources accessible via web services for analytics and visualization.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/pivotgrid/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: PeopleSoft Pivot Grid Documentation\n  url: https://docs.oracle.com/cd/F28299_01/pt857pbr3/eng/pt/tpvg/concept_PeopleSoftPivotGridOverview-1e7c6b.html\ntags:\n- name: Pivot Grids\n  description: Pivot grid and dashboard operations\npaths:\n  /grids:\n\
  \    get:\n      summary: PeopleSoft List Pivot Grids\n      description: Retrieve a list of available pivot grid definitions.\n      operationId: listPivotGrids\n      tags:\n      - Pivot Grids\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with pivot grid list\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  grids:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        gridId:\n                          type: string\n                        name:\n                          type: string\n                        dataSource:\n                          type: string\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /grids/{gridId}/data:\n\
  \    get:\n      summary: PeopleSoft Get Pivot Grid Data\n      description: Retrieve data for a specific pivot grid with optional filters.\n      operationId: getPivotGridData\n      tags:\n      - Pivot Grids\n      security:\n      - basicAuth: []\n      parameters:\n      - name: gridId\n        in: path\n        required: true\n        description: The pivot grid identifier\n        schema:\n          type: string\n        example: PS123456\n      - name: filters\n        in: query\n        description: JSON-encoded filter criteria\n        schema:\n          type: string\n        example: example_value\n      responses:\n        '200':\n          description: Pivot grid data\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized\n        '404':\n          description: Pivot grid not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n\
  \  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/pivot-grid.yml
tags:
- Analytics
- Dashboards
- Pivot Grid
- Reporting
---
