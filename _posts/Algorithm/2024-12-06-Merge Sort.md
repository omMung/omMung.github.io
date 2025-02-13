---
title: "병합 정렬 (Merge Sort)"
excerpt: "Merge Sort"

categories:
  - Algorithm
tags:
  - [Algorithm]

toc: true
toc_sticky: true

date: 2024-12-06 18:02:12 +0900
last_modified_at: 2025-02-12 18:02:13 +0900
---
## 병합 정렬 (Merge Sort)
병합 정렬(Merge Sort)은 분할 정복(Divide and Conquer) 알고리즘을 기반으로 하는 정렬 방법입니다.
주어진 배열을 계속 반으로 나눈 뒤, 정렬된 상태로 병합하는 방식으로 동작합니다.


### 병합 정렬 동작 방식
1️⃣분할(Divide)

- 배열을 절반으로 나누어 더 이상 나눌 수 없을 때까지 재귀 호출
2️⃣ 정렬 및 병합(Merge & Conquer)

- 두 개의 정렬된 배열을 하나의 정렬된 배열로 합침
3️⃣ 완성(Combine)

- 모든 하위 배열이 정렬되어 병합되면 최종 정렬된 배열이 완성
### 병합 정렬의 시간 복잡도
O(n log n)
모든 경우(최선, 평균, 최악)에서 O(n log n) 성능을 보장
안정 정렬(Stable Sort)이며, 정렬 후에도 기존 데이터의 순서가 유지됨
  
### 코드 예제
```javascript
function mergeSort(arr) {
  // 배열 길이가 1 이하이면 이미 정렬된 상태이므로 반환
  if (arr.length <= 1) {
    return arr;
  }

  // 배열을 반으로 나눔
  const mid = Math.floor(arr.length / 2);
  const left = arr.slice(0, mid);
  const right = arr.slice(mid);

  // 좌우 배열을 각각 정렬한 후 병합
  return merge(mergeSort(left), mergeSort(right));
}

// 두 개의 정렬된 배열을 병합하는 함수
function merge(left, right) {
  let result = [];
  let i = 0, j = 0;

  // 두 배열을 비교하면서 정렬된 순서로 result 배열에 추가
  while (i < left.length && j < right.length) {
    if (left[i] < right[j]) {
      result.push(left[i]);
      i++;
    } else {
      result.push(right[j]);
      j++;
    }
  }

  // 남은 요소들을 결과 배열에 추가
  return result.concat(left.slice(i)).concat(right.slice(j));
}

// 테스트 실행
const array = [38, 27, 43, 3, 9, 82, 10];
console.log("정렬 전:", array);
console.log("정렬 후:", mergeSort(array));

```