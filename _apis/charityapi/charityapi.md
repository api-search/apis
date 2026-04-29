---
aid: charityapi:charityapi
baseURL: https://api.charityapi.org/api
description: CharityAPI provides REST endpoints for looking up US nonprofit organizations by EIN, performing public charity 501c3 verification checks, and powering autocomplete search across the IRS Business Master File. The API supports donation platforms, fundraising tools, and compliance workflows that need authoritative tax-status data.
humanURL: https://charityapi.org/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CharityAPI
properties:
- type: Documentation
  url: https://docs.charityapi.org/
- type: GettingStarted
  url: https://docs.charityapi.org/main
- type: Authentication
  url: https://docs.charityapi.org/authentication
- type: Organizations
  url: https://docs.charityapi.org/organizations
- type: Pricing
  url: https://www.charityapi.org/pricing
- type: SignUp
  url: https://www.charityapi.org/get-started
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/charityapi/refs/heads/main/openapi/charityapi-openapi.yml
- type: Spectral
  url: https://raw.githubusercontent.com/api-evangelist/charityapi/refs/heads/main/spectral/charityapi-spectral.yml
- type: NaftikoCapabilities
  url: https://raw.githubusercontent.com/api-evangelist/charityapi/refs/heads/main/naftiko/charityapi-capabilities.yml
provider_name: CharityAPI
provider_slug: charityapi
slug: charityapi
source_filename: charityapi-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CharityAPI\n  description: >-\n    REST API providing access to US nonprofit and charity data sourced from\n    IRS filings. Supports lookup of organizations by EIN, public charity (501c3)\n    verification checks, and name-based autocomplete for donation, fundraising,\n    and compliance workflows.\n  version: '1.0'\n  contact:\n    name: CharityAPI Support\n    url: https://www.charityapi.org/contact\n  termsOfService: https://www.charityapi.org/terms\nexternalDocs:\n  description: CharityAPI Documentation\n  url: https://docs.charityapi.org/\nservers:\n  - url: https://api.charityapi.org/api\n    description: CharityAPI Production\ntags:\n  - name: Organizations\n    description: Look up US nonprofit organization records by EIN\n  - name: Public Charity Check\n    description: Verify whether an EIN is a tax-deductible public charity\n  - name: Autocomplete\n    description: Typeahead search across nonprofit organization names\nsecurity:\n\
  \  - apiKeyAuth: []\npaths:\n  /organizations/{ein}:\n    get:\n      operationId: getOrganizationByEin\n      summary: Get organization by EIN\n      description: >-\n        Retrieve a single nonprofit organization record from the IRS Business\n        Master File by Employer Identification Number. Returns charities,\n        political organizations, insurance organizations, and other nonprofits.\n      tags:\n        - Organizations\n      parameters:\n        - name: ein\n          in: path\n          required: true\n          description: Employer Identification Number for the organization.\n          schema:\n            type: string\n            pattern: '^[0-9]{9}$'\n      responses:\n        '200':\n          description: Organization record\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Organization'\n        '404':\n          description: Organization not found\n        '401':\n          description: Missing\
  \ or invalid API key\n        '429':\n          description: Rate limit exceeded\n  /organizations/autocomplete/{term}:\n    get:\n      operationId: autocompleteOrganizations\n      summary: Autocomplete organization names\n      description: >-\n        Search the IRS Business Master File for organizations whose name\n        matches the supplied term. Designed for typeahead UIs and supports\n        typo tolerance. Available to paying accounts only.\n      tags:\n        - Autocomplete\n      parameters:\n        - name: term\n          in: path\n          required: true\n          description: Partial organization name to match.\n          schema:\n            type: string\n            minLength: 2\n      responses:\n        '200':\n          description: Matching organization suggestions\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/Organization'\n      \
  \  '401':\n          description: Missing or invalid API key\n        '402':\n          description: Endpoint requires a paid subscription\n        '429':\n          description: Rate limit exceeded\n  /public_charity_check/{ein}:\n    get:\n      operationId: publicCharityCheck\n      summary: Check public charity status\n      description: >-\n        Returns a boolean indicating whether the supplied EIN belongs to an\n        IRS public charity, and therefore qualifies as a 501c3 with\n        tax-deductible donation status.\n      tags:\n        - Public Charity Check\n      parameters:\n        - name: ein\n          in: path\n          required: true\n          description: Employer Identification Number to verify.\n          schema:\n            type: string\n            pattern: '^[0-9]{9}$'\n      responses:\n        '200':\n          description: Public charity check result\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/PublicCharityCheck'\n\
  \        '401':\n          description: Missing or invalid API key\n        '429':\n          description: Rate limit exceeded\ncomponents:\n  securitySchemes:\n    apiKeyAuth:\n      type: apiKey\n      in: header\n      name: apikey\n      description: API key issued by CharityAPI, sent in the apikey request header.\n  schemas:\n    Organization:\n      type: object\n      description: A nonprofit organization record sourced from the IRS Business Master File.\n      properties:\n        ein:\n          type: string\n          description: Employer Identification Number.\n        name:\n          type: string\n          description: Legal organization name.\n        ico:\n          type: string\n          description: In Care Of name.\n        street:\n          type: string\n        city:\n          type: string\n        state:\n          type: string\n        zip:\n          type: string\n        group:\n          type: string\n        subsection:\n          type: string\n        affiliation:\n\
  \          type: string\n        classification:\n          type: string\n        ruling:\n          type: string\n        deductibility:\n          type: string\n        foundation:\n          type: string\n        activity:\n          type: string\n        organization:\n          type: string\n        status:\n          type: string\n        tax_period:\n          type: string\n        asset_cd:\n          type: string\n        income_cd:\n          type: string\n        filing_req_cd:\n          type: string\n        pf_filing_req_cd:\n          type: string\n        acct_pd:\n          type: string\n        asset_amt:\n          type: integer\n        income_amt:\n          type: integer\n        revenue_amt:\n          type: integer\n        ntee_cd:\n          type: string\n          description: National Taxonomy of Exempt Entities code.\n        sort_name:\n          type: string\n    PublicCharityCheck:\n      type: object\n      description: Result of a 501c3 public charity\
  \ verification.\n      properties:\n        ein:\n          type: string\n        public_charity:\n          type: boolean\n          description: True when the EIN is registered as an IRS public charity.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/charityapi/refs/heads/main/openapi/charityapi-openapi.yml
tags:
- 501c3
- Charities
- EIN
- IRS
- Non-Profits
- Verification
---
