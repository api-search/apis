---
aid: aladdin-studio:investment-research-api
baseURL: https://api.blackrock.com/research/v1
description: The Aladdin Investment Research API provides access to research data, analyst insights, and quantitative analytics built on Aladdin's data infrastructure. Available as the asdk_plugin_investment_research Python package.
humanURL: https://www.blackrock.com/aladdin/products/apis
image: ''
layout: api
name: Aladdin Investment Research API
properties:
- type: Documentation
  url: https://www.blackrock.com/aladdin/products/apis
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-investment-research-openapi.yaml
- title: Python Investment Research Plugin
  type: SDK
  url: https://pypi.org/project/asdk-plugin-investment-research/
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/json-schema/aladdin-studio-investment-research-security-research-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/json-schema/aladdin-studio-investment-research-portfolio-analytics-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/json-structure/aladdin-studio-investment-research-security-research-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/json-structure/aladdin-studio-investment-research-portfolio-analytics-structure.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/examples/aladdin-studio-investment-research-security-research-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/examples/aladdin-studio-investment-research-portfolio-analytics-example.json
provider_name: Aladdin Studio
provider_slug: aladdin-studio
slug: investment-research-api
source_filename: aladdin-studio-investment-research-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Aladdin Investment Research API\n  description: >-\n    The Aladdin Investment Research API provides access to research data,\n    analyst insights, and quantitative analytics built on Aladdin's data\n    infrastructure. Available via the asdk_plugin_investment_research Python package.\n  version: 1.0.0\n  contact:\n    name: Aladdin Studio\n    url: https://www.blackrock.com/aladdin/products/apis\n  license:\n    name: Proprietary\n    url: https://www.blackrock.com/aladdin/products/aladdin-studio\n  x-generated-from: documentation\nservers:\n  - url: https://api.blackrock.com/research/v1\n    description: Aladdin Investment Research API server\nsecurity:\n  - OAuth2: []\npaths:\n  /securities/{securityId}/research:\n    get:\n      operationId: getSecurityResearch\n      summary: Aladdin Studio Get Security Research\n      description: >-\n        Retrieve investment research data for a specific security including\n        analyst ratings,\
  \ price targets, and research notes.\n      tags:\n        - Research\n      parameters:\n        - name: securityId\n          in: path\n          required: true\n          description: Security identifier (ISIN or internal ID)\n          schema:\n            type: string\n            example: US0378331005\n      responses:\n        '200':\n          description: Security research data\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SecurityResearch'\n              examples:\n                getSecurityResearch200Example:\n                  summary: Default getSecurityResearch 200 response\n                  x-microcks-default: true\n                  value:\n                    securityId: US0378331005\n                    ticker: AAPL\n                    rating: buy\n                    priceTarget: 225.00\n                    analystCount: 42\n                    consensusDate: \"2026-04-19\"\n        '404':\n\
  \          description: Security not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /portfolios/{portfolioId}/analytics:\n    get:\n      operationId: getPortfolioAnalytics\n      summary: Aladdin Studio Get Portfolio Analytics\n      description: >-\n        Retrieve investment analytics for a portfolio including attribution,\n        performance metrics, and factor analysis.\n      tags:\n        - Analytics\n      parameters:\n        - name: portfolioId\n          in: path\n          required: true\n          description: Portfolio identifier\n          schema:\n            type: string\n            example: PF-123456\n        - name: fromDate\n          in: query\n          description: Start date for analytics period (YYYY-MM-DD)\n          schema:\n            type: string\n            format: date\n            example: \"2026-01-01\"\n        - name: toDate\n          in: query\n          description: End date for analytics period (YYYY-MM-DD)\n\
  \          schema:\n            type: string\n            format: date\n            example: \"2026-04-19\"\n      responses:\n        '200':\n          description: Portfolio analytics\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/PortfolioAnalytics'\n              examples:\n                getPortfolioAnalytics200Example:\n                  summary: Default getPortfolioAnalytics 200 response\n                  x-microcks-default: true\n                  value:\n                    portfolioId: PF-123456\n                    fromDate: \"2026-01-01\"\n                    toDate: \"2026-04-19\"\n                    totalReturn: 0.0485\n                    excessReturn: 0.0132\n                    informationRatio: 0.85\n        '404':\n          description: Portfolio not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    OAuth2:\n      type: oauth2\n\
  \      description: OAuth 2.0 authentication for research data access\n      flows:\n        clientCredentials:\n          tokenUrl: https://api.blackrock.com/oauth/token\n          scopes:\n            research:read: Read research data\n            analytics:read: Read analytics data\n  schemas:\n    SecurityResearch:\n      title: SecurityResearch\n      type: object\n      description: Investment research data for a security\n      properties:\n        securityId:\n          type: string\n          description: Security identifier\n          example: US0378331005\n        ticker:\n          type: string\n          description: Ticker symbol\n          example: AAPL\n        rating:\n          type: string\n          description: Analyst consensus rating\n          enum:\n            - buy\n            - hold\n            - sell\n          example: buy\n        priceTarget:\n          type: number\n          description: Consensus price target\n          example: 225.00\n        analystCount:\n\
  \          type: integer\n          description: Number of analysts covering the security\n          example: 42\n        consensusDate:\n          type: string\n          format: date\n          description: Date of consensus calculation\n          example: \"2026-04-19\"\n    PortfolioAnalytics:\n      title: PortfolioAnalytics\n      type: object\n      description: Investment analytics and performance metrics for a portfolio\n      properties:\n        portfolioId:\n          type: string\n          description: Portfolio identifier\n          example: PF-123456\n        fromDate:\n          type: string\n          format: date\n          description: Analytics period start date\n          example: \"2026-01-01\"\n        toDate:\n          type: string\n          format: date\n          description: Analytics period end date\n          example: \"2026-04-19\"\n        totalReturn:\n          type: number\n          description: Total portfolio return for the period\n          example:\
  \ 0.0485\n        excessReturn:\n          type: number\n          description: Excess return vs benchmark\n          example: 0.0132\n        informationRatio:\n          type: number\n          description: Information ratio for the period\n          example: 0.85\n        sharpeRatio:\n          type: number\n          description: Sharpe ratio for the period\n          example: 1.24\ntags:\n  - name: Research\n    description: Investment research data and analyst ratings\n  - name: Analytics\n    description: Portfolio performance and attribution analytics\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-investment-research-openapi.yaml
tags:
- Investment Research
- Analytics
- Portfolio
---
