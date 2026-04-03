# 06. Fork (Copy → Change → PR) & Summary

## Fork (Copy → Change → PR)
- #### What is Fork?
```
 Your own copy of someone’s repo on your GitHub.
```
- #### Workflow:
```
1. Fork the repo on GitHub (your account gets a copy).
2 Clone your fork locally.
3. Create a branch → make changes → commit & push to your fork.
4. Open a Pull Request back to the original repo.
```
- 💡 Tip: Keep your fork updated by adding the original as upstream:
```
git remote add upstream https://github.com/original/repo.git
git fetch upstream
git rebase upstream/main   # or: git merge upstream/main
```
## Summary & Recap
- #### Core loop:
```
status → add → commit → push → pull 🔁
```
- #### Most used commands:
```
git status
git add .
git commit -m "message"
git push
git pull --rebase
git switch -c <branch>   # or: checkout -b
```
- ### Best practices:
 - Small commits with clear messages.
 - Work on feature branches, not main.
 - Use PRs to review and discuss changes.
 - Avoid force-pushing shared branches.
