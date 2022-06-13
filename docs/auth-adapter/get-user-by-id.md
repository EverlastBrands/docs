---
sidebar_position: 2
---

# Get User By Id

```typescript
// Request
authAdapter.getUserById("user-id-string")

// Response
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
}
```
