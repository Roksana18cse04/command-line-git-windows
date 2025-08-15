# Git Learning Guide: Windows Command Line

Learn Git step-by-step using Windows Command Prompt. Covers initialization, staging, committing, pushing, pulling, branching, merging, and using `.gitignore`.

---

## 1️⃣ Setup & Configuration

```cmd
git --version
git config --global user.name "ROKANA"
git config --global user.email "roksana18cse04@gmail.com"
git config --list
```

---

## 2️⃣ Initialize Repository

```cmd
git init
```

---

## 3️⃣ Check Status

```cmd
git status
```

---

## 4️⃣ Add Files to Staging Area

* Single file:

```cmd
git add filename.extension
```

* All files:

```cmd
git add --all
```

* See changes:

```cmd
git diff
```

---

## 5️⃣ Commit Changes

```cmd
git commit -m "Your commit message"
```

### Undo a commit

* Soft reset (keep changes):

```cmd
git reset --soft HEAD~
```

* Hard reset (discard changes):

```cmd
git reset --hard HEAD~
```

---

## 6️⃣ View Commit History

```cmd
git log
git log --oneline
```

---

## 7️⃣ Connect to GitHub

```cmd
git remote add origin https://github.com/USERNAME/REPO_NAME.git
git remote -v
```

---

## 8️⃣ Push Changes to GitHub

```cmd
git push -u origin main
```

> `-u` sets upstream branch.

---

## 9️⃣ Pull Changes from GitHub

```cmd
git pull origin main
```

> Pull updates your local repository with changes from remote.

---

## 🔟 Branching & Merging

### Create a new branch

```cmd
git checkout -b feature-branch
```

### Switch between branches

```cmd
git checkout main
git checkout feature-branch
```

### Rename a branch

```cmd
git branch -m old-branch-name new-branch-name
```

### Merge branches

* Merge `feature-branch` into `main`:

```cmd
git checkout main
git merge feature-branch
```

> Resolve conflicts if Git prompts you.

---

## 1️⃣1️⃣ Go Back to Previous Commits

* View commit history:

```cmd
git log --oneline
```

* Go to a previous commit (detached HEAD):

```cmd
git checkout <commit-hash>
```

* Return to latest commit:

```cmd
git checkout main
```

---

## 1️⃣2️⃣ Use `.gitignore`

### Why

* Avoid unnecessary files
* Keep repo clean
* Prevent sensitive data leaks

### Example `.gitignore`

```
# OS files
Thumbs.db
.DS_Store

# Python
__pycache__/
*.pyc
*.pyo
.env

# IDE/editor
.vscode/
.idea/

# Logs
*.log

# Build files
dist/
build/
```

---

## 1️⃣3️⃣ Recommended Workflow

1. Check status: `git status`
2. Add files: `git add filename.extension` or `git add --all`
3. Commit changes: `git commit -m "message"`
4. Pull latest changes: `git pull origin main`
5. Push changes: `git push -u origin main`
6. Create or switch branches: `git checkout -b branch-name`
7. Merge branches: `git merge branch-name`
─────────────────────────────────────────────
          GIT SETUP & CONFIGURATION
─────────────────────────────────────────────
Check version:        git --version
Set username:         git config --global user.name "ROKANA"
Set email:            git config --global user.email "roksana18cse04@gmail.com"
View settings:        git config --list

─────────────────────────────────────────────
          REPOSITORY INIT & STATUS
─────────────────────────────────────────────
Init repo:            git init
Check status:         git status
See changes:          git diff

─────────────────────────────────────────────
          STAGING & COMMITTING
─────────────────────────────────────────────
Add single file:      git add filename.ext
Add all files:        git add --all
Commit changes:       git commit -m "message"
Undo last commit:
  soft (keep changes): git reset --soft HEAD~
  hard (discard):      git reset --hard HEAD~

─────────────────────────────────────────────
          REMOTE REPOSITORY
─────────────────────────────────────────────
Add remote:           git remote add origin URL
Check remote:         git remote -v
Push changes:         git push -u origin main
Pull changes:         git pull origin main

─────────────────────────────────────────────
          BRANCHING & MERGING
─────────────────────────────────────────────
Create branch:        git checkout -b branch-name
Switch branch:        git checkout branch-name
Rename branch:        git branch -m old-name new-name
Merge branch:         git checkout main
                      git merge branch-name
Resolve conflicts if prompted

─────────────────────────────────────────────
          COMMITS & HISTORY
─────────────────────────────────────────────
View log:             git log
Compact log:          git log --oneline
Go to previous commit:git checkout <commit-hash>
Return to latest:     git checkout main

─────────────────────────────────────────────
          .GITIGNORE
─────────────────────────────────────────────
# OS
Thumbs.db
.DS_Store

# Python
__pycache__/
*.pyc
.env

# IDE/editor
.vscode/
.idea/

# Logs & build
*.log
dist/
build/

─────────────────────────────────────────────
          RECOMMENDED WORKFLOW
─────────────────────────────────────────────
1. git status
2. git add filename.ext / git add --all
3. git commit -m "message"
4. git pull origin main
5. git push -u origin main
6. git checkout -b branch-name (if needed)
7. git merge branch-name (if needed)
─────────────────────────────────────────────


