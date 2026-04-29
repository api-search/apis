---
aid: comcast:open-ingest-api
baseURL: https://compass-mmpwebservice-prod.codebig2.net
description: The Comcast Open Ingest endpoint accepts metadata and content asset packages from NBCUniversal media partners. Clients POST an XML payload describing assets to the Merlin ingest proxy, authenticated with a Comcast SAT bearer token and partnered through partner identifiers such as globalott. The endpoint returns an OpenIngestResult document with per-asset outcome status.
humanURL: https://docs.developer.comcast.com/docs/endpoints
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Comcast Open Ingest API
properties:
- type: Documentation
  url: https://docs.developer.comcast.com/docs/endpoints
provider_name: Comcast
provider_slug: comcast
slug: open-ingest-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: comcast:open-ingest-api\nname: Comcast Open Ingest API\ntags:\n- Ingest\n- Media\n- Metadata\n- NBCUniversal\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://compass-mmpwebservice-prod.codebig2.net\nhumanURL: https://docs.developer.comcast.com/docs/endpoints\nproperties:\n- url: https://docs.developer.comcast.com/docs/endpoints\n  type: Documentation\ndescription: The Comcast Open Ingest endpoint accepts metadata and content asset packages from NBCUniversal\n  media partners. Clients POST an XML payload describing assets to the Merlin ingest proxy, authenticated\n  with a Comcast SAT bearer token and partnered through partner identifiers such as globalott. The endpoint\n  returns an OpenIngestResult document with per-asset outcome status.\nx-features:\n- XML asset and metadata submission\n- Bearer-token authentication via Comcast SAT\n- Partner-scoped ingestion (e.g. globalott)\n- OpenIngestResult outcome reporting\n\
  x-use-cases:\n- Submitting media metadata to NBCUniversal pipelines\n- Bulk content publication for OTT distribution\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/comcast/refs/heads/main/apis.yml
tags:
- Ingest
- Media
- Metadata
- NBCUniversal
---
