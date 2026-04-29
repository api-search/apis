---
aid: cme-group:greeks-iv-api
baseURL: ''
description: REST API delivering CME-calculated option Greeks (delta, gamma, vega, theta, rho) and implied volatility surfaces for CME Group options markets. JSON payloads accessed via the Data Services self-service API portal.
humanURL: https://www.cmegroup.com/market-data/market-data-api.html
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Greeks and Implied Volatility API
properties:
- type: Documentation
  url: https://www.cmegroup.com/market-data/market-data-api.html
provider_name: CME Group
provider_slug: cme-group
slug: greeks-iv-api
source_yaml: "aid: cme-group:greeks-iv-api\nname: Greeks and Implied Volatility API\ntags:\n- Greeks\n- Implied Volatility\n- Options\n- REST\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://www.cmegroup.com/market-data/market-data-api.html\nproperties:\n- url: https://www.cmegroup.com/market-data/market-data-api.html\n  type: Documentation\ndescription: REST API delivering CME-calculated option Greeks (delta, gamma, vega, theta, rho) and implied\n  volatility surfaces for CME Group options markets. JSON payloads accessed via the Data Services self-service\n  API portal.\nx-features:\n- name: Greeks\n  description: Delta, gamma, vega, theta, and rho per option.\n- name: Implied Volatility\n  description: Implied volatility per strike and expiry.\nx-useCases:\n- name: Option Pricing\n  description: Power option pricing and risk systems with CME-calculated Greeks.\n- name: Risk Distribution\n  description: Distribute volatility-surface data\
  \ into trading and analytics systems.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cme-group/refs/heads/main/apis.yml
tags:
- Greeks
- Implied Volatility
- Options
- REST
---
