---
swagger: "2.0"
x-collection-name: AWS OpsWorks
x-complete: 0
info:
  title: AWS OpsWorks API Update My User Profile
  version: 1.0.0
  description: Updates a user's SSH public key.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeMyUserProfile:
    get:
      summary: Describe My User Profile
      description: Describes a user's SSH information.
      operationId: describeMyUserProfile
      x-api-path-slug: actiondescribemyuserprofile-get
      parameters:
      - in: query
        name: UserProfile
        description: A UserProfile object that describes the users SSH information
        type: string
      responses:
        200:
          description: OK
      tags:
      - Describe
      - My
      - User
      - Profile
  /?Action=UpdateMyUserProfile:
    get:
      summary: Update My User Profile
      description: Updates a user's SSH public key.
      operationId: updateMyUserProfile
      x-api-path-slug: actionupdatemyuserprofile-get
      parameters:
      - in: query
        name: SshPublicKey
        description: The users SSH public key
        type: string
      responses:
        200:
          description: OK
      tags:
      - My
      - User
      - Profile
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