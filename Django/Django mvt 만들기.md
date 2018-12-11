###디장고 MVT

sudo apt install python-virtualenv // virtualenv 설치
virtualenv --python=python3.6 myvenv // 가상환경 만들기
mkdir 프로젝트 이름 // 폴더 만들고
. myvenv/bin/activate // 가상환경을 실행시켜준다.
pip install django~=1.11.0 // 장고 설치
django-admin startproject signup . // 현재위치에 프로젝트를 만든다.
setting.py 에서 Allowed_host와 time_zone 수정

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY5NzA5MTk2OCwtMzkxMjUwNDA3LC05OT
gyOTUxNTgsLTQ4MTM4MjY4M119
-->