## Challenge Tasks

### Task 1: Install and Configure Git

# Task 1: Install and Configure Git

## 1. Check Git installation

```bash
git --version

`````
<img width="667" height="137" alt="Screenshot 2026-04-26 111124" src="https://github.com/user-attachments/assets/72fb9099-a08e-4c3d-a538-d6f7542f7052" />



2. Set up your Git identity — name and email
```
git config --global user.name "sumit"
git config --global user.email "sumitshimpale@gmail.com"
````



3. Verify your configuration
````
 git config --list
````


### Task 2: Create Your Git Project

1. Create a new folder called `devops-git-practice`
````
mkdir devops-git-practice
cd devops-git-practice/
````
2. Initialize it as a Git repository
````
git init
````


3. Check the status — read and understand what Git is telling you

```
`git status`
```



4. Explore the hidden `.git/` directory — look at what's inside
````
cd .git/
ls -la
````


---

### Task 3: Create Your Git Commands Reference
1. Create a file called `git-commands.md` inside the repo
````
touch git-commands.md
````
3. Add the Git commands you've used so far, organized by category:
````
## git commands

## setup user and config

- git config --global user.name "your name" : sets ur name
- git config --global user.email "your-email@example.com" : it sets ur email


## ## Basic Workflow

- git init : Initialize a Git repository
- git add : Stages changes - eg: git add git-commands.md
- git commit : Saves staged changes - eg: git commit -m "Added git commands file"

#VIEWING CHANGES

- git status : Shows current state of repo
- git log : commit history
- git log --oneline : Compact commit history
````
---

### Task 4: Stage and Commit
1. Stage your file
````
git add .
````
2. Check what's staged
````
 git status
````
3. Commit with a meaningful message
````
git commit -m "added git commands."
````

4. View your commit history
````
 git log --oneline

````
---

### Task 5: Make More Changes and Build History
1. Edit `git-commands.md` — add more commands as you discover them
````
    git status
    git add .
   git commit -m "added git diff command"
````

2. Check what changed since your last commit
````
git status
````
3. Stage and commit again with a different, descriptive message
````
git commit -m "added git diff command"
 git commit -m "added git restore command"
 git commit -m "added git rm command"
````
4. Repeat this process at least **3 times** so you have multiple commits in your history


5. View the full history in a compact format
````
git log --oneline

````



