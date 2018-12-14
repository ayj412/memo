## Django static 연동
settings.py

    STATIC_ROOT = BASE_DIR + '/static'  
    STATIC_URL = '/static/'  
    STATICFILES_DIRS = [  
        BASE_DIR + '/backend/static/'  
    ]

어플의 view.py 에

    from django.db import connections
    with connections['default'].cursor() as cur:
    query = '''
    select *
    FROM table
    where sample = '{page}'
    '''.format(page=page)
    cur.execute(query)
    rows = cur.fetchall()
    """
    이런식으로 작성해주면 된다.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyMDM5OTE2NDAsLTE0MDU4NDExNzJdfQ
==
-->