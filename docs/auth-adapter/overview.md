---
sidebar_position: 1
---

# Overview

## Description

Optional package when developing new services for everlast brands. This package provides utilities for applications and users to manage identities and connects to our main Auth API.

## Installation

```bash
yarn add @everlast-brands/auth-adapter
# or
npm install @everlast-brands/auth-adapter
```

## Setup

```javascript
import { AuthAdapter } from "@everlast-brands/auth-adapter";

export const authInit = authAdapter({
  enviornmentAddress: "http://127.0.0.1",
  appAPIKey: process.env.APP_API_KEY,
  appID: process.env.APP_ID,
});
```

## Usage

Auth Adapter is used to interact with users identities which is helpful for authentication purposes. There are a number of ways this adapter can be used to provide authentication to client applications.

1. Stateless Log in - Each time a request is made a stateless token commonly a JWT can be used to identify the requesting user and authenticate them with the system.
2. Stateful Log in - Each time a request is made an arbitrary token preferably not a jwt is compared to a session stored on the server that authenticates the user.

Each has their advantages and disadvantages ranging from performance to security. This AuthAdapter, when configured correctly, will comunicate with the authentication server and facilitate communication.
