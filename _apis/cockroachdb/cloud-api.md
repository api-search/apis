---
aid: cockroachdb:cloud-api
baseURL: https://cockroachlabs.cloud
description: REST API for managing the lifecycle of CockroachDB Cloud clusters. Supports cluster provisioning, scaling, deletion, SQL user management, network authorization (IP allowlists, private endpoints), customer-managed encryption keys (CMEK), maintenance windows, version deferral, audit log export, metric and log export, SCIM v2 group/user provisioning, folder organization, service accounts, API keys, invoices, and backup configuration. Authenticated via bearer tokens and rate-limited to 10 requests per second per user.
humanURL: https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CockroachDB Cloud API
properties:
- type: Documentation
  url: https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api
- type: APIReference
  url: https://www.cockroachlabs.com/docs/api/cloud/v1
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cockroachdb/refs/heads/main/openapi/cockroachdb-cloud-api-openapi.yml
provider_name: CockroachDB
provider_slug: cockroachdb
slug: cloud-api
source_yaml: "aid: cockroachdb:cloud-api\nname: CockroachDB Cloud API\ntags:\n- Cloud\n- Cluster Management\n- Database\n- Infrastructure\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://cockroachlabs.cloud\nhumanURL: https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api\nproperties:\n- url: https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api\n  type: Documentation\n- url: https://www.cockroachlabs.com/docs/api/cloud/v1\n  type: APIReference\n- url: openapi/cockroachdb-cloud-api-openapi.yml\n  type: OpenAPI\ndescription: REST API for managing the lifecycle of CockroachDB Cloud clusters. Supports cluster provisioning,\n  scaling, deletion, SQL user management, network authorization (IP allowlists, private endpoints), customer-managed\n  encryption keys (CMEK), maintenance windows, version deferral, audit log export, metric and log export,\n  SCIM v2 group/user provisioning, folder organization, service accounts, API keys, invoices,\
  \ and backup\n  configuration. Authenticated via bearer tokens and rate-limited to 10 requests per second per user.\nx-features:\n- Bearer-token authentication\n- Cc-Version header for API versioning\n- Service accounts and API keys\n- Terraform provider for IaC\n- SCIM v2 endpoints for SSO sync\n- CMEK rotation and revocation\n- Audit log and metric export configuration\nx-use-cases:\n- Programmatic cluster provisioning\n- GitOps with the CockroachDB Terraform provider\n- SCIM-based identity sync\n- Audit log export to SIEM\n- Cost monitoring via invoices\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cockroachdb/refs/heads/main/apis.yml
tags:
- Cloud
- Cluster Management
- Database
- Infrastructure
---
