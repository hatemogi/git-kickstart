class: center, middle

![](img/logo@2x.png)
## Kickstart

---

# 김대현

* 프리랜서 서버 개발자
* Daum 카페, 캘린더, 마이피플 개발
* __사내 Git 저장소 시스템 구축 & 운영__
* Clojure, Ruby, Java
* 한국 개발자를 위한 플랫폼 구축에 관심

.footnote[
[Medium](https://medium.com/@hatemogi)
[Twitter](https://twitter.com/hatemogi)
[GitHub](https://github.com/hatemogi)
[개인홈](https://hatemogi.com)
]
---

# 대상

* 버전 관리를 아직 안하는 개발자
* Git에 관심은 있지만, 아직 기회가 닿지 않은 분

---
# 목표: Kickstart

.full-width[[![](img/kickstart.png)](https://youtu.be/olBM1U5bO7Y?t=8s)]
버전관리 & Git 사용 설득
---

# 차례

1. 버전 관리가 필요한 이유
1. Git이 좋은 점
1. Git 개념 파악
1. 시각화 도구로 연습
1. CLI 실습

---

class: center, middle, inverse

# __기__ 승 전 결

개인 경험 이야기

---

# 2000년 - 버전관리 lv.0

* 물류 IT 회사
* 전자문서 중계 클라이언트/서버
* __대형 고객사 ← 클라이언트 프로그램을 대신 개발해서 설치해 줌__
* 같은 일을 하는 클라이언트 프로그램 OO개

## 버전을 관리하는 방법
```bash
tar -cvzf [백업파일-날짜.tgz] [소스DIR]
cp -R [소스DIR] [적당한-새이름]
```

---
# 2004년 - 버전관리 lv.2

* Daum 카페 개발팀 입사
* 개발팀만 10+명
* CVS([Concurrent Versions System](https://en.wikipedia.org/wiki/Concurrent_Versions_System)) 사용

## 기대 효과

* 개발자간 소스코드 동기화 (sync)
* 서비스 배포시 tag달기
* 누가 이 코드를 짠 건지 확인

> 거봐요, 당신이 커밋한 거잖아!

---

# 2008년 - 버전관리 lv.3

* Daum 캘린더 개발 TFT
* 사내 표준 VCS 시스템 - Subversion (SVN)
* SVN - CVS의 단점을 극복
  * atomic 커밋: 모 아님 도
  * 파일명 변경 추적
* 중앙집중 SVN 서버 → 수백 명이 접근
* SVN에서 브랜치 → 쓰면 안 되는 거.

.footnote[[다음 캘린더 서비스 개발 비하인드 스토리](https://medium.com/happyprogrammer-in-jeju/다음-캘린더-서비스의-비하인드-스토리-ec0faac67f05)]
---

# 2012년 - 버전관리 lv.4

* 사내 Git 저장소 시스템 구축
* Git을 쓰니 비로소 브랜치를 쓸 수 있게 됨
* 배포 / 개발 / 핫픽스 / UI 브랜치 병행 가능
* 분산 버전 관리 → 로컬에서 빠르게 할 수 있는 일 다양

.footnote[[사내 Git 저장소 개발사례](http://www.slideshare.net/hatemogi/devon2013-git)]

---

# 2016년

.center[[![](img/DiffusionOfInnovation.png)](https://en.wikipedia.org/wiki/Early_adopter>)]

* Quiz: 우리의 위치는?

---
# 요약 - Git을 알아야 하는 이유

* 소스코드
  * 잃어 버리면 안된다 → 백업
  * 계속 바뀐다 → 이력 추척
  * 여럿이서 바꾼다 → 누가 뭘 왜 바꿨나?

* Git이 좋은 점
  * 강력하고 편리한 브랜치
  * 빠른 성능
  * 분산 저장소

---
class: center, middle, inverse

# 기 __승__ 전 결

핵심 개념 공략

---

# Git이 참 훌륭한데...

* 숙지할 개념이 있습니다.
* 서브버전과도 다릅니다.
* __한마디로 조금 노력이 필요합니다.__
* 걱정금지: 그래봐야 별 거 아닙니다.
---

background-image: url("img/distributed.png")

# 특징 (1)

DVCS

---

# 특징 (2) - 차이점 or 스냅샷 기록


.full-width[![](img/deltas.png)]
.center[각 파일에 대한 변화를 저장하는 시스템]

---

# 특징 (2) - 차이점 or 스냅샷 기록

.full-width[![](img/snapshots.png)]
.center[시간순으로 프로젝트의 스냅샷을 저장]

---

# 특징 (3) - 세 가지 상태

.full-width[![](img/areas.png)]

---
# 개념 (1) - 세가지 상태 영역

## 작업 디렉토리
## 인덱스
## 히스토리

---
# 개념 (2) - 커밋

* 하나의 트리와 유래된 커밋들을 참조
* 결국 하나의 스냅샷을 의미
* SHA1 아이디

---
# 개념 (3) - 브랜치

* 하나의 트리와 유래된 커밋들을 참조
* 결국 하나의 스냅샷을 의미
* SHA1 아이디

---
class: center, middle, inverse

# 기 승 __전__ 결

실습 해보잣!
---

# 클라이언트 설치

1. 클라이언트 설치
1. 최초 설정
1. 저장소 만들기
1. 파일 변경하기

---

# 클라이언트 설치

<https://git-scm.com/downloads>

## 리눅스

``` bash
apt-get install git
```

## 윈도우

    C:\Program Files\Git

---

# Git: 최초 설정

```bash
git config --global user.name "성명"
git config --global user.email "이메일"
```

```bash
git config --global color.ui true
git config --global push.default simple
```

```bash
git config --global core.quotepath false
git config --global core.precomposeunicode true
```

```bash
git config --global credential.helper osxkeychain
```

---

# Git 저장소 만들기

## 작업중인 디렉토리에서 새로 만들기

```bash
git init
```

## 리모트 저장소에서 복제하기

```bash
git clone [리모트 저장소 주소]
```

### 예)

```bash
git clone https://github.com/hatemogi/git-tutorial-jeju
```


---

# 시뮬레이션


> [Git w/D3](https://onlywei.github.io/explain-git-with-d3/)
>
> [Git w/D3 zen](https://onlywei.github.io/explain-git-with-d3/#zen)


---
class: center, middle, inverse

# 기 승 전 __결__

더 잘 쓰려면?

---
# 무료 GUI 클라이언트

* [GitHub Desktop: Simple collaboration from your desktop](https://desktop.github.com)
* [SourceTree: A free Git & Mercurial client for Windows or Mac](https://www.sourcetreeapp.com)
* [GitKraken: The downright luxurious Git client, for Windows, Mac & Linux](https://www.gitkraken.com)

# 무료 TUI(?) 클라이언트

* [Tig: Text-mode interface for git](https://github.com/jonas/tig)

---
# IDE 플러그인
# 더 볼 자료

## 도서

## 웹사이트


---

# 참고자료

## 한국어
* [git - 간편 안내서](http://rogerdudler.github.io/git-guide/index.ko.html)
* [A Visual Git Reference](https://marklodato.github.io/visual-git-guide/index-ko.html)
* [[NDC16] Effective Git](http://www.slideshare.net/kexplo/ndc2016-effective-git)
* [Pro Git 2판](https://git-scm.com/book/ko/v2)
* [생활코딩 GIT](https://opentutorials.org/course/1492)

## 영문
* [Try Git](http://try.github.io/)
* [Visualiing Git Concepts with D3](https://onlywei.github.io/explain-git-with-d3/)
