# Authentication Microservice
Authentication Microservice description.

## Version: 1.0.0

### /v1/bid

#### GET
##### Description:

List Bids

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header |  | Yes | string |
| offerName | query | Offer Name | No | string |
| shopName | query | Shop Name | No | string |
| page | query | page number | No | integer |
| limit | query | limit to be returned | No | integer |
| all | query |  | No | boolean |
| status | query |  | No | string |
| userId | query |  | No | string |
| offerId | query |  | No | string |
| roundId | query |  | No | string |
| branchId | query |  | No | string |
| shopId | query |  | No | string |
| sortBy | query |  | No | string |
| ids | query |  | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |

#### PATCH
##### Description:

Update Many Bids APi

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |

#### POST
##### Description:

Create Bid APi

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |

### /v1/bid/{id}

#### GET
##### Description:

Get Bid By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header |  | Yes | string |
| id | path | bid Id | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |

#### PATCH
##### Description:

Create Bid APi

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Bid ID | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |

#### DELETE
##### Description:

Cancel Bid APi

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Bid ID | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |
