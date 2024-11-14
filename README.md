# scripts-for-test
#!/bin/bash

# نام کاربری و آدرس مخزن را تنظیم کنید
REPO_URL="https://github.com/USERNAME/REPO_NAME.git"

# اگر مخزن را هنوز کلون نکرده‌اید
if [ ! -d "./REPO_NAME" ]; then
  git clone $REPO_URL
fi

# به دایرکتوری مخزن بروید
cd REPO_NAME

# فایل‌ها را به Git اضافه کنید
git add .

# پیغام Commit
git commit -m "Add new files"

# فایل‌ها را به مخزن روی GitHub بفرستید
git push origin main
