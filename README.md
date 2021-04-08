<img src="https://github.com/stayahead-training/shared/blob/master/stayahead.png" />

# Core Spring

> [Introduction to Spring and Inversion of Control](#introduction-to-spring-and-inversion-of-control)<br />
  [Annotation-based Container Configuration and Dependency Injection](#annotation-based-container-configuration-and-dependency-injection)<br />
  [More Container Configuration](#more-container-configuration)<br />
  [Aspect Oriented Programming](#aspect-oriented-programming)<br >
  [Testing](#testing)<br />
  [Transaction Management](#transaction-management)<br />
  [Accessing Data and JDBC](#accessing-data-and-jdbc)<br />
  [Minimising Configuration with Spring Boot](#minimising-configuration-with-spring-boot)<br />
  [Data Persistence with Spring Data JPA](#data-persistence-with-spring-data-jpa)<br />
  [Web Apps with Spring Web MVC](#web-apps-with-spring-web-mvc)<br />
  [REST APIs with Spring Web MVC](#rest-apis-with-spring-web-mvc)<br />
  [Securing an App with Spring Security](#securing-an-app-with-spring-security)<br />
  [Monitoring and Management with Spring Boot Actuator](#monitoring-and-management-with-spring-boot-actuator)

## Introduction to Spring and Inversion of Control

[Recommended reading](content/recommended-reading.md#introduction-to-spring-and-inversion-of-control)

- About Spring
- Inversion of Control
- The Spring IoC container
- Spring beans
- Configuring the container
- Instantiating a container and obtaining beans

## Annotation-based Container Configuration and Dependency Injection

[Recommended reading](content/recommended-reading.md#annotation-based-container-configuration-and-dependency-injection)

- Classpath scanning and managed components 
- Dependency injection
- Autowiring
- Handling multiple candidate dependencies
- Java configuration vs. annotations, and mixing

## More Container Configuration

[Recommended reading](content/recommended-reading.md#more-container-configuration)

- Acting on a bean's lifecycle events
- Specifying the scope of a bean
- Composing configurations
- Grouping beans into profiles
- Externalising properties
- Environment abstraction
- Spring Expression Language (SpEL)

## Aspect Oriented Programming

[Recommended reading](content/recommended-reading.md#aop)

- About AOP and proxying
- Constructing pointcut expressions
- Advising the target object

## Testing

[Recommended reading](content/recommended-reading.md#testing)

- Spring integration testing with JUnit
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

## Minimising Configuration with Spring Boot

[Recommended reading](content/recommended-reading.md#spring-boot)

- Spring Boot: what and why
- Starter dependencies
- Auto-configuration
- Spring Boot annotations
- Creating a simple Spring Boot app
- Configuration properties
- Executing code on startup using CommandLineRunner

## Data Persistence with Spring Data JPA

[Recommended reading](content/recommended-reading.md#spring-data-jpa)

- ORM, JPA, and Hibernate
- Entity mapping
- Spring Data Repositories
- Persisting entities
- Writing query methods
- Transactionality
- Configuring Spring Data JPA with Spring/Spring Boot

## Web Apps with Spring Web MVC

[Recommended reading](content/recommended-reading.md#spring-web-mvc)

- The DispatcherServlet
- Request processing
- Building a controller
- Handler method parameters
- Configuring Spring Web MVC with Spring/Spring Boot

## REST APIs with Spring Web MVC

- About REST APIs
- Enabling and modifying the MVC Configuration
- @ResponseBody, message conversion, and @RestController
- Content negotiation
- @RequestBody and validation
- @ResponseStatus and exception handling

## Securing an App with Spring Security

[Recommended reading](content/recommended-reading.md#securing-an-app-with-spring-security)

- The big picture
- Architecture components
- Configuring custom authentication
- Configuring authorisation for access to endpoints
- Configuring authorisation at the method level
- Configuring Spring Security with Spring/Spring Boot

## Monitoring and Management with Spring Boot Actuator

[Recommended reading](content/recommended-reading.md#spring-boot-actuator)

- About the actuator
- Exposing endpoints
- Writing custom endpoints
- Dealing with metrics
- Health indicators
- Writing custom health indicators
- Monitoring and management over HTTP & JMX