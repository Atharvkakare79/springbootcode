# Spring Boot JWT Authentication – Complete Guide

This is a **complete reference** for JWT authentication in Spring Boot.  
It contains **theory**, **code blocks**, **usage**, and **best practices**.

---

## 1️⃣ What is JWT?

**JWT (JSON Web Token)** is a compact, URL-safe means of representing claims between two parties.  
It is commonly used for **stateless authentication** in web applications.

A JWT consists of three parts:

1. **Header** – contains the type of token and signing algorithm.  
2. **Payload** – contains user information (claims).  
3. **Signature** – used to verify the integrity of the token.

> JWT allows the server to **authenticate users without storing session data**.

---

## 2️⃣ pom.xml Dependencies

We need Spring Boot, Spring Security, JPA, H2 database (for demo), and jjwt library.

```xml
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-security</artifactId>
    </dependency>
    <dependency>
        <groupId>io.jsonwebtoken</groupId>
        <artifactId>jjwt</artifactId>
        <version>0.9.1</version>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    <dependency>
        <groupId>com.h2database</groupId>
        <artifactId>h2</artifactId>
        <scope>runtime</scope>
    </dependency>
</dependencies>


