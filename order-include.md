# Data Structures

## updateData
+ date: 2017/05/04 11:16:39.000000
+ timezone_type: 3
+ timezone: Asia/Jakarta

## invoiceData
+ id: 34 (required, number) - Unique identifier
+ user_id: 2 (required, number) - Unique identifier
+ subtotal: 24000 (required, number) - Unique identifier
+ tax: 1 (required, number) - Unique identifier
+ total: 1 (required, number) - Unique identifier
+ has: 69d7f90ba754125a789cff97af6c1110
+ status_code: null
+ status_update_at (updateData)

## invoiceList (array)
+ (invoiceData)

# Group Orders
show orders data

## Orders [/api/v1/orders]
### Get Orders [GET]

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (OrderList)

### Add Order [POST]
Add order products.

you must fill header with acces Token

```http
Authorization: Bearer 5262d64b892e8d4341000001
```

example to add orders with form:

key | value
---- | -----------
shipping_name  | octommerce
shipping_phone  | 085813488273
shipping_address | street apron no 43
shipping_city-id | 1
shipping_state_id | 2



+ Response 200 (aplication/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Body

            "data": {
              "id": 70,
              "user_id": 14,
              "order_no": "GBWJ3V1PE",
              "name": "Octommerce",
              "email": "octommerce@octommerce.com",
              "phone": 085813488273,
              "message": "null",
              "subtotal": 200000,
              "discount": 0,
              "tax": 0,
              "misc_fee": 0,
              "total": 200000,
              "is_same_address": "false",
              "shipping_name": "octommerce",
              "shipping_phone": 085813488273,
              "shipping_company": "Octommerce",
              "shipping_address": "street apron no 43",
              "shipping_postcode": 123123,
              "status_code": "waiting",
              "status": {
                "name": "waiting",
                "color": "#f39c12",
                "description": "waiting customer to pay. ",
                }
              "status_update_at": 2017/05/15 13:41:44
              "create_at": 2017/05/15 13:41:44
              "invoice": {
                "data": {
                  "id": 51,
                  "user_id": 14,
                  "subtotal": 211,
                  "discount": 0,
                  "tax": 0,
                  "total": 211,
                  "hash": "9db47f74852a7b7156f91796fd844b3e",
                  "status_code": null,
                  "status_updated_at": "2017-05-15 13:41:44",
                  "created_at": "2017-05-15 13:41:44"
                }
              }
            }



## Order single [/api/v1/orders/id]
### Get single Order [GET]
Get a single of Order.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (OrderList)

### Update Order [PUT]
update orders.

example to update orders with form:

key | value
---- | -----------
shipping_name  | octommerce
shipping_phone  | 085813488273
shipping_address | street apron no 44
shipping_city-id | 1
shipping_state_id | 2

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Body

            "data": {
              "id": 70,
              "user_id": 14,
              "order_no": "GBWJ3V1PE",
              "name": "Octommerce",
              "email": "octommerce@octommerce.com",
              "phone": 085813488273,
              "message": "null",
              "subtotal": 200000,
              "discount": 0,
              "tax": 0,
              "misc_fee": 0,
              "total": 200000,
              "is_same_address": "false",
              "shipping_name": "octommerce",
              "shipping_phone": 085813488273,
              "shipping_company": "Octommerce",
              "shipping_address": "street apron no 44",
              "shipping_postcode": 123123,
              "status_code": "waiting",
              "status": {
                "name": "waiting",
                "color": "#f39c12",
                "description": "waiting customer to pay. ",
                }
              "status_update_at": 2017/05/15 13:41:44
              "create_at": 2017/05/15 13:41:44
                "invoice": {
                  "data": {
                  "id": 51,
                  "user_id": 14,
                  "subtotal": 211,
                  "discount": 0,
                  "tax": 0,
                  "total": 211,
                  "hash": "9db47f74852a7b7156f91796fd844b3e",
                  "status_code": null,
                  "status_updated_at": "2017-05-15 13:41:44",
                  "created_at": "2017-05-15 13:41:44"
                    }
                }
              }
