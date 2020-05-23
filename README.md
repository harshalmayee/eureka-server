# Eureka-server
Eureka Server Used Service Registration and Discovery

# Tech Stack
* Spring Boot
* Netflix Eureka for Service Registration and Discovery
* Maven

# Maven Dependencies
```
<!-- Netflix Eureka Server Dependency-->
		<dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
		</dependency>
```    

# Entries in Application.yml
```
eureka:
    client:
        fetch-registry: false
        register-with-eureka: false
logging:
    level:
        com:
            netflix:
                discovery: 'OFF'
                eureka: 'OFF'
server:
    port: 8083
```    

# Spring Boot Application

* @@EnableEurekaServer : Annotation used for enabling eureka server
```
@SpringBootApplication
@EnableEurekaServer
public class EurekaServerApplication {
	public static void main(String[] args) {
		SpringApplication.run(EurekaServerApplication.class, args);
	}
}
```
