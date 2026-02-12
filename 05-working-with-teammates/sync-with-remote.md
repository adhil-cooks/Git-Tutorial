# Syncing with Remote Repository

How to keep your local branch synchronized with the remote repository safely.

---

## 1️⃣ Check Current Branch

```bash
git branch
```

Verify which branch you're currently on.

---

## 2️⃣ Fetch Latest Changes

```bash
git fetch
```

Downloads the latest changes from the remote repository without modifying your current branch.

---

## 3️⃣ Merge Latest Main into Current Branch

```bash
git merge origin/main
```

Merges the latest changes from the remote main branch into your current branch. This keeps your branch updated with the latest code.

---

## 4️⃣ Alternative: Quick Sync with Pull

```bash
git pull origin main
```

Combines fetch and merge in one command. Use this when you want to quickly sync without reviewing changes first.

---

## 5️⃣ Push Updated Branch

```bash
git push
```

Uploads your local commits to the remote repository.
