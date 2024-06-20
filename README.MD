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