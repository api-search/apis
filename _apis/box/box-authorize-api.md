---
aid: box:box-authorize-api
baseURL: https://account.box.com/api/oauth2
description: The Box Authorize API initiates the OAuth 2.0 authorization flow by redirecting users to the Box website to grant permission for applications to act on their behalf, providing the first step in authenticating users with Box.
humanURL: https://developer.box.com/reference/get-authorize
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Box Authorize API
properties:
- type: Documentation
  url: https://developer.box.com/reference/get-authorize
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/box/refs/heads/main/openapi/authorize-openapi-original.yml
provider_name: Box
provider_slug: box
slug: box-authorize-api
source_filename: authorize-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Box Authorize API\n  description: Needs a description.\npaths:\n  /authorize:\n    get:\n      operationId: get_authorize\n      summary: Box Authorize user\n      description: |-\n        Authorize a user by sending them through the [Box](https://box.com)\n        website and request their permission to act on their behalf.\n\n        This is the first step when authenticating a user using\n        OAuth 2.0. To request a user's authorization to use the Box APIs\n        on their behalf you will need to send a user to the URL with this\n        format.\n      tags:\n        - Authorize\n      x-box-tag: authorization\n      security: []\n      servers:\n        - url: https://account.box.com/api/oauth2\n          description: Server for client-side authentication\n      parameters:\n        - name: response_type\n          description: The type of response we'd like to receive.\n          in: query\n          example: code\n          required:\
  \ true\n          schema:\n            type: string\n            format: token\n            enum:\n              - code\n        - name: client_id\n          description: >-\n            The Client ID of the application that is requesting to authenticate\n\n            the user. To get the Client ID for your application, log in to your\n\n            Box developer console and click the **Edit Application** link for\n\n            the application you're working with. In the OAuth 2.0 Parameters\n            section\n\n            of the configuration page, find the item labelled `client_id`. The\n\n            text of that item is your application's Client ID.\n          in: query\n          example: ly1nj6n11vionaie65emwzk575hnnmrk\n          required: true\n          schema:\n            type: string\n        - name: redirect_uri\n          description: >-\n            The URI to which Box redirects the browser after the user has\n            granted\n\n            or denied the application\
  \ permission. This URI match one of the\n            redirect\n\n            URIs in the configuration of your application. It must be a\n\n            valid HTTPS URI and it needs to be able to handle the redirection to\n\n            complete the next step in the OAuth 2.0 flow.\n\n            Although this parameter is optional, it must be a part of the\n\n            authorization URL if you configured multiple redirect URIs\n\n            for the application in the developer console. A missing parameter\n            causes\n\n            a `redirect_uri_missing` error after the user grants application\n            access.\n          in: query\n          example: http://example.com/auth/callback\n          required: false\n          schema:\n            type: string\n            format: url\n        - name: state\n          description: |-\n            A custom string of your choice. Box will pass the same string to\n            the redirect URL when authentication is complete. This\
  \ parameter\n            can be used to identify a user on redirect, as well as protect\n            against hijacked sessions and other exploits.\n          in: query\n          example: my_state\n          required: false\n          schema:\n            type: string\n        - name: scope\n          description: >-\n            A space-separated list of application scopes you'd like to\n\n            authenticate the user for. This defaults to all the scopes\n            configured\n\n            for the application in its configuration page.\n          in: query\n          example: admin_readwrite\n          required: false\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Does not return any data, but rather should be used in the browser.\n          content:\n            text/html:\n              schema:\n                type: string\n                format: html\n        default:\n          description: Does not return any data,\
  \ but rather should be used in the browser.\n          content:\n            text/html:\n              schema:\n                type: string\n                format: html\ncomponents:\n  schemas: {}\ntags:\n  - name: Authorize\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/box/refs/heads/main/openapi/authorize-openapi-original.yml
tags:
- Authentication
- Authorization
- OAuth
---
