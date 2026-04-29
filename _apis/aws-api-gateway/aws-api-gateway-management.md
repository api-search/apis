---
aid: aws-api-gateway:aws-api-gateway-management
baseURL: https://{api-id}.execute-api.{region}.amazonaws.com/{stage}
description: The API Gateway Management API allows backend services to send messages to connected clients of a deployed WebSocket API and to disconnect clients. Requests are made against the deployed stage's callback URL.
humanURL: https://docs.aws.amazon.com/apigatewaymanagementapi/latest/reference/Welcome.html
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Amazon API Gateway Management API
properties:
- type: Documentation
  url: https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-how-to-call-websocket-api-connections.html
- type: APIReference
  url: https://docs.aws.amazon.com/apigatewaymanagementapi/latest/reference/Welcome.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aws-api-gateway/refs/heads/main/openapi/aws-api-gateway-management-openapi.yml
provider_name: Amazon API Gateway
provider_slug: aws-api-gateway
slug: aws-api-gateway-management
source_yaml: "aid: aws-api-gateway:aws-api-gateway-management\nname: Amazon API Gateway Management API\ndescription: The API Gateway Management API allows backend services to send messages to connected clients\n  of a deployed WebSocket API and to disconnect clients. Requests are made against the deployed stage's\n  callback URL.\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://docs.aws.amazon.com/apigatewaymanagementapi/latest/reference/Welcome.html\nbaseURL: https://{api-id}.execute-api.{region}.amazonaws.com/{stage}\ntags:\n- API Gateway\n- AWS\n- Callback\n- WebSocket\nproperties:\n- type: Documentation\n  url: https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-how-to-call-websocket-api-connections.html\n- type: APIReference\n  url: https://docs.aws.amazon.com/apigatewaymanagementapi/latest/reference/Welcome.html\n- type: OpenAPI\n  url: openapi/aws-api-gateway-management-openapi.yml\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aws-api-gateway/refs/heads/main/apis.yml
tags:
- API Gateway
- AWS
- Callback
- WebSocket
---
