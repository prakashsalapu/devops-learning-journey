# 03. Git Init Lifecycle (6 Stages of Git)

### 1. Init repo
```
git init # Starts tracking your project with Git
```
### 2. Add remote origin (link local → GitHub repo)
```
git remote add origin https://github.com/<user>/<repo>.git
git remote -v

#Example: 

git remote add origin https://github.com/prakashsalapu/100-days-of-devops.git 
git remote -v 

#output
origin  https://github.com/prakashsalapu/100-days-of-devops.git (fetch)
origin  https://github.com/prakashsalapu/100-days-of-devops.git (push)
```
### 3. Set main as default branch
```
git branch -M main
```

### 4. Stage files
```
git add .
```

### 5. Commit snapshot
```
git commit -m "initial commit"
```
### 6. Push with upstream 
```
git push -u origin main
```


#### -u = upstream
```
🔎 Upstream? Links your local main to origin/main. Next time, just git push or git pull.
```