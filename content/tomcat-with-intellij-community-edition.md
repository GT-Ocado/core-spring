<img src="https://github.com/stayahead-training/shared/blob/master/stayahead.png" />

# Tomcat with IntelliJ Community Edition

At the time of writing IntelliJ Community Edition doesn't support server integration. There exists, however, a Maven plugin that you can use to run web apps on Tomcat.

## The Maven Tomcat Plugin

To make use of the Maven Tomcat plugin add the following to the app's POM:

```xml
<build>
  <plugins>
    <plugin>
      <groupId>org.apache.tomcat.maven</groupId>
      <artifactId>tomcat7-maven-plugin</artifactId>
      <version>2.2</version>
    </plugin>
  </plugins>
</build>
```

Then execute the tomcat7:run goal to spin up your web app on the embedded Tomcat instance.

```
$> mvn tomcat7:run
```
