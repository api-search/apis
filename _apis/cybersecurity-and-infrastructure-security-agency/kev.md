---
aid: cybersecurity-and-infrastructure-security-agency:kev
baseURL: https://www.cisa.gov
description: The KEV catalog is CISA's authoritative list of vulnerabilities actively exploited in the wild. The full catalog is published as JSON and CSV at cisa.gov/sites/default/files/feeds, mirrored on GitHub at cisagov/kev-data, and accompanied by a versioned JSON Schema. Federal civilian agencies must remediate KEV entries by the per-entry dueDate under BOD 22-01.
humanURL: https://www.cisa.gov/known-exploited-vulnerabilities-catalog
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CISA Known Exploited Vulnerabilities (KEV) Catalog
properties:
- type: Documentation
  url: https://www.cisa.gov/known-exploited-vulnerabilities-catalog
- type: JSONFeed
  url: https://www.cisa.gov/sites/default/files/feeds/known_exploited_vulnerabilities.json
- type: CSVFeed
  url: https://www.cisa.gov/sites/default/files/feeds/known_exploited_vulnerabilities.csv
- type: JSONSchema
  url: https://www.cisa.gov/sites/default/files/feeds/known_exploited_vulnerabilities_schema.json
- type: GitHubMirror
  url: https://github.com/cisagov/kev-data
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cybersecurity-and-infrastructure-security-agency/refs/heads/main/openapi/cisa-kev-openapi.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/cybersecurity-and-infrastructure-security-agency/refs/heads/main/capabilities/cisa-kev-capabilities.yml
- type: Rules
  url: https://raw.githubusercontent.com/api-evangelist/cybersecurity-and-infrastructure-security-agency/refs/heads/main/rules/cisa-kev-rules.yml
provider_name: Cybersecurity and Infrastructure Security Agency
provider_slug: cybersecurity-and-infrastructure-security-agency
slug: kev
source_filename: cisa-kev-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: CISA Known Exploited Vulnerabilities (KEV) Catalog API\n  description: >-\n    The CISA Known Exploited Vulnerabilities (KEV) Catalog is the\n    authoritative source of vulnerabilities that have been actively\n    exploited in the wild. CISA publishes the catalog as a\n    machine-readable JSON feed (and CSV) updated within minutes of\n    catalog changes during U.S. business hours. Federal civilian\n    agencies are required by Binding Operational Directive 22-01 to\n    remediate KEV-listed vulnerabilities by the dueDate provided in\n    each entry. This OpenAPI describes the unauthenticated public\n    JSON feed and its mirror on GitHub.\n  version: '1.0'\n  contact:\n    name: CISA\n    url: https://www.cisa.gov/known-exploited-vulnerabilities-catalog\nservers:\n  - url: https://www.cisa.gov\n    description: Canonical CISA-hosted feed\n  - url: https://raw.githubusercontent.com/cisagov/kev-data/develop\n    description: GitHub mirror maintained\
  \ by cisagov/kev-data\ntags:\n  - name: KEV\n    description: Known Exploited Vulnerabilities catalog feed\n  - name: Schema\n    description: JSON Schema for the KEV catalog\npaths:\n  /sites/default/files/feeds/known_exploited_vulnerabilities.json:\n    get:\n      tags:\n        - KEV\n      summary: Get the KEV catalog as JSON\n      description: >-\n        Returns the full Known Exploited Vulnerabilities catalog as a\n        JSON document. This endpoint is unauthenticated and intended\n        for public consumption by vulnerability management programs.\n      operationId: getKevJson\n      responses:\n        '200':\n          description: KEV catalog JSON\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/KevCatalog'\n  /sites/default/files/feeds/known_exploited_vulnerabilities.csv:\n    get:\n      tags:\n        - KEV\n      summary: Get the KEV catalog as CSV\n      description: Returns the same KEV data as\
  \ a CSV file.\n      operationId: getKevCsv\n      responses:\n        '200':\n          description: KEV catalog CSV\n          content:\n            text/csv:\n              schema:\n                type: string\n  /sites/default/files/feeds/known_exploited_vulnerabilities_schema.json:\n    get:\n      tags:\n        - Schema\n      summary: Get the JSON Schema for the KEV catalog\n      description: Returns the JSON Schema document used to validate the KEV JSON feed.\n      operationId: getKevJsonSchema\n      responses:\n        '200':\n          description: KEV JSON Schema\n          content:\n            application/json:\n              schema:\n                type: object\ncomponents:\n  schemas:\n    KevCatalog:\n      type: object\n      required:\n        - title\n        - catalogVersion\n        - dateReleased\n        - count\n        - vulnerabilities\n      properties:\n        title:\n          type: string\n          example: CISA Catalog of Known Exploited Vulnerabilities\n\
  \        catalogVersion:\n          type: string\n          description: ISO-style catalog version (YYYY.MM.DD).\n        dateReleased:\n          type: string\n          format: date-time\n        count:\n          type: integer\n          description: Total number of vulnerability entries.\n        vulnerabilities:\n          type: array\n          items:\n            $ref: '#/components/schemas/KevVulnerability'\n    KevVulnerability:\n      type: object\n      required:\n        - cveID\n        - vendorProject\n        - product\n        - vulnerabilityName\n        - dateAdded\n        - shortDescription\n        - requiredAction\n        - dueDate\n        - knownRansomwareCampaignUse\n      properties:\n        cveID:\n          type: string\n          example: CVE-2024-1708\n        vendorProject:\n          type: string\n        product:\n          type: string\n        vulnerabilityName:\n          type: string\n        dateAdded:\n          type: string\n          format: date\n\
  \        shortDescription:\n          type: string\n        requiredAction:\n          type: string\n        dueDate:\n          type: string\n          format: date\n        knownRansomwareCampaignUse:\n          type: string\n          enum: [Known, Unknown]\n        notes:\n          type: string\n        cwes:\n          type: array\n          items:\n            type: string\n            example: CWE-79\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cybersecurity-and-infrastructure-security-agency/refs/heads/main/openapi/cisa-kev-openapi.yml
tags:
- BOD 22-01
- CVE
- CWE
- Federal Government
- JSON Feed
- KEV
- Vulnerability Management
---
