# Authentication Microservice
Authentication Microservice description.

## Version: 1.0.0

[Discover back end api](https://auctionsa.atlassian.net/wiki/spaces/BAC/pages/249266177/backend+API+links)
### /v1/signup

#### POST
##### Summary:

Add a new user

##### Description:



##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | add user object | Yes | [SignUp](#SignUp) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | successful operation | [ [SignUp](#SignUp) ] |
| 400 | Invalid status value |  |

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


#### SignUp

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| password | string |  | No |
| firstName | string |  | No |
| lastName | string |  | No |
| phoneNumber | string |  | No |
| provider | string |  | No |
| email | string |  | No |
| userRole | string |  | No |

#### SendOTP

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| phoneNumber | string |  | No |
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
