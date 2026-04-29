---
aid: zendesk:push-notification-devices
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Push Notification Devices API lets you register and manage the mobile devices that should receive push notifications for a given Zendesk user. With it, you can create device records using the apps push token (APNs for iOS, FCM/GCM for Android), list the devices linked to a user, update or disable a device entry, and delete registrations when a user signs out or a device is replaced.
humanURL: https://developer.zendesk.com/api-reference/ticketing/account-configuration/push_notification_devices/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Push Notification Devices API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/account-configuration/push_notification_devices/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/push-notification-devices-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: push-notification-devices
source_filename: push-notification-devices-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Push Notification Devices\n  description: Needs a description.\npaths:\n  /api/v2/push_notification_devices/destroy_many:\n    post:\n      operationId: PushNotificationDevices\n      tags:\n        - Push Notification Devices\n      summary: Zendesk Post  Api V2 Push_notification_devices Destroy_many\n      description: >-\n        Unregisters the mobile devices that are receiving push notifications.\n        Specify the devices as an array of mobile device tokens.\n\n\n        #### Allowed for\n\n\n        * Admins\n      requestBody:\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/PushNotificationDevicesRequest'\n            examples:\n              default:\n                $ref: '#/components/examples/PushNotificationDevicesRequestExample'\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n\
  \              schema:\n                type: string\n                description: empty\n                example: ''\n              example: ''\ncomponents:\n  schemas: {}\ntags:\n  - name: Push Notification Devices\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/push-notification-devices-openapi-original.yml
tags:
- Devices
- Push Notifications
---
