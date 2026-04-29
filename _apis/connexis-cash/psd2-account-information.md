---
aid: connexis-cash:psd2-account-information
baseURL: https://psd2.api.cib.bnpparibas.com/gb-account-information-psd2-stet
description: A PSD2-compliant Account Information Service (AISP) API exposed by BNP Paribas Corporate and Institutional Banking. Third-party providers consume this REST/JSON API, which follows the STET PSD2 standard, to retrieve account information for Connexis Cash users. Production uses OAuth2 Authorization Code Grant with QWAC certificates; the sandbox uses Client Credentials. Onboarded TPPs must supply QWAC certificates, callback URLs, and EBA reference codes.
humanURL: https://developers.cib.bnpparibas.com/index.php/api-docs/account-information-psd2-stet-mock
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Connexis Cash PSD2 Account Information API (STET)
properties:
- type: Documentation
  url: https://developers.cib.bnpparibas.com/index.php/api-docs/account-information-psd2-stet-mock
- type: Developer Portal
  url: https://developers.cib.bnpparibas.com/
- type: Production
  url: https://psd2.api.cib.bnpparibas.com/gb-account-information-psd2-stet
- type: Fallback
  url: https://connexis.bnpparibas.com/
provider_name: Connexis Cash
provider_slug: connexis-cash
slug: psd2-account-information
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: connexis-cash:psd2-account-information\nname: Connexis Cash PSD2 Account Information API (STET)\ndescription: A PSD2-compliant Account Information Service (AISP) API exposed by BNP Paribas Corporate\n  and Institutional Banking. Third-party providers consume this REST/JSON API, which follows the STET\n  PSD2 standard, to retrieve account information for Connexis Cash users. Production uses OAuth2 Authorization\n  Code Grant with QWAC certificates; the sandbox uses Client Credentials. Onboarded TPPs must supply QWAC\n  certificates, callback URLs, and EBA reference codes.\nhumanURL: https://developers.cib.bnpparibas.com/index.php/api-docs/account-information-psd2-stet-mock\nbaseURL: https://psd2.api.cib.bnpparibas.com/gb-account-information-psd2-stet\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\ntags:\n- AISP\n- PSD2\n- REST\n- STET\nproperties:\n- type: Documentation\n  url: https://developers.cib.bnpparibas.com/index.php/api-docs/account-information-psd2-stet-mock\n\
  - type: Developer Portal\n  url: https://developers.cib.bnpparibas.com/\n- type: Production\n  url: https://psd2.api.cib.bnpparibas.com/gb-account-information-psd2-stet\n- type: Fallback\n  url: https://connexis.bnpparibas.com/\ncontact:\n- FN: BNP Paribas PSD2 API Support\n  email: dl.cib.api.psd2.support@bnpparibas.com\nx-features:\n- PSD2 STET Compliance\n- OAuth2 Authorization Code Grant (production)\n- Client Credentials (sandbox)\n- QWAC Certificate Authentication\n- Account Balances Retrieval\n- Transaction Listing\n- Full-AISP Consent Model\nx-use-cases:\n- Aggregate Connexis Cash balances into TPP dashboards\n- Build accounting tools that pull bank data automatically\n- Power treasury software with multi-bank account access\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/connexis-cash/refs/heads/main/apis.yml
tags:
- AISP
- PSD2
- REST
- STET
---
