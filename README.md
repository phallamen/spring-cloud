# spring-cloud
# spring cloud server and client beginner with gradle using eclipse 

1. To run these project on command line: 
 gradle bootRun
2. To run these project in eclipse:
Right Click on project -> Run as -> Run Configure -> gradle -> key in purpose, java home, project name, gradle version
3. To test modify message property: 
Test the end-to-end result by starting the Config Service first and then, once loaded, starting the client. Visit the client app in the browser, http://localhost:8080/message. There, you should see the String Hello world reflected in the response.
Change the message key in the a-bootiful-client.properties file in the Git repository to something different (Hello Spring!, perhaps?). You can confirm that the Config Server sees the change by visiting http://localhost:8888/a-bootiful-client/default. You need to invoke the refresh Spring Boot Actuator endpoint in order to force the client to refresh itself and draw the new value in. Spring Boot’s Actuator exposes operational endpoints, like health checks and environment information, about an application. In order to use it you must add org.springframework.boot:spring-boot-starter-actuator to the client app’s CLASSPATH. You can invoke the refresh Actuator endpoint by sending an empty HTTP POST to the client’s refresh endpoint, http://localhost:8080/actuator/refresh, and then confirm it worked by reviewing the http://localhost:8080/message endpoint.

# reference 
https://spring.io/guides/gs/centralized-configuration/ ~ 
https://docs.spring.io/spring-boot/docs/current/reference/html/using-boot-running-your-application.html
