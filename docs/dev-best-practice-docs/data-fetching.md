# Data Fetching

To make API requests use the Fetch API or another authorized 3rd party API request library. The fetch API should be wrapped in an intuitive handler function that makes it easy to create requests and get responses.

## Data Fetching Example Function

```typescript
// filename: request.ts

export interface RequestInt {
  method: string;
  path: string;
  auth?: boolean;
  data?: any;
}

export default async function request({
  method = "GET",
  path,
  auth = false,
  data,
}: RequestInt) {
  try {
    const headers: any = {
      Accept: "application/json",
      "Content-type": "application/json",
    };
    if (auth) {
      // Get your access token to authenticate the request
      headers.Authorization = `Bearer ${ACCESS_TOKEN}`;
    }
    const config: any = {
      method,
      headers,
    };
    if (method.toLowerCase() !== "get" && method.toLowerCase() !== "delete") {
      config.body = JSON.stringify(data);
    }
    const response = await fetch(ENVIORNMENT + path, config);
    const processedResponse = await response.json();
    processedResponse.status = response.status;
    return processedResponse;
  } catch (err) {
    console.error(err);
  }
}
```

## React Query

React Query is a new addition to our Data Fetching and State Management strategy. It requests state and stores it using query keys and comes out of the box with great support for hooks.

There are 2 versions of this package that you need to be aware of:

- [Version 3](https://react-query-v3.tanstack.com/overview)
- [Version 4 - Also Known as Tanstack Query](https://tanstack.com/query/v4/docs/overview)

You may be asking yourself why shouldn't we just use version 4 to simplify things? Good questions. We started using this library fairly recently and seeming right after we started using version 3 the next version was released. At some point we will move over to version 4 but for the time being we will stick with version 3 in the projects that use it. If we start a new project then we should use version 4.
