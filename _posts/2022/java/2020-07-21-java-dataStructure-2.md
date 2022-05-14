---
title: Java 전자정부프레임워크 4.0.0 세팅
layout: single
author_profile: true
read_time: true
comments: true
share: true
related: true
categories:
- JAVA
description: 개발자로서 필요한 자료구조란 무엇인지 기본적인 사항에 관해 정리해보겠습니다.
article_tag1: 전자정부프레임워크 4.0.0 설정
article_section: 전자정부프레임워크
meta_keywords: 전자정부프레임워크 4.0.0, CMS, Eclipse, 이클립스, 자바, JAVA, Tomcat, 설정
toc: true
toc_sticky: true
toc_label: 목차
---

# 전자정부프레임워크 4.0.0 (CMS) 세팅

### 소개
회사에서 Java 과제를 내줬다 그 과제는 자바라곤 class밖에 모르는 사람한테 1주일만에 JSTL과 @Controller를 사용하여
캘린더를 만들라는 것이다.. <br>
하지만 그 전에 회사 CMS에 관한 걸 배워서 이 포스트를 쓰려고 한다 기억이 가물가물해서 틀린 부분이 분명히 있을 것이다
나중에 수정하겠다!
<br>
## 전자정부프레임워크
전자정부 표준프레임워크는 대한민국의 공공부문 정보화 사업 시 플랫폼별 표준화된 개발 프레임워크를 말한다. JAVA 언어는 사설 표준으로 우후죽순으로 업체의 자체 프레임워크를 개발하여 적용되다 보니 각 개발프레임워크의 구조 및 수준의 차이에 의하여 여러 가지 문제점이 발생할 수 있다 - 위키백과 <br>

라고 한다.
일단 이걸 쓰기 위해선 설치를 해야 한다 그럼 가보자
그리고 이 포스팅을 보는 사람들은 적어도 Java의 기본 지식은 있다고 가정하기때문에
JDK의 설치와 설정은 따로 포스팅을 하지 않겠다
<br>

### 전자정부프레임워크 설치
다운로드는 [여기](https://www.egovframe.go.kr/home/sub.do?menuNo=94)에서 자신의 운영체제의 맞는 걸 다운받도록 하자<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/1.png){: .align-center .open-new}
<br>
### 톰캣 설치
서버도 필요할테니 Tomcat을 쓰도록 하자!<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/2.png){: .align-center .open-new}<br><br>
Tomcat 버전은 9버전으로 [여기](https://tomcat.apache.org/download-90.cgi)에서 다운로드 받을 수 있다<br>
코어에 있는 링크를 누르면 됐던 것 같다 
<br>

## Eclipse 설정
프레임워크를 다운 받고 압축을 풀었다면 **eclipse**, **workspace** 이 두 개의 폴더가 있을 것이다
eclipse 폴더에 들어가서 eclipse가 잘 실행이 되는지 확인해준다 안 된다면 *나도 모른다 난 한 번에 잘 되어서..*<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/3.png){: .align-center .open-new}<br><br>
잘 켜진다면 Workspace에 작업 폴더를 만들어주자 나 같은 경우엔 <br>
 **workspace/자신이 쓰고 싶은 폴더 이름** 으로 설정했다 지금까지 잘 따라왔다면 요 화면이 뜰 것이다<br><br>
 ![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/4.png){: .align-center .open-new}<br><br>
원래 스프링 머시기가 떴던 것 같은데 지금은 안 뜬다 한 번 해서 그런가 싶다  ++추가 다음 날 해보니 떴당<br><br>
 ![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/13.png){: .align-center .open-new}<br><br>
그리고 CMS를 쓴다면 SourceTree를 다운받아서 쓰는 걸 추천한다 <br>
SourceTree에 관한 내용은 이따가 다루겠다
<br>

