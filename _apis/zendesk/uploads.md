---
aid: zendesk:uploads
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Uploads API lets you upload files to Zendesk Support so they can be attached to tickets or embedded inline in ticket comments. When you POST a file, the API creates an upload and returns metadata plus a short-lived token. You then include one or more of these tokens when creating or updating a ticket to add the files as attachments. The API supports single-shot and chunked uploads (for large files), and provides endpoints to check an uploads details or delete it.
humanURL: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket-attachments/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Uploads API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket-attachments/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/uploads-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: uploads
source_filename: uploads-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Uploads\n  description: Needs a description.\npaths:\n  /api/v2/uploads:\n    post:\n      operationId: UploadFiles\n      tags:\n        - Attachments\n      summary: Zendesk Post  Api V2 Uploads\n      description: >\n        Uploads a file that can be attached to a ticket comment. It doesn't\n        attach the file to the comment. For details and examples, see [Attaching\n        ticket comments with the\n        API](/documentation/ticketing/using-the-zendesk-api/adding-ticket-attachments-with-the-api).\n\n\n        The endpoint has a required `filename` query parameter. The parameter\n        specifies what the file will be named when attached to the ticket\n        comment (to give the agent more context about the file). The parameter\n        does not specify the file on the local system to be uploaded. While the\n        two names can be different, their file extensions must be the same. If\n        they don't match, the agent's\
  \ browser or file reader could give an error\n        when attempting to open the attachment.\n\n\n        The `Content-Type` header must contain a recognized MIME type that\n        correctly describes the type of the uploaded file. Failing to send a\n        recognized, correct type may cause undesired behavior. For example,\n        in-browser audio playback may be interrupted by the browser's security\n        mechanisms for MP3s uploaded with an incorrect type.\n\n\n        Adding multiple files to the same upload is handled by splitting\n        requests and passing the API token received from the first request to\n        each subsequent request. The token is valid for 60 minutes.\n\n\n        **Note**: Even if [private\n        attachments](https://support.zendesk.com/hc/en-us/articles/204265396)\n        are enabled in the Zendesk Support instance, uploaded files are visible\n        to any authenticated user at the `content_URL` specified in the [JSON\n        response](#json-format)\
  \ until the upload token is consumed. Once a file\n        is associated with a ticket or post, visibility is restricted to users\n        with access to the ticket or post with the attachment.\n\n\n        #### Allowed For\n\n\n        * End users\n      responses:\n        '201':\n          description: Created response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/AttachmentUploadResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/AttachmentUploadResponseExample'\n  /api/v2/uploads/{token}:\n    delete:\n      operationId: DeleteUpload\n      tags:\n        - Attachments\n      summary: Zendesk Delete  Api V2 Uploads Token\n      description: |\n        #### Allowed for\n\n        * End Users\n      parameters:\n        - name: token\n          in: path\n          description: The token of the uploaded attachment\n          required: true\n          schema:\n\
  \            type: string\n          example: 6bk3gql82em5nmf\n      responses:\n        '204':\n          description: No Content response\ncomponents:\n  schemas: {}\ntags:\n  - name: Attachments\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/uploads-openapi-original.yml
tags:
- Uploads
---
