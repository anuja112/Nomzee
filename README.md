# 🍽️ NOMZEE

### Full-Stack Food Delivery Platform

NOMZEE is a full-stack food delivery web application that connects customers with restaurants through a simple ordering experience. Customers can browse menus, manage their cart, place orders, and track their order status, while restaurant owners can manage their restaurants and food items through a dedicated dashboard.

The application is built using **React.js, Spring Boot, REST APIs, and MySQL**, following a structured three-tier architecture.

---

## ✨ Features

### 👤 Customer

* User registration and login
* Browse available food items
* Search food items
* Add and remove items from cart
* Adjust item quantities
* View order summary
* Place orders
* Track order progress
* View previous orders

### 🏪 Restaurant / Business

* Business account registration and login
* Add and manage restaurants
* Add, edit, and delete food items
* Upload food images
* Update food prices and descriptions
* Control food availability
* View restaurant-specific food items through the dashboard

### 🔐 Authentication & Access Control

* Session-based authentication using `JSESSIONID`
* Role-based access for `CUSTOMER` and `BUSINESS`
* Protected business operations
* CORS configuration between frontend and backend

---

## 🛠️ Tech Stack

| Category    | Technology                 |
| ----------- | -------------------------- |
| Frontend    | React.js, Vite             |
| Routing     | React Router               |
| Styling     | CSS                        |
| HTTP Client | Axios                      |
| Backend     | Spring Boot                |
| Language    | Java 17                    |
| API         | REST API                   |
| ORM         | Spring Data JPA, Hibernate |
| Database    | MySQL                      |
| Build Tool  | Maven                      |
| API Testing | Postman                    |

---

## 🏗️ Architecture

NOMZEE follows a **three-tier architecture**:

```text
┌──────────────────────────┐
│        React.js          │
│       Presentation       │
└────────────┬─────────────┘
             │ REST API
             ▼
┌──────────────────────────┐
│       Spring Boot        │
│    Business / Services   │
└────────────┬─────────────┘
             │ JPA / Hibernate
             ▼
┌──────────────────────────┐
│          MySQL           │
│       Data Layer         │
└──────────────────────────┘
```

This separation keeps the frontend, application logic, and database operations organized and maintainable.

---

## 📁 Project Structure

```text
NOMZEE/
│
├── Backend/
│   └── OnlineFoodApp/
│       └── src/
│           └── main/
│               ├── java/
│               │   └── com/example/foodapp/
│               │       ├── config/
│               │       ├── controller/
│               │       ├── entity/
│               │       ├── repository/
│               │       └── service/
│               │
│               └── resources/
│
├── Frontend/
│   ├── public/
│   └── src/
│       ├── components/
│       ├── App.jsx
│       ├── App.css
│       └── index.css
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have installed:

* Java 17+
* Maven 3.8+
* Node.js 18+
* MySQL 8.0+

### 1. Clone the Repository

```bash
git clone https://github.com/anuja112/NOMZEE.git
cd NOMZEE
```

### 2. Create the Database

Open MySQL and create the database:

```sql
CREATE DATABASE nomzee;
```

### 3. Configure the Backend

Open the backend `application.properties` file and configure your MySQL credentials:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/nomzee
spring.datasource.username=root
spring.datasource.password=yourpassword

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 4. Start the Backend

```bash
cd Backend/OnlineFoodApp
mvn spring-boot:run
```

The backend will run on:

```text
http://localhost:8080
```

### 5. Start the Frontend

Open another terminal:

```bash
cd Frontend
npm install
npm run dev
```

The frontend will run on:

```text
http://localhost:5173
```

---

## 📡 REST API

| Method | Endpoint            | Purpose                 |
| ------ | ------------------- | ----------------------- |
| POST   | `/auth/register`    | Register a user         |
| POST   | `/auth/login`       | Authenticate a user     |
| GET    | `/food/all`         | Get all food items      |
| POST   | `/food/add`         | Add a food item         |
| PUT    | `/food/update/{id}` | Update a food item      |
| DELETE | `/food/delete/{id}` | Delete a food item      |
| POST   | `/restaurant/add`   | Add a restaurant        |
| GET    | `/restaurant/all`   | Get all restaurants     |
| GET    | `/restaurant/my`    | Get owner's restaurants |
| POST   | `/cart/add`         | Add item to cart        |
| GET    | `/cart/view`        | View cart               |
| POST   | `/order/place`      | Place an order          |

---

## 🗄️ Database

The application uses MySQL with JPA/Hibernate.

Main entities include:

```text
User
 ├── Restaurant
 ├── CartItem
 └── Order

Restaurant
 └── FoodItem
```

The database maintains relationships between users, restaurants, food items, carts, and orders.

---

## 📸 Screenshots

### Home Page

<!-- Add screenshot here -->

### Menu

<!-- Add screenshot here -->

### Cart & Order Summary

<!-- Add screenshot here -->

### Business Dashboard

<!-- Add screenshot here -->

---

## 🔮 Future Improvements

* JWT-based authentication
* Password hashing with Spring Security
* Online payment integration
* Cloud-based image storage
* Real-time order tracking
* Admin dashboard
* Food categories and advanced search
* Ratings and reviews
* Mobile application

---

## 👨‍💻 Contributors

**Anuja Ghosal**
[LinkedIn](https://www.linkedin.com/in/anuja-ghosal-10b10b2b2/)

**Debayan Sarkar**
[LinkedIn](https://www.linkedin.com/in/d3bayansarkar/)

---

## 📄 License

This project is developed for educational and portfolio purposes.
