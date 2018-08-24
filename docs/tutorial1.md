# app Polls
---
## Write first _view_ 
Trong file __polls/views.py__ ta cần thêm đoạn code sau:
```
from django.http import HttpResponse

def index(request):
    return HttpResponse("Hello, world. You're at the polls index.")
```
Đây là View cơ bản nhất trong Django. Để gọi đến __view__, ta cần _map_ nó tới một URL - và cho cái này ta cần URLconf.

Để tạo một __URLconf__ trong thư mục _polls_, tọa một file `urls.py`.
Trong file __polls/urls.py__ ta thêm đoạn code sau:
```
from django.urls import path
from . import views

urlpatterns = [
    path('', views.index, name='index'),
]
```

BƯớc tiếp theo là trỏ URLconf gốc vào module __polls.urls__. In __mysite/urls.py__, thêm một _import_ cho __django.urls.include__ và thêm một __include()__ tại list __urlspatterns__, vậy ta có:
```
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('admin/', admin.site.urls),
    path('polls/', include('polls.urls')),
]
```

