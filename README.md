기존 프로젝트를 git repository에 연결하기
======================================
### 1. 터미널에서 기존 프로젝트폴더 위치로 이동
### 2. git 초기화
```
git init
```
### 3. 프로젝트를 연결 할 github repository 생성(README 등 파일 생성 없이 빈 레포지토리로 생성 권장)

README 파일을 생성하면 최초 커밋 시 파일 기록이 달라서 오류발생할 확률 있다.

### 4. repository 연결
```
git remote add origin "프로젝트 주소"
```

연결된 repo 확인 (fetch / push 주소 확인)
```
git remote -v
```
### 5. repository 원격 브랜치로 commit, push 하기 (파일 업로드)
```
git add .
git commit -m '커밋내용'
git push origin main
```

이렇게 진행하면 git에 생성한 repository에 원격 브랜치 main이 생성되며 업로드된다.

* 참고: https://velog.io/@hyo123/Git-%EA%B8%B0%EC%A1%B4-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EB%A5%BC-git-repository%EC%97%90-%EC%97%B0%EA%B2%B0%ED%95%98%EA%B8%B0
* 마크다운 참고: https://velog.io/@gmlstjq123/Readme.md-%ED%8C%8C%EC%9D%BC-%EC%9E%91%EC%84%B1%EB%B2%95

동빈나 깃허브 유튜브
============================
### 1. 깃허브에서 remote repository 만들고
### 2. 로컬에서 폴더 만들고 
### 3. cmd 그 로컬 폴더 위치로 이동하고 git clone 주소 입력하면 연동됨 ( 로컬 폴더 안에 연동된 repository가 생성된다 )

   git clone은 다운로드 느낌
### 4. cmd 로컬 폴더 안에 연동된 repo 위치로 이동하고
# 명령어
* 파일 생성하거나 파일 내용 변경하면 git add 해야 commit 가능,     여러개는 git add .
* git add 파일명 -> staging area에  수정된 내역을 올려준다.
* git commit -m  "설명하고싶은 내용"
* git commit --amend  ->  commit 내용수정
* git status ->  변경사항확인 
* git push - > remote(깃허브) repository에 올리기
* git push -f -> 깃허브 저장소에 로컬 저장소와 완전히 동일하게 만들 수 있다
* git log  -> 깃 로그 내역 확인,   q로 나올수 있다
* git reset --hard 커밋 해쉬값(git log로 커밋 해쉬값을 알 수 있다) -> 해당 커밋지점으로 이동하고 이후의 발생한 커밋들은 삭제한다.
 
* git branch -> 브랜치 목록확인
* git branch 브랜치명 -> 새로운 브랜치 생성
* git branch -d 브랜치명 -> 해당 브랜치 제거
* git checkout 브랜치명 -> 해당 브랜치를 헤드(*)가 가리킴,  해당 브랜치로 이동
* git merge 브랜치명 -> 해당 브랜치를 합친다

* git log에서 origin은 깃허브 레포지토리가 가리키는 것을 의미한다.
* 브랜치 끼리 merge할 때 특정한 소스코드의 라인이 다르면?(소스코드가 다르면) confilct(충돌)이 발생해 직접 충돌이 난 코드를 확인하고 사용할 코드만 남긴다. 그리고 git add와 commit, merge진행
