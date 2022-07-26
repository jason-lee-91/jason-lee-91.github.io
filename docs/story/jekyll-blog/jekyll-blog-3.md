---
layout: default
title: Jekyll Blog 시작 (3) - Windows 설치
nav_order: 3
description: "Jekyll Blog 시작 - Windows 설치"
parent: Jekyll Blog 시작
grand_parent: Story
permalink: /story/jekyll-blog/3
---

<br>

# 설치 환경

---
 - Windows 10 기반으로 작성 되었습니다.



# 목차

---
 - [시작하며](/story/jekyll-blog/3#시작하며)
 - [Ruby 설치](/story/jekyll-blog/3#ruby-설치)
 - [MSYS2 이란](/story/jekyll-blog/3#msys2-이란)
 - [정리](/story/jekyll-blog/3#정리)

## 시작하며

---
시작 하기에 앞서 동료 들에게 블로그를 시작하며 추천을 하니
Windows 환경에서 작업을 하고싶다 하여 내용이 적을것 같지만 중간에 해당 포스팅을 넣게 되었습니다.

처음에는 Windows 환경에서 사용하는 패키징 관리도구인 chocolate 를 사용 하여 작업하려 했지만,

ruby 환경을 맞춰 준후 Gem 환경 변수가 잘 안맞아 해당 포스팅이 필요한 분들이 ruby 개발자 분들은
아닌거 같아 공식 사이트에서 설치하는 방식으로 진행 하게 되었습니다.


## Ruby 설치

---
[공식 사이트](https://rubyinstaller.org/) 에서 WITH DEVKIT (MSYS2 포함) 다운로드 받은 후 설치를 진행합니다.

해당 설치를 진행 하시다 보면 MSYS2 를 추가적으로 설치를 하게 되는데 아래 간단한 설명으로 보시는것과 같이,

패키징 관리 툴인것 같은데 chocolate 를 사용했을 경우에도 해당 툴을 설치하라고 나와 이 부분도 공식 사이트에서
다운받아 설치하게된 이유중 하나 입니다.

추가적으로 더 궁금하신분은 공식 사이트 링크 걸어놨으니 한번 보시는것도 좋을것 같습니다.

## [MSYS2](https://www.msys2.org/) 이란

---
MSYS2 는 기본 Windows 소프트웨어를 구축, 설치 및 실행하기 위한 사용하기 쉬운 환경을 제공하는 도구 및 라이브러리 모음입니다.

이것은 mintty , bash 라는 명령줄 터미널 , git 및 subversion과 같은 버전 제어 시스템, tar 및 awk와 같은 도구, autotools와 같은 빌드 시스템으로 구성되며 모두 Cygwin 의 수정된 버전을 기반으로 합니다 .

이러한 핵심 부분 중 일부가 Cygwin을 기반으로 함에도 불구하고 MSYS2의 주요 초점은 기본 Windows 소프트웨어를 위한 빌드 환경을 제공하고 Cygwin을 사용하는 부분은 최소한으로 유지하는 것입니다. 

MSYS2는 GCC, mingw-w64, CPython, CMake, Meson, OpenSSL, FFmpeg, Rust, Ruby 등을 위한 최신 기본 빌드를 제공합니다.


---
이후 부분은 [Jekyll Blog 시작 (2)](/story/jekyll-blog/2) 의 내용 진행 하시면 됩니다.

## 정리

---
 1. [공식 사이트](https://rubyinstaller.org/) WITH DEVKIT (MSYS2 포함) 다운로드 받은 후 설치
 1. [Jekyll Blog 시작 (2)](/story/jekyll-blog/2) 의 내용 진행


<br>

[Jekyll Blog 시작 (2)](/story/jekyll-blog/2){: .float-left .btn .btn-green }

<br>
<br>
<br>