---
aid: bigcommerce:bigcommerce-storefront-cookie-consent
baseURL: https://api.example.com
description: The BigCommerce Storefront Cookie Consent app is designed to help online store owners comply with global data protection laws by providing a user-friendly way to inform website visitors about the use of cookies. This app allows businesses to customize their cookie consent banners to match their branding and messaging. By obtaining consent from users before placing cookies on their devices, store owners can enhance data privacy and build trust with customers.
humanURL: https://developer.bigcommerce.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Big Commerce Storefront Cookie Consent
properties:
- type: Documentation
  url: https://developer.bigcommerce.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bigcommerce/refs/heads/main/openapi/storefront-cookie-consent-openapi-original.yml
provider_name: BigCommerce
provider_slug: bigcommerce
slug: bigcommerce-storefront-cookie-consent
source_filename: storefront-cookie-consent-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.1\nservers:\n  - url: https://{store_domain}/api/storefront\n    variables:\n      store_domain:\n        default: your_store.example.com\n        description: >-\n          The [URL\n          authority](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL#authority)\n          of the storefront.\ninfo:\n  title: BigCommerce Storefront Cookie Consent\n  description: >-\n    Specify shopper cookie consent preferences.\n\n\n    For info about API accounts, see our [Guide to API\n    Accounts](/docs/start/authentication/api-accounts).\n        \n    For info about authenticating BigCommerce APIs, see [Authentication and\n    Example\n    Requests](/docs/start/authentication#same-origin-cors-authentication).\n  version: Storefront\ntags:\n  - name: Consent\npaths:\n  /consent:\n    post:\n      summary: BigCommerce Set Cookie Consent Preferences\n      tags:\n        - Consent\n      responses:\n        '200':\n          description:\
  \ Consent Settings Saved\n        '400':\n          description: Invalid input\n      requestBody:\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/ConsentPreferences'\n            examples:\n              Example:\n                value:\n                  allow:\n                    - 2\n                    - 3\n                  deny:\n                    - 4\n        description: >-\n          Data sent to the [Update customer\n          consent](/docs/rest-management/customers/customer-consent#update-customer-consent)\n          endpoint when creating a customer during checkout.\n        required: true\n      description: >\n        Sets the status of a customer's consent to allow data collection by\n        cookies and scripts according to the following consent categories:\n\n\n          2. Analytics — These cookies provide statistical information on site usage so the store owner can improve the website over time.  \n\
  \          3. Functional — These cookies enable enhanced functionality, such as videos and live chat. If a shopper does not allow these, then some or all of these functions may not work properly. \n          4. Targeting; Advertising — These cookies allow merchants to create profiles or personalize content to enhance users' shopping experience.\n          \n          \n        This endpoint only works if the cookie consent feature is enabled. It is\n        assumed the shopper has not consented to anything until a value is\n        explicitly set. The request body must be populated with a complete set\n        of allowed and denied categories.\n\n\n        Once set, consent preferences will be saved as a cookie for guest\n        shoppers. Consent preferences will be persisted to a shopper's account\n        to be used for future sessions once they have logged in. Consent\n        preferences can also be managed using the [Update customer\n        consent](/docs/rest-management/customers/customer-consent#update-customer-consent)\n\
  \        endpoint.   \n\n\n        > #### Note\n\n        > * Substitute your storefront domain for `yourstore.example.com`. \n      operationId: postCookieConsent\n    parameters: []\ncomponents:\n  schemas:\n    ConsentPreferences:\n      type: object\n      title: ConsentPreferences\n      description: >-\n        List of allowed and denied consent categories. Must be populated with a\n        complete set of allowed and denied categories.\n\n\n        Configurable categories are:\n\n\n        2 - Functional\n\n        3 - Analytics\n\n        4 - Targeting; Advertising\n\n\n        For further definition of these categories, see [Scripts\n        API](/docs/integrations/scripts).\n      properties:\n        allow:\n          type: array\n          description: Explicitly allowed consent categories. Allowed values are 2, 3, 4.\n          items:\n            type: integer\n            enum:\n              - 2\n              - 3\n              - 4\n            example: 3\n        deny:\n\
  \          type: array\n          description: Denied consent categories. Allowed values are 2, 3, 4.\n          items:\n            type: integer\n            enum:\n              - 2\n              - 3\n              - 4\n            example: 4\n      required:\n        - allow\n        - deny\n      x-internal: false\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bigcommerce/refs/heads/main/openapi/storefront-cookie-consent-openapi-original.yml
tags:
- Consents
- Cookies
- Storefronts
---
