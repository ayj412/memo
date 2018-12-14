## Django static 연동
settings.py

    STATIC_ROOT = BASE_DIR + '/static'  
    STATIC_URL = '/static/'  
    STATICFILES_DIRS = [  
        BASE_DIR + '/backend/static/'  
    ]

어플의 view.py 에

<!--stackedit_data:
eyJoaXN0b3J5IjpbODYxODI5OTkwLC0xNDA1ODQxMTcyXX0=
-->