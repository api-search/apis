---
aid: absentify:absentify
baseURL: https://api.absentify.com/api/v1
description: REST API for managing employee absences, leave requests, members, departments, leave types, public holidays, and workspace settings. Requires an API key (x-api-key header) available on the Plus plan. Rate limit of 150 requests per second per IP address.
humanURL: https://absentify.com/docs/en/api-reference/introduction
image: ''
layout: api
name: Absentify API
properties:
- type: Documentation
  url: https://absentify.com/docs/en/api-reference/introduction
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/openapi/absentify-openapi.yml
- title: Member Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-schema/absentify-member-schema.json
- title: Department Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-schema/absentify-department-schema.json
- title: Leave Type Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-schema/absentify-leave-type-schema.json
- title: Request Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-schema/absentify-request-schema.json
- title: Absence Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-schema/absentify-absence-schema.json
- title: Workspace Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-schema/absentify-workspace-schema.json
- title: Public Holiday Calendar Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-schema/absentify-public-holiday-calendar-schema.json
- title: Member Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-structure/absentify-member-structure.json
- title: Department Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-structure/absentify-department-structure.json
- title: Leave Type Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-structure/absentify-leave-type-structure.json
- title: Request Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-structure/absentify-request-structure.json
- title: Absence Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-structure/absentify-absence-structure.json
- title: Workspace Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-structure/absentify-workspace-structure.json
- title: Public Holiday Calendar Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-structure/absentify-public-holiday-calendar-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/json-ld/absentify-context.jsonld
- title: Member Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/examples/absentify-member-example.json
- title: Department Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/examples/absentify-department-example.json
- title: Leave Type Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/examples/absentify-leave-type-example.json
- title: Request Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/examples/absentify-request-example.json
- title: Absence Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/examples/absentify-absence-example.json
- title: Workspace Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/examples/absentify-workspace-example.json
provider_name: Absentify
provider_slug: absentify
slug: absentify
source_yaml: "aid: absentify:absentify\nname: Absentify API\ndescription: REST API for managing employee absences, leave requests, members, departments, leave types,\n  public holidays, and workspace settings. Requires an API key (x-api-key header) available on the Plus\n  plan. Rate limit of 150 requests per second per IP address.\nhumanURL: https://absentify.com/docs/en/api-reference/introduction\nbaseURL: https://api.absentify.com/api/v1\ntags:\n- Absence Management\n- Leave Requests\n- Members\n- Departments\n- Leave Types\nproperties:\n- type: Documentation\n  url: https://absentify.com/docs/en/api-reference/introduction\n- type: OpenAPI\n  url: openapi/absentify-openapi.yml\n- type: JSONSchema\n  url: json-schema/absentify-member-schema.json\n  title: Member Schema\n- type: JSONSchema\n  url: json-schema/absentify-department-schema.json\n  title: Department Schema\n- type: JSONSchema\n  url: json-schema/absentify-leave-type-schema.json\n  title: Leave Type Schema\n- type: JSONSchema\n\
  \  url: json-schema/absentify-request-schema.json\n  title: Request Schema\n- type: JSONSchema\n  url: json-schema/absentify-absence-schema.json\n  title: Absence Schema\n- type: JSONSchema\n  url: json-schema/absentify-workspace-schema.json\n  title: Workspace Schema\n- type: JSONSchema\n  url: json-schema/absentify-public-holiday-calendar-schema.json\n  title: Public Holiday Calendar Schema\n- type: JSONStructure\n  url: json-structure/absentify-member-structure.json\n  title: Member Structure\n- type: JSONStructure\n  url: json-structure/absentify-department-structure.json\n  title: Department Structure\n- type: JSONStructure\n  url: json-structure/absentify-leave-type-structure.json\n  title: Leave Type Structure\n- type: JSONStructure\n  url: json-structure/absentify-request-structure.json\n  title: Request Structure\n- type: JSONStructure\n  url: json-structure/absentify-absence-structure.json\n  title: Absence Structure\n- type: JSONStructure\n  url: json-structure/absentify-workspace-structure.json\n\
  \  title: Workspace Structure\n- type: JSONStructure\n  url: json-structure/absentify-public-holiday-calendar-structure.json\n  title: Public Holiday Calendar Structure\n- type: JSON-LD\n  url: json-ld/absentify-context.jsonld\n- type: Example\n  url: examples/absentify-member-example.json\n  title: Member Example\n- type: Example\n  url: examples/absentify-department-example.json\n  title: Department Example\n- type: Example\n  url: examples/absentify-leave-type-example.json\n  title: Leave Type Example\n- type: Example\n  url: examples/absentify-request-example.json\n  title: Request Example\n- type: Example\n  url: examples/absentify-absence-example.json\n  title: Absence Example\n- type: Example\n  url: examples/absentify-workspace-example.json\n  title: Workspace Example\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/absentify/refs/heads/main/apis.yml
tags:
- Absence Management
- Leave Requests
- Members
- Departments
- Leave Types
---
