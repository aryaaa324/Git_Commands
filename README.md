# Git_Commands
This repository contains all the essential git commands, great for quick revisions !


##  1. Installation

- **Install Git**
  ```bash
  sudo apt install git
````

Installs Git on Debian-based systems.

---

##  2. Initializing Git Repository

* **Initialize Git in a Project**

  ```bash
  git init
  ```

  Creates a new local Git repository in your project folder.

---

##  3. Basic File Operations

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

##  4. View History

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

##  5. Branching

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

##  6. Remote Repositories

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

##  7. Pull Requests (on GitHub)

* **Pull Request (Manual via GitHub UI)**
  Push your branch and go to GitHub → "Compare & pull request" → Submit pull request.

---

##  8. Merge & Conflict Resolution

* **Merge Branch**

  ```bash
  git merge feature-branch
  ```

  Merges a branch into the current one.

* **Resolve Conflicts**
  Open conflicted files manually → fix → stage → commit.

---

##  9. Forking

* **Fork a Repo (via GitHub UI)**
  Use GitHub’s "Fork" button → then:

  ```bash
  git clone https://github.com/your-username/forked-repo.git
  ```

---

##  10. Rebasing

* **Rebase Current Branch**

  ```bash
  git rebase main
  ```

  Moves commits on your branch to the latest main branch tip.

* **Interactive Rebase**

  ```bash
  git rebase -i HEAD~3
  ```

  Lets you edit, squash, or reorder the last 3 commits.

---

##  11. Cherry-Picking

* **Cherry Pick a Commit**

  ```bash
  git cherry-pick <commit-hash>
  ```

  Applies a commit from another branch.

---

##  12. Reset & Revert

* **Reset to Previous Commit**

  ```bash
  git reset --hard HEAD~1
  ```

  Removes last commit and changes.

* **Revert a Commit**

  ```bash
  git revert <commit-hash>
  ```

  Reverts a commit without changing history.

---

##  13. Stashing

* **Stash Current Changes**

  ```bash
  git stash
  ```

  Saves unfinished changes.

* **Apply Latest Stash**

  ```bash
  git stash apply
  ```

  Restores the latest stashed changes.

* **View Stash List**

  ```bash
  git stash list
  ```
