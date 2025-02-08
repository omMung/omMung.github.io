---
title: "JavaScript-1"
excerpt: "JavaScript-1"

categories:
  - JavaScript
tags:
  - [JavaScript]

toc: true
toc_sticky: true

date: 2024-10-31
last_modified_at: 2024-10-31
---

## JavaScript

    JavaScript란 객체지향 스크립팅 언어이다

JavaScript에서는 Promise라는 생성된 시점에는 정의되지 않은 값을 **위한** **대리값이** 존재한다.
또한 비동기 연산이 종료된 후 결과 값과 실패사유를 처리하기 **위한** **처리기를** 연결할 수 있다.
Promise를 사용하면 비동기 메서드에서 마치 동기 메서드를 이용하는 것처럼 값을 반환할 수 있는데, 최종 결과를 반환하는 것이 아닌, 미래의 어떤 시점에서의 결과를 제공하는 Promise를 반환한다.

## JavaScript의 역사

    놀랍게도 JavaScript는 Java와 전혀 관련이 없다!

⚙️ JavaScript의 발전 과정

```markdown
- 1995년 자바스크립트 탄생
  - 🌐 넷스케이프 커뮤니케이션(LiveScript → Javascript)
  - 🖥️ 브라우저 동작 스크립트 언어
- 1999년 자바스크립트 표준화(ECMA-262) 완료
- 2005년 AJAX 등장
  - 비동기 웹 애플리케이션 개발 가능
  - 폭발적인 UX 향상 🚀
- 2008년 V8 엔진 출시(google)
  - super fast(코드 실행 속도 상당부분 개선)
  - 🛠️ 컴파일러, 메모리관리 시스템 👍
- 2009년 Node.js 등장, 서버 개발 활성화
  - 서버개발의 지각변동 : PHP, Ruby, Python, Java → **Javascript(Node.js)**
  - 하나의 언어 → FrontEnd + BackEnd + DB(MongoDB) = FullStack
- 2015년 ECMAScript 6(ES6) 버전 출시 🚀
- 2016년 프론트엔드 프레임워크(React, Vue, Angular) 대중화, SPA 개발 활성화 🌟
- 자바스크립트는 프론트엔드 및 백엔드 개발 분야에서 사용되고, Node.js를 이용한 서버 개발 또한 가능하다.
```

## JavaScript의 특징

1. **객체 지향 프로그래밍 지원**
   - 객체 지향이 뭘까?
     객체 지향이란 데이터와 함수를 객체로 묶어서 처리하는 방식으로 객체는 속성과 매소드를 추가하여 사용한다.
2. **동적 타이핑**
   - 변수를 선언할 때 타입을 지정하지 않고 런타임 시점에 변수에 할당되는 값에 따라 자동으로 데이터 타입이 결정 된다.
3. **함수형 프로그래밍 지원**
   - 함수를 일급 객체로 취급하며, 고차 함수를 지원하는 언어로 코드의 재사용성과 가독성을 높였다.
4. **비동기 처리**
   - 작업을 순차적으로 진행하지 않고, 병렬처리 하는 방식을 지원한다.
5. **클라이언트 측 및 서버 측 모두 사용 가능한 언어**
   - 클라이언트에서만 사용되는 것이 아닌 Node.js를 이용해 서버에서도 사용가능하여, 웹 개발 전반에 활용할 수 있다.

## JavaScript의 기본 문법

1. 변수와 상수
2. 데이터 타입과 형 변환
3. 연산자
4. 함수

## 문

### 조건문 (if, else, if, else, switch)

1. 조건문
2. switch문
3. 삼항연산자
4. 조건문의 중첩
5. 조건부 실행
6. 삼항 연산자와 단축 평가
7. falsy한 값과 truthy한 값

### 반복문

1. for문
2. while문
3. do...while문
4. break문과 continue문

## 배열(Array), 객체(Object) 기초

### 객체 생성

### 객체 속성 접근

### 객체 메소드

---

### 배열 생성

### 배열 요소 접근

### 배열 메소드
