---
aid: zendesk:object-layouts
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Object Layouts API lets you programmatically control how record pages look and behave in Agent Workspace. It provides CRUD endpoints to define which fields and components appear for an object (such as tickets, users, organizations, and Sunshine custom objects), how theyre grouped and ordered into sections or panels, and any conditional visibility rules.
humanURL: https://developer.zendesk.com/api-reference/ticketing/introduction/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Object Layouts API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/introduction/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/object-layouts-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: object-layouts
source_filename: object-layouts-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Object Layouts\n  description: Needs a description.\npaths:\n  /api/v2/object_layouts/{object_type}/essentials_card:\n    parameters:\n      - $ref: '#/components/parameters/EssentialsCardKey'\n    get:\n      operationId: ShowEssentialsCard\n      tags:\n        - Essentials Card\n      summary: Zendesk Get  Api V2 Object_layouts Object_type Essentials_card\n      description: |\n        Gets the essentials card for an object type.\n        #### Allowed For\n        * Admins and agents\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/EssentialsCardResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/EssentialsCardExample'\n    put:\n      operationId: UpdateEssentialsCard\n      tags:\n        - Essentials Card\n      summary: Zendesk Put\
  \  Api V2 Object_layouts Object_type Essentials_card\n      description: |\n        Updates the essentials card for an object type.\n        #### Allowed For\n        * Admins\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/EssentialsCardResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/EssentialsCardExample'\n    delete:\n      operationId: DeleteEssentialsCard\n      tags:\n        - Essentials Card\n      summary: Zendesk Delete  Api V2 Object_layouts Object_type Essentials_card\n      description: |\n        Delete the essentials card for an object type.\n        #### Allowed For\n        * Admins and agents\n      responses:\n        '204':\n          description: Success response\n  /api/v2/object_layouts/essentials_cards:\n    get:\n      operationId: ShowEssentialsCards\n    \
  \  tags:\n        - Essentials Card\n      summary: Zendesk Get  Api V2 Object_layouts Essentials_cards\n      description: |\n        Gets the list of essentials cards.\n        #### Allowed For\n        * Admins\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/EssentialsCardsResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/EssentialsCardsExample'\ncomponents:\n  schemas:\n    EssentialsCardResponse:\n      type: object\n      properties:\n        object_layout:\n          $ref: '#/components/schemas/EssentialsCardObject'\n    EssentialsCardsResponse:\n      type: object\n      properties:\n        object_layouts:\n          type: array\n          items:\n            $ref: '#/components/schemas/EssentialsCardObject'\ntags:\n  - name: Essentials Card\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/object-layouts-openapi-original.yml
tags:
- Object Layouts
---
