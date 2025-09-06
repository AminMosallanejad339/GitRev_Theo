## 🔄 Git File States

### 1. **Untracked** → **Staged**
```bash
git add filename.py           # Stage specific file
git add .                    # Stage all changes
git add *.py                 # Stage all Python files
```

### 2. **Staged** → **Committed**
```bash
git commit -m "Your message"  # Commit staged changes
```

### 3. **Staged** → **Unstaged** (Restore)
```bash
git restore --staged filename.py  # Unstage specific file
git restore --staged .           # Unstage all files
```

### 4. **Modified** → **Original** (Discard changes)
```bash
git restore filename.py        # Discard changes in working directory
git checkout -- filename.py    # Alternative (older syntax)
```

### 5. **Checkout** (Switch branches/commits)
```bash
git checkout main              # Switch to main branch
git checkout feature-branch    # Switch to feature branch
git checkout commit-hash       # Checkout specific commit
git checkout HEAD~1           # Checkout previous commit
```

## 📋 Current Status Commands

```bash
git status                     # Show all states
git status -s                 # Short status
```

## 🔍 View Differences

```bash
git diff                      # Unstaged changes
git diff --staged             # Staged changes
git diff HEAD                 # All changes since last commit
```

## 📤 Push to GitHub

```bash
git push origin main          # Push to main branch
git push origin feature       # Push to feature branch
```

## 🗑️ Delete/Revert

```bash
git rm filename.py            # Remove file from git and disk
git rm --cached filename.py   # Remove from git only (keep file)
git reset --soft HEAD~1       # Undo commit but keep changes staged
git reset --hard HEAD~1       # Completely remove last commit
```

## 🏷️ Tagging (Releases)

```bash
git tag v1.0                  # Create tag
git push origin v1.0          # Push tag to GitHub
```

## Example Workflow:
```bash
# 1. Check status
git status

# 2. Stage files
git add .

# 3. Check what's staged
git diff --staged

# 4. Commit
git commit -m "Add new features"

# 5. Push to GitHub
git push origin main
```

# 🔧 Complete Git Workflow Guide

## 📊 **1. FILE STATES in Git**

### **Four Main States:**
1. **Untracked** - New file, not in Git yet
2. **Modified** - Changed but not staged  
3. **Staged** - Ready to be committed
4. **Committed** - Safely stored in repository

## 🎯 **2. STAGING Files (git add)**

### **Stage Specific Files:**
```bash
git add filename.py           # Single file
git add file1.py file2.py    # Multiple files
git add *.py                 # All Python files
```

### **Stage All Changes:**
```bash
git add .                    # All new and modified files
git add -A                  # All files (including deletions)
git add -u                  # Only modified files (no new files)
```

## ↩️ **3. RESTORING/UNSTAGING (git restore)**

### **Unstage Files:**
```bash
git restore --staged filename.py     # Unstage single file
git restore --staged *.py           # Unstage all Python files
git restore --staged .              # Unstage everything
```

### **Discard Changes:**
```bash
git restore filename.py             # Discard unstaged changes
git restore .                      # Discard all unstaged changes
```

## 🔍 **4. CHECKOUT (Switching/Exploring)**

### **Switch Branches:**
```bash
git checkout main                  # Switch to main branch
git checkout develop              # Switch to develop branch
git checkout -b new-feature       # Create and switch to new branch
```

### **Explore History:**
```bash
git checkout HEAD~1               # Go to previous commit
git checkout a1b2c3d             # Go to specific commit
git checkout main -- filename.py  # Get file from main branch
```

### **Return to Current:**
```bash
git checkout main                 # Return to latest commit on main
```

## 💾 **5. COMMITTING (git commit)**

### **Basic Commit:**
```bash
git commit -m "Add new feature"    # Commit with message
```

### **Commit Options:**
```bash
git commit -am "Message"          # Add all modified and commit
git commit --amend               # Fix last commit
git commit --no-verify           # Skip pre-commit hooks
```

### **Good Commit Messages:**
```
feat: add user authentication
fix: resolve login bug
docs: update README
style: format code
refactor: improve performance
```

## 📤 **6. PUSHING to GitHub**

### **Push to Remote:**
```bash
git push origin main              # Push main branch
git push origin feature-branch    # Push specific branch
git push -u origin main          # Set upstream and push
```

### **Force Push (Careful!):**
```bash
git push --force origin main     # Overwrite remote history
git push --force-with-lease     # Safer force push
```

## 🔄 **7. Complete Workflow Example**

```bash
# 1. Check current status
git status

# 2. Stage all changes
git add .

# 3. Verify what's staged
git diff --staged

# 4. Commit changes
git commit -m "Add new Python scripts"

# 5. Push to GitHub
git push origin main

# 6. Verify remote status
git status
```

## 🚨 **8. Emergency Operations**

### **Undo Last Commit (Keep Changes):**
```bash
git reset --soft HEAD~1
```

### **Completely Remove Last Commit:**
```bash
git reset --hard HEAD~1
```

### **Recover Lost Commit:**
```bash
git reflog                     # Find lost commit hash
git checkout a1b2c3d          # Go to that commit
git checkout -b recovered      # Create branch to save it
```

## 📋 **9. Status Checks**

```bash
git status                    # Full status
git status -s                # Short status
git log --oneline -5         # Recent commits
git diff                     # Unstaged changes
git diff --staged           # Staged changes
```

## 🎪 **10. Special Scenarios**

### **Stage Parts of File:**
```bash
git add -p filename.py       # Interactive staging
```

### **Temporarily Hide Changes:**
```bash
git stash                   # Save changes temporarily
git stash pop              # Restore stashed changes
```

### **Move Between Branches:**
```bash
# Save current work
git stash

# Switch branch
git checkout other-branch

# Do work, then return
git checkout original-branch
git stash pop
```

## ✅ **Verification Commands**

```bash
# Verify staging
git diff --staged

# Verify remote connection
git remote -v

# Verify branch status
git branch -vv

# Verify commit history
git log --oneline --graph -10
```

