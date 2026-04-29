---
aid: cigna:drug-formulary-api
baseURL: https://fhir.cigna.com/DrugFormulary/v1
description: Public FHIR-based Drug Formulary API exposing Cigna's covered drug lists, formulary tiers, prior authorization requirements, step therapy, and quantity limits. Implements the HL7 Da Vinci PDex US Drug Formulary implementation guide required by the CMS Interoperability and Patient Access rule.
humanURL: https://developer.cigna.com/docs/service-apis
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cigna Drug Formulary API
properties:
- type: Documentation
  url: https://developer.cigna.com/docs/service-apis
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-drug-formulary-api-openapi.yml
provider_name: Cigna
provider_slug: cigna
slug: drug-formulary-api
source_filename: cigna-drug-formulary-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cigna Drug Formulary API\n  description: >-\n    Public FHIR-based Drug Formulary API exposing Cigna's covered drug lists,\n    formulary tiers, prior authorization, step therapy, and quantity limits.\n    Implements the HL7 Da Vinci PDex US Drug Formulary IG required by the\n    CMS Interoperability and Patient Access rule.\n  version: '1.0'\n  contact:\n    name: Cigna Developer Support\n    url: https://developer.cigna.com/support\nexternalDocs:\n  description: Cigna Service APIs\n  url: https://developer.cigna.com/docs/service-apis\nservers:\n  - url: https://fhir.cigna.com/DrugFormulary/v1\n    description: Cigna Drug Formulary Production\ntags:\n  - name: InsurancePlan\n  - name: MedicationKnowledge\n  - name: Basic\npaths:\n  /metadata:\n    get:\n      operationId: getCapabilityStatement\n      summary: Retrieve the FHIR capability statement\n      tags: [InsurancePlan]\n      responses:\n        '200':\n          description: FHIR CapabilityStatement\n\
  \  /InsurancePlan:\n    get:\n      operationId: searchFormularyPlan\n      summary: List drug formulary plans offered by Cigna\n      tags: [InsurancePlan]\n      parameters:\n        - name: status\n          in: query\n          schema:\n            type: string\n      responses:\n        '200':\n          description: FHIR Bundle of InsurancePlan formulary resources\n  /MedicationKnowledge:\n    get:\n      operationId: searchMedicationKnowledge\n      summary: Search covered drugs and formulary tier, step therapy, and prior auth\n      tags: [MedicationKnowledge]\n      parameters:\n        - name: code\n          in: query\n          schema:\n            type: string\n          description: RxNorm or NDC code\n        - name: DrugPlan\n          in: query\n          schema:\n            type: string\n          description: InsurancePlan id of the formulary\n      responses:\n        '200':\n          description: FHIR Bundle of MedicationKnowledge resources\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-drug-formulary-api-openapi.yml
tags:
- CMS Interoperability
- Drug Formulary
- FHIR
- Public API
---
