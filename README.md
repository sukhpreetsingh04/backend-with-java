# Introduction
Basic Spring Boot Application.
In this repository, we use java as backend language.
we'll learn backend with java as main programming language.


# Java Backend Development Notes (Spring Boot)
1. Setting Up the Project
✅ Use Spring Initializr to generate a Spring Boot project.

✅ Select Spring Boot 3.4.5 (latest stable).
✅ Choose Gradle (Groovy DSL) for dependency management.
✅ Add required dependencies:
- Spring Web → Enables backend web services.
- Spring Boot DevTools → Helps with fast development.

2. Creating the Main Class
✅ Define the main entry point for the application

```Java
package com.example.demo;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class DemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```

✅ @SpringBootApplication → Enables auto-configuration and component scanning.
✅ SpringApplication.run(DemoApplication.class, args); → Starts the Spring Boot application.


3. Adding a Simple REST API
✅ Create a basic controller to return a message:

```java
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {
    @GetMapping("/")
    public String home() {
        return "Hello, Java Backend!";
    }
}
```

✅ @RestController → Marks this class as a web controller.
✅ @GetMapping("/") → Defines a GET request for /.
✅ Running this will display Hello, Java Backend! at http://localhost:8080/.

4. Resolving Import Errors
✅ Ensure spring-boot-starter-web dependency is included.
✅ If errors occur, update build.gradle or pom.xml:

```gradle
dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-web'
}
```

✅ Run ./gradlew build or mvn clean install to refresh dependencies.

5. Running the Server
✅ Start the application → Run DemoApplication.main().
✅ Open browser/Postman → Go to http://localhost:8080/.
✅ Verify response → "Hello, Java Backend!"



