---
aid: convex:server-sdk
baseURL: ''
description: The Convex Server SDK (convex/server) is the TypeScript library for defining backend logic deployed on Convex. It provides primitives for writing query functions for read-only database access, mutation functions for transactional writes, and action functions for general-purpose server-side operations including calling external services. The SDK supports schema definition, full-text search indexes, vector search indexes, file storage, scheduled functions, cron jobs, and HTTP routing via the HttpRouter class.
humanURL: https://docs.convex.dev/functions
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Convex Server SDK
properties:
- type: Documentation
  url: https://docs.convex.dev/functions
- type: Documentation
  url: https://docs.convex.dev/database/schemas
provider_name: Convex
provider_slug: convex
slug: server-sdk
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: convex:server-sdk\nname: Convex Server SDK\ntags:\n- Backend\n- Database\n- Serverless Functions\n- TypeScript\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://docs.convex.dev/functions\nproperties:\n- url: https://docs.convex.dev/functions\n  type: Documentation\n- url: https://docs.convex.dev/database/schemas\n  type: Documentation\ndescription: The Convex Server SDK (convex/server) is the TypeScript library for defining backend logic\n  deployed on Convex. It provides primitives for writing query functions for read-only database access,\n  mutation functions for transactional writes, and action functions for general-purpose server-side operations\n  including calling external services. The SDK supports schema definition, full-text search indexes, vector\n  search indexes, file storage, scheduled functions, cron jobs, and HTTP routing via the HttpRouter class.\nx-features:\n- query, mutation, and action function primitives\n\
  - defineSchema and defineTable for typed database modeling\n- Full-text and vector search indexes\n- Cron jobs and scheduled function execution\n- HttpRouter for custom HTTP endpoints\n- File storage with signed URL generation\nx-useCases:\n- Authoring Convex backend functions in TypeScript\n- Modeling reactive database schemas with type safety\n- Implementing AI workflows with vector search\n- Scheduling recurring background work with cron jobs\n- Building HTTP webhook handlers inside Convex deployments\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/convex/refs/heads/main/apis.yml
tags:
- Backend
- Database
- Serverless Functions
- TypeScript
---
