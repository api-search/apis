---
aid: hubspot:hubspot-crm-search-api
baseURL: https://api.hubapi.com
description: The CRM Search API allows you to query and filter CRM objects using a flexible search interface. You can search across contacts, companies, deals, tickets, and other object types using filter groups, sorts, and pagination.
humanURL: https://developers.hubspot.com/docs/guides/api/crm/search
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: HubSpot CRM Search API
properties:
- type: Documentation
  url: https://developers.hubspot.com/docs/guides/api/crm/search
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/openapi/hubspot-crm-search-api-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-schema/crm-search-api-crmobject-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-schema/crm-search-api-filter-group-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-schema/crm-search-api-filter-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-schema/crm-search-api-paging-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-schema/crm-search-api-search-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-schema/crm-search-api-search-response-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-schema/crm-search-api-sort-schema.json
- title: JSON Structure
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-structure/crm-search-api-crmobject-structure.json
- title: JSON Structure
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-structure/crm-search-api-filter-group-structure.json
- title: JSON Structure
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-structure/crm-search-api-filter-structure.json
- title: JSON Structure
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-structure/crm-search-api-paging-structure.json
- title: JSON Structure
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-structure/crm-search-api-search-request-structure.json
- title: JSON Structure
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-structure/crm-search-api-search-response-structure.json
- title: JSON Structure
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/json-structure/crm-search-api-sort-structure.json
- type: CodeExamples
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/examples/crm-search-api-crmobject-example.json
- type: CodeExamples
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/examples/crm-search-api-filter-example.json
- type: CodeExamples
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/examples/crm-search-api-filter-group-example.json
- type: CodeExamples
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/examples/crm-search-api-paging-example.json
- type: CodeExamples
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/examples/crm-search-api-search-request-example.json
- type: CodeExamples
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/examples/crm-search-api-search-response-example.json
- type: CodeExamples
  url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/examples/crm-search-api-sort-example.json
