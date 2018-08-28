---
swagger: "2.0"
x-collection-name: Google Compute Engine
x-complete: 0
info:
  title: Google Compute Engine API Get Router
  description: Returns the specified Router resource. Get a list of available routers
    by making a list() request.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /compute/v1/projects
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/aggregated/routers:
    get:
      summary: Get Routers
      description: Retrieves an aggregated list of routers.
      operationId: compute.routers.aggregatedList
      x-api-path-slug: projectaggregatedrouters-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Router
      - Aggregation
  /{project}/regions/{region}/routers:
    get:
      summary: Get Routers
      description: Retrieves a list of Router resources available to the specified
        project.
      operationId: compute.routers.list
      x-api-path-slug: projectregionsregionrouters-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region for this request
      responses:
        200:
          description: OK
      tags:
      - Router
    post:
      summary: Create Router
      description: Creates a Router resource in the specified project and region using
        the data included in the request.
      operationId: compute.routers.insert
      x-api-path-slug: projectregionsregionrouters-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region for this request
      responses:
        200:
          description: OK
      tags:
      - Router
  /{project}/regions/{region}/routers/{router}:
    delete:
      summary: Delete Router
      description: Deletes the specified Router resource.
      operationId: compute.routers.delete
      x-api-path-slug: projectregionsregionroutersrouter-delete
      parameters:
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region for this request
      - in: path
        name: router
        description: Name of the Router resource to delete
      responses:
        200:
          description: OK
      tags:
      - Router
    get:
      summary: Get Router
      description: Returns the specified Router resource. Get a list of available
        routers by making a list() request.
      operationId: compute.routers.get
      x-api-path-slug: projectregionsregionroutersrouter-get
      parameters:
      - in: path
        name: project
        description: Project ID for this request
      - in: path
        name: region
        description: Name of the region for this request
      - in: path
        name: router
        description: Name of the Router resource to return
      responses:
        200:
          description: OK
      tags:
      - Router
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