---
layout: post
title: Hydejack Pro, Resume 편집하기 
description: >
    Hydejack Pro 테마에서 지원하는 Resume 편집 방법
image:
  path: /assets/img/resume.png
sitemap: false
hide_last_modified: true
---
* toc
{:toc}

## Resume 편집하기

 Hydejack Pro 버전은 resume 기능을 제공한다. 사실 About.md를 편집하여 resume 처럼 사용할 수 있지만, 해당 기능을 사용하면 손 쉽게 깔끔한 이력서를 작성할 수 있다.

### resume 관련 파일 장소

 * resume.md
 * \_include/pro/resume
 * \_layouts/resume.html
 * \_data/resume.yml
 * \_data/strings.yml

### 이력서 작성 기본

 Resume 관련 파일이 생각보다 많은데,
 우선 기본적인 편집은 \_data/resume.yml에서 할 수 있다.
 제공된 샘플 파일 또는 [깃허브][sample]을 참고하여 작성한다.

[sample]: https://github.com/hydecorp/hydejack-site/blob/master/_data/resume.yml

#### Basics

 기본 정보에는 다음과 같은 정보를 작성할 수 있다.

 * 이름   : Resume 페이지에 표시되는 이름
 * 라벨   : 이름 밑에 표시되는 내용
 * 사진 
 * 이메일
 * 전화번호
 * 웹사이트
 * 요약
 * 장소
   * countryCode  : "KR"과 같이 두 자리로 표현
 * 프로파일

> 굳이 게시하고 싶지 않은 항목은 지워버리거나 \# 으로 주석 처리 한다.
{:.note}

대략적인 구조는 다음과 같다.

 ~~~
basics:
  name:
  label:
  ...
  location:
    address:
	postalCode:
	...
  profiles:
    - network:
	  username:
	  url:
 ~~~

> 하위 정보는 상위 정보 아래 라인에서 두 칸을 띄우고 작성한다.
{:.note}

 프로파일에 여러 소셜 정보를 추가할 수 있다.
 간단한 예제는 다음과 같다.
 
 ~~~
 - network: "GitHub"
   username: "Jooyoung08"
   url: "https://github.com/Jooyoung08"
 ~~~

 여기서 network의 이름이 \_data/social.yml에 있는경우 이를 사용한다.
 그러면 자동으로 해당 아이콘이 표시된다.
 username은 resume 페이지에 표시되는 내용이다.
 url을 설정하면 해당 링크가 삽입된다.

#### Work

 현재 직장 및 과거 직장 정보를 작성할 수 있다.

~~~
work:
  - company: "직장 이름"
    position:
	website:
	startDate:
	endDate:
	summary: >
	highlights:
	  - "표시 내용"
~~~

> endDate를 작성하지 않으면 현재(present)로 표시된다.
{:.note}

#### Education

 학력을 작성할 수 있다.

~~~
education:
  - institution:
    area:
	studyType:
	...
~~~

 학점(GPA)을 작성하지 않았는데 resume 페이지에서 GPA 항목만 사라지고 **with GPA of** 문장은 그대로 남아있었다.
이는 \_data/strings.yml 에서 education_title 항목을 편집하여 삭제할 수 있다. 
 
#### 기타

 이 외에도 awards, publications, skills, languages, interests, references를 작성할 수 있다.
skills, languages에서는 자신의 레벨을 별표로 표시할 수 있다. [참고자료][skill]

예시는 다음과 같다.

~~~
skills:
  - name: "Programming Language"
    level: "1/3"
	keywords:
	  - "C++"
	  - "Python"
	  - "RUST"

languages:
  - language: "Korean"
    fluency: "5/5"
~~~

[skill]: https://hydejack.com/docs/basics/#skill-level-icons
