---
swagger: "2.0"
x-collection-name: AWS Direct Connect
x-complete: 0
info:
  title: AWS Direct Connect API Confirm Public Virtual Interface
  version: 1.0.0
  description: Accept ownership of a public virtual interface created by another customer.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AllocatePublicVirtualInterface:
    get:
      summary: Allocate Public Virtual Interface
      description: Provisions a public virtual interface to be owned by a different
        customer.
      operationId: allocatePublicVirtualInterface
      x-api-path-slug: actionallocatepublicvirtualinterface-get
      parameters:
      - in: query
        name: connectionId
        description: The connection ID on which the public virtual interface is provisioned
        type: string
      - in: query
        name: newPublicVirtualInterfaceAllocation
        description: Detailed information for the public virtual interface to be provisioned
        type: string
      - in: query
        name: ownerAccount
        description: The AWS account that will own the new public virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
  /?Action=ConfirmPublicVirtualInterface:
    get:
      summary: Confirm Public Virtual Interface
      description: Accept ownership of a public virtual interface created by another
        customer.
      operationId: confirmPublicVirtualInterface
      x-api-path-slug: actionconfirmpublicvirtualinterface-get
      parameters:
      - in: query
        name: virtualInterfaceId
        description: ID of the virtual interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Private Virtual Interfaces
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