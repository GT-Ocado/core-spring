<img src="../../../stayahead.png" />

# IoC and DI Exam

## Email Generator

[<< back](../../../../README.md#ioc-and-di)

Your task is to build an app with Spring-managed beans that generates emails from data in a CSV file. You may use whichever means (or combination of means) of configuring the Spring beans you choose.

NB: name the project **spring-essentials_exams_ioc-and-di_email-generator**.

Let's assume a CSV file that looks like this:

```csv
Mrs,Elyssa Bagwell,ebagwell0@mayoclinic.com
Mr,Austina,Rosentholer,arosentholer1@alexa.com
Miss,Alica Klishin,aklishin2@ucla.edu
Mrs,Nikos Brighouse,nbrighouse3@merriam-webster.com
Mr,Francklyn Sedgebeer,fsedgebeer4@moonfruit.com
```

The app should send an email to each individual with a subject and message of your choosing, e.g. Hello from Spring!

You'll need a mail server. We recommend using [smtpbucket](https://www.smtpbucket.com/) for development and testing. The host name is `mail.smtpbucket.com` and the port number is `8025`.

You may use whichever email library you choose but, for the sake of consistency, the code snippet included below assumes Spring's mail package of classes for which you'll need the `spring-context-support` and `mail` (javax.mail) libraries.

The following snippet demonstrates the creation of a JavaMailSender object and the sending of an email:

```java
JavaMailSenderImpl sender = new JavaMailSenderImpl();
sender.setHost("mail.smtpbucket.com");
sender.setPort(8025);
     
Properties props = sender.getJavaMailProperties();
props.put("mail.transport.protocol", "smtp");
props.put("mail.debug", "true");

SimpleMailMessage message = new SimpleMailMessage();
message.setTo("ebagwell0@mayoclinic.com");
message.setSubject("Hello");
message.setText("Hello from Spring!");
sender.send(message);
```

Try to design the app such that it comprises **at least two** reusable components.

[<< back](../../../../README.md#ioc-and-di)
