<img src="https://github.com/stayahead-training/shared/blob/master/stayahead.png" />

# Recommended Reading for Core Spring

[<< back](../README.md)

> [Introduction to Spring and Inversion of Control](#1)<br />
  [Annotation-based Container Configuration and Dependency Injection](#2)<br />
  [More Container Configuration](#3)<br />
  [Aspect Oriented Programming](#4)<br >
  [Testing](#5)<br />
  [Transaction Management](#6)<br />
  [Accessing Data and JDBC](#7)<br />
  [Minimising Configuration with Spring Boot](#8)<br />
  [Data Persistence with Spring Data JPA](#9)<br />
  [Web Apps with Spring Web MVC](#10)<br />
  [REST APIs with Spring Web MVC](#11)<br />
  [Securing an App with Spring Security](#12)<br />
  [Monitoring and Management with Spring Boot Actuator](#13)

<table>
        <tr>
            <th colspan="2"><a name="1"></a><h2>Introduction to Spring and Inversion of Control</h2></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/overview.html#overview-spring">What We Mean by "Spring"</a></td>
            <td><a href="https://www.baeldung.com/spring-why-to-choose">Why Choose Spring as Your Java Framework</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-introduction">Introduction to the Spring IoC Container and Beans</a></td>
            <td><a href="https://www.baeldung.com/inversion-control-and-dependency-injection-in-spring">Intro to Inversion of Control and Dependency Injection with Spring</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-java">Java-based Container Configuration</a></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <th colspan="2"><a name="2"><h2>Annotation-based Container Configuration and Dependency Injection</h2></a></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-classpath-scanning">Classpath Scanning and Managed Components</a></td>
            <td><a href="https://www.baeldung.com/spring-bean-annotations">Spring Bean Annotations</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-factory-collaborators">Dependency Injection</a></td>
            <td><a href="https://www.baeldung.com/inversion-control-and-dependency-injection-in-spring">Intro to Inversion of Control and Dependency Injection with Spring</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-autowired-annotation">Using <code>@Autowired</code></a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-autowired-annotation-primary">Fine-tuning Annotation-based Autowiring with @Primary</a></td>
            <td><a href="https://www.baeldung.com/spring-primary">Spring `@Primary` Annotation</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-autowired-annotation-qualifiers">Fine-tuning Annotation-based Autowiring with Qualifiers</a></td>
            <td><a href="https://www.baeldung.com/spring-qualifier-annotation">Spring <code>@Qualifier</code>Annotation</a></td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <th colspan="2"><a name="3"></a><h2>More Container Configuration</h2></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-factory-lifecycle">Lifecycle Callbacks</a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-factory-scopes">Bean Scopes</td>
            <td><a href="https://www.baeldung.com/spring-bean-scopes">Quick Guide to Spring Bean Scopes</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-java-composing-configuration-classes">Composing Java-based Configurations</td>
            <td><a href="https://www.baeldung.com/spring-import-annotation">Spring <code>@Import</code> Annotation</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-definition-profiles">Bean Definition Profiles</a></td>
            <td><a href="https://www.baeldung.com/spring-profiles">Spring Profiles</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-using-propertysource">Using <code>@PropertySource</code></a></td> 
            <td><a href="https://www.baeldung.com/properties-with-spring">Properties with Spring and Spring Boot</td> 
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-environment">Environment Abstraction</a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#expressions">Spring Expression Language (SpEL)</a></td>
            <td><a href="https://www.baeldung.com/spring-expression-language">Spring Expression Language Guide</td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <th colspan="2"><a name="4"></a><h2>Aspect Oriented Programming</h2></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#aop">Aspect Oriented Programming with Spring (5.1, 5.3, 5.4)</a></td>
            <td><a href="https://www.baeldung.com/spring-aop">Introduction to Spring AOP</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#aop-pointcuts">Declaring a Pointcut</a></td>
            <td><a href="https://www.baeldung.com/spring-aop-pointcut-tutorial">Introduction to Pointcut Expressions in Spring</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#aop-advice">Declaring Advice</a></td>
            <td><a href="https://www.baeldung.com/spring-aop-advice-tutorial">Introduction to Advice Types in Spring</a></td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <th colspan="2"><a name="5"></a><h2>Testing</h2></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/testing.html#integration-testing-overview">Integration Testing Overview</a></td>
            <td><a href="https://www.baeldung.com/integration-testing-in-spring">Integration Testing in Spring</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/testing.html#spring-testing-annotation-contextconfiguration"><code>@ContextConfiguration</code></a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/testing.html#spring-testing-annotation-activeprofiles"><code>@ActiveProfiles</code></a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/testing.html#spring-testing-annotation-dirtiescontext"><code>@DirtiesContext</code></a></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <th colspan="2"><a name="6"></a><h2>Transaction Management</h2></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/data-access.html#transaction-strategies">Understanding the Spring Framework Transaction Abstraction</a></td>
            <td><a href="https://www.baeldung.com/transaction-configuration-with-jpa-and-spring">Transactions with Spring and JPA</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/data-access.html#transaction-declarative-annotations">Using <code>@Transactional</code></a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/data-access.html#tx-prog-template">Using the <code>TransactionTemplate</code></a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/data-access.html#tx-decl-vs-prog">Choosing Between Programmatic and Declarative Transaction Management</a></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <th colspan="2"><a name="7"></a><h2>Accessing Data and JDBC</h2></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/data-access.html#orm-exception-translation">Exception Translation</a></td>
            <td><a href="https://www.baeldung.com/spring-jdbc-jdbctemplate">Spring JDBC</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/data-access.html#dao-annotations">Annotations Used to Configure DAO or Repository Classes</a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/data-access.html#jdbc-JdbcTemplate">Using <code>JdbcTemplate</code></a></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <th colspan="2"><a name="8"></a><h2>Minimising Configuration with Spring Boot</h2></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#getting-started-introducing-spring-boot">Introducing Spring Boot</a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#using-boot-starter">Starters</a></td>
            <td><a href="https://www.baeldung.com/spring-boot-starters">Intro to Spring Boot Starters</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#using-boot-auto-configuration">Auto-configuration</a></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td><a href="https://www.baeldung.com/spring-boot-annotations">Spring Boot Annotations</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#getting-started-first-application">Developing Your First Spring Boot Application</a></td>
            <td><a href="https://www.baeldung.com/spring-boot-start">Bootstrap a Simple Application</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-external-config-typesafe-configuration-properties">Type-safe Configuration Properties</a></td>
            <td><a href="https://www.baeldung.com/configuration-properties-in-spring-boot"><code>@ConfigurationProperties</code> in Spring Boot</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-command-line-runner">Using the <code>ApplicationRunner</code> or <code>CommandLineRunner</code></a></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <th colspan="2"><a name="9"></a><h2>Data Persistence with Spring Data JPA</h2></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td></td>
            <td><a href="https://www.baeldung.com/learn-jpa-hibernate">Learn JPA & Hibernate</a></td>
        </tr>
        <tr>
            <td></td>
            <td><a href="https://www.baeldung.com/jpa-entities">Defining JPA Entities</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#repositories">Working with Spring Data Repositories (4.1-5)</a></td>
            <td><a href="https://www.baeldung.com/the-persistence-layer-with-spring-data-jpa">Introduction to Spring Data JPA</a></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.entity-persistence.saving-entites">Saving Entites</a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.query-methods.query-creation">Query Creation</a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#transactions">Transactionality</a></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <th colspan="2"><a name="10"></a><h2>Web Apps with Spring Web MVC</h2></th>
        </tr>
        <tr>
            <td>Reference</td>
            <td>Other</td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/web.html#mvc-servlet">Dispatcher Servlet (1.1-1.1.8)</a></td>
            <td></td>
        </tr>
        <tr>
            <td><a href="https://docs.spring.io/spring-framework/docs/current/reference/html/web.html#mvc-controller">Annotated Controllers (all)</a></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td><a href="https://www.baeldung.com/spring-mvc-tutorial">Spring MVC Tutorial</a></td>
        </tr>
</table>

[<< back](../README.md)