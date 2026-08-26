
**Authentication** – process of verifying the identity of a user or client.
- **Something you know** – password, PIN, security question.
- **Something you have** – phone, security token, smart card.
- **Something you are/do** – biometrics or behavior, e.g. fingerprint, face, typing pattern.
##### Vulnerabilities in password-based login:
- **Brute-force attacks** - using trial and error to guess valid user credentials, such as username or passwords.
- **Flawed brute-force protection** - flawed account-locking mechanisms, e.g. resetting the account lockout timer after a successful login with valid credentials, or blocking users based on their IP address instead of reliably identifying the source of the requests.
##### Vulnerabilities in multi-factor authentication
- **Flawed two-factor verification logic** - failing to properly verify that the user completing the second authentication step is the same user who completed the first step.
- **Bypassing two-factor authentication** - accessing protected pages directly after entering valid login credentials, without completing the 2FA verification step.
- **Brute-forcing 2FA verification codes** - guessing short verification codes, such as 4- or 6-digit numbers, when the application does not implement effective rate limiting or account lockout mechanisms.


`X-Forwarded-For` – HTTP header used by proxies to pass the original client's IP address to the backend server.