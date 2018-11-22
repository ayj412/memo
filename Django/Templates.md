### 필터 적용하기

    <div  class="content">{{ "{{ post.content|truncatewords:30 " }}}}</div>

truncateworlds 단어 수 필터를 적용하여 30 단어까지만 보여주기

### 게시날짜가 없는 글은 표시 안하기
*{% if post.published_date != None %}*
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg2NTg4OTQwMl19
-->