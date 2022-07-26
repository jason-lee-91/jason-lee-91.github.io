---
layout: default
title: Jekyll Blog 시작 (2) - Theme 선택 후 반영 (JUST THE DOCS)
nav_order: 2
description: "Jekyll Blog 시작 - Theme 선택 후 반영 (JUST THE DOCS)"
parent: Jekyll Blog 시작
grand_parent: Story
permalink: /story/jekyll-blog/2
---

<br>

# 설치 환경

---
 - Mac 기반으로 작성 되었습니다.



# 목차

---
 - [Jekyll 설치](/story/jekyll-blog/2#jekyll-설치)
 - [Jekyll Theme 선택 [Just The Docs ]](/story/jekyll-blog/2#jekyll-theme-선택-just-the-docs--공식-사이트)
    - [Just The Docs 실행](/story/jekyll-blog/2#just-the-docs-실행)
        - [Configurations](/story/jekyll-blog/2#configurations)
        - [Gemfile](/story/jekyll-blog/2#gemfile)
        - [Index](/story/jekyll-blog/2#index)
        - [실행](/story/jekyll-blog/2#실행)



## Jekyll 설치
이전 포스팅의 순서대로 진행이 되었다면 아래의 commend 로 jekyll 설치가 가능합니다.
~~~shell
gem install jekyll
~~~

## Jekyll Theme 선택 [Just The Docs ] [공식 사이트](https://just-the-docs.github.io/just-the-docs/)

---
다음 사이트 또는 추가적인 사이트에서 원하는 Theme 을 선택
 - https://github.com/topics/jekyll-theme [보러가기](https://github.com/topics/jekyll-theme)
 - http://jekyllthemes.org/ [보러가기](http://jekyllthemes.org/)

---
 * 저는 기술 블로그가 목적이였고 UI 가 심플함, 검색 기능 지원 의 이유로 just the docs 선택했지만
지원되지 않는 MarkDown 기능( > 등 ..) 이 있어 원하는 기능에 고려해서 선택 하시면 될것 같습니다.
{: .text-red-000}

## Just The Docs 실행

---

### Configurations
_config.yaml 파일 생성 후 다음 입력 이외의 설정은 아래의 참고 또는 공식사이트 참조
~~~yaml
remote_theme: just-the-docs/just-the-docs
theme: "just-the-docs"                                                                                   ## 상단 git 링크
~~~
 * 로컬 환경에서는 해당 환경을 세팅 후에 작업하는 거라 remote_theme 부분이 필요 없습니다.
 * github 환경에서는 remote_theme 을 이용해 실제 소스를 Overwrite 하는 방식으로 구현하는 거 같아
 theme 설정을 해줄 경우 원격 theme의 설정이 아닌 해당 설치 사이트에서 소스 내용을 찾아 정상적으로
   작동하지 않는것 같습니다. 
 * 해당 이유로 git 배포 시에는 theme 설정 주석 처리 추천 합니다.
{: .text-red-000}
   
_config.yaml 참고
~~~yaml
remote_theme: just-the-docs/just-the-docs
theme: "just-the-docs"


minimal_mistakes_skin    : "air" # "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise"               ## 사이트 스킨
#logo: "/assets/images/just-the-docs.png"                                                                                      ## 사이트 로고
locale                   : "ko-KR"
title                    : "기술 블로그"
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

### Gemfile
Gemfile 빈 파일 생성 후 다음 스크립트 실행

~~~shell
gem install just-the-docs
gem install webrick
bundle add just-the-docs
bundle add webrick
~~~

### Index
다음과 같이 테스트 용으로 간략한 index.md 파일 생성
~~~
---
layout: default
title: Introduce
nav_order: 1
description: "소개"
permalink: /
---


# 개인 기술 블로그
{: .fs-9 }
~~~

### 실행
jekyll 서버 시작
~~~shell
jekyll serve
~~~

기본 포트인 4000 번으로 접근 [http://localhost:4000](http://localhost:4000) 후 화면 확인

   
![Jekyll Start](/assets/images/story/jekyll-start-img.png)

 * 화면이 뜨지 않을 시 baseurl 설정 확인
{: .text-red-000}


## 마치며

---
처음 써보는 블로그라 내용선정 이라든가 포맷화 라든가 어려운 점등이 많아 생각보다 시간이 오래 걸렸던것 같습니다.

원래 생각은 Jekyll 및 Github 배포 관련해서 한 페이지로 끝내고 Design Pattern 이나 알고리즘쪽으로
올리려 했지만 쓰다보니 내용이 많아져 해당 내용으로만 3페이지 정도 구상중에 있습니다.

일기나 글(정리하는 문서로만 작성)등을 잘 쓰지 않았다보니 뭔가 블로그가 정리하는 느낌이 많이 들긴하지만
앞으로 발전할수 있을것 같다 생각 하며 마무리 하겠습니다.

읽을지는 모르겠지만 누군가에게 도움이 되는 블로그이길 바라며 다음으로는 
3. Jekyll Blog 시작 (3) - github 배포 로 생각 하고 있습니다.

검색 해보면 많이 나오는 내용이라 해당 부분 없이 진행 할까 하다가 github 배포 처리 과정에 대해서는
많이 안나오는거 같아 작성해보도록 하겠습니다.

감사합니다.


<br>

[Jekyll Blog 시작 (1)](/story/jekyll-blog/1){: .float-left .btn .btn-green }

[Jekyll Blog 시작 (3)](/story/jekyll-blog/3){: .float-right .btn .btn-purple }


<br>
<br>
<br>