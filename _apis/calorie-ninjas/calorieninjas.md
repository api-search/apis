---
aid: calorie-ninjas:calorieninjas
baseURL: https://api.calorieninjas.com/v1
description: 'The CalorieNinjas API returns nutrition and recipe data for 100,000+ foods and beverages. It offers three endpoints: GET /nutrition for natural-language nutrition lookups (returns calories, macros, vitamins, and minerals), POST /imagetextnutrition for extracting nutrition from images containing food/beverage text, and GET /recipe for searching recipes with titles, ingredients, servings, and instructions. All requests authenticate with an API key sent in the X-Api-Key header.'
humanURL: https://calorieninjas.com/api
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CalorieNinjas API
properties:
- type: Documentation
  url: https://calorieninjas.com/api
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/calorie-ninjas/refs/heads/main/openapi/calorieninjas-openapi.yml
- type: Review
  url: https://raw.githubusercontent.com/api-evangelist/calorie-ninjas/refs/heads/main/openapi/calorieninjas-openapi-review.yml
provider_name: CalorieNinjas
provider_slug: calorie-ninjas
slug: calorieninjas
source_filename: calorieninjas-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CalorieNinjas\n  description: Get nutrition and recipe data for 100,000  foods and beverages.\n  version: 1.0.0\nservers:\n  - url: https://api.calorieninjas.com/v1\npaths:\n  /nutrition:\n    get:\n      summary: CalorieNinjas Get nutrition information\n      description: >-\n        Retrieve a detailed list of nutrition information for items based on a\n        query.\n      parameters:\n        - name: query\n          in: query\n          description: >-\n            A string containing food or drink items. Prefix a quantity before an\n            item to calculate for that quantity. Default is 100 grams if\n            unspecified.\n          required: true\n          schema:\n            type: string\n            maxLength: 1500\n      responses:\n        '200':\n          description: Successful response containing nutrition information.\n          content:\n            application/json:\n              schema:\n                type: object\n\
  \                properties:\n                  items:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        sugar_g:\n                          type: number\n                        fiber_g:\n                          type: number\n                        serving_size_g:\n                          type: number\n                        sodium_mg:\n                          type: number\n                        name:\n                          type: string\n                        potassium_mg:\n                          type: number\n                        fat_saturated_g:\n                          type: number\n                        fat_total_g:\n                          type: number\n                        calories:\n                          type: number\n                        cholesterol_mg:\n                          type: number\n                        protein_g:\n    \
  \                      type: number\n                        carbohydrates_total_g:\n                          type: number\n        '400':\n          description: Bad request.\n        '401':\n          description: Unauthorized.\n      security:\n        - ApiKeyAuth: []\n      tags:\n        - Nutrition\n  /imagetextnutrition:\n    post:\n      summary: CalorieNinjas Get nutrition information from an image\n      description: >-\n        Analyze an image containing food/beverage text to get nutrition\n        information.\n      requestBody:\n        required: true\n        content:\n          multipart/form-data:\n            schema:\n              type: object\n              properties:\n                media:\n                  type: string\n                  format: binary\n      responses:\n        '200':\n          description: Successful response containing nutrition information.\n        '400':\n          description: Bad request.\n        '401':\n          description: Unauthorized.\n\
  \      security:\n        - ApiKeyAuth: []\n      tags:\n        - Imagetextnutrition\n  /recipe:\n    get:\n      summary: CalorieNinjas Get recipes\n      description: Retrieve a list of recipes matching the search query.\n      parameters:\n        - name: query\n          in: query\n          description: A string containing a dish name. Partial match is supported.\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Successful response containing recipe information.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  type: object\n                  properties:\n                    title:\n                      type: string\n                    ingredients:\n                      type: string\n                    servings:\n                      type: string\n                    instructions:\n                    \
  \  type: string\n        '400':\n          description: Bad request.\n        '401':\n          description: Unauthorized.\n      security:\n        - ApiKeyAuth: []\n      tags:\n        - Recipe\ncomponents:\n  securitySchemes:\n    ApiKeyAuth:\n      type: apiKey\n      in: header\n      name: X-Api-Key\ntags:\n  - name: Imagetextnutrition\n  - name: Nutrition\n  - name: Recipe\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/calorie-ninjas/refs/heads/main/openapi/calorieninjas-openapi.yml
tags:
- Beverages
- Foods
- Image Recognition
- Nutrition
- Recipes
---
