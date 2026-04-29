---
aid: codeproject:codeproject-api
baseURL: https://api.codeproject.com
description: OAuth 2.0 protected REST API providing read access to CodeProject articles, forum messages, questions, and authenticated user data (answers, articles, blog posts, bookmarks, notifications, profile, reputation, tips). Supports Client Credentials, Authorization Code, and Implicit Grant flows. Tokens are issued by the CodeProject identity server and presented as Bearer tokens in the Authorization header.
humanURL: https://api.codeproject.com/Help
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CodeProject REST API
properties:
- name: API Documentation
  type: Documentation
  url: https://api.codeproject.com/Help
- name: API Base URL
  type: BaseURL
  url: https://api.codeproject.com/
- name: API Samples
  type: Samples
  url: https://api.codeproject.com/Samples
- name: The CodeProject API - Part 1
  type: Article
  url: https://www.codeproject.com/Articles/986918/The-CodeProject-API-Part
- name: The CodeProject API - Part 2 Getting Some REST
  type: Article
  url: https://www.codeproject.com/articles/989081/the-code-project-api-part-getting-some-rest
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/codeproject/refs/heads/main/openapi/codeproject-rest-api-openapi.yml
provider_name: CodeProject
provider_slug: codeproject
slug: codeproject-api
source_yaml: "aid: codeproject:codeproject-api\nname: CodeProject REST API\ntags:\n- Articles\n- Community\n- Forum\n- OAuth2\n- Q&A\n- Read-Only\ntype: REST\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.codeproject.com\nhumanURL: https://api.codeproject.com/Help\ndescription: OAuth 2.0 protected REST API providing read access to CodeProject articles, forum messages,\n  questions, and authenticated user data (answers, articles, blog posts, bookmarks, notifications, profile,\n  reputation, tips). Supports Client Credentials, Authorization Code, and Implicit Grant flows. Tokens\n  are issued by the CodeProject identity server and presented as Bearer tokens in the Authorization header.\nproperties:\n- url: https://api.codeproject.com/Help\n  name: API Documentation\n  type: Documentation\n- url: https://api.codeproject.com/\n  name: API Base URL\n  type: BaseURL\n- url: https://api.codeproject.com/Samples\n  name: API Samples\n  type:\
  \ Samples\n- url: https://www.codeproject.com/Articles/986918/The-CodeProject-API-Part\n  name: The CodeProject API - Part 1\n  type: Article\n- url: https://www.codeproject.com/articles/989081/the-code-project-api-part-getting-some-rest\n  name: The CodeProject API - Part 2 Getting Some REST\n  type: Article\n- url: openapi/codeproject-rest-api-openapi.yml\n  type: OpenAPI\nx-features:\n- OAuth 2.0 Bearer Token authentication\n- Client Credentials, Authorization Code, and Implicit Grant flows\n- Read-only access to articles, forums, and Q&A\n- My endpoints for authenticated user data\n- Article rating filter (>= 3.0) on the public list\nx-use-cases:\n- Aggregating CodeProject articles into developer reading lists\n- Surfacing CodeProject Q&A in IDE assistants\n- Building user dashboards showing reputation and notifications\n- Periodic content sync into knowledge bases\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/codeproject/refs/heads/main/apis.yml
tags:
- Articles
- Community
- Forum
- OAuth2
- Q&A
- Read-Only
---
