---
aid: cockroach-labs:cockroach-labs-cloud-api
baseURL: https://cockroachlabs.cloud
description: REST API for managing the lifecycle of CockroachDB Cloud clusters. Supports cluster provisioning, scaling, deletion, SQL user management, network authorization (IP allowlists, private endpoints), customer-managed encryption keys (CMEK), maintenance windows, version deferral, audit log export, metric and log export, SCIM v2 group/user provisioning, folder organization, service accounts, API keys, invoices, and backup configuration. Authenticated via bearer tokens and rate-limited to 10 requests per second per user. Also available via the official CockroachDB Cloud Terraform provider.
humanURL: https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api
image: ''
layout: api
name: CockroachDB Cloud API
properties:
- type: Documentation
  url: https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api
- type: APIReference
  url: https://www.cockroachlabs.com/docs/api/cloud/v1
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cockroach-labs/refs/heads/main/openapi/cockroach-labs-cloud-api-openapi.yml
provider_name: Cockroach Labs
provider_slug: cockroach-labs
slug: cockroach-labs-cloud-api
source_yaml: "aid: cockroach-labs:cockroach-labs-cloud-api\nname: CockroachDB Cloud API\ntags:\n- Cloud\n- Cluster Management\n- Database\n- Infrastructure\nhumanURL: https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api\nbaseURL: https://cockroachlabs.cloud\nproperties:\n- url: https://www.cockroachlabs.com/docs/cockroachcloud/cloud-api\n  type: Documentation\n- url: https://www.cockroachlabs.com/docs/api/cloud/v1\n  type: APIReference\n- url: openapi/cockroach-labs-cloud-api-openapi.yml\n  type: OpenAPI\ndescription: REST API for managing the lifecycle of CockroachDB Cloud clusters. Supports cluster provisioning,\n  scaling, deletion, SQL user management, network authorization (IP allowlists, private endpoints), customer-managed\n  encryption keys (CMEK), maintenance windows, version deferral, audit log export, metric and log export,\n  SCIM v2 group/user provisioning, folder organization, service accounts, API keys, invoices, and backup\n  configuration. Authenticated via bearer\
  \ tokens and rate-limited to 10 requests per second per user.\n  Also available via the official CockroachDB Cloud Terraform provider.\nx-features:\n- Bearer-token authentication with service accounts and API keys\n- Cc-Version header for API versioning\n- 10 RPS rate limit per user\n- SCIM v2 endpoints for SSO group/user sync\n- Terraform provider for IaC workflows\n- CMEK rotation, revocation, and key-spec management\n- Cluster scaling, maintenance windows, and version deferral\n- Audit log and metric/log export configuration\nx-use-cases:\n- Programmatic provisioning of CockroachDB clusters\n- GitOps/IaC management with Terraform\n- SCIM-based identity sync from Okta, Entra ID, Google Workspace\n- Compliance automation via audit log export to SIEM\n- Cost monitoring via invoices endpoint\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cockroach-labs/refs/heads/main/apis.yml
tags:
- Cloud
- Cluster Management
- Database
- Infrastructure
---
