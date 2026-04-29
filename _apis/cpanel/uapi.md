---
aid: cpanel:uapi
baseURL: https://hostname:2083/execute
description: The cPanel User API (UAPI) is the modern HTTP API for performing cPanel-level operations such as managing email accounts, mailboxes, files, databases, FTP accounts, SSL certificates, and DNS zones for a single cPanel user. UAPI is the recommended replacement for the legacy cPanel API 2.
humanURL: https://api.docs.cpanel.net/cpanel/introduction/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: cPanel UAPI
properties:
- type: Documentation
  url: https://api.docs.cpanel.net/cpanel/introduction/
- type: GuideToUAPI
  url: https://api.docs.cpanel.net/guides/guide-to-uapi/
- type: AllUAPIFunctions
  url: https://api.docs.cpanel.net/openapi/cpanel/tag/Email/
- type: Authentication
  url: https://api.docs.cpanel.net/guides/guide-to-api-authentication/
provider_name: cPanel
provider_slug: cpanel
slug: uapi
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: cpanel:uapi\nname: cPanel UAPI\ndescription: The cPanel User API (UAPI) is the modern HTTP API for performing cPanel-level operations\n  such as managing email accounts, mailboxes, files, databases, FTP accounts, SSL certificates, and DNS\n  zones for a single cPanel user. UAPI is the recommended replacement for the legacy cPanel API 2.\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://api.docs.cpanel.net/cpanel/introduction/\nbaseURL: https://hostname:2083/execute\ntags:\n- Databases\n- Email\n- Files\n- Hosting\n- REST\n- UAPI\nproperties:\n- type: Documentation\n  url: https://api.docs.cpanel.net/cpanel/introduction/\n- type: GuideToUAPI\n  url: https://api.docs.cpanel.net/guides/guide-to-uapi/\n- type: AllUAPIFunctions\n  url: https://api.docs.cpanel.net/openapi/cpanel/tag/Email/\n- type: Authentication\n  url: https://api.docs.cpanel.net/guides/guide-to-api-authentication/\nfeatures:\n- name: Token Authentication\n\
  \  description: API tokens scoped per cPanel user.\n- name: Modular Function Catalog\n  description: Functions grouped into modules such as Email, DNS, Mysql, and Ftp.\n- name: JSON Responses\n  description: Modern JSON responses with consistent metadata envelope.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cpanel/refs/heads/main/apis.yml
tags:
- Databases
- Email
- Files
- Hosting
- REST
- UAPI
---
