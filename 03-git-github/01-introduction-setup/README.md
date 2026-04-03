# 01. Introduction & Setup


## What is Git?

Git is a **Version Control System (VCS)** that helps you track changes in your project.

You can think of Git like a **time machine for your code**.  
You can move back to older versions anytime.

### Example
```
Without Git :  
- project_v1  
- project_v2  
- final_project_v3  

With Git : 
- One project folder  
- Git tracks all versions internally
```

## What is GitHub?

GitHub is a **cloud platform (remote)** used to store, share, and collaborate on Git repositories.

Simple difference:
- Git → works on your local system
- GitHub → stores code online

### Example

Save your repository on GitHub → Share it with others → They can contribute to your project.


## Why learn Git & GitHub?

- Track changes in code
- Work in teams
- Contribute to open-source projects
- Industry standard for developers and DevOps



## Installation & Setup

#### Windows
```
1. Go to: https://git-scm.com/downloads  
2. Download the Windows installer  
3. Open the `.exe` file  
4. In **PATH environment** option, select:  
   Git from the command line and also from 3rd-party software 
5. Finish installation.  
```

#### macOS (Homebrew)

```
brew install git
```

#### Linux (Ubuntu or Debian)
```
sudo apt-get update
sudo apt-get install git
```

#### Check Git installation
```
git --version
# or
git -v
```

Example output:
```
git version 2.49.0.windows.1
```

If you see a version number, Git is installed successfully.

## Git configuration (first-time setup)

📂 Repository (Repo) – A folder where Git tracks changes

#### a) Configure Username & Email (once per machine)
```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
##### Check current config:
```
git config --global --list
```
#####  💡Example:
![Git Configuration](/01-introduction-setup/images/git-config.png)


#### b) Check whether Git is initialized or not
##### Inside your project folder:
```
ls -a         # shows hidden files like .git (Git Bash/macOS/Linux)
# or (Windows CMD)
# dir /a
```
```
💡If you see a .git/ folder → Git is initialized. If not → run git init.

```
![Git Initialize](/01-introduction-setup/images/git-init.png)

##### c) git status (and its file types)
```
Untracked → New files not tracked yet (add with git add).
Modified → Tracked files changed but not staged.
Staged → Changes added to staging area (git add), ready to commit.
Unmodified → No changes since last commit.
```
##### Check status:
```
git status
```
## Summary

In this module, you learned:

  1. What Git is
  2. What GitHub is
  3. Why Git and GitHub are important
  4. How to install Git
  5. How to verify installation
  6. How to configure Git on your system

