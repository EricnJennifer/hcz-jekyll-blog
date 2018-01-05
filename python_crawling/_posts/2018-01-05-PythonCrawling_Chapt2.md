---
layout: post_study
title:  1. Facebook API 사용등록
date: 2018-01-05 02:01:00
categories: python_crawling
---
## 1. Facebook API 사용등록
<br/><br/>

페이스북(Facebook)은 하버드 대학교의 학생이었던 마크 저커버그가 2003년에 페이스매시(Facemash)라는 이름으로 시작하여 2004년 2월 “더 페이스북(TheFaceBook)”이라는 이름으로 본격적인 서비스를 시작하였다. 서비스 초기에는 하버드 대학내의 학생들이 서로의 개인 정보와 글, 동영상 등을 상호 교류하는 인맥 서비스(Social Network Service)를 목적이였으며 스탠퍼드, 컬럼비아 및 예일 대학으로 서비스를 확대하고 그 이후 미국 전역의 대학으로 서비스가 확장되면서 현재 전세계적으로 가장 많이 사용하고 있는 서비스이다.
<br/><br/>

서비스 주요 기능으로는 뉴스피드, 타임라인 등이 있다.
<br/><br/>
<br/><br/>

#### 1) 뉴스 피드(News Feed)
<br/><br/>
뉴스 피드는 사용자의 친구, 내가 읽은 기사중 ‘좋아요’를 선택한 페이지의 소식을 시간순으로 서비스 한다. 뉴스피드에 나타나는 소식의 중요도는 절대로 시간순이 아니라 페이스북에서 자체 개발한 알고리즘에 의하여 배치 순서가 결정되는데 이에 대한 기준은 기업 비밀로 관리되고 있다.
<br/><br/>
#### 2) 타임 라인(Time Line)
<br/><br/>
사용자가 게시하는 사진, 글 및 동영상등을 실시간, 시간순으로 보여주는 서비스이다. 뉴스피드에 있는 대부분의 소식은 사용자의 친구들 또는 ‘좋아요’를 선택한 페이지 이지만 타임라인은 자신이 올린글을 서비스한다. 
<br/><br/>
<br/><br/>

페이스북은 가입시에 성별, 생년월일 등을 반드시 입력하여야 하며, 이를 통해 개인 페이지가 만들어지게 되어 일정의 마이크로 블로그(micro blog)의 형식을 가지게 된다.
이제 페이스북에 가입하고 개발자 앱 ID를 생성하는 방법을 알아보자. 만약 페이스북의 계정을 가지고 있는 사용자라면 1.1절은 스킵하고 1.2로 이동하기 바란다.
<br/><br/>
<br/><br/>

### 1.1 페이스북 가입
<br/><br/>

페이스북은 개인 페이지를 생성하게 되므로 가입시 개인 정보를 입력하여야 한다. 먼저 페이스북 홈페이지(http://www.facebook.com)으로 이동하면 가입 페이지가 [그림 1]과 같이 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/1.jpg)
[그림 1] 페이스북 사용자 가입 페이지
{: .borderBox}
<br/><br/>

자신의 성과 이름, 휴대폰 번호 또는 이메일과 비밀번호, 생일과 성별을 입력하고 [계정 만들기] 버튼을 클릭하면 [그림 2]와 같이 사용자 이용약관 페이지가 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/2.jpg)
[그림 2] 이용 약관 및 보안 코드 입력
{: .borderBox}
<br/><br/>

이용약관 및 개인정보 처리 방지 지침에 대한 동의를 하고, 보안 확인 코드 문자열을 넣어준 후 하단의 [가입하기] 버튼을 클릭하면 보안코드 입력 페이지가 [그림 3]처럼 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/3.jpg)
[그림 3] 보안 코드 입력
{: .borderBox}
<br/><br/>

보안 코드를 입력하기 위하여 가입시 사용한 이메일을 확인한다. 만약 전화번호를 사용하였다면 인증 코드가 해당 전화번호 문자메시지로 발송된다
<br/><br/>

![](/asset/study/python_crawling/2/4.jpg)
[그림 4] 보안 코드 수신 확인
{: .borderBox}
<br/><br/>

