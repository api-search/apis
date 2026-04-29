---
aid: zendesk:relationships
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Relationships API lets you model, create, and query links between data entities in Zendesk, spanning both standard resources (like users, organizations, and tickets) and Custom Objects. You define relationship types with explicit cardinality (one-to-one, one-to-many, or many-to-many), then create relationship records that connect specific instancesfor example, associating a customer with their devices, subscriptions, or locations, or tying tickets to assets or accounts.
humanURL: https://developer.zendesk.com/api-reference/ticketing/lookup_relationships/lookup_relationships/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Relationships API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/lookup_relationships/lookup_relationships/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/relationships-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: relationships
source_filename: relationships-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Relationships\n  description: Needs a description.\npaths:\n  /api/v2/relationships/definitions/{target_type}:\n    get:\n      operationId: GetRelationshipFilterDefinitions\n      tags:\n        - Lookup Relationships\n      summary: Zendesk Get  Api V2 Relationships Definitions Target_type\n      description: >\n        Returns filter definitions based on the given target type.  Target types\n\n        include users (zen:user), tickets (zen:ticket), organizations\n        (zen:organization), or custom objects\n        (zen:custom_object:CUSTOM_OBJECT_KEY).\n\n        The returned filter definitions are the options that you can use to\n        build a custom field or ticket field's\n\n        `relationship_filter`.\n      parameters:\n        - name: target_type\n          in: path\n          description: >\n            The target type for which you would like to see filter definitions.\n\n            The options are \"zen:user\", \"\
  zen:ticket\", \"zen:organization\", and\n            \"zen:custom_object:CUSTOM_OBJECT_KEY\"\n          required: true\n          schema:\n            type: string\n          example: zen:custom_object:apartment\n        - name: source_type\n          in: query\n          description: |\n            The source type for which you would like to see filter definitions.\n            The options are \"zen:user\", \"zen:ticket\", and \"zen:organization\"\n          schema:\n            type: string\n          example: zen:user\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/RelationshipFilterDefinitionResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/RelationshipFilterDefinitionExample'\ncomponents:\n  schemas:\n    RelationshipFilterDefinitionResponse:\n      type: object\n      properties:\n\
  \        definitions:\n          $ref: '#/components/schemas/RelationshipFilterDefinition'\ntags:\n  - name: Lookup Relationships\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/relationships-openapi-original.yml
tags:
- Relationships
---
