# Data Structures
## Products
+ id: 1 (required, number) - Unique identifier
+ sku: 123 (required, number) - Unique identifier
+ name: Kuku bima Energ i (required) - Single line description
+ description: minuman berenergi roso roso - Full description of the note which supports Markdown.
+ price: 12000 (required, number) - Unique identifier
+ sale_price: null
+ images (ImageList)

## ProductLists (array)
+ (Products)

## ArrayProduct
+ data (ProductLists)

## CartData
+ id: 1 (required, number),
+ user_id: 2 (required, number),
+ total_price: 12000 (required, number),
+ created_at: 2017/05/02 21:24:37,
+ products (ArrayProduct)

## CartList (array)
+ (CartData)

# Group Cart
Group description
## Cart  [/api/v1/cart]
get Cart

### Get cart [GET]

you must fill header with acces Token

```http
Authorization: Bearer 5262d64b892e8d4341000001
```

+ Response 200 (aplication/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms


    + Attributes (CartList)

    + Schema

            <!-- include(example-schema.json) -->

### Add Cart [POST]
Add products to cart using id and quantity.

you must fill header with acces Token

```http
Authorization: Bearer 5262d64b892e8d4341000001
```
example to add cart with form:

key | value
---- | -----------
products[0][id]  | 1
products[0][qty]  | 1



you can add cart with json:
```http
{
  "products": [
    {
      "id": 2,
      "qty": 3
    }
  ]
}
```


+ Response 200 (aplication/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms


    + Attributes (CartList)

### Update Cart [PUT]
Update product on cart using id and quantity.

you must fill header with acces Token

```http
Authorization: Bearer 5262d64b892e8d4341000001
```
example to Update cart:

key | value
---- | -----------
products[0][id]  | 1
products[0][qty]  | 1

you can update cart with json:
```http
{
  "products": [
    {
      "id": 2,
      "qty": 3
    }
  ]
}
```

+ Response 200 (aplication/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms


    + Attributes (CartList)

### Delete Cart [DELETE]
Delete product on cart using id and quantity.

you must fill header with acces Token

```http
Authorization: Bearer 5262d64b892e8d4341000001
```
example to Delete cart:

key | value
---- | -----------
products[0][id]  | 2

+ Response 200 (aplication/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms


    + Attributes (CartList)
