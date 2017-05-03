# Data Structures
## BrandData
+ id: 1 (required, number) - Unique identifier
+ slug: Sidomuncul
+ name: Sidomuncul (required) - Single line description
+ description: minuman berenergi roso roso - Full description of the note which supports Markdown.
+ images (ImageList)
+ keywords: roso roso

## BrandList (array)
+ (BrandData)

# Group Brands
show Brands data

## Brands [/api/v1/brands]
### Get Brands [GET]

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (BrandList)
## Brands single [/api/v1/brands/id]
### Get single Brands [GET]
Get a single of Brand.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (BrandList)
