# Data Structures

## ReviewIncludeProduct
+ id: 1 (required, number) - Unique identifier
+ product_id: 2 (required, number)
+ title: Mantap (required) - Single line description
+ content: hangat di tubuh - Full description of the note which supports Markdown.
+ rating : 1 (required, number)
+ is_buyer: 0 (required, number)
+ product (ProductInclude)


## ReviewProduct (array)
+ (ReviewIncludeProduct)

# Group Reviews
show Reviews data

## Reviews [/api/v1/reviews]
### Get Reviews [GET]

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (ReviewList)

## Reviews Include Product [/api/v1/reviews?include=product]
### Get Reviews Include Products relation [GET]

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (ReviewProduct)

## Reviews single [/api/v1/reviews/id]
### Get single Review [GET]
Get a single of Review.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (ReviewList)
