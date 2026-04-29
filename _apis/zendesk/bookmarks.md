---
aid: zendesk:bookmarks
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Bookmarks API lets you programmatically manage an agents personal starred items in Zendesk, providing endpoints to list, create, and delete bookmarks. A bookmark is a lightweight record that points to another Zendesk resource (for example, something an agent wants quick access to in the interface), and its scoped to the user who created it. With the API you can fetch all of a users bookmarks, add new ones to surface important work, and remove those that are no longer relevant.
humanURL: https://developer.zendesk.com/api-reference/ticketing/ticket-management/bookmarks/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Bookmarks API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/ticket-management/bookmarks/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/bookmarks-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: bookmarks
source_filename: bookmarks-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Bookmarks\n  description: Needs a description.\npaths:\n  /api/v2/bookmarks:\n    get:\n      operationId: ListBookmarks\n      tags:\n        - Bookmarks\n      summary: Zendesk Get  Api V2 Bookmarks\n      description: |-\n        #### Allowed For\n        - Agents\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/BookmarksResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/BookmarksResponse'\n    post:\n      operationId: CreateBookmark\n      tags:\n        - Bookmarks\n      summary: Zendesk Post  Api V2 Bookmarks\n      description: |-\n        #### Allowed For\n        - Agents\n      requestBody:\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/BookmarkCreateRequest'\n\
  \            examples:\n              default:\n                $ref: '#/components/examples/BookmarkCreateRequest'\n      responses:\n        '200':\n          description: Successfully created\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/BookmarkResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/BookmarkResponse'\n        '201':\n          description: Successfully created\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/BookmarkResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/BookmarkResponse'\n  /api/v2/bookmarks/{bookmark_id}:\n    parameters:\n      - $ref: '#/components/parameters/BookmarkId'\n    delete:\n      operationId: DeleteBookmark\n      tags:\n        - Bookmarks\n      summary: Zendesk Delete  Api V2 Bookmarks\
  \ Bookmark_id\n      description: >-\n        #### Allowed For\n\n        - Agents (own bookmarks only)\n\n\n        If the bookmark already exists with a specified ticket id, the response\n        status will be `http Status: 200 OK`.\n      responses:\n        '204':\n          description: No content\ncomponents:\n  schemas:\n    BookmarksResponse:\n      title: Bookmarks\n      type: object\n      allOf:\n        - $ref: '#/components/schemas/OffsetPaginationObject'\n        - type: object\n          properties:\n            bookmarks:\n              type: array\n              items:\n                $ref: '#/components/schemas/BookmarkObject'\n    BookmarkResponse:\n      type: object\n      properties:\n        bookmark:\n          $ref: '#/components/schemas/BookmarkObject'\ntags:\n  - name: Bookmarks\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/bookmarks-openapi-original.yml
tags:
- Bookmarks
---
