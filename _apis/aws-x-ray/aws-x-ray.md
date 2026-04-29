---
aid: aws-x-ray:aws-x-ray
baseURL: https://xray.{region}.amazonaws.com
description: AWS X-Ray is a service that helps developers analyze and debug distributed applications by providing end-to-end tracing of requests as they travel through the application, identifying performance bottlenecks and errors. It is now part of Amazon CloudWatch Application Signals for unified observability.
humanURL: https://aws.amazon.com/xray/
image: ''
layout: api
name: AWS X-Ray
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aws-x-ray/refs/heads/main/openapi/aws-x-ray-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/aws-x-ray/refs/heads/main/json-schema/aws-x-ray-trace-segment.yml
- type: Documentation
  url: https://docs.aws.amazon.com/xray/latest/devguide/aws-xray.html
- type: APIReference
  url: https://docs.aws.amazon.com/xray/latest/api/Welcome.html
provider_name: AWS X-Ray
provider_slug: aws-x-ray
slug: aws-x-ray
source_yaml: "aid: aws-x-ray:aws-x-ray\nname: AWS X-Ray\ndescription: AWS X-Ray is a service that helps developers analyze and debug distributed applications by\n  providing end-to-end tracing of requests as they travel through the application, identifying performance\n  bottlenecks and errors. It is now part of Amazon CloudWatch Application Signals for unified observability.\nhumanURL: https://aws.amazon.com/xray/\nbaseURL: https://xray.{region}.amazonaws.com\ntags:\n- AWS\n- Debugging\n- Distributed Tracing\n- Microservices\n- Observability\nproperties:\n- type: OpenAPI\n  url: openapi/aws-x-ray-openapi.yml\n- type: JSONSchema\n  url: json-schema/aws-x-ray-trace-segment.yml\n- type: Documentation\n  url: https://docs.aws.amazon.com/xray/latest/devguide/aws-xray.html\n- type: APIReference\n  url: https://docs.aws.amazon.com/xray/latest/api/Welcome.html\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aws-x-ray/refs/heads/main/apis.yml
tags:
- AWS
- Debugging
- Distributed Tracing
- Microservices
- Observability
---
