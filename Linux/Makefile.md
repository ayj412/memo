## make 사용법
*venv:
        virtualenv -p python3.6 venv
req:
        pip install -r requirements.txt
db:
        docker-compose up -d
mig:
        python manage.py migrate
sql:
        mysql -h127.0.0.1 -P3315 -uroot -p0000 -e"use main;source make.sql;"
server:
        python manage.py runserver 0.0.0.0:8000*
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg2ODI5MTE1Niw3MzA5OTgxMTZdfQ==
-->