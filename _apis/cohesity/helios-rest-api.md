---
aid: cohesity:helios-rest-api
baseURL: https://helios.cohesity.com/irisservices/api/v1/public/
description: Helios is Cohesity's SaaS-based control plane that manages a fleet of Cohesity clusters from a single global pane of glass. The Helios REST API authenticates via an apiKey generated from the Helios UI and passed in the request header, supports both v1 and v2 endpoint families, and lets customers list and operate registered clusters, run protection jobs, manage policies, and access reporting and analytics globally.
humanURL: https://developer.cohesity.com/helios-api.html
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cohesity Helios REST API
properties:
- type: Documentation
  url: https://developer.cohesity.com/helios-api.html
- type: GettingStarted
  url: https://developer.cohesity.com/docs/helios-getting-started
- type: APIReference
  url: https://developer.cohesity.com/apidocs/versions/
provider_name: Cohesity
provider_slug: cohesity
slug: helios-rest-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: cohesity:helios-rest-api\nname: Cohesity Helios REST API\ntags:\n- Automation\n- Cluster Management\n- DataProtect\n- Helios\n- Orchestration\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://helios.cohesity.com/irisservices/api/v1/public/\nhumanURL: https://developer.cohesity.com/helios-api.html\nproperties:\n- url: https://developer.cohesity.com/helios-api.html\n  type: Documentation\n- url: https://developer.cohesity.com/docs/helios-getting-started\n  type: GettingStarted\n- url: https://developer.cohesity.com/apidocs/versions/\n  type: APIReference\ndescription: Helios is Cohesity's SaaS-based control plane that manages a fleet of Cohesity clusters from\n  a single global pane of glass. The Helios REST API authenticates via an apiKey generated from the Helios\n  UI and passed in the request header, supports both v1 and v2 endpoint families, and lets customers list\n  and operate registered clusters, run protection\
  \ jobs, manage policies, and access reporting and analytics\n  globally.\nx-features:\n- apiKey-based authentication via Helios UI\n- v1 and v2 API surfaces under /irisservices/api/\n- Manage protection groups, policies, and recovery operations\n- Reporting and global analytics across clusters\n- Multi-cluster operations from a single endpoint\nx-use-cases:\n- Centralize backup and recovery automation across many Cohesity clusters\n- Drive policy and SLA enforcement from CI/CD pipelines\n- Trigger or schedule recoveries from external orchestration tools\n- Export reporting data into SIEM or BI dashboards\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cohesity/refs/heads/main/apis.yml
tags:
- Automation
- Cluster Management
- DataProtect
- Helios
- Orchestration
---
