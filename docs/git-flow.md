# Git Flow Workflow

Git Flow is a branching convention, not a tool. Everything here uses plain git — no package required, no deprecation risk.

---

## Branch Structure

| Branch | Purpose |
|---|---|
| `main` | Production-ready code |
| `develop` | Integration branch — base for all features |
| `feature/name` | New features, branched from `develop` |
| `release/0.0.0` | Release prep, branched from `develop` |
| `hotfix/name` | Urgent production fixes, branched from `main` |

---

## Initial Setup

```bash
git checkout main
git checkout -b develop
git push -u origin develop
```

---

## Feature Branch

```bash
# Start
git checkout develop
git checkout -b feature/FeatureName

# Finish
git checkout develop
git merge --no-ff feature/FeatureName
git branch -d feature/FeatureName
git push origin develop
```

---

## Release Branch

```bash
# Start
git checkout develop
git checkout -b release/0.1.0

# Finish — merge into both main and develop
git checkout main
git merge --no-ff release/0.1.0
git tag -a 0.1.0 -m "Release 0.1.0"

git checkout develop
git merge --no-ff release/0.1.0

git branch -d release/0.1.0
git push origin main develop --tags
```

---

## Hotfix Branch

```bash
# Start — branches from main, not develop
git checkout main
git checkout -b hotfix/FixName

# Finish — merge into both main and develop
git checkout main
git merge --no-ff hotfix/FixName
git tag -a 0.1.1 -m "Hotfix 0.1.1"

git checkout develop
git merge --no-ff hotfix/FixName

git branch -d hotfix/FixName
git push origin main develop --tags
```

---

## Why `--no-ff`

`--no-ff` forces a merge commit even when a fast-forward is possible. This preserves the fact that a feature branch existed in history, making it easy to see exactly what was grouped together and when it landed.
