---
aid: microsoft-azure:postgresqlmanagementclient
baseURL: ''
description: Microsoft Azure Postgre Sql management Client is a tool designed to help users easily manage and interact with their Postgre Sql databases hosted on the Microsoft Azure cloud platform. With this client, users can perform a variety of tasks such as creating and managing databases, tables, and indexes, executing SQL queries, and monitoring database performance.
humanURL: https://learn.microsoft.com/en-us/dotnet/api/overview/azure/resourcemanager.postgresql-readme?view=azure-dotnet
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Postgre SQLmanagement Client
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/postgresqlmanagementclient-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/dotnet/api/overview/azure/resourcemanager.postgresql-readme?view=azure-dotnet
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: postgresqlmanagementclient
source_filename: postgresqlmanagementclient-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: 2023-06-01-preview\n  title: Microsoft Azure PostgreSQLManagementClient\n  description: >-\n    The Microsoft Azure management API provides create, read, update, and delete\n    functionality for Azure PostgreSQL resources including servers, databases,\n    firewall rules, VNET rules, security alert policies, log files and\n    configurations with new business model.\nhost: management.azure.com\nschemes:\n  - https\nconsumes:\n  - application/json\nproduces:\n  - application/json\nsecurity:\n  - azure_auth:\n      - user_impersonation\nsecurityDefinitions:\n  azure_auth:\n    type: oauth2\n    authorizationUrl: https://login.microsoftonline.com/common/oauth2/authorize\n    flow: implicit\n    description: Azure Active Directory OAuth2 Flow\n    scopes:\n      user_impersonation: impersonate your user account\npaths:\n  /providers/Microsoft.DBforPostgreSQL/getPrivateDnsZoneSuffix:\n    post:\n      tags:\n        - GetPrivateDnsZoneSuffix\n\
  \      operationId: microsoftAzureGetprivatednszonesuffixExecute\n      x-ms-examples:\n        GetPrivateDnsZoneSuffix:\n          $ref: ./examples/GetPrivateDnsZoneSuffix.json\n      description: Get private DNS zone suffix in the cloud\n      parameters:\n        - $ref: >-\n            ../../../../../common-types/resource-management/v5/types.json#/parameters/ApiVersionParameter\n      responses:\n        '200':\n          description: OK\n          schema:\n            $ref: '#/definitions/PrivateDnsZoneSuffix'\n        default:\n          description: Error response describing why the operation failed.\n          schema:\n            $ref: >-\n              ../../../../../common-types/resource-management/v5/types.json#/definitions/ErrorResponse\n      summary: Microsoft Azure Post Providers Microsoft Dbforpostgresql Getprivatednszonesuffix\ndefinitions:\n  PrivateDnsZoneSuffix:\n    type: string\n    description: Represents a resource name availability.\ntags:\n  - name: GetPrivateDnsZoneSuffix\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/postgresqlmanagementclient-openapi-original.yml
tags: []
---
