# Create and Connect to a GitHub Repository

## Step 1: Create Repository on GitHub
Go to GitHub and create a new repository. Do not initialize it with a README, .gitignore, or license if you already have a local project.

## Step 2: Add Remote
Connect your local repository to the GitHub repository:

```bash
git remote add origin <repo-url>
```

Replace `<repo-url>` with your GitHub repository URL (HTTPS or SSH).

## Step 3: Rename Branch to main (if needed)
If your local branch is named `master` or something else, rename it to `main`:

```bash
git branch -M main
```

## Step 4: Push First Time
Push your local commits to GitHub for the first time:

```bash
git push -u origin main
```

## What -u Does
The `-u` flag sets up tracking between your local `main` branch and the remote `origin/main` branch. After this, you can use `git push` and `git pull` without specifying the remote and branch names.

## Alternative: If Cloning Instead
If you're starting fresh and want to clone an existing repository:

```bash
git clone <repo-url>
```

This creates a local copy of the repository and automatically sets up the remote connection.
