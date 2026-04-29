---
aid: charmhealth:fhir-api
baseURL: https://ehr2.charmtracker.com/api/ehr/v2/fhir
description: CharmHealth EHR FHIR API conforms to FHIR R4 (4.0.1) and the US Core STU 3.1.1 Implementation Guide. It supports 30+ FHIR resources covering clinical (AllergyIntolerance, Condition, Procedure, Immunization, MedicationRequest), care coordination (CarePlan, CareTeam, Goal, Encounter), administrative (Patient, Practitioner, Organization, Location, Appointment), diagnostic (DiagnosticReport, Observation), and documentation resources (DocumentReference, QuestionnaireResponse, Provenance). Authentication uses SMART on FHIR with OAuth 2.0 authorization code flow, PKCE for public clients, and JWT-assertion backend services authorization for system access.
humanURL: https://www.charmhealth.com/resources/fhir/index.html
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CharmHealth FHIR API
properties:
- type: Documentation
  url: https://www.charmhealth.com/resources/fhir/index.html
- type: Authentication
  url: https://www.charmhealth.com/resources/fhir/authorization.html
- type: SMARTOnFHIR
  url: https://www.charmhealth.com/resources/fhir/smart-on-fhir.html
- type: BulkExport
  url: https://www.charmhealth.com/resources/fhir/bulk-data.html
- type: USCore
  url: https://www.hl7.org/fhir/us/core/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/charmhealth/refs/heads/main/openapi/charmhealth-fhir-api-openapi.yml
- type: Spectral
  url: https://raw.githubusercontent.com/api-evangelist/charmhealth/refs/heads/main/spectral/charmhealth-spectral.yml
provider_name: CharmHealth
provider_slug: charmhealth
slug: fhir-api
source_yaml: "aid: charmhealth:fhir-api\nname: CharmHealth FHIR API\ndescription: CharmHealth EHR FHIR API conforms to FHIR R4 (4.0.1) and the US Core STU 3.1.1 Implementation\n  Guide. It supports 30+ FHIR resources covering clinical (AllergyIntolerance, Condition, Procedure, Immunization,\n  MedicationRequest), care coordination (CarePlan, CareTeam, Goal, Encounter), administrative (Patient,\n  Practitioner, Organization, Location, Appointment), diagnostic (DiagnosticReport, Observation), and\n  documentation resources (DocumentReference, QuestionnaireResponse, Provenance). Authentication uses\n  SMART on FHIR with OAuth 2.0 authorization code flow, PKCE for public clients, and JWT-assertion backend\n  services authorization for system access.\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://www.charmhealth.com/resources/fhir/index.html\nbaseURL: https://ehr2.charmtracker.com/api/ehr/v2/fhir\ntags:\n- FHIR\n- HL7\n- Healthcare\n- SMART\
  \ on FHIR\n- US Core\nproperties:\n- type: Documentation\n  url: https://www.charmhealth.com/resources/fhir/index.html\n- type: Authentication\n  url: https://www.charmhealth.com/resources/fhir/authorization.html\n- type: SMARTOnFHIR\n  url: https://www.charmhealth.com/resources/fhir/smart-on-fhir.html\n- type: BulkExport\n  url: https://www.charmhealth.com/resources/fhir/bulk-data.html\n- type: USCore\n  url: https://www.hl7.org/fhir/us/core/\n- type: OpenAPI\n  url: openapi/charmhealth-fhir-api-openapi.yml\n- type: Spectral\n  url: spectral/charmhealth-spectral.yml\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/charmhealth/refs/heads/main/apis.yml
tags:
- FHIR
- HL7
- Healthcare
- SMART on FHIR
- US Core
---
