###디장고 MVT

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

python manage.py startapp backend // 어플리케이션 만들기

어플리케이션을 생성한 후엔 setting.py에 설치했다고 명시를 해줘야한다.

ㅇ
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwMzEyNjE5NjIsMjEwODgwMTg5NywxNj
k3MDkxOTY4LC0zOTEyNTA0MDcsLTk5ODI5NTE1OCwtNDgxMzgy
NjgzXX0=
-->