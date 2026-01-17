
# Spring MVC Security with BCrypt

A secure Spring Boot web application demonstrating **Spring MVC authentication and authorization** using **Spring Security** and **BCrypt password hashing**.

This project showcases how to protect web pages with login and password hashing, using Spring Security’s `BCryptPasswordEncoder` for secure credential storage. :contentReference[oaicite:1]{index=1}

---

## 🚀 Features

- 🔒 User authentication with Spring Security
- 🔑 Secure password storage using BCrypt hashing
- 🧠 JDBC or custom UserDetailsService for user credentials
- 👤 Role-based access control (optional)
- 📄 Thymeleaf views (login page + protected pages)
- 🛡️ Session-based login/logout

---

## 🛠️ Tech Stack

| Category       | Technologies                          |
|----------------|--------------------------------------|
| Language       | Java                                 |
| Framework      | Spring Boot, Spring MVC              |
| Security       | Spring Security, BCrypt (`BCryptPasswordEncoder`) :contentReference[oaicite:2]{index=2} |
| Templating     | Thymeleaf (optional)                 |
| Build Tool     | Maven                                 |
| Version Control| Git, GitHub                          |

---

## 📁 Project Structure

```
├───Sql
│       bcrypt.sql
│       sqlscript.sql
│
├───src
│   ├───main
│   │   ├───java
│   │   │   └───com
│   │   │       └───santanu
│   │   │           └───demo
│   │   │               │   DemoSecurityApplication.java
│   │   │               │
│   │   │               ├───controller
│   │   │               │       DemoController.java
│   │   │               │       LoginController.java
│   │   │               │
│   │   │               └───security
│   │   │                       DemoSecurityConfig.java
│   │   │
│   │   └───resources
│   │       │   application.properties
│   │       │
│   │       ├───static
│   │       └───templates
│   │               access-denied.html
│   │               fancy-login.html
│   │               home.html
│   │               leaders.html
│   │               system.html
│   │
│   └───test

````

---

## 📦 Setup & Installation

### 1️⃣ Clone the repository

```bash
git clone https://github.com/santanudas042002/spring-mvc-security-bcrypt.git
cd spring-mvc-security-bcrypt
````

---

### 2️⃣ Database Configuration (Optional)


Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/your_db
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD
spring.jpa.hibernate.ddl-auto=none
```

---

### 3️⃣ Build & Run

```bash
mvn clean install
mvn spring-boot:run
```

Application starts on:

```
http://localhost:8080
```

---

## 🔐 Security Overview

### 🔑 BCrypt Password Hashing

Spring Security uses `BCryptPasswordEncoder` to hash and compare passwords securely.
BCrypt automatically generates a salt and embeds it in the hashed result, making it stronger against brute-force attacks. ([Home][3])


### 🧠 Authentication Flow

1. User accesses a protected page
2. Spring intercepts and redirects to login form
3. User enters username/password
4. Spring Security validates credentials with `UserDetailsService`
5. Password comparison uses BCrypt hashing

---

## 🖥️ Web Pages (Thymeleaf)

Commonly included views:

| Page             | Purpose                    |
| ---------------- | -------------------------- |
| `login.html`     | Custom login form          |
| `home.html`      | Public homepage            |
| `dashboard.html` | Protected page after login |

---

## 📌 Common URLs (may vary)

| Operation     | URL             |
| ------------- | --------------- |
| Login page    | `/login`        |
| Perform login | `/login` (POST) |
| Logout        | `/logout`       |

---

## 🧪 Testing

1. Start the app
2. Navigate to `/login`
3. Log in with a test user (BCrypt hashed)
4. Access secured pages

**If login redirects back to `/login` repeatedly**, ensure BCrypt hashing is configured correctly and your stored password matches the encoder. ([Stack Overflow][4])

---


## 👨‍💻 Author

**Santanu Kumar Das**
[https://github.com/santanudas042002](https://github.com/santanudas042002)

---

⭐ If you find this project helpful, consider giving it a ⭐!

```

---

### 💡 How to Customize After

Once you open your actual source code, you can add:

✔ Actual login URLs and form fields  
✔ A screenshot of login and secured pages  
✔ Example users (preloaded SQL)  
✔ Exact package names and config classes  

---

If you want, I can also generate:

🔥 A **Postman form flow guide**  
✨ **Swagger/OpenAPI documentation**  
📄 A **deployment guide** (Heroku/Railway/Vercel)
