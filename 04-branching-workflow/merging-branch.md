# Combining Branches (Merge & Rebase)

How to combine changes from different branches using merge or rebase.

---

# 🔵 PART 1 — Using MERGE (Safe & Standard)

## 1️⃣ Update Development with Latest Main

First, bring the latest changes from main into your development branch:

```bash
git checkout development
git merge main
```

This merges all commits from main into development. Git may create a merge commit if there are divergent changes. The `-m "message"` flag is optional and only used when a merge commit is created.

---

## 2️⃣ Merge Development into Main

Switch to main and merge development into it:

```bash
git checkout main
git merge development
```

This brings all changes from development into main. After this, main contains all the work from development.

---

## 3️⃣ Push Changes to Remote

```bash
git push origin main
```

Push the merged changes to the remote repository so teammates can access them.

---

## 4️⃣ Delete Development Branch (Cleanup)

Delete the local branch:

```bash
git branch -d development
```

Delete the remote branch:

```bash
git push origin --delete development
```

Clean up branches that are no longer needed after merging.

---

# 🟠 PART 2 — Using REBASE (Linear History)

Rebase replays your branch commits on top of the latest main branch, creating a linear history instead of merge commits.

## 1️⃣ Rebase Feature Branch onto Main

**Important:** You must be on the branch you want to rebase.

```bash
git checkout feature-branch
git rebase main
```

Rebase replays your feature branch commits on top of the latest main commits. This rewrites history by creating new commits. Safe for local and private branches, but dangerous on shared or public branches because it rewrites commit history that others may have based their work on.

---

## 🔎 Merge vs Rebase Summary

| Merge | Rebase |
|-------|--------|
| Keeps full history | Creates linear history |
| Safer for teams | Cleaner history |
| Does not rewrite history | Rewrites history |
