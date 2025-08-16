
# How to Push Files to GitHub: Complete Guide

This guide provides a detailed, step-by-step instruction on how to push your local files to GitHub using **Git**.

---

## Prerequisites

1. **Git Installed**: Make sure Git is installed on your computer. You can download it from [https://git-scm.com/](https://git-scm.com/).  
2. **GitHub Account**: Create a GitHub account if you don't have one at [https://github.com/](https://github.com/).  
3. **Repository**: Create a new repository on GitHub:
   - Go to GitHub → Click **New Repository**.
   - Give your repository a **name**, description (optional), and select **Public** or **Private**.
   - Click **Create Repository**.

---

## Step 1: Initialize Git in Local Folder

1. Open **Terminal** (macOS/Linux) or **Git Bash** (Windows).  
2. Navigate to your project folder:
   ```bash
   cd /path/to/your/project
   ```
3. Initialize Git in the folder:
   ```bash
   git init
   ```
   You should see:
   ```
   Initialized empty Git repository in /path/to/your/project/.git/
   ```

---

## Step 2: Configure Git (First Time Only)

Set your Git username and email:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
Check your configuration:
```bash
git config --list
```

---

## Step 3: Add Files to Git

Add all files in your folder to Git:
```bash
git add .
```
> The `.` means add all files. You can also add a specific file: `git add filename.ext`.

---

## Step 4: Commit Changes

Commit your changes with a message:
```bash
git commit -m "Initial commit"
```
> Commit messages should be meaningful and describe the changes.

---

## Step 5: Connect Local Repository to GitHub

1. Copy your repository URL from GitHub. It looks like:  
   ```
   https://github.com/username/repository.git
   ```
2. Add it as a remote origin:
```bash
git remote add origin https://github.com/username/repository.git
```
3. Verify remote URL:
```bash
git remote -v
```

---

## Step 6: Push Files to GitHub

Push your local files to GitHub:
```bash
git branch -M main
git push -u origin main
```

- `git branch -M main` ensures your branch is named `main`.
- `git push -u origin main` pushes your changes to GitHub and sets upstream tracking.

---

## Step 7: Verify

Go to your GitHub repository in a browser. You should see your files uploaded.

---

## Step 8: Updating Files (Optional)

When you make changes and want to update GitHub:

```bash
git add .
git commit -m "Describe changes"
git push
```

---

## Common Issues

1. **Authentication Failed**: Use a personal access token instead of your password if GitHub requires it.
2. **Branch Already Exists**: Make sure your branch name matches (`main` or `master`) or rename it.
3. **Changes Not Showing**: Check if you committed changes before pushing.

---

## Resources

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/en)
