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
   - 객체 지향이란?
     객체 지향이란 데이터와 함수를 객체로 묶어서 처리하는 방식으로 객체는 속성과 매소드를 추가하여 사용한다.
2. **동적 타이핑**
   - 변수를 선언할 때 타입을 지정하지 않고 런타임 시점에 변수에 할당되는 값에 따라 자동으로 데이터 타입이 결정 된다.
3. **함수형 프로그래밍 지원**
   - 함수를 일급 객체로 취급하며, 고차 함수를 지원하는 언어로 코드의 재사용성과 가독성을 높였다.
   - 일급 객체 : 함수를 일반 값과 마찬가지로 변수에 할당하거나, 함수의 인자로 전달하거나, 함수의 반환값으로 사용할 수 있는 객체를 의미
   - 고차 함수 : 함수를 인자로 받거나, 함수를 반환하는 함수
4. **비동기 처리**
   - 작업을 순차적으로 진행하지 않고, 병렬처리 하는 방식을 지원한다.
5. **클라이언트 측 및 서버 측 모두 사용 가능한 언어**
   - 클라이언트에서만 사용되는 것이 아닌 Node.js를 이용해 서버에서도 사용가능하여, 웹 개발 전반에 활용할 수 있다.

## JavaScript의 기본 문법

1. 변수와 상수
   1. 변수의 5대 개념
   ```markdown
   변수 이름 :저장된 값의 고유한 이름
   변수 값 : 변수에 저장된 값
   변수 할당 : 변수에 값을 저장하는 행위
   변수 선언 : 변수를 사용하기 위해 컴퓨터에 알리는 행위
   변수 참조 : 변수에 할당된 값을 읽어오는 것
   ```
   2. 변수 할당 방식
   ```javascript
      1. var : 여러 번 같은 이름 선언 가능, 마지막 선언한 값으로 변수가 덮어씌워진다.
      var myVar = "Hello";
      var myVar = "World";
      console.log(myVar); // "World"
      2. let : 같은 이름의 변수 선언 불가, 변수 값 변경 가능
      let myLet = "Hello";
      myLet = "World"; // 기존 값을 덮어쓰기
      console.log(myLet); // "World"
      3. const : 같은 이름의 변수 선언, 변수 값 변경 불가
      const myConst = "Hello";
      myConst = "World"; // 오류 발생
      console.log(myConst);
   ```
2. 데이터 타입과 형 변환
   데이터 타입
   1. 숫자(Number)
      1. 정수형 숫자(Integer)
      ```javascript
      let ex1 = 10;
      console.log(ex1); // 10
      console.log(typeof ex1); // "number"
      ```
      2. 실수형 숫자(Float)
      ```javascript
      let ex2 = 3.14;
      console.log(ex2); // 10
      console.log(typeof ex2); // "number"
      ```
      3. 지수형 숫자(Exponential)
      4. NaN(Not a Number)
      5. Infinity
      6. -Infinity
   2. 문자열(String)
   3. 불리언(Boolean)
   4. undefined
   5. null
   6. 객체(Object)
   7. 배열(Array)
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
