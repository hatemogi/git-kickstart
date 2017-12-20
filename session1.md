# 분산 버전 관리 시스템 개념과 Git 기본 명령어

* 버전 관리 시스템이 무엇이며 왜 유용한가?
* Git은 어떤 버전 관리 시스템인가?
* Git의 기본 명령어를 알아보자. (CRUD)
* 영역 소개 (working/stage/history)
* 로컬 / 리모트 저장소가 무언가?

## 커맨드 라인 툴로 기본을 배웁니다

* 이유 - 다양한 툴이 있고, 사용법은 조금씩 다르지만 기본은 같다
* GUI 툴이 나은 경우

## 학습 주요 명령어

git config
git init
git add
git rm
git mv
git reset
git commit
git log

## git 설치 확인

    $ git version

## 기본 설정

    $ git config --global user.name "홍길동"
    $ git config --global user.email "hong@gil.dong"
    $ git config color.ui true

    $ git config --global core.quotepath false
    $ git config --global core.precomposeunicode true
    $ git config --global push.default simple

## 저장소 (repository)

초기화

    $ git init

현 상태 확인

    $ git status

stage/unstaged/untracked/deleted

첫 파일 준비

    hello.html

인덱스 영역에 추가

    $ git add hello.html

현 상태 확인

    $ git status

커밋 (스테이지 -> 히스토리)

    $ git commit -m "add an html file"

텍스트 파일 여러개 추가

    $ git add '*.txt'

히스토리 로그 확인

     $ git log

리모트 저장소 추가

    $ git remote add origin https://github.com/try-git/try_git.git

git push -u origin master
git pull origin master
git diff HEAD
git add assets/main.js
git diff --staged
git reset assets/main.js
git checkout -- hello.html
git branch clean_up
git checkout clean_up
git rm '*.txt'
git commit -m "remove all the text files"
git checkout master
git merge clean_up
git branch -D clean_up
