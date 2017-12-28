---
layout: post_study
title:  PYTHON 시작전 알아둘 사항
date: 2017-12-28 02:01:00
---
# 파이썬 프로그래밍

프로그래밍이란 크게 세가지 절차를 거친다. 데이터를 입력 받고, 입력받은 데이터를 여러 과정을 거쳐 처리하고, 처리된 데이터를 출력하는 과정이다. 입력의 방식은 단순하게 키보드, 파일등이 될 수 있으며, 처리과정은 우리가 일상생활에서 어떠한 일을 처리하기 위한 계산(연산), 반복, 조건등이 반복되게 되며, 그 결과값이 화면이나 프린터등을 이용하여 출력하게 된는 과정을 컴퓨터 언어로 구현하는 것을 의미한다. 파이썬 설치에서 언급한 것처럼 파이썬은 기존의 프로그래밍언어의 복잡성을 최소화 하여 최대한 단순하게 설계된 언어로써 상대적으로 배우기 쉬운 문법체계를 가지고 있다.
<br/>
파이썬 프로그래밍을 하기 위하여 파이썬을 설치하였다면, 옵션중 ‘tcl/tk IDLE’을 설정하여 파이썬 통합개발환경(Integrated Development Environment)을 설치할 수 있는 것을 알 수 있다. 편집기는 단순하게 IDLE 뿐만 아니라 메모장, Notepad++, PyCharm, Visual Studio 등 다양한 편집기를 사용할 수 있으며, 편의에 따라 편집기는 선택하면 된다. 본 과정에서는 파이썬 IDLE를 사용하도록 하겠다.

## 1.	시작하기 전에 알아둘 사항
### 1.1	파이썬 IDLE 사용법

먼저 [그림 1]처럼 파이썬 메뉴에서 IDLE를 실행한다.
<br/>
![](/asset/study/python_basic/2/1.png)
[그림 1] Python 3.5 메뉴
<br/>
파이썬 IDLE를 실행시키면 [그림 2]와 같이 파이썬 IDLE가 실행된다.
<br/>
![](/asset/study/python_basic/2/2.png)
[그림 2] 파이썬 IDLE 환경
<br/>
파이썬 IDLE는 크게 2가지 부분으로 구성된다. 한 부분은 쉘(Shell)이라고 부르는 파이썬이 실행되는 창과 편집기(Editor) 창으로 구성된다. 파이썬 쉘에 나타나는 ‘>>>’ 모양을 프롬프트(prompt)고 한다. 쉘 프롬프트에 [그림 3]과 같이 입력한다.
<br/>
![](/asset/study/python_basic/2/3.png)
[그림 3] 문자열 출력

