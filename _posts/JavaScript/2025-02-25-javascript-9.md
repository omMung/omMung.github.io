---
title: ""
excerpt: "Express"

categories:
  - JavaScript
tags:
  - [JavaScript]

toc: true
toc_sticky: true

date: 2025-02-28
last_modified_at: 2025-02-28
---

## 깊은 복사와 얕은 복사란?

- 깊은 복사(Deep Copy)는 객체의 실제 값을 새로운 메모리 공간에 복사하는 것으로, 원본과 완전히 독립된 객체로서 복사한다.
- 얉은 복사(Shallow Copy)는 객체의 참조값(주소)만 복사하는 것으로, 복사된 객체가 변경된다면 원본 객체 또한 영향을 받게 된다.
  | 비교 항목 | 얕은 복사(Shallow Copy) | 깊은 복사(Deep Copy) |
  |------------|-----------------|-----------------|
  | **복사 방식** | 객체의 **참조값(주소)**만 복사 | 객체의 실제 값을 새로운 메모리 공간에 복사 |
  | **원본 데이터 영향** | 복사된 객체가 변경되면 원본 객체도 영향받음 | 원본과 완전히 독립적인 객체 생성 |
  | **복사 대상** | 1차원 데이터(Primitive Type)는 값만 복사하지만, 객체(Object, Array)는 참조만 복사 | 모든 계층의 데이터가 새롭게 복사됨 |
  | **성능** | 속도가 빠름(메모리 효율적) | 속도가 느릴 수 있음(메모리 사용 증가) |
  | **사용 예시** | 원본을 유지하면서도 일부 변경할 필요가 있을 때 | 원본과 완전히 분리된 새로운 객체가 필요할 때 |

## 깊은 복사의 구현 방법(JS)

```javascript
const _ = require("lodash"); // Lodash 라이브러리 설치 필요
const deepCopy2 = _.cloneDeep(original);
```

## 얕은 복사의 구현 방법(JS)

```javascript
// 객체 선언
const original = { name: "Alice", age: 25, hobbies: ["reading", "gaming"] };

// 1. Object.assign()을 이용한 얕은 복사
const shallowCopy1 = Object.assign({}, original);

// 2. Spread Operator(...)를 이용한 얕은 복사
const shallowCopy2 = { ...original };

// 값 변경 테스트
shallowCopy1.name = "Bob"; // 원본 영향 X
shallowCopy1.hobbies.push("coding"); // 원본 영향 O (배열은 참조됨)

console.log(original);
// { name: "Alice", age: 25, hobbies: ["reading", "gaming", "coding"] }

console.log(shallowCopy1);
// { name: "Bob", age: 25, hobbies: ["reading", "gaming", "coding"] }
```
