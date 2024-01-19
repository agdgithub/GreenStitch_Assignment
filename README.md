## Installation and Setup

```
### Prerequisites
- Java Development Kit (JDK) 8 or later
- Maven
- Postman (for testing the API)
```

### 1. Instructions to Run the Application
```
./mvnw spring-boot:run

```
**Open [http://localhost:8080](http://localhost:8080)**

### **API's**

### User signp

- Method: POST
- Path: `http://localhost:8080/app/signup`

```

{
  "fullName": "Akshay Daberao",
  "password": "xyz@12",
  "email": "abc@gmail.com"
}
```

### User Login

- Method: GET
- Path: `http://localhost:8080/signIn`
- Authentication: Basic Authentication (Username and Password)
    - Username: [abc@gmail.com](mailto:abc@gmail.com)
    - Password: xyz@12

### Welcome Endpoint 

- Method: GET
- Path: `http://localhost:8080/logged-in/user`
- Description: A protected endpoint that requires authentication to access.
- Authentication: Bearer Token
- Request Header:
    - Authorization: Bearer <token>

### Tech Stack

- Java
- Spring Boot
- H2 Database
- Spring Security
- JWT Token
- Maven


### Test API
Use Postman to test the API endpoints.

## H2 Database Configuration

The configuration can be found in the `application.properties` file:

```
server.port=8080
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

```

 
