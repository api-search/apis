---
aid: peoplesoft:recruiting-and-talent-management-api
baseURL: https://{hostname}:{port}/psft/api/hcm/recruiting/v1
description: REST endpoints for job search services, Candidate Gateway self-service, recruiting solutions, and talent management workflows.
humanURL: https://docs.oracle.com/cd/F85027_01/hcm92pbr47/eng/hcm/ecch/UnderstandingRESTAPIEndpointsForPeopleSoftJobSearchServiceshrsjobs.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Recruiting and Talent Management API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/F85027_01/hcm92pbr47/eng/hcm/ecch/UnderstandingRESTAPIEndpointsForPeopleSoftJobSearchServiceshrsjobs.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/recruiting-talent-management.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: recruiting-and-talent-management-api
source_filename: recruiting-talent-management.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Recruiting and Talent Management API\n  description: REST endpoints for job search services, Candidate Gateway self-service, recruiting solutions, and talent management workflows.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/hcm/recruiting/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: Job Search Services REST API Documentation\n  url: https://docs.oracle.com/cd/F85027_01/hcm92pbr47/eng/hcm/ecch/UnderstandingRESTAPIEndpointsForPeopleSoftJobSearchServiceshrsjobs.html\ntags:\n- name: Jobs\n  description: Job posting and search operations\n\
  - name: Candidates\n  description: Candidate and application operations\npaths:\n  /jobs:\n    get:\n      summary: PeopleSoft Search Jobs\n      description: Search available job postings.\n      operationId: searchJobs\n      tags:\n      - Jobs\n      parameters:\n      - name: keyword\n        in: query\n        description: Keyword search term\n        schema:\n          type: string\n        example: example_value\n      - name: location\n        in: query\n        description: Job location filter\n        schema:\n          type: string\n        example: example_value\n      - name: department\n        in: query\n        description: Department filter\n        schema:\n          type: string\n        example: example_value\n      responses:\n        '200':\n          description: Successful response with job listings\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  jobs:\n    \
  \                type: array\n                    items:\n                      type: object\n                      properties:\n                        jobId:\n                          type: string\n                        title:\n                          type: string\n                        department:\n                          type: string\n                        location:\n                          type: string\n                        postingDate:\n                          type: string\n                          format: date\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /jobs/{jobId}:\n    get:\n      summary: PeopleSoft Get Job Details\n      description: Retrieve details for a specific job posting.\n      operationId: getJobDetails\n      tags:\n      - Jobs\n      parameters:\n      - name: jobId\n        in: path\n        required: true\n        description: The job posting identifier\n        schema:\n          type: string\n        example:\
  \ PS123456\n      responses:\n        '200':\n          description: Job details\n          content:\n            application/json:\n              schema:\n                type: object\n        '404':\n          description: Job not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /candidates/applications:\n    post:\n      summary: PeopleSoft Submit Application\n      description: Submit a candidate application for a job posting.\n      operationId: submitApplication\n      tags:\n      - Candidates\n      security:\n      - basicAuth: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                jobId:\n                  type: string\n                candidateInfo:\n                  type: object\n      responses:\n        '201':\n          description: Application submitted\n        '400':\n          description: Bad request\n\
  \        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/recruiting-talent-management.yml
tags:
- Candidate Gateway
- Job Search
- Recruiting
- Talent Management
---
