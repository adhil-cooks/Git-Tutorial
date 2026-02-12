# Clone an Existing Repository

## Step 1: Get Repository URL
On GitHub, go to the repository page. Click the "Code" button and copy the HTTPS or SSH URL.

## Step 2: Clone the Repository
Clone the repository to your local machine:

```bash
git clone <repo-url>
```

This command downloads the entire repository, including all files, branches, and commit history.

## Step 3: Move Into Project Folder
Navigate into the cloned project folder:

```bash
cd project-name
```

Replace `project-name` with the actual name of the repository.

## Step 4: Verify Status
Check the repository status:

```bash
git status
```

After cloning, you should see "On branch main" (or the default branch) with "nothing to commit, working tree clean".

## What Clone Sets Up Automatically
When you clone a repository, Git automatically:
- Sets up `origin` as the remote repository URL
- Checks out the default branch (usually `main` or `master`)
- Downloads the complete commit history
