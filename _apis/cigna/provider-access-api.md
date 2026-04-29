---
aid: cigna:provider-access-api
baseURL: https://fhir.cigna.com/ProviderAccess/v1
description: FHIR API that allows in-network providers, with appropriate authorization, to retrieve a Cigna member's clinical and claims data to support care coordination. Implements the HL7 Da Vinci PDex Provider Access implementation guide and conforms to the CMS Interoperability and Prior Authorization final rule.
humanURL: https://developer.cigna.com/docs/service-apis
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cigna Provider Access API
properties:
- type: Documentation
  url: https://developer.cigna.com/docs/service-apis
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-provider-access-api-openapi.yml
provider_name: Cigna
provider_slug: cigna
slug: provider-access-api
source_filename: cigna-provider-access-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cigna Provider Access API\n  description: >-\n    FHIR API that allows in-network providers, with appropriate authorization,\n    to retrieve a Cigna member's clinical and claims data to support care\n    coordination. Implements the HL7 Da Vinci PDex Provider Access IG and the\n    CMS Interoperability and Prior Authorization final rule (CMS-0057-F).\n  version: '1.0'\n  contact:\n    name: Cigna Developer Support\n    url: https://developer.cigna.com/support\nexternalDocs:\n  description: Cigna Service APIs\n  url: https://developer.cigna.com/docs/service-apis\nservers:\n  - url: https://fhir.cigna.com/ProviderAccess/v1\n    description: Cigna Provider Access Production\ntags:\n  - name: Patient\n  - name: Coverage\n  - name: ExplanationOfBenefit\n  - name: Bulk Data\nsecurity:\n  - bulkData: []\npaths:\n  /metadata:\n    get:\n      operationId: getCapabilityStatement\n      summary: Retrieve the FHIR capability statement\n      tags: [Patient]\n\
  \      responses:\n        '200':\n          description: FHIR CapabilityStatement\n  /Group/{groupId}/$export:\n    get:\n      operationId: bulkExportGroup\n      summary: Initiate a bulk data export for a panel of attributed members\n      tags: [Bulk Data]\n      parameters:\n        - name: groupId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '202':\n          description: Bulk export accepted\n  /Patient/{patientId}/$everything:\n    get:\n      operationId: getPatientEverything\n      summary: Retrieve a complete clinical record for an attributed member\n      tags: [Patient]\n      parameters:\n        - name: patientId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: FHIR Bundle for the patient\ncomponents:\n  securitySchemes:\n    bulkData:\n      type: oauth2\n      description: SMART Backend Services authorization\
  \ for bulk FHIR export\n      flows:\n        clientCredentials:\n          tokenUrl: https://r-hi2.cigna.com/mga/sps/oauth/oauth20/token\n          scopes:\n            'system/*.read': System-level read access to FHIR resources\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-provider-access-api-openapi.yml
tags:
- CMS Interoperability
- FHIR
- Provider Access
---
