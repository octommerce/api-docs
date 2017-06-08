# Data Structures

## CategoryIncludeProducts
+ id: 1 (required, number) - Unique identifier
+ slug: Minuman
+ name: Minuman (required) - Single line description
+ description: minuman berenergi roso roso - Full description of the note which supports Markdown.
+ images (ImageList)
+ color: null
+ keywords: roso roso
+ products (ProductInclude)


## CategoryProduct (array)
+ (CategoryIncludeProducts)

# Group Categories
show categories data

## Categories [/api/v1/categories]
### Get Categories [GET]

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (CategoryList)

## Categories Include Products [/api/v1/categories?include=products]
### Get Categories Include Products relation [GET]

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (CategoryProduct)

## Categories single [/api/v1/categories/id]
### Get single category [GET]
Get a single of Categories.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (CategoryList)
