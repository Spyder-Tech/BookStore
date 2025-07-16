Book Store Spring Boot Application

This tutorial project is a simple demonstration of building a bookstore REST API using Spring Boot, JPA, Hibernate, and MySQL.

It guides you through creating a full-stack application with CRUD operations, API documentation, and a basic web interface.

Features

    Store book data in a MySQL database table named BOOKS.
    Define a Book Java class with properties mapped to database columns.
    Use Spring Data JPA annotations for ORM mappings.
    Leverage Hibernate to handle SQL query generation and data persistence.
    Configure database connection details in application.properties.
    Expose CRUD operations via RESTful APIs using Spring Web.
    Document and test APIs with OpenAPI and Swagger UI.
    (Optional) Web interface built with HTML and JavaScript for user interaction.

Prerequisites

    Java 11 or higher
    Maven or Gradle build tool
    MySQL Database Server
    spring.datasource.url=jdbc:mysql://localhost:3306/bookstore?useSSL=false&serverTimezone=UTC
    spring.datasource.username=your_db_username
    spring.datasource.password=your_db_password
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true


Setup Instructions
1. Clone the Repository

          

git clone https://github.com/yourusername/bookstore-springboot.git
cd bookstore-springboot

      

2. Configure MySQL Database

Create a database named bookstore and ensure your MySQL user has appropriate permissions.

          

CREATE DATABASE bookstore;

      

3. Update application.properties

In src/main/resources/application.properties, set your database connection details:

          
    spring.datasource.url=jdbc:mysql://localhost:3306/bookstore?useSSL=false&serverTimezone=UTC
    spring.datasource.username=your_db_username
    spring.datasource.password=your_db_password
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true

      

4. Build and Run the Application

Using Maven:

          

mvn clean install
mvn spring-boot:run


Usage
Access REST API

The API endpoints are available at http://localhost:8080/api/books.

Use tools like Postman or your browser to perform CRUD operations:

    GET /api/books — List all books
    GET /api/books/{id} — Get a book by ID
    POST /api/books — Create a new book (with JSON body)
    PUT /api/books/{id} — Update a book
    DELETE /api/books/{id} — Delete a book

API Documentation

OpenAPI and Swagger UI are integrated:

    Access Swagger UI at http://localhost:8080/swagger-ui.html

Web Interface

A simple HTML/JavaScript web page interacts with the REST API (if included). Open the HTML file in your browser and follow the interface prompts.
Project Structure

Dependencies

    Spring Boot Starter Web
    Spring Boot Starter Data JPA
    MySQL Connector Java
    Springdoc OpenAPI UI (for Swagger UI)

License
This project is for educational purposes. Feel free to modify and extend.

Note:
Remember to replace placeholders like yourusername, database credentials, and URLs with your actual project details.
