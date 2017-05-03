
## ProductData
+ id: 1 (required, number) - Unique identifier
+ sku: 123 (required, number) - Unique identifier
+ name: Kuku bima Energi (required) - Single line description
+ description: minuman berenergi roso roso - Full description of the note which supports Markdown.
+ price: 12000 (required, number) - Unique identifier
+ sale_price: null
+ images (ImageList)

## ProductList (array)
+ (ProductData)

# Group Products
show products data

## Products [/api/v1/products]
### GET
Get all of products.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (ProductList)

## Product Single  [/api/v1/products/id]
### Get Single products [GET]
Get a single of products.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (ProductList)

## Products Filter [/api/v1/products?filter%5Bcategory%5D=1]
### filter products [GET]
Get a products filter by category.

+ Response 200 (application/json)

      + Headers

              X-Request-ID: f72fc914
              X-Response-Time: 4ms

      + Attributes (ProductData)

## Products Filter 2 parameters [/api/v1/products?filter%5Bcategory%5D=1&filter%5Bbrand%5D=1]
### filter 2 parameters [GET]
Get a products filter by category and brand.

+ Response 200 (application/json)

      + Headers

              X-Request-ID: f72fc914
              X-Response-Time: 4ms

      + Attributes (ProductData)
