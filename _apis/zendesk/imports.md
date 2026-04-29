---
aid: zendesk:imports
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Imports API lets you programmatically load large volumes of records into Zendesk in a controlled, asynchronous wayideal for migrations, initial seeding, or ongoing syncs. You submit a file or batched payload, define which object type to import (for example, users/organizations/tickets in Support or leads/contacts/deals in Sell), and map fields. The import runs as a background job you can monitor via status endpoints, with progress, per-row validation, and detailed error reporting.
humanURL: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_import/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Imports API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_import/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/imports-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: imports
source_yaml: "aid: zendesk:imports\nname: Zendesk Imports API\ntags:\n- Imports\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://{subdomain}.zendesk.com\nhumanURL: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_import/\nproperties:\n- url: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_import/\n  type: Documentation\n- url: openapi/imports-openapi-original.yml\n  type: OpenAPI\ndescription: The Zendesk Imports API lets you programmatically load large volumes of records into Zendesk\n  in a controlled, asynchronous wayideal for migrations, initial seeding, or ongoing syncs. You submit\n  a file or batched payload, define which object type to import (for example, users/organizations/tickets\n  in Support or leads/contacts/deals in Sell), and map fields. The import runs as a background job you\n  can monitor via status endpoints, with progress, per-row validation, and detailed error reporting.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/apis.yml
tags:
- Imports
---
