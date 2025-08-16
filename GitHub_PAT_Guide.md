
# How to Generate a GitHub Personal Access Token (PAT)

GitHub now requires a **personal access token (PAT)** for HTTPS Git operations instead of your password. This guide explains how to generate one.

---

## Step 1: Sign in to GitHub

1. Go to [https://github.com](https://github.com) and log in with your account.

---

## Step 2: Go to Developer Settings

1. Click your profile picture in the top-right corner.
2. Select **Settings**.
3. Scroll down and click **Developer settings** in the left sidebar.

---

## Step 3: Access Personal Access Tokens

1. Click **Personal access tokens**.
2. Then click **Tokens (classic)** (or "Fine-grained tokens" if preferred).
3. Click **Generate new token** → **Generate new token (classic)**.

---

## Step 4: Configure Token

1. **Note**: Give your token a descriptive name, e.g., `GitHub CLI Access`.
2. **Expiration**: Choose an expiration period (e.g., 30 days, 90 days, or no expiration).
3. **Select Scopes**: These determine what the token can do:
   - For pushing code to repositories, select:
     - `repo` → Full control of private repositories (includes read/write access)
     - `workflow` (optional, for GitHub Actions)
   - For general usage, you can select only `repo`.

---

## Step 5: Generate Token

1. Click **Generate token** at the bottom.
2. Copy the token immediately and store it safely.
   > You **won’t be able to see it again** once you leave the page.

---

## Step 6: Use Token for Git Operations

When Git asks for a username and password:

- **Username**: Your GitHub username
- **Password**: Paste the personal access token

Example for HTTPS push:
```bash
git push https://github.com/username/repository.git
Username: your_username
Password: your_token
```

---

## Step 7: Optional – Store Token Locally

To avoid entering it every time:

```bash
git config --global credential.helper store
```

The next time you enter your token, Git will remember it.

---

## Resources

- [GitHub Docs: Creating a Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
