---
aid: cri-o:cri-o-status-api
baseURL: http://localhost
description: The CRI-O Status API is an HTTP server exposed by the cri-o daemon for runtime introspection, container inspection, and lifecycle control. It provides /info and /config endpoints for daemon configuration, /containers/{id} for live container inspection, /pause/{id} and /unpause/{id} to control container execution, and /debug endpoints for golang debugging. As noted upstream, this API is not considered stable for production use.
humanURL: https://github.com/cri-o/cri-o
image: ''
layout: api
name: CRI-O Status API
properties:
- type: Documentation
  url: https://github.com/cri-o/cri-o
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/openapi/cri-o-status-openapi.yml
- type: Rules
  url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/rules/cri-o-status-rules.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/capabilities/cri-o-status-capabilities.yml
provider_name: CRI-O
provider_slug: cri-o
slug: cri-o-status-api
source_filename: cri-o-status-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CRI-O Status API\n  description: >-\n    The CRI-O Status API is an HTTP server exposed by the cri-o daemon over a\n    Unix domain socket (default /var/run/crio/crio.sock for the gRPC CRI and\n    /var/run/crio/crio.info for status). It provides runtime introspection\n    endpoints for retrieving daemon configuration, version, container\n    information, and golang debug data. As noted upstream, this API is not\n    considered stable for production use and is intended for debugging,\n    operations, and tooling integrations.\n  version: '1.0'\n  contact:\n    name: CRI-O Project\n    url: https://cri-o.io/\n  license:\n    name: Apache 2.0\n    url: https://github.com/cri-o/cri-o/blob/main/LICENSE\nexternalDocs:\n  description: CRI-O Documentation\n  url: https://github.com/cri-o/cri-o/tree/main/docs\nservers:\n  - url: http://localhost\n    description: CRI-O Status API served over the local Unix socket\ntags:\n  - name: Information\n    description:\
  \ Runtime version, configuration, and general info endpoints.\n  - name: Containers\n    description: Endpoints that return information about live containers.\n  - name: Lifecycle\n    description: Endpoints to pause and unpause running containers.\n  - name: Debug\n    description: Golang debug endpoints for goroutines, heap, and profiling.\npaths:\n  /info:\n    get:\n      tags:\n        - Information\n      operationId: getInfo\n      summary: Get runtime information\n      description: >-\n        Returns daemon information including storage driver, storage root,\n        cgroup driver, and runtime defaults.\n      responses:\n        '200':\n          description: Runtime information\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Info'\n  /config:\n    get:\n      tags:\n        - Information\n      operationId: getConfig\n      summary: Get runtime configuration\n      description: Returns the active CRI-O TOML\
  \ configuration as plain text.\n      responses:\n        '200':\n          description: TOML configuration document\n          content:\n            text/plain:\n              schema:\n                type: string\n  /containers/{id}:\n    get:\n      tags:\n        - Containers\n      operationId: getContainer\n      summary: Get container info\n      description: Returns runtime information about a single container by ID.\n      parameters:\n        - name: id\n          in: path\n          required: true\n          description: Container ID.\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Container information\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ContainerInfo'\n        '404':\n          description: Container not found\n  /pause/{id}:\n    post:\n      tags:\n        - Lifecycle\n      operationId: pauseContainer\n      summary: Pause a container\n\
  \      description: Pauses a running container by ID.\n      parameters:\n        - name: id\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '204':\n          description: Container paused\n        '404':\n          description: Container not found\n  /unpause/{id}:\n    post:\n      tags:\n        - Lifecycle\n      operationId: unpauseContainer\n      summary: Unpause a container\n      description: Unpauses a paused container by ID.\n      parameters:\n        - name: id\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '204':\n          description: Container unpaused\n        '404':\n          description: Container not found\n  /debug/goroutines:\n    get:\n      tags:\n        - Debug\n      operationId: getGoroutines\n      summary: Dump goroutine stacks\n      description: Returns the current goroutine stack traces for the daemon.\n      responses:\n\
  \        '200':\n          description: Goroutine stack dump as plain text.\n          content:\n            text/plain:\n              schema:\n                type: string\ncomponents:\n  schemas:\n    Info:\n      type: object\n      properties:\n        storage_driver:\n          type: string\n        storage_root:\n          type: string\n        cgroup_driver:\n          type: string\n        default_runtime:\n          type: string\n        runtimes:\n          type: object\n          additionalProperties: true\n    ContainerInfo:\n      type: object\n      properties:\n        id:\n          type: string\n        name:\n          type: string\n        image:\n          type: string\n        pid:\n          type: integer\n        sandbox_id:\n          type: string\n        created_time:\n          type: string\n          format: date-time\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/openapi/cri-o-status-openapi.yml
tags:
- Debugging
- HTTP
- Lifecycle
- Status
---
