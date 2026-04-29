---
aid: cloudflare:cloudflare-ip-addresses-api
baseURL: https://api.cloudflare.com
description: Provides the ability to manage IP addresses used across a Cloudflare account.
humanURL: https://developers.cloudflare.com/api/operations/ip-access-rules-for-a-user-list-ip-access-rules
image: ''
layout: api
name: Cloudflare IP Addresses API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudflare/refs/heads/main/openapi/cloudflare-ips--openapi-original.yml
- type: Documentation
  url: https://developers.cloudflare.com/api/operations/ip-access-rules-for-a-user-list-ip-access-rules
provider_name: Cloudflare
provider_slug: cloudflare
slug: cloudflare-ip-addresses-api
source_filename: cloudflare-ips--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ncomponents:\n  schemas:\n    addressing_api-response-collection:\n      allOf:\n        - $ref: '#/components/schemas/addressing_api-response-common'\n        - properties:\n            result:\n              type: array\n              nullable: true\n              items: {}\n            result_info:\n              $ref: '#/components/schemas/addressing_result_info'\n      type: object\ninfo:\n  title: 'Cloudflare ips/'\n  description: Needs description.\n  license:\n    name: BSD-3-Clause\n    url: https://opensource.org/licenses/BSD-3-Clause\n  version: 4.0.0\npaths:\n  /accounts/{account_id}/addressing/address_maps/{address_map_id}/ips/{ip_address}:\n    delete:\n      tags:\n        - Accounts\n      summary: Cloudflare Remove an IP from an Address Map\n      description: Remove an IP from a particular address map.\n      operationId: ip-address-management-address-maps-remove-an-ip-from-an-address-map\n      parameters:\n        - name: ip_address\n    \
  \      in: path\n          required: true\n          schema:\n            $ref: '#/components/schemas/addressing_ip_address'\n        - name: address_map_id\n          in: path\n          required: true\n          schema:\n            $ref: '#/components/schemas/addressing_identifier'\n        - name: account_id\n          in: path\n          required: true\n          schema:\n            $ref: '#/components/schemas/addressing_identifier'\n      requestBody:\n        required: true\n        content:\n          application/json: {}\n      responses:\n        '200':\n          description: Remove an IP from an Address Map response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/addressing_api-response-collection'\n        4XX:\n          description: Remove an IP from an Address Map response failure\n          content:\n            application/json:\n              schema:\n                allOf:\n                  - $ref:\
  \ '#/components/schemas/addressing_api-response-collection'\n                  - $ref: >-\n                      #/components/schemas/addressing_api-response-common-failure\n      security:\n        - api_email: []\n          api_key: []\n    put:\n      tags:\n        - Accounts\n      summary: Cloudflare Add an IP to an Address Map\n      description: >-\n        Add an IP from a prefix owned by the account to a particular address\n        map.\n      operationId: ip-address-management-address-maps-add-an-ip-to-an-address-map\n      parameters:\n        - name: ip_address\n          in: path\n          required: true\n          schema:\n            $ref: '#/components/schemas/addressing_ip_address'\n        - name: address_map_id\n          in: path\n          required: true\n          schema:\n            $ref: '#/components/schemas/addressing_identifier'\n        - name: account_id\n          in: path\n          required: true\n          schema:\n            $ref: '#/components/schemas/addressing_identifier'\n\
  \      requestBody:\n        required: true\n        content:\n          application/json: {}\n      responses:\n        '200':\n          description: Add an IP to an Address Map response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/addressing_api-response-collection'\n        4XX:\n          description: Add an IP to an Address Map response failure\n          content:\n            application/json:\n              schema:\n                allOf:\n                  - $ref: '#/components/schemas/addressing_api-response-collection'\n                  - $ref: >-\n                      #/components/schemas/addressing_api-response-common-failure\n      security:\n        - api_email: []\n          api_key: []\nsecurity:\n  - api_email: []\n    api_key: []\n  - api_token: []\n  - user_service_key: []\nservers:\n  - url: https://api.cloudflare.com/client/v4\n    description: Client API\ntags:\n  - name: Accounts\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudflare/refs/heads/main/openapi/cloudflare-ips--openapi-original.yml
tags:
- IP Addresses
---