우리는 print 라는 출력함수를 이용하여 “파이썬 시작”이라는 문자열을 화면에 출력해 보았다(문자열의 처리 등은 후에 설명할 것이니 너무 걱정하지 말자). 여기서 엔터를 치자마자 화면에 “파이썬 시작” 이라는 글자가 화면에 출력되었는데 파이썬 쉘에서는 엔터를 치면 바로 파이썬 인터프리터가 바로 그 명령을 수행하는 구조로 되어 있다. 우리는 필요에 따라서 데이터를 입력받고, 처리하고 출력하는 과정을 프로그래밍해야 하는데 이렇게 엔터를 입력할 때 마다 바로 바로 처리가 되게 되면 문제가 발생한다. 이를 위해서 파이썬 프로그램 파일을 작성하고 이를 한꺼번에 처리하기 위한 방법이 필요하다.
<br/>
![](/asset/study/python_basic/2/4.png)
[그림 4] 파이썬 파일의 생성
<br/>
[그림 4]와 같이 상단의 [File] >> [New File]을 선택하면 [그림 5]와 같이 편집기 창이 나타난다.
<br/>
![](/asset/study/python_basic/2/5.png)
[그림 5] 파이썬 프로그램 편집기
<br/>
편집창에 [그림 5]와 같이 입력한 후 [File]의 [Save]를 선택하면 [그림 6]과 같이 저장 대화상자가 나타난다. PC의 특정 위치에 저장할 파일명을 입력한 후 [저장]버튼을 누른다.
<br/>
![](/asset/study/python_basic/2/5.png)
[그림 6] 작성된 파일의 저장 대화 상자
<br/>
저장이 완료된 후 [그림 7]과 같이 메뉴의 [Run] >> [Run Module]을 선택한다.
<br/>
![](/asset/study/python_basic/2/6.png)
[그림 7] 작성한 프로그램의 실행
<br/>
에러가 없이 정상적으로 입력되었다면 [그림 8]과 같이 파이썬 쉘에 결과값이 나타날 것이다.
<br/>
![](/asset/study/python_basic/2/8.png)
[그림 8] 저장된 파일에서 파이썬의 실행 결과 출력
<br/>
[그림 8]에서 보듯이 파이썬 쉘에서는 저장된 위치의 파일을 실행시키고, 그 결과값을 화면에 출력하였다.
![](/asset/study/python_basic/2/6.png)
<br/>
<br/>
##1.2	기본 규칙
파이썬 프로그래밍에 있어서는 몇 가지 규칙이 존재한다.
<br/>
#### 1)	한줄에 하나의 명령어 입력이 원칙
일반적으로 하나의 명령은 한줄에 기입한다. 만약 두개의 명령을 한줄에 쓰게 되는 경우에는 ; 기호를 이용하여 분리한다. 한 행에 여러 개의 명령어를 입력할 수 있지만 이런 방식은 나중에 프로그램을 분석할 때 혼돈이 생기므로 가급적 사용하지 않는 것이 좋다.
```
>>> a = 1
>>> b = 2
>>> print (a+b)
3
>>> c=3;d=4;print(c+4)
7
>>>
```
<br/>
####2)	들여쓰기
파이썬에서는 공백(space)이 상당히 중요한 역할을 한다. 다음의 예에서는 프롬프트 뒤에 스페이스바를 이용하여 공백을 하나 입력한 후 print 함수를 입력한 예이다.
```
>>>  print ("공백")
SyntaxError: unexpected indent
>>>
```
친절하게 파이썬에서는 들여쓰기(indentation)이 잘못되었다고 오류를 출력한다. 하나의 명령어에 하위로 따라오는 명령어 - 이렇게 구성되는 것을 블록(block)이라고 한다 - 는뒤에 반복문 또는 제어문에서 설명할 것이다. 블록을 구성할 때는 하위 명령어들은 반듯이 [Tab]키를 이용하여 들여쓰거나 스페이스바를 이용하여 4칸을 들여써야 한다.
<br/>
####3)	주석(Comment)
주석(comment)은 프로그래밍 명령과는 상관없이 프로그램을 작성하면서 설명을 기입할 때 사용한다. 프로그램은 작성후 다른 사람이 코드를 볼 수 있으며, 필요에 따라 유지보수가 필요한 경우가 발생하는데 이때 주석을 표기해 놓으면 많은 도움이 된다. 주석은 # 표시 뒤에 기록한다.
```
>>> print("파이썬 시작") #주석
파이썬 시작
>>> #주석표시가 된 부분은 파이썬 인터프리터에서 해석하지 않는다
>>> print(“파이썬 시작”)
파이썬 시작
```
<br/>
####4)	함수(function)
우리가 중학교때 배운 함수를 기억하자. ‘y = 3x + 1’이라는 함수가 있다고 생각해 보자. 우리는 x에 특정값을 입력하면 y의 값을 얻을 수 있다(x=3, y=10). 동일한 개념으로 프로그래밍에서 함수(function)는 어떤 값을 입력하면 특정한 값을 반환하는 역할을 한다. 프로그램에서 모든것을 다 스스로 처리하려면 프로그래밍은 너무 어렵고 고통스러운 작업일 것이다. 이런 불편함을 해소하기 위해서 파이썬에서는 많이 쓰는 기능들을 함수로 미리 만들어 놓고 제공한다. 앞에서 print()라는 것이 함수로써 문자열을 입력하면 화면에 출력하는 것을 보면 쉽게 이해가 갈 것이다.