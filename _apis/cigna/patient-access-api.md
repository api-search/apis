---
aid: cigna:patient-access-api
baseURL: https://fhir.cigna.com/PatientAccess/v1
description: FHIR R4 API that allows authorized third-party applications to access a Cigna member's claims, encounters, clinical data, coverage, and pharmacy information after the member completes SMART on FHIR authorization. Conforms to the CMS Interoperability and Patient Access final rule and the HL7 Da Vinci PDex implementation guide.
humanURL: https://developer.cigna.com/docs/service-apis/patient-access/implementation-guide
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cigna Patient Access API
properties:
- type: Documentation
  url: https://developer.cigna.com/docs/service-apis/patient-access/implementation-guide
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-patient-access-api-openapi.yml
provider_name: Cigna
provider_slug: cigna
slug: patient-access-api
source_filename: cigna-patient-access-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cigna Patient Access API\n  description: >-\n    FHIR R4 API exposing Cigna member health information including coverage,\n    claims, encounters, observations, conditions, medications, and immunizations\n    for authorized third-party applications acting on behalf of a member. Implements\n    the HL7 Da Vinci PDex implementation guide and the CMS Interoperability and\n    Patient Access final rule (CMS-9115-F).\n  version: '1.0'\n  contact:\n    name: Cigna Developer Support\n    url: https://developer.cigna.com/support\nexternalDocs:\n  description: Patient Access Implementation Guide\n  url: https://developer.cigna.com/docs/service-apis/patient-access/implementation-guide\nservers:\n  - url: https://fhir.cigna.com/PatientAccess/v1\n    description: Cigna Patient Access Production\n  - url: https://fhir.cigna.com/PatientAccess/v1-devportal\n    description: Developer Sandbox\ntags:\n  - name: Patient\n  - name: Coverage\n  - name: ExplanationOfBenefit\n\
  \  - name: Encounter\n  - name: Observation\n  - name: Condition\n  - name: MedicationRequest\nsecurity:\n  - smartOnFhir: []\npaths:\n  /metadata:\n    get:\n      operationId: getCapabilityStatement\n      summary: Retrieve the FHIR capability statement\n      tags: [Patient]\n      responses:\n        '200':\n          description: FHIR CapabilityStatement\n  /$userinfo:\n    get:\n      operationId: getUserInfo\n      summary: Retrieve the authenticated member's identifier\n      tags: [Patient]\n      responses:\n        '200':\n          description: User info with member identifier\n  /Patient:\n    get:\n      operationId: searchPatient\n      summary: Search the authenticated member's Patient resource\n      tags: [Patient]\n      parameters:\n        - name: _id\n          in: query\n          schema:\n            type: string\n      responses:\n        '200':\n          description: FHIR Bundle of Patient resources\n  /Coverage:\n    get:\n      operationId: searchCoverage\n\
  \      summary: Retrieve coverage records for the authenticated member\n      tags: [Coverage]\n      parameters:\n        - name: patient\n          in: query\n          schema:\n            type: string\n      responses:\n        '200':\n          description: FHIR Bundle of Coverage resources\n  /ExplanationOfBenefit:\n    get:\n      operationId: searchExplanationOfBenefit\n      summary: Retrieve EOB claims data for the authenticated member\n      tags: [ExplanationOfBenefit]\n      parameters:\n        - name: patient\n          in: query\n          schema:\n            type: string\n      responses:\n        '200':\n          description: FHIR Bundle of ExplanationOfBenefit resources\n  /Encounter:\n    get:\n      operationId: searchEncounter\n      summary: Retrieve encounter records for the authenticated member\n      tags: [Encounter]\n      responses:\n        '200':\n          description: FHIR Bundle of Encounter resources\n  /Observation:\n    get:\n      operationId: searchObservation\n\
  \      summary: Retrieve clinical observations for the authenticated member\n      tags: [Observation]\n      responses:\n        '200':\n          description: FHIR Bundle of Observation resources\n  /Condition:\n    get:\n      operationId: searchCondition\n      summary: Retrieve condition records for the authenticated member\n      tags: [Condition]\n      responses:\n        '200':\n          description: FHIR Bundle of Condition resources\n  /MedicationRequest:\n    get:\n      operationId: searchMedicationRequest\n      summary: Retrieve medication requests for the authenticated member\n      tags: [MedicationRequest]\n      responses:\n        '200':\n          description: FHIR Bundle of MedicationRequest resources\ncomponents:\n  securitySchemes:\n    smartOnFhir:\n      type: oauth2\n      description: SMART on FHIR authorization with patient-context launch\n      flows:\n        authorizationCode:\n          authorizationUrl: https://r-hi2.cigna.com/mga/sps/oauth/oauth20/authorize\n\
  \          tokenUrl: https://r-hi2.cigna.com/mga/sps/oauth/oauth20/token\n          scopes:\n            'patient/*.read': Read all patient-context FHIR resources\n            'launch/patient': Launch in patient context\n            'offline_access': Receive a refresh token\n            'openid': Receive an OpenID Connect identity token\n            'fhirUser': Receive the user resource identifier\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-patient-access-api-openapi.yml
tags:
- CMS Interoperability
- FHIR
- Patient Access
- SMART on FHIR
---
