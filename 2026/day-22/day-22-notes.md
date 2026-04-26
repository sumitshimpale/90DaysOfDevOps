# Day 22 Notes - Git Basics

## 1. Difference between git add and git commit

git add moves changes to staging area
git commit saves those changes permanently in repository

---

## 2. What is staging area?

It is an intermediate layer where we prepare changes before committing.
It helps in selecting only required changes instead of committing everything.

---

## 3. What does git log show?

It shows:

* commit id (hash)
* author name
* date
* commit message

---

## 4. What is .git folder?

It is the core of git repository.
It stores all commits, branches, and history.

If deleted -> repo becomes normal folder (history lost).

---

## 5. Working vs Staging vs Repository

Working Directory -> where you edit files
Staging Area -> where changes are prepared
Repository -> where changes are permanently stored

Flow:
Working -> Staging -> Repository
