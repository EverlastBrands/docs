---
sidebar_position: 3
---

# GET Products

Return all products with the **`ACTIVE`** status that are safe for the public to view.

| verb      | path             |
| --------- | ---------------- |
| **`GET`** | /products/public |

## Example

**Response**

```json
{
  "data": {
    "products": [
      {
        "categoryId": "C4190ZLYpldcAg5uJwii",
        "id": "37nAdFB8QhQfdTMrlxKv",
        "unit": "Bundle",
        "customFields": [],
        "canCoilSell": false,
        "name": "Roof to wall",
        "price": 1500,
        "images": [],
        "material": "STEEL",
        "status": "ACTIVE",
        "quantityOnHand": 0,
        "description": "",
        "color": "DARK BROWN",
        "linkedProducts": [],
        "isSpecialOrder": false,
        "cost": 0,
        "pricing": [],
        "slug": "roof-to-wall"
      },
      {...}
    ]
  }
}
```
