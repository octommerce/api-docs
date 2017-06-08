# Data Structures

## UserIncludeOrders
+ id: 1 (required, number) - Unique identifier
+ name: Octommerce (required) - Single line description
+ username: octommerce (required) - Single line description
+ email: octommerce@octommerce.com - Full description of the note which supports Markdown.
+ last_login: 2017/04/25 17:46:32
+ address_count: 2 (required, number)
+ orders_count: 1 (required, number)
+ orders (OrderInclude)

## UserOrder (array)
+ (UserIncludeOrders)

## OrderInclude
+ data (OrderList)

## UserIncludeAddresses
+ id: 1 (required, number) - Unique identifier
+ name: Octommerce (required) - Single line description
+ username: octommerce (required) - Single line description
+ email: octommerce@octommerce.com - Full description of the note which supports Markdown.
+ last_login: 2017/04/25 17:46:32
+ avatar: null,
+ address_count: 2 (required, number)
+ orders_count: 1 (required, number)
+ addresses (AddressInclude)

## UserAddress (array)
+ (UserIncludeAddresses)

## AddressInclude
+ data (AddressList)

# Group Users

Group description
## User  [/api/v1/me]
get user

### Get user [GET]

you must fill header with acces Token

```http
Authorization: Bearer 5262d64b892e8d4341000001
```

+ Response 200 (aplication/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms


    + Attributes (UserList)

## User Include Orders [/api/v1/me?include=orders]
### Get user include orders relation [GET]

you must fill header with acces Token

```http
Authorization: Bearer 5262d64b892e8d4341000001
```

+ Response 200 (aplication/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms


    + Attributes (UserOrder)



### Update a User [PUT]

you must fill header with acces Token

```http
Authorization: Bearer 5262d64b892e8d4341000001
```
Update a single user by setting the username.
+ Request (application/json)

    + Headers

            Authorizaztion: 5262d64b892e8d4341000001
            Conten-Type: application/x-www-form-urlencoded

    + Body

            {
                "username": "octommerce update"
            }

+ Response 200 (application/json)


  + Body

            [
              {
                  "name": "octommerce update",
                  "image": "http://octommerce.com/octommerce.jpg",
                  "joined": "2013-11-02"
              },
            ]

+ Response 404 (application/json)

    + Body

            {
                "error": "Note not found"
            }


## User Include Address [/api/v1/me?include=addresses]
### Get user include Address relation [GET]

you must fill header with acces Token

```http
Authorization: Bearer 5262d64b892e8d4341000001
```

+ Response 200 (aplication/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms


    + Attributes (UserAddress)
