---
aid: bookingcom:booking-api
baseURL: https://api.booking.com
description: Booking.com provides APIs for hotel search, availability, rates, reservations, and property management. The Connectivity APIs enable partners to distribute and manage accommodation inventory.
humanURL: https://developers.booking.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Booking.com API
properties:
- type: Documentation
  url: https://developers.booking.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bookingcom/refs/heads/main/openapi/bookingcom-booking-api-openapi.yml
provider_name: Booking.com
provider_slug: bookingcom
slug: booking-api
source_filename: bookingcom-booking-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Booking.com API\n  description: >-\n    Booking.com provides APIs for hotel search, availability, rates, reservations, and property management. The Connectivity APIs enable partners to distribute and manage accommodation inventory.\n  version: '1.0'\n  contact:\n    name: Booking.com Developer Support\n    url: https://developers.booking.com/\nexternalDocs:\n  description: Documentation\n  url: https://developers.booking.com/\nservers:\n  - url: https://api.booking.com\n    description: Production\ntags:\n  - name: Travel\n    description: Travel operations\nsecurity:\n  - bearerAuth: []\npaths:\n  /status:\n    get:\n      operationId: getStatus\n      summary: Get API status\n      description: >-\n        Returns the current status of the API.\n      tags:\n        - Travel\n      responses:\n        '200':\n          description: Success\n          content:\n            application/json:\n              schema:\n                type: object\n\
  \                properties:\n                  status:\n                    type: string\n                  version:\n                    type: string\n        '401':\n          description: Unauthorized\n        '429':\n          description: Too many requests\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bookingcom/refs/heads/main/openapi/bookingcom-booking-api-openapi.yml
tags:
- Hospitality
- Hotels
- Reservations
- Travel
---
