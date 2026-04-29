---
aid: palo-alto-networks:cloud-ngfw-api
baseURL: https://api.{region}.aws.cloudngfw.paloaltonetworks.com
description: REST APIs for managing Palo Alto Networks Cloud NGFW, a cloud-native managed firewall service available on AWS and Azure. The API supports creating and managing firewall resources, configuring security rules and rule stacks, managing FQDN lists and prefix lists, and retrieving firewall logs. On AWS, authentication uses IAM roles; on Azure, authentication uses Azure Active Directory.
humanURL: https://pan.dev/cloudngfw/aws/api/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cloud NGFW API
properties:
- type: Documentation
  url: https://pan.dev/cloudngfw/aws/api/
- type: GettingStarted
  url: https://pan.dev/cloudngfw/docs/getstarted_azure/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-cloud-ngfw-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-firewall-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-firewall-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-firewall-summary-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-fqdn-list-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-fqdn-list-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-fqdn-list-summary-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-prefix-list-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-prefix-list-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-prefix-list-summary-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-response-status-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-rule-destination-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-rule-source-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-rule-stack-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-rule-stack-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-rule-stack-summary-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-security-rule-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-security-rule-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-ngfw-api-security-rule-summary-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-firewall-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-firewall-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-firewall-summary-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-fqdn-list-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-fqdn-list-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-fqdn-list-summary-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-prefix-list-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-prefix-list-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-prefix-list-summary-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-response-status-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-rule-destination-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-rule-source-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-rule-stack-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-rule-stack-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-rule-stack-summary-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-security-rule-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-security-rule-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-ngfw-api-security-rule-summary-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-cloud-ngfw-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-firewall-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-firewall-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-firewall-summary-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-fqdn-list-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-fqdn-list-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-fqdn-list-summary-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-prefix-list-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-prefix-list-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-prefix-list-summary-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-response-status-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-rule-destination-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-rule-source-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-rule-stack-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-rule-stack-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-rule-stack-summary-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-security-rule-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-security-rule-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-ngfw-api-security-rule-summary-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: cloud-ngfw-api
source_yaml: "aid: palo-alto-networks:cloud-ngfw-api\nname: Cloud NGFW API\ntags:\n- AWS\n- Azure\n- Cloud Security\n- Cloud-Native Firewall\n- Managed Service\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.{region}.aws.cloudngfw.paloaltonetworks.com\nhumanURL: https://pan.dev/cloudngfw/aws/api/\nproperties:\n- url: https://pan.dev/cloudngfw/aws/api/\n  type: Documentation\n- url: https://pan.dev/cloudngfw/docs/getstarted_azure/\n  type: GettingStarted\n- url: openapi/palo-alto-cloud-ngfw-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/cloud-ngfw-api-firewall-request-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-firewall-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-firewall-summary-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-fqdn-list-request-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-fqdn-list-schema.json\n  type: JSONSchema\n\
  - url: json-schema/cloud-ngfw-api-fqdn-list-summary-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-prefix-list-request-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-prefix-list-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-prefix-list-summary-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-response-status-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-rule-destination-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-rule-source-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-rule-stack-request-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-rule-stack-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-rule-stack-summary-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-security-rule-request-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-ngfw-api-security-rule-schema.json\n  type: JSONSchema\n\
  - url: json-schema/cloud-ngfw-api-security-rule-summary-schema.json\n  type: JSONSchema\n- url: json-structure/cloud-ngfw-api-firewall-request-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-firewall-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-firewall-summary-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-fqdn-list-request-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-fqdn-list-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-fqdn-list-summary-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-prefix-list-request-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-prefix-list-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-prefix-list-summary-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-response-status-structure.json\n  type: JSONStructure\n\
  - url: json-structure/cloud-ngfw-api-rule-destination-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-rule-source-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-rule-stack-request-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-rule-stack-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-rule-stack-summary-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-security-rule-request-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-security-rule-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-ngfw-api-security-rule-summary-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-cloud-ngfw-api-context.jsonld\n  type: JSON-LD\n- url: examples/cloud-ngfw-api-firewall-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-firewall-request-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-firewall-summary-example.json\n\
  \  type: Example\n- url: examples/cloud-ngfw-api-fqdn-list-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-fqdn-list-request-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-fqdn-list-summary-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-prefix-list-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-prefix-list-request-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-prefix-list-summary-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-response-status-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-rule-destination-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-rule-source-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-rule-stack-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-rule-stack-request-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-rule-stack-summary-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-security-rule-example.json\n\
  \  type: Example\n- url: examples/cloud-ngfw-api-security-rule-request-example.json\n  type: Example\n- url: examples/cloud-ngfw-api-security-rule-summary-example.json\n  type: Example\ndescription: REST APIs for managing Palo Alto Networks Cloud NGFW, a cloud-native managed firewall service\n  available on AWS and Azure. The API supports creating and managing firewall resources, configuring security\n  rules and rule stacks, managing FQDN lists and prefix lists, and retrieving firewall logs. On AWS, authentication\n  uses IAM roles; on Azure, authentication uses Azure Active Directory.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- AWS
- Azure
- Cloud Security
- Cloud-Native Firewall
- Managed Service
---
