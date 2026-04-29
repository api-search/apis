---
aid: peoplesoft:cloud-manager-api
baseURL: https://{hostname}:{port}/psft/api/cloudmgr/v1
description: REST APIs for automated environment provisioning and deployment on Oracle Cloud Infrastructure including PeopleTools upgrades, update management, and self-service provisioning templates.
humanURL: https://docs.oracle.com/cd/E52319_01/infoportal/cloudmgr.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Cloud Manager API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E52319_01/infoportal/cloudmgr.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/cloud-manager.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: cloud-manager-api
source_filename: cloud-manager.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Cloud Manager API\n  description: REST APIs for automated environment provisioning and deployment on Oracle Cloud Infrastructure including PeopleTools upgrades, update management, and self-service provisioning \n    templates.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/cloudmgr/v1\n  description: PeopleSoft Cloud Manager Instance\n  variables:\n    hostname:\n      description: Cloud Manager server hostname\n      default: localhost\n    port:\n      description: Cloud Manager server port\n      default: '8000'\nexternalDocs:\n  description: PeopleSoft Cloud Manager Documentation\n  url: https://docs.oracle.com/cd/E52319_01/infoportal/cloudmgr.html\ntags:\n- name: Environments\n  description: Environment provisioning and management\n\
  - name: Templates\n  description: Provisioning template operations\npaths:\n  /environments:\n    get:\n      summary: PeopleSoft List Environments\n      description: Retrieve a list of provisioned PeopleSoft environments.\n      operationId: listEnvironments\n      tags:\n      - Environments\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with environment list\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  environments:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        environmentId:\n                          type: string\n                        name:\n                          type: string\n                        status:\n                          type: string\n                        toolsVersion:\n \
  \                         type: string\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    post:\n      summary: PeopleSoft Provision Environment\n      description: Provision a new PeopleSoft environment on OCI from a template.\n      operationId: provisionEnvironment\n      tags:\n      - Environments\n      security:\n      - basicAuth: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                templateId:\n                  type: string\n                environmentName:\n                  type: string\n                configuration:\n                  type: object\n      responses:\n        '202':\n          description: Provisioning initiated\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n\
  \                  environmentId:\n                    type: string\n                  status:\n                    type: string\n        '400':\n          description: Bad request\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /templates:\n    get:\n      summary: PeopleSoft List Templates\n      description: Retrieve available provisioning templates.\n      operationId: listTemplates\n      tags:\n      - Templates\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with template list\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  templates:\n                    type: array\n                    items:\n                      type: object\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay:\
  \ 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/cloud-manager.yml
tags:
- Cloud
- Deployment
- OCI
- Provisioning
---
