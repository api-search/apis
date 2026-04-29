---
aid: cisco-webex:webex-attachment-actions-api
baseURL: https://webexapis.com/v1
description: Create and retrieve attachment actions for adaptive card interactions. Used with Buttons and Cards to capture user input from interactive card elements submitted in Webex messaging spaces.
humanURL: https://developer.webex.com/docs/api/v1/attachment-actions
image: https://www.webex.com/content/dam/wbx/us/images/webex-logo.svg
layout: api
name: Webex Attachment Actions API
properties:
- type: Documentation
  url: https://developer.webex.com/docs/api/v1/attachment-actions
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-attachment-actions-openapi.yml
provider_name: Cisco Webex
provider_slug: cisco-webex
slug: webex-attachment-actions-api
source_filename: cisco-webex-attachment-actions-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cisco Webex Attachment Actions API\n  description: >-\n    Create and retrieve attachment actions for adaptive card interactions.\n    Used with Buttons and Cards to capture user input from interactive card\n    elements submitted in Webex messaging spaces.\n  version: 1.0.0\n  contact:\n    name: Cisco Webex Developer Support\n    url: https://developer.webex.com/support\n  license:\n    name: Cisco Webex API Terms of Service\n    url: https://developer.webex.com/terms-of-service\nservers:\n  - url: https://webexapis.com/v1\n    description: Webex Production API\nsecurity:\n  - bearerAuth: []\ntags:\n  - name: Attachment Actions\n    description: Operations for managing adaptive card attachment actions\npaths:\n  /attachment/actions:\n    post:\n      operationId: createAttachmentAction\n      summary: Cisco Webex Create an Attachment Action\n      description: >-\n        Creates an attachment action representing a user's interaction with\n\
  \        an adaptive card. The action captures the user's input from the\n        card form fields.\n      tags:\n        - Attachment Actions\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/CreateAttachmentActionRequest'\n      responses:\n        '202':\n          description: Attachment action created successfully.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/AttachmentAction'\n        '400':\n          description: Bad request - invalid input parameters.\n        '401':\n          description: Unauthorized - invalid or missing access token.\n  /attachment/actions/{id}:\n    get:\n      operationId: getAttachmentActionDetails\n      summary: Cisco Webex Get Attachment Action Details\n      description: >-\n        Shows details for an attachment action by ID. Returns the action\n        metadata and user-provided\
  \ input data from the adaptive card.\n      tags:\n        - Attachment Actions\n      parameters:\n        - name: id\n          in: path\n          required: true\n          description: Unique identifier for the attachment action.\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Successful response with attachment action details.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/AttachmentAction'\n        '404':\n          description: Attachment action not found.\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      description: >-\n        Webex API access token. Obtain via OAuth 2.0 authorization flow or\n        personal access token from developer.webex.com.\n  schemas:\n    AttachmentAction:\n      type: object\n      properties:\n        id:\n          type: string\n          description: Unique identifier for the\
  \ attachment action.\n        type:\n          type: string\n          description: The type of action.\n          enum:\n            - submit\n        messageId:\n          type: string\n          description: The parent message ID containing the adaptive card.\n        personId:\n          type: string\n          description: The person ID who performed the action.\n        roomId:\n          type: string\n          description: The room ID where the action occurred.\n        inputs:\n          type: object\n          description: >-\n            User-provided form data from the adaptive card. Keys correspond\n            to the input field IDs defined in the card.\n          additionalProperties: true\n        created:\n          type: string\n          format: date-time\n          description: Date and time the action was created.\n    CreateAttachmentActionRequest:\n      type: object\n      required:\n        - type\n        - messageId\n        - inputs\n      properties:\n    \
  \    type:\n          type: string\n          description: The type of action. Currently only 'submit' is supported.\n          enum:\n            - submit\n        messageId:\n          type: string\n          description: The message ID containing the adaptive card.\n        inputs:\n          type: object\n          description: User input data from the adaptive card fields.\n          additionalProperties: true\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-attachment-actions-openapi.yml
tags:
- Attachment Actions
- Buttons
- Cards
- Interactive
- Messaging
---
