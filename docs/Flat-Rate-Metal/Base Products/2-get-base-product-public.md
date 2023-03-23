# GET Base Product By Id

Retrieves a base product by ID

| verb      | path                                 |
| --------- | ------------------------------------ |
| **`GET`** | /base-products/:baseProductId/public |

| Param               | Description                        |
| ------------------- | ---------------------------------- |
| **`baseProductId`** | Unique Identifier for base product |

## Example

**Response**

```json
{
  "data": {
    "order": 0,
    "categoryId": "mmXLzSSMRjDNiibXeh3t",
    "name": "Drip Edge",
    "description": "",
    "id": "HBaR6rEAayR89lXJ11iY",
    "childProducts": ["7nwqNO2oIr9LyMGX5y9n", "M07IXoWR0prJ07kBmEhy"]
  }
}
```
