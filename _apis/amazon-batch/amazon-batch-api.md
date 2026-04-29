---
aid: amazon-batch:amazon-batch-api
baseURL: https://batch.amazonaws.com
description: The AWS Batch API enables programmatic management of batch computing workloads, including creating and managing compute environments, job queues, job definitions, scheduling policies, and submitting and monitoring batch jobs at any scale. Supports single-node jobs, array jobs for parameter sweeps, and multi-node parallel jobs for HPC.
humanURL: https://aws.amazon.com/batch/
image: ''
layout: api
name: Amazon Batch API
properties:
- type: Documentation
  url: https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/openapi/amazon-batch-openapi.yml
- type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/batch/2016-08-10/openapi.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/json-schema/amazon-batch-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/json-structure/batch-resource-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/json-ld/amazon-batch-context.jsonld
- type: SpectralRuleset
  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/spectral/ruleset.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/capabilities/capabilities.yml
- type: Vocabulary
  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/vocabulary/vocabulary.yml
- type: Pricing
  url: https://aws.amazon.com/batch/pricing/
- type: GettingStarted
  url: https://aws.amazon.com/batch/getting-started/
- type: FAQ
  url: https://aws.amazon.com/batch/faqs/
- type: UserGuide
  url: https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html
- type: APIReference
  url: https://docs.aws.amazon.com/batch/latest/APIReference/Welcome.html
- type: CLIReference
  url: https://docs.aws.amazon.com/cli/latest/reference/batch/
- type: Security
  url: https://docs.aws.amazon.com/batch/latest/userguide/security.html
provider_name: Amazon Batch
provider_slug: amazon-batch
slug: amazon-batch-api
source_yaml: "aid: amazon-batch:amazon-batch-api\nname: Amazon Batch API\ndescription: The AWS Batch API enables programmatic management of batch computing workloads, including\n  creating and managing compute environments, job queues, job definitions, scheduling policies, and submitting\n  and monitoring batch jobs at any scale. Supports single-node jobs, array jobs for parameter sweeps,\n  and multi-node parallel jobs for HPC.\nhumanURL: https://aws.amazon.com/batch/\nbaseURL: https://batch.amazonaws.com\ntags:\n- Batch Computing\n- Compute\n- HPC\n- Job Scheduling\n- Containers\nproperties:\n- type: Documentation\n  url: https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html\n- type: OpenAPI\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/openapi/amazon-batch-openapi.yml\n- type: OpenAPI\n  url: https://api.apis.guru/v2/specs/amazonaws.com/batch/2016-08-10/openapi.json\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/json-schema/amazon-batch-schema.json\n\
  - type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/json-structure/batch-resource-structure.json\n- type: JSONLD\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/json-ld/amazon-batch-context.jsonld\n- type: SpectralRuleset\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/spectral/ruleset.yml\n- type: Capabilities\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/capabilities/capabilities.yml\n- type: Vocabulary\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/vocabulary/vocabulary.yml\n- type: Pricing\n  url: https://aws.amazon.com/batch/pricing/\n- type: GettingStarted\n  url: https://aws.amazon.com/batch/getting-started/\n- type: FAQ\n  url: https://aws.amazon.com/batch/faqs/\n- type: UserGuide\n  url: https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html\n- type: APIReference\n\
  \  url: https://docs.aws.amazon.com/batch/latest/APIReference/Welcome.html\n- type: CLIReference\n  url: https://docs.aws.amazon.com/cli/latest/reference/batch/\n- type: Security\n  url: https://docs.aws.amazon.com/batch/latest/userguide/security.html\ncontact:\n- FN: Amazon Web Services\n  url: https://aws.amazon.com/contact-us/\nfeatures:\n- name: Managed Compute Environments\n  description: Automatically provision, scale, and terminate EC2 On-Demand, Spot, Fargate, or EKS compute\n    resources based on job demand.\n- name: Array Jobs\n  description: Run N identical parallel job instances with unique array indices for parameter sweeps,\n    data parallelism, and large-scale simulations.\n- name: Multi-Node Parallel Jobs\n  description: Execute tightly-coupled HPC workloads (MPI) across multiple EC2 instances in a single coordinated\n    job.\n- name: Spot Instance Integration\n  description: Run batch jobs on EC2 Spot Instances with automatic retry on interruption, reducing compute\n\
  \    costs by up to 90%.\n- name: Fair-Share Scheduling\n  description: Distribute compute resources equitably across users and teams using configurable share\n    weights and usage tracking.\n- name: GPU Support\n  description: Run GPU-accelerated workloads including machine learning training and scientific simulations\n    on GPU instance types.\n- name: EKS Integration\n  description: Run batch jobs on Amazon EKS clusters with Kubernetes-native pod specifications and resource\n    management.\nuseCases:\n- name: Scientific Computing\n  description: Run genomics, climate modeling, and other large-scale simulations with HPC array jobs on\n    managed compute environments.\n- name: Data Processing Pipelines\n  description: Process large datasets in parallel with array jobs and Spot Instances for cost-efficient\n    ETL and analytics workloads.\n- name: Machine Learning Training\n  description: Run distributed ML training jobs across GPU instances with multi-node parallel job support.\n\
  - name: Media Transcoding\n  description: Process large volumes of media files in parallel using containerized transcoding jobs on\n    managed compute environments.\nintegrations:\n- name: Amazon ECR\n  description: Store and pull container images for batch job definitions from Amazon Elastic Container\n    Registry\n- name: Amazon S3\n  description: Read input data and write job output to Amazon S3 storage\n- name: Amazon ECS\n  description: AWS Batch uses ECS under the hood for container orchestration on EC2 and Fargate\n- name: Amazon EKS\n  description: Run batch jobs on Kubernetes clusters via Amazon Elastic Kubernetes Service\n- name: AWS CloudWatch Logs\n  description: Stream job container logs to CloudWatch Logs for monitoring and debugging\n- name: AWS Step Functions\n  description: Orchestrate multi-step workflows with AWS Batch jobs as workflow tasks\n- name: Amazon EventBridge\n  description: Trigger batch jobs on schedule or in response to events\nsolutions:\n- name: Cost-Optimized\
  \ HPC\n  description: Use Spot Instances with SPOT_CAPACITY_OPTIMIZED allocation strategy to run HPC workloads\n    at a fraction of On-Demand pricing.\n- name: Serverless Batch\n  description: Use Fargate compute environments to run batch jobs with no EC2 instance management and\n    per-second billing.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-batch/refs/heads/main/apis.yml
tags:
- Batch Computing
- Compute
- HPC
- Job Scheduling
- Containers
---
