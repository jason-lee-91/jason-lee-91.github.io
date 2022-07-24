---
layout: default
title: Jekyll Blog 시작 (2) - Theme 선택 후 반영(just the docs)
nav_order: 2
description: "Jekyll Blog 시작 - Theme 선택 후 반영"
parent: Jekyll Blog 시작
grand_parent: Etc
permalink: /etc/jekyll-blog/2
---

<br>

# 설치 환경

---
 - Mac 기반으로 작성 되었습니다.



# 목차

---
 - [Jekyll Blog 시작 (1) - Local Jekyll 설치](/etc/jekyll-blog/1)
   - [Local Jekyll 설치](/etc/jekyll-blog/1#local-jekyll-설치)
      - [Ruby 설치](/etc/jekyll-blog/1#ruby-설치)
      - [Homebrew 설치](/etc/jekyll-blog/1#1-homebrew-설치)
      - [rbenv 및 ruby-build 설치](/etc/jekyll-blog/1#2-rbenv-및-ruby-build-설치)
      - [ruby 설치](/etc/jekyll-blog/1#3-ruby-설치)
   - [Jekyll 설치](/etc/jekyll-blog/1#jeykill-설치)


## Jekyll Theme 선택[ just-the-docs ]
---
다음 사이트 또는 추가적인 사이트에서 원하는 Theme 을 선택
 - https://github.com/topics/jekyll-theme [보러가기](https://github.com/topics/jekyll-theme)
 - http://jekyllthemes.org/ [보러가기](http://jekyllthemes.org/)

---
 * 저는 기술 블로그가 목적이였고 UI 가 심플함, 검색 기능 지원 의 이유로 just the docs 선택했지만
지원되지 않는 MarkDown 기능( > 등 ..) 이 있어 원하는 기능에 고려해서 선택 하시면 될것 같습니다.
{: .text-red-000}

## 반영
_config.yml 파일 생성 후 다음 입력
~~~
remote_theme: just-the-docs/just-the-docs
theme: just-the-docs                        ## github 배포시 주석 처리
~~~

~~~shell
gem install just-the-docs

gem "just-the-docs"
gem install webrick
~~~

<br>

[Jekyll Blog 시작 (1)](/etc/jekyll-blog/1){: .float-left .btn .btn-outline }

[comment]: <> ([Jekyll Blog 시작 &#40;3&#41;]&#40;/etc/jekyll-blog/3&#41;{: .float-right .btn .btn-outline })
{: .float: right }

<br>
<br>
<br>