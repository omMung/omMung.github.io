---
title: "TypeScript-3"
excerpt: "TypeScript-3"

categories:
  - TypeScript
tags:
  - [TypeScript]

toc: true
toc_sticky: true

date: 2025-01-22
last_modified_at: 2025-01-22
---

## TypeScript의 고급 타입 정리

TypeScript에서 사용되는 고급 타입형을 한번 알아보자!

### enum과 object literal은 어떻게 다를까?

이전 기본형에서 본 enum을 기억하고 있는가?
enum은 열거형 데이터 타입으로 상수의 그룹화에 자주 사용되고 코드의 가독성을 높여준다!

#### object literal은 어떤걸까?
    
- 객체 리터럴은 키 + 값으 pair로 구성된 객체를 정의하는 방식  
  객체 리터럴은 enum과 다르게 어떤 타입의 값도 대입을 할 수 있어요!  
  코드 내에서 사용하기 전, 값이 할당되어 런타임 오류를 방지할 수 있다.
  
#### 어떤 경우에 enum과 object literal을 사용하면 좋을까?

- 간단한 상수값들을 그룹화하여 관리하려는 경우, 값이 변하지 않을 경우는 enum을 사용하자!
- 복잡한 구조와 다양한 데이터 타입을 사용하고, 값이나 데이터 타입을 변경해야 하는 경우에는 object literal을 사용하자!
---
>리터럴이란 자유로운 객체를 모방한 것일까?

### 유틸리티 타입을 알아보자
#### Partial< T >
  Type T의 모든 속성을 선택적으로 만든다!  
기존 타입의 일부속성만 제공하는 객체를 손쉽게 생성 가능해진다.  
  
예시)
```ts
interface Person {
  name: string;
  age: number;
}

const updatePerson = (person: Person, fields: Partial<Person>): Person => {
  return { ...person, ...fields };
};

const person: Person = { name: "Spartan", age: 30 };
const changedPerson = updatePerson(person, { age: 31 });
```
#### Required< T >
Type T의 모든 속성을 필수적으로 만든다!  
T 타입 객체에 정의된 모든 속성이 반드시 전부 제공되는 객체를 생성할때 사용된다.
예시)
#### Readonly< T >
#### Pick<T,K>
#### Omit<T,K>
