## 장고 게시판구현  models.py 
from django.conf import settings

글을 뜻하는 Post 클래스 생성

    class Post(models.Model):
이 클래스는 djanggo.db.modls.Modle을 상속받아
모델 클래스가 된다.

그 클래스 안에
글에 필요한 작성자, 제목, 내용, 작성날짜, 게시날짜 라는 속성을 정의한다

    author = models.ForeignKey(settings.AUTH_USER_MODEL)
    title = models.CharField(max_length=100)
    content = models.TextField(blank=True)
    created_date = models.DateTimeField(auto_now_add=True)
    published_date = models.DateTimeField(blank=True, null=True)
### Post 클래스에 정의된 필드들
    author = models.ForeignKey(settings.AUTH_USER_MODEL)
models.ForeignKey는 필드를 외래키로 만들고, 다른 테이블과 연결을 뜻한다
models.ForeignKey는 기본적으로 일 대 다 관계이며, 연결 대상이 되는 테이블을 인자로 받는다.
settings.AUTH_USER_MODEL은 Django에 기본적으로 내장된 유저 모델이다.
글이 작성자 테이블에 연결되도록 settings.AUTH_USER_MODEL을 외래키의 인자로 전달하였다.
    title = models.CharField(max_length=100)
models.CharField 글자 수가 제한된 필드

    content = models.TextField(blank=True)
 modles.TextField은 많은 문자열을 저장하는 필드
 blank 옵션은 필드가 비어 있는 경우를 허용하는가에 대한 옵션
    created_date = models.DateTimeField(auto_now_add=True)
    published_date = models.DateTimeField(blank=True, null=True)
    models.DateTimeFiled는 날짜와 시간 필드를 뜻하고, python의 datatime.date의 인스턴스로 생성된다
    auto_now_add옵션은 객체가 처음 생성될 때 시간을 자동으로 저장하는 옵션 이것은 settings.py의 타임존의 시간을 따른다
    null은 비어있는 값을 데이터베이스에 NULL로 저장할지에 대한 옵션

### 데이터 베이스 스키마 확인하기
python manage.py sqlmigrate 앱이름 migration 번호

    python manage.py sqlmigrate blog 0001
    BEGIN;
    -- Create model Post
    CREATE TABLE "blog_post" ("id" integer NOT NULL PRIMARY KEY AUTOINCREMENT, "title" varchar(100) NOT NULL, "content" text NOT NULL, "created_date" datetime NOT NULL, "published_date" datetime NULL, "author_id" integer NOT NULL REFERENCES "auth_user" ("id"));
    CREATE INDEX "blog_post_author_id_dd7a8485" ON "blog_post" ("author_id");
    COMMIT;

우리가 만든 모델이 가지는 구조의 테이블을 데이터베이스에 기록하는 SQL명령어를 확인할 수 있다. 이렇게 데이터베이스의 자료 구조, 자료간 관계 등을 정의해놓은 것을 데이터베이스 스키마라고 한다.

<!--stackedit_data:
eyJoaXN0b3J5IjpbMzMxOTgwOTVdfQ==
-->