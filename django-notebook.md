# Using Django in Jupyter Notebook

การใช้งาน Django ใน Jupyter Notebook สามารถทำตามขั้นตอนดังนี้

1. ติดตั้ง virtualenv และ django
2. สร้าง project Django
3. ติดตั้ง `django-extensions` ด้วยคำสั่ง

```sh
pip install django-extensions
```

4. เพิ่ม `django-extensions` ใน INSTALLED_APPS ในไฟล์ settings.py

```python
INSTALLED_APPS = [
    "django.contrib.admin",
    "django.contrib.auth",
    "django.contrib.contenttypes",
    "django.contrib.sessions",
    "django.contrib.messages",
    "django.contrib.staticfiles",

    "django_extensions",
    "blogs",
]
```

5. ทำการ start Jupyter Notebook server ด้วย command 

```sh
python manage.py shell_plus --notebook
```

ซึ่งจะเปิด Jupyter Notebook ขึ้นมาใน Web Browser

6. จากนั้นใน Cell แรกของไฟล์ Notebook เพิ่ม code นี้ลงไป

```python
import os
os.environ["DJANGO_ALLOW_ASYNC_UNSAFE"] = "true"
```

7. สามารถทำการ import models และ query ข้อมูลโดยใช้ API ของ Django ได้เลย

```python
from blogs.models import Blog

for blog in Blog.objects.all():
    print(blog)
```
