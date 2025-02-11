---
title: "선택 정렬 / SelectionSort"
excerpt: "SelectionSort"

categories:
  - Algorithm
tags:
  - [Algorithm]

toc: true
toc_sticky: true

date: 2024-12-04 18:02:12 +0900
last_modified_at: 2025-02-11 18:02:13 +0900
---
## 선택 정렬
선택 정렬(Selection Sort)은 배열을 정렬하는 간단한 알고리즘 중 하나이다.
배열을 순회하면서 가장 작은 값을 찾아 맨 앞에 위치시키고, 다음으로 작은 값을 찾아 두 번째 위치에 놓는 방식을 반복한다.
### 선택 정렬의 작동 방식
1. 주어진 배열에서 최솟값을 찾습니다.
2. 이 최솟값을 배열의 첫 번째 요소와 교환합니다.
3. 첫 번째 요소를 제외한 나머지 배열에서 다음으로 작은 값을 찾습니다.
4. 이 값을 두 번째 요소와 교환합니다.
5. 위 과정을 배열의 모든 요소가 정렬될 때까지 반복합니다.

### 선택 정렬의 장점과 단점
- 장점
  - 구현이 간단하고 이해하기 쉽습니다.
  - 추가적인 메모리 공간을 거의 사용하지 않는 제자리 정렬(in-place sorting) 알고리즘입니다.
- 단점
  - 시간 복잡도가 O(n^2)으로, 데이터의 개수가 많아질수록 성능이 저하됩니다.
  - 불안정 정렬(unstable sort) 알고리즘입니다. (같은 값을 가진 요소들의 순서가 바뀔 수 있습니다.)
  
### 코드 예제
```javascript
function selectionSort(arr) {
  const n = arr.length;

  for (let i = 0; i < n - 1; i++) {
    let minIndex = i; // 현재 부분 배열에서 최솟값의 인덱스

    for (let j = i + 1; j < n; j++) {
      if (arr[j] < arr[minIndex]) {
        minIndex = j; // 더 작은 값을 찾으면 인덱스 갱신
      }
    }

    // 최솟값을 현재 위치와 교환
    [arr[i], arr[minIndex]] = [arr[minIndex], arr[i]];
  }

  return arr;
}

// 예시 배열
const arr = [64, 25, 12, 22, 11];

// 선택 정렬 실행
const sortedArr = selectionSort(arr);

// 정렬된 배열 출력
console.log(sortedArr); // [11, 12, 22, 25, 64]
```