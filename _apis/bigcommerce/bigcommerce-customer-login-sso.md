---
aid: bigcommerce:bigcommerce-customer-login-sso
baseURL: https://api.example.com
description: BigCommerce Customer Login (SSO) is a feature that allows customers to easily access their account on a BigCommerce site by logging in using a single set of credentials. This seamless process eliminates the need for customers to remember multiple usernames and passwords for different websites, enhancing their user experience. By implementing SSO, businesses can improve customer satisfaction, reduce friction during the checkout process, and potentially increase conversions.
humanURL: https://developer.bigcommerce.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Big Commerce Customer Login (Sso)
properties:
- type: Documentation
  url: https://developer.bigcommerce.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bigcommerce/refs/heads/main/openapi/customer-login-sso-openapi-original.yml
provider_name: BigCommerce
provider_slug: bigcommerce
slug: bigcommerce-customer-login-sso
source_filename: customer-login-sso-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.1\ninfo:\n  title: BigCommerce Customer Login (SSO)\n  description: >-\n    Enable single sign-on for shoppers on BigCommerce hosted storefronts.\n\n\n    [Learn more about the customer login\n    API](/docs/start/authentication/customer-login).\n\n\n    For info about API accounts, see our [Guide to API\n    Accounts](/docs/start/authentication/api-accounts).\n        \n    For info about authenticating BigCommerce APIs, see [Authentication and\n    Example Requests](/docs/start/authentication#user-generated-jwts).\n  termsOfService: https://www.bigcommerce.com/terms\n  contact:\n    name: BigCommerce\n    url: https://www.bigcommerce.com\n    email: support@bigcommerce.com\n  version: ''\nservers:\n  - url: https://{store_domain}\n    variables:\n      store_domain:\n        default: your_store.example.com\n        description: >-\n          The [URL\n          authority](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL#authority)\n\
  \          of the storefront.\ntags:\n  - name: Login Token\npaths:\n  /login/token/{jwt_token}:\n    get:\n      tags:\n        - Login Token\n      summary: BigCommerce Login Token\n      operationId: getCustomerLogin\n      description: >-\n        The customer login access point URL.\n\n\n        [Learn more about the Customer Login\n        API](/docs/start/authentication/customer-login).\n\n\n        ## Example\n\n\n        ```\n\n        https://yourstore.example.com/login/token/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJ7Y2xpZW50X2lkfSIsImlhdCI6MTUzNTM5MzExMywianRpIjoie3V1aWR9Iiwib3BlcmF0aW9uIjoiY3VzdG9tZXJfbG9naW4iLCJzdG9yZV9oYXNoIjoie3N0b3JlX2hhc2h9IiwiY3VzdG9tZXJfaWQiOjJ9.J-fAtbjRFGdLsT744DhoprFEDqIfVq72HbDzrbFy6Is\n\n        ```\n      parameters:\n        - name: jwt_token\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: OK\n          content:\n            '*/*':\n    \
  \          schema:\n                type: object\ncomponents:\n  schemas:\n    customerLoginSSO:\n      title: Customer Login SSO\n      type: object\n      properties:\n        iss:\n          type: string\n          description: >-\n            Indicates the token’s issuer. This is your application’s client ID,\n            which is obtained during application registration in Developer\n            Portal.\n          example: '\"1234r5t6y7u8i9o0p\"'\n        iat:\n          type: integer\n          description: >-\n            Time when the token was generated. This is a numeric value\n            indicating the number of seconds since the [Unix\n            epoch](https://en.wikipedia.org/wiki/Unix_time).\n          example: 1535393113\n        jti:\n          type: string\n          description: >-\n            Request ID string that must be unique across all requests made by\n            your app. A UUID or other random string would be an appropriate\n            value. Most libraries\
  \ contain a method for generating a uuid. For\n            testing a [UUID generator](https://www.uuidgenerator.net/) can be\n            used, but it recommended to use built in libraries.\n          example: '\"20b7c03e-00da-4d29-91bf-2aa06a57575b\"'\n        operation:\n          type: string\n          description: Must contain the string “customer_login”.\n          example: '\"customer_login\"'\n        store_hash:\n          type: string\n          description: |\n            Store hash identifying the store you are logging into.\n          example: '\"abc123\"'\n        customer_id:\n          type: integer\n          description: >\n            ID of the customer you are logging in, as obtained through the\n            Customer API.\n          example: 2\n        redirect_to:\n          type: string\n          description: >\n            Optional field containing a relative path for the shopper’s\n            destination after login. Will default to `/account.php`.\n         \
  \ default: /account.php\n        request_ip:\n          type: string\n          description: >\n            **(Optional)** Field containing the expected IP address for the\n            request. If provided, BigCommerce will check that it matches the\n            browser trying to log in. If there is not a match, it will be\n            rejected.\n          example: '\"111.222.333.444\"'\n      x-internal: false\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bigcommerce/refs/heads/main/openapi/customer-login-sso-openapi-original.yml
tags:
- Customers
- Logins
- Single-Sign-On
- SSO
---
