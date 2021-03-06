| **Command**        | **Description**  |
| ------------- |:-------------:|
| `git init`     | Initialize a local Git repository |
| `git clone <https/ssh url>`     | Create a local copy of a remote repository      |
| `git status` | Check status     |
| `git add [file_name]/.` | Add a file to the staging area or . add all files |
| `git commit -m "[commit message]"`| Commit changes |
|`git rm -r [file-name.txt]` | Remove a file (or folder) |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
|`git fetch`| Retrieves latest metadata info from original without any file transfer|
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |



### Adding an existing project to GitHub using the command line
1. git init
2. git add .
3. git commit -m ""
4. git remote add origin <remote_url>
5. git push origin master
6. git push --set-upstream origin master

### Rewriting git history

| **Case** | **Steps**|
|-----------|-----------|
|Amending Commit| 1. git log --oneline 2. git add . 3. git commit --amend --no-edit |
|Rewording Commit|1. git log --oneline 2. git rebase -i HEAD~1 3. opens up an editor window modify pick to reword then save 4. opens up window to change the text then save |
|Deleteing Commit|1. git rebase -i HEAD~2 2. opens up an editor window modify pick to drop then save  |
|Reordering Commit|1. git rebase -i HEAD~3 2. opens up an editor window just reorder the commits and save |
|Squashing Commit|1. git rebase -i HEAD~3 2. opens up an editor window just modify commits pick to squash or fixup then save|
|Splitting Commit|1. git rebase -i HEAD~4 2. opens up an editor window just modify commit pick to edit then save 3. git reset HEAD^ 4. unstage files those were commited 5. add those separetly then commit |
