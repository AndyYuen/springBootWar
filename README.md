# Spring-Boot and Camel REST-DSL example intended to be running as a .war file on Red Hat EAP

This example demonstrates how to configure Camel routes in Spring Boot via a Spring XML configuration file.

The application utilizes the Spring [`@ImportResource`](http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/context/annotation/ImportResource.html) annotation to load a Camel Context definition via a [camel-context.xml](src/main/resources/spring/camel-context.xml) file on the classpath.

### Building

The example can be built with

    mvn clean install

### Running the example on Red Hat EAP

It is assumed that:
- you already have MySql installed with the creditials set up according to src/main/resources/application.properties file
- the MySql database with database and table set up same as that in the src/main/resources/schema-h2.sql
- copy the target/springBootWar-1.0.0-SNAPSHOT.war to the EAP's standalone/deployment directory

### Running the example locally as a fat jar
Either use the Developer Studio

or command line
mvn clean spring-boot:run
