<img src="https://github.com/stayahead-training/shared/blob/master/stayahead.png" />

# Spring Essentials

> [Introduction](#introduction)<br />
  [IoC and DI](#ioc-and-di)<br />
  [SpEL](#spel)<br />
  [AOP](#aop)<br />
  [JPA with Hibernate](#jpa-with-hibernate)<br />
  [REST APIs](#rest-apis)<br />
  [WebFlux](#webflux)<br />
  [JMS](#jms)<br />
  [Security](#security)

## Introduction

[Recommended reading](content/recommended-reading.md#introduction)

- What is Spring?
- What is it for?

## IoC and DI

[Recommended reading](content/recommended-reading.md#ioc-and-di)

- What is IoC?
- What is a Spring Bean?
- What is DI?
- **Code it: one or more apps with Spring-managed beans**
  - **XML and Java config**
  - **Autowiring**
  - **Component scanning**
  - **Properties files**
  - **Qualifiers**
  - **Bean lifecycle methods**
- **[Assignment: currency converter (Java config)](content/assignments/ioc-and-di/currency-converter-java-config)**
- **[Exam: email generator](content/exams/ioc-and-di/email-generator)**

## SpEL

[Recommended reading](content/recommended-reading.md#spel)

TODO

## AOP

[Recommended reading](content/recommended-reading.md#aop)

- What is AOP?
- What is an aspect?
- What is advice?
- What are the different types of advice?
- What is a joinpoint?
- What is a pointcut?
- **Code it: one or more apps using Spring AOP to separate cross-cutting concerns from business logic**
  - **The advised bean**
  - **The aspect and the advice**
  - **The AOP config**
  - **Pointcut expressions**
- **[Assignment: TODO](#)**

## JPA with Hibernate

[Recommended reading](content/recommended-reading.md#jpa-with-hibernate)

- What is ORM?
- What is JPA?
- What is Hibernate?
- **Code it: a Spring app that persists data using Hibernate**
  - **Data source and JPA beans config**
  - **The entity bean incl. JPA annotations**
  - **The repository/DAO**
    - **EntityManager injection**
    - **Persist, merge, remove, and find**
    - **JPQL**
  - **Transaction management**
- **[Assignment: TODO](#)**
- **Code it: a Spring Data JPA repository**

## REST APIs

[Recommended reading](content/recommended-reading.md#rest-apis)

- What is a REST API?
- **Code it: a Spring REST API**
  - **Dispatcher servlet + contexts config**
  - **The model**
  - **The controller**
    - **Request mapping**
    - **Path variables**
    - **Query parameters**
    - **The request body**
    - **Message conversion (JSON)**
    - **Response entities**
    - **Validation**
    - **Exception handling**
- **[Assignment: TODO](#)**
- **Code it: REST API client**

## WebFlux

[Recommended reading](content/recommended-reading.md#webflux)

TODO

## JMS

[Recommended reading](content/recommended-reading.md#jms)

TODO

## Security

[Recommended reading](content/recommended-reading.md#security)

- What is authentication?
- What is authorisation?
- **Code it: a secure Spring REST API**
  - **Dispatcher servlet + contexts config**
  - **Security filter chain config (minimal)**
  - **Custom authentication provider**
  - **Exression-based access control**
  - **CSRF protection**
- **[Assignment: TODO](#)**
