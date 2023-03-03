<h1>Git 관리 방법</h1>
<h2>Github 시작하기</h2>
1. github에 Repository 를 생성한다.<br>
2. Repository (원격 저장소) 를 연결 한다.<br>
3. add, commit, push를 한다.<br><br>

#
---
#

<h2>기본 셋업 원격 저장소와 로컬 저장소 연결하기</h2>
<h3>$ git init</h3>
현재 폴더를 초기화 (셋업) 한다.
<h3>$ git config --global user.name</h3>
사용자 아이디를 등록, 등록되어있다면 조회한다.
<h3> $ git config --global user.email</h3>
사용자 이메일을 등록, 등록되어있다면 조회한다.<br>
window 기준 자격 증명 관리자를 통해 확인 가능. mac 기준 키체인 접근으로 확인 가능하다.
<h3>$ git remote 별칭 github주소</h3>
원격 저장소와 연결한다.
<h3>$ git remote -v</h3>
연결 정보 확인하기

#
---
#

<h2>파일 업로드</h2>
<h3>$ git add</h3>
Workging tree 에서 Staging area 로 이동 시킨다.
<h3>$ git status</h3>
Working tree 와 Staging area 에 있는 파일들의 상태를 확인한다.
<h3>$ git commit</h3>
로컬 저장소에 등록한다. commit 메시지를 작성할 수 있다.
<h3>$ git push</h3>
로컬 저장소에서 commit된 파일들을 모두 원격 저장소로 업로드한다.
<h3>$ git log --oneline </h3>
commit 정보를 조회한다.
<h3>$ git log --oneline --all --graph</h3>
모든 commit의 정보를 그래프로 조회한다.

#
---
#

<h2>branch</h2>
독립적인 저장소 안에서 작업 후 새로운 버전으로 만들어 낼 수 있다.
<h3>$ git branch</h3>
현재 브랜치 조회 (--list와 같은 기능) 
<h3>$ git branch -all</h3>
원격 브랜치 포함 모든 브랜치 목록 보기
<h3>$ git branch 브랜치이름</h3>
새로운 브랜치를 생성
<h3>$ git switch 브랜치이름</h3>
생성된 브랜치로 이동
<h3>$ git merge 브랜치명</h3>
현재 위치의 브랜치와 입력한 브랜치를 병합한다.
<h3>$ git merge 브랜치명</h3>
기준이 되는 브랜치에 병합하기
<h3>fast-forward merge</h3>
이전 상태의 브랜치가 병합을 통해 최신 상태로 변경되는 것. 단순한 병합.
동시에 여러 브랜치에서 작업을 하는 경우엔 불가능하다.
<h3>3-way merge</h3>
기존의 버전에서 파생된 브랜치의 업데이트와 동시에 기존의 버전도 수정이 된다면 병합시 충돌이 발생한다.
새로운 병합 커밋을 만들어주는 것. ex) 기존 A에서 파생된 B 브랜치. 둘 다 작업이 진행된다면 B가 가져온 버전은 
A의 최신이 아니므로 이 때 C 브랜치를 만들어서 A와 B를 합쳐주는 것
<h3>$ git branch -d 브랜치명</h3>
브랜치 삭제