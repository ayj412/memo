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

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI5Mjk3NzgwMCwxNjk3MDkxOTY4LC0zOT
EyNTA0MDcsLTk5ODI5NTE1OCwtNDgxMzgyNjgzXX0=
-->