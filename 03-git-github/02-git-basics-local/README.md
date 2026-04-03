# 02. Git Basics (Local Repository Workflow)

This module focuses on **working with Git on your local machine**.

No GitHub yet. Only local Git concepts.

## 📁 Repository (Repo)

A **repository** is a folder where Git tracks changes.

Once a folder becomes a Git repository, Git starts managing:
- File changes
- Versions
- History


## Initialize a Git repository

Inside your project folder, run:

```bash
git init
```
This command:
  - Creates a hidden .git folder
  - Starts tracking the project using Git

##### Check if Git is initialized

Inside the project directory:
```
ls -a        # Linux / macOS / Git Bash

#Windows CMD:

dir /a
```

If you see a .git/ folder, Git is initialized.
If not, run git init.

#### 📂 The .git folder

The .git folder contains:
 - Commit history
 - Branch information
 - Configuration
 - Staging area
   
 ⚠️ Do not delete or modify this folder manually.

#### Check repository status
```
git status
```

This command shows:
 - Current branch
 - File changes
 - Staging information

You will use git status very frequently.

#### File states in Git :

Git files exist in different states:
```
Untracked
New files that Git is not tracking yet

Modified
Tracked files that have been changed

Staged
Files added to staging area using git add

Unmodified
Files with no changes since last commit
```
##### Example workflow

Create or modify a file: 
 - Check status
```
git status
```

 - Stage the file
```
git add <file-name>
```

 - Check status again
```
git status
```

#This is the basic local Git workflow.

## Summary

In this module, you learned:
- What a Git repository is
- How to initialize a repository
- Purpose of .git folder
- How git status works
- File states in Git

#### Next module will cover adding, committing, and pushing code.