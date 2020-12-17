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
| local | header | language to return the data based on it | Yes | string |
| offerName | query | Offer Name | No | string |
| shopName | query | Shop Name | No | string |
| page | query | page number | No | integer |
| limit | query | limit to be returned | No | integer |
| all | query | return all bids | No | boolean |
| status | query | filter bids by status | No | string |
| userId | query | user id | No | string |
| offerId | query | filter bids by offer id | No | string |
| roundId | query | filter bids by round id | No | string |
| branchId | query | filter bids by branch id | No | string |
| shopId | query | filter bids by shop id | No | string |
| sortBy | query | sort records by date | No | string |
| ids | query | ids of bids to be returned ex. 5f4e5f1bd75ccc754ffdcc02, 5f4e5f1bd75ccc754ffdcc02 | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful operation |
| 400 | Bad Request |
| 404 | Not found |

#### PATCH
##### Summary:

Update Many Bids APi

##### Description:

Update Many Bids APi

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Update Many Bids APi | Yes | [BidsPatch](#BidsPatch) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful operation |
| 400 | Bad Request |
| 404 | Not found |

#### POST
##### Summary:

Create Bid APi

##### Description:

Create Bid APi

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Create Bid APi | Yes | [BidsPost](#BidsPost) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful operation |
| 400 | Bad Request |
| 404 | Not found |

### /v1/bid/{id}

#### GET
##### Summary:

Get Bid By ID

##### Description:

Get Bid By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header | language to return the data based on it | Yes | string |
| id | path | bid Id | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

#### PATCH
##### Summary:

Get Bid By ID

##### Description:

Get Bid By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | bid Id | Yes | string |
| Body | body | Update Many Bids APi | Yes | [BidPatch](#BidPatch) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

#### DELETE
##### Summary:

Cancel Bid APi

##### Description:

Cancel Bid APi

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | bid Id | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

### Models


#### BidsPatch

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| ids | [ string ] |  | No |
| data | object |  | No |

#### BidPatch

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| amount | integer |  | No |
| quantity | integer |  | No |

#### BidsPost

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| amount | integer |  | No |
| quantity | integer |  | No |
| offerId | string |  | No |
| branchId | string |  | No |
| userId | string |  | No |
