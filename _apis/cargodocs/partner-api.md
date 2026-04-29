---
aid: cargodocs:partner-api
baseURL: https://api.essdocs.com
description: The CargoDocs Partner API enables platform providers and trade finance/trade management platforms to embed CargoDocs DocEx functionality, including original electronic bills of lading (eBoL) and warehouse warrants (eWW). The API exposes Partner Exchange endpoints to retrieve customer, counterparty, document, and transaction data using conditions and filters, and Action endpoints to perform operations over transactions such as signing, transferring, and surrendering documents.
humanURL: https://cargodocs-partner.readme.io/
image: ''
layout: api
name: CargoDocs Partner API
properties:
- type: Documentation
  url: https://cargodocs-partner.readme.io/
- type: GettingStarted
  url: https://cargodocs-partner.readme.io/docs/api-environments
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/openapi/cargodocs-partner-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/json-schema/cargodocs-customer.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/json-schema/cargodocs-counterparty.json
provider_name: CargoDocs
provider_slug: cargodocs
slug: partner-api
source_yaml: "aid: cargodocs:partner-api\nname: CargoDocs Partner API\ndescription: The CargoDocs Partner API enables platform providers and trade finance/trade management platforms\n  to embed CargoDocs DocEx functionality, including original electronic bills of lading (eBoL) and warehouse\n  warrants (eWW). The API exposes Partner Exchange endpoints to retrieve customer, counterparty, document,\n  and transaction data using conditions and filters, and Action endpoints to perform operations over transactions\n  such as signing, transferring, and surrendering documents.\nhumanURL: https://cargodocs-partner.readme.io/\nbaseURL: https://api.essdocs.com\ntags:\n- Bills of Lading\n- Shipping\n- Trade\nproperties:\n- url: https://cargodocs-partner.readme.io/\n  type: Documentation\n- url: https://cargodocs-partner.readme.io/docs/api-environments\n  type: GettingStarted\n- url: openapi/cargodocs-partner-openapi.yml\n  type: OpenAPI\n- url: json-schema/cargodocs-customer.json\n  type: JSONSchema\n\
  - url: json-schema/cargodocs-counterparty.json\n  type: JSONSchema\nx-features:\n- Retrieve customer, counterparty, and transaction data with filters\n- Perform signing, transferring, and surrendering actions\n- Embed DocEx workflows in partner platforms\n- Sandbox and production API environments\n- JSON document retrieval plus PDF rendering\n- Partner-scoped authentication and audit trail\nx-use-cases:\n- Trade finance platforms embedding eBoL workflows\n- TMS/CTRM providers offering native digital docs\n- Freight forwarder portals with integrated surrender flows\n- Bank-held eBoL custody during letter-of-credit settlement\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/apis.yml
tags:
- Bills of Lading
- Shipping
- Trade
---
