# 📘 Git Version Control System - Cheat Sheet

This repository is dedicated to learning Git — the most popular version control system used in software development. Below is a categorized collection of essential Git commands for daily use.

---

## 🛠️ Project Initialization & Configuration

```bash
git init                          # Initialize a new Git repository
git add <filename>               # Add file(s) to staging area
git commit -m "message"          # Commit staged changes with a message

git config --global user.name "your_name"
git config --global user.email "your_email"
```

---

## 🔍 Viewing Project State

```bash
git status                       # Show the working directory status
git log                          # View commit history
git log --all
git log --all --oneline
git log --oneline --all --graph
```

---

## 🌿 Branching

```bash
git branch                       # List local branches
git branch -a                    # List all branches (remote + local)
git branch -r                    # List remote branches
git branch <branch_name>         # Create new branch
git checkout -b <branch_name>    # Create and switch to new branch
git checkout <branch_name>       # Switch to existing branch
git branch -d <branch_name>      # Delete a branch
```

---

## 🔁 Stashing Changes

```bash
git stash -m "message"           # Stash changes with message
git stash list                   # List all stashes
git stash apply index            # Apply specific stash
git stash drop index             # Drop specific stash
git stash clear                  # Clear all stashes
```

---

## 🔄 Remote Repositories

```bash
git remote show origin           # Show info about remote origin
git remote add origin <URL>      # Add a remote repository
git branch -M origin             # Rename current branch to 'origin'
git push -u origin main          # Push local branch to remote
git push                         # Push committed changes
git fetch                        # Fetch changes from remote
git pull                         # Fetch and merge changes
git merge origin/main            # Merge remote main branch into current
```

---

## 🔧 Undo / Revert / Reset Changes

```bash
git restore --staged <file>      # Unstage a staged file

git reset <commit_id>            # Reset to a specific commit (soft by default)
git reset --hard <commit_id>     # Hard reset (discard all changes)
git reset --soft <commit_id>     # Soft reset (keep changes in working dir)

git revert <commit_id> -m 1      # Revert a merge commit
git revert <commit_id>           # Revert a specific commit
git revert head~1                # Revert last commit
git revert head~3..head~0        # Revert range of commits
git revert --no-commit head~3    # Revert without auto-commit
git revert abort                 # Abort revert process
git revert continue              # Continue revert after conflict
```

---

## 🕓 Reflog & Checkout History

```bash
git reflog                       # Show history of HEAD and branch references
git checkout <reflog_id>         # Restore using reflog ID
git checkout head                # Checkout last commit
git checkout head~1              # Checkout previous commit
```

---

## 🍒 Cherry Pick a Commit

```bash
git cherry-pick <commit_id>      # Apply changes from another commit to current branch
```

---

## 🔎 Git Ignore & Remove from Staging

```bash
git rm --cached <filename>       # Remove a file from staging but keep it in the working directory
git rm --cached -r <folder>      # Remove a folder from staging but not delete locally
```

---

## 🔀 Merging Changes

```bash
git merge <branch_name>          # Merge specified branch into current branch
```

---

## 📤 Pull Request

> Pull requests are usually created via GitHub, GitLab, or Bitbucket interfaces.  
> You can push your branch and open a PR from the repository website.

---

## ✅ Final Notes

This cheat sheet will evolve as we learn more.  
Feel free to fork and contribute if you want to add advanced commands or use-cases.

---
