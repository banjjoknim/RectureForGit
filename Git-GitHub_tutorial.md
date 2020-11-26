---
title: Git-GitHub Tutorial
subtitle: CLI(Git Bash) & GUI(SourceTree)
author: banjjoknim
presentedAt: 2020-10-06
---
# 목차

### 1. VCS(Version Control System)

### 2. Git & GitHub 주요 개념 소개

### 3. CLI && GUI

### 4. Git의 명령어

### 5. SourceTree

### 6. .gitignore
---
# VCS(Version Control System)

### 버전

**`버전(version)`** 은 구체적인 한 단어로 명시하기는 힘들지만 의미있는 변화 또는 그 변화가 적용된 상태라고 할 수 있습니다.

![version_description](https://user-images.githubusercontent.com/68052095/95172086-c9dabb00-07f1-11eb-9370-b137555ab7ca.PNG)

- 이미지 출처 : [네이버 지식백과](https://terms.naver.com/entry.nhn?docId=1181091&cid=40942&categoryId=32828)
---
# VCS(Version Control System)

### 버전

![patch_note](https://user-images.githubusercontent.com/68052095/95172172-e676f300-07f1-11eb-8d0b-ee8e526ce858.png)
![hotfix](https://user-images.githubusercontent.com/68052095/95172276-09a1a280-07f2-11eb-8dc0-c35c2dfd2504.jpg)

- 이미지 출처 : [리그 오브 레전드 패치 노트](https://kr.leagueoflegends.com/ko-kr/news/tags/patch-notes)

---
# VCS(Version Control System)

### 버전관리

의미있는 변화 및 기능개선, 버그 수정등 수정사항에 대한 변화들을 관리하는 것을 말합니다.

**`버전관리 시스템(Version control System)`**은 **`버전(version)`**을 관리하는 체계, 즉 파일의 변화를 시간에 따라 기록했다가 나중에 특정 시점의 버전을 다시 꺼내올 수 있는 시스템입니다.


![save_load](https://user-images.githubusercontent.com/68052095/95172372-2f2eac00-07f2-11eb-9a4f-74a10f2e9d4a.png)
![reset](https://user-images.githubusercontent.com/68052095/95172395-3bb30480-07f2-11eb-8893-63e61ea2c8e4.png)

- 이미지 출처 : [디아블로2 관련 포스팅](http://blog.gorekun.com/?p=1272), [언더테일](https://undertale.com/)

---
# VCS(Version Control System)

### Why?

하나의 프로젝트는 마치 거대한 배와도 같습니다.

![ship](https://user-images.githubusercontent.com/68052095/95172410-42417c00-07f2-11eb-8ac2-4fa122b105a8.jpg)

- 이미지 출처 : `삼성중공업 OOCL HONGKONG`

---
# VCS(Version Control System)

### Why?

한번쯤은 사용해보았을 OO드라이브와 같은 클라우드 서비스.

`클라우드 서비스 : 개인의 하드디스크가 아닌 인터넷을 통해 이용할 수 있는 서비스를 말합니다.`

![cloud](https://user-images.githubusercontent.com/68052095/95172413-440b3f80-07f2-11eb-94a3-2e45ba65db86.jpeg)

- 이미지 출처 : [네이버 N드라이브(~~현재는 네이버 클라우드로 대체~~)](https://www.navercloudcorp.com/), [Google 드라이브](https://www.google.com/intl/ko_KR/drive/), [OneDrive](https://www.microsoft.com/ko-kr/microsoft-365/onedrive/online-cloud-storage)

---
# VCS(Version Control System)

### Why?

어느샌가 쌓여버린 수많은 파일들

![dirty_version](https://user-images.githubusercontent.com/68052095/95172416-440b3f80-07f2-11eb-9499-508e6932e10a.jpg)

---
# VCS(Version Control System)

![wikipedia](https://user-images.githubusercontent.com/68052095/95172591-803ea000-07f2-11eb-9dd6-b4527a0b106c.PNG)

- 이미지 출처 : [위키백과](https://ko.wikipedia.org/wiki/%EB%B2%84%EC%A0%84_%EA%B4%80%EB%A6%AC)

---
# VCS(Version Control System)

![wikipedia2](https://user-images.githubusercontent.com/68052095/95172900-ec210880-07f2-11eb-82a9-533c7ea770cb.PNG)

- 이미지 출처 : [위키백과 - 역사 보기](https://ko.wikipedia.org/w/index.php?title=%EC%9C%84%ED%82%A4%EB%B0%B1%EA%B3%BC:%EB%8C%80%EB%AC%B8&action=history)

---
# VCS(Version Control System)

![wikipedia3](https://user-images.githubusercontent.com/68052095/95172902-edeacc00-07f2-11eb-8e50-22324bf85c73.PNG)

- 이미지 출처 : [위키백과 - 역사 보기](https://ko.wikipedia.org/w/index.php?title=%EC%9C%84%ED%82%A4%EB%B0%B1%EA%B3%BC:%EB%8C%80%EB%AC%B8&action=history)

---
# VCS(Version Control System)

### Why?

- 명확한 역할 분담, 안정적인 작업
- 프로젝트에 참여하는 구성원간의 혼란 방지
- 효율적인 작업내용 관리 및 백업

---
# Git

![git](https://user-images.githubusercontent.com/68052095/95176217-86834b00-07f7-11eb-82b2-ffabcb918e32.png)

- 이미지 출처 : [Git](https://git-scm.com/downloads/logos)
>
- 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 `분산 버전 관리 시스템(Distributed Version Control System)`이다.
- 각각의 개발자가 중앙 서버에 접속하지 않은 상태에서도 코드 작업을 할 수 있다.
- 독립적으로 작업한 다음에 변경사항에 대해서 선택적으로 반영, 유연한 채택이 가능하다.

---
# Git

![staging_area](https://user-images.githubusercontent.com/68052095/95195970-4a111880-0812-11eb-810e-50041b2b855a.png)

- 이미지 출처 : [Git Staging Area: Explained Like I'm Five](https://dev.to/sublimegeek/git-staging-area-explained-like-im-five-1anh)

---
# Git

**Working Tree**
- 아직 버전으로 만들어지기 전 단계, 순수하게 작업내용만 존재하는 공간입니다.
- 일반적으로 사용자가 파일과 하위 폴더를 만들고 작업내용을 저장하는 공간입니다.
- 정확하게는 작업 폴더에서 `.git` 폴더를 제외한 나머지 부분입니다.

**Staging Area** 
- 우리가 버전으로 만들고 싶은 파일을 선별해서 올려두는 공간입니다. 여기에 올라온 파일들만을 모아서 하나의 버전으로 만들고 `repository`에 넣습니다.

**Repository** 
- 버전이 저장되는 저장소입니다. `.git` 폴더를 repository라 봐도 됩니다.

---
# Git

### 커밋(commit)

`버전을 만드는(제출하는) 행위 또는 버전 그 자체를 뜻합니다.`

- 새로 커밋을 생성하면 그 커밋의 부모는 언제나 이전 커밋입니다.
- 커밋이 생성되면 HEAD는 새로운 커밋으로 갱신됩니다.
- HEAD가 가리키는 브랜치도 HEAD와 함께 새로운 커밋을 가리킵니다.
- 커밋하면 커밋 객체가 생깁니다. 커밋 객체에는 부모 커밋에 대한 참조와 실제 커밋을 구성하는 파일 객체가 들어 있습니다.

---
# Git

### 브랜치(branch)

해석하면 `가지`라는 뜻입니다. `분기점이 되기 전의 상태(조상)와 같은 상태`를 가지지만 `동시에 독립적인 상태`를 가집니다.
마치 `평행세계`와 같다고 보면 됩니다. 하나의 저장소에서 다양한 작업을 수행할 수 있게 해줍니다.

![branch](https://user-images.githubusercontent.com/68052095/95193268-82165c80-080e-11eb-99ba-5de27ee3beee.jpg)

- 이미지 출처 : [branch](https://lokalise.com/blog/project-branching-using-tags/)

---
# Git

### 브랜치(branch)

- 브랜치는 논리적으로는 어떤 커밋과 그 조상들을 묶어서 뜻하지만, 사실은 단순히 커밋 객체 하나를 가리킬 뿐입니다.  

- **HEAD**
  - HEAD는 특수한 포인터입니다. 이 포인터는 지금 작업하는 로컬 브랜치를 가리킵니다.
  - 브랜치는 커밋을 가리키므로 HEAD도 커밋을 가리킵니다.
  - 결국 HEAD는 현재 작업 중인 브랜치의 최근 커밋을 가리킵니다.


- **브랜치를 주로 사용할 때**

  - 새로운 기능 추가
  - 버그 수정
  - 병합(merge)과 리베이스(rebase) 테스트
  - 이전 코드 개선
  - 특정 커밋으로 돌아가고 싶을 때

---
# Git

![pruning-thinning](https://user-images.githubusercontent.com/68052095/100348312-19877700-302a-11eb-8196-f39b959a4a15.jpg)

- 이미지 출처 : [가지치기](https://www.sunset.com/garden/garden-basics/basic-pruning-cuts)

#### 브랜치(branch)를 왜 사용해야 하나요?

- **목적별로 분류하여 개발할 수 있다. 즉, 의도를 쉽게 알 수 있다.**
- **독립적으로 작업할 수 있다. 즉, 한 사람의 작업이 다른 사람에게 영향을 미치지 않는다.** 
- **하나의 소스코드로 동시에 여러가지 작업을 할 수 있다.**

#### 브랜치(branch)를 꼭 사용해야 하나요?

- **브랜치는 필요하다고 판단될 때 사용하면 됩니다.**


---
# Git

### 태그(tag)

- 주석 있는 태그(권장)
- 간단한 태그
- 커밋에 붙여주는 식별자(이름)
- 커밋을 식별할 수 있는 정보
- ex) `v.1.0.0`

프로그램을 출시하는 것을 **`릴리즈(release)`**라고 하는데, 이때, 태그를 붙여서  사용자들이 쓸 수 있도록 배포하는 것을 말합니다.
태그를 사용하면 **`GitHub`**의 **`[Tags]`** 탭에서 확인할 수 있고, **`[Release]`** 탭에서 다운받을 수도 있습니다.

---
# Git

### 알아둘 것
  - `git`을 이용해서 `한 번이라도 버전관리를 하면` git은 버전관리를 했던 파일을 기억하고 관리대상으로 추가합니다.
  - `git init`을 하지 않으면 git은 그 파일을 관리하지 않습니다. **즉, 자동으로 모든 파일을 관리하지 않습니다.**
  - `HEAD가 가리키는 버전`을 바꿈으로써 우리가 현재 주시하고 있는 디렉토리가 바뀐 버전이 만들어진 시점으로 휙 돌아가게 됩니다.
  - 버전관리를 하지 말아야할 파일이 있다면? `.gitignore`라는 파일을 만들고 버전관리에서 제외할 대상인 파일의 이름을 쓰면됩니다.
---
# GitHub

**Git으로 관리하는 프로젝트를 올릴 수 있는 호스팅 사이트중 하나입니다.**

![github](https://user-images.githubusercontent.com/68052095/95195588-b9d2d380-0811-11eb-9a62-60747e6643f3.jpeg)

- 이미지 출처 : [GitHub](https://github.com/logos)

---
# GitHub

### 대표적인 Git 호스팅 사이트

| Git 호스팅 사이트   |      특징      |  가격 정책 |
|----------|:-------------:|:------:|
| GitHub.com |  사용자 2,800만 명. 세계 최대 규모의 Git 호스팅 사이트 | 공개저장소 생성 무료, 비공개저장소는 작업자 3인 이하인 경우에는 무료. 설치형 버전인 Enterprise를 월 21달러에 이용할 수 있다. |
| GitLab.com |    GitHub에 뒤지지 않는다. NASA, Sony 등 10만 개 이상의 조직이 사용하고 있다. GitLab 프로젝트 자체가 오픈소스여서 직접 서비스 발전에 기여할 수 있다.   |   공개저장소 및 비공개저장소 생성 무료. 소스코드 빌드에 유용한 도구 지원 성능에 따라 월 4달러 ~ 99달러 부담 |
| BitButcket.org | 사용자 600만 명. 이슈 관리 시스템인 지라(Jira)를 만든 Atlassian이 모기업이어서 지라와 연동이 쉽다. |    5명 이하 팀이면 공개저장소 및 비공개저장소 생성 무료. 그 이상이면 월 2달러 ~ 5달러 부담 |

---
# GitHub

### 알아둘 것

- GitHub에 소스코드를 올려두면 시간, 공간의 제약 없이 협업할 수 있습니다.

- 개인의 컴퓨터에 존재하는 디렉토리에서 `git init` 명령으로 생성되는 `.git` 폴더가 `로컬저장소`입니다. 커밋, 커밋을 구성하는 객체, 스테이지가 모두 이 폴더에 저장됩니다.

- 로컬저장소를 업로드하는 공간을 `원격저장소`라고 부릅니다. 여기서는 `GitHub 저장소`가 곧 `원격저장소`입니다.

- 로컬저장소와 원격저장소는 각각 영어로 `Local Repository`, `Remote Repository`라 합니다.

- 각각의 저장소는 Git으로 관리한 소스코드에 대한 버전정보를 담고 있고, 관리할 수 있습니다.

---
# GitHub

### Git-GitHub의 기본적인 작업흐름도
![basic-remote-workflow](https://user-images.githubusercontent.com/68052095/95196558-34502300-0813-11eb-8139-3975ca11975c.png)

---
# GitHub

### fork

브랜치가 `평행세계`를 만드는 것이었다면, `fork`는 `평행우주`를 만드는 것과 같습니다. `독립된 주소`를 가진 원격저장소를 생성합니다.
  
`fork`는 다른 원격저장소의 `브랜치를 포함한 모든 커밋 이력`을 `새로운 원격저장소`로 복사합니다.
  
![fork2](https://user-images.githubusercontent.com/68052095/95202053-c2c8a280-081b-11eb-91d0-bfb8be415308.png)

- 이미지 출처 : [Github Desktop – Step 1 – Fork](https://www.classicpress.net/blog/github-desktop-step-1-fork/)

---
# GitHub

### `branch` vs `fork`
  
|      |     의의   |      편리한 점      |  불편한 점 |
|------|:----------:|:-------------------:|:----------:|
|`브랜치(branch)`| 하나의 원본저장소에서 분기를 나눈다. |  하나의 원본저장소에서 코드 커밋 이력을 편하게 볼 수 있다. | 다수의 사용자가 다수의 브랜치를 만들면 관리하기 힘들다. |
|`포크(fork)`  | 여러 원격저장소를 만들어 분기를 나눈다. |    원본저장소에 영향을 미치지 않으므로 원격저장소에서 마음껏 코드를 수정할 수 있다.   |   원본저장소의 이력을 보려면 따로 주소를 추가해야 한다. |

---
# GitHub

### fork

GitHub에서 `fork`를 하는 방법은 간단합니다. 원본저장소에 들어간 뒤, 우측 상단의 `fork`버튼을 누르면 됩니다.

![fork](https://user-images.githubusercontent.com/68052095/95200611-a75c9800-0819-11eb-93b8-fb7f2d1aad40.PNG)

---
# GitHub

### Pull Request

`Pull Request`는 어떤 브랜치에 또다른 브랜치를 합치려고 할때, 협력자에게 `브랜치 병합을 요청`하는 메시지를 보내는 것입니다.
즉, `코드에 대한 검토요청`을 하는 것입니다.

![pull_request](https://user-images.githubusercontent.com/68052095/95202375-323e9200-081c-11eb-899e-0a38abe25f07.png)

- 이미지 출처 : [5 elements of a perfect pull request](https://www.atlassian.com/blog/bitbucket/5-pull-request-must-haves)

---
# GitHub

### 코드 리뷰란?

![pull_request5](https://user-images.githubusercontent.com/68052095/100341582-11c2d500-3020-11eb-842e-2df2d262ace8.png)

한 명 또는 여러 명의 개발자가 본인이 만들지 않은 코드의 내용을 점검(examining)하고, 피드백을 주는 과정을 말합니다.

### 코드 리뷰의 장점
- **기능의 정상 동작 여부 검증**
- **버그의 조기 발견**
- **가독성과 유지보수 편의성등의 코드 개선**
- **코드 리뷰를 통한 학습**
- **...**

---
# GitHub

### Pull Request

1. 브랜치의 변경사항 원격저장소에 적용한 뒤, `pull request` 버튼 또는 `Compare & pull request` 버튼을 누릅니다.

![pull_request2](https://user-images.githubusercontent.com/68052095/95204583-43d56900-081f-11eb-82cc-74f654df207f.png)

---
# GitHub

### Pull Request

2. 다음과 같이 `pull request`를 작성하는 창이 나오는데, 제목 및 내용을 작성해주시면 됩니다.

![pull_request3](https://user-images.githubusercontent.com/68052095/95204594-459f2c80-081f-11eb-8158-9b0fcf7d0d4f.png)

**`base : master`** : 병합된 커밋이 들어갈 브랜치가 `master`라는 뜻입니다.

**`compare : new`** : 병합의 대상이 될 브랜치가 `new`라는 뜻입니다.

---
# GitHub

### Pull Request

3. 마지막으로 검토가 끝난뒤 `Merge pull request` 버튼을 눌러 브랜치를 병합합니다.

![pull_request4](https://user-images.githubusercontent.com/68052095/95206856-2786fb80-0822-11eb-96c7-3a08d70a04bc.png)

---
# CLI & GUI

### CLI (Command Line Interface)

명령 줄 인터페이스, CLI는 터미널또는 콘솔창을 통해 사용자와 컴퓨터가 상호 작용하는 방식을 뜻한다. 즉, 작업 명령은 사용자가 컴퓨터 키보드를 통해 문자열의 형태로 입력해야만 한다.

![CLI](https://user-images.githubusercontent.com/68052095/95210057-06c0a500-0826-11eb-9e64-d43a88b55f27.png)

- 이미지 출처 : [Command Line Interface](https://namu.moe/w/CLI)

---
# CLI & GUI

### GUI (Graphical User Interface)

그래픽 사용자 인터페이스, GUI는 사용자가 편리하게 사용할 수 있도록 입출력 등의 기능을 알기 쉬운 아이콘 따위의 그래픽으로 나타낸 것, 사용자가 창이나 스크롤, 버튼, 이미지, 아이콘 등을 이용하여 시스템을 조종할 수 있도록 도와준다.

![GUI](https://user-images.githubusercontent.com/68052095/95209744-a7fb2b80-0825-11eb-9bd9-9e21b56631cd.jpg)

- 이미지 출처 : [Graphical User Interface](https://www.omnisci.com/technical-glossary/graphical-user-interface)

---
# Git의 명령어

### 명령줄 구문 표기

- \[옵션인자] : 선택적으로 입력하는 옵션입니다.
- <필수인자> : 필수적으로 입력해야하는 옵션입니다.
- 모든 입력들의 사이는 공백(" ")으로 구분됩니다.

---
# Git의 명령어

![git-init](https://user-images.githubusercontent.com/68052095/100332247-81cb5e00-3014-11eb-9deb-e85d3593153a.PNG)

**git init**

현재 위치한 디렉토리에서 `.git` 숨김폴더를 만듭니다. 즉, 현재 디렉토리를 `Local Repository`로 만듭니다.

![git-status](https://user-images.githubusercontent.com/68052095/100332270-8728a880-3014-11eb-916d-4c7117562ce6.PNG)

---
# Git의 명령어

**git status \[-s]**

`Git 워킹트리의 상태를 보는 명령으로, 매우 자주 사용합니다.
워킹트리가 아닌 폴더에서 실행하면 오류가 발생합니다.`
- `[-s]` 옵션을 사용할 경우, git status 명령보다 짧게 요약해서 상태를 보여줍니다. 이는 변경된 파일이 많을 때 유용합니다.

![git-log](https://user-images.githubusercontent.com/68052095/100332251-82fc8b00-3014-11eb-9ec2-2adb4c83afae.PNG)

---
# Git의 명령어

**git log**

`현재 브랜치의 커밋 이력을 보는 명령입니다.`

- git log -n<숫자> 

`전체 커밋 중에서 최신 n개의 커밋만 살펴봅니다. 아래의 
다양한 옵션과 조합해서 쓸 수 있습니다.`

- git log --oneline --graph --decorate --all 

`자주 사용하는 옵션으로 간결하고 멋지게 보여줍니다.`

>  - --oneline : 커밋 메시지를 한 줄로 요약해서 보여줍니다.
>  - --graph : 커밋 옆에 브랜치의 흐름을 그래프로 보여줍니다. GUI와 유사한 모습으로 나옵니다.
>  - --decorate : 원래는 --decorate=short 옵션을 의미한다. 브랜치와 태그 등의 참조를 간결히 표시합니다.
>  - --all : all 옵션이 없을 경우 HEAD와 관계없는 옵션은 보여주지 않습니다.
  
---
# Git의 명령어

![git-add, commit](https://user-images.githubusercontent.com/68052095/100332277-8b54c600-3014-11eb-8b0d-c3ffb95f204d.PNG)

**git add <파일명>...**

`파일들을 스테이지에 추가합니다.
새로 생성한 파일을 스테이지에 추가하고 싶다면 반드시 add 명령을 사용합니다.`

- <파일> 뒤의 "..."의 의미는 한 번에 여러 파일 이름을 지정할 수도 있다는 뜻입니다.

**git commit \[-a] \[-m "메시지"]**

`스테이지에 있는 파일들을 커밋합니다.`

- `[-m "메시지"]` 옵션을 사용하면 `" "`속의 메시지로 커밋을 만듭니다.
- `[-a]` 옵션은 신규 파일을 제외하고 트래킹하는 모든 파일의 변경사항에 대해서 `git add` 명령어를 실행함과 동시에 커밋을 만들 수 있는 옵션입니다. `[-m]`과 함께 사용할 수 있습니다.
 
---
# Git의 명령어

![git-remote](https://user-images.githubusercontent.com/68052095/100332253-82fc8b00-3014-11eb-937f-00d44359f7e4.PNG)

**git remote add <원격저장소 이름> <원격저장소 주소>**

`원격저장소를 등록합니다.`

- 원격저장소는 여러 개 등록할 수 있지만 같은 별명의 원격저장소는 하나만 가질 수 있습니다. 통상 첫 번째 원격저장소를 origin으로 지정합니다.

**git remote -v**

`원격저장소 목록을 살펴봅니다.`

---
# Git의 명령어

![git-push-error](https://user-images.githubusercontent.com/68052095/100333301-c60b2e00-3015-11eb-8122-7374c1fb09df.PNG)
![git-push-origin-master](https://user-images.githubusercontent.com/68052095/100333303-c6a3c480-3015-11eb-83d1-f6267856162d.PNG)

**git push \[-u] \[원격저장소별명] \[브랜치이름]**

`현재 브랜치에서 새로 생성한 커밋들을 원격저장소에 업로드합니다. [-u] 옵션으로 현재 브랜치의 업스트림 브랜치를 등록할 수 있습니다. 한 번 등록한 후에는 git push만 입력해도 됩니다.`

- 옵션 `[-u]`가 가리키는 것은 `upstream` 이라는 것으로, 업스트림 브랜치는 로컬저장소와 연결된 원격저장소를 일컫는 단어입니다.
- `[-u]`는 `--set-upstream`의 단축 명령입니다.

---
# Git의 명령어

![git-clone](https://user-images.githubusercontent.com/68052095/100337134-5e0b1680-301a-11eb-8a7e-3fc1ade0f3ec.PNG)

**git clone <저장소 주소> \[새로운 폴더명]**

`저장소 주소에서 프로젝트를 복제해 옵니다. 이때 새로 생길 폴더명은 생략 가능하며, 폴더명을 생략하면 프로젝트 이름과 같은 이름의 폴더가 새로 생성됩니다.`

- 저장소 주소가 반드시 원격저장소의 주소일 필요는 없습니다. 때에 따라 로컬저장소도 `git clone` 명령으로 복제하여 사용할 수도 있습니다.
- 현재 폴더에 복제를 하고싶다면 `[새로운 폴더명]` 옵션에 `.`을 입력하면 됩니다.

**git pull**

`원격저장소의 변경사항을 워킹트리에 반영합니다. `

- 사실은 `git fetch`와 `git merge`를 합친 명령입니다.

**git fetch \[원격저장소별명] \[브랜치이름]**

`원격저장소의 브랜치와 커밋들을 로컬저장소와 동기화합니다. 옵션을 생략하면 모든 원격저장소에서 모든 브랜치를 가져옵니다.`

---
# Git의 명령어

![git-reset1](https://user-images.githubusercontent.com/68052095/100332255-83952180-3014-11eb-8e97-4a6c2792cf01.PNG)
![git-reset2](https://user-images.githubusercontent.com/68052095/100332257-83952180-3014-11eb-8cd9-7d6f78141964.PNG)

**git reset \[파일명]**

`스테이지 영역에 있는 파일들을 스테이지에서 내립니다(언스테이징, mixed reset).`
- 워킹트리의 내용은 변경되지 않습니다. \[파일명] 옵션을 생략할 경우 스테이지의 모든 변경사항을 초기화합니다.
- (soft, mixed, hard) 3가지의 옵션을 선택할 수 있으며, 옵션을 생략하고 사용할 경우 mixed reset으로 동작합니다.`

---
# Git의 명령어

![git-reset3](https://user-images.githubusercontent.com/68052095/100332260-842db800-3014-11eb-88f1-7c0cf1ad3536.PNG)
![git-reset4](https://user-images.githubusercontent.com/68052095/100332261-842db800-3014-11eb-8c8b-af73545ecbcc.PNG)

**git reset --hard <이동할 커밋 체크섬>**

`현재 브랜치를 지정한 커밋으로 옮깁니다. 이때, 작업 폴더의 내용도 함께 변경됩니다.`

- `reset`은 현재 브랜치를 특정 커밋으로 되돌릴 때 사용합니다. 이 중에서 가장 많이 사용하는 `git reset --hard` 명령을 실행하면 현재 브랜치를 지정한 커밋으로 옮긴 후 해당 커밋의 내용을 작업 폴더에도 반영합니다.

---
# Git의 명령어

![git-branch1](https://user-images.githubusercontent.com/68052095/100332280-8bed5c80-3014-11eb-96da-38dd78b612f7.PNG)

**git branch**

`현재 브랜치 목록을 보여줍니다.`

**git branch \[-v]**

`로컬저장소의 브랜치 목록을 보는 명령으로 [-v] 옵션을 사용하면 마지막 커밋도 함께 표시됩니다.
표시된 브랜치 중에서 이름 왼쪽에 *가 붙어있으면 HEAD 브랜치입니다.`

**git branch \[-f] <브랜치이름> \[커밋체크섬]**

`새로운 브랜치를 생성합니다. 커밋체크섬 값을 주지 않으면 HEAD로부터 브랜치를 생성합니다. 이미 있는 브랜치를 다른 커밋으로 옮기고 싶을 때는 [-f] 옵션을 줘야 합니다.`

**git checkout <브랜치이름>** 

`특정 브랜치로 체크아웃할 때 사용합니다. 브랜치 이름 대신 커밋 체크섬을 쓸 수 있습니다. 하지만 브랜치 이름을 쓰는 방법을 강력히 권장합니다.`

**git branch -d <브랜치이름>** 

`특정 브랜치를 삭제할 때 사용합니다. HEAD 브랜치나 병합이 되지 않은 브랜치는 삭제할 수 없습니다.`

**git branch -D <브랜치이름>** 

`브랜치를 강제로 삭제하는 명령입니다. \[-d] 로 삭제할 수 없는 브랜치를 지우고 싶을 때 사용합니다. 역시 조심해야 합니다.`

---
# Git의 명령어

**git merge <대상 브랜치>** 

`지정한 브랜치의 커밋들을 현재 브랜치 및 워킹트리에 반영합니다.`

- 현재 브랜치와 대상 브랜치를 병합할 때 사용합니다. `병합 커밋(merge commit)`이 새로 생기는 경우가 많습니다.
- `Fast-forward(빨리 감기) 병합`은 작업의 흐름이 하나일때 할 수 있습니다.
- 충돌시 **`git merge --abort`** 명령을 통해 `병합(merge)을 취소`할 수도 있습니다.

---
# Git의 명령어

### 충돌이란?

![merge-conflict0](https://user-images.githubusercontent.com/68052095/100337105-52b7eb00-301a-11eb-80c3-8aa444926071.png)
![merge conflict](https://user-images.githubusercontent.com/68052095/100242917-ab36ac00-2f78-11eb-97a4-6aefce3cf470.png)

- 이미지 출처 : [Merge Conflicts](https://ao.gl/cant-pull-a-git-branch-because-of-merge-conflicts/)

---
# Git의 명령어

### 충돌 발생시 해결 과정

![merge-conflict2](https://user-images.githubusercontent.com/68052095/100337108-52b7eb00-301a-11eb-9173-724c5f3cc685.PNG)
![merge-conflict3](https://user-images.githubusercontent.com/68052095/100337109-53508180-301a-11eb-97e2-3e6603f82e3d.PNG)

1. 목적에 맞게 충돌 파일 수정.

---
# Git의 명령어

### 충돌 발생시 해결 과정

![merge-conflict5](https://user-images.githubusercontent.com/68052095/100337113-53e91800-301a-11eb-969a-fbb4127506f5.PNG)

2. git add <충돌 파일>.
3. git status 명령어를 통해 충돌해결 확인.
4. git commit 명령어를 통해 merge commit 생성.
5. git log 명령어를 통해 merge 로그 확인 및 충돌 해결 완료.

---
# Git의 명령어

- **git switch**
- **git restore**
- **git cherry-pick**
- **git revert**

**이 외에도 다양한 명령어들과 옵션들이 있습니다. 궁금하신 분은 추가적으로 공부하시길 바랍니다.**

---
# SourceTree

### GUI 클라이언트 중의 하나인 소스트리

![sourcetree](https://user-images.githubusercontent.com/68052095/95224756-06c8a100-0836-11eb-83bc-a5e0ee976975.png)

- 이미지 출처 : [Atlassian - SourceTree](https://www.atlassian.com/ko/software/sourcetree)

---
# SourceTree

### Local 버튼

`내 컴퓨터에 이미 존재하는 로컬저장소 목록을 불러옵니다.`

`단, 소스트리를 통해 생성되거나 추가되지 않은 저장소는 불러오지 않습니다.`

![Local button](https://user-images.githubusercontent.com/68052095/95229019-07176b00-083b-11eb-92d8-9d2af7e82871.PNG)

---
# SourceTree

### Remote 버튼

`원격저장소 목록을 불러옵니다.`

CLI의 `git remote` 명령어와 동일한 역할을 수행합니다.

![Remote button](https://user-images.githubusercontent.com/68052095/95229025-08489800-083b-11eb-8eae-5f1baea8e292.PNG)

---
# SourceTree

### Clone 버튼

`원격 또는 로컬저장소의 주소를 입력하여 설정한 디렉토리에 저장소를 복사합니다.`

CLI의 `git clone` 명령어와 동일한 역할을 수행합니다.

![Clone button](https://user-images.githubusercontent.com/68052095/95229029-08e12e80-083b-11eb-90ae-74e9d97154e5.PNG)

---
# SourceTree

### Add 버튼

`내 컴퓨터에 이미 존재하는 로컬저장소를 소스트리에 추가합니다.`

![Add button](https://user-images.githubusercontent.com/68052095/95229026-08489800-083b-11eb-99d7-0c8cfb7208d0.PNG)

---
# SourceTree

### Create 버튼

`설정한 디렉토리 및 이름으로 로컬저장소를 새롭게 만듭니다.`

CLI의 `git init` 명령어와 동일한 역할을 수행합니다.

![Create button](https://user-images.githubusercontent.com/68052095/95229030-0979c500-083b-11eb-86bd-28323e283d44.PNG)

---
# SourceTree

### Clone, Add, Create 완료시 진입화면
 - 기본적으로 좌측의 `file status`가 선택되어져 있는 상태입니다.
 - `Commit` 버튼을 눌러서도 진입할 수 있습니다.
 
![sourcetree main](https://user-images.githubusercontent.com/68052095/95229595-b8b69c00-083b-11eb-9d30-ee5e1c5f60ef.PNG)

---
# SourceTree

### `Commit`
 - 새롭게 적용할 수 있는 변경점이 있으면 숫자로 알려줍니다.
 
![sourcetree_commit](https://user-images.githubusercontent.com/68052095/95289898-e5ec6400-08a6-11eb-888b-67a26b7bccbc.png)
 
---
# SourceTree

### `staged files`
 - `Staging Area`에 올라간 파일들을 표시합니다.
 
![sourcetree_commit](https://user-images.githubusercontent.com/68052095/95289898-e5ec6400-08a6-11eb-888b-67a26b7bccbc.png)

---
# SourceTree

### `unstaged files`
 - `Staging Area`에 올라가지 않은(작업공간에만 존재하는) 파일들을 표시합니다.
 
![sourcetree_commit](https://user-images.githubusercontent.com/68052095/95289898-e5ec6400-08a6-11eb-888b-67a26b7bccbc.png)

---
# SourceTree

### `아래쪽의 네모박스` 및 `commit 버튼`
 - `네모박스`는 `commit 메시지`를 작성하는 공간입니다.
 - `commit 버튼`을 누르게 되면 `staged files`에 표시되는 파일들이 `commit`됩니다.
 
![sourcetree_commit](https://user-images.githubusercontent.com/68052095/95289898-e5ec6400-08a6-11eb-888b-67a26b7bccbc.png)

---
# SourceTree

### `pull`
- 작업이력을 받아올 `원격저장소` 및 `브랜치`를 선택할 수 있습니다.
- `현재 작업중인(HEAD가 가리키는)브랜치`에 작업이력을 받아온 뒤 병합(merge)합니다.

![sourcetree_pull](https://user-images.githubusercontent.com/68052095/95290380-141e7380-08a8-11eb-8e3f-2706f073dd48.PNG)

---
# SourceTree

### `fetch`

- `원격저장소`로부터 작업이력을 받아옵니다.
- `원격저장소`에서 지워져서 더 이상 필요없는 브랜치를 제거할 수도 있습니다.
  - **prune**은 `가지치기`라는 뜻입니다. (**branch**는 `가지`라는 뜻)
- `태그` 또한 받아올 수 있습니다.

![sourcetree_fetch](https://user-images.githubusercontent.com/68052095/95290386-154fa080-08a8-11eb-9b00-f4ad0c887dbb.PNG)

---
# SourceTree

### `push`

- `로컬저장소`의 작업내용을 `원격저장소`에 반영할때 사용합니다.
- `로컬저장소의 브랜치`를 선택할 수 있으며 그를 반영할 `원격저장소의 브랜치`도 선택할 수 있습니다.

![sourcetree_push](https://user-images.githubusercontent.com/68052095/95290385-154fa080-08a8-11eb-9c0a-3275b4186096.PNG)


---
# SourceTree

### `branch`

- `새로운 브랜치`를 만듭니다.
- `특정 commit`에 대한 브랜치를 만들 수도 있습니다.

![sourcetree_branch](https://user-images.githubusercontent.com/68052095/95290899-51cfcc00-08a9-11eb-8ce3-1a3337e6bbbb.PNG)

---
# SourceTree

### `merge`

- `현재 브랜치`에 병합할 `commit`을 선택할 수 있습니다.
- 선택한 `commit`에 대해서 변경점을 표시해줍니다.

![sourcetree_merge](https://user-images.githubusercontent.com/68052095/95290901-5300f900-08a9-11eb-9b9f-1cdbceb55e42.PNG)

---
# SourceTree

### `history`

- `작업이력(commit history)`을 모두 볼 수 있습니다.
- 각각의 `commit`을 선택시 아래쪽에 변경점 또한 표시해줍니다.

![sourcetree_history](https://user-images.githubusercontent.com/68052095/95291498-a293f480-08aa-11eb-8f1b-563aca83cb6f.PNG)

---
# SourceTree

### `search`

- `commit 메시지`에 `특정 문구`가 포함된 `commit`들을 찾아서 표시해줍니다.

![sourcetree_search](https://user-images.githubusercontent.com/68052095/95291253-108bec00-08aa-11eb-8e03-5cb8e6eb4106.PNG)

---
# SourceTree

### `side menu - BRANCHES` 

- 현재 존재하는 브랜치들을 보여줍니다. `굵은 글씨`로 표시된 브랜치가 현재 작업중인 브랜치입니다.
- 브랜치 이름을 `더블 클릭` 하면 해당 브랜치로 `checkout`할 수 있습니다. 

![sourcetree_side_menu](https://user-images.githubusercontent.com/68052095/95291900-690fb900-08ab-11eb-93c8-514c06d7ba86.PNG)

---
# SourceTree

### `side menu - TAGS` 

- 현재 존재하는 `태그`들을 보여줍니다.
- `태그 이름`을 `더블 클릭` 하면 해당 태그가 가리키는 `commit`으로 `checkout`할 수 있습니다. 

![sourcetree_side_menu](https://user-images.githubusercontent.com/68052095/95291900-690fb900-08ab-11eb-93c8-514c06d7ba86.PNG)

---
# SourceTree

### `side menu - REMOTES` 

- 현재 로컬저장소와 연결된(등록된) `원격저장소`와 `해당 저장소의 브랜치`들을 보여줍니다.
- 브랜치 이름을 `더블 클릭` 하면 해당 브랜치로 `checkout`할 수 있습니다. 

![sourcetree_side_menu](https://user-images.githubusercontent.com/68052095/95291900-690fb900-08ab-11eb-93c8-514c06d7ba86.PNG)

---
# .gitignore

- `Git`에서 특정 파일 혹은 디렉토리를 관리 대상에서 제외할 때 사용하는 파일입니다.
- 원하지 않는 파일이 `업로드`되는 것을 방지할 수 있습니다.
- 예상치 못한 데이터 충돌로 인한 손실을 방지할 수 있습니다.
- `.gitignore`에 작성된 파일은 `git add` 명령시 자동으로 제외됩니다.

---
# .gitignore

`.gitignore` 파일을 만들어주는 대표적인 사이트인 `.gitignore.io`

![gitignore](https://user-images.githubusercontent.com/68052095/95292654-df60eb00-08ac-11eb-9afb-69d8bbc2298c.PNG)

- 이미지 출처 : [.gitignore.io](https://www.toptal.com/developers/gitignore)

---
# .gitignore

### 사용법

- `.gitignore`의 각 라인마다 무시할 파일이나 디렉터리의 패턴을 적어주면 됩니다.
- 여러 파일을 지정할 경우 `*`을 사용해주면 됩니다.
- 주석을 달고 싶다면 `#`을 해당 라인의 맨 앞에 입력하면 됩니다.
- **이미 추가되어 버전 관리중인 파일에는 영향을 미치지 않으며** 새로 add 할 경우에만 적용됩니다.

>filename
>
>*.class
>
>*.jar
>
>folder/*
>
>\# 주석내용

---
# .gitignore

### 사용법

- 만약 `.gitignore` 목록에 있어도 추가해야 할 경우 `-f(force)` 옵션을 사용해서 추가하면 됩니다.
  - 여기서 **`force`**는 `강제로`라는 의미를 가집니다.

>git add -f file
>
>- `.gitignore`에 설정한 정보는 하위 폴더에도 적용됩니다.
>- 만약 특정 하위 폴더만 다르게 관리하고 싶다면 해당 폴더에 `.gitignore`를 만들면 됩니다.
>- `!`는 이전 패턴을 무효화하는 특별한 의미의 문자열입니다.
>- 만약 파일명에 `!`가 들어갈 경우 `\`를 `!`앞에 붙여주면 됩니다.
>
>* (모든 파일을 무시)
>!file (예외로 file만 버전관리 하겠다는 의미)

---
# .gitignore

### 사용법

1. `운영체제`, `프로그래밍언어`, `사용하는 IDE` 등을 입력한뒤 생성

![gitignore2](https://user-images.githubusercontent.com/68052095/95293776-10421f80-08af-11eb-8a5a-36091a40d5ae.PNG)

---
# .gitignore

### 사용법

2. 텍스트로 이루어진 페이지가 표시됩니다. 모든 텍스트를 복사합니다.

![gitignore3](https://user-images.githubusercontent.com/68052095/95293778-10421f80-08af-11eb-9cb4-c2980a0d19c2.PNG)

---
# .gitignore

### 사용법

3. 본인이 사용하는 IDE 프로젝트 화면에서 `프로젝트 - 우클릭 - New - File`을 차례대로 선택하여 파일을 만듭니다.

![gitignore4](https://user-images.githubusercontent.com/68052095/95298165-9b72e380-08b6-11eb-8456-2d6dacda1693.PNG)

---
# .gitignore

### 사용법

4. 이때 파일명은 `.gitignore`로 해야하며, 만들어진 파일에 복사한 내용들을 붙여넣기 한 뒤 저장합니다.

![gitignore5](https://user-images.githubusercontent.com/68052095/95296201-51d4c980-08b3-11eb-8472-42c2a43eefc1.PNG)

---
# .gitignore

### 사용법

5. 특별히 버전관리 대상에서 제외하고 싶은 디렉터리 또는 파일이 있다면 패턴에 맞춰서 입력해준 뒤 커밋과 푸쉬를 해주면 패턴에 해당하는 파일이 버전관리 대상에서 제외됩니다.

![gitignore6](https://user-images.githubusercontent.com/68052095/95304818-20aec600-08c0-11eb-9e5d-ca5b8f6a953d.PNG)

---
# 참고자료

- 팀 개발을 위한 Git, GitHub 시작하기 초판
- [Git](https://git-scm.com/book/en/v2)
- [GitHub](https://docs.github.com/en)

---
# [강의 자료 링크](https://github.com/banjjoknim/RectureForGit)

---

![thankyou](https://user-images.githubusercontent.com/68052095/95304030-f4467a00-08be-11eb-9b70-62233d24a0eb.jpg)