이메일이나 문자로 수신한 보안코드를 [그림 3]의 입력창에 넣은 후 [계속] 버튼을 클릭하면 [그림 5]와 같이 정상적으로 등록된 것을 확인할 수 있다.
<br/><br/>

![](/asset/study/python_crawling/2/5.jpg)
[그림 5] 페이스북 로그인 완료
{: .borderBox}
<br/><br/>

이제 기본적으로 페이스북에 계정이 생성되었으므로 개발자 계정을 얻도록 한다. 개발자 계정이란 서비스를 제공하는 업체에서 서비스를 이용하여 편리한 제 3의 프로그램(3rd party solution)을 제작하는데 편리한 기능을 제공해 주는 API(Application Program Interface)를 사용할 수 있도록 허락하는 것이다.
<br/><br/>
개발자 계정을 얻기 위하여 페이스북 개발자 페이지(http://developer.facebook.com)을 접속하면 [그림 6]과 같이 개발자 페이지로 이동할 수 있다.
<br/><br/>
<br/><br/>

### 1.2 Facebook API 사용등록
<br/><br/>

![](/asset/study/python_crawling/2/6.jpg)
[그림 6] 페이스북 개발자 페이지
{: .borderBox}
<br/><br/>

이미 페이스북에 계정을 만들고 로그인을 하였으므로 브라우저에 쿠키가 남아 있어 자동으로 로그인된 상태임을 확인할 수 있다. [그림 6]의 하단에 보면 페이스북에서 제공해 주는 Facebook 로그인, Facebook에서 공유하기 등의 바로가기 메뉴 뿐만 아니라 제공해주는 모든 서비스를 확인할 수 있다.
<br/><br/>
우리의 목적은 페이스북의 내용을 크롤링(Crawling)하는 것이 목적이므로 새로운 앱(App)을 하나 등록하기로 한다. 화면 상단의 [내 앱] 부분을 클릭하면 다음과 같이 새로운 앱을 만들 수 있는 메뉴가 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/7.jpg)
[그림 7] 새 앱 추가 선택하기
{: .borderBox}
<br/><br/>

[새 앱 추가]를 선택하면 [그림 8]과 같이 “새 앱 ID 만들기” 창이 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/8.jpg)
[그림 8] 새 앱 ID 만들기
{: .borderBox}
<br/><br/>

표시이름은 앱의 고유 이름으로 다른 사람이 사용하지 않는 고유 이름이여야 한다. 카테고리중 마음에 드는 부분을 선택하고 [앱 ID 만들기]를 선택하면 [그림 9]와 같이 보안 코드를 입력하라는 창이 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/9.jpg)
[그림 9] 보안 코드 입력
{: .borderBox}
<br/><br/>

보안 코드를 입력한 후 [제출]버튼을 클릭하면 [그림 10]과 같이 사용할 제품에 대한 설정 페이지로 이동한다.
<br/><br/>

![](/asset/study/python_crawling/2/10.jpg)
[그림 10] 사용할 App의 제품 설정 페이지
{: .borderBox}
<br/><br/>

[그림 10]의 왼쪽 상단에 보면 입력한 App의 이름이 나타나면 정상적으로 서비스 생성이 완료된것이다(필자는 snsCrawler라고 App 표시 이름을 만들었다). 페이스북은 자신들이 서비스하는 거의 모든 내용에 대한 접근을 허용하는 서비스 API를 제공해 준다. 다양한 형태의 서비스가 있지만, 일단 화면 왼쪽 메뉴의 [대시보드]를 선택하면 [그림 11]과 같이 만들어진 앱의 기본 정보를 확인할 수 있다.
<br/><br/>

![](/asset/study/python_crawling/2/11.jpg)
[그림 11] 새로운 앱(snsCrawler) 생성
{: .borderBox}
<br/><br/>

생성된 앱의 ID와 시크릿 코드([보기] 버튼을 누르면 복사할 수 있는 텍스트 형태로 나타난다)는 제작할 크롤러에서 사용되게 되므로 기억하여야 하며, 다른 사람에게 노출될 경우 악용될 수 있기 때문에 잘 보관하여야 한다. 우리는 단순하게 페이지를 크롤링하기 때문에 별도의 제품을 추가할 필요는 없으며 기본 설정으로 페이스북에 접근할 권한을 획득하였다.




