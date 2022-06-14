---
sidebar_position: 7
---

# POST Products

Create a new product.

| verb       | path      |
| ---------- | --------- |
| **`POST`** | /products |

| Body                 | Type      | Description                                                      | Required |
| -------------------- | --------- | ---------------------------------------------------------------- | -------- |
| **`name`**           | `string`  | Unique product name potentially containing the material or color | true     |
| **`price`**          | `int`     | Positive whole number (USD in pennies)                           | true     |
| **`unit`**           | `enum`    | `SINGLE` `BOX` `BUNDLE` `CARTON` `ft` `PAIR` `COIL` `PIECE`      | true     |
| **`categoryId`**     | `string`  | Unique category identifier                                       | false    |
| **`description`**    | `string`  | Product content description                                      | false    |
| **`cost`**           | `int`     | Positive whole number (USD in pennies)                           | false    |
| **`isSpecialOrder`** | `boolean` | Marks the product as special order only                          | false    |
| **`slug`**           | `string`  | Unique product URL snippet                                       | false    |

## Example

**Response**

```json
{
  "data": {
    "productId": "37nAdFB8QhQfdTMrlxKv"
  }
}
```
