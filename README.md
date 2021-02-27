<img src="https://github.com/stayahead-training/shared/blob/master/stayahead.png" />

# Core Spring

> [Introduction](#introduction)<br />
  [Inversion of Control (IoC) and Dependency Injection (DI)](#ioc-and-di)<br />
  [Container Configuration](#container-configuration)<br />
  [Validation and Spring Expression Language (SpEL)](#validation-and-spel)<br />
  [Aspect Oriented Programming (AOP)](#aop)<br >
  [Testing](#testing)<br />
  [Transaction Management](#transaction-management)<br />
  [Accessing Data and JDBC](#accessing-data-and-jdbc)<br />
  [Object Relational Mapping](#object-relational-mapping)<br />
  [Spring Data JPA](#spring-data-jpa)<br />
  [Spring Web MVC and REST](#spring-web-mvc-and-rest)<br />
  [Spring Security](#spring-security)<br />

## Introduction

[Recommended reading](content/recommended-reading.md#introduction)

- What is Spring?
- A short history of the framework
- The design philosophy
- Getting started
- Logging

## Inversion of Control (IoC) and Dependency Injection (DI)

[Recommended reading](content/recommended-reading.md#ioc-and-di)

- What is IoC?
- What is a Spring bean?
- The Spring IoC container
- Container configuration (briefly)
- Instantiating a container
- Obtaining a bean from the container
- What is DI?
- Resolving dependencies with Spring DI

## Container Configuration

[Recommended reading](content/recommended-reading.md#container-configuration)

- Java-based containter configuration
  - @Configuration
  - @Bean
- Annotation-based container configuration
  - Stereotypes
  - Component scanning
  - Autowiring
  - Handling multiple candidate beans
  - Using JSR annotations
  - Injecting values
- Bean scoping
- Acting on a bean's lifecycle events
- Grouping beans into profiles
- Externalising properties

## Validation and Spring Expression Language (SpEL)

[Recommended reading](content/recommended-reading.md#validation-and-spel)

- Validating with Spring's Validator interface
- Validating with Java Bean Validation
- Data binding
- Converting and formatting (briefly)
- What is SpEL?
- SpEL expressions
- Evaluating expressions
- Using expressions in bean definitions

## Aspect Oriented Programming (AOP)

[Recommended reading](content/recommended-reading.md#aop)

- What is AOP? 
- AOP proxies
- Spring and @AspectJ
- Declaring an aspect
- Declaring a pointcut
- Constructing pointcut expressions
- Declaring advice
- Making use of the JoinPoint

## Testing

[Recommended reading](content/recommended-reading.md#testing)

- Spring integration testing with JUnit (4 or 5)
- Loading and configuring the container
- Setting the active profile(s) and property source(s)
- Handling a dirty context

## Transaction Management

[Recommended reading](content/recommended-reading.md#transaction-management)

- Spring's transaction abstraction
- Configuring the data source and transaction manager
- Declarative transaction management
- Programmatic transaction management
- Choosing between the approaches

## Accessing Data and JDBC

[Recommended reading](content/recommended-reading.md#accessing-data-and-jdbc)

- Exception translation
- Annotating DAOs with @Repository
- Implementing a DAO using JdbcTemplate

## Object Relational Mapping (ORM)

[Recommended reading](content/recommended-reading.md#orm)

- What is ORM?
- What is Hibernate?
- Configuring the session factory
- Implementing a DAO using Hibernate
- What is JPA?
- Configuring the entity manager factory
- Implementing a DAO using JPA

## Spring Data JPA

[Recommended reading](content/recommended-reading.md#spring-data-jpa)

- Spring Data Repositories
- Configuring JPA repos
- Persisting entities
- Query methods
  - Derived queries
  - @Query
  - Paging and sorting
  - @EntityGraph
  - Projections
- Building queries programmatically
- Transactionality

## Spring Web MVC and REST

[Recommended reading](content/recommended-reading.md#spring-web-mvc-and-rest)

- Initialising a Spring web app
  - DispatcherServlet
  - The context heirarchy
  - @Controller and @RequestMapping
- Customising the MVC config
  - Type conversion
  - Message conversion
  - Validation
  - Interception
  - View resolution
  - Exception resolution
- Controller advice
- Request mapping
- Handler methods
  - Parameters and return values
  - Handler method annotations
- Putting it all together to create a REST API
- Testing a Spring web application
- Building an API client using RestTemplate

## Spring Security

[Recommended reading](content/recommended-reading.md#spring-security)

- Initialising a secure Spring web app
  - DelegatingFilterProxy
  - SecurityFilterChain
  - Security filters
- Spring Security architecture components
- Username/password authentication
- Basic authentication flow
- Building a custom UserDetailsService
- Password encoding
- Authorising requests with FilterSecurityInterceptor
- SpEL-based access control
- Method-level authorisation
- Testing a secure Spring web application