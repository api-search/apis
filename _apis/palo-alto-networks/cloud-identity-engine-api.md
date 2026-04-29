---
aid: palo-alto-networks:cloud-identity-engine-api
baseURL: https://api.strata.paloaltonetworks.com
description: A REST API for the Cloud Identity Engine (CIE) Directory Sync Service that aggregates, normalizes, and provides access to enterprise identity data from multiple directory sources through a unified API. Supports synchronization of user, group, and organizational unit data from Active Directory, Azure Active Directory, Okta, Google Workspace, and PingFederate. Provides enriched user context including device, location, and logon event data for identity-aware security policies.
humanURL: https://pan.dev/scm/api/config/ciedss/ciedss/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cloud Identity Engine API
properties:
- type: Documentation
  url: https://pan.dev/scm/api/config/ciedss/ciedss/
- type: GettingStarted
  url: https://pan.dev/scm/docs/getstarted/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-cloud-identity-engine-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-attr_based_filter-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-check_group_membership-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-check_user_in_particular_group-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-domain_param-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-fetch_all_users_attrs-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-group_filter-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-list_all_groups_in_domain-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-list_all_users_in_domain-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-list_groups_user_belongs_to-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-list_specific_groups-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-list_specific_users-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-list_users_in_particular_group-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cloud-identity-engine-api-pagination_params-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-attr_based_filter-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-check_group_membership-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-check_user_in_particular_group-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-domain_param-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-fetch_all_users_attrs-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-group_filter-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-list_all_groups_in_domain-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-list_all_users_in_domain-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-list_groups_user_belongs_to-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-list_specific_groups-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-list_specific_users-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-list_users_in_particular_group-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cloud-identity-engine-api-pagination_params-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-cloud-identity-engine-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-attr_based_filter-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-check_group_membership-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-check_user_in_particular_group-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-domain_param-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-fetch_all_users_attrs-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-group_filter-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-list_all_groups_in_domain-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-list_all_users_in_domain-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-list_groups_user_belongs_to-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-list_specific_groups-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-list_specific_users-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-list_users_in_particular_group-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cloud-identity-engine-api-pagination_params-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: cloud-identity-engine-api
source_yaml: "aid: palo-alto-networks:cloud-identity-engine-api\nname: Cloud Identity Engine API\ntags:\n- Active Directory\n- Azure AD\n- Cloud Identity\n- Directory Sync\n- Identity\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.strata.paloaltonetworks.com\nhumanURL: https://pan.dev/scm/api/config/ciedss/ciedss/\nproperties:\n- url: https://pan.dev/scm/api/config/ciedss/ciedss/\n  type: Documentation\n- url: https://pan.dev/scm/docs/getstarted/\n  type: GettingStarted\n- url: openapi/palo-alto-cloud-identity-engine-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/cloud-identity-engine-api-attr_based_filter-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-check_group_membership-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-check_user_in_particular_group-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-domain_param-schema.json\n\
  \  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-fetch_all_users_attrs-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-group_filter-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-list_all_groups_in_domain-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-list_all_users_in_domain-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-list_groups_user_belongs_to-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-list_specific_groups-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-list_specific_users-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-list_users_in_particular_group-schema.json\n  type: JSONSchema\n- url: json-schema/cloud-identity-engine-api-pagination_params-schema.json\n  type: JSONSchema\n- url: json-structure/cloud-identity-engine-api-attr_based_filter-structure.json\n\
  \  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-check_group_membership-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-check_user_in_particular_group-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-domain_param-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-fetch_all_users_attrs-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-group_filter-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-list_all_groups_in_domain-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-list_all_users_in_domain-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-list_groups_user_belongs_to-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-list_specific_groups-structure.json\n  type: JSONStructure\n\
  - url: json-structure/cloud-identity-engine-api-list_specific_users-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-list_users_in_particular_group-structure.json\n  type: JSONStructure\n- url: json-structure/cloud-identity-engine-api-pagination_params-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-cloud-identity-engine-api-context.jsonld\n  type: JSON-LD\n- url: examples/cloud-identity-engine-api-attr_based_filter-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-check_group_membership-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-check_user_in_particular_group-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-domain_param-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-fetch_all_users_attrs-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-group_filter-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-list_all_groups_in_domain-example.json\n\
  \  type: Example\n- url: examples/cloud-identity-engine-api-list_all_users_in_domain-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-list_groups_user_belongs_to-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-list_specific_groups-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-list_specific_users-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-list_users_in_particular_group-example.json\n  type: Example\n- url: examples/cloud-identity-engine-api-pagination_params-example.json\n  type: Example\ndescription: A REST API for the Cloud Identity Engine (CIE) Directory Sync Service that aggregates, normalizes,\n  and provides access to enterprise identity data from multiple directory sources through a unified API.\n  Supports synchronization of user, group, and organizational unit data from Active Directory, Azure Active\n  Directory, Okta, Google Workspace, and PingFederate. Provides enriched\
  \ user context including device,\n  location, and logon event data for identity-aware security policies.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Active Directory
- Azure AD
- Cloud Identity
- Directory Sync
- Identity
---
