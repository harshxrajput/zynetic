# 📚 Bookstore RESTful API (Spring Boot)

A simple bookstore backend built using Java Spring Boot with basic authentication and full CRUD operations on books.

---

## 🚀 Setup Instructions

1. **Clone the repository** (or extract the ZIP if submitted via form)
2. **Open terminal** in the project directory
3. **Run the app** with:
   ```bash
   ./mvnw spring-boot:run
   ```
4. App will start at:  
   `http://localhost:8080/`

---

## 🔐 Authentication

- **Login Page**:  
  `http://localhost:8080/login`

- **Default credentials:**

  ```
  Username: user
  Password: (check console output for auto-generated password)
  ```

- Or set your own in `application.properties`:
  ```properties
  spring.security.user.name=admin
  spring.security.user.password=admin123
  ```

---

## 📘 API Endpoints

### ➕ Create a Book

```
POST /api/books
```

**Body (JSON):**

```json
{
  "title": "Clean Code",
  "author": "Robert C. Martin",
  "genre": "Programming",
  "price": 42.99
}
```

### 📚 Get All Books

```
GET /api/books
```

### 📖 Get Book by ID

```
GET /api/books/{id}
```

### ✏️ Update Book

```
PUT /api/books/{id}
```

**Body:**

```json
{
  "title": "Updated Title",
  "author": "Updated Author",
  "genre": "Drama",
  "price": 25.99
}
```

### ❌ Delete Book

```
DELETE /api/books/{id}
```

---

## 📄 Assumptions / Enhancements

- Basic Spring Security authentication is used
- In-memory H2 database (no persistence after restart)
- Future enhancements possible:
  - JWT token-based auth
  - Search & filter books by title, author, genre
  - Swagger/OpenAPI docs
  - Docker support

---

## ✅ Technologies Used

- Java 18
- Spring Boot
- Spring Security
- Spring Data JPA
- H2 Database
- Maven
