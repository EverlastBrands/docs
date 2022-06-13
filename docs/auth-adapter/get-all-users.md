---
sidebar_position: 3
---

# Get All Users

```typescript
// Request
authAdapter.getAllUsers();

// Response
{
  users: [
    {
      id: string;
      loginAttempts: number;
      loginDates: number[];
      passwordResetAttempts: number;
      passwordResetDates: number[];
      registeredDate: number;
      appId: string;
      appName: string;
      accountId: string;
      email: string;
      name: string;
      phone: string;
      emailVerified: boolean;
      multiFactorAuth: {
        sms: boolean;
        email: boolean;
        app: boolean;
        biometric: boolean;
      }
    },
    {...}
  ]
}
```
