---
layout: default
title: Jekyll Blog 시작 (4) - Github 에서 작업하기
nav_order: 4
description: "Jekyll Blog 시작 - Github 에서 작업하기"
parent: Jekyll Blog 시작
grand_parent: Story
permalink: /story/jekyll-blog/4
---

<br>

# 설치 환경

---
 - Mac 기반으로 작성 되었습니다.



# 목차

---
 - [시작하며](/story/jekyll-blog/4#시작하며)
 - [Repository 추가](/story/jekyll-blog/4#repository-추가)
 - [_config.yaml 파일 추가](/story/jekyll-blog/4#_configyaml-파일-추가)
 - [index.md 파일 추가](/story/jekyll-blog/4#indexmd-파일-추가)
 - [배포 확인 하기](/story/jekyll-blog/4#배포-확인-하기)



## 시작하며

---
이번 포스팅 으로 드디어 "Jekyll Blog 시작" 이 마무리가 되었습니다.

GIT으로 블로그를 띄우는 과정은 구글링을 해보면 너무나 많이 나와 이부분 까지 써야할까 싶었지만

해당 내용들에 배포 과정을 단순히 기다리면 반영된다 라고 나와있어 이 부분을 중점적으로 써야겠다 싶었습니다.

Git 으로 작업 하시는 분들이나 개발자 분들은 바로 목차의 **[배포 확인 하기](/story/jekyll-blog/4#배포-확인-하기)** 만 보셔도 좋을것 같습니다.
{: .text-red-000}

원래 목표로 잡았던건 주 또는 월 1 포스팅 하기였는데..

살짝 뿌듯한 감이 있기도 하고 다음 포스팅에 대한 기대가 들기도 합니다.

앞으로 더욱 풍성해진 블로그를 많은 분들이 봐주셨으면 합니다.

감사합니다.

---

## Repository 추가

---

Git을 회원 가입 한후 오른쪽 상단의 **New repository** 를 클릭 합니다.


![Git Main](/assets/images/story/jekyll/git_main.png)

아래의 이미지와 같이 **{username}.github.io** 로 새로운 Repository 를 생성 합니다. 

아래의 이미지는 이미 생성이 되어있는 상황이라 중복 체크가 되고, 
아래의 생성 버튼이 활성화 되어있지 않지만, 

생성 버튼이 활성화 되면 생성 하시면 됩니다.


![Create Repository](/assets/images/story/jekyll/create_repository.jpg)

## _config.yaml 파일 추가

---

위 순서대로 Repository 를 생성하게 되면 아래와 같은 화면이 뜹니다.

이전 포스팅을 따라오신 분들은 git remote 를 연결 시키시거나 clone 하시면 되고,

웹환경에서만 작업하실 분들은 아래 보시는 이미지의 **creating a new file** 링크를 클릭 합니다.

왠만하면 확인이 편한 로컬 작업을 **추천** 드립니다.

![Create File](/assets/images/story/jekyll/create_file.jpg)

[Jekyll Blog 시작 (2) - Theme 선택 후 반영 (JUST THE DOCS)](/story/jekyll-blog/2) 에서 선택 했던, 

Just The Docs Theme 기반의 설정파일을 생성합니다.

Github 배포 환경에서 기본적으로 Ruby Jekyll 환경을 지원 해주기 때문에 

선택한 **원격 테마(remote_theme)** 를 기본으로 세팅을 해주시면 됩니다.

이후 간단한 커밋 메시지와 함께 **Commit new file** 버튼을 클릭합니다.

![Create Config File](/assets/images/story/jekyll/create_config_file.jpg)

아래는 설정 내용입니다.

~~~
remote_theme: just-the-docs/just-the-docs
#theme: "just-the-docs"


minimal_mistakes_skin    : "air" # "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise"               ## 사이트 스킨
#logo: "/assets/images/logo.jpg"                                                                                      ## 사이트 로고
locale                   : "ko-KR"
title                    : "Jason Tech Story"
title_separator          : "-"
subtitle                 : "기술 블로그"# site tagline that appears below site title in masthead
name                     : "Jason"
description              : "기술 블로그"
url                      : ""# the base hostname & protocol for your site e.g. "https://mmistakes.github.io"
baseurl                  : ""# the subpath of your site, e.g. "/blog"
repository               : "jason-lee-91/jason-lee-91.github.io"# GitHub username/repo-name e.g. "mmistakes/minimal-mistakes"
gh_edit_repository: "https://github.com/jason-lee-91/jason-lee-91.github.io/" # the github URL for your repo



# Aux links for the upper right navigation
aux_links:
  "Jason on GitHub":
    - "//github.com/jason-lee-91/introduce"                                                                                      ## 상단 git 링크
~~~

## index.md 파일 추가

---

_config.yaml 파일을 생성하게 되면 초기 화면과는 다르게 파일을 생성하는 버튼이 생기게 됩니다.

오른쪽 상단의 **Add file > Create new file** 을 클릭 합니다.

![Create Config After](/assets/images/story/jekyll/create_after.png)

이후 아래의 이미지와 같이 **설정 파일**인 **_config.yaml** 와 같이 **가장 중요**한

**메인 페이지**인 **index.md** 파일을 생성 해 줍니다.

![Create Index](/assets/images/story/jekyll/index_md.jpg)

아래는 간단한 메인페이지 내용입니다.

~~~
---
layout: default
title: Introduce
nav_order: 1
description: "소개"
permalink: /
---


# **Jason Tech Story**
**email** merryljh91@naver.com
{:.text-right}
**since** 2022-07-23
{:.text-right}

---
~~~

## 배포 확인 하기

---
Github 에서는 {username}.github.io 의 master branch에 커밋을 하게 되면,

git hook 을 통해 CI/CD 환경을 제공해 배포를 진행 합니다.

CI/CD 관련한 좀 더 상세한 내용은 조만간 포스팅을 진행할 예정이라 그때 자세히 이야기해 보도록 하겠습니다.

아래의 이미지와 같이 **Actions** 탭을 클릭 하시면 git 소스 수정에 대한 배포 history 를 상세히 보실 수 있습니다.

**초록색** 은 성공적인 배포, **노란색** 은 진행 중인 배포, **빨간색** 은 실패한 배포를 뜻합니다.

각 내용을 클릭 하시면 배포 **Pipeline** 들을 확인 하실 수 있습니다.

![Deploy Start](/assets/images/story/jekyll/deploy_start.jpg)

아래의 이미지는 해당 배포를 클릭 했을때 보여지는 Pipeline Flow 화면 입니다.

보시는 것과 같이 **build, report-build-status, deploy** Pipeline이 보입니다.

![Build Process](/assets/images/story/jekyll/build_process.jpg)

위 이미지의 Pipeline을 클릭 하시면 해당 파이프라인의 Stage 진행 상황 및 history 를 볼 수 있습니다.

해당 화면에서 오류가 떻을경우 확인 하신 후 수정 및 배포 진행 상황들을 확인 하시면 됩니다.

![Build Process Second](/assets/images/story/jekyll/build_process_se.jpg)

<br>

[Jekyll Blog 시작 (3)](/story/jekyll-blog/3){: .float-left .btn .btn-green }


<br>
<br>
<br>