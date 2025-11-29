# Git Cheat Sheet 

## بخشی از دستورات اصلی Git

| بخش | دستور | توضیح |
|------|---------|---------|
| **Identity** | `git config --global user.name "Your Name"` | تنظیم نام کاربر |
| | `git config --global user.email "email@example.com"` | تنظیم ایمیل |
| **شروع کار** | `git init` | ساخت مخزن جدید |
| | `git clone URL` | کلون کردن مخزن |
| **Add & Commit** | `git add .` | افزودن همه تغییرات |
| | `git commit -m "message"` | ثبت کامیت |
| **Push & Pull** | `git push origin main` | پوش به ریموت |
| | `git pull` | دریافت آخرین تغییرات |
| **Branching** | `git branch` | نمایش همه شاخه‌ها |
| | `git switch name` | تغییر شاخه |
| | `git branch -d name` | حذف شاخه |
| **Merge** | `git merge branch` | ادغام شاخه‌ها |
| | `git merge --abort` | کنسل ادغام |
| **Logs** | `git log --oneline --graph` | نمایش تاریخچه فشرده |
| | `git show commit` | نمایش جزئیات کامیت |
| **Undo / Reset** | `git restore file` | بازیابی فایل |
| | `git reset HEAD~1` | بازگردانی آخرین کامیت بدون حذف تغییرات |
| | `git reset --hard id` | بازنشانی کامل به یک کامیت |
| **Diff** | `git diff` | مقایسه تغییرات فعلی |
| | `git diff commit1 commit2` | مقایسه دو کامیت |
| **Stash** | `git stash` | ذخیره موقت تغییرات |
| | `git stash pop` | بازگردانی + حذف از stash |
| **Remote** | `git remote -v` | لیست ریموت‌ها |
| | `git remote add origin URL` | اتصال به ریموت |
| **.gitignore** | `echo "node_modules/" >> .gitignore` | اضافه کردن مسیر به گیت‌ignore |

---


