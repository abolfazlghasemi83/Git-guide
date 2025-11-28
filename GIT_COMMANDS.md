# 📚 Git Guide: دستورات گیت (Git Commands)

>  This guide includes essential Git commands in both Persian and English.


>     این راهنما شامل دستورات ضروری گیت به دو زبان فارسی و انگلیسی است.


---

## 🚀 ۱. راه‌اندازی و پیکربندی (Setup & Configuration)

### 1.1. تنظیم نام و ایمیل (Set Name and Email)

**فارسی:** این دستور نام کاربری شما را برای Commitهای محلی تنظیم می‌کند.

**English:** This command sets your username for local commits.

**دستور / Command:**
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"




شاخه‌ها و ادغام (Branches and Merging)
2. نمایش شاخه‌ها (List Branches)
فارسی: تمام شاخه‌های موجود در مخزن محلی را نمایش می‌دهد و شاخه فعلی را با ستاره (*) مشخص می‌کند.

English: Displays all existing branches in the local repository, marking the current branch with an asterisk (*).

دستور / Command:

Bash

git branch
2.1. ایجاد شاخه جدید (Create a New Branch)
فارسی: یک شاخه جدید بر اساس Commit فعلی ایجاد می‌کند. (توجه: به طور خودکار به آن شاخه سوییچ نمی‌کند.)

English: Creates a new branch based on the current commit. (Note: It does not switch to the new branch automatically.)

دستور / Command:

Bash

git branch new-feature
2.2. سوییچ به شاخه (Switch Branches)
فارسی: شما را به شاخه مشخص شده منتقل می‌کند. همچنین برای بازگرداندن فایل‌های فضای کاری به آخرین Commit استفاده می‌شود.

English: Moves you to the specified branch. It is also used to revert working files back to the last commit.

دستور / Command:

Bash

git checkout branch-name
2.3. ایجاد و سوییچ همزمان (Create and Switch Simultaneously)
فارسی: یک شاخه جدید ایجاد کرده و بلافاصله به آن سوییچ می‌کند. این دستور جایگزینی مدرن برای git checkout -b است.

English: Creates a new branch and switches to it immediately. This is the modern replacement for git checkout -b.

دستور / Command:

Bash

git switch -c new-branch-name
2.4. ادغام شاخه‌ها (Merge Branches)
فارسی: تغییرات از شاخه مشخص شده را با شاخه فعلی ادغام می‌کند. این کار یک Commit جدید (Merge Commit) ایجاد می‌کند.

English: Merges changes from the specified branch into the current branch. This action typically creates a new merge commit.

دستور / Command:

Bash

# مطمئن شوید که در شاخه مقصد هستید (مثلاً main)
git merge feature-branch
2.5. حذف شاخه (Delete a Branch)
فارسی: شاخه محلی مشخص شده را حذف می‌کند. پرچم -d تنها در صورتی شاخه را حذف می‌کند که Merge شده باشد. از -D برای حذف اجباری استفاده کنید.

English: Deletes the specified local branch. The -d flag only deletes the branch if it has been merged. Use -D for forceful deletion.

دستور / Command:

Bash

git branch -d old-branch-name
🕰️ 3. تاریخچه، بازگردانی و Diff (History, Undoing, and Diff)
3.1. مشاهده تاریخچه (View History)
فارسی: تاریخچه Commitها را به ترتیب زمانی معکوس نمایش می‌دهد.

English: Displays the history of commits in reverse chronological order.

دستور / Command:

Bash

# نمایش ساده
git log

# نمایش گرافیکی خطی
git log --oneline --graph
3.2. بررسی تفاوت‌ها (View Differences - Diff)
فارسی: تفاوت‌ها بین فضای کاری، Staging Area و آخرین Commit را نشان می‌دهد.

English: Shows the differences between the working directory, the Staging Area, and the last commit.

دستور / Command:

Bash

# تفاوت بین فضای کاری و Staging
git diff

# تفاوت بین Staging و آخرین Commit
git diff --staged

# تفاوت بین دو Commit
git diff commit_hash_1 commit_hash_2
3.3. بازگرداندن فایل‌ها (Discard Local Changes)
فارسی: تغییرات محلی یک فایل را لغو می‌کند و آن را به حالت آخرین Commit یا Staged برمی‌گرداند.

English: Undoes local modifications to a file, restoring it to the state of the last commit or staged version.

دستور / Command:

Bash

git restore file_name.txt
3.4. خروج از Staging (Unstage Files)
فارسی: فایل‌ها را از Staging Area خارج می‌کند و آن‌ها را در فضای کاری نگه می‌دارد.

English: Unstages files from the Staging Area, keeping them in the working directory.

دستور / Command:

Bash

git restore --staged file_name.txt
3.5. بازنشانی (Reset)
فارسی: تاریخچه Commit را تغییر می‌دهد و به Commit قبلی بازمی‌گردد. حالت soft Commit را حذف می‌کند اما فایل‌ها را در Staging نگه می‌دارد. حالت hard Commit و تمام تغییرات را حذف می‌کند.

English: Modifies the commit history and reverts to a previous commit. soft removes the commit but keeps files staged. hard deletes the commit and all local changes.

دستور / Command:

Bash

# بازگشت به commit قبلی (فایل‌ها دست نخورده باقی می‌مانند)
git reset HEAD~1

# بازگشت به commit خاص (تمام تغییرات پس از آن commit از بین می‌روند)
git reset --hard commit_hash
⚙️ 4. دستورات متفرقه و پیشرفته (Miscellaneous and Advanced Commands)
4.1. نمایش اطلاعات ریموت (Show Remote Info)
فارسی: جزئیات مخازن از راه دور پیکربندی شده (مانند آدرس URL) را نمایش می‌دهد.

English: Displays details of the configured remote repositories (such as the URL address).

دستور / Command:

Bash

git remote -v
4.2. نادیده گرفتن فایل‌ها (Ignoring Files)
فارسی: برای تعیین فایل‌ها و پوشه‌هایی که گیت نباید ردیابی کند (مانند فایل‌های موقت، لاگ‌ها، یا پوشه node_modules).

English: Used to specify files and directories that Git should not track (e.g., temporary files, logs, or the node_modules folder).

دستور / Command:

Bash

# پس از ایجاد یا ویرایش فایل .gitignore
git add .gitignore
git commit -m "Add .gitignore file"
