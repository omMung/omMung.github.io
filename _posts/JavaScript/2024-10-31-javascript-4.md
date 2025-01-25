---
title: : "Promise-1"
excerpt: "Promise-1"

categories:
  - JavaScript
tags:
  - [JavaScript]

toc: true
toc_sticky: true

date: 2025-01-25
last_modified_at: 2025-01-25
---

## Promise

    Promise란 비동기 작업의 최종완료 또는 실패를 나타내는 객체이다.

JavaScript에서는 Promise라는 생성된 시점에는 정의되지 않은 값을 위한 대리값이 존재한다.
또한 비동기 연산이 종료된 후 결과 값과 실패사유를 처리하기 위한 처리기를 연결할 수 있다.
Promise를 사용하면 비동기 메서드에서 마치 동기 메서드를 이용하는 것처럼 값을 반환할 수 있는데, 최종 결과를 반환하는 것이 아닌, 미래의 어떤 시점에서의 결과를 제공하는 Promise를 반환한다.

## Promise의 상태

1. 대기(pending): 초기 상태
2. 이행(fulfilled): 연산이 성공적으로 완료된 상태
3. 거부(rejected): 연산이 실패한 상태
