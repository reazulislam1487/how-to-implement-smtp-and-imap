# Git & GitHub Complete Guide (Beginner to Practical)

This repository contains a complete Git & GitHub workflow guide.
It is designed for beginners and covers real-world, team-safe practices.

---

## Table of Contents
1. Basic Git Commands
2. Viewing Commit History
3. Fork & Clone Workflow
4. Remote Repositories
5. Branching Strategy
6. Working with Files
7. git commit -am Explained
8. Replacing Old Code
9. Merge Conflicts
10. Undo / Delete Commits
11. Best Practices
12. One-Line Workflow
13. Interview Notes

---

## 1. Basic Git Commands

Check status:
git status

Initialize repository:
git init

---

## 2. Viewing Commit History

Full history:
git log

Short history:
git log --oneline

---

## 3. Fork & Clone Workflow

Fork the repository from GitHub, then clone your fork:

git clone https://github.com/your-username/repo-name.git
cd repo-name

---

## 4. Remote Repositories

Add original repo as upstream:

git remote add upstream https://github.com/original-owner/repo-name.git

Check remotes:
git remote -v

---

## 5. Branching Strategy

Update main:
git checkout main
git pull upstream main

Create new branch:
git checkout -b feature-branch-name

Never work directly on main.

---

## 6. Working with Files

New file + modified file:

git status
git add .
git commit -m "Add new feature and update existing code"

---

## 7. git commit -am Explained

git commit -am "message"

- Works only for tracked files
- Does NOT include new files

Use only when no new files are added.

---

## 8. Replacing Old Code

Delete old code and write new code is normal modification:

git diff
git add .
git commit -m "Replace old logic with new implementation"

---

## 9. Merge Conflicts

Conflicts happen during:
- git pull
- git merge
- git rebase

After resolving:

git add .
git commit -m "Resolve merge conflict"

---

## 10. Undo / Delete Commits

SAFE (already pushed):

git log --oneline
git revert <commit-hash>

HARD DELETE (personal branch only):

git log --oneline
git reset --hard <previous-commit-hash>
git push --force

---

## 11. Best Practices

- Always create a branch
- Avoid force push on shared branches
- Use git revert for pushed commits
- Write clear commit messages

---

## 12. One-Line Workflow

Fork → Clone → Branch → Code → Add → Commit → Push → Pull Request

---

## 13. Interview Notes

- git commit -am works only for tracked files
- Conflicts occur during merge or pull
- git revert is safer than git reset
- Never commit directly to main

---

End of README
