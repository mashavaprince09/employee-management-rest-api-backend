# Employee Management REST API

A Spring Boot REST API application for managing employee records with PostgreSQL database integration.

## Features

- Full CRUD operations for employee management
- RESTful API endpoints
- PostgreSQL database integration
- Custom exception handling
- Angular frontend integration

## Tech Stack

- **Backend**: Spring Boot
- **Database**: PostgreSQL
- **Frontend**: Angular
- **ORM**: Spring Data JPA

## Prerequisites

- Java 17 or higher
- PostgreSQL installed and running
- Maven
- Node.js (for frontend)

## Database Setup

1. Create a PostgreSQL database named `employee_management_system`:

```sql
CREATE DATABASE employee_management_system;
```

2. Create the `employees` table using the following SQL command:

```sql
CREATE TABLE employees (
    id NUMBER,
    first_name TEXT,
    last_name TEXT,
    email_address TEXT
);
```

## Configuration

Add your PostgreSQL username and password in `src/main/resources/application.properties`:

```properties
spring.datasource.username=your_postgres_username
spring.datasource.password=your_postgres_password
```

## Running the Application

1. Clone the repository
2. Configure your database credentials in `application.properties`
3. Run the Spring Boot application:

```bash
./mvnw spring-boot:run
```

4. The API will be available at `http://localhost:8080`

## API Endpoints

- `GET /api/employees` - Get all employees
- `GET /api/employees/{id}` - Get employee by ID
- `POST /api/employees` - Create new employee
- `PUT /api/employees/{id}` - Update employee
- `DELETE /api/employees/{id}` - Delete employee

## Project Structure

```
src/
├── main/
│   ├── java/com/employee/employee/
│   │   ├── controller/      # REST controllers
│   │   ├── exception/       # Custom exceptions
│   │   ├── model/          # Entity models
│   │   └── repository/     # Data repositories
│   └── resources/
│       └── application.properties
└── test/
```

## License

This project is open source and available under the MIT License.
