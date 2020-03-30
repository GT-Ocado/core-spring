<img src="https://github.com/stayahead-training/shared/blob/master/stayahead.png" />

# Recommended Reading for Spring Essentials

[<< back](../README.md)

## Introduction

- [Spring Docs - Overview](https://docs.spring.io/spring/docs/5.2.2.RELEASE/spring-framework-reference/overview.html#overview)

## IoC and DI

- [Spring Docs - Spring Core](https://docs.spring.io/spring/docs/5.2.2.RELEASE/spring-framework-reference/core.html#spring-core)<br />Sections 1.1 - 1.5, and 1.9.4

- [IoC and DI in Spring - baeldung.com](https://www.baeldung.com/inversion-control-and-dependency-injection-in-spring)<br />
This tutorial describes the concepts of IoC (Inversion of Control) and DI (Dependency Injection). It also describes (with examples) how each is implemented in Spring using both XML and Java configs.

## SpEL

- [Spring Docs - Expressions](https://docs.spring.io/spring/docs/current/spring-framework-reference/core.html#expressions)<br />Sections...

## AOP

- [Spring Docs - AOP](https://docs.spring.io/spring/docs/5.2.2.RELEASE/spring-framework-reference/core.html#aop)<br />Sections 5 - 5.4.4

- [Spring AOP - baeldung.com](https://www.baeldung.com/spring-aop)<br />
This tutorial describes the concepts of AOP (Aspect Oriented Programming) including definitions of the key terms. It also describes (with examples) how AOP is implmented in Spring using XML config.

## JPA with Hibernate

- [Spring Docs - ORM](https://docs.spring.io/spring/docs/5.2.2.RELEASE/spring-framework-reference/data-access.html#orm)<br />Sections 4.1, 4.2, 4.4 - 4.4.3, and 1.4 (all)

- [ORM - hibernate.org](https://hibernate.org/orm/what-is-an-orm/)<br />
This short article defines ORM (Object Relational Mapping). In particular it describes the object-relational impedence mismatch which is the principle reason for using an ORM framework like Hibernate in the first place.

- [Spring and JPA - baeldung.com](https://www.baeldung.com/the-persistence-layer-with-spring-and-jpa)<br />
This tutorial describes the configuration of JPA with Hibernate in a Spring app. Note that it is focused on Spring Boot but does include examples in both XML and Java of the configuration of the key beans - DataSource, EntityManagerFactory, and TransactionManager.

- [JPA Entities - baeldung.com](https://www.baeldung.com/jpa-entities)<br />
This tutorial lists and describes the key JPA annotations you'll need to turn your pojos into JPA entities.

- [Entity State Transitions - thoughts-on-java.org](https://thoughts-on-java.org/persist-save-merge-saveorupdate-whats-difference-one-use/)<br />
This article describes the differences between the JPA methods (persist and merge) and the Hibernate methods (save and update). We're not interested in the Hibernate methods here, rather it is the article's description of entity state transitions that is of most value.

## REST APIs

- [Spring Docs - Spring Web](https://docs.spring.io/spring/docs/5.2.2.RELEASE/spring-framework-reference/web.html#spring-web)<br />Sections 1.1 - 1.1.5, 1.3 - 1.3.3, and 1.3.6

- [Servlets - jenkov.com](http://tutorials.jenkov.com/java-servlets/overview.html)<br />
If you've not built a web app in Java before then it would be worth reading up about servlets. Servlets are the principle mechanism for writing code to handle HTTP requests and form the basis of Spring Web. This article is the second in a series and provides an overview of servlets. If you've time we'd recommend reading the whole series.

- [APIs - medium.com](https://medium.com/@perrysetgo/what-exactly-is-an-api-69f36968a41f)<br />
If you're comfortable with the concept of an API (as it pertains to inter-application comms.) then you needn't bother with this article. It describes APIs and why they're needed. It also describes JSON-format data.

- [REST - medium.com](https://medium.com/extend/what-is-rest-a-simple-explanation-for-beginners-part-1-introduction-b4a072f8740f)<br />
This is a two-part article describing RESTful-type APIs. It defines the acronym and describes the key parts - the identifier (URL) and the operation (HTTP method). It also describes the six REST constraints.

## WebFlux

- [Spring Docs - WebFlux](https://docs.spring.io/spring/docs/current/spring-framework-reference/web-reactive.html#webflux)<br />Sections...

## JMS

- [Spring Docs - JMS](https://docs.spring.io/spring/docs/current/spring-framework-reference/integration.html#jms)<br />Sections...

## Security

- [Spring Docs - Spring Security](https://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/)<br />Sections 8.2 and 8.3, 15.6, 10.8 - 10.10, 11.3, 10.21, and 10.24

- [Servlet Fitlers - jenkov.com](http://tutorials.jenkov.com/java-servlets/servlet-filters.html)<br />
Servlet fitlers form the basis of Spring security. Some knowledge of them will help you to understand what you're doing when securing your Spring web app.

[<< back](../README.md)