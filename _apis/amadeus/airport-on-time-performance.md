---
aid: amadeus:airport-on-time-performance
baseURL: https://api.amadeus.com
description: The Amadeus Airport On-Time Performance API predicts overall airport performance based on historical flight delay data. It estimates the probability of flights being delayed at a specific airport, helping travelers plan around potential disruptions.
humanURL: https://developers.amadeus.com/self-service/category/flights/api-doc/airport-on-time-performance
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Amadeus Airport On-Time Performance API
properties:
- type: Documentation
  url: https://developers.amadeus.com/self-service/category/flights/api-doc/airport-on-time-performance
- type: APIReference
  url: https://developers.amadeus.com/self-service/category/flights/api-doc/airport-on-time-performance/api-reference
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/airport-on-time-performance-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airport-on-time-performance-error-400-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airport-on-time-performance-error-500-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airport-on-time-performance-issue-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airport-on-time-performance-links-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/airport-on-time-performance-meta-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/airport-on-time-performance-error-400-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/airport-on-time-performance-error-500-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/airport-on-time-performance-issue-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-ld/amadeus-airport-on-time-performance-context.jsonld
provider_name: Amadeus
provider_slug: amadeus
slug: airport-on-time-performance
source_filename: airport-on-time-performance-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: 1.0.4\n  title: Amadeus Airport On-Time Performance\n  x-tags:\n  - '#ama-for-dev'\n  x-status: validated\n  x-release-note:\n    '1.0':\n    - Initial Version\n  description: \"Before using this API, we recommend you read our **[Authorization Guide](https://developers.amadeus.com/self-service/apis-docs/guides/authorization-262)** for more information on how to\n    generate an access token.\"\nhost: test.api.amadeus.com\nbasePath: /v1\nschemes:\n- https\nconsumes:\n- application/vnd.amadeus+json\nproduces:\n- application/vnd.amadeus+json\npaths:\n  /airport/predictions/on-time:\n    get:\n      tags:\n      - Airport\n      operationId: getAirportOnTimePrediction\n      summary: Amadeus Returns a Percentage of On-time Flight Departures from a Given Airport.\n      parameters:\n      - name: airportCode\n        in: query\n        description: >-\n          airport [IATA\n          code](http://www.iata.org/publications/Pages/code-search.aspx),\
  \ e.g.\n          BOS for Boston\n        required: true\n        type: string\n        pattern: '[A-Z]{3}'\n        x-example: JFK\n      - name: date\n        in: query\n        description: >-\n          the date on which the traveler will depart from the give airport.\n          Dates are specified in the [ISO\n          8601](https://en.wikipedia.org/wiki/ISO_8601) YYYY-MM-DD format,\n          e.g. 2019-12-25\n        required: true\n        type: string\n        format: date\n        x-example: '2023-11-12'\n      responses:\n        '200':\n          $ref: '#/responses/200'\n        '400':\n          $ref: '#/responses/400'\n        default:\n          $ref: '#/responses/500'\n      description: ''\ndefinitions:\n  Prediction:\n    type: object\n    properties:\n      data:\n        $ref: '#/definitions/OnTimePrediction'\n      meta:\n        $ref: '#/definitions/Meta'\n    example:\n      data:\n        id: JFK20231112\n        probability: '0.928'\n        result: '0.84062016'\n\
  \        subType: on-time\n        type: prediction\n      meta:\n        links:\n          self: >-\n            https://test.api.amadeus.com/v1/airport/predictions/on-time?airportCode=JFK&date=2023-11-12\n  Meta:\n    type: object\n    properties:\n      links:\n        $ref: '#/definitions/Links'\n  OnTimePrediction:\n    properties:\n      type:\n        description: the resource name (`prediction`)\n        type: string\n      subType:\n        type: string\n        example: trip-purpose\n      id:\n        description: item identifier\n        type: string\n        readOnly: true\n      result:\n        $ref: '#/definitions/PredictionResultType'\n      probability:\n        description: probability of the forecast (between 0 and 1)\n        type: string\n  PredictionResultType:\n    description: forecast description\n    type: string\n    example: 0.8\n  Links:\n    properties:\n      self:\n        type: string\n        format: uri\n      related:\n        type: string\n       \
  \ format: uri\n      type:\n        type: string\n  Error_400:\n    properties:\n      errors:\n        type: array\n        items:\n          $ref: '#/definitions/Issue'\n    required:\n    - errors\n    example:\n      errors:\n      - status: 400\n        code: 477\n        title: INVALID FORMAT\n        detail: invalid query parameter format\n        source:\n          parameter: airport\n          example: CDG\n  Error_500:\n    properties:\n      errors:\n        type: array\n        items:\n          $ref: '#/definitions/Issue'\n    required:\n    - errors\n    example:\n      errors:\n      - status: 500\n        code: 141\n        title: SYSTEM ERROR HAS OCCURRED\n  Issue:\n    properties:\n      status:\n        description: the HTTP status code applicable to this error\n        type: integer\n      code:\n        description: an application-specific error code\n        type: integer\n        format: int64\n      title:\n        description: a short summary of the error\n   \
  \     type: string\n      detail:\n        description: explanation of the error\n        type: string\n      source:\n        type: object\n        title: Issue_Source\n        description: an object containing references to the source of the error\n        maxProperties: 1\n        properties:\n          pointer:\n            description: >-\n              a JSON Pointer [RFC6901] to the associated entity in the request\n              document\n            type: string\n          parameter:\n            description: a string indicating which URI query parameter caused the issue\n            type: string\n          example:\n            description: a string indicating an example of the right value\n            type: string\nresponses:\n  '200':\n    description: Success\n    schema:\n      $ref: '#/definitions/Prediction'\n  '400':\n    description: \"code    | title                                 \\n- | - \\n477     | INVALID FORMAT\\n572     | INVALID OPTION\\n4926    | INVALID DATA\
  \ RECEIVED               \\n32171   | MANDATORY DATA MISSING\n      \\t     \\n\"\n    schema:\n      $ref: '#/definitions/Error_400'\n  '500':\n    description: Unexpected Error\n    schema:\n      $ref: '#/definitions/Error_500'\nx-generatedAt: '2020-07-23T14:07:22.902Z'\ntags:\n- name: Airport\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/airport-on-time-performance-openapi.yaml
tags:
- Airports
- Analytics
- Performance
---
