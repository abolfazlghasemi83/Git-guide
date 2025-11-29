1) Setup & Configuration
🔧 Set Username & Email

EN: Configure your identity for Git commits.
FA: تنظیم نام و ایمیل برای کامیت‌ها.

git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

🔧 Check Current Config
git config --list

🌱 2) Create / Clone Repositories
📁 Initialize New Repository
git init

⬇️ Clone a Repository
git clone https://github.com/user/repo.git

📤 3) Add → Commit → Push Workflow
➕ Add Changes
git add file.txt
git add .

💾 Commit Changes
git commit -m "Your commit message"

⬆️ Push to Remote
git push origin main

⬇️ Pull Latest Changes
git pull

🌳 4) Branching
📌 Show Branches
git branch

➕ Create New Branch
git branch new-feature

🔀 Switch Branch
git switch new-feature


or

git checkout new-feature

🎯 Create & Switch
git switch -c new-branch

🗑️ Delete Branch
git branch -d branch-name

🔗 5) Merging
🔀 Merge Branch into Current
git merge feature-branch

⚠️ Abort Merge
git merge --abort

🕰️ 6) History & Logs
📜 Show Commit Log
git log
git log --oneline --graph

🔍 Show Commit Details
git show commit_id

🔄 7) Undoing, Restore, Reset
🔄 Restore File
git restore file.txt

🔄 Unstage File
git restore --staged file.txt

❗ Reset Last Commit (Keep Changes)
git reset HEAD~1

💥 Full Reset (Delete Changes)
git reset --hard commit_id

🗂️ 8) Diff & Compare
🔍 Compare Working Directory
git diff

🔍 Compare Staged Files
git diff --staged

🔍 Compare Two Commits
git diff commit1 commit2

🧳 9) Stash (Save Work Temporarily)
📦 Save to Stash
git stash push -m "my temp work"

📦 List Stashes
git stash list

📦 Apply Stash
git stash apply

📦 Apply + Delete
git stash pop

🪄 10) Rebase (Clean History)
🔄 Rebase on Main
git rebase main

✏️ Interactive Rebase
git rebase -i HEAD~5

🌐 11) Remote Repositories
🔗 Show Remotes
git remote -v

➕ Add Remote
git remote add origin https://github.com/user/repo.git

❌ Remove Remote
git remote remove origin

🧱 12) .gitignore
➕ Create & Add
echo "node_modules/" >> .gitignore
git add .gitignore
git commit -m "Add gitignore"

🚀 13) Useful Commands
Check Status
git status

Rename Branch
git branch -m old-name new-name

Show Last Commit
git show
