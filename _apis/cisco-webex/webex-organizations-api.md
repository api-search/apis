---
aid: cisco-webex:webex-organizations-api
baseURL: https://webexapis.com/v1
description: Retrieve organization details for Webex administration. Provides access to organization-level information and settings, available only to organization administrators.
humanURL: https://developer.webex.com/docs/api/v1/organizations
image: https://www.webex.com/content/dam/wbx/us/images/webex-logo.svg
layout: api
name: Webex Organizations API
properties:
- type: Documentation
  url: https://developer.webex.com/docs/api/v1/organizations
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-organizations-openapi.yml
provider_name: Cisco Webex
provider_slug: cisco-webex
slug: webex-organizations-api
source_filename: cisco-webex-organizations-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cisco Webex Organizations API\n  description: >-\n    Retrieve organization details for Webex administration. Provides access\n    to organization-level information and settings, available only to\n    organization administrators.\n  version: 1.0.0\n  contact:\n    name: Cisco Webex Developer Support\n    url: https://developer.webex.com/support\n  license:\n    name: Cisco Webex API Terms of Service\n    url: https://developer.webex.com/terms-of-service\nservers:\n  - url: https://webexapis.com/v1\n    description: Webex Production API\nsecurity:\n  - bearerAuth: []\ntags:\n  - name: Organizations\n    description: Operations for managing organizations\npaths:\n  /organizations:\n    get:\n      operationId: listOrganizations\n      summary: Cisco Webex List Organizations\n      description: >-\n        Lists organizations associated with the authenticated user.\n        Typically returns a single organization unless the user belongs to\n  \
  \      multiple organizations.\n      tags:\n        - Organizations\n      responses:\n        '200':\n          description: Successful response with list of organizations.\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  items:\n                    type: array\n                    items:\n                      $ref: '#/components/schemas/Organization'\n        '401':\n          description: Unauthorized - invalid or missing access token.\n  /organizations/{orgId}:\n    get:\n      operationId: getOrganizationDetails\n      summary: Cisco Webex Get Organization Details\n      description: >-\n        Shows details for an organization by ID. Returns organization name,\n        creation date, and other metadata. Only available to organization\n        administrators.\n      tags:\n        - Organizations\n      parameters:\n        - name: orgId\n          in: path\n          required:\
  \ true\n          description: Unique identifier for the organization.\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Successful response with organization details.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Organization'\n        '404':\n          description: Organization not found.\n    delete:\n      operationId: deleteOrganization\n      summary: Cisco Webex Delete Organization\n      description: >-\n        Deletes an organization by ID. This action permanently removes the\n        organization and all associated data. Only available to full\n        administrators.\n      tags:\n        - Organizations\n      parameters:\n        - name: orgId\n          in: path\n          required: true\n          description: Unique identifier for the organization.\n          schema:\n            type: string\n      responses:\n        '204':\n          description:\
  \ Organization deleted successfully.\n        '404':\n          description: Organization not found.\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      description: >-\n        Webex API access token. Obtain via OAuth 2.0 authorization flow.\n        Requires spark-admin:organizations_read scope.\n  schemas:\n    Organization:\n      type: object\n      properties:\n        id:\n          type: string\n          description: Unique identifier for the organization.\n        displayName:\n          type: string\n          description: Full name of the organization.\n        created:\n          type: string\n          format: date-time\n          description: Date and time the organization was created.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-organizations-openapi.yml
tags:
- Administration
- Enterprise
- Management
- Organizations
- Settings
---
