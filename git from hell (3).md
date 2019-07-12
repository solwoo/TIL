.git 속에는...

.\HEAD - 헤드 정보

.\config - 사용자정보

.\info\exclude

깃은 중복에 강하다.

내용을 기반으로 이름이 만들어 짐 -> 해싱

똑같은 내용이면 이름이 같을 수 밖에 없다.

Tree(commit 파일은 무엇이 있고, 내용은 어떻다), commit, 내용



add라는 행위는 [index] index 파일에 올리는 것이다.

데이터 구조상, index라는 파일에 등록하는 것이다.

그래서 스테이지, 인덱스, 캐쉬 세가지의 표현으로 불린다.

같은 내용인데 표현이 다른 것 뿐이다.



도메인 날리쥐 , 개발을 사람, 협업을 잘하는 사람. => 프로젝트에 힘이 있는 사람

Fast foward : 금방 병합한다.

merge commit : merge시 충돌이 없으면 commit까지 해준다.



accept both charges : 적당히 섞어주지만, 코드 점검 필요

> git add xx > 나 complicit 해결했어
>
> git commit > editor가 열리는데, Merge bla bla 라고 메시지가 작성되어 있음. #으로 시작하는 부분은 메시지로 입력이 안된다. 첫번째 줄은 보존하고 다른 메시지가 있을 시 두번째 줄에 적어라.



git merge tool > 비교도구가 실행된다. p4merge다운로드. (기본 병합 도구)

2way merge < 3way merge (rebase, reverse, merge, cherrypicked 할때 필요함)



# 백업

인터넷에 있는 저장소 하나 하나를 호스트라 부른다.

깃 호스팅!

개발자의 3대 성지 google, Stack overflow, GitHub(부품 소프트웨어)



로컬리포에게 리모트리포가 누군지 알려줘야 한다.

1. 경로가 어딘지 알아야한다.
2. 어떤 통신 방법을 쓸거야? Https / ssh 중 선택
3. 처음부터 동기화 할거야? 아님, 나중에 할거야?
4. 읽기건 쓰기건 인증이 필요하다. 



ssh 사용법

1. local에 패스워드를 만든다.(ssh_key)
2. 리모트에 패스워드를 알려준다.

1. Ssh-keygen > 지금부터 패스워드 만들거야. enter enter enter 어디에 만들어야~~
2. 숨겨진 파일 보여주는 단축키로 cmd shift . > .ssh 폴더로 들어간다.
3. .pub(public의 약자) 와 아닌애가 짝꿍 키 -> 두가지 파일이 만들어진다. .pub이 안붙어 있는 파일은 절대적으로 노출되서는 안된다.(공개키, 비공개키)
4. .pub를 github에 올린다.(내용을 카피)
5. github의 Settings > SSH and GPG keys > ssh key 등록
6. Ssh 주소 복사
7. 커맨드 라인데 git remote add origin 주소 (origin 대신 다른걸 써도 됨. 관습적으로 origin을 씀) > 내 원격저장소 이거야 : ssh 주소가 길어서 origin을 쓴다. 리모트야 내 ssh 비번 주소를 알려줄게.
8. 지금까지의 것들을 원격저장소로 푸쉬해 > git push > 최초 1회에 한하여 master 누구 브랜치로 선택할지 선택 > git push --set-upstream origin master > 지역저장소가 어디로 스트림될것인지 셋한다.
9. 리모트트래킹브랜치가 생김 > origin/master > 어디까지 동기화 됐는지 확인할 수 있음



Git push > 	원격저장소로 전송이 된다. 트래킹을 해준다.





# right의 등장!!

Setting > collaborators > id 추가 > push할 수 있는 권한이 생긴다

git init,,, 등 원시적인 부분을 묶어주는 것 >	git clone 주소 .(현재 디렉토리) >	원격저장소를 현재디렉토리로 클로닝한다. >	오픈소스 내꺼로 가져와서 보고싶다!!



git add . >	모든 파일 add!

right가 먼저 push를 했을때, left가 달라지면 push를 reject 당한다.

그렇게 되면 pull or fetch를 한다. (pull > petch, pull = petch + merge)

다음 oriin/master를 merge한다.

그런 후 다시 push



trancking vranch



rm file



오픈소스에 참여할 때는 먼저 커뮤니티에 참여하데에 의미를 둔다.



한 줄로 정렬하고 싶은 것 > rebase >	대신 머지의 결과와 리베이스 결과가 같아야만 한다.

Revert D > 그만큼의 변경사항을 취소한 버전 E를 생성. 이미 올라간 내역은 못 바꾼다. 숙명 같은 것. 해당 작업만 취소하겠다. 3way merge 적용.



깃 = 이뮤터블, 로컬 밖으로 동기화되지는 않음







