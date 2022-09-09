# Users

## GET

### Users

Retrieves all users

| Method    | Path    | Cache Behavior | User Role |
| --------- | ------- | -------------- | --------- |
| **`GET`** | /users/ | Pull           | Admin     |

#### Example Response

<details>
<summary>Example Response</summary>

```javascript
function myFunction() {
  console.log("Hello world");
}
```

</details>

### User by ID

Retrieves a user by their ID

| Method    | Path           | Cache Behavior | User Role |
| --------- | -------------- | -------------- | --------- |
| **`GET`** | /users/:userId | Pull           | Admin     |

### Verify Email Token

| Method    | Path                       | Cache Behavior | User Role |
| --------- | -------------------------- | -------------- | --------- |
| **`GET`** | /users/verify-email/:token | N/A            | All       |

### User Company by Company ID

| Method    | Path                      | Cache Behavior | User Role |
| --------- | ------------------------- | -------------- | --------- |
| **`GET`** | /users/company/:companyId | Pull           | All       |

## POST

### Create Retail User

| Method     | Path          | Cache Behavior | User Role |
| ---------- | ------------- | -------------- | --------- |
| **`POST`** | /users/retail | Push           | Admin     |

### Create Retail User Public

| Method     | Path                 | Cache Behavior | User Role |
| ---------- | -------------------- | -------------- | --------- |
| **`POST`** | /users/retail-public | Push           | User      |

### Create Business User

| Method     | Path            | Cache Behavior | User Role |
| ---------- | --------------- | -------------- | --------- |
| **`POST`** | /users/business | Push           | Admin     |

### Create Business User Internal

| Method     | Path                     | Cache Behavior | User Role |
| ---------- | ------------------------ | -------------- | --------- |
| **`POST`** | /users/business-internal | ???            | ???       |

### Create Business User Public

| Method     | Path                   | Cache Behavior | User Role |
| ---------- | ---------------------- | -------------- | --------- |
| **`POST`** | /users/business-public | Push           | User      |

### Create Admin User

| Method     | Path         | Cache Behavior | User Role |
| ---------- | ------------ | -------------- | --------- |
| **`POST`** | /users/admin | Push           | Admin     |

### Create Admin User Initial

| Method     | Path                | Cache Behavior | User Role |
| ---------- | ------------------- | -------------- | --------- |
| **`POST`** | /users/admin-inital | Push & Pull    | N/A       |

### Password Login

| Method     | Path                  | Cache Behavior | User Role |
| ---------- | --------------------- | -------------- | --------- |
| **`POST`** | /users/password-login | Push & Pull    | All       |

### Sign Out

| Method     | Path            | Cache Behavior | User Role |
| ---------- | --------------- | -------------- | --------- |
| **`POST`** | /users/sign-out | Push           | All       |

### Refresh User

| Method     | Path           | Cache Behavior | User Role |
| ---------- | -------------- | -------------- | --------- |
| **`POST`** | /users/refresh | Pull           | All       |

### Reset User Password

| Method     | Path                  | Cache Behavior | User Role |
| ---------- | --------------------- | -------------- | --------- |
| **`POST`** | /users/reset-password | Pull           | All       |

### Add Retail Address

| Method     | Path                         | Cache Behavior | User Role |
| ---------- | ---------------------------- | -------------- | --------- |
| **`POST`** | /users/create-address-retail | Push & Pull    | User      |

### Create Public Business with User

| Method     | Path                             | Cache Behavior | User Role |
| ---------- | -------------------------------- | -------------- | --------- |
| **`POST`** | /users/business-public-with-user | Push & Pull    | User      |

### Get New Access Token

| Method     | Path                        | Cache Behavior | User Role |
| ---------- | --------------------------- | -------------- | --------- |
| **`POST`** | /users/get-new-access-token | N/A            | All       |

## PUT

### Edit User

| Method    | Path   | Cache Behavior | User Role |
| --------- | ------ | -------------- | --------- |
| **`PUT`** | /users | Push           | All       |

### Update Business User Internal

| Method    | Path                    | Cache Behavior | User Role |
| --------- | ----------------------- | -------------- | --------- |
| **`PUT`** | /users/:userId/internal | ???            | ???       |

