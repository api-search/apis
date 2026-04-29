---
aid: cigna:provider-directory-api
baseURL: https://fhir.cigna.com/ProviderDirectory/v1
description: Public FHIR-based Provider Directory API listing Cigna's contracted network providers, organizations, locations, healthcare services, and practitioner roles. Conforms to the HL7 Da Vinci PDex Plan Network implementation guide and the CMS Provider Directory API requirements.
humanURL: https://developer.cigna.com/docs/service-apis/provider-directory/implementation-guide
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cigna Provider Directory API
properties:
- type: Documentation
  url: https://developer.cigna.com/docs/service-apis/provider-directory/implementation-guide
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-provider-directory-api-openapi.yml
provider_name: Cigna
provider_slug: cigna
slug: provider-directory-api
source_filename: cigna-provider-directory-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cigna Provider Directory API\n  description: >-\n    Public FHIR-based Provider Directory API listing Cigna's contracted\n    practitioners, organizations, locations, healthcare services, networks, and\n    insurance plans. Implements the HL7 Da Vinci PDex Plan Network IG and the\n    CMS Provider Directory API requirements.\n  version: '1.0'\n  contact:\n    name: Cigna Developer Support\n    url: https://developer.cigna.com/support\nexternalDocs:\n  description: Provider Directory Implementation Guide\n  url: https://developer.cigna.com/docs/service-apis/provider-directory/implementation-guide\nservers:\n  - url: https://fhir.cigna.com/ProviderDirectory/v1\n    description: Cigna Provider Directory Production\ntags:\n  - name: Practitioner\n  - name: Organization\n  - name: Location\n  - name: HealthcareService\n  - name: PractitionerRole\n  - name: Network\n  - name: InsurancePlan\npaths:\n  /metadata:\n    get:\n      operationId: getCapabilityStatement\n\
  \      summary: Retrieve the FHIR capability statement\n      tags: [Practitioner]\n      responses:\n        '200':\n          description: FHIR CapabilityStatement\n  /Practitioner:\n    get:\n      operationId: searchPractitioner\n      summary: Search practitioners in the Cigna network\n      tags: [Practitioner]\n      parameters:\n        - name: name\n          in: query\n          schema:\n            type: string\n        - name: identifier\n          in: query\n          schema:\n            type: string\n      responses:\n        '200':\n          description: FHIR Bundle of Practitioner resources\n  /Organization:\n    get:\n      operationId: searchOrganization\n      summary: Search organizations in the Cigna network\n      tags: [Organization]\n      responses:\n        '200':\n          description: FHIR Bundle of Organization resources\n  /Location:\n    get:\n      operationId: searchLocation\n      summary: Search locations of Cigna network providers\n      tags: [Location]\n\
  \      parameters:\n        - name: address\n          in: query\n          schema:\n            type: string\n        - name: address-postalcode\n          in: query\n          schema:\n            type: string\n      responses:\n        '200':\n          description: FHIR Bundle of Location resources\n  /HealthcareService:\n    get:\n      operationId: searchHealthcareService\n      summary: Search healthcare services offered by Cigna network providers\n      tags: [HealthcareService]\n      responses:\n        '200':\n          description: FHIR Bundle of HealthcareService resources\n  /PractitionerRole:\n    get:\n      operationId: searchPractitionerRole\n      summary: Search practitioner roles within Cigna networks\n      tags: [PractitionerRole]\n      responses:\n        '200':\n          description: FHIR Bundle of PractitionerRole resources\n  /InsurancePlan:\n    get:\n      operationId: searchInsurancePlan\n      summary: List Cigna insurance plans and the networks associated\
  \ with each\n      tags: [InsurancePlan]\n      responses:\n        '200':\n          description: FHIR Bundle of InsurancePlan resources\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cigna/refs/heads/main/openapi/cigna-provider-directory-api-openapi.yml
tags:
- CMS Interoperability
- FHIR
- Provider Directory
- Public API
---
