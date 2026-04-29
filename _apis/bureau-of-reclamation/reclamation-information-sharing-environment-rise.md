---
aid: bureau-of-reclamation:reclamation-information-sharing-environment-rise
baseURL: https://data.usbr.gov/rise/api/
description: The RISE API allows users to query Bureau of Reclamation water resource data programmatically, returning JSON objects. For Geospatial and File Upload datasets, only metadata can be queried. For time series datasets, both metadata and data can be queried. Data includes hydrometric measurements, reservoir levels, streamflow, and water quality.
humanURL: https://data.usbr.gov/rise/api
image: ''
layout: api
name: Reclamation Information Sharing Environment (RISE) API
properties:
- type: Documentation
  url: https://data.usbr.gov/rise/api
- type: Portal
  url: https://data.usbr.gov/
- type: DataAPI
  url: https://catalog.data.gov/dataset?organization=usbr-gov
provider_name: Bureau of Reclamation
provider_slug: bureau-of-reclamation
slug: reclamation-information-sharing-environment-rise
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: bureau-of-reclamation:reclamation-information-sharing-environment-rise\nname: Reclamation Information Sharing Environment (RISE) API\ntags:\n- Federal Government\n- Water\n- Hydrology\n- Time Series\nhumanURL: https://data.usbr.gov/rise/api\nbaseURL: https://data.usbr.gov/rise/api/\nproperties:\n- url: https://data.usbr.gov/rise/api\n  type: Documentation\n- url: https://data.usbr.gov/\n  type: Portal\n- url: https://catalog.data.gov/dataset?organization=usbr-gov\n  type: DataAPI\ndescription: The RISE API allows users to query Bureau of Reclamation water resource data programmatically,\n  returning JSON objects. For Geospatial and File Upload datasets, only metadata can be queried. For time\n  series datasets, both metadata and data can be queried. Data includes hydrometric measurements, reservoir\n  levels, streamflow, and water quality.\nfeatures:\n- Time Series Data\n- Hydrometric Measurements\n- Reservoir Level Data\n- Streamflow Data\n- Water Quality Data\n- Geospatial\
  \ Metadata\n- JSON Format\n- Paginated Results\nuseCases:\n- Water resource planning\n- Drought monitoring\n- Hydroelectric generation analysis\n- Environmental flow studies\n- Water rights management\n- Climate research\nendpoints:\n- path: /catalog-item\n  description: Query catalog items\n- path: /catalog-record\n  description: Query catalog records\n- path: /location\n  description: Query monitoring locations\n- path: /parameter\n  description: Query measured parameters\n- path: /result\n  description: Query time series results\n- path: /reclamation-region\n  description: Query Reclamation regions\n- path: /model-run\n  description: Query model run data\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bureau-of-reclamation/refs/heads/main/apis.yml
tags:
- Federal Government
- Water
- Hydrology
- Time Series
---
