##  디장고 MVT

sudo apt install python-virtualenv // virtualenv 설치

virtualenv --python=python3.6 myvenv // 가상환경 만들기

mkdir 프로젝트 이름 // 폴더 만들고
. myvenv/bin/activate // 가상환경을 실행시켜준다.

pip install django~=1.11.0 // 장고 설치

django-admin startproject signup . // 현재위치에 프로젝트를 만든다.

setting.py 에서 Allowed_host와 time_zone 수정

마코 템플릿도 적용시키자
**마코 템플릿**

        {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'NAME': 'django',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },

**python manage.py startapp backend // 어플리케이션 만들기**

어플리케이션을 생성한 후엔 setting.py에 설치했다고 명시를 해줘야한다.

메인 어플리케이션에 urls.py에 들어가서 include명령어로 어플리케이션과 urls연동을 시켜주고 메인어플리케이션이 아니면 urls.py가 없기때문에 복사해서 만들어준다.

어플리케이션의 urls.py 에 
from . import views // 현재 어플리케이션의 views항목을 전부 불러와주고

    urlpatterns = [
        url(r'^$', views.post_list, name='post_list'),
    ]
^ == url 시작을 의미
& == url 끝을 의미
즉, r'^&'는 아무것도 안써있는url주소를 의미한다

from. import views 에서 뷰를 불러오긴 했지만 설정을 해준것이 없기때문에 
views.py 를 연다

    def post_list(request)
    	return render(request, '템플릿 주소', 딕셔너리) 이렇게 만들어주면 된다
  마지막으로 데이터 베이스의 model부분은 ORM을 쓰는 것이 아니라 sql을 사용함 // 개발자들이 굳이 orm을 배우는 것보다 사용하던 sql을 사용하는 것이 시간적, 비용적으로 유리함
  
## MYSQL 설치
`sudo apt-get install mysql-server mysql-client` // sql 설치

설치하면 루트 사용자의 비밀번호를 입력하라는 창이 뜬다.

※ 혹시 설치가 안되는 경우

    sudo apt-get install -y python3.6-dev libmysqlclient-dev build-essential uuid-dev libcap-dev libpcre3-dev libssl-dev

설치 후에
setting.py 에 database

    DATABASES = {  
      'default': {  
      'ENGINE': 'django.db.backends.mysql',  
      'NAME': 'signup',  
      'HOST': '127.0.0.1',  
      'PORT': '3306',  
      'USER': 'admin',  
      'PASSWORD': '0000'  
      }  
    }


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE4NDM0OTU0NywtMTQ1NDcxOTMwOSwxMT
E5MjQ3NDU3LDEyNDQzNTY1MTAsNDMyMDg0NjY3LDIxMDg4MDE4
OTcsMTY5NzA5MTk2OCwtMzkxMjUwNDA3LC05OTgyOTUxNTgsLT
Q4MTM4MjY4M119
-->