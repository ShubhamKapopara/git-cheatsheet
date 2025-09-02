Git & GitHub Cheat Sheet
1. Basic Git Commands

git init – Initialize a new repository.

git clone – Clone a repository.

git add – Stage changes.

git add . – Stage all changes.

git status – Show working directory status.

git commit -m "message" – Commit changes.

git commit --amend – Modify the last commit.

git log – Show commit history.

git diff – Show changes.

git diff --staged – Show staged changes.

2. Branching & Merging

git branch – List branches.

git branch – Create a new branch.

git checkout – Switch to branch.

git checkout -b – Create and switch.

git merge – Merge branch into current.

git rebase – Reapply commits.

git cherry-pick – Apply specific commit.

git stash – Temporarily save changes.

git stash pop – Apply stashed changes.

3. Remote Repositories

git remote add origin – Add remote repo.

git remote -v – View remotes.

git push origin – Push to remote.

git push -u origin – Push and set upstream.

git fetch – Download changes.

git pull – Fetch and merge.

git remote remove – Remove a remote.

4. Undoing & Resetting

git reset – Unstage a file.

git reset --hard – Discard all changes.

git checkout -- – Discard file changes.

git revert – Create a commit to undo.

5. Tagging

git tag – List tags.

git tag – Create tag.

git push origin – Push tag.

6. GitHub Actions (CI/CD)

.github/workflows/ – Directory for workflows.

workflow.yml – Define CI/CD steps.

name: – Workflow name.

on: – Events that trigger workflow (push, pull_request, schedule).

jobs: – Group of tasks to execute.

runs-on: – OS to run on (ubuntu-latest, windows-latest).

steps: – Series of tasks.

Example:

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
7. Useful Shortcuts

git log --oneline – Compact log.

git log --graph --oneline --decorate – Visualize branches.

git shortlog -s -n – Commit count per author.

git clean -fd – Remove untracked files.

git blame – Show who changed what.

8. Collaboration Workflow

Fork the repository.

Clone your fork.

Create a feature branch.

Commit changes.

Push to your fork.

Open a Pull Request.
