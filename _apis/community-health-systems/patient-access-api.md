---
aid: community-health-systems:patient-access-api
baseURL: https://api.chs.net/fhir/r4
description: FHIR R4 API published pursuant to the CMS Interoperability and Patient Access Final Rule (CMS-9115-F). Allows third-party applications, with the patient's authorization, to retrieve adjudicated claims and encounters (ExplanationOfBenefit), formulary and medication data (MedicationKnowledge), and clinical data (Patient and related resources). Authentication uses SMART-on-FHIR OAuth2 with patient/launch scopes.
humanURL: https://www.chs.net
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Community Health Systems Patient Access API
properties:
- type: Documentation
  url: https://www.chs.net
- type: CMSFinalRule
  url: https://www.cms.gov/regulations-and-guidance/guidance/interoperability/index
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/community-health-systems/refs/heads/main/openapi/chs-patient-access-api-openapi.yml
provider_name: Community Health Systems
provider_slug: community-health-systems
slug: patient-access-api
source_filename: chs-patient-access-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Community Health Systems Patient Access API\n  description: >-\n    Community Health Systems provides healthcare interoperability APIs\n    pursuant to the CMS Interoperability and Patient Access Final Rule\n    (CMS-9115-F). The Patient Access API allows third-party applications\n    to retrieve data concerning adjudicated claims, encounters, formulary\n    data, and clinical data using FHIR standards.\n  version: '2026-01-01'\n  contact:\n    name: Community Health Systems\n    url: https://www.chs.net\nexternalDocs:\n  description: CMS Interoperability Final Rule\n  url: https://www.cms.gov/regulations-and-guidance/guidance/interoperability/index\nservers:\n  - url: https://api.chs.net/fhir/r4\n    description: FHIR R4 Production Server\ntags:\n  - name: Claims\n    description: Adjudicated claims and encounter data\n  - name: Formulary\n    description: Formulary and medication data\n  - name: Patient\n    description: Patient demographic\
  \ and clinical data\n  - name: Practitioner\n    description: Provider information\nsecurity:\n  - oauth2: []\npaths:\n  /Patient:\n    get:\n      operationId: searchPatients\n      summary: Search patients\n      description: Search for patient records using FHIR Patient resource.\n      tags:\n        - Patient\n      parameters:\n        - name: family\n          in: query\n          schema:\n            type: string\n        - name: given\n          in: query\n          schema:\n            type: string\n        - name: birthdate\n          in: query\n          schema:\n            type: string\n            format: date\n      responses:\n        '200':\n          description: FHIR Bundle of Patient resources\n          content:\n            application/fhir+json:\n              schema:\n                $ref: '#/components/schemas/Bundle'\n        '401':\n          description: Unauthorized\n  /ExplanationOfBenefit:\n    get:\n      operationId: searchClaims\n      summary: Search\
  \ claims\n      description: Retrieve adjudicated claims data as ExplanationOfBenefit resources.\n      tags:\n        - Claims\n      parameters:\n        - name: patient\n          in: query\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: FHIR Bundle of ExplanationOfBenefit resources\n          content:\n            application/fhir+json:\n              schema:\n                $ref: '#/components/schemas/Bundle'\n  /MedicationKnowledge:\n    get:\n      operationId: searchFormulary\n      summary: Search formulary\n      description: Retrieve formulary and medication information.\n      tags:\n        - Formulary\n      responses:\n        '200':\n          description: FHIR Bundle of MedicationKnowledge resources\n          content:\n            application/fhir+json:\n              schema:\n                $ref: '#/components/schemas/Bundle'\n  /Practitioner:\n    get:\n      operationId: searchPractitioners\n\
  \      summary: Search practitioners\n      description: Search for provider directory information.\n      tags:\n        - Practitioner\n      parameters:\n        - name: name\n          in: query\n          schema:\n            type: string\n        - name: specialty\n          in: query\n          schema:\n            type: string\n      responses:\n        '200':\n          description: FHIR Bundle of Practitioner resources\n          content:\n            application/fhir+json:\n              schema:\n                $ref: '#/components/schemas/Bundle'\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: oauth2\n      flows:\n        authorizationCode:\n          authorizationUrl: https://api.chs.net/oauth2/authorize\n          tokenUrl: https://api.chs.net/oauth2/token\n          scopes:\n            patient/*.read: Read access to patient data\n            launch/patient: Patient launch context\n  schemas:\n    Bundle:\n      type: object\n      properties:\n        resourceType:\n\
  \          type: string\n          const: Bundle\n        type:\n          type: string\n        total:\n          type: integer\n        entry:\n          type: array\n          items:\n            type: object\n            properties:\n              resource:\n                type: object\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/community-health-systems/refs/heads/main/openapi/chs-patient-access-api-openapi.yml
tags:
- CMS-9115-F
- FHIR
- Healthcare
- Interoperability
- Patient Access
- SMART-on-FHIR
---
