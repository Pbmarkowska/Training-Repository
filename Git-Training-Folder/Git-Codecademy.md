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
```git branch``` - which branch I am now?

### Basic git workflow
  1. Working Directory - make changes to files
  2. Staging Area - files added here are ready for commit
  3. Repository -  changes saved in a repo as a commit
