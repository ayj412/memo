# 하루에 한번씩은 보자
1. 강제 새로고침을 해서 결과값이 제대로 나왔는지 확인하기
2. 중복된 로직이 있으면 꼭 모듈화로 묶을 것 make명령어
3. root권한은 주지말고, 해당 서비스의 데이터베이스로만 접근할 수 있는 계정을 만들어라
4. 프론트엔드 -> 백엔드 -> 데이터베이스 전부 유효성 처리를 해줘야한다. 이유는 

    프론트엔드에서만 유효성처리
   - 해커에게 노출 됨
    
    백엔드에서만 유효성처리
   - 서버 과부화에 노출 됨
    
    데이터베이스 유효성처리 안함
    - 개발자의 실수를 막아주지 못함
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEyMjk3NDUzOSwtMTExOTY0MDkwMyw2Nz
UxNzM2NjIsMzE1NzE2MDY2LDE2OTc2NDA2NDFdfQ==
-->