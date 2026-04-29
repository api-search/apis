---
aid: peoplesoft:enterprise-performance-management-api
baseURL: https://{hostname}:{port}/psft/api/epm/v1
description: Analytics, budgeting, forecasting, and planning APIs with events and notifications framework for financial and operational performance management.
humanURL: https://docs.oracle.com/cd/E41507_01/epm91pbr3/eng/epm/penw/index.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Enterprise Performance Management API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E41507_01/epm91pbr3/eng/epm/penw/index.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/enterprise-performance-management.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: enterprise-performance-management-api
source_filename: enterprise-performance-management.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Enterprise Performance Management API\n  description: Analytics, budgeting, forecasting, and planning APIs with events and notifications framework for financial and operational performance management.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/epm/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: PeopleSoft EPM Documentation\n  url: https://docs.oracle.com/cd/E41507_01/epm91pbr3/eng/epm/penw/index.html\ntags:\n- name: Budgets\n  description: Budget management operations\n- name: Forecasts\n  description: Forecasting operations\n\
  - name: Analytics\n  description: Analytics and reporting operations\npaths:\n  /budgets:\n    get:\n      summary: PeopleSoft List Budgets\n      description: Retrieve budget definitions and data.\n      operationId: listBudgets\n      tags:\n      - Budgets\n      security:\n      - basicAuth: []\n      parameters:\n      - name: fiscalYear\n        in: query\n        description: Fiscal year filter\n        schema:\n          type: string\n        example: example_value\n      - name: businessUnit\n        in: query\n        description: Business unit filter\n        schema:\n          type: string\n        example: example_value\n      responses:\n        '200':\n          description: Successful response with budget data\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /forecasts:\n    get:\n   \
  \   summary: PeopleSoft List Forecasts\n      description: Retrieve forecast data and projections.\n      operationId: listForecasts\n      tags:\n      - Forecasts\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with forecast data\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /analytics/reports:\n    get:\n      summary: PeopleSoft List Analytics Reports\n      description: Retrieve performance analytics reports.\n      operationId: listAnalyticsReports\n      tags:\n      - Analytics\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with analytics reports\n          content:\n            application/json:\n              schema:\n                type: object\n \
  \       '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/enterprise-performance-management.yml
tags:
- Analytics
- Budgeting
- EPM
- Forecasting
- Planning
---
