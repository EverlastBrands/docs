---
sidebar_position: 11
---

# Login With Token

```typescript
// Request
authAdapter.loginWithToken("login-token");

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
