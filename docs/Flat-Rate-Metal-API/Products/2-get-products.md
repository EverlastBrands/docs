---
sidebar_position: 2
---

# GET Products Admin

Return all products regardless of status.

| verb      | path      |
| --------- | --------- |
| **`GET`** | /products |

## Examples

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
        "isPhoneOrderOnly": false,
        "isOutOfStock": false,
        "hidePrice": false,
        "cost": 0,
        "pricing": [],
        "slug": "roof-to-wall",
        "baseProductId": "adkjfasdkjfals"
      },
      {...}
    ]
  }
}
```
