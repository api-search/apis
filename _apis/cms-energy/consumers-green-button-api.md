---
aid: cms-energy:consumers-green-button-api
baseURL: ''
description: The Consumers Energy Green Button Connect My Data API exposes customer-authorized electric and natural-gas usage data to registered third parties using the NAESB ESPI / Green Button standard. Authorization uses OAuth 2.0 with single sign-on or test-account scopes; data is delivered as Green Button XML or JSON via UtilityAPI's standardized endpoints (Meters, Bills, Intervals, Billing Summaries). Third parties register with Consumers Energy, are issued a client_id, and start in sandbox mode before being approved for live data.
humanURL: https://utilityapi.com/docs/utilities/consumersenergy
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Consumers Energy Green Button Connect My Data API
properties:
- type: Documentation
  url: https://utilityapi.com/docs/utilities/consumersenergy
- type: Portal
  url: https://utilityapi.com/
provider_name: CMS Energy
provider_slug: cms-energy
slug: consumers-green-button-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: cms-energy:consumers-green-button-api\nname: Consumers Energy Green Button Connect My Data API\ntags:\n- Energy Usage\n- Green Button\n- OAuth2\n- Smart Meter\n- Utility\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://utilityapi.com/docs/utilities/consumersenergy\nproperties:\n- url: https://utilityapi.com/docs/utilities/consumersenergy\n  type: Documentation\n- url: https://utilityapi.com/\n  type: Portal\ndescription: The Consumers Energy Green Button Connect My Data API exposes customer-authorized electric\n  and natural-gas usage data to registered third parties using the NAESB ESPI / Green Button standard.\n  Authorization uses OAuth 2.0 with single sign-on or test-account scopes; data is delivered as Green\n  Button XML or JSON via UtilityAPI's standardized endpoints (Meters, Bills, Intervals, Billing Summaries).\n  Third parties register with Consumers Energy, are issued a client_id, and start in sandbox mode\
  \ before\n  being approved for live data.\nx-features:\n- name: Green Button Standard\n  description: NAESB ESPI / Green Button XML for usage point and interval data.\n- name: Meters Endpoint\n  description: Retrieve individual meter information for an authorized customer.\n- name: Bills Endpoint\n  description: Retrieve bill history and charges.\n- name: Intervals Endpoint\n  description: Retrieve granular interval-usage time series.\n- name: Billing Summaries\n  description: Retrieve account-level summary data.\n- name: OAuth 2.0\n  description: Customer authorization via OAuth 2.0 with SSO or test scopes.\n- name: Sandbox Test Accounts\n  description: Built-in test residential and commercial scenarios for development.\nx-useCases:\n- name: Energy Efficiency\n  description: Pull usage data into energy efficiency and benchmarking apps.\n- name: Demand Response\n  description: Power demand-response and load-management programs.\n- name: Solar and EV\n  description: Inform solar sizing\
  \ and EV-charging optimization with real usage.\n- name: Sustainability Reporting\n  description: Aggregate usage into Scope 2 emissions and ESG reporting.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cms-energy/refs/heads/main/apis.yml
tags:
- Energy Usage
- Green Button
- OAuth2
- Smart Meter
- Utility
---
