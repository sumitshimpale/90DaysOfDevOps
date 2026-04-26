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
<img width="1214" height="120" alt="image" src="https://github.com/user-attachments/assets/991d9582-cc09-4fc4-a000-418ee617e939" />



3. Verify your configuration
````
 git config --list
````
<img width="671" height="154" alt="image" src="https://github.com/user-attachments/assets/a6b30f07-ff25-41c6-a496-65b4c380cdc0" />


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
<img width="1177" height="457" alt="image" src="https://github.com/user-attachments/assets/b3e38580-ee22-42bf-adce-ccc6332a33c0" />


3. Check the status — read and understand what Git is telling you

```
`git status`
```

<img width="970" height="207" alt="image" src="https://github.com/user-attachments/assets/bca55468-ce49-4960-9190-046ed0796d8d" />


4. Explore the hidden `.git/` directory — look at what's inside
````
cd .git/
ls -la
````
<img width="965" height="395" alt="image" src="https://github.com/user-attachments/assets/9d0d01e5-feb4-4137-a9a7-956651ab69bd" />


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
<img width="1233" height="811" alt="image" src="https://github.com/user-attachments/assets/e6b4cc0b-3213-4bc7-a653-3ee77f2e59ec" />

4. View your commit history
````
 git log --oneline

````
<img width="952" height="217" alt="image" src="https://github.com/user-attachments/assets/c0111581-26fc-44fd-bfa2-508525c30b45" />


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
git log --oneline
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

<img width="969" height="235" alt="image" src="https://github.com/user-attachments/assets/4a408c2e-abaf-4641-bbd6-1203f539795a" />


