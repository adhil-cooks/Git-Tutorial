# Start a New Local Project

## Step 1: Create Project Folder
Create a new folder for your project and navigate into it.

## Step 2: Initialize Git
Initialize a new Git repository:

```bash
git init
```

## Step 3: Check Status
Check the current status of your repository:

```bash
git status
```

## Step 4: Stage Files
Stage all files in the current directory:

```bash
git add .
```

To stage specific files, use `git add <filename>`.

## Step 5: First Commit
Create your first commit:

```bash
git commit -m "Initial commit"
```

## What This Does Internally
Files move from your working directory → staging area → repository. `git add` moves files to staging, `git commit` saves them permanently to the repository.