### Eclipse Tomcat Connect
이제는 톰캣과 eclipse를 연결해주겠다 <br>
Windows - Preferences 를 누르면 <br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/5.png){: .align-center .open-new} <br><br>
이런 창이 뜬다 <br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/6.png){: .align-center .open-new} <br><br>
여기에서 Web Service - Server and Runtime 에서 9버전으로 맞추고 <br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/7.png){: .align-center .open-new} <br><br>
Server - Runtime Environment - Add - Apache, Tomcat 버전 선택 후  <br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/8.png){: .align-center .open-new} <br><br>
Server가 없을 경우 New Local Server 체크 후에 JRE 경로 설정 하고 <br>
다운로드 받은 Tomcat 루트를 설정해주면 끗!
<br>

### Eclipse File Import (Use SourceTree)
이클립스 파일 임포트에 관한 설정이다 일단 나는 CMS를 쓸 것이기 때문에 SourceTree를 쓰것다 <br><br>
SourceTree 다운로드는 [여기](https://www.sourcetreeapp.com/)에서 할 수 있다<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/9.png){: .align-center .open-new}<br><br>
다운로드 후 실행시키면 오른쪽 위에 설정을 누른다 그럼<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/10.png){: .align-center .open-new}<br><br>
요런 화면이 뜨는데 추가를 눌러서 원격 저장소의 Repo URL을 입력해서 연동해준다<br>
그리고 설정 - 고급 탭에서 .gitignore의 위치를 확인하면 SourceTree와 연동된 파일의 위치를 알 수 있다
그럼 그 파일의 위치를 Eclipse의 FIle - import를 눌러서<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/11.png){: .align-center .open-new}<br><br>
Maven 폴더에 Existing Maven Projects 를 선택한다 다른 Blog를 보면 General폴더를 쓰던데 나는 이렇게 배웠다<br>
여튼 그럼 이 창이 뜨는데<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/12.png){: .align-center .open-new}<br><br>
Root Directory 아까 SourceTree에서 확인한 경로를 넣어주면 <br>
Projects에 SourceTree에서 연동한 BONOBO 라던가 다른 Server에 있는 Project들이 뜰 것이다<br>
이제 Finish를 눌러주면 파일 불러오기는 끗!
<br>

### Tomcat Server Create and FIle connect
이제 톰캣이랑 가져온 파일이랑 연결해야겠다 아래 탑에 Server를 눌러본다 그럼 
> **No Server are available. Click here this link to create  a new server..**

라는 파란 글씨가 보인다 클릭하면 <br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/14.png){: .align-center .open-new}<br><br>
요것과 같은 화면이 보인다 본 화면은 톰캣을 Eclipse에 연결할 떄 했던 것 처럼 <br>
apache에서 톰캣을 버전에 맞게 선택한 화면이다 Next를 누르면<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/15.png){: .align-center .open-new}<br><br>
요런 화면이 뜨는데 상횡에 따라서 이 화면은 안 뜰 수도 있다 <br>
본 화면은 Tomcat Installation directory 에서 톰캣 경로까지 설정해준 화면이다<br>
JRE도 설정해주고 Next를 누르면 <br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/16.png){: .align-center .open-new}<br><br>
요런 화면이 뜨는디 다 추가해주고 된다면 밑에서 파일 다루는 파트는 건너뛰어도 될 것이다<br>
아마 대부분의 사람들은 안 될 것이다 그래서 파일 설정을 해주도록 하겠다
<br>

