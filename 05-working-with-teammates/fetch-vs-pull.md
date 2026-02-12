# Git Fetch vs Git Pull

Understanding the difference between downloading changes and automatically merging them.

---

## 1️⃣ git fetch

```bash
git fetch
```

Downloads changes from the remote repository but does NOT modify your current branch. Updates remote-tracking branches like `origin/main`.

After fetching, merge manually:

```bash
git merge origin/main
```

This merges the fetched changes into your current branch.

---

## 2️⃣ git pull

```bash
git pull
```

Combines `git fetch` and `git merge` in one command. Automatically merges remote changes into your current branch.

---

## 3️⃣ When to Use What?

| git fetch | git pull |
|------------|------------|
| Safer | Faster |
| Review changes first | Immediate merge |
| More control | Less control |
