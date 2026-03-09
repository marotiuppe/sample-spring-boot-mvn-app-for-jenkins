# Sample Spring Boot Maven App for Jenkins

This is a simple Spring Boot "Hello World" application created for demonstration purposes, specifically for integration with Jenkins CI/CD pipelines.

## Features
- **Spring Boot 2.7.18**: Compatible with legacy Tomcat 9.
- **REST Endpoint**: A simple `/hello` endpoint that returns "Hello World!".
- **JUnit 5 & AssertJ**: Automated testing using Spring Boot's testing starter.
- **Maven**: Standard build tool for dependency management and lifecycle.

## Requirements
- **JDK 1.8** or higher (configured for Java 1.8 compatibility)
- **Apache Maven 3.6** or higher
- **Tomcat 8 or 9** running on Java 1.8

## Getting Started

### Build the project
To compile and build the WAR file, run:
```bash
mvn clean package
```

### Run the tests
To execute the JUnit tests:
```bash
mvn test
```

### Run the application
Since this is now a WAR project, you can:
1. **Deploy to Tomcat**: Copy the generated `target/sample-app.war` to the `webapps` folder of your Tomcat installation.
2. **Run with Embedded Tomcat**: You can still run it as a regular Spring Boot app:
   ```bash
   java -jar target/sample-app.war
   ```
The application will start at `http://localhost:2020/sample-app/hello`.

## API Endpoints
- `GET /hello`: Returns a "Hello World!" message.

## Jenkins Integration
This project is designed to be easily integrated into Jenkins. You can use a `Jenkinsfile` (not provided yet) or set up a Maven project job to run `mvn clean test` during the build phase.
