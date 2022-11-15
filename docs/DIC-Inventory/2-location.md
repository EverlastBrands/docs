# Location

Entity that stores bay, section, and row information. Locations store inventory entries.

## GET

### Get All Locations

| Method    | Path       |
| --------- | ---------- |
| **`GET`** | /locations |

### Example

Request
`http://localhost:4444/locations`

<details>
  <summary>Example Response</summary>

```json
{
  "data": {
    "locations": [
      {
        "id": number,
        "section": string,
        "bay": number,
        "startingSlot": number,
        "endingSlot": number,
        "code": string,
        "inventoryEntries": [
          {
            "systemId": number,
            "quantity": number,
            "locationId": number
          },
          ...
        ]
      },
      ...
    ]
  }
}
```

</details>

### Get Location By Code

| Method    | Path             |
| --------- | ---------------- |
| **`GET`** | /locations/:code |

### Example

Request
`http://localhost:4444/locations/:code`

<details>
<summary>Example Response</summary>

```json
{
  "data": {
    "location": {
      "id": number,
      "section": string,
      "bay": number,
      "startingSlot": number,
      "endingSlot": number,
      "code": string,
      "inventoryEntries": [
        {
          "systemId": number,
          "quantity": number,
          "locationId": number
        },
        ...
      ]
    },
  }
}
```

</details>

## POST

## Create Location

| Method     | Path       |
| ---------- | ---------- |
| **`POST`** | /locations |

### Example

Request
`http://localhost:4444/locations/:code`

<details>
<summary>Example Request Body</summary>

```json
  {
    "code": string;
  }
```

</details>

<details>
<summary>Example Response</summary>

```json
  {
    "data": {
      "location": {
        "id": number,
        "section": string,
        "bay": number,
        "startingSlot": number,
        "endingSlot": number,
        "code": string,
      },
    }
  }
```

</details>
