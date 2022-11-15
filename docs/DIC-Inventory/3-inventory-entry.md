# Inventory Entry

Entity that stores product ID and location ID along with quantity.

## GET

### Get All Inventory Entries

| Method    | Path     |
| --------- | -------- |
| **`GET`** | /entries |

<details>
  <summary>Example Response</summary>

```json
{
  "data": {
    "entries": [
      {
        "id": number,
        "systemId": number,
        "quantity": number,
        "locationId": number
      },
      ...
    ]
  }
}
```

</details>

### Get By Search Term

| Method    | Path                 |
| --------- | -------------------- |
| **`GET`** | /entries/:searchTerm |

```json
{
  "data": {
    "entries": [
      {
        "id": number,
        "systemId": number,
        "quantity": number,
        "locationId": number
      },
      ...
    ]
  }
}
```

## POST

### Create Inventory Entry

| Method     | Path     |
| ---------- | -------- |
| **`POST`** | /entries |

<details>
<summary>Request Body<summary>

```json
{
  "itemCode": string,
  "quantity": number,
  "code": string
}
```

</details>

## PUT

## DELETE
