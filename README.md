# Shopping Cart Application

A robust and feature-rich shopping cart application built with **Spring Boot** and following the **Model-View-Controller (MVC)** design pattern. This project is structured to provide seamless functionality for both users and administrators. It supports user authentication, product management, order placement, and more. 🚀

## Features

### User Features
- **Registration & Login**: 🔐 Secure authentication with role-based access control.
- **Browse Products**: 🛍️ View available products and categories.
- **Shopping Cart**: 🛒 Add, update, or remove products.
- **Order Management**: 📦 Place orders and view order history.
- **Profile Management**: 👤 Update user profile details.

### Admin Features
- **Product Management**: 🛠️ Add, update, and delete products.
- **Category Management**: 📂 Manage product categories.
- **User Management**: 👥 View and manage registered users.
- **Order Tracking**: 🚚 Monitor order statuses.

### Technical Features
- **Role-Based Access Control (RBAC)** using Spring Security.
- **Database Integration** with repositories for persistent data.
- **Responsive Design** using HTML, CSS, and Bootstrap.
- **Custom Error Handling** for a better user experience.
- **Utility Classes** for shared functionalities.

## Project Structure

### Root Directory
- **`mvnw` / `mvnw.cmd`**: Maven wrapper scripts for platform-independent builds.
- **`pom.xml`**: Project Object Model (POM) configuration file for dependency management.

### `src/main`

#### `resources`
- **`application.properties`**: Configuration file for the Spring Boot application.
- **Templates**: Thymeleaf templates for dynamic HTML views:
  - **User Templates**: `cart.html`, `home.html`, `my_orders.html`, `order.html`, `profile.html`.
  - **Admin Templates**: `users.html`, `category.html`, `products.html`, `orders.html`, etc.
  - **Common Templates**: `register.html`, `login.html`, `forgot_password.html`, etc.
- **Static Files**: CSS, JS, and images for the frontend.
  - **CSS**: `style.css`
  - **JS**: `script.js`
  - **Images**: Organized into `category_img`, `product_img`, and `profile_img` folders.

#### `java/com/ecom`
- **Application Entry Point**: `ShoppingCartApplication.java`
- **Controller Layer**: 🎮 Handles HTTP requests and maps them to services.
  - `HomeController.java`, `AdminController.java`, `UserController.java`
- **Service Layer**: 🧠 Business logic implementation.
  - `CartService`, `OrderService`, `UserService`, etc., with their `impl` subpackage for implementations.
- **Repository Layer**: 🗄️ Interfaces for database operations using Spring Data JPA.
  - `ProductRepository`, `CartRepository`, `UserRepository`, etc.
- **Model Layer**: 🧩 Data models representing the database schema.
  - `UserDtls`, `Product`, `OrderRequest`, `Cart`, etc.
- **Utility Classes**: 🛠️ Shared helper classes and constants.
  - `OrderStatus`, `AppConstant`, `CommonUtil`
- **Security Configurations**: 🔒 Spring Security setup for authentication and authorization.
  - `SecurityConfig`, `AuthSuccessHandlerImpl`, `AuthFailureHandlerImpl`, etc.

## Prerequisites

- Java 17+
- Maven 3.8+
- MySQL Database

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/parsh05-Shopping-Cart-SBMS.git
   cd parsh05-Shopping-Cart-SBMS
   ```

2. **Configure the Database**:
   Update the `application.properties` file with your database credentials:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/shopping_cart_db
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   spring.jpa.hibernate.ddl-auto=update
   ```

3. **Run the Application**:
   Use the Maven wrapper to build and start the application:
   ```bash
   ./mvnw spring-boot:run
   ```

4. **Access the Application**:
   Open your browser and go to `http://localhost:8080`.

## Technologies Used

- **Backend**: Spring Boot, Spring Security, Spring Data JPA
- **Frontend**: Thymeleaf, Bootstrap, HTML5, CSS3, JavaScript
- **Database**: MySQL
- **Build Tool**: Maven

## Future Enhancements
- Implement payment gateway integration. 💳
- Add an analytics dashboard for administrators. 📊
- Support for product reviews and ratings. ⭐
- Integration with external APIs for advanced features. 🔗

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes. 🙌

---

> **Note**: This project was inspired and developed with the help of a tutorial. Modifications and customizations have been made to suit the specific requirements of this application. 😊

Happy Coding! 💻

