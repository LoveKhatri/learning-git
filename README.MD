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