---
aid: country-io:country-io-data-api
baseURL: https://country.io
description: 'Country.io exposes six static JSON files under https://country.io. Each file is a flat object keyed by ISO 3166-1 alpha-2 country code and maps to a single reference value: country name, capital city, continent code, ISO3 code, dialing prefix, or currency code. The endpoints are open and unauthenticated.'
humanURL: https://country.io/data/
image: ''
layout: api
name: Country.io Data API
properties:
- type: Documentation
  url: https://country.io/data/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/country-io/refs/heads/main/openapi/country-io-data-openapi.yml
- type: Rules
  url: https://raw.githubusercontent.com/api-evangelist/country-io/refs/heads/main/rules/country-io-data-rules.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/country-io/refs/heads/main/capabilities/country-io-data-capabilities.yml
provider_name: Country.io
provider_slug: country-io
slug: country-io-data-api
source_filename: country-io-data-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Country.io Data API\n  description: >-\n    Country.io publishes a small set of static JSON files that map ISO 3166-1\n    alpha-2 country codes to common reference data (country names, capital\n    cities, continent codes, ISO 3166-1 alpha-3 codes, telephone dialing\n    codes, and currency codes). Each endpoint returns a flat JSON object\n    keyed by the two-letter country code.\n  version: '1.0'\n  contact:\n    name: Country.io\n    url: https://country.io/contact/\n  license:\n    name: Country.io Data\n    url: https://country.io/\nexternalDocs:\n  description: Country.io Data Index\n  url: https://country.io/data/\nservers:\n  - url: https://country.io\n    description: Country.io static JSON host\ntags:\n  - name: Names\n    description: Country names by ISO2 code.\n  - name: Capitals\n    description: Capital cities by ISO2 code.\n  - name: Continents\n    description: Continent codes by ISO2 country code.\n  - name: ISO3\n    description:\
  \ ISO 3166-1 alpha-3 codes by ISO2 country code.\n  - name: Phone\n    description: International dialing codes by ISO2 country code.\n  - name: Currency\n    description: Currency codes by ISO2 country code.\npaths:\n  /names.json:\n    get:\n      operationId: getCountryNames\n      summary: Get country names keyed by ISO2 code\n      tags:\n        - Names\n      responses:\n        '200':\n          description: A JSON object mapping ISO2 country codes to country names.\n          content:\n            application/json:\n              schema:\n                type: object\n                additionalProperties:\n                  type: string\n                example:\n                  US: United States\n                  GB: United Kingdom\n                  FR: France\n  /capital.json:\n    get:\n      operationId: getCapitals\n      summary: Get capital cities keyed by ISO2 code\n      tags:\n        - Capitals\n      responses:\n        '200':\n          description: A JSON object\
  \ mapping ISO2 country codes to capital city names.\n          content:\n            application/json:\n              schema:\n                type: object\n                additionalProperties:\n                  type: string\n                example:\n                  US: Washington\n                  GB: London\n                  FR: Paris\n  /continent.json:\n    get:\n      operationId: getContinents\n      summary: Get continent codes keyed by ISO2 country code\n      tags:\n        - Continents\n      responses:\n        '200':\n          description: A JSON object mapping ISO2 country codes to two-letter continent codes (AF, AN, AS, EU, NA, OC, SA).\n          content:\n            application/json:\n              schema:\n                type: object\n                additionalProperties:\n                  type: string\n                example:\n                  US: NA\n                  GB: EU\n                  JP: AS\n  /iso3.json:\n    get:\n      operationId: getIso3\n\
  \      summary: Get ISO 3166-1 alpha-3 codes keyed by ISO2 code\n      tags:\n        - ISO3\n      responses:\n        '200':\n          description: A JSON object mapping ISO2 country codes to ISO 3166-1 alpha-3 codes.\n          content:\n            application/json:\n              schema:\n                type: object\n                additionalProperties:\n                  type: string\n                example:\n                  US: USA\n                  GB: GBR\n                  FR: FRA\n  /phone.json:\n    get:\n      operationId: getPhoneCodes\n      summary: Get international dialing codes keyed by ISO2 country code\n      tags:\n        - Phone\n      responses:\n        '200':\n          description: A JSON object mapping ISO2 country codes to international dialing prefixes.\n          content:\n            application/json:\n              schema:\n                type: object\n                additionalProperties:\n                  type: string\n                example:\n\
  \                  US: '1'\n                  GB: '44'\n                  FR: '33'\n  /currency.json:\n    get:\n      operationId: getCurrencyCodes\n      summary: Get currency codes keyed by ISO2 country code\n      tags:\n        - Currency\n      responses:\n        '200':\n          description: A JSON object mapping ISO2 country codes to ISO 4217 currency codes.\n          content:\n            application/json:\n              schema:\n                type: object\n                additionalProperties:\n                  type: string\n                example:\n                  US: USD\n                  GB: GBP\n                  FR: EUR\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/country-io/refs/heads/main/openapi/country-io-data-openapi.yml
tags:
- Capitals
- Countries
- Currencies
- ISO 3166
- Open Data
- Phone Codes
- Reference Data
---
