### Every git project has two parts:
  1. The directories and files we create and edit
  2. The extra information that Git records about the project history stored in .git directory located in the root directory of the repository <br>

  The combination of those 2 is **repository**

What is diff? <br>
Diff is a formatted display of the differences between two sets of files.

How to compare file's current state to the changes in the staging area? <br>
```git diff -r HEAD``` <br>
flag -r means 'compare to a particular version <br>
**HEAD** is a shortcut meaning for the most recent commit <br>
**HEAD~1** can be used to identify 1 commit before the most recent, and son on <br>
```git diff -r HEAD path/to/the/file```  
```git log``` - shows commits history, the ID number is called hash (SHA) <br>

Hash is 40-character hexadecimal string. To identify the commit, 7 characters is enough. <br>
```git show commit_SHA``` - I can see specific commit <br>
```git log path``` - shows history of a specific file <br>
```git annotate file```- shows who made the latest change <br>
```git show commit_SHA1..commit_SHA2``` - changes between commits

### How does Git store the information?
Git uses a multi-level structure to store data. In simplified form, this has three key parts:
  1. Every unique version of every file. (Git calls these **blobs** because they can contain data of any kind.)
  2. Tree that tracks the names and locations of a set of files.
  3. A commit that records the author, log message, and other properties of a particular commit.

**.gitignore** file contains files that you don't want to track <br>
```git clean -n``` - shows files that are not tracked <br>
```git clean -f``` - this will delete untracked files <br>

### How to see Git's configuration? <br>
```git config --list``` - shows the settings <br>

Additional options: <br>
```--system``` - settings for every user on the computer <br>
```--global``` - settings for every project <br>
```--local``` - settings for one specific project<br>

### How to change Git's configuration? <br>
```git config --global setting.name setting.value``` <br>

Example:
```git config --global user.name user.email email_value ```

### How to undo changes I made? <br>
```git checkout -- filename```

### How to reset the file to the last version staged? <br>
```git reset HEAD filename``` <br>

### How to reset the file to the specific version? <br>
```git checkout commit_SHA filename``` <br>

### How to undo changes to many files? <br>
Good way to do it is to use directory name rather than listing all the files.
```git reset HEAD .``` <br>

Dot signalizes that you mean current directory and all the files in it. <br>
```git checkout -- .``` - brings all the files in the directory to the previous state

### Git branching
```git diff branch_1..branch_2``` - will show difference between branches <br>
```git checkout -b branch_name``` - will create a new branch and switch to it <br>
```git merge source destination``` - merging 2 branches <br>

### Create a repository
```git init repo_name``` - initialize an empty repository <br>
```git init path/to/the/existing/directory``` - convert existing directory into the repository

### Cloning existing repository
```git clone URL new_name``` <br>

When you a clone a repository, Git remembers where the original repository was. It does this by storing a **remote** in the new repository's configuration. A remote is like a browser bookmark with a name and a URL.
```git remote v``` - lists the remotes <br>
```git remote -v``` - list the remotes and URLs <br>

When you clone a repository, Git automatically creates a remote called **origin** that points to the original repository. <br>
```git remote add remote-name URL``` - add a remote <br>
```git remote rm remote-name``` - remove the remote

### How to pull changes from the remote repository? <br>
```git pull remote branch_name``` - gets everything in branch in the remote repository identified by remote and merges it into the current branch of your local repository. <br>

Example: ```git pull origin master```

### What happens if I try to pull when I have unsaved changes?
Git stops you from pulling in changes from a remote repository when doing so might overwrite things you have done locally. The fix is simple: either commit your local changes or revert them, and then try to pull again. <br>

Example: <br>
```git pull origin master``` <br>
```git checkout -- path/to/the/repo``` <br>
```git pull origin master``` <br>
### How can I push my changes to a remote repository?
```git push remote-name branch-name``` <br>

Example: <br>
```git push origin master``` <br>
### What happens if my push conflicts with someone else's work? <br>
Git does not allow you to push changes to a remote repository unless you have merged the contents of the remote repository into your own work. <br>

Example: <br>
```git push origin master```- not successful, you have to update your local branch with the changes from the remote <br>
```git pull origin master``` - merging remote's changes to the local branch <br>
```git push origin master``` - now the push is successful.
