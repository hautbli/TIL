git 시작하기!
git 설치 -> windows는 공식 홈페이지 x- > git for windows 에서 설치 

깃 계정 설정
git config --list
깃 이름 설정
git config --global user.name "유저네임"
이메일 설정
git config --global user.email "이메일"

에디터와  cat설정
git config --global core.editor "vim"
git config --global core.pager "cat"

1. 로컬 -> github
git폴더 설정 
git init -> local repository로서 역할을 시작

로컬 -> Url  별칭 설정 
git remote add puppy remote repository


파일 생성
touch README.md
vi README.md
파일 보기
cat README.md

to index	
git add README.md

to local repository
git commit-> 
commit 메시지를 작성or  git commit -m "커밋메시지"

커밋메세지 말머리에 맞게 작성 
feat: 새로운 기능 추가
docs : 문서수정
test : 테스트코드, 리팩토링 테스트 코드 추가
refactor : 코드 리팩토링
fix : 버그 수정


Git status계속 확인 ~ 
remote repository 에 추가
git push -u puppy master (u처음에만)
u-> set upstream 


2.git clone

Git hub에서 remote repository 생성
주소 복사

git clone remote repository

cd 생성된 폴더로 
파일 생성
touch README.md
vi README.md

git add README.md
git commit
git push origin master

remote repository에서 먼저 끌어와 사용하는 구조
remote repository의 master 브랜치와 local repository의 master 브랜치연결된 상태이므로 -u를 안해도 됨




