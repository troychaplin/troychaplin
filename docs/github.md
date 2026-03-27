# Git Commands

## Repository Setup

**Initialize and connect a local repository**
```bash
git init
git branch -m main
git add .
git commit -m "Initial commit"
git remote add origin <RemoteURL>
git remote -v
git push origin main
```

**Duplicate a repo (full history, no origin link)**
```bash
git clone --bare https://github.com/you/old-repo.git
cd old-repo.git
git push --mirror https://github.com/you/new-repo.git
cd ..
rm -rf old-repo.git
```

---

## Daily Workflow

- `git status` — show status of current branch and working directory
- `git add .` — stage all changes
- `git add <file>` — stage a specific file
- `git commit -m "message"` — commit staged changes
- `git push` — push commits to remote branch
- `git pull` — fetch and merge remote changes into current branch
- `git fetch` — fetch remote changes without merging
- `git stash` — stash tracked changes
- `git stash -u` — stash including untracked files
- `git stash pop` — apply most recent stash and remove it
- `git stash list` — list all stashes
- `git log --oneline` — compact commit history
- `git diff` — show unstaged changes
- `git diff --staged` — show staged changes

---

## Branching

**Viewing branches**
- `git branch` — list local branches
- `git branch -r` — list remote branches
- `git branch -a` — list all local and remote branches

**Creating and switching**
- `git checkout -b BranchName` — create and switch to new branch
- `git checkout BranchName` — switch to existing branch
- `git switch BranchName` — modern alternative to checkout
- `git branch -m NewName` — rename current branch
- `git branch -m OldName NewName` — rename any branch
- `git push -u origin BranchName` — push branch to remote and set upstream tracking

**Merging**
- `git checkout BranchToMergeInto` — switch to target branch
- `git merge BranchName` — merge specified branch into current branch
- `git merge --no-ff BranchName` — merge with a merge commit (preserves branch history)
- `git rebase BranchName` — rebase current branch onto another

**Deleting**
- `git branch -d BranchName` — delete local branch (merged only)
- `git branch -D BranchName` — force delete local unmerged branch
- `git push origin --delete BranchName` — delete remote branch

**Cleanup**
- `git remote update origin --prune` — remove remote tracking refs for deleted branches
- `find . -name ".DS_Store" -delete` — remove macOS junk files

---

## Tags

- `git tag` — list all tags
- `git tag 0.0.0` — create a lightweight tag at current commit
- `git tag -a 0.0.0 -m "message"` — create an annotated tag
- `git tag -a 0.0.0 <commitHash>` — tag a specific past commit
- `git push origin --tags` — push all tags to remote
- `git push origin 0.0.0` — push a specific tag
- `git tag -d 0.0.0` — delete a local tag
- `git push origin --delete 0.0.0` — delete a remote tag

---

## Remote Management

- `git remote -v` — list all remotes with URLs
- `git remote add origin <URL>` — add a remote
- `git remote set-url origin <URL>` — update remote URL (e.g. after a rename)
- `git remote remove origin` — remove a remote
- `git remote update origin --prune` — sync remote tracking branches, remove deleted ones
