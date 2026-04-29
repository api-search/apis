---
aid: factset:factset-exchange-datafeed-data-model-api
baseURL: https://example.com
description: The Exchange DataFeed Data Model API provides mapping tables for enumeration values used in the FactSet Real-Time products.
humanURL: https://developer.factset.com/api-catalog/exchange-datafeed-data-model-api
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: FactSet Exchange DataFeed Data Model API
properties:
- type: Documentation
  url: 'https://raw.githubusercontent.com/api-evangelist/factset/refs/heads/main/

    https://developer.factset.com/api-catalog/exchange-datafeed-data-model-api#overview'
- type: SDK
  url: 'https://raw.githubusercontent.com/api-evangelist/factset/refs/heads/main/

    https://developer.factset.com/api-catalog/exchange-datafeed-data-model-api#sdkLibrary'
- type: Tutorials
  url: 'https://raw.githubusercontent.com/api-evangelist/factset/refs/heads/main/

    https://developer.factset.com/api-catalog/exchange-datafeed-data-model-api#notebooks'
- type: CodeExamples
  url: 'https://raw.githubusercontent.com/api-evangelist/factset/refs/heads/main/

    https://developer.factset.com/api-catalog/exchange-datafeed-data-model-api#codeSnippet'
- type: ChangeLog
  url: 'https://raw.githubusercontent.com/api-evangelist/factset/refs/heads/main/

    https://developer.factset.com/api-catalog/exchange-datafeed-data-model-api#changelog'
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/factset/refs/heads/main/openapi/exchange-datafeed-data-model-openapi-original.yml
provider_name: Factset
provider_slug: factset
slug: factset-exchange-datafeed-data-model-api
source_filename: exchange-datafeed-data-model-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  version: 1.0.0\n  title: Factset Exchange DataFeed Data Model API\n  description: >-\n    FactSet’s Exchange DataFeed products provide access to consolidated\n    real-time and delayed global exchange data. Proprietary technology\n    normalizes over 250 global venues, 18+ million instruments, and 150+ data\n    fields. Asset types integrated include equities, futures, options, warrants,\n    fixed income, mutual funds, ETFs, indices, commodities, and FX rates.\n    Innovative technology ensures reliability and provides scalability that\n    allows clients to make requests based on a symbol list or an exchange.\n    Reduce development time by powering proprietary and third-party applications\n    with exchange data from a unified data model. <p>The Exchange DataFeed Data\n    Model API provides mappings for enumerations used in our Real-Time DataFeed\n    products and should be used in conjunction with the DataFeed Data Model\n    documentation available\
  \ for each product. <p>The initial beta version of\n    this API is limited to include mapping tables for the product codes only.\nservers:\n  - url: https://api.factset.com/RTDataModel\nsecurity:\n  - BasicAuth: []\npaths:\n  /products:\n    get:\n      summary: Request the enumeration table for FactSet product codes.\n      operationId: get_products\n      tags:\n        - Products\n      description: >\n        Data can be returned in CSV, JSON or XML format, use the `format`\n        parameter to chnage from the default JSON format.\n      parameters:\n        - $ref: '#/components/parameters/format'\n      responses:\n        '200':\n          description: Successful response for the FactSet product codes table\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/RTDataModel_Products'\n              example:\n                - product_code: 9001\n                  description: New York Stock Exchange Level 1\n     \
  \           - product_code: 9002\n                  description: Nasdaq Stock Market Level 1\n                - product_code: 9003\n                  description: Nasdaq Stock Market Level 2\n                - product_code: 9004\n                  description: NYSE American Level 1\n                - product_code: 9005\n                  description: US Options Composite Pricing Level 1\n            application/xml:\n              schema:\n                $ref: '#/components/schemas/RTDataModel_Products'\n              example: >-\n                <products type=\"array\"> <product>\n                <product-code>9001</product-code> <description>New York Stock\n                Exchange Level 1</description> </product> <product>\n                <product-code>9002</product-code> <description>Nasdaq Stock\n                Market Level 1</description> </product> <product>\n                <product-code>9003</product-code> <description>Nasdaq Stock\n                Market Level 2</description>\
  \ </product> <product>\n                <product-code>9004</product-code> <description>NYSE American\n                Level 1</description> </product> <product>\n                <product-code>9005</product-code> <description>US Options\n                Composite Pricing Level 1</description> </product> </products>\n        '401':\n          description: >-\n            Unauthenticated USERNAME-SERIAL. Ensure you are logged in and have\n            successfully generated an API KEY for the IP range you are\n            connecting from.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/errorResponse'\n              example:\n                status: 401\n                error: Unauthorized\n        '402':\n          description: Invalid method.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/errorResponse'\n              example:\n                status:\
  \ 402\n                error: Invalid method\n        '404':\n          description: The provided report name is not valid.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/errorResponse'\n              example:\n                status: 404\n                error: Not Found\ncomponents:\n  securitySchemes:\n    BasicAuth:\n      type: http\n      scheme: basic\n  parameters:\n    format:\n      name: format\n      description: >-\n        The format of the output file.<p>**Try it Out** - All formats\n        available</p>\n      in: query\n      schema:\n        type: string\n        default: json\n        enum:\n          - xml\n          - json\n          - csv\n  schemas:\n    RTDataModel_Products:\n      type: object\n      title: Product codes\n      description: sample response\n      properties:\n        product_code:\n          example: 9001\n          type: integer\n          description: FactSet product code\n\
  \        description:\n          example: New York Stock Exchange Level 1\n          type: string\n          description: Product description\n    errorResponse:\n      type: object\n      title: Error Response\n      properties:\n        status:\n          description: status\n          type: integer\n          example: 401\n        error:\n          description: The plain text error message\n          type: string\n          example: Unauthorized\ntags:\n  - name: Products\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/factset/refs/heads/main/openapi/exchange-datafeed-data-model-openapi-original.yml
tags: []
---
