---
title: "TypeScript-2"
excerpt: "TypeScript-2"

categories:
  - TypeScript
tags:
  - [TypeScript]

toc: true
toc_sticky: true

date: 2025-01-21
last_modified_at: 2025-01-21
---

## TypeScript의 기본 표현형

타입 스크립트는 자바 스크립트와 달리 타입을 정확히 명시해 효율적이고 안정적인 코드 작성을 돕는다.
그렇다면 이런 타입들은 어떤 종류가 있을까?

1. Boolean
   - 참(true) 또는 거짓(false) 값을 나타낸다.
   - 조건문, 비교 연산등에 주로 사용되고 2가지 값 외에 다른값을 사용할 수 없다.
2. number
   - 모든 숫자를 나타낸다 (다른 프로그래밍 언어는 유형마다 타입이 존재)
   - 정수, 실수, 2진수 등 모든 수를 표현 가능
   - 모든 수치 연산에 사용되는 값은 number타입을 명시해주면 된다.
3. string
   - 텍스트 데이터를 나타낸다.
   - `(백쿼트), '(작은따옴표), "(큰따옴표)를 사용해 문자열을 표현할 수 있다.
     - ES6 이후 사용되는 템플릿 리터럴을 이용할 때 백쿼트를 사용한다!
   - 텍스트를 조작하거나 출력할 때 사용할 수 있다.
4. array
   - 기본타입에 []를 붙여 사용하는 형태를 띈다
     - ex) number[]
5. tuple
   - 서로 다른 타입의 원소를 순서에 맞춰 가질 수 있게하는 특수한 배열 형태
6. enum
   - 열거형 데이터 타입
   - 직관적으로 데이터의 값을 보여주기에

## LET, CONST, READONLY

## ANY, UNKNOWN, UNION

1. ANY

- ANY는 사실상 사용하지 않는다고 생각하면 된다.
- 타입을 나눠주는 이유가 사라지기 때문이다.

2. UNKNOWN

-

3. ## UNION
