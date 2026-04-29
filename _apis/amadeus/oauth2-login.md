---
aid: amadeus:oauth2-login
baseURL: https://api.amadeus.com
description: The Amadeus OAuth2 Login API provides authentication for all Amadeus self- service APIs. It implements the OAuth 2.0 client credentials grant type, allowing applications to obtain access tokens required to make authenticated requests to any Amadeus API endpoint.
humanURL: https://developers.amadeus.com/self-service/apis-docs/guides/developer-guides/API-Keys/authorization
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Amadeus OAuth2 Login API
properties:
- type: Documentation
  url: https://developers.amadeus.com/self-service/apis-docs/guides/developer-guides/API-Keys/authorization
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/amadeus-oauth2-login-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/amadeus-oauth2-login-amadeusoauth2token-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/amadeus-oauth2-login-errorresponse-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/amadeus-oauth2-login-amadeusoauth2token-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/amadeus-oauth2-login-errorresponse-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-ld/amadeus-amadeus-oauth2-login-context.jsonld
provider_name: Amadeus
provider_slug: amadeus
slug: oauth2-login
source_filename: amadeus-oauth2-login-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  description: >\n    Amadeus for Developers uses OAuth2 to authenticate access requests. OAuth2\n    generates an access token which grants the client permission to access a\n    protected resource. The method to acquire a token is called grant. There are\n    different types of OAuth2 grants. Amadeus for Developers uses the Client\n    Credentials Grant.\n      https://developers.amadeus.com/self-service/apis-docs/guides/authorization-262\n  title: Amadeus OAuth2 Login\n  version: 1.0.0\nservers:\n- url: https://test.api.amadeus.com/v1\npaths:\n  /security/oauth2/token:\n    post:\n      description: >-\n        The token endpoint is used by the client to obtain an access token by\n        presenting its authorization grant.\n\n        To learn more about this endpoint please refer to the specification at\n        https://tools.ietf.org/html/rfc6749#section-3.2\n      tags:\n      - Security\n      summary: Amadeus the OAuth 2.0 Token Endpoint\n   \
  \   operationId: oauth2Token\n      requestBody:\n        content:\n          application/x-www-form-urlencoded:\n            schema:\n              type: object\n              properties:\n                grant_type:\n                  type: string\n                  example: client_credentials\n                client_id:\n                  type: string\n                client_secret:\n                  type: string\n              required:\n              - grant_type\n              - client_id\n              - client_secret\n      responses:\n        '200':\n          description: oauth2TokenResponse\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/AmadeusOAuth2Token'\n        '401':\n          description: genericError\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '500':\n          description: genericError\n         \
  \ content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n  /security/oauth2/token/{access_token}:\n    get:\n      description: Get token information\n      tags:\n      - Security\n      summary: Amadeus the OAuth 2.0 Token Info Endpoint\n      operationId: getOauth2TokenInfo\n      parameters:\n      - in: path\n        name: access_token\n        schema:\n          type: string\n        required: true\n      responses:\n        '200':\n          description: oauth2TokenResponse\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/AmadeusOAuth2Token'\n        '404':\n          description: genericError\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\ncomponents:\n  schemas:\n    AmadeusOAuth2Token:\n      description: The token response\n      type: object\n      properties:\n\
  \        type:\n          description: The access token issued by the authorization server.\n          type: string\n        username:\n          description: The user who requested the access_token\n          type: string\n        application_name:\n          description: The application which is requested the access_token\n          type: string\n        client_id:\n          description: The client_id is a public identifier for apps\n          type: string\n        token_type:\n          description: >-\n            token_type is a parameter in Access Token generate call to\n            Authorization server, which essentially represents how an\n            access_token will be generated and presented for resource access\n            calls\n          type: string\n        access_token:\n          description: >-\n            Access tokens are a String which applications use to make API\n            requests on behalf of a user.\n          type: string\n        expires_in:\n         \
  \ description: The lifetime in seconds of the access token\n          type: integer\n          format: int64\n        state:\n          description: The state\n          type: string\n        scope:\n          description: >-\n            Scope is a mechanism in OAuth 2.0 to limit an application's access\n            to a user's account\n          type: string\n      example:\n        type: amadeusOAuth2Token\n        username: myuser@mydomain.com\n        application_name: My Application\n        client_id: Hs0sNkpTXeu0t2Hw2rLITofK8QELGdfsf\n        token_type: Bearer\n        access_token: f8XgboI1oKyNw7w23bnnAbFANidfgC\n        expires_in: 1799\n        state: approved\n        scope: ''\n    ErrorResponse:\n      description: >-\n        Error responses are sent when an error (e.g. unauthorized, bad request,\n        ...) occurred.\n      type: object\n      title: ErrorResponse\n      required:\n      - error\n      - error_description\n      - code\n      - title\n      properties:\n\
  \        error:\n          description: Name is the error name.\n          type: string\n        error_description:\n          description: A small description about the error\n          type: string\n        code:\n          description: Debug contains debug information.\n          type: integer\n          format: int64\n        title:\n          description: >-\n            Debug contains debug information. This is usually not available and\n            has to be enabled.\n          type: string\n      example:\n        error: invalid_client\n        error_description: Client credentials are invalid\n        code: 38187\n        title: Invalid parameters\ntags:\n- name: Security\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/amadeus-oauth2-login-openapi.yaml
tags:
- Authentication
- OAuth
- Security
---
