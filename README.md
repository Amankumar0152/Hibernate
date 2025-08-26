# 🗄️ Hibernate – Auto Database & Table Creation

This project shows how to use **Hibernate ORM** to automatically create a database and tables from Java classes (entities) — without writing SQL queries manually.

## ✨ Features
- Java classes mapped to database tables (ORM)
- Automatic schema generation using Hibernate
- CRUD operations (Create, Read, Update, Delete)
- Easy integration with MySQL / PostgreSQL

## 🛠️ Tech Stack
- Java (JDK 17+)
- Hibernate ORM
- MySQL / PostgreSQL
- Maven / Gradle

## 🚀 How it Works
1. Define a Java entity class with annotations (`@Entity`, `@Table`, `@Column`)
2. Configure Hibernate (`hibernate.cfg.xml`)
3. Hibernate generates the table automatically when the app runs

## 📌 Example
```java
@Entity
@Table(name = "students")
public class Student {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private int id;

    @Column(name = "first_name")
    private String firstName;

    @Column(name = "last_name")
    private String lastName;
}
