---
aid: consumer-financial-protection-bureau:hmda-institutions
baseURL: https://ffiec.cfpb.gov/v2
description: Returns the financial institutions registered to file HMDA data with the CFPB, keyed by year and Legal Entity Identifier (LEI). Used by filers and researchers to confirm filer identifiers, registration status, and contact info.
humanURL: https://ffiec.cfpb.gov/documentation/api/institutions-api/
image: ''
layout: api
name: HMDA Institutions API
properties:
- type: Documentation
  url: https://ffiec.cfpb.gov/documentation/api/institutions-api/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/consumer-financial-protection-bureau/refs/heads/main/openapi/cfpb-hmda-institutions-openapi.yml
provider_name: Consumer Financial Protection Bureau
provider_slug: consumer-financial-protection-bureau
slug: hmda-institutions
source_filename: cfpb-hmda-institutions-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CFPB HMDA Institutions API\n  description: >-\n    The HMDA Platform Institutions API returns the financial institutions\n    registered to file Home Mortgage Disclosure Act data with the CFPB,\n    keyed by year and LEI. It is used by filers and researchers to\n    confirm filer identifiers, registration status, and contact info.\n  version: '2'\n  contact:\n    name: HMDA Operations\n    url: https://ffiec.cfpb.gov/\nservers:\n  - url: https://ffiec.cfpb.gov/v2\n    description: Production HMDA Platform\npaths:\n  /public/filers/{year}:\n    get:\n      operationId: listInstitutionsByYear\n      summary: List all institutions that filed HMDA data for a year\n      tags:\n        - Institutions\n      parameters:\n        - name: year\n          in: path\n          required: true\n          schema: { type: integer, minimum: 2018 }\n      responses:\n        '200':\n          description: List of filers\n          content:\n            application/json:\n\
  \              schema:\n                type: object\n                properties:\n                  institutions:\n                    type: array\n                    items:\n                      $ref: '#/components/schemas/Institution'\n  /public/institutions/{year}/{lei}:\n    get:\n      operationId: getInstitution\n      summary: Get a single institution by year and LEI\n      tags:\n        - Institutions\n      parameters:\n        - name: year\n          in: path\n          required: true\n          schema: { type: integer }\n        - name: lei\n          in: path\n          required: true\n          schema: { type: string, minLength: 20, maxLength: 20 }\n      responses:\n        '200':\n          description: Institution detail\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Institution'\n        '404':\n          description: Not found\ncomponents:\n  schemas:\n    Institution:\n      type: object\n  \
  \    properties:\n        lei:\n          type: string\n          minLength: 20\n          maxLength: 20\n        activityYear:\n          type: integer\n        agency:\n          type: integer\n        institutionType:\n          type: string\n        institutionId2017:\n          type: string\n        taxId:\n          type: string\n        rssd:\n          type: integer\n        respondent:\n          type: object\n          properties:\n            name: { type: string }\n            state: { type: string }\n            city: { type: string }\n        parent:\n          type: object\n          properties:\n            idRssd: { type: integer }\n            name: { type: string }\n        assets:\n          type: integer\n        otherLenderCode:\n          type: integer\n        topHolder:\n          type: object\n        hmdaFiler:\n          type: boolean\n        quarterlyFiler:\n          type: boolean\n        quarterlyFilerHasFiledQ1:\n          type: boolean\n        quarterlyFilerHasFiledQ2:\n\
  \          type: boolean\n        quarterlyFilerHasFiledQ3:\n          type: boolean\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consumer-financial-protection-bureau/refs/heads/main/openapi/cfpb-hmda-institutions-openapi.yml
tags:
- HMDA
- Institutions
- Open Data
---
