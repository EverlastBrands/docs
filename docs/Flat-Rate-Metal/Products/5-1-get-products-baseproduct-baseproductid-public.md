# Get Products By Base Product

Return all products that are linked to the base product with the **`ACTIVE`** status that is safe for the public to view.

| verb      | path                                         |
| --------- | -------------------------------------------- |
| **`GET`** | /products/base-product/:baseProductId/public |

| Param               | Description                    |
| ------------------- | ------------------------------ |
| **`baseProductId`** | Unique base product identifier |

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
