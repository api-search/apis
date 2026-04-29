---
aid: amadeus:trip-purpose-prediction
baseURL: https://api.amadeus.com
description: The Amadeus Trip Purpose Prediction API predicts whether a flight search is for business or leisure travel using machine learning. It analyzes patterns in departure and arrival cities, flight dates, and search dates to help travel applications personalize offers for each traveler.
humanURL: https://developers.amadeus.com/self-service/category/itinerary-management/api-doc/trip-purpose-prediction
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Amadeus Trip Purpose Prediction API
properties:
- type: Documentation
  url: https://developers.amadeus.com/self-service/category/itinerary-management/api-doc/trip-purpose-prediction
- type: APIReference
  url: https://developers.amadeus.com/self-service/category/itinerary-management/api-doc/trip-purpose-prediction/api-reference
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/trip-purpose-prediction-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/trip-purpose-prediction-defaults-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/trip-purpose-prediction-error-400-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/trip-purpose-prediction-error-500-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/trip-purpose-prediction-issue-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/trip-purpose-prediction-links-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/trip-purpose-prediction-defaults-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/trip-purpose-prediction-error-400-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/trip-purpose-prediction-error-500-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-ld/amadeus-trip-purpose-prediction-context.jsonld
provider_name: Amadeus
provider_slug: amadeus
slug: trip-purpose-prediction
source_filename: trip-purpose-prediction-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: 1.1.4\n  title: Amadeus Trip Purpose Prediction\n  x-tags:\n  - '#ama-for-dev'\n  x-status: pending\n  x-release-note:\n    '1.1':\n    - Remove self section from data\n    - Add defaults to meta\n    - Change result into an enum\n    '1.0':\n    - Initial Version\n  description: \"\\nBefore using this API, we recommend you read our **[Authorization Guide](https://developers.amadeus.com/self-service/apis-docs/guides/authorization-262)** for more information on how to\n    generate an access token.\"\nhost: test.api.amadeus.com\nbasePath: /v1\nschemes:\n- https\nconsumes:\n- application/vnd.amadeus+json\nproduces:\n- application/vnd.amadeus+json\npaths:\n  /travel/predictions/trip-purpose:\n    get:\n      tags:\n      - Travel\n      operationId: getTripPurposePrediction\n      summary: Amadeus Returns the Forecast Purpose of a Trip\n      parameters:\n      - name: originLocationCode\n        in: query\n        description: >-\n          city/airport\
  \ [IATA\n          code](http://www.iata.org/publications/Pages/code-search.aspx) from\n          which the traveler will depart, e.g. BOS for Boston\n        required: true\n        type: string\n        pattern: '[A-Z]{3}'\n        x-example: NYC\n      - name: destinationLocationCode\n        in: query\n        description: >-\n          city/airport [IATA\n          code](http://www.iata.org/publications/Pages/code-search.aspx) to\n          which the traveler is going, e.g. PAR for Paris\n        required: true\n        type: string\n        pattern: '[A-Z]{3}'\n        x-example: MAD\n      - name: departureDate\n        in: query\n        description: >-\n          the date on which the traveler will depart from the origin to go to\n          the destination. Dates are specified in the [ISO\n          8601](https://en.wikipedia.org/wiki/ISO_8601) YYYY-MM-DD format,\n          e.g. 2017-12-25\n        required: true\n        type: string\n        x-example: '2023-12-01'\n      -\
  \ name: returnDate\n        in: query\n        description: >-\n          the date on which the traveler will depart from the destination to\n          return to the origin. Dates are specified in the [ISO\n          8601](https://en.wikipedia.org/wiki/ISO_8601) YYYY-MM-DD format,\n          e.g. 2018-02-28\n        required: true\n        type: string\n        x-example: '2023-12-12'\n      - name: searchDate\n        in: query\n        description: >-\n          the date on which the traveler is performing the search. If this\n          parameter is not specified, current date will be used. Dates are\n          specified in the [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)\n          YYYY-MM-DD format, e.g. 2018-02-28\n        required: false\n        type: string\n      responses:\n        '200':\n          $ref: '#/responses/200'\n        '400':\n          $ref: '#/responses/400'\n        default:\n          $ref: '#/responses/500'\n      description: ''\ndefinitions:\n  Prediction:\n\
  \    type: object\n    properties:\n      data:\n        $ref: '#/definitions/Purpose_Prediction'\n      meta:\n        $ref: '#/definitions/Meta'\n    example:\n      data:\n        id: NYCMAD20231201\n        probability: '0.9995216'\n        result: LEISURE\n        subType: trip-purpose\n        type: prediction\n      meta:\n        defaults:\n          searchDate: '2023-01-12'\n        links:\n          self: >-\n            https://test.api.amadeus.com/v1/travel/predictions/trip-purpose?originLocationCode=NYC&destinationLocationCode=MAD&departureDate=2023-12-01&returnDate=2023-12-12&searchDate=2023-01-12\n  Meta:\n    type: object\n    properties:\n      links:\n        $ref: '#/definitions/Links'\n      defaults:\n        $ref: '#/definitions/Defaults'\n  Purpose_Prediction:\n    properties:\n      type:\n        description: the resource name (`prediction`)\n        type: string\n      subType:\n        type: string\n        example: trip-purpose\n      id:\n        description:\
  \ item identifier\n        type: string\n        readOnly: true\n      result:\n        $ref: '#/definitions/PredictionResultType'\n      probability:\n        description: probability of the forecast (between 0 and 1)\n        type: string\n  PredictionResultType:\n    description: forecast description\n    type: string\n    enum:\n    - BUSINESS\n    - LEISURE\n    example: BUSINESS\n  Links:\n    properties:\n      self:\n        type: string\n        format: uri\n      related:\n        type: string\n        format: uri\n      type:\n        type: string\n  Defaults:\n    description: the query parameters for which default values were used are returned here\n    type: object\n    properties:\n      searchDate:\n        description: the date on which the traveler is performing the search.\n        type: string\n        example: '2019-06-11'\n  Error_400:\n    properties:\n      errors:\n        type: array\n        items:\n          $ref: '#/definitions/Issue'\n    required:\n    -\
  \ errors\n    example:\n      errors:\n      - status: 400\n        code: 477\n        title: INVALID FORMAT\n        detail: invalid query parameter format\n        source:\n          parameter: airport\n          example: CDG\n  Error_500:\n    properties:\n      errors:\n        type: array\n        items:\n          $ref: '#/definitions/Issue'\n    required:\n    - errors\n    example:\n      errors:\n      - status: 500\n        code: 141\n        title: SYSTEM ERROR HAS OCCURRED\n  Issue:\n    properties:\n      status:\n        description: the HTTP status code applicable to this error\n        type: integer\n      code:\n        description: an application-specific error code\n        type: integer\n        format: int64\n      title:\n        description: a short summary of the error\n        type: string\n      detail:\n        description: explanation of the error\n        type: string\n      source:\n        type: object\n        title: Issue_Source\n        description: an\
  \ object containing references to the source of the error\n        maxProperties: 1\n        properties:\n          pointer:\n            description: >-\n              a JSON Pointer [RFC6901] to the associated entity in the request\n              document\n            type: string\n          parameter:\n            description: a string indicating which URI query parameter caused the issue\n            type: string\n          example:\n            description: a string indicating an example of the right value\n            type: string\nresponses:\n  '200':\n    description: Success\n    schema:\n      $ref: '#/definitions/Prediction'\n  '400':\n    description: \"code    | title                                 \\n- | - \\n477     | INVALID FORMAT\\n572     | INVALID OPTION\\n4926    | INVALID DATA RECEIVED               \\n32171   | MANDATORY DATA MISSING\n      \\t     \\n\"\n    schema:\n      $ref: '#/definitions/Error_400'\n  '500':\n    description: Unexpected Error\n    schema:\n\
  \      $ref: '#/definitions/Error_500'\nx-generatedAt: '2020-07-23T08:01:18.792Z'\ntags:\n- name: Travel\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/trip-purpose-prediction-openapi.yaml
tags:
- Itinerary
- Machine Learning
- Prediction
- Trips
---
