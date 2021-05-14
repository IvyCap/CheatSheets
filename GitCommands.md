## Git Commands

### Cloning, Pulling, Pushing, and Fetching branches and commits  
**git clone <*Source*>**  
* Copy/download repo or branch to local machine.
    * Use **git clone https://address.com/reponame**  https clone
    * Use **git clone git@github.com:IvyCap/test-repo.git** SSH clone

**git pull**
* Pulls down latest version of remote repo and merges changes into local repo.

**git fetch http://address.com/reponame**
* Downloads latest version of the remote repo without merging the changes.

**git push <_destination_>**
* Add changes from Committed to destination repo
    * Use **git push origin** to push to original source of cloned repo
    * Use **git push origin <*TagName*>** to push a tag
    * Use **git push --set-upstream origin <*branchName*>** Creates and pushes branch to remote repo

### Changing, and Setting Stages, and Commits  
**git add <*Source*>**
* Add changes from Unstaged to Staged
    * Use **git add .** to add all files in directory
    * Use **git add fileName** to add a specific file  

**git commit -m "message"**
* Add changes from Staged to Committed

**git checkout**
* To revert changes(*Move Head*) to a specific commit.
    * Use **git history** to get UUID for commit
    * User **git checkout <*UUID*>** to revert to a specific commit
    * Use **git checkout master** to revert to the master commit
    * Use **git checkout tags/<*TagName*>** to check out a tags
    * Use **git checkout <*branchName*>** to move to a branch
    * Use **git checkout -b <*branchName*>** to create new branch and move to it.

**git reset**
* Rest unstaged changes if they have not been Committed

### Branches and Stashes

**git branch**
* List branches.
     * Use **git branch <*branchName*>** Create new branch. Does not move you to the new branch.
     * Use **git branch -d <*branchName*>** to delete a branch
**git stash**
* Creates a new stash and reverts to the most resent commits
    * Use **git stash save "StashName"** will save a stash under a name
    * Use **git stash list** to list stashes
    * Use **git stash pop** to restore the changes from the most recent stash

**git diff <*Branch1*> <*Branch2*>**
* Check differences between two branches.

**git merge <*SourceBranch*>**
* Merges specified branch in to currently located branch.
    * Use **git merge --abort** to abort a conflicting merge

**git rebase <*SourceBranch*>**
* Rebase(merge) current branch with SourceBranch

### Tags
**-creates name for specific commits. Use instead of UUIDs.**

**git tag**
* List all tags

**git tag -a <*TagName*> -m "Update note"**
* add a tag with a name and message

### Set User Email and  Name
**git config --global user.email "you@example.com"**
* Set global user email

**git config --local user.email "you@example.com"**
* Set local repo user email

**git config --global user.name "Your Name"**
* Set global user name

**git config --local user.name "Your Name"**
* Set local repo user name


### Status and History
**git status**
* Show current status of local repo

**git log**
* Show history of reponame
    * Use **git log --oneline** for compact version
    * Use **git log --graph** Show commits as a graph
    * Use **git log --graph --oneline** Show commits as a compact graph




### Stages
* **Unstaged** - made changes that may not be kept
* **Staged** - Made changes that you are sure you want to keep
* **Committed** - Defiantly want to keep changes
* **Pushed** -
