# Daily Git Workflow

Essential commands for normal day-to-day development work.

---

## 1️⃣ Before Starting Work (Sync First)

### Pull latest changes
```bash
git pull
```
Download and merge the latest changes from the remote repository.

### Check status
```bash
git status
```
See what changes have been made in your working directory.

---

## 2️⃣ After Making Changes (Save Your Work)

### Stage Changes
```bash
git add .
```

Variations:
```bash
git add file.txt
```
Stage a specific file.

```bash
git add -A
```
Stage every single change across the entire project.

```bash
git add *.txt
```
Stage all txt files in the current directory.

---

### Unstage If Needed
```bash
git reset
```
Remove everything from staging area and return to working directory.

---

### Commit Changes
```bash
git commit -m "clear commit message"
```
Write clear, descriptive commit messages that explain what changed and why.

---

## 3️⃣ Push Your Work

```bash
git push origin main
```
Send your local commits to the remote repository.

---

## 4️⃣ Inspect Changes

### See differences
```bash
git diff
```

Compare between commits:
```bash
git diff <newer-id> <older-id>
```
Shows added and removed lines between two commits.

---

### View Commit History
```bash
git log
```

```bash
git log --oneline
```
Shows a clean summary with shorter commit IDs.

---

## 5️⃣ Managing Files

```bash
git rm file.txt
```
Delete a file and stage the deletion.

```bash
git rm -f file.txt
```
Force remove a file even if it has uncommitted modifications.

```bash
git rm --cached file.txt
```
Stop tracking a file but keep it in your working directory.

```bash
git rm -r folder-name
```
Recursively delete a folder and all subfolders.

---

## 6️⃣ Temporarily Save Work (Stash)

```bash
git stash
```
Save your current changes temporarily.

```bash
git stash pop
```
Apply the most recent stash and remove it from the stash list.

```bash
git stash list
```
List all stashed changes.

```bash
git stash apply
```
Apply the most recent stash without removing it from the list.

```bash
git stash drop
```
Remove the most recent stash from the list.

```bash
git stash clear
```
Remove all stashed changes.

---

# 🚫 Not Included Here

- Branch creation
- Merge workflow
- Rebase
- Revert
- Removing .env from history
