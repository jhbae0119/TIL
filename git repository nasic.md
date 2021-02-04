# 원격저장소 기초 활용

* github을 기준으로 설명하지만 원격 저장소를 제공하는 서비스는 많다



# 0. 준비

* github에서 새로운 원격저장소 만ㄴ들기



## 원격 저장소 설정

```bash
$ git remote add origin __주소__
```

* 로컬 저장소에셔 원격 저장소를 지정

* git아 원격 저장소(`remote`)를 주가(`add`)해줘.  `주소`를 origin이라는 이름으로

* 원격저장소 확인

  ```bash
  $ git remote -v
  origin  https://github.com/jhbae0119/first.git (fetch)
  origin  https://github.com/jhbae0119/first.git (push)
  ```

* 원격저장소 삭제

  ```bash
  $ git remote rm origin
  ```





# 1. push

```bash
$ git push origin master
```

* `origin`으로 지정된 곳에 `master` 브랜치 push