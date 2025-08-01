# Git Commands Cheat Sheet

A beginner-friendly and categorized reference for essential Git commands with examples.

---

## Table of Contents

 [1. Installation](#1-installation)
 [2. Initializing Git Repository](#2-initializing-git-repository)
 [3. Basic File Operations](#3-basic-file-operations)
 [4. View History](#4-view-history)
 [5. Branching](#5-branching)
 [6. Remote Repositories](#6-remote-repositories)
 [7. Pull Requests (on GitHub)](#7-pull-requests-on-github)
 [8. Merge & Conflict Resolution](#8-merge--conflict-resolution)
 [9. Forking](#9-forking)
 [10. Rebasing](#10-rebasing)
 [11. Cherry-Picking](#11-cherry-picking)
 [12. Reset & Revert](#12-reset--revert)
 [13. Stashing](#13-stashing)

## 1. Installation

Install Git

```bash
sudo apt install git
```

Installs Git on Debian-based systems.

---

## 2. Initializing Git Repository

* **Initialize Git in a Project**

  ```bash
  git init
  ```

  Creates a new local Git repository in your project folder.

---

## 3. Basic File Operations

* **Check Status of Files**

  ```bash
  git status
  ```

  Shows the current state of the working directory and staging area.

* **Add Files to Staging**

  ```bash
  git add filename.txt
  ```

  Adds a file to the staging area.

* **Commit Changes**

  ```bash
  git commit -m "Initial commit"
  ```

  Records changes to the repository with a message.

* **Restore Unstaged Changes**

  ```bash
  git restore filename.txt
  ```

  Discards changes in the working directory.

---

## 4. View History

* **View Commit History**

  ```bash
  git log
  ```

  Shows the commit history.

* **View Reflog**

  ```bash
  git reflog
  ```

  Shows a log of all recent HEAD changes.

---

## 5. Branching

* **Create a Branch**

  ```bash
  git branch new-feature
  ```

  Creates a new branch.

* **Switch to Branch**

  ```bash
  git checkout new-feature
  ```

  Switches to the specified branch.

* **Create and Switch to Branch**

  ```bash
  git checkout -b new-feature
  ```

  Creates and switches to a new branch in one step.

* **List All Branches**

  ```bash
  git branch
  ```

  Lists all branches.

* **Delete Branch**

  ```bash
  git branch -d branch-name
  ```

  Deletes the specified branch.

---

## 6. Remote Repositories

* **Add Remote Origin**

  ```bash
  git remote add origin https://github.com/user/repo.git
  ```

  Adds a remote repository.

* **Push to Remote**

  ```bash
  git push -u origin main
  ```

  Pushes commits to the remote `main` branch.

* **Clone a Repo**

  ```bash
  git clone https://github.com/user/repo.git
  ```

  Clones an existing repository.

* **Fetch from Remote**

  ```bash
  git fetch
  ```

  Downloads objects and refs from another repository.

* **Pull Changes**

  ```bash
  git pull
  ```

  Fetches and merges changes from the remote.

---

## 7. Pull Requests (on GitHub)

* **Pull Request (Manual via GitHub UI)**
  Push your branch and go to GitHub → "Compare & pull request" → Submit pull request.

---

## 8. Merge & Conflict Resolution

* **Merge Branch**

  ```bash
  git merge feature-branch
  ```

  Merges a branch into the current one.

* **Resolve Conflicts**
  Open conflicted files manually → fix → stage using `git add <file>` → commit.

---

## 9. Forking

* **Fork a Repo (via GitHub UI)**
  Use GitHub’s "Fork" button → then:

  ```bash
  git clone https://github.com/your-username/forked-repo.git
  ```

---

## 10. Rebasing

* **Rebase Current Branch**

  ```bash
  git rebase main
  ```

  Moves commits on your branch to the latest `main`.

* **Interactive Rebase**

  ```bash
  git rebase -i HEAD~3
  ```

  Lets you edit, squash, or reorder the last 3 commits.

---

## 11. Cherry-Picking

* **Cherry Pick a Commit**

  ```bash
  git cherry-pick <commit-hash>
  ```

  Applies a commit from another branch.

---

## 12. Reset & Revert

* **Reset to Previous Commit**

  ```bash
  git reset --hard HEAD~1
  ```

  Removes the last commit and changes.

* **Revert a Commit**

  ```bash
  git revert <commit-hash>
  ```

  Reverts a commit without modifying history.

---

## 13. Stashing

* **Stash Current Changes**

  ```bash
  git stash
  ```

  Saves unfinished changes temporarily.

* **Apply Latest Stash**

  ```bash
  git stash apply
  ```

  Restores the latest stashed changes.

* **View Stash List**

  ```bash
  git stash list
  ```

  Shows all stashed changes.

---

💡 **Pro Tip**: Use `git config --global alias.co checkout` to create aliases for frequently used commands.

---

## Scenario-wise Git Command Questions:

## 🤝 Teamwork Examples with Git Commands

### Scenario 1: Cloning the Project

You're joining an existing project.

```bash
git clone https://github.com/org/repo.git
cd repo
```

---

### Scenario 2: Creating a Feature Branch

You're building a new feature without affecting the main code.

```bash
git checkout -b feature/login
# make changes
git add .
git commit -m "Add login form"
```

---

### Scenario 3: Pushing Your Work to Remote

Share your work with the team.

```bash
git push origin feature/login
```

---

### Scenario 4: Creating a Pull Request

Merge your feature into the `main` branch using GitHub UI.

---

### Scenario 5: Team Reviews and Approves Pull Request

Teammates give reviews, add comments, or request changes.

---

### Scenario 6: Pull Latest Changes

You want to stay updated with the latest team changes.

```bash
git checkout main
git pull origin main
```

---

### Scenario 7: Resolve Merge Conflict

Two people edited the same file.

```bash
git merge feature/login
# fix manually
git add conflicted-file.txt
git commit -m "Resolve conflict"
```

---

### Scenario 8: Rebase Instead of Merge

Clean history before pushing.

```bash
git checkout feature/login
git rebase main
```

---

### Scenario 9: Use Git Stash During Code Review

You're in the middle of something but need to switch branch.

```bash
git stash
git checkout main
# then back
git stash apply
```

---

### Scenario 10: Cherry-Pick a Hotfix

Take one specific commit from another branch.

```bash
git cherry-pick <commit-hash>
```

---

### Scenario 11: Reset a Mistake in a Shared Repo

You've pushed something wrong, need to undo.

```bash
git reset --hard HEAD~1
git push --force
```

> ⚠️ Only do this if you're **sure** others haven’t pulled the bad commit.

---

### Scenario 12: Revert a Commit Safely

Undo a bad commit without rewriting history.

```bash
git revert <commit-hash>
```

---

### Scenario 13: Review Work of Others

Check another team member’s branch.

```bash
git fetch origin
git checkout feature/teammate-branch
```

---

### Scenario 14: Track Team Activity

View who pushed what.

```bash
git log --oneline --graph --all --decorate
```

---

### Scenario 15: Fork for External Collaboration

Fork a public repo and collaborate.

```bash
# On GitHub → Click "Fork"
git clone https://github.com/your-username/forked-repo.git
```

---

## 🙌 Contributing

Have a command or section you'd like to add? Feel free to open an issue or submit a pull request.

## 📄 License

This project is licensed under the MIT License. You are free to use, modify, and distribute this guide.

## 👤 Author

Maintained by Arya Kashikar.
If you found this helpful, consider ⭐️ starring the repo!

---
