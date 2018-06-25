---
swagger: "2.0"
x-collection-name: AWS Cognito
x-complete: 0
info:
  title: AWS Cognito API Get Identity Pool Configuration
  version: 1.0.0
  description: Gets the configuration settings of an identity pool.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateUserPool:
    get:
      summary: Create User Pool
      description: |-
        Creates a new Amazon Cognito user pool and sets the password policy for the
                    pool.
      operationId: createUserPool
      x-api-path-slug: actioncreateuserpool-get
      parameters:
      - in: query
        name: AdminCreateUserConfig
        description: The configuration for AdminCreateUser requests
        type: string
      - in: query
        name: AliasAttributes
        description: Attributes supported as an alias for this user pool
        type: string
      - in: query
        name: AutoVerifiedAttributes
        description: The attributes to be auto-verified
        type: string
      - in: query
        name: DeviceConfiguration
        description: The device configuration
        type: string
      - in: query
        name: EmailConfiguration
        description: The email configuration
        type: string
      - in: query
        name: EmailVerificationMessage
        description: A string representing the email verification message
        type: string
      - in: query
        name: EmailVerificationSubject
        description: A string representing the email verification subject
        type: string
      - in: query
        name: LambdaConfig
        description: The Lambda trigger configuration information for the new user
          pool
        type: string
      - in: query
        name: MfaConfiguration
        description: Specifies MFA configuration details
        type: string
      - in: query
        name: Policies
        description: The policies associated with the new user pool
        type: string
      - in: query
        name: PoolName
        description: A string used to name the user pool
        type: string
      - in: query
        name: Schema
        description: An array of schema attributes for the new user pool
        type: string
      - in: query
        name: SmsAuthenticationMessage
        description: A string representing the SMS authentication message
        type: string
      - in: query
        name: SmsConfiguration
        description: The SMS configuration
        type: string
      - in: query
        name: SmsVerificationMessage
        description: A string representing the SMS verification message
        type: string
      - in: query
        name: UserPoolTags
        description: The cost allocation tags for the user pool
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
      - Pools
  /?Action=DeleteUserPool:
    get:
      summary: Delete User Pool
      description: Deletes the specified Amazon Cognito user pool.
      operationId: deleteUserPool
      x-api-path-slug: actiondeleteuserpool-get
      parameters:
      - in: query
        name: UserPoolId
        description: The user pool ID for the user pool you want to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
      - Pools
  /?Action=DeleteUserPoolClient:
    get:
      summary: Delete User Pool Client
      description: Allows the developer to delete the user pool client.
      operationId: deleteUserPoolClient
      x-api-path-slug: actiondeleteuserpoolclient-get
      parameters:
      - in: query
        name: ClientId
        description: The ID of the client associated with the user pool
        type: string
      - in: query
        name: UserPoolId
        description: The user pool ID for the user pool where you want to delete the
          client
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
      - Pools
  /?Action=DescribeUserPool:
    get:
      summary: Describe User Pool
      description: |-
        Returns the configuration information and metadata of the specified user
                    pool.
      operationId: describeUserPool
      x-api-path-slug: actiondescribeuserpool-get
      parameters:
      - in: query
        name: UserPoolId
        description: The user pool ID for the user pool you want to describe
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
      - Pools
  /?Action=GetDevice:
    get:
      summary: Get Device
      description: Gets the device.
      operationId: getDevice
      x-api-path-slug: actiongetdevice-get
      parameters:
      - in: query
        name: AccessToken
        description: The access token
        type: string
      - in: query
        name: DeviceKey
        description: The device key
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
      - Pools
  /?Action=ListUserPools:
    get:
      summary: List User Pools
      description: Lists the user pools associated with an AWS account.
      operationId: listUserPools
      x-api-path-slug: actionlistuserpools-get
      parameters:
      - in: query
        name: MaxResults
        description: The maximum number of results you want the request to return
          when listing the user            pools
        type: string
      - in: query
        name: NextToken
        description: An identifier that was returned from the previous call to this
          operation, which can            be used to return the next set of items
          in the list
        type: string
      responses:
        200:
          description: OK
      tags:
      - user Pools
  /?Action=UpdateUserPool:
    get:
      summary: Update User Pool
      description: Updates the specified user pool with the specified attributes.
      operationId: updateUserPool
      x-api-path-slug: actionupdateuserpool-get
      parameters:
      - in: query
        name: AdminCreateUserConfig
        description: The configuration for AdminCreateUser requests
        type: string
      - in: query
        name: AutoVerifiedAttributes
        description: The attributes that are automatically verified when the Amazon
          Cognito service            makes a request to update user pools
        type: string
      - in: query
        name: DeviceConfiguration
        description: Device configuration
        type: string
      - in: query
        name: EmailConfiguration
        description: Email configuration
        type: string
      - in: query
        name: EmailVerificationMessage
        description: The contents of the email verification message
        type: string
      - in: query
        name: EmailVerificationSubject
        description: The subject of the email verification message
        type: string
      - in: query
        name: LambdaConfig
        description: The AWS Lambda configuration information from the request to
          update the user            pool
        type: string
      - in: query
        name: MfaConfiguration
        description: 'Can be one of the following values:'
        type: string
      - in: query
        name: Policies
        description: A container with the policies you wish to update in a user pool
        type: string
      - in: query
        name: SmsAuthenticationMessage
        description: The contents of the SMS authentication message
        type: string
      - in: query
        name: SmsConfiguration
        description: SMS configuration
        type: string
      - in: query
        name: SmsVerificationMessage
        description: A container with information about the SMS verification message
        type: string
      - in: query
        name: UserPoolId
        description: The user pool ID for the user pool you want to update
        type: string
      - in: query
        name: UserPoolTags
        description: The cost allocation tags for the user pool
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
      - Pools
  /?Action=GetIdentityPoolConfiguration:
    get:
      summary: Get Identity Pool Configuration
      description: Gets the configuration settings of an identity pool.
      operationId: getIdentityPoolConfiguration
      x-api-path-slug: actiongetidentitypoolconfiguration-get
      parameters:
      - in: query
        name: IdentityPoolId
        description: A name-spaced GUID (for example, us-east-1:23EC4050-6AEA-7089-A2DD-08002EXAMPLE)
          created by Amazon Cognito
        type: string
      responses:
        200:
          description: OK
      tags:
      - Identity Pools
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