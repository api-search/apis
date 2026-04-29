---
aid: cme-group:fedwatch-api
baseURL: ''
description: 'REST API exposing the data behind the CME FedWatch Tool: market-implied probabilities of FOMC rate-change decisions derived from 30-Day Fed Funds futures pricing.'
humanURL: https://www.cmegroup.com/markets/interest-rates/cme-fedwatch-tool.html
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CME FedWatch API
properties:
- type: Documentation
  url: https://www.cmegroup.com/markets/interest-rates/cme-fedwatch-tool.html
- type: Portal
  url: https://www.cmegroup.com/market-data/market-data-api.html
provider_name: CME Group
provider_slug: cme-group
slug: fedwatch-api
source_yaml: "aid: cme-group:fedwatch-api\nname: CME FedWatch API\ntags:\n- Fed Funds\n- Market-Implied Probabilities\n- Monetary Policy\n- REST\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://www.cmegroup.com/markets/interest-rates/cme-fedwatch-tool.html\nproperties:\n- url: https://www.cmegroup.com/markets/interest-rates/cme-fedwatch-tool.html\n  type: Documentation\n- url: https://www.cmegroup.com/market-data/market-data-api.html\n  type: Portal\ndescription: 'REST API exposing the data behind the CME FedWatch Tool: market-implied probabilities of\n  FOMC rate-change decisions derived from 30-Day Fed Funds futures pricing.'\nx-features:\n- name: FOMC Probabilities\n  description: Probabilities of rate moves at upcoming FOMC meetings.\n- name: Historical Probabilities\n  description: Time series of market-implied probabilities across meeting dates.\nx-useCases:\n- name: Macro Research\n  description: Embed Fed Funds expectations into\
  \ research and macro newsletters.\n- name: Risk Hedging\n  description: Inform interest-rate hedging programs with market-implied policy paths.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cme-group/refs/heads/main/apis.yml
tags:
- Fed Funds
- Market-Implied Probabilities
- Monetary Policy
- REST
---
