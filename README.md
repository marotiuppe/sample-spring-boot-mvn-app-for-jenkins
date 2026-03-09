# Sample Spring Boot Maven App for Jenkins

This is a simple Spring Boot "Hello World" application created for demonstration purposes, specifically for integration with Jenkins CI/CD pipelines.

## Features
- **Spring Boot 3.2.3**: Modern Java framework.
- **REST Endpoint**: A simple `/hello` endpoint that returns "Hello World!".
- **JUnit 5 & AssertJ**: Automated testing using Spring Boot's testing starter.
- **Maven**: Standard build tool for dependency management and lifecycle.

## Requirements
- **JDK 17** or higher (required for Spring Boot 3)
- **Apache Maven 3.6** or higher

## Getting Started

### Build the project
To compile and build the JAR file, run:
```bash
mvn clean package
```

### Run the tests
To execute the JUnit tests:
```bash
mvn test
```

### Run the application
After building, you can run the JAR file:
```bash
java -jar target/sample-spring-boot-mvn-app-for-jenkins-0.0.1-SNAPSHOT.jar
```
The application will start at `http://localhost:8080`.

## API Endpoints
- `GET /hello`: Returns a "Hello World!" message.

## Jenkins Integration
This project is designed to be easily integrated into Jenkins. You can use a `Jenkinsfile` (not provided yet) or set up a Maven project job to run `mvn clean test` during the build phase.
