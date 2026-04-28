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
tags:
- Cloud
- Cluster Management
- Database
- Infrastructure
---
