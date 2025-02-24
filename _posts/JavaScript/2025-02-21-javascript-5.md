---
title: "async/await"
excerpt: "async/await"

categories:
  - JavaScript
tags:
  - [JavaScript]

toc: true
toc_sticky: true

date: 2025-02-21
last_modified_at: 2025-02-24
---

## async/await란?

비동기 프로그래밍을 더 간결하고 가독성 좋게 작성할 수 있도록 도와주는 키워드

- async 함수:
  함수 앞에 async를 붙이면 해당 함수는 항상 Promise를 반환합니다.
  내부에서 await을 사용할 수 있습니다.

- await 키워드:
  Promise가 처리될 때까지 기다린 후, 해당 Promise의 결과 값을 반환합니다.
  await은 async 함수 내부에서만 사용할 수 있습니다.

## 사용법과 예시

await은 JavaScript의 Event Loop를 활용하여 비동기 작업이 완료될 때까지 기다린 후, 다음 코드가 실행되도록 합니다.
기존의 Promise.then()을 활용한 코드보다 직관적이고 동기 코드처럼 작성할 수 있습니다.

```javascript
// 1초 후에 데이터를 반환하는 비동기 함수
function fetchData() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("데이터 받아옴!");
    }, 1000);
  });
}

// async/await을 사용한 비동기 함수
async function getData() {
  console.log("데이터 요청 중...");
  const result = await fetchData(); // fetchData()가 완료될 때까지 기다림
  console.log(result);
}

getData();
// 출력 결과:
// 데이터 요청 중...
// (1초 후) 데이터 받아옴!
```
