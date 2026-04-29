---
aid: amazon-b2b-data-interchange:aws-b2b-data-interchange-api
baseURL: https://b2bi.us-east-1.amazonaws.com
description: The AWS B2B Data Interchange API provides programmatic access to manage EDI transformation workflows, trading partner profiles, capabilities, partnerships, and transformers. It enables creation and management of inbound and outbound EDI pipelines using X12 standards and supports AI-assisted mapping template generation via Amazon Bedrock.
humanURL: https://docs.aws.amazon.com/b2bi/latest/APIReference/api-welcome.html
image: ''
layout: api
name: AWS B2B Data Interchange API
properties:
- type: Documentation
  url: https://docs.aws.amazon.com/b2bi/latest/APIReference/api-welcome.html
- type: Documentation
  url: https://docs.aws.amazon.com/b2bi/latest/userguide/what-is-b2bi.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/openapi/aws-b2b-data-interchange-api-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-schema/profile.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-schema/partnership.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-schema/transformer.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-structure/b2bi-resource-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-ld/context.jsonld
- type: SpectralRuleset
  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/spectral/ruleset.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/capabilities/capabilities.yml
- type: Vocabulary
  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/vocabulary/vocabulary.yml
provider_name: Amazon B2B Data Interchange
provider_slug: amazon-b2b-data-interchange
slug: aws-b2b-data-interchange-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: amazon-b2b-data-interchange:aws-b2b-data-interchange-api\nname: AWS B2B Data Interchange API\ndescription: The AWS B2B Data Interchange API provides programmatic access to manage EDI transformation\n  workflows, trading partner profiles, capabilities, partnerships, and transformers. It enables creation\n  and management of inbound and outbound EDI pipelines using X12 standards and supports AI-assisted mapping\n  template generation via Amazon Bedrock.\nhumanURL: https://docs.aws.amazon.com/b2bi/latest/APIReference/api-welcome.html\nbaseURL: https://b2bi.us-east-1.amazonaws.com\ntags:\n- EDI\n- B2B\n- Transformation\n- X12\n- Trading Partners\n- Capabilities\n- Profiles\n- Partnerships\n- Transformers\nproperties:\n- type: Documentation\n  url: https://docs.aws.amazon.com/b2bi/latest/APIReference/api-welcome.html\n- type: Documentation\n  url: https://docs.aws.amazon.com/b2bi/latest/userguide/what-is-b2bi.html\n- type: OpenAPI\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/openapi/aws-b2b-data-interchange-api-openapi.yml\n\
  - type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-schema/profile.json\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-schema/partnership.json\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-schema/transformer.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-structure/b2bi-resource-structure.json\n- type: JSONLD\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/json-ld/context.jsonld\n- type: SpectralRuleset\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/spectral/ruleset.yml\n- type: Capabilities\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/capabilities/capabilities.yml\n\
  - type: Vocabulary\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/vocabulary/vocabulary.yml\ncontact:\n- FN: AWS Support\n  url: https://aws.amazon.com/contact-us/\nfeatures:\n- name: EDI Transformation\n  description: Transform X12 EDI documents to JSON or XML and generate EDI from JSON/XML data inputs,\n    automating inbound and outbound EDI workflows.\n- name: AI-Assisted Mapping\n  description: Use Amazon Bedrock to automatically generate mapping templates, reducing mapping code development\n    time by up to 50%.\n- name: Trading Partner Management\n  description: Onboard and manage trading partners through profiles, capabilities, and partnerships with\n    visibility into transactional communications.\n- name: EDI Splitting\n  description: Split inbound X12 EDI documents containing multiple transactions into individually processed\n    single-transaction documents, supporting files up to 5GB.\n- name: HIPAA Compliance\n  description:\
  \ Supports secure exchange of protected health information for healthcare EDI workflows in\n    compliance with HIPAA requirements.\nuseCases:\n- name: Supply Chain Partner Onboarding\n  description: Automate onboarding of trading partners in supply chain networks, enabling rapid EDI integration\n    without custom development.\n- name: Healthcare Claims Processing\n  description: Streamline healthcare enrollment and claims processing workflows using X12 EDI standards\n    with HIPAA-compliant data exchange.\n- name: Financial Transaction Processing\n  description: Expedite complex financial transactions like mortgage applications and tax assessments\n    through automated EDI transformation.\nintegrations:\n- name: AWS Transfer Family\n  description: Integrate with AWS Transfer Family for managed file transfer ingestion workflows into the\n    B2B Data Interchange pipeline.\n- name: Amazon S3\n  description: Monitor S3 locations for inbound EDI documents and write transformed outputs\
  \ to S3 buckets\n    for downstream processing.\n- name: Amazon EventBridge\n  description: Trigger event-driven workflows from EDI transformation events using Amazon EventBridge\n    integration.\n- name: Amazon Bedrock\n  description: Leverage Amazon Bedrock generative AI for automated mapping template generation from source\n    and target schemas.\nsolutions:\n- name: EDI Modernization\n  description: Migrate from legacy EDI infrastructure to a cloud-native managed service with pay-as-you-go\n    pricing and no upfront investment.\n- name: Multi-Partner EDI Network\n  description: Build and manage multi-partner EDI networks with centralized visibility and standardized\n    transformation pipelines.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-b2b-data-interchange/refs/heads/main/apis.yml
tags:
- EDI
- B2B
- Transformation
- X12
- Trading Partners
- Capabilities
- Profiles
- Partnerships
- Transformers
---
