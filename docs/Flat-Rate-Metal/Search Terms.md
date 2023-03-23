# Search Terms

## GET

### Get All Search Terms

| Method    | Path          | Cache Behavior | User Role |
| --------- | ------------- | -------------- | --------- |
| **`GET`** | /search-terms | Pull           | Admin     |

#### Example

Request
`https://frm-prod.everlastbrands.dev/frm-api/search-terms`

<details>
<summary>Example Response</summary>

```json
{
  "data": {
    "results": [
      {
        "id": "aslkdjwonawedfoiasdji", // required
        "term": "Steel Drip Edge", // required
        "userId": "2k3lj;lksdjfoaid", // optional
        "timestamp": 123132452435234 // required
      }
    ]
  }
}
```

</details>

## POST

### Create Search Term

| Method     | Path          | Cache Behavior | User Role |
| ---------- | ------------- | -------------- | --------- |
| **`POST`** | /search-terms | none           | All       |

| Query       | Description | Required |
| ----------- | ----------- | -------- |
| **`query`** | Search term | Required |
| **`id`**    | User ID     | Optional |
