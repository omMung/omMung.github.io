---
title: "Hoisting"
excerpt: "Hoisting"

categories:
  - JavaScript
tags:
  - [JavaScript]

toc: true
toc_sticky: true

date: 2025-02-24
last_modified_at: 2025-02-24
---

## Hoisting란?

- 호이스팅(hoisting)은 변수 및 함수 선언이 해당 스코프의 최상단으로 끌어올려지는 동작을 의미

- 코드가 실제로 작성된 위치와 관계없이 변수 및 함수를 선언 전에 사용할 수 있게 해준다.

## Hoisting의 종류

1. 변수 호이스팅 (Variable Hoisting): var 키워드로 선언된 변수는 선언 전에 사용할 수 있습니다. 그러나 변수의 초기화는 호이스팅되지 않으므로, 선언 전에 변수를 사용하면 undefined가 반환됩니다. let 및 const 키워드로 선언된 변수는 블록 스코프를 가지며, 호이스팅 시 TDZ(Temporal Dead Zone)에 빠지게 되어 선언 전에 접근하면 오류가 발생합니다.

2. 함수 호이스팅 (Function Hoisting): 함수 선언식(function declaration)으로 정의된 함수는 전체 함수 정의가 호이스팅됩니다. 따라서 함수 선언 전에 함수를 호출할 수 있습니다. 하지만 함수 표현식(function expression)으로 정의된 함수는 변수 호이스팅과 동일한 방식으로 동작하며, 선언 전에 호출하면 오류가 발생합니다.

## Hoisting의 예

```javascript
myFunctionExpression(); // TypeError: myFunctionExpression is not a function

var myFunctionExpression = function () {
  console.log("This is a function expression");
};
```
