---
aid: amazon-fsx:amazon-fsx-api
baseURL: https://fsx.amazonaws.com
description: The Amazon FSx API enables programmatic access to create, manage, and monitor fully managed file systems. You can create file systems, manage backups, configure data repositories, create snapshots, and manage storage virtual machines across multiple file system types.
humanURL: https://aws.amazon.com/fsx/
image: https://a0.awsstatic.com/libra-css/images/logos/aws_logo_smile_1200x630.png
layout: api
name: Amazon FSx API
properties:
- type: Documentation
  url: https://docs.aws.amazon.com/fsx/latest/APIReference/Welcome.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/openapi/amazon-fsx-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-schema/amazon-fsx-file-system-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-schema/amazon-fsx-backup-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-schema/amazon-fsx-snapshot-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-schema/amazon-fsx-storage-virtual-machine-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-schema/amazon-fsx-tag-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-structure/amazon-fsx-file-system-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-structure/amazon-fsx-backup-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-structure/amazon-fsx-snapshot-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-structure/amazon-fsx-storage-virtual-machine-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/json-structure/amazon-fsx-tag-structure.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/examples/amazon-fsx-file-system-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/examples/amazon-fsx-backup-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/examples/amazon-fsx-snapshot-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/examples/amazon-fsx-storage-virtual-machine-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/examples/amazon-fsx-tag-example.json
- type: GettingStarted
  url: https://aws.amazon.com/fsx/getting-started/
- type: Pricing
  url: https://aws.amazon.com/fsx/pricing/
- type: FAQ
  url: https://aws.amazon.com/fsx/faqs/
- type: APIReference
  url: https://docs.aws.amazon.com/fsx/latest/APIReference/Welcome.html
provider_name: Amazon FSx
provider_slug: amazon-fsx
slug: amazon-fsx-api
source_filename: amazon-fsx-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Amazon FSx API\n  description: >-\n    Amazon FSx provides fully managed file systems optimized for a variety of\n    workloads. This API enables you to create and manage file systems,\n    configure backups and snapshots, manage data repositories, and monitor\n    file system health across Lustre, Windows File Server, NetApp ONTAP,\n    and OpenZFS file system types.\n  version: '2018-03-01'\n  contact:\n    name: Amazon Web Services\n    url: https://aws.amazon.com/contact-us/\n  termsOfService: https://aws.amazon.com/service-terms/\nexternalDocs:\n  description: Amazon FSx API Reference\n  url: https://docs.aws.amazon.com/fsx/latest/APIReference/Welcome.html\nservers:\n  - url: https://fsx.{region}.amazonaws.com\n    description: Amazon FSx Regional Endpoint\n    variables:\n      region:\n        default: us-east-1\n        description: AWS Region\ntags:\n  - name: File Systems\n    description: Operations for creating and managing file systems\n\
  paths:\n  /:\n    post:\n      operationId: CreateFileSystem\n      summary: Amazon FSx Create a new file system\n      description: Creates a new Amazon FSx file system of the specified type.\n      tags:\n        - File Systems\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              required:\n                - FileSystemType\n                - StorageCapacity\n                - SubnetIds\n              properties:\n                FileSystemType:\n                  type: string\n                  enum: [WINDOWS, LUSTRE, ONTAP, OPENZFS]\n                  description: The type of file system to create\n                StorageCapacity:\n                  type: integer\n                  description: Storage capacity in GiB\n                SubnetIds:\n                  type: array\n                  items:\n                    type: string\n                  description: Subnet IDs for the\
  \ file system\n                SecurityGroupIds:\n                  type: array\n                  items:\n                    type: string\n                  description: Security group IDs\n                Tags:\n                  type: array\n                  items:\n                    type: object\n      responses:\n        '200':\n          description: File system created successfully\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  FileSystem:\n                    type: object\n                    description: The configuration of the file system\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-fsx/refs/heads/main/openapi/amazon-fsx-openapi.yml
tags:
- File Systems
- High Performance
- Managed Services
- Storage
---
