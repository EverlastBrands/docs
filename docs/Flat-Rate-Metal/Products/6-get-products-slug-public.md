---
sidebar_position: 6
---

# GET Product By Slug

Return product with the **`ACTIVE`** status that is safe for the public to view.

| verb      | path                        |
| --------- | --------------------------- |
| **`GET`** | /products/slug/:slug/public |

| Param      | Description                |
| ---------- | -------------------------- |
| **`slug`** | Unique product URL snippet |

## Example

**Response**

```json
{
  "data": {
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
  }
}
```
