---
aid: coinapi:market-data-api
baseURL: https://rest.coinapi.io
description: Normalized cryptocurrency market data covering more than 350 exchanges and 28,000+ assets. Provides trades, quotes, order books, OHLCV time series, exchange rates, and derivatives metrics (funding rates, mark prices, liquidations, open interest, volumes). Delivered through REST for historical snapshots and lookups, WebSocket and FIX for real-time streaming, and S3 flat files for bulk historical analysis.
humanURL: https://www.coinapi.io/products/market-data-api
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CoinAPI Market Data API
properties:
- type: Documentation
  url: https://docs.coinapi.io/market-data/
- type: Landing Page
  url: https://www.coinapi.io/products/market-data-api
- type: FAQ
  url: https://www.coinapi.io/products/market-data-api/faq
- type: FIX Documentation
  url: https://www.coinapi.io/products/market-data-api/docs/fix
provider_name: CoinAPI
provider_slug: coinapi
slug: market-data-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: coinapi:market-data-api\nname: CoinAPI Market Data API\ntags:\n- Crypto Metrics\n- Cryptocurrency\n- Exchange Rates\n- FIX\n- Market Data\n- OHLCV\n- Order Books\n- REST\n- WebSocket\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://rest.coinapi.io\nhumanURL: https://www.coinapi.io/products/market-data-api\nproperties:\n- url: https://docs.coinapi.io/market-data/\n  type: Documentation\n- url: https://www.coinapi.io/products/market-data-api\n  type: Landing Page\n- url: https://www.coinapi.io/products/market-data-api/faq\n  type: FAQ\n- url: https://www.coinapi.io/products/market-data-api/docs/fix\n  type: FIX Documentation\ndescription: Normalized cryptocurrency market data covering more than 350 exchanges and 28,000+ assets.\n  Provides trades, quotes, order books, OHLCV time series, exchange rates, and derivatives metrics (funding\n  rates, mark prices, liquidations, open interest, volumes). Delivered through REST for\
  \ historical snapshots\n  and lookups, WebSocket and FIX for real-time streaming, and S3 flat files for bulk historical analysis.\nx-features:\n- REST, WebSocket, and FIX delivery channels\n- S3 flat-file delivery for historical bulk data\n- Normalized symbol IDs across all exchanges\n- 350+ supported exchanges and 28,000+ assets\n- Derivatives metrics (funding, mark prices, OI, liquidations)\n- GeoDNS-routed FIX endpoints (fix.coinapi.io)\n- API-key authentication via X-CoinAPI-Key header\nx-use-cases:\n- Power trading dashboards with live order book data\n- Backtest strategies against full historical OHLCV\n- Compute reference rates from cross-exchange quotes\n- Monitor derivatives exposure (funding, OI) in real time\n- Feed BI/data lakes via daily S3 flat-file drops\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coinapi/refs/heads/main/apis.yml
tags:
- Crypto Metrics
- Cryptocurrency
- Exchange Rates
- FIX
- Market Data
- OHLCV
- Order Books
- REST
- WebSocket
---
