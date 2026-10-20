
```markdown
# ☕ Advanced Java & Web Development Laboratory

This repository contains academic experiments, core concepts, and a complete end-to-end e-commerce web application developed using **Java EE / Jakarta EE**, **Apache Tomcat**, **Servlets**, **JavaServer Pages (JSP)**, and **MySQL**.

---

## 📂 Repository Layout

```text
JavaLab/
├── JavaProject/
│   └── ShopSphere/                  # Full-stack e-commerce project (MVC)
│       ├── pom.xml                  # Project Object Model & build configurations
│       ├── database/                # Database schemas & SQL setup scripts
│       ├── src/main/
│       │   ├── java/com/shopsphere/
│       │   │   ├── controller/      # Servlets handling requests (Auth, Cart, Orders, Admin)
│       │   │   ├── dao/             # Data Access Objects (UserDAO, ProductDAO, OrderDAO, etc.)
│       │   │   ├── desktop/         # Standalone Swing Desktop GUI (SwingInventoryViewer.java)
│       │   │   ├── filter/          # Authentication & role-based authorization filters
│       │   │   ├── listener/        # Application lifecycle & context listeners
│       │   │   ├── model/           # POJO domain entities (User, Product, Order, CartItem, etc.)
│       │   │   └── util/            # JDBC connection manager (DBConnection.java)
│       │   └── webapp/
│       │       ├── WEB-INF/         # Deployment descriptor (web.xml) & private libraries
│       │       ├── admin/           # Admin panel JSPs (dashboard, orders, products, users)
│       │       ├── fragments/       # Reusable layout JSPs (header, footer, navbar)
│       │       └── *.jsp            # Storefront views (index, cart, checkout, login, etc.)
│       └── target/                  # Maven target output (ShopSphere.war)
│
├── Lab-Experiments/
│   ├── Exp1-Tomcat-Setup/           # Static Web Application deployment on Apache Tomcat
│   │   └── MyWebApp/
│   │       └── index.html
│   ├── Exp2-Servlet-Form-Handling/  # Form parameter parsing via HttpServlet doPost/doGet
│   └── Exp7-HTML-to-JSP/            # Refactoring static UI to dynamic JSP using EL and MVC
│       ├── pom.xml
│       └── src/
│           └── main/
│               ├── java/com/servlet/HelloServlet.java
│               └── webapp/
│                   ├── student.jsp
│                   └── result.jsp
└── README.md

```

---

## 🔬 Curriculum Lab Experiments

### 1. Introduction to Apache Tomcat & Basic Web Applications

* Installation, directory structure (`bin`, `conf`, `webapps`, `logs`), and port configuration (default: `8080`).
* Deploying static web contexts and understanding URL routing (`http://localhost:8080/<ContextName>/`).

### 2. Servlet Request Processing

* Handling HTTP POST/GET requests using `HttpServletRequest` and `HttpServletResponse`.
* Retrieving submitted form parameters using `request.getParameter()`.

### 3. HTML to JSP Conversion & MVC Architecture

* Separating request processing/controller tasks (Servlets) from presentation/view rendering (JSP).
* Storing request-scoped attributes using `request.setAttribute()`.
* Forwarding execution flows via `RequestDispatcher.forward()`.
* Rendering dynamic data on the client side using Expression Language (`${...}`).

---

## 🛒 Capstone Project: ShopSphere

**ShopSphere** is an enterprise e-commerce platform built on the **Model-View-Controller (MVC)** architectural pattern.

### Features

* **User Management:** User registration, password handling, session-based authentication, and access control.
* **Product Catalog & Browsing:** Category-based product organization, detail pages, and search.
* **Shopping Cart & Checkout:** Stateful shopping cart, quantity adjustments, order placement, and order tracking.
* **Admin Dashboard (`/admin`):** Management portals for products, categories, customer orders, and registered accounts.
* **Desktop Inventory Utility:** A Java Swing GUI client (`SwingInventoryViewer.java`) for checking local stock levels directly via JDBC.

---

## 🛠️ Tech Stack & Requirements

| Layer | Technology |
| --- | --- |
| **Runtime Environment** | Java Standard Edition (JDK 17+) |
| **Servlet Specification** | Jakarta Servlet API 6.0+ |
| **Web Container / Server** | Apache Tomcat 10.1+ / 11.0+ |
| **View Layer** | JavaServer Pages (JSP), JSTL 3.0, Expression Language (EL) |
| **Database** | MySQL Server 8.0+ |
| **Database Connectivity** | MySQL Connector/J (`mysql-connector-j-8.3.0`) |
| **Build Automation** | Apache Maven |

---

## 🚀 Setup & Execution Guide

### 1. Database Initialization (For ShopSphere)

1. Open your MySQL client and execute:
```sql
CREATE DATABASE shopsphere_db;

```


2. Import the schema script located in `JavaProject/ShopSphere/database/`.
3. Update connection parameters (database URL, username, password) in:
```text
JavaProject/ShopSphere/src/main/java/com/shopsphere/util/DBConnection.java

```



### 2. Build the Application

Navigate to the desired project directory containing `pom.xml` and run:

```bash
mvn clean package

```

This will compile the classes and package a `.war` file under `target/`.

### 3. Deploy to Apache Tomcat

1. Copy the generated `.war` file into your Tomcat deployment folder:
```text
<TOMCAT_HOME>/webapps/

```


2. Start the Tomcat server:
* **Windows:** Run `<TOMCAT_HOME>\bin\startup.bat`
* **Linux/macOS:** Run `<TOMCAT_HOME>/bin/startup.sh`



### 4. Access the Applications

* **ShopSphere Storefront:** `http://localhost:8080/ShopSphere/`
* **ShopSphere Admin Panel:** `http://localhost:8080/ShopSphere/admin/dashboard.jsp`
* **Student JSP Lab:** `http://localhost:8080/servlet/student.jsp`
* **Static Tomcat Test App:** `http://localhost:8080/MyWebApp/`

```

---

Name Rajat Dwivedi

```
