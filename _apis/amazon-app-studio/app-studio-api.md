---
aid: amazon-app-studio:app-studio-api
baseURL: https://appstudio.amazonaws.com
description: The Amazon App Studio API provides programmatic access to App Studio application management, enabling automation of low-code application lifecycle operations including listing and retrieving application details.
humanURL: https://aws.amazon.com/app-studio/
image: https://a0.awsstatic.com/libra-css/images/logos/aws_logo_smile_1200x630.png
layout: api
name: Amazon App Studio API
properties:
- type: Documentation
  url: https://docs.aws.amazon.com/app-studio/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-app-studio/refs/heads/main/openapi/amazon-app-studio-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-app-studio/refs/heads/main/json-schema/amazon-app-studio-app-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-app-studio/refs/heads/main/json-schema/amazon-app-studio-appsummary-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-app-studio/refs/heads/main/json-schema/amazon-app-studio-listappsresponse-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-app-studio/refs/heads/main/json-structure/amazon-app-studio-app-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amazon-app-studio/refs/heads/main/json-ld/amazon-app-studio-context.jsonld
- type: Pricing
  url: https://aws.amazon.com/app-studio/pricing/
provider_name: Amazon App Studio
provider_slug: amazon-app-studio
slug: app-studio-api
source_filename: amazon-app-studio-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Amazon App Studio API\n  description: Amazon App Studio is a generative AI-powered low-code application builder that enables builders to quickly develop internal business applications. This API provides programmatic access \n    to App Studio application management and deployment capabilities.\n  version: '2024-11-01'\n  contact:\n    name: AWS Support\n    url: https://aws.amazon.com/support/\nservers:\n- url: https://appstudio.{region}.amazonaws.com\n  description: Amazon App Studio endpoint\n  variables:\n    region:\n      default: us-east-1\n      description: AWS region\nsecurity:\n- BearerAuth: []\ncomponents:\n  securitySchemes:\n    BearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: AWS Sig V4\n  schemas:\n    App:\n      type: object\n      description: An Amazon App Studio application.\n      properties:\n        appId:\n          type: string\n          description: Unique identifier for the application.\n  \
  \      name:\n          type: string\n          description: Display name of the application.\n        description:\n          type: string\n          description: Description of the application purpose.\n        status:\n          type: string\n          enum:\n          - CREATING\n          - ACTIVE\n          - DELETING\n          - FAILED\n          description: Current status of the application.\n        createdAt:\n          type: string\n          format: date-time\n          description: Timestamp when the application was created.\n        updatedAt:\n          type: string\n          format: date-time\n          description: Timestamp when the application was last updated.\n      required:\n      - appId\n      - name\n      - status\n    AppSummary:\n      type: object\n      description: Summary information for an App Studio application.\n      properties:\n        appId:\n          type: string\n          description: Unique identifier for the application.\n        name:\n\
  \          type: string\n          description: Display name of the application.\n        status:\n          type: string\n          enum:\n          - CREATING\n          - ACTIVE\n          - DELETING\n          - FAILED\n          description: Current status of the application.\n        createdAt:\n          type: string\n          format: date-time\n          description: Creation timestamp.\n    ListAppsResponse:\n      type: object\n      description: Response containing list of App Studio applications.\n      properties:\n        apps:\n          type: array\n          items:\n            $ref: '#/components/schemas/AppSummary'\n          description: List of applications.\n        nextToken:\n          type: string\n          description: Pagination token for next page.\npaths:\n  /apps:\n    get:\n      operationId: ListApps\n      summary: Amazon App Studio List Apps\n      description: Returns a list of all App Studio applications in the account.\n      tags:\n      - Apps\n\
  \      parameters:\n      - name: maxResults\n        in: query\n        schema:\n          type: integer\n        description: Maximum number of results to return.\n      - name: nextToken\n        in: query\n        schema:\n          type: string\n        description: Pagination token.\n      responses:\n        '200':\n          description: Successful list of applications.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ListAppsResponse'\n        '400':\n          description: Bad request.\n        '500':\n          description: Internal server error.\n  /apps/{appId}:\n    get:\n      operationId: GetApp\n      summary: Amazon App Studio Get App\n      description: Returns details for a specific App Studio application.\n      tags:\n      - Apps\n      parameters:\n      - name: appId\n        in: path\n        required: true\n        schema:\n          type: string\n        description: The unique identifier\
  \ of the application.\n      responses:\n        '200':\n          description: Application details.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/App'\n        '404':\n          description: Application not found.\n        '500':\n          description: Internal server error.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-app-studio/refs/heads/main/openapi/amazon-app-studio-openapi.yaml
tags:
- AWS
- Low-Code
- No-Code
---
