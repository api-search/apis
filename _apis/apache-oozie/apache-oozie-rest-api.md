---
aid: apache-oozie:apache-oozie-rest-api
baseURL: http://localhost:11000/oozie
description: The Oozie Web Services API provides REST endpoints for submitting, managing, and monitoring workflow, coordinator, and bundle jobs on Apache Hadoop. Supports full job lifecycle management (submit, start, suspend, resume, kill, rerun), log and status retrieval, DAG visualization, SLA management, and system administration. Available at /oozie/v1 and /oozie/v2 with JSON responses.
humanURL: https://oozie.apache.org/docs/5.2.1/WebServicesAPI.html
image: ''
layout: api
name: Apache Oozie REST API
properties:
- type: Documentation
  url: https://oozie.apache.org/docs/5.2.1/WebServicesAPI.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apache-oozie/refs/heads/main/openapi/apache-oozie-openapi.yaml
- title: Job Info Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-oozie/refs/heads/main/json-schema/apache-oozie-job-info-schema.json
- title: Job List Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-oozie/refs/heads/main/json-schema/apache-oozie-job-list-schema.json
- title: Job ID Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-oozie/refs/heads/main/json-schema/apache-oozie-job-id-schema.json
- title: System Status Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-oozie/refs/heads/main/json-schema/apache-oozie-system-status-schema.json
provider_name: Apache Oozie
provider_slug: apache-oozie
slug: apache-oozie-rest-api
tags:
- REST
- Hadoop
- Workflow Management
- Job Scheduling
---
