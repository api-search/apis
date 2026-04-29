---
aid: microsoft-project:rest-api
baseURL: https://{tenant}.sharepoint.com/sites/pwa/_api/ProjectServer
description: REST API for accessing and managing Microsoft Project Online and Project Server data including projects, tasks, resources, assignments, calendars, custom fields, timesheets, lookup tables, and workflow activities. Uses SharePoint-based REST endpoints via the ProjectServer service.
humanURL: https://learn.microsoft.com/en-us/office/client-developer/project/client-side-object-model-csom-for-project-2013
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Project Online REST API
properties:
- type: Documentation
  url: https://learn.microsoft.com/en-us/office/client-developer/project/client-side-object-model-csom-for-project-2013
- type: APIReference
  url: https://learn.microsoft.com/en-us/office/client-developer/project/javascript-library-and-rest-reference-for-project-server-2013
- type: Authentication
  url: https://learn.microsoft.com/en-us/sharepoint/dev/sp-add-ins/authorization-and-authentication-of-sharepoint-add-ins
- type: CodeExamples
  url: https://github.com/OfficeDev/Project-Samples/tree/main/O365-Project-Online-REST-Samples
- title: REST CRUD Operations Sample
  type: CodeExamples
  url: https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/openapi/microsoft-project-rest-api.yaml
- title: Project Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-schema/rest-api-project-schema.json
- title: Task Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-schema/rest-api-task-schema.json
- title: Enterprise Resource Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-schema/rest-api-enterprise-resource-schema.json
- title: Assignment Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-schema/rest-api-assignment-schema.json
- title: Calendar Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-schema/rest-api-calendar-schema.json
- title: Custom Field Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-schema/rest-api-custom-field-schema.json
- title: TimeSheet Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-schema/rest-api-time-sheet-schema.json
- title: Project Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-structure/rest-api-project-structure.json
- title: Task Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-structure/rest-api-task-structure.json
- title: Enterprise Resource Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-structure/rest-api-enterprise-resource-structure.json
- title: Assignment Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-structure/rest-api-assignment-structure.json
- title: Calendar Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-structure/rest-api-calendar-structure.json
- title: Custom Field Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-structure/rest-api-custom-field-structure.json
- title: TimeSheet Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-structure/rest-api-time-sheet-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/json-ld/microsoft-project-rest-api-context.jsonld
- title: Project Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/examples/rest-api-project-example.json
- title: Task Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/examples/rest-api-task-example.json
- title: Enterprise Resource Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/examples/rest-api-enterprise-resource-example.json
- title: Assignment Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/examples/rest-api-assignment-example.json
- title: Calendar Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/examples/rest-api-calendar-example.json
- title: Custom Field Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/examples/rest-api-custom-field-example.json
- title: TimeSheet Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/examples/rest-api-time-sheet-example.json
provider_name: Microsoft Project
provider_slug: microsoft-project
slug: rest-api
source_yaml: "aid: microsoft-project:rest-api\nname: Microsoft Project Online REST API\ndescription: REST API for accessing and managing Microsoft Project Online and Project Server data including\n  projects, tasks, resources, assignments, calendars, custom fields, timesheets, lookup tables, and workflow\n  activities. Uses SharePoint-based REST endpoints via the ProjectServer service.\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://learn.microsoft.com/en-us/office/client-developer/project/client-side-object-model-csom-for-project-2013\nbaseURL: https://{tenant}.sharepoint.com/sites/pwa/_api/ProjectServer\ntags:\n- Assignments\n- Calendars\n- Custom Fields\n- Projects\n- Resources\n- REST\n- Tasks\n- Timesheets\nproperties:\n- type: Documentation\n  url: https://learn.microsoft.com/en-us/office/client-developer/project/client-side-object-model-csom-for-project-2013\n- type: APIReference\n  url: https://learn.microsoft.com/en-us/office/client-developer/project/javascript-library-and-rest-reference-for-project-server-2013\n\
  - type: Authentication\n  url: https://learn.microsoft.com/en-us/sharepoint/dev/sp-add-ins/authorization-and-authentication-of-sharepoint-add-ins\n- type: CodeExamples\n  url: https://github.com/OfficeDev/Project-Samples/tree/main/O365-Project-Online-REST-Samples\n- type: CodeExamples\n  url: https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations\n  title: REST CRUD Operations Sample\n- type: OpenAPI\n  url: openapi/microsoft-project-rest-api.yaml\n- type: JSONSchema\n  url: json-schema/rest-api-project-schema.json\n  title: Project Schema\n- type: JSONSchema\n  url: json-schema/rest-api-task-schema.json\n  title: Task Schema\n- type: JSONSchema\n  url: json-schema/rest-api-enterprise-resource-schema.json\n  title: Enterprise Resource Schema\n- type: JSONSchema\n  url: json-schema/rest-api-assignment-schema.json\n  title: Assignment Schema\n- type: JSONSchema\n  url: json-schema/rest-api-calendar-schema.json\n  title: Calendar Schema\n- type: JSONSchema\n  url: json-schema/rest-api-custom-field-schema.json\n\
  \  title: Custom Field Schema\n- type: JSONSchema\n  url: json-schema/rest-api-time-sheet-schema.json\n  title: TimeSheet Schema\n- type: JSONStructure\n  url: json-structure/rest-api-project-structure.json\n  title: Project Structure\n- type: JSONStructure\n  url: json-structure/rest-api-task-structure.json\n  title: Task Structure\n- type: JSONStructure\n  url: json-structure/rest-api-enterprise-resource-structure.json\n  title: Enterprise Resource Structure\n- type: JSONStructure\n  url: json-structure/rest-api-assignment-structure.json\n  title: Assignment Structure\n- type: JSONStructure\n  url: json-structure/rest-api-calendar-structure.json\n  title: Calendar Structure\n- type: JSONStructure\n  url: json-structure/rest-api-custom-field-structure.json\n  title: Custom Field Structure\n- type: JSONStructure\n  url: json-structure/rest-api-time-sheet-structure.json\n  title: TimeSheet Structure\n- type: JSONLD\n  url: json-ld/microsoft-project-rest-api-context.jsonld\n- type: Example\n\
  \  url: examples/rest-api-project-example.json\n  title: Project Example\n- type: Example\n  url: examples/rest-api-task-example.json\n  title: Task Example\n- type: Example\n  url: examples/rest-api-enterprise-resource-example.json\n  title: Enterprise Resource Example\n- type: Example\n  url: examples/rest-api-assignment-example.json\n  title: Assignment Example\n- type: Example\n  url: examples/rest-api-calendar-example.json\n  title: Calendar Example\n- type: Example\n  url: examples/rest-api-custom-field-example.json\n  title: Custom Field Example\n- type: Example\n  url: examples/rest-api-time-sheet-example.json\n  title: TimeSheet Example\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/apis.yml
tags:
- Assignments
- Calendars
- Custom Fields
- Projects
- Resources
- REST
- Tasks
- Timesheets
---
