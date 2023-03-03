<h1>Git 관리 방법</h1>
<h2>Git 명령어</h2>
1. github에 Repository 를 생성한다.<br>
2. Repository (원격 저장소) 를 연결 한다.<br>
3. add, commit, push를 한다.<br><br>

#

<h2>기본 셋업</h2>
<h3>$ git init</h3>
현재 폴더를 초기화 (셋업) 한다.
<h3>$ git config --global user.name</h3>
사용자 아이디를 등록, 등록되어있다면 조회한다.
<h3> $ git config --global user.email</h3>
사용자 이메일을 등록, 등록되어있다면 조회한다.<br>
window 기준 자격 증명 관리자를 통해 확인 가능. mac 기준 키체인 접근으로 확인 가능하다.

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
<h3>$ git remote 별명 github주소</h3>
원격 저장소와 연결한다. window는 아이디와 비밀번호로 연결 (* mac은 따로 설명 첨부)
<h3>$ git log --oneline </h3>
commit 정보를 조회한다.