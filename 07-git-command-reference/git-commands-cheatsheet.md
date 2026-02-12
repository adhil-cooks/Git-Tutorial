# 📘 Git Command Reference

---

## 🔹 Repository Setup

### Initialize a Repository
```bash
git init
```

### Clone a Repository
```bash
git clone https://github.com/username/repository.git
```

---

## 🔹 Checking Project State

### Check Status
```bash
git status
```

### View Commit History
```bash
git log
git log --oneline
```

---

## 🔹 Staging Changes

### Stage Specific File
```bash
git add file.txt
```

### Stage All Changes (Recommended)
```bash
git add -A
```

### Stage Current Directory
```bash
git add .
```

⚠️ Avoid `git add *` (can skip files depending on shell).

---

## 🔹 Committing Changes

```bash
git commit -m "commit message"
```

---

## 🔹 Viewing Differences

### Compare Working Directory with Last Commit
```bash
git diff
```

### Compare Two Commits
```bash
git diff commit1 commit2
```

Shows changes required to transform commit1 → commit2.

---

## 🔹 Branching

### List Branches
```bash
git branch
```

### Create Branch
```bash
git branch development
```

### Create & Switch Branch (Preferred)
```bash
git checkout -b development
```

### Switch Branch
```bash
git checkout development
```

---

## 🔹 Merging Branches

### Merge into Current Branch
```bash
git merge development
```

Example:
```bash
git checkout main
git merge development
git push origin main
```

### Delete Branch After Merge
```bash
git branch -d development
```

---

## 🔹 Resolving Merge Conflicts

1. Open conflicted file  
2. Edit manually  
3. Remove conflict markers  
4. Stage file:

```bash
git add file.txt
```

5. Complete merge:

```bash
git commit
```

---

## 🔹 Remote Operations

### Push
```bash
git push
```

### Push Specific Branch
```bash
git push origin main
```

### Fetch (Download Without Merging)
```bash
git fetch
```

### Pull (Fetch + Merge)
```bash
git pull
```

---

## 🔹 Undoing Local Changes

### Unstage Files (Keep Changes)
```bash
git restore --staged file.txt
git restore --staged .
```

### Discard Unstaged Changes
```bash
git restore file.txt
git restore .
```

---

## 🔹 Reset (Use Carefully)

### Undo Last Commit (Keep Changes Staged)
```bash
git reset --soft HEAD~1
```

### Undo Last Commit (Keep Changes Unstaged)
```bash
git reset --mixed HEAD~1
```

### ⚠️ Hard Reset (Dangerous)
```bash
git reset --hard HEAD~1
```

Deletes commits and local changes permanently.

---

## 🔹 Removing Files

### Remove File & Stage Deletion
```bash
git rm file.txt
```

### Force Remove
```bash
git rm -f file.txt
```

### Remove Folder Recursively
```bash
git rm -r folder-name
```

### Stop Tracking File (Keep Locally)
```bash
git rm --cached file.txt
```

Removes from Git tracking but keeps file locally.

---

## 🔹 Stashing Work

### Save Work Temporarily
```bash
git stash
```

### List Stashes
```bash
git stash list
```

### Apply Latest Stash
```bash
git stash pop
```

### Apply Without Removing
```bash
git stash apply
```

### Drop Specific Stash
```bash
git stash drop stash@{0}
```

### Clear All Stashes
```bash
git stash clear
```

---

## 🔹 Reverting Commits (Safe for Shared Branches)

### Revert Specific Commit
```bash
git revert <commit-id>
```

Creates a new commit that reverses changes.
Does NOT rewrite history.

---

## 🔹 Rebase (Advanced – Use Carefully)

```bash
git checkout feature-branch
git rebase main
```

- Replays your branch commits on top of latest main
- Creates linear history
- Rewrites commit history
- Avoid on shared branches

---

## 🔹 Checking Out Old Commits (Detached HEAD)

```bash
git checkout <commit-id>
```

⚠️ This creates a detached HEAD state.

To continue working from there:

```bash
git checkout -b new-branch-name
```
