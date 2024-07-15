---
layout: post
title: 연구 효율 향상을 위한 도구
description: >
    연구 효율 향상을 위한 도구 선택 
image:
  path: /assets/img/resume.png
sitemap: false
hide_last_modified: true
comments: true
---
* toc
{:toc}

## Motivation

 그간 연구를 진행하면서 우여곡절이 많았다. 연구 일정 관리, 환경 정리, 결과 정리 등을 제대로 하지 못해 중복된 일을 한 적도 많다. 또, 협업 연구에서 다른 연구원과의 소통이 원활하지 못해 일정이 지연되는 경우가 많았다. 이러한 삽질을 줄이기 위해 인터넷에서 관련 도구들을 뒤적이며 시간을 보냈다. 결국에는 [옵시디언(Obsidian)][obsidian] 프로그램을 발견하여 이를 지식정리 및 저장에 사용하고 있다. 다양한 플러그인으로 여느 프로그램보다 효율적으로 방대한 데이터베이스를 만들어 가고 있다. 하지만 곧 한계가 드러났다. 프로젝트 관리 기능 및 편의성이 다소 낮고, 오프라인 프로그램이라 연구 내용 공유가 용이하지 않았다. 혼자서 쓰기에는 정말 훌륭하지만 협업에 제약이 커 별도의 도구가 필요하였다.  

[obsidian]: https://obsidian.md/

## Preacquisition

### 연구에 필요한 요소

1. 연구 내용, 결과 등의 정리 및 공유
2. 연구 일정, 단계, 업무 내용 정리 및 공유
3. 연구자 소통

### 도구 선택 요소

1. 오픈소스(OpenSource)
2. 유지 및 보수의 편의성

## Programs

 세상에는 정말 다양한 도구가 많다. 

### 연구 내용 정리

 연구 내용을 정리하고 공유하는데 위키(Wiki)만한 도구는 없다고 생각한다. 다만 다양한 위키엔진 중에서 하나를 선택해야 하는데, 그 종류가 매우 다양하다. 대표적으로 [미디어위키][mediawiki]가 있는데, 소규모 위키로는 적합하지 않아 제외하였다. 수 많은 후보들을 하나씩 찾아 비교한 결과 마크다운을 지원하는 [Wiki.js][wikijs]를 설치하기로 결정하였다.

[mediawiki]: https://www.mediawiki.org/wiki/MediaWiki/ko
[wikijs]: https://js.wiki

### 연구 관리

 단순한 일정 또는 프로젝트 관리 도구는 매우 많다. 한 때는 [옴니포커스][omnifocus]를 사용하기도 하였는데, 협업용으로는 적합하지 않다. 잠깐 [지라(Jira)][jira]도 사용하였는데, 무료 계정의 한계로 사용을 포기하였다. 무료 프로그램 중 [오픈프로젝트(OpenProject)][openproject]를 발견하여 이를 도입하기로 결정 하였다.

[omnifocus]: https://www.omnigroup.com/omnifocus
[jira]: https://www.atlassian.com/software/jira
[openproject]: https://www.openproject.org/

### 소통

 소통 방법은 [슬랙(Slack)][slack]과 같은 메신저 기반과 게시글을 기준으로 소통할 수 있는 포럼으로 구분 하였다.

 사실 메신저의 경우 텔레그램을 이용하려 했다. 따로 서버를 만들지 않고 사용할 수 있고, 윈도우-맥-리눅스 등 어디에서나 사용할 수 있기 때문이다. 다만 국내에서 텔레그램이 범죄에 이용되어 큰 파장을 일으켜 기피하는 메신저가 되었고, 최근 급격히 증가한 스팸을 막을 방도가 마땅치 않으며 슬랙의 기능에 비해 부족한 점이 일부 있기에 제외하였다. [디스코드(Discord)][discord]도 다른 이유로 제외하였다.

 슬랙의 대체 프로그램으로 [매터모스트(MatterMost)][mattermost]를 찾았다. 슬랙과 매우 유사하고, 셀프-호스팅으로 직접 구축하여 사용할 수 있어서 이를 선택하였다.

 포럼의 경우 [디스커스(Discourse)][discourse]를 도입하려 했는데, 설치의 문제로 포기하였다. 그 대체제로 [노드비비(NodeBB)][nodebb]를 선택하였다.

[slack]: https://slack.com
[discord]: https://discord.com
[mattermost]: https://mattermost.com
[discourse]: https://www.discourse.org
[nodbb]: https://nodebb.org

---

## 설치 환경

### Rocky Linux

 현재 컴퓨터에 [Rocky Linux][rockylinux] 9.3 버전이 설치되어 있다. 사실 개인용으로 [우분투(Ubuntu)][ubuntu]가 보다 편하고 문제 해결이 용이하지만, 안정성 및 [ROOT][root], [Geant4][geant4] 등의 사용을 위해 록키리눅스를 설치하였다.

[rockylinux]: https://rockylinux.org
[ubuntu]: https://ubuntu.com
[root]: https://cern.root.ch
[geant4]: https://geant4.web.cern.ch

### 도커(Docker)

 해당 프로그램을 하나의 컴퓨터에 설치하여 서비스하기 위해서 [도커(Docker)][docker]를 도입하였다. 도커를 이용하면 매우 편리하게 테스트, 설치, 업그레이드 등이 용이하다. 특히 [도커-컴포즈(Docker compose)][docker-compose]를 통해 초보자도 쉽게 도커를 이용할 수 있다.
 
[docker]: https://www.docker.com
[docker-compose]: https://docs.docker.com/compose

---

