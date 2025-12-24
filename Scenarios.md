# 🧪 Git Practical Scenarios (Real-World)

This document contains **real-world Git scenarios** along with **short, practical answers**. It is useful for **hands-on practice, interviews, and daily DevOps workflows**.

---

## 🟢 Scenario 1: First Day on a New Project

### Situation

You joined a team. The repository already exists.

### Tasks

* Get the code
* Check branches
* Create your own feature branch

### Tests

`clone`, `branch`, `checkout`, `status`

### Expected Concepts

* Remote repository
* Default branch (`main` / `dev`)
* Feature branching

### Answer

```bash
git clone <repo-url>
cd repo
git branch
git checkout -b feature-x
```

---

## 🟢 Scenario 2: You Modified Files but Forgot What You Changed

### Situation

You edited multiple files and want to review changes before committing.

### Tasks

* See which files changed
* See exact code changes
* Stage only one file

### Tests

`status`, `diff`, `add`

### Expected Concepts

* Working tree vs staging area
* Selective staging

### Answer

```bash
git status
git diff
git add file1
```

---

## 🟢 Scenario 3: Wrong Commit Message / Forgot a File

### Situation

You committed but the message is wrong or a file was missed.

### Tasks

* Fix the last commit without creating a new commit

### Tests

`commit --amend`, `reset --soft`

### Expected Concepts

* Amending commits
* Local history rewrite

### Answer

```bash
git add forgotten_file
git commit --amend
```

---

## 🟡 Scenario 4: Feature Branch Workflow

### Situation

You are working on `feature-login` while `dev` keeps moving.

### Tasks

* Update your branch with latest `dev`
* Keep commit history clean

### Tests

`fetch`, `rebase`, `pull`

### Expected Concepts

* Rebase vs merge
* Linear history

### Answer

```bash
git fetch origin
git rebase origin/dev
```

---

## 🟡 Scenario 5: Merge Conflict (Very Common 🔥)

### Situation

Two developers modified the same file causing a merge conflict.

### Tasks

* Identify conflicting files
* Resolve conflict
* Complete merge

### Tests

`merge`, `status`, `add`, `commit`

### Expected Concepts

* Conflict markers (`<<<<<<<`)
* Manual conflict resolution

### Answer

```bash
git merge dev
# resolve conflicts manually
git add .
git commit
```

---

## 🟡 Scenario 6: Accidentally Pushed to main

### Situation

You pushed a commit directly to `main`, violating team policy.

### Tasks

* Undo the change safely
* Keep history clean

### Tests

`revert`

### Expected Concepts

* Revert vs reset
* Production-safe rollback

### Answer

```bash
git revert <commit-id>
```

---

## 🟡 Scenario 7: Work in Progress, Urgent Hotfix

### Situation

You are mid-work but need to switch branches immediately.

### Tasks

* Save current work temporarily
* Switch branch
* Resume work later

### Tests

`stash`

### Expected Concepts

* Temporary snapshots
* Context switching

### Answer

```bash
git stash
git checkout hotfix
git stash pop
```

---

## 🟠 Scenario 8: Pick One Commit from Another Branch

### Situation

Only one commit from a feature branch is needed in `main`.

### Tasks

* Apply that commit without merging the entire branch

### Tests

`cherry-pick`

### Expected Concepts

* Commit hashes
* Selective application

### Answer

```bash
git cherry-pick <commit-id>
```

---

## 🟠 Scenario 9: “I Deleted My Commit 😱”

### Situation

You ran a reset and lost commits.

### Tasks

* Recover the lost commit

### Tests

`reflog`

### Expected Concepts

* HEAD movement
* Git safety net

### Answer

```bash
git reflog
git checkout <old-hash>
```

---

## 🟠 Scenario 10: Regression Bug in Production

### Situation

A bug appeared after a recent release. You don’t know which commit caused it.

### Tasks

* Find the faulty commit efficiently

### Tests

`bisect`

### Expected Concepts

* Binary search in Git
* Good vs bad commits

### Answer

```bash
git bisect start
git bisect bad
git bisect good v1.0
```

---

## 🔴 Scenario 11: Parallel Feature + Hotfix Work

### Situation

You need to continue feature work and apply an urgent hotfix simultaneously.

### Tests

`worktree`

### Expected Concepts

* Multiple working directories
* Clean parallel workflows

### Answer

```bash
git worktree add ../hotfix main
```

---

## 🔴 Scenario 12: Release Management

### Situation

Your application is ready for release.

### Tasks

* Mark the release
* Push it to remote

### Tests

`tag`

### Expected Concepts

* Versioning
* Immutable release points

### Answer

```bash
git tag v1.0
git push origin v1.0
```

---

✅ **Tip:** Practice these scenarios in a dummy repository to build real confidence.
