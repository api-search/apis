---
aid: apache-event-mesh:eventmesh-messaging-api
baseURL: ''
description: Event-driven messaging via TCP, HTTP, and gRPC protocols. Events follow the CloudEvents specification. Supports pub-sub, request-reply, and broadcast messaging patterns.
humanURL: https://eventmesh.apache.org/docs/sdk-java/tcp-sdk-usage
image: ''
layout: api
name: Apache EventMesh Messaging API
properties:
- type: Documentation
  url: https://eventmesh.apache.org/docs/sdk-java/tcp-sdk-usage
- type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/apache-event-mesh/refs/heads/main/asyncapi/eventmesh-messaging.yml
provider_name: Apache EventMesh
provider_slug: apache-event-mesh
slug: eventmesh-messaging-api
source_filename: eventmesh-messaging.yml
source_heading: AsyncAPI Specification
source_yaml: "asyncapi: 2.6.0\ninfo:\n  title: Apache EventMesh Messaging API\n  version: 1.10.0\n  description: >-\n    Apache EventMesh provides event-driven messaging via multiple protocols\n    including TCP, HTTP, and gRPC. Events follow the CloudEvents specification.\n    EventMesh decouples event producers and consumers, supporting pub-sub,\n    request-reply, and broadcast messaging patterns.\n  contact:\n    name: Apache EventMesh\n    url: https://eventmesh.apache.org/\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nservers:\n  tcp:\n    url: localhost:10000\n    protocol: tcp\n    description: EventMesh TCP endpoint\n  grpc:\n    url: localhost:10205\n    protocol: grpc\n    description: EventMesh gRPC endpoint\ndefaultContentType: application/cloudevents+json\nchannels:\n  '{topic}':\n    description: >-\n      EventMesh topic for pub-sub messaging. Events are published to topics\n      and delivered to all subscribed consumer groups.\n\
  \    parameters:\n      topic:\n        description: The topic name\n        schema:\n          type: string\n    publish:\n      operationId: publishEvent\n      summary: Publish a CloudEvent to a topic\n      message:\n        $ref: '#/components/messages/CloudEventMessage'\n    subscribe:\n      operationId: subscribeEvent\n      summary: Subscribe to events on a topic\n      message:\n        $ref: '#/components/messages/CloudEventMessage'\n  '{topic}/request':\n    description: >-\n      EventMesh request-reply channel. A producer sends a request event and\n      awaits a reply event from a consumer.\n    parameters:\n      topic:\n        schema:\n          type: string\n    publish:\n      operationId: requestEvent\n      summary: Send a request event and await reply\n      message:\n        $ref: '#/components/messages/CloudEventMessage'\n    subscribe:\n      operationId: replyEvent\n      summary: Receive request and send reply\n      message:\n        $ref: '#/components/messages/CloudEventMessage'\n\
  \  '{topic}/broadcast':\n    description: >-\n      EventMesh broadcast channel. Events are delivered to all connected\n      consumers regardless of consumer group.\n    parameters:\n      topic:\n        schema:\n          type: string\n    publish:\n      operationId: broadcastEvent\n      summary: Broadcast a CloudEvent to all consumers\n      message:\n        $ref: '#/components/messages/CloudEventMessage'\n    subscribe:\n      operationId: receiveBroadcast\n      summary: Receive broadcast events\n      message:\n        $ref: '#/components/messages/CloudEventMessage'\ncomponents:\n  messages:\n    CloudEventMessage:\n      name: CloudEventMessage\n      title: CloudEvent Message\n      summary: A CloudEvents v1.0 compliant event routed through EventMesh\n      contentType: application/cloudevents+json\n      headers:\n        type: object\n        properties:\n          ce-specversion:\n            type: string\n            const: \"1.0\"\n          ce-id:\n            type: string\n\
  \          ce-source:\n            type: string\n          ce-type:\n            type: string\n          ce-time:\n            type: string\n            format: date-time\n          ce-subject:\n            type: string\n          ce-datacontenttype:\n            type: string\n          env:\n            type: string\n            description: EventMesh environment\n          idc:\n            type: string\n            description: EventMesh IDC\n          sys:\n            type: string\n            description: EventMesh system\n          pid:\n            type: string\n            description: Producer/consumer process ID\n          group:\n            type: string\n            description: Consumer group\n      payload:\n        type: object\n        description: The CloudEvent data payload\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-event-mesh/refs/heads/main/asyncapi/eventmesh-messaging.yml
tags:
- CloudEvents
- Event-Driven
- Messaging
- Pub-Sub
---
