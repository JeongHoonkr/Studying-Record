## Git 기초

작업디렉토리 = 워킹트리



커밋 = 저장 save

커밋하면 로컬 깃저장소에 들어감, 

.git은 로컬저장소 : 커밋으로 저장할때 건드린다.



원격저장소에 저장하는것이 push



클론 : 원격저장소를 로컬저장소로 옮겨오는 작업



(- -) 붙히는건 옵션



원격저장소를 깃헙 사이트에서 만들고 로컬을 만들기 위해서는

원격저장소 링크를 터미널에 복사한다 이를 클론한다고 한다.



cd 폴더이름 원격저장소링크

mkdir someGit

git init -> .git이 생김



로컬디렉토리 -add> 스테이지 -commit> 로컬저장소  -push> 원격저장소

​                                                                 로컬저장소  <fetch- 원격저장소

 로컬디렉토리—————————<pull————  ------------원격저장소                                     

되돌린다는건 로컬저장소에서 로컬디렉토리로 되돌린다는것 (체크아웃)



git log그동안의 커밋이 나타남

현업에서 작업시 master는 실제 서비스가 돌아가는 공간을 말한다

개발자끼리의 작업은 develop



서로다른걸 하나로 합치는걸 머지라고 한다.

커밋-다른누군가의 상태

머지한것은 커밋이아니라 메타커밋이라고함

푸시는 내 현재저장소를 원격에 올림

origin은 원격저장소

git push origin master

git commit 만 하면 길게 메세지를 넣을 수 있다

Add some commit (하고 아래줄에 메세지넣기)

현재 브랜치영역은 앞에 *가 부틈 = head = 가장 마지막의 참조 (체크아웃했을떄도 옮겨감)

checkout은 특정커밋을 꺼내서 브랜치명적힌곳으로 옮겨주는것

git commit한다는건 현재의 head에 자식을 만들어주는거

브랜치생성 : git branch 브랜치이름

생성한 브랜치로 이동 -> git checkout 생성한 브랜치

브랜치 = 객체의 참조

항상 마스터에선 작업하면안되고 브랜치를 따서 성공하게 되면 마스터로 올린다

git merge 합칠브랜치

깃에선 커밋이 객체고 다른것들은 다 참조다.

branch 객체이름 만들브랜치이름

head가 가르키고 있는 객체로부터 새로운 객체를 생성

그리고 commit을 통해 head가 새로운 객체를 가르키게 한다.

a1 (커밋) a2 (커밋) a3 : dsdsdsd / 



git tag 태그이름 객체이름  (tag도 참조)

(태그는 움직이지않는다, 브랜치는 이동가능)



커밋단위는 작은단위로 한동작의 의미로 작게작게 하는게 좋다.

mergge는 커밋2개를 합쳐서 새로운 커밋을 만들어주는것

리베이스는 내 브랜치와 머지할 브랜치들의 차이점을 들어서 대상에 ? (마스터에서는 리베이스하는거 아님)

git branch -d 지울브랜치이름



pr하는 이미지다 base는 나의 저장소 -> 컴페어는 사다리를 위해 브랜치 생성한 장소다

![pr하기](http://postfiles13.naver.net/MjAxNzEwMzBfMTkx/MDAxNTA5MzQ0MTY2MDM3.UCebLz4N-jV31MjZ0HZmXb3Zy6mNpJWSCuTIaxtqBz8g.5y-2IkuQezvaDI5DSy4QMATHN7-tOXTCj6T_jcRbFBog.PNG.bb_9900/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2017-10-30_%EC%98%A4%ED%9B%84_3.09.41.png?type=w773)

