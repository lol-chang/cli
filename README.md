# git CLI 명령어 간단 정리

</br>

## Initialize

# git clone 주소
새로운 프로젝트를 시작할 때는 먼저 git clone을 사용하여 원격 저장소를 복제

# git remote add origin https://github.com/lol-chang/cli.git
이미 존재하는 로컬 저장소에 원격 저장소를 연결할 때 git remote add origin을 사용

# git init
현재 디렉토리에 새로운 Git 저장소가 만들어지며, 해당 디렉토리 안의 파일들이 Git으로 관리되기 시작

</br> 

# git status 
어떤 파일이 스테이징 영역에 추가되었는지 확인 
### 스테이징 영역(Staging Area)이란, 
Git에서 커밋을 만들기 전에 변경 사항을 일시적으로 저장하는 공간
-> 변경된 파일들 중 어떤 것을 다음 커밋에 포함할지 선택하는 중간 단계 

# git log
현재 커밋 상태 확인 

# git add . 
.은 전체 
add는 커밋 전, 워크스페이스의 모든 변경 사항을 스테이징 영역에 추가하는 명령어


# git commit -m “initial commit”
커밋 

# git reset —hard
마지막 커밋 상태로 이동 

# git reset —hard 커밋코드
해당 커밋코드 상태로 이동 

</br>


# git push origin main
github로 푸쉬 

# git pull origin main 
github page에서 변경사항이 생겨서 내 로컬로 가져오기
(pull해도 로컬에서의 변경사항은 그대로 유지 가능)
현재 상태에서 pull되는 파일만 추가되는 거임

</br>
</br>

# [브랜치를 모르는 상태에서 협업이 가능하다.]
서버에서 항상 pull(변경사항 적용)을 해오고 
커밋(push)을 하면  
*(서버 작업 내용이 적용된 후, 로컬 작업이 적용되어 push하는 느낌)

</br>

여기서 conflict가 발생하면, 직접 conflict 해결해야 한다. 
conflict - 같은 파일의 같은 라인을 동시에 수정하면 문제 발생

</br>

# [항상 pull하기는 귀찮다.] → branch 활용 

나눠서 개발해서 나중에 합치자 
합치기 요청 : PR 
PR을 수락하면 두 코드가 합쳐서 merge됨

</br>

# git branch 
# git branch [branch_name]
브랜치 생성

# git checkout [branch_name]
브랜치 변경

# git push origin [branch_name]
github 메인 브랜치로 푸쉬 

</br>
</br>

# [Fork] - 오픈소스 프로젝트 복사하기 
오픈소스 PR 요청이 받아지면 contibutor 됨 

</br>

# 깃허브 푸쉬 메시지 알림 TMI - 협업 시, 도움됨 

## PR 요청을 github 페이지에서만 확인하기 귀찮다. 
Slack을 이용 
[slack에서 해당 프로젝트 구독해야 함 ]
채팅창에 
## /github subsrcibe 유저네임/레포네임 
ex> /github subsrcibe lol-chang/cli  

# git pull 시, merge 방식을 정해줘야 함 
임시 세팅이라,
향후 global로 하든지, 프로젝트마다 적용시키던지 해야 함.  
참고: https://eocoding.tistory.com/108
