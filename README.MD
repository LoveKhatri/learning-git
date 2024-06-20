`.git` - Folder where all the details about git and the current repository are stored

- Untracked(U) - Files that are not being tracked by git
- Added(A) - Files that are being tracked by git and have been added to the staging area
- Unmodified(M) - Files that are being tracked by git and have not been modified
- Modified(M) - Files that are being tracked by git and have been modified
- Staged(S) - Files that are being tracked by git and have been staged

### Commands
- `git add <file/path>` - Add a file to the staging area (changing status from Untracked to Added)
- `git add .` - Add all files to the staging area

> Making changes to a file will change the status from Added to Modified

- `git rm <file/path>` - Remove a file from the staging area
- `git rm --cached <file/path>` - Remove a file from the staging area but keep it in the working directory
- `git rm -f <file/path>` - Remove a file from the staging area and the working directory (Deletes the file)

- `git commit -m "<message>"` - Commit the changes in the staging area to the repository (changing status from Added to Modified)

- `git diff` - Show the changes made to the files
- `git diff --staged` - Show the changes made to the files in the staging area
> Press `q` to exit the diff view

- `git log` - Show the commit history
- `git log --oneline` - Show the commit history in a single line
- `git log --oneline --graph` - Show the commit history in a single line with a graph

- `git show <commit>` - Show the changes made in a commit
- `git show <commit>:<file>` - Show the changes made in a file in a commit

- `git blame <file>` - Show the changes made in a file and who made them

- `git reset HEAD <file>` - Remove a file from the staging area
- `git reset --hard <commit>` - Reset the repository to a specific commit
- `git revert <commit>` - Revert the changes made in a commit (creates a new commit)


- `git remote -v` - Show the remote repositories
- `git remote add <name> <url>` - Add a remote repository
- `git remote remove <name>` - Remove a remote repository
- `git remote rename <old-name> <new-name>` - Rename a remote repository

> When we revert a commit on local machine, the remote machine HEAD is still on something else, so we push using force
- `git push origin <branch> --force` - Push the changes to the remote repository

## Branches

- `git branch` - Show the branches
- `git branch <name>` - Create a branch
- `git branch -d <name>` - Delete a branch
- `git branch -m <old-name> <new-name>` - Rename a branch
- `git checkout <branch>` - Switch to a branch
- `git checkout -b <name>` - Create a branch and switch to it
- `git merge <branch>` - Merge a branch into the current branch

- `git push --set-upstream origin <branch>` - Push the branch to the remote repository
- `git branch --set-upstream-to=origin/<branch>` - Set the upstream branch

Branch Naming Conventions/Branch Tags
- `feat/<name>` - Feature branch
- `bug/<name>` - Bug branch
- `hotfix/<name>` - Hotfix branch
- `release/<name>` - Release branch
- `wip/<name>` - Work in Progress branch

Rebase

- `git rebase <branch>` - Rebase the current branch onto another branch
- `git rebase --continue` - Continue the rebase after resolving conflicts
- `git rebase --abort` - Abort the rebase

Stash
- `git stash` - Stash the changes
- `git stash list` - Show the stashes
- `git stash apply` - Apply the last stash
- `git stash apply <stash>` - Apply a stash