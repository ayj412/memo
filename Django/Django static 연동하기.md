## Django static 연동
settings.py

    STATIC_ROOT = BASE_DIR + '/static'  
    STATIC_URL = '/static/'  
    STATICFILES_DIRS = [  
        BASE_DIR + '/backend/static/'  
    ]

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0MDU4NDExNzJdfQ==
-->