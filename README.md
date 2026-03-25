# Quiz Engine with Certificate Generation

A professional automated quiz application built with Spring Boot, Java, HTML, and SQL.

## Features

- Interactive multiple-choice quiz interface
- Automatic scoring and result calculation
- Certificate generation for passing scores (70%+)
- Professional, responsive HTML design
- H2 in-memory database for data persistence
- RESTful architecture

## Technology Stack

- **Backend**: Java 17, Spring Boot 3.2.0
- **Database**: H2 (SQL)
- **Frontend**: HTML5, CSS3, Thymeleaf
- **Build Tool**: Maven

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven 3.6+

### Running the Application

1. Navigate to the project directory
2. Run the application:
   ```bash
   mvn spring-boot:run
   ```
3. Open your browser and go to: `http://localhost:8080`

### Database Console

Access the H2 database console at: `http://localhost:8080/h2-console`
- JDBC URL: `jdbc:h2:mem:quizdb`
- Username: `sa`
- Password: (leave empty)

## Application Flow

1. **Home Page** (`/`) - Welcome screen with quiz introduction
2. **Quiz Page** (`/quiz`) - Interactive quiz with multiple-choice questions
3. **Results Page** (`/submit`) - Shows score and performance
4. **Certificate Page** (`/certificate/{id}`) - Printable certificate for passing scores

## Project Structure

```
src/
├── main/
│   ├── java/com/quiz/
│   │   ├── QuizEngineApplication.java
│   │   ├── config/
│   │   │   └── DataInitializer.java
│   │   ├── controller/
│   │   │   └── QuizController.java
│   │   ├── dto/
│   │   │   └── QuizSubmission.java
│   │   ├── model/
│   │   │   ├── Question.java
│   │   │   └── QuizResult.java
│   │   ├── repository/
│   │   │   ├── QuestionRepository.java
│   │   │   └── QuizResultRepository.java
│   │   └── service/
│   │       └── QuizService.java
│   └── resources/
│       ├── application.properties
│       └── templates/
│           ├── index.html
│           ├── quiz.html
│           ├── result.html
│           └── certificate.html
└── pom.xml
```

## Customization

### Adding Questions

Edit `DataInitializer.java` to add more questions to the quiz.

### Passing Score

The passing threshold is set to 70%. Modify in `result.html` and `certificate.html` if needed.

### Styling

All HTML templates include embedded CSS for easy customization.
