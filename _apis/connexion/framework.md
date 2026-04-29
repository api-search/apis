---
aid: connexion:framework
baseURL: https://connexion.readthedocs.io
description: Connexion is a contract-first Python web framework that loads an OpenAPI specification and routes requests to Python handlers based on operationId. It performs request validation, parameter parsing, and response validation against the specification, with first-class support for security schemes and Swagger UI.
humanURL: https://connexion.readthedocs.io/en/latest/
image: ''
layout: api
name: Connexion Python Framework
properties:
- type: Documentation
  url: https://connexion.readthedocs.io/en/latest/
- type: Documentation
  url: https://connexion.readthedocs.io/en/latest/quickstart.html
- type: GitHubRepository
  url: https://github.com/spec-first/connexion
- type: License
  url: https://github.com/spec-first/connexion/blob/main/LICENSE
- type: Issue Tracker
  url: https://github.com/spec-first/connexion/issues
provider_name: Connexion
provider_slug: connexion
slug: framework
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: connexion:framework\nname: Connexion Python Framework\ndescription: Connexion is a contract-first Python web framework that loads an OpenAPI specification and\n  routes requests to Python handlers based on operationId. It performs request validation, parameter parsing,\n  and response validation against the specification, with first-class support for security schemes and\n  Swagger UI.\nhumanURL: https://connexion.readthedocs.io/en/latest/\nbaseURL: https://connexion.readthedocs.io\ntags:\n- Framework\n- OpenAPI\n- Python\n- Validation\nproperties:\n- type: Documentation\n  url: https://connexion.readthedocs.io/en/latest/\n- type: Documentation\n  url: https://connexion.readthedocs.io/en/latest/quickstart.html\n- type: GitHubRepository\n  url: https://github.com/spec-first/connexion\n- type: License\n  url: https://github.com/spec-first/connexion/blob/main/LICENSE\n- type: Issue Tracker\n  url: https://github.com/spec-first/connexion/issues\nx-features:\n- AsyncApp, FlaskApp,\
  \ and ConnexionMiddleware entry points\n- Native ASGI server support and Flask compatibility\n- Automatic routing from operationId via RestyResolver\n- Request and response validation against OpenAPI\n- Security middleware honoring OpenAPI security schemes\n- Swagger UI mounted from the framework\n- Pythonic snake_case parameter conversion\n- Strict parameter validation modes\nx-useCases:\n- Build Python APIs from an OpenAPI 3.x specification\n- Migrate Flask applications to a contract-first model\n- Add request and response validation to an existing ASGI app\n- Generate Swagger UI alongside your API automatically\n- Compose multiple OpenAPI specifications under a single app\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/connexion/refs/heads/main/apis.yml
tags:
- Framework
- OpenAPI
- Python
- Validation
---
