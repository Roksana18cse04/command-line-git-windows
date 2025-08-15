
# Windows Command Line Git Setup Guide

This guide shows how to initialize a Git repository, track files, commit changes, and connect to GitHub using Windows Command Prompt.

---

## 1. Check if Git is initialized

```cmd
git remote
````

---

## 2. Git Configuration

Set your username and email:

```cmd
git config user.name "ROKANA"
git config user.email "roksana18cse04@gmail.com"
git config --list
```

---

## 3. Initialize Git repository

```cmd
git init
```

---

## 4. Check repository status

```cmd
git status
```

---

## 5. Add files to staging area

* Add a single file:

```cmd
git add filename.extension
```

Example:

```cmd
git add Windows-cmd.txt
```

* Add all files:

```cmd
git add --all
```

* See changes before committing:

```cmd
git diff
```

---

## 6. Commit changes

```cmd
git commit -m "Your commit message"
```

Example:

```cmd
git commit -m "Windows command prompt"
```

### Undo a commit

* Keep changes in working directory:

```cmd
git reset --soft HEAD~
```

* Remove changes completely:

```cmd
git reset --hard HEAD~
```

---

## 7. View commit history

```cmd
git log
git log --oneline
```

---

## 8. Connect to GitHub

1. Add remote repository:

```cmd
git remote add origin https://github.com/Roksana18cse04/Windows-Command-line-Status.git
```

2. Verify remote:

```cmd
git remote -v
```

---

## 9. Push changes to GitHub

```cmd
git push -u origin main
```

---

## 10. Recommended Git Workflow

1. `git add filename.extension`
2. `git status`
3. `git commit -m "message"`
4. `git push -u origin main`

```

---

