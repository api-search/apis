---
aid: alation:search-api
baseURL: https://your-instance.alation.com/integration/v2
description: REST API for searching and discovering catalog assets in Alation. Supports full-text search, AI-powered aggregated context retrieval, and article browsing.
humanURL: https://developer.alation.com
image: ''
layout: api
name: Alation Search API
properties:
- type: Documentation
  url: https://developer.alation.com
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/openapi/alation-search-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/json-schema/alation-alation-search-search-result-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/json-schema/alation-alation-search-search-results-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/json-schema/alation-alation-search-context-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/json-schema/alation-alation-search-article-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/json-structure/alation-alation-search-search-result-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/json-structure/alation-alation-search-search-results-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/json-structure/alation-alation-search-context-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/json-structure/alation-alation-search-article-structure.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/examples/alation-alation-search-search-result-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/examples/alation-alation-search-search-results-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/examples/alation-alation-search-context-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/examples/alation-alation-search-article-example.json
provider_name: Alation
provider_slug: alation
slug: search-api
source_filename: alation-search-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Alation Search API\n  description: >-\n    REST API for searching and discovering catalog assets in the Alation\n    data intelligence platform. Supports full-text search, AI-powered\n    semantic search, and aggregated context retrieval.\n  version: 1.0.0\n  contact:\n    name: Alation Developer Support\n    url: https://developer.alation.com\nservers:\n  - url: https://{instance}/integration/v2\n    description: Alation instance\n    variables:\n      instance:\n        default: your-alation-instance.com\nsecurity:\n  - BearerToken: []\ntags:\n  - name: Search\n    description: Search catalog assets\n  - name: Aggregated Context\n    description: Retrieve aggregated context for AI applications\npaths:\n  /search/:\n    get:\n      operationId: searchCatalog\n      summary: Search the catalog\n      description: >-\n        Full-text search across all catalog objects including tables, columns,\n        data sources, glossary terms, and queries.\n\
  \      tags:\n        - Search\n      parameters:\n        - name: q\n          in: query\n          required: true\n          description: Search query string\n          schema:\n            type: string\n        - name: type\n          in: query\n          description: Filter by object type\n          schema:\n            type: string\n            enum: [table, attribute, datasource, schema, glossary_term, query, article]\n        - name: limit\n          in: query\n          schema:\n            type: integer\n            default: 20\n            maximum: 100\n        - name: skip\n          in: query\n          schema:\n            type: integer\n            default: 0\n      responses:\n        '200':\n          description: Search results\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SearchResults'\n        '401':\n          description: Unauthorized\n  /aggregated_context/:\n    post:\n      operationId: getAggregatedContext\n\
  \      summary: Get aggregated context\n      description: >-\n        Retrieves relevant catalog context for a given query or set of objects,\n        optimized for AI and LLM consumption.\n      tags:\n        - Aggregated Context\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/ContextRequest'\n      responses:\n        '200':\n          description: Aggregated context\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ContextResponse'\n        '400':\n          description: Invalid request\n  /article/:\n    get:\n      operationId: listArticles\n      summary: List articles\n      description: Returns catalog articles (wiki pages and documentation).\n      tags:\n        - Search\n      parameters:\n        - name: limit\n          in: query\n          schema:\n            type: integer\n            default: 100\n\
  \        - name: skip\n          in: query\n          schema:\n            type: integer\n            default: 0\n        - name: search\n          in: query\n          schema:\n            type: string\n      responses:\n        '200':\n          description: List of articles\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ArticleList'\n  /article/{id}/:\n    get:\n      operationId: getArticle\n      summary: Get an article\n      description: Returns a specific catalog article.\n      tags:\n        - Search\n      parameters:\n        - name: id\n          in: path\n          required: true\n          schema:\n            type: integer\n      responses:\n        '200':\n          description: Article details\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Article'\ncomponents:\n  securitySchemes:\n    BearerToken:\n      type: http\n      scheme:\
  \ bearer\n  schemas:\n    SearchResult:\n      type: object\n      properties:\n        id:\n          type: integer\n        object_type:\n          type: string\n        title:\n          type: string\n        description:\n          type: string\n        url:\n          type: string\n          format: uri\n        score:\n          type: number\n          format: float\n          description: Relevance score\n        breadcrumb:\n          type: string\n          description: Path to the object in the catalog hierarchy\n    SearchResults:\n      type: object\n      properties:\n        total:\n          type: integer\n        results:\n          type: array\n          items:\n            $ref: '#/components/schemas/SearchResult'\n    ContextRequest:\n      type: object\n      required:\n        - query\n      properties:\n        query:\n          type: string\n          description: Natural language query for context retrieval\n        object_types:\n          type: array\n       \
  \   items:\n            type: string\n          description: Filter results by object types\n        limit:\n          type: integer\n          default: 10\n    ContextResponse:\n      type: object\n      properties:\n        context:\n          type: array\n          items:\n            type: object\n            properties:\n              object_type:\n                type: string\n              object_id:\n                type: integer\n              title:\n                type: string\n              description:\n                type: string\n              metadata:\n                type: object\n                additionalProperties: true\n    Article:\n      type: object\n      properties:\n        id:\n          type: integer\n        title:\n          type: string\n        body:\n          type: string\n        url:\n          type: string\n          format: uri\n        author:\n          type: integer\n          description: User ID of article author\n        created_at:\n   \
  \       type: string\n          format: date-time\n        updated_at:\n          type: string\n          format: date-time\n    ArticleList:\n      type: array\n      items:\n        $ref: '#/components/schemas/Article'\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/openapi/alation-search-openapi.yaml
tags:
- Search
- Data Discovery
- AI
- Catalog
---
