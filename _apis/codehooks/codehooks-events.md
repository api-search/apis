---
aid: codehooks:codehooks-events
baseURL: ''
description: Asynchronous CRUD lifecycle hooks (onBeforeCreate, onAfterCreate, onBeforeRead, onAfterRead, onBeforeUpdate, onAfterUpdate, onBeforeDelete, onAfterDelete) and queue worker processing (onQueueJob) for serverless backend operations. AsyncAPI describes these as event-driven channels backed by an internal pub/sub and persistent queue runtime.
humanURL: https://codehooks.io/docs/hooks-and-workers
image: ''
layout: api
name: Codehooks Events (AsyncAPI)
properties:
- type: Documentation
  url: https://codehooks.io/docs/hooks-and-workers
- type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/codehooks/refs/heads/main/asyncapi/codehooks-events-asyncapi.yml
provider_name: Codehooks
provider_slug: codehooks
slug: codehooks-events
source_yaml: "aid: codehooks:codehooks-events\nname: Codehooks Events (AsyncAPI)\ntags:\n- Async\n- Events\n- Hooks\n- Lifecycle\n- Queues\n- Workers\nhumanURL: https://codehooks.io/docs/hooks-and-workers\nproperties:\n- url: https://codehooks.io/docs/hooks-and-workers\n  type: Documentation\n- url: asyncapi/codehooks-events-asyncapi.yml\n  type: AsyncAPI\ndescription: Asynchronous CRUD lifecycle hooks (onBeforeCreate, onAfterCreate, onBeforeRead, onAfterRead,\n  onBeforeUpdate, onAfterUpdate, onBeforeDelete, onAfterDelete) and queue worker processing (onQueueJob)\n  for serverless backend operations. AsyncAPI describes these as event-driven channels backed by an internal\n  pub/sub and persistent queue runtime.\nx-features:\n- Eight CRUD lifecycle hooks (before/after for each verb)\n- Queue worker (onQueueJob) for deferred work\n- Automatic retry and persistent state on workers\n- CRON-triggered jobs with multi-schedule support\n- Stateful workflow orchestration\nx-use-cases:\n- Validation\
  \ and transformation on writes\n- Audit logging and outbound webhooks\n- PDF/email generation deferred to a worker\n- AI inference pipelines triggered after document creation\n- Scheduled batch jobs (CRON)\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/codehooks/refs/heads/main/apis.yml
tags:
- Async
- Events
- Hooks
- Lifecycle
- Queues
- Workers
---
