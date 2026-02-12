# Pull Request (PR) Workflow

A Pull Request is a way to propose changes and request code review before merging your branch into the main branch.

---

## 1️⃣ Create a Feature Branch

```bash
git checkout -b feature-name
```

Create a new branch for your feature or fix.

---

## 2️⃣ Work and Push the Branch

```bash
git add .
git commit -m "message"
git push -u origin feature-name
```

Make your changes, commit them, and push the branch to GitHub. This uploads your branch to the remote repository.

---

## 3️⃣ Create Pull Request on GitHub

Go to your repository on GitHub:
- Click "Compare & Pull Request" button (appears after pushing a new branch)
- Select the base branch (usually `main`)
- Select the compare branch (your `feature-name`)
- Add a description explaining your changes
- Request review from teammates

Pull Requests are created on GitHub, not through Git commands.

---

## 4️⃣ Code Review and Approval

Teammates review your code:
- They can comment on specific lines
- Request changes if improvements are needed
- Approve the PR when ready to merge

---

## 5️⃣ Merge the Pull Request

Once approved:
- Click "Merge Pull Request" on GitHub
- GitHub merges your branch into main
- Optionally delete the feature branch after merging
