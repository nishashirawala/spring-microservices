# spring-microservices
Learning creation of microservice using spring

For multiple processes working together they need to find each other. Similar to Java RMI. Microservices has the same requirement.

The developers at Netflix had this problem when building their systems and created a registration server called Eureka (“I have found it” in Greek). They made their discovery server open-source and Spring has incorporated into Spring Cloud, making it even easier to run up a Eureka server. 

`@EnableEurekaServer` is annotation used along with `@SpringBootApplication` in order to register service.

As long as Spring Cloud Netflix and Eureka Core are on the classpath any Spring Boot application with @EnableEurekaClient will try to contact a Eureka server on http://localhost:8761 (the default value of eureka.client.serviceUrl.defaultZone):

For this application to run first run - ServiceRegistrationServer.java and then AccountsServer.java
ServiceRegistrationServer will start the eureka server with no services.
AccountsServer will create a new service and deploy it to local eureka server.
