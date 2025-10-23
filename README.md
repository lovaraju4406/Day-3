# REST API to Manage a List of Books – Explanation

This project is a simple **REST API built with Node.js and Express** to manage a list of books. It demonstrates basic CRUD operations without using a database by storing the data in memory.

---

## 📝 How the Code Works

1. **Setup and Middleware**
   - The project uses **Express.js** to create a server that listens on port 3000.
   - Middleware `express.json()` is used to parse incoming JSON request bodies.

2. **In-Memory Data Storage**
   - Books are stored in a simple **array of objects**, where each book has an `id`, `title`, and `author`.
   - Since no database is used, the data resets whenever the server restarts.

3. **GET /books**
   - This endpoint retrieves **all books** from the in-memory array.
   - It responds with a JSON array containing all book objects.

4. **POST /books**
   - This endpoint allows adding a **new book**.
   - The request body should contain `title` and `author`.
   - A new `id` is automatically generated based on the current array length.
   - Returns the newly created book as JSON.

5. **PUT /books/:id**
   - This endpoint updates an **existing book** by its `id`.
   - The request body can contain a new `title`, `author`, or both.
   - If the book exists, it updates the fields and returns the updated book.
   - If the book is not found, it returns a 404 error.

6. **DELETE /books/:id**
   - This endpoint removes a book from the array by its `id`.
   - If the book exists, it is deleted and a success message is returned along with the deleted book.
   - If the book is not found, it returns a 404 error.

7. **Starting the Server**
   - The server listens on **port 3000**, and logs a message confirming it is running.

---

## 🧭 Key Points
- Demonstrates **CRUD operations**: Create, Read, Update, Delete.
- Uses **in-memory storage**, making it simple for learning and testing.
- Allows **API testing with Postman**.
- Provides a foundation to later integrate with databases like MongoDB or MySQL.

---

## ✅ Benefits of this Approach
- Simple and lightweight for learning API basics.
- Helps understand RESTful principles and HTTP methods.
- Easy to extend with additional features like validation, authentication, or persistent storage.

---

This project is a great starting point for building more complex **Node.js APIs** and learning how to manage server-side data efficiently.
