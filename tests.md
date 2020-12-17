# Bidding Microservice
Bidding Microservice description.

## Version: 1.0.0

[Discover back end api](https://auctionsa.atlassian.net/wiki/spaces/BAC/pages/249266177/backend+API+links)
### /v1/bid

#### GET
##### Summary:

List Bids

##### Description:

List Bids

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header | an authorization header | Yes | string |
| offerName | query | Offer Name | Yes | string |
| shopName | query | Shop Name | Yes | string |
| page | query | page number | Yes | integer |
| limit | query | limit to be returned | Yes | integer |
| all | query | return all bids | Yes | boolean |
| status | query | filter bids by status | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

### /v1/sendotp

#### POST
##### Summary:

Send otp

##### Description:



##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Send OTP | Yes | [SendOTP](#SendOTP) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | successful operation | [ [SendOTP](#SendOTP) ] |
| 400 | Invalid status value |  |

### /v1/forgetpassword

#### GET
##### Summary:

forget password

##### Description:



##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| phoneNumber | query |  | Yes | string |
| email | query |  | Yes | string (email) |
| provider | query |  | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

#### POST
##### Summary:

Send otp

##### Description:



##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Send OTP | Yes | [ForgetPassword](#ForgetPassword) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | successful operation | [ [ForgetPassword](#ForgetPassword) ] |
| 400 | Invalid status value |  |

### /v1/getToken

#### POST
##### Summary:

Get token

##### Description:



##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Send OTP | Yes | [GetToken](#GetToken) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | successful operation | [ [GetToken](#GetToken) ] |
| 400 | Invalid status value |  |

### /v1/ConfirmEmail

#### POST
##### Summary:

Get token

##### Description:



##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Send OTP | Yes | [ConfirmEmail](#ConfirmEmail) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | successful operation | [ [ConfirmEmail](#ConfirmEmail) ] |
| 400 | Invalid status value |  |

### /v1/ConfirmPhoneNumber

#### POST
##### Summary:

Get token

##### Description:



##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Send OTP | Yes | [ConfirmPhoneNumber](#ConfirmPhoneNumber) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | successful operation | [ [ConfirmPhoneNumber](#ConfirmPhoneNumber) ] |
| 400 | Invalid status value |  |

### Models


#### bids

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| local | [ string ] |  | No |

#### SendOTP

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| phoneNumber | integer |  | No |
| email | string |  | No |
| provider | string |  | No |

#### ForgetPassword

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| phoneNumber | string |  | No |
| email | string |  | No |
| provider | string |  | No |

#### GetToken

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| password | string |  | No |
| provider | string |  | No |
| username | string |  | No |
| clientId | string |  | No |
| clientSecret | string |  | No |
| grantType | string |  | No |

#### ConfirmEmail

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| verificationCode | string |  | No |
| email | string |  | No |
| provider | string |  | No |

#### ConfirmPhoneNumber

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| verificationCode | string |  | No |
| phoneNumber | string |  | No |
| provider | string |  | No |
