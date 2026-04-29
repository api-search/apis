---
aid: capital-com-public-api:capital-com-rest-api
baseURL: ''
description: The Capital.com REST API provides programmatic access to positions, working orders, deal confirmations, account information, account switching, transaction history, preferences (leverage, hedging mode), market navigation, instrument details, historical prices, watchlists, and client sentiment data. Authentication uses an API key plus login credentials to create a session that returns CST and X-SECURITY-TOKEN headers, which expire after 10 minutes of inactivity.
humanURL: https://open-api.capital.com
image: ''
layout: api
name: Capital.com REST API
properties:
- type: Documentation
  url: https://open-api.capital.com
- type: Base URL
  url: https://api-capital.backend-capital.com/
- type: Sandbox
  url: https://demo-api-capital.backend-capital.com/
- type: Authentication
  url: https://open-api.capital.com
provider_name: Capital.com Public API
provider_slug: capital-com-public-api
slug: capital-com-rest-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: capital-com-public-api:capital-com-rest-api\nname: Capital.com REST API\ndescription: The Capital.com REST API provides programmatic access to positions, working orders, deal\n  confirmations, account information, account switching, transaction history, preferences (leverage, hedging\n  mode), market navigation, instrument details, historical prices, watchlists, and client sentiment data.\n  Authentication uses an API key plus login credentials to create a session that returns CST and X-SECURITY-TOKEN\n  headers, which expire after 10 minutes of inactivity.\nhumanURL: https://open-api.capital.com\ntags:\n- CFD\n- Financial\n- Market Data\n- Trading\nproperties:\n- type: Documentation\n  url: https://open-api.capital.com\n- type: Base URL\n  url: https://api-capital.backend-capital.com/\n- type: Sandbox\n  url: https://demo-api-capital.backend-capital.com/\n- type: Authentication\n  url: https://open-api.capital.com\nx-features:\n- Session-based authentication with CST\
  \ and X-SECURITY-TOKEN\n- API key plus login credentials to create sessions\n- 10-minute inactivity session expiry\n- Position management (open, update, close)\n- Working orders (limit and stop)\n- Deal confirmations and execution tracking\n- Account switching across multiple accounts\n- Transaction and activity history\n- Leverage and hedging-mode preferences\n- Demo account balance adjustment for testing\n- Market navigation hierarchy\n- Instrument details and search\n- Historical price data (OHLC)\n- Client sentiment data\n- Watchlist management\nx-use-cases:\n- Building automated CFD trading strategies\n- Algorithmic execution across shares, forex, commodities, indices, and crypto\n- Copy-trading and signal-provider applications\n- Portfolio and risk dashboards\n- Backtesting against historical price data\n- Sentiment-driven trading signals\n- Demo-account integration testing before going live\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/capital-com-public-api/refs/heads/main/apis.yml
tags:
- CFD
- Financial
- Market Data
- Trading
---
