# Multi-PC GitHub Workflow Guide

A quick-reference guide for syncing work across different computers using GitHub branches.

---

## 1. Clone to Your Second PC
Get your project files onto a new computer by creating a local copy.

1. **On GitHub:** Go to your repository, click **Code**, and copy the URL.
2. **In Terminal (New PC):** Run the clone command:
   ```bash
   git clone https://github.com/USERNAME/REPOSITORY.git
   ```

---

## 2. Create a New Branch & Work
Isolate your new changes from the main project version.

* **Create & switch to a new branch:**
  ```bash
  git checkout -b new-feature
  ```
* **Save work locally (Stage & Commit):**
  ```bash
  git add .
  git commit -m "Describe your changes here"
  ```
* **Push branch to GitHub:**
  ```bash
  git push origin new-feature
  ```

---

## 3. Merge Changes
Combine your finished work back into the main project.

### Option A: Via GitHub Website (Recommended)
1. Go to your repository on GitHub.
2. Click **Compare & pull request** next to your branch notification.
3. Click **Create pull request**.
4. Click **Merge pull request** if there are no conflicts.

### Option B: Via Terminal (Local Merge)
```bash
git checkout main         # Switch to main branch
git pull origin main      # Ensure main is up to date
git merge new-feature     # Merge feature into main
git push origin main      # Upload merged version to GitHub
```

---

## 🔄 Keeping PCs Synced
Always download the latest changes before starting work on any PC:
```bash
git checkout main
git pull origin main
```
