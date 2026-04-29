---
aid: google-analytics:google-analytics-user-deletion-api
baseURL: https://www.googleapis.com/analytics/v3
description: The User Deletion API enables removal of data linked to specific user identifiers in Google Analytics, supporting compliance with data protection and privacy requirements.
humanURL: https://developers.google.com/analytics/devguides/config/userdeletion/v3
image: https://www.google.com/analytics/images/google-analytics-logo.png
layout: api
name: Google Analytics User Deletion API
properties:
- type: Documentation
  url: https://developers.google.com/analytics/devguides/config/userdeletion/v3
- type: APIReference
  url: https://developers.google.com/analytics/devguides/config/userdeletion/v3/reference
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-analytics/refs/heads/main/openapi/google-analytics-user-deletion-api.yaml
- type: Authentication
  url: https://developers.google.com/analytics/devguides/config/userdeletion/v3/authorization
provider_name: Google Analytics
provider_slug: google-analytics
slug: google-analytics-user-deletion-api
source_filename: google-analytics-user-deletion-api.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Google Analytics User Deletion API\n  description: >-\n    The Google Analytics User Deletion API enables removal of data linked to\n    specific user identifiers, supporting compliance with data protection and\n    privacy requirements such as GDPR. Supports deletion by CLIENT_ID, USER_ID,\n    and APP_INSTANCE_ID. Data appears in Individual User Reports within 72\n    hours and complete deletion occurs during bimonthly processes.\n  version: v3\n  contact:\n    name: Google Analytics\n    url: https://developers.google.com/analytics\n  license:\n    name: Google APIs Terms of Service\n    url: https://developers.google.com/analytics/terms\n  x-logo:\n    url: https://www.google.com/analytics/images/google-analytics-logo.png\nexternalDocs:\n  description: User Deletion API documentation\n  url: https://developers.google.com/analytics/devguides/config/userdeletion/v3\nservers:\n- url: https://www.googleapis.com/analytics/v3\n  description: Google\
  \ Analytics API v3\npaths:\n  /userDeletion/userDeletionRequests:upsert:\n    post:\n      operationId: upsertUserDeletionRequest\n      summary: Google Analytics Insert or Update a User Deletion Request\n      description: >-\n        Inserts or updates a user deletion request. Submitting a deletion\n        request for a user that already has a pending request will update the\n        existing request. The User Deletion API does not remove data from\n        reports based on previously aggregated data or exported datasets like\n        BigQuery.\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/UserDeletionRequest'\n      responses:\n        '200':\n          description: Successful user deletion request\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/UserDeletionRequest'\n        '400':\n          description:\
  \ Invalid request - malformed body or invalid ID type\n        '401':\n          description: Authentication required\n        '403':\n          description: Insufficient permissions - missing required OAuth scope\n      security:\n      - oauth2:\n        - https://www.googleapis.com/auth/analytics.user.deletion\n      tags:\n      - User Deletion\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: oauth2\n      description: OAuth 2.0 authentication\n      flows:\n        authorizationCode:\n          authorizationUrl: https://accounts.google.com/o/oauth2/auth\n          tokenUrl: https://oauth2.googleapis.com/token\n          scopes:\n            https://www.googleapis.com/auth/analytics.user.deletion: >-\n              Delete user data from Google Analytics\n  schemas:\n    UserDeletionRequest:\n      type: object\n      required:\n      - id\n      properties:\n        kind:\n          type: string\n\
  \          description: Resource type identifier.\n          default: analytics#userDeletionRequest\n          readOnly: true\n          example: example_value\n        id:\n          $ref: '#/components/schemas/UserDeletionId'\n        webPropertyId:\n          type: string\n          description: >-\n            The Web Property ID for a Universal Analytics property. Required\n            for Universal Analytics properties.\n          example: '123456'\n        firebaseProjectId:\n          type: string\n          description: >-\n            The Firebase Project ID. Required for app streams using\n            APP_INSTANCE_ID.\n          example: '123456'\n        propertyId:\n          type: string\n          description: The GA4 property ID.\n          example: '123456'\n        deletionRequestTime:\n          type: string\n          format: date-time\n          description: >-\n            The time when the deletion request was submitted. Set by the\n            server.\n        \
  \  readOnly: true\n          example: '2026-04-17T12:00:00Z'\n    UserDeletionId:\n      type: object\n      required:\n      - type\n      - userId\n      properties:\n        type:\n          type: string\n          description: The type of user identifier.\n          enum:\n          - CLIENT_ID\n          - USER_ID\n          - APP_INSTANCE_ID\n          example: CLIENT_ID\n        userId:\n          type: string\n          description: >-\n            The actual user identifier value corresponding to the specified\n            type.\n          example: '123456'\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-analytics/refs/heads/main/openapi/google-analytics-user-deletion-api.yaml
tags:
- Compliance
- Data Privacy
- GDPR
- User Deletion
---
