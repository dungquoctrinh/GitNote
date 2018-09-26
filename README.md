# GitNote

Basic command for git. 

# git-cheatsheet

- **git init**                         : Initialize a Git repo here
- **git status**                       : Check the current status of our project
- **git add <filename>**               : Add <filename> to the staging area
- **git add .**              : Add all untracked files to the staging area (Can be used after a merge conflict to resolve the conflict)
- **git commit -m "Message"**          : Store staged changes with a message
- **git commit -a -m "Message"** : Add changes from all "tracked" files and commit (Doesn't add new untracked files)
- **git commit --amend -m "newMessage"** : Add to the last commit all staged changes and create new commit message (Don't do after push)
- **git log**                          : See all the changes we've committed so far
- **git remote add <remoteRepoName> <RepoURL>**  : Add a remote repo
Ex: git remote add origin https://abc.com  - remote name is "origin" and remote URL is "https://abc.com"

- **git remote rm <name>** : Remove remotes
- **git remote -v** : Show remote repoes  == **git remote --verbose**
- **git remote show origin**   :
- **git remote prune origin**  :  Clean up deleted remote branches
- **git push -u <remoteRepoName> <localBranchName>: Push local changes to remote repo
Ex: git push -u origin master  :  -u tells Git to remember the params so next time, we can simply run "git push", "origin" is the name of the remote repo, "master" is the default local branch name
    git push origin localBranchName :  Link local branch to the remote branch
- **git push origin :<branchName>** : Delete remote <branchName> (local <branchName> must be deleted manually)

- **git pull** : Pull all changes from remote
            - **git fetch** : Fetch our local repo with the remote one
            - **git merge origin/master** : Merge the origin/master with master
- **git pull <remoteRepoName> <branchName>**   : Pull down any new changes
Ex: git pull origin master

- **git help**
- **git help <command>** : Get description on <command>
- **git config** : Set up git
Ex: git config --global user.name "abc"

- **git diff** : Show unstaged differences since last commit
- **git diff --staged** : View staged differences
- **git reset HEAD <fileName>**
- **git reset --soft HEAD^**: Undo last commit and put changes into staging (Now you can make changes and re-commit) (Don't do after push)
- **git reset --hard HEAD^**: Undo last commit and delete all changes (Don't do after push)
- **git reset --hard HEAD^^**: Undo last 2 commits and all changes (Don't do after push)
- **git checkout -- <fileName>** : Delete all changes since <fileName>
- **git checkout -b <branchNam>** : Create and switch to <branchName>
- **git clone <URL> <localDirname>** :
            - Download the entire repo into <localDirname>
            - Add the "origin" remote, pointing it to the clone URL
            - Check out initial branch (likely master)
- **git branch** : List all branches
- **git branch -r ** : List all remote branches
- **git branch -d <branchName> ** : Delete <branchName>, will prompt error if there are unstaged changes
- **git branch -D <branchName> ** : Delete <branchName> and all changes
- **git branch <branchName>** : Create a branch <branchName>
- **git merge <branchName>** : merge <branchName> to the current branch
