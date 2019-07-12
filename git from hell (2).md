git은 제품군.

CLI - 오리지널 깃: 

.git을 이용하는 다양한 제품들이 존재한다. 취향대로 선택 가능. ex) 토토 이즈 깃

* status와 log를 통해 상태와 역사를 지속적으로 확인하는 것이 중요

.git 하면 생기는 것이 repo(저장소) => git directory라고 부른다.

Stage area를 도입하여 commit 대기상태를 만들어 놈. 그것이 add.

git diff > add전에 바뀐 점 확인. 어떤 작업을 했고, 문제는 없는지 마지막으로 리뷰할 수 있는 굉장한 기회이다.

git reset —hard master/HEAD/생략 > 마지막 버전 이후로 수정한 모든 내용이 사라진다.

 

커밋 아이디의 메타 정보 : 내용, 메시지, 부모...



Head: 지금의 워킹카피가 어디인지?

Master: 마지막 커밋은?



# branch

### 3 way merge

버전관리 : 파일의 이름을 더럽히지 않으면서도, 이력관리를 하고 싶다.

Ex) 현대 비엠더블유 벤츠로 나누기 => 브랜치 생성

활용 예시) 종량제봉투에 물건 넣어놓고 안쓰면 버리듯, 브랜치 생성 후 작업하다가 필요없으면 버린다.



head가 branch에 붙어있을 때는 attached.

head가 branch에서 떨어져 있는 경우 detached.



git branch exp > exp라는 브랜치를 만들어. head가 가르키는 버전을 가르키는 새로운 브랜치가 만들어짐. 이상태에서 커밋을 한다.

git branch > branch에 대한 리스트를 보여줘

git log —online —all —graph > 좀 더 보기좋게 보여줘 (브랜치 내용을 그림으로 보기 좋게 보여줌)



b라는 버전을 새로 만들시, if(attached? Detached?) 



HEAD는 checkout 으로 브랜치 간 이동



git merge XX > 머지하고 픈 브랜치에서 머지 할 브랜치를 땡겨오는 느낌

일단 헤드가 마스터를 가르키가 한다 > 그런다음 merge를 이용하여 이엑스피의 것을 당겨오기

머지 후, 새로운 버전이 만들어지면서, 병합

git branch -d exp > branch exp를 지워줘 무조건 지원! 할때는 -D

git commit -am "" > Commit 할 때 add 하기 귀찮으면 untracked상태의 파일은 자동 add 불가능하다. 깃은 명시적으로 트랙킹 하기 전에는 알아서 트래킹하지 않음. 그래서 최초 add를 해주지 않으면 안된다.



git merge —abort  > 머지 취소



