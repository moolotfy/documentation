# Shop Microservice
Shop Microservice description.

## Version: 1.0.0

[Discover back end api](https://auctionsa.atlassian.net/wiki/spaces/BAC/pages/249266177/backend+API+links)
### /v1/shop

#### GET
##### Summary:

List Shops

##### Description:

List Shops

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header | language to return the data based on it | Yes | string |
| name | query | Offer Name | No | string |
| page | query | page number | No | integer |
| limit | query | limit to be returned | No | integer |
| nearest | query | get nearest shops by location | No | boolean |
| long | query | user location longitude | No | integer |
| lat | query | user location latitude | No | integer |
| category | query | filter shops by category ID | No | string |
| ids | query | ids of shops to be returned ex. 5f4e5f1bd75ccc754ffdcc02, 5f4e5f1bd75ccc754ffdcc02 | No | string |
| status | query | filter shops by status | No | string |
| hasOrders | query | filter shops by has orders | No | boolean |
| available | query |  | No | boolean |
| hasOffers | query | filter shops by has offers | No | boolean |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful operation |
| 400 | Bad Request |
| 404 | Not found |

#### POST
##### Summary:

Create Shop APi

##### Description:

Create Shop APi

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Create Shop APi | Yes | [Shop](#Shop) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful operation |
| 400 | Bad Request |
| 404 | Not found |

### /v1/shop/{id}

#### GET
##### Summary:

Get Shop By ID

##### Description:

Get Shop By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header | language to return the data based on it | Yes | string |
| id | path | shop Id | Yes | string |
| nearest | query | get nearest shops by location | No | boolean |
| long | query | user location longitude | No | integer |
| lat | query | user location latitude | No | integer |
| available | query |  | No | boolean |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

#### PATCH
##### Summary:

Update Shop By ID

##### Description:

Update Shop By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | shop Id | Yes | string |
| Body | body | Update Many Shops APi | Yes | [ShopPatch](#ShopPatch) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

#### DELETE
##### Summary:

Delete Shop

##### Description:

Delete Shop

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Shop ID | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

### /v1/shop/{id}/check-status

#### GET
##### Summary:

Check Shop Status By ID

##### Description:

Check Shop Status By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | shop Id | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

### /v1/branch

#### GET
##### Summary:

List Branchs

##### Description:

List Branchs

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header | language to return the data based on it | Yes | string |
| shopId | query | filter branches by Shop ID | No | string |
| name | query | search on branches by name | No | string |
| ids | query | ids of Branchs to be returned ex. 5f4e5f1bd75ccc754ffdcc02, 5f4e5f1bd75ccc754ffdcc02 | No | string |
| available | query |  | No | boolean |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful operation |
| 400 | Bad Request |
| 404 | Not found |

#### POST
##### Summary:

Create Branch APi

##### Description:

Create Branch APi

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Create Branch APi | Yes | [Branch](#Branch) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful operation |
| 400 | Bad Request |
| 404 | Not found |

### /v1/branch/{id}

#### GET
##### Summary:

Get Branch By ID

##### Description:

Get Branch By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header | language to return the data based on it | Yes | string |
| id | path | branch Id | Yes | string |
| available | query |  | No | boolean |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

#### PATCH
##### Summary:

Update Branch By ID

##### Description:

Update Branch By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | shop Id | Yes | string |
| Body | body | Update Many Branchs APi | Yes | [BranchPatch](#BranchPatch) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

#### DELETE
##### Summary:

Delete Branch

##### Description:

Delete Branch

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Branch ID | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

### /v1/category

#### GET
##### Summary:

List Categories

##### Description:

List Categories

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header | language to return the data based on it | Yes | string |
| name | query | Category Name | No | string |
| page | query | page number | No | integer |
| limit | query | limit to be returned | No | integer |
| type | query | filter categories by type (product | shop) | No | boolean |
| parent | query | filter categories by parent ID | No | string |
| ids | query | ids of Categories to be returned ex. 5f4e5f1bd75ccc754ffdcc02, 5f4e5f1bd75ccc754ffdcc02 | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful operation |
| 400 | Bad Request |
| 404 | Not found |

#### POST
##### Summary:

Create Category APi

##### Description:

Create Category APi

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Body | body | Create Category APi | Yes | [Category](#Category) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Successful operation |
| 400 | Bad Request |
| 404 | Not found |

### /v1/category/{id}

#### GET
##### Summary:

Get Category By ID

##### Description:

Get Category By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| local | header | language to return the data based on it | Yes | string |
| id | path | category Id | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

#### PATCH
##### Summary:

Update Category By ID

##### Description:

Update Category By ID

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Category Id | Yes | string |
| Body | body | Update Many Categories APi | Yes | [CategoryPatch](#CategoryPatch) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

#### DELETE
##### Summary:

Delete Category

##### Description:

Delete Category

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Category ID | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

### Models


#### Shop

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| nameEn | string |  | No |
| nameAr | string |  | No |
| descriptionEn | string |  | No |
| descriptionAr | string |  | No |
| status | string |  | No |
| category | string |  | No |
| classificationType | string |  | No |
| country | string |  | No |
| role | string |  | No |
| profitPercentage | integer |  | No |
| logo | string |  | No |
| cover | string |  | No |

#### ShopPatch

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| ingredients | [ string ] |  | No |
| nameEn | string |  | No |
| nameAr | string |  | No |
| descriptionEn | string |  | No |
| descriptionAr | string |  | No |
| status | string |  | No |
| category | string |  | No |

#### Branch

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| shopId | string |  | No |
| nameEn | string |  | No |
| nameAr | string |  | No |
| descriptionEn | string |  | No |
| descriptionAr | string |  | No |
| creationDate | string |  | No |
| status | string |  | No |
| location | object |  | No |
| workingHours | [ object ] |  | No |

#### BranchPatch

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| nameEn | string |  | No |
| nameAr | string |  | No |
| status | string |  | No |
| shopId | string |  | No |
| radius | integer |  | No |
| location | object |  | No |
| availability | string | Not Required if all | No |
| workingHours | [ object ] |  | No |

#### Category

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| nameEn | string |  | No |
| nameAr | string |  | No |
| descriptionEn | string |  | No |
| descriptionAr | string |  | No |
| type | string |  | No |
| parent | string |  | No |
| icon | string |  | No |

#### CategoryPatch

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| nameEn | string |  | No |
| nameAr | string |  | No |
| status | string |  | No |
| category | string |  | No |
