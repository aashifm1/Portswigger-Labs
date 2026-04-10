# 2FA simple bypass

With below valid credentials, the two factor authentication cann be bypassed

```bash
**My credentials**: wiener:peter
**Victim's credentials**: carlos:montoya
```

- login /my-account with given credentials

- When i enter the creds carlos:montoya, it redirects to another page (login2)

<img width="700" height="400" alt="Screenshot 2026-04-09 185929" src="https://github.com/user-attachments/assets/281b976b-abde-434a-bcb3-3e1b90910c6a" />



> It is a vulnerability that when entered correct creds you are in already **"logged-in"** state, when it redirects to another page.

When /login2 for the verification code, i skipped it manually as /my-account which eventually bypassed the Two factor authentication. That eventually gave access to carlos's account.
