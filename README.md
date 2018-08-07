# GIT 튜토리얼!


## 시작하기 전에..
다음 두가지를 꼭 해주세요  
- github에 가입하기  
- git 설치하기

## github 둘러보기

### Issue 탭
[튜토리얼 프로젝트의 이슈탭](https://github.com/SexyTreeTrunks/git-totorial/issues)에서 New issue 버튼을 눌러 글을 작성해보기

### Insight  탭
프로젝트 진행에 대한 상세정보 확인  


## git 사용법
이 문서는 자주쓰는 명령어에 대해서만 간략하게 설명이 되어있습니다   
자세한 설명은 [여기](https://backlog.com/git-tutorial/kr/intro/intro1_1.html)를 참고하세요!  
git bash 라는 프로그램을 찾아서 실행하세요

### git config
git 설치했으면 반드시 해야함!  
`git config --global user.name "자신의이름"`  
`git config --global user.email 깃허브가입한@이메일주소`

### git clone
[이클립스를 통해 git clone하기](http://codedragon.tistory.com/49)

혹은    
`git clone https://github.com/SexyTreeTrunks/git-totorial`

### git branch
git에서 branch란 새로운 버전을 의미합니다. 말빨이딸려서 설명을 잘 못하겠으니 제가 참고하라고한 링크에서 잘 읽어보세요

브랜치 생성  
`git branch 브랜치이름`

브랜치로 이동  
`git checkout 브랜치이름`


----------------------------
여기부터 파일을 수정한 뒤 사용하는 명령어들입니다 

---------------------------

### git status
현재 브랜치와 파일 상태 확인  
`git status`

### git diff
파일 수정후 변경내용 확인할때 씀  
`git diff`

### git add

`git add 수정한파일이름`

### git commit

`git commit -m "커밋 메세지"`

### git log

`git log`

----------------------------
여기부터 변경내용을 원격저장소에 업로드하거나 다른 사람이 올린 코드와 합칠때 사용하는 명령어들입니다

---------------------------


### git fetch
`git fetch origin 다운로드할브랜치이름`

### git merge
`git merge --no-ff 합칠 브랜치 이름`

> #### 명령어를 쳤는데 **merge conflict**가 뜰경우  
> master브랜치에서 수정한 부분과 자기브랜치에서 수정한 부분이 충돌할때 나는 에러임!   
> [여기 참고!](https://opentutorials.org/module/2676/15275)


### git push
`git push origin 업로드할브랜치이름`


## git level-up!
git를 맛본후 더 다양하게 git를 사용해보고싶은 분들을 위한 명령어, 혹은 git를 사용하면서 기본기능으로 해결할수없는 예외상황들을 해결할수있는 명령어들이 있습니다.  

### git init
git를 설치했다고해서 모든 프로젝트들을 관리할수있는게 있는게 아닙니다.  
해당프로젝트를 git가 관리할수있는 프로젝트로 만들어주어야 하는데요,  
이때 사용하는것이 `git init`임니다  

### git checkout 
우리는 앞서 git checkout을 브랜치를 이동할때 사용했습니다.  
`git checkout 브랜치이름` 으로하면 해당 브랜치로 이동이 됩니다.  
하지만 `git checkout -- 파일이름` 으로하면 해당 파일에서 변경한 내용을 모두 없앨수있습니다.  
(단 git add 혹은 git commit하기 전 상태여야합니다)

### git reset
git reset은 git add 혹은 git commit을 취소할때 사용하는 명령어 입니다.  
프로젝트를 하다보면 git add로 잘못된파일을 추가해서 add를 취소해야하거나,  
commit한 코드에 에러가 있어서 commit을 취소해야하는 슬픈 일이 생겨날수있습니다.  
여러분은 부디 이 명령어를 쓸일이 없길 바랍니다.  

#### 실수로 잘못된파일을 git add 한 경우
먼저 `git status`로 git add한 파일들의 목록을 확인하세요!  
`git reset HEAD 파일이름` 으로 git add를 취소해보고 `git status`로 다시 확인해보세요!  

#### git commit을 취소해야할 경우
먼저 `git log` 로 커밋 목록을 확인해보세요!  
커밋을 취소할때도 git reset HEAD 명령어를 사용하는데요,    
`git reset HEAD^` 명령어를 치게되면 전 커밋상태로 돌아가게 됩니다.   
`git reset HEAD^^` 명령어를 치게되면 전전 커밋상태로 돌아가게 됩니다.     
`git reset HEAD^^^` 명령어를 치게되면 전전전 커밋상태로 돌아가게 됩니다.   

또한 커밋을 취소할때 --soft 옵션과 --hard 옵션이 있는데요,  
`git reset --soft HEAD^` 하면 **커밋만 취소**되고 파일내용은 그대로 남아있습니다.  
`git reset --hard HEAD^` 하면 **커밋이 취소**되고 **파일내용이 이전 커밋의 상태**로 완전히 바뀝니다.  

**따라서 커밋기록만 취소하고싶으면 --soft옵션을, 파일내용까지 이전상태로 되돌리고싶다면 --hard 옵션을 써서 git reset하시면 됩니다.**  


## 과제

### 코드 수정&업로드
1. git clone을 이용하여 원격저장소에 있는 코드를 자신의 컴퓨터에 저장하기
2. git branch로 새로운 브랜치를 만든다(**브랜치 이름은 자신의 영문이름으로 할것!**)
3. git checkout을 이용하여 자신이 만든 브랜치로 이동한다
4. git add를 이용해서 코드를 수정한다.
5. git commit을 이용해서 수정한 코드를 저장한다.
> ** ※ 주의사항**  
이 과제에서 git add와 git commit은 코드를 한꺼번에 수정하고 하시면 안됩니다!  
'수정할코드' 부분 수정하고 commit,  
'새로작성한코드' 부분 수정하고 commit,  
'삭제할코드' 부분 수정하고 commit,  
이렇게 총 3번의 commit이 있어야 합니다
6. git push를 이용하여 원격저장소에 수정사항들을 업로드 한다

### 업로드 확인하기
github에 [Insights - Network](https://github.com/SexyTreeTrunks/git-totorial/network) 탭에서 진행모양을 확인해본다


### 코드 합치기
* git pull을 이용하여 master브랜치에 수정사항을 다운로드 한다
* `git merge --no-ff 자기브랜치이름` 으로 브랜치를 합친다
* `git log --oneline --graph` 로 브랜치가 합쳐졌는지 확인해본다
* 잘 합쳐졌으면 git push를 이용하여 master브랜치를 업로드한다

## 레벨업 과제
이 레벨업과제는 하셔도 되고, 안하셔도 됩니다.  
시험이 끝나고 난뒤에 혹은 프로젝트가 끝나서 여유가 있으신 분들은 나중에 한번 해보세요.  

### 자바수업때 만든 코드들을 github에 업로드해보기
1. github에 들어가서 새로운 원격저장소를 만든다  
- github에 들어가서 [new repository](https://github.com/new) 를 클릭한다  
- 원격저장소의 이름과 설명을 쓰고, 하단에 `.gitignore 추가` 버튼을 클릭하여 java로 설정한다  
- repository 생성 버튼 클릭하여 생성을 완료한다  

2. git bash를 켜서 자바프로젝트가 있는 폴더로 이동한다
3. `git init` 을 한다
4. `git add *` 로 전체 코드파일들을 커밋 목록에 올린다
5. `git commit`을 이용하여 저장한다

이렇게 하면 여태까지 만든 자바 코드들이 모두 하나의 커밋으로 저장이 됩니다.

> #### ※ 만약 패키지별로 커밋을 하고싶다면?  
> 1. 우선 프로젝트 소스폴더로 이동 (cd 프로젝트폴더/src)  
> 2. `git add 패키지폴더명/* `  
> 3. `git status` 로 확인을 해보면 해당 패키지에 있는 파일들만 new file로 추가된것을 볼수있습니다  
> 4. `git commit `으로 커밋   
> 위와 같은 commit 작업을 각 패키지마다 해주면 됩니다  

6 `git remote add origin 자신이만든원격저장소의링크` 로 원격저장소의 링크를 프로젝트에 등록한다  
7 `git push -u origin master` 로 원격저장소에 커밋 업로드  

