### Django sql과 연동방법

pip install mysqlclient  
설치 안될 시
sudo apt-get install -y python3.6-dev libmysqlclient-dev build-essential uuid-dev libcap-dev libpcre3-dev libssl-dev

**설치 후에**
```
# settings.py

    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.mysql',
            'NAME': '', # DB명
            'USER': '', # 데이터베이스 계정
            'PASSWORD': '', # 계정 비밀번호
            'HOST': '', # 데이테베이스 주소(IP)
            'PORT': '', # 데이터베이스 포트(보통은 3306)
        }
    }

```
settings.py 세팅 후에

    ./manage.py migrate  //명령어를 실행하면 된다.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTMwNTE0MTA5OCwtNjc0NDQzMDE2LDgzMD
c0NDc3OV19
-->