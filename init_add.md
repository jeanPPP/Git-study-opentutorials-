저장소 만들기
----------

프로젝트 파일을 만듦
`mkdir gitfth`

현재 위치 
`~/Documents/gitfth`

현재 디렉토리를 git의 버전 저장소로 만듦
`git init`

git이 관리할 대상으로 파일 등록
----------------------

vim이라는 에디터를 사용한다.
f1.txt라는 파일을 만들고 거기에 숫자 1을 쓸것.
`vim f1.txt`

현재는 아무것도 쓸 수 없는데, 알파벳 i를 입력하면 insert 상태가 됨.

`souce: 1`

입력하고 esc를 누르면 편집할 수 없게 됨.

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
