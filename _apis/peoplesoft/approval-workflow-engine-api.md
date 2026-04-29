---
aid: peoplesoft:approval-workflow-engine-api
baseURL: https://{hostname}:{port}/psft/api/approvals/v1
description: Framework for creating, running, and managing approval processes exposable via REST service operations through Integration Broker or ASF.
humanURL: https://docs.oracle.com/en/applications/peoplesoft/
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Approval Workflow Engine API
properties:
- type: Documentation
  url: https://docs.oracle.com/en/applications/peoplesoft/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/approval-workflow-engine.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: approval-workflow-engine-api
source_filename: approval-workflow-engine.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Approval Workflow Engine API\n  description: Framework for creating, running, and managing approval processes exposable via REST service operations through Integration Broker or ASF.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/approvals/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: PeopleSoft Approval Workflow Engine Documentation\n  url: https://docs.oracle.com/en/applications/peoplesoft/\ntags:\n- name: Approvals\n  description: Approval workflow operations\npaths:\n  /approvals:\n    get:\n      summary: PeopleSoft List Pending\
  \ Approvals\n      description: Retrieve a list of pending approval requests for the current user.\n      operationId: listPendingApprovals\n      tags:\n      - Approvals\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with pending approvals\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  approvals:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        approvalId:\n                          type: string\n                        transactionType:\n                          type: string\n                        status:\n                          type: string\n                        submittedBy:\n                          type: string\n                        submittedDate:\n                          type: string\n\
  \                          format: date-time\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /approvals/{approvalId}:\n    put:\n      summary: PeopleSoft Process Approval\n      description: Approve, deny, or push back an approval request.\n      operationId: processApproval\n      tags:\n      - Approvals\n      security:\n      - basicAuth: []\n      parameters:\n      - name: approvalId\n        in: path\n        required: true\n        description: The approval request identifier\n        schema:\n          type: string\n        example: PS123456\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                action:\n                  type: string\n                  enum:\n                  - approve\n                  - deny\n                  - pushback\n                comments:\n\
  \                  type: string\n      responses:\n        '200':\n          description: Approval processed\n          content:\n            application/json:\n              schema:\n                type: object\n        '400':\n          description: Bad request\n        '401':\n          description: Unauthorized\n        '404':\n          description: Approval not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/approval-workflow-engine.yml
tags:
- Approvals
- AWE
- Workflow
---
