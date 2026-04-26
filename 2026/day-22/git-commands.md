## Challenge Tasks

### Task 1: Install and Configure Git

# Task 1: Install and Configure Git

## 1. Check Git installation

```bash
git --version




2. Set up your Git identity — name and email

git config --global user.name "sumit"
git config --global user.email "sumitshimpale@gmail.com"



3. Verify your configuration

 git config --list
---


### Task 2: Create Your Git Project
1. Create a new folder called `devops-git-practice`

mkdir devops-git-practice
cd devops-git-practice/

2. Initialize it as a Git repository

git init



3. Check the status — read and understand what Git is telling you

```
`git status`
```



4. Explore the hidden `.git/` directory — look at what's inside

cd .git/
ls -la



---

### Task 3: Create Your Git Commands Reference
1. Create a file called `git-commands.md` inside the repo



2. Add the Git commands you've used so far, organized by category:

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

---

### Task 4: Stage and Commit
1. Stage your file

git add .

2. Check what's staged

 git status

3. Commit with a meaningful message

git commit -m "added git commands."


4. View your commit history

 git log


---

### Task 5: Make More Changes and Build History
1. Edit `git-commands.md` — add more commands as you discover them

    git status
    git add .
   git commit -m "added git diff command"


2. Check what changed since your last commit

git status

3. Stage and commit again with a different, descriptive message

git commit -m "added git diff command"
 git commit -m "added git restore command"
 git commit -m "added git rm command"

4. Repeat this process at least **3 times** so you have multiple commits in your history



5. View the full history in a compact format

---


### Task 6: Understand the Git Workflow
Answer these questions in your own words (add them to a `day-22-notes.md` file):
1. What is the difference between `git add` and `git commit`?
2. What does the **staging area** do? Why doesn't Git just commit directly?
3. What information does `git log` show you?
4. What is the `.git/` folder and what happens if you delete it?
5. What is the difference between a **working directory**, **staging area**, and **repository**?

---

## Ongoing Task

**Keep updating `git-commands.md` every day** as you learn new Git commands in the upcoming days. This will become your personal Git reference. Maintain a clean commit history — one commit per update with a clear message.

---

## Hints
- All you need today are about 8-10 Git commands — Google them, try them, break things
- Read what `git status` tells you — it's your best friend
- Use `man git-<command>` or `git <command> --help` to explore

---

## Submission
1. Share a screenshot of your `git log --oneline` output showing multiple commits
2. Add your `day-22-notes.md` to `2026/day-22/`
3. Commit and push to your fork
4. Add your submission for Community Builder of the week on discord


