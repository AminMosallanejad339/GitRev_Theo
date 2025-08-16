
# How to Update Files on GitHub

This guide explains how to update existing files in a GitHub repository using Git.

---

## Step 1: Open Terminal / Git Bash

Open **Terminal** (macOS/Linux) or **Git Bash** (Windows) and navigate to your local repository:

```bash
cd /path/to/your/project
```

---

## Step 2: Check Repository Status

Check which files have changed:

```bash
git status
```

You’ll see modified, added, or deleted files listed.

---

## Step 3: Stage the Changes

Add files you want to update to the staging area:

```bash
git add filename.ext
```

- To add **all changed files**:

```bash
git add .
```

---

## Step 4: Commit the Changes

Commit your changes with a descriptive message:

```bash
git commit -m "Update: describe what changed"
```

- Example:

```bash
git commit -m "Update README with GitHub push instructions"
```

---

## Step 5: Push Changes to GitHub

Push your committed changes to the remote repository:

```bash
git push
```

- If pushing for the first time on a branch:

```bash
git push -u origin main
```

---

## Step 6: Verify on GitHub

Go to your GitHub repository in a browser. The updated files should now be visible.

---

## Optional: Pull Changes from GitHub

Before making updates, it’s good practice to sync your local repository:

```bash
git pull origin main
```

- This fetches any updates from GitHub and merges them with your local repository.

---

## Summary

1. `git status` → check changes
2. `git add` → stage changes
3. `git commit -m "message"` → commit changes
4. `git push` → update GitHub
5. `git pull` → sync before editing (optional)
