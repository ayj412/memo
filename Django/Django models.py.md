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
### Post 클래스에 정읟

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwMjUxMjI2NjRdfQ==
-->