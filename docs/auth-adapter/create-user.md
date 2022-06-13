---
sidebar_position: 5
---

# Create User

```typescript
// Request
NewUserInt {
  email: string;
  password: string;
  name?: string;
  phone?: string;
}

authAdapter.createUser(NewUserInt);

// Response
{
  id: "new-user-id";
}
```
