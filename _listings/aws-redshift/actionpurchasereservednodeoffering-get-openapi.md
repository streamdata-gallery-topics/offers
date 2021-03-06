---
swagger: "2.0"
x-collection-name: AWS Redshift
x-complete: 0
info:
  title: Amazon Redshift API Purchase Reserved Node Offering
  version: 1.0.0
  description: Allows you to purchase reserved nodes.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeReservedNodeOfferings:
    get:
      summary: Describe Reserved Node Offerings
      description: |-
        Returns a list of the available reserved node offerings by Amazon Redshift with their
                    descriptions including the node type, the fixed and recurring costs of reserving the
                    node and duration the node will be reserved for you.
      operationId: describeReservedNodeOfferings
      x-api-path-slug: actiondescribereservednodeofferings-get
      parameters:
      - in: query
        name: Marker
        description: An optional parameter that specifies the starting point to return
          a set of response            records
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of response records to return in each call
        type: string
      - in: query
        name: ReservedNodeOfferingId
        description: The unique identifier for the offering
        type: string
      responses:
        200:
          description: OK
      tags:
      - Reserved Nodes
  /?Action=PurchaseReservedNodeOffering:
    get:
      summary: Purchase Reserved Node Offering
      description: Allows you to purchase reserved nodes.
      operationId: purchaseReservedNodeOffering
      x-api-path-slug: actionpurchasereservednodeoffering-get
      parameters:
      - in: query
        name: NodeCount
        description: The number of reserved nodes that you want to purchase
        type: string
      - in: query
        name: ReservedNodeOfferingId
        description: The unique identifier of the reserved node offering you want
          to purchase
        type: string
      responses:
        200:
          description: OK
      tags:
      - Reserved Nodes
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