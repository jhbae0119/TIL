# git 기초

> 분산 버전 관리 시스템(DVCS)

## git 저장소(repository) 초기화	

```bash
$ git init
Reinitialized existing Git repository in C:/Users/puppy/OneDrive/바탕 화면/git_practice/first/.git/
```



* `.git`숨김 폴더가 생성되고, bash환경에서는 (master)로 branch 정보가 나타난다.



# 작업 흐름

## 1. `add`

현재 작업 중인 파일의 변경사항을 `staging area`로 변경(이동)

* staging area: 커밋(버전)으로 기록할 대상의 파일 목록

```bash
$ git add .				$.현재 디렉토리
$ git add a.txt			$ 특정 파일만
$ git add myfolder/		$ 특정 폴더	
```





> add 전

```bash
$ git status
On branch master
Untracked files:	# 트래킹이 되고 있지 않는 파일
  (use "git add <file>..." to include in what will be committed) #git add를 사용해 staging area로 이동시켜야 함
        12.txt

nothing added to commit but untracked files present (use "git add" to track)
```



> add  후

```bash
puppy@LAPTOP-2M3O3N6V MINGW64 ~/OneDrive/바탕 화면/git_practice/first (master)
$ git add .		# add 실행

puppy@LAPTOP-2M3O3N6V MINGW64 ~/OneDrive/바탕 화면/git_practice/first (master)
$ git status
On branch master
Changes to be committed:	# commit이 될 변경 사항들 목록
  (use "git restore --staged <file>..." to unstage)
        new file:   12.txt
```



## 2. commit

변경 사항을 버전으로 기록

```bash
$ git commit -m 'commit_message'
[master 958f097] commit_message
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 12.txt
```

* 특정 시점을 스냅샷처럼 기록한다
* commit 시 메시지 작성 tip
  * 지금 기록한 코드의 이력을 나타낼 수 있도록 해야함



## 3. log

지금까지 기록된 commit들을 확인 할 수 있음

```bash
$ git log
commit 958f097c2bbe9d6e1dba79177f58e56626825f32 (HEAD -> master)
Author: jhbae <puppy119@naver.com>
Date:   Thu Feb 4 14:10:55 2021 +0900

    commit_message

commit 3a844170cc26308cf5bc231a7c99b0c0939042af
Author: jhbae <puppy119@naver.com>
Date:   Thu Feb 4 11:29:11 2021 +0900

    firstCommit

$ git log --oneline		# 한줄로 간략하게
$ git log -2			# 최근 2개
$ git log --oneline -1	# 최근 1개를 한줄로
```



## 4. status

git 저장소의 파일 변경 사항 등을 확인

```bash
$ git status
On branch master
nothing to commit, working tree clean
```

