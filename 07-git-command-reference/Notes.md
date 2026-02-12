### Initializing a Repository
`git init` 

### Cloning a Repository
`git clone https://github.com/user_name/repo_name.git`

### git status Tracking Changes
`git status` -show what changes have been made in our working directory

### git add Variations (., -A, specific files)
`git add . ` - stage the changes within the current directory you're in and everything within it
`git add file.txt` -specific file
`git add -A or git add --all` -stage every single change across the entire project
`git add * ` stages all visible changes except for deleted files
`git add *.txt ` stage all txt files in the current direc excluding deleted ones

### git reset Unstaging Files
`git reset` -remove everything from staging area & return to working directory

### git commit Saving Changes Permanently
`git commit -m "commit message"`

### git reset HEAD Undoing Last Commit
`git reset HEAD~` -undo the last commit and bring to the working directory

### git rm Deleting Files
`git rm four.txt`-to delete a file and stage at same time

`git reset --hard`-restore both the changes and deleted files

`git rm -f four.txt` - to force remove a file even though it is not commited.(without committing the modified file can't delete with git rm )

`git rm --cached` Stop Tracking Files - only remove it from staging area but keeps in working directory

`git rm -r <FOLDER>` -r means recursive . delete the folder and sub folder recursively

`git log` Viewing Commit History . long random string = commit id. 
`git log --oneline` - show clean & summary of log. commit id more shorter

### Git Branching Explained
`git branch` - show list of all branch
`git branch development` - create a new branch

### git checkout Switching Branches
`git checkout development` - to switch to that branch

### git merge Combining Branches
Sync your branch development with latest main (main to development). 
`git checkout development`
`git merge main -m "merging main into development"` -m means message it is optional . now main branch will appear in development branch.
then switch to the branch you want to merge into
`git checkout main`
`git merge development -m "merging on main with development"` now development branch will appear in main branch.
then push the changes to the remote repository
`git push origin main`
then delete the branch
`git branch -d development`

### Resolving Merge Conflicts
solve manually by editing the files and then commit the changes.

### Checking Out Previous Commits (Time Travel)
`git checkout <commit-id>` - checkout to the commit id. before doing this, make sure to save the changes you made in the current branch.

### git diff Comparing Commits
`git diff <commit-id1> <commit-id2>` - compare the changes between two commits. show the added and removed lines. we put most recent id first and then the older id. then is pov from newer commit to older commit.


### Understanding Push, Fetch, and Pull
`git push` - send local changes to the remote repository.
`git fetch` - bringing remote changes into your local repository, but not merging them yet. 
`git pull` - fetching + merging remote changes into your local repository. git pull = git fetch + git merge.

### git push Uploading to GitHub
`git push origin main` - push the changes to the remote repository. origin is the remote repository name. main is the branch name.
`git push origin development` - create a new branch in the remote repository and push the changes to it.

### git fetch vs. git pull
`git fetch` - fetch the changes from the remote repository. then run `git merge` to merge the changes into your current branch.
`git pull` - fetch and merge the changes from the remote repository.

### git restore Discarding Local Changes
`git restore <file/directory>` - restore the file or directory to the latest commit. if not staged.
`git restore .` - restore all files and directories to the latest commit.if not staged.
`git restore --staged <file/directory>` - restore the file or directory from the staging area to the working directory.if staged.
`git restore --staged .` - restore all files and directories from the staging area to the working directory.if staged.

### git stash Saving Unfinished Work. temporarily set aside your unfinished work, switch to another branch to do something.
`git stash` - save the changes you made in the current branch.
`git stash pop` - apply the changes you saved in the stash and remove it from the stash. the changes are applied to the current branch. pop restore most recently stashed changes.
`git stash list` - list all stashed changes.
`git stash apply` - apply the changes you saved in the stash. reapply without removing from stash. if not specified, it applies the most recently stashed changes.
`git stash apply <stash-name>` - apply the changes you saved in the stash.
`git stash drop <stash-name>` - remove the changes you saved in the stash. if not specified, it removes the most recently stashed changes.


### git revert Undoing Commits Safely
`git revert ` - used to undo the changes made in a previous commit, but instead of deleting that old commit it creates a new one that reverses those changes.
`git revert <commit-id>` - revert the changes made in the commit.


### git rebase Cleaning Up History
`git rebase <branch-name>` - rebase the branch to the latest commit. all the new commits from main branch will be applied to the branch you are on. then all your feature branch commits will be reapplied to the main branch.similar to merge but it is more linear and cleaner . need to be in branch you are rebasing to. for example `git rebase main` to rebase the branch you are on to the latest commit of main branch on to the feature branch you are on. use carefull with rebase as it can be dangerous if not done correctly because it will rewrite the history of the branch you are rebasing to. safe on local and personal .

### Pull Requests (PR) & Collaboration
in github, create a pull request. i've mdade some changes in my branch; please review them, and if everything looks good, merge them into the main branch. you can't directly merge your changes into the main branch. you need to create a pull request.

### important commands to remember:
`git add .` - stage all changes in the current directory.
`git commit -m "commit message"` - commit the changes with a message.
`git push origin main` - push the changes to the remote repository.
`git fetch` - fetch the changes from the remote repository.
`git pull` - fetch and merge the changes from the remote repository.
`git stash` - save the changes you made in the current branch.
`git stash pop` - apply the changes you saved in the stash and remove it from the stash.
`git stash list` - list all stashed changes.
`git stash drop` - remove the changes you saved in the stash.
`git stash clear` - remove all stashed changes.
`git rebase <branch-name>` - rebase the branch to the latest commit. all the new commits from main branch will be applied to the branch you are on. then all your feature branch commits will be reapplied to the main branch.