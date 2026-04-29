---
aid: peoplesoft:notification-framework-api
baseURL: https://{hostname}:{port}/psft/api/notifications/v1
description: Push notification and event-driven notification services including the Notification Composer for email, text, and in-app notifications. Requires PeopleTools 8.59.19+.
humanURL: https://docs.oracle.com/cd/E41507_01/epm91pbr3/eng/epm/eewe/concept_PeopleSoftEventsandNotificationsFrameworkOverview-227ff2.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Notification Framework API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E41507_01/epm91pbr3/eng/epm/eewe/concept_PeopleSoftEventsandNotificationsFrameworkOverview-227ff2.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/notification-framework.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: notification-framework-api
source_filename: notification-framework.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Notification Framework API\n  description: Push notification and event-driven notification services including the Notification Composer for email, text, and in-app notifications. Requires PeopleTools 8.59.19+.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/notifications/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: Events and Notifications Framework Documentation\n  url: https://docs.oracle.com/cd/E41507_01/epm91pbr3/eng/epm/eewe/concept_PeopleSoftEventsandNotificationsFrameworkOverview-227ff2.html\ntags:\n- name: Notifications\n\
  \  description: Notification management operations\npaths:\n  /notifications:\n    get:\n      summary: PeopleSoft List Notifications\n      description: Retrieve a list of notifications for the current user.\n      operationId: listNotifications\n      tags:\n      - Notifications\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with notifications\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  notifications:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        id:\n                          type: string\n                        message:\n                          type: string\n                        type:\n                          type: string\n                        timestamp:\n                          type:\
  \ string\n                          format: date-time\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    post:\n      summary: PeopleSoft Send Notification\n      description: Send a notification via email, text, or in-app channels.\n      operationId: sendNotification\n      tags:\n      - Notifications\n      security:\n      - basicAuth: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                channel:\n                  type: string\n                  enum:\n                  - email\n                  - text\n                  - in-app\n                recipients:\n                  type: array\n                  items:\n                    type: string\n                message:\n                  type: string\n      responses:\n        '202':\n          description: Notification\
  \ queued\n        '400':\n          description: Bad request\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/notification-framework.yml
tags:
- Events
- Messaging
- Notifications
- Push Notifications
---
