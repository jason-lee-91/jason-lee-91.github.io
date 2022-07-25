---
layout: default
title: Jekyll Blog 시작 (1) - Local Jekyll 설치
nav_order: 1
description: "Jekyll Blog 시작 - Local Jekyll 설치"
parent: Jekyll Blog 시작
grand_parent: Etc
permalink: /etc/jekyll-blog/1
---

<br>

# 설치 환경

---
 - Mac 기반으로 작성 되었습니다.



# 목차

---
 - [Local Jekyll 설치](/etc/jekyll-blog/1#local-jekyll-설치)
      - [Ruby 설치](/etc/jekyll-blog/1#ruby-설치)
      - [Homebrew 설치](/etc/jekyll-blog/1#1-homebrew-설치)
      - [rbenv 및 ruby-build 설치](/etc/jekyll-blog/1#2-rbenv-및-ruby-build-설치)
      - [ruby 설치](/etc/jekyll-blog/1#3-ruby-설치)


# Local Jekyll 설치 
[공식 사이트 설치 가이드](https://jekyllrb.com/docs/installation/macos/)

---

## Ruby 설치

### 1. Homebrew 설치
<br>
Homebrew 가 설치 되어 있지 않을경우 아래 command 를 통해 설치 합니다.

~~~shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
~~~

### 2. rbenv 및 ruby-build 설치
<br>
jekyll 공식 사이트 가이드 상에는 가상환경으로 chruby ruby-install 를 설치 하기를 권장하지만

~~~shell
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /Library/Ruby/Gems/2.3.0 directory.
~~~

가이드대로 진행 했을때 위와 같은 에러를 만났습니다.

Ruby를 정확히는 모르지만 짐작하기로는 Ruby 에서 사용하는 패키징 관리 라이브러리인 Gem에 대한 권한이 없다는 메시지 입니다.

Mac에서도 기본적으로 Ruby를 사용 하는것 같고 공식 사이트 상의 가이드대로 따랐을때 가상환경이 잘 잡히지 않은걸로 보이고 
Os상에서 사용하는 기본 라이브러리를 건드리기는 위험 부담이 커 다른 방법을 선택했습니다.

해당 오류 기반으로 구글링을 해보니 chruby ruby-install 가상환경 관련 인것을 알게되었고
또다른 가상환경을 찾아보니 rbenv 를 찾아보니 주로 사용하는 pyenv 와 비슷한것 같아 선택하게 되었습니다.

글을 적으며 생각해보니 환경 설정까지 잡은 후 잡은 환경 변수를 안잡아줘서 그랬던것 같은데 편하신대로 선택하시면 될것 같습니다.

이 경우에는 공식 사이트의 마지막 단계인 jekyll 설치 전 아래 명령어를 추가해 주시면 될것 같습니다.

~~~shell
source ~/.zshrc
gem install jekyll
~~~

이후 아래 commend 사용하여 install rbenv ruby-build 를 설치 후 설치 확인용으로 버전을 확인합니다.

~~~shell
brew install rbenv ruby-build
rbenv versions
~~~
~~~shell
system (set by /Users/{your_name}}/.rbenv/version)
~~~


### 3. ruby 설치
이후 설치 가능한 루비 버전 확인 후 설치 적용을 합니다.
순서는 다음과 같습니다.
~~~shell
rbenv install -l
~~~
~~~shell
2.6.10
2.7.6
3.0.4
3.1.2
jruby-9.3.6.0
mruby-3.1.0
picoruby-3.0.0
rbx-5.0
truffleruby-22.1.0
truffleruby+graalvm-22.1.0
~~~

원하시는 버전 선택 후 설치 후 적용 후 확인
~~~shell
rbenv install 3.1.2
rbenv global 3.1.2
~~~

~~~shell
  system
* 3.1.2 (set by /Users/{your_nmae}/.rbenv/version)
~~~

환경 설정 적용
~~~shell
~/.zshrc
~~~

~~~shell
[[ -d ~/.rbenv  ]] && \
  export PATH=${HOME}/.rbenv/bin:${PATH} && \
  eval "$(rbenv init -)"
~~~

~~~shell
source ~/.zshrc
~~~

<br>

[Jekyll Blog 시작 (2)](/etc/jekyll-blog/2){: .float-right .btn .btn-purple }

<br>
<br>
<br>