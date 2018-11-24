### URL 주소 동적 생성
post_detail.html 템플릿은 기본주소/post/라는 고정된 하나의 주소로 접근이 가능하다 했을때 URL주소를 할당하려면 각각의 post에 대해 따로 뷰와 템플릿을 만들어주고 고유의 URL 주소를 매번 할당해주어야 한다.  //너무 불편하다
url.py

    url(r'^post/(?P<pk>\d+)/',  post_detail),
정규표현식 post/(?P<pk>\d+)/는 post/에 이어서
\d+, 즉 어떤 숫자 \d가 1개 이상(+)올 수 있으며, 그 숫자는 pk라는 이름의 그룹에 포함된다
pk == primary key의 약자, 데이터베이스의 기본키를 뜻함
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzI5OTA1NTMxXX0=
-->