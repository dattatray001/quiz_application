# Quiz Application (Spring Boot)

## Overview
This is a **Java Spring Boot Quiz Application** built using **Spring Boot, Spring Data JPA, and Maven**.
The application provides REST APIs to manage quiz questions and can be extended to support quizzes,
users, scoring, and authentication.

---

## Technology Stack
- **Language:** Java
- **Framework:** Spring Boot
- **Build Tool:** Maven (Maven Wrapper included)
- **Database:** JPA (configurable via application.properties)
- **Architecture:** Layered (Controller → Service → Repository)

---

## Project Structure
```
quiz_application-main/
│
├── pom.xml                         # Maven configuration
├── mvnw / mvnw.cmd                 # Maven wrapper
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── org/datta/quiz_application/
│   │   │       ├── QuizApplication.java        # Main Spring Boot class
│   │   │       ├── controller/
│   │   │       │   └── QuestionController.java # REST endpoints
│   │   │       ├── service/
│   │   │       │   ├── IQuestionService.java   # Service interface
│   │   │       │   └── QuestionService.java    # Business logic
│   │   │       ├── repository/
│   │   │       │   └── QuestionRepository.java # JPA repository
│   │   │       └── model/
│   │   │           └── Question.java            # Entity model
│   │   └── resources/
│   │       └── application.properties           # App configuration
│   └── test/
│       └── java/
│           └── org/datta/quiz_application/
│               └── QuizApplicationTests.java
```

---

## Application Flow
1. **Controller Layer**
   - Exposes REST APIs for quiz questions
2. **Service Layer**
   - Contains business logic
   - Implements interfaces for clean separation
3. **Repository Layer**
   - Handles database operations using Spring Data JPA
4. **Model Layer**
   - Defines entity mappings

---

## Key Components

### QuizApplication.java
- Entry point of the Spring Boot application
- Enables auto-configuration and component scanning

### QuestionController
- Handles HTTP requests related to quiz questions
- Delegates processing to service layer

### QuestionService
- Implements quiz question business logic
- Acts as a bridge between controller and repository

### QuestionRepository
- Extends JPA repository
- Provides CRUD operations

### Question (Entity)
- Represents a quiz question
- Mapped to database table using JPA annotations

---

## Configuration
All configurations are managed in:
```
src/main/resources/application.properties
```

You can configure:
- Server port
- Database connection
- JPA settings

---

## How to Run the Application

### Using Maven Wrapper
```bash
./mvnw spring-boot:run
```

On Windows:
```bash
mvnw.cmd spring-boot:run
```

### Using Installed Maven
```bash
mvn clean install
mvn spring-boot:run
```

Application will start on:
```
http://localhost:8080
```

---

## API Endpoints (Example)
Depending on controller implementation:
- `GET /questions`
- `POST /questions`
- `PUT /questions/{id}`
- `DELETE /questions/{id}`

---

## Future Enhancements
- Quiz and category management
- User authentication (Spring Security + JWT)
- Result calculation
- Difficulty levels
- Swagger/OpenAPI documentation

---

## Author
**Dattatray Narhe**  
Software Developer


