# GIT 튜토리얼!


## 시작하기 전에..
다음 두가지를 꼭 해주세요
* github에 가입하기
* git 설치하기

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
`git merge 합칠 브랜치 이름`

> #### 명령어를 쳤는데 **merge conflict**가 뜰경우  
> master브랜치에서 수정한 부분과 자기브랜치에서 수정한 부분이 충돌할때 나는 에러임!   
> [여기 참고!](https://opentutorials.org/module/2676/15275)


### git push
`git push origin 업로드할브랜치이름`


## github 사용

### Issue 탭
[튜토리얼 프로젝트의 이슈탭](https://github.com/SexyTreeTrunks/git-totorial/issues)에서 New issue 버튼을 눌러 글을 작성해보기

### Insight  탭
프로젝트 진행에 대한 상세정보 확인  



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
* `git merge 자기브랜치이름` 으로 브랜치를 합친다
* 잘 합쳐졌으면 git push를 이용하여 master브랜치를 업로드한다


