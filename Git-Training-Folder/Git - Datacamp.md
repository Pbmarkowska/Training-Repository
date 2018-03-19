### Every git project has two parts:
  1. The directories and files we create and edit
  2. The extra information that Git records about the project history stored in .git directory located in the root directory of the repository <br>

  The combination of those 2 is **repository**

What is diff? <br>
Diff is a formatted display of the differences between two sets of files.

How to compare file's current state to the changes in the staging area? <br>
```git diff -r HEAD``` <br>
flag -r means 'compare to a particular version <br>
HEAD is a shortcut meaning for the most recent commit <br>
```git diff -r HEAD path/to/the/file```<br>  
