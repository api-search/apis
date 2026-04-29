---
aid: apache-dolphinscheduler:apache-dolphinscheduler-rest-api
baseURL: ''
description: The DolphinScheduler REST API enables programmatic management of projects, workflow definitions (DAGs), workflow instances, task types, schedules, resources, data sources, alerts, tenants, and users. Authentication is via API token. A Swagger UI is available at /dolphinscheduler/swagger-ui/index.html.
humanURL: https://dolphinscheduler.apache.org/en-us/docs/latest/user_doc/guide/open-api.html
image: ''
layout: api
name: Apache DolphinScheduler REST API
properties:
- type: Documentation
  url: https://dolphinscheduler.apache.org/en-us/docs/latest/user_doc/guide/open-api.html
- type: GettingStarted
  url: https://dolphinscheduler.apache.org/en-us/docs/latest/user_doc/start/quick-start.html
- type: GitHubRepository
  url: https://github.com/apache/dolphinscheduler
- title: Python SDK (PyDolphinScheduler)
  type: SDK
  url: https://pypi.org/project/apache-airflow-providers-apache-dolphinscheduler/
- title: Docker Image
  type: Tools
  url: https://hub.docker.com/r/apache/dolphinscheduler-standalone-server
- title: Kubernetes Operator
  type: Tools
  url: https://github.com/apache/dolphinscheduler-operator
- title: Schedule
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-schema/apache-dolphinscheduler-schedule-schema.json
- title: Task Definition
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-schema/apache-dolphinscheduler-task-definition-schema.json
- title: Workflow Definition
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-schema/apache-dolphinscheduler-workflow-definition-schema.json
- title: Workflow Instance
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-schema/apache-dolphinscheduler-workflow-instance-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-structure/apache-dolphinscheduler-schedule-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-structure/apache-dolphinscheduler-task-definition-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-structure/apache-dolphinscheduler-workflow-definition-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-structure/apache-dolphinscheduler-workflow-instance-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-ld/apache-dolphinscheduler-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/examples/apache-dolphinscheduler-schedule-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/examples/apache-dolphinscheduler-task-definition-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/examples/apache-dolphinscheduler-workflow-definition-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/examples/apache-dolphinscheduler-workflow-instance-example.json
provider_name: Apache DolphinScheduler
provider_slug: apache-dolphinscheduler
slug: apache-dolphinscheduler-rest-api
source_yaml: "aid: apache-dolphinscheduler:apache-dolphinscheduler-rest-api\nname: Apache DolphinScheduler REST API\ndescription: The DolphinScheduler REST API enables programmatic management of projects, workflow definitions\n  (DAGs), workflow instances, task types, schedules, resources, data sources, alerts, tenants, and users.\n  Authentication is via API token. A Swagger UI is available at /dolphinscheduler/swagger-ui/index.html.\nhumanURL: https://dolphinscheduler.apache.org/en-us/docs/latest/user_doc/guide/open-api.html\ntags:\n- Alerts\n- DAG\n- Data Sources\n- Projects\n- REST\n- Resources\n- Scheduling\n- Tasks\n- Tenants\n- Workflow\nproperties:\n- type: Documentation\n  url: https://dolphinscheduler.apache.org/en-us/docs/latest/user_doc/guide/open-api.html\n- type: GettingStarted\n  url: https://dolphinscheduler.apache.org/en-us/docs/latest/user_doc/start/quick-start.html\n- type: GitHubRepository\n  url: https://github.com/apache/dolphinscheduler\n- type: SDK\n  url: https://pypi.org/project/apache-airflow-providers-apache-dolphinscheduler/\n\
  \  title: Python SDK (PyDolphinScheduler)\n- type: Tools\n  url: https://hub.docker.com/r/apache/dolphinscheduler-standalone-server\n  title: Docker Image\n- type: Tools\n  url: https://github.com/apache/dolphinscheduler-operator\n  title: Kubernetes Operator\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-schema/apache-dolphinscheduler-schedule-schema.json\n  title: Schedule\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-schema/apache-dolphinscheduler-task-definition-schema.json\n  title: Task Definition\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-schema/apache-dolphinscheduler-workflow-definition-schema.json\n  title: Workflow Definition\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-schema/apache-dolphinscheduler-workflow-instance-schema.json\n\
  \  title: Workflow Instance\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-structure/apache-dolphinscheduler-schedule-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-structure/apache-dolphinscheduler-task-definition-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-structure/apache-dolphinscheduler-workflow-definition-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-structure/apache-dolphinscheduler-workflow-instance-structure.json\n- type: JSONLD\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/json-ld/apache-dolphinscheduler-context.jsonld\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/examples/apache-dolphinscheduler-schedule-example.json\n\
  - type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/examples/apache-dolphinscheduler-task-definition-example.json\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/examples/apache-dolphinscheduler-workflow-definition-example.json\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/examples/apache-dolphinscheduler-workflow-instance-example.json\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-dolphinscheduler/refs/heads/main/apis.yml
tags:
- Alerts
- DAG
- Data Sources
- Projects
- REST
- Resources
- Scheduling
- Tasks
- Tenants
- Workflow
---
