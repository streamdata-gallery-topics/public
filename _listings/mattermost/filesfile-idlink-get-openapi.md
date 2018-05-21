---
swagger: "2.0"
x-collection-name: Mattermost
x-complete: 0
info:
  title: Mattermost API Get a public file link
  description: Gets a public link for a file that can be accessed without logging
    into Mattermost.
  termsOfService: https://about.mattermost.com/default-terms/
  version: 4.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /channels/{channel_id}/convert:
    post:
      summary: Convert a channel from public to private
      description: |-
        Convert into private channel from the provided channel id string.

        __Minimum server version__: 4.10

        ##### Permissions
        Must have `manage_system` permission.
      operationId: convert-into-private-channel-from-the-provided-channel-id-string-minimum-server-version--410-permiss
      x-api-path-slug: channelschannel-idconvert-post
      parameters:
      - in: path
        name: channel_id
        description: Channel GUID
      responses:
        200:
          description: OK
      tags:
      - Convert
      - Channel
      - From
      - Public
      - To
      - Private
  /teams/{team_id}/channels:
    get:
      summary: Get public channels
      description: |-
        Get a page of public channels on a team based on query string parameters - page and per_page.
        ##### Permissions
        Must be authenticated and have the `list_team_channels` permission.
      operationId: get-a-page-of-public-channels-on-a-team-based-on-query-string-parameters--page-and-per-page-permissi
      x-api-path-slug: teamsteam-idchannels-get
      parameters:
      - in: query
        name: page
        description: The page to select
      - in: query
        name: per_page
        description: The number of public channels per page
      - in: path
        name: team_id
        description: Team GUID
      responses:
        200:
          description: OK
      tags:
      - Public
      - Channels
  /files/{file_id}/link:
    get:
      summary: Get a public file link
      description: Gets a public link for a file that can be accessed without logging
        into Mattermost.
      operationId: gets-a-public-link-for-a-file-that-can-be-accessed-without-logging-into-mattermost
      x-api-path-slug: filesfile-idlink-get
      parameters:
      - in: path
        name: file_id
        description: The ID of the file to get a link for
      responses:
        200:
          description: OK
      tags:
      - Public
      - File
      - Link
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---