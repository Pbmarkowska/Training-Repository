## Git is a version control system (VCS)
### Basic commands
```git init``` - initialize empty repository <br>
```git status``` - check untracked changes and changes staged for a commit <br>
```git diff filename.txt``` - check changes between current file state and the state added to the staging area <br>
```git commit -m "Commit message"``` - commit the changes <br>
```git log``` - history of commits
```git show HEAD``` - shows the latest commit
```git checkout HEAD filename.txt``` - restores the file before the latest commit <br>
```git reset HEAD filename.txt``` - removes changes to the file from the staging area and restores the file to the latest commit before. <br>
```git reset commit_SHA``` - restores the file to the chosen commit using 7 characters of commit's SHA.
### Branching commands
```git branch``` - which branch I am now? <br>
```git branch newbranch``` - create a new branch, can't contain whitespaces, but ```-``` and ```_``` can <br>
```git checkout branchname``` - switch to different branch <br>
```git merge branchname``` - merge branchname into master <br>

Merge is successful if master hadn't changed since we commited on different branch. If it had changed, we have 2 different versions on separate branches, so when merged, there'll be a conflict. <br>

HEAD - master version <br>
BranchName - BranchName version

After merging BranchName into master we no longer need it. We can delete it with: <br>
```git branch -d branchname```

### Basic git workflow
  1. Working Directory - make changes to files
  2. Staging Area - files added here are ready for commit
  3. Repository -  changes saved in a repo as a commit

### Git Teamwork
```git clone remotelocation remotename``` - clone remote repo to your local env <br>
```git remote -v``` - list Git's project remotes <br>
```git fetch``` - check if there were changes to the remote repo. This will not merge the changes from remote to local, it will bring changes to *remote branch* <br>
```git merge origin/master``` - this will merge remote's branch in sync with your local branch <br>

#### Remote workflow: <br>
  1. Fetch and merge changes from the remote
  2. Create a branch to work on a new project feature
  3. Develop the feature on your branch and commit your work
  4. Fetch and merge from the remote again (in case new commits were made while you were working)
  5. Push your branch up to the remote for review

#### Generalizations again: <br>
```git clone```: Creates a local copy of a remote. <br>
```git remote -v```: Lists a Git project's remotes. <br>
```git fetch```: Fetches work from the remote into the local copy. <br>
```git merge origin/master```: Merges origin/master into your local branch. <br>
```git push origin <branch_name>```: Pushes a local branch to the origin remote. <br>
