---
aid: car-api:vin-decoder-api
baseURL: https://carapi.app/api
description: The CarAPI VIN Decoder API decodes Vehicle Identification Numbers into structured vehicle attributes including year, make, model, trim, body type, engine, transmission, and other specifications. It reuses the same JWT authentication and shares the vehicle database that backs the main Vehicle API.
humanURL: https://carapi.app/features/vin-decoder-api
image: ''
layout: api
name: CarAPI VIN Decoder API
properties:
- type: Documentation
  url: https://carapi.app/features/vin-decoder-api
- type: Developer
  url: https://carapi.app/docs
provider_name: Car API (carapi.app)
provider_slug: car-api
slug: vin-decoder-api
source_yaml: "aid: car-api:vin-decoder-api\nname: CarAPI VIN Decoder API\ndescription: The CarAPI VIN Decoder API decodes Vehicle Identification Numbers into structured vehicle\n  attributes including year, make, model, trim, body type, engine, transmission, and other specifications.\n  It reuses the same JWT authentication and shares the vehicle database that backs the main Vehicle API.\nhumanURL: https://carapi.app/features/vin-decoder-api\nbaseURL: https://carapi.app/api\ntags:\n- Automobiles\n- Vehicles\n- VIN Decoder\nproperties:\n- url: https://carapi.app/features/vin-decoder-api\n  type: Documentation\n- url: https://carapi.app/docs\n  type: Developer\nx-features:\n- VIN to year/make/model/trim decoding\n- Returns body, engine, transmission, and other specs\n- Shared JWT auth with Vehicle API\n- JSON/JSON-LD/HAL response formats\nx-use-cases:\n- Insurance and warranty quote flows\n- Used-car listing auto-population\n- Lienholder, title, and registration tooling\n- Fleet onboarding\
  \ and telematics provisioning\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/car-api/refs/heads/main/apis.yml
tags:
- Automobiles
- Vehicles
- VIN Decoder
---
