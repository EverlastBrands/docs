---
sidebar_position: 1
---

# Overview

## Description

This API exists to standardize authentication accross services used by Everlast Brands Apps. We require a lot of direct control over our applications authorization however authentication can be extracted and used in a more general sense accross the organization for both internal and external use. This service is created in such a way that if the need arises it can be replaced by a third party solution. At this point we do not require third party services as the data we store is never excessively personal such as SSN, Passport Numbers or any form of payment number.

There are two kinds of information that we store. Customer information and Team member information. Lets go through the limits of what we can store in detail bellow:

### Common Information

- User Name
- Full Name
- Email Addresses
- Phone Number
- Password Hashes
- Devices (To limit login locations)

### Customer Information

- Home Addresses
- Business Addresses
- Birthday day of month (excludes year)
- Complete Birthday (in instances where age is a restriction)

### Team Member Information

- Current Geo Location
- Location History

## Usage

All urls follow this pattern

```Javascript
const url = '${process.env.AUTH_SERVER_IP}/${entity}/${api_version}/__PATH__?appId=${process.env.APP_ID}`
```

All responses follow this pattern

```
{
  status: "success", // "success" or "failure"
  // optional
  data: object,
  msg: string
}
```

### User Operations

Users represent people, they are used to authenticate in our apps. Each user is uniquely identified by 2 to 3 things.

1. email - only one user account per email per app
2. userId - given in the database
3. **(optional)** username - depending on the app and the strategy we want to take

#### Register

Registers a new user into the system

```Javascript
const method = 'post';
const path = '/users/v1`;
const data = {
  email: "example@test.com",
  password: "plain text password", // Maybe we should bit 64 encod this?
  // optional
  username: "Crazyguy123"
}
```

**Response**

```
{
  userId: string
}
```

#### Login

Returns user information

```Javascript
const method = 'post';
const path = '/users/v1//login`;
const data = {
  password: "plain text password", // Maybe we sould bit 64 encod this?
  // optional - must include one
  email: "example@test.com",
  username: "Crazyguy123"
}
```

**Response**

```
{
  userId: string,
  email: string,
  username: string,
  token: string
}
```

#### Verify Email

Verifies the user identity for any arbitrary request. Requires a JWT.

```Javascript
const method = 'get';
const path = '/verify-email/:token`;
```

**Response**

```
{
  userId: string,
  email: string,
  username: string
}
```

#### Password Reset

If password needs to be reset from a secure domain this is endpoint to call.

```Javascript
const method = 'post';
const path = '/users/v1/password-reset`;
const data = {
  newPassword: string,
  token: string,
}
```

**Response**

```
{
  userId: string,
}
```

#### Change Password

```Javascript
const method = 'post';
const path = '/users/v1/password-change`;
const data = {
  newPassword: string,
  token: string
}
```

**Response**

```
{
  userId: string,
}
```

#### Email Login Link

```Javascript
const method = 'get';
const path = '/email-login/:token`;
```

**Response**

```
{
  userId: string,
  email: string,
  username: string,
  token: string
}
```

#### Update Information

```Javascript
const method = 'put';
const path = '/update`;
const data = {
  username: string,
  token: string,
  phone: string
}
```

**Response**

```
{
  email: string,
  username: string,
  phone: string,
  userId: string,
}
```

### App Operations

Apps are external services that use the Everlast Brands Auth service to authenticate users. Apps take care of their own sessions and authorization but they register and login users with the auth server.

Each app has a single unique identifier the appId.

#### Create App

```Javascript
const method = 'post';
const path = '/app/v1`;
const data = {
  name: string,
  description: string,
  url: string,
}
```

**Response**

```
{
  id: string;
  name: string;
  description: string;
  url: string;
  key: string;
}
```

## Technologies

### Firestore

Perminant user data storage

### Redis

User session storage
