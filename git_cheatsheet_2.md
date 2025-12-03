# Git Cheat Sheet 

## 🧩 1) Setup & Configuration — تنظیمات اولیه

### 🔧 Set Username & Email — تنظیم نام و ایمیل
**EN:** Configure identity for commits.  
**FA:** تعیین نام و ایمیل برای کامیت‌ها.

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 🔧 Check Current Git Configuration
```bash
git config --list
```

## 🌱 2) Repositories — مخزن‌ها

### 📁 Initialize New Repository
```bash
git init
```

### ⬇️ Clone a Repository
```bash
git clone https://github.com/user/repo.git
```

## 📤 3) Add → Commit → Push — چرخه کاری اصلی

### ➕ Add Changes
```bash
git add file.txt
git add .
```

### 💾 Commit Changes
```bash
git commit -m "Your commit message"
```

### ⬆️ Push to Remote
```bash
git push origin main
```

### ⬇️ Pull Changes
```bash
git pull
```

## 🌳 4) Branching — کار با شاخه‌ها

### 📌 Show Branches
```bash
git branch
```

### ➕ Create New Branch
```bash
git branch new-feature
```

### 🔀 Switch Branch
```bash
git switch new-feature
```

or

```bash
git checkout new-feature
```

### 🎯 Create + Switch
```bash
git switch -c new-branch
```

### 🗑️ Delete Branch
```bash
git branch -d branch-name
```

## 🔗 5) Merging — ادغام شاخه‌ها

### 🔀 Merge Branch
```bash
git merge feature-branch
```

### ⚠️ Abort Merge
```bash
git merge --abort
```

## 🕰️ 6) History & Logs — تاریخچه

### 📜 Show Commit Log
```bash
git log
git log --oneline --graph
```

### 🔍 Show Commit Details
```bash
git show commit_id
```

## 🔄 7) Undo / Restore / Reset — بازگردانی

### 🔄 Restore File
```bash
git restore file.txt
```

### 🔄 Unstage File
```bash
git restore --staged file.txt
```

### ❗ Reset Last Commit (Keep Changes)
```bash
git reset HEAD~1
```

### 💥 Full Reset (Delete Changes)
```bash
git reset --hard commit_id
```

## 🗂️ 8) Diff — مقایسه تغییرات

### 🔍 Working Directory vs Staged
```bash
git diff
```

### 🔍 Staged vs Last Commit
```bash
git diff --staged
```

### 🔍 Compare Two Commits
```bash
git diff commit1 commit2
```

## 🧳 9) Stash — ذخیره موقت

### 📦 Save to Stash
```bash
git stash push -m "my temp work"
```

### 📦 List Stashes
```bash
git stash list
```

### 📦 Apply Stash
```bash
git stash apply
```

### 📦 Apply + Remove
```bash
git stash pop
```

## 🪄 10) Rebase — بازسازی تاریخچه

### 🔄 Rebase on Main
```bash
git rebase main
```

### ✏️ Interactive Rebase
```bash
git rebase -i HEAD~5
```

## 🌐 11) Remote Repositories — مخازن ریموت

### 🔗 Show Remotes
```bash
git remote -v
```

### ➕ Add Remote
```bash
git remote add origin https://github.com/user/repo.git
```

### ❌ Remove Remote
```bash
git remote remove origin
```

## 🧱 12) .gitignore — فایل نادیده‌گرفته‌ها

### ➕ Add Path to .gitignore
```bash
echo "node_modules/" >> .gitignore
git add .gitignore
git commit -m "Add gitignore"
```

## 🚀 13) Useful Commands — دستورات کاربردی

### 🔍 Check Status
```bash
git status
```

### 🏷️ Rename Branch
```bash
git branch -m old-name new-name
```

### 📌 Show Last Commit
```bash
git show
```
