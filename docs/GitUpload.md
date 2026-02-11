## Only first time
## 1️⃣ افتح Git Bash
## 2️⃣ اكتب اسمك (أي اسم تحبه)
git config --global user.name "Mohamed Khalid"
## 3️⃣ اكتب الإيميل (نفس إيميل GitHub)
git config --global user.email "your_email@gmail.com"
## _________________________________________________________________
## رفع كل حاجة على GitHub
git add .
git commit -m "Initial Jenkins CI/CD pipeline"
git push
git status
## _________________________________________________________________
## أول مرة تعمل تعديل جديد
git checkout -b feat/something
# عدّل ملفات
git status
git add <files>
git commit -m "meaningful message"
git push -u origin feat/something
## بعد كده لو عدّلت تاني على نفس الفرع
git status
git add <files>
git commit -m "another update"
git push
## _________________________________________________________________
