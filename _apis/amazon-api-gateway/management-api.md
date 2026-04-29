---
aid: amazon-api-gateway:management-api
baseURL: https://{api-id}.execute-api.{region}.amazonaws.com/{stage}
description: API for directly managing runtime aspects of deployed APIs, including sending data to connected WebSocket clients via the @connections endpoint and managing connection state.
humanURL: https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-how-to-call-websocket-api-connections.html
image: https://a0.awsstatic.com/libra-css/images/logos/aws_logo_smile_1200x630.png
layout: api
name: Amazon API Gateway Management API
properties:
- type: Documentation
  url: https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-how-to-call-websocket-api-connections.html
provider_name: Amazon API Gateway
provider_slug: amazon-api-gateway
slug: management-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "name: Amazon API Gateway Management API\ndescription: API for directly managing runtime aspects of deployed APIs, including sending data to connected\n  WebSocket clients via the @connections endpoint and managing connection state.\nimage: https://a0.awsstatic.com/libra-css/images/logos/aws_logo_smile_1200x630.png\nhumanURL: https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-how-to-call-websocket-api-connections.html\nbaseURL: https://{api-id}.execute-api.{region}.amazonaws.com/{stage}\ntags:\n- Connections\n- Management\n- Runtime\n- WebSocket\nproperties:\n- type: Documentation\n  url: https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-how-to-call-websocket-api-connections.html\naid: amazon-api-gateway:management-api\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-api-gateway/refs/heads/main/apis.yml
tags:
- Connections
- Management
- Runtime
- WebSocket
---
