## python update


우분투를 최신버전으로 업데이트
sudo apt-get update

파이썬을 최신버전으로 업그레이드
sudo apt-get upgrade python3

파이썬이 업그레이드가 됬나
python3 --version으로 확인해봐도 여전히
3.5.2 버전을 가리키고 있다

**sudo add-apt-repository ppa:jonathonf/python-3.6

파이썬 3.6버전을 인스톨 한다
sudo apt-get install python3.6

아래의 명령어를 실행
sudo update-alternatives –install /usr/bin/python3 python3 /usr/bin/python3.5 1

아래의 명령어도 실행

sudo update-alternatives –install /usr/bin/python3 python3 /usr/bin/python3.6 2

마지막 sudo update-alternatives –config python3
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU1NjQ3MzQ1OF19
-->