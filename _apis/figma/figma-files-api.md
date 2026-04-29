---
aid: figma:figma-files-api
baseURL: https://api.figma.com
description: Figma Files API provides access to design file data including document trees, nodes, images, version history, and file metadata. Read and export design data from Figma files programmatically.
humanURL: https://developers.figma.com/docs/rest-api/file-endpoints/
image: https://www.figma.com/favicon.ico
layout: api
name: Figma Files API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-files-api-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-get-file-response-body-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-branch-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-canvas-node-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-color-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-comment-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-component-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-component-set-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-delete-dev-resource-response-body-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-dev-resource-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-document-node-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-documentation-link-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-error-response-payload-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-frame-info-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-get-dev-resources-response-body-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-published-component-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-published-component-set-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-reaction-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-style-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-style-type-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-user-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-files-version-schema.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-ld/figma-files-context.jsonld
- type: Documentation
  url: https://developers.figma.com/docs/rest-api/file-endpoints/
provider_name: Figma
provider_slug: figma
slug: figma-files-api
source_yaml: "aid: figma:figma-files-api\nname: Figma Files API\ndescription: Figma Files API provides access to design file data including document trees, nodes, images,\n  version history, and file metadata. Read and export design data from Figma files programmatically.\nimage: https://www.figma.com/favicon.ico\nbaseURL: https://api.figma.com\nhumanURL: https://developers.figma.com/docs/rest-api/file-endpoints/\ntags:\n- Dev Resources\n- Files\nproperties:\n- type: OpenAPI\n  url: openapi/figma-files-api-openapi.yml\n- type: JSONSchema\n  url: json-schema/figma-files-get-file-response-body-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-branch-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-canvas-node-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-color-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-comment-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-component-schema.json\n- type: JSONSchema\n  url:\
  \ json-schema/figma-files-component-set-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-delete-dev-resource-response-body-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-dev-resource-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-document-node-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-documentation-link-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-error-response-payload-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-frame-info-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-get-dev-resources-response-body-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-published-component-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-published-component-set-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-reaction-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-style-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-style-type-schema.json\n\
  - type: JSONSchema\n  url: json-schema/figma-files-user-schema.json\n- type: JSONSchema\n  url: json-schema/figma-files-version-schema.json\n- type: JSONLD\n  url: json-ld/figma-files-context.jsonld\n- type: Documentation\n  url: https://developers.figma.com/docs/rest-api/file-endpoints/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/apis.yml
tags:
- Dev Resources
- Files
---
