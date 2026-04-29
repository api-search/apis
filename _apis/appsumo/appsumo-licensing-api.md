---
aid: appsumo:appsumo-licensing-api
baseURL: https://appsumo.com
description: The AppSumo Licensing API (v2) enables software partners selling products on the AppSumo marketplace to programmatically manage licenses for their customers. Partners can retrieve license details, validate activations, and manage license states via REST API endpoints authenticated with an API key. The API also supports OAuth integration, allowing customers to connect their AppSumo purchases directly to partner applications.
humanURL: https://docs.licensing.appsumo.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: AppSumo Licensing API
properties:
- type: Documentation
  url: https://docs.licensing.appsumo.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/openapi/appsumo-licensing-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/json-schema/license-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/json-structure/license-structure.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/examples/license-example.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/json-ld/appsumo-context.jsonld
- type: SpectralRules
  url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/rules/appsumo-spectral-rules.yml
- type: NaftikoCapability
  url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/capabilities/shared/appsumo-api.yaml
- type: NaftikoCapability
  url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/capabilities/license-management.yaml
- type: Vocabulary
  url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/vocabulary/appsumo-vocabulary.yaml
provider_name: AppSumo
provider_slug: appsumo
slug: appsumo-licensing-api
source_filename: appsumo-licensing-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: AppSumo Licensing API\n  description: >-\n    The AppSumo Licensing API enables software partners selling on the AppSumo\n    marketplace to programmatically manage licenses for their customers. Partners\n    can retrieve license details, validate activations, and manage license states\n    via REST endpoints authenticated with an API key.\n  version: 2.0.0\n  contact:\n    name: AppSumo Partner Support\n    url: https://docs.licensing.appsumo.com\n  license:\n    name: Proprietary\nservers:\n  - url: https://appsumo.com/api/v2\n    description: AppSumo Licensing API v2\nsecurity:\n  - apiKeyAuth: []\ntags:\n  - name: Licenses\n    description: License management for AppSumo marketplace purchases\n  - name: Profile\n    description: Partner profile management\npaths:\n  /licenses/{licenseKey}:\n    get:\n      operationId: getLicense\n      summary: AppSumo - Get License\n      description: Returns details for a specific license key purchased\
  \ through AppSumo\n      tags:\n        - Licenses\n      parameters:\n        - name: licenseKey\n          in: path\n          required: true\n          description: The license key to retrieve information for\n          schema:\n            type: string\n      responses:\n        '200':\n          description: License details\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/License'\n              examples:\n                GetLicenseExample:\n                  x-microcks-default: true\n                  summary: Example license detail response\n                  value:\n                    licenseKey: APPSUMO-XXXXXXXX-XXXXXXXX-XXXXXXXX\n                    productSlug: my-saas-tool\n                    status: active\n                    tier: Tier 2\n                    activatedAt: \"2026-03-01T10:00:00Z\"\n                    userId: user-12345\n                    email: customer@example.com\n        '404':\n\
  \          description: License not found\n        '401':\n          description: Unauthorized - invalid or missing API key\n  /licenses/{licenseKey}/activate:\n    post:\n      operationId: activateLicense\n      summary: AppSumo - Activate License\n      description: Activates a license key for a customer within the partner application\n      tags:\n        - Licenses\n      parameters:\n        - name: licenseKey\n          in: path\n          required: true\n          description: The license key to activate\n          schema:\n            type: string\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                userId:\n                  type: string\n                  description: Partner application user ID to bind the license to\n            examples:\n              ActivateLicenseExample:\n                x-microcks-default: true\n                summary:\
  \ Example license activation request\n                value:\n                  userId: partner-user-001\n      responses:\n        '200':\n          description: License activated successfully\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/License'\n        '400':\n          description: Invalid request or license already activated\n        '404':\n          description: License not found\n        '401':\n          description: Unauthorized - invalid or missing API key\n  /licenses/{licenseKey}/deactivate:\n    post:\n      operationId: deactivateLicense\n      summary: AppSumo - Deactivate License\n      description: Deactivates an active license key within the partner application\n      tags:\n        - Licenses\n      parameters:\n        - name: licenseKey\n          in: path\n          required: true\n          description: The license key to deactivate\n          schema:\n            type: string\n      responses:\n\
  \        '200':\n          description: License deactivated successfully\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/License'\n        '404':\n          description: License not found\n        '401':\n          description: Unauthorized - invalid or missing API key\n  /profile:\n    get:\n      operationId: getPartnerProfile\n      summary: AppSumo - Get Partner Profile\n      description: Returns the partner profile information for the authenticated API key\n      tags:\n        - Profile\n      responses:\n        '200':\n          description: Partner profile\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/PartnerProfile'\n              examples:\n                GetProfileExample:\n                  x-microcks-default: true\n                  summary: Example partner profile response\n                  value:\n                    partnerId:\
  \ partner-001\n                    productSlug: my-saas-tool\n                    productName: My SaaS Tool\n                    webhookUrl: https://myapp.com/webhooks/appsumo\n        '401':\n          description: Unauthorized - invalid or missing API key\ncomponents:\n  securitySchemes:\n    apiKeyAuth:\n      type: apiKey\n      in: header\n      name: X-AppSumo-API-Key\n  schemas:\n    License:\n      title: License\n      description: An AppSumo software license\n      type: object\n      properties:\n        licenseKey:\n          type: string\n          description: Unique license key for activation\n        productSlug:\n          type: string\n          description: AppSumo product slug identifier\n        status:\n          type: string\n          enum: [active, inactive, refunded]\n          description: Current license status\n        tier:\n          type: string\n          description: License tier level\n        activatedAt:\n          type: string\n          format: date-time\n\
  \          description: License activation timestamp\n        userId:\n          type: string\n          description: AppSumo user who purchased the license\n        email:\n          type: string\n          format: email\n          description: Purchaser email address\n    PartnerProfile:\n      title: PartnerProfile\n      description: AppSumo marketplace partner profile\n      type: object\n      properties:\n        partnerId:\n          type: string\n          description: Unique partner identifier\n        productSlug:\n          type: string\n          description: Partner product slug on AppSumo\n        productName:\n          type: string\n          description: Partner product display name\n        webhookUrl:\n          type: string\n          description: Webhook URL for license event notifications\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/appsumo/refs/heads/main/openapi/appsumo-licensing-openapi.yaml
tags:
- Licensing
- Marketplace
- SaaS
- Software Deals
---
