---
aid: community-health-systems:provider-directory-api
baseURL: https://api.chs.net/fhir/r4
description: FHIR R4 read API exposing provider and pharmacy directory data in compliance with CMS interoperability requirements. Third-party applications can search Practitioner, Organization, and Location resources without patient consent (no PHI is exposed by these directory endpoints).
humanURL: https://www.chs.net
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Community Health Systems Provider Directory API
properties:
- type: Documentation
  url: https://www.chs.net
- type: CMSFinalRule
  url: https://www.cms.gov/regulations-and-guidance/guidance/interoperability/index
provider_name: Community Health Systems
provider_slug: community-health-systems
slug: provider-directory-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: community-health-systems:provider-directory-api\nname: Community Health Systems Provider Directory API\ntags:\n- CMS-9115-F\n- FHIR\n- Healthcare\n- Interoperability\n- Provider Directory\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.chs.net/fhir/r4\nhumanURL: https://www.chs.net\nproperties:\n- url: https://www.chs.net\n  type: Documentation\n- url: https://www.cms.gov/regulations-and-guidance/guidance/interoperability/index\n  type: CMSFinalRule\ndescription: FHIR R4 read API exposing provider and pharmacy directory data in compliance with CMS interoperability\n  requirements. Third-party applications can search Practitioner, Organization, and Location resources\n  without patient consent (no PHI is exposed by these directory endpoints).\nx-features:\n- FHIR R4 Practitioner, Organization, Location resources\n- Public read access (no patient consent required)\n- Search by name, specialty, location\nx-use-cases:\n\
  - Public provider/pharmacy directory lookup\n- Network adequacy and accessibility reporting\n- Care coordination and referral apps\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/community-health-systems/refs/heads/main/apis.yml
tags:
- CMS-9115-F
- FHIR
- Healthcare
- Interoperability
- Provider Directory
---
