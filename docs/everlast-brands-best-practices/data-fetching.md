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
