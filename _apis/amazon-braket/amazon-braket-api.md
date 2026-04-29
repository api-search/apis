---
aid: amazon-braket:amazon-braket-api
baseURL: https://braket.us-east-1.amazonaws.com
description: The Amazon Braket API provides programmatic access to quantum computing resources including quantum task execution on QPUs and simulators, hybrid quantum-classical job management, device discovery, and spending limit management.
humanURL: https://aws.amazon.com/braket/
image: ''
layout: api
name: Amazon Braket API
properties:
- type: Documentation
  url: https://docs.aws.amazon.com/braket/latest/APIReference/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/openapi/amazon-braket-api-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/json-schema/braket-task-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/json-structure/braket-resource-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/json-ld/context.jsonld
- type: SpectralRuleset
  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/spectral/ruleset.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/capabilities/capabilities.yml
- type: Vocabulary
  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/vocabulary/vocabulary.yml
provider_name: Amazon Braket
provider_slug: amazon-braket
slug: amazon-braket-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: amazon-braket:amazon-braket-api\nname: Amazon Braket API\ndescription: The Amazon Braket API provides programmatic access to quantum computing resources including\n  quantum task execution on QPUs and simulators, hybrid quantum-classical job management, device discovery,\n  and spending limit management.\nhumanURL: https://aws.amazon.com/braket/\nbaseURL: https://braket.us-east-1.amazonaws.com\ntags:\n- Quantum Computing\n- QPU\n- Quantum Tasks\n- Hybrid Jobs\n- Simulators\nproperties:\n- type: Documentation\n  url: https://docs.aws.amazon.com/braket/latest/APIReference/\n- type: OpenAPI\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/openapi/amazon-braket-api-openapi.yml\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/json-schema/braket-task-schema.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/json-structure/braket-resource-structure.json\n\
  - type: JSONLD\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/json-ld/context.jsonld\n- type: SpectralRuleset\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/spectral/ruleset.yml\n- type: Capabilities\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/capabilities/capabilities.yml\n- type: Vocabulary\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/vocabulary/vocabulary.yml\ncontact:\n- FN: AWS Support\n  url: https://aws.amazon.com/contact-us/\nfeatures:\n- name: Quantum Task Execution\n  description: Submit quantum circuits to QPU devices or simulators as quantum tasks, with results stored\n    in Amazon S3.\n- name: Hybrid Jobs\n  description: Run hybrid quantum-classical algorithms with managed classical compute resources and priority\n    QPU access.\n- name: Device Discovery\n  description: Search and retrieve details about available\
  \ quantum devices including QPUs from multiple\n    providers and simulators.\n- name: Multiple QPU Providers\n  description: Access quantum hardware from IonQ, Rigetti, QuEra, Oxford Quantum Circuits, IQM, and other\n    providers through a unified API.\n- name: Quantum Simulators\n  description: Use high-performance local and managed simulators (SV1, DM1, TN1) for circuit testing before\n    running on QPUs.\n- name: Spending Limits\n  description: Create and manage spending limits to control QPU and simulator usage costs at the account\n    level.\n- name: Pulse Control\n  description: Access native gate-level pulse control for advanced quantum hardware calibration and experimentation.\nuseCases:\n- name: Quantum Algorithm Research\n  description: Develop and test quantum algorithms on simulators before running on QPU hardware across\n    multiple providers.\n- name: Quantum Machine Learning\n  description: Run quantum-classical hybrid ML algorithms combining quantum circuits with classical\
  \ optimization\n    using Braket Hybrid Jobs.\n- name: Quantum Chemistry Simulation\n  description: Simulate molecular interactions and chemical reactions using variational quantum eigensolvers\n    (VQE) on QPU hardware.\n- name: Quantum Optimization\n  description: Solve combinatorial optimization problems using QAOA and other quantum optimization algorithms\n    on available QPUs.\nintegrations:\n- name: Amazon S3\n  description: Store quantum task results and job artifacts in Amazon S3\n- name: Amazon CloudWatch\n  description: Monitor quantum job metrics and logs in CloudWatch\n- name: AWS IAM\n  description: Control access to Braket resources with IAM policies\n- name: Amazon ECR\n  description: Store custom container images for Braket Hybrid Jobs\n- name: Amazon SageMaker\n  description: Integrate quantum algorithms with SageMaker ML workflows\nsolutions:\n- name: Quantum Research Platform\n  description: Build a comprehensive quantum research platform with access to multiple QPU\
  \ providers,\n    simulators, and managed job infrastructure.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-braket/refs/heads/main/apis.yml
tags:
- Quantum Computing
- QPU
- Quantum Tasks
- Hybrid Jobs
- Simulators
---
