information manager from hell

install(시작이 반) & run, create, read, update, delete , , , 하고 나서의 마음가짐 : 나 이거 할 줄 안다. 후 손을 털지? 계속 할지 선택.

git config —global user.name "solwoo" > 이 컴퓨터의 사용자 이름은 solwoo야 (처음 딱 1회만 하면 된다.)

git config —global user.email "woosun@walkmate.kr" > 이 컴퓨터에 사용될 이메일은 이거야. 

git, 나 버전관리 할거야. >  create repository (.git 폴더가 생긴다)

ctrl+j, ctrl+~ > console창 열기

View > command palette > default shell > bash

pwd > 위치 확인

git > 너 뭐 할수 있어? (물어보는 명령어)

git init . > 현재 디렉토리(.) 버전관리 해

git add 파일명 > 해당파일을 버전관리를 시작할거야. (git이 해당 파일을 감시하기 시작) 초록색으로 변경

git commit -m "work 1" > 새로운 버전을 만들어서 제출할거야. 내가 작업한 메시지는 워크 1이야. (커밋 후 버전이 생성)

git log > 버전의 역사를 보여줘

git log —oneline —all > 한 줄씩 보여줘. master 까지 보여줘

git status > 현재 내 저장소의 상태좀 보여줘( 개 중요) 



Working Dir >>>>>>(add)>>>>>> stage area >>>>>>(commit)>>>>>> git(저장소)

단위작업 하나가 완성되었을 때, 그것이 버전이다. 최대한 작게 끊을수록 가치가 생긴다.

* stage area : 버전 후보들 중에 선택적으로 버전을 만들기 위해 만들어진 곳



운영체제 차원 : 내가 어디에 있는지 확인

깃 차원 : git status 를 하여 상태 확인 (지속적으로 계속 합니다.)



about add

add를 한 번이라도 했었다 하면, 추적이 가능한 상태. 아니면, 추적이 불가능한 상태.

1. 새로 추가된 파일을 깃에게 추적을 시키는 등록의 의미. (stage area)
2. 추적되면서 동시에 stage로 들어간다.



Commit 할 때 -m을 안적으면 메모장이 떠서 더 많은 글을 적을 수 있다.



버전을 관리하는 의의

master(last commit) 는 가장 최신 commit 이 무엇인지 알려준다. git log 를 한 후, Head를 찾고 마스터를 찾아라. 이 저장소의 최신 commit은 누구냐?? 알려줌 

2로 reset시에 : Working copy는 2에서 이루어진 것 이다 master가 움직임

head(current working dir) 는 워킹 카피, 워킹 디렉토리만 바꾼다.(시간여행 수준) 마스터는 여전히 라스트 커밋을 가르킴.



git reset —hard 버전이름 > 나 버전을 <버전이름>으로 리셋하고 싶어! 리포지토리의 데이터를 꺼내서 워킹 디렉토리에 쏟아붙는다. 당시의 워킹디렉토리로 돌려버림

git reset 을 통하여 과거로 돌아갔다가 현재로 돌어올 수도 있다.



git checkout xx 를 한 후에는 반드시 git checkout master 를 한 후 다시 commit 을 이어나가야 한다. 



시간여행을 마치지 않고, head가 master를 가르키지 않는 상태에서 새로운 커밋을 하게되면, head는 새로운 버전을 가르키게 되고, 이 상태를 detached 상태라 부른다. 이러한 상태를 경계하여야 한다.



git은 어떤것도 지우지 않는다. .git은 portable-! 완벽 백업!



git reflog > 그동안의 명령어모두 저장.

