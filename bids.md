swagger: "2.0"
info:
  description: "Bidding Microservice description."
  version: "1.0.0"
  title: "Bidding Microservice"
tags:
- name: "Bidding"
paths:
    /v1/bid:
      get:
        tags:
          - Bid
        description: List Bids
        parameters:
            - in: header
              name: local
              required: true
              schema:
                type: string
                description: language to return the data based on it
                enum: [ar-SA, en-US, Multi]
            - in: query
              name: offerName
              required: false
              schema:
                type: string
              description: Offer Name
            - in: query
              name: shopName
              required: false
              schema:
                type: string
              description: Shop Name
            - in: query
              name: page
              required: false
              schema:
                type: integer
              description: page number
            - in: query
              name: limit
              required: false
              schema:
                type: integer
              description: limit to be returned
            - in: query
              name: all
              required: false
              schema:
                type: boolean
                description: return all bids
                enum: [true]
            - in: query
              name: status
              required: false
              schema:
                type: string
                description: filter bids by status
                enum: ['PendingResult', 'WaitingOrder', 'PendingResult, WaitingOrder', 'Canceled, Expired, Lost']
            - in: query
              name: userId
              required: false
              schema:
                type: string
                description: user id
            - in: query
              name: offerId
              required: false
              schema:
                type: string
                description: filter bids by offer id
            - in: query
              name: roundId
              required: false
              schema:
                type: string
                description: filter bids by round id
            - in: query
              name: branchId
              required: false
              schema:
                type: string
                description: filter bids by branch id
            - in: query
              name: shopId
              required: false
              schema:
                type: string
                description: filter bids by shop id
            - in: query
              name: sortBy
              required: false
              schema:
                type: string
                description: sort records by date
                enum: [asc, desc]
            - in: query
              name: ids
              required: false
              schema:
                type: string
                description: ids of bids to be returned ex. 5f4e5f1bd75ccc754ffdcc02, 5f4e5f1bd75ccc754ffdcc02
        responses:
          '200':
            description: Auto generated using Swagger Inspector
            content:
              application/json; charset=utf-8:
                schema:
                  type: string
                examples:
                  'list normal shops':
                    value: |-
                      {
                        "data": [
                            {
                              "_id": "5f6cedaaa4ab557befedac30",
                              "status": "WaitingOrder",
                              "amount": 20,
                              "quantity": 10,
                              "userId": "5f69b00c722063000d9cc85f",
                              "offerId": "5f672b4e2387d094a4843cad",
                              "branchId": "5f4e3a50d443e9d95f3aca54",
                              "totalAmount": 200,
                              "round": {
                                "_id": "5f8455d079dd4c8c35ccd246",
                                "roundNumber": 0,
                                "startDate": "2020-10-11T15:14:06.000Z",
                                "endDate": "2020-10-13T15:16:36.000Z",
                                "roundDuration": 3,
                                "remainingTime": 10000
                              },
                              "createdAt": "2020-09-24T19:04:10.528Z",
                              "updatedAt": "2020-09-24T19:04:10.528Z",
                              "remainingTime": 10000,
                              "__v": 0
                            }
                        ],
                        "page": 1,
                        "limit": 10,
                        "prevPage": 0,
                        "nextPage": 2,
                        "total": 5,
                        "pages": 1
                      }
      patch:
        tags:
          - Bid
        description: Update Many Bids APi
        requestBody:
          content:
            application/json:
              schema:
                type: object
                properties:
                  ids:
                    type: array
                  quantity:
                    type: number
              examples:
                '0':
                  value: |-
                    {
                      "ids": ["5f6cedaaa4ab557befedac30"],
                      "data": {"status": "WaitingOrder"}
                    }
                'description':
                  value: |-
                    {
                      "ids": ["5f6cedaaa4ab557befedac30"],
                      "data": {"status": "WaitingOrder"}
                    }
        responses:
          '200':
            description: Auto generated using Swagger Inspector
            content:
              application/json; charset=utf-8:
                schema:
                  type: string
                examples:
                  'Success Response':
                    value: |-
                      {
                        "id": "5f37e8d545380f35802f7369"
                      }
                  'Validations Error Response':
                    value: |-
                      {
                        "errors": [
                            {
                                "message": "invalid Params",
                                "type": "validation Error",
                                "code": 400,
                                "trace_id": "190e4bd9-f09e-41de-a473-d91779a54c5a",
                                "params": [
                                    {
                                        "param_name": "amount",
                                        "description": "required field",
                                        "code": 401
                                    }
                                ]
                            }
                        ]
                      }        
      post:
        tags:
          - Bid
        description: Create Bid APi
        requestBody:
          content:
            application/json:
              schema:
                type: object
                properties:
                  amount:
                    type: number
                  quantity:
                    type: number
                  offerId:
                    type: string
                  userId:
                    type: string
                  branchId:
                    type: string
              examples:
                '0':
                  value: |-
                    {
                      "amount": 20,
                      "quantity": 10,
                      "userId": "5f69b00c722063000d9cc85f",
                      "offerId": "5f672b4e2387d094a4843cad",
                      "branchId": "5f4e3a50d443e9d95f3aca54"
                    }
                'description':
                  value: |-
                    {
                      "amount": "selected user of bewtween ( min( minimum offer price) 10 and max( orginal price)  10 )",
                      "quantity": 10,
                      "userId": "the user who add new bid ",
                      "offerId": " selected offer id ",
                      "branchId": "selected branch id from offer "
                    }
        responses:
          '200':
            description: Auto generated using Swagger Inspector
            content:
              application/json; charset=utf-8:
                schema:
                  type: string
                examples:
                  'Success Response':
                    value: |-
                      {
                        "id": "5f37e8d545380f35802f7369"
                      }
                  'Validations Error Response':
                    value: |-
                      {
                        "errors": [
                            {
                                "message": "invalid Params",
                                "type": "validation Error",
                                "code": 400,
                                "trace_id": "190e4bd9-f09e-41de-a473-d91779a54c5a",
                                "params": [
                                    {
                                        "param_name": "amount",
                                        "description": "required field",
                                        "code": 401
                                    }
                                ]
                            }
                        ]
                      }
    /v1/bid/{id}:
      get:
        tags:
          - Bid
        description: Get Bid By ID
        parameters:
            - in: header
              name: local
              required: true
              schema:
                type: string
                description: language to return the data based on it
                enum: [ar-SA, en-US, Multi]
            - in: path
              name: id
              required: true
              schema:
                type: string
              description: bid Id
        responses:
          '200':
            description: Auto generated using Swagger Inspector
            content:
              application/json; charset=utf-8:
                schema:
                  type: string
                examples:
                  '0':
                    value: |-
                      {
                        "_id": "5f6cedaaa4ab557befedac30",
                        "status": "WaitingOrder",
                        "amount": 20,
                        "quantity": 10,
                        "userId": "5f69b00c722063000d9cc85f",
                        "offerId": "5f672b4e2387d094a4843cad",
                        "branchId": "5f4e3a50d443e9d95f3aca54",
                        "round": {
                          "_id": "5f8455d079dd4c8c35ccd246",
                          "roundNumber": 0,
                          "startDate": "2020-10-11T15:14:06.000Z",
                          "endDate": "2020-10-13T15:16:36.000Z",
                          "roundDuration": 3,
                          "remainingTime": 10000
                        },
                        "totalAmount": 200,
                        "createdAt": "2020-09-24T19:04:10.528Z",
                        "updatedAt": "2020-09-24T19:04:10.528Z",
                        "remainingTime": 10000,
                        "__v": 0
                      }
      patch:
        tags:
          - Bid
        description: Create Bid APi
        parameters:
            - in: path
              name: id
              required: true
              schema:
                type: string
              description: Bid ID
        requestBody:
          content:
            application/json:
              schema:
                type: object
                properties:
                  amount:
                    type: number
                  quantity:
                    type: number
              examples:
                '0':
                  value: |-
                    {
                      "amount": 20,
                      "quantity": 10
                    }
                'description':
                  value: |-
                    {
                      "amount": "selected user of bewtween ( min( minimum offer price) 10 and max( orginal price)  10 )",
                      "quantity": 'selected quantity',
                    }
        responses:
          '200':
            description: Auto generated using Swagger Inspector
            content:
              application/json; charset=utf-8:
                schema:
                  type: string
                examples:
                  'Success Response':
                    value: |-
                      {
                        "id": "5f37e8d545380f35802f7369"
                      }
                  'Validations Error Response':
                    value: |-
                      {
                        "errors": [
                            {
                                "message": "invalid Params",
                                "type": "validation Error",
                                "code": 400,
                                "trace_id": "190e4bd9-f09e-41de-a473-d91779a54c5a",
                                "params": [
                                    {
                                        "param_name": "amount",
                                        "description": "required field",
                                        "code": 401
                                    }
                                ]
                            }
                        ]
                      }
      delete:
        tags:
          - Bid
        description: Cancel Bid APi
        parameters:
            - in: path
              name: id
              required: true
              schema:
                type: string
              description: Bid ID
        responses:
          '200':
            description: Auto generated using Swagger Inspector
            content:
              application/json; charset=utf-8:
                schema:
                  type: string
                examples:
