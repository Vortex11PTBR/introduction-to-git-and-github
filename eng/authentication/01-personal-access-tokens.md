# Personal Access Tokens (PATs)

Personal Access Tokens (PATs) are a secure alternative for authentication on GitHub/GitLab, especially when SSH authentication is not feasible or preferred. They function like passwords but with defined scope and validity, offering greater control over permissions.

## When to use PATs?

- When you need programmatic access to your repositories.
- In environments where SSH configuration is complex or restricted.
- To integrate third-party tools that need to interact with your repositories.

## How to create a PAT (GitHub)

1.  **Access Developer Settings**: On GitHub, go to `Settings` > `Developer settings` > `Personal access tokens` > `Tokens (classic)`.
2.  **Generate a New Token**: Click on `Generate new token`.
3.  **Define Scope and Validity**: Choose the permissions (scopes) the token will have (e.g., `repo` for full repository access) and set an expiration date.
4.  **Save the Token**: After creation, the token will be displayed **only once**. Copy it and store it in a **secure** location, such as a password manager. **Never share your PAT publicly.**

## How to use a PAT

When performing Git operations that require authentication (such as `git push` or `git clone` via HTTPS), you will be prompted to provide your username and password. Instead of your account password, you will use the PAT.

```bash
Username for 'https://github.com': your_username
Password for 'https://your_username@github.com': your_personal_access_token
```

**Important**: Always set an expiration date for your PATs and revoke them when they are no longer needed to minimize security risks.
