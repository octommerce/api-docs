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


    + Body

            [
                {
                    "name": "octommerce",
                    "image": "http://octommerce.com/octommerce.jpg",
                    "joined": "2013-11-01"
                },
            ]

    + Schema

            <!-- include(example-schema.json) -->

### Update a User [PUT]
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
