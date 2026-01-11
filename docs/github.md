# Github Commands

## Repository Setup

**Initialize and Connect Local Repository**

```
git init
git branch -m main
git add .
git commit -m "Initial commit message"
git remote add origin <AddRemoteURL>
git remote -v
git push origin main
```

## Basic Commands

- `git status` - show status of current branch and working directory
- `git push` - push commits to remote branch
- `git pull` - pull commits from remote and merge into current branch
- `git fetch` - fetch commits from remote but do not merge into current branch

## Branching

**Viewing Branches**

- `git branch` - list all local branches
- `git branch -r` - list all remote branches
- `git branch -a` - list all local and remote branches

**Creating and Switching Branches**

- `git checkout -b BranchName` - create new branch and switch to it
- `git checkout BranchName` - switch to existing branch
- `git branch -m OldName NewName` - rename branch (use without OldName to rename current branch)
- `git push -u origin BranchName` - push local branch to remote and set upstream tracking

**Merging Branches**

- `git checkout BranchToMergeInto` - switch to target branch
- `git merge BranchName` - merge specified branch into current branch

**Deleting Branches**

- `git branch -d BranchName` - delete local branch (only if already merged)
- `git branch -D BranchName` - force delete local unmerged branch
- `git push origin --delete BranchName` - delete remote branch

**Cleanup Commands**

- `git remote update origin --prune` - prune list of branches
- `find . -name ".DS_Store" -delete` - remove files
- `git stash -u` - stash untracked files

## Tags

- `git tag 0.0.0` - create a tag at current commit
- `git push origin --tags` - push all tags to remote
- `git push origin 0.0.0` - push specific tag to remote

## Remote Management

- `git remote -v` - list all remote repositories
- `git remote add origin <URL>` - add remote repository
- `git remote update origin --prune` - update remote tracking branches and remove deleted ones

## Git Flow

- `git flow init` - initialize git flow in the repository

**Command Structure**

`git flow <branch-type> <command> <name>`

**Branch Types**

- `feature` - for new features
- `hotfix` - for urgent production fixes
- `release` - for preparing releases

**Commands**

- `start` - create and switch to a new branch
- `finish` - merge branch back to main/develop and clean up
- `publish` - push branch to remote repository
- `pull` - pull latest commits from remote branch

**Examples**

- `git flow feature start FeatureName` - create a feature branch
- `git flow feature finish FeatureName` - finalize and merge a feature
- `git flow release start 0.1.0` - create a release branch
- `git flow hotfix start 0.1.1` - create a hotfix branch