provider_name: HubSpot
provider_slug: hubspot
slug: hubspot-crm-search-api
source_filename: hubspot-crm-search-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: HubSpot CRM Search API\n  description: >-\n    The CRM Search API allows you to query and filter CRM objects using a\n    flexible search interface. You can search across contacts, companies, deals,\n    tickets, and other object types using filter groups, sorts, and pagination.\n    Each search request targets a specific object type.\n  version: v3\n  contact:\n    name: HubSpot Developer Support\n    url: https://developers.hubspot.com/\nservers:\n- url: https://api.hubapi.com\n  description: HubSpot API\nsecurity:\n- oauth2: []\ntags:\n- name: Search\n  description: Operations for searching CRM objects\npaths:\n  /crm/v3/objects/{objectType}/search:\n    post:\n      operationId: searchCRMObjects\n      summary: Hubspot Search Crm Objects\n      description: >-\n        Searches for CRM object records of the specified type using filter\n        groups, sort criteria, and other query parameters. Supports complex\n        filtering with multiple\
  \ filter groups (joined with OR logic) where\n        each group contains filters (joined with AND logic). Returns matching\n        records with the specified properties.\n      tags:\n      - Search\n      parameters:\n      - name: objectType\n        in: path\n        required: true\n        description: >-\n          The type of CRM object to search. Supported values include contacts,\n          companies, deals, tickets, products, line_items, quotes, and\n          custom object type names.\n        schema:\n          type: string\n          example: contacts\n        example: contacts\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/SearchRequest'\n            examples:\n              filterByEmail:\n                summary: Filter contacts by email domain\n                value:\n                  filterGroups:\n                  - filters:\n                    - propertyName:\
  \ email\n                      operator: CONTAINS_TOKEN\n                      value: '@example.com'\n                  properties:\n                  - email\n                  - firstname\n                  - lastname\n                  limit: 10\n              filterByDealStage:\n                summary: Filter deals by stage and amount\n                value:\n                  filterGroups:\n                  - filters:\n                    - propertyName: dealstage\n                      operator: EQ\n                      value: contractsent\n                    - propertyName: amount\n                      operator: GT\n                      value: '10000'\n                  sorts:\n                  - propertyName: amount\n                    direction: DESCENDING\n                  properties:\n                  - dealname\n                  - amount\n                  - dealstage\n                  - closedate\n                  limit: 20\n      responses:\n        '200':\n\
  \          description: Search results returned successfully.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SearchResponse'\n              examples:\n                Searchcrmobjects200Example:\n                  summary: Default searchCRMObjects 200 response\n                  x-microcks-default: true\n                  value:\n                    total: 10\n                    results: &id002\n                    - id: '500123'\n                      properties: &id001\n                        key: value\n                      createdAt: '2025-03-15T14:30:00Z'\n                      updatedAt: '2025-03-15T14:30:00Z'\n                      archived: true\n                    paging:\n                      next: {}\n        '400':\n          $ref: '#/components/responses/BadRequest'\n        '401':\n          $ref: '#/components/responses/Unauthorized'\n      x-microcks-operation:\n        delay: 0\n        dispatcher:\
  \ FALLBACK\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: http\n      scheme: bearer\n      description: OAuth 2.0 Bearer token (access token from OAuth flow)\n  schemas:\n    SearchRequest:\n      type: object\n      description: >-\n        A search request for CRM objects. Filter groups are combined with OR\n        logic; filters within a group are combined with AND logic.\n      properties:\n        filterGroups:\n          type: array\n          description: >-\n            An array of filter groups. Records matching any filter group will\n            be included in results (OR logic between groups). Filters within\n            a group are all required (AND logic within groups).\n          items:\n            $ref: '#/components/schemas/FilterGroup'\n          example:\n          - filters:\n            - {}\n        sorts:\n          type: array\n          description: An array of sort criteria to order the results.\n          items:\n            $ref: '#/components/schemas/Sort'\n\
  \          example:\n          - propertyName: Example Record\n            direction: ASCENDING\n        query:\n          type: string\n          description: >-\n            A full-text search query string. When provided, returns records\n            where any searchable property contains the query term.\n          example: example-value\n        properties:\n          type: array\n          description: >-\n            An array of property names to include in the response for each\n            record. If not specified, a default set of properties is returned.\n          items:\n            type: string\n          example:\n          - example-value\n        limit:\n          type: integer\n          description: The maximum number of results to return. Maximum value is 200.\n          default: 10\n          maximum: 200\n          example: 10\n        after:\n          type: string\n          description: >-\n            The cursor token for pagination. Use the value from the previous\n\
  \            response's paging.next.after to get the next page of results.\n          example: example-value\n    FilterGroup:\n      type: object\n      description: >-\n        A group of filter conditions combined with AND logic. Use multiple\n        filter groups to create OR conditions between groups.\n      properties:\n        filters:\n          type: array\n          description: An array of filters, all of which must match (AND logic).\n          items:\n            $ref: '#/components/schemas/Filter'\n          example:\n          - propertyName: Example Record\n            operator: EQ\n            value: example-value\n            highValue: example-value\n            values:\n            - {}\n    Filter:\n      type: object\n      description: A single filter condition for a CRM object property.\n      required:\n      - propertyName\n      - operator\n      properties:\n        propertyName:\n          type: string\n          description: The name of the CRM property to\
  \ filter on.\n          example: Example Record\n        operator:\n          type: string\n          description: The comparison operator for the filter.\n          enum:\n          - EQ\n          - NEQ\n          - LT\n          - LTE\n          - GT\n          - GTE\n          - BETWEEN\n          - IN\n          - NOT_IN\n          - HAS_PROPERTY\n          - NOT_HAS_PROPERTY\n          - CONTAINS_TOKEN\n          - NOT_CONTAINS_TOKEN\n          example: EQ\n        value:\n          type: string\n          description: >-\n            The value to compare against. Not required for HAS_PROPERTY and\n            NOT_HAS_PROPERTY operators.\n          example: example-value\n        highValue:\n          type: string\n          description: >-\n            The upper bound value for BETWEEN operator comparisons.\n          example: example-value\n        values:\n          type: array\n          items:\n            type: string\n          description: >-\n            An array of values\
  \ for IN and NOT_IN operator comparisons.\n          example:\n          - example-value\n    Sort:\n      type: object\n      description: A sort criterion for ordering search results.\n      required:\n      - propertyName\n      properties:\n        propertyName:\n          type: string\n          description: The name of the CRM property to sort by.\n          example: Example Record\n        direction:\n          type: string\n          description: The sort direction.\n          enum: [ASCENDING, DESCENDING]\n          default: ASCENDING\n          example: ASCENDING\n    CRMObject:\n      type: object\n      description: A CRM object record returned from a search.\n      properties:\n        id:\n          type: string\n          description: The unique identifier for the CRM record.\n          example: '500123'\n        properties:\n          type: object\n          description: The CRM record's properties as key-value pairs.\n          additionalProperties:\n            type:\
  \ string\n          example: *id001\n        createdAt:\n          type: string\n          format: date-time\n          description: The date and time the record was created.\n          example: '2025-03-15T14:30:00Z'\n        updatedAt:\n          type: string\n          format: date-time\n          description: The date and time the record was last updated.\n          example: '2025-03-15T14:30:00Z'\n        archived:\n          type: boolean\n          description: Whether the record has been archived.\n          example: true\n    SearchResponse:\n      type: object\n      description: The response from a CRM search operation.\n      properties:\n        total:\n          type: integer\n          description: The total number of records matching the search criteria.\n          example: 10\n        results:\n          type: array\n          description: The matching CRM records for the current page.\n          items:\n            $ref: '#/components/schemas/CRMObject'\n          example:\
  \ *id002\n        paging:\n          $ref: '#/components/schemas/Paging'\n    Paging:\n      type: object\n      description: Pagination information for the response.\n      properties:\n        next:\n          type: object\n          description: Information for retrieving the next page of results.\n          properties:\n            after:\n              type: string\n              description: The cursor token to use in the after parameter for the next page.\n            link:\n              type: string\n              description: A URL link to the next page of results.\n          example:\n            after: example-value\n            link: https://app.hubspot.com/contacts/12345\n    Error:\n      type: object\n      description: An error response.\n      properties:\n        status:\n          type: string\n          example: active\n        message:\n          type: string\n          example: This is an example description.\n        correlationId:\n          type: string\n    \
  \      example: '500123'\n        category:\n          type: string\n          example: standard\n        errors:\n          type: array\n          items:\n            type: object\n            properties:\n              message:\n                type: string\n              in:\n                type: string\n              code:\n                type: string\n          example:\n          - message: This is an example description.\n            in: example-value\n            code: example-value\n  responses:\n    Unauthorized:\n      description: Authentication credentials are missing or invalid.\n      content:\n        application/json:\n          schema:\n            $ref: '#/components/schemas/Error'\n    BadRequest:\n      description: The request is invalid or missing required parameters.\n      content:\n        application/json:\n          schema:\n            $ref: '#/components/schemas/Error'\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hubspot/refs/heads/main/openapi/hubspot-crm-search-api-openapi.yml
tags:
- CRM
- Query
- Search
---
