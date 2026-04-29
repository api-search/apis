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
source_filename: codeproject-rest-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CodeProject REST API\n  description: >-\n    CodeProject's REST API at api.codeproject.com provides read access to\n    articles, forum messages, questions, and authenticated user profile data\n    from the codeproject.com developer community. Authentication uses OAuth 2.0\n    Bearer Tokens via Client Credentials, Authorization Code, or Implicit Grant\n    flows. The \"My\" API set requires the Authorization Code or Implicit Grant\n    flows because it accesses the signed-in user's resources, while the\n    Articles, ForumMessages, and Questions endpoints can be accessed with a\n    Client Credentials token. Tokens are sent in the Authorization header.\n  version: '1.0-beta'\n  contact:\n    name: CodeProject API Support\n    url: https://api.codeproject.com/Help\nexternalDocs:\n  description: CodeProject API Help\n  url: https://api.codeproject.com/Help\nservers:\n  - url: https://api.codeproject.com\n    description: CodeProject Resource Server\n\
  tags:\n  - name: Articles\n    description: Articles, technical blogs, and tips and tricks (rating >= 3.0).\n  - name: ForumMessages\n    description: Latest messages for a forum or message thread.\n  - name: Questions\n    description: Q&A questions (new, active, unanswered).\n  - name: My\n    description: Authenticated user resources (answers, articles, blogs, bookmarks, notifications, profile, reputation, tips).\nsecurity:\n  - oauth2: [read]\npaths:\n  /v1/Articles:\n    get:\n      operationId: listArticles\n      summary: List the latest articles\n      description: Retrieve the latest articles, technical blogs, and tips & tricks (rating >= 3.0), ordered by modified date.\n      tags: [Articles]\n      parameters:\n        - name: page\n          in: query\n          schema:\n            type: integer\n            minimum: 1\n        - name: minRating\n          in: query\n          schema:\n            type: number\n            format: float\n      responses:\n        '200':\n\
  \          description: Article list\n  /v1/Articles/{id}:\n    get:\n      operationId: getArticle\n      summary: Get a single article\n      tags: [Articles]\n      parameters:\n        - name: id\n          in: path\n          required: true\n          schema:\n            type: integer\n      responses:\n        '200':\n          description: Article detail\n        '404':\n          description: Not found\n  /v1/ForumMessages/{forumId}:\n    get:\n      operationId: listForumMessages\n      summary: List the latest messages for a forum\n      tags: [ForumMessages]\n      parameters:\n        - name: forumId\n          in: path\n          required: true\n          schema:\n            type: integer\n        - name: page\n          in: query\n          schema:\n            type: integer\n            minimum: 1\n      responses:\n        '200':\n          description: Forum messages\n  /v1/Questions:\n    get:\n      operationId: listQuestions\n      summary: List Q&A questions\n  \
  \    tags: [Questions]\n      parameters:\n        - name: filter\n          in: query\n          description: Filter set - new, active, unanswered.\n          schema:\n            type: string\n            enum: [new, active, unanswered]\n        - name: page\n          in: query\n          schema:\n            type: integer\n            minimum: 1\n      responses:\n        '200':\n          description: Question list\n  /v1/Questions/{id}:\n    get:\n      operationId: getQuestion\n      summary: Get a question and its answers\n      tags: [Questions]\n      parameters:\n        - name: id\n          in: path\n          required: true\n          schema:\n            type: integer\n      responses:\n        '200':\n          description: Question detail\n  /v1/My/Profile:\n    get:\n      operationId: getMyProfile\n      summary: Get the authenticated user's profile\n      tags: [My]\n      security:\n        - oauth2: [read]\n      responses:\n        '200':\n          description:\
  \ Profile\n        '401':\n          description: Unauthorized\n  /v1/My/Reputation:\n    get:\n      operationId: getMyReputation\n      summary: Get the authenticated user's reputation\n      tags: [My]\n      security:\n        - oauth2: [read]\n      responses:\n        '200':\n          description: Reputation\n        '401':\n          description: Unauthorized\n  /v1/My/Articles:\n    get:\n      operationId: listMyArticles\n      summary: List the authenticated user's articles\n      tags: [My]\n      security:\n        - oauth2: [read]\n      responses:\n        '200':\n          description: Articles\n        '401':\n          description: Unauthorized\n  /v1/My/Answers:\n    get:\n      operationId: listMyAnswers\n      summary: List the authenticated user's answers\n      tags: [My]\n      security:\n        - oauth2: [read]\n      responses:\n        '200':\n          description: Answers\n        '401':\n          description: Unauthorized\n  /v1/My/Blog:\n    get:\n    \
  \  operationId: listMyBlogPosts\n      summary: List the authenticated user's blog posts\n      tags: [My]\n      security:\n        - oauth2: [read]\n      responses:\n        '200':\n          description: Blog posts\n        '401':\n          description: Unauthorized\n  /v1/My/Bookmarks:\n    get:\n      operationId: listMyBookmarks\n      summary: List the authenticated user's bookmarks\n      tags: [My]\n      security:\n        - oauth2: [read]\n      responses:\n        '200':\n          description: Bookmarks\n        '401':\n          description: Unauthorized\n  /v1/My/Notifications:\n    get:\n      operationId: listMyNotifications\n      summary: List the authenticated user's notifications\n      tags: [My]\n      security:\n        - oauth2: [read]\n      responses:\n        '200':\n          description: Notifications\n        '401':\n          description: Unauthorized\n  /v1/My/Tips:\n    get:\n      operationId: listMyTips\n      summary: List the authenticated user's\
  \ tips\n      tags: [My]\n      security:\n        - oauth2: [read]\n      responses:\n        '200':\n          description: Tips\n        '401':\n          description: Unauthorized\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: oauth2\n      description: >-\n        OAuth 2.0 Bearer Tokens are issued by the CodeProject identity server.\n        Use Client Credentials Grant for read access to public resources and\n        Authorization Code Grant or Implicit Grant for the My API.\n      flows:\n        clientCredentials:\n          tokenUrl: https://api.codeproject.com/Token\n          scopes:\n            read: Read access to public resources\n        authorizationCode:\n          authorizationUrl: https://api.codeproject.com/Authorize\n          tokenUrl: https://api.codeproject.com/Token\n          scopes:\n            read: Read access to public and user-owned resources\n        implicit:\n          authorizationUrl: https://api.codeproject.com/Authorize\n          scopes:\n\
  \            read: Read access to public and user-owned resources\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/codeproject/refs/heads/main/openapi/codeproject-rest-api-openapi.yml
tags:
- Articles
- Community
- Forum
- OAuth2
- Q&A
- Read-Only
---
