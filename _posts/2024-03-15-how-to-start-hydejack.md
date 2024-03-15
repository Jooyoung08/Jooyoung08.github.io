---
layout: post
title: Hydejack Pro 테마로 블로그 시작하기 
description: >
    Hydejack Pro 테마를 이용하여 Github Pages로 블로그 배포하는 법
sitemap: false
hide_last_modified: true
---
* toc
{:toc}

## 블로그를 시작하게 된 계기

 각종 정보들을 체계적으로 정리해두지 않아서 다시 찾아보는데 많은 곤욕을 치루었다. 그 와중에 [제텔카스텐](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=322210531)을 접하고 체계적인 지식 및 정보 정리를 시작하였다. (관련 내용은 차차 정리하여 포스팅할 계획이다.) 한 가지 문제는 정리된 정보를 공유하는데 어려움이 있었다. 그래서 Github에 일부 자료 등을 업로드 하였다. 다만 Github는 코드 공유에 특화되어 기타 정보 공유를 원활하게 하기 어렵다. 물론 Wiki 페이지를 지원하지만 사용성 및 접근성이 아쉬웠다.

  정보를 정리 및 공유를 하기에 기존의 블로그 플랫폼을 이용하는 것이 최선이라 결정을 내렸다. 블로그 시작을 결심하였지만 구체적인 계획은 없었다. 우선 무료로 사용할 수 있는 블로그 서비스를 검색하여 그 후기등을 확인하였다. **blogger**, **Tistory**, **velog** 등을 확인하였다. 쉽게 시작할 수 있기 때문에 많은 고민을 하였는데 그 와중에 [Jekyll](https://jekyllrb-ko.github.io/)과 [Github Pages](https://pages.github.com/)를 이용한 블로그 만들기가 내 눈길을 끌었다. 특히, 마크다운으로 글을 쓸 수 있는 장점에 매료되었다. 현재 사용하고 있는 노트 프로그램인 [옵시디언](https://obsidian.md/)의 내용을 빠르고 편리하게 붙여 넣을 수 있을것으로 기대된다.

  Jekyll 기반 블로그를 지원하는 수 많은 테마가 있는데, 유난히 [Hydejack](https://hydejack.com/) 테마에 눈길이 갔다. 이를 사용하는 이들의 블로그를 둘러보니 꽤나 괜찮아보였다. 기본적으로 무료로 사용할 수 있지만, 약간의 비용을 지불하면 Pro 버전을 사용할 수 있다. 완전히 바닥에서 시작하기 때문에 여러 기능을 구현하는데 시간이 오래 걸릴듯하여 곧바로 Pro 버전을 결제하였다. Pro 버전에는 다크모드와 검색기능 등이 포함되어있어 초보자가 빠르게 그럴싸한 블로그를 시작할 수 있다.

## 블로그 시작하기

 이 글은 블로그 시작을 결심하고 진행한 일을 시간순으로 나열하였다. 그러므로 이 페이지를 보고 똑같이 따라하기 보다는 어떤 시행착오가 있었는지 확인하는 것이 좋을듯하다.

### Github

 이미 깃허브에 개발 관련 정보 및 코드 등을 구축하고 있었기 때문에 깃허브에서 블로그를 배포하기로 결정하였다. 깃허브는 1 GB의 저장 공간과 100 GB의 밴드위드를 무료로 제공한다.

 Jekyll을 깃허브로 배포하기 위해서 사전 준비가 필요한데, 이미 잘 설명된 자료가 많기 때문에 이는 생략한다. [Github Pages 준비](https://bbarry-lee.github.io/dev/lets-create-a-github-page-1.html) 포스팅을 참고.

### Jekyll

 사실 지금 생각해보면 Jekyll 기반의 블로그를 만들기로 했으니 Jekyll이 뭔지부터 공부했어야 하는데 그러지 않았다. 그래서 Hydejack 테마를 보고도 제대로 이해하지 못하고 계속 헤매고 말았다. 지금도 잘 이해하지는 못했지만, 이 글을 보는 분들은 우선 Jekyll 관련 자료부터 훑어보는 것을 추천한다.

### Hydejack Pro

 무료로 사용할 수 있는 테마는 깃허브에서 [hydejack-starter-kit](https://github.com/hydecorp/hydejack-starter-kit)을 포크하거나 다운로드 받아서 설치할 수 있다. 유료버전은 README에 안내된 페이지에서 결제 후 다운로드 받는다.

 우선 [설치 매뉴얼](https://hydejack.com/docs/install/)을 보고 따라 했는데, 정확히 이해하지 못해서 시간을 낭비하였다. 깃허브를 통해 배포하므로 설명서의 Github Pages만 따라가면 된다.

 > 깃허브는 자동으로 빌드 및 배포를 해주기 때문에 굳이 로컬에 Jekyll 패키지를 설치할 필요가 없다.
{:.note}

#### 설치

 깃허브 페이지를 이미 만들고, 로컬에 클론을 만들었다고 가정하고 진행한다.

 Hydejack Pro 패키지에 여러 파일과 디렉토리가 존재하는데, starter-kit을 사용하면 된다. 편의상 다음과 같이 진행하였다.

 1. starter-kit 내부에 `#jekyll-theme-hydejack' 디렉토리를 제외한 모든 파일을 깃 디렉토리로 복사한다.
 2. `#jekyll-theme-hydejack' 디렉토리 내부에서 `_config.yml', `jekyll-theme-hydejack.gemspec' 파일을 제외하고 모두 깃 디렉토리로 복사한다.
 3. 중복되는 파일은 그냥 덮어쓴다.

  위 순서대로 진행하더라도 큰 문제는 발생하지 않았다. 다만 그림 파일등이 유실되어 보이지 않았다.
{:.note}

 위 과정이 끝나면 다음과 같은 설정이 필요하다.

#### 설정

 Gemfile에서 다음을 수정한다.

~~~
file: Gemfile

// 기존
gem "jekyll-theme-hydejack", path: "./#jekyll-theme-hydejack"

// 수정
gem "jekyll-theme-hydejack"
~~~

 다음으로 `_config.yml' 파일을 수정한다.

~~~
file: _config.yml

//기존
theme: jekyll-theme-hydejack

//수정
remote_theme: hydecorp/hydejack@v9
~~~

 이것으로 Hydejack 테마 기본 블로그를 배포할 수 있다.

 ~~~git
 git add -A

 git commit -m "Hydejack"

 git push
 ~~~
