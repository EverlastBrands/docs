---
sidebar_position: 5
---

# Update User

```typescript
// Request
UserUpdateInt {
  id: string;
  email?: string;
  phone?: string;
  name?: string;
}
const response = await authAdapter.updateUser(UserUpdateInt);

// Response
response = Boolean // true or false
```
