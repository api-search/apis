---
aid: connexion:middleware
baseURL: https://connexion.readthedocs.io
description: Connexion 3 introduces a stack of pluggable ASGI middlewares that handle exceptions, server errors, lifespan, security, routing, request validation, response validation, Swagger UI, and context propagation. The middleware stack can be applied to any ASGI or WSGI application via ConnexionMiddleware.
humanURL: https://connexion.readthedocs.io/en/latest/middleware.html
image: ''
layout: api
name: Connexion Middleware Stack
properties:
- type: Documentation
  url: https://connexion.readthedocs.io/en/latest/middleware.html
- type: Reference
  url: https://github.com/spec-first/connexion/tree/main/connexion/middleware
provider_name: Connexion
provider_slug: connexion
slug: middleware
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: connexion:middleware\nname: Connexion Middleware Stack\ndescription: Connexion 3 introduces a stack of pluggable ASGI middlewares that handle exceptions, server\n  errors, lifespan, security, routing, request validation, response validation, Swagger UI, and context\n  propagation. The middleware stack can be applied to any ASGI or WSGI application via ConnexionMiddleware.\nhumanURL: https://connexion.readthedocs.io/en/latest/middleware.html\nbaseURL: https://connexion.readthedocs.io\ntags:\n- ASGI\n- Middleware\n- WSGI\nproperties:\n- type: Documentation\n  url: https://connexion.readthedocs.io/en/latest/middleware.html\n- type: Reference\n  url: https://github.com/spec-first/connexion/tree/main/connexion/middleware\nx-features:\n- Routing, security, request, and response validation middleware\n- SwaggerUIMiddleware for interactive docs\n- LifespanMiddleware for startup and shutdown hooks\n- ContextMiddleware to propagate request context\nx-useCases:\n- Add Connexion validation\
  \ to FastAPI or Starlette\n- Wrap an existing WSGI application without rewriting handlers\n- Customize the middleware stack for a specific deployment\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/connexion/refs/heads/main/apis.yml
tags:
- ASGI
- Middleware
- WSGI
---
