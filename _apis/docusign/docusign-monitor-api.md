---
aid: docusign:docusign-monitor-api
baseURL: https://lens-d.docusign.net
description: The Docusign Monitor API helps organizations protect their agreements with round-the-clock activity tracking. It receives a data feed containing security events for Docusign accounts, enabling integration with security information and event management (SIEM) systems and other monitoring applications.
humanURL: https://developers.docusign.com/docs/monitor-api/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Docusign Monitor API
properties:
- type: Documentation
  url: https://developers.docusign.com/docs/monitor-api/reference/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-monitor-openapi-original.yml
- type: GettingStarted
  url: https://developers.docusign.com/docs/monitor-api/monitor101/
- type: Tutorials
  url: https://developers.docusign.com/docs/monitor-api/how-to/
provider_name: Docusign
provider_slug: docusign
slug: docusign-monitor-api
source_filename: docusign-monitor-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.1\ninfo:\n  title: Docusign Monitor API\n  description: An API for an integrator to access the features of DocuSign Monitor\n  termsOfService: https://www.docusign.com/company/terms-and-conditions/web\n  contact:\n    name: DocuSign Developer Center\n    url: https://developers.docusign.com\n    email: devcenter@docusign.com\n  version: v2.0\nexternalDocs:\n  description: \"\"\n  url: \"\"\nservers:\n  - url: https://lens.docusign.net/\nsecurity:\n  - Bearer: []\ntags:\n  - name: DataSet\n    description: The DataSet resource provides methods that allow you to fetch organization event data. The `dataSet` path parameter must be set to `monitor`.\npaths:\n  /api/v{version}/datasets/{dataSetName}/stream:\n    get:\n      tags:\n        - DataSet\n      summary: Docusign Gets customer event data for an organization.\n      description: |\n        Gets customer event data for the organization that owns the integration key.\n\n        The results for this endpoint are\
  \ paginated by event timestamp. Use the `cursor` parameter to specify where the query begins in the dataset. Use the `limit` parameter to set the number of records returned.\n      operationId: Api_Version_DatasetsByDataSetNameStreamGet\n      parameters:\n        - name: dataSetName\n          in: path\n          description: Must be `monitor`.\n          required: true\n          schema:\n            type: string\n        - name: version\n          in: path\n          description: |\n            Must be `2`.\n          required: true\n          schema:\n            type: string\n            default: \"2.0\"\n        - name: cursor\n          in: query\n          description: |\n            Specifies a pointer into the dataset where your query will begin. You can either provide an ISO DateTime or a string cursor (from the `endCursor` value in the response). If no value is provided, the query begins from seven days ago.\n\n            For example, to fetch event data beginning from January\
  \ 1, 2022, set this value to `2022-01-01T00:00:00Z`. The response will include data about events starting from that date in chronological order. The response also includes an `endCursor` property. To fetch the next page of event data, call this endpoint again with `cursor` set to the previous `endCursor` value.\n          schema:\n            type: string\n        - name: limit\n          in: query\n          description: The maximum number of records to return. The default value is 1000.\n          schema:\n            type: integer\n            format: int32\n            default: 1000\n      responses:\n        \"200\":\n          description: Success\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/CursoredResult'\n      security:\n        - accessCode:\n            - impersonation\n      x-ds-methodname: getStream\n      x-ds-method: getStream\n      x-ds-service: DataSet\n      x-ds-in-sdk: true\ncomponents:\n \
  \ schemas:\n    CursoredResult:\n      type: object\n      properties:\n        endCursor:\n          type: string\n          description: \"\"\n        data:\n          type: array\n          description: \"\"\n          items:\n            type: object\n            properties: {}\n      description: \"\"\n      x-ds-definition-name: CursoredResult\n      x-ms-summary: \"\"\n    DataSet:\n      type: object\n      properties:\n        endCursor:\n          type: string\n          description: \"\"\n        data:\n          type: array\n          description: \"\"\n          items:\n            type: object\n            properties: {}\n      description: Methods to fetch organization event data.\n      x-ds-definition-name: CursoredResult\n      x-ms-summary: Methods to fetch organization event data.\n      x-ds-category: Monitor\n      x-ds-order: \"100\"\n  securitySchemes:\n    Bearer:\n      type: apiKey\n      description: \"JWT Authorization header using the Bearer scheme. Example:\
  \ \\\"Authorization: Bearer {token}\\\"\"\n      name: Authorization\n      in: header\nx-ds-categories:\n  - name: Monitor\n    summary: The DocuSign Monitor API receives a data feed containing security events for your DocuSign account. This data goes directly to whichever application or website you choose to integrate with DocuSign's eSignature REST API.\n    description: |\n      Each time an event occurs, DocuSign Monitor returns JSON Data Types from a download endpoint. The endpoints include the Monitor UI, SIEMs such as Splunk, and other Customer API endpoints.\n\n      **Note:** Your accounts must exist inside an organization to access this data.\nx-ds-devdocs:\n  stamp: ca00a16 2022-10-04 12:15:28-0400\nx-original-swagger-version: \"2.0\"\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/docusign/refs/heads/main/openapi/docusign-monitor-openapi-original.yml
tags:
- Audit
- Events
- Monitoring
- Security
---
