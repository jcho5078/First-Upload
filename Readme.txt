git init   :   현재 디렉터리를 홈으로 설정..?

리눅스와 비슷함
vim f1.txt : 텍스트 만들고 편집 가는 vi느낌

git status : 버전 관리 여부 확인

git add f1.txt : 버전 관리 시작 = commit 대기 상태로 진입
다시 git status   하면 new file 이리고 나옴

내 이름 부여

git config --global user.name stairs
git config --global user.mail sungdoolim@naver.com
git commit

git log   하면 정보가 나옴
git log -p   : 차이점 출력

편집 :
vim f1.txt 해서 기존 파일 수정후 
git status 하면 modified라 뜬다 빨강색
그후 git add f1.txt해줘야함
그후에 git status하면 modifeid 노랑색
다음 git commit후 버전 써주기 2???

git log  [commit 주소]
그 이전 버젼들의 로그가 나옴
git diff [커밋주소]..[커밋주소]
 : 비교점 출력

기존 파일 편집후
git diff 하면 수정 파일과의 차이 를 보여줌
add 하고난후에는 안보여줌


과거 버전으로 돌아가기
 
git reset [원하는 버전의 커밋 주소] --hard
하면 그 커밋 주소 까지의 버전이 나옴


파일 수정때마다 add 하고 commit 하기 귀찮

git commit --help 로 도움 보기

결론 : vim으로 기존 파일 편집후
git commit -a하면 add된것
git commit -am "[쓰고싶은 말]"    하면 바로 끝
단 한번은 꼭 add가 됬을 경우에만 적용 가능

브랜치
마스터에서 파일 하나 만든후에 실행 가능
git branch
git branch [이름]    = 생성
git checkout [이름]  = 브랜치 사용자 변경(기본 = master)
git checkout -b [이름] = 생성후 변경

브랜치 차이 보기
git log --branches	--decorate --graph --oneline

차이보기
git log master..exp   : master에는 없고 exp에는 있는걸 출력' 
git log -p exp..master : exp에는 없고 master에있는것을 출력해주고
exp에는 없는것이 --로 출력 master에 있는것 ++ 그것의 내용 +로 나옴
  
git diff master..exp



병합
exp의 내용들을 master로 옮겨보자
git merge exp

exp 지우기 
git branch -d exp
같은파일 수정후 병합 = 충돌
다른 파일 병합 = 복붙..?
충돌나면 직접 수정해야함

stash? comiit하지 않고 딴짓 하고 싶을때
파일들 커밋 하지 않으면 따른 브랜치에 있는것도 자동으로 수정적용 됨
커밋해야 각자 사용 가능
git stash 하면 됨(죽이기...?)
git stash apply : 되살리기~
git stash list : 죽인 목록
git stash drop :목록 가장 최신 것 죽이기 0번꺼
git stash pop : apply 되면서 drop도 함

원격 저장소 만들기
git init local
파일 만들기 
git init --bare remote
: 작업은 안되고 저장만 가능한 remote 디렉터리 만듬
git remote add origin /c/Users/bohee/desktop/programming/git/remote
끝에 /가 있으면 안됨 ex ) remote/


origin이 이제부터 경로의 별명이 됨
별명 확인
git remote -v
별명 지우기
git remote remove origin

git push
$ git config --global push.default simple
$ git push --set-upstream origin master
앞으로  push 하면 origin의 마스터로  push 하겠다

그러면 local에 만들어 넣은 파일이 remote에도 있는걸 확인
------------파일 자체가 있는게 아님 git log 했을때 보임cd-----------------------------------


git에 로그인 후 fork 하고 clone or download에서 주소 복사
git clone [주소] [새 디렉터리]



깃에 가입 ->뉴레포짓
mkdir gfh만들고
init 후 파일 추가 커밋 후

두번째 칸에서 첫 줄 복사 후 붙여 넣기
git remote -v 해보기
git remote remove origin 하면 삭제 됨

git push -u origin master
후 로그인
하면 앞으로 push 하면 주소로 올라감

올라간 파일 내려 받기
clone and download에서 주소 복사
새 디렉터리 만들고
git clone https://github.com/sungdoolim/gfh.git .
여기서 . 은 현 디렉터리


commit 메시지 개정 하기 
git commit --amend 하면 vi같이 됨

가져오기
git clone [주소] [폴더이름]
그 안에서 git pull


ssh-keygen
하고 엔터에너터어어어
비번 경로  (/c/Users/bohee/.ssh/id_rsa)
cd ~/.ssh로 가보기
하면 두개 있음 private / public
local 에는 private가 저장됨
원격 저장소에는 public이 저장됨

git tag [태크커멘트] [주소]
커멘트 태그가 달림
git checkout [태크커멘트]


태그 내용 추가
git tag -a [1.1.0] -m "bug fix" [주소]
git tag -v [tag이름] 하면 bugfix 나옴

1.1.0이라는 태그를 주고
git tag -v 1.1.0---------------------------------------
하면 bug fix 출력

태그도 올리려면 git push --tags
삭제
git tag -d 1.1.0


git rebase master
merge와 비슷하지만 더깔끔


















