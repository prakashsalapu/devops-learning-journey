# 05. Git Pull & Undoing Git Changes

## 01-Git PULL (Bring Remote Changes Locally)
#### Default (merge)
```
git pull origin main
```
 - Fetches & merges remote changes into your current branch (may create a merge commit).

#### Cleaner history (rebase)
```
git pull --rebase origin main
```
 - Replays your commits on top of the updated remote branch (no merge commit).
```
⚠️ Prefer --rebase for solo work; in teams, follow the repo’s policy.
```

## 02-Undoing Git Changes - 3 Common Cases
### Case 1: Staged Change - added but not commited
```
git restore --stage <file>     # unstage (keeps changes in working dir)

# older style: 
git reset <file>
git reset  # for all files
```
### Case 2: For last commit (One commit)
```
git reset HEAD-1
```

### Case 3: Undo multiple commits
- #### Safe (keeps history):
```
git revert <commitSHA>      # creates a new commit that undoes that commit

#old style :
git reset commit-hash
	#use git.log for commit-hashes 
	
	#Example : git reset 82e52219bb7a6642475a132c3ca18e0135315630 (origin/f1)
```  
 - #### Hard reset (dangerous, rewrites history):
```
git reset --hard <commitSHA>

#old style:
git reset --hard commit-hash #to delete changes in code also.
```
- 🔥 Warning: Avoid --hard on shared branches. Use revert instead.

