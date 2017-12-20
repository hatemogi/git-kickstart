# Git 고급 기능과 실전 상황별 예제와 실습

## git commit --amend

## 로그 보는 옵션

    $ git log --pretty=oneline
    $ git log --pretty=oneline --all
    # The --all flag makes sure that we see all the branches. The default is to show only the current branch.
    $ git log --pretty=oneline --since='5 minutes ago'
    $ git log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short

## 앨리어스 걸기 - 어떻게?

    hist = log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short

## git reset --soft / --hard

## git stash

## git push -f

## 충돌 해결하기

## 이전 버전으로 되돌려서 재작업하기

* 이전 커밋으로 가기
* 특정 커밋으로 가기
* 태그로 가기

## 개발 브랜치에서 배포 브랜치로 돌아가서 핫픽스 적용하기

## 체리픽

## 여러 저장소 같이 쓰기

어떤 상황?

## 계정 여러개

## git bisect
