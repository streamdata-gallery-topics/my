---
swagger: "2.0"
x-collection-name: Reverb
x-complete: 0
info:
  title: Reverb Post My Curated Set Product Product
  description: Post my curated set product product.
  termsOfService: https://reverb.com/page/terms
  contact:
    name: Reverb API
    url: https://dev.reverb.com
    email: integrations@reverb.com
  version: "3.0"
host: api.reverb.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /my/account:
    get:
      summary: Get My Account
      description: Get account details
      operationId: getMyAccount
      x-api-path-slug: myaccount-get
      responses:
        200:
          description: OK
      tags:
      - My
      - Account
    put:
      summary: Put My Account
      description: Update account details
      operationId: putMyAccount
      x-api-path-slug: myaccount-put
      parameters:
      - in: body
        name: body
        description: the content of the request
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - My
      - Account
  /my/addresses:
    get:
      summary: Get My Addresses
      description: See all addresses in your address book
      operationId: getMyAddresses
      x-api-path-slug: myaddresses-get
      responses:
        200:
          description: OK
      tags:
      - My
      - Addresses
    post:
      summary: Post My Addresses
      description: Create a new address in your address book
      operationId: postMyAddresses
      x-api-path-slug: myaddresses-post
      responses:
        200:
          description: OK
      tags:
      - My
      - Addresses
  /my/addresses/{address_id}:
    delete:
      summary: Delete My Addresses Address
      description: Delete an existing address in your address book
      operationId: deleteMyAddressesAddress
      x-api-path-slug: myaddressesaddress-id-delete
      parameters:
      - in: path
        name: address_id
      responses:
        200:
          description: OK
      tags:
      - My
      - Addresses
      - Address
      - Id
    put:
      summary: Put My Addresses Address
      description: Update an existing address in your address book
      operationId: putMyAddressesAddress
      x-api-path-slug: myaddressesaddress-id-put
      parameters:
      - in: path
        name: address_id
      responses:
        200:
          description: OK
      tags:
      - My
      - Addresses
      - Address
      - Id
  /my/conversations:
    get:
      summary: Get My Conversations
      description: Get a list of your conversations
      operationId: getMyConversations
      x-api-path-slug: myconversations-get
      parameters:
      - in: query
        name: offset
      - in: query
        name: page
      - in: query
        name: per_page
      - in: query
        name: search
        description: Query string to search conversations by
      - in: query
        name: unread_only
        description: Show unread conversations only
      responses:
        200:
          description: OK
      tags:
      - My
      - Conversations
    post:
      summary: Post My Conversations
      description: Post my conversations.
      operationId: postMyConversations
      x-api-path-slug: myconversations-post
      parameters:
      - in: body
        name: body
        description: the content of the request
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - My
      - Conversations
  /my/conversations/{conversation_id}/messages:
    post:
      summary: Post My Conversations Conversation Messages
      description: Post my conversations conversation messages.
      operationId: postMyConversationsConversationMessages
      x-api-path-slug: myconversationsconversation-idmessages-post
      parameters:
      - in: body
        name: body
        description: the content of the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: conversation_id
      responses:
        200:
          description: OK
      tags:
      - My
      - Conversations
      - Conversation
      - Id
      - Messages
  /my/conversations/{id}:
    get:
      summary: Get My Conversations
      description: Display conversation details with messages in natural time order
        (oldest to newest)
      operationId: getMyConversations
      x-api-path-slug: myconversationsid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - My
      - Conversations
      - Id
    put:
      summary: Put My Conversations
      description: Mark a conversation read/unread
      operationId: putMyConversations
      x-api-path-slug: myconversationsid-put
      parameters:
      - in: body
        name: body
        description: the content of the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - My
      - Conversations
      - Id
  /my/counts:
    get:
      summary: Get My Counts
      description: Get your actionable status counts
      operationId: getMyCounts
      x-api-path-slug: mycounts-get
      responses:
        200:
          description: OK
      tags:
      - My
      - Counts
  /my/curated_set/product/{product_id}:
    delete:
      summary: Delete My Curated Set Product Product
      description: Delete my curated set product product.
      operationId: deleteMyCuratedSetProductProduct
      x-api-path-slug: mycurated-setproductproduct-id-delete
      parameters:
      - in: path
        name: product_id
      responses:
        200:
          description: OK
      tags:
      - My
      - Curated
      - Set
      - Product
      - Product
      - Id
    post:
      summary: Post My Curated Set Product Product
      description: Post my curated set product product.
      operationId: postMyCuratedSetProductProduct
      x-api-path-slug: mycurated-setproductproduct-id-post
      parameters:
      - in: path
        name: product_id
      responses:
        200:
          description: OK
      tags:
      - My
      - Curated
      - Set
      - Product
      - Product
      - Id
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