
## ProductIncludeCategories
+ id: 1 (required, number) - Unique identifier
+ sku: 123 (required, number) - Unique identifier
+ name: Kuku bima Energi (required) - Single line description
+ description: minuman berenergi roso roso - Full description of the note which supports Markdown.
+ price: 12000 (required, number) - Unique identifier
+ sale_price: null
+ images (ImageList)
+ categories (CategoryInclude)

## CategoryInclude 
+ data (CategoryList)

## ProductCategory (array)
+ (ProductIncludeCategories)

## ProductIncludeReviews
+ id: 1 (required, number) - Unique identifier
+ sku: 123 (required, number) - Unique identifier
+ name: Kuku bima Energi (required) - Single line description
+ description: minuman berenergi roso roso - Full description of the note which supports Markdown.
+ price: 12000 (required, number) - Unique identifier
+ sale_price: null
+ images (ImageList)
+ reviews (ReviewInclude)

## ReviewInclude 
+ data (ReviewList)

## ProductReview (array)
+ (ProductIncludeReviews)

## ProductIncludeBrand
+ id: 1 (required, number) - Unique identifier
+ sku: 123 (required, number) - Unique identifier
+ name: Kuku bima Energi (required) - Single line description
+ description: minuman berenergi roso roso - Full description of the note which supports Markdown.
+ price: 12000 (required, number) - Unique identifier
+ sale_price: null
+ images (ImageList)
+ Brand (BrandInclude)

## BrandInclude 
+ data (BrandList)

## ProductBrand (array)
+ (ProductIncludeBrand)

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

## Products include categories [/api/v1/products?include=categories]
### GET
Get all of products include with categories relation.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (ProductCategory)

## Products include reviews [/api/v1/products?include=reviews]
### GET
Get all of products include with reviews relation.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (ProductReview)

## Product include brand [/api/v1/products/1?include=brand]
### GET
Get single product include with brand relation.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (ProductBrand)

## Product Single  [/api/v1/products/id]
### Get Single products [GET]
Get a single of products.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (ProductList)

## Products Filter category [/api/v1/products?filter%5Bcategory%5D=1]
### filter products cateogy [GET]
Get a products filter by category.

+ Response 200 (application/json)

      + Headers

              X-Request-ID: f72fc914
              X-Response-Time: 4ms

      + Attributes (ProductList)

## Products Filter lists [/api/v1/products?filter%5Blists%5D=1]
### filter products list [GET]
Get a products filter by lists.

+ Response 200 (application/json)

      + Headers

              X-Request-ID: f72fc914
              X-Response-Time: 4ms

      + Attributes (ProductList)

## Products Filter search [/api/v1/products?filter%5Bsearch%5D=bima]
### filter products search [GET]
Get a products filter by search.

+ Response 200 (application/json)

      + Headers

              X-Request-ID: f72fc914
              X-Response-Time: 4ms

      + Attributes (ProductList)

## Products Filter stock [/api/v1/products?filter%5Boutsock%5D=true]
### filter products stock [GET]
Get if value of parameter outstock is true, then it show just stock product is true.

+ Response 200 (application/json)

      + Headers

              X-Request-ID: f72fc914
              X-Response-Time: 4ms

      + Attributes (ProductList)

## Products Filter 2 parameters [/api/v1/products?filter%5Bcategory%5D=1&filter%5Bbrand%5D=1]
### filter 2 parameters [GET]
Get a products filter by category and brand.

+ Response 200 (application/json)

      + Headers

              X-Request-ID: f72fc914
              X-Response-Time: 4ms

      + Attributes (ProductData)

## Products sort order [/api/v1/products?sort=name+desc]
### show products by sort order [GET]
show product by sort order, it can sort by:
name, created_at, price, random, reordered and sales

+ Response 200 (application/json)

      + Headers

              X-Request-ID: f72fc914
              X-Response-Time: 4ms

      + Attributes (ProductList)