# Spring Boot H2 Database

This project demonstrates a simple Spring Boot application using an H2 in-memory database. It includes CRUD operations via RESTful APIs for managing student records.

## Table of Contents

- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Running the Application](#running-the-application)
- [Testing the APIs](#testing-the-apis)
- [Additional Notes](#additional-notes)
- [Contributing](#contributing)
- [License](#license)

## Technologies Used

- **Spring Boot:** Framework for creating standalone, production-grade Spring-based applications.
- **H2 Database:** In-memory SQL database for development and testing.
- **Spring Data JPA:** Simplifies data access using Hibernate under the hood.
- **Spring Web:** Provides RESTful web services support.
- **Postman:** API client for testing and documenting APIs.

## Project Structure
````bash
SpringBootH2DatabaseExample
├── src
│ ├── main
│ │ ├── java
│ │ │ └── com
│ │ │ └── javatpoint
│ │ │ ├── controller
│ │ │ │ └── StudentController.java
│ │ │ ├── model
│ │ │ │ └── Student.java
│ │ │ ├── repository
│ │ │ │ └── StudentRepository.java
│ │ │ └── service
│ │ │ └── StudentService.java
│ │ └── resources
│ │ └── application.properties
│ └── test
│ └── java
├── pom.xml
└── README.md
````


## Setup Instructions

1. **Clone the repository:**
````bash
git clone https://github.com/your-repository-url.git
cd SpringBootH2DatabaseExample
````


2. **Configure database:**
- Open `application.properties` and configure the following properties:
  ```
  spring.datasource.url=jdbc:h2:mem:javatpoint
  spring.datasource.driverClassName=org.h2.Driver
  spring.datasource.username=sa
  spring.datasource.password=
  spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
  spring.h2.console.enabled=true
  ```

3. **Run the application:**
- Execute the main class `SpringBootH2DatabaseExampleApplication.java` to start the Spring Boot application.

## Running the Application

- Once the application is running, you can access the H2 console using the URL `http://localhost:8080/h2-console` and JDBC URL `jdbc:h2:mem:javatpoint`.
- Use Postman or any other REST client to interact with the APIs.

## Testing the APIs

- **GET All Students:**
````bash
GET http://localhost:8080/student
````


- **GET Student by ID:**
````bash
GET http://localhost:8080/student/{id}
````


- **DELETE Student by ID:**
````bash
DELETE http://localhost:8080/student/{id}
````


- **POST Student:**
````bash
POST http://localhost:8080/student
Content-Type: application/json

{
"id": "006",
"name": "John Doe",
"age": 30,
"email": "john.doe@example.com"
}
````


## Additional Notes

- This project uses Spring Boot with H2 database, suitable for lightweight application development and testing.
- Ensure the H2 console is enabled in `application.properties` for easy database visualization.

## Contributing

- Contributions are welcome! Fork the repository and submit a pull request.

## License

- This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
