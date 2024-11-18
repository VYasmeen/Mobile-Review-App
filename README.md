# **Movie Review Application**

A full-stack application for managing movies and their reviews. The backend is built using **Spring Boot** and **Jdbi**, offering a modular and scalable architecture to handle CRUD operations for movies and reviews.

---

## **Features**

- **Movies**:
  - View all movies.
  - Get details of a specific movie.
  
- **Reviews**:
  - Add a new review for a movie.
  - View all reviews for a specific movie.
  - Update an existing review.
  - Delete a review.

---

## **Technologies Used**

### **Backend**
- **Java 17**
- **Spring Boot**:
  - REST API
  - Dependency Injection
- **Jdbi**: Database interactions with SQL.
- **H2 Database** (or any configured database).
- **Tomcat**: Embedded web server.

### **Build Tool**
- **Maven**

---

## **Setup and Installation**

### **Prerequisites**
- Install **Java 17** or higher.
- Install **Maven**.
- Optionally, set up a relational database (e.g., MySQL, PostgreSQL).

### **Steps to Run the Application**

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/movie-review.git
   cd movie-review
   ```

2. Build the project:
   ```bash
   mvn clean install
   ```

3. Run the application:
   ```bash
   mvn spring-boot:run
   ```

4. Access the application:
   - Backend API runs by default on [http://localhost:8080](http://localhost:8080).

---

## **API Endpoints**

### **Movies**
| Method | Endpoint         | Description                      |
|--------|------------------|----------------------------------|
| GET    | `/movies/`       | Fetch all movies.               |
| GET    | `/movies/{id}`   | Fetch details of a specific movie. |

### **Reviews**
| Method | Endpoint                 | Description                            |
|--------|--------------------------|----------------------------------------|
| POST   | `/review/add`            | Add a new review.                     |
| GET    | `/review/{movieId}`      | Fetch all reviews for a specific movie.|
| PUT    | `/review/{reviewId}`     | Update a specific review.             |
| DELETE | `/review/{reviewId}`     | Delete a specific review.             |

---

## **Database Structure**

### **Movie Table**
| Column       | Type        | Description                |
|--------------|-------------|----------------------------|
| `id`         | INT         | Primary Key                |
| `name`       | VARCHAR     | Name of the movie          |
| `description`| VARCHAR     | Description of the movie   |
| `bannerUrl`  | VARCHAR     | URL of the movie's banner  |

### **Review Table**
| Column       | Type        | Description                  |
|--------------|-------------|------------------------------|
| `reviewId`   | INT         | Primary Key                  |
| `movieId`    | INT         | Foreign Key referencing `Movie` |
| `review`     | VARCHAR     | Review content              |
| `rating`     | INT         | Rating for the movie         |

---

## **Future Enhancements**
- Implement user authentication and authorization.
- Add pagination for reviews and movies.
- Introduce advanced search and filter options.
- Deploy the application on a cloud service (e.g., AWS, Azure).

---

## **Contributing**

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your message here"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature
   ```
5. Submit a pull request.

---

## **Contact**

For questions or feedback, feel free to reach out:

- **Name**: Yasmeen  
- **Email**: [vyasmeen333@example.com]  
- **GitHub**: [https://github.com/<your-username>](https://github.com/VYasmeen)

---
