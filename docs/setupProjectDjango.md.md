# 1. Thiết lập Django
---
### cài đặt Django
```
$ sudo pip3 install Django
```
### Kiểm tra version 
```
$ django-admin --version

2.0.6
```
# 2. Taọ project với Django

Tạo project
```
django-admin startproject mysite
```
Cấu trúc __startproject__ vừa tạo:
```
mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        wsgi.py
```
Những file này là:
- Bên ngoài thư mục gôc __mysite/__ thư mục gôc là nơi chứa các file cho project. 
- __manage.py__ : Command-line cho phép bạn tương tác với project này theo nhiều cách khác nhau.
- Bên trong thư mục __mysite/__ là Python package cho project. 
- __mysite/\_\_init\_\_.py__ : Một file rỗng cho Python biết rằng thư mục này được coi là một Python package.
- __mysite/settings.py__ : Setting/configuration cho projcet.
- __mysite/urls.py__: Các khai báo URL  cho project.
- __mysite/wsgi.py__: Một điểm vào cho các máy chủ web tương thích với WSGI để phục vụ project.

## Chạy server 
```
$ python3 manage.py runserver
Performing system checks...

System check identified no issues (0 silenced).

You have 14 unapplied migration(s). Your project may not work properly until you apply the migrations forapp(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.

August 24, 2018 - 07:51:19
Django version 2.0.6, using settings 'mysite.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```
## Tạo app trong mysite 
```
$ python3 manage.py startapp polls
```






