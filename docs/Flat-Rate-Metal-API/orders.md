# Order

## GET

### Get All

| Path      | Role  | Privileges  |
| --------- | ----- | ----------- |
| `/orders` | ADMIN | VIEW_ORDERS |

Retrieves all orders.

<details>
  <summary>Example Response</summary>

```json
{
  "data": []
}
```

</details>

### Get Active

| Path             | Role | Privileges         |
| ---------------- | ---- | ------------------ |
| `/orders/active` | N/A  | VIEW_ACTIVE_ORDERS |

Retrieves all orders that do not have the `FULFILLED`, `ARCHIVED`, or `CANCELLED` status.

#### Todo

&#x2610; Deprecate or refactor endpoint
&#x2610; Set role verification to `ADMIN`

<details>
  <summary>Example Response</summary>

```json
{
  "data": []
}
```

</details>

### Get By Requesting User

Get all orders accessible to the requesting user.

<details>
  <summary>Example Response</summary>

```json
{
  "data": []
}
```

</details>

### Get By ID

Get an order by ID.

<details>
  <summary>Example Response</summary>

```json
{
  "data": {}
}
```

</details>

### Get By Company ID

Get all orders associated with Company ID.

<details>
  <summary>Example Response</summary>

```json
{
  "data": []
}
```

</details>

### Email Reciept [Unique]

## POST

### Create Order - Guest Card

### Create Order - Retail Card

### Create Order - Company Card

### Create Order - Company Credit

### Create Order - Company ACH

## PUT

### Update Order

### Update Order Status - Confirm

### Update Order Status - Picking

### Update Order Status - Out For Delivery

### Update Order Status - Ready For Pickup

### Update Order Status - Fulfill

### Update Order Status - Archive [Unique]

### Update Order Status - Paid [Unique]

### Refund [Unique]

### Paid At Terminal [Unique]

### Card Payment Result

### Adjust [Unique]

### Adjust Order Items - Guest Card

### Adjust Order Items - Retail Card

### Adjust Order Items - Business Card

### Adjust Order Items - Business Credit

| Path                                            | Role  | Privileges    |
| ----------------------------------------------- | ----- | ------------- |
| `/orders/:orderId/adjust-items-business-credit` | ADMIN | UPDATE_ORDERS |

Add or remove items associated to a business credit order. Add or remove miscelaneous items.

<details>
  <summary>Example Request Body</summary>

```json
{
  "productsRemoved": string[],
  "productsUpdated": [{
    "specialId": string,
    "quantity": number,
    "individualPrice": number,
    "totalPrice" :number,
  }],
  "productsAdded": [{
    "id": string,
    "specialId": string,
    "quantity": number,
    "individualPrice": number,
    "totalPrice": number
  }]
}
```

</details>

<details>
  <summary>Example Response</summary>

```json
{
  "data": []
}
```

</details>

### Adjust Order Items - Business ACH

### Cancel Order - Guest

### Cancel Order - Retail

### Cancel Order - Business Card

### Cancel Order - Business Credit

### Cancel Order - Business ACH

### Cancel Order - Guest Public

### Cancel Order - Retail Public

### Cancel Order - Business Card Public

### Cancel Order - Business Credit Public

### Cancel Order - Business ACH Public

## DELETE
