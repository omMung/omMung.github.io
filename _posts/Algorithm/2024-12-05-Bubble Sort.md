---
title: "버블 정렬 (Bubble Sort)"
excerpt: "Bubble Sort"

categories:
  - Algorithm
tags:
  - [Algorithm]

toc: true
toc_sticky: true

date: 2024-12-05 18:02:12 +0900
last_modified_at: 2025-02-12 18:02:13 +0900
---
## 버블 정렬 (Bubble Sort)
버블 정렬(Bubble Sort)은 인접한 두 요소를 비교하며 정렬하는 알고리즘으로, 정렬해야 할 리스트를 여러 번 반복하여 정렬이 완료될 때까지 수행됩니다.

### 버블 정렬 동작 방식
1. 배열의 처음부터 인접한 두 개의 요소를 비교합니다.
2. 앞의 요소가 뒤의 요소보다 크다면 두 요소의 위치를 바꿉니다.
3. 배열의 끝까지 이를 반복하면 가장 큰 값이 맨 끝으로 이동합니다.
4. 위 과정을 배열의 길이만큼 반복하면서 정렬을 수행합니다.
### 버블 정렬의 시간 복잡도
최선(이미 정렬된 경우): O(n)
평균 및 최악: O(n²)
(이중 루프를 사용하기 때문에 느린 편이다.)
  
### 코드 예제
```javascript
function bubbleSort(arr) {
    let n = arr.length;
    let swapped;
    
    for (let i = 0; i < n - 1; i++) {
        swapped = false;
        for (let j = 0; j < n - 1 - i; j++) {
            if (arr[j] > arr[j + 1]) {
                // 두 요소를 교환
                [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
                swapped = true;
            }
        }
        // 만약 한 번도 교환되지 않았다면 정렬이 완료된 것이므로 종료
        if (!swapped) break;
    }
    return arr;
}

// 사용 예제
let numbers = [5, 3, 8, 4, 2];
console.log("정렬 전:", numbers);
console.log("정렬 후:", bubbleSort(numbers));

```