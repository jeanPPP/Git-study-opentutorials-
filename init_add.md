저장소 만들기
----------

프로젝트 파일을 만듦<br/>
`mkdir gitfth`



현재 위치<br/>`~/Documents/gitfth`



현재 디렉토리를 git의 버전 저장소로 만듦  
`git init`



git이 관리할 대상으로 파일 등록
----------------------

vim이라는 에디터를 사용한다.
f1.txt라는 파일을 만들고 거기에 숫자 1을 쓸것.
`vim f1.txt`

현재는 아무것도 쓸 수 없는데, 알파벳 i를 입력하면 insert 상태가 됨.

`souce: 1` 입력하고 esc를 누르면 편집할 수 없게 됨.

`:wq`  
종료와 저장

`cat f1.txt`  
내용을 확인할 수 있음.

`git status`  
현재 상황에서 status를 입력하면 untracked files가 나옴.  
프로젝트 폴더 안에 있긴 하지만 이 파일을 버전관리하라고 지정하지는 않았으므로, git에서 배제하는 것.

`git add f1.txt`

그리고 다시 status를 입력하면

`new file: f1.txt` 
라고 뜸. 

임시로 필요한 파일은 버전관리에서 배제해야하기 때문에, 명확하게 git에게 알려줘야 함.


버전 만들기(commit)
-------------------

버전: 의미있는 변화. 어떠한 작업이 있으면, 그 작업이 완결된 상태.  


먼저 이름을 세팅해야함.

`git config --global user.name "자신의 이름"`
`git config --global user.email "자신의 이메일"`


이 상태에서 `git commit`을 치고 enter  
vim이 실행됨  
git status했을 때 내용이 나오는데, #처리 되어있는 부분은 참고삼아 보면 됨.  

위에 버전의 메시지를 씀.  
이 변화가 어떤 변화를 담고 있는가, 이 파일들이 왜 변경되었는지를 쓰는 것  

i를 눌러 insert를 바꿈
1을 누르고 esc, :wq  
-> **최초로 버전을 생성한 것**
  
현재 버전이 잘 생성되었는지 확인
`git log`  

f1.txt의 버전을 바꿔보자
`vim f1.txt`

souce : 2로 바꾼 뒤 esc :wq   

git status modified되었다고 나옴  
**다시 git add f1.txt을 해야됨**  

이제 git commit을 할 수 있고 버전1을 2로 바꿈.

