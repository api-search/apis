---
aid: zendesk:sessions
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Sessions API lets you audit and control users active sign-in sessions in your Zendesk account. It provides endpoints to list current sessions (for the authenticated user or a specified user) and returns metadata such as device/user agent, IP, creation time, and last activity. You can revoke an individual session or all sessions for a user to force logouts across Zendesk web and mobile experiencesuseful for security incidents, offboarding, and SSO changes.
humanURL: https://developer.zendesk.com/api-reference/ticketing/account-configuration/sessions/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Sessions API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/account-configuration/sessions/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/sessions-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: sessions
source_filename: sessions-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Sessions\n  description: Needs a description.\npaths:\n  /api/v2/sessions:\n    parameters:\n      - $ref: '#/components/parameters/UserId'\n    get:\n      operationId: ListSessions\n      tags:\n        - Sessions\n      summary: Zendesk Get  Api V2 Sessions\n      description: >\n        If authenticated as an admin, returns all the account's sessions. If\n        authenticated as an agent or end user, returns only the sessions of the\n        user making the request.\n\n\n        #### Pagination\n\n\n        - Cursor pagination (recommended)\n\n        - Offset pagination\n\n\n        See [Pagination](/api-reference/introduction/pagination/).\n\n\n        #### Allowed For\n\n\n        * Admins, Agents, End users\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SessionsResponse'\n        \
  \      examples:\n                default:\n                  $ref: '#/components/examples/SessionsResponseExample'\n  /api/v2/users/{user_id}/sessions:\n    parameters:\n      - $ref: '#/components/parameters/UserId'\n    delete:\n      operationId: BulkDeleteSessionsByUserId\n      tags:\n        - Sessions\n      summary: Zendesk Delete  Api V2 Users User_id Sessions\n      description: |\n        Deletes all the sessions for a user.\n\n        #### Allowed For\n\n        * Admins, Agents, End users\n      responses:\n        '204':\n          description: No Content\n  /api/v2/users/{user_id}/sessions/{session_id}:\n    parameters:\n      - $ref: '#/components/parameters/SessionId'\n      - $ref: '#/components/parameters/UserId'\n    get:\n      operationId: ShowSession\n      tags:\n        - Sessions\n      summary: Zendesk Get  Api V2 Users User_id Sessions Session_id\n      description: |\n        #### Allowed For\n\n        * Admins, Agents, End users\n      responses:\n     \
  \   '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SessionResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/SessionResponseExample'\n    delete:\n      operationId: DeleteSession\n      tags:\n        - Sessions\n      summary: Zendesk Delete  Api V2 Users User_id Sessions Session_id\n      description: |\n        #### Allowed For\n\n        * Admins, Agents, End users\n      responses:\n        '204':\n          description: No Content\ncomponents:\n  schemas:\n    SessionsResponse:\n      type: object\n      properties:\n        sessions:\n          type: array\n          items:\n            $ref: '#/components/schemas/SessionObject'\n    SessionResponse:\n      type: object\n      properties:\n        session:\n          type: array\n          items:\n            $ref: '#/components/schemas/SessionObject'\n\
  tags:\n  - name: Sessions\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/sessions-openapi-original.yml
tags:
- Sessions
---
