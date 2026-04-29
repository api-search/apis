---
aid: amadeus:airline-code-lookup
baseURL: https://api.amadeus.com
description: The Amadeus Airline Code Lookup API finds the name of an airline by its IATA or ICAO airline codes. It helps travel applications display human-readable airline names alongside flight data that uses industry-standard airline code identifiers.
humanURL: https://developers.amadeus.com/self-service/category/flights/api-doc/airline-code-lookup
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Amadeus Airline Code Lookup API
properties:
- type: Documentation
  url: https://developers.amadeus.com/self-service/category/flights/api-doc/airline-code-lookup
- type: APIReference
  url: https://developers.amadeus.com/self-service/category/flights/api-doc/airline-code-lookup/api-reference
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/airline-code-lookup-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airline-code-lookup-airline-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airline-code-lookup-airlinecollection-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airline-code-lookup-collectionmeta-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airline-code-lookup-errorresponse-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airline-code-lookup-issue-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/airline-code-lookup-airline-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/airline-code-lookup-airlinecollection-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/airline-code-lookup-collectionmeta-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-ld/amadeus-airline-code-lookup-context.jsonld
provider_name: Amadeus
provider_slug: amadeus
slug: airline-code-lookup
source_filename: airline-code-lookup-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Amadeus Airline Code Lookup API\n  description: >-\n    The Amadeus Airline Code Lookup API finds the name of an airline by its IATA\n    or ICAO airline codes. It helps travel applications display human-readable\n    airline names alongside flight data that uses industry-standard airline code\n    identifiers. The API accepts a unified airlineCodes parameter supporting both\n    two-letter IATA codes and three-letter ICAO codes.\n  version: '1.1.1'\n  contact:\n    name: Amadeus for Developers\n    url: https://developers.amadeus.com/support\n  termsOfService: https://developers.amadeus.com/legal/terms-of-use\nexternalDocs:\n  description: Amadeus Airline Code Lookup API Documentation\n  url: https://developers.amadeus.com/self-service/category/flights/api-doc/airline-code-lookup\nservers:\n- url: https://api.amadeus.com/v1\n  description: Production Server\n- url: https://test.api.amadeus.com/v1\n  description: Test Server\ntags:\n- name: Airlines\n\
  \  description: >-\n    Operations for looking up airline information using IATA or ICAO codes.\nsecurity:\n- bearerAuth: []\npaths:\n  /reference-data/airlines:\n    get:\n      operationId: getAirlines\n      summary: Amadeus Look Up Airline by IATA or ICAO Code\n      description: >-\n        Returns airline information for the given IATA or ICAO airline codes. The\n        airlineCodes parameter accepts both two-letter IATA codes and three-letter\n        ICAO codes, and supports multiple comma-separated codes in a single\n        request.\n      tags:\n      - Airlines\n      parameters:\n      - $ref: '#/components/parameters/airlineCodes'\n      responses:\n        '200':\n          description: Successful response containing matching airline data.\n          content:\n            application/vnd.amadeus+json:\n              schema:\n                $ref: '#/components/schemas/AirlineCollection'\n        '400':\n          description: >-\n            Bad request due to invalid parameters\
  \ such as malformed airline codes.\n          content:\n            application/vnd.amadeus+json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized request due to missing or invalid access token.\n          content:\n            application/vnd.amadeus+json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '500':\n          description: Internal server error due to an unexpected system condition.\n          content:\n            application/vnd.amadeus+json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n      description: >-\n        Access token obtained from the Amadeus OAuth2 token endpoint using\n        client credentials grant.\n  parameters:\n    airlineCodes:\n      name: airlineCodes\n      in: query\n\
  \      required: false\n      description: >-\n        IATA or ICAO airline codes. Accepts two-letter IATA codes or three-letter\n        ICAO codes. Multiple codes can be provided separated by commas.\n      schema:\n        type: string\n      example: BA\n  schemas:\n    AirlineCollection:\n      type: object\n      description: >-\n        A collection response containing an array of airline resources and\n        associated metadata.\n      properties:\n        meta:\n          $ref: '#/components/schemas/CollectionMeta'\n        data:\n          type: array\n          description: Array of airline resources matching the query.\n          items:\n            $ref: '#/components/schemas/Airline'\n        warnings:\n          type: array\n          description: >-\n            Non-blocking issues encountered during the request processing.\n          items:\n            $ref: '#/components/schemas/Issue'\n    Airline:\n      type: object\n      description: >-\n        An airline resource\
  \ containing identifying codes and names for a single\n        airline carrier.\n      properties:\n        type:\n          type: string\n          description: Resource type identifier.\n          const: airline\n        iataCode:\n          type: string\n          description: >-\n            Two-letter IATA airline designator code.\n          pattern: '[A-Z0-9]{2}'\n          example: BA\n        icaoCode:\n          type: string\n          description: >-\n            Three-letter ICAO airline designator code.\n          pattern: '[A-Z]{3}'\n          example: BAW\n        businessName:\n          type: string\n          description: >-\n            The official business name of the airline.\n          example: BRITISH AIRWAYS\n        commonName:\n          type: string\n          description: >-\n            The commonly used abbreviated name of the airline.\n          example: BRITISH A/W\n    CollectionMeta:\n      type: object\n      description: Metadata about the response collection.\n\
  \      properties:\n        count:\n          type: integer\n          description: Total number of items in the collection.\n          example: 1\n        links:\n          type: object\n          description: Links related to the collection.\n          properties:\n            self:\n              type: string\n              format: uri\n              description: Link to the current request.\n    Issue:\n      type: object\n      description: >-\n        A non-blocking warning or issue encountered during request processing.\n      properties:\n        status:\n          type: integer\n          description: HTTP status code associated with the issue.\n        code:\n          type: integer\n          description: Application-specific error code.\n        title:\n          type: string\n          description: Short description of the issue.\n        detail:\n          type: string\n          description: Detailed explanation of the issue.\n        source:\n          type: object\n  \
  \        properties:\n            pointer:\n              type: string\n              description: JSON pointer to the associated entity in the request.\n            parameter:\n              type: string\n              description: Name of the query parameter that caused the issue.\n            example:\n              type: string\n              description: Example of a valid value for the parameter.\n    ErrorResponse:\n      type: object\n      description: Error response containing one or more error details.\n      properties:\n        errors:\n          type: array\n          description: Array of error details.\n          items:\n            $ref: '#/components/schemas/Issue'\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/airline-code-lookup-openapi.yaml
tags:
- Airlines
- Codes
- IATA
- ICAO
---
