# 04. Clone, Branch, Merge & Git Stash

This module covers how developers work on existing repositories, create branches, merge changes, and temporarily save work using git stash.


### 1. Clone a repository

Cloning means **copying an existing remote repository to your local machine**.
```
git clone <repo-url>
cd <repo-folder>

Example:

git clone https://github.com/prakashsalapu/100-days-of-devops.git

cd 100-days-of-devops

```


### 2. Check current branch


```
git branch

The branch with `*` is the current branch.

```

### 3. Create a new branch

#### Old method
```
git checkout -b feature1

```
#### New method (recommended)
```
git switch -c feature1
```
This creates a new branch and switches to it.

### 4. Switch between branches
```
git switch main


or (old method)


git checkout main
```

### 5. Make changes and commit in branch
```
git status
git add .
git commit -m "added new feature"

```
Changes are now saved inside the branch.

## 6. Merge branch into main

First switch to main branch:
```
git switch main

Then merge:

git merge feature1
```
This combines changes from `feature1` into `main`.

## 7. Delete a branch (after merge)
```
git branch -d feature1
```

## 8. Git Stash (temporary save)

Git stash is used when:
- You are working on something
- You don’t want to commit yet
- You need to switch branches quickly

#### Save changes using stash

```
git stash

```
#### View stashed changes
```
git stash list
```
#### Apply latest stash
```
git stash pop
```
This restores the changes and removes them from stash.

#### Apply stash without deleting
```
git stash apply
```

## Summary

In this module you learned:
- How to clone a repository
- How to create and switch branches
- How to merge branches
- How to temporarily save work using git stash