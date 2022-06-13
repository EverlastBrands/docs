---
sidebar_position: 10
---

# Login

```typescript
// Request
LoginInt {
  email: string;
  password: string;
}

authAdapter.login(LoginInt);

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
