---
aid: pluralsight:public-course-catalog-rest-api
baseURL: https://paas-rest-api.pluralsight.com
description: Legacy public REST API for accessing the full course catalog without authentication. Returns course IDs, titles, durations, release dates, and retirement status.
humanURL: https://help.pluralsight.com/hc/en-us/articles/24420554286868-Skills-APIs-and-integrations
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Public Course Catalog REST API
properties:
- type: Documentation
  url: https://help.pluralsight.com/hc/en-us/articles/24420554286868-Skills-APIs-and-integrations
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/public-course-catalog-rest.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: public-course-catalog-rest-api
source_filename: public-course-catalog-rest.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Public Course Catalog REST API\n  description: Legacy public REST API for accessing the full course catalog without authentication. Returns course IDs, titles, durations, release dates, and retirement status.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://paas-rest-api.pluralsight.com\n  description: Production\nexternalDocs:\n  description: Skills APIs and Integrations\n  url: https://help.pluralsight.com/hc/en-us/articles/24420554286868-Skills-APIs-and-integrations\ntags:\n- name: Catalog\n  description: Public course catalog operations\npaths:\n  /courses:\n    get:\n      summary: Pluralsight Get Course Catalog\n      description: Retrieve the full public course catalog without authentication. Returns course IDs, titles, durations,\
  \ release dates, and retirement status.\n      operationId: getCourseCatalog\n      tags:\n      - Catalog\n      responses:\n        '200':\n          description: Successful response with course catalog\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        id:\n                          type: string\n                          description: Course identifier\n                        title:\n                          type: string\n                          description: Course title\n                        duration:\n                          type: string\n                          description: Course duration\n                        releaseDate:\n                          type: string\n                          format: date\n  \
  \                        description: Course release date\n                        retiredDate:\n                          type: string\n                          format: date\n                          description: Course retirement date if applicable\n                    description: Course records\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/public-course-catalog-rest.yml
tags:
- Catalog
- Courses
- Legacy
- Public
---
