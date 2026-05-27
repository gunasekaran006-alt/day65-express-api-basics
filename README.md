# Day 65: Express.js API Basics (MVC Architecture)

A simple, beginner-friendly Express.js REST API that demonstrates how to handle `GET` and `POST` requests. This project follows the **MVC (Model-View-Controller)** pattern and uses an in-memory JavaScript array as a temporary database.

---

## 🏗️ Backend Architecture

The project is structured logically to separate concerns:
* **Model (`models/`)**: Manages the data structure and acts as a temporary database array.
* **Controller (`controllers/`)**: Contains the application logic for fetching and adding products.
* **Routes (`routes/`)**: Maps the URLs/endpoints to the respective controller functions.
* **Main (`main.js`)**: Entry point that configures Express and starts the server.

---

## 🛠️ Project Setup Steps

Follow these steps to create and run this backend application from scratch:

### 1. Initialize Project
Create a new folder, navigate inside it, and initialize npm:
```bash
npm init -y
```

### 2. Configure package.json
Open `package.json` and change the `"main"` entry point from `"index.js"` to `"main.js"`.

### 3. Install Dependencies
Install Express (Production) and Nodemon (Development):
```bash
npm i express
npm i -D nodemon
```

### 4. Setup Gitignore
Create a `.gitignore` file and add the following to ignore node modules:
```text
node_modules/
```

### 5. Add Start Script
Add a `dev` script inside the `"scripts"` block in your `package.json`:
```json
"scripts": {
  "dev": "nodemon main.js"
}
```

### 6. Start the Server
Run the application using nodemon:
```bash
npm run dev
```

---

## 🗺️ API Endpoints

The server runs on port `8080` by default (`http://localhost:8080`).

### 1. Get All Products
* **Endpoint:** `/products`
* **Method:** `GET`
* **Response (Empty):** `{"message": "No Products Added"}`
* **Response (Success):** Array of product objects.

### 2. Create a Product
* **Endpoint:** `/create`
* **Method:** `POST`
* **Headers:** `Content-Type: application/json`
* **Request Body:**
  ```json
  {
    "title": "Smart Watch",
    "price": 2999,
    "category": "Electronics"
  }
  ```
* **Response:** `{"message": "Product Added"}`

---

## 📁 Folder Structure

```text
├── controllers/
│   └── products.controller.js
├── models/
│   └── products.model.js
├── routes/
│   └── products.routes.js
├── .gitignore
├── main.js
├── package.json
└── README.md
```
