swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 1
info:
  title: plentymarkets REST-API
  description: the-plentymarkets-rest-api-expands-the-functionality-of-the-plentymarkets-cms-and-allows-access-to-resources-i-e--data-records-via-unique-uri-paths
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/storage/frontend/file:
    get:
      summary: Get file information for a single object in frontend storage. Append
        public cloudfront url to retrieved object.
      description: Get file information for a single object in frontend storage. append
        public cloudfront url to retrieved object..
      operationId: getRestStorageFrontendFile
      x-api-path-slug: reststoragefrontendfile-get
      parameters:
      - in: query
        name: key
        description: The key of the object to get information about
      responses:
        200:
          description: OK
      tags:
      - File
      - Informationa
      - Single
      - Object
      - In
      - Frontend
      - Storage
      - ""
      - Append
      - Public
      - Cloudfront
      - Url
      - To
      - Retrieved
      - Object
  /rest/storage/frontend/files:
    get:
      summary: List files from frontend storage. Append public cloudfront url to each
        retrieved object.
      description: List files from frontend storage. append public cloudfront url
        to each retrieved object..
      operationId: getRestStorageFrontendFiles
      x-api-path-slug: reststoragefrontendfiles-get
      parameters:
      - in: query
        name: continuationToken
        description: The continuationToken of a previous request to continue listing
          objects with
      responses:
        200:
          description: OK
      tags:
      - List
      - Files
      - From
      - Frontend
      - Storage
      - ""
      - Append
      - Public
      - Cloudfront
      - Url
      - To
      - Each
      - Retrieved
      - Object