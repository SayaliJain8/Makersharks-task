# Makersharks-task
Here's a slightly modified version of your project documentation:

---

# MakerSharks

## Overview
MakerSharks is developing a proof of concept (POC) for a search API that allows buyers to find manufacturers based on customized criteria such as location, nature of business, and manufacturing processes.

## Features
- **Search Manufacturers**: Retrieve manufacturers based on location, nature of business, and manufacturing processes.
- **Pagination**: Handle large result sets efficiently.
- **Input Validation**: Ensure that inputs are valid and sanitized.
- **Exception Handling**: Manage errors gracefully.
- **Basic Security**: Implement basic security using Spring Security.
- **API Documentation**: Provide comprehensive documentation with Swagger.

## Technologies Used
- **Java**: 17
- **Spring Boot**: 3.x
- **Spring Data JPA**
- **H2 Database** (for development/testing)
- **Maven**
- **Swagger** (Springdoc OpenAPI)
- **Spring Security**
- **Lombok**

## Setup and Running the Application

### Prerequisites
- JDK 17 or higher
- Maven
- An IDE (e.g., IntelliJ IDEA, Eclipse, or VS Code)

### Cloning the Repository
1. Clone the Repository:
   ```bash
   git clone https://github.com/dvarad20/MakerSharks
   cd MakerSharks
   ```

2. Build and Run the Application:
   ```bash
   mvn spring-boot:run
   ```

### Configuration
1. Navigate to `src/main/resources/application.properties`.
2. Update the PostgreSQL configuration with your own database settings.

### Accessing the API
Once the application is running, access the API at [http://localhost:8080](http://localhost:8080).

#### API Endpoints

- **Query Manufacturers Endpoint**:
  - **Path**: `/api/supplier/query`
  - **Method**: POST
  - **Description**: Retrieve a list of manufacturers based on location, nature of business, and manufacturing processes.
  - **Request Parameters**:
    - `location`: The location of the manufacturer (e.g., India).
    - `natureOfBusiness`: The nature of the business (e.g., small_scale).
    - `manufacturingProcess`: The manufacturing processes the manufacturer can perform (e.g., 3d_printing).

  **Example Request**:
  ```bash
  curl -X POST "http://localhost:8080/api/supplier/query?location=India&natureOfBusiness=SMALL_SCALE&manufacturingProcess=MOULDING"
  ```

### Accessing Swagger Documentation
The API documentation is available at:
- [Swagger UI](http://localhost:8080/swagger-ui.html)
- [Swagger Index](http://localhost:8080/swagger-ui/index.html)

### Running Tests
Run unit tests using Maven:
```bash
mvn test
```

### Security
The application uses basic authentication for simplicity. For production, consider implementing OAuth2 or JWT for more secure authentication and authorization.

### Troubleshooting
If you encounter issues with Maven commands, ensure Maven is properly installed and added to your system's PATH.

