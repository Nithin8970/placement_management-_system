# placement_management-_system
"Developed the Student Service module of a Placement Management System using Spring Boot 3, MySQL, and REST APIs, enabling secure CRUD operations for student placement records with full service-repository integration and Postman-tested endpoints.
# Placement Management System – Student Service Module

## Overview

This project is a **Student Service Module** of a Placement Management System built using **Spring Boot 3** and **MySQL**. It exposes RESTful APIs to manage student records such as name, contact details, department, academic year, and CGPA. The module follows a clean layered architecture with **Controller → Service → Repository → Database** and uses **Spring Data JPA** for ORM.

## Tech Stack

- **Backend:** Java 21, Spring Boot 3.5.x  
- **Frameworks:** Spring Web, Spring Data JPA  
- **Database:** MySQL 8.x  
- **Build Tool:** Maven  
- **Tools:** STS / IntelliJ IDEA, Postman  
- **Package:** `com.tns.studentservice`

## Features

- Add new student records  
- Fetch all students  
- Fetch a single student by ID  
- Update existing student details  
- Delete student records  
- Automatic table creation using Hibernate/JPA

## Project Architecture

- **Student** – JPA Entity representing the `student` table
- **StudentRepository** – `JpaRepository<Student, Integer>` for DB operations
- **StudentService** – Business logic for CRUD operations
- **StudentController** – REST controller exposing HTTP endpoints

```text
Client (Postman / Browser)
        |
        v
StudentController (REST Layer)
        |
        v
StudentService (Business Layer)
        |
        v
StudentRepository (Data Access)
        |
        v
MySQL Database (placementdb.student)