### Add Device Push Token

| Method    | Path                         | Cache Behavior | User Role |
| --------- | ---------------------------- | -------------- | --------- |
| **`PUT`** | /users/add-device-push-token | Push & Pull    | User      |

### Password

| Method    | Path            | Cache Behavior | User Role |
| --------- | --------------- | -------------- | --------- |
| **`PUT`** | /users/password | N/A            | All       |

### Password Update

| Method    | Path                   | Cache Behavior | User Role |
| --------- | ---------------------- | -------------- | --------- |
| **`PUT`** | /users/password-update | Pull           | All       |

### Archive Self

| Method    | Path                | Cache Behavior | User Role |
| --------- | ------------------- | -------------- | --------- |
| **`PUT`** | /users/archive-self | Push & Pull    | All       |

### Update Notification Settings

| Method    | Path                                | Cache Behavior | User Role |
| --------- | ----------------------------------- | -------------- | --------- |
| **`PUT`** | /users/update-notification-settings | Push & Pull    | All       |

### Update Default Address

:::caution Unused Endpoint
:::

| Method    | Path                          | Cache Behavior | User Role |
| --------- | ----------------------------- | -------------- | --------- |
| **`PUT`** | /users/update-default-address | Push & Pull    | User      |

### Update Notification

| Method    | Path                       | Cache Behavior | User Role |
| --------- | -------------------------- | -------------- | --------- |
| **`PUT`** | /users/update-notification | Push & Pull    | All       |

### Favorites

| Method    | Path             | Cache Behavior | User Role |
| --------- | ---------------- | -------------- | --------- |
| **`PUT`** | /users/favorites | Push & Pull    | User      |

### Favorite Product by Product ID

:::danger Deprecated Endpoint
:::

| Method    | Path                                | Cache Behavior | User Role |
| --------- | ----------------------------------- | -------------- | --------- |
| **`PUT`** | /users/favorite-product/:product-id | Push & Pull    | User      |

### Edit User by User ID

:::info Needs Refactoring
:::

| Method    | Path           | Cache Behavior | User Role |
| --------- | -------------- | -------------- | --------- |
| **`PUT`** | /users/:userId | Push & Pull    | Admin     |

### Edit User Password by User ID

| Method    | Path                    | Cache Behavior | User Role |
| --------- | ----------------------- | -------------- | --------- |
| **`PUT`** | /users/:userId/password | Push & Pull    | Admin     |

### Archive User by User ID

| Method    | Path                   | Cache Behavior | User Role |
| --------- | ---------------------- | -------------- | --------- |
| **`PUT`** | /users/:userId/archive | Push & Pull    | Admin     |

### Disable User by User ID

| Method    | Path                   | Cache Behavior | User Role |
| --------- | ---------------------- | -------------- | --------- |
| **`PUT`** | /users/:userId/disable | Push & Pull    | Admin     |

### Activate User by User ID

| Method    | Path                    | Cache Behavior | User Role |
| --------- | ----------------------- | -------------- | --------- |
| **`PUT`** | /users/:userId/activate | Push & Pull    | Admin     |

### Update Retail Address by Address ID

| Method    | Path                                    | Cache Behavior | User Role |
| --------- | --------------------------------------- | -------------- | --------- |
| **`PUT`** | /users/update-address-retail/:addressId | Push & Pull    | User      |

## DELETE

### Delete User by ID

| Method       | Path           | Cache Behavior | User Role |
| ------------ | -------------- | -------------- | --------- |
| **`DELETE`** | /users/:userId | Push & Pull    | Admin     |

### Delete Retail Address by Address ID

| Method       | Path                                    | Cache Behavior | User Role |
| ------------ | --------------------------------------- | -------------- | --------- |
| **`DELETE`** | /users/delete-address-retail/:addressId | Push & Pull    | User      |

### Delete Business User Internal

| Method       | Path                    | Cache Behavior | User Role |
| ------------ | ----------------------- | -------------- | --------- |
| **`DELETE`** | /users/:userId/internal | ???            | ???       |
