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
| Request body | body | add user object | Yes | [SignUp](#SignUp) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | successful operation | [ [SignUp](#SignUp) ] |
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
