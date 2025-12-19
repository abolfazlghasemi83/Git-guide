# 📘 The Essential Git Guide — راهنمای دستورات ضروری گیت

This guide covers all the essential commands you need for your daily Git workflow, from beginner to proficient.

این راهنما تمام دستورات ضروری برای کارهای روزمره با گیت را پوشش می‌دهد، از سطح مبتدی تا حرفه‌ای.

---

## 🧩 1) Setup & Configuration — تنظیمات اولیه (یک بار برای همیشه)

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git config --global user.name "..."` | تنظیم نام کاربری | Sets your username for all projects. |
| `git config --global user.email "..."` | تنظیم ایمیل | Sets your email for all projects. |
| `git config --list` | نمایش تنظیمات | Shows the current configuration. |

---

## 🌱 2) Creating a Repository — ساخت مخزن

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git init` | ساخت مخزن جدید در پوشه فعلی | Initializes a new repository in the current directory. |
| `git clone [url]` | کپی کردن یک مخزن از راه دور | Clones a repository from a remote URL. |

---

## 📤 3) The Core Workflow — چرخه کاری اصلی

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git status` | نمایش وضعیت فایل‌ها | Shows the status of your files. |
| `git add [file]` | افزودن یک فایل به صف کامیت | Adds a specific file to the staging area. |
| `git add .` | افزودن تمام تغییرات به صف | Adds all current changes to the staging area. |
| `git commit -m "..."` | ثبت نهایی تغییرات با یک پیام | Commits the staged changes with a message. |
| `git push` | ارسال تغییرات به مخزن ریموت | Pushes your commits to the remote repository. |
| `git pull` | دریافت و ادغام تغییرات از ریموت | Fetches and merges changes from the remote. |

---

## 🌳 4) Branching — کار با شاخه‌ها

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git branch` | نمایش لیست شاخه‌ها | Lists all local branches. |
| `git branch [name]` | ساخت یک شاخه جدید | Creates a new branch. |
| `git switch [name]` | جابجایی به یک شاخه | Switches to the specified branch. |
| `git switch -c [name]` | ساخت شاخه جدید و جابجایی به آن | Creates and switches to a new branch. |
| `git branch -d [name]` | حذف یک شاخه (پس از ادغام) | Deletes a merged branch. |
| `git branch -m [new-name]` | تغییر نام شاخه فعلی | Renames the current branch. |

---

## 🔗 5) Merging & Rebasing — ادغام و بازآرایی

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git merge [branch]` | ادغام یک شاخه در شاخه فعلی | Merges the specified branch into the current one. |
| `git merge --abort` | لغو عملیات ادغام (در صورت تداخل) | Aborts a merge that has conflicts. |
| `git rebase [branch]` | بازآرایی کامیت‌ها روی شاخه‌ای دیگر | Re-applies commits from your branch onto another. |

---

## 🕰️ 6) History & Logs — تاریخچه

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git log` | نمایش کامل تاریخچه کامیت‌ها | Shows the detailed commit history. |
| `git log --oneline --graph` | نمایش تاریخچه به صورت فشرده و گرافیکی | Shows a compact, graphical view of the history. |
| `git show [commit]` | نمایش جزئیات یک کامیت | Shows the details of a specific commit. |

---

## 🔄 7) Undoing Changes — بازگردانی تغییرات

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git restore [file]` | لغو تغییرات در یک فایل (قبل از `add`) | Discards changes in a file. |
| `git restore --staged [file]` | خارج کردن فایل از حالت Staging | Unstages a file while keeping the changes. |
| `git reset HEAD~1` | لغو آخرین کامیت (تغییرات باقی می‌ماند) | Undoes the last commit, but keeps the file changes. |
| `git reset --hard [commit]` | بازنشانی کامل به یک کامیت (تغییرات حذف می‌شود) | Resets to a specific commit, discarding all changes. |

---

## 🗂️ 8) Diff — مقایسه تغییرات

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git diff` | مقایسه تغییرات فعلی با آخرین کامیت | Shows changes between working directory and the last commit. |
| `git diff --staged` | مقایسه تغییرات Staged با آخرین کامیت | Shows changes between the staging area and the last commit. |

---

## 🧳 9) Stash — ذخیره موقت

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git stash` | ذخیره موقت تغییرات | Temporarily stores all uncommitted changes. |
| `git stash pop` | اعمال آخرین Stash و حذف آن | Applies the last stash and removes it from the list. |
| `git stash list` | نمایش لیست Stashها | Lists all stashed changes. |

---

## 🌐 10) Remotes — کار با مخازن ریموت

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git remote -v` | نمایش لیست ریموت‌ها | Lists all remote repositories. |
| `git remote add [name] [url]` | افزودن یک ریموت جدید | Adds a new remote repository. |

---

## 🔖 11) Tagging — برچسب‌گذاری (نسخه‌بندی)

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `git tag [tag-name]` | ساخت یک تگ جدید (مثلا `v1.0`) | Creates a new tag for versioning. |
| `git push --tags` | ارسال تمام تگ‌ها به ریموت | Pushes all local tags to the remote. |

---

## 🧱 12) .gitignore — نادیده گرفتن فایل‌ها

| دستور (Command) | توضیح فارسی | English Description |
| :--- | :--- | :--- |
| `echo "node_modules/" >> .gitignore` | افزودن فایل/پوشه به لیست نادیده‌ها | Adds a path to the `.gitignore` file. |

