---
sidebar_position: 4
---

# Get Users By Query

```typescript
// Request
authAdapter.getUsersByQuery(field: string, operator: string, value: string)

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