### File Setting
일단 추가가 안 되는 프로젝트 폴더를 우클릭하면 맨 아래에 Properties 가 뜨는데 그걸 누르면
아까 본 익숙한 창이 뜰 것이다 그럼 Java Build Path에 Libraries탭에 들어가면<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/17.png){: .align-center .open-new}<br><br>
이런 화면이 뜨는디 우리의 전자정부 4.0.0은 (JDK는 11 버전 사용이 필수) 라고 한다.. JRE도 같은 것 같다<br>
나는 JRE 버전이 15버전으로 떠서 11버전으로 맞춰주것다.
Classpath - JRE System Libray를 클릭하고 오른쪽에 Edit을 누르면<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/18.png){: .align-center .open-new}<br><br>
요런 화면이 뜨는디 Execution encironment  실행 환경의 인풋 박스를 클릭하면 여러가지 버전이 뜰 것이다<br>
그러면 11버전으로 클릭해서 바꿔주고<br>
Alternate JRE도 Installed JREs.... 를 눌러서 11버전을 맞춰준다 그리고<br>
이건 꼭 해야 하는 지는 모르겠는데 **.jar** 파일을 설정해주겟다<br><br>
다시 Java Build Path에 Libraries탭에 들어가서 ModulePath를 클릭해주고 오른쪽 버튼중 Add Jars.. 를 눌러준다 그럼
<br><br>![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/19.png){: .align-center .open-new}<br><br>
요런 창이 뜨는디 자신이 불러온 CMS 파일 중에서 위에 Search 창에서 *.jar 을 검색하면 찾을 수 있다<br>
그리고 제일 중요한 파트가 남았다 바로 지금까지 불러온 친구들을 Java Build Path 에서 Oroder and Export 탭에서 <br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/20.png){: .align-center .open-new}<br><br>
고냥 다 활성화를 시켜준다 그러면 파일 설정은 끗<br>
이제 다시 톰캣 서버 파트로 가보겠다
<br>


### Tomcat Setting
아래의 Server 탭에서 만들어진 Tomcat Server를 더블클릭을 해보자 그러면<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/21.png){: .align-center .open-new}<br><br>
이런 화면이 뜰 것이다 요기서 Timout 탭을 누르면<br>
*** Start와 Stop*** Seconds가 보일 것이당 전자정부는 굉장히 무겁기 떄문에 저 초들을 2배로 늘려줄 것이다<br>
Default 값은 45와 15일텐데 90이랑 30으로 맞춰준다 이렇게 하는 **이유**는<br>
아마 안전..? 이였나 까먹어버렸다 월요일날 물어봐서 수정하겠다..! 여튼, <br>
여튼 그 아래 Port 탭에서 Port Number중에 쓰고 있는 포트가 있는지 확인하고 없다면 그대로 두면 된다<br><br>
이제 Overview가 아닌 Module 탭에 들어가면<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/22.png){: .align-center .open-new}<br><br>
요렇게 뜬다 그럼 회사에서 그 도메인이 있을긴데 우리는 /이랑 /m***** 이다 혹시 몰라서 삐처리 했다<br>
요 도메인을 설정해주겟다 설정해줄 파일들을 클릭해서 Edit 버튼을 누르면<br><br>
![img]({{ site.url }}{{ site.baseurl }}/assets/images/post/java/23.png){: .align-center .open-new}<br><br>
이런 것이 뜨는디 여기서 Path값을 바꿔주고 <br>
세이브 후 Server 탭에 Tomcat을 우클릭 후 Start를 누르고 localhost:port 에 들어가보면 뜰 것이다!<br>

## Error
스타트 시키고 로컬에 들어가봤는데 안 뜨는 에러가 생길 것이다<br>
콘솔 창에 보면 매핑이 안 된다는 오류가 뜨는 사람이 있을텐데 이걸 분명 해결했었는데 까먹었다.
이래서 TIL이 킹갓짱짱이다 습관을 들여야겠다 이 부분도 월요일날 물어보고 다시 쓰겠다

## 마무리
이제 아마 세팅은 다 끝난 것 같다 인생 처음으로 배운 세팅이고 인생 처음으로 쓰는 블로그라 여러 가지 부족한 점이 많은 것 같다<br> 앞으로 열심히 공부를 해서 완벽한 정보를 전달할 수 있는 블로그를 쓰는 게 내 목표이다<br>
그리고 눈치 채신 분들이 있을 수 있는디 지금 오른쪽에 있는 목차가 제대로 작동하지 않는다 이것도 나중에 고치겠다 그럼 20000!
