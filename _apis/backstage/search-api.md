---
aid: backstage:search-api
baseURL: ''
description: The Backstage Search API provides endpoints for querying the Backstage search index. It enables full-text search across all indexed content including catalog entities, TechDocs pages, and any other content indexed by search collators. The API supports filtering by document type, pagination via cursors, and term-based queries.
humanURL: https://backstage.io/docs/features/search/
image: ''
layout: api
name: Backstage Search API
properties:
- type: Documentation
  url: https://backstage.io/docs/features/search/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/openapi/backstage-search-openapi.yml
provider_name: Backstage
provider_slug: backstage
slug: search-api
source_filename: backstage-search-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Backstage Search API\n  description: >-\n    The Backstage Search API provides endpoints for querying the Backstage\n    search index. It enables full-text search across all indexed content\n    including catalog entities, TechDocs pages, and any other content\n    indexed by search collators. The API supports filtering by document\n    type, pagination via cursors, and term-based queries.\n  version: 1.0.0\n  contact:\n    name: Backstage\n    url: https://backstage.io\n  license:\n    name: Apache-2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nexternalDocs:\n  description: Backstage Search Documentation\n  url: https://backstage.io/docs/features/search/\nservers:\n  - url: https://localhost:7007/api/search\n    description: Local development server\npaths:\n  /query:\n    get:\n      operationId: searchQuery\n      summary: Backstage Query the search index\n      description: >-\n        Performs a search query against the Backstage\
  \ search index. Returns\n        matching documents with their metadata, ranked by relevance. Supports\n        filtering by document type, term-based queries, and cursor-based\n        pagination for large result sets.\n      tags:\n        - Search\n      security:\n        - bearerAuth: []\n      parameters:\n        - name: term\n          in: query\n          required: false\n          description: The search term to query for.\n          schema:\n            type: string\n        - name: types\n          in: query\n          required: false\n          description: >-\n            Comma-separated list of document types to filter results\n            (e.g., software-catalog, techdocs).\n          schema:\n            type: array\n            items:\n              type: string\n          style: form\n          explode: true\n        - name: filters\n          in: query\n          required: false\n          description: >-\n            Key-value filter pairs to narrow search results.\
  \ Filters are\n            specific to the document type.\n          schema:\n            type: object\n            additionalProperties:\n              type: string\n          style: deepObject\n        - name: pageCursor\n          in: query\n          required: false\n          description: Cursor for pagination. Obtained from a previous search response.\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Search results matching the query.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SearchResultSet'\n        '400':\n          description: Invalid search query parameters.\n        '401':\n          description: Authentication required.\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n  schemas:\n    SearchResultSet:\n      type: object\n      properties:\n        results:\n          type: array\n\
  \          items:\n            $ref: '#/components/schemas/SearchResult'\n          description: Array of search result documents.\n        nextPageCursor:\n          type: string\n          description: Cursor to fetch the next page of results.\n        previousPageCursor:\n          type: string\n          description: Cursor to fetch the previous page of results.\n        numberOfResults:\n          type: integer\n          description: Total number of matching results.\n    SearchResult:\n      type: object\n      properties:\n        type:\n          type: string\n          description: >-\n            The document type (e.g., software-catalog, techdocs).\n        document:\n          $ref: '#/components/schemas/SearchDocument'\n        rank:\n          type: number\n          description: Relevance rank of the result.\n        highlight:\n          type: object\n          properties:\n            preTag:\n              type: string\n            postTag:\n              type: string\n\
  \            fields:\n              type: object\n              additionalProperties:\n                type: string\n    SearchDocument:\n      type: object\n      required:\n        - title\n        - text\n        - location\n      properties:\n        title:\n          type: string\n          description: Title of the document.\n        text:\n          type: string\n          description: Text content of the document.\n        location:\n          type: string\n          description: URL or path to the original content.\n      additionalProperties: true\ntags:\n  - name: Search\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/openapi/backstage-search-openapi.yml
tags:
- Developer Portal
- Discovery
- Search
---
