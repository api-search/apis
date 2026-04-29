---
aid: pluralsight:practice-exams-api
baseURL: https://paas-api.pluralsight.com/graphql
description: GraphQL query for retrieving practice exam attempt data including scores and results.
humanURL: https://developer.pluralsight.com
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Practice Exams API
properties:
- type: Documentation
  url: https://developer.pluralsight.com
- type: GraphQL
  url: https://paas-api.pluralsight.com/graphql
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/practice-exams.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: practice-exams-api
source_filename: practice-exams.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Practice Exams API\n  description: GraphQL query for retrieving practice exam attempt data including scores and results.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://paas-api.pluralsight.com\n  description: Production\nexternalDocs:\n  description: Pluralsight Developer Documentation\n  url: https://developer.pluralsight.com\ntags:\n- name: GraphQL\n  description: GraphQL query operations\npaths:\n  /graphql:\n    post:\n      summary: Pluralsight Query Practice Exams\n      description: Execute GraphQL queries to retrieve practice exam attempt data including scores and results.\n      operationId: queryPracticeExams\n      tags:\n      - GraphQL\n      security:\n      - bearerAuth: []\n      requestBody:\n        required: true\n  \
  \      content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/GraphQLRequest'\n      responses:\n        '200':\n          description: Successful GraphQL response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/GraphQLResponse'\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n  schemas:\n    GraphQLRequest:\n      type: object\n      required:\n      - query\n      properties:\n        query:\n          type: string\n          description: The GraphQL query string\n          example: example_value\n        variables:\n          type: object\n          description:\
  \ Variables for the GraphQL query\n        operationName:\n          type: string\n          description: Name of the operation to execute\n          example: Example Course\n    GraphQLResponse:\n      type: object\n      properties:\n        data:\n          type: object\n          description: The query result data\n        errors:\n          type: array\n          items:\n            $ref: '#/components/schemas/GraphQLError'\n          description: Any errors that occurred during query execution\n    GraphQLError:\n      type: object\n      properties:\n        message:\n          type: string\n          description: Error message\n          example: example_value\n        locations:\n          type: array\n          items:\n            type: object\n            properties:\n              line:\n                type: integer\n              column:\n                type: integer\n        path:\n          type: array\n          items:\n            type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/practice-exams.yml
tags:
- Assessments
- Certification Prep
- Graphql
- Practice Exams
---
