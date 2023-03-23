# POST Create Business User Internal

Use this method to allow company admins to create additional users in their company.

| verb       | path                     |
| ---------- | ------------------------ |
| **`POST`** | /users/business-internal |

| Body             | Type     | Description                                                      | Required |
| ---------------- | -------- | ---------------------------------------------------------------- | -------- |
| **`name`**       | `string` | Unique product name potentially containing the material or color | true     |
| **`email`**      | `string` | Positive whole number (USD in pennies)                           | true     |
| **`privileges`** | `array`  | Unique category identifier                                       | true     |
| **`phone`**      | `number` | `SINGLE` `BOX` `BUNDLE` `CARTON` `ft` `PAIR` `COIL` `PIECE`      | false    |
