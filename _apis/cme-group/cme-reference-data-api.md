---
aid: cme-group:cme-reference-data-api
baseURL: ''
description: A set of JSON RESTful web service APIs that provide access to product and instrument reference data for CME Group, BrokerTec, EBS, hosted partners, and CME Group-cleared markets. Supports OAuth-secured access to product definitions, instrument metadata, market segment information, and trading hours used to power trading automation and risk systems.
humanURL: https://www.cmegroup.com/trading/market-tech-and-data-services/cme-reference-data-api.html
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CME Reference Data API
properties:
- type: Documentation
  url: https://www.cmegroup.com/trading/market-tech-and-data-services/cme-reference-data-api.html
- type: Reference
  url: https://cmegroupclientsite.atlassian.net/wiki/display/EPICSANDBOX/CME+Reference+Data+API+Version+3
- type: Portal
  url: https://www.cmegroup.com/market-data/market-data-api.html
provider_name: CME Group
provider_slug: cme-group
slug: cme-reference-data-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: cme-group:cme-reference-data-api\nname: CME Reference Data API\ntags:\n- Instruments\n- OAuth\n- Products\n- Reference Data\n- REST\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://www.cmegroup.com/trading/market-tech-and-data-services/cme-reference-data-api.html\nproperties:\n- url: https://www.cmegroup.com/trading/market-tech-and-data-services/cme-reference-data-api.html\n  type: Documentation\n- url: https://cmegroupclientsite.atlassian.net/wiki/display/EPICSANDBOX/CME+Reference+Data+API+Version+3\n  type: Reference\n- url: https://www.cmegroup.com/market-data/market-data-api.html\n  type: Portal\ndescription: A set of JSON RESTful web service APIs that provide access to product and instrument reference\n  data for CME Group, BrokerTec, EBS, hosted partners, and CME Group-cleared markets. Supports OAuth-secured\n  access to product definitions, instrument metadata, market segment information, and trading hours used\n\
  \  to power trading automation and risk systems.\nx-features:\n- name: Product Reference\n  description: Lookup of CME Group product definitions across asset classes.\n- name: Instrument Reference\n  description: Detailed instrument-level data including expirations, contract specs, and tick sizes.\n- name: Trading Hours\n  description: Authoritative trading hours and holiday calendars by venue.\n- name: OAuth Authentication\n  description: OAuth 2.0 secured access to reference data endpoints.\nx-useCases:\n- name: Trading Automation\n  description: Hydrate algorithmic trading systems with current product and instrument metadata.\n- name: Risk and Compliance\n  description: Drive risk and surveillance systems with authoritative reference data.\n- name: Order Routing\n  description: Validate and route orders against the latest CME instrument definitions.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cme-group/refs/heads/main/apis.yml
tags:
- Instruments
- OAuth
- Products
- Reference Data
- REST
---
