# Spring Boot.

- It is an open source, microservice-based **Java** web framework. 
- It creates a fully production-ready environment that is completely configurable using its prebuilt code within its codebase
- It doesn't allow us to manually configure any configurations as it doesn't generate any XML files, but we can do this by adding our required properties in the file application.properties provided by it.
- It contains a container known as Spring Container which contains objects knows as Spring Beans.
- The run method initializes the Spring Container
- By default, it uses the concept of Singleton Design Pattern, so if you dont even create an object, it will be created before hand by it. Even if you create multiple objects, only one object will be created.
- By default, @Autowired searches for the type  

## Dependency Injection

- It is a design pattern that removes the dependency from the programming code so that it can be easy to manage and test the application. 
- Dependency Injection makes our programming code loosely coupled.
- Spring framework provides two ways to inject dependency
  - By Constructor
  - By Setter method

## JPA - Java Persistence API

- It is a specification of Java. 
- It is used to persist data between Java object and relational database. 
- JPA acts as a bridge between object-oriented domain models and relational database systems.
- As JPA is just a specification, it doesn't perform any operation by itself. It requires an implementation. So, ORM(Object Relational Mapping) tools like Hibernate, TopLink and iBatis implements JPA specifications for data persistence.

## Hibernate Framework

- It is a Java framework that simplifies the development of Java application to interact with the database. 
- It is an open source, lightweight, ORM (Object Relational Mapping) tool. Hibernate implements the specifications of JPA (Java Persistence API) for data persistence.
- The ORM tool internally uses the JDBC API to interact with the database.

![hibernate tutorial, An introduction to hibernate](https://www.javatpoint.com/images/hibernate/orm.jpg)

## Spring Boot H2 Database

- H2 is an In-memory database. It creates the configuration automatically.
- In-memory database relies on system memory as oppose to disk space for storage of data. Because memory access is faster than disk access. 
- We use the in-memory database when we do not need to persist the data. 
- The in-memory database is an embedded database. The in-memory databases are volatile, by default, and all stored data loss when we restart the application.