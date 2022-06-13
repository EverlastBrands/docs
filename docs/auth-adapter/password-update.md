---
sidebar_position: 7
---

# Password Update

```typescript
// Request
const result = await authAdapter.passwordUpdate(
  "user-id",
  "current-password",
  "new-password"
);

// Response
response = Boolean; // true or false
```
