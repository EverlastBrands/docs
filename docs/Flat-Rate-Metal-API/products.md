# Products

## GET

### Get All Products

| Method    | Path      | Cache Behavior | User Role |
| --------- | --------- | -------------- | --------- |
| **`GET`** | /products | Pull           | Admin     |

```JSON

```

### Get All Products Public

| Method    | Path             | Cache Behavior | User Role |
| --------- | ---------------- | -------------- | --------- |
| **`GET`** | /products/public | Pull           | All       |

### Get Product ny ID Public

| Method    | Path                        | Cache Behavior | User Role |
| --------- | --------------------------- | -------------- | --------- |
| **`GET`** | /products/:productId/public | Pull           | All       |

### Get Category by ID Public

| Method    | Path                                  | Cache Behavior | User Role |
| --------- | ------------------------------------- | -------------- | --------- |
| **`GET`** | /products/category/:categoryId/public | Pull           | All       |

### Get Product by Product Slug

| Method    | Path                        | Cache Behavior | User Role |
| --------- | --------------------------- | -------------- | --------- |
| **`GET`** | /products/slug/:slug/public | Pull           | All       |

### Get Base Products by ID

| Method    | Path                                         | Cache Behavior | User Role |
| --------- | -------------------------------------------- | -------------- | --------- |
| **`GET`** | /products/base-product/:baseProductId/public | Pull           | All       |

## POST

### Create New Product

| Method     | Path      | Cache Behavior | User Role |
| ---------- | --------- | -------------- | --------- |
| **`POST`** | /products | Push           | Admin     |

### Update Cart Products

| Method     | Path                    | Cache Behavior | User Role |
| ---------- | ----------------------- | -------------- | --------- |
| **`POST`** | /products/cart-products | Push           | User      |

### Batch Product Creation

:::info Needs Refactoring
:::

| Method     | Path                        | Cache Behavior | User Role |
| ---------- | --------------------------- | -------------- | --------- |
| **`POST`** | /products/batch-file-create | Push           | Admin     |

### Batch Product Delete

| Method     | Path                   | Cache Behavior | User Role |
| ---------- | ---------------------- | -------------- | --------- |
| **`POST`** | /products/batch-delete | Push & Pull    | Admin     |

## PUT

### Bulk Product Update

| Method    | Path           | Cache Behavior | User Role |
| --------- | -------------- | -------------- | --------- |
| **`PUT`** | /products/bulk | Push & Pull    | Admin     |

### Batch Product Update

| Method    | Path                        | Cache Behavior | User Role |
| --------- | --------------------------- | -------------- | --------- |
| **`PUT`** | /products/batch-file-update | Push & Pull    | Admin     |

### Update Product by ID

| Method    | Path                 | Cache Behavior | User Role |
| --------- | -------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId | Push & Pull    | Admin     |

### Update Sale Units by Product ID

| Method    | Path                           | Cache Behavior | User Role |
| --------- | ------------------------------ | -------------- | --------- |
| **`PUT`** | /products/:productId/sale-unit | Push & Pull    | Admin     |

### Toggle Coil Sell

| Method    | Path                                  | Cache Behavior | User Role |
| --------- | ------------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/toggle-coil-sell | Push & Pull    | Admin     |

### Toggle Special Order

| Method    | Path                                      | Cache Behavior | User Role |
| --------- | ----------------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/toggle-special-order | Push & Pull    | Admin     |

### Toggle Hide

| Method    | Path                             | Cache Behavior | User Role |
| --------- | -------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/toggle-hide | Push & Pull    | Admin     |

### Toggle Hide Price

| Method    | Path                                   | Cache Behavior | User Role |
| --------- | -------------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/toggle-hide-price | Push & Pull    | Admin     |

### Toggle Out of Stock

| Method    | Path                                     | Cache Behavior | User Role |
| --------- | ---------------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/toggle-out-of-stock | Push & Pull    | Admin     |

### Toggle Phone Order Only

| Method    | Path                                         | Cache Behavior | User Role |
| --------- | -------------------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/toggle-phone-order-only | Push & Pull    | Admin     |

### Toggle On Sale

| Method    | Path                                | Cache Behavior | User Role |
| --------- | ----------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/toggle-on-sale | Push & Pull    | Admin     |

### Link Products

| Method    | Path                      | Cache Behavior | User Role |
| --------- | ------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/link | Push & Pull    | Admin     |

### Update Product Pricing

| Method    | Path                                | Cache Behavior | User Role |
| --------- | ----------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/update-pricing | Pull           | Admin     |

### Update Product Images

| Method    | Path                        | Cache Behavior | User Role |
| --------- | --------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/images | Push & Pull    | Admin     |

### Unlink Products

| Method    | Path                                           | Cache Behavior | User Role |
| --------- | ---------------------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/unlink/:unlinkedProductId | Push & Pull    | Admin     |

### Update Product Status

| Method    | Path                                | Cache Behavior | User Role |
| --------- | ----------------------------------- | -------------- | --------- |
| **`PUT`** | /products/:productId/status/:status | Push & Pull    | Admin     |

## DELETE

### Delete a Product

| Method       | Path                 | Cache Behavior | User Role |
| ------------ | -------------------- | -------------- | --------- |
| **`DELETE`** | /products/:productId | Push & Pull    | Admin     |

### Remove a Product Sale Unit

| Method       | Path                                       | Cache Behavior | User Role |
| ------------ | ------------------------------------------ | -------------- | --------- |
| **`DELETE`** | /products/:productId/sale-unit/:saleUnitId | Push & Pull    | Admin     |

### Remove Product Image

| Method       | Path                                | Cache Behavior | User Role |
| ------------ | ----------------------------------- | -------------- | --------- |
| **`DELETE`** | /products/:productId/image/:imageId | Push & Pull    | Admin     |
