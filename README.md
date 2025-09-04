# Git & GitHub Cheat Sheet

A quick reference guide for essential Git commands, GitHub workflows, and CI/CD basics.

---

## 1. Basic Git Commands

- `git init` – Initialize a new repository  
- `git clone <repo>` – Clone a repository  
- `git add <file>` – Stage changes  
- `git add .` – Stage all changes  
- `git status` – Show working directory status  
- `git commit -m "message"` – Commit changes  
- `git commit --amend` – Modify the last commit  
- `git log` – Show commit history  
- `git diff` – Show changes  
- `git diff --staged` – Show staged changes  

---

## 2. Branching & Merging

- `git branch` – List branches  
- `git branch <branch>` – Create a new branch  
- `git checkout <branch>` – Switch to branch  
- `git checkout -b <branch>` – Create and switch  
- `git merge <branch>` – Merge branch into current  
- `git rebase <branch>` – Reapply commits  
- `git cherry-pick <commit>` – Apply specific commit  
- `git stash` – Temporarily save changes  
- `git stash pop` – Apply stashed changes  

---

## 3. Remote Repositories

- `git remote add origin <url>` – Add remote repo  
- `git remote -v` – View remotes  
- `git push origin <branch>` – Push to remote  
- `git push -u origin <branch>` – Push and set upstream  
- `git fetch` – Download changes  
- `git pull` – Fetch and merge  
- `git remote remove origin` – Remove a remote  

---

## 4. Undoing & Resetting

- `git reset <file>` – Unstage a file  
- `git reset --hard` – Discard all changes  
- `git checkout -- <file>` – Discard file changes  
- `git revert <commit>` – Create a commit to undo  

---

## 5. Tagging

- `git tag` – List tags  
- `git tag <tag>` – Create tag  
- `git push origin <tag>` – Push tag  

---

## 6. GitHub Actions (CI/CD)

- `.github/workflows/` – Directory for workflows  
- `workflow.yml` – Define CI/CD steps  
- `name:` – Workflow name  
- `on:` – Events that trigger workflow (`push`, `pull_request`, `schedule`)  
- `jobs:` – Group of tasks to execute  
- `runs-on:` – OS to run on (`ubuntu-latest`, `windows-latest`)  
- `steps:` – Series of tasks  

**Example:**

```yaml
name: CI
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '16'
      - name: Install dependencies
        run: npm install
      - name: Run tests
        run: npm test


Commit changes.

Push to your fork.

Open a Pull Request.
