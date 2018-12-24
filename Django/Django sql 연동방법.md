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

sudo apt-get install mysql-server

mysql -u root -p

sudo mysql

ex)
grant all privileges on *.* to 'id'@'%' identified by 'password' with grant option;

grant all privileges on *.* to 'admin'@'%' identified by '0000' with grant option;
flush privileges;

show databases;

install workbench

cd /etc/mysql/

sudo grep -r "bind" .

sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf

- change bind address

sudo service mysql restart

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjc4OTAyMjM1LDI3ODkwMjIzNSwtMzA1MT
QxMDk4LC02NzQ0NDMwMTYsODMwNzQ0Nzc5XX0=
-->