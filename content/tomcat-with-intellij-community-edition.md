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

Then execute the `tomcat7:run` goal to spin up your web app on the embedded Tomcat instance.

```
$> mvn tomcat7:run
```

## Using the Maven Tomcat Plugin to Deploy to an Existing Tomcat Instance

Tomcat 7 is an old version (servlet spec 3.0; JSP spec 2.2 etc.) and will fall over when using some Spring 5 features e.g. javax.validation and Spring Security. Unfortunately there is no Tomcat 8/9 Maven plugin so the only way around these issues to install Tomcat 8/9 locally and then use the plugin to deploy your app to the local instance. This is not ideal but it's far better than manually packaging and deploying the app. 

1. Install Tomcat 8/9 locally.

2. Edit the `<tomcat_home>/conf/tomcat-users.xml` file and add a user with manager-gui and manager-script roles, e.g.:

   ```xml
   <tomcat-users>
     <role rolename="manager-gui"/>  
     <role rolename="manager-script"/>   
     <user username="admin" password="admin" roles="manager-gui,manager-script" />  
   </tomcat-users>
   ```
   
3. Edit (you may have to create) the Maven settings file (`<user_home>/.m2/settings.xml`) and add a server representing your local Tomcat instance, e.g.:

   ```xml
   <settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
     xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
                         https://maven.apache.org/xsd/settings-1.0.0.xsd">
     <servers>  
       <server>
         <id>tomcat</id>
         <username>admin</username>
         <password>admin</password>
       </server>
     </servers>
   </settings>
   ```
   
4. Edit the Tomcat Maven plugin in the POM so as to reference the local Tomcat instance.

   ```xml
   <build>
     <plugins>
       <plugin>
         <groupId>org.apache.tomcat.maven</groupId>
         <artifactId>tomcat7-maven-plugin</artifactId>
         <version>2.2</version>
         <configuration>
           <server>tomcat</server> <!-- the value here must match the server ID specified in Maven's settings.xml file -->
         </configuration>
       </plugin>
     </plugins>
   </build>
   ```
   
5. Start your local Tomcat instance outside of InteliiJ.

   ```
   $> <tomcat_home>/bin/startup.bat (or startup.sh on Linux/Mac)
   ```
   
6. Make sure that you can access Tomcat's Manager GUI at `localhost:8080/manager` using the credentials you specified in `tomcat-users.xml`.

7. Execute the `tomcat7:deploy` goal to deploy your web app on the local Tomcat instance.

   ```
   $> mvn tomcat7:deploy
   ```
   
8. Execute the `tomcat7:redeploy` goal to redeploy your web app after making changes.

   ```
   $> mvn tomcat7:redeploy
   ```

NB: I have yes to test this with Spring 5 and **Java 11**.
