# 🛒 Electronic Store – Spring MVC Project
## 1. Prerequisites
- JDK 21 installed and set in PATH  
- Maven installed (to build project)  
- Oracle Database 21c (or MySQL/Oracle Developer) running with schema created  
- Apache Tomcat 11 installed  
## 2. Database Setup
1. Create an Oracle schema (e.g., `electronic_store`).  
2. Run the provided SQL scripts (if available) to generate tables.  
3. Update `application.properties` with your Oracle connection:  
.properties
# Oracle Database Configuration
spring.datasource.url=jdbc:oracle:thin:@localhost:1521:xe
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.datasource.driver-class-name=oracle.jdbc.driver.OracleDriver

# JPA / Hibernate Settings
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.database-platform=org.hibernate.dialect.Oracle12cDialect

3. Build the Project
Open terminal in the project folder and run:
mvn clean install

4.To Run the Application
  1.Right clcik on project 
  2.select Run As Run on Server
  3.choose Apache Tomact11 
  4.click on ok

5.Acces The Application By url:
Open Broswer  ---> http://localhost:8080/
it will show 
Customer → register/login, browse products, add to cart, place orders.
Admin → login and manage products/inventory.

6.Tech Stack:
Backend: Spring MVC, Spring Data JPA
Frontend: Thymeleaf, HTML, CSS, JS
Database: Oracle21c/mySql

7.Key Features:
->User Authentication & Management – Customers can register/login and manage their profiles.
->Admin Dashboard – Admins can add, update, and delete products.
->Product Catalog – Products are displayed with categories and search functionality.
->Shopping Cart – Users can add/remove items, update quantities, and proceed to checkout.
->Order Management – Buy flow allows customers to place orders, linked with the database.
->Database Integration – Oracle DB handles persistence of customers, products, carts, and orders.
->Frontend UI – Built with Thymeleaf + CSS/JS for dynamic and responsive pages.
8.AdditionalDetails:
->Architecture & Layers: Followed a 3-tier architecture (Controller → Service → Repository/DAO → DB) for clean separation of concerns and maintainability.
->Security: Implemented authentication and session management to secure both customer and admin actions.
->Validation: Used frontend validation (Thymeleaf + JavaScript) and backend validation (Spring Validation) to ensure data integrity.
->Database Design: Designed relational tables in Oracle (Customers, Products, Orders, CartItems, Admin) with proper foreign key relationships for referential integrity.
->Testing: Added JUnit test cases for service and repository layers to ensure data consistency.
->Deployment: Built with Maven and deployed as a WAR file on Apache Tomcat.
9. Future Enhancements
Online payment integration
Responsive frontend with Bootstrap
REST APIs for third-party integration
