---
aid: aptargroup:aptargroup-api
baseURL: ''
description: API for the AptarGroup product catalog of dispensing, sealing, and active packaging solutions for beauty, pharmaceutical, food, and home care markets.
humanURL: https://www.aptargroup.com
image: ''
layout: api
name: AptarGroup API
properties:
- type: Website
  url: https://www.aptargroup.com
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/openapi/aptargroup-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/json-schema/product-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/json-structure/product-structure.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/examples/product-example.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/json-ld/aptargroup-context.jsonld
- type: SpectralRules
  url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/rules/aptargroup-spectral-rules.yml
- type: NaftikoCapability
  url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/capabilities/shared/aptargroup-api.yaml
- type: NaftikoCapability
  url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/capabilities/packaging-sourcing.yaml
- type: Vocabulary
  url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/vocabulary/aptargroup-vocabulary.yaml
provider_name: AptarGroup
provider_slug: aptargroup
slug: aptargroup-api
source_filename: aptargroup-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: AptarGroup Product Catalog API\n  description: >-\n    API for the AptarGroup product catalog of dispensing, sealing, and active\n    packaging solutions for the beauty, personal care, pharmaceutical, food, and\n    home care markets. Enables partners to browse and integrate product data.\n  version: 1.0.0\n  contact:\n    name: AptarGroup\n    url: https://www.aptargroup.com\n  license:\n    name: Proprietary\nservers:\n  - url: https://api.aptargroup.com/v1\n    description: AptarGroup Product Catalog API\nsecurity:\n  - bearerAuth: []\ntags:\n  - name: Products\n    description: AptarGroup product catalog\n  - name: Orders\n    description: Sample and order management\npaths:\n  /products:\n    get:\n      operationId: listProducts\n      summary: AptarGroup - List Products\n      description: Returns a list of AptarGroup dispensing and packaging products\n      tags:\n        - Products\n      parameters:\n        - name: category\n     \
  \     in: query\n          description: Filter by product category (dispensing, sealing, active-packaging)\n          schema:\n            type: string\n        - name: market\n          in: query\n          description: Filter by target market (beauty, pharma, food, home-care)\n          schema:\n            type: string\n        - name: sustainable\n          in: query\n          description: Filter to only sustainable products\n          schema:\n            type: boolean\n      responses:\n        '200':\n          description: A list of products\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      $ref: '#/components/schemas/Product'\n              examples:\n                ListProductsExample:\n                  x-microcks-default: true\n                  summary: Example product list\n      \
  \            value:\n                    data:\n                      - productId: APTAR-PUMP-001\n                        name: EcoStar Airless Pump\n                        category: dispensing\n                        market: beauty\n                        sustainable: true\n        '401':\n          description: Unauthorized - invalid or missing authentication token\n  /products/{productId}:\n    get:\n      operationId: getProduct\n      summary: AptarGroup - Get Product\n      description: Returns details for a specific AptarGroup product\n      tags:\n        - Products\n      parameters:\n        - name: productId\n          in: path\n          required: true\n          description: Unique product identifier\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Product details\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Product'\n              examples:\n\
  \                GetProductExample:\n                  x-microcks-default: true\n                  summary: Example product detail\n                  value:\n                    productId: APTAR-PUMP-001\n                    name: EcoStar Airless Pump\n                    category: dispensing\n                    market: beauty\n                    description: Airless pump dispenser for skincare products\n                    material: recycled-plastic\n                    sustainable: true\n                    sku: ECO-PUMP-50ML\n        '404':\n          description: Product not found\n        '401':\n          description: Unauthorized - invalid or missing authentication token\n  /orders:\n    post:\n      operationId: createSampleRequest\n      summary: AptarGroup - Create Sample Request\n      description: Creates a sample request for AptarGroup packaging products\n      tags:\n        - Orders\n      requestBody:\n        required: true\n        content:\n          application/json:\n\
  \            schema:\n              $ref: '#/components/schemas/SampleRequest'\n            examples:\n              SampleRequestExample:\n                x-microcks-default: true\n                summary: Example sample request\n                value:\n                  productId: APTAR-PUMP-001\n                  quantity: 5\n                  contactEmail: designer@brand.com\n                  notes: Need samples for our new skincare line launch\n      responses:\n        '201':\n          description: Sample request created successfully\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Order'\n        '400':\n          description: Invalid request body\n        '401':\n          description: Unauthorized - invalid or missing authentication token\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n  schemas:\n    Product:\n      title: Product\n     \
  \ description: An AptarGroup dispensing or packaging product\n      type: object\n      properties:\n        productId:\n          type: string\n          description: Unique product identifier\n        name:\n          type: string\n          description: Product name\n        category:\n          type: string\n          description: Product category\n        market:\n          type: string\n          description: Target market\n        description:\n          type: string\n          description: Product description\n        material:\n          type: string\n          description: Primary material\n        sustainable:\n          type: boolean\n          description: Whether the product uses sustainable materials\n        sku:\n          type: string\n          description: Stock keeping unit identifier\n    SampleRequest:\n      title: SampleRequest\n      description: A request for product samples\n      type: object\n      properties:\n        productId:\n          type: string\n\
  \          description: Product to sample\n        quantity:\n          type: integer\n          description: Number of samples requested\n        contactEmail:\n          type: string\n          description: Contact email for the sample request\n        notes:\n          type: string\n          description: Additional notes about the sample request\n    Order:\n      title: Order\n      description: A created sample order\n      type: object\n      properties:\n        orderId:\n          type: string\n          description: Unique order identifier\n        productId:\n          type: string\n          description: Product ordered\n        status:\n          type: string\n          enum: [pending, processing, shipped, delivered]\n          description: Order status\n        createdAt:\n          type: string\n          format: date-time\n          description: Order creation timestamp\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aptargroup/refs/heads/main/openapi/aptargroup-openapi.yaml
tags:
- Packaging
- Dispensing
- Sustainability
- Manufacturing
---
