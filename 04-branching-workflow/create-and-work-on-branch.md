# Create and Work on a Branch

How to create and work on a feature branch in a team project.

---

## 1️⃣ Create a New Branch

```bash
git checkout -b feature-name
```
Creates a new branch and switches to it in one command.

Alternative method:
```bash
git branch feature-name
git checkout feature-name
```
Create the branch first, then switch to it.

---

## 2️⃣ Verify Current Branch

```bash
git branch
```
Shows all branches. The current branch is marked with an asterisk (*).

---

## 3️⃣ Work and Commit Normally

```bash
git status
git add .
git commit -m "message"
```
Work on your changes, stage them, and commit as usual. All commits go to your current branch.

---

## 4️⃣ Push Branch to GitHub

```bash
git push -u origin feature-name
```
Pushes your branch to GitHub and sets up tracking. After this, you can use `git push` without specifying the remote and branch name.
