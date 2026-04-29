---
aid: github:github-zen-api
baseURL: ''
description: The GitHub Zen API is a playful REST endpoint that returns a random aphorism from the Zen of GitHub, such as Keep it logically awesome. Each request to GET https://api.github.com/zen responds with a single plain-text line, making it useful for quick connectivity checks, demoing HTTP calls, or verifying authentication. It doesnt require auth, but you can include a token to benefit from higher rate limits.
humanURL: ''
image: ''
layout: api
name: GitHub Zen API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-zen-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/meta/meta
provider_name: GitHub
provider_slug: github
slug: github-zen-api
source_filename: github-zen-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  version: 1.1.4\n  title: GitHub Zen API\n  description: >-\n    The GitHub Zen API is a simple, lighthearted endpoint that returns a random\n    piece of philosophical or inspirational wisdom from GitHub's design\n    philosophy when called. This playful API serves no functional purpose in\n    application development but instead offers a moment of reflection, often\n    sharing pithy sayings about software development, collaboration, or design\n    principles that embody GitHub's cultural values. Developers sometimes use it\n    as a simple test endpoint to verify API connectivity, as an Easter egg in\n    applications, or simply to get a bit of inspiration during their coding\n    sessions—it's GitHub's way of adding a human touch to their technical\n    platform.\n  license:\n    name: MIT\n    url: https://spdx.org/licenses/MIT\n  termsOfService: https://docs.github.com/articles/github-terms-of-service\n  contact:\n    name: Support\n    url: https://support.github.com/contact?tags=dotcom-rest-api\n\
  \  x-github-plan: ghes\n  x-github-release: 3.9\ntags:\n- name: Get\n- name: Zen\nservers:\n- url: '{protocol}://{hostname}/api/v3'\n  variables:\n    hostname:\n      description: Self-hosted Enterprise Server hostname\n      default: HOSTNAME\n    protocol:\n      description: Self-hosted Enterprise Server protocol\n      default: http\nexternalDocs:\n  description: GitHub Enterprise Developer Docs\n  url: https://docs.github.com/enterprise-server@3.9/rest/\npaths:\n  /zen:\n    get:\n      summary: GitHub Get the Zen of Github\n      description: Get a random sentence from the Zen of GitHub\n      tags:\n      - Get\n      - Zen\n      operationId: getTheZenOfGithub\n      externalDocs:\n        description: API method documentation\n        url: >-\n          https://docs.github.com/enterprise-server@3.9/rest/meta/meta#get-the-zen-of-github\n      responses:\n        '200':\n          description: Response\n          content:\n            application/json:\n              schema:\n\
  \                type: string\n              examples:\n                default:\n                  summary: Example response\n                  value: Responsive is better than fast\n      x-github:\n        githubCloudOnly: false\n        enabledForGitHubApps: true\n        category: meta\n        subcategory: meta\n      security:\n      - bearerHttpAuthentication: []\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  examples: {}\n  reponses: {}\n  parameters: {}\n  schemas: {}\n  responses: {}\n  headers: {}\n  securitySchemes:\n    bearerHttpAuthentication:\n      description: Bearer Token\n      type: http\n      scheme: Bearer\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-zen-openapi.yml
tags:
- Zen
---
