브랜치란?
브랜치란 독립적으로 어떤 작업을 진행하기 위한 개념
-> 필요에 의해 만들어지는 각각의 브랜치는 다른 브랜치의 영향을 받지 않기 때문에, 
여러 작업을 동시에 진행 , 다른 브랜치와 병합(merge) -> 하나의 브랜치로 모음!

master branch?
저장소 처음 만들면 master라는 브랜치가 만들어짐
master가 새로운 브랜치를 만들어 선언(checkout)하지 않는 이상 
모든 작업은 'master'브랜치에서 함!

commit -> 시간의 이동
branch -> 공간의 이동 ..평행이동

git branch
->현재 어느 공간인지
git checkout (브랜치네임)
->브랜치 체인지

협업 할 때 브랜치 -> 순차적 코드 정리가 됨!

마무리 하고 브랜치 checkout

git merge (브랜치네임)
->작업한 내용 병합!

git branch -D (브랜치네임)
->다하면 만든 브랜치 없애기

<conflict 충돌 ! >

vi에서 수정한다 ! -"solve conflict! "
**충돌된 건 브랜치 네트워크에 다 찍힘
**정상적으로 merge-> push하면 네트워크에 기록 x

git flow
https://danielkummer.github.io/git-flow-cheatsheet/index.ko_KR.html



git flow init
git feature start 브랜치이름(주로 기능이름)
commit
finish -> merge됨 !

git release start 버전
finish -> develop과 master에 병합됨!


[팀워크 충돌 연습]
git이슈 쓰기 -> 제안 문서화 기타 등등 커뮤니케이션..!

git clone 내 포크 주소 -> origin

-> 폴더 들어가서
git remote add pmorigin  (팀장의 주소) -> pmorigin

develop branch 위에서!!!

git pull pmorigin develop or master

수정하고 commit!

git push origin develop (내포크주소, 내 브랜치)

but!
이후 팀장이 pull받으면 파일이 달라지기 때문에 conflict발생!

충돌 해결-> pull pmorigin해서 다시 commit! -> psuh


git push하고 확인
resitory -> develop ->
pullrequest ->  create pullrequest-> solved # 이슈넘버


팀장 :
develop 취합 완료-> pull origin develop
git checkout master
git merge devleop
푸쉬!

