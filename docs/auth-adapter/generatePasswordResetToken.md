---
sidebar_position: 14
---

# Generate Password Reset Token

```typescript
// Request
const result = await authAdapter.generatePasswordResetToken("user-id");

// Response
{
  token: string;
}
```
