---
aid: canvas:canvas-lms-rest-api
baseURL: ''
description: The Canvas LMS REST API provides programmatic access to courses, assignments, quizzes, grades, users, enrollments, accounts, discussions, files, modules, rubrics, submissions, SIS imports, and account administration. It uses OAuth 2.0 access tokens and returns JSON with ISO 8601 timestamps, supporting pagination, request throttling, masquerading, and compound documents.
humanURL: https://canvas.instructure.com/doc/api/
image: ''
layout: api
name: Canvas LMS REST API
properties:
- type: Documentation
  url: https://canvas.instructure.com/doc/api/
- type: Authentication
  url: https://canvas.instructure.com/doc/api/file.oauth.html
- type: Pagination
  url: https://canvas.instructure.com/doc/api/file.pagination.html
- type: GitHub Repository
  url: https://github.com/instructure/canvas-lms
provider_name: Canvas
provider_slug: canvas
slug: canvas-lms-rest-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: canvas:canvas-lms-rest-api\nname: Canvas LMS REST API\ndescription: The Canvas LMS REST API provides programmatic access to courses, assignments, quizzes, grades,\n  users, enrollments, accounts, discussions, files, modules, rubrics, submissions, SIS imports, and account\n  administration. It uses OAuth 2.0 access tokens and returns JSON with ISO 8601 timestamps, supporting\n  pagination, request throttling, masquerading, and compound documents.\nhumanURL: https://canvas.instructure.com/doc/api/\ntags:\n- Education\n- LMS\n- REST\nproperties:\n- type: Documentation\n  url: https://canvas.instructure.com/doc/api/\n- type: Authentication\n  url: https://canvas.instructure.com/doc/api/file.oauth.html\n- type: Pagination\n  url: https://canvas.instructure.com/doc/api/file.pagination.html\n- type: GitHub Repository\n  url: https://github.com/instructure/canvas-lms\nx-features:\n- OAuth 2.0 authentication with access tokens\n- JSON responses with ISO 8601 timestamps\n- 64-bit\
  \ integer IDs and string ID support\n- Form-encoded and JSON request bodies\n- Pagination for large result sets\n- Request throttling and quota controls\n- Masquerading for acting on behalf of users\n- Compound documents for linked resources\n- File upload workflows\n- SIS imports and roster sync\n- Live event streams via Canvas Data services\n- Caliper event format compatibility\n- xAPI statement support\nx-use-cases:\n- Building custom student dashboards or mobile apps\n- Automating course provisioning and enrollment via SIS imports\n- Syncing grades and assignments to external gradebooks\n- Analytics and learning-event data pipelines\n- Integrating third-party tools through LTI\n- Bulk content migration between courses or institutions\n- Institutional reporting and audit-log extraction\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/canvas/refs/heads/main/apis.yml
tags:
- Education
- LMS
- REST
---
