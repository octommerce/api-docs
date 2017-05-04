# Data Structures
## OrderData
+ id: 1 (required, number) - Unique identifier
+ user_id: 2 (required, number) - Unique identifier
+ order_no: F4C5JLDHT
+ name: Octommerce (required) - Single line description
+ email: octommerce@octommerce.com
+ phone: 08887758271
+ message: null
+ subtotal: 24000 (required, number) - Unique identifier
+ discount:  0 (required, number) - Unique identifier
+ tax:  0 (required, number) - Unique identifier
+ misc_fee:  0 (required, number) - Unique identifier
+ total:  24000 (required, number) - Unique identifier
+ status_code: waiting
+ status_update_at(updateData)
+ create_at: 2017/05/04 11:16:39
+ invoices (invoiceList)
+ update_at: 2017/05/04 11:16:39

## OrderList (array)
+ (OrderData)

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

+ Response 200 (aplication/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms


    + Attributes (CartList)
## Order single [/api/v1/orders/id]
### Get single Order [GET]
Get a single of Order.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (OrderList)
