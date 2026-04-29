---
aid: amazon-backup:amazon-backup-api
baseURL: https://backup.us-east-1.amazonaws.com
description: API for centrally managing and automating backups across AWS services including Amazon EBS, Amazon RDS, Amazon DynamoDB, Amazon EFS, Amazon FSx, Amazon EC2, and AWS Storage Gateway. Supports creating backup plans, managing backup vaults, starting and monitoring backup jobs, restoring resources, cross-region copy, legal holds, compliance frameworks, and automated restore testing.
humanURL: https://aws.amazon.com/backup/
image: ''
layout: api
name: Amazon Backup API
properties:
- type: Documentation
  url: https://docs.aws.amazon.com/aws-backup/latest/devguide/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/openapi/amazon-backup-openapi.yml
- type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/backup/2018-11-15/openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/json-schema/amazon-backup-plan-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/json-structure/backup-resource-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/json-ld/amazon-backup-context.jsonld
- type: SpectralRuleset
  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/spectral/ruleset.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/capabilities/capabilities.yml
- type: Vocabulary
  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/vocabulary/vocabulary.yml
- type: Pricing
  url: https://aws.amazon.com/backup/pricing/
- type: GettingStarted
  url: https://aws.amazon.com/backup/getting-started/
- type: FAQ
  url: https://aws.amazon.com/backup/faqs/
- type: UserGuide
  url: https://docs.aws.amazon.com/aws-backup/latest/devguide/
- type: APIReference
  url: https://docs.aws.amazon.com/aws-backup/latest/devguide/API_Reference.html
- type: CLIReference
  url: https://docs.aws.amazon.com/cli/latest/reference/backup/
- type: Security
  url: https://docs.aws.amazon.com/aws-backup/latest/devguide/security.html
provider_name: Amazon Backup
provider_slug: amazon-backup
slug: amazon-backup-api
source_yaml: "aid: amazon-backup:amazon-backup-api\nname: Amazon Backup API\ndescription: API for centrally managing and automating backups across AWS services including Amazon EBS,\n  Amazon RDS, Amazon DynamoDB, Amazon EFS, Amazon FSx, Amazon EC2, and AWS Storage Gateway. Supports creating\n  backup plans, managing backup vaults, starting and monitoring backup jobs, restoring resources, cross-region\n  copy, legal holds, compliance frameworks, and automated restore testing.\nhumanURL: https://aws.amazon.com/backup/\nbaseURL: https://backup.us-east-1.amazonaws.com\ntags:\n- AWS\n- Backup\n- Data Protection\n- Disaster Recovery\n- Storage\n- Compliance\nproperties:\n- type: Documentation\n  url: https://docs.aws.amazon.com/aws-backup/latest/devguide/\n- type: OpenAPI\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/openapi/amazon-backup-openapi.yml\n- type: OpenAPI\n  url: https://api.apis.guru/v2/specs/amazonaws.com/backup/2018-11-15/openapi.yaml\n\
  - type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/json-schema/amazon-backup-plan-schema.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/json-structure/backup-resource-structure.json\n- type: JSONLD\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/json-ld/amazon-backup-context.jsonld\n- type: SpectralRuleset\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/spectral/ruleset.yml\n- type: Capabilities\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/capabilities/capabilities.yml\n- type: Vocabulary\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/vocabulary/vocabulary.yml\n- type: Pricing\n  url: https://aws.amazon.com/backup/pricing/\n- type: GettingStarted\n  url: https://aws.amazon.com/backup/getting-started/\n- type:\
  \ FAQ\n  url: https://aws.amazon.com/backup/faqs/\n- type: UserGuide\n  url: https://docs.aws.amazon.com/aws-backup/latest/devguide/\n- type: APIReference\n  url: https://docs.aws.amazon.com/aws-backup/latest/devguide/API_Reference.html\n- type: CLIReference\n  url: https://docs.aws.amazon.com/cli/latest/reference/backup/\n- type: Security\n  url: https://docs.aws.amazon.com/aws-backup/latest/devguide/security.html\ncontact:\n- FN: Amazon Web Services\n  url: https://aws.amazon.com/contact-us/\nfeatures:\n- name: Automated Backup Scheduling\n  description: Create backup plans with cron-based schedules to automatically back up AWS resources on\n    a defined cadence with configurable start and completion windows.\n- name: Lifecycle Management\n  description: Automatically transition recovery points from warm to cold storage and delete them after\n    configurable retention periods to optimize costs.\n- name: Cross-Region Copy\n  description: Copy recovery points to backup vaults in other\
  \ AWS regions for disaster recovery and geographic\n    redundancy.\n- name: Cross-Account Management\n  description: Centrally manage backup policies across multiple AWS accounts within an AWS Organizations\n    structure.\n- name: Vault Lock (WORM)\n  description: Enforce write-once-read-many protection on backup vaults to prevent deletion or modification\n    of recovery points, supporting regulatory compliance.\n- name: Legal Holds\n  description: Preserve recovery points from deletion during legal discovery or compliance investigations\n    with legal hold policies.\n- name: Compliance Frameworks\n  description: Create compliance frameworks with controls that automatically evaluate backup configurations\n    against governance requirements.\n- name: Automated Restore Testing\n  description: Schedule periodic automated restore tests to validate backup recoverability and generate\n    compliance reports.\n- name: Continuous Backup (PITR)\n  description: Enable point-in-time recovery\
  \ for supported services, allowing restore to any second within\n    the retention window.\nuseCases:\n- name: Enterprise Backup Automation\n  description: Automate backup policies across all AWS resources with tag-based selection rules and centralized\n    management.\n- name: Regulatory Compliance\n  description: Meet compliance requirements for data retention with Vault Lock, compliance frameworks,\n    and automated reporting.\n- name: Disaster Recovery\n  description: Replicate backups cross-region and validate restore procedures with automated restore testing\n    plans.\n- name: Legal Hold Management\n  description: Preserve backup data during legal proceedings or investigations with automated legal hold\n    policies.\nintegrations:\n- name: Amazon CloudWatch\n  description: Monitor backup metrics and create alarms for backup failures\n- name: Amazon EventBridge\n  description: React to backup events with event-driven workflows\n- name: AWS CloudTrail\n  description: Audit backup\
  \ activity with consolidated CloudTrail logs\n- name: Amazon SNS\n  description: Receive backup event notifications via Amazon Simple Notification Service\n- name: AWS Organizations\n  description: Apply backup policies centrally across organization accounts\n- name: AWS KMS\n  description: Encrypt backup vaults with customer-managed KMS keys\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-backup/refs/heads/main/apis.yml
tags:
- AWS
- Backup
- Data Protection
- Disaster Recovery
- Storage
- Compliance
---
