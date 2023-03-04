---
layout: single
title:  "Spring 기초"
categories: Spring
tags: [Java, Spring, 스프링]
---

***

# Spring 기초

![image](https://user-images.githubusercontent.com/108318494/222224029-0ef2a24a-532b-46ce-83d2-a1895deff651.png)

- 사용자의 요청을 처리한 후, 지정된 뷰에 모델 객체를 넘겨준다.
  - 클라이언트의 요청에 대해 어떤 처리를 할지 Service로 넘겨준다.
  - Service에서 처리된 내용을 View로 넘겨준다.
  
- URL마다 처리해야 할 기능을 정해놓은 API를 모아놓은 클래스이다.
 - 클라이언트가 API로 요청을 보내면, 서버에서 기능을 처리한 후 API를 통해 결과를 보내준다.
 
- 사용자와 상호작용을 처리하는 Presentation 계층에 속해 있다.

1. Java 객체가 Controller 역할을 한다고 알려주는 어노테이션.

2. 각각의 레이어는 자기와 인접한 레이어와 직접 소통 /  ContentService 객체를 가지고 있기에 2-1와 같은 서비스 로직 호출 가능.

3. 특정 요청에 호출될 메소드를 지정하는 어노테이션

4. 해당 메서드에 넘기는 인자값을 쉽게 넘기도록 도와준다. 일치하는 변수값을 메서드 호출시 같이 넘어감.

5. 3번과 다른 이유는 Http 메서드에 따라 다른 Controller 메서드를 연결해줄 수 있기 때문 / Get과 Post를 나눠 처리하기 용이함.

6. 뷰까지 같이 반환 or JSON형식으로 데이터만 반환을 따짐

<br><br><br>

![image](https://user-images.githubusercontent.com/108318494/222224376-3839eb8c-9bb9-4357-9a81-91fe45af96a5.png)

- 비즈니스 로직을 수행한다.
- Repository에서 받아온 데이터를 가공하여 Controller에게 보내준다.
- 서비스 / 시스템의 핵심 로직인 Domain(Business or Service) 계층에 속해 있다.

1. Java 객체가 서비스 역할을 하는 객체라고 알려주는 어노테이션

2. 인접한 계층의 Repository 객체를 가져옴

3. 인접한 계층으로 데이터를 전달하는 부분

<br><br><br>

![image](https://user-images.githubusercontent.com/108318494/222224568-dfc3c111-d07d-48fb-907b-2eee1295a7ef.png)

1. Java객체가 Repository 역할을 한다고 알려주는 어노테이션

2. JpaRepository상속을 통해 사용.
