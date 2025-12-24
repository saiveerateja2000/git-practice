# 📘 Git Commands – Beginner to Advanced

This repository contains a **complete Git command reference**, structured from **beginner to expert level**, with clear explanations and real-world usage. It is designed for **Developers, DevOps Engineers, SREs**, and anyone preparing for **interviews or daily Git usage**.

---

## 🟢 Beginner Level (Git Basics)

### 1. `git config`

Configure Git user information.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@email.com"
git config --list
```

**Usage:** Initial Git setup or switching machines.

---

### 2. `git init`

Initialize a new Git repository.

```bash
git init
```

**Usage:** Start tracking a new project.

---

### 3. `git clone`

Clone a remote repository.

```bash
git clone https://github.com/user/repo.git
```

**Usage:** Copy existing project to local system.

---

### 4. `git status`

Check repository status.

```bash
git status
```

**Usage:** Shows modified, staged, and untracked files.

---

### 5. `git add`

Stage changes.

```bash
git add file.txt
git add .
```

**Usage:** Prepare files for commit.

---

### 6. `git commit`

Commit staged changes.

```bash
git commit -m "Initial commit"
```

**Usage:** Save work to local repository.

---

### 7. `git log`

View commit history.

```bash
git log
git log --oneline
```

**Usage:** Track changes over time.

---

### 8. `git diff`

Show differences.

```bash
git diff
git diff --staged
```

**Usage:** Review code changes before commit.

---

## 🟡 Intermediate Level (Branching & Collaboration)

### 9. `git branch`

Manage branches.

```bash
git branch
git branch feature-login
git branch -d feature-login
```

**Usage:** Feature-based development.

---

### 10. `git checkout` / `git switch`

Switch branches.

```bash
git checkout dev
git switch main
```

**Usage:** Move between branches.

---

### 11. `git merge`

Merge branches.

```bash
git merge feature-login
```

**Usage:** Combine feature into main branch.

---

### 12. `git pull`

Fetch and merge remote changes.

```bash
git pull origin main
```

**Usage:** Sync local repo with remote.

---

### 13. `git push`

Push commits to remote repository.

```bash
git push origin dev
git push -u origin feature-login
```

**Usage:** Share changes with team.

---

### 14. `git remote`

Manage remotes.

```bash
git remote -v
git remote add origin <URL>
```

**Usage:** Handle multiple remotes.

---

### 15. `git fetch`

Fetch remote changes without merging.

```bash
git fetch origin
```

**Usage:** Inspect changes before merging.

---

## 🟠 Advanced Level (Power Git Usage)

### 16. `git rebase`

Reapply commits on top of another branch.

```bash
git rebase main
```

**Usage:** Maintain clean commit history.

---

### 17. `git cherry-pick`

Apply a specific commit.

```bash
git cherry-pick <commit-hash>
```

**Usage:** Apply hotfixes selectively.

---

### 18. `git reset`

Undo commits.

```bash
git reset --soft HEAD~1
git reset --hard HEAD~1
```

**Usage:** Rewrite commit history (use carefully).

---

### 19. `git revert`

Create a new commit that undoes changes.

```bash
git revert <commit-hash>
```

**Usage:** Safe rollback in production.

---

### 20. `git stash`

Temporarily save changes.

```bash
git stash
git stash pop
git stash list
```

**Usage:** Switch context without committing.

---

### 21. `git reflog`

View reference logs.

```bash
git reflog
```

**Usage:** Recover lost commits.

---

### 22. `git blame`

Show author of each line.

```bash
git blame file.txt
```

**Usage:** Debug issues and track ownership.

---

### 23. `git tag`

Tag releases.

```bash
git tag v1.0
git push origin v1.0
```

**Usage:** Versioning and releases.

---

## 🔴 Expert Level (DevOps / SRE)

### 24. `git bisect`

Find faulty commit.

```bash
git bisect start
git bisect bad
git bisect good v1.0
```

**Usage:** Debug regressions efficiently.

---

### 25. `git worktree`

Multiple working directories.

```bash
git worktree add ../hotfix main
```

**Usage:** Parallel development.

---

### 26. `git submodule`

Manage nested repositories.

```bash
git submodule add <repo-url>
```

**Usage:** Shared libraries or mono-repos.

---

## 📌 Important Git Concepts

* Working Tree vs Staging Area vs Repository
* Merge vs Rebase
* Reset vs Revert
* Fast-forward vs 3-way merge
* Detached HEAD
* `.gitignore`

---

## 🔥 Common DevOps Git Workflow

```bash
git pull origin dev
git checkout -b feature-x
git add .
git commit -m "Implement feature x"
git push -u origin feature-x
```

---

## 📚 Who Is This For?

* Beginners learning Git
* DevOps / SRE engineers
* Interview preparation
* Daily Git reference

---

⭐ If you find this useful, consider starring the repository!
