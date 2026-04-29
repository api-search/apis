---
aid: alchemy:alchemy-transfers-api
baseURL: ''
description: The Alchemy Transfers API provides access to historical on-chain transfer data across EVM-compatible networks. Query asset transfers by address, block range, and transfer category (ETH, ERC-20, ERC-721, ERC-1155, and internal transfers), enabling wallet activity tracking, portfolio history, and transaction auditing.
humanURL: https://www.alchemy.com/transfers-api
image: ''
layout: api
name: Alchemy Transfers API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-transfers-api-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/json-schema/alchemy-transfers-api-asset-transfer-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/json-schema/alchemy-transfers-api-transfer-metadata-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/json-schema/alchemy-transfers-api-asset-transfers-result-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/json-schema/alchemy-transfers-api-asset-transfers-response-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/json-structure/alchemy-transfers-api-asset-transfer-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/json-structure/alchemy-transfers-api-transfer-metadata-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/json-structure/alchemy-transfers-api-asset-transfers-result-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/json-structure/alchemy-transfers-api-asset-transfers-response-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/json-ld/alchemy-transfers-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/examples/alchemy-transfers-api-asset-transfer-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/examples/alchemy-transfers-api-transfer-metadata-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/examples/alchemy-transfers-api-asset-transfers-result-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/examples/alchemy-transfers-api-asset-transfers-response-example.json
provider_name: Alchemy
provider_slug: alchemy
slug: alchemy-transfers-api
source_filename: alchemy-transfers-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Alchemy Transfers API\n  description: >-\n    The Alchemy Transfers API provides access to historical on-chain transfer\n    data across EVM-compatible networks. Developers can query asset transfers\n    by address, block range, and transfer category (ETH, ERC-20, ERC-721,\n    ERC-1155, and internal transfers), enabling wallet activity tracking,\n    portfolio history, and transaction auditing.\n  version: '1.0'\n  contact:\n    name: Alchemy Support\n    url: https://www.alchemy.com/support\n  x-generated-from: documentation\nservers:\n  - url: https://eth-mainnet.g.alchemy.com/v2/{apiKey}\n    description: Ethereum Mainnet\n    variables:\n      apiKey:\n        default: your-api-key\n        description: Your Alchemy API key.\n  - url: https://polygon-mainnet.g.alchemy.com/v2/{apiKey}\n    description: Polygon Mainnet\n    variables:\n      apiKey:\n        default: your-api-key\n        description: Your Alchemy API key.\ntags:\n  - name:\
  \ Transfers\n    description: Query historical asset transfer data across EVM networks.\npaths:\n  /:\n    post:\n      operationId: getAssetTransfers\n      summary: Alchemy Get Asset Transfers\n      description: >-\n        Returns an array of asset transfers based on the specified filters.\n        Supports querying ETH transfers, ERC-20 token transfers, ERC-721 NFT\n        transfers, ERC-1155 multi-token transfers, and internal contract\n        transfers across supported EVM networks.\n      tags:\n        - Transfers\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/JsonRpcRequest'\n            examples:\n              GetAssetTransfersRequestExample:\n                summary: Default getAssetTransfers request\n                x-microcks-default: true\n                value:\n                  id: 1\n                  jsonrpc: '2.0'\n                  method: alchemy_getAssetTransfers\n\
  \                  params:\n                    - fromAddress: '0x0000000000000000000000000000000000000000'\n                      fromBlock: '0xfda53c'\n                      toBlock: latest\n                      category:\n                        - erc721\n                        - erc1155\n                      withMetadata: true\n                      excludeZeroValue: true\n                      maxCount: '0x10'\n                      order: desc\n      security:\n        - apiKeyPath: []\n      responses:\n\n        '200':\n          description: Asset transfers retrieved successfully.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/AssetTransfersResponse'\n              examples:\n                GetAssetTransfers200Example:\n                  summary: Default getAssetTransfers 200 response\n                  x-microcks-default: true\n                  value:\n                    id: 1\n                    jsonrpc:\
  \ '2.0'\n                    result:\n                      transfers:\n                        - blockNum: '0xfda53c'\n                          hash: '0xabc123def456'\n                          from: '0x0000000000000000000000000000000000000000'\n                          to: '0xd8da6bf26964af9d7eed9e03e53415d37aa96045'\n                          value: 1.0\n                          asset: ETH\n                          category: external\n                          metadata:\n                            blockTimestamp: '2026-04-19T10:00:00Z'\n                      pageKey: abc123nextpage\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    apiKeyPath:\n      type: apiKey\n      in: header\n      name: X-Alchemy-Token\n      description: Alchemy API key passed as a header. The API key is also embedded in the server URL path.\n  schemas:\n    JsonRpcRequest:\n      type: object\n      title: JSON-RPC Request\n      description:\
  \ Standard JSON-RPC 2.0 request format for Alchemy API calls.\n      required:\n        - id\n        - jsonrpc\n        - method\n        - params\n      properties:\n        id:\n          type: integer\n          description: Request identifier for matching responses.\n          example: 1\n        jsonrpc:\n          type: string\n          description: JSON-RPC protocol version.\n          example: '2.0'\n        method:\n          type: string\n          description: Alchemy method name to invoke.\n          example: alchemy_getAssetTransfers\n        params:\n          type: array\n          description: Parameters for the method call.\n          items: {}\n    AssetTransfer:\n      type: object\n      title: Asset Transfer\n      description: Represents a single asset transfer event on the blockchain.\n      properties:\n        blockNum:\n          type: string\n          description: Block number of the transfer in hexadecimal.\n          example: '0xfda53c'\n        hash:\n\
  \          type: string\n          description: Transaction hash of the transfer.\n          example: '0xabc123def456abc123def456abc123def456'\n        from:\n          type: string\n          description: Sender wallet address.\n          example: '0x0000000000000000000000000000000000000000'\n        to:\n          type: string\n          description: Recipient wallet address.\n          example: '0xd8da6bf26964af9d7eed9e03e53415d37aa96045'\n        value:\n          type: number\n          description: Transfer value in native units.\n          example: 1.0\n        asset:\n          type: string\n          description: Asset symbol (e.g., ETH, USDC, or NFT collection name).\n          example: ETH\n        category:\n          type: string\n          description: Transfer category (external, internal, erc20, erc721, erc1155).\n          enum:\n            - external\n            - internal\n            - erc20\n            - erc721\n            - erc1155\n          example: external\n\
  \        metadata:\n          $ref: '#/components/schemas/TransferMetadata'\n    TransferMetadata:\n      type: object\n      title: Transfer Metadata\n      description: Additional metadata for an asset transfer.\n      properties:\n        blockTimestamp:\n          type: string\n          format: date-time\n          description: ISO 8601 timestamp of the block.\n          example: '2026-04-19T10:00:00Z'\n    AssetTransfersResult:\n      type: object\n      title: Asset Transfers Result\n      description: Result payload containing the list of asset transfers.\n      properties:\n        transfers:\n          type: array\n          items:\n            $ref: '#/components/schemas/AssetTransfer'\n          description: List of asset transfer events matching the query.\n        pageKey:\n          type: string\n          description: Pagination key for retrieving the next page of results.\n          example: abc123nextpage\n    AssetTransfersResponse:\n      type: object\n      title:\
  \ Asset Transfers Response\n      description: JSON-RPC response for getAssetTransfers requests.\n      properties:\n        id:\n          type: integer\n          description: Matches the request ID.\n          example: 1\n        jsonrpc:\n          type: string\n          description: JSON-RPC version.\n          example: '2.0'\n        result:\n          $ref: '#/components/schemas/AssetTransfersResult'\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-transfers-api-openapi.yml
tags:
- Transfers
- NFTs
- Transaction History
---
